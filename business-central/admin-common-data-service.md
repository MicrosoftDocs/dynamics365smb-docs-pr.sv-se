---
title: Använda Common Data Service
description: Introduktion till Common Data Service och dess komponenter.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 06/30/2020
ms.openlocfilehash: 278797e8a1647fff8fd607cf075657c960004e65
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529394"
---
# <a name="integrating-with-common-data-service"></a>Integrera med Common Data Service

I företagsappar används ofta data från mer än en källa. [!INCLUDE[d365fin](includes/cds_long_md.md)] kombinerar data till en enda logikuppsättning som gör det enklare att ansluta andra Dynamics 365-program, t.ex. [!INCLUDE[crm_md](includes/crm_md.md)] eller ett eget program som bygger på [!INCLUDE[d365fin](includes/cds_long_md.md)], till [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Mer information om [!INCLUDE[d365fin](includes/cds_long_md.md)] finns i [Vad är Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

Följande steg ger en översikt över hur du integrerar [!INCLUDE[d365fin](includes/cds_long_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Dessa uppgifter kräver säkerhetsrollen **Systemadministratör** i [!INCLUDE[d365fin](includes/cds_long_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Tilldela licenser för [!INCLUDE[d365fin](includes/cds_long_md.md)] till de [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare som ska använda de inbyggda programmen.

2. Ställ in en anslutning till [!INCLUDE[d365fin](includes/cds_long_md.md)]. Mer information finns i [Anslut till Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synkronisera data mellan apparna. Mer information finns i [Synkronisera Business Central och Common Data Service](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-d365fin"></a>Komma igång med [!INCLUDE[d365fin](includes/cds_long_md.md)]
För att komma igång med [!INCLUDE[d365fin](includes/cds_long_md.md)] behöver du ett Microsoft Power Apps-konto. Om du inte redan har ett Power Apps-konto kan du få ett gratis genom att besöka [powerapps.com](https://web.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) och välja länken **Kom igång gratis**. Mer information om hur du kommer igång med [!INCLUDE[d365fin](includes/cds_long_md.md)] finns i avsnittet [Komma igång med Common Data Service](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/)-modulen från Microsft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Dubbelriktad eller enkelriktad datasynkronisering
Beroende på ditt företags behov kan du ställa in integreringen för att synkronisera data antingen till eller från en Dynamics 365-affärsapp till en annan, eller i båda riktningarna i närapå realtid via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Om du t.ex. integrerar [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] med hjälp av [!INCLUDE[d365fin](includes/cds_long_md.md)] kan en säljare skapa en försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] och ordern synkroniseras till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Från [!INCLUDE[crm_md](includes/crm_md.md)] kan säljaren å andra sidan se information från [!INCLUDE[d365fin](includes/d365fin_md.md)] som berör tillgängligheten för artikeln på ordern. 

## <a name="standard-and-custom-entities"></a>Standard- och anpassade eenheter
[!INCLUDE[d365fin](includes/cds_long_md.md)] lagrar data säkert i en uppsättning eenheter, som är grupper av transaktioner som påminner om hur en tabell lagrar data i en databas. [!INCLUDE[d365fin](includes/cds_long_md.md)] innehåller en grundläggande uppsättning standardeenheter som täcker typiska scenarier, men du kan också skapa egna eenheter som är specifika för organisationen. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du visa standardenheter och anpassade entiteter som synkroniseras på sidan Tabellmappningar för integrering.

## <a name="about-the-base-cds-integration-solution"></a>Om lösningen för basintegrering med CDS

Lösningen för basintegrering med CDS är en nyckelkomponent i integreringen. Lösningen lägger till de roller och åtkomstnivåer som krävs i användarkontona för integreringen, och skapar entiteter som behövs för att mappa [!INCLUDE[d365fin](includes/d365fin_md.md)]-företaget till affärsenheten i [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

Den assisterade konfigurationen **Ställ in [!INCLUDE[d365fin](includes/cds_long_md.md)]-anslutning** kommer att importera lösningen som standard. För att göra detta använder inställningsguiden ett administratörsanvändarkonto som du anger. Detta konto måste även vara en giltig användare i [!INCLUDE[d365fin](includes/cds_long_md.md)] med följande säkerhetsroll:

* Systemadministratör  

Mer information finns i [Ställa in användarkonton för integrering med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) och [Skapa användare i Microsoft Dynamics 365 (online) och tilldela säkerhetsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Administratörskontot används endast en gång under installationen på grund av de konfigurationsändringar som bas-CDS-lösningen gör i [!INCLUDE[d365fin](includes/cds_long_md.md)]. När lösningen har importerats behövs inte kontot längre. Integreringen fortsätter att använda användarkontot som har skapats automatiskt särskilt för integrering.

Förutom att anpassa [!INCLUDE[d365fin](includes/cds_long_md.md)]  kommer integreringslösningen även att skapa följande roller i [!INCLUDE[d365fin](includes/cds_long_md.md)] för integreringen:

* **Integreringsadministratören** - tillåter användare att hantera anslutningen mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[d365fin](includes/cds_long_md.md)]. Vanligtvis tilldelas detta bara till det automatiskt skapade användarkontot för synkronisering.  
* **Integreringsanvändare** - tillåter användare att komma åt synkroniserade data. Detta tilldelas normalt till det automatiskt skapade användarkontot för synkronisering och andra användare som behöver visa eller komma åt synkroniserade data.

Mer information om varje roll, t.ex. behörigheter och åtkomstnivåer finns i [Konfigurera användarkonton för integrering med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Under anslutningsinstallationen skapas integreringstabellmappningar som behövs för att synkronisera data. Enheter i Common Data Service är mappade till tabeller och tabellfält i Business Central via integreringstabeller. Mer information finns i [Standardinställd enhetsmappning för synkronisering](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).

## <a name="see-also"></a>Se även
[Modeller för dataägarskap](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Common Data Service](docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration) -->



