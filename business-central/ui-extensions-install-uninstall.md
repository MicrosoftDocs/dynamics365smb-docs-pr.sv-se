---
title: Installera och avinstallera tillägg
description: Läs mer om att installera och avinstallera tillägg i Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.search.form: 2500
ms.date: 03/25/2022
ms.author: solsen
ms.openlocfilehash: fcdfe843071bc416973b7411e5702a690e7e377d
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514757"
---
# <a name="install-and-uninstall-extensions-in-business-central"></a>Installera och avinstallera tillägg i Business Central

Du kan ändra [!INCLUDE[prod_short](includes/prod_short.md)] genom att installera tillägg som exempelvis lägger till funktioner, ändrar beteenden eller ger dig tillgång till nya onlinetjänster. Mer information finns i [Anpassa Business Central med hjälp av tillägg](ui-extensions.md).

> [!NOTE]
> Om du vill installera eller avinstallera tillägg från AppSource eller lägga till tillägg per klientorganisation måste du ha rätt behörigheter. Du måste antingen vara medlem i EXTEND. MGT. - ADMIN-användargruppen, eller så måste du ha EXTEND. MGT. - ADMIN-behörighetsuppsättningen. Om du är administratör kan du tilldela användargrupper och behörigheter till andra användare i företaget.
>
> Om du vill använda funktionen som tillhandahålls av ett tillägg, till exempel att öppna sidor, köra rapporter, välja åtgärder och så vidare, måste du koppla behörighetsuppsättningarna som installeras som en del av tillägget.

> [!NOTE]  
> Behörighetsuppsättningen **EXTEND. MGT. – ADMIN** infördes i Business Central 2021 utgivningscykel 1 som ersättning av behörighetsuppsättningen **D365 EXTENSION MGT** i tidigare versioner.

## <a name="install-an-extension"></a><a name="install"></a>Installera ett tillägg

Du hanterar tillägg på sidan **Tilläggshantering**. Du kan öppna den här sidan från startsidan. Välj ikonen **Sök efter sida eller rapport** ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") i det övre högra hörnet ange **Tillägget** och välj sedan relaterad länk.  

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

## <a name="upload-a-per-tenant-extension-pte"></a>Ladda upp en PTE (tillägg per klientorganisation)

Du överför en PTE med hjälp av sidan för **tilläggshantering**. På siden **Tilläggshantering**, gå till **Hantera**, välj sedan **Ladda upp tillägg**. Sidan **Ladda upp och distribuera tillägg** ange vilken .app-fil som ska laddas upp. Om du vill fortsätta klickar du på knappen **Acceptera** och sedan knappen **Distribuera**, detta kommer att starta processen med att distribuera PTE.

Om PTE innehåller bryt schemaändringar går det att *Framtvinga* en uppladdning av den. Det gör du i läget för **Synkroniseringsläge för schema** välja alternativet **Framtvinga**. Du får en bekräftelse dialogruta som du kan ta emot innan du fortsätter.  

## <a name="uninstall-an-extension"></a>Avinstallera ett tillägg

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
[Gör dig redo att göra affärer](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]