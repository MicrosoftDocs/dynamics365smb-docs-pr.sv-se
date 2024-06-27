---
title: Anpassa Business Central Online med hjälp av appar
description: Lär dig mer om att lägga till funktioner och att anpassa Business Central genom att installera appar i den här artikeln.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '2500, 2502, 20350, 20353'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---
# Anpassa Business Central Online med hjälp av appar

Du kan ändra [!INCLUDE[prod_short](includes/prod_short.md)] online genom att installera appar som lägger till funktioner, ändrar beteende eller ger dig tillgång till nya onlinetjänster. Dessa appar kallas även *tillägg* eftersom de *utökar* [!INCLUDE [prod_short](includes/prod_short.md)].

## Hantera appar

När du först startar [!INCLUDE[prod_short](includes/prod_short.md)] är några appar redan installerade. Med tiden kommer fler appar att göras tillgängliga till dig, och du kan då välja om du vill använda appen eller inte.

Till exempel ger Microsoft en app som låter dig integrera med PayPal Payments Standard. Detta tillägg instalelras dessutom som standard. Men ett tillägg som erbjuder integration med en annan betaltjänst kan komma med. I så fall kan du installera det nya tillägget och sedan välja vilket du vill använda.  

För att använda en app måste du ha behörighetsuppsättningarna som installerades med den.

Om du vill installera eller avinstallera appar från AppSource eller lägga till tillägg per klientorganisation måste du ha rätt behörigheter. Du måste antingen vara medlem i användargruppen **D365 Extension Mgt.** eller ha behörighetsuppsättningen **EXTENSION MGT - ADMIN**. Om du är administratör kan du tilldela användargrupper och behörigheter till andra användare i företaget. Mer information finns i [Skapa användare enligt licenser](ui-how-users-permissions.md).  

> [!IMPORTANT]  
> För lokalt [!INCLUDE [prod_short](includes/prod_short.md)] kan du inte ladda upp tillägg per klientorganisation eller installera AppSource-appar genom sidan **Tilläggshantering**. Du kan inte installera AppSource-appar lokalt, inklusive i Docker-baserade distributioner.

Du hanterar apparna på sidan **Tilläggshantering**. Du kan öppna den här sidan från startsidan. Du kan också välja ikonen **Sök efter sidan eller rapporten** ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") i övre högra hörnet och ange **tillägg** och välj sedan den relaterade länken. Mer information finns i [Installera och avinstallera appar](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Om du tror att du borde ha åtkomst till en app, men dess funktioner inte går att hitta kontrollerar du sidan **Tilläggshantering**. Om appen inte finns, kan du installera den enligt vad som beskrivs i följande avsnitt.  

> [!NOTE]  
> Logga in på [AppSource.microsoft.com](https://appsource.microsoft.com/) med hjälp av det e-postkonto som du använder för [!INCLUDE[prod_short](includes/prod_short.md)] online. Använd samma e-postkonto för andra tjänster och produkter för en bra upplevelse.  

Du kan också komma till marknadsplatsen från [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **Tilläggshantering** kan du se apparna som är installerade för närvarande, och du kan öppna sidan **Tilläggmarknadsplatsen** som visar apparna för [!INCLUDE[prod_short](includes/prod_short.md)] som för närvarande finns tillgängliga i AppSource. Om du väljer länken *Fler appar* tas du till [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Om du väljer en app kan du läsa om vad appen används till och du kan få mer information om appen i hjälpavsnittet. När du väljer att hämta en app, måste du godkänna användningsvillkoret. Om du hämtar appen från AppSource-webbplatsen loggar du in på [!INCLUDE[prod_short](includes/prod_short.md)] för att slutföra installationen.  

När du installerar en app kanske du måste konfigurera den, till exempel ange ett konto för användning med tillägget **PayPal Payments Standard för [!INCLUDE[prod_short](includes/prod_short.md)]**. Andra appar lägger till fält på en befintlig sida, eller lägger till en ny sida, till exempel.

Om du avinstallerar en app och du sedan ändrar dig kan du installera den på nytt. När du avinstallerar en app bevaras dina data. Om du installerar appen igen är den fortfarande tillgänglig. Det finns vissa appar som krävs och du kan inte avinstallera dem från **Tilläggshantering**.

Några appar ges ut av Microsoft, och andra appar ges ut av [andra företag](ui-extensions-other.md). Alla appar testas innan de görs tillgängliga för dig, men vi rekommenderar att du öppnar länkarna som tillhandahålls med varje tillägg om du vill veta mer om appen innan du väljer att installera den.  

> [!NOTE]  
> Du kan hålla utkik efter nya appar från Microsoft och andra leverantörer på [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## Appar och dataöverföring

Eftersom följande appar kommunicerar med andra tjänster kan de överföra data ur geografin för [!INCLUDE[prod_short](includes/prod_short.md)]-miljön:

* AMC Banking 365 Fundamentals-tillägg
* Image Analyzer
* Prediktion om sen betalning
* PayPal Payments Standard
* Försäljnings- och lagerprognos
* WorldPay Payments Standard

Samma sak gäller för basprogrammet, till exempel följande funktioner:

* Kassaflödesprognos
* Dokumentväxlingstjänst
* Dataverse-anslutningar
* OCR-tjänst
* Online Map
* EU:s momsregistreringsnummer Tjänst

## Anslut företaget

Från och med utgivningscykel 2 2022 kan [!INCLUDE [prod_short](includes/prod_short.md)]-onlinemiljöer lista en eller flera appar på sidorna **Anslutningsappar** och **Bankappar**. Dessa appar kan ansluta ditt företag till externa tjänster, vilket ökar produktiviteten genom att processer automatiseras. Du kan t.ex. ansluta till dina banker och importera banktransaktioner automatiskt. Apparna är enkla att installera och konfigurera direkt från den här sidan. Välj en app för att lära dig mer om funktioner och prissättning.  

Visa listan över föreslagna appar genom att välja åtgärden **Anslutningsappar** på sidan **Tilläggshantering**.  

> [!NOTE]
> Den första personen som öppnar sidan **Anslutningsappar** måste bevilja tillägget tillstånd att ansluta till en extern tjänst. Tillåt anslutningen en gång eller alltid. Om du väljer att blockera anslutningen måste du hitta relevanta appar på AppSource.

Den här externa tjänsten kommer att generera en lista över relevanta appar som baseras på ditt land eller din region

## Rekommenderade appar

Microsofts partner och återförsäljare kan skapa en app som de kan använda för att sammanställa listor över appar som de ofta rekommenderar till sina kunder. Om de gör det och har distribuerat appen till din klientorganisation kommer apparna att vara tillgängliga på sidan **Rekommenderade appar**. Där kan du läsa om varje app och bestämma om du ska installera dem.

> [!NOTE]
> Om du är Microsoft-partner eller återförsäljare och vill tillhandahålla en lista över rekommenderade appar, se [Rekommenderade appar från AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps) i administrationsinnehållet.

## Se även

[Installera och avinstallera appar](ui-extensions-install-uninstall.md)  
[Anpassa Business Central](ui-customizing-overview.md)  
[Business Central-appar från andra leverantörer](ui-extensions-other.md)  
[Skapa tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Aktivera kundbetalningar via betalningstjänster](sales-how-enable-payment-service-extensions.md)  
[Migrera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ställ in tillägget GetAddress.io för postnummer i Storbritannien](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-appar från andra leverantörer](ui-extensions-other.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
