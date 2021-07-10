---
description: Erste Schritte mit HTML und dem DOM
title: 'DevTools für Anfänger: Erste Schritte mit HTML und dem DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, Devtools, Devtools für Anfänger, Devtools-HTML für Anfänger, Devtools-DOM für Anfänger, Devtools-HTML-Lernprogramm, Devtools-DOM-Lernprogramm, DevTools-Lernprogramm zum Dokumentobjektmodell
ms.openlocfilehash: a049ec500e22f89db3ab1e966b55d89c2ad682fe
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a>DevTools für Anfänger: Erste Schritte mit HTML und dem DOM  

Dies ist der erste einer Reihe von Lernprogrammen, die Ihnen die Grundlagen der Webentwicklung vermitteln. Erfahren Sie mehr über eine Reihe von Webentwicklertools namens Microsoft Edge DevTools, die Ihre Produktivität steigern können.  

In diesem Lernprogramm werden HTML und das [Dokumentobjektmodell](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\) beschrieben. HTML ist eine der Kerntechnologien der Webentwicklung. Es ist die Sprache, die die Struktur und den Inhalt von Webseiten steuert. Das DOM bezieht sich auch auf die Struktur und den Inhalt von Webseiten, über die wir später mehr erfahren.

## <a name="goals"></a>Ziele  

Sie werden die Webentwicklung erlernen, indem Sie eine Website erstellen.  Wenn Sie alle Lernprogramme in der **DevTools for Beginners-Reihe** abgeschlossen haben, sieht Ihre fertige Website möglicherweise wie in der folgenden Abbildung aus.  

:::image type="complex" source="media/beginners-html-finished.msft.png" alt-text="Die fertige Website" lightbox="media/beginners-html-finished.msft.png":::
   Die fertige Website  
:::image-end:::  

Am Ende dieses Lernprogramms sollten Sie die folgenden Konzepte verstehen.  

*   Wie HTML und das DOM die Inhalte erstellen, die auf Webseiten angezeigt werden.  
*   Wie Microsoft Edge DevTools Ihnen beim Experimentieren mit HTML- und DOM-Änderungen helfen kann.  
*   Der Unterschied zwischen HTML und DOM.  

Sie haben auch eine funktionsfähige Website. Sie können die Website verwenden, um Ihren Lebenslauf oder Blog zu hosten.  

## <a name="prerequisites"></a>Voraussetzungen  

Bevor Sie dieses Lernprogramm testen, erfüllen Sie die folgenden Voraussetzungen:  

*   Wenn Sie mit HTML nicht vertraut sind, lesen Sie ["Erste Schritte mit HTML"][MDNGettingStartedHtml].  
*   Laden Sie den [Microsoft Edge][MicrosoftEdgeInsider] Webbrowser herunter.  Dieses Lernprogramm verwendet eine Reihe von Webentwicklungstools, die als Microsoft Edge DevTools bezeichnet werden, die in Microsoft Edge integriert sind.  

## <a name="set-up-your-code"></a>Einrichten des Codes  

Sie werden eine Website im Glitch-Onlinecode-Editor erstellen.  

1.  Öffnen Sie den [Quellcode.][GlitchAlluringShockIndex] Diese Registerkarte wird in diesem Lernprogramm als **Editor-Registerkarte** bezeichnet.  
    
    :::image type="complex" source="media/beginners-html-setup1.msft.png" alt-text="Die Registerkarte "Editor"" lightbox="media/beginners-html-setup1.msft.png":::
       Die Registerkarte "Editor"  
    :::image-end:::  
    
1.  Wählen Sie **"Verallgemählt" aus.** Das Menü **Project Optionen** wird geöffnet.  
    
    :::image type="complex" source="media/beginners-html-setup2.msft.png" alt-text="Menü "Project-Optionen"" lightbox="media/beginners-html-setup2.msft.png":::
       Menü "Project-Optionen"  
    :::image-end:::  
    
1.  Wählen Sie **Remix Project**aus. Glitch erstellt eine Kopie des Projekts, die Sie bearbeiten können, und generiert zufällig einen neuen Namen für das Projekt. Der Inhalt ist derselbe wie zuvor.  
    
    :::image type="complex" source="media/beginners-html-setup3.msft.png" alt-text="Das remixierte Projekt" lightbox="media/beginners-html-setup3.msft.png":::
       Das remixierte Projekt  
    :::image-end:::  
    
1.  Wenn Sie das nächste Lernprogramm dieser Reihe abschließen möchten, wählen Sie "Bei Glitch **anmelden"** mit Ihrem Facebook-, GitHub- oder Google-Konto aus. oder senden Sie sich selbst einen Hexenlink. Wenn Sie sich nicht bei einem Konto anmelden möchten, können Sie das Projekt nach dem Schließen der Editorregisterkarte nicht bearbeiten.

1.  Wählen **** Sie  \>  **"In einem neuen Fenster anzeigen"** aus.  Eine neue Registerkarte mit der Liveseite wird geöffnet. Diese Registerkarte wird in diesem Lernprogramm als **Live-Registerkarte** bezeichnet.  
    
    :::image type="complex" source="media/beginners-html-setup4.msft.png" alt-text="Die Live-Registerkarte" lightbox="media/beginners-html-setup4.msft.png":::
       Die Live-Registerkarte  
    :::image-end:::  
    
## <a name="add-content"></a>Hinzufügen von Inhalten  

Ihre Website benötigt weitere Informationen. Führen Sie die folgenden Schritte aus, um Einige Inhalte hinzuzufügen.  

1. Ersetzen Sie auf der **Registerkarte "Editor"** `<!-- You're "About Me" will go here.  -->` durch `<h1>About Me</h1>` .  
    
    ```html
        ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                </main>
        ...
    ```  
    
    :::image type="complex" source="media/beginners-html-add1.msft.png" alt-text="Der neue Code wird auf der Registerkarte "Editor" hervorgehoben." lightbox="media/beginners-html-add1.msft.png":::
        Der neue Code wird auf der Registerkarte "Editor" hervorgehoben.  
    :::image-end:::  
    
1. Zeigen Sie Ihre Änderungen auf der **Registerkarte "Live" an.** Der Text `About Me` ist auf der Seite sichtbar. Der Text ist größer als der umgebende Text, da das `<h1>` Element eine Überschrift 1 darstellt.  Ihr Webbrowser formatiert Überschriften automatisch in größeren Schriftgraden.  
    
    :::image type="complex" source="media/beginners-html-add2.msft.png" alt-text="Die neue Überschrift ist auf der Registerkarte "Live" sichtbar." lightbox="media/beginners-html-add2.msft.png":::
       Die neue Überschrift ist auf der Registerkarte "Live" sichtbar.  
    :::image-end:::  
    
1. Zurück auf der **Registerkarte "Editor"** fügen Sie `<p>I am learning web development. Recent accomplishments:</p>` die Zeile darunter  `<h1>About Me</h1>` ein.  
    
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

    :::image type="complex" source="media/beginners-html-add3.msft.png" alt-text="Der aktualisierte Code wird auf der Registerkarte "Editor" hervorgehoben." lightbox="media/beginners-html-add3.msft.png":::
        Der aktualisierte Code wird auf der Registerkarte "Editor" hervorgehoben.  
    :::image-end:::  
    
1. Zeigen Sie Ihre Änderung auf der **Registerkarte "Live" an.**

1. Fügen Sie auf der **Registerkarte "Editor"** mithilfe des folgenden Codes eine Liste Ihrer Erfolge hinzu.
    
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

    :::image type="complex" source="media/beginners-html-add4.msft.png" alt-text="Der aktualisierte Code wird auch auf der Registerkarte "Editor" hervorgehoben." lightbox="media/beginners-html-add4.msft.png":::
        Der aktualisierte Code wird auch auf der Registerkarte "Editor" hervorgehoben.  
    :::image-end:::  

1. Zeigen Sie die **Live-Registerkarte** an, um sicherzustellen, dass der neue Inhalt korrekt angezeigt wird.  
    
    :::image type="complex" source="media/beginners-html-add5.msft.png" alt-text="Die neue Liste ist auf der Registerkarte "Live" sichtbar." lightbox="media/beginners-html-add5.msft.png":::
       Die neue Liste ist auf der Registerkarte "Live" sichtbar.  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a>Experimentieren Mit Inhaltsänderungen in Microsoft Edge DevTools  

Wenn Sie eine Seite mit viel HTML entwickeln, wird es mühsam, zwischen der Editor-Registerkarte und der Live-Registerkarte hin und her zu wechseln, um Ihre Änderungen anzuzeigen. Microsoft Edge DevTools hilft Ihnen beim Experimentieren mit Inhaltsänderungen, ohne die **Live-Registerkarte**zu verlassen.  

### <a name="learn-the-difference-between-html-and-the-dom"></a>Lernen Sie den Unterschied zwischen HTML und DOM kennen.  

Bevor Sie Inhalte von Microsoft Edge DevTools bearbeiten, sollten wir den Unterschied zwischen HTML und DOM verstehen. Fahren Sie mit den folgenden Schritten fort, um von einem Beispiel zu lernen.

1. Navigieren Sie zur **Registerkarte "Live".** Am unteren Rand der Seite wird der Text `A new element!?!` angezeigt.  

    <!--
        :::image type="complex" source="media/beginners-html-dom1.msft.png" alt-text="At the bottom of the page the text A new element!?! displays" lightbox="media/beginners-html-dom1.msft.png":::
        At the bottom of the page the text `A new element!?!` is displays  
        :::image-end:::
    -->
    
1. Öffnen Sie die **Registerkarte "Editor",** und versuchen Sie, den Text in zu `index.html` finden. Der Text wird in dieser Ansicht nicht angezeigt.  

    <!--
        :::image type="complex" source="media/beginners-html-dom2.msft.png" alt-text="The mystery text A new element!?! is not found in index.html" lightbox="media/beginners-html-dom2.msft.png":::
        The mystery text `A new element!?!` is not found in `index.html`  
        :::image-end:::
    -->

1. Öffnen Sie die **Registerkarte "Live",** zeigen Sie darauf, öffnen Sie `A new element!?!` das Kontextmenü (Rechtsklick), und wählen Sie dann **"Überprüfen"** aus.  
    
    :::image type="complex" source="media/beginners-html-dom3.msft.png" alt-text="Überprüfen von Text" lightbox="media/beginners-html-dom3.msft.png":::
       Überprüfen von Text  
    :::image-end:::  
    
    DevTools wird zusammen mit Ihrer Seite geöffnet. `<div>A new element!?!</div>` hervorgehoben ist. Obwohl diese Struktur in DevTools wie HTML aussieht, ist sie die **DOM-Struktur.**  
    
    :::image type="complex" source="media/beginners-html-dom4.msft.png" alt-text="DevTools ist neben der Seite geöffnet" lightbox="media/beginners-html-dom4.msft.png":::
       DevTools ist neben der Seite geöffnet  
    :::image-end:::  
    
Wenn Ihre Seite geladen wird, verwendet der Browser den HTML-Code, um den anfänglichen Inhalt der Seite zu erstellen. Das DOM stellt den aktuellen Inhalt der Seite dar, der sich im Laufe der Zeit ändern kann. 

Der `<div>A new element!?!</div>` Inhalt wird ihrer Seite aufgrund des Tags am `<script src="new.js"></script>` unteren Rand Ihres HTML-Codes hinzugefügt. Dieses Tag bewirkt, dass JavaScript-Code ausgeführt wird. Weitere Informationen zu JavaScript finden Sie in einem [späteren Lernprogramm.](../javascript/index.md)

Stellen Sie sich vorerst eine Skriptsprache vor, die den Inhalt Ihrer Seite ändern kann. In diesem Fall wird Ihrer Seite JavaScript-Code `<div>A new element!?!</div>` hinzugefügt. Aus diesem Grund wird dieser Text auf der **Live-Registerkarte,** aber nicht im HTML-Code angezeigt.  

### <a name="edit-the-dom"></a>Bearbeiten des DOM  

Wenn Sie schnell mit Inhaltsänderungen experimentieren möchten, ohne die Live-Registerkarte verlassen zu müssen, testen Sie DevTools.  

1.  Zeigen Sie in DevTools mit dem Mauszeiger darauf, öffnen Sie `Your site!` das Kontextmenü (rechtsklick), und wählen Sie **"Als HTML bearbeiten"** aus.  
    
1.  Ersetzen Sie `<p>Your site!</p>` dies durch den folgenden Code.  

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

1.  Wählen Sie `Control` + `Enter` \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus, um Ihre Änderungen zu speichern, oder wählen Sie außerhalb des Felds aus. Ihre Änderungen werden automatisch in der Liveansicht Ihrer Seite angezeigt. Der Text `Your site!` wurde durch den neuen Inhalt ersetzt.  
    
    :::image type="complex" source="media/beginners-html-edit3.msft.png" alt-text="Der neue Inhalt wird sofort auf der Seite angezeigt." lightbox="media/beginners-html-edit3.msft.png":::
       Der neue Inhalt wird sofort auf der Seite angezeigt.  
    :::image-end:::  
    
Dieser Workflow eignet sich nur für das Experimentieren mit Inhaltsänderungen. Wenn Sie die Seite aktualisieren oder die Registerkarte schließen, gehen Ihre Änderungen verloren. Wenn Sie Ihre Änderungen speichern möchten, kopieren Sie den Code manuell in Ihre HTML-Datei. In den nächsten Abschnitten werden einige weitere Möglichkeiten zum Ändern von Inhalten aus der DOM-Struktur erläutert.  

## <a name="reorder-nodes"></a>Knoten neu anordnen

Sie können auch die Reihenfolge der DOM-Knoten ändern. Beispielsweise befindet sich das Navigationsmenü auf ihrer Webseite am unteren Rand. Führen Sie die folgenden Schritte aus, um sie nach oben zu verschieben.  

1.  Suchen Sie den `<nav>` Knoten in der **DOM-Struktur** von DevTools.  
    
    :::image type="complex" source="media/beginners-html-reorder1.msft.png" alt-text="Der Navigationsknoten ist in DevTools hervorgehoben." lightbox="media/beginners-html-reorder1.msft.png":::
       Der Navigationsknoten ist in DevTools hervorgehoben.  
    :::image-end:::  
    
1.  Ziehen Sie den `<nav>` Knoten nach oben, damit der Knoten das erste untergeordnete Element nach dem `<body>` Knoten ist.  
    
    :::image type="complex" source="media/beginners-html-reorder3.msft.png" alt-text="Der Navigationsknoten befindet sich oben auf der Seite." lightbox="media/beginners-html-reorder3.msft.png":::
        Der Navigationsknoten befindet sich oben auf der Seite.  
    :::image-end:::  
    
### <a name="delete-a-node"></a>Löschen eines Knotens

Sie können auch Knoten aus der DOM-Struktur entfernen. Führen Sie die folgenden Schritte aus.

1.  Wählen Sie in der **DOM-Struktur** `<div>A new element!?!</div>` . DevTools hebt den Knoten hervor. 
    
1.  Wählen Sie die `Delete` Taste auf der Tastatur aus.  Der `<div>A new element!?!</div>` Knoten wird aus der DOM-Struktur entfernt.  
    
    :::image type="complex" source="media/beginners-html-delete2.msft.png" alt-text="Der Knoten wurde gelöscht." lightbox="media/beginners-html-delete2.msft.png":::
       Der Knoten wurde gelöscht.  
    :::image-end:::  
    
## <a name="copy-your-changes"></a>Kopieren Ihrer Änderungen  

Sie sind fast fertig. Sie haben einige Änderungen an der Seite in DevTools vorgenommen, diese werden jedoch nicht im Quellcode gespeichert.  

1.  Aktualisieren Sie die **Live-Registerkarte**. Die Änderungen, die Sie in der DOM-Struktur vorgenommen haben, werden nicht mehr angezeigt. Insbesondere kehrt der Text `Your site!` zum oberen Rand der Seite zurück, und der Text wird nach unten `A new element!?!` zurückgegeben.  
    
    :::image type="complex" source="media/beginners-html-copy1.msft.png" alt-text="Die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden." lightbox="media/beginners-html-copy1.msft.png":::
       Die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden.  
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
    
1.  Wechseln Sie zurück zur **Registerkarte "Editor",** und ersetzen Sie den Inhalt Der `index.html` Datei durch den Code, den Sie kopiert haben.  
    
    :::image type="complex" source="media/beginners-html-copy2.msft.png" alt-text="Aussehen der index.html-Datei" lightbox="media/beginners-html-copy2.msft.png":::
       So sollte Ihre `index.html` Datei aussehen  
    :::image-end:::  
    
## <a name="next-steps"></a>Nächste Schritte  

*   Schließen Sie das nächste Lernprogramm dieser Reihe [ab, Erste Schritte mit CSS,][DevToolsBeginnersCss]um zu erfahren, wie Sie Ihre Seite formatieren und mit Formatvorlagenänderungen in Microsoft Edge DevTools experimentieren.  
*   Lesen Sie ["Einführung in das DOM",][MDNIntroductionDom] um mehr über das DOM zu erfahren.  
*   Sehen Sie sich einen Kurs wie ["Einführung in die Webentwicklung"][CourseraIntroductionToWebDevelopment] an, um weitere praktische Webentwicklungserfahrungen zu erhalten.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools für Anfänger: Erste Schritte mit CSS-| Microsoft-Dokumente"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Einführung in webentwicklungs | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html – | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Erste Schritte mit HTML-| Mdn"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in die DOM-| Mdn"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die originale Seite wurde [hier](https://developers.google.com/web/tools/chrome-devtools/beginners/html) gefunden und von [Einersine(" ("Technical][KatherineJackson] Writer Intern", "Chrome DevTools\") verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
