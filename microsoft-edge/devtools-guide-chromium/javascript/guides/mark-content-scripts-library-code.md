---
description: Aktivieren Sie "Inhalts Skripts als Bibliothekscode markieren" aus Einstellungen > Framework-Bibliothekscode.
title: Markieren von Inhaltsskripts als Bibliothekscode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 2a9bca703004b6232bef857d7b9e2f45458db52d
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124698"
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

# Markieren von Inhalts Skripts als Bibliothekscode  

Wenn Sie den Quellcode **-Panel von** Microsoft Edge devtools verwenden, um Code zu [durchlaufen][DevToolsJavascriptStepThroughCode], können Sie manchmal auf Code pausieren, den Sie nicht erkennen.  Wahrscheinlich haben Sie den Code für eine der installierten Microsoft-Edge-Erweiterungen angehalten.  Führen Sie die folgenden Schritte aus, um den Erweiterungscode nicht zu unterbrechen.  

1.  Öffnen Sie devtools, wählen Sie **anpassen und Steuer devtools** \ ( `...` \) aus, und wählen Sie **Einstellungen**aus.  Sie können die **Einstellungen** auch öffnen, indem Sie auswählen `F1` .  

1.  Wählen Sie die Registerkarte " **Bibliothekscode** " aus, um den Abschnitt " **Framework Library Code** " von **Settings**zu öffnen.  
1.  Aktivieren Sie das Kontrollkästchen **Inhalts Skripts als Bibliothekscode markieren** .  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Aktivieren des Kontrollkästchens &quot;Inhalts Skripts als Bibliothekscode markieren&quot;" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       Aktivieren des Kontrollkästchens " **Inhalts Skripts als Bibliothekscode markieren** "  
    :::image-end:::  
    
## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Schritt 4: schrittweise durch den Code – erste Schritte mit dem Debuggen von JavaScript in Microsoft Edge devtools | Microsoft docs"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
