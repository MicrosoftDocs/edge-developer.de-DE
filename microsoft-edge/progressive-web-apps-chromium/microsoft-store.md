---
description: Machen Sie Ihre PWA leichter auffindbar, indem Sie sie im Microsoft Store
title: Veröffentlichen Ihrer Progressive Web App im Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Progressive Web Apps, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 40a6b94412a0788c87f7231025809098c98f18e9
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643249"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a>Veröffentlichen Ihrer Progressive Web App im Microsoft Store  

Die Veröffentlichung Ihrer Progressive Web App \(PWA\) im [Microsoft Store][WindowsUwpPublishIndex] bietet die folgenden Vorteile.  

:::row:::
   :::column span="1":::
      **Erkennbarkeit**  
   :::column-end:::
   :::column span="2":::
      Benutzer suchen im App Store natürlich nach Apps.  Wenn Sie im Microsoft Store veröffentlichen, können Millionen Windows Benutzer Ihre PWA zusammen mit anderen Windows-Apps entdecken.  Die Store zeigt Apps in Kategorien, zusammengestellten Sammlungen und mehr.  Die App-Suchportale bieten potenziellen Benutzern Ihrer App ein einfaches Browsen und Shoppingerlebnis.  Sie können Ihren Store Eintrag sogar mit Screenshots, einem Favoritenbild und Videotrailern [verbessern.][WindowsUwpPublishAppScreenshotsImages]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Vertrauenswürdigkeit**  
   :::column-end:::
   :::column span="2":::
      Windows Kunden wissen, dass sie ihren Microsoft Store Einkäufen und Downloads vertrauen können, da sie die strengen [Qualitäts- und Sicherheitsstandards][LegalWindowsAgreementsStorePolicies]von Microsoft einhalten.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Einfache Installation**  
   :::column-end:::
   :::column span="2":::
      Das Microsoft Store bietet eine konsistente und benutzerfreundliche Installationsumgebung für [alle Windows 10 Apps.][MicrosoftStoreAppsWindows]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **App-Analysen**  
   :::column-end:::
   :::column span="2":::
      Das [Windows Partner Center-Dashboard][WindowsUwpPublishIndex] bietet Ihnen [detaillierte Analysen][WindowsUwpPublishAnalytics] zur App-Integrität, -Nutzung und vieles mehr.  
   :::column-end:::
:::row-end:::  

Um Ihre PWA im Microsoft Store zu veröffentlichen, sind keine Codeänderungen erforderlich.  Stattdessen erstellen Sie eine App-Reservierung, verpacken Ihre PWA und übermitteln Ihr Paket an die Store.  In den folgenden Abschnitten werden die Schritte erläutert.   

## <a name="create-an-app-reservation"></a>Erstellen einer App-Reservierung  

[Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] ist der Hub, über den Sie Ihre App an die Microsoft Store übermitteln können.  

Führen Sie die folgenden Aktionen aus, um eine App-Reservierung zu erstellen.  

1.  Führen Sie die folgenden Aktionen aus, um ihre registrierten Programme anzuzeigen.  
    1.  Melden Sie sich mit Ihrem Microsoft-Konto bei Windows Partner Center an, und navigieren Sie zum [Partner Center-Dashboard.][MicrosoftPartnerDashboardHome]  
    1.  Navigieren Sie zu **Windows & Xbox**  
        *   Wenn **Windows & Xbox** angezeigt wird, ist Ihre App bereits registriert.  
        *   Wenn **Windows & Xbox** nicht angezeigt wird, wählen Sie Programm **hinzufügen**aus.  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Hinzufügen eines Programms im Windows Partner Center-Dashboard" lightbox="./media/windows-partner-center-add-program.msft.png":::
       Hinzufügen eines Programms im Windows Partner Center-Dashboard
    :::image-end:::  
    
1.  Führen Sie die folgenden Aktionen aus, um sich für das Entwicklerprogramm zu registrieren.  
    1.  Navigieren Sie zu **Windows & Xbox**.  
    1.  Wählen Sie **"Erste Schritte" aus.**  
    1.  Befolgen Sie die Anweisungen.  
1.  Jetzt ist Ihr Konto für das App-Entwicklerprogramm registriert. Führen Sie die folgenden Aktionen aus, um eine App-Reservierung zu erstellen.  
    1.  Navigieren Sie zu **Windows & Xbox**.  
    1.  Wählen Sie **"Übersicht**  >  **Erstellen einer neuen App"** aus.  
    1.  Geben Sie in der Eingabeaufforderung den Namen Ihrer App ein.  
    1.  Wählen Sie `Reserve product name` .  
        
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Erstellen einer App-Reservierung im Windows Partner Center" lightbox="./media/windows-partner-center-create-app.msft.png":::
       Erstellen einer App-Reservierung im Windows Partner Center  
    :::image-end:::  
    
1.  Wählen Sie **"Produktverwaltung**Produktidentität" aus, um die Herausgeberdetails für die Verwendung im Abschnitt ["Paket für Ihre PWA"](#package-your-pwa-for-the-store)  >  **** anzuzeigen.  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Kopieren Ihrer Herausgeberinformationen aus Windows Partner Center" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       Kopieren Ihrer Herausgeberinformationen aus Windows Partner Center  
    :::image-end:::  
    
1.  Kopieren und speichern Sie die folgenden Werte.  
    *   **Paket-ID**  
    *   **Herausgeber-ID**  
    *   **Publisher Anzeigename**  
        
## <a name="package-your-pwa-for-the-store"></a>Verpacken Der PWA für die Store 

Nachdem Sie nun über Ihre App-Veröffentlichungsinformationen verfügen, generieren Sie ein Windows App-Paket für Ihre PWA.

Führen Sie die folgenden Aktionen aus, um ein App-Paket zu generieren.  

1.  Navigieren Sie zu [PWA Generator][PwabuilderMain].  
1.  Geben Sie die URL Ihrer PWA ein.  
1.  Wählen **** Sie  >  **"Start Build My PWA**  >  **Windows**  >  **Options"** aus.  
1.  Fügen Sie die folgenden Werte ein, die Sie im Abschnitt ["App-Reservierung erstellen"](#create-an-app-reservation) gespeichert haben.  
    *   **Paket-ID**  
    *   **Herausgeber-ID**  
    *   **Publisher Anzeigename**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Einfügen von Herausgeberinformationen in PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       Einfügen von Herausgeberinformationen in PWABuilder  
    :::image-end:::  
    
1.  Wählen Sie **"Fertig" aus.**  
1.  Um Ihr Windows-App-Paket herunterzuladen, wählen Sie **"Herunterladen"** aus.

Ihr Download ist ein `.zip` Archiv, das eine `.msixbundle` Datei und eine Datei `.classic.appxbundle` enthält.  Mit den beiden App-Paketen können Ihre PWA auf einer Vielzahl von Windows Versionen ausgeführt werden.  Navigieren Sie für weitere Informationen zu ["Was ist ein klassisches Paket?".][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]  

### <a name="submit-your-app-package-to-the-store"></a>Übermitteln Des App-Pakets an die Store  

Führen Sie die folgenden Aktionen aus, um Ihre App an die Store zu übermitteln.  

1.  Navigieren Sie zu [Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] 
1.  Wählen Sie Ihre App aus.  
1.  Wählen Sie **"Übermittlung starten" aus.**  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Starten einer neuen App-Übermittlung im Windows Partner Center" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       Starten einer neuen App-Übermittlung im Windows Partner Center  
    :::image-end:::  
    
1.  Führen Sie die folgenden Eingabeaufforderungen aus, um Informationen zu Ihrer App zu erhalten.
    *   pricing  
    *   Altersfreigabe  
    *   und mehr  
        
1.  Wählen Sie in der Aufforderung **"Pakete"** die `.msixbundle` Dateien aus, `.classic.appxbundle` die Sie im Abschnitt ["Verpacken Ihres PWA"](#package-your-pwa-for-the-store) generiert haben.  
    
Nach Abschluss der Übermittlung wird Ihre App überprüft, in der Regel innerhalb von 24 bis 48 Stunden.  Nachdem Sie die Genehmigung erhalten haben, ist Ihre PWA im Microsoft Store verfügbar.  

### <a name="measure-usage-of-your-store-installed-pwa"></a>Messen der Nutzung Ihrer Store installierten PWA

Wenn Ihre PWA gestartet wird und die PWA über die Microsoft Store installiert wurde, enthält Microsoft Edge den folgenden `Referer` Header mit der Anforderung für die erste Navigation Ihrer Web-App.

```
Referer: app-info://platform/microsoft-store
```

Verwenden Sie dieses Feature, um den Datenverkehr von Ihren Store installierten PWA zu messen.  Basierend auf dem Datenverkehr können Sie die Inhalte Ihrer App anpassen, um die Benutzererfahrung zu verbessern.  Auf dieses Feature kann sowohl auf Client- als auch auf Servercode zugegriffen werden.

Dieses Feature wurde in Microsoft Edge Version 91 eingeführt.

## <a name="see-also"></a>Weitere Informationen  

PWABuilder bietet weitere Dokumentation, die Ihnen dabei hilft, Ihre PWA im Microsoft Store zu erhalten.  

*   [Testen und Übermitteln Ihres PWA-App-Pakets][GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]  
*   [Veröffentlichen eines neuen PWA im Store][GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]  
*   [Aktualisieren einer vorhandenen Store-App auf eine PWA][GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]  
*   [Bildempfehlungen für PWAs im Store][GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]  
*   [Erklärung zum Packen von Apps][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Microsoft Store Richtlinien | Microsoft-Dokumente"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analysieren der App-Leistung | Microsoft-Dokumente"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "App-Screenshots, Bilder und Trailer | Microsoft-Dokumente"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Veröffentlichen Windows Apps und Spiele | Microsoft-Dokumente"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Home | Microsoft Partner Center"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Ressourcen für Partner | Microsoft Partner Center"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Apps | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "| für gehostete App-Modelle Windows Entwicklerblog"  

[GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/classic-package.md "Was ist ein klassisches Paket? | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/image-recommendations.md "Bildempfehlungen für Windows PWA Pakete | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/next-steps.md "Nächste Schritte, um Ihre PWA in die Microsoft Store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/publish-new-app.md "Veröffentlichen einer neuen App im Store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/update-existing-app.md "Aktualisieren einer vorhandenen App im Store | GitHub"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  
