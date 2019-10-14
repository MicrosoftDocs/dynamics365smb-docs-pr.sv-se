---
title: Designdetaljer - Värderingsprinciper | Microsoft Docs
description: Värderingsprincipen avgör om ett faktiskt eller budgeterat värde ska kapitaliseras och användas i kostnadsberäkningen. Tillsammans med bokföringsdatumet och sekvensen, påverkar värderingsprincipen också hur kostnadsflödet registreras.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6f009b0e43a3d3424782f5c3f052033c813e3f18
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303655"
---
# <a name="design-details-costing-methods"></a>Designdetaljer: Värderingsprinciper
Värderingsprincipen avgör om ett faktiskt eller budgeterat värde ska kapitaliseras och användas i kostnadsberäkningen. Tillsammans med bokföringsdatumet och sekvensen, påverkar värderingsprincipen också hur kostnadsflödet registreras.

> [!NOTE]
> Du kan inte ändra värderingsprincipen för en artikel om det finns artikeltransaktioner för artikeln.<br /><br />
> Information kommer snart att publiceras här om lösningar på hur du ändrar en värderingsprincip i särskilda situationer.

Följande metoder stöds i [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

|Värderingsprincip|Beskrivning|Används när|  
|--------------------|---------------------------------------|-----------------|  
|FIFO|En artikels styckkostnad är det verkliga värdet på en mottagen artikel, vald enligt FIFO-regeln.<br /><br /> I lagervärdering antas det att de första artiklarna in i lagret säljs först.|I affärsmiljöer där produktkostnaden är stabil.<br /><br /> (När priser stiger visar balansräkningen ett högre värde. Det betyder att skatteskuler ökar, men kreditpoängen och förmåga att låna kontant ökar.)<br /><br /> För artiklar med ett begränsat hållbarhetstid, eftersom de äldsta varorna måste säljas innan deras hållbarhetstid passerat.|  
|LIFO (Sist in, först ut)|En artikels styckkostnad är det verkliga värdet på en mottagen artikel, vald enligt LIFO-regeln.<br /><br /> I lagervärdering antas det att de senaste artiklarna in i lagret säljs först.|Tillåts inte i många länder/regioner, eftersom det kan användas för att dölja vinst.<br /><br /> (När priser vill stiger, minskas värdet på resultaträkningen. Det betyder att skatteskulder minskar, men din förmåga att låna kontant försämras.)|  
|Genomsnitt|En artikels styckkostnad beräknas enligt den genomsnittliga styckkostnaden vid varje tidpunkt efter ett inköp.<br /><br /> För lagervärdering förutsätts att alla lagerartiklar säljs samtidigt.|I affärsmiljöer där produktkostnaden inte är stabil.<br /><br /> När lager travas eller blandas samman och inte kan åtskiljas, till exempel kemikalier.|  
|Specifik|En artikels styckkostnad är den exakta kostnaden för mottagandet av den aktuella enheten.|I produktionen eller handel med enkelt härledas artiklar med i höga kostnadspris.<br /><br /> För artiklar som lyder under regler.<br /><br /> För artiklar med serienummer.|  
|Standard|En artikels styckkostnad är förinställd baserad på uppskattning.<br /><br /> När den verkliga kostnaden senare realiseras, måste standardkostnaden justeras med den verkliga kostnaden via skillnadsvärden.|När kostnadskontroll är kritisk.<br /><br /> I upprepande produktion för att värdera kostnaderna för direkt material, direkt arbete och produktionsoverheadkostnad.<br /><br /> När det finns funktion och personal som underhåller standarder.|  

 Följande bild visar hur kostnader flödar via lagret för varje värderingsprincip.  

 ![Värderingsprinciper](media/design_details_inventory_costing_7_costing_methods.png "Värderingsprinciper")  

 Värderingsprinciper skiljer sig åt på sättet som de värderar lagerminskningar, och om de använder de faktiska kostnaderna eller standardkostnader som värderingsbas. Följande tabell förklarar de olika egenskaperna. (LIFO-metoden används inte eftersom den påminner om FIFO-metoden).  

||FIFO|Genomsnitt|Standard|Specifik|  
|-|----------|-------------|--------------|--------------|  
|Allmänna egenskaper|Enkelt att förstå|Baserat på periodalternativ: **Dag**/**Vecka**/**Månad**/**Kvartal**/**Bokföringsperiod**.<br /><br /> Kan beräknas per artikel eller per artikel/lagerställe/variant.|Enkelt att använda men kräver kvalificerat underhåll.|Kräver artikelspårning på både ankommande och avgående transaktioner.<br /><br /> Används vanligtvis för artiklar med serienummer.|  
|Koppling/justering|Koppling håller reda på **det återstående antalet**.<br /><br /> Justering vidarebefordrar kostnader enligt antalskoppling.|Koppling håller reda på **återstående antal**.<br /><br /> Kostnader beräknas och speditioneras per **värderingsdatum**.|Koppling håller reda på **återstående antal**.<br /><br /> Koppling baseras på FIFO.|Alla kopplingar är fasta.|  
|Omvärdering|Omvärderar endast fakturerat antal.<br /><br /> Kan utföras per artikel eller per artikeltransaktion.<br /><br /> Kan utföras bakåt i tiden.|Omvärderar endast fakturerat antal.<br /><br /> Kan endast utföras per artikel.<br /><br /> Kan utföras bakåt i tiden.|Omvärderar fakturerade och icke-fakturerade antal.<br /><br /> Kan utföras per artikel eller per artikeltransaktion.<br /><br /> Kan utföras bakåt i tiden.|Omvärderar endast fakturerat antal.<br /><br /> Kan utföras per artikel eller per artikeltransaktion.<br /><br /> Kan utföras bakåt i tiden.|  
|Diverse|Om du bakåtdaterar en lagerminskning kopplas befintliga transaktioner INTE om för att ge ett korrekt FIFO-kostnadsflöde.|Om du bakåtdaterar en lagerökning eller lagerminskning beräknas genomsnittskostnaden om och alla transaktioner som påverkas justeras.<br /><br /> Om du ändrar perioden eller beräkningstypen måste alla påverkade transaktioner justeras.|Använd sidan **Standardformulär** för att regelbundet uppdatera och summera standardkostnader.<br /><br /> Stöds INTE per lagerställeenhet.<br /><br /> Inga historiska transaktioner finns för standardkostnader.|Du kan använda specifik artikelspårning utan att använda värderingsprincipen Specifik. Sedan följer kostnaden INTE partinumret, utan kostnadsantagandet för den valda värderingsprincipen.|  

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
>  De resulterande antalet i lagret är noll. Därför måste lagervärdet också vara noll, oavsett vilken värderingsprincip som används.  

### <a name="effect-of-costing-methods-on-valuing-inventory-increases"></a>Effekt av värderingsprinciper på att värdering av lagerökningar  
 **FIFO**/**LIFO**/**Genomsnitt**/**Specifik**  

 För artiklar med värderingsprinciper som använder faktiska kostnader som värderingsbas (**FIFO**, **LIFO**, **Genomsnitt** eller **Specifik**) värderas lagerökningar på artikelns anskaffningskostnad.  

 Följande tabell visar hur lagerökningar värderas för alla värderingsprinciper förutom **Standard**.  

|Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Löpnr|  
|------------------|--------------|----------------------------|---------------|  
|01-01-20|1|10,00|1|  
|01-01-20|1|20,00|2|  
|01-01-20|1|30,00|3|  

 **Standard**  

 För artiklar som använder värderingsprincipen **Standard** värderas lagerökningar enligt artikelns aktuella standardkostnad.  

 Följande tabell visar hur lagerökningar värderas för värderingsprincipen **Standard**.  

|Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Löpnr|  
|------------------|--------------|----------------------------|---------------|  
|01-01-20|1|15,00|1|  
|01-01-20|1|15,00|2|  
|01-01-20|1|15,00|3|  

### <a name="effect-of-costing-methods-on-valuing-inventory-decreases"></a>Effekt av värderingsprinciper på att värdering av lagerminskningar  
 **FIFO**  

 För artiklar med värderingsprincipen **FIFO** säljs artiklar som köptes först alltid först (löpnummer 3, 2 och 1 i det här exemplet). Lagerminskningar värderas enligt värdet av de första lagerökningarna.  

 KSV beräknas med hjälp av värdet på de första lageranskaffningarna.  

 Följande tabell visar hur lagerminskningar värderas för värderingsprincipen **FIFO**.  

|Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Löpnr|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-10.00|4|  
|03-01-20|-1|-20.00|5|  
|04-01-20|-1|-30.00|6|  

 **LIFO**  

 För artiklar med värderingsprincipen **LIFO** säljs artiklar som köptes senast alltid först (löpnummer 3, 2 och 1 i det här exemplet). Lagerminskningar värderas enligt värdet av den senaste lagerökningen.  

 KSV beräknas med hjälp av värdet på de senaste lageranskaffningarna.  

 Följande tabell visar hur lagerminskningar värderas för värderingsprincipen **LIFO**.  

|Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Löpnr|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-30.00|4|  
|03-01-20|-1|-20.00|5|  
|04-01-20|-1|-10.00|6|  

 **Genomsnitt**  

 För artiklar som använder värderingsprincipen **Genomsnitt** värderas lagerminskningar enligt ett vägt medeltal av återstående lager på det sista datumet i perioden för genomsnittskostnad som lagerminskningen bokfördes i. Mer information finns i [Designdetaljer: genomsnittskostnad](design-details-average-cost.md).  

 Följande tabell visar hur lagerminskningar värderas för värderingsprincipen **Genomsnitt**.  

|Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Löpnr|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-20.00|4|  
|03-01-20|-1|-20.00|5|  
|04-01-20|-1|-20.00|6|  

 **Standard**  

 För artiklar med värderingsprincipen **Normal** värderas lagerminskningar på liknande sätt som värderingsprincipen **FIFO**, förutom att värderingen baseras på en standardkostnad och inte på den faktiska kostnaden.  

 Följande tabell visar hur lagerminskningar värderas för värderingsprincipen **Standard**.  

|Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Löpnr|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-15.00|4|  
|03-01-20|-1|-15.00|5|  
|04-01-20|-1|-15.00|6|  

 **Specifik**  

 Värderingsprinciperna bygger på ett antagande om hur kostnadsflöden går från en lagerökning till en lagerminskning. Men om det finns mer exakt information om kostnadsflödet kan du åsidosätta detta antagande genom att skapa en fast koppling mellan transaktioner. En fast koppling skapar en länk mellan en lagerminskning och en viss lagerökning och leder kostnadflödet därefter.  

 För artiklar med värderingsprincipen **Specifik** värderas lagerminskningar enligt lagerökningen som de är kopplade till via den fasta kopplingen.  

 Följande tabell visar hur lagerminskningar värderas för värderingsprincipen **Specifik**.  

|Bokföringsdatum|Antal|Kost.belopp (aktuellt)|Kopplas till löpnr|Löpnr|  
|------------------|--------------|----------------------------|-----------------------|---------------|  
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
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
