---
description: Microsoft Edge Add-Ons Store Entwicklerrichtlinien
title: Microsoft Edge Add-Ons Store Entwicklerrichtlinien
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungsentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 8b3e537752e1f5e891626f8cd28cb89806295166
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643427"
---
# <a name="microsoft-edge-add-ons-store-developer-policies"></a>Microsoft Edge Add-Ons Store Entwicklerrichtlinien  

## <a name="introduction-and-objective-of-this-document"></a>Einführung und Ziel dieses Dokuments  

Vielen Dank für Ihr Interesse an der Entwicklung von Erweiterungen für den Microsoft Edge Add-Ons Store.  Die Microsoft Edge Add-Ons store developer policies \(Add-ons store developer policies\) gelten für Ihre Erweiterungen, einschließlich der Übermittlung von Erweiterungen über [Partner Center][MicrosoftPartnerCenter] und der Bereitstellung solcher Erweiterungen über die Microsoft Edge-Add-Ons.  

## <a name="principles"></a>Prinzipien  

Zunächst einige wichtige Grundregeln:  

*   Sie sollten einen eindeutigen und eindeutigen Wert in Ihren Erweiterungen für Microsoft Edge bieten.  Geben Sie einen überzeugenden Grund an, Ihre Erweiterungen aus dem Microsoft Edge Add-Ons Store \(Microsoft Edge Add-Ons\) herunterzuladen.  
*   Sie dürfen unsere gemeinsamen Benutzer nicht darüber in die Irre führen, was Ihre Erweiterung bewirkt, wer sie anbietet usw.  
*   Sie dürfen nicht versuchen, Benutzer, das System oder das Ökosystem zu betrügen.  In unseren Microsoft Edge-Add-Ons gibt es keinen Ort für jegliche Art von Betrug. Sei es Bewertungen und Überprüfung von Manipulationen, Kreditkartenbetrügern oder anderen betrügerischen Aktivitäten.  
    
Die Einhaltung der Entwicklerrichtlinien für den Microsoft Edge Add-Ons Store sollte Ihnen helfen, Entscheidungen zu treffen, die die Benutzerfreundlichkeit und Zielgruppe Ihrer Erweiterung verbessern.  

Ihre Erweiterungen sind entscheidend für die Erfahrung von Hunderten Millionen Von Benutzern.  Wir freuen uns darauf, das zu erleben, was Sie erstellen, und freuen uns, Ihre Erweiterungen auf der ganzen Welt bereitzustellen.  

## <a name="1-product-policies"></a>1. Produktrichtlinien  

### <a name="11-distinct-function--value-accurate-representation"></a>1.1 Distinct Function & Value; Genaue Darstellung  

Ihre Erweiterung und die zugehörigen Metadaten müssen die Quelle, Funktionalität und Features, die Sie beschreiben, genau und deutlich wiedergeben.  

#### <a name="111-extensions-must-have-a-single-purpose"></a>1.1.1 Erweiterungen müssen einen einzigen Zweck haben  

Ihre Erweiterung muss einen einzigen Zweck mit schmaler Funktionalität haben.  

#### <a name="112-describe-your-extension"></a>1.1.2 Beschreiben Der Erweiterung  

Alle Aspekte Ihrer Erweiterung sollten die Funktionen, Features und wichtigen Einschränkungen Ihrer Erweiterung, einschließlich erforderlicher oder unterstützter Eingabegeräte, genau beschreiben.  Das Leistungsversprechen Ihrer Erweiterung muss während der ersten Ausführung klar sein.  Ihre Erweiterung darf keinen Namen oder kein Symbol wie andere Erweiterungen verwenden und darf nicht beanspruchen, ein Unternehmen, einen Behördenkörper oder eine andere Entität darzustellen, wenn Sie nicht über die Berechtigung verfügen, diese Darstellung vorzunehmen.  

#### <a name="113-functionality"></a>1.1.3 Funktionalität  

Die Erweiterung muss voll funktionsfähig sein.  

#### <a name="114-search-and-discovery"></a>1.1.4 Suche und Ermittlung  

Suchbegriffe dürfen sieben eindeutige Begriffe nicht überschreiten und sollten für Ihre Erweiterung relevant sein.  

#### <a name="115-provide-appropriate-details"></a>1.1.5 Geben Sie die entsprechenden Details an  

Sie müssen eindeutige und informative Details zu Ihrer Erweiterung und die Funktionalität im Eintrag \(Metadaten\) für Ihre Erweiterung angeben.  Ihre Erweiterung muss eine wertvolle und qualitativ hochwertige Benutzererfahrung bieten.  Ihre Erweiterung muss auch in Microsoft Edge Add-Ons aktiv sein.  

#### <a name="116-stability-and-performance"></a>1.1.6 Stabilität und Leistung  

Ihre Erweiterung darf sich nicht negativ auf die Leistung oder Stabilität von Microsoft Edge auswirken.  

#### <a name="117-obfuscation"></a>1.1.7 Verschleierung  

Erweiterungen mit verborgenem Code sind nicht zulässig.  Dazu gehören code within your extension package sowie any external code or resource fetched from the web.  Möglicherweise werden Sie aufgefordert, Teile Des Codes umgestalten, wenn er nicht überprüft werden kann.  

#### <a name="118-altering-browser-settings"></a>1.1.8 Ändern der browserbasierten Einstellungen  

Ihre Erweiterung darf ohne entsprechende Zustimmung des Benutzers die Browserfunktionalität oder -einstellungen nicht ändern oder ändern, einschließlich, aber nicht beschränkt auf: den Suchanbieter und Vorschläge der Adressleiste, die Startseite, die neue Registerkartenseite und das Hinzufügen oder Entfernen des Favoriten.  

Änderungen an den Browsereinstellungen sollten explizit in der Beschreibung Ihrer Erweiterung dokumentiert werden.  

Ihre Erweiterung kann wichtige Einstellungen nur überarbeiten, um eine Microsoft-Webseite oder einen Dienst durch die eines Drittanbieters zu ersetzen (z. B. die Verwendung einer Suchmaschine eines Drittanbieters erfordern oder die Startseite auf eine Drittanbieter-Webeigenschaft festlegen\), wenn Sie von einem solchen Drittanbieter angestellt oder anderweitig mit diesem verbunden sind.  

### <a name="12-security"></a>1.2 Sicherheit  

Ihre Erweiterung darf weder die Benutzersicherheit noch die Sicherheit oder Funktionalität des Geräts, Systems oder verwandter Systeme gefährden oder gefährden.  

#### <a name="121-content-security-policies"></a>1.2.1 Inhaltssicherheitsrichtlinien  

> [!NOTE]
> Wenn Sie Änderungen an Ihrer Erweiterung vornehmen, die über die beschriebene Funktionalität hinausgehen, müssen alle Codeänderungen mit der [Microsoft Edge Inhaltssicherheitsrichtlinie][MicrosoftEdgeContentSecurityPolicyRemoteScript]konform sein.  Ihre Erweiterung sollte z. B. kein Remoteskript herunterladen und dieses Skript anschließend auf eine Weise ausführen, die nicht mit der beschriebenen Funktionalität übereinstimmt.  

#### <a name="122-unwanted-and-malicious-software"></a>1.2.2 Unerwünschte und bösartige Software  

Ihre Erweiterung darf keine Schadsoftware enthalten oder aktivieren, wie in den Microsoft-Kriterien für [unerwünschte und bösartige Software][MicrosoftIdentifiesMalwareUnwantedApplications]definiert.  

#### <a name="123-dependency-on-other-software"></a>1.2.3 Abhängigkeit von anderer Software  

Ihre Erweiterung hängt möglicherweise von nicht integrierter Software \(z. B. einem anderen Produkt, Modul oder Dienst\) ab, um die primäre Funktionalität bereitzustellen, vorausgesetzt, Sie geben die Abhängigkeit in der Beschreibung offen.  

#### <a name="124-extensions-update"></a>1.2.4 Erweiterungsupdate  

Sofern nicht anders von Microsoft zugelassen, dürfen Ihre Erweiterungen nur über Microsoft Edge-Add-Ons aktualisiert werden.  

### <a name="13-product-is-testable"></a>1.3 Produkt kann getestet werden  

Ihre Erweiterung muss testbar sein.  Wenn es nicht möglich ist, Ihre Erweiterung aus irgendeinem Grund zu testen, einschließlich, aber nicht beschränkt auf die unten stehenden Elemente, kann ihre Erweiterung diese Anforderung nicht erfüllen.  

#### <a name="131-user-credentials"></a>1.3.1 Benutzeranmeldeinformationen  

Wenn Ihre Erweiterung Anmeldeinformationen erfordert, geben Sie ein funktionierendes Demokonto mithilfe des `Notes for certification` Felds an.  

#### <a name="132-availability-of-services"></a>1.3.2 Verfügbarkeit von Diensten  

Wenn Ihre Erweiterung Zugriff auf einen Server benötigt, muss der Server funktionsfähig sein, um sicherzustellen, dass er ordnungsgemäß funktioniert.  

### <a name="14-usability"></a>1.4 Benutzerfreundlichkeit  

Ihre Erweiterung muss Microsoft Edge Add-Ons-Speicherstandards für die Benutzerfreundlichkeit erfüllen, einschließlich, aber nicht beschränkt auf die in den unteren Abschnitten unten aufgeführten Standards.  

#### <a name="141-compatibility-across-platforms"></a>1.4.1 Plattformübergreifende Kompatibilität  

Ihre Erweiterung sollte mit Microsoft Edge auf allen Geräten und Plattformen kompatibel sein, auf die sie heruntergeladen werden können.  Wenn eine Erweiterung auf ein Gerät heruntergeladen wird, mit dem sie nicht kompatibel ist, sollte sie dies beim Start erkennen und dem Benutzer eine Meldung anzeigen, in der die Anforderungen aufgeführt sind, die Geräte erfüllen müssen, um mit Ihrer Erweiterung kompatibel zu sein.  

#### <a name="142-user-experience"></a>1.4.2 Benutzererfahrung  

Ihre Erweiterung muss sofort gestartet werden und für Benutzereingaben reaktionsfähig bleiben.  Ihre Erweiterung muss weiterhin ausgeführt werden und für Benutzereingaben reaktionsfähig bleiben.  Ihre Erweiterung muss ordnungsgemäß heruntergefahren werden und nicht unerwartet geschlossen werden.  Die Erweiterung sollte Ausnahmen behandeln und auf Benutzereingaben reagieren, nachdem die Ausnahme behandelt wurde.  

### <a name="15-personal-information"></a>1.5 Persönliche Informationen  

Die folgenden Anforderungen gelten für Erweiterungen, die auf persönliche Informationen zugreifen.  Personenbezogene Informationen umfassen alle Informationen oder Daten, die eine Person identifizieren oder zur Identifizierung verwendet werden können oder die mit diesen Informationen oder Daten verknüpft sind.  

#### <a name="151-collect-personal-information-only-when-necessary"></a>1.5.1 Persönliche Informationen nur bei Bedarf sammeln  

Ihre Erweiterung kann personenbezogene Informationen sammeln, auf sie zugreifen, diese verwenden oder übertragen \(einschließlich Webbrowsingaktivität\); nur, wenn dies von und nur für die Verwendung in einem hervorgehoben offengelegten, benutzerorientierten Feature erforderlich ist.  

#### <a name="152-maintain-a-privacy-policy"></a>1.5.2 Verwalten einer Datenschutzrichtlinie  

Unabhängig davon, ob Ihre Erweiterung auf personenbezogene Informationen zugreift, diese sammelt oder überträgt; Sie müssen Ihre Datenschutzrichtlinie bekannt geben und einhalten, wenn dies gesetzlich vorgeschrieben ist.  Ihre Datenschutzrichtlinie muss die Benutzer über die personenbezogenen Informationen informieren, auf die von Ihrer Erweiterung zugegriffen, gesammelt oder übermittelt wurde, wie diese Informationen verwendet, gespeichert und gesichert werden, und die Arten von Parteien angeben, für die sie offengelegt werden.  Ihre Datenschutzrichtlinie muss die Steuerelemente beschreiben, über die Benutzer über die Nutzung und Freigabe ihrer Informationen verfügen, wie sie auf ihre Informationen zugreifen, und sie muss die geltenden Gesetze und Vorschriften einhalten.  Ihre Datenschutzrichtlinie muss auf dem neuesten Stand gehalten werden, wenn Sie Ihrer Erweiterung neue Features und Funktionen hinzufügen.  

Wenn Sie Microsoft Ihre Datenschutzrichtlinie zur Verfügung stellen, erklären Sie sich damit einverstanden, Microsoft zu gestatten, diese Datenschutzrichtlinie für Benutzer Ihrer Erweiterung freizugeben.  

#### <a name="153-sharing-data-with-third-parties"></a>1.5.3 Freigeben von Daten für Dritte  

Sie können die persönlichen Informationen von Benutzern Ihrer Erweiterung nur nach Erhalt der Zustimmung dieser Benutzer für einen externen Dienst oder Drittanbieter über Ihre Erweiterung oder zugehörige Metadaten veröffentlichen.  "Zustimmung" bedeutet, dass die Benutzer ihre ausdrückliche Berechtigung in der Benutzeroberfläche Ihrer Erweiterung für die angeforderte Aktivität erteilen, nachdem Sie:  

*   Beschreiben Sie Ihren Benutzern, wie auf die Informationen zugegriffen, verwendet oder freigegeben wird, und geben Sie die Arten von Parteien an, für die sie offengelegt werden, und  
*   Stellen Sie Ihren Benutzern einen Mechanismus auf der Benutzeroberfläche ihrer Erweiterung bereit, über den sie die Möglichkeit haben, die Berechtigung später aufzuheben und abzumelden.  
    
#### <a name="154-sharing-information-of-non-users"></a>1.5.4 Freigabeinformationen von Nicht-Benutzern  

Wenn Sie die persönlichen Informationen einer Person über Ihre Erweiterung oder die Metadaten für einen externen Dienst oder Drittanbieter veröffentlichen, die Person, deren Informationen freigegeben werden, jedoch kein Benutzer Ihrer Erweiterung ist;  

1.  Sie müssen die ausdrückliche schriftliche Zustimmung einholen, um diese persönlichen Informationen zu veröffentlichen.  
1.  Sie müssen zulassen, dass die Person, deren Informationen freigegeben werden, diese Zustimmung jederzeit widerruft.  
1.  Ihre Datenschutzrichtlinie muss deutlich offenlegen, dass Sie personenbezogene Informationen auf diese Weise sammeln dürfen.  
1.  Wenn dies nach geltendem Recht erforderlich ist, müssen Sie die personenbezogenen Informationen einer beliebigen Person auf Anfrage löschen, einschließlich Personen, deren Informationen Sie auf diese Weise sammeln.  
1.  Wenn Ihre Erweiterung Benutzern Zugriff auf die persönlichen Informationen einer anderen Person bietet, gilt diese Anforderung auch.  
    
#### <a name="155-transmit-information-securely"></a>1.5.5 Informationen sicher übertragen  

Wenn Ihre Erweiterung personenbezogene Informationen sammelt, speichert oder überträgt; Dies muss mithilfe moderner Kryptografiemethoden sicher erfolgen.  

#### <a name="156-highly-sensitive-information"></a>1.5.6 Streng vertrauliche Informationen  

Ihre Erweiterung darf keine streng vertraulichen persönlichen Informationen wie Gesundheits- oder Finanzdaten sammeln, speichern oder übertragen, es sei denn, die Informationen beziehen sich auf die Funktionalität Ihrer Erweiterung.  Ihre Erweiterung muss auch die ausdrückliche Zustimmung des Benutzers einholen, bevor diese Informationen gesammelt, gespeichert oder übertragen werden.  

### <a name="16-permissions"></a>1.6 Berechtigungen  

Ihre Erweiterung darf nur die Berechtigungen anfordern, die für die Funktion erforderlich sind.  Sie müssen eine Beschreibung der Funktionsweise Ihrer Erweiterung angeben.  Die Erweiterung darf nur wie beschrieben ausgeführt werden.  Ihre Erweiterung fordert möglicherweise keine Berechtigung für Funktionen an, die über die für die Ausführung und Funktion erforderlichen Funktionen hinausgehen, wie deklariert.  

### <a name="17-localization"></a>1.7 Lokalisierung  

Sie sollten Die Erweiterung für alle Sprachen lokalisieren, die ihre Erweiterung unterstützen soll.  Der Text der Beschreibung Der Erweiterung sollte in jeder Sprache lokalisiert werden, die Sie deklarieren.  
Wenn Ihre Erweiterung so lokalisiert ist, dass einige Features in einer lokalisierten Version nicht verfügbar sind, müssen Sie die Grenzen der Lokalisierung in Ihrer Erweiterungsbeschreibung deutlich angeben oder anzeigen. Die von einer Erweiterung bereitgestellte Erfahrung muss in allen unterstützten Sprachen einigermaßen ähnlich sein.  

### <a name="18-financial-transactions"></a>1.8 Finanztransaktionen  

Wenn Ihr Produkt produktinterne Käufe, Abonnements, virtuelle Währung, Abrechnungsfunktionen oder finanzbezogene Informationen enthält; es gelten die Anforderungen in den folgenden Abschnitten.  

#### <a name="181-paid-features"></a>1.8.1 Kostenpflichtige Features  

Ihre Erweiterung kann es Benutzern ermöglichen, digitale Inhalte oder Dienste zu nutzen, die über einen Drittanbieter-Kaufmechanismus oder eine API erworben wurden.  

Sie müssen eine sichere Drittanbieter-Einkaufs-API für den Kauf von physischen Waren oder Dienstleistungen verwenden.  Sie müssen eine sichere Drittanbieter-Einkaufs-API für Zahlungen verwenden, die in Verbindung mit anderen Diensten, einschließlich realer Spiele oder Hilfsbeiträgen, getätigt werden.  

*   Wenn Ihre Erweiterung verwendet wird, um Beitragsbeiträge zu erleichtern oder zu sammeln oder um Werbeauslosungen oder -prüfungen durchzuführen, müssen Sie dies in Übereinstimmung mit dem geltenden Recht tun.  
*   Zudem muss deutlich gemacht werden, dass Microsoft weder als Spendensammler noch als Sponsor der Werbeaktion auftritt.  
*   In Ihrer Erweiterung verkaufte Produktangebote dürfen nicht in eine rechtsgültige Währung \(z. B. USD, Euro usw.\) oder physische Waren oder Dienstleistungen umgewandelt werden.  
    
Für die Verwendung einer sicheren Drittanbieter-Einkaufs-API gelten die folgenden Anforderungen:  

*   Zum Zeitpunkt der Transaktion oder beim Sammeln von Zahlungs- oder Finanzinformationen des Benutzers; Ihre Erweiterung muss den Anbieter der Commerce-Transaktion identifizieren, den Benutzer authentifizieren und eine Benutzerbestätigung für die Transaktion erhalten.  Ein Anbieter von Handelstransaktionen verwaltet eine sichere Plattform für den Finanzaustausch.  
*   Ihre Erweiterung bietet Benutzern möglicherweise die Möglichkeit, diese Authentifizierung zu speichern, aber die Benutzer müssen entweder eine Authentifizierung für jede Transaktion anfordern oder Produkttransaktionen deaktivieren können.  
*   Wenn Ihre Erweiterung Kreditkarteninformationen sammelt oder einen Drittanbieter-Zahlungsauftragsverarbeiter verwendet, der Kreditkarteninformationen sammelt, muss die Zahlungsverarbeitung den aktuellen PCI Data Security Standard \(PCI DSS\) erfüllen.  
    
#### <a name="182-disclosing-paid-features"></a>1.8.2 Offenlegung kostenpflichtiger Features  

Ihre Erweiterung und die zugehörigen Metadaten müssen Informationen über die Art der angebotenen Produktkäufe und den Preisbereich bereitstellen.  Sie dürfen Benutzer nicht in die Irre führen und müssen über die Art Ihrer produktinternen Werbeaktionen und Angebote, einschließlich des Umfangs und der Bedingungen von Testerfahrungen, informiert sein.  Wenn Ihre Erweiterung den Zugriff auf vom Benutzer erstellte Inhalte während oder nach einer Testversion einschränkt, müssen Sie die Benutzer im Voraus benachrichtigen.  Darüber hinaus muss Ihre Erweiterung den Benutzern deutlich machen, dass sie eine Kaufoption in Ihrer Erweiterung initiieren.  

### <a name="19-notifications"></a>1.9 Benachrichtigungen  

Ihre Erweiterung muss die Systemeinstellungen für Benachrichtigungen berücksichtigen.  Dies bedeutet, dass jede Darstellung von Anzeigen und Benachrichtigungen für Benutzer mit den Benutzereinstellungen konsistent sein muss, unabhängig davon, ob die Benachrichtigungen vom Microsoft-Pushbenachrichtigungsdienst \(MPNS\), Windows Pushbenachrichtigungsdienst \(WNS\) oder einem anderen Dienst bereitgestellt werden.  Wenn der Benutzer Benachrichtigungen entweder produktspezifisch oder systemweit deaktiviert, muss Ihre Erweiterung funktionsfähig bleiben.  

Wenn Ihr Produkt MPNS oder WNS zum Übertragen von Benachrichtigungen verwendet, muss es die folgenden Anforderungen erfüllen:  

#### <a name="191-general-guidance"></a>1.9.1 Allgemeiner Leitfaden  

Benachrichtigungen, die über WNS oder MPNS bereitgestellt werden, gelten als Produktinhalte und unterliegen allen Add-Ons-Katalog-Entwicklerrichtlinien.  

#### <a name="192-ownership-of-notifications"></a>1.9.2 Besitz von Benachrichtigungen  

Sie dürfen die Quelle von Benachrichtigungen, die von Ihrer Erweiterung initiiert wurden, weder verdecken noch versuchen, sie zu verbergen.  

#### <a name="193-no-confidential-or-sensitive-information"></a>1.9.3 Keine vertraulichen oder vertraulichen Informationen  

Sie dürfen keine Informationen in eine Benachrichtigung aufnehmen, die Benutzer in angemessenem Umfang als vertraulich oder vertraulich betrachten können.  

#### <a name="194-purpose-of-notifications"></a>1.9.4 Zweck von Benachrichtigungen  

Benachrichtigungen, die von Ihrer Erweiterung gesendet werden, müssen sich auf diese Erweiterung oder auf andere Erweiterungen beziehen, die Sie im Store Microsoft Edge Add-Ons veröffentlichen, und dürfen keine Werbenachrichten jeglicher Art enthalten, die nicht mit Ihren Erweiterungen zusammenhängen.  

### <a name="110-advertising-conduct-and-content"></a>1.10 Werbeverhalten und -inhalte  

Für alle Aktivitäten im Zusammenhang mit Werbung gelten die folgenden Anforderungen:  

#### <a name="1101-purpose"></a>1.10.1 Zweck  

Der Hauptinhalt Ihrer Erweiterung darf keine Werbung sein, und Werbung muss deutlich von anderen Inhalten in Ihrer Erweiterung unterschieden werden können.  

#### <a name="1102-policies-and-agreements"></a>1.10.2 Richtlinien und Vereinbarungen  

Alle Von Ihrer Erweiterung angezeigten Werbeinhalte müssen der [Microsoft Creative Acceptance Policy][MicrosoftAdvertisingCreativeAcceptancePolicies]entsprechen.  
Wenn Ihre Erweiterung Anzeigen anzeigt, müssen alle angezeigten Inhalte den Werbeanforderungen der [Vereinbarung für App-Entwickler][MicrosoftAppDeveloperAgreement] und dieser Richtlinie entsprechen.  

#### <a name="1103-quality-of-advertising"></a>1.10.3 Qualität der Werbung  

*   Der Hauptzweck Ihrer Erweiterung darf nicht darin sein, Benutzer dazu zu bringen, auf Anzeigen zu klicken.  
*   Ihre Erweiterung darf keine Aktionen ausführen, die die Sichtbarkeit, den Wert oder die Qualität von Anzeigen beeinträchtigen oder verringern, die sie anzeigt.  

#### <a name="1104-promotions"></a>1.10.4 Werbeaktionen  

Wenn Sie Werbekampagnen erwerben oder erstellen, um Ihre Erweiterungen über die Funktionen der Anzeigenkampagne im [Partner Center][MicrosoftPartnerCenter]zu bewerben, müssen alle Anzeigenmaterialien, die Sie Microsoft zur Verfügung stellen, einschließlich aller zugehörigen Angebotsseiten, die Microsoft [Creative Specifications-Richtlinie][MicrosoftAdvertisingCreativeSpecifications] und [die Microsoft Creative Acceptance Policy][MicrosoftAdvertisingCreativeAcceptancePolicies]einhalten.  

#### <a name="1105-notifying-users-of-opt-out-for-interest-based-advertising"></a>1.10.5 Benachrichtigen von Benutzern über Opt-Out für Interest-Based Werbung  

Ihre Datenschutzbestimmungen oder Nutzungsbedingungen müssen Die Benutzer darüber informieren, dass Sie beabsichtigen, persönliche Informationen an den Anzeigendienstanbieter zu senden, und sie müssen den Benutzern mitteilen, wie sie sich von interessenbasierter Werbung abmelden können.  

#### <a name="1106-other-guidelines"></a>1.10.6 Weitere Richtlinien  

Wenn Ihre Erweiterung an Kinder unter 13 Jahren gerichtet ist, wie im [Children's Online Privacy Protection Act][FTCChildrensPrivacy]definiert; Sie müssen Microsoft im [Partner Center][MicrosoftPartnerCenter] darüber informieren und sicherstellen, dass alle in Ihrer Erweiterung angezeigten Anzeigeninhalte für Kinder unter 13 Jahren geeignet sind.  

## <a name="2-content-policies"></a>2 Inhaltsrichtlinien  

Die folgenden Richtlinien gelten für Inhalte und Metadaten \(einschließlich Herausgebername, Erweiterungsname, Erweiterungssymbol, Erweiterungsbeschreibung, Erweiterungsfotos, Erweiterungstrailer und Trailerminiaturansichten und alle anderen Erweiterungsmetadaten\), die für die Verteilung in Microsoft Edge-Add-Ons angeboten werden.  Inhalt bezeichnet die Bilder, Sounds, Videos und Text in Ihrer Erweiterung, die Kacheln, Benachrichtigungen, Fehlermeldungen oder Anzeigen, die über Ihre Erweiterung verfügbar gemacht werden, und alles, was von einem Server übermittelt wird oder mit dem Ihre Erweiterung eine Verbindung herstellt.  Da Erweiterungen und Microsoft Edge-Add-Ons auf der ganzen Welt verwendet werden, werden diese Anforderungen im Kontext von regionalen und kulturellen Normen interpretiert und angewendet.  

### <a name="21-content-requirements-for-microsoft-edge-addon-catalog-listing"></a>2.1 Inhaltsanforderungen für Microsoft Edge Addon-Katalogeintrag  

Metadaten und andere Inhalte, die Sie zur Erweiterung übermitteln, enthalten möglicherweise keine ausgereiften Inhalte.  
Übermittlungen, die nicht Microsoft Edge Anforderungen für Add-Ons store listings erfüllen, werden abgelehnt oder umgehend entfernt.  

### <a name="22-content-including-names-logos-original-and-third-party"></a>2.2 Inhalte wie Namen, Logos, Original und Drittanbieter  

Alle Inhalte in Ihrer Erweiterung und die zugehörigen Metadaten müssen entweder ursprünglich von Ihnen erstellt oder ordnungsgemäß von einem Drittanbieter lizenziert werden und dürfen nur verwendet werden, wenn dies vom Rechtsinhaber erlaubt oder anderweitig gesetzlich zulässig ist.  

### <a name="23-risk-of-harm"></a>2.3 Schadensrisiko  

#### <a name="231-requirements"></a>2.3.1 Anforderungen  

Ihre Erweiterung darf keine Inhalte enthalten, die die folgenden realen Aktivitäten erleichtern oder verherrlichen: \(a\) extreme oder willkürliche Gewalt; \(b\) Verletzungen der Rechte; \(c\) die Erstellung von illegalen Waffen; oder \(d\) die Verwendung von Waffen gegen eine Person, ein Tier oder ein echtes oder persönliches Eigentum.  

#### <a name="232-responsibility"></a>2.3.2 Verantwortlichkeit  

Ihre Erweiterung darf nicht: \(a\) ein Sicherheitsrisiko für Endbenutzer oder andere Personen oder Tiere darstellen oder zu Schäden führen, die weder für Endbenutzer noch für Tier oder Tier entstehen; oder \(b\) ein Risiko darstellen oder zu Schäden an realen oder persönlichen Eigenschaften führen.  Sie sind allein für alle Erweiterungssicherheitstests, den Zertifikaterwerb und die Implementierung geeigneter Funktionsvorkehrungen verantwortlich.  Sie dürfen keine Plattformsicherheits- oder Komfortfeatures deaktivieren, und Sie müssen alle anwendbaren gesetzlich erforderlichen und branchenüblichen Warnungen, Benachrichtigungen und Haftungsausschlüsse in Ihre Erweiterung aufnehmen.  

### <a name="24-defamatory-libelous-slanderous-and-threatening"></a>2.4 Verleumdung, Verleumdung, Verleumdung und Beleidigung  

Ihre Erweiterung darf keine Inhalte enthalten, die verleumderisch, verleumderisch, beleidigend oder bedrohlich sind.  

### <a name="25-offensive-content"></a>2.5 Anstößige Inhalte  

Ihre Erweiterung und die zugehörigen Metadaten dürfen keine potenziell vertraulichen oder anstößigen Inhalte enthalten.  Inhalte können in bestimmten Ländern/Regionen aufgrund lokaler Gesetze oder kulturellen Normen als vertraulich oder anstößig betrachtet werden.  Darüber hinaus dürfen Ihre Erweiterung und die zugehörigen Metadaten keine Inhalte enthalten, die Hass, Hass oder Gewalt aus Gründen der Ethnischen Herkunft, der nationalen Herkunft, der Sprache, des Geschlechtes, des Alters, der Invalidität, der Sexuellen Orientierung, des Status als Routinier oder der Mitgliedschaft in einer anderen sozialen Gruppe propagieren.  

### <a name="26-alcohol-tobacco-and-drugs"></a>2.6 Alko, Konsum und Drogen  

Ihre Erweiterung darf keine Inhalte enthalten, die den exzessiven oder unverantwortlichen Konsum von Konsum von Betäubsucht, Konsumprodukten oder Drogen erleichtern oder verherrlichen.  

### <a name="27-adult-content"></a>2.7 Nicht jugendfreie Inhalte  

Ihre Erweiterung darf keine Inhalte enthalten oder anzeigen, die eine angemessene Person als grafisch oder sexuallich explizit ansehen würde.  

### <a name="28-prohibited-content-services-and-activity"></a>2.8 Unzulässige Inhalte, Dienste und Aktivitäten  

Ihre Erweiterung muss die folgenden Bedingungen erfüllen.  

*   Ihre Erweiterung darf keine Inhalte enthalten oder Dienste bereitstellen, die das Online-Spiel erleichtern.  Online-Spiele umfassen unter anderem Online-, Sport- und Trainingsspiele, die Geld oder anderen Wert bieten.  
*   Ihre Erweiterung darf keinen nicht autorisierten Zugriff auf Websiteinhalte ermöglichen, z. B. durch Umgehung von Paywalls oder Anmeldeeinschränkungen.  
*   Ihre Erweiterung darf den nicht autorisierten Zugriff, den nicht autorisierten Download oder das Streaming urheberrechtlich geschützter Inhalte oder Medien nicht bereitstellen, fördern oder aktivieren.  
*   Ihre Erweiterung darf keine Kryptodaten minen.  
    
### <a name="29-illegal-activity"></a>2.9 Unzulässige Aktivitäten  

Ihre Erweiterung darf keine Inhalte oder Funktionen enthalten, die zu illegalen Aktivitäten in der realen Welt ermuntern, sie erleichtern oder verherrlichen.  

### <a name="210-excessive-profanity-and-inappropriate-content"></a>2.10 Exzessive Anstößigkeit und unangemessene Inhalte  

*   Ihre Erweiterung darf keine übermäßige oder willkürliche Anstößigkeit enthalten.  
*   Ihre Erweiterung darf keine Inhalte enthalten oder anzeigen, die eine angemessene Person als obszön betrachtet.  
    
### <a name="211-countryregion-specific-requirements"></a>2.11 Länder-/regionsspezifische Anforderungen  

Inhalte, die in allen Ländern/Regionen, auf die Ihre Erweiterung ausgerichtet ist, anstößig sind, sind nicht zulässig.  Inhalte können aufgrund lokaler Gesetze oder kultureller Normen in bestimmten Ländern/Regionen als beleidigend angesehen werden.  Beispiele für potenziell beleidigende Inhalte in bestimmten Ländern/Regionen:  

**China**  

*   Verbot pornographischer Inhalte  
*   Verweise auf umstrittene Gebiete oder Regionen  
*   Bereitstellung oder Zugriff auf Inhalte oder Dienste, die unter dem jeweils anwendbaren Recht rechtswidrig sind.  
    
### <a name="212-age-ratings"></a>2.12 Altersfreigaben  

#### <a name="2121-mature-content"></a>2.12.1 Ausgereifte Inhalte  

Wenn Sie Ihre Erweiterung an [Partner Center][MicrosoftPartnerCenter]übermitteln, müssen Sie angeben, ob ihre Erweiterung Inhalte anzeigt, die als "Ausgereift" gekennzeichnet werden sollen.  Berücksichtigen Sie bei der Festlegung der Bewertung für Ihre Erweiterung alle Inhalte in Ihrer App, einschließlich der vom Benutzer generierten Inhalte und Anzeigen, sowie die Inhalte, auf die Ihre Erweiterung verweist.  Wenn Sie angeben, dass Ihre Erweiterung keine "ausgereiften" Inhalte enthält, sind Sie für die Aufrechterhaltung der Genauigkeit dieser Bewertung verantwortlich.  Unabhängig von der Bewertung, die Ihrer Erweiterung erteilt wird, muss sie dennoch alle Inhaltsanforderungen von Microsoft Edge Add-Ons-Entwicklerrichtlinien erfüllen.  

#### <a name="2122-ratings-change"></a>2.12.2 Änderung der Bewertungen  

Wenn Ihre Erweiterung Inhalte \(z. B. vom Benutzer generierte, einzelhandelsbezogene oder andere webbasierte Inhalte\) bereitstellt, die möglicherweise für eine höhere Altersfreigabe als die zugewiesene Bewertung geeignet sind, müssen Sie festlegen, dass Benutzer sich für den Empfang solcher Inhalte entscheiden, indem Sie einen Inhaltsfilter verwenden oder sich mit einem bereits vorhandenen Konto anmelden.  

### <a name="213-videos"></a>2.13 Videos  

Wenn Sie ein Werbevideo im Eintrag übermitteln, sollte es allen in dieser Richtlinie genannten Inhaltsrichtlinien entsprechen.  Wenn Sie einen YouTube-Link bereitstellen, müssen Sie sicherstellen, dass Werbung für die spezifischen Videos, die Sie einbetten möchten, deaktiviert ist.  Weitere Informationen zum Aktivieren oder Deaktivieren von Anzeigen auf YouTube, navigieren Sie zu ["Standardanzeigeformate festlegen"][GoogleYoutubeAnswer2531367Topic7072227] und ["Anzeigen" in eingebetteten Videos.][GoogleYoutubeAnswer132596]


## <a name="certification-appeal-process"></a>Zertifizierungsbeschwerdeprozess

Alle Erweiterungen sollten den oben aufgeführten Store-Richtlinien entsprechen. Wenn ihre Erweiterung im Überprüfungsprozess fehlgeschlagen ist, überprüfen Sie die Store-Richtlinien, um den Grund für den Fehler zu verstehen. Navigieren Sie nach dem Übermitteln Ihrer Erweiterung über das Partner Center zu einer Frage zum Überprüfungs- oder Zertifizierungsstatus der Erweiterung, navigieren Sie zur [Neuen Supportanfrage,][MicrosoftSupportSupportrequestformE7a381be9c9aFafbEd76262bc93fd9e4] und füllen Sie das Formular aus.

### <a name="microsoft-edge-add-ons-appeal-statistics-for-fy2021"></a>Microsoft Edge Add-Ons– Statistiken zu Aufrufen für GJ2021

| Hauptbeschwerdetyp #1: Durchsetzungsbeschwerde | Hauptbeschwerdetyp #2: Zertifizierungsergebnisse | Andere Arten von Beanstandungen | Gesamtbeschwerden | Geklagte Beschwerden |
|:--- |:--- |
| 8 | 2 | 4 | 14 | 0 |


<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Festlegen der Standardrichtlinie – Inhaltssicherheitsrichtlinie \(CSP\) | Microsoft-Dokumente"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Vereinbarung für App-Entwickler | Microsoft-Dokumente"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "So identifiziert Microsoft Schadsoftware und potenziell unerwünschte Anwendungen | Microsoft-Dokumente"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Festlegen der standardmäßigen Anzeigenformate – YouTube-Hilfe"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anzeigen in eingebetteten Videos – YouTube-Hilfe"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Datenschutz für Kinder – Federal Trade Commission"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Richtlinien für die kreative Akzeptanz – Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Creative Specifications – Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

[MicrosoftSupportSupportrequestformE7a381be9c9aFafbEd76262bc93fd9e4]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Erweiterungen – Neue Supportanfrage | Microsoft-Support"