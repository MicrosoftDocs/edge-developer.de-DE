---
description: Hier erfahren Sie, wie Sie die HTTP-Cookies für eine Seite mit Microsoft Edge devtools anzeigen, bearbeiten und löschen.
title: Anzeigen, bearbeiten und Löschen von Cookies mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: eaaf4663504fc674fd70dc1ca9e0357febb529e0
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993240"
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

# <span data-ttu-id="0827d-104">Anzeigen, bearbeiten und Löschen von Cookies mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="0827d-104">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="0827d-105">[Http-Cookies][MDNHTTPCookies] werden hauptsächlich verwendet, um Benutzersitzungen zu verwalten, Benutzer Personalisierungseinstellungen zu speichern und das Benutzerverhalten nachvollziehen zu können.</span><span class="sxs-lookup"><span data-stu-id="0827d-105">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="0827d-106">Cookies sind auch die Ursache für alle ärgerlichen Einwilligungsformulare "Diese Seite verwendet Cookies", die Sie im gesamten Web sehen.</span><span class="sxs-lookup"><span data-stu-id="0827d-106">Cookies are also the cause of all of the annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="0827d-107">Im folgenden Leitfaden erfahren Sie, wie Sie die HTTP-Cookies für eine Seite mit [Microsoft Edge devtools][MicrosoftEdgeDevTools]anzeigen, bearbeiten und löschen.</span><span class="sxs-lookup"><span data-stu-id="0827d-107">The following guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="0827d-108">Öffnen des Bereichs "Cookies"</span><span class="sxs-lookup"><span data-stu-id="0827d-108">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="0827d-109">[Öffnen Sie devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="0827d-109">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="0827d-110">Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0827d-110">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="0827d-111">Der Bereich **Manifest** sollte geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="0827d-111">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="0827d-113">Abbildung 1: der Bereich "Manifest"</span><span class="sxs-lookup"><span data-stu-id="0827d-113">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="0827d-114">Erweitern Sie unter **Speicher** den Eintrag **Cookies**, und wählen Sie dann einen Ursprung aus.</span><span class="sxs-lookup"><span data-stu-id="0827d-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="0827d-116">Abbildung 2: der Bereich "Cookies"</span><span class="sxs-lookup"><span data-stu-id="0827d-116">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <span data-ttu-id="0827d-117">Felder</span><span class="sxs-lookup"><span data-stu-id="0827d-117">Fields</span></span>  

<span data-ttu-id="0827d-118">Die Tabelle " **Cookies** " enthält die folgenden Felder.</span><span class="sxs-lookup"><span data-stu-id="0827d-118">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="0827d-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="0827d-119">**Name**.</span></span>  <span data-ttu-id="0827d-120">Der Name des Cookies.</span><span class="sxs-lookup"><span data-stu-id="0827d-120">The name of the cookie.</span></span>  
*   <span data-ttu-id="0827d-121">**Value**aus.</span><span class="sxs-lookup"><span data-stu-id="0827d-121">**Value**.</span></span>  <span data-ttu-id="0827d-122">Der Wert des Cookies.</span><span class="sxs-lookup"><span data-stu-id="0827d-122">The value of the cookie.</span></span>  
*   <span data-ttu-id="0827d-123">**Domäne**aus.</span><span class="sxs-lookup"><span data-stu-id="0827d-123">**Domain**.</span></span>  <span data-ttu-id="0827d-124">Die Hosts, die das Cookie empfangen dürfen.</span><span class="sxs-lookup"><span data-stu-id="0827d-124">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="0827d-125">Siehe [Bereich der Cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="0827d-125">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="0827d-126">**Path**aus.</span><span class="sxs-lookup"><span data-stu-id="0827d-126">**Path**.</span></span>  <span data-ttu-id="0827d-127">Die URL, die in der angeforderten URL vorhanden sein muss, um die Kopfzeile zu senden `Cookie` .</span><span class="sxs-lookup"><span data-stu-id="0827d-127">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="0827d-128">Siehe [Bereich der Cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="0827d-128">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="0827d-129">**Läuft ab/max-Alter**.</span><span class="sxs-lookup"><span data-stu-id="0827d-129">**Expires / Max-Age**.</span></span>  <span data-ttu-id="0827d-130">Das Ablaufdatum oder das maximale Alter des Cookies.</span><span class="sxs-lookup"><span data-stu-id="0827d-130">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="0827d-131">Weitere Informationen finden Sie unter [permanente Cookies][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="0827d-131">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="0827d-132">Für [Sitzungscookies][MDNHTTPCookiesSession] ist dieser Wert immer `Session` .</span><span class="sxs-lookup"><span data-stu-id="0827d-132">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="0827d-133">**Größe**aus.</span><span class="sxs-lookup"><span data-stu-id="0827d-133">**Size**.</span></span>  <span data-ttu-id="0827d-134">Die Größe des Cookies in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0827d-134">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="0827d-135">**Http**.</span><span class="sxs-lookup"><span data-stu-id="0827d-135">**HTTP**.</span></span>  <span data-ttu-id="0827d-136">Ist "true", gibt dieses Feld an, dass das Cookie nur über HTTP verwendet und JavaScript-Änderungen nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0827d-136">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="0827d-137">Siehe [HttpOnly-Cookies][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="0827d-137">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="0827d-138">**Sicher**.</span><span class="sxs-lookup"><span data-stu-id="0827d-138">**Secure**.</span></span>  <span data-ttu-id="0827d-139">Ist "true", gibt dieses Feld an, dass das Cookie nur über eine sichere HTTPS-Verbindung an den Server gesendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="0827d-139">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="0827d-140">Siehe [sichere Cookies][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="0827d-140">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="0827d-141">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="0827d-141">**SameSite**.</span></span>  <span data-ttu-id="0827d-142">Enthält `strict` oder `lax` Wenn das Cookie das experimentelle [SameSite][MDNHTTPCookiesSamesite] -Attribut verwendet.</span><span class="sxs-lookup"><span data-stu-id="0827d-142">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="0827d-143">**Priorität**.</span><span class="sxs-lookup"><span data-stu-id="0827d-143">**Priority**.</span></span>  <span data-ttu-id="0827d-144">Contains `low` , `medium` \ (Standard \) oder `high` Wenn das Cookie das veraltete [Cookie Priority][ChromiumIssue232693] -Attribut verwendet.</span><span class="sxs-lookup"><span data-stu-id="0827d-144">Contains `low`, `medium` \(default\), or `high` if the cookie is using the deprecated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <span data-ttu-id="0827d-145">Filtern von Cookies</span><span class="sxs-lookup"><span data-stu-id="0827d-145">Filter cookies</span></span>  

<span data-ttu-id="0827d-146">Verwenden Sie das Textfeld " **Filter** ", um Cookies nach **Name** oder **Wert**zu filtern.</span><span class="sxs-lookup"><span data-stu-id="0827d-146">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="0827d-147">Das Filtern nach anderen Feldern wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0827d-147">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="0827d-149">Abbildung 3: Filtern von Cookies, die keinen Text enthalten</span><span class="sxs-lookup"><span data-stu-id="0827d-149">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <span data-ttu-id="0827d-150">Bearbeiten eines Cookies</span><span class="sxs-lookup"><span data-stu-id="0827d-150">Edit a cookie</span></span>  

<span data-ttu-id="0827d-151">Die Felder **Name**, **value**, **Domain**, **path**und **Expires/max-age** können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0827d-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="0827d-152">Doppelklicken Sie auf ein Feld, um es zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="0827d-152">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="0827d-154">Abbildung 4: Festlegen des Namens eines Cookies auf</span><span class="sxs-lookup"><span data-stu-id="0827d-154">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <span data-ttu-id="0827d-155">Löschen von Cookies</span><span class="sxs-lookup"><span data-stu-id="0827d-155">Delete cookies</span></span>  

<span data-ttu-id="0827d-156">Wählen Sie ein Cookie aus, **und wählen Sie ausgewählte** löschen ausgewählt löschen aus ![ ][ImageDeleteIcon]  , um das bestimmte Cookie zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0827d-156">Select a cookie and select **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="0827d-158">Abbildung 5: Löschen eines bestimmten Cookies</span><span class="sxs-lookup"><span data-stu-id="0827d-158">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="0827d-159">Wählen **Sie alle löschen** ![ aus ][ImageClearIcon]  , um alle Cookies zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0827d-159">Select **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="0827d-161">Abbildung 6: Löschen aller Cookies</span><span class="sxs-lookup"><span data-stu-id="0827d-161">Figure 6:  Clearing all cookies</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Öffnen von Microsoft Edge devtools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Chrom Problem 232693: Implementieren des Prioritäts Felds für Cookies | Chrom Fehler"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "HTTP-Cookies | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "HTTP-Cookies – permanente Cookies | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "HTTP-Cookies-SameSite Cookies | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "HTTP-Cookies – Bereich von Cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "HTTP-Cookies – sichere und HttpOnly Cookies | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "HTTP-Cookies – Sitzungscookies | MDN"  

> [!NOTE]
> <span data-ttu-id="0827d-171">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0827d-171">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0827d-172">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="0827d-172">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="0827d-174">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0827d-174">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
