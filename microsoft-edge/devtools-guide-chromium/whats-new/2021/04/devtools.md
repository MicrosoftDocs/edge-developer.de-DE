---
description: Wavy underlines highlight code issues in the Elements tool, Service worker update timeline, and more.
title: Neuigkeiten in DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 69fcd29f9b4cae9ec290798b767fbe54793cb2fd
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624780"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-91"></a><span data-ttu-id="5e443-104">Neuigkeiten in DevTools (Microsoft Edge 91)</span><span class="sxs-lookup"><span data-stu-id="5e443-104">What's New In DevTools (Microsoft Edge 91)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a><span data-ttu-id="5e443-105">Wellenförmige Unterstreichungen heben Codeprobleme und Verbesserungen im Elementtool hervor</span><span class="sxs-lookup"><span data-stu-id="5e443-105">Wavy underlines highlight code issues and improvements in Elements tool</span></span>  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

<span data-ttu-id="5e443-106">In den meisten modernen IDEs weisen wellenförmige Unterstreichungen unter Text auf Syntaxfehler hin.</span><span class="sxs-lookup"><span data-stu-id="5e443-106">In most modern IDEs, wavy underlines under text indicate syntax errors.</span></span>   <span data-ttu-id="5e443-107">In Microsoft Edge Version 91 oder höher werden wellenförmige Unterstreichungen in der **DOM-Ansicht** des **Elements-Tools** unter HTML angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-107">In Microsoft Edge version 91 or later, wavy underlines display under HTML in the **DOM** view of the **Elements** tool.</span></span>  <span data-ttu-id="5e443-108">Die wellenförmigen Unterstreichungen deuten auf Codeprobleme und Vorschläge im Zusammenhang mit Barrierefreiheit, Kompatibilität, Leistung usw. hin.</span><span class="sxs-lookup"><span data-stu-id="5e443-108">The wavy underlines indicate code issues and suggestions related to accessibility, compatibility, performance, and so on.</span></span>  <span data-ttu-id="5e443-109">For more information about how to review and edit issues, navigate to [Find and fix problems using the Issues tool][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="5e443-109">For more information about how to review and edit issues, navigate to [Find and fix problems using the Issues tool][DevtoolsIssuesIndex].</span></span>  

<span data-ttu-id="5e443-110">Führen Sie eine der folgenden Aktionen aus, um das Tool **"Probleme"** zu öffnen und mehr über das Problem und dessen Behebung zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="5e443-110">To open the **Issues** tool and learn more about the issue and how to fix it, complete one of the following actions.</span></span>  

*   <span data-ttu-id="5e443-111">Wählen Sie "Halten" `Shift` aus, und wählen Sie dann eine beliebige wellenförmige Unterstreichung aus.</span><span class="sxs-lookup"><span data-stu-id="5e443-111">Select and hold `Shift`, and then choose any wavy underline.</span></span>  
*   <span data-ttu-id="5e443-112">Führen Sie die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="5e443-112">Complete the following actions.</span></span>  
    1.  <span data-ttu-id="5e443-113">Zeigen Sie auf eine beliebige wellenförmige Unterstreichung.</span><span class="sxs-lookup"><span data-stu-id="5e443-113">Hover on any wavy underline.</span></span>  
    1.  <span data-ttu-id="5e443-114">Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).</span><span class="sxs-lookup"><span data-stu-id="5e443-114">Open the contextual menu \(right-click\).</span></span>  
    1.  <span data-ttu-id="5e443-115">Wählen Sie **"In Problemen anzeigen"** aus.</span><span class="sxs-lookup"><span data-stu-id="5e443-115">Choose **Show in Issues**.</span></span>  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Auswählen des unterstrichenen Fehlers im Elementtool" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         <span data-ttu-id="5e443-117">Auswählen des unterstrichenen Fehlers im **Elementtool**</span><span class="sxs-lookup"><span data-stu-id="5e443-117">Choose the underlined error in the **Elements** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Anzeigen von Fehlerdetails im Tool "Probleme"" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         <span data-ttu-id="5e443-119">Anzeigen von Fehlerdetails im **Tool "Probleme"**</span><span class="sxs-lookup"><span data-stu-id="5e443-119">Display error details in the **Issues** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="5e443-120">Mehr über DevTools mit informativen QuickInfos erfahren</span><span class="sxs-lookup"><span data-stu-id="5e443-120">Learn about DevTools with informative tooltips</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

<span data-ttu-id="5e443-121">Die DevTools-QuickInfos-Funktion hilft Ihnen, sich über alle verschiedenen Tools und Bereiche in DevTools zu informieren.</span><span class="sxs-lookup"><span data-stu-id="5e443-121">The DevTools Tooltips feature helps you learn about all the different tools and panes in DevTools.</span></span>  <span data-ttu-id="5e443-122">Um QuickInfos zu deaktivieren, wählen Sie `Esc` .</span><span class="sxs-lookup"><span data-stu-id="5e443-122">To turn off Tooltips, select `Esc`.</span></span>  <span data-ttu-id="5e443-123">Führen Sie eine der folgenden Aktionen aus, um QuickInfos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5e443-123">To turn on Tooltips, complete one of the following actions.</span></span>  

*   <span data-ttu-id="5e443-124">Wählen Sie `Ctrl` + `Shift` + `H` \(Windows/Linux\) oder `Cmd` + `Shift` + `H` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="5e443-124">Select `Ctrl`+`Shift`+`H` \(Windows/Linux\) or `Cmd`+`Shift`+`H` \(macOS\).</span></span>  
*   <span data-ttu-id="5e443-125">[Öffnen Sie das Befehlsmenü,][DevtoolsCommandMenuIndexOpenCommandMenu] und geben Sie dann `tooltips` .</span><span class="sxs-lookup"><span data-stu-id="5e443-125">[Open the Command Menu][DevtoolsCommandMenuIndexOpenCommandMenu] and then type `tooltips`.</span></span>  
*   <span data-ttu-id="5e443-126">Choose **Customize and control DevTools** \( `...` \) > **Help**  >  **Toggle the DevTools Tooltips**.</span><span class="sxs-lookup"><span data-stu-id="5e443-126">Choose **Customize and control DevTools** \(`...`\) > **Help** > **Toggle the DevTools Tooltips**.</span></span>  

<span data-ttu-id="5e443-127">Wenn Sie außerdem das Experiment ["Fokusmodus" und "DevTools-QuickInfos"][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] aktivieren, können Sie auch die Schaltfläche **"DevTools-QuickInfos** \( `?` \) " am unteren Rand der **Aktivitätsleiste**auswählen.</span><span class="sxs-lookup"><span data-stu-id="5e443-127">Also, if you turn on the [Focus Mode and DevTools Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] experiment, you may also choose the **Toggle the DevTools Tooltips** \(`?`\) button at the bottom of the **Activity Bar**.</span></span>  

<span data-ttu-id="5e443-128">Um weitere Informationen zur Verwendung der DevTools anzuzeigen, aktivieren Sie QuickInfos, und zeigen Sie dann auf die einzelnen umrissenen Regionen der DevTools.</span><span class="sxs-lookup"><span data-stu-id="5e443-128">To display more information about how to use the DevTools, turn on Tooltips, and then hover on each outlined region of the DevTools.</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des Tools "Probleme", um weitere Details anzuzeigen." lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   <span data-ttu-id="5e443-130">Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des **Tools "Probleme",** um weitere Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e443-130">Hover on anywhere in the highlighted region of the **Issues** tool to display more details</span></span>  
:::image-end:::  

## <a name="service-worker-update-timeline"></a><span data-ttu-id="5e443-131">Zeitachse für Dienstmitarbeiteraktualisierungen</span><span class="sxs-lookup"><span data-stu-id="5e443-131">Service worker update timeline</span></span>  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

<span data-ttu-id="5e443-132">Zeigen Sie in Microsoft Edge Version 91 oder höher, wenn Sie Progressive Web App- oder Service Worker-Entwickler sind, den Updatelebenszyklus Ihrer Service Worker als Zeitachse im **Anwendungstool** an.</span><span class="sxs-lookup"><span data-stu-id="5e443-132">In Microsoft Edge version 91 or later, if you're a Progressive Web App or Service Worker developer, display the update lifecycle of your Service Workers as a timeline in the **Application** tool.</span></span>  <span data-ttu-id="5e443-133">Dieses Feature hilft Ihnen, die Zeit zu verstehen, die Ihr Service Worker in den einzelnen folgenden Phasen verbringt.</span><span class="sxs-lookup"><span data-stu-id="5e443-133">This feature helps you understand the time your Service Worker spends in each of the following stages.</span></span>  

*   **<span data-ttu-id="5e443-134">Installieren</span><span class="sxs-lookup"><span data-stu-id="5e443-134">Install</span></span>**  
*   **<span data-ttu-id="5e443-135">Warte</span><span class="sxs-lookup"><span data-stu-id="5e443-135">Wait</span></span>**  
*   **<span data-ttu-id="5e443-136">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="5e443-136">Activate</span></span>**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Überprüfen der Zeitachse im Updatezyklus für Den Service Worker" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   <span data-ttu-id="5e443-138">Überprüfen der **Zeitachse** im **Updatezyklus** für Den Service Worker</span><span class="sxs-lookup"><span data-stu-id="5e443-138">Review the **Timeline** in the **Update Cycle** for your Service Worker</span></span>  
:::image-end:::  

<span data-ttu-id="5e443-139">For more information about the lifecycle of your Service Workers, navigate to [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span><span class="sxs-lookup"><span data-stu-id="5e443-139">For more information about the lifecycle of your Service Workers, navigate to [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span></span>  <span data-ttu-id="5e443-140">For more information about debugging tools for Progressive Web Apps and Service Workers in the DevTools, navigate to [Service Worker improvements][DevtoolsServiceWorkerIndex].</span><span class="sxs-lookup"><span data-stu-id="5e443-140">For more information about debugging tools for Progressive Web Apps and Service Workers in the DevTools, navigate to [Service Worker improvements][DevtoolsServiceWorkerIndex].</span></span>  <span data-ttu-id="5e443-141">Navigieren Sie zu Problem [1066604,][CR1066604]um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-141">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1066604][CR1066604].</span></span>  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a><span data-ttu-id="5e443-142">Progressive Web Apps zeigen keine Warnungen mehr für nicht quadratische Symbole an</span><span class="sxs-lookup"><span data-stu-id="5e443-142">Progressive Web Apps no longer display warnings for non-square icons</span></span>  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

<span data-ttu-id="5e443-143">Wenn [in Microsoft Edge Version 90][DevtoolsWhatsNew202102Devtools] oder früheren Versionen des Web App-Manifests Ihrer PWA ein nicht quadratisches Symbol enthalten war, wurde im Abschnitt **"Fehler und Warnungen"** für jedes nicht quadratische Symbol eine Warnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-143">In [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] or earlier, if the Web App Manifest of your PWA included a non-square icon, a warning was displayed in the **Errors and Warnings**  section for each non-square icon.</span></span>  <span data-ttu-id="5e443-144">In Microsoft Edge Version 91 oder höher zeigt der **Manifestabschnitt** im **Anwendungstool** keine Warnungen an, wenn Sie mindestens ein quadratisches Symbol bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5e443-144">In Microsoft Edge version 91 or later, the **Manifest** section in the **Application** tool displays no warnings if you provide at least one square icon.</span></span>  <span data-ttu-id="5e443-145">Wenn Sie keine quadratischen Symbole angeben, wird die folgende Meldung mit einer Warnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-145">If you don't provide any square icons, a warning displays the following message.</span></span>  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 90 oder früheren Versionen wird für jedes Nicht-Quadrat-Symbol ein Fehler angezeigt." lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="5e443-147">In Microsoft Edge Version 90 oder früheren Versionen wird für jedes Nicht-Quadrat-Symbol ein Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-147">In Microsoft Edge version 90 or earlier, an error displays for each icon that is non-square</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein Quadratsymbol bereitstellen." lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="5e443-149">In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein Quadratsymbol bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5e443-149">In Microsoft Edge version 91 or later, no error displays when you provide at least one square icon</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5e443-150">Navigieren Sie zum Überprüfen von Fehlern und Warnungen im Web App-Manifest zum **Anwendungstool,** und wählen Sie den Abschnitt **"Manifest"** aus.</span><span class="sxs-lookup"><span data-stu-id="5e443-150">To review errors and warnings in your Web App Manifest, navigate to the **Application** tool and choose the **Manifest** section.</span></span>  <span data-ttu-id="5e443-151">Fehler und Warnungen werden unter der Überschrift **"Fehler und Warnungen"** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e443-151">Errors and warnings are listed under the **Errors and Warnings** heading.</span></span>  <span data-ttu-id="5e443-152">For more information about the Web App Manifest, navigate to [Use the Web App Manifest to integrate your Progressive Web App into the Operating System][ProgressiveWebAppsWebappmanifests].</span><span class="sxs-lookup"><span data-stu-id="5e443-152">For more information about the Web App Manifest, navigate to [Use the Web App Manifest to integrate your Progressive Web App into the Operating System][ProgressiveWebAppsWebappmanifests].</span></span>  <span data-ttu-id="5e443-153">Navigieren Sie zum [PWABuilder Image Generator,][PwabuilderImagegenerator]um Symbole zu erstellen, die in Ihr Web App-Manifest aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5e443-153">To create icons to include in your Web App Manifest, navigate to the [PWABuilder Image Generator][PwabuilderImagegenerator].</span></span>  <span data-ttu-id="5e443-154">Navigieren Sie zu Problem [1185945][CR1185945], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-154">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1185945][CR1185945].</span></span>  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a><span data-ttu-id="5e443-155">Lokalisierte DevTools jetzt in Chromium-basierten Browsern unterstützt</span><span class="sxs-lookup"><span data-stu-id="5e443-155">Localized DevTools now supported in Chromium-based browsers</span></span>  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

<span data-ttu-id="5e443-156">Ab [Microsoft Edge Version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]wird Microsoft Edge DevTools in Ihrer eigenen Sprache angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-156">Starting in [Microsoft Edge version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools displays in your own language.</span></span>  <span data-ttu-id="5e443-157">Viele Entwickler verwenden andere Entwicklertools wie StackOverflow und Visual Studio Code in ihrer Sprache, nicht nur in Englisch.</span><span class="sxs-lookup"><span data-stu-id="5e443-157">Many developers use other developer tools like StackOverflow and Visual Studio Code in their native language, not just in English.</span></span>  <span data-ttu-id="5e443-158">Das Microsoft Edge DevTools-Team, das Chrome DevTools-Team und das Google-Dropdown-Team haben zusammengearbeitet, um die gleiche Oberfläche in allen Chromium-basierten Browsern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5e443-158">The Microsoft Edge DevTools team, Chrome DevTools team, and the Google Lighthouse team collaborated to provide the same experience in all Chromium-based browsers.</span></span>  <span data-ttu-id="5e443-159">For more information about how to use DevTools in your language, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span><span class="sxs-lookup"><span data-stu-id="5e443-159">For more information about how to use DevTools in your language, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  <span data-ttu-id="5e443-160">For more information about the collaboration on this feature in the Chromium open-source project, navigate to [1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="5e443-160">For more information about the collaboration on this feature in the Chromium open-source project, navigate to [1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge Browser und DevTools auf Japanisch festgelegt" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   <span data-ttu-id="5e443-162">Microsoft Edge Browser und DevTools auf Japanisch festgelegt</span><span class="sxs-lookup"><span data-stu-id="5e443-162">Microsoft Edge browser and DevTools set to Japanese</span></span>  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a><span data-ttu-id="5e443-163">Verwenden der Tastatur zum Navigieren zu CSS-Variablen</span><span class="sxs-lookup"><span data-stu-id="5e443-163">Use the keyboard to navigate to CSS variables</span></span>  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

<span data-ttu-id="5e443-164">Ab [Microsoft Edge Version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]zeigt der Bereich **Formatvorlagen** CSS-Variablen an und stellt einen Link direkt zur Definition der einzelnen Variablen bereit.</span><span class="sxs-lookup"><span data-stu-id="5e443-164">Starting in [Microsoft Edge version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], the **Styles** pane displays CSS variables and provides a link directly to the definition of each variable.</span></span>  <span data-ttu-id="5e443-165">In Microsoft Edge Version 91 oder höher können Sie mithilfe der Pfeiltasten ganz einfach zu CSS-Variablen navigieren.</span><span class="sxs-lookup"><span data-stu-id="5e443-165">In Microsoft Edge version 91 or later, you may use the arrow keys to easily navigate to CSS variables.</span></span>  <span data-ttu-id="5e443-166">Zeigen Sie auf eine Variable, und wählen Sie dann aus, um die Definition im Bereich **"Formatvorlagen"** zu `Enter` öffnen.</span><span class="sxs-lookup"><span data-stu-id="5e443-166">To open the definition in the **Styles** pane, hover on a variable, and then select `Enter`.</span></span>  <span data-ttu-id="5e443-167">Weitere Informationen zu CSS-Variablen erhalten Sie, indem Sie zu [benutzerdefinierten CSS-Eigenschaften (Variablen)][MdnDocsWebCssUsingCssCustomProperties]navigieren.</span><span class="sxs-lookup"><span data-stu-id="5e443-167">For more information about CSS variables, navigate to [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span></span>  <span data-ttu-id="5e443-168">Navigieren Sie zu Problem [1187735][CR1187735], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-168">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1187735][CR1187735].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Die CSS-Variable "-theme-body-background" im Bereich "Formatvorlagen"" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   <span data-ttu-id="5e443-170">Die `--theme-body-background` im Bereich **"Formatvorlagen"** hervorgehobene CSS-Variable</span><span class="sxs-lookup"><span data-stu-id="5e443-170">The `--theme-body-background` CSS variable highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a><span data-ttu-id="5e443-171">Probleme werden automatisch nach Schweregrad sortiert.</span><span class="sxs-lookup"><span data-stu-id="5e443-171">Issues are automatically sorted by severity</span></span>  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

<span data-ttu-id="5e443-172">Das **Tool "Probleme"** zeigt Empfehlungen zur Verbesserung Ihrer Website an, einschließlich Barrierefreiheit, Leistung, Sicherheit usw.</span><span class="sxs-lookup"><span data-stu-id="5e443-172">The **Issues** tool displays recommendations to improve your website, including accessibility, performance, security, and so on.</span></span> <span data-ttu-id="5e443-173">Basierend auf Ihrem Feedback werden die Probleme jetzt automatisch nach Schweregrad sortiert.</span><span class="sxs-lookup"><span data-stu-id="5e443-173">Based on your feedback, issues are now automatically sorted by severity.</span></span>  <span data-ttu-id="5e443-174">In jeder Feedbackkategorie wird jedes als **Fehler** gekennzeichnete Problem zuerst angezeigt, gefolgt von jedem Problem, das als **Warnung**gekennzeichnet ist, und dann jedem Problem, das als **Tipp**gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="5e443-174">In each feedback category, each issue marked as an **Error** appears first, followed each issue marked as a **Warning**, then each issue marked as a **Tip**.</span></span>  <span data-ttu-id="5e443-175">Um Ihre Probleme zu verfeinern, sind zusätzliche Filteroptionen für ein zukünftiges Update geplant.</span><span class="sxs-lookup"><span data-stu-id="5e443-175">To help you refine your issues, extra filter options are planned for a future update.</span></span>  <span data-ttu-id="5e443-176">For more information about how to review issues, navigate to [Find and fix problems using the Issues tool][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="5e443-176">For more information about how to review issues, navigate to [Find and fix problems using the Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="Das Tool "Probleme" zeigt sortierte Probleme nach Schweregrad an." lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   <span data-ttu-id="5e443-178">Das Tool **"Probleme"** zeigt sortierte Probleme nach Schweregrad an.</span><span class="sxs-lookup"><span data-stu-id="5e443-178">The **Issues** tool displays sorted issues by severity</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a><span data-ttu-id="5e443-179">Microsoft Edge Entwicklertools für Visual Studio Code Version 1.1.7</span><span class="sxs-lookup"><span data-stu-id="5e443-179">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.7</span></span>  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

<span data-ttu-id="5e443-180">The [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 provides the DevTools from Microsoft Edge version [88][DevtoolsWhatsNew202011Devtools].</span><span class="sxs-lookup"><span data-stu-id="5e443-180">The [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 provides the DevTools from [Microsoft Edge version 88][DevtoolsWhatsNew202011Devtools].</span></span>  <span data-ttu-id="5e443-181">Diese Erweiterung unterstützt jetzt ARM-Geräte und ist nicht mehr vom [Debugger für Microsoft Edge-Erweiterung][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] abhängig.</span><span class="sxs-lookup"><span data-stu-id="5e443-181">This extension now supports ARM devices and no longer depends on the [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extension.</span></span>  <span data-ttu-id="5e443-182">Version 1.1.7 enthält die folgenden Fehlerbehebungen und Verbesserungen.</span><span class="sxs-lookup"><span data-stu-id="5e443-182">Version 1.1.7 includes the following bug fixes and improvements.</span></span>  

*   <span data-ttu-id="5e443-183">Die Zuverlässigkeit des Schließens des Ziels wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5e443-183">Updated the reliability of target closure.</span></span>  
*   <span data-ttu-id="5e443-184">Der Seitenbereich wurde so aktualisiert, dass er automatisch aktualisiert wird, wenn Sie Ziele debuggen, die erstellt oder zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="5e443-184">Updated the side panel to automatically refreshes when you debug targets that are created or destroyed.</span></span>  
*   <span data-ttu-id="5e443-185">Ein neues Kontextmenü wurde hinzugefügt, mit dem Sie schneller auf die Erweiterungseinstellungen und das neueste Changelog zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="5e443-185">Added a new contextual menu that gives you faster access to the extension settings and the latest Changelog.</span></span>  
*   <span data-ttu-id="5e443-186">Die Veröffentlichung der Erweiterungsdokumentation einschließlich der neuesten Features wurde aktualisiert und vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="5e443-186">Updated and simplified the release of extension documentation including the newest features.</span></span>  
    
<span data-ttu-id="5e443-187">Um die Version 1.1.7 manuell zu aktualisieren, navigieren Sie manuell zu ["Erweiterung aktualisieren".][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="5e443-187">To manually update to version 1.1.7, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="5e443-188">Sie können Probleme melden und zur Erweiterung im [vscode-edge-devtools GitHub-Repository][GithubMicrosoftVscodeEdgeDevtools] mitwirken.</span><span class="sxs-lookup"><span data-stu-id="5e443-188">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="5e443-189">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="5e443-189">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="visualize-css-scroll-snap"></a><span data-ttu-id="5e443-190">Visualisieren des CSS-Bildlauf-Snaps</span><span class="sxs-lookup"><span data-stu-id="5e443-190">Visualize CSS scroll-snap</span></span>  

<span data-ttu-id="5e443-191">Sie können nun das `scroll-snap` Signal im **Elementtool** umschalten, um die CSS-Bildlauf-Snap-Ausrichtung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-191">You may now toggle the `scroll-snap` badge in the **Elements** tool to inspect the CSS scroll-snap alignment.</span></span>  <span data-ttu-id="5e443-192">Wenn ein HTML-Element auf Ihrer Webseite `scroll-snap-type` darauf angewendet wurde, wird ein `scroll-snap` Signal daneben im **Elementtool** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-192">When an HTML element on your webpage has `scroll-snap-type` applied to it, a `scroll-snap` badge displays next to it in the **Elements** tool.</span></span>  <span data-ttu-id="5e443-193">Wählen Sie das Signal aus, um die Anzeige einer Bildlauf-Snap-Überlagerung auf der Webseite zu aktivieren (oder zu deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="5e443-193">Choose the badge to turn on \(or off\) the display of a scroll-snap overlay on the webpage.</span></span>  <span data-ttu-id="5e443-194">Um eine Beispielwebseite zu überprüfen, navigieren Sie zu [Scroll Snap Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].</span><span class="sxs-lookup"><span data-stu-id="5e443-194">To review an example webpage, navigate to [Scroll Snap Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].</span></span>  <span data-ttu-id="5e443-195">Im Beispiel werden Punkte an Andockkanten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-195">In the example, dots display on snap edges.</span></span>  <span data-ttu-id="5e443-196">Der Bildlaufport weist eine durchgezogene Kontur auf, während die Andockelemente Strichumrisse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5e443-196">The scroll port has a solid outline while the snap items have dash outlines.</span></span>  <span data-ttu-id="5e443-197">Der Bildlaufabstand ist grün gefüllt, während der Bildlaufrand orangefarben gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="5e443-197">The scroll padding is filled in green while the scroll margin is filled in orange.</span></span>  <span data-ttu-id="5e443-198">Navigieren Sie zu Problem [862450,][CR862450]um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-198">To review the history of this feature in the Chromium open-source project, navigate to Issue [862450][CR862450].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-scroll-snap-highlight.msft.png" alt-text="CSS-Bildlauf-Snap" lightbox="../../media/2021/04/elements-scroll-snap-highlight.msft.png":::
   <span data-ttu-id="5e443-200">CSS-Bildlauf-Snap</span><span class="sxs-lookup"><span data-stu-id="5e443-200">CSS scroll-snap</span></span>  
:::image-end:::  

### <a name="new-memory-inspector-tool"></a><span data-ttu-id="5e443-201">Neues Speicherprüfungstool</span><span class="sxs-lookup"><span data-stu-id="5e443-201">New Memory Inspector tool</span></span>  

<span data-ttu-id="5e443-202">Verwenden Sie das neue **Speicherprüfungstool,** um einen `ArrayBuffer` Speicher in JavaScript und Wasm zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-202">Use the new **Memory Inspector** tool to inspect an `ArrayBuffer` in JavaScript and Wasm memory.</span></span>  <span data-ttu-id="5e443-203">Öffnen Sie die [Demowebseite "Memory in JS".][GlitchMemoryInspectorDemoJsHtml]</span><span class="sxs-lookup"><span data-stu-id="5e443-203">Open the [Memory in JS][GlitchMemoryInspectorDemoJsHtml] demo webpage.</span></span>  <span data-ttu-id="5e443-204">Öffnen Sie im **Tool "Quellen"** die `memory-write-wasm` Datei, und legen Sie einen Haltepunkt an der Zeile `0x03c` fest.</span><span class="sxs-lookup"><span data-stu-id="5e443-204">In the **Sources** tool, open the `memory-write-wasm` file, and set a breakpoint at line `0x03c`.</span></span>  <span data-ttu-id="5e443-205">Aktualisieren Sie die Webseite.</span><span class="sxs-lookup"><span data-stu-id="5e443-205">Refresh the webpage.</span></span>  <span data-ttu-id="5e443-206">Erweitern Sie den **Bereich** im Debuggerbereich.</span><span class="sxs-lookup"><span data-stu-id="5e443-206">Expand the **Scope** section in the debugger pane.</span></span>  <span data-ttu-id="5e443-207">Das neue Symbol wird neben dem **Pufferwert** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-207">The new icon is displayed next to the **buffer** value.</span></span>  <span data-ttu-id="5e443-208">Wählen Sie ihn aus, um das neue **Speicherprüfungstool** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5e443-208">Choose it to open the new **Memory Inspector** tool.</span></span>  

<span data-ttu-id="5e443-209">Um mehr über das Debuggen im **Quellentool** zu erfahren, navigieren Sie zum Debuggen von [JavaScript-Code im Bereich "Debugger".][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]</span><span class="sxs-lookup"><span data-stu-id="5e443-209">To learn more about debugging in the **Sources** tool, navigate to [Using the Debugger pane to debug JavaScript code][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode].</span></span>  <span data-ttu-id="5e443-210">Navigieren Sie zu Problem [1166577][CR1166577][CR1166577], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-210">To review the history of this feature in the Chromium open-source project, navigate to Issue [1166577][CR1166577].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png" alt-text="Speicherprüfungstool" lightbox="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png":::
   <span data-ttu-id="5e443-212">**Speicherprüfungstool**</span><span class="sxs-lookup"><span data-stu-id="5e443-212">**Memory inspector** tool</span></span>  
:::image-end:::  

### <a name="new-badge-settings-pane-in-the-elements-tool"></a><span data-ttu-id="5e443-213">Bereich "Neue Signaleinstellungen" im Tool "Elemente"</span><span class="sxs-lookup"><span data-stu-id="5e443-213">New Badge settings pane in the Elements tool</span></span>  

<span data-ttu-id="5e443-214">Verwenden Sie nun die **Badge-Einstellungen** im **Elementtool,** um einzelne Badges zu aktivieren (oder zu deaktivieren).)</span><span class="sxs-lookup"><span data-stu-id="5e443-214">Now, use the **Badge settings** in the **Elements** tool to turn on \(or off\) individual badges.</span></span>  <span data-ttu-id="5e443-215">Verwenden Sie dieses Feature, um wichtige Badges anzupassen und sich auf diese zu konzentrieren, während Sie Webseiten überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-215">Use this feature to customize and stay focused on important badges while you inspect webpages.</span></span>  <span data-ttu-id="5e443-216">Führen Sie die folgenden Aktionen aus, um den Bereich "Signaleinstellungen" oben im **Elementtool** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e443-216">To display the badge settings pane at the top of the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="5e443-217">Zeigen Sie auf ein beliebiges Element.</span><span class="sxs-lookup"><span data-stu-id="5e443-217">Hover on any element.</span></span>  
1.  <span data-ttu-id="5e443-218">Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).</span><span class="sxs-lookup"><span data-stu-id="5e443-218">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="5e443-219">Wählen Sie **Badge-Einstellungen... aus.**</span><span class="sxs-lookup"><span data-stu-id="5e443-219">Choose **Badge settings...**.</span></span>  
    
<span data-ttu-id="5e443-220">Um die Badges anzuzeigen (oder auszublenden),wählen Sie \(oder entfernen\) das Kontrollkästchen neben dem Signalnamen aus.</span><span class="sxs-lookup"><span data-stu-id="5e443-220">To display \(or hide\) the badges, choose \(or remove\) the checkbox next to the badge name.</span></span>  

<!--  To review the history of this feature in the Chromium open-source project, navigate to Issue [1066772][CR1066772].  -->  

:::image type="complex" source="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png" alt-text="Bereich "Signaleinstellungen" im Elementtool" lightbox="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png":::
   <span data-ttu-id="5e443-222">Bereich **"Signaleinstellungen"** **im** Elementtool</span><span class="sxs-lookup"><span data-stu-id="5e443-222">**Badge settings** pane in the **Elements** tool</span></span>  
:::image-end:::  

### <a name="enhanced-image-preview-with-aspect-ratio-information"></a><span data-ttu-id="5e443-223">Erweiterte Bildvorschau mit Informationen zum Seitenverhältnis</span><span class="sxs-lookup"><span data-stu-id="5e443-223">Enhanced image preview with aspect ratio information</span></span>  

<span data-ttu-id="5e443-224">Die Bildvorschau in den DevTools wurde verbessert, um weitere Informationen anzuzeigen, einschließlich der folgenden Details.</span><span class="sxs-lookup"><span data-stu-id="5e443-224">Image previews in the DevTools have been enhanced to display more information, including the following details.</span></span>  

*   <span data-ttu-id="5e443-225">Gerenderte Größe</span><span class="sxs-lookup"><span data-stu-id="5e443-225">Rendered size</span></span>  
*   <span data-ttu-id="5e443-226">Gerendertes Seitenverhältnis</span><span class="sxs-lookup"><span data-stu-id="5e443-226">Rendered aspect ratio</span></span>  
*   <span data-ttu-id="5e443-227">Systeminterne Größe</span><span class="sxs-lookup"><span data-stu-id="5e443-227">Intrinsic size</span></span>  
*   <span data-ttu-id="5e443-228">Systeminternes Seitenverhältnis</span><span class="sxs-lookup"><span data-stu-id="5e443-228">Intrinsic aspect ratio</span></span>  
*   <span data-ttu-id="5e443-229">Dateigröße</span><span class="sxs-lookup"><span data-stu-id="5e443-229">File size</span></span>  
    
<span data-ttu-id="5e443-230">Die Informationen helfen Ihnen, Ihre Bilder besser zu verstehen und die Optimierung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="5e443-230">The  information helps you better understand your images and apply optimization.</span></span>  <span data-ttu-id="5e443-231">Die Informationen zum Bildseitenverhältnis sind auch im **Netzwerktool** verfügbar, wenn Sie eine Bildvorschau auswählen.</span><span class="sxs-lookup"><span data-stu-id="5e443-231">The image aspect ratio information is also available in the **Network** tool, when you choose an image preview.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5e443-232">Im Tool **"Elemente"** zeigt die Bildvorschau jetzt weitere Informationen zum Bild an.</span><span class="sxs-lookup"><span data-stu-id="5e443-232">In the **Elements** tool, image preview now displays more information about the image.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5e443-233">Außerdem sind die Informationen zum Bildseitenverhältnis im **Netzwerktool** verfügbar, wenn Sie eine Bildvorschau auswählen.</span><span class="sxs-lookup"><span data-stu-id="5e443-233">Also, the image aspect ratio information is available in the **Network** tool, when you choose an image preview.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png" alt-text="Bildvorschau mit Informationen zum Seitenverhältnis im Elementtool" lightbox="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png":::
         <span data-ttu-id="5e443-235">Bildvorschau mit Informationen zum Seitenverhältnis im **Elementtool**</span><span class="sxs-lookup"><span data-stu-id="5e443-235">Image preview with aspect ratio information in the **Element** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/network-img-name-filters-preview.msft.png" alt-text="Bildseitenverhältnisinformationen im Netzwerktool" lightbox="../../media/2021/04/network-img-name-filters-preview.msft.png":::
         <span data-ttu-id="5e443-237">Bildseitenverhältnisinformationen im **Netzwerktool**</span><span class="sxs-lookup"><span data-stu-id="5e443-237">Image aspect ratio information in the **Network** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5e443-238">Navigieren Chromium Sie zu Problemen [1149832][CR1149832][CR1149832] und [1170656][CR1170656].</span><span class="sxs-lookup"><span data-stu-id="5e443-238">To review the history of this feature in the Chromium open-source project, navigate to Issues [1149832][CR1149832] and [1170656][CR1170656].</span></span>  

### <a name="new-options-to-configure-content-encodings-in-the-network-conditions-tool"></a><span data-ttu-id="5e443-239">Neue Optionen zum Konfigurieren von Inhaltscodierungen im Netzwerkbedingungentool</span><span class="sxs-lookup"><span data-stu-id="5e443-239">New options to configure Content-Encodings in the Network conditions tool</span></span> 

<span data-ttu-id="5e443-240">Wählen Sie im **Netzwerktool** die neue Schaltfläche **"Weitere Netzwerkbedingungen...** " neben dem Dropdownmenü **"Drosselung"** aus, um das **Tool "Netzwerkbedingungen"** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5e443-240">In the **Network** tool, choose the new **More network conditions...** button next to the **Throttling** dropdown menu to open the **Network conditions** tool.</span></span>  <span data-ttu-id="5e443-241">Führen Sie die folgenden Aktionen aus, um zu testen, ob Serverantworten korrekt für Browser codiert sind, die [gzip,][GnuSoftwareGzipManual] [brotli][|::ref1::|Main]oder eine andere Zukunft nicht `Content-Encoding` unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5e443-241">To test if server responses are correctly encoded for browsers that don't support [gzip][GnuSoftwareGzipManual], [brotli][|::ref1::|Main], or another future `Content-Encoding`, complete the following actions.</span></span>  

1.  <span data-ttu-id="5e443-242">Öffnen des Tools für **Netzwerkbedingungen**</span><span class="sxs-lookup"><span data-stu-id="5e443-242">Open the **Network conditions** tool</span></span>
1.  <span data-ttu-id="5e443-243">Navigieren Sie zu **akzeptierten Inhaltscodierungen.**</span><span class="sxs-lookup"><span data-stu-id="5e443-243">Navigate to **Accepted Content-Encodings**.</span></span> 
1.  <span data-ttu-id="5e443-244">Entfernen Sie das Kontrollkästchen neben dem, das `Content-Encoding` Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="5e443-244">Remove the checkbox next to the `Content-Encoding` you want to test.</span></span>  
    
<span data-ttu-id="5e443-245">Navigieren Sie zu Problem [1162042][CR1162042], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-245">To review the history of this feature in the Chromium open-source project, navigate to Issue [1162042][CR1162042].</span></span>  

:::image type="complex" source="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png" alt-text="Neue weitere Netzwerkbedingungen... schaltfläche öffnet das Netzwerkbedingungen-Tool zum Konfigurieren der Inhaltscodierung" lightbox="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png":::
   <span data-ttu-id="5e443-247">Neue **Weitere Netzwerkbedingungen...** Schaltfläche öffnet das **Netzwerkbedingungen-Tool** zum Konfigurieren</span><span class="sxs-lookup"><span data-stu-id="5e443-247">New **More network conditions...** button opens the **Network conditions** tool to configure</span></span> `Content-Encoding`  
:::image-end:::  

### <a name="styles-pane-enhancements"></a><span data-ttu-id="5e443-248">Erweiterungen des Stilbereichs</span><span class="sxs-lookup"><span data-stu-id="5e443-248">Styles pane enhancements</span></span>  

#### <a name="new-shortcut-to-display-computed-value-in-the-styles-pane"></a><span data-ttu-id="5e443-249">Neue Verknüpfung zum Anzeigen des berechneten Werts im Bereich "Formatvorlagen"</span><span class="sxs-lookup"><span data-stu-id="5e443-249">New shortcut to display computed value in the Styles pane</span></span>  

<span data-ttu-id="5e443-250">Führen Sie nun die folgenden Aktionen aus, um den berechneten CSS-Wert im Bereich **"Formatvorlagen"** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e443-250">Now, to display the computed CSS value in the **Styles** pane, complete the following actions.</span></span>  

1.  <span data-ttu-id="5e443-251">Zeigen Sie auf eine CSS-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5e443-251">Hover on a CSS property.</span></span>  
1.  <span data-ttu-id="5e443-252">Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).</span><span class="sxs-lookup"><span data-stu-id="5e443-252">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="5e443-253">Choose **View computed value**.</span><span class="sxs-lookup"><span data-stu-id="5e443-253">Choose **View computed value**.</span></span>  
    
<span data-ttu-id="5e443-254">Navigieren Sie zu Problem [1076198][CR1076198], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-254">To review the history of this feature in the Chromium open-source project, navigate to Issue [1076198][CR1076198].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png" alt-text="Neue Verknüpfung zum Anzeigen des berechneten Werts" lightbox="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png":::
   <span data-ttu-id="5e443-256">Neue Verknüpfung zum Anzeigen des berechneten Werts</span><span class="sxs-lookup"><span data-stu-id="5e443-256">New shortcut to display computed value</span></span>  
:::image-end:::  

#### <a name="support-for-the-accent-color-keyword"></a><span data-ttu-id="5e443-257">Unterstützung für das Schlüsselwort Akzentfarbe</span><span class="sxs-lookup"><span data-stu-id="5e443-257">Support for the accent-color keyword</span></span>  

<span data-ttu-id="5e443-258">Die Benutzeroberfläche für automatisches Vervollständigen des Bereichs **"Formatvorlagen"** erkennt nun das `accent-color` CSS-Schlüsselwort, mit dem Sie die Akzentfarbe für ui-Steuerelemente angeben können, die vom Element generiert werden.</span><span class="sxs-lookup"><span data-stu-id="5e443-258">The autocomplete UI of the **Styles** pane now detects the `accent-color` CSS keyword, which allows you to specify the accent color for UI controls generated by the element.</span></span>  <span data-ttu-id="5e443-259">Beispiele für UI-Steuerelemente, die von einem Element generiert werden, sind Kontrollkästchen oder Optionsfelder.</span><span class="sxs-lookup"><span data-stu-id="5e443-259">Examples of UI controls that are generated by an element include checkboxes or radio buttons.</span></span> <span data-ttu-id="5e443-260">For more information about the status of the Chromium implementation, navigate to [Feature: accent-color CSS property][ChromestatusFeature4752739957473280].</span><span class="sxs-lookup"><span data-stu-id="5e443-260">For more information about the status of the Chromium implementation, navigate to [Feature: accent-color CSS property][ChromestatusFeature4752739957473280].</span></span>  <span data-ttu-id="5e443-261">Um dieses Feature zu aktivieren, navigieren Sie zu `edge://flags#enable-experimental-web-platform-features` "Aktiviert", und legen Sie das Kontrollkästchen auf **"Aktiviert"** fest.</span><span class="sxs-lookup"><span data-stu-id="5e443-261">To turn on this feature, navigate to `edge://flags#enable-experimental-web-platform-features` and set the checkbox to **Enabled**.</span></span>  <span data-ttu-id="5e443-262">Navigieren Sie zu Problem [1092093][CR1092093], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-262">To review the history of this feature in the Chromium open-source project, navigate to Issue [1092093][CR1092093].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-accent-color.msft.png" alt-text="CSS-Schlüsselwort für Akzentfarbe" lightbox="../../media/2021/04/elements-styles-accent-color.msft.png":::
   `accent-color` <span data-ttu-id="5e443-264">CSS-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="5e443-264">CSS keyword</span></span>
:::image-end:::  

### <a name="display-details-about-blocked-features-in-the-frame-details-view"></a><span data-ttu-id="5e443-265">Anzeigen von Details zu blockierten Features in der Frame-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="5e443-265">Display details about blocked features in the Frame details view</span></span>  

<span data-ttu-id="5e443-266">Die Berechtigungsrichtlinie ist eine Webplattform-API, die einer Website die Möglichkeit gibt, die Verwendung von Browserfeatures in einem einzelnen Frame oder in einem eingebetteten Frame zuzulassen oder zu `iframe` blockieren.</span><span class="sxs-lookup"><span data-stu-id="5e443-266">Permissions Policy is a web platform API that gives a website the ability to allow or block the use of browser features in an individual frame or in an `iframe` that it embeds.</span></span> <span data-ttu-id="5e443-267">Weitere Informationen finden Sie unter [Berechtigungsrichtlinienerklärer.][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]</span><span class="sxs-lookup"><span data-stu-id="5e443-267">For more information, navigate to [Permissions Policy Explainer][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd].</span></span>  <span data-ttu-id="5e443-268">Führen Sie die folgenden Aktionen aus, um die Gründe für die Blockierfunktion anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e443-268">To display the details on why a feature is blocked, complete the following actions.</span></span>  

1.  <span data-ttu-id="5e443-269">Navigieren Sie zur [OOPIF-Berechtigungsrichtlinie.][GlitchPermissionPolicyDemoMain]</span><span class="sxs-lookup"><span data-stu-id="5e443-269">Navigate to [OOPIF Permissions Policy][GlitchPermissionPolicyDemoMain].</span></span>  
1.  <span data-ttu-id="5e443-270">Navigieren Sie zum **Anwendungstool.**</span><span class="sxs-lookup"><span data-stu-id="5e443-270">Navigate to the **Application** tool.</span></span>  
1.  <span data-ttu-id="5e443-271">Wählen Sie einen Frame aus.</span><span class="sxs-lookup"><span data-stu-id="5e443-271">Choose a frame.</span></span>  
1.  <span data-ttu-id="5e443-272">Navigieren Sie zum Abschnitt **"Berechtigungsrichtlinie".**</span><span class="sxs-lookup"><span data-stu-id="5e443-272">Navigate to the **Permissions Policy** section.</span></span>  
1.  <span data-ttu-id="5e443-273">Navigieren Sie zur Eigenschaft **"Deaktivierte Features".**</span><span class="sxs-lookup"><span data-stu-id="5e443-273">Navigate to the **Disabled Features** property.</span></span>  
1.  <span data-ttu-id="5e443-274">Wählen Sie **"Details anzeigen"** aus.</span><span class="sxs-lookup"><span data-stu-id="5e443-274">Choose **Show details**.</span></span>  
1.  <span data-ttu-id="5e443-275">Wählen Sie das Symbol neben jeder Richtlinie aus, um zu der oder der Netzwerkanforderung zu `iframe` navigieren, die das Feature blockiert hat.</span><span class="sxs-lookup"><span data-stu-id="5e443-275">Choose the icon next to each policy to navigate to the `iframe` or network request that blocked the feature.</span></span>  
    
<span data-ttu-id="5e443-276">Navigieren Sie zu Problem [1158827][CR1158827], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-276">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png" alt-text="Blockierte Features in der Frame-Detailansicht" lightbox="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png":::
   <span data-ttu-id="5e443-278">Blockierte Features in der Frame-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="5e443-278">Blocked features in the Frame details view</span></span>  
:::image-end:::  

### <a name="filter-experiments-in-the-experiments-setting"></a><span data-ttu-id="5e443-279">Filtern von Experimenten in der Einstellung "Experimente"</span><span class="sxs-lookup"><span data-stu-id="5e443-279">Filter experiments in the Experiments setting</span></span>  

<span data-ttu-id="5e443-280">Suchen Sie Experimente schneller mit dem neuen Experimentfilter.</span><span class="sxs-lookup"><span data-stu-id="5e443-280">Find experiments quicker with the new experiment filter.</span></span>  <span data-ttu-id="5e443-281">Führen Sie beispielsweise die folgenden Aktionen aus, um neue Experimente für Codeprobleme zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5e443-281">For example, to turn on new experiments for code issues, complete the following actions.</span></span>
``

1.  <span data-ttu-id="5e443-282">Navigieren Sie zu **Einstellungen**  >  **Experiments**.</span><span class="sxs-lookup"><span data-stu-id="5e443-282">Navigate to **Settings** > **Experiments**.</span></span>  
1.  <span data-ttu-id="5e443-283">Navigieren Sie zum Textfeld \*\* Filter .\*\*</span><span class="sxs-lookup"><span data-stu-id="5e443-283">Navigate to the **Filter** textbox.</span></span>  
1.  <span data-ttu-id="5e443-284">Geben Sie `issues` ein.</span><span class="sxs-lookup"><span data-stu-id="5e443-284">Type `issues`.</span></span>  
    
:::image type="complex" source="../../media/2021/04/settings-experiments-filter-by-issues.msft.png" alt-text="Filtern von Experimenten in der Einstellung "Experimente"" lightbox="../../media/2021/04/settings-experiments-filter-by-issues.msft.png":::
   <span data-ttu-id="5e443-286">Filtern von Experimenten in der Einstellung **"Experimente"**</span><span class="sxs-lookup"><span data-stu-id="5e443-286">Filter experiments in the **Experiments** setting</span></span>  
:::image-end:::  

### <a name="new-vary-header-column-in-the-cache-storage-pane"></a><span data-ttu-id="5e443-287">Neue Spalte "Kopfzeile variieren" im Speicherbereich "Cache"</span><span class="sxs-lookup"><span data-stu-id="5e443-287">New Vary Header column in the Cache storage pane</span></span>  

<span data-ttu-id="5e443-288">Verwenden Sie die neue `Vary Header` Spalte im **Bereich "Cache Storage",** um die Werte der [Vary][HttpwgSpecsRfc7231HtmlHeaderVary] HTTP-Antwortheader anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e443-288">Use the new `Vary Header` column in the **Cache Storage** pane to display the [Vary][HttpwgSpecsRfc7231HtmlHeaderVary] HTTP response header values.</span></span>  <span data-ttu-id="5e443-289">Navigieren Sie zu Problem [1186049][CR1186049], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-289">To review the history of this feature in the Chromium open-source project, navigate to Issue [1186049][CR1186049].</span></span>  

:::image type="complex" source="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png" alt-text="Spalte "Kopfzeile variieren"" lightbox="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png":::
   <span data-ttu-id="5e443-291">Spalte "Kopfzeile variieren"</span><span class="sxs-lookup"><span data-stu-id="5e443-291">Vary Header column</span></span>  
:::image-end:::  

### <a name="sources-tool-improvements"></a><span data-ttu-id="5e443-292">Verbesserungen am Tool "Quellen"</span><span class="sxs-lookup"><span data-stu-id="5e443-292">Sources tool improvements</span></span>  

#### <a name="support-for-new-javascript-features"></a><span data-ttu-id="5e443-293">Unterstützung für neue JavaScript-Features</span><span class="sxs-lookup"><span data-stu-id="5e443-293">Support for new JavaScript features</span></span>  

<span data-ttu-id="5e443-294">DevTools unterstützt jetzt die neue [Private Marke checks a.k.a. #foo in obj][V8DevFeaturesPrivateBrandChecks] JavaScript language feature.</span><span class="sxs-lookup"><span data-stu-id="5e443-294">DevTools now support the new [Private brand checks a.k.a. #foo in obj][V8DevFeaturesPrivateBrandChecks] JavaScript language feature.</span></span>  <span data-ttu-id="5e443-295">Das Feature "Überprüfungen privater Marken" erweitert den [Operator "in",][MdnDocsWebJavascriptReferenceOperatorsIn] um [Felder der privaten Klasse][V8DevFeaturesClassFieldsPrivateClassFields] für ein bestimmtes Objekt zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5e443-295">The private brand checks feature extends the [in operator][MdnDocsWebJavascriptReferenceOperatorsIn] to support [Private class fields][V8DevFeaturesClassFieldsPrivateClassFields] on a specific object.</span></span>  <span data-ttu-id="5e443-296">Probieren Sie es in den **Konsolen-** und **Quellentools** aus.</span><span class="sxs-lookup"><span data-stu-id="5e443-296">Try it in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="5e443-297">Führen Sie außerdem die folgenden Aktionen aus, um die privaten Felder zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-297">Also, to inspect the private fields, complete the following actions.</span></span>  

1.  <span data-ttu-id="5e443-298">Navigieren Sie zum **Debuggerbereich.**</span><span class="sxs-lookup"><span data-stu-id="5e443-298">Navigate to **debugger** pane.</span></span>  
1.  <span data-ttu-id="5e443-299">Navigieren Sie zum **Bereichsbereich.**</span><span class="sxs-lookup"><span data-stu-id="5e443-299">Navigate to the **Scope** section.</span></span>  
    
<span data-ttu-id="5e443-300">Navigieren Sie zu Problem [11374,][CR11374]um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-300">To review the history of this feature in the Chromium open-source project, navigate to Issue [11374][CR11374].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png" alt-text="JavaScript Private Brand Checks" lightbox="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png":::
   <span data-ttu-id="5e443-302">JavaScript Private Brand Checks</span><span class="sxs-lookup"><span data-stu-id="5e443-302">JavaScript private brand checks</span></span>  
:::image-end:::  

#### <a name="enhanced-support-for-breakpoints-debugging"></a><span data-ttu-id="5e443-303">Erweiterte Unterstützung für das Debuggen von Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="5e443-303">Enhanced support for breakpoints debugging</span></span>  

<span data-ttu-id="5e443-304">Moderne JavaScript-Bundler wie [Webpack][WebpackJsMain]und [Rollup][RollupjsMain] unterstützen die Codeteilung.</span><span class="sxs-lookup"><span data-stu-id="5e443-304">Modern JavaScript bundlers like [Webpack][WebpackJsMain], and [Rollup][RollupjsMain] support code splitting.</span></span>  <span data-ttu-id="5e443-305">Um mehr über das Teilen von Code zu erfahren, navigieren Sie zum [Codetrennen.][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]</span><span class="sxs-lookup"><span data-stu-id="5e443-305">To learn more about code splitting, navigate to [Code splitting][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules].</span></span>  <span data-ttu-id="5e443-306">In Microsoft Edge Version 90 oder früheren Versionen legen DevTools nur Haltepunkte in einem einzigen Bündel fest.</span><span class="sxs-lookup"><span data-stu-id="5e443-306">In Microsoft Edge version 90 or earlier, DevTools only set breakpoints in a single bundle.</span></span>  <span data-ttu-id="5e443-307">In Microsoft Edge Version 91 oder höher legt DevTools beim Debuggen einer freigegebenen Komponente Haltepunkte in mehreren Bundles fest.</span><span class="sxs-lookup"><span data-stu-id="5e443-307">In Microsoft Edge version 91 or later, DevTools properly sets breakpoints in multiple bundles when you debug a shared component.</span></span>  <span data-ttu-id="5e443-308">Navigieren Sie zu Problemen [1142705][CR1142705], [979000][CR979000]und [1180794][CR1180794], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-308">To review the history of this feature in the Chromium open-source project, navigate to Issues [1142705][CR1142705], [979000][CR979000], and [1180794][CR1180794].</span></span>  

#### <a name="support-hover-preview-with-bracket-notation"></a><span data-ttu-id="5e443-309">Unterstützung der Hovervorschau mit Klammer-Notation</span><span class="sxs-lookup"><span data-stu-id="5e443-309">Support hover preview with bracket notation</span></span>  

<span data-ttu-id="5e443-310">DevTools unterstützt jetzt die Hovervorschau für JavaScript-Memberausdrücke, die die `[]` Notation im **Tool "Quellen"** verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e443-310">DevTools now support hover preview on JavaScript member expressions that use the `[]` notation in the **Sources** tool.</span></span>  <span data-ttu-id="5e443-311">Navigieren Sie zu Problem [1178305][CR1178305], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-311">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178305][CR1178305].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png" alt-text="Unterstützung der Hovervorschau mit [] Notation" lightbox="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png":::
   <span data-ttu-id="5e443-313">Unterstützung der Hovervorschau mit `[]` Notation</span><span class="sxs-lookup"><span data-stu-id="5e443-313">Support hover preview with `[]` notation</span></span>  
:::image-end:::  

#### <a name="improved-outline-of-html-files"></a><span data-ttu-id="5e443-314">Verbesserte Gliederung von HTML-Dateien</span><span class="sxs-lookup"><span data-stu-id="5e443-314">Improved outline of HTML files</span></span>  

<span data-ttu-id="5e443-315">DevTools bietet jetzt eine bessere Gliederungsunterstützung für `.html` Dateien.</span><span class="sxs-lookup"><span data-stu-id="5e443-315">DevTools now has better outline support for `.html` files.</span></span>  <span data-ttu-id="5e443-316">Öffnen Sie im **Tool "Quellen"** die `.html` Datei.</span><span class="sxs-lookup"><span data-stu-id="5e443-316">In the **Sources** tool, open the `.html` file.</span></span>  <span data-ttu-id="5e443-317">Um die Codegliederung zu aktivieren (oder zu deaktivieren), wählen Sie `Ctrl` + `Shift` + `O` Windows/Linux oder `Cmd` + `Shift` + `O` macOS aus.</span><span class="sxs-lookup"><span data-stu-id="5e443-317">To turn on \(or off\) the code outline, select `Ctrl`+`Shift`+`O` on Windows/Linux or `Cmd`+`Shift`+`O` on macOS.</span></span>  <span data-ttu-id="5e443-318">In der folgenden Abbildung listen DevTools nun alle Funktionen in der Gliederung ordnungsgemäß auf.</span><span class="sxs-lookup"><span data-stu-id="5e443-318">In the following figure, DevTools now correctly list all functions in the outline.</span></span>  <span data-ttu-id="5e443-319">Bisher wurden von DevTools nur einige der Funktionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-319">Previously, DevTools only displayed some of the functions.</span></span>  <span data-ttu-id="5e443-320">Navigieren Sie zu Problemen [761019][CR761019] und [1191465][CR1191465], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-320">To review the history of this feature in the Chromium open-source project, navigate to Issues [761019][CR761019] and [1191465][CR1191465].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-jobobbx-at.msft.png" alt-text=" Verbesserte Gliederung von HTML-Dateien" lightbox="../../media/2021/04/sources-page-jobobbx-at.msft.png":::
   <span data-ttu-id="5e443-322">Verbesserte Gliederung von HTML-Dateien</span><span class="sxs-lookup"><span data-stu-id="5e443-322">Improved outline of HTML files</span></span>  
:::image-end:::  

#### <a name="proper-error-stack-traces-for-wasm-debugging"></a><span data-ttu-id="5e443-323">Ordnungsgemäße Fehlerstapelüberwachungen für wasm-Debugging</span><span class="sxs-lookup"><span data-stu-id="5e443-323">Proper error stack traces for Wasm debugging</span></span>  

<span data-ttu-id="5e443-324">In Microsoft Edge Version 90 oder früher wurden in DevTools nur generische Wasm-Verweise in Fehlerstapelablaufverfolgungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-324">In Microsoft Edge version 90 or earlier, DevTools only displayed generic Wasm references in Error stack traces.</span></span>  <span data-ttu-id="5e443-325">In Microsoft Edge Version 91 oder höher löst DevTools Inlinefunktionsanforderungen auf und zeigt den Quellspeicherort in Fehlerstapelablaufverfolgungen für das Wasm-Debuggen an.</span><span class="sxs-lookup"><span data-stu-id="5e443-325">In Microsoft Edge version 91 or later, DevTools resolves inline function requests and displays the source location in Error stack traces for Wasm debugging.</span></span>  <span data-ttu-id="5e443-326">Um mehr über Fehlerstapelablaufverfolgungen in der **Konsole**zu erfahren, navigieren Sie zu ["Fehler".][DevtoolsConsoleApiError]</span><span class="sxs-lookup"><span data-stu-id="5e443-326">To learn more about Error stack traces in the **Console**, navigate to [error][DevtoolsConsoleApiError].</span></span>  

<span data-ttu-id="5e443-327">In Microsoft Edge Version 91 oder höher löst DevTools Inlinefunktionsanforderungen auf und zeigt die richtigen Fehlerstapelüberwachungen für das Wasm-Debuggen an.</span><span class="sxs-lookup"><span data-stu-id="5e443-327">In Microsoft Edge version 91 or later, DevTools resolves inline function requests and displays proper error stack traces for Wasm debugging.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5e443-328">In Microsoft Edge Version 90 und früheren Versionen wird der Quellspeicherort im Fehlerstapelablaufverfolgungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-328">In Microsoft Edge version 90 and earlier, the source location doesn't display in the Error stack traces.</span></span>  <span data-ttu-id="5e443-329">Quellspeicherorte sind `dsquare` .</span><span class="sxs-lookup"><span data-stu-id="5e443-329">Source locations include `dsquare`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5e443-330">In Microsoft Edge Version 91 und höher wird der Quellspeicherort im Fehlerstapelablaufverfolgungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e443-330">In Microsoft Edge version 91 and later, the source location displays in the Error stack traces.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png" alt-text="Vorherige Fehlerstapelüberwachungen für wasm-Debugging" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png":::
         <span data-ttu-id="5e443-332">Ordnungsgemäße Fehlerstapelüberwachungen für wasm-Debugging</span><span class="sxs-lookup"><span data-stu-id="5e443-332">Proper error stack traces for Wasm debugging</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png" alt-text="Ordnungsgemäße Fehlerstapelüberwachungen für wasm-Debugging" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png":::
         <span data-ttu-id="5e443-334">Ordnungsgemäße Fehlerstapelüberwachungen für wasm-Debugging</span><span class="sxs-lookup"><span data-stu-id="5e443-334">Proper error stack traces for Wasm debugging</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5e443-335">Navigieren Sie zu Problem [1189161][CR1189161], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5e443-335">To review the history of this feature in the Chromium open-source project, navigate to Issue [1189161][CR1189161].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="5e443-336">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="5e443-336">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="5e443-337">Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e443-337">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="5e443-338">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="5e443-338">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="5e443-339">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="5e443-339">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Verwenden der DevTools in anderen Sprachen – Neuigkeiten in DevTools (Microsoft Edge 81) | Microsoft-Dokumente"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Neuigkeiten in DevTools (Microsoft Edge 88) | Microsoft-Dokumente"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: ../../2020/11/devtools.md#css-variable-definitions-in-styles-pane "CSS-Variablendefinitionen im Bereich &quot;Formatvorlagen&quot; – Neuigkeiten in DevTools (Microsoft Edge 88) | Microsoft-Dokumente"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Neuigkeiten in DevTools (Microsoft Edge 90) | Microsoft-Dokumente"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Gruppieren von Tools im Fokusmodus – Neuigkeiten in DevTools (Microsoft Edge 90) | Microsoft-Dokumente"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: ../../../command-menu/index.md#open-the-command-menu "Öffnen des Befehlsmenüs – Ausführen von Befehlen mit dem Befehlsmenü Microsoft Edge DevTools | Microsoft-Dokumente"  
[DevtoolsConsoleApiError]: ../../../console/api.md#error "error – Konsolen-API-Referenz | Microsoft-Dokumente"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Ändern der DevTools-Spracheinstellungen | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Suchen und Beheben von Problemen mithilfe des Tools &quot;Probleme&quot; | Microsoft-Dokumente"  
[DevtoolsServiceWorkerIndex]: ../../../service-workers/index.md "Verbesserungen für Service Worker | Microsoft-Dokumente"  
[DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]: ../../../sources/index.md#using-the-debugger-pane-to-debug-javascript-code "Verwenden des Debuggerbereichs zum Debuggen von JavaScript-Code – Übersicht über das Quellentool | Microsoft-Dokumente"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: ../../../../progressive-web-apps-chromium/serviceworker.md#the-service-worker-lifecycle "Service Worker-Lebenszyklus – Verwenden von Service Workern zum Verwalten von Netzwerkanforderungen und Pushbenachrichtigungen | Microsoft-Dokumente"  
[ProgressiveWebAppsWebappmanifests]: ../../../../progressive-web-apps-chromium/webappmanifests.md "Verwenden Sie das Web App-Manifest, um Ihre progressive Web App in das Betriebssystem | Microsoft-Dokumente"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

[BrotliMain]: https://www.brotli.org "Brotli"  

[ChromestatusFeature4752739957473280]: https://chromestatus.com/feature/4752739957473280 "Feature: CSS-Eigenschaft mit Akzentfarbe | Chrome Platform Status"  

[CsswgDraftsCssUi4WidgetAccent]: https://drafts.csswg.org/css-ui-4/#widget-accent "Widget-Akzentfarben: die Akzentfarbeneigenschaft – CSS Basic User Interface Module Level 4 | Entwürfe des CSS-Arbeitsgruppen-Editors"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  
[CR11374]: https://crbug.com/v8/11374 "Problem 11374: Implementieren der überprüfung der marke für private Felder"  
[CR761019]: https://crbug.com/761019 "Problem 761019: &quot;Zum Symbol wechseln&quot; verpasst die erste Funktion und bevorzugt eine schlechtere Übereinstimmung, wenn sie alle typisierten Zeichen enthält."  
[CR862450]: https://crbug.com/862450 "Problem 862450: [css-scroll-snap] Erwägen Sie das Hinzufügen des Devtools-Features für css-Bildlauf-Snap"  
[CR979000]: https://crbug.com/979000 "Problem 979000: Quellzuordnungen mit kollidierenden Quellenpfaden funktionieren nicht."  
[CR1066604]: https://crbug.com/1066604 "Problem 1066604: DevTools: Details zur Installation und Aktivierung von ServiceWorker-Ereignissen | Chromium Fehler"  
<!--  [CR1066772]: https://crbug.com/1066772 "Issue 1066772: "  locked  -->  
[CR1076198]: https://crbug.com/1076198 "Problem 1076198: [Featureanforderung] Springen sie von der Registerkarte zur berechneten `styles` Eigenschaft"  
[CR1092093]: https://crbug.com/1092093 "Problem 1092093: Gestalten Sie Formularsteuerelemente durch Unterstützung der CSS-Eigenschaft "Akzentfarbe" farbstilfähiger".  
[CR1136655]: https://crbug.com/1136655 "Problem 1136655: Devtools: Lokalisierung V2 | Chromium Fehler"  
[CR1142705]: https://crbug.com/1142705 "Problem 1142705: Haltepunkte funktionieren nicht mehr, wenn 2 Quellmaps bei Verwendung von Webpack auf dieselbe virtuelle Datei verweisen"  
[CR1149832]: https://crbug.com/1149832 "Problem 1149832: Featureanforderung: Bildvorschau sollte auch Dateigröße anzeigen"  
[CR1158827]: https://crbug.com/1158827 "Problem 1158827: [Berechtigungsrichtlinie] Implementieren der Devtool-Unterstützung für Berechtigungsrichtlinien"  
[CR1162042]: https://crbug.com/1162042 "Problem 1162042: DevTools: Unterstützen der Deaktivierung der gzip/brotli/jxl-Inhaltscodierung"  
[CR1166577]: https://crbug.com/1166577 "Problem 1166577: ☂️ Linear Memory Inspector 1.0"  
[CR1170656]: https://crbug.com/1170656 "Problem 1170656: Systeminternes Seitenverhältnis anzeigen"  
[CR1178305]: https://crbug.com/1178305 "Problem 1178305: Debugger zeigt den Eigenschaftswert eines indizierten Elements nicht an, wenn darauf gezeigt wird"  
[CR1180794]: https://crbug.com/1180794 "Problem 1180794: Haltepunkte funktionieren nicht mit dem Verschlusscompiler inlining optimization"  
[CR1185945]: https://crbug.com/1185945 "Problem 1185945: Manifestwarnung impliziert, dass alle Symbole quadratisch | Chromium Bugs"  
[CR1186049]: https://crbug.com/1186049 "Problem 1186049: Spalte für Vary: Header im Cache Storage Viewer"  
[CR1187735]: https://crbug.com/1187735 "Problem 1187735: Barrierefreiheit: MAS2.1.1: Tastatur: Funktion &quot;Var(.)&quot; kann nicht mithilfe der Tastatur | Chromium Fehler"  
[CR1189161]: https://crbug.com/1189161 "Problem 1189161: `new Error` Stacktraces werden nicht über ENING TRANSFORMIERT"  
[CR1191465]: https://crbug.com/1191465 "Problem 1191465: STRG+UMSCHALT+O in HTML beschädigt"  

[GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Berechtigungsrichtlinienerklärer | GitHub"  

[GlitchMemoryInspectorDemoJsHtml]: https://memory-inspector.glitch.me/demo-js.html "Arbeitsspeicher in JS-| Glitch"  
[GlitchMemoryInspectorDemoWasmHtml]: https://memory-inspector.glitch.me/demo-wasm.html "Arbeitsspeicher in Wasm | Glitch"  

[GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml]: https://microsoft-edge-chromium-devtools.glitch.me/css-dbg-stories/css-scroll-snap.html "Bildlauf-Snap-Demo | Glitch"  

[GlitchPermissionPolicyDemoMain]: http://permission-policy-demo.glitch.me "| der OOPIF-Berechtigungsrichtlinie Glitch"  

[GnuSoftwareGzipManual]: https://www.gnu.org/software/gzip/manual "gzip: das Datenkomprimierungsprogramm | SYSTEMS-Betriebssystem"  

[HttpwgSpecsRfc7231HtmlHeaderVary]: https://httpwg.org/specs/rfc7231.html#header.vary "Vary – Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content | IETF-HTTP-Arbeitsgruppe"  

[JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]: https://webpack.js.org/guides/code-splitting/#:~:text=There%20are%20three%20general%20approaches%20to%20code%20splitting,Split%20code%20via%20inline%20function%20calls%20within%20modules. "Es gibt drei allgemeine Ansätze für die Codeteilung: Einstiegspunkte: Manuell geteilter Code mithilfe der Eintragskonfiguration.  Duplizierung verhindern: Verwenden Sie Eintragsabhängigkeiten oder SplitChunksPlugin, um Blöcke zu deduplizieren und aufzuteilen.  Dynamische Importe: Teilen von Code über Inlinefunktionsaufrufe innerhalb von Modulen. – | der Codeaufteilung webpack"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Verwenden von benutzerdefinierten CSS-Eigenschaften (Variablen) | MDN"  

[MdnDocsWebJavascriptReferenceOperatorsIn]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/in "in Operator | Mdn"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Image Generator | PWABuilder"  

[RollupjsMain]: https://rollupjs.org "rollup.js"  

[V8DevFeaturesPrivateBrandChecks]: https://v8.dev/features/private-brand-checks "Private Marke überprüft a.k.a. #foo in obj | V8"  
[V8DevFeaturesClassFieldsPrivateClassFields]: https://v8.dev/features/class-fields#private-class-fields "Private Klassenfelder – Öffentliche und private Klassenfelder | V8"  

[WebpackJsMain]: https://webpack.js.org "webpack"  

> [!NOTE]
> <span data-ttu-id="5e443-398">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e443-398">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5e443-399">Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-91) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="5e443-399">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-91) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="5e443-401">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5e443-401">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
