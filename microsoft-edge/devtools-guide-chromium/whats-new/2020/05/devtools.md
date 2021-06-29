---
description: Verwenden Sie die DevTools in Windows Modus mit hohem Kontrast, passen Sie Tastenkombinationen in devTools an Visual Studio Code an und vieles mehr.
title: Neuigkeiten in DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: fabfa21abedb02bc83ec2bedbe3662f0d81c1bf9
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624808"
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
# <a name="whats-new-in-devtools-microsoft-edge-84"></a><span data-ttu-id="e3acb-104">Neuigkeiten in DevTools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="e3acb-104">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e3acb-105">Ankündigungen des Microsoft Edge DevTools-Teams</span><span class="sxs-lookup"><span data-stu-id="e3acb-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="e3acb-106">In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise vom Microsoft Edge DevTools-Team verpasst haben.</span><span class="sxs-lookup"><span data-stu-id="e3acb-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="e3acb-107">Sehen Sie sich die Ankündigungen an, um neue Features in devTools, Microsoft Visual Studio Codeerweiterungen und vieles mehr auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="e3acb-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="e3acb-108">Um über die neuesten und besten Features in Ihren Entwicklertools auf dem Laufenden zu bleiben, laden Sie die [Microsoft Edge Vorschaukanäle][MicrosoftEdgePreviewChannels] herunter, und [folgen Sie uns auf Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="e3acb-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a><span data-ttu-id="e3acb-109">Verwenden der DevTools im Modus Windows hohen Kontrasts</span><span class="sxs-lookup"><span data-stu-id="e3acb-109">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="e3acb-110">Die Microsoft Edge DevTools werden jetzt im Modus mit hohem Kontrast angezeigt, wenn sich Windows im Modus mit hohem Kontrast befindet.</span><span class="sxs-lookup"><span data-stu-id="e3acb-110">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Die Microsoft Edge DevTools im Modus mit hohem Kontrast" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="e3acb-112">Die Microsoft Edge DevTools im Modus mit hohem Kontrast</span><span class="sxs-lookup"><span data-stu-id="e3acb-112">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="e3acb-113">[Befolgen Sie die Anweisungen, um den Modus für hohen Kontrast in Windows zu aktivieren.][MicrosoftSupportWindows10HighContrastMode]</span><span class="sxs-lookup"><span data-stu-id="e3acb-113">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="e3acb-114">Um die DevTools in Microsoft Edge zu öffnen, wählen `F12` Sie oder `Ctrl` + `Shift` + `I` aus.</span><span class="sxs-lookup"><span data-stu-id="e3acb-114">To open the DevTools in Microsoft Edge, select `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="e3acb-115">Die DevTools werden im Modus mit hohem Kontrast angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3acb-115">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="e3acb-116">Die Microsoft Edge DevTools unterstützen derzeit den Modus mit hohem Kontrast auf Windows, jedoch nicht unter macOS.</span><span class="sxs-lookup"><span data-stu-id="e3acb-116">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span>  

<span data-ttu-id="e3acb-117">Chromium Problem [#1048378][CR1048378]</span><span class="sxs-lookup"><span data-stu-id="e3acb-117">Chromium issue [#1048378][CR1048378]</span></span>  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a><span data-ttu-id="e3acb-118">Anpassen von Tastenkombinationen in devTools an Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e3acb-118">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="e3acb-119">Anhand Ihres [Feedbacks](#getting-in-touch-with-microsoft-edge-devtools-team) und der [Chromium öffentlichen Problemverfolgung][CRIssuesList]hat das Microsoft Edge DevTools-Team erfahren, dass Sie die Möglichkeit haben wollten, Tastenkombinationen in den DevTools anzupassen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-119">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="e3acb-120">In Microsoft Edge 84 können Sie nun Tastenkombinationen in devTools mit [Visual Studio Code][VisualStudioCodeMain]abgleichen, was nur eines der Features ist, an denen das Team für die Anpassung von Tastenkombinationen arbeitet.</span><span class="sxs-lookup"><span data-stu-id="e3acb-120">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [Visual Studio Code][VisualStudioCodeMain], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Anpassen von Tastenkombinationen in devTools an Visual Studio Code" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="e3acb-122">Die Microsoft Edge DevTools im Modus mit hohem Kontrast</span><span class="sxs-lookup"><span data-stu-id="e3acb-122">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="e3acb-123">Um das Experiment auszuprobieren, öffnen Sie DevTools Einstellungen, indem Sie `?` in der oberen rechten Ecke der DevTools das Symbol devtools Einstellungen auswählen oder ![ ](../../../media/settings-icon.msft.png) auswählen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-123">To try the experiment, open DevTools Settings by selecting `?` or choosing the ![Devtools Settings icon](../../../media/settings-icon.msft.png) icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="e3acb-124">Navigieren Sie zum Abschnitt **"Experimente",** und aktivieren Sie die Registerkarte "Einstellungen für **benutzerdefinierte Tastenkombinationen aktivieren" (muss neu geladen werden).**</span><span class="sxs-lookup"><span data-stu-id="e3acb-124">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="e3acb-125">Laden Sie nun die DevTools neu, öffnen Sie Einstellungen erneut, und navigieren Sie zum Abschnitt **"Verknüpfungen".**</span><span class="sxs-lookup"><span data-stu-id="e3acb-125">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="e3acb-126">Wählen Sie **DevTools (Standard)** in den **Verknüpfungen "Übereinstimmung" aus dem vordefinierten** Dropdownmenü aus, und wählen Sie **Visual Studio Code**aus.</span><span class="sxs-lookup"><span data-stu-id="e3acb-126">Choose **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="e3acb-127">Die Tastenkombinationen in den DevTools stimmen jetzt mit den Tastenkombinationen für entsprechende Aktionen in Visual Studio Code überein.</span><span class="sxs-lookup"><span data-stu-id="e3acb-127">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

<span data-ttu-id="e3acb-128">Beispielsweise lautet die Tastenkombination zum Anhalten oder Fortsetzen der Ausführung eines Skripts in [Visual Studio Code][VisualStudioCodeShortcuts] `F5` .</span><span class="sxs-lookup"><span data-stu-id="e3acb-128">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="e3acb-129">Mit der **Voreinstellung DevTools (Standard)** ist die gleiche Verknüpfung in devTools, `F8` aber mit der **Visual Studio Code** Voreinstellung ist diese Verknüpfung jetzt auch `F5` .</span><span class="sxs-lookup"><span data-stu-id="e3acb-129">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="e3acb-130">Das Feature ist derzeit in Microsoft Edge 84 als Experiment verfügbar. Teilen Sie ihr [Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) also bitte mit dem Team!</span><span class="sxs-lookup"><span data-stu-id="e3acb-130">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="e3acb-131">Chromium Problem [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="e3acb-131">Chromium issue [#174309][CR174309]</span></span>  

### <a name="remote-debug-surface-duo-emulators"></a><span data-ttu-id="e3acb-132">Remotedebugging von Surface Duo-Emulatoren</span><span class="sxs-lookup"><span data-stu-id="e3acb-132">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="e3acb-133">Sie können jetzt Ihre Webinhalte, die im [Surface Duo-Emulator][DualScreensAndroidEmulator] ausgeführt werden, remote debuggen, indem Sie die volle Leistungsfähigkeit der [Microsoft Edge DevTools][DevtoolsIndex]nutzen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-133">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  

<span data-ttu-id="e3acb-134">Mit dem [Surface Duo-Emulator][DualScreensAndroidEmulator]können Sie testen, wie Ihre Webinhalte auf einer neuen Klasse von faltbaren Geräten und Geräten mit dualem Bildschirm gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="e3acb-134">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="e3acb-135">Der Emulator führt das Android-Betriebssystem aus und stellt die [Microsoft Edge Android-App bereit.][AndroidEdge]</span><span class="sxs-lookup"><span data-stu-id="e3acb-135">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="e3acb-136">Laden Sie Ihre Webinhalte in die [Microsoft Edge-App,][AndroidEdge] und debuggen Sie sie mit [der Microsoft Edge DevTools.][DevtoolsIndex]</span><span class="sxs-lookup"><span data-stu-id="e3acb-136">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Die Microsoft Edge-App, die auf dem Surface Duo-Emulator ausgeführt wird" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="e3acb-138">Die Microsoft Edge-App im Surface Duo-Emulator</span><span class="sxs-lookup"><span data-stu-id="e3acb-138">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="e3acb-139">Die `edge://inspect` Seite in einer Desktopinstanz von [Microsoft Edge][DesktopEdge] zeigt den **SurfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs][PwaIndex] an, die im [Surface Duo-Emulator][DualScreensAndroidEmulator]ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e3acb-139">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="Auf der edge://inspect Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge App angezeigt, die im Emulator ausgeführt wird." lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="e3acb-141">Auf `edge://inspect` der Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge App angezeigt, die im Emulator ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3acb-141">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="e3acb-142">Überprüfen \*\*\*\* Sie die Registerkarte oder PWA, die Sie debuggen möchten, um die [Microsoft Edge DevTools][DevtoolsIndex]zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-142">Choose **inspect** for the tab or PWA that you want to debug to open the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="e3acb-143">[Befolgen Sie die schrittweise Anleitung, um Webinhalte im Surface Duo-Emulator remote zu debuggen.][DevtoolsRemoteDebugDuoEmulator]</span><span class="sxs-lookup"><span data-stu-id="e3acb-143">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevtoolsRemoteDebugDuoEmulator].</span></span>  

### <a name="resize-the-devtools-drawer-more-easily"></a><span data-ttu-id="e3acb-144">Einfacheres Ändern der Größe der DevTools-Schublade</span><span class="sxs-lookup"><span data-stu-id="e3acb-144">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="e3acb-145">In Microsoft Edge 83 oder früheren Versionen konnten Sie die Größe der [Devtools-Schublade][DevtoolsDrawer] nur ändern, indem Sie auf die Symbolleiste der Schublade zeigen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-145">In Microsoft Edge 83 or earlier, you were only able to resize the [Devtools Drawer][DevtoolsDrawer] by hovering inside the toolbar of the Drawer.</span></span>  <span data-ttu-id="e3acb-146">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover on the border of the pane toize it.</span><span class="sxs-lookup"><span data-stu-id="e3acb-146">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover on the border of the pane to resize it.</span></span>  <span data-ttu-id="e3acb-147">Wählen Sie die folgende Abbildung aus, um anzuzeigen, wie die Größenänderung der Schublade in Version 83 oder früher von Microsoft Edge funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="e3acb-147">Choose the following image to display how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Ändern der Größe der DevTools-Schublade in Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="e3acb-149">Ändern der Größe der DevTools-Schublade in Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="e3acb-149">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="e3acb-150">Ab Microsoft Edge 84 können Sie jetzt die Größe der Schublade ändern, indem Sie über den Rahmen der Schublade zeigen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-150">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="e3acb-151">Diese Änderung richtet das Verhalten beim Ändern der Größe der DevTools-Schublade an die Art und Weise aus, wie Sie die Größe anderer Bereiche in den DevTools ändern.</span><span class="sxs-lookup"><span data-stu-id="e3acb-151">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="e3acb-152">Wählen Sie das folgende Bild aus, um die Größenänderung in Aktion in Microsoft Edge 84 anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-152">Choose the following image to display resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Ändern der Größe der DevTools-Schublade in Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="e3acb-154">Ändern der Größe der DevTools-Schublade in Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="e3acb-154">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="e3acb-155">Chromium Problem [#1076112][CR1076112]</span><span class="sxs-lookup"><span data-stu-id="e3acb-155">Chromium issue [#1076112][CR1076112]</span></span>  

### <a name="screencasting-navigation-buttons-display-focus"></a><span data-ttu-id="e3acb-156">Bildschirmcasting-Navigationsschaltflächen zeigen den Fokus an</span><span class="sxs-lookup"><span data-stu-id="e3acb-156">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="e3acb-157">Beim Remotedebuggen eines [Android-Geräts,][DevtoolsRemoteDebugAndroid]eines [Windows 10 Geräts][DevtoolsRemoteDebugWindows]oder eines [Surface Duo-Emulators][DevtoolsRemoteDebugDuoEmulator]können Sie screencasting mit dem ![ Toggle ](../../../media/toggle-screencast-icon.msft.png) Screencast-Symbol in der oberen linken Ecke der DevTools umschalten.</span><span class="sxs-lookup"><span data-stu-id="e3acb-157">When remote debugging an [Android device][DevtoolsRemoteDebugAndroid], a [Windows 10 device][DevtoolsRemoteDebugWindows], or a [Surface Duo emulator][DevtoolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast](../../../media/toggle-screencast-icon.msft.png) icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="e3acb-158">Wenn Screencasting aktiviert ist, können Sie über das DevTools-Fenster in Microsoft Edge auf dem Remotegerät navigieren.</span><span class="sxs-lookup"><span data-stu-id="e3acb-158">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="e3acb-159">In Microsoft Edge 84 sind diese Navigationsschaltflächen jetzt auch über die Tastatur zugänglich.</span><span class="sxs-lookup"><span data-stu-id="e3acb-159">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Wählen Sie "UMSCHALT+TAB" aus der bildschirmierten URL-Leiste aus, um den Fokus auf der Schaltfläche "Aktualisieren" anzuzeigen." lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="e3acb-161">Wählen Sie `Shift` + `Tab` in der Screencast-URL-Leiste den Fokus auf der Schaltfläche **"Aktualisieren"** aus.</span><span class="sxs-lookup"><span data-stu-id="e3acb-161">Select `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="e3acb-162">Chromium Problem [#1081486][CR1081486]</span><span class="sxs-lookup"><span data-stu-id="e3acb-162">Chromium issue [#1081486][CR1081486]</span></span>  

### <a name="network-panel-details-pane-is-now-accessible"></a><span data-ttu-id="e3acb-163">Auf den Bereich "Netzwerkpaneldetails" kann jetzt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="e3acb-163">Network panel Details pane is now accessible</span></span>  

<span data-ttu-id="e3acb-164">In Microsoft Edge 84 erhält der [Detailbereich][DevtoolsNetworkDetails] im **Netzwerktool** jetzt den Fokus, wenn Sie ihn für eine Ressource im [Netzwerkprotokoll][DevtoolsNetworkLog]öffnen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-164">In Microsoft Edge 84, the [Details pane][DevtoolsNetworkDetails] in the **Network** tool now takes focus when you open it for a resource in the [Network Log][DevtoolsNetworkLog].</span></span>  <span data-ttu-id="e3acb-165">Diese Änderung ermöglicht es Bildschirmleseprogrammen, den Inhalt des **Detailbereichs** auszulesen und mit ihnen zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="e3acb-165">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Der Bereich "Details" im Netzwerkbereich erhält beim Öffnen den Fokus." lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="e3acb-167">Der **Detailbereich** im **Netzwerktool** erhält den Fokus, wenn er geöffnet wird</span><span class="sxs-lookup"><span data-stu-id="e3acb-167">The **Details** pane in the **Network** tool takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="e3acb-168">Chromium Problem [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="e3acb-168">Chromium issue [#963183][CR963183]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="e3acb-169">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="e3acb-169">Announcements from the Chromium project</span></span>  

<span data-ttu-id="e3acb-170">In den folgenden Abschnitten werden zusätzliche Features angekündigt, die in Microsoft Edge 84 verfügbar sind, die zum Open Source Chromium Projekt beigetragen haben.</span><span class="sxs-lookup"><span data-stu-id="e3acb-170">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a><span data-ttu-id="e3acb-171">Beheben von Websiteproblemen mit dem neuen Tool "Probleme" in der DevTools-Schublade</span><span class="sxs-lookup"><span data-stu-id="e3acb-171">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="e3acb-172">Das neue **Tool "Probleme"** in der DevTools-Schublade wurde entwickelt, um die Benachrichtigungsermüdung und Unübersichtlichkeit der **Konsole**zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="e3acb-172">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="e3acb-173">Derzeit ist die **Konsole** der zentrale Ort für Websiteentwickler, Bibliotheken, Frameworks und Microsoft Edge zum Protokollieren von Nachrichten, Warnungen und Fehlern.</span><span class="sxs-lookup"><span data-stu-id="e3acb-173">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="e3acb-174">Das \*\*\*\* Problemtool aggregiert Warnungen aus dem Browser auf strukturierte, aggregierte und umsetzbare Weise, links zu betroffenen Ressourcen in Microsoft Edge DevTools und bietet Anleitungen zum Beheben der Probleme.</span><span class="sxs-lookup"><span data-stu-id="e3acb-174">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="e3acb-175">Im Laufe der Zeit werden mehr und mehr Warnungen in Microsoft Edge im **Problemtool** anstelle der **Konsole**angezeigt, was dazu beitragen sollte, die Unübersichtlichkeit in der **Konsole**zu verringern.</span><span class="sxs-lookup"><span data-stu-id="e3acb-175">Over time, more and more warnings are surfaced in Microsoft Edge in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="e3acb-176">To get started, navigate to [Find and fix problems using the Issues tool][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="e3acb-176">To get started, navigate to [Find and fix problems using the Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Das Tool "Probleme" in der DevTools-Schublade" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="e3acb-178">Das **Tool "Probleme"** in der DevTools-Schublade</span><span class="sxs-lookup"><span data-stu-id="e3acb-178">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="e3acb-179">Chromium Problem [#1068116][CR1068116]</span><span class="sxs-lookup"><span data-stu-id="e3acb-179">Chromium issue [#1068116][CR1068116]</span></span>  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a><span data-ttu-id="e3acb-180">Anzeigen von Barrierefreiheitsinformationen in der QuickInfo zum Überprüfen des Modus</span><span class="sxs-lookup"><span data-stu-id="e3acb-180">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="e3acb-181">Die QuickInfo zum **Prüfen des Modus** gibt nun an, ob das Element einen Namen und eine [Rolle][WebhintHintsAxeNameRoleValue] für die Verwendung durch Zugriff auf die Tastatur hat und [tastaturfokussierbar][WebhintHintsAxeKeyboard]ist.</span><span class="sxs-lookup"><span data-stu-id="e3acb-181">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="QuickInfo zum Überprüfungsmodus mit Informationen zur Barrierefreiheit" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="e3acb-183">QuickInfo zum **Überprüfungsmodus** mit Informationen zur Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="e3acb-183">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="e3acb-184">Chromium Problem [#1040025][CR1040025]</span><span class="sxs-lookup"><span data-stu-id="e3acb-184">Chromium issue [#1040025][CR1040025]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="e3acb-185">Aktualisierungen des Leistungsbereichs</span><span class="sxs-lookup"><span data-stu-id="e3acb-185">Performance panel updates</span></span>  

#### <a name="view-total-blocking-time-information-in-the-footer"></a><span data-ttu-id="e3acb-186">Anzeigen der Informationen zur Gesamtblockierungszeit in der Fußzeile</span><span class="sxs-lookup"><span data-stu-id="e3acb-186">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="e3acb-187">Nach dem Aufzeichnen der Ladeleistung zeigt der **Leistungsbereich** nun informationen zur Gesamtblockierungszeit \(TBT\) in der Fußzeile an.</span><span class="sxs-lookup"><span data-stu-id="e3acb-187">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="e3acb-188">TBT ist eine Lastleistungsmetrik, die quantifiziert, wie lange eine Seite benötigt, um verwendbar zu werden.</span><span class="sxs-lookup"><span data-stu-id="e3acb-188">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="e3acb-189">Es misst im Wesentlichen, wie lange eine Seite verwendbar zu sein scheint \(da der Inhalt auf dem Bildschirm gerendert wird\); kann jedoch nicht verwendet werden, da JavaScript den Hauptthread blockiert und die Seite daher nicht auf Benutzereingaben reagiert.</span><span class="sxs-lookup"><span data-stu-id="e3acb-189">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="e3acb-190">TBT ist die Hauptmetrik für die Ersteingabeverzögerung.</span><span class="sxs-lookup"><span data-stu-id="e3acb-190">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="e3acb-191">Verwenden Sie zum Abrufen der Informationen zur Gesamtblockierungszeit nicht den Symbolworkflow **"Seite** aktualisieren", um die Leistung beim Laden der ![ ](../../../media/refresh-page-icon.msft.png) Seite aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-191">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon](../../../media/refresh-page-icon.msft.png) workflow for recording page load performance.</span></span>  

<span data-ttu-id="e3acb-192">**Wählen** Sie stattdessen ![ das Datensatzsymbol ](../../../media/record-icon.msft.png) aus, laden Sie die Seite manuell neu, warten Sie, bis die Seite geladen wird, und beenden Sie die Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="e3acb-192">Instead, select **Record** ![Record icon](../../../media/record-icon.msft.png), manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="e3acb-193">Wenn `Total Blocking Time: Unavailable` diese angezeigt wird, hat Microsoft Edge DevTools nicht die erforderlichen Informationen aus den internen Profilerstellungsdaten in Microsoft Edge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-193">If `Total Blocking Time: Unavailable` is displayed, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Informationen zur Gesamtblockierungszeit in der Fußzeile einer Aufzeichnung des Leistungsbereichs" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="e3acb-195">Informationen zur Gesamtblockierungszeit in der Fußzeile einer Aufzeichnung des **Leistungsbereichs**</span><span class="sxs-lookup"><span data-stu-id="e3acb-195">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="e3acb-196">Chromium Problem [#1054381][CR1054381]</span><span class="sxs-lookup"><span data-stu-id="e3acb-196">Chromium issue [#1054381][CR1054381]</span></span>  

#### <a name="layout-shift-events-in-the-new-experience-section"></a><span data-ttu-id="e3acb-197">Layout shift events in the new Experience section</span><span class="sxs-lookup"><span data-stu-id="e3acb-197">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="e3acb-198">Der neue Abschnitt **"Erfahrung"** im **Bereich "Leistung"** hilft Ihnen, Layoutverschiebungen zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-198">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="e3acb-199">Kumulative Layoutverschiebung \(CLS\) ist eine Metrik, die Ihnen hilft, unerwünschte visuelle Instabilität zu quantifizieren.</span><span class="sxs-lookup"><span data-stu-id="e3acb-199">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="e3acb-200">Wählen Sie das **Layout shift-Ereignis** aus, um die Details der Layoutverschiebung im **Zusammenfassungsbereich** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-200">Choose the **Layout Shift** event to display the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="e3acb-201">Zeigen Sie auf die Felder **"Verschoben von"** und **"Verschoben",** um zu visualisieren, wo die Layoutverschiebung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e3acb-201">Hover on the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Die Details einer Layoutverschiebung" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="e3acb-203">Die Details einer Layoutverschiebung</span><span class="sxs-lookup"><span data-stu-id="e3acb-203">The details of a layout shift</span></span>  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a><span data-ttu-id="e3acb-204">Präzisere Zusageterminologie in der Konsole</span><span class="sxs-lookup"><span data-stu-id="e3acb-204">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="e3acb-205">Bei der Protokollierung eines `Promise` **Werts** wurde für die Konsole fälschlicherweise `PromiseStatus` ein Wert bereitgestellt, der auf `resolved` .</span><span class="sxs-lookup"><span data-stu-id="e3acb-205">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Ein Beispiel für die Konsole mit der alten aufgelösten Terminologie" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="e3acb-207">Ein Beispiel für die **Konsole** mit der alten `resolved` Terminologie</span><span class="sxs-lookup"><span data-stu-id="e3acb-207">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="e3acb-208">Die **Konsole** verwendet nun den `fulfilled` Begriff, der der Spezifikation entspricht. `Promise`</span><span class="sxs-lookup"><span data-stu-id="e3acb-208">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="e3acb-209">Weitere Informationen zur `Promise` Spezifikation, navigieren Sie zu ["Zustände" und "Zustände" auf GitHub.](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md)</span><span class="sxs-lookup"><span data-stu-id="e3acb-209">For more information about the `Promise` specification, navigate to [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Ein Beispiel für die Konsole mit der neuen erfüllten Terminologie" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="e3acb-211">Ein Beispiel für die **Konsole** mit der neuen `fulfilled` Terminologie</span><span class="sxs-lookup"><span data-stu-id="e3acb-211">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="e3acb-212">V8-Problem [#6751][CRV86751]</span><span class="sxs-lookup"><span data-stu-id="e3acb-212">V8 issue [#6751][CRV86751]</span></span>  

### <a name="styles-pane-updates"></a><span data-ttu-id="e3acb-213">Aktualisierungen des Formatvorlagenbereichs</span><span class="sxs-lookup"><span data-stu-id="e3acb-213">Styles pane updates</span></span>  

#### <a name="support-for-the-revert-keyword"></a><span data-ttu-id="e3acb-214">Unterstützung für das Revert-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="e3acb-214">Support for the revert keyword</span></span>  

<span data-ttu-id="e3acb-215">Die Benutzeroberfläche für automatisches Vervollständigen des Bereichs **"Formatvorlagen"** erkennt nun das [CSS-Schlüsselwort "Zurücksetzen",][MDNRevert] das den überlappenden Wert einer Eigenschaft auf den vorherigen Wert zurücksetzt, der auf die Formatierung des Elements angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e3acb-215">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Festlegen des Werts einer Eigenschaft, die wiederhergestellt werden soll" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="e3acb-217">Festlegen des Werts einer Eigenschaft, die wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="e3acb-217">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="e3acb-218">Chromium Problem [#1075437][CR1075437]</span><span class="sxs-lookup"><span data-stu-id="e3acb-218">Chromium issue [#1075437][CR1075437]</span></span>  

#### <a name="image-previews"></a><span data-ttu-id="e3acb-219">Bildvorschau</span><span class="sxs-lookup"><span data-stu-id="e3acb-219">Image previews</span></span>  

<span data-ttu-id="e3acb-220">Zeigen Sie auf einen `background-image` Wert im Bereich **"Formatvorlagen",** um eine Vorschau des Bilds in einer QuickInfo anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-220">Hover on a `background-image` value in the **Styles** pane to display a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Bewegen des Mauszeigers über einen Hintergrundbildwert" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="e3acb-222">Bewegen des Mauszeigers über einen `background-image` Wert</span><span class="sxs-lookup"><span data-stu-id="e3acb-222">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="e3acb-223">Chromium Problem [#1040019][CR1040019]</span><span class="sxs-lookup"><span data-stu-id="e3acb-223">Chromium issue [#1040019][CR1040019]</span></span>  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a><span data-ttu-id="e3acb-224">Die Farbauswahl verwendet jetzt eine durch Leerzeichen getrennte funktionale Farbschreibweise.</span><span class="sxs-lookup"><span data-stu-id="e3acb-224">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="e3acb-225">[Css Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()` , should support space-separated arguments.</span><span class="sxs-lookup"><span data-stu-id="e3acb-225">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="e3acb-226">So ist zum Beispiel `rgb(0, 0, 0)` gleichwertig mit `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="e3acb-226">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="e3acb-227">Wenn Sie Farben mit der [Farbauswahl][DevtoolsCssReferenceColorPicker] auswählen oder zwischen Farbdarstellungen im Bereich **"Formatvorlagen"** wechseln, indem Sie den Wert beibehalten `Shift` und `background-color` auswählen, wird die Durch Leerzeichen getrennte Argumentsyntax angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3acb-227">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, the space-separated argument syntax is displayed.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Verwenden von durch Leerzeichen getrennten Argumenten im Bereich "Formatvorlagen"" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="e3acb-229">Verwenden von durch Leerzeichen getrennten Argumenten im Bereich **"Formatvorlagen"**</span><span class="sxs-lookup"><span data-stu-id="e3acb-229">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="e3acb-230">Sie sollten auch die Syntax im **Bereich "Berechnet"** und in der QuickInfo zum **Prüfen des Modus** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-230">You should also display the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="e3acb-231">Microsoft Edge DevTools verwendet die neue Syntax, da anstehende CSS-Features wie [color()][CSSWGDraftsColor4Property] die veraltete Syntax von durch Kommas getrennten Argumenten nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e3acb-231">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="e3acb-232">Die Durch Leerzeichen getrennte Argumentsyntax wird in den meisten Browsern seit einer Weile unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3acb-232">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="e3acb-233">Navigieren Sie für weitere Informationen zu ["Kann ich folgendes verwenden: Durch Leerzeichen getrennte funktionale Farbschreibweise"?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span><span class="sxs-lookup"><span data-stu-id="e3acb-233">For more information, navigate to [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="e3acb-234">Chromium Problem [#1072952][CR1072952]</span><span class="sxs-lookup"><span data-stu-id="e3acb-234">Chromium issue [#1072952][CR1072952]</span></span>  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a><span data-ttu-id="e3acb-235">Veralteter Eigenschaftenbereich im Elementbereich</span><span class="sxs-lookup"><span data-stu-id="e3acb-235">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="e3acb-236">Der **Eigenschaftenbereich** **im** Elementtool ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="e3acb-236">The **Properties** pane in the **Elements** tool is deprecated.</span></span>  <span data-ttu-id="e3acb-237">Führen Sie `console.dir($0)` stattdessen in der **Konsole** aus.</span><span class="sxs-lookup"><span data-stu-id="e3acb-237">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Der veraltete Eigenschaftenbereich" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="e3acb-239">Der veraltete **Eigenschaftenbereich**</span><span class="sxs-lookup"><span data-stu-id="e3acb-239">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <a name="references"></a><span data-ttu-id="e3acb-240">Verweise</span><span class="sxs-lookup"><span data-stu-id="e3acb-240">References</span></span>  

*   [<span data-ttu-id="e3acb-241">console.dir()</span><span class="sxs-lookup"><span data-stu-id="e3acb-241">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="e3acb-242">0 USD</span><span class="sxs-lookup"><span data-stu-id="e3acb-242">$0</span></span>][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a><span data-ttu-id="e3acb-243">Unterstützung von App-Verknüpfungen im Manifestbereich</span><span class="sxs-lookup"><span data-stu-id="e3acb-243">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="e3acb-244">App-Verknüpfungen helfen Benutzern, allgemeine oder empfohlene Aufgaben innerhalb einer Web-App schnell zu starten.</span><span class="sxs-lookup"><span data-stu-id="e3acb-244">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="e3acb-245">Das Kontextmenü der App wird nur für [Progressive Web Apps][PwaIndex] angezeigt, die auf dem Desktop oder mobilen Gerät des Benutzers installiert sind.</span><span class="sxs-lookup"><span data-stu-id="e3acb-245">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="App-Verknüpfungen im Manifestbereich" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="e3acb-247">App-Verknüpfungen im **Manifestbereich**</span><span class="sxs-lookup"><span data-stu-id="e3acb-247">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="e3acb-248">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="e3acb-248">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="e3acb-249">Wenn Sie Windows oder macOS verwenden, sollten Sie die [Microsoft Edge Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="e3acb-249">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="e3acb-250">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="e3acb-250">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="e3acb-251">Kontakt mit Microsoft Edge Devtools-Team aufnehmen</span><span class="sxs-lookup"><span data-stu-id="e3acb-251">Getting in touch with Microsoft Edge Devtools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

<!--[DevtoolsWhatsNew201901Inspect]: ../../../whats-new/2019/01/devtools.md#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[DevtoolsConsoleApiDir]: ../../../console/api.md#dir "dir – Konsolen-API-Referenz | Microsoft-Dokumente"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]: ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Kürzlich ausgewähltes Element oder JavaScript-Objekt – Api-Referenz für Konsolenprogramme | Microsoft-Dokumente"  
[DevtoolsCssReferenceColorPicker]: ../../../css/reference.md#change-colors-with-the-color-picker "Ändern von Farben mit der Farbauswahl – CSS-Verweis | Microsoft-Dokumente"  
[DevtoolsDrawer]: ../../../customize/index.md#drawer "Schublade – Anpassen der Übersicht | Microsoft-Dokumente"  
[DevtoolsIndex]: ../../../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Suchen und Beheben von Problemen mit der Registerkarte &quot;Microsoft Edge DevTools-Probleme&quot; | Microsoft-Dokumente"  
[DevtoolsNetworkDetails]: ../../../network/index.md#inspect-the-details-of-the-resource "Überprüfen Sie die Details der Ressource | Microsoft-Dokumente"  
[DevtoolsNetworkLog]: ../../../network/index.md#log-network-activity "Protokollieren der | der Netzwerkaktivität Microsoft-Dokumente"  
[DevtoolsRemoteDebugAndroid]: ../../../remote-debugging/index.md "Erste Schritte mit Remotedebugging für Android-Geräte | Microsoft-Dokumente"  
[DevtoolsRemoteDebugDuoEmulator]: ../../../remote-debugging/surface-duo-emulator.md "Erste Schritte mit Surface Duo-Remotedebugging-Emulatoren | Microsoft-Dokumente"  
[DevtoolsRemoteDebugWindows]: ../../../remote-debugging/windows.md "Erste Schritte mit Remotedebugging Windows 10 Geräte | Microsoft-Dokumente"  

[PwaIndex]: ../../../../progressive-web-apps-chromium/index.md "Progressive Web-Apps unter Windows | Microsoft Docs"  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface Duo-Emulators | Microsoft-Dokumente"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge Android-App"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Durch Leerzeichen getrennte funktionale Farbschreibweise – MDN-| Kann ich verwenden?"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"

[CR174309]: https://crbug.com/174309 "DevTools: Anpassen von Tastenkombinationen/Tastenbindungen | Chromium Fehler"  
[CR963183]: https://crbug.com/963183 "DevTools sind nicht WCAG-konform | Chromium Fehler"  
[CR1040019]: https://crbug.com/1040019 "DevTools: Einfache Vorschau von Bildern und Hintergrundbildern im Bereich &quot;Formatvorlagen&quot; | Chromium Fehler"  
[CR1040025]: https://crbug.com/1040025 "DevTools: Zeigen Sie grundlegende a11y-Informationen im Elementpopover | Chromium Fehler"  
[CR1048378]: https://crbug.com/1048378 "DevTools-Ui-Unterstützung für den Modus &quot;Hoher Kontrast&quot; | Chromium Fehler"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Chromium Fehler"  
[CR1068116]: https://crbug.com/1068116 "Bereich &quot;Versandprobleme&quot; | Chromium Fehler"  
[CR1072952]: https://crbug.com/1072952 "DevTools: Farbauswahl sollte moderne CSS-Farbsyntax | Chromium Fehler"  
[CR1075437]: https://crbug.com/1075437 "DevTools: Fügen Sie Unterstützung für das CSS-Schlüsselwort/den Wert | Chromium Fehler"  
[CR1076112]: https://crbug.com/1076112 "Devtools-Personalisierung – Schubladen-Resizer"  
[CR1081486]: https://crbug.com/1081486 "Tastaturfokus für Navigationsschaltflächen im Screencastmodus nicht sichtbar | Chromium Fehler"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus sollte &quot;erfüllt&quot; und nicht &quot;aufgelöst&quot; | V8-Fehler"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Änderungen von Farben 3 – CSS-Farbmodul Ebene 4 | W3C-CSS-Arbeitsgruppen-Editor-Entwürfe"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Vordergrundfarbe: die &quot;Farbe&quot; – CSS-Farbmodul Ebene 4 | W3C-CSS-Arbeitsgruppen-Editor-Entwürfe"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Einführung in die neue Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Zustände und Zustände – domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "revertieren | Mdn"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Browserkompatibilität | Mdn"  

[VisualStudioCodeMain]: https://code.visualstudio.com/ "Visual Studio Code"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Tastenkombinationen für Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axt: Tastatur| WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axt: Name Role Value | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Aktivieren oder Deaktivieren des Modus für hohen Kontrast in Windows | Windows Unterstützung"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Posten eines Tweets"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools Twitter-Konto"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/Edge-Entwickler"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Vorschaukanäle"  
[TheWebWeWantMain]: https://aka.ms/webwewant "The Web We Want"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> <span data-ttu-id="e3acb-296">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3acb-296">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e3acb-297">Die ursprüngliche Seite ist [hier](https://developer.chrome.com/blog/new-in-devtools-84) zu finden und wurde von [Kaince Baskisch][KayceBasques] \(Technical Writer, Chrome DevTools \& Ausrufebereich\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3acb-297">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-84) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="e3acb-299">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e3acb-299">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
