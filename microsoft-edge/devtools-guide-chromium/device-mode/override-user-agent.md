---
description: Öffnen Sie die Registerkarte Netzwerkbedingungen, deaktivieren Sie automatisch auswählen, und wählen Sie aus der Liste aus, oder geben Sie eine benutzerdefinierte Zeichenfolge ein.
title: Überschreiben der Benutzer-Agent-Zeichenfolge von Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: befbe186a5992c651f877a18f1c3232bf212394a
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124950"
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

# Überschreiben der Benutzer-Agent-Zeichenfolge von Microsoft Edge devtools  

So überschreiben Sie die Zeichenfolge des [Benutzer-Agents][MDNUserAgent] von Microsoft Edge devtools:  

1.  Wählen Sie `Control` + `Shift` + `P` \ (Windows, Linux \) oder `Command` + `Shift` + `P` \ (macOS \) aus, um das **Befehlsmenü**zu öffnen.  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-console-command-menu.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Geben `network conditions` Sie **Netzwerkbedingungen anzeigen**ein, und wählen Sie aus, `Enter` um die Registerkarte **Netzwerkbedingungen** zu öffnen.  
1.  Deaktivieren Sie im Abschnitt **Benutzer-Agent** das Kontrollkästchen **automatisch auswählen** .  
    
    :::image type="complex" source="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png":::
       **Automatisches auswählen** deaktivieren  
    :::image-end:::  
    
1.  Wählen Sie eine Benutzer-Agent-Zeichenfolge aus der Liste aus, oder geben Sie eine eigene benutzerdefinierte Zeichenfolge ein.  
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Benutzer-Agent | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
