---
title: "Anpassa din Dynamics 365 for Financials med tillägg | Microsoft Docs"
description: "Anpassa din Dynamics 365 for Financials med tillägg"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 04/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1de01d9944489f862dfc6db145c1542c3d0dd2e3
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="customizing-dynamics-365-for-financials-using-extensions"></a>Anpassa din Dynamics 365 for Financials med tillägg
Du kan ändra [!INCLUDE[d365fin](includes/d365fin_md.md)] genom att installera tillägg som lägger till funktioner, ändrar beteende eller ger dig tillgång till nya onlinetjänster.
När du först startar först [!INCLUDE[d365fin](includes/d365fin_md.md)], har du dessutom några tillägg installerade. Med tiden kommer fler tillägg att göras tillgängliga till dig, och du kan då välja om du vill använda tillägg eller inte.

Till exempel ger Microsoft ett tillägg som ger integrering med PayPal Payments Standard. Detta tillägg instalelras dessutom som standard.
Men om ett annat tillägg är tillgängligt som erbjuder integrering med en annan utbetalningtjänst, kan du installera det nya tillägget och sedan välja vilka av de två tjänsterna som ska användas.  

Du hanterar tilläggen i fönstret **Tilläggshantering**. Du kan öppna det här fönstret från startsidan. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten") i det övre högra hörnet anger du **Underhåll, nästa service**, och välj sedan relaterad länk.  

**Obs!** Om du tror att du borde ha åtkomst till ett tillägg, men dess funktioner inte går att hitta kontrollerar du fönstret **tilläggshantering** om tillägget inte finns, kan du installera det enligt vad som beskrivs i följande avsnitt.  

## <a name="installing-an-extension"></a>Installerar tillägg
Du kan skapa nya tillägg från marknadsplatsen på [AppSource.microsoft.com](https://appsource.microsoft.com/). Här kan du se alla tillgängliga tillägg för [!INCLUDE[d365fin](includes/d365fin_md.md)], och du kan få program, tillägg och innehållspaket för andra Microsoft-produkter. Ange relevanta filter, ta en titt på varje tilläggs uppgifter och få tillägg för ditt [!INCLUDE[d365fin](includes/d365fin_md.md)].  
**Obs!** Logga in på [AppSource.microsoft.com](https://appsource.microsoft.com/) med hjälp av e-postkonto som du använder för [!INCLUDE[d365fin](includes/d365fin_md.md)]. Använd samma e-postkonto för andra tjänster och produkter för en bra upplevelse.  

Du kan också komma till marknadsplatsen från [!INCLUDE[d365fin](includes/d365fin_md.md)]. I fönstret **Tilläggshantering** kan du se tilläggen som installeras för närvarande, och du kan öppna sidan **tilläggmarknadsplatsen** som visar tilläggen för [!INCLUDE[d365fin](includes/d365fin_md.md)] som för närvarande finns tillgängliga i AppSource. Om du väljer länken *Fler appar* tas du till [AppSource.microsoft.com](https://appsource.microsoft.com/).  

Om du väljer ett tillägg kan du läsa om vad tillägget används till och du kan få mer information om tillägget. När du väljer att få ett tillägg, måste du godkänna användningsvillkoret. Om du får tillägget från AppSource-webbplatsen kommer du att loggas in på [!INCLUDE[d365fin](includes/d365fin_md.md)] för att slutföra installationen.  

När du installerar tillägget kanske du behöver måste konfigurera det, till exempel ange ett konto för användning med tillägget **PayPal-standardbetalning för [!INCLUDE[d365fin](includes/d365fin_md.md)]**.
Andra tillägg lägger bara till i fält på en befintlig sida, eller lägger till en ny sida, till exempel.   

Om du avinstallerar tillägget och du sedan ändrar dig kan du installera det på nytt. När du avinstallerar tillägg som du har använt, bevaras data så att de är tillgängliga om du installerar tillägget igen.  

Några tillägg ges ut av Microsoft, och andra tillägg ges ut av [andra företag](ui-extensions-other.md). Alla tillägg testas innan de görs tillgängliga för dig, men vi rekommenderar att du öppnar länkarna som tillhandahålls med varje tillägg om du vill veta mer om tillägget innan du väljer att installera det.  

Microsoft ger även följande tillägg:  

* [Dynamics GP Datamigrering](ui-extensions-dynamicsgp-data-migration.md)  
* [Envestnet Yodlee bankfeeder](ui-extensions-yodlee-bank-feeds.md)  
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [QuickBooks datamigrering](ui-extensions-quickbooks-data-migration.md)  
* [Försäljnings- och lagerprognos](ui-extensions-sales-forecast.md)  
* [Ceridian löner](ui-extensions-ceridian-payroll.md)  
* [Importera QuickBooks-lönefil](ui-extensions-quickbooks-payroll.md)  
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)

## <a name="see-also"></a>Se även
[Så här konfigurerar du tjänsten Envestnet Yodlee bankfeeder](bank-how-setup-bank-statement-service.md)  
[Så här aktiverar du kundutbetalning via PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrera verksamhetsdata från andra finanssystem](upload-data.md)  
[Ställ in tillägget GetAddress.io för postnummer i Storbritannien](uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Tillägg av andra leverantörer] (ui-extensions-other.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]] (index.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
