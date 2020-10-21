---
description: Überprüfen Sie mithilfe des Sicherheits Panels, ob eine Seite vollständig durch HTTPS geschützt ist.
title: Grundlegendes zu Sicherheitsproblemen mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 09f7e641ddd8da74c361980b9ce61b212a8477fe
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125384"
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

# <span data-ttu-id="637c6-104">Grundlegendes zu Sicherheitsproblemen mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="637c6-104">Understand security issues with Microsoft Edge DevTools</span></span>  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <span data-ttu-id="637c6-105">Öffnen des Fensters "Sicherheit"</span><span class="sxs-lookup"><span data-stu-id="637c6-105">Open the Security panel</span></span>  

<span data-ttu-id="637c6-106">Der Bereich " **Sicherheit** " ist der wichtigste Ort in devtools, um die Sicherheit einer Seite zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="637c6-106">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="637c6-107">[Öffnen Sie devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="637c6-107">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="637c6-108">Wählen Sie die Registerkarte **Sicherheit** aus, um das **Sicherheits** Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="637c6-108">Choose the **Security** tab to open the **Security** panel.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Das Sicherheitspanel" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="637c6-110">Das **Sicherheits** Panel</span><span class="sxs-lookup"><span data-stu-id="637c6-110">The **Security** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="637c6-111">Häufig auftretende Probleme</span><span class="sxs-lookup"><span data-stu-id="637c6-111">Common problems</span></span>  

### <span data-ttu-id="637c6-112">Nicht sichere Haupt Ursprünge</span><span class="sxs-lookup"><span data-stu-id="637c6-112">Non-secure main origins</span></span>  

<span data-ttu-id="637c6-113">Wenn der Haupt Ursprung einer Seite nicht sicher ist, lautet die **Sicherheitsübersicht** , dass **Diese Seite nicht sicher ist**.</span><span class="sxs-lookup"><span data-stu-id="637c6-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Das Sicherheitspanel" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="637c6-115">Eine nicht sichere Seite</span><span class="sxs-lookup"><span data-stu-id="637c6-115">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="637c6-116">Dieses Problem tritt auf, wenn die URL, die Sie besucht haben, über HTTP angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="637c6-116">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="637c6-117">Um die Sicherheit zu gewährleisten, müssen Sie Sie über HTTPS anfordern.</span><span class="sxs-lookup"><span data-stu-id="637c6-117">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="637c6-118">Wenn Sie beispielsweise die URL in der Adressleiste betrachten, sieht Sie wahrscheinlich ähnlich aus `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="637c6-118">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="637c6-119">Um die URL zu sichern, sollte die URL `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="637c6-119">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="637c6-120">Wenn Sie bereits HTTPS auf dem Server eingerichtet haben, müssen Sie lediglich den Server so konfigurieren, dass alle HTTP-Anforderungen an https umgeleitet werden, um dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="637c6-120">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="637c6-121">Wenn Sie HTTPS auf dem Server nicht eingerichtet haben, können Sie durch [verschlüsseln][LetsEncrypt] eine ﻿kostenlose und relativ einfache Möglichkeit zum Starten des Prozesses bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="637c6-121">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="637c6-122">Oder Sie können das Hosten Ihrer Website in einem CDN in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="637c6-122">Or, you might consider hosting your site on a CDN.</span></span>  <span data-ttu-id="637c6-123">Die meisten wichtigen CDNs-Host Websites sind jetzt standardmäßig auf HTTPS.</span><span class="sxs-lookup"><span data-stu-id="637c6-123">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="637c6-124">Der [use https][WebhintUseHttps] -Hinweis in [webhint][Webhint] kann dazu beitragen, den Vorgang zu automatisieren, um sicherzustellen, dass alle HTTP-Anforderungen an https weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="637c6-124">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <span data-ttu-id="637c6-125">Gemischter Inhalt</span><span class="sxs-lookup"><span data-stu-id="637c6-125">Mixed content</span></span>  

<span data-ttu-id="637c6-126">**Gemischte Inhalte** bedeuten, dass der Haupt Ursprung einer Seite sicher ist, die Seite jedoch Ressourcen von nicht sicheren Ursprüngen angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="637c6-126">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="637c6-127">Gemischte Inhaltsseiten sind nur teilweise geschützt, da der HTTP-Inhalt für Sniffer zugänglich und anfällig für man-in-the-Middle-Angriffe ist.</span><span class="sxs-lookup"><span data-stu-id="637c6-127">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Das Sicherheitspanel" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="637c6-129">Gemischter Inhalt</span><span class="sxs-lookup"><span data-stu-id="637c6-129">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="637c6-130">Wählen Sie in der vorherigen Abbildung **in der Netzwerksteuerung Ansicht 1 anfordern** aus, um die **Netzwerk** Steuerung zu öffnen und den Filter anzuwenden, `mixed-content:displayed` damit im **Netzwerkprotokoll** nur nicht sichere Ressourcen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="637c6-130">In the previous figure, choose **View 1 request in Network panel** to open the **Network** panel and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Das Sicherheitspanel" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="637c6-132">Gemischte Ressourcen im **Netzwerkprotokoll**</span><span class="sxs-lookup"><span data-stu-id="637c6-132">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <span data-ttu-id="637c6-133">Details anzeigen</span><span class="sxs-lookup"><span data-stu-id="637c6-133">View details</span></span>  

### <span data-ttu-id="637c6-134">Haupt Ursprungszertifikat anzeigen</span><span class="sxs-lookup"><span data-stu-id="637c6-134">View main origin certificate</span></span>  

<span data-ttu-id="637c6-135">Wählen Sie in der **Übersicht Sicherheit**die Option **Zertifikat anzeigen** aus, um das Zertifikat schnell auf den Haupt Ursprung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="637c6-135">From the **Security Overview**, choose **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Das Sicherheitspanel" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="637c6-137">Ein Haupt Ursprungszertifikat</span><span class="sxs-lookup"><span data-stu-id="637c6-137">A main origin certificate</span></span>  
:::image-end:::  

### <span data-ttu-id="637c6-138">Anzeigen von Ursprungs Details</span><span class="sxs-lookup"><span data-stu-id="637c6-138">View origin details</span></span>  

<span data-ttu-id="637c6-139">Klicken Sie auf einen der Einträge im Navigationsbereich auf der linken Seite, um die Details des Ursprungs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="637c6-139">Click one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="637c6-140">Auf der Seite "Details" können Sie die Verbindungs-und Zertifikatinformationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="637c6-140">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="637c6-141">Die Informationen zur Transparenz der Zertifikate werden ebenfalls angezeigt, wenn Sie verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="637c6-141">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Das Sicherheitspanel" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="637c6-143">Details des Haupt Ursprungs</span><span class="sxs-lookup"><span data-stu-id="637c6-143">Main origin details</span></span>  
:::image-end:::  

## <span data-ttu-id="637c6-144">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="637c6-144">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  
[DevToolsOpen]: ../open.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  
[LetsEncrypt]: https://letsencrypt.org "Verschlüsseln-﻿kostenlose SSL/TLS-Zertifikate"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Verwenden von HTTPS | webhint-Dokumentation"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="637c6-150">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="637c6-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="637c6-151">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/security/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="637c6-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="637c6-153">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="637c6-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
