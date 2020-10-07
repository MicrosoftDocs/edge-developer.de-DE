---
description: How to debug Background Fetch, Background Sync, Notifications, and Push Messages with Microsoft Edge DevTools.
title: Debug Background Services With Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: 1724bd3a5e45734555650c3d46e377161a3a7c65
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992869"
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





# <span data-ttu-id="9ff62-104">Debug Background Services With Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9ff62-104">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="9ff62-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span><span class="sxs-lookup"><span data-stu-id="9ff62-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="9ff62-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="9ff62-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="9ff62-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span><span class="sxs-lookup"><span data-stu-id="9ff62-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="9ff62-108">Background Fetch</span><span class="sxs-lookup"><span data-stu-id="9ff62-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="9ff62-109">Background Sync</span><span class="sxs-lookup"><span data-stu-id="9ff62-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="9ff62-110">Notifications</span><span class="sxs-lookup"><span data-stu-id="9ff62-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="9ff62-111">Push Messages</span><span class="sxs-lookup"><span data-stu-id="9ff62-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="9ff62-112">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span><span class="sxs-lookup"><span data-stu-id="9ff62-112">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="9ff62-113">This can help you make sure that events are being sent and received as expected.</span><span class="sxs-lookup"><span data-stu-id="9ff62-113">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="9ff62-114">You may also inspect the details of each event.</span><span class="sxs-lookup"><span data-stu-id="9ff62-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="9ff62-116">View the details of an event in the **Push Messaging** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-116">View the details of an event in the **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="9ff62-117">Background Fetch</span><span class="sxs-lookup"><span data-stu-id="9ff62-117">Background Fetch</span></span>   

<span data-ttu-id="9ff62-118">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span><span class="sxs-lookup"><span data-stu-id="9ff62-118">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="9ff62-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span><span class="sxs-lookup"><span data-stu-id="9ff62-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="9ff62-120">[Open DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="9ff62-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="9ff62-121">Open the **Application** panel.</span><span class="sxs-lookup"><span data-stu-id="9ff62-121">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="9ff62-122">Open the **Background Fetch** pane.</span><span class="sxs-lookup"><span data-stu-id="9ff62-122">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="9ff62-124">The **Background Fetch** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-124">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ff62-125">Click **Record** \(![Record][ImageRecordIcon]\).</span><span class="sxs-lookup"><span data-stu-id="9ff62-125">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="9ff62-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span><span class="sxs-lookup"><span data-stu-id="9ff62-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="9ff62-128">A log of events in the **Background Fetch** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-128">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ff62-129">Click an event to view its details in the space below the table.</span><span class="sxs-lookup"><span data-stu-id="9ff62-129">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="9ff62-131">View the details of an event in the **Background Fetch** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9ff62-132">Background Sync</span><span class="sxs-lookup"><span data-stu-id="9ff62-132">Background Sync</span></span>   

<span data-ttu-id="9ff62-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span><span class="sxs-lookup"><span data-stu-id="9ff62-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="9ff62-134">To log Background Sync events for 3 days, even when DevTools is not open:</span><span class="sxs-lookup"><span data-stu-id="9ff62-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="9ff62-135">[Open DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="9ff62-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="9ff62-136">Open the **Application** panel.</span><span class="sxs-lookup"><span data-stu-id="9ff62-136">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="9ff62-137">Open the **Background Sync** pane.</span><span class="sxs-lookup"><span data-stu-id="9ff62-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="9ff62-139">The **Background Sync** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ff62-140">Click **Record** \(![Record][ImageRecordIcon]\).</span><span class="sxs-lookup"><span data-stu-id="9ff62-140">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="9ff62-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span><span class="sxs-lookup"><span data-stu-id="9ff62-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="9ff62-143">A log of events in the **Background Sync** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ff62-144">Click an event to view its details in the space below the table.</span><span class="sxs-lookup"><span data-stu-id="9ff62-144">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="9ff62-146">View the details of an event in the **Background Sync** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9ff62-147">Notifications</span><span class="sxs-lookup"><span data-stu-id="9ff62-147">Notifications</span></span> 

<span data-ttu-id="9ff62-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span><span class="sxs-lookup"><span data-stu-id="9ff62-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="9ff62-149">To log Notifications for 3 days, even when DevTools is not open:</span><span class="sxs-lookup"><span data-stu-id="9ff62-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="9ff62-150">[Open DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="9ff62-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="9ff62-151">Open the **Application** panel.</span><span class="sxs-lookup"><span data-stu-id="9ff62-151">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="9ff62-152">Open the **Notifications** pane.</span><span class="sxs-lookup"><span data-stu-id="9ff62-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="9ff62-154">The **Notifications** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ff62-155">Click **Record** \(![Record][ImageRecordIcon]\).</span><span class="sxs-lookup"><span data-stu-id="9ff62-155">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="9ff62-156">After triggering some Notifications activity, DevTools logs the events to the table.</span><span class="sxs-lookup"><span data-stu-id="9ff62-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="9ff62-158">A log of events in the **Notifications** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ff62-159">Click an event to view its details in the space below the table.</span><span class="sxs-lookup"><span data-stu-id="9ff62-159">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="9ff62-161">View the details of an event in the **Notifications** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9ff62-162">Push Messages</span><span class="sxs-lookup"><span data-stu-id="9ff62-162">Push Messages</span></span> 

<span data-ttu-id="9ff62-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span><span class="sxs-lookup"><span data-stu-id="9ff62-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="9ff62-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="9ff62-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="9ff62-165">To log Push Messages for 3 days, even when DevTools is not open:</span><span class="sxs-lookup"><span data-stu-id="9ff62-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="9ff62-166">[Open DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="9ff62-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="9ff62-167">Open the **Application** panel.</span><span class="sxs-lookup"><span data-stu-id="9ff62-167">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="9ff62-168">Open the **Push Messaging** pane.</span><span class="sxs-lookup"><span data-stu-id="9ff62-168">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="9ff62-170">The **Push Messaging** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-170">The **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ff62-171">Click **Record** \(![Record][ImageRecordIcon]\).</span><span class="sxs-lookup"><span data-stu-id="9ff62-171">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="9ff62-172">After triggering some Push Message activity, DevTools logs the events to the table.</span><span class="sxs-lookup"><span data-stu-id="9ff62-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="9ff62-174">A log of events in the **Push Messaging** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ff62-175">Click an event to view its details in the space below the table.</span><span class="sxs-lookup"><span data-stu-id="9ff62-175">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="View the details of an event in the Push Messaging pane" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="9ff62-177">View the details of an event in the **Push Messaging** pane</span><span class="sxs-lookup"><span data-stu-id="9ff62-177">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Open Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Notifications API | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "Push API | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "Background process - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="9ff62-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9ff62-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9ff62-183">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="9ff62-183">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="9ff62-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9ff62-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
