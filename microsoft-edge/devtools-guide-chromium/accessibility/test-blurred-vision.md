---
description: Um zu überprüfen, ob eine Webseite mit verschwommener Sicht verwendet werden kann, verwenden Sie im Renderingtool die Dropdownliste "Sehschwächen emulieren".
title: Überprüfen Sie, ob die Seite mit verschwommener Sicht verwendet werden kann
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 2fc1a1cf7746591573fce07946c7fb11abf42705
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597450"
---
# <a name="verify-that-the-page-is-usable-with-blurred-vision"></a><span data-ttu-id="9e2cb-104">Überprüfen Sie, ob die Seite mit verschwommener Sicht verwendet werden kann</span><span class="sxs-lookup"><span data-stu-id="9e2cb-104">Verify that the page is usable with blurred vision</span></span>

<!-- Rendering tool: Emulate vision deficiencies: Blurred vision -->

<span data-ttu-id="9e2cb-105">Um verschwommenes Sehen zu simulieren, verwenden Sie im **Renderingtool** das Menü **"Sehschwächen emulieren".**</span><span class="sxs-lookup"><span data-stu-id="9e2cb-105">To simulate blurred vision, in the **Rendering** tool, use the **Emulate vision deficiencies** menu.</span></span>  <span data-ttu-id="9e2cb-106">Wenn Sie dieses Feature mit der Demowebseite verwenden, können Sie sehen, dass der Schlagschatten des Texts im oberen Menü das Lesen der Menüelemente erschwert.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-106">When you use this feature with the demo webpage, you can see that the drop shadow on the text in the upper menu makes it hard to read the menu items.</span></span>

<span data-ttu-id="9e2cb-107">So überprüfen Sie, ob eine Webseite mit verschwommener Vision verwendet werden kann:</span><span class="sxs-lookup"><span data-stu-id="9e2cb-107">To check whether a webpage is usable with blurred vision:</span></span>

1.  <span data-ttu-id="9e2cb-108">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-108">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="9e2cb-109">Wählen Sie **Esc** aus, um die Schublade am unteren Rand von DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-109">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="9e2cb-110">Wählen Sie das **+** Symbol oben in der Schublade aus, um die Liste der Tools anzuzeigen, und wählen Sie dann **Rendern**aus.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-110">Select the **+** icon at the top of the Drawer to display the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="9e2cb-111">Wählen Sie in der Dropdownliste **"Sehschwächen emulieren"** die Option **"Verschwommene Vision"** aus.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-111">In the **Emulate vision deficiencies** dropdown list, select **Blurred vision**.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="Simulieren einer verschwommenen Seite" lightbox="../media/a11y-testing-simulating-blur.msft.png":::
        <span data-ttu-id="9e2cb-113">Simulieren einer verschwommenen Seite</span><span class="sxs-lookup"><span data-stu-id="9e2cb-113">Simulating a blurred page</span></span>
    :::image-end:::

    <span data-ttu-id="9e2cb-114">Beachten Sie, dass `text-shadow` die CSS-Eigenschaft den Text der Menüelemente im oberen Menü nur schwer lesen kann.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-114">Notice that the `text-shadow` CSS property makes the text of the menu items difficult to read on the upper menu.</span></span> <span data-ttu-id="9e2cb-115">Überprüfen Sie z. B. **"Home",** **"Adopt a Pet"** und andere Menüelemente.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-115">For example, review the **Home**, **Adopt a Pet**, and other menu items.</span></span>
    
1.  <span data-ttu-id="9e2cb-116">Wählen Sie im **Renderingtool** unter **"Sehschwäche emulieren"** die Option **"Keine Emulation"** aus, um die unscharfe Sehsimulation zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-116">In the **Rendering** tool, in **Emulate vision deficiencies**, select **No emulation** to remove the blurred vision simulation.</span></span>


## <a name="see-also"></a><span data-ttu-id="9e2cb-117">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="9e2cb-117">See also</span></span>

*  [<span data-ttu-id="9e2cb-118">Emulieren von Sehstörungen</span><span class="sxs-lookup"><span data-stu-id="9e2cb-118">Emulate vision deficiencies</span></span>](emulate-vision-deficiencies.md)
*  [<span data-ttu-id="9e2cb-119">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="9e2cb-119">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9e2cb-120">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="9e2cb-120">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
