---
description: Progressively enhance your PWA for Windows with native app features
title: Tailor your PWA (EdgeHTML) for Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: progressive web apps, PWA, Edge, Windows, WinRT, UWP, EdgeHTML
ms.openlocfilehash: 70a675b1a4057326463fb63c6a93abf8f428c677
ms.sourcegitcommit: 8510fdaa72c8940440133e4c5b36349997d94127
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/04/2020
ms.locfileid: "10905573"
---
# <span data-ttu-id="f27ab-104">Tailor your PWA (EdgeHTML) for Windows</span><span class="sxs-lookup"><span data-stu-id="f27ab-104">Tailor your PWA (EdgeHTML) for Windows</span></span>  

<span data-ttu-id="f27ab-105">PWAs installed on Windows 10 enjoy [all the benefits][PwaIndexWindows10] of running as [Universal Windows Platform \(UWP\)][WindowsUWPGetStartedGuide] apps, including protection through Windows app sandboxing security and full access to [Windows Runtime \(WinRT\))][UwpApiIndex] APIs, including those for:</span><span class="sxs-lookup"><span data-stu-id="f27ab-105">PWAs installed on Windows 10 enjoy [all the benefits][PwaIndexWindows10] of running as [Universal Windows Platform \(UWP\)][WindowsUWPGetStartedGuide] apps, including protection through Windows app sandboxing security and full access to [Windows Runtime \(WinRT\))][UwpApiIndex] APIs, including those for:</span></span>  

*   <span data-ttu-id="f27ab-106">Controlling device features \(such as camera, microphone, GPS\)</span><span class="sxs-lookup"><span data-stu-id="f27ab-106">Controlling device features \(such as camera, microphone, GPS\)</span></span>  
*   <span data-ttu-id="f27ab-107">Accessing user resources \(such as calendar, contacts, documents, music\)</span><span class="sxs-lookup"><span data-stu-id="f27ab-107">Accessing user resources \(such as calendar, contacts, documents, music\)</span></span>  
*   <span data-ttu-id="f27ab-108">Launching / navigating your app through Cortana voice commands</span><span class="sxs-lookup"><span data-stu-id="f27ab-108">Launching / navigating your app through Cortana voice commands</span></span>  
*   <span data-ttu-id="f27ab-109">Integrating with the Windows OS \(through the Windows Action Center, desktop taskbar, and context menus\)</span><span class="sxs-lookup"><span data-stu-id="f27ab-109">Integrating with the Windows OS \(through the Windows Action Center, desktop taskbar, and context menus\)</span></span>  

<span data-ttu-id="f27ab-110">These are only a few of the added possibilities for your PWA \(EdgeHTML\) on Windows.</span><span class="sxs-lookup"><span data-stu-id="f27ab-110">These are only a few of the added possibilities for your PWA \(EdgeHTML\) on Windows.</span></span>  

<span data-ttu-id="f27ab-111">This article shows you how to install, run, and enhance your PWA \(EdgeHTML\) as a Windows 10 app, while still ensuring cross-browser and cross-platform compatibility.</span><span class="sxs-lookup"><span data-stu-id="f27ab-111">This article shows you how to install, run, and enhance your PWA \(EdgeHTML\) as a Windows 10 app, while still ensuring cross-browser and cross-platform compatibility.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f27ab-112">The examples and steps in this article require Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="f27ab-112">The examples and steps in this article require Visual Studio 2017.</span></span> <span data-ttu-id="f27ab-113">Visual Studio 2019 does not include the template used in this article.</span><span class="sxs-lookup"><span data-stu-id="f27ab-113">Visual Studio 2019 does not include the template used in this article.</span></span> <span data-ttu-id="f27ab-114">To download Visual Studio 2017, see [Visual Studio Downloads - 2017, 2015 & Previous Versions][PreviousVSDownloads]</span><span class="sxs-lookup"><span data-stu-id="f27ab-114">To download Visual Studio 2017, see [Visual Studio Downloads - 2017, 2015 & Previous Versions][PreviousVSDownloads]</span></span>  


## <span data-ttu-id="f27ab-115">Prerequisites</span><span class="sxs-lookup"><span data-stu-id="f27ab-115">Prerequisites</span></span>  

*   <span data-ttu-id="f27ab-116">An existing PWA \(or hosted web app\), either a live or localhost site.</span><span class="sxs-lookup"><span data-stu-id="f27ab-116">An existing PWA \(or hosted web app\), either a live or localhost site.</span></span>  <span data-ttu-id="f27ab-117">This guide uses the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted].</span><span class="sxs-lookup"><span data-stu-id="f27ab-117">This guide uses the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted].</span></span>  
*   <span data-ttu-id="f27ab-118">Download the \(free\) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].</span><span class="sxs-lookup"><span data-stu-id="f27ab-118">Download the \(free\) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].</span></span>  <span data-ttu-id="f27ab-119">You are also able to use the Professional, Enterprise, or [Preview][MicrosoftVisualStudioPreview] editions.</span><span class="sxs-lookup"><span data-stu-id="f27ab-119">You are also able to use the Professional, Enterprise, or [Preview][MicrosoftVisualStudioPreview] editions.</span></span>  <span data-ttu-id="f27ab-120">From the Visual Studio Installer, choose the following Workloads:</span><span class="sxs-lookup"><span data-stu-id="f27ab-120">From the Visual Studio Installer, choose the following Workloads:</span></span>  
    *   **<span data-ttu-id="f27ab-121">Universal Windows Platform development</span><span class="sxs-lookup"><span data-stu-id="f27ab-121">Universal Windows Platform development</span></span>**  

## <span data-ttu-id="f27ab-122">Set up and run your Universal Windows app</span><span class="sxs-lookup"><span data-stu-id="f27ab-122">Set up and run your Universal Windows app</span></span>  

<span data-ttu-id="f27ab-123">A PWA \(EdgeHTML\) installed as a Windows 10 app runs independently from the browser, in a standalone \(`WWAHost.exe` process\) window.</span><span class="sxs-lookup"><span data-stu-id="f27ab-123">A PWA \(EdgeHTML\) installed as a Windows 10 app runs independently from the browser, in a standalone \(`WWAHost.exe` process\) window.</span></span>  <span data-ttu-id="f27ab-124">Enabling this simply requires a lightweight app wrapper that contains your hosted web app, which you are able to quickly set up using the Visual Studio `Progressive Web App (Universal Windows)` project template.</span><span class="sxs-lookup"><span data-stu-id="f27ab-124">Enabling this simply requires a lightweight app wrapper that contains your hosted web app, which you are able to quickly set up using the Visual Studio `Progressive Web App (Universal Windows)` project template.</span></span>  <span data-ttu-id="f27ab-125">\(All your app logic, including sending native Windows Runtime API requests, still happens in your original web app code.\)</span><span class="sxs-lookup"><span data-stu-id="f27ab-125">\(All your app logic, including sending native Windows Runtime API requests, still happens in your original web app code.\)</span></span>  

<span data-ttu-id="f27ab-126">Set up your Windows app development environment in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f27ab-126">Set up your Windows app development environment in Visual Studio.</span></span>  

1.  <span data-ttu-id="f27ab-127">In your Windows Settings, turn on [Developer mode][WindowsUWPGetStartedEnable].</span><span class="sxs-lookup"><span data-stu-id="f27ab-127">In your Windows Settings, turn on [Developer mode][WindowsUWPGetStartedEnable].</span></span>  <span data-ttu-id="f27ab-128">\(Type `developer mode` in the Windows searchbar to find it.\)</span><span class="sxs-lookup"><span data-stu-id="f27ab-128">\(Type `developer mode` in the Windows searchbar to find it.\)</span></span>  
1.  <span data-ttu-id="f27ab-129">Launch Visual Studio and select **Create a new project...**.</span><span class="sxs-lookup"><span data-stu-id="f27ab-129">Launch Visual Studio and select **Create a new project...**.</span></span>  
1.  <span data-ttu-id="f27ab-130">Choose **Javascript** > **Windows Universal** and select **Progressive Web App (Universal Windows)** from the list of project types in Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="f27ab-130">Choose **Javascript** > **Windows Universal** and select **Progressive Web App (Universal Windows)** from the list of project types in Visual Studio 2017.</span></span>  
1.  <span data-ttu-id="f27ab-131">Select the default Windows 10 `Target version` \(most recent release\) and `Minimum version` \(build 10586 or higher\) and choose **OK**.</span><span class="sxs-lookup"><span data-stu-id="f27ab-131">Select the default Windows 10 `Target version` \(most recent release\) and `Minimum version` \(build 10586 or higher\) and choose **OK**.</span></span>  

    ![Visual Studio selection dialog for UWP project target builds](media/vs-target-min-version.png)  

    <span data-ttu-id="f27ab-133">Your new project loads with the package.appxmanifest designer open.</span><span class="sxs-lookup"><span data-stu-id="f27ab-133">Your new project loads with the package.appxmanifest designer open.</span></span>  <span data-ttu-id="f27ab-134">This is where you configure the details of your app, including package identity, package dependencies, required capabilities, visual elements, and extensibility points.</span><span class="sxs-lookup"><span data-stu-id="f27ab-134">This is where you configure the details of your app, including package identity, package dependencies, required capabilities, visual elements, and extensibility points.</span></span>  <span data-ttu-id="f27ab-135">This is an easily configurable, temporary version of the app package manifest used during app development.</span><span class="sxs-lookup"><span data-stu-id="f27ab-135">This is an easily configurable, temporary version of the app package manifest used during app development.</span></span>  
    <span data-ttu-id="f27ab-136">When you build your app project, [Visual Studio generates an AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] file from this metadata, which is used to install and run your app.</span><span class="sxs-lookup"><span data-stu-id="f27ab-136">When you build your app project, [Visual Studio generates an AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] file from this metadata, which is used to install and run your app.</span></span>  <span data-ttu-id="f27ab-137">Whenever you update your `package.appxmanifest` file, be sure to rebuild the project so both are reflected in your `AppxManifest.xml` at runtime.</span><span class="sxs-lookup"><span data-stu-id="f27ab-137">Whenever you update your `package.appxmanifest` file, be sure to rebuild the project so both are reflected in your `AppxManifest.xml` at runtime.</span></span>  

1.  <span data-ttu-id="f27ab-138">In the manifest designer **Application** panel, enter the URL of your PWA as the `Start page`.</span><span class="sxs-lookup"><span data-stu-id="f27ab-138">In the manifest designer **Application** panel, enter the URL of your PWA as the `Start page`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f27ab-139">Service workers are supported for all https \(secure, remote\) urls specified as the `StartPage`.</span><span class="sxs-lookup"><span data-stu-id="f27ab-139">Service workers are supported for all https \(secure, remote\) urls specified as the `StartPage`.</span></span>  <span data-ttu-id="f27ab-140">Service workers are not supported by default for web apps that specify a local start page.</span><span class="sxs-lookup"><span data-stu-id="f27ab-140">Service workers are not supported by default for web apps that specify a local start page.</span></span>  <span data-ttu-id="f27ab-141">To enable service worker support for these cases, add an explicit [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) entry to the manifest, for example:</span><span class="sxs-lookup"><span data-stu-id="f27ab-141">To enable service worker support for these cases, add an explicit [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) entry to the manifest, for example:</span></span> `<uap:Rule Match="http://web-platform.test/" Type="include" uap5:ServiceWorker="true"/>`  
    
    ![Application panel of package.appxmanifest designer](media/vs-manifest-application.png)  
    
    <span data-ttu-id="f27ab-143">You are able to also modify the `Display name` and `Description` as you like.</span><span class="sxs-lookup"><span data-stu-id="f27ab-143">You are able to also modify the `Display name` and `Description` as you like.</span></span>  
1.  <span data-ttu-id="f27ab-144">Save this file \(or another 512x512 image of your choosing\) to your desktop.</span><span class="sxs-lookup"><span data-stu-id="f27ab-144">Save this file \(or another 512x512 image of your choosing\) to your desktop.</span></span>  
    <span data-ttu-id="f27ab-145">Then, in the manifest designer **Visual Assets** panel, click on the `Source` field **...** button, select it as your source file, and click **Generate**.</span><span class="sxs-lookup"><span data-stu-id="f27ab-145">Then, in the manifest designer **Visual Assets** panel, click on the `Source` field **...** button, select it as your source file, and click **Generate**.</span></span>  <span data-ttu-id="f27ab-146">\(Then click **OK** to overwrite the default placeholder images\).</span><span class="sxs-lookup"><span data-stu-id="f27ab-146">\(Then click **OK** to overwrite the default placeholder images\).</span></span>  
    
    ![Visual Assets panel of package.appxmanifest designer](media/vs-manifest-visual-assets.png)  
    
    <span data-ttu-id="f27ab-148">This generates the basic visual assets for installing, running, launching, and distributing your app in the store.</span><span class="sxs-lookup"><span data-stu-id="f27ab-148">This generates the basic visual assets for installing, running, launching, and distributing your app in the store.</span></span>  
    <span data-ttu-id="f27ab-149">If you see any red \(`X`\) errors indicating missing images, you are able to click on the **...** buttons to manually select a file from the generated images.</span><span class="sxs-lookup"><span data-stu-id="f27ab-149">If you see any red \(`X`\) errors indicating missing images, you are able to click on the **...** buttons to manually select a file from the generated images.</span></span>  
1.  <span data-ttu-id="f27ab-150">In the manifest designer **Content URIs** panel, replace `http://example.com` with the location of your PWA \(such that `Rule` = `include` and `WinRT Access` = `All`\).</span><span class="sxs-lookup"><span data-stu-id="f27ab-150">In the manifest designer **Content URIs** panel, replace `http://example.com` with the location of your PWA \(such that `Rule` = `include` and `WinRT Access` = `All`\).</span></span>  
    <span data-ttu-id="f27ab-151">This grants your PWA permission to send native Windows Runtime \(WinRT\) API requests when running as a Windows 10 app, which is covered a bit later.</span><span class="sxs-lookup"><span data-stu-id="f27ab-151">This grants your PWA permission to send native Windows Runtime \(WinRT\) API requests when running as a Windows 10 app, which is covered a bit later.</span></span>   <span data-ttu-id="f27ab-152">If your actual PWA does not require WinRT access, you are able to switch the `WinRT Access` value to `None`.</span><span class="sxs-lookup"><span data-stu-id="f27ab-152">If your actual PWA does not require WinRT access, you are able to switch the `WinRT Access` value to `None`.</span></span>  <span data-ttu-id="f27ab-153">Either way, be sure to sub out the default `http://example.com` string with the URI of your PWA, or your app is not able to properly load at runtime.</span><span class="sxs-lookup"><span data-stu-id="f27ab-153">Either way, be sure to sub out the default `http://example.com` string with the URI of your PWA, or your app is not able to properly load at runtime.</span></span>  
    <span data-ttu-id="f27ab-154">You are ready to run and debug your PWA as a Windows 10 app.</span><span class="sxs-lookup"><span data-stu-id="f27ab-154">You are ready to run and debug your PWA as a Windows 10 app.</span></span>  <span data-ttu-id="f27ab-155">If you are using a localhost site to step through this guide, make sure it is running.</span><span class="sxs-lookup"><span data-stu-id="f27ab-155">If you are using a localhost site to step through this guide, make sure it is running.</span></span>  <span data-ttu-id="f27ab-156">Then,</span><span class="sxs-lookup"><span data-stu-id="f27ab-156">Then,</span></span>  
1.  <span data-ttu-id="f27ab-157">Build \(`Ctrl`+`Shift`+`F5`\) and Run \(`F5`\) your PWA project.</span><span class="sxs-lookup"><span data-stu-id="f27ab-157">Build \(`Ctrl`+`Shift`+`F5`\) and Run \(`F5`\) your PWA project.</span></span>  <span data-ttu-id="f27ab-158">Your website should now launch in a standalone app window.</span><span class="sxs-lookup"><span data-stu-id="f27ab-158">Your website should now launch in a standalone app window.</span></span>  <span data-ttu-id="f27ab-159">Not only is it a hosted web app; it is running as a Progressive Web App installed on Windows 10!</span><span class="sxs-lookup"><span data-stu-id="f27ab-159">Not only is it a hosted web app; it is running as a Progressive Web App installed on Windows 10!</span></span>  

    ![PWA running in a WWAHost.exe window](media/wwahost.png)  

## <span data-ttu-id="f27ab-161">Debug your PWA \(EdgeHTML\) as a Windows app</span><span class="sxs-lookup"><span data-stu-id="f27ab-161">Debug your PWA \(EdgeHTML\) as a Windows app</span></span>  

<span data-ttu-id="f27ab-162">Because a PWA \(EdgeHTML\) is simply a progressively enhanced hosted web app, you are able to debug your server-side code the same as any web app, using your usual IDE and workflow.</span><span class="sxs-lookup"><span data-stu-id="f27ab-162">Because a PWA \(EdgeHTML\) is simply a progressively enhanced hosted web app, you are able to debug your server-side code the same as any web app, using your usual IDE and workflow.</span></span>  <span data-ttu-id="f27ab-163">The changes you deploy live are reflected in your installed PWA the next time you launch it \(no need to redeploy your Universal Windows app package\).</span><span class="sxs-lookup"><span data-stu-id="f27ab-163">The changes you deploy live are reflected in your installed PWA the next time you launch it \(no need to redeploy your Universal Windows app package\).</span></span>

<span data-ttu-id="f27ab-164">For client-side debugging within your Windows 10 app, you must have the `Microsoft Edge DevTools Preview` app.</span><span class="sxs-lookup"><span data-stu-id="f27ab-164">For client-side debugging within your Windows 10 app, you must have the `Microsoft Edge DevTools Preview` app.</span></span>  <span data-ttu-id="f27ab-165">This standalone app includes all the functionality of the original in-browser [Microsoft Edge DevTools][DevToolsGuide] \(including [PWA tools][DevToolsGuideServiceWorkers]\), plus basic [remote debugging][DevToolsProtocol01ClientsEdgePreview] support and a [Debug Target chooser][DevToolsGuideMicrosoftStoreApp] for attaching to any running instance of the EdgeHTML engine, including add-ins for Office, Cortana, app webviews, and of course, PWAs running on Windows.</span><span class="sxs-lookup"><span data-stu-id="f27ab-165">This standalone app includes all the functionality of the original in-browser [Microsoft Edge DevTools][DevToolsGuide] \(including [PWA tools][DevToolsGuideServiceWorkers]\), plus basic [remote debugging][DevToolsProtocol01ClientsEdgePreview] support and a [Debug Target chooser][DevToolsGuideMicrosoftStoreApp] for attaching to any running instance of the EdgeHTML engine, including add-ins for Office, Cortana, app webviews, and of course, PWAs running on Windows.</span></span>  

<span data-ttu-id="f27ab-166">Here is how to set up debugging for your PWA \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="f27ab-166">Here is how to set up debugging for your PWA \(EdgeHTML\).</span></span>  

1.  <span data-ttu-id="f27ab-167">Install the [Microsoft Edge DevTools Preview][MicrosoftStoreEdgeDevtoolsPreview] app from the Microsoft Store if you do not already have it.</span><span class="sxs-lookup"><span data-stu-id="f27ab-167">Install the [Microsoft Edge DevTools Preview][MicrosoftStoreEdgeDevtoolsPreview] app from the Microsoft Store if you do not already have it.</span></span>  
1.  <span data-ttu-id="f27ab-168">With your PWA site up and running, launch the DevTools app.</span><span class="sxs-lookup"><span data-stu-id="f27ab-168">With your PWA site up and running, launch the DevTools app.</span></span>  
1.  <span data-ttu-id="f27ab-169">From Visual Studio, launch your Windows 10 app with the `Start Without Debugging` (`Ctrl`+`F5`) command.</span><span class="sxs-lookup"><span data-stu-id="f27ab-169">From Visual Studio, launch your Windows 10 app with the `Start Without Debugging` (`Ctrl`+`F5`) command.</span></span>  <span data-ttu-id="f27ab-170">\(The DevTools app does not attach properly if the Visual Studio debugger is active.\)</span><span class="sxs-lookup"><span data-stu-id="f27ab-170">\(The DevTools app does not attach properly if the Visual Studio debugger is active.\)</span></span>  
1.  <span data-ttu-id="f27ab-171">In the DevTools app, click the **Refresh** button in the Local debug target chooser.</span><span class="sxs-lookup"><span data-stu-id="f27ab-171">In the DevTools app, click the **Refresh** button in the Local debug target chooser.</span></span>  <span data-ttu-id="f27ab-172">Your PWA \(EdgeHTML\) site should now be listed.</span><span class="sxs-lookup"><span data-stu-id="f27ab-172">Your PWA \(EdgeHTML\) site should now be listed.</span></span>  <span data-ttu-id="f27ab-173">\(If it is also running in a browser window, it is the last instance of that site in the list.\)</span><span class="sxs-lookup"><span data-stu-id="f27ab-173">\(If it is also running in a browser window, it is the last instance of that site in the list.\)</span></span>  
1.  <span data-ttu-id="f27ab-174">Click on your PWA \(EdgeHTML\) site listing to open a new DevTools instance tab and start debugging.</span><span class="sxs-lookup"><span data-stu-id="f27ab-174">Click on your PWA \(EdgeHTML\) site listing to open a new DevTools instance tab and start debugging.</span></span>  
    
    ![Local Debug Targets chooser in the Microsoft Edge DevTools app](media/devtools-local.png)  
    
1.  <span data-ttu-id="f27ab-176">You are able to verify that DevTools is attached to your PWA-running-as-Windows-app.</span><span class="sxs-lookup"><span data-stu-id="f27ab-176">You are able to verify that DevTools is attached to your PWA-running-as-Windows-app.</span></span>  <span data-ttu-id="f27ab-177">In the DevTools **Console**, type:</span><span class="sxs-lookup"><span data-stu-id="f27ab-177">In the DevTools **Console**, type:</span></span>  
    
    ```shell
    window.Windows
    ```  
    
    <span data-ttu-id="f27ab-178">This returns the global `Windows Runtime` object containing all of the [top-level WinRT namespaces](#find-windows-runtime-winrt-apis).</span><span class="sxs-lookup"><span data-stu-id="f27ab-178">This returns the global `Windows Runtime` object containing all of the [top-level WinRT namespaces](#find-windows-runtime-winrt-apis).</span></span>  <span data-ttu-id="f27ab-179">This is your PWA \(EdgeHTML\) entrypoint to the [Universal Windows Platform][WindowsUWPIndex], and only exposed to web apps that run as Windows 10 apps (running outside the browser, in a `WWAHost.exe` process).</span><span class="sxs-lookup"><span data-stu-id="f27ab-179">This is your PWA \(EdgeHTML\) entrypoint to the [Universal Windows Platform][WindowsUWPIndex], and only exposed to web apps that run as Windows 10 apps (running outside the browser, in a `WWAHost.exe` process).</span></span>  
    
## <span data-ttu-id="f27ab-180">Find Windows Runtime (WinRT) APIs</span><span class="sxs-lookup"><span data-stu-id="f27ab-180">Find Windows Runtime (WinRT) APIs</span></span>  

<span data-ttu-id="f27ab-181">As an installed Windows app, your [PWA \(EdgeHTML\) has full access to native Windows Runtime APIs][WindowsRuntime]; identify what you need to use, obtain the requisite permissions, and employ feature detection to send that API request on supported environments.</span><span class="sxs-lookup"><span data-stu-id="f27ab-181">As an installed Windows app, your [PWA \(EdgeHTML\) has full access to native Windows Runtime APIs][WindowsRuntime]; identify what you need to use, obtain the requisite permissions, and employ feature detection to send that API request on supported environments.</span></span>  <span data-ttu-id="f27ab-182">Walk through this process to add a progressive enhancement for Windows desktop users of your PWA.</span><span class="sxs-lookup"><span data-stu-id="f27ab-182">Walk through this process to add a progressive enhancement for Windows desktop users of your PWA.</span></span>  

<span data-ttu-id="f27ab-183">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for PWAs on Windows.</span><span class="sxs-lookup"><span data-stu-id="f27ab-183">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for PWAs on Windows.</span></span>

<span data-ttu-id="f27ab-184">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for [PWAs on Windows 10 (EdgeHTML)][PwaIndexWindows10].</span><span class="sxs-lookup"><span data-stu-id="f27ab-184">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for [PWAs on Windows 10 (EdgeHTML)][PwaIndexWindows10].</span></span>  

<span data-ttu-id="f27ab-185">Overall, WinRT APIs work in JavaScript the same way they do in C#, so you may follow the general [Universal Windows Platform documentation][WindowsUWPIndex] and [API Reference][UwpApiIndex] for usage.</span><span class="sxs-lookup"><span data-stu-id="f27ab-185">Overall, WinRT APIs work in JavaScript the same way they do in C#, so you may follow the general [Universal Windows Platform documentation][WindowsUWPIndex] and [API Reference][UwpApiIndex] for usage.</span></span>  <span data-ttu-id="f27ab-186">However, please note the following differences:</span><span class="sxs-lookup"><span data-stu-id="f27ab-186">However, please note the following differences:</span></span>  

*   <span data-ttu-id="f27ab-187">WinRT features in JavaScript use  [different casing conventions][ScriptingJsinrtUsingWinRTCasingConventions]</span><span class="sxs-lookup"><span data-stu-id="f27ab-187">WinRT features in JavaScript use  [different casing conventions][ScriptingJsinrtUsingWinRTCasingConventions]</span></span>  
*   <span data-ttu-id="f27ab-188">[Events are represented as string identifiers][ScriptingJsinrtHandlingWinRTEvents] passed to class `addEventListener`/`removeEventListener` methods</span><span class="sxs-lookup"><span data-stu-id="f27ab-188">[Events are represented as string identifiers][ScriptingJsinrtHandlingWinRTEvents] passed to class `addEventListener`/`removeEventListener` methods</span></span>  
*   <span data-ttu-id="f27ab-189">[Asynchronous methods][ScriptingJsinrtUsingWinRT] use the JavaScript Promise model</span><span class="sxs-lookup"><span data-stu-id="f27ab-189">[Asynchronous methods][ScriptingJsinrtUsingWinRT] use the JavaScript Promise model</span></span>  
*   <span data-ttu-id="f27ab-190">APIs in the `Windows.UI.Xaml` namespace are not supported for JavaScript apps, which instead use the [EdgeHTML][DevGuideWhatsNew] engine web rendering stack \(HTML, CSS\)</span><span class="sxs-lookup"><span data-stu-id="f27ab-190">APIs in the `Windows.UI.Xaml` namespace are not supported for JavaScript apps, which instead use the [EdgeHTML][DevGuideWhatsNew] engine web rendering stack \(HTML, CSS\)</span></span>  

<span data-ttu-id="f27ab-191">For more details, see [Using the Windows Runtime in JavaScript][WindowRuntimeUsingJavascript].</span><span class="sxs-lookup"><span data-stu-id="f27ab-191">For more details, see [Using the Windows Runtime in JavaScript][WindowRuntimeUsingJavascript].</span></span>  

### <span data-ttu-id="f27ab-192">UWP code samples</span><span class="sxs-lookup"><span data-stu-id="f27ab-192">UWP code samples</span></span>  

<span data-ttu-id="f27ab-193">Check out the [Universal Windows Platform \(UWP\) Code Samples][MicrosoftDeveloperWindowsSamples] repo to browse JavaScript examples for common Windows 10 app scenarios.</span><span class="sxs-lookup"><span data-stu-id="f27ab-193">Check out the [Universal Windows Platform \(UWP\) Code Samples][MicrosoftDeveloperWindowsSamples] repo to browse JavaScript examples for common Windows 10 app scenarios.</span></span>  <span data-ttu-id="f27ab-194">Although the JS versions of these samples use the [WinJS][GithubWinjsWinjs] library to structure the sample template, WinJS is not required for sending the WinRT API requests demonstrated in these samples.</span><span class="sxs-lookup"><span data-stu-id="f27ab-194">Although the JS versions of these samples use the [WinJS][GithubWinjsWinjs] library to structure the sample template, WinJS is not required for sending the WinRT API requests demonstrated in these samples.</span></span>  

> [!NOTE]
> <span data-ttu-id="f27ab-195">If you need to listen for the [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] event for the app, you are able to do this using the following native WinRT API:</span><span class="sxs-lookup"><span data-stu-id="f27ab-195">If you need to listen for the [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] event for the app, you are able to do this using the following native WinRT API:</span></span>  
> 
> **<span data-ttu-id="f27ab-196">Use this</span><span class="sxs-lookup"><span data-stu-id="f27ab-196">Use this</span></span>**  
> 
> ```javascript
> Windows.UI.WebUI.WebUIApplication.addEventListener("activated", function (activatedEventArgs) {
>     // Check activatedEventArgs.kind and respond as needed
> });
> ```  
> 
> <span data-ttu-id="f27ab-197">... as opposed this type of WinJS request used in the samples:</span><span class="sxs-lookup"><span data-stu-id="f27ab-197">... as opposed this type of WinJS request used in the samples:</span></span>  
> 
> **<span data-ttu-id="f27ab-198">Not this</span><span class="sxs-lookup"><span data-stu-id="f27ab-198">Not this</span></span>**  
> 
> ```javascript
>     var page = WinJS.UI.Pages.define("/html/scenario1-launched.html", {
>         ready: function (element, options) {
>             // Check options.activationKind and respond as needed
>         }
>     });
> ```  

## <span data-ttu-id="f27ab-199">Send WinRT API requests from your PWA (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="f27ab-199">Send WinRT API requests from your PWA (EdgeHTML)</span></span>  

<span data-ttu-id="f27ab-200">At this point, pretend you want to add a custom context menu for Windows users of our PWA \(EdgeHTML\) and have identified the APIs you need in the [Windows.UI.Popups][UwpApiWindowsUiPopups] namespace.</span><span class="sxs-lookup"><span data-stu-id="f27ab-200">At this point, pretend you want to add a custom context menu for Windows users of our PWA \(EdgeHTML\) and have identified the APIs you need in the [Windows.UI.Popups][UwpApiWindowsUiPopups] namespace.</span></span>  

<span data-ttu-id="f27ab-201">In order to send any WinRT APIs requests from our PWA \(EdgeHTML\), you first need to [establish the requisite permissions](#set-application-content-uri-rules-acurs) \(or, Application Content URI Rules\) in your Windows app package manifest \(`.appxmanifest`\) file.</span><span class="sxs-lookup"><span data-stu-id="f27ab-201">In order to send any WinRT APIs requests from our PWA \(EdgeHTML\), you first need to [establish the requisite permissions](#set-application-content-uri-rules-acurs) \(or, Application Content URI Rules\) in your Windows app package manifest \(`.appxmanifest`\) file.</span></span>  

<span data-ttu-id="f27ab-202">If any of these API requests involve access to user resources like pictures or music, or to device features like the camera or microphone, you also need to add [app capability declarations](#app-capability-declarations) to the app package manifest in order for Windows to prompt the user for permission.</span><span class="sxs-lookup"><span data-stu-id="f27ab-202">If any of these API requests involve access to user resources like pictures or music, or to device features like the camera or microphone, you also need to add [app capability declarations](#app-capability-declarations) to the app package manifest in order for Windows to prompt the user for permission.</span></span>  <span data-ttu-id="f27ab-203">If you later publish your PWA \(EdgeHTML\) to the Microsoft Store, these required [App permissions][MicrosoftSupportWindowsAppPermissions] are also noted in your store listing.</span><span class="sxs-lookup"><span data-stu-id="f27ab-203">If you later publish your PWA \(EdgeHTML\) to the Microsoft Store, these required [App permissions][MicrosoftSupportWindowsAppPermissions] are also noted in your store listing.</span></span>  

#### <span data-ttu-id="f27ab-204">Set Application Content URI Rules (ACURs)</span><span class="sxs-lookup"><span data-stu-id="f27ab-204">Set Application Content URI Rules (ACURs)</span></span>  

<span data-ttu-id="f27ab-205">Through ACURs, otherwise known as a URL allow list, you are able to give the URLs of your PWA \(EdgeHTML\) direct access to Windows Runtime APIs.</span><span class="sxs-lookup"><span data-stu-id="f27ab-205">Through ACURs, otherwise known as a URL allow list, you are able to give the URLs of your PWA \(EdgeHTML\) direct access to Windows Runtime APIs.</span></span>  <span data-ttu-id="f27ab-206">At the Windows OS level, the right policy bounds are set to allow code hosted on your web server to directly send platform API requests.</span><span class="sxs-lookup"><span data-stu-id="f27ab-206">At the Windows OS level, the right policy bounds are set to allow code hosted on your web server to directly send platform API requests.</span></span>  <span data-ttu-id="f27ab-207">You define these bounds in the app package manifest file when you specify your PWA URLs as `ApplicationContentUriRules`.</span><span class="sxs-lookup"><span data-stu-id="f27ab-207">You define these bounds in the app package manifest file when you specify your PWA URLs as `ApplicationContentUriRules`.</span></span>  

<span data-ttu-id="f27ab-208">Your rules should include the start page for your app and any other pages you want included as app pages.</span><span class="sxs-lookup"><span data-stu-id="f27ab-208">Your rules should include the start page for your app and any other pages you want included as app pages.</span></span>  <span data-ttu-id="f27ab-209">If your user navigates to a URL that is not included in your rules, Windows opens the target URL in the Microsoft Edge browser rather than your standalone PWA \(EdgeHTML\) window \(`WWAHost.exe` process\).</span><span class="sxs-lookup"><span data-stu-id="f27ab-209">If your user navigates to a URL that is not included in your rules, Windows opens the target URL in the Microsoft Edge browser rather than your standalone PWA \(EdgeHTML\) window \(`WWAHost.exe` process\).</span></span>  <span data-ttu-id="f27ab-210">You may also exclude specific URLs.</span><span class="sxs-lookup"><span data-stu-id="f27ab-210">You may also exclude specific URLs.</span></span>  

<span data-ttu-id="f27ab-211">There are several ways to specify a URL `Match` in your rules:</span><span class="sxs-lookup"><span data-stu-id="f27ab-211">There are several ways to specify a URL `Match` in your rules:</span></span>  

*   <span data-ttu-id="f27ab-212">An exact hostname</span><span class="sxs-lookup"><span data-stu-id="f27ab-212">An exact hostname</span></span>  
*   <span data-ttu-id="f27ab-213">Ein Hostname, für den ein URI mit einer Unterdomäne dieses Hostnamens einbezogen oder ausgeschlossen wird</span><span class="sxs-lookup"><span data-stu-id="f27ab-213">A hostname for which a URI with any subdomain of that hostname is included or excluded</span></span>  
*   <span data-ttu-id="f27ab-214">An exact URI</span><span class="sxs-lookup"><span data-stu-id="f27ab-214">An exact URI</span></span>  
*   <span data-ttu-id="f27ab-215">An exact URI containing a query property</span><span class="sxs-lookup"><span data-stu-id="f27ab-215">An exact URI containing a query property</span></span>  
*   <span data-ttu-id="f27ab-216">A partial path and a wildcard to indicate a particular file extension for an include rule</span><span class="sxs-lookup"><span data-stu-id="f27ab-216">A partial path and a wildcard to indicate a particular file extension for an include rule</span></span>  
*   <span data-ttu-id="f27ab-217">Relative paths for exclude rules</span><span class="sxs-lookup"><span data-stu-id="f27ab-217">Relative paths for exclude rules</span></span>  

<span data-ttu-id="f27ab-218">Here are a few examples of ACURs in a `.appxmanifest` file:</span><span class="sxs-lookup"><span data-stu-id="f27ab-218">Here are a few examples of ACURs in a `.appxmanifest` file:</span></span>  

```xml
<Application
Id="App"
StartPage="https://contoso.com/home">
<uap:ApplicationContentUriRules>
    <uap:Rule Type="include" Match="https://contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="include" Match="https://*.contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="exclude" Match="https://contoso.com/excludethispage.aspx" />
</uap:ApplicationContentUriRules>
```  

<span data-ttu-id="f27ab-219">URLs defined within the ACURs for your app are able to be granted permission to the Windows Runtime through the `WindowsRuntimeAccess` attribute, which accepts the following values:</span><span class="sxs-lookup"><span data-stu-id="f27ab-219">URLs defined within the ACURs for your app are able to be granted permission to the Windows Runtime through the `WindowsRuntimeAccess` attribute, which accepts the following values:</span></span>  

*   `all`<span data-ttu-id="f27ab-220">: Remote JavaScript code has access to all WinRT APIs and any local packaged components.</span><span class="sxs-lookup"><span data-stu-id="f27ab-220">: Remote JavaScript code has access to all WinRT APIs and any local packaged components.</span></span>  <span data-ttu-id="f27ab-221">The [Windows \(WinRT\))][UwpApiIndex] namespace is injected and present in the script engine.</span><span class="sxs-lookup"><span data-stu-id="f27ab-221">The [Windows \(WinRT\))][UwpApiIndex] namespace is injected and present in the script engine.</span></span>  
*   `allowForWeb`<span data-ttu-id="f27ab-222">: Remote JavaScript code access is limited to local packaged components, including custom C++/C# components.</span><span class="sxs-lookup"><span data-stu-id="f27ab-222">: Remote JavaScript code access is limited to local packaged components, including custom C++/C# components.</span></span>  
*   `none`<span data-ttu-id="f27ab-223">: Default.</span><span class="sxs-lookup"><span data-stu-id="f27ab-223">: Default.</span></span>  <span data-ttu-id="f27ab-224">The specified URL has no platform access.</span><span class="sxs-lookup"><span data-stu-id="f27ab-224">The specified URL has no platform access.</span></span>  

<span data-ttu-id="f27ab-225">In this tutorial, you already set the only ACUR that you need \(Step 6 of the previous [Set up and run your app](#set-up-and-run-your-universal-windows-app) section\) for your single-page app.</span><span class="sxs-lookup"><span data-stu-id="f27ab-225">In this tutorial, you already set the only ACUR that you need \(Step 6 of the previous [Set up and run your app](#set-up-and-run-your-universal-windows-app) section\) for your single-page app.</span></span>  <span data-ttu-id="f27ab-226">You are able to confirm this from the **Content URIs** panel of the Visual Studio `package.appxmanifest` designer.</span><span class="sxs-lookup"><span data-stu-id="f27ab-226">You are able to confirm this from the **Content URIs** panel of the Visual Studio `package.appxmanifest` designer.</span></span>  

![Content URI panel of the Visual Studio appxmanifest designer](media/vs-appxmanifest-editor-acurs.png)  

<span data-ttu-id="f27ab-228">You are also able to view the raw XML of your manifest by right-clicking your `package.appxmanifest` file in Visual Studio Solution Explorer and selecting **View Code** \(`F7`\).</span><span class="sxs-lookup"><span data-stu-id="f27ab-228">You are also able to view the raw XML of your manifest by right-clicking your `package.appxmanifest` file in Visual Studio Solution Explorer and selecting **View Code** \(`F7`\).</span></span>  <span data-ttu-id="f27ab-229">To toggle back to the Designer view, select **View Designer** \(`Shift`+`F7`\).</span><span class="sxs-lookup"><span data-stu-id="f27ab-229">To toggle back to the Designer view, select **View Designer** \(`Shift`+`F7`\).</span></span>  

#### <span data-ttu-id="f27ab-230">App capability declarations</span><span class="sxs-lookup"><span data-stu-id="f27ab-230">App capability declarations</span></span>  

<span data-ttu-id="f27ab-231">If your app needs programmatic access to user resources like pictures or music, or to devices like a camera or a microphone, you must include the corresponding [App capability declarations][WindowsUwpPackagingAppCapabilities] in your app package manifest file.</span><span class="sxs-lookup"><span data-stu-id="f27ab-231">If your app needs programmatic access to user resources like pictures or music, or to devices like a camera or a microphone, you must include the corresponding [App capability declarations][WindowsUwpPackagingAppCapabilities] in your app package manifest file.</span></span>  <span data-ttu-id="f27ab-232">There are three app capability declaration categories:</span><span class="sxs-lookup"><span data-stu-id="f27ab-232">There are three app capability declaration categories:</span></span>  

*   <span data-ttu-id="f27ab-233">[Funktionen zur allgemeinen Verwendung][WindowsUwpPackagingAppCapabilitiesGeneralUse], die auf die meisten allgemeinen App-Szenarien zutreffen.</span><span class="sxs-lookup"><span data-stu-id="f27ab-233">[General-use capabilities][WindowsUwpPackagingAppCapabilitiesGeneralUse] that apply to most common app scenarios.</span></span>  
*   <span data-ttu-id="f27ab-234">[Device capabilities][WindowsUwpPackagingAppCapabilitiesDevice] that allow your app to access peripheral and internal devices.</span><span class="sxs-lookup"><span data-stu-id="f27ab-234">[Device capabilities][WindowsUwpPackagingAppCapabilitiesDevice] that allow your app to access peripheral and internal devices.</span></span>  
*   <span data-ttu-id="f27ab-235">[Special-use capabilities][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] that support enterprise scenarios and require a Microsoft Store company account.</span><span class="sxs-lookup"><span data-stu-id="f27ab-235">[Special-use capabilities][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] that support enterprise scenarios and require a Microsoft Store company account.</span></span>  <span data-ttu-id="f27ab-236">For more info about company accounts, see [Account types, locations, and fees][WindowsUwpPublishAccountTypesLocationsFees].</span><span class="sxs-lookup"><span data-stu-id="f27ab-236">For more info about company accounts, see [Account types, locations, and fees][WindowsUwpPublishAccountTypesLocationsFees].</span></span>

<span data-ttu-id="f27ab-237">Your Microsoft Store app page lists all the capabilities you declare in your app package manifest, so be sure to only specify the capabilities that your app actually uses.</span><span class="sxs-lookup"><span data-stu-id="f27ab-237">Your Microsoft Store app page lists all the capabilities you declare in your app package manifest, so be sure to only specify the capabilities that your app actually uses.</span></span>

<span data-ttu-id="f27ab-238">Some capabilities provide apps access to sensitive resources.</span><span class="sxs-lookup"><span data-stu-id="f27ab-238">Some capabilities provide apps access to sensitive resources.</span></span>  <span data-ttu-id="f27ab-239">These resources are considered sensitive because each is able to access the user's personal data or cost the user money.</span><span class="sxs-lookup"><span data-stu-id="f27ab-239">These resources are considered sensitive because each is able to access the user's personal data or cost the user money.</span></span>  <span data-ttu-id="f27ab-240">Privacy settings, managed by the Windows 10 [Settings][BingResultsWindows10Settings] app, let the user dynamically control access to sensitive resources.</span><span class="sxs-lookup"><span data-stu-id="f27ab-240">Privacy settings, managed by the Windows 10 [Settings][BingResultsWindows10Settings] app, let the user dynamically control access to sensitive resources.</span></span>  <span data-ttu-id="f27ab-241">Thus, it is important that your app does not assume a sensitive resource is always available.</span><span class="sxs-lookup"><span data-stu-id="f27ab-241">Thus, it is important that your app does not assume a sensitive resource is always available.</span></span>  <span data-ttu-id="f27ab-242">For more info about accessing sensitive resources, see [Guidelines for privacy-aware apps][WindowsUwp|::ref2::|Index].</span><span class="sxs-lookup"><span data-stu-id="f27ab-242">For more info about accessing sensitive resources, see [Guidelines for privacy-aware apps][WindowsUwp|::ref2::|Index].</span></span>  

<span data-ttu-id="f27ab-243">You request access by declaring capabilities in the package manifest for your app.</span><span class="sxs-lookup"><span data-stu-id="f27ab-243">You request access by declaring capabilities in the package manifest for your app.</span></span>  <span data-ttu-id="f27ab-244">In Visual Studio, you are able to do this from the **Capabilities** panel of the package.appxmanifest designer.</span><span class="sxs-lookup"><span data-stu-id="f27ab-244">In Visual Studio, you are able to do this from the **Capabilities** panel of the package.appxmanifest designer.</span></span>  

![Capabilities panel of the Visual Studio appxmanifest designer](media/vs-appxmanifest-editor-capabilities.png)  

<span data-ttu-id="f27ab-246">In this tutorial, only the default Internet \(Client\) capability is required, so no further action is needed.</span><span class="sxs-lookup"><span data-stu-id="f27ab-246">In this tutorial, only the default Internet \(Client\) capability is required, so no further action is needed.</span></span>  

### <span data-ttu-id="f27ab-247">Use feature detection to invoke WinRT</span><span class="sxs-lookup"><span data-stu-id="f27ab-247">Use feature detection to invoke WinRT</span></span>  

<span data-ttu-id="f27ab-248">To ensure a quality baseline experience for your PWA audience across all platforms, you progressively enhance your PWA experience on Windows using WinRT feature detection.</span><span class="sxs-lookup"><span data-stu-id="f27ab-248">To ensure a quality baseline experience for your PWA audience across all platforms, you progressively enhance your PWA experience on Windows using WinRT feature detection.</span></span>  <span data-ttu-id="f27ab-249">This way, you are able to be sure your Windows-specific code is only run in a context where WinRT APIs are available and applicable.</span><span class="sxs-lookup"><span data-stu-id="f27ab-249">This way, you are able to be sure your Windows-specific code is only run in a context where WinRT APIs are available and applicable.</span></span>  

<span data-ttu-id="f27ab-250">Feature detection may be as simple as looking for the `Windows` object \(the entrypoint to the [WinRT namespace][UwpApiIndex]\) as below:</span><span class="sxs-lookup"><span data-stu-id="f27ab-250">Feature detection may be as simple as looking for the `Windows` object \(the entrypoint to the [WinRT namespace][UwpApiIndex]\) as below:</span></span>  

```javascript
if(window.Windows){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="f27ab-251">However, given that not all Windows APIs are available on all [Windows 10 device types][UwpExtensionSdkDeviceFamiliesOverview], it is generally useful to use more specific feature detection to further qualify the namespace of the API request you are sending:</span><span class="sxs-lookup"><span data-stu-id="f27ab-251">However, given that not all Windows APIs are available on all [Windows 10 device types][UwpExtensionSdkDeviceFamiliesOverview], it is generally useful to use more specific feature detection to further qualify the namespace of the API request you are sending:</span></span>  

```javascript
if(window.Windows && Windows.Media.SpeechRecognition){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="f27ab-252">With that background, you are ready to add some WinRT code to implement a custom context menu.</span><span class="sxs-lookup"><span data-stu-id="f27ab-252">With that background, you are ready to add some WinRT code to implement a custom context menu.</span></span>  <span data-ttu-id="f27ab-253">If you are using the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted]:</span><span class="sxs-lookup"><span data-stu-id="f27ab-253">If you are using the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted]:</span></span>

1.  <span data-ttu-id="f27ab-254">Open Visual Studio to your PWA site project.</span><span class="sxs-lookup"><span data-stu-id="f27ab-254">Open Visual Studio to your PWA site project.</span></span>

1.  <span data-ttu-id="f27ab-255">In Solution Explorer, open the `views\layout.pug` file and add the following line, right below the `script` reference for your service worker:</span><span class="sxs-lookup"><span data-stu-id="f27ab-255">In Solution Explorer, open the `views\layout.pug` file and add the following line, right below the `script` reference for your service worker:</span></span>
    
    ```xml
    script(src='/javascripts/site.js')
    ```  

1.  <span data-ttu-id="f27ab-256">In Solution Explorer, right-click on the `javascripts` folder and **Add** > **New File...**.</span><span class="sxs-lookup"><span data-stu-id="f27ab-256">In Solution Explorer, right-click on the `javascripts` folder and **Add** > **New File...**.</span></span>

1.  <span data-ttu-id="f27ab-257">Name your file: `site.js`, and copy in the following code:</span><span class="sxs-lookup"><span data-stu-id="f27ab-257">Name your file: `site.js`, and copy in the following code:</span></span>
    
    ```javascript
    if (window.Windows && Windows.UI.Popups) {
        document.addEventListener('contextmenu', function (e) {

            // Build the context menu
            var menu = new Windows.UI.Popups.PopupMenu();
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 1", null, 1));
            menu.commands.append(new Windows.UI.Popups.UICommandSeparator);
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 2", null, 2));

            // Convert from webpage to WinRT coordinates
            function pageToWinRT(pageX, pageY) {
                var zoomFactor = document.documentElement.msContentZoomFactor;
                return {
                    x: (pageX - window.pageXOffset) * zoomFactor,
                    y: (pageY - window.pageYOffset) * zoomFactor
                };
            }

            // When the menu is invoked, execute the requested command
            menu.showAsync(pageToWinRT(e.pageX, e.pageY)).done(function (invokedCommand) {
                if (invokedCommand !== null) {
                    switch (invokedCommand.id) {
                        case 1:
                            console.log('Option 1 selected');
                            // Invoke code for option 1
                            break;
                        case 2:
                            console.log('Option 2 selected');
                            // Invoke code for option 2
                            break;
                        default:
                            break;
                    }
                } else {
                    // The command is null if no command was invoked.
                    console.log("Context menu dismissed");
                }
            });
        }, false);
    }
    ```

1.  <span data-ttu-id="f27ab-258">Compare the context menu behavior when you run your PWA in the browser \(`F5` from your PWA site project\) versus from inside the Windows app window \(`F5` from your Universal Windows app project\).</span><span class="sxs-lookup"><span data-stu-id="f27ab-258">Compare the context menu behavior when you run your PWA in the browser \(`F5` from your PWA site project\) versus from inside the Windows app window \(`F5` from your Universal Windows app project\).</span></span>  <span data-ttu-id="f27ab-259">In the browser, right-clicking gives you the Microsoft Edge default context menu, whereas in the `WWAHost.exe` process, your custom menu now appears.</span><span class="sxs-lookup"><span data-stu-id="f27ab-259">In the browser, right-clicking gives you the Microsoft Edge default context menu, whereas in the `WWAHost.exe` process, your custom menu now appears.</span></span>  

    | <span data-ttu-id="f27ab-260">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f27ab-260">Microsoft Edge</span></span> | <span data-ttu-id="f27ab-261">Windows 10 app</span><span class="sxs-lookup"><span data-stu-id="f27ab-261">Windows 10 app</span></span> |  
    |:--- |:---- |  
    | ![Browser default context menu](media/browser-context-menu.png) | ![App custom context menu](media/app-context-menu.png) |  

<span data-ttu-id="f27ab-264">Hopefully you now have a solid foundation for progressively enhancing your PWAs on Windows.</span><span class="sxs-lookup"><span data-stu-id="f27ab-264">Hopefully you now have a solid foundation for progressively enhancing your PWAs on Windows.</span></span>  <span data-ttu-id="f27ab-265">If you run into questions or anything is unclear, please send a comment!</span><span class="sxs-lookup"><span data-stu-id="f27ab-265">If you run into questions or anything is unclear, please send a comment!</span></span>  

## <span data-ttu-id="f27ab-266">Going further</span><span class="sxs-lookup"><span data-stu-id="f27ab-266">Going further</span></span>

<span data-ttu-id="f27ab-267">The [Windows Dev Center][MicrosoftDeveloperWindowsApps] is your complete reference for all stages of Windows app building, from [getting started][MicrosoftDeveloperWindowsAppsGetStarted], to [designing][MicrosoftDeveloperWindowsAppsDesign], [developing][MicrosoftDeveloperWindowsAppsDevelop], and [publishing][MicrosoftDeveloperStorePublishApps] to the Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="f27ab-267">The [Windows Dev Center][MicrosoftDeveloperWindowsApps] is your complete reference for all stages of Windows app building, from [getting started][MicrosoftDeveloperWindowsAppsGetStarted], to [designing][MicrosoftDeveloperWindowsAppsDesign], [developing][MicrosoftDeveloperWindowsAppsDevelop], and [publishing][MicrosoftDeveloperStorePublishApps] to the Microsoft Store.</span></span>  

<span data-ttu-id="f27ab-268">For a general overview on the Universal Windows Platform \(UWP\) and how to target different Windows 10 device families, see [Intro to the Universal Windows Platform][WindowsUWPGetStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="f27ab-268">For a general overview on the Universal Windows Platform \(UWP\) and how to target different Windows 10 device families, see [Intro to the Universal Windows Platform][WindowsUWPGetStartedGuide].</span></span>  

<span data-ttu-id="f27ab-269">And when you are ready, here is how \(and why!\) to [Submit your PWA to the Microsoft Store](./microsoft-store.md).</span><span class="sxs-lookup"><span data-stu-id="f27ab-269">And when you are ready, here is how \(and why!\) to [Submit your PWA to the Microsoft Store](./microsoft-store.md).</span></span>  

<!-- image links -->  

<!-- links -->  

[PwaGetStarted]: ./get-started.md "Get started with Progressive Web Apps"  
[PwaIndexWindows10]: ./index.md#pwas-on-windows-10-edgehtml "PWAs on Windows 10 (EdgeHTML) - Progressive Web Apps on Windows"  
[DevToolsGuide]: ../devtools-guide.md "Microsoft Edge (EdgeHTML) Developer Tools"  
[DevToolsGuideMicrosoftStoreApp]: ../devtools-guide.md#microsoft-store-app "Microsoft Store app - Microsoft Edge (EdgeHTML) Developer Tools"  
[DevToolsGuideServiceWorkers]: ../devtools-guide/service-workers.md "Service Workers"  
[DevToolsProtocol01ClientsEdgePreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge DevTools Preview - DevTools Protocol Clients"  
[DevGuideWhatsNew]: ../dev-guide/whats-new.md "What's New in EdgeHTML"  
[WindowsRuntime]: ../windows-runtime/index.md "Windows Runtime (WinRT) for JavaScript"  
[WindowRuntimeUsingJavascript]: ../windows-runtime/using-the-windows-runtime-in-javascript.md "Using the Windows Runtime in JavaScript"  

[ScriptingJsinrtHandlingWinRTEvents]: /scripting/jswinrt/handling-windows-runtime-events-in-javascript "Handling Windows Runtime Events in JavaScript"  
[ScriptingJsinrtUsingWinRT]: /scripting/jswinrt/using-windows-runtime-asynchronous-methods "Using Windows Runtime Asynchronous Methods"  
[ScriptingJsinrtUsingWinRTCasingConventions]:  /scripting/jswinrt/using-the-windows-runtime-in-javascript#casing-conventions-with-windows-runtime-features "Casing Conventions with Windows Runtime Features - Using the Windows Runtime in JavaScript"  
[UwpApiIndex]: /uwp/api/index "Windows UWP Namespaces"  
[UwpApiWindowsUiPopups]: /uwp/api/windows.ui.popups "Windows.UI.Popups Namespace"  
[UwpApiWindowsUiWebuiWebapplicationActivated]: /uwp/api/windows.ui.webui.webuiapplication.activated "WebUIApplication.Activated Event"  
[UwpExtensionSdkDeviceFamiliesOverview]: /uwp/extension-sdks/device-families-overview "Device families overview"  
[UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest]: /uwp/schemas/appxpackage/uapmanifestschema/generate-package-manifest "How Visual Studio generates an app package manifest"  
[WindowsUWPIndex]: /windows/uwp/index "Universal Windows Platform documentation"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide "What's a Universal Windows Platform (UWP) app?"  
[WindowsUWPGetStartedEnable]: /windows/uwp/get-started/enable-your-device-for-development "Enable your device for development"  
[WindowsUwpSecurityIndex]: /windows/uwp/security/index "Security"  
[WindowsUwpPublishAccountTypesLocationsFees]: /windows/uwp/publish/account-types-locations-and-fees "Account types, locations, and fees"  
[WindowsUwpPackagingAppCapabilitiesSpecialRestricted]: /windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities "Restricted capabilities"  
[WindowsUwpPackagingAppCapabilitiesDevice]: /windows/uwp/packaging/app-capability-declarations#device-capabilities "Device capabilities"  
[WindowsUwpPackagingAppCapabilitiesGeneralUse]: /windows/uwp/packaging/app-capability-declarations#general-use-capabilities "General-use capabilities"  
[WindowsUwpPackagingAppCapabilities]: /windows/uwp/packaging/app-capability-declarations "App capability declarations"  

[BingResultsWindows10Settings]: https://binged.it/2lOGSH0 "windows 10 settings - Bing"  
[GithubWinjsWinjs]: https://github.com/winjs/winjs "winjs/winjs | GitHub"  
[MicrosoftDeveloperStorePublishApps]: https://developer.microsoft.com/store/publish-apps/index "Publish Windows apps and games"  
[MicrosoftDeveloperWindowsApps]: https://developer.microsoft.com/windows/apps/index "Universal Windows Platform documentation"  
[MicrosoftDeveloperWindowsAppsDesign]: https://developer.microsoft.com/windows/apps/design/index "Design and code Windows apps"  
[MicrosoftDeveloperWindowsAppsDevelop]: https://developer.microsoft.com/windows/apps/develop/index "Develop UWP apps"  
[MicrosoftDeveloperWindowsAppsGetStarted]: https://developer.microsoft.com/windows/apps/getstarted/index "Get started with Windows 10 apps"  
[MicrosoftDeveloperWindowsSamples]: https://developer.microsoft.com/windows/samples "Code samples"  
[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge DevTools Preview"  
[MicrosoftSupportWindowsAppPermissions]: https://support.microsoft.com/help/10557/windows-10-app-permissions "App permissions"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Downloads"  
[MicrosoftVisualStudioPreview]: https://visualstudio.microsoft.com/vs/preview "Visual Studio Preview"  
[PreviousVSDownloads]: https://visualstudio.microsoft.com/vs/older-downloads/ "Visual Studio downloads"