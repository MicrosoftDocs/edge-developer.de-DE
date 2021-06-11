---
description: Verwenden Sie das Tool "Probleme", um Probleme mit Ihrer Website zu suchen und zu beheben.
title: Suchen und Beheben von Problemen mit dem Tool "Microsoft Edge DevTools-Probleme"
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 17c1162bdec21ccc4abe1d3d34ce7c766aeb1009
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11596989"
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
# <a name="find-and-fix-problems-with-the-microsoft-edge-devtools-issues-tool"></a>Suchen und Beheben von Problemen mit dem Tool "Microsoft Edge DevTools-Probleme"  

Das **Tool "Probleme"** in Microsoft Edge DevTools reduziert die Benachrichtigungsermüdung und -unübersichtlichkeit der **Konsole.**  Verwenden Sie es, um Lösungen für vom Browser erkannte Probleme zu finden, z. B. Cookieprobleme und gemischte Inhalte.  

> [!NOTE]
> In Microsoft Edge 84 unterstützt **das** Problemtool drei Arten von Problemen:  
> *   [Cookieprobleme][MDNSameSiteCookies]  
> *   [Gemischter Inhalt][MDNMixedContent]  
> *   [COEP-Probleme][W3CCOEPSpec]
> 
> Das Microsoft Edge DevTools-Team plant, weitere Problemtypen in zukünftigen Versionen von Microsoft Edge zu unterstützen.  

## <a name="open-the-issues-tool-in-the-devtools-drawer"></a>Öffnen des Tools "Probleme" in der DevTools-Schublade  

1.  Navigieren Sie zu einer Webseite, z. [B. samesite-sandbox.glitch.me,][GlitchSamesiteSandbox]die Zu behebende Probleme enthält.  
1.  [Öffnen Sie DevTools][DevtoolsOpen].  
1.  :::row:::
       :::column span="":::
          Klicken Sie auf der gelben Warnleiste auf die Schaltfläche **"Zu Problemen wechseln".**  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Wechseln Sie zur Schaltfläche Probleme in der gelben Warnleiste, wenn Probleme erkannt werden." lightbox="../media/issues-open-issues-tab.msft.png":::
             Die Schaltfläche **"Zu Problemen wechseln"** in der gelben Warnleiste, wenn Probleme erkannt werden.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Alternativ können Sie im Menü **"Weitere Tools"** die Option **"Probleme"** auswählen.  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Problemtool im Menü Weitere Tools" lightbox="../media//issues-more-tools-menu.msft.png":::
             **Problemtool** im Menü **"Weitere Tools"**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Wählen Sie bei Bedarf die Schaltfläche **"Seite neu laden"** aus.  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Problemtool in der DevTools-Schublade mit der Schaltfläche Seite neu laden" lightbox="../media/issues-tab-before-refresh.msft.png":::
       **Problemtool** in der DevTools-Schublade mit der Schaltfläche **"Seite neu laden"**  
    :::image-end:::  

    Die in der **Konsole** gemeldeten Probleme sind schwer zu verstehen, z. B. die Cookiewarnungen in der folgenden Abbildung.  Basierend auf den gemeldeten Problemen ist möglicherweise nicht klar, was Sie tun müssen.  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Problemtool in der DevTools-Schublade mit drei Cookie-Problemen" lightbox="../media/issues-tab-after-refresh.msft.png":::
       **Problemtool** in der DevTools-Schublade mit drei Cookie-Problemen  
    :::image-end:::  
    
## <a name="view-items-in-the-issues-tool"></a>Anzeigen von Elementen im Tool "Probleme"  

Das Tool **"Probleme"** in der DevTools-Schublade zeigt Warnungen strukturiert, aggregiert und umsetzbar an.  

1.  Wählen Sie ein Element im **Tool "Probleme"** aus, um Anleitungen zum Beheben des Problems und zum Auffinden betroffener Ressourcen zu erhalten.  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Markieren websiteübergreifender Cookies als sicheres Problem im Tool Probleme" lightbox="../media/issues-tab-issue-open.msft.png":::
       **Markieren websiteübergreifender Cookies als sicheres** Problem im **Tool "Probleme"**  
    :::image-end:::  
    
    Jedes Element hat vier Komponenten:  
    
    *   Eine Überschrift, die das Problem beschreibt.  
    *   Eine Beschreibung, die den Kontext und die Lösung bereitstellt.  
    *   Ein **Abschnitt "BETROFFENE RESSOURCEN",** der mit Ressourcen im entsprechenden DevTools-Kontext verknüpft ist, z. B. dem Netzwerkbereich.  
    *   Links zu weiteren Anleitungen.  
    
1.  Wählen Sie Elemente in **BETROFFENEN RESSOURCEN** aus, um Details anzuzeigen.  Im folgenden Beispiel betrifft das Problem **"Websiteübergreifende Cookies als sicher** markieren" ein Cookie und zwei Anforderungen.  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Betroffene Ressourcen im Tool Probleme geöffnet" lightbox="../media/issues-tab-affected-resources.msft.png":::
       Betroffene Ressourcen im **Tool "Probleme"** in der DevTools-Schublade geöffnet  
    :::image-end:::  
    
## <a name="view-issues-in-context"></a>Anzeigen von Problemen im Kontext  

1.  Wählen Sie einen Ressourcenlink aus, um das Element im entsprechenden Kontext in DevTools anzuzeigen.  Wählen Sie im folgenden Beispiel `samesite-sandbox.glitch.me` unter **"Anforderungen"** aus, um die an diese Anforderung angefügten Cookies anzuzeigen.  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Anzeigen des betroffenen Cookies im DevTools-Netzwerktool" lightbox="../media/issues-tab-view-request.msft.png":::
       Anzeigen des betroffenen Cookies im **DevTools-Netzwerktool**  
    :::image-end:::  

1.  Scrollen Sie, um das Element mit einem Problem anzuzeigen: für das folgende Beispiel das `ck02` Cookie.  Zeigen Sie auf die **SameSite-Spalte,** um den Wert zu `None` überprüfen, den das Problem erkannt hat.  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Kein Wert in der SameSite-Spalte für das ck02-Cookie im DevTools-Netzwerktool" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` Wert in der **SameSite-Spalte** für das `ck02` Cookie im **DevTools-Netzwerktool**  
    :::image-end:::  


## <a name="see-also"></a>Weitere Informationen:

* [Automatisches Testen einer Webseite auf Barrierefreiheitsprobleme](../accessibility/test-issues-tool.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Öffnen sie Microsoft Edge DevTools-| Microsoft-Dokumente"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "SameSite-Cookietests | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite-Cookies | Mdn"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Gemischte Inhalte | Mdn"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Cross-Origin Embedder Policy | Web-Community-Gruppe"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/issues/index) gefunden und von [Sam Dutton][SamDutton] \(Developer Advocate\) verfasst.  
[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton  
