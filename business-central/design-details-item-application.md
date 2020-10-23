---
title: Designdetaljer - artikelkoppling | Microsoft Docs
description: Det här avsnittet beskriver var lagerkvantitet och värdet registreras när du bokför en lagertransaktion.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, items, ledger entries, posting, inventory
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 14aae820463718357d3bac69524751833f5dd79d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913669"
---
# <a name="design-details-item-application"></a>Designdetaljer: Artikelkoppling

När du bokför en lagertransaktion registreras antalsbokföringen i artikeltransaktionerna, och värdebokföringen i värdetransaktionerna. Mer information finns i [Designdetaljer: Lagerbokföring](design-details-inventory-posting.md)  

Dessutom skapas en artikelkoppling för att koppla kostnadsmottagare till sin kostnadskälla för att skapa kostnadsspedition enligt värderingsprincipen. Mer information finns i [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] gör två typer av artikelkopplingar.  

|Kopplingstyp|Description|  
|----------------------|---------------------------------------|  
|Antalskoppling|Skapat för alla lagertransaktioner|  
|Kostnadskoppling|Skapat för ankommande transaktioner tillsammans med en antalskoppling som ett resultat av användarinteraktion i specialprocesser.|  

Artikelkopplingar kan utföras på följande sätt.  

|Metod|Description|Kopplingstyp|  
|------------|---------------------------------------|----------------------|  
|Automatiskt|Uppstår som allmän kostnadsspedition enligt värderingsprincipen|Antalskoppling|  
|Fast|Gjort av användaren när:<br /><br /> -   Bearbeta returer<br />-   Bokföringskorrigeringar<br />-   Ångra bokförda antal<br />-   Skapa direktleveranser **Obs!**  Fast koppling kan göras antingen manuellt, genom att ange ett löpnummer i fältet **Koppla från artikellöpnr**, eller genom att använda en funktion som **Hämta bokförda dokumentrader som ska återföras**.|Antalskoppling<br /><br /> Kostnadskoppling **Obs!**  Kostnadskopplingen uppstår endast i ankommande transaktioner där fältet **Koppla från artikellöpnr** fylls för att skapa en fast koppling. Visa nästa tabell.|  

Om du gör antalskopplingar eller kostnadskopplingar beror på lagertransaktionens riktning, och om en artikelkoppling utförs automatiskt eller fast, i samband med specifika processer.  

Efterföljande tabell visar, baserat på de centrala kopplingsfälten på lagertransaktionsrader, hur kostnader flödar beroende på transaktionsriktningen. Det innebär även när och varför artikelkopplingen är av typen antal eller kostnad.  

|-|Koppla till fältet Artikeltrans.|Koppla från fältet Artikeltrans.|  
|-|--------------------------------|----------------------------------|  
|Koppling för avgående transaktion|Den avgående transaktionen drar kostnaden från den öppna ankommande transaktionen.<br /><br /> **Antalskoppling**|Stöds inte|  
|Koppling för ankommande transaktion|Den ankommande transaktionen trycker kostnaden på den öppna avgående transaktionen.<br /><br /> Den ankommande transaktionen är kostnadskällan.<br /><br /> **Antalskoppling**|Den ankommande transaktionen drar kostnaden från den avgående transaktionen. **Obs!**  När du gör den fast kopplingen hanteras ankommande transaktioner som en försäljningsretur. Därför förblir den kopplade avgående transaktionen öppen. <br /><br /> Den ankommande transaktionen är INTE kostnadskällan.<br /><br /> **Kostnadskoppling**|  

> [!IMPORTANT]  
> En försäljningsretur anses INTE vara en kostnadskälla när den är fast kopplad.  
>
> Försäljningsposten förblir öppen tills den verkliga källan bokförs.  

I en artikelkopplingstransaktion registreras följande information.  

|Fält|Description|  
|---------------------------------|---------------------------------------|  
|**Artikeltrans.löpnr**|Artikeltransaktionens nummer för transaktionen som den här kopplingstransaktionen skapas för.|  
|**Ankommande artikeltrans.nr.**|Artikeltransaktionens nummer för lagerökningen som transaktionen ska kopplas till om det är tillämpbart.|  
|**Avgående artikeltrans.nr.**|Artikeltransaktionens nummer för lagerminskningen som transaktionen ska kopplas till om det är tillämpbart.|  
|**Antal**|Antalet som kopplas.|  
|**Bokföringsdatum**|Transaktionens bokföringsdatum.|  

## <a name="inventory-increase"></a>Lagerökning  
När en lagerökning bokförs registreras en enkel artikelkopplingstransaktion utan koppling till avgående transaktion.  

### <a name="example"></a>Exempel  
Följande tabell visar den artikeltransaktion som skapas när du bokför en inleverans på 10 enheter.  

|Bokföringsdatum|Ankommande artikeltrans.nr|Avgående artikeltrans.nr|Antal|Artikeltrans.löpnr|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  

## <a name="inventory-decrease"></a>Lagerminskning  
När en lagerminskning bokförs skapas en artikelkopplingstransaktion som kopplar lagerminskningen till en lagerökning. Länken har skapats med artikelns värderingsprincip som riktlinje. För artiklar som använder värderingsprinciperna FIFO, Standard och Genomsnitt baseras kopplingen på FIFO-principen. Lagerminskningen kopplas till lagerökningen med det tidigaste bokföringsdatumet. För artiklar som använder värderingsprinciperna LIFO baseras kopplingen på LIFO-principen. Lagerminskningen kopplas till lagerökningen med det senaste bokföringsdatumet.  

I tabellen  **Artikeltransaktion** visas antalet som ännu inte har kopplats i fältet **Återstående antal**. Om det återstående antalet överstiger 0 så markeras kryssrutan **Öppen**.  

### <a name="example"></a>Exempel  
Följande exempel visar artikelkopplingstransaktionen som skapas när en utleverans bokförs som innehåller fem enheter av artiklarna från inleveransen i föregående exempel. Den första artikelkopplingstransaktionen är inköpsinleveransen. Den andra kopplingstransaktionen tillhör utleveransen.  

Följande tabell visar de två artikelkopplingstransaktionerna som är resultatet av lagerökningen och lagerminskningen.  

|Bokföringsdatum|Ankommande artikeltrans.nr|Avgående artikeltrans.nr|Antal|Artikeltrans.löpnr|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  
|01-03-20|1|2|-5|2|  

## <a name="fixed-application"></a>Fast koppling  
När kostnaden för en lagerökning ska kopplas till en specifik lagerminskning (eller vice versa) skapas en fast koppling. Den fasta kopplingen påverkar transaktionernas återstående antal, men den fasta kopplingen återför också den exakt kostnaden för den ursprungliga transaktionen som kopplingen utförs till, eller från.  

Om en fast koppling ska skapas använder du fältet **Koppla till artikellöpnr** eller **Koppla från artikellöpnr** på dokumentraderna anger du artikeltransaktionen som transaktionsraden ska kopplas till, eller från. En fast koppling kan till exempel utföras när en kostnadskoppling skapas som anger att en försäljningsretur ska kopplas till en specifik utleverans, så att kostnaden för utleveransen kan återföras. I det här fallet ignorerar [!INCLUDE[d365fin](includes/d365fin_md.md)] värderingsprincipen i programmet och lagerminskningen, eller lagerökningen för en försäljningsretur, kopplas till den angivna artikeltransaktionen. Fördelen med fasta kopplingar är att kostnaden för den ursprungliga transaktionen överförs till den nya transaktionen.  

### <a name="example--fixed-application-in-purchase-return"></a>Exempel – Fast koppling i inköpsretur  
Följande exempel, som visar effekten av fast koppling på en inköpsretur av en artikel som använder FIFO-värderingsprincipen, baseras på följande scenariot:  

1. I transaktionen 1 bokför användaren ett inköp till en kostnad av BVA 10,00.  
2. I transaktionen 2 bokför användaren ett inköp till en kostnad av BVA 20,00.  
3. I transaktionen 3 bokför användaren en inköpsretur. Användaren skapar en fast koppling till det andra köpet genom att ange löpnumret för artikeltransaktionen i fältet **Koppla till artikellöpnr** på inköpsreturorderraden.  

Följande tabell visar artikeltransaktioner som är resultatet av scenariot.  

|**Bokföringsdatum**|**Artikeltransaktionstyp**|**Antal**|**Kost.belopp (aktuellt)**|**Artikeltrans.löpnr**|  
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
|01-04-20|Inköp|10|10.00|1|  
|01-05-20|Inköp|10|20.00|2|  
|01-06-20|Inköps(retur)|-10|-20.00|3|  

Eftersom en fast koppling skapas från inköpsreturen till den andra inköpstransaktionen, returneras artiklarna till rätt kostnad. Om användaren inte hade utfört den fasta kopplingen så skulle den returnerade artikeln vara felaktigt värderad till BVA 10,00, eftersom returen skulle ha kopplats till den första inköpsposten enligt FIFO-principen.  

Följande tabell visar den artikelkopplingstransaktion som härrör från den fasta kopplingen.  

|Bokföringsdatum|Ankommande artikeltrans.nr|Avgående artikeltrans.nr|Antal|Artikeltrans.löpnr|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-06-20|2|3|10|3|  

Kostnaden för det andra inköpet, 20,00 BVA, överförs då på ett korrekt sätt till inköpsreturen.  

### <a name="example--fixed-application-with-average-cost"></a>Exempel – Fast koppling med genomsnittskostnad  
Följande exempel, som visar effekten av fast koppling, baseras på följande scenario för en artikel som använder värderingsprincipen Genomsnitt:  

1. I löpnummer 1 och 2 bokför användaren två inköpsfakturor. Den andra fakturan har den felaktiga direkta styckkostnaden BVA 1 000,00.  
2. I löpnummer 3 bokför användaren en inköpskreditnota med en fast koppling som kopplas till inköpstransaktionen med fel direkt styckkostnad. Summan av fältet **Kostnadsbelopp (aktuellt)** för de två fast kopplade värdetransaktionerna blir 0,00  
3. I löpnummer 4 bokför användaren en annan inköpsfaktura med rätt direkt styckkostnad på BVA 100,00  
4. I löpnummer 5 bokför användaren en försäljningsfaktura.  
5. Lagerantalet är 0, och lagervärdet är också 0,00  

Följande tabell visar resultatet av scenariot på artikelns värdetransaktioner.  

|Bokföringsdatum|Artikeltransaktionstyp|Antal|Kost.belopp (aktuellt)|Koppla till artikellöpnr|Genomsnittligt|Artikeltrans.löpnr|Löpnr|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Inköp|1|200.00||Nr|1|1|  
|01-01-20|Inköp|1|1000.00||Nej|2|2|  
|01-01-20|Inköp|-1|-1 000|2|Nej|3|3|  
|01-01-20|Inköp|1|100,00||Nej|4|4|  
|01-01-20|Försäljning|-2|-300.00||Ja|5|5|  

Om användaren inte har gjort den fasta kopplingen mellan inköpskreditnotan och inköpet med den felaktiga direkta enhetskostnaden (moment 2 i föregående scenario), så skulle kostnaden ha justerats på ett annat sätt.  

Följande tabell visar resultatet på artikelns värdetransaktioner om moment 2 i föregående scenario utförs utan en fast koppling.  

|Bokföringsdatum|Artikeltransaktionstyp|Antal|Kost.belopp (aktuellt)|Koppla till artikellöpnr|Genomsnittligt|Artikeltrans.löpnr|Löpnr|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Inköp|1|200.00||Nr|1|1|  
|01-01-20|Inköp|1|1000.00||Nej|2|2|  
|01-01-20|Inköp|-1|433,33||Ja|3|3|  
|01-01-20|Inköp|1|100,00||Nej|4|4|  
|01-01-20|Försäljning|-2|866,67||Ja|5|5|  

I löpnummer 3 värderas värdet i fältet **Kostnadsbelopp (Aktuell)** genom genomsnitt och därför inkluderas den felaktiga bokföringen på 1000,00. På så sätt blir den -433,33, som är ett överdrivet kostnadsbelopp. Beräkningen är 1300 / 3 = .-433,33.  

I löpnummer 5 är värdet för fältet **Kostnadsbelopp (Aktuellt)** för den här transaktionen också felaktigt av samma anledning.  

> [!NOTE]  
>  Om en fast koppling skapas för en lagerminskning för en artikel med värderingsprincipen Genomsnitt, vidarebefordras inte artikelns genomsnittskostnad till minskningen som vanligt. I stället vidarebefordras den angivna kostnaden för lagerökningen. Lagerminskningen är då inte längre en del av beräkningen av genomsnittskostnad.  

### <a name="example--fixed-application-in-sales-return"></a>Exempel – Fast koppling i försäljningsretur  
Fasta kopplingar är också ett mycket bra sätt att återföra kostnad exakt, till exempel med försäljningsreturer.  

Följande exempel, som visar hur en fast koppling säkerställer exakt kostnadsåterföring, baseras på följande scenario:  

1.  Användaren bokför en inköpsfaktura.  
2.  Användaren bokför en försäljningsfaktura.  
3.  Användaren bokför en försäljningskreditnota för den returnerade artikeln, som gäller för försäljningstransaktionen, för att återföra kostnaden korrekt.  
4.  En fraktkostnad, som hör till inköpsordern som tidigare har bokförts, anländer. Användaren bokför det som en artikelomkostnad.  

Följande tabell visar resultatet av scenariomoment 1 till 3 på artikelns värdetransaktioner.  

|Bokföringsdatum|Artikeltransaktionstyp|Antal|Kost.belopp (aktuellt)|Koppla från artikellöpnr|Artikeltrans.löpnr|Löpnr|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Inköp|1|1000.00||1|1|  
|02-01-20|Försäljning|-1|1000.00||2|2|  
|03-01-20|Försäljning (kreditnota)|1|1000|2|3|3|  

Följande tabell visar värdetransaktionen som härrör från scenariomoment 4 som bokför artikelomkostnaden.  

|Bokföringsdatum|Artikeltransaktionstyp|Antal|Kost.belopp (aktuellt)|Koppla från artikellöpnr|Artikeltrans.löpnr|Löpnr|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|04-01-20|(Artikelomkostnad)|1|100.00||1|4|  

Följande tabell visar effekten av den exakta kostnadsåterföringen på artikelns värdetransaktioner.  

|Bokföringsdatum|Artikeltransaktionstyp|Antal|Kost.belopp (aktuellt)|Koppla från artikellöpnr|Artikeltrans.löpnr|Löpnr|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Inköp|1|1000.00||1|1|  
|02-01-20|Försäljning|-1|1100.00||2|2|  
|03-01-20|Försäljning (kreditnota)|1|1100.00|2|3|3|  
|04-01-20|(Artikelomkostnad)|1|100.00||1|4|  

När du kör batchjobbet **Justera kostnader - artikeltrans** vidarebefordras den ökade kostnaden för inköpstransaktionen, på grund av artikelomkostnaden, till försäljningstransaktionen (löpnummer 2). Försäljningsposten flyttar sedan fram den ökade kostnaden till försäljningskredittransaktionen (löpnummer 3). Det sista resultatet är att kostnaden återförs korrekt.  

> [!NOTE]  
>  Om du arbetar med returer eller kreditnotor och har konfigurerat fältet **Kräv exakt kostnadsåterföring** på antigen sidan **Inköpsinställningar** eller sidan **Försäljningsinställningar** (beroende på situation) kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] automatiskt att fylla i respektive inmatningsfält när du använder funktionen **Kopiera från dokument**. Om funktionen **Hämta bokförda dokumentrader som ska återföras** används fylls de här fälten alltid i automatiskt.  

> [!NOTE]  
>  Om en transaktion med en fast koppling bokförs och om artikeltransaktionen som kopplingen ska utföras till är stängd, d.v.s. om det återstående antalet är noll, återställs den gamla kopplingen automatiskt i programmet och artikeltransaktionen kopplas om med den angivna fasta kopplingen.  

## <a name="transfer-application"></a>Överföring koppling  
När en artikel överförs från en lagerplats till en annan, inom företagslagret, skapas en koppling mellan de två överföringstransaktionerna. Värderingen av en överföringstransaktion är beroende av värderingsprincipen. För artiklar som använder värderingsprincipen Genomsnitt sker värderingen med hjälp av genomsnittskostnaden i genomsnittskostnadsperioden där värderingsdatumet för överföring finns. För artiklar som använder andra värderingsprinciper sker värderingen genom att spåra baklänges till kostnaden för den ursprungliga lagerökningen.  

### <a name="example--average-costing-method"></a>Exempel – Metoden Genomsnittskostnad  
Följande exempel, som visas hur överföringstransaktioner används, baseras på följande scenario för en artikel som använder värderingsprincipen Genomsnitt och genomsnittskostnadsperioden Dag.  

1. Användaren köper artikeln till en kostnad av BVA 10,00.  
2. Användaren köper artikeln igen till en kostnad av BVA 20,00.  
3. Användaren överför artikeln från lagerställe BLÅ till RÖD.  

Följande tabell visar effekten av den överföringen på artikelns värdetransaktioner.  

|Bokföringsdatum|Artikeltransaktionstyp|Lagerställekod|Antal|Kost.belopp (aktuellt)|Löpnr|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Inköp|BLÅ|1|10.00|1|  
|01-01-20|Inköp|BLÅ|1|20.00|2|  
|02-01-20|Överföring:|BLÅ|-1|15,00|3|  
|02-01-20|Överföring:|RÖD|1|15,00|4|  

### <a name="example--standard-costing-method"></a>Exempel – Värderingsprincip Standard  
Följande exempel, som visar hur överföringstransaktioner används, baseras på följande scenario för en artikel som använder värderingsprincipen Standard och genomsnittskostnadsperioden Dag.  

1. Användaren köper artikeln till en standardkostnad på BVA 10,00.  
2. Användaren överför artiklar från lagerställe BLÅ till lagerställe RÖD med en standardkostnad på BVA 12,00.  

Följande tabell visar effekten av den överföringen på artikelns värdetransaktioner.  

|Bokföringsdatum|Artikeltransaktionstyp|Lagerställekod|Antal|Kost.belopp (aktuellt)|Löpnr|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Inköp|BLÅ|1|10.00|1|  
|02-01-20|Överföring|BLÅ|-1|10,00|2|  
|02-01-20|Överföring:|RÖD|1|10,00|3|  

Eftersom värdet för den ursprungliga lagerökningen är BVA 10,00, värderas överföringen till den kostnaden, och inte till BVA 12,00.  

## <a name="reapplication"></a>Omkopplingar  
På grund av sättet som en artikels styckkostnad beräknas på kan en felaktig artikelkoppling medföra att genomsnittskostnaden och styckkostnaden får oriktiga resultat. Följande scenarier kan orsaka felaktiga artikelkopplingar som kräver att du ångra artikelkopplingar och kopplar om artikeltransaktioner:  

* Användaren har glömt att göra en fast koppling.  
* En felaktig fast koppling har gjorts.  
* Du vill åsidosätta kopplingen som skapas automatiskt när du bokför, enligt artikelns värderingsprincip.  
* Du måste returnera en artikel som en försäljning redan har kopplats till manuellt, utan att använda funktionen **Hämta bokförda dokumentrader som ska återföras**, och du måste därför ångra kopplingen.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] erbjuder en funktionen för analysering och rättning av artikelkopplingar. Detta arbete utförs på sidan **Kopplingsformulär**.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Kända problem med artikelkopplingar](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)  
[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)  
[Designdetaljer: Genomsnittskostnad](design-details-average-cost.md)   
[Designdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
