---
title: Översikt över uppgifter för inställning av Business Central
description: 'Läs en översikt av de uppgifter som krävs för att installera, initialisera och konfigurera Business Central för att passa just dina behov.'
author: brentholtorf
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'configure, initialize'
ms.date: 12/19/2023
ms.author: bholtorf
---
# Översikt över arbetsuppgifter för att ställa in [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_short](includes/prod_short.md)] inkluderar standardinställningar för de flesta verksamhetsprocesser, men du kan ändra konfigurationen så att denna passar organisationens behov. Med hjälp av artiklarna i [Business Central snabbstart](quick-start-business-central.md) kan du ta de första stegen att göra [!INCLUDE [prod_short](includes/prod_short.md)] till din egen. Den här artikeln innehåller en översikt över hur du kan konfigurera [!INCLUDE [prod_short](includes/prod_short.md)] för organisationen.

Till exempel fylls kontoplanen i med bokföringskonton som är klara för användning. Du kan naturligtvis ändra kontoplanen så att dessa stämmer överens med dina behov. Läs mer i [Finans](finance.md).

Från ![Kugghjulsikon för att öppna menyn Inställningar.](media/ui-experience/settings_icon_small.png) kan du få åtkomst till assisterade konfigurationsguider som gör det enklare att ställa in vissa scenarier och lägga till funktioner i [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer om hur du får åtkomst till samtliga assisterade och manuella konfigurationssidor på [Gör dig redo att göra affärer](ui-get-ready-business.md).

> [!NOTE]
> [!INCLUDE [ua-checklist](includes/ua-checklist.md)]

Utöver guiderna för assisterad konfiguration kan några allmänna funktioner och specifika affärsprocesser konfigureras manuellt. I följande tabell anges några av de funktioner som du kan ställa in manuellt.

| Till | Gå till |
| --- | --- |
| Ställa in betalningsmetoder, valutor, bankkonton och definiera regler och standarder för att hantera ekonomiska transaktioner. |[Ställa in Finance](finance-setup-finance.md) |
| Ställa in egna och dina leverantörers bankkontonoch aktivera tjänster för import och export av bankfiler. |[Ställa in bankverksamhet](bank-setup-banking.md) |
| Konfigurera reglerna och värdena som definierar företagets försäljningspolicyer, registrera nya kunder och ställa in hur du kommunicerar med kunderna. |[Konfigurera försäljning](sales-setup-sales.md) |
| Konfigurera de regler och värden som kan styra företagets inköp, registrera nya leverantörer och prioritera leverantörerna för betalningshantering. |[Ställa in inköp](purchasing-setup-purchasing.md) |
| Konfigurera reglerna och värdena som definierar företagets lagerpolicyer, ställa in lagerställen om du vill hålla lager på flera distributionslager och kategorisera artiklar för att förbättra sökning och sortering. |[Ställa in lager](inventory-setup-inventory.md) |
|Ange standardrapporter som ska användas med olika dokumenttyper.|[Rapportval för dokument](across-report-selections.md)|
| Ställa in hur du ställer in resurser och tidrapporter och projekt för att hantera projekt. |[Ställa in projekthantering](projects-setup-projects.md) |
| Konfigurera hur du försäkrar, underhåller och skriver av anläggningstillgångar och hur du registrerar kostnader för anläggningstillgångar i företagets redovisning. |[Ställa in anläggningstillgångar](fa-setup.md) |
|Definiera allmänna regler och värden för lagerprocesser och särskild hantering vid varje lagerställe.|[Ställa in lagerstyrning](warehouse-setup-warehouse.md)|
|Förbereda produktionsstrukturer och verksamhetsföljder för att definiera hur artiklar tillverkas och förbereda maskin- eller produktionsgrupper för att vidta nödvändiga åtgärder.|[Ställa in Produktion](production-configure-production-processes.md)|
|Standardtjänster, symptom och felkoder och skapa serviceartiklar, resurser och dokumentation som behövs för att tillhandahålla service till kunder.|[Ställa in tjänstehantering](service-setup-service.md)|
|Läs om bästa praxis för att konfigurera artiklar för lagerkostnad och leveransplanering.|[Ställa in komplexa moduler med hjälp av bästa praxis](set-up-complex-application-areas-using-best-practices.md)|
|Förbättra kvalitet på implementeringen och minska driftsättningstiden med hjälp av en uppsättning verktyg för att skapa ett nytt företag med hjälp av guider, mallar, kalkylblad och frågeformulär för kunden.|[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)|
|Överför information för kunder, leverantörer, lager och bankkonton från ett annat system i [!INCLUDE[prod_short](includes/prod_short.md)]|[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)|
|Använd tillägget Business Central Outlook för att se ekonomiska data som relateras till kunder och leverantörer, samt visa och skicka ekonomiska dokument som t.ex offerter och fakturor.|[Använda Business Central som din företagsinkorg i Outlook](admin-outlook.md)|
|Få insyn i Business Central-data med hjälp av Power BI och Business Central-innehållspaket.|[Aktivera dina affärsdata för Power BI](admin-powerbi.md)|
|Använd Business Central-data som en del av ett arbetsflöde i Power Automate.|[Använda Business Central i ett automatiskt arbetsflöde](across-how-use-financials-data-source-flow.md)|
|Gör din Business Central-data tillgänglig som underlag för datakälla i Power Apps.|[Ansluta till dina Business Central-data i syfte att skapa en företagsapp med hjälp av Power Apps](across-how-use-financials-data-source-powerapps.md)|
|Använd särskilda Quickbooks migreringsguider.|[Om du byter från en QuickBooks-app till Business Central](across-quickbooks-to-business-edition.md)|
|Komma åt Business Central-data från en mobil enhet.|[Få Business Central på din mobila enhet](install-mobile-app.md)|
|Bulkfakturera avtalade tider som skapats i Microsoft Bookings.|[Bulkfakturera för Microsoft Bookings](finance-bookings.md)|
|Skapa en SMTP-server för att aktivera e-postkommunikation i och utanför [!INCLUDE[prod_short](includes/prod_short.md)].| [Konfigurera e-post manuellt eller med hjälp av assisterad konfiguration](admin-how-setup-email.md)|
| Skapa unika identifieringskoder för poster, som till exempel kort, dokument och journalrader, för att spåra dem i systemet. |[Skapa nummerserier](ui-create-number-series.md) |
|Konfigurera och tilldela företaget och dess affärspartner, till exempel kunder, leverantörer och lagerställen, en baskalender. De angivna arbetsdagarna i kalendern används för att beräkna leveransdatum och inleveransdatum på rader på försäljningsorder, inköpsorder, överföringsorder och produktionsorder.|[Skapa baskalendrar](across-how-to-assign-base-calendars.md)|

Vissa områden kräver att du är administratör i din [!INCLUDE[prod_short](includes/prod_short.md)]-prenumeration. Läs mer i [Administration](admin-setup-and-administration.md).  

> [!NOTE]
> Som administratör kan du skapa ett nytt företag i [!INCLUDE[prod_short](includes/prod_short.md)] med RapidStart Services som är ett verktyg utformat för att förkorta distributionstider, förbättra implementeringskvaliteten, införa en upprepningsbar implementeringsmetod samt öka produktiviteten genom att automatisera och underlätta återkommande uppgifter. Läs mer på [Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

## Konfigurera appar

Utöver huvudfunktionerna i [!INCLUDE [prod_short](includes/prod_short.md)] lägger Microsoft till några appar som anges på [sidan **Tilläggshantering**](https://businesscentral.dynamics.com/?page=2500). Från och med oktober 2022 ger varje app en länk som öppnar konfigurationssidan – bara välj åtgärden **Konfigurera**.  

Du kan också lägga till funktioner i [!INCLUDE [prod_short](includes/prod_short.md)] genom att lägga till AppSource-appar. Läs mer på [Anpassa Business Central Online med hjälp av tillägg](ui-extensions.md).  

## Se även

[Företagsinformation, översikt](admin-company-information.md)  
[Administration](admin-setup-and-administration.md)  
[Ekonomi](finance.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Lager](inventory-manage-inventory.md)  
[Projekthantering](projects-manage-projects.md)  
[Anläggningstillgångar](fa-manage.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Produktion](production-manage-manufacturing.md)  
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Skapa nya företag i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Snabbstart för Business Central](quick-start-business-central.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
