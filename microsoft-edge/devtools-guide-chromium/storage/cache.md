---
description: How to view Cache data from the Application panel of Microsoft Edge DevTools.
title: View Cache Data With Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: c920a171ec89925cc79ab741eed01e11d749bf1b
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993296"
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





# <span data-ttu-id="c5b4e-104">View cache data with Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c5b4e-104">View cache data with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="c5b4e-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="c5b4e-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="c5b4e-107">Look for the information in the **Size** column of the **Network Log**.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-107">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="c5b4e-108">See [Log network activity][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="c5b4e-108">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="c5b4e-109">View cache data</span><span class="sxs-lookup"><span data-stu-id="c5b4e-109">View cache data</span></span>   

1.  <span data-ttu-id="c5b4e-110">Select the **Application** tab to open the **Application** panel.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-110">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="c5b4e-111">The **Manifest** pane usually opens by default.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="c5b4e-113">The **Manifest** pane</span><span class="sxs-lookup"><span data-stu-id="c5b4e-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c5b4e-114">Expand the **Cache Storage** section to view available caches.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="c5b4e-116">Available caches</span><span class="sxs-lookup"><span data-stu-id="c5b4e-116">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c5b4e-117">Select a cache to view the contents.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-117">Select a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="c5b4e-119">View the contents of a cache</span><span class="sxs-lookup"><span data-stu-id="c5b4e-119">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c5b4e-120">Select a resource to view the HTTP headers in the section below the table.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-120">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="c5b4e-122">View the HTTP headers of a resource</span><span class="sxs-lookup"><span data-stu-id="c5b4e-122">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c5b4e-123">Select **Preview** to view the content of a resource.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-123">Select **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="c5b4e-125">View the content of a resource</span><span class="sxs-lookup"><span data-stu-id="c5b4e-125">View the content of a resource</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c5b4e-126">Refresh a resource</span><span class="sxs-lookup"><span data-stu-id="c5b4e-126">Refresh a resource</span></span>   

1.  <span data-ttu-id="c5b4e-127">[View the data for a cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="c5b4e-127">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="c5b4e-128">Select the resource that you want to refresh.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-128">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="c5b4e-129">DevTools highlights it to indicate that it is selected.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-129">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="c5b4e-131">Select a resource</span><span class="sxs-lookup"><span data-stu-id="c5b4e-131">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c5b4e-132">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span><span class="sxs-lookup"><span data-stu-id="c5b4e-132">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="c5b4e-133">Filter resources</span><span class="sxs-lookup"><span data-stu-id="c5b4e-133">Filter resources</span></span>   

1.  <span data-ttu-id="c5b4e-134">[View the data for a cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="c5b4e-134">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="c5b4e-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="c5b4e-137">Filter out resources that do not match the specified path</span><span class="sxs-lookup"><span data-stu-id="c5b4e-137">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c5b4e-138">Delete a resource</span><span class="sxs-lookup"><span data-stu-id="c5b4e-138">Delete a resource</span></span>   

1.  <span data-ttu-id="c5b4e-139">[View the data for a cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="c5b4e-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="c5b4e-140">Select the resource that you want to delete.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-140">Select the resource that you want to delete.</span></span>  <span data-ttu-id="c5b4e-141">DevTools highlights it to indicate that it is selected.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-141">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="c5b4e-143">Select a resource</span><span class="sxs-lookup"><span data-stu-id="c5b4e-143">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c5b4e-144">Select **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span><span class="sxs-lookup"><span data-stu-id="c5b4e-144">Select **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="c5b4e-145">Delete all cache data</span><span class="sxs-lookup"><span data-stu-id="c5b4e-145">Delete all cache data</span></span>   

1.  <span data-ttu-id="c5b4e-146">Open **Application** > **Clear Storage**.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-146">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="c5b4e-147">Make sure that the **Cache Storage** checkbox is enabled.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-147">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="c5b4e-149">The **Cache Storage** checkbox</span><span class="sxs-lookup"><span data-stu-id="c5b4e-149">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c5b4e-150">Select **Clear site data**.</span><span class="sxs-lookup"><span data-stu-id="c5b4e-150">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="c5b4e-152">The **Clear Site Data** button</span><span class="sxs-lookup"><span data-stu-id="c5b4e-152">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
<!--  
  


-->  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chromium) Developer tools | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Log network activity | Microsoft Docs"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "HTTP caching | MDN"  

> [!NOTE]
> <span data-ttu-id="c5b4e-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c5b4e-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c5b4e-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="c5b4e-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="c5b4e-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c5b4e-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
