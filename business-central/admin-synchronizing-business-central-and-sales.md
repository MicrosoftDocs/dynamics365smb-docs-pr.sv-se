---
title: Synkronisering och dataintegrering | Microsoft Docs
description: Synkroniseringen kopierar data mellan Dynamics 365 for Sales-transaktioner och Business Central-poster och behåller data i båda systemen uppdaterade.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: a2adf188f616f3a9cbb0e0d3135ee79d238c453b
ms.sourcegitcommit: 92c7b6c5f0a5d8becbef106ab85258906765bc3e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540229"
---
# <a name="synchronizing-data-in-business-central-and-dynamics-365-for-sales"></a>Synkroniserar data i Business Central och Dynamics 365 for Sales
När du integrerar [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du bestämma om du vill synkronisera data i valda fält för i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster (till exempel kunder, kontakter och säljare) med motsvarande poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] (till exempel konton, kontaktpersoner och användare). Beroende på vilken typ av post kan du synkronisera data från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)] och vice versa. Mer information finns i [Integrera med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkronisering använder följande element:

* Tabellmappningar för integrering
* Fältmappningar för integrering
* Synkroniseringsregler
* Kopplade poster

När synkroniseringen har konfigurerats kan du koppla upp [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster till [!INCLUDE[crm_md](includes/crm_md.md)]-poster för att synkronisera deras data. Du kan starta en synkronisering manuellt eller enligt ett schema. I tabellen nedan finns en översikt över hur du kan synkronisera poster.  

|  Typ  |  Metod  |  Gå till  |  
|--------|----------|-------|  
|Manuell synkronisering|Synkronisera med utgångspunkt från post till post.<br /><br /> Du kan synkronisera enskilda poster i [!INCLUDE[d365fin](includes/d365fin_md.md)], till exempel en kund med en motsvarande [!INCLUDE[crm_md](includes/crm_md.md)]-post, till exempel ett konto. Detta är vanligtvis hur användarna kommer att arbeta med [!INCLUDE[crm_md](includes/crm_md.md)] data i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Koppla och synkronisera poster manuellt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronisera utifrån tabellmappningen.<br /><br /> Du kan synkronisera alla poster i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell med en enhet [!INCLUDE[crm_md](includes/crm_md.md)]-enhet.|[Synkronisera individuella tabellmappningar](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synkronisera alla ändrade poster för alla tabellmappningar.<br /><br /> Du kan synkronisera alla poster som har ändrats i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller sedan den senaste synkroniseringen.|[Synkronisera alla ändrade poster](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Fullständig synkronisering av all data för alla tabellmappningar.<br /><br /> Du kan synkronisera all data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller och [!INCLUDE[crm_md](includes/crm_md.md)]-enheter som mappas och skapa nya poster i mållösningen för ej kopplade poster i källösningen.<br /><br /> Fullständig synkronisering synkroniserar alla data och ignorerar kopplingen. Vanligtvis gör du en fullständig synkronisering när du ställer in integrering och endast en av lösningarna innehåller data. En fullständig synkronisering kan också vara lämplig i demonstrationsmiljöer.|[Kör en fullständig synkronisering](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Schemalagd synkronisering|Synkronisera alla ändringar i data för alla tabellmappningar.<br /><br /> Du kan synkronisera [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] på schemalagda intervall, genom att ställa in projekt i jobbkön.|[Schemalägg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Standardinställd försäljningsenhetsmappningar för synkronisering
Enheter i [!INCLUDE[crm_md](includes/crm_md.md)] till exempel konton, är integrerade med motsvarande typer av enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] till exempel kunder. För att arbeta med [!INCLUDE[crm_md](includes/crm_md.md)] data anger du länkar som kallas kopplingar mellan enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)].

I följande tabell visas standardmappningen mellan enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] som [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Synkroniseringsriktning|Standardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Säljare/Inköpare|Användare|[!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **Status** är **Nej**, **licensierad användare** är **Ja**, integrationsanvändarläge är **Nej**|
|Kund|Konto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontofilter: **Relationstyp** är **Kund** och **Status** är **Aktiv**.|
|Kontakt|Kontakt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-kontaktfilter: **Typen** är **Person** och kontakten har tilldelats till ett företag. Sales-kontaktfilter: Kontakten har tilldelats till ett företag och överordnad kundtyp är **Konto**|
|Valuta|Transaktionsvaluta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Måttenhet|Enhetsgrupp|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Artikel|Produkt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **produkttyp** är **Sales-lager**|
|Resurs|Produkt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **produkttyp** är **Tjänster**|
|Kund prisgrupp|Prislista|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Förs.pris|Produktprislista|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] kontaktfilter: **försäljningskod** är inte tom, **förs.typ** är **kundprisgrupp**|
|Affärsmöjlighet|Affärsmöjlighet|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|Försäljningsfakturahuvud|Fakturera|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Försäljningsfakturarad|Fakturaprodukt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Rubrik för försäljningsorder|Reservationstransaktion|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] Försäljningsrubrikfilter: **Dokumenttyp** är Order, **Status** är Frisläppt|
|Försäljningsordermeddelanden|Försäljningsordermeddelanden|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="tip-for-admins-viewing-entity-mappings"></a>Tips för administratörer: Visa entitetsmappningar
Kan du visa mappning mellan enheter i [!INCLUDE[crm_md](includes/crm_md.md)] och tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] på sidan **Tabellmappningar för integrering**, där du kan även använda filter. Du definierar mappningen mellan fälten i [!INCLUDE[d365fin](includes/d365fin_md.md)] tabeller och fält i [!INCLUDE[crm_md](includes/crm_md.md)] enheter på sidan **Tabellmappningar för integrering**, där du kan lägga till ytterligare mappningslogik. Det kan exempelvis vara praktiskt om du behöver felsöka synkronisering.

### <a name="tip-for-developers-mapping-fields-in-business-central-to-the-option-sets-in-sales"></a>Tips för utvecklare: mappningsfält i Business Central till alternativuppsättningar i Sales
Om du är utvecklare och vill lägga till alternativ för alternativuppsättningar [!INCLUDE[crm_md](includes/crm_md.md)], måste du ha angett detta. Det finns tre tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] som mappas till alternativfältet för enheten **konto** i [!INCLUDE[crm_md](includes/crm_md.md)]. Poster i tabellerna som inte är länkade till alternativ i [!INCLUDE[crm_md](includes/crm_md.md)] kommer inte att synkroniseras. Det innebär att fälten **alternativet** kommer att vara tomt i [!INCLUDE[crm_md](includes/crm_md.md)].

Följande tabell visar mappningar från [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller för fältet **alternativ** i enheten **konto** i [!INCLUDE[crm_md](includes/crm_md.md)].

|Bord|Alternativfältet i kontoentiteten|
|----------------------|-------------------------------------------|
|Betalningsvillkor|Betalningsvillkor|
|Utleveransvillkor|Adress 1: Leveransvillkor|
|Speditör|Adress 1: Leveransmetod|

### <a name="synchronization-rules"></a>Synkroniseringsregler
Följande tabell beskriver regler som kontrollerar synkroniseringen mellan appar.

> [!NOTE]  
> Ändrar data i [!INCLUDE[crm_md](includes/crm_md.md)] som genomfördes av [!INCLUDE[crm_md](includes/crm_md.md)]-anslutning användarkontot är inte synkroniserade. Därför rekommenderar vi att du inte ändrar data när du använder kontot. Mer information finns i [Ställa in integration med Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Bord|Regel|
|-----|----|
|Kunder|Innan en kund kan synkroniseras till ett konto måste försäljningpersonen, som tilldelats kunden, kopplas till en [!INCLUDE[crm_md](includes/crm_md.md)]-användare. Därför när du vill köra synkroniseringsjobbet KUNDER – Dynamics 365 for Sales och du ställer in det till att skapa nya poster, säkerställ att du synkroniserar säljare med [!INCLUDE[crm_md](includes/crm_md.md)] innan du synkroniserar kunder med [!INCLUDE[crm_md](includes/crm_md.md)]-konton. <br /> <br />Synkroniseringsjobbet KUNDER – Dynamics 365 for Sales synkroniserar endast Sales-konton som har relationstypen Kund.|
|Kontakter|Endast kontakter i [!INCLUDE[crm_md](includes/crm_md.md)] som associeras med ett konto skapas i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Säljarkod värdet definierar ägare till den kopplade enheten i [!INCLUDE[crm_md](includes/crm_md.md)].|
|Valutor|Valutor kopplas till transaktionvalutor i [!INCLUDE[crm_md](includes/crm_md.md)] baserat på ISO-koder. Endast valutor, som har en standard-ISO-kod, kopplas och synkroniseras med transaktionsvalutor.|
|Enheter|Måttenheter synkroniseras med enhetsgrupper i [!INCLUDE[crm_md](includes/crm_md.md)]. Det kan finnas endast en måttenhet som definieras i enhetsgruppen.|
|Artiklar|När artiklar synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter skapar [!INCLUDE[d365fin](includes/d365fin_md.md)] automatiskt en prislista i [!INCLUDE[crm_md](includes/crm_md.md)]. För att undvika synkroniseringsfel bör du inte ändra denna prislista manuellt.|
|Säljare|Säljare är kopplat till systemanvändare i [!INCLUDE[crm_md](includes/crm_md.md)]. Användaren måste vara aktiverad och licens och vara integrationsanvändaren. Observera att detta är den första tabellen som måste synkroniseras eftersom den används i kunder, kontaktpersoner, affärsmöjligheter och fakturor.|
|Resurser|Resurser som ska synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter som har produktypen tjänster.|
|Kundprisgrupper|Kundprisgrupper synkroniseras med Sales-prislistor.|
|Förs.priser|Sales-priser som har försäljning skriver kundprisgrupp och har definierats försäljningskod synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-prislistrader|
|Affärsmöjligheter|Affärsmöjligheter som ska synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-affärsmöjligheter. Säljarkod värdet definierar ägare till den kopplade enheten i [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bokförda försäljningsfakturor|Bokförda försäljningsfakturor som är synkroniserade med försäljningsfakturor. Innan du kan synkronisera en faktura, är det bättre att synkronisera alla andra enheter som kan delta i fakturan från säljare till prislistor. Säljarkodvärdet i fakturarubriken definierar ägare till den kopplade enheten i Sales.|
|Försäljningsorder|Släppta försäljningsorder (rubriker) synkroniseras med försäljningsordern. Innan en order kan synkroniseras, är det bättre att synkronisera alla andra enheter som kan delta i ordern från säljare till prislistor. Säljarkodvärdet i orderrubriken definierar ägare till den kopplade enheten i Sales.|  

## <a name="see-also"></a>Se även  
[Koppla och synkronisera poster manuellt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Schemalägg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrera med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
