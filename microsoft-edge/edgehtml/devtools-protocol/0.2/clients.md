---
description: Microsoft Edge devtools Protocol, Version 0,2, unterstützt die folgenden Tooling-Clients.
title: Microsoft Edge devtools-Protokoll Version 0,2-Clients (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b471ff5a4051411fc205a269d811524c38acac72
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233639"
---
# <span data-ttu-id="a2609-103">Microsoft Edge devtools-Protokoll Version 0,2-Clients (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="a2609-103">Microsoft Edge DevTools Protocol Version 0.2 Clients (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="a2609-104">Version 0,2 des Microsoft Edge devtools-Protokolls funktioniert nur auf dem [Windows 10 October 2018-Update](/windows/uwp/whats-new/windows-10-build-17763) und später in [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) -Builds.</span><span class="sxs-lookup"><span data-stu-id="a2609-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>  

<span data-ttu-id="a2609-105">Das **devtools-Protokoll 0,2** unterstützt die folgenden Tooling-Clients.</span><span class="sxs-lookup"><span data-stu-id="a2609-105">**DevTools Protocol 0.2** supports the following tooling clients.</span></span>

<span data-ttu-id="a2609-106">[ ![ Microsoft Edge devtools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ Visual Studio-Code](../media/visual-studio-code.png)](#visual-studio-code) [ ![ Microsoft Visual Studio 15,8](../media/visual-studio-2017.png)](#microsoft-visual-studio)</span><span class="sxs-lookup"><span data-stu-id="a2609-106">[![Microsoft Edge DevTools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [![Visual Studio Code](../media/visual-studio-code.png)](#visual-studio-code) [![Microsoft Visual Studio 15.8](../media/visual-studio-2017.png)](#microsoft-visual-studio)</span></span>

## <span data-ttu-id="a2609-107">Microsoft Edge DevTools-Vorschau</span><span class="sxs-lookup"><span data-stu-id="a2609-107">Microsoft Edge DevTools Preview</span></span>

<span data-ttu-id="a2609-108">Sie können die eigenständige [**Microsoft Edge devtools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Windows 10-App aus dem Microsoft Store zum Remotedebuggen eines Hostgeräts mit Microsoft Edge ([EdgeHTML 17](../../dev-guide/index.md) oder höher) verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2609-108">You can use the standalone [**Microsoft Edge DevTools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Windows 10 app from the Microsoft Store to remotely debug a host device running Microsoft Edge ([EdgeHTML 17](../../dev-guide/index.md) or later).</span></span>

<span data-ttu-id="a2609-109">Version 0,2 des devtools-Protokolls bietet neue Domänen für das Debuggen von Stilen und Layouts sowie Konsolen-APIs sowie die in Version 0,1 eingeführten Kernskript Debugging-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a2609-109">Version 0.2 of the DevTools Protocol provides new domains for style and layout debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="a2609-110">In der Benutzeroberfläche von Edge devtools wird dadurch die Funktionalität übersetzt, die in den Panels [**Elemente**](../../devtools-guide/elements.md), [**Konsole**](../../devtools-guide/console.md) und [**Debugger**](../../devtools-guide/debugger.md) zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="a2609-110">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md) panels.</span></span> <span data-ttu-id="a2609-111">Derzeit ist das Microsoft Edge-Remotedebuggen auf Desktop Hosts mit Unterstützung für andere Windows 10-Geräte in zukünftigen Versionen limitiert.</span><span class="sxs-lookup"><span data-stu-id="a2609-111">Currently Microsoft Edge remote debugging is limited to desktop hosts, with support for other Windows 10 devices coming in future releases.</span></span>

<span data-ttu-id="a2609-112">Hier erfahren Sie, wie Sie das Remotedebuggen mit der Microsoft Edge devtools Preview-App einrichten.</span><span class="sxs-lookup"><span data-stu-id="a2609-112">Here's how to set up remote debugging with the Microsoft Edge DevTools Preview app.</span></span> <span data-ttu-id="a2609-113">Das devtools-Protokoll, Version 0,2, erfordert [Windows 10 Oktober 2018-Update](/windows/uwp/whats-new/windows-10-build-17763) oder einen späteren Windows Insider Preview-Build auf dem Hostcomputer (debugee).</span><span class="sxs-lookup"><span data-stu-id="a2609-113">The DevTools Protocol version 0.2 requires [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later Windows Insider Preview build on the host (debugee) machine.</span></span> <span data-ttu-id="a2609-114">Die Edge devtools Preview-app (auf dem Debugger-Computer verwendet) wird unter Windows 10 Version 16299 (Windows 10 Fall Creators Update, 10/2017) oder höher ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2609-114">The Edge DevTools Preview app (used on the debugger machine) will run on Windows 10 version 16299 (Windows 10 Fall Creators Update, 10/2017) or higher.</span></span>

**<span data-ttu-id="a2609-115">Auf dem Hostcomputer (debugee)...</span><span class="sxs-lookup"><span data-stu-id="a2609-115">On the host (debugee) machine...</span></span>**

1. <span data-ttu-id="a2609-116">Wenn Sie ein WLAN-Netzwerk haben, stellen Sie sicher, dass das Netzwerk entweder als " **Domäne** " oder " **Privat**" gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="a2609-116">If you're on a WiFi network, ensure the network is marked as either **Domain** or **Private**.</span></span> <span data-ttu-id="a2609-117">Sie können dies überprüfen, indem Sie die [**Windows Defender-Sicherheits Center**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) -APP öffnen, auf **Firewall & Netzwerkschutz** klicken und überprüfen, ob Ihr Netzwerk als *Domänennetzwerk* oder *privates Netzwerk*aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="a2609-117">You can verify this by opening the [**Windows Defender Security Center**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) app, clicking on **Firewall & network protection** and checking if your network is listed as a *Domain network* or *Private network*.</span></span> 

    <span data-ttu-id="a2609-118">Wenn die Liste als *öffentlich*aufgeführt ist, wechseln Sie zu **Einstellungen**  >  **Netzwerk & Internet**  >  **WLAN**, klicken Sie auf Ihr Netzwerk, und schalten Sie die Schaltfläche *Netzwerkprofil* auf **Privat**.</span><span class="sxs-lookup"><span data-stu-id="a2609-118">If its listed as *Public*, go to **Settings** > **Network & Internet** > **Wi-Fi**, click on your network and toggle the *Network profile* button to **Private**.</span></span>

2. <span data-ttu-id="a2609-119">Öffnen Sie die Systemsteuerung **für Entwickler** unter Windows- *Einstellungen* (suchen Sie nach *Entwickler* , und klicken Sie auf *Entwicklerfeatures verwenden*) und:</span><span class="sxs-lookup"><span data-stu-id="a2609-119">Open the **For developers** control panel in Windows *Settings* (search for *developer* and click on *Use developer features*), and:</span></span> 

    <span data-ttu-id="a2609-120">a.</span><span class="sxs-lookup"><span data-stu-id="a2609-120">a.</span></span> <span data-ttu-id="a2609-121">Wechseln Sie im **Entwicklermodus**.</span><span class="sxs-lookup"><span data-stu-id="a2609-121">Toggle on **Developer Mode**.</span></span> <span data-ttu-id="a2609-122">Dadurch wird das *Entwicklermodus* -Paket installiert, das Remotetools für Desktops ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a2609-122">This will install the *Developer Mode* package, enabling remote tooling for desktop.</span></span>

    <span data-ttu-id="a2609-123">b.</span><span class="sxs-lookup"><span data-stu-id="a2609-123">b.</span></span> <span data-ttu-id="a2609-124">Aktivieren des [**Geräte Portals**](/windows/uwp/debug-test-perf/device-portal) (Aktivieren der*Remote Diagnose über lokale Netzwerkverbindungen*) und **Geräteerkennung** (*machen Sie Ihr Gerät für USB-Verbindungen und Ihr lokales Netzwerk sichtbar*).</span><span class="sxs-lookup"><span data-stu-id="a2609-124">Enable [**Device Portal**](/windows/uwp/debug-test-perf/device-portal) (*Turn on remote diagnostics over local area network connections*) and **Device discovery** (*Make your device visible to USB connections and your local network*).</span></span>

    <span data-ttu-id="a2609-125">c.</span><span class="sxs-lookup"><span data-stu-id="a2609-125">c.</span></span> <span data-ttu-id="a2609-126">Aktivieren Sie die **Authentifizierung** , und geben Sie einen Benutzernamen/ein Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="a2609-126">Turn on **Authentication** and supply a username / password.</span></span>

    <span data-ttu-id="a2609-127">d.</span><span class="sxs-lookup"><span data-stu-id="a2609-127">d.</span></span> <span data-ttu-id="a2609-128">Beachten Sie, dass die IP-Adresse des Computers und der Verbindungsanschluss (50443) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a2609-128">Note the machine IP address and connection port (50443) displayed.</span></span>

3. <span data-ttu-id="a2609-129">Öffnen Sie die Registerkarten in Microsoft Edge, die Sie auf dem Clientcomputer debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="a2609-129">Open tabs in Microsoft Edge that you wish to debug from the client machine.</span></span>

**<span data-ttu-id="a2609-130">Auf dem Clientcomputer (Debugger)...</span><span class="sxs-lookup"><span data-stu-id="a2609-130">On the client (debugger) machine...</span></span>**

1.  <span data-ttu-id="a2609-131">Installieren und starten Sie die eigenständige [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) -App aus dem Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="a2609-131">Install and launch the standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app from the Microsoft Store.</span></span>

2. <span data-ttu-id="a2609-132">Öffnen Sie den Bereich **Remote** , und geben Sie den Netzwerkspeicherort (URL und Port) des Hostcomputers ein, und klicken Sie auf **verbinden**.</span><span class="sxs-lookup"><span data-stu-id="a2609-132">Open the **Remote** panel and enter the network location (URL and port) of the host machine and click **Connect**.</span></span>

3. <span data-ttu-id="a2609-133">**Installieren** Sie das Zertifikat des Hostcomputers aus dem Dialogfeld "nicht *vertrauenswürdiges Zertifikat* ", das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a2609-133">**Install** the host machine's certificate from the *Untrusted Certificate* dialog that appears.</span></span>

4. <span data-ttu-id="a2609-134">Geben Sie den Benutzernamen/das Kennwort an, den Sie für die Geräte Portal Authentifizierung festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="a2609-134">Supply the username/password you designated for Device Portal authentication.</span></span>

5. <span data-ttu-id="a2609-135">Das *Remote* Panel lädt eine Liste von debugfähigen-Seiten Zielen auf dem Hostcomputer.</span><span class="sxs-lookup"><span data-stu-id="a2609-135">The *Remote* panel will load a list of debuggable page targets on the host machine.</span></span> <span data-ttu-id="a2609-136">Wählen Sie eine aus, um mit dem Debuggen zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="a2609-136">Select one to start debugging.</span></span>

6. <span data-ttu-id="a2609-137">Verwenden Sie die Schaltfläche **Aktualisieren** , um die Liste der Remote Seiten Ziele auf dem Hostcomputer zu aktualisieren und neu zu laden.</span><span class="sxs-lookup"><span data-stu-id="a2609-137">Use the **Refresh** button to update and reload the list of remote page targets on the host machine.</span></span> <span data-ttu-id="a2609-138">Klicken Sie auf die Schaltfläche " **trennen** ", um zum Bildschirm "mit *einem Remotegerät verbinden* " zurückzukehren und an einen anderen Host anzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2609-138">Click the **Disconnect** button to return to the *Connect to a remote device* screen and attach to a different host.</span></span>

## <span data-ttu-id="a2609-139">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a2609-139">Visual Studio Code</span></span>

<span data-ttu-id="a2609-140">Mit dem [Debugger für Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) -vs-Code Erweiterung können Sie Skripts, die in Microsoft Edge ausgeführt werden, direkt in Visual Studio-Code Debuggen.</span><span class="sxs-lookup"><span data-stu-id="a2609-140">With the [Debugger for Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can debug script running in Microsoft Edge directly in Visual Studio Code.</span></span> <span data-ttu-id="a2609-141">Die Erweiterung setzt voraus, dass Sie Ihre Webanwendung von localhost aus bedienen, was Sie entweder über die Befehlszeile oder über eine [Aufgabe](https://code.visualstudio.com/docs/editor/tasks)starten können.</span><span class="sxs-lookup"><span data-stu-id="a2609-141">The extension requires you to be serving your web application from localhost, which you can start from either command-line or a [Task](https://code.visualstudio.com/docs/editor/tasks).</span></span>

<span data-ttu-id="a2609-142">Erste Schritte:</span><span class="sxs-lookup"><span data-stu-id="a2609-142">To get started:</span></span>

1. <span data-ttu-id="a2609-143">Installieren Sie den [Debugger für Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) -vs-Code Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="a2609-143">Install the [Debugger for Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension.</span></span>

2. <span data-ttu-id="a2609-144">Starten Sie vs-Code neu, öffnen Sie den Ordner, in dem sich das Projekt befindet, das Sie debuggen möchten, und legen Sie Haltepunkte im Code ab.</span><span class="sxs-lookup"><span data-stu-id="a2609-144">Restart VS Code, open the folder containing the project you wish to debug and set breakpoints in your code.</span></span>

3. <span data-ttu-id="a2609-145">Konfigurieren Sie eine localhost- [Startaufgabe](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) , um die gewünschte Seite Ihres Projekts zu öffnen: **Debug**-  >  **Add-Konfiguration.**... Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a2609-145">Configure a localhost [launch task](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) to open the desired page of your project: **Debug** > **Add Configuration...**. For example:</span></span>

    ```json
    {
        "version": "0.2.0",
        "configurations": [

            {
                "name": "Launch localhost",
                "type": "edge",
                "request": "launch",
                "url": "http://localhost/mypage.html",
                "webRoot": "${workspaceFolder}/wwwroot"
            }
        ]
    }
    ```

    <span data-ttu-id="a2609-146">[*Die Verwendung des Debuggers*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) bietet mehr Informationen zu den Startkonfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="a2609-146">[*Using the debugger*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) has more on launch configuration settings.</span></span> 

4. <span data-ttu-id="a2609-147">Starten Sie den Server auf localhost, und klicken Sie auf die Schaltfläche **Debuggen starten** (wiedergeben), oder starten Sie `F5` Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a2609-147">Start your server on localhost and press the **Start Debugging** (play) button or `F5` to launch Microsoft Edge.</span></span> <span data-ttu-id="a2609-148">Wenn ein Haltepunkt erreicht ist, brechen Sie in den vs-Code auf und können den Code von dort aus weiter prüfen und durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a2609-148">When a breakpoint is hit, you'll break into VS Code and can further inspect and step through code from there.</span></span>

<span data-ttu-id="a2609-149">Weitere Informationen finden Sie im [vs-Code-Debugger für Microsoft Edge-](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a2609-149">For more, check out the [VS Code - Debugger for Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) documentation.</span></span>

## <span data-ttu-id="a2609-150">Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a2609-150">Microsoft Visual Studio</span></span>

<span data-ttu-id="a2609-151">Mit der neuesten Version von [**Visual Studio**](https://www.visualstudio.com) (Visual Studio 15,8 oder höher), die unter [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763)ausgeführt wird, können Sie Microsoft Edge in einem beliebigen ASP.net-oder .net Core-Projekt in der IDE starten und Debuggen.</span><span class="sxs-lookup"><span data-stu-id="a2609-151">Using the latest [**Visual Studio**](https://www.visualstudio.com) version (Visual Studio 15.8 or later) running on [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763), you can launch and debug Microsoft Edge from the IDE on any ASP.NET or .NET Core project.</span></span>

<span data-ttu-id="a2609-152">Hier erfahren Sie, wie Sie Microsoft Edge-Debuggen mit Visual Studio einrichten:</span><span class="sxs-lookup"><span data-stu-id="a2609-152">Here's how to set up Microsoft Edge debugging with Visual Studio:</span></span>

1.  <span data-ttu-id="a2609-153">Installieren und starten Sie das neueste [**Visual Studio**](https://www.visualstudio.com/) (Visual Studio 15,8 oder höher).</span><span class="sxs-lookup"><span data-stu-id="a2609-153">Install and launch the latest [**Visual Studio**](https://www.visualstudio.com/) (Visual Studio 15.8 or later).</span></span>

2. <span data-ttu-id="a2609-154">Öffnen Sie ein vorhandenes ASP.net-oder .net Core-Projekt, oder erstellen Sie ein **Neues Projekt** , indem Sie eine der **Visual C#** .net-Vorlagen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2609-154">Open an existing ASP.NET or .NET Core project or **Create new project...** using one of the **Visual C#** .NET templates.</span></span>

3. <span data-ttu-id="a2609-155">Öffnen Sie im Projekt **Mappen-Explorer**die JavaScript-Dateien, die Sie debuggen möchten, und setzen Sie Haltepunkte in der IDE genauso wie bei serverseitigem Code.</span><span class="sxs-lookup"><span data-stu-id="a2609-155">In the project **Solution Explorer**, open the JavaScript files you wish to debug and set breakpoints within the IDE just as you would with server-side code.</span></span>

4. <span data-ttu-id="a2609-156">Drücken Sie `F5` zum Starten von Microsoft Edge, auf dem der devtools-Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2609-156">Press `F5` to launch Microsoft Edge running the DevTools Server.</span></span> <span data-ttu-id="a2609-157">Wenn ein Haltepunkt erreicht ist, brechen Sie in Visual Studio ab und können den Code von dort aus weiter überprüfen und durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a2609-157">When a breakpoint is hit, you'll break into Visual Studio and can further inspect and step through the code from there.</span></span>
