---
title: Installera tillägg för att anpassa Business Central | Microsoft Docs
description: Lär dig mer om att lägga till funktioner och att anpassa Business Central genom att installera tillägg.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 06/13/2019
ms.author: edupont
ms.openlocfilehash: e1f7d9891be4ae31fc3f98fb768bfddcd38582ca
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629878"
---
# <a name="customizing-business-central-using-extensions"></a>Anpassa Business Central med tillägg
Du kan ändra [!INCLUDE[d365fin](includes/d365fin_md.md)] genom att installera tillägg som lägger till funktioner, ändrar beteende eller ger dig tillgång till nya onlinetjänster.
När du först startar först [!INCLUDE[d365fin](includes/d365fin_md.md)], har du dessutom några tillägg installerade. Med tiden kommer fler tillägg att göras tillgängliga till dig, och du kan då välja om du vill använda tillägg eller inte.

Till exempel ger Microsoft ett tillägg som ger integrering med PayPal Payments Standard. Detta tillägg instalelras dessutom som standard.
Men om ett annat tillägg är tillgängligt som erbjuder integrering med en annan utbetalningtjänst, kan du installera det nya tillägget och sedan välja vilka av de två tjänsterna som ska användas.  

Du hanterar tilläggen på sidan **Tilläggshantering**. Du kan öppna den här sidan från startsidan. Du kan också välja ikonen **Sök efter sidan eller rapporten** ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") i övre högra hörnet och ange **tillägg** och välj sedan den relaterade länken.  

> [!NOTE]  
>   Om du tror att du borde ha åtkomst till ett tillägg, men dess funktioner inte går att hitta kontrollerar du sidan **tilläggshantering** om tillägget inte finns, kan du installera det enligt vad som beskrivs i följande avsnitt.  

## <a name="installing-an-extension"></a>Installerar tillägg
Du kan skapa nya tillägg från marknadsplatsen på [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?src=dynamics365website&product=dynamics-365-business-central). Här kan du se alla tillgängliga tillägg för [!INCLUDE[d365fin](includes/d365fin_md.md)], och du kan få program, tillägg och innehållspaket för andra Microsoft-produkter. Ange relevanta filter, ta en titt på varje tilläggs uppgifter och få tillägg för ditt [!INCLUDE[d365fin](includes/d365fin_md.md)].  
> [!NOTE]  
>   Logga in på [AppSource.microsoft.com](https://appsource.microsoft.com/) med hjälp av e-postkonto som du använder för [!INCLUDE[d365fin](includes/d365fin_md.md)]. Använd samma e-postkonto för andra tjänster och produkter för en bra upplevelse.  

Du kan också komma till marknadsplatsen från [!INCLUDE[d365fin](includes/d365fin_md.md)]. På sidan **Tilläggshantering** kan du se tilläggen som installeras för närvarande, och du kan öppna sidan **tilläggmarknadsplatsen** som visar tilläggen för [!INCLUDE[d365fin](includes/d365fin_md.md)] som för närvarande finns tillgängliga i AppSource. Om du väljer länken *Fler appar* tas du till [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).  

Om du väljer ett tillägg kan du läsa om vad tillägget används till och du kan få mer information om tillägget. När du väljer att få ett tillägg, måste du godkänna användningsvillkoret. Om du får tillägget från AppSource-webbplatsen kommer du att loggas in på [!INCLUDE[d365fin](includes/d365fin_md.md)] för att slutföra installationen.  

När du installerar tillägget kanske du behöver måste konfigurera det, till exempel ange ett konto för användning med tillägget **PayPal Payments Standard för [!INCLUDE[d365fin](includes/d365fin_md.md)]**.
Andra tillägg lägger bara till i fält på en befintlig sida, eller lägger till en ny sida, till exempel.   

Om du avinstallerar tillägget och du sedan ändrar dig kan du installera det på nytt. När du avinstallerar tillägg som du har använt, bevaras data så att de är tillgängliga om du installerar tillägget igen.  

Några tillägg ges ut av Microsoft, och andra tillägg ges ut av [andra företag](ui-extensions-other.md). Alla tillägg testas innan de görs tillgängliga för dig, men vi rekommenderar att du öppnar länkarna som tillhandahålls med varje tillägg om du vill veta mer om tillägget innan du väljer att installera det.  

Microsoft ger även följande tillägg:  

* [Revisorportal för Business Central](ui-extensions-accountant-portal.md)
* [Ceridian löner](ui-extensions-ceridian-payroll.md)
* [Dynamics GP Datamigrering](ui-extensions-dynamicsgp-data-migration.md)
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)
* [Information om viktiga affärsdata](ui-extensions-essential-business-insights.md)
* [Image Analyzer](ui-extensions-image-analyzer.md)
* [Intelligent moln](ui-extensions-data-replication.md)
* [Intelligent molnbas](ui-extensions-intelligent-cloud.md)
* [Prediktioner om sen betalning](ui-extensions-late-payment-prediction.md)
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)
* [QuickBooks datamigrering](ui-extensions-quickbooks-data-migration.md)
* [QuickBooks Online Datamigrering](ui-extensions-quickbooks-online-data-migration.md)
* [Importera QuickBooks-lönefil](ui-extensions-quickbooks-payroll.md)
* [Försäljnings- och lagerprognos](ui-extensions-sales-forecast.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK - C5 datamigrering](ui-extensions-c5-data-migration.md)
* [DK - Betalningar och betalningsavstämningar](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK - momsfilformat](ui-extensions-tax-file-formats-dk.md)
* [UK - GetAddress.io för postnummer i Storbritannien](ui-extensions-getaddressio.md)
* [US/CA/UK/AU/NZ/ZA - Skicka kundremissa](ui-extensions-send-remittance-advice.md)
* [Business Central-tillägg från andra leverantörer](ui-extensions-other.md)

> [!NOTE]  
>  Tillägg är inte tillgängliga i AppSource så snart vi meddelar en uppdatering. Du kan hålla utkik efter tillägg i [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).

## <a name="see-also"></a>Se även
[Utökning av Dynamics 365 Business Central](about-develop-extensions.md)  
[Business Central-tillägg från andra leverantörer](ui-extensions-other.md)  
[Skapa tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Så här aktiverar du kundutbetalning via PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Konfigurera tillägget GetAddress.io för postnummer i Storbritannien](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]-tillägg från andra leverantörer](ui-extensions-other.md)  
[Komma igång](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
