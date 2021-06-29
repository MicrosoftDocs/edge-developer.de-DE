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
# <a name="experimental-features"></a><span data-ttu-id="17b37-104">Experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="17b37-104">Experimental features</span></span>  

<span data-ttu-id="17b37-105">Microsoft Edge DevTools bieten Zugriff auf experimentelle Features, die sich noch in der Entwicklung befinden.</span><span class="sxs-lookup"><span data-stu-id="17b37-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="17b37-106">Sie können testen und [Feedback geben,](#providing-feedback-on-experimental-features) bevor jedes Feature veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="17b37-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="17b37-107">Obwohl experimentelle Features in allen Kanälen von Microsoft Edge verfügbar sind, erhalten Sie möglicherweise die neuesten experimentellen Features mithilfe der Microsoft Edge Canary Channel.</span><span class="sxs-lookup"><span data-stu-id="17b37-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="17b37-108">Aktivieren experimenteller Features</span><span class="sxs-lookup"><span data-stu-id="17b37-108">Turn on experimental features</span></span>  

<span data-ttu-id="17b37-109">Führen Sie die folgenden Schritte aus, um experimentelle Features in Microsoft Edge zu aktivieren( oder zu deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="17b37-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="17b37-110">[Öffnen Sie DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="17b37-110">[Open DevTools][DevtoolsOpenIndex].</span></span>  
    *   <span data-ttu-id="17b37-111">Wählen Sie `Control` + `Shift` + `I` \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="17b37-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="17b37-112">Navigieren Sie zu [Microsoft Edge DevTools-Tastenkombinationen,][DevtoolsShortcutsIndex]um weitere Informationen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="17b37-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="17b37-113">Öffnen Sie den [bereich Einstellungen.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="17b37-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="17b37-114">Wählen Sie `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="17b37-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="17b37-115">Navigieren Sie zu [Microsoft Edge DevTools-Tastenkombinationen,][DevtoolsShortcutsIndex]um weitere Informationen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="17b37-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="17b37-116">Wählen Sie auf der linken Seite des **Einstellungen** Bereichs den Abschnitt **"Experimente"** aus.</span><span class="sxs-lookup"><span data-stu-id="17b37-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Seite "Experimente" in Einstellungen" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="17b37-118">Seite **"Experimente"** in **Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="17b37-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="17b37-119">Scrollen Sie auf der Seite **"Experimente"** durch die Liste aller verfügbaren experimentellen Features, und aktivieren Sie das Kontrollkästchen neben jedem Feature, das Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="17b37-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="17b37-120">Schließen Sie Microsoft Edge DevTools, und öffnen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="17b37-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="17b37-121">Experimentelle Features werden ständig aktualisiert und können Leistungsprobleme verursachen.</span><span class="sxs-lookup"><span data-stu-id="17b37-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="17b37-122">Um ein experimentelles Feature zu deaktivieren, öffnen Sie die Seite **"Experimente",** und deaktivieren Sie das Kontrollkästchen des experimentellen Features, das Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="17b37-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="17b37-123">Hervorgehobene experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="17b37-123">Highlighted experimental features</span></span>  

<span data-ttu-id="17b37-124">In den folgenden Abschnitten werden die neuen experimentellen Features beschrieben, die in Microsoft Edge verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="17b37-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="17b37-125">Experimentelles Feature</span><span class="sxs-lookup"><span data-stu-id="17b37-125">Experimental feature</span></span> | <span data-ttu-id="17b37-126">Microsoft Edge Version</span><span class="sxs-lookup"><span data-stu-id="17b37-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [Enable webhint](#enable-webhint) | <span data-ttu-id="17b37-127">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="17b37-127">85 or later</span></span> |  
| [Enable Network Console](#enable-network-console) | <span data-ttu-id="17b37-128">85 oder höher</span><span class="sxs-lookup"><span data-stu-id="17b37-128">85 or later</span></span> |  
| [Source Order Viewer](#source-order-viewer) | <span data-ttu-id="17b37-129">86 oder höher</span><span class="sxs-lookup"><span data-stu-id="17b37-129">86 or later</span></span> |  
| [Enable Composited Layers in 3D View](#enable-composited-layers-in-3d-view) | <span data-ttu-id="17b37-130">87 oder höher</span><span class="sxs-lookup"><span data-stu-id="17b37-130">87 or later</span></span> |  
| [Enable new Font Editor tool within the Styles pane](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="17b37-131">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="17b37-131">89 or later</span></span> |  
| [Enable new CSS Flexbox debugging features](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="17b37-132">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="17b37-132">89 or later</span></span> |  
| [Enable + button tab menus to open more tools](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="17b37-133">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="17b37-133">89 or later</span></span> |  
| [Enable Welcome tab](#enable-welcome-tab) | <span data-ttu-id="17b37-134">89 oder höher</span><span class="sxs-lookup"><span data-stu-id="17b37-134">89 or later</span></span> |  

### Enable webhint  

<span data-ttu-id="17b37-135">[Webhint][WebhintMain] ist ein Open-Source-Tool, das Feedback in Echtzeit für Websites und lokale Webseiten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="17b37-135">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="17b37-136">Die Art des Von Webhint bereitgestellten [Feedbacks.][WebhintMain]</span><span class="sxs-lookup"><span data-stu-id="17b37-136">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="17b37-137">Bedienungshilfen</span><span class="sxs-lookup"><span data-stu-id="17b37-137">accessibility</span></span>  
*   <span data-ttu-id="17b37-138">Browserübergreifende Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="17b37-138">cross-browser compatibility</span></span>  
*   <span data-ttu-id="17b37-139">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="17b37-139">security</span></span>  
*   <span data-ttu-id="17b37-140">Leistung</span><span class="sxs-lookup"><span data-stu-id="17b37-140">performance</span></span>  
*   <span data-ttu-id="17b37-141">Progressive Web Apps (PWAs)</span><span class="sxs-lookup"><span data-stu-id="17b37-141">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="17b37-142">Andere allgemeine Probleme bei der Webentwicklung</span><span class="sxs-lookup"><span data-stu-id="17b37-142">other common web development issues</span></span>  
    
<span data-ttu-id="17b37-143">Das [Webhint-Experiment][WebhintMain] zeigt das Webhint-Feedback im [Bereich "Probleme"][DevtoolsIssuesIndex] an.</span><span class="sxs-lookup"><span data-stu-id="17b37-143">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssuesIndex] panel.</span></span>  <span data-ttu-id="17b37-144">Wählen Sie ein Problem aus, um die Lösungsdokumentation und eine Liste der betroffenen Ressourcen auf Ihrer Website anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="17b37-144">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="17b37-145">Wählen Sie einen Ressourcenlink aus, um den relevanten **Bereich "Netzwerk",** **"Quellen"** oder **"Elemente"** in DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="17b37-145">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="Webhint-Feedback im Bereich "Probleme"" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="17b37-147">Webhint-Feedback im **Bereich "Probleme"**</span><span class="sxs-lookup"><span data-stu-id="17b37-147">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Enable Network Console  

<span data-ttu-id="17b37-148">**Die Netzwerkkonsole** ist der Arbeitstitel eines Experiments für synthetische Netzwerkanforderungen über HTTP.</span><span class="sxs-lookup"><span data-stu-id="17b37-148">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="17b37-149">Sie können das **Netzwerkkonsolen-Experiment** verwenden, um Web-API-Anforderungen zu senden.</span><span class="sxs-lookup"><span data-stu-id="17b37-149">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="17b37-150">Stellen Sie nach dem Aktivieren des Experiments sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="17b37-150">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="17b37-151">Führen Sie die folgenden Schritte aus, um die **Netzwerkkonsole**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="17b37-151">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="17b37-152">Öffnen Sie den **Netzwerkbereich.**</span><span class="sxs-lookup"><span data-stu-id="17b37-152">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="17b37-153">Suchen Sie die Netzwerkanforderung, die Sie ändern und erneut senden möchten.</span><span class="sxs-lookup"><span data-stu-id="17b37-153">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="17b37-154">Öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **Bearbeiten und Wiedergeben**aus.</span><span class="sxs-lookup"><span data-stu-id="17b37-154">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="17b37-155">Wenn die **Netzwerkkonsole** geöffnet wird, bearbeiten Sie die Netzwerkanforderungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="17b37-155">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="17b37-156">Wählen Sie **"Senden"** aus.</span><span class="sxs-lookup"><span data-stu-id="17b37-156">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Netzwerkkonsole in der Konsolenschublade" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="17b37-158">**Netzwerkkonsole** in der **Konsolenschublade**</span><span class="sxs-lookup"><span data-stu-id="17b37-158">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Source Order Viewer  

<span data-ttu-id="17b37-159">**Source Order Viewer** ist ein Experiment, das die Reihenfolge der Elemente in der Webseitenquelle anzeigt.</span><span class="sxs-lookup"><span data-stu-id="17b37-159">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="17b37-160">Die Anzeigereihenfolge auf dem Bildschirm kann sich von der Reihenfolge der Quelle unterscheiden, was die Bildschirmleseprogramme und Tastaturbenutzer verwirren kann.</span><span class="sxs-lookup"><span data-stu-id="17b37-160">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="17b37-161">Verwenden Sie das **Source Order Viewer** Experiment, um die Unterschiede zwischen der Bildschirmanzeigereihenfolge und der Reihenfolge der Quelle zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="17b37-161">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="17b37-162">Stellen Sie nach dem Aktivieren des Experiments sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="17b37-162">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="17b37-163">Führen Sie die folgenden Schritte aus, um dies zu **Source Order Viewer** verwenden.</span><span class="sxs-lookup"><span data-stu-id="17b37-163">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="17b37-164">Öffnen Sie **das** Elementtool.</span><span class="sxs-lookup"><span data-stu-id="17b37-164">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="17b37-165">Wählen Sie rechts neben der Registerkarte **"Formatvorlagen"** die Registerkarte **"Barrierefreiheit"** aus.</span><span class="sxs-lookup"><span data-stu-id="17b37-165">To the right of the **Styles** tab, select the **Accessibility** tab.</span></span>  
1.  <span data-ttu-id="17b37-166">Aktivieren Sie im **Source Order Viewer** Abschnitt das Kontrollkästchen **"Quellreihenfolge anzeigen".**</span><span class="sxs-lookup"><span data-stu-id="17b37-166">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="17b37-167">Markieren Sie jedes HTML-Element, um eine Überlagerung anzuzeigen, die in der Reihenfolge in der Webseitenquelle angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="17b37-167">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text=":::<span data-ttu-id="17b37-168">no-loc(Source Order Viewer)::: in the Accessibility pane" lightbox=". /media/experiments-source-order-viewer.msft.png"::: im **Source Order Viewer** Bereich **"Barrierefreiheit"**</span><span class="sxs-lookup"><span data-stu-id="17b37-168">no-loc(Source Order Viewer)::: in the Accessibility pane" lightbox="../media/experiments-source-order-viewer.msft.png"::: **Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Enable Composited Layers in 3D View  

<span data-ttu-id="17b37-169">Sie können Layer jetzt zusammen mit Z-Indizes und dem Dokumentobjektmodell \(DOM\) visualisieren.</span><span class="sxs-lookup"><span data-stu-id="17b37-169">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="17b37-170">Dieses Feature hilft Ihnen beim Debuggen, ohne den Kontext so oft zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="17b37-170">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="17b37-171">Sie haben festgestellt, dass die Reduzierung des Kontextwechsels ein wichtiger Problempunkt war.</span><span class="sxs-lookup"><span data-stu-id="17b37-171">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="17b37-172">Es ist nicht immer klar, wie sich der von Ihnen geschriebene Code auf Ihre Web-App auswirkt.</span><span class="sxs-lookup"><span data-stu-id="17b37-172">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="17b37-173">Für ein umfassendes visuelles Debugging werden jetzt die 3D View zusammengesetzten Layer kombiniert.</span><span class="sxs-lookup"><span data-stu-id="17b37-173">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="17b37-174">Stellen Sie nach dem Aktivieren des Experiments sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="17b37-174">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="17b37-175">Führen Sie die folgenden Schritte aus, um **zusammengesetzte Layer**zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="17b37-175">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="17b37-176">Wählen Sie in der Schublade das **3D View** Tool aus.</span><span class="sxs-lookup"><span data-stu-id="17b37-176">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="17b37-177">Öffnen Sie den Bereich **"Zusammengesetzte Ebenen".**</span><span class="sxs-lookup"><span data-stu-id="17b37-177">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="17b37-178">Alle gezeichneten Ebenen der App werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17b37-178">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="17b37-179">Testen Sie dieses Feature mit Ihren eigenen Web-Apps.</span><span class="sxs-lookup"><span data-stu-id="17b37-179">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Bereich „Zusammengesetzte Ebenen“" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="17b37-181">Bereich **Zusammengesetzte Ebenen**</span><span class="sxs-lookup"><span data-stu-id="17b37-181">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Enable new Font Editor tool within the Styles pane  

<span data-ttu-id="17b37-182">Sie können jetzt den neuen visuellen [Schriftarten-Editor][DevtoolsInspectStylesEditFonts] verwenden, um Schriftarten zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="17b37-182">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="17b37-183">Verwenden Sie sie, um Schriftarten und Schriftartmerkmale zu definieren.</span><span class="sxs-lookup"><span data-stu-id="17b37-183">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="17b37-184">Mit dem visuellen **Schriftarten-Editor** können Sie die folgenden Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="17b37-184">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="17b37-185">Wechseln zwischen Einheiten für unterschiedliche Schriftarteigenschaften</span><span class="sxs-lookup"><span data-stu-id="17b37-185">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="17b37-186">Wechseln zwischen Schlüsselwörtern für unterschiedliche Schriftarteigenschaften</span><span class="sxs-lookup"><span data-stu-id="17b37-186">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="17b37-187">Konvertieren von Einheiten</span><span class="sxs-lookup"><span data-stu-id="17b37-187">Convert units</span></span>  
*   <span data-ttu-id="17b37-188">Generieren von genauem CSS-Code</span><span class="sxs-lookup"><span data-stu-id="17b37-188">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="17b37-189">Stellen Sie nach dem Aktivieren des Experiments sicher, dass Sie die DevTools neu starten.</span><span class="sxs-lookup"><span data-stu-id="17b37-189">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="17b37-190">Führen Sie die folgenden Schritte aus, um den neuen visuellen **Schriftarten-Editor zu**verwenden.</span><span class="sxs-lookup"><span data-stu-id="17b37-190">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="17b37-191">Öffnen Sie **das** Elementtool.</span><span class="sxs-lookup"><span data-stu-id="17b37-191">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="17b37-192">Öffnen Sie den Bereich **"Formatvorlagen".**</span><span class="sxs-lookup"><span data-stu-id="17b37-192">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="17b37-193">Klicken Sie auf das **Schriftarten-Editor-Symbol.**</span><span class="sxs-lookup"><span data-stu-id="17b37-193">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="17b37-194">For more information about the new visual **Font Editor**, navigate to Edit CSS font styles and settings in the Styles pane [in DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="17b37-194">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Der Bereich des visuellen Schriftarten-Editors ist hervorgehoben." lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="17b37-196">Der Bereich des visuellen **Schriftarten-Editors** ist hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="17b37-196">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable new CSS Flexbox debugging features  

<span data-ttu-id="17b37-197">Dieses experimentelle Feature bietet viele neue Visualisierungen, die Ihnen beim Debuggen von CSS-Flexbox-Layouts helfen.</span><span class="sxs-lookup"><span data-stu-id="17b37-197">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="17b37-198">Um eine Vorschau der neuesten experimentellen Features anzuzeigen, [aktivieren Sie dieses Experiment,](#turn-on-experimental-features) und laden Sie DevTools neu.</span><span class="sxs-lookup"><span data-stu-id="17b37-198">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="17b37-199">Anzeigen persistenter Überlagerungen auf Flexbox-Layouts mit dem Inspect-Tool</span><span class="sxs-lookup"><span data-stu-id="17b37-199">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="17b37-200">Das **Inspect-Tool** bietet eine schnelle Möglichkeit, CSS Flexbox-Layouts in einer Website zu identifizieren und zu visualisieren, indem Sie mit der Maus darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="17b37-200">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="17b37-201">Klicken Sie in der oberen linken Ecke von DevTools auf das Symbol **"Überprüfen** ![ \( Überprüfen ](../media/inspect-icon.msft.png) \)".</span><span class="sxs-lookup"><span data-stu-id="17b37-201">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="17b37-202">Zeigen Sie dann beim Debuggen der Website auf einen Flex-Container, um Gliederungen um den Flex-Container anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="17b37-202">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Anzeigen von Flexbox-Containern mit dem Inspect-Tool" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="17b37-204">Anzeigen von Flexbox-Containern mit dem **Inspect-Tool**</span><span class="sxs-lookup"><span data-stu-id="17b37-204">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="17b37-205">Anzeigen persistenter Überlagerungen in Flexbox-Layouts</span><span class="sxs-lookup"><span data-stu-id="17b37-205">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="17b37-206">In Microsoft Edge Version 89 oder höher bietet das experimentelle CSS-Flexbox-Feature auch die Möglichkeit, persistente Überlagerungen für Flexbox-Layouts zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="17b37-206">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="17b37-207">Persistente Überlagerungen bieten die folgenden Vorteile.</span><span class="sxs-lookup"><span data-stu-id="17b37-207">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="17b37-208">Persistente Überlagerungen bleiben auf der Webseite sichtbar, während Sie scrollen, die Maus bewegen und andere Features der DevTools verwenden.</span><span class="sxs-lookup"><span data-stu-id="17b37-208">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="17b37-209">Mehrere persistente Überlagerungen können gleichzeitig verwendet werden, damit Sie mehrere Flexbox-Layouts gleichzeitig überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="17b37-209">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="17b37-210">Persistente Überlagerungen bieten Optionen für die Farbkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="17b37-210">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="17b37-211">Verwenden Sie eine der folgenden Aktionen, um beständige Überlagerungen im Flexbox-Layout umzuschalten.</span><span class="sxs-lookup"><span data-stu-id="17b37-211">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="17b37-212">Wählen Sie das **Flexbox-Ovalsymbol** neben einem beliebigen Flexbox-Container aus, der in der DOM-Struktur des **Elements-Tools** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="17b37-212">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="17b37-213">Öffnen Sie den neuen **Layoutbereich** im **Elementtool,** und aktivieren Sie das Kontrollkästchen neben jedem Flexbox-Container, den Sie hervorheben möchten.</span><span class="sxs-lookup"><span data-stu-id="17b37-213">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Flex-Symbole und Layoutpanel in DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="17b37-215">Flex-Symbole und **Layoutpanel** in DevTools</span><span class="sxs-lookup"><span data-stu-id="17b37-215">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="17b37-216">Konfigurieren persistenter Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="17b37-216">Configure persistent overlays</span></span>  

<span data-ttu-id="17b37-217">Verwenden Sie den **Layoutbereich,** um Optionen für persistente Überlagerungen für CSS-Raster oder Flexbox-Layouts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="17b37-217">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="17b37-218">Der **Layoutbereich** befindet sich im **Elementtool** neben den Bereichen **"Formatvorlagen"** und **"Berechnet".**</span><span class="sxs-lookup"><span data-stu-id="17b37-218">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Layoutpanel" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="17b37-220">Layoutpanel</span><span class="sxs-lookup"><span data-stu-id="17b37-220">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable + button tab menus to open more tools  

<span data-ttu-id="17b37-221">Sie können jetzt weitere Tools mit dem neuen Symbol **"Weitere Tools** \( `+` \)" öffnen.</span><span class="sxs-lookup"><span data-stu-id="17b37-221">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="17b37-222">Nachdem Sie das Experiment aktiviert **Enable + button tab menus to open more tools** und DevTools neu geladen haben, wird rechts `+` neben der Registerkartengruppe oben in den DevTools ein Pluszeichen \( \) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17b37-222">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="17b37-223">Um eine Liste anderer Tools anzuzeigen, die Sie der Registerkartenleiste hinzufügen können, wählen Sie das neue Symbol **"Weitere Tools** \( `+` \) " aus.</span><span class="sxs-lookup"><span data-stu-id="17b37-223">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Weitere Tools im oberen Bereich" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="17b37-225">**Weitere Tools** im oberen Bereich</span><span class="sxs-lookup"><span data-stu-id="17b37-225">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable Welcome tab

<span data-ttu-id="17b37-226">Dieses Experiment ersetzt das Tool **"Neuigkeiten"** durch das neue **Willkommenstool.**</span><span class="sxs-lookup"><span data-stu-id="17b37-226">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="17b37-227">Es wird ein aktualisiertes Design für den folgenden Inhalt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17b37-227">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="17b37-228">Links zu Entwicklerdokumenten</span><span class="sxs-lookup"><span data-stu-id="17b37-228">Links to developer docs</span></span>  
*   <span data-ttu-id="17b37-229">Die neuesten Features</span><span class="sxs-lookup"><span data-stu-id="17b37-229">the latest features</span></span>  
*   <span data-ttu-id="17b37-230">Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="17b37-230">release notes</span></span>  
*   <span data-ttu-id="17b37-231">Option zum Kontaktieren des Microsoft Edge DevTools-Teams</span><span class="sxs-lookup"><span data-stu-id="17b37-231">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="17b37-232">Das **Willkommenstool** wird nach jedem Update für Microsoft Edge automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="17b37-232">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="17b37-233">Um zu verhindern, \*\*\*\* dass das Willkommens-Tool nach jedem Update angezeigt wird, deaktivieren Sie das Kontrollkästchen neben der **Registerkarte "Öffnen" nach jedem Update** unter dem Titel des **Willkommenstools.**</span><span class="sxs-lookup"><span data-stu-id="17b37-233">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="17b37-234">Wenn Sie das ursprüngliche Tool **"What's New"** bevorzugen, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings]  >  **Experiments,** und entfernen Sie das Kontrollkästchen neben **Enable Welcome tab** .</span><span class="sxs-lookup"><span data-stu-id="17b37-234">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Willkommens-Tool" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="17b37-236">**Willkommens-Tool**</span><span class="sxs-lookup"><span data-stu-id="17b37-236">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="17b37-237">Frühere experimentelle Features</span><span class="sxs-lookup"><span data-stu-id="17b37-237">Previous experimental features</span></span>  

*   <span data-ttu-id="17b37-238">[3D View][Devtools3dViewIndex]ist jetzt in Microsoft Edge Version 83 oder höher standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="17b37-238">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="17b37-239">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex]ist jetzt in Microsoft Edge Version 85 oder höher standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="17b37-239">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="17b37-240">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]ist jetzt in Microsoft Edge Version 86 oder höher standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="17b37-240">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="17b37-241">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]ist jetzt in Microsoft Edge Version 89 oder höher standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="17b37-241">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="17b37-242">[Turn on new CSS grid debugging features][DevtoolsCssGrid]ist jetzt in Microsoft Edge Version 89 oder höher standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="17b37-242">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="17b37-243">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables]ist jetzt in Microsoft Edge Version 90 oder höher standardmäßig verfügbar und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="17b37-243">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 90 or later.</span></span>  

## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="17b37-244">Bereitstellen von Feedback zu experimentellen Features</span><span class="sxs-lookup"><span data-stu-id="17b37-244">Providing feedback on experimental features</span></span>  

<span data-ttu-id="17b37-245">Um Feedback zu Microsoft Edge DevTools-Experimenten oder zu anderen mit DevTools verbundenen Themen zu geben.</span><span class="sxs-lookup"><span data-stu-id="17b37-245">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="17b37-246">Senden Sie Ihr Feedback über das Symbol **"Feedback senden"** in den DevTools.</span><span class="sxs-lookup"><span data-stu-id="17b37-246">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="17b37-247">Tweet bei [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="17b37-247">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol Feedback senden in den Microsoft Edge-Entwicklungstools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="17b37-249">Das Symbol **Feedback senden** in den Microsoft Edge-Entwicklungstools</span><span class="sxs-lookup"><span data-stu-id="17b37-249">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
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
