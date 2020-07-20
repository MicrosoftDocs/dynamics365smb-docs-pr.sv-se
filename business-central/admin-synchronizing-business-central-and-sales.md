---
title: Synkronisering och dataintegrering | Microsoft Docs
description: Synkroniseringen kopierar data mellan Common Data Service-transaktioner och Business Central-transaktioner och håller datan i båda systemen uppdaterade.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 0763119e323a8bae6d2b7ce3db0780284befa292
ms.sourcegitcommit: 0c6f4382fad994fb6aea9dcde3b2dc25382c5968
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484115"
---
# <a name="synchronizing-data-in-business-central-with-common-data-service"></a>Synkroniserar data i Business Central med Common Data Service
När du integrerar [!INCLUDE[d365fin](includes/cds_long_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du bestämma om du vill synkronisera data i valda fält för i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster (till exempel kunder, kontakter och säljare) med motsvarande poster i [!INCLUDE[d365fin](includes/cds_long_md.md)] (till exempel konton, kontaktpersoner och användare). Beroende på vilken typ av post kan du synkronisera data från [!INCLUDE[d365fin](includes/cds_long_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)] och vice versa. Mer information finns i [Integrera med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkronisering använder följande element:

* Tabellmappningar för integrering
* Fältmappningar för integrering
* Synkroniseringsregler
* Kopplade poster

När synkroniseringen har konfigurerats kan du koppla upp [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster till [!INCLUDE[d365fin](includes/cds_long_md.md)]-poster för att synkronisera deras data. Du kan starta en synkronisering manuellt eller enligt ett schema. I tabellen nedan finns en översikt över hur du kan synkronisera poster.  

|  Typ  |  Metod  |  Gå till  |  
|--------|----------|-------|  
|Manuell synkronisering|Synkronisera med utgångspunkt från post till post.<br /><br /> Du kan synkronisera enskilda poster i [!INCLUDE[d365fin](includes/d365fin_md.md)], till exempel en kund med en motsvarande [!INCLUDE[d365fin](includes/cds_long_md.md)]-post, till exempel ett konto. Detta är vanligtvis hur användarna kommer att arbeta med [!INCLUDE[d365fin](includes/cds_long_md.md)] data i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Koppla och synkronisera poster manuellt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronisera utifrån tabellmappningen.<br /><br /> Du kan synkronisera alla poster i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell med en enhet [!INCLUDE[d365fin](includes/cds_long_md.md)]-enhet.|[Synkronisera individuella tabellmappningar](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synkronisera alla ändrade poster för alla tabellmappningar.<br /><br /> Du kan synkronisera alla poster som har ändrats i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller sedan den senaste synkroniseringen.|[Synkronisera alla ändrade poster](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Fullständig synkronisering av all data för alla tabellmappningar.<br /><br /> Du kan synkronisera all data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller och [!INCLUDE[d365fin](includes/cds_long_md.md)]-enheter som mappas och skapa nya poster i mållösningen för ej kopplade poster i källösningen.<br /><br /> Fullständig synkronisering synkroniserar alla data och ignorerar kopplingen. Vanligtvis gör du en fullständig synkronisering när du ställer in integrering och endast en av lösningarna innehåller data. En fullständig synkronisering kan också vara lämplig i demonstrationsmiljöer.|[Kör en fullständig synkronisering](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Schemalagd synkronisering|Synkronisera alla ändringar i data för alla tabellmappningar.<br /><br /> Du kan synkronisera [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[d365fin](includes/cds_long_md.md)] på schemalagda intervall, genom att ställa in projekt i jobbkön.|[Schemalägg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-entity-mapping-for-synchronization"></a>Standardenhetsmappningar för synkronisering
Enheter i [!INCLUDE[d365fin](includes/cds_long_md.md)] till exempel konton, är integrerade med motsvarande typer av enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] till exempel kunder. För att arbeta med [!INCLUDE[d365fin](includes/cds_long_md.md)] data anger du länkar som kallas kopplingar mellan enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[d365fin](includes/cds_long_md.md)].

I följande tabell visas standardmappningen mellan enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[d365fin](includes/cds_long_md.md)] som [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/cds_long_md.md)]|Synkroniseringsriktning|Standardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Säljare/Inköpare|Användare|[!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/cds_long_md.md)] kontaktfilter: **Status** är **Nej**, **Licensierad användare** är **Ja**, integreringsanvändarläge är **Nej**|
|Kund|Konto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] och [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/cds_long_md.md)] kontofilter: **Relationstyp** är **Kund** och **Status** är **Aktiv**. [!INCLUDE[d365fin](includes/d365fin_md.md)] filter: **Spärrad** är tom (kunden är inte spärrad).|
|Leverantör|Konto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] och [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/cds_long_md.md)] kontofilter: **Relationstyp** är **Leverantör** och **Status** är **Aktiv**. [!INCLUDE[d365fin](includes/d365fin_md.md)] filter: **Spärrad** är tom (leverantör är inte spärrad).|
|Kontakt|Kontakt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] och [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-kontaktfilter: **Typen** är **Person** och kontakten har tilldelats till ett företag. [!INCLUDE[d365fin](includes/cds_long_md.md)] kontaktfilter: Kontakten har tilldelats till ett företag och överordnad kundtyp är **Konto**|
|Valuta|Transaktionsvaluta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)]| |


### <a name="tip-for-admins-viewing-entity-mappings"></a>Tips för administratörer: Visa entitetsmappningar
Kan du visa mappning mellan enheter i [!INCLUDE[d365fin](includes/cds_long_md.md)] och tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] på sidan **Tabellmappningar för integrering**, där du kan även använda filter. Du definierar mappningen mellan fälten i [!INCLUDE[d365fin](includes/d365fin_md.md)] tabeller och fält i [!INCLUDE[d365fin](includes/cds_long_md.md)] enheter på sidan **Tabellmappningar för integrering**, där du kan lägga till ytterligare mappningslogik. Det kan exempelvis vara praktiskt om du behöver felsöka synkronisering.

## <a name="see-also"></a>Se även  
[Koppla och synkronisera poster manuellt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Schemalägg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrering med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
