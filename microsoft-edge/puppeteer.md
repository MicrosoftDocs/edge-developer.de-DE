---
description: Use Puppeteer to automate and test in Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, web development, developer, tools, automation, test
ms.openlocfilehash: bef3f0d7472f7bc595998829546fb540041f20fc
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986157"
---
# Puppeteer  

[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library which provides a high-level API to control Microsoft Edge \(Chromium\) over the [DevTools Protocol][GithubChromedevtoolsProtocol].  Puppeteer runs [headless][WikiHeadlessBrowser] by default, which means that you do not see a UI, and instead must use the command-line.  You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge or Chromium as well.  

By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].  If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].  `puppeteer-core` is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).  To download Microsoft Edge \(Chromium\), see [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].

## Installing puppeteer-core  

You may add `puppeteer-core` to your website or app with one of the following commands.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## Launch Microsoft Edge with puppeteer-core  

> [!NOTE]
> `puppeteer-core` relies on Node v8.9.0 or later.  The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.  Run `node -v` from the command-line to ensure you have a compatible version of Node.js.  

`puppeteer-core` should be familiar to users of other browser-testing-frameworks like [WebDriver][WebDriverEdgehtmlMain].  You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.  In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.  

Copy the code sample below and save it as `example.js`.  

```javascript
const puppeteer = require('puppeteer-core');

(async () => {
  const browser = await puppeteer.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoftedgeinsider.com');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).  For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.  To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

Finally, set `executablePath: EDGE_PATH` in `example.js`.  Save your changes.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.  You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.  

Now run `example.js` from the command-line.  

```shell
node example.js
```  

`puppeteer-core` launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com` and saves an 800px x 600px screenshot of the page.  You are able to customize the page size with [page.setViewport()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="The example.png file produced by example.js":::
   Figure 1:  The `example.png` file produced by `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.  For more information about Puppeteer and how it works, see [Puppeteer][|::ref2::|Main].  

## Getting in touch with the Microsoft Edge DevTools team  

The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.  Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.  


:::image type="complex" source="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="The example.png file produced by example.js"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "puppeteer vs. puppeteer-core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page.setViewport(viewport) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools - Post a Tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Headless browser | Wikipedia"  
