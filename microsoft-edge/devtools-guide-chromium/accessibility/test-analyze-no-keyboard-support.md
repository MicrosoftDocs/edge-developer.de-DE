---
description: Analysieren der fehlenden Tastaturunterstützung für ein Formular, das das div-Element mit dem Tool Inspect und der Registerkarte "Ereignislistener" verwendet.
title: Analysieren der Tastaturunterstützung für Formulare mithilfe von DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 16ec030ed433fc24d3b2b88bfb423a2479996dfe
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597453"
---
# <a name="analyze-keyboard-support-on-forms-using-the-devtools"></a><span data-ttu-id="50c91-104">Analysieren der Tastaturunterstützung für Formulare mithilfe von DevTools</span><span class="sxs-lookup"><span data-stu-id="50c91-104">Analyze keyboard support on forms using the DevTools</span></span>

<span data-ttu-id="50c91-105">In diesem Artikel wird das Tool **Inspect** und die Registerkarte **"Ereignislistener"** verwendet, um die fehlende Tastaturunterstützung auf einer Demoseite zu analysieren, die Schaltflächen enthält, die das `div` Element verwenden.</span><span class="sxs-lookup"><span data-stu-id="50c91-105">This article uses the **Inspect** tool and **Event Listeners** tab to analyze the lack of keyboard support on a demo page which has buttons that use the `div` element.</span></span>

<span data-ttu-id="50c91-106">Im Formular \*\* Einnahmen \*\* funktionieren die Schaltflächen Betrag und Zuordnen nicht mit einer Tastatur. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="50c91-106">On the **Donate** form, the amount buttons and **Donate** button doesn't work with a keyboard.</span></span>  <span data-ttu-id="50c91-107">Für das Debuggen des Gabeformulars müssen Sie verstehen, warum die fehlende Fokusformatierung nicht als Problem mit automatischen Testtools wie dem **Tool "Probleme"** gekennzeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="50c91-107">Debugging the donation form requires understanding why the lack of focus styling isn't flagged as a problem with automatic testing tools like the **Issues** tool.</span></span>  <span data-ttu-id="50c91-108">In diesem Beispiel werden die Schaltflächen mithilfe `div` von Elementen implementiert, die von diesen Tools nicht als Steuerelement in einem Formular erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="50c91-108">In this example, the buttons are implemented using `div` elements, which are not recognized by these tools as a control on a form.</span></span>

<span data-ttu-id="50c91-109">So verwenden Sie das Tool Inspect und die Registerkarte "Ereignislistener", um die fehlende Tastaturunterstützung auf der Demoseite zu analysieren:</span><span class="sxs-lookup"><span data-stu-id="50c91-109">To use the Inspect tool and Event Listeners tab to analyze the lack of keyboard support on the demo page:</span></span>

<!-- 1. Inspect tool: Accessibility section: keyboard-focusable row -->

1.  <span data-ttu-id="50c91-110">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="50c91-110">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>
    
1.  <span data-ttu-id="50c91-111">Wählen Sie die Schaltfläche **Inspect** \( ![ Inspect icon ](../media/inspect-icon.msft.png) \) in der oberen linken Ecke von DevTools aus, sodass die Schaltfläche hervorgehoben ist (blau).</span><span class="sxs-lookup"><span data-stu-id="50c91-111">Select the **Inspect** \(![Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="50c91-112">Zeigen Sie auf die Schaltflächen **50,** **100**und **200** Schenkungen.</span><span class="sxs-lookup"><span data-stu-id="50c91-112">Hover over the **50**, **100**, and **200** donation buttons.</span></span>  <span data-ttu-id="50c91-113">Das Tool Inspect wird auf der Webseite als Überlagerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="50c91-113">The Inspect tool appears on the webpage, as an overlay.</span></span>  <span data-ttu-id="50c91-114">Die **tastaturfokussierbare** Zeile des Inspect-Overlays zeigt, dass keine der Schaltflächen für den Betrag der Gabe über die Tastatur zugänglich ist, wie durch einen grauen Kreis mit diagonaler Linie angegeben.</span><span class="sxs-lookup"><span data-stu-id="50c91-114">The **keyboard-focusable** row of the Inspect overlay shows that none of the donation amount buttons are keyboard-accessible, as indicated by a gray circle with diagonal line.</span></span>  <span data-ttu-id="50c91-115">Die Schaltflächen haben keinen Namen und eine Rolle, `generic` da sie `div` Elemente sind, was bedeutet, dass die Schaltflächen für Hilfstechnologien nicht zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="50c91-115">The buttons have no name, and have a role of `generic` because they are `div` elements, which means that the buttons aren't accessible to assistive technology.</span></span>

    :::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="Die Überprüfung der Schaltflächen des Formulars zeigt, dass auf sie nicht über die Tastatur zugegriffen werden kann." lightbox="../media/a11y-testing-donation-button-info.msft.png":::
        <span data-ttu-id="50c91-117">Die Überprüfung der Schaltflächen des Formulars zeigt, dass auf sie nicht über die Tastatur zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="50c91-117">Inspecting the buttons of the form shows that they aren't keyboard-accessible</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="50c91-118">Wenn das **Tool Inspect** aktiv ist, wählen Sie auf der Webseite das Textfeld **"Andere** Eingabe" über der Schaltfläche **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="50c91-118">When the **Inspect** tool is active, on the webpage, select the **Other** input textbox, above the **Donate** button.</span></span>  <span data-ttu-id="50c91-119">Das \*\*\*\* Elementtool wird mit der DOM-Struktur für die Webseite geöffnet.</span><span class="sxs-lookup"><span data-stu-id="50c91-119">The **Elements** tool opens, showing the DOM tree for the webpage.</span></span>  <span data-ttu-id="50c91-120">Das Element `<input id="freedonation" class="smallinput">` ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="50c91-120">The element `<input id="freedonation" class="smallinput">` is selected.</span></span>

    ```html
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

    <span data-ttu-id="50c91-121">Die Verwendung des `label` Textfelds Other und der Elemente im `input` Textfeld Other ist gültig, d. h., die Beschriftung Other ist ordnungsgemäß mit dem Eingabetextfeld verknüpft. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="50c91-121">The use of the `label` and `input` elements on the **Other** textbox is valid, which means that the **Other** label is correctly linked with the input textbox.</span></span>  <span data-ttu-id="50c91-122">Auf `input` das Textfeld kann auch über die Tastatur zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="50c91-122">The `input` textbox is also keyboard-accessible.</span></span>  <span data-ttu-id="50c91-123">Der Rest des Markups des Formulars sind `div` Elemente, die einfach zu formatieren sind, aber keine semantische Bedeutung haben.</span><span class="sxs-lookup"><span data-stu-id="50c91-123">The rest of the form's markup are `div` elements, which are easy to style, but have no semantic meaning.</span></span>

    <!-- 2. Elements tool: Event Listeners tab -->

    <span data-ttu-id="50c91-124">Die Funktionalität des Formulars wird mit JavaScript erstellt, und Sie können dies testen, indem Sie die Registerkarte **Ereignislistener** wie folgt überprüfen.</span><span class="sxs-lookup"><span data-stu-id="50c91-124">The form's functionality is created with JavaScript, and you can test this by checking the **Event Listeners** tab, as follows.</span></span>

1.  <span data-ttu-id="50c91-125">Wenn das Element `<input id="freedonation" class="smallinput">` weiterhin in der DOM-Struktur ausgewählt ist, wählen Sie rechts neben der Registerkarte **"Formatvorlagen"** die Registerkarte **"Ereignislistener"** aus, und erweitern Sie dann den `click` Ereignislistener.</span><span class="sxs-lookup"><span data-stu-id="50c91-125">With the element `<input id="freedonation" class="smallinput">` still selected in the DOM tree, select the **Event Listeners** tab to the right of the **Styles** tab, and then expand the `click` event listener.</span></span>

    :::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="Das Ereignislistener-Tool, das Ihnen zeigt, wo das JavaScript das Formular funktioniert" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
        <span data-ttu-id="50c91-127">Das Ereignislistener-Tool, das Ihnen zeigt, wo das JavaScript das Formular funktioniert</span><span class="sxs-lookup"><span data-stu-id="50c91-127">The Event listeners tool showing you where the JavaScript is that makes the form work</span></span>
    :::image-end:::

1.  <span data-ttu-id="50c91-128">Wählen Sie den `buttons.js:18` Link aus.</span><span class="sxs-lookup"><span data-stu-id="50c91-128">Select the `buttons.js:18` link.</span></span>  <span data-ttu-id="50c91-129">Das **Tool "Quellen"** wird mit dem angewendeten JavaScript geöffnet.</span><span class="sxs-lookup"><span data-stu-id="50c91-129">The **Sources** tool opens, showing the applied JavaScript.</span></span>

    :::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="Der JavaScript-Code, der für die Funktionalität des Schenkungsformulars verantwortlich ist, dargestellt im Tool "Quellen"." lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
        <span data-ttu-id="50c91-131">Der JavaScript-Code, der für die Funktionalität des Schenkungsformulars verantwortlich ist, dargestellt im Tool "Quellen".</span><span class="sxs-lookup"><span data-stu-id="50c91-131">The JavaScript responsible for the donation form's functionality, shown in the Sources tool</span></span>
    :::image-end:::

```javascript
donations.addEventListener('click', e => {
  let t = e.target;
  if (t.classList.contains('donationbutton')) {
    if (currentbutton) { currentbutton.classList.remove('current'); }
    t.classList.add('current');
    currentbutton = t;
    e.preventDefault();
  }
  if (t.classList.contains('submitbutton')) {
    alert('Thanks for your donation!')
  } 
})
```

<span data-ttu-id="50c91-132">Die Verwendung eines `click` Ereignisses zum Lesen der Schaltflächen ist eine bewährte Methode, da ein `click` Ereignis sowohl beim Mauszeiger als auch bei der Tastaturinteraktion ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="50c91-132">Using a `click` event to read the buttons is good practice, because a `click` event fires both on mouse pointer and keyboard interaction.</span></span>  <span data-ttu-id="50c91-133">Da auf ein Element jedoch `div` nicht über die Tastatur zugegriffen werden kann und diese Schaltfläche \*\* Hilfe \*\* als Element ( ) implementiert ist, `div` wird diese `<div class="submitbutton">Donate</div>` JavaScript-Funktion nur ausgeführt, wenn Sie eine Maus oder eine andere Quelle eines `click` Ereignisses verwenden, z. B. eine spezielle Schaltfläche, die auf einigen Tastaturen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="50c91-133">However, because a `div` element isn't keyboard-accessible, and this **Donate** button is implemented as a `div` element (`<div class="submitbutton">Donate</div>`), this JavaScript functionality never runs unless you use a mouse or another source of a `click` event, such as a special button available on some keyboards.</span></span>

<span data-ttu-id="50c91-134">Dies ist ein klassisches Beispiel, in dem JavaScript hinzugefügt wurde, um Funktionen zu erstellen, die `button` Elemente nativ bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="50c91-134">This is a classic example where JavaScript was added to create functionality that `button` elements provide natively.</span></span>  <span data-ttu-id="50c91-135">Das Simulieren der Funktionalität von Schaltflächen mit `div` Elementen hat zu einer unzugänglichen Erfahrung führen können.</span><span class="sxs-lookup"><span data-stu-id="50c91-135">Simulating the functionality of buttons with `div` elements ended up producing an inaccessible experience.</span></span>


## <a name="see-also"></a><span data-ttu-id="50c91-136">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="50c91-136">See also</span></span>

*  [<span data-ttu-id="50c91-137">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="50c91-137">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="50c91-138">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="50c91-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
