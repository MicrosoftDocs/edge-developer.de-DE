---
description: Alles über Service Worker-Verbesserungen und die Verwendung der einzelnen.
title: Verbesserungen für Service Worker
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, Devtools, Service Worker, PWA
ms.openlocfilehash: c00b7c7fd18d4bb3d413369ec1464c0cb0255311
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597145"
---
# <a name="service-worker-improvements"></a><span data-ttu-id="d5d4b-104">Verbesserungen für Service Worker</span><span class="sxs-lookup"><span data-stu-id="d5d4b-104">Service Worker improvements</span></span>  

<span data-ttu-id="d5d4b-105">In diesem Artikel erfahren Sie mehr über Verbesserungen an Entwicklertools für die Arbeit mit [Service-Workern][MdnServiceWorkerApi] und die Netzwerkanforderungen, die jeweils durchgehen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-105">This article teaches you about improvements to developer tools for working with [service workers][MdnServiceWorkerApi] and the network requests that pass through each one.</span></span>  <span data-ttu-id="d5d4b-106">Die Verbesserungen für **Service Worker** sind in den Tools **"Netzwerk",** **"Anwendung"** und **"Quellen"** enthalten.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-106">The **service worker improvements** are in the **Network**, **Application**, and **Sources** tools.</span></span>  <span data-ttu-id="d5d4b-107">Die Verbesserungen vereinfachen die folgenden Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-107">The improvements simplify the following tasks.</span></span>  

*   <span data-ttu-id="d5d4b-108">Debuggen basierend auf Service Worker-Zeitachsen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-108">Debug based on Service Worker timelines.</span></span>  
    *   <span data-ttu-id="d5d4b-109">Der Anfang einer Anforderung und die Dauer des Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-109">The start of a request and duration of the bootstrap.</span></span>  
    *   <span data-ttu-id="d5d4b-110">Aktualisieren sie auf die Service Worker-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-110">Update to Service worker registration.</span></span>  
    *   <span data-ttu-id="d5d4b-111">Die Laufzeit einer Anforderung mithilfe des [Fetch-Ereignishandlers.][MdnFetchEvent]</span><span class="sxs-lookup"><span data-stu-id="d5d4b-111">The runtime of a request using the [fetch event][MdnFetchEvent] handler.</span></span>  
    *   <span data-ttu-id="d5d4b-112">Die Laufzeit aller Abrufereignisse zum Laden eines Clients.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-112">The runtime of all fetch events for loading a client.</span></span>  
*   <span data-ttu-id="d5d4b-113">Erkunden Sie die Laufzeitdetails zum Abrufen von Ereignishandlern, Installieren von Ereignishandlern und Aktivieren von Ereignishandlern.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-113">Explore the runtime details of fetch event handlers, install event handlers, and activate event handlers.</span></span>  
*   <span data-ttu-id="d5d4b-114">Treten Sie mit [Seitenskriptinformationen](#sources)in den Ereignishandler ein und aus dem Abruf.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-114">Step into and out of fetch event handler with [page script information](#sources).</span></span>  
    
<span data-ttu-id="d5d4b-115">Die Umgebung umfasst drei verschiedene Entwicklertools.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-115">The experiences span three different developer tools.</span></span>  

1.  <span data-ttu-id="d5d4b-116">Das [Netzwerktool.](#network)</span><span class="sxs-lookup"><span data-stu-id="d5d4b-116">The [Network](#network) tool.</span></span>  <span data-ttu-id="d5d4b-117">Wählen Sie eine Netzwerkanforderung aus, die über einen Service Worker ausgeführt wird, und greifen Sie im **Timing-Tool** auf die entsprechende Zeitachse des Service Worker zu.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-117">Choose a network request that runs through a service worker and access the corresponding timeline of the service worker in the **Timing** tool.</span></span>  
1.  <span data-ttu-id="d5d4b-118">Das [Anwendungstool.](#application)</span><span class="sxs-lookup"><span data-stu-id="d5d4b-118">The [Application](#application) tool.</span></span>  <span data-ttu-id="d5d4b-119">Navigieren Sie zum Debuggen der Service Worker zum **Service Worker-Tool.**</span><span class="sxs-lookup"><span data-stu-id="d5d4b-119">To debug the service workers, navigate to the **Service Workers** tool.</span></span>  
1.  <span data-ttu-id="d5d4b-120">Das [Tool "Quellen".](#sources)</span><span class="sxs-lookup"><span data-stu-id="d5d4b-120">The [Sources](#sources) tool.</span></span>  <span data-ttu-id="d5d4b-121">Greifen Sie auf Seitenskriptinformationen zu, wenn Sie in das Abrufen von Ereignishandlern eintreten.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-121">Access page script information when stepping into fetch event handlers.</span></span>  
    
## <a name="network"></a><span data-ttu-id="d5d4b-122">Network</span><span class="sxs-lookup"><span data-stu-id="d5d4b-122">Network</span></span>  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Zeitachse für Service Worker im Netzwerktool" lightbox="../media/sw-network-timeline.msft.png":::
   <span data-ttu-id="d5d4b-124">Netzwerkansicht</span><span class="sxs-lookup"><span data-stu-id="d5d4b-124">Network view</span></span>  
:::image-end:::  

<span data-ttu-id="d5d4b-125">Führen Sie eine der folgenden Aktionen aus, um auf die Debugfeatures von Service Workern im **Netzwerktool** zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-125">To access the service worker debugging features in the **Network** tool, complete one of the following actions.</span></span>  

*   <span data-ttu-id="d5d4b-126">Zugriff direkt im **Netzwerktool.**</span><span class="sxs-lookup"><span data-stu-id="d5d4b-126">Access directly in the **Network** tool.</span></span>  
*   <span data-ttu-id="d5d4b-127">Gestartet im **Anwendungstool.**</span><span class="sxs-lookup"><span data-stu-id="d5d4b-127">Started in the **Application** tool.</span></span>  
    
### <a name="request-routing"></a><span data-ttu-id="d5d4b-128">Anforderungsrouting</span><span class="sxs-lookup"><span data-stu-id="d5d4b-128">Request routing</span></span>  

<span data-ttu-id="d5d4b-129">Um das Anforderungsrouting einfacher visualisieren zu können, zeigen zeitachsen jetzt das Service Worker-Start-Up und die `respondWith` Abrufereignisse an.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-129">To make request routing easier to visualize, timelines now display the service worker start-up and the `respondWith` fetch events.</span></span>  <span data-ttu-id="d5d4b-130">Führen Sie die folgenden Aktionen aus, um eine Netzwerkanforderung zu debuggen und zu visualisieren, die an einen Service Worker übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-130">To debug and visualize a network request that passed through a service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="d5d4b-131">Wählen Sie die Netzwerkanforderung aus, die über einen Service Worker gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-131">Choose the network request that went through a service worker.</span></span>  
1.  <span data-ttu-id="d5d4b-132">Öffnen Sie das **Timing-Tool.**</span><span class="sxs-lookup"><span data-stu-id="d5d4b-132">Open the **Timing** tool.</span></span>  
    
### <a name="fetch-events"></a><span data-ttu-id="d5d4b-133">Abrufen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="d5d4b-133">Fetch events</span></span>  

<span data-ttu-id="d5d4b-134">Um mehr über die Abrufereignisse zu `respondWith` erfahren, wählen Sie den Dropdownpfeil links neben der `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="d5d4b-134">To learn more about the `respondWith` fetch events, choose the dropdown arrow to the left of the `respondWith`.</span></span>  <span data-ttu-id="d5d4b-135">Verwenden Sie die entsprechenden Dropdownpfeile, um weitere Details über die **ursprüngliche Anforderung** und **die empfangene Antwort**zu finden.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-135">To find more details about the **Original Request** and **Response Received**, use the corresponding dropdown arrows.</span></span>  

## <a name="application"></a><span data-ttu-id="d5d4b-136">Anwendung</span><span class="sxs-lookup"><span data-stu-id="d5d4b-136">Application</span></span>  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Anwendungsansicht" lightbox="../media/sw-application-timeline.msft.png":::
   <span data-ttu-id="d5d4b-138">Anwendungsansicht</span><span class="sxs-lookup"><span data-stu-id="d5d4b-138">Application view</span></span>  
:::image-end:::  

### <a name="service-worker-update-timeline"></a><span data-ttu-id="d5d4b-139">Zeitachse für Dienstmitarbeiteraktualisierungen</span><span class="sxs-lookup"><span data-stu-id="d5d4b-139">Service worker update timeline</span></span>  

<span data-ttu-id="d5d4b-140">Das Microsoft Edge DevTools-Team hat eine Zeitachse im **Anwendungstool** hinzugefügt, um den Aktualisierungslebenszyklus des Service Worker widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-140">The Microsoft Edge DevTools team added a timeline in the **Application** tool to reflect the update lifecycle of the service worker.</span></span>  <span data-ttu-id="d5d4b-141">Es zeigt die Installations- und Aktivierungsereignisse an.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-141">It displays the installation and activation events.</span></span>  <span data-ttu-id="d5d4b-142">Jedes Ereignis verfügt über einen entsprechenden Dropdownpfeil, um Ihnen weitere Details zu geben.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-142">Each of the events has a corresponding dropdown arrow to give you more details.</span></span>  

### <a name="request-routing-and-fetch-events"></a><span data-ttu-id="d5d4b-143">Anfordern des Routings und Abrufen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="d5d4b-143">Request routing and fetch events</span></span>  

<span data-ttu-id="d5d4b-144">Sie können jetzt über das **Netzwerktool** in der Konsolenschublade auf die Zeitachsen der Service worker zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-144">You may now access the service worker timelines through the **Network** tool in the console drawer.</span></span>  <span data-ttu-id="d5d4b-145">Das Feature bietet Vorteile für die Leistung, minimiert die Duplizierung der Benutzeroberfläche und erstellt eine umfassendere Debugumgebung.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-145">The feature benefits performance, minimizes UI duplication, and creates a more comprehensive debugging experience.</span></span>  

1.  <span data-ttu-id="d5d4b-146">Öffnen Sie den Dienstmitarbeiter, den Sie debuggen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-146">Open the service worker you are debugging.</span></span>  
1.  <span data-ttu-id="d5d4b-147">Klicken Sie auf die Schaltfläche **"Netzwerk",** um die [Anforderungsweiterleitung](#network)zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-147">Choose the **Network** button to open up the [request routing experience](#network).</span></span>  
1.  <span data-ttu-id="d5d4b-148">Verwenden Sie die **Dropdowns "respondWith"** zum Abrufen von Ereignisanforderungs- und Antwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-148">Use the **respondWith** dropdowns for fetch event request and response information.</span></span>  

<span data-ttu-id="d5d4b-149">Das **Netzwerktool** zeigt die Netzwerkanforderungen an, die den Dienstmitarbeiter durchlaufen haben, den Sie debuggen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-149">The **Network** tool displays the network requests that went through the service worker you are debugging.</span></span>  <span data-ttu-id="d5d4b-150">Mit dem automatischen Filter können Sie Ihre Untersuchung eingrenzen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-150">The automatic filter is a way to narrow down your exploration.</span></span>

## <a name="sources"></a><span data-ttu-id="d5d4b-151">Quellen</span><span class="sxs-lookup"><span data-stu-id="d5d4b-151">Sources</span></span>  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="DOM-Struktur" lightbox="../media/sw-sources.msft.png":::
   <span data-ttu-id="d5d4b-153">DOM-Struktur</span><span class="sxs-lookup"><span data-stu-id="d5d4b-153">DOM tree</span></span>  
:::image-end:::  

<span data-ttu-id="d5d4b-154">Um weitere Stapelinformationen zu finden, legen Sie einen Haltepunkt im Fetch-Handler fest.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-154">To find more stack information, set a break point in the fetch handler.</span></span>  <span data-ttu-id="d5d4b-155">Die Details führen dazu, wo die Ressource im Seitenskript angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-155">The details lead to where the resource is requested in the page script.</span></span>  <span data-ttu-id="d5d4b-156">Wenn der Debugger innerhalb eines Abrufhandlers angehalten wird, werden im Bereich auf der rechten Seite kombinierte Stapelinformationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-156">When the debugger pauses inside a fetch handler, a combined stack information is displayed in the panel to the right.</span></span>  <span data-ttu-id="d5d4b-157">Danach können Sie sich in den Stapelframes bewegen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-157">After that, you may move around in the stack frames.</span></span>  

### <a name="future-work"></a><span data-ttu-id="d5d4b-158">Zukünftige Arbeit</span><span class="sxs-lookup"><span data-stu-id="d5d4b-158">Future work</span></span>  

<span data-ttu-id="d5d4b-159">Das Microsoft Edge DevTools-Team plant, das Cachedetail weiter zu entwickeln, und untersucht weitere Möglichkeiten, um das Debuggen von Service Workern für [Progressive Webanwendungsentwickler][MdnProgressiveWebApps] zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-159">The Microsoft Edge DevTools team plans to further develop the cache detail and are investigating more ways to improve the service worker debugging experience for [Progressive Web Application][MdnProgressiveWebApps] developers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d5d4b-160">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="d5d4b-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | Mdn"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Progressive Web Apps (PWAs) | Mdn"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Dienstmitarbeiter-API-| Mdn"  
