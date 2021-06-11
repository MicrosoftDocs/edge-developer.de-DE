---
description: Debugging-Unterstützung für CSS Flexbox, Anzeige zum Leistungs-Heads-up auf der Webseite, Problem von Tool-Updates und mehr
title: Neuigkeiten in DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.localizationpriority: high
ms.openlocfilehash: a13c344bb31cdfb7d0402132e3be82e4c330c612
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597166"
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
# <a name="whats-new-in-devtools-microsoft-edge-90"></a>Neuigkeiten in DevTools (Microsoft Edge 90)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a>Gruppieren von Tools im Fokusmodus  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

Der Fokusmodus ist eine experimentelle Oberfläche, mit der Sie verschiedene Tools basierend auf Ihren eigenen Debugging-Szenarien gruppieren können.  Die neue **Aktivitätsleiste,** auf der linken Seite enthält vordefinierte Toolgruppen wie **Layout** und **Debugging.**  Um jede Toolgruppe anzupassen, schließen Sie Tools  mit dem Symbol **Schließen** \(`X`\) oder fügen Sie neue Tools mit dem Symbol **Weitere Tools** \(`+`\) hinzu.  

Um das Experiment einzuschalten, navigieren Sie zu [Experimentelle Features aktivieren][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] und aktivieren Sie die Kontrollkästchen neben **Fokusmodus und DevTools-QuickInfos** sowie **Registerkartenmenüs Aktivieren + zum Öffnen weiterer Tools**.  Für weitere Informationen zu dieser Funktion oder um Kommentare mit Fragen und Ideen abzugeben, navigieren Sie zu [DevTools: UI-Fokusmodus][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Anzeigen der Aktivitätsleiste" lightbox="../../media/2021/02/focus-mode.msft.png":::
   Anzeigen der **Aktivitätsleiste**  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Mehr über DevTools mit informativen QuickInfos erfahren  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

Das DevTools-QuickInfos-Feature hilft Ihnen, mehr über alle verschiedenen Tools und Bereiche zu erfahren.  Wählen Sie das Symbol Hilfe \(`?`\) unten in der **Aktivitätsleiste**, um die QuickInfos in den DevTools umzuschalten.  Wenn die QuickInfos aktiviert sind, bewegen Sie den Mauszeiger über die einzelnen umrissenen Bereiche von DevTools, um weitere Informationen zur Verwendung des Tools zu erhalten.  Um das Experiment einzuschalten, navigieren Sie zu [Experimentelle Features aktivieren][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] und aktivieren Sie die Kontrollkästchen neben **Fokusmodus und DevTools-QuickInfos** sowie **Registerkartenmenüs Aktivieren + zum Öffnen weiterer Tools**.  Für weitere Informationen zu dieser Funktion oder um Kommentare mit Fragen und Ideen einzureichen, navigieren Sie zu [DevTools: UI-Fokusmodus][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Auswählen des Hilfesymbols (?) In der Aktivitätsleiste, um QuickInfos anzuzeigen" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   Wählen Sie das Symbol Hilfe \(`?`\) in der **Aktivitätsleiste** aus, um QuickInfos anzeigen zu können.  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Anpassen von Tastaturkürzeln in den Einstellungen  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

Sie können die Tastenkombination nun für jede Aktion in den DevTools anpassen.  Führen Sie die folgenden Aktionen aus, um eine Tastenkombination zu bearbeiten.  

1.  Öffnen Sie die DevTools, und wählen Sie dann **Einstellungen**  >  **Verknüpfungen** aus.  
1.  Wählen Sie die Aktion aus, die Sie anpassen möchten.  
1.  Wählen Sie das Bearbeiten \(![Tastenkombinationssymbol "Bearbeiten"](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)\) -Symbol.  
1.  Wählen Sie die Schlüssel aus, die Sie an die Aktion binden möchten.  
1.  Aktivieren Sie das Häkchen \(![Tastenkombinationssymbol "Häkchen"](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)\) -Symbol.  
    
Weitere Informationen zum Anpassen und Bearbeiten von Verknüpfungen finden Sie unter [Anpassen von Tastaturkürzeln in den Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  Um Echtzeitaktualisierungen dieses Features im Open Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [174309][CR174309].  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Anpassen von Tastenkombinationen in den DevTools-Einstellungen für Verknüpfungen mit einer Verknüpfung im Bearbeitungsmodus" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   Anpassen von Tastenkombinationen in den [DevTools-Einstellungen][DevtoolsCustomizeIndexSettings] für Verknüpfungen mit einer Verknüpfung im Bearbeitungsmodus  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a>Microsoft Edge DevTools für Visual Studio Codeerweiterungsupdate 1.1.4  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

Die [Microsoft Edge Developer Tools für Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] -Erweiterung Version 1.1.4 für Microsoft Visual Studio Code zeigt jetzt neben jeder DevTools-Instanz ein Favicon an.  Konsolennachrichten von Microsoft Edge werden jetzt in der **DevTools-Konsole** unter **Problem** von Microsoft Visual Studio-Code angezeigt.  Microsoft Visual Studio Code aktualisiert Erweiterungen automatisch.  Navigieren Sie zum manuellen Aktualisieren auf Version 1.1.4 zu [Manuelles Aktualisieren einer Erweiterung][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].  Sie können Probleme einreichen und zur Erweiterung des GitHub-Repos [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools] beitragen.  

:::row:::
   :::column span="":::
      In der folgenden Abbildung werden Nachrichten von einer Beispielwebseite angezeigt, die im **Konsole** -Tool in Microsoft Edge protokolliert wurde.  
   :::column-end:::
   :::column span="":::
      In der folgenden Abbildung werden dieselben Nachrichten von der Beispielwebseite angezeigt, die in der **DevTools-Konsole** unter **Problem** von Microsoft Visual Studio-Code protokolliert ist.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Anzeigen einer Nachricht in der Konsole in Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         Anzeigen einer Nachricht in der Konsole in Microsoft Edge DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Anzeigen derselben Nachricht in der DevTools-Konsole unter Problem von Microsoft Visual Studio-Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         Anzeigen derselben Nachricht in der DevTools-Konsole unter Problem von Microsoft Visual Studio-Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a>Verbesserte CSS-Flexbox-Bearbeitung mit visuellem Flexbox-Editor und mehreren Overlays  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

DevTools verfügt jetzt über dedizierte CSS-Flexbox-Debuggingtools.  Wenn der `display: flex` oder `display: inline-flex` CSS-Stil auf ein HTML-Element angewendet wird, wird ein `flex` Symbol neben diesem Element im **Element**-Tool angezeigt.  Zum Anzeigen \(oder Ausblenden\) einer Flexüberlagerung auf der Webseite wählen Sie das `flex` Symbol aus.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [1166710][CR1166710] und [1175699][CR1175699].  

:::row:::
   :::column span="":::
      Navigieren Sie zum Öffnen des **Flexbox** -Editors zum Bereich**Stile**, und wählen Sie das neue Symbol neben dem Stil `display: flex` oder `display: inline-flex` aus.  Der **Flexbox** -Editor bietet eine schnelle Möglichkeit, die Flexbox-Eigenschaften zu bearbeiten.  
   :::column-end:::
   :::column span="":::
      Darüber hinaus werden im Abschnitt **Flexbox** im Bereich **Layout** alle Flexbox-Elemente auf der Webseite angezeigt.  Sie können die Überlagerung der einzelnen Elemente umschalten.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="CSS-Flexbox-Debuggingtools" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         CSS-Flexbox-Debuggingtools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Abschnitt Flexbox im Layoutbereich" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         Abschnitt **Flexbox** im Bereich **Layout**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a>Verbesserungen der Tastaturnavigation für Netzwerkanforderungen  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

Bisher war es Ihnen nicht möglich, die Anforderungskette mithilfe der Pfeiltasten auf der Tastatur im Bereich **Initiator** zu erweitern oder zu reduzieren, im Gegensatz zum DOM im Tool **Elemente**.  Wenn im **Netzwerk** -Tool eine Netzwerkanforderung ausgewählt ist, wird im Bereich **Initiator** die Anforderungskette angezeigt, welche die aktuell ausgewählte Anforderung initiiert hat.  

In Microsoft Edge Version 90 können Sie die Anforderungskette mithilfe der Pfeiltasten auf der Tastatur im Bereich **Initiator** erweitern oder reduzieren.  Die fokussierte Netzwerkanforderung in der Kette wird jetzt ebenfalls hervorgehoben.  Weitere Informationen zu Initiatoren im **Netzwerk** -Tool finden Sie unter [Anzeigen von Initiatoren und Abhängigkeiten][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].  Um den Verlauf dieses Features im Chromium-Open-Source-Projekt zu überprüfen, navigieren Sie zu den Problemen [1158276][CR1158276] und [1160637][CR1160637].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Wählen Sie eine Netzwerkanforderung und dann den Initiatorbereich." lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         Wählen Sie eine Netzwerkanforderung und dann den Bereich **Initiator**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Erweitern oder reduzieren Sie die Anforderungsinitiator-Kette und folgen Sie der markierten Zeile" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         Erweitern oder reduzieren Sie die Anforderungsinitiator-Kette und folgen Sie der markierten Zeile  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a>Das Filtern in der Konsole ist konsistenter  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

Während Sie mit der [Konsolen-Randleiste][DevtoolsConsoleReferenceOpenConsoleSidebar] filtern, sind die Filter in der Dropdown-Liste [Protokollebenen][DevtoolsConsoleReferenceFilterByLogLevel] nicht verfügbar.  Zuvor wurde die Dropdown-Liste **Protokollebenen** hervorgehoben, wenn Sie mit der Maus darüber gefahren sind, obwohl ein Filter aus der **Konsolen-Randleiste** ausgewählt wurde.  In Microsoft Edge Version 90 wird die Dropdown-Liste **Protokollebenen** nicht mehr hervorgehoben, wenn Sie den Mauszeiger darüber halten, während ein Filter aus der **Konsolen-Randleiste** ausgewählt ist.  Weitere Informationen zum Filtern in der **Konsole** finden Sie unter [Nachrichten filtern][DevtoolsConsoleReferenceFilterMessages].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Wenn Sie zuvor die Konsolen-Randleiste geöffnet haben und mit der Maus über die Standardebenen bewegen, wurde diese hervorgehoben." lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         Wenn Sie zuvor die **Konsolen-Randleiste** geöffnet haben und mit der Maus über die **Standardebenen** bewegen, wurde diese hervorgehoben.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="Wenn Sie ab Microsoft Edge 90 die Konsolen-Randleiste auswählen und den Mauszeiger auf den Standardebenen bewegen, wird diese nicht hervorgehoben." lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         Wenn Sie ab Microsoft Edge 90 die **Konsolen-Randleiste** auswählen und den Mauszeiger auf den **Standardebenen** bewegen, wird diese nicht hervorgehoben.  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a>Die Konsole entkommt nun doppelten Anführungszeichen  

Zuvor hat die **Konsole** keine gültigen doppelten Anführungszeichen \(`"`\) in JavaScript-Zeichenfolgen ausgegeben.  Ab Microsoft Edge Version 90 gibt die **Konsole** JavaScript-Zeichenfolgen mit maskierten doppelten Anführungszeichen \(`"`\) aus.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [1178530][CR1178530].  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="Die Konsole gibt JavaScript-Zeichenfolgen mit maskierten doppelten Anführungszeichen (& # 0022;) aus" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   Die **Konsole** gibt JavaScript-Zeichenfolgen unter Verwendung von maskierten doppelten Anführungszeichen \(`"`\) aus.  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a>Emulieren des CSS-Medienfeatures mit Farbskala  

Die Medienabfrage mit [Farbskala][ChromestatusFeature5354410980933632] emuliert den ungefähren Farbbereich, der vom Browser und dem zu testenden Gerät unterstützt wird.  Das Dropdown-Menü unter **Emulieren der Farbskala für CSS-Medienfunktionen** enthält Farbräume, die DevTools möglicherweise emulieren.  Beispielsweise, zum Auslösen einer `color-gamut: p3` Medienabfrage, wählen Sie die **Farbskala: p3**in der Dropdown-Liste.  

Zum Emulieren des CSS-Features für Farbskalenmedien, führen Sie die folgenden Aktionen aus.  

1.  Öffnen Sie das [Befehlsmenü][DevtoolsCommandMenuIndex].  
1.  Geben Sie `Rendering` ein.  
1.  Führen Sie den Befehl **Rendering anzeigen** aus.  
1.  Navigieren Sie zu **Emulieren der Farbskala für CSS-Medienfunktionen** und wählen Sie eine Option aus.  

Um mehr über das `color-gamut` Feature zu erfahren, navigieren Sie zu [Farbanzeigequalität: das Feature "Farbskala"][CsswgDraftsMediaqueries4ColorGamut].  Navigieren Sie zur Problem [1073887][CR1073887], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emulieren des CSS-Medienfeatures mit Farbskala" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   Emulieren des CSS-Medienfeatures mit Farbskala  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a>Verbesserte Progressive Web Apps-Tools  

#### <a name="pwa-installability-warning-in-the-console"></a>PWA-Installationswarnung in der Konsole  

Die **Konsole** zeigt jetzt eine detailliertere Warnmeldung zur Installiationsfähigkeit von [Progressive Web Apps (PWA)][ProgressiveWebAppsIndex] mit einem Link zur [Verbesserung der Offline-Supporterkennung für Progressive Web Apps][ChromeDeveloperBlogImprovedPwaOfflineDetection] an.  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Warnung zur Installiationsfähigkeit von PWA im Konsolentool" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   Warnung zur Installiationsfähigkeit von PWA im Tool **Konsole**  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a>Warnung zur Länge der PWA-Beschreibung im Manifestbereich

Im Bereich **Manifest** wird jetzt eine Warnmeldung angezeigt, wenn die Manifestbeschreibung mehr als 324 Zeichen enthält.  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Warnung zum Kürzen der PWA-Beschreibung" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   Warnung zum Kürzen der PWA-Beschreibung  
:::image-end:::  

Navigieren Sie zu den Problemen [965802][CR965802], [1146450][CR1146450] und [1169689][CR1169689], um den Verlauf dieser Funktion im Chromium-Open-Source-Projekt zu überprüfen.  

### <a name="new-remote-address-space-column-in-the-network-tool"></a>Neue Remote-Adressraum-Spalte im Netzwerk-Tool  

<!-- does not work in canary 90.0.813.0 -->  
In der neuen Spalte **Remote-Adressraum** wird der Netzwerk-IP-Adressraum jeder Netzwerkressource angezeigt.  Führen Sie die folgenden Aktionen aus, um die neue Spalte "Remote-Adressraum" anzuzeigen.  

1.  Navigieren Sie zum **Netzwerk**-Tool.  
1.  Bewegen Sie den Mauszeiger in der Tabelle "Anforderungen" über die Kopfzeile und öffnen Sie das Kontextmenü \(Rechtsklick\).  Navigieren Sie zu [Spalten hinzufügen oder entfernen][DevtoolsNetworkReferenceAddRemoveColumns], um zu erfahren, wie Sie Spalten zur Tabelle "Anforderungen" hinzufügen oder daraus entfernen.  
1.  Wählen Sie **Remote-Adressraum** aus.  
    
In der Tabelle "Anforderungen" wird jetzt eine neue Spalte mit der Kopfzeile **Remote-Adressraum** angezeigt.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [1128885][CR1128885].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="Wählen Sie im Kontextmenü Remote-Adressraum" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         Wählen Sie im Kontextmenü den **Remote-Adressraum**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="In der Tabelle Anforderungen wird jetzt die Spalte Remote-Adressraum angezeigt." lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         In der Tabelle "Anforderungen" wird jetzt die Spalte **Remote-Adressraum** angezeigt. :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a>Anzeigen zulässiger und nicht zulässiger Features in der Frame-Detailansicht  

In der Frame-Detailansicht wird jetzt eine Liste der zulässigen und nicht zulässigen Browserfunktionen angezeigt, die von der [Berechtigungsrichtlinie][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer] gesteuert werden.  Die Berechtigungsrichtlinie ist eine Webplattform-API, die es einer Webseite ermöglicht (oder blockiert), Browserfeatures in einem einzelnen Frame oder in eingebetteten iframes zu verwenden.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Zulässige und nicht zulässige Features basierend auf der Berechtigungsrichtlinie" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   Zulässige und nicht zulässige Features basierend auf der Berechtigungsrichtlinie  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a>Neue SameParty-Spalte im Bereich "Cookies"  

Im Bereich **Cookies** im Tool **Anwendung** wird jetzt das `SameParty` Attribut für jedes Cookie angezeigt.  Das `SameParty` Attribut ist ein neues boolesches Attribut, das angibt, ob ein Cookie in Anforderungen an Ursprünge derselben [First-Party-Sets][GithubPrivacycgFirstPartySets] enthalten ist.  Navigieren Sie zu Problem [1161427][CR1161427], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="SameParty-Spalte im Bereich Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   **SameParty**-Spalte im Bereich **Cookies**  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a>Die Eigenschaft fn.displayName im Konsolentool ist jetzt veraltet.  

Bisher konnten Sie mit der `fn.displayName` Eigenschaft Debug-Namen für Funktionen steuern, die in `error.stack` und in DevTools-Stapelüberwachung angezeigt werden sollen.  Ab Microsoft Edge Version 90 ist die `fn.displayName` Eigenschaft jetzt veraltet und wird durch die `fn.name` Eigenschaft ersetzt.  Verwenden Sie die `Object.defineProperty` Standardmethode, um die `fn.name` Eigenschaft zu definieren.  Um mehr über zu `fn.name` erfahren, navigieren Sie zu [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].  Navigieren Sie zu Problem [1177685][CR1177685], um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Ein Beispiel für die Eigenschaft fn.name zur Steuerung von Debug-Namen für Funktionen" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   Ein Beispiel für die `fn.name` Eigenschaft zur Steuerung von Debug-Namen für Funktionen  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a>Vollständige Barrierefreiheitsstrukturansicht im Elements-Tool  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Dieses Experiment bietet eine **vollständige Barrierefreiheitsstrukturansicht** im **Elemente**-Tool.  Der Bereich [Barrierefreiheit][DevtoolsAccessibilityTab] bietet eine teilweise Barrierefreiheitsstrukturansicht, in der die direkte Ahnenkette vom Stammknoten zum inspizierten Knoten angezeigt wird.  
Nachdem Sie dieses Experiment aktiviert und die DevTools neu geladen haben, wählen Sie eine der folgenden Schaltflächen, um die Anzeige im Elementwerkzeug für alle Elemente auf der Webseite zu wechseln.  

*   Um die vollständige Barrierefreiheitsstrukturansicht anzuzeigen, wählen Sie **Zur Barrierefreiheitsstrukturansicht wechseln**.  
*   Wählen Sie zum Anzeigen der DOM-Strukturansicht **Zur DOM-Strukturansicht wechseln** aus.  
    
Um das Experiment zu aktivieren, navigieren Sie zu [Experimentelle Features aktivieren][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben **Aktivieren der vollständigen Barrierefreiheitsstruktur im Elementbereich**.  Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Problem [887173][CR887173].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Anzeigen der DOM-Strukturansicht" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         Anzeigen der **DOM-Strukturansicht**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Anzeigen der Strukturansicht „Vollständige Barrierefreiheit“" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         Anzeigen der **Vollständigen Barrierefreiheitsstrukturansicht**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityTab]: ../../../accessibility/accessibility-tab.md "Testen Sie die Barrierefreiheit mithilfe der Registerkarte &quot;Barrierefreiheit&quot; | Microsoft-Dokumentation"  
[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Ausführen von Befehlen mit dem Microsoft Edge DevTools-Befehlsmenü | Microsoft-Dokumentation"  
[DevtoolsConsoleReferenceFilterByLogLevel]: ../../../console/reference.md#filter-by-log-level "Filtern nach Protokollebene – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: ../../../console/reference.md#filter-messages "Filtern von Nachrichten – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: ../../../console/reference.md#open-the-console-sidebar "Öffnen der Konsolen-Randleiste – Konsolenreferenz | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: ../../../experimental-features/index.md#enable--button-tab-menus-to-open-more-tools "Aktivieren Sie die Registerkartenmenüs +, um weitere Werkzeuge zu öffnen – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../../../experimental-features/index.md#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: ../../../network/reference.md#add-or-remove-columns "Hinzufügen oder Entfernen von Spalten – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: ../../../network/reference.md#display-initiators-and-dependencies "Anzeigen von Initiatoren und Abhängigkeiten – Netzwerkanalysereferenz | Microsoft Docs"  

[ProgressiveWebAppsIndex]: ../../../../progressive-web-apps-chromium/index.md "Übersicht über progressive Web Apps unter Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Verbessern der Erkennung der progressiven Web App-Offline-Unterstützung | Chrome-Entwickler"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "Farbskala-Medienabfrage | Chrome-Plattformstatus"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  
[CR174309]: https://crbug.com/174309 "Problem 174309: DevTools: Zulassen der Anpassung von Tastenkombinationen/Tastenbindungen | Chromium-Fehler"  
[CR887173]: https://crbug.com/887173 "Problem 887173: DevTools: Vollständige Barrierefreiheitsstrukturüberprüfung | Chromium-Fehler"  
[CR965802]: https://crbug.com/965802 "Problem 965802: Implementieren einer genaueren Offline-Fähigkeitserkennung für Servicemitarbeiter | Chromium-Fehler"  
[CR1073887]: https://crbug.com/1073887 "Problem 1073887: DevTools: @media (Farbskala: ...) Farbraumemulation | Chromium-Fehler"  
[CR1128885]: https://crbug.com/1128885 "Problem 1128885: DevTools-Unterstützung für CORS-RFC1918 | Chromium-Fehler"  
[CR1146450]: https://crbug.com/1146450 "Problem 1146450: [Android] Implementieren von Bottom Sheet-Installationen | Chromium-Fehler"  
[CR1158276]: https://crbug.com/1158276 "Problem 1158276: Der Bereich &quot;Initiator-Kette anfordern&quot; kann nicht mithilfe der Pfeiltasten im Abschnitt &quot;Netzwerk&quot; von DevTools erweitert/verkleinert werden | Chromium-Fehler"  
[CR1158827]: https://crbug.com/1158827 "Problem 1158827: [Berechtigungsrichtlinie] Implementieren der Devtool-Unterstützung für Berechtigungsrichtlinien | Chromium-Fehler"  
[CR1160637]: https://crbug.com/1160637 "Problem 1160637: Der Fokus auf 'Initiierungskette anfordern' wird im Abschnitt 'Netzwerk' des Fensters 'Dev Tools' unvollständig angezeigt | Chromium-Fehler"  
[CR1161427]: https://crbug.com/1161427 "Problem 1161427: &#9730; Unterstützt das Debuggen von SameParty-Cookie-Attributen in DevTools | Chromium-Fehler"  
[CR1166710]: https://crbug.com/1166710 "Problem 1166710: Standardmäßiges Aktivieren des Flexbox-Tooling-Experiment | Chromium-Fehler"  
[CR1169689]: https://crbug.com/1169689 "Problem 1169689: Das untere Blatt der PWA-Installation sollte keine Kategorien enthalten | Chromium-Fehler"  
[CR1175699]: https://crbug.com/1175699 "Problem 1175699: Flexbox-Editor | Chromium-Fehler"  
[CR1177685]: https://crbug.com/1177685 "Problem 1177685: Entfernen von nicht standardmäßiger Unterstützung für fn.displayName | Chromium-Fehler"  
[CR1178530]: https://crbug.com/1178530 "Problem 1178530: Die Konsole maskiert beim Drucken von Zeichenfolgen keine doppelten Anführungszeichen | Chromium-Fehler"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Farbanzeigequalität: Das Feature &quot;Farbskala&quot; | Entwürfe des CSS-Arbeitsgruppen-Editors"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: Benutzeroberfläche für den Fokusmodus – MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "First-Party-Sets | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Berechtigungsrichtlinienerklärer | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-90) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
