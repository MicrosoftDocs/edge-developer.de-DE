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
# <a name="test-accessibility-using-the-accessibility-tab"></a><span data-ttu-id="67e7b-104">Testen Sie die Barrierefreiheit mithilfe der Registerkarte "Barrierefreiheit"</span><span class="sxs-lookup"><span data-stu-id="67e7b-104">Test accessibility using the Accessibility tab</span></span>

<span data-ttu-id="67e7b-105">Auf der Registerkarte **"Barrierefreiheit"** können Sie die Barrierefreiheitsstruktur, ARIA-Attribute und berechneten Barrierefreiheitseigenschaften von DOM-Knoten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="67e7b-105">The **Accessibility** tab is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="67e7b-106">So öffnen Sie die Registerkarte **"Barrierefreiheit":**</span><span class="sxs-lookup"><span data-stu-id="67e7b-106">To open the **Accessibility** tab:</span></span>

1.  <span data-ttu-id="67e7b-107">Wählen Sie das Elementtool **aus.**</span><span class="sxs-lookup"><span data-stu-id="67e7b-107">Select the **Elements** tool.</span></span>  
1.  <span data-ttu-id="67e7b-108">Wählen Sie in der **DOM-Struktur**das Element aus, das Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="67e7b-108">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="67e7b-109">Wählen Sie die Registerkarte **"Barrierefreiheit" aus.**  Möglicherweise müssen Sie zuerst die Schaltfläche **"Weitere Registerkarten** \( ![ die Schaltfläche "Weitere Registerkarten"\) ](../media/more-tabs-icon.msft.png) rechts neben der Registerkarte **"Formatvorlagen"** auswählen.</span><span class="sxs-lookup"><span data-stu-id="67e7b-109">Select the **Accessibility** tab.  You might need to first select the **More tabs** \(![the More tabs button](../media/more-tabs-icon.msft.png)\) button to the right of the **Styles** tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Überprüfen Sie das h1-Element der DevTools-Startseite auf der Registerkarte "Barrierefreiheit"." lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="67e7b-111">Überprüfen Sie das `h1` Element der DevTools-Startseite auf der Registerkarte **"Barrierefreiheit".**</span><span class="sxs-lookup"><span data-stu-id="67e7b-111">Inspect the `h1` element of the DevTools homepage in the **Accessibility** tab</span></span>
:::image-end:::  


## <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a><span data-ttu-id="67e7b-112">Anzeigen der Position eines Elements in der Barrierefreiheitsstruktur</span><span class="sxs-lookup"><span data-stu-id="67e7b-112">View the position of an element in the Accessibility Tree</span></span>

<span data-ttu-id="67e7b-113">Die [Barrierefreiheitsstruktur][MDNAccessibilityTree] ist eine Teilmenge der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="67e7b-113">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="67e7b-114">Die Barrierefreiheitsstruktur enthält nur Elemente aus der DOM-Struktur, die relevant und nützlich sind, um den Inhalt einer Seite über Hilfstechnologien wie Bildschirmleseprogramme anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="67e7b-114">The accessibility tree only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page through assistive technologies such as screen readers.</span></span>

<span data-ttu-id="67e7b-115">Überprüfen Sie die Position eines Elements in der Barrierefreiheitsstruktur auf der Registerkarte **"Barrierefreiheit".**</span><span class="sxs-lookup"><span data-stu-id="67e7b-115">Inspect the position of an element in the accessibility tree from the **Accessibility** tab.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Abschnitt "Barrierefreiheitsstruktur"" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="67e7b-117">Abschnitt **"Barrierefreiheitsstruktur"**</span><span class="sxs-lookup"><span data-stu-id="67e7b-117">The **Accessibility Tree** section</span></span>  
:::image-end:::  


## <a name="view-the-aria-attributes-of-an-element"></a><span data-ttu-id="67e7b-118">Anzeigen der ARIA-Attribute eines Elements</span><span class="sxs-lookup"><span data-stu-id="67e7b-118">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="67e7b-119">ARIA-Attribute stellen sicher, dass Hilfstechnologien wie Bildschirmleseprogramme über alle Informationen verfügen, die sie benötigen, um den Inhalt einer Seite korrekt darzustellen.</span><span class="sxs-lookup"><span data-stu-id="67e7b-119">ARIA attributes ensure that assistive technologies such as screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="67e7b-120">Zeigen Sie die ARIA-Attribute eines Elements auf der Registerkarte **Barrierefreiheit an.**</span><span class="sxs-lookup"><span data-stu-id="67e7b-120">View the ARIA attributes of an element in the **Accessibility** tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Abschnitt "ARIA Attributes"" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="67e7b-122">Abschnitt **"ARIA Attributes"**</span><span class="sxs-lookup"><span data-stu-id="67e7b-122">The **ARIA Attributes** section</span></span>  
:::image-end:::  


## <a name="view-the-computed-accessibility-properties-of-an-element"></a><span data-ttu-id="67e7b-123">Anzeigen der berechneten Barrierefreiheitseigenschaften eines Elements</span><span class="sxs-lookup"><span data-stu-id="67e7b-123">View the computed accessibility properties of an element</span></span>  


<span data-ttu-id="67e7b-124">Einige Barrierefreiheitseigenschaften werden vom Browser dynamisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="67e7b-124">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="67e7b-125">Diese Eigenschaften werden im Abschnitt **"Berechnete Eigenschaften"** der Registerkarte **"Barrierefreiheit"** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="67e7b-125">These properties are displayed in the **Computed Properties** section of the **Accessibility** tab.</span></span>  

<span data-ttu-id="67e7b-126">Zeigen Sie die berechneten Barrierefreiheitseigenschaften eines Elements auf der Registerkarte **"Barrierefreiheit" an.**</span><span class="sxs-lookup"><span data-stu-id="67e7b-126">View the computed accessibility properties of an element in the **Accessibility** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="67e7b-127">Verwenden Sie für berechnete CSS-Eigenschaften die Registerkarte ["Berechnet".][DevtoolsCssReferenceViewActuallyAppliedElements]</span><span class="sxs-lookup"><span data-stu-id="67e7b-127">For computed CSS properties, use the [Computed][DevtoolsCssReferenceViewActuallyAppliedElements] tab.</span></span>

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Der Abschnitt "Berechnete Eigenschaften" der Registerkarte "Barrierefreiheit"" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="67e7b-129">Der Abschnitt **"Berechnete Eigenschaften"** der Registerkarte **"Barrierefreiheit"**</span><span class="sxs-lookup"><span data-stu-id="67e7b-129">The **Computed Properties** section of the **Accessibility** tab</span></span>  
:::image-end:::  


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="67e7b-130">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="67e7b-130">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="67e7b-131">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67e7b-131">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="67e7b-132">Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) zu finden und wurde von [Baskisch (Technical][KayceBasques] Writer, Chrome DevTools \& Ausrufebereich\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="67e7b-132">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="67e7b-134">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="67e7b-134">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Nur die CSS anzeigen, die tatsächlich auf ein Element angewendet wird – CSS-Verweis | Microsoft-Dokumente"  
[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "| der Barrierefreiheitsstruktur (Accessibility Tree, AOM) Mdn"  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
