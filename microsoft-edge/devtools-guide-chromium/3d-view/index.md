---
description: Alles über die 3D-Ansicht und deren Verwendung
title: 3D-Ansicht
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: bd91939a19f02a426834a85ef92eca388f8f1eda
ms.sourcegitcommit: 5e218b24fb21fcfa9c82b99f17373fed1ba5a21c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2021
ms.locfileid: "11203970"
---
# <a name="3d-view"></a>3D-Ansicht  

Verwenden Sie die **3D-Ansicht**, um Ihre Webanwendung zu debuggen, indem Sie durch das [Dokumentobjektmodell (DOM)][MDNDocumentObjectModel] oder den [z-index][MDNZIndex]-Stapelkontext navigieren.  Damit können Sie die folgenden Aufgaben ausführen:  

*   [Erkunden der Webseite, übersetzt in eine 3D-Perspektive](#3d-dom)  
*   [Debuggen basierend auf z-index-Stapelkontext](#z-index)  
*   [Zugreifen auf die Ebenen-Toolfunktion aus der 3D-Ansicht mit zusammengesetzten Ebenen](#composited-layers)  
*   [Für etwas Ordnung im DOM-Bereich](#changing-your-view) oder im [z-index-Bereich](#change-the-scope-of-your-exploration) sorgen  
*   [Das Farbschema auswählen, um DOM-](#dom-color-type) oder [z-index-Probleme](#z-index-color-type) am besten zu debuggen.  

Wenn Sie einen frühen Prototyp des 3D-Ansichtsprojekts ausprobieren und den Code selbst ausführen möchten, wechseln Sie zum [3D-Ansichtsbeispiel][GithubMicrosoftedgeDevtoolssamples3dview].  

Auf der linken Seite gibt es drei Bereiche, die Sie für das Debuggen verwenden können.  

*   Der [z-index](#z-index)-Bereich:  Sehen Sie sich unter Berücksichtigung des z-index-Kontexts die verschiedenen Elemente in der Web-App an.  Der **z-index**-Bereich ist der Standardbereich.  
*   Der [3D DOM](#3d-dom)-Bereich:  Erkunden Sie das DOM als Ganzes einschließlich aller leicht zugänglichen Elemente.  Um auf den Bereich zuzugreifen, wählen Sie den **DOM**-Bereich neben dem **z-index**-Bereich aus.  
*   Der Bereich [zusammengesetzte Ebenen](#composited-layers):  Fügen Sie ein weiteres 3D-Element hinzu, um eine umfassendere Erfahrung im Hinblick auf die Ebenen zu schaffen.  Um auf den Bereich zuzugreifen, wählen Sie den Bereich **Zusammengesetzte Ebenen** neben dem **DOM**-Bereich aus.  
    
Auf der rechten Seite wird im Canvas Ihre Auswahl aus [z-index](#z-index), [3D DOM](#3d-dom) oder [zusammengesetzten Ebenen](#composited-layers) angezeigt.  

## <a name="navigating-the-canvas"></a>Navigieren im Canvas  

:::image type="complex" source="../media/3d-view-canvas.msft.png" alt-text="Canvas der 3D-Ansicht" lightbox="../media/3d-view-canvas.msft.png":::
   Canvas der 3D-Ansicht  
:::image-end:::  

### <a name="keyboard-shortcuts"></a>Tastenkombinationen  

*   Drehen des DOM: Verwenden Sie zum horizontalen Drehen die `left-arrow`- und `right-arrow`-Tasten.  Verwenden Sie zum senkrechten Drehen hingegen die `up-arrow`- und `down-arrow`-Tasten.  
*   Navigieren im DOM: Um durch die benachbarten Elemente zu navigieren, wählen Sie ein Element aus, und verwenden Sie dann die `up-arrow`- und `down-arrow`-Tasten.  

### <a name="mouse-controls"></a>Maussteuerung  

*   Drehen des DOM: Klicken und ziehen Sie den Canvasbereich.  
*   Schwenken des DOM: Öffnen Sie das Kontextmenü \(Rechtsklick\), und ziehen Sie in die Richtung, in die das DOM verschoben werden soll.  
*   Vergrößern/Verkleinern: Ziehen Sie mit zwei Fingern über das Touchpad, oder verwenden Sie das Bildlaufrad der Maus.  

### <a name="on-screen-controls"></a>Steuerelemente auf dem Bildschirm  

:::image type="complex" source="../media/3d-view-controls-small.msft.png" alt-text="Steuerelemente auf dem Bildschirm" lightbox="../media/3d-view-controls-small.msft.png":::
   Steuerelemente auf dem Bildschirm  
:::image-end:::  

*   Zurücksetzen der Canvas-Ansicht auf die ursprüngliche Ansicht: Wählen Sie die Schaltfläche **Kamera zurücksetzen** oder zum **Zurücksetzen von angezeigten Elementen und Neuzentrieren der Kamera** \(seitliches Aktualisierungssymbol\)  aus.  
*   Aktualisieren des Canvas \(z. B. wenn der Browser geändert wurde oder Sie zu einer Geräte-Emulatoransicht gewechselt sind\): Wählen Sie die Schaltfläche zum **erneuten Aufnehmen der Momentaufnahme** oder zum **Aufnehmen einer neuen Momentaufnahme** \(Aktualisierungssymbol\) aus.  

## <a name="z-index"></a>z-index  

:::image type="complex" source="../media/3d-view-z-index-view-box.msft.png" alt-text="z-index-Ansicht" lightbox="../media/3d-view-z-index-view-box.msft.png":::
   z-index-Ansicht  
:::image-end:::  

Im **z-index**- und im **3D DOM**-Bereich gibt es zwar gemeinsam genutzte Features, die Bereiche weisen jedoch auch jeweils verschiedene Elemente auf.  

### <a name="highlight-elements-with-stacking-context"></a>Hervorheben von Elementen mit Stapelkontext  

Über die Einstellung zum **Hervorheben von Elementen mit Stapelkontext** können Sie die z-index-Tags für die Elemente auf dem Canvas aktivieren bzw. deaktivieren.  Das Kontrollkästchen ist standardmäßig aktiviert.  

### <a name="change-the-scope-of-your-exploration"></a>Ändern des Umfangs der Untersuchung  

Über die Schaltfläche **Alle Elemente anzeigen** können Sie am schnellsten alle Elemente des DOM anzeigen, nachdem die Einstellungen darunter geändert wurden.  

Durch das Klicken auf **Nur Elemente mit Stapelkontext anzeigen** werden Elemente ohne Stapelkontext ausgeblendet und das DOM für eine einfachere Navigation vereinfacht.  

Die Schaltfläche **Ausgewähltes Element isolieren** ist im Wesentlichen drei Schaltflächen in einem.  Unterhalb der Schaltfläche **Ausgewähltes Element isolieren** gibt es zwei Kontrollkästchen: **Alle übergeordneten Elemente anzeigen** und **Nur übergeordnete Elemente mit neuem Stapelkontext beibehalten**.  

Das Kontrollkästchen **Alle übergeordneten Elemente anzeigen** ist standardmäßig aktiviert.  Um das Element und alle übergeordneten Elemente auf dem Canvas anzuzeigen, wählen Sie ein Element und dann die Schaltfläche **Ausgewähltes Element isolieren** aus.  

Um das Element und die übergeordneten Elemente mit neuem Stapelkontext auf dem Canvas anzuzeigen, aktivieren Sie die Einstellung **Nur übergeordnete Elemente mit neuem Stapelkontext beibehalten**, und klicken Sie auf die Schaltfläche **Ausgewähltes Element isolieren**.  

Um das gewünschte Element auf dem Canvas anzuzeigen, deaktivieren Sie beide Einstellungen, und klicken Sie auf die Schaltfläche **Ausgewähltes Element isolieren**.  

Suchen Sie am unteren Rand des **3D DOM**-Bereichs das Kontrollkästchen **Elemente mit der gleichen Paint-Order wie das übergeordnete ausblenden**.  Wenn Sie das Kontrollkästchen aktivieren bzw. deaktivieren, werden die Elemente entsprechend aktualisiert.  Bei Aktivierung werden Elemente mit gleicher Paint-Order auf das übergeordnete Element vereinfacht.  

Die Optionen helfen dabei, die Darstellung komplexerer Webseiten im Canvas übersichtlicher zu machen.  

### <a name="z-index-color-type"></a>z-index-Farbtyp  

Sie können verschiedene Visualisierungen für das DOM in Ihrem Canvas verwenden.  Ganz gleich, ob Sie es zum Spaß verwenden oder weil die Visualisierungen Ihnen helfen, das DOM besser darzustellen, die DevTools bieten verschiedene Farbkombinationen sowie die Option **Hintergrundfarbe verwenden**.  Sowohl der **z-index**-Bereich als auch der **3D DOM**-Bereich weisen die **Lila-zu-Weiß**-Option sowie die gleiche **Hintergrundfarbe** auf.  Ihr Feedback hat uns zu einer Reduzierung der Anzahl der Farboptionen bei dem hinzugefügten visuellen Element der z-index-Beschriftungen bewogen.  Durch die Vereinfachung wird das z-index-Debugging erleichtert.  Über die Optionsfelder können Sie die Optionen umschalten und den Farbtyp auswählen.  Der Farbtyp sollte entweder für Ihr Projekt am besten geeignet oder der von Ihnen bevorzugte sein.  

## <a name="3d-dom"></a>3D DOM  

:::image type="complex" source="../media/3d-view-dom-purple-box.msft.png" alt-text="DOM-Ansicht" lightbox="../media/3d-view-dom-purple-box.msft.png":::
   DOM-Ansicht  
:::image-end:::  

Wenn Sie an einer allgemeineren Debugansicht anstelle der z-index-Darstellung interessiert sind, bietet das **3D DOM** einen Überblick über das DOM.  Da der z-index-Kontext entfernt wird, wird das DOM genauer und übersichtlicher.  Der **3D DOM**-Bereich weist ähnliche Funktionen auf, es gibt jedoch einige Unterschiede.  

### <a name="changing-your-view"></a>Ändern der Ansicht  

Im **3D DOM**-Bereich gibt es bei der Schaltfläche **Ausgewähltes Element isolieren** die Kontrollkästchen **Untergeordnete Elemente einschließen** und **Übergeordnete Elemente einschließen**.  Beide Kontrollkästchen sind standardmäßig aktiviert.  Das bedeutet, dass wenn Sie nach dem Auswählen eines Elements auf die Schaltfläche **Ausgewähltes Element isolieren** klicken, im Canvas das ausgewählte Element sowie dessen über- und untergeordneten Elemente angezeigt werden.  Deaktivieren Sie die Einstellung **Untergeordnete Elemente einschließen**, und klicken Sie erneut auf die Schaltfläche **Ausgewähltes Element isolieren**, um das ausgewählte Element und dessen übergeordnete Elemente anzuzeigen.  Wenn Sie die Einstellung **Untergeordnete Elemente einschließen** aktivieren und **Übergeordnete Elemente einschließen** deaktivieren, und anschließend auf die Schaltfläche **Ausgewähltes Element isolieren** klicken, werden im Canvas das ausgewählte Element sowie alle untergeordneten Elemente angezeigt.  Wenn Sie beide Einstellungen deaktivieren und auf die Schaltfläche **Ausgewähltes Element isolieren** klicken, wird im Canvas nur das zuvor ausgewählte Element angezeigt.  

Ein Schieberegler im Kontrollbereich mit der Bezeichnung **Nesting level for page** (Schachtelungstiefe für die Seite) mit einer Zahl daneben.  Die Zahl gibt die Anzahl der Ebenen für das Dokument an.  Wenn Sie den Schieberegler nach links ziehen, werden die äußersten Ebenen weggelassen, bis nur eine auf `1` festgelegte Schachtelungsebene zurückbleibt, bei der nur das Element ganz hinten im DOM angezeigt wird.  Verwenden Sie den Schieberegler, um die Unübersichtlichkeit zu reduzieren.  Dadurch können Sie sich genauer ansehen, was in den unteren Ebenen los ist.  

### <a name="dom-color-type"></a>DOM-Farbtyp  

Im **3D DOM**-Bereich werden die nachstehend aufgeführten Optionen angezeigt.  

*   Drei verschiedene Farbkombinationen:  
    *   **Heatmap: Lila bis Weiß**  
    *   **Heatmap: Blau bis Gelb**  
    *   **Heatmap: Regenbogen**  
*   **Hintergrundfarbe verwenden**  
*   **Bildschirmtextur verwenden**  
    
Durch die Option **Bildschirmtextur verwenden** wird Kontext zu Ihrer Debugumgebung hinzugefügt.  Der Inhalt der Webseite wird direkt auf den Elementen angezeigt.  

## <a name="composited-layers"></a>Zusammengesetzte Ebenen

:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Bereich Zusammengesetzte Ebenen" lightbox="../media/experiments-layers.msft.png":::
   Der Bereich **Zusammengesetzte Ebenen**
:::image-end:::  

Im Bereich **Zusammengesetzte Ebenen** werden die Elemente des **Ebenentools** geöffnet, ohne den Kontext zu ändern.  Sie können weiterhin auf die Details der einzelnen Ebenen zugreifen und verfügen über **Slow scroll rects** und **Paint**.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

Das Microsoft Edge DevTools-Team arbeitet weiter an der Benutzeroberfläche und fügt basierend auf Ihrem Feedback weitere Funktionen zur 3D-Ansicht hinzu.  Senden Sie uns Ihr Feedback, damit wir die Microsoft Edge DevTools verbessern können.  Klicken Sie in den DevTools auf das Symbol zum **Feedback senden**, oder drücken Sie `Alt` + `Shift` + `I` unter Windows/Linux bzw. `Option` + `Shift` + `I` unter macOS, und geben Sie dann Feedback oder Featurewünsche zu den DevTools ein.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Microsoft Edge DevTools 3D-Ansicht – MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Dokumentobjektmodell (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
