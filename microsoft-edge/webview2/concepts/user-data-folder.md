---
description: Informationen zum Verwalten von Benutzerdatenordnern in WebView2-Anwendungen
title: Verwalten des Benutzerdatenordners in WebView2-Anwendungen.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html, user data folder
ms.openlocfilehash: d3b3e8d81ddffec043f0988385a433eb7c817de7
ms.sourcegitcommit: 5ae09b1ad6cd576c9fec12538b23cd849861f2b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "11627957"
---
# <a name="manage-the-user-data-folder"></a>Verwalten Sie den Benutzerdatenordner  

WebView2-Anwendungen interagieren mit Benutzerdatenordnern, um Browserdaten wie Cookies, Berechtigungen und zwischengespeicherte Ressourcen zu speichern.  Jede Instanz eines WebView2-Steuerelements ist einem Benutzerdatenordner zugeordnet.  Jeder Benutzerdatenordner ist für einen Benutzer eindeutig.  

## <a name="best-practices"></a>Bewährte Methoden  

Benutzerdatenordner werden automatisch von WebView2 erstellt.  WebView2-Entwickler steuern die Lebensdauer des Benutzerdatenordners.  Wenn Ihre Anwendung Benutzerdaten aus Anwendungssitzungen erneut verwendet, sollten Sie die Benutzerdatenordner speichern, andernfalls können Sie sie löschen.  Berücksichtigen Sie die folgenden Szenarien bei der Entscheidung, wie Sie Ihre Benutzerdatenordner verwalten:  

*   Wenn derselbe Benutzer Ihre Anwendung wiederholt verwendet und der Webinhalt der Anwendung von den Daten des Benutzers abhängt, speichern Sie den Benutzerdatenordner.  Wenn ihre Anwendung mehrmals von mehreren Benutzern verwendet wird, erstellen Sie einen neuen Benutzerdatenordner für jeden neuen Benutzer, und speichern Sie den Benutzerdatenordner jedes Benutzers.
*   Wenn Ihre Anwendung keine wiederholten Benutzer hat, erstellen Sie einen neuen Benutzerdatenordner für jeden Benutzer, und löschen Sie den vorherigen Benutzerdatenordner.  
    
## <a name="create-user-data-folders"></a>Erstellen von Benutzerdatenordnern  

Um den Speicherort des Benutzerdatenordners anzugeben, schließen Sie den Parameter beim Aufrufen von `userDataFolder` [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) oder [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\) ein.  Nach der Erstellung werden Browserdaten aus Ihrem WebView2-Steuerelement in einem Unterordner von `userDataFolder` gespeichert.  Wenn `userDataFolder` nicht angegeben, erstellt WebView2 Wie folgt Benutzerdatenordner an Standardspeicherorten:  

*   Bei verpackten Windows Store Apps ist der Standardbenutzerordner der `ApplicationData\LocalFolder` Unterordner im Ordner des Pakets.  
*   Bei vorhandenen Desktop-Apps ist der Standardbenutzerdatenordner der Exe-Pfad Ihrer Anwendung + `.WebView2` .  Anstatt den Standard zu verwenden, wird empfohlen, dass Sie einen Benutzerdatenordner angeben und ihn im selben Ordner erstellen, in dem alle anderen App-Daten gespeichert sind.  
    
## <a name="delete-user-data-folders"></a>Löschen von Benutzerdatenordnern  

Ihre Anwendung muss möglicherweise Benutzerdatenordner löschen:  

*   Beim Deinstallieren Ihrer App.  Wenn Sie Windows Store Apps gepackte Apps deinstallieren, löscht Windows Benutzerdatenordner automatisch.  
*   So bereinigen Sie den gesamten Browserdatenverlauf.  
*   So stellen Sie die Datenbeschädigung wieder her.  
*   So entfernen Sie vorherige Sitzungsdaten.  
    
> [!NOTE]
> Dateien in Benutzerdatenordnern werden möglicherweise weiterhin verwendet, nachdem die WebView2-Anwendung geschlossen wurde.  Warten Sie in diesem Fall, bis der Browserprozess und alle untergeordneten Prozesse beendet werden, bevor Sie den Ordner löschen.  Sie können die Prozess-ID des Browserprozesses mithilfe der `BrowserProcessId` Eigenschaft von WebView2 abrufen.  

## <a name="share-user-data-folders"></a>Freigeben von Benutzerdatenordnern  

WebView2-Steuerelemente können dieselben Benutzerdatenordner für Folgendes freigeben:  

*   [Optimieren Sie Systemressourcen,](../concepts/process-model.md) indem Sie in einem Browserprozess ausgeführt werden.  
*   Freigeben des Browserverlaufs und zwischengespeicherter Ressourcen.  
    
Berücksichtigen Sie beim Freigeben von Benutzerdatenordnern Folgendes:  

1.  Stellen Sie beim erneuten Erstellen von WebView2-Steuerelementen zum Aktualisieren von Browserversionen mit [add_NewBrowserVersionAvailable](/microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable) \(Win32\) oder [NewBrowserVersionAvailable](/dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable) \(.NET\)-Ereignissen sicher, dass Browserprozesse WebView2-Steuerelemente beenden und schließen, die denselben Benutzerdatenordner verwenden.  Verwenden Sie die Eigenschaft des WebView2-Steuerelements, um die Prozess-ID des Browserprozesses `BrowserProcessId` abzurufen.  
1.  WebView2-Steuerelemente, die denselben Benutzerdatenordner gemeinsam verwenden, müssen die gleichen Optionen für [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) oder [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\) verwenden.  Wenn nicht, schlägt die WebView2-Erstellung mit `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` fehl.  
    
Um unterschiedliche Teile Ihrer Anwendung zu isolieren oder wenn die Freigabe von Daten zwischen WebView2-Steuerelementen nicht erforderlich ist, können Sie verschiedene Benutzerdatenordner verwenden.  Beispielsweise kann eine Anwendung aus zwei WebView2-Steuerelementen bestehen, eines zum Anzeigen einer Ankündigung und das andere zum Anzeigen von Anwendungsinhalten.  In diesem Szenario können Entwickler für jedes WebView2-Steuerelement unterschiedliche Benutzerdatenordner verwenden.  

> [!NOTE]
> Jeder WebView2-Browserprozess verbraucht zusätzlichen Arbeitsspeicher und Speicherplatz.  Daher wird empfohlen, WebView2s nicht gleichzeitig mit zu vielen unterschiedlichen Benutzerdatenordnern auszuführen.  
