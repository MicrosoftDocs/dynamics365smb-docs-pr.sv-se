---
title: Använda Microsoft Dataverse
description: Introduktion till Microsoft Dataverse och dess komponenter.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 1d740cf645739e89dddc9173583eb5fa639f6be6
ms.sourcegitcommit: edac6cbb8b19ac426f8dcbc83f0f9e308fb0d45d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/29/2020
ms.locfileid: "4817110"
---
# <a name="integrating-with-microsoft-dataverse"></a>Integrera med Microsoft Dataverse
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

I företagsappar används ofta data från mer än en källa. [!INCLUDE[prod_short](includes/cds_long_md.md)] kombinerar data till en enda logikuppsättning som gör det enklare att ansluta andra Dynamics 365-program, t.ex. [!INCLUDE[crm_md](includes/crm_md.md)] eller ett eget program som bygger på [!INCLUDE[prod_short](includes/cds_long_md.md)], till [!INCLUDE[prod_short_md](includes/prod_short.md)]. Mer information om [!INCLUDE[prod_short](includes/cds_long_md.md)] finns i [Vad är Dataverse?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

Följande steg ger en översikt över hur du integrerar [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Dessa uppgifter kräver säkerhetsrollen **Systemadministratör** i [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Tilldela licenser för [!INCLUDE[prod_short](includes/cds_long_md.md)] till de [!INCLUDE[prod_short](includes/prod_short.md)]-användare som ska använda de inbyggda programmen.

2. Ställ in en anslutning till [!INCLUDE[prod_short](includes/cds_long_md.md)]. Mer information finns i [Anslut till Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synkronisera data mellan apparna. Mer information finns i [Synkronisera Business Central och Dataverse](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-prod_short"></a>Komma igång med [!INCLUDE[prod_short](includes/cds_long_md.md)]
För att komma igång med [!INCLUDE[prod_short](includes/cds_long_md.md)] behöver du ett Microsoft Power Apps-konto. Om du inte redan har ett Power Apps-konto kan du få ett gratis genom att besöka [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) och välja länken **Kom igång gratis**. För mer information om hur du kommer igång med [!INCLUDE[prod_short](includes/cds_long_md.md)], se modulen [Komma igång med Dataverse](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) från Microsoft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Dubbelriktad eller enkelriktad datasynkronisering
Beroende på ditt företags behov kan du ställa in integreringen för att synkronisera data antingen till eller från en Dynamics 365-affärsapp till en annan, eller i båda riktningarna i närapå realtid via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Om du t.ex. integrerar [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] med hjälp av [!INCLUDE[prod_short](includes/cds_long_md.md)] kan en säljare skapa en försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] och ordern synkroniseras till [!INCLUDE[prod_short](includes/prod_short.md)]. Från [!INCLUDE[crm_md](includes/crm_md.md)] kan säljaren å andra sidan se information från [!INCLUDE[prod_short](includes/prod_short.md)] som berör tillgängligheten för artikeln på ordern. 

## <a name="standard-and-custom-entities"></a>Standard- och anpassade eenheter
[!INCLUDE[prod_short](includes/cds_long_md.md)] lagrar data säkert i en uppsättning tabeller, som är grupper av transaktioner som påminner om hur en tabell lagrar data i en databas. [!INCLUDE[prod_short](includes/cds_long_md.md)] innehåller en grundläggande uppsättning tabeller som täcker typiska scenarier, men du kan också skapa egna tabeller som är specifika för organisationen. I [!INCLUDE[prod_short](includes/prod_short.md)] kan du visa standard- och anpassade tabeller som synkroniseras på sidan Registermappningar för integrering.

## <a name="about-the-business-central-base-integration-solution"></a>Om basintegreringslösningen i Business Central

Lösningen för basintegrering är en nyckelkomponent i integreringen. Lösningen lägger till de roller och åtkomstnivåer som krävs för integreringen i användarkontona, och skapar de tabeller som behövs för att mappa [!INCLUDE[prod_short](includes/prod_short.md)]-företaget till affärsenheten i [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Den assisterade konfigurationen **Ställ in [!INCLUDE[prod_short](includes/cds_long_md.md)]-anslutning** kommer att importera lösningen som standard. För att göra detta använder inställningsguiden ett administratörsanvändarkonto som du anger. Detta konto måste även vara en giltig användare i [!INCLUDE[prod_short](includes/cds_long_md.md)] med följande säkerhetsroll:

* Systemadministratör  

Mer information finns i [Ställa in användarkonton för integrering med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) och [Skapa användare i Microsoft Dynamics 365 (online) och tilldela säkerhetsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Administratörskontot används endast en gång under installationen av de konfigurationsändringar som basintegreringslösningen gör i [!INCLUDE[prod_short](includes/cds_long_md.md)]. När lösningen har importerats behövs inte kontot längre. Integreringen fortsätter att använda användarkontot som har skapats automatiskt särskilt för integrering.

Förutom att anpassa [!INCLUDE[prod_short](includes/cds_long_md.md)]  kommer integreringslösningen även att skapa följande roller i [!INCLUDE[prod_short](includes/cds_long_md.md)] för integreringen:

* **Integreringsadministratören** – tillåter användare att hantera anslutningen mellan [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)]. Vanligtvis tilldelas detta bara till det automatiskt skapade användarkontot för synkronisering.  
* **Integreringsanvändare** – tillåter användare att komma åt synkroniserade data. Detta tilldelas normalt till det automatiskt skapade användarkontot för synkronisering och andra användare som behöver visa eller komma åt synkroniserade data.

Mer information om varje roll, t.ex. behörigheter och åtkomstnivåer finns i [Konfigurera användarkonton för integrering med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Under anslutningsinstallationen skapas integreringsregistermappningar som behövs för att synkronisera data. Enheter i [!INCLUDE[prod_short](includes/cds_long_md.md)] är mappade till tabeller och tabellfält i Business Central via integreringstabeller. Mer information finns i [Standardinställd enhetsmappning för synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="see-also"></a>Se även
[Modeller för dataägarskap](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->





[!INCLUDE[footer-include](includes/footer-banner.md)]