---
description: Überprüfen Sie, ob Webseiten mit deaktivierter BENUTZERoberflächenanimation (reduzierte Bewegung) mithilfe des Css-Medienfeatures "Emulieren" der Dropdownliste "Bevorzugt reduzierte Bewegung" im Renderingtool verwendet werden können.
title: Stellen Sie sicher, dass die Seite mit deaktivierter UI-Animation verwendet werden kann
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ec30925b706b4b1c6dfaaa6ce66a38fab8759ac2
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597414"
---
# <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off"></a><span data-ttu-id="bfcb0-104">Stellen Sie sicher, dass die Seite mit deaktivierter UI-Animation verwendet werden kann</span><span class="sxs-lookup"><span data-stu-id="bfcb0-104">Verify that the page is usable with UI animation turned off</span></span>

<span data-ttu-id="bfcb0-105">Eine Webseite sollte einem Benutzer, der Animationen im Betriebssystem deaktiviert hat, keine Animationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-105">A webpage should not show animations to a user who turned off animations in the operating system.</span></span>  <span data-ttu-id="bfcb0-106">Animationen können zur Benutzerfreundlichkeit eines Produkts beitragen, können aber auch Ablenkungen, Verwirrung oder Verwirrung verursachen.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-106">Animations can help the usability of a product, but they can also cause distraction, confusion, or nausea.</span></span>

<span data-ttu-id="bfcb0-107">Um zu überprüfen, ob eine Webseite mit deaktivierter BENUTZERoberflächenanimation (reduzierte Bewegung) verwendet werden kann, verwenden Sie im **Renderingtool** die Dropdownliste zum **Emulieren von CSS-Medienfeatures mit vorzuziehenden Bewegungen.**</span><span class="sxs-lookup"><span data-stu-id="bfcb0-107">To check that a webpage is usable with UI animation turned off (reduced motion), in the **Rendering** tool, use the **Emulate CSS media feature prefers-reduced-motion** dropdown list.</span></span>

<span data-ttu-id="bfcb0-108">Wenn Sie auf der Demowebseite für Barrierefreiheitstests Animationen im Betriebssystem deaktivieren oder diese Einstellungen mit DevTools emulieren, verwendet die Webseite keinen reibungslosen Bildlauf, wenn Sie die Links des Navigationsmenüs auf der Seitenleiste auswählen.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-108">In the accessibility-testing demo webpage, when you turn off animations in the operating system, or emulate that settings by using DevTools, the webpage doesn't use smooth scrolling when you select the links of the sidebar navigation menu.</span></span>  <span data-ttu-id="bfcb0-109">Dies wird erreicht, indem die Einstellung für den gleichmäßigen Bildlauf in CSS in einer Medienabfrage umgebrochen und dann das **Renderingtool** zum Emulieren der Betriebssystemeinstellung für reduzierte Animationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-109">This is achieved by wrapping the smooth-scrolling setting in CSS in a media query, and then using the **Rendering** tool to emulate the operating system setting for reduced animation.</span></span>

<span data-ttu-id="bfcb0-110">So überprüfen Sie, ob die Seite mit deaktivierten Animationen verwendet werden kann:</span><span class="sxs-lookup"><span data-stu-id="bfcb0-110">To check whether the page is usable with animations turned off:</span></span>

1.  <span data-ttu-id="bfcb0-111">Öffnen Sie die [Demo-Webseite für Barrierefreiheitstests][DevToolsA11yErrorsDemopage] auf einer neuen Registerkarte des Browsers, und wählen Sie **F12** aus, um DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-111">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="bfcb0-112">Wählen Sie oben in DevTools das **Tool "Quellen"** aus, und wählen Sie dann im **Navigationsbereich** auf der linken Seite die Option `styles.css` aus.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-112">At the top of DevTools, select the **Sources** tool, and then in the **Navigation** pane on the left, select `styles.css`.</span></span>  <span data-ttu-id="bfcb0-113">Die CSS-Datei wird im **Editorbereich** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-113">The CSS file appears in the **Editor** pane.</span></span>

1.  <span data-ttu-id="bfcb0-114">Wählen Sie **STRG+F** unter Windows/Linux oder **Befehl+F** unter macOS aus, und geben Sie dann `@media` ein.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-114">Select **Ctrl+F** on Windows/Linux or **Command+F** on macOS, and then enter `@media`.</span></span>  <span data-ttu-id="bfcb0-115">Die folgende CSS-Medienabfrage wird angezeigt, die bestätigt, dass sie auf der Webseite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-115">The following CSS media query is displayed, which confirms that it is used on the webpage.</span></span>

    ```css
    @media (prefers-reduced-motion: no-preference) {
      html {
        scroll-behavior: smooth;
      }
    }
    ```

    <span data-ttu-id="bfcb0-116">Emulieren Sie als Nächstes die Einstellung des Betriebssystems, um die Animation wie folgt zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-116">Next, emulate the operating system setting to reduce animation, as follows.</span></span>

1.  <span data-ttu-id="bfcb0-117">Wählen Sie **Esc** aus, um die Schublade am unteren Rand von DevTools zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-117">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="bfcb0-118">Wählen Sie oben in der Schublade die Schaltfläche **Weitere Tools** ( **+** ) aus, um die Liste der Tools anzuzeigen, und wählen Sie dann **Rendering**aus.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-118">Select the **More tools** (**+**) button at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="bfcb0-119">Wählen Sie in der Dropdownliste **"Emulate CSS media feature prefers-reduced-motion"** die Option **"prefers-reduced-motion: reduced"** aus.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-119">In the **Emulate CSS media feature prefers-reduced-motion** dropdown list, select **prefers-reduced-motion: reduced**.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulieren von reduzierter Bewegung und css, die sicherstellen, dass ein gleichmäßiger Bildlauf nur erfolgt, wenn der Benutzer dies möchte" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
        <span data-ttu-id="bfcb0-121">Simulieren von reduzierter Bewegung und css, die sicherstellen, dass ein gleichmäßiger Bildlauf nur erfolgt, wenn der Benutzer dies möchte</span><span class="sxs-lookup"><span data-stu-id="bfcb0-121">Simulating reduced motion and the CSS that makes sure that smooth scrolling only happens when the user wants it</span></span>
    :::image-end:::

1.  <span data-ttu-id="bfcb0-122">Wählen Sie auf der Webseite die blauen Menüelemente aus, **z. B. "Käufe"** oder **"Doppelklicken".**</span><span class="sxs-lookup"><span data-stu-id="bfcb0-122">In the webpage, select the blue menu items, such as **Horses** or **Alpacas**.</span></span>  <span data-ttu-id="bfcb0-123">Jetzt führt die Webseite sofort einen Bildlauf zum ausgewählten Abschnitt durch, anstatt die Animation für den gleichmäßigen Bildlauf zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-123">Now the webpage instantly scrolls to the selected section, rather than using the smooth-scrolling animation.</span></span>

1.  <span data-ttu-id="bfcb0-124">Wählen Sie im **Renderingtool** unter dem **Emulieren der CSS-Medienfunktion "Prefers-reduced-motion"** die Option **"Keine Emulation"** aus, um diese Einstellung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-124">In the **Rendering** tool, below **Emulate CSS media feature prefers-reduced-motion**, select **No emulation** to remove this setting.</span></span>
   
<span data-ttu-id="bfcb0-125">Beachten Sie, dass die Demowebseite auch mit den oben genannten Medienabfrage- und Emulationseinstellungen weiterhin die folgenden Animationen ausführt.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-125">Notice that the demo webpage still runs the following animations, even with the above media query and emulation settings.</span></span> <span data-ttu-id="bfcb0-126">Stellen Sie beim Erstellen Ihres Webprodukts sicher, dass Sie alle ähnlichen Animationen beheben.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-126">When building your web product, ensure you fix all similar animations.</span></span>  
*  <span data-ttu-id="bfcb0-127">Animation der blauen Menüelemente, wenn Sie mit dem Mauszeiger darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-127">Animation of the blue menu items when you hover over them.</span></span>
*  <span data-ttu-id="bfcb0-128">Animation der Kreise auf den **Links "Mehr",** wenn Sie mit dem Mauszeiger darauf zeigen.</span><span class="sxs-lookup"><span data-stu-id="bfcb0-128">Animation of the circles on the **More** links when you hover over them.</span></span>



## <a name="see-also"></a><span data-ttu-id="bfcb0-129">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="bfcb0-129">See also</span></span>

*  [<span data-ttu-id="bfcb0-130">Simulation reduzierter Bewegungen</span><span class="sxs-lookup"><span data-stu-id="bfcb0-130">Reduced motion simulation</span></span>](reduced-motion-simulation.md)
*  [<span data-ttu-id="bfcb0-131">Übersicht über Barrierefreiheitstests mit DevTools</span><span class="sxs-lookup"><span data-stu-id="bfcb0-131">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="bfcb0-132">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="bfcb0-132">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Demowebseite für Barrierefreiheitstests | GitHub"
