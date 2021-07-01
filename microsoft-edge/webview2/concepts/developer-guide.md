---
description: Erfahren Sie mehr über bewährte Methoden für die Entwicklung ihrer WebView2-Anwendung.
title: Bewährte Methoden für die Entwicklung mit WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, Webview2, WebView, Webview, Edge, bewährte Methoden
ms.openlocfilehash: 7e8c6746e864b474c2987817c521224499a95e1f
ms.sourcegitcommit: 5ae09b1ad6cd576c9fec12538b23cd849861f2b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "11627978"
---
# <a name="webview2-development-best-practices"></a>Bewährte Methoden für die Entwicklung mit WebView2  

Jedes Entwicklungsteam folgt beim Erstellen seiner Anwendung unterschiedlichen Methoden. Wenn Sie WebView2-Anwendungen erstellen, wird empfohlen, dass Sie diese Vorgehensweisen befolgen. In diesem Artikel werden diese Empfehlungen und bewährten Methoden für Sie beim Erstellen produktionsbasierter WebView2-Anwendungen beschrieben.

## <a name="use-evergreen-webview2-runtime-recommended"></a>Verwenden von Evergreen WebView2 Runtime (empfohlen)  

Feste Version bietet zwar Anwendungsfälle für Apps mit strengen Kompatibilitätsanforderungen, es wird jedoch generell empfohlen, die Evergreen WebView2 Runtime zu verwenden.  Die Evergreen WebView2 Runtime-Updates werden automatisch aktualisiert und enthalten die neuesten Features und Sicherheitspatches, die für Ihre WebView2-Anwendung verfügbar sind. Die Evergreen WebView2 Runtime benötigt auch weniger Speicherplatz auf dem Datenträger.

Stellen Sie sicher, dass die Evergreen WebView2-Runtime installiert ist, bevor Sie Ihre WebView2-Anwendung verwenden.  Navigieren Sie für weitere Informationen zur [Bereitstellung der Evergreen WebView2 Runtime.][Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime]  

## <a name="run-compatibility-tests-regularly-when-using-the-evergreen-webview2-runtime"></a>Führen Sie bei Verwendung der Evergreen WebView2 Runtime regelmäßig Kompatibilitätstests aus.

Bei Verwendung der Evergreen WebView2 Runtime wird die Laufzeit automatisch aktualisiert, sodass Sie regelmäßig Kompatibilitätstests ausführen müssen. Testen Sie den Webinhalt im WebView2-Steuerelement mit den nicht stabilen Versionen von Microsoft Edge, um sicherzustellen, dass Ihre WebView2-Anwendung wie erwartet funktioniert.

Dieser Leitfaden ähnelt dem Leitfaden, den wir Webentwicklern bieten. Navigieren Sie im [Evergreen-Modus][Webview2ConceptsDistributionStayCompatibleEvergreenMode]zu "Kompatibel bleiben", um weitere Informationen zu erfahren.

## <a name="ensure-apis-are-supported-by-the-installed-webview2-runtime"></a>Stellen Sie sicher, dass APIs von der installierten WebView2 Runtime unterstützt werden.

WebView2-Anwendungen benötigen zum Ausführen sowohl ein Webview2 SDK als auch eine auf dem Computer installierte WebView2-Runtime. Sowohl das SDK als auch die Laufzeit sind versioniert. Da APIs ständig zu WebView2 hinzugefügt werden, werden auch neue Versionen der Laufzeit veröffentlicht, um die neuen APIs zu unterstützen. Stellen Sie sicher, dass die von Ihrer WebView2-Anwendung verwendeten APIs von der WebView2-Runtime unterstützt werden, die auf dem Computer installiert ist. 

Wenn Sie die Evergreen WebView2 Runtime verwenden, gibt es einige Szenarien, in denen die Laufzeit möglicherweise nicht aktualisiert wird, um die neueste Version zu verwenden. Wenn Benutzer beispielsweise keinen Internetzugang haben, wird die Laufzeit in dieser Umgebung nicht automatisch aktualisiert. Darüber hinaus unterbrechen einige Gruppenrichtlinien WebView2-Updates. Wenn Sie ein Update auf Ihre WebView2-Anwendung übertragen, kann die Anwendung beschädigt werden, da sie neuere APIs verwendet, die in der installierten Laufzeit nicht verfügbar sind.   
 
Um diese Situation zu lösen, können Sie die Verfügbarkeit der APIs in der installierten Laufzeit testen, bevor Ihr Code die API aufruft. Dieser Test für neuere Funktionen ähnelt anderen bewährten Methoden für die Webentwicklung, die unterstützte Features vor der Verwendung neuer Web-APIs erkennen. Um die API-Verfügbarkeit in der installierten Laufzeit zu testen, verwenden Sie Folgendes:  

*   Die `queryinterface` in C/C++. 
*   Ein try/catch-Block in .NET oder WinUI. 
    
Weitere Informationen finden Sie unter Ermitteln der [WebView2-Laufzeitanforderung.][Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement]  

## <a name="update-the-fixed-version-runtime"></a>Aktualisieren der Laufzeit mit fester Version  

Wenn Sie die Fixed Version Runtime verwenden, stellen Sie sicher, dass Sie Ihre Laufzeit regelmäßig aktualisieren, um potenzielle Sicherheitsrisiken zu verringern. Wenn Sie Inhalte von Drittanbietern in Webview2-Anwendungen verwenden, sollten Sie den Inhalt immer als nicht vertrauenswürdig betrachten.  Navigieren Sie zum [Verteilungsmodus für feste Versionen,][Webview2ConceptsDistributionFixedVersionDistributionMode]um weitere Informationen zu erfahren.  

## <a name="manage-new-versions-of-the-runtime"></a>Verwalten neuer Versionen der Laufzeit  

Wenn eine neue Version der Evergreen WebView2 Runtime auf das Gerät heruntergeladen wird, verwenden alle ausgeführten WebView2-Anwendungen weiterhin die vorherige Laufzeit, bis der Browserprozess freigegeben wird.  Dieses Verhalten ermöglicht die fortlaufende Ausführung von Anwendungen und verhindert, dass die vorherige Laufzeit gelöscht wird.  Um die neue Version der Laufzeit zu verwenden, müssen Sie alle Verweise auf die vorherigen WebView2-Umgebungsobjekte freigeben oder die Anwendung neu starten.  Wenn Sie das nächste Mal eine neue WebView2-Umgebung erstellen, wird die neue Version verwendet.

Wenn eine neue Version verfügbar ist, können Sie automatisch Maßnahmen ergreifen, z. B. den Benutzer benachrichtigen, die Anwendung neu zu starten.  Um zu erkennen, dass eine neue Version verfügbar ist, können Sie das [ereignis add_NewBrowserVersionAvailable(Win32)][Webview2ReferenceaddNewBrowserVersionAvailable] oder [CoreWebView2Environment.NewBrowserVersionAvailable(.NET)][Webview2ReferenceNewBrowserVersionAvailable] in Ihrem Code verwenden. Wenn der Code den Neustart der Anwendung verarbeitet, sollten Sie den Benutzerstatus speichern, bevor die WebView2-Anwendung beendet wird.  

## <a name="manage-the-lifetime-of-the-user-data-folder"></a>Verwalten der Lebensdauer des Benutzerdatenordners 
WebView2-Apps erstellen einen Benutzerdatenordner zum Speichern von Daten wie Cookies, Anmeldeinformationen und Berechtigungen.  Nach dem Erstellen des Ordners ist Ihre App für die Verwaltung der Lebensdauer des Benutzerdatenordners verantwortlich.  Ihre App muss beispielsweise eine Bereinigung durchführen, wenn die App deinstalliert wird.  Navigieren Sie zu ["Verwalten des Benutzerdatenordners",][Webview2ConceptsUserDataFolder]um weitere Informationen zu erfahren.  

## <a name="handle-runtime-process-failures"></a>Behandeln von Laufzeitprozessfehlern
Ihre WebView2-App sollte das Ereignis überwachen und `ProcessFailed` behandeln, damit die App nach Fehlern von Laufzeitprozessen, die den WebView2-App-Prozess unterstützen, wiederhergestellt werden kann.

WebView2-Apps werden von einer Sammlung von Laufzeitprozessen unterstützt, die zusammen mit dem App-Prozess ausgeführt werden. Diese unterstützenden Laufzeitprozesse können aus verschiedenen Gründen fehlschlagen, z. B. wenn der Arbeitsspeicher knapp wird oder vom Benutzer beendet wird. Wenn ein unterstützender Laufzeitprozess fehlschlägt, benachrichtigt WebView2 die Anwendung durch Auslösen des [ProcessFailed-Ereignisses.][WebView2ProcessFailedEvent]

## <a name="follow-recommended-webview2-security-best-practices"></a>Befolgen empfohlener bewährter Methoden für die WebView2-Sicherheit 
Stellen Sie für jede WebView2-Anwendung sicher, dass Sie die empfohlenen bewährten Methoden für die WebView2-Sicherheit befolgen.  Navigieren Sie für weitere Informationen zu bewährten Methoden für die [Entwicklung sicherer WebView2-Anwendungen.][Webview2ConceptsSecurity]  

<!-- links -->  

[Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime]: ../concepts/distribution.md#deploying-the-evergreen-webview2-runtime "Bereitstellen der Evergreen WebView2-Laufzeit – Verteilung von Apps mit WebView2 | Microsoft-Dokumente"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ../concepts/distribution.md#fixed-version-distribution-mode "Verteilungsmodus für feste Versionen – Verteilung von Apps mithilfe von WebView2 | Microsoft-Dokumente"  
[Webview2ConceptsDistributionStayCompatibleEvergreenMode]: ../concepts/distribution.md#stay-compatible-in-evergreen-mode "Im Evergreen-Modus kompatibel bleiben – Verteilung von Apps mit WebView2 | Microsoft-Dokumente"  
[Webview2ConceptsSecurity]: ../concepts/security.md "Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen | Microsoft-Dokumente"  
[Webview2ConceptsUserDataFolder]: ../concepts/user-data-folder.md "Verwalten des Benutzerdatenordners | Microsoft-Dokumente"  
[Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement]: ../concepts/versioning.md#determine-webview2-runtime-requirement "Ermitteln der WebView2-Laufzeitanforderung – Grundlegendes zu WebView2 SDK-Versionen | Microsoft-Dokumente"  
[Webview2GetStartedWin32]: ../get-started/win32.md "Erste Schritte mit WebView2 | Microsoft-Dokumente"  
[Webview2GetStartedWinforms]: ../get-started/winforms.md "Erste Schritte mit WebView2 in Windows Forms | Microsoft-Dokumente"  
[Webview2GetStartedWinui]: ../get-started/winui.md "Erste Schritte mit WebView2 in WinUI 3 (Vorschau) | Microsoft-Dokumente"  
[Webview2GetStartedWpf]: ../get-started/wpf.md "Erste Schritte mit WebView2 in WPF | Microsoft-Dokumente"  

[Webview2ReferenceaddNewBrowserVersionAvailable]: /microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable "add_NewBrowserVersionAvailable | Microsoft-Dokumente"  

[Webview2ReferenceNewBrowserVersionAvailable]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable "CoreWebView2Environment.NewBrowserVersionAvailable-Ereignis | Microsoft-Dokumente"  
[WebView2ProcessFailedEvent]: /microsoft-edge/webview2/reference/win32/icorewebview2processfailedeventargs "ICoreWebView2ProcessFailedEventArgs | Microsoft-Dokumente"  

