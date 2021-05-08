---
description: Anzeigen und Bearbeiten von localStorage mit dem Bereich "Lokaler Speicher" und der Konsole.
title: Anzeigen und Bearbeiten des lokalen Speichers mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 4eebf3108e7b1c6ecaecbfed445e8f3fe26215c4
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439675"
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

# <a name="view-and-edit-local-storage-with-microsoft-edge-devtools"></a><span data-ttu-id="143f4-104">Anzeigen und Bearbeiten des lokalen Speichers mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="143f4-104">View and edit local storage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="143f4-105">In diesem Handbuch erfahren Sie, wie [Sie Microsoft Edge DevTools][MicrosoftEdgeDevTools] zum Anzeigen, Bearbeiten und Löschen von localStorage-Schlüssel-Wert-Paaren verwenden. [][MDNWindowsLocalStorage]</span><span class="sxs-lookup"><span data-stu-id="143f4-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <a name="view-localstorage-keys-and-values"></a><span data-ttu-id="143f4-106">Anzeigen von localStorage-Schlüsseln und -Werten</span><span class="sxs-lookup"><span data-stu-id="143f4-106">View localStorage keys and values</span></span>  

1.  <span data-ttu-id="143f4-107">Wählen Sie die **Registerkarte Anwendung** aus, um das **Anwendungstool zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="143f4-107">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="143f4-108">Der **Manifestbereich** wird standardmäßig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="143f4-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="143f4-110">Der **Manifestbereich**</span><span class="sxs-lookup"><span data-stu-id="143f4-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="143f4-111">Erweitern Sie **das Menü Lokaler Speicher.**</span><span class="sxs-lookup"><span data-stu-id="143f4-111">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Menü "Lokaler Speicher"" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="143f4-113">Menü **"Lokaler Speicher"**</span><span class="sxs-lookup"><span data-stu-id="143f4-113">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="143f4-114">Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="143f4-114">Choose a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Die localStorage-Schlüssel-Wert-Paare für die https://www.bing.com Domäne" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="143f4-116">Die `localStorage` Schlüssel-Wert-Paare für die `https://www.bing.com` Domäne</span><span class="sxs-lookup"><span data-stu-id="143f4-116">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="143f4-117">Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unterhalb der Tabelle anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="143f4-117">Choose a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Anzeigen des Werts des eventLogQueue_Online Schlüssels" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="143f4-119">Anzeigen des Werts des `eventLogQueue_Online` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="143f4-119">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <a name="create-a-new-localstorage-key-value-pair"></a><span data-ttu-id="143f4-120">Erstellen eines neuen localStorage-Schlüssel-Wert-Paars</span><span class="sxs-lookup"><span data-stu-id="143f4-120">Create a new localStorage key-value pair</span></span>  

1.  <span data-ttu-id="143f4-121">[Zeigen Sie die localStorage-Schlüssel-Wert-Paare einer Domäne an.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="143f4-121">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="143f4-122">Doppelklicken Sie auf den leeren Teil der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="143f4-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="143f4-123">DevTools erstellt eine neue Zeile und konzentriert den Cursor in der **Spalte Schlüssel.**</span><span class="sxs-lookup"><span data-stu-id="143f4-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Der leere Teil der Tabelle, auf den sie doppelklicken soll, um ein neues Schlüssel-Wert-Paar zu erstellen." lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="143f4-125">Der leere Teil der Tabelle, auf den sie doppelklicken soll, um ein neues Schlüssel-Wert-Paar zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="143f4-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <a name="edit-localstorage-keys-or-values"></a><span data-ttu-id="143f4-126">Bearbeiten von localStorage-Schlüsseln oder -Werten</span><span class="sxs-lookup"><span data-stu-id="143f4-126">Edit localStorage keys or values</span></span>  

1.  <span data-ttu-id="143f4-127">[Zeigen Sie die localStorage-Schlüssel-Wert-Paare einer Domäne an.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="143f4-127">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="143f4-128">Doppelklicken Sie in der Spalte **Schlüssel** oder **Wert** auf eine Zelle, um diesen Schlüssel oder Wert zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="143f4-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Bearbeiten eines localStorage-Schlüssels" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="143f4-130">Bearbeiten eines `localStorage` Schlüssels</span><span class="sxs-lookup"><span data-stu-id="143f4-130">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <a name="delete-localstorage-key-value-pairs"></a><span data-ttu-id="143f4-131">Löschen von localStorage-Schlüssel-Wert-Paaren</span><span class="sxs-lookup"><span data-stu-id="143f4-131">Delete localStorage key-value pairs</span></span>  

1.  <span data-ttu-id="143f4-132">[Zeigen Sie `localStorage` die Schlüssel-Wert-Paare einer Domäne an.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="143f4-132">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="143f4-133">Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="143f4-133">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="143f4-134">DevTools hebt es blau hervor, um anzugeben, dass es ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="143f4-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="143f4-135">Wählen Sie `Delete` den Schlüssel aus, oder wählen **Sie Ausgewählte \(** ![ Ausgewählte Option löschen ](../media/delete-icon.msft.png) \) aus.</span><span class="sxs-lookup"><span data-stu-id="143f4-135">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
## <a name="delete-all-localstorage-key-value-pairs-for-a-domain"></a><span data-ttu-id="143f4-136">Löschen aller `localStorage` Schlüssel-Wert-Paare für eine Domäne</span><span class="sxs-lookup"><span data-stu-id="143f4-136">Delete all `localStorage` key-value pairs for a domain</span></span>  

1.  <span data-ttu-id="143f4-137">[Zeigen Sie `localStorage` die Schlüssel-Wert-Paare einer Domäne an.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="143f4-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="143f4-138">Wählen **Sie Alle löschen** \( Alle löschen ![ ](../media/clear-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="143f4-138">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\).</span></span>  
    
## <a name="interact-with-localstorage-from-the-console"></a><span data-ttu-id="143f4-139">Interagieren mit localStorage über die Konsole</span><span class="sxs-lookup"><span data-stu-id="143f4-139">Interact with localStorage from the Console</span></span>  

<span data-ttu-id="143f4-140">Da Sie JavaScript in der Konsole ausführen \*\*\*\* können **und**die Konsole Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit über die Konsole `localStorage` zu **interagieren.**</span><span class="sxs-lookup"><span data-stu-id="143f4-140">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="143f4-141">Verwenden Sie **das Menü JavaScript-Kontexte,** um den JavaScript-Kontext der **Konsole** zu ändern, wenn Sie auf die Schlüssel-Wert-Paare einer anderen Domäne als der angezeigten Seite `localStorage` zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="143f4-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Ändern des JavaScript-Kontexts der Konsole" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="143f4-143">Ändern des JavaScript-Kontexts der Konsole</span><span class="sxs-lookup"><span data-stu-id="143f4-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="143f4-144">Führen Sie `localStorage` Ihre Ausdrücke in der Konsole aus, genauso wie in Ihrem JavaScript.</span><span class="sxs-lookup"><span data-stu-id="143f4-144">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interagieren mit localStorage über die Konsole" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="143f4-146">Interagieren mit `localStorage` über die **Konsole**</span><span class="sxs-lookup"><span data-stu-id="143f4-146">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="143f4-147">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="143f4-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="143f4-150">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="143f4-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="143f4-151">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="143f4-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="143f4-153">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="143f4-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
