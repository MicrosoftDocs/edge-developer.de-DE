---
description: Erfahren Sie, was als Nächstes für WebView2 verfügbar ist.
title: Roadmap für Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 7b67e4a6844ead0f845667a70df8657745ece938
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643420"
---
# <a name="microsoft-edge-webview2-roadmap"></a>Microsoft Edge WebView2-Roadmap  

> [!NOTE]
> Last Updated: July 2021  

Mit dem WebView2-Steuerelement können Entwickler Webtechnologien in ihre nativen Anwendungen einbetten.  Auf der folgenden Seite wird die potenzielle Roadmap für WebView2 beschrieben.  

> [!NOTE]
> WebView2 befindet sich in der aktiven Entwicklung, und die Roadmap wird basierend auf Marktänderungen und Kundenfeedback weiterentwickelt. Beachten Sie daher, dass die hier beschriebenen Pläne nicht vollständig sind und änderungen vorbehalten sind.  

Wenn Sie Bedenken oder Fragen zur Roadmap haben, geben Sie Ihr Feedback im [Feedback-Repository.][GithubMicrosoftedgeWebviewfeedbackMain]  

Das WebView2-Team plant die folgenden wichtigen Anstrengungen für zukünftige Updates.  

* UWP-Vorschau
* MacOS Preview
* Xbox Preview
* HoloLens Vorschau

## <a name="webview2-runtime-and-installer"></a>WebView2 Runtime und Installer  

Mit dem [Evergreen-Verteilungsmodell][ConceptDistributionEvergreenModel] können Sie die WebView2-Runtime als Ziel oder Kette auf dem Computer Des Benutzers installieren.  Die Evergreen WebView2 Runtime und das Installationsprogramm haben die allgemeine Verfügbarkeit \(GA\) erreicht.  

## <a name="fixed-version"></a>Feste Version  

Mit [dem Verteilungsmodell][ConceptsDistributionFixedVersionModel] für feste Versionen können Sie die Microsoft Edge Binärdateien in Ihrer systemeigenen Anwendung verpacken.  Die feste Version hat die allgemeine Verfügbarkeit \(GA\) erreicht.  

## <a name="general-availability"></a>Allgemeine Verfügbarkeit  

### <a name="win32-cc"></a>Win32 C/C++  

Das Win32 C/C++-SDK hat GA erreicht.  

### <a name="net"></a>.NET  

Das .NET SDK hat ga erreicht. 

### <a name="windows-ui-library-3"></a>Windows UI Library 3

Sie können in Ihren Anwendungen mit [Windows UI Library 3 (WinUI3)][UwpToolkitsWinui3Index] mit dem Windows App SDK auf WebView2-Steuerelemente zugreifen. Dies befindet sich derzeit in der Vorschau. Weitere Informationen finden Sie im [Windows App SDK-Roadmap.][WindowsAppSDK|::ref1::|]

 
<!-- links -->  

[WindowsAppSDKRoadmap]: https://github.com/microsoft/WindowsAppSDK/blob/main/docs/roadmap.md "Fahrplan"
[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Evergreen-Verteilungsmodell – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft-Dokumente"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Verteilungsmodell für feste Versionen – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft-Dokumente"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows UI Library 3.0 Preview 1 (Mai 2020) | Microsoft-Dokumente"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Windows Benutzeroberflächenbibliothek-Roadmap – microsoft/microsoft-ui-xaml-| GitHub"  
