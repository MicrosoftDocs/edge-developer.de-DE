---
description: Microsoft Edge unter Linux, verbesserte Webhint-Tipps im Probleme-Tool, neue Features für das Service Worker-Debugging und vieles mehr.
title: Neuerungen in DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.localizationpriority: high
ms.openlocfilehash: e5706de4c7938a3cb2246aa34de07c73dafe5776
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624773"
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
# <a name="whats-new-in-devtools-microsoft-edge-88"></a><span data-ttu-id="39c2c-104">Neuerungen in DevTools (Microsoft Edge 88)</span><span class="sxs-lookup"><span data-stu-id="39c2c-104">What's New in DevTools (Microsoft Edge 88)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="microsoft-edge-and-microsoft-edge-driver-now-available-on-linux"></a><span data-ttu-id="39c2c-105">Microsoft Edge und Microsoft Edge-Treiber jetzt unter Linux verfügbar</span><span class="sxs-lookup"><span data-stu-id="39c2c-105">Microsoft Edge and Microsoft Edge Driver now available on Linux</span></span>  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

<span data-ttu-id="39c2c-106">Microsoft Edge Dev wird nun von Ubuntu-, Debian-, Fedora- und openSUSE-Distributionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-106">Microsoft Edge Dev is now supported on Ubuntu, Debian, Fedora, and openSUSE distributions.</span></span>  <span data-ttu-id="39c2c-107">Laden Sie das Microsoft Edge Dev `.deb`- oder `.rpm`-Paket direkt von der [Microsoft Edge Insider-Website][MicrosoftinsiderDownloadPlatformLinux] herunter und installieren Sie es, oder verwenden Sie die standardmäßigen Paketverwaltungstools Ihrer Linux-Distribution.</span><span class="sxs-lookup"><span data-stu-id="39c2c-107">Download and install the Microsoft Edge Dev `.deb` or `.rpm` package directly from the [Microsoft Edge Insider site][MicrosoftinsiderDownloadPlatformLinux] or use the standard package management tools of your Linux distribution.</span></span>  

<span data-ttu-id="39c2c-108">Wenn Sie eine Linux-Umgebung in Ihren Continuous Integration und Continuous Delivery \(CI/CD\)-Lösungen verwenden, ist Microsoft Edge Driver auch unter Linux verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39c2c-108">If you are using a Linux environment in your continuous integration and delivery \(CI/CD\) solutions, Microsoft Edge Driver is also available on Linux.</span></span>  <span data-ttu-id="39c2c-109">Wenn Sie mit der Automatisierung von Microsoft Edge Dev mit Microsoft Edge Driver beginnen möchten, navigieren Sie zur [Downloadseite für Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="39c2c-109">To get started automating Microsoft Edge Dev with Microsoft Edge Driver, navigate to [Microsoft Edge Driver Downloads page][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="39c2c-110">Hilfe zur Automatisierung von Microsoft Edge Dev zusammen mit Microsoft Edge Driver finden Sie unter [Verwenden von WebDriver (Chromium) für die Testautomatisierung][WebdriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="39c2c-110">For help with automating Microsoft Edge Dev along with Microsoft Edge Driver, navigate to [Use WebDriver (Chromium) for test automation][WebdriverChromiumMain].</span></span>  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools in Microsoft Edge unter Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   <span data-ttu-id="39c2c-112">DevTools in Microsoft Edge unter Linux</span><span class="sxs-lookup"><span data-stu-id="39c2c-112">DevTools in Microsoft Edge on Linux</span></span>  
:::image-end:::  

## <a name="improved-webhint-and-platform-tips-in-the-issues-tool"></a><span data-ttu-id="39c2c-113">Verbesserte Webhint- und Plattformtipps im Probleme-Tool</span><span class="sxs-lookup"><span data-stu-id="39c2c-113">Improved webhint and platform tips in the Issues tool</span></span>  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

<span data-ttu-id="39c2c-114">Ein Open-Source-Tool, [Webhint][WebhintMain], bietet Echtzeitfeedback für Websites und lokale Webseiten.</span><span class="sxs-lookup"><span data-stu-id="39c2c-114">An open-source tool, [webhint][WebhintMain], provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="39c2c-115">Überprüfen Sie ab [Microsoft Edge Version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel] das Webhint-Feedback im [Issues][DevtoolsIssuesIndex]-Tool.</span><span class="sxs-lookup"><span data-stu-id="39c2c-115">Starting with [Microsoft Edge version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], review webhint feedback in the [Issues][DevtoolsIssuesIndex] tool.</span></span>  <span data-ttu-id="39c2c-116">Probleme, die im **Probleme**-Tool angezeigt werden, sind jetzt mit den folgenden, neu hinzugefügten Kategorien leichter zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-116">Issues that appear in the **Issues** tool are now easier to review with the addition of the following categories.</span></span>  

*   [<span data-ttu-id="39c2c-117">Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="39c2c-117">Accessibility</span></span>][WebhintUserGuideHintsAccessibility]  
*   [<span data-ttu-id="39c2c-118">Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="39c2c-118">Compatibility</span></span>][WebhintUserGuideHintsCompatibility]  
*   [<span data-ttu-id="39c2c-119">Leistung</span><span class="sxs-lookup"><span data-stu-id="39c2c-119">Performance</span></span>][WebhintUserGuideHintsPerformance]  
*   [<span data-ttu-id="39c2c-120">Fallstricke</span><span class="sxs-lookup"><span data-stu-id="39c2c-120">Pitfalls</span></span>][WebhintUserGuideHintsPitfalls]  
*   [<span data-ttu-id="39c2c-121">PWA</span><span class="sxs-lookup"><span data-stu-id="39c2c-121">PWA</span></span>][WebhintUserGuideHintsPwa]  
*   [<span data-ttu-id="39c2c-122">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="39c2c-122">Security</span></span>][WebhintUserGuideHintsSecurity]  
    
<span data-ttu-id="39c2c-123">Sie können jetzt die Probleme von Drittanbietern mithilfe eines neuen Kontrollkästchens herausfiltern.</span><span class="sxs-lookup"><span data-stu-id="39c2c-123">You are now able to filter out third-party issues using a new checkbox.</span></span>  <span data-ttu-id="39c2c-124">Die Filterfunktionalität hilft Ihnen, Probleme im Zusammenhang mit Code aus Drittanbieterbibliotheken oder anderen Quellen auszublenden.</span><span class="sxs-lookup"><span data-stu-id="39c2c-124">The filter functionality helps you hide issues related to code from third-party libraries or other sources.</span></span>  

<span data-ttu-id="39c2c-125">Zur leichteren Überprüfung der von [webhint][WebhintMain] aufgedeckten Probleme werden im **Probleme**-Tool nun die folgenden Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-125">To help you review issues revealed by [webhint][WebhintMain], the **Issues** tool now displays the following information.</span></span>  

*   <span data-ttu-id="39c2c-126">Verbesserte Codeausschnitte.</span><span class="sxs-lookup"><span data-stu-id="39c2c-126">Improved code snippets.</span></span>  
*   <span data-ttu-id="39c2c-127">Links zu anderen relevanten Panels.</span><span class="sxs-lookup"><span data-stu-id="39c2c-127">Links to other relevant panels.</span></span>  
*   <span data-ttu-id="39c2c-128">Links zur Dokumentation, die Ihnen bei der Behebung von Problemen in Ihrer Website helfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-128">Links to documentation to help you fix problems in your website.</span></span>  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Probleme-Tool" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   <span data-ttu-id="39c2c-130">**Probleme**-Tool</span><span class="sxs-lookup"><span data-stu-id="39c2c-130">**Issues** tool</span></span>  
:::image-end:::  

## <a name="composited-layers-are-now-in-3d-view"></a><span data-ttu-id="39c2c-131">Zusammengesetzte Ebenen werden jetzt in der 3D-Ansicht dargestellt</span><span class="sxs-lookup"><span data-stu-id="39c2c-131">Composited Layers are now in 3D View</span></span>  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="39c2c-132">Sie können nun Inhalte von **Ebenen** neben Z-Indexwerten und dem Dokumentobjektmodell \(DOM\) visualisieren.</span><span class="sxs-lookup"><span data-stu-id="39c2c-132">You may now visualize **Layers** content alongside z-index values and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="39c2c-133">Mit diesem Feature können Sie Debuggen, ohne zwischen den Tools [3D-Ansicht][Devtools3dViewIndex] und **Ebenen** umzuschalten.</span><span class="sxs-lookup"><span data-stu-id="39c2c-133">This feature helps you debug without switching between the [3D view][Devtools3dViewIndex] and **Layers** tools as often.</span></span>  <span data-ttu-id="39c2c-134">Für ein umfassendes visuelles Debugging werden jetzt [die 3D-Ansicht und die zusammengesetzten Ebenen kombiniert][Devtools3dViewIndex].</span><span class="sxs-lookup"><span data-stu-id="39c2c-134">For a comprehensive visual debugging experience, the [3D View and Composited Layers are now combined][Devtools3dViewIndex].</span></span>  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Bereich Zusammengesetzte Ebenen" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   <span data-ttu-id="39c2c-136">Bereich **Zusammengesetzte Ebenen**</span><span class="sxs-lookup"><span data-stu-id="39c2c-136">**Composited Layers** pane</span></span>  
:::image-end:::  

## <a name="css-variable-definitions-in-styles-pane"></a><span data-ttu-id="39c2c-137">CSS-Variablendefinitionen im Bereich „Stile“</span><span class="sxs-lookup"><span data-stu-id="39c2c-137">CSS variable definitions in Styles pane</span></span>  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

<span data-ttu-id="39c2c-138">Im Bereich **Stile** werden die [CSS-Variablen][MdnUsingCssCustomProperties] nun direkt mit jeder Definition verknüpft.</span><span class="sxs-lookup"><span data-stu-id="39c2c-138">In the **Styles** pane, [CSS variables][MdnUsingCssCustomProperties] now link directly to each definition.</span></span>  <span data-ttu-id="39c2c-139">Wählen Sie eine Variable aus, um die Definition der CSS-Variablen einfach anzuzeigen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="39c2c-139">Choose the variable to easily view or change the CSS variable definition.</span></span>  <span data-ttu-id="39c2c-140">Im Beispiel zeigt DevTools die CSS-Attribute für das `body`-Element an.</span><span class="sxs-lookup"><span data-stu-id="39c2c-140">In the example, DevTools displays the CSS attributes for the `body` element.</span></span>  <span data-ttu-id="39c2c-141">Führen Sie die folgenden Aktionen aus, um die Variablendefinition für die CSS-Variable `--theme-body-background` anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-141">To display the variable definition for the `--theme-body-background` CSS variable, complete the following actions.</span></span>  

1.  <span data-ttu-id="39c2c-142">Wählen Sie im Bereich **Stile** `var(--theme-body-background)` aus.</span><span class="sxs-lookup"><span data-stu-id="39c2c-142">In the **Styles** pane, choose `var(--theme-body-background)`.</span></span>  
1.  <span data-ttu-id="39c2c-143">Im Bereich **Stile** wird nun die Definition der CSS-Variablen `--theme-body-background` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-143">The **Styles** pane now displays the definition of the `--theme-body-background` CSS variable.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Mit dem Stil verknüpfte CSS-Variable" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         <span data-ttu-id="39c2c-145">Mit dem Stil verknüpfte CSS-Variable</span><span class="sxs-lookup"><span data-stu-id="39c2c-145">CSS variable linked to the style</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Mit dem Stilziel verknüpfte CSS-Variable" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         <span data-ttu-id="39c2c-147">Mit dem Stilziel verknüpfte CSS-Variable</span><span class="sxs-lookup"><span data-stu-id="39c2c-147">CSS variable linked to style target</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="service-worker-debugging-improvements"></a><span data-ttu-id="39c2c-148">Verbesserungen beim Service Worker-Debugging</span><span class="sxs-lookup"><span data-stu-id="39c2c-148">Service worker debugging improvements</span></span>  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

<span data-ttu-id="39c2c-149">Die folgenden neuen Features in den Tools [Netzwerk](#network-tool), [Anwendung](#application-tool) und [Quellen](#sources-tool) unterstützen Sie beim Erstellen Ihrer [PWA][ProgressiveWebAppsIndex].</span><span class="sxs-lookup"><span data-stu-id="39c2c-149">The following new features in the [Network](#network-tool), [Application](#application-tool), and [Sources](#sources-tool) tools help you build your [PWA][ProgressiveWebAppsIndex].</span></span>  <span data-ttu-id="39c2c-150">Verwenden Sie die folgenden Features, wenn Probleme beim Debuggen Ihrer Service Worker auftreten.</span><span class="sxs-lookup"><span data-stu-id="39c2c-150">Use the following features when you have difficulty debugging your service worker.</span></span>  

<span data-ttu-id="39c2c-151">Das Routing von Anforderungen zeigt die `startup`- und `fetch`-Ereignisse basierend auf den Netzwerkanforderungen an, die von Service Workern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="39c2c-151">Request routing displays the `startup` and `fetch` events based on the network requests that run through service workers.</span></span>  <span data-ttu-id="39c2c-152">Der Zugriff auf die Zeitpläne erfolgt entweder über das **Anwendung**- oder das **Netzwerk**-Tool.</span><span class="sxs-lookup"><span data-stu-id="39c2c-152">The timelines are accessed from either the **Application** or **Network** tool.</span></span>  <span data-ttu-id="39c2c-153">Die Zeitpläne helfen, wenn Sie Probleme mit Service Workers haben und anzeigen möchten, ob etwas mit dem Ereignis `startup` oder `fetch` nicht stimmt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-153">The timelines help when you are having trouble with service workers and want to display if something is wrong with the `startup` or `fetch` event.</span></span>  

### <a name="application-tool"></a><span data-ttu-id="39c2c-154">Anwendung-Tool</span><span class="sxs-lookup"><span data-stu-id="39c2c-154">Application tool</span></span>  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

<span data-ttu-id="39c2c-155">Zeigen Sie mit dem neuen Link **Netzwerkanforderungen** alle Routinginformationen für Service Worker-Anforderungen an.</span><span class="sxs-lookup"><span data-stu-id="39c2c-155">View all service worker request routing information with the new **Network requests** link.</span></span>  <span data-ttu-id="39c2c-156">Führen Sie die folgenden Aktionen aus, um beim Debuggen des Service Workers zusätzlichen Kontext anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-156">To display additional context when debugging the service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="39c2c-157">Navigieren Sie zu **Anwendung** > **Service Workers**.</span><span class="sxs-lookup"><span data-stu-id="39c2c-157">Navigate to **Application** > **Service Workers**.</span></span>  
1.  <span data-ttu-id="39c2c-158">Wählen Sie **Netzwerkanforderungen** aus.</span><span class="sxs-lookup"><span data-stu-id="39c2c-158">Choose **Network requests**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Öffnen des Netzwerk-Tools im Bereich Service Workers" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       <span data-ttu-id="39c2c-160">Öffnen des **Netzwerk**-Tools im Bereich **Service Workers**</span><span class="sxs-lookup"><span data-stu-id="39c2c-160">Open **Network** tool from the **Service Workers** pane</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="39c2c-161">Das **Netzwerk**-Tool wird in der **Schublade** geöffnet und zeigt alle Netzwerkanforderungen für Service Worker an.</span><span class="sxs-lookup"><span data-stu-id="39c2c-161">The **Network** tool opens in the **drawer** and displays all service worker-related network requests.</span></span>  <span data-ttu-id="39c2c-162">Die Netzwerkanforderungen werden mithilfe von `is:service-worker-intercepted` gefiltert.</span><span class="sxs-lookup"><span data-stu-id="39c2c-162">The network requests are filtered using `is:service-worker-intercepted`.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Netzwerk-Tool in der Schublade" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       <span data-ttu-id="39c2c-164">**Netzwerk**-Tool in der **Schublade**</span><span class="sxs-lookup"><span data-stu-id="39c2c-164">**Network** tool in **drawer**</span></span>  
    :::image-end:::
    
1. <span data-ttu-id="39c2c-165">Wenn Sie das **Netzwerk**-Tool wieder in den oberen Bereich verschieben möchten, schließen Sie die **Schublade**.</span><span class="sxs-lookup"><span data-stu-id="39c2c-165">To return the **Network** tool to the top panel, close the **drawer**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Schließen der Schublade, um das Network-Tool zurückzugeben" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       <span data-ttu-id="39c2c-167">Schließen der **Schublade**, um das **Netzwerk**-Tool zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="39c2c-167">Close the **drawer** to return **Network** tool</span></span>  
    :::image-end:::  
    
### <a name="network-tool"></a><span data-ttu-id="39c2c-168">Network-Tool</span><span class="sxs-lookup"><span data-stu-id="39c2c-168">Network tool</span></span>  

<span data-ttu-id="39c2c-169">Debuggen Sie Netzwerkanforderungen, die über Service Worker ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="39c2c-169">Debug network requests that run through service workers.</span></span>  <span data-ttu-id="39c2c-170">Sie können Netzwerkanforderungen auch über das **Anwendung**-Tool öffnen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-170">You may also open network requests from the **Application** tool.</span></span>  <span data-ttu-id="39c2c-171">DevTools zeigen für jede Anforderung die folgenden Informationen im [Timing] [DevtoolsNetworkReferenceDisplayTimingBreakdownRequest]-Bereich an.</span><span class="sxs-lookup"><span data-stu-id="39c2c-171">For each request, DevTools display the following information in the [Timing][DevtoolsNetworkReferenceDisplayTimingBreakdownRequest] pane.</span></span>  

*   <span data-ttu-id="39c2c-172">Der Anfang einer Anforderung und die Dauer des Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="39c2c-172">The start of a request and duration of the bootstrap.</span></span>  
*   <span data-ttu-id="39c2c-173">Änderungen an der Service Worker-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="39c2c-173">Changes to service worker registration.</span></span>  
*   <span data-ttu-id="39c2c-174">Die Laufzeit eines `fetch`-Ereignishandlers.</span><span class="sxs-lookup"><span data-stu-id="39c2c-174">The runtime of a `fetch` event handler.</span></span>  
*   <span data-ttu-id="39c2c-175">Die Laufzeit aller `fetch`-Ereignisse zum Laden eines Clients.</span><span class="sxs-lookup"><span data-stu-id="39c2c-175">The runtime of all `fetch` events for loading a client.</span></span>  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Bereich Timing" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   <span data-ttu-id="39c2c-177">Bereich **Timing**</span><span class="sxs-lookup"><span data-stu-id="39c2c-177">**Timing** pane</span></span>  
:::image-end:::  

### <a name="sources-tool"></a><span data-ttu-id="39c2c-178">Quellen-Tool</span><span class="sxs-lookup"><span data-stu-id="39c2c-178">Sources tool</span></span>  

<span data-ttu-id="39c2c-179">In früheren Versionen von Microsoft Edge war die Tiefe im Aufrufstapel auf den JavaScript-Code in Ihrem Service Worker beschränkt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-179">In previous versions of Microsoft Edge, the level of depth in the call stack was limited to the JavaScript code in your service worker.</span></span>  <span data-ttu-id="39c2c-180">In Microsoft Edge 88 zeigt der Aufrufstapel nun den Initiator von Anforderungen an, die über Ihren Service Worker ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="39c2c-180">In Microsoft Edge 88, the call stack now displays the initiator of requests that run through your service worker.</span></span>  

<span data-ttu-id="39c2c-181">Zum Auffinden des Initiators der Anforderung verwenden Sie den Aufrufstapel Ihres JavaScript-Codes im Service Worker.</span><span class="sxs-lookup"><span data-stu-id="39c2c-181">To locate the initiator of the request, use the call stack of your JavaScript code in the service worker.</span></span>  <span data-ttu-id="39c2c-182">Der Aufrufstapel in den folgenden Abbildungen beginnt mit dem JavaScript-Code in Ihrem Service Worker und zeigt einen Verweis auf die ursprüngliche Webseitenanforderung als `(index):157` an.</span><span class="sxs-lookup"><span data-stu-id="39c2c-182">The call stack in the following figures starts with the JavaScript code in your service worker and displays a reference to the original webpage request as `(index):157`.</span></span>  <span data-ttu-id="39c2c-183">In der zweiten Abbildung wurde der Verweis ausgewählt und hat den Initiator geöffnet, der die Anforderung gestellt hat.</span><span class="sxs-lookup"><span data-stu-id="39c2c-183">In the second figure, the reference is chosen and opened the initiator that made the request.</span></span>  <span data-ttu-id="39c2c-184">Der Initiator in der zweiten Abbildung ist die Webseite.</span><span class="sxs-lookup"><span data-stu-id="39c2c-184">The initiator in the second figure is the webpage.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Datei service-worker.js und Aufrufstapel mit Hervorhebung des Ursprungs der Anforderung" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         <span data-ttu-id="39c2c-186">Datei `service-worker.js` und Aufrufstapel mit Hervorhebung des Ursprungs der Anforderung</span><span class="sxs-lookup"><span data-stu-id="39c2c-186">The `service-worker.js` file and call stack highlighting request originator</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="Die (Index-)Webseite ist der Anforderungsinitiator" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         <span data-ttu-id="39c2c-188">Die Webseite `(index)` ist der Initiator der Anforderung</span><span class="sxs-lookup"><span data-stu-id="39c2c-188">The `(index)` webpage is the request initiator</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="copy-property-value-of-a-network-request"></a><span data-ttu-id="39c2c-189">Kopieren des Eigenschaftswerts einer Netzwerkanforderung</span><span class="sxs-lookup"><span data-stu-id="39c2c-189">Copy property value of a network request</span></span>  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

<span data-ttu-id="39c2c-190">Im Tool **Netzwerk** können Sie den Eigenschaftswert einer Netzwerkanforderung mit der neuen Option **Wert kopieren** kopieren.</span><span class="sxs-lookup"><span data-stu-id="39c2c-190">In the **Network** tool, copy the property value of a network request using the new **Copy value** option.</span></span>  <span data-ttu-id="39c2c-191">Der Eigenschaftswert wird als decodierter JSON-Wert kopiert.</span><span class="sxs-lookup"><span data-stu-id="39c2c-191">The property value is copied as a decoded JSON value.</span></span>  <span data-ttu-id="39c2c-192">In früheren Versionen von Microsoft Edge mussten Sie einen Wert mithilfe einer der folgenden Aktionen kopieren.</span><span class="sxs-lookup"><span data-stu-id="39c2c-192">In previous versions of Microsoft Edge, you had to copy a value using one of the following actions.</span></span>  

*   <span data-ttu-id="39c2c-193">Hervorheben des gesamten Texts und Kopieren.</span><span class="sxs-lookup"><span data-stu-id="39c2c-193">Highlight the entire text and copy it.</span></span>  
*   <span data-ttu-id="39c2c-194">Speichern des Werts als globale Variable (sofern zutreffend) und Kopieren des Werts in der DevTools-[Konsole][DevtoolsConsoleIndex].</span><span class="sxs-lookup"><span data-stu-id="39c2c-194">Store the value as global variable, as applicable, and copy it from the DevTools [Console][DevtoolsConsoleIndex].</span></span>  
    
<span data-ttu-id="39c2c-195">Navigieren Sie zum Kopieren des Eigenschaftswerts in die Zwischenablage zu [Formatierte Antwort JSON in die Zwischenablage kopieren][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span><span class="sxs-lookup"><span data-stu-id="39c2c-195">To copy the property value to your clipboard, navigate to [Copy formatted response JSON to the clipboard][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span></span>  <span data-ttu-id="39c2c-196">Navigieren Sie zu Problem [1132084][CR1132084], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1132084][CR1132084].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Kopieren eines Eigenschaftswerts in DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         <span data-ttu-id="39c2c-198">Kopieren eines Eigenschaftswerts in DevTools</span><span class="sxs-lookup"><span data-stu-id="39c2c-198">Copy property value in DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Einfügen eines Eigenschaftswerts in Microsoft Visual Studio Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         <span data-ttu-id="39c2c-200">Einfügen eines Eigenschaftswerts in Microsoft Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="39c2c-200">Paste property value in Microsoft Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="customize-multi-press-keyboard-shortcuts"></a><span data-ttu-id="39c2c-201">Anpassen von mehrfach gedrückten Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="39c2c-201">Customize multi-press keyboard shortcuts</span></span>  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="39c2c-202">[Seit Microsoft Edge, Version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], können Sie Tastenkombinationen für jede Aktion in DevTools anpassen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-202">[Since Microsoft Edge version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], you may customize keyboard shortcuts for any action in DevTools.</span></span>  <span data-ttu-id="39c2c-203">In Microsoft Edge, Version 88, können Sie jetzt Multipress-Tastenkombinationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-203">In Microsoft Edge version 88, you may now create multi-press keyboard shortcuts.</span></span>  <span data-ttu-id="39c2c-204">Wenn Sie eine Tastenkombination für eine Aktion in DevTools festlegen möchten, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings] > **Experimente**, und aktivieren Sie das Kontrollkästchen neben **Tastenkombinations-Editor aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="39c2c-204">To set a shortcut for an action in the DevTools, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="39c2c-205">Weitere Informationen zum Anpassen und Bearbeiten von Verknüpfungen finden Sie unter [Bearbeiten von Tastenkombinationen für alle Aktionen in devTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].</span><span class="sxs-lookup"><span data-stu-id="39c2c-205">For more information about customizing and editing shortcuts, navigate to [Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].</span></span>  

<span data-ttu-id="39c2c-206">Die rote Markierung zeigt beispielsweise eine angepasste Multipress-Tastenkombination für die Aktion **Aufzeichnen von Ereignissen starten** an.</span><span class="sxs-lookup"><span data-stu-id="39c2c-206">For example, the red highlight displays a multi-press keyboard shortcut customized for the **Start recording events** action.</span></span>  <span data-ttu-id="39c2c-207">Navigieren Sie zu [Problem #174309][CR174309], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-207">To review real-time updates on this feature in the Chromium open-source project, navigate to [Issue #174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Akkord-Tastenkombinationen" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   <span data-ttu-id="39c2c-209">Multipress-Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="39c2c-209">Multi-press keyboard shortcuts</span></span>  
:::image-end:::  

## <a name="devtools-now-match-browser-language"></a><span data-ttu-id="39c2c-210">DevTools-Sprache entspricht nun der Browsersprache</span><span class="sxs-lookup"><span data-stu-id="39c2c-210">DevTools now match browser language</span></span>  

<span data-ttu-id="39c2c-211">Wenn Sie in Microsoft Edge, Version 87, in den [DevTools-Einstellungen][DevtoolsCustomizeIndexSettings] die Einstellung **Übereinstimmung mit der Browser-Sprache** aktiviert haben, entsprach die Sprache von DevTools nicht der Browsersprache.</span><span class="sxs-lookup"><span data-stu-id="39c2c-211">In Microsoft Edge version 87, if you turned on the **Match browser language** setting in [DevTools Settings][DevtoolsCustomizeIndexSettings], DevTools did not match the browser language.</span></span>  <span data-ttu-id="39c2c-212">In Microsoft Edge, Version 88, entspricht DevTools nun der Browsersprache, wenn Sie die Einstellung **Übereinstimmung mit der Browsersprache** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="39c2c-212">In Microsoft Edge version 88, DevTools now matches the browser language if you turn on the **Match browser language** setting.</span></span>  <span data-ttu-id="39c2c-213">Weitere Informationen zur DevTools-Einstellung **Übereinstimmung mit der Browsersprache** erhalten Sie, wenn Sie zu [Ändern der DevTools-Spracheinstellungen][DevtoolsCustomizeLocalization] navigieren.</span><span class="sxs-lookup"><span data-stu-id="39c2c-213">For more information about the **Match browser language** DevTools Setting, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  

:::image type="complex" source="../../media/2020/11/startpage-devtools-settings-japanese.msft.png" alt-text="DevTools-Einstellung Übereinstimmung mit der Browsersprache in Japanisch" lightbox="../../media/2020/11/startpage-devtools-settings-japanese.msft.png":::
   <span data-ttu-id="39c2c-215">DevTools-Einstellung **Übereinstimmung mit der Browsersprache** in Japanisch</span><span class="sxs-lookup"><span data-stu-id="39c2c-215">**Match browser language** DevTools setting in Japanese</span></span>  
:::image-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="39c2c-216">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="39c2c-216">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-css-angle-visualization-tools"></a><span data-ttu-id="39c2c-217">Neue Visualisierungstools für CSS-Winkel</span><span class="sxs-lookup"><span data-stu-id="39c2c-217">New CSS angle visualization tools</span></span>  

<span data-ttu-id="39c2c-218">DevTools unterstützt jetzt das Debuggen von CSS-Winkeln besser.</span><span class="sxs-lookup"><span data-stu-id="39c2c-218">DevTools now have better support for CSS angle debugging.</span></span>  <span data-ttu-id="39c2c-219">Wenn auf ein HTML-Element auf Ihrer Seite ein CSS-Winkel angewendet wurde, wird neben dem Winkel im **Stile**-Tool ein Uhrensymbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-219">When an HTML element on your page has CSS angle applied to it, a clock icon is displayed next to the angle in the **Styles** tool.</span></span>  <span data-ttu-id="39c2c-220">Wenn Sie die Uhr-Überlagerung ein-/ausschalten möchten, wählen Sie das Uhrensymbol aus.</span><span class="sxs-lookup"><span data-stu-id="39c2c-220">To toggle the clock overlay, choose the clock icon.</span></span>  <span data-ttu-id="39c2c-221">Wenn Sie den Winkel ändern möchten, wählen Sie eine beliebige Stelle in der Uhr aus, oder ziehen Sie am Zeiger.</span><span class="sxs-lookup"><span data-stu-id="39c2c-221">To change the angle, choose anywhere in the clock or drag the needle.</span></span>  <span data-ttu-id="39c2c-222">Zum Ändern des Winkelwerts können Sie auch Mausverfahren und Tastenkombinationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="39c2c-222">To change the angle value, you may also use mouse and keyboard shortcuts.</span></span>  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  <span data-ttu-id="39c2c-223">Navigieren Sie zu den Problemen [1126178][CR1126178] und [1138633][CR1138633], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-223">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1126178][CR1126178] and [1138633][CR1138633].</span></span>  

<!--todo:  add link when css angle clock section exists.  -->  

<span data-ttu-id="39c2c-224">Für das Beispiel wird der folgende CSS-Winkel verwendet.</span><span class="sxs-lookup"><span data-stu-id="39c2c-224">The following CSS angle is used for the example.</span></span>  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="CSS-Winkel" lightbox="../../media/2020/11/css-angle.msft.png":::
   <span data-ttu-id="39c2c-226">CSS-Winkel</span><span class="sxs-lookup"><span data-stu-id="39c2c-226">CSS angle</span></span>  
:::image-end:::  

### <a name="simulate-storage-quota-size-in-the-storage-pane"></a><span data-ttu-id="39c2c-227">Simulieren der Speicherkontingentgröße im Speicherbereich</span><span class="sxs-lookup"><span data-stu-id="39c2c-227">Simulate storage quota size in the Storage pane</span></span>  

<span data-ttu-id="39c2c-228">Sie können jetzt die Größe des Speicherkontingents im Bereich **Speicher** außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-228">You may now override storage quota size in the **Storage** pane.</span></span>  <span data-ttu-id="39c2c-229">Dieses Feature ermöglicht es Ihnen, verschiedene Geräte zu simulieren und das Verhalten Ihrer Website oder App in Szenarien mit wenig verfügbarem Speicherplatz zu testen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-229">This feature allows you to simulate different devices and test the behavior of your website or app in low disk availability scenarios.</span></span>  <span data-ttu-id="39c2c-230">Führen Sie die folgenden Aktionen aus, um das Speicherkontingent zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="39c2c-230">To simulate the storage quota, complete the following actions.</span></span>  

1.  <span data-ttu-id="39c2c-231">Navigieren Sie zu **Anwendung** > **Speicher**.</span><span class="sxs-lookup"><span data-stu-id="39c2c-231">Navigate to **Application** > **Storage**.</span></span>  
1.  <span data-ttu-id="39c2c-232">Aktivieren Sie das Kontrollkästchen **Benutzerdefiniertes Speicherkontingent simulieren**.</span><span class="sxs-lookup"><span data-stu-id="39c2c-232">Turn on the **Simulate custom storage quota** checkbox.</span></span>  
1.  <span data-ttu-id="39c2c-233">Geben Sie eine gültige Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="39c2c-233">Enter a valid number.</span></span>  
    
<span data-ttu-id="39c2c-234">Weitere Informationen zum Emulieren von mobilen Geräten und anderen Features in DevTools finden Sie unter [Emulieren von mobilen Geräten in Microsoft Edge DevTools][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="39c2c-234">For more information about how to emulate mobile devices and other features in the DevTools, navigate to [Emulate mobile devices in Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span></span>  <span data-ttu-id="39c2c-235">Navigieren Sie zu den Problemen [945786][CR945786] und [1146985][CR1146985], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-235">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [945786][CR945786] and [1146985][CR1146985].</span></span>  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simulieren der Speicherkontingentgröße" lightbox="../../media/2020/11/storage-quota.msft.png":::
   <span data-ttu-id="39c2c-237">Simulieren der Speicherkontingentgröße</span><span class="sxs-lookup"><span data-stu-id="39c2c-237">Simulate storage quota size</span></span>  
:::image-end:::  

### <a name="report-cors-errors-in-the-network-tool"></a><span data-ttu-id="39c2c-238">Melden von CORS-Fehlern im Netzwerk-Tool</span><span class="sxs-lookup"><span data-stu-id="39c2c-238">Report CORS errors in the Network tool</span></span>  

<span data-ttu-id="39c2c-239">Testen Sie dieses Feature, indem Sie zur [CORS-Fehlerdemo][GlitchCorsErrors] navigieren.</span><span class="sxs-lookup"><span data-stu-id="39c2c-239">Try out this feature by navigating to [CORS error demo][GlitchCorsErrors].</span></span>  <span data-ttu-id="39c2c-240">Öffnen Sie das Tool **Netzwerk**, aktualisieren Sie die Seite, und beobachten Sie die fehlerhafte CORS-Netzwerkanforderung.</span><span class="sxs-lookup"><span data-stu-id="39c2c-240">Open the **Network** tool, refresh the page, and observe the failed CORS network request.</span></span>  <span data-ttu-id="39c2c-241">In der Statusspalte wird der **CORS-Fehler** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-241">The status column displays the **CORS error**.</span></span>  <span data-ttu-id="39c2c-242">Wenn Sie auf den Fehler zeigen, wird in der QuickInfo nun der Fehlercode angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-242">When you hover on the error, the tooltip now displays the error code.</span></span>  <span data-ttu-id="39c2c-243">In Microsoft Edge, Version 87 und früheren Versionen, hat DevTools nur den generischen **(failed)**-Status für CORS-Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-243">In Microsoft Edge version 87 and earlier, DevTools only displayed generic **(failed)** status for CORS errors.</span></span>  <span data-ttu-id="39c2c-244">Navigieren Sie zu Problem [1141824][CR1141824], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="CORS-Fehler" lightbox="../../media/2020/11/cors-err.msft.png":::
   <span data-ttu-id="39c2c-246">CORS-Fehler</span><span class="sxs-lookup"><span data-stu-id="39c2c-246">CORS errors</span></span>  
:::image-end:::  

### <a name="frame-details-view-updates"></a><span data-ttu-id="39c2c-247">Updates der Frame-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="39c2c-247">Frame details view updates</span></span>  

#### <a name="cross-origin-isolation-information-in-the-frame-details-view"></a><span data-ttu-id="39c2c-248">Informationen zur ursprungsübergreifenden Isolierung in der Frame-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="39c2c-248">Cross-origin isolation information in the Frame details view</span></span>  

<span data-ttu-id="39c2c-249">Der Status ursprungsübergreifend isoliert (cross-origin isolated) wird nun unter dem Abschnitt **Sicherheit & Isolierung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-249">The cross-origin isolated status is now displayed under the **Security & Isolation** section.</span></span>  <span data-ttu-id="39c2c-250">Der neue Abschnitt **API-Verfügbarkeit** zeigt die Verfügbarkeit von `SharedArrayBuffer`s \(SAB\) und ob die Puffer mit `postMessage()` freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="39c2c-250">The new **API availability** section displays the availability of `SharedArrayBuffer`s \(SAB\) and whether the buffers may be shared using `postMessage()`.</span></span>  <span data-ttu-id="39c2c-251">Eine Warnung „veraltet“ wird angezeigt, wenn der SAB und `postMessage()` derzeit verfügbar sind, der Kontext aber nicht ursprungsübergreifend isoliert ist.</span><span class="sxs-lookup"><span data-stu-id="39c2c-251">A deprecation warning displays if the SAB and `postMessage()` is currently available, but the context is not cross-origin isolated.</span></span>  <span data-ttu-id="39c2c-252">Weitere Informationen zur ursprungsübergreifenden Isolierung und warum sie für Features wie `SharedArrayBuffers` erforderlich ist, finden Sie unter [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span><span class="sxs-lookup"><span data-stu-id="39c2c-252">For more information about cross-origin isolation and why it is required for features like `SharedArrayBuffers`, navigate to [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span></span>  <span data-ttu-id="39c2c-253">Navigieren Sie zu Problem [1139899][CR1139899], um Echtzeitupdates dieser Funktion im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-253">To review real-time updates of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informationen über einen anderen Ursprung" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   <span data-ttu-id="39c2c-255">Informationen über einen anderen Ursprung</span><span class="sxs-lookup"><span data-stu-id="39c2c-255">Cross-origin information</span></span>  
:::image-end:::  

#### <a name="new-web-workers-information-in-the-frame-details-view"></a><span data-ttu-id="39c2c-256">Neue Web-Worker-Informationen in der Frame-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="39c2c-256">New Web Workers information in the Frame details view</span></span>  

<span data-ttu-id="39c2c-257">DevTools organisiert nun Web-Worker unter dem entsprechenden übergeordneten Frame.</span><span class="sxs-lookup"><span data-stu-id="39c2c-257">DevTools now organizes web workers under the relevant parent frame.</span></span>  <span data-ttu-id="39c2c-258">Beispiel: Wenn der `someName`-Frame `worker.js` erstellt, wird `worker.js` unter `someName` in der Liste **Frames** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-258">For example, if the `someName` frame creates `worker.js`, then `worker.js` appears under `someName` in the **Frames** list.</span></span>  <span data-ttu-id="39c2c-259">Führen Sie die folgenden Aktionen aus, um die Details des Web-Worker anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-259">To view the details of the web worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="39c2c-260">Öffnen Sie das **Anwendung**-Tool.</span><span class="sxs-lookup"><span data-stu-id="39c2c-260">Open **Application** tool.</span></span>  
1.  <span data-ttu-id="39c2c-261">Erweitern Sie einen Frame, der Web-Worker enthält.</span><span class="sxs-lookup"><span data-stu-id="39c2c-261">Expand a frame that contains web workers.</span></span>  
1.  <span data-ttu-id="39c2c-262">Erweitern Sie die **Worker**-Struktur.</span><span class="sxs-lookup"><span data-stu-id="39c2c-262">Expand the **Workers** tree.</span></span>  
1.  <span data-ttu-id="39c2c-263">Wählen Sie einen Worker aus.</span><span class="sxs-lookup"><span data-stu-id="39c2c-263">Choose a worker.</span></span>  
    
<span data-ttu-id="39c2c-264">Navigieren Sie zu den Problemen [1122507][CR1122507] und [1051466][CR1051466], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-264">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1122507][CR1122507] and [1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informationen für Web-Worker" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   <span data-ttu-id="39c2c-266">Informationen für Web-Worker</span><span class="sxs-lookup"><span data-stu-id="39c2c-266">Web workers information</span></span>  
:::image-end:::  

#### <a name="display-opener-frame-details-for-opened-windows"></a><span data-ttu-id="39c2c-267">Anzeigen von Details zum öffnenden Frame für geöffnete Fenster</span><span class="sxs-lookup"><span data-stu-id="39c2c-267">Display opener frame details for opened windows</span></span>  

<span data-ttu-id="39c2c-268">DevTools organisiert nun geöffnete [Fenster][MdnWindowConstructors] unter dem relevanten übergeordneten [Frame][MdnWindowFrames].</span><span class="sxs-lookup"><span data-stu-id="39c2c-268">DevTools now organizes opened [Windows][MdnWindowConstructors] under the relevant parent [frame][MdnWindowFrames].</span></span>  <span data-ttu-id="39c2c-269">Wenn beispielsweise der `top`-Frame ein `Window` mit `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` öffnet, wird das `Window` unter `top` in der Liste **Frames** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-269">For example, if the `top` frame opens a `Window` to `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, then the `Window` appears under `top` in the **Frames** list.</span></span>  

<span data-ttu-id="39c2c-270">Führen Sie im **Elemente**-Tool die folgenden Aktionen aus, um den Frame anzuzeigen, der für das Öffnen eines anderen Fensters verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="39c2c-270">To reveal the frame responsible for opening another Window in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="39c2c-271">Öffnen Sie die Struktur **Frames**.</span><span class="sxs-lookup"><span data-stu-id="39c2c-271">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="39c2c-272">Erweitern Sie **Geöffnete Fenster**, und wählen Sie das `Window` für den betreffenden übergeordneten Frame aus.</span><span class="sxs-lookup"><span data-stu-id="39c2c-272">Expand **Opened Windows** and choose the `Window` for the parent frame you want to know.</span></span>  
1.  <span data-ttu-id="39c2c-273">Wählen Sie den Link **Öffnender Frame** aus.</span><span class="sxs-lookup"><span data-stu-id="39c2c-273">Choose the **Opener Frame** link.</span></span>  

<span data-ttu-id="39c2c-274">Es werden Details angezeigt, welcher Frame das Öffnen eines anderen `Window` verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="39c2c-274">The details are displayed about which frame caused the opening of another `Window`.</span></span>  <span data-ttu-id="39c2c-275">Führen Sie die folgenden Aktionen aus, um den Öffner im **Elemente**-Tool anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-275">To reveal the opener in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="39c2c-276">Öffnen Sie die Struktur **Frames**.</span><span class="sxs-lookup"><span data-stu-id="39c2c-276">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="39c2c-277">Wählen Sie ein geöffnetes Fenster aus, um die `Window`-Details zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-277">Choose an opened window to open the `Window` details.</span></span>  
1.  <span data-ttu-id="39c2c-278">Wählen Sie den Link **Öffnender Frame** aus.</span><span class="sxs-lookup"><span data-stu-id="39c2c-278">Choose the **Opener Frame** link.</span></span>  
    
<span data-ttu-id="39c2c-279">Navigieren Sie zu Problem [1107766][CR1107766], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-279">To review the history of this feature in the Chromium open-source project, navigate to Issue [1107766][CR1107766].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Details zum geöffneten Frame" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   <span data-ttu-id="39c2c-281">Details zum geöffneten Frame</span><span class="sxs-lookup"><span data-stu-id="39c2c-281">Opened frame details</span></span>  
:::image-end:::  

### <a name="copy-stacktrace-for-network-initiator"></a><span data-ttu-id="39c2c-282">Kopieren von StackTrace für den Netzwerkinitiator</span><span class="sxs-lookup"><span data-stu-id="39c2c-282">Copy stacktrace for network initiator</span></span>  

<span data-ttu-id="39c2c-283">Führen Sie die folgenden Aktionen aus, um den StackTrace in Ihre Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="39c2c-283">To copy the stacktrace to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="39c2c-284">Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).</span><span class="sxs-lookup"><span data-stu-id="39c2c-284">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="39c2c-285">Wählen Sie **Kopieren** > **StackTrace kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="39c2c-285">Choose **Copy** > **Copy stacktrace**.</span></span>  
    
<span data-ttu-id="39c2c-286">Navigieren Sie zu Problem [1139615][CR1139615], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-286">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139615][CR1139615].</span></span>

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Kopieren von StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   <span data-ttu-id="39c2c-288">Kopieren von StackTrace</span><span class="sxs-lookup"><span data-stu-id="39c2c-288">Copy stacktrace</span></span>  
:::image-end:::  

### <a name="preview-wasm-variable-value-on-mouseover"></a><span data-ttu-id="39c2c-289">Vorschau eines Wasm-Variablenwerts bei Mouseover</span><span class="sxs-lookup"><span data-stu-id="39c2c-289">Preview Wasm variable value on mouseover</span></span>  

<span data-ttu-id="39c2c-290">Verwenden Sie dieses Feature, um den Wert einer WebAssembly \(WASM\)-Variablen zu überprüfen, wenn der Code angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="39c2c-290">Use this feature to review the value of a WebAssembly \(Wasm\) variable when your code is paused.</span></span>  <span data-ttu-id="39c2c-291">Um den aktuellen Wert einer Variablen anzuzeigen, zeigen Sie auf eine Variable.</span><span class="sxs-lookup"><span data-stu-id="39c2c-291">To display the current value of a variable, hover on a variable.</span></span>  <span data-ttu-id="39c2c-292">Navigieren Sie zu den Problemen [1058836][CR1058836] und [1071432][CR1071432], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-292">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1058836][CR1058836] and [1071432][CR1071432].</span></span>  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Vorschau von Wasm-Variable bei Mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   <span data-ttu-id="39c2c-294">Vorschau von Wasm-Variable bei Mouseover</span><span class="sxs-lookup"><span data-stu-id="39c2c-294">Preview Wasm variable on mouseover</span></span>  
:::image-end:::  

### <a name="consistent-units-of-measurement-for-sizes-of-files-and-memory"></a><span data-ttu-id="39c2c-295">Einheitliche Maßeinheiten für die Größe von Dateien und Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="39c2c-295">Consistent units of measurement for sizes of files and memory</span></span>  

<span data-ttu-id="39c2c-296">DevTools verwendet jetzt einheitlich `kB`, um die Größe von Dateien und Arbeitsspeicher anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-296">DevTools now consistently use `kB` for displaying sizes of files and memory.</span></span>  <span data-ttu-id="39c2c-297">Zuvor wurden in DevTools `kB` und `KiB` gemischt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-297">Previously DevTools mixed `kB` and `KiB`.</span></span>

*   `kB` <span data-ttu-id="39c2c-298">oder Kilobyte \(10^3 oder 1000 Byte\)</span><span class="sxs-lookup"><span data-stu-id="39c2c-298">or kilobyte \(10^3 or 1000 bytes\)</span></span>  
*   `KiB` <span data-ttu-id="39c2c-299">oder Kibibyte \(2^10 oder 1024 Byte\)</span><span class="sxs-lookup"><span data-stu-id="39c2c-299">or kibibyte \(2^10 or 1024 bytes\)</span></span>  
    
<span data-ttu-id="39c2c-300">Das **Netzwerk**-Tool hat beispielsweise zuvor `kB` in den Beschriftungen, aber `KiB` in Berechnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="39c2c-300">For example, the **Network** tool previously used `kB` in the labels, but used `KiB` in calculations.</span></span>  <span data-ttu-id="39c2c-301">Ihr Feedback hat gezeigt, dass diese Inkonsistenz Verwirrung stiftet.</span><span class="sxs-lookup"><span data-stu-id="39c2c-301">Your feedback showed that this inconsistency caused confusion.</span></span>  <span data-ttu-id="39c2c-302">Navigieren Sie zu Problem [1035309][CR1035309], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39c2c-302">To review the history of this feature in the Chromium open-source project, navigate to Issue [1035309][CR1035309].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="39c2c-303">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="39c2c-303">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="39c2c-304">Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="39c2c-304">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="39c2c-305">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="39c2c-305">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="39c2c-306">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="39c2c-306">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: ../10/devtools.md#customize-keyboard-shortcuts-in-settings "Anpassen von Tastenkombinationen in den Einstellungen – Neuerungen in DevTools (Microsoft Edge 87) | Microsoft Docs"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: ../06/devtools.md#webhint-feedback-in-the-issues-panel "Webhint-Feedback im Bereich „Probleme“ – Neuerungen in DevTools (Microsoft Edge 85) | Microsoft Docs"  

[Devtools3dViewIndex]: ../../../3d-view/index.md "3D-Ansicht | Microsoft Docs"  
[DevtoolsConsoleIndex]: ../../../console/index.md "Übersicht über die Konsole | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Ändern der DevTools-Spracheinstellungen | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../../../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Bearbeiten von Tastenkombinationen für alle Aktionen in DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: ../../../experimental-features/index.md#enable-keyboard-shortcut-editor "Enable keyboard shortcut editor - Experimental features | microsoft Docs"  -->  
<!--  [DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: ../../../experimental-features/index.md#turn-on-composited-layers-in-3d-view "Turn on Composited Layers in 3D View - Experimental features | Microsoft Docs"  -->  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Suchen und Beheben von Problemen mithilfe des Issues-Tools | Microsoft Docs"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: ../../../network/reference.md#copy-formatted-response-json-to-the-clipboard "Formatierte Antwort-JSON in die Zwischenablage kopieren – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayTimingBreakdownRequest]: ../../../network/reference.md#display-the-timing-breakdown-of-a-request "Anzeigen der zeitlichen Aufteilung einer Anforderung – Netzwerkanalysereferenz | Microsoft Docs"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: ../../../css/reference.md#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsIndex]: ../../../../progressive-web-apps-chromium/index.md "Progressive Web-Apps unter Windows | Microsoft Docs"  

[WebdriverChromiumMain]: ../../../../webdriver-chromium/index.md "Verwenden von WebDriver (Chromium) für die Testautomatisierung | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Herunterladen von WebDriver | Microsoft-Entwickler"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

[CR174309]: https://crbug.com/174309 "Problem 174309: DevTools: Zulassen der Anpassung von Tastenkombinationen/Tastenbindungen | Chromium-Fehler"  
[CR945786]: https://crbug.com/945786 "Problem 945786: DevTools: Zulassen des Überschreibens von navigator.storage.estimate() | Chromium-Fehler"  
[CR1029427]: https://crbug.com/1029427 "Problem 1029427: Reduzieren des Leistungsmehraufwands beim Protokollnachrichtenversand im Front-End | Chromium-Fehler"  
[CR1035309]: https://crbug.com/1035309 "Problem 1035309: DevTools sollte konsistent MB für Megabyte verwenden, nicht Mebibyte | Chromium-Fehler"  
[CR1051466]: https://crbug.com/1051466 "Problem 1051466: Unterstützung für COOP/COEP-Debugging in DevTools | Chromium-Fehler"  
[CR1058836]: https://crbug.com/1058836 "Problem 1058836: UX-Probleme rund um das WASM-Debuggen | Chromium-Fehler"  
[CR1071432]: https://crbug.com/1071432 "Problem 1071432: ☂️ Grundlegende Wasm-Entwicklererfahrung | Chromium-Fehler"  
[CR1107766]: https://crbug.com/1107766 "Problem 1107766: Anzeigen von Informationen zu von 'window.open()' generierten Frames in der Frame-Struktur | Chromium-Fehler"  
[CR1122507]: https://crbug.com/1122507 "Problem 1122507: Anzeigen von Worker-Informationen in der Framestrukturansicht | Chromium-Fehler"  
[CR1126178]: https://crbug.com/1126178 "Problem 1126178: ☂ Devtools: CSS <type>-Komponenten | Chromium-Fehler"  
[CR1130556]: https://crbug.com/1130556 "Problem 1130556: DevTools: Testen von Bild-Fallbacks (Emulation) | Chromium-Fehler"  
[CR1132084]: https://crbug.com/1132084 "Problem 1132084: Keine einfache Möglichkeit zum Kopieren von JSON-Anforderungsnutzlast | Chromium-Fehler"  
[CR1136394]: https://crbug.com/1136394 "Problem 1136394: Flexbox-Tooling | Chromium-Fehler"  
[CR1138633]: https://crbug.com/1138633 "Problem 1138633: DevTools: CSS <angle>-Komponente sollte das Erscheinungsbild ihrer Eigenschaft im Hintergrund der Uhr widerspiegeln | Chromium-Fehler"  
[CR1139615]: https://crbug.com/1139615 "Problem 1139615: Netzwerkinitiator sollte die Möglichkeit bieten, die Stapelüberwachung zu kopieren | Chromium-Fehler"  
[CR1139899]: https://crbug.com/1139899 "Problem 1139899: Verfügbarkeit der Gated-API in der Frame-Detailansicht melden | Chromium-Fehler"  
[CR1139945]: https://crbug.com/1139945 "Problem 1139945: Symbole für Flexbox-CSS-Eigenschaften im Bereich &quot;Stile&quot; | Chromium-Fehler"  
[CR1141824]: https://crbug.com/1141824 "Problem 1141824: Verbessern der CORS-Fehlerberichterstattung in DevTools | Chromium-Fehler"  
[CR1144090]: https://crbug.com/1144090 "Problem 1144090: Hinzufügen von Flex-Stil-Adornern zur Elemente-Struktur | Chromium-Fehler"  
[CR1146985]: https://crbug.com/1146985 "Problem 1146985: Gelöschter Text wird weiterhin im Textfeld des Abschnitts &quot;Speicher&quot; des DevTools-Fensters angezeigt | Chromium-Fehler"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "CORS-Fehler | Glitch"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Cross-Origin Resource Sharing (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Verwenden von benutzerdefinierten CSS-Eigenschaften (Variablen) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Konstruktoren – Fenster | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window.frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope.crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Barrierefreiheit | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Kompatibilität | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Leistung | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Fallstricke | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Sicherheit | webhint"  

> [!NOTE]
> <span data-ttu-id="39c2c-358">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39c2c-358">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="39c2c-359">Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-88) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="39c2c-359">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-88) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="39c2c-361">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="39c2c-361">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
