---
description: Verteilungsoptionen beim Freigeben einer App mit Microsoft Edge WebView2
title: Verteilung von Microsoft Edge WebView2-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, Webview2, Webview, wpf-Apps, Wpf, Microsoft Edge, ICoreWebView2, ICoreWebView2Host, Browsersteuerung, Edge-HTML
ms.openlocfilehash: 97ede968e066c572bb1b22e10ed7e758e38e3ca4
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535699"
---
# <a name="distribution-of-apps-using-webview2"></a>Verteilung von Apps mit WebView2  

Stellen Sie beim Verteilen Ihrer WebView2-App sicher, dass die unterstützende Webplattform, die [WebView2 Runtime][Webview2Installer], vorhanden ist, bevor die App gestartet wird.  In diesem Artikel wird beschrieben, wie Sie (der Entwickler) die WebView2 Runtime installieren und die beiden Verteilungsmodi für Ihre WebView2-App verwenden: [Evergreen](#evergreen-distribution-mode) und [Fixed Version](#fixed-version-distribution-mode).  

## <a name="evergreen-distribution-mode"></a>Evergreen Verteilungsmodus  

> [!NOTE]
> Der Evergreen-Verteilungsmodus wird für die meisten Entwickler empfohlen.  

Der Evergreen-Verteilungsmodus stellt sicher, dass Ihre App die neuesten Funktionen und Sicherheitsupdates nutzt.  Er hat die folgenden Eigenschaften.  

*   Die zugrunde liegende Webplattform \(WebView2 Runtime\) wird ohne zusätzlichen Aufwand automatisch aktualisiert.  
*   Alle Apps, die den Evergreen-Verteilungsmodus verwenden, verwenden eine gemeinsam genutzte Kopie der Evergreen WebView2-Runtime, wodurch Speicherplatz gespart wird.  
    
### <a name="understanding-the-webview2-runtime"></a>Grundlegendes zur WebView2 Runtime  

Die WebView2-Runtime ist eine weiterverteilbare Runtime und dient als unterstützende Webplattform für WebView2-Apps.  Das Konzept ähnelt Visual C++ oder der .NET Runtime für C++/.NET-Apps.  Die Runtime enthält modifizierte Microsoft Edge \(Chromium\)-Binärdateien, die optimiert und für Apps getestet wurden.  Die Runtime wird bei der Installation nicht als vom Benutzer sichtbarer Browser angezeigt.  Beispielsweise verfügt ein Benutzer nicht über eine Browser-Desktop-Verknüpfung oder einen Startmenüeintrag.  

Während der Entwicklung und des Testens können Sie beide als Backing-Webplattform verwenden.  

*   Die WebView2 Runtime  
*   Beliebiger Insider \(nicht stabil\) Microsoft Edge \(Chromium\) Browserkanal  
    
In Produktionsumgebungen müssen Sie sicherstellen, dass die Runtime auf Benutzergeräten vorhanden ist, bevor die App gestartet wird.  Der Microsoft Edge Stable-Kanal ist für die Verwendung mit WebView2 nicht verfügbar.  Die Entscheidung verhindert, dass Apps in der Produktion von dem Browser abhängig werden.

Nehmen Sie keine Abhängigkeit vom Browser an, weil:  

*   Es ist nicht garantiert, dass Microsoft Edge \(Chromium\) auf allen Benutzergeräten vorhanden ist.  Beispielsweise verfügen Geräte, die von Windows Update getrennt oder nicht direkt von Microsoft verwaltet werden (ein großer Teil des Enterprise- und EDU-Marktes), möglicherweise nicht über den Browser.  Da Sie die WebView2 Runtime verteilen können, wird vermieden, dass eine Abhängigkeit vom Browser als Voraussetzung für Apps erforderlich ist.  
*   Browser und Apps haben unterschiedliche Anwendungsfälle. Wenn Sie also von einem Browser abhängig sind, kann dies unbeabsichtigte Nebenwirkungen auf Ihre Apps haben.  Beispielsweise können IT-Administratoren den Browser aus Gründen der internen Website-Kompatibilität versionieren.  Mit der WebView2 Runtime können Apps immer am Laufen bleiben, während Browser-Updates aktiv verwaltet werden.  
*   Im Gegensatz zum Browser wurde die Runtime für App-Szenarien entwickelt und getestet und kann in einigen Fällen Fehlerbehebungen enthalten, die im Browser noch nicht verfügbar sind.  
    
In Zukunft plant Evergreen WebView2 Runtime die Auslieferung zukünftiger Windows-Versionen.  Stellen Sie die Runtime mit Ihrer Produktions-App bereit, bis die Runtime universeller verfügbar ist.  

### <a name="deploying-the-evergreen-webview2-runtime"></a>Bereitstellen der Evergreen WebView2 Runtime  

Für alle Evergreen-Apps auf dem Gerät ist nur eine Installation der Evergreen WebView2 Runtime erforderlich.  Auf der [Download-Seite von WebView2 Runtime][Webview2Installer] stehen eine Reihe von Tools zur Verfügung.  Mit den folgenden Tools können Sie die Evergreen Runtime bereitstellen.  

*   WebView2 Runtime Bootstrapper ist ein winziges \(ca. 2 MB \) Installationsprogramm.  WebView2 Runtime Bootstrapper lädt die Evergreen Runtime von Microsoft-Servern, die der Gerätearchitektur des Benutzers entsprechen, herunter und installiert sie.  
*   Verwenden Sie einen Link, um den Bootstrapper programmgesteuert herunterzuladen.  
*   WebView2 Runtime Standalone Installer ist ein vollständiges Installationsprogramm, das Evergreen WebView2 Runtime in Offline-Umgebungen installiert.  
    
Derzeit unterstützen sowohl der Bootstrapper als auch das Standalone-Installationsprogramm nur Installationen pro Computer, für die eine Erhöhung erforderlich ist.  Wenn ein Installationsprogramm ohne Erhöhung ausgeführt wird, wird der Benutzer aufgefordert, die Berechtigungen zu erhöhen.  

Verwenden Sie die folgenden Workflows, um sicherzustellen, dass die Runtime bereits vor dem Start Ihrer App installiert ist.  Sie können Ihren Workflow je nach Szenario anpassen.  Der Beispielcode ist im [Beispiel-Repository][GitHubMicrosoftedgeWebView2samplesWebview2Deployment] verfügbar.  

#### <a name="online-only-deployment"></a>Nur Onlinebereitstellung  

Wenn Sie ein reines Online-Bereitstellungsszenario haben, bei dem davon ausgegangen wird, dass Benutzer über einen Internetzugang verfügen, führen Sie die folgenden Schritte aus.  

1.  Stellen Sie während des App-Setups sicher, dass die Runtime bereits installiert ist.  Führen Sie zur Überprüfung eine der folgenden Aktionen aus.  
    *   Überprüfen Sie, ob der `pv (REG_SZ)` Regkey vorhanden und nicht `null` oder leer ist.  Suchen Sie `pv (REG_SZ)` am folgenden Ort.  
        
        Unter 64-Bit-Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        Unter 32-Bit-Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Führen [Sie GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] aus, und stellen Sie sicher, dass der `versionInfo` `NULL` ist.  
1.  Wenn die Runtime nicht installiert ist, können Sie den Bootstrapper über den Link programmgesteuert herunterladen.  
1.  Rufen Sie den Bootstrapper von einem erhöhten Prozess oder einer Eingabeaufforderung mit `MicrosoftEdgeWebview2Setup.exe /silent /install` für eine unbeaufsichtigte Installation auf.  
    
Der vorherige Workflow bietet die folgenden Vorteile.  

*   Installieren Sie die Runtime nur bei Bedarf oder wenn Sie keine Installationsprogramme packen müssen.  
*   Der Bootstrapper erkennt automatisch die Gerätearchitektur und installiert die entsprechende Runtime.  
*   Installieren Sie die Runtime im Hintergrund.  
    
Sie können den Bootstrapper auch mit Ihrer App packen, anstatt ihn bei Bedarf programmgesteuert herunterzuladen.  

#### <a name="offline-deployment"></a>Offlinebereitstellung  

Wenn Sie ein Offline-Bereitstellungsszenario haben, in dem die App-Bereitstellung vollständig offline funktionieren muss, führen Sie die folgenden Schritte aus.  

1.  Laden Sie das [eigenständige Installationsprogramm][Webview2Installer] herunter.  
1.  Fügen Sie das Installationsprogramm in Ihr App-Installationsprogramm oder Ihren Updater ein.  
1.  Stellen Sie während des App-Setups sicher, dass die Runtime bereits installiert ist.  Führen Sie zur Überprüfung eine der folgenden Aktionen aus.  
    *   Überprüfen Sie, ob der `pv (REG_SZ)` Regkey vorhanden und nicht `null` oder leer ist.  Suchen Sie `pv (REG_SZ)` am folgenden Ort.  
        
        Unter 64-Bit-Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        Unter 32-Bit-Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Führen [Sie GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] aus, und stellen Sie sicher, dass der `versionInfo` `NULL` ist.  
1.  Wenn die Runtime nicht installiert ist, führen Sie das eigenständige Installationsprogramm aus.  Wenn Sie eine Installation im Hintergrund ausführen möchten, führen Sie das Installationsprogramm entweder über einen erhöhten Prozess aus oder kopieren Sie den folgenden Befehl und führen Sie ihn aus.  
    
    ```shell
    MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install
    ```  
    
### <a name="stay-compatible-in-evergreen-mode"></a>Im Evergreen-Modus kompatibel bleiben  

Das Web entwickelt sich ständig weiter.  Die Evergreen WebView2 Runtime wird auf dem neuesten Stand gehalten, um Ihnen die neuesten Funktionen und Sicherheitskorrekturen bereitzustellen.  Um sicherzustellen, dass Ihre App mit dem Web kompatibel bleibt, sollten Sie eine Testinfrastruktur einrichten.  

Nicht stabile Microsoft Edge-Kanäle \(Beta/Dev/Canary\) bieten einen kleinen Einblick in die nächsten Schritte in WebView2 Runtime.  Genau wie beim Entwickeln von Websites für Microsoft Edge sollten Sie Ihre WebView2-App regelmäßig testen.  Testen Sie Ihre WebView2-App anhand eines der nicht stabilen Kanäle und aktualisieren Sie Ihre App oder [melden Sie Probleme][GithubMicrosoftedgeWebviewfeedback], wenn Probleme auftreten. Normalerweise sind Dev und Beta die empfohlenen Kanäle.  Navigieren Sie zur [Übersicht über die Microsoft Edge-Kanäle][DeployEdgeMicrosoftEdgeChannels], um zu entscheiden, welcher Kanal richtig ist.  Sie können den [nicht stabilen Microsoft Edge-Kanal][DownloadNonstableEdge] in Ihre Testumgebung herunterladen und `regkey` oder Umgebungsvariablen verwenden, um die Kanalpräferenz für Ihre Test-App anzugeben.  Weitere Informationen finden Sie unter [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions].  Sie können [WebDriver][HowToWebdriver] auch verwenden, um WebView2-Tests zu automatisieren.

## <a name="fixed-version-distribution-mode"></a>Verteilungsmodus "Fixierte Version"   

In eingeschränkten Umgebungen mit strengen Kompatibilitätsanforderungen sollten Sie den Verteilungsmodus "Fixierte Version" verwenden.  Wählen Sie eine bestimmte Version von WebView2 Runtime aus und packen Sie sie im Verteilungsmodus "Fixierte Version".  Sie können den Zeitpunkt der Runtime-Aktualisierungen für Ihre App festlegen.  Der Verteilungsmodus für Fixierte Versionen erhält keine automatischen Updates. Planen Sie, Ihre App und die Runtime zu aktualisieren.  

> [!NOTE] 
> Der Verteilungsmodus für die Fixierte Version wurde zuvor als "Bring-Your-Own" bezeichnet.  

Führen Sie die folgenden Aktionen aus, um den Modus "Fixierte Version" zu verwenden

1.  [Laden Sie][Webview2Installer] das Paket Fixierte Version herunter. 
1.  Dekomprimieren Sie das Paket über die Befehlszeile `expand {path to the package} -F:* {path to the destination folder}` oder mit Tools wie WinRAR. Vermeiden Sie das Dekomprimieren über den Datei-Explorer, da möglicherweise nicht die richtige Ordnerstruktur generiert wird.  
1.  Fügen Sie die dekomprimierten Binärdateien der Fixierten Version in Ihr Projekt ein.  
1.  Geben Sie beim Erstellen der WebView2-Umgebung den Pfad zu den Binärdateien mit der Fixierten Version an.  
    *   Für Win32 C/C++ können Sie die Umgebung mit der Funktion [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions] erstellen.  Verwenden Sie den `browserExecutableFolder` Parameter, um den Pfad zu dem Ordner anzugeben, der `msedgewebview2.exe` enthält.  
    *   Für .NET können Sie eine der folgenden Optionen ausführen, um die Umgebung anzugeben.  
        
        > [!NOTE]
        > Sie müssen die Umgebung angeben, bevor die WebView2-Eigenschaft `Source` wirksam wird.  
        
        *   Legen Sie `CreationProperties` die Eigenschaft \([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]\) für das WebView2-Element fest.  Verwenden Sie das `BrowserExecutableFolder` Element in der Klasse `CoreWebView2CreationProperties` \([WPF][ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinForms]\), um den Pfad zu den Binärdateien für Fixierte Version anzugeben.  
        *   Verwenden `EnsureCoreWebView2Async` Sie \([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async] / [WinForms][ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]\), um die Umgebung anzugeben.  Verwenden Sie `browserExecutableFolder` den Parameter in [CoreWebView2Environment.CreateAsync,][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync] um den Pfad zu den Binärdateien für die Fixierte Version anzugeben.  
1.  Packen und versenden Sie die Binärdateien der Fixierten Version mit Ihrer App.  Aktualisieren Sie die Binärdateien entsprechend.  
    
### <a name="known-issues-for-fixed-version"></a>Bekannte Probleme für die Fixierte Version  

Im Vergleich zur Evergreen Runtime verfügt die Fixierte Version über keinen Installationsprozess, sodass [Microsoft PlayReady][MicrosoftPlayReady] nicht ohne Änderungen funktioniert.  Sie können das Problem beheben, indem Sie die folgenden Aktionen ausführen.  

1.  Suchen Sie den Pfad, in dem Sie das Paket mit der Fixierten Version auf dem Gerät des Benutzers bereitstellen, z. B. den folgenden Speicherort.
    
    ```text
    D:\myapp\Microsoft.WebView2.FixedVersionRuntime.87.0.664.8.x64
    ```  
    
1.  Führen Sie die folgenden Befehle auf dem Gerät des Benutzers aus.

    ```shell
    icacls {Fixed Version path} /grant *S-1-15-2-2:(OI)(CI)(RX)
    icacls {Fixed Version path} /grant *S-1-15-2-1:(OI)(CI)(RX)
    ```  

1.  PlayReady sollte jetzt auf dem Gerät des Benutzers funktionieren.  Auf der Registerkarte **Sicherheit** des Ordners **Fixierten Version**sollten Berechtigungen für `ALL APPLICATION PACKAGES` und `ALL RESTRICTED APPLICATION PACKAGES` enthalten sein.  

    :::image type="complex" source="../media/play-ready-permission.png" alt-text="Berechtigung für PlayReady" lightbox="../media/play-ready-permission.png":::
        Berechtigung für PlayReady  
    :::image-end:::  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Grundlegendes zu Browserversionen und WebView2 | Microsoft-Dokumentation"  
[HowToWebdriver]: ../how-to/webdriver.md "Automatisieren und Testen von WebView2 mit Microsoft Edge Driver | Microsoft-Dokumentation"  

[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions – Globals | Microsoft-Dokumentation"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString – Globale | Microsoft-Dokumentation"  

[DeployEdgeMicrosoftEdgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft-Dokumentation"  

[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.createasync "CreateAsync – Microsoft.Web.WebView2.Core.CoreWebView2Environment-Klasse | Microsoft-Dokumentation"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "EnsureCoreWebView2Async -Microsoft.Web.WebView2.Wpf.WebView2 Klasse | Microsoft-Dokumentation"  
[ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "EnsureCoreWebView2Async – Microsoft.Web.WebView2.WinForms.WebView2 Klasse | Microsoft-Dokumentation"  
[ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.corewebview2creationproperties "CoreWebView2CreationProperties – Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties Klasse | Microsoft-Dokumentation"  
[ReferenceWinFormsMicrosoftWebWebview2WinForms]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft.Web.WebView2.WinForms Klasse | Microsoft-Dokumentation"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.webview2.creationproperties "CreationProperties – Microsoft.Web.WebView2.Wpf.WebView2 Klasse | Microsoft-Dokumentation"  
[ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Microsoft.Web.WebView2.WinForms.WebView2 Klasse | Microsoft-Dokumentation"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installationsprogramm | Microsoft Entwickler"  

[DownloadNonstableEdge]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback | GitHub"  

[GitHubMicrosoftEdgeWebView2SamplesWebview2Deployment]: https://github.com/MicrosoftEdge/WebView2Samples#webview2-deployment "WebView2-Bereitstellung – MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftPlayReady]: https://www.microsoft.com/playready "Microsoft PlayReady"  
