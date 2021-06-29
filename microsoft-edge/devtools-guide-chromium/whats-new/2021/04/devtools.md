---
description: Wavy underlines highlight code issues in the Elements tool, Service worker update timeline, and more.
title: Neuigkeiten in DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 69fcd29f9b4cae9ec290798b767fbe54793cb2fd
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624780"
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
# <a name="whats-new-in-devtools-microsoft-edge-91"></a>Neuigkeiten in DevTools (Microsoft Edge 91)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a>Wellenförmige Unterstreichungen heben Codeprobleme und Verbesserungen im Elementtool hervor  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

In den meisten modernen IDEs weisen wellenförmige Unterstreichungen unter Text auf Syntaxfehler hin.   In Microsoft Edge Version 91 oder höher werden wellenförmige Unterstreichungen in der **DOM-Ansicht** des **Elements-Tools** unter HTML angezeigt.  Die wellenförmigen Unterstreichungen deuten auf Codeprobleme und Vorschläge im Zusammenhang mit Barrierefreiheit, Kompatibilität, Leistung usw. hin.  For more information about how to review and edit issues, navigate to [Find and fix problems using the Issues tool][DevtoolsIssuesIndex].  

Führen Sie eine der folgenden Aktionen aus, um das Tool **"Probleme"** zu öffnen und mehr über das Problem und dessen Behebung zu erfahren.  

*   Wählen Sie "Halten" `Shift` aus, und wählen Sie dann eine beliebige wellenförmige Unterstreichung aus.  
*   Führen Sie die folgenden Aktionen aus.  
    1.  Zeigen Sie auf eine beliebige wellenförmige Unterstreichung.  
    1.  Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).  
    1.  Wählen Sie **"In Problemen anzeigen"** aus.  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Auswählen des unterstrichenen Fehlers im Elementtool" lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         Auswählen des unterstrichenen Fehlers im **Elementtool**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Anzeigen von Fehlerdetails im Tool "Probleme"" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         Anzeigen von Fehlerdetails im **Tool "Probleme"**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Mehr über DevTools mit informativen QuickInfos erfahren  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

Die DevTools-QuickInfos-Funktion hilft Ihnen, sich über alle verschiedenen Tools und Bereiche in DevTools zu informieren.  Um QuickInfos zu deaktivieren, wählen Sie `Esc` .  Führen Sie eine der folgenden Aktionen aus, um QuickInfos zu aktivieren.  

*   Wählen Sie `Ctrl` + `Shift` + `H` \(Windows/Linux\) oder `Cmd` + `Shift` + `H` \(macOS\) aus.  
*   [Öffnen Sie das Befehlsmenü,][DevtoolsCommandMenuIndexOpenCommandMenu] und geben Sie dann `tooltips` .  
*   Choose **Customize and control DevTools** \( `...` \) > **Help**  >  **Toggle the DevTools Tooltips**.  

Wenn Sie außerdem das Experiment ["Fokusmodus" und "DevTools-QuickInfos"][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] aktivieren, können Sie auch die Schaltfläche **"DevTools-QuickInfos** \( `?` \) " am unteren Rand der **Aktivitätsleiste**auswählen.  

Um weitere Informationen zur Verwendung der DevTools anzuzeigen, aktivieren Sie QuickInfos, und zeigen Sie dann auf die einzelnen umrissenen Regionen der DevTools.  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des Tools "Probleme", um weitere Details anzuzeigen." lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des **Tools "Probleme",** um weitere Details anzuzeigen.  
:::image-end:::  

## <a name="service-worker-update-timeline"></a>Zeitachse für Dienstmitarbeiteraktualisierungen  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

Zeigen Sie in Microsoft Edge Version 91 oder höher, wenn Sie Progressive Web App- oder Service Worker-Entwickler sind, den Updatelebenszyklus Ihrer Service Worker als Zeitachse im **Anwendungstool** an.  Dieses Feature hilft Ihnen, die Zeit zu verstehen, die Ihr Service Worker in den einzelnen folgenden Phasen verbringt.  

*   **Installieren**  
*   **Warte**  
*   **Aktivieren**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Überprüfen der Zeitachse im Updatezyklus für Den Service Worker" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   Überprüfen der **Zeitachse** im **Updatezyklus** für Den Service Worker  
:::image-end:::  

For more information about the lifecycle of your Service Workers, navigate to [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].  For more information about debugging tools for Progressive Web Apps and Service Workers in the DevTools, navigate to [Service Worker improvements][DevtoolsServiceWorkerIndex].  Navigieren Sie zu Problem [1066604,][CR1066604]um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a>Progressive Web Apps zeigen keine Warnungen mehr für nicht quadratische Symbole an  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

Wenn [in Microsoft Edge Version 90][DevtoolsWhatsNew202102Devtools] oder früheren Versionen des Web App-Manifests Ihrer PWA ein nicht quadratisches Symbol enthalten war, wurde im Abschnitt **"Fehler und Warnungen"** für jedes nicht quadratische Symbol eine Warnung angezeigt.  In Microsoft Edge Version 91 oder höher zeigt der **Manifestabschnitt** im **Anwendungstool** keine Warnungen an, wenn Sie mindestens ein quadratisches Symbol bereitstellen.  Wenn Sie keine quadratischen Symbole angeben, wird die folgende Meldung mit einer Warnung angezeigt.  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 90 oder früheren Versionen wird für jedes Nicht-Quadrat-Symbol ein Fehler angezeigt." lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         In Microsoft Edge Version 90 oder früheren Versionen wird für jedes Nicht-Quadrat-Symbol ein Fehler angezeigt.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein Quadratsymbol bereitstellen." lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein Quadratsymbol bereitstellen.  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Navigieren Sie zum Überprüfen von Fehlern und Warnungen im Web App-Manifest zum **Anwendungstool,** und wählen Sie den Abschnitt **"Manifest"** aus.  Fehler und Warnungen werden unter der Überschrift **"Fehler und Warnungen"** aufgeführt.  For more information about the Web App Manifest, navigate to [Use the Web App Manifest to integrate your Progressive Web App into the Operating System][ProgressiveWebAppsWebappmanifests].  Navigieren Sie zum [PWABuilder Image Generator,][PwabuilderImagegenerator]um Symbole zu erstellen, die in Ihr Web App-Manifest aufgenommen werden sollen.  Navigieren Sie zu Problem [1185945][CR1185945], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a>Lokalisierte DevTools jetzt in Chromium-basierten Browsern unterstützt  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

Ab [Microsoft Edge Version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]wird Microsoft Edge DevTools in Ihrer eigenen Sprache angezeigt.  Viele Entwickler verwenden andere Entwicklertools wie StackOverflow und Visual Studio Code in ihrer Sprache, nicht nur in Englisch.  Das Microsoft Edge DevTools-Team, das Chrome DevTools-Team und das Google-Dropdown-Team haben zusammengearbeitet, um die gleiche Oberfläche in allen Chromium-basierten Browsern bereitzustellen.  For more information about how to use DevTools in your language, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].  For more information about the collaboration on this feature in the Chromium open-source project, navigate to [1136655][CR1136655].  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge Browser und DevTools auf Japanisch festgelegt" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   Microsoft Edge Browser und DevTools auf Japanisch festgelegt  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a>Verwenden der Tastatur zum Navigieren zu CSS-Variablen  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

Ab [Microsoft Edge Version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]zeigt der Bereich **Formatvorlagen** CSS-Variablen an und stellt einen Link direkt zur Definition der einzelnen Variablen bereit.  In Microsoft Edge Version 91 oder höher können Sie mithilfe der Pfeiltasten ganz einfach zu CSS-Variablen navigieren.  Zeigen Sie auf eine Variable, und wählen Sie dann aus, um die Definition im Bereich **"Formatvorlagen"** zu `Enter` öffnen.  Weitere Informationen zu CSS-Variablen erhalten Sie, indem Sie zu [benutzerdefinierten CSS-Eigenschaften (Variablen)][MdnDocsWebCssUsingCssCustomProperties]navigieren.  Navigieren Sie zu Problem [1187735][CR1187735], um Echtzeitupdates für dieses Feature im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Die CSS-Variable "-theme-body-background" im Bereich "Formatvorlagen"" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   Die `--theme-body-background` im Bereich **"Formatvorlagen"** hervorgehobene CSS-Variable  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a>Probleme werden automatisch nach Schweregrad sortiert.  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

Das **Tool "Probleme"** zeigt Empfehlungen zur Verbesserung Ihrer Website an, einschließlich Barrierefreiheit, Leistung, Sicherheit usw. Basierend auf Ihrem Feedback werden die Probleme jetzt automatisch nach Schweregrad sortiert.  In jeder Feedbackkategorie wird jedes als **Fehler** gekennzeichnete Problem zuerst angezeigt, gefolgt von jedem Problem, das als **Warnung**gekennzeichnet ist, und dann jedem Problem, das als **Tipp**gekennzeichnet ist.  Um Ihre Probleme zu verfeinern, sind zusätzliche Filteroptionen für ein zukünftiges Update geplant.  For more information about how to review issues, navigate to [Find and fix problems using the Issues tool][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="Das Tool "Probleme" zeigt sortierte Probleme nach Schweregrad an." lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   Das Tool **"Probleme"** zeigt sortierte Probleme nach Schweregrad an.  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a>Microsoft Edge Entwicklertools für Visual Studio Code Version 1.1.7  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

The [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 provides the DevTools from Microsoft Edge version [88][DevtoolsWhatsNew202011Devtools].  Diese Erweiterung unterstützt jetzt ARM-Geräte und ist nicht mehr vom [Debugger für Microsoft Edge-Erweiterung][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] abhängig.  Version 1.1.7 enthält die folgenden Fehlerbehebungen und Verbesserungen.  

*   Die Zuverlässigkeit des Schließens des Ziels wurde aktualisiert.  
*   Der Seitenbereich wurde so aktualisiert, dass er automatisch aktualisiert wird, wenn Sie Ziele debuggen, die erstellt oder zerstört werden.  
*   Ein neues Kontextmenü wurde hinzugefügt, mit dem Sie schneller auf die Erweiterungseinstellungen und das neueste Changelog zugreifen können.  
*   Die Veröffentlichung der Erweiterungsdokumentation einschließlich der neuesten Features wurde aktualisiert und vereinfacht.  
    
Um die Version 1.1.7 manuell zu aktualisieren, navigieren Sie manuell zu ["Erweiterung aktualisieren".][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Sie können Probleme melden und zur Erweiterung im [vscode-edge-devtools GitHub-Repository][GithubMicrosoftVscodeEdgeDevtools] mitwirken.  

## <a name="announcements-from-the-chromium-project"></a>Ankündigungen aus dem Chromium-Projekt  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="visualize-css-scroll-snap"></a>Visualisieren des CSS-Bildlauf-Snaps  

Sie können nun das `scroll-snap` Signal im **Elementtool** umschalten, um die CSS-Bildlauf-Snap-Ausrichtung zu überprüfen.  Wenn ein HTML-Element auf Ihrer Webseite `scroll-snap-type` darauf angewendet wurde, wird ein `scroll-snap` Signal daneben im **Elementtool** angezeigt.  Wählen Sie das Signal aus, um die Anzeige einer Bildlauf-Snap-Überlagerung auf der Webseite zu aktivieren (oder zu deaktivieren).  Um eine Beispielwebseite zu überprüfen, navigieren Sie zu [Scroll Snap Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].  Im Beispiel werden Punkte an Andockkanten angezeigt.  Der Bildlaufport weist eine durchgezogene Kontur auf, während die Andockelemente Strichumrisse aufweisen.  Der Bildlaufabstand ist grün gefüllt, während der Bildlaufrand orangefarben gefüllt ist.  Navigieren Sie zu Problem [862450,][CR862450]um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/elements-scroll-snap-highlight.msft.png" alt-text="CSS-Bildlauf-Snap" lightbox="../../media/2021/04/elements-scroll-snap-highlight.msft.png":::
   CSS-Bildlauf-Snap  
:::image-end:::  

### <a name="new-memory-inspector-tool"></a>Neues Speicherprüfungstool  

Verwenden Sie das neue **Speicherprüfungstool,** um einen `ArrayBuffer` Speicher in JavaScript und Wasm zu überprüfen.  Öffnen Sie die [Demowebseite "Memory in JS".][GlitchMemoryInspectorDemoJsHtml]  Öffnen Sie im **Tool "Quellen"** die `memory-write-wasm` Datei, und legen Sie einen Haltepunkt an der Zeile `0x03c` fest.  Aktualisieren Sie die Webseite.  Erweitern Sie den **Bereich** im Debuggerbereich.  Das neue Symbol wird neben dem **Pufferwert** angezeigt.  Wählen Sie ihn aus, um das neue **Speicherprüfungstool** zu öffnen.  

Um mehr über das Debuggen im **Quellentool** zu erfahren, navigieren Sie zum Debuggen von [JavaScript-Code im Bereich "Debugger".][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]  Navigieren Sie zu Problem [1166577][CR1166577][CR1166577], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png" alt-text="Speicherprüfungstool" lightbox="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png":::
   **Speicherprüfungstool**  
:::image-end:::  

### <a name="new-badge-settings-pane-in-the-elements-tool"></a>Bereich "Neue Signaleinstellungen" im Tool "Elemente"  

Verwenden Sie nun die **Badge-Einstellungen** im **Elementtool,** um einzelne Badges zu aktivieren (oder zu deaktivieren).)  Verwenden Sie dieses Feature, um wichtige Badges anzupassen und sich auf diese zu konzentrieren, während Sie Webseiten überprüfen.  Führen Sie die folgenden Aktionen aus, um den Bereich "Signaleinstellungen" oben im **Elementtool** anzuzeigen.  

1.  Zeigen Sie auf ein beliebiges Element.  
1.  Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).  
1.  Wählen Sie **Badge-Einstellungen... aus.**  
    
Um die Badges anzuzeigen (oder auszublenden),wählen Sie \(oder entfernen\) das Kontrollkästchen neben dem Signalnamen aus.  

<!--  To review the history of this feature in the Chromium open-source project, navigate to Issue [1066772][CR1066772].  -->  

:::image type="complex" source="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png" alt-text="Bereich "Signaleinstellungen" im Elementtool" lightbox="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png":::
   Bereich **"Signaleinstellungen"** **im** Elementtool  
:::image-end:::  

### <a name="enhanced-image-preview-with-aspect-ratio-information"></a>Erweiterte Bildvorschau mit Informationen zum Seitenverhältnis  

Die Bildvorschau in den DevTools wurde verbessert, um weitere Informationen anzuzeigen, einschließlich der folgenden Details.  

*   Gerenderte Größe  
*   Gerendertes Seitenverhältnis  
*   Systeminterne Größe  
*   Systeminternes Seitenverhältnis  
*   Dateigröße  
    
Die Informationen helfen Ihnen, Ihre Bilder besser zu verstehen und die Optimierung anzuwenden.  Die Informationen zum Bildseitenverhältnis sind auch im **Netzwerktool** verfügbar, wenn Sie eine Bildvorschau auswählen.  

:::row:::
   :::column span="":::
      Im Tool **"Elemente"** zeigt die Bildvorschau jetzt weitere Informationen zum Bild an.  
   :::column-end:::
   :::column span="":::
      Außerdem sind die Informationen zum Bildseitenverhältnis im **Netzwerktool** verfügbar, wenn Sie eine Bildvorschau auswählen.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png" alt-text="Bildvorschau mit Informationen zum Seitenverhältnis im Elementtool" lightbox="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png":::
         Bildvorschau mit Informationen zum Seitenverhältnis im **Elementtool**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/network-img-name-filters-preview.msft.png" alt-text="Bildseitenverhältnisinformationen im Netzwerktool" lightbox="../../media/2021/04/network-img-name-filters-preview.msft.png":::
         Bildseitenverhältnisinformationen im **Netzwerktool**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Navigieren Chromium Sie zu Problemen [1149832][CR1149832][CR1149832] und [1170656][CR1170656].  

### <a name="new-options-to-configure-content-encodings-in-the-network-conditions-tool"></a>Neue Optionen zum Konfigurieren von Inhaltscodierungen im Netzwerkbedingungentool 

Wählen Sie im **Netzwerktool** die neue Schaltfläche **"Weitere Netzwerkbedingungen...** " neben dem Dropdownmenü **"Drosselung"** aus, um das **Tool "Netzwerkbedingungen"** zu öffnen.  Führen Sie die folgenden Aktionen aus, um zu testen, ob Serverantworten korrekt für Browser codiert sind, die [gzip,][GnuSoftwareGzipManual] [brotli][|::ref1::|Main]oder eine andere Zukunft nicht `Content-Encoding` unterstützen.  

1.  Öffnen des Tools für **Netzwerkbedingungen**
1.  Navigieren Sie zu **akzeptierten Inhaltscodierungen.** 
1.  Entfernen Sie das Kontrollkästchen neben dem, das `Content-Encoding` Sie testen möchten.  
    
Navigieren Sie zu Problem [1162042][CR1162042], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png" alt-text="Neue weitere Netzwerkbedingungen... schaltfläche öffnet das Netzwerkbedingungen-Tool zum Konfigurieren der Inhaltscodierung" lightbox="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png":::
   Neue **Weitere Netzwerkbedingungen...** Schaltfläche öffnet das **Netzwerkbedingungen-Tool** zum Konfigurieren `Content-Encoding`  
:::image-end:::  

### <a name="styles-pane-enhancements"></a>Erweiterungen des Stilbereichs  

#### <a name="new-shortcut-to-display-computed-value-in-the-styles-pane"></a>Neue Verknüpfung zum Anzeigen des berechneten Werts im Bereich "Formatvorlagen"  

Führen Sie nun die folgenden Aktionen aus, um den berechneten CSS-Wert im Bereich **"Formatvorlagen"** anzuzeigen.  

1.  Zeigen Sie auf eine CSS-Eigenschaft.  
1.  Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).  
1.  Choose **View computed value**.  
    
Navigieren Sie zu Problem [1076198][CR1076198], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png" alt-text="Neue Verknüpfung zum Anzeigen des berechneten Werts" lightbox="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png":::
   Neue Verknüpfung zum Anzeigen des berechneten Werts  
:::image-end:::  

#### <a name="support-for-the-accent-color-keyword"></a>Unterstützung für das Schlüsselwort Akzentfarbe  

Die Benutzeroberfläche für automatisches Vervollständigen des Bereichs **"Formatvorlagen"** erkennt nun das `accent-color` CSS-Schlüsselwort, mit dem Sie die Akzentfarbe für ui-Steuerelemente angeben können, die vom Element generiert werden.  Beispiele für UI-Steuerelemente, die von einem Element generiert werden, sind Kontrollkästchen oder Optionsfelder. For more information about the status of the Chromium implementation, navigate to [Feature: accent-color CSS property][ChromestatusFeature4752739957473280].  Um dieses Feature zu aktivieren, navigieren Sie zu `edge://flags#enable-experimental-web-platform-features` "Aktiviert", und legen Sie das Kontrollkästchen auf **"Aktiviert"** fest.  Navigieren Sie zu Problem [1092093][CR1092093], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/elements-styles-accent-color.msft.png" alt-text="CSS-Schlüsselwort für Akzentfarbe" lightbox="../../media/2021/04/elements-styles-accent-color.msft.png":::
   `accent-color` CSS-Schlüsselwort
:::image-end:::  

### <a name="display-details-about-blocked-features-in-the-frame-details-view"></a>Anzeigen von Details zu blockierten Features in der Frame-Detailansicht  

Die Berechtigungsrichtlinie ist eine Webplattform-API, die einer Website die Möglichkeit gibt, die Verwendung von Browserfeatures in einem einzelnen Frame oder in einem eingebetteten Frame zuzulassen oder zu `iframe` blockieren. Weitere Informationen finden Sie unter [Berechtigungsrichtlinienerklärer.][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]  Führen Sie die folgenden Aktionen aus, um die Gründe für die Blockierfunktion anzuzeigen.  

1.  Navigieren Sie zur [OOPIF-Berechtigungsrichtlinie.][GlitchPermissionPolicyDemoMain]  
1.  Navigieren Sie zum **Anwendungstool.**  
1.  Wählen Sie einen Frame aus.  
1.  Navigieren Sie zum Abschnitt **"Berechtigungsrichtlinie".**  
1.  Navigieren Sie zur Eigenschaft **"Deaktivierte Features".**  
1.  Wählen Sie **"Details anzeigen"** aus.  
1.  Wählen Sie das Symbol neben jeder Richtlinie aus, um zu der oder der Netzwerkanforderung zu `iframe` navigieren, die das Feature blockiert hat.  
    
Navigieren Sie zu Problem [1158827][CR1158827], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png" alt-text="Blockierte Features in der Frame-Detailansicht" lightbox="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png":::
   Blockierte Features in der Frame-Detailansicht  
:::image-end:::  

### <a name="filter-experiments-in-the-experiments-setting"></a>Filtern von Experimenten in der Einstellung "Experimente"  

Suchen Sie Experimente schneller mit dem neuen Experimentfilter.  Führen Sie beispielsweise die folgenden Aktionen aus, um neue Experimente für Codeprobleme zu aktivieren.
``

1.  Navigieren Sie zu **Einstellungen**  >  **Experiments**.  
1.  Navigieren Sie zum Textfeld ** Filter .**  
1.  Geben Sie `issues` ein.  
    
:::image type="complex" source="../../media/2021/04/settings-experiments-filter-by-issues.msft.png" alt-text="Filtern von Experimenten in der Einstellung "Experimente"" lightbox="../../media/2021/04/settings-experiments-filter-by-issues.msft.png":::
   Filtern von Experimenten in der Einstellung **"Experimente"**  
:::image-end:::  

### <a name="new-vary-header-column-in-the-cache-storage-pane"></a>Neue Spalte "Kopfzeile variieren" im Speicherbereich "Cache"  

Verwenden Sie die neue `Vary Header` Spalte im **Bereich "Cache Storage",** um die Werte der [Vary][HttpwgSpecsRfc7231HtmlHeaderVary] HTTP-Antwortheader anzuzeigen.  Navigieren Sie zu Problem [1186049][CR1186049], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png" alt-text="Spalte "Kopfzeile variieren"" lightbox="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png":::
   Spalte "Kopfzeile variieren"  
:::image-end:::  

### <a name="sources-tool-improvements"></a>Verbesserungen am Tool "Quellen"  

#### <a name="support-for-new-javascript-features"></a>Unterstützung für neue JavaScript-Features  

DevTools unterstützt jetzt die neue [Private Marke checks a.k.a. #foo in obj][V8DevFeaturesPrivateBrandChecks] JavaScript language feature.  Das Feature "Überprüfungen privater Marken" erweitert den [Operator "in",][MdnDocsWebJavascriptReferenceOperatorsIn] um [Felder der privaten Klasse][V8DevFeaturesClassFieldsPrivateClassFields] für ein bestimmtes Objekt zu unterstützen.  Probieren Sie es in den **Konsolen-** und **Quellentools** aus.  Führen Sie außerdem die folgenden Aktionen aus, um die privaten Felder zu überprüfen.  

1.  Navigieren Sie zum **Debuggerbereich.**  
1.  Navigieren Sie zum **Bereichsbereich.**  
    
Navigieren Sie zu Problem [11374,][CR11374]um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png" alt-text="JavaScript Private Brand Checks" lightbox="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png":::
   JavaScript Private Brand Checks  
:::image-end:::  

#### <a name="enhanced-support-for-breakpoints-debugging"></a>Erweiterte Unterstützung für das Debuggen von Haltepunkten  

Moderne JavaScript-Bundler wie [Webpack][WebpackJsMain]und [Rollup][RollupjsMain] unterstützen die Codeteilung.  Um mehr über das Teilen von Code zu erfahren, navigieren Sie zum [Codetrennen.][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]  In Microsoft Edge Version 90 oder früheren Versionen legen DevTools nur Haltepunkte in einem einzigen Bündel fest.  In Microsoft Edge Version 91 oder höher legt DevTools beim Debuggen einer freigegebenen Komponente Haltepunkte in mehreren Bundles fest.  Navigieren Sie zu Problemen [1142705][CR1142705], [979000][CR979000]und [1180794][CR1180794], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

#### <a name="support-hover-preview-with-bracket-notation"></a>Unterstützung der Hovervorschau mit Klammer-Notation  

DevTools unterstützt jetzt die Hovervorschau für JavaScript-Memberausdrücke, die die `[]` Notation im **Tool "Quellen"** verwenden.  Navigieren Sie zu Problem [1178305][CR1178305], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png" alt-text="Unterstützung der Hovervorschau mit [] Notation" lightbox="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png":::
   Unterstützung der Hovervorschau mit `[]` Notation  
:::image-end:::  

#### <a name="improved-outline-of-html-files"></a>Verbesserte Gliederung von HTML-Dateien  

DevTools bietet jetzt eine bessere Gliederungsunterstützung für `.html` Dateien.  Öffnen Sie im **Tool "Quellen"** die `.html` Datei.  Um die Codegliederung zu aktivieren (oder zu deaktivieren), wählen Sie `Ctrl` + `Shift` + `O` Windows/Linux oder `Cmd` + `Shift` + `O` macOS aus.  In der folgenden Abbildung listen DevTools nun alle Funktionen in der Gliederung ordnungsgemäß auf.  Bisher wurden von DevTools nur einige der Funktionen angezeigt.  Navigieren Sie zu Problemen [761019][CR761019] und [1191465][CR1191465], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/sources-page-jobobbx-at.msft.png" alt-text=" Verbesserte Gliederung von HTML-Dateien" lightbox="../../media/2021/04/sources-page-jobobbx-at.msft.png":::
   Verbesserte Gliederung von HTML-Dateien  
:::image-end:::  

#### <a name="proper-error-stack-traces-for-wasm-debugging"></a>Ordnungsgemäße Fehlerstapelüberwachungen für wasm-Debugging  

In Microsoft Edge Version 90 oder früher wurden in DevTools nur generische Wasm-Verweise in Fehlerstapelablaufverfolgungen angezeigt.  In Microsoft Edge Version 91 oder höher löst DevTools Inlinefunktionsanforderungen auf und zeigt den Quellspeicherort in Fehlerstapelablaufverfolgungen für das Wasm-Debuggen an.  Um mehr über Fehlerstapelablaufverfolgungen in der **Konsole**zu erfahren, navigieren Sie zu ["Fehler".][DevtoolsConsoleApiError]  

In Microsoft Edge Version 91 oder höher löst DevTools Inlinefunktionsanforderungen auf und zeigt die richtigen Fehlerstapelüberwachungen für das Wasm-Debuggen an.  

:::row:::
   :::column span="":::
      In Microsoft Edge Version 90 und früheren Versionen wird der Quellspeicherort im Fehlerstapelablaufverfolgungen nicht angezeigt.  Quellspeicherorte sind `dsquare` .  
   :::column-end:::
   :::column span="":::
      In Microsoft Edge Version 91 und höher wird der Quellspeicherort im Fehlerstapelablaufverfolgungen angezeigt.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png" alt-text="Vorherige Fehlerstapelüberwachungen für wasm-Debugging" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png":::
         Ordnungsgemäße Fehlerstapelüberwachungen für wasm-Debugging  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png" alt-text="Ordnungsgemäße Fehlerstapelüberwachungen für wasm-Debugging" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png":::
         Ordnungsgemäße Fehlerstapelüberwachungen für wasm-Debugging  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Navigieren Sie zu Problem [1189161][CR1189161], um den Verlauf dieses Features im Chromium Open-Source-Projekt zu überprüfen.  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Verwenden der DevTools in anderen Sprachen – Neuigkeiten in DevTools (Microsoft Edge 81) | Microsoft-Dokumente"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Neuigkeiten in DevTools (Microsoft Edge 88) | Microsoft-Dokumente"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: ../../2020/11/devtools.md#css-variable-definitions-in-styles-pane "CSS-Variablendefinitionen im Bereich &quot;Formatvorlagen&quot; – Neuigkeiten in DevTools (Microsoft Edge 88) | Microsoft-Dokumente"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Neuigkeiten in DevTools (Microsoft Edge 90) | Microsoft-Dokumente"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Gruppieren von Tools im Fokusmodus – Neuigkeiten in DevTools (Microsoft Edge 90) | Microsoft-Dokumente"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: ../../../command-menu/index.md#open-the-command-menu "Öffnen des Befehlsmenüs – Ausführen von Befehlen mit dem Befehlsmenü Microsoft Edge DevTools | Microsoft-Dokumente"  
[DevtoolsConsoleApiError]: ../../../console/api.md#error "error – Konsolen-API-Referenz | Microsoft-Dokumente"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Ändern der DevTools-Spracheinstellungen | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Suchen und Beheben von Problemen mithilfe des Tools &quot;Probleme&quot; | Microsoft-Dokumente"  
[DevtoolsServiceWorkerIndex]: ../../../service-workers/index.md "Verbesserungen für Service Worker | Microsoft-Dokumente"  
[DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]: ../../../sources/index.md#using-the-debugger-pane-to-debug-javascript-code "Verwenden des Debuggerbereichs zum Debuggen von JavaScript-Code – Übersicht über das Quellentool | Microsoft-Dokumente"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: ../../../../progressive-web-apps-chromium/serviceworker.md#the-service-worker-lifecycle "Service Worker-Lebenszyklus – Verwenden von Service Workern zum Verwalten von Netzwerkanforderungen und Pushbenachrichtigungen | Microsoft-Dokumente"  
[ProgressiveWebAppsWebappmanifests]: ../../../../progressive-web-apps-chromium/webappmanifests.md "Verwenden Sie das Web App-Manifest, um Ihre progressive Web App in das Betriebssystem | Microsoft-Dokumente"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

[BrotliMain]: https://www.brotli.org "Brotli"  

[ChromestatusFeature4752739957473280]: https://chromestatus.com/feature/4752739957473280 "Feature: CSS-Eigenschaft mit Akzentfarbe | Chrome Platform Status"  

[CsswgDraftsCssUi4WidgetAccent]: https://drafts.csswg.org/css-ui-4/#widget-accent "Widget-Akzentfarben: die Akzentfarbeneigenschaft – CSS Basic User Interface Module Level 4 | Entwürfe des CSS-Arbeitsgruppen-Editors"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  
[CR11374]: https://crbug.com/v8/11374 "Problem 11374: Implementieren der überprüfung der marke für private Felder"  
[CR761019]: https://crbug.com/761019 "Problem 761019: &quot;Zum Symbol wechseln&quot; verpasst die erste Funktion und bevorzugt eine schlechtere Übereinstimmung, wenn sie alle typisierten Zeichen enthält."  
[CR862450]: https://crbug.com/862450 "Problem 862450: [css-scroll-snap] Erwägen Sie das Hinzufügen des Devtools-Features für css-Bildlauf-Snap"  
[CR979000]: https://crbug.com/979000 "Problem 979000: Quellzuordnungen mit kollidierenden Quellenpfaden funktionieren nicht."  
[CR1066604]: https://crbug.com/1066604 "Problem 1066604: DevTools: Details zur Installation und Aktivierung von ServiceWorker-Ereignissen | Chromium Fehler"  
<!--  [CR1066772]: https://crbug.com/1066772 "Issue 1066772: "  locked  -->  
[CR1076198]: https://crbug.com/1076198 "Problem 1076198: [Featureanforderung] Springen sie von der Registerkarte zur berechneten `styles` Eigenschaft"  
[CR1092093]: https://crbug.com/1092093 "Problem 1092093: Gestalten Sie Formularsteuerelemente durch Unterstützung der CSS-Eigenschaft "Akzentfarbe" farbstilfähiger".  
[CR1136655]: https://crbug.com/1136655 "Problem 1136655: Devtools: Lokalisierung V2 | Chromium Fehler"  
[CR1142705]: https://crbug.com/1142705 "Problem 1142705: Haltepunkte funktionieren nicht mehr, wenn 2 Quellmaps bei Verwendung von Webpack auf dieselbe virtuelle Datei verweisen"  
[CR1149832]: https://crbug.com/1149832 "Problem 1149832: Featureanforderung: Bildvorschau sollte auch Dateigröße anzeigen"  
[CR1158827]: https://crbug.com/1158827 "Problem 1158827: [Berechtigungsrichtlinie] Implementieren der Devtool-Unterstützung für Berechtigungsrichtlinien"  
[CR1162042]: https://crbug.com/1162042 "Problem 1162042: DevTools: Unterstützen der Deaktivierung der gzip/brotli/jxl-Inhaltscodierung"  
[CR1166577]: https://crbug.com/1166577 "Problem 1166577: ☂️ Linear Memory Inspector 1.0"  
[CR1170656]: https://crbug.com/1170656 "Problem 1170656: Systeminternes Seitenverhältnis anzeigen"  
[CR1178305]: https://crbug.com/1178305 "Problem 1178305: Debugger zeigt den Eigenschaftswert eines indizierten Elements nicht an, wenn darauf gezeigt wird"  
[CR1180794]: https://crbug.com/1180794 "Problem 1180794: Haltepunkte funktionieren nicht mit dem Verschlusscompiler inlining optimization"  
[CR1185945]: https://crbug.com/1185945 "Problem 1185945: Manifestwarnung impliziert, dass alle Symbole quadratisch | Chromium Bugs"  
[CR1186049]: https://crbug.com/1186049 "Problem 1186049: Spalte für Vary: Header im Cache Storage Viewer"  
[CR1187735]: https://crbug.com/1187735 "Problem 1187735: Barrierefreiheit: MAS2.1.1: Tastatur: Funktion &quot;Var(.)&quot; kann nicht mithilfe der Tastatur | Chromium Fehler"  
[CR1189161]: https://crbug.com/1189161 "Problem 1189161: `new Error` Stacktraces werden nicht über ENING TRANSFORMIERT"  
[CR1191465]: https://crbug.com/1191465 "Problem 1191465: STRG+UMSCHALT+O in HTML beschädigt"  

[GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Berechtigungsrichtlinienerklärer | GitHub"  

[GlitchMemoryInspectorDemoJsHtml]: https://memory-inspector.glitch.me/demo-js.html "Arbeitsspeicher in JS-| Glitch"  
[GlitchMemoryInspectorDemoWasmHtml]: https://memory-inspector.glitch.me/demo-wasm.html "Arbeitsspeicher in Wasm | Glitch"  

[GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml]: https://microsoft-edge-chromium-devtools.glitch.me/css-dbg-stories/css-scroll-snap.html "Bildlauf-Snap-Demo | Glitch"  

[GlitchPermissionPolicyDemoMain]: http://permission-policy-demo.glitch.me "| der OOPIF-Berechtigungsrichtlinie Glitch"  

[GnuSoftwareGzipManual]: https://www.gnu.org/software/gzip/manual "gzip: das Datenkomprimierungsprogramm | SYSTEMS-Betriebssystem"  

[HttpwgSpecsRfc7231HtmlHeaderVary]: https://httpwg.org/specs/rfc7231.html#header.vary "Vary – Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content | IETF-HTTP-Arbeitsgruppe"  

[JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]: https://webpack.js.org/guides/code-splitting/#:~:text=There%20are%20three%20general%20approaches%20to%20code%20splitting,Split%20code%20via%20inline%20function%20calls%20within%20modules. "Es gibt drei allgemeine Ansätze für die Codeteilung: Einstiegspunkte: Manuell geteilter Code mithilfe der Eintragskonfiguration.  Duplizierung verhindern: Verwenden Sie Eintragsabhängigkeiten oder SplitChunksPlugin, um Blöcke zu deduplizieren und aufzuteilen.  Dynamische Importe: Teilen von Code über Inlinefunktionsaufrufe innerhalb von Modulen. – | der Codeaufteilung webpack"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Verwenden von benutzerdefinierten CSS-Eigenschaften (Variablen) | MDN"  

[MdnDocsWebJavascriptReferenceOperatorsIn]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/in "in Operator | Mdn"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Image Generator | PWABuilder"  

[RollupjsMain]: https://rollupjs.org "rollup.js"  

[V8DevFeaturesPrivateBrandChecks]: https://v8.dev/features/private-brand-checks "Private Marke überprüft a.k.a. #foo in obj | V8"  
[V8DevFeaturesClassFieldsPrivateClassFields]: https://v8.dev/features/class-fields#private-class-fields "Private Klassenfelder – Öffentliche und private Klassenfelder | V8"  

[WebpackJsMain]: https://webpack.js.org "webpack"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-91) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
