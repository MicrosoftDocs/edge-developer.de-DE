---
description: Überprüfen der Barrierefreiheitsstruktur auf Tastatur- und Sprachausgabeunterstützung.
title: Überprüfen Sie die Barrierefreiheitsstruktur auf Tastatur- und Sprachausgabeunterstützung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 0ab5e5609485505d1ad5fa6e2fffced9af25edcb
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597462"
---
# <a name="check-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a><span data-ttu-id="c9ecc-104">Überprüfen Sie die Barrierefreiheitsstruktur auf Tastatur- und Sprachausgabeunterstützung</span><span class="sxs-lookup"><span data-stu-id="c9ecc-104">Check the Accessibility Tree for keyboard and screen reader support</span></span>

<!-- Accessibility tab: Accessibility Tree -->

<span data-ttu-id="c9ecc-105">Mehrere DevTools-Features überprüfen auf Tastatur- und Sprachausgabeunterstützung.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-105">Several DevTools features check for keyboard and screen reader support.</span></span>  <span data-ttu-id="c9ecc-106">Die Verwendung des **Inspect-Tools** zum Überprüfen der Barrierefreiheit der einzelnen Seitenelemente kann ziemlich zeitaufwändig werden.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-106">Using the **Inspect** tool to check the accessibility of each page element individually can become pretty time-consuming.</span></span>  <span data-ttu-id="c9ecc-107">Eine alternative Möglichkeit zum Überprüfen einer Webseite ist die Verwendung der **Barrierefreiheitsstruktur.**</span><span class="sxs-lookup"><span data-stu-id="c9ecc-107">An alternative way to check a webpage is to use the **Accessibility Tree**.</span></span>  <span data-ttu-id="c9ecc-108">Die **Barrierefreiheitsstruktur** gibt an, welche Informationen die Seite für Hilfstechnologien wie Bildschirmleseprogramme bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-108">The **Accessibility Tree** indicates what information the page provides to assistive technology such as screen readers.</span></span>

<span data-ttu-id="c9ecc-109">Die **Barrierefreiheitsstruktur** ist eine Teilmenge der DOM-Struktur, die Elemente aus der DOM-Struktur enthält, die relevant und nützlich sind, um den Inhalt einer Seite in einer Sprachausgabe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-109">The **Accessibility Tree** is a subset of the DOM tree, which contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  <span data-ttu-id="c9ecc-110">Die **Barrierefreiheitsstruktur** befindet sich auf der Registerkarte **"Barrierefreiheit"** **des** Elements-Tools (in der Nähe der Registerkarte **"Formatvorlagen").**</span><span class="sxs-lookup"><span data-stu-id="c9ecc-110">The **Accessibility Tree** is in the **Accessibility** tab of the **Elements** tool (near the **Styles** tab).</span></span>


<span data-ttu-id="c9ecc-111">So erkunden Sie die Verwendung der Barrierefreiheitsstruktur mit der Demoseite:</span><span class="sxs-lookup"><span data-stu-id="c9ecc-111">To explore using the Accessibility Tree with the demo page:</span></span>

1.  <span data-ttu-id="c9ecc-112">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte.  Wählen Sie dann **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-112">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="c9ecc-113">Wählen Sie in der oberen linken Ecke von DevTools die Schaltfläche **"Überprüfen** \( ![ das Symbol ](../media/inspect-icon.msft.png) \) aus, damit die Schaltfläche hervorgehoben ist (blau).</span><span class="sxs-lookup"><span data-stu-id="c9ecc-113">Select the **Inspect** \(![the Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="c9ecc-114">Zeigen Sie auf der gerenderten Webseite im Abschnitt **"Schenkung"** auf die Schaltfläche **100.**</span><span class="sxs-lookup"><span data-stu-id="c9ecc-114">In the rendered webpage, in the **Donation** section, hover over the **100** button.</span></span>  <span data-ttu-id="c9ecc-115">Die \*\*\*\* Überprüfungstoolüberlagerung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-115">The **Inspect** tool overlay appears.</span></span>

1.  <span data-ttu-id="c9ecc-116">Wählen Sie in der gerenderten Webseite die Schaltfläche **100** aus.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-116">In the rendered webpage, select the **100** button.</span></span>  <span data-ttu-id="c9ecc-117">In DevTools wird das **Elementtool** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-117">In DevTools, the **Elements** tool is displayed.</span></span>  <span data-ttu-id="c9ecc-118">Die DOM-Struktur zeigt das `div` Element für die Schaltfläche **100** an.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-118">The DOM tree shows the `div` element for the **100** button.</span></span>  <span data-ttu-id="c9ecc-119">Im Bereich **"Formatvorlagen"** werden die CSS-Einstellungen für das Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-119">The **Styles** pane shows the CSS settings for the element.</span></span>

1.  <span data-ttu-id="c9ecc-120">Wählen Sie rechts neben der Registerkarte **"Formatvorlagen"** die Registerkarte **"Barrierefreiheit"** aus.  Die **Barrierefreiheitsstruktur** für das Element wird angezeigt und erweitert.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-120">To the right of the **Styles** tab, select the **Accessibility** tab.  The **Accessibility Tree** for the element is displayed, and is expanded.</span></span>

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Schaltfläche "Schenkungsformular" im Tool "Barrierefreiheitsstruktur"" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    <span data-ttu-id="c9ecc-122">Schaltfläche "Schenkungsformular" im Tool "Barrierefreiheitsstruktur"</span><span class="sxs-lookup"><span data-stu-id="c9ecc-122">Donation form button in the Accessibility Tree tool</span></span>
:::image-end:::

<span data-ttu-id="c9ecc-123">Jedes Element in der Struktur, das keinen Namen hat oder eine Rolle `generic` hat (z. B. das `div` Element), ist ein Problem, da dieses Element für Tastaturbenutzer oder Benutzer, die Hilfstechnologien verwenden, nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c9ecc-123">Any element in the tree that doesn't have a name, or has a role of `generic` (such as the `div` element) is a problem, because that element won't be available to keyboard users, or to users who are using assistive technology.</span></span>


## <a name="see-also"></a><span data-ttu-id="c9ecc-124">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="c9ecc-124">See also</span></span>

*  [<span data-ttu-id="c9ecc-125">Anzeigen der Position eines Elements in der Barrierefreiheitsstruktur</span><span class="sxs-lookup"><span data-stu-id="c9ecc-125">View the position of an element in the Accessibility Tree</span></span>][DevtoolsAccessibilityAccessibilityTabViewTree]
*  [<span data-ttu-id="c9ecc-126">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="c9ecc-126">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c9ecc-127">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="c9ecc-127">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevtoolsAccessibilityAccessibilityTabViewTree]: accessibility-tab.md#view-the-position-of-an-element-in-the-accessibility-tree "Anzeigen der Position eines Elements in der Barrierefreiheitsstruktur – Testen der Barrierefreiheit mithilfe der Registerkarte &quot;Barrierefreiheit&quot; | Microsoft-Dokumente"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
