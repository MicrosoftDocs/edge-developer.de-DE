---
description: Um die Aktivierreihenfolge der Abschnitte einer Seite schnell anzuzeigen, verwenden Sie die Quellreihenfolgeanzeige im Barrierefreiheitstool rechts neben der Registerkarte "Formatvorlagen".
title: Testen Sie die Tastaturunterstützung mithilfe des Source Order Viewers
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 7e90221b581280a6eb63cee4d073622a80871903
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597411"
---
# <a name="test-keyboard-support-using-the-source-order-viewer"></a><span data-ttu-id="856cb-104">Testen Sie die Tastaturunterstützung mithilfe des Source Order Viewers</span><span class="sxs-lookup"><span data-stu-id="856cb-104">Test keyboard support using the Source Order Viewer</span></span>

<span data-ttu-id="856cb-105">Die Quellreihenfolge eines Dokuments ist für die Hilfstechnologie wichtig und kann sich von der Reihenfolge unterscheiden, in der Elemente auf der gerenderten Seite angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="856cb-105">The source order of a document is important for assistive technology, and can be different than the order in which elements appear on the rendered page.</span></span>  <span data-ttu-id="856cb-106">MitHILFE von CSS können Sie Seitenelemente visuell neu anordnen, was jedoch nicht bedeutet, dass Hilfstechnologien wie Sprachausgabe Seitenelemente in der gleichen Reihenfolge darstellen würden.</span><span class="sxs-lookup"><span data-stu-id="856cb-106">Using CSS, you can re-order page elements in a visual way, but that doesn't mean that assistive technology such as screen readers would represent page elements in the same order.</span></span>  

<span data-ttu-id="856cb-107">Um sicherzustellen, dass das Dokument eine logische Reihenfolge aufweist, können Sie die **Quellreihenfolgeanzeige** verwenden, um unterschiedliche Seitenelemente mit Zahlen zu beschriften, die die Reihenfolge im Quellcode des Dokuments angeben.</span><span class="sxs-lookup"><span data-stu-id="856cb-107">To ensure that the document has a logical order, you can use the **Source Order Viewer** to label different page elements with numbers that specify the order in the source code of the document.</span></span>  <span data-ttu-id="856cb-108">Die **Quellreihenfolgeanzeige** befindet sich auf der Registerkarte **"Barrierefreiheit"** (in der Nähe der Registerkarte **"Formatvorlagen").**</span><span class="sxs-lookup"><span data-stu-id="856cb-108">The **Source Order Viewer** is in the **Accessibility** tab (near the **Styles** tab).</span></span>


## <a name="analyzing-the-order-of-keyboard-access-through-sections-of-the-page"></a><span data-ttu-id="856cb-109">Analysieren der Reihenfolge des Tastaturzugriffs über Abschnitte der Seite</span><span class="sxs-lookup"><span data-stu-id="856cb-109">Analyzing the order of keyboard access through sections of the page</span></span>

<span data-ttu-id="856cb-110">Die [Demowebseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] weist eine gegenintuitive Aktivierreihenfolge auf, in der Tastaturbenutzer erst nach dem Tabulatoren über alle **Links "Mehr"** auf das Navigationsmenü in der Seitenleiste zugreifen.</span><span class="sxs-lookup"><span data-stu-id="856cb-110">The [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] has a counterintuitive tabbing order, where keyboard users access the sidebar navigation menu only after tabbing through all the **More** links.</span></span>  <span data-ttu-id="856cb-111">Das Navigationsmenü in der Seitenleiste ist als Verknüpfung gedacht, um tief in den Seiteninhalt zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="856cb-111">The sidebar navigation menu is meant to be a shortcut to reach deep into the page content.</span></span>  <span data-ttu-id="856cb-112">Da Sie jedoch die gesamte Seite durchlaufen müssen, bevor Sie das Navigationsmenü auf der Seitenleiste erreichen, ist dieses Navigationsmenü für Tastaturbenutzer wirkungslos.</span><span class="sxs-lookup"><span data-stu-id="856cb-112">But because you need to go through the entire page before you reach the sidebar navigation menu, that navigation menu is ineffective for keyboard users.</span></span>

<span data-ttu-id="856cb-113">Die `Tab` wichtigste Reihenfolge auf der Demoseite lautet:</span><span class="sxs-lookup"><span data-stu-id="856cb-113">The `Tab` key order on the demo page is:</span></span>
1. <span data-ttu-id="856cb-114">Das **Suchfeld** und dann die Schaltfläche **"Los"** für das **Suchfeld.**</span><span class="sxs-lookup"><span data-stu-id="856cb-114">The **Search** field, then the **go** button for the **Search** field.</span></span>
1. <span data-ttu-id="856cb-115">Die Schaltfläche **"Mehr"** im Abschnitt **"Katzen",** um zu einer "Katzen"-Webseite zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="856cb-115">The **More** button in the **Cats** section, to navigate to a "Cats" webpage.</span></span>  <span data-ttu-id="856cb-116">Dann die anderen Schaltflächen **"Mehr",** "Hunde", "Hunde", "Hunde", "Dogchen" und dann "Almacas".</span><span class="sxs-lookup"><span data-stu-id="856cb-116">Then the other **More** buttons, for Dogs, Sheep, Horses, and then Alpacas.</span></span>
1. <span data-ttu-id="856cb-117">Die blauen Links des Navigationsmenüs in der Seitenleiste: **Katzen,** **Hunde,** **Hunde, Hunde,** Hunde , **Hunde**und dann **Almacas**.</span><span class="sxs-lookup"><span data-stu-id="856cb-117">The blue links of the sidebar navigation menu: **Cats**, **Dogs**, **Sheep**, **Horses**, and then **Alpacas**.</span></span>
1. <span data-ttu-id="856cb-118">Das Textfeld für die Schenkung im Formular für die Gabe.</span><span class="sxs-lookup"><span data-stu-id="856cb-118">The donation textbox in the donation form.</span></span>
1. <span data-ttu-id="856cb-119">Die Schaltflächen in der oberen Navigationsleiste: **Home**, **Adopt a pet**, **Environs**, **Jobs**, and then **About Us**.</span><span class="sxs-lookup"><span data-stu-id="856cb-119">The buttons in the top navigation bar: **Home**, **Adopt a pet**, **Donate**, **Jobs**, and then **About Us**.</span></span>
1. <span data-ttu-id="856cb-120">Die obere Fensteroberfläche des Browsers.</span><span class="sxs-lookup"><span data-stu-id="856cb-120">The browser's top-of-window interface.</span></span>

<span data-ttu-id="856cb-121">Der Grund für die verwirrende `Tab` Tastenreihenfolge ist, dass die Reihenfolge, in der eine Tastatur verwendet wird, durch die Quellreihenfolge des Dokuments bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="856cb-121">The reason for the confusing `Tab` key order is that the order experienced when using a keyboard is determined by the source order of the document.</span></span>  <span data-ttu-id="856cb-122">Die Reihenfolge, in der eine Tastatur verwendet wird, kann mithilfe des Attributs für Elemente geändert `tabindex` werden, das dieses Element aus der Quellreihenfolge herausnimmt.</span><span class="sxs-lookup"><span data-stu-id="856cb-122">The order experienced using a keyboard can be modified using the `tabindex` attribute on elements, which takes that element out of the source order.</span></span>

<span data-ttu-id="856cb-123">Im Quellcode des Dokuments wird das Seitenleisten-Navigationsmenü hinter dem Hauptinhalt der Webseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="856cb-123">In the source code of the document, the sidebar navigation menu appears after the main content of the webpage.</span></span>  <span data-ttu-id="856cb-124">CSS wurde verwendet, um das Seitenleisten-Navigationsmenü über den meisten Hauptinhalten der Webseite zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="856cb-124">CSS was used to position the sidebar navigation menu above most of the main content of the webpage.</span></span> 

<span data-ttu-id="856cb-125">Sie können die Reihenfolge der Seitenelemente mithilfe der **Quellreihenfolgeanzeige** auf der **Barrierefreiheitsregisterkarte** testen.  Der **Source Order Viewer** ist ein experimentelles Feature.</span><span class="sxs-lookup"><span data-stu-id="856cb-125">You can test the order of page elements by using the **Source Order Viewer** in the **Accessibility** tab.  The **Source Order Viewer** is an experimental feature.</span></span> <span data-ttu-id="856cb-126">Für weitere Informationen navigieren Sie zur [Quellreihenfolgeanzeige.](../experimental-features/index.md#source-order-viewer)</span><span class="sxs-lookup"><span data-stu-id="856cb-126">For more information, navigate to [Source Order Viewer](../experimental-features/index.md#source-order-viewer).</span></span>


<span data-ttu-id="856cb-127">So aktivieren Sie die Quellreihenfolgeanzeige:</span><span class="sxs-lookup"><span data-stu-id="856cb-127">To turn on the Source Order Viewer:</span></span>

1.  <span data-ttu-id="856cb-128">Wählen Sie in DevTools oben rechts die Schaltfläche **Einstellungen** \( ![ Einstellungen Schaltfläche ](../media/settings-button-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="856cb-128">In DevTools, in the upper right, select the **Settings** \(![Settings button](../media/settings-button-icon.msft.png)\) button.</span></span>  

1.  <span data-ttu-id="856cb-129">Wählen Sie unter **Einstellungen** **Experimente**aus.</span><span class="sxs-lookup"><span data-stu-id="856cb-129">Below **Settings**, select **Experiments**.</span></span>  

1.  <span data-ttu-id="856cb-130">Aktivieren Sie das **Kontrollkästchen Quellreihenfolge-Viewer .**</span><span class="sxs-lookup"><span data-stu-id="856cb-130">Select the **Source Order Viewer** checkbox.</span></span>

1.  <span data-ttu-id="856cb-131">Wählen Sie in der oberen rechten Ecke der **Einstellungen** Seite **X** aus, um die Einstellungen Seite zu schließen.</span><span class="sxs-lookup"><span data-stu-id="856cb-131">In the upper-right corner of the **Settings** page, select **X** to close the Settings page.</span></span>  <span data-ttu-id="856cb-132">Oben in DevTools hat sich die Meldung geändert, dass **mindestens eine Einstellung geändert wurde, die ein erneutes Laden erfordert, um wirksam zu werden.**</span><span class="sxs-lookup"><span data-stu-id="856cb-132">At the top of DevTools, the message **One or more settings have changed which require a reload to take effect.**</span></span> <span data-ttu-id="856cb-133">wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="856cb-133">is displayed.</span></span>  <span data-ttu-id="856cb-134">Wählen Sie die Schaltfläche **"DevTools neu laden" aus.**</span><span class="sxs-lookup"><span data-stu-id="856cb-134">Select the **Reload DevTools** button.</span></span>



<span data-ttu-id="856cb-135">So aktivieren und verwenden Sie den Source Order Viewer mit der Demoseite:</span><span class="sxs-lookup"><span data-stu-id="856cb-135">To activate and use the Source Order Viewer, with the demo page:</span></span>

1.  <span data-ttu-id="856cb-136">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte.  Wählen Sie dann **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="856cb-136">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="856cb-137">Wählen Sie im Tool **"Elemente"** rechts auf der Registerkarte **"Formatvorlagen"** die Registerkarte **"Barrierefreiheit"** aus.</span><span class="sxs-lookup"><span data-stu-id="856cb-137">In the **Elements** tool, to the right of the **Styles** tab, select the **Accessibility** tab.</span></span>

1.  <span data-ttu-id="856cb-138">Aktivieren Sie im Abschnitt **"Source Order Viewer"** das Kontrollkästchen **"Quellreihenfolge anzeigen".**</span><span class="sxs-lookup"><span data-stu-id="856cb-138">In the **Source Order Viewer** section, select the **Show source order** checkbox.</span></span>  <span data-ttu-id="856cb-139">Auf der gerenderten Webseite werden Zahlen angezeigt, die die Reihenfolge entsprechend der Steuerung `Tab` durch die Reihenfolge der Codezeilen in der Quelldatei angeben.</span><span class="sxs-lookup"><span data-stu-id="856cb-139">In the rendered webpage, numbers appear, indicating the `Tab` order as controlled by the order of lines of code in the source file.</span></span>

1.  <span data-ttu-id="856cb-140">Wählen Sie in der DOM-Struktur im **Elementtool** ein Hauptlayoutelement aus, `header` z. B. das Element.</span><span class="sxs-lookup"><span data-stu-id="856cb-140">In the DOM tree in the **Elements** tool, select a major layout element, such as the `header` element.</span></span>  <span data-ttu-id="856cb-141">Numerische Überlagerungen werden nun in Abschnitten der gerenderten Seite angezeigt, die die Quellreihenfolge der verschiedenen Elemente angeben.</span><span class="sxs-lookup"><span data-stu-id="856cb-141">Numeric overlays are now displayed on sections of the rendered page, which indicate the source order of the different elements.</span></span> 

    :::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="Durch Aktivieren des Viewers für die Quellreihenfolge wird die Reihenfolge der Elemente in der Quelle als Überlagerungen auf der Seite angezeigt." lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
        <span data-ttu-id="856cb-143">Durch Aktivieren des Viewers für die **Quellreihenfolge** wird die Reihenfolge der Elemente in der Quelle als Überlagerungen auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="856cb-143">Activating the **Source Order Viewer** shows the order of the elements in the source as overlays on the page</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="856cb-144">Scrollen Sie auf der Seite, um alle numerischen Überlagerungen anzuzeigen, einschließlich des Seitenfußbereichs.</span><span class="sxs-lookup"><span data-stu-id="856cb-144">Scroll the page to see all of the numeric overlays, including on the page footer section.</span></span>


## <a name="see-also"></a><span data-ttu-id="856cb-145">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="856cb-145">See also</span></span>

*  [<span data-ttu-id="856cb-146">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="856cb-146">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="856cb-147">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="856cb-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
