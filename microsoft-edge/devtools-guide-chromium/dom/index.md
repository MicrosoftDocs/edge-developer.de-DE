---
description: Anzeigen von Knoten, Suchen nach Knoten, Bearbeiten von Knoten, Verweisen auf Knoten in der Konsole, Unterbrechen von Knotenänderungen und vieles mehr.
title: Erste Schritte mit dem Anzeigen und Ändern des DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 8340c4d4d7eacdb6ad4155c1c9699db150522f16
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643434"
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
# <a name="get-started-with-viewing-and-changing-the-dom"></a><span data-ttu-id="fc26e-104">Erste Schritte mit dem Anzeigen und Ändern des DOM</span><span class="sxs-lookup"><span data-stu-id="fc26e-104">Get started with viewing and changing the DOM</span></span>  

<span data-ttu-id="fc26e-105">Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen zum Anzeigen und Ändern des [Dokumentobjektmodells](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\) einer Seite mit Microsoft Edge DevTools zu erlernen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-105">Complete these interactive tutorials to learn the basics of viewing and changing the [Document Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\) of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="fc26e-106">In diesem Lernprogramm wird davon ausgegangen, dass Sie den Unterschied zwischen DOM und HTML kennen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-106">This tutorial assumes that you know the difference between the DOM and HTML.</span></span> <span data-ttu-id="fc26e-107">Navigieren Sie zu [Anhang: HTML im Vergleich zum DOM,](#appendix-html-versus-the-dom) um eine Erklärung zu geben.</span><span class="sxs-lookup"><span data-stu-id="fc26e-107">Navigate to [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <a name="open-dom-examples"></a><span data-ttu-id="fc26e-108">Open DOM-Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc26e-108">Open DOM examples</span></span>  

1.  <span data-ttu-id="fc26e-109">Halten Sie `Control` \(Windows, Linux\) oder `Command` \(macOS\) gedrückt, und wählen Sie **DOM-Beispiele aus,** um sie auf einer neuen Registerkarte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="fc26e-110">DOM-Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc26e-110">DOM Examples</span></span>][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a><span data-ttu-id="fc26e-111">Anzeigen von DOM-Knoten</span><span class="sxs-lookup"><span data-stu-id="fc26e-111">View DOM nodes</span></span>  

<span data-ttu-id="fc26e-112">In der DOM-Struktur des Elements-Bereichs werden alle DOM-bezogenen Aktivitäten in DevTools ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc26e-112">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <a name="inspect-a-node"></a><span data-ttu-id="fc26e-113">Überprüfen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="fc26e-113">Inspect a node</span></span>  

<span data-ttu-id="fc26e-114">Wenn Sie an einem bestimmten DOM-Knoten interessiert sind, ist **Inspect** eine schnelle Möglichkeit, DevTools zu öffnen und diesen Knoten zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-114">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="fc26e-115">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-115">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-116">Wählen Sie unter **"Knoten überprüfen"** mit der rechten Maustaste **"Überprüfen"** **aus.**</span><span class="sxs-lookup"><span data-stu-id="fc26e-116">Under **Inspect a Node**, right-choose **Michelangelo** and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="fc26e-118">Überprüfen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="fc26e-118">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="fc26e-119">Das **Elementtool** von DevTools wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fc26e-119">The **Elements** tool of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="fc26e-120">ist in der **DOM-Struktur**hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="fc26e-120">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Hervorheben des Knotens "Knoten"" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="fc26e-122">Hervorheben des `Michelangelo` Knotens</span><span class="sxs-lookup"><span data-stu-id="fc26e-122">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="fc26e-123">Klicken Sie in der oberen linken Ecke von DevTools auf das Symbol **"Überprüfen** ![ \( Überprüfen ](../media/inspect-icon.msft.png) \)".</span><span class="sxs-lookup"><span data-stu-id="fc26e-123">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Das Inspect-Symbol" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="fc26e-125">Das \*\*\*\* Inspect-Symbol</span><span class="sxs-lookup"><span data-stu-id="fc26e-125">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="fc26e-126">Wählen Sie unter **"Knoten überprüfen"** den Text **"Tokio"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-126">Under **Inspect a Node**, choose the **Tokyo** text.</span></span>  <span data-ttu-id="fc26e-127">Wird nun `<li>Tokyo</li>` in der DOM-Struktur hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="fc26e-127">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="fc26e-128">Das Überprüfen eines Knotens ist auch der erste Schritt zum Anzeigen und Ändern der Formatvorlagen eines Knotens.</span><span class="sxs-lookup"><span data-stu-id="fc26e-128">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="fc26e-129">Navigieren Sie mit dem Anzeigen und Ändern von CSS zu [Erste Schritte.][DevToolsCssGetStarted]</span><span class="sxs-lookup"><span data-stu-id="fc26e-129">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a><span data-ttu-id="fc26e-130">Navigieren in der DOM-Struktur mit einer Tastatur</span><span class="sxs-lookup"><span data-stu-id="fc26e-130">Navigate the DOM Tree with a keyboard</span></span>  

<span data-ttu-id="fc26e-131">Nachdem Sie einen Knoten in der DOM-Struktur ausgewählt haben, können Sie mit ihrer Tastatur in der DOM-Struktur navigieren.</span><span class="sxs-lookup"><span data-stu-id="fc26e-131">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="fc26e-132">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-132">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-133">Wählen Sie unter **"DOM-Struktur mit Tastatur navigieren" mit**der rechten Maustaste **"Ringo"** aus, und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-133">Under **Navigate the DOM Tree with a Keyboard**, right-choose **Ringo** and choose **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="fc26e-134">ist in der DOM-Struktur ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="fc26e-134">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Überprüfen des Ringo-Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="fc26e-136">Überprüfen des `Ringo` Knotens</span><span class="sxs-lookup"><span data-stu-id="fc26e-136">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="fc26e-137">Wählen Sie die `Up` Pfeiltaste zweimal aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-137">Select the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="fc26e-138"> markiert ist.</span><span class="sxs-lookup"><span data-stu-id="fc26e-138">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Überprüfen des ul-Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="fc26e-140">Überprüfen des `ul` Knotens</span><span class="sxs-lookup"><span data-stu-id="fc26e-140">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="fc26e-141">Wählen Sie die `Left` Pfeiltaste aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-141">Select the `Left` arrow key.</span></span>  <span data-ttu-id="fc26e-142">Die `<ul>` Liste wird reduziert.</span><span class="sxs-lookup"><span data-stu-id="fc26e-142">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="fc26e-143">Wählen Sie erneut die `Left` Pfeiltaste aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-143">Select the `Left` arrow key again.</span></span>  <span data-ttu-id="fc26e-144">Das übergeordnete Element des `<ul>` Knotens ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="fc26e-144">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="fc26e-145">In diesem Fall ist dies die `<div>` mit der `navigate-the-dom-tree-with-a-keyboard-1` ID.</span><span class="sxs-lookup"><span data-stu-id="fc26e-145">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="fc26e-146">Wählen Sie die `Down` Pfeiltaste zweimal aus, damit Sie die gerade reduzierte Liste erneut ausgewählt `<ul>` haben.</span><span class="sxs-lookup"><span data-stu-id="fc26e-146">Select the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="fc26e-147">Es sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="fc26e-147">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="fc26e-148">Wählen Sie die `Right` Pfeiltaste aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-148">Select the `Right` arrow key.</span></span>  <span data-ttu-id="fc26e-149">Die Liste wird erweitert.</span><span class="sxs-lookup"><span data-stu-id="fc26e-149">The list expands.</span></span>  

### <a name="scroll-into-view"></a><span data-ttu-id="fc26e-150">Bildlauf in die Ansicht</span><span class="sxs-lookup"><span data-stu-id="fc26e-150">Scroll into view</span></span>  

<span data-ttu-id="fc26e-151">Beim Anzeigen der DOM-Struktur sind Sie möglicherweise an einem DOM-Knoten interessiert, der sich derzeit nicht im Viewport befindet.</span><span class="sxs-lookup"><span data-stu-id="fc26e-151">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="fc26e-152">Angenommen, Sie scrollen nach unten auf der Seite, und sie interessieren sich für den `<h1>` Knoten oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="fc26e-152">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="fc26e-153">**Mit einem Bildlauf in** die Ansicht können Sie den Viewport schnell neu positionieren, damit Sie den Knoten überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="fc26e-153">**Scroll into view** lets you quickly reposition the viewport so that you are able to review the node.</span></span>  

1.  <span data-ttu-id="fc26e-154">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-154">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-155">Klicken Sie unter **"In Ansicht scrollen"** mit der rechten Maustaste auf **"Magritte",** und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-155">Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="fc26e-156">Scrollen Sie zum Ende der DOM-Beispielseite.</span><span class="sxs-lookup"><span data-stu-id="fc26e-156">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="fc26e-157">Der `<li>Magritte</li>` Knoten sollte weiterhin in ihrer DOM-Struktur ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="fc26e-157">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="fc26e-158">Wenn nicht, wechseln Sie zurück zum [Bildlauf in](#scroll-into-view) die Ansicht, und beginnen Sie von vorn.</span><span class="sxs-lookup"><span data-stu-id="fc26e-158">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="fc26e-159">Zeigen Sie auf den Knoten, öffnen Sie `<li>Magritte</li>` das Kontextmenü \(Rechtsklick\), und wählen Sie **Bildlauf in die Ansicht**aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-159">Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.</span></span>  <span data-ttu-id="fc26e-160">Ihr Viewport scrollt wieder nach oben, sodass Sie den **Magritte-Knoten** überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="fc26e-160">Your viewport scrolls back up so that you may review the **Magritte** node.</span></span>  <span data-ttu-id="fc26e-161">Navigieren Sie zu [Anhang: Fehlende Optionen,](#appendix-missing-options) wenn Sie die Option **"In Ansicht** scrollen" nicht überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="fc26e-161">Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to review the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Bildlauf in die Ansicht" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="fc26e-163">Bildlauf in die Ansicht</span><span class="sxs-lookup"><span data-stu-id="fc26e-163">Scroll into view</span></span>**  
    :::image-end:::  

### <a name="search-for-nodes"></a><span data-ttu-id="fc26e-164">Suchen nach Knoten</span><span class="sxs-lookup"><span data-stu-id="fc26e-164">Search for nodes</span></span>  

<span data-ttu-id="fc26e-165">Sie können die DOM-Struktur nach Zeichenfolge, CSS-Selektor oder XPath-Auswahl durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-165">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="fc26e-166">Konzentrieren Sie den Cursor auf **das** Elementtool.</span><span class="sxs-lookup"><span data-stu-id="fc26e-166">Focus your cursor on the **Elements** tool.</span></span>  
1.  <span data-ttu-id="fc26e-167">Wählen Sie `Control` + `F` \(Windows, Linux\) oder `Command` + `F` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-167">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="fc26e-168">Die Suchleiste wird am unteren Rand der DOM-Struktur geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fc26e-168">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="fc26e-169">Geben Sie `The Moon is a Harsh Mistress` ein.</span><span class="sxs-lookup"><span data-stu-id="fc26e-169">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="fc26e-170">Der letzte Satz wird in der DOM-Struktur hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="fc26e-170">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Hervorheben der Abfrage in der Suchleiste" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="fc26e-172">Hervorheben der Abfrage in der Suchleiste</span><span class="sxs-lookup"><span data-stu-id="fc26e-172">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="fc26e-173">Wie oben erwähnt, unterstützt die Suchleiste auch CSS- und XPath-Selektoren.</span><span class="sxs-lookup"><span data-stu-id="fc26e-173">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <a name="edit-the-dom"></a><span data-ttu-id="fc26e-174">Bearbeiten des DOM</span><span class="sxs-lookup"><span data-stu-id="fc26e-174">Edit the DOM</span></span>  

<span data-ttu-id="fc26e-175">Sie können das DOM im Fly-Format bearbeiten und überprüfen, wie sich die Änderungen auf die Seite auswirken.</span><span class="sxs-lookup"><span data-stu-id="fc26e-175">You may edit the DOM on the fly and review how the changes affect the page.</span></span>  

### <a name="edit-content"></a><span data-ttu-id="fc26e-176">Inhalt bearbeiten</span><span class="sxs-lookup"><span data-stu-id="fc26e-176">Edit content</span></span>  

<span data-ttu-id="fc26e-177">Doppelklicken Sie zum Bearbeiten des Inhalts eines Knotens auf den Inhalt in der DOM-Struktur.</span><span class="sxs-lookup"><span data-stu-id="fc26e-177">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="fc26e-178">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-178">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-179">Klicken Sie unter **Inhalt bearbeiten**mit der rechten Maustaste auf **"Michelle",** und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-179">Under **Edit Content**, right-choose **Michelle** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="fc26e-180">Doppelklicken Sie in der DOM-Struktur auf `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="fc26e-180">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="fc26e-181">Doppelklicken Sie also auf den Text zwischen `<li>` und `</li>` .</span><span class="sxs-lookup"><span data-stu-id="fc26e-181">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="fc26e-182">Der Text wird hervorgehoben, um anzugeben, dass er ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="fc26e-182">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Bearbeiten des Texts" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="fc26e-184">Bearbeiten des Texts</span><span class="sxs-lookup"><span data-stu-id="fc26e-184">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="fc26e-185">Löschen Sie , geben Sie ein, und `Michelle` wählen Sie dann `Leela` `Enter` aus, um die Änderung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-185">Delete `Michelle`, type `Leela`, then select `Enter` to confirm the change.</span></span>  <span data-ttu-id="fc26e-186">Der Text im DOM ändert sich von **Michelle** zu **Leela**.</span><span class="sxs-lookup"><span data-stu-id="fc26e-186">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <a name="edit-attributes"></a><span data-ttu-id="fc26e-187">Bearbeiten von Attributen</span><span class="sxs-lookup"><span data-stu-id="fc26e-187">Edit attributes</span></span>  

<span data-ttu-id="fc26e-188">Doppelklicken Sie zum Bearbeiten von Attributen auf den Attributnamen oder -wert.</span><span class="sxs-lookup"><span data-stu-id="fc26e-188">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="fc26e-189">Befolgen Sie die Anweisungen, um zu erfahren, wie Sie einem Knoten Attribute hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-189">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="fc26e-190">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-190">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-191">Wählen Sie unter **"Attribute bearbeiten"** mit der rechten **Maustaste",** und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-191">Under **Edit Attributes**, right-choose **Howard** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="fc26e-192">Doppelklicken Sie auf `<li>` .</span><span class="sxs-lookup"><span data-stu-id="fc26e-192">Double-click `<li>`.</span></span>  <span data-ttu-id="fc26e-193">Der Text wird hervorgehoben, um anzugeben, dass der Knoten ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="fc26e-193">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Bearbeiten des Knotens" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="fc26e-195">Bearbeiten des Knotens</span><span class="sxs-lookup"><span data-stu-id="fc26e-195">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fc26e-196">Wählen Sie die `Right` Pfeiltaste aus, fügen Sie ein Leerzeichen hinzu, geben Sie `style="background-color:gold"` ein, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-196">Select the `Right` arrow key, add a space, type `style="background-color:gold"`, and then select `Enter`.</span></span>  <span data-ttu-id="fc26e-197">Die Hintergrundfarbe des Knotens ändert sich in Gold.</span><span class="sxs-lookup"><span data-stu-id="fc26e-197">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Hinzufügen eines Style-Attributs zum Knoten" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="fc26e-199">Hinzufügen eines `style` Attributs zum Knoten</span><span class="sxs-lookup"><span data-stu-id="fc26e-199">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <a name="edit-node-type"></a><span data-ttu-id="fc26e-200">Knotentyp bearbeiten</span><span class="sxs-lookup"><span data-stu-id="fc26e-200">Edit node type</span></span>  

<span data-ttu-id="fc26e-201">Doppelklicken Sie zum Bearbeiten des Knotentyps auf den Typ, und geben Sie dann den neuen Typ ein.</span><span class="sxs-lookup"><span data-stu-id="fc26e-201">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="fc26e-202">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-202">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-203">Klicken Sie unter **Knotentyp bearbeiten**mit der rechten Maustaste auf **"Hank",** und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-203">Under **Edit Node Type**, right-choose **Hank** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="fc26e-204">Doppelklicken Sie auf `<li>` .</span><span class="sxs-lookup"><span data-stu-id="fc26e-204">Double-click `<li>`.</span></span>  <span data-ttu-id="fc26e-205">Der Text `li` ist hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="fc26e-205">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="fc26e-206">Löschen `li` , eingeben , dann auswählen `button` `Enter` .</span><span class="sxs-lookup"><span data-stu-id="fc26e-206">Delete `li`, type `button`, then select `Enter`.</span></span>  <span data-ttu-id="fc26e-207">Der `<li>` Knoten wird in einen Knoten `<button>` geändert.</span><span class="sxs-lookup"><span data-stu-id="fc26e-207">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Ändern des Knotentyps in die Schaltfläche" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="fc26e-209">Ändern des Knotentyps in</span><span class="sxs-lookup"><span data-stu-id="fc26e-209">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a><span data-ttu-id="fc26e-210">Neu anordnen von DOM-Knoten</span><span class="sxs-lookup"><span data-stu-id="fc26e-210">Reorder DOM nodes</span></span>  

<span data-ttu-id="fc26e-211">Ziehen Sie Knoten, um sie neu anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-211">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="fc26e-212">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-212">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-213">Wählen Sie unter **"DOM-Knoten neu anordnen"** mit der rechten Maustaste **"Presley"** aus, und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-213">Under **Reorder DOM Nodes**, right-choose **Elvis Presley** and choose **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="fc26e-214">Es ist das letzte Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="fc26e-214">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="fc26e-215">Ziehen Sie in der DOM-Struktur `<li>Elvis Presley</li>` an den Anfang der Liste.</span><span class="sxs-lookup"><span data-stu-id="fc26e-215">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Ziehen Des Knotens an den Anfang der Liste" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="fc26e-217">Ziehen Des Knotens an den Anfang der Liste</span><span class="sxs-lookup"><span data-stu-id="fc26e-217">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <a name="force-state"></a><span data-ttu-id="fc26e-218">Erzwingen des Zustands</span><span class="sxs-lookup"><span data-stu-id="fc26e-218">Force state</span></span>  

<span data-ttu-id="fc26e-219">Sie können erzwingen, dass Knoten in Zuständen wie `:active` , `:hover` , und `:focus` `:visited` `:focus-within` verbleiben.</span><span class="sxs-lookup"><span data-stu-id="fc26e-219">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="fc26e-220">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-220">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-221">Zeigen Sie im **Zustand "Force"** auf **"TheRest of the Mof".**</span><span class="sxs-lookup"><span data-stu-id="fc26e-221">Under **Force state**, hover on **The Lord of the Flies**.</span></span>  <span data-ttu-id="fc26e-222">Die Hintergrundfarbe wird orange.</span><span class="sxs-lookup"><span data-stu-id="fc26e-222">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="fc26e-223">Zeigen Sie auf **"The Menu of the Maustaste",** öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-223">Hover on **The Lord of the Flies**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="fc26e-224">Zeigen Sie auf , öffnen Sie `<li class="demo--hover">The Lord of the Flies</li>` das Kontextmenü \(rechtsklick\), und wählen Sie **"Zustand erzwingen":Hover**  >  \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="fc26e-224">Hover on `<li class="demo--hover">The Lord of the Flies</li>`, open the contextual menu \(right-click\), and choose **Force State** > **:hover**.</span></span>  <span data-ttu-id="fc26e-225">Navigieren Sie zu [Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fc26e-225">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  <span data-ttu-id="fc26e-226">Die Hintergrundfarbe bleibt orange, auch wenn Sie nicht tatsächlich auf den Knoten zeigen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-226">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <a name="hide-a-node"></a><span data-ttu-id="fc26e-227">Ausblenden eines Knotens</span><span class="sxs-lookup"><span data-stu-id="fc26e-227">Hide a node</span></span>  

<span data-ttu-id="fc26e-228">Wählen Sie `H` diese Option aus, um einen Knoten auszublenden.</span><span class="sxs-lookup"><span data-stu-id="fc26e-228">Select `H` to hide a node.</span></span>  

1.  <span data-ttu-id="fc26e-229">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-229">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-230">Klicken Sie unter **"Knoten ausblenden"** mit der rechten Maustaste auf **"The Stars My Destination",** und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-230">Under **Hide a node**, right-choose **The Stars My Destination** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="fc26e-231">Wählen Sie den `H` Schlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-231">Select the `H` key.</span></span>  <span data-ttu-id="fc26e-232">Der Knoten ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="fc26e-232">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Wie der Knoten in der DOM-Struktur aussieht, nachdem er ausgeblendet wurde" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="fc26e-234">Wie der Knoten in der DOM-Struktur aussieht, nachdem er ausgeblendet wurde</span><span class="sxs-lookup"><span data-stu-id="fc26e-234">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="fc26e-235">Wählen Sie die `H` Taste erneut aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-235">Select the `H` key again.</span></span>  <span data-ttu-id="fc26e-236">Der Knoten wird erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc26e-236">The node is shown again.</span></span>  

### <a name="delete-a-node"></a><span data-ttu-id="fc26e-237">Löschen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="fc26e-237">Delete a node</span></span>  

<span data-ttu-id="fc26e-238">Wählen Sie `Delete` diese Option aus, um einen Knoten zu löschen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-238">Select `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="fc26e-239">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-239">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-240">Klicken Sie unter **"Knoten löschen"** mit der rechten Maustaste auf **"Foundation",** und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-240">Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="fc26e-241">Wählen Sie den `Delete` Schlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-241">Select the `Delete` key.</span></span>  <span data-ttu-id="fc26e-242">Der Knoten wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fc26e-242">The node is deleted.</span></span>  
    1.  <span data-ttu-id="fc26e-243">Wählen Sie `Control` + `Z` \(Windows, Linux\) oder `Command` + `Z` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-243">Select `Control`+`Z` \(Windows, Linux\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="fc26e-244">Die letzte Aktion wird rückgängig und der Knoten erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc26e-244">The last action is undone and the node reappears.</span></span>  

## <a name="access-nodes-in-the-console"></a><span data-ttu-id="fc26e-245">Zugriffsknoten in der Konsole</span><span class="sxs-lookup"><span data-stu-id="fc26e-245">Access nodes in the Console</span></span>  

<span data-ttu-id="fc26e-246">DevTools bietet einige Tastenkombinationen für den Zugriff auf DOM-Knoten über die Konsole oder zum Abrufen von JavaScript-Verweisen auf die einzelnen Knoten.</span><span class="sxs-lookup"><span data-stu-id="fc26e-246">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <a name="reference-the-currently-selected-node-with-0"></a><span data-ttu-id="fc26e-247">Verweisen Auf den aktuell ausgewählten Knoten mit $0</span><span class="sxs-lookup"><span data-stu-id="fc26e-247">Reference the currently-selected node with $0</span></span>  

<span data-ttu-id="fc26e-248">Wenn Sie einen Knoten untersuchen, bedeutet der `== $0` Text neben dem Knoten, dass Sie in der Konsole mit der Variablen auf diesen Knoten verweisen `$0` können.</span><span class="sxs-lookup"><span data-stu-id="fc26e-248">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="fc26e-249">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-249">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-250">Under **Reference the currently-selected node with $0**, right-choose **The left hand of Darkness** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="fc26e-250">Under **Reference the currently-selected node with $0**, right-choose **The Left Hand of Darkness** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="fc26e-251">Wählen Sie die `Escape` Taste aus, um die Konsolenschublade zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-251">Select the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="fc26e-252">Geben Sie `$0` den Schlüssel ein, und wählen Sie den `Enter` Schlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-252">Type `$0` and select the `Enter` key.</span></span>  <span data-ttu-id="fc26e-253">Das Ergebnis des Ausdrucks zeigt, dass `$0` ausgewertet `<li>The Left Hand of Darkness</li>` wird.</span><span class="sxs-lookup"><span data-stu-id="fc26e-253">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Das Ergebnis des ersten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="fc26e-255">Das Ergebnis des ersten `$0` **Ausdrucks** in der Konsole</span><span class="sxs-lookup"><span data-stu-id="fc26e-255">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="fc26e-256">Zeigen Sie auf das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="fc26e-256">Hover on the result.</span></span>  <span data-ttu-id="fc26e-257">Der Knoten wird im Viewport hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="fc26e-257">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="fc26e-258">Wählen Sie `<li>Dune</li>` in der DOM-Struktur aus, geben Sie `$0` die Konsole erneut ein, und wählen Sie dann `Enter` erneut aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-258">Choose `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then select `Enter` again.</span></span>  <span data-ttu-id="fc26e-259">Wird `$0` nun ausgewertet zu `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="fc26e-259">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Das Ergebnis des zweiten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="fc26e-261">Das Ergebnis des zweiten `$0` **Ausdrucks** in der Konsole</span><span class="sxs-lookup"><span data-stu-id="fc26e-261">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a><span data-ttu-id="fc26e-262">Store als globale Variable</span><span class="sxs-lookup"><span data-stu-id="fc26e-262">Store as global variable</span></span>  

<span data-ttu-id="fc26e-263">Wenn Sie mehrmals auf einen Knoten verweisen müssen, speichern Sie ihn als globale Variable.</span><span class="sxs-lookup"><span data-stu-id="fc26e-263">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="fc26e-264">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-264">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-265">Zeigen Sie unter **Store als globale Variable**auf **"The Big Sleep",** öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-265">Under **Store as global variable**, hover on **The Big Sleep**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="fc26e-266">Zeigen Sie `<li>The Big Sleep</li>` in der DOM-Struktur darauf, öffnen Sie das Kontextmenü \(Rechtsklick\), und wählen Sie **Store als globale Variable**aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-266">Hover on `<li>The Big Sleep</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Store as global variable**.</span></span>  <span data-ttu-id="fc26e-267">Navigieren Sie zu [Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fc26e-267">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="fc26e-268">Geben Sie `temp1` die Konsole ein, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-268">Type `temp1` in the Console and then select `Enter`.</span></span>  <span data-ttu-id="fc26e-269">Das Ergebnis des Ausdrucks zeigt, dass die Variable auf den Knoten ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="fc26e-269">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Das Ergebnis des ausdrucks temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="fc26e-271">Das Ergebnis des `temp1` Ausdrucks</span><span class="sxs-lookup"><span data-stu-id="fc26e-271">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <a name="copy-js-path"></a><span data-ttu-id="fc26e-272">JS-Pfad kopieren</span><span class="sxs-lookup"><span data-stu-id="fc26e-272">Copy JS path</span></span>  

<span data-ttu-id="fc26e-273">Kopieren Sie den JavaScript-Pfad zu einem Knoten, wenn Sie in einem automatisierten Test darauf verweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-273">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="fc26e-274">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-274">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-275">Zeigen Sie unter **"JS-Pfad kopieren"** auf **"TheZzov",** öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-275">Under **Copy JS path**, hover on **The Brothers Karamazov**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="fc26e-276">Zeigen Sie `<li>The Brothers Karamazov</li>` in der DOM-Struktur darauf, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie \*\*\*\*  >  **"JS-Pfad kopieren"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-276">Hover on `<li>The Brothers Karamazov</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="fc26e-277">Ein `document.querySelector()` Ausdruck, der in den Knoten aufgelöst wird, wurde in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="fc26e-277">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="fc26e-278">Wählen Sie `Control` + `V` \(Windows, Linux\) oder `Command` + `V` \(macOS\) aus, um den Ausdruck in die Konsole einzufügen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-278">Select `Control`+`V` \(Windows, Linux\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="fc26e-279">Wählen Sie `Enter` diese Option aus, um den Ausdruck auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="fc26e-279">Select `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Das Ergebnis des Ausdrucks "JS-Pfad kopieren"" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="fc26e-281">Das Ergebnis des Ausdrucks **"JS-Pfad kopieren"**</span><span class="sxs-lookup"><span data-stu-id="fc26e-281">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a><span data-ttu-id="fc26e-282">Unterbrechen von DOM-Änderungen</span><span class="sxs-lookup"><span data-stu-id="fc26e-282">Break on DOM changes</span></span>  

<span data-ttu-id="fc26e-283">Mit DevTools können Sie das JavaScript einer Seite anhalten, wenn javaScript das DOM ändert.</span><span class="sxs-lookup"><span data-stu-id="fc26e-283">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <a name="break-on-attribute-modifications"></a><span data-ttu-id="fc26e-284">Unterbrechen von Attributänderungen</span><span class="sxs-lookup"><span data-stu-id="fc26e-284">Break on attribute modifications</span></span>  

<span data-ttu-id="fc26e-285">Verwenden Sie Haltepunkte für die Attributänderung, wenn Sie das JavaScript anhalten möchten, das bewirkt, dass sich jedes Attribut eines Knotens ändert.</span><span class="sxs-lookup"><span data-stu-id="fc26e-285">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="fc26e-286">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-286">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-287">Klicken Sie unter **"Unterbrechen" auf Attributänderungen**mit der rechten Maustaste **auf",** und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-287">Under **Break on attribute modifications**, right-choose **Sauerkraut** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="fc26e-288">Zeigen Sie in der DOM-Struktur auf , öffnen Sie `<li id="target">Sauerkraut</li>` das Kontextmenü \(rechtsklick\), und wählen Sie **"Bei**  >  **Attributänderungen unterbrechen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-288">In the DOM Tree, hover on `<li id="target">Sauerkraut</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="fc26e-289">Navigieren Sie zu [Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fc26e-289">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Unterbrechen von Attributänderungen" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="fc26e-291">Unterbrechen von Attributänderungen</span><span class="sxs-lookup"><span data-stu-id="fc26e-291">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="fc26e-292">Im nächsten Schritt werden Sie angewiesen, eine Schaltfläche auszuwählen, mit der der Code der Seite angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="fc26e-292">In the next step you are going to be instructed to choose a button that pauses the code of the page.</span></span>  <span data-ttu-id="fc26e-293">Nachdem die Seite angehalten wurde, können Sie keinen Bildlauf mehr auf der Seite ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-293">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="fc26e-294">Sie müssen **"Skript fortsetzen"** \( ![ "Skript ](../media/resume-script-icon.msft.png) fortsetzen"\) auswählen, damit die Seite erneut bildlauffähig ist.</span><span class="sxs-lookup"><span data-stu-id="fc26e-294">You must choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Ort, an dem die Skriptausführung fortgesetzt werden soll" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="fc26e-296">Ort, an dem die Skriptausführung fortgesetzt werden soll</span><span class="sxs-lookup"><span data-stu-id="fc26e-296">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="fc26e-297">Klicken Sie oben auf die Schaltfläche **"Hintergrund festlegen".**</span><span class="sxs-lookup"><span data-stu-id="fc26e-297">Choose the **Set Background** button above.</span></span>  <span data-ttu-id="fc26e-298">Dadurch wird das `style` Attribut des Knotens auf `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="fc26e-298">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="fc26e-299">DevTools hält die Seite an und hebt den Code hervor, der zu einer Änderung des Attributs geführt hat.</span><span class="sxs-lookup"><span data-stu-id="fc26e-299">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="fc26e-300">Wählen Sie **"Skript fortsetzen"** \( ![ "Skript ](../media/resume-script-icon.msft.png) fortsetzen", wie bereits erwähnt).</span><span class="sxs-lookup"><span data-stu-id="fc26e-300">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\), as mentioned earlier.</span></span>  
    
### <a name="break-on-node-removal"></a><span data-ttu-id="fc26e-301">Unterbrechung beim Entfernen von Knoten</span><span class="sxs-lookup"><span data-stu-id="fc26e-301">Break on node removal</span></span>  

<span data-ttu-id="fc26e-302">Wenn Sie anhalten möchten, wenn ein bestimmter Knoten entfernt wird, verwenden Sie Haltepunkte zum Entfernen von Knoten.</span><span class="sxs-lookup"><span data-stu-id="fc26e-302">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="fc26e-303">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-303">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-304">Wählen Sie unter **"Unterbrechung beim Entfernen von Knoten"** mit der rechten Maustaste **"Doppelklicken"** aus, und wählen Sie **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-304">Under **Break on Node Removal**, right-choose **Neuromancer** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="fc26e-305">Zeigen Sie in der DOM-Struktur auf , öffnen Sie `<li id="target">Neuromancer</li>` das Kontextmenü \(rechtsklick\), und wählen Sie **"Beim**  >  **Entfernen von Knoten unterbrechen" aus.**</span><span class="sxs-lookup"><span data-stu-id="fc26e-305">In the DOM Tree, hover on `<li id="target">Neuromancer</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="fc26e-306">Navigieren Sie zu [Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fc26e-306">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="fc26e-307">Klicken Sie oben auf die Schaltfläche **"Löschen".**</span><span class="sxs-lookup"><span data-stu-id="fc26e-307">Choose the **Delete** button above.</span></span>  <span data-ttu-id="fc26e-308">DevTools hält die Seite an und hebt den Code hervor, der dazu führte, dass der Knoten entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="fc26e-308">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="fc26e-309">Wählen Sie **"Skript fortsetzen"** \( ![ "Skript ](../media/resume-script-icon.msft.png) fortsetzen" \) aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-309">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\).</span></span>  
    
### <a name="break-on-subtree-modifications"></a><span data-ttu-id="fc26e-310">Unterbrechen von Unterstrukturänderungen</span><span class="sxs-lookup"><span data-stu-id="fc26e-310">Break on subtree modifications</span></span>  

<span data-ttu-id="fc26e-311">Nachdem Sie einen Unterstrukturänderungs-Haltepunkt auf einem Knoten platziert haben, hält DevTools die Seite an, wenn eines der Nachfolger des Knotens hinzugefügt oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="fc26e-311">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="fc26e-312">[Open DOM Examples](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="fc26e-312">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="fc26e-313">Under **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="fc26e-313">Under **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="fc26e-314">Zeigen Sie in der DOM-Struktur auf den Knoten oben , öffnen Sie `<ul id="target">` `<li>A Fire Upon the Deep</li>` das Kontextmenü \(Rechtsklick\), und wählen Sie **"Bei**  >  **Unterstrukturänderungen unterbrechen"** aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-314">In the DOM Tree, hover on `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="fc26e-315">Wenn die Option nicht angezeigt wird, navigieren Sie zu [Anhang: Fehlende Optionen.](#appendix-missing-options)</span><span class="sxs-lookup"><span data-stu-id="fc26e-315">If the option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).</span></span>  
    1.  <span data-ttu-id="fc26e-316">Wählen Sie **Untergeordnetes hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-316">Choose **Add Child**.</span></span>  <span data-ttu-id="fc26e-317">Der Code wird angehalten, da der Liste ein `<li>` Knoten hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="fc26e-317">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="fc26e-318">Wählen Sie **"Skript fortsetzen"** \( ![ "Skript ](../media/resume-script-icon.msft.png) fortsetzen" \) aus.</span><span class="sxs-lookup"><span data-stu-id="fc26e-318">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\).</span></span>  
    
## <a name="next-steps"></a><span data-ttu-id="fc26e-319">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="fc26e-319">Next steps</span></span>  

<span data-ttu-id="fc26e-320">Dies deckt die meisten DOM-bezogenen Features in DevTools ab.</span><span class="sxs-lookup"><span data-stu-id="fc26e-320">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="fc26e-321">Sie können die restlichen Features ermitteln, indem Sie auf Knoten in der DOM-Struktur zeigen, das Kontextmenü \(Rechtsklick\) öffnen und mit den anderen Optionen experimentieren, die in diesem Lernprogramm nicht behandelt wurden.</span><span class="sxs-lookup"><span data-stu-id="fc26e-321">You are able to discover the rest of the features by hovering on nodes in the DOM Tree, opening the contextual menu \(right-click\), and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="fc26e-322">Navigieren Sie zu [Tastenkombinationen für den Elementbereich.][DevToolsShortcutsElements]</span><span class="sxs-lookup"><span data-stu-id="fc26e-322">Navigate to [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="fc26e-323">Sehen Sie sich die [Microsoft Edge DevTools-Homepage][MicrosoftEdgeDevTools] an, um alles zu entdecken, was Sie mit DevTools noch tun können.</span><span class="sxs-lookup"><span data-stu-id="fc26e-323">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a><span data-ttu-id="fc26e-324">Anhang: HTML im Vergleich zum DOM</span><span class="sxs-lookup"><span data-stu-id="fc26e-324">Appendix: HTML versus the DOM</span></span>  

<span data-ttu-id="fc26e-325">Im folgenden Abschnitt wird der Unterschied zwischen HTML und DOM schnell erläutert.</span><span class="sxs-lookup"><span data-stu-id="fc26e-325">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="fc26e-326">Wenn Sie einen Webbrowser verwenden, um eine Seite anzufordern, gibt der Server HTML wie den folgenden Codeausschnitt zurück.</span><span class="sxs-lookup"><span data-stu-id="fc26e-326">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="fc26e-327">Der Browser analysiert den HTML-Code und erstellt eine Struktur von Objekten wie die folgende Liste.</span><span class="sxs-lookup"><span data-stu-id="fc26e-327">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="fc26e-328">Diese Struktur von Objekten oder Knoten, die den Inhalt der Seite darstellen, wird dom genannt.</span><span class="sxs-lookup"><span data-stu-id="fc26e-328">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="fc26e-329">Derzeit sieht es wie der HTML-Code aus, aber nehmen wir an, dass das Skript, auf das unten im HTML-Code verwiesen wird, den folgenden Codeausschnitt ausführt.</span><span class="sxs-lookup"><span data-stu-id="fc26e-329">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="fc26e-330">Mit diesem Code wird der Knoten entfernt `h1` und dem DOM ein weiterer Knoten `p` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fc26e-330">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="fc26e-331">Das vollständige DOM zeigt nun die folgende Liste an.</span><span class="sxs-lookup"><span data-stu-id="fc26e-331">The complete DOM now displays the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="fc26e-332">Der HTML-Code für die Seite unterscheidet sich jetzt vom DOM.</span><span class="sxs-lookup"><span data-stu-id="fc26e-332">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="fc26e-333">Mit anderen Worten: HTML stellt den anfänglichen Seiteninhalt dar, und das DOM stellt den aktuellen Seiteninhalt dar.</span><span class="sxs-lookup"><span data-stu-id="fc26e-333">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="fc26e-334">Wenn JavaScript Knoten hinzufügt, entfernt oder bearbeitet, unterscheidet sich das DOM vom HTML-Code.</span><span class="sxs-lookup"><span data-stu-id="fc26e-334">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="fc26e-335">Navigieren Sie zu ["Einführung in das DOM",][MDNIntroductionToDOM] um mehr zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="fc26e-335">Navigate to [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a><span data-ttu-id="fc26e-336">Anhang: Fehlende Optionen</span><span class="sxs-lookup"><span data-stu-id="fc26e-336">Appendix: Missing options</span></span>  

<span data-ttu-id="fc26e-337">Viele der Anweisungen in diesem Lernprogramm weisen Sie an, auf einen Knoten in der DOM-Struktur zu zeigen, das Kontextmenü \(Rechtsklick\) zu öffnen und dann eine Option aus dem Kontextmenü auszuwählen, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fc26e-337">Many of the instructions in this tutorial instruct you to hover on a node in the DOM Tree, open the contextual menu \(right-click\), and then choose an option from the context menu that pops up.</span></span>  <span data-ttu-id="fc26e-338">Wenn die angegebene Option im Kontextmenü nicht angezeigt wird, versuchen Sie, mit dem Mauszeiger vom Knotentext wegzuzeigen und das Kontextmenü \(Rechtsklick\) zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fc26e-338">If the specified option in the context menu is not displayed, try hovering away from the node text and opening the contextual menu \(right-click\).</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Ort der Auswahl, ob nicht alle Optionen angezeigt werden" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="fc26e-340">Ort der Auswahl, ob nicht alle Optionen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="fc26e-340">Where to choose if all of the options are not displayed</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="fc26e-341">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="fc26e-341">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge \(Chromium\) | Microsoft-Dokumente"  
[DevToolsCssGetStarted]: ../css/index.md "Erste Schritte Mit Anzeigen und Ändern von CSS-| Microsoft-Dokumente"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Tastenkombinationen des Elements-Tools – Microsoft Edge DevTools-Tastenkombinationen | Microsoft-Dokumente"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chromium) DevTools-DOM-Beispiel | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in die DOM-| Mdn"  

> [!NOTE]
> <span data-ttu-id="fc26e-347">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc26e-347">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fc26e-348">Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/dom/index) zu finden und wurde von [Kaince-Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Ausrufebereich\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc26e-348">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="fc26e-350">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fc26e-350">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
