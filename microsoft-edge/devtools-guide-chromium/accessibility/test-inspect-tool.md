---
description: Verwenden Sie das Inspect-Tool, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen.
title: Verwenden Sie das Inspect-Tool, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: c95116d38e5b0bda88af43ef8bfde4204b8cb372
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597417"
---
# <a name="use-the-inspect-tool-to-detect-accessibility-issues-by-hovering-over-the-webpage"></a><span data-ttu-id="e1c47-104">Verwenden Sie das Inspect-Tool, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen</span><span class="sxs-lookup"><span data-stu-id="e1c47-104">Use the Inspect tool to detect accessibility issues by hovering over the webpage</span></span>

<span data-ttu-id="e1c47-105">Das **Tool Inspect** zeigt Informationen zu einzelnen Elementen an, während Sie auf die gerenderte Webseite zeigen, einschließlich Barrierefreiheitsinformationen.</span><span class="sxs-lookup"><span data-stu-id="e1c47-105">The **Inspect** tool displays information about individual elements as you hover over the rendered webpage, including accessibility information.</span></span>
<span data-ttu-id="e1c47-106">Im Gegensatz dazu meldet das Tool **Probleme** automatisch Probleme für die gesamte Webseite.</span><span class="sxs-lookup"><span data-stu-id="e1c47-106">In contrast, the **Issues** tool automatically reports issues for the entire webpage.</span></span>

<span data-ttu-id="e1c47-107">The **Inspect** tool button \( ![ Inspect ](../media/inspect-icon.msft.png) \) is in the upper-left corner of DevTools.</span><span class="sxs-lookup"><span data-stu-id="e1c47-107">The **Inspect** tool button \(![Inspect](../media/inspect-icon.msft.png)\) is in the upper-left corner of DevTools.</span></span>  <span data-ttu-id="e1c47-108">Wenn Sie die Schaltfläche "Tool **überprüfen"** auswählen, wird die Schaltfläche blau angezeigt, was bedeutet, dass das Tool **"Überprüfen"** aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="e1c47-108">When you select the **Inspect** tool button, the button turns blue, indicating that the **Inspect** tool is active.</span></span>

<span data-ttu-id="e1c47-109">Wenn das **Inspect-Tool** aktiv ist, wird beim Bewegen des Mauszeigers auf ein beliebiges Element auf der gerenderten Webseite die **Inspect-Überlagerung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1c47-109">When the **Inspect** tool is active, hovering over any element on the rendered webpage displays the **Inspect** overlay.</span></span> <span data-ttu-id="e1c47-110">Diese Überlagerung zeigt allgemeine Informationen und Barrierefreiheitsinformationen zu diesem Element an.</span><span class="sxs-lookup"><span data-stu-id="e1c47-110">This overlay displays general information and accessibility information about that element.</span></span>  <span data-ttu-id="e1c47-111">Im Abschnitt **"Barrierefreiheit"** der **Inspect-Überlagerung** werden Informationen zu Textfarbkontrast, Sprachausgabetext und Tastaturunterstützung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1c47-111">The **Accessibility** section of the **Inspect** overlay displays information about text-color contrast, screen reader text, and keyboard support.</span></span>

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="Das Tool Inspect, das den Bereich des Elements als mehrfarbige Überlagerung und die Details des Elements als große Informationsüberlagerung anzeigt" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    <span data-ttu-id="e1c47-113">Das **Tool Inspect,** das den Bereich des Elements als mehrfarbige Überlagerung und die Details des Elements als große Informationsüberlagerung anzeigt</span><span class="sxs-lookup"><span data-stu-id="e1c47-113">The **Inspect** tool, showing the element's area as a multicolor overlay, and showing the element's details as a large information overlay</span></span>
:::image-end:::


## <a name="check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a><span data-ttu-id="e1c47-114">Überprüfen einzelner Elemente auf Textkontrast, Text für die Sprachausgabe und Tastaturunterstützung</span><span class="sxs-lookup"><span data-stu-id="e1c47-114">Check individual elements for text contrast, screen reader text, and keyboard support</span></span>

<!-- Inspect tool: Accessibility section of overlay -->

1.  <span data-ttu-id="e1c47-115">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e1c47-115">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="e1c47-116">Wählen Sie in der oberen linken Ecke von DevTools die Schaltfläche **"Überprüfen** \( ![ Überprüfen ](../media/inspect-icon.msft.png) \)" aus, damit das Symbol hervorgehoben wird (blau).</span><span class="sxs-lookup"><span data-stu-id="e1c47-116">Select the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

    :::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Um das Inspect-Tool zu aktivieren, wählen Sie die Schaltfläche "Überprüfen" aus." lightbox="../media/a11y-testing-basics-inspector.msft.png":::
        <span data-ttu-id="e1c47-118">Um das **Inspect-Tool** zu aktivieren, wählen Sie die Schaltfläche **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="e1c47-118">To turn on the **Inspect** tool, select the **Inspect** button</span></span>
    :::image-end:::

1.  <span data-ttu-id="e1c47-119">Zeigen Sie auf ein beliebiges Element auf der gerenderten Demowebseite.</span><span class="sxs-lookup"><span data-stu-id="e1c47-119">Hover over any element in the rendered demo webpage.</span></span>  <span data-ttu-id="e1c47-120">Das **Tool Inspect** zeigt eine Informationsüberlagerung unterhalb des Elements innerhalb der gerenderten Webseite an.</span><span class="sxs-lookup"><span data-stu-id="e1c47-120">The **Inspect** tool shows an information overlay below the element within the rendered webpage.</span></span>

    :::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="Das Tool Inspect, das das Layout des Elements als mehrfarbige Überlagerung und die Details des Elements als große Informationsüberlagerung anzeigt" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
        <span data-ttu-id="e1c47-122">Das **Tool Inspect,** das das Layout des Elements als mehrfarbige Überlagerung und die Details des Elements als große Informationsüberlagerung anzeigt</span><span class="sxs-lookup"><span data-stu-id="e1c47-122">The **Inspect** tool, showing the element's layout as a multicolor overlay, and showing the element's details as a large information overlay</span></span>
    :::image-end:::

<span data-ttu-id="e1c47-123">Der untere \*\*\*\* Teil der Inspect-Überlagerung verfügt über einen Abschnitt **"Barrierefreiheit",** der die folgenden Informationen enthält:</span><span class="sxs-lookup"><span data-stu-id="e1c47-123">The bottom part of the **Inspect** overlay has an **Accessibility** section that contains the following information:</span></span>

*   <span data-ttu-id="e1c47-124">**Der Kontrast** definiert, ob ein Element von Personen mit sehschwächerer Sicht verstanden werden kann.</span><span class="sxs-lookup"><span data-stu-id="e1c47-124">**Contrast** defines whether an element can be understood by people with low vision.</span></span>  <span data-ttu-id="e1c47-125">Das in den [WCAG-Richtlinien][WCAG] definierte [Kontrastverhältnis][W3CContrastRatio] gibt an, ob ausreichend Kontrast vorhanden ist (ein grünes Häkchensymbol) oder nicht ausreichend (ein orangefarbenes Ausrufezeichensymbol).</span><span class="sxs-lookup"><span data-stu-id="e1c47-125">The [contrast ratio][W3CContrastRatio] as defined by the [WCAG Guidelines][WCAG] indicates whether there is enough contrast (a green check mark icon) or not enough (an orange exclamation-point icon).</span></span>

*   <span data-ttu-id="e1c47-126">**Name** und **Rolle** sind die Hilfstechnologien, z. B. Bildschirmleseprogramme, die über das Element berichten.</span><span class="sxs-lookup"><span data-stu-id="e1c47-126">**Name** and **Role** are what assistive technology such as screen readers will report about the element.</span></span>
    *   <span data-ttu-id="e1c47-127">Der **Name** ist der Textinhalt eines `a` Elements.</span><span class="sxs-lookup"><span data-stu-id="e1c47-127">The **Name** is the text content of an `a` element.</span></span>  <span data-ttu-id="e1c47-128">Für das Element `<a href="/">About Us</a>` lautet der im Inspect-Tool angezeigte **Name** "Über uns".</span><span class="sxs-lookup"><span data-stu-id="e1c47-128">For the element `<a href="/">About Us</a>`, the **Name** shown in the Inspect tool is "About Us".</span></span>
    *   <span data-ttu-id="e1c47-129">Die **Rolle** des Elements.</span><span class="sxs-lookup"><span data-stu-id="e1c47-129">The **Role** of the element.</span></span>  <span data-ttu-id="e1c47-130">Dies ist in der Regel der Elementname, z. `article` B. `img` , oder `link` `heading` .</span><span class="sxs-lookup"><span data-stu-id="e1c47-130">This is usually the element name, such as `article`, `img` , `link`, or `heading`.</span></span>  <span data-ttu-id="e1c47-131">The `div` and elements are referred to as `span` `generic` .</span><span class="sxs-lookup"><span data-stu-id="e1c47-131">The `div` and `span` elements are referred to as `generic`.</span></span>

*   <span data-ttu-id="e1c47-132">**Tastaturfokussierbar** gibt an, ob Benutzer das Element unabhängig vom Eingabegerät erreichen können.</span><span class="sxs-lookup"><span data-stu-id="e1c47-132">**Keyboard-focusable** indicates whether users can reach the element regardless of input device.</span></span>
    *   <span data-ttu-id="e1c47-133">Ein grünes Häkchensymbol weist darauf hin, dass das Element tastaturfokussierbar ist.</span><span class="sxs-lookup"><span data-stu-id="e1c47-133">A green check mark icon indicates that the element is keyboard-focusable.</span></span>
    *   <span data-ttu-id="e1c47-134">Ein grauer Kreis mit diagonaler Linie weist darauf hin, dass das Element nicht tastaturfokussierbar ist.</span><span class="sxs-lookup"><span data-stu-id="e1c47-134">A gray circle with diagonal line indicates that the element isn't keyboard-focusable.</span></span>


## <a name="additional-information-in-the-inspect-overlay"></a><span data-ttu-id="e1c47-135">Zusätzliche Informationen in der Inspect-Überlagerung</span><span class="sxs-lookup"><span data-stu-id="e1c47-135">Additional information in the Inspect overlay</span></span>

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

<span data-ttu-id="e1c47-136">Der obere \*\*\*\* Teil der Inspect-Überlagerung, der sich oberhalb des **Abschnitts "Barrierefreiheit"** befindet, listet die folgenden Details des Elements auf.</span><span class="sxs-lookup"><span data-stu-id="e1c47-136">The top part of the **Inspect** overlay, which is above the **Accessibility** section, lists the following details of the element.</span></span>

*   <span data-ttu-id="e1c47-137">Layouttyp.</span><span class="sxs-lookup"><span data-stu-id="e1c47-137">Layout type.</span></span> <span data-ttu-id="e1c47-138">Wenn das Element mit einem Flexbox- oder Raster positioniert wird, wird ein Symbol \(</span><span class="sxs-lookup"><span data-stu-id="e1c47-138">If the element is positioned using a flexbox or grid, an icon \(</span></span>![Rasterlayoutsymbol](../media/grid-icon.msft.png)<span data-ttu-id="e1c47-140">\) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e1c47-140">\) is displayed.</span></span>
*   <span data-ttu-id="e1c47-141">Name des Elements, z. `h1` B. , `h2` oder `div` .</span><span class="sxs-lookup"><span data-stu-id="e1c47-141">Name of the element, such as `h1`, `h2`, or `div`.</span></span>
*   <span data-ttu-id="e1c47-142">Die Abmessungen des Elements in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e1c47-142">The dimensions of the element in pixels.</span></span>
*   <span data-ttu-id="e1c47-143">Die Farbe als Farbmuster (oder als kleines, farbiges Quadrat) und als Zeichenfolge (z. B. `#336699` ).</span><span class="sxs-lookup"><span data-stu-id="e1c47-143">The color as a color swatch (or a small, colored square) and as a string (such as `#336699`).</span></span>
*   <span data-ttu-id="e1c47-144">Schriftartinformationen, z. B. Schriftgrad und Schriftfamilien.</span><span class="sxs-lookup"><span data-stu-id="e1c47-144">Font information, such as size and font families.</span></span>
*   <span data-ttu-id="e1c47-145">Rand und Abstand in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e1c47-145">Margin and padding in pixels.</span></span>


## <a name="identify-nested-regions-using-color-highlighting"></a><span data-ttu-id="e1c47-146">Identifizieren von geschachtelten Regionen mithilfe von Farbhervorhebung</span><span class="sxs-lookup"><span data-stu-id="e1c47-146">Identify nested regions using color highlighting</span></span> 

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

<span data-ttu-id="e1c47-147">Zusätzlich zur Informationsüberlagerung stellt das **Tool Inspect** auch Regionsfarben bereit, die dem Daraufzeigen in der DOM-Struktur im **Elementtool** ähneln.</span><span class="sxs-lookup"><span data-stu-id="e1c47-147">In addition to the information overlay, the **Inspect** tool also provides region-coloring that's similar to hovering in the DOM tree in the **Elements** tool.</span></span>

1.  <span data-ttu-id="e1c47-148">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e1c47-148">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="e1c47-149">Wählen Sie **in** der oberen linken Ecke von DevTools die Schaltfläche \( ![ Toolsymbol überprüfen ](../media/inspect-icon.msft.png) \) aus, damit die Schaltfläche hervorgehoben ist (blau).</span><span class="sxs-lookup"><span data-stu-id="e1c47-149">Select the **Inspect** button \(![Inspect tool icon](../media/inspect-icon.msft.png)\) in the top-left corner of DevTools, so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="e1c47-150">Zeigen Sie auf verschiedene Teile der gerenderten Demowebseite.</span><span class="sxs-lookup"><span data-stu-id="e1c47-150">Hover over different parts of the rendered demo webpage.</span></span>  <span data-ttu-id="e1c47-151">Jedes Element auf der Webseite wird jetzt mit einer Mehrfarbenüberlagerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1c47-151">Each element in the webpage now displays with a multicolor overlay.</span></span> <span data-ttu-id="e1c47-152">Diese Mehrfarbenüberlagerung kann geschachtelte Bereiche innerhalb eines Elements anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e1c47-152">This multicolor overlay can display nested regions inside of an element.</span></span> <span data-ttu-id="e1c47-153">Zeigen Sie beispielsweise über den linken Rand von **Katzen.**</span><span class="sxs-lookup"><span data-stu-id="e1c47-153">For example, hover over the left margin of **Cats**.</span></span>  <span data-ttu-id="e1c47-154">Das **Inspect-Tool** hebt mehrere rechteckige Teile des **Abschnitts "Katzen"** mit unterschiedlichen Farben hervor und zeigt das Layout an, das aus den CSS-Flexboxdefinitionen auf Ihrer Webseite resultiert.</span><span class="sxs-lookup"><span data-stu-id="e1c47-154">The **Inspect** tool highlights several rectangular portions of the **Cats** section with different colors, showing the layout that results from the CSS flexbox definitions on your webpage.</span></span>

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Mehrfarbige Flexboxüberlagerung und Informationsüberlagerung bei Verwendung des Inspect-Tools" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    <span data-ttu-id="e1c47-156">Mehrfarbige Flexboxüberlagerung und Informationsüberlagerung bei Verwendung des **Inspect-Tools**</span><span class="sxs-lookup"><span data-stu-id="e1c47-156">Multicolor flexbox overlay and information overlay when using the **Inspect** tool</span></span>
:::image-end:::

<span data-ttu-id="e1c47-157">Um die Rasterüberlagerung oder Flexboxüberlagerung zu konfigurieren, wählen Sie im Tool **"Elemente"** die Registerkarte **"Layout"** aus.  Navigieren Sie zu [Css-Raster untersuchen,](..\css\grid.md)um weitere Informationen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="e1c47-157">To configure the grid overlay or flexbox overlay, in the **Elements** tool, select the **Layout** tab.  For more information, navigate to [Inspect CSS Grid](..\css\grid.md).</span></span>


## <a name="use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a><span data-ttu-id="e1c47-158">Verwenden Sie das Inspect-Tool, um mit dem Mauszeiger auf die Webseite zu zeigen, um DAS DOM und CSS hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="e1c47-158">Use the Inspect tool to hover over the webpage to highlight the DOM and CSS</span></span>

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

1.  <span data-ttu-id="e1c47-159">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e1c47-159">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="e1c47-160">Wählen Sie **in** der oberen linken Ecke von DevTools die Schaltfläche \( das Tool Inspect ![ ](../media/inspect-icon.msft.png) \) aus, sodass die Schaltfläche hervorgehoben ist (blau).</span><span class="sxs-lookup"><span data-stu-id="e1c47-160">Select the **Inspect** button \(![the Inspect tool](../media/inspect-icon.msft.png)\) in the top-left corner of DevTools, so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="e1c47-161&quot;>Wählen Sie das Elementtool **aus.**</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e1c47-161&quot;>Select the **Elements** tool.</span></span>

1.  <span data-ttu-id=&quot;e1c47-162&quot;>Wenn das **Inspect-Tool** aktiv ist, bewegen Sie den Mauszeiger über verschiedene Teile der gerenderten Webseite.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e1c47-162&quot;>With the **Inspect** tool active, hover over different parts of the rendered webpage.</span></span>  <span data-ttu-id=&quot;e1c47-163&quot;>Im **Elementtool** wird die HTML-DOM-Struktur automatisch erweitert, um Informationen zu dem Element anzuzeigen, auf das Sie zeigen.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e1c47-163&quot;>In the **Elements** tool, the HTML DOM tree automatically expands to show information about the element you hover over.</span></span>  <span data-ttu-id=&quot;e1c47-164&quot;>Wenn Sie mit dem Mauszeiger darauf zeigen, wird der Bereich **&quot;Formatvorlagen&quot;** nicht aktualisiert.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e1c47-164&quot;>Hovering doesn't cause the **Styles** pane to update.</span></span>

1.  <span data-ttu-id=&quot;e1c47-165&quot;>Wählen Sie nun ein beliebiges Element auf der gerenderten Webseite aus.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e1c47-165&quot;>Now select any element within the rendered webpage.</span></span>  <span data-ttu-id=&quot;e1c47-166&quot;>Das \*\*\*\* Elementtool wird automatisch geöffnet und zeigt den HTML-Code des Elements in der DOM-Struktur an.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e1c47-166&quot;>The **Elements** tool automatically opens and displays the HTML of the element in the DOM tree.</span></span> <span data-ttu-id=&quot;e1c47-167&quot;>Das Tool zeigt auch das angewendete CSS für das Element im Bereich **&quot;Formatvorlagen&quot;** an.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e1c47-167&quot;>The tool also displays the applied CSS on the element in the **Styles** pane.</span></span>  <span data-ttu-id=&quot;e1c47-168&quot;>Wenn Sie ein Element auf der gerenderten Webseite auswählen, wird das **Inspect-Tool** deaktiviert.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e1c47-168&quot;>Selecting an element on the rendered webpage turns off the **Inspect** tool.</span></span>

:::image type=&quot;complex&quot; source=&quot;../media/a11y-testing-basics-inspector-selected-element.msft.png&quot; alt-text=&quot;Details zum ausgewählten Element werden im Elementtool angezeigt.&quot; lightbox=&quot;../media/a11y-testing-basics-inspector-selected-element.msft.png&quot;:::
    <span data-ttu-id=&quot;e1c47-170&quot;>Details zum ausgewählten Element werden **im** Elementtool angezeigt.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e1c47-170&quot;>Details about the selected element are displayed in the **Elements** tool</span></span>
:::image-end:::

<span data-ttu-id=&quot;e1c47-171&quot;>Nachdem Sie ein Element auf der gerenderten Seite ausgewählt haben, können Sie die **Barrierefreiheitsregisterkarte** (in der Nähe der Registerkarte **&quot;Formatvorlagen")** verwenden, um die **Barrierefreiheitsstruktur** anzuzeigen und die **Quellreihenfolgeanzeige**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1c47-171">After selecting an element in the rendered page, you could then use the **Accessibility** tab (near the **Styles** tab) to view the **Accessibility Tree** and use the **Source Order Viewer**.</span></span>


## <a name="see-also"></a><span data-ttu-id="e1c47-172">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="e1c47-172">See also</span></span>

*  [<span data-ttu-id="e1c47-173">Überprüfen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="e1c47-173">Inspect a node</span></span>](../dom/index.md#inspect-a-node)
*  [<span data-ttu-id="e1c47-174">Überprüfen des Textfarbkontrasts im Standardzustand mithilfe des Inspect-Tools</span><span class="sxs-lookup"><span data-stu-id="e1c47-174">Check text-color contrast in the default state using the Inspect tool</span></span>](test-inspect-text-contrast.md)
*  [<span data-ttu-id="e1c47-175">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="e1c47-175">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e1c47-176">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="e1c47-176">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "Kontrastverhältnis | W3c"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Richtlinien für die Barrierefreiheit von Webinhalten | W3c"
