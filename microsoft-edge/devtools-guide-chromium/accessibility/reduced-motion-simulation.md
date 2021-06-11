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
# <a name="reduced-motion-simulation"></a>Simulation reduzierter Bewegungen  

Animationen in Webprodukten können ein Problem mit der Barrierefreiheit darstellen.  Betriebssysteme behandeln dieses Problem, indem sie eine Option zum Deaktivieren von Animationen einschließen, um Benutzerverwechslungen und potenzielle gesundheitsbezogene Probleme zu vermeiden, z. B. das Auslösen von Anfällen.  

Auf einer Webseite können Sie die [CSS-Medienabfrage][MDNPrefersReducedMotion] mit eingeschränkter Bewegung verwenden, um zu ermitteln, ob der Benutzer Animationen anzeigen möchte.  Schließen Sie dann den Animationscode in einen Test ein, um Animationen bedingt auszuführen.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

Testen Sie dann Den Code wie folgt.

So simulieren Sie die Einstellung für reduzierte Bewegungen des Betriebssystems, ohne die Einstellung des Betriebssystems ändern zu müssen:

1.  Öffnen Sie das **Befehlsmenü**.  
    1.  Wählen Sie `Control` + `Shift` + `P` unter Windows/Linux oder `Command` + `Shift` + `P` unter macOS aus.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Das **Befehlsmenü**  
        :::image-end:::  
        
1.  Geben Sie `reduced` ein, um die Simulation ein- und auszuschalten.  Wählen Sie die Option aus, und wählen Sie `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Aktivieren oder Deaktivieren der Einstellung Bevorzugte reduzierte Bewegung im Befehlsmenü" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Aktivieren oder Deaktivieren der **Einstellung "Bevorzugte reduzierte Bewegung"** im **Befehlsmenü**  
    :::image-end:::  
    
1.  Aktualisieren Sie die Webseite, und überprüfen Sie, ob Ihre Animationen ausgeführt werden.


## <a name="see-also"></a>Weitere Informationen:

* [Stellen Sie sicher, dass die Seite mit deaktivierter BENUTZERoberflächenanimation verwendet werden kann](test-reduced-ui-motion.md) . Eine exemplarische Vorgehensweise mithilfe einer Demoseite mit Erläuterungen.

    
<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "bevorzugt reduzierte | Mdn"  
