---
description: Erfahren Sie, wie Sie mithilfe von systemeigenem Messaging ihre Erweiterung mit einer Begleit UWP-App kommunizieren können.
title: Erweiterungen – systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, Native, Messaging, UWP
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 983ae11822edabc0f27bd6c02f9397104b082ad6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234174"
---
# <span data-ttu-id="89021-104">Systemeigenes Messaging in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="89021-104">Native messaging in Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <span data-ttu-id="89021-105">Übersicht über die native Messaging-Architektur</span><span class="sxs-lookup"><span data-stu-id="89021-105">Native messaging architecture overview</span></span>

<span data-ttu-id="89021-106">Mit dem Windows 10 Creators-Update können Microsoft Edge-Erweiterungen natives Messaging verwenden, um mit einer Companion-App für die universelle Windows-Plattform (UWP) zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="89021-106">With the Windows 10 Creators Update, Microsoft Edge extensions are able to use native messaging to communicate with a companion Universal Windows Platform (UWP) app.</span></span>  <span data-ttu-id="89021-107">Auf hoher Ebene verwenden Microsoft Edge-Erweiterungen dieselben APIs für natives Messaging wie Chrome-und Firefox-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="89021-107">At a high level, Microsoft Edge extensions use the same APIs for native messaging as Chrome and Firefox extensions.</span></span> <span data-ttu-id="89021-108">Der systemeigene Messaging-Host muss jedoch mithilfe der universellen Windows-Plattform implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="89021-108">However, the native messaging host will need to be implemented using the Universal Windows Platform.</span></span>

> [!NOTE]
> <span data-ttu-id="89021-109">Die nachstehende Methode (Herstellen einer Verbindung mit einer UWP-App über AppService) ist der einzige unterstützte Mechanismus zum Aktivieren der Kommunikation zwischen Microsoft-Edge-Erweiterungen und systemeigenen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="89021-109">The method outlined below (connecting to a UWP app via AppService) is the only supported mechanism for enabling communication between Microsoft Edge extensions and native components.</span></span> <span data-ttu-id="89021-110">Weitere Informationen dazu, wie Sie die Kommunikation mit Legacy-Win32-Komponenten aktivieren, finden Sie im Abschnitt [Hinzufügen einer Desktop Brücken Komponente](#adding-a-desktop-bridge-component) dieses Handbuchs.</span><span class="sxs-lookup"><span data-stu-id="89021-110">Please see the [Adding a Desktop Bridge component](#adding-a-desktop-bridge-component) section of this guide for more information on how to enable communication with legacy Win32 components.</span></span> 

 <span data-ttu-id="89021-111">Die native Messaging-Architektur von Microsoft Edge nutzt die vorhandene [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API als zugrunde liegende Infrastruktur für die Inter-Process Communication (IPC).</span><span class="sxs-lookup"><span data-stu-id="89021-111">Microsoft Edge's native messaging architecture leverages the existing [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API as the underlying inter-process communication (IPC) infrastructure.</span></span> <span data-ttu-id="89021-112">UWP-Apps verwenden die `AppService` API, um miteinander zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="89021-112">UWP apps use the `AppService` API to communicate with one another.</span></span> <span data-ttu-id="89021-113">Aus diesem Grund können Microsoft Edge-Erweiterungen nun mit UWP-apps kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="89021-113">Because of this, Microsoft Edge extensions can now communicate with UWP apps.</span></span>

![systemeigene Messaging Architektur](./../media/native-messaging-architecture.png)

### <span data-ttu-id="89021-115">Zeitpunkt und Zeitpunkt der Verwendung von systemeigenem Messaging</span><span class="sxs-lookup"><span data-stu-id="89021-115">When and when not to use native messaging</span></span>

<span data-ttu-id="89021-116">Systemeigene Nachrichten fügen ihrer Erweiterung eine ganz neue Ebene hinzu.</span><span class="sxs-lookup"><span data-stu-id="89021-116">Native messaging adds a whole new layer to your extension.</span></span> <span data-ttu-id="89021-117">Wenn Sie eine UWP-Begleit-App für Ihre Erweiterung implementieren, stehen Ihnen die folgenden Möglichkeiten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="89021-117">By implementing a UWP companion app for your extension, the following possibilities become available to you:</span></span>

* <span data-ttu-id="89021-118">Synchronisieren Sie Daten (z. b. Anmeldeinformationen) mit einer Begleit UWP-app.</span><span class="sxs-lookup"><span data-stu-id="89021-118">Synchronize data (e.g. credentials) with a companion UWP app.</span></span>
* <span data-ttu-id="89021-119">Implementieren Sie stärkere Verschlüsselungs-/Entschlüsselungsalgorithmen, die in Web-APIs nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="89021-119">Implement stronger encryption/decryption algorithms not available in web APIs.</span></span>
* <span data-ttu-id="89021-120">Zugriff auf Ressourcen, auf die über Web-APIs nicht zugegriffen werden kann, beispielsweise Hardware-oder USB-Geräte</span><span class="sxs-lookup"><span data-stu-id="89021-120">Access resources that are not accessible through web APIs, e.g. hardware or USB devices</span></span>

<span data-ttu-id="89021-121">Es gibt ein paar Fälle, in denen systemeigenes Messaging aufgrund von Sicherheits-oder Richtlinieneinschränkungen nicht verwendet werden kann:</span><span class="sxs-lookup"><span data-stu-id="89021-121">There are a few instances where native messaging can't be used due to security or policy restrictions:</span></span>

* <span data-ttu-id="89021-122">Ändern von Benutzereinstellungen in Microsoft Edge oder Windows, beispielsweise Ändern des Standardbrowsers oder Suchanbieters.</span><span class="sxs-lookup"><span data-stu-id="89021-122">Modifying user settings in either Microsoft Edge or Windows, e.g. changing the default browser or search provider.</span></span>
* <span data-ttu-id="89021-123">Aktionen, die gegen die Microsoft Store-Richtlinien für apps und Erweiterungen verstoßen.</span><span class="sxs-lookup"><span data-stu-id="89021-123">Actions that violate Microsoft Store policies for both apps and extensions.</span></span>
* <span data-ttu-id="89021-124">Übertragen von Daten an den Remoteendpunkt über den systemeigenen Nachrichten Host</span><span class="sxs-lookup"><span data-stu-id="89021-124">Transferring data to remote endpoint via native message host.</span></span>
* <span data-ttu-id="89021-125">Zulassen, dass andere apps Inhalte herunterladen, die das Erweiterungs Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="89021-125">Allowing other apps to download content that changes extension behavior.</span></span>

## <span data-ttu-id="89021-126">Demos</span><span class="sxs-lookup"><span data-stu-id="89021-126">Demos</span></span>

<span data-ttu-id="89021-127">Wenn Sie sich ein Bild davon machen möchten, wie eine Microsoft Edge Native Messaging-Erweiterung mit einer Begleit UWP-APP und einer Desktop Brücke aussieht, lesen Sie die Beispiele für [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) und [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="89021-127">To get a feel for what an Microsoft Edge native messaging extension that has both a companion UWP app and a Desktop Bridge looks like, check out the [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) and [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) examples on GitHub.</span></span>

### <span data-ttu-id="89021-128">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="89021-128">How it works</span></span>

<span data-ttu-id="89021-129">Die Microsoft-Komponente "Edge Extension" des Beispiels verwendet das Inhalts Skript, um zu erkennen, wenn ein Benutzerinformationen eingibt, die verschlüsselt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="89021-129">The Microsoft Edge extension component of the sample uses its content script to detect when a user is typing in information that should be encrypted.</span></span> <span data-ttu-id="89021-130">Mit der Erweiterung wird diese über systemeigene Nachrichten an die Desktop-Bridge-Komponente kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="89021-130">The extension communicates this to the Desktop Bridge component via native messaging.</span></span> <span data-ttu-id="89021-131">Wenn der Benutzer bereit ist, die Daten zu übermitteln, gibt die Erweiterung einen verschlüsselten Wert zurück an die Website zurück.</span><span class="sxs-lookup"><span data-stu-id="89021-131">When the user is ready to submit the data, the extension will return an encrypted value back to the website.</span></span>

> [!NOTE]
> <span data-ttu-id="89021-132">Dieses Beispiel funktioniert nur auf einer Webseite, die benutzerdefinierte Ereignisse verwendet, um mit dem Inhalts Skript der Erweiterung zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="89021-132">This sample will only work on a webpage that uses custom events to communicate with the extension's content script.</span></span> <span data-ttu-id="89021-133">Der Beispielordner enthält eine [HTML-Datei](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) , mit der die Erweiterung getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89021-133">The sample folder includes a [.html file](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) to test the extension with.</span></span>

<span data-ttu-id="89021-134">In diesem Beispiel wird die UWP-App verwendet, um Antworten von der Desktop Brücke an Microsoft Edge zu übergeben, die dann per Rückruf an die Microsoft Edge-Erweiterung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="89021-134">In this example, the UWP app is used to pass responses from the Desktop Bridge to Microsoft Edge, which then gets sent to the Microsoft Edge extension via callback.</span></span> <span data-ttu-id="89021-135">Während in diesem Beispiel der systemeigene Messaging-Host in der Haupt-app ausgeführt wird, kann er auch als Hintergrundaufgabe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="89021-135">While this example has the native messaging host run in the main app, it's also able to run as a background task.</span></span> <span data-ttu-id="89021-136">Für den Wechsel zwischen den beiden muss das Hintergrundskript der Erweiterung bearbeitet werden, wobei die Zeichenfolge in in geändert wird `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` `"NativeMessagingHostOutOfProcess"` .</span><span class="sxs-lookup"><span data-stu-id="89021-136">Switching between the two requires editing the extension's background script, changing the string within `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` to `"NativeMessagingHostOutOfProcess"`.</span></span>

## <span data-ttu-id="89021-137">Chrome vs Microsoft Edge-Implementierung</span><span class="sxs-lookup"><span data-stu-id="89021-137">Chrome vs Microsoft Edge implementation</span></span>

<span data-ttu-id="89021-138">Während Chrome die Route für die Verwendung von APIs für die Nachrichtenübergabe für Ihre Erweiterungen für die Kommunikation mit Apps verwendet, nutzt Microsoft Edge die [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API, die jetzt Microsoft Edge Extensions-und UWP-Apps für die Kommunikation ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="89021-138">While Chrome goes the route of using message passing APIs for their extensions to communicate with apps, Microsoft Edge utilizes the [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API which now enables Microsoft Edge extensions and UWP apps to communicate.</span></span>

<span data-ttu-id="89021-139">In diesem Abschnitt werden die Unterschiede zwischen der Implementierung von systemeigenem Messaging durch Chrome und Microsoft Edge erläutert.</span><span class="sxs-lookup"><span data-stu-id="89021-139">This section details the differences between how Chrome and Microsoft Edge handle native messaging implementation.</span></span>

### <span data-ttu-id="89021-140">Registrierung und Host Manifest</span><span class="sxs-lookup"><span data-stu-id="89021-140">Registration and host manifest</span></span>
<span data-ttu-id="89021-141">Damit Ihre APP von ihrer Erweiterung als systemeigener Messaging-Host erkannt wird, muss Sie registriert sein.</span><span class="sxs-lookup"><span data-stu-id="89021-141">In order for your app to be recognized by your extension as a native messaging host, it will need to be registered.</span></span>

<span data-ttu-id="89021-142">Bei der [nativen Messaging](https://developer.chrome.com/extensions/nativeMessaging) -Host Registrierung von Chrome muss Ihre APP eine Manifestdatei an einer beliebigen Stelle im Windows-Dateisystem installieren, die die systemeigene Messaginghost Konfiguration definiert.</span><span class="sxs-lookup"><span data-stu-id="89021-142">For [Chrome native messaging](https://developer.chrome.com/extensions/nativeMessaging) host registration, your app needs to install a manifest file anywhere in the Windows file system that defines the native messaging host configuration.</span></span>

<span data-ttu-id="89021-143">Das folgende JSON-Beispiel zeigt, wie die Konfigurationsdatei eingerichtet werden kann:</span><span class="sxs-lookup"><span data-stu-id="89021-143">The following JSON is an example of how the config file can be set up:</span></span>

```json
{
   "name": "com.my_company.my_application",
   "description": "My Application",
   "path": "C:\\ProgramFiles\\MyApplication\\chrome_native_messaging_host.exe",
   "type": "stdio",
   "allowed_origins": [
      "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```  

<span data-ttu-id="89021-144">Um diese Datei zu installieren, muss die APP:</span><span class="sxs-lookup"><span data-stu-id="89021-144">To install this file, the app would need to:</span></span>

1.  <span data-ttu-id="89021-145">Registrieren Sie die Manifestdatei an einem vordefinierten Speicherort in der Registrierung, in dem die Hostkonfiguration definiert ist:</span><span class="sxs-lookup"><span data-stu-id="89021-145">Register the manifest file in a predefined location in the registry that defines the host configuration:</span></span>
    -   ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application
        ```  
        
        <span data-ttu-id="89021-146">oder</span><span class="sxs-lookup"><span data-stu-id="89021-146">or</span></span>
        
    -   ```text
        HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application
        ```  
        
2.  <span data-ttu-id="89021-147">Legen Sie den Standardwert für diesen Schlüssel auf den vollständigen Pfad zur Manifestdatei fest, beispielsweise</span><span class="sxs-lookup"><span data-stu-id="89021-147">Set the default value of that key to the full path to the manifest file, e.g.</span></span> 
    
    ```text
    [HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
<span data-ttu-id="89021-148">Für Microsoft Edge [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) müssen Sie die UWP-Begleit-app in das gleiche Paket wie Ihre Erweiterung einbeziehen und die [AppService-Erweiterung](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in der Projektdatei angeben, um einen (nativen Messaging-Host) registrieren zu können `Package.appxmanifest` .</span><span class="sxs-lookup"><span data-stu-id="89021-148">For Microsoft Edge, in order to register an [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx)(native messaging host) you'll need to include the UWP companion app in the same package as your extension and specify the [AppService extension](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in your project's `Package.appxmanifest` file.</span></span> <span data-ttu-id="89021-149">Die `EntryPoint` `Name` Attribute und können von Ihnen konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="89021-149">The `EntryPoint` and `Name` attributes can be configured by you:</span></span>

```xml
...
<Applications>    
    <Application Id="App"         
        <Extensions>        
            <uap:Extension Category="windows.appService" EntryPoint="MyAppService.Inventory">          
            <uap:AppService Name="com.microsoft.inventory"/>        
            </uap:Extension>      
        </Extensions>      
        ...    
    </Application>
</Applications>
```


<span data-ttu-id="89021-150">Darüber hinaus müssen Sie die Durchwahl (n) für die Verbindung mit dem Dienst einstellen.</span><span class="sxs-lookup"><span data-stu-id="89021-150">You'll also need to set which extension(s) are allowed to connect to the service.</span></span> <span data-ttu-id="89021-151">Da Microsoft Edge `"allowed_origins"` in seinen AppxManifest keine entsprechende Manifest-Eigenschaft aufweist, muss dies zur Laufzeit von der UWP-App bestimmt und erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="89021-151">Because Microsoft Edge doesn't have an equivalent `"allowed_origins"` manifest property in its AppxManifest, this will need to be determined and enforced at runtime by your UWP app.</span></span> <span data-ttu-id="89021-152">Da Microsoft Edge die Verbindung für die Erweiterung herstellt, kann die APP den Namen der paketfamilie des Anrufers nachschlagen, um festzustellen, ob Sie mit Microsoft Edge verbunden sind, um den Anrufer zu kontrollieren oder zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="89021-152">Since Microsoft Edge will be establishing the connection on behalf of the extension, the app can look up the caller's Package Family Name to determine if they're being connected by Microsoft Edge to control or authenticate the caller.</span></span> <span data-ttu-id="89021-153">z.B.</span><span class="sxs-lookup"><span data-stu-id="89021-153">E.g.</span></span> 

```csharp
protected async override void
OnBackgroundActivated(BackgroundActivatedEventArgs args)
{
    IBackgroundTaskInstance taskInstance = args.TaskInstance;
    if (taskInstance.TriggerDetails is AppServiceTriggerDetails)
    {
        AppServiceTriggerDetails appService = taskInstance.TriggerDetails as AppServiceTriggerDetails;
        if (appService.CallerPackageFamilyName == EdgePFN)
        {
            // Establish the connection
        }
        else
        {
            // Reject the connection
        }
    }
}
```  

### <span data-ttu-id="89021-154">Nachrichtenversand</span><span class="sxs-lookup"><span data-stu-id="89021-154">Message sending</span></span>

<span data-ttu-id="89021-155">Damit eine APP und eine Erweiterung miteinander kommunizieren können, müssen Nachrichten an und von Ihnen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="89021-155">For an app and an extension to communicate with one another, messages need to be sent to and from them.</span></span>

<span data-ttu-id="89021-156">Chrome-Erweiterungen initiieren eine Nachricht mithilfe der [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API, um eine Nachricht mit einem nicht persistenten Kanal an den systemeigenen Host zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="89021-156">Chrome extensions initiate a message using the [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API to deliver a message to the native host using a non-persistent channel.</span></span> 

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

<span data-ttu-id="89021-157">Der erste Parameter ist der Name des systemeigenen Hosts, in dem Chrome in der Registrierung für das Manifest nachschlägt.</span><span class="sxs-lookup"><span data-stu-id="89021-157">The first parameter is the name of the native host, which Chrome looks up in the registry for the manifest.</span></span> <span data-ttu-id="89021-158">Das Manifest gibt die exe-Nachricht an, die von Chrome in einem Sandkasten gestartet wird, und die Nachricht wird mithilfe von Std-i/o gesendet.</span><span class="sxs-lookup"><span data-stu-id="89021-158">The manifest specifies the .exe that Chrome will launch in a sandbox, and the message is sent using std i/o.</span></span> <span data-ttu-id="89021-159">Erweiterungen können auch einen beständigen Kanal mithilfe der `runtime.connectNative` API einrichten, die den Namen des systemeigenen Hosts als einzigen Parameter übernimmt.</span><span class="sxs-lookup"><span data-stu-id="89021-159">Extensions can also establish a persistent channel using the `runtime.connectNative` API, which takes the name of the native host as the only parameter.</span></span> 

<span data-ttu-id="89021-160">Microsoft Edge verwendet das gleiche Konstrukt wie die native Messaging-API von Chrome, damit Microsoft Edge-Erweiterungen angeben können, mit welchem App-Dienst eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="89021-160">Microsoft Edge uses the same construct as Chrome's native messaging API to allow Microsoft Edge extensions to specify which app service to connect to.</span></span> <span data-ttu-id="89021-161">Der erste Parameter in `runtime.sendNativeMessage` gibt den Namen des App-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="89021-161">The first parameter in `runtime.sendNativeMessage` specifies the app service name.</span></span> <span data-ttu-id="89021-162">Im Abschnitt [Registrierung und Host Manifest](#registration-and-host-manifest) ist dies `"com.microsoft.inventory"` .</span><span class="sxs-lookup"><span data-stu-id="89021-162">In the [Registration and host manifest](#registration-and-host-manifest) section, this is `"com.microsoft.inventory"`.</span></span> <span data-ttu-id="89021-163">Die Microsoft Edge-Erweiterungs Plattform schränkt den systemeigenen Messaging-Host auf eine UWP-App ein, die im gleichen AppX wie die Erweiterung verpackt ist.</span><span class="sxs-lookup"><span data-stu-id="89021-163">The Microsoft Edge extension platform restricts the native messaging host to being a UWP app that is packaged in the same AppX as the extension.</span></span> <span data-ttu-id="89021-164">Dadurch werden alle Sicherheitsrisiken verringert, die mit böswilligen Angriffen einhergehen, die versuchen, Microsoft Edge mit einem anderen Paket Familiennamen zu verbinden, indem Sie Manifest-Einträge manipulieren.</span><span class="sxs-lookup"><span data-stu-id="89021-164">This mitigates any security risks associated with malicious attacks that try to connect Microsoft Edge with another Package Family Name by tampering with manifest entries.</span></span> 

<span data-ttu-id="89021-165">Dies bedeutet, dass Microsoft Edge neben dem in der API angegebenen Namen denselben Paket Familiennamen wie die Erweiterung verwendet, `AppService` um den Anbieter des App-Diensts eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="89021-165">This means that Microsoft Edge will use the same Package Family Name as the extension, in addition to the `AppService` name specified in the API, to uniquely identify the provider of the app service.</span></span>  

> [!NOTE]
> <span data-ttu-id="89021-166">Dies kann nicht einfach vom [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md)konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="89021-166">This will not be easily converted by the [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md).</span></span> <span data-ttu-id="89021-167">Alle Erweiterungen, die die Berechtigung angeben, werden `"nativeMessaging"` als obligatorische manuelle Konvertierung für diese Komponente gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="89021-167">Any extensions that specifies the `"nativeMessaging"` permission will be flagged as requiring manual conversion for this component.</span></span>

### <span data-ttu-id="89021-168">Kommunikationsprotokoll</span><span class="sxs-lookup"><span data-stu-id="89021-168">Communication protocol</span></span>

<span data-ttu-id="89021-169">Das Kommunikationsprotokoll für systemeigene Messaging bestimmt, wie Nachrichten vor dem Senden formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="89021-169">Communication protocol for native messaging determines how messages are formatted before sending.</span></span>

<span data-ttu-id="89021-170">Chrome startet jeden systemeigenen Messaging-Host in einem separaten Prozess und kommuniziert mit ihm über die Standardeingabe und die Standardausgabe.</span><span class="sxs-lookup"><span data-stu-id="89021-170">Chrome starts each native messaging host in a separate process and communicates with it using standard input and standard output.</span></span> <span data-ttu-id="89021-171">Das gleiche Format wird verwendet, um Nachrichten in beide Richtungen zu senden: jede Nachricht wird mit JSON, UTF-8-codiert und mit der 32-Bit-Nachrichtenlänge in der systemeigenen Bytereihenfolge vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="89021-171">The same format is used to send messages in both directions: each message is serialized using JSON, UTF-8 encoded and is preceded with 32-bit message length in native byte order.</span></span>

<span data-ttu-id="89021-172">Für Microsoft Edge wird die Hintergrundaufgabe/Haupt-APP, die den App-Dienst implementiert, von der Plattform gestartet.</span><span class="sxs-lookup"><span data-stu-id="89021-172">For Microsoft Edge, the background task/main app that implements the app service will be started by the platform.</span></span> <span data-ttu-id="89021-173">Beim Start wird die Methode der Hintergrundaufgabe `Run` aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="89021-173">On startup, the background task's `Run` method will be invoked:</span></span>  

```csharp
public void Run(IBackgroundTaskInstance taskInstance)    
{
    this.backgroundTaskDeferral = taskInstance.GetDeferral();
    // Get a deferral so that the service isn't terminated.
    taskInstance.Canceled += OnTaskCanceled;
    // Associate a cancellation handler with the background task.
    // Retrieve the app service connection and set up a listener for incoming app service requests.
    var details = taskInstance.TriggerDetails as AppServiceTriggerDetails;
    appServiceconnection = details.AppServiceConnection;
    appServiceconnection.RequestReceived += OnRequestReceived;
}
```  

<span data-ttu-id="89021-174">Wenn Ihre Erweiterung eine Nachricht an Ihre UWP-App sendet, [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) wird das Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="89021-174">When your extension sends a message to your UWP app, the [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) event will be raised.</span></span> <span data-ttu-id="89021-175">Diese JSON-formatierte Nachricht wird dann in das erste keywert-Paar eines [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) Objekts stringified.</span><span class="sxs-lookup"><span data-stu-id="89021-175">This JSON formatted message will then be stringified into the first KeyValue pair of a [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) object.</span></span> <span data-ttu-id="89021-176">:</span><span class="sxs-lookup"><span data-stu-id="89021-176">:</span></span>

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

<span data-ttu-id="89021-177">Wenn Ihre UWP-App eine Antwort an Ihre Durchwahl zurücksendet, [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) wird Sie dem Objekt hinzugefügt `ValueSet` .</span><span class="sxs-lookup"><span data-stu-id="89021-177">When your UWP app sends a response back to your extension, a [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) will be added to the `ValueSet` object.</span></span> <span data-ttu-id="89021-178">Die `Key` Eigenschaft wird von Microsoft Edge ignoriert, die `Value` Eigenschaft enthält jedoch eine gültige JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="89021-178">The `Key` property will be ignored by Microsoft Edge, but the `Value` property will contain a valid JSON string.</span></span>

### <span data-ttu-id="89021-179">Rückruf</span><span class="sxs-lookup"><span data-stu-id="89021-179">Callback</span></span>

<span data-ttu-id="89021-180">Für Rückrufe verwendet Chrome [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) eine Rückruffunktion, mit der jede asynchrone Antwort vom Senden einer Nachricht verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="89021-180">For callbacks, Chrome uses [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) which allows a callback function to handle any asynchronous response from sending a message.</span></span>

<span data-ttu-id="89021-181">Microsoft Edge verwendet die [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) Methode des Objekts [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) , damit die APP ein [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) Objekt wieder an die Erweiterung senden kann.</span><span class="sxs-lookup"><span data-stu-id="89021-181">Microsoft Edge uses the [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) object's [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) method to let the app send a [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) object back to the extension.</span></span>


### <span data-ttu-id="89021-182">Beschränkung der Nachrichtengröße</span><span class="sxs-lookup"><span data-stu-id="89021-182">Message size limit</span></span>
<span data-ttu-id="89021-183">Nachrichten, die zwischen einer Erweiterung und einer APP hin-und hergesendet werden, weisen für Chrome und Microsoft Edge unterschiedliche Einschränkungen für die Nachrichtengröße auf.</span><span class="sxs-lookup"><span data-stu-id="89021-183">Messages that are sent back and forth between an extension and an app have different message size limitations in place for Chrome and Microsoft Edge.</span></span>

<span data-ttu-id="89021-184">Chrome weist die folgenden Einschränkungen für die Nachrichtengröße auf:</span><span class="sxs-lookup"><span data-stu-id="89021-184">Chrome has the following message size limitations:</span></span>
-   <span data-ttu-id="89021-185">Grenzwert für einzelne Nachrichten vom systemeigenen Messaging-Host: 1 MB</span><span class="sxs-lookup"><span data-stu-id="89021-185">Single message limit from native messaging host: 1 MB</span></span>
-   <span data-ttu-id="89021-186">Einzige Nachrichtengrenze, die an den systemeigenen Messaging-Host gesendet wird: 4 GB</span><span class="sxs-lookup"><span data-stu-id="89021-186">Single message limit sent to native messaging host: 4 GB</span></span>
    
<span data-ttu-id="89021-187">Für Microsoft Edge ist zwar `AppService` keine Beschränkung der Nachrichtengröße (abhängig vom Arbeitsspeicher) vorhanden, doch Microsoft Edge schützt sich selbst vor Fehlverhalten von systemeigenen apps, indem die folgenden Einschränkungen für die Nachrichtengröße auferlegt werden:</span><span class="sxs-lookup"><span data-stu-id="89021-187">For Microsoft Edge, while `AppService` has no limit on message size (dependent on memory), Microsoft Edge protects itself against misbehaving native apps by imposing the following message size limits:</span></span>
-   <span data-ttu-id="89021-188">Beschränkung einzelner Nachrichten von der UWP-App zur Erweiterung: 1 MB</span><span class="sxs-lookup"><span data-stu-id="89021-188">Single message limit from UWP app to extension: 1 MB</span></span>
-   <span data-ttu-id="89021-189">Beschränkung einzelner Nachrichten von der Erweiterung auf die UWP-App: 100 MB</span><span class="sxs-lookup"><span data-stu-id="89021-189">Single message limit from extension to UWP app: 100 MB</span></span>
    
### <span data-ttu-id="89021-190">Systemeigene Messagingverbindungen</span><span class="sxs-lookup"><span data-stu-id="89021-190">Native messaging connections</span></span>

<span data-ttu-id="89021-191">Es gibt zwei Arten von Verbindungen für systemeigene Nachrichten. persistent und nicht persistent.</span><span class="sxs-lookup"><span data-stu-id="89021-191">There are two types of connections for native messaging; persistent and non-persistent.</span></span>
<span data-ttu-id="89021-192">Eine **dauerhafte** Verbindung ist eine Verbindung, die weiterhin ausgeführt wird, bis der Port zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="89021-192">A **persistent** connection is a connection that is kept running until the port is destroyed.</span></span> <span data-ttu-id="89021-193">Eine **nicht persistente** Verbindung ist eine Verbindung, die für eine Nachricht gleichzeitig geöffnet und nach der Zustellung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="89021-193">A **non-persistent** connection is a connection that is opened for one message at a time and closes after delivery.</span></span>

#### <span data-ttu-id="89021-194">Permanent</span><span class="sxs-lookup"><span data-stu-id="89021-194">Persistent</span></span>

<span data-ttu-id="89021-195">Bei Chrome wird eine dauerhafte Verbindung hergestellt, indem ein Messagingport mithilfe von erstellt wird [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) .</span><span class="sxs-lookup"><span data-stu-id="89021-195">For Chrome, a persistent connection is made by creating a messaging port using [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span> <span data-ttu-id="89021-196">Sobald der Port erstellt wurde, startet Chrome einen systemeigenen Messaging-Hostprozess, der bis zum zerstörten Port weiter ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89021-196">Once the port is made, Chrome starts a native messaging host process that keeps running until the port it destroyed.</span></span>

<span data-ttu-id="89021-197">Für Microsoft Edge wird nach dem Erstellen eines Messagingports mit `runtime.connectNative` Microsoft Edge das Programm gestartet, [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) und es wird weiterhin ausgeführt, bis der Port zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="89021-197">For Microsoft Edge, once a messaging port is created using `runtime.connectNative`, Microsoft Edge starts the [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) and keeps it running until the port is destroyed.</span></span> <span data-ttu-id="89021-198">Der folgende Codeausschnitt zeigt, wie eine dauerhafte Verbindung in einer UWP-App hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="89021-198">The following snippet shows how a persistent connection is established from within a UWP app.</span></span> 

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <span data-ttu-id="89021-199">Nicht persistent</span><span class="sxs-lookup"><span data-stu-id="89021-199">Non-persistent</span></span>

<span data-ttu-id="89021-200">Wenn eine Nachricht mit [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome gesendet wird, ohne einen Messagingport zu erstellen, startet Chrome einen neuen systemeigenen Messaging-Hostprozess für jede Nachricht.</span><span class="sxs-lookup"><span data-stu-id="89021-200">When a message is sent using [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome, without creating a messaging port, Chrome starts a new native messaging host process for each message.</span></span> <span data-ttu-id="89021-201">Die erste vom Hostprozess generierte Nachricht wird als Antwort auf die ursprüngliche Anforderung verarbeitet, und alle anderen Nachrichten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="89021-201">The first message generated by the host process is handled as a response to the original request, and all other messages after it are ignored.</span></span>

<span data-ttu-id="89021-202">Microsoft Edge beendet die Verbindung, nachdem die Antwort jeder Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="89021-202">Microsoft Edge will terminate the connection after every messages' response has been received.</span></span> <span data-ttu-id="89021-203">Der folgende Codeausschnitt zeigt eine nicht persistente Verbindung, die dadurch hergestellt wird `AppServiceConnection` , dass Sie in der UWP-App beendet wird, nachdem eine Anforderung empfangen und als eine gespeichert wurde [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse) .</span><span class="sxs-lookup"><span data-stu-id="89021-203">The following snippet shows a non-persistent connection that is established with `AppServiceConnection` that will then be terminated within the UWP app after a request has been received and stored as an [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse).</span></span>

```csharp
using (var connection = new AppServiceConnection())
{    
    //Set up a new app service connection
    connection.AppServiceName = "com.microsoft.randomnumbergenerator";
    connection.PackageFamilyName = "Microsoft.SDKSamples.AppServicesProvider.CS_8wekyb3d8bbwe";
    AppServiceConnectionStatus status = await connection.OpenAsync();
    AppServiceResponse response = await connection.SendMessageAsync(inputs);
}
```  

### <span data-ttu-id="89021-204">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="89021-204">Permission</span></span>

<span data-ttu-id="89021-205">Um die Verwendung der systemeigenen Messagingfunktion mit ihrer Erweiterung zu aktivieren, müssen Sie für Chrome und Microsoft Edge die `"nativeMessaging"` Berechtigung in Ihrer `manifest.json` Datei deklarieren.</span><span class="sxs-lookup"><span data-stu-id="89021-205">In order to enable native messaging use with your extension, for both Chrome and Microsoft Edge you'll need to declare the `"nativeMessaging"` permission in you `manifest.json` file.</span></span>

## <span data-ttu-id="89021-206">App-Dienste</span><span class="sxs-lookup"><span data-stu-id="89021-206">App services</span></span>
<span data-ttu-id="89021-207">In diesem Abschnitt werden die Auswirkungen von App-Diensten auf die Microsoft Edge-systemeigene Messagingleistung und den Arbeitsspeicher erläutert.</span><span class="sxs-lookup"><span data-stu-id="89021-207">This section details the impact app services has on Microsoft Edge native messaging performance and memory.</span></span>

### <span data-ttu-id="89021-208">Leistung</span><span class="sxs-lookup"><span data-stu-id="89021-208">Performance</span></span>

<span data-ttu-id="89021-209">App-Dienste werden von der Vordergrund-APP, die Sie anruft, "gesponsert", was für systemeigene Messagingzwecke Microsoft Edge ist.</span><span class="sxs-lookup"><span data-stu-id="89021-209">App services are "sponsored" by the foreground app that calls them which for native messaging purposes is Microsoft Edge.</span></span> <span data-ttu-id="89021-210">Dies bedeutet, dass APP-Dienste ausgeführt werden können, solange Microsoft Edge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89021-210">This means that app services can run as long as Microsoft Edge is running.</span></span>

<span data-ttu-id="89021-211">In Bezug auf Latenz verwenden App-Dienste Named Pipes, die nach der ersten Verbindung zwei apps direkt kommunizieren lassen.</span><span class="sxs-lookup"><span data-stu-id="89021-211">In regards to latency, app services use named pipes that, after initial connection, allow two apps to directly communicate.</span></span> <span data-ttu-id="89021-212">Diese Methode der Kommunikation erzeugt eine niedrige Latenzzeit.</span><span class="sxs-lookup"><span data-stu-id="89021-212">This method of communication produces low latency.</span></span> <span data-ttu-id="89021-213">Bei Geräten mit langsamen CPUs wird nach dem Starten des Prozesses, der den App-Dienst hostet (~ 80ms zum Starten der Hintergrundaufgabe auf einigen Geräten), eine anfängliche Latenzzeit auftreten.</span><span class="sxs-lookup"><span data-stu-id="89021-213">Devices with slow CPUs will experience some initial latency after starting up the process that hosts the app service (~80ms to startup the background task on some devices).</span></span> <span data-ttu-id="89021-214">Nach dem Start sollte die Leistung auf langsamen CPU-Geräten gut sein.</span><span class="sxs-lookup"><span data-stu-id="89021-214">After start-up, performance on slow CPU devices should be good.</span></span> 

### <span data-ttu-id="89021-215">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="89021-215">Memory</span></span>
<span data-ttu-id="89021-216">Der einem App-Dienst zugewiesene Arbeitsspeicher wird aus dem für Microsoft Edge zugewiesenen Kontingent herausgenommen.</span><span class="sxs-lookup"><span data-stu-id="89021-216">The memory allocated to an app service is taken out of the quota allocated to Microsoft Edge.</span></span> <span data-ttu-id="89021-217">Wenn Microsoft Edge also zu viele APP-Dienste startet, besteht die Möglichkeit, dass Ihnen der Arbeitsspeicher ausgeht.</span><span class="sxs-lookup"><span data-stu-id="89021-217">This means that if Microsoft Edge starts too many app services there is a possibility that they could run out of memory.</span></span> <span data-ttu-id="89021-218">Die üblichen Speicher Caps für Hintergrundaufgaben werden für App-Dienste erzwungen.</span><span class="sxs-lookup"><span data-stu-id="89021-218">The usual background task memory caps are enforced on app services.</span></span> <span data-ttu-id="89021-219">Auf einem 512 MB-Gerät kann eine APP-Dienst Hintergrundaufgabe beispielsweise nicht größer als 16MB sein.</span><span class="sxs-lookup"><span data-stu-id="89021-219">For instance, on a 512MB device an app service background task can be no larger than 16MB.</span></span> <span data-ttu-id="89021-220">Diese Nummer steigt, wenn die Geräte skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="89021-220">This number goes up as the devices scale up.</span></span>

## <span data-ttu-id="89021-221">Erstellen einer Erweiterung mit systemeigenem Messaging</span><span class="sxs-lookup"><span data-stu-id="89021-221">Creating an extension with native messaging</span></span>

<span data-ttu-id="89021-222">Damit systemeigene Nachrichten getestet werden können, benötigt Ihre Erweiterung einen Paket Familiennamen.</span><span class="sxs-lookup"><span data-stu-id="89021-222">In order to test native messaging, your extension needs a Package Family Name.</span></span> <span data-ttu-id="89021-223">Microsoft Edge ermittelt mithilfe dieser Methode die Identität des systemeigenen Nachrichten Hosts, was bedeutet, dass Ihre Erweiterung verpackt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="89021-223">Microsoft Edge uses this to determine the native message host identity, which means your extension should be packaged.</span></span> 

<span data-ttu-id="89021-224">So erstellen Sie Ihre Erweiterung mit systemeigenem Messaging in Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="89021-224">To create your extension with native messaging in Visual Studio:</span></span>

1.  <span data-ttu-id="89021-225">Erstellen Sie ein UWP-Projekt in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="89021-225">Create a UWP project in Visual Studio.</span></span>
2.  <span data-ttu-id="89021-226">[ `AppService` Zu ihrer UWP-app hinzufügen](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span><span class="sxs-lookup"><span data-stu-id="89021-226">[Add `AppService` to your UWP app](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span></span>
    -   <span data-ttu-id="89021-227">Sie können an dieser Stelle optional [konfigurieren `AppService` , dass Sie in der Haupt-App](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) statt als Hintergrundaufgabe gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="89021-227">You can optionally [configure `AppService` to be hosted in the main app](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) instead of as a background task at this point.</span></span>
3.  <span data-ttu-id="89021-228">Erstellen und testen Sie Ihr UWP-Projekt.</span><span class="sxs-lookup"><span data-stu-id="89021-228">Build and test your UWP project.</span></span>
    -   <span data-ttu-id="89021-229">Optional können Sie eine [Desktop Brücken Komponente](#adding-a-desktop-bridge-component)hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="89021-229">You can optionally add a [Desktop Bridge component](#adding-a-desktop-bridge-component).</span></span>
4.  <span data-ttu-id="89021-230">Erstellen Sie eine Microsoft Edge-Erweiterung, die systemeigene Nachrichten für die Kommunikation mit der UWP-Begleit-App verwendet.</span><span class="sxs-lookup"><span data-stu-id="89021-230">Create a Microsoft Edge extension that uses native messaging to communicate with the UWP companion app.</span></span> <span data-ttu-id="89021-231">Die Erweiterungsdateien können einem `Extension` im UWP-Projekt benannten Ordner hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="89021-231">The extension files can be added into a folder named `Extension` in the UWP project.</span></span> <span data-ttu-id="89021-232">Alle Dateien unterhalb dieses Ordners, einschließlich Unterordnern, müssen ihre Eigenschaften so konfiguriert haben, dass `Build Action=Content` und `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="89021-232">All of the files underneath this folder, including subfolders, need to have their properties configured such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span> <span data-ttu-id="89021-233">Stellen Sie sicher, dass `manifest.json` auch diese Eigenschaften konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="89021-233">Make sure `manifest.json` is also configured with these properties.</span></span>
5.  <span data-ttu-id="89021-234">Ändern `package.manifest.xml` Sie die Datei im Projekt so, dass Sie Erweiterungs Metadaten enthält, und konvertieren Sie Sie in eine headless-APP, indem Sie Folgendes hinzufügen `AppListEntry="none"` :</span><span class="sxs-lookup"><span data-stu-id="89021-234">Modify the `package.manifest.xml` file in the project to include extension metadata and convert it to a headless app by adding `AppListEntry="none"`:</span></span>
    
    ```xml
    <Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10" 
    xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities" 
    xmlns:mp="http://schemas.microsoft.com/appx/2014/phone/manifest" 
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10" 
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap uap3 mp rescap build" 
    xmlns:build="http://schemas.microsoft.com/developer/appx/2015/build">

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.15063.0" MaxVersionTested="10.0.15063.0" />
    </Dependencies>

       <Application Id="App" Executable="$targetnametoken$.exe" EntryPoint="NativeMessagingHostInProcess.App">
          <uap:VisualElements AppListEntry="none"
            DisplayName="SecureInput"
            Square150x150Logo="Assets\Square150x150Logo.png"
            Square44x44Logo="Assets\Square44x44Logo.png"
            Description="NativeMessagingHostInProcess"
            BackgroundColor="transparent">
          </uap:VisualElements>
          <Extensions>
            <uap3:Extension Category="windows.appExtension">
                <uap3:AppExtension
                    Name="com.microsoft.edge.extension"
                    Id="EdgeExtension"
                    PublicFolder="Extension"
                    DisplayName="ms-resource:DisplayName">
                </uap3:AppExtension>
            </uap3:Extension>
          </Extensions>
    </Application>
    ```
    
6.  <span data-ttu-id="89021-235">Verwenden Sie den `AppService` für UWP konfigurierten Namen in den systemeigenen Messaging-APIs.</span><span class="sxs-lookup"><span data-stu-id="89021-235">Use the `AppService` name configured for the UWP in the native messaging APIs.</span></span>
7.  <span data-ttu-id="89021-236">Erstellen und [Bereitstellen](#deploying) des UWP-Projekts (mit der optionalen Desktop Brücken Komponente)</span><span class="sxs-lookup"><span data-stu-id="89021-236">Build and [deploy](#deploying) the UWP project (with the optional Desktop Bridge component).</span></span>
8.  <span data-ttu-id="89021-237">[Verpacken](#packaging) der nativen Messaging-Erweiterung, sobald Sie für die Übermittlung an den Store bereit ist</span><span class="sxs-lookup"><span data-stu-id="89021-237">[Package](#packaging) your native messaging extension once it's ready for Store submission</span></span>
    
> [!NOTE]
> <span data-ttu-id="89021-238">Verweisen Sie auf den Abschnitt [Demos](#demos) , um ein Beispiel für eine vollständige Native Messaging-Erweiterung zu finden.</span><span class="sxs-lookup"><span data-stu-id="89021-238">Reference the [Demos](#demos) section for an example of a complete native messaging extension.</span></span>

## <span data-ttu-id="89021-239">Hinzufügen einer Desktop Brücken Komponente</span><span class="sxs-lookup"><span data-stu-id="89021-239">Adding a Desktop Bridge component</span></span> 
<span data-ttu-id="89021-240">Wenn Sie dem Paket eine Desktop Brücken Komponente hinzufügen möchten, müssen Sie Ihr Win32-Projekt in Visual Studio erstellen und erstellen.</span><span class="sxs-lookup"><span data-stu-id="89021-240">If you want to add a Desktop Bridge component to your package, you'll need to create and build your Win32 project in Visual Studio.</span></span> <span data-ttu-id="89021-241">Informationen dazu, wie Sie Ihre Win32-app in UWP konvertieren, finden Sie unter [Portieren von apps auf Windows 10 über die Desktop-Brücke](/windows/uwp/porting/desktop-to-uwp-root).</span><span class="sxs-lookup"><span data-stu-id="89021-241">For info on how to convert your win32 app to UWP, see [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span></span> <span data-ttu-id="89021-242">Nachdem Sie in Visual Studio erstellt haben, können Sie die ausführbare Win32-Datei zum Paket hinzufügen, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="89021-242">Once built in Visual Studio, you can add the Win32 executable to the package by doing the following steps:</span></span>

1.  <span data-ttu-id="89021-243">Fügen Sie das Win32-Projekt der gleichen Projektmappe wie das UWP-Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="89021-243">Add the Win32 project to the same solution as the UWP project.</span></span> 
2.  <span data-ttu-id="89021-244">Das Win32-Projekt als abhängiges Projekt für das UWP-Projekt einrichten:</span><span class="sxs-lookup"><span data-stu-id="89021-244">Set the Win32 project as a dependent project for the UWP project:</span></span>
    
    ![Einrichten von Projektabhängigkeiten](./../media/project-dependencies.PNG)
    
3.  <span data-ttu-id="89021-246">Erstellen Sie einen `Win32` Ordner im UWP-Projekt.</span><span class="sxs-lookup"><span data-stu-id="89021-246">Create a `Win32` folder within the UWP project.</span></span> <span data-ttu-id="89021-247">Kopieren Sie die erforderlichen Binärdateien für das `Win32` Projekt in diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="89021-247">Copy the necessary binaries for the `Win32` project to this folder.</span></span> <span data-ttu-id="89021-248">Konfigurieren Sie die Eigenschaften aller Binärdateien wie `Build Action=Content` und `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="89021-248">Configure the properties of all the binaries such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>
    
    ![Ordner mit Win32-und UWP-APP-Dateien](./../media/desktop-bridge.png)
    
4.  <span data-ttu-id="89021-250">Ändern Sie die UWP-Projektdatei, um alle erforderlichen Binärdateien für das `Win32` Projekt in diesen Ordner mit dem Befehl Postbuild-Ereignis zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="89021-250">Modify the UWP project file to copy all the necessary binaries for the `Win32` project into this folder using PostBuild event command.</span></span> <span data-ttu-id="89021-251">Dadurch wird sichergestellt, dass die aktualisierten Binärdateien jedes Mal in den Ordner kopiert werden, wenn die Projektmappe neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="89021-251">This ensures that the updated binaries are being copied to the folder every time the solution is rebuilt.</span></span>
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```
    
5.  <span data-ttu-id="89021-252">Ändern `package.manifest.xml` `<desktop:Extension>` Sie, indem Sie das Element zum Element hinzufügen `<Extensions>` :</span><span class="sxs-lookup"><span data-stu-id="89021-252">Modify `package.manifest.xml` by adding the `<desktop:Extension>` element to the `<Extensions>` element:</span></span>
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```
    
## <span data-ttu-id="89021-253">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="89021-253">Deploying</span></span>
<span data-ttu-id="89021-254">Nachdem Sie Ihr UWP-Projekt (und optional Win32-Projekt) wie oben beschrieben konfiguriert haben, können Sie die Projektmappe mit Visual Studio bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="89021-254">Once you have configured your UWP project (and optionally Win32 project) as outlined above, you are ready to deploy the solution using Visual Studio.</span></span>

![Erstellen eines InProcess-Projekts](../media/native-message-uwp-debug.PNG)

<span data-ttu-id="89021-256">Nachdem die Lösung richtig bereitgestellt wurde, sollte Ihre Erweiterung in Microsoft Edge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="89021-256">Once the solution is correctly deployed, you should see your extension in Microsoft Edge.</span></span>

![in Microsoft Edge angezeigte Erweiterung](../media/secureextension.png)

## <span data-ttu-id="89021-258">Verpacken</span><span class="sxs-lookup"><span data-stu-id="89021-258">Packaging</span></span>

> [!NOTE]
> <span data-ttu-id="89021-259">Das Übermitteln einer Microsoft Edge-Erweiterung an den Microsoft Store ist derzeit eine eingeschränkte Funktion.</span><span class="sxs-lookup"><span data-stu-id="89021-259">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="89021-260">Wenden Sie sich mit Ihren Anforderungen an den Microsoft Store an [uns](https://aka.ms/extension-request) , und wir werden Sie für ein zukünftiges Update in Erwägung ziehen.</span><span class="sxs-lookup"><span data-stu-id="89021-260">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>

<span data-ttu-id="89021-261">Mit der integrierten Funktionalität von Visual Studio können Sie ein Store-Paket für die Übermittlung an das Windows dev Center generieren:</span><span class="sxs-lookup"><span data-stu-id="89021-261">You can generate a Store package for submission to the Windows Dev Center using built-in Visual Studio functionality:</span></span>

![Erstellen eines Store-Pakets](../media/create-store-package.PNG)

## <span data-ttu-id="89021-263">Debuggen</span><span class="sxs-lookup"><span data-stu-id="89021-263">Debugging</span></span>
<span data-ttu-id="89021-264">Die Anweisungen für das Debuggen variieren je nachdem, welche Komponente Sie testen möchten:</span><span class="sxs-lookup"><span data-stu-id="89021-264">The instructions for debugging vary depending on which component you want to test out:</span></span>

### <span data-ttu-id="89021-265">Debuggen der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="89021-265">Debugging the extension</span></span>
<span data-ttu-id="89021-266">Nachdem die Lösung bereitgestellt wurde, wird die Erweiterung in Microsoft Edge installiert.</span><span class="sxs-lookup"><span data-stu-id="89021-266">Once the solution is deployed, the extension will be installed in Microsoft Edge.</span></span> <span data-ttu-id="89021-267">Informationen zum Debuggen einer Erweiterung finden Sie im Leitfaden zur [Fehlerbehebung](./debugging-extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="89021-267">Check out the [Debugging](./debugging-extensions.md) guide for info on how to debug an extension.</span></span>


### <span data-ttu-id="89021-268">Debuggen der UWP-App</span><span class="sxs-lookup"><span data-stu-id="89021-268">Debugging the UWP app</span></span>
<span data-ttu-id="89021-269">Die UWP-APP wird gestartet, wenn die Erweiterung versucht, eine Verbindung mit der [systemeigenen Messaging-API](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative)herzustellen.</span><span class="sxs-lookup"><span data-stu-id="89021-269">The UWP app will launch when the extension tries to connect to it using [native messaging APIs](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span> <span data-ttu-id="89021-270">Sie müssen die UWP-app nur Debuggen, nachdem der Prozess gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="89021-270">You'll need to debug the UWP app only once the process starts.</span></span> <span data-ttu-id="89021-271">Dies kann über die Eigenschaftenseite des Projekts konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="89021-271">This can be configured via the project's Property page:</span></span>

1.  <span data-ttu-id="89021-272">Klicken Sie in Visual Studio mit der rechten Maustaste auf das UWP-App-Projekt.</span><span class="sxs-lookup"><span data-stu-id="89021-272">In Visual Studio, right click your UWP app project</span></span>
2.  <span data-ttu-id="89021-273">Eigenschaften auswählen</span><span class="sxs-lookup"><span data-stu-id="89021-273">Select Properties</span></span>
3.  <span data-ttu-id="89021-274">Aktivieren Sie "nicht starten, aber meinen Code beim Starten Debuggen"</span><span class="sxs-lookup"><span data-stu-id="89021-274">Check "Do not launch, but debug my code when it starts"</span></span>
    
    ![Feld "nicht starten" auswählen](../media/native-message-do-not-launch.png)
    
<span data-ttu-id="89021-276">In Visual Studio können Sie jetzt Haltepunkte im Code festlegen, in dem Sie debuggen möchten, und dann den Debugger starten, indem Sie F5 drücken.</span><span class="sxs-lookup"><span data-stu-id="89021-276">In Visual Studio you can now set breakpoints in the code where you want to debug, then launch the debugger by pressing F5.</span></span> <span data-ttu-id="89021-277">Sobald Sie mit der Erweiterung interagieren, um eine Verbindung mit der UWP-App herzustellen, wird Visual Studio automatisch an den Prozess angefügt.</span><span class="sxs-lookup"><span data-stu-id="89021-277">Once you interact with the extension to connect to the UWP app, Visual Studio will automatically attach to the process.</span></span>

### <span data-ttu-id="89021-278">Debuggen der Desktop Brücke</span><span class="sxs-lookup"><span data-stu-id="89021-278">Debugging the Desktop Bridge</span></span>
<span data-ttu-id="89021-279">Obwohl es verschiedene [Methoden zum Debuggen einer Desktop Brücke](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (konvertierte Win32-APP) gibt, ist die einzige Anwendung für diese Szenarien die PLMDebug-Option.</span><span class="sxs-lookup"><span data-stu-id="89021-279">Even though there are various [methods for debugging a Desktop Bridge](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (converted Win32 app), the only one applicable for this scenarios is the PLMDebug option.</span></span> <span data-ttu-id="89021-280">Sie können der Startfunktion auch Debugcode hinzufügen, um eine Wartezeit für eine bestimmte Zeit durchzuführen, sodass Sie Visual Studio an den Prozess anfügen können.</span><span class="sxs-lookup"><span data-stu-id="89021-280">You could also add debugging code to the startup function to perform a wait for a specific time, allowing you to attach Visual Studio to the process.</span></span>
