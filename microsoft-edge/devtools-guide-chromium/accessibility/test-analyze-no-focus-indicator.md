---
description: Analyse der fehlenden Anzeige des Tastaturfokus in einem Randleistenmenü aufgrund einer fehlenden CSS-Pseudoklassenregel für den Fokusstatus eines Links in Kombination mit dem Link ohne Gliederungseinstellung.
title: Analysieren Sie die fehlenden Anzeige des Tastaturfokus in einem Randleistenmenü
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 3626de9bdc2cce266efafe4b1b2e8fff501a74f7
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597461"
---
# <a name="analyze-the-lack-of-indication-of-keyboard-focus-in-a-sidebar-menu"></a><span data-ttu-id="779d7-104">Analysieren Sie die fehlenden Anzeige des Tastaturfokus in einem Randleistenmenü</span><span class="sxs-lookup"><span data-stu-id="779d7-104">Analyze the lack of indication of keyboard focus in a sidebar menu</span></span>

<!-- Inspect tool, and CSS rules: pseudo-classes for states -->

<span data-ttu-id="779d7-105">Auf der Demoseite für Barrierefreiheitstests zeigt das Seitenleisten-Navigationsmenü mit blauen Links nicht visuell an, welcher Link den Fokus hat, wenn eine Tastatur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="779d7-105">In the accessibility-testing demo page, the sidebar navigation menu with blue links doesn't visually indicate which link has focus, when using a keyboard.</span></span>  <span data-ttu-id="779d7-106">Um herauszufinden, warum das Seitenleistenmenü für Tastaturbenutzer verwirrend ist, suchen wir nach CSS-Pseudoklassenregeln für die `hover` `focus` Und-Zustände sowie nach der CSS-Eigenschaft für Linkgliederungen.</span><span class="sxs-lookup"><span data-stu-id="779d7-106">To find out why the sidebar menu is confusing to keyboard users, we'll look for CSS pseudo-class rules for the `hover` and `focus` states, along with the CSS property for link outlines.</span></span>  

<span data-ttu-id="779d7-107">Bei dieser Analyse wird festgestellt, dass die fehlende Anzeige des Tastaturfokus in den Links des Navigationsmenüs auf der Seitenleiste auf Folgendes zurückzuführen ist:</span><span class="sxs-lookup"><span data-stu-id="779d7-107">This analysis finds that the lack of indication of keyboard focus in the links of the sidebar navigation menu is because:</span></span>
*  <span data-ttu-id="779d7-108">Die `a` Links haben eine CSS-Eigenschaftseinstellung von `outline: none` .</span><span class="sxs-lookup"><span data-stu-id="779d7-108">The `a` links have a CSS property setting of `outline: none`.</span></span>
*  <span data-ttu-id="779d7-109">Den `a` Verknüpfungen fehlt eine CSS-Pseudoklassenregel für den `:focus` Zustand.</span><span class="sxs-lookup"><span data-stu-id="779d7-109">The `a` links lack a CSS pseudo-class rule for the `:focus` state.</span></span>

<span data-ttu-id="779d7-110">Um zum CSS zu navigieren, verwenden wir das Tool **Inspect,** um einen blauen Link im Navigationsmenü auf der Seitenleiste hervorzuheben, und zeigen dann die DOM-Struktur und CSS für das Element an, das `a` diese Verknüpfung definiert.</span><span class="sxs-lookup"><span data-stu-id="779d7-110">To navigate to the CSS, we'll use the **Inspect** tool to highlight a blue link on the sidebar navigation menu, and then view the DOM tree and CSS for the `a` element that defines that link.</span></span>

1.  <span data-ttu-id="779d7-111">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="779d7-111">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="779d7-112">Wählen Sie die Schaltfläche **Inspect** \( ![ Inspect icon ](../media/inspect-icon.msft.png) \) in der oberen linken Ecke von DevTools aus, sodass die Schaltfläche hervorgehoben ist (blau).</span><span class="sxs-lookup"><span data-stu-id="779d7-112">Select the **Inspect** \(![Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="779d7-113">Zeigen Sie im Navigationsmenü der Seitenleiste auf den blauen **Katzenlink.**</span><span class="sxs-lookup"><span data-stu-id="779d7-113">Hover over the blue **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="779d7-114">Die Inspect-Überlagerung wird angezeigt und zeigt an, dass das `a` Element tastaturfokussierbar ist.</span><span class="sxs-lookup"><span data-stu-id="779d7-114">The Inspect overlay appears, showing that the `a` element is keyboard-focusable.</span></span>  <span data-ttu-id="779d7-115">Die Überlagerung zeigt jedoch nicht an, dass es keine visuellen Hinweise gibt, wenn der Link den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="779d7-115">But the overlay doesn't show that there's no visual indication when the link has focus.</span></span>

    <span data-ttu-id="779d7-116">Als Nächstes überprüfen wir das CSS-Format dieses Links.</span><span class="sxs-lookup"><span data-stu-id="779d7-116">Next, we'll inspect the CSS styling of this link.</span></span>
 
1.  <span data-ttu-id="779d7-117">Wählen Sie im Navigationsmenü der Seitenleiste den Link **"Katzen"** aus.</span><span class="sxs-lookup"><span data-stu-id="779d7-117">Select the **Cats** link in the sidebar navigation menu.</span></span>  <span data-ttu-id="779d7-118">Das Tool **Inspect** wird deaktiviert, und **das** Elementtool wird geöffnet, wobei der Knoten in der `a` DOM-Struktur hervorgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="779d7-118">The **Inspect** tool turns off, and the **Elements** tool opens, highlighting the `a` node in the DOM tree.</span></span>

1.  <span data-ttu-id="779d7-119">Wählen Sie die Registerkarte **"Formatvorlagen" aus.**  Die CSS-Regel `#sidebar nav li a` wird zusammen mit einem Link zu einer Zeilennummer in `styles.css` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="779d7-119">Select the **Styles** tab.  The CSS rule `#sidebar nav li a` appears, along with a link to a line number in `styles.css`.</span></span>

    :::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Überprüfen des Quellcodes und der angewendeten Formatvorlagen eines Links im Menü" lightbox="../media/a11y-testing-menu-link.msft.png":::
        <span data-ttu-id="779d7-121">Überprüfen des Quellcodes und der angewendeten Formatvorlagen eines Links im Menü</span><span class="sxs-lookup"><span data-stu-id="779d7-121">Inspecting the source code and the applied styles of a link in the menu</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="779d7-122">Wählen Sie den Link zur CSS-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="779d7-122">Select the link to the CSS file.</span></span>  <span data-ttu-id="779d7-123">Die CSS-Datei wird im **Tool "Quellen"** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="779d7-123">The CSS file opens within the **Sources** tool.</span></span>

    :::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Die Formatvorlagen, die auf den Link im Quellentool angewendet werden" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
        <span data-ttu-id="779d7-125">Die Formatvorlagen, die auf den Link im Quellentool angewendet werden</span><span class="sxs-lookup"><span data-stu-id="779d7-125">The styles applied to the link in the Sources tool</span></span>
    :::image-end:::
    
<span data-ttu-id="779d7-126">Die Formatvorlagen der Seite weisen eine CSS-Pseudoklassenregel für den Zustand auf, die `hover` angibt, welches Menüelement Sie verwenden, wenn Sie eine Maus verwenden: `#sidebar nav li a:hover` .</span><span class="sxs-lookup"><span data-stu-id="779d7-126">The styles of the page have a CSS pseudo-class rule for the `hover` state that indicates which menu item you are on when you use a mouse: `#sidebar nav li a:hover`.</span></span>  <span data-ttu-id="779d7-127">Es gibt jedoch keine CSS-Pseudoklassenregel für den `focus` Zustand, um visuell anzugeben, welches Menüelement Sie verwenden, wenn Sie eine Tastatur verwenden, z. `#sidebar nav li a:focus` B. .</span><span class="sxs-lookup"><span data-stu-id="779d7-127">However, there is no CSS pseudo-class rule for the `focus` state to visually indicate which menu item you are on when you use a keyboard, such as `#sidebar nav li a:focus`.</span></span>

<span data-ttu-id="779d7-128">Beachten Sie außerdem, dass die Links eine CSS-Eigenschaftseinstellung von `outline: none` haben.</span><span class="sxs-lookup"><span data-stu-id="779d7-128">Also, notice that the links have a CSS property setting of `outline: none`.</span></span>  <span data-ttu-id="779d7-129">Dies ist eine gängige Vorgehensweise, um die Gliederung zu entfernen, die Browser elementen automatisch hinzufügen, wenn Sie sich über eine Tastatur darauf konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="779d7-129">This is a common practice, to remove the outline which browsers automatically add to elements when you focus on them using a keyboard.</span></span>  <span data-ttu-id="779d7-130">Wenn Sie `focus` keine Formatierung verwenden, ist dies für Ihre Benutzer verwirrend.</span><span class="sxs-lookup"><span data-stu-id="779d7-130">Not using `focus` styling causes confusion for your users.</span></span>


## <a name="see-also"></a><span data-ttu-id="779d7-131">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="779d7-131">See also</span></span> 

*  [<span data-ttu-id="779d7-132">Nachverfolgen, welches Element den Fokus hat</span><span class="sxs-lookup"><span data-stu-id="779d7-132">Track which element has focus</span></span>](focus.md)
*  [<span data-ttu-id="779d7-133">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="779d7-133">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="779d7-134">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="779d7-134">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
