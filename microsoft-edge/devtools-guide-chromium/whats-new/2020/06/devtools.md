---
description: CSS-Rasterdebuggingfeatures, Bearbeiten und Wiederholen von Anforderungen mit der Netzwerkkonsole und vieles mehr.
title: Neuigkeiten in DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 65a3fb4da235d2330bf9205b7a4a79a999559ca4
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624801"
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
# <a name="whats-new-in-devtools-microsoft-edge-85"></a>Neuigkeiten in DevTools (Microsoft Edge 85)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Ankündigungen des Microsoft Edge DevTools-Teams  

In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise vom Microsoft Edge DevTools-Team verpasst haben.  Sehen Sie sich die Ankündigungen an, um neue Features in devTools, Microsoft Visual Studio Codeerweiterungen und vieles mehr auszuprobieren.  Um über die neuesten und besten Features in Ihren Entwicklertools auf dem Laufenden zu bleiben, laden Sie die [Microsoft Edge Vorschaukanäle][MicrosoftEdgePreviewChannels] herunter, und [folgen Sie dem Microsoft Edge DevTools-Team auf Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="css-grid-debugging-features"></a>CSS-Rasterdebuggingfeatures  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

Das Microsoft Edge DevTools-Team arbeitet mit dem Chrome DevTools-Team und Chromium Community zusammen, um DevTools neue CSS-Rasterdebuggingfeatures hinzuzufügen.  Sie können jetzt Rasterliniennummern, Rasterlücken und erweiterte Rasterlinien als Seitenüberlagerung anzeigen.  Darüber hinaus werden in Kürze weitere Verbesserungen an den Rastertools verfügbar sein.  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="CSS-Rasterdebuggingfeatures" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   CSS-Rasterdebuggingfeatures
:::image-end:::  

> [!NOTE]
> Um das Experiment zu aktivieren, navigieren Sie zu ["Experimentelle Features aktivieren",][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben **"Neue CSS-Rasterdebuggingfeatures aktivieren".**  
> 
> Um das Experiment mit einem Beispiel auszuprobieren, navigieren Sie zum [CSS-Rasterplanerbeispiel.][CodepenRachelweilYzwBzKM]  

Chromium Problem [#1047356][CR1047356]  

### <a name="edit-and-replay-requests-with-the-network-console"></a>Bearbeiten und Wiedergeben von Anforderungen mit der Netzwerkkonsole  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

Sie können jetzt **Bearbeiten und Wiedergeben** von Anforderungen im [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity] mithilfe der **Netzwerkkonsole**verwenden.  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Bearbeiten und Wiedergeben einer Anforderung im Netzwerkprotokoll mit der Netzwerkkonsole" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   Bearbeiten und Wiedergeben einer Anforderung im [Netzwerkprotokoll][DevtoolsNetworkIndexLogActivity] mit der **Netzwerkkonsole**  
:::image-end:::  

In einem neuen Bereich wird die **Netzwerkkonsole** in der [DevTools-Schublade][DevtoolsCustomizeIndexDrawer] geöffnet und automatisch mit Informationen für die HTTP-Anforderung aufgefüllt.  Bearbeiten Sie zum Anzeigen der vom Server zurückgegebenen Antwort die Anforderung \(falls erforderlich\), und wählen Sie **"Senden"** aus.  

Sie können auch die **Netzwerkkonsole** verwenden, um HTTP-Anforderungen direkt über devTools zu erstellen und zu senden.  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Der Bereich Netzwerkkonsole" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   **Der Bereich "Netzwerkkonsole"**  
:::image-end:::  

> [!TIP]
> Um die **Netzwerkkonsole** im Hauptbereich \(oben\) anstelle der [DevTools-Schublade][DevtoolsCustomizeIndexDrawer]anzuzeigen, navigieren Sie zu Verschieben von [Tools zwischen Bereichen.](#move-tools-between-panels)  

> [!NOTE]
> Um das Experiment zu aktivieren, navigieren Sie zu ["Experimentelle Features aktivieren",][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben **"Netzwerkkonsole aktivieren".**  
> 
> Öffnen Sie das [Netzwerkprotokoll,][DevtoolsNetworkIndexLogActivity]öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **Bearbeiten und Wiedergeben**aus.  

Chromium Problem [#1093687][CR1093687]  

### <a name="service-worker-respondwith-events-in-the-timing-tab"></a>Service Worker respondWith-Ereignisse auf der Registerkarte "Timing"  

Die Registerkarte **"Timing"** des **Netzwerktools** enthält jetzt `respondWith` Service Worker-Ereignisse.  Das `respondWith` Service Worker-Ereignis zeigt die Dauer von der Zeit unmittelbar vor der Ausführung des Service `fetch` Worker-Ereignishandlers bis zu dem Zeitpunkt an, zu dem `respondWith` die Zusage des `fetch` Handlers nicht erfüllt ist.  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Das RespondWith Service Worker-Ereignis auf der Registerkarte Timing des Netzwerkbereichs" lightbox="../../media/2020/06/timing-tab.msft.png":::
   Das `respondWith` Service Worker-Ereignis auf der Registerkarte **"Timing"** des **Netzwerktools**  
:::image-end:::  

Erweitern Sie **die empfangene Antwort,** um zusätzliche Informationen aus der `fetch` Antwort anzuzeigen, z. `CacheStorageCacheName` B. , und `serviceWorkerResponseSource` `ResponseTime` .  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Erweitern der empfangenen Antwort, um zusätzliche Informationen aus der Abrufantwort anzuzeigen" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   Erweitern sie **die empfangene Antwort,** um zusätzliche Informationen aus der Antwort anzuzeigen. `fetch`  
:::image-end:::  

Chromium Problem [#1066579][CR1066579]  

### <a name="webhint-feedback-in-the-issues-panel"></a>Webhint-Feedback im Bereich "Probleme"  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

[Webhint][WebhintMain] ist ein Open Source-Tool, das Echtzeitfeedback zu Barrierefreiheit, browserübergreifender Kompatibilität, Sicherheit, Leistung, PWAs und anderen allgemeinen Webentwicklungsproblemen von Websites bereitstellt.  So überprüfen Sie Webhint-Feedback im [Bereich "Probleme".][DevtoolsIssues]  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Webhint-Feedback im Bereich Probleme" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   Webhint-Feedback im Bereich "Probleme"  
:::image-end:::  

> [!NOTE]
> Um das Experiment zu aktivieren, navigieren Sie zu ["Experimentelle Features aktivieren",][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben **"Webhint aktivieren".**  
> 
> Öffnen Sie den [Bereich "Probleme",][DevtoolsIssues] um Feedback von Webhint anzuzeigen.  

Chromium Problem [#1070378][CR1070378]  

### <a name="move-tools-between-panels"></a>Verschieben von Tools zwischen Bereichen  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Experimentelles Feature":::
   Experimentelles Feature  
:::image-end:::  

Normalerweise können Tools wie **"Elemente"** und **"Netzwerk"** nur im Hauptbereich \(oben\) von DevTools geöffnet werden.  Ebenso können Tools wie **die 3D-Ansicht** und **Probleme** nur im Bereich "Schublade \(bottom\)" von DevTools geöffnet werden.  Sie können nun Ihr DevTools-Layout anpassen, indem Sie Tools zwischen den oberen und unteren Bereichen verschieben.  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Verschieben von Tools zwischen Bereichen" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   Verschieben von Tools zwischen Bereichen  
:::image-end:::  

> [!NOTE]
> Um das Experiment zu aktivieren, navigieren Sie zu ["Experimentelle Features aktivieren",][DevtoolsExperimentalFeaturesTurnOn] und aktivieren Sie das Kontrollkästchen neben "Unterstützung zum Verschieben von **Registerkarten zwischen Bereichen aktivieren".**  

Chromium Problem [#897944][CR897944]  

### <a name="improved-initiator-tooltip-in-the-network-panel"></a>Verbesserte Initiator-QuickInfo im Netzwerkbereich  

In Microsoft Edge 83 und 84 quickinfos for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.  Sie konnten nur den Aufrufstapel anzeigen, der die Anforderung initiiert hat, indem Sie in der QuickInfo horizontal scrollen.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Die Initiator-QuickInfo in Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   Die Initiator-QuickInfo in Microsoft Edge 84  
:::image-end:::  

Ab Microsoft Edge 85 können Sie nun den Initiator-Aufrufstapel in der QuickInfo anzeigen, ohne horizontal zu scrollen.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Die Initiator-QuickInfo in Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   Die Initiator-QuickInfo in Microsoft Edge 85
:::image-end:::  

Chromium Problem [#1069404][CR1069404]  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

In den folgenden Abschnitten werden zusätzliche Features angekündigt, die in Microsoft Edge 85 verfügbar sind und zum Open Source Chromium Projekt beigetragen haben.  

### <a name="style-editing-for-css-in-js-frameworks"></a>Formatvorlagenbearbeitung für CSS-in-JS-Frameworks  

Der Bereich **"Formatvorlagen"** bietet jetzt eine bessere Unterstützung für die Bearbeitung von Formatvorlagen, die mit den [CSS-Objektmodell-APIs (CSSOM)][CsswgDraftsCssom] erstellt wurden.  Viele CSS-in-JS-Frameworks und -Bibliotheken verwenden die CSSOM-APIs im Rahmen der Erstellung von Formatvorlagen.  

Sie können jetzt Formatvorlagen bearbeiten, die in JavaScript [mithilfe von constructable Stylesheets][WicgConstructStylesheet]hinzugefügt wurden.  Konstruktierbare Stylesheets sind eine neue Möglichkeit zum Erstellen und Verteilen wiederverwendbarer Formatvorlagen bei Verwendung von [Shadow DOM.][MdnShadowDom]  

Beispielsweise waren die `h1` mit `CSSStyleSheet` \(CSSOM-APIs\) hinzugefügten Formatvorlagen zuvor nicht bearbeitbar.  Die Formatvorlagen können jetzt im Bereich **"Formatvorlagen"** bearbeitet werden.  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Ändern der Hintergrundeigenschaft der h1-Formatvorlagen, die mit CSSStyleSheet hinzugefügt wurden, von Rosa in Hellblau" lightbox="../../media/2020/06/css-in-js.msft.png":::
   Ändern der `background` Eigenschaft der `h1` Formatvorlagen, mit denen hinzugefügt `CSSStyleSheet` wurde, in `pink` `lightblue` .
:::image-end:::  

Probieren Sie dieses Feature mit einem [Beispiel aus, das CSS-in-JS verwendet.][CodepenZoherghadyaliAbdgrpz]

Chromium Problem [#946975][CR946975]  

### <a name="lighthouse-6-in-the-lighthouse-panel"></a>"6" im Panel "Panels"  

Im **Panel "Panels"** wird jetzt "6" ausgeführt.  Navigieren Sie für eine vollständige Liste aller Änderungen zu [den Versionshinweisen von v6.0.0.][GithubGoogleChromeLighthouse600]  

Mit "6.0" werden drei neue Metriken in den Bericht eingeführt: größte contentful Paint \(LCP\), kumulative Layoutverschiebung \(CLS\) und Gesamtblockierungszeit \(TBT\).  

Die Leistungsbewertungsformel wurde ebenfalls neu gewichtet, um die Ladeerfahrung des Benutzers besser widerzuspiegeln.  

Chromium Problem [#772558][CR772558]  

#### <a name="first-meaningful-paint-deprecation"></a>First Meaningful Paint deprecation  

First Meaningful Paint \(FMP\) is deprecated inIron 6.0.  FMP wurde auch aus dem **Leistungsbereich** entfernt.  **Der größte inhaltsreiche Paint** ist der empfohlene Ersatz für FMP.  <!--For an explanation of why it was deprecated, navigate to [First Meaningful Paint][WebDevFirstMeaningfulPaint].  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

Chromium Problem [#1096008][CR1096008]  

### <a name="support-for-new-javascript-features"></a>Unterstützung für neue JavaScript-Features  

DevTools bietet jetzt eine bessere Unterstützung für einige der neuesten JavaScript-Sprachfeatures.  

:::row:::
   :::column span="1":::
      [Optionale automatische Verkettungssyntax][V8DevOptionalChaining]  
   :::column-end:::
   :::column span="2":::
      Die automatische Vervollständigung der Eigenschaft in der **Konsole** unterstützt jetzt die optionale Verkettungssyntax, z. B.  `name?.` funktioniert jetzt zusätzlich zu und `name.` `name[` .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Syntaxhervorhebung für [private Felder][V8DevClassFieldsPrivate]  
   :::column-end:::
   :::column span="2":::
      Private Klassenfelder werden nun im Bereich **"Quellen"** korrekt hervorgehoben und ziemlich gedruckt.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Syntaxhervorhebung für [Nullish-Koalescing-Operator][V8DevNullishCoalescing]
   :::column-end:::
   :::column span="2":::
      DevTools druckt nun den Null-Koalescing-Operator im **Quellenbereich** ordnungsgemäß.  
   :::column-end:::
:::row-end:::  

Chromium Probleme [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]  

### <a name="new-app-shortcut-warnings-in-the-manifest-pane"></a>Warnungen zu neuen App-Verknüpfungen im Manifestbereich  

**App-Verknüpfungen** helfen Benutzern, allgemeine oder empfohlene Aufgaben innerhalb einer Web-App schnell zu starten.  

<!--todo: add App shortcuts when section is live  -->  

Im **Manifestbereich** werden nun Warnungen für die folgenden Bedingungen angezeigt.  

* Die App-Verknüpfungssymbole sind kleiner als 96 x 96 Pixel  
* Die App-Verknüpfungssymbole und Manifestsymbole sind nicht quadratisch \(da die Symbole ignoriert werden\)  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="App-Tastenkombinationswarnungen" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   App-Tastenkombinationswarnungen  
:::image-end:::  

Chromium Problem [#955497][CR955497]  

### <a name="consistent-display-of-the-computed-pane"></a>Konsistente Anzeige des berechneten Bereichs  

Der **Bereich Berechnet ** im Tool ** Elemente ** wird jetzt konsistent als Bereich für alle Viewportgrößen angezeigt.  Zuvor wurde der **Bereich "Berechnet"** im Bereich **"Formatvorlagen"** zusammengeführt, wenn die Breite des DevTools-Viewports schmal war.  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Der berechnete Bereich wird konsistent als separater Bereich angezeigt, auch wenn die DevTools schmal sind." lightbox="../../media/2020/06/computed-pane.msft.png":::
   Der **berechnete** Bereich wird konsistent als separater Bereich angezeigt, auch wenn die DevTools schmal sind.
:::image-end:::  

Chromium Problem [#1073899][CR1073899]  

### <a name="bytecode-offsets-for-webassembly-files"></a>Bytecode-Offsets für WebAssembly-Dateien  

DevTools verwendet jetzt Bytecode-Offsets zum Anzeigen von Zeilennummern der Wasm-Zerlegung.  
Die Zeilennummern verdeutlichen, dass Sie binäre Daten betrachten, und sind konsistenter mit der Art und Weise, wie die Wasm-Laufzeit auf Speicherorte verweist.  

Chromium Problem [#1071432][CR1071432]  

### <a name="line-wise-copy-and-cut-in-sources-panel"></a>Zeilenweises Kopieren und Ausschneiden im Quellenbereich  

Wenn Sie das Kopieren oder Ausschneiden ohne Auswahl im Editor des [Quellenbereichs][DevtoolsSourcesIndexUsingEditorPaneToViewEditFiles]ausführen, kopiert oder schneidet DevTools die aktuelle Inhaltszeile.  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Mit dem Cursor am Ende von Zeile 5 kopieren Sie die gesamte Zeile aus pen.js in devTools und einfügen in Visual Studio Code" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   Kopieren Sie mit dem Cursor am Ende von Zeile 5 die gesamte Zeile aus **pen.js** in den DevTools, und kopieren Sie sie in [Visual Studio Code.][VisualStudioCode]
:::image-end:::  

Chromium Problem [#800028][CR800028]

### <a name="console-settings-updates"></a>Konsolen-Einstellungen-Updates  

#### <a name="ungroup-same-console-messages"></a>Aufheben der Gruppierung derselben Konsolennachrichten  

Die **Umschaltfläche "Gruppe"** in konsolenähnlicher Einstellungen gilt jetzt für doppelte Nachrichten.  Zuvor wurde sie nur auf ähnliche Nachrichten angewendet.  

Beispielsweise hat DevTools zuvor die Gruppierung der Nachrichten nicht aufgehoben, `hello` obwohl **"Gruppe ähnlich"** deaktiviert ist.  Jetzt werden die Gruppierung der `hello` Nachrichten aufgehoben.  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Wenn Gruppe ähnlich deaktiviert ist, werden die Hello-Nachrichten nicht gruppiert." lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   Wenn **"Gruppe ähnlich"** deaktiviert ist, werden die Gruppierung der `hello` Nachrichten aufgehoben.
:::image-end:::  

Probieren Sie dieses Feature mit einem [Beispiel aus, das doppelte Nachrichten an die Konsole sendet.][CodepenZoherghadyaliZyrjgdJ]  

Chromium Problem [#1082963][CR1082963]  

### <a name="persisting-selected-context-only-settings"></a>Speichern ausgewählter Kontexteinstellungen  

Die Einstellungen für **den ausgewählten Kontext** in Konsolen-Einstellungen werden jetzt beibehalten.  Zuvor wurden die Einstellungen jedes Mal zurückgesetzt, wenn Sie DevTools geschlossen und erneut geöffnet haben.  Die Änderung sorgt dafür, dass das Einstellungsverhalten mit anderen Konsolen-Einstellungen-Optionen konsistent ist.  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Einstellung nur für ausgewählten Kontext" lightbox="../../media/2020/06/selected-context.msft.png":::
   **Einstellung nur für ausgewählten Kontext**  
:::image-end:::  

Chromium Problem [#1055875][CR1055875]  

### <a name="performance-panel-updates"></a>Aktualisierungen des Leistungsbereichs  

#### <a name="javascript-compilation-cache-information-in-performance-tool"></a>JavaScript-Kompilierungscacheinformationen im **Leistungstool**  

[JavaScript-Kompilierungscacheinformationen][V8DevCodeCaching] werden jetzt immer im **Zusammenfassungsbereich** des **Leistungstools** angezeigt.  Bisher hat DevTools nichts im Zusammenhang mit der Codezwischenspeicherung angezeigt, wenn keine Codezwischenspeicherung durchgeführt wurde.  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="JavaScript-Kompilierungscacheinformationen" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   JavaScript-Kompilierungscacheinformationen  
:::image-end:::  

Chromium Problem [#912581][CR912581]  

#### <a name="navigation-timing-alignment-in-the-performance-panel"></a>Ausrichtung des Navigationszeitpunkts im Leistungsbereich  

Der **Leistungsbereich,** der verwendet wird, um Zeiten in den Lineals basierend auf dem Start der Aufzeichnung anzuzeigen.  Das Timing für Aufzeichnungen, in denen der Benutzer navigiert, wurde nun geändert, wobei DevTools stattdessen Linealzeiten relativ zur Navigation anzeigt.  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Ausrichten des Navigationszeitpunkts im Leistungstool" lightbox="../../media/2020/06/nav-timing.msft.png":::
   Ausrichten des Navigationszeitpunkts im **Leistungstool**  
:::image-end:::  

Die Zeiten für `DOMContentLoaded` ereignisse , first Paint, First Contentful Paint und Largest Contentful Paint werden so aktualisiert, dass sie relativ zum Start der Navigation sind, was bedeutet, dass das Timing mit den von gemeldeten Zeitangaben `PerformanceObserver` übereinstimmt.  

Chromium Problem [#974550][CR974550]  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a>Neue Symbole für Haltepunkte, bedingte Haltepunkte und Protokollpunkte  

Der **Quellenbereich** verfügt über neue Designs für Haltepunkte, bedingte Haltepunkte und Protokollpunkte.  Haltepunkte werden wie [Visual Studio Code][VisualStudioCode] und [Visual Studio][VisualStudio]durch einen roten Kreis dargestellt.  Symbole werden hinzugefügt, um bedingte Haltepunkte und Protokollpunkte zu unterscheiden.  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Breakpoints" lightbox="../../media/2020/06/breakpoints.msft.png":::
   Breakpoints  
:::image-end:::  

Chromium Problem [#1041830][CR1041830]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie Windows oder macOS verwenden, sollten Sie die [Microsoft Edge Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../../../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsCommandMenu]: ../../../command-menu.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft-Dokumente"
[DevtoolsCustomizeIndexDrawer]: ../../../customize/index.md#drawer "Schublade – Anpassen Microsoft Edge DevTools-| Microsoft-Dokumente"
[DevtoolsExperimentalFeaturesTurnOn]: ../../../experimental-features/index.md#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsIssues]: ../../../issues/index.md "Suchen und Beheben von Problemen mithilfe des Tools &quot;Probleme&quot; | Microsoft-Dokumente"
[DevtoolsSourcesIndexUsingEditorPaneToViewEditFiles]: ../../../sources/index.md#using-the-editor-pane-to-view-or-edit-files "Verwenden des Editorbereichs zum Anzeigen oder Bearbeiten von Dateien – Übersicht über den Quellenbereich | Microsoft-Dokumente"  
[DevtoolsNetworkIndexLogActivity]: ../../../network/index.md#log-network-activity "Protokollieren von Netzwerkaktivitäten – Überprüfen der Netzwerkaktivität in Microsoft Edge DevTools-| Microsoft-Dokumente"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Formatvorlagenbearbeitung für CSS-in-JS-Frameworks | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Senden doppelter Nachrichten an konsolen | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "CSS-Rasterplaner –Beispiel | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

[CR772558]: https://crbug.com/772558 "DevTools: Update auf die neueste Version von | Chromium Fehler"  
[CR800028]: https://crbug.com/800028 "Doppelte Zeilenverknüpfung im Entwicklertools-Editor funktioniert nach chrome update | Chromium Fehler"  
[CR912581]: https://crbug.com/912581 "Verfügbar machen, welche Skripts von V8 in DevTools/about:tracing | codecachediert wurden Chromium Fehler"  
[CR946975]: https://crbug.com/946975 "Die DevTools-Formatvorlagen-Randleiste funktioniert nicht mit erstellten Stylesheets | Chromium Fehler"  
[CR955497]: https://crbug.com/955497 "Kontextmenü für App-Symbole für PWAs | Chromium Fehler"  
[CR974550]: https://crbug.com/974550 "Metrikkonflikt zwischen Perf-Bereich und performanceObserver-| Chromium Fehler"  
[CR1041830]: https://crbug.com/1041830 "Verbessern von Farben für Haltepunkte | Chromium Fehler"  
[CR1055875]: https://crbug.com/1055875 "Der Wert der Konsoleneinstellung &quot;Ausgewählter Kontext&quot; bleibt nach dem Schließen und erneuten Öffnen der Entwicklertools | Chromium Fehler"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Show ServiceWorkers Fetch Timeline per request in Network panel | Chromium Fehler"  
[CR1071432]: https://crbug.com/1071432 "Wasm Basic Developer Experience | Chromium Fehler"  
[CR1073899]: https://crbug.com/1073899 "Registerkarte für berechnete Stile wird im reaktionsfähigen Modus nicht mehr angezeigt | Chromium Fehler"  
[CR1073903]: https://crbug.com/1073903 "DevTools: Die Syntaxhervorhebung funktioniert bei privaten Feldern nicht | Chromium Fehler"  
[CR1082963]: https://crbug.com/1082963 "Gruppenähnliches Nachrichtenverhalten der Konsole kann nicht deaktiviert werden | Chromium Fehler"  
[CR1083214]: https://crbug.com/1083214 "Acorn unterstützt keine optionale Verkettung | Chromium Fehler"  
[CR1083797]: https://crbug.com/1083797 "Ziemlicher Druck für Null-Koalescing | Chromium Fehler"  
[CR1096008]: https://crbug.com/1096008 "Entfernen von FMP-| Chromium Fehler"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Chromium Fehler"  
[CR1093687]: https://crbug.com/1093687 "Erstellungstool zum Erstellen und Wiedergeben synthetischer Netzwerkanforderungen | Chromium Fehler"  
[CR1070378]: https://crbug.com/1070378 "Integrieren von Webhint in DevTools | Chromium Fehler"  
[CR1069404]: https://crbug.com/1069404 "[Dev Tools] Widget-Popups sind zu eng | Chromium Fehler"  
[CR897944]: https://crbug.com/897944 "Dragable devtool panels | Chromium Fehler"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v6.0.0 – GoogleChrome/- | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Neues Problem – MicrosoftDocs/Edge-Entwickler"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Verwenden von Schatten-DOM-| Mdn"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Microsoft Edge-Vorschaukanäle"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"
[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "CSSOM-| W3C-CSS-Arbeitsgruppen-Editor-Entwürfe"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Posten eines Tweets"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools, Twitter-Konto"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Private Klassenfelder – Öffentliche und private Klassenfelder | V8. Dev"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Zwischenspeichern von Code für JavaScript-Entwickler | V8. Dev"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Null-Koalescing | V8. Dev"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Optionale verkettete | V8. Dev"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Constructable Stylesheet-Objekte | Web-Eningen CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "The Web We Want"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-85) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
