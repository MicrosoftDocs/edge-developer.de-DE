---
description: Progressive Web Apps (Chromium) werden nativ auf Windows 10 ausgeführt.  Hier ist alles, was Sie als Webentwickler wissen müssen.
title: Progressive Web Apps auf Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: Progressive Web Apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 47c6f98329a1da67e0f2c1a8e6243250992fb599
ms.sourcegitcommit: f4488cf2dfef0aeec04712b2ed933d68b8e93a94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "11608836"
---
# <a name="progressive-web-apps-on-windows-overview"></a><span data-ttu-id="b1281-105">Übersicht über progressive Web Apps auf Windows</span><span class="sxs-lookup"><span data-stu-id="b1281-105">Progressive Web Apps on Windows overview</span></span>  

<span data-ttu-id="b1281-106">[Progressive Web Apps][MDNApps] \(PWAs\) bieten Zugriff auf offene Webtechnologien für plattformübergreifende Interoperabilität und bieten Ihren Benutzern eine systemeigene, appähnliche Oberfläche, die für ihre Geräte angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="b1281-106">[Progressive Web Apps][MDNApps] \(PWAs\) provide access to open web technologies for cross-platform interoperability and provide your users with a native, app-like experience customized for their devices.</span></span> <span data-ttu-id="b1281-107">PWAs sind Websites, die [schrittweise erweitert][AListApartUnderstandingProgressiveEnhancement] werden, um wie systemeigene Apps auf unterstützenden Plattformen zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="b1281-107">PWAs are websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span> <span data-ttu-id="b1281-108">Die Eigenschaften einer PWA vereinen das Beste aus Web- und nativen Apps.</span><span class="sxs-lookup"><span data-stu-id="b1281-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification-small.png":::  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="discoverablemdnpwaadvantagesdiscoverable"></a><span data-ttu-id="b1281-109">[Erkennbar][MDNPwaAdvantagesDiscoverable]</span><span class="sxs-lookup"><span data-stu-id="b1281-109">[Discoverable][MDNPwaAdvantagesDiscoverable]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="installablemdnpwaadvantagesinstallable"></a><span data-ttu-id="b1281-110">[Installierbare][MDNPwaAdvantagesInstallable]</span><span class="sxs-lookup"><span data-stu-id="b1281-110">[Installable][MDNPwaAdvantagesInstallable]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="re-engageablemdnpwaadvantagesreengageable"></a><span data-ttu-id="b1281-111">[Reaktivierbar][MDNPwaAdvantagesReEngageable]</span><span class="sxs-lookup"><span data-stu-id="b1281-111">[Re-engageable][MDNPwaAdvantagesReEngageable]</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="b1281-112">Aus Websuchergebnissen und unterstützenden App-Stores</span><span class="sxs-lookup"><span data-stu-id="b1281-112">From web search results and supporting app stores</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="b1281-113">Anheften und Starten über den Startbildschirm, das Startmenü, die Taskleiste usw.</span><span class="sxs-lookup"><span data-stu-id="b1281-113">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="b1281-114">Senden von Pushbenachrichtigungen, auch wenn die App nicht aktiv ist</span><span class="sxs-lookup"><span data-stu-id="b1281-114">Send push notifications, even when the app is not active</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security-small.png":::  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="network-independentmdnpwaadvantagesnetworkindependent"></a><span data-ttu-id="b1281-115">[Netzwerkunabhängig][MDNPwaAdvantagesNetworkIndependent]</span><span class="sxs-lookup"><span data-stu-id="b1281-115">[Network Independent][MDNPwaAdvantagesNetworkIndependent]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="progressivemdnpwaadvantagesprogressive"></a><span data-ttu-id="b1281-116">[Progressive][MDNPwaAdvantagesProgressive]</span><span class="sxs-lookup"><span data-stu-id="b1281-116">[Progressive][MDNPwaAdvantagesProgressive]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="safemdnpwaadvantagessafe"></a><span data-ttu-id="b1281-117">[Safe][MDNPwaAdvantagesSafe]</span><span class="sxs-lookup"><span data-stu-id="b1281-117">[Safe][MDNPwaAdvantagesSafe]</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="b1281-118">Funktioniert offline und unter Bedingungen mit geringem Netzwerk</span><span class="sxs-lookup"><span data-stu-id="b1281-118">Works offline and in low-network conditions</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="b1281-119">Erfahrungsskala mit Gerätefunktionen nach oben (oder unten)</span><span class="sxs-lookup"><span data-stu-id="b1281-119">Experience scales up (or down) with device capabilities</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="b1281-120">Bietet einen sicheren HTTPS-Endpunkt und andere Benutzervorkehrungen</span><span class="sxs-lookup"><span data-stu-id="b1281-120">Provides a secure HTTPS endpoint and other user safeguards</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link-small.png":::  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="responsivemdnpwaadvantagesresponsive"></a><span data-ttu-id="b1281-121">[Dynamisch][MDNPwaAdvantagesResponsive]</span><span class="sxs-lookup"><span data-stu-id="b1281-121">[Responsive][MDNPwaAdvantagesResponsive]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="linkablemdnpwaadvantageslinkable"></a><span data-ttu-id="b1281-122">[Verknüpfbar][MDNPwaAdvantagesLinkable]</span><span class="sxs-lookup"><span data-stu-id="b1281-122">[Linkable][MDNPwaAdvantagesLinkable]</span></span>  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="b1281-123">Passt sich an die Bildschirmgröße oder Ausrichtungs- und Eingabemethode des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="b1281-123">Adapts to the user's screen size or orientation and input method</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="b1281-124">Freigeben und Starten über einen Standardhyperlink</span><span class="sxs-lookup"><span data-stu-id="b1281-124">Share and launch from a standard hyperlink</span></span>  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  

<span data-ttu-id="b1281-125">Erstellen Sie \(oder konvertieren Sie\) Ihre vorhandene Website in eine PWA, um das Engagement für Ihre Benutzer zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="b1281-125">Build \(or convert\) your existing website to a PWA to enhance engagement with your users.</span></span> <span data-ttu-id="b1281-126">Zu den Verbesserungen gehören Pushbenachrichtigungen, app-ähnliche Integration und Offlineunterstützung.</span><span class="sxs-lookup"><span data-stu-id="b1281-126">Enhancements include push notifications, app-like integration, and offline support.</span></span> <span data-ttu-id="b1281-127">Setzen Sie fort, Ihre Zielgruppe im offenen Web zu erstellen, damit Benutzer Ihre PWA durch Suche und Linkfreigabe entdecken können.</span><span class="sxs-lookup"><span data-stu-id="b1281-127">Continue to build your audience on the open web for users to discover your PWA through search and link-sharing.</span></span> <span data-ttu-id="b1281-128">Das Beste ist, dass Ihre App mit ihrem Webservercode aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b1281-128">Best of all, your app is updated using your web server code.</span></span>  

## <a name="pwas-on-microsoft-edge-chromium"></a><span data-ttu-id="b1281-129">PWAs auf Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="b1281-129">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="b1281-130">Wenn Sie eine Progressive Web App für Webstandard-APIs erstellen, kann Ihre App plattform- und geräteübergreifend bereitgestellt werden und die verfügbaren gerätespezifischen Funktionen nutzen.</span><span class="sxs-lookup"><span data-stu-id="b1281-130">When you build a Progressive Web App targeting web standard APIs, your app may be deployed across platforms and devices and take advantage of the device-specific capabilities as available.</span></span> <span data-ttu-id="b1281-131">PWAs in Microsoft Edge \(Chromium\) bieten Ihrer Website die folgenden Vorteile.</span><span class="sxs-lookup"><span data-stu-id="b1281-131">PWAs in Microsoft Edge \(Chromium\) add the following advantages to your website.</span></span>  

*   <span data-ttu-id="b1281-132">Ihre App basiert auf einer standardsbasierten Webplattform.</span><span class="sxs-lookup"><span data-stu-id="b1281-132">Your app is built on a standards-based web platform.</span></span>  
*   <span data-ttu-id="b1281-133">Ermöglicht Ihren Benutzern, Ihre App direkt über den Browser zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b1281-133">Allows your users to install your app directly from the browser.</span></span>  
*   <span data-ttu-id="b1281-134">Ermöglicht Es Ihren Benutzern, Ihre App ohne Store-basierte Bereitstellung oder Registrierung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b1281-134">Allows your users to install your app without a Store-based deployment or registration.</span></span>  
    
<span data-ttu-id="b1281-135">Desktop-PWAs werden auf allen Plattformen unterstützt, Microsoft Edge \(Chromium\) [verfügbar](https://www.microsoft.com/edge)ist.</span><span class="sxs-lookup"><span data-stu-id="b1281-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is [available](https://www.microsoft.com/edge).</span></span> <span data-ttu-id="b1281-136">Die folgenden Vorteile sind enthalten.</span><span class="sxs-lookup"><span data-stu-id="b1281-136">The following benefits are included.</span></span>

*   <span data-ttu-id="b1281-137">Apps können über das Symbol **"Installieren"** in der Navigationsleiste direkt im Browser installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b1281-137">Apps may be installed directly from within the browser using the **Install** icon in the navigation bar.</span></span>  
    
    :::image type="complex" source="./media/install-progressive-web-app-icon.png" alt-text="Installieren von App-Flyout und Symbol" lightbox="./media/install-progressive-web-app-icon.png":::
       <span data-ttu-id="b1281-139">Installieren von App-Flyout und Symbol</span><span class="sxs-lookup"><span data-stu-id="b1281-139">Install app flyout and icon</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="b1281-140">Apps können auch über das Menü **Einstellungen**  >  **Apps** installiert, ausgeführt und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="b1281-140">Apps may also be installed, run, and managed from the **Settings** > **Apps** menu</span></span>  
    
    :::image type="complex" source="./media/app-menus.png" alt-text="App-Menüelemente unter "Einstellungen"" lightbox="./media/app-menus.png":::
       <span data-ttu-id="b1281-142">App-Menüelemente unter "Einstellungen"</span><span class="sxs-lookup"><span data-stu-id="b1281-142">App menu items under settings</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="b1281-143">Webbenachrichtigungen sind in das Windows Benachrichtigungssystem integriert.</span><span class="sxs-lookup"><span data-stu-id="b1281-143">Web Notifications are integrated into the Windows notification system</span></span>  
*   <span data-ttu-id="b1281-144">Freigegebener Cookiespeicher mit dem Browserprofil, das die App installiert hat</span><span class="sxs-lookup"><span data-stu-id="b1281-144">Shared cookie store with the browser profile that installed the app</span></span>  
*   <span data-ttu-id="b1281-145">Zugriff auf andere Browserfeatures mithilfe des **Menüs "Einstellung" und mehr** \( `...` \) einschließlich Zertifikatüberprüfung, Websiteberechtigungen, Tracking-Schutz und Browsererweiterungen</span><span class="sxs-lookup"><span data-stu-id="b1281-145">Access to other browser features using the **Setting and more** \(`...`\) menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>  
*   <span data-ttu-id="b1281-146">Vollzugriff auf [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] zum Debuggen Ihrer App</span><span class="sxs-lookup"><span data-stu-id="b1281-146">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  
    
> [!NOTE]
> <span data-ttu-id="b1281-147">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session.][BuildVideo]</span><span class="sxs-lookup"><span data-stu-id="b1281-147">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session][BuildVideo].</span></span> 

## <a name="requirements"></a><span data-ttu-id="b1281-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1281-148">Requirements</span></span>  

<span data-ttu-id="b1281-149">Um als PWA ausgeführt zu werden, sollte Ihre servergehostete Web-App die folgenden Mindestanforderungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b1281-149">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="b1281-150">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b1281-150">HTTPS</span></span>][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b1281-151">Schützt Ihre Benutzer, indem eine sichere Verbindung für die Server- oder App-Kommunikation bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b1281-151">Protects your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="b1281-152">Service Worker und andere PWA Technologien funktionieren nur mit Webressourcen, die über eine sichere Verbindung \(oder aus `localhost` dem zu Debugzwecken\) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b1281-152">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="b1281-153">Service Workers</span><span class="sxs-lookup"><span data-stu-id="b1281-153">Service Workers</span></span>][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b1281-154">Verwendet Service Worker-Threads, um als Netzwerkproxys zwischen Ihrem Server und Ihrer Client-App zu fungieren.</span><span class="sxs-lookup"><span data-stu-id="b1281-154">Uses Service Worker threads to act as network proxies between your server and client app.</span></span>  <span data-ttu-id="b1281-155">Service Worker-Threads bieten Offlineunterstützung, Zwischenspeicherung von Ressourcen, Pushbenachrichtigungen, Synchronisierung von Hintergrunddaten und Leistungsoptimierungen beim Laden von Seiten.</span><span class="sxs-lookup"><span data-stu-id="b1281-155">Service Worker threads provide offline support, resource caching, push notifications, background data sync, and  page-load performance optimizations.</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="b1281-156">Web App-Manifest</span><span class="sxs-lookup"><span data-stu-id="b1281-156">Web App Manifest</span></span>][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b1281-157">Stellt eine JSON-basierte Metadatendatei bereit, die wichtige Informationen zu Ihrer Web-App beschreibt, sodass Windows 10 und andere Hostplattformen Ihren PWA Benutzern eine installierbare, systemeigene App-ähnliche Oberfläche bieten.</span><span class="sxs-lookup"><span data-stu-id="b1281-157">Provides a JSON-based metadata file that describes key information about your web app, so that Windows 10 and other host platforms provide your PWA users with an installable, native app-like experience.</span></span>  <span data-ttu-id="b1281-158">Wichtige Informationen umfassen Symbole, Sprache und URL-Einstiegspunkt.</span><span class="sxs-lookup"><span data-stu-id="b1281-158">Key information includes icons, language, and URL entry point.</span></span> 
   :::column-end:::
:::row-end:::  

<span data-ttu-id="b1281-159">Um eine hervorragende PWA zu sein, muss Ihre App auch die folgenden Anforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="b1281-159">To be a great PWA, your app must also meet the following requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="b1281-160">Browserübergreifende Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="b1281-160">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b1281-161">Stellen Sie sicher, dass Ihre PWA funktioniert, indem Sie sie in verschiedenen Browsern und Umgebungen [testen.][MicrosoftDeveloperEdgeToolsRemote]</span><span class="sxs-lookup"><span data-stu-id="b1281-161">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="b1281-162">Dynamisches Design</span><span class="sxs-lookup"><span data-stu-id="b1281-162">Responsive design</span></span>][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b1281-163">Verwendet dynamische Layouts und flexible Bilder.</span><span class="sxs-lookup"><span data-stu-id="b1281-163">Employs fluid layouts and flexible images.</span></span>  <span data-ttu-id="b1281-164">Reaktionsfähiges Design umfasst die folgenden Elemente, die Ihre Benutzeroberfläche an das Gerät Des Benutzers anpassen.</span><span class="sxs-lookup"><span data-stu-id="b1281-164">Responsive design includes the following elements that adapt your UX to your user's device.</span></span>  
      
      *   <span data-ttu-id="b1281-165">[CSS-Raster][MDNCssGridLayout]</span><span class="sxs-lookup"><span data-stu-id="b1281-165">CSS [grid][MDNCssGridLayout]</span></span>  
      *   [<span data-ttu-id="b1281-166">Flexbox</span><span class="sxs-lookup"><span data-stu-id="b1281-166">flexbox</span></span>][MDNCssFlexibleBoxLayout]  
      *   <span data-ttu-id="b1281-167">[CSS-Raster][MDNCssGridLayout] und [Flexbox][MDNCssFlexibleBoxLayout]</span><span class="sxs-lookup"><span data-stu-id="b1281-167">CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout]</span></span>  
      *   [<span data-ttu-id="b1281-168">Medienabfragen</span><span class="sxs-lookup"><span data-stu-id="b1281-168">media queries</span></span>][MDNMediaQueries]  
      *   [<span data-ttu-id="b1281-169">Reaktionsfähige Bilder</span><span class="sxs-lookup"><span data-stu-id="b1281-169">responsive images</span></span>][MDNResponsiveImages]  
          
      <span data-ttu-id="b1281-170">Verwendet [Geräteemulationstools][DevToolsGuideDeviceModeTestingOtherBrowsers] aus Ihrem Browser, um lokal zu testen oder eine Remotedebuggingsitzung auf [Windows][DevtoolsRemoteDebuggingWindows] oder [Android][DevtoolsRemoteDebuggingIndex] zu erstellen, um direkt auf einem Zielgerät zu testen.</span><span class="sxs-lookup"><span data-stu-id="b1281-170">Uses [device emulation tools][DevToolsGuideDeviceModeTestingOtherBrowsers] from your browser to locally test, or create a remote debugging session on [Windows][DevtoolsRemoteDebuggingWindows] or [Android][DevtoolsRemoteDebuggingIndex] to test directly on a target device.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="b1281-171">Deep-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="b1281-171">Deep linking</span></span>][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b1281-172">Leitet jede Seite Ihrer Website an eine eindeutige URL weiter, damit vorhandene Benutzer ihnen helfen können, eine noch größere Zielgruppe durch die Freigabe von sozialen Medien zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="b1281-172">Routes each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="b1281-173">Validierungs- und Testmethoden</span><span class="sxs-lookup"><span data-stu-id="b1281-173">Validation and testing practices</span></span>][Webhint]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b1281-174">Verwendet Codequalitätstools wie [webhint][Webhint] linter, um die Effizienz, Robustheit, Sicherheit und Barrierefreiheit Ihrer App zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="b1281-174">Uses code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="b1281-175">Prüfliste für Chromium PWA</span><span class="sxs-lookup"><span data-stu-id="b1281-175">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b1281-176">Überprüft Ihre PWA anhand der Checkliste für die Google-Baseline PWA.</span><span class="sxs-lookup"><span data-stu-id="b1281-176">Verifies your PWA against the Google baseline PWA checklist.</span></span>  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> <span data-ttu-id="b1281-177">Um Ihre PWA in eine [Microsoft Store][MicrosoftDeveloperStore] App zu verwandeln, navigieren Sie im Microsoft Store zu [Progressive Web Apps.][PwaChromiumMicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="b1281-177">To turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] app, navigate to [Progressive Web Apps in the Microsoft Store][PwaChromiumMicrosoftStore].</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1281-178">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b1281-178">See also</span></span>  

*   [<span data-ttu-id="b1281-179">Myth Busting PWAs</span><span class="sxs-lookup"><span data-stu-id="b1281-179">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="b1281-180">Eine progressive Roadmap für Ihre progressive Web-App</span><span class="sxs-lookup"><span data-stu-id="b1281-180">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="b1281-181">Offline-POSTs mit progressiven Web-Apps</span><span class="sxs-lookup"><span data-stu-id="b1281-181">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="b1281-182">PWA F&A</span><span class="sxs-lookup"><span data-stu-id="b1281-182">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="b1281-183">Im Web</span><span class="sxs-lookup"><span data-stu-id="b1281-183">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="b1281-184">Benennen progressiver Web-Apps</span><span class="sxs-lookup"><span data-stu-id="b1281-184">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="b1281-185">Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 1)</span><span class="sxs-lookup"><span data-stu-id="b1281-185">Designing And Building A Progressive Web App Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart1]  
*   [<span data-ttu-id="b1281-186">Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 2)</span><span class="sxs-lookup"><span data-stu-id="b1281-186">Designing And Building A Progressive Web App Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart2]  
*   [<span data-ttu-id="b1281-187">Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 3)</span><span class="sxs-lookup"><span data-stu-id="b1281-187">Designing And Building A Progressive Web App Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Erste Schritte mit dem Remotedebuggen von Android-Geräten | Microsoft-Dokumente"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Erste Schritte mit Remotedebugging Windows 10 Geräte | Microsoft-Dokumente"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Emulieren und Testen anderer Browser | Microsoft-Dokumente"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Debuggen von progressiven Web Apps-| Microsoft-Dokumente"  
[PwaChromiumMicrosoftStore]: ./microsoft-store.md "Veröffentlichen Ihrer Progressive Web App im Microsoft Store | Microsoft-Dokumente"

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Windows Übersicht über Pushbenachrichtigungsdienste (Push Notification Services, WNS) | Microsoft-Dokumente"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Entwerfen für Xbox- und TV-| Microsoft-Dokumente"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Überlegungen zur Benutzeroberfläche für UWP-Geräte | Microsoft-Dokumente"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Was ist eine UWP-App (Universelle Windows-Plattform)? | Microsoft-Dokumente"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Unterstützen Ihrer App mit Hintergrundaufgaben | Microsoft-Dokumente"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Veröffentlichen Windows Apps und Spiele | Microsoft-Dokumente"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Öffnen eines Entwicklerkontos | Microsoft-Dokumente"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Willkommensgrierung progressiver Web-Apps für Microsoft Edge und Windows 10 – Windows Blogs"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "Hintergrundsynchronisierungs-API – Microsoft Edge Plattformstatus"  
[MicrosoftDeveloperEdgePlatformStatusWebAppManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Web App-Manifest – Microsoft Edge Plattformstatus"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Soforttests"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Mixed Reality für Entwickler"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Neuen Microsoft Edge Browser herunterladen"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Aktivieren oder Deaktivieren des Fokusassistenten in Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Ändern von Benachrichtigungseinstellungen in Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA F&A"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Grundlegendes zur progressiven Verbesserung – eine Liste getrennt"  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "Apps | Mdn"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | Mdn"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Browserübergreifende Tests | Mdn"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "CSS Flexible Box Layout | Mdn"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "CSS-Rasterlayout | Mdn"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "API-| abrufen Mdn"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Medienabfragen | Mdn"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "| der Benachrichtigungs-API Mdn"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push-API-| Mdn"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Auffindbar – Progressive Web App-Vorteile"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Installierbar – Vorteile progressiver Web-Apps"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Verlinkbar – Vorteile progressiver Web-Apps"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Netzwerkunabhängig – Vorteile progressiver Web-Apps"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Progressiv – Vorteile progressiver Web-Apps"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Wiederverwendebar – Vorteile progressiver Web-Apps"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Reaktionsfähig – Vorteile progressiver Web-Apps"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Safe – Vorteile progressiver Web-Apps"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Reaktionsfähige Bilder | Mdn"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Dienstmitarbeiter-API-| Mdn"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | Mdn"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "| des Web App-Manifests Mdn"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "video PWA"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Eine progressive Roadmap für Ihre progressive Web-App"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Busting PWAs – die neue Edge Edition"  

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Benennen progressiver Web-Apps"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Im Web"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Offline-POSTs mit progressiven Web-Apps"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 1)"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 2)"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Entwerfen und Erstellen einer progressiven Webanwendung ohne Framework (Teil 3)"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Was macht eine gute progressive Web-App aus? | web.dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Deep Linking – Wikipedia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS – Wikipedia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Dynamisches Webdesign – Wikipedia"  
