---
description: Erfahren Sie, wie thePayment Request APIenables Microsoft Edge als Vermittler zwischen Händlern, Verbrauchern und Zahlungsmethoden für Verbraucher in der Cloud fungiert.
title: API für Zahlungsanforderungen – dev-Leitfaden
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 338940ab6f7e6bb04c6d5a8cc6ff0a198e7afbcc
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941853"
---
# API für Zahlungsanforderungen (EdgeHTML)  

> [!NOTE]
> In diesem Artikel wird der Workflow beschrieben, der in der [Legacy Version von Microsoft Edge][MicrosoftSupport44533505]unterstützt wird.  Microsoft Edge \ (Chrom \) unterstützt die Zahlungs Anforderungs-API mit einer anderen Implementierung basierend auf dem Chromium-Projekt.  

E-Commerce-Umsätze wachsen weiterhin rasant.  Laut [eMarketer](https://www.emarketer.com)wird der digitale Umsatz von 2018 um 23% auf die in 2013 gemessenen Werte steigen.  Während Verbraucher und Unternehmen den Vorteil von e-Commerce-Verkäufen genießen, bestehen weiterhin Herausforderungen.  Heute muss jeder e-Commerce-Websitebesitzer Zeit investieren, um qualitativ hochwertige Zahlungs Checkout-Abläufe und Gültigkeitsprüfungsregeln zu entwickeln.  Verbraucher müssen in verschiedenen Zahlungs Auszahlungs strömen navigieren und die gleichen Zahlungs-und Versandinformationen auf jeder Website, auf der Sie einkaufen, erneut eingeben.  Dies kann für die Verbraucher zeitaufwendig und frustrierend sein, was zu einer großen Anzahl von Einkaufswagen und verminderten Verkäufen für Händler führt.  Händler [schätzen](http://baymard.com/lists/cart-abandonment-rate) , dass zwischen 60% und 70% der Einkaufswagen aufgegeben werden.  

Die [Zahlungs Anforderungs-API](https://w3.org/TR/payment-request) standardisiert den Zahlungs Checkout-Prozess.  Diese API erfordert weniger benutzerdefinierte Anpassungen für Webentwickler und bietet eine schnellere, konsistentere und daher weniger verwirrende Benutzeroberfläche.  Da die Verbraucher Zahlungsinstrumente und Versandadressen von Ihrem Microsoft-Konto aus auswählen können, müssen Sie weniger Daten eingeben, um Käufe abzuschließen, wodurch die Zeit und die Dateneingabe reduziert werden, die zum Abschließen einer Zahlung erforderlich sind.  

Die [Zahlungs Anforderungs-API](https://w3.org/TR/payment-request) ist ein offener, browserübergreifender Standard, der es Browsern ermöglicht, als Vermittler zwischen Händlern, Verbrauchern und Zahlungsmethoden zu fungieren (wie Kreditkarten \), die von Verbrauchern in der Cloud gespeichert wurden.  
  
Zusammenfassend können die Kunden bei der Verwendung der [API für Zahlungsanforderungen](https://w3.org/TR/payment-request)wie gewohnt auf Händler Websites einkaufen.  Wenn Sie zur Zahlung bereit sind, ruft die Händler Website die API zur **Zahlungsanforderung** an, um eine **Zahlungsanforderung** zu erstellen, und übergibt die entsprechenden Zahlungsinformationen (wie unterstützte Zahlungsmethoden, Einkaufsbetrag, Währung usw.) an den Browser.  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Zahlungs Anforderungs Konstrukt" lightbox="../media/payment_request_construct.png":::
   Zahlungs Anforderungs Konstrukt  
:::image-end:::  

Der Browser authentifiziert den Benutzer, ermöglicht es dem Benutzer, eine unterstützte Zahlungsmethode für die Datei auszuwählen und die Zahlungsdetails zu verarbeiten.  Der Browser sendet dann die Informationen zur Zahlungsinformation zurück an die Händler-Website, damit der Händler die Zahlung abschließen kann.  Zusätzlich zum Empfang von Zahlungsinformationen kann der Händler auch beschließen, Versandinformationen im Rahmen der **Zahlungsaufforderung**zu erhalten.  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Zahlungs Anforderungs Konstrukt" lightbox="../media/payment_response_construct.png":::
   Konstrukt "Zahlungsantwort"  
:::image-end:::  

Schauen Sie sich dieses Video an, um die API zur Zahlungsanforderung in Aktion zu sehen und sich einen Überblick darüber zu verschaffen, wie Sie Sie verwenden können.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> Die API für Zahlungsanforderungen wird in Microsoft Edge Build 14992 oder höher unterstützt.  

## Erstellen einer Zahlungsanforderung  

Webseiten erstellen eine **Zahlungsanforderung** in der Regel, wenn der Benutzer einen Zahlungsvorgang initiiert, indem Sie auf die Schaltfläche "kaufen" klicken.  Der [Konstruktor](/previous-versions/mt790440(v=vs.85)) für **Zahlungsanforderungen** umfasst methodData, Details und Optionen.  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

Der [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) -Parameter enthält eine Liste der Zahlungsmethoden und Netzwerke, die von der Website akzeptiert werden, sowie alle zugehörigen Zahlungsmethoden spezifischen Daten.  In Microsoft Edge wird diese Liste mit den unterstützten Zahlungsmethoden abgeglichen, die der Käufer in seinem Microsoft-Konto gespeichert hat, und führt in der Liste "Zahlung mit" zur Zahlungsmethode.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="Zahlungs Anforderungs Konstrukt" lightbox="../media/pay_with.png":::
         Die Liste " **bezahlen mit** " in der Microsoft Wallet-Benutzeroberfläche  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var supportedInstruments = [{
          supportedMethods: ['basic-card'],
          data: {
              supportedNetworks: ['visa', 'mastercard', 'amex'],
              supportedTypes: ['credit'] 
          }         
      }]; 
      ```  
   :::column-end:::
:::row-end:::  

Der Parameter [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) enthält Informationen, die der Händler dem Kunden über die Transaktion übermitteln möchte.  Dazu zählen Bestell Zusammenfassungs Elemente wie Summe, Steuern, Versand Betrag und andere Zusammenfassungs Ebenen, die sich auf den Zahlungsbetrag auswirken.  Diese sind nicht als Auftragspositionen vorgesehen.  
  
Der Parameter [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) wird auch verwendet, um Versandoptionen zu definieren, die dem Kunden bei Bedarf zur Verfügung stehen.  Weitere Informationen finden Sie unten im Abschnitt **Zahlungsanforderung** mit Versand.  

Jede [Detail](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) Zeile enthält eine Bezeichnung für die Währung und den Betrag.  

> [!NOTE]
> Die **Zahlungsanforderung** berechnet nicht die Summe oder Summe dieser Beträge.  Es liegt in der Verantwortung der Website des Händlers, sicherzustellen, dass die Einzelposten richtig sind.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Zahlungs Anforderungs Konstrukt" lightbox="../media/show_details.png":::
         Zwischensumme, Versand, Steuern und Gesamt Details  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var details = {
          total: {
              label: 'Total (USD)',
              amount: {currency: 'USD', value: '193.98'}
          },
          displayItems: [{
                  label: 'Subtotal',
                  amount: {currency: 'USD', value: '174.99'}
              }, {
                  label: 'Taxes',
                  amount: {currency: "USD", value: '18.99'}
          }],
      };  
      ```  
   :::column-end:::
:::row-end:::  

[PaymentRequest](/previous-versions/mt790440(v=vs.85)) unterstützt keine Rückerstattungen, daher sollten die Beträge immer positiv sein; einzelne Listenelemente können negativ sein, beispielsweise Rabatte.  

Der Browser rendert die Beschriftungen, während Sie Sie definieren, und rendert automatisch die richtige Währungsformatierung basierend auf dem Gebietsschema des Kunden.  Beachten Sie, dass die Beschriftungen in der gleichen Sprache wie Ihre Inhalte gerendert werden sollen.  

Der [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) -Parameter definiert Daten, die die Webseite aus der **Zahlungsanforderung**zurückgeben möchte.  Damit werden auch die Daten definiert, die erfasst werden müssen, einschließlich, wenn Versand, e-Mail-Adresse, Telefonnummer oder alle erforderlich sind.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Zahlungs Anforderungs Konstrukt" lightbox="../media/email_snippet.png":::
         Dropdownliste "e-Mail-Adresse"  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var options =
          {
              requestPayerEmail: true
          }; 
      ```  
   :::column-end:::
:::row-end:::  

## Zahlungsanforderung anzeigen  

Die [Show ()](/previous-versions/mt790448(v=vs.85)) -Methode wird von der Webseite aufgerufen, um dem Benutzer die Interaktion mit der Benutzeroberfläche der **Zahlungsanforderung** zu ermöglichen.  Die [Show ()](/previous-versions/mt790448(v=vs.85)) -Methode gibt eine Versprechung zurück, die aufgelöst wird, wenn der Benutzer die Zahlungsanforderung autorisiert.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Zahlungs Anforderungs Konstrukt" lightbox="../media/pay_screen_default.png":::
         Details bestätigen und bezahlen  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      paymentRequest.show().then(paymentInstrumentResponse => {
          paymentInstrumentResponse.complete('success').then().catch(error => {
              handlePaymentRequestError(error); 
      });
      ```  
   :::column-end:::
:::row-end:::  

## Abbrechen einer Zahlungsanforderung  
 
Die [Abort ()](/previous-versions/mt790437(v=vs.85)) -Methode kann von der Webseite zu einem beliebigen Zeitpunkt aufgerufen werden, nachdem die [Show ()](/previous-versions/mt790448(v=vs.85)) -Methode aufgerufen wurde, bis zu dem Punkt, an dem die Verheißung aufgelöst wurde.  Die [Abort ()](/previous-versions/mt790437(v=vs.85)) -Methode führt dazu, dass der Browser die **Zahlungsanforderung** abbricht und die Benutzeroberfläche für die **Zahlungsanforderung** schließt.  So kann beispielsweise eine Webseite abgebrochen werden, wenn der Benutzer die Transaktion nicht im erforderlichen Zeitraum abgeschlossen hat.  

```javascript
payment.abort();
```  

## Zahlungsantwort  
Wenn der Kunde die **Zahlungsanforderung**genehmigt, wird eine **Zahlungsantwort** an die Website zurückgegeben.  Die **Zahlungsantwort** enthält Folgendes:  

 Eigenschaft      | Beschreibung | Erforderlich | Zusätzliche Infos
|---------------|-----------------|-------|-----------------|
[MethodName](/previous-versions/mt790656(v=vs.85)) | Die ID für die vom Benutzer ausgewählte Zahlungsmethode | Y | |   
[details](/previous-versions/mt790655(v=vs.85)) | Ein JSON-Objekt, das alle Daten enthält, die der Händler benötigt, um die Transaktion mit der ausgewählten Zahlungsmethode oder einem Zahlungs Token zu verarbeiten | Y | [Standardkarte](https://w3c.github.io/payment-method-basic-card) Dictionary: Karten Inhabername; cardNumber expiryMonth; expiryYear; cardSecurityCode; billingAddress; |   
["shippingaddress"](/previous-versions/mt790445(v=vs.85)) | Die vom Benutzer ausgewählte Versandadresse  |  Optional.  Erforderlich, wenn [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) ist `True`  | Adressverzeichnis: Land; addressLine Region Stadt dependentLocality; PostalCode sortingCode; languageCode Organisation Empfänger Telefon |  
[shippingOption](/previous-versions/mt790446(v=vs.85)) | Die ID für die ausgewählte Versandoption | Optional.  Erforderlich, wenn [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) ist `True`  | |   
[payername](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Der vom Benutzer angegebene Name  | Optional.  Erforderlich, wenn [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) ist `True` | |  
[payerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Die vom Benutzer ausgewählte e-Mail-Adresse | Optional.  Erforderlich, wenn [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) ist `True`  | |  
[PayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Die vom Benutzer ausgewählte Telefonnummer | Optional.  Erforderlich, wenn [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) ist `True` | |  

Das JSON-Objekt " [Details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) " in der **Zahlungsantwort** enthält die Zahlungsdaten, die vom Händler zur Abwicklung einer Zahlung benötigt werden.  In ihrer einfachsten Form wird die Antwort eine [einfache Karten](https://w3c.github.io/payment-method-basic-card) Nutzlast mit Klartext-Zahlungskarten Details sein.  Wenn Händler über Vereinbarungen mit zusätzlichen Gateway/Prozessor-Partnern verfügen, um Zahlungen zu unterstützen, kann der Händler eine Nutzlast anfordern, die der Prozessor verarbeiten kann.  Diese können die Form eines Prozessor/Gateway-Tokens oder eines verschlüsselten Zahlungsinstruments annehmen.  Diese Zahlungsmethoden liegen außerhalb des Anwendungsbereichs dieses Dokuments und werden in der für den prozessorspezifischen Dokumentation behandelt.  Darüber hinaus ist für den Entwickler keine zusätzliche Onboarding-Lösung erforderlich, um eine [einfache Karten](https://w3c.github.io/payment-method-basic-card) Antwort zu erhalten, im Gegensatz zu anderen Prozessor/Gateway-spezifischen Zahlungsmethoden, die möglicherweise eine Onboarding-Verschlüsselung oder eine Autorisierung anfordern \ (oAuth \).  

Nach Eingang der **Zahlungsantwort**übermittelt die Website die Zahlungsinformationen an Ihren Zahlungsprozessor.  Der Browser zeigt eine Drehfeld-Seite an, während die Zahlung verarbeitet wird.  

:::image type="complex" source="../media/loading_screen.png" alt-text="Zahlungs Anforderungs Konstrukt" lightbox="../media/loading_screen.png":::
   Die Seite, die angezeigt wird, wenn die Zahlung verarbeitet wird  
:::image-end:::  

Nach Abschluss der Zahlung Ruft die Webseite die [vollständige ()](/previous-versions/mt790642(v=vs.85)) -Methode auf und übergibt den Wert **Success** oder **Fail**.  Mit der [Complete ()](/previous-versions/mt790642(v=vs.85)) -Methode wird der Browser darüber informiert, dass der Kauf abgeschlossen ist, und der entsprechende abschließende UI-Bildschirm sollte je nach dem Wert von **Success** oder **Fail**angezeigt werden.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="Zahlungs Anforderungs Konstrukt" lightbox="../media/response_payment-request_complete.png":::
         Die beim erfolgreichen Kauf angezeigte Benutzeroberfläche  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="Zahlungs Anforderungs Konstrukt" lightbox="../media/response_payment-request_failure.png":::
         Die Benutzeroberfläche, die beim Kauf nicht angezeigt wird  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Zahlungsanforderung mit Versand  

### Lieferadresse  

Für Verkäufe, die den Versand physischer waren erfordern, ist eine Lieferadresse erforderlich.  Wenn Sie eine Lieferadresse angeben möchten, legen Sie `requestShipping = True` die Optionen in den [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) -Parameter der Anforderung.  

Wenn der Benutzer die Versandadresse auswählt oder aktualisiert, wird das [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) -Ereignis ausgeführt.  Die Website mit einem Ereignislistener ist sich der Änderung bewusst und kann dann die Adresse überprüfen, die Versandkosten und Steuern neu berechnen sowie [Versand](/previous-versions/mt790440(v=vs.85)) Optionen aktualisieren, um die geänderten Kosten und Versandoptionen anzuzeigen, die für die ausgewählte Adresse verfügbar sind \ (falls zutreffend).  

### Versandoptionen  

Versandoptionen können dem Kunden angezeigt werden, indem dem [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) -Parameter [shippingoptions](/previous-versions/mt790440(v=vs.85)) hinzugefügt werden.  Eine Standardeinstellung kann festgelegt werden, indem eine der Versandoptionen festgelegt wird `selected = True` .  
 
Wenn der Benutzer die Versandarten auswählt oder aktualisiert, wird das [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) -Ereignis ausgeführt.  Die Website mit einem Ereignis-Listener ist sich der Änderung bewusst und kann den Parameter [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) mit dem korrekten Versand Betrag aktualisieren.  

```javascript
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
         label: 'Subtotal',
         amount: {currency: 'USD', value: '174.99'}
        }, {
            label: 'Shipping',
            amount: {currency: 'USD', value: '0.00'}
        }, {
            label: 'Taxes',
            amount: {currency: "USD", '18.99'}
    }],
    shippingOptions: [{
        id: 'STANDARD',
        label: 'Standard – FREE (5-6 Business days)',
        amount: {currency: 'USD', value: '0.00'},
        selected: true
    }, {
        id: 'EXPEDITED',
        label: 'Two-Day Shipping',
        amount: {currency: 'USD', value: '7.00'}
    }]
};
        
var options = {
    requestShipping: true,
    requestPayerEmail: true
}; 
```  

## API-Referenz  

[Payments Request-API](/previous-versions/mt790447(v=vs.85))  

## Spezifikation
[Payments Request-API](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "Was ist Microsoft Edge Legacy?"  
