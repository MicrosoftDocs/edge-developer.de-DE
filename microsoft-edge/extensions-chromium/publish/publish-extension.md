---
description: Veröffentlichen Microsoft Edge (Chromium)-Erweiterungen im Microsoft Edge Add-Ons-Speicher
title: Veröffentlichen Sie die Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungsentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: aadb3470eb295934cde4ad26b089ac0c83898e5c
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643242"
---
# <a name="publish-your-extension"></a>Veröffentlichen Sie die Erweiterung  

Nachdem Sie Ihre Erweiterung entwickelt und getestet haben, können Sie ihre Erweiterung verteilen. Verwenden Sie den Microsoft Edge-Add-Ons-Speicher, um Ihre Erweiterung zu verteilen.  Um Ihre vorhandene Chromium Erweiterung für Microsoft Edge Benutzer freizugeben, navigieren Sie zum [Portieren Ihrer vorhandenen Chromium-Erweiterung.][PortChromiumExtension]  

Veröffentlichen Sie Ihre Erweiterung im Microsoft Edge Add-Ons-Speicher, um die Reichweite zu erhöhen und sie anderen Microsoft Edge Benutzern zur Verfügung zu stellen.  Dieser Artikel enthält den Prozess zum Übermitteln Ihrer Erweiterung an den Microsoft Edge-Add-Ons-Speicher.  

## <a name="before-you-begin"></a>Bevor Sie beginnen  

Sie sollten einen funktionsfähigen Prototyp Ihrer Erweiterung bereit haben.  Informationen zum Erstellen einer Erweiterung finden Sie im [Lernprogramm "Erste Schritte".][ExtensionsGettingStarted]  

Verwenden Sie Ihr aktives Entwicklerkonto im [Partner Center,][MicrosoftPartnerCenter]um Ihre Erweiterung im Microsoft Edge Store für Add-Ons zu veröffentlichen.  Wenn Sie kein Entwicklerkonto haben, erstellen Sie ein neues Entwicklerkonto.  Navigieren Sie zur [Entwicklerregistrierung,][DeveloperRegistration]um ein neues Entwicklerkonto zu öffnen und sich beim Microsoft Edge-Add-Ons-Programm zu registrieren.  

Erstellen Sie eine ZIP-Datei, die Ihr Erweiterungspaket darstellt.  Das Erweiterungspaket muss die folgenden Dateien enthalten.  

*   Das Erweiterungsmanifest, das Details wie den Namen der Erweiterung, eine kurze Beschreibung, Berechtigungen und die Standardsprache angibt.  
*   Bilder und andere Dateien, die für Ihre Erweiterung erforderlich sind.  
    
Die folgenden Felder im Manifest werden automatisch in die Details ihres Store-Eintrags aufgenommen.  Die Felder sind auf der **Webseite für Store Einträge schreibgeschützt.**  Die Webseite für den Store-Eintrag wird weiter unten in diesem Artikel beschrieben.  Stellen Sie sicher, dass die Feldwerte ihrer bevorzugten Anzeige auf der Store-Detailwebseite entsprechen, bevor Sie Ihr Paket in Partner Center hochladen.  Ein Beispiel für den code erforderlich für die Manifestdatei, überprüfen Sie die Grundlagen der Manifestdatei.  

*   `Name` in der Manifestdatei, d. h. dem **Anzeigenamen** auf der Store-Detailwebseite.  
*   `Description` in der Manifestdatei, die die **Kurzbeschreibung** auf der Store-Detailwebseite darstellt.  Geben Sie eine kurze, eingängige Beschreibung an, die am Anfang des Eintrags für Ihre Erweiterung angezeigt werden soll.  Wenn Sie die kurze Beschreibung in die Erweiterungsmanifestdatei einschließen, wird sie in Ihrem Store-Eintrag angezeigt.  Wenn Sie keine kurze Beschreibung in die Manifestdatei einfügen, werden die ersten Zeilen `Description` in Ihrem Store-Eintrag angezeigt.  Geben Sie eine kurze Beschreibung an, um Wiederholungen von Inhalten auf Ihrer Webseite für den Store-Eintrag zu vermeiden.  
    
## <a name="submit-your-extension-to-microsoft-edge-add-ons-store"></a>Übermitteln Ihrer Erweiterung an Microsoft Edge Add-Ons Store  

Führen Sie die folgenden Schritte aus, um Ihre Erweiterung an [Partner Center][MicrosoftPartnerCenter]zu übermitteln.  

## <a name="step-1--start-a-new-submission"></a>Schritt 1: Starten einer neuen Übermittlung  

Navigieren Sie zum [Entwicklerdashboard,][MicrosoftPartnerCenter] und wählen Sie auf der Webseite **"Übersicht"** die Option **"Neue Erweiterung** erstellen" aus.  

## <a name="step-2--upload-the-extension-package"></a>Schritt 2: Hochladen des Erweiterungspakets  

Verwenden Sie die **Webseite "Pakete",** um die ZIP-Datei Ihres Erweiterungspakets hochzuladen.  Sie dürfen jeweils nur ein Paket hochladen.  Ihre Übermittlung wird blockiert, wenn der Paketupload auf der **Paketwebseite** nicht erfolgreich war.  

Um das Paket hochzuladen, wählen Sie das Paket aus, und ziehen Sie es in das Uploadfeld.  Sie können auch **"Dateien durchsuchen"** auswählen.  Nachdem das Paket hochgeladen wurde, wird das Paket überprüft.  Nachdem die Überprüfung erfolgreich war, überprüfen Sie die Erweiterungsdetails, und wählen Sie dann **"Weiter"** aus, um fortzufahren.  Wenn Validierungsfehler auftreten, beheben Sie die Probleme, und versuchen Sie erneut, sie hochzuladen.  

## <a name="step-3--provide-availability-details"></a>Schritt 3: Bereitstellen von Verfügbarkeitsdetails  

Geben Sie auf der **Webseite "Verfügbarkeit"** die folgenden Informationen zur Verfügbarkeit Ihrer Erweiterung ein.  

### <a name="visibility"></a>Sichtbarkeit  

Wählen Sie eine der folgenden Sichtbarkeitsoptionen aus, um zu definieren, ob Ihre Erweiterung im Microsoft Edge Add-Ons Store auffindbar ist.  

*   `Public` \(Standard\)  
    Öffentlich ermöglicht es jedem, Ihre Erweiterung über die Suche zu entdecken, im Microsoft Edge Add-Ons-Speicher zu browsen oder die Eintrags-URL zu Ihrer Erweiterung im Microsoft Edge Add-Ons Store zu verwenden.  Die Eintrags-URL ist auf Ihrem Partner Center-Dashboard auf der Webseite **"Erweiterungsübersicht"** verfügbar.  
*   `Hidden`  
    Ausgeblendet werden Erweiterungen aus Suchergebnissen entfernt oder im Microsoft Edge Add-Ons-Speicher browsen.  Um ausgeblendete Erweiterungen im Microsoft Edge Store für Add-Ons zu verteilen, müssen Sie die Eintrags-URL für die Erweiterung für Ihre Kunden freigeben.  
    
> [!NOTE]
> Sie können die Sichtbarkeit Ihrer Erweiterung von **"Öffentlich"** in **"Ausgeblendet"** ändern.  Benutzer, die Ihre Erweiterung installiert haben, während die Sichtbarkeit auf öffentlich festgelegt wurde, behalten den Zugriff auf Ihre Erweiterung bei und erhalten alle Updates, die Sie über die Microsoft Edge-Add-Ons Website zur Verfügung stellen.  

### <a name="markets"></a>Märkte  

Definieren Sie die spezifischen Märkte, in denen Sie Ihre Erweiterung anbieten möchten.  Die Standardeinstellung für Märkte ist alle Märkte und umfasst alle zukünftigen Märkte, die später hinzugefügt werden.  Um bestimmte Märkte auszuwählen, wählen Sie **"Märkte ändern" aus.**  Schalten Sie die einzelnen Märkte um, um die einzelnen Märkte auszuschließen, oder wählen Sie **"Auswahl aufheben"** aus, und fügen Sie dann einzelne Märkte Ihrer Wahl hinzu.  

> [!NOTE]
> Sie können die Märkte ändern, in denen Ihre Erweiterung angeboten wird.  Ein Benutzer, der Ihre Erweiterung installiert, während sie auf dem Markt des Benutzers verfügbar ist, behält den Zugriff auf Ihre Erweiterung.  Der Benutzer hat jedoch keinen Zugriff auf zukünftige Updates, die an den Microsoft Edge-Add-Ons-Speicher übermittelt werden.  

Wählen Sie **"Speichern"** aus, um mit dem Abschnitt **"Eigenschaften"** fortzufahren.  

## <a name="step-4-select-properties-for-your-extension"></a>Schritt 4: Auswählen von Eigenschaften für Ihre Erweiterung  

Geben **** Sie auf der Webseite Eigenschaften die folgenden Informationen ein, um die Eigenschaften Ihrer Erweiterung anzugeben.  Die Eigenschaften werden Benutzern im Microsoft Edge Add-Ons-Speicher angezeigt.  

| Name der Erweiterungseigenschaft | Beschreibung |  
|:--- |:--- |  
| Kategorie \(erforderlich\) | Die Kategorie, die Ihre Erweiterung am besten beschreibt.  Wenn Sie Ihre Erweiterung in der richtigen Kategorie auflisten, können Benutzer Ihre Erweiterung leicht finden und mehr darüber erfahren.  |  
| Datenschutzrichtlinienanforderungen \(erforderlich\) | Geben Sie an, ob Ihre Erweiterung auf persönliche Informationen zugreift, diese sammelt oder überträgt.  Ihre Erweiterung schlägt möglicherweise beim Zertifizierungsschritt fehl, wenn Sie **"Ja"** auswählen und keine . `Privacy policy URL`  |  
| URL zu den Datenschutzrichtlinien | Eine gültige Datenschutzrichtlinien-URL, um zu kommunizieren, wie Ihre Erweiterung den Datenschutzgesetzen und -bestimmungen folgt.  Sie sind dafür verantwortlich, sicherzustellen, dass Ihre Erweiterung den Datenschutzgesetzen und -bestimmungen entspricht.  Sie sind auch für die Angabe einer Datenschutzrichtlinien-URL verantwortlich, wenn von Ihrer Erweiterung auf personenbezogene Informationen zugegriffen, übertragen oder gesammelt wird.  Um festzustellen, ob Ihre Erweiterung eine Datenschutzrichtlinie erfordert, navigieren Sie zu [Microsoft Edge Entwicklervereinbarung][MicrosoftAppDeveloperAgreement] und [Microsoft Edge Add-Ons Store-Entwicklerrichtlinien.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  |  
| Website-URL | Eine Webseite, die zusätzliche Informationen zu Ihrer Erweiterung bereitstellt.  Der `Website URL` muss auf eine Webseite auf Ihrer eigenen Website verweisen, nicht auf den Webeintrag für Ihre Erweiterung im Microsoft Edge Add-Ons-Speicher.  Dies `Website URL` hilft Benutzern, mehr über Ihre Erweiterung, ihre Features und alle anderen relevanten Informationen zu erfahren.  |  
| Supportkontaktdetails | Die URL zu Ihrer Supportwebseite oder die E-Mail-Adresse, über die Sie sich an Ihr Supportteam wenden können.  |  
| Ausgereifter Inhalt | Kontrollkästchen, um anzugeben, ob Ihre Erweiterung ausgereifte Inhalte enthält.  Die Erweiterungsbewertung hilft bei der Ermittlung der geeigneten Altersgruppe der Zielgruppe Ihrer Erweiterung.  Um festzustellen, ob Ihre Erweiterung ausgereifte Inhalte enthält, navigieren Sie zu [Microsoft Edge Add-Ons Store-Entwicklerrichtlinien.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  |  

Wählen Sie **"Speichern"** aus, um mit dem **Abschnitt Store Einträgen** fortzufahren.  

> [!Important]
> Der Name Ihres Entwicklers/Ihrer Organisation, die Website-URL und die Supportkontaktdetails, die Sie während der Registrierung übermittelt haben, werden Benutzern im Microsoft Edge Add-Ons Store angezeigt.  

## <a name="step-5-add-store-listing-details-for-your-extension"></a>Schritt 5: Hinzufügen Store Eintragsdetails für Ihre Erweiterung  

Die im folgenden Abschnitt bereitgestellten Informationen werden Benutzern angezeigt, die Ihren Eintrag im store für Microsoft Edge-Add-Ons überprüfen.  Obwohl einige Felder optional sind, sollten Sie so viele Informationen wie möglich bereitstellen.  Zum Auflisten der Erweiterung im Store sind die folgenden Details erforderlich.  

*   **Beschreibung** für jede Sprache in Ihrem Erweiterungspaket. Um mehrere Sprachen zu unterstützen, können Sie die Internationalisierungs-API ([chrome.i18n](https://go.microsoft.com/fwlink/?linkid=2167478)) verwenden.  
*   **Erweiterung Store Logo** für jede Sprache in Ihrem Erweiterungspaket.  
    
> [!NOTE]
> Die mindestens erforderlichen Details zum Store-Eintrag müssen für mindestens eine der sprachen ausgefüllt werden, die in Ihrem Erweiterungs-ZIP-Paket erwähnt werden.  Verwenden Sie zum Hinzufügen oder Entfernen von Sprachen in Ihrem Store-Eintrag im Microsoft Edge-Add-Ons-Speicher die Dropdownliste **"Sprache hinzufügen"** auf der Webseite **Store Einträge.**  Darüber hinaus können Sie Ihre Ressourcen mithilfe der Schaltfläche für doppelte Funktionen auf der Webseite für Sprachdetails aus einer Sprache duplizieren.  

| Name der Eigenschaft "Language Details" | Beschreibung |  
|:--- |:--- |  
| Anzeigename \(erforderlich\) | Die `name` in der Manifestdatei der Erweiterung angegebene Erweiterung.  Um den Anzeigenamen des Speichers nach der Übermittlung zu ändern, können Sie den Namen in der Manifestdatei aktualisieren, ein neues Erweiterungspaket erstellen und es dann erneut laden.  |  
| Beschreibung \(erforderlich\) | Das `description` Feld konzentriert sich auf die Erläuterung, was Ihre Erweiterung bewirkt, warum Benutzer sie installieren sollten oder andere relevante Informationen, die Benutzer wissen müssen.  Sie sollte kleiner als 10.000 Zeichen sein.  |  
| Erweiterung Store Logo \(erforderlich\) | Ein Bild, das Ihr Unternehmen oder `extension logo` ein Seitenverhältnis von 1 und einer empfohlenen Größe von 300 x 300 Pixeln darstellt.  Darüber hinaus können Sie die Ressource mithilfe der Schaltfläche "Duplizieren" aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche wird nach dem Hochladen ihres Logos für die Sprache nach dem Feld gefunden.  |  
| Kleine Werbekachel \(optional\) | Das `Small promotional tile` Bild wird verwendet, um Ihre Erweiterung zusammen mit anderen Erweiterungen im Store anzuzeigen.  Die Größe des Bilds sollte 440 x 280 Pixel betragen.  Darüber hinaus können Sie die Ressource mithilfe der Schaltfläche "Duplizieren" aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche wird nach dem Hochladen einer Werbekachel für die Sprache nach dem Feld gefunden.  |  
| Screenshots \(optional\) | Sie können maximal 10 Übermitteln, `screenshots` um die Funktionalität Ihrer Erweiterung im Detail zu beschreiben.  Die Größe der Screenshots muss entweder 640 x 480 Pixel oder 1280 x 800 Pixel betragen.  Darüber hinaus können Sie die Ressource mithilfe der Schaltfläche "Duplizieren" aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche wird nach dem Hochladen mindestens eines für die Sprache nach dem Feld gefunden.|  
| Große Werbekachel \(optional\) | `Large promotion tiles` werden im Store verwendet, um Erweiterungen auf der Microsoft Edge-Add-Ons Website bekannter zu machen.  Wenn die Bilder übermittelt werden, sind sie für die Benutzer sichtbar.  Die Größe der PNG-Dateien muss 1400 x 560 Pixel betragen.  Darüber hinaus können Sie die Ressource mithilfe der Schaltfläche "Duplizieren" aus einer Sprache in alle anderen Sprachen kopieren.  Die Schaltfläche wird nach dem Hochladen einer Werbekachel für die Sprache nach dem Feld gefunden.  |  
| YouTube-Video-URL \(optional\) | Sie können ein YouTube-Werbevideo Ihrer Erweiterung hinzufügen.  Das `YouTube video URL` Video wird auf der Store-Eintragswebseite Ihrer Erweiterung angezeigt.  |  
| Kurzbeschreibung \(erforderlich\) | Um die `short description` zu bearbeiten, müssen Sie das Beschreibungsfeld in der Manifestdatei des Erweiterungspakets aktualisieren und erneut laden.  |  
| Suchbegriffe \(optional\) | `Search terms` sind einzelne Wörter oder Ausdrücke, mit denen Sie Ihre Erweiterung ermitteln können, wenn ein Benutzer im Microsoft Edge Add-Ons-Speicher sucht.  Die Suchbegriffe werden Benutzern nicht angezeigt.  |  

### <a name="youtube-video-url-requirements"></a>Anforderungen an die YouTube-Video-URL  

Stellen Sie sicher, dass Ihr Video die folgenden Anforderungen erfüllt.  

*   Stellen Sie sicher, dass der Inhalt des YouTube-Videos den [Entwicklerrichtlinien Microsoft Edge Add-Ons Store][MicrosoftEdgeAddonsCatalogDeveloperPolicies]folgt.  
*   Deaktivieren Sie Werbung in Ihrem Video.  Navigieren Sie für weitere Informationen zu ["Standardanzeigenformate][GoogleYoutubeAnswer2531367Topic7072227] und [Anzeigen für eingebettete Videos][GoogleYoutubeAnswer132596]festlegen".  
*   Aktivieren Sie die Einbettung für Ihre Videos.  Navigieren Sie für weitere Informationen zu [Einbetten von Videos & Wiedergabelisten.][GoogleYoutubeAnswer171780]  
    
Führen Sie die folgenden Schritte aus, um die YouTube-Video-URL Ihres Videos zu übermitteln.  

1.  Suchen Sie auf YouTube das Video, das Sie ihrer Webseite für den Store-Eintrag hinzufügen möchten.  
1.  Wählen Sie unter dem Video **"Einbetten freigeben"**  >  **aus.**  
1.  Kopieren Sie den angezeigten HTML-Code.  
1.  Fügen Sie den HTML-Code in das Feld ein, um die Detailwebseite des Store-Eintrags `YouTube video URL` anzuzeigen.  
    
### <a name="search-terms-requirements"></a>Anforderungen an Suchbegriffe  

Suchbegriffe müssen die folgenden Anforderungen erfüllen.  

*   Sie können Suchbegriffe eingeben, um maximal 21 Wörter zu verwenden.  Unabhängig davon, ob sie als einzelne Wörter, Ausdrücke oder eine Kombination aus beiden verwendet werden, sind nur maximal 21 Wörter zulässig.  
*   Maximal sieben Suchbegriffe: einzelne Wörter oder Ausdrücke.  Jeder Suchbegriff hat eine Zeichenbegrenzung von 30 Zeichen.  
    
## <a name="step-6-complete-your-submission"></a>Schritt 6: Abschließen der Übermittlung  

Fügen **Sie** auf der Webseite zum Übermitteln Ihrer Erweiterung Hinweise zur Zertifizierung hinzu, um Ihre Erweiterung zu testen.  

### <a name="notes-for-certification-optional"></a>Hinweise zur Zertifizierung (optional)  

Wenn Sie Ihre Erweiterung übermitteln, verwenden Sie die Webseite **"Hinweise zur Zertifizierung",** um den Zertifizierungstestern zusätzliche Informationen bereitzustellen.  Die zusätzlichen Informationen tragen dazu bei, dass Ihre Erweiterung ordnungsgemäß getestet wird.  Wenn Ihre Erweiterung nicht vollständig getestet wurde, schlägt die Zertifizierung möglicherweise fehl.  

Stellen Sie sicher, dass Sie bei Bedarf die folgenden Informationen einschließen.  

*   Benutzernamen und Kennwörter für Testkonten.  
*   Schritte für den Zugriff auf ausgeblendete oder gesperrte Features.  
*   Es wurden Unterschiede bei der Funktionalität basierend auf der Region oder anderen Benutzereinstellungen erwartet.  
*   Wenn Es sich bei Ihrer Übermittlung um ein Update für eine vorhandene Erweiterung handelt, fügen Sie Informationen zu den An der Erweiterung vorgenommenen Änderungen ein.  
*   Alle zusätzlichen Informationen, die Tester über Ihre Übermittlung verstehen müssen.  
    
Nachdem Sie die Informationen bereitgestellt haben, wählen Sie **"Veröffentlichen"** aus, um Ihre Erweiterung an den Microsoft Edge-Add-Ons-Speicher zu übermitteln.  Ihre Übermittlung fährt mit dem Zertifizierungsschritt fort.  Der Zertifizierungsprozess kann bis zu sieben Werktage nach der Übermittlung dauern.  

Nachdem Ihre Übermittlung die Zertifizierung bestanden hat, wird Ihre Erweiterung im Microsoft Edge Add-Ons Store veröffentlicht.  Der Status Ihrer Erweiterung im Partner Center-Dashboard ändert sich in `In the Store` .  

> [!NOTE]
> Wenn beim Übermittlungs- oder Registrierungsvorgang Probleme auftreten, melden Sie ein Supportticket auf [erweiterungsneuer Supportanfrage][ExtensionsSupportForm] an, oder senden Sie eine E-Mail an [ext_dev_support@microsoft.com.][MailtoExtDevSupportMicrosoftCom]  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Erste Schritte mit Microsoft Edge-Erweiterungen (Chromium) | Microsoft Docs"  
[DeveloperRegistration]: ./create-dev-account.md "Registrieren als Microsoft Edge-Erweiterungsentwickler | Microsoft-Dokumente"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Portieren Ihrer Chromium-Erweiterung zu Microsoft Edge | Microsoft-Dokumente"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Microsoft Edge Add-Ons store Developer Policies | Microsoft-Dokumente"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Vereinbarung für App-Entwickler | Microsoft-Dokumente"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Erweiterungen – Neue Supportanfrage | Microsoft-Support"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Festlegen der standardmäßigen Anzeigenformate | YouTube-Hilfe"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anzeigen für eingebettete Videos | YouTube-Hilfe"  
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Einbetten von Videos & Wiedergabelisten | YouTube-Hilfe"  

[MailtoExtDevSupportMicrosoftCom]: mailto:ext_dev_support@microsoft.com "Senden von E-Mails an ext_dev_support@microsoft.com" 

