---
description: Verschieben von Benutzern zu Microsoft Edge aus Internet Explorer
title: Verschieben von Benutzern zu Microsoft Edge aus Internet Explorer
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Microsoft Edge, Kompatibilität, Webplattform, Internet Explorer
ms.openlocfilehash: dd8db64311b60ff0c740776de94def88f22c2e96
ms.sourcegitcommit: 0e67a56b9dc1f7a86924d142db0efd36fd99d38b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "11608667"
---
# <a name="moving-users-to-microsoft-edge-from-internet-explorer"></a><span data-ttu-id="70d4c-104">Verschieben von Benutzern zu Microsoft Edge aus Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="70d4c-104">Moving users to Microsoft Edge from Internet Explorer</span></span>  

<span data-ttu-id="70d4c-105">Viele moderne Websites verfügen über Designs, die mit Internet Explorer \(IE\) nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="70d4c-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="70d4c-106">Wenn ein IE-Benutzer eine inkompatible öffentliche Website besucht, erhält der Benutzer möglicherweise eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="70d4c-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="70d4c-107">Die Meldung besagt, dass die Website mit dem Browser nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="70d4c-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="70d4c-108">Nachdem die Meldung angezeigt wurde, wird erwartet, dass der Benutzer manuell zu einem modernen Browser wechselt.</span><span class="sxs-lookup"><span data-stu-id="70d4c-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="70d4c-109">Um Unterbrechungen zu minimieren, unterstützt Microsoft Edge ab Version 84 eine neue Funktion, die Benutzer automatisch umleitet.</span><span class="sxs-lookup"><span data-stu-id="70d4c-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="70d4c-110">Wenn ein IE-Benutzer zu einer Website navigiert, die mit IE nicht kompatibel ist, leitet Windows den Benutzer automatisch zu Microsoft Edge um.</span><span class="sxs-lookup"><span data-stu-id="70d4c-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="70d4c-111">Um die Websites in der Liste zu überprüfen, navigieren Sie zu ["Need Microsoft Edge list".][MicrosoftEdgeNeededgeV1]</span><span class="sxs-lookup"><span data-stu-id="70d4c-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="70d4c-112">In diesem Artikel werden die folgenden Konzepte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="70d4c-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="70d4c-113">Warum eine Website zur Liste hinzugefügt wird</span><span class="sxs-lookup"><span data-stu-id="70d4c-113">Why a website is added to the list</span></span>  
*   <span data-ttu-id="70d4c-114">Die Benutzeroberfläche für die Umleitung</span><span class="sxs-lookup"><span data-stu-id="70d4c-114">The user experience for redirection</span></span>  
*   <span data-ttu-id="70d4c-115">Anfordern einer Aktualisierung der Liste</span><span class="sxs-lookup"><span data-stu-id="70d4c-115">Request an update to the list</span></span>  
    
## <a name="why-is-a-website-added-to-the-ie-compatibility-list"></a><span data-ttu-id="70d4c-116">Warum wird der IE-Kompatibilitätsliste eine Website hinzugefügt?</span><span class="sxs-lookup"><span data-stu-id="70d4c-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="70d4c-117">Die IE-Kompatibilitätsliste fügt nur dann eine Website hinzu, wenn die folgenden Aktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="70d4c-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="70d4c-118">Zeigt einem IE-Benutzer eine Meldung an, in der vorgeschlagen wird, dass der Benutzer aus Kompatibilitätsgründen einen anderen Browser verwenden sollte.</span><span class="sxs-lookup"><span data-stu-id="70d4c-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="70d4c-119">Der Besitzer fordert an, die Website der IE-Kompatibilitätsliste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="70d4c-119">Owner requests to add the website to the IE compatibility list.</span></span>  

## <a name="redirection-experience"></a><span data-ttu-id="70d4c-120">Umleitungserfahrung</span><span class="sxs-lookup"><span data-stu-id="70d4c-120">Redirection experience</span></span>

<span data-ttu-id="70d4c-121">Bei der Umleitung zu Microsoft Edge wird dem Benutzer im nächsten Screenshot das einmalige Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70d4c-121">On redirection to Microsoft Edge, the user is shown the one-time dialog in the next screenshot.</span></span>  <span data-ttu-id="70d4c-122">Das Dialogfeld stellt dem Benutzer die folgenden Informationen bereit.</span><span class="sxs-lookup"><span data-stu-id="70d4c-122">The dialog provides the user with the following information.</span></span>  

*   <span data-ttu-id="70d4c-123">Es wird erläutert, warum die Website umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="70d4c-123">It explains why the website is being redirected.</span></span>  
*   <span data-ttu-id="70d4c-124">Der Benutzer wird aufgefordert, zuzustimmen, Browserdaten und -einstellungen von IE in Microsoft Edge zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="70d4c-124">It prompts the user for consent to copy browsing data and preferences from IE to Microsoft Edge.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="70d4c-125">Die folgenden Browserdaten werden importiert.</span><span class="sxs-lookup"><span data-stu-id="70d4c-125">The following browsing data is imported.</span></span>  
      
      *   <span data-ttu-id="70d4c-126">Favoriten</span><span class="sxs-lookup"><span data-stu-id="70d4c-126">Favorites</span></span>  
      *   <span data-ttu-id="70d4c-127">Kennwörter</span><span class="sxs-lookup"><span data-stu-id="70d4c-127">Passwords</span></span>  
      *   <span data-ttu-id="70d4c-128">Suchmaschinen</span><span class="sxs-lookup"><span data-stu-id="70d4c-128">Search engines</span></span>  
      *   <span data-ttu-id="70d4c-129">Offene Registerkarten</span><span class="sxs-lookup"><span data-stu-id="70d4c-129">Open tabs</span></span>  
      *   <span data-ttu-id="70d4c-130">Verlauf</span><span class="sxs-lookup"><span data-stu-id="70d4c-130">History</span></span>  
      *   <span data-ttu-id="70d4c-131">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="70d4c-131">Settings</span></span>  
      *   <span data-ttu-id="70d4c-132">Cookies</span><span class="sxs-lookup"><span data-stu-id="70d4c-132">Cookies</span></span>  
      *   <span data-ttu-id="70d4c-133">Die Startseite</span><span class="sxs-lookup"><span data-stu-id="70d4c-133">The Home Page</span></span>  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Browserbenachrichtigung und Eingabeaufforderung zum Importieren von Daten und Einstellungen" lightbox="../media/neededge-dialog1.msft.png":::
         <span data-ttu-id="70d4c-135">Browserbenachrichtigung und Eingabeaufforderung zum Importieren von Daten und Einstellungen</span><span class="sxs-lookup"><span data-stu-id="70d4c-135">Browsing notification and prompt to import data and preferences</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="70d4c-136">Wenn der Benutzer nicht zustimmt, indem er das Kontrollkästchen **"Meine Browserdaten und -einstellungen immer** über Internet Explorer übertragen" auswählt, kann der Benutzer **"Browsen fortsetzen"**   auswählen, um die Browsersitzung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="70d4c-136">If the user does not consent by choosing the **Always bring over my browsing data and preferences from Internet Explorer** checkbox, the user may choose **Continue browsing** to continue the browsing session.</span></span>  

<span data-ttu-id="70d4c-137">Schließlich wird unter der Adressleiste für jede Umleitung ein Banner zur Inkompatibilität der Website angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70d4c-137">Finally, a website incompatibility banner is displayed under the address bar for each redirection.</span></span>  <span data-ttu-id="70d4c-138">Ein Beispiel für ein Banner zur Inkompatibilität einer Website wird in der folgenden Abbildung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70d4c-138">An example of a website incompatibility banner is displayed in following figure.</span></span>

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Benachrichtigung über moderne Websites und Aufforderung, Microsoft Edge als Standardbrowser festzulegen oder Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   <span data-ttu-id="70d4c-140">Benachrichtigung über moderne Websites und Aufforderung, Microsoft Edge als Standardbrowser festzulegen oder Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="70d4c-140">Notification about modern sites and prompt to set Microsoft Edge as default browser or explore Microsoft Edge</span></span>  
:::image-end:::

<span data-ttu-id="70d4c-141">Das Banner zur Inkompatibilität der Website stellt dem Benutzer die folgenden Details bereit.</span><span class="sxs-lookup"><span data-stu-id="70d4c-141">The website incompatibility banner provides the following details to the user.</span></span>  

*   <span data-ttu-id="70d4c-142">Es wird empfohlen, dass der Benutzer zu Microsoft Edge wechselt.</span><span class="sxs-lookup"><span data-stu-id="70d4c-142">Recommends that the user to switch to Microsoft Edge.</span></span>  
*   <span data-ttu-id="70d4c-143">Bietet an, Microsoft Edge als Standardbrowser festzulegen.</span><span class="sxs-lookup"><span data-stu-id="70d4c-143">Offers to set Microsoft Edge as the default browser.</span></span>  
*   <span data-ttu-id="70d4c-144">Gibt dem Benutzer die Möglichkeit, Microsoft Edge zu erkunden.</span><span class="sxs-lookup"><span data-stu-id="70d4c-144">Gives the user the option to explore Microsoft Edge.</span></span>    
    
<span data-ttu-id="70d4c-145">Wenn eine Website von Internet Explorer zu Microsoft Edge umgeleitet wird, wird eine der folgenden Aktionen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70d4c-145">When a website is redirected from Internet Explorer to Microsoft Edge, one of the following actions occurs.</span></span>

*   <span data-ttu-id="70d4c-146">Wenn die aktive IE-Registerkarte keine vorherigen Inhalte hatte, wird sie geschlossen.</span><span class="sxs-lookup"><span data-stu-id="70d4c-146">If the active IE tab had no prior content, it is closed.</span></span>  
*   <span data-ttu-id="70d4c-147">Wenn die aktive IE-Registerkarte vorherige Inhalte hatte, wird zur [Microsoft-Supportseite navigiert, auf der erläutert wird, warum die Website zu Microsoft Edge umgeleitet wurde.][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]</span><span class="sxs-lookup"><span data-stu-id="70d4c-147">If the active IE tab had prior content, it navigates to the [Microsoft support page that explains why the website was redirected to Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span></span>  

> [!NOTE]
> <span data-ttu-id="70d4c-148">Nach einer Umleitung können Benutzer IE weiterhin für Websites verwenden, die nicht in der IE-Kompatibilitätsliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="70d4c-148">After a redirection, users may continue to use IE for websites that are not on the IE compatibility list.</span></span>  

## <a name="request-an-update-to-the-ie-compatibility-list"></a><span data-ttu-id="70d4c-149">Anfordern eines Updates für die IE-Kompatibilitätsliste</span><span class="sxs-lookup"><span data-stu-id="70d4c-149">Request an update to the IE compatibility list</span></span>  

<span data-ttu-id="70d4c-150">Die IE-Kompatibilitätsliste ist eine XML-Datei [auf microsoft.com.][MicrosoftOfficialHome]</span><span class="sxs-lookup"><span data-stu-id="70d4c-150">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="70d4c-151">Die Liste wird regelmäßig als Reaktion auf Benutzer- und Websiteentwickleranforderungen aktualisiert, um Websites hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="70d4c-151">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="70d4c-152">Updates für die Liste werden automatisch auf Benutzercomputer heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="70d4c-152">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="70d4c-153">Senden Sie die folgenden Informationen per E-Mail an [ietoedge@microsoft.com,][MailtoMicrosoftIetoedge] damit Ihre Website der IE-Kompatibilitätsliste hinzugefügt oder daraus entfernt werden kann.</span><span class="sxs-lookup"><span data-stu-id="70d4c-153">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="70d4c-154">Besitzername</span><span class="sxs-lookup"><span data-stu-id="70d4c-154">Owner name</span></span>  
*   <span data-ttu-id="70d4c-155">Unternehmenstitel</span><span class="sxs-lookup"><span data-stu-id="70d4c-155">Corporate title</span></span>  
*   <span data-ttu-id="70d4c-156">E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="70d4c-156">Email address</span></span>  
*   <span data-ttu-id="70d4c-157">Name des Unternehmens</span><span class="sxs-lookup"><span data-stu-id="70d4c-157">Company name</span></span>  
*   <span data-ttu-id="70d4c-158">Straße</span><span class="sxs-lookup"><span data-stu-id="70d4c-158">Street address</span></span>  
*   <span data-ttu-id="70d4c-159">Websiteadresse</span><span class="sxs-lookup"><span data-stu-id="70d4c-159">Website address</span></span>  
    
<span data-ttu-id="70d4c-160">Die IE-Kompatibilitätsliste wird innerhalb einer Woche aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="70d4c-160">The IE compatibility list is updated within a week.</span></span>

> [!NOTE]
> <span data-ttu-id="70d4c-161">Die IE-Kompatibilitätsliste ist nur für die Verwendung mit öffentlichen Websites konzipiert.</span><span class="sxs-lookup"><span data-stu-id="70d4c-161">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Senden einer E-Mail an ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Offizielle Startseite von Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Xml-| für Microsoft Edge Liste v1 erforderlich Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "Die Website, die Sie erreichen wollten, funktioniert nicht mit Internet Explorer | Microsoft Office Unterstützung"  
