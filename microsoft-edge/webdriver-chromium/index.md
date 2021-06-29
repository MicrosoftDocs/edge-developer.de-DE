---
description: Erfahren Sie, wie Sie Ihre Website oder App in Microsoft Edge testen oder den Browser mit WebDriver automatisieren
title: Verwenden von WebDriver (Chromium) für die Testautomatisierung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, HTML, CSS, Javascript, Entwickler, WebDriver, Selenium, Tests, Tools, Automatisierung, Test
ms.openlocfilehash: a1ec308fc1412ead27c4776ce0ccc2e873376652
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624675"
---
# <a name="use-webdriver-chromium-for-test-automation"></a><span data-ttu-id="c9bac-104">Verwenden von WebDriver (Chromium) für die Testautomatisierung</span><span class="sxs-lookup"><span data-stu-id="c9bac-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="c9bac-105">Mit WebDriver können Entwickler automatisierte Tests erstellen, welche die Benutzerinteraktion simulieren.</span><span class="sxs-lookup"><span data-stu-id="c9bac-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="c9bac-106">WebDriver-Tests und -Simulationen unterscheiden sich in folgenden Punkten von JavaScript-Komponententests.</span><span class="sxs-lookup"><span data-stu-id="c9bac-106">WebDriver tests and simulations differ from JavaScript unit tests in the following ways.</span></span>  

*   <span data-ttu-id="c9bac-107">Greift auf Funktionen und Informationen zu, die JavaScript in Browsern nicht zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="c9bac-108">Simuliert Benutzerereignisse oder Ereignisse auf Betriebssystemebene genauer.</span><span class="sxs-lookup"><span data-stu-id="c9bac-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="c9bac-109">Verwaltet mehrere Fenster, Registerkarten und Webseiten in einer einzigen Testsitzung.</span><span class="sxs-lookup"><span data-stu-id="c9bac-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="c9bac-110">Führt mehrere Sitzungen von Microsoft Edge auf einem bestimmten Computer aus.</span><span class="sxs-lookup"><span data-stu-id="c9bac-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  


## <a name="relationship-between-webdriver-and-other-software"></a><span data-ttu-id="c9bac-111">Beziehung zwischen WebDriver und anderer Software</span><span class="sxs-lookup"><span data-stu-id="c9bac-111">Relationship between WebDriver and other software</span></span>

<span data-ttu-id="c9bac-112">Um Microsoft Edge mit WebDriver zu automatisieren, um Benutzerinteraktionen zu simulieren, benötigen Sie drei Komponenten:</span><span class="sxs-lookup"><span data-stu-id="c9bac-112">To automate Microsoft Edge with WebDriver to simulate user interaction, you need three components:</span></span>

*  <span data-ttu-id="c9bac-113">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c9bac-113">Microsoft Edge</span></span>
*  <span data-ttu-id="c9bac-114">Microsoft Edge-Treiber</span><span class="sxs-lookup"><span data-stu-id="c9bac-114">Microsoft Edge Driver</span></span>
*  <span data-ttu-id="c9bac-115">WebDriver-Testframework</span><span class="sxs-lookup"><span data-stu-id="c9bac-115">A WebDriver testing framework</span></span>

<span data-ttu-id="c9bac-116">Die funktionale Beziehung zwischen diesen Komponenten lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="c9bac-116">The functional relationship between these components is as follows.</span></span>

| <span data-ttu-id="c9bac-117">Technologie</span><span class="sxs-lookup"><span data-stu-id="c9bac-117">Technology</span></span> | <span data-ttu-id="c9bac-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="c9bac-118">Role</span></span> |
|---|---|
| <span data-ttu-id="c9bac-119">WebDriver</span><span class="sxs-lookup"><span data-stu-id="c9bac-119">WebDriver</span></span> | <span data-ttu-id="c9bac-120">Ein W3C-Standard für ein plattform- und sprachneutrales Kabelprotokoll.</span><span class="sxs-lookup"><span data-stu-id="c9bac-120">A W3C standard for a platform- and language-neutral wire protocol.</span></span>  <span data-ttu-id="c9bac-121">Mit diesem Protokoll können Out-of-Process-Programme remote das Verhalten von Webbrowsern anweisen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-121">This protocol allows out-of-process programs to remotely instruct the behavior of web browsers.</span></span> |
| <span data-ttu-id="c9bac-122">Microsoft Edge-Treiber</span><span class="sxs-lookup"><span data-stu-id="c9bac-122">Microsoft Edge Driver</span></span> | <span data-ttu-id="c9bac-123">Microsoft-Implementierung des WebDriver-Protokolls speziell für Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c9bac-123">Microsoft's implementation of the WebDriver protocol specifically for Microsoft Edge.</span></span>  <span data-ttu-id="c9bac-124">Testautoren schreiben Tests, die WebDriver-Befehle verwenden, die Microsoft Edge Treiber empfängt.</span><span class="sxs-lookup"><span data-stu-id="c9bac-124">Test authors write tests that use WebDriver commands that Microsoft Edge Driver receives.</span></span>  <span data-ttu-id="c9bac-125">Microsoft Edge Der Treiber ist dann für die Kommunikation dieses Befehls mit dem Browser verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="c9bac-125">Microsoft Edge Driver is then responsible for communicating that command to the browser.</span></span> |
| <span data-ttu-id="c9bac-126">WebDriver-Testframework</span><span class="sxs-lookup"><span data-stu-id="c9bac-126">A WebDriver testing framework</span></span> | <span data-ttu-id="c9bac-127">Testautoren verwenden ein Testframework, um End-to-End-Tests zu schreiben und Browser zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="c9bac-127">Test authors use a testing framework to write end-to-end tests and automate browsers.</span></span>  <span data-ttu-id="c9bac-128">Stellt eine sprachspezifische Schnittstelle bereit, die Ihren Code in Befehle übersetzt, die Microsoft Edge Treiber in Microsoft Edge \(Chromium\) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9bac-128">Provides a language-specific interface that translates your code into commands that Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="c9bac-129">WebDriver-Testframeworks sind für alle wichtigen Plattformen und Sprachen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c9bac-129">WebDriver testing frameworks exist for all major platforms and languages.</span></span>  <span data-ttu-id="c9bac-130">Ein solches Framework ist Selenium.</span><span class="sxs-lookup"><span data-stu-id="c9bac-130">One such framework is Selenium.</span></span> |
| <span data-ttu-id="c9bac-131">Internet Explorer-Treiber</span><span class="sxs-lookup"><span data-stu-id="c9bac-131">Internet Explorer Driver</span></span> | <span data-ttu-id="c9bac-132">Eine Implementierung des WebDriver-Protokolls speziell für Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c9bac-132">An implementation of the WebDriver protocol specifically for Internet Explorer.</span></span>  <span data-ttu-id="c9bac-133">Um ältere End-to-End-Tests für Internet Explorer auszuführen, empfehlen wir die Verwendung des Internet Explorer-Treibers.</span><span class="sxs-lookup"><span data-stu-id="c9bac-133">To run legacy end-to-end tests for Internet Explorer, we recommend using Internet Explorer Driver.</span></span> |

<span data-ttu-id="c9bac-134">In den folgenden Abschnitten wird beschrieben, wie Sie mit WebDriver für Microsoft Edge \(Chromium\) beginnen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-134">The following sections describe how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  


## <a name="install-microsoft-edge-chromium"></a><span data-ttu-id="c9bac-135">Installieren von Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="c9bac-135">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="c9bac-136">Stellen Sie sicher, dass Sie [Microsoft Edge (Chromium)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="c9bac-136">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="c9bac-137">Um zu bestätigen, dass Microsoft Edge \(Chromium\) installiert ist, navigieren Sie zu `edge://settings/help` und überprüfen Sie, ob die Versionsnummer 75 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="c9bac-137">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify that the version number is 75 or later.</span></span>


## <a name="download-microsoft-edge-driver"></a><span data-ttu-id="c9bac-138">Herunterladen des Microsoft Edge-Treibers</span><span class="sxs-lookup"><span data-stu-id="c9bac-138">Download Microsoft Edge Driver</span></span>

<span data-ttu-id="c9bac-139">Führen Sie die folgenden Schritte aus, um die Automatisierung von Tests zu starten und sicherzustellen, dass die von Ihnen installierte WebDriver-Version mit Ihrer Browserversion übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c9bac-139">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="c9bac-140">Suchen Sie Ihre Version von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c9bac-140">Find your version of Microsoft Edge.</span></span>  
    1.  <span data-ttu-id="c9bac-141">Navigieren Sie zu `edge://settings/help`.</span><span class="sxs-lookup"><span data-stu-id="c9bac-141">Navigate to `edge://settings/help`.</span></span>  
        
        :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="Die Buildnummer für Microsoft Edge am 15. April 2021" lightbox="./media/microsoft-edge-version.msft.png":::
           <span data-ttu-id="c9bac-143">Die Buildnummer für Microsoft Edge am 15. April 2021</span><span class="sxs-lookup"><span data-stu-id="c9bac-143">The build number for Microsoft Edge on April 15, 2021</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="c9bac-144">Navigieren Sie zu [Microsoft Edge Treiber.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="c9bac-144">Navigate to [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  
1.  <span data-ttu-id="c9bac-145">Navigieren Sie zu **"Aktuelle Version abrufen".**</span><span class="sxs-lookup"><span data-stu-id="c9bac-145">Navigate to **Get the latest version**.</span></span>  
1.  <span data-ttu-id="c9bac-146">Wählen Sie den Build des Kanals aus, der ihrer Versionsnummer von Microsoft Edge entspricht.</span><span class="sxs-lookup"><span data-stu-id="c9bac-146">Choose the build of channel that matches your version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="Der Abschnitt "Aktuelle Version abrufen" auf der Webseite "Microsoft Edge Treiber"" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       <span data-ttu-id="c9bac-148">Der Abschnitt **"Aktuelle Version abrufen"** auf der Webseite ["Microsoft Edge Treiber"][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="c9bac-148">The **Get the latest version** section on the [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] webpage</span></span>  
    :::image-end:::  
   
    
## <a name="choose-a-webdriver-testing-framework"></a><span data-ttu-id="c9bac-149">Auswählen eines WebDriver-Testframeworks</span><span class="sxs-lookup"><span data-stu-id="c9bac-149">Choose a WebDriver testing framework</span></span>

<span data-ttu-id="c9bac-150">Nach dem Herunterladen Microsoft Edge Treibers ist die letzte Komponente, die Sie herunterladen müssen, ein WebDriver-Testframework.</span><span class="sxs-lookup"><span data-stu-id="c9bac-150">After downloading Microsoft Edge Driver, the last component you must download is a WebDriver testing framework.</span></span> <span data-ttu-id="c9bac-151">Testautoren verwenden WebDriver-Testframeworks, um End-to-End-Tests zu schreiben und Browser zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="c9bac-151">Test authors use WebDriver testing frameworks to write end-to-end tests and automate browsers.</span></span> <span data-ttu-id="c9bac-152">Das Framework bietet eine sprachspezifische Schnittstelle, die Ihren Code (z. B. Python, Java, C#, Ruby oder JavaScript) in Befehle übersetzt, die Microsoft Edge Treiber in Microsoft Edge \(Chromium\) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9bac-152">The framework provides a language-specific interface that translates your code (such as Python, Java, C#, Ruby, or JavaScript) into commands that Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span> <span data-ttu-id="c9bac-153">WebDriver-Testframeworks sind für alle wichtigen Plattformen und Sprachen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c9bac-153">WebDriver testing frameworks exist for all major platforms and languages.</span></span>


<span data-ttu-id="c9bac-154">Dieser Artikel enthält Anweisungen für die Verwendung des Selenium-Frameworks, Sie können jedoch eine beliebige Bibliothek, jedes Framework und jede Programmiersprache verwenden, die WebDriver unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9bac-154">This article provides instructions for using the Selenium framework, but you can use any library, framework, and programming language that supports WebDriver.</span></span>  <span data-ttu-id="c9bac-155">Um die gleichen Aufgaben mit einem anderen WebDriver-Testframework als Selenium auszuführen, lesen Sie die offizielle Dokumentation ihres bevorzugten Frameworks.</span><span class="sxs-lookup"><span data-stu-id="c9bac-155">To accomplish the same tasks using a WebDriver testing framework other than Selenium, consult the official documentation for your framework of choice.</span></span>

<span data-ttu-id="c9bac-156">Wenn Sie Selenium verwenden, empfiehlt das Microsoft Edge Team [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] oder höher, da diese Version von Selenium Microsoft Edge \(Chromium\) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9bac-156">If you are using Selenium, the Microsoft Edge team recommends [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] or later, because that version of Selenium supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="c9bac-157">Sie können jedoch Microsoft Edge \(Chromium\) in allen älteren Versionen von Selenium steuern, einschließlich der aktuellen stabilen Selenium 3-Version.</span><span class="sxs-lookup"><span data-stu-id="c9bac-157">However, you can control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="c9bac-158">Wenn Sie zuvor Microsoft Edge \(Chromium\) mit `ChromeDriver` und `ChromeOptions` Klassen automatisiert oder getestet haben, automatisiert oder getestet haben, wird Ihr WebDriver-Code nicht unter Microsoft Edge Version 80 oder höher ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9bac-158">If you previously automated or tested Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="c9bac-159">Um das Problem zu beheben, aktualisieren Sie Ihre Tests, um die Klasse `EdgeOptions` verwenden, und laden Sie [Microsoft Edge-Treiber][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] herunter.</span><span class="sxs-lookup"><span data-stu-id="c9bac-159">To solve the problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  

### <a name="using-selenium-4"></a><span data-ttu-id="c9bac-160">Verwenden von Selenium 4</span><span class="sxs-lookup"><span data-stu-id="c9bac-160">Using Selenium 4</span></span>

<span data-ttu-id="c9bac-161">Das Selenium WebDriver-Testframework kann auf jeder Plattform verwendet werden und ist für Java, Python, C#, Ruby und JavaScript verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c9bac-161">The Selenium WebDriver testing framework can be used on any platform, and is available for Java, Python, C#, Ruby, and JavaScript.</span></span>

<span data-ttu-id="c9bac-162">Selenium 4 bietet integrierte Unterstützung für Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="c9bac-162">Selenium 4 has built-in support for Microsoft Edge (Chromium).</span></span>  <span data-ttu-id="c9bac-163">Navigieren Sie zum Installieren von Selenium 4 zu ["Selenium-Bibliotheken installieren".][SeleniumInstallingLibraries]</span><span class="sxs-lookup"><span data-stu-id="c9bac-163">To install Selenium 4, navigate to [Installing Selenium libraries][SeleniumInstallingLibraries].</span></span>

<span data-ttu-id="c9bac-164">Wenn Sie Selenium 4 verwenden, müssen Sie selenium-Tools nicht für Microsoft Edge verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9bac-164">If you use Selenium 4, you don't need to use Selenium Tools for Microsoft Edge.</span></span>  <span data-ttu-id="c9bac-165">Selenium-Tools für Microsoft Edge gelten nur für Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="c9bac-165">Selenium Tools for Microsoft Edge are for Selenium 3 only.</span></span>  <span data-ttu-id="c9bac-166">If you try to use Selenium 4 with Selenium Tools for Microsoft Edge and try to create a new `EdgeDriver` instance, you get the following error: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'` .</span><span class="sxs-lookup"><span data-stu-id="c9bac-166">If you try to use Selenium 4 with Selenium Tools for Microsoft Edge and try to create a new `EdgeDriver` instance, you get the following error: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'`.</span></span>  

<span data-ttu-id="c9bac-167">Wenn Sie Selenium 4 verwenden und diesen Fehler erhalten, entfernen `Microsoft.Edge.SeleniumTools` Sie es aus Ihrem Projekt, und stellen Sie sicher, dass Sie den Offiziellen und die Klassen aus dem Namespace `EdgeOptions` `EdgeDriver` `OpenQA.Selenium.Edge` verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9bac-167">If you're using Selenium 4 and get this error, remove `Microsoft.Edge.SeleniumTools` from your project, and make sure you're using the official `EdgeOptions` and `EdgeDriver` classes from the `OpenQA.Selenium.Edge` namespace.</span></span>

### <a name="using-selenium-3"></a><span data-ttu-id="c9bac-168">Verwenden von Selenium 3</span><span class="sxs-lookup"><span data-stu-id="c9bac-168">Using Selenium 3</span></span>  

<span data-ttu-id="c9bac-169">Wenn Sie [Selenium 3][|::ref1::|]bereits verwenden, verfügen Sie möglicherweise über vorhandene Browsertests und möchten die Abdeckung für Microsoft Edge \(Chromium\) hinzufügen, ohne Ihre Selenium-Version zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c9bac-169">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="c9bac-170">Um mit [Selenium 3][|::ref2::|] automatisierte Tests für Microsoft Edge \(EdgeHTML\) und Microsoft Edge \(Chromium\) zu schreiben, installieren Sie das Paket [Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools], um den aktualisierten Treiber zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9bac-170">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="c9bac-171">Die in den Tools enthaltenen Klassen `EdgeDriver` und `EdgeDriverService` sind vollständig mit den in Selenium 4 integrierten Äquivalenten kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c9bac-171">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="c9bac-172">Wenn Sie Selenium 3 verwenden, führen Sie die folgenden Schritte aus, um Ihrem Projekt die [Selenium-Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] und [Selenium 3][|::ref3::|] hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-172">If you are using Selenium 3, use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>

#### [<a name="c"></a><span data-ttu-id="c9bac-173">C#</span><span class="sxs-lookup"><span data-stu-id="c9bac-173">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="c9bac-174">Fügen Sie die Pakete [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] und [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] mithilfe der [NuGet CLI][NugetCLI] oder [Visual Studio][VisualStudio] zu Ihrem .NET-Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9bac-174">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<a name="python"></a><span data-ttu-id="c9bac-175">Python</span><span class="sxs-lookup"><span data-stu-id="c9bac-175">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="c9bac-176">Verwenden Sie [pip][PythonPip], um die [msedge-selenium-tools][PythonSeleniumTools] und [selenium][PythonSelenium]-Pakete zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c9bac-176">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a><span data-ttu-id="c9bac-177">Java</span><span class="sxs-lookup"><span data-stu-id="c9bac-177">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="c9bac-178">Wenn Ihr Java Maven verwendet, kopieren Sie die folgende Abhängigkeit und fügen Sie diese in Ihre Datei ein, um `pom.xml` [msedge-selenium-tools-java][SonatypeMavenRepositorySearch] hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-178">If your Java project uses Maven, copy and paste the following dependency to your `pom.xml` file to add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="c9bac-179">Das Java-Paket kann auch direkt auf der Seite [Selenium Tools für Microsoft Edge-Versionen][GithubMicrosoftEdgeSeleniumToolsReleases] heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c9bac-179">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<a name="javascript"></a><span data-ttu-id="c9bac-180">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c9bac-180">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="c9bac-181">Verwenden Sie [npm][JavaScript|::ref4::|], um die Pakete [edge-selenium-tools][JavaScriptSeleniumTools] und [selenium-webdriver][JavaScriptSelenium] zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c9bac-181">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  


## <a name="automate-microsoft-edge-chromium-with-webdriver"></a><span data-ttu-id="c9bac-182">Automatisieren von Microsoft Edge (Chromium) mit WebDriver</span><span class="sxs-lookup"><span data-stu-id="c9bac-182">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="c9bac-183">Um einen Browser mitHilfe von WebDriver zu automatisieren, müssen Sie zunächst eine WebDriver-Sitzung mit Ihrem bevorzugten WebDriver-Testframework starten.</span><span class="sxs-lookup"><span data-stu-id="c9bac-183">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver testing framework.</span></span>  <span data-ttu-id="c9bac-184">Eine Sitzung ist eine einzelne ausgeführte Instanz eines Browsers, die mithilfe von WebDriver-Befehlen gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="c9bac-184">A session is a single running instance of a browser controlled using WebDriver commands.</span></span>  <span data-ttu-id="c9bac-185">Starten Sie eine WebDriver-Sitzung, um eine neue Browserinstanz zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-185">Start a WebDriver session to launch a new browser instance.</span></span>  <span data-ttu-id="c9bac-186">Die gestartete Browserinstanz bleibt geöffnet, bis Sie die WebDriver-Sitzung schließen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-186">The launched browser instance remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="c9bac-187">Der folgende Inhalt führt Sie durch die Verwendung von Selenium zum Starten einer WebDriver-Sitzung mit Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="c9bac-187">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="c9bac-188">Sie können diese Beispiele entweder mit Selenium 3 oder 4 ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-188">You can run these examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="c9bac-189">Um WebDriver mit Selenium 3 zu verwenden, müssen die [Selenium-Tools für Microsoft Edge-Paket][GithubMicrosoftEdgeSeleniumTools] installiert sein.</span><span class="sxs-lookup"><span data-stu-id="c9bac-189">To use WebDriver with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

> [!NOTE]
> <span data-ttu-id="c9bac-190">Dieser Artikel enthält Anweisungen für die Verwendung des Selenium-Frameworks, Sie können jedoch eine beliebige Bibliothek, jedes Framework und jede Programmiersprache verwenden, die WebDriver unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9bac-190">This article provides instructions for using the Selenium framework, but you can use any library, framework, and programming language that supports WebDriver.</span></span>  <span data-ttu-id="c9bac-191">Wenn Sie die gleichen Aufgaben mit einem anderen Framework ausführen möchten, lesen Sie die offizielle Dokumentation ihres bevorzugten Frameworks.</span><span class="sxs-lookup"><span data-stu-id="c9bac-191">To accomplish the same tasks using another framework, consult the official documentation for your framework of choice.</span></span>

### <a name="automate-microsoft-edge-chromium"></a><span data-ttu-id="c9bac-192">Automatisieren von Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="c9bac-192">Automate Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="c9bac-193">Selenium verwendet die Klasse `EdgeDriver`, zum Verwalten einer Microsoft Edge \(Chromium\)-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c9bac-193">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span>  <span data-ttu-id="c9bac-194">Um eine Sitzung zu starten und Microsoft Edge \(Chromium\) zu automatisieren, erstellen Sie ein neues `EdgeDriver` Objekt, und übergeben Sie es an ein `EdgeOptions` mit der festgelegten Eigenschaft `true`.</span><span class="sxs-lookup"><span data-stu-id="c9bac-194">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<a name="c"></a><span data-ttu-id="c9bac-195">C#</span><span class="sxs-lookup"><span data-stu-id="c9bac-195">C#</span></span>](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="c9bac-196">Python</span><span class="sxs-lookup"><span data-stu-id="c9bac-196">Python</span></span>](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="c9bac-197">Java</span><span class="sxs-lookup"><span data-stu-id="c9bac-197">Java</span></span>](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="c9bac-198">Die Klasse `EdgeDriver` unterstützt nur Microsoft Edge \(Chromium\), Microsoft Edge \(EdgeHTML\) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9bac-198">The `EdgeDriver` class only supports Microsoft Edge \(Chromium\), and doesn't support Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="c9bac-199">Für die grundlegende Verwendung können Sie eine `EdgeDriver` erstellen, ohne `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="c9bac-199">For basic usage, you can create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a><span data-ttu-id="c9bac-200">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c9bac-200">JavaScript</span></span>](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="c9bac-201">Wenn Ihr IT-Administrator die [DeveloperToolsAvailability-Richtlinie][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] auf `2` festgelegt hat, kann der [Microsoft Edge-Treiber][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] Microsoft Edge \(Chromium\) nicht steuern, da der Treiber die [Microsoft Edge DevTools][DevtoolsIndex] verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9bac-201">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`,  [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] is blocked from driving Microsoft Edge \(Chromium\), because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="c9bac-202">Stellen Sie sicher, dass die [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]-Richtlinie auf `0` oder `1` festgelegt ist, um Microsoft Edge (Chromium) zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="c9bac-202">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <a name="choose-specific-browser-binaries-chromium-only"></a><span data-ttu-id="c9bac-203">Auswählen bestimmter Browser-Binärdateien (nur Chromium)</span><span class="sxs-lookup"><span data-stu-id="c9bac-203">Choose Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="c9bac-204">Sie können eine WebDriver-Sitzung mit bestimmten Microsoft Edge \(Chromium\)-Binärdateien starten.</span><span class="sxs-lookup"><span data-stu-id="c9bac-204">You can start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="c9bac-205">Sie können z. B. Tests mithilfe der [Microsoft Edge Vorschaukanäle][MicrosoftedgeinsiderDownload] wie Microsoft Edge Beta ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-205">For example, you can run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<a name="c"></a><span data-ttu-id="c9bac-206">C#</span><span class="sxs-lookup"><span data-stu-id="c9bac-206">C#</span></span>](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="c9bac-207">Python</span><span class="sxs-lookup"><span data-stu-id="c9bac-207">Python</span></span>](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="c9bac-208">Java</span><span class="sxs-lookup"><span data-stu-id="c9bac-208">Java</span></span>](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a><span data-ttu-id="c9bac-209">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c9bac-209">JavaScript</span></span>](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a><span data-ttu-id="c9bac-210">Anpassen des Microsoft Edge-Treiberdiensts</span><span class="sxs-lookup"><span data-stu-id="c9bac-210">Customize the Microsoft Edge Driver Service</span></span>  

#### [<a name="c"></a><span data-ttu-id="c9bac-211">C#</span><span class="sxs-lookup"><span data-stu-id="c9bac-211">C#</span></span>](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="c9bac-212">Wenn Sie die `EdgeOptions` Klasse zum Erstellen einer `EdgeDriver` Klasseninstanz verwenden, wird die entsprechende `EdgeDriverService` Klasse entweder für Microsoft Edge \(EdgeHTML\) oder Microsoft Edge \(Chromium\) erstellt und gestartet.</span><span class="sxs-lookup"><span data-stu-id="c9bac-212">When you use the `EdgeOptions` class to create an `EdgeDriver` class instance, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="c9bac-213">Wenn Sie einen `EdgeDriverService` erstellen möchten, verwenden Sie die `CreateChromiumService()`-Methode, um eine für Microsoft Edge \(Chromium\) konfigurierte Methode zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-213">If you want to create an `EdgeDriverService`, use the `CreateChromiumService()` method to create one configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="c9bac-214">Die `CreateChromiumService()` Methode ist nützlich, wenn Sie Anpassungen hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-214">The `CreateChromiumService()` method is useful when you need to add customizations.</span></span>  <span data-ttu-id="c9bac-215">Der folgende Code startet beispielsweise die ausführliche Protokollausgabe.</span><span class="sxs-lookup"><span data-stu-id="c9bac-215">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="c9bac-216">Sie müssen das `EdgeOptions` Objekt nicht bereitstellen, wenn Sie `EdgeDriverService` an die Instanz `EdgeDriver` übergeben.</span><span class="sxs-lookup"><span data-stu-id="c9bac-216">You do not need to provide the `EdgeOptions` object when you pass `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="c9bac-217">Die `EdgeDriver` Klasse verwendet die Standardoptionen für Microsoft Edge \(EdgeHTML\) oder Microsoft Edge \(Chromium\), basierend auf dem von Ihnen angebotenen Dienst.</span><span class="sxs-lookup"><span data-stu-id="c9bac-217">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="c9bac-218">Wenn Sie jedoch sowohl `EdgeDriverService` als auch `EdgeOptions` Klassen bereitstellen möchten, stellen Sie sicher, dass beide für die gleiche Version von Microsoft Edge konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="c9bac-218">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="c9bac-219">Beispielsweise können Sie eine `EdgeDriverService` Standardklasse für Microsoft Edge \(EdgeHTML\) Chromium-Eigenschaften in der `EdgeOptions` Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9bac-219">For example, you may use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="c9bac-220">Die `EdgeDriver` Klasse gibt einen Fehler aus, um die Verwendung unterschiedlicher Versionen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="c9bac-220">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<a name="python"></a><span data-ttu-id="c9bac-221">Python</span><span class="sxs-lookup"><span data-stu-id="c9bac-221">Python</span></span>](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="c9bac-222">Wenn Sie Python verwenden, erstellt und verwaltet das `Edge` Objekt das `EdgeService`.</span><span class="sxs-lookup"><span data-stu-id="c9bac-222">When you use Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="c9bac-223">Um das `EdgeService` zu konfigurieren, übergeben Sie zusätzliche Argumente an das `Edge` Objekt, wie im folgenden Code angegeben.</span><span class="sxs-lookup"><span data-stu-id="c9bac-223">To configure the `EdgeService`, pass extra arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a><span data-ttu-id="c9bac-224">Java</span><span class="sxs-lookup"><span data-stu-id="c9bac-224">Java</span></span>](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="c9bac-225">Verwenden Sie die `createDefaultService()` Methode, um eine `EdgeDriverService` für Microsoft Edge \(Chromium\) konfigurierte Methode zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-225">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="c9bac-226">Verwenden Sie die Java-Systemeigenschaften, um die Treiberdienste in Java anzupassen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-226">Use Java system properties to customize driver services in Java.</span></span>  <span data-ttu-id="c9bac-227">Der folgende Code verwendet beispielsweise die `"webdriver.edge.verboseLogging"` Eigenschaft, um die ausführliche Protokollausgabe zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c9bac-227">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to turn on verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a><span data-ttu-id="c9bac-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c9bac-228">JavaScript</span></span>](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="c9bac-229">Wenn Sie JavaScript verwenden, erstellen und konfigurieren Sie eine `Service` mit der `ServiceBuilder` Klasse.</span><span class="sxs-lookup"><span data-stu-id="c9bac-229">When you use JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="c9bac-230">Optional können Sie das `Service` Objekt an das Objekt `Driver` übergeben, das \(und stoppt\) den Dienst für Sie startet.</span><span class="sxs-lookup"><span data-stu-id="c9bac-230">Optionally, you can pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="c9bac-231">Führen Sie zum Konfigurieren der `Service` eine andere Methode in der `ServiceBuilder` Klasse aus, bevor Sie die `build()` Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9bac-231">To configure the `Service`, run another method in the `ServiceBuilder` class before you use the `build()` method.</span></span>  <span data-ttu-id="c9bac-232">Übergeben Sie dann `service` als Parameter in der `Driver.createSession()`-Methode.</span><span class="sxs-lookup"><span data-stu-id="c9bac-232">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a><span data-ttu-id="c9bac-233">Verwenden von Chromium-spezifischer Optionen</span><span class="sxs-lookup"><span data-stu-id="c9bac-233">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="c9bac-234">Wenn Sie die `UseChromium` Eigenschaft auf `true` festlegen, können Sie mithilfe der `EdgeOptions` Klasse auf dieselben [Chromium-spezifischen Eigenschaften und Methoden][WebdriverCapabilitiesEdgeOptions] zugreifen, die verwendet werden, wenn Sie andere Chromium Browser automatisieren.</span><span class="sxs-lookup"><span data-stu-id="c9bac-234">If you set the `UseChromium` property to `true`, you can use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when you automate other Chromium browsers.</span></span>  

#### [<a name="c"></a><span data-ttu-id="c9bac-235">C#</span><span class="sxs-lookup"><span data-stu-id="c9bac-235">C#</span></span>](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a><span data-ttu-id="c9bac-236">Python</span><span class="sxs-lookup"><span data-stu-id="c9bac-236">Python</span></span>](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a><span data-ttu-id="c9bac-237">Java</span><span class="sxs-lookup"><span data-stu-id="c9bac-237">Java</span></span>](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a><span data-ttu-id="c9bac-238">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c9bac-238">JavaScript</span></span>](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="c9bac-239">Wenn die `UseChromium` Eigenschaft auf `true` festgelegt ist, können Sie keine Eigenschaften und Methoden für Microsoft Edge \(EdgeHTML\) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9bac-239">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  


## <a name="other-webdriver-installation-options"></a><span data-ttu-id="c9bac-240">Andere WebDriver-Installationsoptionen</span><span class="sxs-lookup"><span data-stu-id="c9bac-240">Other WebDriver installation options</span></span>  

### <a name="docker"></a><span data-ttu-id="c9bac-241">Docker</span><span class="sxs-lookup"><span data-stu-id="c9bac-241">Docker</span></span>  

<span data-ttu-id="c9bac-242">Wenn Sie [Docker][DockerHub] verwenden, führen Sie den folgenden Befehl aus, um ein vorkonfiguriertes Image mit vorinstalliertem Microsoft Edge \(Chromium\) und [Microsoft Edge-Treiber][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-242">If you use [Docker][DockerHub], run the following command to download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pre-installed.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="c9bac-243">Weitere Informationen finden Sie im [msedgedriver-Container auf Docker Hub][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="c9bac-243">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  


## <a name="testing-internet-explorer"></a><span data-ttu-id="c9bac-244">Testen von Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c9bac-244">Testing Internet Explorer</span></span>

<span data-ttu-id="c9bac-245">Um Websites zu testen, die Internet Explorer erfordern, verwenden Sie [Internet Explorer-Treiber][GithubSeleniumHqWikiIEDriver] mit Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c9bac-245">To test sites that require Internet Explorer, use [Internet Explorer Driver][GithubSeleniumHqWikiIEDriver] with Internet Explorer.</span></span>  <span data-ttu-id="c9bac-246">Der Internet Explorer-Treiber wird vom Selenium-Projekt verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c9bac-246">Internet Explorer Driver is maintained by the Selenium project.</span></span>  <span data-ttu-id="c9bac-247">Obwohl Microsoft Edge den IE-Modus unterstützt, können Sie Microsoft Edge Treiber mit Microsoft Edge nicht verwenden, um Websites im IE-Modus zu testen.</span><span class="sxs-lookup"><span data-stu-id="c9bac-247">Even though Microsoft Edge supports IE Mode, you can't use Microsoft Edge Driver with Microsoft Edge to test sites in IE Mode.</span></span>


## <a name="application-guard"></a><span data-ttu-id="c9bac-248">Application Guard</span><span class="sxs-lookup"><span data-stu-id="c9bac-248">Application Guard</span></span>

<span data-ttu-id="c9bac-249">Vertrauenswürdige Websites, die Microsoft Defender Application Guard (Application Guard) verwenden, können mithilfe Microsoft Edge Treibers automatisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c9bac-249">Trusted sites that use Microsoft Defender Application Guard (Application Guard) can be automated using Microsoft Edge Driver.</span></span>

<span data-ttu-id="c9bac-250">Nicht vertrauenswürdige Websites, die Application Guard verwenden, können nicht mit Microsoft Edge Driver automatisiert oder bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c9bac-250">Untrusted sites that use Application Guard cannot be automated or manipulated using Microsoft Edge Driver.</span></span>  <span data-ttu-id="c9bac-251">Application Guard startet nicht vertrauenswürdige Websites in einem Container, und dieser Container macht den Remotedebuggingport, den Microsoft Edge Treiber für die Kommunikation mit der Website benötigt, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c9bac-251">Application Guard launches untrusted sites in a container, and this container doesn't expose the remote debugging port that Microsoft Edge Driver needs to communicate with the site.</span></span>

<span data-ttu-id="c9bac-252">Ihr Unternehmensadministrator definiert, was vertrauenswürdige Websites sind, einschließlich Cloudressourcen und internen Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="c9bac-252">Your enterprise administrator defines what are trusted sites, including cloud resources and internal networks.</span></span>  <span data-ttu-id="c9bac-253">Websites, die nicht in der Liste der vertrauenswürdigen Websites enthalten sind, gelten als nicht vertrauenswürdig.</span><span class="sxs-lookup"><span data-stu-id="c9bac-253">Sites that aren't in the trusted sites list are considered untrusted.</span></span>  <span data-ttu-id="c9bac-254">Microsoft Edge Der Treiber kann sowohl InPrivate-Fenster als auch Websites in der Liste der vertrauenswürdigen Websites automatisieren.</span><span class="sxs-lookup"><span data-stu-id="c9bac-254">Microsoft Edge Driver can automate both InPrivate windows, and sites in the trusted sites list.</span></span>

<span data-ttu-id="c9bac-255">Weitere Informationen zu Application Guard, navigieren Sie zu:</span><span class="sxs-lookup"><span data-stu-id="c9bac-255">For more information about Application Guard, navigate to:</span></span> 

*  [<span data-ttu-id="c9bac-256">Microsoft Edge-Unterstützung für Microsoft Defender Application Guard</span><span class="sxs-lookup"><span data-stu-id="c9bac-256">Microsoft Edge support for Microsoft Defender Application Guard</span></span>][DeployedgeMicrosoftEdgeSecurityWindowsDefenderApplicationGuard]
*  [<span data-ttu-id="c9bac-257">Übersicht über Microsoft Defender Application Guard</span><span class="sxs-lookup"><span data-stu-id="c9bac-257">Microsoft Defender Application Guard overview</span></span>][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]


## <a name="see-also"></a><span data-ttu-id="c9bac-258">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c9bac-258">See also</span></span>

*  <span data-ttu-id="c9bac-259">[Selenium-Dokumentation][SeleniumDocumentation] – Informationen zu WebDriver im Kontext von Selenium und zum Schreiben automatisierter WebDriver-Tests mit Selenium.</span><span class="sxs-lookup"><span data-stu-id="c9bac-259">[Selenium documentation][SeleniumDocumentation] - Information about WebDriver in the context of Selenium, and how to write automated WebDriver tests using Selenium.</span></span>


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c9bac-260">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="c9bac-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="c9bac-261">Das Microsoft Edge Team freuen sich über Ihr Feedback zur Verwendung von WebDriver, WebDriver-Testframeworks (z. B. Selenium) und Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c9bac-261">The Microsoft Edge team is eager to hear your feedback about using WebDriver, WebDriver testing frameworks (such as Selenium), and Microsoft Edge.</span></span>  <span data-ttu-id="c9bac-262">Um dem Team Ihre Fragen und Kommentare zu senden, wählen Sie das Symbol **Feedback senden** in den Microsoft Edge DevTools aus, oder senden Sie einen Tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="c9bac-262">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol „Feedback senden“ in den Microsoft Edge-Entwicklungstools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="c9bac-264">Das Symbol **Feedback senden** in den Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c9bac-264">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  


<!-- links -->  
[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Funktionen und EdgeOptions | Microsoft Docs"  
<!-- external links -->
[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability – Microsoft Edge – Richtlinien | Microsoft-Dokumente"  
[DeployedgeMicrosoftEdgeSecurityWindowsDefenderApplicationGuard]: /deployedge/microsoft-edge-security-windows-defender-application-guard "Microsoft Edge Unterstützung für Microsoft Defender Application Guard | Microsoft-Dokumente"

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Microsoft Defender Application Guard (Windows 10) – Windows | Microsoft-Dokumente"  

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
[SeleniumInstallingLibraries]: https://www.selenium.dev/documentation/en/selenium_installation/installing_selenium_libraries "Installieren von Selenium-Bibliotheken | Selen"

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "Sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Veröffentlichen eines Tweets"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Monitorlose Browser-| Wikipedia"  
