---
title: Designdetaljer - Planeringsparametrar | Microsoft Docs
description: I det här avsnittet beskrivs de olika planeringsparametrar som du kan använda i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, design
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: aeafdd37a40d393fbb62501d67b14f3e351ea254
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807611"
---
# <a name="design-details-planning-parameters"></a>Designdetaljer: Planeringsparametrar
I det här avsnittet beskrivs de olika planeringsparametrarna som du kan använda i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Det sätt som planeringssystemet styr artikeltillgång bestäms av olika inställningar på artikelkortet eller lagerställeenheten, och inställningar i produktionskonfigurationen. Följande tabell visar hur parametrarna används för planering.  

|Syfte|Parameter|  
|-------------|---------------|  
|Ange om artikeln ska planeras|Partiformningsmetod = Tom|  
|Definiera när du ska beställa|Tidsenhet<br /><br /> Beställningspunkt<br /><br /> Säkerhetsledtid|  
|Definiera hur mycket som ska beställas|Säkerhetslager<br /><br /> Partiformningsmetod:<br /><br /> -   Fast orderkvantitet plus beställningsantal<br />-   Maximalt antal plus Beställningsgräns<br />-   Order<br />-   Parti-för-parti|  
|Optimera när och hur mycket som ska beställas|Omplaneringsperiod<br /><br /> Partiackumuleringsperiod<br /><br /> Utjämningsperiod|  
|Ändra leveransorder|Min. partistorlek<br /><br /> Max. partistorlek<br /><br /> Partistorleksmultipel|  
|Begränsa den planerade artikeln|Produktionsprincip:<br /><br /> -   Tillverka-Mot-Lager<br />-   Tillverka-Mot-Order|  

## <a name="define-if-the-item-will-be-planned"></a>Ange om artikeln kommer att planeras  
För att ta med en artikel/lagerställeenhet i planeringsprocessen måste den ha en partiformningsmetod, annars måste den planeras manuellt, till exempel funktionen med Orderplanering.  

## <a name="define-when-to-reorder"></a>Definiera när du ska beställa  
Beställningsförslag släpps allmänt endast när den planerade tillgängliga kvantiteten har fallit till eller under ett visst antal. Antalet definieras av beställningspunkten. Annars kommer det att vara noll. Noll kan justeras genom att ange ett säkerhetslager. Om användaren har definierat en säkerhetsledtid kommer den att orsaka kalkylarket ska levereras under perioden för det förfallodatum som krävs.  

Fältet **Tidsenhet** används i partiformningsmetoder (**Fast orderkvantitet** och **Maximalt antal**), där lagernivån kontrolleras efter varje tidsenhet. Den första tidsenheten börjar på planeringsstartdatumet.  

> [!NOTE]  
>  När beräkningen av tidsenheterna, ignorerar planeringssystemet eventuella ledig kalendrar som definieras i fältet **Baskalenderkod** på sidorna **företagsinformation** och **lagerställekort**.  

Standardsäkerhetsledtiden på sidan **Produktionsinställning** ska anges till minst en dag. Förfallodatumet för efterfrågan kanske är känd, men inte den förfallotiden. Planeringen schemalägger bakåt för att uppfylla bruttobehov och om ingen säkerhetsledtid definieras kan varorna anlända för sent för att uppfylla efterfrågan.  

Ytterligare tre periodfält för beställningscykel **omplaneringsperiod**, **partiackumuleringsperiod**, och **Utjämningsperiod**, har också betydelse för att definiera när du ska beställa om. Mer information finns i [Optimera när och hur mycket som ska beställas](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

## <a name="define-how-much-to-reorder"></a>Definiera hur mycket som ska beställas  
Om planeringssystemet identifierar behovet att beställa om används den angivna partiformningsmetoden för att bestämma när och hur mycket som ska beställas.  

Oberoende av partiformningsmetoden följer planeringssystemet vanligtvis den här logiken:  

1. Antalet i orderkalkylarket beräknas av för att uppfylla den angivna lägsta lagernivån för artikeln, vanligtvis säkerhetslagret. Om inget har angetts är den minsta lagernivån noll.  
2. Om det planerade tillgängliga lagret är lägre än säkerhetslagret föreslås bakåtplanerad leveransorder. Partistorlek fyller minst säkerhetslagret och kan ökas med icke-härledd efterfrågan inom tidsenheten genom partiformningsmetoden och per ordermodifierarna.  
3. Om det planerade lagret är på eller under beställningspunkten (som beräknas från ackumulerade ändringar inom tidsenheten) och över säkerhetslagrets antal, föreslås en framåtplanerad undantagsorder. Både bruttobehovet som ska uppfyllas och partiformningsmetoden fastställer partistorleken. Orderantalet uppfyller minst orderpunkten.  
4. Om det finns mer bruttobehov som förfaller före slutdatumet för det framåtplanerade orderkalkylarket, och det här behovet gör att det aktuella beräknade planerade tillgängliga lagret hamnar lägre än säkerhetslagret, ökas partistorleken för att fylla upp underskottet. Leveransorderkalkylarket schemaläggs sedan bakåt från förfallodatumet för den icke-härledda efterfrågan som skulle ha överskridit säkerhetslagret.  
5. Om fältet **Tidsenhet** inte är ifyllt kommer bara bruttoefterfrågan på samma förfallodatum att läggas till.  

     Ytterligare periodfält för beställningscykel spellar också en roll när man definierar hur mycket som ska beställa om: **omplaneringsperiod**, **partiackumuleringsperiod**, och **Utjämningsperiod**. Mer information finns i [Optimera när och hur mycket som ska beställas](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

### <a name="reordering-policies"></a>Partiformningsmetoder  
Följande partiformningsmetoder påverkar den kvantitet som ska beställas.  

|Partiformningsmetod|Beskrivning|  
|-----------------------|---------------------------------------|  
|**Fast orderkvantitet**|Orderantalet är minst lika med orderkvantiteten. Den kan ökas så att den uppfyller efterfrågan eller önskad lagernivå. Den här partiformningsmetoden används vanligtvis med en beställningspunkt.|  
|**Maximalt antal**|Partistorlek beräknas för att uppfylla det maximal lagret. Om antalsändringar används kanske det maximala lagret överträds. Vi rekommenderar att du inte använder tidsenheten tillsammans med maximalt antal. Tidsenheten åsidosätts ofta. Den här partiformningsmetoden används vanligtvis med en beställningspunkt.|  
|**Order**|Partistorlek beräknas för att uppfylla varje enskild efterfråganshändelse och uppsättningen med efterfrågan-tillgång fortsätter att vara kopplad till körningen. Inga planeringsparametrar beaktas.|  
|**Parti-för-parti**|Antalet beräknas så att det uppfyller summan av efterfrågan som förfaller inom tidsenheten.|  

##  <a name="optimize-when-and-how-much-to-reorder"></a>Optimera när och hur mycket som ska beställas  
För att få en rationell tillförselplan finjusterar en planerare planeringsparametrar för att begränsa omplaneringsförslag, ackumulera efterfrågan (dynamiskt beställningsantal) eller för att undvika oviktiga planeringsåtgärder. Följande periodfält för beställningscykel hjälper till att optimera när och hur mycket som ska beställas.  

|Fält|Beskrivning|  
|---------------------------------|---------------------------------------|  
|**Omplaneringsperiod**|Detta fält används för att bestämma om åtgärdsmeddelande ska ändra tidpunkten för en befintlig order eller avbryta den och skapa en ny order. Den befintliga ordern omplaneras i en omplaneringsperiod före den aktuella leveransen och till en omplaneringsperiod efter den aktuella leveransen.|  
|**Partiackumuleringsperiod**|Med partiformningsmetoden Parti-för-parti används detta fält för att ackumulera flera leveransbehov till en leveransorder. Från den första planerade tillgången samlas alla tillgångsbehov i den följande partiackumuleringsperioden i en tillgång, som placeras på datumet för den första tillgången. Efterfrågan utanför partiackumuleringsperioden omfattas inte av den här leveransen.|  
|**Utjämningsperiod**|Detta fält används för att undvika mindre omplanering av befintlig leverans ut i tid. Ändringar från leveransdatum till en utjämningsperiod från leveransdatum skapar inga åtgärdsmeddelanden.<br /><br /> Den max. avvikelseperioden anger en tidsperiod då du inte vill att planeringssystemet ska föreslå omplanering av befintliga leveransorder framåt. Den begränsar antal obetydliga omplaneringsförslag för befintliga leveranser till ett senare datum om det omplanerade datumet ligger inom den maximala avvikelseperioden.<br /><br /> Som ett resultat kommer en positiv delta mellan det föreslagna nya leveransdatumet och det ursprungliga leveransdatumet alltid att vara större än den utjämningsperioden.|  

Tidsplaneringen av omplaneringsperioden, utjämningsperiod och partiackumuleringsperioden baseras på ett leveransdatum. Tidsenheten baseras på planeringsstartdatumet, som visas i följande illustration.  

![Tidsenhetelement](media/supply_planning_5_time_bucket_elements.png "Tidsenhetelement")  

I följande exempel representerar de svarta pilarna befintlig tillgång (upp) och efterfrågan (ned). Röda, gröna och orange pilar är planeringsförslag.  

**Exempel 1**: Det ändrade datumet ligger utanför omplaneringsperioden, vilket innebär att den befintliga leveransen annulleras. En ny tillgång föreslås för att täcka behovet i partiackumuleringsperioden.  

![Omplaneringsperiod och partiackumuleringsperiod](media/supply_planning_5_recheduling_period_lot_accumulation_period.png "Omplaneringsperiod och partiackumuleringsperiod")  

**Exempel 2**: Det ändrade datumet ligger i omplaneringsperioden, vilket innebär att den befintliga leveransen planeras om. En ny tillgång föreslås för att täcka behovet utanför partiackumuleringsperioden.  

![Omplaneringsperiod, partiackumuleringsperiod och omplanera](media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png "Omplaneringsperiod, partiackumuleringsperiod och omplanera")  

**Exempel 3**: Det finns en efterfrågan i utjämningsperioden och tillgångsantalet i partiackumuleringsperioden matchar tillgångsantalet. Nästa behov har inte täckts och en ny tillgång föreslås.  

![Utjämningsperiod och partiackumuleringsperiod](media/supply_planning_5_dampener_period_lot_accumulation_period.png "Utjämningsperiod och partiackumuleringsperiod")  

**Exempel 4**: Det finns en efterfrågan i utjämningsperioden och tillgången förblir på samma datum. Dock är antalet för aktuell tillgång inte tillräckligt för att täcka efterfrågan i partiackumuleringsperioden, så en antalsändringsåtgärd för den befintliga leveransordern föreslås.  

![Utjämningsperiod, partiackumuleringsperiod och ändra antal](media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png "Utjämningsperiod, partiackumuleringsperiod och ändra antal")  

**Standardvärden:** Standardvärdet i fältet **Tidsenhet** och de tre fälten för beställningsperiod är tomma. För alla fält utom fältet **Utjämningsperiod** betyder det 0D (noll dagar). Om fältet **Utjämningsperiod** är tomt, används det globala värdet i **Standard för utjämningsperiod** på sidan **Produktionsinställningar**.  

## <a name="modify-the-supply-orders"></a>Ändra leveransorder  
När orderkalkylarkets antal har beräknats kan en eller flera av ordermodifierarna kan justera det. Till exempel är den maximal partistorlek större än eller lika med det lägsta partistorlek, som är större än eller lika med ordermultipeln.  

Antalet minskas om det överskrider den maximal partistorleken. Sedan ökas den om den är nedanför den lägsta partistorleken. Slutligen avrundas den så att den motsvarar en viss partistorleksmultipel. Alla återstående antal använder samma justeringar tills den totala efterfrågan konverterats till orderförslag.  

## <a name="delimit-the-item"></a>Begränsa artikeln  
Alternativet **Produktionsprincip** definierar vilka extra order nettobehovsberäkningen ska föreslå.  

Om alternativet **Tillverka-Mot-Lager** används rör beställningarna endast artikeln i fråga.  

Om alternativet **Tillverka-mot-Order** används kommer planeringssystemet att analysera produktionsstrukturen för artikeln och skapa ytterligare länkade som orderförslag för de artiklar på lägre nivå som också definieras som tillverka-mot-order. Detta fortsätter så länge det finns tillverka-mot-order-artiklar i de fallande strukturerna.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)
