---
description: Eine Einführung in das Konsolentool in den Microsoft Edge Developer Tools.
title: Verwenden der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: badcaae0ad637fe7a027f78d00daf9133789693e
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624745"
---
# <a name="use-the-console"></a>Verwenden der Konsole  

Das **Konsolentool** der DevTools hilft Ihnen bei verschiedenen Aufgaben.  Die folgende Liste enthält einige der Aufgaben.  

*   Erfahren Sie, warum etwas im aktuellen Projekt nicht funktioniert, und [ermitteln Sie Probleme.][DevtoolsConsoleConsoleDebugJavascript]  
*   [Abrufen von Informationen über das Webprojekt][DevtoolsConsoleConsoleFilters] im Browser als Protokollmeldungen.  
*   [Protokollieren Sie Informationen][DevtoolsConsoleConsoleLog] in Skripts zu Debugzwecken.  
*   [Testen Sie JavaScript-Ausdrücke][DevtoolsConsoleConsoleJavascript] live in einer [REPL-Umgebung.][WikiReadEvalPrintLoop]  
*   [Interagieren Sie mit dem Webprojekt im Browser][DevtoolsConsoleConsoleDomInteraction] mit JavaScript.  
    
Die **Konsole** ist ein hervorragendes Begleittool für die Verwendung mit anderen Tools.  Die **Konsole** bietet eine leistungsstarke Möglichkeit zum Skripten von Funktionen, zum Überprüfen und Bearbeiten der aktuellen Webseite mit JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-main.msft.png" alt-text="Das Konsolentool wird im oberen Bereich geöffnet" lightbox="../media/console-intro-console-main.msft.png":::
         Das **Konsolentool** wird im oberen Bereich geöffnet  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-panel.msft.png" alt-text="Konsole im unteren Bereich, über der das Elementtool geöffnet ist" lightbox="../media/console-intro-console-panel.msft.png":::
         **Konsole** im unteren Bereich, über der das **Elementtool** geöffnet ist  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Die schnellste Möglichkeit zum direkten Öffnen der **Konsole** besteht `Control` + `Shift` + `J` darin, \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) auszuwählen.  

## <a name="error-reports-and-console"></a>Fehlerberichte und Konsole  

**Die Konsole** ist der Standardort, an dem JavaScript- und Verbindungsfehler gemeldet werden.  Wenn Fehler auftreten, wird der **Problemindikator** neben dem **Einstellungen-Symbol** in DevTools angezeigt, das die Anzahl der Fehler und Warnungen bereitstellt.  Wählen Sie den **Problemindikator aus,** um **das** Problemtool zu öffnen und das Problem anzuzeigen.  Navigieren Sie zu [Debugfehlern,][DevtoolsConsoleConsoleDebugJavascript]die in der Konsole gemeldet werden, um weitere Informationen zu erfahren.

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools liefert detaillierte Informationen zu dem Fehler in der Konsole" lightbox="../media/console-debug-displays-error.msft.png":::
   DevTools liefert detaillierte Informationen zu dem Fehler in der **Konsole**  
:::image-end:::  

## <a name="inspect-and-filter-information-on-the-current-webpage"></a>Überprüfen und Filtern von Informationen auf der aktuellen Webseite  

Wenn Sie DevTools auf einer Webseite öffnen, gibt es möglicherweise eine große Menge an Informationen in der **Konsole.**  Die Menge der Informationen wird zum Problem, wenn Sie wichtige Informationen identifizieren müssen.  Verwenden Sie das Tool ["Probleme"][DevtoolsIssuesIndex] in DevTools, um die wichtigen Informationen anzuzeigen, die eine Aktion erfordern.

Probleme werden schrittweise von der **Konsole** in das **Tool "Probleme"** verschoben.  Es gibt jedoch immer noch viele Informationen in der **Konsole,** weshalb es ratsam ist, die automatisierten Protokoll- und Filteroptionen in der **Konsole**zu kennen.  Navigieren Sie zu ["Konsolenmeldungen filtern",][DevtoolsConsoleConsoleFilters]um weitere Informationen zu erfahren.

:::image type="complex" source="../media/console-intro-noise.msft.png" alt-text="DevTools mit einer Konsole voller Nachrichten" lightbox="../media/console-intro-noise.msft.png":::
   DevTools mit einer **Konsole** voller Nachrichten  
:::image-end:::  

## <a name="log-information-to-display-in-the-console"></a>Protokollinformationen, die in der Konsole angezeigt werden sollen  

Der am häufigsten verwendete Anwendungsfall für die **Konsole** ist das Protokollieren von Informationen aus Ihren Skripts mithilfe der `console.log()` Methode oder anderer ähnlicher Methoden.  Führen Sie die folgenden Aktionen aus, um es zu testen.  

1.  Wählen Sie zum Öffnen der **Konsole** `Control` + `Shift` + `J` \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.  
1.  Navigieren Sie zu [Beispielen für Konsolenmeldungen: Protokoll, Informationen, Fehler und Warnungen,][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]oder kopieren Sie den folgenden Codeausschnitt in der **Konsole,** und führen Sie ihn aus.  
    
    ```javascript
    console.log('This is a log message');
    console.info('This is some information'); 
    console.error('This is an error');
    console.warn('This is a warning');
    console.log(document.body.getBoundingClientRect());
    console.table(document.body.getBoundingClientRect());
    let technologies = ["HTML", "CSS", "SVG", "ECMAScript"];
    console.groupCollapsed('Technolgies');
    technologies.forEach(tech => {console.info(tech);})
    console.groupEnd('Technolgies');
    ```  
    
1.  Die **Konsole** zeigt die Ergebnisse an.  
    
    :::image type="complex" source="../media/console-intro-logging.msft.png" alt-text="Konsole mit Nachrichten, die durch Democode verursacht wurden" lightbox="../media/console-intro-logging.msft.png":::
       **Konsole** mit Nachrichten, die durch Democode verursacht wurden  
    :::image-end:::  
    
Viele nützliche Methoden stehen zur Verfügung, wenn Sie mit der **Konsole**arbeiten.  Navigieren Sie im [Konsolentool][DevtoolsConsoleConsoleLog]zu Protokollieren von Nachrichten, um weitere Informationen zu erfahren.  

## <a name="try-your-javascript-live-in-the-console"></a>Testen Von JavaScript live in der Konsole  

Die **Konsole** ist nicht nur ein Ort zum Protokollieren von Informationen.  Die **Konsole** ist eine [REPL-Umgebung.][WikiReadEvalPrintLoop]  Wenn Sie JavaScript in der **Konsole**schreiben, wird der Code sofort ausgeführt.  Möglicherweise ist es hilfreich, einige neue JavaScript-Features zu testen oder einige schnelle Berechnungen durchzuführen.  Außerdem erhalten Sie alle Features, die Sie von einer modernen Bearbeitungsumgebung erwarten, z. B. autocompletion, Syntaxhervorhebung und Verlauf.  Führen Sie die folgenden Aktionen aus, um es zu testen.  

1.  Navigieren Sie zur **Konsole.**  
1.  Geben Sie `2 + 2` ein.  
    
In der **Konsole** wird das Ergebnis `4` in der folgenden Zeile angezeigt.  Dieses Feature für die prüfungswillige **Prüfung** ist nützlich, um zu debuggen und zu überprüfen, ob Sie in Ihrem Code keine Fehler machen.  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="Die Konsole zeigt das Ergebnis von 2 + 2 live während der Eingabe an." lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   Die **Konsole** zeigt das Ergebnis von Live während der `2 + 2` Eingabe an.  
:::image-end:::  

Um den JavaScript-Ausdruck in der **Konsole** auszuführen und optional ein Ergebnis anzuzeigen, wählen Sie `Enter` .  Anschließend können Sie den nächsten JavaScript-Code schreiben, der in der **Konsole**ausgeführt werden soll.  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Ausführen mehrerer JavaScript-Codezeilen nacheinander" lightbox="../media/console-javascript-several-expressions.msft.png":::
   Ausführen mehrerer JavaScript-Codezeilen nacheinander  
:::image-end:::  

Standardmäßig führen Sie JavaScript-Code in einer einzigen Zeile aus.  Um eine Zeile auszuführen, geben Sie Ihr JavaScript ein, und wählen Sie dann `Enter` aus.  Um die einzeilige Einschränkung zu umgehen, wählen Sie `Shift` + `Enter` anstelle von `Enter` .  Wählen Sie, ähnlich wie bei anderen Befehlszeilenfunktionen, die Option aus, um auf Ihre vorherigen JavaScript-Befehle `Arrow-Up` zuzugreifen.  Das Feature für die automatische Vervollständigung der **Konsole** ist eine hervorragende Möglichkeit, sich mit unbekannten Methoden vertraut zu machen.  Führen Sie die folgenden Aktionen aus, um es zu testen.  

1.  Öffnen Sie die **Konsole**.  
1.  Geben Sie `doc` ein.  
1.  Wählen Sie `document` aus dem Dropdownmenü aus.  
1.  Wählen Sie den `tab` Schlüssel aus, um ihn auszuwählen.  
1.  Geben Sie `.bo` ein.  
1.  Wählen Sie `tab` aus, um `document.body` .  
1.  Geben Sie einen anderen Typ `.` ein, um die vollständige Liste der Eigenschaften und Methoden anzuzeigen, die im Textkörper der aktuellen Webseite verfügbar sind.  
    
Weitere Informationen zu allen Möglichkeiten zum Arbeiten mit **der Konsole**finden Sie in der Konsole [als JavaScript-Umgebung.][DevtoolsConsoleConsoleJavascript]  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Automatische Konsolenkompletion von JavaScript-Ausdrücken" lightbox="../media/console-javascript-autocomplete.msft.png":::
   **Automatische Konsolenkompletion** von JavaScript-Ausdrücken  
:::image-end:::  

## <a name="interact-with-the-current-webpage-in-the-browser"></a>Interagieren mit der aktuellen Webseite im Browser  

Die **Konsole** hat Zugriff auf das [Window-Objekt][MdnDocsWebApiWindow] des Browsers.  Sie können Skripts schreiben, die mit der aktuellen Webseite interagieren.  Führen Sie die folgenden Aktionen aus, um es zu testen.  

1.  Öffnen Sie die **Konsole**.  
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.  
    
    ```javascript
    document.querySelector('h1').innerHTML
    ```  
    
:::image type="complex" source="../media/console-intro-reading-DOM.msft.png" alt-text="Kopieren des Inhalts der oberen Überschrift (h1) aus dem DOM und Anzeigen in der Konsole" lightbox="../media/console-intro-reading-DOM.msft.png":::
   Kopieren Sie den Inhalt der oberen Überschrift \( `h1` \) aus dem DOM, und zeigen Sie sie in der **Konsole** an.  
:::image-end:::  

Anstatt nur von der Webseite zu lesen, können Sie sie auch ändern.  Führen Sie die folgenden Aktionen aus, um zu versuchen, die Webseite zu ändern.  

1.  Öffnen Sie die **Konsole**.  
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.  
    
    ```javascript
    document.querySelector('h1').innerHTML = 'Rocking the Console';
    ```  
    
:::image type="complex" source="../media/console-intro-wrtiting-DOM.msft.png" alt-text="Schreiben von Text in das DOM in der Konsole" lightbox="../media/console-intro-wrtiting-DOM.msft.png":::
   Schreiben von Text in das DOM in der **Konsole**  
:::image-end:::  

Sie haben die Hauptüberschrift der Webseite in **"Wackeln der Konsole"** geändert.  Die **Konsolenhilfsprogrammmethoden** erleichtern den Zugriff auf die aktuelle Webseite und deren Bearbeitung.  Navigieren Sie für weitere Informationen zur [API-Referenz für Konsolenprogramme.][DevtoolsConsoleUtilities]  Um beispielsweise einen grünen Rahmen um alle Links auf der aktuellen Webseite hinzuzufügen, führen Sie die folgenden Aktionen aus.  

1.  Öffnen Sie die **Konsole**.  
1.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.  
    
    ```javascript
    $$('a').forEach(a => a.style.border='1px solid lime');
    ```  
    
:::image type="complex" source="../media/console-intro-changing-styles.msft.png" alt-text="Bearbeiten einer Auswahl von Elementen mithilfe der Konsole" lightbox="../media/console-intro-changing-styles.msft.png":::
    Bearbeiten einer Auswahl von Elementen mithilfe der **Konsole**  
:::image-end:::  

For more information about working with the DOM, navigate to [Use the Console to interact with the DOM][DevtoolsConsoleConsoleDomInteraction].  

## <a name="learn-more-about-console"></a>Weitere Informationen zur Konsole  

For more information about the **Console**, navigate to [Console reference][DevtoolsConsoleReference], Console Utilities [API reference][DevtoolsConsoleUtilities], and Console [API reference][DevtoolsConsoleApi].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  
[DevtoolsConsoleApi]: ./api.md "Konsolen-API-Referenz | Microsoft-Dokumente"  
[DevtoolsConsoleConsoleDebugJavascript]: ./console-debug-javascript.md "Debugfehler, die in Konsolen-| gemeldet wurden Microsoft-Dokumente"  
[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Verwenden der Konsole für die Interaktion mit dem DOM-| Microsoft-Dokumente" 
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtern von Konsolenmeldungen | Microsoft-Dokumente"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Konsole als JavaScript-Umgebung | Microsoft-Dokumente"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Protokollieren von Nachrichten im Konsolentool | Microsoft-Dokumente"  
[DevtoolsConsoleReference]: ./reference.md "Konsolenreferenz | Microsoft-Dokumente"  
[DevtoolsConsoleUtilities]: ./utilities.md "API-Referenz für Konsolenprogramme | Microsoft-Dokumente"  
[DevtoolsIssuesIndex]: ../issues/index.md "Suchen und Beheben von Problemen mithilfe des Tools &quot;Probleme&quot; | Microsoft-Dokumente"  
<!-- external links -->
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-demo.html "Beispiele für Konsolenmeldungen: Protokollieren, Informationen, Fehler und Warnen | GitHub"  
[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Fenster | Mdn"  
[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Read-eval-print-| Wikipedia"  
