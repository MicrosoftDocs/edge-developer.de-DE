---
description: Eine Übersicht über die Interaktion mit der aktuellen Webseite im Browser mithilfe des Konsolentools
title: Verwenden der Konsole für die Interaktion mit dem DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 56ce6b1d8f1ad98eeb9c141c2e9b002e7679d7de
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597018"
---
# <a name="use-the-console-to-interact-with-the-dom"></a><span data-ttu-id="2a33c-104">Verwenden der Konsole für die Interaktion mit dem DOM</span><span class="sxs-lookup"><span data-stu-id="2a33c-104">Use the Console to interact with the DOM</span></span>

<span data-ttu-id="2a33c-105">Das **Konsolentool** dient nicht nur zum [Protokollieren von Informationen][DevtoolsConsoleConsoleLog] oder zum Ausführen von [beliebigem JavaScript.][DevtoolsConsoleConsoleJavascript]</span><span class="sxs-lookup"><span data-stu-id="2a33c-105">The **Console** tool isn't only for [logging information][DevtoolsConsoleConsoleLog] or to [run arbitrary JavaScript][DevtoolsConsoleConsoleJavascript].</span></span>  <span data-ttu-id="2a33c-106">Es ist auch eine hervorragende Möglichkeit, mit der Webseite im Browser zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="2a33c-106">It also is a great way to interact with the webpage in the browser.</span></span>  <span data-ttu-id="2a33c-107">Betrachten Sie es als Skriptumgebungsversion des **Inspect-Tools.**</span><span class="sxs-lookup"><span data-stu-id="2a33c-107">Consider it a script-environment version of the **Inspect** tool.</span></span>  

## <a name="read-from-the-dom"></a><span data-ttu-id="2a33c-108">Lesen aus dem DOM</span><span class="sxs-lookup"><span data-stu-id="2a33c-108">Read from the DOM</span></span>

<span data-ttu-id="2a33c-109">Führen Sie die folgenden Aktionen aus, um auf die Kopfzeile der Webseite zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-109">To reference the header of the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="2a33c-110">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="2a33c-110">Open the **Console**.</span></span>
    *   <span data-ttu-id="2a33c-111">Wählen Sie `Control` + `Shift` + `J` \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="2a33c-111">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="2a33c-112">Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn in die **Konsole**ein.</span><span class="sxs-lookup"><span data-stu-id="2a33c-112">Type or copy and paste the following code snippet in the **Console**.</span></span>  
    
    ```javascript
    document.querySelector('header')
    ```  
    
:::image type="complex" source="../media/console-dom-get-reference.msft.png" alt-text="Verwenden Sie document.querySelector, um einen Verweis auf die Kopfzeile in der Konsole abzurufen." lightbox="../media/console-dom-get-reference.msft.png":::
    <span data-ttu-id="2a33c-114">Verwenden Sie zum Abrufen eines Verweises auf die Kopfzeile in der Konsole</span><span class="sxs-lookup"><span data-stu-id="2a33c-114">To get a reference to the header in console, use</span></span> `document.querySelector`  
:::image-end:::  

<span data-ttu-id="2a33c-115">Wenn Sie `Shift` + `Tab` den Mauszeiger auswählen oder über das HTML-Ergebnis bewegen, hebt DevTools die Kopfzeile für Sie hervor.</span><span class="sxs-lookup"><span data-stu-id="2a33c-115">If you select `Shift`+`Tab` or move your mouse cursor over the HTML result, DevTools highlights the header for you.</span></span>  

:::image type="complex" source="../media/console-dom-highlight-element.msft.png" alt-text="DevTools hebt den abschnitt hervor, den Sie in der Konsole auswählen" lightbox="../media/console-dom-highlight-element.msft.png":::
    <span data-ttu-id="2a33c-117">DevTools hebt den abschnitt hervor, den Sie in der **Konsole** auswählen</span><span class="sxs-lookup"><span data-stu-id="2a33c-117">DevTools highlights the section you choose in the **Console**</span></span>  
:::image-end:::  

## <a name="manipulate-the-dom"></a><span data-ttu-id="2a33c-118">Bearbeiten des DOM</span><span class="sxs-lookup"><span data-stu-id="2a33c-118">Manipulate the DOM</span></span>

<span data-ttu-id="2a33c-119">Sie können auch die Webseite bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="2a33c-119">You may manipulate the webpage, too.</span></span>  <span data-ttu-id="2a33c-120">Wenn Sie z. B. **Folgendes**kopieren und einfügen oder in die Konsole eingeben, wird um die Kopfzeile ein grüner Rahmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a33c-120">For example, if you copy and paste or type the following into the **Console**, a green border displays around the header.</span></span>

```javascript
document.querySelector('header').style.border = '2em solid green'
```  

:::image type="complex" source="../media/console-dom-add-border.msft.png" alt-text="Verwenden Sie die Konsole, um einem Element einen Rahmen hinzuzufügen." lightbox="../media/console-dom-add-border.msft.png":::
    <span data-ttu-id="2a33c-122">Verwenden Sie die **Konsole,** um einem Element einen Rahmen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-122">To add a border to an element, use the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-123">Je nach Komplexität der Webseite kann es schwierig sein, das richtige Element zu finden, das bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a33c-123">Depending on the complexity of the webpage, It may be daunting to find the right element to manipulate.</span></span>  <span data-ttu-id="2a33c-124">Sie können jedoch das **Inspect-Tool** verwenden, um Ihnen zu helfen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-124">But you may use the **Inspect** tool to help you.</span></span>  <span data-ttu-id="2a33c-125">Angenommen, Sie möchten den `Documentation` Teil in der Kopfzeile bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="2a33c-125">Say you want to manipulate the `Documentation` part in the header.</span></span>

:::image type="complex" source="../media/console-dom-highlight-documentation.msft.png" alt-text="Anzeigen des Elements, das Sie auf dem Bildschirm überprüfen" lightbox="../media/console-dom-highlight-documentation.msft.png":::
    <span data-ttu-id="2a33c-127">Anzeigen des Elements, das Sie auf dem Bildschirm überprüfen</span><span class="sxs-lookup"><span data-stu-id="2a33c-127">Display the element that you inspect on the screen</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-128">Führen Sie die folgenden Aktionen aus, um einen direkten Verweis auf das zu bearbeitende Element zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a33c-128">To get a direct reference to the element to manipulate, complete the following actions.</span></span>  

1.  <span data-ttu-id="2a33c-129">Verwenden \*\*\*\* Sie das Inspect-Tool, um das Element auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-129">Use the **Inspect** tool to choose the element.</span></span>  

    :::image type="complex" source="../media/console-dom-use-inspector-to-get-element.msft.png" alt-text="Verwenden Sie zum Auswählen eines Elements das Tool Inspect" lightbox="../media/console-dom-use-inspector-to-get-element.msft.png":::
        <span data-ttu-id="2a33c-131">Verwenden Sie zum Auswählen eines Elements das **Tool Inspect**</span><span class="sxs-lookup"><span data-stu-id="2a33c-131">To choose an element, use the **Inspect** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2a33c-132">Wählen Sie es aus, und DevTools springt zum **Elementtool.**</span><span class="sxs-lookup"><span data-stu-id="2a33c-132">Choose it and DevTools jumps to the **Elements** tool.</span></span>  
1.  <span data-ttu-id="2a33c-133">Wählen Sie das `...` Menü neben dem Element in der DOM-Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="2a33c-133">Choose the `...` menu next to the element in the DOM tree.</span></span>  
    
    :::image type="complex" source="../media/console-dom-overflow-menu-in-elements.msft.png" alt-text="Das ausgewählte Element wird in der DOM-Struktur des Elements-Tools angezeigt, wählen Sie das Überlaufmenü aus, um weitere Features zu erhalten." lightbox="../media/console-dom-overflow-menu-in-elements.msft.png":::
        <span data-ttu-id="2a33c-135">Das ausgewählte Element wird in der DOM-Struktur des **Elements-Tools** angezeigt, wählen Sie das Überlaufmenü aus, um weitere Features zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a33c-135">The chosen element displays in the DOM tree of the **Elements** tool, choose the overflow menu to get more features</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2a33c-136">Öffnen Sie das Kontextmenü, und wählen Sie `Copy`  >  `Copy JS Path` .</span><span class="sxs-lookup"><span data-stu-id="2a33c-136">Open the contextual menu and choose `Copy` > `Copy JS Path`.</span></span>  
    
    :::image type="complex" source="../media/console-dom-copy-JS-path.msft.png" alt-text="Kopieren des JavaScript-Pfads aus einem Element in der DOM-Struktur des Elements-Tools" lightbox="../media/console-dom-copy-JS-path.msft.png":::
        <span data-ttu-id="2a33c-138">Kopieren des JavaScript-Pfads aus einem Element in der DOM-Struktur des **Elements-Tools**</span><span class="sxs-lookup"><span data-stu-id="2a33c-138">Copy the JavaScript path from an element in the DOM tree of the **Elements** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2a33c-139">Wechseln Sie zurück zur **Konsole,** und fügen Sie den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="2a33c-139">Go back to the **Console** and paste the command.</span></span>  
    
<span data-ttu-id="2a33c-140">Um den Text des Links zu `My Playground` ändern, fügen `.textContent = "My Playground"` Sie dem befehl, den Sie zuvor eingefügt haben, hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a33c-140">To change the text of the link to `My Playground`, add `.textContent = "My Playground"` to the command you previously pasted.</span></span>  

:::image type="complex" source="../media/console-dom-change-content.msft.png" alt-text="Verwenden der Konsole zum Ändern des Inhalts eines Elements" lightbox="../media/console-dom-change-content.msft.png":::
    <span data-ttu-id="2a33c-142">Verwenden der **Konsole** zum Ändern des Inhalts eines Elements</span><span class="sxs-lookup"><span data-stu-id="2a33c-142">Use the **Console** to change the content of an element</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-143">Verwenden Sie alle JavaScript-DOM-Manipulationen, die Sie in der **Konsole**ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="2a33c-143">Use any JavaScript DOM manipulations you want to do in the **Console**.</span></span>  <span data-ttu-id="2a33c-144">Um dies bequemer zu gestalten, enthält die **Konsole** einige Hilfsmethoden.</span><span class="sxs-lookup"><span data-stu-id="2a33c-144">To make it more convenient, the **Console** comes with a few helper methods.</span></span>  

## <a name="helpful-console-utility-methods"></a><span data-ttu-id="2a33c-145">Hilfreiche Konsolenhilfsmethoden</span><span class="sxs-lookup"><span data-stu-id="2a33c-145">Helpful Console utility methods</span></span>  

<span data-ttu-id="2a33c-146">Viele Komfortmethoden und Verknüpfungen stehen Ihnen als [Konsolendienstprogramme][DevtoolsConsoleUtilities]zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2a33c-146">Many convenience methods and shortcuts are available to you as [Console Utilities][DevtoolsConsoleUtilities].</span></span>  <span data-ttu-id="2a33c-147">Einige der Methoden sind unglaublich leistungsstark und sind Dinge, die Sie wahrscheinlich als eine Reihe von Anweisungen in der Vergangenheit geschrieben `console.log()` haben.</span><span class="sxs-lookup"><span data-stu-id="2a33c-147">Some of the methods are incredibly powerful and are things you probably wrote as a series of `console.log()` statements in the past.</span></span>

### <a name="the-power-to-the-"></a><span data-ttu-id="2a33c-148">Die Leistungsfähigkeit von $</span><span class="sxs-lookup"><span data-stu-id="2a33c-148">The power to the $</span></span>

<span data-ttu-id="2a33c-149">Die `$` hat in der **Konsole** besondere Möglichkeiten, und Sie können sich dies von jQuery merken.</span><span class="sxs-lookup"><span data-stu-id="2a33c-149">The `$` has special powers in **Console** and you may remember that from jQuery.</span></span>

*   `$_` <span data-ttu-id="2a33c-150">speichert das Ergebnis des letzten Befehls.</span><span class="sxs-lookup"><span data-stu-id="2a33c-150">stores the result of the last command.</span></span>  <span data-ttu-id="2a33c-151">Wenn Sie also eingeben `2 + 2` und auswählen und dann `Enter` `$_` eingeben, werden Sie von der **Konsole** `4` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a33c-151">So, if you type `2 + 2` and select `Enter`, and then type `$_`, the **Console** displays you `4`.</span></span>
*   `$0` <span data-ttu-id="2a33c-152">`$4`ist ein Stapel der zuletzt überprüften Elemente ist immer das `$0` neueste.</span><span class="sxs-lookup"><span data-stu-id="2a33c-152">to `$4` is a stack of the last inspected elements `$0` is always the newest one.</span></span>  <span data-ttu-id="2a33c-153">Im vorherigen Beispiel haben Sie also gerade das Element im **Inspect-Tool** ausgewählt und `$0.textContent = "My Playground"` denselben Effekt eingegeben.</span><span class="sxs-lookup"><span data-stu-id="2a33c-153">So in the earlier example, you just chose the element in the **Inspect** tool and type `$0.textContent = "My Playground"` to get the same effect.</span></span>
*   `$x()` <span data-ttu-id="2a33c-154">ermöglicht ihnen die Auswahl von DOM-Elementen mit XPATH.</span><span class="sxs-lookup"><span data-stu-id="2a33c-154">allows you to choose DOM elements using XPATH.</span></span>
*   `$()` <span data-ttu-id="2a33c-155">und `$$()` sind kürzere Versionen von for und `document.querySelector()` `document.querySelectorAll()` .</span><span class="sxs-lookup"><span data-stu-id="2a33c-155">and `$$()` are shorter versions of for `document.querySelector()` and `document.querySelectorAll()`.</span></span>  
    
<span data-ttu-id="2a33c-156">Der folgende Codeausschnitt ruft beispielsweise alle Links auf der Webseite \(kurz für \) ab `$$('a')` und zeigt die `document.querySelectorAll('a')` Verknüpfungen als sortierbare Tabelle zum Kopieren und Einfügen an, z. B. in Excel.</span><span class="sxs-lookup"><span data-stu-id="2a33c-156">For example, the following code snippet retrieves all the links in the webpage \(as `$$('a')` is short for `document.querySelectorAll('a')`\) and displays the links as a sortable table to copy and paste, for example, into Excel.</span></span>

```javascript
console.table($$('a'),['href','text']);
```  

:::image type="complex" source="../media/console-dom-get-all-links.msft.png" alt-text="Abrufen aller Links auf der Webseite und Anzeigen des Ergebnisses als Tabelle" lightbox="../media/console-dom-get-all-links.msft.png":::
    <span data-ttu-id="2a33c-158">Abrufen aller Links auf der Webseite und Anzeigen des Ergebnisses als Tabelle</span><span class="sxs-lookup"><span data-stu-id="2a33c-158">Get all links in the webpage and display the result as a table</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-159">Wenn Sie die Informationen jedoch nicht anzeigen möchten, sie aber als Daten abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="2a33c-159">However, if you don't want to display the information, but you want to grab it as data.</span></span>  <span data-ttu-id="2a33c-160">Die `$$('a')` Verknüpfung enthält die Ankerverknüpfungen und alle Eigenschaften für die einzelnen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-160">The `$$('a')` shortcut provides the anchor links and all of the properties for each one.</span></span>  <span data-ttu-id="2a33c-161">Das Problem besteht darin, dass Sie nur die Links und den zugehörigen Text verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="2a33c-161">The problem is that you only want the links and the related text.</span></span>  

:::image type="complex" source="../media/console-dom-too-much-link-information.msft.png" alt-text="Die $$-Verknüpfung gibt viel zu viele Informationen zurück." lightbox="../media/console-dom-too-much-link-information.msft.png":::
    <span data-ttu-id="2a33c-163">Die `$$` Verknüpfung gibt viel zu viele Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="2a33c-163">The `$$` shortcut returns far too much information</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-164">Die `$$` Verknüpfung verfügt über ein interessantes zusätzliches Feature.</span><span class="sxs-lookup"><span data-stu-id="2a33c-164">The `$$` shortcut has an interesting extra feature.</span></span>  <span data-ttu-id="2a33c-165">Anstatt ein reines `NodeList` Like `document.querySelectorAll()` zurückzugeben, erhalten Sie mit der `$$` Verknüpfung alle `Array` Methoden.</span><span class="sxs-lookup"><span data-stu-id="2a33c-165">Instead of returning a pure `NodeList` like `document.querySelectorAll()`, the `$$` shortcut gives you all of the `Array` methods.</span></span>  <span data-ttu-id="2a33c-166">Verwenden Sie `map()` die Methode, um die Informationen auf das zu reduzieren, was Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-166">Use `map()` method to reduce the information to what you need.</span></span>  

```javascript
$$('a').map(a => {
    return {url: a.href, text: a.innerText}
})
```  

<span data-ttu-id="2a33c-167">Der Codeausschnitt gibt ein Array aller Verknüpfungen als Objekte mit `url` und `text` Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="2a33c-167">The code snippet returns an Array of all the links as objects with `url` and `text` properties.</span></span>  

:::image type="complex" source="../media/console-dom-filter-link-data.msft.png" alt-text="Verwenden der Karte auf $$ zum Filtern von Informationen auf das absolute Minimum" lightbox="../media/console-dom-filter-link-data.msft.png":::
    <span data-ttu-id="2a33c-169">Verwenden der Zuordnung zum Filtern von `$$` Informationen bis zum minimalen Minimum</span><span class="sxs-lookup"><span data-stu-id="2a33c-169">Use map on `$$` to filter information down to the bare minimum</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-170">Sie sind noch nicht fertig, mehrere Links sind interne Links zur Webseite oder haben leeren Text.</span><span class="sxs-lookup"><span data-stu-id="2a33c-170">You aren't done yet, several links are internal links to the webpage or have empty text.</span></span>  <span data-ttu-id="2a33c-171">Verwenden Sie die Filtermethode, um die internen Links zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-171">Use the filter method to get rid of the internal links.</span></span>  

```javascript
$$('a').map(a => {
    return {text: a.innerText, url: a.href}
}).filter(a => {
    return a.text !== '' && !a.url.match('docs.microsoft.com')
})
```  

:::image type="complex" source="../media/console-dom-filter-out-empty-links.msft.png" alt-text="Abrufen der Links, die nicht leer und extern sind" lightbox="../media/console-dom-filter-out-empty-links.msft.png":::
    <span data-ttu-id="2a33c-173">Abrufen der Links, die nicht leer und extern sind</span><span class="sxs-lookup"><span data-stu-id="2a33c-173">Get the links that aren't empty and are external</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-174">Wie am Anfang der Webseite angezeigt, können Sie auch diese Elemente ändern.</span><span class="sxs-lookup"><span data-stu-id="2a33c-174">As displayed at the start of the webpage, you may also change these elements.</span></span>  <span data-ttu-id="2a33c-175">Der folgende Codeausschnitt erstellt beispielsweise einen grünen Rahmen um alle externen Links:</span><span class="sxs-lookup"><span data-stu-id="2a33c-175">For example, the following code snippet creates a green border around all external links:</span></span>

```javascript
$$('a[href^="https://"]').forEach(
  a => a.style.border = '1px solid green'
)
```  

:::image type="complex" source="../media/console-dom-highlight-links.msft.png" alt-text="Um alle externen Links hervorzuheben, fügen Sie jeweils einen grünen Rahmen hinzu." lightbox="../media/console-dom-highlight-links.msft.png":::
    <span data-ttu-id="2a33c-177">Um alle externen Links hervorzuheben, fügen Sie jeweils einen grünen Rahmen hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a33c-177">To highlight all external links, add a green border around each</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-178">Anstatt komplexes JavaScript zum Filtern von Ergebnissen zu schreiben, verwenden Sie die Leistungsfähigkeit von CSS-Selektoren.</span><span class="sxs-lookup"><span data-stu-id="2a33c-178">Instead of writing complex JavaScript to filter results, use the power of CSS selectors.</span></span>  

<span data-ttu-id="2a33c-179">Führen Sie die folgenden Aktionen aus, um eine Tabelle mit den Informationen für alle Bilder auf der Webseite zu erstellen, bei denen es sich nicht um `src` `alt` Inlinebilder handelt.</span><span class="sxs-lookup"><span data-stu-id="2a33c-179">To create a table of the `src` and `alt` information for all images on the webpage that aren't inline images, complete the following actions.</span></span>  

1.  <span data-ttu-id="2a33c-180">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="2a33c-180">Open the **Console**.</span></span>  
1.  <span data-ttu-id="2a33c-181">Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="2a33c-181">Type or copy and paste the following code snippet.</span></span>  

```javascript
console.table($$('img:not([src^=data])'), ['src','alt'])
```  

:::image type="complex" source="../media/console-dom-complex-CSS-selector.msft.png" alt-text="Verwenden Sie zum Auswählen von Elementen eine komplexe CSS-Auswahl" lightbox="../media/console-dom-complex-CSS-selector.msft.png":::
    <span data-ttu-id="2a33c-183">Verwenden Sie zum Auswählen von Elementen eine komplexe CSS-Auswahl</span><span class="sxs-lookup"><span data-stu-id="2a33c-183">To choose elements, use a complex CSS selector</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-184">Sind Sie bereit für ein noch komplexeres Beispiel?</span><span class="sxs-lookup"><span data-stu-id="2a33c-184">Ready for an even more complex example?</span></span>  <span data-ttu-id="2a33c-185">HTML-Webseiten, die aus Markdown wie diesem Artikel generiert werden, verfügen über automatische ID-Werte für jede Überschrift, damit Sie einen Deep-Link zu diesem Abschnitt erstellen können.</span><span class="sxs-lookup"><span data-stu-id="2a33c-185">HTML webpages generated from markdown like this article, have automatic ID values for each heading to allow you to deep link to that section.</span></span>  <span data-ttu-id="2a33c-186">Beispielsweise wird eine `# New features` Änderung an `<h1 id="new-features">New features</h1>` .</span><span class="sxs-lookup"><span data-stu-id="2a33c-186">For example, a `# New features` changes to `<h1 id="new-features">New features</h1>`.</span></span>  

<span data-ttu-id="2a33c-187">Führen Sie die folgenden Aktionen aus, um alle automatischen Überschriften aufzuführen, die kopiert und eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-187">To list of all of the automatic headings to copy and paste, complete the following actions.</span></span>  

1.  <span data-ttu-id="2a33c-188">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="2a33c-188">Open the **Console**.</span></span>  
1.  <span data-ttu-id="2a33c-189">Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="2a33c-189">Type or copy and paste the following code snippet.</span></span>  

```javascript
let out = '';
$$('#main [id]').filter(
    elm => {return elm.nodeName.startsWith('H')}
).forEach(elm => {
   out += elm.innerText + "\n" + 
          document.location.href + '#' +
          elm.id + "\n";
});
console.log(out);
```  

<span data-ttu-id="2a33c-190">Das Ergebnis ist Text, der Inhalte für jede Überschrift enthält, gefolgt von der vollständigen URL, die darauf zeigt.</span><span class="sxs-lookup"><span data-stu-id="2a33c-190">The result is text that contains content for each heading followed by the full URL that points to it.</span></span>  

:::image type="complex" source="../media/console-dom-get-generated-headings.msft.png" alt-text="Abrufen aller Überschriften und der generierten URLs von der Webseite" lightbox="../media/console-dom-get-generated-headings.msft.png":::
    <span data-ttu-id="2a33c-192">Abrufen aller Überschriften und der generierten URLs von der Webseite</span><span class="sxs-lookup"><span data-stu-id="2a33c-192">Get all the headings and the generated URLs from the webpage</span></span>  
:::image-end:::  

### <a name="clean-up-with-clear-and-copy"></a><span data-ttu-id="2a33c-193">Bereinigen mit "Löschen und Kopieren"</span><span class="sxs-lookup"><span data-stu-id="2a33c-193">Clean up with clear and copy</span></span>

<span data-ttu-id="2a33c-194">Bei der Entwicklung in der **Konsole**kann es unübersichtlich werden.</span><span class="sxs-lookup"><span data-stu-id="2a33c-194">When developing in the **Console**, things may get messy.</span></span>  <span data-ttu-id="2a33c-195">Möglicherweise ist es frustrierend, beim Kopieren und Einfügen ergebnisse auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-195">You may find it frustrating to try to choose results while you copy and paste.</span></span>  <span data-ttu-id="2a33c-196">Die folgenden beiden Hilfsmethoden helfen Ihnen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-196">The following two utility methods help you.</span></span>  

*   `copy()` <span data-ttu-id="2a33c-197">kopiert alles, was Sie in die Zwischenablage geben.</span><span class="sxs-lookup"><span data-stu-id="2a33c-197">copies whatever you give it to the clipboard.</span></span>  <span data-ttu-id="2a33c-198">Die `copy()` Methode ist besonders nützlich, wenn Sie sie mit dieser Kopie des letzten `$_` Ergebnisses kombinieren.</span><span class="sxs-lookup"><span data-stu-id="2a33c-198">The `copy()` method is especially useful when you mix it with `$_` that copies the last result.</span></span>
*   `clear()` <span data-ttu-id="2a33c-199">löscht die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="2a33c-199">clears the **Console**.</span></span>

### <a name="read-and-monitor-events"></a><span data-ttu-id="2a33c-200">Lesen und Überwachen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="2a33c-200">Read and monitor events</span></span>

<span data-ttu-id="2a33c-201">Zwei weitere interessante Hilfsmethoden der **Konsole** befassen sich mit der Ereignisbehandlung.</span><span class="sxs-lookup"><span data-stu-id="2a33c-201">Two other interesting utility methods of **Console** deal with event handling.</span></span>

*   `getEventListeners(node)` <span data-ttu-id="2a33c-202">Listet alle Ereignislistener eines Knotens auf.</span><span class="sxs-lookup"><span data-stu-id="2a33c-202">lists all the event listeners of a node.</span></span>
*   `monitorEvents(node, events)` <span data-ttu-id="2a33c-203">überwacht und protokolliert die Ereignisse, die auf einem Knoten auftreten.</span><span class="sxs-lookup"><span data-stu-id="2a33c-203">monitors and logs the events that happen on a node.</span></span>

<span data-ttu-id="2a33c-204">Führen Sie die folgenden Aktionen aus, um alle Ereignislistener aufzuführen, die dem ersten Formular auf der Webseite zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="2a33c-204">To list all of the event listener assigned to the first form in the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="2a33c-205">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="2a33c-205">Open the **Console**.</span></span>  
1.  <span data-ttu-id="2a33c-206">Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="2a33c-206">Type or copy and paste the following code snippet.</span></span>  
    
    ```javascript
    getEventListeners($('form')); 
    ```  

:::image type="complex" source="../media/console-dom-get-form-events.msft.png" alt-text="Abrufen aller Ereignislistener für das erste Formular auf der Webseite" lightbox="../media/console-dom-get-form-events.msft.png":::
    <span data-ttu-id="2a33c-208">Abrufen aller Ereignislistener für das erste Formular auf der Webseite</span><span class="sxs-lookup"><span data-stu-id="2a33c-208">Get all events listeners for the first form in the webpage</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-209">Beim Überwachen erhalten Sie jedes Mal eine Benachrichtigung in der **Konsole,** wenn sich etwas an den angegebenen Elementen ändert.</span><span class="sxs-lookup"><span data-stu-id="2a33c-209">When you monitor, you to get a notification in the **Console** every time something changes to the specified elements.</span></span>  <span data-ttu-id="2a33c-210">Sie definieren die Ereignisse, auf die Sie lauschen möchten, als zweiten Parameter.</span><span class="sxs-lookup"><span data-stu-id="2a33c-210">You define the events you want to listen to as a second parameter.</span></span>  <span data-ttu-id="2a33c-211">Es ist wichtig, dass Sie die Ereignisse definieren, die Sie überwachen möchten, andernfalls werden alle Ereignisse gemeldet, die mit dem Element geschehen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-211">It is important for you to define the events that you want to monitor, otherwise any event happening to the element is reported.</span></span>

<span data-ttu-id="2a33c-212">Führen Sie die folgenden Aktionen aus, um jedes Mal, wenn Sie einen Bildlauf durchführen, die Größe des Fensters ändern oder wenn der Benutzer eine Eingabe im Suchformular durchführt, eine Benachrichtigung in der **Konsole** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a33c-212">To get a notification in the **Console** every time you scroll, resize the window, or when the user types in the search form, complete the following actions.</span></span>  

1.  <span data-ttu-id="2a33c-213">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="2a33c-213">Open the **Console**.</span></span>  
1.  <span data-ttu-id="2a33c-214">Geben Sie den folgenden Codeausschnitt ein, oder kopieren Sie ihn, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="2a33c-214">Type or copy and paste the following code snippet.</span></span>  
    
    ```javascript
    monitorEvents(window, ['resize', 'scroll']);
    monitorEvents($0, 'keyup');
    ```  
    
:::image type="complex" source="../media/console-dom-monitor-events.msft.png" alt-text="Konsole zeigt jedes Bildlaufereignis an, das im Fenster auftritt" lightbox="../media/console-dom-monitor-events.msft.png":::
    <span data-ttu-id="2a33c-216">**Konsole** zeigt jedes Bildlaufereignis an, das im Fenster auftritt</span><span class="sxs-lookup"><span data-stu-id="2a33c-216">**Console** displays every scroll event that happens on the Window</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-217">Um eine Tastenaktion für das aktuell ausgewählte Element zu protokollieren, konzentrieren Sie sich auf das Suchformular in der Kopfzeile, und wählen Sie einige Schlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="2a33c-217">To log any key action on the currently chosen element, focus on the search form in the header and select some keys.</span></span>  

:::image type="complex" source="../media/console-dom-monitor-key-events.msft.png" alt-text="Konsole zeigt Keyupereignisse an, die im Formular auftreten" lightbox="../media/console-dom-monitor-key-events.msft.png":::
    <span data-ttu-id="2a33c-219">**Konsole** zeigt `keyup` Ereignisse an, die im Formular auftreten</span><span class="sxs-lookup"><span data-stu-id="2a33c-219">**Console** displays `keyup` events that happen on the form</span></span>  
:::image-end:::  

<span data-ttu-id="2a33c-220">Um sie zu beenden, entfernen Sie die von Ihnen festgelegte Überwachung mithilfe des folgenden Codeausschnitts.</span><span class="sxs-lookup"><span data-stu-id="2a33c-220">To stop it, remove the monitoring you set using the following code snippet.</span></span>  

```javascript
unmonitorEvents(window, ['resize', 'scroll']);
unmonitorEvents($0, 'key');
```  

## <a name="reuse-dom-manipulation-scripts"></a><span data-ttu-id="2a33c-221">Wiederverwenden von DOM-Manipulationsskripts</span><span class="sxs-lookup"><span data-stu-id="2a33c-221">Reuse DOM manipulation scripts</span></span>

<span data-ttu-id="2a33c-222">Möglicherweise ist es hilfreich, das DOM über die **Konsole**zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="2a33c-222">You may find it useful to manipulate the DOM from the **Console**.</span></span>  <span data-ttu-id="2a33c-223">Möglicherweise gelten bald die Einschränkungen der **Konsole** als Entwicklungsplattform.</span><span class="sxs-lookup"><span data-stu-id="2a33c-223">You may soon run into the limitations of the **Console** as a development platform.</span></span>  <span data-ttu-id="2a33c-224">Die gute Nachricht ist, dass das [Tool "Quellen"][DevtoolsSourcesIndex] in DevTools eine entwicklungsumgebung mit vollem Funktionsumfang bietet.</span><span class="sxs-lookup"><span data-stu-id="2a33c-224">The good news is that the [Sources][DevtoolsSourcesIndex] tool in DevTools offers a fully featured development environment.</span></span>  <span data-ttu-id="2a33c-225">Im **Tool "Quellen"** können Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-225">In the **Sources** tool, you may complete the following actions.</span></span>  

*   <span data-ttu-id="2a33c-226">Store Die Skripts für die **Konsole** als [Codeausschnitte.][DevToolsJavascriptSnippets]</span><span class="sxs-lookup"><span data-stu-id="2a33c-226">Store your scripts for the **Console** as [Snippets][DevToolsJavascriptSnippets].</span></span>  
*   <span data-ttu-id="2a33c-227">Führen Sie die Skripts auf einer Webseite mithilfe einer Tastenkombination oder des Editors aus.</span><span class="sxs-lookup"><span data-stu-id="2a33c-227">Run the scripts in a webpage using a keyboard shortcut or the editor.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2a33c-228">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="2a33c-228">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Konsole als JavaScript-Umgebung | Microsoft-Dokumente"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Protokolle im Konsolentool | Microsoft-Dokumente"  
[DevtoolsConsoleUtilities]: ./utilities.md "API-Referenz für Konsolenprogramme | Microsoft-Dokumente"  

[DevToolsJavascriptSnippets]: ../javascript/snippets.md "Ausführen von JavaScript-Codeausschnitten auf jeder Seite mit Microsoft Edge DevTools | Microsoft-Dokumente"  
[DevtoolsSourcesIndex]: ../sources/index.md "Übersicht über die Quellentools | Microsoft-Dokumente"  
