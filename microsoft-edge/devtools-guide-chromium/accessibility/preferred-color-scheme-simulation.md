---
description: Erzwingen Microsoft Edge DevTools in den Vorschaumodus für Farbschemas.
title: Erzwingen Microsoft Edge DevTools in den Vorschaumodus für Farbschemas (CSS bevorzugt Farbschema)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: dc2911ce7a7fcbeef7763099541822b5cd6cf053
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597068"
---
# <a name="dark-or-light-color-scheme-simulation"></a><span data-ttu-id="dc421-104">Simulation von dunklen oder hellen Farbschemas</span><span class="sxs-lookup"><span data-stu-id="dc421-104">Dark or light color scheme simulation</span></span>  

<span data-ttu-id="dc421-105">Viele Betriebssysteme haben eine Möglichkeit, jede Anwendung in dunkleren oder helleren Farben anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dc421-105">Many operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="dc421-106">Ein Webprodukt, das ein helles Design in einem Betriebssystem im dunklen Modus aufweist, ist riebend und kann für einige Benutzer ein Problem mit der Barrierefreiheit sein.</span><span class="sxs-lookup"><span data-stu-id="dc421-106">Having a web product that has a light theme in a dark-mode operating system is grating and can be an accessibility issue for some users.</span></span>  

<span data-ttu-id="dc421-107">Für eine Webseite können Sie die [CSS-Medienabfrage "prefers-color-scheme"][MDNPrefersColorScheme] verwenden, um zu ermitteln, ob der Benutzer ihr Produkt lieber in einem dunkleren oder helleren Farbschema anzeigen möchte.</span><span class="sxs-lookup"><span data-stu-id="dc421-107">For a webpage, you can use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect whether the user prefers to display your product in a darker or lighter color scheme.</span></span>  <span data-ttu-id="dc421-108">Verwenden Sie dann zum Testen des Ergebnisses [Microsoft Edge DevTools,][DevtoolsIndex] um einen Wechsel vom dunklen in den hellen Modus zu simulieren, ohne die Einstellung für das gesamte Betriebssystem ändern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="dc421-108">Then to test the result, use [Microsoft Edge DevTools][DevtoolsIndex] to simulate a change from dark to light mode, without having to change the setting for your entire operating system.</span></span>  

**<span data-ttu-id="dc421-109">So emulieren Sie dunkles oder helles Design:</span><span class="sxs-lookup"><span data-stu-id="dc421-109">To emulate dark or light theme:</span></span>**

1.  <span data-ttu-id="dc421-110">Öffnen Sie das **Befehlsmenü**.</span><span class="sxs-lookup"><span data-stu-id="dc421-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="dc421-111">Wählen Sie `Ctrl` + `Shift` + `P` \(Windows/Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="dc421-111">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="dc421-113">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="dc421-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="dc421-114">Geben `emulate color` Sie ein, wählen Sie entweder **Emulate CSS prefers-color-scheme: dark** oder **Emulate CSS prefers-color-scheme: light** and then select `Enter` .</span><span class="sxs-lookup"><span data-stu-id="dc421-114">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Farbschemaoption im Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="dc421-116">Farbschemaoption im **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="dc421-116">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="dc421-117">Einfach eingeben `dark` oder zeigt nicht das richtige Tool `light` an, da es auch eine Möglichkeit gibt, [ein Design für DevTools auszuwählen.][DevtoolsCustomizeDarkTheme]</span><span class="sxs-lookup"><span data-stu-id="dc421-117">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsCustomizeDarkTheme].</span></span>  <span data-ttu-id="dc421-118">Wenn Sie sich fragen, was Sie auswählen sollten, stellen Sie sicher, dass Sie ein **Renderingmenüelement** und kein **Darstellungsmenüelement** auswählen.</span><span class="sxs-lookup"><span data-stu-id="dc421-118">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="dc421-119">Nachdem Sie ein Farbschema ausgewählt haben, aktualisieren Sie das aktuelle Dokument, um den simulierten Modus anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dc421-119">After you choose a color scheme, refresh the current document to display the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Simulierter Lichtmodus innerhalb Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="dc421-121">Simulierter Lichtmodus innerhalb Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="dc421-121">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="dc421-122">Zeigen Sie Ihre CSS wie jede andere Webseite an, und ändern Sie sie.</span><span class="sxs-lookup"><span data-stu-id="dc421-122">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="dc421-123">Weitere Informationen finden Sie unter ["Erste Schritte mit dem Anzeigen und Ändern von CSS".][DevtoolsCssIndex]</span><span class="sxs-lookup"><span data-stu-id="dc421-123">For more information, navigate to [Get started with viewing and changing CSS][DevtoolsCssIndex].</span></span>  


## <a name="see-also"></a><span data-ttu-id="dc421-124">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="dc421-124">See also</span></span>

* [<span data-ttu-id="dc421-125">Überprüfen Sie auf Kontrastprobleme mit dunklem Design und hellem Design</span><span class="sxs-lookup"><span data-stu-id="dc421-125">Check for contrast issues with dark theme and light theme</span></span>](test-dark-mode.md)


<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Aktivieren des dunklen Designs in Microsoft Edge DevTools-| Microsoft-Dokumente"
[DevtoolsCssIndex]: ../css/index.md "Erste Schritte mit dem Anzeigen und Ändern von CSS-| Microsoft-Dokumente"  
<!-- external links -->
[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | Mdn"  
