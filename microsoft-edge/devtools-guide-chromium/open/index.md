---
description: Alle Möglichkeiten zum Öffnen der Microsoft Edge DevTools.
title: Öffnen Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 00bb5a2c11fcadd4a0eba22c29ac5a2652b9edb6
ms.sourcegitcommit: 2b225426e90b017f9766ea8568713b95d267cd6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2021
ms.locfileid: "11607315"
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
   limitations under the License. -->
# <a name="open-microsoft-edge-devtools"></a>Öffnen Microsoft Edge DevTools  

Es gibt viele Möglichkeiten, Microsoft Edge DevTools zu öffnen, da unterschiedliche Benutzer schnellen Zugriff auf verschiedene Teile der DevTools-Benutzeroberfläche wünschen.  

## <a name="open-the-elements-panel-to-inspect-the-dom-or-css"></a>Öffnen sie den Bereich "Elemente", um das DOM oder CSS zu überprüfen.  

Mit jeder der folgenden Aufgaben können Sie die Formatvorlagen oder Attribute eines DOM-Knotens überprüfen.

*   Zeigen Sie auf das Element, öffnen Sie das Kontextmenü \(rechtsklick\), und wählen Sie **"Überprüfen"** aus.  
*   Wählen Sie `Control` + `Shift` + `C` \(Windows, Linux\) oder `Command` + `Option` + `C` \(macOS\) aus.  Navigieren Sie für weitere Informationen zu [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]  

:::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="Die Inspect-Option" lightbox="../media/bing-right-click-inspect.msft.png":::
   Die **** Inspect-Option  
:::image-end:::  

<!--Navigate to [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <a name="open-the-console-panel"></a>Öffnen des Konsolenbereichs  

Mit jeder der folgenden Aufgaben können Sie den [Konsolenbereich][DevtoolsConsoleIndex] öffnen, um protokollierte Nachrichten anzuzeigen oder JavaScript auszuführen.  

*   Führen Sie die folgenden Schritte aus, um den [Konsolenbereich][DevtoolsConsoleIndex] zu öffnen.  
    
    1.  [Öffnen Sie DevTools](#open-microsoft-edge-devtools).  
    1.  Wählen Sie den [Konsolenbereich][DevtoolsConsoleIndex] aus.  

*   Um direkt in den [Konsolenbereich][DevtoolsConsoleIndex] zu springen, wählen Sie `Control` + `Shift` + `J` \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.  Navigieren Sie für weitere Informationen zu [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]  

<!--Navigate to [Get Started With The Console][ConsoleGetStarted].  -->

## <a name="open-the-previous-panel"></a>Öffnen des vorherigen Bereichs  

Um zum vorherigen Bereich zu wechseln, den Sie geöffnet hatten, wählen Sie `Control` + `Shift` + `I` \(Windows, Linux\) oder `Command` + `Option` + `I` \(macOS\) aus.  Navigieren Sie für weitere Informationen zu [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]  

## <a name="open-microsoft-edge-devtools"></a>Öffnen Microsoft Edge DevTools  

Um DevTools zu öffnen, verwenden Sie eine der folgenden Optionen.  

*   Verwenden Sie die Microsoft Edge Benutzeroberfläche.  
    
    1.  Wählen Sie das **Symbol Einstellungen und mehr** \( `...` \) > Weitere **Tools**  >   **Entwicklertools**aus.  
    
*   Verwenden Sie die Tastatur.  
    *   Select `F12` or `Control` + `Shift` + `I` \(Windows, Linux\) or `Command` + `Option` + `I` \(macOS\).  

Navigieren Sie für weitere Informationen zu [Microsoft Edge DevTools-Tastenkombinationen.][DevtoolsShortcutsIndex]  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Öffnen von DevTools im Microsoft Edge Hauptmenü" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Öffnen von DevTools im Microsoft Edge Hauptmenü  
:::image-end:::  

## <a name="auto-open-devtools-on-every-new-tab"></a>DevTools automatisch auf jeder neuen Registerkarte öffnen  

Öffnen Sie zum automatischen Öffnen von DevTools auf jeder neuen Registerkarte Microsoft Edge über die Befehlszeile, und übergeben Sie das `--auto-open-devtools-for-tabs` Flag.  

### [<a name="cmd-windows"></a>CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

### [<a name="powershell-windows"></a>PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

### [<a name="bash-macos"></a>bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

### [<a name="bash-linux"></a>bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## <a name="toggle-the-f12-keyboard-shortcut-on-or-off"></a>Ein- oder Ausschalten der F12-Tastenkombination  

Führen Sie die folgenden Aktionen aus, um die `F12` Tastenkombinationseinstellung zu ändern, mit der die DevTools geöffnet werden.  

1.  Navigieren Sie zu `edge://settings/system`.  
1.  Wählen Sie in `Developer Tools` DevTools **öffnen aus, wenn die F12-Taste gedrückt wird,** um die Einstellung zu deaktivieren oder zu aktivieren.  Schalten Sie die Einstellung auf "Aus", um zu verhindern, dass die `F12` Tastenkombination DevTools öffnet.  
1.  Nachdem Sie die Umschaltfläche deaktiviert haben, stellen Sie sicher, dass `F12` DevTools nicht mehr geöffnet wird.  
    
    > [!NOTE]
    > Nachdem Sie devTools beim **Drücken der F12-Taste**deaktiviert haben, führen Sie eine der folgenden Aktionen aus, um die DevTools zu öffnen.  
    > 
    > *   Wählen Sie `Ctrl` + `Shift` + `I` .  
    > *   Öffnen Sie das Kontextmenü \(Rechtsklick\) > **Überprüfen.**  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Übersicht über die Konsole | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge DevTools-Tastenkombinationen | Microsoft-Dokumente"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite ist [hier](https://developers.google.com/web/tools/chrome-devtools/open) zu finden und wurde von [Baskisch (Technical][KayceBasques] Writer, Chrome DevTools \& Ausrufebereich\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
