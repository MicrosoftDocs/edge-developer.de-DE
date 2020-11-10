---
description: Einführung in die Microsoft Edge (EdgeHTML)-Entwicklertools
title: Microsoft Edge (EdgeHTML)-Entwicklertools 
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, web development, f12 tools, devtools
experimental: true
experiment_id: "51fe4b97-3e55-41"
ms.localizationpriority: high
---

# Microsoft Edge (EdgeHTML)-Entwicklertools  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

Die Microsoft Edge (EdgeHTML)-Entwicklertools (DevTools) wurden mit [TypeScript][TypeScriptIndex] erstellt, basieren auf [Open Source][GithubMicrosoftChakracore], die für moderne Front-End-Workflows optimiert sind, und sind jetzt als [eigenständige Windows 10-App][MicrosoftStoreEdgeDevtoolsPreview] im Microsoft Store verfügbar!  

Wenn Sie mehr über die neuesten Funktionen erfahren möchten, lesen Sie [Entwicklertools in der neuesten Version von Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Grundlegende Tools  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
  Microsoft Edge (EdgeHTML) DevTools
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

Die Microsoft Edge (EdgeHTML) DevTools umfassen:  

*   Einen [Elemente][DevtoolsGuideEdgehtmlElements]-Bereich zum Bearbeiten von HTML und CSS, Untersuchen von Barrierefreiheitseigenschaften, Anzeigen von Ereignislistenern und Festlegen von DOM-Mutation-Haltepunkten  
*   Eine [Konsole][DevtoolsGuideEdgehtmlConsole] zum Anzeigen und Filtern von Protokollmeldungen, Überprüfen von JavaScript-Objekten und DOM-Knoten sowie zum Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Frames  
*   Einen [Debugger][DevtoolsGuideEdgehtmlDebugger] zum Durchlaufen von Code, Festlegen von Überwachungen und Haltepunkten, Bearbeiten von Code und Überprüfen von Webspeicher- und Cookie-Caches  
*   Einen [Netzwerk][DevtoolsGuideEdgehtmlNetwork]-Bereich zum Überwachen und Überprüfen von Anforderungen und Antworten aus dem Netzwerk und Browsercache  
*   Einen [Leistungsbereich][DevtoolsGuideEdgehtmlPerformance], um die Zeit und Systemressourcen zu ermitteln, die für Ihre Website erforderlich sind  
*   Einen [Arbeitsspeicher][DevtoolsGuideEdgehtmlMemory]-Bereich zum Messen der Nutzung von Speicherressourcen und Vergleichen von Heap-Momentaufnahmen in unterschiedlichen Code-Runtime-Phasen  
*   Einen [Speicher][DevtoolsGuideEdgehtmlStorage]-Bereich für die Überprüfung und Verwaltung von Webspeicher, IndexedDB, Cookies und Cachedaten  
*   Einen [Dienstmitarbeiter][DevtoolsGuideEdgehtmlServiceworkers]-Bereich zum Verwalten und Debuggen Ihrer Servicemitarbeiter  
*   Einen [Emulations][DevtoolsGuideEdgehtmlEmulation]-Bereich zum Testen Ihrer Website mit unterschiedlichen Browserprofilen, Bildschirmauflösungen und GPS-Positionskoordinaten  

Bitte senden Sie uns weiterhin [Ihr Feedback und Ihre Wünsche zu Features](#getting-in-touch-with-the-microsoft-edge-devtools-team)!  

> [! Tipp]
> [In Microsoft Edge (EdgeHTML) kostenlos über jeden Browser testen][BrowserstackEdgehtml].  
> Das Microsoft Edge-Team ist eine Partnerschaft mit [BrowserStack][BrowserstackEdgehtml] eingegangen, um ﻿kostenlose automatisierte und Live-Tests in Microsoft Edge (EdgeHTML) zu ermöglichen.  

## Microsoft Store-App  

Die **Microsoft Edge (EdgeHTML)-Entwicklertools** sind jetzt [als eigenständige][DevtoolsGuideEdgehtmlWhatsnew] [Windows 10-App im Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview] zusätzlich zum Tooling-Feature (`F12`) innerhalb des Browsers verfügbar. Die Store-Version verfügt über einen **Auswahl**-Bereich zum Anfügen für das Öffnen von lokalen und Remote-Seitenzielen sowie über ein Layout im Tab-Format für den einfachen Wechsel zwischen Entwicklertool-Instanzen.  

### Lokales Debugging  

Um eine Seite lokal zu debuggen, starten Sie einfach die Microsoft Edge-Entwicklertool-App. Im Bereich **Lokal** der Auswahl werden alle aktiven EdgeHTML-Inhaltsprozesse angezeigt, einschließlich geöffneter Edge Browser-Tabs, die, [PWAs][PwasEdgehtmlIndex] (`WWAHost.exe`-Prozesse) und [webview][HostingWebview]-Steuerelemente ausführen. Wählen Sie das gewünschte Ziel zum Anfügen aus, und öffnen Sie eine neue Tab-Instanz der Entwicklertools.  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Bereich ‚Lokal‘ in der Entwicklertools-App":::
  Bereich ‚Lokal‘ in der Entwicklertools-App
::: Image-End:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Remotedebugging  

Die Microsoft Edge-Entwicklertools-App bietet grundlegende Unterstützung beim Debuggen von Seiten auf einem Remotecomputer über unser neu veröffentlichtes [DevTools-Protokoll][DevtoolsProtocolEdgehtmlIndex]. Mit der neuesten Version wird der Remotezugriff auf die Kernfunktionen der Bereiche [Debugger][DevtoolsGuideEdgehtmlDebugger], [Elemente][DevtoolsGuideEdgehtmlElements] (für Vorgänge mit reinem Lesezugriff) und [Konsole][DevtoolsGuideEdgehtmlConsole] möglich. Das Remotedebugging ist auf Microsoft Edge (EdgeHTML) ausführende Desktop-Hosts beschränkt. Die Unterstützung weiterer EdgeHTML-Hosts und Windows 10-Geräte wird mit zukünftigen Versionen eingeführt.  

Lesen Sie für die ersten Schritte den Abschnitt [*Microsoft Edge DevTool*][DevtoolsProtocolEdgehtmlClientsEdgePreview] der [DevTools-Protokoll][DevtoolsProtocolEdgehtmlIndex]-Dokumente.  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="Bereich ‚Remote‘ in der Entwicklertools-App":::
  Bereich ‚Remote‘ in der Entwicklertools-App
::: Image-End:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Allgemeine Tastaturkurzbefehle  

> [! WICHTIG]
> Sämtliche Tastaturkurzbefehle wurden in der aktuellsten Windows-Version überprüft.  
> Sollte ein Tastaturkurzbefehl bei Ihnen nicht funktionieren, aktualisieren Sie Ihre Windows-Kopie.  

Mit diesen Tastaturkurzbefehlen wird das DevTools-Hauptfenster gesteuert. Sie sollten für alle Tools funktionieren.  

| Aktion | Tastaturkurzbefehl |  
|:--- |:--- |  
| Einblenden/Ausblenden der DevTools (es wird der zuletzt angezeigte Bereich geöffnet) | `F12` `STRG`+`UMSCHALT`+`I` |  
| Andocken umschalten (Abdocken/unten/rechts) | `STRG`+`UMSCHALT`+`D` |  
| Datei öffnen | `STRG`+`P`, `STRG`+`O` |  
| Nicht bearbeitbaren HTML-Quellcode im Debugger anzeigen | `STRG`+`U` |  
| Ein-/Ausblenden der Konsole unterhalb eines beliebigen anderen Tools | `STRG`+``  ` `` |  
| Zu "Elementen" wechseln (DOM-Explorer) | `STRG`+`1` |  
| Zu "Konsole" wechseln | `STRG`+`2` |  
| Zu "Debugger" wechseln | `STRG`+`3` |  
| Zu "Netzwerk" wechseln | `STRG`+`4` |  
| Zu "Leistung" wechseln | `STRG`+`5` |  
| Zu "Speicher" wechseln | `STRG`+`6` |  
| Zu "Emulation" wechseln | `STRG`+`7` |  
| Hilfedokumentation | `F1` |  
| Nächstes Tool | `STRG`+`F6` |  
| Vorheriges Tool | `STRG`+`UMSCHALT`+`F6` |  
| Vorheriges Tool (aus Verlauf) | `STRG`+`UMSCHALT`+`[` |  
| Nächstes Tool (aus Verlauf) | `STRG`+`UMSCHALT`+`]` |  
| Nächster Subframe | `F6` |  
| Vorheriger Subframe | `UMSCHALT`+`F6` |  
| Nächste Übereinstimmung im Suchfeld | `F3` |  
| Vorherige Übereinstimmung im Suchfeld | `UMSCHALT`+`F3` |  
| Im Suchfeld suchen | `STRG`+`F` |  
| Fokus auf Konsole am unteren Rand legen | `ALT`+`UMSCHALT`+`I` |  
| DevTools in Konsole starten | `STRG`+`UMSCHALT`+`J` |  
| Seite aktualisieren | `STRG`+`UMSCHALT`+`F5`, `STRG`+`R` |  

> [! HINWEIS]
> Wenn Sie während des Debuggens bei einem Haltepunkt pausiert haben, wird durch die Aktion **Seite aktualisieren** zuerst die Runtime fortgesetzt.  

## Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

Bitte senden Sie uns Ihr Feedback, um uns bei der Verbesserung der Microsoft Edge (EdgeHTML)-Entwicklertools zu helfen! Öffnen Sie einfach die Tools (`F12`), und klicken Sie dann auf die Schaltfläche [Feedback senden](#microsoft-edge-edgehtml-developer-tools).  

Werden Sie [Windows-Insider][WindowsInsiderProgram], um die [neuesten DevTools-Funktionen][DevtoolsGuideEdgehtmlWhatsnew] in der Vorschauversion ausprobieren zu können. Verwenden Sie die Windows-Feedback-Hub-App, um allgemeine Windows-Vorschläge und -Probleme zu veröffentlichen, zu bewerten, zu verfolgen und diesbezüglich Support zu erhalten.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Konsole"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Debugger"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elemente"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulation"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Arbeitsspeicher"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Netzwerk"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Leistung"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Dienstmitarbeiter"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Speicher"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools im neuesten Windows 10-Update (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Microsoft Edge (EdgeHTML) DevTools-Protokoll"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge-DevTools (Vorschau) – DevTools-Protokoll-Clients"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) für Windows 10-Apps"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Progressive Web Apps (EdgeHTML) unter Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge DevTools (Vorschau)"  

[WindowsInsiderProgram]: https://insider.windows.com "Windows-Insider-Programm"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Kostenloser Microsoft Edge-Browsertest | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
