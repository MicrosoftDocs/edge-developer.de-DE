---
description: Use virtual devices in Microsoft Edge to build mobile-first websites.
title: Emulate Mobile Devices in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, emulation, device, simulation, mobile
ms.openlocfilehash: c70b81eabb145461eac7d1b9a8f438d6a18fbc89
ms.sourcegitcommit: cc96ada9679b23feb841e46f19d8077251c4a4df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "10997089"
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

# <span data-ttu-id="e7f00-104">Emulate mobile devices in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e7f00-104">Emulate mobile devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="e7f00-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span><span class="sxs-lookup"><span data-stu-id="e7f00-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span></span>  <span data-ttu-id="e7f00-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span><span class="sxs-lookup"><span data-stu-id="e7f00-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span></span>  <span data-ttu-id="e7f00-107">The collection includes the following features.</span><span class="sxs-lookup"><span data-stu-id="e7f00-107">The collection includes the following features.</span></span>  

*   [<span data-ttu-id="e7f00-108">Simulate a mobile viewport</span><span class="sxs-lookup"><span data-stu-id="e7f00-108">Simulate a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="e7f00-109">Throttle the network</span><span class="sxs-lookup"><span data-stu-id="e7f00-109">Throttle the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="e7f00-110">Throttle the CPU</span><span class="sxs-lookup"><span data-stu-id="e7f00-110">Throttle the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="e7f00-111">Simulate geolocation</span><span class="sxs-lookup"><span data-stu-id="e7f00-111">Simulate geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="e7f00-112">Set orientation</span><span class="sxs-lookup"><span data-stu-id="e7f00-112">Set orientation</span></span>](#set-orientation)  
*   [<span data-ttu-id="e7f00-113">Set the user agent string</span><span class="sxs-lookup"><span data-stu-id="e7f00-113">Set the user agent string</span></span>](#set-user-agent-string)  

## <span data-ttu-id="e7f00-114">Limitations</span><span class="sxs-lookup"><span data-stu-id="e7f00-114">Limitations</span></span>  

<span data-ttu-id="e7f00-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span><span class="sxs-lookup"><span data-stu-id="e7f00-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span></span>  <span data-ttu-id="e7f00-116">**Device emulation** does not actually run your code on a mobile device.</span><span class="sxs-lookup"><span data-stu-id="e7f00-116">**Device emulation** does not actually run your code on a mobile device.</span></span>  <span data-ttu-id="e7f00-117">Instead you simulate the mobile user experience from your laptop or desktop.</span><span class="sxs-lookup"><span data-stu-id="e7f00-117">Instead you simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="e7f00-118">Some aspects of mobile devices are never emulated in DevTools.</span><span class="sxs-lookup"><span data-stu-id="e7f00-118">Some aspects of mobile devices are never emulated in DevTools.</span></span>  <span data-ttu-id="e7f00-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span><span class="sxs-lookup"><span data-stu-id="e7f00-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="e7f00-120">When in doubt, your best bet is to actually run your page on a mobile device.</span><span class="sxs-lookup"><span data-stu-id="e7f00-120">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="e7f00-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span><span class="sxs-lookup"><span data-stu-id="e7f00-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span></span>  <span data-ttu-id="e7f00-122">You may view, change, debug, profile, or all four while you interact with the code.</span><span class="sxs-lookup"><span data-stu-id="e7f00-122">You may view, change, debug, profile, or all four while you interact with the code.</span></span>  <span data-ttu-id="e7f00-123">Your machine may be a notebook or desktop computer.</span><span class="sxs-lookup"><span data-stu-id="e7f00-123">Your machine may be a notebook or desktop computer.</span></span>  

## <span data-ttu-id="e7f00-124">Simulate a mobile viewport</span><span class="sxs-lookup"><span data-stu-id="e7f00-124">Simulate a mobile viewport</span></span>  

<span data-ttu-id="e7f00-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span><span class="sxs-lookup"><span data-stu-id="e7f00-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    <span data-ttu-id="e7f00-127">The Device Toolbar</span><span class="sxs-lookup"><span data-stu-id="e7f00-127">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="e7f00-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span><span class="sxs-lookup"><span data-stu-id="e7f00-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="e7f00-129">Responsive Viewport Mode</span><span class="sxs-lookup"><span data-stu-id="e7f00-129">Responsive Viewport Mode</span></span>  

<span data-ttu-id="e7f00-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span><span class="sxs-lookup"><span data-stu-id="e7f00-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span></span>  <span data-ttu-id="e7f00-131">You may also enter specific values in the width and height boxes.</span><span class="sxs-lookup"><span data-stu-id="e7f00-131">You may also enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="e7f00-132">In the following figure, the width is set to `626` and the height is set to `516`.</span><span class="sxs-lookup"><span data-stu-id="e7f00-132">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    <span data-ttu-id="e7f00-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span><span class="sxs-lookup"><span data-stu-id="e7f00-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <span data-ttu-id="e7f00-135">Show media queries</span><span class="sxs-lookup"><span data-stu-id="e7f00-135">Show media queries</span></span>  

<span data-ttu-id="e7f00-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span><span class="sxs-lookup"><span data-stu-id="e7f00-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span></span>  <span data-ttu-id="e7f00-137">Choose **More options** > **Show media queries**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-137">Choose **More options** > **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="e7f00-139">Show media queries</span><span class="sxs-lookup"><span data-stu-id="e7f00-139">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="e7f00-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span><span class="sxs-lookup"><span data-stu-id="e7f00-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="e7f00-142">Choose a breakpoint to change the width of the viewport</span><span class="sxs-lookup"><span data-stu-id="e7f00-142">Choose a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <span data-ttu-id="e7f00-143">Set the device type</span><span class="sxs-lookup"><span data-stu-id="e7f00-143">Set the device type</span></span>  

<span data-ttu-id="e7f00-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span><span class="sxs-lookup"><span data-stu-id="e7f00-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="e7f00-146">The **Device Type** list</span><span class="sxs-lookup"><span data-stu-id="e7f00-146">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="e7f00-147">The following table describes the differences between the available device type options.</span><span class="sxs-lookup"><span data-stu-id="e7f00-147">The following table describes the differences between the available device type options.</span></span>  <span data-ttu-id="e7f00-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span><span class="sxs-lookup"><span data-stu-id="e7f00-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="e7f00-149">The Cursor icon column refers to what type of cursor you see when you hover on the page.</span><span class="sxs-lookup"><span data-stu-id="e7f00-149">The Cursor icon column refers to what type of cursor you see when you hover on the page.</span></span>  <span data-ttu-id="e7f00-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span><span class="sxs-lookup"><span data-stu-id="e7f00-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="e7f00-151">Option</span><span class="sxs-lookup"><span data-stu-id="e7f00-151">Option</span></span> | <span data-ttu-id="e7f00-152">Rendering method</span><span class="sxs-lookup"><span data-stu-id="e7f00-152">Rendering method</span></span> | <span data-ttu-id="e7f00-153">Cursor icon</span><span class="sxs-lookup"><span data-stu-id="e7f00-153">Cursor icon</span></span> | <span data-ttu-id="e7f00-154">Events triggered</span><span class="sxs-lookup"><span data-stu-id="e7f00-154">Events triggered</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="e7f00-155">Mobile</span><span class="sxs-lookup"><span data-stu-id="e7f00-155">Mobile</span></span> | <span data-ttu-id="e7f00-156">Mobile</span><span class="sxs-lookup"><span data-stu-id="e7f00-156">Mobile</span></span> | <span data-ttu-id="e7f00-157">Circle</span><span class="sxs-lookup"><span data-stu-id="e7f00-157">Circle</span></span> | <span data-ttu-id="e7f00-158">touch</span><span class="sxs-lookup"><span data-stu-id="e7f00-158">touch</span></span> |  
| <span data-ttu-id="e7f00-159">Mobile \(no touch\)</span><span class="sxs-lookup"><span data-stu-id="e7f00-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="e7f00-160">Mobile</span><span class="sxs-lookup"><span data-stu-id="e7f00-160">Mobile</span></span> | <span data-ttu-id="e7f00-161">Normal</span><span class="sxs-lookup"><span data-stu-id="e7f00-161">Normal</span></span> | <span data-ttu-id="e7f00-162">click</span><span class="sxs-lookup"><span data-stu-id="e7f00-162">click</span></span> |  
| <span data-ttu-id="e7f00-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="e7f00-163">Desktop</span></span> | <span data-ttu-id="e7f00-164">Desktop</span><span class="sxs-lookup"><span data-stu-id="e7f00-164">Desktop</span></span> | <span data-ttu-id="e7f00-165">Normal</span><span class="sxs-lookup"><span data-stu-id="e7f00-165">Normal</span></span> | <span data-ttu-id="e7f00-166">click</span><span class="sxs-lookup"><span data-stu-id="e7f00-166">click</span></span> |  
| <span data-ttu-id="e7f00-167">Desktop \(touch\)</span><span class="sxs-lookup"><span data-stu-id="e7f00-167">Desktop \(touch\)</span></span> | <span data-ttu-id="e7f00-168">Desktop</span><span class="sxs-lookup"><span data-stu-id="e7f00-168">Desktop</span></span> | <span data-ttu-id="e7f00-169">Circle</span><span class="sxs-lookup"><span data-stu-id="e7f00-169">Circle</span></span> | <span data-ttu-id="e7f00-170">touch</span><span class="sxs-lookup"><span data-stu-id="e7f00-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="e7f00-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span></span>  

### <span data-ttu-id="e7f00-172">Mobile Device Viewport Mode</span><span class="sxs-lookup"><span data-stu-id="e7f00-172">Mobile Device Viewport Mode</span></span>  

<span data-ttu-id="e7f00-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span><span class="sxs-lookup"><span data-stu-id="e7f00-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="e7f00-175">The **Device** list</span><span class="sxs-lookup"><span data-stu-id="e7f00-175">The **Device** list</span></span>  
:::image-end:::  

#### <span data-ttu-id="e7f00-176">Rotate the viewport to landscape orientation</span><span class="sxs-lookup"><span data-stu-id="e7f00-176">Rotate the viewport to landscape orientation</span></span>  

<span data-ttu-id="e7f00-177">Test your webpage in landscape orientation.</span><span class="sxs-lookup"><span data-stu-id="e7f00-177">Test your webpage in landscape orientation.</span></span>  

*   <span data-ttu-id="e7f00-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate][ImageRotateIcon]\).</span><span class="sxs-lookup"><span data-stu-id="e7f00-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate][ImageRotateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       <span data-ttu-id="e7f00-180">Page displayed in landscape orientation</span><span class="sxs-lookup"><span data-stu-id="e7f00-180">Page displayed in landscape orientation</span></span>  
    :::image-end:::  
    
> [!NOTE]
> <span data-ttu-id="e7f00-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span><span class="sxs-lookup"><span data-stu-id="e7f00-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="e7f00-183">The **Device Toolbar**</span><span class="sxs-lookup"><span data-stu-id="e7f00-183">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="e7f00-184">For more information, go to [Set orientation](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="e7f00-184">For more information, go to [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="e7f00-185">Show device frame</span><span class="sxs-lookup"><span data-stu-id="e7f00-185">Show device frame</span></span>  

<span data-ttu-id="e7f00-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span><span class="sxs-lookup"><span data-stu-id="e7f00-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span></span>  

1.  <span data-ttu-id="e7f00-187">Open **More options**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-187">Open **More options**.</span></span>  
1.  <span data-ttu-id="e7f00-188">Choose **Show device frame**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-188">Choose **Show device frame**.</span></span>  

> [!NOTE]
> <span data-ttu-id="e7f00-189">If you do not see a device frame for a particular device, it means that DevTools does not have art for that option.</span><span class="sxs-lookup"><span data-stu-id="e7f00-189">If you do not see a device frame for a particular device, it means that DevTools does not have art for that option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="e7f00-191">Show device frame</span><span class="sxs-lookup"><span data-stu-id="e7f00-191">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="e7f00-193">The device frame for the iPhone 6</span><span class="sxs-lookup"><span data-stu-id="e7f00-193">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="e7f00-194">Add a custom mobile device</span><span class="sxs-lookup"><span data-stu-id="e7f00-194">Add a custom mobile device</span></span>  

<span data-ttu-id="e7f00-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span><span class="sxs-lookup"><span data-stu-id="e7f00-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span></span>  <span data-ttu-id="e7f00-196">To add a custom device, complete the following steps.</span><span class="sxs-lookup"><span data-stu-id="e7f00-196">To add a custom device, complete the following steps.</span></span>  

1.  <span data-ttu-id="e7f00-197">Choose the **Device** list > **Edit**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-197">Choose the **Device** list > **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="e7f00-199">Select **Edit**</span><span class="sxs-lookup"><span data-stu-id="e7f00-199">Select **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e7f00-200">Choose **Add custom device**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-200">Choose **Add custom device**.</span></span>  
1.  <span data-ttu-id="e7f00-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span><span class="sxs-lookup"><span data-stu-id="e7f00-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span></span>  <span data-ttu-id="e7f00-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span><span class="sxs-lookup"><span data-stu-id="e7f00-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="e7f00-203">The device type field defaults to **Mobile**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-203">The device type field defaults to **Mobile**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="e7f00-205">Create a custom device</span><span class="sxs-lookup"><span data-stu-id="e7f00-205">Create a custom device</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e7f00-206">Show rulers</span><span class="sxs-lookup"><span data-stu-id="e7f00-206">Show rulers</span></span>  

<span data-ttu-id="e7f00-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span><span class="sxs-lookup"><span data-stu-id="e7f00-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span></span>  <span data-ttu-id="e7f00-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span><span class="sxs-lookup"><span data-stu-id="e7f00-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         <span data-ttu-id="e7f00-210">Menu item to display rulers</span><span class="sxs-lookup"><span data-stu-id="e7f00-210">Menu item to display rulers</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="e7f00-212">Rulers above and to the left of the viewport</span><span class="sxs-lookup"><span data-stu-id="e7f00-212">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="e7f00-213">Zoom the viewport</span><span class="sxs-lookup"><span data-stu-id="e7f00-213">Zoom the viewport</span></span>  

<span data-ttu-id="e7f00-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span><span class="sxs-lookup"><span data-stu-id="e7f00-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="e7f00-216">Zoom</span><span class="sxs-lookup"><span data-stu-id="e7f00-216">Zoom</span></span>**  
:::image-end:::  

## <span data-ttu-id="e7f00-217">Throttle the network and CPU</span><span class="sxs-lookup"><span data-stu-id="e7f00-217">Throttle the network and CPU</span></span>  

<span data-ttu-id="e7f00-218">Mobile devices often have network and CPU constraints.</span><span class="sxs-lookup"><span data-stu-id="e7f00-218">Mobile devices often have network and CPU constraints.</span></span>  <span data-ttu-id="e7f00-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span><span class="sxs-lookup"><span data-stu-id="e7f00-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span></span>  

<span data-ttu-id="e7f00-220">Throttle the network and CPU.</span><span class="sxs-lookup"><span data-stu-id="e7f00-220">Throttle the network and CPU.</span></span>  

1.  <span data-ttu-id="e7f00-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span></span>  
    *   <span data-ttu-id="e7f00-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span><span class="sxs-lookup"><span data-stu-id="e7f00-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span></span>  <span data-ttu-id="e7f00-223">It is four times slower than normal.</span><span class="sxs-lookup"><span data-stu-id="e7f00-223">It is four times slower than normal.</span></span>  
    *   <span data-ttu-id="e7f00-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span><span class="sxs-lookup"><span data-stu-id="e7f00-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span></span>  <span data-ttu-id="e7f00-225">It is six times slower than normal.</span><span class="sxs-lookup"><span data-stu-id="e7f00-225">It is six times slower than normal.</span></span>  
    
<span data-ttu-id="e7f00-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span><span class="sxs-lookup"><span data-stu-id="e7f00-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="e7f00-228">The **Throttle** list in the Device Toolbar</span><span class="sxs-lookup"><span data-stu-id="e7f00-228">The **Throttle** list in the Device Toolbar</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e7f00-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span><span class="sxs-lookup"><span data-stu-id="e7f00-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span></span>  <span data-ttu-id="e7f00-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="e7f00-232">The **Device Toolbar**</span><span class="sxs-lookup"><span data-stu-id="e7f00-232">The **Device Toolbar**</span></span>  
:::image-end:::  

### <span data-ttu-id="e7f00-233">Throttle the CPU only</span><span class="sxs-lookup"><span data-stu-id="e7f00-233">Throttle the CPU only</span></span>  

<span data-ttu-id="e7f00-234">To throttle the CPU only and not the network, complete the following steps.</span><span class="sxs-lookup"><span data-stu-id="e7f00-234">To throttle the CPU only and not the network, complete the following steps.</span></span>

1.  <span data-ttu-id="e7f00-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span><span class="sxs-lookup"><span data-stu-id="e7f00-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>
1.  <span data-ttu-id="e7f00-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span></span>
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       <span data-ttu-id="e7f00-238">The **CPU** list in the **Performance** panel</span><span class="sxs-lookup"><span data-stu-id="e7f00-238">The **CPU** list in the **Performance** panel</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e7f00-239">Throttle the network only</span><span class="sxs-lookup"><span data-stu-id="e7f00-239">Throttle the network only</span></span>  

<span data-ttu-id="e7f00-240">To throttle the network only, complete the following steps.</span><span class="sxs-lookup"><span data-stu-id="e7f00-240">To throttle the network only, complete the following steps.</span></span>

1.  <span data-ttu-id="e7f00-241">Choose the **Network** panel.</span><span class="sxs-lookup"><span data-stu-id="e7f00-241">Choose the **Network** panel.</span></span>
1.  <span data-ttu-id="e7f00-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span></span>
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-network-throttle.msft.png":::
       <span data-ttu-id="e7f00-244">The **Throttle** list in the Network panel</span><span class="sxs-lookup"><span data-stu-id="e7f00-244">The **Throttle** list in the Network panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e7f00-245">Or select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-245">Or select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       <span data-ttu-id="e7f00-247">The **Command Menu**</span><span class="sxs-lookup"><span data-stu-id="e7f00-247">The **Command Menu**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e7f00-248">You may also set network throttling from the **Performance** panel.</span><span class="sxs-lookup"><span data-stu-id="e7f00-248">You may also set network throttling from the **Performance** panel.</span></span>  

1.  <span data-ttu-id="e7f00-249">Choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-249">Choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       <span data-ttu-id="e7f00-251">Set network throttling from the **Performance** panel</span><span class="sxs-lookup"><span data-stu-id="e7f00-251">Set network throttling from the **Performance** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e7f00-252">Override geolocation</span><span class="sxs-lookup"><span data-stu-id="e7f00-252">Override geolocation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e7f00-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span><span class="sxs-lookup"><span data-stu-id="e7f00-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span></span>  

      1.  <span data-ttu-id="e7f00-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="e7f00-256">**Sensors** for geolocation</span><span class="sxs-lookup"><span data-stu-id="e7f00-256">**Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="e7f00-257">Open the Command Menu.</span><span class="sxs-lookup"><span data-stu-id="e7f00-257">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="e7f00-258">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="e7f00-258">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="e7f00-259">Type `Sensors`, and choose **Show Sensors**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-259">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="e7f00-261">**Show Sensors** for geolocation</span><span class="sxs-lookup"><span data-stu-id="e7f00-261">**Show Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e7f00-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span><span class="sxs-lookup"><span data-stu-id="e7f00-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span></span>  <span data-ttu-id="e7f00-263">To enter a custom location, choose **Other…**</span><span class="sxs-lookup"><span data-stu-id="e7f00-263">To enter a custom location, choose **Other…**</span></span> <span data-ttu-id="e7f00-264">and enter the coordinates of your custom location.</span><span class="sxs-lookup"><span data-stu-id="e7f00-264">and enter the coordinates of your custom location.</span></span>  <span data-ttu-id="e7f00-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    <span data-ttu-id="e7f00-267">**Sensors** panel with a preset location selected.</span><span class="sxs-lookup"><span data-stu-id="e7f00-267">**Sensors** panel with a preset location selected.</span></span>  
:::image-end:::

## <span data-ttu-id="e7f00-268">Set orientation</span><span class="sxs-lookup"><span data-stu-id="e7f00-268">Set orientation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e7f00-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span><span class="sxs-lookup"><span data-stu-id="e7f00-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span></span>  

      1.  <span data-ttu-id="e7f00-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="e7f00-272">**Sensors** for orientation</span><span class="sxs-lookup"><span data-stu-id="e7f00-272">**Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="e7f00-273">Open the Command Menu.</span><span class="sxs-lookup"><span data-stu-id="e7f00-273">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="e7f00-274">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="e7f00-274">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="e7f00-275">Type `Sensors`, and choose **Show Sensors**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-275">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="e7f00-277">**Show Sensors** for orientation</span><span class="sxs-lookup"><span data-stu-id="e7f00-277">**Show Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e7f00-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span><span class="sxs-lookup"><span data-stu-id="e7f00-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span></span>  <span data-ttu-id="e7f00-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span><span class="sxs-lookup"><span data-stu-id="e7f00-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    <span data-ttu-id="e7f00-281">**Orientation** options on the **Sensors** panel</span><span class="sxs-lookup"><span data-stu-id="e7f00-281">**Orientation** options on the **Sensors** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="e7f00-282">Set user agent string</span><span class="sxs-lookup"><span data-stu-id="e7f00-282">Set user agent string</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e7f00-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span><span class="sxs-lookup"><span data-stu-id="e7f00-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span></span>  
      
      1.  <span data-ttu-id="e7f00-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         <span data-ttu-id="e7f00-286">**Network conditions** entry in the **More tools** menu</span><span class="sxs-lookup"><span data-stu-id="e7f00-286">**Network conditions** entry in the **More tools** menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="e7f00-287">Open the Command Menu.</span><span class="sxs-lookup"><span data-stu-id="e7f00-287">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="e7f00-288">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="e7f00-288">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="e7f00-289">Type `Network conditions`, and choose **Show Network conditions**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-289">Type `Network conditions`, and choose **Show Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **<span data-ttu-id="e7f00-291">Show Network conditions</span><span class="sxs-lookup"><span data-stu-id="e7f00-291">Show Network conditions</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e7f00-292">Next to **User agent**, clear the **Select automatically** checkbox.</span><span class="sxs-lookup"><span data-stu-id="e7f00-292">Next to **User agent**, clear the **Select automatically** checkbox.</span></span>  <span data-ttu-id="e7f00-293">Then, select **Custom...** to select from a list of predefined user agent strings.</span><span class="sxs-lookup"><span data-stu-id="e7f00-293">Then, select **Custom...** to select from a list of predefined user agent strings.</span></span>  <span data-ttu-id="e7f00-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span><span class="sxs-lookup"><span data-stu-id="e7f00-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="The Device Toolbar" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    <span data-ttu-id="e7f00-296">Set the user agent string to Microsoft Edge on macOS</span><span class="sxs-lookup"><span data-stu-id="e7f00-296">Set the user agent string to Microsoft Edge on macOS</span></span>  
:::image-end:::  

## <span data-ttu-id="e7f00-297">Getting in touch with the Microsoft Edge DevTools team</span><span class="sxs-lookup"><span data-stu-id="e7f00-297">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: ../remote-debugging/index.md "Get started with remote debugging Android devices | Microsoft Docs"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window.devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "User Agent | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent.alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent.beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent.gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Order of Approximation - First-order - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="e7f00-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e7f00-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e7f00-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="e7f00-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="e7f00-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e7f00-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
