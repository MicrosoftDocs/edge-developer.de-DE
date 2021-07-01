---
description: Hosten von Webinhalten in Win32-, .NET- und UWP-Apps mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge WebView2-Steuerelement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, browser control, edge html, Windows Forms, WinForms, WPF, .NET, WinUI, Project Re ré ré
ms.openlocfilehash: 64c835d0122a1c72e610efed2c060f7921a8e2b5
ms.sourcegitcommit: 5ae09b1ad6cd576c9fec12538b23cd849861f2b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "11627985"
---
# <a name="introduction-to-microsoft-edge-webview2"></a><span data-ttu-id="a3943-104">Einführung in Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="a3943-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="a3943-105">Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webtechnologien \(HTML, CSS und JavaScript\) in Ihre nativen Apps einbetten.</span><span class="sxs-lookup"><span data-stu-id="a3943-105">The Microsoft Edge WebView2 control allows you to embed web technologies \(HTML, CSS, and JavaScript\) in your native apps.</span></span>  <span data-ttu-id="a3943-106">Das WebView2-Steuerelement verwendet [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] als Renderingmodul, um den Webinhalt in systemeigenen Apps anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a3943-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native apps.</span></span>  <span data-ttu-id="a3943-107">Mit WebView2 können Sie Webcode in verschiedene Teile Ihrer systemeigenen App einbetten.</span><span class="sxs-lookup"><span data-stu-id="a3943-107">With WebView2, you may embed web code in different parts of your native app.</span></span>  <span data-ttu-id="a3943-108">Erstellen Sie die gesamte systemeigene App in einer einzelnen WebView-Instanz.</span><span class="sxs-lookup"><span data-stu-id="a3943-108">Build all of the native app within a single WebView instance.</span></span>  <span data-ttu-id="a3943-109">Informationen zum Erstellen einer WebView2-App finden Sie unter [Erste Schritte](#get-started).</span><span class="sxs-lookup"><span data-stu-id="a3943-109">For information on how to start building a WebView2 app, navigate to [Get Started](#get-started).</span></span>  

:::image type="complex" source="./media/WebView2/what-webview.png" alt-text="Was ist WebView?" lightbox="./media/WebView2/what-webview.png":::
   <span data-ttu-id="a3943-111">Was ist WebView?</span><span class="sxs-lookup"><span data-stu-id="a3943-111">What is WebView?</span></span>  
:::image-end:::    

## <a name="hybrid-app-approach"></a><span data-ttu-id="a3943-112">Hybrid-App-Ansatz</span><span class="sxs-lookup"><span data-stu-id="a3943-112">Hybrid app approach</span></span>  

<span data-ttu-id="a3943-113">Entwickler müssen sich häufig zwischen dem Erstellen einer Web-App oder einer nativen App entscheiden.</span><span class="sxs-lookup"><span data-stu-id="a3943-113">Developers must often decide between building a web app or a native app.</span></span>  <span data-ttu-id="a3943-114">Die Entscheidung hängt vom Kompromiss zwischen Reichweite und Energie ab.</span><span class="sxs-lookup"><span data-stu-id="a3943-114">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="a3943-115">Web-Apps ermöglichen eine breite Reichweite.</span><span class="sxs-lookup"><span data-stu-id="a3943-115">Web apps allow for a broad reach.</span></span>  <span data-ttu-id="a3943-116">Als Webentwickler können Sie den großteil ihres Codes auf verschiedenen Plattformen wiederverwenden.</span><span class="sxs-lookup"><span data-stu-id="a3943-116">As a Web developer, you may reuse most of your code across different platforms.</span></span>  <span data-ttu-id="a3943-117">Verwenden Sie eine systemeigene App, um auf alle Funktionen einer nativen Plattform zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a3943-117">To access the all capabilities of a native platform, use a native app.</span></span>  

:::image type="complex" source="./media/WebView2/web-native.png" alt-text="Systemeigenes Web" lightbox="./media/WebView2/web-native.png":::
   <span data-ttu-id="a3943-119">Systemeigenes Web</span><span class="sxs-lookup"><span data-stu-id="a3943-119">Web native</span></span>  
:::image-end:::    

<span data-ttu-id="a3943-120">Hybrid-Apps ermöglichen Es Entwicklern, das Beste aus beiden Welten zu genießen.</span><span class="sxs-lookup"><span data-stu-id="a3943-120">Hybrid apps allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="a3943-121">Hybrid-App-Entwickler profitieren von den folgenden Vorteilen.</span><span class="sxs-lookup"><span data-stu-id="a3943-121">Hybrid app developers benefit from the following advantages.</span></span>  

*   <span data-ttu-id="a3943-122">Die Spezifität und Stärke der Webplattform.</span><span class="sxs-lookup"><span data-stu-id="a3943-122">The ubiquity and strength of the web platform.</span></span>  
*   <span data-ttu-id="a3943-123">Die Leistungsfähigkeit und die vollständigen Funktionen der nativen Plattform.</span><span class="sxs-lookup"><span data-stu-id="a3943-123">The power and full capabilities of the native platform.</span></span>  
    
## <a name="webview2-benefits"></a><span data-ttu-id="a3943-124">WebView2-Vorteile</span><span class="sxs-lookup"><span data-stu-id="a3943-124">WebView2 benefits</span></span>   

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="web-ecosystem--skillset"></a><span data-ttu-id="a3943-125">Webökosystem & Skillset</span><span class="sxs-lookup"><span data-stu-id="a3943-125">Web ecosystem & skillset</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="rapid-innovation"></a><span data-ttu-id="a3943-126">Schnelle Innovation</span><span class="sxs-lookup"><span data-stu-id="a3943-126">Rapid innovation</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="windows-7-8-and-10-support"></a><span data-ttu-id="a3943-127">Windows 7-, 8- und 10-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a3943-127">Windows 7, 8, and 10 support</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="a3943-128">Nutzen Sie die gesamte Webplattform, Bibliotheken, Tools und Begabungen, die innerhalb des Webökosystems vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a3943-128">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="a3943-129">Die Webentwicklung ermöglicht eine schnellere Bereitstellung und Iteration.</span><span class="sxs-lookup"><span data-stu-id="a3943-129">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="a3943-130">Unterstützung für eine konsistente Benutzererfahrung in Windows 7, Windows 8 und Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a3943-130">Support for a consistent user experience across Windows 7, Windows 8, and Windows 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="native-capabilities"></a><span data-ttu-id="a3943-131">Systemeigene Funktionen</span><span class="sxs-lookup"><span data-stu-id="a3943-131">Native capabilities</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="code-sharing"></a><span data-ttu-id="a3943-132">Codefreigabe</span><span class="sxs-lookup"><span data-stu-id="a3943-132">Code-sharing</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="microsoft-support"></a><span data-ttu-id="a3943-133">Microsoft-Support</span><span class="sxs-lookup"><span data-stu-id="a3943-133">Microsoft support</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="a3943-134">Greifen Sie auf den vollständigen Satz systemeigener APIs zu.</span><span class="sxs-lookup"><span data-stu-id="a3943-134">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="a3943-135">Das Hinzufügen von Webcode zu Ihrer Codebasis ermöglicht eine höhere Wiederverwendung auf mehreren Plattformen.</span><span class="sxs-lookup"><span data-stu-id="a3943-135">Add web code to your codebase allows for increased reuse across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="a3943-136">Microsoft bietet Unterstützung und fügt neue Featureanforderungen hinzu, wenn WebView2 unter Allgemein verfügbar \(GA\) veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="a3943-136">Microsoft provides support and adds new feature requests when WebView2 releases at Generally Availability \(GA\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="evergreen-distribution"></a><span data-ttu-id="a3943-137">Evergreen-Verteilung</span><span class="sxs-lookup"><span data-stu-id="a3943-137">Evergreen distribution</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="fixed"></a><span data-ttu-id="a3943-138">Behoben</span><span class="sxs-lookup"><span data-stu-id="a3943-138">Fixed</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="incremental-adoption"></a><span data-ttu-id="a3943-139">Inkrementelle Einführung</span><span class="sxs-lookup"><span data-stu-id="a3943-139">Incremental adoption</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="a3943-140">Verlassen Sie sich auf eine aktuelle Version von Chromium mit regelmäßigen Plattformupdates und Sicherheitspatches.</span><span class="sxs-lookup"><span data-stu-id="a3943-140">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="a3943-141">\(in Kürze verfügbar\) Wählen Sie aus, ob Sie die Chromium Bits in Ihrer App verpacken möchten.</span><span class="sxs-lookup"><span data-stu-id="a3943-141">\(coming soon\)  Choose to package the Chromium bits in your app.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="a3943-142">Fügen Sie Ihrer App Webkomponenten nach und nach hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3943-142">Add web components piece by piece to your app.</span></span>  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a><span data-ttu-id="a3943-143">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="a3943-143">Get started</span></span>  

<span data-ttu-id="a3943-144">Um Ihre App mithilfe des WebView2-Steuerelements zu erstellen und zu testen, müssen Sie</span><span class="sxs-lookup"><span data-stu-id="a3943-144">To build and test your app using the WebView2 control, you need to have</span></span> <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  --><span data-ttu-id="a3943-145">[WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installiert.</span><span class="sxs-lookup"><span data-stu-id="a3943-145">the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="a3943-146">Wählen Sie eine der folgenden Optionen aus, um loszulegen.</span><span class="sxs-lookup"><span data-stu-id="a3943-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="a3943-147">Erste Schritte mit Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="a3943-147">Get Started with Win32 C/C++</span></span>][Webview2GetStartedWin32]  
*   [<span data-ttu-id="a3943-148">Erste Schritte mit WPF</span><span class="sxs-lookup"><span data-stu-id="a3943-148">Get Started with WPF</span></span>][Webview2GetStartedWpf]  
*   [<span data-ttu-id="a3943-149">Erste Schritte mit WinForms</span><span class="sxs-lookup"><span data-stu-id="a3943-149">Get Started with WinForms</span></span>][Webview2GetStartedWinforms]  
*   [<span data-ttu-id="a3943-150">Erste Schritte mit WinUI3</span><span class="sxs-lookup"><span data-stu-id="a3943-150">Get Started with WinUI3</span></span>][Webview2GetStartedWinui]  
    
<span data-ttu-id="a3943-151">Das [WebView2 Samples-Repository][GithubMicrosoftedgeWebview2samples] enthält Beispiele, die alle WebView2 SDK-Features und API-Verwendungsmuster veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="a3943-151">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="a3943-152">Wenn dem WebView2 SDK weitere Features hinzugefügt werden, werden die Beispiel-Apps aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a3943-152">As more features are added to the WebView2 SDK, the sample apps will be updated.</span></span>  

## <a name="supported-platforms"></a><span data-ttu-id="a3943-153">Unterstützte Plattformen</span><span class="sxs-lookup"><span data-stu-id="a3943-153">Supported platforms</span></span>  

<span data-ttu-id="a3943-154">Eine Allgemeine Verfügbarkeit \(GA\) oder Vorschauversion ist in den folgenden Programmierumgebungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a3943-154">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="a3943-155">Win32 C/C++ \(GA\)</span><span class="sxs-lookup"><span data-stu-id="a3943-155">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="a3943-156">.NET Framework 4.5 oder höher</span><span class="sxs-lookup"><span data-stu-id="a3943-156">.NET Framework 4.5 or later</span></span>  
*   <span data-ttu-id="a3943-157">.NET Core 3.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="a3943-157">.NET Core 3.1 or later</span></span>  
*   <span data-ttu-id="a3943-158">.NET 5</span><span class="sxs-lookup"><span data-stu-id="a3943-158">.NET 5</span></span>  
*   <span data-ttu-id="a3943-159">[WinUI 3.0][UwpToolkitsWinui3] \(Vorschau\)</span><span class="sxs-lookup"><span data-stu-id="a3943-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  
    
<span data-ttu-id="a3943-160">Sie können WebView2-Apps in den folgenden Versionen von Windows ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3943-160">You may run WebView2 apps on the following versions of Windows.</span></span>  

*   <span data-ttu-id="a3943-161">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a3943-161">Windows 10</span></span>  
*   <span data-ttu-id="a3943-162">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a3943-162">Windows 8.1</span></span>  
*   <span data-ttu-id="a3943-163">Windows 7 \*\*</span><span class="sxs-lookup"><span data-stu-id="a3943-163">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="a3943-164">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="a3943-164">Windows Server 2019</span></span>  
*   <span data-ttu-id="a3943-165">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a3943-165">Windows Server 2016</span></span>  
*   <span data-ttu-id="a3943-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3943-166">Windows Server 2012</span></span>  
*   <span data-ttu-id="a3943-167">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a3943-167">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="a3943-168">Windows Server 2008 R2 \*\*</span><span class="sxs-lookup"><span data-stu-id="a3943-168">Windows Server 2008 R2 \*\*</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="a3943-169">\*\* WebView2-Unterstützung für Windows 7 und Windows Server 2008 R2 hat den gleichen Supportzyklus wie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a3943-169">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="a3943-170">Weitere Informationen erhalten Sie, wenn Sie zu [Microsoft Edge unterstützten Betriebssystemen][DeployedgeMicrosoftEdgeSupportedOS]navigieren.</span><span class="sxs-lookup"><span data-stu-id="a3943-170">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="a3943-171">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="a3943-171">Next steps</span></span>  

<span data-ttu-id="a3943-172">Weitere Informationen zum Erstellen und Bereitstellen von WebView2-Apps finden Sie in der konzeptionellen Dokumentation und den Anleitungen.</span><span class="sxs-lookup"><span data-stu-id="a3943-172">For more information on how to build and deploy WebView2 apps, review the conceptual documentation and how-to guides.</span></span>  

### <a name="concepts"></a><span data-ttu-id="a3943-173">Konzepte</span><span class="sxs-lookup"><span data-stu-id="a3943-173">Concepts</span></span>  

*   [<span data-ttu-id="a3943-174">Grundlegendes zu WebView2 SDK-Versionen</span><span class="sxs-lookup"><span data-stu-id="a3943-174">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]  
*   [<span data-ttu-id="a3943-175">Verteilung von Apps mit WebView2</span><span class="sxs-lookup"><span data-stu-id="a3943-175">Distribution of apps using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="a3943-176">Bewährte Methoden für die Entwicklung sicherer WebView2-Apps</span><span class="sxs-lookup"><span data-stu-id="a3943-176">Best practices for developing secure WebView2 apps</span></span>][Webview2ConceptsSecurity]  
*   [<span data-ttu-id="a3943-177">Verwalten des Benutzerdatenordners in WebView2-Apps</span><span class="sxs-lookup"><span data-stu-id="a3943-177">Manage User Data Folder in WebView2 apps</span></span>][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a><span data-ttu-id="a3943-178">How-To Handbücher</span><span class="sxs-lookup"><span data-stu-id="a3943-178">How-To guides</span></span>  

*   [<span data-ttu-id="a3943-179">Debuggen mit WebView2</span><span class="sxs-lookup"><span data-stu-id="a3943-179">How to Debug with WebView2</span></span>][Webview2HowToDebug]  
*   [<span data-ttu-id="a3943-180">Automatisieren und Testen von WebView2 mit Microsoft Edge-Treiber</span><span class="sxs-lookup"><span data-stu-id="a3943-180">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="a3943-181">Kontakt mit dem Microsoft Edge WebView-Team aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a3943-181">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Verteilung von Apps mitHilfe von WebView2 | Microsoft-Dokumente"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Bewährte Methoden für die Entwicklung sicherer WebView2-Apps | Microsoft-Dokumente"  
[Webview2ConceptsUserDataFolder]: ./concepts/user-data-folder.md "Verwalten des Benutzerdatenordners | Microsoft-Dokumente"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Grundlegendes zu WebView2 SDK-Versionen | Microsoft-Dokumente"  
[Webview2GetStartedWin32]: ./get-started/win32.md "Erste Schritte mit WebView2 | Microsoft-Dokumente"  
[Webview2GetStartedWinforms]: ./get-started/winforms.md "Erste Schritte mit WebView2 in Windows Forms-Apps (Vorschau) | Microsoft-Dokumente"  
[Webview2GetStartedWinui]: ./get-started/winui.md "Erste Schritte mit WebView2 in WinUI3 (Vorschau) | Microsoft-Dokumente"  
[Webview2GetStartedWpf]: ./get-started/wpf.md "Erste Schritte mit WebView2 in WPF (Vorschau) | Microsoft-Dokumente"  
[Webview2HowToDebug]: ./how-to/debug.md "Debuggen mit WebView2-| Microsoft-Dokumente"  
[Webview2HowToWebdriver]: ./how-to/webdriver.md "Automatisieren und Testen von WebView2 mit Microsoft Edge Driver | Microsoft-Dokumente"  
[Webview2ReleaseNotes]: ./release-notes.md "Versionshinweise für WebView2 SDK-| Microsoft-Dokumente"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows UI Library 3 Preview 2 (Juli 2020) | Microsoft-Dokumente"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Microsoft Edge unterstützte Betriebssystem-| Microsoft-Dokumente"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | NuGet Galerie"  
