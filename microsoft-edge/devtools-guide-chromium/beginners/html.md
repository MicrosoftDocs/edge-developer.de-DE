---
description: Erste Schritte mit HTML und dem DOM
title: 'DevTools für Anfänger: Erste Schritte mit HTML und dem DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, Devtools, Devtools für Anfänger, Devtools-HTML für Anfänger, Devtools-DOM für Anfänger, Devtools-HTML-Lernprogramm, Devtools-DOM-Lernprogramm, DevTools-Lernprogramm zum Dokumentobjektmodell
ms.openlocfilehash: a049ec500e22f89db3ab1e966b55d89c2ad682fe
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643512"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a><span data-ttu-id="ad81b-104">DevTools für Anfänger: Erste Schritte mit HTML und dem DOM</span><span class="sxs-lookup"><span data-stu-id="ad81b-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="ad81b-105">Dies ist der erste einer Reihe von Lernprogrammen, die Ihnen die Grundlagen der Webentwicklung vermitteln.</span><span class="sxs-lookup"><span data-stu-id="ad81b-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span> <span data-ttu-id="ad81b-106">Erfahren Sie mehr über eine Reihe von Webentwicklertools namens Microsoft Edge DevTools, die Ihre Produktivität steigern können.</span><span class="sxs-lookup"><span data-stu-id="ad81b-106">Learn about a set of web developer tools, named Microsoft Edge DevTools, that may increase your productivity.</span></span>  

<span data-ttu-id="ad81b-107">In diesem Lernprogramm werden HTML und das [Dokumentobjektmodell](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ad81b-107">This tutorial describes HTML and the [Document Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\).</span></span> <span data-ttu-id="ad81b-108">HTML ist eine der Kerntechnologien der Webentwicklung.</span><span class="sxs-lookup"><span data-stu-id="ad81b-108">HTML is one of the core technologies of web development.</span></span> <span data-ttu-id="ad81b-109">Es ist die Sprache, die die Struktur und den Inhalt von Webseiten steuert.</span><span class="sxs-lookup"><span data-stu-id="ad81b-109">It is the language that controls the structure and content of webpages.</span></span> <span data-ttu-id="ad81b-110">Das DOM bezieht sich auch auf die Struktur und den Inhalt von Webseiten, über die wir später mehr erfahren.</span><span class="sxs-lookup"><span data-stu-id="ad81b-110">The DOM is also related to the structure and content of webpages, which we learn more about later.</span></span>

## <a name="goals"></a><span data-ttu-id="ad81b-111">Ziele</span><span class="sxs-lookup"><span data-stu-id="ad81b-111">Goals</span></span>  

<span data-ttu-id="ad81b-112">Sie werden die Webentwicklung erlernen, indem Sie eine Website erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-112">You're going to learn web development by building a website.</span></span>  <span data-ttu-id="ad81b-113">Wenn Sie alle Lernprogramme in der **DevTools for Beginners-Reihe** abgeschlossen haben, sieht Ihre fertige Website möglicherweise wie in der folgenden Abbildung aus.</span><span class="sxs-lookup"><span data-stu-id="ad81b-113">By the time you complete all of the tutorials in the **DevTools for Beginners** series, your finished site may look like the following figure.</span></span>  

:::image type="complex" source="media/beginners-html-finished.msft.png" alt-text="Die fertige Website" lightbox="media/beginners-html-finished.msft.png":::
   <span data-ttu-id="ad81b-115">Die fertige Website</span><span class="sxs-lookup"><span data-stu-id="ad81b-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="ad81b-116">Am Ende dieses Lernprogramms sollten Sie die folgenden Konzepte verstehen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-116">By the end of this tutorial, you should understand the following concepts.</span></span>  

*   <span data-ttu-id="ad81b-117">Wie HTML und das DOM die Inhalte erstellen, die auf Webseiten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad81b-117">How HTML and the DOM create the content displayed on webpages.</span></span>  
*   <span data-ttu-id="ad81b-118">Wie Microsoft Edge DevTools Ihnen beim Experimentieren mit HTML- und DOM-Änderungen helfen kann.</span><span class="sxs-lookup"><span data-stu-id="ad81b-118">How Microsoft Edge DevTools may help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="ad81b-119">Der Unterschied zwischen HTML und DOM.</span><span class="sxs-lookup"><span data-stu-id="ad81b-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="ad81b-120">Sie haben auch eine funktionsfähige Website.</span><span class="sxs-lookup"><span data-stu-id="ad81b-120">You will also have a working website.</span></span> <span data-ttu-id="ad81b-121">Sie können die Website verwenden, um Ihren Lebenslauf oder Blog zu hosten.</span><span class="sxs-lookup"><span data-stu-id="ad81b-121">You may use the site to host your resume or blog.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="ad81b-122">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ad81b-122">Prerequisites</span></span>  

<span data-ttu-id="ad81b-123">Bevor Sie dieses Lernprogramm testen, erfüllen Sie die folgenden Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="ad81b-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="ad81b-124">Wenn Sie mit HTML nicht vertraut sind, lesen Sie ["Erste Schritte mit HTML"][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="ad81b-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="ad81b-125">Laden Sie den [Microsoft Edge][MicrosoftEdgeInsider] Webbrowser herunter.</span><span class="sxs-lookup"><span data-stu-id="ad81b-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="ad81b-126">Dieses Lernprogramm verwendet eine Reihe von Webentwicklungstools, die als Microsoft Edge DevTools bezeichnet werden, die in Microsoft Edge integriert sind.</span><span class="sxs-lookup"><span data-stu-id="ad81b-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="ad81b-127">Einrichten des Codes</span><span class="sxs-lookup"><span data-stu-id="ad81b-127">Set up your code</span></span>  

<span data-ttu-id="ad81b-128">Sie werden eine Website im Glitch-Onlinecode-Editor erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-128">You are going to build a site in the Glitch online code editor.</span></span>  

1.  <span data-ttu-id="ad81b-129">Öffnen Sie den [Quellcode.][GlitchAlluringShockIndex]</span><span class="sxs-lookup"><span data-stu-id="ad81b-129">Open the [source code][GlitchAlluringShockIndex].</span></span> <span data-ttu-id="ad81b-130">Diese Registerkarte wird in diesem Lernprogramm als **Editor-Registerkarte** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ad81b-130">This tab is called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup1.msft.png" alt-text="Die Registerkarte "Editor"" lightbox="media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="ad81b-132">Die Registerkarte "Editor"</span><span class="sxs-lookup"><span data-stu-id="ad81b-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ad81b-133">Wählen Sie **"Verallgemählt" aus.**</span><span class="sxs-lookup"><span data-stu-id="ad81b-133">Choose **alluring-shock**.</span></span> <span data-ttu-id="ad81b-134">Das Menü **Project Optionen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ad81b-134">The **Project Options** menu opens.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup2.msft.png" alt-text="Menü "Project-Optionen"" lightbox="media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="ad81b-136">Menü "Project-Optionen"</span><span class="sxs-lookup"><span data-stu-id="ad81b-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ad81b-137">Wählen Sie **Remix Project**aus.</span><span class="sxs-lookup"><span data-stu-id="ad81b-137">Choose **Remix Project**.</span></span> <span data-ttu-id="ad81b-138">Glitch erstellt eine Kopie des Projekts, die Sie bearbeiten können, und generiert zufällig einen neuen Namen für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-138">Glitch creates a copy of the project that you may edit and randomly generates a new name for the project.</span></span> <span data-ttu-id="ad81b-139">Der Inhalt ist derselbe wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="ad81b-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup3.msft.png" alt-text="Das remixierte Projekt" lightbox="media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="ad81b-141">Das remixierte Projekt</span><span class="sxs-lookup"><span data-stu-id="ad81b-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ad81b-142">Wenn Sie das nächste Lernprogramm dieser Reihe abschließen möchten, wählen Sie "Bei Glitch **anmelden"** mit Ihrem Facebook-, GitHub- oder Google-Konto aus. oder senden Sie sich selbst einen Hexenlink.</span><span class="sxs-lookup"><span data-stu-id="ad81b-142">If you plan to complete the next tutorial in this series, choose **Sign In** to Glitch using your Facebook, GitHub, or Google account; or email yourself a magic link.</span></span> <span data-ttu-id="ad81b-143">Wenn Sie sich nicht bei einem Konto anmelden möchten, können Sie das Projekt nach dem Schließen der Editorregisterkarte nicht bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ad81b-143">If you choose not to sign in to an account, you cannot edit the project after closing the editor tab.</span></span>

1.  <span data-ttu-id="ad81b-144">Wählen \*\*\*\* Sie  \>  **"In einem neuen Fenster anzeigen"** aus.</span><span class="sxs-lookup"><span data-stu-id="ad81b-144">Choose **Show** \> **In a New Window**.</span></span>  <span data-ttu-id="ad81b-145">Eine neue Registerkarte mit der Liveseite wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ad81b-145">A new tab opens, showing the live page.</span></span> <span data-ttu-id="ad81b-146">Diese Registerkarte wird in diesem Lernprogramm als **Live-Registerkarte** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ad81b-146">This tab is called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup4.msft.png" alt-text="Die Live-Registerkarte" lightbox="media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="ad81b-148">Die Live-Registerkarte</span><span class="sxs-lookup"><span data-stu-id="ad81b-148">The live tab</span></span>  
    :::image-end:::  
    
## <a name="add-content"></a><span data-ttu-id="ad81b-149">Hinzufügen von Inhalten</span><span class="sxs-lookup"><span data-stu-id="ad81b-149">Add content</span></span>  

<span data-ttu-id="ad81b-150">Ihre Website benötigt weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-150">Your site needs more information.</span></span> <span data-ttu-id="ad81b-151">Führen Sie die folgenden Schritte aus, um Einige Inhalte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-151">Complete the following steps to add some content.</span></span>  

1. <span data-ttu-id="ad81b-152">Ersetzen Sie auf der **Registerkarte "Editor"** `<!-- You're "About Me" will go here.  -->` durch `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="ad81b-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    ```html
        ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                </main>
        ...
    ```  
    
    :::image type="complex" source="media/beginners-html-add1.msft.png" alt-text="Der neue Code wird auf der Registerkarte "Editor" hervorgehoben." lightbox="media/beginners-html-add1.msft.png":::
        <span data-ttu-id="ad81b-154">Der neue Code wird auf der Registerkarte "Editor" hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="ad81b-154">The new code is highlighted in the editor tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="ad81b-155">Zeigen Sie Ihre Änderungen auf der **Registerkarte "Live" an.** Der Text `About Me` ist auf der Seite sichtbar.</span><span class="sxs-lookup"><span data-stu-id="ad81b-155">View your changes in the **live tab**. The text `About Me` is visible on the page.</span></span> <span data-ttu-id="ad81b-156">Der Text ist größer als der umgebende Text, da das `<h1>` Element eine Überschrift 1 darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-156">The text is larger than the surrounding text because the `<h1>` element represents a Heading 1.</span></span>  <span data-ttu-id="ad81b-157">Ihr Webbrowser formatiert Überschriften automatisch in größeren Schriftgraden.</span><span class="sxs-lookup"><span data-stu-id="ad81b-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="media/beginners-html-add2.msft.png" alt-text="Die neue Überschrift ist auf der Registerkarte "Live" sichtbar." lightbox="media/beginners-html-add2.msft.png":::
       <span data-ttu-id="ad81b-159">Die neue Überschrift ist auf der Registerkarte "Live" sichtbar.</span><span class="sxs-lookup"><span data-stu-id="ad81b-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="ad81b-160">Zurück auf der **Registerkarte "Editor"** fügen Sie `<p>I am learning web development. Recent accomplishments:</p>` die Zeile darunter  `<h1>About Me</h1>` ein.</span><span class="sxs-lookup"><span data-stu-id="ad81b-160">Back in the **editor tab**, insert `<p>I am learning web development. Recent accomplishments:</p>` on the line below  `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                    <p>I am learning web development. Recent accomplishments:</p>
                </main>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add3.msft.png" alt-text="Der aktualisierte Code wird auf der Registerkarte "Editor" hervorgehoben." lightbox="media/beginners-html-add3.msft.png":::
        <span data-ttu-id="ad81b-162">Der aktualisierte Code wird auf der Registerkarte "Editor" hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="ad81b-162">The updated code is highlighted in the editor tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="ad81b-163">Zeigen Sie Ihre Änderung auf der **Registerkarte "Live" an.**</span><span class="sxs-lookup"><span data-stu-id="ad81b-163">View your change in the **live tab**.</span></span>

1. <span data-ttu-id="ad81b-164">Fügen Sie auf der **Registerkarte "Editor"** mithilfe des folgenden Codes eine Liste Ihrer Erfolge hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad81b-164">Back in the **editor tab**, add a list of your accomplishments using the following code.</span></span>
    
    ```html
    ...
    <p>I am learning web development.  Recent accomplishments:</p>
        <ul>
            <li>Learned how to set up my code in Glitch.</li>
            <li>Added content to my HTML.</li>
            <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
            <li>TODO: Learn the difference between HTML and the DOM.</li>
        </ul>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add4.msft.png" alt-text="Der aktualisierte Code wird auch auf der Registerkarte "Editor" hervorgehoben." lightbox="media/beginners-html-add4.msft.png":::
        <span data-ttu-id="ad81b-166">Der aktualisierte Code wird auch auf der Registerkarte "Editor" hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="ad81b-166">The updated code is also highlighted in the editor tab</span></span>  
    :::image-end:::  

1. <span data-ttu-id="ad81b-167">Zeigen Sie die **Live-Registerkarte** an, um sicherzustellen, dass der neue Inhalt korrekt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ad81b-167">View the **live tab** to make sure that the new content displays correctly.</span></span>  
    
    :::image type="complex" source="media/beginners-html-add5.msft.png" alt-text="Die neue Liste ist auf der Registerkarte "Live" sichtbar." lightbox="media/beginners-html-add5.msft.png":::
       <span data-ttu-id="ad81b-169">Die neue Liste ist auf der Registerkarte "Live" sichtbar.</span><span class="sxs-lookup"><span data-stu-id="ad81b-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a><span data-ttu-id="ad81b-170">Experimentieren Mit Inhaltsänderungen in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ad81b-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="ad81b-171">Wenn Sie eine Seite mit viel HTML entwickeln, wird es mühsam, zwischen der Editor-Registerkarte und der Live-Registerkarte hin und her zu wechseln, um Ihre Änderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-171">If you are developing a page with a lot of HTML, it becomes tedious to go back-and-forth between the editor tab and the live tab to see your changes.</span></span> <span data-ttu-id="ad81b-172">Microsoft Edge DevTools hilft Ihnen beim Experimentieren mit Inhaltsänderungen, ohne die **Live-Registerkarte**zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-172">Microsoft Edge DevTools helps you experiment with content changes without ever leaving the **live tab**.</span></span>  

### <a name="learn-the-difference-between-html-and-the-dom"></a><span data-ttu-id="ad81b-173">Lernen Sie den Unterschied zwischen HTML und DOM kennen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="ad81b-174">Bevor Sie Inhalte von Microsoft Edge DevTools bearbeiten, sollten wir den Unterschied zwischen HTML und DOM verstehen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-174">Before editing content from Microsoft Edge DevTools, let's understand the difference between HTML and the DOM.</span></span> <span data-ttu-id="ad81b-175">Fahren Sie mit den folgenden Schritten fort, um von einem Beispiel zu lernen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-175">Proceed with the following steps to learn from an example.</span></span>

1. <span data-ttu-id="ad81b-176">Navigieren Sie zur **Registerkarte "Live".** Am unteren Rand der Seite wird der Text `A new element!?!` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-176">Navigate to the **live tab**. At the bottom of your page, the text `A new element!?!` displays.</span></span>  

    <!--
        :::image type="complex" source="media/beginners-html-dom1.msft.png" alt-text="At the bottom of the page the text A new element!?! displays" lightbox="media/beginners-html-dom1.msft.png":::
        At the bottom of the page the text `A new element!?!` is displays  
        :::image-end:::
    -->
    
1. <span data-ttu-id="ad81b-177">Öffnen Sie die **Registerkarte "Editor",** und versuchen Sie, den Text in zu `index.html` finden.</span><span class="sxs-lookup"><span data-stu-id="ad81b-177">Open the **editor tab** and try to find the text in `index.html`.</span></span> <span data-ttu-id="ad81b-178">Der Text wird in dieser Ansicht nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-178">The text does not display in this view.</span></span>  

    <!--
        :::image type="complex" source="media/beginners-html-dom2.msft.png" alt-text="The mystery text A new element!?! is not found in index.html" lightbox="media/beginners-html-dom2.msft.png":::
        The mystery text `A new element!?!` is not found in `index.html`  
        :::image-end:::
    -->

1. <span data-ttu-id="ad81b-179">Öffnen Sie die **Registerkarte "Live",** zeigen Sie darauf, öffnen Sie `A new element!?!` das Kontextmenü (Rechtsklick), und wählen Sie dann **"Überprüfen"** aus.</span><span class="sxs-lookup"><span data-stu-id="ad81b-179">Open the **live tab**, hover over `A new element!?!`, open the contextual menu (right-click) and then choose **Inspect**.</span></span>  
    
    :::image type="complex" source="media/beginners-html-dom3.msft.png" alt-text="Überprüfen von Text" lightbox="media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="ad81b-181">Überprüfen von Text</span><span class="sxs-lookup"><span data-stu-id="ad81b-181">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="ad81b-182">DevTools wird zusammen mit Ihrer Seite geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ad81b-182">DevTools opens up alongside your page.</span></span> `<div>A new element!?!</div>` <span data-ttu-id="ad81b-183">hervorgehoben ist.</span><span class="sxs-lookup"><span data-stu-id="ad81b-183">is highlighted.</span></span> <span data-ttu-id="ad81b-184">Obwohl diese Struktur in DevTools wie HTML aussieht, ist sie die **DOM-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="ad81b-184">Although this structure in DevTools looks like HTML, it is the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="media/beginners-html-dom4.msft.png" alt-text="DevTools ist neben der Seite geöffnet" lightbox="media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="ad81b-186">DevTools ist neben der Seite geöffnet</span><span class="sxs-lookup"><span data-stu-id="ad81b-186">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="ad81b-187">Wenn Ihre Seite geladen wird, verwendet der Browser den HTML-Code, um den anfänglichen Inhalt der Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-187">When your page loads, the browser uses the HTML to create the initial content of the page.</span></span> <span data-ttu-id="ad81b-188">Das DOM stellt den aktuellen Inhalt der Seite dar, der sich im Laufe der Zeit ändern kann.</span><span class="sxs-lookup"><span data-stu-id="ad81b-188">The DOM represents the current content of the page, which may change over time.</span></span> 

<span data-ttu-id="ad81b-189">Der `<div>A new element!?!</div>` Inhalt wird ihrer Seite aufgrund des Tags am `<script src="new.js"></script>` unteren Rand Ihres HTML-Codes hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-189">The `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span> <span data-ttu-id="ad81b-190">Dieses Tag bewirkt, dass JavaScript-Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad81b-190">This tag causes some JavaScript code to run.</span></span> <span data-ttu-id="ad81b-191">Weitere Informationen zu JavaScript finden Sie in einem [späteren Lernprogramm.](../javascript/index.md)</span><span class="sxs-lookup"><span data-stu-id="ad81b-191">Learn more about JavaScript in a [later tutorial](../javascript/index.md).</span></span>

<span data-ttu-id="ad81b-192">Stellen Sie sich vorerst eine Skriptsprache vor, die den Inhalt Ihrer Seite ändern kann.</span><span class="sxs-lookup"><span data-stu-id="ad81b-192">For now, think of it as a scripting language that may change the content of your page.</span></span> <span data-ttu-id="ad81b-193">In diesem Fall wird Ihrer Seite JavaScript-Code `<div>A new element!?!</div>` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-193">In this case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span> <span data-ttu-id="ad81b-194">Aus diesem Grund wird dieser Text auf der **Live-Registerkarte,** aber nicht im HTML-Code angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-194">That is why this text is displayed in the **live** tab, but not in the HTML.</span></span>  

### <a name="edit-the-dom"></a><span data-ttu-id="ad81b-195">Bearbeiten des DOM</span><span class="sxs-lookup"><span data-stu-id="ad81b-195">Edit the DOM</span></span>  

<span data-ttu-id="ad81b-196">Wenn Sie schnell mit Inhaltsänderungen experimentieren möchten, ohne die Live-Registerkarte verlassen zu müssen, testen Sie DevTools.</span><span class="sxs-lookup"><span data-stu-id="ad81b-196">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="ad81b-197">Zeigen Sie in DevTools mit dem Mauszeiger darauf, öffnen Sie `Your site!` das Kontextmenü (rechtsklick), und wählen Sie **"Als HTML bearbeiten"** aus.</span><span class="sxs-lookup"><span data-stu-id="ad81b-197">In DevTools, hover over `Your site!`, open the contextual menu (right-click) and choose **Edit as HTML**.</span></span>  
    
1.  <span data-ttu-id="ad81b-198">Ersetzen Sie `<p>Your site!</p>` dies durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="ad81b-198">Replace `<p>Your site!</p>` with the following code.</span></span>  

```html
    ...
    <header>
        <p><b>Welcome to my site!</b></p>
        <button>Download my resume</button>
    </header>
    ...
```  

:::image type="complex" source="media/beginners-html-edit2.msft.png" alt-text="Aktualisieren des Knotens als HTML" lightbox="media/beginners-html-edit2.msft.png":::
    <span data-ttu-id="ad81b-200">Aktualisieren des Knotens als HTML</span><span class="sxs-lookup"><span data-stu-id="ad81b-200">Updating the node as HTML</span></span>  
<span data-ttu-id="ad81b-201">::image-end:::</span><span class="sxs-lookup"><span data-stu-id="ad81b-201">::image-end:::</span></span>  

1.  <span data-ttu-id="ad81b-202">Wählen Sie `Control` + `Enter` \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus, um Ihre Änderungen zu speichern, oder wählen Sie außerhalb des Felds aus.</span><span class="sxs-lookup"><span data-stu-id="ad81b-202">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or select outside the box.</span></span> <span data-ttu-id="ad81b-203">Ihre Änderungen werden automatisch in der Liveansicht Ihrer Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-203">Your changes automatically show up in the live view of your page.</span></span> <span data-ttu-id="ad81b-204">Der Text `Your site!` wurde durch den neuen Inhalt ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-204">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="media/beginners-html-edit3.msft.png" alt-text="Der neue Inhalt wird sofort auf der Seite angezeigt." lightbox="media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="ad81b-206">Der neue Inhalt wird sofort auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-206">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="ad81b-207">Dieser Workflow eignet sich nur für das Experimentieren mit Inhaltsänderungen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-207">This workflow is only suitable for experimenting with content changes.</span></span> <span data-ttu-id="ad81b-208">Wenn Sie die Seite aktualisieren oder die Registerkarte schließen, gehen Ihre Änderungen verloren.</span><span class="sxs-lookup"><span data-stu-id="ad81b-208">If you refresh the page or close the tab, your changes are lost.</span></span> <span data-ttu-id="ad81b-209">Wenn Sie Ihre Änderungen speichern möchten, kopieren Sie den Code manuell in Ihre HTML-Datei.</span><span class="sxs-lookup"><span data-stu-id="ad81b-209">If you want to save your changes, manually copy the code to your HTML file.</span></span> <span data-ttu-id="ad81b-210">In den nächsten Abschnitten werden einige weitere Möglichkeiten zum Ändern von Inhalten aus der DOM-Struktur erläutert.</span><span class="sxs-lookup"><span data-stu-id="ad81b-210">The next couple of sections show you some more ways to change content from the DOM Tree.</span></span>  

## <a name="reorder-nodes"></a><span data-ttu-id="ad81b-211">Knoten neu anordnen</span><span class="sxs-lookup"><span data-stu-id="ad81b-211">Reorder nodes</span></span>

<span data-ttu-id="ad81b-212">Sie können auch die Reihenfolge der DOM-Knoten ändern.</span><span class="sxs-lookup"><span data-stu-id="ad81b-212">You may also change the order of DOM nodes.</span></span> <span data-ttu-id="ad81b-213">Beispielsweise befindet sich das Navigationsmenü auf ihrer Webseite am unteren Rand.</span><span class="sxs-lookup"><span data-stu-id="ad81b-213">For example, on your web page the navigation menu is near the bottom.</span></span> <span data-ttu-id="ad81b-214">Führen Sie die folgenden Schritte aus, um sie nach oben zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ad81b-214">To move it to the top, perform the following steps.</span></span>  

1.  <span data-ttu-id="ad81b-215">Suchen Sie den `<nav>` Knoten in der **DOM-Struktur** von DevTools.</span><span class="sxs-lookup"><span data-stu-id="ad81b-215">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="media/beginners-html-reorder1.msft.png" alt-text="Der Navigationsknoten ist in DevTools hervorgehoben." lightbox="media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="ad81b-217">Der Navigationsknoten ist in DevTools hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="ad81b-217">The nav node is highlighted in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ad81b-218">Ziehen Sie den `<nav>` Knoten nach oben, damit der Knoten das erste untergeordnete Element nach dem `<body>` Knoten ist.</span><span class="sxs-lookup"><span data-stu-id="ad81b-218">Drag the `<nav>` node to the top, so that the node is the first child after the `<body>` node.</span></span>  
    
    :::image type="complex" source="media/beginners-html-reorder3.msft.png" alt-text="Der Navigationsknoten befindet sich oben auf der Seite." lightbox="media/beginners-html-reorder3.msft.png":::
        <span data-ttu-id="ad81b-220">Der Navigationsknoten befindet sich oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="ad81b-220">The nav node is at the top of the page</span></span>  
    :::image-end:::  
    
### <a name="delete-a-node"></a><span data-ttu-id="ad81b-221">Löschen eines Knotens</span><span class="sxs-lookup"><span data-stu-id="ad81b-221">Delete a node</span></span>

<span data-ttu-id="ad81b-222">Sie können auch Knoten aus der DOM-Struktur entfernen.</span><span class="sxs-lookup"><span data-stu-id="ad81b-222">You may also remove nodes from the DOM Tree.</span></span> <span data-ttu-id="ad81b-223">Führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="ad81b-223">Perform the following steps.</span></span>

1.  <span data-ttu-id="ad81b-224">Wählen Sie in der **DOM-Struktur** `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="ad81b-224">In the **DOM Tree**, choose `<div>A new element!?!</div>`.</span></span> <span data-ttu-id="ad81b-225">DevTools hebt den Knoten hervor.</span><span class="sxs-lookup"><span data-stu-id="ad81b-225">DevTools highlights the node.</span></span> 
    
1.  <span data-ttu-id="ad81b-226">Wählen Sie die `Delete` Taste auf der Tastatur aus.</span><span class="sxs-lookup"><span data-stu-id="ad81b-226">Select the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="ad81b-227">Der `<div>A new element!?!</div>` Knoten wird aus der DOM-Struktur entfernt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-227">The `<div>A new element!?!</div>` node is removed from the DOM Tree.</span></span>  
    
    :::image type="complex" source="media/beginners-html-delete2.msft.png" alt-text="Der Knoten wurde gelöscht." lightbox="media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="ad81b-229">Der Knoten wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ad81b-229">The node has been deleted</span></span>  
    :::image-end:::  
    
## <a name="copy-your-changes"></a><span data-ttu-id="ad81b-230">Kopieren Ihrer Änderungen</span><span class="sxs-lookup"><span data-stu-id="ad81b-230">Copy your changes</span></span>  

<span data-ttu-id="ad81b-231">Sie sind fast fertig.</span><span class="sxs-lookup"><span data-stu-id="ad81b-231">You're almost done.</span></span> <span data-ttu-id="ad81b-232">Sie haben einige Änderungen an der Seite in DevTools vorgenommen, diese werden jedoch nicht im Quellcode gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ad81b-232">You made a few changes to the page in DevTools, but they're not saved to your source code.</span></span>  

1.  <span data-ttu-id="ad81b-233">Aktualisieren Sie die **Live-Registerkarte**. Die Änderungen, die Sie in der DOM-Struktur vorgenommen haben, werden nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad81b-233">Refresh the **live tab**. The changes that you made in the DOM Tree disappear.</span></span> <span data-ttu-id="ad81b-234">Insbesondere kehrt der Text `Your site!` zum oberen Rand der Seite zurück, und der Text wird nach unten `A new element!?!` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad81b-234">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="media/beginners-html-copy1.msft.png" alt-text="Die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden." lightbox="media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="ad81b-236">Die von Ihnen vorgenommenen Änderungen sind nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ad81b-236">The changes that you made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ad81b-237">Kopieren Sie den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="ad81b-237">Copy the following code.</span></span>  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
    
1.  <span data-ttu-id="ad81b-238">Wechseln Sie zurück zur **Registerkarte "Editor",** und ersetzen Sie den Inhalt Der `index.html` Datei durch den Code, den Sie kopiert haben.</span><span class="sxs-lookup"><span data-stu-id="ad81b-238">Go back to the **editor tab** and replace the content of your `index.html` file with the code that you copied.</span></span>  
    
    :::image type="complex" source="media/beginners-html-copy2.msft.png" alt-text="Aussehen der index.html-Datei" lightbox="media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="ad81b-240">So sollte Ihre `index.html` Datei aussehen</span><span class="sxs-lookup"><span data-stu-id="ad81b-240">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="ad81b-241">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ad81b-241">Next steps</span></span>  

*   <span data-ttu-id="ad81b-242">Schließen Sie das nächste Lernprogramm dieser Reihe [ab, Erste Schritte mit CSS,][DevToolsBeginnersCss]um zu erfahren, wie Sie Ihre Seite formatieren und mit Formatvorlagenänderungen in Microsoft Edge DevTools experimentieren.</span><span class="sxs-lookup"><span data-stu-id="ad81b-242">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="ad81b-243">Lesen Sie ["Einführung in das DOM",][MDNIntroductionDom] um mehr über das DOM zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="ad81b-243">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="ad81b-244">Sehen Sie sich einen Kurs wie ["Einführung in die Webentwicklung"][CourseraIntroductionToWebDevelopment] an, um weitere praktische Webentwicklungserfahrungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ad81b-244">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] for more hands-on web development experience.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ad81b-245">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="ad81b-245">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools für Anfänger: Erste Schritte mit CSS-| Microsoft-Dokumente"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Einführung in webentwicklungs | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html – | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Erste Schritte mit HTML-| Mdn"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Einführung in die DOM-| Mdn"  

> [!NOTE]
> <span data-ttu-id="ad81b-252">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad81b-252">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ad81b-253">Die originale Seite wurde [hier](https://developers.google.com/web/tools/chrome-devtools/beginners/html) gefunden und von [Einersine(" ("Technical][KatherineJackson] Writer Intern", "Chrome DevTools\") verfasst.</span><span class="sxs-lookup"><span data-stu-id="ad81b-253">The original page was found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and was authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="ad81b-255">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ad81b-255">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
