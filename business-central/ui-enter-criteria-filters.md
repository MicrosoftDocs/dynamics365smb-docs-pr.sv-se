---
title: "Sortering, sökning och filtrering av listor | Microsoft Docs"
description: "Arbeta effektivt i listor genom att söka i data, sortera kolumner och förfina resultaten med hjälp av kraftfulla filtersymboler och kortkommandon."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: f0cdb045d314a630e795ec744f2f4470d930835a
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="sorting-searching-and-filtering-lists"></a>Sortera, söka och filtrera listor
Det finns några saker som du kan göra som hjälper dig att söka, hitta och begränsa poster i en lista. Dessa inkluderar sortering, sökning och filtrering. Du kan använda några eller alla av dessa samtidigt för att snabbt söka efter och analysera data.

> [!TIP]
> När du visar data sida vid sida kan du söka och använda enkel filtrering. Om du vill använda alla kraftfulla funktioner för sortering, sökning och filtrering, väljer du ikonen ![Visa som lista](media/ui_show_as_list_icon.png "Visa som lista vänsterpil") om du vill visa en lista.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Sortering
Med hjälp av sorteringsfunktionen kan du snabbt få en överblick över dina data. Om t.ex. har många kunder kan du sortera dem efter **Kundnr.**, **Kundbokföringsmall**, **Valutakod**, **Lands-/regionkod**, eller **Momsregistreringsnr.** för att få den översikt som du behöver.

Om du vill sortera en lista, kan du välja en kolumn rubriktexten för att växla mellan stigande och fallande ordning, eller välja små listrutor pilen i kolumnrubriken och välj **stigande** eller **fallande**.  

> [!NOTE]  
>   Sortering stöds inte på bilder, BLOB-fält, Flowfilter och fält som inte tillhör samma tabell.  

## <a name="searching"></a>Sökning
<!--## Searching by using the Quick Filter -->Högst upp på varje listsida finns ikonen ![söklista](media/ui-search/search-list.png "ikonen söklista")**Sök** som är ett snabbt och enkelt sätt att minska posterna i en lista och enbart visa de poster som innehåller de data som du är intresserad av att se.

Sök genom att bara markera sökikonen och skriv den text som du vill söka efter i rutan. Du kan ange bokstäver, siffror och andra symboler.

### <a name="fine-tune-the-search"></a>Finjustera sökningen
I allmänhet försöker sökningen att matcha texten i alla fält. Den skiljer inte mellan versaler och gemener (d.v.s. skiftlägeskänslig) och matchar texten som placeras var som helst i fältet (i början, slutet eller i mitten).

Men du kan göra en mer exakt sökning med hjälp av följande tecken:

- För att hitta endast fältvärden som matchar hela texten och fallet exakt, placera söktexten mellan enskilda citat `''` (till exempel `'man'`).

- För att hitta fältvärden som börjar med en viss text och matchar gemener/versaler, placera `*` efter söktexten (till exempel `man*`).

- För att hitta fältvärden som slutar med en viss text och matchar gemener/versaler, placera `*` före söktexten (till exempel `*man`).

- Om du använder `''`eller `*`, är sökningen skiftlägeskänslig. Om du vill göra sökningen skiftlägeskänsligt, placera `@` före texten (till exempel `@man*`).

I tabellen nedan finns några exempel som förklarar hur du kan använda sökningen.


<!--
In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.-->

<!--
The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options. Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.  

* If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.  
* If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.
-->
<!--

|Search Criteria|Interpreted as...|Finds...|
|---------------|----------------|----------|
|`man`<br />or <br />`Man`|Contains the text; case insensitive|All records with fields that contain the text **man**, regardless of the case.|
|`'Man'`|Entire text match; case sensitive.|All records with fields that only contain **Man** exactly.|
|`Man*`|Starts with the text; case sensitive.|All records with fields that start with the text <b>Man</b> exactly.|
|`@Man*`|Starts with the text; case insensitive.|All records with fields that start with **man**, regardless of the case.|
|`@*man`|Ends with the text; case insensitive.|All records that end with **man**, regardless of the case.|
-->

|Sökkriterier|Söker efter...|
|---------------|----------|
|`man`<br />eller <br />`Man`|Alla poster med fält som innehåller texten **man**, oavsett gemener eller versaler. Till exempel **Manchester**, **manuell**, eller **Idrottsman**. |
|`'Man'`|Alla poster med fält som endast innehåller texten **Man** som matchar gemener eller versaler.|
|`Man*`|Alla poster med fält som börjar med texten <b>Man</b>, som matchar gemener eller versaler. Till exempel **Manchester** men inte **manuell**, eller **Idrottsman**.|
|`@Man*`|Alla poster med fält som börjar med texten **man** oavsett om de är gemener eller versaler. Till exempel **Manchester** och **manuell** men inte **Idrottsman**.|
|`@*man`|Alla poster som slutar med texten **man** oavsett om de är gemener eller versaler. Till exempel **Idrottsman** men inte **Manchester**, eller **manuell**.|

> [!TIP]
> Du kan trycka på F3 för att aktivera och avaktivera sökrutan. Mer information finns i [Kortkommandon](keyboard-shortcuts.md#KeyboardFilter).

## <a name="filtering"></a>Filtrering
Filtrering ger ett mer avancerat och flexibelt sätt att kontrollera vilka poster som ska visas i en lista. Det finns två stora skillnader mellan sökning och filtrering, enligt beskrivningen i följande tabell.

|| **Sökning** | **Filtrering** |
|--|----------|------------|
| **Tillämpliga fält** | Söker i alla fält som visas på sidan. | Filtrerar ett eller flera fält individuellt med val från något av fälten i tabellen, inklusive fält som inte visas på sidan. |
| **Matchning** | Visar poster med fält som matchar söktexten, oavsett versaler eller gemener eller placeringen av texten. | Visar poster där fältet matchar filtret exakt och är skiftlägeskänsliga, om inte särskilda filtersymboler har angetts.

Filtrering låter dig visa poster för specifika konton eller kunder, datum, belopp och annan information genom att ange filterkriterier. Bara poster som matchar kriteriet visas. Om du anger kriterier för flera fält, kommer endast posterna som matchar alla kriterier att visas.

### <a name="working-in-the-filter-pane"></a>Arbeta i filterrutan
Filterrutan visar en lista över aktuella filter för en lista och gör att du kan ställa in egna anpassade filter på ett eller flera fält. I bilden nedan visas ett exempelfilterfönster för en lista med försäljningsofferter.

![Översikt över filterruta](media/filter-pane-overview.png "Filterikon")

Om du vill visa filterrutan, använd kortkommandot **Shift + F3**. För listor i Rollcenter kan du också välja den nedåtriktade pilen bredvid en rubrik i fältet ovanför listan och väljer sedan **visa filterruta**.

![Visa filterruta](media/open-filter-pane.png "Visa filterruta")

En filterruta är indelad i tre avsnitt: **Vyer**, **Filtrera lista efter** och **Filtrera summor efter**:

- **Vyer**

  Vissa listor inkluderar avsnittet **Vyer**. Vyer är varianter av listan som har förkonfigurerats med filter. Om du vill växla till en annan vy i listan, markerar du bara en annan länk. Du kan tillfälligt ändra filter i en vy, men ändringarna kommer inte att sparas permanent.

- **Filtrera lista efter**

  Avsnittet **Filtrera listan efter** är där du lägger till filter på särskilda fält för att minska antalet visade poster. Om du vill lägga till ett filter, markera **+ Filter**, välj fältet som du vill filtrera från något fält i tabellen och ange sedan filterkriterierna i rutan.

- **Filtrera summor efter**

  Vissa listor som visar beräknade fält, till exempel belopp och kvantitet, inkluderar avsnittet **Filtrera summor efter** där du kan justera olika dimensioner som påverkar beräkningar. Till exempel kan du snabbt analysera din kontoplan genom att filtrera belopp till en viss period eller du kan visa summor för försäljningsorder bara från ett visst lagerställe.

  Lägg till ett filter genom att markera **+ Filter**, välj en av de fördefinierade dimensionerna och ange filterkriterierna i rutan.

  > [!NOTE]
  > Filter i avsnittet **Filtrera summor efter** styrs av FlowFilter på sidans design. Teknisk information finns i [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).


### <a name="entering-filter-criteria-in-the-filter-pane"></a>Ange filterkriterier i filterrutan
Gör något av följande för att välja ett fält att filtrera:
  - Välj **+ Fält** i filterrutan. Skriv namnet på det fält som du vill filtrera eller välj ett fält från menyn som visar alla fält i tabellen.

  - Välj nedpilen i en kolumnrubrik och välj **Filter...**. Detta öppnar filterfönstret och lägger till kolumnen i filterrutan.

Du kan nu skriva eller välja filterkriterier i rutan. Typen av fält som du vill filtrera avgör vilka kriterier du kan ange. Till exempel kommer filtrering av ett fält som har fasta värden bara låta dig välja mellan dessa värden. Mer information om särskilda filtersymboler finns i [Filterkriterier](#FilterCriteria) och [Filtertoken](#FilterTokens).

Kolumner som redan har filter som indikeras av ![filterikon](media/ui-search/filter-icon.png "filterikon") i kolumnrubriken. Om du vill ta bort ett filter, markera kolumnrubriken och välj **Ta bort filter**.


### <a name="entering-filter-criteria-without-the-filter-pane"></a>Ange filterkriterier utan filterrutan
Du kan ange enkla filter direkt i listan utan att behöva använda filterrutan.
Med något fält valt på en rad, använd kortkommandot **Alt + F3** för att endast visa de poster som har samma värde. Du kan sedan välja ett annat fält och använda samma kortkommando igen för att fortsätta att förfina dina filter. Om det markerade fältet redan är filtrerat kommer **Alt + F3** att ta bort filtret.

> [!TIP]
> Sök och analysera dina data snabbare genom att använda kombinationer av kortkommandon. Exempelvis markerar du ett fält, använder **Skift + Alt + F3** om du vill lägga till fältet i filterrutan, använder **Ctrl + Retur** om du vill återgå till raderna, markerar ett annat fält och använder **Alt + F3** för att filtrera det värdet.
Mer information finns i [Kortkommandon](keyboard-shortcuts.md#KeyboardFilter).


## <a name="FilterCriteria"> </a>Filterkriterier och symboler
När du anger kriterier kan du använda alla siffror och bokstäver som du normalt kan använda i fältet. Dessutom kan du använda specialtecken som du vill filtrera resultatet ytterligare. I tabellen nedan visas de symboler som kan användas i filter. För datum och tid kan du också se [Arbeta med kalenderdatum och tider](ui-enter-date-ranges.md) för mer detaljerad information.

> [!IMPORTANT]  
>  Det kan finnas fall där fältvärdena innehåller dessa symboler och du vill filtrera efter de. Genom att ibland behöva du inkludera det filteruttryck som innehåller symbolen med citattecken (”). Om du exempelvis vill filtrera poster som börjar med texten till exempel *S&R* är filteruttrycket `'S&R*'`.  

### <a name="-interval"></a>(..) Intervall

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`1100..2100`|Fr.o.m. 1100 t.o.m. 2100|  
|`..2500`|Alla t.o.m. 2500|  
|`..12 31 00`|Datum t.o.m. 00-12-31|  
|`P8..`|Information för bokföringsperiod 8 och framåt|  
|`..23`|Från startdatumet till den 23 innevarande månad, innevarande år 23:59:59|  
|`23..`|Från 23 innevarande månad, innevarande år 0:00:00 till tidsperiodens slut|  
|`22..23`|Från 22 innevarande månad, innevarande år 0:00:00 till 23 innevarande månad, innevarande år 23:59:59|  

### <a name="124-eitheror"></a>(&#124;) Antingen/eller  

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`1200|1300`|Nummer med 1200 eller 1300|  

### <a name="-not-equal-to"></a>(<>) Inte lika med  

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`<>0`|Alla nummer förutom 0<br /><br /> SQL-serveralternativet låter dig kombinera tecknet med ett jokertecken. Till exempel betyder <>A* inte lika med valfri text som börjar med A.|  

### <a name="-greater-than"></a>(>) Större än  

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`>1200`|Nummer större än 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Större än eller lika med  

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`>=1200`|Nummer större än eller lika med 1200|  

### <a name="-less-than"></a>(<) Mindre än  

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`<1200`|Nummer mindre än 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Mindre än eller lika med  

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`<=1200`|Nummer mindre än eller lika med 1200|  

### <a name="-and"></a>(&) och  

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`>200&<1200`|Nummer som är större än 200 och mindre än 1 200.|  

### <a name="-an-exact-character-match"></a>('') En exakt teckenmatchning  

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`'man'`|Text som matchar man exakt och är skiftlägeskänslig.|  

### <a name="-case-insensitive"></a>(@) Okänslig för skiftläge  

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`@man*`|Text som börjar med man och är skiftlägesokänslig.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Ett obestämt antal okända bokstäver

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`*Co*`|Text som innehåller ”Co” och är skiftlägeskänsligt.|  
|`*Co`|Text som slutar med ”Co” och är skiftlägeskänsligt.|  
|`Co*`|Text som börjar med ”Co” och är skiftlägeskänsligt.|  

> [!NOTE]  
>   Du kan inte använda `*` när du filtrerar på uppräkningsfält, t.ex fältet **Status** på försäljningsordern. För att ange ett filter för den här typen av fält kan du ange det numeriska värdet som en filtreringsparameter. T.ex. i fältet **Status** på en försäljningsorder som har värdena **Öppen**, **Släppt**, **Väntar på godkännande** och **Väntar på förskottsbetalning** använder du värdena `0`, `1`, `2` och `3` för att filtrera för dessa alternativ.

### <a name="-one-unknown-character"></a>(?) En okänd bokstav  

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`Hans?n`|Text som exempelvis Hansen eller Hanson|  

### <a name="combined-format-expressions"></a>Kombinerade uttryck  

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Ta med post nummer 5999 och poster med nummer fr.o.m. 8100 t.o.m.|  
|`..1299|1400..`|Ta med poster med nummer mindre än eller lika med 1299 och nummer större än eller lika med 1400 (d.v.s. alla nummer utom 1300 t.o.m. 1399)|  
|`>50&<100`|Ta med poster med nummer större än 50 och mindre än 100 (d.v.s. nummer fr.o.m. 51 t.o.m. 99)|  


## <a name="FilterTokens"></a> Filtertoken
När du anger filterkriterier kan du även skriva ord som har en speciell betydelse som kallas filtertoken. När du har angett tokenordet, ersätts ordet med värden som det representerar. Detta gör filtreringen enklare genom att minska behovet av att gå till andra sidor för att söka efter värden som du vill lägga till i filtret. Tabellerna nedan beskriver några av de token som du kan skriva som filterkriterier.

> [!TIP]
> Ditt företag kanske använder egna token. För mer information om den fullständiga uppsättningen med token som finns tillgängliga för dig eller om du vill lägga till fler anpassade variabler, kontakta administratören. Teknisk information finns i [Lägga till filtertoken](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)


### <a name="me-or-userid-records-assigned-to-you"></a>(%me eller %userid) Poster som har tilldelats dig

Använd `%me` eller `%userid` när du filtrerar i fält som innehåller användar-ID såsom fältet **Tilldelats användar-ID** om du vill visa alla poster som har tilldelats dig.

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`%me`<br />eller<br />`%userid`|Poster som är tilldelade till ditt användarkonto. |  

### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Kunder i Mina kunder

Använd `%mycustomers` i fältet kund**nr** om du vill visa alla poster för kunder som ingår i listan **mina kunder** i ditt rollcenter.

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`%mycustomers`|Kunder i **mina kunder** i rollcentret. |  

### <a name="myitems-items-in-my-items"></a>(%myitems) objekt i Mina objekt

Använd `%myitems` i fältet objekt**nr** om du vill visa alla poster för objekt som ingår i listan **mina objekt** i ditt rollcenter.

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`%myitems`|Objekt i **mina objekt** i rollcentret. |  

### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Leverantörer i Mina leverantörer

Använd `%myvendors` i fältet leverantörs**nr** om du vill visa alla poster för leverantörer som ingår i listan **mina leverantörer** i ditt rollcenter.

|Exempel|Poster som visas|  
|-----------------------|-----------------------|  
|`%myvendors`|Leverantörer i **mina leverantörer** i rollcentret. |  


## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Vanliga frågor om sökning och filtrering](ui-search-filter-faq.md)

