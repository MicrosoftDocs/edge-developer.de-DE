---
description: Get to know the Microsoft Edge Developer Tools
title: Microsoft Edge Developer Tools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: microsoft edge, web development, f12 tools, devtools
experimental: false
experiment_id: 51fe4b97-3e55-41
ms.openlocfilehash: 3aee2ab67c6e703a0a31b58b5bf985a23fcbb481
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986220"
---
# <span data-ttu-id="3cc56-104">Microsoft Edge Developer Tools</span><span class="sxs-lookup"><span data-stu-id="3cc56-104">Microsoft Edge Developer Tools</span></span>  

> [!NOTE]
> <span data-ttu-id="3cc56-105">The Microsoft Edge DevTools help web developers build and test websites.</span><span class="sxs-lookup"><span data-stu-id="3cc56-105">The Microsoft Edge DevTools help web developers build and test websites.</span></span>  <span data-ttu-id="3cc56-106">If you accidentally opened the DevTools, just press `F12` to close.</span><span class="sxs-lookup"><span data-stu-id="3cc56-106">If you accidentally opened the DevTools, just press `F12` to close.</span></span>  

<span data-ttu-id="3cc56-107">The Microsoft Edge DevTools are built with [TypeScript](https://www.typescriptlang.org/), powered by [open source](https://github.com/Microsoft/ChakraCore), optimized for modern front-end workflows, and now available as a [standalone Windows 10 app](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) in the Microsoft Store!</span><span class="sxs-lookup"><span data-stu-id="3cc56-107">The Microsoft Edge DevTools are built with [TypeScript](https://www.typescriptlang.org/), powered by [open source](https://github.com/Microsoft/ChakraCore), optimized for modern front-end workflows, and now available as a [standalone Windows 10 app](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) in the Microsoft Store!</span></span>

<span data-ttu-id="3cc56-108">For more on the latest features, check out [*DevTools in the latest update of Windows 10 (EdgeHTML 17)*](./devtools-guide/whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="3cc56-108">For more on the latest features, check out [*DevTools in the latest update of Windows 10 (EdgeHTML 17)*](./devtools-guide/whats-new.md).</span></span>

## <span data-ttu-id="3cc56-109">Core tools</span><span class="sxs-lookup"><span data-stu-id="3cc56-109">Core tools</span></span>

![Microsoft Edge DevTools](./devtools-guide/media/devtools.png)

<span data-ttu-id="3cc56-111">The Microsoft Edge DevTools include:</span><span class="sxs-lookup"><span data-stu-id="3cc56-111">The Microsoft Edge DevTools include:</span></span>

 - <span data-ttu-id="3cc56-112">An [**Elements**](./devtools-guide/elements.md) panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span><span class="sxs-lookup"><span data-stu-id="3cc56-112">An [**Elements**](./devtools-guide/elements.md) panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>
 - <span data-ttu-id="3cc56-113">A [**Console**](./devtools-guide/console.md) to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span><span class="sxs-lookup"><span data-stu-id="3cc56-113">A [**Console**](./devtools-guide/console.md) to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>
 - <span data-ttu-id="3cc56-114">A [**Debugger**](./devtools-guide/debugger.md) to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span><span class="sxs-lookup"><span data-stu-id="3cc56-114">A [**Debugger**](./devtools-guide/debugger.md) to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>
 - <span data-ttu-id="3cc56-115">A [**Network**](./devtools-guide/network.md) panel to monitor and inspect requests and responses from the network and browser cache</span><span class="sxs-lookup"><span data-stu-id="3cc56-115">A [**Network**](./devtools-guide/network.md) panel to monitor and inspect requests and responses from the network and browser cache</span></span> 
 - <span data-ttu-id="3cc56-116">A [**Performance**](./devtools-guide/performance.md) panel to profile the time and system resources required by your site</span><span class="sxs-lookup"><span data-stu-id="3cc56-116">A [**Performance**](./devtools-guide/performance.md) panel to profile the time and system resources required by your site</span></span>
 - <span data-ttu-id="3cc56-117">A [**Memory**](./devtools-guide/memory.md) panel to measure your use of memory resources and compare heap snapshots at different states of code execution</span><span class="sxs-lookup"><span data-stu-id="3cc56-117">A [**Memory**](./devtools-guide/memory.md) panel to measure your use of memory resources and compare heap snapshots at different states of code execution</span></span>
 - <span data-ttu-id="3cc56-118">An [**Emulation**](./devtools-guide/emulation.md) panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span><span class="sxs-lookup"><span data-stu-id="3cc56-118">An [**Emulation**](./devtools-guide/emulation.md) panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>

<span data-ttu-id="3cc56-119">Please keep sending your [feedback and feature requests](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="3cc56-119">Please keep sending your [feedback and feature requests](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>

> [!TIP]
> <span data-ttu-id="3cc56-120">**[Test on Microsoft Edge free from any browser](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: We partnered with [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) to provide free live and automated testing on Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3cc56-120">**[Test on Microsoft Edge free from any browser](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: We partnered with [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) to provide free live and automated testing on Microsoft Edge.</span></span>

## <span data-ttu-id="3cc56-121">Microsoft Store app</span><span class="sxs-lookup"><span data-stu-id="3cc56-121">Microsoft Store app</span></span>

<span data-ttu-id="3cc56-122">The **Microsoft Edge DevTools** are [now available for preview](./devtools-guide/whats-new.md) as a standalone [Windows 10 app from the Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab), in addition to the in-browser (`F12`) tooling experience.</span><span class="sxs-lookup"><span data-stu-id="3cc56-122">The **Microsoft Edge DevTools** are [now available for preview](./devtools-guide/whats-new.md) as a standalone [Windows 10 app from the Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab), in addition to the in-browser (`F12`) tooling experience.</span></span> <span data-ttu-id="3cc56-123">Die Store-Version enthält einen Bereich *Auswahl* zum Anfügen an geöffnete lokale und remote Seitenziele und ein Layout im Registerkartenformat für den einfachen Wechsel zwischen DevTools-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="3cc56-123">With the store version comes a *chooser* panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>

### <span data-ttu-id="3cc56-124">Local debugging</span><span class="sxs-lookup"><span data-stu-id="3cc56-124">Local debugging</span></span>

<span data-ttu-id="3cc56-125">To debug a page locally, simply launch the *Microsoft Edge DevTools* app.</span><span class="sxs-lookup"><span data-stu-id="3cc56-125">To debug a page locally, simply launch the *Microsoft Edge DevTools* app.</span></span> <span data-ttu-id="3cc56-126">The **Local** panel of the chooser will display all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs](./progressive-web-apps-edgehtml/index.md) (*WWAHost.exe* processes), and [webview](./webview.md) controls.</span><span class="sxs-lookup"><span data-stu-id="3cc56-126">The **Local** panel of the chooser will display all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs](./progressive-web-apps-edgehtml/index.md) (*WWAHost.exe* processes), and [webview](./webview.md) controls.</span></span> <span data-ttu-id="3cc56-127">Click on your desired target to attach and open a new tab instance of the DevTools.</span><span class="sxs-lookup"><span data-stu-id="3cc56-127">Click on your desired target to attach and open a new tab instance of the DevTools.</span></span>

![DevTools app Local panel](./devtools-guide/media/chooser_local.png)

### <span data-ttu-id="3cc56-129">Remote debugging</span><span class="sxs-lookup"><span data-stu-id="3cc56-129">Remote debugging</span></span>

<span data-ttu-id="3cc56-130">The *Microsoft Edge DevTools* app introduces basic support for debugging pages on a remote machine via our newly released [**DevTools Protocol**](./devtools-protocol/index.md).</span><span class="sxs-lookup"><span data-stu-id="3cc56-130">The *Microsoft Edge DevTools* app introduces basic support for debugging pages on a remote machine via our newly released [**DevTools Protocol**](./devtools-protocol/index.md).</span></span> <span data-ttu-id="3cc56-131">With this release comes remote access to core funtionality in the [**Debugger**](./devtools-guide/debugger.md) panel, minus cache inspection (for Web storage, Service worker, Cache API, and IndexedDB).</span><span class="sxs-lookup"><span data-stu-id="3cc56-131">With this release comes remote access to core funtionality in the [**Debugger**](./devtools-guide/debugger.md) panel, minus cache inspection (for Web storage, Service worker, Cache API, and IndexedDB).</span></span> <span data-ttu-id="3cc56-132">Remote debugging is limited to *Microsoft Edge* running *desktop* hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span><span class="sxs-lookup"><span data-stu-id="3cc56-132">Remote debugging is limited to *Microsoft Edge* running *desktop* hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>

<span data-ttu-id="3cc56-133">To get started, check out the [*Microsoft Edge DevTools*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) section of the [DevTools Protocol](./devtools-protocol/index.md) docs.</span><span class="sxs-lookup"><span data-stu-id="3cc56-133">To get started, check out the [*Microsoft Edge DevTools*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) section of the [DevTools Protocol](./devtools-protocol/index.md) docs.</span></span>

![DevTools-App, Bereich "Remote"](./devtools-guide/media/chooser_remote.png)

## <span data-ttu-id="3cc56-135">General Shortcuts</span><span class="sxs-lookup"><span data-stu-id="3cc56-135">General Shortcuts</span></span>

<span data-ttu-id="3cc56-136">These shortcuts control the main DevTools window and/or work across all tools.</span><span class="sxs-lookup"><span data-stu-id="3cc56-136">These shortcuts control the main DevTools window and/or work across all tools.</span></span>

<span data-ttu-id="3cc56-137">Action</span><span class="sxs-lookup"><span data-stu-id="3cc56-137">Action</span></span> | <span data-ttu-id="3cc56-138">Shortcut</span><span class="sxs-lookup"><span data-stu-id="3cc56-138">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="3cc56-139">Show/Hide DevTools (opens to last viewed panel)</span><span class="sxs-lookup"><span data-stu-id="3cc56-139">Show/Hide DevTools (opens to last viewed panel)</span></span> | <span data-ttu-id="3cc56-140">F12, Ctrl+Shift+I</span><span class="sxs-lookup"><span data-stu-id="3cc56-140">F12, Ctrl+Shift+I</span></span>
<span data-ttu-id="3cc56-141">Toggle docking (Undock/Bottom/Right)</span><span class="sxs-lookup"><span data-stu-id="3cc56-141">Toggle docking (Undock/Bottom/Right)</span></span> | <span data-ttu-id="3cc56-142">Ctrl+Shift+D</span><span class="sxs-lookup"><span data-stu-id="3cc56-142">Ctrl+Shift+D</span></span> 
<span data-ttu-id="3cc56-143">Show non-editable HTML source code in Debugger</span><span class="sxs-lookup"><span data-stu-id="3cc56-143">Show non-editable HTML source code in Debugger</span></span> | <span data-ttu-id="3cc56-144">Ctrl+U</span><span class="sxs-lookup"><span data-stu-id="3cc56-144">Ctrl+U</span></span>
<span data-ttu-id="3cc56-145">Show/hide Console at the bottom of any other tool</span><span class="sxs-lookup"><span data-stu-id="3cc56-145">Show/hide Console at the bottom of any other tool</span></span>  | <span data-ttu-id="3cc56-146">Ctrl+**\`**</span><span class="sxs-lookup"><span data-stu-id="3cc56-146">Ctrl+**\`**</span></span>
<span data-ttu-id="3cc56-147">Switch to Elements (DOM Explorer)</span><span class="sxs-lookup"><span data-stu-id="3cc56-147">Switch to Elements (DOM Explorer)</span></span> | <span data-ttu-id="3cc56-148">Ctrl+1</span><span class="sxs-lookup"><span data-stu-id="3cc56-148">Ctrl+1</span></span>
<span data-ttu-id="3cc56-149">Switch to Console</span><span class="sxs-lookup"><span data-stu-id="3cc56-149">Switch to Console</span></span> |  <span data-ttu-id="3cc56-150">Ctrl+2</span><span class="sxs-lookup"><span data-stu-id="3cc56-150">Ctrl+2</span></span>
<span data-ttu-id="3cc56-151">Switch to Debugger</span><span class="sxs-lookup"><span data-stu-id="3cc56-151">Switch to Debugger</span></span> | <span data-ttu-id="3cc56-152">Ctrl+3</span><span class="sxs-lookup"><span data-stu-id="3cc56-152">Ctrl+3</span></span>
<span data-ttu-id="3cc56-153">Switch to Network</span><span class="sxs-lookup"><span data-stu-id="3cc56-153">Switch to Network</span></span> | <span data-ttu-id="3cc56-154">Ctrl+4</span><span class="sxs-lookup"><span data-stu-id="3cc56-154">Ctrl+4</span></span>
<span data-ttu-id="3cc56-155">Switch to Performance</span><span class="sxs-lookup"><span data-stu-id="3cc56-155">Switch to Performance</span></span> | <span data-ttu-id="3cc56-156">Ctrl+5</span><span class="sxs-lookup"><span data-stu-id="3cc56-156">Ctrl+5</span></span>
<span data-ttu-id="3cc56-157">Switch to Memory</span><span class="sxs-lookup"><span data-stu-id="3cc56-157">Switch to Memory</span></span> | <span data-ttu-id="3cc56-158">Ctrl+6</span><span class="sxs-lookup"><span data-stu-id="3cc56-158">Ctrl+6</span></span>
<span data-ttu-id="3cc56-159">Switch to Emulation</span><span class="sxs-lookup"><span data-stu-id="3cc56-159">Switch to Emulation</span></span> | <span data-ttu-id="3cc56-160">Ctrl+7</span><span class="sxs-lookup"><span data-stu-id="3cc56-160">Ctrl+7</span></span>
<span data-ttu-id="3cc56-161">Help Document</span><span class="sxs-lookup"><span data-stu-id="3cc56-161">Help Document</span></span> | <span data-ttu-id="3cc56-162">F1</span><span class="sxs-lookup"><span data-stu-id="3cc56-162">F1</span></span>
<span data-ttu-id="3cc56-163">Next tool</span><span class="sxs-lookup"><span data-stu-id="3cc56-163">Next tool</span></span> | <span data-ttu-id="3cc56-164">Ctrl+F6</span><span class="sxs-lookup"><span data-stu-id="3cc56-164">Ctrl+F6</span></span>
<span data-ttu-id="3cc56-165">Previous tool</span><span class="sxs-lookup"><span data-stu-id="3cc56-165">Previous tool</span></span> | <span data-ttu-id="3cc56-166">Ctrl+Shift+F6</span><span class="sxs-lookup"><span data-stu-id="3cc56-166">Ctrl+Shift+F6</span></span>
<span data-ttu-id="3cc56-167">Previous tool (from history)</span><span class="sxs-lookup"><span data-stu-id="3cc56-167">Previous tool (from history)</span></span> | <span data-ttu-id="3cc56-168">Ctrl+Shift+[</span><span class="sxs-lookup"><span data-stu-id="3cc56-168">Ctrl+Shift+[</span></span>
<span data-ttu-id="3cc56-169">Next tool (from history)</span><span class="sxs-lookup"><span data-stu-id="3cc56-169">Next tool (from history)</span></span> | <span data-ttu-id="3cc56-170">Ctrl+Shift+]</span><span class="sxs-lookup"><span data-stu-id="3cc56-170">Ctrl+Shift+]</span></span>
<span data-ttu-id="3cc56-171">Next Subframe</span><span class="sxs-lookup"><span data-stu-id="3cc56-171">Next Subframe</span></span>    | <span data-ttu-id="3cc56-172">F6</span><span class="sxs-lookup"><span data-stu-id="3cc56-172">F6</span></span>
<span data-ttu-id="3cc56-173">Previous Subframe</span><span class="sxs-lookup"><span data-stu-id="3cc56-173">Previous Subframe</span></span> | <span data-ttu-id="3cc56-174">Shift+F6</span><span class="sxs-lookup"><span data-stu-id="3cc56-174">Shift+F6</span></span>
<span data-ttu-id="3cc56-175">Next match in Search box</span><span class="sxs-lookup"><span data-stu-id="3cc56-175">Next match in Search box</span></span> | <span data-ttu-id="3cc56-176">F3</span><span class="sxs-lookup"><span data-stu-id="3cc56-176">F3</span></span>
<span data-ttu-id="3cc56-177">Previous match in Search box</span><span class="sxs-lookup"><span data-stu-id="3cc56-177">Previous match in Search box</span></span> | <span data-ttu-id="3cc56-178">Shift+F3</span><span class="sxs-lookup"><span data-stu-id="3cc56-178">Shift+F3</span></span>
<span data-ttu-id="3cc56-179">Find in search box</span><span class="sxs-lookup"><span data-stu-id="3cc56-179">Find in search box</span></span> | <span data-ttu-id="3cc56-180">Ctrl+F</span><span class="sxs-lookup"><span data-stu-id="3cc56-180">Ctrl+F</span></span>
<span data-ttu-id="3cc56-181">Give focus to console at the bottom</span><span class="sxs-lookup"><span data-stu-id="3cc56-181">Give focus to console at the bottom</span></span> | <span data-ttu-id="3cc56-182">Alt+Shift+I</span><span class="sxs-lookup"><span data-stu-id="3cc56-182">Alt+Shift+I</span></span>
<span data-ttu-id="3cc56-183">Dock/undock tools (toggle docking)</span><span class="sxs-lookup"><span data-stu-id="3cc56-183">Dock/undock tools (toggle docking)</span></span> | <span data-ttu-id="3cc56-184">Ctrl+P</span><span class="sxs-lookup"><span data-stu-id="3cc56-184">Ctrl+P</span></span>  
<span data-ttu-id="3cc56-185">Launch DevTools to Console</span><span class="sxs-lookup"><span data-stu-id="3cc56-185">Launch DevTools to Console</span></span> | <span data-ttu-id="3cc56-186">Ctrl+Shift+J</span><span class="sxs-lookup"><span data-stu-id="3cc56-186">Ctrl+Shift+J</span></span>
<span data-ttu-id="3cc56-187">Refresh the page.</span><span class="sxs-lookup"><span data-stu-id="3cc56-187">Refresh the page.</span></span> <span data-ttu-id="3cc56-188">**Note:** if you're debugging and paused at a breakpoint, this resumes execution first.</span><span class="sxs-lookup"><span data-stu-id="3cc56-188">**Note:** if you're debugging and paused at a breakpoint, this resumes execution first.</span></span> | <span data-ttu-id="3cc56-189">Ctrl+Shift+F5 or Ctrl+R</span><span class="sxs-lookup"><span data-stu-id="3cc56-189">Ctrl+Shift+F5 or Ctrl+R</span></span>

## <span data-ttu-id="3cc56-190">Getting in touch with the Microsoft Edge DevTools team</span><span class="sxs-lookup"><span data-stu-id="3cc56-190">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](./devtools-guide-chromium/includes/contact-devtools-team-note.md)]  
