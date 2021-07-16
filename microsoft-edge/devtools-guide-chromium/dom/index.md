---
description: Anzeigen von Knoten, Suchen nach Knoten, Bearbeiten von Knoten, Verweisen auf Knoten in der Konsole, Unterbrechen von Knotenänderungen und vieles mehr.
title: Erste Schritte mit dem Anzeigen und Ändern des DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 8340c4d4d7eacdb6ad4155c1c9699db150522f16
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643434"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="get-started-with-viewing-and-changing-the-dom"></a>Erste Schritte mit dem Anzeigen und Ändern des DOM  

Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen zum Anzeigen und Ändern des [Dokumentobjektmodells](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\) einer Seite mit Microsoft Edge DevTools zu erlernen.  

In diesem Lernprogramm wird davon ausgegangen, dass Sie den Unterschied zwischen DOM und HTML kennen. Navigieren Sie zu [Anhang: HTML im Vergleich zum DOM,](#appendix-html-versus-the-dom) um eine Erklärung zu geben.  

## <a name="open-dom-examples"></a>Open DOM-Beispiele  

1.  Halten Sie `Control` \(Windows, Linux\) oder `Command` \(macOS\) gedrückt, und wählen Sie **DOM-Beispiele aus,** um sie auf einer neuen Registerkarte zu öffnen.  
    
    [DOM-Beispiele][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a>Anzeigen von DOM-Knoten  

In der DOM-Struktur des Elements-Bereichs werden alle DOM-bezogenen Aktivitäten in DevTools ausgeführt.  

### <a name="inspect-a-node"></a>Überprüfen eines Knotens  

Wenn Sie an einem bestimmten DOM-Knoten interessiert sind, ist **Inspect** eine schnelle Möglichkeit, DevTools zu öffnen und diesen Knoten zu untersuchen.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Wählen Sie unter **"Knoten überprüfen"** mit der rechten Maustaste **"Überprüfen"** **aus.**  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Überprüfen eines Knotens" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Überprüfen eines Knotens  
    :::image-end:::  
    
    1.  Das **Elementtool** von DevTools wird geöffnet.  `<li>Michelangelo</li>` ist in der **DOM-Struktur**hervorgehoben.  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Hervorheben des Knotens Knoten" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Hervorheben des `Michelangelo` Knotens  
        :::image-end:::  
        
        1.  Klicken Sie in der oberen linken Ecke von DevTools auf das Symbol **"Überprüfen** ![ \( Überprüfen ](../media/inspect-icon.msft.png) \)".  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Das Inspect-Symbol" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               Das **** Inspect-Symbol  
            :::image-end:::  
            
1.  Wählen Sie unter **"Knoten überprüfen"** den Text **"Tokio"** aus.  Wird nun `<li>Tokyo</li>` in der DOM-Struktur hervorgehoben.  

Das Überprüfen eines Knotens ist auch der erste Schritt zum Anzeigen und Ändern der Formatvorlagen eines Knotens.  Navigieren Sie mit dem Anzeigen und Ändern von CSS zu [Erste Schritte.][DevToolsCssGetStarted]  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a>Navigieren in der DOM-Struktur mit einer Tastatur  

Nachdem Sie einen Knoten in der DOM-Struktur ausgewählt haben, können Sie mit ihrer Tastatur in der DOM-Struktur navigieren.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Wählen Sie unter **"DOM-Struktur mit Tastatur navigieren" mit**der rechten Maustaste **"Ringo"** aus, und wählen Sie **"Überprüfen"** aus.  `<li>Ringo</li>` ist in der DOM-Struktur ausgewählt.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Überprüfen des Ringo-Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Überprüfen des `Ringo` Knotens  
    :::image-end:::  
    
    1.  Wählen Sie die `Up` Pfeiltaste zweimal aus.  `<ul>`  markiert ist.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Überprüfen des ul-Knotens" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Überprüfen des `ul` Knotens  
        :::image-end:::  
        
    1.  Wählen Sie die `Left` Pfeiltaste aus.  Die `<ul>` Liste wird reduziert.  
    1.  Wählen Sie erneut die `Left` Pfeiltaste aus.  Das übergeordnete Element des `<ul>` Knotens ist ausgewählt.  In diesem Fall ist dies die `<div>` mit der `navigate-the-dom-tree-with-a-keyboard-1` ID.  
    1.  Wählen Sie die `Down` Pfeiltaste zweimal aus, damit Sie die gerade reduzierte Liste erneut ausgewählt `<ul>` haben.  Es sollte wie folgt aussehen: `<ul>... </ul>`  
    1.  Wählen Sie die `Right` Pfeiltaste aus.  Die Liste wird erweitert.  

### <a name="scroll-into-view"></a>Bildlauf in die Ansicht  

Beim Anzeigen der DOM-Struktur sind Sie möglicherweise an einem DOM-Knoten interessiert, der sich derzeit nicht im Viewport befindet.  Angenommen, Sie scrollen nach unten auf der Seite, und sie interessieren sich für den `<h1>` Knoten oben auf der Seite.  **Mit einem Bildlauf in** die Ansicht können Sie den Viewport schnell neu positionieren, damit Sie den Knoten überprüfen können.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Klicken Sie unter **"In Ansicht scrollen"** mit der rechten Maustaste auf **"Magritte",** und wählen Sie **"Überprüfen"** aus.  
1.  Scrollen Sie zum Ende der DOM-Beispielseite.  
1.  Der `<li>Magritte</li>` Knoten sollte weiterhin in ihrer DOM-Struktur ausgewählt werden.  Wenn nicht, wechseln Sie zurück zum [Bildlauf in](#scroll-into-view) die Ansicht, und beginnen Sie von vorn.  
1.  Zeigen Sie auf den Knoten, öffnen Sie `<li>Magritte</li>` das Kontextmenü \(Rechtsklick\), und wählen Sie **Bildlauf in die Ansicht**aus.  Ihr Viewport scrollt wieder nach oben, sodass Sie den **Magritte-Knoten** überprüfen können.  Navigieren Sie zu [Anhang: Fehlende Optionen,](#appendix-missing-options) wenn Sie die Option **"In Ansicht** scrollen" nicht überprüfen können.
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Bildlauf in die Ansicht" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Bildlauf in die Ansicht**  
    :::image-end:::  

### <a name="search-for-nodes"></a>Suchen nach Knoten  

Sie können die DOM-Struktur nach Zeichenfolge, CSS-Selektor oder XPath-Auswahl durchsuchen.  

1.  Konzentrieren Sie den Cursor auf **das** Elementtool.  
1.  Wählen Sie `Control` + `F` \(Windows, Linux\) oder `Command` + `F` \(macOS\) aus.  Die Suchleiste wird am unteren Rand der DOM-Struktur geöffnet.  
1.  Geben Sie `The Moon is a Harsh Mistress` ein.  Der letzte Satz wird in der DOM-Struktur hervorgehoben.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Hervorheben der Abfrage in der Suchleiste" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Hervorheben der Abfrage in der Suchleiste  
    :::image-end:::  
    
Wie oben erwähnt, unterstützt die Suchleiste auch CSS- und XPath-Selektoren.  

## <a name="edit-the-dom"></a>Bearbeiten des DOM  

Sie können das DOM im Fly-Format bearbeiten und überprüfen, wie sich die Änderungen auf die Seite auswirken.  

### <a name="edit-content"></a>Inhalt bearbeiten  

Doppelklicken Sie zum Bearbeiten des Inhalts eines Knotens auf den Inhalt in der DOM-Struktur.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Klicken Sie unter **Inhalt bearbeiten**mit der rechten Maustaste auf **"Michelle",** und wählen Sie **"Überprüfen"** aus.  
    1.  Doppelklicken Sie in der DOM-Struktur auf `Michelle` .  Doppelklicken Sie also auf den Text zwischen `<li>` und `</li>` .  Der Text wird hervorgehoben, um anzugeben, dass er ausgewählt ist.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Bearbeiten des Texts" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Bearbeiten des Texts  
        :::image-end:::  
        
    1.  Löschen Sie , geben Sie ein, und `Michelle` wählen Sie dann `Leela` `Enter` aus, um die Änderung zu bestätigen.  Der Text im DOM ändert sich von **Michelle** zu **Leela**.  

### <a name="edit-attributes"></a>Bearbeiten von Attributen  

Doppelklicken Sie zum Bearbeiten von Attributen auf den Attributnamen oder -wert.  Befolgen Sie die Anweisungen, um zu erfahren, wie Sie einem Knoten Attribute hinzufügen.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Wählen Sie unter **"Attribute bearbeiten"** mit der rechten **Maustaste",** und wählen Sie **"Überprüfen"** aus.  
1.  Doppelklicken Sie auf `<li>` .  Der Text wird hervorgehoben, um anzugeben, dass der Knoten ausgewählt ist.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Bearbeiten des Knotens" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Bearbeiten des Knotens  
    :::image-end:::  
    
1.  Wählen Sie die `Right` Pfeiltaste aus, fügen Sie ein Leerzeichen hinzu, geben Sie `style="background-color:gold"` ein, und wählen Sie dann `Enter` aus.  Die Hintergrundfarbe des Knotens ändert sich in Gold.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Hinzufügen eines Style-Attributs zum Knoten" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Hinzufügen eines `style` Attributs zum Knoten  
    :::image-end:::  
    
### <a name="edit-node-type"></a>Knotentyp bearbeiten  

Doppelklicken Sie zum Bearbeiten des Knotentyps auf den Typ, und geben Sie dann den neuen Typ ein.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Klicken Sie unter **Knotentyp bearbeiten**mit der rechten Maustaste auf **"Hank",** und wählen Sie **"Überprüfen"** aus.  
    1.  Doppelklicken Sie auf `<li>` .  Der Text `li` ist hervorgehoben.  
    1.  Löschen `li` , eingeben , dann auswählen `button` `Enter` .  Der `<li>` Knoten wird in einen Knoten `<button>` geändert.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Ändern des Knotentyps in die Schaltfläche" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Ändern des Knotentyps in `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a>Neu anordnen von DOM-Knoten  

Ziehen Sie Knoten, um sie neu anzuordnen.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Wählen Sie unter **"DOM-Knoten neu anordnen"** mit der rechten Maustaste **"Presley"** aus, und wählen Sie **"Überprüfen"** aus.  
    
    > [!NOTE]
    > Es ist das letzte Element in der Liste.  
    
    1.  Ziehen Sie in der DOM-Struktur `<li>Elvis Presley</li>` an den Anfang der Liste.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Ziehen Des Knotens an den Anfang der Liste" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Ziehen Des Knotens an den Anfang der Liste  
        :::image-end:::  
        
### <a name="force-state"></a>Erzwingen des Zustands  

Sie können erzwingen, dass Knoten in Zuständen wie `:active` , `:hover` , und `:focus` `:visited` `:focus-within` verbleiben.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Zeigen Sie im **Zustand "Force"** auf **"TheRest of the Mof".**  Die Hintergrundfarbe wird orange.  
    1.  Zeigen Sie auf **"The Menu of the Maustaste",** öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **"Überprüfen"** aus.  
    1.  Zeigen Sie auf , öffnen Sie `<li class="demo--hover">The Lord of the Flies</li>` das Kontextmenü \(rechtsklick\), und wählen Sie **"Zustand erzwingen":Hover**  >  ****.  Navigieren Sie zu [Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.  Die Hintergrundfarbe bleibt orange, auch wenn Sie nicht tatsächlich auf den Knoten zeigen.  

### <a name="hide-a-node"></a>Ausblenden eines Knotens  

Wählen Sie `H` diese Option aus, um einen Knoten auszublenden.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Klicken Sie unter **"Knoten ausblenden"** mit der rechten Maustaste auf **"The Stars My Destination",** und wählen Sie **"Überprüfen"** aus.  
    1.  Wählen Sie den `H` Schlüssel aus.  Der Knoten ist ausgeblendet.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Wie der Knoten in der DOM-Struktur aussieht, nachdem er ausgeblendet wurde" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           Wie der Knoten in der DOM-Struktur aussieht, nachdem er ausgeblendet wurde  
        :::image-end:::  
        
    1.  Wählen Sie die `H` Taste erneut aus.  Der Knoten wird erneut angezeigt.  

### <a name="delete-a-node"></a>Löschen eines Knotens  

Wählen Sie `Delete` diese Option aus, um einen Knoten zu löschen.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Klicken Sie unter **"Knoten löschen"** mit der rechten Maustaste auf **"Foundation",** und wählen Sie **"Überprüfen"** aus.  
    1.  Wählen Sie den `Delete` Schlüssel aus.  Der Knoten wird gelöscht.  
    1.  Wählen Sie `Control` + `Z` \(Windows, Linux\) oder `Command` + `Z` \(macOS\) aus.  Die letzte Aktion wird rückgängig und der Knoten erneut angezeigt.  

## <a name="access-nodes-in-the-console"></a>Zugriffsknoten in der Konsole  

DevTools bietet einige Tastenkombinationen für den Zugriff auf DOM-Knoten über die Konsole oder zum Abrufen von JavaScript-Verweisen auf die einzelnen Knoten.  

### <a name="reference-the-currently-selected-node-with-0"></a>Verweisen Auf den aktuell ausgewählten Knoten mit $0  

Wenn Sie einen Knoten untersuchen, bedeutet der `== $0` Text neben dem Knoten, dass Sie in der Konsole mit der Variablen auf diesen Knoten verweisen `$0` können.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Under **Reference the currently-selected node with $0**, right-choose **The left hand of Darkness** and choose **Inspect**.  
    1.  Wählen Sie die `Escape` Taste aus, um die Konsolenschublade zu öffnen.  
    1.  Geben Sie `$0` den Schlüssel ein, und wählen Sie den `Enter` Schlüssel aus.  Das Ergebnis des Ausdrucks zeigt, dass `$0` ausgewertet `<li>The Left Hand of Darkness</li>` wird.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Das Ergebnis des ersten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            Das Ergebnis des ersten `$0` **Ausdrucks** in der Konsole  
        :::image-end:::  
        
    1.  Zeigen Sie auf das Ergebnis.  Der Knoten wird im Viewport hervorgehoben.  
    1.  Wählen Sie `<li>Dune</li>` in der DOM-Struktur aus, geben Sie `$0` die Konsole erneut ein, und wählen Sie dann `Enter` erneut aus.  Wird `$0` nun ausgewertet zu `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Das Ergebnis des zweiten $0-Ausdrucks in der Konsole" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           Das Ergebnis des zweiten `$0` **Ausdrucks** in der Konsole  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a>Store als globale Variable  

Wenn Sie mehrmals auf einen Knoten verweisen müssen, speichern Sie ihn als globale Variable.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Zeigen Sie unter **Store als globale Variable**auf **"The Big Sleep",** öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **"Überprüfen"** aus.  
    1.  Zeigen Sie `<li>The Big Sleep</li>` in der DOM-Struktur darauf, öffnen Sie das Kontextmenü \(Rechtsklick\), und wählen Sie **Store als globale Variable**aus.  Navigieren Sie zu [Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.  
    1.  Geben Sie `temp1` die Konsole ein, und wählen Sie dann `Enter` aus.  Das Ergebnis des Ausdrucks zeigt, dass die Variable auf den Knoten ausgewertet wird.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Das Ergebnis des ausdrucks temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           Das Ergebnis des `temp1` Ausdrucks  
        :::image-end:::  
        
### <a name="copy-js-path"></a>JS-Pfad kopieren  

Kopieren Sie den JavaScript-Pfad zu einem Knoten, wenn Sie in einem automatisierten Test darauf verweisen müssen.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Zeigen Sie unter **"JS-Pfad kopieren"** auf **"TheZzov",** öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **"Überprüfen"** aus.  
    1.  Zeigen Sie `<li>The Brothers Karamazov</li>` in der DOM-Struktur darauf, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie ****  >  **"JS-Pfad kopieren"** aus.  Ein `document.querySelector()` Ausdruck, der in den Knoten aufgelöst wird, wurde in die Zwischenablage kopiert.  
    1.  Wählen Sie `Control` + `V` \(Windows, Linux\) oder `Command` + `V` \(macOS\) aus, um den Ausdruck in die Konsole einzufügen.  
    1.  Wählen Sie `Enter` diese Option aus, um den Ausdruck auszuwerten.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Das Ergebnis des Ausdrucks JS-Pfad kopieren" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           Das Ergebnis des Ausdrucks **"JS-Pfad kopieren"**  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a>Unterbrechen von DOM-Änderungen  

Mit DevTools können Sie das JavaScript einer Seite anhalten, wenn javaScript das DOM ändert.  

### <a name="break-on-attribute-modifications"></a>Unterbrechen von Attributänderungen  

Verwenden Sie Haltepunkte für die Attributänderung, wenn Sie das JavaScript anhalten möchten, das bewirkt, dass sich jedes Attribut eines Knotens ändert.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Klicken Sie unter **"Unterbrechen" auf Attributänderungen**mit der rechten Maustaste **auf",** und wählen Sie **"Überprüfen"** aus.  
    1.  Zeigen Sie in der DOM-Struktur auf , öffnen Sie `<li id="target">Sauerkraut</li>` das Kontextmenü \(rechtsklick\), und wählen Sie **"Bei**  >  **Attributänderungen unterbrechen"** aus.  Navigieren Sie zu [Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Unterbrechen von Attributänderungen" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Unterbrechen von Attributänderungen**  
        :::image-end:::  
        
    1.  Im nächsten Schritt werden Sie angewiesen, eine Schaltfläche auszuwählen, mit der der Code der Seite angehalten wird.  Nachdem die Seite angehalten wurde, können Sie keinen Bildlauf mehr auf der Seite ausführen.  Sie müssen **"Skript fortsetzen"** \( ![ "Skript ](../media/resume-script-icon.msft.png) fortsetzen"\) auswählen, damit die Seite erneut bildlauffähig ist.
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Ort, an dem die Skriptausführung fortgesetzt werden soll" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Ort, an dem die Skriptausführung fortgesetzt werden soll  
        :::image-end:::  
        
    1.  Klicken Sie oben auf die Schaltfläche **"Hintergrund festlegen".**  Dadurch wird das `style` Attribut des Knotens auf `background-color:thistle` .  DevTools hält die Seite an und hebt den Code hervor, der zu einer Änderung des Attributs geführt hat.  
    1.  Wählen Sie **"Skript fortsetzen"** \( ![ "Skript ](../media/resume-script-icon.msft.png) fortsetzen", wie bereits erwähnt).  
    
### <a name="break-on-node-removal"></a>Unterbrechung beim Entfernen von Knoten  

Wenn Sie anhalten möchten, wenn ein bestimmter Knoten entfernt wird, verwenden Sie Haltepunkte zum Entfernen von Knoten.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Wählen Sie unter **"Unterbrechung beim Entfernen von Knoten"** mit der rechten Maustaste **"Doppelklicken"** aus, und wählen Sie **"Überprüfen"** aus.  
    1.  Zeigen Sie in der DOM-Struktur auf , öffnen Sie `<li id="target">Neuromancer</li>` das Kontextmenü \(rechtsklick\), und wählen Sie **"Beim**  >  **Entfernen von Knoten unterbrechen" aus.**  Navigieren Sie zu [Anhang: Fehlende Optionen,](#appendix-missing-options) wenn die Option nicht angezeigt wird.  
    1.  Klicken Sie oben auf die Schaltfläche **"Löschen".**  DevTools hält die Seite an und hebt den Code hervor, der dazu führte, dass der Knoten entfernt wurde.  
    1.  Wählen Sie **"Skript fortsetzen"** \( ![ "Skript ](../media/resume-script-icon.msft.png) fortsetzen" \) aus.  
    
### <a name="break-on-subtree-modifications"></a>Unterbrechen von Unterstrukturänderungen  

Nachdem Sie einen Unterstrukturänderungs-Haltepunkt auf einem Knoten platziert haben, hält DevTools die Seite an, wenn eines der Nachfolger des Knotens hinzugefügt oder entfernt wird.  

1.  [Open DOM Examples](#open-dom-examples).  
1.  Under **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** and choose **Inspect**.  
    1.  Zeigen Sie in der DOM-Struktur auf den Knoten oben , öffnen Sie `<ul id="target">` `<li>A Fire Upon the Deep</li>` das Kontextmenü \(Rechtsklick\), und wählen Sie **"Bei**  >  **Unterstrukturänderungen unterbrechen"** aus.  Wenn die Option nicht angezeigt wird, navigieren Sie zu [Anhang: Fehlende Optionen.](#appendix-missing-options)  
    1.  Wählen Sie **Untergeordnetes hinzufügen**aus.  Der Code wird angehalten, da der Liste ein `<li>` Knoten hinzugefügt wurde.  
    1.  Wählen Sie **"Skript fortsetzen"** \( ![ "Skript ](../media/resume-script-icon.msft.png) fortsetzen" \) aus.  
    
## <a name="next-steps"></a>Nächste Schritte  

Dies deckt die meisten DOM-bezogenen Features in DevTools ab.  Sie können die restlichen Features ermitteln, indem Sie auf Knoten in der DOM-Struktur zeigen, das Kontextmenü \(Rechtsklick\) öffnen und mit den anderen Optionen experimentieren, die in diesem Lernprogramm nicht behandelt wurden.  Navigieren Sie zu [Tastenkombinationen für den Elementbereich.][DevToolsShortcutsElements]  

Sehen Sie sich die [Microsoft Edge DevTools-Homepage][MicrosoftEdgeDevTools] an, um alles zu entdecken, was Sie mit DevTools noch tun können.  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a>Anhang: HTML im Vergleich zum DOM  

Im folgenden Abschnitt wird der Unterschied zwischen HTML und DOM schnell erläutert.  

:::row:::
   :::column span="":::
      Wenn Sie einen Webbrowser verwenden, um eine Seite anzufordern, gibt der Server HTML wie den folgenden Codeausschnitt zurück.  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      Der Browser analysiert den HTML-Code und erstellt eine Struktur von Objekten wie die folgende Liste.  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

Diese Struktur von Objekten oder Knoten, die den Inhalt der Seite darstellen, wird dom genannt.  

:::row:::
   :::column span="":::
      Derzeit sieht es wie der HTML-Code aus, aber nehmen wir an, dass das Skript, auf das unten im HTML-Code verwiesen wird, den folgenden Codeausschnitt ausführt.  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      Mit diesem Code wird der Knoten entfernt `h1` und dem DOM ein weiterer Knoten `p` hinzugefügt.  Das vollständige DOM zeigt nun die folgende Liste an.  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

Der HTML-Code für die Seite unterscheidet sich jetzt vom DOM.  Mit anderen Worten: HTML stellt den anfänglichen Seiteninhalt dar, und das DOM stellt den aktuellen Seiteninhalt dar.  Wenn JavaScript Knoten hinzufügt, entfernt oder bearbeitet, unterscheidet sich das DOM vom HTML-Code.  

Navigieren Sie zu ["Einführung in das DOM",][MDNIntroductionToDOM] um mehr zu erfahren.  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a>Anhang: Fehlende Optionen  

Viele der Anweisungen in diesem Lernprogramm weisen Sie an, auf einen Knoten in der DOM-Struktur zu zeigen, das Kontextmenü \(Rechtsklick\) zu öffnen und dann eine Option aus dem Kontextmenü auszuwählen, das angezeigt wird.  Wenn die angegebene Option im Kontextmenü nicht angezeigt wird, versuchen Sie, mit dem Mauszeiger vom Knotentext wegzuzeigen und das Kontextmenü \(Rechtsklick\) zu öffnen.  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Ort der Auswahl, ob nicht alle Optionen angezeigt werden" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Ort der Auswahl, ob nicht alle Optionen angezeigt werden  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge \(Chromium\) | Microsoft-Dokumente"  
[DevToolsCssGetStarted]: ../css/index.md "Erste Schritte Mit Anzeigen und Ändern von CSS-| Microsoft-Dokumente"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Tastenkombinationen des Elements-Tools – Microsoft Edge DevTools-Tastenkombinationen | Microsoft-Dokumente"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chromium) DevTools-DOM-Beispiel | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in die DOM-| Mdn"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/dom/index) zu finden und wurde von [Kaince-Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Ausrufebereich\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
