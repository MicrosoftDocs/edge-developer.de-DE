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
# <a name="progressive-web-apps-on-windows-overview"></a>Übersicht über progressive Web Apps auf Windows  

[Progressive Web Apps][MDNApps] \(PWAs\) bieten Zugriff auf offene Webtechnologien für plattformübergreifende Interoperabilität und bieten Ihren Benutzern eine systemeigene, appähnliche Oberfläche, die für ihre Geräte angepasst wurde. PWAs sind Websites, die [schrittweise erweitert][AListApartUnderstandingProgressiveEnhancement] werden, um wie systemeigene Apps auf unterstützenden Plattformen zu funktionieren. Die Eigenschaften einer PWA vereinen das Beste aus Web- und nativen Apps.  

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
        ### <a name="discoverablemdnpwaadvantagesdiscoverable"></a>[Erkennbar][MDNPwaAdvantagesDiscoverable]  
    :::column-end:::
    :::column:::
        ### <a name="installablemdnpwaadvantagesinstallable"></a>[Installierbare][MDNPwaAdvantagesInstallable]  
    :::column-end:::
    :::column:::
        ### <a name="re-engageablemdnpwaadvantagesreengageable"></a>[Reaktivierbar][MDNPwaAdvantagesReEngageable]  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        Aus Websuchergebnissen und unterstützenden App-Stores  
    :::column-end:::
    :::column:::
        Anheften und Starten über den Startbildschirm, das Startmenü, die Taskleiste usw.  
    :::column-end:::
    :::column:::
        Senden von Pushbenachrichtigungen, auch wenn die App nicht aktiv ist  
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
        ### <a name="network-independentmdnpwaadvantagesnetworkindependent"></a>[Netzwerkunabhängig][MDNPwaAdvantagesNetworkIndependent]  
    :::column-end:::
    :::column:::
        ### <a name="progressivemdnpwaadvantagesprogressive"></a>[Progressive][MDNPwaAdvantagesProgressive]  
    :::column-end:::
    :::column:::
        ### <a name="safemdnpwaadvantagessafe"></a>[Safe][MDNPwaAdvantagesSafe]  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        Funktioniert offline und unter Bedingungen mit geringem Netzwerk  
    :::column-end:::
    :::column:::
        Erfahrungsskala mit Gerätefunktionen nach oben (oder unten)  
    :::column-end:::
    :::column:::
        Bietet einen sicheren HTTPS-Endpunkt und andere Benutzervorkehrungen  
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
        ### <a name="responsivemdnpwaadvantagesresponsive"></a>[Dynamisch][MDNPwaAdvantagesResponsive]  
    :::column-end:::
    :::column:::
        ### <a name="linkablemdnpwaadvantageslinkable"></a>[Verknüpfbar][MDNPwaAdvantagesLinkable]  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        Passt sich an die Bildschirmgröße oder Ausrichtungs- und Eingabemethode des Benutzers an.  
    :::column-end:::
    :::column:::
        Freigeben und Starten über einen Standardhyperlink  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  

Erstellen Sie \(oder konvertieren Sie\) Ihre vorhandene Website in eine PWA, um das Engagement für Ihre Benutzer zu verbessern. Zu den Verbesserungen gehören Pushbenachrichtigungen, app-ähnliche Integration und Offlineunterstützung. Setzen Sie fort, Ihre Zielgruppe im offenen Web zu erstellen, damit Benutzer Ihre PWA durch Suche und Linkfreigabe entdecken können. Das Beste ist, dass Ihre App mit ihrem Webservercode aktualisiert wird.  

## <a name="pwas-on-microsoft-edge-chromium"></a>PWAs auf Microsoft Edge (Chromium)  

Wenn Sie eine Progressive Web App für Webstandard-APIs erstellen, kann Ihre App plattform- und geräteübergreifend bereitgestellt werden und die verfügbaren gerätespezifischen Funktionen nutzen. PWAs in Microsoft Edge \(Chromium\) bieten Ihrer Website die folgenden Vorteile.  

*   Ihre App basiert auf einer standardsbasierten Webplattform.  
*   Ermöglicht Ihren Benutzern, Ihre App direkt über den Browser zu installieren.  
*   Ermöglicht Es Ihren Benutzern, Ihre App ohne Store-basierte Bereitstellung oder Registrierung zu installieren.  
    
Desktop-PWAs werden auf allen Plattformen unterstützt, Microsoft Edge \(Chromium\) [verfügbar](https://www.microsoft.com/edge)ist. Die folgenden Vorteile sind enthalten.

*   Apps können über das Symbol **"Installieren"** in der Navigationsleiste direkt im Browser installiert werden.  
    
    :::image type="complex" source="./media/install-progressive-web-app-icon.png" alt-text="Installieren von App-Flyout und Symbol" lightbox="./media/install-progressive-web-app-icon.png":::
       Installieren von App-Flyout und Symbol  
    :::image-end:::  
    
*   Apps können auch über das Menü **Einstellungen**  >  **Apps** installiert, ausgeführt und verwaltet werden.  
    
    :::image type="complex" source="./media/app-menus.png" alt-text="App-Menüelemente unter "Einstellungen"" lightbox="./media/app-menus.png":::
       App-Menüelemente unter "Einstellungen"  
    :::image-end:::  
    
*   Webbenachrichtigungen sind in das Windows Benachrichtigungssystem integriert.  
*   Freigegebener Cookiespeicher mit dem Browserprofil, das die App installiert hat  
*   Zugriff auf andere Browserfeatures mithilfe des **Menüs "Einstellung" und mehr** \( `...` \) einschließlich Zertifikatüberprüfung, Websiteberechtigungen, Tracking-Schutz und Browsererweiterungen  
*   Vollzugriff auf [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] zum Debuggen Ihrer App  
    
> [!NOTE]
> For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session.][BuildVideo] 

## <a name="requirements"></a>Anforderungen  

Um als PWA ausgeführt zu werden, sollte Ihre servergehostete Web-App die folgenden Mindestanforderungen enthalten.  

:::row:::
   :::column span="1":::
      [HTTPS][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      Schützt Ihre Benutzer, indem eine sichere Verbindung für die Server- oder App-Kommunikation bereitgestellt wird.  Service Worker und andere PWA Technologien funktionieren nur mit Webressourcen, die über eine sichere Verbindung \(oder aus `localhost` dem zu Debugzwecken\) bereitgestellt werden.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Service Workers][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      Verwendet Service Worker-Threads, um als Netzwerkproxys zwischen Ihrem Server und Ihrer Client-App zu fungieren.  Service Worker-Threads bieten Offlineunterstützung, Zwischenspeicherung von Ressourcen, Pushbenachrichtigungen, Synchronisierung von Hintergrunddaten und Leistungsoptimierungen beim Laden von Seiten.    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Web App-Manifest][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      Stellt eine JSON-basierte Metadatendatei bereit, die wichtige Informationen zu Ihrer Web-App beschreibt, sodass Windows 10 und andere Hostplattformen Ihren PWA Benutzern eine installierbare, systemeigene App-ähnliche Oberfläche bieten.  Wichtige Informationen umfassen Symbole, Sprache und URL-Einstiegspunkt. 
   :::column-end:::
:::row-end:::  

Um eine hervorragende PWA zu sein, muss Ihre App auch die folgenden Anforderungen erfüllen.  

:::row:::
   :::column span="1":::
      [Browserübergreifende Kompatibilität][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      Stellen Sie sicher, dass Ihre PWA funktioniert, indem Sie sie in verschiedenen Browsern und Umgebungen [testen.][MicrosoftDeveloperEdgeToolsRemote]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Dynamisches Design][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      Verwendet dynamische Layouts und flexible Bilder.  Reaktionsfähiges Design umfasst die folgenden Elemente, die Ihre Benutzeroberfläche an das Gerät Des Benutzers anpassen.  
      
      *   [CSS-Raster][MDNCssGridLayout]  
      *   [Flexbox][MDNCssFlexibleBoxLayout]  
      *   [CSS-Raster][MDNCssGridLayout] und [Flexbox][MDNCssFlexibleBoxLayout]  
      *   [Medienabfragen][MDNMediaQueries]  
      *   [Reaktionsfähige Bilder][MDNResponsiveImages]  
          
      Verwendet [Geräteemulationstools][DevToolsGuideDeviceModeTestingOtherBrowsers] aus Ihrem Browser, um lokal zu testen oder eine Remotedebuggingsitzung auf [Windows][DevtoolsRemoteDebuggingWindows] oder [Android][DevtoolsRemoteDebuggingIndex] zu erstellen, um direkt auf einem Zielgerät zu testen.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Deep-Verknüpfung][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      Leitet jede Seite Ihrer Website an eine eindeutige URL weiter, damit vorhandene Benutzer ihnen helfen können, eine noch größere Zielgruppe durch die Freigabe von sozialen Medien zu erreichen.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Validierungs- und Testmethoden][Webhint]  
   :::column-end:::
   :::column span="2":::
      Verwendet Codequalitätstools wie [webhint][Webhint] linter, um die Effizienz, Robustheit, Sicherheit und Barrierefreiheit Ihrer App zu optimieren.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Prüfliste für Chromium PWA][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      Überprüft Ihre PWA anhand der Checkliste für die Google-Baseline PWA.  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> Um Ihre PWA in eine [Microsoft Store][MicrosoftDeveloperStore] App zu verwandeln, navigieren Sie im Microsoft Store zu [Progressive Web Apps.][PwaChromiumMicrosoftStore]  
  
## <a name="see-also"></a>Weitere Informationen  

*   [Myth Busting PWAs][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Eine progressive Roadmap für Ihre progressive Web-App][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Offline-POSTs mit progressiven Web-Apps][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA F&A][AaronGustafsonNotebookPwaQa]  
*   [Im Web][JoretegBlogBettingWeb]  
*   [Benennen progressiver Web-Apps][Fberriman20170626NamingProgressiveWebApps]  
*   [Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 1)][Smashingmagazine201907ProgressiveWebAppFrameworkPart1]  
*   [Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 2)][Smashingmagazine201907ProgressiveWebAppFrameworkPart2]  
*   [Entwerfen und Erstellen einer progressiven Web-App ohne Framework (Teil 3)][Smashingmagazine201907ProgressiveWebAppFrameworkPart3]  
    
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
