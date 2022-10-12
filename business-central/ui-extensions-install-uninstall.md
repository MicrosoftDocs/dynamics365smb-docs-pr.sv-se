---
title: Installera och avinstallera appar
description: Läs mer om hur du kan installera och avinstallera appar och tillägg i Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.search.form: 2500, 20350
ms.date: 09/22/2022
ms.author: solsen
ms.openlocfilehash: db08c13d5e6a5dd29cf9a32b56ab3b5fa9ce77f9
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605988"
---
# <a name="install-and-uninstall-extensions-apps-in-business-central"></a>Installera och avinstallera tillägg (appar) i Business Central

Du kan ändra [!INCLUDE[prod_short](includes/prod_short.md)] genom att installera appar som exempelvis lägger till funktioner, ändrar beteenden eller ger dig tillgång till nya onlinetjänster. Mer information finns i [Anpassa Business Central med hjälp av tillägg](ui-extensions.md).

> [!NOTE]
> Om du vill installera eller avinstallera appar från AppSource eller lägga till appar per klientorganisation måste du ha rätt behörigheter. Du måste antingen vara medlem i EXTEND. MGT. - ADMIN-användargruppen, eller så måste du ha EXTEND. MGT. - ADMIN-behörighetsuppsättningen. Om du är administratör kan du tilldela användargrupper och behörigheter till andra användare i företaget.
>
> Om du vill använda funktionen som tillhandahålls av ett tillägg, till exempel att öppna sidor, köra rapporter, välja åtgärder och så vidare, måste du koppla behörighetsuppsättningarna som installeras som en del av tillägget.

Om du vill använda funktionen som tillhandahålls av ett tillägg, till exempel att öppna sidor, köra rapporter, välja åtgärder och så vidare, måste du koppla behörighetsuppsättningarna som installeras som en del av tillägget.

## <a name="install-an-extension"></a><a name="install"></a>Installera ett tillägg

Du hanterar appar och tillägg på sidan **Tilläggshantering**. Du kan öppna den här sidan från startsidan. Välj ikonen **Sök efter sida eller rapport** ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") i det övre högra hörnet ange **Tillägget** och välj sedan relaterad länk.  

Du kan hämta nya appar från marknadsplatsen på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Marknadsplatsen innehåller alla tillgängliga appar för [!INCLUDE[prod_short](includes/prod_short.md)], plus appar och innehållspaket för andra Microsoft-produkter. Ange relevanta filter, ta en titt på varje tilläggs uppgifter och få tillägg för ditt [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Logga in på [AppSource.microsoft.com](https://appsource.microsoft.com/) med hjälp av e-postkonto som du använder för [!INCLUDE[prod_short](includes/prod_short.md)]. Använd samma e-postkonto för andra tjänster och produkter för en bra upplevelse.  

Du kan också komma till AppSource från [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **Tilläggshantering** kan du se apparna som är installerade för närvarande, och du kan öppna sidan **Tilläggmarknadsplatsen** som visar apparna för [!INCLUDE[prod_short](includes/prod_short.md)] som för närvarande finns tillgängliga i AppSource. Om du väljer länken *Fler appar* tas du till [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Om du väljer en app kan du läsa om vad appen används till och du kan få mer information om appen i hjälpavsnittet. När du väljer att hämta en app, måste du godkänna användningsvillkoret. Om du hämtar appen från AppSource-webbplatsen kommer du att loggas in på [!INCLUDE[prod_short](includes/prod_short.md)] för att slutföra installationen.  

När du har installerat en app måste du kanske konfigurera den. I vissa appar måste du ange en del information innan du kan använda dem. Till exempel måste du, när du har installerat appen **PayPal Payments Standard**, ange e-postadressen eller konto-ID för ditt PayPal-konto. Om du vill konfigurera en app eller ta reda på vilken information du behöver går du till sidan **Installerade tillägg** och väljer åtgärden **Konfigurera**.  

Andra appar lägger bara till fält på en befintlig sida, eller lägger till en ny sida, till exempel.

Om du avinstallerar en app och du sedan ändrar dig kan du installera den på nytt. När du avinstallerar en app som du har använt, bevaras data så att de är tillgängliga om du installerar appen igen. Det finns vissa appar som krävs. Du kan inte avinstallera dessa appar från sidan **Tilläggshantering**. Om du försöker visas ett felmeddelande.

Några appar ges ut av Microsoft, och andra appar ges ut av [andra företag](ui-extensions-other.md). Alla appar testas innan de görs tillgängliga för dig, men vi rekommenderar att du öppnar länkarna som tillhandahålls med varje app om du vill veta mer om appen innan du väljer att installera den.

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

## <a name="set-up-an-extension"></a>Konfigurera ett tillägg
När du har installerat en app måste du kanske konfigurera den. Till exempel för appen **PayPal Payments Standard för [!INCLUDE[prod_short](includes/prod_short.md)]** måste du ange det PayPal-konto som ska användas. Om så är fallet frågar [!INCLUDE[prod_short](includes/prod_short.md)], när installationen har slutförts, om du vill konfigurera appen direkt. Konfigurationer kan krävas för att appen ska fungera, eller så kan de vara valfria.

Om du väljer att konfigurera din app direkt och den har en konfiguration som krävs, öppnar [!INCLUDE[prod_short](includes/prod_short.md)] den konfiguration som krävs. Konfigurationen kan vara antingen en sida där du anger information eller en guide för assisterad konfiguration som hjälper dig genom stegen. Om du inte slutför konfigurationen på en gång kan du använda sidan **Konfigurationer för _appens namn_**, som innehåller en lista över alla konfigurationer för appen. Obligatoriska konfigurationer anges i **fetstil**.

## <a name="upload-a-per-tenant-extension-pte"></a>Ladda upp ett tillägg per klientorganisation (PTE)

Du överför en PTE med hjälp av sidan för **tilläggshantering**. På siden **Tilläggshantering**, gå till **Hantera**, välj sedan **Ladda upp tillägg**. Sidan **Ladda upp och distribuera tillägg** ange vilken .app-fil som ska laddas upp. Om du vill fortsätta klickar du på knappen **Acceptera** och sedan knappen **Distribuera**, detta kommer att starta processen med att distribuera PTE.

Om PTE innehåller bryt schemaändringar går det att *Framtvinga* en uppladdning av den. Det gör du i läget för **Synkroniseringsläge för schema** välja alternativet **Framtvinga**. Du får en bekräftelse dialogruta som du kan ta emot innan du fortsätter.  

## <a name="uninstall-an-app"></a>Avinstallera en app

Du avinstallerar en app på sidan **Tilläggshantering**. Om du vill avinstallera en app markerar du den på sidan och väljer åtgärden **Avinstallera**. Om du avinstallerar en app och du sedan ändrar dig kan du installera appen på nytt.

När du avinstallerar en app som du har använt bevaras data som standard så att de finns tillgängliga om du installerar appen igen. Du kan i stället välja att ta bort datan tillsammans med appen. Denna åtgärd styrs av växlingen **Ta bort tilläggsdata**. Funktionen är normalt inte **aktiv**. När du försöker aktivera **Ta bort tilläggsdata** för appen visas en bekräftelsedialog och du måste välja **Ja** för att aktivera den. När växlingen **Ta bort tilläggsdata** är aktiverad kan du avinstallera appen, bekräfta att du vill avinstallera appen och ta bort datan.

> [!IMPORTANT]  
> - Det kan finnas andra appar som kräver eller är beroende av den app som du vill avinstallera för att kunna fungera. Dessa andra appar kallas för *beroenden*. Du kan inte avinstallera en app såvida inte dess beroenden också avinstalleras.
> - När du väljer att avinstallera en app som har ett eller flera beroenden visas en bekräftelsedialogruta med en lista över beroenden och du tillfrågas om du vill avinstallera appen och alla dess beroenden. Du måste välja **Ja** för att fortsätta.
> - Om du aktiverar **Ta bort tilläggsdata** tas alla data för appen bort när du avinstallerar appen, **plus** data för alla beroende appar. Denna åtgärd kan inte ångras.
> - Vissa appar är obligatoriska. Du kan inte avinstallera dem från sidan **Tilläggshantering**. Om du försöker visas ett felmeddelande.  

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