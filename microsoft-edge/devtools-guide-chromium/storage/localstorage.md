---
description: How to view and edit localStorage with the Local Storage pane and the Console.
title: View And Edit Local Storage With Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: aa5365d1764ea0db537ea24464f9c76441f05322
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993555"
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





# <span data-ttu-id="b4294-104">View and edit local storage with Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b4294-104">View and edit local storage with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="b4294-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span><span class="sxs-lookup"><span data-stu-id="b4294-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="b4294-106">View localStorage keys and values</span><span class="sxs-lookup"><span data-stu-id="b4294-106">View localStorage keys and values</span></span>   

1.  <span data-ttu-id="b4294-107">Select the **Application** tab to open the **Application** panel.</span><span class="sxs-lookup"><span data-stu-id="b4294-107">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="b4294-108">The **Manifest** pane is shown by default.</span><span class="sxs-lookup"><span data-stu-id="b4294-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="b4294-110">The **Manifest** pane</span><span class="sxs-lookup"><span data-stu-id="b4294-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b4294-111">Expand the **Local Storage** menu.</span><span class="sxs-lookup"><span data-stu-id="b4294-111">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="b4294-113">The **Local Storage** menu</span><span class="sxs-lookup"><span data-stu-id="b4294-113">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b4294-114">Select a domain to view the key-value pairs.</span><span class="sxs-lookup"><span data-stu-id="b4294-114">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="b4294-116">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span><span class="sxs-lookup"><span data-stu-id="b4294-116">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b4294-117">Select a row of the table to view the value in the viewer below the table.</span><span class="sxs-lookup"><span data-stu-id="b4294-117">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="b4294-119">View the value of the `eventLogQueue_Online` key</span><span class="sxs-lookup"><span data-stu-id="b4294-119">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b4294-120">Create a new localStorage key-value pair</span><span class="sxs-lookup"><span data-stu-id="b4294-120">Create a new localStorage key-value pair</span></span>   

1.  <span data-ttu-id="b4294-121">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="b4294-121">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="b4294-122">Double-click the empty part of the table.</span><span class="sxs-lookup"><span data-stu-id="b4294-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="b4294-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span><span class="sxs-lookup"><span data-stu-id="b4294-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="b4294-125">The empty part of the table to double-click in order to create a new key-value pair</span><span class="sxs-lookup"><span data-stu-id="b4294-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b4294-126">Edit localStorage keys or values</span><span class="sxs-lookup"><span data-stu-id="b4294-126">Edit localStorage keys or values</span></span>   

1.  <span data-ttu-id="b4294-127">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="b4294-127">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="b4294-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span><span class="sxs-lookup"><span data-stu-id="b4294-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="b4294-130">Edit a `localStorage` key</span><span class="sxs-lookup"><span data-stu-id="b4294-130">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b4294-131">Delete localStorage key-value pairs</span><span class="sxs-lookup"><span data-stu-id="b4294-131">Delete localStorage key-value pairs</span></span>   

1.  <span data-ttu-id="b4294-132">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="b4294-132">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="b4294-133">Select the key-value pair that you want to delete.</span><span class="sxs-lookup"><span data-stu-id="b4294-133">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="b4294-134">DevTools highlights it blue to indicate that it is selected.</span><span class="sxs-lookup"><span data-stu-id="b4294-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="b4294-135">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span><span class="sxs-lookup"><span data-stu-id="b4294-135">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="b4294-136">Delete all `localStorage` key-value pairs for a domain</span><span class="sxs-lookup"><span data-stu-id="b4294-136">Delete all `localStorage` key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="b4294-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="b4294-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="b4294-138">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span><span class="sxs-lookup"><span data-stu-id="b4294-138">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="b4294-139">Interact with localStorage from the Console</span><span class="sxs-lookup"><span data-stu-id="b4294-139">Interact with localStorage from the Console</span></span>   

<span data-ttu-id="b4294-140">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span><span class="sxs-lookup"><span data-stu-id="b4294-140">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="b4294-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span><span class="sxs-lookup"><span data-stu-id="b4294-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="b4294-143">Change the JavaScript context of the Console</span><span class="sxs-lookup"><span data-stu-id="b4294-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b4294-144">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b4294-144">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="b4294-146">Interact with `localStorage` from the **Console**</span><span class="sxs-lookup"><span data-stu-id="b4294-146">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chromium) Developer tools | Microsoft Docs"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="b4294-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b4294-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b4294-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="b4294-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="b4294-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b4294-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
