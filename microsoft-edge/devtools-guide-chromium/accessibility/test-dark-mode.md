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
# <a name="check-for-contrast-issues-with-dark-theme-and-light-theme"></a>Überprüfen Sie auf Kontrastprobleme mit dunklem Design und hellem Design

<!-- Rendering tool: Emulate CSS media feature prefers-color-scheme -->

Beim Testen der Barrierefreiheit von Farben können unterschiedliche Anzeigefarbdesigns vorhanden sein, die Sie auf Kontrastprobleme testen müssen.

Die meisten Betriebssysteme haben einen dunklen und einen hellen Modus.  Ihre Webseite kann mithilfe einer CSS-Medienabfrage auf diese Betriebssystemeinstellung reagieren.  Sie können diese Designs testen und Ihre CSS-Medienabfrage testen, ohne die Einstellung des Betriebssystems ändern zu müssen, indem Sie die `prefers-color-scheme` CSS-Optionen im **Renderingtool** verwenden.

Als Beispiel enthält die Demoseite für Barrierefreiheitstests ein helles Design und ein dunkles Design.  Die Demoseite erbt die Einstellung für dunkles oder helles Design vom Betriebssystem.  Wenn wir DevTools verwenden, um zu simulieren, dass das Betriebssystem auf ein Lichtschema festgelegt wird, und dann die Demowebseite aktualisieren, zeigt **das** Problemtool sechs Farbkontrastprobleme anstelle von zwei an.  (Möglicherweise werden unterschiedliche Zahlen angezeigt.)


So emulieren Sie die Auswahl des bevorzugten Farbdesigns eines Benutzers:

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie **Esc** aus, um die Schublade am unteren Rand von DevTools zu öffnen.  Wählen Sie das **+** Symbol oben in der Schublade aus, um die Liste der Tools anzuzeigen, und wählen Sie dann **Rendern**aus.  Das Renderingtool wird angezeigt.

1.  Wählen Sie in der Dropdownliste für das **Emulieren von CSS-Medienfeatures "prefers-color-scheme"** die Option **"prefers-color-scheme: light" aus.**      Die Webseite wird erneut mithilfe von `light-theme.css` gerendert.


    :::image type="complex" source="../media/a11y-testing-simulating-light-mode.msft.png" alt-text="Verwenden des Renderingtools zum Simulieren eines Lichtmodus und Auslösen des anderen Designs des Dokuments" lightbox="../media/a11y-testing-simulating-light-mode.msft.png":::
        Verwenden des Renderingtools zum Simulieren eines Lichtmodus und Auslösen des anderen Designs des Dokuments
    :::image-end:::


1.  Wählen Sie das Tool **"Probleme" aus,** und erweitern Sie dann den Abschnitt **"Barrierefreiheit".**  Abhängig von verschiedenen Faktoren erhalten Sie möglicherweise `Insufficient color contrast` Warnungen. Beachten Sie in **DEN BETROFFENEN RESSOURCEN,** dass es 6 Elemente mit unzureichendem Farbkontrast gibt.
    
    :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Neue Kontrastprobleme aufgrund der Änderung des hellen Designs erkannt" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
        Neue Kontrastprobleme aufgrund der Änderung des hellen Designs erkannt
    :::image-end:::
    
    Auf unserer Demoseite ist der Abschnitt **"Schenkungsstatus"** der Seite im Lichtmodus unlesbar und muss sich ändern. 
    
    :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="Der Abschnitt Schenkungsstatus weist Kontrastprobleme im Lichtmodus auf." lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
        Der Abschnitt **"Schenkungsstatus"** weist Kontrastprobleme im Lichtmodus auf.
    :::image-end:::
    
1.  Wählen Sie in DevTools **das** Elementtool und dann **STRG+F** unter Windows/Linux oder **Befehl+F** unter macOS aus.  Das Textfeld **suchen** wird angezeigt, um in der HTML-DOM-Struktur zu suchen.
 
1.  Geben Sie `scheme` .  Die folgenden CSS-Medienabfragen wurden gefunden, und die entsprechenden CSS-Dateien können jetzt aktualisiert werden.

    ```html
    <link rel="stylesheet" href="css/light-theme.css" media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)">
    <link rel="stylesheet" href="css/dark-theme.css" media="(prefers-color-scheme: dark)">
    ```


## <a name="see-also"></a>Weitere Informationen:

*  [Simulation von dunklen oder hellen Farbschemas][DevToolsColorSchemeSimulation]
*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Simulation von dunklen oder hellen Farbschemas | Microsoft-Dokumente"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
