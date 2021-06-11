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
# <a name="use-the-inspect-tool-to-detect-accessibility-issues-by-hovering-over-the-webpage"></a>Verwenden Sie das Inspect-Tool, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen

Das **Tool Inspect** zeigt Informationen zu einzelnen Elementen an, während Sie auf die gerenderte Webseite zeigen, einschließlich Barrierefreiheitsinformationen.
Im Gegensatz dazu meldet das Tool **Probleme** automatisch Probleme für die gesamte Webseite.

The **Inspect** tool button \( ![ Inspect ](../media/inspect-icon.msft.png) \) is in the upper-left corner of DevTools.  Wenn Sie die Schaltfläche "Tool **überprüfen"** auswählen, wird die Schaltfläche blau angezeigt, was bedeutet, dass das Tool **"Überprüfen"** aktiv ist.

Wenn das **Inspect-Tool** aktiv ist, wird beim Bewegen des Mauszeigers auf ein beliebiges Element auf der gerenderten Webseite die **Inspect-Überlagerung** angezeigt. Diese Überlagerung zeigt allgemeine Informationen und Barrierefreiheitsinformationen zu diesem Element an.  Im Abschnitt **"Barrierefreiheit"** der **Inspect-Überlagerung** werden Informationen zu Textfarbkontrast, Sprachausgabetext und Tastaturunterstützung angezeigt.

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="Das Tool Inspect, das den Bereich des Elements als mehrfarbige Überlagerung und die Details des Elements als große Informationsüberlagerung anzeigt" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    Das **Tool Inspect,** das den Bereich des Elements als mehrfarbige Überlagerung und die Details des Elements als große Informationsüberlagerung anzeigt
:::image-end:::


## <a name="check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a>Überprüfen einzelner Elemente auf Textkontrast, Text für die Sprachausgabe und Tastaturunterstützung

<!-- Inspect tool: Accessibility section of overlay -->

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie in der oberen linken Ecke von DevTools die Schaltfläche **"Überprüfen** \( ![ Überprüfen ](../media/inspect-icon.msft.png) \)" aus, damit das Symbol hervorgehoben wird (blau).

    :::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Um das Inspect-Tool zu aktivieren, wählen Sie die Schaltfläche Überprüfen aus." lightbox="../media/a11y-testing-basics-inspector.msft.png":::
        Um das **Inspect-Tool** zu aktivieren, wählen Sie die Schaltfläche **"Überprüfen"** aus.
    :::image-end:::

1.  Zeigen Sie auf ein beliebiges Element auf der gerenderten Demowebseite.  Das **Tool Inspect** zeigt eine Informationsüberlagerung unterhalb des Elements innerhalb der gerenderten Webseite an.

    :::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="Das Tool Inspect, das das Layout des Elements als mehrfarbige Überlagerung und die Details des Elements als große Informationsüberlagerung anzeigt" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
        Das **Tool Inspect,** das das Layout des Elements als mehrfarbige Überlagerung und die Details des Elements als große Informationsüberlagerung anzeigt
    :::image-end:::

Der untere **** Teil der Inspect-Überlagerung verfügt über einen Abschnitt **"Barrierefreiheit",** der die folgenden Informationen enthält:

*   **Der Kontrast** definiert, ob ein Element von Personen mit sehschwächerer Sicht verstanden werden kann.  Das in den [WCAG-Richtlinien][WCAG] definierte [Kontrastverhältnis][W3CContrastRatio] gibt an, ob ausreichend Kontrast vorhanden ist (ein grünes Häkchensymbol) oder nicht ausreichend (ein orangefarbenes Ausrufezeichensymbol).

*   **Name** und **Rolle** sind die Hilfstechnologien, z. B. Bildschirmleseprogramme, die über das Element berichten.
    *   Der **Name** ist der Textinhalt eines `a` Elements.  Für das Element `<a href="/">About Us</a>` lautet der im Inspect-Tool angezeigte **Name** "Über uns".
    *   Die **Rolle** des Elements.  Dies ist in der Regel der Elementname, z. `article` B. `img` , oder `link` `heading` .  The `div` and elements are referred to as `span` `generic` .

*   **Tastaturfokussierbar** gibt an, ob Benutzer das Element unabhängig vom Eingabegerät erreichen können.
    *   Ein grünes Häkchensymbol weist darauf hin, dass das Element tastaturfokussierbar ist.
    *   Ein grauer Kreis mit diagonaler Linie weist darauf hin, dass das Element nicht tastaturfokussierbar ist.


## <a name="additional-information-in-the-inspect-overlay"></a>Zusätzliche Informationen in der Inspect-Überlagerung

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

Der obere **** Teil der Inspect-Überlagerung, der sich oberhalb des **Abschnitts "Barrierefreiheit"** befindet, listet die folgenden Details des Elements auf.

*   Layouttyp. Wenn das Element mit einem Flexbox- oder Raster positioniert wird, wird ein Symbol \(![Rasterlayoutsymbol](../media/grid-icon.msft.png)\) angezeigt wird.
*   Name des Elements, z. `h1` B. , `h2` oder `div` .
*   Die Abmessungen des Elements in Pixel.
*   Die Farbe als Farbmuster (oder als kleines, farbiges Quadrat) und als Zeichenfolge (z. B. `#336699` ).
*   Schriftartinformationen, z. B. Schriftgrad und Schriftfamilien.
*   Rand und Abstand in Pixel.


## <a name="identify-nested-regions-using-color-highlighting"></a>Identifizieren von geschachtelten Regionen mithilfe von Farbhervorhebung 

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

Zusätzlich zur Informationsüberlagerung stellt das **Tool Inspect** auch Regionsfarben bereit, die dem Daraufzeigen in der DOM-Struktur im **Elementtool** ähneln.

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie **in** der oberen linken Ecke von DevTools die Schaltfläche \( ![ Toolsymbol überprüfen ](../media/inspect-icon.msft.png) \) aus, damit die Schaltfläche hervorgehoben ist (blau).

1.  Zeigen Sie auf verschiedene Teile der gerenderten Demowebseite.  Jedes Element auf der Webseite wird jetzt mit einer Mehrfarbenüberlagerung angezeigt. Diese Mehrfarbenüberlagerung kann geschachtelte Bereiche innerhalb eines Elements anzeigen. Zeigen Sie beispielsweise über den linken Rand von **Katzen.**  Das **Inspect-Tool** hebt mehrere rechteckige Teile des **Abschnitts "Katzen"** mit unterschiedlichen Farben hervor und zeigt das Layout an, das aus den CSS-Flexboxdefinitionen auf Ihrer Webseite resultiert.

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Mehrfarbige Flexboxüberlagerung und Informationsüberlagerung bei Verwendung des Inspect-Tools" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    Mehrfarbige Flexboxüberlagerung und Informationsüberlagerung bei Verwendung des **Inspect-Tools**
:::image-end:::

Um die Rasterüberlagerung oder Flexboxüberlagerung zu konfigurieren, wählen Sie im Tool **"Elemente"** die Registerkarte **"Layout"** aus.  Navigieren Sie zu [Css-Raster untersuchen,](..\css\grid.md)um weitere Informationen zu erfahren.


## <a name="use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a>Verwenden Sie das Inspect-Tool, um mit dem Mauszeiger auf die Webseite zu zeigen, um DAS DOM und CSS hervorzuheben.

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie **in** der oberen linken Ecke von DevTools die Schaltfläche \( das Tool Inspect ![ ](../media/inspect-icon.msft.png) \) aus, sodass die Schaltfläche hervorgehoben ist (blau).

1.  Wählen Sie das Elementtool **aus.**

1.  Wenn das **Inspect-Tool** aktiv ist, bewegen Sie den Mauszeiger über verschiedene Teile der gerenderten Webseite.  Im **Elementtool** wird die HTML-DOM-Struktur automatisch erweitert, um Informationen zu dem Element anzuzeigen, auf das Sie zeigen.  Wenn Sie mit dem Mauszeiger darauf zeigen, wird der Bereich **"Formatvorlagen"** nicht aktualisiert.

1.  Wählen Sie nun ein beliebiges Element auf der gerenderten Webseite aus.  Das **** Elementtool wird automatisch geöffnet und zeigt den HTML-Code des Elements in der DOM-Struktur an. Das Tool zeigt auch das angewendete CSS für das Element im Bereich **"Formatvorlagen"** an.  Wenn Sie ein Element auf der gerenderten Webseite auswählen, wird das **Inspect-Tool** deaktiviert.

:::image type="complex" source="../media/a11y-testing-basics-inspector-selected-element.msft.png" alt-text="Details zum ausgewählten Element werden im Elementtool angezeigt." lightbox="../media/a11y-testing-basics-inspector-selected-element.msft.png":::
    Details zum ausgewählten Element werden **im** Elementtool angezeigt.
:::image-end:::

Nachdem Sie ein Element auf der gerenderten Seite ausgewählt haben, können Sie die **Barrierefreiheitsregisterkarte** (in der Nähe der Registerkarte **"Formatvorlagen")** verwenden, um die **Barrierefreiheitsstruktur** anzuzeigen und die **Quellreihenfolgeanzeige**zu verwenden.


## <a name="see-also"></a>Weitere Informationen:

*  [Überprüfen eines Knotens](../dom/index.md#inspect-a-node)
*  [Überprüfen des Textfarbkontrasts im Standardzustand mithilfe des Inspect-Tools](test-inspect-text-contrast.md)
*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "Kontrastverhältnis | W3c"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Richtlinien für die Barrierefreiheit von Webinhalten | W3c"
