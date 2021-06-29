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
# <a name="use-the-console"></a><span data-ttu-id="31acb-104">Verwenden der Konsole</span><span class="sxs-lookup"><span data-stu-id="31acb-104">Use the Console</span></span>  

<span data-ttu-id="31acb-105">Das **Konsolentool** der DevTools hilft Ihnen bei verschiedenen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="31acb-105">The **Console** tool of the DevTools helps you with several tasks.</span></span>  <span data-ttu-id="31acb-106">Die folgende Liste enthält einige der Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="31acb-106">The following list includes some of the tasks.</span></span>  

*   <span data-ttu-id="31acb-107">Erfahren Sie, warum etwas im aktuellen Projekt nicht funktioniert, und [ermitteln Sie Probleme.][DevtoolsConsoleConsoleDebugJavascript]</span><span class="sxs-lookup"><span data-stu-id="31acb-107">Find out why something isn't working in the current project and [track down problems][DevtoolsConsoleConsoleDebugJavascript].</span></span>  
*   <span data-ttu-id="31acb-108">[Abrufen von Informationen über das Webprojekt][DevtoolsConsoleConsoleFilters] im Browser als Protokollmeldungen.</span><span class="sxs-lookup"><span data-stu-id="31acb-108">[Get information about the web project][DevtoolsConsoleConsoleFilters] in the browser as log messages.</span></span>  
*   <span data-ttu-id="31acb-109">[Protokollieren Sie Informationen][DevtoolsConsoleConsoleLog] in Skripts zu Debugzwecken.</span><span class="sxs-lookup"><span data-stu-id="31acb-109">[Log information][DevtoolsConsoleConsoleLog] in scripts for debugging purposes.</span></span>  
*   <span data-ttu-id="31acb-110">[Testen Sie JavaScript-Ausdrücke][DevtoolsConsoleConsoleJavascript] live in einer [REPL-Umgebung.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="31acb-110">[Try JavaScript expressions][DevtoolsConsoleConsoleJavascript] live in a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  
*   <span data-ttu-id="31acb-111">[Interagieren Sie mit dem Webprojekt im Browser][DevtoolsConsoleConsoleDomInteraction] mit JavaScript.</span><span class="sxs-lookup"><span data-stu-id="31acb-111">[Interact with the web project in the browser][DevtoolsConsoleConsoleDomInteraction] using JavaScript.</span></span>  
    
<span data-ttu-id="31acb-112">Die **Konsole** ist ein hervorragendes Begleittool für die Verwendung mit anderen Tools.</span><span class="sxs-lookup"><span data-stu-id="31acb-112">The **Console** is a great companion tool to use with others tools.</span></span>  <span data-ttu-id="31acb-113">Die **Konsole** bietet eine leistungsstarke Möglichkeit zum Skripten von Funktionen, zum Überprüfen und Bearbeiten der aktuellen Webseite mit JavaScript.</span><span class="sxs-lookup"><span data-stu-id="31acb-113">The **Console** provides a powerful way to script functionality, inspect, and manipulate the current webpage using JavaScript.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-main.msft.png" alt-text="Das Konsolentool wird im oberen Bereich geöffnet" lightbox="../media/console-intro-console-main.msft.png":::
         <span data-ttu-id="31acb-115">Das **Konsolentool** wird im oberen Bereich geöffnet</span><span class="sxs-lookup"><span data-stu-id="31acb-115">The **Console** tool open in the upper panel</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-panel.msft.png" alt-text="Konsole im unteren Bereich, über der das Elementtool geöffnet ist" lightbox="../media/console-intro-console-panel.msft.png":::
         <span data-ttu-id="31acb-117">**Konsole** im unteren Bereich, über der das **Elementtool** geöffnet ist</span><span class="sxs-lookup"><span data-stu-id="31acb-117">**Console** in the lower panel with the **Elements** tool open above it</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="31acb-118">Die schnellste Möglichkeit zum direkten Öffnen der **Konsole** besteht `Control` + `Shift` + `J` darin, \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="31acb-118">The fastest way to directly open the **Console** is to select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

## <a name="error-reports-and-console"></a><span data-ttu-id="31acb-119">Fehlerberichte und Konsole</span><span class="sxs-lookup"><span data-stu-id="31acb-119">Error reports and Console</span></span>  

<span data-ttu-id="31acb-120">**Die Konsole** ist der Standardort, an dem JavaScript- und Verbindungsfehler gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="31acb-120">**Console** is the default place where JavaScript and connectivity errors are reported.</span></span>  <span data-ttu-id="31acb-121">Wenn Fehler auftreten, wird der **Problemindikator** neben dem **Einstellungen-Symbol** in DevTools angezeigt, das die Anzahl der Fehler und Warnungen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="31acb-121">If any errors occur, the **Issues counter** is displayed next to the **Settings** icon in DevTools that provides the number of errors and warnings.</span></span>  <span data-ttu-id="31acb-122">Wählen Sie den **Problemindikator aus,** um **das** Problemtool zu öffnen und das Problem anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="31acb-122">Select the **Issues counter** to open the **Issues** tool and display the problem.</span></span>  <span data-ttu-id="31acb-123">Navigieren Sie zu [Debugfehlern,][DevtoolsConsoleConsoleDebugJavascript]die in der Konsole gemeldet werden, um weitere Informationen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="31acb-123">For more information, navigate to [Debug errors reported in Console][DevtoolsConsoleConsoleDebugJavascript].</span></span>

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools liefert detaillierte Informationen zu dem Fehler in der Konsole" lightbox="../media/console-debug-displays-error.msft.png":::
   <span data-ttu-id="31acb-125">DevTools liefert detaillierte Informationen zu dem Fehler in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="31acb-125">DevTools gives detailed information about the error in the **Console**</span></span>  
:::image-end:::  

## <a name="inspect-and-filter-information-on-the-current-webpage"></a><span data-ttu-id="31acb-126">Überprüfen und Filtern von Informationen auf der aktuellen Webseite</span><span class="sxs-lookup"><span data-stu-id="31acb-126">Inspect and filter information on the current webpage</span></span>  

<span data-ttu-id="31acb-127">Wenn Sie DevTools auf einer Webseite öffnen, gibt es möglicherweise eine große Menge an Informationen in der **Konsole.**</span><span class="sxs-lookup"><span data-stu-id="31acb-127">When you open DevTools on a webpage, there may be an overwhelming amount of information in the **Console**.</span></span>  <span data-ttu-id="31acb-128">Die Menge der Informationen wird zum Problem, wenn Sie wichtige Informationen identifizieren müssen.</span><span class="sxs-lookup"><span data-stu-id="31acb-128">The amount of information becomes a problem when you need to identify important information.</span></span>  <span data-ttu-id="31acb-129">Verwenden Sie das Tool ["Probleme"][DevtoolsIssuesIndex] in DevTools, um die wichtigen Informationen anzuzeigen, die eine Aktion erfordern.</span><span class="sxs-lookup"><span data-stu-id="31acb-129">To view the important information that needs action, use the [Issues][DevtoolsIssuesIndex] tool in DevTools.</span></span>

<span data-ttu-id="31acb-130">Probleme werden schrittweise von der **Konsole** in das **Tool "Probleme"** verschoben.</span><span class="sxs-lookup"><span data-stu-id="31acb-130">Issues are gradually being moved from the **Console** to the **Issues** tool.</span></span>  <span data-ttu-id="31acb-131">Es gibt jedoch immer noch viele Informationen in der **Konsole,** weshalb es ratsam ist, die automatisierten Protokoll- und Filteroptionen in der **Konsole**zu kennen.</span><span class="sxs-lookup"><span data-stu-id="31acb-131">However, there's still a lot of information in **Console**, which is why it's a good idea to know about the automated log and filter options in the **Console**.</span></span>  <span data-ttu-id="31acb-132">Navigieren Sie zu ["Konsolenmeldungen filtern",][DevtoolsConsoleConsoleFilters]um weitere Informationen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="31acb-132">For more information, navigate to [Filter Console messages][DevtoolsConsoleConsoleFilters].</span></span>

:::image type="complex" source="../media/console-intro-noise.msft.png" alt-text="DevTools mit einer Konsole voller Nachrichten" lightbox="../media/console-intro-noise.msft.png":::
   <span data-ttu-id="31acb-134">DevTools mit einer **Konsole** voller Nachrichten</span><span class="sxs-lookup"><span data-stu-id="31acb-134">DevTools with a **Console** full of messages</span></span>  
:::image-end:::  

## <a name="log-information-to-display-in-the-console"></a><span data-ttu-id="31acb-135">Protokollinformationen, die in der Konsole angezeigt werden sollen</span><span class="sxs-lookup"><span data-stu-id="31acb-135">Log information to display in the Console</span></span>  

<span data-ttu-id="31acb-136">Der am häufigsten verwendete Anwendungsfall für die **Konsole** ist das Protokollieren von Informationen aus Ihren Skripts mithilfe der `console.log()` Methode oder anderer ähnlicher Methoden.</span><span class="sxs-lookup"><span data-stu-id="31acb-136">The most popular use case for the **Console** is logging information from your scripts using the `console.log()` method or other similar methods.</span></span>  <span data-ttu-id="31acb-137">Führen Sie die folgenden Aktionen aus, um es zu testen.</span><span class="sxs-lookup"><span data-stu-id="31acb-137">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="31acb-138">Wählen Sie zum Öffnen der **Konsole** `Control` + `Shift` + `J` \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="31acb-138">To open **Console**, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="31acb-139">Navigieren Sie zu [Beispielen für Konsolenmeldungen: Protokoll, Informationen, Fehler und Warnungen,][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]oder kopieren Sie den folgenden Codeausschnitt in der **Konsole,** und führen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="31acb-139">Navigate to [Console messages examples: log, info, error and warn][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml], or copy and run the following code snippet in the **Console**.</span></span>  
    
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
    
1.  <span data-ttu-id="31acb-140">Die **Konsole** zeigt die Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="31acb-140">The **Console** displays the results.</span></span>  
    
    :::image type="complex" source="../media/console-intro-logging.msft.png" alt-text="Konsole mit Nachrichten, die durch Democode verursacht wurden" lightbox="../media/console-intro-logging.msft.png":::
       <span data-ttu-id="31acb-142">**Konsole** mit Nachrichten, die durch Democode verursacht wurden</span><span class="sxs-lookup"><span data-stu-id="31acb-142">**Console** full of messages caused by demo code</span></span>  
    :::image-end:::  
    
<span data-ttu-id="31acb-143">Viele nützliche Methoden stehen zur Verfügung, wenn Sie mit der **Konsole**arbeiten.</span><span class="sxs-lookup"><span data-stu-id="31acb-143">Many useful methods are available when you work with the **Console**.</span></span>  <span data-ttu-id="31acb-144">Navigieren Sie im [Konsolentool][DevtoolsConsoleConsoleLog]zu Protokollieren von Nachrichten, um weitere Informationen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="31acb-144">For more information, navigate to [Log messages in the Console tool][DevtoolsConsoleConsoleLog].</span></span>  

## <a name="try-your-javascript-live-in-the-console"></a><span data-ttu-id="31acb-145">Testen Von JavaScript live in der Konsole</span><span class="sxs-lookup"><span data-stu-id="31acb-145">Try your JavaScript live in the Console</span></span>  

<span data-ttu-id="31acb-146">Die **Konsole** ist nicht nur ein Ort zum Protokollieren von Informationen.</span><span class="sxs-lookup"><span data-stu-id="31acb-146">The **Console** isn't only a place to log information.</span></span>  <span data-ttu-id="31acb-147">Die **Konsole** ist eine [REPL-Umgebung.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="31acb-147">The **Console** is a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  <span data-ttu-id="31acb-148">Wenn Sie JavaScript in der **Konsole**schreiben, wird der Code sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31acb-148">When you write any JavaScript in the **Console**, the code runs immediately.</span></span>  <span data-ttu-id="31acb-149">Möglicherweise ist es hilfreich, einige neue JavaScript-Features zu testen oder einige schnelle Berechnungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="31acb-149">You may find it useful to test some new JavaScript features or to do some quick calculations.</span></span>  <span data-ttu-id="31acb-150">Außerdem erhalten Sie alle Features, die Sie von einer modernen Bearbeitungsumgebung erwarten, z. B. autocompletion, Syntaxhervorhebung und Verlauf.</span><span class="sxs-lookup"><span data-stu-id="31acb-150">Also, you get all of the features you expect from a modern editing environment, such as autocompletion, syntax highlighting, and history.</span></span>  <span data-ttu-id="31acb-151">Führen Sie die folgenden Aktionen aus, um es zu testen.</span><span class="sxs-lookup"><span data-stu-id="31acb-151">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="31acb-152">Navigieren Sie zur **Konsole.**</span><span class="sxs-lookup"><span data-stu-id="31acb-152">Navigate to the **Console**.</span></span>  
1.  <span data-ttu-id="31acb-153">Geben Sie `2 + 2` ein.</span><span class="sxs-lookup"><span data-stu-id="31acb-153">Type `2 + 2`.</span></span>  
    
<span data-ttu-id="31acb-154">In der **Konsole** wird das Ergebnis `4` in der folgenden Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31acb-154">The **Console** displays the result `4` on the following line.</span></span>  <span data-ttu-id="31acb-155">Dieses Feature für die prüfungswillige **Prüfung** ist nützlich, um zu debuggen und zu überprüfen, ob Sie in Ihrem Code keine Fehler machen.</span><span class="sxs-lookup"><span data-stu-id="31acb-155">This **Eager evaluation** feature is useful to debug and verify that you aren't making mistakes in your code.</span></span>  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="Die Konsole zeigt das Ergebnis von 2 + 2 live während der Eingabe an." lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   <span data-ttu-id="31acb-157">Die **Konsole** zeigt das Ergebnis von Live während der `2 + 2` Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="31acb-157">The **Console** displays the result of `2 + 2` live as you type it</span></span>  
:::image-end:::  

<span data-ttu-id="31acb-158">Um den JavaScript-Ausdruck in der **Konsole** auszuführen und optional ein Ergebnis anzuzeigen, wählen Sie `Enter` .</span><span class="sxs-lookup"><span data-stu-id="31acb-158">To run the JavaScript expression in the **Console** and optionally display a result, select `Enter`.</span></span>  <span data-ttu-id="31acb-159">Anschließend können Sie den nächsten JavaScript-Code schreiben, der in der **Konsole**ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="31acb-159">Then, you can write the next JavaScript code to run in the **Console**.</span></span>  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Ausführen mehrerer JavaScript-Codezeilen nacheinander" lightbox="../media/console-javascript-several-expressions.msft.png":::
   <span data-ttu-id="31acb-161">Ausführen mehrerer JavaScript-Codezeilen nacheinander</span><span class="sxs-lookup"><span data-stu-id="31acb-161">Run several lines of JavaScript code in succession</span></span>  
:::image-end:::  

<span data-ttu-id="31acb-162">Standardmäßig führen Sie JavaScript-Code in einer einzigen Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="31acb-162">By default, you run JavaScript code on a single line.</span></span>  <span data-ttu-id="31acb-163">Um eine Zeile auszuführen, geben Sie Ihr JavaScript ein, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="31acb-163">To run a line, type your JavaScript and then select `Enter`.</span></span>  <span data-ttu-id="31acb-164">Um die einzeilige Einschränkung zu umgehen, wählen Sie `Shift` + `Enter` anstelle von `Enter` .</span><span class="sxs-lookup"><span data-stu-id="31acb-164">To work around the single-line limitation, select `Shift`+`Enter` instead of `Enter`.</span></span>  <span data-ttu-id="31acb-165">Wählen Sie, ähnlich wie bei anderen Befehlszeilenfunktionen, die Option aus, um auf Ihre vorherigen JavaScript-Befehle `Arrow-Up` zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="31acb-165">Similar to other command-line experiences, to access your previous JavaScript commands, select `Arrow-Up`.</span></span>  <span data-ttu-id="31acb-166">Das Feature für die automatische Vervollständigung der **Konsole** ist eine hervorragende Möglichkeit, sich mit unbekannten Methoden vertraut zu machen.</span><span class="sxs-lookup"><span data-stu-id="31acb-166">The autocompletion feature of the **Console** is a great way to learn about unfamiliar methods.</span></span>  <span data-ttu-id="31acb-167">Führen Sie die folgenden Aktionen aus, um es zu testen.</span><span class="sxs-lookup"><span data-stu-id="31acb-167">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="31acb-168">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="31acb-168">Open the **Console**.</span></span>  
1.  <span data-ttu-id="31acb-169">Geben Sie `doc` ein.</span><span class="sxs-lookup"><span data-stu-id="31acb-169">Type `doc`.</span></span>  
1.  <span data-ttu-id="31acb-170">Wählen Sie `document` aus dem Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="31acb-170">Choose `document` from the dropdown menu.</span></span>  
1.  <span data-ttu-id="31acb-171">Wählen Sie den `tab` Schlüssel aus, um ihn auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="31acb-171">Select the `tab` key to choose it.</span></span>  
1.  <span data-ttu-id="31acb-172">Geben Sie `.bo` ein.</span><span class="sxs-lookup"><span data-stu-id="31acb-172">Type `.bo`.</span></span>  
1.  <span data-ttu-id="31acb-173">Wählen Sie `tab` aus, um `document.body` .</span><span class="sxs-lookup"><span data-stu-id="31acb-173">Select `tab` to get `document.body`.</span></span>  
1.  <span data-ttu-id="31acb-174">Geben Sie einen anderen Typ `.` ein, um die vollständige Liste der Eigenschaften und Methoden anzuzeigen, die im Textkörper der aktuellen Webseite verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="31acb-174">Type another `.` to display the complete list of properties and methods available on the body of the current webpage.</span></span>  
    
<span data-ttu-id="31acb-175">Weitere Informationen zu allen Möglichkeiten zum Arbeiten mit **der Konsole**finden Sie in der Konsole [als JavaScript-Umgebung.][DevtoolsConsoleConsoleJavascript]</span><span class="sxs-lookup"><span data-stu-id="31acb-175">For more information about all the ways to work with **Console**, navigate to [Console as a JavaScript environment][DevtoolsConsoleConsoleJavascript].</span></span>  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Automatische Konsolenkompletion von JavaScript-Ausdrücken" lightbox="../media/console-javascript-autocomplete.msft.png":::
   <span data-ttu-id="31acb-177">**Automatische Konsolenkompletion** von JavaScript-Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="31acb-177">**Console** autocompletion of JavaScript expressions</span></span>  
:::image-end:::  

## <a name="interact-with-the-current-webpage-in-the-browser"></a><span data-ttu-id="31acb-178">Interagieren mit der aktuellen Webseite im Browser</span><span class="sxs-lookup"><span data-stu-id="31acb-178">Interact with the current webpage in the browser</span></span>  

<span data-ttu-id="31acb-179">Die **Konsole** hat Zugriff auf das [Window-Objekt][MdnDocsWebApiWindow] des Browsers.</span><span class="sxs-lookup"><span data-stu-id="31acb-179">The **Console** has access to the [Window][MdnDocsWebApiWindow] object of the browser.</span></span>  <span data-ttu-id="31acb-180">Sie können Skripts schreiben, die mit der aktuellen Webseite interagieren.</span><span class="sxs-lookup"><span data-stu-id="31acb-180">You can write scripts that interact with the current webpage.</span></span>  <span data-ttu-id="31acb-181">Führen Sie die folgenden Aktionen aus, um es zu testen.</span><span class="sxs-lookup"><span data-stu-id="31acb-181">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="31acb-182">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="31acb-182">Open the **Console**.</span></span>  
1.  <span data-ttu-id="31acb-183">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="31acb-183">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML
    ```  
    
:::image type="complex" source="../media/console-intro-reading-DOM.msft.png" alt-text="Kopieren des Inhalts der oberen Überschrift (h1) aus dem DOM und Anzeigen in der Konsole" lightbox="../media/console-intro-reading-DOM.msft.png":::
   <span data-ttu-id="31acb-185">Kopieren Sie den Inhalt der oberen Überschrift \( `h1` \) aus dem DOM, und zeigen Sie sie in der **Konsole** an.</span><span class="sxs-lookup"><span data-stu-id="31acb-185">Copy the top heading \(`h1`\) content from the DOM and display in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="31acb-186">Anstatt nur von der Webseite zu lesen, können Sie sie auch ändern.</span><span class="sxs-lookup"><span data-stu-id="31acb-186">Instead of only reading from the webpage, you can also change it.</span></span>  <span data-ttu-id="31acb-187">Führen Sie die folgenden Aktionen aus, um zu versuchen, die Webseite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="31acb-187">To try changing the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="31acb-188">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="31acb-188">Open the **Console**.</span></span>  
1.  <span data-ttu-id="31acb-189">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="31acb-189">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML = 'Rocking the Console';
    ```  
    
:::image type="complex" source="../media/console-intro-wrtiting-DOM.msft.png" alt-text="Schreiben von Text in das DOM in der Konsole" lightbox="../media/console-intro-wrtiting-DOM.msft.png":::
   <span data-ttu-id="31acb-191">Schreiben von Text in das DOM in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="31acb-191">Write text to the DOM in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="31acb-192">Sie haben die Hauptüberschrift der Webseite in **"Wackeln der Konsole"** geändert.</span><span class="sxs-lookup"><span data-stu-id="31acb-192">You changed the main heading of the webpage to **Rocking the Console**.</span></span>  <span data-ttu-id="31acb-193">Die **Konsolenhilfsprogrammmethoden** erleichtern den Zugriff auf die aktuelle Webseite und deren Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="31acb-193">The **Console Utility** methods make it easy to access and manipulate the current webpage.</span></span>  <span data-ttu-id="31acb-194">Navigieren Sie für weitere Informationen zur [API-Referenz für Konsolenprogramme.][DevtoolsConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="31acb-194">For more information, navigate to [Console Utilities API reference][DevtoolsConsoleUtilities].</span></span>  <span data-ttu-id="31acb-195">Um beispielsweise einen grünen Rahmen um alle Links auf der aktuellen Webseite hinzuzufügen, führen Sie die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="31acb-195">For example, to add a green border around all the links in the current webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="31acb-196">Öffnen Sie die **Konsole**.</span><span class="sxs-lookup"><span data-stu-id="31acb-196">Open the **Console**.</span></span>  
1.  <span data-ttu-id="31acb-197">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="31acb-197">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    $$('a').forEach(a => a.style.border='1px solid lime');
    ```  
    
:::image type="complex" source="../media/console-intro-changing-styles.msft.png" alt-text="Bearbeiten einer Auswahl von Elementen mithilfe der Konsole" lightbox="../media/console-intro-changing-styles.msft.png":::
    <span data-ttu-id="31acb-199">Bearbeiten einer Auswahl von Elementen mithilfe der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="31acb-199">Manipulate a selection of elements using the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="31acb-200">For more information about working with the DOM, navigate to [Use the Console to interact with the DOM][DevtoolsConsoleConsoleDomInteraction].</span><span class="sxs-lookup"><span data-stu-id="31acb-200">For more information about working with the DOM, navigate to [Use the Console to interact with the DOM][DevtoolsConsoleConsoleDomInteraction].</span></span>  

## <a name="learn-more-about-console"></a><span data-ttu-id="31acb-201">Weitere Informationen zur Konsole</span><span class="sxs-lookup"><span data-stu-id="31acb-201">Learn more about Console</span></span>  

<span data-ttu-id="31acb-202">For more information about the **Console**, navigate to [Console reference][DevtoolsConsoleReference], Console Utilities [API reference][DevtoolsConsoleUtilities], and Console [API reference][DevtoolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="31acb-202">For more information about the **Console**, navigate to [Console reference][DevtoolsConsoleReference], [Console Utilities API reference][DevtoolsConsoleUtilities], and [Console API reference][DevtoolsConsoleApi].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="31acb-203">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="31acb-203">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
