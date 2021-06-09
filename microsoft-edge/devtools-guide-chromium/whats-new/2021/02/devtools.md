---
description: Debugging-Unterstützung für CSS Flexbox, Anzeige zum Leistungs-Heads-up auf der Webseite, Problem von Tool-Updates und mehr
title: Neuigkeiten in DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.localizationpriority: high
ms.openlocfilehash: a13c344bb31cdfb7d0402132e3be82e4c330c612
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597166"
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
# <a name="whats-new-in-devtools-microsoft-edge-90"></a><span data-ttu-id="5c4a7-104">Neuigkeiten in DevTools (Microsoft Edge 90)</span><span class="sxs-lookup"><span data-stu-id="5c4a7-104">What's New In DevTools (Microsoft Edge 90)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a><span data-ttu-id="5c4a7-105">Gruppieren von Tools im Fokusmodus</span><span class="sxs-lookup"><span data-stu-id="5c4a7-105">Group tools together in Focus Mode</span></span>  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

<span data-ttu-id="5c4a7-106">Der Fokusmodus ist eine experimentelle Oberfläche, mit der Sie verschiedene Tools basierend auf Ihren eigenen Debugging-Szenarien gruppieren können.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-106">Focus Mode is an experimental interface that allows you to group different tools together based on your own debugging scenarios.</span></span>  <span data-ttu-id="5c4a7-107">Die neue **Aktivitätsleiste,** auf der linken Seite enthält vordefinierte Toolgruppen wie **Layout** und **Debugging.**</span><span class="sxs-lookup"><span data-stu-id="5c4a7-107">The new **Activity Bar** displayed on the left includes predefined tool groups such as **Layout** and **Debugging**.</span></span>  <span data-ttu-id="5c4a7-108">Um jede Toolgruppe anzupassen, schließen Sie Tools  mit dem Symbol **Schließen** \(`X`\) oder fügen Sie neue Tools mit dem Symbol **Weitere Tools** \(`+`\) hinzu.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-108">To customize each tool group, close tools with the **Close** \(`X`\) icon or add new tools with the **More tools** \(`+`\) icon.</span></span>  

<span data-ttu-id="5c4a7-109">Um das Experiment einzuschalten, navigieren Sie zu [Experimentelle Features aktivieren][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] und aktivieren Sie die Kontrollkästchen neben **Fokusmodus und DevTools-QuickInfos** sowie **Registerkartenmenüs Aktivieren + zum Öffnen weiterer Tools**.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-109">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="5c4a7-110">Für weitere Informationen zu dieser Funktion oder um Kommentare mit Fragen und Ideen abzugeben, navigieren Sie zu [DevTools: UI-Fokusmodus][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-110">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Anzeigen der Aktivitätsleiste" lightbox="../../media/2021/02/focus-mode.msft.png":::
   <span data-ttu-id="5c4a7-112">Anzeigen der **Aktivitätsleiste**</span><span class="sxs-lookup"><span data-stu-id="5c4a7-112">Display the **Activity Bar**</span></span>  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="5c4a7-113">Mehr über DevTools mit informativen QuickInfos erfahren</span><span class="sxs-lookup"><span data-stu-id="5c4a7-113">Learn about DevTools with informative tooltips</span></span>  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

<span data-ttu-id="5c4a7-114">Das DevTools-QuickInfos-Feature hilft Ihnen, mehr über alle verschiedenen Tools und Bereiche zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-114">The DevTools Tooltips feature helps you learn about all the different tools and panes.</span></span>  <span data-ttu-id="5c4a7-115">Wählen Sie das Symbol Hilfe \(`?`\) unten in der **Aktivitätsleiste**, um die QuickInfos in den DevTools umzuschalten.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-115">Choose the Help \(`?`\) icon at the bottom of the **Activity Bar** to toggle tooltips in the DevTools.</span></span>  <span data-ttu-id="5c4a7-116">Wenn die QuickInfos aktiviert sind, bewegen Sie den Mauszeiger über die einzelnen umrissenen Bereiche von DevTools, um weitere Informationen zur Verwendung des Tools zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-116">When tooltips are on, hover over each outlined region of DevTools to learn more about how to use the tool.</span></span>  <span data-ttu-id="5c4a7-117">Um das Experiment einzuschalten, navigieren Sie zu [Experimentelle Features aktivieren][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] und aktivieren Sie die Kontrollkästchen neben **Fokusmodus und DevTools-QuickInfos** sowie **Registerkartenmenüs Aktivieren + zum Öffnen weiterer Tools**.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-117">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="5c4a7-118">Für weitere Informationen zu dieser Funktion oder um Kommentare mit Fragen und Ideen einzureichen, navigieren Sie zu [DevTools: UI-Fokusmodus][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-118">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Auswählen des Hilfesymbols (?) In der Aktivitätsleiste, um QuickInfos anzuzeigen" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   <span data-ttu-id="5c4a7-120">Wählen Sie das Symbol Hilfe \(`?`\) in der **Aktivitätsleiste** aus, um QuickInfos anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-120">Choose the Help \(`?`\) icon in the **Activity Bar** to display tooltips</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="5c4a7-121">Anpassen von Tastaturkürzeln in den Einstellungen</span><span class="sxs-lookup"><span data-stu-id="5c4a7-121">Customize keyboard shortcuts in Settings</span></span>  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

<span data-ttu-id="5c4a7-122">Sie können die Tastenkombination nun für jede Aktion in den DevTools anpassen.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-122">You may now customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="5c4a7-123">Führen Sie die folgenden Aktionen aus, um eine Tastenkombination zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-123">To edit a keyboard shortcut, complete the following actions.</span></span>  

1.  <span data-ttu-id="5c4a7-124">Öffnen Sie die DevTools, und wählen Sie dann **Einstellungen**  >  **Verknüpfungen** aus.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-124">Open the DevTools, and then choose **Settings** > **Shortcuts**.</span></span>  
1.  <span data-ttu-id="5c4a7-125">Wählen Sie die Aktion aus, die Sie anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-125">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="5c4a7-126">Wählen Sie das Bearbeiten \(</span><span class="sxs-lookup"><span data-stu-id="5c4a7-126">Choose the Edit \(</span></span>![Tastenkombinationssymbol "Bearbeiten"](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)<span data-ttu-id="5c4a7-128">\) -Symbol.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-128">\) icon.</span></span>  
1.  <span data-ttu-id="5c4a7-129">Wählen Sie die Schlüssel aus, die Sie an die Aktion binden möchten.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-129">Select the keys you want to bind to the action.</span></span>  
1.  <span data-ttu-id="5c4a7-130">Aktivieren Sie das Häkchen \(</span><span class="sxs-lookup"><span data-stu-id="5c4a7-130">Choose the checkmark \(</span></span>![Tastenkombinationssymbol "Häkchen"](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="5c4a7-132">\) -Symbol.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-132">\) icon.</span></span>  
    
<span data-ttu-id="5c4a7-133">Weitere Informationen zum Anpassen und Bearbeiten von Verknüpfungen finden Sie unter [Anpassen von Tastaturkürzeln in den Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-133">For more information about customizing and editing shortcuts, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="5c4a7-134">Um Echtzeitaktualisierungen dieses Features im Open Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-134">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Anpassen von Tastenkombinationen in den DevTools-Einstellungen für Verknüpfungen mit einer Verknüpfung im Bearbeitungsmodus" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   <span data-ttu-id="5c4a7-136">Anpassen von Tastenkombinationen in den [DevTools-Einstellungen][DevtoolsCustomizeIndexSettings] für Verknüpfungen mit einer Verknüpfung im Bearbeitungsmodus</span><span class="sxs-lookup"><span data-stu-id="5c4a7-136">Customize keyboard shortcuts in the [DevTools Settings][DevtoolsCustomizeIndexSettings] on Shortcuts with a shortcut in edit mode</span></span>  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a><span data-ttu-id="5c4a7-137">Microsoft Edge DevTools für Visual Studio Codeerweiterungsupdate 1.1.4</span><span class="sxs-lookup"><span data-stu-id="5c4a7-137">Microsoft Edge DevTools for Visual Studio Code extension update 1.1.4</span></span>  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

<span data-ttu-id="5c4a7-138">Die [Microsoft Edge Developer Tools für Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] -Erweiterung Version 1.1.4 für Microsoft Visual Studio Code zeigt jetzt neben jeder DevTools-Instanz ein Favicon an.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-138">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.4 for Microsoft Visual Studio Code now displays a favicon next to each of the DevTools instances.</span></span>  <span data-ttu-id="5c4a7-139">Konsolennachrichten von Microsoft Edge werden jetzt in der **DevTools-Konsole** unter **Problem** von Microsoft Visual Studio-Code angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-139">Console messages from Microsoft Edge now display in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  <span data-ttu-id="5c4a7-140">Microsoft Visual Studio Code aktualisiert Erweiterungen automatisch.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-140">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="5c4a7-141">Navigieren Sie zum manuellen Aktualisieren auf Version 1.1.4 zu [Manuelles Aktualisieren einer Erweiterung][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-141">To manually update to version 1.1.4, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="5c4a7-142">Sie können Probleme einreichen und zur Erweiterung des GitHub-Repos [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools] beitragen.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-142">You may file issues and contribute to the extension on the [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools] GitHub repo.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5c4a7-143">In der folgenden Abbildung werden Nachrichten von einer Beispielwebseite angezeigt, die im **Konsole** -Tool in Microsoft Edge protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-143">The following figure displays messages from an example webpage logged in the **Console** tool in Microsoft Edge.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5c4a7-144">In der folgenden Abbildung werden dieselben Nachrichten von der Beispielwebseite angezeigt, die in der **DevTools-Konsole** unter **Problem** von Microsoft Visual Studio-Code protokolliert ist.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-144">The following figure displays the same messages from the example webpage logged in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Anzeigen einer Nachricht in der Konsole in Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         <span data-ttu-id="5c4a7-146">Anzeigen einer Nachricht in der Konsole in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5c4a7-146">Display a message in Console in Microsoft Edge DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Anzeigen derselben Nachricht in der DevTools-Konsole unter Problem von Microsoft Visual Studio-Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         <span data-ttu-id="5c4a7-148">Anzeigen derselben Nachricht in der DevTools-Konsole unter Problem von Microsoft Visual Studio-Code</span><span class="sxs-lookup"><span data-stu-id="5c4a7-148">Display the same message in the DevTools Console under Output of Microsoft Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a><span data-ttu-id="5c4a7-149">Verbesserte CSS-Flexbox-Bearbeitung mit visuellem Flexbox-Editor und mehreren Overlays</span><span class="sxs-lookup"><span data-stu-id="5c4a7-149">Improved CSS flexbox editing with visual flexbox editor and multiple overlays</span></span>  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

<span data-ttu-id="5c4a7-150">DevTools verfügt jetzt über dedizierte CSS-Flexbox-Debuggingtools.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-150">DevTools now has dedicated CSS flexbox debugging tools.</span></span>  <span data-ttu-id="5c4a7-151">Wenn der `display: flex` oder `display: inline-flex` CSS-Stil auf ein HTML-Element angewendet wird, wird ein `flex` Symbol neben diesem Element im **Element**-Tool angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-151">If the `display: flex` or `display: inline-flex` CSS style is applied to an HTML element, a `flex` icon displays next to that element in the **Elements** tool.</span></span>  <span data-ttu-id="5c4a7-152">Zum Anzeigen \(oder Ausblenden\) einer Flexüberlagerung auf der Webseite wählen Sie das `flex` Symbol aus.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-152">To display \(or hide\) a flex overlay on the webpage, choose the `flex` icon.</span></span>  <span data-ttu-id="5c4a7-153">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [1166710][CR1166710] und [1175699][CR1175699].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-153">To review the history of this feature in the Chromium open-source project, navigate to Issues [1166710][CR1166710] and [1175699][CR1175699].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5c4a7-154">Navigieren Sie zum Öffnen des **Flexbox** -Editors zum Bereich**Stile**, und wählen Sie das neue Symbol neben dem Stil `display: flex` oder `display: inline-flex` aus.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-154">To open the **Flexbox** editor, navigate to the **Styles** pane and choose the new icon next to the `display: flex` or `display: inline-flex` style.</span></span>  <span data-ttu-id="5c4a7-155">Der **Flexbox** -Editor bietet eine schnelle Möglichkeit, die Flexbox-Eigenschaften zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-155">The **Flexbox** editor provides a quick way to edit the flexbox properties.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5c4a7-156">Darüber hinaus werden im Abschnitt **Flexbox** im Bereich **Layout** alle Flexbox-Elemente auf der Webseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-156">In addition, the **Flexbox** section in the **Layout** pane displays all of the flexbox elements on the webpage.</span></span>  <span data-ttu-id="5c4a7-157">Sie können die Überlagerung der einzelnen Elemente umschalten.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-157">You may toggle the overlay of each element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="CSS-Flexbox-Debuggingtools" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         <span data-ttu-id="5c4a7-159">CSS-Flexbox-Debuggingtools</span><span class="sxs-lookup"><span data-stu-id="5c4a7-159">CSS flexbox debugging tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Abschnitt "Flexbox" im Layoutbereich" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         <span data-ttu-id="5c4a7-161">Abschnitt **Flexbox** im Bereich **Layout**</span><span class="sxs-lookup"><span data-stu-id="5c4a7-161">**Flexbox** section in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a><span data-ttu-id="5c4a7-162">Verbesserungen der Tastaturnavigation für Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="5c4a7-162">Keyboard navigation improvements for network requests</span></span>  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

<span data-ttu-id="5c4a7-163">Bisher war es Ihnen nicht möglich, die Anforderungskette mithilfe der Pfeiltasten auf der Tastatur im Bereich **Initiator** zu erweitern oder zu reduzieren, im Gegensatz zum DOM im Tool **Elemente**.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-163">Previously, you were not able to expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane, unlike the DOM in the **Elements** tool.</span></span>  <span data-ttu-id="5c4a7-164">Wenn im **Netzwerk** -Tool eine Netzwerkanforderung ausgewählt ist, wird im Bereich **Initiator** die Anforderungskette angezeigt, welche die aktuell ausgewählte Anforderung initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-164">When a network request is selected in the **Network** tool, the **Initiator** pane displays the chain of requests that initiated the currently selected request.</span></span>  

<span data-ttu-id="5c4a7-165">In Microsoft Edge Version 90 können Sie die Anforderungskette mithilfe der Pfeiltasten auf der Tastatur im Bereich **Initiator** erweitern oder reduzieren.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-165">In Microsoft Edge version 90, you may expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane.</span></span>  <span data-ttu-id="5c4a7-166">Die fokussierte Netzwerkanforderung in der Kette wird jetzt ebenfalls hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-166">The focused network request in the chain is also now highlighted.</span></span>  <span data-ttu-id="5c4a7-167">Weitere Informationen zu Initiatoren im **Netzwerk** -Tool finden Sie unter [Anzeigen von Initiatoren und Abhängigkeiten][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-167">To learn more about initiators in the **Network** tool, navigate to [Display initiators and dependencies][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].</span></span>  <span data-ttu-id="5c4a7-168">Um den Verlauf dieses Features im Chromium-Open-Source-Projekt zu überprüfen, navigieren Sie zu den Problemen [1158276][CR1158276] und [1160637][CR1160637].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-168">To review the history of this feature in the Chromium open-source project, navigate to Issues [1158276][CR1158276] and [1160637][CR1160637].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Wählen Sie eine Netzwerkanforderung und dann den Initiatorbereich." lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         <span data-ttu-id="5c4a7-170">Wählen Sie eine Netzwerkanforderung und dann den Bereich **Initiator**</span><span class="sxs-lookup"><span data-stu-id="5c4a7-170">Choose a Network request and choose the **Initiator** pane</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Erweitern oder reduzieren Sie die Anforderungsinitiator-Kette und folgen Sie der markierten Zeile" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         <span data-ttu-id="5c4a7-172">Erweitern oder reduzieren Sie die Anforderungsinitiator-Kette und folgen Sie der markierten Zeile</span><span class="sxs-lookup"><span data-stu-id="5c4a7-172">Expand or collapse the request initiator chain and follow the highlighted row</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a><span data-ttu-id="5c4a7-173">Das Filtern in der Konsole ist konsistenter</span><span class="sxs-lookup"><span data-stu-id="5c4a7-173">Filtering in the Console is more consistent</span></span>  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

<span data-ttu-id="5c4a7-174">Während Sie mit der [Konsolen-Randleiste][DevtoolsConsoleReferenceOpenConsoleSidebar] filtern, sind die Filter in der Dropdown-Liste [Protokollebenen][DevtoolsConsoleReferenceFilterByLogLevel] nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-174">While you filter with the [Console Sidebar][DevtoolsConsoleReferenceOpenConsoleSidebar], the filters in the [Log Levels][DevtoolsConsoleReferenceFilterByLogLevel] dropdown are not available.</span></span>  <span data-ttu-id="5c4a7-175">Zuvor wurde die Dropdown-Liste **Protokollebenen** hervorgehoben, wenn Sie mit der Maus darüber gefahren sind, obwohl ein Filter aus der **Konsolen-Randleiste** ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-175">Previously, the **Log Levels** dropdown highlighted when you hovered on it, even while a filter from the **Console Sidebar** was chosen.</span></span>  <span data-ttu-id="5c4a7-176">In Microsoft Edge Version 90 wird die Dropdown-Liste **Protokollebenen** nicht mehr hervorgehoben, wenn Sie den Mauszeiger darüber halten, während ein Filter aus der **Konsolen-Randleiste** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-176">In Microsoft Edge version 90, the **Log Levels** dropdown no longer highlights when you hover on it while a filter from the **Console Sidebar** is chosen.</span></span>  <span data-ttu-id="5c4a7-177">Weitere Informationen zum Filtern in der **Konsole** finden Sie unter [Nachrichten filtern][DevtoolsConsoleReferenceFilterMessages].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-177">To learn more about filtering in the **Console**, navigate to [Filter Messages][DevtoolsConsoleReferenceFilterMessages].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Wenn Sie zuvor die Konsolen-Randleiste geöffnet haben und mit der Maus über die Standardebenen bewegen, wurde diese hervorgehoben." lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         <span data-ttu-id="5c4a7-179">Wenn Sie zuvor die **Konsolen-Randleiste** geöffnet haben und mit der Maus über die **Standardebenen** bewegen, wurde diese hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-179">Previously, if you open the **Console sidebar** and hover on **Default levels** it was highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="Wenn Sie ab Microsoft Edge 90 die Konsolen-Randleiste auswählen und den Mauszeiger auf den Standardebenen bewegen, wird diese nicht hervorgehoben." lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         <span data-ttu-id="5c4a7-181">Wenn Sie ab Microsoft Edge 90 die **Konsolen-Randleiste** auswählen und den Mauszeiger auf den **Standardebenen** bewegen, wird diese nicht hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-181">Starting in Microsoft Edge 90, if you choose the **Console sidebar** and hover on **Default levels**, it does not highlight</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="5c4a7-182">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="5c4a7-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a><span data-ttu-id="5c4a7-183">Die Konsole entkommt nun doppelten Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="5c4a7-183">The Console now escapes double quote characters</span></span>  

<span data-ttu-id="5c4a7-184">Zuvor hat die **Konsole** keine gültigen doppelten Anführungszeichen \(`"`\) in JavaScript-Zeichenfolgen ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-184">Previously, the **Console** did not output valid double quote \(`"`\) characters in JavaScript strings.</span></span>  <span data-ttu-id="5c4a7-185">Ab Microsoft Edge Version 90 gibt die **Konsole** JavaScript-Zeichenfolgen mit maskierten doppelten Anführungszeichen \(`"`\) aus.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-185">Starting in Microsoft Edge version 90, the **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters.</span></span>  <span data-ttu-id="5c4a7-186">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [1178530][CR1178530].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-186">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178530][CR1178530].</span></span>  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="Die Konsole gibt JavaScript-Zeichenfolgen mit maskierten doppelten Anführungszeichen (& # 0022;) aus" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   <span data-ttu-id="5c4a7-188">Die **Konsole** gibt JavaScript-Zeichenfolgen unter Verwendung von maskierten doppelten Anführungszeichen \(`"`\) aus.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-188">The **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters</span></span>  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a><span data-ttu-id="5c4a7-189">Emulieren des CSS-Medienfeatures mit Farbskala</span><span class="sxs-lookup"><span data-stu-id="5c4a7-189">Emulate the CSS color-gamut media feature</span></span>  

<span data-ttu-id="5c4a7-190">Die Medienabfrage mit [Farbskala][ChromestatusFeature5354410980933632] emuliert den ungefähren Farbbereich, der vom Browser und dem zu testenden Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-190">The [color-gamut][ChromestatusFeature5354410980933632] media query emulates the approximate range of colors supported by the browser and the device you are testing.</span></span>  <span data-ttu-id="5c4a7-191">Das Dropdown-Menü unter **Emulieren der Farbskala für CSS-Medienfunktionen** enthält Farbräume, die DevTools möglicherweise emulieren.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-191">The dropdown under **Emulate CSS media feature color-gamut** contains color spaces that DevTools may emulate.</span></span>  <span data-ttu-id="5c4a7-192">Beispielsweise, zum Auslösen einer `color-gamut: p3` Medienabfrage, wählen Sie die **Farbskala: p3**in der Dropdown-Liste.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-192">For example, to trigger a `color-gamut: p3` media query, choose **color-gamut: p3** from the dropdown.</span></span>  

<span data-ttu-id="5c4a7-193">Zum Emulieren des CSS-Features für Farbskalenmedien, führen Sie die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-193">To emulate the CSS color-gamut media feature, complete the following actions.</span></span>  

1.  <span data-ttu-id="5c4a7-194">Öffnen Sie das [Befehlsmenü][DevtoolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-194">Open the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
1.  <span data-ttu-id="5c4a7-195">Geben Sie `Rendering` ein.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-195">Type `Rendering`.</span></span>  
1.  <span data-ttu-id="5c4a7-196">Führen Sie den Befehl **Rendering anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-196">Run the **Show Rendering** command.</span></span>  
1.  <span data-ttu-id="5c4a7-197">Navigieren Sie zu **Emulieren der Farbskala für CSS-Medienfunktionen** und wählen Sie eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-197">Navigate to **Emulate CSS media feature color-gamut** and choose an option.</span></span>  

<span data-ttu-id="5c4a7-198">Um mehr über das `color-gamut` Feature zu erfahren, navigieren Sie zu [Farbanzeigequalität: das Feature "Farbskala"][CsswgDraftsMediaqueries4ColorGamut].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-198">To learn more about the `color-gamut` feature, navigate to [Color Display Quality: the 'color-gamut' feature][CsswgDraftsMediaqueries4ColorGamut].</span></span>  <span data-ttu-id="5c4a7-199">Navigieren Sie zur Problem [1073887][CR1073887], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-199">To review the history of this feature in the Chromium open-source project, navigate to Issue [1073887][CR1073887].</span></span>  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emulieren des CSS-Medienfeatures mit Farbskala" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   <span data-ttu-id="5c4a7-201">Emulieren des CSS-Medienfeatures mit Farbskala</span><span class="sxs-lookup"><span data-stu-id="5c4a7-201">Emulate the CSS color-gamut media feature</span></span>  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a><span data-ttu-id="5c4a7-202">Verbesserte Progressive Web Apps-Tools</span><span class="sxs-lookup"><span data-stu-id="5c4a7-202">Improved Progressive Web Apps tooling</span></span>  

#### <a name="pwa-installability-warning-in-the-console"></a><span data-ttu-id="5c4a7-203">PWA-Installationswarnung in der Konsole</span><span class="sxs-lookup"><span data-stu-id="5c4a7-203">PWA installability warning in the Console</span></span>  

<span data-ttu-id="5c4a7-204">Die **Konsole** zeigt jetzt eine detailliertere Warnmeldung zur Installiationsfähigkeit von [Progressive Web Apps (PWA)][ProgressiveWebAppsIndex] mit einem Link zur [Verbesserung der Offline-Supporterkennung für Progressive Web Apps][ChromeDeveloperBlogImprovedPwaOfflineDetection] an.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-204">The **Console** now displays a more detailed [Progressive Web Apps (PWA)][ProgressiveWebAppsIndex] installability warning message with a link to [Improving Progressive Web App offline support detection][ChromeDeveloperBlogImprovedPwaOfflineDetection].</span></span>  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Warnung zur Installiationsfähigkeit von PWA im Konsolentool" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   <span data-ttu-id="5c4a7-206">Warnung zur Installiationsfähigkeit von PWA im Tool **Konsole**</span><span class="sxs-lookup"><span data-stu-id="5c4a7-206">PWA installability warning in **Console** tool</span></span>  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a><span data-ttu-id="5c4a7-207">Warnung zur Länge der PWA-Beschreibung im Manifestbereich</span><span class="sxs-lookup"><span data-stu-id="5c4a7-207">PWA description length warning in the Manifest pane</span></span>

<span data-ttu-id="5c4a7-208">Im Bereich **Manifest** wird jetzt eine Warnmeldung angezeigt, wenn die Manifestbeschreibung mehr als 324 Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-208">The **Manifest** pane now displays a warning message if the manifest description exceeds 324 characters.</span></span>  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Warnung zum Kürzen der PWA-Beschreibung" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   <span data-ttu-id="5c4a7-210">Warnung zum Kürzen der PWA-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c4a7-210">PWA description truncate warning</span></span>  
:::image-end:::  

<span data-ttu-id="5c4a7-211">Navigieren Sie zu den Problemen [965802][CR965802], [1146450][CR1146450] und [1169689][CR1169689], um den Verlauf dieser Funktion im Chromium-Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-211">To review the history of this feature in the Chromium open-source project, navigate to Issues [965802][CR965802], [1146450][CR1146450], and [1169689][CR1169689].</span></span>  

### <a name="new-remote-address-space-column-in-the-network-tool"></a><span data-ttu-id="5c4a7-212">Neue Remote-Adressraum-Spalte im Netzwerk-Tool</span><span class="sxs-lookup"><span data-stu-id="5c4a7-212">New Remote Address Space column in the Network tool</span></span>  

<!-- does not work in canary 90.0.813.0 -->  
<span data-ttu-id="5c4a7-213">In der neuen Spalte **Remote-Adressraum** wird der Netzwerk-IP-Adressraum jeder Netzwerkressource angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-213">The new **Remote Address Space** column displays the network IP address space of each network resource.</span></span>  <span data-ttu-id="5c4a7-214">Führen Sie die folgenden Aktionen aus, um die neue Spalte "Remote-Adressraum" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-214">To display the new Remote Address Space column, complete the following actions.</span></span>  

1.  <span data-ttu-id="5c4a7-215">Navigieren Sie zum **Netzwerk**-Tool.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-215">Navigate to the **Network** tool.</span></span>  
1.  <span data-ttu-id="5c4a7-216">Bewegen Sie den Mauszeiger in der Tabelle "Anforderungen" über die Kopfzeile und öffnen Sie das Kontextmenü \(Rechtsklick\).</span><span class="sxs-lookup"><span data-stu-id="5c4a7-216">In the Requests table, hover on the header row, and open the contextual menu \(right-click\).</span></span>  <span data-ttu-id="5c4a7-217">Navigieren Sie zu [Spalten hinzufügen oder entfernen][DevtoolsNetworkReferenceAddRemoveColumns], um zu erfahren, wie Sie Spalten zur Tabelle "Anforderungen" hinzufügen oder daraus entfernen.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-217">To learn how to add or remove columns from the Requests table, navigate to [Add or remove columns][DevtoolsNetworkReferenceAddRemoveColumns].</span></span>  
1.  <span data-ttu-id="5c4a7-218">Wählen Sie **Remote-Adressraum** aus.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-218">Choose **Remote Address Space**.</span></span>  
    
<span data-ttu-id="5c4a7-219">In der Tabelle "Anforderungen" wird jetzt eine neue Spalte mit der Kopfzeile **Remote-Adressraum** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-219">The Requests table now displays a new column with the header named **Remote Address Space**.</span></span>  <span data-ttu-id="5c4a7-220">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [1128885][CR1128885].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-220">To review the history of this feature in the Chromium open-source project, navigate to Issue [1128885][CR1128885].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="Wählen Sie im Kontextmenü Remote-Adressraum" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         <span data-ttu-id="5c4a7-222">Wählen Sie im Kontextmenü den **Remote-Adressraum**</span><span class="sxs-lookup"><span data-stu-id="5c4a7-222">In the contextual menu, choose the **Remote Address Space**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="In der Tabelle "Anforderungen" wird jetzt die Spalte "Remote-Adressraum" angezeigt." lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         <span data-ttu-id="5c4a7-224">In der Tabelle "Anforderungen" wird jetzt die Spalte **Remote-Adressraum** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-224">The Requests table now displays the **Remote Address Space** column</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a><span data-ttu-id="5c4a7-225">Anzeigen zulässiger und nicht zulässiger Features in der Frame-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="5c4a7-225">Display allowed and disallowed features in the Frame details view</span></span>  

<span data-ttu-id="5c4a7-226">In der Frame-Detailansicht wird jetzt eine Liste der zulässigen und nicht zulässigen Browserfunktionen angezeigt, die von der [Berechtigungsrichtlinie][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer] gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-226">The Frame details view now displays a list of allowed and disallowed browser features controlled by the [Permissions Policy][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].</span></span>  <span data-ttu-id="5c4a7-227">Die Berechtigungsrichtlinie ist eine Webplattform-API, die es einer Webseite ermöglicht (oder blockiert), Browserfeatures in einem einzelnen Frame oder in eingebetteten iframes zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-227">Permissions Policy is a web platform API that allows \(or blocks\) a webpage the use of browser features in an individual frame or in iframes that it embeds.</span></span>  <span data-ttu-id="5c4a7-228">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [1158827][CR1158827].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-228">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Zulässige und nicht zulässige Features basierend auf der Berechtigungsrichtlinie" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   <span data-ttu-id="5c4a7-230">Zulässige und nicht zulässige Features basierend auf der Berechtigungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="5c4a7-230">Allowed and disallowed features based on the Permission Policy</span></span>  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a><span data-ttu-id="5c4a7-231">Neue SameParty-Spalte im Bereich "Cookies"</span><span class="sxs-lookup"><span data-stu-id="5c4a7-231">New SameParty column in the Cookies pane</span></span>  

<span data-ttu-id="5c4a7-232">Im Bereich **Cookies** im Tool **Anwendung** wird jetzt das `SameParty` Attribut für jedes Cookie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-232">The **Cookies** pane in the **Application** tool now displays the `SameParty` attribute for each cookie.</span></span>  <span data-ttu-id="5c4a7-233">Das `SameParty` Attribut ist ein neues boolesches Attribut, das angibt, ob ein Cookie in Anforderungen an Ursprünge derselben [First-Party-Sets][GithubPrivacycgFirstPartySets] enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-233">The `SameParty` attribute is a new boolean attribute to indicate whether a cookie is included in requests to origins of the same [First-Party Sets][GithubPrivacycgFirstPartySets].</span></span>  <span data-ttu-id="5c4a7-234">Navigieren Sie zu Problem [1161427][CR1161427], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-234">To review the history of this feature in the Chromium open-source project, navigate to Issue [1161427][CR1161427].</span></span>  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="SameParty-Spalte im Bereich "Cookies"" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   <span data-ttu-id="5c4a7-236">**SameParty**-Spalte im Bereich **Cookies**</span><span class="sxs-lookup"><span data-stu-id="5c4a7-236">**SameParty** column in the **Cookies** pane</span></span>  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a><span data-ttu-id="5c4a7-237">Die Eigenschaft fn.displayName im Konsolentool ist jetzt veraltet.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-237">fn.displayName property in the Console tool is now deprecated</span></span>  

<span data-ttu-id="5c4a7-238">Bisher konnten Sie mit der `fn.displayName` Eigenschaft Debug-Namen für Funktionen steuern, die in `error.stack` und in DevTools-Stapelüberwachung angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-238">Previously, the `fn.displayName` property allowed you to control debug names for functions to display in `error.stack` and in DevTools stack traces.</span></span>  <span data-ttu-id="5c4a7-239">Ab Microsoft Edge Version 90 ist die `fn.displayName` Eigenschaft jetzt veraltet und wird durch die `fn.name` Eigenschaft ersetzt.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-239">Starting in Microsoft Edge version 90, the `fn.displayName` property is now deprecated, and replaced by the `fn.name` property.</span></span>  <span data-ttu-id="5c4a7-240">Verwenden Sie die `Object.defineProperty` Standardmethode, um die `fn.name` Eigenschaft zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-240">Use the standard `Object.defineProperty` method to define the `fn.name` property.</span></span>  <span data-ttu-id="5c4a7-241">Um mehr über zu `fn.name` erfahren, navigieren Sie zu [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-241">To learn more about `fn.name`, navigate to [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span></span>  <span data-ttu-id="5c4a7-242">Navigieren Sie zu Problem [1177685][CR1177685], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-242">To review the history of this feature in the Chromium open-source project, navigate to Issue [1177685][CR1177685].</span></span>  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Ein Beispiel für die Eigenschaft fn.name zur Steuerung von Debug-Namen für Funktionen" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   <span data-ttu-id="5c4a7-244">Ein Beispiel für die `fn.name` Eigenschaft zur Steuerung von Debug-Namen für Funktionen</span><span class="sxs-lookup"><span data-stu-id="5c4a7-244">An example of the `fn.name` property to control debug names for functions</span></span>  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a><span data-ttu-id="5c4a7-245">Vollständige Barrierefreiheitsstrukturansicht im Elements-Tool</span><span class="sxs-lookup"><span data-stu-id="5c4a7-245">Full accessibility tree view in the Elements tool</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="5c4a7-246">Dieses Experiment bietet eine **vollständige Barrierefreiheitsstrukturansicht** im **Elemente**-Tool.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-246">This experiment provides a **full accessibility tree view** in the **Elements** tool.</span></span>  <span data-ttu-id="5c4a7-247">Der Bereich [Barrierefreiheit][DevtoolsAccessibilityTab] bietet eine teilweise Barrierefreiheitsstrukturansicht, in der die direkte Ahnenkette vom Stammknoten zum inspizierten Knoten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-247">The [Accessibility][DevtoolsAccessibilityTab] pane provides a partial accessibility tree view, that displays the direct ancestor chain from the root node to the inspected node.</span></span>  
<span data-ttu-id="5c4a7-248">Nachdem Sie dieses Experiment aktiviert und die DevTools neu geladen haben, wählen Sie eine der folgenden Schaltflächen, um die Anzeige im Elementwerkzeug für alle Elemente auf der Webseite zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-248">After you turn on this experiment and reload the DevTools, choose one of the following buttons to switch the display in the Elements tool for all elements on the webpage.</span></span>  

*   <span data-ttu-id="5c4a7-249">Um die vollständige Barrierefreiheitsstrukturansicht anzuzeigen, wählen Sie **Zur Barrierefreiheitsstrukturansicht wechseln**.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-249">To display the full accessibility tree view , choose the **Switch to Accessibility Tree view**.</span></span>  
*   <span data-ttu-id="5c4a7-250">Wählen Sie zum Anzeigen der DOM-Strukturansicht **Zur DOM-Strukturansicht wechseln** aus.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-250">To display the DOM tree view, choose the **Switch to DOM Tree view**.</span></span>  
    
<span data-ttu-id="5c4a7-251">Um das Experiment zu aktivieren, navigieren Sie zu [Experimentelle Features aktivieren][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **Aktivieren der vollständigen Barrierefreiheitsstruktur im Elementbereich**.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-251">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkbox next to **Enable full accessibility tree view in Elements pane**.</span></span>  <span data-ttu-id="5c4a7-252">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [887173][CR887173].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-252">To review the history of this feature in the Chromium open-source project, navigate to Issue [887173][CR887173].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Anzeigen der DOM-Strukturansicht" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         <span data-ttu-id="5c4a7-254">Anzeigen der **DOM-Strukturansicht**</span><span class="sxs-lookup"><span data-stu-id="5c4a7-254">Display the **DOM Tree view**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Anzeigen der Strukturansicht „Vollständige Barrierefreiheit“" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         <span data-ttu-id="5c4a7-256">Anzeigen der **Vollständigen Barrierefreiheitsstrukturansicht**</span><span class="sxs-lookup"><span data-stu-id="5c4a7-256">Display the **Full Accessibility Tree view**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="5c4a7-257">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="5c4a7-257">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="5c4a7-258">Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-258">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="5c4a7-259">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-259">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="5c4a7-260">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="5c4a7-260">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityTab]: ../../../accessibility/accessibility-tab.md "Testen Sie die Barrierefreiheit mithilfe der Registerkarte &quot;Barrierefreiheit&quot; | Microsoft-Dokumentation"  
[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft-Dokumentation"  
[DevtoolsConsoleReferenceFilterByLogLevel]: ../../../console/reference.md#filter-by-log-level "Filtern nach Protokollebene – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: ../../../console/reference.md#filter-messages "Filtern von Nachrichten – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: ../../../console/reference.md#open-the-console-sidebar "Öffnen der Konsolen-Randleiste – Konsolenreferenz | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: ../../../experimental-features/index.md#enable--button-tab-menus-to-open-more-tools "Aktivieren Sie die Registerkartenmenüs +, um weitere Werkzeuge zu öffnen – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../../../experimental-features/index.md#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: ../../../network/reference.md#add-or-remove-columns "Hinzufügen oder Entfernen von Spalten – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: ../../../network/reference.md#display-initiators-and-dependencies "Anzeigen von Initiatoren und Abhängigkeiten – Netzwerkanalysereferenz | Microsoft Docs"  

[ProgressiveWebAppsIndex]: ../../../../progressive-web-apps-chromium/index.md "Übersicht über progressive Web Apps unter Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Verbessern der Erkennung der progressiven Web App-Offline-Unterstützung | Chrome-Entwickler"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "Farbskala-Medienabfrage | Chrome-Plattformstatus"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  
[CR174309]: https://crbug.com/174309 "Problem 174309: DevTools: Zulassen der Anpassung von Tastenkombinationen/Tastenbindungen | Chromium-Fehler"  
[CR887173]: https://crbug.com/887173 "Problem 887173: DevTools: Vollständige Barrierefreiheitsstrukturüberprüfung | Chromium-Fehler"  
[CR965802]: https://crbug.com/965802 "Problem 965802: Implementieren einer genaueren Offline-Fähigkeitserkennung für Servicemitarbeiter | Chromium-Fehler"  
[CR1073887]: https://crbug.com/1073887 "Problem 1073887: DevTools: @media (Farbskala: ...) Farbraumemulation | Chromium-Fehler"  
[CR1128885]: https://crbug.com/1128885 "Problem 1128885: DevTools-Unterstützung für CORS-RFC1918 | Chromium-Fehler"  
[CR1146450]: https://crbug.com/1146450 "Problem 1146450: [Android] Implementieren von Bottom Sheet-Installationen | Chromium-Fehler"  
[CR1158276]: https://crbug.com/1158276 "Problem 1158276: Der Bereich &quot;Initiator-Kette anfordern&quot; kann nicht mithilfe der Pfeiltasten im Abschnitt &quot;Netzwerk&quot; von DevTools erweitert/verkleinert werden | Chromium-Fehler"  
[CR1158827]: https://crbug.com/1158827 "Problem 1158827: [Berechtigungsrichtlinie] Implementieren der Devtool-Unterstützung für Berechtigungsrichtlinien | Chromium-Fehler"  
[CR1160637]: https://crbug.com/1160637 "Problem 1160637: Der Fokus auf 'Initiierungskette anfordern' wird im Abschnitt 'Netzwerk' des Fensters 'Dev Tools' unvollständig angezeigt | Chromium-Fehler"  
[CR1161427]: https://crbug.com/1161427 "Problem 1161427: &#9730; Unterstützt das Debuggen von SameParty-Cookie-Attributen in DevTools | Chromium-Fehler"  
[CR1166710]: https://crbug.com/1166710 "Problem 1166710: Standardmäßiges Aktivieren des Flexbox-Tooling-Experiment | Chromium-Fehler"  
[CR1169689]: https://crbug.com/1169689 "Problem 1169689: Das untere Blatt der PWA-Installation sollte keine Kategorien enthalten | Chromium-Fehler"  
[CR1175699]: https://crbug.com/1175699 "Problem 1175699: Flexbox-Editor | Chromium-Fehler"  
[CR1177685]: https://crbug.com/1177685 "Problem 1177685: Entfernen von nicht standardmäßiger Unterstützung für fn.displayName | Chromium-Fehler"  
[CR1178530]: https://crbug.com/1178530 "Problem 1178530: Die Konsole maskiert beim Drucken von Zeichenfolgen keine doppelten Anführungszeichen | Chromium-Fehler"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Farbanzeigequalität: Das Feature &quot;Farbskala&quot; | Entwürfe des CSS-Arbeitsgruppen-Editors"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: Benutzeroberfläche für den Fokusmodus – MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "First-Party-Sets | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Berechtigungsrichtlinienerklärer | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> <span data-ttu-id="5c4a7-300">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-300">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5c4a7-301">Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-90) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="5c4a7-301">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-90) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="5c4a7-303">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5c4a7-303">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
