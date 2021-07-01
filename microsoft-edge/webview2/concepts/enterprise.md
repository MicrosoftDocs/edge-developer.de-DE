---
description: Grundlegendes zum Verwalten von WebView2-Anwendungen
title: Verwalten von WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html, enterprise, group policy, manageability
ms.openlocfilehash: f32488a26f3e3c926517b0e40e6aac6a309e42b8
ms.sourcegitcommit: 5ae09b1ad6cd576c9fec12538b23cd849861f2b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "11627964"
---
# <a name="managing-webview2-applications"></a>Verwalten von WebView2-Anwendungen  

[WebView2][WebView2Landing] ist eine Komponente, die Entwickler zum Erstellen ihrer Anwendungen verwenden, und die Entwickler stellen möglicherweise eine [selbstaktualisierungsfähige Evergreen WebView2-Runtime][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] auf dem Benutzergerät bereit, um ihre Anwendungen zu unterstützen.  In diesem Dokument wird erläutert, wie IT-Administratoren WebView2-Anwendungen und Laufzeit verwalten können.  Feedback von IT-Administratoren und Entwicklern ist im [WebView2-Feedback-Repository][GithubMicrosoftedgeWebviewfeddback]willkommen.  

## <a name="group-policies-for-webview2"></a>Gruppenrichtlinien für WebView2  

IT-Administratoren können Gruppenrichtlinienobjekte \(GPO\) verwenden, um Richtlinieneinstellungen für WebView2 zu konfigurieren.  Die folgenden Richtlinien gelten nicht für WebView2,  

*   [Microsoft Edge : It-Administratoren][EdgeUpdatePolicies] stehen Updaterichtlinien zur Verfügung, um die Installations- und Updateaspekte der WebView2-Runtime zu verwalten.  Der Microsoft Edge Browser und WebView2 Runtime werden mit demselben Updatemechanismus aktualisiert.  Es sei denn, eine Richtlinie, z. `Update` B. , ist kanalspezifisch, gilt sowohl für den Browser als auch für WebView2 Runtime.  Ermöglicht ES IT-Administratoren beispielsweise, `UpdateSuppressed` die Zeit für jeden Tag festzulegen, um automatische Updates sowohl für den Browser als auch für die WebView2-Runtime zu unterdrücken.  Auf diese Weise können IT-Administratoren Einstellungen und Proxys einmal für den Browser und WebView2 Runtime konfigurieren, um die Netzwerkbandbreite/den Netzwerkdatenverkehr zu steuern oder für andere Zwecke.  IT-Administratoren folgen möglicherweise [Microsoft Edge Anleitung][ConfigureMicrosoftEdge] zum Konfigurieren von Microsoft Edge – Updaterichtlinien.  
*   [Microsoft Edge: Browserrichtlinien][EdgeBrowserPolicies] gelten nicht für WebView2-Anwendungen.  Dies ist beabsichtigt, da Apps und Browser unterschiedliche Anwendungsfälle haben und IT-Administratoren möglicherweise nicht wissen, welche Anwendungen WebView2 verwenden.  Das Anwenden von Browserrichtlinien auf WebView2 kann unbeabsichtigte Folgen haben.  IT-Administratoren können beispielsweise JavaScript im Browser blockieren, und alle WebView2-Apps, die JavaScript verwenden, sind fehlerhaft.  
*   [WebView2-spezifische Richtlinien][WebView2Policies] stehen Ihnen zur verfügung, um WebView2 direkt zu verwalten.  Es wird jedoch empfohlen, dass Entwickler ihre eigenen Gruppenrichtlinien implementieren, um die Verwendung von WebView2 zu verwalten, da es für Administratoren einfacher ist, die App zu verwalten, anstatt WebView2 direkt zu verwalten.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Grundlegendes zur WebView2-Laufzeit und zum Installationsprogramm (Vorschau) – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft-Dokumente"  

[WebView2Landing]: ../index.md "Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft-Dokumente"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge – Aktualisieren von Richtlinien | Microsoft-Dokumente"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge – Browserrichtlinien | Microsoft-Dokumente"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Konfigurieren Microsoft Edge Richtlinieneinstellungen für Windows | Microsoft-Dokumente"  
[WebView2Policies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2-Richtliniendokumentation | Microsoft-Dokumente" 

[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  
