---
description: Die Schaltfläche "Weitere Tools", die Kontextdokumentation für die ersten Schritte mit der DevTools-Erweiterung, die erweiterte Unterstützung für Bildschirmleseprogramme in der Konsole und vieles mehr.
title: Neuigkeiten in DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 09e1438ae7fd6547a7dd14757f54f370c9008773
ms.sourcegitcommit: 1dd6376784c394087fe2938acaa069212cf7656e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2021
ms.locfileid: "11659428"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a>Neuigkeiten in DevTools (Microsoft Edge 92)

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]

> [!TIP]
> Die **Microsoft Build 2021-Konferenz** war vom 25. bis 27. Mai.  Hier ist ein Video von Build über die Updates für DevTools: [Microsoft Edge | Status der Plattform][YoutubeEdgeStateOfThePlatform] – Microsoft Edge bietet eine überzeugende und konsistente Plattform mit Tools für Entwickler.  Wenn der Support für unsere älteren Browser eingestellt wird, wird Edge in Kürze der einzige unterstützte Browser von Microsoft auf Windows 10 sein.  Nehmen Sie an uns teil, um mehr über die neuesten Informationen auf der Edge-Plattform, den Tools und Web-Apps zu erfahren.


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a>Die Schaltfläche "Schließen" ist nicht mehr ausgeblendet, wenn DevTools schmal ist

<!-- Title: DevTools is now easier to close -->
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->

In Microsoft Edge Version 91 oder früheren Versionen wird die Schaltfläche **"Schließen"** zum Schließen von DevTools nicht angezeigt, wenn der DevTools-Viewport schmal ist.  In Microsoft Edge Version 92 ist die Schaltfläche **"Schließen"** in den DevTools immer vorhanden, unabhängig von der Breite des DevTools-Viewports.

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="Die Schaltfläche "DevTools schließen" ist jetzt auch dann vorhanden, wenn der Viewport schmal ist." lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   Die Schaltfläche **"DevTools schließen"** ist jetzt auch dann vorhanden, wenn der Viewport schmal ist.
:::image-end:::


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a>Schnelles Hinzufügen von Tools mit der neuen Schaltfläche "Weitere Tools"

<!-- Title: Add tools quickly with the new More Tools button -->
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->

Es gibt eine neue Möglichkeit, weitere Tools in Microsoft Edge DevTools zu öffnen: das Menü **"Weitere Tools** ( `+` ) ". Das Menü **"Weitere Tools"** wird auf der Symbolleiste im Hauptbereich und auf der Symbolleiste der Schublade angezeigt. Wenn Sie ein Tool aus dem Menü **"Weitere Tools"** auswählen, wird das Tool zur Symbolleiste hinzugefügt.

Um die Registerkarten auf beiden Symbolleisten neu anzuordnen, wählen Sie die Registerkarten aus, und ziehen Sie sie.

Das Menü **"Weitere Tools"** war in Microsoft Edge Version 89 als Experiment verfügbar und ist jetzt immer vorhanden.

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="Die Schaltfläche "Weitere Tools" auf der oberen Symbolleiste und der Schublade-Symbolleiste" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   Die Schaltfläche **"Weitere Tools"** auf der oberen Symbolleiste und der Schublade-Symbolleiste
:::image-end:::

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Das Menü "Weitere Tools"" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   Das Menü **"Weitere Tools"**
:::image-end:::


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a>Verbesserungen beim Zeigen, Auswählen und Schließen von Tools

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

Registerkarten für jedes Tool wurden neu formatiert, um die Wahrscheinlichkeit zu verringern, dass ein Tool versehentlich geschlossen wird.  Auf jeder Registerkarte in der Hauptsymbolleiste und in der Symbolleiste der Schublade haben wir Folgendes hinzugefügt:
*  Abstand um die Registerkarte.
*  Abstand um die Schaltfläche "Schließen" `x` ()" auf der Registerkarte.
*  Eine Hintergrundfarbe beim Bewegen über die Registerkarte.
*  Eine QuickInfo für die Schaltfläche zum Schließen ( `x` ) der Registerkarte.
*  Höherer Kontrast für die Schaltfläche zum Schließen ( `x` ) der Registerkarte.

Wenn Sie sich beispielsweise im **Leistungstool** befinden und auf die Registerkarte des **Netzwerktools** zeigen, verhindern diese Verbesserungen das versehentliche Schließen des **Netzwerktools.**

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Registerkarten vor der Neuformatierung" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           Registerkarten vor der Neuformatierung :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Registerkarten nach der Neuformatierung" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           Registerkarten nach der Neuformatierung :::image-end:::
    :::column-end:::
:::row-end:::

Diese Verbesserungen sind besonders für Benutzer lokalisierter DevTools relevant, bei denen die Registerkarten möglicherweise schmaler sind und versehentlich leichter geschlossen werden können.

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="Lokalisierte DevTools mit schmalen Registerkarten" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   Lokalisierte DevTools mit schmalen Registerkarten
:::image-end:::

Außerdem wurde es einfacher, ein Tool, das Sie geschlossen haben, erneut hinzuzufügen, indem ein [Menü "Weitere Tools"](#add-tools-quickly-with-the-new-more-tools-button) zur Hauptsymbolleiste und der Schublade-Symbolleiste hinzugefügt wurde.


## <a name="better-support-for-screen-readers-in-the-console"></a>Bessere Unterstützung für Bildschirmleseprogramme in der Konsole

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

Vor Microsoft Edge Version 92 in der **Konsole**haben Hilfstechnologien wie Bildschirmleseprogramme keine Vorschläge zur automatischen Vervollständigung oder die Ergebnisse ausgewerteter Ausdrücke angekündigt. Dies wurde jetzt behoben.

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="In der Konsole kündigen Bildschirmleseprogramme jetzt den aktuell ausgewählten AutoVervollständigen-Vorschlag an." lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           In der **Konsole**kündigen Bildschirmleseprogramme jetzt den aktuell ausgewählten Vorschlag für automatisches Vervollständigen an. :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="In der Konsole kündigen Bildschirmleseprogramme nun das Ergebnis eines ausgewerteten Ausdrucks an." lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           In der **Konsole**kündigen Bildschirmleseprogramme nun das Ergebnis eines ausgewerteten Ausdrucks an. :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="source-order-viewer"></a>Source Order Viewer

<!--  Title: Source Order Viewer -->
<!--  Subtitle: The new Source Order Viewer displays numbers on the webpage indicating the order of page elements in the source file, independently of how the page sections are positioned by CSS. -->

Sie können jetzt die Reihenfolge der Quellelemente anzeigen, die auf der gerenderten Webseite überlagert sind, um eine bessere Barrierefreiheitsüberprüfung zu erzielen.

Die Reihenfolge der Inhalte in einem HTML-Dokument ist wichtig für die Optimierung und Barrierefreiheit der Suchmaschine.  MIT CSS können Entwickler Inhalte erstellen, die in der Reihenfolge auf dem Bildschirm anders aussieht als die Reihenfolge im HTML-Quelldokument.  Dies ist ein Problem mit der Barrierefreiheit, da Die Benutzer der Sprachausgabe eine verwirrende Erfahrung erhalten könnten.

:::image type="complex" source="../../media/2021/05/source-order-viewer.msft.png" alt-text="Durch Aktivieren des Viewers für die Quellreihenfolge wird die Reihenfolge der Elemente in der Quelle als Überlagerungen auf der Seite angezeigt." lightbox="../../media/2021/05/source-order-viewer.msft.png":::
   Durch Aktivieren des Viewers für die **Quellreihenfolge** wird die Reihenfolge der Elemente in der Quelle als Überlagerungen auf der Seite angezeigt.
:::image-end:::

Navigieren Sie für weitere Informationen zur [Unterstützung der Tastatur mithilfe des Viewers für die Quellreihenfolge.](../../../accessibility/test-tab-key-source-order-viewer.md)

Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1094406][CR1094406].


## <a name="user-agent-client-hints-for-devices-in-the-network-conditions-tab"></a>User-Agent Clienthinweise für Geräte auf der Registerkarte "Netzwerkbedingungen"

<!--  Title: User-Agent Client Hints -->
<!--  Subtitle: Access information about a user's browser in an ergonomic way that preserves privacy. -->

User-Agent Clienthinweise werden jetzt auf Geräte im **Feld "Benutzer-Agent"** im **Netzwerkbedingungentool** angewendet.  User-Agent Clienthinweise sind eine neue Erweiterung der Client hints-API, mit der Sie auf eine einzigartige Weise auf Informationen über den Browser eines Benutzers zugreifen können, um den Datenschutz zu wahren.

:::image type="complex" source="../../media/2021/05/user-agent.msft.png" alt-text="Benutzer-Agent" lightbox="../../media/2021/05/user-agent.msft.png":::
   Benutzer-Agent
:::image-end:::

Navigieren Sie zu [Benutzer-Agent-Clienthinweisen,](../../../../web-platform/user-agent-guidance.md#user-agent-client-hints)um weitere Informationen zu erfahren.

Navigieren Sie zu Problem 1174299, um den Verlauf dieses Features im open-source-Projekt [Chromium][CR1174299]zu überprüfen.


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a>Microsoft Edge Entwicklertools für Visual Studio Code Version 1.1.8

Die [Microsoft Edge Developer Tools für Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Erweiterungsversion 1.1.8 für Microsoft Visual Studio Code weist seit der vorherigen Version die folgenden Änderungen auf.  Microsoft Visual Studio Code aktualisiert Erweiterungen automatisch.  Um die Version 1.1.8 manuell zu aktualisieren, navigieren Sie manuell zu ["Erweiterung aktualisieren".][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]

Sie können Probleme melden und an der Erweiterung im [vscode-edge-devtools GitHub Repo][GithubMicrosoftVscodeEdgeDevtools]mitwirken.

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a>Kontextdokumentation und Benutzeroberfläche, um die Verwendung der DevTools-Erweiterung zu vereinfachen

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->

Version 1.1.8 der [Microsoft Edge Developer Tools für Visual Studio Code-Erweiterung][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] bietet jetzt eine einfachere Möglichkeit, eine neue Instanz von Microsoft Edge zu starten, indem Sie Anweisungen, Schaltflächen, Links und eine Dokumentationsseite zur Anleitung präsentieren.

*  Wenn Sie die Schaltfläche **Microsoft Edge Tools** in der **Aktivitätsleiste** von Visual Studio Code auswählen, enthält der Bereich **Microsoft Edge Extras: Ziele** jetzt erläuternden Text, Schaltflächen und Links, die Sie führen sollen, anstelle eines leeren Bereichs.

*  Wenn Sie eine neue Instanz von Microsoft Edge in Visual Studio Code öffnen, zeigt Microsoft Edge jetzt eine Startseite an, auf der erläutert wird, wie die Entwicklertools-Erweiterung anstelle einer leeren Seite verwendet wird.

*  Der Bereich **Microsoft Edge Tools: Targets** verfügt nun über eine Schaltfläche **"Generieren launch.js"** und Anweisungen, die Ihnen helfen, Ihr Projekt für das Debuggen in Microsoft Edge zu starten.

Navigieren Sie zu ["Verwenden der Tools",][GithubIoDevToolsUsing]um weitere Informationen zu erfahren.


## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]


### <a name="css-grid-editor"></a>CSS-Raster-Editor

Sie können jetzt css-Rasterlayouts in der Vorschau anzeigen und erstellen, indem Sie den neuen CSS-Raster-Editor verwenden.

Wenn ein HTML-Element auf Ihrer Seite darauf angewendet oder angewendet wurde, wird auf `display: grid` `display: inline-grid` der Registerkarte Formatvorlagen daneben ein Rastersymbol angezeigt. Klicken Sie auf das Rastersymbol, um den CSS-Raster-Editor anzuzeigen oder auszublenden. **** Wählen Sie im CSS-Raster-Editor eines der Symbole (z. B. ) aus, `justify-content: space-around` um eine Vorschau des Layouts auf der gerenderten Seite anzuzeigen.  Das Flex-Layout funktioniert ähnlich.

:::image type="complex" source="../../media/2021/05/css-grid-editor.msft.png" alt-text="CSS-Raster-Editor" lightbox="../../media/2021/05/css-grid-editor.msft.png":::
   CSS-Raster-Editor
:::image-end:::

<!-- screenshot uses https://jec.fyi -->

Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1203241][CR1203241].


### <a name="support-for-const-redeclarations-in-the-console"></a>Unterstützung für neu zu deklarierende Konstanten in der Konsole

Die Konsole unterstützt jetzt die erneute Deklarierung von `const` Variablen in separaten REPL-Skripts (z. B. beim Ausführen einer Anweisung in der Konsole) zusätzlich zu den vorhandenen `let` und neu zu `class` deklarieren.  Mit dieser Unterstützung können Sie mit verschiedenen Deklarationen für Variablen experimentieren, `const` ohne die Seite zu aktualisieren.  Bisher hat DevTools einen Syntaxfehler ausgegeben, wenn Sie eine Bindung neu `const` deklarieren.

Verweisen Sie auf das folgende Beispiel. `const` Die erneute Deklarierung wird über separate REPL-Skripts hinweg unterstützt (siehe `a` Variable).  Beachten Sie, dass die folgenden Szenarien entwurfsbedingt nicht unterstützt werden:

*  `const` Die erneute Deklarierung von Seitenskripts ist in REPL-Skripts nicht zulässig.
*  `const` Eine erneute Deklarierung innerhalb desselben REPL-Skripts ist nicht zulässig (siehe `b` Variable).

:::image type="complex" source="../../media/2021/05/support-for-const-redeclaration.msft.png" alt-text="Das erneute Deklarieren einer Konstantenvariablen ist in der Konsole zulässig." lightbox="../../media/2021/05/support-for-const-redeclaration.msft.png":::
   Das erneute Deklarieren einer Konstantenvariablen ist in der Konsole zulässig.
:::image-end:::

Um zu erfahren, wie Sie ein einzelnes REPL-Skript oder ein mehrzeiliges REPL-Skript ausführen, navigieren Sie zur [Konsole als JavaScript-Umgebung.](../../../console/console-javascript.md)
    
Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1076427][CR1076427].


### <a name="new-shortcut-to-view-iframe-details"></a>Neue Verknüpfung zum Anzeigen von iframe-Details

Um Details schnell `iframe` anzuzeigen, können Sie jetzt mit der rechten Maustaste auf ein Element im Elementtool klicken `iframe` und dann **iframedetails anzeigen**auswählen. ****

:::image type="complex" source="../../media/2021/05/show-iframe-details.msft.png" alt-text="iframe-Detailansicht" lightbox="../../media/2021/05/show-iframe-details.msft.png":::
   iframe-Detailansicht
:::image-end:::

Dadurch werden die Details zum `iframe` Anwendungstool angezeigt. ****  Im **Anwendungstool** können Sie Dokumentdetails, Sicherheits- und Isolationsstatus, Berechtigungsrichtlinien und vieles mehr untersuchen, um potenzielle Probleme zu debuggen.

:::image type="complex" source="../../media/2021/05/show-iframe-details-application-tool.msft.png" alt-text="Framedetails im Anwendungstool" lightbox="../../media/2021/05/show-iframe-details-application-tool.msft.png":::
   Framedetails im **Anwendungstool**
:::image-end:::

<!-- demo page: https://wolfib.github.io/web-demos/ esp https://wolfib.github.io/web-demos/jsIframe.html -->

Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1192084][CR1192084].


### <a name="enhanced-cors-debugging-support"></a>Erweiterte CORS-Debuggingunterstützung

CORS-Fehler (Cross-Origin Resource Sharing) werden nun auf der Registerkarte **"Probleme"** angezeigt.  Es gibt verschiedene mögliche Ursachen für CORS-Fehler.  Klicken Sie, um die einzelnen Probleme zu erweitern, um die möglichen Ursachen und Lösungen zu verstehen.

:::image type="complex" source="../../media/2021/05/cors-debugging-support.msft.png" alt-text="CORS-Probleme auf der Registerkarte "Probleme"" lightbox="../../media/2021/05/cors-debugging-support.msft.png":::
   CORS-Probleme auf der Registerkarte "Probleme"
:::image-end:::

<!-- screenshot uses http://cors-errors.glitch.me -->

Um den Verlauf dieses Features im Chromium Open Source-Projekt zu überprüfen, navigieren Sie zu Problem [1141824][CR1141824].


### <a name="renamed-xhr-filter-to-fetchxhr"></a>Umbenannter XHR-Filter in Fetch\/XHR

Im **Netzwerktool** wird der **XHR-Filter** jetzt in **Fetch/XHR**umbenannt. Diese Änderung verdeutlicht, dass dieser Filter sowohl API-Netzwerkanforderungen als auch `XMLHttpRequest` `Fetch` API-Netzwerkanforderungen enthält.

:::image type="complex" source="../../media/2021/05/fetch-xhr.msft.png" alt-text="Das Netzwerktool zeigt jetzt Fetch/XHR anstelle von XHR an." lightbox="../../media/2021/05/fetch-xhr.msft.png":::
   Das **Netzwerktool** zeigt jetzt **Fetch/XHR** anstelle von **XHR** an.
:::image-end:::

Navigieren Sie für weitere Informationen zu:
*  [XMLHttpRequest-Spezifikation][XhrSpecWhatwgOrg]
*  [Fetch-Spezifikation][FetchSpecWhatwgOrg]

Navigieren Sie zu Problem [1201398,][CR1201398]um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.


### <a name="filter-wasm-resource-type-in-the-network-tool"></a>Filtern des Wasm-Ressourcentyps im Netzwerktool

Im **Netzwerktool** können Sie nun den neuen **Wasm-Filter** auswählen, um die WebAssembly-Netzwerkanforderungen zu filtern.

:::image type="complex" source="../../media/2021/05/wasm-network-requests.msft.png" alt-text="Filtern nach Wasm" lightbox="../../media/2021/05/wasm-network-requests.msft.png":::
   Filtern nach Wasm
:::image-end:::

<!-- screenshot uses http://memory-inspector.glitch.me/demo-wasm.html -->

Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1103638][CR1103638].


### <a name="compute-intersections-are-now-included-in-the-performance-tool"></a>Compute-Schnittmengen sind jetzt im Leistungstool enthalten

Im **Tool "Leistung"** zeigt DevTools jetzt **Compute-Schnittmengen** im Diagramm an. Diese Änderungen helfen Ihnen bei der Identifizierung von Überschneidungsereignissen und beim Debuggen des potenziellen Leistungsaufwands von Schnittpunktbegegnungen.

:::image type="complex" source="../../media/2021/05/compute-intersections-in-perf-tool.msft.png" alt-text="Berechnen von Schnittmengen im Leistungstool" lightbox="../../media/2021/05/compute-intersections-in-perf-tool.msft.png":::
   Berechnen von Schnittmengen im **Leistungstool**
:::image-end:::

<!-- screenshot uses https://googlechrome.github.io/samples/intersectionobserver -->

Weitere Informationen zu Schnittmengenbetrachtern, navigieren Sie zu [Vertrauensstellung ist gut, Beobachtung ist besser: IntersectionSynktion v2][WebDevIntersectionObserverV2].  Um Informationen zur Verwendung des Diagramms zu suchen, navigieren Sie zu ["Analysieren einer Leistungsaufzeichnung".][DevtoolsEvaluatePerfRefAnalyzeAPerfRecording]  Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1199137][CR1199137].


## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle

Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]


<!-- links -->
[DevtoolsEvaluatePerfRefAnalyzeAPerfRecording]: ../../../evaluate-performance/reference.md#analyze-a-performance-recording "Analysieren einer Leistungsaufzeichnung | Microsoft-Dokumente"
<!-- external links -->
[XhrSpecWhatwgOrg]: https://xhr.spec.whatwg.org "XMLHttpRequest-Spezifikation | WHATWG"
[FetchSpecWhatwgOrg]: https://fetch.spec.whatwg.org "Fetch spec | WHATWG"

[WebDevIntersectionObserverV2]: https://web.dev/intersectionobserver-v2 "Vertrauen ist gut, Beobachtung ist besser: IntersectionSynktion v2 | web.dev"

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Verwenden der Tools | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace | Visual Studio Code"

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Entwicklertools für Visual Studio Code | Visual Studio Markt"

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge: Status des Plattform-| Youtube"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"
[CR1094406]: https://crbug.com/1094406 "Problem 1094406: Entwickler möchten eine Quellreihenfolgeanzeige | Chromium Fehler"
[CR1174299]: https://crbug.com/1174299 "Problem 1174299: UA-Clienthinweise beim Überschreiben der UA-Zeichenfolge über die Registerkarte &quot;Netzwerkbedingungen&quot; von Chrome DevTools | Chromium Fehler"
[CR1203241]: https://crbug.com/1203241 "Problem 1203241: CSS-Raster-Editor | Chromium Fehler"
[CR1076427]: https://crbug.com/1076427 "Problem 1076427: Die DevTools-Konsole sollte die erneute Deklarierung | Chromium Fehler"
[CR1192084]: https://crbug.com/1192084 "Problem 1192084: Hinzufügen der Option &quot;Framedetails anzeigen&quot; mit der rechten Maustaste zu iframe-/html-Tags in der Elementansicht | Chromium Fehler"
[CR1141824]: https://crbug.com/1141824 "Problem 1141824: Verbessern der CORS-Fehlerberichterstattung in DevTools | Chromium-Fehler"
[CR1201398]: https://crbug.com/1201398 "Problem 1201398: Featureanforderung: XHR-Typfilter im Netzwerkbereich umbenennen | Chromium Fehler"
[CR1103638]: https://crbug.com/1103638 "Problem 1103638: Netzwerkbereich zum Anzeigen von WebAssembly-Ressourcen | Chromium Fehler"
[CR1199137]: https://crbug.com/1199137 "Problem 1199137: Anzeigen von IntersectionObserver-Kosten im bereichsbasierten | Chromium Fehler"

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.
> Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-xx) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.

[ ![ Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
