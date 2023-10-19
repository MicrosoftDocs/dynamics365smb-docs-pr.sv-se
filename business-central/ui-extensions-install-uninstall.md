---
title: Installera och avinstallera appar
description: Läs mer om hur du kan installera och avinstallera appar och tillägg i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 09/07/2023
ms.custom: bap-template
ms.search.keywords: 'app, add-in, manifest, customize, install, uninstall'
ms.search.form: '2500, 2514, 20350'
---

# <a name="install-and-uninstall-extensions-apps-in-business-central"></a>Installera och avinstallera tillägg (appar) i Business Central

Du kan ändra [!INCLUDE[prod_short](includes/prod_short.md)] genom att installera appar som exempelvis lägger till funktioner, ändrar beteenden eller ger dig tillgång till nya onlinetjänster. Mer information finns i [Anpassa Business Central med hjälp av tillägg](ui-extensions.md).

> [!NOTE]
> Om du vill installera eller avinstallera appar från AppSource eller lägga till appar per klientorganisation måste du ha rätt behörigheter. Du måste antingen vara medlem i användargruppen D365 Extension MGT, eller också måste du ha EXTEND. MGT. - ADMIN-behörighetsuppsättningen. Om du är administratör kan du tilldela användargrupper och behörigheter till andra användare i företaget. För att lära dig mer om användargrupper och behörigheter, gå till [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).
>
> Om du vill använda funktionen som tillhandahålls av ett tillägg, till exempel att öppna sidor, köra rapporter, välja åtgärder och så vidare, måste du koppla behörighetsuppsättningarna som installeras som en del av tillägget.

Om du vill använda ett tillägg måste du tilldela de behörighetsgrupper som medföljer det.

## <a name="install-an-extension"></a><a name="install"></a>Installera ett tillägg

Du hanterar appar och tillägg på sidan **Tilläggshantering**. Du kan öppna den här sidan från startsidan. Välj ikonen **Sök efter sida eller rapport** ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") i det övre högra hörnet ange **Tillägget** och välj sedan relaterad länk.  

Du kan hämta nya appar från marknadsplatsen på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Marknadsplatsen innehåller alla tillgängliga appar för [!INCLUDE[prod_short](includes/prod_short.md)], plus appar och innehållspaket för andra Microsoft-produkter. Ange relevanta filter, ta en titt på varje tilläggs uppgifter och få tillägg för ditt [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Logga in på [AppSource.microsoft.com](https://appsource.microsoft.com/) med hjälp av e-postkonto som du använder för [!INCLUDE[prod_short](includes/prod_short.md)]. Använd samma e-postkonto för andra tjänster och produkter för en bra upplevelse.  

Du kan också komma till AppSource från [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **Tilläggshantering** kan du se apparna som är installerade för närvarande, och du kan öppna sidan **Tilläggmarknadsplatsen** som visar apparna för [!INCLUDE[prod_short](includes/prod_short.md)] som för närvarande finns tillgängliga i AppSource. Om du väljer länken *Fler appar* tas du till [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Välj en app att lära dig om vad den gör och du kan få mer information om appen i hjälpavsnittet. När du väljer att hämta en app, måste du godkänna användningsvillkoret. Om du hämtar appen från AppSource-webbplatsen kommer du att loggas in på [!INCLUDE[prod_short](includes/prod_short.md)] för att slutföra installationen.  

När du har installerat en app måste du kanske konfigurera den. I vissa appar måste du ange en del information innan du kan använda dem. Till exempel måste du, när du har installerat appen **PayPal Payments Standard**, ange e-postadressen eller konto-ID för ditt PayPal-konto. Om du vill konfigurera en app eller ta reda på vilken information du behöver går du till sidan **Installerade tillägg** och väljer åtgärden **Konfigurera**.  

Andra appar lägger bara till fält på en befintlig sida, eller lägger till en ny sida, till exempel.

Om du avinstallerar en app och du sedan ändrar dig kan du installera den på nytt. När du avinstallerar en app som du har använt dina data tas inte bort. Informationen är tillgänglig om du installerar appen igen.

Några appar ges ut av Microsoft, och andra appar ges ut av [andra företag](ui-extensions-other.md). Vi rekommenderar att du lär dig mer om programmet innan du väljer att installera det.

Microsoft ger även följande appar:

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

## <a name="set-up-an-app"></a>Konfigurera en app

När du har installerat en app måste du kanske konfigurera den. Till exempel för appen **PayPal Payments Standard för [!INCLUDE[prod_short](includes/prod_short.md)]** måste du ange det PayPal-konto som ska användas. Om så är fallet frågar [!INCLUDE[prod_short](includes/prod_short.md)], när installationen har slutförts, om du vill konfigurera appen direkt. Konfigurationer kan krävas för att appen ska fungera, eller så kan de vara valfria.

Om du väljer att konfigurera din app direkt och den har en konfiguration som krävs, öppnar [!INCLUDE[prod_short](includes/prod_short.md)] den konfiguration som krävs. Konfigurationen kan vara antingen en sida där du anger information eller en guide för assisterad konfiguration som hjälper dig genom stegen. Om du inte slutför konfigurationen på en gång kan du använda sidan **Konfigurationer för _appens namn_**, som innehåller en lista över alla konfigurationer för appen. Obligatoriska konfigurationer anges i **fetstil**.

## <a name="upload-a-per-tenant-extension-pte"></a>Ladda upp ett tillägg per klientorganisation (PTE)

Du överför en PTE med hjälp av sidan för **tilläggshantering**. På siden **Tilläggshantering**, gå till **Hantera**, välj sedan **Ladda upp tillägg**. Sidan **Ladda upp och distribuera tillägg** ange vilken .app-fil som ska laddas upp. Om du vill fortsätta klickar du på knappen **Acceptera** och sedan knappen **Distribuera**, detta kommer att starta processen med att distribuera PTE.

Om PTE innehåller bryt schemaändringar går det att *Framtvinga* en uppladdning av den. Det gör du i läget för **Synkroniseringsläge för schema** välja alternativet **Framtvinga**. Du får en bekräftelse dialogruta som du kan ta emot innan du fortsätter.  

## <a name="uninstall-an-app"></a>Avinstallera en app

Du avinstallerar en app på sidan **Tilläggshantering**. Om du vill avinstallera en app markerar du den på sidan och väljer åtgärden **Avinstallera**. Om du avinstallerar en app och du sedan ändrar dig kan du installera appen på nytt.

Som standard, när du avinstallerar en app som du har använt dina data tas inte bort. Om du är säker på att du inte installerar programmet igen och du kan ta bort dem när du avinstallerar den. Om du vill ta bort data när du avinstallerar en app aktiverar du växlingsknappen **Ta bort tilläggsdata**. Du får en bekräftelse dialogruta och du måste välja **Ja** för att aktivera den. När växlingen **Ta bort tilläggsdata** är aktiverad kan du avinstallera appen, bekräfta att du vill avinstallera appen och ta bort datan.

> [!IMPORTANT]  
> * Det kan finnas andra appar som kräver eller är beroende av den app som du vill avinstallera. Dessa appar kallas för *beroenden*. Du kan inte avinstallera en app om du inte också avinstallerar dess anhöriga. När du avinstallerar en app som innehåller underordnade visas en dialog med en lista över de underordnade. Om du vill fortsätta måste du välja **Ja** för att avinstallera programmet och dess beroenden.
> * Om du aktiverar växlingsknappen **Ta bort tilläggsdata** tas alla data för appen bort när du avinstallerar appen, *plus* data för alla beroende appar. Denna åtgärd kan inte ångras.
> * Vissa appar krävs och du kan inte ta bort dem på sidan för **Tilläggshantering**.  

Om du vill behålla data för ett avinstallerat program kan du ta bort datan senare. På sidan **Ta bort överblivna tilläggsdata** visas de program som du fortfarande har data för. Om du vill ta bort datan väljer du programmet och sedan **Ta bort data**. 

## <a name="see-also"></a>Se även

[Anpassa Business Central](ui-customizing-overview.md)  
[Business Central-tillägg från andra leverantörer](ui-extensions-other.md)  
[Konfigurera tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Så här aktiverar du kundutbetalning via PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställ in tillägget GetAddress.io för postnummer i Storbritannien](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-tillägg från andra leverantörer](ui-extensions-other.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
