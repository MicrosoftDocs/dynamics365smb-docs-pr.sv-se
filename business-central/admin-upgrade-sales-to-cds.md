---
title: Uppgradera en integrering med Dynamics 365 Sales | Microsoft-dokument
description: Lär dig hur du hämtar Dynamics 365 Business Central redo att integreras med Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 95098397bd9554be6c993b6107963eba9a99c067
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196898"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Uppgradera en integrering med Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] integreras också med [!INCLUDE[d365fin](includes/cds_long_md.md)], vilket gör det enkelt att ansluta och synkronisera data med andra Dynamics 365-program, till exempel [!INCLUDE[crm_md](includes/crm_md.md)] eller till och med appar som du själv skapar. Om du integrerar för första gången rekommenderar vi att du gör det via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Mer information finns i [Integrera med Common Data Service](admin-common-data-service.md).

Om du redan har integrerat [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du fortsätta att synkronisera data med hjälp av dina inställningar. Om du uppgraderar [!INCLUDE[d365fin](includes/d365fin_md.md)] eller stänger av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen måste du emellertid ansluta dig via [!INCLUDE[d365fin](includes/cds_long_md.md)] för att aktivera den igen. 

> [!NOTE]
> När du återansluter via [!INCLUDE[d365fin](includes/cds_long_md.md)] används standardinställningarna för synkroniseringen, och eventuella konfigurationsinställningar skrivs över. Till exempel tillämpas standardmappningarna för tabeller.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Så här uppgraderar du anslutningen till att använda Common Data Service
1. Öppna sidan **Konfigurera anslutning för Microsoft Dynamics 365**, välj brytaren **Aktivera** för att stänga av den befintliga anslutningen till [!INCLUDE[crm_md](includes/crm_md.md)].
2. Öppna sidan **Konfiguration av anslutning till Common Data Service** och välj brytaren **Aktivera** för att slå på anslutningen.
3. När du har aktiverat CDS-anslutningen distribueras anslutningen till basintegrering med CDS för Business Central till Common Data Service.
4. På inställningssidan för Microsoft Dynamics 365-anslutningar väljer du brytaren Aktivera för att slå på anslutningen till [!INCLUDE[crm_md](includes/crm_md.md)].
5. När du har aktiverat Sales-anslutningen distribueras anslutningen till basintegrering med CDS för Business Central till Sales. Detta möjliggör integrering med enheter som är specifika för [!INCLUDE[crm_md](includes/crm_md.md)], t.ex. försäljningsorder, offerter och fakturor.
6. På sidan **Anslutningsinställningar för Sales** väljer du **Använd standardinställningar för synkronisering** om du vill initiera tabellmappningarna för [!INCLUDE[crm_md](includes/crm_md.md)].
7. Välj **Omdistribuera integreringslösning** för att installera och konfigurera den uppgraderade integreringslösningen för Business Central.

## <a name="see-also"></a>Se även
[Integrering med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrera med Common Data Service](admin-common-data-service.md)