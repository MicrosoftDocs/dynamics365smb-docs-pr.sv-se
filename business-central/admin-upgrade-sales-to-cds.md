---
title: Uppgradera en integrering med Dynamics 365 Sales
description: Lär dig hur du flyttar Dynamics 365 Business Central-integrationen med Dynamics 365 Sales till den senaste versionen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 4e3b79d6245a0f1b8277c94faa58c24edc66662e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777022"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Uppgradera en integrering med Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] integreras också med [!INCLUDE[prod_short](includes/cds_long_md.md)], vilket gör det enkelt att ansluta och synkronisera data med andra Dynamics 365-program, till exempel [!INCLUDE[crm_md](includes/crm_md.md)] eller till och med appar som du själv skapar. Om du integrerar för första gången rekommenderar vi att du gör det via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Mer information finns i [Integrera med Dataverse](admin-common-data-service.md).

Om du redan har integrerat [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)] kan du fortsätta att synkronisera data med hjälp av dina inställningar. Om du uppgraderar [!INCLUDE[prod_short](includes/prod_short.md)] eller stänger av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen måste du emellertid ansluta dig via [!INCLUDE[prod_short](includes/cds_long_md.md)] för att aktivera den igen. 

> [!NOTE]
> När du återansluter via [!INCLUDE[prod_short](includes/cds_long_md.md)] används standardinställningarna för synkroniseringen, och eventuella konfigurationsinställningar skrivs över. Till exempel tillämpas standardmappningarna för tabeller.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>Så här uppgraderar du anslutningen till att använda Dataverse
1. Öppna sidan **Anslutningskonfiguration för Microsoft Dynamics 365** och stäng av brytaren **Aktiverad** för att koppla ifrån [!INCLUDE[crm_md](includes/crm_md.md)].
2. Öppna sidan **Anslutningskonfiguration för Dataverse** och välj brytaren **Aktiverad** för att aktivera anslutningen till [!INCLUDE[prod_short](includes/cds_long_md.md)].
  
   > [!NOTE]
   > När du har aktiverat anslutningen distribueras integreringslösningen till Business Central till Dataverse.
3. Välj **Omdistribuera integreringslösning** för att ominstallera integreringslösningen för Business Central.
4. På sidan **Anslutningskonfiguration för Microsoft Dynamics 365** aktiverar du reglaget **Aktiverad** för att återansluta till [!INCLUDE[crm_md](includes/crm_md.md)].
  
   > [!NOTE]
   > När du har aktiverat anslutningen distribueras integreringslösningen till Business Central till [!INCLUDE[prod_short](includes/prod_short.md)]. Detta möjliggör integrering med tabeller som är specifika för [!INCLUDE[crm_md](includes/crm_md.md)], t. ex. försäljningsorder, offerter och fakturor.
5. Välj **Omdistribuera integreringslösning** för att ominstallera integreringslösningen för Business Central.
6. På sidan **Anslutningsinställningar för Sales** väljer du **Använd standardinställningar för synkronisering** om du vill initiera registermappningarna för [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Se även
[Integrering med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrera med Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]