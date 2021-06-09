---
description: Testen der Barrierefreiheit mithilfe von "Commerce" in DevTools.
title: Testen Sie die Barrierefreiheit mithilfe von Lighthouse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: bb158085eb516c8d4ce37a22f6b612784db51461
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597477"
---
<!-- this article was created on 05/11/2021 by moving a section out from the "Accessibility reference" article (reference.md) -->
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

# <a name="test-accessibility-using-lighthouse"></a><span data-ttu-id="457d0-104">Testen Sie die Barrierefreiheit mithilfe von Lighthouse</span><span class="sxs-lookup"><span data-stu-id="457d0-104">Test accessibility using Lighthouse</span></span>

<span data-ttu-id="457d0-105">Sie können Mithilfe von "Kerberos" in DevTools die Barrierefreiheit einer Seite überwachen und einen Bericht generieren.</span><span class="sxs-lookup"><span data-stu-id="457d0-105">You can use Lighthouse from within DevTools to audit the accessibility of a page and generate a report.</span></span> <span data-ttu-id="457d0-106">Sie können mit dem Tool "Werkzeuge" Folgendes ermitteln:</span><span class="sxs-lookup"><span data-stu-id="457d0-106">You can use the Lighthouse tool to determine:</span></span>

*   <span data-ttu-id="457d0-107">Gibt an, ob eine Seite für Bildschirmleseprogramme ordnungsgemäß markiert ist.</span><span class="sxs-lookup"><span data-stu-id="457d0-107">Whether a page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="457d0-108">Gibt an, ob die Textelemente auf einer Seite mithilfe der Farbauswahl über ausreichende Kontrastverhältnisse verfügen.</span><span class="sxs-lookup"><span data-stu-id="457d0-108">Whether the text elements on a page have sufficient contrast ratios using the Color Picker.</span></span> <span data-ttu-id="457d0-109">Navigieren Sie für weitere Informationen [mithilfe der Farbauswahl zu "Textfarbkontrast testen".](color-picker.md)</span><span class="sxs-lookup"><span data-stu-id="457d0-109">For more information, navigate to [Test text-color contrast using the Color Picker](color-picker.md).</span></span>   

> [!NOTE]
> <span data-ttu-id="457d0-110">Das **Tool "Jugend"** enthält Links zu Inhalten, die auf Websites von Drittanbietern gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="457d0-110">The **Lighthouse** tool provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="457d0-111">Microsoft ist nicht verantwortlich für und hat keine Kontrolle über den Inhalt dieser Websites und alle Daten, die gesammelt werden können.</span><span class="sxs-lookup"><span data-stu-id="457d0-111">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="457d0-112">Führen Sie die folgenden Schritte aus, um eine Seite mithilfe des Tools "Werben" zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="457d0-112">To audit a page using the Lighthouse tool, perform the following steps.</span></span>

1.  <span data-ttu-id="457d0-113">Navigieren Sie zu der URL, die Sie überwachen möchten.</span><span class="sxs-lookup"><span data-stu-id="457d0-113">Navigate to the URL that you want to audit.</span></span>
1.  <span data-ttu-id="457d0-114">Wählen Sie in DevTools das **Tool "Werkzeuge" aus.**</span><span class="sxs-lookup"><span data-stu-id="457d0-114">In DevTools, select the **Lighthouse** tool.</span></span>  <span data-ttu-id="457d0-115">Konfigurationsoptionen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="457d0-115">Configuration options are displayed.</span></span>
    
    :::image type="complex" source="../media/accessibility-lighthouse.msft.png" alt-text="Konfigurationsoptionen für Konfigurationskonfigurationen" lightbox="../media/accessibility-lighthouse.msft.png":::
       <span data-ttu-id="457d0-117">Konfigurationsoptionen für Konfigurationskonfigurationen</span><span class="sxs-lookup"><span data-stu-id="457d0-117">Lighthouse configuration options</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="457d0-118">Wählen Sie für **"Gerät"** die Option **"Mobil"** aus, wenn Sie ein mobiles Gerät simulieren möchten.</span><span class="sxs-lookup"><span data-stu-id="457d0-118">For **Device**, select **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="457d0-119">Diese Option ändert die Zeichenfolge des Benutzer-Agenten und ändert die Größe des Viewports.</span><span class="sxs-lookup"><span data-stu-id="457d0-119">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="457d0-120">Diese Option kann sich auf die Überwachungsergebnisse auswirken.</span><span class="sxs-lookup"><span data-stu-id="457d0-120">This option can affect the audit results.</span></span>
1.  <span data-ttu-id="457d0-121">Wählen Sie im Abschnitt **"Kategorien"** die Option **"Barrierefreiheit" aus.**</span><span class="sxs-lookup"><span data-stu-id="457d0-121">In the **Categories** section, select **Accessibility**.</span></span>
1.  <span data-ttu-id="457d0-122">Wählen Sie **Bericht generieren aus.**</span><span class="sxs-lookup"><span data-stu-id="457d0-122">Select **Generate report**.</span></span> <span data-ttu-id="457d0-123">Nach 10 bis 30 Sekunden zeigt DevTools einen Bericht an.</span><span class="sxs-lookup"><span data-stu-id="457d0-123">After 10 to 30 seconds, DevTools displays a report.</span></span>  <span data-ttu-id="457d0-124">Der Bericht enthält Tipps zur Verbesserung der Barrierefreiheit der Seite.</span><span class="sxs-lookup"><span data-stu-id="457d0-124">The report gives tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result.msft.png" alt-text="Bericht "Ein Barrierefreiheitsbericht" für die Kategorie "Barrierefreiheit"" lightbox="../media/accessibility-lighthouse-result.msft.png":::
       <span data-ttu-id="457d0-126">Bericht "Ein **Barrierefreiheitsbericht"** für die Kategorie "Barrierefreiheit"</span><span class="sxs-lookup"><span data-stu-id="457d0-126">A Lighthouse report for the **Accessibility** category</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="457d0-127">Wählen Sie ein Element im Bericht aus, um mehr darüber zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="457d0-127">Select an item in the report to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result-issue-expanded.msft.png" alt-text="Ein erweitertes Problem in einem Bericht zum Thema"." lightbox="../media/accessibility-lighthouse-result-issue-expanded.msft.png":::
       <span data-ttu-id="457d0-129">Ein erweitertes Problem in einem Bericht zum Thema".</span><span class="sxs-lookup"><span data-stu-id="457d0-129">An expanded issue in a Lighthouse report</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="457d0-130">Wählen Sie den Link **"Weitere Informationen"** aus, um die Dokumentation des Problems anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="457d0-130">Select the **Learn more** link to view the documentation of the issue.</span></span>
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Anzeigen der Dokumentation eines Problems" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="457d0-132">Anzeigen der Dokumentation eines Problems</span><span class="sxs-lookup"><span data-stu-id="457d0-132">View the documentation of an issue</span></span>
    :::image-end:::  

1.  <span data-ttu-id="457d0-133">Um zu den Konfigurationsoptionen zurückzukehren, wählen Sie in DevTools **eine Überwachung (** ) `+` aus.</span><span class="sxs-lookup"><span data-stu-id="457d0-133">To return to the configuration options, in DevTools, select **Perform an audit** (`+`).</span></span>    


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="457d0-134">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="457d0-134">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="457d0-135">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="457d0-135">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="457d0-136">Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) zu finden und wurde von [Baskisch (Technical][KayceBasques] Writer, Chrome DevTools \& Ausrufebereich\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="457d0-136">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="457d0-138">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="457d0-138">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->  
[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe – Web Accessibility Testing – Chrome Web Store"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
