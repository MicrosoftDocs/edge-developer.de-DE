---
description: Hier erfahren Sie, wie Sie Nachrichten in der Konsole protokollieren.
title: Erste Schritte mit der Protokollierung von Nachrichten in der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 96e3ad76fb86e32cf58abe6187fa0d6e75a2c00a
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125272"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="e12d8-104">Erste Schritte mit der Protokollierung von Nachrichten in der Konsole</span><span class="sxs-lookup"><span data-stu-id="e12d8-104">Get Started With Logging Messages In The Console</span></span>  

<span data-ttu-id="e12d8-105">In diesem interaktiven Lernprogramm erfahren Sie, wie Sie Nachrichten in der [Microsoft Edge devtools][MicrosoftEdgeDevTools] -Konsole protokollieren und filtern.</span><span class="sxs-lookup"><span data-stu-id="e12d8-105">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="e12d8-107">Nachrichten in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="e12d8-107">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="e12d8-108">Dieses Lernprogramm soll in der entsprechenden Reihenfolge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e12d8-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="e12d8-109">Es wird davon ausgegangen, dass Sie die Grundlagen der Webentwicklung verstehen, beispielsweise die Verwendung von JavaScript zum Hinzufügen von Interaktivität zu einer Seite.</span><span class="sxs-lookup"><span data-stu-id="e12d8-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="e12d8-110">Einrichten der Demo-und DevTools</span><span class="sxs-lookup"><span data-stu-id="e12d8-110">Set up the demo and DevTools</span></span>  

<span data-ttu-id="e12d8-111">Dieses Lernprogramm ist so konzipiert, dass Sie die Demo öffnen und alle Workflows selbst ausprobieren können.</span><span class="sxs-lookup"><span data-stu-id="e12d8-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="e12d8-112">Wenn Sie physisch miteinander in Verbindung bleiben, können Sie die Workflows später wahrscheinlicher merken.</span><span class="sxs-lookup"><span data-stu-id="e12d8-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="e12d8-113">Halten `Control` Sie \ (Windows, Linux \) oder `Command` \ (macOS \) gedrückt, und wählen Sie **Konsolenprotokoll Beispiele** aus, die auf einer neuen Registerkarte geöffnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e12d8-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="e12d8-114">Beispiele für Konsolen Protokolle</span><span class="sxs-lookup"><span data-stu-id="e12d8-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="e12d8-115">Konzentrieren Sie die Demo, und wählen Sie dann `Control` + `Shift` + `J` \ (Windows, Linux \) oder `Command` + `Option` + `J` \ (macOS \) aus, um devtools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e12d8-115">Focus the demo and then select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="e12d8-116">Standardmäßig wird devtools rechts neben der Demo geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e12d8-116">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="e12d8-118">DevTools wird rechts neben der Demo geöffnet</span><span class="sxs-lookup"><span data-stu-id="e12d8-118">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="e12d8-119">[Docken Sie devtools an den unteren Rand des Fensters an][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="e12d8-119">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="e12d8-121">DevTools angedockt am Ende der Demo</span><span class="sxs-lookup"><span data-stu-id="e12d8-121">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="e12d8-122">[Docken Sie devtools in einem separaten Fenster][DevToolsCustomizePlacement]ab.</span><span class="sxs-lookup"><span data-stu-id="e12d8-122">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="e12d8-124">Browser in einem separaten Fenster</span><span class="sxs-lookup"><span data-stu-id="e12d8-124">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="e12d8-125">[Docken Sie devtools in einem separaten Fenster][DevToolsCustomizePlacement]ab.</span><span class="sxs-lookup"><span data-stu-id="e12d8-125">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="e12d8-127">DevTools Abdocken in einem separaten Fenster</span><span class="sxs-lookup"><span data-stu-id="e12d8-127">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="e12d8-128">Anzeigen von Nachrichten, die von JavaScript protokolliert wurden</span><span class="sxs-lookup"><span data-stu-id="e12d8-128">View messages logged from JavaScript</span></span>  

<span data-ttu-id="e12d8-129">Die meisten Nachrichten, die Sie in der Konsole sehen, stammen von den Web-Entwicklern, die das JavaScript der Seite verfasst haben.</span><span class="sxs-lookup"><span data-stu-id="e12d8-129">Most messages that you see in the Console come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="e12d8-130">In diesem Abschnitt möchten wir Ihnen die verschiedenen Nachrichtentypen vorstellen, die Sie wahrscheinlich in der Konsole sehen werden, und erläutern, wie Sie die einzelnen Nachrichtentypen selbst aus Ihrem eigenen JavaScript-Protokoll aufzeichnen können.</span><span class="sxs-lookup"><span data-stu-id="e12d8-130">The goal of this section is to introduce you to the different message types that you are likely to see in the Console, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="e12d8-131">Klicken Sie in der Demo auf die Schaltfläche **Log-Informationen** .</span><span class="sxs-lookup"><span data-stu-id="e12d8-131">Click the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="e12d8-132">wird in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="e12d8-132">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="e12d8-134">Die **Konsole** nach dem Klicken auf " **Protokollinformationen** "</span><span class="sxs-lookup"><span data-stu-id="e12d8-134">The **Console** after clicking **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-135">`Hello, Console!`Wählen Sie neben der Nachricht in der Konsole **log.js:2**aus.</span><span class="sxs-lookup"><span data-stu-id="e12d8-135">Next to the `Hello, Console!` message in the Console choose **log.js:2**.</span></span>  <span data-ttu-id="e12d8-136">Das Fenster "Quellen" wird geöffnet, und die Codezeile wird hervorgehoben, die dazu geführt hat, dass die Nachricht in der Konsole protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="e12d8-136">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="e12d8-137">Die Nachricht wurde protokolliert, als das JavaScript der Seite ausgeführt wurde `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="e12d8-137">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="e12d8-139">DevTools öffnet das **Quellen** Panel, nachdem Sie auf</span><span class="sxs-lookup"><span data-stu-id="e12d8-139">DevTools opens the **Sources** panel after you click</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-140">Navigieren Sie mit einem der folgenden Workflows zurück zur **Konsole** :</span><span class="sxs-lookup"><span data-stu-id="e12d8-140">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="e12d8-141">Klicken Sie auf die Registerkarte **Konsole** .</span><span class="sxs-lookup"><span data-stu-id="e12d8-141">Click the **Console** tab.</span></span>  
    *   <span data-ttu-id="e12d8-142">Wählen Sie `Control` + `[` \ (Windows, Linux \) oder `Command` + `[` \ (macOS \) aus, bis das Konsolenfenster den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="e12d8-142">Select `Control`+`[` \(Windows, Linux\) or `Command`+`[` \(macOS\) until the Console panel is in focus.</span></span>  
    *   <span data-ttu-id="e12d8-143">[Öffnen Sie das Menübefehl][DevToolsCommandMenu], beginnen `Console` Sie mit der Eingabe, wählen Sie den Befehl **Konsolen Panel anzeigen** aus, und wählen Sie dann aus `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e12d8-143">[Open the Command Menu][DevToolsCommandMenu], start typing `Console`, select the **Show Console Panel** command, and then select `Enter`.</span></span>  
    
1.  <span data-ttu-id="e12d8-144">Klicken Sie in der Demo auf die Schaltfläche **Warnungsprotokoll** .</span><span class="sxs-lookup"><span data-stu-id="e12d8-144">Click the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="e12d8-145">wird in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="e12d8-145">gets logged to the Console.</span></span>  <span data-ttu-id="e12d8-146">So formatierte Nachrichten sind Warnungen.</span><span class="sxs-lookup"><span data-stu-id="e12d8-146">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="e12d8-148">Die **Konsole** nach Auswahl der Option " **Protokoll Warnung** "</span><span class="sxs-lookup"><span data-stu-id="e12d8-148">The **Console** after you choose **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="e12d8-149">Wenn Sie den Code anzeigen möchten, der dazu geführt hat, dass eine Nachricht protokolliert wird, klicken Sie auf ein Skript \ (beispielsweise `log.js:12` \), um den Code anzuzeigen, der dazu geführt hat, dass die Nachricht formatiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e12d8-149">If you want to see the code that caused a message to get logged a certain way, click on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="e12d8-150">Klicken Sie auf das Symbol **erweitern** \ ( ![ Erweitern ][ImageExpandIcon] \) vor `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="e12d8-150">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="e12d8-151">DevTools zeigt die [Stapelüberwachung][WikiStackTrace] an, die zum Aufruf führt.</span><span class="sxs-lookup"><span data-stu-id="e12d8-151">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="e12d8-153">Eine Stapelüberwachung</span><span class="sxs-lookup"><span data-stu-id="e12d8-153">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e12d8-154">In der Stapelüberwachung wird Ihnen mitgeteilt, dass eine Funktion namens `logWarning` aufgerufen wurde, die wiederum eine Funktion mit dem Namen genannt wird `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="e12d8-154">The stack trace is telling you that a function named `logWarning` was called, which in turn called a function named `quoteDante`.</span></span>  <span data-ttu-id="e12d8-155">Anders ausgedrückt: der Aufruf, der sich zuerst ereignet hat, befindet sich am Ende der Stapelüberwachung.</span><span class="sxs-lookup"><span data-stu-id="e12d8-155">In other words, the call that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="e12d8-156">Sie können Stack-Ablaufverfolgungen jederzeit durch Aufrufen protokollieren `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="e12d8-156">You may log stack traces at any time by calling `console.trace()`.</span></span>  

1.  <span data-ttu-id="e12d8-157">Wählen Sie **Protokollfehler**aus.</span><span class="sxs-lookup"><span data-stu-id="e12d8-157">Choose **Log Error**.</span></span>  <span data-ttu-id="e12d8-158">Die folgende Fehlermeldung wird protokolliert:</span><span class="sxs-lookup"><span data-stu-id="e12d8-158">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="e12d8-160">Eine Fehlermeldung</span><span class="sxs-lookup"><span data-stu-id="e12d8-160">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-161">Wählen Sie **Protokolltabelle**aus.</span><span class="sxs-lookup"><span data-stu-id="e12d8-161">Choose **Log Table**.</span></span>  <span data-ttu-id="e12d8-162">Eine Tabelle über berühmte Interpreten wird an der Konsole angemeldet.</span><span class="sxs-lookup"><span data-stu-id="e12d8-162">A table about famous artists gets logged to the Console.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e12d8-163">Die `birthday` Spalte wird nur für eine Zeile ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="e12d8-163">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="e12d8-164">Überprüfen Sie den Code, um zu ermitteln, warum dies der Grund ist.</span><span class="sxs-lookup"><span data-stu-id="e12d8-164">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="e12d8-166">Eine Tabelle in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="e12d8-166">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-167">Wählen Sie **Protokollgruppe**aus.</span><span class="sxs-lookup"><span data-stu-id="e12d8-167">Choose **Log Group**.</span></span>  <span data-ttu-id="e12d8-168">Unter dem Label sind die Namen von vier berühmten, kriminalisch bekämpften Schildkröten gruppiert `Adolescent Irradiated Espionage Tortoises` .</span><span class="sxs-lookup"><span data-stu-id="e12d8-168">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="e12d8-170">Eine Gruppe von Nachrichten in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="e12d8-170">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-171">Wählen Sie **Protokoll Benutzerdefiniert**aus.</span><span class="sxs-lookup"><span data-stu-id="e12d8-171">Choose **Log Custom**.</span></span>  <span data-ttu-id="e12d8-172">Eine Nachricht mit rotem Rahmen und blauem Hintergrund wird in der Konsole protokolliert.</span><span class="sxs-lookup"><span data-stu-id="e12d8-172">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="e12d8-174">Eine Nachricht mit benutzerdefinierter Formatierung in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="e12d8-174">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e12d8-175">Der Grundgedanke hierbei ist, dass Sie eine der Methoden verwenden, wenn Sie Nachrichten von Ihrem JavaScript-Konto in der Konsole protokollieren möchten `console` .</span><span class="sxs-lookup"><span data-stu-id="e12d8-175">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="e12d8-176">Jede Methode formatiert Nachrichten unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="e12d8-176">Each method formats messages differently.</span></span>  

<span data-ttu-id="e12d8-177">Es gibt noch mehr Methoden als das, was in diesem Abschnitt gezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="e12d8-177">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="e12d8-178">In diesem Lernprogramm erfahren Sie, wie Sie die restlichen Methoden erkunden.</span><span class="sxs-lookup"><span data-stu-id="e12d8-178">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="e12d8-179">Anzeigen von vom Browser protokollierten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e12d8-179">View messages logged by the browser</span></span>  

<span data-ttu-id="e12d8-180">Der Browser protokolliert auch Nachrichten an der Konsole.</span><span class="sxs-lookup"><span data-stu-id="e12d8-180">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="e12d8-181">Dies geschieht in der Regel, wenn ein Problem mit der Seite vorliegt.</span><span class="sxs-lookup"><span data-stu-id="e12d8-181">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="e12d8-182">Wählen Sie **Ursache 404**aus.</span><span class="sxs-lookup"><span data-stu-id="e12d8-182">Choose **Cause 404**.</span></span>  <span data-ttu-id="e12d8-183">Der Browser protokolliert einen HTTP-Statuscode des `404` Netzwerkfehlers, weil das JavaScript der Seite versucht hat, eine Datei abzurufen, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e12d8-183">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="e12d8-185">`404`Fehler in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="e12d8-185">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-186">Wählen Sie **Fehlerursache**aus.</span><span class="sxs-lookup"><span data-stu-id="e12d8-186">Choose **Cause Error**.</span></span>  <span data-ttu-id="e12d8-187">Der Browser protokolliert eine nicht abgefangene `TypeError` , da JavaScript versucht, einen nicht vorhandenen DOM-Knoten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e12d8-187">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="e12d8-189">A `TypeError` in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="e12d8-189">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-190">Klicken Sie auf die Dropdownliste **Protokollebenen** , und aktivieren Sie die Option **verbose** , wenn Sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e12d8-190">Click the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="e12d8-191">Weitere Informationen zum Filtern finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="e12d8-191">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="e12d8-192">Sie müssen dies tun, um sicherzustellen, dass die nächste Nachricht, die Sie protokollieren, sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="e12d8-192">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e12d8-193">Wenn die Dropdownliste Standardebenen deaktiviert ist, müssen Sie möglicherweise die Sidebar der **Konsole** schließen.</span><span class="sxs-lookup"><span data-stu-id="e12d8-193">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="e12d8-194">Filtern nach Nachrichtenquelle unten, um weitere Informationen zur Sidebar der **Konsole** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e12d8-194">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="e12d8-196">Aktivieren der ausführlichen Protokollebene</span><span class="sxs-lookup"><span data-stu-id="e12d8-196">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-197">Wählen Sie **Ursache Verletzung**aus.</span><span class="sxs-lookup"><span data-stu-id="e12d8-197">Choose **Cause Violation**.</span></span>  <span data-ttu-id="e12d8-198">Die Seite reagiert für ein paar Sekunden nicht mehr, und dann protokolliert der Browser die Nachricht `[Violation] 'click' handler took 3000ms` auf der Konsole.</span><span class="sxs-lookup"><span data-stu-id="e12d8-198">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="e12d8-199">Die genaue Dauer kann variieren.</span><span class="sxs-lookup"><span data-stu-id="e12d8-199">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="e12d8-201">Eine Verletzung in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="e12d8-201">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e12d8-202">Filtern von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e12d8-202">Filter messages</span></span>  

<span data-ttu-id="e12d8-203">Auf einigen Seiten wird die Konsole mit Nachrichten überschwemmt.</span><span class="sxs-lookup"><span data-stu-id="e12d8-203">On some pages you see the Console get flooded with messages.</span></span>  <span data-ttu-id="e12d8-204">DevTools bietet viele verschiedene Methoden zum Filtern von Nachrichten, die für die jeweilige Aufgabe nicht relevant sind.</span><span class="sxs-lookup"><span data-stu-id="e12d8-204">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="e12d8-205">Nach Protokollebene Filtern</span><span class="sxs-lookup"><span data-stu-id="e12d8-205">Filter by log level</span></span>  

<span data-ttu-id="e12d8-206">Jeder `console` Methode wird ein Schweregrad zugewiesen: `Verbose` , `Info` , `Warning` , oder `Error` .</span><span class="sxs-lookup"><span data-stu-id="e12d8-206">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="e12d8-207">Beispielsweise `console.log()` ist eine Nachricht auf einer `Info` Ebene, während `console.error()` die Nachricht auf eine `Error` Ebene lautet.</span><span class="sxs-lookup"><span data-stu-id="e12d8-207">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="e12d8-208">Klicken Sie auf die Dropdownliste **Protokollebenen** , und deaktivieren Sie **Fehler**.</span><span class="sxs-lookup"><span data-stu-id="e12d8-208">Click the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="e12d8-209">Eine Ebene ist deaktiviert, wenn daneben kein Häkchen mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e12d8-209">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="e12d8-210">Die `Error` Nachrichten auf der Ebene verschwinden.</span><span class="sxs-lookup"><span data-stu-id="e12d8-210">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="e12d8-212">Deaktivieren von Nachrichten auf Fehlerebene in der **Konsole**</span><span class="sxs-lookup"><span data-stu-id="e12d8-212">Disabling Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-213">Klicken Sie erneut auf die Dropdownliste **Protokollebenen** , und aktivieren Sie dann **Fehler**erneut.</span><span class="sxs-lookup"><span data-stu-id="e12d8-213">Click the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="e12d8-214">Die `Error` Nachrichten auf der Ebene werden erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e12d8-214">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="e12d8-215">Filtern nach Text</span><span class="sxs-lookup"><span data-stu-id="e12d8-215">Filter by text</span></span>  

<span data-ttu-id="e12d8-216">Wenn Sie nur Nachrichten anzeigen möchten, die eine exakte Zeichenfolge enthalten, geben Sie diese Zeichenfolge in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="e12d8-216">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="e12d8-217">Geben Sie `Dave` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="e12d8-217">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="e12d8-218">Alle Nachrichten, die die Zeichenfolge nicht enthalten, `Dave` werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="e12d8-218">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="e12d8-219">Möglicherweise wird auch die `Adolescent Irradiated Espionage Tortoises` Beschriftung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e12d8-219">You might also see the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="e12d8-220">Das ist ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="e12d8-220">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="e12d8-222">Filtern von Nachrichten, die nicht enthalten sind</span><span class="sxs-lookup"><span data-stu-id="e12d8-222">Filtering out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-223">Löschen `Dave` aus dem Textfeld " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="e12d8-223">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="e12d8-224">Alle Nachrichten werden wieder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e12d8-224">All the messages reappear.</span></span>  

### <span data-ttu-id="e12d8-225">Nach regulärem Ausdruck filtern</span><span class="sxs-lookup"><span data-stu-id="e12d8-225">Filter by regular expression</span></span>  

<span data-ttu-id="e12d8-226">Wenn Sie alle Nachrichten anzeigen möchten, die anstelle einer bestimmten Zeichenfolge ein Textmuster enthalten, verwenden Sie einen [regulären Ausdruck][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="e12d8-226">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="e12d8-227">Geben Sie `/^[AH]/` in das Textfeld **Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="e12d8-227">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="e12d8-228">Geben Sie dieses Muster in [regexr][|::ref1::|Main] ein, um zu erläutern, was es tut.</span><span class="sxs-lookup"><span data-stu-id="e12d8-228">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="e12d8-230">Filtern von Nachrichten, die nicht dem Muster entsprechen</span><span class="sxs-lookup"><span data-stu-id="e12d8-230">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-231">Löschen `/^[AH]/` aus dem Textfeld " **Filter** "</span><span class="sxs-lookup"><span data-stu-id="e12d8-231">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="e12d8-232">Alle Nachrichten sind wieder sichtbar.</span><span class="sxs-lookup"><span data-stu-id="e12d8-232">All messages are visible again.</span></span>  

### <span data-ttu-id="e12d8-233">Nach Nachrichtenquelle Filtern</span><span class="sxs-lookup"><span data-stu-id="e12d8-233">Filter by message source</span></span>  

<span data-ttu-id="e12d8-234">Wenn Sie nur die Nachrichten anzeigen möchten, die von einer bestimmten URL stammen, verwenden Sie die **Seitenleiste**.</span><span class="sxs-lookup"><span data-stu-id="e12d8-234">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="e12d8-235">Wählen Sie **Console Sidebar anzeigen** \ ( ![ Konsolen-Sidebar anzeigen ][ImageShowConsoleSidebarIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="e12d8-235">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="e12d8-237">Die Seitenleiste</span><span class="sxs-lookup"><span data-stu-id="e12d8-237">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-238">Klicken Sie auf das Symbol **erweitern** \ ( ![ Erweitern ][ImageExpandIcon] \) neben der Anzahl der Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="e12d8-238">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon next to the number of messages.</span></span>  <span data-ttu-id="e12d8-239">In der folgenden Abbildung wird die Anzahl der Nachrichten als **13 Nachrichten**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e12d8-239">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="e12d8-240">Die **Seitenleiste** zeigt eine Liste der URLs, die dazu geführt haben, dass Nachrichten protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="e12d8-240">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="e12d8-241">Beispielsweise `log.js` verursachte 11 Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="e12d8-241">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="e12d8-243">Anzeigen der Quelle von Nachrichten in der Seitenleiste</span><span class="sxs-lookup"><span data-stu-id="e12d8-243">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e12d8-244">Nach Benutzer Nachrichten filtern</span><span class="sxs-lookup"><span data-stu-id="e12d8-244">Filter by user messages</span></span>  

<span data-ttu-id="e12d8-245">Wenn Sie zuvor auf **Protokollinformationen**geklickt haben, wurde ein Skript aufgerufen, um `console.log('Hello, Console!')` die Nachricht in der Konsole zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="e12d8-245">Earlier, when you clicked **Log Info**, a script called `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="e12d8-246">Nachrichten, die von JavaScript wie diesem protokolliert werden, werden als **Benutzer Nachrichten**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e12d8-246">Messages logged from JavaScript like this are called **user messages**.</span></span>  <span data-ttu-id="e12d8-247">Wenn Sie hingegen auf **Ursache 404**geklickt haben, hat der Browser die Meldung auf eine Ebene protokolliert, `Error` die besagt, dass die angeforderte Ressource nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="e12d8-247">In contrast, when you clicked **Cause 404**, the browser logged an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="e12d8-248">Nachrichten wie diese werden als **Browser Nachrichten**angesehen.</span><span class="sxs-lookup"><span data-stu-id="e12d8-248">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="e12d8-249">Verwenden Sie die **Seitenleiste** , um Browser Nachrichten zu filtern und nur Benutzer Nachrichten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e12d8-249">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="e12d8-250">Wählen Sie **9 Benutzer Nachrichten**aus.</span><span class="sxs-lookup"><span data-stu-id="e12d8-250">Choose **9 User Messages**.</span></span>  <span data-ttu-id="e12d8-251">Die Browser Nachrichten werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="e12d8-251">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="e12d8-253">Filtern von Browser Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e12d8-253">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e12d8-254">Wählen Sie **13 Nachrichten** aus, um alle Nachrichten erneut anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e12d8-254">Choose **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="e12d8-255">Verwenden der Konsole neben einem anderen Panel</span><span class="sxs-lookup"><span data-stu-id="e12d8-255">Use the Console alongside any other panel</span></span>  

<span data-ttu-id="e12d8-256">Was passiert, wenn Sie Formatvorlagen bearbeiten, aber Sie müssen das Konsolenprotokoll schnell auf etwas überprüfen?</span><span class="sxs-lookup"><span data-stu-id="e12d8-256">What if you are editing styles, but you need to quickly check the Console log for something?</span></span>  <span data-ttu-id="e12d8-257">Verwenden Sie die Schublade.</span><span class="sxs-lookup"><span data-stu-id="e12d8-257">Use the Drawer.</span></span>  

1.  <span data-ttu-id="e12d8-258">Klicken Sie auf die Registerkarte **Elemente** .</span><span class="sxs-lookup"><span data-stu-id="e12d8-258">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="e12d8-259">Wählen Sie aus `Escape` .</span><span class="sxs-lookup"><span data-stu-id="e12d8-259">Select `Escape`.</span></span>  <span data-ttu-id="e12d8-260">Die Registerkarte " **Konsole** " des **Fachs** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e12d8-260">The **Console** tab of the **Drawer** opens.</span></span>  <span data-ttu-id="e12d8-261">Es enthält alle Features des Konsolen Panels, die Sie in diesem Lernprogramm verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="e12d8-261">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Nachrichten in der Konsole" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="e12d8-263">Die Registerkarte ' **Konsole** ' im **Einzug**</span><span class="sxs-lookup"><span data-stu-id="e12d8-263">The **Console** tab in the **Drawer**</span></span>  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

## <span data-ttu-id="e12d8-264">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="e12d8-264">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge \ (Chrom \) Developer Tools | Microsoft docs"  
[DevToolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools | Microsoft docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Ändern der Position von Microsoft Edge devtools | Microsoft docs"  
[DevToolsConsoleApi]: ./api.md "Konsolen-API-Referenz | Microsoft docs"  
[DevToolsConsoleReference]: ./reference.md "Konsolen Referenz | Microsoft docs"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Erste Schritte mit der Protokollierung von Nachrichten | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Reguläre Ausdrücke | MDN"  

[RegExrMain]: https://regexr.com "Regexr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Stack-Trace – Wikipedia"  
> [!NOTE]
> <span data-ttu-id="e12d8-274">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e12d8-274">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e12d8-275">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/console/log) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e12d8-275">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="e12d8-277">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e12d8-277">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
