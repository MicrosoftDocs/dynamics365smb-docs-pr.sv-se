---
title: Designdetaljer – Planeringsparametrar
description: I denna artikel beskrivs de olika planeringsparametrarna som du kan använda och hur de påverkar planeringssystemet.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/26/2023
ms.custom: bap-template
---
# Designdetaljer: Planeringsparametrar

I denna artikel beskrivs de olika planeringsparametrarna som du kan använda i [!INCLUDE[prod_short](includes/prod_short.md)].  

Hur planeringssystemet styr artikeltillförseln bestäms av olika inställningar på **Artikelkort**, **SKU** och **Produktionsinställningar**. I följande tabell förklaras hur de här inställningarna används i planeringen.  

|Syfte|Inställningar|
|-------------|---------------|
|Ange om artikeln ska planeras|Partiformningsmetod = Tom|
|Definiera när du ska beställa|Tidsenhet<br /><br /> Beställningspunkt<br /><br /> Säkerhetsledtid|
|Definiera hur mycket som ska beställas|Säkerhetslager<br /><br /> Partiformningsmetod:<br /><br /> -   Fast orderkvantitet plus beställningsantal<br />-   Maximalt antal plus Beställningsgräns<br />-   Order<br />-   Parti-för-parti|
|Optimera när och hur mycket som ska beställas|Omplaneringsperiod<br /><br /> Partiackumuleringsperiod<br /><br /> Utjämningsperiod|
|Ändra leveransorder|Min. partistorlek<br /><br /> Max. partistorlek<br /><br /> Partistorleksmultipel|
|Begränsa den planerade artikeln|Produktionsprincip:<br /><br /> -  Tillverka-Mot-Lager<br />- Tillverka-Mot-Order|

## Ange om artikeln ska planeras  

Om du vill inkludera en artikel eller lagerställeenhet i planeringsförfarandet måste du tilldela den en partiformningsmetod. I annat fall måste den planeras manuellt, till exempel med hjälp av funktionen orderplanering.  

## Definiera när du ska beställa  

Beställningsförslag släpps allmänt endast när den planerade tillgängliga kvantiteten har fallit till eller under ett visst antal. Återbeställningspunkten definierar kvantiteten. Annars kommer det att vara noll. Noll kan justeras genom att ange ett säkerhetslager. Om du definierar en säkerhetsledtid kommer förslaget att levereras under perioden för det förfallodatum som krävs.  

Fältet **Tidsenhet** används i partiformningsmetoder (**Fast orderkvantitet** och **Maximal kvantitet**). Lagernivån kontrolleras efter varje tidsenhet. Den första tidsenheten börjar på planeringsstartdatumet.  

> [!NOTE]  
> När beräkningen av tidsenheterna, ignorerar planeringssystemet eventuella ledig kalendrar som definieras i fältet **Baskalenderkod** på sidorna **företagsinformation** och **lagerställekort**.  

På sidan **Produktionsinställning** bör du ställa in standard säkerhetsledtiden till minst en dag. Förfallodatumet för efterfrågan kanske är känd, men inte den förfallotiden. Planerings schemana bakåt för att uppfylla bruttoefterfrågan. Om du inte definierar en säkerhetsledtid kan varorna komma in för sent för att uppfylla behovet.  

Fälten **omplaneringsperiod**, **partiackumuleringsperiod**, och **Utjämningsperiod** har också betydelse för att definiera när du ska beställa om. Mer information finns i [Optimera när och hur mycket som ska beställas](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

## Definiera hur mycket som ska beställas

Om planeringssystemet identifierar behovet att beställa om bestämma partiformningsmetoden när och hur mycket som ska beställas.  

Oberoende av partiformningsmetoden följer planeringssystemet vanligtvis den här logiken:  

1. Beräkna antalet i orderkalkylarket för att uppfylla den lägsta lagernivån för artikeln, vanligtvis säkerhetslagret. Om inget har angetts är den minsta lagernivån noll.  
2. Om det planerade tillgängliga lagret är lägre än säkerhetslagret föreslås bakåtplanerad leveransorder. Partistorlek fyller minst säkerhetslagret och kan ökas med icke-härledd efterfrågan inom tidsenheten genom partiformningsmetoden och per ordermodifierarna.  
3. Om det planerade lagret är på eller under beställningspunkten (som beräknas från ackumulerade ändringar inom tidsenheten) och över säkerhetslagrets antal, föreslås en framåtplanerad undantagsorder. Både bruttobehovet som ska uppfyllas och partiformningsmetoden fastställer partistorleken. Orderantalet uppfyller minst orderpunkten.  
4. Om det finns mer bruttobehov som förfaller före slutdatumet för det framåtplanerade orderkalkylarket, och det här behovet gör att det aktuella beräknade planerade tillgängliga lagret hamnar lägre än säkerhetslagret, ökas partistorleken för att fylla upp underskottet. Leveransorderkalkylarket schemaläggs sedan bakåt från förfallodatumet för den icke-härledda efterfrågan som skulle ha överskridit säkerhetslagret.  
5. Om fältet **Tidsenhet** inte är ifyllt kommer bara bruttoefterfrågan på samma förfallodatum att läggas till.  

### Partiformningsmetoder  

Följande partiformningsmetoder påverkar den kvantitet som ska beställas. Om du vill lära dig mer om partiformningsmetoder går du till [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md).  

|Partiformningsmetod|Description|  
|-----------------------|---------------------------------------|  
|**Fast orderkvantitet **|Orderantalet är minst lika med orderkvantiteten. Du kan öka antalet för att uppfylla efterfrågan eller önskad lagernivå. Den här partiformningsmetoden används vanligtvis med en beställningspunkt.|  
|**Maximalt antal **|Partistorlek beräknas för att uppfylla det maximal lagret. Om antalsändringar används kanske det maximala lagret överträds. Vi rekommenderar att du inte använder tidsenheten tillsammans med maximalt antal. Tidsenheten åsidosätts ofta. Den här partiformningsmetoden används vanligtvis med en beställningspunkt.|  
|**Order**|Partistorlek beräknas för att uppfylla varje enskild efterfråganshändelse och uppsättningen med efterfrågan-tillgång fortsätter att vara kopplad till körningen. Inga planeringsparametrar beaktas.|  
|**Parti-för-parti**|Antalet beräknas så att det uppfyller summan av efterfrågan som förfaller inom tidsenheten.|  

## Optimera när och hur mycket som ska beställas  

En planerare kan finjustera planeringsparametrar för att begränsa omplaneringsförslag, ackumulera efterfrågan (dynamiskt beställningsantal) eller för att undvika oviktiga planeringsåtgärder. Följande fält för hjälper till att optimera när och hur mycket som ska beställas.  

|Fält|Description|  
|---------------------------------|---------------------------------------|  
|**Omplaneringsperiod**|Detta fält bestämmer om åtgärdsmeddelande ska ändra tidpunkten för en befintlig order eller avbryta den och skapa en ny order. Den befintliga ordern omplaneras i en omplaneringsperiod före den aktuella leveransen och till en omplaneringsperiod efter den aktuella leveransen.<br><br>**Obs!** Denna parameter fungerar endast med partiformningsmetoden **parti-för-parti**.|  
|**Partiackumuleringsperiod**|Med partiformningsmetoden Parti-för-parti används detta fält för att ackumulera flera leveransbehov till en leveransorder. Från den första planerade tillgången samlas alla tillgångsbehov i den följande partiackumuleringsperioden i en tillgång, som placeras på datumet för den första tillgången. Efterfrågan utanför partiackumuleringsperioden omfattas inte av den här leveransen.|  
|**Utjämningsperiod**|Detta fält används för att undvika mindre omplanering av befintlig leverans ut i tid. Ändringar från leveransdatum till en utjämningsperiod från leveransdatum skapar inga åtgärdsmeddelanden.<br /><br /> Den max. avvikelseperioden anger en tidsperiod då du inte vill att planeringssystemet ska föreslå omplanering av befintliga leveransorder framåt. Den begränsar antal obetydliga omplaneringsförslag för befintliga leveranser till ett senare datum om det omplanerade datumet ligger inom den maximala avvikelseperioden.<br /><br /> Som ett resultat kommer en positiv delta mellan det föreslagna nya leveransdatumet och det ursprungliga leveransdatumet alltid att vara större än den utjämningsperioden.|  

> [!NOTE]
> Med partiformningsmetoden Parti-för-part måste värdet i fältet **partiackumuleringsperiod** vara lika med eller större än värdet i fältet **utjämningsperiod**. Annars minskas utjämningsperioden under planeringsrutinen så att den stämmer med partiackumuleringsperioden.  

Tidsplaneringen av omplaneringsperioden, utjämningsperiod och partiackumuleringsperioden baseras på ett leveransdatum. Tidsenheten baseras på planeringsstartdatumet, som visas i följande illustration.  

:::image type="content" source="media/supply_planning_5_time_bucket_elements.png" alt-text="Tidsenhetselement.":::

I följande exempel representerar de svarta pilarna befintlig tillgång (upp) och efterfrågan (ned). Röda, gröna och orange pilar är planeringsförslag.  

**Exempel 1**: Det ändrade datumet ligger utanför omplaneringsperioden, vilket innebär att den befintliga leveransen annulleras. En ny tillgång föreslås för att täcka behovet i partiackumuleringsperioden.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accumulation_period.png" alt-text="Omplanering och partiackumuleringsperioder.":::

**Exempel 2**: Det ändrade datumet ligger i omplaneringsperioden, vilket innebär att den befintliga leveransen planeras om. En ny tillgång föreslås för att täcka behovet utanför partiackumuleringsperioden.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png" alt-text="Omplaneringsperiod, partiackumuleringsperiod och omplanering.":::

**Exempel 3**: Det finns en efterfrågan i utjämningsperioden och tillgångsantalet i partiackumuleringsperioden matchar tillgångsantalet. Nästa behov har inte täckts och en ny tillgång föreslås.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accumulation_period.png" alt-text="Utjämningsperiod och partiackumuleringsperiod.":::

**Exempel 4**: Det finns en efterfrågan i utjämningsperioden och tillgången förblir på samma datum. Det aktuella leveransantalet täcker dock inte behovet i partiackumuleringsperiod. En åtgärd för att ändra kvantitet för den befintliga leveransordern föreslås.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png" alt-text="Utjämningsperiod, partiackumuleringsperiod och ändra antal.":::

**Standardvärden:** Standardvärdet i fältet **Tidsenhet** och de tre fälten för beställningsperiod är tomma. För alla fält utom fältet **Utjämningsperiod** betyder det 0D (noll dagar). Om fältet **Utjämningsperiod** är tomt, används det globala värdet i **Standard för utjämningsperiod** på sidan **Produktionsinställningar**.  

## Ändra leveransorder  

När orderkalkylarkets antal har beräknats kan en eller flera av ordermodifierarna kan justera det. Till exempel är den maximal partistorlek större än eller lika med det lägsta partistorlek, som är större än eller lika med ordermultipeln.  

Antalet minskas om det överskrider den maximal partistorleken. Sedan ökas den om den är nedanför den lägsta partistorleken. Slutligen avrundas den så att den motsvarar en viss partistorleksmultipel. Alla återstående antal använder samma justeringar tills den totala efterfrågan konverterats till orderförslag.  

## Begränsa artikeln  

Fältet **Produktionsprincip** på sidan **Artikelkort** definierar vilka andra order som MRP-beräkningen avser.  

Om alternativet **Tillverka-Mot-Lager** används rör beställningarna endast artikeln.  

Om alternativet **Tillverka-mot-Order** används analyserar planeringssystemet produktionsstrukturen för artikeln och skapar länkade orderförslag för de artiklar på lägre nivå som också definieras som tillverka-mot-order. Detta fortsätter så länge det finns tillverka-mot-order-artiklar i de fallande strukturerna.

## Använd lågnivåkoder för att hantera härledd efterfrågan

Använd lågnivåkoder för att skapa härledd efterfrågan för komponenter till de lägre nivåerna i strukturen. Om du vill lära dig mer om lågnivåkoder går du till [Artikelprioritet/lågnivå kod](design-details-central-concepts-of-the-planning-system.md#item-priority--low-level-code).

Du kan koppla en lägsta-nivå-kod till varje komponent i produktionsstrukturen eller den indragna strukturen. Slutmonteringsnivån betecknas som nivå 0, d.v.s. slutartikeln. Ju högre nummer en lägsta-nivå-kod har, desto längre ned i hierarkin finns artikeln. Exempelvis har alla slutartiklar lägsta-nivå-koden 0 och artiklar som ingår i monteringen av slutartiklar har lägsta-nivå-koden 1, 2, 3 o.s.v. Resultatet blir att planeringen av komponenter samordnas med behovet för alla artiklar och komponenter med högre lägsta-nivå-kod. När du beräknar en planering expanderas strukturen i planeringsförslaget och bruttobehoven för nivå 0 skickas nedåt i planeringsnivåerna som bruttobehov för nästa planeringsnivå.

På sidan **Produktionsinställningar**, använd växlingsknappen **Dynamisk lågnivåkod** för att ange om du direkt vill tilldela och beräkna lågnivåkoder för respektive komponent i produktstrukturen. Vid stora mängder data kan funktionen ha negativa effekter på programmets kapacitet, till exempel i samband med automatisk kostnadsjustering. Observera att detta inte är en retroaktiv funktion, varför det är en god idé att överväga användning av funktionen i förväg.

Istället för den automatiska beräkning som sker dynamiskt om fältet väljs kan du också köra batchjobbet **Beräkna lågnivåkod** från menyn **Tillverkning** genom att klicka på **Produktdesign**, **Beräkna lågnivåkod**.

> [!IMPORTANT]
> Om du inte aktiverar växlingsknappen **Dynamisk lågnivåkod** måste du köra batchjobbet **Beräkna lågnivåkod** innan du beräknar en försörjningsplan (batchjobbet **Beräkna plan**).  

> [!NOTE]
> Du aktiverar fältet **Dynamisk lågnivåkod** markeras ändras inte lägstanivåkoderna för komponentartiklar dynamiskt om en överordnad struktur tas bort eller anges som ocertifierad. Det kan då bli svårt att lägga till nya artiklar i slutet av produktionsstrukturen eftersom detta kan överskrida det maximala antalet lägstanivåkoder. För större produktionsstrukturer som uppnår gränsen för lägstanivåkod kan du köra batch-jobbet **Beräkna lägstanivåkod** ofta i syfte att bibehålla strukturen.  

## Se även  

[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)  
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]