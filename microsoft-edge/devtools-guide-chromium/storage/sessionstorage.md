---
description: How to view and edit sessionStorage with the Session Storage pane and the Console.
title: View And Edit Session Storage With Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: 24fca3fd3a068f3b2ffbe4ec1c23e6b80b968953
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993548"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="246f3-104">View and edit Session Storage with Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="246f3-104">View and edit Session Storage with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="246f3-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span><span class="sxs-lookup"><span data-stu-id="246f3-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="246f3-106">View sessionStorage keys and values</span><span class="sxs-lookup"><span data-stu-id="246f3-106">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="246f3-107">Select the **Application** tab to open the **Application** panel.</span><span class="sxs-lookup"><span data-stu-id="246f3-107">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="246f3-108">The **Manifest** pane is shown by default.</span><span class="sxs-lookup"><span data-stu-id="246f3-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="246f3-110">The **Manifest** pane</span><span class="sxs-lookup"><span data-stu-id="246f3-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="246f3-111">Expand the **Session Storage** menu.</span><span class="sxs-lookup"><span data-stu-id="246f3-111">Expand the **Session Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       <span data-ttu-id="246f3-113">The **Session Storage** Menu</span><span class="sxs-lookup"><span data-stu-id="246f3-113">The **Session Storage** Menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="246f3-114">Select a domain to view the key-value pairs.</span><span class="sxs-lookup"><span data-stu-id="246f3-114">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       <span data-ttu-id="246f3-116">The `sessionStorage` key-value pairs</span><span class="sxs-lookup"><span data-stu-id="246f3-116">The `sessionStorage` key-value pairs</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="246f3-117">Select a row of the table to view the value in the viewer below the table.</span><span class="sxs-lookup"><span data-stu-id="246f3-117">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       <span data-ttu-id="246f3-119">View the value of the `x-sid` key</span><span class="sxs-lookup"><span data-stu-id="246f3-119">View the value of the `x-sid` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="246f3-120">Create a new sessionStorage key-value pair</span><span class="sxs-lookup"><span data-stu-id="246f3-120">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="246f3-121">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="246f3-121">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="246f3-122">Double-click the empty part of the table.</span><span class="sxs-lookup"><span data-stu-id="246f3-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="246f3-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span><span class="sxs-lookup"><span data-stu-id="246f3-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       <span data-ttu-id="246f3-125">The empty part of the table to double-click in order to create a new key-value pair</span><span class="sxs-lookup"><span data-stu-id="246f3-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="246f3-126">Edit sessionStorage keys or values</span><span class="sxs-lookup"><span data-stu-id="246f3-126">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="246f3-127">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="246f3-127">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="246f3-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span><span class="sxs-lookup"><span data-stu-id="246f3-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       <span data-ttu-id="246f3-130">Edit a `sessionStorage` key</span><span class="sxs-lookup"><span data-stu-id="246f3-130">Edit a `sessionStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="246f3-131">Delete sessionStorage key-value pairs</span><span class="sxs-lookup"><span data-stu-id="246f3-131">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="246f3-132">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="246f3-132">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="246f3-133">Select the key-value pair that you want to delete.</span><span class="sxs-lookup"><span data-stu-id="246f3-133">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="246f3-134">DevTools highlights it blue to indicate that it is selected.</span><span class="sxs-lookup"><span data-stu-id="246f3-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="246f3-135">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span><span class="sxs-lookup"><span data-stu-id="246f3-135">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="246f3-136">Delete all sessionStorage key-value pairs for a domain</span><span class="sxs-lookup"><span data-stu-id="246f3-136">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="246f3-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="246f3-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="246f3-138">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span><span class="sxs-lookup"><span data-stu-id="246f3-138">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="246f3-139">Interact with sessionStorage from the Console</span><span class="sxs-lookup"><span data-stu-id="246f3-139">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="246f3-140">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span><span class="sxs-lookup"><span data-stu-id="246f3-140">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="246f3-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span><span class="sxs-lookup"><span data-stu-id="246f3-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-console-domain-selection.msft.png":::
       <span data-ttu-id="246f3-143">Change the JavaScript context of the Console</span><span class="sxs-lookup"><span data-stu-id="246f3-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="246f3-144">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span><span class="sxs-lookup"><span data-stu-id="246f3-144">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       <span data-ttu-id="246f3-146">Interact with `sessionStorage` from the **Console**</span><span class="sxs-lookup"><span data-stu-id="246f3-146">Interact with `sessionStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
   

  
-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chromium) Developer tools | Microsoft Docs"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window.sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="246f3-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="246f3-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="246f3-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="246f3-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="246f3-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="246f3-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
