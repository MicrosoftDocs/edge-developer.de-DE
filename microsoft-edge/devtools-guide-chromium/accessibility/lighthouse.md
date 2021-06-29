---
description: Testen der Barrierefreiheit mithilfe von "Commerce" in DevTools.
title: Testen Sie die Barrierefreiheit mithilfe von Lighthouse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 822c25240ba30df31416ca783bf48d6d9ba52ed2
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624633"
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

# <a name="test-accessibility-using-lighthouse"></a>Testen Sie die Barrierefreiheit mithilfe von Lighthouse

Sie können Mithilfe von "Kerberos" in DevTools die Barrierefreiheit einer Seite überwachen und einen Bericht generieren. Sie können mit dem Tool "Werkzeuge" Folgendes ermitteln:

*   Gibt an, ob eine Seite für Bildschirmleseprogramme ordnungsgemäß markiert ist.  
*   Gibt an, ob die Textelemente auf einer Seite mithilfe der Farbauswahl über ausreichende Kontrastverhältnisse verfügen. Navigieren Sie für weitere Informationen [mithilfe der Farbauswahl zu "Textfarbkontrast testen".](color-picker.md)   

> [!NOTE]
> Das **Tool "Jugend"** enthält Links zu Inhalten, die auf Websites von Drittanbietern gehostet werden.  Microsoft ist nicht verantwortlich für und hat keine Kontrolle über den Inhalt dieser Websites und alle Daten, die gesammelt werden können.  

Führen Sie die folgenden Schritte aus, um eine Seite mithilfe des Tools "Werben" zu überwachen.

1.  Navigieren Sie zu der URL, die Sie überwachen möchten.
1.  Wählen Sie in DevTools das **Tool "Werkzeuge" aus.**  Konfigurationsoptionen werden angezeigt.
    
    :::image type="complex" source="../media/accessibility-lighthouse.msft.png" alt-text="Konfigurationsoptionen für Konfigurationskonfigurationen" lightbox="../media/accessibility-lighthouse.msft.png":::
       Konfigurationsoptionen für Konfigurationskonfigurationen
    :::image-end:::  
    
1.  Wählen Sie für **"Gerät"** die Option **"Mobil"** aus, wenn Sie ein mobiles Gerät simulieren möchten.  Diese Option ändert die Zeichenfolge des Benutzer-Agenten und ändert die Größe des Viewports.  Diese Option kann sich auf die Überwachungsergebnisse auswirken.
1.  Wählen Sie im Abschnitt **"Kategorien"** die Option **"Barrierefreiheit" aus.**
1.  Wählen Sie **Bericht generieren aus.** Nach 10 bis 30 Sekunden zeigt DevTools einen Bericht an.  Der Bericht enthält Tipps zur Verbesserung der Barrierefreiheit der Seite.  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result.msft.png" alt-text="Bericht "Ein Barrierefreiheitsbericht" für die Kategorie "Barrierefreiheit"" lightbox="../media/accessibility-lighthouse-result.msft.png":::
       Bericht "Ein **Barrierefreiheitsbericht"** für die Kategorie "Barrierefreiheit"
    :::image-end:::  
    
1.  Wählen Sie ein Element im Bericht aus, um mehr darüber zu erfahren.  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result-issue-expanded.msft.png" alt-text="Ein erweitertes Problem in einem Bericht zum Thema"." lightbox="../media/accessibility-lighthouse-result-issue-expanded.msft.png":::
       Ein erweitertes Problem in einem Bericht zum Thema".
    :::image-end:::  
    
1.  Wählen Sie den Link **"Weitere Informationen"** aus, um die Dokumentation des Problems anzuzeigen.
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Anzeigen der Dokumentation eines Problems" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Anzeigen der Dokumentation eines Problems
    :::image-end:::  

1.  Um zu den Konfigurationsoptionen zurückzukehren, wählen Sie in DevTools **eine Überwachung (** ) `+` aus.    


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) zu finden und wurde von [Kaince Baskisch][KayceBasques] \(Technical Writer, Chrome DevTools \& Ausrufebereich\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  


<!-- links -->  
[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd "axe – Web Accessibility Testing – Chrome Web Store"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
