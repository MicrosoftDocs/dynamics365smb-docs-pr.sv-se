---
title: Värderingsprinciper för designdetaljer
description: Det här ämnet beskriver hur värderingsprincipen påverkar hur faktiska eller budgeterade värden aktiveras och används i kostnadsberäkningen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="design-details-costing-methods"></a>Värderingsprinciper: för designdetaljer

Värderingsprincipen avgör om ett faktiskt eller budgeterat värde ska kapitaliseras och användas i kostnadsberäkningen. Tillsammans med bokföringsdatumet och sekvensen, påverkar värderingsprincipen också hur kostnadsflödet registreras.

> [!NOTE]
> Du kan inte ändra värderingsprincipen för en artikel om det finns artikeltransaktioner för artikeln. Mer information finns i [Designinformation: ändra värderingsprincipen för artiklar](design-details-changing-costing-methods.md).

Följande metoder stöds i [!INCLUDE[prod_short](includes/prod_short.md)]:  

| Värderingsprincip | Beskrivning | Används när |
|--|--|--|
| FIFO | En artikels styckkostnad är det verkliga värdet på en mottagen artikel, vald enligt FIFO-regeln.<br /><br /> Lagervärdering antas det att de första artiklarna in i lagret säljs först. | I affärsmiljöer där produktkostnaden är stabil.<br /><br /> (När priser stiger visar balansräkningen ett högre värde. Det betyder att skatteskuler ökar, men kreditpoängen och förmåga att låna kontant ökar.)<br /><br /> För artiklar med ett begränsat hållbarhetstid, eftersom de äldsta varorna måste säljas innan deras hållbarhetstid passerat. |
| LIFO (Sist in, först ut) | En artikels styckkostnad är det verkliga värdet på en mottagen artikel, vald enligt LIFO-regeln.<br /><br /> Lagervärdering antas det att de sista artiklarna in i lagret säljs först. | Tillåts inte i många länder/regioner, eftersom det kan användas för att dölja vinst.<br /><br /> (När priser vill stiger, minskas värdet på resultaträkningen. Det betyder att skatteskulder minskar, men din förmåga att låna kontant försämras.) |
| Genomsnitt | En artikels styckkostnad beräknas enligt den genomsnittliga styckkostnaden vid varje tidpunkt efter ett inköp.<br /><br /> Lagervärdering förutsätter förutsätts att alla lagerartiklar säljs samtidigt. | I affärsmiljöer där produktkostnaden inte är stabil.<br /><br /> När lager travas eller blandas samman och inte kan åtskiljas, till exempel kemikalier. |
| Specifikt | En artikels styckkostnad är den exakta kostnaden för mottagandet av den aktuella enheten. | I produktionen eller handel med enkelt härledas artiklar med i höga kostnadspris.<br /><br /> För artiklar som lyder under regler.<br /><br /> För artiklar med serienummer. |
| Standard | En artikels styckkostnad är förinställd baserad på uppskattning.<br /><br /> När den verkliga kostnaden senare realiseras, måste standardkostnaden justeras med den verkliga kostnaden via skillnadsvärden. | När kostnadskontroll är kritisk.<br /><br /> I upprepande produktion för att värdera kostnaderna för direkt material, direkt arbete och produktionsoverheadkostnad.<br /><br /> När det finns funktion och personal som underhåller standarder. |

Följande bild visar hur kostnader flödar via lagret för varje värderingsprincip.  

![Visualiserade värderingsmetoder.](media/design_details_inventory_costing_7_costing_methods.png "Visualiserade värderingsmetoder")  

Värderingsprinciper skiljer sig åt på sättet som de värderar lagerminskningar, och om de använder de faktiska kostnaderna eller standardkostnader som värderingsbas. Följande tabell förklarar de olika egenskaperna. (LIFO-metoden används inte eftersom den påminner om FIFO-metoden).  
<!--Old  table
|Category|FIFO|Average|Standard|Specific|  
|-|----------|-------------|--------------|--------------|  
|General characteristic|Easy to understand|Based on period options: **Day**/**Week**/**Month**/**Quarter**/**Accounting Period**.<br /><br /> Can be calculated per item or per item/location/variant.|Easy to use, but requires qualified maintenance.|Requires item tracking on both inbound and outbound transaction.<br /><br /> Typically used for serialized items.|  
|Application/Adjustment|Application keeps track of **the remaining quantity**.<br /><br /> Adjustment forwards costs according to quantity application.|Application keeps track of the **remaining quantity**.<br /><br /> Costs are calculated and forwarded per the **valuation date**.|Application keeps track of the **remaining quantity**.<br /><br /> Application is based on FIFO.|All applications are fixed.|  
|Revaluation|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item only.<br /><br /> Can be done backward in time.|Revalues invoiced and un-invoiced quantities.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|  
|Miscellaneous|If you back-date an inventory decrease, then existing entries are NOT reapplied to provide a correct FIFO cost flow.|If you back-date an inventory increase or decrease, then the average cost is recalculated, and all affected entries are adjusted.<br /><br /> If you change the period or calculation type, then all affected entries must be adjusted.|Use the **Standard Worksheet** page to periodically update and roll up standard costs.<br /><br /> Is NOT supported per SKU.<br /><br /> No historic records exist for standard costs.|You can use specific item tracking without using the Specific costing method. Then the cost will NOT follow the lot number, but the cost assumption of the selected costing method.|  
-->
<!--Table flipped for slightly better readability -->

||Allmänna egenskaper|Koppling/justering |Omvärdering|Diverse |
|-|---------|---------|---------|---------|
|**FIFO**     |Enkelt att förstå|Koppling håller reda på **det återstående antalet**.<br /><br /> Justering vidarebefordrar kostnader enligt antalskoppling. |Omvärderar endast fakturerat antal.<br /><br /> Kan utföras per artikel eller per artikeltransaktion.<br /><br /> Kan utföras bakåt i tiden.|Om du bakåtdaterar en lagerminskning kopplas befintliga transaktioner INTE om för att ge ett korrekt FIFO-kostnadsflöde.|
|**Genomsnitt**     |Baserat på periodalternativ: **Dag**/**Vecka**/**Månad**/**Kvartal**/**Bokföringsperiod**.<br /><br /> Kan beräknas per artikel eller per artikel/lagerställe/variant.|Koppling håller reda på **återstående antal**.<br /><br /> Kostnader beräknas och speditioneras per **värderingsdatum**. |Omvärderar endast fakturerat antal.<br /><br /> Kan endast utföras per artikel.<br /><br /> Kan utföras bakåt i tiden. |Om du bakåtdaterar en lagerökning eller lagerminskning beräknas genomsnittskostnaden om och alla transaktioner som påverkas justeras.<br /><br /> Om du ändrar perioden eller beräkningstypen måste alla påverkade transaktioner justeras.|
|**Standard**     |Enkelt att använda men kräver kvalificerat underhåll.|Koppling håller reda på **återstående antal**.<br /><br /> Koppling baseras på FIFO.|Omvärderar fakturerade och icke-fakturerade antal.<br /><br /> Kan utföras per artikel eller per artikeltransaktion.<br /><br /> Kan utföras bakåt i tiden.|Använd sidan **Standardformulär** för att regelbundet uppdatera och summera standardkostnader.<br /><br /> Stöds INTE per lagerställeenhet.<br /><br /> Inga historiska transaktioner finns för standardkostnader.|
|**Specifikt**     |Kräver artikelspårning på både inkommande och utgående transaktioner.<br /><br /> Används vanligtvis för artiklar med serienummer.|Alla kopplingar är fasta.|Omvärderar endast fakturerat antal.<br /><br /> Kan utföras per artikel eller per artikeltransaktion.<br /><br /> Kan utföras bakåt i tiden.|Du kan använda specifik artikelspårning utan att använda värderingsprincipen Specifik. Sedan följer kostnaden INTE partinumret, utan kostnadsantagandet för den valda värderingsprincipen.|

## <a name="example"></a>Exempel

Det här avsnittet ger exempel på hur olika värderingsprinciper påverkar lagervärdet.  

Följande tabell visar lagerökningarna och lagerminskningarna som exemplen baseras på.  

|Bokföringsdatum|Antal|Löpnr|  
|------------------|--------------|---------------|  
|01-01-20|1|1|  
|01-01-20|1|2|  
|01-01-20|1|3|  
|02-01-20|-1|4|  
|03-01-20|-1|5|  
|04-01-20|-1|6|  

> [!NOTE]  
> De resulterande antalet i lagret är noll. Därför måste lagervärdet också vara noll, oavsett vilken värderingsprincip som används.  

### <a name="effect-of-costing-methods-on-valuing-inventory-increases"></a>Effekt av värderingsprinciper på att värdering av lagerökningar

För artiklar med värderingsprinciper som använder faktiska kostnader som värderingsbas (**FIFO**, **LIFO**, **Genomsnitt** eller **Specifik**) värderas lagerökningar på artikelns anskaffningskostnad.  

- **Standard**  

    För artiklar som använder värderingsprincipen **Standard** värderas lagerökningar enligt artikelns aktuella standardkostnad.  

#### <a name="standard"></a>Standard

För artiklar som använder värderingsprincipen **Standard** värderas lagerökningar enligt artikelns aktuella standardkostnad.  

### <a name="effect-of-costing-methods-on-valuing-inventory-decreases"></a>Effekt av värderingsprinciper på att värdering av lagerminskningar

- **FIFO**  

    För artiklar med värderingsprincipen **FIFO** säljs artiklar som köptes först alltid först (löpnummer 3, 2 och 1 i det här exemplet). Lagerminskningar värderas enligt värdet av de första lagerökningarna.  

     KSV beräknas med hjälp av värdet på de första lageranskaffningarna.  

     Följande tabell visar hur lagerminskningar värderas för värderingsprincipen **FIFO**.  

    |Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Löpnr|  
    |------------------|--------------|----------------------------|---------------|  
    |02-01-20|-1|-10.00|4|  
    |03-01-20|-1|-20.00|5|  
    |04-01-20|-1|-30.00|6|  

- **LIFO**  

    För artiklar med värderingsprincipen **LIFO** säljs artiklar som köptes senast alltid först (löpnummer 3, 2 och 1 i det här exemplet). Lagerminskningar värderas enligt värdet av den senaste lagerökningen.  

     KSV beräknas med hjälp av värdet på de senaste lageranskaffningarna.  

     Följande tabell visar hur lagerminskningar värderas för värderingsprincipen **LIFO**.  

    |Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Löpnr|  
    |------------|--------|--------------------|---------|  
    |02-01-20|-1|-30.00|4|  
    |03-01-20|-1|-20.00|5|  
    |04-01-20|-1|-10.00|6|  

- **Genomsnitt**  

    För artiklar som använder värderingsprincipen **Genomsnitt** värderas lagerminskningar enligt ett vägt medeltal av återstående lager på det sista datumet i perioden för genomsnittskostnad som lagerminskningen bokfördes i. Mer information finns i [Designdetaljer: genomsnittskostnad](design-details-average-cost.md).  

     Följande tabell visar hur lagerminskningar värderas för värderingsprincipen **Genomsnitt**.  

    | Bokföringsdatum | Antal | Kost.belopp (aktuellt) | Löpnr |
    |--|--|--|--|
    | 02-01-20 | -1 | -20.00 | 4 |
    | 03-01-20 | -1 | -20.00 | 5 |
    | 04-01-20 | -1 | -20.00 | 6 |

- **Standard**  

    För artiklar med värderingsprincipen **Normal** värderas lagerminskningar på liknande sätt som värderingsprincipen **FIFO**, förutom att värderingen baseras på en standardkostnad och inte på den faktiska kostnaden.  

    Följande tabell visar hur lagerminskningar värderas för värderingsprincipen **Standard**.  

    |Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Löpnr|  
    |------------------|--------------|----------------------------|---------------|  
    |02-01-20|-1|-15.00|4|  
    |03-01-20|-1|-15.00|5|  
    |04-01-20|-1|-15.00|6|  

- **Specifik**  

    Värderingsprinciperna bygger på ett antagande om hur kostnadsflöden går från en lagerökning till en lagerminskning. Men om det finns mer exakt information om kostnadsflödet kan du åsidosätta detta antagande genom att skapa en fast koppling mellan transaktioner. En fast koppling skapar en länk mellan en lagerminskning och en viss lagerökning och leder kostnadflödet därefter.  

    För artiklar med värderingsprincipen **Specifik** värderas lagerminskningar enligt lagerökningen som de är kopplade till via den fasta kopplingen.  

    Följande tabell visar hur lagerminskningar värderas för värderingsprincipen **Specifik**.  

    |Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Kopplas till löpnr|Löpnr|
    |------------|--------|--------------------|----------------|---------|  
    |02-01-20|-1|-20.00|**2**|4|  
    |03-01-20|-1|-10.00|**1**|5|  
    |04-01-20|-1|-30.00|**3**|6|  

## <a name="see-also"></a>Se även

[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)  
[Designdetaljer: Varians](design-details-variance.md)  
[Designdetaljer: Genomsnittskostnad](design-details-average-cost.md)  
[Designdetaljer: Artikelkoppling](design-details-item-application.md)  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ord lista över termer i Dynamics 365 affärsprocesser](/dynamics365/guidance/business-processes/glossary)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
