---
title: Integrera med Microsoft Dataverse via datasynkronisering
description: Introduktion till hur du integrerar och använder Microsoft Dataverse och dess komponenter för att ansluta till andra Dynamics 365-program.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/08/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="integrate-with-microsoft-dataverse-via-data-sync"></a>Integrera med Microsoft Dataverse via datasynkronisering

I företagsappar används ofta data från mer än en källa. [!INCLUDE[prod_short](includes/cds_long_md.md)] data till en enda logikuppsättning som gör det enklare att ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till andra Dynamics 365-progeam. Till exempel [!INCLUDE[crm_md](includes/crm_md.md)] eller ett eget program skapat med [!INCLUDE[prod_short](includes/cds_long_md.md)]. För att lära dig om [!INCLUDE[prod_short](includes/cds_long_md.md)], gå till [Vad är Dataverse?](/powerapps/maker/common-data-service/data-platform-intro).

Följande steg ger en översikt över hur du integrerar [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Dessa uppgifter kräver säkerhetsrollen **Systemadministratör** i [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Tilldela licenser för [!INCLUDE[prod_short](includes/cds_long_md.md)] till de [!INCLUDE[prod_short](includes/prod_short.md)]-användare som ska använda de inbyggda programmen.

2. Ställ in en anslutning till [!INCLUDE[prod_short](includes/cds_long_md.md)]. Mer information finns i [Anslut till Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synkronisera data mellan apparna. Mer information finns i [Synkronisera Business Central och Dataverse](admin-synchronizing-business-central-and-sales.md). 

## <a name="get-started-with-"></a>Kom igång med [!INCLUDE[prod_short](includes/cds_long_md.md)]

För att komma igång med [!INCLUDE[prod_short](includes/cds_long_md.md)] behöver du ett Microsoft Power Apps-konto. Om du inte redan har ett Power Apps-konto kan du få ett gratis genom att besöka [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) och välja länken **Kom igång gratis**. Mer information om hur du kommer igång med [!INCLUDE[prod_short](includes/cds_long_md.md)] finns i avsnittet [Komma igång med Dataverse](/training/modules/get-started-with-powerapps-common-data-service/)-modulen från Microsoft utbildning.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Dubbelriktad eller enkelriktad datasynkronisering

Du kan synkronisera data antingen till eller från en Dynamics 365-affärsapp till en annan, eller i båda riktningarna i närapå realtid via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Om du t.ex. integrerar [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[crm_md](includes/crm_md.md)], kan en säljare skapa en försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] och ordern synkroniseras till [!INCLUDE[prod_short](includes/prod_short.md)]. Artiklar, från [!INCLUDE[crm_md](includes/crm_md.md)], kan säljaren som berör tillgängligheten för artikeln på ordern i [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="standard-and-custom-entities"></a>Standard- och anpassade enheter

[!INCLUDE[prod_short](includes/cds_long_md.md)] lagrar data säkert i en uppsättning tabeller, som är grupper av transaktioner som påminner om hur en tabell lagrar data i en databas. [!INCLUDE[prod_short](includes/cds_long_md.md)] innehåller en grundläggande uppsättning tabeller som täcker typiska scenarier, men du kan också skapa egna tabeller som är specifika för organisationen. I [!INCLUDE[prod_short](includes/prod_short.md)] kan du visa standard- och anpassade tabeller som synkroniseras på sidan Registermappningar för integrering.

## <a name="about-the-business-central-base-integration-solution"></a>Om basintegreringslösningen i Business Central

Lösningen för basintegrering är en nyckelkomponent i integreringen. Lösningen lägger till de roller och åtkomstnivåer som krävs för integreringen i användarkontona, och skapar de tabeller som behövs för att mappa [!INCLUDE[prod_short](includes/prod_short.md)]-företaget till affärsenheten i [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Den assisterade konfigurationen **Ställ in [!INCLUDE[prod_short](includes/cds_long_md.md)]-anslutning** kommer att importera lösningen som standard. För att göra detta använder inställningsguiden ett administratörsanvändarkonto som du anger. Detta konto måste även vara en giltig användare i [!INCLUDE[prod_short](includes/cds_long_md.md)] med säkerhetsrollen **Systemadministratör**.  

Mer information om användarkonton finns i följande artiklar:

* [Ställa in konton för integrering med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) 
* [Skapa användare i Microsoft Dynamics 365 (online) och tilldela säkerhetsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Administratörskontot används endast en gång under installationen av de konfigurationsändringar som basintegreringslösningen gör i [!INCLUDE[prod_short](includes/cds_long_md.md)]. När lösningen har importerats behövs inte kontot längre. Integreringen fortsätter att använda användarkontot som har skapats automatiskt särskilt för integrering.

Förutom att anpassa [!INCLUDE [cds_long_md](includes/cds_long_md.md)]  kommer integreringslösningen även att skapa en säkerhetsroll i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] för integreringen:

* **Business Central Dataverse-integrering** – Tillåter dig att hantera anslutningen mellan [!INCLUDE [prod_short](includes/prod_short.md)] och [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Vanligtvis tilldelas rollen bara till det automatiskt skapade användarkontot för synkronisering. För att lära dig mer om den här rollen, gå till [Konfigurera användarkonton för integration med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

När du ställer in anslutningen skapar du de integrationens tabellmappningar som du behöver för att synkronisera data. Enheter i [!INCLUDE[prod_short](includes/cds_long_md.md)] är mappade till tabeller och tabellfält i [!INCLUDE [prod_short](includes/prod_short.md)] via integreringstabeller. Om du vill veta mer om mappningar går du till [Standardenhetsmappning för synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="handle-differences-in-local-and-base-transaction-currencies"></a>Hantera skillnader i lokala och grundläggande transaktionsvalutor

Du kan ansluta till en [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljö med en annan basvaluta än den lokala valutan i [!INCLUDE[prod_short](includes/prod_short.md)]. Du gör anslutningen i [!INCLUDE[prod_short](includes/prod_short.md)] på sidan **Dataverse-anslutningsinställningar** eller med hjälp av **Konfigurera anslutning till Dataverse** assisterad inställningsguide.

För att kunna ansluta måste du kontrollera att inställningen bastransaktionens valuta i [!INCLUDE[prod_short](includes/cds_long_md.md)] har den valuta som har angetts på sidan **Valutor** i [!INCLUDE [prod_short](includes/prod_short.md)] och minst en valutakurs har angetts för valutan på sidan **Valutakurser**.

Här är ett exempel. Du ansluter [!INCLUDE[prod_short](includes/cds_long_md.md)] med euro (EUR) angiven som lokal valuta på sidan **Redovisningsinställningar** till en [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljö med en bastransaktionsvaluta inställd på amerikanska dollar (USD). Du måste ha USD på sidan **Valutor** i [!INCLUDE [prod_short](includes/prod_short.md)] och rätt valutakurs. 

När du aktiverar anslutningen till [!INCLUDE[prod_short](includes/cds_long_md.md)], [!INCLUDE [prod_short](includes/prod_short.md)] lägger det till lokal valuta till entiteten **Valuta** i [!INCLUDE[prod_short](includes/cds_long_md.md)] med valutakursen från fältet **Valutafaktor** på **Valutakurser**.

Synkronisering med valuta är enkelriktad, från [!INCLUDE [prod_short](includes/prod_short.md)] till [!INKLUDERA [!INCLUDE[prod_short](includes/cds_long_md.md)], belopp konverteras och synkroniseras enligt följande:

* Belopp i [!INCLUDE[prod_short](includes/cds_long_md.md)] basvalutan konverteras till [!INCLUDE [prod_short](includes/prod_short.md)] lokala valutan baserat på den senaste valutakursen som synkroniseras från [!INCLUDE [prod_short](includes/prod_short.md)].
* Belopp i [!INCLUDE [prod_short](includes/prod_short.md)] lokal valuta synkroniseras med [!INCLUDE [prod_short](includes/prod_short.md)] lokala valutan i någon av de andra valutorna i [!INCLUDE[prod_short](includes/cds_long_md.md)].

## <a name="what-happens-when-you-copy-a-company"></a>Vad händer när du kopierar ett företag?

Du kan säkert kopiera företag som integrerar med [!INCLUDE[prod_short](includes/cds_long_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)]. Kopiera företag hjälper till att minska risken för inkonsekventa data och kan spara värdefull tid. Mer information om kopiera företag finns i [Kopiera ett företag](about-new-company.md#copy-a-company).

[!INCLUDE [dataverse-copy-company](includes/dataverse-copy-company.md)]

## <a name="see-also"></a>Se även

[Modeller för dataägarskap](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
