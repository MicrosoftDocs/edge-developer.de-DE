---
description: IE-Modus und die Microsoft Edge (Chromium) DevTools
title: Internet Explorer-Modus und devTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, Devtools, ie11, Internet Explorer 11, ie-Modus
ms.openlocfilehash: 070bf970c784b4f2173ebc52e4494fc6807b4a8e
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643235"
---
# <a name="internet-explorer-mode-and-the-devtools"></a><span data-ttu-id="adc4e-104">Internet Explorer-Modus und devTools</span><span class="sxs-lookup"><span data-stu-id="adc4e-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="adc4e-105">In diesem Artikel wird beschrieben, wie der Internet Explorer-Modus \(IE-Modus\) in die Microsoft Edge \(Chromium\) DevTools integriert wird.</span><span class="sxs-lookup"><span data-stu-id="adc4e-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <a name="understanding-ie-mode"></a><span data-ttu-id="adc4e-106">Grundlegendes zum IE-Modus</span><span class="sxs-lookup"><span data-stu-id="adc4e-106">Understanding IE mode</span></span>  

<span data-ttu-id="adc4e-107">Im IE-Modus können Unternehmen eine Liste von Websites angeben, die nur in Internet Explorer 11 funktionieren.</span><span class="sxs-lookup"><span data-stu-id="adc4e-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="adc4e-108">Wenn Sie in Microsoft Edge \(Chromium\) zu diesen Websites navigieren, wird eine Instanz von Internet Explorer 11 ausgeführt und die Website auf einer Registerkarte gerendert.  Die Funktionalität ermöglicht Es Unternehmen, die Kompatibilität mit Technologien zu verwalten, die derzeit nicht mit modernen Webbrowsern kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="adc4e-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="adc4e-109">Unterstützung für die folgenden Technologien ist im IE-Modus enthalten.</span><span class="sxs-lookup"><span data-stu-id="adc4e-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="adc4e-110">IE-Dokumentmodi</span><span class="sxs-lookup"><span data-stu-id="adc4e-110">IE document modes</span></span>  
*   <span data-ttu-id="adc4e-111">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="adc4e-111">ActiveX controls</span></span>  
*   <span data-ttu-id="adc4e-112">Andere Legacykomponenten</span><span class="sxs-lookup"><span data-stu-id="adc4e-112">other legacy components</span></span>  

<span data-ttu-id="adc4e-113">Im IE-Modus basiert der Renderingprozess auf Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="adc4e-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="adc4e-114">Der Microsoft Edge \(Chromium\)-Prozess-Manager übernimmt die Lebensdauer des Renderingprozesses.</span><span class="sxs-lookup"><span data-stu-id="adc4e-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="adc4e-115">Sie ist auf die Lebensdauer der Registerkarte für eine bestimmte Website \(oder App\) beschränkt.</span><span class="sxs-lookup"><span data-stu-id="adc4e-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="adc4e-116">Wenn eine Registerkarte im IE-Modus gerendert wird, wird in der Adressleiste für die jeweilige Registerkarte ein Signal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="adc4e-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="IE-Modus-Signal in der Adressleiste" lightbox="../media/ie-mode-badge.msft.png":::
   <span data-ttu-id="adc4e-118">IE-Modus-Signal in der Adressleiste</span><span class="sxs-lookup"><span data-stu-id="adc4e-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="adc4e-119">Der IE-Modus ist derzeit auf Windows 10 Version 1903 \(Update vom Mai 2019\) verfügbar, wird aber in Kürze für alle unterstützten Windows-Plattformen verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="adc4e-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a><span data-ttu-id="adc4e-120">Starten der DevTools auf einer Registerkarte im IE-Modus</span><span class="sxs-lookup"><span data-stu-id="adc4e-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="adc4e-121">Wenn Sie versuchen, den Dokumentmodus einer Website im IE-Modus anzuzeigen, wählen Sie das Signal in der Adressleiste aus.</span><span class="sxs-lookup"><span data-stu-id="adc4e-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Anzeigen des Dokumentmodus mithilfe des IE-Modus-Badge" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="adc4e-123">Anzeigen des Dokumentmodus mithilfe des IE-Modus-Badge</span><span class="sxs-lookup"><span data-stu-id="adc4e-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="adc4e-124">Wenn eine Registerkarte den IE-Modus verwendet, funktionieren die DevTools nicht, und die folgenden Bedingungen treten auf.</span><span class="sxs-lookup"><span data-stu-id="adc4e-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="adc4e-125">Wenn Sie `F12` `Ctrl` + `Shift` + `I` DevTools auswählen oder auswählen, wird in einer leeren Instanz des Microsoft Edge \(Chromium\) die folgende Meldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="adc4e-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="adc4e-126">Wenn Sie ein Kontextmenü \(rechtsklick\) öffnen und **"Quelle anzeigen"** auswählen, wird Editor gestartet.</span><span class="sxs-lookup"><span data-stu-id="adc4e-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="adc4e-127">Wenn Sie ein Kontextmenü \(rechtsklick\) öffnen, ist das **Inspect-Element** nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="adc4e-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="adc4e-128">Der Grund dafür, dass eine Reihe von Tools innerhalb der DevTools \(wie die **Netzwerk-** und **Leistungstools\)** nicht funktionieren, ist das Renderingmodul wechselt von Chromium zu Internet Explorer 11 im IE-Modus.</span><span class="sxs-lookup"><span data-stu-id="adc4e-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="adc4e-129">Um Feedback zu geben, navigieren Sie zu ["Erste Schritte mit dem Microsoft Edge DevTools-Team".](#getting-in-touch-with-the-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="adc4e-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools im IE-Modus gestartet" lightbox="../media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="adc4e-131">DevTools im IE-Modus gestartet</span><span class="sxs-lookup"><span data-stu-id="adc4e-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="adc4e-132">Führen Sie die folgenden Schritte aus, um Ihre Internet Explorer 11-basierte Website \(oder App\) im Internet Explorer 11- und IE-Modus zu testen.</span><span class="sxs-lookup"><span data-stu-id="adc4e-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="adc4e-133">Öffnen Sie Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="adc4e-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="adc4e-134">Suchen Sie auf Windows 10 die Verknüpfung für Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="adc4e-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="adc4e-135">**Startmenü**  >  **Windows Zubehör**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="adc4e-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="adc4e-136">Suchen Sie Windows 7 nach Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="adc4e-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="adc4e-137">**Startmenü**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="adc4e-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="adc4e-138">Öffnen Sie in Internet Explorer 11 dieselbe Webseite.</span><span class="sxs-lookup"><span data-stu-id="adc4e-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="adc4e-139">Starten Sie die Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="adc4e-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="adc4e-140">Wählen Sie `F12` .</span><span class="sxs-lookup"><span data-stu-id="adc4e-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="adc4e-141">Zeigen Sie auf eine beliebige Stelle, öffnen Sie ein Kontextmenü \(rechtsklick\), und wählen Sie **"Inspect"-Element**aus.</span><span class="sxs-lookup"><span data-stu-id="adc4e-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="adc4e-142">Weitere Informationen zur Verwendung dieser Tools finden Sie unter [Verwendung der F12-Entwicklertools.][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]</span><span class="sxs-lookup"><span data-stu-id="adc4e-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

<span data-ttu-id="adc4e-143">Wenn Internet Explorer 11 nicht verfügbar ist, z. B. auf Windows 11, können Sie IEChooser verwenden, um die DevTools von Internet Explorer zu starten, um den Inhalt Ihrer IE-Modus-Registerkarten zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="adc4e-143">If Internet Explorer 11 is not available, such as on Windows 11, you can use IEChooser to launch the Internet Explorer DevTools to debug the content of your IE mode tabs.</span></span> <span data-ttu-id="adc4e-144">Führen Sie die folgenden Schritte aus, um IEChooser zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="adc4e-144">To use IEChooser, perform the following steps.</span></span>

1.  <span data-ttu-id="adc4e-145">Öffnen Sie IEChooser.</span><span class="sxs-lookup"><span data-stu-id="adc4e-145">Open IEChooser.</span></span>
    1. <span data-ttu-id="adc4e-146">Öffnen des Dialogfelds Ausführen</span><span class="sxs-lookup"><span data-stu-id="adc4e-146">Open the Run dialog box.</span></span> <span data-ttu-id="adc4e-147">Drücken Sie z. B. die `Windows logo key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="adc4e-147">For example, press the `Windows logo key` + `R`.</span></span>
    2. <span data-ttu-id="adc4e-148">Geben Sie `%systemroot%\system32\f12\IEChooser.exe` ein, und wählen Sie dann **OK**aus.</span><span class="sxs-lookup"><span data-stu-id="adc4e-148">Enter `%systemroot%\system32\f12\IEChooser.exe`, and then select **Ok**.</span></span>
2.  <span data-ttu-id="adc4e-149">Wählen Sie in IEChooser den Eintrag für die Registerkarte "IE-Modus" aus.</span><span class="sxs-lookup"><span data-stu-id="adc4e-149">In IEChooser, select the entry for the IE mode tab.</span></span>


## <a name="remote-debugging-and-ie-mode"></a><span data-ttu-id="adc4e-150">Remotedebugging und IE-Modus</span><span class="sxs-lookup"><span data-stu-id="adc4e-150">Remote debugging and IE mode</span></span>  

<span data-ttu-id="adc4e-151">Starten Sie Microsoft Edge \(Chromium\) mit aktivierten Remotedebugging über die Befehlszeilenschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="adc4e-151">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="adc4e-152">Microsoft Visual Studio, Microsoft Visual Studio Code und andere Entwicklungstools führen in der Regel einen Befehl aus, um Microsoft Edge zu starten.</span><span class="sxs-lookup"><span data-stu-id="adc4e-152">Microsoft Visual Studio, Microsoft Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="adc4e-153">Der folgende Befehl startet Microsoft Edge, wobei der Remotedebuggingport `9222` auf .</span><span class="sxs-lookup"><span data-stu-id="adc4e-153">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="adc4e-154">Nachdem Sie Microsoft Edge \(Chromium\) mit einem Befehlszeilenargument gestartet haben, ist der IE-Modus nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="adc4e-154">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="adc4e-155">Sie können weiterhin zu Websites \(oder Apps\) navigieren, die andernfalls im IE-Modus angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="adc4e-155">You may still navigate to websites \(or apps\) that are otherwise displayed in IE mode.</span></span>  <span data-ttu-id="adc4e-156">Der Websiteinhalt \(oder App\) wird mit Chromium gerendert, nicht mit Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="adc4e-156">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="adc4e-157">Erwarten Sie, dass die Teile der Webseiten, die IE11 verwenden, z. B. ActiveX Steuerelemente, nicht ordnungsgemäß gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="adc4e-157">Expect the parts of the webpages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="adc4e-158">Der IE-Modus-Badge wird nicht in der Adressleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="adc4e-158">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="adc4e-159">Der IE-Modus bleibt nicht verfügbar, bis Sie Microsoft Edge \(Chromium\) vollständig schließen und neu starten.</span><span class="sxs-lookup"><span data-stu-id="adc4e-159">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="adc4e-160">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="adc4e-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Verwenden der F12-Entwicklertools | Microsoft-Dokumente"  
