---
description: Simulieren Sie die reduzierte Bewegung mithilfe von Entwicklertools.
title: Simulieren von reduzierter Bewegung mithilfe von Entwicklertools (CSS bevorzugt reduzierte Bewegung)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 7244c2e80bbf9070214b6abd02583792c785953c
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597059"
---
# <a name="reduced-motion-simulation"></a><span data-ttu-id="0744a-104">Simulation reduzierter Bewegungen</span><span class="sxs-lookup"><span data-stu-id="0744a-104">Reduced motion simulation</span></span>  

<span data-ttu-id="0744a-105">Animationen in Webprodukten können ein Problem mit der Barrierefreiheit darstellen.</span><span class="sxs-lookup"><span data-stu-id="0744a-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="0744a-106">Betriebssysteme behandeln dieses Problem, indem sie eine Option zum Deaktivieren von Animationen einschließen, um Benutzerverwechslungen und potenzielle gesundheitsbezogene Probleme zu vermeiden, z. B. das Auslösen von Anfällen.</span><span class="sxs-lookup"><span data-stu-id="0744a-106">Operating systems deal with this problem by including an option to turn off animations to avoid user confusion and potential health-related problems, such as triggering seizures.</span></span>  

<span data-ttu-id="0744a-107">Auf einer Webseite können Sie die [CSS-Medienabfrage][MDNPrefersReducedMotion] mit eingeschränkter Bewegung verwenden, um zu ermitteln, ob der Benutzer Animationen anzeigen möchte.</span><span class="sxs-lookup"><span data-stu-id="0744a-107">On a webpage, you can use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS media query to detect whether the user prefers to display any animations.</span></span>  <span data-ttu-id="0744a-108">Schließen Sie dann den Animationscode in einen Test ein, um Animationen bedingt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0744a-108">Then wrap your animation code in a test, to conditionally run animations.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="0744a-109">Testen Sie dann Den Code wie folgt.</span><span class="sxs-lookup"><span data-stu-id="0744a-109">Then test your code, as follows.</span></span>

<span data-ttu-id="0744a-110">So simulieren Sie die Einstellung für reduzierte Bewegungen des Betriebssystems, ohne die Einstellung des Betriebssystems ändern zu müssen:</span><span class="sxs-lookup"><span data-stu-id="0744a-110">To simulate the operating system's reduced motion setting, without having to change your operating system setting:</span></span>

1.  <span data-ttu-id="0744a-111">Öffnen Sie das **Befehlsmenü**.</span><span class="sxs-lookup"><span data-stu-id="0744a-111">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="0744a-112">Wählen Sie `Control` + `Shift` + `P` unter Windows/Linux oder `Command` + `Shift` + `P` unter macOS aus.</span><span class="sxs-lookup"><span data-stu-id="0744a-112">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="0744a-114">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="0744a-114">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="0744a-115">Geben Sie `reduced` ein, um die Simulation ein- und auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="0744a-115">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="0744a-116">Wählen Sie die Option aus, und wählen Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="0744a-116">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Aktivieren oder Deaktivieren der Einstellung "Bevorzugte reduzierte Bewegung" im Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="0744a-118">Aktivieren oder Deaktivieren der **Einstellung "Bevorzugte reduzierte Bewegung"** im **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="0744a-118">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0744a-119">Aktualisieren Sie die Webseite, und überprüfen Sie, ob Ihre Animationen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0744a-119">Refresh the webpage and check whether your animations run.</span></span>


## <a name="see-also"></a><span data-ttu-id="0744a-120">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="0744a-120">See also</span></span>

* <span data-ttu-id="0744a-121">[Stellen Sie sicher, dass die Seite mit deaktivierter BENUTZERoberflächenanimation verwendet werden kann](test-reduced-ui-motion.md) . Eine exemplarische Vorgehensweise mithilfe einer Demoseite mit Erläuterungen.</span><span class="sxs-lookup"><span data-stu-id="0744a-121">[Verify that the page is usable with UI animation turned off](test-reduced-ui-motion.md) - A walkthrough using a demo page, with explanations.</span></span>

    
<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "bevorzugt reduzierte | Mdn"  
