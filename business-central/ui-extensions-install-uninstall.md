---
title: Installera och avinstallera tillägg i Business Central | Microsoft Docs
description: Läs mer om att installera och avinstallera tillägg i Business Central.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: bcd7a60f9e8fd6739a3d09f5aa1b3e6819e3ccc3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757549"
---
# <a name="installing-and-uninstalling-extensions-in-business-central"></a>Installera och avinstallera tillägg i Business Central

Du kan ändra [!INCLUDE[prod_short](includes/prod_short.md)] genom att installera tillägg som exempelvis lägger till funktioner, ändrar beteenden eller ger dig tillgång till nya onlinetjänster. Mer information finns i [Anpassa Business Central med hjälp av tillägg](ui-extensions.md).

> [!NOTE]
> Om du vill installera tillägg från AppSource eller lägga till tillägg per klientorganisation måste du ha rätt behörigheter. Du måste antingen vara medlem i användargruppen D365 Tilläggshant. eller så måste du ha behörighetsuppsättningen D365 Tilläggshant. Om du är administratör kan du tilldela användargrupper och behörigheter till andra användare i företaget.<br /><br />
Om du vill använda funktionen som tillhandahålls av ett tillägg, till exempel att öppna sidor, köra rapporter, välja åtgärder och så vidare, måste du koppla behörighetsuppsättningarna som installeras som en del av tillägget.

## <a name="installing-an-extension"></a>Installerar tillägg

Du hanterar tillägg på sidan **Tilläggshantering**. Du kan öppna den här sidan från startsidan. Du kan också välja ikonen **Sök efter sidan eller rapporten** ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") i övre högra hörnet och ange **tillägg** och välj sedan den relaterade länken.  

Du kan skapa nya tillägg från marknadsplatsen på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Här kan du se alla tillgängliga tillägg för [!INCLUDE[prod_short](includes/prod_short.md)], och du kan få program, tillägg och innehållspaket för andra Microsoft-produkter. Ange relevanta filter, ta en titt på varje tilläggs uppgifter och få tillägg för ditt [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Logga in på [AppSource.microsoft.com](https://appsource.microsoft.com/) med hjälp av e-postkonto som du använder för [!INCLUDE[prod_short](includes/prod_short.md)]. Använd samma e-postkonto för andra tjänster och produkter för en bra upplevelse.  

Du kan också komma till marknadsplatsen från [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **Tilläggshantering** kan du se tilläggen som installeras för närvarande, och du kan öppna sidan **tilläggmarknadsplatsen** som visar tilläggen för [!INCLUDE[prod_short](includes/prod_short.md)] som för närvarande finns tillgängliga i AppSource. Om du väljer länken *Fler appar* tas du till [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

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

## <a name="uninstalling-an-extension"></a>Avinstallera ett tillägg

Du avinstallerar ett tillägg på sidan **Tilläggshantering**. Om du avinstallerar ett tillägg och du sedan ändrar dig kan du installera tillägget på nytt. När du avinstallerar ett tillägg som du har använt bevaras data som standar så att de finns tillgängliga om du installerar tillägget igen. Du kan i stället välja att ta bort datan tillsammans med tillägget. Detta styrs av kryssrutan **Ta bort tilläggsdata**. Denna kryssruta är som standard *inte aktiverad*.

> [!IMPORTANT]  
> Om du aktiverar kryssrutan **Ta bort tilläggsdata** visas en bekräftelsedialogruta där du väljer **OK**. När kryssrutan **Ta bort tilläggsdata** är aktiverad kan du avinstallera filtillägget, bekräfta att du vill avinstallera tillägget och ta bort datan. Denna åtgärd kan inte ångras.
Vissa tillägg är obligatoriska. Du kan inte avinstallera dem från sidan för **tilläggshantering**. Om du försöker visas ett felmeddelande.  

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


[!INCLUDE[footer-include](includes/footer-banner.md)]