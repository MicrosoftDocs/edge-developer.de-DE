---
description: Die neuesten experimentellen Features in Microsoft Edge DevTools
title: Experimentelle Features
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, Devtools, Experimentieren
no-loc:
- Enable webhint
- Enable Network Console
- Source Order Viewer
- Enable Composited Layers in 3D View
- Enable new Font Editor tool within the Styles pane
- Enable new CSS Flexbox debugging features
- Enable + button tab menus to open more tools
- Enable Welcome tab
- 3D View
- Turn on support to move tabs between panels
- Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code
- Edit keyboard shortcuts for any action in the DevTools
- Turn on new CSS grid debugging features
- 'Emulation: Support dual screen mode'
ms.openlocfilehash: dec4b4d111c0eb8dc9cc3963bac7339df1d9b6f6
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624752"
---
# <a name="experimental-features"></a>Experimentelle Features  

Microsoft Edge DevTools bieten Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.  Sie können testen und [Feedback geben,](#providing-feedback-on-experimental-features) bevor jedes Feature veröffentlicht wird.  

Obwohl experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features mithilfe der Microsoft Edge Canary Channel.  

## <a name="turn-on-experimental-features"></a>Aktivieren experimenteller Features  

Führen Sie die folgenden Schritte aus, um experimentelle Features in Microsoft Edge zu aktivieren( oder zu deaktivieren).  

1.  [Öffnen Sie DevTools][DevtoolsOpenIndex].  
    *   Wählen Sie `Control` + `Shift` + `I` \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\) aus.  Navigieren Sie zu [Microsoft Edge DevTools-Tastenkombinationen,][DevtoolsShortcutsIndex]um weitere Informationen zu erfahren.  
1.  Öffnen Sie den [bereich Einstellungen.][DevToolsCustomizeIndexSettings]  
    *   Wählen Sie `Shift` + `?` .  Navigieren Sie zu [Microsoft Edge DevTools-Tastenkombinationen,][DevtoolsShortcutsIndex]um weitere Informationen zu erfahren.  
1.  Wählen Sie auf der linken Seite des **Einstellungen** Bereichs den Abschnitt **"Experimente"** aus.  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Seite Experimente in Einstellungen" lightbox="../media/experiments-devtools.msft.png":::
       Seite **"Experimente"** in **Einstellungen**  
    :::image-end:::  
    
1.  Scrollen Sie auf der Seite **"Experimente"** durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben jedem Feature, das Sie testen möchten.  
1.  Schließen Sie Microsoft Edge DevTools, und öffnen Sie es erneut.  
    
> [!NOTE]
> Experimentelle Features werden ständig aktualisiert und können Leistungsprobleme verursachen.  Um ein experimentelles Feature zu deaktivieren, öffnen Sie die Seite **"Experimente",** und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.  

## <a name="highlighted-experimental-features"></a>Hervorgehobene experimentelle Features  

In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge verfügbar sind.  

| Experimentelles Feature | Microsoft Edge Version |  
|:--- |:--- |  
| [Enable webhint](#enable-webhint) | 85 oder höher |  
| [Enable Network Console](#enable-network-console) | 85 oder höher |  
| [Source Order Viewer](#source-order-viewer) | 86 oder höher |  
| [Enable Composited Layers in 3D View](#enable-composited-layers-in-3d-view) | 87 oder höher |  
| [Enable new Font Editor tool within the Styles pane](#enable-new-font-editor-tool-within-the-styles-pane) | 89 oder höher |  
| [Enable new CSS Flexbox debugging features](#enable-new-css-flexbox-debugging-features) | 89 oder höher |  
| [Enable + button tab menus to open more tools](#enable--button-tab-menus-to-open-more-tools) | 89 oder höher |  
| [Enable Welcome tab](#enable-welcome-tab) | 89 oder höher |  

### Enable webhint  

[Webhint][WebhintMain] ist ein Open-Source-Tool, das Feedback in Echtzeit für Websites und lokale Webseiten bereitstellt.  Die Art des Von Webhint bereitgestellten [Feedbacks.][WebhintMain]  

*   Bedienungshilfen  
*   Browserübergreifende Kompatibilität  
*   Sicherheit  
*   Leistung  
*   Progressive Web Apps (PWAs)  
*   Andere allgemeine Probleme bei der Webentwicklung  
    
Das [Webhint-Experiment][WebhintMain] zeigt das Webhint-Feedback im [Bereich "Probleme"][DevtoolsIssuesIndex] an.  Wählen Sie ein Problem aus, um die Lösungsdokumentation und eine Liste der betroffenen Ressourcen auf Ihrer Website anzuzeigen.  Wählen Sie einen Ressourcenlink aus, um den relevanten **Bereich "Netzwerk",** **"Quellen"** oder **"Elemente"** in DevTools zu öffnen.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="Webhint-Feedback im Bereich Probleme" lightbox="../media/experiments-webhint.msft.png":::
   Webhint-Feedback im **Bereich "Probleme"**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Enable Network Console  

**Die Netzwerkkonsole** ist der Arbeitstitel eines Experiments für synthetische Netzwerkanforderungen über HTTP.  Sie können das **Netzwerkkonsolen-Experiment** verwenden, um Web-API-Anforderungen zu senden.  

Stellen Sie nach dem Aktivieren des Experiments sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden Schritte aus, um die **Netzwerkkonsole**zu verwenden.  

1.  Öffnen Sie den **Netzwerkbereich.**  
1.  Suchen Sie die Netzwerkanforderung, die Sie ändern und erneut senden möchten.  
1.  Öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **Bearbeiten und Wiedergeben**aus.  
1.  Wenn die **Netzwerkkonsole** geöffnet wird, bearbeiten Sie die Netzwerkanforderungsinformationen.  
1.  Wählen Sie **"Senden"** aus.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Netzwerkkonsole in der Konsolenschublade" lightbox="../media/network-network-console.msft.png":::
   **Netzwerkkonsole** in der **Konsolenschublade**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Source Order Viewer  

**Source Order Viewer** ist ein Experiment, das die Reihenfolge der Elemente in der Webseitenquelle anzeigt.  Die Anzeigereihenfolge auf dem Bildschirm kann sich von der Reihenfolge der Quelle unterscheiden, was die Bildschirmleseprogramme und Tastaturbenutzer verwirren kann.  Verwenden Sie das **Source Order Viewer** Experiment, um die Unterschiede zwischen der Bildschirmanzeigereihenfolge und der Reihenfolge der Quelle zu ermitteln.  

Stellen Sie nach dem Aktivieren des Experiments sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden Schritte aus, um dies zu **Source Order Viewer** verwenden.  

1.  Öffnen Sie **das** Elementtool.  
1.  Wählen Sie rechts neben der Registerkarte **"Formatvorlagen"** die Registerkarte **"Barrierefreiheit"** aus.  
1.  Aktivieren Sie im **Source Order Viewer** Abschnitt das Kontrollkästchen **"Quellreihenfolge anzeigen".**  
1.  Markieren Sie jedes HTML-Element, um eine Überlagerung anzuzeigen, die in der Reihenfolge in der Webseitenquelle angegeben ist.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Source Order Viewer in the Accessibility pane" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Source Order Viewer** in the **Accessibility** pane  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Enable Composited Layers in 3D View  

Sie können Layer jetzt zusammen mit Z-Indizes und dem Dokumentobjektmodell \(DOM\) visualisieren.  Dieses Feature hilft Ihnen beim Debuggen, ohne den Kontext so oft zu wechseln.  Sie haben festgestellt, dass die Reduzierung des Kontextwechsels ein wichtiger Problempunkt war.  Es ist nicht immer klar, wie sich der von Ihnen geschriebene Code auf Ihre Web-App auswirkt.  Für ein umfassendes visuelles Debugging werden jetzt die 3D View zusammengesetzten Layer kombiniert.  

Stellen Sie nach dem Aktivieren des Experiments sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden Schritte aus, um **zusammengesetzte Layer**zu verwenden.  

1.  Wählen Sie in der Schublade das **3D View** Tool aus.  
1.  Öffnen Sie den Bereich **"Zusammengesetzte Ebenen".**  
1.  Alle gezeichneten Ebenen der App werden angezeigt.  Testen Sie dieses Feature mit Ihren eigenen Web-Apps.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Bereich Zusammengesetzte Ebenen" lightbox="../media/experiments-layers.msft.png":::
   Bereich **Zusammengesetzte Ebenen**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Enable new Font Editor tool within the Styles pane  

Sie können jetzt den neuen visuellen [Schriftarten-Editor][DevtoolsInspectStylesEditFonts] verwenden, um Schriftarten zu bearbeiten.  Verwenden Sie sie, um Schriftarten und Schriftartmerkmale zu definieren.  Mit dem visuellen **Schriftarten-Editor** können Sie die folgenden Aktionen ausführen.  

*   Wechseln zwischen Einheiten für unterschiedliche Schriftarteigenschaften  
*   Wechseln zwischen Schlüsselwörtern für unterschiedliche Schriftarteigenschaften  
*   Konvertieren von Einheiten  
*   Generieren von genauem CSS-Code  
    
Stellen Sie nach dem Aktivieren des Experiments sicher, dass Sie die DevTools neu starten.  Führen Sie die folgenden Schritte aus, um den neuen visuellen **Schriftarten-Editor zu**verwenden.  

1.  Öffnen Sie **das** Elementtool.  
1.  Öffnen Sie den Bereich **"Formatvorlagen".**  
1.  Klicken Sie auf das **Schriftarten-Editor-Symbol.**  
    
For more information about the new visual **Font Editor**, navigate to Edit CSS font styles and settings in the Styles pane [in DevTools][DevtoolsInspectStylesEditFonts].  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Der Bereich des visuellen Schriftarten-Editors ist hervorgehoben." lightbox="../media/font-editor-open.msft.png":::
   Der Bereich des visuellen **Schriftarten-Editors** ist hervorgehoben.  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable new CSS Flexbox debugging features  

Dieses experimentelle Feature bietet viele neue Visualisierungen, die Ihnen beim Debuggen von CSS-Flexbox-Layouts helfen.  Um eine Vorschau der neuesten experimentellen Features anzuzeigen, [aktivieren Sie dieses Experiment,](#turn-on-experimental-features) und laden Sie DevTools neu.  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a>Anzeigen persistenter Überlagerungen auf Flexbox-Layouts mit dem Inspect-Tool  

Das **Inspect-Tool** bietet eine schnelle Möglichkeit, CSS Flexbox-Layouts in einer Website zu identifizieren und zu visualisieren, indem Sie mit der Maus darauf zeigen.  Klicken Sie in der oberen linken Ecke von DevTools auf das Symbol **"Überprüfen** ![ \( Überprüfen ](../media/inspect-icon.msft.png) \)".  Zeigen Sie dann beim Debuggen der Website auf einen Flex-Container, um Gliederungen um den Flex-Container anzuzeigen.  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Anzeigen von Flexbox-Containern mit dem Inspect-Tool" lightbox="../media/flexbox-hover.msft.png":::
   Anzeigen von Flexbox-Containern mit dem **Inspect-Tool**  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a>Anzeigen persistenter Überlagerungen in Flexbox-Layouts  

In Microsoft Edge Version 89 oder höher bietet das experimentelle CSS-Flexbox-Feature auch die Möglichkeit, persistente Überlagerungen für Flexbox-Layouts zu aktivieren.  Persistente Überlagerungen bieten die folgenden Vorteile.  

*   Persistente Überlagerungen bleiben auf der Webseite sichtbar, während Sie scrollen, die Maus bewegen und andere Features der DevTools verwenden.
*   Mehrere persistente Überlagerungen können gleichzeitig verwendet werden, damit Sie mehrere Flexbox-Layouts gleichzeitig überprüfen können.  
*   Persistente Überlagerungen bieten Optionen für die Farbkonfiguration.  
    
Verwenden Sie eine der folgenden Aktionen, um beständige Überlagerungen im Flexbox-Layout umzuschalten.  

*   Wählen Sie das **Flexbox-Ovalsymbol** neben einem beliebigen Flexbox-Container aus, der in der DOM-Struktur des **Elements-Tools** angezeigt wird.  
*   Öffnen Sie den neuen **Layoutbereich** im **Elementtool,** und aktivieren Sie das Kontrollkästchen neben jedem Flexbox-Container, den Sie hervorheben möchten.  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Flex-Symbole und Layoutpanel in DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   Flex-Symbole und **Layoutpanel** in DevTools  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a>Konfigurieren persistenter Überlagerungen  

Verwenden Sie den **Layoutbereich,** um Optionen für persistente Überlagerungen für CSS-Raster oder Flexbox-Layouts zu konfigurieren.  Der **Layoutbereich** befindet sich im **Elementtool** neben den Bereichen **"Formatvorlagen"** und **"Berechnet".**  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Layoutpanel" lightbox="../media/flexbox-layout.msft.png":::
   Layoutpanel  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable + button tab menus to open more tools  

Sie können jetzt weitere Tools mit dem neuen Symbol **"Weitere Tools** \( `+` \)" öffnen.  Nachdem Sie das Experiment aktiviert **Enable + button tab menus to open more tools** und DevTools neu geladen haben, wird rechts `+` neben der Registerkartengruppe oben in den DevTools ein Pluszeichen \( \) angezeigt.  Um eine Liste anderer Tools anzuzeigen, die Sie der Registerkartenleiste hinzufügen können, wählen Sie das neue Symbol **"Weitere Tools** \( `+` \) " aus.  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Weitere Tools im oberen Bereich" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Weitere Tools** im oberen Bereich
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable Welcome tab

Dieses Experiment ersetzt das Tool **"Neuigkeiten"** durch das neue **Willkommenstool.**  Es wird ein aktualisiertes Design für den folgenden Inhalt angezeigt.  

*   Links zu Entwicklerdokumenten  
*   Die neuesten Features  
*   Versionshinweise  
*   Option zum Kontaktieren des Microsoft Edge DevTools-Teams  
    
Das **Willkommenstool** wird nach jedem Update für Microsoft Edge automatisch geöffnet.  Um zu verhindern, **** dass das Willkommens-Tool nach jedem Update angezeigt wird, deaktivieren Sie das Kontrollkästchen neben der **Registerkarte "Öffnen" nach jedem Update** unter dem Titel des **Willkommenstools.**  

Wenn Sie das ursprüngliche Tool **"What's New"** bevorzugen, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings]  >  **Experiments,** und entfernen Sie das Kontrollkästchen neben **Enable Welcome tab** .  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Willkommens-Tool" lightbox="../media/experiments-welcome.msft.png":::
   **Willkommens-Tool**  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a>Frühere experimentelle Features  

*   [3D View][Devtools3dViewIndex]ist jetzt in Microsoft Edge Version 83 oder höher standardmäßig verfügbar und aktiviert.  
*   [Turn on support to move tabs between panels][DevtoolsCustomizeIndex]ist jetzt in Microsoft Edge Version 85 oder höher standardmäßig verfügbar und aktiviert.  
*   [Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]ist jetzt in Microsoft Edge Version 86 oder höher standardmäßig verfügbar und aktiviert.  
*   [Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]ist jetzt in Microsoft Edge Version 89 oder höher standardmäßig verfügbar und aktiviert.  
*   [Turn on new CSS grid debugging features][DevtoolsCssGrid]ist jetzt in Microsoft Edge Version 89 oder höher standardmäßig verfügbar und aktiviert.  
*   [Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables]ist jetzt in Microsoft Edge Version 90 oder höher standardmäßig verfügbar und aktiviert.  

## <a name="providing-feedback-on-experimental-features"></a>Bereitstellen von Feedback zu experimentellen Features  

Um Feedback zu Microsoft Edge DevTools-Experimenten oder zu anderen mit DevTools verbundenen Themen zu geben.  

*   Senden Sie Ihr Feedback über das Symbol **"Feedback senden"** in den DevTools.  
*   Tweet bei [@EdgeDevTools][TwitterEdgedevtools]  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol Feedback senden in den Microsoft Edge-Entwicklungstools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   Das Symbol **Feedback senden** in den Microsoft Edge-Entwicklungstools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  
[Devtools3dViewIndex]: ../3d-view/index.md "3D View | Microsoft-Dokumente"  
[DevtoolsCssGrid]: ../css/grid.md "Untersuchen des CSS-Rasters in Microsoft Edge DevTools-| Microsoft-Dokumente"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Anpassen Microsoft Edge DevTools-| Microsoft-Dokumente"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Edit keyboard shortcuts for any action in the DevTools | Microsoft-Dokumente"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code | Microsoft-Dokumente"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emulieren von Geräten mit dualem Bildschirm und faltbaren Geräten in Microsoft Edge DevTools | Microsoft-Dokumente"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simulieren mobiler Geräte mit gerätemodus in Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich „Formatvorlagen“ in DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Suchen und Beheben von Problemen mithilfe des Tools &quot;Probleme&quot; | Microsoft-Dokumente"  
[DevtoolsOpenIndex]: ../open/index.md "Öffnen sie Microsoft Edge DevTools-| Microsoft-Dokumente"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge DevTools-Tastenkombinationen | Microsoft-Dokumente"  
<!-- external links: -->
[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  
[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  
[WebhintMain]: https://webhint.io "webhint"  
