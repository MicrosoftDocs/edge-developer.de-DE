---
description: Leitfaden für die ersten Schritte mit WebView2 für Win32-Apps
title: Erste Schritte mit WebView2 für Win32-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html
ms.openlocfilehash: 6eae00a0fddb75782be5a3e94efaa5a8965674a0
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643448"
---
# <a name="get-started-with-webview2"></a>Erste Schritte mit WebView2  

Beginnen Sie in diesem Artikel mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Hauptfeatures von [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]  Für weitere Informationen zu einzelnen WebView2-APIs navigieren Sie zur [API-Referenz.][Webview2ReferenceWin32]  

## <a name="prerequisites"></a>Voraussetzungen  

Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.  

*   [WebView2 Runtime][Webview2Installer] oder ein [Microsoft Edge (Chromium) nicht stabiler Kanal,][MicrosoftedgeinsiderDownload] der auf dem unterstützten Betriebssystem \(derzeit Windows 10, Windows 8.1 und Windows 7\) installiert ist.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2015 oder höher mit installierter C++-Unterstützung.  
    
## <a name="step-1---create-a-single-window-app"></a>Schritt 1: Erstellen einer Einzelfenster-App  

Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.  

> [!IMPORTANT]
> Um sich besser auf die exemplarische Vorgehensweise zu konzentrieren, verwenden Sie den geänderten Beispielcode aus [walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] für Ihre Beispiel-App.  Navigieren Sie zu [WebView2-Beispielen,][GithubMicrosoftedgeWebview2samplesGettingStartedGuide]um das geänderte Beispiel herunterzuladen und zu beginnen.  

1.  Öffnen Sie in Visual Studio `WebView2GettingStarted.sln` .  
    Wenn Sie eine ältere Version von Visual Studio verwenden, zeigen Sie auf das **WebView2GettingStarted-Projekt,** öffnen Sie das Kontextmenü \(Rechtsklick\), und wählen Sie **Eigenschaften**aus.  Ändern Sie unter **"Konfigurationseigenschaften**  >  **allgemein"** **Windows SDK-Versions-** und **Plattformtoolset,** um das Win10 SDK und Visual Studio Toolset zu verwenden, das Ihnen zur Verfügung steht.  
    
:::image type="complex" source="../media/tool-version.png" alt-text="Toolversion" lightbox="../media/tool-version.png":::
   Toolversion  
:::image-end:::      

Visual Studio können Fehler anzeigen, da dem Projekt die WebView2-Headerdatei fehlt.  Die Fehler sollten nach [Schritt 2](#step-2---install-webview2-sdk)behoben werden.  

## <a name="step-2---install-webview2-sdk"></a>Schritt 2: Installieren des WebView2 SDK  

Fügen Sie das WebView2 SDK dem Projekt hinzu.  Verwenden Sie NuGet, um das Win32 SDK zu installieren.  

1.  Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen **Sie "Verwalten NuGet Pakete" aus.**  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="NuGet-Pakete verwalten" lightbox="../media/manage-nuget-packages.png":::
       NuGet-Pakete verwalten  
    :::image-end:::  
    
1.  Installieren Sie die Windows-Implementierungsbibliothek.  
    1.  Geben Sie in der Suchleiste `Microsoft.Windows.ImplementationLibrary` > Wählen Sie **"Microsoft.Windows" aus. ImplementationLibrary**.  
    1.  Wählen Sie im rechten Fenster die Option **"Installieren"** aus.  NuGet lädt die Bibliothek auf Ihren Computer herunter.  
        
        > [!NOTE]
        > Die [Windows Implementierungsbibliothek][GithubMicrosoftWilMain] und [Windows C++-Laufzeitvorlagenbibliothek][CppCxWrlTemplateLibraryVS2019] sind optional und erleichtern das Arbeiten mit COM für das Beispiel.  
        
        :::image type="complex" source="../media/wil.png" alt-text="Windows Implementierungsbibliothek" lightbox="../media/wil.png":::
           Windows Implementierungsbibliothek  
        :::image-end:::  
        
1.  Installieren Sie das WebView2 SDK.  
    1.  Geben Sie in der Suchleiste `Microsoft.Web.WebView2` > wählen Sie **Microsoft.Web.WebView2**aus.  
    1.  Wählen Sie im rechten Fenster die Option **"Installieren"** aus.  NuGet lädt das SDK auf Ihren Computer herunter.  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet Paket-Manager" lightbox="../media/nuget.png":::
           NuGet Paket-Manager
        :::image-end:::  
        
1.  Fügen Sie WebView2-Header zu Ihrem Projekt hinzu.  
    
    :::row:::
       :::column span="1":::
          Kopieren Sie in der `HelloWebView.cpp` Datei den folgenden Codeausschnitt, und fügen Sie ihn nach der letzten `#include` Zeile ein.  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          Der Include-Abschnitt sollte dem folgenden Codeausschnitt ähneln.  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
Bereit für die Verwendung und Erstellung für die WebView2-API.  

### <a name="build-your-empty-sample-app"></a>Erstellen Einer leeren Beispiel-App  

Um die Beispiel-App zu erstellen und auszuführen, wählen Sie `F5` .  Ihre App zeigt ein leeres Fenster an.  

:::image type="complex" source="../media/empty-app.png" alt-text="Leere App" lightbox="../media/empty-app.png":::
   Leere App  
:::image-end:::    

## <a name="step-3---create-a-single-webview-within-the-parent-window"></a>Schritt 3: Erstellen einer einzelnen WebView im übergeordneten Fenster  

Fügen Sie dem Hauptfenster eine WebView hinzu.  

Verwenden Sie die `CreateCoreWebView2Environment` Methode, um die Umgebung einzurichten und den Microsoft Edge \(Chromium\)-Browser zu suchen, der das Steuerelement ansteuert.  Sie können die Methode auch verwenden, wenn Sie den `CreateCoreWebView2EnvironmentWithOptions` Speicherort des Browsers, den Benutzerordner, Browserflags usw. anstelle der Standardeinstellung angeben möchten.  Führen Sie nach Abschluss der `CreateCoreWebView2Environment` Methode die Methode innerhalb des `ICoreWebView2Environment::CreateCoreWebView2Controller` `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` Rückrufs aus, und führen Sie die `ICoreWebView2Controller::get_CoreWebView2` Methode aus, um die zugeordnete WebView abzurufen.  

Legen Sie im Rückruf einige weitere Einstellungen fest, ändern Sie die Größe von WebView auf 100 % des übergeordneten Fensters, und navigieren Sie zu Bing.  

Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `HelloWebView.cpp` nach dem Kommentar und vor dem Kommentar `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` ein.  

```cpp
// Step 3 - Create a single WebView within the parent window
// Locate the browser and set up the environment for WebView
CreateCoreWebView2EnvironmentWithOptions(nullptr, nullptr, nullptr,
    Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
        [hWnd](HRESULT result, ICoreWebView2Environment* env) -> HRESULT {
        
            // Create a CoreWebView2Controller and get the associated CoreWebView2 whose parent is the main window hWnd
            env->CreateCoreWebView2Controller(hWnd, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                [hWnd](HRESULT result, ICoreWebView2Controller* controller) -> HRESULT {
                if (controller != nullptr) {
                    webviewController = controller;
                    webviewController->get_CoreWebView2(&webviewWindow);
                }
                
                // Add a few settings for the webview
                // The demo step is redundant since the values are the default settings
                ICoreWebView2Settings* Settings;
                webviewWindow->get_Settings(&Settings);
                Settings->put_IsScriptEnabled(TRUE);
                Settings->put_AreDefaultScriptDialogsEnabled(TRUE);
                Settings->put_IsWebMessageEnabled(TRUE);
                
                // Resize WebView to fit the bounds of the parent window
                RECT bounds;
                GetClientRect(hWnd, &bounds);
                webviewController->put_Bounds(bounds);
                
                // Schedule an async task to navigate to Bing
                webviewWindow->Navigate(L"https://www.bing.com/");
                
                // Step 4 - Navigation events
                
                // Step 5 - Scripting
                
                // Step 6 - Communication between host and web content
                
                return S_OK;
            }).Get());
        return S_OK;
    }).Get());
```  

### <a name="build-your-bing-sample-app"></a>Erstellen Ihrer Bing-Beispiel-App  

Um die App zu erstellen und auszuführen, wählen Sie `F5` .  Nun wird in einem WebView-Fenster die Bing Seite angezeigt.  

:::image type="complex" source="../media/bing-window.png" alt-text="Bing Fenster" lightbox="../media/bing-window.png":::
   Bing Fenster  
:::image-end:::    

## <a name="step-4---navigation-events"></a>Schritt 4: Navigationsereignisse  

Das WebView-Team hat bereits im letzten Schritt die Navigation zur URL mithilfe `ICoreWebView2::Navigate` der Methode behandelt.  Während der Navigation löst WebView eine Abfolge von Ereignissen aus, auf die der Host lauscht.  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   
    
Navigieren Sie zu [Navigationsereignissen,][Webview2ConceptsNavigationEvents]um weitere Informationen zu erfahren.  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse" lightbox="../media/navigation-events.png":::
   Navigationsereignisse  
:::image-end:::    

In Fehlerfällen kann eines oder mehrere der folgenden Ereignisse auftreten, je nachdem, ob die Navigation zu einer Fehlerwebseite fortgesetzt wurde.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`
    
> [!NOTE]
> Wenn eine HTTP-Umleitung erfolgt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.  

Registrieren Sie als Beispiel für die Verwendung der Ereignisse einen Handler für das `NavigationStarting` Ereignis, um alle Nicht-HTTPS-Anforderungen abzubrechen.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` .  

```cpp
// register an ICoreWebView2NavigationStartingEventHandler to cancel any non-https navigation
EventRegistrationToken token;
webviewWindow->add_NavigationStarting(Callback<ICoreWebView2NavigationStartingEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2NavigationStartingEventArgs * args) -> HRESULT {
        PWSTR uri;
        args->get_Uri(&uri);
        std::wstring source(uri);
        if (source.substr(0, 5) != L"https") {
            args->put_Cancel(true);
        }
        CoTaskMemFree(uri);
        return S_OK;
    }).Get(), &token);
```  

Jetzt navigiert die App nicht zu Websites, die keine HTTPS-Websites sind.  Sie können einen ähnlichen Mechanismus verwenden, um andere Aufgaben auszuführen, z. B. das Einschränken der Navigation auf Ihre eigene Domäne.  

## <a name="step-5---scripting"></a>Schritt 5 – Skripting  

Sie können Host-Apps verwenden, um JavaScript-Code zur Laufzeit in WebView2-Steuerelemente einzufügen.  Sie können WebView zum Ausführen beliebigen JavaScripts oder zum Hinzufügen von Initialisierungsskripts verwenden.  Das eingefügte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis javaScript entfernt wird.  Das eingefügte JavaScript wird mit einem bestimmten Timing ausgeführt.  

*   Führen Sie es nach der Erstellung des globalen Objekts aus.  
*   Führen Sie es aus, bevor ein anderes skript, das im HTML-Dokument enthalten ist, ausgeführt wird.  
    
Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` .  

```cpp
// Schedule an async task to add initialization script that freezes the Object object
webviewWindow->AddScriptToExecuteOnDocumentCreated(L"Object.freeze(Object);", nullptr);
// Schedule an async task to get the document URL
webviewWindow->ExecuteScript(L"window.document.URL;", Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
    [](HRESULT errorCode, LPCWSTR resultObjectAsJson) -> HRESULT {
        LPCWSTR URL = resultObjectAsJson;
        //doSomethingWithURL(URL);
        return S_OK;
    }).Get());
```  

Jetzt sollte WebView das Objekt immer fixieren `Object` und das Seitendokument einmal zurückgeben.  

> [!NOTE] 
> Die Skripteinfügungs-APIs \(und einige andere WebView2-APIs\) sind asynchron. Sie sollten Rückrufe verwenden, wenn Code in einer bestimmten Reihenfolge ausgeführt werden muss.  

## <a name="step-6---communication-between-host-and-web-content"></a>Schritt 6 : Kommunikation zwischen Host- und Webinhalten  

Der Host und der Webinhalt können auch über die Methode miteinander `postMessage` kommunizieren.  Der in einer WebView ausgeführte Webinhalt kann über die Methode an den Host gesendet `window.chrome.webview.postMessage` werden, und die Nachricht wird von jedem registrierten `ICoreWebView2WebMessageReceivedEventHandler` Ereignishandler auf dem Host verarbeitet.  Ebenso kann der Host die Nachricht an den Webinhalt oder die `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` Methode senden, die von Handlern abgefangen wird, die vom Listener hinzugefügt `window.chrome.webview.addEventListener` wurden.  Der Kommunikationsmechanismus ermöglicht es dem Webinhalt, systemeigene Funktionen zu verwenden, indem Nachrichten übergeben werden, um den Host aufzufordern, systemeigene APIs auszuführen.  

Um den Mechanismus zu verstehen, werden die folgenden Schritte ausgeführt, wenn Sie versuchen, die Dokument-URL in WebView auszugeben.  

1.  Der Host registriert einen Handler, um empfangene Nachrichten an den Webinhalt zurückzugeben  
1.  Der Host fügt ein Skript in den Webinhalt ein, der einen Handler zum Drucken von Nachrichten vom Host registriert.  
1.  Der Host fügt ein Skript in den Webinhalt ein, der die URL an den Host sendet  
1.  Der Handler des Hosts wird ausgelöst und gibt die Nachricht \(die URL\) an den Webinhalt zurück.  
1.  Der Handler des Webinhalts wird ausgelöst und druckt die Nachricht vom Host \(die URL\)  
    
Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` .  

```cpp
// Set an event handler for the host to return received message back to the web content
webviewWindow->add_WebMessageReceived(Callback<ICoreWebView2WebMessageReceivedEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2WebMessageReceivedEventArgs * args) -> HRESULT {
        PWSTR message;
        args->TryGetWebMessageAsString(&message);
        // processMessage(&message);
        webview->PostWebMessageAsString(message);
        CoTaskMemFree(message);
        return S_OK;
    }).Get(), &token);

// Schedule an async task to add initialization script that
// 1) Add an listener to print message from the host
// 2) Post document URL to the host
webviewWindow->AddScriptToExecuteOnDocumentCreated(
    L"window.chrome.webview.addEventListener(\'message\', event => alert(event.data));" \
    L"window.chrome.webview.postMessage(window.document.URL);",
nullptr);
```  

### <a name="build-your-display-url-sample-app"></a>Erstellen der Beispiel-APP für die Anzeige-URL  

Um die App zu erstellen und auszuführen, wählen Sie `F5` .  Die URL wird in einem Popupfenster angezeigt, bevor Sie zu einer Webseite navigieren.  

:::image type="complex" source="../media/show-url.png" alt-text="Anzeige-URL" lightbox="../media/show-url.png":::
   Anzeige-URL  
:::image-end:::    

Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.  

## <a name="next-steps"></a>Nächste Schritte  

Weitere WebView2-Funktionen, die in diesem Artikel nicht behandelt werden, finden Sie in den folgenden Ressourcen.  

*   Um mehr über das Erstellen von WebView2-Anwendungen zu erfahren, navigieren Sie zu bewährten Methoden für die [WebView2-Entwicklung.][WV2BestPractices]  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie im [WebView2-API-Beispiel.][GithubMicrosoftedgeWebview2samplesApisample]  
*   Navigieren Sie für eine Beispiel-App, die mit WebView2 erstellt wurde, zu [WebView2Browser.][GithubMicrosoftedgeWebview2browser]  
*   Ausführliche Informationen zur WebView2-API finden Sie in der [API-Referenz.][Webview2ReferenceWin32]  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team aufnehmen  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WV2BestPractices]: ../concepts/developer-guide.md "Bewährte Methoden für die WebView2-Entwicklung | Microsoft-Dokumente"  
[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2-| Microsoft Edge Entwickler"  

[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++-Referenz | Microsoft-Dokumente"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft-Dokumente"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Windows Laufzeit-C++-Vorlagenbibliothek (WRL) | Microsoft-Dokumente"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Exemplarische Vorgehensweise: Erstellen einer herkömmlichen Windows Desktopanwendung (C++) | Microsoft-Dokumente"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser – MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "WebView2-API-Beispiel – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Windows Implementierungsbibliotheken (WIL) – microsoft/wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2-Installationsprogramm"  
