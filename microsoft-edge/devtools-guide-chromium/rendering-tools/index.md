---
description: Benutzer erwartet interaktive und glatte Seiten.  Jede Phase in der pixelpipeline stellt eine Möglichkeit dar, Jank einzuführen.  Erfahren Sie mehr über Tools und Strategien, um häufige Probleme zu erkennen und zu beheben, die die Runtime-Leistung verlangsamen.
title: Analysieren der Laufzeitleistung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: d42ac5e7a7456971d48198a1f362eebe7156bbce
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230607"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="b4be4-106">Analysieren der Laufzeitleistung</span><span class="sxs-lookup"><span data-stu-id="b4be4-106">Analyze runtime performance</span></span> 

<span data-ttu-id="b4be4-107">Benutzer erwartet interaktive und glatte Seiten.</span><span class="sxs-lookup"><span data-stu-id="b4be4-107">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="b4be4-108">Jede Phase in der pixelpipeline stellt eine Möglichkeit dar, Jank einzuführen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-108">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="b4be4-109">Erfahren Sie mehr über Tools und Strategien, um häufige Probleme zu erkennen und zu beheben, die die Runtime-Leistung verlangsamen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-109">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <span data-ttu-id="b4be4-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b4be4-110">Summary</span></span>  

*   <span data-ttu-id="b4be4-111">Schreiben Sie keine JavaScript-Daten, die den Browser zwingen, das Layout neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-111">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="b4be4-112">Trennen Sie die Lese-und Schreibfunktionen, und führen Sie zuerst Lesevorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="b4be4-112">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="b4be4-113">Verkomplizieren Sie Ihre CSS nicht.</span><span class="sxs-lookup"><span data-stu-id="b4be4-113">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="b4be4-114">Verwenden Sie nicht so viel CSS, damit Ihre CSS-Auswahl einfach ist.</span><span class="sxs-lookup"><span data-stu-id="b4be4-114">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="b4be4-115">Vermeiden Sie das Layout so weit wie möglich.</span><span class="sxs-lookup"><span data-stu-id="b4be4-115">Avoid layout as much as possible.</span></span>  <span data-ttu-id="b4be4-116">Wählen Sie CSS aus, das Layout überhaupt nicht auslöst.</span><span class="sxs-lookup"><span data-stu-id="b4be4-116">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="b4be4-117">Das zeichnen kann mehr Zeit als alle anderen Rendering-Aktivitäten beanspruchen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-117">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="b4be4-118">Achten Sie auf Farb Engpässe.</span><span class="sxs-lookup"><span data-stu-id="b4be4-118">Watch out for paint bottlenecks.</span></span>  
    
## <span data-ttu-id="b4be4-119">JavaScript</span><span class="sxs-lookup"><span data-stu-id="b4be4-119">JavaScript</span></span>  

<span data-ttu-id="b4be4-120">JavaScript-Berechnungen, insbesondere diejenigen, die umfangreiche visuelle Änderungen auslösen, können die Anwendungsleistung verzögern.</span><span class="sxs-lookup"><span data-stu-id="b4be4-120">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="b4be4-121">Lassen Sie nicht zu, dass die Interaktion zwischen unregelmäßigen oder langlebigen JavaScript-Benutzern beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="b4be4-121">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <span data-ttu-id="b4be4-122">JavaScript: Tools</span><span class="sxs-lookup"><span data-stu-id="b4be4-122">JavaScript: Tools</span></span>  

<span data-ttu-id="b4be4-123">Nehmen Sie im **Leistungs** Panel eine Aufzeichnung auf, und suchen Sie nach verdächtig langen `Evaluate Script` Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-123">Take a recording in the **Performance** panel and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="b4be4-124">Wenn Sie einiges an Jank in Ihrem JavaScript bemerken, müssen Sie möglicherweise Ihre Analyse auf die nächste Ebene übertragen und ein JavaScript-CPU-Profil erfassen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-124">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="b4be4-125">In CPU-Profilen wird angezeigt, wo die Laufzeit innerhalb der Funktionen Ihrer Seite ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b4be4-125">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="b4be4-126">Erfahren Sie, wie Sie CPU-Profile in der [JavaScript-Laufzeit beschleunigen][DevtoolsRenderingToolsJavascriptRuntime].</span><span class="sxs-lookup"><span data-stu-id="b4be4-126">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <span data-ttu-id="b4be4-127">JavaScript: Probleme</span><span class="sxs-lookup"><span data-stu-id="b4be4-127">JavaScript: Problems</span></span>  

<span data-ttu-id="b4be4-128">In der folgenden Tabelle werden einige häufige JavaScript-Probleme und mögliche Lösungen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="b4be4-128">The following table describes some common JavaScript problems and potential solutions:</span></span>  

| <span data-ttu-id="b4be4-129">Problem</span><span class="sxs-lookup"><span data-stu-id="b4be4-129">Problem</span></span> | <span data-ttu-id="b4be4-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b4be4-130">Example</span></span> | <span data-ttu-id="b4be4-131">Lösung</span><span class="sxs-lookup"><span data-stu-id="b4be4-131">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b4be4-132">Kostspielige Eingabehandler, die die Antwort oder Animation beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-132">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="b4be4-133">Tippen Sie auf, um den Bildschirm zu scrollen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-133">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="b4be4-134">Lassen Sie den Browser Fingereingabe und scrollen, oder binden Sie den Listener so spät wie möglich.</span><span class="sxs-lookup"><span data-stu-id="b4be4-134">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="b4be4-135">Informationen [zu kostspieligen Eingabe Handlern finden Sie in der Checkliste zur Leistungsfähigkeit von Paul Lewis][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="b4be4-135">See [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="b4be4-136">JavaScript mit starkem Zeitlimit, das die Antwort, Animation, Auslastung beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="b4be4-136">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="b4be4-137">Der Benutzer scrollt direkt nach dem Laden der Seite, setTimeout/setInterval.</span><span class="sxs-lookup"><span data-stu-id="b4be4-137">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="b4be4-138">JavaScript-Laufzeit optimieren: Verwenden Sie `requestAnimationFrame` , verbreiten Sie DOM-Manipulation über Frames, verwenden Sie [Web-Worker][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="b4be4-138">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="b4be4-139">JavaScript mit langer Laufzeit, das die Antwort beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="b4be4-139">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="b4be4-140">Das [DOMContentLoaded-Ereignis][MDNUsingWebWorkers] wird angehalten, da es mit js work überschwemmt wird.</span><span class="sxs-lookup"><span data-stu-id="b4be4-140">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="b4be4-141">Verschieben Sie reine Rechenarbeit auf [web work worker][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="b4be4-141">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="b4be4-142">Wenn Sie DOM-Zugriff benötigen, verwenden Sie `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="b4be4-142">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="b4be4-143">Garbage-y-Skripte, die die Antwort oder Animation beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-143">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="b4be4-144">Die Garbage Collection kann überall vorkommen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-144">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="b4be4-145">Schreiben Sie geringere Garbage-y-Skripte.</span><span class="sxs-lookup"><span data-stu-id="b4be4-145">Write less garbage-y scripts.</span></span>  <span data-ttu-id="b4be4-146">Informationen dazu finden Sie unter [Garbage Collection in Animation in Paul Lewis ' Runtime Performance Checkliste][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="b4be4-146">See [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <span data-ttu-id="b4be4-147">Format</span><span class="sxs-lookup"><span data-stu-id="b4be4-147">Style</span></span>  

<span data-ttu-id="b4be4-148">Formatänderungen sind kostspielig, insbesondere dann, wenn sich diese Änderungen auf mehr als ein Element im Dom auswirken.</span><span class="sxs-lookup"><span data-stu-id="b4be4-148">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="b4be4-149">Jedes Mal, wenn Sie Formatvorlagen auf ein Element anwenden, wird der Browser die Auswirkungen auf alle zugehörigen Elemente ermitteln, das Layout neu berechnen und neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-149">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <span data-ttu-id="b4be4-150">Formatvorlage: Tools</span><span class="sxs-lookup"><span data-stu-id="b4be4-150">Style: Tools</span></span>  

<span data-ttu-id="b4be4-151">Führen Sie eine Aufzeichnung im **Leistungs** Panel aus.</span><span class="sxs-lookup"><span data-stu-id="b4be4-151">Take a recording in the **Performance** panel.</span></span>  <span data-ttu-id="b4be4-152">Überprüfen Sie die Aufzeichnung auf große `Recalculate Style` Ereignisse \ (in Lila angezeigt).</span><span class="sxs-lookup"><span data-stu-id="b4be4-152">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="b4be4-153">Klicken Sie auf ein `Recalculate Style` Ereignis, um weitere Informationen dazu im **Detail** Bereich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-153">Click on a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="b4be4-154">Wenn die Formatänderungen sehr lange dauern, handelt es sich um einen leistungserfolg.</span><span class="sxs-lookup"><span data-stu-id="b4be4-154">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="b4be4-155">Wenn sich die Format Berechnungen auf eine große Anzahl von Elementen auswirken, handelt es sich um einen anderen Bereich mit Raum für Verbesserungen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-155">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Formatvorlage ' lange neu berechnen '" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="b4be4-157">Formatvorlage ' lange neu berechnen '</span><span class="sxs-lookup"><span data-stu-id="b4be4-157">Long recalculate style</span></span>  
:::image-end:::  

<span data-ttu-id="b4be4-158">So verringern Sie die Auswirkungen von `Recalculate Style` Ereignissen:</span><span class="sxs-lookup"><span data-stu-id="b4be4-158">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="b4be4-159">Verwenden Sie die [CSS-Trigger][CssTriggers] , um zu erfahren, welche CSS-Eigenschaften Layout, Paint und Composite auslösen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-159">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="b4be4-160">Diese Eigenschaften haben die größten Auswirkungen auf die Leistung des Renderings.</span><span class="sxs-lookup"><span data-stu-id="b4be4-160">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="b4be4-161">Wechseln Sie zu Eigenschaften, die geringere Auswirkungen haben.</span><span class="sxs-lookup"><span data-stu-id="b4be4-161">Switch to properties that have less impact.</span></span>  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <span data-ttu-id="b4be4-162">Formatvorlage: Probleme</span><span class="sxs-lookup"><span data-stu-id="b4be4-162">Style: Problems</span></span>  

<span data-ttu-id="b4be4-163">In der folgenden Tabelle werden einige allgemeine Stil Probleme und mögliche Lösungen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="b4be4-163">The following table describes some common style problems and potential solutions:</span></span>  

| <span data-ttu-id="b4be4-164">Problem</span><span class="sxs-lookup"><span data-stu-id="b4be4-164">Problem</span></span> | <span data-ttu-id="b4be4-165">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b4be4-165">Example</span></span> | <span data-ttu-id="b4be4-166">Lösung</span><span class="sxs-lookup"><span data-stu-id="b4be4-166">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b4be4-167">Kostspielige Formatvorlagen Berechnungen, die die Antwort oder Animation beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-167">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="b4be4-168">Eine beliebige CSS-Eigenschaft, die die Geometrie eines Elements ändert, wie Breite, Höhe oder Position; der Browser überprüft alle anderen Elemente und berechnet das Layout neu.</span><span class="sxs-lookup"><span data-stu-id="b4be4-168">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="b4be4-169">Vermeiden von CSS, das Layouts auslöst</span><span class="sxs-lookup"><span data-stu-id="b4be4-169">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="b4be4-170">Komplexe Auswahlen, die die Antwort oder Animation beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-170">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="b4be4-171">Geschachtelte Auswahlen zwingen den Browser, alles über alle anderen Elemente zu erfahren, einschließlich Eltern und untergeordneten Elementen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-171">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="b4be4-172">Verweisen Sie mit nur einer Klasse auf ein Element in Ihrem CSS.</span><span class="sxs-lookup"><span data-stu-id="b4be4-172">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <span data-ttu-id="b4be4-173">Layout</span><span class="sxs-lookup"><span data-stu-id="b4be4-173">Layout</span></span>  

<span data-ttu-id="b4be4-174">Layout (oder Reflow in Firefox) ist der Prozess, bei dem der Browser die Positionen und Größen aller Elemente auf einer Seite berechnet.</span><span class="sxs-lookup"><span data-stu-id="b4be4-174">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="b4be4-175">Das Layout-Modell des Webs bedeutet, dass ein Element andere beeinflussen kann. beispielsweise wirkt sich die Breite des `<body>` Elements in der Regel auf die Breite aller untergeordneten Elemente und so weiter auf die gesamte Struktur nach oben und unten aus.</span><span class="sxs-lookup"><span data-stu-id="b4be4-175">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="b4be4-176">Der Vorgang ist möglicherweise für den Browser ziemlich kompliziert.</span><span class="sxs-lookup"><span data-stu-id="b4be4-176">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="b4be4-177">Als Faustregelgilt: Wenn Sie einen geometrischen Wert zurück aus dem Dom anfordern, bevor ein Frame abgeschlossen ist, werden Sie sich mit "erzwungenen synchronen Layouts" befunden, was ein großer Leistungsengpass sein kann, wenn Sie häufig wiederholt werden oder für eine große DOM-Struktur ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b4be4-177">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <span data-ttu-id="b4be4-178">Layout: Tools</span><span class="sxs-lookup"><span data-stu-id="b4be4-178">Layout: Tools</span></span>  

<span data-ttu-id="b4be4-179">Der Bereich " **Leistung** " gibt an, wann eine Seite erzwungene synchrone Layouts verursacht.</span><span class="sxs-lookup"><span data-stu-id="b4be4-179">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="b4be4-180">Diese `Layout` Ereignisse sind mit roten Balken gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="b4be4-180">These `Layout` events are marked with red bars.</span></span>  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Erzwungenes synchrones Layout" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="b4be4-182">Erzwungenes synchrones Layout</span><span class="sxs-lookup"><span data-stu-id="b4be4-182">Forced synchronous layout</span></span>  
:::image-end:::  

<span data-ttu-id="b4be4-183">"Layout-Thrashing" ist eine Wiederholung erzwungener synchroner layoutbedingungen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-183">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="b4be4-184">Dies tritt auf, wenn JavaScript wiederholt vom Dom geschrieben und gelesen wird, wodurch der Browser die Neuberechnung des Layouts erzwungen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-184">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="b4be4-185">Suchen Sie nach einem Muster mehrerer erzwungener synchroner Layout-Warnungen, um das verprügeln des Layouts zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-185">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="b4be4-186">Sehen Sie sich die vorhergehende Zahl an.</span><span class="sxs-lookup"><span data-stu-id="b4be4-186">See the previous figure.</span></span>  

### <span data-ttu-id="b4be4-187">Layout: Probleme</span><span class="sxs-lookup"><span data-stu-id="b4be4-187">Layout: Problems</span></span>  

<span data-ttu-id="b4be4-188">In der folgenden Tabelle werden einige häufige Probleme beim Layout und mögliche Lösungen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="b4be4-188">The following table describes some common layout problems and potential solutions:</span></span>  

| <span data-ttu-id="b4be4-189">Problem</span><span class="sxs-lookup"><span data-stu-id="b4be4-189">Problem</span></span> | <span data-ttu-id="b4be4-190">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b4be4-190">Example</span></span> | <span data-ttu-id="b4be4-191">Lösung</span><span class="sxs-lookup"><span data-stu-id="b4be4-191">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b4be4-192">Erzwungenes synchrones Layout, das die Antwort oder Animation beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="b4be4-192">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="b4be4-193">Erzwingen, dass der Browser das Layout zuvor in der pixelpipeline ausführt, wodurch sich wieder holende Schritte im Renderingprozess ergeben.</span><span class="sxs-lookup"><span data-stu-id="b4be4-193">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="b4be4-194">Stapeln Sie Ihre Formatvorlage zuerst, und führen Sie dann alle Schreibvorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="b4be4-194">Batch your style reads first, then do any writes.</span></span>  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="b4be4-195">Das Layout verprügelt Auswirkungen auf die Antwort oder Animation.</span><span class="sxs-lookup"><span data-stu-id="b4be4-195">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="b4be4-196">Eine Schleife, die den Browser in einen Lese-Schreib-Lese-/Schreibzugriff.-Zyklus versetzt, wodurch der Browser das Layout immer wieder neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="b4be4-196">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="b4be4-197">Automatisches Stapeln von Lese-und Schreibvorgängen mithilfe der [FastDom-Bibliothek][GitHubWilsonpageFastdom]</span><span class="sxs-lookup"><span data-stu-id="b4be4-197">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <span data-ttu-id="b4be4-198">Malen und Composite</span><span class="sxs-lookup"><span data-stu-id="b4be4-198">Paint and composite</span></span>  

<span data-ttu-id="b4be4-199">Paint ist der Vorgang des Füllens von Pixeln.</span><span class="sxs-lookup"><span data-stu-id="b4be4-199">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="b4be4-200">Es ist oft der kostspieligste Teil des Rendering-Prozesses.</span><span class="sxs-lookup"><span data-stu-id="b4be4-200">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="b4be4-201">Wenn Sie festgestellt haben, dass Ihre Seite in irgendeiner Weise Janky ist, haben Sie wahrscheinlich Probleme mit Paint.</span><span class="sxs-lookup"><span data-stu-id="b4be4-201">If you noticed that your page is janky in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="b4be4-202">Compositing ist der Ort, an dem die gemalten Teile der Seite für die Anzeige auf dem Bildschirm zusammengestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b4be4-202">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="b4be4-203">In den meisten Fällen sollten Sie, wenn Sie sich an nur für Compositor-Eigenschaften halten und die Farbe ganz vermeiden, eine deutliche Verbesserung der Leistung festzustellen, doch müssen Sie auf eine übermäßige Anzahl von Ebenen achten.</span><span class="sxs-lookup"><span data-stu-id="b4be4-203">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should see a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <span data-ttu-id="b4be4-204">Paint und Composite: Tools</span><span class="sxs-lookup"><span data-stu-id="b4be4-204">Paint and composite: Tools</span></span>  

<span data-ttu-id="b4be4-205">Möchten Sie wissen, wie lange das Malen dauert oder wie oft gemalt wird?</span><span class="sxs-lookup"><span data-stu-id="b4be4-205">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="b4be4-206">Aktivieren Sie das Kontrollkästchen [Erweiterte Farben Instrumentation aktivieren][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] im **Leistungs** Panel, und nehmen Sie dann eine Aufzeichnung vor.</span><span class="sxs-lookup"><span data-stu-id="b4be4-206">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="b4be4-207">Wenn die meiste Zeit für das Rendern von Bildern verwendet wird, gibt es Probleme mit der Farbwiedergabe.</span><span class="sxs-lookup"><span data-stu-id="b4be4-207">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <span data-ttu-id="b4be4-208">Paint und Composite: Probleme</span><span class="sxs-lookup"><span data-stu-id="b4be4-208">Paint and composite: Problems</span></span>  

<span data-ttu-id="b4be4-209">In der folgenden Tabelle werden einige häufige Probleme bei der Farb-und Zusammensetzung und mögliche Lösungen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="b4be4-209">The following table describes some common paint and composite problems and potential solutions:</span></span>  

| <span data-ttu-id="b4be4-210">Problem</span><span class="sxs-lookup"><span data-stu-id="b4be4-210">Problem</span></span> | <span data-ttu-id="b4be4-211">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b4be4-211">Example</span></span> | <span data-ttu-id="b4be4-212">Lösung</span><span class="sxs-lookup"><span data-stu-id="b4be4-212">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b4be4-213">Malen Sie Stürme, die die Antwort oder Animation beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-213">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="b4be4-214">Große Farbbereiche oder kostspielige Farben, die die Antwort oder Animation beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="b4be4-214">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="b4be4-215">Vermeiden Sie Paint, fördern Sie Elemente, die in eine eigene Ebene verschoben werden, und verwenden Sie Transformationen und Deckkraft.</span><span class="sxs-lookup"><span data-stu-id="b4be4-215">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="b4be4-216">Layer-Explosionen, die Animationen beeinflussen</span><span class="sxs-lookup"><span data-stu-id="b4be4-216">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="b4be4-217">Die über Förderung von zu vielen Elementen mit `translateZ(0)` starkem Einfluss auf die animationsleistung.</span><span class="sxs-lookup"><span data-stu-id="b4be4-217">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="b4be4-218">Werben Sie auf Ebenen sparsam, und nur, wenn Sie wissen, dass es greifbare Verbesserungen bietet.</span><span class="sxs-lookup"><span data-stu-id="b4be4-218">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <span data-ttu-id="b4be4-219">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="b4be4-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Beschleunigen der JavaScript-Laufzeit | Microsoft docs"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Aktivieren von Advanced Paint Instrumentation – Referenz zur Leistungsanalyse | Microsoft docs"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: ./rendering-tools/forced-synchronous-layouts.md "Diagnose Forced Synchronous Layouts | Microsoft Docs"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: ../evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: ../evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: ../evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: ../evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool | Microsoft Docs"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "CSS-Trigger"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Verwenden von Web Workers | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Die Checkliste für die Laufzeitleistung – webleistungs Kalender"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> <span data-ttu-id="b4be4-226">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4be4-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b4be4-227">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) und [Meggin Kearney][MegginKearney] \ (Tech Writer \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="b4be4-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="b4be4-229">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b4be4-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
