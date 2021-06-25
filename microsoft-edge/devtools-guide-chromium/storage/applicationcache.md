---
description: Anzeigen von Anwendungscachedaten aus dem Anwendungsbereich von Microsoft Edge DevTools.
title: Anzeigen von Anwendungscachedaten mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 71e71555940d74f2071178be2e6daf0ec2f49dfd
ms.sourcegitcommit: d0a6959c5338cf1927093b4a9ed29a0bc0390b43
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "11615421"
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
# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a>Anzeigen von Anwendungscachedaten mit Microsoft Edge DevTools  

> [!WARNING]
> Der Anwendungscache ist veraltet, und Sie sollten die Verwendung vermeiden.  Die Anwendungscache-API wird von der Webplattform entfernt.  Navigieren Sie für weitere Informationen zu ["Vorbereiten der AppCache-Entfernung".][WebDevAppcacheRemoval]

In diesem Leitfaden erfahren Sie, wie Sie [Microsoft Edge DevTools][MicrosoftEdgeDevTools] verwenden, um [Anwendungscacheressourcen][MDNWebAPIsWindowApplicationCache] zu überprüfen.  

## <a name="view-application-cache-data"></a>Anzeigen von Anwendungscachedaten  

1.  Wählen Sie oben in DevTools das **Anwendungstool** aus.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       Der **Manifestbereich**  
    :::image-end:::  

1.  Erweitern Sie den Abschnitt **"Anwendungscache",** und wählen Sie einen Cache aus, um die Ressourcen anzuzeigen.  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Bereich "Anwendungscache"" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       Bereich **"Anwendungscache"**  
    :::image-end:::  

Jede Zeile der Tabelle stellt eine zwischengespeicherte Ressource dar.  

Die **Spalte Type ** stellt die [Kategorie der Ressource][MDNHTMLResourcesInAnApplicationCache]dar.  

| Kategorie | Details |  
|:--- |:--- |  
| `Explicit` | Diese Ressource wurde explizit im Manifest aufgeführt. |  
| `Fallback` | Die URL ist ein Fallback für eine andere Ressource.  Die URL der anderen Ressource ist in DevTools nicht aufgeführt. |  
| `Master` | Das `manifest` Attribut für die Ressource gibt an, dass der Cache das übergeordnete Element der Ressource ist. |  
| `Network` | Das Manifest gibt an, dass die Ressource aus dem Netzwerk stammen muss. |  

<!--todo:  replace "Master" phrasing if possible.  -->  

Am unteren Rand der Tabelle befinden sich Statussymbole, die Ihre Netzwerkverbindung und den Status des **Anwendungscaches**angeben.  Der **Anwendungscache** kann die folgenden Zustände aufweisen.  

| Status | Details |  
|:--- |:--- |  
| `CHECKING` | Das Manifest wird abgerufen und auf Updates überprüft. |  
| `DOWNLOADING` | Ressourcen werden dem Cache hinzugefügt. |  
| `IDLE` | Der Cache hat keine neuen Änderungen. |  
| `OBSOLETE` | Der Cache wird gelöscht. |  
| `UPDATEREADY` |  Eine neue Version des Caches ist verfügbar. |  

<!-- links -->  
[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
<!-- external links: -->
[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressourcen in einem Anwendungscache | Mdn"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache – Web-APIs | Mdn"  

[WebDevAppcacheRemoval]: https://web.dev/appcache-removal "Vorbereiten der AppCache-Entfernung | web.dev"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) zu finden und wurde von [Baskisch (Technical][KayceBasques] Writer, Chrome DevTools \& Ausrufebereich\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
