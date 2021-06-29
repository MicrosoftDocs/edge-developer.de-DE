---
description: Enthält eine Zusammenfassung der Änderungen mit hoher Auswirkung, die sich auf die Websitekompatibilität auswirken können.
title: Websitekompatibilität – Auswirkungen von Änderungen an Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/27/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Kompatibilität, Webplattform
ms.openlocfilehash: 194e612c008016299b234de816114d24e5569aef
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624787"
---
# <a name="site-compatibility-impacting-changes-coming-to-microsoft-edge"></a>Websitekompatibilität – Auswirkungen von Änderungen an Microsoft Edge  

Die Webplattform ist eine Sammlung von Technologien, die zum Erstellen von Webseiten verwendet werden.  Zu den Technologien gehören HTML, CSS, JavaScript und viele andere offene Standards.  Die Webplattform wird ständig weiterentwickelt, um benutzerfreundlichkeit, Sicherheit und Datenschutz zu verbessern.  In einigen Fällen können Sich Änderungen auf die Funktionalität vorhandener Webseiten auswirken.  For more information about upcoming Chromium project web platform changes, navigate to [Chrome Platform Status Release timeline][ChromestatusFeaturesSchedule].  

Microsoft Edge übernimmt fast alle Upstream-Änderungen an der Webplattform aus dem Chromium-Projekt.  Zu den Gründen gehören Funktionalitäts- und Kompatibilitätsgründe.  Microsoft hat die vollständige Kontrolle über den Microsoft Edge Browser und kann Änderungen zurückstellen oder ablehnen.  Das Microsoft Edge-Team entscheidet, ob die Änderung Browserbenutzern vorteile.  Featurebereiche, in denen Microsoft Edge plänen, von Chromium Änderungen an Timing oder Verhalten abzuweichen, sind in der folgenden Tabelle aufgeführt.  In der Tabelle werden auch änderungen mit hoher Auswirkung hervorgehoben, die das Microsoft Edge-Team verfolgt.  

Lesen Sie diesen Artikel häufig.  Das Microsoft Edge Team aktualisiert diesen Artikel, wenn sich das Denken weiterentwickelt, Zeitachsen verfestigen und neue Änderungen angekündigt werden.  

| Änderung | Stable-Kanal | Experimentation | Weitere Informationen |  
|:--- |:--- |:--- |:--- |
| Cookies standardmäßig `SameSite=Lax` und `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | Diese Änderung erfolgt im Chromium Projekt, auf dem Microsoft Edge basiert.  For more information, including the planned timeline by Google for this change, navigate to the [Chrome Platform Status entry][ChromestatusFeature5088147346030592].  |  
| Referrer-Richtlinie: Standardeinstellung: `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | Diese Änderung erfolgt im Chromium Projekt, auf dem Microsoft Edge basiert.  For more information, including the planned timeline by Google for this change, navigate to the [Chrome Platform Status entry][ChromestatusFeature6251880185331712].  |  
| Synchrone `XmlHttpRequest` Seitenentlassung nicht zulassen | [Chrome+1](#release-comments) \(Edge v83\) |  | Diese Änderung erfolgt im Chromium Projekt, auf dem Microsoft Edge basiert.  Ab Chrome bietet Microsoft Edge eine Gruppenrichtlinie, um diese Änderung bis Edge v88 zu deaktivieren.  For more information, including the planned timeline by Google for this change, navigate to the [Chrome Platform Status entry][ChromestatusFeature4664843055398912].  |  
| Dezente Aufforderung für Benachrichtigungsberechtigungsanforderungen anzeigen | Edge v84 |  | Still notification requests display a subtle request icon in the address bar for site notification permissions requested using the `Notifications` or `Push` API, replacing the full or standard permission flyout prompt UI.  Dieses Feature ist derzeit für alle Benutzer aktiviert.  Um stille Benachrichtigungsanforderungen zu deaktivieren, navigieren Sie zu `edge://settings/content/notifications` .  In Zukunft kann das Microsoft Edge-Team die erneute Aktivierung der vollständigen Flyout-Benachrichtigungsaufforderung in einigen Szenarien untersuchen.  |  
| Deaktivieren von TLS/1.0 und TLS/1.1 | Edge v84 |  |  |  
| Blockieren von Downloads gemischter Inhalte | [Chrome+1](#release-comments) \(Edge v86\)  |  | Diese Änderung erfolgt im Chromium Projekt, auf dem Microsoft Edge basiert.  For more information, including the planned timeline by Google for this change, navigate to the [Google security blog entry][GoogleBlogSecurity20200206].  Der Microsoft-Rolloutplan für Dateitypen, die gewarnt oder blockiert werden sollen, ist für eine Version nach Chrome geplant.  |  
| Veralteter AppCache | [Chrome+1](#release-comments) \(Edge v86\)  |  | Diese Änderung erfolgt im Chromium Projekt, auf dem Microsoft Edge basiert.  Navigieren Sie zur [WebDev-Dokumentation,][WebDevAppCacheRemoval]um weitere Informationen zu erfahren.  Der Microsoft-Rolloutplan für die Einstellung ist für eine Version nach Chrome geplant.  Das Anfordern eines [AppCache OriginTrial-Tokens][ChromeDevelopersOrigintrialsAppCacheOriginTrial] ermöglicht Es Websites, die veraltete API bis Edge v90 weiterhin zu verwenden.  |  
| Entfernen von Adobe Flash | Edge v88  |  | Diese Änderung erfolgt im Chromium Projekt, auf dem Microsoft Edge basiert.  Für weitere Informationen navigieren Sie zur [Adobe Flash Chromium Roadmap.][ChromiumFlashRoadmapSupportRemoved]  | 
| Entfernen der FTP-Unterstützung | Edge v88  | Edge Beta v87 | In Edge v88 wird die FTP-Unterstützung vollständig entfernt.  Diese Änderung erfolgt im Chromium Projekt, auf dem Microsoft Edge basiert.  Navigieren Sie für weitere Informationen zum [Chrome Platform-Statuseintrag.][ChromestatusFeature6246151319715840]  Unternehmen mit Websites, die weiterhin FTP-Unterstützung benötigen, können weiterhin FTP verwenden, indem sie die Website für den [IE-Modus][DeployedgeEdgeIeMode]konfigurieren.  | 
| AutoUpgrade gemischter Inhaltsbilder | Edge v88  |  | Nicht sichere \(HTTP\)-Verweise auf Bilder werden automatisch auf HTTPS aktualisiert. Wenn das Bild nicht über HTTPS verfügbar ist, schlägt der Bilddownload fehl. Zum Steuern dieses Features steht eine [Gruppenrichtlinie][DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls] zur Verfügung. Diese Änderung erfolgt im Chromium Projekt, auf dem Microsoft Edge basiert. Für weitere Informationen navigieren Sie zum [Chrome Platform Status-Eintrag.][ChromestatusFeature4926989725073408]  | 
| HTTP-Authentifizierung nicht zulässig, wenn Cookies von Drittanbietern blockiert werden  | Edge v87  |  | Ab Edge v87 ist auch die HTTP-Authentifizierung nicht zulässig, wenn Cookies für Anforderungen von Drittanbietern blockiert werden, entweder mithilfe der [BlockThirdPartyCookies-Richtlinie][DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies] oder der Umschaltfläche. `edge://settings` Diese Änderung kann sich auf Enterprise Mode [Site List-Downloads für den Internet Explorer-Modus][DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy] auswirken, wenn für den Endpunkt, der die Liste hostet, die Verwendung der HTTP-Authentifizierung erforderlich ist.  Um die Verwendung von Cookies und die HTTP-Authentifizierung für Enterprise Mode Site List-Downloads zuzulassen, fügen Sie der [CookiesAllowedForURLs-Richtlinie][DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls] ein übereinstimmendes URL-Muster hinzu.  |
| Entfernen von 3DES in TLS  | Edge v93  |  | Ab Edge v93 wird die Unterstützung für die TLS_RSA_WITH_3DES_EDE_CBC_SHA Verschlüsselungssuite entfernt. Diese Änderung erfolgt im Chromium Projekt, auf dem Microsoft Edge basiert. Für weitere Informationen navigieren Sie zum [Chrome Platform Status-Eintrag.][ChromestatusFeature6678134168485888] Darüber hinaus wird in Edge v93 eine Kompatibilitätsrichtlinie zur Unterstützung von Szenarien verfügbar sein, die die Kompatibilität mit veralteten Servern beibehalten müssen. Diese Kompatibilitätsrichtlinie wird veraltet und funktioniert in Edge v95 nicht mehr. Stellen Sie sicher, dass Sie betroffene Server vorher aktualisieren. |
| Einschränken privater Netzwerkanforderungen auf sichere Kontexte  | Edge v93  |  | Ab Edge v93 erfordert der Zugriff auf Ressourcen in lokalen (Intranet-)Netzwerken von Seiten im Internet, dass diese Seiten über HTTPS bereitgestellt werden. Diese Änderung erfolgt im Chromium Projekt, auf dem Microsoft Edge basiert. Für weitere Informationen navigieren Sie zum [Chrome Platform Status-Eintrag.][ChromestatusFeature5436853517811712] Zur Unterstützung von Szenarien, die die Kompatibilität mit nicht sicheren Seiten beibehalten müssen, stehen zwei Kompatibilitätsrichtlinien zur Verfügung: [InsecurePrivateNetworkRequestAllowed][DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowed] und [InsecurePrivateNetworkRequestAllowedForUrls.][DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowedForUrls] |

##### <a name="release-comments"></a>Anmerkungen zur Version  

:::row:::
   :::column span="1":::
      Chrome+1  
   :::column-end:::
   :::column span="2":::
      Basierend auf dem Feedback von Benutzern und Entwicklern wird das angegebene Feature oder die angegebene Änderung eine Version nach Chrome ausgeliefert.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome oder Chrome+1  
   :::column-end:::
   :::column span="2":::
      Basierend auf dem Feedback von Benutzern und Entwicklern wird das angegebene Feature oder die angegebene Änderung gleichzeitig oder mit einer Version nach Chrome ausgeliefert.  
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "Informationen zum | des IE-Modus Microsoft-Dokumente"  
[DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy]: /deployedge/edge-ie-mode-policies#configure-using-the-use-the-enterprise-mode-ie-website-list-policy "Konfigurieren mithilfe der IE-Websitelistenrichtlinie &quot;Use the Enterprise Mode IE&quot; – Konfigurieren von IE-Modusrichtlinien | Microsoft-Dokumente"  
[DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies]: /deployedge/microsoft-edge-policies#blockthirdpartycookies "BlockThirdPartyCookies – Microsoft Edge – Richtlinien | Microsoft-Dokumente"  
[DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]: /deployedge/microsoft-edge-policies#cookiesallowedforurls "CookiesAllowedForUrls – Microsoft Edge – Richtlinien | Microsoft-Dokumente"  
[DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls – Microsoft Edge – Richtlinien | Microsoft-Dokumente"  
[DeployedgeMicrosoftEdgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin – Microsoft Edge – Richtlinien | Microsoft-Dokumente"  
[DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowed]: /deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed "InsecurePrivateNetworkRequestsAllowed – Microsoft Edge – Richtlinien | Microsoft-Dokumente"
[DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowedForUrls]: /deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls "InsecurePrivateNetworkRequestsAllowedForUrls – Microsoft Edge – Richtlinien | Microsoft-Dokumente"

[ChromestatusFeaturesSchedule]: https://www.chromestatus.com/features/schedule "Veröffentlichungszeitachse | Chrome Platform Status"  
[ChromestatusFeature4664843055398912]: https://chromestatus.com/feature/4664843055398912 "Synchronisierungs-XHR in JavaScript-| zur Seitenentlassung nicht zulassen Chrome Platform Status"  
[ChromestatusFeature4926989725073408]: https://chromestatus.com/feature/4926989725073408 "| für gemischten Inhalt von Autoupgrade-Bildern Chrome Platform Status"  
[ChromestatusFeature5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Cookies standardmäßig sameSite=Lax | Chrome Platform Status"  
[ChromestatusFeature6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Veraltete FTP-Unterstützung | Chrome Platform Status"  
[ChromestatusFeature6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Referrer-Richtlinie: Standardeinstellung ist &quot;strict-origin-when-cross-origin&quot; | Chrome Platform Status"  
[ChromestatusFeature6678134168485888]: https://chromestatus.com/feature/6678134168485888 "Entfernen von 3DES in TLS-| Chrome Platform Status"
[ChromestatusFeature5436853517811712]: https://chromestatus.com/feature/5436853517811712 "Beschränken sie private Netzwerkanforderungen für Unterressourcen auf sichere Kontexte | Chrome Platform Status"
[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Flash-Unterstützung aus Chromium entfernt (Ziel: Chrome 88+ – Januar 2021) – Flash-Roadmap | Chromium Projekte"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "AppCache OriginTrial-Token | Chrome-Entwickler"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Schützen von Benutzern vor unsicheren Downloads in Google Chrome – Google Online Security Blog" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Vorbereiten der AppCache-Entfernung | web.dev"  

<!--todo:  cleanup links  -->  
