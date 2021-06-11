---
description: Überprüfen der Barrierefreiheitsstruktur auf Tastatur- und Sprachausgabeunterstützung.
title: Überprüfen Sie die Barrierefreiheitsstruktur auf Tastatur- und Sprachausgabeunterstützung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 0ab5e5609485505d1ad5fa6e2fffced9af25edcb
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597462"
---
# <a name="check-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a>Überprüfen Sie die Barrierefreiheitsstruktur auf Tastatur- und Sprachausgabeunterstützung

<!-- Accessibility tab: Accessibility Tree -->

Mehrere DevTools-Features überprüfen auf Tastatur- und Sprachausgabeunterstützung.  Die Verwendung des **Inspect-Tools** zum Überprüfen der Barrierefreiheit der einzelnen Seitenelemente kann ziemlich zeitaufwändig werden.  Eine alternative Möglichkeit zum Überprüfen einer Webseite ist die Verwendung der **Barrierefreiheitsstruktur.**  Die **Barrierefreiheitsstruktur** gibt an, welche Informationen die Seite für Hilfstechnologien wie Bildschirmleseprogramme bereitstellt.

Die **Barrierefreiheitsstruktur** ist eine Teilmenge der DOM-Struktur, die Elemente aus der DOM-Struktur enthält, die relevant und nützlich sind, um den Inhalt einer Seite in einer Sprachausgabe anzuzeigen.  Die **Barrierefreiheitsstruktur** befindet sich auf der Registerkarte **"Barrierefreiheit"** **des** Elements-Tools (in der Nähe der Registerkarte **"Formatvorlagen").**


So erkunden Sie die Verwendung der Barrierefreiheitsstruktur mit der Demoseite:

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte.  Wählen Sie dann **F12** aus, um DevTools zu öffnen.

1.  Wählen Sie in der oberen linken Ecke von DevTools die Schaltfläche **"Überprüfen** \( ![ das Symbol ](../media/inspect-icon.msft.png) \) aus, damit die Schaltfläche hervorgehoben ist (blau).

1.  Zeigen Sie auf der gerenderten Webseite im Abschnitt **"Schenkung"** auf die Schaltfläche **100.**  Die **** Überprüfungstoolüberlagerung wird angezeigt.

1.  Wählen Sie in der gerenderten Webseite die Schaltfläche **100** aus.  In DevTools wird das **Elementtool** angezeigt.  Die DOM-Struktur zeigt das `div` Element für die Schaltfläche **100** an.  Im Bereich **"Formatvorlagen"** werden die CSS-Einstellungen für das Element angezeigt.

1.  Wählen Sie rechts neben der Registerkarte **"Formatvorlagen"** die Registerkarte **"Barrierefreiheit"** aus.  Die **Barrierefreiheitsstruktur** für das Element wird angezeigt und erweitert.

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Schaltfläche Schenkungsformular im Tool "Barrierefreiheitsstruktur"" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    Schaltfläche "Schenkungsformular" im Tool "Barrierefreiheitsstruktur"
:::image-end:::

Jedes Element in der Struktur, das keinen Namen hat oder eine Rolle `generic` hat (z. B. das `div` Element), ist ein Problem, da dieses Element für Tastaturbenutzer oder Benutzer, die Hilfstechnologien verwenden, nicht verfügbar ist.


## <a name="see-also"></a>Weitere Informationen:

*  [Anzeigen der Position eines Elements in der Barrierefreiheitsstruktur][DevtoolsAccessibilityAccessibilityTabViewTree]
*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityAccessibilityTabViewTree]: accessibility-tab.md#view-the-position-of-an-element-in-the-accessibility-tree "Anzeigen der Position eines Elements in der Barrierefreiheitsstruktur – Testen der Barrierefreiheit mithilfe der Registerkarte &quot;Barrierefreiheit&quot; | Microsoft-Dokumente"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
