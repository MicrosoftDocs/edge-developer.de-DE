---
description: Überprüfen Sie die Barrierefreiheit aller Zustände von Elementen, z. B. den Textkontrast während des Hoverzustands, im Bereich "Formatvorlagen" mithilfe des Toggle-Elementstatus.
title: Überprüfen der Barrierefreiheit aller Zustände von Elementen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 129a89f94925de24a4e649bd91f513de031d6b4a
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597443"
---
# <a name="verify-accessibility-of-all-states-of-elements"></a><span data-ttu-id="389cf-104">Überprüfen Sie die Barrierefreiheit aller Zustände von Elementen</span><span class="sxs-lookup"><span data-stu-id="389cf-104">Verify accessibility of all states of elements</span></span>

<!-- 5. STYLES: TOGGLE STATE -->

<span data-ttu-id="389cf-105">Überprüfen Sie die Barrierefreiheit aller Zustände von Elementen, z. B. den Kontrast der Textfarbe während des `hover` Zustands.</span><span class="sxs-lookup"><span data-stu-id="389cf-105">Check the accessibility of all states of elements, such as text color contrast during the `hover` state.</span></span>  <span data-ttu-id="389cf-106">Das **Tool Inspect** meldet Barrierefreiheitsprobleme für jeweils einen Status.</span><span class="sxs-lookup"><span data-stu-id="389cf-106">The **Inspect** tool reports accessibility issues for one state at a time.</span></span>  <span data-ttu-id="389cf-107">Um die Barrierefreiheit der verschiedenen Zustände von Elementen zu überprüfen, wählen Sie auf der Registerkarte **Formatvorlagen** **\:hov** (**Toggle Element State**), wie in diesem Artikel beschrieben.</span><span class="sxs-lookup"><span data-stu-id="389cf-107">To check accessibility of the various states of elements, in the **Styles** tab, select **\:hov** (**Toggle Element State**), as described in this article.</span></span> <span data-ttu-id="389cf-108">Wir zeigen zunächst, warum die Zustandssimulation mit dem **Inspect-Tool** erforderlich ist, und dann zeigen wir, wie Zustandssimulationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="389cf-108">We first show why state simulation is necessary using the **Inspect** tool, and then we show how to use state simulation.</span></span>


## <a name="checking-text-color-contrast-in-the-default-state"></a><span data-ttu-id="389cf-109">Überprüfen des Textfarbkontrasts im Standardzustand</span><span class="sxs-lookup"><span data-stu-id="389cf-109">Checking text color contrast in the default state</span></span>

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

<span data-ttu-id="389cf-110">Zusätzlich zu den automatischen Farbkontrasttests im Tool **"Probleme"** können Sie auch das **Tool Inspect** verwenden, um zu überprüfen, ob einzelne Seitenelemente über genügend Kontrast verfügen.</span><span class="sxs-lookup"><span data-stu-id="389cf-110">In addition to the automatic color-contrast tests in the **Issues** tool, you can also use the **Inspect** tool to check whether individual page elements have enough contrast.</span></span>  <span data-ttu-id="389cf-111">Wenn Kontrastinformationen verfügbar \*\*\*\* sind, zeigt die Inspect-Überlagerung das Kontrastverhältnis und ein Kontrollkästchenelement an.</span><span class="sxs-lookup"><span data-stu-id="389cf-111">If contrast information is available, the **Inspect** overlay shows the contrast ratio and a checkbox item.</span></span>  <span data-ttu-id="389cf-112">Ein grünes Häkchensymbol zeigt an, dass genügend Kontrast vorhanden ist, und ein gelbes Warnsymbol zeigt an, dass nicht genügend Kontrast vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="389cf-112">A green check mark icon indicates there's enough contrast, and a yellow alert icon indicates that there's not enough contrast.</span></span>

<span data-ttu-id="389cf-113">Beispielsweise weisen die Links im Navigationsmenü der Seitenleiste ausreichend Kontrast auf.</span><span class="sxs-lookup"><span data-stu-id="389cf-113">For example, the links in the sidebar navigation menu have enough contrast.</span></span>  <span data-ttu-id="389cf-114">Das grüne **Listenelement "Hunde"** im Abschnitt **"Schenkungsstatus"** hat jedoch nicht genügend Kontrast und wird daher durch eine Warnung in der **Inspect-Überlagerung** gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="389cf-114">But the green **Dogs** list item in the **Donation status** section doesn't have enough contrast, and so is flagged by a warning in the **Inspect** overlay.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Die Links im Navigationsmenü der Seitenleiste weisen ausreichend Kontrast auf, wie in der Inspect-Überlagerung dargestellt." lightbox="../media/a11y-testing-enough-contrast.msft.png":::
            <span data-ttu-id="389cf-116">Die Links im Navigationsmenü der Seitenleiste weisen \*\*\*\* ausreichend Kontrast auf, wie in der Inspect-Überlagerung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="389cf-116">The links in the sidebar navigation menu have enough contrast, as shown in the **Inspect** overlay</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Ein Element, das nicht über genügend Kontrast verfügt, wird durch eine Warnung in der Inspect-Überlagerung gekennzeichnet." lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
            <span data-ttu-id="389cf-118">Ein Element, das nicht über genügend Kontrast verfügt, \*\*\*\* wird durch eine Warnung in der Inspect-Überlagerung gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="389cf-118">An element that doesn't have enough contrast is flagged by a warning in the **Inspect** overlay</span></span> :::image-end:::
    :::column-end:::
:::row-end:::
        

## <a name="hovering-when-the-inspect-tool-is-active-doesnt-show-the-text-color-contrast-for-the-hover-state"></a><span data-ttu-id="389cf-119">Beim Bewegen des Mauszeigers, wenn das Tool Inspect aktiv ist, wird der Textfarbkontrast für den Hoverzustand nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="389cf-119">Hovering when the Inspect tool is active doesn't show the text-color contrast for the hover state</span></span>

<span data-ttu-id="389cf-120">Die Informationsüberlagerung des **Tools Inspect** stellt nur einen einzelnen Zustand dar.</span><span class="sxs-lookup"><span data-stu-id="389cf-120">The **Inspect** tool's information overlay only represents a single state.</span></span>  <span data-ttu-id="389cf-121">Elemente auf der Seite können unterschiedliche Zustände aufweisen, die alle getestet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="389cf-121">Elements on the page can have different states, all of which need to be tested.</span></span>  <span data-ttu-id="389cf-122">Wenn Sie beispielsweise mit dem Mauszeiger über das Menü der Demoseite für Barrierefreiheitstests zeigen, erhalten Sie eine Animation, die die Farben ändert.</span><span class="sxs-lookup"><span data-stu-id="389cf-122">For example, when you hover the mouse pointer over the menu of the accessibility-testing demo page, you get an animation that changes the colors.</span></span> <span data-ttu-id="389cf-123">Führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="389cf-123">Perform the following steps.</span></span>

1.  <span data-ttu-id="389cf-124">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="389cf-124">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.</span></span>

1.  <span data-ttu-id="389cf-125">Zeigen Sie auf die blauen Menüelemente im Seitenleisten-Navigationsmenü.</span><span class="sxs-lookup"><span data-stu-id="389cf-125">Hover over the blue menu items in the sidebar navigation menu.</span></span>  <span data-ttu-id="389cf-126">Beachten Sie, dass jedes Element über eine Animation verfügt.</span><span class="sxs-lookup"><span data-stu-id="389cf-126">Notice that each item has an animation.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="Das Menüelement mit unterschiedlichen Farben, wenn sich der Mauszeiger darüber befindet" lightbox="../media/a11y-testing-hover.msft.png":::
        <span data-ttu-id="389cf-128">Das Menüelement mit unterschiedlichen Farben, wenn sich der Mauszeiger darüber befindet</span><span class="sxs-lookup"><span data-stu-id="389cf-128">The menu item showing different colors when the mouse pointer is over it</span></span>
    :::image-end:::
    
<span data-ttu-id="389cf-129">Verwenden Sie nun das Tool Inspect.</span><span class="sxs-lookup"><span data-stu-id="389cf-129">Now, use the Inspect tool.</span></span> <span data-ttu-id="389cf-130">Wenn das Tool Inspect verwendet wird, werden Animationen für die Menüelemente nicht ausgeführt, wenn Sie mit dem Mauszeiger darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="389cf-130">When the Inspect tool is used, animations on the menu items won't run when you hover over them.</span></span>  <span data-ttu-id="389cf-131">Wenn Sie das Tool Inspect verwenden, können Sie den Status für Menüelemente nicht `hover` erreichen, um das Kontrastverhältnis zu testen, da der `hover` Status in Ihren Formatvorlagen nicht ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="389cf-131">When using the Inspect tool, you can't reach the `hover` state on menu items to test the contrast ratio, because the `hover` state in your styles isn't triggered.</span></span>  
    
<span data-ttu-id="389cf-132">Führen Sie die folgenden Schritte aus, um zu bestätigen, dass die Animationen nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="389cf-132">To confirm that your animations don't run, perform the following steps.</span></span>
    
1.  <span data-ttu-id="389cf-133">Wählen \*\*\*\* Sie in der oberen linken Ecke von DevTools die Schaltfläche Überprüfen ![ \( Schaltfläche Überprüfen ](../media/inspect-icon.msft.png) aus, damit das Symbol hervorgehoben wird (blau).</span><span class="sxs-lookup"><span data-stu-id="389cf-133">Select the **Inspect** \(![the Inspect button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="389cf-134">Zeigen Sie auf die blauen Links im Navigationsmenü der Seitenleiste.</span><span class="sxs-lookup"><span data-stu-id="389cf-134">Hover over the blue links on the sidebar navigation menu.</span></span>  <span data-ttu-id="389cf-135">Die Animationen für die Menüelemente werden nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="389cf-135">The animations for the menu items don't run.</span></span> <span data-ttu-id="389cf-136">Stattdessen werden die Menüelemente mit Farben und Hervorhebungen für die Flexbox-Überlagerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="389cf-136">Instead, the menu items are displayed using colors and highlights for the flexbox overlay.</span></span>

<span data-ttu-id="389cf-137">Die Überprüfung auf einen ausreichenden Textkontrast auf diese Weise reicht nicht aus, da die Elemente auf der Seite unterschiedliche Zustände aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="389cf-137">Checking for sufficient text contrast this way isn't enough, because the elements on the page could have different states.</span></span>


## <a name="use-state-simulation-to-simulate-the-hover-state-of-an-animated-menu-item"></a><span data-ttu-id="389cf-138">Verwenden der Zustandssimulation zum Simulieren des Hoverzustands eines animierten Menüelements</span><span class="sxs-lookup"><span data-stu-id="389cf-138">Use state simulation to simulate the hover state of an animated menu item</span></span> 

<!-- Elements tool: Styles pane: Toggle Element State -->

<span data-ttu-id="389cf-139">Wenn das **Inspect-Tool** aktiv ist, müssen Sie den Status des Menüelements simulieren, anstatt mit dem Mauszeiger auf ein animiertes Element zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="389cf-139">When the **Inspect** tool is active, instead of hovering over an animated element, you need to simulate the state of the menu item.</span></span>  <span data-ttu-id="389cf-140">Um den Status eines Menüelements zu simulieren, verwenden Sie die Zustandssimulation im Bereich **"Formatvorlagen".**</span><span class="sxs-lookup"><span data-stu-id="389cf-140">To simulate the state of a menu item, use the state simulation in the **Styles** pane.</span></span>  <span data-ttu-id="389cf-141">Der Bereich **Formatvorlagen** verfügt über die Schaltfläche **\:hov** (**Toggle Element State**), die eine Gruppe von Kontrollkästchen mit der Bezeichnung **"Force"-Elementstatus**anzeigt.</span><span class="sxs-lookup"><span data-stu-id="389cf-141">The **Styles** pane has a **\:hov** (**Toggle Element State**) button, which displays a group of checkboxes labeled **Force element state**.</span></span>

<span data-ttu-id="389cf-142">So aktivieren Sie den Hoverzustand während der Verwendung des Inspect-Tools:</span><span class="sxs-lookup"><span data-stu-id="389cf-142">To turn on the hover state while using the Inspect tool:</span></span>

1.  <span data-ttu-id="389cf-143">Wenn es noch nicht geöffnet ist, öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte.  Wählen Sie dann **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="389cf-143">If it's not open already, open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="389cf-144">Wählen Sie die Schaltfläche **"Inspect** \( ![ Inspect tool button ](../media/inspect-icon.msft.png) \) " in der oberen linken Ecke von DevTools aus, sodass das Symbol hervorgehoben ist (blau).</span><span class="sxs-lookup"><span data-stu-id="389cf-144">Select the **Inspect** \(![Inspect tool button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="389cf-145">Wählen Sie auf der gerenderten Webseite den blauen **Katzenlink** im Seitenleisten-Navigationsmenü aus.</span><span class="sxs-lookup"><span data-stu-id="389cf-145">In the rendered webpage, select the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="389cf-146">Das \*\*\*\* Elementtool wird geöffnet, wobei das Element `<a href="#cats">Cats</a>` ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="389cf-146">The **Elements** tool opens, with the element `<a href="#cats">Cats</a>` selected.</span></span>

    :::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Überprüfen des Elements mit einem Hoverstatus im Elementtool" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
        <span data-ttu-id="389cf-148">Überprüfen des Elements mit einem Hoverstatus im Elementtool</span><span class="sxs-lookup"><span data-stu-id="389cf-148">Inspecting the element that has a hover state in the Elements tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="389cf-149">Wählen Sie die Registerkarte **"Formatvorlagen" aus.**  Das ausgewählte `a` Element weist einen Zustand im CSS `hover` auf, der darauf angewendet wird, aber im Bereich **"Formatvorlagen"** nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="389cf-149">Select the **Styles** tab.  The selected `a` element has a `hover` state in the CSS that is applied to it, but that's not visible in the **Styles** pane.</span></span> 

1.  <span data-ttu-id="389cf-150">Wählen Sie im Bereich **"Formatvorlagen"** rechts neben der Formatvorlagenregel `#sidebar nav li a` den Link `styles.css` aus.</span><span class="sxs-lookup"><span data-stu-id="389cf-150">In the **Styles** pane, to the right of the style rule `#sidebar nav li a`, select the `styles.css` link.</span></span>  <span data-ttu-id="389cf-151">Das **Tool "Quellen"** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="389cf-151">The **Sources** tool opens.</span></span>  <span data-ttu-id="389cf-152">Suchen Sie dann die CSS-Pseudoklassenregel. `#sidebar nav li a:hover`</span><span class="sxs-lookup"><span data-stu-id="389cf-152">Then find the CSS pseudo-class rule `#sidebar nav li a:hover`.</span></span>  <span data-ttu-id="389cf-153">Diese Regel wird nicht ausgeführt, wenn das **Tool Inspect** aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="389cf-153">This rule doesn't run when the **Inspect** tool is active.</span></span>  <span data-ttu-id="389cf-154">In den nächsten Schritten wird die Ausführung dieser Zustandsregel simuliert.</span><span class="sxs-lookup"><span data-stu-id="389cf-154">We'll simulate running this state rule in the next steps.</span></span>

1.  <span data-ttu-id="389cf-155">Wählen Sie das Elementtool **aus.**</span><span class="sxs-lookup"><span data-stu-id="389cf-155">Select the **Elements** tool.</span></span>  <span data-ttu-id="389cf-156">Wählen Sie dann im Bereich **"Formatvorlagen"** die Schaltfläche **:hov** (**Toggle Element State**) aus.</span><span class="sxs-lookup"><span data-stu-id="389cf-156">Then in the **Styles** pane, select the **:hov** (**Toggle Element State**) button.</span></span>  <span data-ttu-id="389cf-157">Die **Force-Elementstatusgruppe** der Kontrollkästchen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="389cf-157">The **Force element state** group of checkboxes is displayed.</span></span>

    :::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="Das Zustandssimulationstool mit allen Optionen" lightbox="../media/a11y-testing-state-simulation.msft.png":::
        <span data-ttu-id="389cf-159">Das Zustandssimulationstool mit allen Optionen</span><span class="sxs-lookup"><span data-stu-id="389cf-159">The state simulation tool showing all the options</span></span>
    :::image-end:::

1.  <span data-ttu-id="389cf-160">Aktivieren Sie das **Kontrollkästchen :hover.**</span><span class="sxs-lookup"><span data-stu-id="389cf-160">Select the **:hover** checkbox.</span></span>  <span data-ttu-id="389cf-161">Im DOM wird links neben dem Element `<a href="#cats">Cats</a>` ein gelber Punkt angezeigt, der angibt, dass das Element einen simulierten Zustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="389cf-161">In the DOM, to the left of the element `<a href="#cats">Cats</a>`, a yellow dot appears, indicating that the element has a simulated state.</span></span>  <span data-ttu-id="389cf-162">Das **Menüelement "Katzen"** wird nun auf der Webseite angezeigt, als würde der Zeiger darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="389cf-162">The **Cats** menu item now appears in the webpage as if the pointer were hovering over it.</span></span>  <span data-ttu-id="389cf-163">Die Animation für das Menüelement kann ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="389cf-163">The animation on the menu item might run.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulieren einen Hoverzustand" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
        <span data-ttu-id="389cf-165">DevTools simulieren einen Hoverzustand</span><span class="sxs-lookup"><span data-stu-id="389cf-165">DevTools simulating a hover state</span></span>
    :::image-end:::

    <span data-ttu-id="389cf-166">Nachdem der simulierte Zustand angewendet wurde, können Sie das **Inspect-Tool** erneut verwenden, um den Kontrast des Elements zu überprüfen, wenn der Benutzer mit dem Mauszeiger darauf zeigt, wie folgt.</span><span class="sxs-lookup"><span data-stu-id="389cf-166">After the simulated state is applied, you can use the **Inspect** tool again to check the contrast of the element when the user hovers over it, as follows.</span></span>

1.  <span data-ttu-id="389cf-167">Wählen Sie in der oberen linken Ecke von DevTools die Schaltfläche **"Überprüfen** \( ![ Inspektorsymbol \) " ](../media/inspect-icon.msft.png) aus, damit das Symbol hervorgehoben ist (blau).</span><span class="sxs-lookup"><span data-stu-id="389cf-167">Select the **Inspect** \(![Inspector icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="389cf-168">Zeigen Sie im Navigationsmenü der Seitenleiste auf den blauen **Katzenlink.**</span><span class="sxs-lookup"><span data-stu-id="389cf-168">Hover over the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="389cf-169">Der Link ist nun hellblau, aufgrund der simulierten Hoveranimation.</span><span class="sxs-lookup"><span data-stu-id="389cf-169">The link is now light blue, because of the simulated hover animation.</span></span>  <span data-ttu-id="389cf-170">Die Informationsüberlagerung des **Inspect-Tools** wird mit einem orangefarbenen Ausrufezeichen in der **Zeile "Kontrast"** angezeigt, das angibt, dass der Kontrast nicht hoch genug ist.</span><span class="sxs-lookup"><span data-stu-id="389cf-170">The **Inspect** tool's information overlay appears, showing an orange exclamation point in the **Contrast** row, indicating that the contrast isn't high enough.</span></span>

    :::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Testen des Kontrasts eines Elements in einem simulierten Hoverzustand" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
        <span data-ttu-id="389cf-172">Testen des Kontrasts eines Elements in einem simulierten Hoverzustand</span><span class="sxs-lookup"><span data-stu-id="389cf-172">Testing the contrast of an element in a simulated hover state</span></span>
    :::image-end:::

<span data-ttu-id="389cf-173">Die Zustandssimulation ist auch eine gute Möglichkeit, um zu überprüfen, ob Sie unterschiedliche Benutzeranforderungen berücksichtigt haben, z. B. die Anforderungen von Tastaturbenutzern.</span><span class="sxs-lookup"><span data-stu-id="389cf-173">State simulation is also a good way to check whether you considered different user needs, such as the needs of keyboard users.</span></span>  <span data-ttu-id="389cf-174">Mithilfe der Kontrollkästchen für den **Force-Elementstatus** können Sie den Zustand simulieren, `:focus` um festzustellen, dass die Benutzeroberfläche unverändert bleibt, wenn sie den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="389cf-174">By using the **Force element state** checkboxes, you can simulate the `:focus` state to discover that the UI remains unchanged when it has focus.</span></span> <span data-ttu-id="389cf-175">Dieses Fehlen eines Indikators, wenn ein Element den Fokus hat, ist ein Problem.</span><span class="sxs-lookup"><span data-stu-id="389cf-175">This lack of an indicator when an element has focus is a problem.</span></span>


## <a name="see-also"></a><span data-ttu-id="389cf-176">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="389cf-176">See also</span></span>

*  [<span data-ttu-id="389cf-177">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="389cf-177">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="389cf-178">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="389cf-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
