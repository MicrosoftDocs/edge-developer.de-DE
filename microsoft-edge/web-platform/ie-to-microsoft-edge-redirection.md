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
# <a name="moving-users-to-microsoft-edge-from-internet-explorer"></a>Verschieben von Benutzern zu Microsoft Edge aus Internet Explorer  

Viele moderne Websites verfügen über Designs, die mit Internet Explorer \(IE\) nicht kompatibel sind.  Wenn ein IE-Benutzer eine inkompatible öffentliche Website besucht, erhält der Benutzer möglicherweise eine Nachricht.  Die Meldung besagt, dass die Website mit dem Browser nicht kompatibel ist.  Nachdem die Meldung angezeigt wurde, wird erwartet, dass der Benutzer manuell zu einem modernen Browser wechselt.  Um Unterbrechungen zu minimieren, unterstützt Microsoft Edge ab Version 84 eine neue Funktion, die Benutzer automatisch umleitet.  Wenn ein IE-Benutzer zu einer Website navigiert, die mit IE nicht kompatibel ist, leitet Windows den Benutzer automatisch zu Microsoft Edge um.  Um die Websites in der Liste zu überprüfen, navigieren Sie zu ["Need Microsoft Edge list".][MicrosoftEdgeNeededgeV1]

In diesem Artikel werden die folgenden Konzepte beschrieben.  

*   Warum eine Website zur Liste hinzugefügt wird  
*   Die Benutzeroberfläche für die Umleitung  
*   Anfordern einer Aktualisierung der Liste  
    
## <a name="why-is-a-website-added-to-the-ie-compatibility-list"></a>Warum wird der IE-Kompatibilitätsliste eine Website hinzugefügt?  

Die IE-Kompatibilitätsliste fügt nur dann eine Website hinzu, wenn die folgenden Aktionen ausgeführt werden.  

*   Zeigt einem IE-Benutzer eine Meldung an, in der vorgeschlagen wird, dass der Benutzer aus Kompatibilitätsgründen einen anderen Browser verwenden sollte.  
*   Der Besitzer fordert an, die Website der IE-Kompatibilitätsliste hinzuzufügen.  

## <a name="redirection-experience"></a>Umleitungserfahrung

Bei der Umleitung zu Microsoft Edge wird dem Benutzer im nächsten Screenshot das einmalige Dialogfeld angezeigt.  Das Dialogfeld stellt dem Benutzer die folgenden Informationen bereit.  

*   Es wird erläutert, warum die Website umgeleitet wird.  
*   Der Benutzer wird aufgefordert, zuzustimmen, Browserdaten und -einstellungen von IE in Microsoft Edge zu kopieren.  

:::row:::
   :::column span="":::
      Die folgenden Browserdaten werden importiert.  
      
      *   Favoriten  
      *   Kennwörter  
      *   Suchmaschinen  
      *   Offene Registerkarten  
      *   Verlauf  
      *   Einstellungen  
      *   Cookies  
      *   Die Startseite  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Browserbenachrichtigung und Eingabeaufforderung zum Importieren von Daten und Einstellungen" lightbox="../media/neededge-dialog1.msft.png":::
         Browserbenachrichtigung und Eingabeaufforderung zum Importieren von Daten und Einstellungen  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Wenn der Benutzer nicht zustimmt, indem er das Kontrollkästchen **"Meine Browserdaten und -einstellungen immer** über Internet Explorer übertragen" auswählt, kann der Benutzer **"Browsen fortsetzen"**   auswählen, um die Browsersitzung fortzusetzen.  

Schließlich wird unter der Adressleiste für jede Umleitung ein Banner zur Inkompatibilität der Website angezeigt.  Ein Beispiel für ein Banner zur Inkompatibilität einer Website wird in der folgenden Abbildung angezeigt.

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Benachrichtigung über moderne Websites und Aufforderung, Microsoft Edge als Standardbrowser festzulegen oder Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   Benachrichtigung über moderne Websites und Aufforderung, Microsoft Edge als Standardbrowser festzulegen oder Microsoft Edge  
:::image-end:::

Das Banner zur Inkompatibilität der Website stellt dem Benutzer die folgenden Details bereit.  

*   Es wird empfohlen, dass der Benutzer zu Microsoft Edge wechselt.  
*   Bietet an, Microsoft Edge als Standardbrowser festzulegen.  
*   Gibt dem Benutzer die Möglichkeit, Microsoft Edge zu erkunden.    
    
Wenn eine Website von Internet Explorer zu Microsoft Edge umgeleitet wird, wird eine der folgenden Aktionen ausgeführt.

*   Wenn die aktive IE-Registerkarte keine vorherigen Inhalte hatte, wird sie geschlossen.  
*   Wenn die aktive IE-Registerkarte vorherige Inhalte hatte, wird zur [Microsoft-Supportseite navigiert, auf der erläutert wird, warum die Website zu Microsoft Edge umgeleitet wurde.][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]  

> [!NOTE]
> Nach einer Umleitung können Benutzer IE weiterhin für Websites verwenden, die nicht in der IE-Kompatibilitätsliste enthalten sind.  

## <a name="request-an-update-to-the-ie-compatibility-list"></a>Anfordern eines Updates für die IE-Kompatibilitätsliste  

Die IE-Kompatibilitätsliste ist eine XML-Datei [auf microsoft.com.][MicrosoftOfficialHome]  Die Liste wird regelmäßig als Reaktion auf Benutzer- und Websiteentwickleranforderungen aktualisiert, um Websites hinzuzufügen oder zu entfernen.  Updates für die Liste werden automatisch auf Benutzercomputer heruntergeladen.  

Senden Sie die folgenden Informationen per E-Mail an [ietoedge@microsoft.com,][MailtoMicrosoftIetoedge] damit Ihre Website der IE-Kompatibilitätsliste hinzugefügt oder daraus entfernt werden kann.    

*   Besitzername  
*   Unternehmenstitel  
*   E-Mail-Adresse  
*   Name des Unternehmens  
*   Straße  
*   Websiteadresse  
    
Die IE-Kompatibilitätsliste wird innerhalb einer Woche aktualisiert.

> [!NOTE]
> Die IE-Kompatibilitätsliste ist nur für die Verwendung mit öffentlichen Websites konzipiert.  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Senden einer E-Mail an ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Offizielle Startseite von Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Xml-| für Microsoft Edge Liste v1 erforderlich Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "Die Website, die Sie erreichen wollten, funktioniert nicht mit Internet Explorer | Microsoft Office Unterstützung"  
