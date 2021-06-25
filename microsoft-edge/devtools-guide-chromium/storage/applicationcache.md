---
description: Anzeigen von Anwendungscachedaten aus dem Anwendungsbereich von Microsoft Edge DevTools.
title: Anzeigen von Anwendungscachedaten mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 71e71555940d74f2071178be2e6daf0ec2f49dfd
ms.sourcegitcommit: d0a6959c5338cf1927093b4a9ed29a0bc0390b43
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "11615421"
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
# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a><span data-ttu-id="a7e47-104">Anzeigen von Anwendungscachedaten mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a7e47-104">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="a7e47-105">Der Anwendungscache ist veraltet, und Sie sollten die Verwendung vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a7e47-105">The Application Cache is deprecated, and you should avoid using it.</span></span>  <span data-ttu-id="a7e47-106">Die Anwendungscache-API wird von der Webplattform entfernt.</span><span class="sxs-lookup"><span data-stu-id="a7e47-106">The Application Cache API is being removed from the web platform.</span></span>  <span data-ttu-id="a7e47-107">Navigieren Sie für weitere Informationen zu ["Vorbereiten der AppCache-Entfernung".][WebDevAppcacheRemoval]</span><span class="sxs-lookup"><span data-stu-id="a7e47-107">For more information, navigate to [Preparing for AppCache removal][WebDevAppcacheRemoval].</span></span>

<span data-ttu-id="a7e47-108">In diesem Leitfaden erfahren Sie, wie Sie [Microsoft Edge DevTools][MicrosoftEdgeDevTools] verwenden, um [Anwendungscacheressourcen][MDNWebAPIsWindowApplicationCache] zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a7e47-108">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <a name="view-application-cache-data"></a><span data-ttu-id="a7e47-109">Anzeigen von Anwendungscachedaten</span><span class="sxs-lookup"><span data-stu-id="a7e47-109">View Application Cache data</span></span>  

1.  <span data-ttu-id="a7e47-110">Wählen Sie oben in DevTools das **Anwendungstool** aus.</span><span class="sxs-lookup"><span data-stu-id="a7e47-110">At the top of DevTools, choose the **Application** tool.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="a7e47-112">Der **Manifestbereich**</span><span class="sxs-lookup"><span data-stu-id="a7e47-112">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="a7e47-113">Erweitern Sie den Abschnitt **"Anwendungscache",** und wählen Sie einen Cache aus, um die Ressourcen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a7e47-113">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Bereich "Anwendungscache"" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="a7e47-115">Bereich **"Anwendungscache"**</span><span class="sxs-lookup"><span data-stu-id="a7e47-115">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="a7e47-116">Jede Zeile der Tabelle stellt eine zwischengespeicherte Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="a7e47-116">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="a7e47-117">Die \*\*Spalte Type \*\* stellt die [Kategorie der Ressource][MDNHTMLResourcesInAnApplicationCache]dar.</span><span class="sxs-lookup"><span data-stu-id="a7e47-117">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="a7e47-118">Kategorie</span><span class="sxs-lookup"><span data-stu-id="a7e47-118">Category</span></span> | <span data-ttu-id="a7e47-119">Details</span><span class="sxs-lookup"><span data-stu-id="a7e47-119">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="a7e47-120">Diese Ressource wurde explizit im Manifest aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7e47-120">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="a7e47-121">Die URL ist ein Fallback für eine andere Ressource.</span><span class="sxs-lookup"><span data-stu-id="a7e47-121">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="a7e47-122">Die URL der anderen Ressource ist in DevTools nicht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7e47-122">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="a7e47-123">Das `manifest` Attribut für die Ressource gibt an, dass der Cache das übergeordnete Element der Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="a7e47-123">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="a7e47-124">Das Manifest gibt an, dass die Ressource aus dem Netzwerk stammen muss.</span><span class="sxs-lookup"><span data-stu-id="a7e47-124">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="a7e47-125">Am unteren Rand der Tabelle befinden sich Statussymbole, die Ihre Netzwerkverbindung und den Status des **Anwendungscaches**angeben.</span><span class="sxs-lookup"><span data-stu-id="a7e47-125">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="a7e47-126">Der **Anwendungscache** kann die folgenden Zustände aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a7e47-126">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="a7e47-127">Status</span><span class="sxs-lookup"><span data-stu-id="a7e47-127">State</span></span> | <span data-ttu-id="a7e47-128">Details</span><span class="sxs-lookup"><span data-stu-id="a7e47-128">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="a7e47-129">Das Manifest wird abgerufen und auf Updates überprüft.</span><span class="sxs-lookup"><span data-stu-id="a7e47-129">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="a7e47-130">Ressourcen werden dem Cache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a7e47-130">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="a7e47-131">Der Cache hat keine neuen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="a7e47-131">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="a7e47-132">Der Cache wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a7e47-132">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="a7e47-133">Eine neue Version des Caches ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7e47-133">A new version of the cache is available.</span></span> |  

<!-- links -->  
[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
<!-- external links: -->
[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressourcen in einem Anwendungscache | Mdn"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache – Web-APIs | Mdn"  

[WebDevAppcacheRemoval]: https://web.dev/appcache-removal "Vorbereiten der AppCache-Entfernung | web.dev"  

> [!NOTE]
> <span data-ttu-id="a7e47-138">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7e47-138">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a7e47-139">Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) zu finden und wurde von [Baskisch (Technical][KayceBasques] Writer, Chrome DevTools \& Ausrufebereich\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="a7e47-139">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a7e47-141">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a7e47-141">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
