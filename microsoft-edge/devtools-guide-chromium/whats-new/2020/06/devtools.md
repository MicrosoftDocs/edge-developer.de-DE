---
description: CSS-Rasterdebuggingfeatures, Bearbeiten und Wiederholen von Anforderungen mit der Netzwerkkonsole und vieles mehr.
title: Neuigkeiten in DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 65a3fb4da235d2330bf9205b7a4a79a999559ca4
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624801"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-85"></a><span data-ttu-id="71ad9-104">Neuigkeiten in DevTools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="71ad9-104">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="71ad9-105">Ankündigungen des Microsoft Edge DevTools-Teams</span><span class="sxs-lookup"><span data-stu-id="71ad9-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="71ad9-106">In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise vom Microsoft Edge DevTools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="71ad9-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="71ad9-107">Sehen Sie sich die Ankündigungen an, um neue Features in devTools, Microsoft Visual Studio Codeerweiterungen und vieles mehr auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="71ad9-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="71ad9-108">Um über die neuesten und besten Features in Ihren Entwicklertools auf dem Laufenden zu bleiben, laden Sie die [Microsoft Edge Vorschaukanäle][MicrosoftEdgePreviewChannels] herunter, und [folgen Sie dem Microsoft Edge DevTools-Team auf Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="71ad9-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="css-grid-debugging-features"></a><span data-ttu-id="71ad9-109">CSS-Rasterdebuggingfeatures</span><span class="sxs-lookup"><span data-stu-id="71ad9-109">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="71ad9-111">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="71ad9-111">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-112">Das Microsoft Edge DevTools-Team arbeitet mit dem Chrome DevTools-Team und Chromium Community zusammen, um DevTools neue CSS-Rasterdebuggingfeatures hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="71ad9-112">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="71ad9-113">Sie können jetzt Rasterliniennummern, Rasterlücken und erweiterte Rasterlinien als Seitenüberlagerung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="71ad9-113">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="71ad9-114">Darüber hinaus werden in Kürze weitere Verbesserungen an den Rastertools verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="71ad9-114">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="CSS-Rasterdebuggingfeatures" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="71ad9-116">CSS-Rasterdebuggingfeatures</span><span class="sxs-lookup"><span data-stu-id="71ad9-116">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="71ad9-117">Um das Experiment zu aktivieren, navigieren Sie zu ["Experimentelle Features aktivieren",][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben **"Neue CSS-Rasterdebuggingfeatures aktivieren".**</span><span class="sxs-lookup"><span data-stu-id="71ad9-117">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="71ad9-118">Um das Experiment mit einem Beispiel auszuprobieren, navigieren Sie zum [CSS-Rasterplanerbeispiel.][CodepenRachelweilYzwBzKM]</span><span class="sxs-lookup"><span data-stu-id="71ad9-118">To try out the experiment with a sample, navigate to [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="71ad9-119">Chromium Problem [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="71ad9-119">Chromium issue [#1047356][CR1047356]</span></span>  

### <a name="edit-and-replay-requests-with-the-network-console"></a><span data-ttu-id="71ad9-120">Bearbeiten und Wiedergeben von Anforderungen mit der Netzwerkkonsole</span><span class="sxs-lookup"><span data-stu-id="71ad9-120">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="71ad9-122">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="71ad9-122">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-123">Sie können jetzt **Bearbeiten und Wiedergeben** von Anforderungen im [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity] mithilfe der **Netzwerkkonsole**verwenden.</span><span class="sxs-lookup"><span data-stu-id="71ad9-123">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Bearbeiten und Wiedergeben einer Anforderung im Netzwerkprotokoll mit der Netzwerkkonsole" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="71ad9-125">Bearbeiten und Wiedergeben einer Anforderung im [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity] mit der **Netzwerkkonsole**</span><span class="sxs-lookup"><span data-stu-id="71ad9-125">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-126">In einem neuen Bereich wird die **Netzwerkkonsole** in der [DevTools-Schublade][DevtoolsCustomizeIndexDrawer] geöffnet und automatisch mit Informationen für die HTTP-Anforderung aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-126">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="71ad9-127">Bearbeiten Sie zum Anzeigen der vom Server zurückgegebenen Antwort die Anforderung \(falls erforderlich\), und wählen Sie **"Senden"** aus.</span><span class="sxs-lookup"><span data-stu-id="71ad9-127">To display the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="71ad9-128">Sie können auch die **Netzwerkkonsole** verwenden, um HTTP-Anforderungen direkt über devTools zu erstellen und zu senden.</span><span class="sxs-lookup"><span data-stu-id="71ad9-128">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Der Bereich "Netzwerkkonsole"" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="71ad9-130">**Der Bereich "Netzwerkkonsole"**</span><span class="sxs-lookup"><span data-stu-id="71ad9-130">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="71ad9-131">Um die **Netzwerkkonsole** im Hauptbereich \(oben\) anstelle der [DevTools-Schublade][DevtoolsCustomizeIndexDrawer]anzuzeigen, navigieren Sie zu Verschieben von [Tools zwischen Bereichen.](#move-tools-between-panels)</span><span class="sxs-lookup"><span data-stu-id="71ad9-131">To display **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], navigate to [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="71ad9-132">Um das Experiment zu aktivieren, navigieren Sie zu ["Experimentelle Features aktivieren",][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben **"Netzwerkkonsole aktivieren".**</span><span class="sxs-lookup"><span data-stu-id="71ad9-132">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="71ad9-133">Öffnen Sie das [Netzwerkprotokoll,][DevtoolsNetworkIndexLogActivity]öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **Bearbeiten und Wiedergeben**aus.</span><span class="sxs-lookup"><span data-stu-id="71ad9-133">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  

<span data-ttu-id="71ad9-134">Chromium Problem [#1093687][CR1093687]</span><span class="sxs-lookup"><span data-stu-id="71ad9-134">Chromium issue [#1093687][CR1093687]</span></span>  

### <a name="service-worker-respondwith-events-in-the-timing-tab"></a><span data-ttu-id="71ad9-135">Service Worker respondWith-Ereignisse auf der Registerkarte "Timing"</span><span class="sxs-lookup"><span data-stu-id="71ad9-135">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="71ad9-136">Die Registerkarte **"Timing"** des **Netzwerktools** enthält jetzt `respondWith` Service Worker-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="71ad9-136">The **Timing** tab of the **Network** tool now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="71ad9-137">Das `respondWith` Service Worker-Ereignis zeigt die Dauer von der Zeit unmittelbar vor der Ausführung des Service `fetch` Worker-Ereignishandlers bis zu dem Zeitpunkt an, zu dem `respondWith` die Zusage des `fetch` Handlers nicht erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="71ad9-137">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Das RespondWith Service Worker-Ereignis auf der Registerkarte "Timing" des Netzwerkbereichs" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="71ad9-139">Das `respondWith` Service Worker-Ereignis auf der Registerkarte **"Timing"** des **Netzwerktools**</span><span class="sxs-lookup"><span data-stu-id="71ad9-139">The `respondWith` service worker event in the **Timing** tab of the **Network** tool</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-140">Erweitern Sie **die empfangene Antwort,** um zusätzliche Informationen aus der `fetch` Antwort anzuzeigen, z. `CacheStorageCacheName` B. , und `serviceWorkerResponseSource` `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="71ad9-140">Expand **Response received** to display additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Erweitern der empfangenen Antwort, um zusätzliche Informationen aus der Abrufantwort anzuzeigen" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="71ad9-142">Erweitern sie **die empfangene Antwort,** um zusätzliche Informationen aus der Antwort anzuzeigen. `fetch`</span><span class="sxs-lookup"><span data-stu-id="71ad9-142">Expand **Response received** to display additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-143">Chromium Problem [#1066579][CR1066579]</span><span class="sxs-lookup"><span data-stu-id="71ad9-143">Chromium issue [#1066579][CR1066579]</span></span>  

### <a name="webhint-feedback-in-the-issues-panel"></a><span data-ttu-id="71ad9-144">Webhint-Feedback im Bereich "Probleme"</span><span class="sxs-lookup"><span data-stu-id="71ad9-144">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="71ad9-146">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="71ad9-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-147">[Webhint][WebhintMain] ist ein Open Source-Tool, das Echtzeitfeedback zu Barrierefreiheit, browserübergreifender Kompatibilität, Sicherheit, Leistung, PWAs und anderen allgemeinen Webentwicklungsproblemen von Websites bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-147">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="71ad9-148">So überprüfen Sie Webhint-Feedback im [Bereich "Probleme".][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="71ad9-148">To review webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Webhint-Feedback im Bereich "Probleme"" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="71ad9-150">Webhint-Feedback im Bereich "Probleme"</span><span class="sxs-lookup"><span data-stu-id="71ad9-150">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="71ad9-151">Um das Experiment zu aktivieren, navigieren Sie zu ["Experimentelle Features aktivieren",][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben **"Webhint aktivieren".**</span><span class="sxs-lookup"><span data-stu-id="71ad9-151">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="71ad9-152">Öffnen Sie den [Bereich "Probleme",][DevtoolsIssues] um Feedback von Webhint anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="71ad9-152">Open the [Issues][DevtoolsIssues] panel to display feedback from webhint.</span></span>  

<span data-ttu-id="71ad9-153">Chromium Problem [#1070378][CR1070378]</span><span class="sxs-lookup"><span data-stu-id="71ad9-153">Chromium issue [#1070378][CR1070378]</span></span>  

### <a name="move-tools-between-panels"></a><span data-ttu-id="71ad9-154">Verschieben von Tools zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="71ad9-154">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   <span data-ttu-id="71ad9-156">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="71ad9-156">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-157">Normalerweise können Tools wie **"Elemente"** und **"Netzwerk"** nur im Hauptbereich \(oben\) von DevTools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="71ad9-157">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="71ad9-158">Ebenso können Tools wie **die 3D-Ansicht** und **Probleme** nur im Bereich "Schublade \(bottom\)" von DevTools geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="71ad9-158">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="71ad9-159">Sie können nun Ihr DevTools-Layout anpassen, indem Sie Tools zwischen den oberen und unteren Bereichen verschieben.</span><span class="sxs-lookup"><span data-stu-id="71ad9-159">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Verschieben von Tools zwischen Bereichen" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="71ad9-161">Verschieben von Tools zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="71ad9-161">Move tools between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="71ad9-162">Um das Experiment zu aktivieren, navigieren Sie zu ["Experimentelle Features aktivieren",][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben "Unterstützung zum Verschieben von **Registerkarten zwischen Bereichen aktivieren".**</span><span class="sxs-lookup"><span data-stu-id="71ad9-162">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="71ad9-163">Chromium Problem [#897944][CR897944]</span><span class="sxs-lookup"><span data-stu-id="71ad9-163">Chromium issue [#897944][CR897944]</span></span>  

### <a name="improved-initiator-tooltip-in-the-network-panel"></a><span data-ttu-id="71ad9-164">Verbesserte Initiator-QuickInfo im Netzwerkbereich</span><span class="sxs-lookup"><span data-stu-id="71ad9-164">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="71ad9-165">In Microsoft Edge 83 und 84 quickinfos for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span><span class="sxs-lookup"><span data-stu-id="71ad9-165">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="71ad9-166">Sie konnten nur den Aufrufstapel anzeigen, der die Anforderung initiiert hat, indem Sie in der QuickInfo horizontal scrollen.</span><span class="sxs-lookup"><span data-stu-id="71ad9-166">You were only able to display the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Die Initiator-QuickInfo in Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="71ad9-168">Die Initiator-QuickInfo in Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="71ad9-168">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-169">Ab Microsoft Edge 85 können Sie nun den Initiator-Aufrufstapel in der QuickInfo anzeigen, ohne horizontal zu scrollen.</span><span class="sxs-lookup"><span data-stu-id="71ad9-169">Starting with Microsoft Edge 85, you are now able to display the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Die Initiator-QuickInfo in Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="71ad9-171">Die Initiator-QuickInfo in Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="71ad9-171">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="71ad9-172">Chromium Problem [#1069404][CR1069404]</span><span class="sxs-lookup"><span data-stu-id="71ad9-172">Chromium issue [#1069404][CR1069404]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="71ad9-173">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="71ad9-173">Announcements from the Chromium project</span></span>  

<span data-ttu-id="71ad9-174">In den folgenden Abschnitten werden zusätzliche Features angekündigt, die in Microsoft Edge 85 verfügbar sind und zum Open Source Chromium Projekt beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="71ad9-174">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <a name="style-editing-for-css-in-js-frameworks"></a><span data-ttu-id="71ad9-175">Formatvorlagenbearbeitung für CSS-in-JS-Frameworks</span><span class="sxs-lookup"><span data-stu-id="71ad9-175">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="71ad9-176">Der Bereich **"Formatvorlagen"** bietet jetzt eine bessere Unterstützung für die Bearbeitung von Formatvorlagen, die mit den [CSS-Objektmodell-APIs (CSSOM)][CsswgDraftsCssom] erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="71ad9-176">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="71ad9-177">Viele CSS-in-JS-Frameworks und -Bibliotheken verwenden die CSSOM-APIs im Rahmen der Erstellung von Formatvorlagen.</span><span class="sxs-lookup"><span data-stu-id="71ad9-177">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="71ad9-178">Sie können jetzt Formatvorlagen bearbeiten, die in JavaScript [mithilfe von constructable Stylesheets][WicgConstructStylesheet]hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="71ad9-178">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="71ad9-179">Konstruktierbare Stylesheets sind eine neue Möglichkeit zum Erstellen und Verteilen wiederverwendbarer Formatvorlagen bei Verwendung von [Shadow DOM.][MdnShadowDom]</span><span class="sxs-lookup"><span data-stu-id="71ad9-179">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="71ad9-180">Beispielsweise waren die `h1` mit `CSSStyleSheet` \(CSSOM-APIs\) hinzugefügten Formatvorlagen zuvor nicht bearbeitbar.</span><span class="sxs-lookup"><span data-stu-id="71ad9-180">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="71ad9-181">Die Formatvorlagen können jetzt im Bereich **"Formatvorlagen"** bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="71ad9-181">The styles are editable now in the **Styles** panel.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Ändern der Hintergrundeigenschaft der h1-Formatvorlagen, die mit CSSStyleSheet hinzugefügt wurden, von Rosa in Hellblau" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="71ad9-183">Ändern der `background` Eigenschaft der `h1` Formatvorlagen, mit denen hinzugefügt `CSSStyleSheet` wurde, in `pink` `lightblue` .</span><span class="sxs-lookup"><span data-stu-id="71ad9-183">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="71ad9-184">Probieren Sie dieses Feature mit einem [Beispiel aus, das CSS-in-JS verwendet.][CodepenZoherghadyaliAbdgrpz]</span><span class="sxs-lookup"><span data-stu-id="71ad9-184">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="71ad9-185">Chromium Problem [#946975][CR946975]</span><span class="sxs-lookup"><span data-stu-id="71ad9-185">Chromium issue [#946975][CR946975]</span></span>  

### <a name="lighthouse-6-in-the-lighthouse-panel"></a><span data-ttu-id="71ad9-186">"6" im Panel "Panels"</span><span class="sxs-lookup"><span data-stu-id="71ad9-186">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="71ad9-187">Im **Panel "Panels"** wird jetzt "6" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-187">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="71ad9-188">Navigieren Sie für eine vollständige Liste aller Änderungen zu [den Versionshinweisen von v6.0.0.][GithubGoogleChromeLighthouse600]</span><span class="sxs-lookup"><span data-stu-id="71ad9-188">For a full list of all changes, navigate to [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="71ad9-189">Mit "6.0" werden drei neue Metriken in den Bericht eingeführt: größte contentful Paint \(LCP\), kumulative Layoutverschiebung \(CLS\) und Gesamtblockierungszeit \(TBT\).</span><span class="sxs-lookup"><span data-stu-id="71ad9-189">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="71ad9-190">Die Leistungsbewertungsformel wurde ebenfalls neu gewichtet, um die Ladeerfahrung des Benutzers besser widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="71ad9-190">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="71ad9-191">Chromium Problem [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="71ad9-191">Chromium issue [#772558][CR772558]</span></span>  

#### <a name="first-meaningful-paint-deprecation"></a><span data-ttu-id="71ad9-192">First Meaningful Paint deprecation</span><span class="sxs-lookup"><span data-stu-id="71ad9-192">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="71ad9-193">First Meaningful Paint \(FMP\) is deprecated inIron 6.0.</span><span class="sxs-lookup"><span data-stu-id="71ad9-193">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="71ad9-194">FMP wurde auch aus dem **Leistungsbereich** entfernt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-194">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="71ad9-195">**Der größte inhaltsreiche Paint** ist der empfohlene Ersatz für FMP.</span><span class="sxs-lookup"><span data-stu-id="71ad9-195">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--For an explanation of why it was deprecated, navigate to [First Meaningful Paint][WebDevFirstMeaningfulPaint].  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="71ad9-196">Chromium Problem [#1096008][CR1096008]</span><span class="sxs-lookup"><span data-stu-id="71ad9-196">Chromium issue [#1096008][CR1096008]</span></span>  

### <a name="support-for-new-javascript-features"></a><span data-ttu-id="71ad9-197">Unterstützung für neue JavaScript-Features</span><span class="sxs-lookup"><span data-stu-id="71ad9-197">Support for new JavaScript features</span></span>  

<span data-ttu-id="71ad9-198">DevTools bietet jetzt eine bessere Unterstützung für einige der neuesten JavaScript-Sprachfeatures.</span><span class="sxs-lookup"><span data-stu-id="71ad9-198">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="71ad9-199">[Optionale automatische Verkettungssyntax][V8DevOptionalChaining]</span><span class="sxs-lookup"><span data-stu-id="71ad9-199">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="71ad9-200">Die automatische Vervollständigung der Eigenschaft in der **Konsole** unterstützt jetzt die optionale Verkettungssyntax, z. B.  `name?.` funktioniert jetzt zusätzlich zu und `name.` `name[` .</span><span class="sxs-lookup"><span data-stu-id="71ad9-200">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="71ad9-201">Syntaxhervorhebung für [private Felder][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="71ad9-201">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="71ad9-202">Private Klassenfelder werden nun im Bereich **"Quellen"** korrekt hervorgehoben und ziemlich gedruckt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-202">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="71ad9-203">Syntaxhervorhebung für [Nullish-Koalescing-Operator][V8DevNullishCoalescing]</span><span class="sxs-lookup"><span data-stu-id="71ad9-203">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="71ad9-204">DevTools druckt nun den Null-Koalescing-Operator im **Quellenbereich** ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="71ad9-204">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="71ad9-205">Chromium Probleme [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="71ad9-205">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <a name="new-app-shortcut-warnings-in-the-manifest-pane"></a><span data-ttu-id="71ad9-206">Warnungen zu neuen App-Verknüpfungen im Manifestbereich</span><span class="sxs-lookup"><span data-stu-id="71ad9-206">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="71ad9-207">**App-Verknüpfungen** helfen Benutzern, allgemeine oder empfohlene Aufgaben innerhalb einer Web-App schnell zu starten.</span><span class="sxs-lookup"><span data-stu-id="71ad9-207">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="71ad9-208">Im **Manifestbereich** werden nun Warnungen für die folgenden Bedingungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-208">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="71ad9-209">Die App-Verknüpfungssymbole sind kleiner als 96 x 96 Pixel</span><span class="sxs-lookup"><span data-stu-id="71ad9-209">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="71ad9-210">Die App-Verknüpfungssymbole und Manifestsymbole sind nicht quadratisch \(da die Symbole ignoriert werden\)</span><span class="sxs-lookup"><span data-stu-id="71ad9-210">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="App-Tastenkombinationswarnungen" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="71ad9-212">App-Tastenkombinationswarnungen</span><span class="sxs-lookup"><span data-stu-id="71ad9-212">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-213">Chromium Problem [#955497][CR955497]</span><span class="sxs-lookup"><span data-stu-id="71ad9-213">Chromium issue [#955497][CR955497]</span></span>  

### <a name="consistent-display-of-the-computed-pane"></a><span data-ttu-id="71ad9-214">Konsistente Anzeige des berechneten Bereichs</span><span class="sxs-lookup"><span data-stu-id="71ad9-214">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="71ad9-215">Der \*\*Bereich Berechnet \*\* im Tool \*\* Elemente \*\* wird jetzt konsistent als Bereich für alle Viewportgrößen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-215">The **Computed** pane in the **Elements** tool now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="71ad9-216">Zuvor wurde der **Bereich "Berechnet"** im Bereich **"Formatvorlagen"** zusammengeführt, wenn die Breite des DevTools-Viewports schmal war.</span><span class="sxs-lookup"><span data-stu-id="71ad9-216">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Der berechnete Bereich wird konsistent als separater Bereich angezeigt, auch wenn die DevTools schmal sind." lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="71ad9-218">Der **berechnete** Bereich wird konsistent als separater Bereich angezeigt, auch wenn die DevTools schmal sind.</span><span class="sxs-lookup"><span data-stu-id="71ad9-218">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="71ad9-219">Chromium Problem [#1073899][CR1073899]</span><span class="sxs-lookup"><span data-stu-id="71ad9-219">Chromium issue [#1073899][CR1073899]</span></span>  

### <a name="bytecode-offsets-for-webassembly-files"></a><span data-ttu-id="71ad9-220">Bytecode-Offsets für WebAssembly-Dateien</span><span class="sxs-lookup"><span data-stu-id="71ad9-220">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="71ad9-221">DevTools verwendet jetzt Bytecode-Offsets zum Anzeigen von Zeilennummern der Wasm-Zerlegung.</span><span class="sxs-lookup"><span data-stu-id="71ad9-221">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="71ad9-222">Die Zeilennummern verdeutlichen, dass Sie binäre Daten betrachten, und sind konsistenter mit der Art und Weise, wie die Wasm-Laufzeit auf Speicherorte verweist.</span><span class="sxs-lookup"><span data-stu-id="71ad9-222">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="71ad9-223">Chromium Problem [#1071432][CR1071432]</span><span class="sxs-lookup"><span data-stu-id="71ad9-223">Chromium issue [#1071432][CR1071432]</span></span>  

### <a name="line-wise-copy-and-cut-in-sources-panel"></a><span data-ttu-id="71ad9-224">Zeilenweises Kopieren und Ausschneiden im Quellenbereich</span><span class="sxs-lookup"><span data-stu-id="71ad9-224">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="71ad9-225">Wenn Sie das Kopieren oder Ausschneiden ohne Auswahl im Editor des [Quellenbereichs][DevtoolsSourcesIndexUsingEditorPaneToViewEditFiles]ausführen, kopiert oder schneidet DevTools die aktuelle Inhaltszeile.</span><span class="sxs-lookup"><span data-stu-id="71ad9-225">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesIndexUsingEditorPaneToViewEditFiles], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Mit dem Cursor am Ende von Zeile 5 kopieren Sie die gesamte Zeile aus pen.js in devTools und einfügen in Visual Studio Code" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="71ad9-227">Kopieren Sie mit dem Cursor am Ende von Zeile 5 die gesamte Zeile aus **pen.js** in den DevTools, und kopieren Sie sie in [Visual Studio Code.][VisualStudioCode]</span><span class="sxs-lookup"><span data-stu-id="71ad9-227">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [Visual Studio Code][VisualStudioCode].</span></span>
:::image-end:::  

<span data-ttu-id="71ad9-228">Chromium Problem [#800028][CR800028]</span><span class="sxs-lookup"><span data-stu-id="71ad9-228">Chromium issue [#800028][CR800028]</span></span>

### <a name="console-settings-updates"></a><span data-ttu-id="71ad9-229">Konsolen-Einstellungen-Updates</span><span class="sxs-lookup"><span data-stu-id="71ad9-229">Console Settings updates</span></span>  

#### <a name="ungroup-same-console-messages"></a><span data-ttu-id="71ad9-230">Aufheben der Gruppierung derselben Konsolennachrichten</span><span class="sxs-lookup"><span data-stu-id="71ad9-230">Ungroup same console messages</span></span>  

<span data-ttu-id="71ad9-231">Die **Umschaltfläche "Gruppe"** in konsolenähnlicher Einstellungen gilt jetzt für doppelte Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="71ad9-231">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="71ad9-232">Zuvor wurde sie nur auf ähnliche Nachrichten angewendet.</span><span class="sxs-lookup"><span data-stu-id="71ad9-232">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="71ad9-233">Beispielsweise hat DevTools zuvor die Gruppierung der Nachrichten nicht aufgehoben, `hello` obwohl **"Gruppe ähnlich"** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="71ad9-233">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="71ad9-234">Jetzt werden die Gruppierung der `hello` Nachrichten aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="71ad9-234">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Wenn "Gruppe ähnlich" deaktiviert ist, werden die Hello-Nachrichten nicht gruppiert." lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="71ad9-236">Wenn **"Gruppe ähnlich"** deaktiviert ist, werden die Gruppierung der `hello` Nachrichten aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="71ad9-236">When **Group similar** is unchecked, the `hello` messages are ungrouped</span></span>
:::image-end:::  

<span data-ttu-id="71ad9-237">Probieren Sie dieses Feature mit einem [Beispiel aus, das doppelte Nachrichten an die Konsole sendet.][CodepenZoherghadyaliZyrjgdJ]</span><span class="sxs-lookup"><span data-stu-id="71ad9-237">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="71ad9-238">Chromium Problem [#1082963][CR1082963]</span><span class="sxs-lookup"><span data-stu-id="71ad9-238">Chromium issue [#1082963][CR1082963]</span></span>  

### <a name="persisting-selected-context-only-settings"></a><span data-ttu-id="71ad9-239">Speichern ausgewählter Kontexteinstellungen</span><span class="sxs-lookup"><span data-stu-id="71ad9-239">Persisting Selected context only settings</span></span>  

<span data-ttu-id="71ad9-240">Die Einstellungen für **den ausgewählten Kontext** in Konsolen-Einstellungen werden jetzt beibehalten.</span><span class="sxs-lookup"><span data-stu-id="71ad9-240">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="71ad9-241">Zuvor wurden die Einstellungen jedes Mal zurückgesetzt, wenn Sie DevTools geschlossen und erneut geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="71ad9-241">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="71ad9-242">Die Änderung sorgt dafür, dass das Einstellungsverhalten mit anderen Konsolen-Einstellungen-Optionen konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="71ad9-242">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Einstellung nur für ausgewählten Kontext" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="71ad9-244">**Einstellung nur für ausgewählten Kontext**</span><span class="sxs-lookup"><span data-stu-id="71ad9-244">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-245">Chromium Problem [#1055875][CR1055875]</span><span class="sxs-lookup"><span data-stu-id="71ad9-245">Chromium issue [#1055875][CR1055875]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="71ad9-246">Aktualisierungen des Leistungsbereichs</span><span class="sxs-lookup"><span data-stu-id="71ad9-246">Performance panel updates</span></span>  

#### <a name="javascript-compilation-cache-information-in-performance-tool"></a><span data-ttu-id="71ad9-247">JavaScript-Kompilierungscacheinformationen im **Leistungstool**</span><span class="sxs-lookup"><span data-stu-id="71ad9-247">JavaScript compilation cache information in **Performance** tool</span></span>  

<span data-ttu-id="71ad9-248">[JavaScript-Kompilierungscacheinformationen][V8DevCodeCaching] werden jetzt immer im **Zusammenfassungsbereich** des **Leistungstools** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-248">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the **Summary** panel of the **Performance** tool.</span></span>  <span data-ttu-id="71ad9-249">Bisher hat DevTools nichts im Zusammenhang mit der Codezwischenspeicherung angezeigt, wenn keine Codezwischenspeicherung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="71ad9-249">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="JavaScript-Kompilierungscacheinformationen" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="71ad9-251">JavaScript-Kompilierungscacheinformationen</span><span class="sxs-lookup"><span data-stu-id="71ad9-251">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-252">Chromium Problem [#912581][CR912581]</span><span class="sxs-lookup"><span data-stu-id="71ad9-252">Chromium issue [#912581][CR912581]</span></span>  

#### <a name="navigation-timing-alignment-in-the-performance-panel"></a><span data-ttu-id="71ad9-253">Ausrichtung des Navigationszeitpunkts im Leistungsbereich</span><span class="sxs-lookup"><span data-stu-id="71ad9-253">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="71ad9-254">Der **Leistungsbereich,** der verwendet wird, um Zeiten in den Lineals basierend auf dem Start der Aufzeichnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="71ad9-254">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="71ad9-255">Das Timing für Aufzeichnungen, in denen der Benutzer navigiert, wurde nun geändert, wobei DevTools stattdessen Linealzeiten relativ zur Navigation anzeigt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-255">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Ausrichten des Navigationszeitpunkts im Leistungstool" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="71ad9-257">Ausrichten des Navigationszeitpunkts im **Leistungstool**</span><span class="sxs-lookup"><span data-stu-id="71ad9-257">Align navigation timing in **Performance** tool</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-258">Die Zeiten für `DOMContentLoaded` ereignisse , first Paint, First Contentful Paint und Largest Contentful Paint werden so aktualisiert, dass sie relativ zum Start der Navigation sind, was bedeutet, dass das Timing mit den von gemeldeten Zeitangaben `PerformanceObserver` übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-258">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="71ad9-259">Chromium Problem [#974550][CR974550]</span><span class="sxs-lookup"><span data-stu-id="71ad9-259">Chromium issue [#974550][CR974550]</span></span>  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a><span data-ttu-id="71ad9-260">Neue Symbole für Haltepunkte, bedingte Haltepunkte und Protokollpunkte</span><span class="sxs-lookup"><span data-stu-id="71ad9-260">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="71ad9-261">Der **Quellenbereich** verfügt über neue Designs für Haltepunkte, bedingte Haltepunkte und Protokollpunkte.</span><span class="sxs-lookup"><span data-stu-id="71ad9-261">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="71ad9-262">Haltepunkte werden wie [Visual Studio Code][VisualStudioCode] und [Visual Studio][VisualStudio]durch einen roten Kreis dargestellt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-262">Breakpoints are represented by a red circle, just like [Visual Studio Code][VisualStudioCode] and [Visual Studio][VisualStudio].</span></span>  <span data-ttu-id="71ad9-263">Symbole werden hinzugefügt, um bedingte Haltepunkte und Protokollpunkte zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="71ad9-263">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Breakpoints" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="71ad9-265">Breakpoints</span><span class="sxs-lookup"><span data-stu-id="71ad9-265">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="71ad9-266">Chromium Problem [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="71ad9-266">Chromium issue [#1041830][CR1041830]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="71ad9-267">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="71ad9-267">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="71ad9-268">Wenn Sie Windows oder macOS verwenden, sollten Sie die [Microsoft Edge Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="71ad9-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="71ad9-269">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="71ad9-269">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="71ad9-270">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="71ad9-270">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../../../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsCommandMenu]: ../../../command-menu.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft-Dokumente"
[DevtoolsCustomizeIndexDrawer]: ../../../customize/index.md#drawer "Schublade – Anpassen Microsoft Edge DevTools-| Microsoft-Dokumente"
[DevtoolsExperimentalFeaturesTurnOn]: ../../../experimental-features/index.md#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsIssues]: ../../../issues/index.md "Suchen und Beheben von Problemen mithilfe des Tools &quot;Probleme&quot; | Microsoft-Dokumente"
[DevtoolsSourcesIndexUsingEditorPaneToViewEditFiles]: ../../../sources/index.md#using-the-editor-pane-to-view-or-edit-files "Verwenden des Editorbereichs zum Anzeigen oder Bearbeiten von Dateien – Übersicht über den Quellenbereich | Microsoft-Dokumente"  
[DevtoolsNetworkIndexLogActivity]: ../../../network/index.md#log-network-activity "Protokollieren von Netzwerkaktivitäten – Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools-| Microsoft-Dokumente"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Formatvorlagenbearbeitung für CSS-in-JS-Frameworks | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Senden doppelter Nachrichten an konsolen | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "CSS-Rasterplaner –Beispiel | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

[CR772558]: https://crbug.com/772558 "DevTools: Update auf die neueste Version von | Chromium Fehler"  
[CR800028]: https://crbug.com/800028 "Doppelte Zeilenverknüpfung im Entwicklertools-Editor funktioniert nach chrome update | Chromium Fehler"  
[CR912581]: https://crbug.com/912581 "Verfügbar machen, welche Skripts von V8 in DevTools/about:tracing | codecachediert wurden Chromium Fehler"  
[CR946975]: https://crbug.com/946975 "Die DevTools-Formatvorlagen-Randleiste funktioniert nicht mit erstellten Stylesheets | Chromium Fehler"  
[CR955497]: https://crbug.com/955497 "Kontextmenü für App-Symbole für PWAs | Chromium Fehler"  
[CR974550]: https://crbug.com/974550 "Metrikkonflikt zwischen Perf-Bereich und performanceObserver-| Chromium Fehler"  
[CR1041830]: https://crbug.com/1041830 "Verbessern von Farben für Haltepunkte | Chromium Fehler"  
[CR1055875]: https://crbug.com/1055875 "Der Wert der Konsoleneinstellung &quot;Ausgewählter Kontext&quot; bleibt nach dem Schließen und erneuten Öffnen der Entwicklertools | Chromium Fehler"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Show ServiceWorkers Fetch Timeline per request in Network panel | Chromium Fehler"  
[CR1071432]: https://crbug.com/1071432 "Wasm Basic Developer Experience | Chromium Fehler"  
[CR1073899]: https://crbug.com/1073899 "Registerkarte für berechnete Stile wird im reaktionsfähigen Modus nicht mehr angezeigt | Chromium Fehler"  
[CR1073903]: https://crbug.com/1073903 "DevTools: Die Syntaxhervorhebung funktioniert bei privaten Feldern nicht | Chromium Fehler"  
[CR1082963]: https://crbug.com/1082963 "Gruppenähnliches Nachrichtenverhalten der Konsole kann nicht deaktiviert werden | Chromium Fehler"  
[CR1083214]: https://crbug.com/1083214 "Acorn unterstützt keine optionale Verkettung | Chromium Fehler"  
[CR1083797]: https://crbug.com/1083797 "Ziemlicher Druck für Null-Koalescing | Chromium Fehler"  
[CR1096008]: https://crbug.com/1096008 "Entfernen von FMP-| Chromium Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Chromium Fehler"  
[CR1093687]: https://crbug.com/1093687 "Erstellungstool zum Erstellen und Wiedergeben synthetischer Netzwerkanforderungen | Chromium Fehler"  
[CR1070378]: https://crbug.com/1070378 "Integrieren von Webhint in DevTools | Chromium Fehler"  
[CR1069404]: https://crbug.com/1069404 "[Dev Tools] Widget-Popups sind zu eng | Chromium Fehler"  
[CR897944]: https://crbug.com/897944 "Dragable devtool panels | Chromium Fehler"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v6.0.0 – GoogleChrome/- | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Neues Problem – MicrosoftDocs/Edge-Entwickler"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Verwenden von Schatten-DOM-| Mdn"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Microsoft Edge-Vorschaukanäle"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"
[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "CSSOM-| W3C-CSS-Arbeitsgruppen-Editor-Entwürfe"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Posten eines Tweets"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools, Twitter-Konto"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Private Klassenfelder – Öffentliche und private Klassenfelder | V8. Dev"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Zwischenspeichern von Code für JavaScript-Entwickler | V8. Dev"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Null-Koalescing | V8. Dev"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Optionale verkettete | V8. Dev"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Constructable Stylesheet-Objekte | Web-Eningen CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "The Web We Want"  

> [!NOTE]
> <span data-ttu-id="71ad9-319">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71ad9-319">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="71ad9-320">Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-85) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="71ad9-320">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-85) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="71ad9-322">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="71ad9-322">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
