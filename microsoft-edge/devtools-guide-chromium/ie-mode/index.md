---
description: IE-Modus und die Microsoft Edge (Chromium) DevTools
title: Internet Explorer-Modus und devTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, Devtools, ie11, Internet Explorer 11, ie-Modus
ms.openlocfilehash: 070bf970c784b4f2173ebc52e4494fc6807b4a8e
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643235"
---
# <a name="internet-explorer-mode-and-the-devtools"></a>Internet Explorer-Modus und devTools  

In diesem Artikel wird beschrieben, wie der Internet Explorer-Modus \(IE-Modus\) in die Microsoft Edge \(Chromium\) DevTools integriert wird.  

## <a name="understanding-ie-mode"></a>Grundlegendes zum IE-Modus  

Im IE-Modus können Unternehmen eine Liste von Websites angeben, die nur in Internet Explorer 11 funktionieren.  Wenn Sie in Microsoft Edge \(Chromium\) zu diesen Websites navigieren, wird eine Instanz von Internet Explorer 11 ausgeführt und die Website auf einer Registerkarte gerendert.  Die Funktionalität ermöglicht Es Unternehmen, die Kompatibilität mit Technologien zu verwalten, die derzeit nicht mit modernen Webbrowsern kompatibel sind.  Unterstützung für die folgenden Technologien ist im IE-Modus enthalten.  

*   IE-Dokumentmodi  
*   ActiveX-Steuerelemente  
*   Andere Legacykomponenten  

Im IE-Modus basiert der Renderingprozess auf Internet Explorer 11.  Der Microsoft Edge \(Chromium\)-Prozess-Manager übernimmt die Lebensdauer des Renderingprozesses.  Sie ist auf die Lebensdauer der Registerkarte für eine bestimmte Website \(oder App\) beschränkt.  Wenn eine Registerkarte im IE-Modus gerendert wird, wird in der Adressleiste für die jeweilige Registerkarte ein Signal angezeigt.  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="IE-Modus-Signal in der Adressleiste" lightbox="../media/ie-mode-badge.msft.png":::
   IE-Modus-Signal in der Adressleiste  
:::image-end:::  

Der IE-Modus ist derzeit auf Windows 10 Version 1903 \(Update vom Mai 2019\) verfügbar, wird aber in Kürze für alle unterstützten Windows-Plattformen verfügbar sein.  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a>Starten der DevTools auf einer Registerkarte im IE-Modus  

Wenn Sie versuchen, den Dokumentmodus einer Website im IE-Modus anzuzeigen, wählen Sie das Signal in der Adressleiste aus.  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Anzeigen des Dokumentmodus mithilfe des IE-Modus-Badge" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   Anzeigen des Dokumentmodus mithilfe des IE-Modus-Badge  
:::image-end:::  

Wenn eine Registerkarte den IE-Modus verwendet, funktionieren die DevTools nicht, und die folgenden Bedingungen treten auf.

*   Wenn Sie `F12` `Ctrl` + `Shift` + `I` DevTools auswählen oder auswählen, wird in einer leeren Instanz des Microsoft Edge \(Chromium\) die folgende Meldung angezeigt.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   Wenn Sie ein Kontextmenü \(rechtsklick\) öffnen und **"Quelle anzeigen"** auswählen, wird Editor gestartet.  
*   Wenn Sie ein Kontextmenü \(rechtsklick\) öffnen, ist das **Inspect-Element** nicht sichtbar.  

Der Grund dafür, dass eine Reihe von Tools innerhalb der DevTools \(wie die **Netzwerk-** und **Leistungstools\)** nicht funktionieren, ist das Renderingmodul wechselt von Chromium zu Internet Explorer 11 im IE-Modus.  Um Feedback zu geben, navigieren Sie zu ["Erste Schritte mit dem Microsoft Edge DevTools-Team".](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools im IE-Modus gestartet" lightbox="../media/ie-mode-devtools.msft.png":::
   DevTools im IE-Modus gestartet  
:::image-end:::  

Führen Sie die folgenden Schritte aus, um Ihre Internet Explorer 11-basierte Website \(oder App\) im Internet Explorer 11- und IE-Modus zu testen.  

1.  Öffnen Sie Internet Explorer 11.  
    *   Suchen Sie auf Windows 10 die Verknüpfung für Internet Explorer 11.
        1.  **Startmenü**  >  **Windows Zubehör**  >  **Internet Explorer 11**.  
    *   Suchen Sie Windows 7 nach Internet Explorer 11.
        1.  **Startmenü**  >  **Internet Explorer 11**.  
1.  Öffnen Sie in Internet Explorer 11 dieselbe Webseite.  
1.  Starten Sie die Internet Explorer DevTools.  
    *   Wählen Sie `F12` .  
    *   Zeigen Sie auf eine beliebige Stelle, öffnen Sie ein Kontextmenü \(rechtsklick\), und wählen Sie **"Inspect"-Element**aus.  Weitere Informationen zur Verwendung dieser Tools finden Sie unter [Verwendung der F12-Entwicklertools.][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]  

Wenn Internet Explorer 11 nicht verfügbar ist, z. B. auf Windows 11, können Sie IEChooser verwenden, um die DevTools von Internet Explorer zu starten, um den Inhalt Ihrer IE-Modus-Registerkarten zu debuggen. Führen Sie die folgenden Schritte aus, um IEChooser zu verwenden.

1.  Öffnen Sie IEChooser.
    1. Öffnen des Dialogfelds Ausführen Drücken Sie z. B. die `Windows logo key`  +  `R` .
    2. Geben Sie `%systemroot%\system32\f12\IEChooser.exe` ein, und wählen Sie dann **OK**aus.
2.  Wählen Sie in IEChooser den Eintrag für die Registerkarte "IE-Modus" aus.


## <a name="remote-debugging-and-ie-mode"></a>Remotedebugging und IE-Modus  

Starten Sie Microsoft Edge \(Chromium\) mit aktivierten Remotedebugging über die Befehlszeilenschnittstelle.  Microsoft Visual Studio, Microsoft Visual Studio Code und andere Entwicklungstools führen in der Regel einen Befehl aus, um Microsoft Edge zu starten.  Der folgende Befehl startet Microsoft Edge, wobei der Remotedebuggingport `9222` auf .  

```shell
start msedge --remote-debugging-port=9222
```  

Nachdem Sie Microsoft Edge \(Chromium\) mit einem Befehlszeilenargument gestartet haben, ist der IE-Modus nicht mehr verfügbar.  Sie können weiterhin zu Websites \(oder Apps\) navigieren, die andernfalls im IE-Modus angezeigt werden.  Der Websiteinhalt \(oder App\) wird mit Chromium gerendert, nicht mit Internet Explorer 11.  Erwarten Sie, dass die Teile der Webseiten, die IE11 verwenden, z. B. ActiveX Steuerelemente, nicht ordnungsgemäß gerendert werden.  Der IE-Modus-Badge wird nicht in der Adressleiste angezeigt.  

Der IE-Modus bleibt nicht verfügbar, bis Sie Microsoft Edge \(Chromium\) vollständig schließen und neu starten.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Verwenden der F12-Entwicklertools | Microsoft-Dokumente"  
