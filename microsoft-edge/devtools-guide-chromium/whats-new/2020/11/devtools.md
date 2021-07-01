---
description: Microsoft Edge unter Linux, verbesserte Webhint-Tipps im Probleme-Tool, neue Features für das Service Worker-Debugging und vieles mehr.
title: Neuerungen in DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.localizationpriority: high
ms.openlocfilehash: e5706de4c7938a3cb2246aa34de07c73dafe5776
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624773"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-88"></a>Neuerungen in DevTools (Microsoft Edge 88)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="microsoft-edge-and-microsoft-edge-driver-now-available-on-linux"></a>Microsoft Edge und Microsoft Edge-Treiber jetzt unter Linux verfügbar  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

Microsoft Edge Dev wird nun von Ubuntu-, Debian-, Fedora- und openSUSE-Distributionen unterstützt.  Laden Sie das Microsoft Edge Dev `.deb`- oder `.rpm`-Paket direkt von der [Microsoft Edge Insider-Website][MicrosoftinsiderDownloadPlatformLinux] herunter und installieren Sie es, oder verwenden Sie die standardmäßigen Paketverwaltungstools Ihrer Linux-Distribution.  

Wenn Sie eine Linux-Umgebung in Ihren Continuous Integration und Continuous Delivery \(CI/CD\)-Lösungen verwenden, ist Microsoft Edge Driver auch unter Linux verfügbar.  Wenn Sie mit der Automatisierung von Microsoft Edge Dev mit Microsoft Edge Driver beginnen möchten, navigieren Sie zur [Downloadseite für Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].  Hilfe zur Automatisierung von Microsoft Edge Dev zusammen mit Microsoft Edge Driver finden Sie unter [Verwenden von WebDriver (Chromium) für die Testautomatisierung][WebdriverChromiumMain].  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools in Microsoft Edge unter Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   DevTools in Microsoft Edge unter Linux  
:::image-end:::  

## <a name="improved-webhint-and-platform-tips-in-the-issues-tool"></a>Verbesserte Webhint- und Plattformtipps im Probleme-Tool  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

Ein Open-Source-Tool, [Webhint][WebhintMain], bietet Echtzeitfeedback für Websites und lokale Webseiten.  Überprüfen Sie ab [Microsoft Edge Version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel] das Webhint-Feedback im [Issues][DevtoolsIssuesIndex]-Tool.  Probleme, die im **Probleme**-Tool angezeigt werden, sind jetzt mit den folgenden, neu hinzugefügten Kategorien leichter zu überprüfen.  

*   [Barrierefreiheit][WebhintUserGuideHintsAccessibility]  
*   [Kompatibilität][WebhintUserGuideHintsCompatibility]  
*   [Leistung][WebhintUserGuideHintsPerformance]  
*   [Fallstricke][WebhintUserGuideHintsPitfalls]  
*   [PWA][WebhintUserGuideHintsPwa]  
*   [Sicherheit][WebhintUserGuideHintsSecurity]  
    
Sie können jetzt die Probleme von Drittanbietern mithilfe eines neuen Kontrollkästchens herausfiltern.  Die Filterfunktionalität hilft Ihnen, Probleme im Zusammenhang mit Code aus Drittanbieterbibliotheken oder anderen Quellen auszublenden.  

Zur leichteren Überprüfung der von [webhint][WebhintMain] aufgedeckten Probleme werden im **Probleme**-Tool nun die folgenden Informationen angezeigt.  

*   Verbesserte Codeausschnitte.  
*   Links zu anderen relevanten Panels.  
*   Links zur Dokumentation, die Ihnen bei der Behebung von Problemen in Ihrer Website helfen.  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Probleme-Tool" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   **Probleme**-Tool  
:::image-end:::  

## <a name="composited-layers-are-now-in-3d-view"></a>Zusammengesetzte Ebenen werden jetzt in der 3D-Ansicht dargestellt  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Sie können nun Inhalte von **Ebenen** neben Z-Indexwerten und dem Dokumentobjektmodell \(DOM\) visualisieren.  Mit diesem Feature können Sie Debuggen, ohne zwischen den Tools [3D-Ansicht][Devtools3dViewIndex] und **Ebenen** umzuschalten.  Für ein umfassendes visuelles Debugging werden jetzt [die 3D-Ansicht und die zusammengesetzten Ebenen kombiniert][Devtools3dViewIndex].  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Bereich Zusammengesetzte Ebenen" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   Bereich **Zusammengesetzte Ebenen**  
:::image-end:::  

## <a name="css-variable-definitions-in-styles-pane"></a>CSS-Variablendefinitionen im Bereich „Stile“  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

Im Bereich **Stile** werden die [CSS-Variablen][MdnUsingCssCustomProperties] nun direkt mit jeder Definition verknüpft.  Wählen Sie eine Variable aus, um die Definition der CSS-Variablen einfach anzuzeigen oder zu ändern.  Im Beispiel zeigt DevTools die CSS-Attribute für das `body`-Element an.  Führen Sie die folgenden Aktionen aus, um die Variablendefinition für die CSS-Variable `--theme-body-background` anzuzeigen.  

1.  Wählen Sie im Bereich **Stile** `var(--theme-body-background)` aus.  
1.  Im Bereich **Stile** wird nun die Definition der CSS-Variablen `--theme-body-background` angezeigt.  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Mit dem Stil verknüpfte CSS-Variable" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         Mit dem Stil verknüpfte CSS-Variable  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Mit dem Stilziel verknüpfte CSS-Variable" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         Mit dem Stilziel verknüpfte CSS-Variable  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="service-worker-debugging-improvements"></a>Verbesserungen beim Service Worker-Debugging  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

Die folgenden neuen Features in den Tools [Netzwerk](#network-tool), [Anwendung](#application-tool) und [Quellen](#sources-tool) unterstützen Sie beim Erstellen Ihrer [PWA][ProgressiveWebAppsIndex].  Verwenden Sie die folgenden Features, wenn Probleme beim Debuggen Ihrer Service Worker auftreten.  

Das Routing von Anforderungen zeigt die `startup`- und `fetch`-Ereignisse basierend auf den Netzwerkanforderungen an, die von Service Workern ausgeführt werden.  Der Zugriff auf die Zeitpläne erfolgt entweder über das **Anwendung**- oder das **Netzwerk**-Tool.  Die Zeitpläne helfen, wenn Sie Probleme mit Service Workers haben und anzeigen möchten, ob etwas mit dem Ereignis `startup` oder `fetch` nicht stimmt.  

### <a name="application-tool"></a>Anwendung-Tool  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

Zeigen Sie mit dem neuen Link **Netzwerkanforderungen** alle Routinginformationen für Service Worker-Anforderungen an.  Führen Sie die folgenden Aktionen aus, um beim Debuggen des Service Workers zusätzlichen Kontext anzuzeigen.  

1.  Navigieren Sie zu **Anwendung** > **Service Workers**.  
1.  Wählen Sie **Netzwerkanforderungen** aus.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Öffnen des Netzwerk-Tools im Bereich Service Workers" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       Öffnen des **Netzwerk**-Tools im Bereich **Service Workers**
    :::image-end:::  
    
1.  Das **Netzwerk**-Tool wird in der **Schublade** geöffnet und zeigt alle Netzwerkanforderungen für Service Worker an.  Die Netzwerkanforderungen werden mithilfe von `is:service-worker-intercepted` gefiltert.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Netzwerk-Tool in der Schublade" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       **Netzwerk**-Tool in der **Schublade**  
    :::image-end:::
    
1. Wenn Sie das **Netzwerk**-Tool wieder in den oberen Bereich verschieben möchten, schließen Sie die **Schublade**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Schließen der Schublade, um das Network-Tool zurückzugeben" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       Schließen der **Schublade**, um das **Netzwerk**-Tool zurückzugeben  
    :::image-end:::  
    
### <a name="network-tool"></a>Network-Tool  

Debuggen Sie Netzwerkanforderungen, die über Service Worker ausgeführt werden.  Sie können Netzwerkanforderungen auch über das **Anwendung**-Tool öffnen.  DevTools zeigen für jede Anforderung die folgenden Informationen im [Timing] [DevtoolsNetworkReferenceDisplayTimingBreakdownRequest]-Bereich an.  

*   Der Anfang einer Anforderung und die Dauer des Bootstrap.  
*   Änderungen an der Service Worker-Registrierung.  
*   Die Laufzeit eines `fetch`-Ereignishandlers.  
*   Die Laufzeit aller `fetch`-Ereignisse zum Laden eines Clients.  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Bereich Timing" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   Bereich **Timing**  
:::image-end:::  

### <a name="sources-tool"></a>Quellen-Tool  

In früheren Versionen von Microsoft Edge war die Tiefe im Aufrufstapel auf den JavaScript-Code in Ihrem Service Worker beschränkt.  In Microsoft Edge 88 zeigt der Aufrufstapel nun den Initiator von Anforderungen an, die über Ihren Service Worker ausgeführt werden.  

Zum Auffinden des Initiators der Anforderung verwenden Sie den Aufrufstapel Ihres JavaScript-Codes im Service Worker.  Der Aufrufstapel in den folgenden Abbildungen beginnt mit dem JavaScript-Code in Ihrem Service Worker und zeigt einen Verweis auf die ursprüngliche Webseitenanforderung als `(index):157` an.  In der zweiten Abbildung wurde der Verweis ausgewählt und hat den Initiator geöffnet, der die Anforderung gestellt hat.  Der Initiator in der zweiten Abbildung ist die Webseite.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Datei service-worker.js und Aufrufstapel mit Hervorhebung des Ursprungs der Anforderung" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         Datei `service-worker.js` und Aufrufstapel mit Hervorhebung des Ursprungs der Anforderung  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="Die (Index-)Webseite ist der Anforderungsinitiator" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         Die Webseite `(index)` ist der Initiator der Anforderung  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="copy-property-value-of-a-network-request"></a>Kopieren des Eigenschaftswerts einer Netzwerkanforderung  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

Im Tool **Netzwerk** können Sie den Eigenschaftswert einer Netzwerkanforderung mit der neuen Option **Wert kopieren** kopieren.  Der Eigenschaftswert wird als decodierter JSON-Wert kopiert.  In früheren Versionen von Microsoft Edge mussten Sie einen Wert mithilfe einer der folgenden Aktionen kopieren.  

*   Hervorheben des gesamten Texts und Kopieren.  
*   Speichern des Werts als globale Variable (sofern zutreffend) und Kopieren des Werts in der DevTools-[Konsole][DevtoolsConsoleIndex].  
    
Navigieren Sie zum Kopieren des Eigenschaftswerts in die Zwischenablage zu [Formatierte Antwort JSON in die Zwischenablage kopieren][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].  Navigieren Sie zu Problem [1132084][CR1132084], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Kopieren eines Eigenschaftswerts in DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         Kopieren eines Eigenschaftswerts in DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Einfügen eines Eigenschaftswerts in Microsoft Visual Studio Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         Einfügen eines Eigenschaftswerts in Microsoft Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="customize-multi-press-keyboard-shortcuts"></a>Anpassen von mehrfach gedrückten Tastenkombinationen  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

[Seit Microsoft Edge, Version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], können Sie Tastenkombinationen für jede Aktion in DevTools anpassen.  In Microsoft Edge, Version 88, können Sie jetzt Multipress-Tastenkombinationen erstellen.  Wenn Sie eine Tastenkombination für eine Aktion in DevTools festlegen möchten, navigieren Sie zu [Einstellungen][DevtoolsCustomizeIndexSettings] > **Experimente**, und aktivieren Sie das Kontrollkästchen neben **Tastenkombinations-Editor aktivieren**.  Weitere Informationen zum Anpassen und Bearbeiten von Verknüpfungen finden Sie unter [Bearbeiten von Tastenkombinationen für alle Aktionen in devTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].  

Die rote Markierung zeigt beispielsweise eine angepasste Multipress-Tastenkombination für die Aktion **Aufzeichnen von Ereignissen starten** an.  Navigieren Sie zu [Problem #174309][CR174309], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Akkord-Tastenkombinationen" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   Multipress-Tastenkombinationen  
:::image-end:::  

## <a name="devtools-now-match-browser-language"></a>DevTools-Sprache entspricht nun der Browsersprache  

Wenn Sie in Microsoft Edge, Version 87, in den [DevTools-Einstellungen][DevtoolsCustomizeIndexSettings] die Einstellung **Übereinstimmung mit der Browser-Sprache** aktiviert haben, entsprach die Sprache von DevTools nicht der Browsersprache.  In Microsoft Edge, Version 88, entspricht DevTools nun der Browsersprache, wenn Sie die Einstellung **Übereinstimmung mit der Browsersprache** aktivieren.  Weitere Informationen zur DevTools-Einstellung **Übereinstimmung mit der Browsersprache** erhalten Sie, wenn Sie zu [Ändern der DevTools-Spracheinstellungen][DevtoolsCustomizeLocalization] navigieren.  

:::image type="complex" source="../../media/2020/11/startpage-devtools-settings-japanese.msft.png" alt-text="DevTools-Einstellung Übereinstimmung mit der Browsersprache in Japanisch" lightbox="../../media/2020/11/startpage-devtools-settings-japanese.msft.png":::
   DevTools-Einstellung **Übereinstimmung mit der Browsersprache** in Japanisch  
:::image-end:::  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-css-angle-visualization-tools"></a>Neue Visualisierungstools für CSS-Winkel  

DevTools unterstützt jetzt das Debuggen von CSS-Winkeln besser.  Wenn auf ein HTML-Element auf Ihrer Seite ein CSS-Winkel angewendet wurde, wird neben dem Winkel im **Stile**-Tool ein Uhrensymbol angezeigt.  Wenn Sie die Uhr-Überlagerung ein-/ausschalten möchten, wählen Sie das Uhrensymbol aus.  Wenn Sie den Winkel ändern möchten, wählen Sie eine beliebige Stelle in der Uhr aus, oder ziehen Sie am Zeiger.  Zum Ändern des Winkelwerts können Sie auch Mausverfahren und Tastenkombinationen verwenden.  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  Navigieren Sie zu den Problemen [1126178][CR1126178] und [1138633][CR1138633], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.  

<!--todo:  add link when css angle clock section exists.  -->  

Für das Beispiel wird der folgende CSS-Winkel verwendet.  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="CSS-Winkel" lightbox="../../media/2020/11/css-angle.msft.png":::
   CSS-Winkel  
:::image-end:::  

### <a name="simulate-storage-quota-size-in-the-storage-pane"></a>Simulieren der Speicherkontingentgröße im Speicherbereich  

Sie können jetzt die Größe des Speicherkontingents im Bereich **Speicher** außer Kraft setzen.  Dieses Feature ermöglicht es Ihnen, verschiedene Geräte zu simulieren und das Verhalten Ihrer Website oder App in Szenarien mit wenig verfügbarem Speicherplatz zu testen.  Führen Sie die folgenden Aktionen aus, um das Speicherkontingent zu simulieren.  

1.  Navigieren Sie zu **Anwendung** > **Speicher**.  
1.  Aktivieren Sie das Kontrollkästchen **Benutzerdefiniertes Speicherkontingent simulieren**.  
1.  Geben Sie eine gültige Zahl ein.  
    
Weitere Informationen zum Emulieren von mobilen Geräten und anderen Features in DevTools finden Sie unter [Emulieren von mobilen Geräten in Microsoft Edge DevTools][DevtoolsDeviceModeIndex].  Navigieren Sie zu den Problemen [945786][CR945786] und [1146985][CR1146985], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simulieren der Speicherkontingentgröße" lightbox="../../media/2020/11/storage-quota.msft.png":::
   Simulieren der Speicherkontingentgröße  
:::image-end:::  

### <a name="report-cors-errors-in-the-network-tool"></a>Melden von CORS-Fehlern im Netzwerk-Tool  

Testen Sie dieses Feature, indem Sie zur [CORS-Fehlerdemo][GlitchCorsErrors] navigieren.  Öffnen Sie das Tool **Netzwerk**, aktualisieren Sie die Seite, und beobachten Sie die fehlerhafte CORS-Netzwerkanforderung.  In der Statusspalte wird der **CORS-Fehler** angezeigt.  Wenn Sie auf den Fehler zeigen, wird in der QuickInfo nun der Fehlercode angezeigt.  In Microsoft Edge, Version 87 und früheren Versionen, hat DevTools nur den generischen **(failed)**-Status für CORS-Fehler angezeigt.  Navigieren Sie zu Problem [1141824][CR1141824], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="CORS-Fehler" lightbox="../../media/2020/11/cors-err.msft.png":::
   CORS-Fehler  
:::image-end:::  

### <a name="frame-details-view-updates"></a>Updates der Frame-Detailansicht  

#### <a name="cross-origin-isolation-information-in-the-frame-details-view"></a>Informationen zur ursprungsübergreifenden Isolierung in der Frame-Detailansicht  

Der Status ursprungsübergreifend isoliert (cross-origin isolated) wird nun unter dem Abschnitt **Sicherheit & Isolierung** angezeigt.  Der neue Abschnitt **API-Verfügbarkeit** zeigt die Verfügbarkeit von `SharedArrayBuffer`s \(SAB\) und ob die Puffer mit `postMessage()` freigegeben werden können.  Eine Warnung „veraltet“ wird angezeigt, wenn der SAB und `postMessage()` derzeit verfügbar sind, der Kontext aber nicht ursprungsübergreifend isoliert ist.  Weitere Informationen zur ursprungsübergreifenden Isolierung und warum sie für Features wie `SharedArrayBuffers` erforderlich ist, finden Sie unter [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].  Navigieren Sie zu Problem [1139899][CR1139899], um Echtzeitupdates dieser Funktion im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informationen über einen anderen Ursprung" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   Informationen über einen anderen Ursprung  
:::image-end:::  

#### <a name="new-web-workers-information-in-the-frame-details-view"></a>Neue Web-Worker-Informationen in der Frame-Detailansicht  

DevTools organisiert nun Web-Worker unter dem entsprechenden übergeordneten Frame.  Beispiel: Wenn der `someName`-Frame `worker.js` erstellt, wird `worker.js` unter `someName` in der Liste **Frames** angezeigt.  Führen Sie die folgenden Aktionen aus, um die Details des Web-Worker anzuzeigen.  

1.  Öffnen Sie das **Anwendung**-Tool.  
1.  Erweitern Sie einen Frame, der Web-Worker enthält.  
1.  Erweitern Sie die **Worker**-Struktur.  
1.  Wählen Sie einen Worker aus.  
    
Navigieren Sie zu den Problemen [1122507][CR1122507] und [1051466][CR1051466], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informationen für Web-Worker" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   Informationen für Web-Worker  
:::image-end:::  

#### <a name="display-opener-frame-details-for-opened-windows"></a>Anzeigen von Details zum öffnenden Frame für geöffnete Fenster  

DevTools organisiert nun geöffnete [Fenster][MdnWindowConstructors] unter dem relevanten übergeordneten [Frame][MdnWindowFrames].  Wenn beispielsweise der `top`-Frame ein `Window` mit `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` öffnet, wird das `Window` unter `top` in der Liste **Frames** angezeigt.  

Führen Sie im **Elemente**-Tool die folgenden Aktionen aus, um den Frame anzuzeigen, der für das Öffnen eines anderen Fensters verantwortlich ist.  

1.  Öffnen Sie die Struktur **Frames**.  
1.  Erweitern Sie **Geöffnete Fenster**, und wählen Sie das `Window` für den betreffenden übergeordneten Frame aus.  
1.  Wählen Sie den Link **Öffnender Frame** aus.  

Es werden Details angezeigt, welcher Frame das Öffnen eines anderen `Window` verursacht hat.  Führen Sie die folgenden Aktionen aus, um den Öffner im **Elemente**-Tool anzuzeigen.  

1.  Öffnen Sie die Struktur **Frames**.  
1.  Wählen Sie ein geöffnetes Fenster aus, um die `Window`-Details zu öffnen.  
1.  Wählen Sie den Link **Öffnender Frame** aus.  
    
Navigieren Sie zu Problem [1107766][CR1107766], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Details zum geöffneten Frame" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   Details zum geöffneten Frame  
:::image-end:::  

### <a name="copy-stacktrace-for-network-initiator"></a>Kopieren von StackTrace für den Netzwerkinitiator  

Führen Sie die folgenden Aktionen aus, um den StackTrace in Ihre Zwischenablage zu kopieren.  

1.  Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).  
1.  Wählen Sie **Kopieren** > **StackTrace kopieren** aus.  
    
Navigieren Sie zu Problem [1139615][CR1139615], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Kopieren von StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   Kopieren von StackTrace  
:::image-end:::  

### <a name="preview-wasm-variable-value-on-mouseover"></a>Vorschau eines Wasm-Variablenwerts bei Mouseover  

Verwenden Sie dieses Feature, um den Wert einer WebAssembly \(WASM\)-Variablen zu überprüfen, wenn der Code angehalten wird.  Um den aktuellen Wert einer Variablen anzuzeigen, zeigen Sie auf eine Variable.  Navigieren Sie zu den Problemen [1058836][CR1058836] und [1071432][CR1071432], um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Vorschau von Wasm-Variable bei Mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   Vorschau von Wasm-Variable bei Mouseover  
:::image-end:::  

### <a name="consistent-units-of-measurement-for-sizes-of-files-and-memory"></a>Einheitliche Maßeinheiten für die Größe von Dateien und Arbeitsspeicher  

DevTools verwendet jetzt einheitlich `kB`, um die Größe von Dateien und Arbeitsspeicher anzuzeigen.  Zuvor wurden in DevTools `kB` und `KiB` gemischt.

*   `kB` oder Kilobyte \(10^3 oder 1000 Byte\)  
*   `KiB` oder Kibibyte \(2^10 oder 1024 Byte\)  
    
Das **Netzwerk**-Tool hat beispielsweise zuvor `kB` in den Beschriftungen, aber `KiB` in Berechnungen verwendet.  Ihr Feedback hat gezeigt, dass diese Inkonsistenz Verwirrung stiftet.  Navigieren Sie zu Problem [1035309][CR1035309], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: ../10/devtools.md#customize-keyboard-shortcuts-in-settings "Anpassen von Tastenkombinationen in den Einstellungen – Neuerungen in DevTools (Microsoft Edge 87) | Microsoft Docs"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: ../06/devtools.md#webhint-feedback-in-the-issues-panel "Webhint-Feedback im Bereich „Probleme“ – Neuerungen in DevTools (Microsoft Edge 85) | Microsoft Docs"  

[Devtools3dViewIndex]: ../../../3d-view/index.md "3D-Ansicht | Microsoft Docs"  
[DevtoolsConsoleIndex]: ../../../console/index.md "Übersicht über die Konsole | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Ändern der DevTools-Spracheinstellungen | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../../../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Bearbeiten von Tastenkombinationen für alle Aktionen in DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emulieren von mobilen Geräten in Microsoft Edge DevTools | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: ../../../experimental-features/index.md#enable-keyboard-shortcut-editor "Enable keyboard shortcut editor - Experimental features | microsoft Docs"  -->  
<!--  [DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: ../../../experimental-features/index.md#turn-on-composited-layers-in-3d-view "Turn on Composited Layers in 3D View - Experimental features | Microsoft Docs"  -->  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Suchen und Beheben von Problemen mithilfe des Issues-Tools | Microsoft Docs"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: ../../../network/reference.md#copy-formatted-response-json-to-the-clipboard "Formatierte Antwort-JSON in die Zwischenablage kopieren – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayTimingBreakdownRequest]: ../../../network/reference.md#display-the-timing-breakdown-of-a-request "Anzeigen der zeitlichen Aufteilung einer Anforderung – Netzwerkanalysereferenz | Microsoft Docs"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: ../../../css/reference.md#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsIndex]: ../../../../progressive-web-apps-chromium/index.md "Progressive Web-Apps unter Windows | Microsoft Docs"  

[WebdriverChromiumMain]: ../../../../webdriver-chromium/index.md "Verwenden von WebDriver (Chromium) für die Testautomatisierung | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Herunterladen von WebDriver | Microsoft-Entwickler"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  

[CR174309]: https://crbug.com/174309 "Problem 174309: DevTools: Zulassen der Anpassung von Tastenkombinationen/Tastenbindungen | Chromium-Fehler"  
[CR945786]: https://crbug.com/945786 "Problem 945786: DevTools: Zulassen des Überschreibens von navigator.storage.estimate() | Chromium-Fehler"  
[CR1029427]: https://crbug.com/1029427 "Problem 1029427: Reduzieren des Leistungsmehraufwands beim Protokollnachrichtenversand im Front-End | Chromium-Fehler"  
[CR1035309]: https://crbug.com/1035309 "Problem 1035309: DevTools sollte konsistent MB für Megabyte verwenden, nicht Mebibyte | Chromium-Fehler"  
[CR1051466]: https://crbug.com/1051466 "Problem 1051466: Unterstützung für COOP/COEP-Debugging in DevTools | Chromium-Fehler"  
[CR1058836]: https://crbug.com/1058836 "Problem 1058836: UX-Probleme rund um das WASM-Debuggen | Chromium-Fehler"  
[CR1071432]: https://crbug.com/1071432 "Problem 1071432: ☂️ Grundlegende Wasm-Entwicklererfahrung | Chromium-Fehler"  
[CR1107766]: https://crbug.com/1107766 "Problem 1107766: Anzeigen von Informationen zu von 'window.open()' generierten Frames in der Frame-Struktur | Chromium-Fehler"  
[CR1122507]: https://crbug.com/1122507 "Problem 1122507: Anzeigen von Worker-Informationen in der Framestrukturansicht | Chromium-Fehler"  
[CR1126178]: https://crbug.com/1126178 "Problem 1126178: ☂ Devtools: CSS <type>-Komponenten | Chromium-Fehler"  
[CR1130556]: https://crbug.com/1130556 "Problem 1130556: DevTools: Testen von Bild-Fallbacks (Emulation) | Chromium-Fehler"  
[CR1132084]: https://crbug.com/1132084 "Problem 1132084: Keine einfache Möglichkeit zum Kopieren von JSON-Anforderungsnutzlast | Chromium-Fehler"  
[CR1136394]: https://crbug.com/1136394 "Problem 1136394: Flexbox-Tooling | Chromium-Fehler"  
[CR1138633]: https://crbug.com/1138633 "Problem 1138633: DevTools: CSS <angle>-Komponente sollte das Erscheinungsbild ihrer Eigenschaft im Hintergrund der Uhr widerspiegeln | Chromium-Fehler"  
[CR1139615]: https://crbug.com/1139615 "Problem 1139615: Netzwerkinitiator sollte die Möglichkeit bieten, die Stapelüberwachung zu kopieren | Chromium-Fehler"  
[CR1139899]: https://crbug.com/1139899 "Problem 1139899: Verfügbarkeit der Gated-API in der Frame-Detailansicht melden | Chromium-Fehler"  
[CR1139945]: https://crbug.com/1139945 "Problem 1139945: Symbole für Flexbox-CSS-Eigenschaften im Bereich &quot;Stile&quot; | Chromium-Fehler"  
[CR1141824]: https://crbug.com/1141824 "Problem 1141824: Verbessern der CORS-Fehlerberichterstattung in DevTools | Chromium-Fehler"  
[CR1144090]: https://crbug.com/1144090 "Problem 1144090: Hinzufügen von Flex-Stil-Adornern zur Elemente-Struktur | Chromium-Fehler"  
[CR1146985]: https://crbug.com/1146985 "Problem 1146985: Gelöschter Text wird weiterhin im Textfeld des Abschnitts &quot;Speicher&quot; des DevTools-Fensters angezeigt | Chromium-Fehler"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "CORS-Fehler | Glitch"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Cross-Origin Resource Sharing (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Verwenden von benutzerdefinierten CSS-Eigenschaften (Variablen) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Konstruktoren – Fenster | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window.frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope.crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Barrierefreiheit | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Kompatibilität | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Leistung | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Fallstricke | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Sicherheit | webhint"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-88) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
