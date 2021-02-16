---
title: Installera tillägg för att anpassa Business Central
description: Lär dig mer om att lägga till funktioner och att anpassa Business Central genom att installera tillägg.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: app, add-in, manifest, customize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fa72fad5899fab4830bf6c0956eaf99b6c773a53
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757023"
---
# <a name="customizing-business-central-using-extensions"></a>Anpassa Business Central med tillägg

Du kan ändra [!INCLUDE[prod_short](includes/prod_short.md)] genom att installera tillägg som lägger till funktioner, ändrar beteende eller ger dig tillgång till nya onlinetjänster.

> [!NOTE]
> Om du vill installera tillägg från AppSource eller lägga till tillägg per klientorganisation måste du ha rätt behörigheter. Du måste antingen vara medlem i användargruppen D365 Tilläggshant. eller så måste du ha behörighetsuppsättningen D365 Tilläggshant. Om du är administratör kan du tilldela användargrupper och behörigheter till andra användare i företaget.

Om du vill använda funktionen som tillhandahålls av ett tillägg, till exempel att öppna sidor, köra rapporter, välja åtgärder och så vidare, måste du koppla behörighetsuppsättningarna som installeras som en del av tillägget.

> [!IMPORTANT]  
> Överföring av tillägg per innehavare och installation av AppSource-tillägg stöds inte via sidan **Tilläggshantering** för lokala installationer.

När du först startar först [!INCLUDE[prod_short](includes/prod_short.md)], har du dessutom några tillägg installerade. Med tiden kommer fler tillägg att göras tillgängliga till dig, och du kan då välja om du vill använda tillägg eller inte.

Till exempel ger Microsoft ett tillägg som ger integrering med PayPal Payments Standard. Detta tillägg instalelras dessutom som standard.
Men om ett annat tillägg är tillgängligt som erbjuder integrering med en annan utbetalningtjänst, kan du installera det nya tillägget och sedan välja vilka av de två tjänsterna som ska användas.  

Du hanterar tilläggen på sidan **Tilläggshantering**. Du kan öppna den här sidan från startsidan. Du kan också välja ikonen **Sök efter sidan eller rapporten** ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") i övre högra hörnet och ange **tillägg** och välj sedan den relaterade länken. Mer information finns i [Installera och avinstallera tillägg](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Om du tror att du borde ha åtkomst till ett tillägg, men dess funktioner inte går att hitta kontrollerar du sidan **tilläggshantering** om tillägget inte finns, kan du installera det enligt vad som beskrivs i följande avsnitt.  

> [!NOTE]  
> Logga in på [AppSource.microsoft.com](https://appsource.microsoft.com/) med hjälp av e-postkonto som du använder för [!INCLUDE[prod_short](includes/prod_short.md)]. Använd samma e-postkonto för andra tjänster och produkter för en bra upplevelse.  

Du kan också komma till marknadsplatsen från [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **Tilläggshantering** kan du se tilläggen som installeras för närvarande, och du kan öppna sidan **tilläggmarknadsplatsen** som visar tilläggen för [!INCLUDE[prod_short](includes/prod_short.md)] som för närvarande finns tillgängliga i AppSource. Om du väljer länken *Fler appar* tas du till [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Om du väljer ett tillägg kan du läsa om vad tillägget används till och du kan få mer information om tillägget. När du väljer att få ett tillägg, måste du godkänna användningsvillkoret. Om du får tillägget från AppSource-webbplatsen kommer du att loggas in på [!INCLUDE[prod_short](includes/prod_short.md)] för att slutföra installationen.  

När du installerar tillägget kanske du behöver måste konfigurera det, till exempel ange ett konto för användning med tillägget **PayPal Payments Standard för [!INCLUDE[prod_short](includes/prod_short.md)]**.
Andra tillägg lägger bara till i fält på en befintlig sida, eller lägger till en ny sida, till exempel.   

Om du avinstallerar tillägget och du sedan ändrar dig kan du installera det på nytt. När du avinstallerar tillägg som du har använt, bevaras data så att de är tillgängliga om du installerar tillägget igen. Det finns vissa tillägg som krävs. Du kan inte avinstallera dem från sidan för **tilläggshantering**. Om du försöker visas ett felmeddelande.  

Några tillägg ges ut av Microsoft, och andra tillägg ges ut av [andra företag](ui-extensions-other.md). Alla tillägg testas innan de görs tillgängliga för dig, men vi rekommenderar att du öppnar länkarna som tillhandahålls med varje tillägg om du vill veta mer om tillägget innan du väljer att installera det.  

Microsoft ger även följande tillägg:  

* [AMC Banking 365 Fundamentals-tillägg](ui-extensions-amc-banking.md)
* [Ceridian löner](ui-extensions-ceridian-payroll.md)
* [Företagsnav](ui-extensions-company-hub.md)  
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
* [Momsgrupp](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK – C5 datamigrering](ui-extensions-c5-data-migration.md)
* [DK – Betalningar och betalningsavstämningar](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK – momsfilformat](ui-extensions-tax-file-formats-dk.md)
* [Tillägget GetAddress.io för postnummer i Storbritannien ](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA – Skicka kundremissa](ui-extensions-send-remittance-advice.md)

> [!NOTE]  
> Tillägg är inte tillgängliga i AppSource så snart vi meddelar en uppdatering. Du kan hålla utkik efter tillägg i [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="see-also"></a>Se även

[Anpassa Business Central](ui-customizing-overview.md)  
[Business Central-tillägg från andra leverantörer](ui-extensions-other.md)  
[Skapa tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Så här aktiverar du kundutbetalning via PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Konfigurera tillägget GetAddress.io för postnummer i Storbritannien](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-tillägg från andra leverantörer](ui-extensions-other.md)  
[Komma igång](product-get-started.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
