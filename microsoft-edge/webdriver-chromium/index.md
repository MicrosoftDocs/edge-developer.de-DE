---
description: Erfahren Sie, wie Sie Ihre Website oder App in Microsoft Edge testen oder den Browser mit WebDriver automatisieren
title: Verwenden von WebDriver (Chromium) für die Testautomatisierung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, HTML, CSS, Javascript, Entwickler, WebDriver, Selenium, Tests, Tools, Automatisierung, Test
ms.openlocfilehash: 3865162b8227db2f0cfa051801a5de28ecf4b9d1
ms.sourcegitcommit: 3094c972532bc89dcb429d26880c873809fd1ab8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "11599457"
---
# <a name="use-webdriver-chromium-for-test-automation"></a><span data-ttu-id="42dcc-104">Verwenden von WebDriver (Chromium) für die Testautomatisierung</span><span class="sxs-lookup"><span data-stu-id="42dcc-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="42dcc-105">Mit WebDriver können Entwickler automatisierte Tests erstellen, welche die Benutzerinteraktion simulieren.</span><span class="sxs-lookup"><span data-stu-id="42dcc-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="42dcc-106">WebDriver-Tests und -Simulationen unterscheiden sich in folgenden Punkten von JavaScript-Komponententests.</span><span class="sxs-lookup"><span data-stu-id="42dcc-106">WebDriver tests and simulations differ from JavaScript unit tests in the following ways.</span></span>  

*   <span data-ttu-id="42dcc-107">Greift auf Funktionen und Informationen zu, die JavaScript in Browsern nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="42dcc-108">Simuliert Benutzerereignisse oder Ereignisse auf Betriebssystemebene genauer.</span><span class="sxs-lookup"><span data-stu-id="42dcc-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="42dcc-109">Verwaltet mehrere Fenster, Registerkarten und Webseiten in einer einzigen Testsitzung.</span><span class="sxs-lookup"><span data-stu-id="42dcc-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="42dcc-110">Führt mehrere Sitzungen von Microsoft Edge auf einem bestimmten Computer aus.</span><span class="sxs-lookup"><span data-stu-id="42dcc-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  

## <a name="relationship-between-webdriver-and-other-software"></a><span data-ttu-id="42dcc-111">Beziehung zwischen WebDriver und anderer Software</span><span class="sxs-lookup"><span data-stu-id="42dcc-111">Relationship between WebDriver and other software</span></span>

<span data-ttu-id="42dcc-112">Um Microsoft Edge mit WebDriver zu automatisieren, um Benutzerinteraktionen zu simulieren, benötigen Sie drei Komponenten:</span><span class="sxs-lookup"><span data-stu-id="42dcc-112">To automate Microsoft Edge with WebDriver to simulate user interaction, you need 3 components:</span></span>

*  <span data-ttu-id="42dcc-113">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="42dcc-113">Microsoft Edge</span></span>
*  <span data-ttu-id="42dcc-114">Microsoft Edge-Treiber</span><span class="sxs-lookup"><span data-stu-id="42dcc-114">Microsoft Edge Driver</span></span>
*  <span data-ttu-id="42dcc-115">Ein WebDriver-Testframework, z. B. Selenium</span><span class="sxs-lookup"><span data-stu-id="42dcc-115">A WebDriver testing framework, such as Selenium</span></span>

<span data-ttu-id="42dcc-116">Die funktionale Beziehung zwischen WebDriver, Microsoft Edge Driver, Selenium und Internet Explorer Driver lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="42dcc-116">The functional relationship between WebDriver, Microsoft Edge Driver, Selenium, and Internet Explorer Driver is as follows.</span></span>

| <span data-ttu-id="42dcc-117">Technologie</span><span class="sxs-lookup"><span data-stu-id="42dcc-117">Technology</span></span> | <span data-ttu-id="42dcc-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="42dcc-118">Role</span></span> |
|---|---|
| <span data-ttu-id="42dcc-119">WebDriver</span><span class="sxs-lookup"><span data-stu-id="42dcc-119">WebDriver</span></span> | <span data-ttu-id="42dcc-120">Ein W3C-Standard für ein plattform- und sprachneutrales Kabelprotokoll.</span><span class="sxs-lookup"><span data-stu-id="42dcc-120">A W3C standard for a platform- and language-neutral wire protocol.</span></span>  <span data-ttu-id="42dcc-121">Mit diesem Protokoll können Out-of-Process-Programme remote das Verhalten von Webbrowsern anweisen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-121">This protocol allows out-of-process programs to remotely instruct the behavior of web browsers.</span></span> |
| <span data-ttu-id="42dcc-122">Microsoft Edge-Treiber</span><span class="sxs-lookup"><span data-stu-id="42dcc-122">Microsoft Edge Driver</span></span> | <span data-ttu-id="42dcc-123">Microsoft-Implementierung des WebDriver-Protokolls speziell für Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="42dcc-123">Microsoft's implementation of the WebDriver protocol specifically for Microsoft Edge.</span></span> <span data-ttu-id="42dcc-124">Testautoren schreiben Tests, die WebDriver-Befehle verwenden, die Microsoft Edge Treiber empfängt.</span><span class="sxs-lookup"><span data-stu-id="42dcc-124">Test authors write tests that use WebDriver commands that Microsoft Edge Driver receives.</span></span> <span data-ttu-id="42dcc-125">Microsoft Edge Der Treiber ist dann für die Kommunikation dieses Befehls mit dem Browser verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="42dcc-125">Microsoft Edge Driver is then responsible for communicating that command to the browser.</span></span> |
| <span data-ttu-id="42dcc-126">Selen</span><span class="sxs-lookup"><span data-stu-id="42dcc-126">Selenium</span></span> | <span data-ttu-id="42dcc-127">Ein beliebtes WebDriver-Testframework, mit dem Testautoren End-to-End-Tests schreiben und Browser automatisieren.</span><span class="sxs-lookup"><span data-stu-id="42dcc-127">A popular WebDriver testing framework that test authors use to write end-to-end tests and automate browsers.</span></span> <span data-ttu-id="42dcc-128">Selenium kann auf jeder Plattform verwendet werden und ist in Java, Python, C#, Ruby und JavaScript verfügbar.</span><span class="sxs-lookup"><span data-stu-id="42dcc-128">Selenium can be used on any platform, and is available in Java, Python, C#, Ruby, and JavaScript.</span></span> |
| <span data-ttu-id="42dcc-129">Internet Explorer-Treiber</span><span class="sxs-lookup"><span data-stu-id="42dcc-129">Internet Explorer Driver</span></span> | <span data-ttu-id="42dcc-130">Eine Implementierung des WebDriver-Protokolls speziell für Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="42dcc-130">An implementation of the WebDriver protocol specifically for Internet Explorer.</span></span> <span data-ttu-id="42dcc-131">Dieses Produkt wird vom Selenium-Projekt verwaltet.</span><span class="sxs-lookup"><span data-stu-id="42dcc-131">This product is maintained by the Selenium project.</span></span> <span data-ttu-id="42dcc-132">Um ältere End-to-End-Tests für Internet Explorer auszuführen, empfehlen wir die Verwendung des Internet Explorer-Treibers.</span><span class="sxs-lookup"><span data-stu-id="42dcc-132">To run legacy end-to-end tests for Internet Explorer, we recommend using Internet Explorer Driver.</span></span> |

<span data-ttu-id="42dcc-133">In den folgenden Abschnitten wird beschrieben, wie Sie mit WebDriver für Microsoft Edge \(Chromium\) beginnen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-133">The following sections describe how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <a name="install-microsoft-edge-chromium"></a><span data-ttu-id="42dcc-134">Installieren von Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="42dcc-134">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="42dcc-135">Stellen Sie sicher, dass Sie [Microsoft Edge (Chromium)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="42dcc-135">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="42dcc-136">Um zu bestätigen, dass Microsoft Edge \(Chromium\) installiert ist, navigieren Sie zu `edge://settings/help`, und überprüfen Sie, ob die Versionsnummer Version 75 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="42dcc-136">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is version 75 or later.</span></span>  

## <a name="download-microsoft-edge-driver"></a><span data-ttu-id="42dcc-137">Herunterladen des Microsoft Edge-Treibers</span><span class="sxs-lookup"><span data-stu-id="42dcc-137">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="42dcc-138">Führen Sie die folgenden Schritte aus, um die Automatisierung von Tests zu starten und sicherzustellen, dass die von Ihnen installierte WebDriver-Version mit Ihrer Browserversion übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="42dcc-138">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="42dcc-139">Suchen Sie Ihre Version von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="42dcc-139">Find your version of Microsoft Edge.</span></span>  
    1.  <span data-ttu-id="42dcc-140">Navigieren Sie zu `edge://settings/help`.</span><span class="sxs-lookup"><span data-stu-id="42dcc-140">Navigate to `edge://settings/help`.</span></span>  
        
        :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="Die Buildnummer für Microsoft Edge am 15. April 2021" lightbox="./media/microsoft-edge-version.msft.png":::
           <span data-ttu-id="42dcc-142">Die Buildnummer für Microsoft Edge am 15. April 2021</span><span class="sxs-lookup"><span data-stu-id="42dcc-142">The build number for Microsoft Edge on April 15, 2021</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="42dcc-143">Navigieren Sie zu [Microsoft Edge Treiber.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="42dcc-143">Navigate to [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  
1.  <span data-ttu-id="42dcc-144">Navigieren Sie zu **"Aktuelle Version abrufen".**</span><span class="sxs-lookup"><span data-stu-id="42dcc-144">Navigate to **Get the latest version**.</span></span>  
1.  <span data-ttu-id="42dcc-145">Wählen Sie den Build des Kanals aus, der Ihrer Versionsnummer von Microsoft Edge entspricht.</span><span class="sxs-lookup"><span data-stu-id="42dcc-145">Choose the build of channel that matches your version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="Der Abschnitt "Aktuelle Version abrufen" auf der Webseite "Microsoft Edge Treiber"" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       <span data-ttu-id="42dcc-147">The **Get the latest version** section on the Microsoft Edge [Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] webpage</span><span class="sxs-lookup"><span data-stu-id="42dcc-147">The **Get the latest version** section on the [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] webpage</span></span>  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  
    
## <a name="choose-a-webdriver-language-binding"></a><span data-ttu-id="42dcc-148">Auswählen einer WebDriver-Sprachbindung</span><span class="sxs-lookup"><span data-stu-id="42dcc-148">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="42dcc-149">Die letzte Komponente, die Sie herunterladen müssen, ist ein sprachspezifischer Client-Treiber, um Ihren Code \(Python, Java, C\#, Ruby, JavaScript\) in Befehle zu übersetzen, die der Microsoft Edge-Treiber in Microsoft Edge \(Chromium\) ausführt.</span><span class="sxs-lookup"><span data-stu-id="42dcc-149">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="42dcc-150">[Laden Sie die WebDriver-Sprachbindung Ihrer Wahl herunter][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="42dcc-150">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="42dcc-151">Das Microsoft Edge Team empfiehlt [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] oder höher, da es Microsoft Edge \(Chromium\) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42dcc-151">The Microsoft Edge team recommends [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="42dcc-152">Sie können jedoch Microsoft Edge \(Chromium\) in allen älteren Versionen von Selenium steuern, einschließlich der aktuellen stabilen Selenium 3-Version.</span><span class="sxs-lookup"><span data-stu-id="42dcc-152">However, you can control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="42dcc-153">Wenn Sie zuvor Microsoft Edge \(Chromium\) mit `ChromeDriver` und `ChromeOptions` Klassen automatisiert oder getestet haben, automatisiert oder getestet haben, wird Ihr WebDriver-Code nicht unter Microsoft Edge Version 80 oder höher ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42dcc-153">If you previously automated or tested Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="42dcc-154">Um das Problem zu beheben, aktualisieren Sie Ihre Tests, um die Klasse `EdgeOptions` verwenden, und laden Sie [Microsoft Edge-Treiber][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] herunter.</span><span class="sxs-lookup"><span data-stu-id="42dcc-154">To solve the problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  

### <a name="using-selenium-4"></a><span data-ttu-id="42dcc-155">Verwenden von Selenium 4</span><span class="sxs-lookup"><span data-stu-id="42dcc-155">Using Selenium 4</span></span>

<span data-ttu-id="42dcc-156">Selenium 4 bietet integrierte Unterstützung für Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="42dcc-156">Selenium 4 has built-in support for Microsoft Edge (Chromium).</span></span>  <span data-ttu-id="42dcc-157">Navigieren Sie zum Installieren von Selenium 4 zu ["Selenium-Bibliotheken installieren".][SeleniumInstallingLibraries]</span><span class="sxs-lookup"><span data-stu-id="42dcc-157">To install Selenium 4, navigate to [Installing Selenium libraries][SeleniumInstallingLibraries].</span></span>

<span data-ttu-id="42dcc-158">Wenn Sie Selenium 4 verwenden, müssen Sie selenium-Tools nicht für Microsoft Edge verwenden.</span><span class="sxs-lookup"><span data-stu-id="42dcc-158">When you use Selenium 4, you don't need to use Selenium Tools for Microsoft Edge.</span></span>  <span data-ttu-id="42dcc-159">Selenium-Tools für Microsoft Edge gelten nur für Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="42dcc-159">Selenium Tools for Microsoft Edge are for Selenium 3 only.</span></span>  <span data-ttu-id="42dcc-160">If you try to use Selenium 4 with Selenium Tools for Microsoft Edge and try to create a new `EdgeDriver` instance, you get the following error: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'` .</span><span class="sxs-lookup"><span data-stu-id="42dcc-160">If you try to use Selenium 4 with Selenium Tools for Microsoft Edge and try to create a new `EdgeDriver` instance, you get the following error: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'`.</span></span>  

<span data-ttu-id="42dcc-161">Wenn Sie Selenium 4 verwenden und diesen Fehler erhalten, entfernen `Microsoft.Edge.SeleniumTools` Sie es aus Ihrem Projekt, und stellen Sie sicher, dass Sie den Offiziellen und die Klassen aus dem Namespace `EdgeOptions` `EdgeDriver` `OpenQA.Selenium.Edge` verwenden.</span><span class="sxs-lookup"><span data-stu-id="42dcc-161">If you're using Selenium 4 and get this error, remove `Microsoft.Edge.SeleniumTools` from your project, and make sure you're using the official `EdgeOptions` and `EdgeDriver` classes from the `OpenQA.Selenium.Edge` namespace.</span></span>

### <a name="using-selenium-3"></a><span data-ttu-id="42dcc-162">Verwenden von Selenium 3</span><span class="sxs-lookup"><span data-stu-id="42dcc-162">Using Selenium 3</span></span>  

<span data-ttu-id="42dcc-163">Wenn Sie [Selenium 3][|::ref1::|]bereits verwenden, verfügen Sie möglicherweise über vorhandene Browsertests und möchten die Abdeckung für Microsoft Edge \(Chromium\) hinzufügen, ohne Ihre Selenium-Version zu ändern.</span><span class="sxs-lookup"><span data-stu-id="42dcc-163">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="42dcc-164">Um mit [Selenium 3][|::ref2::|] automatisierte Tests für Microsoft Edge \(EdgeHTML\) und Microsoft Edge \(Chromium\) zu schreiben, installieren Sie das Paket [Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools], um den aktualisierten Treiber zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="42dcc-164">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="42dcc-165">Die in den Tools enthaltenen Klassen `EdgeDriver` und `EdgeDriverService` sind vollständig mit den in Selenium 4 integrierten Äquivalenten kompatibel.</span><span class="sxs-lookup"><span data-stu-id="42dcc-165">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="42dcc-166">Führen Sie die folgenden Schritte aus, um die [Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] und [Selenium 3][|::ref3::|] zu Ihrem Projekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-166">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>  

#### [<a name="c"></a><span data-ttu-id="42dcc-167">C#</span><span class="sxs-lookup"><span data-stu-id="42dcc-167">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="42dcc-168">Fügen Sie die Pakete [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] und [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] mithilfe der [NuGet CLI][NugetCLI] oder [Visual Studio][VisualStudio] zu Ihrem .NET-Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="42dcc-168">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<a name="python"></a><span data-ttu-id="42dcc-169">Python</span><span class="sxs-lookup"><span data-stu-id="42dcc-169">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="42dcc-170">Verwenden Sie [pip][PythonPip], um die [msedge-selenium-tools][PythonSeleniumTools] und [selenium][PythonSelenium]-Pakete zu installieren.</span><span class="sxs-lookup"><span data-stu-id="42dcc-170">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a><span data-ttu-id="42dcc-171">Java</span><span class="sxs-lookup"><span data-stu-id="42dcc-171">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="42dcc-172">Wenn Ihr Java Maven verwendet, kopieren Sie die folgende Abhängigkeit und fügen Sie diese in Ihre Datei ein, um `pom.xml` [msedge-selenium-tools-java][SonatypeMavenRepositorySearch] hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-172">If your Java project uses Maven, copy and paste the following dependency to your `pom.xml` file to add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="42dcc-173">Das Java-Paket kann auch direkt auf der Seite [Selenium Tools für Microsoft Edge-Versionen][GithubMicrosoftEdgeSeleniumToolsReleases] heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="42dcc-173">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<a name="javascript"></a><span data-ttu-id="42dcc-174">JavaScript</span><span class="sxs-lookup"><span data-stu-id="42dcc-174">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="42dcc-175">Verwenden Sie [npm][JavaScript|::ref4::|], um die Pakete [edge-selenium-tools][JavaScriptSeleniumTools] und [selenium-webdriver][JavaScriptSelenium] zu installieren.</span><span class="sxs-lookup"><span data-stu-id="42dcc-175">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <a name="automate-microsoft-edge-chromium-with-webdriver"></a><span data-ttu-id="42dcc-176">Automatisieren von Microsoft Edge (Chromium) mit WebDriver</span><span class="sxs-lookup"><span data-stu-id="42dcc-176">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="42dcc-177">Um einen Browser mit WebDriver zu automatisieren, müssen Sie zuerst eine WebDriver-Sitzung mit Ihrer bevorzugten WebDriver-Sprachbindung starten.</span><span class="sxs-lookup"><span data-stu-id="42dcc-177">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver language binding.</span></span>  <span data-ttu-id="42dcc-178">Eine Sitzung ist eine einzelne ausgeführte Instanz eines Browsers, die mithilfe von WebDriver-Befehlen gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="42dcc-178">A session is a single running instance of a browser controlled using WebDriver commands.</span></span>  <span data-ttu-id="42dcc-179">Starten Sie eine WebDriver-Sitzung, um eine neue Browserinstanz zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-179">Start a WebDriver session to launch a new browser instance.</span></span>  <span data-ttu-id="42dcc-180">Die gestartete Browserinstanz bleibt geöffnet, bis Sie die WebDriver-Sitzung schließen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-180">The launched browser instance remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="42dcc-181">Der folgende Inhalt führt Sie durch die Verwendung von Selenium zum Starten einer WebDriver-Sitzung mit Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="42dcc-181">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="42dcc-182">Sie können die Beispiele entweder mit Selenium 3 oder 4 ausführen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-182">You can run the examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="42dcc-183">Zur Verwendung mit Selenium 3 muss das Paket [Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] installiert sein.</span><span class="sxs-lookup"><span data-stu-id="42dcc-183">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <a name="automate-microsoft-edge-chromium"></a><span data-ttu-id="42dcc-184">Automatisieren von Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="42dcc-184">Automate Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="42dcc-185">Selenium verwendet die Klasse `EdgeDriver`, zum Verwalten einer Microsoft Edge \(Chromium\)-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="42dcc-185">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span>  <span data-ttu-id="42dcc-186">Um eine Sitzung zu starten und Microsoft Edge \(Chromium\) zu automatisieren, erstellen Sie ein neues `EdgeDriver` Objekt, und übergeben Sie es an ein `EdgeOptions` mit der festgelegten Eigenschaft `true`.</span><span class="sxs-lookup"><span data-stu-id="42dcc-186">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<a name="c"></a><span data-ttu-id="42dcc-187">C#</span><span class="sxs-lookup"><span data-stu-id="42dcc-187">C#</span></span>](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="42dcc-188">Python</span><span class="sxs-lookup"><span data-stu-id="42dcc-188">Python</span></span>](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="42dcc-189">Java</span><span class="sxs-lookup"><span data-stu-id="42dcc-189">Java</span></span>](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="42dcc-190">Die Klasse `EdgeDriver` unterstützt nur Microsoft Edge \(Chromium\), Microsoft Edge \(EdgeHTML\) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42dcc-190">The `EdgeDriver` class only supports Microsoft Edge \(Chromium\), and doesn't support Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="42dcc-191">Für die grundlegende Verwendung können Sie eine `EdgeDriver` erstellen, ohne `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="42dcc-191">For basic usage, you can create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a><span data-ttu-id="42dcc-192">JavaScript</span><span class="sxs-lookup"><span data-stu-id="42dcc-192">JavaScript</span></span>](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="42dcc-193">Wenn Ihr IT-Administrator die [DeveloperToolsAvailability-Richtlinie][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] auf `2` festgelegt hat, kann der [Microsoft Edge-Treiber][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] Microsoft Edge \(Chromium\) nicht steuern, da der Treiber die [Microsoft Edge DevTools][DevtoolsIndex] verwendet.</span><span class="sxs-lookup"><span data-stu-id="42dcc-193">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`,  [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] is blocked from driving Microsoft Edge \(Chromium\), because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="42dcc-194">Stellen Sie sicher, dass die [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]-Richtlinie auf `0` oder `1` festgelegt ist, um Microsoft Edge (Chromium) zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="42dcc-194">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <a name="choose-specific-browser-binaries-chromium-only"></a><span data-ttu-id="42dcc-195">Auswählen bestimmter Browser-Binärdateien (nur Chromium)</span><span class="sxs-lookup"><span data-stu-id="42dcc-195">Choose Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="42dcc-196">Sie können eine WebDriver-Sitzung mit bestimmten Microsoft Edge \(Chromium\)-Binärdateien starten.</span><span class="sxs-lookup"><span data-stu-id="42dcc-196">You can start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="42dcc-197">Sie können z. B. Tests mithilfe der [Microsoft Edge Vorschaukanäle][MicrosoftedgeinsiderDownload] wie Microsoft Edge Beta ausführen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-197">For example, you can run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<a name="c"></a><span data-ttu-id="42dcc-198">C#</span><span class="sxs-lookup"><span data-stu-id="42dcc-198">C#</span></span>](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="42dcc-199">Python</span><span class="sxs-lookup"><span data-stu-id="42dcc-199">Python</span></span>](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="42dcc-200">Java</span><span class="sxs-lookup"><span data-stu-id="42dcc-200">Java</span></span>](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a><span data-ttu-id="42dcc-201">JavaScript</span><span class="sxs-lookup"><span data-stu-id="42dcc-201">JavaScript</span></span>](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a><span data-ttu-id="42dcc-202">Anpassen des Microsoft Edge-Treiberdiensts</span><span class="sxs-lookup"><span data-stu-id="42dcc-202">Customize the Microsoft Edge Driver Service</span></span>  

#### [<a name="c"></a><span data-ttu-id="42dcc-203">C#</span><span class="sxs-lookup"><span data-stu-id="42dcc-203">C#</span></span>](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="42dcc-204">Wenn Sie die `EdgeOptions` Klasse zum Erstellen einer `EdgeDriver` Klasseninstanz verwenden, wird die entsprechende `EdgeDriverService` Klasse entweder für Microsoft Edge \(EdgeHTML\) oder Microsoft Edge \(Chromium\) erstellt und gestartet.</span><span class="sxs-lookup"><span data-stu-id="42dcc-204">When you use the `EdgeOptions` class to create an `EdgeDriver` class instance, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="42dcc-205">Wenn Sie einen `EdgeDriverService` erstellen möchten, verwenden Sie die `CreateChromiumService()`-Methode, um eine für Microsoft Edge \(Chromium\) konfigurierte Methode zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-205">If you want to create an `EdgeDriverService`, use the `CreateChromiumService()` method to create one configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="42dcc-206">Die `CreateChromiumService()` Methode ist nützlich, wenn Sie Anpassungen hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-206">The `CreateChromiumService()` method is useful when you need to add customizations.</span></span>  <span data-ttu-id="42dcc-207">Der folgende Code startet beispielsweise die ausführliche Protokollausgabe.</span><span class="sxs-lookup"><span data-stu-id="42dcc-207">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="42dcc-208">Sie müssen das `EdgeOptions` Objekt nicht bereitstellen, wenn Sie `EdgeDriverService` an die Instanz `EdgeDriver` übergeben.</span><span class="sxs-lookup"><span data-stu-id="42dcc-208">You do not need to provide the `EdgeOptions` object when you pass `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="42dcc-209">Die `EdgeDriver` Klasse verwendet die Standardoptionen für Microsoft Edge \(EdgeHTML\) oder Microsoft Edge \(Chromium\), basierend auf dem von Ihnen angebotenen Dienst.</span><span class="sxs-lookup"><span data-stu-id="42dcc-209">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="42dcc-210">Wenn Sie jedoch sowohl `EdgeDriverService` als auch `EdgeOptions` Klassen bereitstellen möchten, stellen Sie sicher, dass beide für die gleiche Version von Microsoft Edge konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="42dcc-210">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="42dcc-211">Beispielsweise können Sie eine `EdgeDriverService` Standardklasse für Microsoft Edge \(EdgeHTML\) Chromium-Eigenschaften in der `EdgeOptions` Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="42dcc-211">For example, you may use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="42dcc-212">Die `EdgeDriver` Klasse gibt einen Fehler aus, um die Verwendung unterschiedlicher Versionen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="42dcc-212">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<a name="python"></a><span data-ttu-id="42dcc-213">Python</span><span class="sxs-lookup"><span data-stu-id="42dcc-213">Python</span></span>](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="42dcc-214">Wenn Sie Python verwenden, erstellt und verwaltet das `Edge` Objekt das `EdgeService`.</span><span class="sxs-lookup"><span data-stu-id="42dcc-214">When you use Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="42dcc-215">Um das `EdgeService` zu konfigurieren, übergeben Sie zusätzliche Argumente an das `Edge` Objekt, wie im folgenden Code angegeben.</span><span class="sxs-lookup"><span data-stu-id="42dcc-215">To configure the `EdgeService`, pass extra arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a><span data-ttu-id="42dcc-216">Java</span><span class="sxs-lookup"><span data-stu-id="42dcc-216">Java</span></span>](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="42dcc-217">Verwenden Sie die `createDefaultService()` Methode, um eine `EdgeDriverService` für Microsoft Edge \(Chromium\) konfigurierte Methode zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-217">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="42dcc-218">Verwenden Sie die Java-Systemeigenschaften, um die Treiberdienste in Java anzupassen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-218">Use Java system properties to customize driver services in Java.</span></span>  <span data-ttu-id="42dcc-219">Der folgende Code verwendet beispielsweise die `"webdriver.edge.verboseLogging"` Eigenschaft, um die ausführliche Protokollausgabe zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="42dcc-219">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to turn on verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a><span data-ttu-id="42dcc-220">JavaScript</span><span class="sxs-lookup"><span data-stu-id="42dcc-220">JavaScript</span></span>](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="42dcc-221">Wenn Sie JavaScript verwenden, erstellen und konfigurieren Sie eine `Service` mit der `ServiceBuilder` Klasse.</span><span class="sxs-lookup"><span data-stu-id="42dcc-221">When you use JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="42dcc-222">Optional können Sie das `Service` Objekt an das Objekt `Driver` übergeben, das \(und stoppt\) den Dienst für Sie startet.</span><span class="sxs-lookup"><span data-stu-id="42dcc-222">Optionally, you can pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="42dcc-223">Führen Sie zum Konfigurieren der `Service` eine andere Methode in der `ServiceBuilder` Klasse aus, bevor Sie die `build()` Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="42dcc-223">To configure the `Service`, run another method in the `ServiceBuilder` class before you use the `build()` method.</span></span>  <span data-ttu-id="42dcc-224">Übergeben Sie dann `service` als Parameter in der `Driver.createSession()`-Methode.</span><span class="sxs-lookup"><span data-stu-id="42dcc-224">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a><span data-ttu-id="42dcc-225">Verwenden von Chromium-spezifischer Optionen</span><span class="sxs-lookup"><span data-stu-id="42dcc-225">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="42dcc-226">Wenn Sie die `UseChromium` Eigenschaft auf `true` festlegen, können Sie mithilfe der `EdgeOptions` Klasse auf dieselben [Chromium-spezifischen Eigenschaften und Methoden][WebdriverCapabilitiesEdgeOptions] zugreifen, die verwendet werden, wenn Sie andere Chromium Browser automatisieren.</span><span class="sxs-lookup"><span data-stu-id="42dcc-226">If you set the `UseChromium` property to `true`, you can use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when you automate other Chromium browsers.</span></span>  

#### [<a name="c"></a><span data-ttu-id="42dcc-227">C#</span><span class="sxs-lookup"><span data-stu-id="42dcc-227">C#</span></span>](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a><span data-ttu-id="42dcc-228">Python</span><span class="sxs-lookup"><span data-stu-id="42dcc-228">Python</span></span>](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a><span data-ttu-id="42dcc-229">Java</span><span class="sxs-lookup"><span data-stu-id="42dcc-229">Java</span></span>](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a><span data-ttu-id="42dcc-230">JavaScript</span><span class="sxs-lookup"><span data-stu-id="42dcc-230">JavaScript</span></span>](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="42dcc-231">Wenn die `UseChromium` Eigenschaft auf `true` festgelegt ist, können Sie keine Eigenschaften und Methoden für Microsoft Edge \(EdgeHTML\) verwenden.</span><span class="sxs-lookup"><span data-stu-id="42dcc-231">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <a name="other-webdriver-installation-options"></a><span data-ttu-id="42dcc-232">Andere WebDriver-Installationsoptionen</span><span class="sxs-lookup"><span data-stu-id="42dcc-232">Other WebDriver installation options</span></span>  

### <a name="docker"></a><span data-ttu-id="42dcc-233">Docker</span><span class="sxs-lookup"><span data-stu-id="42dcc-233">Docker</span></span>  

<span data-ttu-id="42dcc-234">Wenn Sie [Docker][DockerHub] verwenden, führen Sie den folgenden Befehl aus, um ein vorkonfiguriertes Image mit vorinstalliertem Microsoft Edge \(Chromium\) und [Microsoft Edge-Treiber][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-234">If you use [Docker][DockerHub], run the following command to download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pre-installed.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="42dcc-235">Weitere Informationen finden Sie im [msedgedriver-Container auf Docker Hub][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="42dcc-235">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <a name="testing-internet-explorer"></a><span data-ttu-id="42dcc-236">Testen von Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="42dcc-236">Testing Internet Explorer</span></span>

<span data-ttu-id="42dcc-237">Obwohl Microsoft Edge den IE-Modus unterstützt, können Sie Microsoft Edge Treiber nicht mit Microsoft Edge verwenden, um Websites im IE-Modus zu testen.</span><span class="sxs-lookup"><span data-stu-id="42dcc-237">Even though Microsoft Edge supports IE Mode, you can't use Microsoft Edge Driver with Microsoft Edge to test sites in IE Mode.</span></span>  <span data-ttu-id="42dcc-238">Um Websites zu testen, die Internet Explorer erfordern, verwenden Sie [Internet Explorer-Treiber][GithubSeleniumHqWikiIEDriver] mit Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="42dcc-238">To test sites that require Internet Explorer, use [Internet Explorer Driver][GithubSeleniumHqWikiIEDriver] with Internet Explorer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="42dcc-239">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="42dcc-239">Next steps</span></span>  

<span data-ttu-id="42dcc-240">Weitere Informationen zu WebDriver und zum Schreiben automatisierter WebDriver-Tests mit Selenium finden Sie in der [Selenium-Dokumentation.][SeleniumDocumentation]</span><span class="sxs-lookup"><span data-stu-id="42dcc-240">For more information about WebDriver and how to write automated WebDriver tests using Selenium, navigate to the [Selenium documentation][SeleniumDocumentation].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="42dcc-241">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="42dcc-241">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="42dcc-242">Das Microsoft Edge-Team freut sich über Ihr Feedback zur Verwendung von WebDriver, Selenium und Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="42dcc-242">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="42dcc-243">Um dem Team Ihre Fragen und Kommentare zu senden, wählen Sie das Symbol **Feedback senden** in den Microsoft Edge DevTools aus, oder senden Sie einen Tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="42dcc-243">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol „Feedback senden“ in den Microsoft Edge-Entwicklungstools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="42dcc-245">Das Symbol **Feedback senden** in den Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="42dcc-245">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Funktionen und EdgeOptions | Microsoft Docs"  

<!--[Webdriver]: /archive/microsoft-edge/legacy/developer/webdriver/index "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability – Microsoft Edge – Richtlinien | Microsoft Docs"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Docker hub"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  
[GithubSeleniumHqWikiIEDriver]: https://github.com/SeleniumHQ/selenium/wiki/InternetExplorerDriver "Internet Explorer-Treiber – Selenium | GitHub"

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Microsoft Edge Treiber | Microsoft Edge Entwickler"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Den neuen Microsoft Edge-Browser herunterladen"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | NuGet Gallery"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | NuGet Gallery"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | NuGet Gallery"  
[NugetPackagesSeleniumWebdriver400beta02]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-beta2 "Selenium.WebDriver 4.0.0-beta2 | NuGet Galerie"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "Das Selenium Browser Automation Project | Dokumentation für Selenium"  
[SeleniumDownloads]: https://selenium.dev/downloads "Downloads | Selen"  
[SeleniumInstallingLibraries]: https://www.selenium.dev/documentation/en/selenium_installation/installing_selenium_libraries "Installieren von Selenium-Bibliotheken | Selen"

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "Sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Veröffentlichen eines Tweets"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Monitorlose Browser-| Wikipedia"  
