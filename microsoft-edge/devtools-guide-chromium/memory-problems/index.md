---
description: Erfahren Sie, wie Sie Microsoft Edge und DevTools verwenden, um Speicherprobleme zu finden, die sich auf die Seitenleistung auswirken, wie Speicherverluste, aufblasen des Arbeitsspeichers und häufige Garbage Collections.
title: Beheben von Speicherproblemen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ef820353f81eb3fd791433e9c53434dff3b10a60
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992778"
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

# <span data-ttu-id="86051-104">Beheben von Speicherproblemen</span><span class="sxs-lookup"><span data-stu-id="86051-104">Fix Memory Problems</span></span>  

<span data-ttu-id="86051-105">Erfahren Sie, wie Sie Microsoft Edge und DevTools verwenden, um Speicherprobleme zu finden, die sich auf die Seitenleistung auswirken, wie Speicherverluste, aufblasen des Arbeitsspeichers und häufige Garbage Collections.</span><span class="sxs-lookup"><span data-stu-id="86051-105">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <span data-ttu-id="86051-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="86051-106">Summary</span></span>  

*   <span data-ttu-id="86051-107">Finden Sie heraus, wie viel Arbeitsspeicher Ihre Seite zurzeit mit dem Task-Manager von Microsoft Edge-Browser verwendet.</span><span class="sxs-lookup"><span data-stu-id="86051-107">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="86051-108">Visualisieren Sie die Speichernutzung im Zeitverlauf mit dem **Speicher** Panel.</span><span class="sxs-lookup"><span data-stu-id="86051-108">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="86051-109">Identifizieren Sie freigegebene Dom-Bäume \ (eine häufige Ursache für Speicherverluste \) mit **Heap-Snapshots**.</span><span class="sxs-lookup"><span data-stu-id="86051-109">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="86051-110">Informieren Sie sich, wann der neue Arbeitsspeicher in Ihrem JavaScript-Heap \ (JS-Heap \) mit **Zuordnungs Instrumentation auf Zeitachse**zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="86051-110">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <span data-ttu-id="86051-111">Übersicht</span><span class="sxs-lookup"><span data-stu-id="86051-111">Overview</span></span>  

<span data-ttu-id="86051-112">Im Sinne des **Rail** -Leistungsmodells sollten Ihre Benutzer den Schwerpunkt ihrer Leistungs Bemühungen haben.</span><span class="sxs-lookup"><span data-stu-id="86051-112">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="86051-113">Speicherprobleme sind wichtig, da Sie für die Benutzer oft wahrnehmbar sind.</span><span class="sxs-lookup"><span data-stu-id="86051-113">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="86051-114">Benutzer können Speicherprobleme wie folgt erkennen:</span><span class="sxs-lookup"><span data-stu-id="86051-114">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="86051-115">**Die Leistung einer Seite wird im Laufe der Zeit zunehmend schlechter**.</span><span class="sxs-lookup"><span data-stu-id="86051-115">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="86051-116">Dies ist möglicherweise ein Symptom für einen Speicherverlust.</span><span class="sxs-lookup"><span data-stu-id="86051-116">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="86051-117">Ein Speicherverlust ist, wenn ein Fehler auf der Seite dazu führt, dass die Seite zunehmend mehr und mehr Arbeitsspeicher im Laufe der Zeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="86051-117">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="86051-118">**Die Leistung einer Seite ist durchwegs schlecht**.</span><span class="sxs-lookup"><span data-stu-id="86051-118">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="86051-119">Dies ist möglicherweise ein Symptom des Aufblasens des Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="86051-119">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="86051-120">Der Arbeitsspeicher wird aufgebläht, wenn eine Seite mehr Arbeitsspeicher benötigt, als für optimale Seiten Geschwindigkeit erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="86051-120">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="86051-121">**Die Leistung einer Seite wird verzögert oder wird häufig angehalten**.</span><span class="sxs-lookup"><span data-stu-id="86051-121">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="86051-122">Dies ist möglicherweise ein Symptom häufiger Garbage Collections.</span><span class="sxs-lookup"><span data-stu-id="86051-122">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="86051-123">Die Garbage Collection ist der Fall, wenn der Browser Speicher aufhebt.</span><span class="sxs-lookup"><span data-stu-id="86051-123">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="86051-124">Der Browser entscheidet, wann dies geschieht.</span><span class="sxs-lookup"><span data-stu-id="86051-124">The browser decides when this happens.</span></span>  <span data-ttu-id="86051-125">Während Auflistungen wird alle ausgeführten Skripts angehalten.</span><span class="sxs-lookup"><span data-stu-id="86051-125">During collections, all script running is paused.</span></span>  <span data-ttu-id="86051-126">Wenn der Browser also viel Garbage Collection durchläuft, wird die Skriptlaufzeit viel angehalten.</span><span class="sxs-lookup"><span data-stu-id="86051-126">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <span data-ttu-id="86051-127">Speicher aufblasen: wie viel ist "zu viel"?</span><span class="sxs-lookup"><span data-stu-id="86051-127">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="86051-128">Ein Speicherverlust ist einfach zu definieren.</span><span class="sxs-lookup"><span data-stu-id="86051-128">A memory leak is easy to define.</span></span>  <span data-ttu-id="86051-129">Wenn eine Website zunehmend mehr und mehr Arbeitsspeicher verwendet, liegt ein Leck vor.</span><span class="sxs-lookup"><span data-stu-id="86051-129">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="86051-130">Aber der Speicher aufblasen ist etwas schwieriger zu anheften.</span><span class="sxs-lookup"><span data-stu-id="86051-130">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="86051-131">Was qualifiziert als "Verwenden von zu viel Arbeitsspeicher"?</span><span class="sxs-lookup"><span data-stu-id="86051-131">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="86051-132">Hier gibt es keine harten Zahlen, da unterschiedliche Geräte und Browser unterschiedliche Funktionen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="86051-132">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="86051-133">Die gleiche Seite, die auf einem Highend-Smartphone problemlos läuft, kann auf einem Low-End-Smartphone abstürzen.</span><span class="sxs-lookup"><span data-stu-id="86051-133">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="86051-134">Der Schlüssel besteht darin, das Schienen Modell zu verwenden und sich auf die Benutzer zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="86051-134">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="86051-135">Finden Sie heraus, welche Geräte für Ihre Benutzer beliebt sind, und testen Sie dann Ihre Seite auf diesen Geräten.</span><span class="sxs-lookup"><span data-stu-id="86051-135">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="86051-136">Wenn die Erfahrung durchweg fehlerhaft ist, kann die Seite die Speicherfunktionen dieser Geräte überschreiten.</span><span class="sxs-lookup"><span data-stu-id="86051-136">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <span data-ttu-id="86051-137">Überwachen der Speichernutzung in Echtzeit mit dem Microsoft Edge-Browser-Task-Manager</span><span class="sxs-lookup"><span data-stu-id="86051-137">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="86051-138">Verwenden Sie den Microsoft Edge-Browser-Task-Manager als Ausgangspunkt für die Untersuchung des Speicherproblems.</span><span class="sxs-lookup"><span data-stu-id="86051-138">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="86051-139">Der Microsoft Edge-Browser-Task-Manager ist ein Echtzeitmonitor, der Ihnen mitteilt, wie viel Arbeitsspeicher eine Seite zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="86051-139">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="86051-140">Drücken `Shift` + `Esc` oder wechseln Sie zum Hauptmenü von Microsoft Edge, und wählen Sie **Weitere Tools**  >  **Browser Task-Manager** aus, um den Task-Manager von Microsoft Edge-Browser zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="86051-140">Press `Shift`+`Esc` or go to the Microsoft Edge main menu and select **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       <span data-ttu-id="86051-142">Abbildung 1: Öffnen des Microsoft Edge-Browser-Task-Managers</span><span class="sxs-lookup"><span data-stu-id="86051-142">Figure 1:  Opening the Microsoft Edge Browser Task Manager</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="86051-143">Zeigen Sie auf die Tabellenüberschrift des Microsoft Edge-Browser-Task-Managers, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und aktivieren Sie den **JavaScript-Speicher**.</span><span class="sxs-lookup"><span data-stu-id="86051-143">Hover on the table header of the Microsoft Edge Browser Task Manager, open the contextual menu \(right-click\), and enable **JavaScript memory**.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       <span data-ttu-id="86051-145">Abbildung 2: Aktivieren des JavaScript-Speichers</span><span class="sxs-lookup"><span data-stu-id="86051-145">Figure 2:  Enable JavaScript memory</span></span>  
    :::image-end:::  
    
<span data-ttu-id="86051-146">Diese beiden Spalten geben Ihnen unterschiedliche Informationen dazu, wie Ihre Seite den Arbeitsspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="86051-146">These two columns tell you different things about how your page is using memory.</span></span>  

*   <span data-ttu-id="86051-147">Die **Speicher** Spalte stellt den systemeigenen Speicher dar.</span><span class="sxs-lookup"><span data-stu-id="86051-147">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="86051-148">DOM-Knoten werden im systemeigenen Speicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="86051-148">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="86051-149">Wenn dieser Wert immer größer wird, werden DOM-Knoten erstellt.</span><span class="sxs-lookup"><span data-stu-id="86051-149">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="86051-150">Die **JavaScript-Speicher** Spalte stellt den js-Heap dar.</span><span class="sxs-lookup"><span data-stu-id="86051-150">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="86051-151">Diese Spalte enthält zwei Werte.</span><span class="sxs-lookup"><span data-stu-id="86051-151">This column contains two values.</span></span>  <span data-ttu-id="86051-152">Der Wert, an dem Sie interessiert sind, ist die Live-Nummer \ (die Zahl in Klammern \).</span><span class="sxs-lookup"><span data-stu-id="86051-152">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="86051-153">Die Live-Nummer gibt an, wie viel Arbeitsspeicher die erreichbaren Objekte auf der Seite verwenden.</span><span class="sxs-lookup"><span data-stu-id="86051-153">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="86051-154">Wenn diese Zahl zunimmt, werden entweder neue Objekte erstellt, oder die vorhandenen Objekte werden größer.</span><span class="sxs-lookup"><span data-stu-id="86051-154">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <span data-ttu-id="86051-155">Visualisieren von Speicherverlusten mithilfe des Leistungs Panels</span><span class="sxs-lookup"><span data-stu-id="86051-155">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="86051-156">Sie können das Leistungs Panel auch als weiteren Ausgangspunkt ihrer Untersuchung verwenden.</span><span class="sxs-lookup"><span data-stu-id="86051-156">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="86051-157">Der Leistungs Panel hilft Ihnen, die Speichernutzung einer Seite im Laufe der Zeit zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="86051-157">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="86051-158">Öffnen Sie in devtools das Panel **Leistung** .</span><span class="sxs-lookup"><span data-stu-id="86051-158">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="86051-159">Aktivieren Sie das Kontrollkästchen **Speicher** .</span><span class="sxs-lookup"><span data-stu-id="86051-159">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="86051-160">[Führen Sie eine Aufzeichnung][DevtoolsEvaluatePerformanceReferenceRecord]aus.</span><span class="sxs-lookup"><span data-stu-id="86051-160">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="86051-161">Es empfiehlt sich, die Aufzeichnung mit einer erzwungenen Garbage Collection zu starten und zu beenden.</span><span class="sxs-lookup"><span data-stu-id="86051-161">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="86051-162">Wählen Sie **collect garbage** ![ beim Aufzeichnen die Garbage Collection ][ImageForceGarbageCollectionIcon] -Schaltfläche "Garbage Force sammeln" aus, um die Garbage Collection zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="86051-162">Select the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording to force garbage collection.</span></span>  

<span data-ttu-id="86051-163">Wenn Sie Speicher Aufzeichnungen demonstrieren möchten, sollten Sie den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="86051-163">To demonstrate memory recordings, consider the code below:</span></span>  

```javascript
var x = [];
function grow() {
    for (var i = 0; i < 10000; i++) {
        document.body.appendChild(document.createElement('div'));
    }
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="86051-164">Jedes Mal, wenn die Schaltfläche, auf die im Code verwiesen wird, gedrückt wird, werden 10000- `div` Knoten an den Dokument Text angefügt, und eine Zeichenfolge mit 1 Million `x` Zeichen wird auf das `x` Array verschoben.</span><span class="sxs-lookup"><span data-stu-id="86051-164">Every time that the button referenced in the code is pressed, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="86051-165">Beim Ausführen des vorherigen Codebeispiels wird eine Aufzeichnung im **Leistungs** Panel wie in der folgenden Abbildung erstellt.</span><span class="sxs-lookup"><span data-stu-id="86051-165">Running the previous code sample produces a recording in the **Performance** panel like the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   <span data-ttu-id="86051-167">Abbildung 3: einfaches Wachstum</span><span class="sxs-lookup"><span data-stu-id="86051-167">Figure 3:  Simple growth</span></span>  
:::image-end:::  

<span data-ttu-id="86051-168">Zunächst eine Erläuterung der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="86051-168">First, an explanation of the user interface.</span></span>  <span data-ttu-id="86051-169">Das **Heap** Diagramm im Übersichts \**Bereich \** (unter **net**\) stellt den js-Heap dar.</span><span class="sxs-lookup"><span data-stu-id="86051-169">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="86051-170">Unter dem Übersichtsbereich befindet sich **der Bereich** **Zähler** .</span><span class="sxs-lookup"><span data-stu-id="86051-170">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="86051-171">Hier können **Sie die Speicher** Auslastung nach js-Heap (wie **Heap** Diagramm im Übersichtsbereich \), Dokumente, DOM-Knoten, Listener und GPU-Speicher unterteilt sehen.</span><span class="sxs-lookup"><span data-stu-id="86051-171">Here you are able to see memory usage broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="86051-172">Wenn Sie ein Kontrollkästchen deaktivieren, wird es aus dem Diagramm ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="86051-172">Disabling a checkbox hides it from the graph.</span></span>  

<span data-ttu-id="86051-173">Nun eine Analyse des Codes im Vergleich zur vorherigen Zahl.</span><span class="sxs-lookup"><span data-stu-id="86051-173">Now, an analysis of the code compared with the previous figure.</span></span>  <span data-ttu-id="86051-174">Wenn Sie sich den Knoten Zähler \ (das grüne Diagramm \) ansehen, können Sie sehen, dass er mit dem Code sauber übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="86051-174">If you look at the node counter \(the green graph\) you are able to see that it matches up cleanly with the code.</span></span>  <span data-ttu-id="86051-175">Die Anzahl der Knoten nimmt in diskreten Schritten zu.</span><span class="sxs-lookup"><span data-stu-id="86051-175">The node count increases in discrete steps.</span></span>  <span data-ttu-id="86051-176">Sie können davon ausgehen, dass jede Erhöhung der Knotenanzahl ein Aufruf von ist `grow()` .</span><span class="sxs-lookup"><span data-stu-id="86051-176">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="86051-177">Das js-Heap Diagramm \ (das blaue Diagramm \) ist nicht so einfach.</span><span class="sxs-lookup"><span data-stu-id="86051-177">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="86051-178">In Übereinstimmung mit den bewährten Methoden ist der erste DIP eine erzwungene Garbage Collection \ (erreicht durch **collect garbage** Drücken der ![ Schaltfläche Garbage Force Garbage Collection sammeln ][ImageForceGarbageCollectionIcon] ).</span><span class="sxs-lookup"><span data-stu-id="86051-178">In keeping with best practices, the first dip is actually a forced garbage collection \(achieved by pressing the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="86051-179">Während die Aufzeichnung fortschreitet, können Sie sehen, dass die JS-Heapgröße Spikes.</span><span class="sxs-lookup"><span data-stu-id="86051-179">As the recording progresses you are able to see that the JS heap size spikes.</span></span>  <span data-ttu-id="86051-180">Dies ist natürlich und erwartet: der JavaScript-Code erstellt die DOM-Knoten auf jeder Schaltfläche und macht viel Arbeit, wenn die Zeichenfolge von 1 Million-Zeichen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="86051-180">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button press and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="86051-181">Der wichtigste Punkt hierbei ist die Tatsache, dass der JS-Heap höher als gestartet ist \ (der "Anfang" hier ist der Punkt nach der erzwungenen Garbage Collection \).</span><span class="sxs-lookup"><span data-stu-id="86051-181">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="86051-182">Wenn Sie in der realen Welt dieses Muster mit einer zunehmenden js-Heapgröße oder Knoten Größe gesehen haben, kann dies potenziell einen Speicherverlust definieren.</span><span class="sxs-lookup"><span data-stu-id="86051-182">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <span data-ttu-id="86051-183">Entdecken von frei gelösten Dom-Strukturspeicher Lecks mit Heap-Schnappschüssen</span><span class="sxs-lookup"><span data-stu-id="86051-183">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="86051-184">Ein DOM-Knoten ist nur Garbage Collection, wenn keine Verweise auf den Knoten aus der DOM-Struktur oder dem auf der Seite ausgeführten JavaScript-Code vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="86051-184">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="86051-185">Ein Knoten wird als "losgelöst" bezeichnet, wenn er aus der DOM-Struktur entfernt wird, aber einige JavaScript-Objekte verweisen weiterhin auf ihn.</span><span class="sxs-lookup"><span data-stu-id="86051-185">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="86051-186">Getrennte DOM-Knoten sind eine häufige Ursache für Speicherverluste.</span><span class="sxs-lookup"><span data-stu-id="86051-186">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="86051-187">In diesem Abschnitt erfahren Sie, wie Sie die Heap-Profiler in devtools verwenden, um getrennte Knoten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="86051-187">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="86051-188">Es folgt ein einfaches Beispiel für getrennte DOM-Knoten.</span><span class="sxs-lookup"><span data-stu-id="86051-188">Here is a simple example of detached DOM nodes.</span></span>  

```javascript
var detachedTree;

function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedTree = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

<span data-ttu-id="86051-189">Wenn Sie im Code auf die Schaltfläche klicken `ul` , wird ein Knoten mit zehn unter `li` geordneten Elementen erstellt.</span><span class="sxs-lookup"><span data-stu-id="86051-189">Selecting the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="86051-190">Auf die Knoten wird vom Code verwiesen, aber Sie sind nicht in der DOM-Struktur vorhanden, daher wird jeder getrennt.</span><span class="sxs-lookup"><span data-stu-id="86051-190">The nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="86051-191">Heap-Schnappschüsse sind eine Möglichkeit, getrennte Knoten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="86051-191">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="86051-192">Wie der Name schon sagt, zeigen Heap-Schnappschüsse an, wie der Speicher zwischen den js-Objekten und DOM-Knoten für Ihre Seite zum Zeitpunkt des Schnappschusses verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="86051-192">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="86051-193">Wenn Sie einen Schnappschuss erstellen möchten, öffnen Sie devtools, und wechseln Sie zum **Speicher** Panel, wählen Sie das Optionsfeld **Heap-Snapshot** aus, und drücken Sie dann die Schaltfläche **Schnappschuss aufnehmen** .</span><span class="sxs-lookup"><span data-stu-id="86051-193">To create a snapshot, open DevTools and go to the **Memory** panel, select the **Heap snapshot** radio button, and then press the **Take snapshot** button.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   <span data-ttu-id="86051-195">Abbildung 4: Erstellen eines Heap-Snapshots</span><span class="sxs-lookup"><span data-stu-id="86051-195">Figure 4:  Take heap snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="86051-196">Der Snapshot kann einige Zeit dauern, bis er verarbeitet und geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="86051-196">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="86051-197">Wenn Sie den Vorgang beenden, wählen Sie ihn im linken Panel aus. \ (benannte **Heap-Schnappschüsse**\).</span><span class="sxs-lookup"><span data-stu-id="86051-197">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="86051-198">Geben `Detached` Sie in das Textfeld **Klassenfilter** ein, um nach frei gelösten Dom-Strukturen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="86051-198">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   <span data-ttu-id="86051-200">Abbildung 5: Filtern nach getrennten Knoten</span><span class="sxs-lookup"><span data-stu-id="86051-200">Figure 5:  Filtering for detached nodes</span></span>  
:::image-end:::  

<span data-ttu-id="86051-201">Erweitern Sie die Karat, um eine frei gelöste Struktur zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="86051-201">Expand the carats to investigate a detached tree.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   <span data-ttu-id="86051-203">Abbildung 6: untersuchen einer getrennten Struktur</span><span class="sxs-lookup"><span data-stu-id="86051-203">Figure 6:  Investigating detached tree</span></span>  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="86051-204">Wählen Sie einen Knoten aus, um ihn weiter zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="86051-204">Select a node to investigate it further.</span></span>  <span data-ttu-id="86051-205">Im **Objekt** Bereich können Sie weitere Informationen zu dem Code anzeigen, der darauf verweist.</span><span class="sxs-lookup"><span data-stu-id="86051-205">In the **Objects** pane you are able to see more information about the code that is referencing it.</span></span>  <span data-ttu-id="86051-206">In der folgenden Abbildung können Sie beispielsweise feststellen, dass die `detachedNodes` Variable auf den Knoten verweist.</span><span class="sxs-lookup"><span data-stu-id="86051-206">For example, in the following figure you are able to see that the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="86051-207">Um diesen bestimmten Speicherverlust zu beheben, sollten Sie den Code untersuchen, der die Variable verwendet, `detachedUNode` und sicherstellen, dass der Verweis auf den Knoten entfernt wird, wenn er nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="86051-207">To fix this particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   <span data-ttu-id="86051-209">Abbildung 7: Untersuchen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="86051-209">Figure 7:  Investigating a node</span></span>  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <span data-ttu-id="86051-210">Ermitteln von JS-Heapspeicher Lecks mit Zuordnungs Instrumentation auf Zeitachse</span><span class="sxs-lookup"><span data-stu-id="86051-210">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="86051-211">Die **Zuweisungs Instrumentation auf der Zeitachse** ist ein weiteres Tool, mit dem Sie möglicherweise Speicherverluste in Ihrem js-Heap ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="86051-211">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="86051-212">Demonstrieren Sie die **Zuweisungs Instrumentation auf Zeitachse**  mithilfe des folgenden Codes.</span><span class="sxs-lookup"><span data-stu-id="86051-212">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="86051-213">Jedes Mal, wenn die Schaltfläche, auf die im Code verwiesen wird, gedrückt wird, wird dem Array eine Zeichenfolge von 1 Million-Zeichen hinzugefügt `x` .</span><span class="sxs-lookup"><span data-stu-id="86051-213">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="86051-214">Wenn Sie eine Zuordnungs Instrumentation auf der Zeitachse aufzeichnen möchten, öffnen Sie devtools, wechseln Sie zur Register **Karte Speicher** , wählen Sie das Optionsfeld **Zuweisungs Instrumentation auf Zeitachse** aus, drücken Sie die Schaltfläche **Start** , führen Sie die Aktion aus, die Sie vermuten, dass der Speicherverlust verursacht wird, und drücken Sie dann die Schaltfläche **Aufzeichnung** Beenden der Aufzeichnung beenden, ![ ][ImageStopRecordingIcon] Wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="86051-214">To record an Allocation instrumentation on timeline, open DevTools, go to the **Memory** panel, select the **Allocation instrumentation on timeline** radio button, press the **Start** button, perform the action that you suspect is causing the memory leak, and then press the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="86051-215">Beachten Sie während der Aufzeichnung, ob blaue Balken in der Zuordnungs Instrumentation auf der Zeitachse angezeigt werden, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="86051-215">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   <span data-ttu-id="86051-217">Abbildung 8: neue Zuweisungen</span><span class="sxs-lookup"><span data-stu-id="86051-217">Figure 8:  New allocations</span></span>  
:::image-end:::  

<span data-ttu-id="86051-218">Diese blauen Balken stellen neue Speicherzuweisungen dar.</span><span class="sxs-lookup"><span data-stu-id="86051-218">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="86051-219">Diese neuen Speicherzuweisungen sind ihre Kandidaten für Speicherverluste.</span><span class="sxs-lookup"><span data-stu-id="86051-219">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="86051-220">Sie können auf eine Leiste Zoomen, um den Bereich " **Konstruktor** " zu filtern, sodass nur Objekte angezeigt werden, die während des angegebenen Zeitrahmens reserviert wurden.</span><span class="sxs-lookup"><span data-stu-id="86051-220">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   <span data-ttu-id="86051-222">Abbildung 9: Zeitachse mit vergrößerten Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="86051-222">Figure 9:  Zoomed allocation timeline</span></span>  
:::image-end:::  

<span data-ttu-id="86051-223">Erweitern Sie das Objekt, und wählen Sie den Wert aus, um weitere Details im **Objekt** Bereich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="86051-223">Expand the object and select the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="86051-224">In der folgenden Abbildung können Sie beispielsweisedurch Anzeigen der Details des Objekts, das neu zugeordnet wurde, sehen, dass es der `x` Variablen im Bereich zugeordnet wurde `Window` .</span><span class="sxs-lookup"><span data-stu-id="86051-224">For example, in the following figure, by viewing the details of the object that was newly allocated, you should be able to see that it was allocated to the `x` variable in the `Window` scope.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   <span data-ttu-id="86051-226">Abbildung 10: Objektdetails</span><span class="sxs-lookup"><span data-stu-id="86051-226">Figure 10:  Object details</span></span>  
:::image-end:::  

## <span data-ttu-id="86051-227">Untersuchen der Speicherzuweisung nach Funktion</span><span class="sxs-lookup"><span data-stu-id="86051-227">Investigate memory allocation by function</span></span>  

<span data-ttu-id="86051-228">Verwenden Sie den Profilerstellungs-Typ der **Zuordnungs Stichprobe** , um die Speicherzuweisung nach JavaScript-Funktion anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="86051-228">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   <span data-ttu-id="86051-230">Abbildung 11: Sampling zur Daten Satz Zuteilung</span><span class="sxs-lookup"><span data-stu-id="86051-230">Figure 11:  Record Allocation sampling</span></span>  
:::image-end:::  

1.  <span data-ttu-id="86051-231">Aktivieren Sie das Optionsfeld **Zuweisungs Sampling** .</span><span class="sxs-lookup"><span data-stu-id="86051-231">Select the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="86051-232">Wenn auf der Seite eine Arbeitskraft vorhanden ist, können Sie diese über das Dropdownmenü neben der Schaltfläche **Start** als Profil Ziel auswählen.</span><span class="sxs-lookup"><span data-stu-id="86051-232">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="86051-233">Drücken Sie die Schaltfläche **Start** .</span><span class="sxs-lookup"><span data-stu-id="86051-233">Press the **Start** button.</span></span>  
1.  <span data-ttu-id="86051-234">Führen Sie die Aktionen auf der Seite aus, die Sie untersuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="86051-234">Perform the actions on the page which you want to investigate.</span></span>  
1.  <span data-ttu-id="86051-235">Drücken Sie die **Stopp** -Taste, wenn Sie alle Ihre Aktionen beendet haben.</span><span class="sxs-lookup"><span data-stu-id="86051-235">Press the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="86051-236">DevTools zeigt eine Aufschlüsselung der Speicherzuweisung nach Funktion.</span><span class="sxs-lookup"><span data-stu-id="86051-236">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="86051-237">Die Standardansicht ist **schwer (unten nach oben)**, in der die Funktionen angezeigt werden, die den größten Arbeitsspeicher oben zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="86051-237">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Öffnen des Task-Managers des Microsoft Edge-Browsers" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   <span data-ttu-id="86051-239">Abbildung 12: Zuordnungs Stichproben</span><span class="sxs-lookup"><span data-stu-id="86051-239">Figure 12:  Allocation sampling</span></span>  
:::image-end:::  

## <span data-ttu-id="86051-240">Häufige Garbage Collections erkennen</span><span class="sxs-lookup"><span data-stu-id="86051-240">Spot frequent garbage collections</span></span>  

<span data-ttu-id="86051-241">Wenn Ihre Seite häufig angehalten wird, haben Sie möglicherweise Probleme mit der Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="86051-241">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="86051-242">Sie können entweder den Microsoft Edge-Browser-Task-Manager oder Leistungs Speicher Aufzeichnungen verwenden, um häufige Garbage Collection zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="86051-242">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="86051-243">Im Microsoft Edge-Browser Task-Manager stellen häufig steigende und fallende **Speicher** -oder **JavaScript-Speicher** Werte häufige Garbage Collection dar.</span><span class="sxs-lookup"><span data-stu-id="86051-243">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="86051-244">In Leistungs Aufzeichnungen zeigen häufige Änderungen \ (steigende und fallende \) zu den js-Heap-oder Knotenanzahl-Diagrammen auf häufige Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="86051-244">In Performance recordings, frequent changes \(rising and falling\) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="86051-245">Nachdem Sie das Problem identifiziert haben, können Sie eine **Zuordnungs Instrumentation für die Zeitachsen** Aufzeichnung verwenden, um herauszufinden, wo Speicher reserviert wird und welche Funktionen die Zuweisungen verursachen.</span><span class="sxs-lookup"><span data-stu-id="86051-245">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Aufzeichnen einer Leistungsanalyse Referenz"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> <span data-ttu-id="86051-247">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86051-247">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="86051-248">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="86051-248">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="86051-250">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="86051-250">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
