---
title: Integrera med Dynamics 365 for Sales| Microsoft Docs
description: Lär dig hur du hämtar Dynamics 365 Business Central redo att integreras med Dynamics 365 for Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: bbe5041f853af9d58149d446627b0b21fa0e0f12
ms.sourcegitcommit: 92c7b6c5f0a5d8becbef106ab85258906765bc3e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540252"
---
# <a name="integrating-with-dynamics-365-for-sales"></a>Integrera med Dynamics 365 for Sales
Rollen säljare betraktas ofta som en de mest utåtriktade jobben i ett företag. Men kan det vara användbart för säljare att kunna se inuti verksamheten och se vad som händer på serverdelen. Genom att integrera [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] kan du ge säljare denna information genom att visa informationen i [!INCLUDE[d365fin](includes/d365fin_md.md)] medan de arbetar i [!INCLUDE[crm_md](includes/crm_md.md)]. Till exempel när du förbereder en försäljningsoffert kan det vara bra att veta om det finns tillräckligt mycket lager för att uppfylla ordern. Mer information finns i [Använda Dynamics 365 for Sales från Business Central](marketing-integrate-dynamicscrm.md).

> [!Note]
> Här beskrivs hur du integrerar onlineversioner av [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)].

<!--## Software Requirements
You must have an Office 365 subscription, and both [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] must be part of the same organization.  -->

## <a name="overview-of-the-integration-process"></a>Översikt över integrationsprocessen
Följande steg ger en översikt över hur du integrerar [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Dessa uppgifter kräver säkerhetsrollen **Systemadministratör** i [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. I Office 365 administratörscenter anger du ett konto att ansluta till och synkronisera data med [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Ställa in integration med Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

2. Tilldela licenser för [!INCLUDE[crm_md](includes/crm_md.md)] till de [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare som ska använda de inbyggda programmen.

3. Ställ in en anslutning till [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Ställa in en anslutning till Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. Valfritt: Koppla [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)]-poster. Mer information finns i [Koppla och synkronisera posterna manuellt](admin-how-to-couple-and-synchronize-records-manually.md).

5. Synkronisera data mellan apparna. Mer information finns i [Synkronisera Business Central och Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md).  

## <a name="about-the-business-central-integration-solution"></a>Om Business Central integrerad affärslösning
Lösningen låter användare visa information i [!INCLUDE[d365fin](includes/d365fin_md.md)] medan de arbetar i [!INCLUDE[crm_md](includes/crm_md.md)]. Det kan till exempel ge insyn i kundstatistik, låta användare koppla och visa poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] från [!INCLUDE[crm_md](includes/crm_md.md)] och gör det möjligt att se om det finns produkter i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Som standard kommer inställningen av Dynamics 365 for Sales assisterad inställningsguide för anslutning att importera [!INCLUDE[d365fin](includes/d365fin_md.md)]-integreringslösningen. För att göra detta använder inställningsguiden ett administratörsanvändarkonto. Kontot måste även vara en giltig användare i [!INCLUDE[crm_md](includes/crm_md.md)] med följande säkerhetsrollerna:

* Systemadministratör  
* Lösningsanpassare  

Mer information finns i [ställa in konton för att integrera med Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md), [skapa användare i Microsoft Dynamics 365 (online) och tilldela säkerhetsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles.md) och [hantera användare och behörigheter](ui-how-users-permissions.md).  

Det här kontot används bara en gång vid installationen. När lösningen har importerats till [!INCLUDE[d365fin](includes/d365fin_md.md)], behövs inte längre kontot. Integrationen fortsätter att använda användarkontot som har skapats särskilt för integrering.

Förutom att anpassa [!INCLUDE[crm_md](includes/crm_md.md)], [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer integreringslösningen även att skapa följande roller i [!INCLUDE[crm_md](includes/crm_md.md)] för integreringen:

* **Integrationsadministratören** - tillåter användare att hantera anslutningen mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)]. Vanligtvis tilldelas den bara användarkontot för synkronisering.  
* **Integrationsanvändare** - tillåter användare att komma åt synkroniserade data. Tilldelas normalt till användarkontot för synkronisering och alla användare som behöver visa eller komma åt synkroniserade data.
* **Produkttillgänglighetsanvändare** - tillåter att användare frågar om produkttillgänlighet i [!INCLUDE[d365fin](includes/d365fin_md.md)] från [!INCLUDE[crm_md](includes/crm_md.md)].

I slutet av installationsguiden [!INCLUDE[d365fin](includes/d365fin_md.md)] uppmanas du att koppla säljare till användare i [!INCLUDE[crm_md](includes/crm_md.md)]. Poster i [!INCLUDE[crm_md](includes/crm_md.md)] har vanligtvis en ägare (användare) som tilldelats dem, och om koppling mellan användare i [!INCLUDE[crm_md](includes/crm_md.md)] och säljare i [!INCLUDE[d365fin](includes/d365fin_md.md)] inte finns kommer synkroniseringen att misslyckas. Du kan också göra det senare med hjälp av åtgärden **Koppla säljare** på sidan **Microsoft Dynamics 365 anslutningsinställningar**.

## <a name="see-also"></a>Se även  
[Ställa in konton för integrering med Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Göra en anslutning till Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md)
[Synkronisera Business Central och Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)
