---
title: Uppgradera en integrering med Dynamics 365 Sales
description: Detta ämne lär dig hur du flyttar Dynamics 365 Business Central-integrationen med Dynamics 365 Sales till den senaste versionen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 06/14/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Uppgradera en integrering med Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] integreras också med [!INCLUDE[prod_short](includes/cds_long_md.md)], vilket gör det enkelt att ansluta och synkronisera data med andra Dynamics 365-program, till exempel [!INCLUDE[crm_md](includes/crm_md.md)] eller till och med appar som du själv skapar. Om du integrerar för första gången rekommenderar vi att du gör det via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Mer information finns i [Integrera med Dataverse](admin-common-data-service.md).

Om du redan har integrerat [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)] kan du fortsätta att synkronisera data med hjälp av dina inställningar. Om du uppgraderar [!INCLUDE[prod_short](includes/prod_short.md)] eller stänger av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen måste du emellertid ansluta dig via [!INCLUDE[prod_short](includes/cds_long_md.md)] för att aktivera den igen. 

> [!NOTE]
> När du återansluter via [!INCLUDE[prod_short](includes/cds_long_md.md)] används standardinställningarna för synkroniseringen, och eventuella konfigurationsinställningar skrivs över. Till exempel tillämpas standardmappningarna för tabeller.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>Så här uppgraderar du anslutningen till att använda Dataverse
1. Öppna sidan **Konfiguration av anslutning till Microsoft Dynamics 365** stänger du av reglaget **Aktiverad**. Stäng sedan sidan att koppla från [!INCLUDE[crm_md](includes/crm_md.md)].
2. Öppna sidan **Dataverse anslutningsinställningar** och välj **Ägarskapsmodlel**, välj **Person**. Välj sedan växlingen **Aktivera** för att aktivera anslutningen till [!INCLUDE[prod_short](includes/cds_long_md.md)].
  
   > [!NOTE]
   > När du har aktiverat anslutningen distribueras integreringslösningen till Business Central till Dataverse.
4. På sidan **Konfiguration av anslutning till Microsoft Dynamics 365**, välj **Omdistribuera integreringslösning** för att installera om integreringslösningen för Business Central.
5. Aktivera växlingen **Aktiverad** för att ansluta igen till [!INCLUDE[crm_md](includes/crm_md.md)].
  
   > [!NOTE]
   > När du har aktiverat anslutningen distribueras integreringslösningen till Business Central till [!INCLUDE[prod_short](includes/prod_short.md)]. Detta möjliggör integrering med tabeller som är specifika för [!INCLUDE[crm_md](includes/crm_md.md)], t. ex. försäljningsorder, offerter och fakturor.
6. På sidan **Anslutningsinställningar för Sales** väljer du **Använd standardinställningar för synkronisering** om du vill initiera registermappningarna för [!INCLUDE[crm_md](includes/crm_md.md)].

   > [!IMPORTANT]
   > När du använder åtgärden **Använd standardsynkronisering** tillämpas standardmappningar för integreringstabell. Alla anpassade mappningar skrivs över. Om du har anpassade mappningar som du vill behålla rekommenderar vi att du exporterar dem till Excel eller pratar med din Microsoft-partner om andra sätt att behålla dina egna mappningar.    

## <a name="see-also"></a>Se även
[Integrering med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrera med Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
