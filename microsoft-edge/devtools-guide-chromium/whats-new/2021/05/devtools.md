---
description: Die Schaltfläche "Weitere Tools", die Kontextdokumentation für die ersten Schritte mit der DevTools-Erweiterung, die erweiterte Unterstützung für Bildschirmleseprogramme in der Konsole und vieles mehr.
title: Neuigkeiten in DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ebd512800b8e55b5e9c0001c314a7c08fd242d5d
ms.sourcegitcommit: 30817cd9ae187a716d14d06962eb23b32dd54548
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "11590867"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a>Neuigkeiten in DevTools (Microsoft Edge 92)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

> [!TIP]
> Die **Microsoft Build 2021-Konferenz** war vom 25. bis 27. Mai.  Hier ist ein Video von Build über die Updates für DevTools: [Microsoft Edge | Status der Plattform][YoutubeEdgeStateOfThePlatform] – Microsoft Edge bietet eine überzeugende und konsistente Plattform mit Tools für Entwickler.  Wenn der Support für unsere älteren Browser eingestellt wird, wird Edge in Kürze der einzige unterstützte Browser von Microsoft auf Windows 10 sein.  Nehmen Sie an uns teil, um mehr über die neuesten Informationen auf der Edge-Plattform, den Tools und Web-Apps zu erfahren.


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a>Die Schaltfläche "Schließen" ist nicht mehr ausgeblendet, wenn DevTools schmal ist

<!-- Title: DevTools is now easier to close -->  
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->  

In Microsoft Edge Version 91 oder früheren Versionen wird die Schaltfläche **"Schließen",** um DevTools zu schließen, nicht angezeigt, wenn der DevTools-Viewport schmal ist.  In Microsoft Edge Version 92 ist die Schaltfläche **"Schließen"** in den DevTools immer vorhanden, unabhängig von der Breite des DevTools-Viewports.

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="Die Schaltfläche DevTools schließen ist jetzt auch dann vorhanden, wenn der Viewport schmal ist." lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   Die Schaltfläche **"DevTools schließen"** ist jetzt auch dann vorhanden, wenn der Viewport schmal ist.  
:::image-end:::  


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a>Schnelles Hinzufügen von Tools mit der neuen Schaltfläche "Weitere Tools"

<!-- Title: Add tools quickly with the new More Tools button -->  
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->  

Es gibt eine neue Möglichkeit, weitere Tools in Microsoft Edge DevTools zu öffnen: das Menü **"Weitere Tools** ( `+` ) ". Das Menü **"Weitere Tools"** wird auf der Symbolleiste im Hauptbereich und auf der Symbolleiste der Schublade angezeigt. Wenn Sie ein Tool aus dem Menü **"Weitere Tools"** auswählen, wird das Tool zur Symbolleiste hinzugefügt.

Um die Registerkarten auf beiden Symbolleisten neu anzuordnen, wählen Sie die Registerkarten aus, und ziehen Sie sie.  

Das Menü **"Weitere Tools"** war in Microsoft Edge Version 89 als Experiment verfügbar und ist jetzt immer vorhanden.

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="Die Schaltfläche Weitere Tools auf der oberen Symbolleiste und der Schublade-Symbolleiste" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   Die Schaltfläche **"Weitere Tools"** auf der oberen Symbolleiste und der Schublade-Symbolleiste
:::image-end:::  

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Das Menü Weitere Tools" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
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

Vor Microsoft Edge Version 92 haben Hilfstechnologien wie Sprachausgabe in der **Konsole**keine Vorschläge zur automatischen Vervollständigung oder die Ergebnisse ausgewerteter Ausdrücke angekündigt. Dies wurde jetzt behoben.

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


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a>Microsoft Edge Entwicklertools für Visual Studio Code Version 1.1.8

Die [Microsoft Edge Developer Tools für Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Erweiterungsversion 1.1.8 für Microsoft Visual Studio Code weist seit der vorherigen Version die folgenden Änderungen auf.  Microsoft Visual Studio Code aktualisiert Erweiterungen automatisch.  Um die Version 1.1.8 manuell zu aktualisieren, navigieren Sie manuell zu ["Erweiterung aktualisieren".][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

Sie können Probleme melden und zur Erweiterung im [vscode-edge-devtools GitHub Repo][GithubMicrosoftVscodeEdgeDevtools]beitragen.  

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a>Kontextdokumentation und Benutzeroberfläche, um die Verwendung der DevTools-Erweiterung zu vereinfachen

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->  
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->  

Version 1.1.8 der [Microsoft Edge Developer Tools für Visual Studio Code-Erweiterung][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] bietet jetzt eine einfachere Möglichkeit, eine neue Instanz von Microsoft Edge zu starten, indem Anweisungen, Schaltflächen, Links und eine Dokumentationsseite zur Anleitung präsentiert werden.

*  Wenn Sie die Schaltfläche **Microsoft Edge Tools** in der **Aktivitätsleiste** von Visual Studio Code auswählen, werden im Bereich **Microsoft Edge Tools: Targets** nun erläuternder Text, Schaltflächen und Links zur Anleitung anstelle eines leeren Bereichs angezeigt.

*  Wenn Sie eine neue Instanz von Microsoft Edge in Visual Studio Code öffnen, zeigt Microsoft Edge jetzt eine Startseite an, auf der erläutert wird, wie die Entwicklertools-Erweiterung anstelle einer leeren Seite verwendet wird.

*  Der Bereich **Microsoft Edge Tools: Targets** verfügt jetzt über eine Schaltfläche **"Generieren launch.js"** und Anweisungen, um das Projekt zum Debuggen in Microsoft Edge zu starten.

Navigieren Sie zu ["Verwenden der Tools",][GithubIoDevToolsUsing]um weitere Informationen zu erfahren.


## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Verwenden der Tools | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Entwicklertools für Visual Studio Code | Visual Studio Markt"  

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge: Status des Plattform-| Youtube"

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
