---
description: Überprüfen Sie, ob Webseiten von Personen mit Farbenblindheit verwendet werden können, indem Sie die Dropdownliste "Sehschwächen emulieren" im Renderingtool verwenden.
title: Stellen Sie sicher, dass die Seite von Personen mit Farbblindheit verwendet werden kann
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 54cd7230f0402bfeb4b5ee28d2bcd0947794676f
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597448"
---
# <a name="verify-that-the-page-is-usable-by-people-with-color-blindness"></a><span data-ttu-id="a3182-104">Stellen Sie sicher, dass die Seite von Personen mit Farbblindheit verwendet werden kann</span><span class="sxs-lookup"><span data-stu-id="a3182-104">Verify that the page is usable by people with color blindness</span></span>

<!-- Rendering tool: Emulate vision deficiencies: Protanopia -->

<span data-ttu-id="a3182-105">Um zu überprüfen, ob eine Webseite von Personen mit Farbenblindheit verwendet werden kann, verwenden Sie im **Renderingtool** die Dropdownliste **"Sehschwächen emulieren".**</span><span class="sxs-lookup"><span data-stu-id="a3182-105">To check that a webpage is usable by people with color blindness, in the **Rendering** tool, use the **Emulate vision deficiencies** dropdown list.</span></span>

<span data-ttu-id="a3182-106">Auf der Demo-Webseite für Barrierefreiheitstests verwenden die verschiedenen Schenkungszustände Farbe als einzige Möglichkeit zur Differenzierung.</span><span class="sxs-lookup"><span data-stu-id="a3182-106">On the accessibility-testing demo webpage, the different donation states use color as the only means of differentiation.</span></span>
*  <span data-ttu-id="a3182-107">Grün bedeutet, dass eine große Menge von Schenkungen empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="a3182-107">Green means a high amount of donations have been received.</span></span>
*  <span data-ttu-id="a3182-108">Gelb bedeutet, dass eine mittlere Menge von Schenkungen empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="a3182-108">Yellow means a medium amount of donations have been received.</span></span>
*  <span data-ttu-id="a3182-109">Rot bedeutet, dass eine geringe Menge von Käufen empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="a3182-109">Red means a low amount of donations have been received.</span></span>

<span data-ttu-id="a3182-110">Sie können jedoch nicht erwarten, dass alle Ihre Benutzer diese Farben wie gewünscht sehen.</span><span class="sxs-lookup"><span data-stu-id="a3182-110">But you can't expect all of your users to experience these colors as intended.</span></span>  <span data-ttu-id="a3182-111">Indem Sie das Feature **"Sehschwächen emulieren"** des **Rendering-Tools** verwenden, können Sie feststellen, dass dieses Design nicht gut genug ist, indem Sie simulieren, wie Personen mit einer anderen Vision Ihr Design wahrnehmen würden.</span><span class="sxs-lookup"><span data-stu-id="a3182-111">By using the **Emulate vision deficiencies** feature of the **Rendering** tool, you can find out that this design is not good enough, by simulating how people with different vision would perceive your design.</span></span>


<span data-ttu-id="a3182-112">So überprüfen Sie, ob eine Webseite von Personen mit Farbenblindheit verwendet werden kann:</span><span class="sxs-lookup"><span data-stu-id="a3182-112">To check whether a webpage is usable by people with color blindness:</span></span>

1.  <span data-ttu-id="a3182-113">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a3182-113">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="a3182-114">Wählen Sie **Esc** aus, um die Schublade am unteren Rand von DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a3182-114">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="a3182-115">Wählen Sie das **+** Symbol oben in der Schublade aus, um die Liste der Tools anzuzeigen, und wählen Sie dann **Rendern**aus.</span><span class="sxs-lookup"><span data-stu-id="a3182-115">Select the **+** icon at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="a3182-116">Wählen Sie in der Dropdownliste **"Sehschwächen emulieren"** die Option **"Protanopia"** aus.</span><span class="sxs-lookup"><span data-stu-id="a3182-116">In the **Emulate vision deficiencies** dropdown list, select **Protanopia**.</span></span>  <span data-ttu-id="a3182-117">_Protanopia_ ist eine reduzierte Empfindlichkeit gegenüber rotem Licht, wodurch es schwierig ist, Grün, Rot und Gelb zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a3182-117">_Protanopia_ is reduced sensitivity to red light, making it hard to differentiate green, red, and yellow.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Anzeigen des Dokuments als jemand mit Protanopie würde es sehen" lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
        <span data-ttu-id="a3182-119">Anzeigen des Dokuments als jemand mit Protanopie würde es sehen</span><span class="sxs-lookup"><span data-stu-id="a3182-119">Showing the document as someone with protanopia would see it</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="a3182-120">Wählen Sie im **Renderingtool** unterhalb **von Emulieren von Sehschwächen** **"Keine Emulation"** aus, um die Simulation zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a3182-120">In the **Rendering** tool, below **Emulate vision deficiencies**, select **No emulation** to remove the simulation.</span></span>


## <a name="see-also"></a><span data-ttu-id="a3182-121">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="a3182-121">See also</span></span>

*  <span data-ttu-id="a3182-122">[Emulieren von Sehschwächen][DevToolsVisionDeficiencies] – Definiert die Elemente in der Dropdownliste **"Sehschwächen emulieren",** einschließlich Protanopia, Deuteranopia, Tritanopia und Aopsia.</span><span class="sxs-lookup"><span data-stu-id="a3182-122">[Emulate vision deficiencies][DevToolsVisionDeficiencies] - Defines the items in the **Emulate vision deficiencies** dropdown list, including Protanopia, Deuteranopia, Tritanopia, and Achromatopsia.</span></span>
*  [<span data-ttu-id="a3182-123">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="a3182-123">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a3182-124">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a3182-124">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Emulieren von Sehschwächen | Microsoft-Dokumente"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
