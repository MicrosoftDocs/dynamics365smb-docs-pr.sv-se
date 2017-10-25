---
title: "Söka efter data och ange filterkriterier | Microsoft Docs"
description: "Beskriver hur du arbetar med filter, till exempel snabbfiltret för att förfina resultaten när du söker efter data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11d7ef56e980ba263dba6328b2f2f08b86410242
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="searching-filtering-and-sorting-data"></a>Söka, filtrera och sortera data
Det finns några saker som du kan göra som hjälper dig att hitta, precisera och skanna poster i en lista. Dessa inkluderar sortering, sökning och filtrering.

När du vill söka efter data, till exempel kundnamn, adresser eller produktgrupper, anger du kriterier. I sökkriterier kan du använda alla siffror och bokstäver som du normalt kan använda i det specifika fältet. Dessutom kan du använda specialtecken som du vill filtrera resultatet ytterligare. Det finns två sätt att söka: använda snabbfilter eller kolumn filtren.

## <a name="sorting"></a>Sortering
Med hjälp av sorteringsfunktionen kan du snabbt få en överblick över dina data. Om t.ex. har många kunder kan du sortera dem efter **Kundnr.**, **Kundbokföringsmall**, **Valutakod**, **Lands-/regionkod**, eller **Momsregistreringsnr.** för att få den översikt som du behöver.

Om du vill sortera en lista, kan du välja en kolumn rubriktexten för att växla mellan stigande och fallande ordning, eller välja små listrutor pilen i kolumnrubriken och välj **stigande** eller **fallande**.  

> [!NOTE]  
>   Sortering stöds inte på bilder, BLOB-fält, Flowfilter och fält som inte tillhör samma tabell.  

## <a name="searching-by-using-the-quick-filter"></a>Sök genom att använda snabbfiltret
Du kan lägga till filter för alla sidor genom att använda snabbfiltret. Snabbfiltret aktiveras genom att välja ikonen med förstoringsglas i det övre högra hörnet av en sida. Filtrering av den här typen används för att snabbt ange kriterier.

> [!IMPORTANT]  
>   Snabbfiltret ger enkelt tillgång till filterdata genom att ange vanlig text, men ger även många alternativet för sökningkriterier. Beroende på om du anger vanlig text, eller text inklusive symboler, uppför sig snabbfiltret på olika sätt.  

* Om du anger vanlig text i sökkriterierna tolkas sökkriterierna som en skiftlägesokänslig sökning som innehåller viss text.  
* Om du anger en text inklusive symboler i sökkriterierna tolkas sökkriterierna exakt som du har angett den, och sökningen är skiftlägeskänslig.

### <a name="quick-filter-criteria"></a>Snabbfilterkriterium
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Sökkriterier</TH>
    <TH>Tolkat som…</TH>
    <TH>Returer...</TH>
  </TR>
  <TR>
    <TD>tillverk</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Alla transaktioner som innehåller texten <b>man</b> och är skiftlägesokänsliga.</TD>
  </TR>
  <TR>
    <TD>sö</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Alla transaktioner som innehåller texten <b>se</b> och är skiftlägesokänsliga.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Börjar med <b>Man</b> och är skiftlägeskänsligt.</TD>
    <TD>Alla poster som börjar med texten <b>Man</b>.</TD>
  </TR>
  <TR>
    <TD>'tillverk'</TD>
    <TD>En exakt text och är skiftlägeskänsligt.</TD>
    <TD>Alla poster som matchar <b>man</b> exakt.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Börjar med och skiftlägesokänsligt.</TD>
    <TD>Alla poster som börjar med <b>man</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Slutar på och är skiftlägesokänsligt.</TD>
    <TD>Alla poster som slutar på <b>man</b>.</TD>
  </TR>
</TABLE>

> [!NOTE]  
>   Du kan inte använda ett jokertecken när du filtrerar på uppräkningsfält, t.ex fältet **Status** på försäljningsorder. För att ange ett filter för den här typen av fält kan du ange det numeriska värdet som en filtreringsparameter. Använd till exempel värdena **0**, **1**, **2** och **3** för att filtrera för dessa alternativ i fältet **Status** på en försäljningsorder, som har värdena **Öppna**, **Släppt**, **Väntar på godkännande** och **Väntar på förskottsbetalning**. 

## <a name="searching-by-using-column-filters"></a>Söka med hjälp av kolumnfilter
Du kan lägga till ett filter för en eller flera kolumner i en lista. Filtrera efter kolumner är mer flexibelt och bättre än snabbfiltret. 

### <a name="to-add-a-filter-on-a-column"></a>Lägga till ett filter på en kolumn
1.  Innan du lägger till ett filter kan du välja ![visa som lista](media/ui_show_as_list_icon.png "Visa som lista VÄNSTERPIL") om du vill ändra i vyn lista.
2. Välj den nedåt pilen i kolumnrubriken och välj **Filter**.
3. Gör något av följande: 
  -  Välj *...* bredvid rutan Välj ett värde i listan.
  -  Ange filtervillkor i rutan Se avsnittet Mer information.
4. Välj knappen **OK**.

## <a name="filter-criteria-and-symbols"></a>Filterkriterier och symboler
När du anger kriterier kan du använda alla siffror och bokstäver som du normalt kan använda i fältet. Dessutom kan du använda specialtecken som du vill filtrera resultatet ytterligare. I tabellen nedan visas de symboler som kan användas i filter.  
  
> [!IMPORTANT]  
>  Det kan finnas fall där fältvärdena innehåller dessa symboler och du vill filtrera efter de. Genom att ibland behöva du inkludera det filteruttryck som innehåller symbolen med citattecken (”). Om du vill filtrera poster som börjar med texten till exempel *S&R*, är filteruttrycket **S&R*'**.  
  
### <a name="-interval"></a>(..) Intervall  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|1100..2100|Fr.o.m. 1100 t.o.m. 2100|  
|..2500|Alla t.o.m. 2500|  
|..12 31 00|Datum t.o.m. 00-12-31|  
|P8..|Information för bokföringsperiod 8 och framåt|  
|..23|Från startdatumet till den 23 innevarande månad, innevarande år 23:59:59|  
|23..|Från 23 innevarande månad, innevarande år 0:00:00 till tidsperiodens slut|  
|22..23|Från 22 innevarande månad, innevarande år 0:00:00 till 23 innevarande månad, innevarande år 23:59:59|  
  
### <a name="124-eitheror"></a>(&#124;) Antingen/eller  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|1200&#124;1300|Nummer med 1200 eller 1300|  
  
### <a name="-not-equal-to"></a>(<>) Inte lika med  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|<>0|Alla nummer förutom 0<br /><br /> SQL-serveralternativet låter dig kombinera tecknet med ett jokertecken. Till exempel betyder <>A* inte lika med valfri text som börjar med A.|  
  
### <a name="-greater-than"></a>(>) Större än  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|>1200|Nummer större än 1200|  
  
### <a name="-greater-than-or-equal-to"></a>(>=) Större än eller lika med  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|>=1200|Nummer större än eller lika med 1200|  
  
### <a name="-less-than"></a>(<) Mindre än  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|<1200|Nummer mindre än 1200|  
  
### <a name="-less-than-or-equal-to"></a>(<=) Mindre än eller lika med  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|<=1200|Nummer mindre än eller lika med 1200|  
  
### <a name="-and"></a>(&) och  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|>200&<1200|Nummer som är större än 200 och mindre än 1 200.|  
  
### <a name="-an-exact-character-match"></a>('') En exakt teckenmatchning  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|'tillverk'|Text som matchar man exakt och är skiftlägeskänslig.|  
  
### <a name="-case-insensitive"></a>(@) Okänslig för skiftläge  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|@man*|Text som börjar med man och är skiftlägesokänslig.|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Ett obestämt antal okända bokstäver  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|*Co*|Text som innehåller ”Co” och är skiftlägeskänsligt.|  
|*co|Text som slutar med ”Co” och är skiftlägeskänsligt.|  
|co*|Text som börjar med ”Co” och är skiftlägeskänsligt.|  
  
### <a name="-one-unknown-character"></a>(?) En okänd bokstav  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|Hans?n|Text som exempelvis Hansen eller Hanson|  
  
### <a name="combined-format-expressions"></a>Kombinerade uttryck  
  
|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|5999&#124;8100..8490|Ta med post nummer 5999 och poster med nummer fr.o.m. 8100 t.o.m.|  
|..1299&#124;1400..|Ta med poster med nummer mindre än eller lika med 1299 och nummer större än eller lika med 1400 (d.v.s. alla nummer utom 1300 t.o.m.|  
|>50&<100|Ta med poster med nummer större än 50 och mindre än 100 (d.v.s. nummer fr.o.m. 51 t.o.m.|  
 
## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

