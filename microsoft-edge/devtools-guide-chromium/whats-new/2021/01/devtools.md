---
description: Das Neuigkeiten-Tool ist jetzt Willkommen, visueller Schriftarten-Editor im Bereich „Formatvorlagen“, CSS Flexbox-Debugtools und vieles mehr.
title: Neuigkeiten in DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.localizationpriority: high
ms.openlocfilehash: 9eb9f35427829dbe262b4c71d8ff5474b28eae77
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597157"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-89"></a>Neuigkeiten in DevTools (Microsoft Edge 89)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="whats-new-is-now-welcome"></a>Neuigkeiten ist jetzt Willkommen  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Das **Neuigkeiten**-Tool in den Microsoft Edge DevTools hat jetzt ein neues Erscheinungsbild und einen neuen Name:  **Willkommen**.  Das **Willkommen**-Tool zeigt weiterhin die neuesten DevTools-Neuigkeiten und -Updates an.  Es enthält jetzt auch Links zur Microsoft Edge DevTools-Dokumentation, Möglichkeiten zum Senden von Feedback und vieles mehr.  Wenn Sie das **Willkommen**-Tool nach jedem Update für Microsoft Edge anzeigen möchten, aktivieren Sie das Kontrollkästchen neben **Registerkarte nach jedem Update öffnen** unter dem Titel.  Um das **Willkommen**-Tool zu schließen, wählen Sie das **X** auf der rechten Seite des Registerkartentitels aus.  Wenn Sie das ursprüngliche **Neuigkeiten**-Tool bevorzugen, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings] > **Experimente**, und entfernen Sie das Kontrollkästchen neben **Registerkarte „Willkommen“ aktivieren**.  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="Das Willkommen-Tool wird hervorgehoben" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   Das **Willkommen**-Tool wird hervorgehoben  
:::image-end:::  

## <a name="visual-font-editor-in-the-styles-pane"></a>Visueller Schriftarten-Editor im Bereich „Formatvorlagen“  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Wenn Sie mit Schriftarten in CSS arbeiten, verwenden Sie den neuen visuellen [Schriftarten-Editor][DevtoolsInspectStylesEditFonts].  Sie können Fallbackschriftarten definieren und Schieberegler verwenden, um Schriftbreite, Schriftgröße, Zeilenhöhe und Abstand zu definieren.  Der **Schriftarten-Editor** hilft Ihnen beim Ausführen der folgenden Aktionen.  

*   Wechseln zwischen Einheiten für unterschiedliche Schriftarteigenschaften  
*   Wechseln zwischen Schlüsselwörtern für unterschiedliche Schriftarteigenschaften  
*   Konvertieren von Einheiten  
*   Generieren von genauem CSS-Code  
    
Um dieses Experiment zu aktivieren, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings] > **Experimente**, und wählen Sie das Kontrollkästchen neben **Neue Schriftarten-Editor-Tools im Bereich „Formatvorlagen“ aktivieren** aus.  Weitere Informationen finden Sie unter [Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich „Formatvorlagen“ in DevTools][DevtoolsInspectStylesEditFonts].  Navigieren Sie zu Problem [1093229][CR1093229], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="Der visuelle Schriftarten-Editor wird im Bereich „Formatvorlagen“ hervorgehoben." lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   Der visuelle **Schriftarten-Editor** wird im Bereich **Formatvorlagen** hervorgehoben.  
:::image-end:::  

## <a name="css-flexbox-debugging-tools"></a>CSS Flexbox-Debugtools  

Die Flexbox-Debugfeatures befinden sich in der aktiven Entwicklung.  Um das Experiment für die folgenden beiden Features zu aktivieren, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings] > **Experimente**, und wählen Sie das Kontrollkästchen neben **Neue CSS Flexbox-Debugfeatures aktivieren** aus.  Navigieren Sie zu Problem [1136394][CR1136394] und [1139949][CR1139949], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

### <a name="new-flexbox-flex-icon-helps-identify-and-display-flex-containers"></a>Neues Flexbox(Flex)-Symbol hilft beim Identifizieren und Anzeigen von Flexcontainern  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Im **Element**-Tool hilft Ihnen das neue Flexbox(Flex)-Symbol, Flexbox-Container in Ihrem Code zu identifizieren.  Wählen Sie das Flexbox \(Flex\)-Symbol aus, um den Überlagerungseffekt zu aktivieren oder zu deaktivieren, der einen Flexbox-Container umreißt.  Sie können die Farbe der Überlagerung im Bereich **Layout** anpassen, der sich neben **Formatvorlagen** und **Berechnet** befindet.  

:::row:::
   :::column span="":::
      Zum Aktivieren und Deaktivieren des Überlagerungseffekts, der den Flexbox-Container umreißt, wählen Sie das Symbol Flexbox \(`flex`\) aus.  
   :::column-end:::
   :::column span="":::
      Sie können die Farbe der Überlagerung im Bereich **Layout** neben **Formatvorlagen** und **Berechnet** anpassen.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Das Flexbox (Flex)-Symbol und die hervorgehobene Webseite" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         Das **Flexbox** \(`flex`\)-Symbol und die hervorgehobene Webseite :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Die im Bereich „Layout“ hervorgehobenen Flexbox-Überlagerungen" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         Die im Bereich **Layout** hervorgehobenen **Flexbox-Überlagerungen**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-alignment-icons-and-visual-guides-when-flexbox-layouts-change-using-css-properties"></a>Anzeigen von Ausrichtungssymbolen und visuellen Führungslinien, wenn das Layout von Flexboxlayouts mithilfe von CSS-Eigenschaften geändert wird  

<!--  Title: Display alignment icons and visual guides for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Wenn Sie CSS für Ihr Flexbox-Layout bearbeiten, werden bei automatischen CSS-Vervollständigungen im Bereich **Formatvorlagen** nun hilfreiche Symbole neben relevanten Flexbox-Eigenschaften angezeigt.  Öffnen Sie zum Testen dieses neuen Features das Tool ** Elemente**, und wählen Sie einen Flexcontainer aus.  Fügen Sie dann eine Eigenschaft für den Container im Bereich **Formatvorlagen** hinzu oder ändern Sie sie.  

:::row:::
   :::column span="":::
      Im Menü „AutoVervollständigung“ werden jetzt Symbole angezeigt, die die Auswirkung von Ausrichtungseigenschaften wie `align-content` und `align-items` angeben.  
   :::column-end:::
   :::column span="":::
      Darüber hinaus zeigt DevTools jetzt eine Leitlinie an, um die CSS-Eigenschaft `align-items` besser zu überprüfen.  Die CSS-Eigenschaft `gap` wird ebenfalls unterstützt.  In der folgenden Abbildung wird die CSS-Eigenschaft `gap` auf `gap: 12px;` festgelegt, und das Schraffurmuster für jede Lücke wird angezeigt.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Das Menü AutoVervollständigung wird für CSS-Eigenschaften hervorgehoben, die mit ausrichten- beginnen" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Das Menü "AutoVervollständigung" wird für CSS-Eigenschaften hervorgehoben, die beginnen mit `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Flexboxlücke in CSS-Eigenschaften und Webseite hervorgehoben" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` in CSS-Eigenschaften und Webseite hervorgehoben  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="add-tools-quickly-with-new-more-tools-button"></a>Schnelles Hinzufügen von Tools mit der neuen Schaltfläche "Weitere Tools"  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Sie haben nun eine neue Möglichkeit, weitere Tools in den Microsoft Edge DevTools zu öffnen.  Nachdem Sie dieses Experiment aktivieren, wird das Symbol **Weitere Tools** rechts neben dem Hauptbereich als Pluszeichen (`+`) angezeigt.  Wenn Sie eine Liste anderer Tools anzeigen möchten, die dem Hauptbereich hinzugefügt werden, wählen Sie das Symbol **Weitere Tools** \(`+`\) aus.  Um dieses Experiment zu aktivieren, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings] > **Experimente**, und wählen Sie dann das Kontrollkästchen neben **Registerkartenmenüs „Schaltfläche „+“ aktivieren“ aus, um weitere Tools zu öffnen**.  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Weitere Tools in DevTools hervorgehoben" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Weitere Tools** in DevTools hervorgehoben  
:::image-end:::  

## <a name="assistive-technologies-now-announce-position-and-count-of-css-suggestions"></a>Hilfstechnologien kündigen jetzt Position und Anzahl von CSS-Vorschlägen an  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

Wenn Sie CSS bearbeiten, erhalten Sie eine Dropdownliste mit Features.  Dieses Feature war für Benutzer von Hilfstechnologien nicht verfügbar, da es in Microsoft Edge (Version 89) angekündigt ist.  Ein Benutzer von Hilfstechnologien kann nun im Bereich **Formatvorlagen** durch CSS-Vorschläge navigieren.  In Microsoft Edge (Version 88) und früher kündigte die Hilfstechnologie `Suggestion` an, wenn ein Benutzer durch die Liste der Vorschläge navigierte, wenn er CSS im Bereich **Formatvorlagen** bearbeitete.  In Microsoft Edge (Version 89) hört ein Benutzer der Hilfstechnologie jetzt die Position und Anzahl des aktuellen Vorschlags.  Jeder Vorschlag wird angekündigt, wenn der Benutzer durch die Liste der Vorschläge navigiert, z. B. Vorschlag 3 von 5.  Weitere Informationen zum Schreiben von CSS in DevTools finden Sie unter [CSS ändern][DevtoolsCssReferenceChangeCss].  Navigieren Sie zu Problem [1157329][CR1157329], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

Um ein Video anzuzeigen, das mehrere Vorschläge anzeigt und laut vorlesen kann, wenn dieses Experiment aktiviert ist, navigieren Sie zu [Voiceover kündigt DevTools-Optionen an](https://youtu.be/9TcUpleEwwA) auf YouTube.  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Der im Bereich „Formatvorlagen“ hervorgehobene Vorschlag" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   Die im Bereich **Formatvorlagen** hervorgehobene `suggestion`-Liste  
:::image-end:::  

## <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Emulieren von Surface Duo und Samsung Galaxy Fold  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Testen Sie die Darstellung Ihrer Website oder App auf den folgenden Geräten in Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Samsung Galaxy Fold][SamsungUsMobileGalaxyFold]  
    
Aktivieren Sie die **Features der experimentellen Webplattform**, um auf das neue [Feature „CSS-Medienbildschirmbereich“][DualScreenWebCssMediaSpanning] und die [API „getWindowSegments JavaScript“][DualScreenWebJavascriptGetwindowsegments] zuzugreifen.  Navigieren Sie zu `edge://flags` und umschalten Sie das Kennzeichen neben **Features der experimentellen Webplattform**.  Um Ihre Website oder App für die Geräte mit dualem Bildschirm oder für die faltbare Geräte zu verbessern, verwenden Sie die folgenden Features bei der [Emulation des Geräts][DevtoolsDeviceModeIndex].  

*   [Aufteilung][DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices], das ist, wenn Ihre Website \(oder App\) auf beiden Bildschirmen angezeigt wird.  
*   [Rendering der Naht][DualScreenIntroductionHowToWorkWithSeam], das ist der Abstand zwischen den beiden Bildschirmen.  
    
Navigieren Sie zu Problem [1054281][CR1054281], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emulieren des dualen Bildschirms" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Emulieren des dualen Bildschirms  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-112"></a>Microsoft Edge Developer Tools für Visual Studio Code Version 1.1.2  

Die Erweiterung [Microsoft Edge Developer Tools für Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] (Version 1.1.2) für Microsoft Visual Studio Code hat die folgenden Änderungen seit der vorherigen Version.  Microsoft Visual Studio Code aktualisiert Erweiterungen automatisch.  Navigieren Sie zum manuellen Aktualisieren auf Version 1.1.2 zu [Erweiterung manuell aktualisieren][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].  

*   Jedem Element in der Zielliste wurde eine Schaltfläche **Instanz schließen** hinzugefügt \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Die Version der [Microsoft Edge DevTools][DevtoolsIndex] wurde von 84.0.522.63 auf [85.0.564.40][DevtoolsWhatsNew85] aktualisiert \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   Enthaltener [Debugger für Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] als Abhängigkeit \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Implementierte Einstellungsoption zum Ändern von Erweiterungsthemen \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
Sie können Probleme melden und zur Erweiterung im [vscode-edge-devtools GitHub-Repository][GithubMicrosoftVscodeEdgeDevtools] mitwirken.  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="capture-node-screenshot-beyond-viewport"></a>Screenshot von Knoten außerhalb des Ansichtsfensters erfassen  

In Microsoft Edge (Version 89) sind Screenshots von Knoten genauer und erfassen den vollständigen Knoten, auch wenn der Inhalt des Knotens im Ansichtsfenster nicht sichtbar ist.  Zeigen Sie im Tool **Elemente** auf ein Element, öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\), und wählen Sie **Screenshot des Knotens erfassen** aus.  Navigieren Sie zu Problem [1003629][CR1003629], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Screenshot des Knotens erfassen, der im Kontextmenü des Tools „Elemente“ hervorgehoben ist" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Screenshot des Knotens erfassen**, der im Kontextmenü des Tools **Elemente** hervorgehoben ist  
:::image-end:::  

### <a name="elements-tool-updates"></a>Aktualisierungen des Tools „Elemente“  

#### <a name="support-forcing-the-target-css-state"></a>Unterstützung zum Erzwingen des CSS-Zustands :target  

Sie können DevTools nun verwenden, um die CSS-Pseudoklasse [:target][MdnDocsWebCssTarget] zu erzwingen.  Die Pseudoklasse `:target` wird ausgelöst, wenn ein eindeutiges Element \(das Zielelement\) über ein `id` verfügt, das einem Fragment der URL entspricht.  Beispielsweise löst die `http://www.example.com/index.html#section1`-URL die Pseudoklasse `:target` für ein HTML-Element mit `id="section1"` aus.  Um eine Demo mit hervorgehobener Abschnitt 1 zu testen, navigieren Sie zu [CSS :target Demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].  Navigieren Sie zu Problem [1156628][CR1156628], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Die Webseite ohne erzwungene CSS hervorgehoben" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Webseite ohne erzwungene CSS hervorgehoben  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS erzwungen und Webseite hervorgehoben" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` CSS erzwungen und Webseite hervorgehoben  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <a name="use-duplicate-elements-to-copy-elements"></a>Verwenden Sie „Elemente duplizieren“, um Elemente zu kopieren  

Verwenden Sie die neue Tastenkombination **Element duplizieren**, um ein Element zu klonen.  Zeigen Sie im Tool **Elemente** auf ein Element, öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\), wählen Sie **Element duplizieren** aus.  Unter dem ausgewählten Element wird ein neues Element erstellt.  Um das Element mit einer Tastenkombination zu duplizieren, wählen Sie `Shift`+`Alt`+`Down Arrow` \(Windows/Linux\) oder `Shift`+`Option`+`Down Arrow` \(macOS\) aus.  Navigieren Sie zu Problem [1150797][CR1150797], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="Die Option „Element duplizieren“ wird im Kontextmenü eines Elements im Tool „Elemente“ hervorgehoben" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   Die Option **Element duplizieren** wird im Kontextmenü eines Elements im Tool **Elemente** hervorgehoben  
:::image-end:::  

#### <a name="color-pickers-for-custom-css-properties"></a>Farbwähler für benutzerdefinierte CSS-Eigenschaften  

Im Bereich **Formatvorlagen** werden nun Farbwähler für benutzerdefinierte CSS-Eigenschaften angezeigt.  Zum Durchschleifen der RGBA-, HSLA- und Hex-Formate des Farbwerts halten Sie `Shift` gedrückt und wählen Sie den Farbwähler aus.  Navigieren Sie zu Problem [1147016][CR1147016], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Farbwähler für benutzerdefinierte CSS-Eigenschaften" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   Farbwähler für benutzerdefinierte CSS-Eigenschaften  
:::image-end:::  

#### <a name="copy-css-classes-and-properties"></a>Kopieren von CSS-Klassen und -Eigenschaften  

Sie können jetzt die CSS-Eigenschaften mit einigen neuen Optionen im Kontextmenü schneller kopieren.  Wählen Sie im Tool **Elemente** ein Element aus.  Wenn Sie den Wert kopieren möchten, zeigen Sie im Bereich **Formatvorlagen** auf eine CSS-Klasse oder eine CSS-Eigenschaft, öffnen Sie ein Kontextmenü \(mit der rechten Maustaste klicken\), und wählen Sie die Kopieroption aus.  

:::row:::
   :::column span="":::
      Kopieroptionen für eine CSS-Klasse.  
      
      | Option | Details |  
      |:--- |:--- |  
      | **Selektor kopieren** | Kopieren Sie den A=aktuellen Selektornamen. |  
      | **Regel kopieren** | Kopieren Sie die Regel des aktuellen Selektors. |  
      | **Alle Deklarationen kopieren** | Kopieren Sie alle Deklarationen unter der aktuellen Regel, einschließlich nicht gültiger und Präfixeigenschaften. |  
   :::column-end:::
   :::column span="":::
      Kopieroptionen für eine CSS-Eigenschaft.  
      
      | Option | Details |      
      |:--- |:--- |  
      | **Deklaration kopieren** | Kopieren Sie die Deklaration der aktuellen Zeile. |  
      | **Eigenschaft kopieren** | Kopieren Sie die Eigenschaft der aktuellen Zeile. |  
      | **Wert kopieren** | Kopieren Sie den Wert der aktuellen Zeile. |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Kopieroptionen für eine CSS-Klasse im Kontextmenü" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         Kopieroptionen für eine CSS-Klasse im Kontextmenü  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Kopieroptionen für eine CSS-Eigenschaft im Kontextmenü" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         Kopieroptionen für eine CSS-Eigenschaft im Kontextmenü  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Navigieren Sie zu Problem [1152391][CR1152391], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

### <a name="cookies-updates"></a>Updates für Cookies  

#### <a name="new-option-to-display-url-decoded-cookies"></a>Neue Option zum Anzeigen von URL-decodierten Cookies  

Sie können jetzt entscheiden, den URL-decodierten Cookiewert im Bereich **Cookies** anzuzeigen.  Navigieren Sie zum Anzeigen des decodierten Cookies zum Bereich **Anwendung** > **Cookies**, wählen Sie ein beliebiges Cookie in der Liste aus, und aktivieren Sie das Kontrollkästchen neben **Decodierte URL anzeigen**.  Navigieren Sie zu Problem [997625][CR997625], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Option zum Anzeigen von URL-decodierten Cookies" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Option zum Anzeigen von URL-decodierten Cookies  
:::image-end:::  

#### <a name="filter-and-clear-visible-cookies"></a>Filtern und Löschen sichtbarer Cookies  

In Microsoft Edge (Version 88) oder früher, bot das Tool **Anwendung** nur eine Möglichkeit, alle Cookies mit der Schaltfläche **Alle Cookies löschen** zu löschen.  In Microsoft Edge (Version 89) können Sie nun **Gefilterte Cookies löschen** auswählen, um nur die gefilterten Cookies zu löschen.  Navigieren Sie zum Filtern von Cookies zu **Anwendung** > **Cookies**, und geben Sie in das Textfeld **Filter** ein.  Um die angezeigten Cookies zu löschen, wählen Sie die Schaltfläche **Gefilterte Cookies löschen** aus.  Wenn Sie alle anderen Cookies anzeigen möchten, löschen Sie den Filtertext.  Navigieren Sie zu Problem [978059][CR978059], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Nur sichtbare Cookies löschen" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Nur sichtbare Cookies löschen  
:::image-end:::  

#### <a name="new-option-to-clear-third-party-cookies-in-the-storage-pane"></a>Neue Option zum Löschen von Drittanbietercookies im Bereich „Speicher“  

DevTools löschen jetzt standardmäßig nur Erstanbietercookies.  Navigieren Sie zum Löschen von Websitedaten und Erstanbietercookies zu **Anwendung** > **Speicher**, und wählen Sie dann **Websitedaten löschen** aus.  

Um Websitedaten und alle Cookies zu löschen, navigieren Sie zu **Anwendung** > **Speicher**.  Aktivieren Sie das Kontrollkästchen neben **Drittanbietercookies einschließen**, und wählen Sie dann **Websitedaten löschen** aus.  

Navigieren Sie zu Problem [1012337][CR1012337], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Option zum Löschen von Drittanbietercookies" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Option zum Löschen von Drittanbietercookies  
:::image-end:::  

### <a name="network-tool-updates"></a>Aktualisierungen des Tools „Netzwerk“  

#### <a name="persist-record-network-log-setting"></a>Einstellung „Netzwerkprotokoll aufzeichnen“ beibehalten  

In Microsoft Edge (Version 88) oder früher, setzt DevTools die Einstellung **Netzwerkprotokoll aufzeichnen** bei Aktualisierung einer Webseite zurück.  In Microsoft Edge (Version 89) behält DevTools nun die Einstellung **Netzwerkprotokoll aufzeichnen** bei.  Navigieren Sie zu Problem [1122580][CR1122580], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Netzwerkprotokoll aufzeichnen" lightbox="../../media/2021/01/network-log.msft.png":::
   Netzwerkprotokoll aufzeichnen  
:::image-end:::  

#### <a name="online-option-is-now-no-throttling-option"></a>Die Option „Online“ wird zur Option „Keine Einschränkung“  

Die Netzwerkemulationsoption **Online** wird jetzt in **Keine Einschränkung** umbennant.  Navigieren Sie zu Problem [1028078][CR1028078], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Keine Einschränkungsoption" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   **Keine Einschränkungsoption**  
:::image-end:::  

### <a name="new-copy-options-in-the-console-tool-sources-tool-and-styles-pane"></a>Neue Kopieroptionen im Tool „Konsole“, „Quellen“ und im Bereich „Formatvorlagen“

#### <a name="copy-object-in-the-console-and-sources-tool"></a>Kopieren des Objekts im Tool „Konsole“ und „Quellen“  

Sie können nun Objektwerte in die Tools **Konsole** und **Quellen** kopieren.  Die Möglichkeit, Objektwerte zu kopieren, ist bei der Arbeit mit großen Objekten hilfreich.  Navigieren Sie zu Problem [1148353][CR1148353] und [1149859][CR1149859], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::row:::
   :::column span="":::
      Zeigen Sie im Tool **Konsole** auf ein Objekt, öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\), und wählen Sie dann **Objekt kopieren** aus.  
   :::column-end:::
   :::column span="":::
      Zeigen Sie im Tool **Quellen** auf einem Haltepunkt auf ein Objekt, markieren Sie im Popupfenster **Objekt** ein Objekt, öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\), und wählen Sie dann **Objekt kopieren** aus.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Objekt in der Konsole kopieren" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         Objekt in der **Konsole** kopieren  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Objekt in Quellen kopieren" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         Objekt in **Quellen** kopieren  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="copy-file-name-in-the-sources-tool-and-styles-pane"></a>Kopieren des Dateinamens im Tool „Quellen“ und im Bereich „Formatvorlagen“  

Sie können nun einen Dateinamen mithilfe des Kontextmenüs kopieren.  Navigieren Sie zu Problem [1155120][CR1155120], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::row:::
   :::column span="":::
      Zeigen Sie im Tool **Quellen** auf einen Dateinamen, öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\), und wählen Sie dann **Dateinamen kopieren** aus.  
   :::column-end:::
   :::column span="":::
      Zeigen Sie im Tool **Elemente** > Bereich **Formatvorlagen** auf einen Dateinamen, öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\), und wählen Sie dann **Dateinamen kopieren** aus.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Dateiname in Quellen kopieren" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Dateiname in **Quellen** kopieren  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Dateiname im Bereich Formatvorlagen kopieren" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Dateiname im Bereich **Formatvorlagen** kopieren  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="updates-to-frame-details"></a>Aktualisierungen für Frame-Details  

#### <a name="service-workers-information-in-frame-details"></a>Service Workers-Informationen in Frame-Details  

DevTools listet nun einen dedizierten Service Worker unter dem übergeordneten Frame auf.  In der folgenden Abbildung werden die Details der Service Worker angezeigt.  Um die Details der Service Worker anzuzeigen, navigieren Sie zu **Anwendung** > **Frames** > `top` > **Service Workers**, und wählen Sie dann einen Service Worker aus.  Navigieren Sie zu Problem [1122507][CR1122507], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Service Workers-Informationen in den Frames-Details" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   **Service Workers**-Informationen in den **Frames**-Details  
:::image-end:::  

#### <a name="measure-memory-information-in-frame-details"></a>Messen von Speicherinformationen in Frame-Details  

Der API-Status „`performance.measureMemory()`“ wird nun im Abschnitt **API-Verfügbarkeit** angezeigt.  Die neue API „`performance.measureMemory()`“ schätzt die Speicherauslastung der gesamten Webseite.  Navigieren Sie zu Problem [1139899][CR1139899], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Arbeitsspeicher messen" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Arbeitsspeicher messen  
:::image-end:::  

### <a name="dropped-frames-in-the-performance-tool"></a>Verworfene Frames im Tool "Leistung"  

Wenn Sie [die Lastleistung im Tool "Leistung" analysieren][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], markiert der Abschnitt **Frames** verworfene Frames nun als rot.  Zeigen Sie zum Anzeigen der Bildfrequenz auf einen verworfenen Frame.  Navigieren Sie zu Problem [1075865][CR1075865], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Verworfene Frames" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Verworfene Frames  
:::image-end:::  

#### <a name="new-color-contrast-calculation---advanced-perceptual-contrast-algorithm-apca"></a>Neue Farbkontrastberechnung – Advanced Perceptual Contrast Algorithm (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Der [Advanced Perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] ersetzt das [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced]-Richtlinienkontrastverhältnis im [Farbwähler][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].  APCA ist eine neue Methode zum Berechnen des Kontrasts.  Sie basiert auf modernen Forschungen zur Farbwahrnehmung.  Im Vergleich zu AA/AAA-Richtlinien ist APCA kontextabhängiger.  Der Kontrast wird basierend auf den folgenden räumlichen Eigenschaften des Texts, der Farbe und des Kontexts berechnet.  

*   Räumliche Eigenschaften von Text, die Schriftbreite und Schriftgröße enthalten.  
*   Räumliche Eigenschaften der Farbe, die wahrgenommenen Kontrast zwischen Text und Hintergrund enthalten.  
*   Räumliche Eigenschaften des Kontexts, die Umgebungslicht, Umgebung und beabsichtigten Zweck enthalten.  
    
Um dieses Experiment zu aktivieren, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings] > **Experimente**, und aktivieren Sie das Kontrollkästchen neben **Aktivieren des neuen Advanced Perceptual Contrast Algorithm (APCA), der das vorherige Kontrastverhältnis und AA/AAA-Richtlinien** ersetzt.  Navigieren Sie zu Problem [1121900][CR1121900], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA im Farbwähler" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA im Farbwähler  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Neuigkeiten in DevTools (Microsoft Edge 85) | Microsoft-Dokumentation"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: ../../../accessibility/color-picker.md "Testen des Kontrasts von Text und Farbe mithilfe der Farbauswahl | Microsoft-Dokumentation"  
[DevtoolsCssReferenceChangeCss]: ../../../css/reference.md#change-css "Ändern von CSS – CSS-Referenz | Microsoft-Dokumentation"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices]: ../../../device-mode/dual-screen-and-foldables.md#test-on-foldable-and-dual-screen-devices "Auf zusammenklappbaren und dualen Bildschirmgeräten testen – Emulieren Sie Geräte mit dualem Bildschirm und faltbaren Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simulieren eines mobilen Ansichtsfensters – Emulieren mobiler Geräte in Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: ../../../evaluate-performance/reference.md#record-load-performance "Datensatzlastleistung – Leistungsanalysereferenz | Microsoft Docs"  
[DevtoolsIndex]: ../../../index.md "Microsoft Edge (Chromium) Entwickler Tools Übersicht | Microsoft-Dokumentation"  
[DevtoolsInspectStylesEditFonts]: ../../../inspect-styles/edit-fonts.md "Bearbeiten von CSS-Schriftstile und -Einstellungen im Bereich „Formatvorlagen“ in DevTools | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Arbeiten mit der Naht – Einführung in Geräten mit dualem Bildschirm | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Feature „CSS-Medienbildschirmaufteilung“ für die Erkennung von dualem Bildschirm | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "Die API „getWindowSegments JavaScript“ für Geräte mit dualem Bildschirm | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Abschnitt 1 – CSS :target Demo für Neuigkeiten in DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementieren des Dropdowns in Einstellungen zum Ändern von Designs | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: Einschließlich Debugger für Microsoft Edge als Abhängigkeitsmodus | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Upgrade der Edge DevTools-Version auf 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Hinzufügen einzelner Schließen-Schaltflächen zum Instanzenbereich | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Wählen Sie Schriftartmerkmale und Hintergrundfarben aus, um genügend Kontrast für die Lesbarkeit zu bieten | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Vertrauenswürdige Typen | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Neue Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  
[CR978059]: https://crbug.com/978059 "Problem 978059: Löschen von Cookies beim Filtern, alle Cookies löschen, nicht nur die gefilterten | Chromium-Fehler"  
[CR997625]: https://crbug.com/997625 "Problem 997625: Neue Featureanforderung | Option zum Anzeigen des URL-decodierten Werts in Cookies | Chromium-Fehler"  
[CR1003629]: https://crbug.com/1003629 "Problem 1003629: „Knoten erfassen“ macht keinen Screenshot des Knotens unterhalb der Faltung mehr. | Chromium-Fehler"  
[CR1012337]: https://crbug.com/1012337 "Problem 1012337: „Websitedaten löschen“ unterbricht die Google-Sitzung auf Nicht-Google-Seiten | Chromium-Fehler"  
[CR1028078]: https://crbug.com/1028078 "Problem 1028078: Setzen Sie Online und Offline nebeneinander in die Liste | Chromium-Fehler"  
[CR1054281]: https://crbug.com/1054281 "Problem 1054281: Featureanforderung: DevTools sollte faltbare Geräte und Geräte mit dualem Bildschirm emulieren | Chromium-Fehler"  
[CR1075865]: https://crbug.com/1075865 "Problem 1075865: Verworfene Frames in der DevTools-Chronik anzeigen | Chromium-Fehler"  
[CR1093229]: https://crbug.com/1093229 "Problem 1093229: DevTools: bietet eine spezielle Schriftart-Editor-Oberfläche | Chromium-Fehler"  
[CR1121900]: https://crbug.com/1121900 "Problem 1121900: DevTools: Kontrastberechnungslogik gemäß neuer Spezifikation aktualisieren | Chromium-Fehler"  
[CR1122507]: https://crbug.com/1122507 "Problem 1122507: Anzeigen von Worker-Informationen in der Framestrukturansicht | Chromium-Fehler"  
[CR1122580]: https://crbug.com/1122580 "Problem 1122580: Deaktivieren der Netzwerkaufzeichnung beim Neuladen nicht möglich | Chromium-Fehler"  
[CR1136394]: https://crbug.com/1136394 "Problem 1136394: Flexbox-Tooling | Chromium-Fehler"  
[CR1139899]: https://crbug.com/1139899 "Problem 1139899: Verfügbarkeit der Gated-API in der Frame-Detailansicht melden | Chromium-Fehler"  
[CR1139949]: https://crbug.com/1139949 "Problem 1139949: Flexbox-Ablageordner | Chromium-Fehler"  
[CR1147016]: https://crbug.com/1147016 "Problem 1147016: Der Farbwähler wird in der var()-Funktion nicht angezeigt. | Chromium-Fehler"  
[CR1148353]: https://crbug.com/1148353 "Problem 1148353: Featureanforderung: Objekt aus der DevTools-Konsole kopieren | Chromium-Fehler"  
[CR1149859]: https://crbug.com/1149859 "Problem 1149859: [Featureanforderung][Konsole] Hinzufügen des Elements „Objekt in der Zwischenablage zum Kontextmenü kopieren“ | Chromium-Fehler"  
[CR1150797]: https://crbug.com/1150797 "Problem 1150797: Hinzufügen des Kontextmenüs „Element duplizieren“ im Bereich „Element“ | Chromium-Fehler"  
[CR1152391]: https://crbug.com/1152391 "Problem 1152391: Support für &quot;CSS-Kontextmenü im Bereich &quot;Formatvorlagen&quot; kopieren&quot; | Chromium-Fehler"  
[CR1155120]: https://crbug.com/1155120 "Problem 1155120: [FR]Support für „Dateiname und Zeilennummer kopieren“ | Chromium-Fehler"  
[CR1156628]: https://crbug.com/1156628 "Problem 1156628: DevTools: Support für das Feature &quot;:target im erzwungenem Elementzustand&quot; hinzufügen | Chromium-Fehler"  
[CR1157329]: https://crbug.com/1157329 "Problem 1157329: Barrierefreiheit – Sprachausgabe: Die Sprachausgabe kündigt nicht die Anzahl und Position für Vorschläge an, die für Code auf der Registerkarte „Formatvorlagen“ verfügbar sind | Chromium-Fehler"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Kontrast (Erweitert) – So erfüllen Sie WCAG (Kurzübersicht) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Kontrast (Minimum) – So erfüllen Sie WCAG (Kurzübersicht) | W3C"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-89) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen

[SpanningPlaceholder]: link-t-b-d "Übergreifender Platzhalter"  
