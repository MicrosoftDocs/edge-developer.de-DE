---
description: Verwenden Sie das Tool "Probleme", um Probleme mit der aktuellen Webseite zu identifizieren und zu beheben.
title: Suchen und Beheben von Problemen mit dem Tool "Probleme"
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 86277c509aa4b67635661ba3a316fb5b1e3b9d14
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624703"
---
<!-- Copyright Sam Dutton

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="find-and-fix-problems-using-the-issues-tool"></a>Suchen und Beheben von Problemen mit dem Tool "Probleme"

In Microsoft Edge DevTools analysiert das **Tool "Probleme"** automatisch die aktuelle Webseite, meldet Probleme nach Typ und stellt Dokumentation bereit, um die Probleme zu erläutern und zu beheben.

Das **Tool "Probleme"** bietet Feedback in den folgenden Kategorien:
*  Zugänglichkeit.
*  Browserübergreifende Kompatibilität.
*  Leistung.
*  Progressive Web Apps.
*  Sicherheit.
*  Andere.

Feedback im **Problemtool** wird von mehreren Quellen bereitgestellt, einschließlich der Chromium-Plattform, Deque axe, MDN-Browserkompatibilitätsdaten und Webhint.  Informationen zu diesen Feedbackquellen, die das Tool **"Probleme"** auffüllen, erhalten Sie unter:
*  [Axe Tools (Übersicht)][DequeAxe]
*  [browser-compat-data repo][MDNCompat]
*  [Webhint][webhintIo]


## <a name="open-the-issues-tool"></a>Öffnen des Tools "Probleme"

Führen Sie die folgenden Schritte aus, um das **Problemtool** mithilfe einer Demoseite zu öffnen.


1.  Navigieren Sie zu einer Webseite, die Zu behebende Probleme enthält.  Öffnen Sie beispielsweise die [Demoseite für Barrierefreiheitstests][A11ytestingPagewitherrors] in einer neuen Registerkarte oder einem neuen Fenster.

1.  Öffnen Sie DevTools.  Nach ein paar Sekunden wird der **Problemindikator** \( ![ Problemindikator ](../media/issues-counter-icon.msft.png) \) in der oberen rechten Ecke von DevTools angezeigt.  Die Anzahl der Probleme im Problemindikator kann unterschiedlich sein.

1.  Wählen Sie den **Problemindikator aus.**  Das Tool **"Probleme"** wird mit Problemen geöffnet, die in verschiedene Kategorien unterteilt sind.

    :::image type="complex" source="../media/issues-tool-categories.msft.png" alt-text="Kategorien von Problemen im Tool Probleme auf der Demoseite" lightbox="../media/issues-tool-categories.msft.png":::
       Kategorien von Problemen im Tool "Probleme" auf der Demoseite
    :::image-end:::

### <a name="other-ways-to-open-the-issues-tool"></a>Weitere Möglichkeiten zum Öffnen des Tools "Probleme"

Es gibt mehrere zusätzliche Möglichkeiten, das **Problemtool** zu öffnen:
*  Wählen Sie im Hauptbereich oder in der Schublade das Menü **"Weitere Tools** " ( **+** ) aus, und wählen Sie dann **"Probleme"** aus. ****
*  Wählen Sie **Anpassen und Steuern von DevTools**Weitere  >  **Tools**  >  **Probleme**.
*  Wählen Sie in der DOM-Struktur im **Elementtool** einen Wellen unterstrichenen Elementnamen aus, `Shift` und klicken Sie dann darauf.  Oder öffnen Sie das Kontextmenü für ein wellenförmiges unterstrichenes Element, und wählen Sie dann **Probleme anzeigen**aus.

### <a name="issues-are-automatically-ordered-by-severity"></a>Probleme werden automatisch nach Schweregrad sortiert

Innerhalb jeder Problemkategorie werden zuerst die Fehler aufgelistet, dann Warnungen und dann Tipps.

:::image type="complex" source="../media/issues-ordered-by-severity.msft.png" alt-text="Das Tool Probleme zeigt Leistungsprobleme nach Schweregrad sortiert an." lightbox="../media/issues-ordered-by-severity.msft.png":::
   Das Tool **"Probleme"** zeigt Leistungsprobleme nach Schweregrad sortiert an.
:::image-end:::

### <a name="include-third-party-issues"></a>Einbeziehen von Problemen von Drittanbietern

Um Probleme einzuschließen, die durch Websites von Drittanbietern verursacht werden, aktivieren Sie oben im **Problemtool** das Kontrollkästchen **"Probleme** von Drittanbietern einschließen".


## <a name="expand-entries-in-the-issues-tool"></a>Erweitern von Einträgen im Tool "Probleme"

Das Tool **"Probleme"** enthält zusätzliche Dokumentationen und empfohlene Korrekturen, die für jedes Problem gelten.  Um ein Problem zu erweitern, um diese zusätzlichen Informationen zu erhalten, wählen Sie ein Problem wie folgt aus.

1.  Öffnen Sie die [Demoseite][A11ytestingPagewitherrors] in einem neuen Fenster oder einer neuen Registerkarte, und öffnen Sie dann DevTools.

1.  Öffnen Sie das **Tool "Probleme",** indem Sie den **Problemindikator** \( ![ Problemzähler ](../media/issues-counter-icon.msft.png) \) auswählen.

1.  Wählen Sie ein Problem aus, um das Problem zu erweitern.

    :::image type="complex" source="../media/issues-tool-initial-view-accessibility-page.msft.png" alt-text="Das Tool Probleme mit zusätzlichen Informationen zum Beheben des Problems" lightbox="../media/issues-tool-initial-view-accessibility-page.msft.png":::
       Das **Tool "Probleme"** mit zusätzlichen Informationen zum Beheben des Problems
    :::image-end:::

Jedes angezeigte Problem hat die folgenden Komponenten:
*   Eine Überschrift, die das Problem beschreibt.
*   Eine Beschreibung, die mehr Kontext und vorgeschlagene Lösungen bietet.
*   Ein **Abschnitt "BETROFFENE RESSOURCEN",** der mit Ressourcen in DevTools verknüpft ist, z. B. dem Tool **"Elemente",** **"Quellen"** oder **"Netzwerk".**
*   Links zu weiteren Dokumentationen.


## <a name="view-issues-in-context-of-an-associated-tool"></a>Anzeigen von Problemen im Kontext eines zugeordneten Tools

Ein Problem im **Problemtool** kann eine oder mehrere Links enthalten, die unterschiedliche Tools öffnen, z. B. das Tool **"Elemente",** **"Quellen"** oder **"Netzwerk".** Sie können eines dieser Tools öffnen, um zusätzliche Problembehandlungsschritte auszuführen. Führen Sie die folgenden Schritte aus, um ein verknüpftes Tool aus dem Tool **"Probleme"** zu öffnen.

1.  Öffnen Sie wie im vorherigen Abschnitt beschrieben die Demoseite, und erweitern Sie dann ein Problem im **Tool "Probleme".**

1.  Wählen Sie in **"BETROFFENE RESSOURCEN**  >  **öffnen in"** den Toolnamen aus.  Die betroffene Ressource wird im ausgewählten Tool angezeigt.

    :::image type="complex" source="../media/issues-tool-affected-resource-opens-elements-tool.msft.png" alt-text="Wählen Sie ein Tool aus, um eine betroffene Ressource im Tool Probleme zu öffnen." lightbox="../media/issues-tool-affected-resource-opens-elements-tool.msft.png":::
       Wählen Sie ein Tool aus, um eine betroffene Ressource im Tool "Probleme" zu öffnen.
    :::image-end:::

    Ein erweitertes Problem kann eine **Netzwerkverbindung** aufweisen, um die betroffene Ressource im **Netzwerktool** anzuzeigen.

    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Das Netzwerktool wird geöffnet, wenn Sie eine Netzwerkressourcenverbindung auswählen" lightbox="../media/issues-tab-view-issue.msft.png":::
    Das **Netzwerktool** wird geöffnet, wenn Sie eine **Netzwerkressourcenverbindung** auswählen
    :::image-end:::


## <a name="open-issues-from-the-dom-tree"></a>Offene Probleme aus der DOM-Struktur

Wenn einem Element ein Problem zugeordnet ist, zeigt die DOM-Struktur im **Elementtool** eine wellenförmige Unterstreichung unter dem Elementnamen an.  Sie können das Kontextmenü (Rechtsklick) für das Element öffnen und dann Probleme **anzeigen**auswählen oder `Shift` mit der linken Maustaste auf das Element mit der wellenförmigen Unterstreichung klicken.

Führen Sie die folgenden Schritte aus, um ein Problem für Elemente mit wellenförmigen Unterstreichungen in der DOM-Struktur anzuzeigen.

1.  Öffnen Sie eine Seite, z. B. die [Demoseite,][A11ytestingPagewitherrors]in einer neuen Registerkarte oder einem neuen Fenster.

1.  Öffnen Sie DevTools, und wählen Sie dann die Registerkarte **"Elemente" aus.**

1.  Erweitern Sie in der DOM-Struktur `<body>`  >  `<header>`  >  `<form>` .  Beachten Sie, dass das `<input>` Element eine wellenförmige Unterstreichung aufweist.

    :::image type="complex" source="../media/issues-wavy-underlines-dom-tree.msft.png" alt-text="Wavy-underlined issues in the DOM tree in the Elements tool" lightbox="../media/issues-wavy-underlines-dom-tree.msft.png":::
       Wavy-underlined issues in the **DOM tree** in the **Elements** tool
    :::image-end:::

1.  Zeigen Sie auf das `<input>` Element.  Eine QuickInfo zeigt Informationen zu dem Problem an.

1.  Öffnen Sie das Kontextmenü des Elements mit der wellenförmigen Unterstreichung, und wählen Sie dann **Probleme anzeigen**aus.  Das Tool **"Probleme"** wird geöffnet und zeigt das Problem an, das diesem Element zugeordnet ist.

    :::image type="complex" source="../media/issues-opened-from-dom-tree-wavy-underline.msft.png" alt-text="Details zu Problemen mit einem wellenförmigen unterstrichenen Element in der DOM-Struktur" lightbox="../media/issues-opened-from-dom-tree-wavy-underline.msft.png":::
       Details zu Problemen mit einem wellenförmigen unterstrichenen Element in der **DOM-Struktur**
    :::image-end:::


## <a name="see-also"></a>Weitere Informationen

* [Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme](../accessibility/test-issues-tool.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]

<!-- links -->
[DevtoolsOpenIndex]: ../open/index.md "Öffnen sie Microsoft Edge DevTools-| Microsoft-Dokumente"
<!-- external links -->
[A11ytestingPagewitherrors]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demoseite für Barrierefreiheitstests | Microsoft-Dokumente"
[DequeAxe]: https://www.deque.com/axe "Axe Tools – Übersicht | Deque"
[MDNCompat]: https://github.com/mdn/browser-compat-data "MDN-Browserkompatibilitätsdaten | GitHub"
[webhintIo]: https://webhint.io "webhint.io"

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/issues/index) gefunden und von [Sam Dutton][SamDutton] \(Developer Advocate\) verfasst.
[ ![ Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton
