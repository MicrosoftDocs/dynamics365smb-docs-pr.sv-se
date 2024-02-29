---
title: 'Sortera, söka och filtrera listor'
description: 'Arbeta effektivt i listor genom att söka i data, sortera kolumner och förfina resultaten med hjälp av filtersymboler och kortkommandon.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'delimit, FlowFilter, totals, limit, advanced'
ms.search.form: null
ms.date: 10/30/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="sorting-searching-and-filtering"></a>Sortera, söka och filtrera

Det finns några saker som du kan göra som hjälper dig att söka, hitta och begränsa poster i en lista eller i en rapport eller XMLport. Dessa inkluderar sortering, sökning och filtrering. Du kan använda några eller alla av dessa samtidigt för att snabbt söka efter och analysera data.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

För rapporter och XMLportar kan du, som i listor, ange filter för att begränsa vilka data som ska tas med i rapporten eller din XMLport, men du kan inte sortera eller söka.

> [!TIP]
> När du visar data sida vid sida kan du söka och använda filtrering. Om du vill använda alla kraftfulla funktioner för sortering, sökning och filtrering, väljer du ikonen ![Visa som lista](media/ui_show_as_list_icon.png "Visa som vänster listpil"). om du vill visa posterna som en lista.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Sortering

Med hjälp av sorteringsfunktionen kan du snabbt få en överblick över dina data. Om du har många kunder kan du till exempelsortera dem efter **Kundnr.**, **Valutakod** eller **Lands-/regionkod** för att få den översikt du behöver.

Om du vill sortera en lista kan du antingen:

- Välja en kolumnrubrikstext för att växla mellan stigande och fallande ordning, eller
- Välja listpilen i kolumnrubriken och sedan välja åtgärden **Stigande** eller **Fallande**.  

> [!NOTE]  
> Sortering stöds inte på bilder, BLOB-fält, FlowFilter och fält som inte tillhör samma tabell.  

## <a name="searching"></a>Sökning

<!--## Searching by using the Quick Filter -->
Högst upp på listsidan finns en ![Sök lista.](media/ui-search/search-list.png "Ikon för Söklista") Åtgärden **Sök** som ger ett snabbt och enkelt sätt att minska posterna i en lista och enbart visa de poster som innehåller de data som du är intresserad av att se.

Sök genom att helt enkelt markera åtgärden **Sök** och ange sedan den text som du vill söka efter i rutan. Du kan ange bokstäver, siffror och andra symboler.

Vanligtvis försöker sökningen matcha text i alla fält. Den skiljer inte mellan versaler och gemener (den är alltså skiftlägesokänslig) och matchar texten som placeras var som helst i fältet – i början, i slutet eller i mitten.

> [!TIP]
> Du kan välja <kbd>F3</kbd> för att aktivera och inaktivera sökrutan. Mer information finns i [Kortkommandon](keyboard-shortcuts.md#KeyboardFilter).

> [!NOTE]  
> Sökningen matchar inte värden i bilder, BLOB-fält, FlowFilter, FlowFields och andra fält som inte ingår i en tabell.


### <a name="fine-tuning-the-search-with-filter-criteria"></a>Finjustera sökningen med filtervillkor

Du kan göra en mer exakt sökning genom att använda filteroperatorer, uttryck och filter-token. Till skillnad från vid filtrering används dessa i alla fält när de används i sökrutan, vilket gör dem mindre effektiva än vid filtrering.

- För att hitta endast fältvärden som matchar hela texten och fallet exakt, placera söktexten mellan enskilda citat `''` (till exempel `'man'`).

- För att hitta fältvärden som börjar med en viss text och matchar gemener/versaler, placera `*` efter söktexten (till exempel `man*`).

- För att hitta fältvärden som slutar med en viss text och matchar gemener/versaler, placera `*` före söktexten (till exempel `*man`).

- Om du använder `''` eller `*` är sökningen skiftlägeskänslig. Om du vill göra sökningen skiftlägeskänsligt, placera `@` före texten (till exempel `@man*`).

I tabellen nedan finns några exempel som förklarar hur du kan använda sökningen.

|Sökkriterier|Söker efter...|
|---------------|----------|
|`man`<br />eller <br />`Man`|Alla poster med fält som innehåller texten **man**, oavsett gemener eller versaler. Till exempel **Manchester**, **manuell**, eller **Idrottsman**. |
|`'Man'`|Alla poster med fält som endast innehåller texten **Man** som matchar gemener eller versaler.|
|`Man*`|Alla poster med fält som börjar med texten <b>Man</b>, som matchar gemener eller versaler. Till exempel **Manchester** men inte **manuell**, eller **Idrottsman**.|
|`@Man*`|Alla poster med fält som börjar med texten **man** oavsett om de är gemener eller versaler. Till exempel **Manchester** och **manuell** men inte **Idrottsman**.|
|`@*man`|Alla poster som slutar med texten **man** oavsett om de är gemener eller versaler. Till exempel **Idrottsman** men inte **Manchester**, eller **manuell**.|


## <a name="filtering"></a><a name="filtering"></a>Filtrering

Filtrering ger ett mer avancerat och flexibelt sätt att kontrollera vilka poster som ska inkluderas i en lista, en rapport eller i XMLport. Det finns två stora skillnader mellan sökning och filtrering, enligt beskrivningen i följande tabell.

|| **Sökning** | **Filtrering** |
|--|----------|------------|
| **Tillämpliga fält** | Söker i alla fält som visas på sidan. | Filtrerar ett eller flera fält individuellt med val från något av fälten i tabellen, inklusive fält som inte visas på sidan. |
| **Matchning** | Visar poster med fält som matchar söktexten, oavsett versaler eller gemener i texten eller dess placering. | Visar poster där fältet matchar filtret exakt, inklusive skiftlägeskänsligheten, såvida inte särskilda filtersymboler har angetts.

Filtrering låter dig visa poster för specifika konton eller kunder, datum, belopp och annan information genom att ange filterkriterier. Endast poster som matchar kriteriet visas i listan eller tas med i rapporten, batch-jobbet eller XMLport. Om du anger kriterier för flera fält, kommer endast posterna som matchar alla kriterier att visas.

För listor visas filtren i ett filterfönster som visas till vänster om listan när du aktiverar den. För rapporter, batch-jobb och XMLport-kolumner visas filtren direkt på sidan för begäran.

### <a name="filtering-with-option-fields"></a>Filtrera med alternativfält

För "vanliga" fält som innehåller data, inställningsdatum eller affärsdata kan du ange filter både genom att markera data och genom att ange filtervärden, och du kan använda symboler för att definiera avancerade filterkriterier. Mer information finns i [Ange filtervillkor](ui-enter-criteria-filters.md#entering-filter-criteria).

För fält av typen **alternativ**kan du bara ange ett filter genom att välja ett eller flera alternativ i en listruta med tillgängliga alternativ. Ett exempel på ett alternativfält är fältet **status** på sidan **försäljningsorder**.

> [!NOTE]
> När du väljer flera alternativ som filtervärde definieras relationen mellan alternativen som *ELLER*. Om du till exempel markerar både kryssrutan **öppna** och **släppta** i fältet **status** på sidan **försäljningsorder** betyder det att försäljningsorder som antingen är öppna eller släppta visas.

### <a name="setting-filters-on-lists"></a>Ange filter för listor

I listor anger du filter genom att använda filterrutan. Om du vill visa filterrutan för en lista väljer du listpilen bredvid sidans namn och väljer sedan åtgärden **Visa filterruta**. Välj även <kbd>Shift</kbd>+<kbd>F3</kbd>.

Om du vill visa filterrutan för en kolumn på en lista väljer du listpilen bredvid och väljer sedan åtgärden **Filter**. Välj även <kbd>Shift</kbd>+<kbd>F3</kbd>. Filterrutan öppnas och den markerade kolumnen visas som ett filterfält i avsnittet **Filtrera lista efter**.

Filterrutan visar en lista över aktuella filter för en lista och gör att du kan ställa in egna anpassade filter på ett eller flera fält genom att välja åtgärden **+ Filter**.

 En filterruta är indelad i tre avsnitt: **Vyer**, **Filtrera lista efter** och **Filtrera summor efter**:

- **Vyer**

  Vissa listor inkluderar avsnittet **Vyer**. Vyer är varianter av listan som har förkonfigurerats med filter. Du kan definiera och spara hur många vyer du vill per lista. Vyerna blir tillgängliga för dig på alla enheter som du loggar in på. Mer information finns i avsnittet [Spara och anpassa listvyer](ui-views.md).

- **Filtrera lista efter**

  Det är i detta avsnitt som du lägger till filter på särskilda fält för att minska antalet visade poster. För att lägga till ett filter väljer du åtgärden **+ Filter**. Därefter anger du namnet på det fält som du vill filtrera listan efter eller väljer ett fält i listrutan.

- **Filtrera summor efter**

  Vissa listor som visar beräknade fält, till exempel belopp och kvantitet, inkluderar avsnittet **Filtrera summor efter** där du kan justera olika dimensioner som påverkar beräkningar. För att lägga till ett filter väljer du åtgärden **+ Filter**. Därefter anger du namnet på det fält som du vill filtrera listan efter eller väljer ett fält i listrutan.

  > [!NOTE]
  > Filter i avsnittet **Filtrera summor efter** styrs av FlowFilter på sidans design. Teknisk information finns i [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

Du kan ställa in ett enkelt filter direkt på en lista i med hjälp av filterrutan, nämligen ett filter som visar endast poster med samma värde som i den markerade cellen. Välj en cell på listan, välj listpilen bredvid och väljer sedan åtgärden **Filtrera på det här värdet**. Välj även <kbd>Alt</kbd>+<kbd>F3</kbd>.

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a>Ange filter i rapporter, batch-jobb och XMLport

För rapporter och XMLport-kolumner visas filtren direkt på sidan för begäran. På sidan för begäran visas de filter som används senast enligt ditt val i fältet **Använd standardvärden från**. Mer information finns i [Använda sparade inställningar](ui-work-report.md#SavedSettings).

I huvudavsnittet **filter** visas de standardfilterfält som du använder för att avgränsa vilka poster som ska ingå i rapporten or XMLport. För att lägga till ett filter väljer du åtgärden **+ Filter**. Därefter anger du namnet på det fält som du vill filtrera efter eller väljer ett fält i listrutan.

I avsnittet **Filtrera summor efter** kan du justera olika dimensioner som påverkar beräkningarna i rapporten eller XMLport. För att lägga till ett filter väljer du åtgärden **+ Filter**. Därefter anger du namnet på det fält som du vill filtrera efter eller väljer ett fält i listrutan.

## <a name="entering-filter-criteria"></a>Ange villkor i filter

Både i filterrutan och på sidan för förfrågan anger du filterkriterier i rutan under filterfältet.

Typen av filterfält som du vill filtrera avgör vilka kriterier du kan ange. Till exempel kommer filtrering av ett fält som har fasta värden bara låta dig välja mellan dessa värden. Mer information om särskilda filtersymboler finns i [Filterkriterier](#FilterCriteria) och [Filtertoken](#FilterTokens).

Kolumner som redan har filter som indikeras av ikonen ![filterikon.](media/ui-search/filter-icon.png "Filterikon") i kolumnrubriken. Om du vill ta bort ett filter på en sida klickar du på listpilen i sidrubriken och klickar sedan på åtgärden **Rensa filter**.

> [!TIP]
> Sök och analysera dina data snabbare genom att använda kombinationer av kortkommandon. Exempelvis markerar du ett fält, använder <kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>F3</kbd> om du vill lägga till fältet i filterrutan, skriver in filterkriteriet <kbd>Ctrl</kbd>+<kbd>Retur</kbd> om du vill återgå till raderna, markerar ett annat fält och använder <kbd>Alt</kbd>+<kbd>F3</kbd> för att filtrera det värdet. Mer information finns i [Kortkommandon](keyboard-shortcuts.md#KeyboardFilter).

### <a name="a-namefiltercriteria-afilter-criteria-and-operators"></a><a name="FilterCriteria"> </a>Filterkriterier och operatorer

När du anger kriterier kan du använda alla siffror och bokstäver som du normalt kan använda i fältet. Det finns emellertid även en uppsättning specialsymboler som du kan använda som operatorer för att ytterligare filtrera resultaten. I följande avsnitt beskrivs dessa symboler och hur du använder dem som operatorer i filter.

> [!TIP]
> Mer information om filtrering av datum och tider finns i [Arbeta med datum och tider i kalendrar](ui-enter-date-ranges.md).

> [!IMPORTANT]
> - Situationer kan uppstå där det värde du vill applicera filter på innehåller en symbol som är en operator. För mer information om hur du hanterar dessa situtioner, se [Filtrera värden som innehåller symboler](#symbols) för att få fler instruktioner kring hur situationen ska hanteras.
>
> - Om det finns fler än 200 operatorer i ett enda filter, systemet grupperar automatiskt några uttryck inom parenteser `()` i syfte att behandla det. Det påverkar inte filtret eller resultaten.  

#### <a name="-interval"></a>(..) Intervall

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`1100..2100`|Fr.o.m. 1100 t.o.m. 2100|  
|`..2500`|Alla t.o.m. 2500|  
|`..12 31 00`|Datum t.o.m. 00-12-31|  
|`Bicycle..Car`| Stringar Cykel genom bil när den beställs lexiografiskt|  
|`P8..`|Information för bokföringsperiod 8 och framåt|  
|`..23`|Från startdatumet till den 23 innevarande månad, innevarande år 23:59:59|  
|`23..`|Från 23 innevarande månad, innevarande år 0:00:00 till tidsperiodens slut|  
|`22..23`|Från 22 innevarande månad, innevarande år 0:00:00 till 23 innevarande månad, innevarande år 23:59:59| 

> [!TIP]
> Om du använder ett numeriskt tangentbord kan du använda decimal tecknet för att skriva ett tecken som inte är punkt (.). Om du vill växla till en punkt trycker du på tangenterna <kbd>Alt</kbd>+<kbd>decimalavgränsare</kbd> på det numeriska tangentbordet. När du vill växla tillbaka trycker du på <kbd>Alt</kbd>+<kbd>decimalavgränsare</kbd> igen. För mer information, se [Ange decimalavgränsare som används av numeriska tangentbord](ui-enter-data.md#decimal).

> [!NOTE]  
> Om fältet som du filtrerar på är av typen Text, används lexiografisk ordning för att avgöra vad som ingår i intervallet. För sådana fält som används för att lagra heltal kan detta leda till det (oväntade) resultatet att ett filter på 10000..10042 även inkluderar värdena 100000 och 1000042.

#### <a name="124-eitheror"></a>(&#124;) Antingen eller

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`1200|1300`|Nummer med 1200 eller 1300|  

#### <a name="-not-equal-to"></a>(<>) Inte lika med

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`<>0`|Alla nummer förutom 0<br /><br /> SQL-serveralternativet låter dig kombinera denna symbol med ett jokertecken. Till exempel betyder <>A* inte lika med valfri text som börjar med A.|  

#### <a name="-greater-than"></a>(>) Större än

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`>1200`|Nummer större än 1200|  

#### <a name="-greater-than-or-equal-to"></a>(>=) Större än eller lika med

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`>=1200`|Nummer större än eller lika med 1200|  

#### <a name="-less-than"></a>(<) Mindre än

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`<1200`|Nummer mindre än 1200|  

#### <a name="-less-than-or-equal-to"></a>(<=) Mindre än eller lika med

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`<=1200`|Nummer mindre än eller lika med 1200|  

#### <a name="-and"></a>(&) och

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`>200&<1200`|Nummer som är större än 200 och mindre än 1 200.|  

#### <a name="-an-exact-character-match"></a>('') En exakt teckenmatchning

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`'man'`|Text som matchar **man** exakt och är skiftlägeskänslig.|  
|`''`|Text som är tom.|  

#### <a name="-case-insensitive"></a>(@) Okänslig för skiftläge

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`@man*`|Text som börjar med **man** och är skiftlägesokänslig.|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Ett obestämt antal okända bokstäver

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`*Co*`|Text som innehåller **Co** och är skiftlägeskänslig.|  
|`*Co`|Text som slutar med **Co** och är skiftlägeskänslig.|  
|`Co*`|Text som börjar med **Co** och är skiftlägeskänslig.|  

#### <a name="-one-unknown-character"></a>(?) En okänd bokstav

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`Hans?n`|Text som exempelvis **Hansen** eller **Hanson**|  

#### <a name="combined-format-expressions"></a>Kombinerade formatuttryck

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Ta med post nummer 5999 och poster med nummer fr.o.m. 8100 t.o.m. 8490.|  
|`..1299|1400..`|Ta med poster med nummer mindre än eller lika med 1299 och nummer större än eller lika med 1400 (d.v.s. alla nummer utom 1300 t.o.m. 1399)|  
|`>50&<100`|Ta med poster med nummer större än 50 och mindre än 100 (d.v.s. nummer fr.o.m. 51 t.o.m. 99)|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a>Filtrera värden som innehåller symboler

Det kan finnas fall där fältvärden innehåller någon av följande symboler:

- &
- (
- )
- =
- &#124;

Om du vill filtrera efter någon av dessa symboler måste du placera filteruttrycket inom citattecken (`'<expression with symbol>'`). Om du exempelvis vill filtrera poster som börjar med texten *J & V* blir filteruttrycket `'J & V*'`.

Detta krav är inte nödvändigt för andra symboler.

### <a name="a-namefiltertokens-afilter-tokens"></a><a name="FilterTokens"> </a>Filtertoken

När du anger filterkriterier kan du även skriva ord som har en speciell betydelse som kallas filtertoken. När du har angett tokenordet, ersätts ordet med värden som det representerar. Filtertoken underlättar filtreringen genom att minska behovet av att gå till andra sidor för att söka efter värden som du vill lägga till i filtret. Tabellerna nedan beskriver några av de token som du kan skriva som filterkriterier.

> [!TIP]
> Ditt företag kanske använder egna token. För mer information om den fullständiga uppsättningen med token som finns tillgängliga för dig eller om du vill lägga till fler anpassade variabler, kontakta administratören. Teknisk information finns i [Lägga till filtertoken](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).

#### <a name="me-or-user-records-assigned-to-you"></a>(%me eller %userid) poster som har tilldelats dig

Använd `%me` eller `%userid` när du filtrerar i fält som innehåller användar-ID såsom fältet **Tilldelats användar-ID** om du vill visa alla poster som har tilldelats dig.

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`%me`<br />eller<br />`%userid`|Poster som är tilldelade till ditt användarkonto. |  

#### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Kunder i Mina kunder

Använd `%mycustomers` i fältet kund**nr** om du vill visa alla poster för kunder som ingår i listan **mina kunder** i ditt rollcenter.

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`%mycustomers`|Kunder i **mina kunder** i rollcentret. |  

#### <a name="myitems-items-in-my-items"></a>(%myitems) objekt i Mina objekt

Använd `%myitems` i fältet objekt**nr** om du vill visa alla poster för objekt som ingår i listan **mina objekt** i ditt rollcenter.

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`%myitems`|Objekt i **mina objekt** i rollcentret. |  

#### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Leverantörer i Mina leverantörer

Använd `%myvendors` i fältet leverantörs**nr** om du vill visa alla poster för leverantörer som ingår i listan **mina leverantörer** i ditt rollcenter.

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`%myvendors`|Leverantörer i **mina leverantörer** i rollcentret. |  

## <a name="see-also"></a>Se även

[Vanliga frågor och svar om sökning och filtrering](ui-search-filter-faq.yml)  
[Spara och personanpassa listvyer](ui-views.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
