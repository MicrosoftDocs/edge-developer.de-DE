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
# <a name="test-text-color-contrast-using-the-color-picker"></a><span data-ttu-id="35d92-104">Testen Sie den Kontrast von Text und Farbe mithilfe des Farbwählers</span><span class="sxs-lookup"><span data-stu-id="35d92-104">Test text-color contrast using the Color Picker</span></span>

<span data-ttu-id="35d92-105">Personen mit geringem Sehvermögen sehen möglicherweise keine Bereiche, die sehr hell oder sehr dunkel sind.</span><span class="sxs-lookup"><span data-stu-id="35d92-105">People with low vision may not see areas that are very bright or very dark.</span></span>  <span data-ttu-id="35d92-106">Alles wird in der Regel auf ungefähr der gleichen Helligkeitsstufe angezeigt, wodurch es schwierig ist, Gliederungen und Ränder zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="35d92-106">Everything tends to appear at about the same level of brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="35d92-107">Das Kontrastverhältnis misst den Helligkeitsunterschied zwischen Dem Vordergrund und Hintergrund von Text.</span><span class="sxs-lookup"><span data-stu-id="35d92-107">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="35d92-108">Wenn Ihr Text ein niedriges Kontrastverhältnis aufweist, wird Ihre Website für Personen mit geringem Sehvermögen möglicherweise als leerer Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35d92-108">If your text has a low contrast ratio, then people with low vision may experience your site as a blank screen.</span></span>  

<span data-ttu-id="35d92-109">In DevTools besteht eine Möglichkeit zum Anzeigen des Kontrastverhältnisses eines Textelements in der Verwendung der Farbauswahl auf der Registerkarte **"Formatvorlagen".**  Mit der Farbauswahl können Sie überprüfen, ob Ihr Text die empfohlenen Kontrastverhältnisstufen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="35d92-109">In DevTools, one way to view the contrast ratio of a text element is to use the Color Picker, from the **Styles** tab.  The Color Picker helps you verify that your text meets recommended contrast ratio levels.</span></span>

**<span data-ttu-id="35d92-110">So überprüfen Sie den Kontrast zwischen Text und Farbe mithilfe der Farbauswahl:</span><span class="sxs-lookup"><span data-stu-id="35d92-110">To check the text-color contrast using the Color Picker:</span></span>**

1.  <span data-ttu-id="35d92-111">Wählen Sie in DevTools **das** Elementtool aus.</span><span class="sxs-lookup"><span data-stu-id="35d92-111">In DevTools, select the **Elements** tool.</span></span>  
1.  <span data-ttu-id="35d92-112">Wählen Sie in der **DOM-Struktur**das Textelement aus, das Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="35d92-112">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Überprüfen eines Absatzes in der DOM-Struktur" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="35d92-114">Überprüfen eines Absatzes in der **DOM-Struktur**</span><span class="sxs-lookup"><span data-stu-id="35d92-114">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="35d92-115">Suchen Sie auf der Registerkarte **"Formatvorlagen"** die **Farbeigenschaft,** die auf das Element angewendet wird, und wählen Sie dann das Farbquadrat neben der **Farbeigenschaft** aus.</span><span class="sxs-lookup"><span data-stu-id="35d92-115">On the **Styles** tab, locate the **color** property that's applied to the element, and then select the color square next to the **color** property.</span></span>
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Die Farbeigenschaft des Elements" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="35d92-117">Die `color` Eigenschaft des Elements</span><span class="sxs-lookup"><span data-stu-id="35d92-117">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="35d92-118">Untersuchen Sie den Abschnitt **"Kontrastverhältnis"** der Farbauswahl.</span><span class="sxs-lookup"><span data-stu-id="35d92-118">Examine the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="35d92-119">Ein Häkchen bedeutet, dass das Element die [Mindestempfehlung][W3CContrastMinimum]erfüllt.</span><span class="sxs-lookup"><span data-stu-id="35d92-119">One check mark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="35d92-120">Zwei Häkchen bedeuten, dass die [erweiterte Empfehlung][W3CContrastEnhanced]erfüllt wird.</span><span class="sxs-lookup"><span data-stu-id="35d92-120">Two check marks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="Im Abschnitt "Kontrastverhältnis" der Farbauswahl werden zwei Häkchen und ein Wert von 13,97 angezeigt." lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="35d92-122">Im Abschnitt **"Kontrastverhältnis"** der Farbauswahl werden 2 Häkchen und ein Wert von</span><span class="sxs-lookup"><span data-stu-id="35d92-122">The **Contrast Ratio** section of the Color Picker shows 2 check marks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="35d92-123">Wählen Sie für weitere Informationen den Abschnitt **"Kontrastverhältnis"** aus, um ihn zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="35d92-123">For more information, select the **Contrast ratio** section to expand it.</span></span>  <span data-ttu-id="35d92-124">In der visuellen Auswahl oben in der Farbauswahl werden zwei Zeilen angezeigt, die über die visuelle Auswahl verlaufen, zusammen mit einem Kreis für die aktuelle Farbe.</span><span class="sxs-lookup"><span data-stu-id="35d92-124">In the visual picker at the top of the Color Picker, two lines appear, running across the visual picker, along with a circle for the current color.</span></span>  <span data-ttu-id="35d92-125">Wenn die aktuelle Farbe den Empfehlungen entspricht, entspricht auch alles auf derselben Seite der Zeile den Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="35d92-125">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="35d92-126">Wenn die aktuelle Farbe nicht den Empfehlungen entspricht, entspricht alles auf derselben Seite auch nicht den Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="35d92-126">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  

    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Die Kontrastverhältnislinie in der visuellen Auswahl" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="35d92-128">Die **Kontrastverhältnislinie** in der visuellen Auswahl</span><span class="sxs-lookup"><span data-stu-id="35d92-128">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  

1. <span data-ttu-id="35d92-129">Um verschiedene Farben auszuprobieren, wählen Sie in der visuellen Auswahl aus, oder wählen Sie unten in der Farbauswahl ein Farbmuster aus.</span><span class="sxs-lookup"><span data-stu-id="35d92-129">To try different colors, select within the visual picker, or select a color swatch at the bottom of the Color Picker.</span></span>
    

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="35d92-130">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="35d92-130">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="35d92-131">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35d92-131">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="35d92-132">Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) zu finden und wurde von [Baskisch (Technical][KayceBasques] Writer, Chrome DevTools \& Ausrufebereich\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="35d92-132">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="35d92-134">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="35d92-134">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->  
[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Aaa-| der Kontrastebene (verbessert) W3c"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Kontrast (Minimum) Level AA | W3c"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
