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
# <a name="emulate-vision-deficiencies"></a>Emulieren von Sehstörungen  

Um die Anforderungen Ihrer Benutzer mit [Farbsehenmangel][ColorblindawarenessMain] \(Farbblindheit\) oder verschwommener Sehvermögen besser zu erfüllen, können Sie [mit Microsoft Edge DevTools][DevtoolsIndex] verschwommenes Sehvermögen und bestimmte Farbsehenschwächen simulieren.  Das Tool **zum Emulieren von Sehschwächen** simuliert die folgenden Kategorien.  

| Farbsehenmangel | Details |  
|:--- |:--- |  
| Verschwommene Vision | Der Benutzer hat Schwierigkeiten, sich auf details zu konzentrieren. |  
| Protanopie | Der Benutzer kann kein rotes Licht wahrnehmen. |  
| Deuteranopia | Der Benutzer kann kein grünes Licht wahrnehmen. |  
| Tritanopia | Der Benutzer kann kein blaues Licht wahrnehmen. |  
| Aopsia | Der Benutzer kann keine Farbe wahrnehmen, wodurch die gesamte Farbe auf einen Grauton reduziert wird. |  


## <a name="navigate-to-the-rendering-tool"></a>Navigieren Sie zum Renderingtool

Öffnen Sie die [Renderingtools,][DevtoolsRenderingToolsIndex]um einen Sehfehler zu simulieren, der für Ihr Webprodukt angewendet wird.  

1.  Um das Renderingtool zu öffnen, wählen Sie das `...` Menüelement in der Symbolleiste aus.  
1.  Auswählen **weiterer Tools**  
1.  **Rendern** auswählen  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Öffnen des Renderingtools" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Öffnen des **Renderingtools**
    :::image-end:::  
    
Das **Menü "Rendern"** wird in der Schublade angezeigt.  

1.  Scrollen Sie nach unten zum `Emulate vision deficiencies` Menüelement, und wählen Sie das Dropdownmenü aus, um die Optionen anzuzeigen.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Menü Sehschwächen emulieren im Renderingtool" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Menü **"Sehschwächen emulieren"** im **Renderingtool**
    :::image-end:::  
    
1.  Wählen Sie eine Option aus.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Die Menüoptionen Sehschwächen emulieren" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Menüoptionen zum **Emulieren von Sehschwächen**  
    :::image-end:::  
    
1.  In den Hauptfenstern wird die Simulation der ausgewählten Option angezeigt, die auf die aktuelle Seite angewendet wird.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Anzeigen mit der Simulation Verschwommenes Sehen" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Anzeigen mithilfe einer Simulation der **verschwommenen Sehkraft**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Anzeigen mithilfe einer Aopsia-Simulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Anzeigen mithilfe einer **Aopsia-Simulation** :::image-end:::  
       :::column-end:::
    :::row-end:::
    

## <a name="use-the-command-menu"></a>Verwenden des Befehlsmenüs  

Sie können auch **das Befehlsmenü** verwenden, um auf die verschiedenen Simulationen zuzugreifen.  

1.  Wählen Sie `Ctrl` + `Shift` + `P` \(Windows/Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü**zu öffnen.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Geben `emulate` Sie ein, wählen Sie, was Sie simulieren möchten, und wählen Sie `Enter` aus.  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Die verschiedenen Simulationsoptionen, die im Befehlsmenü verfügbar sind" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Die verschiedenen Simulationsoptionen, die im **Befehlsmenü** verfügbar sind  
    :::image-end:::  
    
> [!IMPORTANT]
> Die Tools zum **Emulieren von Sehschwächen** simulieren näherungsweise, wie eine Person mit jedem Mangel Ihr Produkt sehen kann.  Jede Person ist unterschiedlich, daher unterscheiden sich Sehschwächen je nach Schweregrad von Person zu Person.  Um die Anforderungen Ihrer Benutzer besser zu erfüllen, vermeiden Sie farbkombinationen, die möglicherweise ein Problem darstellen.  Die Tools zur **Emulieren von Sehschwächen** sind keine vollständige Bewertung der Barrierefreiheit Ihres Produkts.  Stattdessen sollten Ihnen die Tools zum **Emulieren von Sehschwächen** einen guten ersten Schritt bieten, um Probleme zu vermeiden.  


## <a name="see-also"></a>Weitere Informationen:

* [Überprüfen Sie, ob die Seite mit verschwommener Sicht verwendet werden kann](test-blurred-vision.md)


<!-- links -->  
[DevToolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analysieren der Laufzeitleistung | Microsoft-Dokumente"  

[ColorblindawarenessMain]: https://www.colourblindawareness.org "Die Organisation für blinde Sensibilisierung"  

[AmfcbMain]: https://www.amfcb.org "The American Foundation for the Color Blind (AFCB)"  
