---
description: Testen des Text-Farbkontrasts mithilfe der Farbauswahl.
title: Testen Sie den Kontrast von Text und Farbe mithilfe des Farbwählers
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: f4ba5f3706460c443ae06a393e5ef63e5d336229
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597479"
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
# <a name="test-text-color-contrast-using-the-color-picker"></a>Testen Sie den Kontrast von Text und Farbe mithilfe des Farbwählers

Personen mit geringem Sehvermögen sehen möglicherweise keine Bereiche, die sehr hell oder sehr dunkel sind.  Alles wird in der Regel auf ungefähr der gleichen Helligkeitsstufe angezeigt, wodurch es schwierig ist, Gliederungen und Ränder zu unterscheiden.  

Das Kontrastverhältnis misst den Helligkeitsunterschied zwischen Dem Vordergrund und Hintergrund von Text.  Wenn Ihr Text ein niedriges Kontrastverhältnis aufweist, wird Ihre Website für Personen mit geringem Sehvermögen möglicherweise als leerer Bildschirm angezeigt.  

In DevTools besteht eine Möglichkeit zum Anzeigen des Kontrastverhältnisses eines Textelements in der Verwendung der Farbauswahl auf der Registerkarte **"Formatvorlagen".**  Mit der Farbauswahl können Sie überprüfen, ob Ihr Text die empfohlenen Kontrastverhältnisstufen erfüllt.

**So überprüfen Sie den Kontrast zwischen Text und Farbe mithilfe der Farbauswahl:**

1.  Wählen Sie in DevTools **das** Elementtool aus.  
1.  Wählen Sie in der **DOM-Struktur**das Textelement aus, das Sie überprüfen möchten.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Überprüfen eines Absatzes in der DOM-Struktur" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Überprüfen eines Absatzes in der **DOM-Struktur**  
    :::image-end:::  
    
1.  Suchen Sie auf der Registerkarte **"Formatvorlagen"** die **Farbeigenschaft,** die auf das Element angewendet wird, und wählen Sie dann das Farbquadrat neben der **Farbeigenschaft** aus.
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Die Farbeigenschaft des Elements" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       Die `color` Eigenschaft des Elements  
    :::image-end:::  
    
1.  Untersuchen Sie den Abschnitt **"Kontrastverhältnis"** der Farbauswahl.  Ein Häkchen bedeutet, dass das Element die [Mindestempfehlung][W3CContrastMinimum]erfüllt.  Zwei Häkchen bedeuten, dass die [erweiterte Empfehlung][W3CContrastEnhanced]erfüllt wird.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="Im Abschnitt Kontrastverhältnis der Farbauswahl werden zwei Häkchen und ein Wert von 13,97 angezeigt." lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       Im Abschnitt **"Kontrastverhältnis"** der Farbauswahl werden 2 Häkchen und ein Wert von `13.97`  
    :::image-end:::  
    
1.  Wählen Sie für weitere Informationen den Abschnitt **"Kontrastverhältnis"** aus, um ihn zu erweitern.  In der visuellen Auswahl oben in der Farbauswahl werden zwei Zeilen angezeigt, die über die visuelle Auswahl verlaufen, zusammen mit einem Kreis für die aktuelle Farbe.  Wenn die aktuelle Farbe den Empfehlungen entspricht, entspricht auch alles auf derselben Seite der Zeile den Empfehlungen.  Wenn die aktuelle Farbe nicht den Empfehlungen entspricht, entspricht alles auf derselben Seite auch nicht den Empfehlungen.  

    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Die Kontrastverhältnislinie in der visuellen Auswahl" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       Die **Kontrastverhältnislinie** in der visuellen Auswahl  
    :::image-end:::  

1. Um verschiedene Farben auszuprobieren, wählen Sie in der visuellen Auswahl aus, oder wählen Sie unten in der Farbauswahl ein Farbmuster aus.
    

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) zu finden und wurde von [Baskisch (Technical][KayceBasques] Writer, Chrome DevTools \& Ausrufebereich\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  


<!-- links -->  
[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Aaa-| der Kontrastebene (verbessert) W3c"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Kontrast (Minimum) Level AA | W3c"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
