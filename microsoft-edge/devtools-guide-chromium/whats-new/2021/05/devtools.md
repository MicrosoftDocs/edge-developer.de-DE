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
# <a name="whats-new-in-devtools-microsoft-edge-92"></a><span data-ttu-id="f4c04-104">Neuigkeiten in DevTools (Microsoft Edge 92)</span><span class="sxs-lookup"><span data-stu-id="f4c04-104">What's New In DevTools (Microsoft Edge 92)</span></span>

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]

> [!TIP]
> <span data-ttu-id="f4c04-105">Die **Microsoft Build 2021-Konferenz** war vom 25. bis 27. Mai.</span><span class="sxs-lookup"><span data-stu-id="f4c04-105">The **Microsoft Build 2021** conference was on May 25-27.</span></span>  <span data-ttu-id="f4c04-106">Hier ist ein Video von Build über die Updates für DevTools: [Microsoft Edge | Status der Plattform][YoutubeEdgeStateOfThePlatform] – Microsoft Edge bietet eine überzeugende und konsistente Plattform mit Tools für Entwickler.</span><span class="sxs-lookup"><span data-stu-id="f4c04-106">Here's a video from Build about the updates to DevTools: [Microsoft Edge | State of the Platform][YoutubeEdgeStateOfThePlatform] - Microsoft Edge brings a compelling and consistent platform with tools for developers.</span></span>  <span data-ttu-id="f4c04-107">Wenn der Support für unsere älteren Browser eingestellt wird, wird Edge in Kürze der einzige unterstützte Browser von Microsoft auf Windows 10 sein.</span><span class="sxs-lookup"><span data-stu-id="f4c04-107">As our legacy browsers phase out of support, Edge will soon be the only supported browser from Microsoft on Windows 10.</span></span>  <span data-ttu-id="f4c04-108">Nehmen Sie an uns teil, um mehr über die neuesten Informationen auf der Edge-Plattform, den Tools und Web-Apps zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="f4c04-108">Join us to learn about the latest across the Edge platform, tools, and web apps.</span></span>


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a><span data-ttu-id="f4c04-109">Die Schaltfläche "Schließen" ist nicht mehr ausgeblendet, wenn DevTools schmal ist</span><span class="sxs-lookup"><span data-stu-id="f4c04-109">The Close button is no longer hidden when DevTools is narrow</span></span>

<!-- Title: DevTools is now easier to close -->
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->

<span data-ttu-id="f4c04-110">In Microsoft Edge Version 91 oder früheren Versionen wird die Schaltfläche **"Schließen"** zum Schließen von DevTools nicht angezeigt, wenn der DevTools-Viewport schmal ist.</span><span class="sxs-lookup"><span data-stu-id="f4c04-110">In Microsoft Edge version 91 or earlier, the **Close** button to close DevTools isn't displayed when the DevTools viewport is narrow.</span></span>  <span data-ttu-id="f4c04-111">In Microsoft Edge Version 92 ist die Schaltfläche **"Schließen"** in den DevTools immer vorhanden, unabhängig von der Breite des DevTools-Viewports.</span><span class="sxs-lookup"><span data-stu-id="f4c04-111">In Microsoft Edge version 92, the **Close** button in the DevTools is always present, regardless of the DevTools viewport width.</span></span>

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="Die Schaltfläche "DevTools schließen" ist jetzt auch dann vorhanden, wenn der Viewport schmal ist." lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   <span data-ttu-id="f4c04-113">Die Schaltfläche **"DevTools schließen"** ist jetzt auch dann vorhanden, wenn der Viewport schmal ist.</span><span class="sxs-lookup"><span data-stu-id="f4c04-113">The **Close** DevTools button is now present even when the viewport is narrow</span></span>
:::image-end:::


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a><span data-ttu-id="f4c04-114">Schnelles Hinzufügen von Tools mit der neuen Schaltfläche "Weitere Tools"</span><span class="sxs-lookup"><span data-stu-id="f4c04-114">Add tools quickly with the new More Tools button</span></span>

<!-- Title: Add tools quickly with the new More Tools button -->
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->

<span data-ttu-id="f4c04-115">Es gibt eine neue Möglichkeit, weitere Tools in Microsoft Edge DevTools zu öffnen: das Menü **"Weitere Tools** ( `+` ) ".</span><span class="sxs-lookup"><span data-stu-id="f4c04-115">There's a new way to open more tools in Microsoft Edge DevTools: the **More Tools** (`+`) menu.</span></span> <span data-ttu-id="f4c04-116">Das Menü **"Weitere Tools"** wird auf der Symbolleiste im Hauptbereich und auf der Symbolleiste der Schublade angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f4c04-116">The **More Tools** menu appears on the toolbar in the main panel and on the toolbar of the drawer.</span></span> <span data-ttu-id="f4c04-117">Wenn Sie ein Tool aus dem Menü **"Weitere Tools"** auswählen, wird das Tool zur Symbolleiste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f4c04-117">Selecting a tool from the **More Tools** menu adds the tool to the toolbar.</span></span>

<span data-ttu-id="f4c04-118">Um die Registerkarten auf beiden Symbolleisten neu anzuordnen, wählen Sie die Registerkarten aus, und ziehen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="f4c04-118">To reorder the tabs on either toolbar, select and drag the tabs.</span></span>

<span data-ttu-id="f4c04-119">Das Menü **"Weitere Tools"** war in Microsoft Edge Version 89 als Experiment verfügbar und ist jetzt immer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f4c04-119">The **More Tools** menu was available as an experiment in Microsoft Edge version 89, and is now always present.</span></span>

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="Die Schaltfläche "Weitere Tools" auf der oberen Symbolleiste und der Schublade-Symbolleiste" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   <span data-ttu-id="f4c04-121">Die Schaltfläche **"Weitere Tools"** auf der oberen Symbolleiste und der Schublade-Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="f4c04-121">The **More Tools** button on the upper toolbar and drawer toolbar</span></span>
:::image-end:::

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Das Menü "Weitere Tools"" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   <span data-ttu-id="f4c04-123">Das Menü **"Weitere Tools"**</span><span class="sxs-lookup"><span data-stu-id="f4c04-123">The **More Tools** menu</span></span>
:::image-end:::


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a><span data-ttu-id="f4c04-124">Verbesserungen beim Zeigen, Auswählen und Schließen von Tools</span><span class="sxs-lookup"><span data-stu-id="f4c04-124">Improvements for hovering, selecting, and closing tools</span></span>

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

<span data-ttu-id="f4c04-125">Registerkarten für jedes Tool wurden neu formatiert, um die Wahrscheinlichkeit zu verringern, dass ein Tool versehentlich geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="f4c04-125">Tabs for each tool have been reformatted to reduce the chance of accidentally closing a tool.</span></span>  <span data-ttu-id="f4c04-126">Auf jeder Registerkarte in der Hauptsymbolleiste und in der Symbolleiste der Schublade haben wir Folgendes hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="f4c04-126">On each tab in the main toolbar and in the toolbar of the drawer, we added:</span></span>
*  <span data-ttu-id="f4c04-127">Abstand um die Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="f4c04-127">Spacing around the tab.</span></span>
*  <span data-ttu-id="f4c04-128">Abstand um die Schaltfläche "Schließen" `x` ()" auf der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="f4c04-128">Spacing around the close (`x`) button in the tab.</span></span>
*  <span data-ttu-id="f4c04-129">Eine Hintergrundfarbe beim Bewegen über die Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="f4c04-129">A background color when hovering over the tab.</span></span>
*  <span data-ttu-id="f4c04-130">Eine QuickInfo für die Schaltfläche zum Schließen ( `x` ) der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="f4c04-130">A tooltip for the close (`x`) button of the tab.</span></span>
*  <span data-ttu-id="f4c04-131">Höherer Kontrast für die Schaltfläche zum Schließen ( `x` ) der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="f4c04-131">Higher contrast for the close (`x`) button of the tab.</span></span>

<span data-ttu-id="f4c04-132">Wenn Sie sich beispielsweise im **Leistungstool** befinden und auf die Registerkarte des **Netzwerktools** zeigen, verhindern diese Verbesserungen das versehentliche Schließen des **Netzwerktools.**</span><span class="sxs-lookup"><span data-stu-id="f4c04-132">For example, when you are in the **Performance** tool and you hover over the **Network** tool's tab, these improvements help prevent accidentally closing the **Network** tool.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Registerkarten vor der Neuformatierung" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           <span data-ttu-id="f4c04-134">Registerkarten vor der Neuformatierung</span><span class="sxs-lookup"><span data-stu-id="f4c04-134">Tabs before reformatting</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Registerkarten nach der Neuformatierung" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           <span data-ttu-id="f4c04-136">Registerkarten nach der Neuformatierung</span><span class="sxs-lookup"><span data-stu-id="f4c04-136">Tabs after reformatting</span></span> :::image-end:::
    :::column-end:::
:::row-end:::

<span data-ttu-id="f4c04-137">Diese Verbesserungen sind besonders für Benutzer lokalisierter DevTools relevant, bei denen die Registerkarten möglicherweise schmaler sind und versehentlich leichter geschlossen werden können.</span><span class="sxs-lookup"><span data-stu-id="f4c04-137">These improvements are especially relevant for users of localized DevTools, in which the tabs may be narrower and easier to accidentally close.</span></span>

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="Lokalisierte DevTools mit schmalen Registerkarten" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   <span data-ttu-id="f4c04-139">Lokalisierte DevTools mit schmalen Registerkarten</span><span class="sxs-lookup"><span data-stu-id="f4c04-139">Localized DevTools with narrow tabs</span></span>
:::image-end:::

<span data-ttu-id="f4c04-140">Außerdem wurde es einfacher, ein Tool, das Sie geschlossen haben, erneut hinzuzufügen, indem ein [Menü "Weitere Tools"](#add-tools-quickly-with-the-new-more-tools-button) zur Hauptsymbolleiste und der Schublade-Symbolleiste hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f4c04-140">We also made it easier to re-add a tool that you closed by adding a [More Tools menu](#add-tools-quickly-with-the-new-more-tools-button) to the main toolbar and drawer toolbar.</span></span>


## <a name="better-support-for-screen-readers-in-the-console"></a><span data-ttu-id="f4c04-141">Bessere Unterstützung für Bildschirmleseprogramme in der Konsole</span><span class="sxs-lookup"><span data-stu-id="f4c04-141">Better support for screen readers in the Console</span></span>

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

<span data-ttu-id="f4c04-142">Vor Microsoft Edge Version 92 in der **Konsole**haben Hilfstechnologien wie Bildschirmleseprogramme keine Vorschläge zur automatischen Vervollständigung oder die Ergebnisse ausgewerteter Ausdrücke angekündigt.</span><span class="sxs-lookup"><span data-stu-id="f4c04-142">Prior to Microsoft Edge version 92, in the **Console**, assistive technologies such as screen readers didn't announce autocomplete suggestions or the results of evaluated expressions.</span></span> <span data-ttu-id="f4c04-143">Dies wurde jetzt behoben.</span><span class="sxs-lookup"><span data-stu-id="f4c04-143">This has been fixed now.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="In der Konsole kündigen Bildschirmleseprogramme jetzt den aktuell ausgewählten AutoVervollständigen-Vorschlag an." lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           <span data-ttu-id="f4c04-145">In der **Konsole**kündigen Bildschirmleseprogramme jetzt den aktuell ausgewählten Vorschlag für automatisches Vervollständigen an.</span><span class="sxs-lookup"><span data-stu-id="f4c04-145">In the **Console**, screen readers now announce the currently selected autocomplete suggestion</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="In der Konsole kündigen Bildschirmleseprogramme nun das Ergebnis eines ausgewerteten Ausdrucks an." lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           <span data-ttu-id="f4c04-147">In der **Konsole**kündigen Bildschirmleseprogramme nun das Ergebnis eines ausgewerteten Ausdrucks an.</span><span class="sxs-lookup"><span data-stu-id="f4c04-147">In the **Console**, screen readers now announce the result of an evaluated expression</span></span> :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="source-order-viewer"></a><span data-ttu-id="f4c04-148">Source Order Viewer</span><span class="sxs-lookup"><span data-stu-id="f4c04-148">Source Order Viewer</span></span>

<!--  Title: Source Order Viewer -->
<!--  Subtitle: The new Source Order Viewer displays numbers on the webpage indicating the order of page elements in the source file, independently of how the page sections are positioned by CSS. -->

<span data-ttu-id="f4c04-149">Sie können jetzt die Reihenfolge der Quellelemente anzeigen, die auf der gerenderten Webseite überlagert sind, um eine bessere Barrierefreiheitsüberprüfung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="f4c04-149">You can now view the order of source elements overlaid on the rendered webpage, for better accessibility inspection.</span></span>

<span data-ttu-id="f4c04-150">Die Reihenfolge der Inhalte in einem HTML-Dokument ist wichtig für die Optimierung und Barrierefreiheit der Suchmaschine.</span><span class="sxs-lookup"><span data-stu-id="f4c04-150">The order of content in an HTML document is important for search engine optimization and accessibility.</span></span>  <span data-ttu-id="f4c04-151">MIT CSS können Entwickler Inhalte erstellen, die in der Reihenfolge auf dem Bildschirm anders aussieht als die Reihenfolge im HTML-Quelldokument.</span><span class="sxs-lookup"><span data-stu-id="f4c04-151">CSS allows developers to create content that looks different in its on-screen order than the order in the HTML source document.</span></span>  <span data-ttu-id="f4c04-152">Dies ist ein Problem mit der Barrierefreiheit, da Die Benutzer der Sprachausgabe eine verwirrende Erfahrung erhalten könnten.</span><span class="sxs-lookup"><span data-stu-id="f4c04-152">This is an accessibility problem, because screen-reader users could get a confusing experience.</span></span>

:::image type="complex" source="../../media/2021/05/source-order-viewer.msft.png" alt-text="Durch Aktivieren des Viewers für die Quellreihenfolge wird die Reihenfolge der Elemente in der Quelle als Überlagerungen auf der Seite angezeigt." lightbox="../../media/2021/05/source-order-viewer.msft.png":::
   <span data-ttu-id="f4c04-154">Durch Aktivieren des Viewers für die **Quellreihenfolge** wird die Reihenfolge der Elemente in der Quelle als Überlagerungen auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f4c04-154">Activating the **Source Order Viewer** shows the order of the elements in the source as overlays on the page</span></span>
:::image-end:::

<span data-ttu-id="f4c04-155">Navigieren Sie für weitere Informationen zur [Unterstützung der Tastatur mithilfe des Viewers für die Quellreihenfolge.](../../../accessibility/test-tab-key-source-order-viewer.md)</span><span class="sxs-lookup"><span data-stu-id="f4c04-155">For more information, navigate to [Test keyboard support using the Source Order Viewer](../../../accessibility/test-tab-key-source-order-viewer.md).</span></span>

<span data-ttu-id="f4c04-156">Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1094406][CR1094406].</span><span class="sxs-lookup"><span data-stu-id="f4c04-156">To review the history of this feature in the Chromium open-source project, navigate to Issue [1094406][CR1094406].</span></span>


## <a name="user-agent-client-hints-for-devices-in-the-network-conditions-tab"></a><span data-ttu-id="f4c04-157">User-Agent Clienthinweise für Geräte auf der Registerkarte "Netzwerkbedingungen"</span><span class="sxs-lookup"><span data-stu-id="f4c04-157">User-Agent Client Hints for devices in the Network conditions tab</span></span>

<!--  Title: User-Agent Client Hints -->
<!--  Subtitle: Access information about a user's browser in an ergonomic way that preserves privacy. -->

<span data-ttu-id="f4c04-158">User-Agent Clienthinweise werden jetzt auf Geräte im **Feld "Benutzer-Agent"** im **Netzwerkbedingungentool** angewendet.</span><span class="sxs-lookup"><span data-stu-id="f4c04-158">User-Agent Client Hints are now applied for devices in the **User agent** field in the **Network conditions** tool.</span></span>  <span data-ttu-id="f4c04-159">User-Agent Clienthinweise sind eine neue Erweiterung der Client hints-API, mit der Sie auf eine einzigartige Weise auf Informationen über den Browser eines Benutzers zugreifen können, um den Datenschutz zu wahren.</span><span class="sxs-lookup"><span data-stu-id="f4c04-159">User-Agent Client Hints are a new expansion to the Client Hints API that enables you to access information about a user's browser in an ergonomic way that preserves privacy.</span></span>

:::image type="complex" source="../../media/2021/05/user-agent.msft.png" alt-text="Benutzer-Agent" lightbox="../../media/2021/05/user-agent.msft.png":::
   <span data-ttu-id="f4c04-161">Benutzer-Agent</span><span class="sxs-lookup"><span data-stu-id="f4c04-161">User agent</span></span>
:::image-end:::

<span data-ttu-id="f4c04-162">Navigieren Sie zu [Benutzer-Agent-Clienthinweisen,](../../../../web-platform/user-agent-guidance.md#user-agent-client-hints)um weitere Informationen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="f4c04-162">For more information, navigate to [User-Agent Client Hints](../../../../web-platform/user-agent-guidance.md#user-agent-client-hints).</span></span>

<span data-ttu-id="f4c04-163">Navigieren Sie zu Problem 1174299, um den Verlauf dieses Features im open-source-Projekt [Chromium][CR1174299]zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f4c04-163">To review the history of this feature in the Chromium open-source project, navigate to Issue [1174299][CR1174299].</span></span>


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a><span data-ttu-id="f4c04-164">Microsoft Edge Entwicklertools für Visual Studio Code Version 1.1.8</span><span class="sxs-lookup"><span data-stu-id="f4c04-164">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.8</span></span>

<span data-ttu-id="f4c04-165">Die [Microsoft Edge Developer Tools für Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Erweiterungsversion 1.1.8 für Microsoft Visual Studio Code weist seit der vorherigen Version die folgenden Änderungen auf.</span><span class="sxs-lookup"><span data-stu-id="f4c04-165">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.8 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="f4c04-166">Microsoft Visual Studio Code aktualisiert Erweiterungen automatisch.</span><span class="sxs-lookup"><span data-stu-id="f4c04-166">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="f4c04-167">Um die Version 1.1.8 manuell zu aktualisieren, navigieren Sie manuell zu ["Erweiterung aktualisieren".][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="f4c04-167">To manually update to version 1.1.8, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>

<span data-ttu-id="f4c04-168">Sie können Probleme melden und an der Erweiterung im [vscode-edge-devtools GitHub Repo][GithubMicrosoftVscodeEdgeDevtools]mitwirken.</span><span class="sxs-lookup"><span data-stu-id="f4c04-168">You can file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a><span data-ttu-id="f4c04-169">Kontextdokumentation und Benutzeroberfläche, um die Verwendung der DevTools-Erweiterung zu vereinfachen</span><span class="sxs-lookup"><span data-stu-id="f4c04-169">In-context documentation and UI to make it easier to use the DevTools extension</span></span>

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->

<span data-ttu-id="f4c04-170">Version 1.1.8 der [Microsoft Edge Developer Tools für Visual Studio Code-Erweiterung][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] bietet jetzt eine einfachere Möglichkeit, eine neue Instanz von Microsoft Edge zu starten, indem Sie Anweisungen, Schaltflächen, Links und eine Dokumentationsseite zur Anleitung präsentieren.</span><span class="sxs-lookup"><span data-stu-id="f4c04-170">Version 1.1.8 of the [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension now features a simpler way to start a new instance of Microsoft Edge, by presenting instructions, buttons, links, and a documentation page to guide you.</span></span>

*  <span data-ttu-id="f4c04-171">Wenn Sie die Schaltfläche **Microsoft Edge Tools** in der **Aktivitätsleiste** von Visual Studio Code auswählen, enthält der Bereich **Microsoft Edge Extras: Ziele** jetzt erläuternden Text, Schaltflächen und Links, die Sie führen sollen, anstelle eines leeren Bereichs.</span><span class="sxs-lookup"><span data-stu-id="f4c04-171">When you select the **Microsoft Edge Tools** button in the **Activity Bar** of Visual Studio Code, the **Microsoft Edge Tools: Targets** panel now presents explanatory text, buttons, and links to guide you, instead of a blank panel.</span></span>

*  <span data-ttu-id="f4c04-172">Wenn Sie eine neue Instanz von Microsoft Edge in Visual Studio Code öffnen, zeigt Microsoft Edge jetzt eine Startseite an, auf der erläutert wird, wie die Entwicklertools-Erweiterung anstelle einer leeren Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4c04-172">When you open a new instance of Microsoft Edge from within Visual Studio Code, Microsoft Edge now shows a start page that explains how to use the Developer Tools extension, instead of a blank page.</span></span>

*  <span data-ttu-id="f4c04-173">Der Bereich **Microsoft Edge Tools: Targets** verfügt nun über eine Schaltfläche **"Generieren launch.js"** und Anweisungen, die Ihnen helfen, Ihr Projekt für das Debuggen in Microsoft Edge zu starten.</span><span class="sxs-lookup"><span data-stu-id="f4c04-173">The **Microsoft Edge Tools: Targets** panel now has a **Generate launch.json** button and instructions, to help launch your project for debugging in Microsoft Edge.</span></span>

<span data-ttu-id="f4c04-174">Navigieren Sie zu ["Verwenden der Tools",][GithubIoDevToolsUsing]um weitere Informationen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="f4c04-174">For more information, navigate to [Using the tools][GithubIoDevToolsUsing].</span></span>


## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="f4c04-175">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="f4c04-175">Announcements from the Chromium project</span></span>

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]


### <a name="css-grid-editor"></a><span data-ttu-id="f4c04-176">CSS-Raster-Editor</span><span class="sxs-lookup"><span data-stu-id="f4c04-176">CSS Grid editor</span></span>

<span data-ttu-id="f4c04-177">Sie können jetzt css-Rasterlayouts in der Vorschau anzeigen und erstellen, indem Sie den neuen CSS-Raster-Editor verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4c04-177">You can now preview and author CSS Grid layouts, using the new CSS Grid editor.</span></span>

<span data-ttu-id="f4c04-178">Wenn ein HTML-Element auf Ihrer Seite darauf angewendet oder angewendet wurde, wird auf `display: grid` `display: inline-grid` der Registerkarte Formatvorlagen daneben ein Rastersymbol angezeigt. Klicken Sie auf das Rastersymbol, um den CSS-Raster-Editor anzuzeigen oder auszublenden. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f4c04-178">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a grid icon is displayed next to it in the **Styles** tab. Click the grid icon to display or hide the CSS grid editor.</span></span> <span data-ttu-id="f4c04-179">Wählen Sie im CSS-Raster-Editor eines der Symbole (z. B. ) aus, `justify-content: space-around` um eine Vorschau des Layouts auf der gerenderten Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f4c04-179">In the CSS grid editor, select any of the icons (such as `justify-content: space-around`) to preview the layout in the rendered page.</span></span>  <span data-ttu-id="f4c04-180">Das Flex-Layout funktioniert ähnlich.</span><span class="sxs-lookup"><span data-stu-id="f4c04-180">Flex layout works similarly.</span></span>

:::image type="complex" source="../../media/2021/05/css-grid-editor.msft.png" alt-text="CSS-Raster-Editor" lightbox="../../media/2021/05/css-grid-editor.msft.png":::
   <span data-ttu-id="f4c04-182">CSS-Raster-Editor</span><span class="sxs-lookup"><span data-stu-id="f4c04-182">CSS Grid editor</span></span>
:::image-end:::

<!-- screenshot uses https://jec.fyi -->

<span data-ttu-id="f4c04-183">Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1203241][CR1203241].</span><span class="sxs-lookup"><span data-stu-id="f4c04-183">To review the history of this feature in the Chromium open-source project, navigate to Issue [1203241][CR1203241].</span></span>


### <a name="support-for-const-redeclarations-in-the-console"></a><span data-ttu-id="f4c04-184">Unterstützung für neu zu deklarierende Konstanten in der Konsole</span><span class="sxs-lookup"><span data-stu-id="f4c04-184">Support for const redeclarations in the Console</span></span>

<span data-ttu-id="f4c04-185">Die Konsole unterstützt jetzt die erneute Deklarierung von `const` Variablen in separaten REPL-Skripts (z. B. beim Ausführen einer Anweisung in der Konsole) zusätzlich zu den vorhandenen `let` und neu zu `class` deklarieren.</span><span class="sxs-lookup"><span data-stu-id="f4c04-185">The Console now supports redeclaration of `const` variables across separate REPL scripts (such as when you run a statement in the Console), in addition to the existing `let` and `class` redeclarations.</span></span>  <span data-ttu-id="f4c04-186">Mit dieser Unterstützung können Sie mit verschiedenen Deklarationen für Variablen experimentieren, `const` ohne die Seite zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f4c04-186">This support allows you to experiment with different declarations for `const` variables without refreshing the page.</span></span>  <span data-ttu-id="f4c04-187">Bisher hat DevTools einen Syntaxfehler ausgegeben, wenn Sie eine Bindung neu `const` deklarieren.</span><span class="sxs-lookup"><span data-stu-id="f4c04-187">Previously, DevTools threw a syntax error if you redeclared a `const` binding.</span></span>

<span data-ttu-id="f4c04-188">Verweisen Sie auf das folgende Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f4c04-188">Refer to the example below.</span></span> `const` <span data-ttu-id="f4c04-189">Die erneute Deklarierung wird über separate REPL-Skripts hinweg unterstützt (siehe `a` Variable).</span><span class="sxs-lookup"><span data-stu-id="f4c04-189">redeclaration is supported across separate REPL scripts (refer to variable `a`).</span></span>  <span data-ttu-id="f4c04-190">Beachten Sie, dass die folgenden Szenarien entwurfsbedingt nicht unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="f4c04-190">Note that the following scenarios are not supported, by design:</span></span>

*  `const` <span data-ttu-id="f4c04-191">Die erneute Deklarierung von Seitenskripts ist in REPL-Skripts nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="f4c04-191">redeclaration of page scripts is not allowed in REPL scripts.</span></span>
*  `const` <span data-ttu-id="f4c04-192">Eine erneute Deklarierung innerhalb desselben REPL-Skripts ist nicht zulässig (siehe `b` Variable).</span><span class="sxs-lookup"><span data-stu-id="f4c04-192">redeclaration within the same REPL script is not allowed (refer to variable `b`).</span></span>

:::image type="complex" source="../../media/2021/05/support-for-const-redeclaration.msft.png" alt-text="Das erneute Deklarieren einer Konstantenvariablen ist in der Konsole zulässig." lightbox="../../media/2021/05/support-for-const-redeclaration.msft.png":::
   <span data-ttu-id="f4c04-194">Das erneute Deklarieren einer Konstantenvariablen ist in der Konsole zulässig.</span><span class="sxs-lookup"><span data-stu-id="f4c04-194">Redeclaring a const variable is allowed in the console</span></span>
:::image-end:::

<span data-ttu-id="f4c04-195">Um zu erfahren, wie Sie ein einzelnes REPL-Skript oder ein mehrzeiliges REPL-Skript ausführen, navigieren Sie zur [Konsole als JavaScript-Umgebung.](../../../console/console-javascript.md)</span><span class="sxs-lookup"><span data-stu-id="f4c04-195">To learn how to run a single REPL script or a multi-line REPL script, navigate to [The Console as a JavaScript environment](../../../console/console-javascript.md).</span></span>
    
<span data-ttu-id="f4c04-196">Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1076427][CR1076427].</span><span class="sxs-lookup"><span data-stu-id="f4c04-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1076427][CR1076427].</span></span>


### <a name="new-shortcut-to-view-iframe-details"></a><span data-ttu-id="f4c04-197">Neue Verknüpfung zum Anzeigen von iframe-Details</span><span class="sxs-lookup"><span data-stu-id="f4c04-197">New shortcut to view iframe details</span></span>

<span data-ttu-id="f4c04-198">Um Details schnell `iframe` anzuzeigen, können Sie jetzt mit der rechten Maustaste auf ein Element im Elementtool klicken `iframe` und dann **iframedetails anzeigen**auswählen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f4c04-198">To quickly view `iframe` details, you can now right-click an `iframe` element in the **Elements** tool, and then select **Show iframe details**.</span></span>

:::image type="complex" source="../../media/2021/05/show-iframe-details.msft.png" alt-text="iframe-Detailansicht" lightbox="../../media/2021/05/show-iframe-details.msft.png":::
   <span data-ttu-id="f4c04-200">iframe-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="f4c04-200">iframe details view</span></span>
:::image-end:::

<span data-ttu-id="f4c04-201">Dadurch werden die Details zum `iframe` Anwendungstool angezeigt. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f4c04-201">This displays the details about the `iframe` in the **Application** tool.</span></span>  <span data-ttu-id="f4c04-202">Im **Anwendungstool** können Sie Dokumentdetails, Sicherheits- und Isolationsstatus, Berechtigungsrichtlinien und vieles mehr untersuchen, um potenzielle Probleme zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="f4c04-202">In the **Application** tool, you can examine document details, security and isolation status, permissions policy, and more, to debug potential issues.</span></span>

:::image type="complex" source="../../media/2021/05/show-iframe-details-application-tool.msft.png" alt-text="Framedetails im Anwendungstool" lightbox="../../media/2021/05/show-iframe-details-application-tool.msft.png":::
   <span data-ttu-id="f4c04-204">Framedetails im **Anwendungstool**</span><span class="sxs-lookup"><span data-stu-id="f4c04-204">Frame details in the **Application** tool</span></span>
:::image-end:::

<!-- demo page: https://wolfib.github.io/web-demos/ esp https://wolfib.github.io/web-demos/jsIframe.html -->

<span data-ttu-id="f4c04-205">Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1192084][CR1192084].</span><span class="sxs-lookup"><span data-stu-id="f4c04-205">To review the history of this feature in the Chromium open-source project, navigate to Issue [1192084][CR1192084].</span></span>


### <a name="enhanced-cors-debugging-support"></a><span data-ttu-id="f4c04-206">Erweiterte CORS-Debuggingunterstützung</span><span class="sxs-lookup"><span data-stu-id="f4c04-206">Enhanced CORS debugging support</span></span>

<span data-ttu-id="f4c04-207">CORS-Fehler (Cross-Origin Resource Sharing) werden nun auf der Registerkarte **"Probleme"** angezeigt.  Es gibt verschiedene mögliche Ursachen für CORS-Fehler.</span><span class="sxs-lookup"><span data-stu-id="f4c04-207">Cross-origin resource sharing (CORS) errors are now surfaced in the **Issues** tab.  There are various potential causes of CORS errors.</span></span>  <span data-ttu-id="f4c04-208">Klicken Sie, um die einzelnen Probleme zu erweitern, um die möglichen Ursachen und Lösungen zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="f4c04-208">Click to expand each issue to understand the potential causes and solutions.</span></span>

:::image type="complex" source="../../media/2021/05/cors-debugging-support.msft.png" alt-text="CORS-Probleme auf der Registerkarte "Probleme"" lightbox="../../media/2021/05/cors-debugging-support.msft.png":::
   <span data-ttu-id="f4c04-210">CORS-Probleme auf der Registerkarte "Probleme"</span><span class="sxs-lookup"><span data-stu-id="f4c04-210">CORS issues in the Issues tab</span></span>
:::image-end:::

<!-- screenshot uses http://cors-errors.glitch.me -->

<span data-ttu-id="f4c04-211">Um den Verlauf dieses Features im Chromium Open Source-Projekt zu überprüfen, navigieren Sie zu Problem [1141824][CR1141824].</span><span class="sxs-lookup"><span data-stu-id="f4c04-211">To review the history of this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>


### <a name="renamed-xhr-filter-to-fetchxhr"></a><span data-ttu-id="f4c04-212">Umbenannter XHR-Filter in Fetch\/XHR</span><span class="sxs-lookup"><span data-stu-id="f4c04-212">Renamed XHR filter to Fetch\/XHR</span></span>

<span data-ttu-id="f4c04-213">Im **Netzwerktool** wird der **XHR-Filter** jetzt in **Fetch/XHR**umbenannt.</span><span class="sxs-lookup"><span data-stu-id="f4c04-213">In the **Network** tool, the **XHR** filter is now renamed to **Fetch/XHR**.</span></span> <span data-ttu-id="f4c04-214">Diese Änderung verdeutlicht, dass dieser Filter sowohl API-Netzwerkanforderungen als auch `XMLHttpRequest` `Fetch` API-Netzwerkanforderungen enthält.</span><span class="sxs-lookup"><span data-stu-id="f4c04-214">This change makes it clearer that this filter includes both `XMLHttpRequest` and `Fetch` API network requests.</span></span>

:::image type="complex" source="../../media/2021/05/fetch-xhr.msft.png" alt-text="Das Netzwerktool zeigt jetzt Fetch/XHR anstelle von XHR an." lightbox="../../media/2021/05/fetch-xhr.msft.png":::
   <span data-ttu-id="f4c04-216">Das **Netzwerktool** zeigt jetzt **Fetch/XHR** anstelle von **XHR** an.</span><span class="sxs-lookup"><span data-stu-id="f4c04-216">The **Network** tool now shows **Fetch/XHR** instead of **XHR**</span></span>
:::image-end:::

<span data-ttu-id="f4c04-217">Navigieren Sie für weitere Informationen zu:</span><span class="sxs-lookup"><span data-stu-id="f4c04-217">For more information, navigate to:</span></span>
*  [<span data-ttu-id="f4c04-218">XMLHttpRequest-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="f4c04-218">XMLHttpRequest spec</span></span>][XhrSpecWhatwgOrg]
*  [<span data-ttu-id="f4c04-219">Fetch-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="f4c04-219">Fetch spec</span></span>][FetchSpecWhatwgOrg]

<span data-ttu-id="f4c04-220">Navigieren Sie zu Problem [1201398,][CR1201398]um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f4c04-220">To review the history of this feature in the Chromium open-source project, navigate to Issue [1201398][CR1201398].</span></span>


### <a name="filter-wasm-resource-type-in-the-network-tool"></a><span data-ttu-id="f4c04-221">Filtern des Wasm-Ressourcentyps im Netzwerktool</span><span class="sxs-lookup"><span data-stu-id="f4c04-221">Filter Wasm resource type in the Network tool</span></span>

<span data-ttu-id="f4c04-222">Im **Netzwerktool** können Sie nun den neuen **Wasm-Filter** auswählen, um die WebAssembly-Netzwerkanforderungen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="f4c04-222">In the **Network** tool, you can now select the new **Wasm** filter to filter the WebAssembly network requests.</span></span>

:::image type="complex" source="../../media/2021/05/wasm-network-requests.msft.png" alt-text="Filtern nach Wasm" lightbox="../../media/2021/05/wasm-network-requests.msft.png":::
   <span data-ttu-id="f4c04-224">Filtern nach Wasm</span><span class="sxs-lookup"><span data-stu-id="f4c04-224">Filter by Wasm</span></span>
:::image-end:::

<!-- screenshot uses http://memory-inspector.glitch.me/demo-wasm.html -->

<span data-ttu-id="f4c04-225">Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1103638][CR1103638].</span><span class="sxs-lookup"><span data-stu-id="f4c04-225">To review the history of this feature in the Chromium open-source project, navigate to Issue [1103638][CR1103638].</span></span>


### <a name="compute-intersections-are-now-included-in-the-performance-tool"></a><span data-ttu-id="f4c04-226">Compute-Schnittmengen sind jetzt im Leistungstool enthalten</span><span class="sxs-lookup"><span data-stu-id="f4c04-226">Compute Intersections are now included in the Performance tool</span></span>

<span data-ttu-id="f4c04-227">Im **Tool "Leistung"** zeigt DevTools jetzt **Compute-Schnittmengen** im Diagramm an.</span><span class="sxs-lookup"><span data-stu-id="f4c04-227">In the **Performance** tool, DevTools now displays **Compute Intersections** in the flame chart.</span></span> <span data-ttu-id="f4c04-228">Diese Änderungen helfen Ihnen bei der Identifizierung von Überschneidungsereignissen und beim Debuggen des potenziellen Leistungsaufwands von Schnittpunktbegegnungen.</span><span class="sxs-lookup"><span data-stu-id="f4c04-228">These changes help you identify intersection observers events and debug the potential performance overhead of intersection observers.</span></span>

:::image type="complex" source="../../media/2021/05/compute-intersections-in-perf-tool.msft.png" alt-text="Berechnen von Schnittmengen im Leistungstool" lightbox="../../media/2021/05/compute-intersections-in-perf-tool.msft.png":::
   <span data-ttu-id="f4c04-230">Berechnen von Schnittmengen im **Leistungstool**</span><span class="sxs-lookup"><span data-stu-id="f4c04-230">Compute Intersections in the **Performance** tool</span></span>
:::image-end:::

<!-- screenshot uses https://googlechrome.github.io/samples/intersectionobserver -->

<span data-ttu-id="f4c04-231">Weitere Informationen zu Schnittmengenbetrachtern, navigieren Sie zu [Vertrauensstellung ist gut, Beobachtung ist besser: IntersectionSynktion v2][WebDevIntersectionObserverV2].</span><span class="sxs-lookup"><span data-stu-id="f4c04-231">For more about intersection observers, navigate to [Trust is good, observation is better: Intersection Observer v2][WebDevIntersectionObserverV2].</span></span>  <span data-ttu-id="f4c04-232">Um Informationen zur Verwendung des Diagramms zu suchen, navigieren Sie zu ["Analysieren einer Leistungsaufzeichnung".][DevtoolsEvaluatePerfRefAnalyzeAPerfRecording]</span><span class="sxs-lookup"><span data-stu-id="f4c04-232">For information about using the flame chart, navigate to [Analyze a performance recording][DevtoolsEvaluatePerfRefAnalyzeAPerfRecording].</span></span>  <span data-ttu-id="f4c04-233">Um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen, navigieren Sie zu Problem [1199137][CR1199137].</span><span class="sxs-lookup"><span data-stu-id="f4c04-233">To review the history of this feature in the Chromium open-source project, navigate to Issue [1199137][CR1199137].</span></span>


## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="f4c04-234">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="f4c04-234">Download the Microsoft Edge preview channels</span></span>

<span data-ttu-id="f4c04-235">Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4c04-235">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="f4c04-236">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="f4c04-236">The preview channels give you access to the latest DevTools features.</span></span>


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="f4c04-237">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="f4c04-237">Getting in touch with Microsoft Edge DevTools team</span></span>

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
> <span data-ttu-id="f4c04-258">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4c04-258">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>
> <span data-ttu-id="f4c04-259">Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-xx) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="f4c04-259">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-xx) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>

<span data-ttu-id="f4c04-260">[ ![ Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f4c04-260">[![Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
