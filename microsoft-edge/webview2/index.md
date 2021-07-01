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
# <a name="introduction-to-microsoft-edge-webview2"></a>Einführung in Microsoft Edge WebView2  

Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webtechnologien \(HTML, CSS und JavaScript\) in Ihre nativen Apps einbetten.  Das WebView2-Steuerelement verwendet [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] als Renderingmodul, um den Webinhalt in systemeigenen Apps anzuzeigen.  Mit WebView2 können Sie Webcode in verschiedene Teile Ihrer systemeigenen App einbetten.  Erstellen Sie die gesamte systemeigene App in einer einzelnen WebView-Instanz.  Informationen zum Erstellen einer WebView2-App finden Sie unter [Erste Schritte](#get-started).  

:::image type="complex" source="./media/WebView2/what-webview.png" alt-text="Was ist WebView?" lightbox="./media/WebView2/what-webview.png":::
   Was ist WebView?  
:::image-end:::    

## <a name="hybrid-app-approach"></a>Hybrid-App-Ansatz  

Entwickler müssen sich häufig zwischen dem Erstellen einer Web-App oder einer nativen App entscheiden.  Die Entscheidung hängt vom Kompromiss zwischen Reichweite und Energie ab.  Web-Apps ermöglichen eine breite Reichweite.  Als Webentwickler können Sie den großteil ihres Codes auf verschiedenen Plattformen wiederverwenden.  Verwenden Sie eine systemeigene App, um auf alle Funktionen einer nativen Plattform zuzugreifen.  

:::image type="complex" source="./media/WebView2/web-native.png" alt-text="Systemeigenes Web" lightbox="./media/WebView2/web-native.png":::
   Systemeigenes Web  
:::image-end:::    

Hybrid-Apps ermöglichen Es Entwicklern, das Beste aus beiden Welten zu genießen.  Hybrid-App-Entwickler profitieren von den folgenden Vorteilen.  

*   Die Spezifität und Stärke der Webplattform.  
*   Die Leistungsfähigkeit und die vollständigen Funktionen der nativen Plattform.  
    
## <a name="webview2-benefits"></a>WebView2-Vorteile   

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
      ### <a name="web-ecosystem--skillset"></a>Webökosystem & Skillset  
   :::column-end:::
   :::column span="1":::
      ### <a name="rapid-innovation"></a>Schnelle Innovation  
   :::column-end:::
   :::column span="1":::
      ### <a name="windows-7-8-and-10-support"></a>Windows 7-, 8- und 10-Unterstützung  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Nutzen Sie die gesamte Webplattform, Bibliotheken, Tools und Begabungen, die innerhalb des Webökosystems vorhanden sind.  
   :::column-end:::
   :::column span="1":::
      Die Webentwicklung ermöglicht eine schnellere Bereitstellung und Iteration.  
   :::column-end:::
   :::column span="1":::
      Unterstützung für eine konsistente Benutzererfahrung in Windows 7, Windows 8 und Windows 10.  
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
      ### <a name="native-capabilities"></a>Systemeigene Funktionen  
   :::column-end:::
   :::column span="1":::
      ### <a name="code-sharing"></a>Codefreigabe  
   :::column-end:::
   :::column span="1":::
      ### <a name="microsoft-support"></a>Microsoft-Support  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Greifen Sie auf den vollständigen Satz systemeigener APIs zu.  
   :::column-end:::
   :::column span="1":::
      Das Hinzufügen von Webcode zu Ihrer Codebasis ermöglicht eine höhere Wiederverwendung auf mehreren Plattformen.  
   :::column-end:::
   :::column span="1":::
      Microsoft bietet Unterstützung und fügt neue Featureanforderungen hinzu, wenn WebView2 unter Allgemein verfügbar \(GA\) veröffentlicht wird.  
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
      ### <a name="evergreen-distribution"></a>Evergreen-Verteilung  
   :::column-end:::
   :::column span="1":::
      ### <a name="fixed"></a>Behoben  
   :::column-end:::
   :::column span="1":::
      ### <a name="incremental-adoption"></a>Inkrementelle Einführung  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Verlassen Sie sich auf eine aktuelle Version von Chromium mit regelmäßigen Plattformupdates und Sicherheitspatches.  
   :::column-end:::
   :::column span="1":::
      \(in Kürze verfügbar\) Wählen Sie aus, ob Sie die Chromium Bits in Ihrer App verpacken möchten.  
   :::column-end:::
   :::column span="1":::
      Fügen Sie Ihrer App Webkomponenten nach und nach hinzu.  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a>Erste Schritte  

Um Ihre App mithilfe des WebView2-Steuerelements zu erstellen und zu testen, müssen Sie <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  -->[WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installiert.  Wählen Sie eine der folgenden Optionen aus, um loszulegen.  

*   [Erste Schritte mit Win32 C/C++][Webview2GetStartedWin32]  
*   [Erste Schritte mit WPF][Webview2GetStartedWpf]  
*   [Erste Schritte mit WinForms][Webview2GetStartedWinforms]  
*   [Erste Schritte mit WinUI3][Webview2GetStartedWinui]  
    
Das [WebView2 Samples-Repository][GithubMicrosoftedgeWebview2samples] enthält Beispiele, die alle WebView2 SDK-Features und API-Verwendungsmuster veranschaulichen.  Wenn dem WebView2 SDK weitere Features hinzugefügt werden, werden die Beispiel-Apps aktualisiert.  

## <a name="supported-platforms"></a>Unterstützte Plattformen  

Eine Allgemeine Verfügbarkeit \(GA\) oder Vorschauversion ist in den folgenden Programmierumgebungen verfügbar.  

*   Win32 C/C++ \(GA\)  
*   .NET Framework 4.5 oder höher  
*   .NET Core 3.1 oder höher  
*   .NET 5  
*   [WinUI 3.0][UwpToolkitsWinui3] \(Vorschau\)  
    
Sie können WebView2-Apps in den folgenden Versionen von Windows ausführen.  

*   Windows 10  
*   Windows 8.1  
*   Windows 7 \*\*  
*   Windows Server 2019  
*   Windows Server 2016  
*   Windows Server 2012  
*   Windows Server 2012 R2  
*   Windows Server 2008 R2 \*\*  
    
> [!IMPORTANT]
> \*\* WebView2-Unterstützung für Windows 7 und Windows Server 2008 R2 hat den gleichen Supportzyklus wie Microsoft Edge.  Weitere Informationen erhalten Sie, wenn Sie zu [Microsoft Edge unterstützten Betriebssystemen][DeployedgeMicrosoftEdgeSupportedOS]navigieren.  

## <a name="next-steps"></a>Nächste Schritte  

Weitere Informationen zum Erstellen und Bereitstellen von WebView2-Apps finden Sie in der konzeptionellen Dokumentation und den Anleitungen.  

### <a name="concepts"></a>Konzepte  

*   [Grundlegendes zu WebView2 SDK-Versionen][Webview2ConceptsVersioning]  
*   [Verteilung von Apps mit WebView2][Webview2ConceptsDistribution]  
*   [Bewährte Methoden für die Entwicklung sicherer WebView2-Apps][Webview2ConceptsSecurity]  
*   [Verwalten des Benutzerdatenordners in WebView2-Apps][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a>How-To Handbücher  

*   [Debuggen mit WebView2][Webview2HowToDebug]  
*   [Automatisieren und Testen von WebView2 mit Microsoft Edge-Treiber][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team aufnehmen  

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
