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
ms.openlocfilehash: 2714f9a6cffea3cb7d53f9a4128d64920fd02dce
ms.sourcegitcommit: 7713eec634264b0c44b1bb426f5b466c44b4e005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2021
ms.locfileid: "11618386"
---
# <a name="get-started-with-webview2"></a><span data-ttu-id="8d42c-104">Erste Schritte mit WebView2</span><span class="sxs-lookup"><span data-stu-id="8d42c-104">Get started with WebView2</span></span>  

<span data-ttu-id="8d42c-105">Beginnen Sie in diesem Artikel mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Hauptfeatures von [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]</span><span class="sxs-lookup"><span data-stu-id="8d42c-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="8d42c-106">Für weitere Informationen zu einzelnen WebView2-APIs navigieren Sie zur [API-Referenz.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="8d42c-106">For more information about individual WebView2 APIs, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="8d42c-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8d42c-107">Prerequisites</span></span>  

<span data-ttu-id="8d42c-108">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="8d42c-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="8d42c-109">[WebView2 Runtime][Webview2Installer] oder ein [Microsoft Edge (Chromium) nicht stabiler Kanal,][MicrosoftedgeinsiderDownload] der unter unterstützten Betriebssystemen \(derzeit Windows 10, Windows 8.1 und Windows 7\) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8d42c-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
*   <span data-ttu-id="8d42c-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 oder höher mit installierter C++-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="8d42c-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  
    
## <a name="step-1---create-a-single-window-app"></a><span data-ttu-id="8d42c-111">Schritt 1: Erstellen einer Einzelfenster-App</span><span class="sxs-lookup"><span data-stu-id="8d42c-111">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="8d42c-112">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="8d42c-112">Start with a basic desktop project that contains a single main window.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8d42c-113">Um sich besser auf die exemplarische Vorgehensweise zu konzentrieren, verwenden Sie geänderten Beispielcode aus [walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span><span class="sxs-lookup"><span data-stu-id="8d42c-113">To better focus the walkthrough, use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="8d42c-114">Navigieren Sie zu [WebView2-Beispielen,][GithubMicrosoftedgeWebview2samplesGettingStartedGuide]um das geänderte Beispiel herunterzuladen und zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="8d42c-114">To download the modified sample and get started, navigate to [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

1.  <span data-ttu-id="8d42c-115">Öffnen Sie in Visual Studio `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="8d42c-115">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  
    <span data-ttu-id="8d42c-116">Wenn Sie eine ältere Version von Visual Studio verwenden, zeigen Sie auf das **WebView2GettingStarted-Projekt,** öffnen Sie das Kontextmenü \(Rechtsklick\), und wählen Sie **Eigenschaften**aus.</span><span class="sxs-lookup"><span data-stu-id="8d42c-116">If you use an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and choose **Properties**.</span></span>  <span data-ttu-id="8d42c-117">Ändern Sie unter **"Konfigurationseigenschaften**  >  **allgemein"** **Windows SDK-Version** und **-Plattformtoolset,** um das Win10 SDK und Visual Studio Toolset zu verwenden, das Ihnen zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="8d42c-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset available to you.</span></span>  
    
:::image type="complex" source="../media/tool-version.png" alt-text="Toolversion" lightbox="../media/tool-version.png":::
   <span data-ttu-id="8d42c-119">Toolversion</span><span class="sxs-lookup"><span data-stu-id="8d42c-119">Tool version</span></span>  
:::image-end:::      

<span data-ttu-id="8d42c-120">Visual Studio können Fehler anzeigen, da dem Projekt die WebView2-Headerdatei fehlt.</span><span class="sxs-lookup"><span data-stu-id="8d42c-120">Visual Studio may display errors, because your project is missing the WebView2 header file.</span></span>  <span data-ttu-id="8d42c-121">Die Fehler sollten nach [Schritt 2](#step-2---install-webview2-sdk)behoben werden.</span><span class="sxs-lookup"><span data-stu-id="8d42c-121">The errors should be fixed after [Step 2](#step-2---install-webview2-sdk).</span></span>  

## <a name="step-2---install-webview2-sdk"></a><span data-ttu-id="8d42c-122">Schritt 2: Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="8d42c-122">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="8d42c-123">Fügen Sie das WebView2 SDK zum Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="8d42c-123">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="8d42c-124">Verwenden Sie NuGet, um das Win32 SDK zu installieren.</span><span class="sxs-lookup"><span data-stu-id="8d42c-124">Use NuGet to install the Win32 SDK.</span></span>  

1.  <span data-ttu-id="8d42c-125">Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen **Sie "Verwalten NuGet Pakete" aus.**</span><span class="sxs-lookup"><span data-stu-id="8d42c-125">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="NuGet-Pakete verwalten" lightbox="../media/manage-nuget-packages.png":::
       <span data-ttu-id="8d42c-127">NuGet-Pakete verwalten</span><span class="sxs-lookup"><span data-stu-id="8d42c-127">Manage NuGet packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8d42c-128">Installieren Sie die Windows Implementierungsbibliothek.</span><span class="sxs-lookup"><span data-stu-id="8d42c-128">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="8d42c-129">Geben Sie in der Suchleiste `Microsoft.Windows.ImplementationLibrary` > Wählen Sie **"Microsoft.Windows" aus. ImplementationLibrary**.</span><span class="sxs-lookup"><span data-stu-id="8d42c-129">In the search bar, type `Microsoft.Windows.ImplementationLibrary` > choose **Microsoft.Windows.ImplementationLibrary**.</span></span>  
    1.  <span data-ttu-id="8d42c-130">Wählen Sie im rechten Fenster die Option **"Installieren"** aus.</span><span class="sxs-lookup"><span data-stu-id="8d42c-130">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="8d42c-131">NuGet lädt die Bibliothek auf Ihren Computer herunter.</span><span class="sxs-lookup"><span data-stu-id="8d42c-131">NuGet downloads the library to your machine.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="8d42c-132">Die [Windows Implementierungsbibliothek][GithubMicrosoftWilMain] und [Windows C++-Laufzeitvorlagenbibliothek][CppCxWrlTemplateLibraryVS2019] sind optional und erleichtern das Arbeiten mit COM für das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="8d42c-132">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Windows Implementierungsbibliothek" lightbox="../media/wil.png":::
           <span data-ttu-id="8d42c-134">Windows Implementierungsbibliothek</span><span class="sxs-lookup"><span data-stu-id="8d42c-134">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="8d42c-135">Installieren Sie das WebView2 SDK.</span><span class="sxs-lookup"><span data-stu-id="8d42c-135">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="8d42c-136">Geben Sie in der Suchleiste `Microsoft.Web.WebView2` > wählen Sie **Microsoft.Web.WebView2**aus.</span><span class="sxs-lookup"><span data-stu-id="8d42c-136">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    1.  <span data-ttu-id="8d42c-137">Wählen Sie im rechten Fenster die Option **"Installieren"** aus.</span><span class="sxs-lookup"><span data-stu-id="8d42c-137">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="8d42c-138">NuGet lädt das SDK auf Ihren Computer herunter.</span><span class="sxs-lookup"><span data-stu-id="8d42c-138">NuGet downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet Paket-Manager" lightbox="../media/nuget.png":::
           <span data-ttu-id="8d42c-140">NuGet Paket-Manager</span><span class="sxs-lookup"><span data-stu-id="8d42c-140">NuGet Package Manager</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="8d42c-141">Fügen Sie WebView2-Header zu Ihrem Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="8d42c-141">Add WebView2 header to your project.</span></span>  
    
    :::row:::
       :::column span="1":::
          <span data-ttu-id="8d42c-142">Kopieren Sie in der `HelloWebView.cpp` Datei den folgenden Codeausschnitt, und fügen Sie ihn nach der letzten `#include` Zeile ein.</span><span class="sxs-lookup"><span data-stu-id="8d42c-142">In the `HelloWebView.cpp` file, copy the following code snippet and paste it after the last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="8d42c-143">Der Include-Abschnitt sollte dem folgenden Codeausschnitt ähneln.</span><span class="sxs-lookup"><span data-stu-id="8d42c-143">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="8d42c-144">Bereit für die Verwendung und Erstellung für die WebView2-API.</span><span class="sxs-lookup"><span data-stu-id="8d42c-144">Ready to use and build against the WebView2 API.</span></span>  

### <a name="build-your-empty-sample-app"></a><span data-ttu-id="8d42c-145">Erstellen Einer leeren Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="8d42c-145">Build your empty sample app</span></span>  

<span data-ttu-id="8d42c-146">Um die Beispiel-App zu erstellen und auszuführen, wählen Sie `F5` .</span><span class="sxs-lookup"><span data-stu-id="8d42c-146">To build and run the sample app, select `F5`.</span></span>  <span data-ttu-id="8d42c-147">Ihre App zeigt ein leeres Fenster an.</span><span class="sxs-lookup"><span data-stu-id="8d42c-147">Your app displays an empty window.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Leere App" lightbox="../media/empty-app.png":::
   <span data-ttu-id="8d42c-149">Leere App</span><span class="sxs-lookup"><span data-stu-id="8d42c-149">Empty app</span></span>  
:::image-end:::    

## <a name="step-3---create-a-single-webview-within-the-parent-window"></a><span data-ttu-id="8d42c-150">Schritt 3: Erstellen einer einzelnen WebView im übergeordneten Fenster</span><span class="sxs-lookup"><span data-stu-id="8d42c-150">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="8d42c-151">Fügen Sie dem Hauptfenster eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="8d42c-151">Add a WebView to the main window.</span></span>  

<span data-ttu-id="8d42c-152">Verwenden Sie die `CreateCoreWebView2Environment` Methode, um die Umgebung einzurichten und den Microsoft Edge \(Chromium\)-Browser zu suchen, der das Steuerelement ansteuert.</span><span class="sxs-lookup"><span data-stu-id="8d42c-152">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="8d42c-153">Sie können die Methode auch verwenden, wenn Sie den `CreateCoreWebView2EnvironmentWithOptions` Speicherort des Browsers, den Benutzerordner, Browserflags usw. anstelle der Standardeinstellung angeben möchten.</span><span class="sxs-lookup"><span data-stu-id="8d42c-153">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="8d42c-154">Führen Sie nach Abschluss der `CreateCoreWebView2Environment` Methode die Methode innerhalb des `ICoreWebView2Environment::CreateCoreWebView2Controller` `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` Rückrufs aus, und führen Sie die `ICoreWebView2Controller::get_CoreWebView2` Methode aus, um die zugeordnete WebView abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8d42c-154">Upon the completion of the `CreateCoreWebView2Environment` method, run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="8d42c-155">Legen Sie im Rückruf einige weitere Einstellungen fest, ändern Sie die Größe von WebView auf 100 % des übergeordneten Fensters, und navigieren Sie zu Bing.</span><span class="sxs-lookup"><span data-stu-id="8d42c-155">In the callback, set a few more settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="8d42c-156">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `HelloWebView.cpp` nach dem Kommentar und vor dem Kommentar `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` ein.</span><span class="sxs-lookup"><span data-stu-id="8d42c-156">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` comment and before the `// <-- WebView2 sample code ends here -->` comment.</span></span>  

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

### <a name="build-your-bing-sample-app"></a><span data-ttu-id="8d42c-157">Erstellen Ihrer Bing-Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="8d42c-157">Build your Bing sample app</span></span>  

<span data-ttu-id="8d42c-158">Um die App zu erstellen und auszuführen, wählen Sie `F5` .</span><span class="sxs-lookup"><span data-stu-id="8d42c-158">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="8d42c-159">Jetzt haben Sie ein WebView-Fenster, in dem die Bing Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8d42c-159">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Bing Fenster" lightbox="../media/bing-window.png":::
   <span data-ttu-id="8d42c-161">Bing Fenster</span><span class="sxs-lookup"><span data-stu-id="8d42c-161">Bing window</span></span>  
:::image-end:::    

## <a name="step-4---navigation-events"></a><span data-ttu-id="8d42c-162">Schritt 4: Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="8d42c-162">Step 4 - Navigation events</span></span>  

<span data-ttu-id="8d42c-163">Das WebView-Team hat bereits im letzten Schritt die Navigation zur URL mithilfe `ICoreWebView2::Navigate` der Methode behandelt.</span><span class="sxs-lookup"><span data-stu-id="8d42c-163">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="8d42c-164">Während der Navigation löst WebView eine Abfolge von Ereignissen aus, auf die der Host lauscht.</span><span class="sxs-lookup"><span data-stu-id="8d42c-164">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   
    
<span data-ttu-id="8d42c-165">Navigieren Sie zu [Navigationsereignissen,][Webview2ConceptsNavigationEvents]um weitere Informationen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="8d42c-165">For more information, navigate to [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse" lightbox="../media/navigation-events.png":::
   <span data-ttu-id="8d42c-167">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="8d42c-167">Navigation events</span></span>  
:::image-end:::    

<span data-ttu-id="8d42c-168">In Fehlerfällen kann eines oder mehrere der folgenden Ereignisse auftreten, je nachdem, ob die Navigation zu einer Fehlerwebseite fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="8d42c-168">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`
    
> [!NOTE]
> <span data-ttu-id="8d42c-169">Wenn eine HTTP-Umleitung erfolgt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="8d42c-169">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="8d42c-170">Registrieren Sie als Beispiel für die Verwendung der Ereignisse einen Handler für das `NavigationStarting` Ereignis, um alle Nicht-HTTPS-Anforderungen abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="8d42c-170">As an example of using the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="8d42c-171">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="8d42c-171">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="8d42c-172">Jetzt navigiert die App nicht mehr zu websites, die nicht https sind.</span><span class="sxs-lookup"><span data-stu-id="8d42c-172">Now the app does not navigate to any non-https sites.</span></span>  <span data-ttu-id="8d42c-173">Sie können einen ähnlichen Mechanismus verwenden, um andere Aufgaben auszuführen, z. B. das Einschränken der Navigation auf Ihre eigene Domäne.</span><span class="sxs-lookup"><span data-stu-id="8d42c-173">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <a name="step-5---scripting"></a><span data-ttu-id="8d42c-174">Schritt 5 – Skripting</span><span class="sxs-lookup"><span data-stu-id="8d42c-174">Step 5 - Scripting</span></span>  

<span data-ttu-id="8d42c-175">Sie können Host-Apps verwenden, um JavaScript-Code zur Laufzeit in WebView2-Steuerelemente einzufügen.</span><span class="sxs-lookup"><span data-stu-id="8d42c-175">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="8d42c-176">Sie können WebView zum Ausführen beliebigen JavaScripts oder zum Hinzufügen von Initialisierungsskripts verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d42c-176">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="8d42c-177">Das eingefügte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis javaScript entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8d42c-177">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="8d42c-178">Das eingefügte JavaScript wird mit einem bestimmten Timing ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d42c-178">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="8d42c-179">Führen Sie es nach der Erstellung des globalen Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="8d42c-179">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="8d42c-180">Führen Sie es aus, bevor ein anderes skript, das im HTML-Dokument enthalten ist, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d42c-180">Run it before any other script included in the HTML document is run.</span></span>  
    
<span data-ttu-id="8d42c-181">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="8d42c-181">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="8d42c-182">Jetzt sollte WebView das Objekt immer fixieren `Object` und das Seitendokument einmal zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8d42c-182">Now, WebView should always freeze the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="8d42c-183">Die Skripteinfügungs-APIs \(und einige andere WebView2-APIs\) sind asynchron. Sie sollten Rückrufe verwenden, wenn Code in einer bestimmten Reihenfolge ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="8d42c-183">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <a name="step-6---communication-between-host-and-web-content"></a><span data-ttu-id="8d42c-184">Schritt 6 : Kommunikation zwischen Host- und Webinhalten</span><span class="sxs-lookup"><span data-stu-id="8d42c-184">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="8d42c-185">Der Host und der Webinhalt können auch über die Methode miteinander `postMessage` kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="8d42c-185">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="8d42c-186">Der in einer WebView ausgeführte Webinhalt kann über die Methode an den Host gesendet `window.chrome.webview.postMessage` werden, und die Nachricht wird von jedem registrierten `ICoreWebView2WebMessageReceivedEventHandler` Ereignishandler auf dem Host verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8d42c-186">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="8d42c-187">Ebenso kann der Host die Nachricht an den Webinhalt oder die `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` Methode senden, die von Handlern abgefangen wird, die vom Listener hinzugefügt `window.chrome.webview.addEventListener` wurden.</span><span class="sxs-lookup"><span data-stu-id="8d42c-187">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="8d42c-188">Der Kommunikationsmechanismus ermöglicht es dem Webinhalt, systemeigene Funktionen zu verwenden, indem Nachrichten übergeben werden, um den Host aufzufordern, systemeigene APIs auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8d42c-188">The communication mechanism allows the web content to use native capabilities by passing messages to ask the host to run native APIs.</span></span>  

<span data-ttu-id="8d42c-189">Um den Mechanismus zu verstehen, werden die folgenden Schritte ausgeführt, wenn Sie versuchen, die Dokument-URL in WebView auszugeben.</span><span class="sxs-lookup"><span data-stu-id="8d42c-189">As an example to understand the mechanism, the following steps occur when you try to output the document URL in WebView.</span></span>  

1.  <span data-ttu-id="8d42c-190">Der Host registriert einen Handler, um empfangene Nachrichten an den Webinhalt zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="8d42c-190">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="8d42c-191">Der Host fügt ein Skript in den Webinhalt ein, der einen Handler zum Drucken von Nachrichten vom Host registriert.</span><span class="sxs-lookup"><span data-stu-id="8d42c-191">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="8d42c-192">Der Host fügt ein Skript in den Webinhalt ein, der die URL an den Host sendet</span><span class="sxs-lookup"><span data-stu-id="8d42c-192">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="8d42c-193">Der Handler des Hosts wird ausgelöst und gibt die Nachricht \(die URL\) an den Webinhalt zurück.</span><span class="sxs-lookup"><span data-stu-id="8d42c-193">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="8d42c-194">Der Handler des Webinhalts wird ausgelöst und druckt die Nachricht vom Host \(die URL\)</span><span class="sxs-lookup"><span data-stu-id="8d42c-194">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  
    
<span data-ttu-id="8d42c-195">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="8d42c-195">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

### <a name="build-your-display-url-sample-app"></a><span data-ttu-id="8d42c-196">Erstellen der Beispiel-APP für die Anzeige-URL</span><span class="sxs-lookup"><span data-stu-id="8d42c-196">Build your display URL sample app</span></span>  

<span data-ttu-id="8d42c-197">Um die App zu erstellen und auszuführen, wählen Sie `F5` .</span><span class="sxs-lookup"><span data-stu-id="8d42c-197">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="8d42c-198">Die URL wird in einem Popupfenster angezeigt, bevor Sie zu einer Webseite navigieren.</span><span class="sxs-lookup"><span data-stu-id="8d42c-198">The URL appears in a pop-up window before navigating to a webpage.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Anzeige-URL" lightbox="../media/show-url.png":::
   <span data-ttu-id="8d42c-200">Anzeige-URL</span><span class="sxs-lookup"><span data-stu-id="8d42c-200">Display url</span></span>  
:::image-end:::    

<span data-ttu-id="8d42c-201">Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.</span><span class="sxs-lookup"><span data-stu-id="8d42c-201">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="8d42c-202">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="8d42c-202">Next steps</span></span>  

<span data-ttu-id="8d42c-203">Weitere WebView2-Funktionen, die in diesem Artikel nicht behandelt werden, finden Sie in den folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8d42c-203">For additional WebView2 functionality that isn't covered in this article, review the following resources.</span></span>  

*   <span data-ttu-id="8d42c-204">Um mehr über das Erstellen von WebView2-Anwendungen zu erfahren, navigieren Sie zu bewährten Methoden für die [WebView2-Entwicklung.][WV2BestPractices]</span><span class="sxs-lookup"><span data-stu-id="8d42c-204">To learn more about building WebView2 applications, navigate to [WebView2 development best practices][WV2BestPractices].</span></span>  
*   <span data-ttu-id="8d42c-205">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie im [WebView2-API-Beispiel.][GithubMicrosoftedgeWebview2samplesApisample]</span><span class="sxs-lookup"><span data-stu-id="8d42c-205">For a comprehensive example of WebView2 capabilities, navigate to [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="8d42c-206">Navigieren Sie für eine Beispiel-App, die mit WebView2 erstellt wurde, zu [WebView2Browser.][GithubMicrosoftedgeWebview2browser]</span><span class="sxs-lookup"><span data-stu-id="8d42c-206">For a sample app built using WebView2, navigate to [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="8d42c-207">Ausführliche Informationen zur WebView2-API finden Sie in der [API-Referenz.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="8d42c-207">For detailed information about the WebView2 API, navigate to [API reference][Webview2ReferenceWin32].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="8d42c-208">Kontakt mit dem Microsoft Edge WebView-Team aufnehmen</span><span class="sxs-lookup"><span data-stu-id="8d42c-208">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WV2BestPractices]: ../concepts/developer-guide.md "Bewährte Methoden für die WebView2-Entwicklung | Microsoft-Dokumente"  
[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2-| Microsoft Edge Entwickler"  

[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++-Referenz | Microsoft-Dokumente"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft-Dokumente"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Windows Laufzeit-C++-Vorlagenbibliothek (WRL) | Microsoft-Dokumente"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Walkthrough: Create a traditional Windows Desktop application (C++) | Microsoft-Dokumente"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser – MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback – MicrosoftEdge/WebViewFeedback-| GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "WebView2-API-Beispiel – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Windows Implementierungsbibliotheken (WIL) – microsoft/wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2-Installationsprogramm"  
