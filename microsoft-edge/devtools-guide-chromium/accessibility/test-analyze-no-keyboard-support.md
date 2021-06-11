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
# <a name="analyze-keyboard-support-on-forms-using-the-devtools"></a>Analysieren der Tastaturunterstützung für Formulare mithilfe von DevTools

In diesem Artikel wird das Tool **Inspect** und die Registerkarte **"Ereignislistener"** verwendet, um die fehlende Tastaturunterstützung auf einer Demoseite zu analysieren, die Schaltflächen enthält, die das `div` Element verwenden.

Im Formular ** Einnahmen ** funktionieren die Schaltflächen Betrag und Zuordnen nicht mit einer Tastatur. ****  Für das Debuggen des Gabeformulars müssen Sie verstehen, warum die fehlende Fokusformatierung nicht als Problem mit automatischen Testtools wie dem **Tool "Probleme"** gekennzeichnet wird.  In diesem Beispiel werden die Schaltflächen mithilfe `div` von Elementen implementiert, die von diesen Tools nicht als Steuerelement in einem Formular erkannt werden.

So verwenden Sie das Tool Inspect und die Registerkarte "Ereignislistener", um die fehlende Tastaturunterstützung auf der Demoseite zu analysieren:

<!-- 1. Inspect tool: Accessibility section: keyboard-focusable row -->

1.  Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.
    
1.  Wählen Sie die Schaltfläche **Inspect** \( ![ Inspect icon ](../media/inspect-icon.msft.png) \) in der oberen linken Ecke von DevTools aus, sodass die Schaltfläche hervorgehoben ist (blau).

1.  Zeigen Sie auf die Schaltflächen **50,** **100**und **200** Schenkungen.  Das Tool Inspect wird auf der Webseite als Überlagerung angezeigt.  Die **tastaturfokussierbare** Zeile des Inspect-Overlays zeigt, dass keine der Schaltflächen für den Betrag der Gabe über die Tastatur zugänglich ist, wie durch einen grauen Kreis mit diagonaler Linie angegeben.  Die Schaltflächen haben keinen Namen und eine Rolle, `generic` da sie `div` Elemente sind, was bedeutet, dass die Schaltflächen für Hilfstechnologien nicht zugänglich sind.

    :::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="Die Überprüfung der Schaltflächen des Formulars zeigt, dass auf sie nicht über die Tastatur zugegriffen werden kann." lightbox="../media/a11y-testing-donation-button-info.msft.png":::
        Die Überprüfung der Schaltflächen des Formulars zeigt, dass auf sie nicht über die Tastatur zugegriffen werden kann.
    :::image-end:::
    
1.  Wenn das **Tool Inspect** aktiv ist, wählen Sie auf der Webseite das Textfeld **"Andere** Eingabe" über der Schaltfläche **"Überprüfen"** aus.  Das **** Elementtool wird mit der DOM-Struktur für die Webseite geöffnet.  Das Element `<input id="freedonation" class="smallinput">` ist ausgewählt.

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

    Die Verwendung des `label` Textfelds Other und der Elemente im `input` Textfeld Other ist gültig, d. h., die Beschriftung Other ist ordnungsgemäß mit dem Eingabetextfeld verknüpft. **** ****  Auf `input` das Textfeld kann auch über die Tastatur zugegriffen werden.  Der Rest des Markups des Formulars sind `div` Elemente, die einfach zu formatieren sind, aber keine semantische Bedeutung haben.

    <!-- 2. Elements tool: Event Listeners tab -->

    Die Funktionalität des Formulars wird mit JavaScript erstellt, und Sie können dies testen, indem Sie die Registerkarte **Ereignislistener** wie folgt überprüfen.

1.  Wenn das Element `<input id="freedonation" class="smallinput">` weiterhin in der DOM-Struktur ausgewählt ist, wählen Sie rechts neben der Registerkarte **"Formatvorlagen"** die Registerkarte **"Ereignislistener"** aus, und erweitern Sie dann den `click` Ereignislistener.

    :::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="Das Ereignislistener-Tool, das Ihnen zeigt, wo das JavaScript das Formular funktioniert" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
        Das Ereignislistener-Tool, das Ihnen zeigt, wo das JavaScript das Formular funktioniert
    :::image-end:::

1.  Wählen Sie den `buttons.js:18` Link aus.  Das **Tool "Quellen"** wird mit dem angewendeten JavaScript geöffnet.

    :::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="Der JavaScript-Code, der für die Funktionalität des Schenkungsformulars verantwortlich ist, dargestellt im Tool Quellen." lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
        Der JavaScript-Code, der für die Funktionalität des Schenkungsformulars verantwortlich ist, dargestellt im Tool "Quellen".
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

Die Verwendung eines `click` Ereignisses zum Lesen der Schaltflächen ist eine bewährte Methode, da ein `click` Ereignis sowohl beim Mauszeiger als auch bei der Tastaturinteraktion ausgelöst wird.  Da auf ein Element jedoch `div` nicht über die Tastatur zugegriffen werden kann und diese Schaltfläche ** Hilfe ** als Element ( ) implementiert ist, `div` wird diese `<div class="submitbutton">Donate</div>` JavaScript-Funktion nur ausgeführt, wenn Sie eine Maus oder eine andere Quelle eines `click` Ereignisses verwenden, z. B. eine spezielle Schaltfläche, die auf einigen Tastaturen verfügbar ist.

Dies ist ein klassisches Beispiel, in dem JavaScript hinzugefügt wurde, um Funktionen zu erstellen, die `button` Elemente nativ bereitstellen.  Das Simulieren der Funktionalität von Schaltflächen mit `div` Elementen hat zu einer unzugänglichen Erfahrung führen können.


## <a name="see-also"></a>Weitere Informationen:

*  [Übersicht über Barrierefreiheitstests mit DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
