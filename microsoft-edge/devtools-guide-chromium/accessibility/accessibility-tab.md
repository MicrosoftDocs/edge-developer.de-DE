---
description: Testen der Barrierefreiheit mithilfe der Registerkarte "Barrierefreiheit".
title: Testen Sie die Barrierefreiheit mithilfe der Registerkarte "Barrierefreiheit"
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 839feed56fc82af2b4d96a081c476696166075b9
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597483"
---
<!-- this article was created on 05/11/2021 by moving a section out from the "Accessibility reference" article (reference.md) -->
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="test-accessibility-using-the-accessibility-tab"></a>Testen Sie die Barrierefreiheit mithilfe der Registerkarte "Barrierefreiheit"

Auf der Registerkarte **"Barrierefreiheit"** können Sie die Barrierefreiheitsstruktur, ARIA-Attribute und berechneten Barrierefreiheitseigenschaften von DOM-Knoten anzeigen.  

So öffnen Sie die Registerkarte **"Barrierefreiheit":**

1.  Wählen Sie das Elementtool **aus.**  
1.  Wählen Sie in der **DOM-Struktur**das Element aus, das Sie überprüfen möchten.  
1.  Wählen Sie die Registerkarte **"Barrierefreiheit" aus.**  Möglicherweise müssen Sie zuerst die Schaltfläche **"Weitere Registerkarten** \( ![ die Schaltfläche "Weitere Registerkarten"\) ](../media/more-tabs-icon.msft.png) rechts neben der Registerkarte **"Formatvorlagen"** auswählen.

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Überprüfen Sie das h1-Element der DevTools-Startseite auf der Registerkarte Barrierefreiheit." lightbox="../media/accessibility-elements-accessibility.msft.png":::
   Überprüfen Sie das `h1` Element der DevTools-Startseite auf der Registerkarte **"Barrierefreiheit".**
:::image-end:::  


## <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a>Anzeigen der Position eines Elements in der Barrierefreiheitsstruktur

Die [Barrierefreiheitsstruktur][MDNAccessibilityTree] ist eine Teilmenge der DOM-Struktur.  Die Barrierefreiheitsstruktur enthält nur Elemente aus der DOM-Struktur, die relevant und nützlich sind, um den Inhalt einer Seite über Hilfstechnologien wie Bildschirmleseprogramme anzuzeigen.

Überprüfen Sie die Position eines Elements in der Barrierefreiheitsstruktur auf der Registerkarte **"Barrierefreiheit".**  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Abschnitt Barrierefreiheitsstruktur" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   Abschnitt **"Barrierefreiheitsstruktur"**  
:::image-end:::  


## <a name="view-the-aria-attributes-of-an-element"></a>Anzeigen der ARIA-Attribute eines Elements  

ARIA-Attribute stellen sicher, dass Hilfstechnologien wie Bildschirmleseprogramme über alle Informationen verfügen, die sie benötigen, um den Inhalt einer Seite korrekt darzustellen.  

Zeigen Sie die ARIA-Attribute eines Elements auf der Registerkarte **Barrierefreiheit an.**

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Abschnitt ARIA Attributes" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   Abschnitt **"ARIA Attributes"**  
:::image-end:::  


## <a name="view-the-computed-accessibility-properties-of-an-element"></a>Anzeigen der berechneten Barrierefreiheitseigenschaften eines Elements  


Einige Barrierefreiheitseigenschaften werden vom Browser dynamisch berechnet.  Diese Eigenschaften werden im Abschnitt **"Berechnete Eigenschaften"** der Registerkarte **"Barrierefreiheit"** angezeigt.  

Zeigen Sie die berechneten Barrierefreiheitseigenschaften eines Elements auf der Registerkarte **"Barrierefreiheit" an.**

> [!NOTE]
> Verwenden Sie für berechnete CSS-Eigenschaften die Registerkarte ["Berechnet".][DevtoolsCssReferenceViewActuallyAppliedElements]

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Der Abschnitt Berechnete Eigenschaften der Registerkarte Barrierefreiheit" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   Der Abschnitt **"Berechnete Eigenschaften"** der Registerkarte **"Barrierefreiheit"**  
:::image-end:::  


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) zu finden und wurde von [Baskisch (Technical][KayceBasques] Writer, Chrome DevTools \& Ausrufebereich\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  


<!-- links -->
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Nur die CSS anzeigen, die tatsächlich auf ein Element angewendet wird – CSS-Verweis | Microsoft-Dokumente"  
[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "| der Barrierefreiheitsstruktur (Accessibility Tree, AOM) Mdn"  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
