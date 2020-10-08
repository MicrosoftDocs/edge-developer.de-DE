---
description: Öffnen Sie die Konsole, erstellen Sie einen Live Ausdruck, und legen Sie den Ausdruck auf Document. activeElement.
title: Nachverfolgen, welches Element den Fokus hat
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 9000b8ca1fa52daf5257f201c65dcabd78298ec7
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993205"
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

# Nachverfolgen, welches Element den Fokus hat  

Angenommen, Sie testen die Barrierefreiheit der Tastaturnavigation auf einer Seite.  Beim Navigieren auf der Seite mit dem `Tab` Schlüssel verschwindet der Fokus Ring manchmal, da das Element mit dem Fokus ausgeblendet ist.  

Führen Sie die folgenden Aktionen aus, um das fokussierte Element in devtools zu verfolgen.  

1.  Öffnen Sie die **Konsole**.  
1.  Klicken Sie auf **Live Ausdruck erstellen** \ ( ![ Live Ausdruck erstellen ][ImageCreateIcon] \).  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Erstellen eines Live Ausdrucks" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       Erstellen eines Live Ausdrucks  
    :::image-end:::  
    
1.  Geben Sie `document.activeElement` ein.  
1.  Klicken Sie auf eine Stelle außerhalb der **Live Ausdruck** -Benutzeroberfläche, um Sie zu speichern.  
    
Der unten angezeigte Wert `document.activeElement` ist das Ergebnis des Ausdrucks.  

Da dieser Ausdruck immer das Focused-Element darstellt, haben Sie jetzt die Möglichkeit, immer nachzuverfolgen, welches Element den Fokus hat.  

*   Zeigen Sie mit der Maus auf das Ergebnis, um das fokussierte Element im Viewport zu markieren.  
*   Klicken Sie mit der rechten Maustaste auf das Ergebnis, und wählen Sie **im Element Fenster** anzeigen aus, um das Element in der DOM- **Struktur im Element Panel anzuzeigen** .  
*   Klicken Sie mit der rechten Maustaste auf das Ergebnis, und wählen Sie **als globale Variable speichern** aus, um einen Variablen Bezug auf den Knoten zu erstellen, den Sie in der **Konsole**verwenden können.  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
