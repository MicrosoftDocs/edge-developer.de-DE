---
description: Versionshinweise für Microsoft Edge WebView2 SDK
title: Versionshinweise für Microsoft Edge WebView2 für Win32, WPF und WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html
ms.openlocfilehash: 2c07430668b269dcada16c96045022fd68398508
ms.sourcegitcommit: 0e67a56b9dc1f7a86924d142db0efd36fd99d38b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "11608681"
---
# <a name="release-notes-for-webview2-sdk"></a>Versionshinweise für WebView2 SDK  

Das WebView2-Team aktualisiert das [WebView2 SDK][NuGetGallery] in einem Sechs-Wochen-Rhythmus.  Überprüfen Sie den folgenden Inhalt, um aktuelle Informationen zu Produktankündigungen, Ergänzungen, Änderungen und grundlegenden Änderungen an den APIs zu suchen.  

> [!NOTE]
> Stellen Sie sicher, dass Sie Ihre App nach dem Aktualisieren des NuGet-Pakets erneut kompilieren.  Das WebView-Team empfiehlt die Verwendung des Canary-Kanals bei der Entwicklung mithilfe der Vorabversionspakete und der Evergreen WebView2 Runtime, wenn Sie die Releasepakete verwenden.  Navigieren Sie zu [übereinstimmenden WebView2-Runtime-Versionen,][Webview2ConceptsVersioningMatchingWebview2RuntimeVersions]um weitere Informationen zu erfahren.  

> [!NOTE]
> WebView2-Fehlerbehebungen sind laufzeit- oder SDK-spezifisch.  

## <a name="10902-prerelease"></a>1.0.902-prerelease

Veröffentlichungsdatum: 1. Juni 2021  

[NuGet-Paket][NuGetGallery1.0.902-prerelease] \| Mindestens Microsoft Edge zu ladende Version: 86.0.616.0 oder höher \| Vollständige API-Kompatibilität: 92.0.902.0 oder höher  

### <a name="general"></a>Allgemein  
*   Verbesserte WebView2-Startleistung und Datenträgerbedarf.

#### <a name="experimental-features"></a>Experimentelle Features  

*   [IsSwipeNavigationEnabled-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalsettings5ViewWebview210902PrereleaseGetIsswipenavigationenabled] hinzugefügt, um die Möglichkeit des Endbenutzers zu aktivieren oder zu deaktivieren, die Wischbewegung auf Geräten mit Toucheingaben zu verwenden, um in WebView2 zu navigieren.
*   [BrowserProcessExited-Ereignis hinzugefügt.][Webview2ReferenceWin32Icorewebview2experimentalenvironment4ViewWebview210902PrereleaseAddBrowserprocessexited]
*   [Add_ClientCertificateRequested-API][Webview2ReferenceWin32Icorewebview2experimental3ViewWebview210902PrereleaseAddClientcertificaterequested]hinzugefügt. Es ermöglicht, bei Bedarf eine Aufforderung zum Dialogfeld "Clientzertifikat" anzuzeigen, und ermöglicht den Zugriff auf erforderliche Metadaten, um die Standardmäßige Aufforderung zum Clientzertifikat zu ersetzen.

#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Behebung eines Fehlers, bei dem das Kontextmenü durch Klicken mit der mauslinken Maustaste nicht geschlossen wird. Diese Änderung ist laufzeitspezifisch.
*   Ein Fehler wurde behoben, bei dem die WebView2-Erstellung fehlschlägt, wenn Exe-Dateien für Apps, die denselben Benutzerdatenordner freigeben, inkonsistente Versionsinformationen aufweisen.
*   Ein Fehler wurde behoben, bei dem spezielle Browserschlüssel wie Refresh, Home, Back usw. von AreBrowserAcceleratorKeysEnabled nicht deaktiviert werden können. Diese Änderung ist laufzeitspezifisch.
*   Es wurde ein Fehler in WebView2 .NET-Steuerelementen behoben, bei denen WebView2-Fenster leer sind, wenn sie im Hintergrund erstellt wurden. \([\#1077][GithubMicrosoftedgeWebviewfeedbackIssue1077]\). 
*   Das Schließen eines Dateiauswahldialogfelds durch Drücken von 'enter' oder 'esc' stürzt keine WPF-Anwendungen mehr mithilfe des WebView-Steuerelements ab. \([\#1099][GithubMicrosoftedgeWebviewfeedbackIssue1099]\). 
*   Ein Fehler wurde behoben, bei dem [AllowSingleSignOnUsingOSPrimaryAccount][Webview2ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount] nicht ordnungsgemäß mit WebView2 funktioniert, wenn ein WebResourceRequested-Ereignishandler angefügt ist. Diese Änderung ist laufzeitspezifisch. \([\#1183][GithubMicrosoftedgeWebviewfeedbackIssue1183]\).  
*   Durch das Herunterladen einer Datei wird die Transparenz von WebView2 DefaultBackgroundColor nicht mehr unterbrochen. Diese Änderung ist laufzeitspezifisch. \([\#1108][GithubMicrosoftedgeWebviewfeedbackIssue1108]\). 
*   Die Bildschirmfreigabe-Medienauswahlnachricht, die das Microsoft-Branding enthält, wurde entfernt. \([\#940][GithubMicrosoftedgeWebviewfeedbackIssue940]\). 
*   Ein Fehler im WebView2 WinForm-Steuerelement wurde behoben, bei dem das Ausblenden des übergeordneten Formulars das WebView2-Steuerelement \([\#828][GithubMicrosoftedgeWebviewfeedbackIssue828] und [\#1079][GithubMicrosoftedgeWebviewfeedbackIssue1079]\) nicht ausblendet.
*   Statische WS_CLIPCHILDREN Formatvorlage zu den WPF-Fenstern von WebView2 hinzugefügt. \([\#1013][GithubMicrosoftedgeWebviewfeedbackIssue1013]\). 
*   Es wurde ein Fehler behoben, der beim Klicken mit der rechten Maustaste auf einen Link die WebView2-Host-App abstürzte. Diese Änderung ist laufzeitspezifisch.
*   Fehler bei der Zuverlässigkeit behoben, der den Host-App-Prozess beim Wechsel zur neueren Edge WebView2 Runtime-Version abstürzen konnte.
*   **DEPRECATION:** Offiziell veraltete DefaultBackgroundColor-API für Windows 7.


#### <a name="promotions"></a>Promotions

*   [Die Download-API][Webview2ReferenceWin32Icorewebview24ViewWebview210902PrereleaseAddDownloadstarting] wird jetzt zu stabil gestuft.
*   [Die PinchZoom-API][Webview2ReferenceWin32Icorewebview2setting5ViewWebview210902PrereleaseGetIspinchzoomenabled] wird nun zu stabil gestuft.
*   [AddFrameCreated][Webview2ReferenceWin32Icorewebview24ViewWebview210902PrereleaseAddFramecreated] wird jetzt zu stabil höher gestuft.
*   [AddHostObjectToScriptWithOrigins][AddHostObjectToScriptWithOriginsAPI] API, die mit iFrame-Elementunterstützung stabil wird.
*   [Die API zum automatischen Ausfüllen][Webview2ReferenceWin32Icorewebview2setting4ViewWebview210902PrereleaseGetIsgeneralautofillenabled] wird jetzt zu stabil gestuft.
    > [!NOTE]
    > Es gibt keine aktuelle API zum Löschen der lokal gespeicherten allgemeinen Informationen zum automatischen Ausfüllen und automatischen Speichern von Kennwörtern.  Stellen Sie ein Steuerelement zum Löschen der Daten bereit, das das Löschen des gesamten Benutzerdatenordners umfasst. 



### <a name="net"></a>.NET  
    
#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Ein Fehler im WebView2 WinForm-Steuerelement wurde behoben, bei dem die Sichtbarkeit des WebView2-Fensters nach dem Löschen des übergeordneten Fensters nicht ordnungsgemäß aktualisiert wurde. \([\#1282][GithubMicrosoftedgeWebviewfeedbackIssue1282] und [\#828][GithubMicrosoftedgeWebviewfeedbackIssue828]\).
*   Es wurde ein Fehler im WebView2-WPF-Steuerelement behoben, bei dem die Quelleigenschaftsbindung im WPF OneWay-Bindungsmodus nicht ordnungsgemäß funktionierte. \([\#619][GithubMicrosoftedgeWebviewfeedbackIssue619] und [\#608][GithubMicrosoftedgeWebviewfeedbackIssue608]\).

## <a name="1086435"></a>1.0.864.35

Veröffentlichungsdatum: 31. Mai 2021  

[NuGet-Paket][NuGetGallery1.0.864.35] \| Mindestens zu ladende Laufzeitversion: 86.0.616.0 oder höher \| Vollständige API-Kompatibilität: 91.0.864.35 oder höher  

### <a name="general"></a>Allgemein  

#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Fehler bei der Zuverlässigkeit behoben, der den Host-App-Prozess beim Wechsel zur neueren Edge WebView2 Runtime-Version abstürzen konnte.
*   Es wurde ein Fehler behoben, der in einigen Situationen die Speicherbereinigung verhinderte. Diese Änderung ist laufzeitspezifisch.
*   Fehler im 818 SDK-Releasepaket behoben, bei dem das Projekt die Datei "WebView2.h" nicht finden konnte. \([\#1209][GithubMicrosoftedgeWebviewfeedbackIssue1209]\). 
*   Ein Fehler wurde behoben, der dazu führte, dass das WebResourceRequested-Ereignis für einige Anforderungen mit binären Textkörpern verworfen wurde.
*   Verbessern der NewWindowRequested-Dokumentation. \([\#448][GithubMicrosoftedgeWebviewfeedbackIssue448]\). 

#### <a name="promotions"></a>Promotions
*   [Die UserAgent-API][Webview2ReferenceWin32Icorewebview2setting2ViewWebview21086435GetUseragent] ist jetzt stabil.
*   [AreBrowserkeysenabled][Webview2ReferenceWin32Icorewebview2setting2ViewWebview21086435GetArebrowseracceleratorkeysenabled] ist jetzt stabil.

### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Fehlerbehebungen  
*   Es wurde ein Fehler in WebView2 .NET-Steuerelementen behoben, bei dem der erste Header beim Durchlaufen der CoreWebView2WebResourceRequest-Headersammlung fehlte. \([\#1123][GithubMicrosoftedgeWebviewfeedbackIssue1123]\). 

## <a name="10865-prerelease"></a>1.0.865-prerelease  

Veröffentlichungsdatum: 26. April 2021  

[NuGet-Paket][NuGetGallery1.0.865-prerelease] \| Mindestens Microsoft Edge zu ladende Version: 86.0.616.0 oder höher \| Vollständige API-Kompatibilität: 91.0.865.0 oder höher  

### <a name="general"></a>Allgemein  

#### <a name="experimental-features"></a>Experimentelle Features  

*   [IsPinchZoomEnabled-Einstellung][Webview2ReferenceWin32Icorewebview2experimentalsettings4ViewWebview210865PrereleaseIspinchzoomenabled] hinzugefügt. Sie können das Zoomsteuerelement für die Seitenskala in einer Einstellung aktivieren oder deaktivieren.  
*   Benutzerdefinierte [add_DownloadStarting-API][Webview2ReferenceWin32Icorewebview2experimental2ViewWebview210865PrereleaseAddDownloadstarting] hinzugefügt.  Sie können Downloads blockieren, in einem anderen Pfad speichern und auf die erforderlichen Metadaten zugreifen, um eine benutzerdefinierte Download-Benutzeroberfläche zu erstellen.  
*   `iframe`Elementunterstützung von [AddHostObjectToScriptWithOrigins][Webview2ReferenceWin32Icorewebview2experimentalframeViewWebview210865PrereleaseAddhostobjecttoscriptwithorigins]hinzugefügt.  
*   Beispielcode für [WPF-Beispiel-App][GithubMicrosoftedgeWebview2samplesWebview2wpfbrowser] hinzugefügt, um die API zum Deaktivieren von Browserfunktionsschlüsseln zu verwenden.  
*   Die [UpdateRuntime-API][Webview2ReferenceWin32Icorewebview2experimentalenvironment3ViewWebview210865PrereleaseUpdateruntime] wurde hinzugefügt, um die WebView2-Runtime einfach zu aktualisieren.  
    
#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Der Handler für eine `Chromium DevTools Protocol` Nachricht mit `POST` binären Daten in WebView2 wurde behoben.  
*   Die `OpenSaveAsAwareness` Download-Benutzeroberfläche wurde deaktiviert, da sie Links zu `edge://settings` enthält.  \([\#1120][GithubMicrosoftedgeWebviewfeedbackIssue1120]\).  
*   Das Branding wurde aus dem Dialogfeld "Bildschirmfreigabe" entfernt.  \([\#940][GithubMicrosoftedgeWebviewfeedbackIssue940]\).  
*   Fehler wurde behoben, bei dem die [SetWindowDisplayAffinity-Funktion][WindowsWin32ApiWinuserSetWindowDisplayAffinity] WebView2 unterbricht, als die Bildschirmaufnahme in einer WebView2-App beendet wurde.  \([\#841][GithubMicrosoftedgeWebviewfeedbackIssue841]\).
*   Fehler beim Hosten der Komposition behoben, bei dem die Mauseingabe nicht mehr funktionierte, wenn eine Stifteingabe an WebView2 gesendet wurde.  
*   Fehler wurde behoben, der die Mauseingabe nach jeder Stifteingabe unterbricht.  Diese Änderung ist laufzeitspezifisch.  
    
### <a name="net"></a>.NET  

#### <a name="experimental-features"></a>Experimentelle Features  

*   WebView2-Designertool zur WPF-Toolbox hinzugefügt.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   WebView2 UI-Element im .NET Designer-Modus hinzugefügt.  
    
#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Verbesserte COM-Ausnahmebeschreibungen durch Umschließen einer detaillierteren .NET-Ausnahme.  \([\#338][GithubMicrosoftedgeWebviewfeedbackIssue338]\).  Diese Änderung ist laufzeitspezifisch.  
*   Fehler behoben, der verursacht wurde, wenn Sie den `tab` Fokus verlagern, was dazu führte, dass das WebView2-Steuerelement in Microsoft Visual Studio Tools für Office abstürzte.  \([\#589][GithubMicrosoftedgeWebviewfeedbackIssue589] und [\#933][GithubMicrosoftedgeWebviewfeedbackIssue933]\).  Diese Änderung ist laufzeitspezifisch.  
*   Verbessertes .NET Framework-Ladeprogramm nach unten, um robuster zu sein.  \([\#946][GithubMicrosoftedgeWebviewfeedbackIssue946]\).
*   Es wurde ein Fehler behoben, der zu einem Absturz führte, wenn Sie versuchen, die Aktualisierung vor Abschluss der ersten Navigation zu versuchen.  \([\#1011][GithubMicrosoftedgeWebviewfeedbackIssue1011]\).
*   Die Initialisierung wurde behoben, sodass die Navigation während der `CoreWebView2InitializationCompleted` .  \([\#1050][GithubMicrosoftedgeWebviewfeedbackIssue1050]\).
*   Verbesserte Fehlerbehandlung bei .NET-Browserprozessabstürzen.  Sie können nun Steuerelemente neu erstellen, nachdem Sie ein Ereignis ohne Absturz behandelt `ProcessFailed` haben.  \([\#996][GithubMicrosoftedgeWebviewfeedbackIssue996]\).  
    
## <a name="1081841"></a>1.0.818.41  

Veröffentlichungsdatum: 21. April 2021  

[NuGet-Paket][NuGetGallery1.0.818.41] \| Mindestens zu ladende Laufzeitversion: 86.0.616.0 oder höher \| Vollständige API-Kompatibilität: 90.0.818.41 oder höher  

### <a name="general"></a>Allgemein  

#### <a name="features"></a>Features  

*   Das Ereignis wurde `ProcessFailed` erweitert.  Sie wird jetzt für untergeordnete Prozesse und Framerenderer, die keine Renderer sind, ausgelöst.  
*   `iframe`Elementunterstützung für `AddScriptToExecuteOnDocumentCreated` hinzugefügt.  
*   Verbesserter WebView2-Code, um stabiler für `.exe` Anwendungsdateien mit falsch formatierten Versionsinformationen zu sein.  \([\#850][GithubMicrosoftedgeWebviewfeedbackIssue850]\).  
*   Aus `--winhttp-proxy-resolver` der Befehlszeile des WebView-Browserprozesses entfernt, andere Proxy-Befehlszeilenoptionen für WebView2 aktiviert.  
    
## <a name="10824-prerelease"></a>1.0.824-prerelease  

Veröffentlichungsdatum: 8. März 2021  

[NuGet-Paket][NuGetGallery1.0.824-prerelease] \| Mindestens Microsoft Edge zu ladende Version: 86.0.616.0 oder höher \| Vollständige API-Kompatibilität: 91.0.824.0 oder höher  

### <a name="general"></a>Allgemein  

#### <a name="features"></a>Features  

*   Das Ereignis wurde `ProcessFailed` erweitert.  Sie wird jetzt für untergeordnete Prozesse und Framerenderer, die keine Renderer sind, ausgelöst.  
*   Experimentelle [AreBrowserAcceleratorKeysEnabled-Einstellung][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210824GetArebrowseracceleratorkeysenabled] hinzugefügt.  Möglicherweise verhindern Sie, dass der Browser auf Tastenkombinationen im Zusammenhang mit Navigation, Drucken, Speichern und anderen browserspezifischen Funktionen reagiert.  
*   `iframe`Elementunterstützung für `AddScriptToExecuteOnDocumentCreated` hinzugefügt.  
    
#### <a name="promotion"></a>Promotion  

*   [UserAgent][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived] Die API wird nun zu Stable höhergestuft.  
*   Rasterization Scale APIs \([RasterizationScale-Eigenschaft,][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]  [RasterizationScaleChanged-Ereignis,][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] [BoundsMode-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]und [ShouldDetectMonitorScaleChanges-Eigenschaft\)][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] werden jetzt zu Stable höher gestuft.  
    
#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Erweiterte unterstützte C++- und .NET-Projekttypen wie MFC und ATL.  \([\#506][GithubMicrosoftedgeWebviewfeedbackIssue506], [\#669][GithubMicrosoftedgeWebviewfeedbackIssue669]und [\#851][GithubMicrosoftedgeWebviewfeedbackIssue851]\).  
*   Es wurde ein Fehler behoben, bei dem evergreen WebView2 Runtime eingehende Firewalleingaben durchläuft.  
*   Antwort auf Einstellung während `WebResourceRequested` des Ereignisses behoben.  \([\#568][GithubMicrosoftedgeWebviewfeedbackIssue568]\).  
*   Ein Fehler wurde behoben, der beim Navigieren dazu führt, dass `edge://` der Browserprozess beendet wird.  \([\#604][GithubMicrosoftedgeWebviewfeedbackIssue604]\).  
*   Ein Fehler wurde behoben, der WebView2 an die Bildschirmgröße im Visual Hosting-Modus beschränkte.  
    
## <a name="1077444"></a>1.0.774.44  

Veröffentlichungsdatum: 8. März 2021  

[NuGet-Paket][NuGetGallery1.0.774.44] \| Mindestens zu ladende Laufzeitversion: 86.0.616.0 oder höher \| Vollständige API-Kompatibilität: 89.0.774.44 oder höher  

### <a name="general"></a>Allgemein  

#### <a name="features"></a>Features  

*   Verschiedene Microsoft Edge Browserdienste in WebView2 deaktiviert.  
*   Visual Hosting-APIs sind jetzt allgemein verfügbar.  
    
#### <a name="promotions"></a>Promotions  

*   Die folgenden experimentellen APIs werden nun zu Stable höhergestuft.  
    *   [DPI-Unterstützung][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived] verwandter APIs  
    *   Visuelle Hosting-APIs  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
    *   [TrySuspend und Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]  
    *   [DefaultBackgroundColor][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]  
        
#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Ein Fehler wurde behoben, der WebView2 an die Bildschirmgröße im Visual Hosting-Modus beschränkte.  
    
## <a name="10790-prerelease"></a>1.0.790-prerelease  

Veröffentlichungsdatum: 10. Februar 2021  

[NuGet-Paket][NuGetGallery1.0.790-prerelease] \| Microsoft Edge Version 86.0.616.0 oder höher  

### <a name="general"></a>Allgemein  

> [!IMPORTANT]
> **Grundlegende Änderung:** WebView2-Pre-Release-Paket 1.0.781 ist veraltet.  Stellen Sie die Entwicklung mit Paket 1.0.781 ein.  

> [!IMPORTANT]
> WebView2-Vorabversionspaket 0.9.430 ist veraltet und wird mit der nächsten Version entfernt.  Wenn Ihre WebView-App das Paket verwendet, empfiehlt das WebView-Team, zu einem neueren Paket zu wechseln.  

#### <a name="features"></a>Features  

*   [TrySuspend- und Resume-Methode][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend] zum Anhalten und Fortsetzen von WebViews hinzugefügt.  
*   [SetVirtualHostNameToFolderMapping-Methode][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping] hinzugefügt, die einen virtuellen Hostnamen einem Verzeichnispfad zufügt.  \([\#37][GithubMicrosoftedgeWebviewfeedbackIssue37], [\#161][GithubMicrosoftedgeWebviewfeedbackIssue161]und [\#212][GithubMicrosoftedgeWebviewfeedbackIssue212]\).  
*   Die [DefaultBackgroundColor-Eigenschaft][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor] wurde hinzugefügt, um die Farbe und den Alphakanal des Hintergrunds festzulegen.  \([\#414][GithubMicrosoftedgeWebviewfeedbackIssue414]\).  
*   Die [UserAgent-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent] wurde hinzugefügt, um den Benutzer-Agent abzurufen oder festzulegen.  \([\#122][GithubMicrosoftedgeWebviewfeedbackIssue122]\).  
*   Die Methode wurde `CreateCookieWithCookie` durch die `CopyCookie` Methode ersetzt.  
*   Unterstützung für visuelles Hosting mithilfe der [ICoreWebView2CompositionController-Schnittstelle][Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease] hinzugefügt, die mithilfe der neuen Methode von erstellt `CreateCoreWebView2CompositionController` `ICoreWebView2Environment3` wird.  
    
#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Das Feature Microsoft Edge Shopping in WebView2 wurde deaktiviert.  
*   Deaktiviert das Kontextmenü im PDF-Viewer, wenn dies der `AreDefaultContextMenusEnabled` Zeitpunkt `false` ist.  \([\#605][GithubMicrosoftedgeWebviewfeedbackIssue605]\).  
*   Ein Fehler wurde behoben, `E_NOINTERFACE` der bei der Abfrage zurückgegeben `ICoreWebView2` `ICoreWebView2Experimental` wurde.  \([\#691][GithubMicrosoftedgeWebviewfeedbackIssue691]\).  
*   Ein Fehler wurde behoben, der die Navigation mit falsch formatierten URIs zulässt, wenn `CoreWebView2NavigationStartingEventArgs.Cancel` diese auf festgelegt `false` ist.  \([\#400][GithubMicrosoftedgeWebviewfeedbackIssue400]\).  
*   Es wurde ein Fehler behoben, der Popupfenster mit Ereignishandlern blockierte, `window.print()` die an Ereignisse angefügt `NewWindowRequested` waren.  \([\#409][GithubMicrosoftedgeWebviewfeedbackIssue409]\).  
*   Es wurde ein Problem mit dynamischen DPI-Werten beim Verschieben von Apps zwischen verschiedenen Monitoren behoben.  \([\#58][GithubMicrosoftedgeWebviewfeedbackIssue58]\)  
*   Die `HRESULT` von [ICoreWebView2WebResourceResponseViewGetContentCompletedHandler übergebenen Instanzen wurden verbessert::Invoke][Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke].  
*   Schaltfläche zum Verwalten des automatischen Ausfüllens deaktiviert.  \([\#585][GithubMicrosoftedgeWebviewfeedbackIssue585]\).  
*   Es wurde Visual Studio abstürzen, während Sie ausgeführt `WebView2.Dispose` werden, wenn sie in mehreren Fenstern gehostet werden.  \([\#816][GithubMicrosoftedgeWebviewfeedbackIssue816]\) und [\#442][GithubMicrosoftedgeWebviewfeedbackIssue442]\).  
*   Fehler beim Anzeigen des WebView2-Steuerelements in Visual Studio Toolbox wurde behoben.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   Reduzierte Probleme mit hoher CPU-Auslastung.  \([\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
*   Probleme mit veraltetem 1.0.781-prerelease-Paket wurden behoben.  \([\#875][GithubMicrosoftedgeWebviewfeedbackIssue875] und [\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
    
#### <a name="promotions"></a>Promotions  

*   Die folgenden experimentellen APIs werden nun zu Stable höhergestuft.  
    *   Visual Hosting-APIs  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
        
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Fehler behoben, bei dem WebView-Apps abgestürzt sind, die das WPF SDK verwenden.  Der Absturz ist aufgetreten, wenn Sie `F4` ein Fenster geschlossen haben.  \([\#399][GithubMicrosoftedgeWebviewfeedbackIssue399]\).  
*   Der WebView2-Initialisierungsbildschirm ist jetzt transparent und nicht grau.  \([\#196][GithubMicrosoftedgeWebviewfeedbackIssue196]\).  
    
## <a name="1070550"></a>1.0.705.50  

Veröffentlichungsdatum: 25. Januar 2021  

[NuGet-Paket][NuGetGallery1.0.705.50] \| WebView2 Runtime Version 86.0.616.0 oder höher  

### <a name="general"></a>Allgemein  

#### <a name="promotions"></a>Promotions  

*   Die folgenden experimentellen APIs werden nun zu Stable höhergestuft.  
    *   [WebResourceResponseReceived-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest-API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [Cookieverwaltungs-API][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [WebView Environment-Eigenschaft][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  
        
## <a name="10721-prerelease"></a>1.0.721-prerelease  

Veröffentlichungsdatum: 8. Dezember 2020  

[NuGet-Paket][NuGetGallery1.0.721-prerelease] \| Microsoft Edge Version 86.0.616.0 oder höher  

### <a name="general"></a>Allgemein  

> [!IMPORTANT]
> **Grundlegende Änderung:** WebView2-Vorabversionspaket 1.0.707 und Paket 0.9.628 sind veraltet.  Stellen Sie die Entwicklung mit paket 1.0.707 und package0.9.628 ein.  

#### <a name="features"></a>Features  

*   [WebView2-Gruppenrichtlinien][DeployedgeMicrosoftEdgeWebviewPolicies]hinzugefügt.  Weitere Informationen zu empfohlenen Methoden, navigieren Sie zu [Gruppenrichtlinien für WebView2][Webview2ConceptsEnterpriseGroupPoliciesForWebview2].  
*   > [!IMPORTANT]
    > **Grundlegende Änderung:** Veraltet der alte Registrierungsspeicherort.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
    
*   Added support for [Drag and Drop][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease] in WebView2.  
*   APIs zur Behandlung der DPI-Unterstützung hinzugefügt.  
    *   [Die RasterizationScale-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] wurde hinzugefügt, um die DPI-Skalierung für WebView-Inhalte und Ui-Popups sowie das [zugeordnete RasterizationScaleChanged-Ereignis][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] zu ändern.  
    *   [ShouldDetectMonitorScaleChanges-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] hinzugefügt, um die Eigenschaft bei Bedarf automatisch zu `RasterizationScale` aktualisieren.  
    *   [BoundsMode-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode] hinzugefügt, um anzugeben, dass es sich bei den Grenzen um logische Pixel handelt und WebView die Verwendung `RasterizationScale` für die WebView2-Pixelanzeige ermöglicht, und WebView verwendet die `RasterizationScale` mit `Bounds` der, um die physische Größe abzurufen.  
*   Aktualisiertes `NewWindowRequested` Ereignis zu behandeln und `Ctrl` + `click` `Shift` + `click` .  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] und [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  
*   Die folgenden experimentellen APIs werden nun zu Stable höhergestuft.  
    *   [WebResourceResponseReceived-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest-API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [Cookieverwaltungs-API][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [WebView Environment-Eigenschaft][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  
        
### <a name="net"></a>.NET  

#### <a name="features"></a>Features  

*   WinForms-Designer in .NET Core 3.1+ und .NET 5 aktiviert.  
*   Verbesserte .NET-Cookieverwaltung.  \([\#611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Ersetzt `CoreWebView2Ready` durch [CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs].  
    
#### <a name="bug-fixes"></a>Fehlerbehebungen

*   [AcceleratorKeyPressed-Ereignis][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] zur Unterstützung der `AcceleratorKey` Auswahl in WebView2 hinzugefügt.  \([\#288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Unnötige Dateien wurden aus der Ausgabe in WebView2-Ordner entfernt.  \([\#461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   Verbesserte Hostobjekt-API.  \([\#335][GithubMicrosoftedgeWebviewfeedbackIssue335] und [\#525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  
    
## <a name="1066437"></a>1.0.664.37  

Veröffentlichungsdatum: 20. November 2020  

[NuGet-Paket][NuGetGallery1.0.664.37] \| WebView2 Runtime Version 86.0.616.0 oder höher  

### <a name="general"></a>Allgemein  

> [!IMPORTANT]
> **Ankündigung:**.NET WPF/WinForms WebView2 SDKs sind jetzt allgemein verfügbar \(GA\).  Ab dieser Version sind Release-SDKs vorwärtskompatibel.  Weitere Informationen finden Sie im Blogbeitrag zur [GA-Ankündigung.][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]  

#### <a name="features"></a>Features  

*   .NET WPF/WinForms WebView2 ist jetzt allgemein verfügbar \(GA\).  
*   Fixed Distribution \(Bring-your-own\) mode reached GA.  
    
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` Verhindert das Öffnen eines neuen Fensters.  \([\#549][GithubMicrosoftedgeWebviewfeedbackIssue549] und [\#560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  
    
## <a name="10674-prerelease"></a>1.0.674-prerelease  

Veröffentlichungsdatum: 19. Oktober 2020  

[NuGet-Paket][NuGetGallery1.0.674-prerelease] \| WebView2 Runtime Version 86.0.616.0 oder höher  

### <a name="general"></a>Allgemein  

*   [NavigateWithWebResourceRequest-Methode][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest] hinzugefügt, um Postdaten oder andere Anforderungsheader während der Navigation bereitzustellen.  
*   [DomContentLoaded-Ereignis][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded] hinzugefügt, das ausgeführt wird, wenn das ursprüngliche HTML-Dokument geladen und analysiert wird.  
*   Die [Environment-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment] wurde zu WebView2 hinzugefügt.  Diese Eigenschaft macht die WebView2-Umgebung verfügbar, in der eine Instanz von WebView2 erstellt wurde.  
*   Es wurden [Cookieverwaltungs-APIs][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager] hinzugefügt, mit denen Entwickler die WebView2-Sitzung authentifizieren oder Cookies aus WebView abrufen können, um andere Tools zu authentifizieren.  Das Webview-Team plant sprach- oder frameworkspezifische Verbesserungen.  Weitere Informationen finden Sie unter [API-Überprüfung: Cookieverwaltung.][GithubMicrosoftedgeWebview2AnnouncementIssue2]  
*   Das [WebResourceResponseReceived-Ereignis][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived] wurde aktualisiert und unveränderliche [WebResourceResponseView][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease] und [WebResourceResponseReceivedEventArgs::P opulateResponseContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent] zu [WebResourceResponseView::GetContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent]hinzugefügt.  
*   Deaktiviert [Microsoft Defender Application Guard (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] in WebView2.  
*   [SystemCursorId][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid] für visuelles Hosting hinzugefügt.  
*   Fehler für Eingabemethode in Visual Hosting behoben.  
*   Die Anforderung für `version.lib` die Verwendung der statischen WebView2-Bibliothek wurde entfernt.  
    
### <a name="net"></a>.NET  

*   [CoreWebView2-Klasse][DotnetApiMicrosoftWebWebview2CoreCorewebview2] wurde aktualisiert, um die Variable verfügbar zu `CoreWebView2Environment` machen.  
*   Implementierungen von benutzerdefinierten EventArgs-Klassen im Namespace wurden `Microsoft.Web.WebView2.Core` in Unterklassen von [System.EventArgs][DotnetApiSystemEventargs] oder [System.ComponentModel.CancelEventArgs][DotnetApiSystemComponentmodelCancelEventargs]geändert.  \([\#250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Unterstützung für [CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] in WinForms hinzugefügt.  \([\#204][GithubMicrosoftedgeWebviewfeedbackIssue204]\).  
*   [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] .NET-APIs hinzugefügt.  \([\#219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   WinForms Designer [Source-Eigenschaft][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] auf "Standard" aktualisiert oder auf NULL zurückgesetzt.  \([\#177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   WebView2-Grenzen in WebView2.Init() wurden aktualisiert, um DPI-Modi zu unterstützen, die kleiner als 100 % sind.  \([\#432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   [BuildWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] und [DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] wurden aktualisiert, um die Robustheit zu erhöhen.  \([\#382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Aktualisierte .NET Loader-Basis zum Laden des Prozessbits anstelle der Betriebssystemarchitektur.  \([\#431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Umbenannt `EdgeNotFoundException` in [WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception].  
    
## <a name="1062222"></a>1.0.622.22  

Veröffentlichungsdatum: 19. Oktober 2020  

[NuGet-Paket][NuGetGallery1.0.622.22] \| WebView2 Runtime Version 86.0.616.0 oder höher  

### <a name="general"></a>Allgemein  

> [!IMPORTANT]
> **Ankündigung:** Win32 C/C++ WebView2 ist jetzt allgemein verfügbar \(GA\).  Ab dieser Version sind Release-SDKs vorwärtskompatibel.  For more information, navigate to [GA announcement blog post][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability].  

*   [Evergreen WebView2 Runtime und Installer][Webview2ConceptsDistributionUnderstandRuntimeInstaller] sind GA.  Bootstrapper, downlink link for the Bootstrapper, and Standalone Installer for the Evergreen WebView2 Runtime are available on [Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2].  Beispielcode für den Installationsworkflow ist auch im [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samplesMain]verfügbar.  
*   [Der Modus "Feste Version"][Webview2ConceptsDistributionFixedVersionDistributionMode] ist für die Entwicklervorschau verfügbar.  
    
## <a name="0962211"></a>0.9.622.11  

Veröffentlichungsdatum: 10. September 2020  

[NuGet-Paket][NuGetGallery0.9.622.11] \| WebView2 Runtime Version 86.0.616.0 oder höher  

### <a name="general"></a>Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung:** Dieses SDK ist der Release Candidate für WebView2 Win32 C/C++ GA.  Die GA-Version sollte dieselbe API-Schnittstelle und -Funktionalität verwenden.  
    
*   Getrennte [Browserrichtlinien.][DeployedgeMicrosoftEdgePolicies]  
*   [AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount] zu WebView2-Umgebungsoptionen hinzugefügt, um den bedingten Zugriff für WebView zu aktivieren.  
*   Aktualisiert, `ICoreWebView2NewWindowRequestedEventArgs` um [die WindowFeatures-Eigenschaft][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures] und die [zugehörigen ICoreWebView2WindowFeatures einzuschließen.][Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Aktualisiert `System.Windows.Rect`  für die Verwendung anstelle von `System.Drawing.Rectangle` `System.Windows.Rect` \([\#235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Das NewWindowRequested-Ereignis wurde aktualisiert, um die Anforderung ohne Parameter zu `window.open()` verarbeiten.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [AdditionalBrowserArguments][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments] specified with `ICoreWebView2EnvironmentOptions` aren't overridden with environment variables or registry values.  Weitere Informationen finden Sie unter [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions].  
    
## <a name="09579"></a>0.9.579  

Veröffentlichungsdatum: 20. Juli 2020  

[NuGet-Paket][NuGetGallery0.9.579] \| Microsoft Edge Version 86.0.579.0.  

### <a name="general"></a>Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung:** Evergreen WebView2 Runtime und Installationsprogramm werden für die Vorschau veröffentlicht.  Navigieren Sie für weitere Informationen zur [Verteilung von WebView2.][Webview2ConceptsDistributionUnderstandRuntimeInstaller]  
    
*   > [!IMPORTANT]
    > **Ankündigung:** Die folgenden WebView2 SDK-Versionen werden nach der nächsten SDK-Version nicht mehr unterstützt.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Die WebView2 SDK-Versionen sind in nuget.org ebenfalls als veraltet gekennzeichnet.  WebView2 empfiehlt, mit der neuesten Version von WebView2 auf dem neuesten Stand zu bleiben.  
    
*   WebView-Workerthreadverbesserungen hinzugefügt.  \([\#318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Popupblocker in WebView deaktiviert.  Navigieren Sie für weitere Informationen zur [IsUserInitiated-Eigenschaft][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated] im `NewWindowRequested` Ereignis.  
*   Sicherstellen, dass das WebView-Navigationsstartereignis für ausgeführt `about:blank` wird.  Jetzt `NavigationStarting` werden Ereignisse für die gesamte Navigation ausgeführt, Aber Absagen für `about:blank` oder für das Element werden nicht unterstützt und `srcdoc` `iframe` ignoriert.  
*   Einige `edge://` URI-Schemas in WebView wurden blockiert.  
*   Die experimentelle [IsSingleSignOnUsingOSPrimaryAccountEnabled-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled] wurde zu WebView2-Umgebungsoptionen hinzugefügt, um den bedingten Zugriff für WebView zu aktivieren.  
*   Experimentelles [WebResourceResponseReceived-Ereignis][Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived] hinzugefügt, das ausgeführt wird, nachdem WebView die Antwort von einer WebResource-Anforderung empfangen und verarbeitet hat.  Authentifizierungsheader, falls vorhanden, sind im Antwortobjekt enthalten.  
    
### <a name="net"></a>.NET  

*   Verbesserte WPF-Fokusbehandlung.  \([\#185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   `ZoomFactor`Eigenschaft für WPF Webview2 Controller hinzugefügt.  
    
## <a name="09538"></a>0.9.538  

[NuGet-Paket][NuGetGallery0.9.538] \| Microsoft Edge Version 85.0.538.0.  

### <a name="general"></a>Allgemein  

*   Ablegen der Unterstützung für WebView2 SDK Version [0.8.149](#08149).  WebView2 empfiehlt, mit der neuesten Version von WebView2 auf dem neuesten Stand zu bleiben.  
*   Die Gruppenrichtlinie wurde aktualisiert, um zu berücksichtigen, wann der Profilpfad des Microsoft Edge Browsers geändert wird \([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  
    
### <a name="win32-cc"></a>Win32 C/C++  

*   [ICoreWebView2ExperimentalNewWindowRequestedEventArgs::get_WindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]hinzugefügt, das ausgelöst wird, wenn `window.open()` es ausgeführt und [ICoreWebView2ExperimentalWindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease] \([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\) zugeordnet wird.  
*   > [!IMPORTANT]
    > **Grundlegende Änderung:** [Veraltete CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] und ersetzt durch [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions].  
    
*   > [!IMPORTANT]
    > **Grundlegende Änderung:** Um sicherzustellen, dass die WebView2-API den Benennungskonventionen der Windows API entspricht, hat das WebView-Team die Namen der folgenden Elemente aktualisiert.  
    > 
    > *   [AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed] ist jetzt [AreHostObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed].  
    
*   [AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]aktualisiert.  Die ursprünglichen Serialisierungsmarkierungen des Hostobjekts sind jetzt auf die Proxyobjekte festgelegt.  Anschließend werden Serialisierungsmarkierungen des Hostobjekts wieder als Hostobjekt serialisiert, wenn sie als Parameter im JavaScript-Rückruf \([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\) übergeben werden.  
    
### <a name="net-09538-pre-release"></a>.NET (0.9.538 Vorabversion)  

*   Veröffentlichte WinForms- und WPF WebView2API-Beispiele, die umfassende Handbücher des WebView2 SDK sind.  For more information, navigate to [Samples Repo][GithubMicrosoftedgeWebview2samplesMain].  
*   Unterstützung für visuelles Hosting und [fensterfeatures experimentelle APIs][Webview2ConceptsVersioningExperimentalApis]hinzugefügt.  
*   > [!IMPORTANT]
    > **Grundlegende Änderung:** Die folgenden Verzögerungen implementieren jetzt IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]und [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
    
*   [GetAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] und [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] wurden als [CoreWebView2Environment-Statik][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment] hinzugefügt.  
    
## <a name="09515-prerelease"></a>0.9.515-prerelease  

[NuGet-Paket][NuGetGallery0.9.515-prerelease] \| Microsoft Edge Version 84.0.515.0.  

*   > [!IMPORTANT]
    > **Ankündigung:** WebView2 unterstützt jetzt Windows Forms und WPF auf .NET Framework 4.6.2 oder höher und .NET Core 3.0 oder höher im **Vorabversionspaket.**  
    
*   For more information about building WPF apps, navigate to the [WPF Erste Schritte Guide][Webview2GetStartedWpf] and the WebView2 [WPF Reference][DotnetApiMicrosoftWebWebview2Wpf] for WPF-specific APIs.  
*   For more information about building Windows Forms apps, navigate to the [Windows Forms Erste Schritte Guide][Webview2GetStartedWinforms] and the WebView2 Windows Forms [Reference][DotnetApiMicrosoftWebWebview2Winforms] for Windows Forms specific APIs.  
*   For more information about the CoreWebView2 APIs, navigate to [.NET Reference][DotnetApiMicrosoftWebWebview2Core].  
*   > [!CAUTION]
    > **Bekannte Probleme:** Das WebView-Team ist sich einiger Probleme in der Vorabversion bewusst, die in zukünftigen Versionen behoben werden.  
    > 
    > *   **DPI-Grad:** WebView2 für WPF ist derzeit nicht DPI-fähig.  Bei der Initialisierung von WebView2 auf Monitoren mit hohem DPI-Wert gibt es ein bekanntes Problem, bei dem WebView zunächst als Bruchteil des Fensters initialisiert wird, bis die Größe des Fensters geändert wird.  
    > *   **WPF-Designer:** Der WPF-Designer wird derzeit nicht unterstützt.  Fügen Sie das WebView2-Steuerelement in Ihrer App hinzu, indem Sie den entsprechenden XAML-Code direkt in einem Text-Editor ändern.  
    
## <a name="09488"></a>0.9.488  

[NuGet-Paket][NuGetGallery0.9.488] \| Microsoft Edge Version 84.0.488.0.  

*   > [!IMPORTANT]
    > **Ankündigung:** Ab dem bevorstehenden Microsoft Edge Version 83 ist Evergreen WebView nicht mehr auf den Stable-Browserkanal ausgerichtet.  Stattdessen ist eine andere Gruppe von Binärdateien als [Evergreen WebView2 Runtime][Webview2ConceptsDistributionEvergreenDistributionMode]vorgesehen, die Sie über ein Installationsprogramm, das das WebView-Team derzeit entwickelt, verketten können.  Navigieren Sie zu [App-Verteilung,][Webview2ConceptsDistribution]um weitere Informationen zu erfahren.  
    
*   > [!IMPORTANT]
    > **Ankündigung:** In Zukunft veröffentlicht das WebView-Team zwei Pakete: ein Vorabversionspaket mit experimentellen APIs \(für Sie zum Testen\) und ein stabiles Releasepaket mit stabilen APIs \(für Ihr Vertrauen\).  Navigieren Sie zu Grundlegendes zu [Browserversionen und WebView2,][Webview2ConceptsVersioning]um mehr über die Unterschiede zu erfahren.  
    
*   > [!IMPORTANT]
    > **Grundlegende Änderung:** Um sicherzustellen, dass die WebView2-API den Benennungskonventionen der Windows-API entspricht, hat das WebView-Team die Namen der folgenden Schnittstellen aktualisiert.  
    > 
    > *   `CORE_WEBVIEW2_*` Präfix ist jetzt `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo] ist jetzt [GetAvailableCoreWebView2BrowserVersionString][Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo] ist jetzt [get_BrowserVersionString.][Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring]  
    > *   [AddRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] ist jetzt [AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject] ist jetzt [RemoveHostObjectFromScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` ist jetzt `chrome.webview.hostObjects` .  
    
*   > [!IMPORTANT]
    > **Grundlegende Änderung:** Die `AddRemoteObject` JS-Proxymethoden werden ebenfalls umbenannt.  
    > 
    > *   `getLocal` ist jetzt `getLocalProperty` .  
    > *   `setLocal` ist jetzt `setLocalProperty` .  
    > *   `getRemote` ist jetzt `getHostProperty` .  
    > *   `setRemote` ist jetzt `setHostProperty` .  
    > *   `applyRemote` ist jetzt `applyHostFunction` .  
    
*   > [!IMPORTANT]
    > **Grundlegende Änderung:** [Veraltete CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] und ersetzt durch [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions].  
    
*   [FrameNavigationCompleted-Ereignis hinzugefügt.][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]  Wenn nun ein `iframe` Element die Navigation abgeschlossen hat, wird ein Ereignis ausgeführt und gibt den Erfolg der Navigation und die Navigations-ID zurück.  
*   [Die ICoreWebView2EnvironmentOptions-Schnittstelle][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488] wurde hinzugefügt, die verwendet werden kann, um die Version der Evergreen WebView2-Runtime für Ihre App zu ermitteln.  
*   [IsBuiltInErrorPageEnabled-Einstellung][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled] hinzugefügt.  Jetzt können Sie die integrierte Fehlerwebseite für Navigationsfehler und Renderprozessfehler aktivieren oder deaktivieren.  
*   Remoteobjekteinfügung zur Unterstützung von `IDispatch` .NET-Implementierungen \([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\) aktualisiert.  
*   [NewWindowRequested-Ereignis][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested] zum Behandeln von Anforderungen aus Kontextmenüs \([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\) aktualisiert.  
*   Das erste separate WebView2-Vorabversionspaket, in dem Sie auf visuelle Hosting-APIs zugreifen können, wurde veröffentlicht.  Das WebView-Team hat [APISample][GithubMicrosoftedgeWebview2samplesMain] aktualisiert, um die neuen experimentellen APIs einzuschließen.  
    *   [Die ICoreWebView2ExperimentalCompositionController-Schnittstelle][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease] wurde hinzugefügt, um eine Verbindung mit einer Kompositionsstruktur herzustellen und Eingaben für WebView bereitzustellen.  
    *   [ICoreWebView2ExperimentalPointerInfo][Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]hinzugefügt, das alle Informationen aus einer `POINTER_INFO` enthält.  Dieses Objekt wird an SendPointerInput übergeben, um Zeigereingaben in WebView einzufügen.  
    *   [ICoreWebView2ExperimentalCursorChangedEventHandler][Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]wurde hinzugefügt, das der App mitteilt, wann der Mauszeiger über der WebView geändert werden soll.  Wenn sich die Maus über einem Textfeld in der WebView befindet, wechselt der Cursor vom Pfeil zum Selektor.  Die `cursor` Eigenschaft auf der App teilt der App `CompositionController` mit, was der Mauszeiger derzeit für WebView sein sollte.  
        
## <a name="09430"></a>0.9.430  

[NuGet-Paket][NuGetGallery0.9.430] \| Microsoft Edge Version 82.0.430.0.  

WebView2 SDK ist die offizielle Win32 C++-Betaversion, die mehrere Featureanfragen aus Feedback enthält.  Das WebView-Team versucht, die Anzahl der Versionen mit grundlegenden Änderungen zu begrenzen.  Im Rahmen der allgemeinen Verfügbarkeitsansätze sind mehrere wichtige grundlegende Änderungen in die Betaversion integriert.  

*   > [!IMPORTANT]
    > **Grundlegende Änderung:** Bei der letzten Version hat das WebView-Team das Präfix `IWebView2WebView` `ICoreWebView2` umbenannt, um sicherzustellen, dass die WebView2-API mit der Benennungskonvention der Windows-API übereinstimmt.  Um das WebView2 SDK von UI-Frameworks zu nutzen, wurde das WebView-Team `ICoreWebView2` in [ICoreWebView2][Webview2ReferenceWin32Icorewebview2ViewWebview209430] und [ICoreWebView2Host][Webview2ReferenceWin32Icorewebview2hostViewWebview209430]getrennt.  `ICoreWebView2Host` unterstützt Größenanpassung, Anzeigen und Ausblenden, Scharfhalten und andere Funktionen im Zusammenhang mit Fenstern und Komposition.  ICoreWebView2 unterstützt alle anderen WebView2-Funktionen.  Um mehr über das Einbinden der Änderungen zu [][GithubMicrosoftedgeWebview2samplesPr17] erfahren, navigieren Sie zur WebView2-Pullanforderung im WebView2-APISample-Projekt. [][GithubMicrosoftedgeWebview2samplesMain]  
    
*   > [!IMPORTANT]
    > **Grundlegende Änderung:** Aufteilen von [DocumentStateChanged][Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged] in drei Komponenten:  [SourceChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged], [ContentLoading][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]und [HistoryChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged].  Wenn die Quell-URL nun geändert wird, wird das `SourceChanged` Ereignis ausgeführt.  Wenn der Verlaufsstatus geändert wird, wird das `HistoryChanged` Ereignis ausgeführt.  Das `ContentLoading` Ereignis wird vor dem ersten Skript ausgeführt, wenn ein neues Dokument geladen wird.  
    
*   Unterstützung für ARM64-Architektur hinzugefügt.  
*   Unterstützung für Soft Input Panel \(SIP\) für Touchscreengeräte hinzugefügt.  
*   Unterstützung für Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 und Windows Server 2016 hinzugefügt.  
*   [NotifyParentWindowPositionChanged][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged] für die Statusleiste hinzugefügt, um dem Fenster im Fenstermodus zu folgen.  Implementieren Sie außerdem die Änderung im fensterlosen Modus, damit Barrierefreiheitsfeatures funktionieren.  
*   [AreRemoteObjectsAllowed-Einstellung][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed] hinzugefügt, um global zu steuern, ob remoteobjekte auf eine Webseite zugreifen können.  Standardmäßig `AreRemoteObjectsAllowed` ist sie aktiviert, sodass von [AddRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] hinzugefügte Remoteobjekte über die Webseite zugänglich sind.  Wenn die Option `AreRemoteObjectsAllowed` deaktiviert ist, kann auf der Webseite nicht auf die Objekte zugegriffen werden.  Änderungen werden auf das nächste Navigationsereignis angewendet.  
*   [IsZoomControlEnabled-Einstellung hinzugefügt,][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled] um zu verhindern, dass Benutzer den Zoom der WebView mit `ctrl` + `+` `ctrl` + `-` \(oder `ctrl` + Mausrad\) beeinträchtigen.  Der Zoom kann weiterhin mit [put_ZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor] festgelegt werden, wenn die Einstellung deaktiviert ist.  
*   ZoomFactor wurde so geändert, dass er nur auf die aktuelle WebView angewendet wird.  Zoomänderungen an der aktuellen WebView wirken sich nicht auf andere WebViews aus, zu denen Sie mit derselben Ursprungswebsite navigiert sind.  Navigieren Sie zu get_ZoomFactor , um weitere Informationen zu [erfahren.][Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor]  
*   Ausblenden der ZoomView-Benutzeroberfläche für WebView \([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   [SetBoundsAndZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]hinzugefügt.  Jetzt können Sie den Zoomfaktor und die Grenzen einer WebView gleichzeitig festlegen.  
*   [WindowCloseRequested-Ereignis hinzugefügt.][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]  Weitere Informationen erhalten Sie, wenn Sie zu [add_WindowCloseRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested] \([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\) navigieren.  
*   Unterstützung für den `beforeunload` Dialogtyp für JavaScript-Dialogereignisse hinzugefügt und [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind] Enumerationseintrag hinzugefügt.  
*   [GetHeaders][Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders] zu HttpRequestHeaders, [GetHeader][Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader] zu HttpResponseHeaders und [get_HasCurrentHeader-Eigenschaft][Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader] zu HttpHeadersCollectionIterator hinzugefügt.  
*   > [!IMPORTANT]
    > **Grundlegende Änderung:** Geändertes `DevToolsProtocolEventReceived` Verhalten.  Jetzt können Sie einen [DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430] für ein bestimmtes DevTools-Protokollereignis erstellen und dieses Ereignis mit [add_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived] / [remove_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived]abonnieren/kündigen.  
    
*   > [!IMPORTANT]
    > **Breaking Change**: `WebMessageReceivedEventArgs` [Get_WebMessageAsString-Eigenschaft][Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring] in eine [TryGetWebMessageAsString-Methode][Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring] geändert.  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Geänderte `AcceleratorKeyPressedEventArgs` [Handle-Methode][Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle] in eine [get_Handled-Eigenschaft.][Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled]  
    
## <a name="08355"></a>0.8.355  

[NuGet-Paket][NuGetGallery0.8.355] \| Microsoft Edge Version 80.0.355.0.  

*   Veröffentlichtes WebView2API-Beispiel, eine umfassende Anleitung des WebView2 SDK.  Navigieren Sie zu [API-Beispiel,][GithubMicrosoftedgeWebview2samplesApisample]um weitere Informationen zu finden.  
*   IME-Unterstützung für alle Sprachen außer Englisch \([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\) hinzugefügt.  
*   Api-Oberfläche des `WebResourceRequested` Ereignisses als Reaktion auf Fehlerberichte aktualisiert.  Das gleichzeitige Angeben eines Filters und eines Ereignisses bei der Erstellung ist jetzt veraltet.  Verwenden Sie zum Erstellen eines angeforderten Webressourcenereignisses [add_WebResourceRequested,][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested] um das Ereignis hinzuzufügen, und [AddWebResourceRequestedFilter,][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter] um einen Filter hinzuzufügen.  [RemoveWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter] entfernt den Filter \([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Grundlegende Änderung:** Geändertes Vollbildverhalten.  [Veraltete IsFullScreenAllowed][Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated].  Wenn ein Element in einer WebView \(z. B. ein Video\) auf den Vollbildmodus festgelegt ist, füllt es standardmäßig die Grenzen der WebView.  Verwenden Sie das [ContainsFullScreenElementChanged-Ereignis][Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355] und [get_ContainsFullScreenElement,][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement] um anzugeben, wie die App die Größe von WebView ändern soll, wenn ein Element in den Vollbildmodus wechseln möchte.  
    
## <a name="08314"></a>0.8.314  

[NuGet-Paket][NuGetGallery0.8.314] \| Microsoft Edge Version 80.0.314.0.  

*   Unterstützung für Windows 7, Windows 8 und Windows 8.1 hinzugefügt.  
*   Visual Studio und Visual Studio Code Debugunterstützung für WebView2 hinzugefügt.  Debuggen Sie nun Ihr Skript in WebView2 direkt aus Ihrer IDE.  Weitere Informationen finden Sie unter [Debuggen beim Entwickeln mit WebView2-Steuerelementen.][Webview2HowToDebug]  
*   Für `Native Object Injection` das ausgeführte Skript in WebView2 hinzugefügt, um von der Win32-Komponente der App auf ein IDispatch-Objekt zuzugreifen und auf die Eigenschaften des IDispatch-Objekts zuzugreifen.  Weitere Informationen erhalten Sie, wenn Sie zu [AddRemoteObject][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject] \([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\) navigieren.  
*   `AcceleratorKeyPressed`Ereignis hinzugefügt.  Weitere Informationen erhalten Sie, wenn Sie zu [add_AcceleratorKeyPressed][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\) navigieren.  
*   Deaktiviert die `Context Menus` .  Weitere Informationen erhalten Sie, wenn Sie zu [put_AreDefaultContextMenusEnabled][Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\) navigieren.  
*   `DPI Awareness`Aktualisiert.  Jetzt entspricht der DPI-Grad von WebView dem DPI-Grad der Host-App.  
    
    > [!NOTE]
    > Wenn eine andere Hybrid-App mit einem anderen DPI-Grad gestartet wird als die ursprüngliche WebView, wird die neue WebView nicht gestartet, wenn die `user data folder` gleiche \([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\) ist.  
    
*   Wurde `Notification Change Behavior` aktualisiert, sodass WebView2 automatisch Benachrichtigungsberechtigungsanforderungen ablehnt, die von in WebView gehosteten Webinhalten angefordert werden.  
    
## <a name="08270"></a>0.8.270  

[NuGet-Paket][NuGetGallery0.8.270] \| Microsoft Edge Version 78.0.270.0.  

*   Ereignis wurde hinzugefügt, um die Änderung des `DocumentTitleChanged` Dokumenttitels anzugeben \([\#27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   `GetWebView2BrowserVersionInfo`API \([\#18][GithubMicrosoftedgeWebviewfeedbackIssue18]\) hinzugefügt.  
*   `NewWindowRequested`Ereignis hinzugefügt.  
*   Aktualisierte `CreateWebView2EnvironmentWithDetails` Funktion zum Entfernen `releaseChannelPreference` .  Weitere Informationen zu der `CreateWebView2EnvironmentWithDetails` Funktion, navigieren Sie zu [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Die Außerkraftsetzung von Registrierungs- und Umgebungsvariablen wird weiterhin unterstützt.  Die Standardkanaleinstellung wird verwendet, es sei denn, sie wird überschrieben.  
    Während der Kanalsuche überspringt das WebView-Team alle vorherigen Kanalversionen, die nicht mit dem WebView2 SDK kompatibel sind.  
    Das WebView-Team wählt den stabileren Kanal aus, um das einheitlichste Verhalten für den Endbenutzer sicherzustellen.  Wenn Sie mit den neuesten Canary-Builds testen, sollten Sie ein Skript erstellen, auf das die `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` Umgebungsvariable `1` festgelegt wird, bevor Sie die App starten.  
*   Die `CreateWebView2EnvironmentWithDetails` Funktion wurde mit der Logik für die Auswahl `userDataFolder` aktualisiert, wenn sie nicht angegeben wurde.  Weitere Informationen zu der `CreateWebView2EnvironmentWithDetails` Funktion, navigieren Sie zu [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Wenn Sie zuvor den `userDataFolder` Standardspeicherort verwendet haben, wird beim Wechsel zum neuen SDK der Standardwert `userDataFolder` "\(auf einen neuen Speicherort im Hostcodeverzeichnis festgelegt\) zurückgesetzt, und Ihr Status wird ebenfalls zurückgesetzt.  Wenn der Hostprozess nicht über die Berechtigung zum Schreiben in das angegebene Verzeichnis verfügt, schlägt die `CreateWebView2EnvironmentWithDetails` Funktion möglicherweise fehl.  Sie können die Daten aus dem alten `user data folder` in das neue Verzeichnis kopieren.  
    
## <a name="08230"></a>0.8.230  

[NuGet-Paket][NuGetGallery0.8.230] \| Microsoft Edge Version 77.0.230.0.  

*   `Stop`API zum Beenden aller Navigation und ausstehender Ressourcenabrufe \([\#28][GithubMicrosoftedgeWebviewfeedbackIssue28]\) hinzugefügt.  
*   `.tlb`Datei zum NuGet Paket \([\#22][GithubMicrosoftedgeWebviewfeedbackIssue22]\) hinzugefügt.  
*   .NET-Projekte zur Installerliste im NuGet-Paket \([\#32][GithubMicrosoftedgeWebviewfeedbackIssue32]\) hinzugefügt.  
    
## <a name="08190"></a>0.8.190  

[NuGet-Paket][NuGetGallery0.8.190] \| Microsoft Edge Version 77.0.190.0.  

*   Hinzugefügt, `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` um zu steuern, ob Benutzer DevTools \([\#16][GithubMicrosoftedgeWebviewfeedbackIssue16]\) öffnen können.  
*   Zum `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` Steuerelement hinzugefügt, ob die Statusleiste angezeigt wird \([\#19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Für `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` das Zurück- und Vorwärtsgehen durch den Navigationsverlauf hinzugefügt.  
*   HTTP-Headertypen \( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` \) zum Anzeigen und Ändern von HTTP-Headern in WebView hinzugefügt.  
*   32-Bit-WebView-Unterstützung auf 64-Bit-Computern hinzugefügt \([\#13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   WebView-IDL zum SDK \([\#14][GithubMicrosoftedgeWebviewfeedbackIssue14]\) hinzugefügt.  
*   Lib zur Unterstützung von `IID\_\*` Schnittstellen-ID-Objekten \([\#12][GithubMicrosoftedgeWebviewfeedbackIssue12]\) hinzugefügt.  
*   Hinzugefügt wurden Pfad, Verknüpfung und automatisches Kopieren von DLL-Dateien zu NuGet `TARGET` Datei im SDK.  
*   Das Anfordern im Skript ist `window.open()` aktiviert.  
    
## <a name="08149"></a>0.8.149  

[NuGet-Paket][NuGetGallery0.8.149] \| Microsoft Edge Version 76.0.149.0.  

Anfängliche Entwicklervorschauversion.  

<!-- Links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Verteilung von Anwendungen mithilfe von WebView2 | Microsoft-Dokumente"  
[Webview2ConceptsDistributionEvergreenDistributionMode]: ./concepts/distribution.md#evergreen-distribution-mode "Evergreen-Verteilungsmodus – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft-Dokumente"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Verteilungsmodus für feste Versionen – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft-Dokumente"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Grundlegendes zur WebView2-Laufzeit und zum Installationsprogramm – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft-Dokumente"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Gruppenrichtlinien für WebView2 – Verwalten von WebView2-Anwendungen | Microsoft-Dokumente"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Grundlegendes zu Browserversionen und WebView2 | Microsoft-Dokumentation"  
[Webview2ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "Experimentelle APIs – Grundlegendes zu Browserversionen und WebView2-| Microsoft-Dokumente"  
[Webview2ConceptsVersioningMatchingWebview2RuntimeVersions]: ./concepts/versioning.md#matching-webview2-runtime-versions "Übereinstimmende WebView2-Laufzeitversionen – Grundlegendes zu WebView2 SDK-Versionen | Microsoft-Dokumente"  
[Webview2GetStartedWinforms]: ./get-started/winforms.md "Erste Schritte mit WebView2 in Windows Forms-Apps | Microsoft-Dokumente"  
[Webview2GetStartedWpf]: ./get-started/wpf.md "Erste Schritte mit WebView2 in WPF | Microsoft-Dokumente"  
[Webview2HowToDebug]: ./how-to/debug.md "Debuggen beim Entwickeln mit WebView2-Steuerelementen | Microsoft-Dokumente"  

[Webview2ReferenceWin32Icorewebview2experimental2ViewWebview210865PrereleaseAddDownloadstarting]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental2?view=webview2-1.0.865-prerelease&preserve-view=true#add_downloadstarting  "add_DownloadStarting – Schnittstelle ICoreWebView2Experimental2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironment3ViewWebview210865PrereleaseUpdateruntime]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment3?view=webview2-1.0.865-prerelease&preserve-view=true#updateruntime  "UpdateRuntime – Schnittstelle ICoreWebView2ExperimentalEnvironment3 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalframeViewWebview210865PrereleaseAddhostobjecttoscriptwithorigins]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalframe?view=webview2-1.0.865-prerelease&preserve-view=true#addhostobjecttoscriptwithorigins  "AddHostObjectToScriptWithOrigins – Schnittstelle ICoreWebView2ExperimentalFrame | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalsettings4ViewWebview210865PrereleaseIspinchzoomenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings4?view=webview2-1.0.865-prerelease&preserve-view=true#ispinchzoomenabled  "IsPinchZoomEnabled – Schnittstelle ICoreWebView2ExperimentalSettings4 | Microsoft-Dokumente" 

[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210824GetArebrowseracceleratorkeysenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings2?view=webview2-1.0.824&preserve-view=true#get_arebrowseracceleratorkeysenabled "get_AreBrowserAcceleratorKeyPressed – Schnittstelle ICoreWebView2ExperimentalSettings | Microsoft-Dokumente" 

[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded – ICoreWebView2_2 | der Schnittstelle Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#get_environment "ICoreWebView2CookieManager | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#setvirtualhostnametofoldermapping "SetVirtualHostNameToFolderMapping – Schnittstelle ICoreWebView2_3 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#trysuspend "TrySuspend – Schnittstelle ICoreWebview2_3 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled – Schnittstelle ICoreWebView2AcceleratorKeyPressedEventArgs | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2compositioncontroller?view=webview2-1.0.790-prerelease&preserve-view=true "schnittstelle ICoreWebView2CompositionController | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]: /microsoft-edge/webview2/reference/win32/icorewebview2controller2?view=webview2-1.0.790-prerelease&preserve-view=true#get_defaultbackgroundcolor "get_DefaultBackgroundColor – Schnittstelle ICoreWebView2Controller2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2cookiemanager?view=webview2-1.0.721-prerelease&preserve-view=true "ICoreWebView2CookieManager | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "schnittstelle ICoreWebView2DevToolsProtocolEventReceiver | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived – Schnittstelle ICoreWebView2DevToolsProtocolEventReceiver | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived – Schnittstelle ICoreWebView2DevToolsProtocolEventReceiver | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2environment2?view=webview2-1.0.721-prerelease&preserve-view=true#createwebresourcerequest "CreateWebResourceRequest – Schnittstelle ICoreWebView2Environment | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "schnittstelle ICoreWebView2EnvironmentOptions | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount – Schnittstelle ICoreWebView2EnvironmentOptions | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments – Schnittstelle ICoreWebView2EnvironmentOptions | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo – schnittstelle ICoreWebView2Environment | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring "get_BrowserVersionString – Schnittstelle ICoreWebView2Environment | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2?view=webview2-1.0.674-prerelease&preserve-view=true#get_systemcursorid "schnittstelle ICoreWebView2ExperimentalWebResourceResponseView | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "schnittstelle ICoreWebView2ExperimentalCompositionController3 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "schnittstelle ICoreWebView2ExperimentalCompositionController | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged – Schnittstelle ICoreWebView2ExperimentalController | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode – Schnittstelle ICoreWebView2ExperimentalController | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale – Schnittstelle ICoreWebView2ExperimentalController | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges – Schnittstelle ICoreWebView2ExperimentalController | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "schnittstelle ICoreWebView2ExperimentalCursorChangedEventHandler | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled – schnittstelle ICoreWebView2ExperimentalEnvironmentOptions | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures – Schnittstelle ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "schnittstelle ICoreWebView2ExperimentalPointerInfo | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings?view=webview2-1.0.790-prerelease&preserve-view=true#get_useragent "get_UserAgent – Schnittstelle ICoreWebView2ExperimentalSettings | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived – Schnittstelle ICoreWebView2Experimental | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded – Schnittstelle ICoreWebView2Experimental | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived – Schnittstelle ICoreWebView2Experimental | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager – Schnittstelle ICoreWebView2Experimental | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment – Schnittstelle ICoreWebView2Experimental | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest – Schnittstelle ICoreWebView2Experimental | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent – Schnittstelle ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "schnittstelle ICoreWebView2ExperimentalWebResourceResponseView | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent – Schnittstelle ICoreWebView2ExperimentalWebResourceResponseView | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "schnittstelle ICoreWebView2ExperimentalWindowFeatures | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "schnittstelle ICoreWebView2Host | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor – Schnittstelle ICoreWebView2Host | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged – Schnittstelle ICoreWebView2Host | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor – Schnittstelle ICoreWebView2Host | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor – Schnittstelle ICoreWebView2Host | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader – Schnittstelle ICoreWebView2HttpHeadersCollectionIterator | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders – Schnittstelle ICoreWebView2HttpRequestHeaders | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader – Schnittstelle ICoreWebView2HttpResponseHeaders | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated Schnittstelle ICoreWebView2NewWindowRequestedEventArgs | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures – Schnittstelle ICoreWebView2NewWindowRequestedEventArgs | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed – Schnittstelle ICoreWebView2Settings | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled – Schnittstelle ICoreWebView2Settings | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed – Schnittstelle ICoreWebView2Settings | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled "get_IsBuiltInErrorPageEnabled – Schnittstelle ICoreWebView2Settings | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed – Schnittstelle ICoreWebView2Settings | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading – ICoreWebView2-| der Schnittstelle Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.538&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript – Schnittstelle ICoreWebView2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString – Schnittstelle ICoreWebView2WebMessageReceivedEventArgs | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke]: /microsoft-edge/webview2/reference/win32/icorewebview2webresourceresponseviewgetcontentcompletedhandler?view=webview2-1.0.790-prerelease&preserve-view=true#invoke "Invoke – Schnittstelle ICoreWebView2WebResourceResponseViewGetContentCompletedHandler | Microsoft-Dokumente" 
[Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "schnittstelle ICoreWebView2WindowFeatures | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle – Schnittstelle IWebView2AcceleratorKeyPressedEventArgs | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "schnittstelle IWebView2ContainsFullScreenElementChangedEventHandler | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled – Schnittstelle IWebView2Settings2 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated – Schnittstelle IWebView2Settings | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString – Schnittstelle IWebView2WebMessageReceivedEventArgs | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed – Schnittstelle IWebView2WebView4 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject – Schnittstelle IWebView2WebView4 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested – Schnittstelle IWebView2WebView5 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter – Schnittstelle IWebView2WebView5 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement – Schnittstelle IWebView2WebView5 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter – Schnittstelle IWebView2WebView5 | Microsoft-Dokumente" 
[Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged – Schnittstelle IWebView2WebView | Microsoft-Dokumente" 
[Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails – Globals | Microsoft-Dokumente" 
[Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo – Globale | Microsoft-Dokumente" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails – Globals | Microsoft-Dokumente" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions – Globals | Microsoft-Dokumentation" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString – Globale | Microsoft-Dokumente" 
[Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions – Globals | Microsoft-Dokumentation" 
[Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions – Globals | Microsoft Edge" 

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge – Richtlinien | Microsoft-Dokumente"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2 – Richtlinien | Microsoft-Dokumente"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Microsoft.Web.WebView2.Core-Namespace | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "CoreWebView2-Klasse (Microsoft.Web.WebView2.Core) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "CoreWebView2Environment-Klasse (Microsoft.Web.WebView2.Core) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "CoreWebView2Environment.CompareBrowserVersions(String, String) Method (Microsoft.Web.WebView2.Core) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "CoreWebView2Environment.GetAvailableBrowserVersionString(String)-Methode (Microsoft.Web.WebView2.Core) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "CoreWebView2HttpRequestHeaders-Klasse (Microsoft.Web.WebView2.Core) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "CoreWebView2HttpResponseHeaders-Klasse (Microsoft.Web.WebView2.Core) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "CoreWebView2.NewWindowRequested-Ereignis (Microsoft.Web.WebView2.Core) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "CoreWebView2.PermissionRequested-Ereignis (Microsoft.Web.WebView2.Core) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "CoreWebView2.ScriptDialogOpening-Ereignis (Microsoft.Web.WebView2.Core) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "CoreWebView2.WebResourceRequested-Ereignis (Microsoft.Web.WebView2.Core) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "CoreWebView2InitializationCompletedEventArgs-Klasse | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2.WebView2RuntimeNotFound (Microsoft.Web.WebView2.Core) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft.Web.WebView2.WinForms-Namespace | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "CoreWebView2CreationProperties-Klasse (Microsoft.Web.WebView2.Winforms) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Webview2.Source-Klasse (Microsoft.Web.WebView2.Winforms) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Microsoft.Web.WebView2.Wpf-Namespace | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "microsoft.web.webview2.wpf.webview2.acceleratorkeypressed | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "WebView2.BuildWindowCore(HandleRef)-Methode (Microsoft.Web.WebView2.Wpf) | Microsoft-Dokumente"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "WebView2.DestroyWindowCore(HandleRef)-Methode (Microsoft.Web.WebView2.Wpf) | Microsoft-Dokumente"  
[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "CancelEventArgs-Klasse (System.ComponentModel) | Microsoft-Dokumente"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "EventArgs-Klasse (System) | Microsoft-Dokumente"  

[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Assemblys mit starkem Namen | Microsoft-Dokumente"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Microsoft Defender Application Guard (Windows 10) – Windows | Microsoft-Dokumente"  
[WindowsWin32ApiWinuserSetWindowDisplayAffinity]: /windows/win32/api/winuser/nf-winuser-setwindowdisplayaffinity "SetWindowDisplayAffinity-Funktion (winuser.h) – Win32-Apps | Microsoft-Dokumente"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]: https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Ankündigungs-Repository für MicrosoftEdge/WebViewAnnouncement Issue 2"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "WebView2-API-Beispiel – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesWebview2wpfbrowser]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2WpfBrowser "WebView2WpfBrowser – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Verschieben des Projekts zur Verwendung des neuesten WebView2 SDK 0.9.430 – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue37]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/37 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 37"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue58]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/58 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 58"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 108"  
[GithubMicrosoftedgeWebviewfeedbackIssue113]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Feedback-Repository für MicrosoftEdge/WebViewFeedback-Problem 119"  
[GithubMicrosoftedgeWebviewfeedbackIssue122]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/122 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 122"  
[GithubMicrosoftedgeWebviewfeedbackIssue131]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 131"  
[GithubMicrosoftedgeWebviewfeedbackIssue148]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue161]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/161 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 161"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 177"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 179"  
[GithubMicrosoftedgeWebviewfeedbackIssue181]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 181"  
[GithubMicrosoftedgeWebviewfeedbackIssue183]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 183"  
[GithubMicrosoftedgeWebviewfeedbackIssue185]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 185"  
[GithubMicrosoftedgeWebviewfeedbackIssue196]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/196 "Feedback-Repository für MicrosoftEdge/WebViewFeedback-Problem 196"  
[GithubMicrosoftedgeWebviewfeedbackIssue204]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 204"  
[GithubMicrosoftedgeWebviewfeedbackIssue205]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/205 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 205"  
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 210"  
[GithubMicrosoftedgeWebviewfeedbackIssue212]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/212 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 212"  
[GithubMicrosoftedgeWebviewfeedbackIssue219]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 219"  
[GithubMicrosoftedgeWebviewfeedbackIssue228]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 228"  
[GithubMicrosoftedgeWebviewfeedbackIssue235]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 235"  
[GithubMicrosoftedgeWebviewfeedbackIssue250]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 250"  
[GithubMicrosoftedgeWebviewfeedbackIssue275]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/275 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 275"  
[GithubMicrosoftedgeWebviewfeedbackIssue288]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 288"  
[GithubMicrosoftedgeWebviewfeedbackIssue293]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 293"  
[GithubMicrosoftedgeWebviewfeedbackIssue318]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue399]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/399 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 399"  
[GithubMicrosoftedgeWebviewfeedbackIssue400]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/400 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 400"  
[GithubMicrosoftedgeWebviewfeedbackIssue409]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/409 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 409"  
[GithubMicrosoftedgeWebviewfeedbackIssue414]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/414 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 414"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue442]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/442 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 442"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue506]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/506 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 506"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue568]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/568 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 568"  
[GithubMicrosoftedgeWebviewfeedbackIssue585]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/585 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 585"  
[GithubMicrosoftedgeWebviewfeedbackIssue604]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/604 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 604"  
[GithubMicrosoftedgeWebviewfeedbackIssue605]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/605 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 605"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 611"  
[GithubMicrosoftedgeWebviewfeedbackIssue669]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/669 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 669"  
[GithubMicrosoftedgeWebviewfeedbackIssue691]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/691 "Feedback-Repository für MicrosoftEdge/WebViewFeedback-Problem 691"  
[GithubMicrosoftedgeWebviewfeedbackIssue816]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/816 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 816"  
[GithubMicrosoftedgeWebviewfeedbackIssue851]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/851 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 851"  
[GithubMicrosoftedgeWebviewfeedbackIssue875]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/875 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 875"  
[GithubMicrosoftedgeWebviewfeedbackIssue878]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/878 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 878"  
[GithubMicrosoftedgeWebviewfeedbackIssue1120]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1120 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 1120"
[GithubMicrosoftedgeWebviewfeedbackIssue940]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/940 "Feedback-Repository für MicrosoftEdge/WebViewFeedback-Problem 940"
[GithubMicrosoftedgeWebviewfeedbackIssue841]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/841 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 841"
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 210"
[GithubMicrosoftedgeWebviewfeedbackIssue338]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/338 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 338"
[GithubMicrosoftedgeWebviewfeedbackIssue589]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/589 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 589"
[GithubMicrosoftedgeWebviewfeedbackIssue933]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/933 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 933"
[GithubMicrosoftedgeWebviewfeedbackIssue946]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/946 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 946"
[GithubMicrosoftedgeWebviewfeedbackIssue1011]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1011 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 1011"
[GithubMicrosoftedgeWebviewfeedbackIssue1050]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1050 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 1050"
[GithubMicrosoftedgeWebviewfeedbackIssue996]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/996 "Feedback-Repository für MicrosoftEdge/WebViewFeedback-Problem 996"
[GithubMicrosoftedgeWebviewfeedbackIssue850]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/850 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 850"
[GithubMicrosoftedgeWebviewfeedbackIssue1077]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1077 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 1077"
[GithubMicrosoftedgeWebviewfeedbackIssue1099]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1099 "Feedback-Repository für MicrosoftEdge/WebViewFeedback-Problem 1099"
[GithubMicrosoftedgeWebviewfeedbackIssue1183]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1183 "Feedback-Repository für MicrosoftEdge/WebViewFeedback-Problem 1183"
[GithubMicrosoftedgeWebviewfeedbackIssue1108]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1108 "Feedback-Repository für MicrosoftEdge/WebViewFeedback-Problem 1108"
[GithubMicrosoftedgeWebviewfeedbackIssue940]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/940 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 850"
[GithubMicrosoftedgeWebviewfeedbackIssue1079]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1079 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 1079"
[GithubMicrosoftedgeWebviewfeedbackIssue1013]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1013 "Feedback-Repository für MicrosoftEdge/WebViewFeedback-Problem 1013"
[GithubMicrosoftedgeWebviewfeedbackIssue1282]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1282 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 1282"
[GithubMicrosoftedgeWebviewfeedbackIssue828]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/828 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 828"
[GithubMicrosoftedgeWebviewfeedbackIssue619]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/619 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 619"
[GithubMicrosoftedgeWebviewfeedbackIssue608]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/608 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 608"
[GithubMicrosoftedgeWebviewfeedbackIssue1209]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1209 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 1209"
[GithubMicrosoftedgeWebviewfeedbackIssue448]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/448 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 448"
[GithubMicrosoftedgeWebviewfeedbackIssue1123]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1123 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Problem 1123"

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Ankündigung der allgemeinen Verfügbarkeit für Microsoft Edge WebView2 für .NET und fixed Distribution Method | .NET Blog"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2-| Microsoft Edge Entwickler"  

[NuGetGallery]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "NuGet Katalog | Microsoft.Web.WebView2"  
[NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.149"  
[NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.190"  
[NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.230"  
[NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.270"  
[NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.314"  
[NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.355"  
[NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "NuGet Katalog | Microsoft.Web.WebView2 v0.9.430"  
[NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "NuGet Katalog | Microsoft.Web.WebView2 v0.9.488"  
[NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v0.9.515 prerelease"  
[NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "NuGet Katalog | Microsoft.Web.WebView2 v0.9.538"  
[NuGetGallery0.9.579]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "NuGet Katalog | Microsoft.Web.WebView2 v0.9.579"  
[NuGetGallery0.9.622.11]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "NuGet Katalog | Microsoft.Web.WebView2 v0.9.622.11"  
[NuGetGallery0.9.628-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v0.9.628 prerelease"  
[NuGetGallery1.0.622.22]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.622.22"  
[NuGetGallery1.0.664.34]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.664.34"  
[NuGetGallery1.0.664.37]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.664.37"  
[NuGetGallery1.0.674-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v1.0.674 prerelease"  
[NuGetGallery1.0.705.50]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.705.50 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.705.50"  
[NuGetGallery1.0.721-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v1.0.721 prerelease"  
[NuGetGallery1.0.774.44]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.774.44 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.774.44"  
[NuGetGallery1.0.790-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.790-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v1.0.790 prerelease"  
[NuGetGallery1.0.818.41]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.818.41 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.818.41"  
[NuGetGallery1.0.864.35]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.864.35 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.864.35"  
[NuGetGallery1.0.824-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.824-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v1.0.824 prerelease"  
[NuGetGallery1.0.865-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.865-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v1.0.865 prerelease"  
[NuGetGallery1.0.902-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.902-prerelease "NuGet Katalog | Vorabversion von Microsoft.Web.WebView2 v1.0.902"  

[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Ankündigung der allgemeinen Verfügbarkeit von Microsoft Edge WebView2 | Microsoft Edge Blog"  
[Webview2ReferenceWin32Icorewebview2experimentalsettings5ViewWebview210902PrereleaseGetIsswipenavigationenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings5?view=webview2-1.0.902-prerelease&preserve-view=true#get_isswipenavigationenabled "get_IsSwipeNavigationEnabled – Schnittstelle ICoreWebView2ExperimentalSettings5 | Microsoft-Dokumente"
[Webview2ReferenceWin32Icorewebview2experimentalenvironment4ViewWebview210902PrereleaseAddBrowserprocessexited]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment4?view=webview2-1.0.902-prerelease&preserve-view=true#add_browserprocessexited "add_BrowserProcessExited – Schnittstelle ICoreWebView2ExperimentalEnvironment4 | Microsoft-Dokumente"
[Webview2ReferenceWin32Icorewebview2experimental3ViewWebview210902PrereleaseAddClientcertificaterequested]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental3?view=webview2-1.0.902-prerelease&preserve-view=true#add_clientcertificaterequested "add_ClientCertificateRequested – Schnittstelle ICoreWebView2Experimental3 | Microsoft-Dokumente"


[Webview2ReferenceWin32Icorewebview24ViewWebview210902PrereleaseAddDownloadstarting]: /microsoft-edge/webview2/reference/win32/icorewebview2_4?view=webview2-1.0.902-prerelease&preserve-view=true#add_downloadstarting "add_DownloadStarting – ICoreWebView2_4 | der Schnittstelle Microsoft-Dokumente"
[Webview2ReferenceWin32Icorewebview24ViewWebview210902PrereleaseAddFramecreated]: /microsoft-edge/webview2/reference/win32/icorewebview2_4?view=webview2-1.0.902-prerelease&preserve-view=true#add_framecreated "add_FrameCreated – Schnittstellen-ICoreWebView2_4 | Microsoft-Dokumente"
[Webview2ReferenceWin32Icorewebview2setting4ViewWebview210902PrereleaseGetIsgeneralautofillenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings4?view=webview2-1.0.902-prerelease&preserve-view=true#get_isgeneralautofillenabled "get_IsGeneralAutofillEnabled – Schnittstelle ICoreWebView2Settings4 | Microsoft-Dokumente"

[AddHostObjectToScriptWithOriginsAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2frame?view=webview2-1.0.902-prerelease&preserve-view=true#addhostobjecttoscriptwithorigins "AddHostObjectToScriptWithOrigins | Microsoft-Dokumente"

[Webview2ReferenceWin32Icorewebview2setting5ViewWebview210902PrereleaseGetIspinchzoomenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings5?view=webview2-1.0.902-prerelease&preserve-view=true#get_ispinchzoomenabled "get_IsPinchZoomEnabled – Schnittstelle ICoreWebView2Settings5 | Microsoft-Dokumente"

[Webview2ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount – Schnittstelle ICoreWebView2EnvironmentOptions | Microsoft-Dokumente"
[Webview2ReferenceWin32Icorewebview2setting2ViewWebview21086435GetUseragent]: /microsoft-edge/webview2/reference/win32/icorewebview2settings2?view=webview2-1.0.864.35&preserve-view=true#get_useragent 

/microsoft-edge/webview2/reference/win32/icorewebview2settings2?view=webview2-1.0.864.35&preserve-view=true#get_useragent 

"get_UserAgent – Schnittstelle ICoreWebView2Setting2 | Microsoft Docs"
[Webview2ReferenceWin32Icorewebview2setting2ViewWebview21086435GetArebrowseracceleratorkeysenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings3?view=webview2-1.0.864.35&preserve-view=true#get_arebrowseracceleratorkeysenabled "get_AreBrowserAcceleratorKeysEnabled – Schnittstelle ICoreWebView2Settings3 | Microsoft-Dokumente"
