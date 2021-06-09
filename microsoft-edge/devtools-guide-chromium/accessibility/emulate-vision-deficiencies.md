---
description: Emulieren Sie Sehschwächen in Microsoft Edge DevTools.
title: Emulieren von Sehschwächen in Microsoft Edge DevTools (Farbenblindheit)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 0a0ee09c2f739beb366b4c39d113b31fb719ec6a
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597120"
---
# <a name="emulate-vision-deficiencies"></a><span data-ttu-id="83bc9-104">Emulieren von Sehstörungen</span><span class="sxs-lookup"><span data-stu-id="83bc9-104">Emulate vision deficiencies</span></span>  

<span data-ttu-id="83bc9-105">Um die Anforderungen Ihrer Benutzer mit [Farbsehenmangel][ColorblindawarenessMain] \(Farbblindheit\) oder verschwommener Sehvermögen besser zu erfüllen, können Sie [mit Microsoft Edge DevTools][DevtoolsIndex] verschwommenes Sehvermögen und bestimmte Farbsehenschwächen simulieren.</span><span class="sxs-lookup"><span data-stu-id="83bc9-105">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\) or blurred vision, [Microsoft Edge DevTools][DevtoolsIndex] allow you to simulate blurred vision and specific color vision deficiencies.</span></span>  <span data-ttu-id="83bc9-106">Das Tool **zum Emulieren von Sehschwächen** simuliert die folgenden Kategorien.</span><span class="sxs-lookup"><span data-stu-id="83bc9-106">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="83bc9-107">Farbsehenmangel</span><span class="sxs-lookup"><span data-stu-id="83bc9-107">Color vision deficiency</span></span> | <span data-ttu-id="83bc9-108">Details</span><span class="sxs-lookup"><span data-stu-id="83bc9-108">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="83bc9-109">Verschwommene Vision</span><span class="sxs-lookup"><span data-stu-id="83bc9-109">Blurred vision</span></span> | <span data-ttu-id="83bc9-110">Der Benutzer hat Schwierigkeiten, sich auf details zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="83bc9-110">The user has difficulty focusing on fine details.</span></span> |  
| <span data-ttu-id="83bc9-111">Protanopie</span><span class="sxs-lookup"><span data-stu-id="83bc9-111">Protanopia</span></span> | <span data-ttu-id="83bc9-112">Der Benutzer kann kein rotes Licht wahrnehmen.</span><span class="sxs-lookup"><span data-stu-id="83bc9-112">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="83bc9-113">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="83bc9-113">Deuteranopia</span></span> | <span data-ttu-id="83bc9-114">Der Benutzer kann kein grünes Licht wahrnehmen.</span><span class="sxs-lookup"><span data-stu-id="83bc9-114">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="83bc9-115">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="83bc9-115">Tritanopia</span></span> | <span data-ttu-id="83bc9-116">Der Benutzer kann kein blaues Licht wahrnehmen.</span><span class="sxs-lookup"><span data-stu-id="83bc9-116">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="83bc9-117">Aopsia</span><span class="sxs-lookup"><span data-stu-id="83bc9-117">Achromatopsia</span></span> | <span data-ttu-id="83bc9-118">Der Benutzer kann keine Farbe wahrnehmen, wodurch die gesamte Farbe auf einen Grauton reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="83bc9-118">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  


## <a name="navigate-to-the-rendering-tool"></a><span data-ttu-id="83bc9-119">Navigieren Sie zum Renderingtool</span><span class="sxs-lookup"><span data-stu-id="83bc9-119">Navigate to the Rendering tool</span></span>

<span data-ttu-id="83bc9-120">Öffnen Sie die [Renderingtools,][DevtoolsRenderingToolsIndex]um einen Sehfehler zu simulieren, der für Ihr Webprodukt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="83bc9-120">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][DevtoolsRenderingToolsIndex].</span></span>  

1.  <span data-ttu-id="83bc9-121">Um das Renderingtool zu öffnen, wählen Sie das `...` Menüelement in der Symbolleiste aus.</span><span class="sxs-lookup"><span data-stu-id="83bc9-121">To open the Rendering tool, choose the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="83bc9-122">Auswählen **weiterer Tools**</span><span class="sxs-lookup"><span data-stu-id="83bc9-122">Choose **More tools**</span></span>  
1.  <span data-ttu-id="83bc9-123">**Rendern** auswählen</span><span class="sxs-lookup"><span data-stu-id="83bc9-123">Choose **Rendering**</span></span>  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Öffnen des Renderingtools" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="83bc9-125">Öffnen des **Renderingtools**</span><span class="sxs-lookup"><span data-stu-id="83bc9-125">Opening the **Rendering** tool</span></span>
    :::image-end:::  
    
<span data-ttu-id="83bc9-126">Das **Menü "Rendern"** wird in der Schublade angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83bc9-126">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="83bc9-127">Scrollen Sie nach unten zum `Emulate vision deficiencies` Menüelement, und wählen Sie das Dropdownmenü aus, um die Optionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="83bc9-127">Scroll down to the `Emulate vision deficiencies` menu item and choose the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Menü "Sehschwächen emulieren" im Renderingtool" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="83bc9-129">Menü **"Sehschwächen emulieren"** im **Renderingtool**</span><span class="sxs-lookup"><span data-stu-id="83bc9-129">The **Emulate vision deficiencies** menu on the **Rendering** tool</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="83bc9-130">Wählen Sie eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="83bc9-130">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Die Menüoptionen "Sehschwächen emulieren"" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="83bc9-132">Menüoptionen zum **Emulieren von Sehschwächen**</span><span class="sxs-lookup"><span data-stu-id="83bc9-132">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="83bc9-133">In den Hauptfenstern wird die Simulation der ausgewählten Option angezeigt, die auf die aktuelle Seite angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="83bc9-133">The main windows displays the simulation of your chosen option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Anzeigen mit der Simulation "Verschwommenes Sehen"" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="83bc9-135">Anzeigen mithilfe einer Simulation der **verschwommenen Sehkraft**</span><span class="sxs-lookup"><span data-stu-id="83bc9-135">Display using **Blurred vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Anzeigen mithilfe einer Aopsia-Simulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="83bc9-137">Anzeigen mithilfe einer **Aopsia-Simulation**</span><span class="sxs-lookup"><span data-stu-id="83bc9-137">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    

## <a name="use-the-command-menu"></a><span data-ttu-id="83bc9-138">Verwenden des Befehlsmenüs</span><span class="sxs-lookup"><span data-stu-id="83bc9-138">Use the Command Menu</span></span>  

<span data-ttu-id="83bc9-139">Sie können auch **das Befehlsmenü** verwenden, um auf die verschiedenen Simulationen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="83bc9-139">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="83bc9-140">Wählen Sie `Ctrl` + `Shift` + `P` \(Windows/Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="83bc9-140">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="83bc9-142">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="83bc9-142">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="83bc9-143">Geben `emulate` Sie ein, wählen Sie, was Sie simulieren möchten, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="83bc9-143">Type `emulate`, choose what you want to simulate and choose `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Die verschiedenen Simulationsoptionen, die im Befehlsmenü verfügbar sind" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="83bc9-145">Die verschiedenen Simulationsoptionen, die im **Befehlsmenü** verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="83bc9-145">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="83bc9-146">Die Tools zum **Emulieren von Sehschwächen** simulieren näherungsweise, wie eine Person mit jedem Mangel Ihr Produkt sehen kann.</span><span class="sxs-lookup"><span data-stu-id="83bc9-146">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="83bc9-147">Jede Person ist unterschiedlich, daher unterscheiden sich Sehschwächen je nach Schweregrad von Person zu Person.</span><span class="sxs-lookup"><span data-stu-id="83bc9-147">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="83bc9-148">Um die Anforderungen Ihrer Benutzer besser zu erfüllen, vermeiden Sie farbkombinationen, die möglicherweise ein Problem darstellen.</span><span class="sxs-lookup"><span data-stu-id="83bc9-148">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="83bc9-149">Die Tools zur **Emulieren von Sehschwächen** sind keine vollständige Bewertung der Barrierefreiheit Ihres Produkts.</span><span class="sxs-lookup"><span data-stu-id="83bc9-149">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="83bc9-150">Stattdessen sollten Ihnen die Tools zum **Emulieren von Sehschwächen** einen guten ersten Schritt bieten, um Probleme zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="83bc9-150">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  


## <a name="see-also"></a><span data-ttu-id="83bc9-151">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="83bc9-151">See also</span></span>

* [<span data-ttu-id="83bc9-152">Überprüfen Sie, ob die Seite mit verschwommener Sicht verwendet werden kann</span><span class="sxs-lookup"><span data-stu-id="83bc9-152">Verify that the page is usable with blurred vision</span></span>](test-blurred-vision.md)


<!-- links -->  
[DevToolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analysieren der Laufzeitleistung | Microsoft-Dokumente"  

[ColorblindawarenessMain]: https://www.colourblindawareness.org "Die Organisation für blinde Sensibilisierung"  

[AmfcbMain]: https://www.amfcb.org "The American Foundation for the Color Blind (AFCB)"  
