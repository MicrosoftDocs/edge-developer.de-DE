---
description: Verwenden Sie das Tool "Probleme", um Probleme mit der aktuellen Webseite zu identifizieren und zu beheben.
title: Suchen und Beheben von Problemen mit dem Tool "Probleme"
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 86277c509aa4b67635661ba3a316fb5b1e3b9d14
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624703"
---
<!-- Copyright Sam Dutton

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="find-and-fix-problems-using-the-issues-tool"></a><span data-ttu-id="226b2-104">Suchen und Beheben von Problemen mit dem Tool "Probleme"</span><span class="sxs-lookup"><span data-stu-id="226b2-104">Find and fix problems using the Issues tool</span></span>

<span data-ttu-id="226b2-105">In Microsoft Edge DevTools analysiert das **Tool "Probleme"** automatisch die aktuelle Webseite, meldet Probleme nach Typ und stellt Dokumentation bereit, um die Probleme zu erläutern und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="226b2-105">In Microsoft Edge DevTools, the **Issues** tool automatically analyzes the current webpage, reports issues grouped by type, and provides documentation to help explain and resolve the issues.</span></span>

<span data-ttu-id="226b2-106">Das **Tool "Probleme"** bietet Feedback in den folgenden Kategorien:</span><span class="sxs-lookup"><span data-stu-id="226b2-106">The **Issues** tool provides feedback in the following categories:</span></span>
*  <span data-ttu-id="226b2-107">Zugänglichkeit.</span><span class="sxs-lookup"><span data-stu-id="226b2-107">Accessibility.</span></span>
*  <span data-ttu-id="226b2-108">Browserübergreifende Kompatibilität.</span><span class="sxs-lookup"><span data-stu-id="226b2-108">Compatibility across browsers.</span></span>
*  <span data-ttu-id="226b2-109">Leistung.</span><span class="sxs-lookup"><span data-stu-id="226b2-109">Performance.</span></span>
*  <span data-ttu-id="226b2-110">Progressive Web Apps.</span><span class="sxs-lookup"><span data-stu-id="226b2-110">Progressive Web Apps.</span></span>
*  <span data-ttu-id="226b2-111">Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="226b2-111">Security.</span></span>
*  <span data-ttu-id="226b2-112">Andere.</span><span class="sxs-lookup"><span data-stu-id="226b2-112">Other.</span></span>

<span data-ttu-id="226b2-113">Feedback im **Problemtool** wird von mehreren Quellen bereitgestellt, einschließlich der Chromium-Plattform, Deque axe, MDN-Browserkompatibilitätsdaten und Webhint.</span><span class="sxs-lookup"><span data-stu-id="226b2-113">Feedback in the **Issues** tool is provided by several sources, including the Chromium platform, Deque axe, MDN browser compatibility data, and webhint.</span></span>  <span data-ttu-id="226b2-114">Informationen zu diesen Feedbackquellen, die das Tool **"Probleme"** auffüllen, erhalten Sie unter:</span><span class="sxs-lookup"><span data-stu-id="226b2-114">For information about these sources of feedback that populate the **Issues** tool, navigate to:</span></span>
*  [<span data-ttu-id="226b2-115">Axe Tools (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="226b2-115">axe Tools Overview</span></span>][DequeAxe]
*  [<span data-ttu-id="226b2-116">browser-compat-data repo</span><span class="sxs-lookup"><span data-stu-id="226b2-116">browser-compat-data repo</span></span>][MDNCompat]
*  [<span data-ttu-id="226b2-117">Webhint</span><span class="sxs-lookup"><span data-stu-id="226b2-117">webhint</span></span>][webhintIo]


## <a name="open-the-issues-tool"></a><span data-ttu-id="226b2-118">Öffnen des Tools "Probleme"</span><span class="sxs-lookup"><span data-stu-id="226b2-118">Open the Issues tool</span></span>

<span data-ttu-id="226b2-119">Führen Sie die folgenden Schritte aus, um das **Problemtool** mithilfe einer Demoseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="226b2-119">Perform the following steps to open the **Issues** tool using a demo page.</span></span>


1.  <span data-ttu-id="226b2-120">Navigieren Sie zu einer Webseite, die Zu behebende Probleme enthält.</span><span class="sxs-lookup"><span data-stu-id="226b2-120">Navigate to a webpage that contains issues to fix.</span></span>  <span data-ttu-id="226b2-121">Öffnen Sie beispielsweise die [Demoseite für Barrierefreiheitstests][A11ytestingPagewitherrors] in einer neuen Registerkarte oder einem neuen Fenster.</span><span class="sxs-lookup"><span data-stu-id="226b2-121">For example, open the [accessibility-testing demo page][A11ytestingPagewitherrors] in a new tab or window.</span></span>

1.  <span data-ttu-id="226b2-122">Öffnen Sie DevTools.</span><span class="sxs-lookup"><span data-stu-id="226b2-122">Open DevTools.</span></span>  <span data-ttu-id="226b2-123">Nach ein paar Sekunden wird der **Problemindikator** \( ![ Problemindikator ](../media/issues-counter-icon.msft.png) \) in der oberen rechten Ecke von DevTools angezeigt.</span><span class="sxs-lookup"><span data-stu-id="226b2-123">After a few seconds, the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) appears, in the upper right corner of DevTools.</span></span>  <span data-ttu-id="226b2-124">Die Anzahl der Probleme im Problemindikator kann unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="226b2-124">The number of issues in your Issues counter might be different.</span></span>

1.  <span data-ttu-id="226b2-125">Wählen Sie den **Problemindikator aus.**</span><span class="sxs-lookup"><span data-stu-id="226b2-125">Select the **Issues counter**.</span></span>  <span data-ttu-id="226b2-126">Das Tool **"Probleme"** wird mit Problemen geöffnet, die in verschiedene Kategorien unterteilt sind.</span><span class="sxs-lookup"><span data-stu-id="226b2-126">The **Issues** tool opens with issues grouped into different categories.</span></span>

    :::image type="complex" source="../media/issues-tool-categories.msft.png" alt-text="Kategorien von Problemen im Tool "Probleme" auf der Demoseite" lightbox="../media/issues-tool-categories.msft.png":::
       <span data-ttu-id="226b2-128">Kategorien von Problemen im Tool "Probleme" auf der Demoseite</span><span class="sxs-lookup"><span data-stu-id="226b2-128">Categories of issues in the Issues tool on the demo page</span></span>
    :::image-end:::

### <a name="other-ways-to-open-the-issues-tool"></a><span data-ttu-id="226b2-129">Weitere Möglichkeiten zum Öffnen des Tools "Probleme"</span><span class="sxs-lookup"><span data-stu-id="226b2-129">Other ways to open the Issues tool</span></span>

<span data-ttu-id="226b2-130">Es gibt mehrere zusätzliche Möglichkeiten, das **Problemtool** zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="226b2-130">There are several additional ways to open the **Issues** tool:</span></span>
*  <span data-ttu-id="226b2-131">Wählen Sie im Hauptbereich oder in der Schublade das Menü **"Weitere Tools** " ( **+** ) aus, und wählen Sie dann **"Probleme"** aus. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="226b2-131">Select the **More Tools** (**+**) menu in the main panel or the **Drawer**, and then select **Issues**.</span></span>
*  <span data-ttu-id="226b2-132">Wählen Sie **Anpassen und Steuern von DevTools**Weitere  >  **Tools**  >  **Probleme**.</span><span class="sxs-lookup"><span data-stu-id="226b2-132">Select **Customize and control DevTools** > **More tools** > **Issues**.</span></span>
*  <span data-ttu-id="226b2-133">Wählen Sie in der DOM-Struktur im **Elementtool** einen Wellen unterstrichenen Elementnamen aus, `Shift` und klicken Sie dann darauf.</span><span class="sxs-lookup"><span data-stu-id="226b2-133">In the DOM tree in the **Elements** tool, select `Shift` and then click a wavy-underlined element name.</span></span>  <span data-ttu-id="226b2-134">Oder öffnen Sie das Kontextmenü für ein wellenförmiges unterstrichenes Element, und wählen Sie dann **Probleme anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="226b2-134">Or, open the context menu on a wavy-underlined element and then select **View issues**.</span></span>

### <a name="issues-are-automatically-ordered-by-severity"></a><span data-ttu-id="226b2-135">Probleme werden automatisch nach Schweregrad sortiert</span><span class="sxs-lookup"><span data-stu-id="226b2-135">Issues are automatically ordered by severity</span></span>

<span data-ttu-id="226b2-136">Innerhalb jeder Problemkategorie werden zuerst die Fehler aufgelistet, dann Warnungen und dann Tipps.</span><span class="sxs-lookup"><span data-stu-id="226b2-136">Within each category of issues, first the errors are listed, then warnings, and then tips.</span></span>

:::image type="complex" source="../media/issues-ordered-by-severity.msft.png" alt-text="Das Tool "Probleme" zeigt Leistungsprobleme nach Schweregrad sortiert an." lightbox="../media/issues-ordered-by-severity.msft.png":::
   <span data-ttu-id="226b2-138">Das Tool **"Probleme"** zeigt Leistungsprobleme nach Schweregrad sortiert an.</span><span class="sxs-lookup"><span data-stu-id="226b2-138">The **Issues** tool displays Performance issues sorted by severity</span></span>
:::image-end:::

### <a name="include-third-party-issues"></a><span data-ttu-id="226b2-139">Einbeziehen von Problemen von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="226b2-139">Include third-party issues</span></span>

<span data-ttu-id="226b2-140">Um Probleme einzuschließen, die durch Websites von Drittanbietern verursacht werden, aktivieren Sie oben im **Problemtool** das Kontrollkästchen **"Probleme** von Drittanbietern einschließen".</span><span class="sxs-lookup"><span data-stu-id="226b2-140">To include issues that are caused by third-party sites, at the top of the **Issues** tool, select the **Include third-party issues** checkbox.</span></span>


## <a name="expand-entries-in-the-issues-tool"></a><span data-ttu-id="226b2-141">Erweitern von Einträgen im Tool "Probleme"</span><span class="sxs-lookup"><span data-stu-id="226b2-141">Expand entries in the Issues tool</span></span>

<span data-ttu-id="226b2-142">Das Tool **"Probleme"** enthält zusätzliche Dokumentationen und empfohlene Korrekturen, die für jedes Problem gelten.</span><span class="sxs-lookup"><span data-stu-id="226b2-142">The **Issues** tool presents additional documentation and recommended fixes to apply to each issue.</span></span>  <span data-ttu-id="226b2-143">Um ein Problem zu erweitern, um diese zusätzlichen Informationen zu erhalten, wählen Sie ein Problem wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="226b2-143">To expand an issue to get this additional information, select an issue, as follows.</span></span>

1.  <span data-ttu-id="226b2-144">Öffnen Sie die [Demoseite][A11ytestingPagewitherrors] in einem neuen Fenster oder einer neuen Registerkarte, und öffnen Sie dann DevTools.</span><span class="sxs-lookup"><span data-stu-id="226b2-144">Open the [demo page][A11ytestingPagewitherrors] in a new window or tab, and then open DevTools.</span></span>

1.  <span data-ttu-id="226b2-145">Öffnen Sie das **Tool "Probleme",** indem Sie den **Problemindikator** \( ![ Problemzähler ](../media/issues-counter-icon.msft.png) \) auswählen.</span><span class="sxs-lookup"><span data-stu-id="226b2-145">Open the **Issues** tool by selecting the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\).</span></span>

1.  <span data-ttu-id="226b2-146">Wählen Sie ein Problem aus, um das Problem zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="226b2-146">Select an issue to expand the issue.</span></span>

    :::image type="complex" source="../media/issues-tool-initial-view-accessibility-page.msft.png" alt-text="Das Tool "Probleme" mit zusätzlichen Informationen zum Beheben des Problems" lightbox="../media/issues-tool-initial-view-accessibility-page.msft.png":::
       <span data-ttu-id="226b2-148">Das **Tool "Probleme"** mit zusätzlichen Informationen zum Beheben des Problems</span><span class="sxs-lookup"><span data-stu-id="226b2-148">The **Issues** tool displaying additional information on how to fix the issue</span></span>
    :::image-end:::

<span data-ttu-id="226b2-149">Jedes angezeigte Problem hat die folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="226b2-149">Each displayed issue has the following components:</span></span>
*   <span data-ttu-id="226b2-150">Eine Überschrift, die das Problem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="226b2-150">A headline describing the issue.</span></span>
*   <span data-ttu-id="226b2-151">Eine Beschreibung, die mehr Kontext und vorgeschlagene Lösungen bietet.</span><span class="sxs-lookup"><span data-stu-id="226b2-151">A description providing more context and proposed solutions.</span></span>
*   <span data-ttu-id="226b2-152">Ein **Abschnitt "BETROFFENE RESSOURCEN",** der mit Ressourcen in DevTools verknüpft ist, z. B. dem Tool **"Elemente",** **"Quellen"** oder **"Netzwerk".**</span><span class="sxs-lookup"><span data-stu-id="226b2-152">An **AFFECTED RESOURCES** section that links to resources in DevTools, such as the **Elements**, **Sources**, or **Network** tool.</span></span>
*   <span data-ttu-id="226b2-153">Links zu weiteren Dokumentationen.</span><span class="sxs-lookup"><span data-stu-id="226b2-153">Links to further documentation.</span></span>


## <a name="view-issues-in-context-of-an-associated-tool"></a><span data-ttu-id="226b2-154">Anzeigen von Problemen im Kontext eines zugeordneten Tools</span><span class="sxs-lookup"><span data-stu-id="226b2-154">View issues in context of an associated tool</span></span>

<span data-ttu-id="226b2-155">Ein Problem im **Problemtool** kann eine oder mehrere Links enthalten, die unterschiedliche Tools öffnen, z. B. das Tool **"Elemente",** **"Quellen"** oder **"Netzwerk".**</span><span class="sxs-lookup"><span data-stu-id="226b2-155">An issue in the **Issues** tool may include one or more links that open different tools, such as the **Elements**, **Sources**, or **Network** tool.</span></span> <span data-ttu-id="226b2-156">Sie können eines dieser Tools öffnen, um zusätzliche Problembehandlungsschritte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="226b2-156">You can open one of these tools to perform additional troubleshooting steps.</span></span> <span data-ttu-id="226b2-157">Führen Sie die folgenden Schritte aus, um ein verknüpftes Tool aus dem Tool **"Probleme"** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="226b2-157">To open a linked tool from the **Issues** tool, perform the following steps.</span></span>

1.  <span data-ttu-id="226b2-158">Öffnen Sie wie im vorherigen Abschnitt beschrieben die Demoseite, und erweitern Sie dann ein Problem im **Tool "Probleme".**</span><span class="sxs-lookup"><span data-stu-id="226b2-158">As described in the previous section, open the demo page and then expand an issue in the **Issues** tool.</span></span>

1.  <span data-ttu-id="226b2-159">Wählen Sie in **"BETROFFENE RESSOURCEN**  >  **öffnen in"** den Toolnamen aus.</span><span class="sxs-lookup"><span data-stu-id="226b2-159">In **AFFECTED RESOURCES** > **Open in**, select the tool name.</span></span>  <span data-ttu-id="226b2-160">Die betroffene Ressource wird im ausgewählten Tool angezeigt.</span><span class="sxs-lookup"><span data-stu-id="226b2-160">The affected resource is displayed in the selected tool.</span></span>

    :::image type="complex" source="../media/issues-tool-affected-resource-opens-elements-tool.msft.png" alt-text="Wählen Sie ein Tool aus, um eine betroffene Ressource im Tool "Probleme" zu öffnen." lightbox="../media/issues-tool-affected-resource-opens-elements-tool.msft.png":::
       <span data-ttu-id="226b2-162">Wählen Sie ein Tool aus, um eine betroffene Ressource im Tool "Probleme" zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="226b2-162">Select a tool to open an affected resource from within the Issues tool</span></span>
    :::image-end:::

    <span data-ttu-id="226b2-163">Ein erweitertes Problem kann eine **Netzwerkverbindung** aufweisen, um die betroffene Ressource im **Netzwerktool** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="226b2-163">An expanded issue may have a **Network** link, to display the affected resource in the **Network** tool.</span></span>

    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Das Netzwerktool wird geöffnet, wenn Sie eine Netzwerkressourcenverbindung auswählen" lightbox="../media/issues-tab-view-issue.msft.png":::
    <span data-ttu-id="226b2-165">Das **Netzwerktool** wird geöffnet, wenn Sie eine **Netzwerkressourcenverbindung** auswählen</span><span class="sxs-lookup"><span data-stu-id="226b2-165">The **Network** tool opens when you select a **Network** resource link</span></span>
    :::image-end:::


## <a name="open-issues-from-the-dom-tree"></a><span data-ttu-id="226b2-166">Offene Probleme aus der DOM-Struktur</span><span class="sxs-lookup"><span data-stu-id="226b2-166">Open issues from the DOM tree</span></span>

<span data-ttu-id="226b2-167">Wenn einem Element ein Problem zugeordnet ist, zeigt die DOM-Struktur im **Elementtool** eine wellenförmige Unterstreichung unter dem Elementnamen an.</span><span class="sxs-lookup"><span data-stu-id="226b2-167">If an element has an associated issue, the DOM tree in the **Elements** tool shows a wavy underline under the element name.</span></span>  <span data-ttu-id="226b2-168">Sie können das Kontextmenü (Rechtsklick) für das Element öffnen und dann Probleme **anzeigen**auswählen oder `Shift` mit der linken Maustaste auf das Element mit der wellenförmigen Unterstreichung klicken.</span><span class="sxs-lookup"><span data-stu-id="226b2-168">You can open the context menu (right-click) on the element and then select **View issues**, or select `Shift` and left-click the element with the wavy underline.</span></span>

<span data-ttu-id="226b2-169">Führen Sie die folgenden Schritte aus, um ein Problem für Elemente mit wellenförmigen Unterstreichungen in der DOM-Struktur anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="226b2-169">To display an issue for elements with wavy underlines in the DOM tree, perform the following steps.</span></span>

1.  <span data-ttu-id="226b2-170">Öffnen Sie eine Seite, z. B. die [Demoseite,][A11ytestingPagewitherrors]in einer neuen Registerkarte oder einem neuen Fenster.</span><span class="sxs-lookup"><span data-stu-id="226b2-170">Open a page, such as the [demo page][A11ytestingPagewitherrors], in a new tab or window.</span></span>

1.  <span data-ttu-id="226b2-171">Öffnen Sie DevTools, und wählen Sie dann die Registerkarte **"Elemente" aus.**</span><span class="sxs-lookup"><span data-stu-id="226b2-171">Open DevTools and then select the **Elements** tab.</span></span>

1.  <span data-ttu-id="226b2-172">Erweitern Sie in der DOM-Struktur `<body>`  >  `<header>`  >  `<form>` .</span><span class="sxs-lookup"><span data-stu-id="226b2-172">In the DOM tree, expand `<body>` > `<header>` > `<form>`.</span></span>  <span data-ttu-id="226b2-173">Beachten Sie, dass das `<input>` Element eine wellenförmige Unterstreichung aufweist.</span><span class="sxs-lookup"><span data-stu-id="226b2-173">Notice that the `<input>` element has a wavy underline.</span></span>

    :::image type="complex" source="../media/issues-wavy-underlines-dom-tree.msft.png" alt-text="Wavy-underlined issues in the DOM tree in the Elements tool" lightbox="../media/issues-wavy-underlines-dom-tree.msft.png":::
       <span data-ttu-id="226b2-175">Wavy-underlined issues in the **DOM tree** in the **Elements** tool</span><span class="sxs-lookup"><span data-stu-id="226b2-175">Wavy-underlined issues in the **DOM tree** in the **Elements** tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="226b2-176">Zeigen Sie auf das `<input>` Element.</span><span class="sxs-lookup"><span data-stu-id="226b2-176">Hover over the `<input>` element.</span></span>  <span data-ttu-id="226b2-177">Eine QuickInfo zeigt Informationen zu dem Problem an.</span><span class="sxs-lookup"><span data-stu-id="226b2-177">A tooltip displays information about the issue.</span></span>

1.  <span data-ttu-id="226b2-178">Öffnen Sie das Kontextmenü des Elements mit der wellenförmigen Unterstreichung, und wählen Sie dann **Probleme anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="226b2-178">Open the context menu on the element with the wavy underline, and then select **View issues**.</span></span>  <span data-ttu-id="226b2-179">Das Tool **"Probleme"** wird geöffnet und zeigt das Problem an, das diesem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="226b2-179">The **Issues** tool opens and displays the issue that's associated with that element.</span></span>

    :::image type="complex" source="../media/issues-opened-from-dom-tree-wavy-underline.msft.png" alt-text="Details zu Problemen mit einem wellenförmigen unterstrichenen Element in der DOM-Struktur" lightbox="../media/issues-opened-from-dom-tree-wavy-underline.msft.png":::
       <span data-ttu-id="226b2-181">Details zu Problemen mit einem wellenförmigen unterstrichenen Element in der **DOM-Struktur**</span><span class="sxs-lookup"><span data-stu-id="226b2-181">Details about issues on a wavy-underlined element in the **DOM tree**</span></span>
    :::image-end:::


## <a name="see-also"></a><span data-ttu-id="226b2-182">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="226b2-182">See also</span></span>

* [<span data-ttu-id="226b2-183">Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme</span><span class="sxs-lookup"><span data-stu-id="226b2-183">Automatically test a webpage for accessibility issues</span></span>](../accessibility/test-issues-tool.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="226b2-184">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="226b2-184">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]

<!-- links -->
[DevtoolsOpenIndex]: ../open/index.md "Öffnen sie Microsoft Edge DevTools-| Microsoft-Dokumente"
<!-- external links -->
[A11ytestingPagewitherrors]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demoseite für Barrierefreiheitstests | Microsoft-Dokumente"
[DequeAxe]: https://www.deque.com/axe "Axe Tools – Übersicht | Deque"
[MDNCompat]: https://github.com/mdn/browser-compat-data "MDN-Browserkompatibilitätsdaten | GitHub"
[webhintIo]: https://webhint.io "webhint.io"

> [!NOTE]
> <span data-ttu-id="226b2-190">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="226b2-190">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>
> <span data-ttu-id="226b2-191">Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/issues/index) gefunden und von [Sam Dutton][SamDutton] \(Developer Advocate\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="226b2-191">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>
<span data-ttu-id="226b2-192">[ ![ Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="226b2-192">[![Creative Commons License][CCby4Image]][CCA4IL] This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton
