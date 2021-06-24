---
description: Auf dieser Seite finden Sie Dokumentationen zum Feature Microsoft Edge (Chromium) zur Nachverfolgungsverhütung
title: Tracking-Verhinderung in Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Kompatibilität, Webplattform, Tracking-Verhinderung, Tracker, Cookies, Speicher, Anzeigenblockierung, Tracker-Blockierung, Tracking-Schutz
ms.openlocfilehash: 24c410beba34b992cf01b973e79c1247fdc26fee
ms.sourcegitcommit: b5acfd4dd7f57991d659715e4621edd786d44052
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "11614635"
---
# <a name="tracking-prevention-in-microsoft-edge-chromium"></a>Tracking-Verhinderung in Microsoft Edge (Chromium)  

Die Tracking-Verhinderungsfunktion in Microsoft Edge schützt Benutzer vor der Onlineverfolgung, indem die Möglichkeit von Trackern eingeschränkt wird, auf browserbasierten Speicher und das Netzwerk zuzugreifen.  Es wurde entwickelt, um die Microsoft Edge [Datenschutzzusage][MicrosoftEdgeBrowserPrivacyPromise] des Browsers einzuhalten und gleichzeitig sicherzustellen, dass es standardmäßig keine Auswirkungen auf die Websitekompatibilität oder die rentabilität des Webs gibt.  

Microsoft Edge bietet Benutzern derzeit drei Stufen der Nachverfolgungsverhinderung, die durch Navigieren zu ausgewählt `edge://settings/privacy` werden.  

![Drei Einstellungen der Nachverfolgungsverhütung][ImageThreeSettingsTrackingPrevention]  

1.  ** Einfach ** – Das am wenigsten restriktive Maß an Tracking-Verhinderung, das für Benutzer entwickelt wurde, die personalisierte Werbung nutzen und keine Bedenken haben, im Web nachverfolgt zu werden.  Basic schützt Benutzer nur vor bösartigen Trackern wie Fingerabdrücken und Kryptominern.  
1.  **Ausgeglichen (Standard)** – Die Standardstufe der Nachverfolgungsverhütung, die für Benutzer entwickelt wurde, die weniger personalisierte Werbung anzeigen möchten, während das Risiko von Kompatibilitätsproblemen beim Surfen im Web minimiert wird.  Balanced zielt darauf ab, Tracker von Websites zu blockieren, mit denen Benutzer niemals interagieren.  
1.  **Streng** – das restriktivste Maß an Tracking-Verhinderung, das für Benutzer entwickelt wurde, die für die Kompatibilität von Handelswebsites in Ordnung sind, um maximalen Datenschutz zu gewährleisten.  

Die Tracking-Verhinderungsfunktion in Microsoft Edge besteht aus drei Hauptkomponenten, die zusammenarbeiten, um zu bestimmen, ob eine bestimmte Ressource von einer Website als Tracker klassifiziert und blockiert werden soll.  Die Komponenten sind wie folgt:  

1.  **Klassifizierung** – Die Art und Weise, wie Microsoft Edge bestimmt, ob eine URL zu einem Tracker gehört.  
1.  **Erzwingung** – Die Maßnahmen zum Schutz Microsoft Edge Benutzer vor URLs, die als Tracker klassifiziert werden.  
1.  **Gegenmaßnahmen** – Die bereitgestellten Mechanismen, um sicherzustellen, dass benutzerdefinierte Lieblingswebsites weiterhin funktionieren und gleichzeitig einen starken Standardschutz bieten.  

Jede der Komponenten wird auf dieser Seite untersucht und ausführlich erläutert.  

## <a name="classification"></a>Klassifizierung  

Die erste Komponente des Features zur Nachverfolgungsverhütung in Microsoft Edge ist die Klassifizierung.  Um Online-Tracker zu klassifizieren und in Kategorien zu gruppieren, verwendet Microsoft Edge die Open Source [Tracking-Schutzlisten][GitHubDisconnectMeTrackingProtection] ["Disconnect".][|::ref1::|Main]  Die Listen werden über die Komponente "Vertrauensschutzlisten" bereitgestellt, die unter angezeigt werden `edge://components` kann.  Nach dem Herunterladen werden die Listen auf dem Datenträger gespeichert, auf dem Sie sie verwenden können, um zu bestimmen, ob/wie eine bestimmte URL klassifiziert wird.  

Um festzustellen, ob eine URL vom Klassifizierungssystem in Microsoft Edge als Tracker betrachtet wird, wird eine Reihe von Hostnamen überprüft, beginnend mit einer genauen Übereinstimmung, und dann wird nach Teilübereinstimmungen für bis zu vier Bezeichnungen außerhalb der Domäne der obersten Ebene gesucht.  

> **Beispiel**:  
> 
> Url: `https://a.subdomain.of.a.known.tracker.test/some/path`  
> 
> Getestete Hostnamen:  
> 
> *   `a.subdomain.of.a.known.tracker.test`  
> *   `of.a.known.tracker.test`  
> *   `a.known.tracker.test`  
> *   `known.tracker.test`  
> *   `tracker.test`  

Wenn einer dieser Hostnamen mit einem Hostnamen in den [][|::ref2::|Main] [Disconnect-Listen][GitHubDisconnectMeTrackingProtection]übereinstimmt, wird Microsoft Edge mit der Auswertung von Erzwingungsaktionen fortfahren, um zu verhindern, dass Benutzer nachverfolgt werden.  

## <a name="enforcement"></a>Erzwingung  

Um Schutz vor Nachverfolgungsaktionen im Web zu bieten, führt Microsoft Edge zwei Durchsetzungsmaßnahmen gegen klassifizierte Tracker aus:

*   **Einschränken des Speicherzugriffs** – Wenn eine bekannte Trackingressource versucht, auf einen Webspeicher zuzugreifen, in dem sie möglicherweise versucht, Daten über den Benutzer zu speichern, Microsoft Edge diesen Zugriff blockiert.  Dies umfasst die Einschränkung der Möglichkeit für diesen Tracker, Cookies abzurufen oder festzulegen, sowie den Zugriff auf Speicher-APIs wie `IndexedDB` und `localStorage` .  
*   **Laden** von Ressourcen blockieren : Wenn eine bekannte Tracking-Ressource auf einer Website geladen wird, können Microsoft Edge diese Last blockieren, bevor die Anforderung das Netzwerk erreicht, je nach Kompatibilitätsauswirkungen der Last und der von einem Benutzer festgelegten Einstellung für die Tracking-Verhinderung.  Blockierte Ladevorgänge können Nachverfolgungsskripts, Pixel, iframes und mehr umfassen.  Dies verhindert, dass Daten potenziell an die Tracking-Domäne gesendet werden, und kann sogar die Ladezeiten und die Seitenleistung als Nebeneffekt verbessern.  

Ein Benutzer kann das Flyoutsymbol für Seiteninformationen auf der linken Seite der Adressleiste auswählen, um herauszufinden, welche Tracker auf einer bestimmten Seite blockiert wurden: 

![Blockierte Tracker im Seiteninfo-Flyout][ImageBlockedTrackersPageInfoFlyout]  

Wie die Erzwingungen angewendet werden, hängt davon ab, welche Stufe der Nachverfolgungsverhütung vom Benutzer ausgewählt wurde, und welche Gegenmaßnahmen angewendet werden können.  

## <a name="mitigations"></a>Schutzmaßnahmen  

Um sicherzustellen, dass die Webkompatibilität so weit wie möglich erhalten bleibt, verfügt Microsoft Edge über drei Gegenmaßnahmen, um die Durchsetzung in bestimmten Situationen auszugleichen.  Hierbei handelt es sich um die Risikominderung für [Organisationsbeziehungen,](#org-relationship-mitigation)die [Risikominderung von Org Engagement](#org-engagement-mitigation)und die Liste der [CompatExceptions](#the-compatexceptions-list).  

Bevor Sie sich mit den Gegenmaßnahmen befassen, sollten Sie das Konzept einer "Organisation" oder "Organisation" definieren.  [Beim Trennen][|::ref3::|Main] wird auch eine Liste mit dem Namen [entities.js][GitHubDisconnectMeTrackingProtectionEntitiesJson] verwaltet, die Gruppen von URLs definiert, die im Besitz derselben übergeordneten Organisation/desselben Unternehmens sind.  Das Feature zur Nachverfolgungsverhütung in Microsoft Edge verwendet diese Liste sowohl in der [Minderung](#org-relationship-mitigation) der Organisationsbeziehung als auch in der Risikominderung durch [Org Engagement,](#org-engagement-mitigation) um das Auftreten von Kompatibilitätsproblemen zu minimieren, die durch die Nachverfolgungsverhütung verursacht werden, die sich auf organisationsübergreifende Anforderungen auswirkt.  

### <a name="org-relationship-mitigation"></a>Risikominderung für Organisationsbeziehungen  

Mehrere beliebte Websites verwalten sowohl Websites als auch Netzwerke für die Inhaltsübermittlung \(CDNs\), um statische Ressourcen und Inhalte für diese Websites zu verwenden.  Um sicherzustellen, dass diese Arten von Szenarien von der Nachverfolgungsverhinderung nicht betroffen sind, Microsoft Edge eine Website von der Nachverfolgungsverhinderung ausnehmen, wenn die Website Anforderungen von Drittanbietern an andere Websites stellt, die derselben übergeordneten Organisation gehören \(wie in der [Disconnect entities.json list][GitHubDisconnectMeTrackingProtectionEntitiesJson]\definiert).  Dies wird am besten anhand eines Beispiels veranschaulicht.  

> **Beispiel:**
> 
> Eine Organisation mit dem Namen "Org1" besitzt die Domänen `org1.test` und , wie in der Liste `org1-cdn.test` ["Trennen" entities.js][GitHubDisconnectMeTrackingProtectionEntitiesJson]definiert.  Imagine, die `org1-cdn.test` als Tracker klassifiziert wird und normalerweise Durchsetzungsmaßnahmen zur Verfolgungsverhinderung angewendet werden.  Wenn ein Benutzer besucht `https://org1.test` und die Website versucht, eine Ressource zu `https://org1-cdn.test` laden, führt Microsoft Edge keine Erzwingungsaktionen für Anforderungen aus, die an gestellt werden, obwohl es sich nicht um `org1-cdn.test` eine Erstanbieter-URL handelt.  Wenn jedoch eine andere URL, die nicht Teil der Organisation Org1 ist, versucht, dieselbe Ressource zu laden, unterliegt die Anforderung den Erzwingungen, da sie nicht Teil derselben Organisation ist.  
> 
> Obwohl dies die Durchsetzung von Nachverfolgungsverhinderung für Websites erleichtert, die derselben Organisation angehören, ist es unwahrscheinlich, dass dies ein hohes Maß an Datenschutzrisiko mit sich bringt, da solche Organisationen in der Lage sind, zu bestimmen, auf welche Websites/Ressourcen Sie zugegriffen `https://org1.test` haben, sowie `https://org1-cdn.test` interne Back-End-Daten zu verwenden.  

### <a name="org-engagement-mitigation"></a>Risikominderung durch Org Engagement  

Die Risikominderung des Organisationsengagements wurde erstellt, um Kompatibilitätsrisiken zu minimieren, die durch die Nachverfolgung der Verhinderung entstehen, indem sichergestellt wird, dass Websites im Besitz von Organisationen, mit denen Benutzer ausreichend interagieren, weiterhin wie erwartet im Web funktionieren.  Die [Websitebindung][ChromiumDesignDocsSiteEngagement] wird verwendet, um die Erzwingung zu lockern, wenn ein Benutzer eine fortlaufende Beziehung \(derzeit durch einen Standort-Engagement-Score von 4,1 oder höher\ definiert) mit einer bestimmten Website eingerichtet hat.  Dies lässt sich am besten anhand eines Beispiels veranschaulichen:

> **Beispiel:**
> 
> Eine Organisation mit dem Namen "Soziale Organisation" besitzt die Domänen `social.example` und `social-videos.example` .
> 
> Es wird davon ausgegangen, dass Benutzer eine Beziehung mit der Organisation für soziale Netzwerke haben, wenn sie eine Site-Engagement-Bewertung von 4,1 oder höher mit einer der Domänen eingerichtet haben, die im Besitz von Social Org sind.
> 
> Wenn eine andere Website, Inhalte von `https://content-embedder.example` Drittanbietern \(z. B. ein eingebettetes Video von \) aus einer der Domänen enthält, die sich im Besitz der Organisation für soziale Netzwerke `social-videos.example` befinden und normalerweise durch die Verfolgung von Verhinderungserzwingungen eingeschränkt würden, ist die Website von der Nachverfolgung von Durchsetzungsmaßnahmen zur Verhinderung ausgenommen, solange die Website-Interaktionsbewertung des Benutzers mit Domänen, die im Besitz der Organisation für soziale Netzwerke sind, über dem Schwellenwert gehalten wird.
> 
> Wenn eine Website nicht zu einer Organisation gehört, muss ein Benutzer eine Standortaktivierungsbewertung von 4,1 oder höher einrichten, bevor speicherzugriffs-/ressourcenlastblöcke, die durch die Nachverfolgungsverhinderung erzwungen werden, gelockert werden.

Die Risikominderung des Organisationsengagements wird derzeit nur im ausgeglichenen Modus angewendet, sodass Microsoft Edge den größtmöglichen Schutz für Benutzer bietet, die sich für Strict entschieden haben.

### <a name="the-compatexceptions-list"></a>Die CompatExceptions-Liste  

Basierend auf dem kürzlich von Microsoft erhaltenen Benutzerfeedback verwaltet Microsoft Edge eine kleine Liste von Websites \(die meisten befinden sich in der Kategorie "Inhalt trennen"\), die aufgrund der Nachverfolgungsverhinderung unterbrochen wurden, obwohl die oben genannten beiden Gegenmaßnahmen vorhanden waren. Websites in dieser Liste sind von der Verfolgung der Durchsetzung der Verhinderung ausgenommen.  Die Liste befindet sich auf dem Datenträger an den unten beschriebenen [Speicherorten.](#determining-whetherhow-a-particular-url-is-classified)  Benutzer können Einträge darin mithilfe der Option **"Blockieren"** in `edge://settings/content/cookies` überschreiben.

Um zu vermeiden, dass diese Liste in Zukunft beibehalten wird, arbeitet Microsoft derzeit an der [Storage Access-API][GitHubMsExplainersStorageAccessApi] in der Chromium Codebasis.  Die [Storage Access-API][GitHubMsExplainersStorageAccessApi] bietet Websiteentwicklern die Möglichkeit, den Speicherzugriff von Benutzern direkt anzufordern. Sie bietet Benutzern mehr Transparenz darüber, wie sich ihre Datenschutzeinstellungen auf ihre Browsererfahrung auswirken, und bietet Websiteentwicklern Die Steuerungsmöglichkeiten, um sich selbst schnell und intuitiv zu entsperren.

Nachdem die [Storage Access-API][GitHubMsExplainersStorageAccessApi] implementiert wurde, setzt Microsoft die CompatExceptions-Liste ab und wendet sich an die betroffenen Websites, um sie auf die Probleme aufmerksam zu machen und die Verwendung der [Storage Access-API][GitHubMsExplainersStorageAccessApi] in Zukunft anzufordern.  

## <a name="current-tracking-prevention-behavior"></a>Aktuelles Verhalten der Nachverfolgungsverhütung  

In der folgenden Tabelle sind die Erzwingungsaktionen und -gegenmaßnahmen aufgeführt, die auf jede Kategorie von klassifizierten Trackern in Microsoft Edge angewendet werden.  

*   Oben sind die Kategorien von Trackern aufgeführt, die durch die Listenkategorien des [Tracking-Schutzes][GitHubDisconnectTrackingProtectionCategories]trennen definiert sind.  
*   Auf der linken Seite befinden sich die drei Stufen der Nachverfolgungsverhinderung in Microsoft Edge \(Basic, Balanced und Strict\).  
*   Der Buchstabe `S` weist darauf hin, dass der Speicherzugriff blockiert ist.  
*   Der Buchstabe `B` weist darauf hin, dass sowohl speicherzugriff als auch Ressourcenlasten \(z. B. Netzwerkanforderungen\) blockiert sind.  
*   Ein Bindestrich \( `-` \) gibt an, dass kein Block auf Speicherzugriff oder Ressourcenlasten angewendet wird.  

| | Werbung | Analysen | Inhalt | Kryptomining | Fingerabdruck | Soziale Netzwerke | Other | Gegenmaßnahmen der gleichen Organisation | Risikominderung durch Org Engagement |  
| - | - | - | - | - | - | - | - | - | - | - |  
| **Einfach** | - | - | - | B | B | - | - | Aktiviert | Nicht zutreffend |  
| **Ausgeglichen** | E | - | E | B | B | E | E | Aktiviert | Aktiviert |  
| **Streng** | B | B | E | B | B | B | B | Aktiviert | Deaktiviert |  

> [!NOTE]
> Die Risikominderung des Organisationsengagements gilt nicht für die Kategorien Cryptomining oder Fingerabdruck.  

> [!TIP]
> Der strikte Modus blockiert mehr Ressourcenlasten als Balanced.  Das Blockieren weiterer Ressourcenlasten kann dazu führen, dass der Strict-Modus weniger Tracking-Anforderungen blockiert als Balanced, da die Tracker, die die Anforderungen stellen, nie geladen werden.  

> [!NOTE]
> Die Spalte "Fingerabdruck" im [Aktuellen Tracking-Verhinderungsverhalten](#current-tracking-prevention-behavior) bezieht sich auf Tracker, die sich zusätzlich zu einer anderen Liste in der Fingerabdruckliste befinden.  Tracker, die ausschließlich in der Fingerabdruckliste angezeigt werden, gelten als nicht böswillige Fingerabdrucker und werden nicht blockiert.

### <a name="inprivate-behavior"></a>InPrivate-Verhalten  

In Microsoft Edge 79 bestand das Standardverhalten darin, strenge Modusschutzmechanismen in InPrivate anzuwenden.  In Microsoft Edge 80 wurde dieses Verhalten durch einen Schalter ersetzt, mit dem Benutzer entscheiden können, ob sie `edge://settings/privacy` den strengen Modus anwenden oder ihre regulären Einstellungen beim Browsen in InPrivate beibehalten möchten.  

## <a name="determining-whetherhow-a-particular-url-is-classified"></a>Bestimmen, ob/wie eine bestimmte URL klassifiziert wird  

Die einfachste Möglichkeit, um festzustellen, ob eine bestimmte URL als bekannter Tracker klassifiziert wird, besteht darin, die folgenden Schritte auszuführen.  

1.  Öffnen Sie DevTools, und navigieren Sie zur Registerkarte "Konsole".  
1.  Aktualisieren Sie die Webseite.  
    1.  Möglicherweise möchten Sie **Cookies und andere Websitedaten** zuerst löschen, um die Ergebnisse des Website-Engagements zurückzusetzen und eine völlig sauberen Schiefer zu gewährleisten.  
1.  Suchen Sie nach Nachrichten, die `Tracking Prevention blocked access to storage for <URL>` lesen.  
    1.  Sie können die Nachrichten erweitern, um die einzelnen URLs anzuzeigen, die blockiert wurden.  
1.  Wenn Sie ermitteln müssen, in welcher Kategorie sich eine bestimmte blockierte Website befindet, suchen Sie dazu am einfachsten im [services.js"Trennen"][GitHubDisconnectTrackingProtectionCategories]in der Liste danach.  Die Einträge sind alphabetisiert, sodass Sie mit einem Bildlauf nach oben in einem Block von Websiteeinträgen die spezifische Kategorie für eine bestimmte Website finden können.  

> [!TIP]
> Wenn Sie auf die auf dem Datenträger gespeicherten Listen zur Nachverfolgungsverhinderung zugreifen müssen, finden Sie diese an einem von zwei Speicherorten.  
>
> **Komponentenbasierte Updates** – Die Listen, die von der Komponente "Vertrauensschutzlisten" heruntergeladen werden  
>
> Fenster: `%LOCALAPPDATA%\Microsoft\Edge <OptionalChannelName>\User Data\Trust Protection Lists`  
>
> Macos: `~/Library/Application Support/Microsoft Edge <OptionalChannelName>/Trust Protection Lists`  
>
> **Installationsverzeichnis** – Die Listen, die mit dem Microsoft Edge Installer gebündelt sind.  Wenn Sie ein anderes Installationsverzeichnis ausgewählt haben, können die genauen Pfade unterschiedlich sein.  
>
> Fenster: `%PROGRAMFILES(x86)%\Microsoft\ Edge <OptionalChannelName>\Application<Version>\Trust Protection Lists`  
>
> Macos: `/Applications/Microsoft Edge.app/Contents/Frameworks/Microsoft Edge Framework.framework/Libraries/Trust Protection Lists`  

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen  

Der folgende Abschnitt enthält Antworten auf häufig gestellte Fragen zum Feature zur Nachverfolgungsverhütung in Microsoft Edge.  

**Gibt es eine Möglichkeit, bestimmte Tracker zu Debugzwecken zu blockieren oder zuzulassen?**  

Derzeit macht Microsoft Edge nur eine Option verfügbar, um die Ausführung von Tracking-Verhinderungserzwingungen auf einer bestimmten Website zu deaktivieren.  Auf diese Option kann über das Seiteninfo-Flyout oder über die Seite zugegriffen `edge://settings/privacy/trackingPreventionExceptions` werden.  

Allerdings können die Optionen **"Blockieren"** und **"Zulassen"** auf der `edge://settings/content/cookies` Seite verwendet werden, um bestimmten Domänen den Zugriff auf Speicher wie Cookies und andere Browserspeichermechanismen zu erlauben oder zu verweigern.  Dies ist nützlich, um Websiteprobleme zu debuggen, die durch nachverfolgte Verhinderungserzwingungen verursacht werden, die den Zugriff auf den Speicher für eine bestimmte Website blockieren.  

<!-- image links -->  

[ImageThreeSettingsTrackingPrevention]: ./media/tracking-prevention-settings.png  
[ImageBlockedTrackersPageInfoFlyout]: ./media/page-info-flyout.png  

<!-- links -->  

[MicrosoftEdgeBrowserPrivacyPromise]: https://microsoftedgewelcome.microsoft.com/privacy "Datenschutz – Microsoft Edge"  

[ChromiumDesignDocsSiteEngagement]: https://www.chromium.org/developers/design-documents/site-engagement "Site Engagement – die Chromium Projekte"  

[DisconnectMain]: https://disconnect.me "Trennen"  

[GitHubDisconnectMeTrackingProtection]: https://github.com/disconnectme/disconnect-tracking-protection "disconnectme/disconnect-tracking-protection | Github"  
[GitHubDisconnectTrackingProtectionCategories]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/services.json "services.json – disconnectme/disconnect-tracking-protection | Github"  
[GitHubDisconnectMeTrackingProtectionEntitiesJson]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/entities.json "entities.json – disconnectme/disconnect-tracking-protection | Github"  

[GitHubMsExplainersStorageAccessApi]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/StorageAccessAPI/explainer.md "Storage Access API Explainer – MSEdgeExplainers/StorageAccessAPI | GitHub"
