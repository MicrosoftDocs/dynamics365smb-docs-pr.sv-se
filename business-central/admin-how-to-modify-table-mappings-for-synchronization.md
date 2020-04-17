---
title: Mappa registren och fälten som ska synkroniseras | Microsoft docs
description: Läs om hur du kartlägger tabeller och fält för synkronisering av data mellan Business Central och Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: d8377e5042ac647386e1b3b02e1f97d2e14eb3ae
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196525"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Mappa register och fält som ska synkroniseras
Grunden för att synkronisera data i [!INCLUDE[d365fin](includes/d365fin_md.md)] med data i [!INCLUDE[d365fin](includes/cds_long_md.md)] är att mappa registren och fälten som innehåller data med varandra. Mappning sker via integreringsregister. 

## <a name="mapping-integration-tables"></a>Integreringsregister för mappning
En integreringsregister är en register i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen som representerar en enhet, exempelvis konto, i [!INCLUDE[d365fin](includes/cds_long_md.md)]. Integreringsregisteren innehåller fält som motsvarar fält i registeren för enheten [!INCLUDE[d365fin](includes/cds_long_md.md)]. Till exempel ansluter integreringsregisteren Konto till enheten Konton i [!INCLUDE[d365fin](includes/cds_long_md.md)]. För varje enhet i [!INCLUDE[d365fin](includes/cds_long_md.md)] som du vill synkronisera med data i [!INCLUDE[d365fin](includes/d365fin_md.md)] måste det finnas en mappning för integreringsregister.

När du skapar anslutningen mellan programmen ställer [!INCLUDE[d365fin](includes/d365fin_md.md)] in vissa standardmappningar för register och fält. Om du vill kan du ändra registermappningarna. Mer information finns i [Standardinställd enhetsmappning för synkronisering](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization). Om du har ändrat standardmappningarna och vill återställa ändringarna går du till sidan **Anslutningsinställningar för [!INCLUDE[d365fin](includes/cds_long_md.md)]** och väljer **Använd standardinställningar för synkronisering**.

> [!Note]
> Om du använder en lokal version av [!INCLUDE[d365fin](includes/d365fin_md.md)] lagras mappningarna för integreringsregister i registeren 5335 för registermappningar för integrering, och kan visas och ändras från sidan 5335 för registermappningar för integrering. Komplexa mappningar och synkroniseringsregler definieras i codeunit 5341. 

### <a name="synchronization-rules"></a>Synkroniseringsregler
En mappning av integreringsregister innehåller också regler som styr hur synkroniseringsjobb för integrering synkroniserar poster i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-register och en enhet i [!INCLUDE[d365fin](includes/cds_long_md.md)]. <!--For examples of rules for an integration with Sales, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules). need to verify link -->

## <a name="mapping-integration-fields"></a>Mappa integreringsfält
Att mappa register är bara det första steget. Du måste också mappa fälten i registren. Mappning av integreringsfält länkar fält i [!INCLUDE[d365fin](includes/d365fin_md.md)]-register med motsvarande fält i [!INCLUDE[d365fin](includes/cds_long_md.md)] och avgör om data ska synkroniseras i respektive register. Den standardregistermappning som [!INCLUDE[d365fin](includes/d365fin_md.md)] tillhandahåller innehåller fältmappningar, men du kan ändra dessa om du vill. Mer information finns i [Visa enhetsmappningar](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Om du använder en lokal version av [!INCLUDE[d365fin](includes/d365fin_md.md)] definieras mappningar av integreringsfält i register 5336 Mappning av integreringsfält.

### <a name="handling-differences-in-field-values"></a>Hantera skillnader i fältvärden
Ibland är värdena i de fält som du vill mappa olika. I [!INCLUDE[crm_md](includes/crm_md.md)] är exempelvis språkkoden för USA "U.S.", men i [!INCLUDE[d365fin](includes/d365fin_md.md)] är den "US." Detta innebär att du måste omvandla värdet när du synkroniserar data. Detta sker genom omvandlingsregler som du definierar för fälten. Du definierar omvandlingsregler på sidan **Tabellmappningar för integrering** genom att välja **Mappning** och sedan **Fält**. Fördefinierade regler tillhandahålls, men du kan också skapa egna. Mer information finns i [Omvandlingsregler](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handling-missing-option-values-in-mapping"></a>Hantera alternativvärden som saknas i mappningen
[!INCLUDE[d365fin](includes/cds_long_md.md)] innehåller fält för alternativuppsättningar som tillhandahåller värden som du kan mappa till [!INCLUDE[d365fin](includes/d365fin_md.md)]-fält av typen **Alternativ** för automatisk synkronisering. Under synkroniseringen ignoreras icke-mappade alternativ, saknade alternativ läggs till i relaterad [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen och läggs till i systemtabellen **CDS-alternativmappning** för att hanteras manuellt senare. Du kan t.ex. lägga till saknade alternativ i någon av produkterna och sedan uppdatera mappningen. Mer information finns i [Hantera saknade alternativvärden](admin-cds-missing-option-values.md).

## <a name="coupling-records"></a>Kopplingsposter
Kopplingen länkar poster i [!INCLUDE[d365fin](includes/cds_long_md.md)] med poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Till exempel är konton i [!INCLUDE[d365fin](includes/cds_long_md.md)] vanligtvis kopplade till kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kopplingsposter ger följande fördelar:

* Det möjliggör synkroniseringen.
* Användare kan öppna poster i en företagsapp från den andra. Detta kräver att programmen redan har integrerats.

Kopplingar kan ställas in automatiskt genom att använda synkroniseringsjobb, eller manuellt genom att redigera posten i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Synkronisera data i [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) och [Koppla och synkronisera poster manuellt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filtering-records"></a>Filtrera poster  
Om du inte vill synkronisera alla poster för en specifik [!INCLUDE[d365fin](includes/cds_long_md.md)]-enhet eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell, kan du ställa in filter för att begränsa posterna som synkroniseras. Du ställer in filtren på sidan **Tabellmappningar för integrering**.  

#### <a name="to-filter-records-for-synchronization"></a>Om du vill filtrera poster för synkronisering  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Tabellmappningar för integrering** och välj sedan relaterad länk.

2.  För att filtrera [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster anger du fältet **Tabellfilter**.  

3.  För att filtrera [!INCLUDE[d365fin](includes/cds_long_md.md)]-poster anger du fältet **Filter för integreringstabell**.  

## <a name="creating-new-records"></a>Skapa nya poster  
Som standard är det bara de poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[d365fin](includes/cds_long_md.md)] som är kopplade som synkroniseras med integreringssynkroniseringsjobben. Du kan ställa in tabellmappningar så att nya poster skapas i målet (till exempel [!INCLUDE[d365fin](includes/d365fin_md.md)]) för varje post i källan (till exempel [!INCLUDE[d365fin](includes/cds_long_md.md)]) som inte redan är kopplad.  

Till exempel använder synkroniseringsjobbet SÄLJARE – Dynamics 365 Sales tabellmappningen SÄLJARE. Synkroniseringsjobbet kopierar informationen [!INCLUDE[d365fin](includes/cds_long_md.md)]från användarposter till säljarposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om du skapar tabellmappningen för att skapa nya poster, för varje användare i [!INCLUDE[d365fin](includes/cds_long_md.md)] som inte redan är kopplad till en säljare i [!INCLUDE[d365fin](includes/d365fin_md.md)], skapas en ny säljarpost i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Så här skapar du nya poster under synkroniseringen  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Tabellmappningar för integrering** och välj sedan relaterad länk.

2.  Rensa fältet i tabellmappningposten i fältet **Synka endast kopplade poster**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Använda konfigurationsmallar på tabellmappningar
Du kan tilldela konfigurationsmallar till tabellmappningar som ska användas för nya poster som skapas i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[d365fin](includes/cds_long_md.md)]. För varje tabellmappning kan du ange en konfigurationsmall som ska användas för nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster och en annan mall för att använda nya [!INCLUDE[d365fin](includes/cds_long_md.md)]-poster.  

Om du installerar standardsynkroniseringsinstallationen kommer för det mesta två konfigurationsmallar att skapas automatiskt och användas på tabellmappningen för [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder och [!INCLUDE[crm_md](includes/crm_md.md)]-konton: **CDSCUST** och **CDSACCOUNT**.  

-   **CDSCUST** används för att skapa och synkronisera nya kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)] baserat på ett konto i [!INCLUDE[crm_md](includes/crm_md.md)].  

     Den här mallen skapas, genom att kopiera en befintlig konfigurationsmall för kunder i programmet. **CDSCUST** skapas endast om det finns en befintlig konfigurationsmall och fältet **Valutakod** i mallen är tomt. Om ett fält i konfigurationsmallen innehåller ett värde, ska värdet användas i stället för värdet i det mappade fältet i [!INCLUDE[d365fin](includes/cds_long_md.md)]-kontot. Till exempel, om fältet **Land/region** i ett konto i [!INCLUDE[d365fin](includes/cds_long_md.md)] innehåller *USA* och fältet **Land/region** i konfigurationsmallen är *GB* används *GB* som **Land/region** för kunden i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CDSACCOUNT** skapar och synkroniserar nya konton i [!INCLUDE[d365fin](includes/cds_long_md.md)] baserat på ett konto i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Ange konfigurationsmallar på en tabellmappning  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Tabellmappningar för integrering** och välj sedan relaterad länk.

2.  I tabellmappningposten i listan anger du fältet **Mallkod för tabellkonfig.** till konfigurationsmallen som ska användas för nya poster i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Ange fältet **Mallkod för int.tabellkonfig.** till konfigurationsmallen som ska användas för nya poster i [!INCLUDE[d365fin](includes/cds_long_md.md)].

## <a name="see-also"></a>Se även  
[Om integrering Dynamics 365 Business Central med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synkroniserar Business Central och [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)   
[Schemalägg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
