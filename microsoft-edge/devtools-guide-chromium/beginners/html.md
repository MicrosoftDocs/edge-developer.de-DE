---
description: Erste Schritte mit HTML und dem Dokumentobjektmodell
title: 'Entwicklungstools für Anfänger: Erste Schritte mit HTML und dem Dokumentobjektmodell'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, DevTools, DevTools für Anfänger, DevTools-HTML für Anfänger, DevTools DOM für Anfänger, DevTools HTML-Lernprogramm, DevTools DOM-Lernprogramm, DevTools-Lernprogramm zum Dokumentobjektmodell
ms.openlocfilehash: a049ec500e22f89db3ab1e966b55d89c2ad682fe
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643512"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a>Entwicklungstools für Anfänger: Erste Schritte mit HTML und dem Dokumentobjektmodell  

Dies ist das erste einer Reihe von Lernprogrammen, die Ihnen die Grundlagen der Webentwicklung vermitteln. Erfahren Sie mehr über eine Reihe von Webentwicklertools namens Microsoft Edge DevTools, die Ihre Produktivität steigern können.  

In diesem Lernprogramm werden HTML und das [Dokumentobjektmodell](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\) beschrieben. HTML ist eine der Kerntechnologien bei der Webentwicklung. Es ist die Sprache, über die Struktur und Inhalte von Webseiten gesteuert werden. Das DOM steht ebenfalls mit Struktur und Inhalt von Webseiten in Zusammenhang. Dazu später mehr.

## <a name="goals"></a>Ziele  

Sie werden Grundlagen der Webentwicklung erlernen durch das Erstellen einer Website.  Wenn Sie alle Lernprogramme der **DevTools for Beginners-Reihe** abgeschlossen haben, sieht Ihre fertige Website möglicherweise wie in der folgenden Abbildung aus.  

:::image type="complex" source="media/beginners-html-finished.msft.png" alt-text="Die fertige Website" lightbox="media/beginners-html-finished.msft.png":::
   Die fertige Website  
:::image-end:::  

Am Ende dieses Lernprogramms sollten Sie die nachstehend aufgeführten Konzepte verstehen.  

*   Wie über HTML und das DOM die Inhalte erstellt werden, die auf Webseiten angezeigt werden  
*   Wie Microsoft Edge DevTools Ihnen beim Experimentieren mit HTML- und DOM-Änderungen helfen kann  
*   Den Unterschied zwischen HTML und DOM  

Sie werden dann außerdem über eine funktionsfähige Website verfügen. Diese können Sie z. B. für Ihren Lebenslauf oder zum Hosten Ihres Blogs verwenden.  

## <a name="prerequisites"></a>Voraussetzungen  

Bevor Sie dieses Lernprogramm angehen, müssen die folgenden Voraussetzungen erfüllt sein:  

*   Wenn Sie mit HTML noch nicht vertraut sind, lesen Sie [Erste Schritte mit HTML][MDNGettingStartedHtml].  
*   Laden Sie den [Microsoft Edge][MicrosoftEdgeInsider]-Webbrowser herunter.  In diesem Lernprogramm werden verschiedene, in Microsoft Edge integrierte Webentwicklungstools verwendet, die als Microsoft Edge DevTools bezeichnet werden.  

## <a name="set-up-your-code"></a>Einrichten des Codes  

Sie werden eine Website im Glitch-Online-Code-Editor erstellen.  

1.  Öffnen Sie den [Quellcode.][GlitchAlluringShockIndex] Diese Registerkarte wird in diesem Lernprogramm als **Editor-Registerkarte** bezeichnet.  
    
    :::image type="complex" source="media/beginners-html-setup1.msft.png" alt-text="Die Editor-Registerkarte" lightbox="media/beginners-html-setup1.msft.png":::
       Die Editor-Registerkarte  
    :::image-end:::  
    
1.  Wählen Sie **alluring-shock** aus. Das Menü **Project Options** wird geöffnet.  
    
    :::image type="complex" source="media/beginners-html-setup2.msft.png" alt-text="Menü "Project Options"" lightbox="media/beginners-html-setup2.msft.png":::
       Menü "Project Options"  
    :::image-end:::  
    
1.  Wählen Sie **Remix Project** aus. Glitch erstellt eine Kopie des Projekts, die Sie bearbeiten können, und generiert einen neuen zufälligen Namen für das Projekt. Der Inhalt ist derselbe wie zuvor.  
    
    :::image type="complex" source="media/beginners-html-setup3.msft.png" alt-text="Das remixte Projekt" lightbox="media/beginners-html-setup3.msft.png":::
       Das remixte Projekt  
    :::image-end:::  
    
1.  Wenn Sie beabsichtigen, das nächste Lernprogramm in dieser Reihe zu absolvieren, wählen Sie "Bei Glitch **anmelden"** aus, und melden Sie sich mit Ihrem Facebook-, GitHub- oder Google-Konto an. Oder senden Sie sich selbst einen "magischen" Link. Wenn Sie sich nicht bei einem Konto anmelden, können Sie das Projekt nach dem Schließen der Editor-Registerkarte nicht bearbeiten.

1.  Wählen Sie **Show** \> **In a New Window** (In neuem Fenster anzeigen) aus.  Eine neue Registerkarte mit der Liveseite wird geöffnet. Diese Registerkarte wird in diesem Lernprogramm als **Live-Registerkarte** bezeichnet.  
    
    :::image type="complex" source="media/beginners-html-setup4.msft.png" alt-text="Die Live-Registerkarte" lightbox="media/beginners-html-setup4.msft.png":::
       Die Live-Registerkarte  
    :::image-end:::  
    
## <a name="add-content"></a>Hinzufügen von Inhalten  

Für Ihre Website werden weitere Informationen benötigt. Führen Sie die folgenden Schritte aus, um einige Inhalte hinzuzufügen.  

1. Ersetzen Sie auf der **Editor-Registerkarte** `<!-- You're "About Me" will go here.  -->` durch `<h1>About Me</h1>`.  
    
    ```html
        ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                </main>
        ...
    ```  
    
    :::image type="complex" source="media/beginners-html-add1.msft.png" alt-text="Der neue Code wird auf der Editor-Registerkarte hervorgehoben." lightbox="media/beginners-html-add1.msft.png":::
        Der neue Code wird auf der Editor-Registerkarte hervorgehoben.  
    :::image-end:::  
    
1. Sehen Sie sich Ihre Änderungen auf der **Live-Registerkarte** an. Auf der Seite wird der Text `About Me` angezeigt. Er ist größer als der umgebende Text, da das `<h1>`-Element für eine "Überschrift 1" steht.  Ihr Webbrowser stellt deshalb Überschriften automatisch in größeren Schriftgraden dar.  
    
    :::image type="complex" source="media/beginners-html-add2.msft.png" alt-text="Die neue Überschrift wird auf der Live-Registerkarte angezeigt." lightbox="media/beginners-html-add2.msft.png":::
       Die neue Überschrift wird auf der Live-Registerkarte angezeigt.  
    :::image-end:::  
    
1. Kehren Sie zur **Editor-Registerkarte** zurück, und fügen Sie `<p>I am learning web development. Recent accomplishments:</p>` in die Zeile unter `<h1>About Me</h1>` ein.  
    
    ```html
    ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                    <p>I am learning web development. Recent accomplishments:</p>
                </main>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add3.msft.png" alt-text="Der aktualisierte Code wird auf der Editor-Registerkarte hervorgehoben." lightbox="media/beginners-html-add3.msft.png":::
        Der aktualisierte Code wird auf der Editor-Registerkarte hervorgehoben.  
    :::image-end:::  
    
1. Sehen Sie sich Ihre Änderung auf der **Live-Registerkarte** an.

1. Fügen Sie auf der **Editor-Registerkarte** mithilfe des folgenden Codes eine Liste erreichter Ziele hinzu.
    
    ```html
    ...
    <p>I am learning web development.  Recent accomplishments:</p>
        <ul>
            <li>Learned how to set up my code in Glitch.</li>
            <li>Added content to my HTML.</li>
            <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
            <li>TODO: Learn the difference between HTML and the DOM.</li>
        </ul>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add4.msft.png" alt-text="Der aktualisierte Code wird ebenfalls auf der Editor-Registerkarte hervorgehoben." lightbox="media/beginners-html-add4.msft.png":::
        Der aktualisierte Code wird ebenfalls auf der Editor-Registerkarte hervorgehoben.  
    :::image-end:::  

1. Überprüfen Sie auf der **Live-Registerkarte**, ob der neue Inhalt korrekt angezeigt wird.  
    
    :::image type="complex" source="media/beginners-html-add5.msft.png" alt-text="Die neue Liste wird auf der Live-Registerkarte angezeigt." lightbox="media/beginners-html-add5.msft.png":::
       Die neue Liste wird auf der Live-Registerkarte angezeigt.  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a>Experimentieren mit Änderungen an Inhalten in Microsoft Edge DevTools  

Wenn Sie eine Seite mit viel HTML-Code entwickeln, wird das Hin- und Herwechseln zwischen Editor- und Live-Registerkarte zur Überprüfung der Änderungen mühsam. Mit Microsoft Edge DevTools können Sie mit Inhaltsänderungen experimentieren, ohne die **Live-Registerkarte** zu verlassen.  

### <a name="learn-the-difference-between-html-and-the-dom"></a>Der Unterschied zwischen HTML und DOM  

Bevor Sie Inhalte über Microsoft Edge DevTools bearbeiten, sehen wir uns an, worin sich HTML und das DOM unterscheiden. Fahren Sie mit den folgenden Schritten fort, um dies anhand eines Beispiels zu verstehen.

1. Navigieren Sie zur **Live-Registerkarte**. Am unteren Rand der Seite wird der Text `A new element!?!` angezeigt.  

    <!--
        :::image type="complex" source="media/beginners-html-dom1.msft.png" alt-text="At the bottom of the page the text A new element!?! displays" lightbox="media/beginners-html-dom1.msft.png":::
        At the bottom of the page the text `A new element!?!` is displays  
        :::image-end:::
    -->
    
1. Öffnen Sie die **Editor-Registerkarte**, und suchen Sie nach dem Text in `index.html`. Der Text wird in dieser Ansicht nicht angezeigt.  

    <!--
        :::image type="complex" source="media/beginners-html-dom2.msft.png" alt-text="The mystery text A new element!?! is not found in index.html" lightbox="media/beginners-html-dom2.msft.png":::
        The mystery text `A new element!?!` is not found in `index.html`  
        :::image-end:::
    -->

1. Öffnen Sie die **Live-Registerkarte**, zeigen Sie auf `A new element!?!`, öffnen Sie das Kontextmenü (Rechtsklick), und wählen Sie dann **Inspect**aus.  
    
    :::image type="complex" source="media/beginners-html-dom3.msft.png" alt-text="Überprüfen von Text" lightbox="media/beginners-html-dom3.msft.png":::
       Überprüfen von Text  
    :::image-end:::  
    
    DevTools wird zusammen mit Ihrer Seite geöffnet. `<div>A new element!?!</div>` ist hervorgehoben. Obwohl diese Struktur in DevTools wie HTML aussieht, handelt es sich um die **DOM-Struktur**.  
    
    :::image type="complex" source="media/beginners-html-dom4.msft.png" alt-text="DevTools ist neben der Seite geöffnet" lightbox="media/beginners-html-dom4.msft.png":::
       DevTools ist neben der Seite geöffnet  
    :::image-end:::  
    
Wenn Ihre Seite geladen wird, erstellt der Browser anhand des HTML-Codes deren anfänglichen Inhalt. Das DOM stellt den aktuellen Inhalt der Seite dar, der sich im Laufe der Zeit ändern kann. 

Der `<div>A new element!?!</div>`-Inhalt wird Ihrer Seite aufgrund des `<script src="new.js"></script>`-Tags am unteren Ende Ihres HTML-Codes hinzugefügt. Dieses Tag bewirkt, dass JavaScript-Code ausgeführt wird. Weitere Informationen zu JavaScript finden Sie in einem [späteren Lernprogramm](../javascript/index.md).

Stellen Sie sich darunter vorerst eine Skriptsprache vor, über die der Inhalt Ihrer Seite geändert werden kann. In diesem Fall fügt JavaScript-Code Ihrer Seite `<div>A new element!?!</div>` hinzu. Aus diesem Grund wird dieser Text auf der **Live-Registerkarte**, aber nicht im HTML-Code angezeigt.  

### <a name="edit-the-dom"></a>Bearbeiten des DOM  

Wenn Sie schnell mit Inhaltsänderungen experimentieren möchten, ohne die Live-Registerkarte verlassen zu müssen, probieren Sie DevTools aus.  

1.  Zeigen Sie in DevTools mit dem Mauszeiger auf `Your site!`, öffnen Sie das Kontextmenü (rechtsklick), und wählen Sie **Edit as HTML** aus.  
    
1.  Ersetzen Sie `<p>Your site!</p>` durch den folgenden Code.  

```html
    ...
    <header>
        <p><b>Welcome to my site!</b></p>
        <button>Download my resume</button>
    </header>
    ...
```  

:::image type="complex" source="media/beginners-html-edit2.msft.png" alt-text="Aktualisieren des Knotens als HTML" lightbox="media/beginners-html-edit2.msft.png":::
    Aktualisieren des Knotens als HTML  
::image-end:::  

1.  Klicken Sie auf `Control` + `Enter` \(Windows, Linux\) oder `Command` + `Enter` \(macOS\), um Ihre Änderungen zu speichern, oder klicken Sie außerhalb des Felds. Ihre Änderungen werden automatisch in der Liveansicht Ihrer Seite angezeigt. Der Text `Your site!` wurde durch den neuen Inhalt ersetzt.  
    
    :::image type="complex" source="media/beginners-html-edit3.msft.png" alt-text="Der neue Inhalt wird sofort auf der Seite angezeigt." lightbox="media/beginners-html-edit3.msft.png":::
       Der neue Inhalt wird sofort auf der Seite angezeigt.  
    :::image-end:::  
    
Dieser Workflow eignet sich nur für das Experimentieren mit Inhaltsänderungen. Wenn Sie die Seite aktualisieren oder die Registerkarte schließen, gehen Ihre Änderungen verloren. Wenn Sie die Änderungen speichern möchten, kopieren Sie den Code manuell in Ihre HTML-Datei. In den nächsten Abschnitten werden einige weitere Möglichkeiten zum Ändern von Inhalten über die DOM-Struktur erläutert.  

## <a name="reorder-nodes"></a>Knoten neu anordnen

Sie können auch die Reihenfolge von DOM-Knoten ändern. Beispielsweise befindet sich das Navigationsmenü auf Ihrer Webseite am unteren Rand. Führen Sie die folgenden Schritte aus, um sie nach oben zu verschieben.  

1.  Suchen Sie den `<nav>`-Knoten in der **DOM-Struktur** von DevTools.  
    
    :::image type="complex" source="media/beginners-html-reorder1.msft.png" alt-text="Der Navigationsknoten ist in DevTools hervorgehoben." lightbox="media/beginners-html-reorder1.msft.png":::
       Der Navigationsknoten ist in DevTools hervorgehoben.  
    :::image-end:::  
    
1.  Ziehen Sie den `<nav>`-Knoten nach oben, sodass er das erste untergeordnete Element nach dem `<body>`-Knoten ist.  
    
    :::image type="complex" source="media/beginners-html-reorder3.msft.png" alt-text="Der Navigationsknoten befindet sich oben auf der Seite." lightbox="media/beginners-html-reorder3.msft.png":::
        Der Navigationsknoten befindet sich oben auf der Seite.  
    :::image-end:::  
    
### <a name="delete-a-node"></a>Löschen eines Knotens

Sie können Knoten aus der DOM-Struktur auch entfernen. Führen Sie dazu die folgenden Schritte aus:

1.  Wählen Sie in der **DOM-Struktur** `<div>A new element!?!</div>` aus. Der Knoten wird in DevTools hervorgehoben. 
    
1.  Drücken Sie die `Delete`-Taste auf der Tastatur.  Der `<div>A new element!?!</div>`-Knoten wird aus der DOM-Struktur entfernt.  
    
    :::image type="complex" source="media/beginners-html-delete2.msft.png" alt-text="Der Knoten wurde gelöscht." lightbox="media/beginners-html-delete2.msft.png":::
       Der Knoten wurde gelöscht.  
    :::image-end:::  
    
## <a name="copy-your-changes"></a>Kopieren Ihrer Änderungen  

Sie sind jetzt fast fertig. Sie haben einige Änderungen an der Seite in DevTools vorgenommen, diese werden jedoch nicht im Quellcode gespeichert.  

1.  Aktualisieren Sie die **Live-Registerkarte**. Die Änderungen, die Sie in der DOM-Struktur vorgenommen haben, werden nicht mehr angezeigt. Insbesondere kehrt der Text `Your site!` an den oberen Rand und der Text `A new element!?!` an den unteren zurück.  
    
    :::image type="complex" source="media/beginners-html-copy1.msft.png" alt-text="Die von Ihnen vorgenommenen Änderungen sind weg" lightbox="media/beginners-html-copy1.msft.png":::
       Die von Ihnen vorgenommenen Änderungen sind weg  
    :::image-end:::  
    
1.  Kopieren Sie den folgenden Code.  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
    
1.  Wechseln Sie zurück zur **Editor-Registerkarte**, und ersetzen Sie den Inhalt Ihrer `index.html`-Datei durch den kopierten Code.  
    
    :::image type="complex" source="media/beginners-html-copy2.msft.png" alt-text="So sollte Ihre index.html-Datei aussehen" lightbox="media/beginners-html-copy2.msft.png":::
       So sollte Ihre `index.html`-Datei aussehen  
    :::image-end:::  
    
## <a name="next-steps"></a>Nächste Schritte  

*   Absolvieren Sie das nächste Lernprogramm dieser Reihe ([Erste Schritte mit CSS][DevToolsBeginnersCss]) um zu lernen, wie Sie Ihre Seite designen und mit Designänderungen in Microsoft Edge DevTools experimentieren können.  
*   Näheres zum DOM erfahren Sie unter [Einführung in das DOM][MDNIntroductionDom].  
*   Sehen Sie sich einen Kurs wie [Einführung in die Webentwicklung][CourseraIntroductionToWebDevelopment] an, um weitere praktische Webentwicklungstipps zu erhalten.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools für Anfänger: Erste Schritte mit CSS | Microsoft-Dokumentation"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Einführung in die Webentwicklung | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html – alluring-shock | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Erste Schritte mit HTML| MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in das DOM | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite wurde [hier](https://developers.google.com/web/tools/chrome-devtools/beginners/html) gefunden und von [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
