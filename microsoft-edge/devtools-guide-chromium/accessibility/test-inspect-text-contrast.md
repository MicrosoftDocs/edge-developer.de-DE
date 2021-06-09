---
description: Überprüfen Sie den Kontrast der Textfarbe im Standardzustand, indem Sie die Informationsüberlagerung des Tools "Inspect" auf der Seite verwenden, die über einen Abschnitt "Barrierefreiheit" verfügt, der Kontrastinformationen enthält.
title: Überprüfen des Textfarbkontrasts im Standardzustand mithilfe des Inspect-Tools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ade9fd6d685f6f7cea6311b1645a527ece352a38
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597413"
---
# <a name="check-text-color-contrast-in-the-default-state-using-the-inspect-tool"></a><span data-ttu-id="a8e69-104">Überprüfen des Textfarbkontrasts im Standardzustand mithilfe des Inspect-Tools</span><span class="sxs-lookup"><span data-stu-id="a8e69-104">Check text-color contrast in the default state using the Inspect tool</span></span>

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

<span data-ttu-id="a8e69-105">Überprüfen Sie den Kontrast der Textfarbe im Standardzustand, indem Sie das Tool **Inspect** verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8e69-105">Check text color contrast in the default state by using the **Inspect** tool.</span></span>  <span data-ttu-id="a8e69-106">Die Informationsüberlagerung des **Tools "Inspect"** auf der Webseite verfügt über einen Abschnitt **"Barrierefreiheit",** der **Kontrastinformationen** enthält.</span><span class="sxs-lookup"><span data-stu-id="a8e69-106">The **Inspect** tool's information overlay on the webpage has an **Accessibility** section that includes **Contrast** information.</span></span>

<span data-ttu-id="a8e69-107">Führen Sie die folgenden Schritte aus, um den Textfarbkontrast im Standardzustand mithilfe der Informationsüberlagerung des Tools Inspect zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a8e69-107">To check text-color contrast in the default state using the Inspect tool's information overlay, perform the following steps.</span></span>

<!-- Inspect tool -->
<span data-ttu-id="a8e69-108">Für Elemente mit Text zeigt die Informationsüberlagerung des **Inspect-Tools** Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="a8e69-108">For elements that have text, the **Inspect** tool's information overlay shows the following:</span></span>
*  <span data-ttu-id="a8e69-109">Das Kontrastverhältnis zwischen Text und Hintergrundfarben.</span><span class="sxs-lookup"><span data-stu-id="a8e69-109">The contrast ratio of text versus background colors.</span></span>
*  <span data-ttu-id="a8e69-110">Ein grünes Häkchensymbol für Elemente mit genügend Kontrast.</span><span class="sxs-lookup"><span data-stu-id="a8e69-110">A green check mark icon for elements with enough contrast.</span></span>
*  <span data-ttu-id="a8e69-111">Ein gelbes Warnsymbol für Elemente, die nicht über genügend Kontrast verfügen.</span><span class="sxs-lookup"><span data-stu-id="a8e69-111">A yellow alert icon for elements that don't have enough contrast.</span></span>

<span data-ttu-id="a8e69-112">In einigen Fällen wird der Kontrast beeinflusst, indem der Browser auf helles oder dunkles Design festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a8e69-112">In some cases, contrast is affected by setting the browser to light theme or dark theme.</span></span>

<span data-ttu-id="a8e69-113">Auf der Demoseite haben beispielsweise die blauen Links des Navigationsmenüs auf der Seitenleiste genügend Kontrast, aber der grüne Link **"Hunde"** im Abschnitt **"Schenkungsstatus"** hat nicht genügend Kontrast.</span><span class="sxs-lookup"><span data-stu-id="a8e69-113">As an example, on the demo page, the blue links of the sidebar navigation menu have enough contrast, but the green **Dogs** link in the **Donation status** section does not have enough contrast.</span></span>  <span data-ttu-id="a8e69-114">Überprüfen Sie diese \*\*\*\* Elemente wie folgt mithilfe des Inspect-Tools:</span><span class="sxs-lookup"><span data-stu-id="a8e69-114">Review those elements using the **Inspect** tool, as follows:</span></span>

1.  <span data-ttu-id="a8e69-115">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte.  Wählen Sie dann **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a8e69-115">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="a8e69-116">Wählen Sie in der oberen linken Ecke von DevTools die Schaltfläche **"Überprüfen** \( ![ Schaltfläche ](../media/inspect-icon.msft.png) überprüfen\) aus, damit das Symbol hervorgehoben wird (blau).</span><span class="sxs-lookup"><span data-stu-id="a8e69-116">Select the **Inspect** \(![Inspect button](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

1.  <span data-ttu-id="a8e69-117">Zeigen Sie auf der gerenderten Webseite über den blauen **Katzenlink** des Navigationsmenüs in der Seitenleiste.</span><span class="sxs-lookup"><span data-stu-id="a8e69-117">In the rendered webpage, hover over the blue **Cats** link of the sidebar navigation menu.</span></span>  <span data-ttu-id="a8e69-118">Die Informationsüberlagerung des **Tools "Überprüfen"** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8e69-118">The **Inspect** tool's information overlay appears.</span></span>  <span data-ttu-id="a8e69-119">Im Abschnitt **"Barrierefreiheit"** der Informationsüberlagerung wird in der Zeile \*\* Contrast \*\* ein grünes Häkchen angezeigt, das angibt, dass dieses Element über genügend Kontrast zwischen Textfarbe und Hintergrundfarbe verfügt.</span><span class="sxs-lookup"><span data-stu-id="a8e69-119">In the **Accessibility** section of the information overlay, a green checkmark appears on the **Contrast** row, indicating that this element has enough contrast of text color versus background color.</span></span>

    :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Die Menüelemente weisen genügend Kontrast auf, wie im Inspect-Tool dargestellt." lightbox="../media/a11y-testing-enough-contrast.msft.png":::
        <span data-ttu-id="a8e69-121">Die Menüelemente weisen genügend Kontrast auf, wie im Inspect-Tool dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a8e69-121">The menu items have enough contrast, as shown in the Inspect tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="a8e69-122">Zeigen Sie auf der gerenderten Webseite im Abschnitt **"Schenkungsstatus"** auf den Link **"Hunde".**</span><span class="sxs-lookup"><span data-stu-id="a8e69-122">In the rendered webpage, in the **Donation Status** section, hover over the **Dogs** link.</span></span>  <span data-ttu-id="a8e69-123">Die Informationsüberlagerung des **Inspect-Tools** zeigt ein orangefarbenes Ausrufezeichen in der **Zeile "Kontrast",** das angibt, dass dieses Element nicht über genügend Kontrast zwischen Text und Hintergrundfarben verfügt.</span><span class="sxs-lookup"><span data-stu-id="a8e69-123">The **Inspect** tool's information overlay shows an orange exclamation point on the **Contrast** row, indicating that this element doesn't have enough contrast of text versus background colors.</span></span>

    :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Ein Element, das nicht über genügend Kontrast verfügt, wie die Warnung im Inspect-Tool zeigt" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
        <span data-ttu-id="a8e69-125">Ein Element, das nicht über genügend Kontrast verfügt, wie die Warnung im Inspect-Tool zeigt</span><span class="sxs-lookup"><span data-stu-id="a8e69-125">An element that doesn't have enough contrast, as shown by the warning in the Inspect tool</span></span>
    :::image-end:::


## <a name="different-options-to-inspect-text-color-contrast-in-devtools"></a><span data-ttu-id="a8e69-126">Verschiedene Optionen zum Überprüfen des Kontrasts von Textfarben in DevTools</span><span class="sxs-lookup"><span data-stu-id="a8e69-126">Different options to inspect text-color contrast in DevTools</span></span>

<span data-ttu-id="a8e69-127">Verwenden Sie die folgenden DevTools-Features, um den Kontrast von Textfarben zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a8e69-127">Use the following DevTools features to inspect text-color contrast.</span></span>

*  <span data-ttu-id="a8e69-128">Verwenden Sie das **Tool Inspect** (als Informationsüberlagerung auf der Webseite), um zu überprüfen, ob ein einzelnes Seitenelement über genügend Textfarbkontrast verfügt.</span><span class="sxs-lookup"><span data-stu-id="a8e69-128">Use the **Inspect** tool (as an information overlay on the webpage) to check whether an individual page element has enough text-color contrast.</span></span>  <span data-ttu-id="a8e69-129">Die Informationsüberlagerung des **Tools "Inspect"** enthält einen Abschnitt **"Barrierefreiheit",** der über eine Zeile mit **Kontrastinformationen** verfügt.</span><span class="sxs-lookup"><span data-stu-id="a8e69-129">The **Inspect** tool's information overlay includes an **Accessibility** section that has a **Contrast** information row.</span></span>  <span data-ttu-id="a8e69-130">Das **Tool Inspect** zeigt nur Informationen zum Textkontrast für den aktuellen Zustand an.</span><span class="sxs-lookup"><span data-stu-id="a8e69-130">The **Inspect** tool only shows text-contrast information for the current state.</span></span>  <span data-ttu-id="a8e69-131">Dieser Ansatz wird im aktuellen Artikel beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a8e69-131">This approach is described in the current article.</span></span>

*  <span data-ttu-id="a8e69-132">Das Tool **"Probleme"** meldet automatisch alle Farbkontrastprobleme für die gesamte Webseite, wenn Text- und Hintergrundfarbe nicht ausreichend kontrastreich sind.</span><span class="sxs-lookup"><span data-stu-id="a8e69-132">The **Issues** tool automatically reports any color-contrast issues for the entire webpage, when text and background color don't contrast enough.</span></span>  <span data-ttu-id="a8e69-133">Dieser Ansatz wird unter [Überprüfen beschrieben, ob Textfarben genügend Kontrast aufweisen.](test-issues-tool.md#verify-that-text-colors-have-enough-contrast)</span><span class="sxs-lookup"><span data-stu-id="a8e69-133">This approach is described in [Verify that text colors have enough contrast](test-issues-tool.md#verify-that-text-colors-have-enough-contrast).</span></span>

*  <span data-ttu-id="a8e69-134">Emulieren Eines nicht standardmäßigen Zustands, z. B. des `hover` Zustands, mithilfe von **Toggle Element State** im Bereich **Formatvorlagen,** beschrieben unter [Überprüfen der Barrierefreiheit aller Zustände von Elementen.](test-inspect-states.md)</span><span class="sxs-lookup"><span data-stu-id="a8e69-134">Emulate a non-default state, such as the `hover` state, by using **Toggle Element State** in the **Styles** pane, described in [Verify accessibility of all states of elements](test-inspect-states.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="a8e69-135">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="a8e69-135">See also</span></span>

*  [<span data-ttu-id="a8e69-136">Überprüfen Sie die Barrierefreiheit aller Zustände von Elementen</span><span class="sxs-lookup"><span data-stu-id="a8e69-136">Verify accessibility of all states of elements</span></span>][DevtoolsAccessibilityTestInspectStates]
*  [<span data-ttu-id="a8e69-137">Verwenden Sie das Inspect-Tool, um Barrierefreiheitsprobleme zu erkennen, indem Sie auf die Webseite zeigen</span><span class="sxs-lookup"><span data-stu-id="a8e69-137">Use the Inspect tool to detect accessibility issues by hovering over the webpage</span></span>](test-inspect-tool.md)
*  [<span data-ttu-id="a8e69-138">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="a8e69-138">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a8e69-139">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a8e69-139">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityTestInspectStates]: test-inspect-states.md "Überprüfen der Barrierefreiheit aller Zustände von Elementen | Microsoft-Dokumente"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
