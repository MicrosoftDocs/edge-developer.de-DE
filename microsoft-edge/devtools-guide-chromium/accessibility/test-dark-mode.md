---
description: Überprüfen Sie im Renderingtool mithilfe der Dropdownliste "\"Css-Medienfeature bevorzugen-farbschema\" auf Kontrastprobleme mit dunklem Design und hellem Design (für den dunklen Modus und den hellen Modus).
title: Überprüfen Sie auf Kontrastprobleme mit dunklem Design und hellem Design
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 052c75b610ec872329f387e46819867f299a8ca9
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597447"
---
# <a name="check-for-contrast-issues-with-dark-theme-and-light-theme"></a><span data-ttu-id="dd02a-104">Überprüfen Sie auf Kontrastprobleme mit dunklem Design und hellem Design</span><span class="sxs-lookup"><span data-stu-id="dd02a-104">Check for contrast issues with dark theme and light theme</span></span>

<!-- Rendering tool: Emulate CSS media feature prefers-color-scheme -->

<span data-ttu-id="dd02a-105">Beim Testen der Barrierefreiheit von Farben können unterschiedliche Anzeigefarbdesigns vorhanden sein, die Sie auf Kontrastprobleme testen müssen.</span><span class="sxs-lookup"><span data-stu-id="dd02a-105">When testing color accessibility, there could be different display color themes that you need to test for contrast issues.</span></span>

<span data-ttu-id="dd02a-106">Die meisten Betriebssysteme haben einen dunklen und einen hellen Modus.</span><span class="sxs-lookup"><span data-stu-id="dd02a-106">Most operating systems come with a dark mode and a light mode.</span></span>  <span data-ttu-id="dd02a-107">Ihre Webseite kann mithilfe einer CSS-Medienabfrage auf diese Betriebssystemeinstellung reagieren.</span><span class="sxs-lookup"><span data-stu-id="dd02a-107">Your webpage can react to this operating system setting, by using a CSS media query.</span></span>  <span data-ttu-id="dd02a-108">Sie können diese Designs testen und Ihre CSS-Medienabfrage testen, ohne die Einstellung des Betriebssystems ändern zu müssen, indem Sie die `prefers-color-scheme` CSS-Optionen im **Renderingtool** verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd02a-108">You can test these themes and test your CSS media query without having to change your operating system setting, by using the `prefers-color-scheme` CSS options in the **Rendering** tool.</span></span>

<span data-ttu-id="dd02a-109">Als Beispiel enthält die Demoseite für Barrierefreiheitstests ein helles Design und ein dunkles Design.</span><span class="sxs-lookup"><span data-stu-id="dd02a-109">As an example, the accessibility-testing demo page includes a light theme and a dark theme.</span></span>  <span data-ttu-id="dd02a-110">Die Demoseite erbt die Einstellung für dunkles oder helles Design vom Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="dd02a-110">The demo page inherits the dark or light theme setting from the operating system.</span></span>  <span data-ttu-id="dd02a-111">Wenn wir DevTools verwenden, um zu simulieren, dass das Betriebssystem auf ein Lichtschema festgelegt wird, und dann die Demowebseite aktualisieren, zeigt **das** Problemtool sechs Farbkontrastprobleme anstelle von zwei an.</span><span class="sxs-lookup"><span data-stu-id="dd02a-111">If we use DevTools to simulate the operating system being set to a light scheme and then refresh the demo webpage, the **Issues** tool shows six color-contrast problems instead of two.</span></span>  <span data-ttu-id="dd02a-112">(Möglicherweise werden unterschiedliche Zahlen angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="dd02a-112">(You might see different numbers.)</span></span>


<span data-ttu-id="dd02a-113">So emulieren Sie die Auswahl des bevorzugten Farbdesigns eines Benutzers:</span><span class="sxs-lookup"><span data-stu-id="dd02a-113">To emulate a user's selection of preferred color theme:</span></span>

1.  <span data-ttu-id="dd02a-114">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dd02a-114">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="dd02a-115">Wählen Sie **Esc** aus, um die Schublade am unteren Rand von DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dd02a-115">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="dd02a-116">Wählen Sie das **+** Symbol oben in der Schublade aus, um die Liste der Tools anzuzeigen, und wählen Sie dann **Rendern**aus.</span><span class="sxs-lookup"><span data-stu-id="dd02a-116">Select the **+** icon at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  <span data-ttu-id="dd02a-117">Das Renderingtool wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd02a-117">The Rendering tool appears.</span></span>

1.  <span data-ttu-id="dd02a-118">Wählen Sie in der Dropdownliste für das **Emulieren von CSS-Medienfeatures "prefers-color-scheme"** die Option **"prefers-color-scheme: light" aus.**</span><span class="sxs-lookup"><span data-stu-id="dd02a-118">In the **Emulate CSS media feature prefers-color-scheme** dropdown list, select **prefers-color-scheme: light**.</span></span>      <span data-ttu-id="dd02a-119">Die Webseite wird erneut mithilfe von `light-theme.css` gerendert.</span><span class="sxs-lookup"><span data-stu-id="dd02a-119">The webpage is re-rendered using `light-theme.css`.</span></span>


    :::image type="complex" source="../media/a11y-testing-simulating-light-mode.msft.png" alt-text="Verwenden des Renderingtools zum Simulieren eines Lichtmodus und Auslösen des anderen Designs des Dokuments" lightbox="../media/a11y-testing-simulating-light-mode.msft.png":::
        <span data-ttu-id="dd02a-121">Verwenden des Renderingtools zum Simulieren eines Lichtmodus und Auslösen des anderen Designs des Dokuments</span><span class="sxs-lookup"><span data-stu-id="dd02a-121">Using the Rendering tool to simulate a light mode and triggering the other theme of the document</span></span>
    :::image-end:::


1.  <span data-ttu-id="dd02a-122">Wählen Sie das Tool **"Probleme" aus,** und erweitern Sie dann den Abschnitt **"Barrierefreiheit".**</span><span class="sxs-lookup"><span data-stu-id="dd02a-122">Select the **Issues** tool, and then expand the **Accessibility** section.</span></span>  <span data-ttu-id="dd02a-123">Abhängig von verschiedenen Faktoren erhalten Sie möglicherweise `Insufficient color contrast` Warnungen.</span><span class="sxs-lookup"><span data-stu-id="dd02a-123">Depending on various factors, you might get `Insufficient color contrast` warnings.</span></span> <span data-ttu-id="dd02a-124">Beachten Sie in **DEN BETROFFENEN RESSOURCEN,** dass es 6 Elemente mit unzureichendem Farbkontrast gibt.</span><span class="sxs-lookup"><span data-stu-id="dd02a-124">Notice in **AFFECTED RESOURCES** there are 6 elements with insufficient color contrast.</span></span>
    
    :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Neue Kontrastprobleme aufgrund der Änderung des hellen Designs erkannt" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
        <span data-ttu-id="dd02a-126">Neue Kontrastprobleme aufgrund der Änderung des hellen Designs erkannt</span><span class="sxs-lookup"><span data-stu-id="dd02a-126">New contrast issues detected because of the change to light theme</span></span>
    :::image-end:::
    
    <span data-ttu-id="dd02a-127">Auf unserer Demoseite ist der Abschnitt **"Schenkungsstatus"** der Seite im Lichtmodus unlesbar und muss sich ändern.</span><span class="sxs-lookup"><span data-stu-id="dd02a-127">On our demo page, the **Donation status** section of the page is unreadable in light mode, and needs to change.</span></span> 
    
    :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="Der Abschnitt "Schenkungsstatus" weist Kontrastprobleme im Lichtmodus auf." lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
        <span data-ttu-id="dd02a-129">Der Abschnitt **"Schenkungsstatus"** weist Kontrastprobleme im Lichtmodus auf.</span><span class="sxs-lookup"><span data-stu-id="dd02a-129">The **Donation Status** section has contrast issues in light mode</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="dd02a-130">Wählen Sie in DevTools **das** Elementtool und dann **STRG+F** unter Windows/Linux oder **Befehl+F** unter macOS aus.</span><span class="sxs-lookup"><span data-stu-id="dd02a-130">In DevTools, select the **Elements** tool, and then select **Ctrl+F** on Windows/Linux or **Command+F** on macOS.</span></span>  <span data-ttu-id="dd02a-131">Das Textfeld **suchen** wird angezeigt, um in der HTML-DOM-Struktur zu suchen.</span><span class="sxs-lookup"><span data-stu-id="dd02a-131">The **Find** textbox appears, to search within the HTML DOM tree.</span></span>
 
1.  <span data-ttu-id="dd02a-132">Geben Sie `scheme` .</span><span class="sxs-lookup"><span data-stu-id="dd02a-132">Enter `scheme`.</span></span>  <span data-ttu-id="dd02a-133">Die folgenden CSS-Medienabfragen wurden gefunden, und die entsprechenden CSS-Dateien können jetzt aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="dd02a-133">The following CSS media queries are found, and the corresponding CSS files can now be updated.</span></span>

    ```html
    <link rel="stylesheet" href="css/light-theme.css" media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)">
    <link rel="stylesheet" href="css/dark-theme.css" media="(prefers-color-scheme: dark)">
    ```


## <a name="see-also"></a><span data-ttu-id="dd02a-134">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="dd02a-134">See also</span></span>

*  [<span data-ttu-id="dd02a-135">Simulation von dunklen oder hellen Farbschemas</span><span class="sxs-lookup"><span data-stu-id="dd02a-135">Dark or light color scheme simulation</span></span>][DevToolsColorSchemeSimulation]
*  [<span data-ttu-id="dd02a-136">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="dd02a-136">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="dd02a-137">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="dd02a-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Simulation von dunklen oder hellen Farbschemas | Microsoft-Dokumente"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
