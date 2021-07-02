---
description: Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme mithilfe des Abschnitts "Barrierefreiheit" des Tools "Probleme".
title: Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 1cba9db1744235dfbfd2a007e33d1101452aab31
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624738"
---
# <a name="automatically-test-a-webpage-for-accessibility-issues"></a>Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme

Das Tool **"Probleme"** enthält einen Abschnitt **zur Barrierefreiheit,** in dem Automatisch Probleme gemeldet werden, z. B. fehlender alternativer Text auf Bildern, fehlende Beschriftungen in Formularfeldern und unzureichender Kontrast von Textfarben.  Das Tool **"Probleme"** befindet sich in der **Schublade** am unteren Rand von DevTools.  In diesem Artikel wird die Demowebseite zum Testen der Barrierefreiheit verwendet, um den Abschnitt **"Barrierefreiheit"** des **Tools "Probleme"** zu verwenden.

Es gibt mehrere Möglichkeiten, das **Problemtool** zu öffnen, z. B.:
*  Wählen Sie den **Problemindikator** \( ![ Problemzähler ](../media/issues-counter-icon.msft.png) \) in der oberen rechten Ecke von DevTools aus.
*  Klicken Sie **im** Elementtool in der DOM-Struktur **umschalten+auf** eine wellenförmige Unterstreichung für ein Element.
*  Geben Sie im **Befehlsmenü** `issues` ein, und wählen Sie dann **Probleme anzeigen aus.**


## <a name="view-the-accessibility-section-of-the-issues-tool"></a>Anzeigen des Abschnitts "Barrierefreiheit" des Tools "Probleme"

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.  In der oberen rechten Ecke wird der **Problemindikator** \( ![ Problemzähler ](../media/issues-counter-icon.msft.png) \) als Symbol für die Sprachblase zusammen mit der Anzahl der automatisch erkannten Probleme angezeigt.  Möglicherweise wird in Ihrem Browser eine andere Nummer angezeigt, und die Nummer wird möglicherweise aktualisiert, wenn Sie DevTools verwenden.

    :::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="Der Problemindikator in DevTools, der angibt, wie viele Probleme im aktuellen Dokument vorhanden sind" lightbox="../media/a11y-testing-issues-tracker.msft.png":::
        Der **Problemindikator** in DevTools, der angibt, wie viele Probleme im aktuellen Dokument vorhanden sind
    :::image-end:::

1.  Wählen Sie den **Problemindikator aus.**  Das Tool **"Probleme"** wird in der **Schublade** am unteren Rand von DevTools geöffnet.

    :::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Warnungen zur Barrierefreiheit, die im Tool Probleme angezeigt werden" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
        Warnungen zur Barrierefreiheit, die im Tool "Probleme" angezeigt werden
    :::image-end:::

1.  Erweitern Sie auf der Registerkarte **"Probleme"** den Abschnitt **"Barrierefreiheit".**


## <a name="verify-that-input-fields-have-labels"></a>Überprüfen, ob Eingabefelder Bezeichnungen aufweisen

Um zu überprüfen, ob mit Eingabefeldern Bezeichnungen verbunden sind, verwenden Sie das Tool **"Probleme",** das automatisch die gesamte Webseite überprüft und dieses Problem im Abschnitt **"Barrierefreiheit"** meldet.

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie oben rechts den **Problemindikator** \( ![ Problemzähler ](../media/issues-counter-icon.msft.png) \) aus.  Das Tool **"Probleme"** wird in der **Schublade** am unteren Rand von DevTools geöffnet.

1.  Erweitern Sie auf der Registerkarte **"Probleme"** den Abschnitt **"Barrierefreiheit".**

1.  Erweitern Sie die **Warnung** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute` .

1. Wählen Sie den Link **"In Elementen öffnen"** aus.

    :::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Elementtool, das den problematischen HTML-Code zeigt, nachdem der Link im Tool Probleme ausgewählt wurde" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
        Elementtool, das den problematischen HTML-Code zeigt, nachdem der Link im Tool **"Probleme"** ausgewählt wurde :::image-end:::

    Das **** Elementtool wird geöffnet, wobei das Element in der DOM-Struktur hervorgehoben ist.  Im Bereich **"Formatvorlagen"** werden die angewendeten CSS-Regeln für das Element angezeigt.  Der folgende Code wird nun angezeigt.

    ```html
    <label>Search</label>
    <input type="search">
    <input type="submit" value="go">
    ```

    Im obigen Code wird das `label` Element falsch verwendet, da es keine Verbindung zwischen dem `label` Element und einem bestimmten Element `input` gibt.  Verwenden Sie eine der folgenden Optionen, um das `label` Element mit einem bestimmten Element zu `input` verbinden.
    *   Schachteln Sie das `input` Element innerhalb des `label` Elements.
    *   Fügen Sie im `label` Element ein Attribut hinzu, das mit einem `for` Attribut des Elements `id` `input` übereinstimmt.

    Es gibt auch eine andere Möglichkeit, auf fehlende Verbindungen zwischen Elementen zu testen. Wählen Sie im Tool **"Elemente"** das `<label>Search</label>` Element in der DOM-Struktur aus.  Beachten Sie auf der Webseite, dass der Fokus nur auf der **Beschriftung "Suchen"** und nicht auf dem Eingabetextfeld angezeigt wird.  Bei der richtigen Implementierung würden der Fokus auf das `search` Eingabetextfeld und die **Suchbeschriftung** gesetzt.

1.  Wählen Sie als Beispiel für eine korrekte Verbindung die Bezeichnung **"Andere"** auf dem Formular für die Gabe aus.  Ein Fokusindikatorfeld wird im Eingabetextfeld neben **** der Beschriftung Other korrekt angezeigt, da Übereinstimmungs- und Attributwerte vorhanden `for` `id` sind.

1.  Wählen Sie im **Tool "Probleme"** die Option **"Weitere Informationen"** aus, um mehr über das Problem zu erfahren.  Um den Link auf einer neuen Registerkarte zu öffnen, klicken Sie **mit strg** + **auf** den Link auf Windows/Linux, oder **klicken**Sie auf den Link unter + **** macOS.

    :::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Link auf der Registerkarte Probleme mit detaillierteren Informationen zu dem Problem" lightbox="../media/a11y-testing-more-information-links.msft.png":::
        Link auf der Registerkarte **"Probleme"** mit detaillierteren Informationen zu dem Problem
    :::image-end:::


## <a name="verify-that-images-have-alt-text"></a>Stellen Sie sicher, dass Bilder über alt-Text verfügen

Für grundlegende Barrierefreiheitstests muss sichergestellt werden, dass für Bilder alternativer Text (auch _als Alttext_bezeichnet) bereitgestellt wird.

Verwenden Sie das Tool **"Probleme",** das über einen Abschnitt **"Barrierefreiheit"** verfügt, um automatisch zu überprüfen, ob alternativer Text für Bilder bereitgestellt wird.  Das **Tool "Probleme"** befindet sich in der **Schublade** am unteren Rand von DevTools.

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.

1.  Um das Tool **"Probleme"** zu öffnen, wählen Sie den **Problemindikator** in der oberen rechten Ecke von DevTools aus.

1.  Erweitern Sie auf der Registerkarte **"Probleme"** die `Images must have alternate text: Element has no title attribute` Warnung.  Es gibt vier Instanzen von Bildern, für die kein alternativer Text vorhanden ist.

    :::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="Das Tool Probleme, das Bilder meldet, für die alternativer Text fehlt" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
        Das Tool "Probleme", das Bilder meldet, für die alternativer Text fehlt
    :::image-end:::

Um weitere Informationen zu erhalten, müssen Sie zu ["Bilder" alternativen Text haben.](https://dequeuniversity.com/rules/axe/4.1/image-alt)


## <a name="verify-that-text-colors-have-enough-contrast"></a>Sicherstellen, dass Textfarben über genügend Kontrast verfügen

Um automatisch zu überprüfen, ob Textfarben über genügend Kontrast verfügen, verwenden Sie das Tool **"Probleme",** das über einen Abschnitt **"Barrierefreiheit"** verfügt.  Das **Tool "Probleme"** befindet sich in der **Schublade** am unteren Rand von DevTools.

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.

1.  Um das Tool **"Probleme"** zu öffnen, wählen Sie den **Problemindikator** in der oberen rechten Ecke von DevTools aus.  Möglicherweise erhalten Sie Warnungen, dass zwei Elemente auf der Demowebseite nicht über genügend Kontrast verfügen.

    :::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Im Tool Probleme gemeldete Kontrastprobleme" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
        Im Tool "Probleme" gemeldete Kontrastprobleme
    :::image-end:::

1.  Abhängig von Ihren Einstellungen wird auf der Registerkarte **"Probleme"** möglicherweise eine Warnung angezeigt, z. B. wenn **Benutzer aufgrund eines unzureichenden Farbkontrasts Probleme**beim Lesen von Textinhalten haben.   Sie können diese Warnung erweitern und dann betroffene **Ressourcen**erweitern.  Eine Liste von Elementen wird mit einer Liste von Elementen angezeigt, die nicht über genügend Kontrast verfügen.


1.  Wählen Sie das `li.high` Element aus.  Auf der gerenderten Webseite wird der Link **"Hunde"** im Abschnitt ** Hebung ** hervorgehoben, wobei eine kleine Informationsüberlagerung angezeigt wird.  Dies ist die gleiche Überlagerung, die angezeigt wird, wenn Sie mit dem Mauszeiger über ein Element in der DOM-Struktur im **Elementtool** zeigen.

    :::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Element auf der Webseite, das nach dem Auswählen eines Links im Abschnitt Betroffene Ressourcen hervorgehoben wurde" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
        Element auf der Webseite, das nach dem Auswählen eines Links im Abschnitt **"Betroffene Ressourcen"** hervorgehoben wurde
    :::image-end:::


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a>Wellenförmige Unterstreichungen in der DOM-Struktur weisen auf automatisch erkannte Probleme hin 

Die DOM-Struktur im **Elementtool** kennzeichnet Probleme direkt im HTML-Code mit wellenförmigen Unterstreichungen.  Diese Probleme werden vom **Tool "Probleme"** gemeldet.  Wenn Sie **umschalten und auf** ein Beliebiges Element mit wellenförmiger Unterstreichung klicken, wird das **Tool "Probleme"** angezeigt.

1.  Klicken Sie im Tool **"Elemente"** in der DOM-Struktur **umschalten+auf** das `<input type="search">` Element, das eine wellenförmige Linie unter `input` sich hat.  Das **Tool "Probleme"** wird angezeigt und zeigt das Problem für dieses Element an.

    :::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Ein Element mit einer wellenförmigen Unterstreichung in der DOM-Ansicht hat ein Problem" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
        Ein Element mit einer wellenförmigen Unterstreichung in der DOM-Ansicht hat ein Problem
    :::image-end:::


## <a name="see-also"></a>Weitere Informationen

*  [Suchen und Beheben von Problemen mit dem Tool "Probleme"][DevToolsIssuesTool]
*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsIssuesTool]: ../issues/index.md "Suchen und Beheben von Problemen mithilfe des Tools &quot;Probleme&quot; | Microsoft-Dokumente"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
