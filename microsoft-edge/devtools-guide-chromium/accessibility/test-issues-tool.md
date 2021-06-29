---
description: Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme mithilfe des Abschnitts "Barrierefreiheit" des Tools "Probleme".
title: Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 1cba9db1744235dfbfd2a007e33d1101452aab31
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624738"
---
# <a name="automatically-test-a-webpage-for-accessibility-issues"></a><span data-ttu-id="303c5-104">Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme</span><span class="sxs-lookup"><span data-stu-id="303c5-104">Automatically test a webpage for accessibility issues</span></span>

<span data-ttu-id="303c5-105">Das Tool **"Probleme"** enthält einen Abschnitt **zur Barrierefreiheit,** in dem Automatisch Probleme gemeldet werden, z. B. fehlender alternativer Text auf Bildern, fehlende Beschriftungen in Formularfeldern und unzureichender Kontrast von Textfarben.</span><span class="sxs-lookup"><span data-stu-id="303c5-105">The **Issues** tool includes an **Accessibility** section that automatically reports issues such as missing alternative text on images, missing labels on form fields, and insufficient contrast of text colors.</span></span>  <span data-ttu-id="303c5-106">Das Tool **"Probleme"** befindet sich in der **Schublade** am unteren Rand von DevTools.</span><span class="sxs-lookup"><span data-stu-id="303c5-106">The **Issues** tool is within the **Drawer** at the bottom of DevTools.</span></span>  <span data-ttu-id="303c5-107">In diesem Artikel wird die Demowebseite zum Testen der Barrierefreiheit verwendet, um den Abschnitt **"Barrierefreiheit"** des **Tools "Probleme"** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="303c5-107">This article uses the accessibility-testing demo webpage to step through using the **Accessibility** section of the **Issues** tool.</span></span>

<span data-ttu-id="303c5-108">Es gibt mehrere Möglichkeiten, das **Problemtool** zu öffnen, z. B.:</span><span class="sxs-lookup"><span data-stu-id="303c5-108">There are several ways to open the **Issues** tool, such as:</span></span>
*  <span data-ttu-id="303c5-109">Wählen Sie den **Problemindikator** \( ![ Problemzähler ](../media/issues-counter-icon.msft.png) \) in der oberen rechten Ecke von DevTools aus.</span><span class="sxs-lookup"><span data-stu-id="303c5-109">Select the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) in the upper right of DevTools.</span></span>
*  <span data-ttu-id="303c5-110">Klicken Sie **im** Elementtool in der DOM-Struktur **umschalten+auf** eine wellenförmige Unterstreichung für ein Element.</span><span class="sxs-lookup"><span data-stu-id="303c5-110">In the **Elements** tool, in the DOM tree, **Shift+click** a wavy underline on an element.</span></span>
*  <span data-ttu-id="303c5-111">Geben Sie im **Befehlsmenü** `issues` ein, und wählen Sie dann **Probleme anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="303c5-111">In the **Command Menu**, type `issues`, and then select **Show Issues**.</span></span>


## <a name="view-the-accessibility-section-of-the-issues-tool"></a><span data-ttu-id="303c5-112">Anzeigen des Abschnitts "Barrierefreiheit" des Tools "Probleme"</span><span class="sxs-lookup"><span data-stu-id="303c5-112">View the Accessibility section of the Issues tool</span></span>

1.  <span data-ttu-id="303c5-113">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="303c5-113">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>  <span data-ttu-id="303c5-114">In der oberen rechten Ecke wird der **Problemindikator** \( ![ Problemzähler ](../media/issues-counter-icon.msft.png) \) als Symbol für die Sprachblase zusammen mit der Anzahl der automatisch erkannten Probleme angezeigt.</span><span class="sxs-lookup"><span data-stu-id="303c5-114">In the upper right, the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\) appears, as a speech-bubble icon along with the number of automatically detected issues.</span></span>  <span data-ttu-id="303c5-115">Möglicherweise wird in Ihrem Browser eine andere Nummer angezeigt, und die Nummer wird möglicherweise aktualisiert, wenn Sie DevTools verwenden.</span><span class="sxs-lookup"><span data-stu-id="303c5-115">A different number might appear in your browser, and the number might update as you use DevTools.</span></span>

    :::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="Der Problemindikator in DevTools, der angibt, wie viele Probleme im aktuellen Dokument vorhanden sind" lightbox="../media/a11y-testing-issues-tracker.msft.png":::
        <span data-ttu-id="303c5-117">Der **Problemindikator** in DevTools, der angibt, wie viele Probleme im aktuellen Dokument vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="303c5-117">The **Issues counter** in DevTools, indicating how many problems there are in the current document</span></span>
    :::image-end:::

1.  <span data-ttu-id="303c5-118">Wählen Sie den **Problemindikator aus.**</span><span class="sxs-lookup"><span data-stu-id="303c5-118">Select the **Issues counter**.</span></span>  <span data-ttu-id="303c5-119">Das Tool **"Probleme"** wird in der **Schublade** am unteren Rand von DevTools geöffnet.</span><span class="sxs-lookup"><span data-stu-id="303c5-119">The **Issues** tool opens, in the **Drawer** at the bottom of DevTools.</span></span>

    :::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Warnungen zur Barrierefreiheit, die im Tool "Probleme" angezeigt werden" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
        <span data-ttu-id="303c5-121">Warnungen zur Barrierefreiheit, die im Tool "Probleme" angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="303c5-121">Accessibility warnings displayed in the Issues tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="303c5-122">Erweitern Sie auf der Registerkarte **"Probleme"** den Abschnitt **"Barrierefreiheit".**</span><span class="sxs-lookup"><span data-stu-id="303c5-122">On the **Issues** tab, expand the **Accessibility** section.</span></span>


## <a name="verify-that-input-fields-have-labels"></a><span data-ttu-id="303c5-123">Überprüfen, ob Eingabefelder Bezeichnungen aufweisen</span><span class="sxs-lookup"><span data-stu-id="303c5-123">Verify that input fields have labels</span></span>

<span data-ttu-id="303c5-124">Um zu überprüfen, ob mit Eingabefeldern Bezeichnungen verbunden sind, verwenden Sie das Tool **"Probleme",** das automatisch die gesamte Webseite überprüft und dieses Problem im Abschnitt **"Barrierefreiheit"** meldet.</span><span class="sxs-lookup"><span data-stu-id="303c5-124">To check whether input fields have labels connected to them, use the **Issues** tool, which automatically checks the entire webpage and reports this issue in the **Accessibility** section.</span></span>

1.  <span data-ttu-id="303c5-125">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="303c5-125">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="303c5-126">Wählen Sie oben rechts den **Problemindikator** \( ![ Problemzähler ](../media/issues-counter-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="303c5-126">In the upper right, select the **Issues counter** \(![Issues counter](../media/issues-counter-icon.msft.png)\).</span></span>  <span data-ttu-id="303c5-127">Das Tool **"Probleme"** wird in der **Schublade** am unteren Rand von DevTools geöffnet.</span><span class="sxs-lookup"><span data-stu-id="303c5-127">The **Issues** tool opens, in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="303c5-128">Erweitern Sie auf der Registerkarte **"Probleme"** den Abschnitt **"Barrierefreiheit".**</span><span class="sxs-lookup"><span data-stu-id="303c5-128">On the **Issues** tab, expand the **Accessibility** section.</span></span>

1.  <span data-ttu-id="303c5-129">Erweitern Sie die **Warnung** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute` .</span><span class="sxs-lookup"><span data-stu-id="303c5-129">Expand the **Warning** `Form elements must have labels: Element has no title attribute Element has no placeholder attribute`.</span></span>

1. <span data-ttu-id="303c5-130">Wählen Sie den Link **"In Elementen öffnen"** aus.</span><span class="sxs-lookup"><span data-stu-id="303c5-130">Select the **Open in Elements** link.</span></span>

    :::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Elementtool, das den problematischen HTML-Code zeigt, nachdem der Link im Tool "Probleme" ausgewählt wurde" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
        <span data-ttu-id="303c5-132">Elementtool, das den problematischen HTML-Code zeigt, nachdem der Link im Tool **"Probleme"** ausgewählt wurde</span><span class="sxs-lookup"><span data-stu-id="303c5-132">Elements tool showing the problematic HTML after selecting the link in the **Issues** tool</span></span> :::image-end:::

    <span data-ttu-id="303c5-133">Das \*\*\*\* Elementtool wird geöffnet, wobei das Element in der DOM-Struktur hervorgehoben ist.</span><span class="sxs-lookup"><span data-stu-id="303c5-133">The **Elements** tool opens, with the element highlighted in the DOM tree.</span></span>  <span data-ttu-id="303c5-134">Im Bereich **"Formatvorlagen"** werden die angewendeten CSS-Regeln für das Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="303c5-134">The **Styles** pane displays the applied CSS rules for the element.</span></span>  <span data-ttu-id="303c5-135">Der folgende Code wird nun angezeigt.</span><span class="sxs-lookup"><span data-stu-id="303c5-135">The following code is now displayed.</span></span>

    ```html
    <label>Search</label>
    <input type="search">
    <input type="submit" value="go">
    ```

    <span data-ttu-id="303c5-136">Im obigen Code wird das `label` Element falsch verwendet, da es keine Verbindung zwischen dem `label` Element und einem bestimmten Element `input` gibt.</span><span class="sxs-lookup"><span data-stu-id="303c5-136">In the above code, the `label` element is used incorrectly, because there is no connection between the `label` element and a particular `input` element.</span></span>  <span data-ttu-id="303c5-137">Verwenden Sie eine der folgenden Optionen, um das `label` Element mit einem bestimmten Element zu `input` verbinden.</span><span class="sxs-lookup"><span data-stu-id="303c5-137">To connect the `label` element to a specific `input` element, use any of the following options.</span></span>
    *   <span data-ttu-id="303c5-138">Schachteln Sie das `input` Element innerhalb des `label` Elements.</span><span class="sxs-lookup"><span data-stu-id="303c5-138">Nest the `input` element within the `label` element.</span></span>
    *   <span data-ttu-id="303c5-139">Fügen Sie im `label` Element ein Attribut hinzu, das mit einem `for` Attribut des Elements `id` `input` übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="303c5-139">In the `label` element, add a `for` attribute that matches an `id` attribute of the `input` element.</span></span>

    <span data-ttu-id="303c5-140">Es gibt auch eine andere Möglichkeit, auf fehlende Verbindungen zwischen Elementen zu testen.</span><span class="sxs-lookup"><span data-stu-id="303c5-140">There's also another way to test for lack of connections between elements.</span></span> <span data-ttu-id="303c5-141">Wählen Sie im Tool **"Elemente"** das `<label>Search</label>` Element in der DOM-Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="303c5-141">In the **Elements** tool, select the `<label>Search</label>` element in the DOM tree.</span></span>  <span data-ttu-id="303c5-142">Beachten Sie auf der Webseite, dass der Fokus nur auf der **Beschriftung "Suchen"** und nicht auf dem Eingabetextfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="303c5-142">On the webpage, notice that focus only appears on the **Search** label, and not the input textbox.</span></span>  <span data-ttu-id="303c5-143">Bei der richtigen Implementierung würden der Fokus auf das `search` Eingabetextfeld und die **Suchbeschriftung** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="303c5-143">The correct implementation would put focus on the `search` input textbox and the **Search** label.</span></span>

1.  <span data-ttu-id="303c5-144">Wählen Sie als Beispiel für eine korrekte Verbindung die Bezeichnung **"Andere"** auf dem Formular für die Gabe aus.</span><span class="sxs-lookup"><span data-stu-id="303c5-144">As an example of a correct connection, select the **Other** label on the donation form.</span></span>  <span data-ttu-id="303c5-145">Ein Fokusindikatorfeld wird im Eingabetextfeld neben \*\*\*\* der Beschriftung Other korrekt angezeigt, da Übereinstimmungs- und Attributwerte vorhanden `for` `id` sind.</span><span class="sxs-lookup"><span data-stu-id="303c5-145">A focus-indicator box correctly appears on the input textbox next to the **Other** label, because there are matching `for` and `id` attribute values.</span></span>

1.  <span data-ttu-id="303c5-146">Wählen Sie im **Tool "Probleme"** die Option **"Weitere Informationen"** aus, um mehr über das Problem zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="303c5-146">In the **Issues tool**, select **Further reading** to learn more about the issue.</span></span>  <span data-ttu-id="303c5-147">Um den Link auf einer neuen Registerkarte zu öffnen, klicken Sie **mit strg** + **auf** den Link auf Windows/Linux, oder **klicken**Sie auf den Link unter + \*\*\*\* macOS.</span><span class="sxs-lookup"><span data-stu-id="303c5-147">To open the link in a new tab, **Ctrl**+**click** the link on Windows/Linux, or **Command**+**click** the link on macOS.</span></span>

    :::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Link auf der Registerkarte "Probleme" mit detaillierteren Informationen zu dem Problem" lightbox="../media/a11y-testing-more-information-links.msft.png":::
        <span data-ttu-id="303c5-149">Link auf der Registerkarte **"Probleme"** mit detaillierteren Informationen zu dem Problem</span><span class="sxs-lookup"><span data-stu-id="303c5-149">Link on the **Issues** tab pointing to more in-depth information about the issue</span></span>
    :::image-end:::


## <a name="verify-that-images-have-alt-text"></a><span data-ttu-id="303c5-150">Stellen Sie sicher, dass Bilder über alt-Text verfügen</span><span class="sxs-lookup"><span data-stu-id="303c5-150">Verify that images have alt text</span></span>

<span data-ttu-id="303c5-151">Für grundlegende Barrierefreiheitstests muss sichergestellt werden, dass für Bilder alternativer Text (auch _als Alttext_bezeichnet) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="303c5-151">Basic accessibility testing requires making sure alternative text (also called _alt text_) is provided for images.</span></span>

<span data-ttu-id="303c5-152">Verwenden Sie das Tool **"Probleme",** das über einen Abschnitt **"Barrierefreiheit"** verfügt, um automatisch zu überprüfen, ob alternativer Text für Bilder bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="303c5-152">To automatically check whether alt text is provided for images, use the **Issues** tool, which has an **Accessibility** section.</span></span>  <span data-ttu-id="303c5-153">Das **Tool "Probleme"** befindet sich in der **Schublade** am unteren Rand von DevTools.</span><span class="sxs-lookup"><span data-stu-id="303c5-153">The **Issues** tool is located in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="303c5-154">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="303c5-154">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="303c5-155">Um das Tool **"Probleme"** zu öffnen, wählen Sie den **Problemindikator** in der oberen rechten Ecke von DevTools aus.</span><span class="sxs-lookup"><span data-stu-id="303c5-155">To open the **Issues** tool, select the **Issues** counter in the upper right of DevTools.</span></span>

1.  <span data-ttu-id="303c5-156">Erweitern Sie auf der Registerkarte **"Probleme"** die `Images must have alternate text: Element has no title attribute` Warnung.</span><span class="sxs-lookup"><span data-stu-id="303c5-156">On the **Issues** tab, expand the warning `Images must have alternate text: Element has no title attribute`.</span></span>  <span data-ttu-id="303c5-157">Es gibt vier Instanzen von Bildern, für die kein alternativer Text vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="303c5-157">There are four instances of images that lack alt text.</span></span>

    :::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="Das Tool "Probleme", das Bilder meldet, für die alternativer Text fehlt" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
        <span data-ttu-id="303c5-159">Das Tool "Probleme", das Bilder meldet, für die alternativer Text fehlt</span><span class="sxs-lookup"><span data-stu-id="303c5-159">The Issues tool reporting images that are missing alternative text</span></span>
    :::image-end:::

<span data-ttu-id="303c5-160">Um weitere Informationen zu erhalten, müssen Sie zu ["Bilder" alternativen Text haben.](https://dequeuniversity.com/rules/axe/4.1/image-alt)</span><span class="sxs-lookup"><span data-stu-id="303c5-160">For more information, navigate to [Images must have alternate text](https://dequeuniversity.com/rules/axe/4.1/image-alt).</span></span>


## <a name="verify-that-text-colors-have-enough-contrast"></a><span data-ttu-id="303c5-161">Sicherstellen, dass Textfarben über genügend Kontrast verfügen</span><span class="sxs-lookup"><span data-stu-id="303c5-161">Verify that text colors have enough contrast</span></span>

<span data-ttu-id="303c5-162">Um automatisch zu überprüfen, ob Textfarben über genügend Kontrast verfügen, verwenden Sie das Tool **"Probleme",** das über einen Abschnitt **"Barrierefreiheit"** verfügt.</span><span class="sxs-lookup"><span data-stu-id="303c5-162">To automatically check whether text colors have enough contrast, use the **Issues** tool, which has an **Accessibility** section.</span></span>  <span data-ttu-id="303c5-163">Das **Tool "Probleme"** befindet sich in der **Schublade** am unteren Rand von DevTools.</span><span class="sxs-lookup"><span data-stu-id="303c5-163">The **Issues** tool is located in the **Drawer** at the bottom of DevTools.</span></span>

1.  <span data-ttu-id="303c5-164">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="303c5-164">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="303c5-165">Um das Tool **"Probleme"** zu öffnen, wählen Sie den **Problemindikator** in der oberen rechten Ecke von DevTools aus.</span><span class="sxs-lookup"><span data-stu-id="303c5-165">To open the **Issues** tool, select the **Issues** counter in the upper right of DevTools.</span></span>  <span data-ttu-id="303c5-166">Möglicherweise erhalten Sie Warnungen, dass zwei Elemente auf der Demowebseite nicht über genügend Kontrast verfügen.</span><span class="sxs-lookup"><span data-stu-id="303c5-166">You may receive warnings that two elements on the demo webpage don't have enough contrast.</span></span>

    :::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Im Tool "Probleme" gemeldete Kontrastprobleme" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
        <span data-ttu-id="303c5-168">Im Tool "Probleme" gemeldete Kontrastprobleme</span><span class="sxs-lookup"><span data-stu-id="303c5-168">Contrast problems reported in the Issues tool</span></span>
    :::image-end:::

1.  <span data-ttu-id="303c5-169">Abhängig von Ihren Einstellungen wird auf der Registerkarte **"Probleme"** möglicherweise eine Warnung angezeigt, z. B. wenn **Benutzer aufgrund eines unzureichenden Farbkontrasts Probleme**beim Lesen von Textinhalten haben.</span><span class="sxs-lookup"><span data-stu-id="303c5-169">Depending on your settings, the **Issues** tab might have a warning like **Users may have difficulties reading text content due to insufficient color contrast**.</span></span>   <span data-ttu-id="303c5-170">Sie können diese Warnung erweitern und dann betroffene **Ressourcen**erweitern.</span><span class="sxs-lookup"><span data-stu-id="303c5-170">You can expand that warning, and then expand **Affected resources**.</span></span>  <span data-ttu-id="303c5-171">Eine Liste von Elementen wird mit einer Liste von Elementen angezeigt, die nicht über genügend Kontrast verfügen.</span><span class="sxs-lookup"><span data-stu-id="303c5-171">A list of elements appears with a list of elements that don't have enough contrast.</span></span>


1.  <span data-ttu-id="303c5-172">Wählen Sie das `li.high` Element aus.</span><span class="sxs-lookup"><span data-stu-id="303c5-172">Select the `li.high` element.</span></span>  <span data-ttu-id="303c5-173">Auf der gerenderten Webseite wird der Link **"Hunde"** im Abschnitt \*\* Hebung \*\* hervorgehoben, wobei eine kleine Informationsüberlagerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="303c5-173">In the rendered webpage, the **Dogs** link in the **Donate** section is highlighted, displaying a small information overlay.</span></span>  <span data-ttu-id="303c5-174">Dies ist die gleiche Überlagerung, die angezeigt wird, wenn Sie mit dem Mauszeiger über ein Element in der DOM-Struktur im **Elementtool** zeigen.</span><span class="sxs-lookup"><span data-stu-id="303c5-174">This is the same overlay that appears when you hover over an element in the DOM tree in the **Elements** tool.</span></span>

    :::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Element auf der Webseite, das nach dem Auswählen eines Links im Abschnitt "Betroffene Ressourcen" hervorgehoben wurde" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
        <span data-ttu-id="303c5-176">Element auf der Webseite, das nach dem Auswählen eines Links im Abschnitt **"Betroffene Ressourcen"** hervorgehoben wurde</span><span class="sxs-lookup"><span data-stu-id="303c5-176">Element in the webpage highlighted after selecting a link in the **Affected Resources** section</span></span>
    :::image-end:::


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a><span data-ttu-id="303c5-177">Wellenförmige Unterstreichungen in der DOM-Struktur weisen auf automatisch erkannte Probleme hin</span><span class="sxs-lookup"><span data-stu-id="303c5-177">Wavy underlines in the DOM tree indicate automatically detected issues</span></span> 

<span data-ttu-id="303c5-178">Die DOM-Struktur im **Elementtool** kennzeichnet Probleme direkt im HTML-Code mit wellenförmigen Unterstreichungen.</span><span class="sxs-lookup"><span data-stu-id="303c5-178">The DOM tree in the **Elements** tool flags issues directly in the HTML with wavy underlines.</span></span>  <span data-ttu-id="303c5-179">Diese Probleme werden vom **Tool "Probleme"** gemeldet.</span><span class="sxs-lookup"><span data-stu-id="303c5-179">These issues are reported by the **Issues** tool.</span></span>  <span data-ttu-id="303c5-180">Wenn Sie **umschalten und auf** ein Beliebiges Element mit wellenförmiger Unterstreichung klicken, wird das **Tool "Probleme"** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="303c5-180">When you **Shift+click** any element with a wavy underline, the **Issues tool** is displayed.</span></span>

1.  <span data-ttu-id="303c5-181">Klicken Sie im Tool **"Elemente"** in der DOM-Struktur **umschalten+auf** das `<input type="search">` Element, das eine wellenförmige Linie unter `input` sich hat.</span><span class="sxs-lookup"><span data-stu-id="303c5-181">In the **Elements** tool, in the DOM tree, **Shift+click** the element `<input type="search">`, which has a wavy line under `input`.</span></span>  <span data-ttu-id="303c5-182">Das **Tool "Probleme"** wird angezeigt und zeigt das Problem für dieses Element an.</span><span class="sxs-lookup"><span data-stu-id="303c5-182">The **Issues tool** is displayed, and shows the issue for that element.</span></span>

    :::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Ein Element mit einer wellenförmigen Unterstreichung in der DOM-Ansicht hat ein Problem" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
        <span data-ttu-id="303c5-184">Ein Element mit einer wellenförmigen Unterstreichung in der DOM-Ansicht hat ein Problem</span><span class="sxs-lookup"><span data-stu-id="303c5-184">An element that has a wavy underline in the DOM view has an issue</span></span>
    :::image-end:::


## <a name="see-also"></a><span data-ttu-id="303c5-185">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="303c5-185">See also</span></span>

*  [<span data-ttu-id="303c5-186">Suchen und Beheben von Problemen mit dem Tool "Probleme"</span><span class="sxs-lookup"><span data-stu-id="303c5-186">Find and fix problems using the Issues tool</span></span>][DevToolsIssuesTool]
*  [<span data-ttu-id="303c5-187">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="303c5-187">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="303c5-188">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="303c5-188">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsIssuesTool]: ../issues/index.md "Suchen und Beheben von Problemen mithilfe des Tools &quot;Probleme&quot; | Microsoft-Dokumente"
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
