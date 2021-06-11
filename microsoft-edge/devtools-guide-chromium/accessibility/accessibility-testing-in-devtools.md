---
description: Erste Schritte beim Testen von Barrierefreiheitsproblemen mit DevTools
title: Übersicht über Barrierefreiheitstests mit DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 50661f68c7b3269d003bdc25f6a8098ae0e3ec89
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597481"
---
# <a name="overview-of-accessibility-testing-using-devtools"></a>Übersicht über Barrierefreiheitstests mit DevTools

In diesem Artikel behandeln wir einige der Features, die Sie in DevTools verwenden können, um auf Barrierefreiheitsprobleme zu testen.  Wir durchgehen die Verwendung verschiedener Features von DevTools, um Barrierefreiheitsprobleme auf einer Demoseite zu erkennen, und wir besprechen, wie sie behoben werden können.  Öffnen Sie die [Demoseite][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte, um sie selbst auszuprobieren, und Testen Sie mit.

:::image type="complex" source="../media/a11y-testing-basics-demopage.msft.png" alt-text="Die in diesem Artikel verwendete Demoseite mit einigen Barrierefreiheitsproblemen" lightbox="../media/a11y-testing-basics-demopage.msft.png":::
    Die in diesem Artikel verwendete Demoseite mit einigen Barrierefreiheitsproblemen
:::image-end:::


## <a name="automated-testing-by-using-the-issues-tool"></a>Automatisierte Tests mithilfe des Tools "Probleme"

Wenn Sie die Demoseite im Browser öffnen und DevTools öffnen, beachten Sie, dass einige Probleme automatisch im **Problemzähler**erkannt werden.  Wählen Sie den **Problemindikator** \( ![ Problemzähler ](../media/issues-counter-icon.msft.png) \) aus, um das [Problemtool][DevToolsIssuesTool] zu öffnen, um die Probleme und weitere Informationen anzuzeigen.

:::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="Der Problemindikator zeigt, wie viele Probleme auf der aktuellen Webseite vorhanden sind, und öffnet das Tool Probleme." lightbox="../media/a11y-testing-issues-tracker.msft.png":::
    Der Problemindikator zeigt, wie viele Probleme auf der aktuellen Webseite vorhanden sind, und öffnet das Tool "Probleme".
:::image-end:::

In diesem Artikel konzentrieren wir uns auf den Abschnitt **"Barrierefreiheit"** des **Tools "Probleme".**

:::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Warnungen zur Barrierefreiheit, die im Tool Probleme angezeigt werden" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
    Warnungen zur Barrierefreiheit, die im Tool "Probleme" angezeigt werden
:::image-end:::

Für ausführliche exemplarische Vorgehensweisen navigieren Sie zum [Abschnitt "Barrierefreiheit" des Tools "Probleme".][DevToolsAccessibilityTestIssuesToolViewAccSection]


### <a name="automatically-checking-that-input-fields-have-labels"></a>Automatische Überprüfung, ob Eingabefelder Bezeichnungen aufweisen

Die erste angezeigte Warnung ist `Form elements must have labels: Element has no title attribute. Element has no placeholder attribute` .  Wenn Sie diesen Abschnitt erweitern und dann den Link **"In Elementen öffnen"** auswählen, wird **das** Elementtool geöffnet, wobei das Element in der DOM-Struktur hervorgehoben ist.  Auf der Registerkarte **"Formatvorlagen"** wird das CSS angezeigt, das auf das Element angewendet wird.

Für detaillierte exemplarische Vorgehensweisen navigieren Sie zu [Überprüfen, ob Eingabefelder Beschriftungen aufweisen.][DevtoolsAccessibilityTestIssuesToolCheckFieldsLabels]

:::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Elementtool, das den problematischen HTML-Code zeigt, nachdem der Link im Tool Probleme ausgewählt wurde" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
    Elementtool, das den problematischen HTML-Code zeigt, nachdem der Link im Tool "Probleme" ausgewählt wurde
:::image-end:::

In diesem Fall weist der HTML-Code ein `label` Element auf, das nicht funktioniert.

```html
<label>Search</label>
<input type="search">
<input type="submit" value="go">
```

Die Verwendung des `label` Elements hier ist falsch, da es keine Verbindung zwischen dem `label` Element und dem Element `input` gibt.  Eine gültige HTML-Bezeichnung würde den Fokus auf das Sucheingabetextfeld setzen, wenn Sie die **Suchbezeichnung** auswählen. 

Sie können dieses Problem beheben, indem Sie entweder das Element in einem Element verschachteln `input` `label` oder ein Attribut hinzufügen, das auf `for` ein Attribut des Elements `id` `input` verweist.  Um eine korrekte Verbindung anzuzeigen, wählen Sie die Bezeichnung **"Andere"** auf dem Formular für die Gabe aus.

Sie können auch die erläuternden Links im **Tool "Probleme"** auswählen, um diese Informationen abzurufen.

:::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Links im Problemtool, die auf ausführlichere Informationen zu dem Problem verweisen" lightbox="../media/a11y-testing-more-information-links.msft.png":::
    Links im **Problemtool,** die auf ausführlichere Informationen zu dem Problem verweisen
:::image-end:::


### <a name="automatically-checking-that-images-have-alt-text"></a>Automatische Überprüfung, ob Bilder alternativtext aufweisen

Das andere automatisch erkannte Problem besteht darin, dass viele der Bilder auf der Seite keinen alternativen Text haben.  Wenn Sie die `Images must have alternate text: Element has no title attribute` Warnung erweitern, erhalten Sie vier Instanzen von Bildern mit diesem Problem.

:::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="Das Tool Probleme, das Bilder mit fehlendem alternativen Text meldet" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
    Das **Tool "Probleme",** das Bilder mit fehlendem alternativen Text meldet
:::image-end:::

Für ausführliche exemplarische Vorgehensweisen navigieren Sie zu [Überprüfen, ob Bilder alternativ text][DevtoolsAccessibilityTestIssuesToolCheckAltText]aufweisen.


### <a name="automatically-checking-that-text-colors-have-enough-contrast"></a>Automatische Überprüfung, ob Textfarben über genügend Kontrast verfügen

Das Tool **"Probleme"** meldet auch, wenn zwei Elemente auf der Seite nicht über genügend Kontrast verfügen.

:::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Im Tool Probleme gemeldete Kontrastprobleme" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
    Im Tool **"Probleme"** gemeldete Kontrastprobleme
:::image-end:::

Das Tool **"Probleme"** enthält ausführliche Erläuterungen zur Warnung.  Wenn Sie einen Drilldown ausführen, erhalten Sie eine Liste der Elemente, die dieses Problem aufweisen.  Wenn Sie im Tool **"Probleme"** einen Link auswählen, der auf ein Element zeigt, wird dieses Element auf der gerenderten Seite hervorgehoben.

:::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Element auf der Seite, das nach der Auswahl des Links hervorgehoben wurde" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
    Element auf der Seite, das nach der Auswahl des Links hervorgehoben wurde
:::image-end:::

Für ausführliche exemplarische Vorgehensweisen navigieren Sie zu [Überprüfen, ob Textfarben genügend Kontrast aufweisen.][DevtoolsAccessibilityTestIssuesToolCheckContrast]


### <a name="verify-that-the-webpage-layout-is-usable-when-narrow"></a>Stellen Sie sicher, dass das Webseitenlayout verwendet werden kann, wenn es schmal ist.

<!-- by design, this section doesn't have a corresponding how-to article -->

Ein wichtiger Bestandteil der Barrierefreiheit besteht darin, sicherzustellen, dass Ihre Webprodukte auf einem schmalen Viewport gut funktionieren. Viele Benutzer müssen die Seite zoomen, um sie verwenden zu können. Dies bedeutet, dass nicht mehr viel Platz vorhanden ist. Wenn nicht genügend Platz vorhanden ist, sollte das mehrspaltige Layout in ein einspaltiges Layout umgewandelt werden, wobei der Inhalt in einer verständlichen Reihenfolge platziert wird. Dies bedeutet, dass sie den wichtigsten Inhalt oben auf der Seite platzieren und zusätzliche Inhalte weiter unten auf der Seite platzieren.

Indem Sie das Browserfenster eingrenzen und die Pfeiltasten zum Scrollen der Seite verwenden, können Sie sehen, dass die obere Navigationsleiste der Demoseite einige Probleme mit der Barrierefreiheit aufweist.  Die obere Navigationsleiste überlappt das **Suchformular,** wie im vorherigen Bild dargestellt, und dieses Problem muss behoben werden.

Sie können einen schmalen Viewport simulieren, indem Sie die Größe des Browserfensters ändern. Eine bessere Möglichkeit zum Testen der Reaktionsfähigkeit Ihres Designs ist jedoch die Verwendung des **Geräteemulationstools.**  Hier sind einige Features des **Geräteemulationstools,** die Ihnen helfen, Barrierefreiheitsprobleme jeder Website zu finden:

*  Ändern Sie die Größe des Browserfensters nicht, ändern Sie die Größe der Seite, und testen Sie, ob Ihre [CSS-Medienabfragen][DevToolsMediaQueries] eine Änderung des Layouts auslösen.
*  Suchen Sie nach Abhängigkeiten, die eine Maus verwenden. Standardmäßig wird bei der Geräteemulation von einem Touchgerät ausgegangen. Dies bedeutet, dass alle Funktionen Ihres Produkts, die auf Hoverinteraktion basieren, nicht funktionieren. 
*  Führen Sie visuelle Tests durch, indem Sie verschiedene Geräte, Zoomstufen und Pixelverhältnisse simulieren.
*  Testen Sie, wie sich Ihr Produkt bei unzuverlässigen Verbindungen verhält oder wenn der Benutzer offline ist.  Das Anzeigen der wichtigsten Interaktionen für einen Benutzer bei einer langsamen Verbindung ist ebenfalls eine Barrierefreiheitsüberlegung.

Um mehr über das **Geräteemulationstool** zu erfahren, navigieren Sie zu [Emulieren mobiler Geräte in Microsoft Edge DevTools][DevToolsDeviceModeIndex].


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a>Wellenförmige Unterstreichungen in der DOM-Struktur weisen auf automatisch erkannte Probleme hin

Die DOM-Struktur im **Elementtool** kennzeichnet Probleme automatisch direkt im HTML-Code, indem eine wellenförmige Unterstreichung hinzugefügt wird.  Wenn Sie `Shift` + `click` ein Element mit wellenförmiger Unterstreichung verwenden, wird das Tool **"Probleme"** geöffnet.

:::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Ein Element, das mit wellenförmiger Unterstreichung in der DOM-Struktur angezeigt wird, hat Probleme.  Umschalt+Klicken auf das Element, um direkt zum Problem zu gelangen" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
    Ein Element, das mit wellenförmiger Unterstreichung in der DOM-Struktur angezeigt wird, hat Probleme.  `Shift`+`click` das Element, um direkt zum Problem zu gelangen.
:::image-end:::

Diese Probleme, die vom Tool **"Probleme"** gefunden wurden, sind einige relativ offensichtliche Barrierefreiheitsprobleme, die vermieden werden können.  Wenn Sie das Tool **"Probleme"** und die zugehörigen geführten Erläuterungen verwenden, um sie zu beheben, sind Sie auf dem Weg zu einem barrierefreien Produkt.


## <a name="limits-of-automated-testing"></a>Grenzwerte für automatisierte Tests

Das [Tool "Probleme",][DevToolsIssuesTool] ["Accessibility Insights"][AccessibilityInsights]und ["Debugging"][Lighthouse] sind Tools, die automatisch einen Barrierefreiheitsbericht für eine Webseite generieren.  Das Abrufen eines automatisierten Berichts aus diesen Tools ist nur der Anfang Ihrer Reise zum Testen der Barrierefreiheit.

Bei der Barrierefreiheit geht es um menschliche Interaktionen – Personen mit unterschiedlichen Anforderungen, die Ihre Produkte in verschiedenen technischen Umgebungen verwenden.  Diese Tests können nicht vollständig automatisiert werden, müssen jedoch von einem Benutzer überprüft werden, der durch das Produkt navigiert.  Im besten Szenario hätten Sie Zugriff auf Tester mit unterschiedlichen Barrierefreiheitsanforderungen und Tester in verschiedenen Umgebungen.  Sie können jedoch bereits viel selbst tun, indem Sie die Tastatur verwenden, um zu navigieren, und indem Sie verschiedene Teile der Seite überprüfen.

Auf der Demoseite gibt es zusätzliche Probleme, die automatisierte Tests nicht erkennen können, einschließlich: 

*  Probleme, die nach der Interaktion mit der Seite auftreten. 
*  Probleme im Zusammenhang mit Änderungen an der Anzeige, z. B. das Eingrenzen des Fensters.

Eines dieser Probleme ist das Schenkungsformular.  Wenn Sie eine Maus verwenden, können Sie auf die verschiedenen Optionen klicken, um Geld zu verdienen.  Wenn Sie jedoch versuchen, über die Tastatur auf das Gabeformular zuzugreifen, passiert nichts. Um dieses Problem zu lösen, müssen Sie das **Inspect-Tool** verwenden.

:::image type="complex" source="../media/a11y-testing-basics-donation-form-issue.msft.png" alt-text="Das Schenkungsformular auf der Demoseite ist hervorgehoben" lightbox="../media/a11y-testing-basics-donation-form-issue.msft.png":::
    Das Schenkungsformular auf der Demoseite ist hervorgehoben
:::image-end:::


## <a name="using-the-inspect-tool-to-detect-accessibility-issues"></a>Verwenden des Inspect-Tools zum Erkennen von Barrierefreiheitsproblemen

Verwenden **** Sie das Inspect-Tool, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf Teile der Webseite zeigen.  Das Tool **Inspect** \( ![ Inspect ](../media/inspect-icon.msft.png) \) befindet sich in der oberen linken Ecke von DevTools.  Aktivieren Sie das Tool "Überprüfen", indem Sie die Schaltfläche "Tool **überprüfen"** auswählen.

:::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Aktivieren Sie das Tool Überprüfen, indem Sie auf die Schaltfläche Tool überprüfen klicken." lightbox="../media/a11y-testing-basics-inspector.msft.png":::
    Aktivieren Sie das **Tool "Überprüfen",** indem Sie auf die Schaltfläche "Tool **überprüfen"** klicken.
:::image-end:::

Nachdem Sie die Schaltfläche des Tools **Inspect** ausgewählt haben, können Sie den Zeiger über ein beliebiges Element auf der gerenderten Seite bewegen.  Das Tool Inspect zeigt das Layout des Elements als mehrfarbige Flexboxüberlagerung und Elementdetails als Informationsüberlagerung ähnlich einer QuickInfo an.

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Mehrfarbige Flexboxüberlagerung und Informationsüberlagerung bei Verwendung des Inspect-Tools" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    Mehrfarbige Flexboxüberlagerung und Informationsüberlagerung bei Verwendung des **Inspect-Tools**
:::image-end:::

Der Abschnitt **"Barrierefreiheit"** des Tools "Inspect" enthält ggf. eine **Kontrastlinie.**

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="Der Abschnitt Barrierefreiheit des Tools Inspect enthält ggf. eine Kontrastlinie." lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    Der Abschnitt **"Barrierefreiheit"** des Tools "Inspect" enthält ggf. eine **Kontrastlinie.**
:::image-end:::

Für ausführliche exemplarische Vorgehensweisen navigieren Sie zur [Identifizierung geschachtelter Regionen mithilfe der Farbhervorhebung.][DevtoolsAccessibilityTestInspectToolColorHighlighting]
<!-- = test-inspect-tool.md##identify-nested-regions-using-color-highlighting -->

Im oberen Abschnitt der Informationsüberlagerung des **Tools "Inspect"** werden die folgenden Informationen angezeigt:

* Layouttyp; wenn das Element mit einem Flexbox- oder Raster positioniert wird, wird ein entsprechendes Symbol \(![Rasterlayoutsymbol](../media/grid-icon.msft.png)\).
* Der Name des Elements, z. B. **ein**, **h1**oder **div**.
* Die Abmessungen des Elements in Pixel.
* Die Farbe als Farbmuster (kleines, farbiges Quadrat) und als formatierter Wert (z. B. `#336699` ).
* Schriftinformationen (Schriftgrad und Schriftfamilien).
* Rand und Abstand in Pixel.

Der **Barrierefreiheitsteil** der **Inspect-Überlagerung** wird im folgenden Abschnitt beschrieben.


### <a name="checking-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a>Überprüfen einzelner Elemente auf Textkontrast, Sprachausgabetext und Tastaturunterstützung

Der Abschnitt **"Barrierefreiheit"** **der** Inspect-Überlagerung enthält die folgenden Zeilen:

*   **Der Kontrast** definiert, ob ein Element von Personen mit eingeschränkter Sehkraft verstanden werden kann.
    *   Das in den [WCAG-Richtlinien][WCAG] definierte [Kontrastverhältnis][W3CContrastRatio] gibt an, ob genügend Kontrast zwischen Text- und Hintergrundfarben vorhanden ist.  Ein grünes Häkchensymbol zeigt an, dass genügend Kontrast vorhanden ist, und ein orangefarbenes Ausrufezeichensymbol zeigt an, dass nicht genügend Kontrast vorhanden ist.

*   **Name** und **Rolle** geben an, welche Information assistive technology, z. B. Bildschirmleseprogramme, über das Element berichten.
    *   Der **Name** ist der Textinhalt eines `a` Elements.  Für das Element `<a href="/">About Us</a>` lautet der im Inspect-Tool angezeigte **Name** "Über uns".
    *   Die **Rolle** des Elements.  Die **Rolle** ist in der Regel der Elementname, z. `article` B. , oder `img` `link` `heading` .  The `div` and elements are represented as `span` `generic` .

*   **Tastaturfokussierbar** gibt an, ob Benutzer das Element mit anderen Eingabegeräten als einer Maus erreichen können.
    *   Ein grünes Häkchensymbol weist darauf hin, dass das Element tastaturfokussierbar ist.
    *   Ein grauer Kreis mit diagonaler Linie weist darauf hin, dass das Element nicht tastaturfokussierbar ist.

Für ausführliche exemplarische Vorgehensweisen navigieren Sie zu [Check individual elements for text contrast, screen reader text, and keyboard support.][DevtoolsAccessibilityTestInspectToolIndivElems]
<!-- = test-inspect-tool.md#check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support -->


### <a name="using-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a>Verwenden des Inspect-Tools zum Bewegen des Mauszeigers über die Webseite, um das DOM und CSS hervorzuheben

Wenn Sie das **Tool Inspect** verwenden, wird durch Auswählen eines Elements auf der gerenderten Seite **das** Elementtool geöffnet.  Die DOM-Struktur zeigt den HTML-Code des Elements, und **Styles** zeigt die CSS-Eigenschaften, die auf das Element angewendet werden.

:::image type="complex" source="../media/a11y-testing-basics-inspector-selected-element.msft.png" alt-text="Details zum ausgewählten Element, das im Elementtool angezeigt wird" lightbox="../media/a11y-testing-basics-inspector-selected-element.msft.png":::
    Details zum ausgewählten Element, das im Elementtool angezeigt wird
:::image-end:::

Wenn Sie mit dem **Inspect-Tool** auf verschiedene Teile der gerenderten Seite zeigen, während **Elemente** geöffnet sind, werden Sie feststellen, dass die DOM-Struktur automatisch aktualisiert wird.

Für ausführliche exemplarische Vorgehensweisen navigieren Sie zum [Verwenden des Inspect-Tools, um mit dem Mauszeiger über die Webseite zu zeigen, um DOM und CSS hervorzuheben.][DevtoolsAccessibilityTestInspectToolDomCss]
<!-- = test-inspect-tool.md#use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css -->


## <a name="verify-keyboard-support-by-using-the-tab-and-enter-keys"></a>Überprüfen der Tastaturunterstützung mithilfe der Tabulator- und Eingabetasten

Nicht alle Personen verwenden Zeiger- oder Touchgeräte, und einige Personen haben möglicherweise eine sehschwächeren Blick. Um diese Szenarien zu unterstützen, stellen Sie sicher, dass Benutzeroberflächen mit Tastaturen funktionieren.

Sie können die Verwendung einer Tastatur testen, um auf der Seite zu navigieren, indem Sie `Tab` von Element zu Element `Shift+Tab` springen.  Wenn Sie `Tab` auf die Demoseite drücken, erhält zuerst das **Suchformular** in der Kopfzeile der Seite den Fokus.  Durch Drücken des Formulars `Enter` können Sie sogar das Formular übermitteln, damit es funktioniert, trotz des Bezeichnungsproblems, das wir zuvor bei der Verwendung des Tools **"Probleme"** entdeckt haben.

Für ausführliche exemplarische Vorgehensweisen navigieren Sie [mithilfe der Tab- und Eingabetasten zu "Überprüfen auf Tastaturunterstützung".](test-tab-enter-keys.md)

Wenn Sie `Tab` stattdessen `Enter` drücken, ist das nächste Element, das den Fokus erhält, der erste **Link "Mehr"** im Inhaltsbereich der Seite, wie durch eine Gliederung angegeben.

:::image type="complex" source="../media/a11y-testing-keyboard-focus-on-element.msft.png" alt-text="Navigieren auf der Seite mithilfe der Tabulatortaste.  Der Fokus wird auf einem Link Mehr auf der Seite angezeigt." lightbox="../media/a11y-testing-keyboard-focus-on-element.msft.png":::
    Navigieren auf der Seite mithilfe des `Tab` Schlüssels.  Der Fokus wird auf einem **Link "Mehr"** auf der Seite angezeigt.
:::image-end:::

Nachdem Sie den letzten Link **"Mehr"** eingefügt haben, wird der Bildlauf nach oben ausgeführt, und es ist unklar, welches Element den Fokus hat.

Wenn Sie links unten auf dem Bildschirm suchen oder eine Sprachausgabe verwenden, können Sie feststellen, dass der blaue **Katzenlink** im Navigationsmenü der Seitenleiste den Fokus hat, da der Browser die URL `#cats` anzeigt.

:::image type="complex" source="../media/a11y-testing-lack-of-focus-style.msft.png" alt-text="Eine fehlende Fokusformatierung macht es unmöglich, zu wissen, wo Sie sich derzeit auf der Seite befinden.  Der einzige Hinweis ist die Anzeige des Linkziels in der unteren linken Ecke des Fensters." lightbox="../media/a11y-testing-lack-of-focus-style.msft.png":::
    Eine fehlende Fokusformatierung macht es unmöglich, zu wissen, wo Sie sich derzeit auf der Seite befinden.  Der einzige Hinweis ist die Anzeige des Linkziels in der unteren linken Ecke des Fensters.
:::image-end:::

Wenn `Tab` Sie erneut auswählen, gelangen Sie in das Eingabetextfeld des Gabeformulars.  Sie können jedoch nicht die **Schaltflächen 50,** **100** oder **200** über dem Eingabetextfeld erreichen.  Wenn der Fokus auf diesem Eingabetextfeld liegt, sendet die Auswahl `Enter` das Formular nicht.

:::image type="complex" source="../media/a11y-testing-form-field-with-outline.msft.png" alt-text="Das einzige Element, auf das über die Tastatur zugegriffen werden kann, im Gabeformular ist das Eingabetextfeld." lightbox="../media/a11y-testing-form-field-with-outline.msft.png":::
    Das einzige Element, auf das über die Tastatur zugegriffen werden kann, im Formular für die Gabe ist das Textfeld.
:::image-end:::

Wenn Sie `Tab` erneut auswählen, wird der Fokus auf der oberen Navigationsleiste platziert, in der Sie `Enter` zu einem anderen Abschnitt der Seite oder zu einer anderen Seite der Website wechseln können.  Sie wissen, auf welchem Element Sie sich befinden, da es eine Fokusgliederung gibt.  Um einen Link in der oberen Navigationsleiste auszuwählen, verwenden `Tab` Oder setzen Sie den Fokus auf einen `Shift+Tab` Link, und wählen Sie dann `Enter` aus.

:::image type="complex" source="../media/a11y-testing-menu-with-outline.msft.png" alt-text="Die obere Navigationsleiste weist eine Hervorhebung und eine Fokusgliederung auf und ist daher über die Tastatur zugänglich." lightbox="../media/a11y-testing-menu-with-outline.msft.png":::
    Die obere Navigationsleiste weist eine Hervorhebung und eine Fokusgliederung auf und ist daher über die Tastatur zugänglich.
:::image-end:::

Wir haben hier einige Probleme gefunden, um Folgendes zu beheben:

* Das Navigationsmenü auf der Seitenleiste zeigt benutzern nicht an, wo der `Tab` Fokus liegt, wenn sie Tastaturen verwenden, um sich auf der Seite zu bewegen.
* Auf dem Schenkungsformular funktionieren die Schaltflächen **50, 100, ** und **200** sowie die Funktion zum Übermitteln des Formulars bei Verwendung der Tastatur nicht.
* Die Aktivierreihenfolge der Tastatur ist falsch. Die `Tab` Taste navigiert durch alle **"Mehr"-Links** auf der Seite vor dem Navigationsmenü in der Seitenleiste.  Diese `Tab` Reihenfolge ist nicht hilfreich, da sie mit der Seitenleistennavigation zu den verschiedenen Abschnitten dieser Seite führen soll. 

Lassen Sie uns diese Probleme mit DevTools analysieren.


## <a name="analyze-keyboard-accessibility-issues-using-devtools"></a>Analysieren von Problemen bei der Barrierefreiheit von Tastaturen mit DevTools


### <a name="analyzing-the-lack-of-indication-of-keyboard-focus-in-the-sidebar-menu"></a>Analysieren der fehlenden Anzeige des Tastaturfokus im Randleistenmenü

Um herauszufinden, warum die Seitenleistennavigation nicht wie erwartet für die Verwendung mit Tastaturen optimiert ist, verwenden Sie zunächst das **Tool Inspect,** um einen Link im Navigationsmenü der Seitenleiste hervorzuheben, und führen Sie dann einen Drilldown in der DOM-Struktur zum `a` Element durch. 

:::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Überprüfen des Quellcodes und der angewendeten Formatvorlagen eines Links im Navigationsmenü der Seitenleiste" lightbox="../media/a11y-testing-menu-link.msft.png":::
    Überprüfen des Quellcodes und der angewendeten Formatvorlagen eines Links im Navigationsmenü der Seitenleiste
:::image-end:::

Auf der Registerkarte **"Formatvorlagen"** können Sie das CSS sehen, das auf den Link angewendet wird, und wenn Sie den Link `styles.css` auswählen, wird die Datei im **Tool "Quellen"** geöffnet.

:::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Die Formatvorlagen, die auf die Verknüpfung angewendet werden, die im Tool Quellen angezeigt werden" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
    Die Formatvorlagen, die auf die Verknüpfung angewendet werden, die im Tool "Quellen" angezeigt werden
:::image-end:::

Im obigen Beispiel enthalten die Formatvorlagen der Seite einen `hover` Status für das Menüelement, wenn Sie eine Maus verwenden, aber es gibt keinen `focus` Zustand im CSS für Tastaturbenutzer.  

Außerdem verwenden die Links in diesem Beispiel `outline: none` . Dieser Stil wird verwendet, um die Gliederung zu entfernen, die von Browsern automatisch zu Elementen hinzugefügt wird, wenn sie den Fokus haben und Tastaturen verwendet werden.  Um dieses Problem zu vermeiden, verwenden Sie nicht `outline: none` .

Für ausführliche exemplarische Vorgehensweisen navigieren Sie zu [Analysieren der fehlenden Anzeige des Tastaturfokus in einem Randleistenmenü.](test-analyze-no-focus-indicator.md)


### <a name="analyzing-the-lack-of-keyboard-support-in-the-donation-form"></a>Analysieren der fehlenden Tastaturunterstützung im Gabeformular

Die Schaltflächen auf dem Schenkungsformular werden mithilfe des `div` Elements implementiert, das von automatisierten Testtools nicht als Steuerelement eines Formulars erkannt wird.

Um dies zu untersuchen, können Sie mit dem **Inspect-Tool** auf die Schaltflächen des Schenkungsformulars zeigen.  Das Ergebnis ist, dass keine davon über die Tastatur zugänglich ist, wie durch den grauen Ring auf der **tastaturfokussierbaren** Zeile der Informationsüberlagerung angegeben.  Wie in den **Zeilen "Name"** und **"Rolle"** der Informationsüberlagerung gezeigt, haben die Schaltflächen des Schenkungsformulars auch keinen Namen und eine Rolle `generic` von (Darstellen oder `div` `span` Elemente), was bedeutet, dass sie für Hilfstechnologien nicht zugänglich sind.

:::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="Die Überprüfung der Schaltflächen des Formulars zeigt, dass auf sie nicht über die Tastatur zugegriffen werden kann." lightbox="../media/a11y-testing-donation-button-info.msft.png":::
    Die Überprüfung der Schaltflächen des Formulars zeigt, dass auf sie nicht über die Tastatur zugegriffen werden kann.
:::image-end:::

Ausführliche Exemplarische Vorgehensweisen finden Sie unter [Analysieren der fehlenden Tastaturunterstützung in einem Formular.](test-analyze-no-keyboard-support.md)

Wenn Sie auf die Schaltfläche **"Überprüfen"** klicken, gelangen Sie mit dem Tool **"Überprüfen"** zum Tool **"Elemente"** und zeigen den HTML-Code des Formulars an.

```HTML
<div class="donationrow">
    <div class="donationbutton">50</div>
    <div class="donationbutton">100</div>
    <div class="donationbutton">200</div>
</div>
<div class="donationrow">
    <label for="freedonation">Other</label>
    <input id="freedonation" class="smallinput">
</div>
<div class="donationrow">
    <div class="submitbutton">Donate</div>
</div>
```

Die Verwendung der Elemente und der `label` `input` Elemente ist gültig, was dazu führt, dass die Bezeichnung wie beabsichtigt funktioniert und auf das Textfeld über die `input` Tastatur zugegriffen werden kann.  Der Rest des Formulars verwendet `div` Elemente, die einfach zu formatieren sind, aber keine semantische Bedeutung haben.

Als Nächstes analysieren wir die JavaScript-Funktionalität des Formulars. Wählen Sie in **"Elemente"** die Registerkarte **"Ereignislistener" aus,** um das JavaScript des Formulars zu analysieren.

:::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="Registerkarte Ereignislistener mit einem Link zum JavaScript für das Formular" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
    Registerkarte **"Ereignislistener"** mit einem Link zum JavaScript für das Formular
:::image-end:::

Wählen Sie auf der Registerkarte **"Ereignislistener"** den `buttons.js:18` Link aus, um das **Tool "Quellen"** zu öffnen, und überprüfen Sie dann das JavaScript, das für die Funktionalität des Formulars verantwortlich ist.

:::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="Das JavaScript, das für die Funktionalität des Schenkungsformulars verantwortlich ist, das im Tool Quellen angezeigt wird" lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
    Das JavaScript, das für die Funktionalität des Schenkungsformulars verantwortlich ist, das im **Tool "Quellen"** angezeigt wird
:::image-end:::

Die Verwendung von `click` Ereignissen mit Schaltflächen wird empfohlen, da `click` Ereignisse sowohl mit Mauszeigern als auch mit Tastaturen funktionieren.  Da auf ein `div` Element jedoch nicht über die Tastatur zugegriffen werden kann und die Schaltfläche ** Abwendung ** als Element implementiert `div` ist, wird dieser JavaScript-Code nur ausgeführt, wenn eine Maus verwendet wird.

Die Verwendung `div` von "as a button" ist ein klassisches Beispiel, bei dem zusätzliches JavaScript erforderlich ist, um Funktionen zu erstellen, die `button` Von Elementen bereitgestellt werden. Dies führt zu einer Erfahrung, auf die nicht zugegriffen werden kann.


### <a name="checking-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a>Überprüfen der Barrierefreiheitsstruktur auf Tastatur- und Sprachausgabeunterstützung

Die Verwendung des **Inspect-Tools** zum einzelnen Überprüfen jedes Elements auf der Seite ist zeitaufwändig.  Verwenden Sie stattdessen die Registerkarte **"Barrierefreiheit",** um in der **Barrierefreiheitsstruktur**der Seite zu navigieren.  Die Barrierefreiheitsstruktur gibt an, welche Informationen die Seite für Hilfstechnologien wie Bildschirmleseprogramme bereitstellt.

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Schaltfläche Schenkungsformular in der Barrierefreiheitsstruktur" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    Schaltfläche "Schenkungsformular" in der **Barrierefreiheitsstruktur**
:::image-end:::

Jedes Element in der Struktur, das keinen Namen oder eine Rolle `generic` hat, ist ein Problem, da dieses Element für Tastaturbenutzer oder Personen, die Hilfstechnologien verwenden, nicht verfügbar ist.

Navigieren Sie für ausführliche exemplarische Vorgehensweisen zur [Überprüfung der Barrierefreiheitsstruktur für die Unterstützung von Tastatur und Sprachausgabe.](test-accessibility-tree.md)


### <a name="analyzing-the-order-of-keyboard-access-to-sections-of-the-page"></a>Analysieren der Reihenfolge des Tastaturzugriffs auf Abschnitte der Seite

Ein weiteres Problem ist die unklare Aktivierreihenfolge auf der Seite.  Tastaturbenutzer erreichen das Navigationsmenü in der Seitenleiste erst, nachdem sie alle **"Mehr"-Links** auf der gesamten Seite durchlaufen haben.  In diesem Beispiel soll das Navigationsmenü auf der Seitenleiste eine Verknüpfung mit verschiedenen Abschnitten dieser Seite sein.  Diese Aktivierreihenfolge führt zu einer schlechten Benutzererfahrung. 

Der Grund für die verwirrende `Tab` Reihenfolge ist, dass sie durch die Quellreihenfolge des Dokuments bestimmt wird.  Die Aktivierreihenfolge kann auch mithilfe des Attributs für ein Element geändert `tabindex` werden, das dieses Element aus der Standardquellreihenfolge herausnimmt.

Im Quellcode des Dokuments wird das Seitennavigationsmenü hinter dem Hauptinhalt der Seite angezeigt.  Das Navigationsmenü der Seitenleiste wird nur oberhalb des Hauptinhalts der Seite angezeigt, da das Navigationsmenü der Seitenleiste mitHILFE von CSS positioniert wurde.

Die Quellreihenfolge eines Dokuments ist für die Hilfstechnologie wichtig und kann sich von der Reihenfolge unterscheiden, in der Elemente auf der gerenderten Seite angezeigt werden.  MitHILFE von CSS können Sie Seitenelemente auf visuelle Weise neu anordnen, was jedoch nicht bedeutet, dass Hilfstechnologien wie Sprachausgabe Seitenelemente in der gleichen Reihenfolge wie diese CSS darstellen.

Sie können die Reihenfolge der Seitenelemente mithilfe der **Quellreihenfolgeanzeige** auf der **Barrierefreiheitsregisterkarte** testen.  Scrollen Sie ganz nach unten, und aktivieren Sie das Kontrollkästchen **Quellreihenfolge anzeigen.**  Wenn Sie nun in der DOM-Struktur im **Elementtool** navigieren, z. B. beim Auswählen des `header` Elements, werden numerische Überlagerungen in Abschnitten der gerenderten Seite angezeigt, die die Quellreihenfolge darstellen. 

:::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="Durch Aktivieren des Viewers für die Quellreihenfolge wird die Reihenfolge der Elemente im Quellcode als numerische Überlagerungen auf der Seite angezeigt." lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
    Durch Aktivieren des Viewers für die **Quellreihenfolge** wird die Reihenfolge der Elemente im Quellcode als numerische Überlagerungen auf der Seite angezeigt.
:::image-end:::

Ausführliche exemplarische Vorgehensweisen finden Sie unter [Testen der Tastaturunterstützung mithilfe der Source Order Viewer](test-tab-key-source-order-viewer.md).


## <a name="testing-contrast-of-text-colors-in-various-states"></a>Testen des Kontrasts von Textfarben in verschiedenen Zuständen

Das **Tool Inspect** meldet Barrierefreiheitsprobleme für jeweils einen Status.  Zunächst beschreiben wir die Einschränkung der Verwendung des Inspect-Tools, um nur den statischen Zustand eines Seitenelements anzuzeigen.  Anschließend wird erläutert, wie andere Zustände eines Seitenelements überprüft werden, indem auf der Registerkarte **"Formatvorlagen"** die Option **\:hov (Toggle Element State)** ausgewählt wird.

### <a name="checking-text-color-contrast-in-the-default-state"></a>Überprüfen des Textfarbkontrasts im Standardzustand

Zusätzlich zu den automatischen Farbkontrasttests im Tool **"Probleme"** können Sie auch das **Tool Inspect** verwenden, um zu überprüfen, ob einzelne Seitenelemente über genügend Kontrast verfügen.  Wenn Kontrastinformationen verfügbar **** sind, zeigt die Inspect-Überlagerung das Kontrastverhältnis und ein Kontrollkästchenelement an.  Ein grünes Häkchensymbol zeigt an, dass genügend Kontrast vorhanden ist, und ein gelbes Warnsymbol zeigt an, dass nicht genügend Kontrast vorhanden ist.

Beispielsweise haben die Links im Navigationsmenü der Seitenleiste genügend Kontrast, das grüne **Listenelement "Hunde"** im Abschnitt **"Schenkungsstatus"** jedoch nicht.  Ein Element, das nicht über genügend Kontrast verfügt, **** wird durch eine Warnung in der Inspect-Überlagerung gekennzeichnet.

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Die Links im Navigationsmenü der Seitenleiste weisen ausreichend Kontrast auf, wie in der Inspect-Überlagerung dargestellt." lightbox="../media/a11y-testing-enough-contrast.msft.png":::
            Die Links im Navigationsmenü der Seitenleiste weisen **** ausreichend Kontrast auf, wie in der Inspect-Überlagerung dargestellt. :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Ein Element, das nicht über genügend Kontrast verfügt, wird durch eine Warnung in der Inspect-Überlagerung gekennzeichnet." lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
            Ein Element, das nicht über genügend Kontrast verfügt, **** wird durch eine Warnung in der Inspect-Überlagerung gekennzeichnet. :::image-end:::
    :::column-end:::
:::row-end:::

Die Verwendung des **Inspect-Tools** auf diese Weise testet Ihre Elemente nicht vollständig. Elemente auf der Seite können unterschiedliche Zustände aufweisen, die alle getestet werden müssen. Wenn Sie z. B. mit der Maus auf das Navigationsmenü in der Seitenleiste zeigen, beachten Sie die Animation, die die Farbe der Links ändert.

:::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="Das Menüelement mit unterschiedlichen Farben, wenn sich der Mauszeiger darüber befindet" lightbox="../media/a11y-testing-hover.msft.png":::
    Das Menüelement mit unterschiedlichen Farben, wenn sich der Mauszeiger darüber befindet
:::image-end:::

### <a name="verify-accessibility-of-all-states-of-elements-such-as-the-contrast-on-hover"></a>Überprüfen der Barrierefreiheit aller Zustände von Elementen, z. B. des Kontrasts beim Daraufzeigern

Bei Verwendung der DevTools müssen Sie alle Zustände Ihres Elements simulieren, da das **Tool Inspect** nicht gleichzeitig Informationen für alle Zustände anzeigt. In diesem Beispiel können Sie bei Verwendung des **Inspect-Tools** den `hover` Status des Katzenlinks im Navigationsmenü der Seitenleiste nicht erreichen, um das Kontrastverhältnis in einem Zustand zu **** `hover` analysieren, da der Status in Ihren `hover` Formatvorlagen nicht ausgelöst wird.  Stattdessen müssen Sie den Status des **Menüelements "Katzen"** mithilfe der Zustandssimulation auf der Registerkarte **"Formatvorlagen"** simulieren.

Für ausführliche exemplarische Vorgehensweisen navigieren Sie zu [Überprüfen der Barrierefreiheit aller Zustände von Elementen.](test-inspect-states.md)

Aktivieren Sie das **Tool Inspect,** und wählen Sie dann auf der gerenderten Seite den **blauen** Katzenlink im Navigationsmenü der Seitenleiste aus.  Das **** Elementtool wird geöffnet, wobei das `a` Element in der DOM-Struktur ausgewählt ist.  Navigieren Sie bei Bedarf in der DOM-Struktur zu dem Element, das einen `hover` Status im CSS aufweist.  In diesem Fall weist das `a` Element einen `hover` Status auf.

:::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Überprüfen des Elements mit einem Hoverstatus im Elementtool" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
    Überprüfen des Elements mit einem Hoverstatus im Elementtool
:::image-end:::

Wählen Sie auf der Registerkarte **"Formatvorlagen"** die Schaltfläche **\:hov (Toggle Element State)** aus.  Verwenden Sie dann die Kontrollkästchen zum Erzwingen des **Elementstatus,** um auszuwählen, welcher Zustand simuliert werden soll.

:::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="Das Statussimulationsfeature mit allen Optionen" lightbox="../media/a11y-testing-state-simulation.msft.png":::
    Das Statussimulationsfeature mit allen Optionen
:::image-end:::

Aktivieren Sie das **Kontrollkästchen \:hover.**  Neben dem DOM-Element wird nun ein gelber Punkt angezeigt, der angibt, dass das DOM-Element einen simulierten Zustand aufweist.  Außerdem wird **der** Katzenlink im Navigationsmenü der Seitenleiste jetzt auf der Seite hervorgehoben, als würde der Mauszeiger darauf zeigen.

:::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulieren einen Hoverzustand" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
    DevTools simulieren einen Hoverzustand
:::image-end:::

Nachdem der simulierte Zustand angewendet wurde, können Sie das **Tool Inspect** erneut verwenden, um den Kontrast des Elements zu überprüfen, wenn der Benutzer mit dem Mauszeiger darauf zeigt.  In diesem Fall ist der Kontrast nicht hoch genug.

:::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Testen des Kontrasts eines Elements in einem simulierten Hoverzustand" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
    Testen des Kontrasts eines Elements in einem simulierten Hoverzustand
:::image-end:::

Die Zustandssimulation ist auch eine gute Möglichkeit, um zu überprüfen, ob Sie unterschiedliche Benutzeranforderungen berücksichtigt haben.  Im Navigationsmenü der Seitenleiste können Sie feststellen, dass der `:focus` Zustand ein Kontrastproblem aufweist.


## <a name="use-the-rendering-tool-to-test-accessibility-for-visual-impairment"></a>Verwenden des Renderingtools zum Testen der Barrierefreiheit für Sehschwächen

### <a name="check-contrast-issues-with-dark-theme-and-light-themes"></a>Überprüfen von Kontrastproblemen mit dunklem Design und hellen Designs

Eine weitere Überlegung in Bezug auf die Barrierefreiheit von Farben besteht darin, dass es möglicherweise unterschiedliche Designs gibt, die Sie auf Kontrastprobleme testen müssen.  Die meisten Betriebssysteme verfügen über einen dunklen und einen hellen Modus.  Ihre Webseite kann mithilfe von CSS-Medienabfragen auf diese unterschiedlichen Einstellungen reagieren.

Diese Demoseite hat ein helles und dunkles Design.  Sie können beide Designs testen, ohne das Betriebssystem zu ändern, indem Sie im **Rendering-Tool** die Simulation des [dunklen oder hellen Farbschemas][DevToolsColorSchemeSimulation] verwenden.  Bisher wurde in diesem Artikel die Demoseite mit einem Betriebssystem mit einer dunklen Designeinstellung betrachtet.  Wenn wir stattdessen ein Lichtschema simulieren und dann die Seite aktualisieren, zeigt das Tool **Probleme** sechs Farbkontrastprobleme anstelle von zwei an.

Für ausführliche exemplarische Vorgehensweisen navigieren Sie zu ["Auf Kontrastprobleme mit dunklem Design und hellem Design](test-dark-mode.md)prüfen".


Beachten Sie beim Wechsel zu einem hellen Design im **Renderingtool** die folgenden Elemente.

*  Neue Kontrastprobleme werden aufgrund der Änderung des hellen Designs erkannt.
*  Der gesamte **Abschnitt "Schenkungsstatus"** der Seite kann im Lichtmodus nicht gelesen werden.

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Neue Kontrastprobleme aufgrund der Änderung des hellen Designs erkannt" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
            Neue Kontrastprobleme aufgrund der Änderung des hellen Designs erkannt :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="Die Als Kontrastprobleme gekennzeichneten Schenkungsstatuselemente im Lichtmodus" lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
            Die Als Kontrastprobleme gekennzeichneten Schenkungsstatuselemente im Lichtmodus :::image-end:::
    :::column-end:::
:::row-end:::


### <a name="verify-that-the-webpage-is-usable-by-people-with-color-blindness"></a>Stellen Sie sicher, dass die Webseite von Personen mit Farbenblindheit verwendet werden kann.

Die verschiedenen Schenkungszustände verwenden Farbe (Rot, Grün, Gelb) als einzige Methode, um zwischen den Zuständen der Bereitstellung zu unterscheiden.  Sie können jedoch nicht erwarten, dass alle Ihre Benutzer diese Farben wie beabsichtigt sehen.  Wenn Sie die Emulationsfunktion für [Sehschwächen][DevToolsVisionDeficiencies] von DevTools verwenden, können Sie feststellen, dass dies nicht gut genug ist, indem Sie simulieren, wie Personen mit einer anderen Vision Ihr Design wahrnehmen würden.
Für ausführliche exemplarische Vorgehensweisen navigieren Sie zu [Überprüfen, ob die Seite von Personen mit Farbenblindheit verwendet werden kann.](test-color-blindness.md)
:::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Das Anzeigen der Seite als Person mit Protanopie (roter Farbenblindheit) würde sie sehen." lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
    Anzeigen der Seite, als ob jemand mit Protanopie (roter Farbenblindheit) sie sehen würde
:::image-end:::



### <a name="verify-that-the-webpage-is-usable-with-blurred-vision"></a>Überprüfen, ob die Webseite mit verschwommener Sehkraft verwendet werden kann

Ein weiteres interessantes Feature des **Renderingtools** ist, dass Sie verschwommenes Sehen simulieren können.  Wenn wir die Option **"Verschwommenes Sehen"** aus der Dropdownliste **"Sehschwächen emulieren"** auswählen, können wir sehen, dass der Schlagschatten im Text im oberen Menü das Lesen der Menüelemente erschwert.
Für ausführliche exemplarische Vorgehensweisen navigieren Sie zu [Überprüfen, ob die Seite mit verschwommener Vision verwendet werden kann.](test-blurred-vision.md)

:::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="Das Simulieren einer verschwommenen Seite kann Barrierefreiheitsprobleme aufdecken." lightbox="../media/a11y-testing-simulating-blur.msft.png":::
    Das Simulieren einer verschwommenen Seite kann Barrierefreiheitsprobleme aufdecken.
:::image-end:::


### <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off-reduced-motion"></a>Stellen Sie sicher, dass die Seite mit deaktivierter UI-Animation verwendet werden kann (reduzierte Bewegung)

Eine weitere Einstellung, die in diesen Tagen für Betriebssysteme verfügbar ist, ist eine Möglichkeit, Animationen zu deaktivieren.  Animationen können zur Benutzerfreundlichkeit eines Produkts beitragen, können aber auch viele Probleme verursachen, von Verwirrung bis hin zu Verwirrung. Aus diesem Grund sollten Ihre Produkte Benutzern, die sie im Betriebssystem deaktiviert haben, keine Animationen anzeigen.  Mithilfe einer CSS-Medienabfrage können Sie überprüfen, ob der Benutzer Animationen anzeigen möchte, und diese entsprechend deaktivieren.  Und ähnlich wie im dunklen und hellen Modus gibt es eine Möglichkeit, [reduzierte Bewegungen mit DevTools][DevToolsReducedMotion]zu simulieren.

Auf der Demoseite hier verhindert das Deaktivieren von Animationen den reibungslosen Bildlauf der Seite, wenn Sie verschiedene Teile des Navigationsmenüs auf der Seitenleiste auswählen.  Dies wird erreicht, indem die Einstellung für den reibungslosen Bildlauf in CSS in einer Medienabfrage umgebrochen wird:

:::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulieren von reduzierter Bewegung und css, die sicherstellen, dass ein gleichmäßiger Bildlauf nur erfolgt, wenn der Benutzer dies möchte" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
    Simulieren von reduzierter Bewegung und css, die sicherstellen, dass ein gleichmäßiger Bildlauf nur erfolgt, wenn der Benutzer dies möchte
:::image-end:::

```css
@media (prefers-reduced-motion: no-preference) {
  html {
    scroll-behavior: smooth;
  }
}
```

Diese CSS-Medienabfrage führt die Animation für einen gleichmäßigen Bildlauf bedingt aus.  Die Animation der oberen Navigationsleiste, des Seitenleisten-Navigationsmenüs und **weiterer** Links wird jedoch weiterhin ausgeführt, auch wenn der Benutzer keine Animationen sehen möchte. Diese anderen Animationen müssen bedingt ausgeführt werden, z. B. durch Hinzufügen zusätzlicher Medienabfragen.

Für detaillierte exemplarische Vorgehensweisen navigieren Sie zu [Überprüfen, ob die Seite mit deaktivierter BENUTZERoberflächenanimation verwendet werden kann.](test-reduced-ui-motion.md)


## <a name="what-to-do-next"></a>Wie geht es weiter?

Wir haben einige Tools behandelt, mit denen Sie sicherstellen können, dass Sie Barrierefreiheitsprobleme in Ihren Produkten abfangen.  Diese Tools reichen von automatisierten Prüfungen und manuellen Detailprüfungen bis hin zur Simulation verschiedener Zustände und Umgebungen.  Diese Tools werden in Features zum Testen der [Barrierefreiheit in DevTools](reference.md)zusammengefasst.  Automatisierte Tools können nicht alle Probleme in einem Produkt finden, da viele der Barrierefreiheitsbarrieren nur bei der interaktiven Verwendung auftreten.

Keines dieser Tools kann eine ordnungsgemäße Testphase Ihrer Produkte durch Personen ersetzen, die Hilfstechnologien verwenden, und einen Plan befolgen, um alle erforderlichen Tests zu überprüfen. Sie können auch das [Bewertungsfeature][AccessibilityInsightsAssessment] von [Accessibility Insights][AccessibilityInsights]verwenden.  Möglicherweise müssen Sie zusätzliche Prüfungen durchführen, z. B.:

* Testen beim Vergrößern.
* Testen mit Bildschirmleseprogrammen.
* Testen mit Spracherkennung.
* Testen im Modus mit hohem Kontrast.

Eine weitere Möglichkeit, herauszufinden, was Sie tun müssen, um Ihr Webprodukt zu verbessern, besteht darin, die [Webhint-Erweiterung für Visual Studio Code][WebhintForCode]zu verwenden.  Diese Erweiterung kennzeichnet die leicht erkennbaren Barrierefreiheitsprobleme in Ihrem Quellcode und gibt Einblicke, wie sie behoben werden können.

:::image type="complex" source="../media/a11y-testing-webhint-in-vs-code.msft.png" alt-text="Webhint in Visual Studio Code mit einem Problem bei der Barrierefreiheit, indem das HTML-Element und eine Erläuterung des Problems erläutert werden" lightbox="../media/a11y-testing-webhint-in-vs-code.msft.png":::
    Webhint in Visual Studio Code mit einem Problem bei der Barrierefreiheit, indem das HTML-Element und eine Erläuterung des Problems erläutert werden
:::image-end:::

Wir arbeiten ständig an neuen Barrierefreiheitsfunktionen für DevTools.  Wenn Etwas fehlt, senden Sie uns eine Nachricht, und teilen Sie uns mit, was wir tun können.


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]


<!-- links -->
[DevToolsMediaQueries]: ../device-mode/index.md#show-media-queries "Anzeigen von Medienabfragen – Emulieren mobiler Geräte in Microsoft Edge DevTools | Microsoft-Dokumente"
[DevToolsDeviceModeIndex]: ../device-mode/index.md "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsAccessibilityReference]: reference.md "Features für Barrierefreiheitstests in DevTools | Microsoft-Dokumente"
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Simulation von dunklen oder hellen Farbschemas | Microsoft-Dokumente"
[DevToolsIssuesTool]: ../issues/index.md "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"
[DevToolsReducedMotion]: ./reduced-motion-simulation.md "Reduzierte Bewegungssimulation | Microsoft-Dokumente"
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Emulieren von Sehschwächen | Microsoft-Dokumente"
<!-- links into test-issues-tool.md -->
[DevToolsAccessibilityTestIssuesToolViewAccSection]: test-issues-tool.md#view-the-accessibility-section-of-the-issues-tool "Anzeigen des Abschnitts &quot;Barrierefreiheit&quot; des Tools &quot;Probleme&quot; – Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme | Microsoft-Dokumente"
[DevtoolsAccessibilityTestIssuesToolCheckFieldsLabels]: test-issues-tool.md#verify-that-input-fields-have-labels "Überprüfen, ob Eingabefelder Bezeichnungen aufweisen – Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme | Microsoft-Dokumente" 
[DevtoolsAccessibilityTestIssuesToolCheckAltText]: test-issues-tool.md#verify-that-images-have-alt-text "Überprüfen, ob Bilder alternativ text sind – Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme | Microsoft-Dokumente "
[DevtoolsAccessibilityTestIssuesToolCheckContrast]: test-issues-tool.md#verify-that-text-colors-have-enough-contrast "Stellen Sie sicher, dass textfarben genügend Kontrast aufweisen – Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme | Microsoft-Dokumente"
<!-- links into test-inspect-tool.md -->
[DevtoolsAccessibilityTestInspectToolColorHighlighting]: test-inspect-tool.md#identify-nested-regions-using-color-highlighting "Identifizieren von geschachtelten Regionen mithilfe von Farbhervorhebung – Verwenden Sie das Tool Inspect, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen | Microsoft-Dokumente"
[DevtoolsAccessibilityTestInspectToolIndivElems]: test-inspect-tool.md#check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support "Überprüfen Einzelner Elemente auf Textkontrast, Sprachausgabetext und Tastaturunterstützung – Verwenden Sie das Tool Inspect, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen | Microsoft-Dokumente"
[DevtoolsAccessibilityTestInspectToolDomCss]: test-inspect-tool.md#use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css "Verwenden Sie das Inspect-Tool, um auf die Webseite zu zeigen, um das DOM und CSS hervorzuheben. Verwenden Sie das Tool Inspect, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen, | Microsoft-Dokumente"
<!-- external links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "Kontrastverhältnis | W3c"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Richtlinien für die Barrierefreiheit von Webinhalten | W3c"
[AccessibilityInsightsAssessment]: https://accessibilityinsights.io/docs/en/web/getstarted/assessment/ "Assessment in Accessibility Insights for Web | Insights zur Barrierefreiheit"
[AccessibilityInsights]: https://accessibilityinsights.io "Insights zur Barrierefreiheit"
[Lighthouse]: https://developers.google.com/web/tools/lighthouse/ "| Google"
[WebhintForCode]:https://aka.ms/webhint4code "webhint | Visual Studio Markt"
