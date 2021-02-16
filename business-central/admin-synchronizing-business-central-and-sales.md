---
title: Synkronisering och dataintegrering | Microsoft Docs
description: Synkroniseringen kopierar data mellan Microsoft Dataverse-register och Business Central-poster, och håller datan i båda systemen uppdaterade.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 83de0f6eb46921afdb4e69fbbe5260670a7fdbbc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755107"
---
# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Synkroniserar data i Business Central med Microsoft Dataverse
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

När du integrerar [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)] kan du bestämma om du vill synkronisera data i valda fält i [!INCLUDE[prod_short](includes/prod_short.md)] (till exempel kunder, kontakter och säljare) med motsvarande rader i [!INCLUDE[prod_short](includes/cds_long_md.md)] (till exempel konton, kontaktpersoner och användare). Beroende på radtyp kan du synkronisera data från [!INCLUDE[prod_short](includes/cds_long_md.md)] till [!INCLUDE[prod_short](includes/prod_short.md)] och vice versa. Mer information finns i [Integrera med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkronisering använder följande element:

* Registermappningar för integrering
* Fältmappningar för integrering
* Synkroniseringsregler
* Kopplade poster

När synkroniseringen har konfigurerats kan du koppla [!INCLUDE[prod_short](includes/prod_short.md)]-poster till [!INCLUDE[prod_short](includes/cds_long_md.md)]-rader i syfte att synkronisera deras data. Du kan starta en synkronisering manuellt eller enligt ett schema. I tabellen nedan finns en översikt över olika sätt att synkronisera.  

|  Typ  |  Metod  |  Gå till  |  
|--------|----------|-------|  
|Manuell synkronisering|Synkronisera med utgångspunkt från rad-till-rad.<br /><br /> Du kan synkronisera enskilda poster i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel en kund, med en motsvarande [!INCLUDE[prod_short](includes/cds_long_md.md)]-rad, till exempel ett konto. Detta är vanligtvis hur användarna kommer att arbeta med [!INCLUDE[prod_short](includes/cds_long_md.md)] data i [!INCLUDE[prod_short](includes/prod_short.md)].|[Koppla och synkronisera poster manuellt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronisera utifrån registermappningen.<br /><br /> Du kan synkronisera alla poster i ett [!INCLUDE[prod_short](includes/prod_short.md)]-register med ett [!INCLUDE[prod_short](includes/cds_long_md.md)]-register.|[Synkronisera individuella registermappningar](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synkronisera alla ändrade poster för alla registermappningar.<br /><br /> Du kan synkronisera alla poster som har ändrats i [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller sedan den senaste synkroniseringen.|[Synkronisera alla ändrade poster](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Fullständig synkronisering av all data för alla registermappningar.<br /><br /> Du kan synkronisera all data i [!INCLUDE[prod_short](includes/prod_short.md)]- och [!INCLUDE[prod_short](includes/cds_long_md.md)]-register som mappas, och skapa nya poster eller rader i mållösningen för ej kopplade poster i ursprungslösningen.<br /><br /> Fullständig synkronisering synkroniserar alla data och ignorerar kopplingen. Vanligtvis gör du en fullständig synkronisering när du ställer in integrering och endast en av lösningarna innehåller data. En fullständig synkronisering kan också vara lämplig i demonstrationsmiljöer.|[Kör en fullständig synkronisering](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Schemalagd synkronisering|Synkronisera alla ändringar i data för alla registermappningar.<br /><br /> Du kan synkronisera [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)] på schemalagda intervall, genom att ställa in projekt i jobbkön.|[Schemalägg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-table-mapping-for-synchronization"></a>Standardregistermappningar för synkronisering
Register i [!INCLUDE[prod_short](includes/cds_long_md.md)], till exempel konton, är integrerade med motsvarande registertyper i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel kunder. För att arbeta med [!INCLUDE[prod_short](includes/cds_long_md.md)]-data anger du länkar kallade "kopplingar" mellan tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)].

I följande tabell visas standardmappningen mellan register i [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> Du kan återställa konfigurationsändringar som har gjorts i integrationstabellen och fältmappningarna till standardinställningarna genom att välja mappningarna och sedan välja **Använd standardinställning för synkronisering**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Synkroniseringsriktning | Standardfilter |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Säljare/Inköpare | Användare | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] kontaktfilter: **Status** är **Nej**, **Licensierad användare** är **Ja**, integreringsanvändarläge är **Nej** |
| Kund | Konto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] kontofilter: **Relationstyp** är **Kund** och **Status** är **Aktiv**. [!INCLUDE[prod_short](includes/prod_short.md)] filter: **Spärrad** är tom (kunden är inte spärrad). |
| Leverantör | Konto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] kontofilter: **Relationstyp** är **Leverantör** och **Status** är **Aktiv**. [!INCLUDE[prod_short](includes/prod_short.md)] filter: **Spärrad** är tom (leverantör är inte spärrad). |
| Kontakt | Kontakt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/prod_short.md)]-kontaktfilter: **Typen** är **Person** och kontakten har tilldelats till ett företag. [!INCLUDE[prod_short](includes/cds_long_md.md)] kontaktfilter: Kontakten har tilldelats till ett företag och överordnad kundtyp är **Konto** |
| Valuta | Transaktionsvaluta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |


### <a name="tip-for-admins-viewing-table-mappings"></a>Tips för administratörer: Visa registermappningar
Du kan visa mappningen mellan register i [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)] på sidan **Tabellmappningar för integrering**, där du även kan tillämpa filter. Du definierar mappningen mellan fälten i [!INCLUDE[prod_short](includes/prod_short.md)]-register och kolumnerna i [!INCLUDE[prod_short](includes/cds_long_md.md)]-register på sidan **Mappning av integreringsfält**, där du kan lägga till ytterligare mappningslogik. Det kan exempelvis vara praktiskt om du behöver felsöka synkronisering.

## <a name="see-also"></a>Se även  
[Koppla och synkronisera poster manuellt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Schemalägg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrering med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
