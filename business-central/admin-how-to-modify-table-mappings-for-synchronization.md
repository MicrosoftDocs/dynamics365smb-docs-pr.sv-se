---
title: Ändra tabellmappningar för synkronisering | Microsoft Docs
description: Lär dig ändra den registermappning som används vid synkronisering av data mellan Business Central och Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: de924baa494ae00c09dcb7657c050f2d9ae3ba87
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "940366"
---
# <a name="modify-table-mappings-for-synchronization"></a>Ändra tabellmappningar för synkronisering
En integrationstabellmappning länkar en tabell i [!INCLUDE[d365fin](includes/d365fin_md.md)] till en integrationstabell för [!INCLUDE[crm_md](includes/crm_md.md)]-enheten. För varje enhet i [!INCLUDE[crm_md](includes/crm_md.md)] som du vill synkronisera med motsvarande data i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste det finnas en motsvarande integrationstabellmappning. En integrationstabellmappning innehåller flera inställningar som låter dig styra hur posterna i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen och en [!INCLUDE[crm_md](includes/crm_md.md)]-enhet synkroniseras av motsvarande integrationssynkroniseringsjobb.  

## <a name="filtering-records"></a>Filtrera poster  
 Om du inte vill synkronisera alla poster för en specifik [!INCLUDE[crm_md](includes/crm_md.md)]-enhet eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell, kan du ställa in filter för att begränsa posterna som synkroniseras. Du ställer in filtren på sidan **Tabellmappningar för integrering**.  

#### <a name="to-filter-records-for-synchronization"></a>Om du vill filtrera poster för synkronisering  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Tabellmappningar för integrering** och välj sedan relaterad länk.

2.  För att filtrera [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster anger du fältet **Tabellfilter**.  

3.  För att filtrera [!INCLUDE[crm_md](includes/crm_md.md)]-poster anger du fältet **Filter för integreringstabell**.  

## <a name="creating-new-records"></a>Skapa nya poster  
 Som standard är det bara de poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] som är kopplade som synkroniseras med integrationssynkroniseringsjobben. Du kan ställa in tabellmappningar så att nya poster skapas i målet (till exempel [!INCLUDE[d365fin](includes/d365fin_md.md)]) för varje post i källan (till exempel [!INCLUDE[crm_md](includes/crm_md.md)]) som inte redan är kopplad.  

 Till exempel använder synkroniseringsjobbet SÄLJARE - Dynamics 365 for Sales tabellmappningen SÄLJARE. Synkroniseringsjobbet kopierar informationen [!INCLUDE[crm_md](includes/crm_md.md)]från användarposter till säljarposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om du skapar tabellmappningen för att skapa nya poster, för varje användare i [!INCLUDE[crm_md](includes/crm_md.md)] som inte redan är kopplad till en säljare i [!INCLUDE[d365fin](includes/d365fin_md.md)], skapas en ny säljarpost i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Så här skapar du nya poster under synkroniseringen  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Tabellmappningar för integrering** och välj sedan relaterad länk.

2.  Rensa fältet i tabellmappningposten i fältet **Synka endast kopplade poster**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Använda konfigurationsmallar på tabellmappningar
Du kan tilldela konfigurationsmallar till tabellmappningar som ska användas för nya poster som skapas i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)]. För varje tabellmappning kan du ange en konfigurationsmall som ska användas för nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster och en annan mall för att använda nya [!INCLUDE[crm_md](includes/crm_md.md)]-poster.  

Om du installerar standardsynkroniseringsinstallationen, för det mesta, skapas två konfigurationsmallar automatiskt och används på tabellmappningen för [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder och [!INCLUDE[crm_md](includes/crm_md.md)]-konton: **CRMCUST** och **CRMACCOUNT**.  

-   **CRMCUST** används för att skapa och synkronisera nya kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)] baserat på ett konto i [!INCLUDE[crm_md](includes/crm_md.md)].  

     Den här mallen skapas, genom att kopiera en befintlig konfigurationsmall för kunder i programmet. **CRMCUST** skapas endast om det finns en befintlig konfigurationsmall och fältet **Valutakod** i mallen är tomt. Om ett fält i konfigurationsmallen innehåller ett värde, ska värdet användas i stället för värdet i det mappade fältet i [!INCLUDE[crm_md](includes/crm_md.md)]-kontot. Till exempel, om fältet **Land/region** i ett konto i [!INCLUDE[crm_md](includes/crm_md.md)] innehåller *USA* och fältet **Land/region** i konfigurationsmallen är *GB* används *GB* som **Land/region** för kunden i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CRMACCOUNT** skapar och synkroniserar nya konton i [!INCLUDE[crm_md](includes/crm_md.md)] baserat på ett konto i [!INCLUDE [d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Ange konfigurationsmallar på en tabellmappning  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Tabellmappningar för integrering** och välj sedan relaterad länk.

2.  I tabellmappningposten i listan anger du fältet **Mallkod för tabellkonfig.** till konfigurationsmallen som ska användas för nya poster i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Ange fältet **Mallkod för int.tabellkonfig.** till konfigurationsmallen som ska användas för nya poster i [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Se även  
[Om integrering Dynamics 365 Business Central med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synkroniserar Business Central och Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)   
[Schemalägg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
