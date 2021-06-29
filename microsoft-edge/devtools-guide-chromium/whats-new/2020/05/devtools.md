---
description: Verwenden Sie die DevTools in Windows Modus mit hohem Kontrast, passen Sie Tastenkombinationen in devTools an Visual Studio Code an und vieles mehr.
title: Neuigkeiten in DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: fabfa21abedb02bc83ec2bedbe3662f0d81c1bf9
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624808"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-84"></a>Neuigkeiten in DevTools (Microsoft Edge 84)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Ankündigungen des Microsoft Edge DevTools-Teams  

In den folgenden Abschnitten finden Sie eine Liste der Ankündigungen, die Sie möglicherweise vom Microsoft Edge DevTools-Team verpasst haben.  Sehen Sie sich die Ankündigungen an, um neue Features in devTools, Microsoft Visual Studio Codeerweiterungen und vieles mehr auszuprobieren.  Um über die neuesten und besten Features in Ihren Entwicklertools auf dem Laufenden zu bleiben, laden Sie die [Microsoft Edge Vorschaukanäle][MicrosoftEdgePreviewChannels] herunter, und [folgen Sie uns auf Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a>Verwenden der DevTools im Modus Windows hohen Kontrasts

Die Microsoft Edge DevTools werden jetzt im Modus mit hohem Kontrast angezeigt, wenn sich Windows im Modus mit hohem Kontrast befindet.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Die Microsoft Edge DevTools im Modus mit hohem Kontrast" lightbox="../../media/2020/05/high-contrast.msft.png":::
   Die Microsoft Edge DevTools im Modus mit hohem Kontrast  
:::image-end:::  

[Befolgen Sie die Anweisungen, um den Modus für hohen Kontrast in Windows zu aktivieren.][MicrosoftSupportWindows10HighContrastMode]  Um die DevTools in Microsoft Edge zu öffnen, wählen `F12` Sie oder `Ctrl` + `Shift` + `I` aus.  Die DevTools werden im Modus mit hohem Kontrast angezeigt.  

> [!NOTE]
> Die Microsoft Edge DevTools unterstützen derzeit den Modus mit hohem Kontrast auf Windows, jedoch nicht unter macOS.  

Chromium Problem [#1048378][CR1048378]  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a>Anpassen von Tastenkombinationen in devTools an Visual Studio Code  

Anhand Ihres [Feedbacks](#getting-in-touch-with-microsoft-edge-devtools-team) und der [Chromium öffentlichen Problemverfolgung][CRIssuesList]hat das Microsoft Edge DevTools-Team erfahren, dass Sie die Möglichkeit haben wollten, Tastenkombinationen in den DevTools anzupassen.  In Microsoft Edge 84 können Sie nun Tastenkombinationen in devTools mit [Visual Studio Code][VisualStudioCodeMain]abgleichen, was nur eines der Features ist, an denen das Team für die Anpassung von Tastenkombinationen arbeitet.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Anpassen von Tastenkombinationen in devTools an Visual Studio Code" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   Die Microsoft Edge DevTools im Modus mit hohem Kontrast  
:::image-end:::  

Um das Experiment auszuprobieren, öffnen Sie DevTools Einstellungen, indem Sie `?` in der oberen rechten Ecke der DevTools das Symbol devtools Einstellungen auswählen oder ![ ](../../../media/settings-icon.msft.png) auswählen.  Navigieren Sie zum Abschnitt **"Experimente",** und aktivieren Sie die Registerkarte "Einstellungen für **benutzerdefinierte Tastenkombinationen aktivieren" (muss neu geladen werden).**  Laden Sie nun die DevTools neu, öffnen Sie Einstellungen erneut, und navigieren Sie zum Abschnitt **"Verknüpfungen".**  

Wählen Sie **DevTools (Standard)** in den **Verknüpfungen "Übereinstimmung" aus dem vordefinierten** Dropdownmenü aus, und wählen Sie **Visual Studio Code**aus.  Die Tastenkombinationen in den DevTools stimmen jetzt mit den Tastenkombinationen für entsprechende Aktionen in Visual Studio Code überein.  

Beispielsweise lautet die Tastenkombination zum Anhalten oder Fortsetzen der Ausführung eines Skripts in [Visual Studio Code][VisualStudioCodeShortcuts] `F5` .  Mit der **Voreinstellung DevTools (Standard)** ist die gleiche Verknüpfung in devTools, `F8` aber mit der **Visual Studio Code** Voreinstellung ist diese Verknüpfung jetzt auch `F5` .  

Das Feature ist derzeit in Microsoft Edge 84 als Experiment verfügbar. Teilen Sie ihr [Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) also bitte mit dem Team!  

Chromium Problem [#174309][CR174309]  

### <a name="remote-debug-surface-duo-emulators"></a>Remotedebugging von Surface Duo-Emulatoren  

Sie können jetzt Ihre Webinhalte, die im [Surface Duo-Emulator][DualScreensAndroidEmulator] ausgeführt werden, remote debuggen, indem Sie die volle Leistungsfähigkeit der [Microsoft Edge DevTools][DevtoolsIndex]nutzen.  

Mit dem [Surface Duo-Emulator][DualScreensAndroidEmulator]können Sie testen, wie Ihre Webinhalte auf einer neuen Klasse von faltbaren Geräten und Geräten mit dualem Bildschirm gerendert werden.  Der Emulator führt das Android-Betriebssystem aus und stellt die [Microsoft Edge Android-App bereit.][AndroidEdge]  Laden Sie Ihre Webinhalte in die [Microsoft Edge-App,][AndroidEdge] und debuggen Sie sie mit [der Microsoft Edge DevTools.][DevtoolsIndex]  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Die Microsoft Edge-App, die auf dem Surface Duo-Emulator ausgeführt wird" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   Die Microsoft Edge-App im Surface Duo-Emulator  
:::image-end:::  

Die `edge://inspect` Seite in einer Desktopinstanz von [Microsoft Edge][DesktopEdge] zeigt den **SurfaceDuoEmulator** mit einer Liste der geöffneten Registerkarten oder [PWAs][PwaIndex] an, die im [Surface Duo-Emulator][DualScreensAndroidEmulator]ausgeführt werden.  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="Auf der edge://inspect Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge App angezeigt, die im Emulator ausgeführt wird." lightbox="../../media/2020/05/edge-inspect.msft.png":::
   Auf `edge://inspect` der Seite wird eine Liste der geöffneten Registerkarten in der Microsoft Edge App angezeigt, die im Emulator ausgeführt wird.
:::image-end:::  

Überprüfen **** Sie die Registerkarte oder PWA, die Sie debuggen möchten, um die [Microsoft Edge DevTools][DevtoolsIndex]zu öffnen.  [Befolgen Sie die schrittweise Anleitung, um Webinhalte im Surface Duo-Emulator remote zu debuggen.][DevtoolsRemoteDebugDuoEmulator]  

### <a name="resize-the-devtools-drawer-more-easily"></a>Einfacheres Ändern der Größe der DevTools-Schublade  

In Microsoft Edge 83 oder früheren Versionen konnten Sie die Größe der [Devtools-Schublade][DevtoolsDrawer] nur ändern, indem Sie auf die Symbolleiste der Schublade zeigen.  The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover on the border of the pane toize it.  Wählen Sie die folgende Abbildung aus, um anzuzeigen, wie die Größenänderung der Schublade in Version 83 oder früher von Microsoft Edge funktioniert hat.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Ändern der Größe der DevTools-Schublade in Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Ändern der Größe der DevTools-Schublade in Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Ab Microsoft Edge 84 können Sie jetzt die Größe der Schublade ändern, indem Sie über den Rahmen der Schublade zeigen.  Diese Änderung richtet das Verhalten beim Ändern der Größe der DevTools-Schublade an die Art und Weise aus, wie Sie die Größe anderer Bereiche in den DevTools ändern.  Wählen Sie das folgende Bild aus, um die Größenänderung in Aktion in Microsoft Edge 84 anzuzeigen.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Ändern der Größe der DevTools-Schublade in Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Ändern der Größe der DevTools-Schublade in Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Chromium Problem [#1076112][CR1076112]  

### <a name="screencasting-navigation-buttons-display-focus"></a>Bildschirmcasting-Navigationsschaltflächen zeigen den Fokus an  

Beim Remotedebuggen eines [Android-Geräts,][DevtoolsRemoteDebugAndroid]eines [Windows 10 Geräts][DevtoolsRemoteDebugWindows]oder eines [Surface Duo-Emulators][DevtoolsRemoteDebugDuoEmulator]können Sie screencasting mit dem ![ Toggle ](../../../media/toggle-screencast-icon.msft.png) Screencast-Symbol in der oberen linken Ecke der DevTools umschalten.  Wenn Screencasting aktiviert ist, können Sie über das DevTools-Fenster in Microsoft Edge auf dem Remotegerät navigieren.  In Microsoft Edge 84 sind diese Navigationsschaltflächen jetzt auch über die Tastatur zugänglich.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Wählen Sie "UMSCHALT+TAB" aus der bildschirmierten URL-Leiste aus, um den Fokus auf der Schaltfläche "Aktualisieren" anzuzeigen." lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   Wählen Sie `Shift` + `Tab` in der Screencast-URL-Leiste den Fokus auf der Schaltfläche **"Aktualisieren"** aus.
:::image-end:::  

Chromium Problem [#1081486][CR1081486]  

### <a name="network-panel-details-pane-is-now-accessible"></a>Auf den Bereich "Netzwerkpaneldetails" kann jetzt zugegriffen werden.  

In Microsoft Edge 84 erhält der [Detailbereich][DevtoolsNetworkDetails] im **Netzwerktool** jetzt den Fokus, wenn Sie ihn für eine Ressource im [Netzwerkprotokoll][DevtoolsNetworkLog]öffnen.  Diese Änderung ermöglicht es Bildschirmleseprogrammen, den Inhalt des **Detailbereichs** auszulesen und mit ihnen zu interagieren.  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Der Bereich "Details" im Netzwerkbereich erhält beim Öffnen den Fokus." lightbox="../../media/2020/05/network-details.msft.png":::
   Der **Detailbereich** im **Netzwerktool** erhält den Fokus, wenn er geöffnet wird
:::image-end:::  

Chromium Problem [#963183][CR963183]  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

In den folgenden Abschnitten werden zusätzliche Features angekündigt, die in Microsoft Edge 84 verfügbar sind, die zum Open Source Chromium Projekt beigetragen haben.  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a>Beheben von Websiteproblemen mit dem neuen Tool "Probleme" in der DevTools-Schublade

Das neue **Tool "Probleme"** in der DevTools-Schublade wurde entwickelt, um die Benachrichtigungsermüdung und Unübersichtlichkeit der **Konsole**zu reduzieren.  Derzeit ist die **Konsole** der zentrale Ort für Websiteentwickler, Bibliotheken, Frameworks und Microsoft Edge zum Protokollieren von Nachrichten, Warnungen und Fehlern.  Das **** Problemtool aggregiert Warnungen aus dem Browser auf strukturierte, aggregierte und umsetzbare Weise, links zu betroffenen Ressourcen in Microsoft Edge DevTools und bietet Anleitungen zum Beheben der Probleme.  Im Laufe der Zeit werden mehr und mehr Warnungen in Microsoft Edge im **Problemtool** anstelle der **Konsole**angezeigt, was dazu beitragen sollte, die Unübersichtlichkeit in der **Konsole**zu verringern.  

To get started, navigate to [Find and fix problems using the Issues tool][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Das Tool "Probleme" in der DevTools-Schublade" lightbox="../../media/2020/05/issues.msft.png":::
   Das **Tool "Probleme"** in der DevTools-Schublade  
:::image-end:::  

Chromium Problem [#1068116][CR1068116]  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a>Anzeigen von Barrierefreiheitsinformationen in der QuickInfo zum Überprüfen des Modus  

Die QuickInfo zum **Prüfen des Modus** gibt nun an, ob das Element einen Namen und eine [Rolle][WebhintHintsAxeNameRoleValue] für die Verwendung durch Zugriff auf die Tastatur hat und [tastaturfokussierbar][WebhintHintsAxeKeyboard]ist.  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="QuickInfo zum Überprüfungsmodus mit Informationen zur Barrierefreiheit" lightbox="../../media/2020/05/a11y.msft.png":::
  QuickInfo zum **Überprüfungsmodus** mit Informationen zur Barrierefreiheit  
:::image-end:::  

Chromium Problem [#1040025][CR1040025]  

### <a name="performance-panel-updates"></a>Aktualisierungen des Leistungsbereichs  

#### <a name="view-total-blocking-time-information-in-the-footer"></a>Anzeigen der Informationen zur Gesamtblockierungszeit in der Fußzeile  

Nach dem Aufzeichnen der Ladeleistung zeigt der **Leistungsbereich** nun informationen zur Gesamtblockierungszeit \(TBT\) in der Fußzeile an.  TBT ist eine Lastleistungsmetrik, die quantifiziert, wie lange eine Seite benötigt, um verwendbar zu werden.  Es misst im Wesentlichen, wie lange eine Seite verwendbar zu sein scheint \(da der Inhalt auf dem Bildschirm gerendert wird\); kann jedoch nicht verwendet werden, da JavaScript den Hauptthread blockiert und die Seite daher nicht auf Benutzereingaben reagiert.  TBT ist die Hauptmetrik für die Ersteingabeverzögerung.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Verwenden Sie zum Abrufen der Informationen zur Gesamtblockierungszeit nicht den Symbolworkflow **"Seite** aktualisieren", um die Leistung beim Laden der ![ ](../../../media/refresh-page-icon.msft.png) Seite aufzuzeichnen.  

**Wählen** Sie stattdessen ![ das Datensatzsymbol ](../../../media/record-icon.msft.png) aus, laden Sie die Seite manuell neu, warten Sie, bis die Seite geladen wird, und beenden Sie die Aufzeichnung.  

Wenn `Total Blocking Time: Unavailable` diese angezeigt wird, hat Microsoft Edge DevTools nicht die erforderlichen Informationen aus den internen Profilerstellungsdaten in Microsoft Edge abgerufen.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Informationen zur Gesamtblockierungszeit in der Fußzeile einer Aufzeichnung des Leistungsbereichs" lightbox="../../media/2020/05/tbt.msft.png":::
   Informationen zur Gesamtblockierungszeit in der Fußzeile einer Aufzeichnung des **Leistungsbereichs**  
:::image-end:::  

Chromium Problem [#1054381][CR1054381]  

#### <a name="layout-shift-events-in-the-new-experience-section"></a>Layout shift events in the new Experience section  

Der neue Abschnitt **"Erfahrung"** im **Bereich "Leistung"** hilft Ihnen, Layoutverschiebungen zu erkennen.  Kumulative Layoutverschiebung \(CLS\) ist eine Metrik, die Ihnen hilft, unerwünschte visuelle Instabilität zu quantifizieren.

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

Wählen Sie das **Layout shift-Ereignis** aus, um die Details der Layoutverschiebung im **Zusammenfassungsbereich** anzuzeigen.  Zeigen Sie auf die Felder **"Verschoben von"** und **"Verschoben",** um zu visualisieren, wo die Layoutverschiebung aufgetreten ist.  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Die Details einer Layoutverschiebung" lightbox="../../media/2020/05/cls.msft.png":::
   Die Details einer Layoutverschiebung  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a>Präzisere Zusageterminologie in der Konsole  

Bei der Protokollierung eines `Promise` **Werts** wurde für die Konsole fälschlicherweise `PromiseStatus` ein Wert bereitgestellt, der auf `resolved` .  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Ein Beispiel für die Konsole mit der alten aufgelösten Terminologie" lightbox="../../media/2020/05/resolved.msft.png":::
   Ein Beispiel für die **Konsole** mit der alten `resolved` Terminologie  
:::image-end:::  

Die **Konsole** verwendet nun den `fulfilled` Begriff, der der Spezifikation entspricht. `Promise`  Weitere Informationen zur `Promise` Spezifikation, navigieren Sie zu ["Zustände" und "Zustände" auf GitHub.](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md)  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Ein Beispiel für die Konsole mit der neuen erfüllten Terminologie" lightbox="../../media/2020/05/fulfilled.msft.png":::
  Ein Beispiel für die **Konsole** mit der neuen `fulfilled` Terminologie  
:::image-end:::  

V8-Problem [#6751][CRV86751]  

### <a name="styles-pane-updates"></a>Aktualisierungen des Formatvorlagenbereichs  

#### <a name="support-for-the-revert-keyword"></a>Unterstützung für das Revert-Schlüsselwort  

Die Benutzeroberfläche für automatisches Vervollständigen des Bereichs **"Formatvorlagen"** erkennt nun das [CSS-Schlüsselwort "Zurücksetzen",][MDNRevert] das den überlappenden Wert einer Eigenschaft auf den vorherigen Wert zurücksetzt, der auf die Formatierung des Elements angewendet wurde.  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Festlegen des Werts einer Eigenschaft, die wiederhergestellt werden soll" lightbox="../../media/2020/05/revert.msft.png":::
  Festlegen des Werts einer Eigenschaft, die wiederhergestellt werden soll  
:::image-end:::  

Chromium Problem [#1075437][CR1075437]  

#### <a name="image-previews"></a>Bildvorschau  

Zeigen Sie auf einen `background-image` Wert im Bereich **"Formatvorlagen",** um eine Vorschau des Bilds in einer QuickInfo anzuzeigen.  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Bewegen des Mauszeigers über einen Hintergrundbildwert" lightbox="../../media/2020/05/image-preview.msft.png":::
  Bewegen des Mauszeigers über einen `background-image` Wert  
:::image-end:::  

Chromium Problem [#1040019][CR1040019]  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a>Die Farbauswahl verwendet jetzt eine durch Leerzeichen getrennte funktionale Farbschreibweise.  

[Css Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()` , should support space-separated arguments.  So ist zum Beispiel `rgb(0, 0, 0)` gleichwertig mit `rbg(0 0 0)`.  

Wenn Sie Farben mit der [Farbauswahl][DevtoolsCssReferenceColorPicker] auswählen oder zwischen Farbdarstellungen im Bereich **"Formatvorlagen"** wechseln, indem Sie den Wert beibehalten `Shift` und `background-color` auswählen, wird die Durch Leerzeichen getrennte Argumentsyntax angezeigt.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Verwenden von durch Leerzeichen getrennten Argumenten im Bereich "Formatvorlagen"" lightbox="../../media/2020/05/color.msft.png":::
  Verwenden von durch Leerzeichen getrennten Argumenten im Bereich **"Formatvorlagen"**  
:::image-end:::  

Sie sollten auch die Syntax im **Bereich "Berechnet"** und in der QuickInfo zum **Prüfen des Modus** anzeigen.  

Microsoft Edge DevTools verwendet die neue Syntax, da anstehende CSS-Features wie [color()][CSSWGDraftsColor4Property] die veraltete Syntax von durch Kommas getrennten Argumenten nicht unterstützen.  

Die Durch Leerzeichen getrennte Argumentsyntax wird in den meisten Browsern seit einer Weile unterstützt.  Navigieren Sie für weitere Informationen zu ["Kann ich folgendes verwenden: Durch Leerzeichen getrennte funktionale Farbschreibweise"?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]  

Chromium Problem [#1072952][CR1072952]  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a>Veralteter Eigenschaftenbereich im Elementbereich  

Der **Eigenschaftenbereich** **im** Elementtool ist veraltet.  Führen Sie `console.dir($0)` stattdessen in der **Konsole** aus.  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Der veraltete Eigenschaftenbereich" lightbox="../../media/2020/05/properties.msft.png":::
   Der veraltete **Eigenschaftenbereich**  
:::image-end:::  

#### <a name="references"></a>Verweise  

*   [console.dir()][DevtoolsConsoleApiDir]  
*   [0 USD][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a>Unterstützung von App-Verknüpfungen im Manifestbereich  

App-Verknüpfungen helfen Benutzern, allgemeine oder empfohlene Aufgaben innerhalb einer Web-App schnell zu starten.  Das Kontextmenü der App wird nur für [Progressive Web Apps][PwaIndex] angezeigt, die auf dem Desktop oder mobilen Gerät des Benutzers installiert sind.  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="App-Verknüpfungen im Manifestbereich" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  App-Verknüpfungen im **Manifestbereich**  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie Windows oder macOS verwenden, sollten Sie die [Microsoft Edge Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Kontakt mit Microsoft Edge Devtools-Team aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

<!--[DevtoolsWhatsNew201901Inspect]: ../../../whats-new/2019/01/devtools.md#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[DevtoolsConsoleApiDir]: ../../../console/api.md#dir "dir – Konsolen-API-Referenz | Microsoft-Dokumente"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]: ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Kürzlich ausgewähltes Element oder JavaScript-Objekt – Api-Referenz für Konsolenprogramme | Microsoft-Dokumente"  
[DevtoolsCssReferenceColorPicker]: ../../../css/reference.md#change-colors-with-the-color-picker "Ändern von Farben mit der Farbauswahl – CSS-Verweis | Microsoft-Dokumente"  
[DevtoolsDrawer]: ../../../customize/index.md#drawer "Schublade – Anpassen der Übersicht | Microsoft-Dokumente"  
[DevtoolsIndex]: ../../../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Suchen und Beheben von Problemen mit der Registerkarte &quot;Microsoft Edge DevTools-Probleme&quot; | Microsoft-Dokumente"  
[DevtoolsNetworkDetails]: ../../../network/index.md#inspect-the-details-of-the-resource "Überprüfen Sie die Details der Ressource | Microsoft-Dokumente"  
[DevtoolsNetworkLog]: ../../../network/index.md#log-network-activity "Protokollieren der | der Netzwerkaktivität Microsoft-Dokumente"  
[DevtoolsRemoteDebugAndroid]: ../../../remote-debugging/index.md "Erste Schritte mit Remotedebugging für Android-Geräte | Microsoft-Dokumente"  
[DevtoolsRemoteDebugDuoEmulator]: ../../../remote-debugging/surface-duo-emulator.md "Erste Schritte mit Surface Duo-Remotedebugging-Emulatoren | Microsoft-Dokumente"  
[DevtoolsRemoteDebugWindows]: ../../../remote-debugging/windows.md "Erste Schritte mit Remotedebugging Windows 10 Geräte | Microsoft-Dokumente"  

[PwaIndex]: ../../../../progressive-web-apps-chromium/index.md "Progressive Web-Apps unter Windows | Microsoft Docs"  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface Duo-Emulators | Microsoft-Dokumente"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge Android-App"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Durch Leerzeichen getrennte funktionale Farbschreibweise – MDN-| Kann ich verwenden?"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"

[CR174309]: https://crbug.com/174309 "DevTools: Anpassen von Tastenkombinationen/Tastenbindungen | Chromium Fehler"  
[CR963183]: https://crbug.com/963183 "DevTools sind nicht WCAG-konform | Chromium Fehler"  
[CR1040019]: https://crbug.com/1040019 "DevTools: Einfache Vorschau von Bildern und Hintergrundbildern im Bereich &quot;Formatvorlagen&quot; | Chromium Fehler"  
[CR1040025]: https://crbug.com/1040025 "DevTools: Zeigen Sie grundlegende a11y-Informationen im Elementpopover | Chromium Fehler"  
[CR1048378]: https://crbug.com/1048378 "DevTools-Ui-Unterstützung für den Modus &quot;Hoher Kontrast&quot; | Chromium Fehler"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Chromium Fehler"  
[CR1068116]: https://crbug.com/1068116 "Bereich &quot;Versandprobleme&quot; | Chromium Fehler"  
[CR1072952]: https://crbug.com/1072952 "DevTools: Farbauswahl sollte moderne CSS-Farbsyntax | Chromium Fehler"  
[CR1075437]: https://crbug.com/1075437 "DevTools: Fügen Sie Unterstützung für das CSS-Schlüsselwort/den Wert | Chromium Fehler"  
[CR1076112]: https://crbug.com/1076112 "Devtools-Personalisierung – Schubladen-Resizer"  
[CR1081486]: https://crbug.com/1081486 "Tastaturfokus für Navigationsschaltflächen im Screencastmodus nicht sichtbar | Chromium Fehler"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus sollte &quot;erfüllt&quot; und nicht &quot;aufgelöst&quot; | V8-Fehler"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Änderungen von Farben 3 – CSS-Farbmodul Ebene 4 | W3C-CSS-Arbeitsgruppen-Editor-Entwürfe"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Vordergrundfarbe: die &quot;Farbe&quot; – CSS-Farbmodul Ebene 4 | W3C-CSS-Arbeitsgruppen-Editor-Entwürfe"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Einführung in die neue Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Zustände und Zustände – domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "revertieren | Mdn"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Browserkompatibilität | Mdn"  

[VisualStudioCodeMain]: https://code.visualstudio.com/ "Visual Studio Code"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Tastenkombinationen für Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axt: Tastatur| WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axt: Name Role Value | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Aktivieren oder Deaktivieren des Modus für hohen Kontrast in Windows | Windows Unterstützung"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Posten eines Tweets"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools Twitter-Konto"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Neues Problem – MicrosoftDocs/Edge-Entwickler"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Vorschaukanäle"  
[TheWebWeWantMain]: https://aka.ms/webwewant "The Web We Want"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite ist [hier](https://developer.chrome.com/blog/new-in-devtools-84) zu finden und wurde von [Kaince Baskisch][KayceBasques] \(Technical Writer, Chrome DevTools \& Ausrufebereich\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
