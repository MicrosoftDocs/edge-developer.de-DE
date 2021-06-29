---
description: Eine Referenz zu WebDriver-Funktionen und Microsoft Edge-spezifischen Optionen, die von EdgeDriver (Chromium) unterstützt werden.
title: Funktionen und EdgeOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, HTML, CSS, Javascript, Entwickler, WebDriver, Selenium, Tests, Tools, Automatisierung, Test
ms.openlocfilehash: 33b9d53b72a16a9c02a03a43679137d25de0025f
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624766"
---
# <a name="capabilities-and-edgeoptions"></a>Funktionen und EdgeOptions  

Funktionen sind Optionen, die Sie zum Anpassen und Konfigurieren einer Sitzung verwenden `EdgeDriver` können.  Um mehr über das Starten einer neuen `EdgeDriver` Sitzung zu erfahren, navigieren Sie zu [Automating Microsoft Edge][WebdriverIndexAutomateMicrosoftEdgeChromium].  In diesem Artikel werden alle unterstützten Funktionen für [Microsoft Edge][WebdriverIndexInstallMicrosoftEdgeChromium] und Details zum Übergeben der Funktionen an `EdgeDriver` Sitzungen beschrieben.  

Funktionen werden als JSON-Karte an eine WebDriver-Sitzung übergeben.  Ein WebDriver-Testframework stellt eine WebDriver-Sprachbindung bereit.  WebDriver-Sprachbindungen bieten in der Regel typsichere Komfortmethoden, sodass Sie die JSON-Karte nicht selbst konfigurieren müssen.  Unterschiedliche WebDriver-Sprachbindungen verwenden unterschiedliche Mechanismen zum Konfigurieren von Funktionen.  [Selenium][SeleniumMain] konfiguriert Funktionen über die `EdgeOptions` Klasse.

Weitere Informationen zum Konfigurieren von Funktionen finden Sie in der Dokumentation zu Ihrem bevorzugten WebDriver-Testframework.  Navigieren Sie für weitere Informationen zu ["WebDriver-Testframework auswählen".][WebdriverIndexChooseAWebdriverTestingFramework]

## <a name="using-the-edgeoptions-class"></a>Verwenden der EdgeOptions-Klasse  

Erstellen Sie eine Instanz von `EdgeOptions` , die Komfortmethoden zum Festlegen Microsoft Edge-spezifischen Funktionen bereitstellt.  Übergeben Sie das Objekt nach dem Konfigurieren `EdgeOptions` `EdgeOptions` an den `EdgeDriver` Konstruktor.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Verwenden Sie die Methode, um Funktionen zu verwenden, die nicht über eine zugehörige `AddAdditionalCapability` Komfortmethode verfügen.  Sie müssen den vollständigen Namen der Funktion und einen Wert mit dem richtigen Typ übergeben.  Navigieren Sie zum [EdgeOptions -Objekt,](#edgeoptions-object)um die vollständige Liste der akzeptierten Funktionen und Werttypen zu überprüfen.  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

## <a name="recognized-capabilities"></a>Erkannte Funktionen  

Für Standardfunktionen, die `EdgeDriver` dies akzeptieren, navigieren Sie zur [Selenium-Dokumentation][SharedCapabilitiesSeleniumDocumentation] und zum [W3C WebDriver-Standard.][CapabilitiesW3cWebdriver]  In diesem Artikel werden nur funktionen aufgeführt, die für Microsoft Edge spezifisch sind.  

## <a name="edgeoptions-object"></a>EdgeOptions-Objekt  

Die meisten Microsoft Edge-spezifischen Funktionen werden über das Objekt verfügbar `EdgeOptions` gemacht.  In einigen Sprachen werden die Funktionen von der `EdgeOptions` Klasse implementiert.  In anderen Sprachen werden die Funktionen unter dem `ms:edgeOptions` Wörterbuch in `DesiredCapabilities` gespeichert.  

| Funktion | Typ | Standardwert | Details |  
|:--- |:--- |:--- |:--- |  
| Args | Liste der Zeichenfolgen |  | Liste der Befehlszeilenargumente, die beim Starten Microsoft Edge verwendet werden sollen.  Argumente mit einem zugeordneten Wert sollten durch ein `=` Vorzeichen \(z. `['start-maximized', 'user-data-dir=/tmp/temp_profile']` B. \) getrennt werden. |  
| Binäre | string |  | Der Pfad zu der Microsoft Edge Binärdatei, die \(unter macOS) verwendet werden soll, sollte der Pfad die tatsächliche Binärdatei sein, nicht nur die App.  z. B. `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \). |  
| debuggerAddress | string |  | Eine Adresse eines Debuggerservers, mit dem eine Verbindung hergestellt werden soll, `hostname/ip:port` z. B. in Form von `127.0.0.1:38947` . |
| Trennen | boolean | `false` | Wenn `false` , wird Microsoft Edge beendet, wenn der WebDriver-Dienst heruntergefahren wird, auch wenn das lokale WebDriver-Ende die Sitzung nicht geschlossen hat.  Wenn `true` , wird Microsoft Edge nur beendet, wenn das lokale WebDriver-Ende die Sitzung schließt.  Wenn `true` und das lokale WebDriver-Ende die Sitzung nicht schließt, wird der temporäre `EdgeDriver` Benutzerdatenordner, der von der Microsoft Edge Instanz verwendet wird, nicht bereinigt. |  
| excludeSwitches | Liste der Zeichenfolgen |  | Liste der Microsoft Edge Befehlszeilenoptionen, um auszuschließen, dass EdgeDriver beim Starten Microsoft Edge standardmäßig besteht.  Vermeiden Sie das `--` Präfix für Schalter. |  
| Erweiterungen | Liste der Zeichenfolgen |  | Eine Liste der Erweiterungen, die beim Start installiert werden sollen.  Jedes Element in der Liste sollte eine base64-codierte gepackte Erweiterung \( `.crx` \) sein. |  
| localState | dictionary |  | Ein Wörterbuch mit jedem Eintrag, der aus dem Namen der Einstellung und dem Wert besteht.  Die Einstellungen werden auf die Datei "Lokaler Zustand" im Benutzerdatenordner angewendet. |  
| minidumpPath | string |  | Verzeichnis zum Speichern Microsoft Edge Minidumps.  \(Wird nur unter Linux unterstützt.\) |  
| mobileEmulation | dictionary |  | Ein Wörterbuch mit einem Wert für `deviceName` , oder Werte für und `deviceMetrics` `userAgent` . |  
| perfLoggingPrefs | dictionary |  | Ein optionales Wörterbuch, das Einstellungen für die Leistungsprotokollierung angibt.  Navigieren Sie für weitere Informationen zum [perfLoggingPrefs-Objekt.](#perfloggingprefs-object) |  
| Prefs | dictionary |  | Ein Wörterbuch mit jedem Eintrag, der aus dem Namen der Einstellung und dem Wert besteht.  Die Einstellungen werden nur auf das verwendete Benutzerprofil angewendet.  For examples, navigate to the `Preferences` file in the user data folder of Microsoft Edge. |  
| wdpAddress | string |  | Eine Adresse eines Windows Device Portal-Servers, mit dem Sie eine Verbindung herstellen, `hostname/ip:port` z. B. in Form von `127.0.0.1:50080` .  Navigieren Sie zu [Remotedebugging – Windows 10 Geräten,][DevtoolsRemoteDebuggingWindows]um weitere Informationen zu erfahren. |  
| wdpPassword | string |  | Optionales Kennwort, das beim Herstellen einer Verbindung mit einem Windows Device Portal-Server verwendet werden soll.  Erforderlich, wenn die Authentifizierung auf dem Server aktiviert ist. |  
| wdpUsername | string |  | Optionaler Benutzername, der beim Herstellen einer Verbindung mit einem Windows Device Portal-Server verwendet werden soll.  Erforderlich, wenn die Authentifizierung auf dem Server aktiviert ist. |  
| windowsApp | string |  | Anwendungsbenutzermodell-ID eines zu startenden Microsoft Edge-App-Pakets, `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` z. B. .  Anstatt `windowsApp` beim Herstellen einer Verbindung mit einem Windows 10X Gerät oder Emulator mit Windows Device Portal zu `binary` verwenden. |  
| windowTypes | Liste der Zeichenfolgen |  | Eine Liste der Fenstertypen, die in der Liste der Fensterhandles angezeigt werden.  Fügen Sie für den Zugriff auf Android-Webview-Elemente `webview` die Liste hinzu. |  

## <a name="perfloggingprefs-object"></a>perfLoggingPrefs-Objekt  

Das `perfLoggingPrefs` Wörterbuch hat das folgende Format \(alle Schlüssel sind optional\).  

| Key | Typ | Standardwert | Details |  
|:--- |:--- |:--- |:--- |  
| bufferUsageReportingInterval | Positive ganze Zahl | 1000 | Die angeforderte Anzahl von Millisekunden zwischen DevTools-Ablaufverfolgungspuffer-Verwendungsereignissen.  Wenn z. B. 1000, dann einmal pro Sekunde, meldet DevTools, wie voll der Ablaufverfolgungspuffer ist.  Wenn ein Bericht angibt, dass die Puffernutzung 100 % beträgt, wird eine Warnung ausgegeben. |  
| enableNetwork | boolean | true | Zum Sammeln von \(oder nicht sammeln\)-Ereignissen aus der Netzwerkdomäne. |  
| enablePage | boolean | true | Zum Sammeln von \(oder nicht sammeln\)-Ereignissen aus der Page-Domäne. |  
| traceCategories | string | \(leer\) | Eine durch Trennzeichen getrennte Zeichenfolge Microsoft Edge Ablaufverfolgungskategorien, für die Ablaufverfolgungsereignisse erfasst werden sollen.  Eine nicht angegebene oder leere Zeichenfolge deaktiviert die Ablaufverfolgung. |  

## <a name="returned-capabilities"></a>Zurückgegebene Funktionen  

Die folgende Liste enthält alle Microsoft Edge-spezifischen Funktionen, die `EdgeDriver` beim Erstellen einer neuen Sitzung zurückgegeben werden.  

| Funktion | Typ | Details |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | string | Die Version von EdgeDriver. |  
| msedge.userDataDir | string | Der Pfad zum Benutzerdatenordner, der von der Microsoft Edge Instanz verwendet wird. |  

<!-- links -->  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Erste Schritte mit Remotedebugging Windows 10 Geräten | Microsoft-Dokumente"  
[WebdriverIndexChooseAWebdriverTestingFramework]: ./index.md#choose-a-webdriver-testing-framework "Auswählen eines WebDriver-Testframeworks – Verwenden von WebDriver (Chromium) für die Testautomatisierung | Microsoft-Dokumente"
[WebdriverIndexAutomateMicrosoftEdgeChromium]: ./index.md#automate-microsoft-edge-chromium "Automate Microsoft Edge (Chromium) – WebDriver (Chromium) | Microsoft-Dokumente"    
[WebdriverIndexInstallMicrosoftEdgeChromium]: ./index.md#install-microsoft-edge-chromium "Installieren von Microsoft Edge (Chromium) – WebDriver (Chromium) | Microsoft-Dokumente"  
<!-- external links -->
[SeleniumMain]: https://www.selenium.dev "SeleniumHQ-Browserautomatisierung"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Gemeinsam genutzte Funktionen | Selenium-Dokumentation"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver#capabilities "Funktionen – WebDriver-Spezifikation | W3c"   
