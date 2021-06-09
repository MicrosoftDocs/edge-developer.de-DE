---
description: Öffnen Sie die Konsole, erstellen Sie einen Live-Ausdruck, und legen Sie den Ausdruck auf document.activeElement fest.
title: Nachverfolgen, welches Element den Fokus hat
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 2fd53caccefefb0b0bce4b5c82f30632e11a3cb6
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597108"
---
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
# <a name="track-which-element-has-focus"></a><span data-ttu-id="2758f-104">Nachverfolgen, welches Element den Fokus hat</span><span class="sxs-lookup"><span data-stu-id="2758f-104">Track which element has focus</span></span>  

<span data-ttu-id="2758f-105">Angenommen, Sie testen die Barrierefreiheit der Tastaturnavigation einer Seite.</span><span class="sxs-lookup"><span data-stu-id="2758f-105">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="2758f-106">Beim Navigieren auf der Seite mit der `Tab` Taste wird der Fokusring manchmal ausgeblendet, da das Element, das den Fokus hat, ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="2758f-106">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  

<span data-ttu-id="2758f-107">So verfolgen Sie das fokussierte Element in DevTools:</span><span class="sxs-lookup"><span data-stu-id="2758f-107">To track the focused element in DevTools:</span></span>

1.  <span data-ttu-id="2758f-108">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="2758f-108">Open the **Console**.</span></span>  
1.  <span data-ttu-id="2758f-109">Wählen **Sie "Liveausdruck erstellen"** \( ![ Liveausdruck erstellen ](../media/create-live-expression-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="2758f-109">Choose **Create live expression** \(![Create live expression](../media/create-live-expression-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Erstellen eines Liveausdrucks" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       <span data-ttu-id="2758f-111">Erstellen eines Liveausdrucks</span><span class="sxs-lookup"><span data-stu-id="2758f-111">Create a Live Expression</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2758f-112">Geben Sie `document.activeElement` ein.</span><span class="sxs-lookup"><span data-stu-id="2758f-112">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="2758f-113">Um den Ausdruck zu speichern, wählen Sie außerhalb des Liveausdrucks aus.</span><span class="sxs-lookup"><span data-stu-id="2758f-113">To save the expression, select outside of the live expression.</span></span>
    
<span data-ttu-id="2758f-114">Der unten angezeigte Wert `document.activeElement` ist das Ergebnis des Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="2758f-114">The value displayed below `document.activeElement` is the result of the expression.</span></span>  

<span data-ttu-id="2758f-115">Da dieser Ausdruck immer das fokussierte Element darstellt, haben Sie jetzt eine Möglichkeit, immer nachzuverfolgen, welches Element den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="2758f-115">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="2758f-116">Zeigen Sie auf das Ergebnis, um das fokussierte Element im Viewport hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="2758f-116">Hover on the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="2758f-117">Zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **"Einblenden" im Bereich "Elemente"** aus, um das Element in der DOM-Struktur im **Elementtool** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2758f-117">Hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** tool.</span></span>  
*   <span data-ttu-id="2758f-118">Zeigen Sie auf das Ergebnis, öffnen Sie das Kontextmenü \(Rechtsklick\), und wählen Sie **Store als globale Variable** aus, um einen Variablenverweis auf den Knoten zu erstellen, den Sie in der **Konsole**verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2758f-118">Hover on the result, open the contextual menu \(right-click\), and choose **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  


## <a name="see-also"></a><span data-ttu-id="2758f-119">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="2758f-119">See also</span></span>

*  [<span data-ttu-id="2758f-120">Analysieren Sie die fehlenden Anzeige des Tastaturfokus in einem Randleistenmenü</span><span class="sxs-lookup"><span data-stu-id="2758f-120">Analyze the lack of indication of keyboard focus in a sidebar menu</span></span>](test-analyze-no-focus-indicator.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2758f-121">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="2758f-121">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->  
> [!NOTE]
> <span data-ttu-id="2758f-122">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2758f-122">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2758f-123">Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) zu finden und wurde von [Baskisch (Technical][KayceBasques] Writer, Chrome DevTools \& Ausrufebereich\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="2758f-123">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="2758f-125">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2758f-125">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
