---
title: Designdetaljer - Bokföring av monteringsorder | Microsoft Docs
description: Monteringsorderbokföring baserad på samma principer som när du bokför de liknande aktiviteterna försäljningsorder och produktionförbrukning/utflöde. Principerna kombineras genom att monteringsorder har sitt eget användargränssnitt för bokföring, liknande det för försäljningsorder, medan den faktiska transaktionsbokföringen sker i bakgrunden som direkta artikel- och resursjournalbokföringar, som det för produktionsförbrukning, utflöde och kapacitet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a26cafc11479d7065645947f63fa93d28ddb824f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "941779"
---
# <a name="design-details-assembly-order-posting"></a>Designdetaljer: Bokföring av monteringsorder
Monteringsorderbokföring baserad på samma principer som när du bokför de liknande aktiviteterna försäljningsorder och produktionförbrukning/utflöde. Principerna kombineras genom att monteringsorder har sitt eget användargränssnitt för bokföring, liknande det för försäljningsorder, medan den faktiska transaktionsbokföringen sker i bakgrunden som direkta artikel- och resursjournalbokföringar, som det för produktionsförbrukning, utflöde och kapacitet.  

Precis som för produktionsorderbokföring konverteras de förbrukade resurserna och utflödas som monteringsartikeln när monteringsordern har bokförts. Mer information finns i [Designdetaljer: Bokföring av produktionsorder](design-details-production-order-posting.md) Däremot är kostnadsflödet för monteringsorder mindre komplicerat, särskilt eftersom bokföring av monteringskostnad endast uppstår en gång och därför inte genererar lager för produkter i arbete.  

Följande journalbokföringar uppstår under monteringsorderbokföring:  

-   Artikeljournalen bokför positiva artikeltransaktioner som representerar utflöde av monteringsartikeln från monteringsorderhuvudet.  
-   Artikeljournalen bokför negativa artikeltransaktioner som representerar förbrukningen av monteringkomponenter från monteringsorderraderna.  
-   Resursjournalen bokför förbrukningen av monteringsresurser (tidsenheter), från monteringsorderraderna.  
-   Kapacitetsjournalen bokför värdetransaktioner som avser resursförbrukningen från monteringsorderraderna.  

Följande diagram visar strukturen på artikel- och resurstransaktioner som kommer från monteringsorderbokföring.  

![Artikel, resurs och kapacitetstransaktioner som resulterar från monteringsorderbokföring](media/design_details_assembly_posting_1.png "Artikel, resurs och kapacitetstransaktioner som resulterar från monteringsorderbokföring")  

> [!NOTE]  
>  Maskinen och produktionsgrupper inkluderas för att visa att kapacitetstransaktioner skapas från både produktion och montering.  

Följande diagram visar hur monteringsdata flödar till transaktioner under bokföringen:  

![Monteringsrelaterat transaktionsflöde vid bokföring](media/design_details_assembly_posting_2.png "Monteringsrelaterat transaktionsflöde vid bokföring")  

## <a name="posting-sequence"></a>Bokföringssekvens  
Bokföring av en monteringsorder uppstår i följande ordning:  

1.  Monteringsorderraderna är bokförda.  
2.  Monteringsorderhuvudet bokförs.  

Följande tabell skisserar sekvensen med åtgärder.  

|Åtgärd|Description|  
|------------|-----------------|  
|initialisera bokföring|1. Gör inledande kontroller.<br />2. Lägg till bokföringsnumret och ändra monteringsorderhuvudet.<br />3. Släpp monteringsordern.|  
|Post|<ol><li>Skapa det bokförda monteringsorderhuvudet.</li><li>Kopiera kommentarsrader.</li><li>Bokför monteringsorderrader (förbrukning):<br /><br /> <ol><li>Skapa en statussida för att beräkna monteringsförbrukning.</li><li>Få det återstående antalet som artikeljournalraden ska baseras på.</li><li>Återställ förbrukade och återstående kvantiteter.</li><li>För monteringsorderrader av typen Artikel:<br /><br /> <ol><li>Fyll i fälten för varje artikeljournalrad.</li><li>Överför reservationer till artikeljournalraden.</li><li>Bokför artikeljournalraden för att skapa artikeltransaktionerna.</li><li>Skapa distributionslagerjournalraderna och bokför dem.</li></ol></li><li>För monteringsorderrader av typen Resurs:<br /><br /> <ol><li>Fyll i fälten för varje artikeljournalrad.</li><li>Bokför artikeljournalraden. Det skapar kapacitetstransaktioner.</li><li>Skapa och bokför resursjournalraden.</li></ol></li><li>Överför fältvärden från monteringsorderraden till en nyligen skapad och bokförd monteringsorderrad.</li></ol></li><li>Bokför monteringsorderhuvudet (utflöde).<br /><br /> <ol><li>Fyll i fälten för varje artikeljournalrad.</li><li>Överför reservationer till artikeljournalraden.</li><li>Bokför artikeljournalraden för att skapa artikeltransaktionerna.</li><li>Skapa distributionslagerjournalraderna och bokför dem.</li><li>Återställ monteringsantalet och den återstående kvantiteten.</li></ol></li></ol>|  

> [!IMPORTANT]  
>  Till skillnad från utflöde från produktion, som bokförs med förväntad kostnad, bokförs monteringsutflöde med faktisk kostnad.  

## <a name="cost-adjustment"></a>Kostnadsjustering  
 När en monteringsorder bokförs, vilket betyder att komponenter (material) och resurser monteras till en ny artikel, kommer det vara möjligt att bestämma den faktiska kostnaden för monteringsartikeln och den faktiska lagerkostnaden för de ingående komponenterna. Det kan uppnås genom att flytta fram kostnader från de bokförda transaktionerna för källan (komponenter och resurser) till destinationens bokförda transaktioner (monteringsartikeln). Speditionen av kostnader sker genom att beräkna och skapa nya transaktioner som kallas justeringstransaktioner som blir associerade med destinationstransaktionerna.  

 Monteringskostnaderna som ska flyttas fram identifieras med detekteringsmekanismen Ordernivå. Information om andra identifieringsmetoder för justering finns i [detaljer: kostnadsjustering](design-details-cost-adjustment.md).  

### <a name="detecting-the-adjustment"></a>Identifiera justeringen  
Funktionen för ordernivåidentifiering används i konverteringscenarion, produktion och montering. Funktionen fungerar så här:  

-   Kostnadsjustering upptäcks genom att markera ordern när ett material/en resurs bokförs som förbrukad/använd.  
-   Kostnader speditioneras genom att använda kostnaderna från material/resurs till de utflödetransaktioner som är kopplade till samma order.  

Följande grafik visar strukturen för justeringstransaktionen och hur monteringskostnader justeras.  

![Monteringsrelaterat transaktionsflöde under kostnadsjustering](media/design_details_assembly_posting_3.png "Monteringsrelaterat transaktionsflöde under kostnadsjustering")  

### <a name="performing-the-adjustment"></a>Utföra justeringen  
Distribution av identifierade justeringar från material- och resurskostnader till monteringsutflödetransaktionerna utförs av batchjobbet **Justera kost. - artikeltrans.**. Den innehåller funktionen Gör justeringar på flera nivåer som består av följande två element:  

-   Gör monteringsorderjustering – som flyttar fram kostnad från material och resursförbrukning till monteringsutflödestransaktionen. Rad 5 och 6 i algoritmen nedan ansvarar för det.  
-   Gör justeringar på en nivå – som flyttar fram kostnader för enskilda artiklar med deras värderingsprincip. Rad 9 och 10 i algoritmen nedan ansvarar för det.  

![Sammanfattning av kostnadsjusteringsalgoritm för monteringsbokföring](media/design_details_assembly_posting_4.jpg "Sammanfattning av kostnadsjusteringsalgoritm för monteringsbokföring")  

> [!NOTE]  
>  Elementet Gör PIA-justeringar, på rad 7 och 8, är ansvarigt för att flytta fram produktionsmaterial och kapacitetsanvändning till utflödet av oavslutade produktionsorder. Det används inte när du justerar monteringsorderkostnader eftersom PIA-konceptet inte gäller för montering.  

För mer information om hur kostnader från produktion och montering bokförs i redovisningen, se [Designdetaljer: Lagerbokföring](design-details-inventory-posting.md).  

## <a name="assembly-costs-are-always-actual"></a>Monteringkostnader är alltid faktiska  
 Begreppet produkter i arbete (PIA) tillämpas inte i monteringsorderbokföring. Monteringkostnader bokförs bara som faktiska kostnader, aldrig som förväntade kostnader. Mer information finns i [Designdetaljer: Bokföring av förväntad kostnad](design-details-expected-cost-posting.md)  

Det aktiveras av följande datastruktur.  

-   I fältet **Typ** på artikeljournalrader i tabellerna **Kapacitetstrans.** och **Värdetransaktion** används *Resurs* för att identifiera monteringresurstransaktioner.  
-   I fältet **Artikeltransaktionstyp** på artikeljournalrader i tabellerna **Kapacitetstrans.** och **Värdetransaktion** används *Monteringsutflöde* och *Monteringsförbrukning* för att identifiera utflödesmonteringsartikeltransaktionerna och de förbrukade monteringskomponenttransaktionerna.  

Dessutom fylls bokföringsmallfält på monteringsorderhuvuden och monteringsorderrader i som standard enligt följande.  

|Enhet|Typ|Bokföringsmall|Produktbokföringsmall|  
|------------|----------|-------------------|------------------------------|  
|Monteringsorderhuvud|Artikel|Lagerbokföringsmall|Produktbokföringsmall|  
|Monteringsorderrad|Artikel|Lagerbokföringsmall|Produktbokföringsmall|  
|Monteringsorderrad|Resurs||Produktbokföringsmall|  

Därmed bokförs endast faktiska kostnader till redovisningen, och inga interimskonton fylls i från monteringsorderbokföring. Mer information finns i [detaljer: konton i redovisningen](design-details-accounts-in-the-general-ledger.md).  

## <a name="assemble-to-order"></a>Montering mot kundorder  
Artikeltransaktionen som är resultatet av att bokföra en försäljning med montering mot kundorder är kopplad till motsvarande artikeltransaktion för monteringsutflödet. Därefter hämtas kostnaden för en försäljning med montering mot kundorder från monteringsordern som den kopplats till.  

Artikeltransaktioner av typen Försäljning som kommer från bokföring av antalet för montering mot kundorder markeras med **Ja** i fältet **Montering mot kundorder**.  

Vid bokföring av försäljningsorderrader, där en del är lagerkvantitet och en annan del är antal för montering mot kundorder resulterar i separata artikeltransaktioner, en för lagerkvantitet och en för antalet för montering mot kundorder.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Bokföring av produktionsorder](design-details-production-order-posting.md)   
 [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)  
 [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
