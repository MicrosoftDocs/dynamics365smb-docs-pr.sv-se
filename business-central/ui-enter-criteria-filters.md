---
title: Sortering, sökning och filtrering av listor | Microsoft Docs
description: Arbeta effektivt i listor genom att söka i data, sortera kolumner och förfina resultaten med hjälp av kraftfulla filtersymboler och kortkommandon.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: c6eb9465d07b702e545347cad5acf0a42f01d1de
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807923"
---
# <a name="sorting-searching-and-filtering-lists"></a><span data-ttu-id="b09ed-103">Sortera, söka och filtrera listor</span><span class="sxs-lookup"><span data-stu-id="b09ed-103">Sorting, Searching, and Filtering Lists</span></span>
<span data-ttu-id="b09ed-104">Det finns några saker som du kan göra som hjälper dig att söka, hitta och begränsa poster i en lista.</span><span class="sxs-lookup"><span data-stu-id="b09ed-104">There are a few things that you can do that will help you scan, find, and limit records in a list.</span></span> <span data-ttu-id="b09ed-105">Dessa inkluderar sortering, sökning och filtrering.</span><span class="sxs-lookup"><span data-stu-id="b09ed-105">These include sorting, searching and filtering.</span></span> <span data-ttu-id="b09ed-106">Du kan använda några eller alla av dessa samtidigt för att snabbt söka efter och analysera data.</span><span class="sxs-lookup"><span data-stu-id="b09ed-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

> [!TIP]
> <span data-ttu-id="b09ed-107">När du visar data sida vid sida kan du söka och använda enkel filtrering.</span><span class="sxs-lookup"><span data-stu-id="b09ed-107">When viewing your data as tiles, you can search and use basic filtering.</span></span> <span data-ttu-id="b09ed-108">Om du vill använda alla kraftfulla funktioner för sortering, sökning och filtrering, väljer du ikonen ![Visa som lista](media/ui_show_as_list_icon.png "Visa som lista vänsterpil") om du vill visa en lista.</span><span class="sxs-lookup"><span data-stu-id="b09ed-108">To use the full set of powerful features for sorting, searching and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to show as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="b09ed-109">Sortering</span><span class="sxs-lookup"><span data-stu-id="b09ed-109">Sorting</span></span>
<span data-ttu-id="b09ed-110">Med hjälp av sorteringsfunktionen kan du snabbt få en överblick över dina data.</span><span class="sxs-lookup"><span data-stu-id="b09ed-110">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="b09ed-111">Om t.ex. har många kunder kan du sortera dem efter **Kundnr.**, **Kundbokföringsmall**, **Valutakod**, **Lands-/regionkod**, eller **Momsregistreringsnr.** för att få den översikt som du behöver.</span><span class="sxs-lookup"><span data-stu-id="b09ed-111">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="b09ed-112">Om du vill sortera en lista, kan du välja en kolumn rubriktexten för att växla mellan stigande och fallande ordning, eller välja små listrutor pilen i kolumnrubriken och välj **stigande** eller **fallande**.</span><span class="sxs-lookup"><span data-stu-id="b09ed-112">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small down arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="b09ed-113">Sortering stöds inte på bilder, BLOB-fält, Flowfilter och fält som inte tillhör samma tabell.</span><span class="sxs-lookup"><span data-stu-id="b09ed-113">Sorting is not supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="b09ed-114">Sökning</span><span class="sxs-lookup"><span data-stu-id="b09ed-114">Searching</span></span>
<span data-ttu-id="b09ed-115"><!--## Searching by using the Quick Filter -->Högst upp på varje listsida finns ikonen ![söklista](media/ui-search/search-list.png "ikonen söklista")**Sök** som är ett snabbt och enkelt sätt att minska posterna i en lista och enbart visa de poster som innehåller de data som du är intresserad av att se.</span><span class="sxs-lookup"><span data-stu-id="b09ed-115"><!--## Searching by using the Quick Filter --> At the top of each list page, there is a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** icon that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you are interested in seeing.</span></span>

<span data-ttu-id="b09ed-116">Sök genom att bara markera sökikonen och skriv den text som du vill söka efter i rutan.</span><span class="sxs-lookup"><span data-stu-id="b09ed-116">To search, simply select the search icon, and then in the box, type the text that you are looking for.</span></span> <span data-ttu-id="b09ed-117">Du kan ange bokstäver, siffror och andra symboler.</span><span class="sxs-lookup"><span data-stu-id="b09ed-117">You can enter letters, numbers, and other symbols.</span></span>

### <a name="fine-tune-the-search"></a><span data-ttu-id="b09ed-118">Finjustera sökningen</span><span class="sxs-lookup"><span data-stu-id="b09ed-118">Fine-tune the search</span></span>
<span data-ttu-id="b09ed-119">I allmänhet försöker sökningen att matcha texten i alla fält. Den skiljer inte mellan versaler och gemener (d.v.s. skiftlägeskänslig) och matchar texten som placeras var som helst i fältet (i början, slutet eller i mitten).</span><span class="sxs-lookup"><span data-stu-id="b09ed-119">In general, search will attempt to match text across all fields; it does not distinguish between uppercase and lowercase characters (in other words, case insensitive), and will match text placed anwhere in the field (at the beginning, end, or in the middle).</span></span>

<span data-ttu-id="b09ed-120">Men du kan göra en mer exakt sökning med hjälp av följande tecken:</span><span class="sxs-lookup"><span data-stu-id="b09ed-120">However, you can make a more exact search by using the following special characters:</span></span>

- <span data-ttu-id="b09ed-121">För att hitta endast fältvärden som matchar hela texten och fallet exakt, placera söktexten mellan enskilda citat `''` (till exempel `'man'`).</span><span class="sxs-lookup"><span data-stu-id="b09ed-121">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="b09ed-122">För att hitta fältvärden som börjar med en viss text och matchar gemener/versaler, placera `*` efter söktexten (till exempel `man*`).</span><span class="sxs-lookup"><span data-stu-id="b09ed-122">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="b09ed-123">För att hitta fältvärden som slutar med en viss text och matchar gemener/versaler, placera `*` före söktexten (till exempel `*man`).</span><span class="sxs-lookup"><span data-stu-id="b09ed-123">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="b09ed-124">Om du använder `''`eller `*`, är sökningen skiftlägeskänslig.</span><span class="sxs-lookup"><span data-stu-id="b09ed-124">When using  `''` or `*`, the search is case sensitive.</span></span> <span data-ttu-id="b09ed-125">Om du vill göra sökningen skiftlägeskänsligt, placera `@` före texten (till exempel `@man*`).</span><span class="sxs-lookup"><span data-stu-id="b09ed-125">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="b09ed-126">I tabellen nedan finns några exempel som förklarar hur du kan använda sökningen.</span><span class="sxs-lookup"><span data-stu-id="b09ed-126">The following table provides some examples to explain how you can use the search.</span></span>


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

|<span data-ttu-id="b09ed-127">Sökkriterier</span><span class="sxs-lookup"><span data-stu-id="b09ed-127">Search Criteria</span></span>|<span data-ttu-id="b09ed-128">Söker efter...</span><span class="sxs-lookup"><span data-stu-id="b09ed-128">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="b09ed-129">eller</span><span class="sxs-lookup"><span data-stu-id="b09ed-129">or</span></span> <br />`Man`|<span data-ttu-id="b09ed-130">Alla poster med fält som innehåller texten **man**, oavsett gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="b09ed-130">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="b09ed-131">Till exempel **Manchester**, **manuell**, eller **Idrottsman**.</span><span class="sxs-lookup"><span data-stu-id="b09ed-131">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="b09ed-132">Alla poster med fält som endast innehåller texten **Man** som matchar gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="b09ed-132">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="b09ed-133">Alla poster med fält som börjar med texten <b>Man</b>, som matchar gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="b09ed-133">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="b09ed-134">Till exempel **Manchester** men inte **manuell**, eller **Idrottsman**.</span><span class="sxs-lookup"><span data-stu-id="b09ed-134">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="b09ed-135">Alla poster med fält som börjar med texten **man** oavsett om de är gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="b09ed-135">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="b09ed-136">Till exempel **Manchester** och **manuell** men inte **Idrottsman**.</span><span class="sxs-lookup"><span data-stu-id="b09ed-136">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="b09ed-137">Alla poster som slutar med texten **man** oavsett om de är gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="b09ed-137">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="b09ed-138">Till exempel **Idrottsman** men inte **Manchester**, eller **manuell**.</span><span class="sxs-lookup"><span data-stu-id="b09ed-138">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|

> [!TIP]
> <span data-ttu-id="b09ed-139">Du kan trycka på F3 för att aktivera och avaktivera sökrutan.</span><span class="sxs-lookup"><span data-stu-id="b09ed-139">You can press F3 to activate and deactivate the search box.</span></span> <span data-ttu-id="b09ed-140">Mer information finns i [Kortkommandon](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="b09ed-140">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

## <a name="filtering"></a><span data-ttu-id="b09ed-141">Filtrering</span><span class="sxs-lookup"><span data-stu-id="b09ed-141">Filtering</span></span>
<span data-ttu-id="b09ed-142">Filtrering ger ett mer avancerat och flexibelt sätt att kontrollera vilka poster som ska visas i en lista.</span><span class="sxs-lookup"><span data-stu-id="b09ed-142">Filtering provides a more advanced and versatile way of controlling which records display in a list.</span></span> <span data-ttu-id="b09ed-143">Det finns två stora skillnader mellan sökning och filtrering, enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="b09ed-143">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="b09ed-144">**Sökning**</span><span class="sxs-lookup"><span data-stu-id="b09ed-144">**Searching**</span></span> | <span data-ttu-id="b09ed-145">**Filtrering**</span><span class="sxs-lookup"><span data-stu-id="b09ed-145">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="b09ed-146">**Tillämpliga fält**</span><span class="sxs-lookup"><span data-stu-id="b09ed-146">**Applicable fields**</span></span> | <span data-ttu-id="b09ed-147">Söker i alla fält som visas på sidan.</span><span class="sxs-lookup"><span data-stu-id="b09ed-147">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="b09ed-148">Filtrerar ett eller flera fält individuellt med val från något av fälten i tabellen, inklusive fält som inte visas på sidan.</span><span class="sxs-lookup"><span data-stu-id="b09ed-148">Filters one or more fields individually, selecting from any field on the table, including fields that are not visible on the page.</span></span> |
| <span data-ttu-id="b09ed-149">**Matchning**</span><span class="sxs-lookup"><span data-stu-id="b09ed-149">**Matching**</span></span> | <span data-ttu-id="b09ed-150">Visar poster med fält som matchar söktexten, oavsett versaler eller gemener eller placeringen av texten.</span><span class="sxs-lookup"><span data-stu-id="b09ed-150">Displays records with fields that match the search text, irrespective of casing or placement of that text.</span></span> | <span data-ttu-id="b09ed-151">Visar poster där fältet matchar filtret exakt och är skiftlägeskänsliga, om inte särskilda filtersymboler har angetts.</span><span class="sxs-lookup"><span data-stu-id="b09ed-151">Displays records where the field matches the filter exactly and is case sensitive, unless special filter symbols are entered.</span></span>

<span data-ttu-id="b09ed-152">Filtrering låter dig visa poster för specifika konton eller kunder, datum, belopp och annan information genom att ange filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="b09ed-152">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="b09ed-153">Bara poster som matchar kriteriet visas.</span><span class="sxs-lookup"><span data-stu-id="b09ed-153">Only records that match the criteria are displayed.</span></span> <span data-ttu-id="b09ed-154">Om du anger kriterier för flera fält, kommer endast posterna som matchar alla kriterier att visas.</span><span class="sxs-lookup"><span data-stu-id="b09ed-154">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

### <a name="working-in-the-filter-pane"></a><span data-ttu-id="b09ed-155">Arbeta i filterrutan</span><span class="sxs-lookup"><span data-stu-id="b09ed-155">Working in the filter pane</span></span>
<span data-ttu-id="b09ed-156">Filterrutan visar en lista över aktuella filter för en lista och gör att du kan ställa in egna anpassade filter på ett eller flera fält.</span><span class="sxs-lookup"><span data-stu-id="b09ed-156">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields.</span></span> <span data-ttu-id="b09ed-157">I bilden nedan visas ett exempelfilterfönster för en lista med försäljningsofferter.</span><span class="sxs-lookup"><span data-stu-id="b09ed-157">The following figure shows an example filter pane for a Sales Quotes list.</span></span>

<span data-ttu-id="b09ed-158">![Översikt över filterruta](media/filter-pane-overview.png "Filterikon")</span><span class="sxs-lookup"><span data-stu-id="b09ed-158">![Filter pane overview ](media/filter-pane-overview.png "Filter icon")</span></span>

<span data-ttu-id="b09ed-159">Om du vill visa filterrutan, använd kortkommandot **Shift + F3**.</span><span class="sxs-lookup"><span data-stu-id="b09ed-159">To display the filter pane, use the **Shift+F3** keyboard shortcut.</span></span> <span data-ttu-id="b09ed-160">För listor i Rollcenter kan du också välja den nedåtriktade pilen bredvid en rubrik i fältet ovanför listan och väljer sedan **visa filterruta**.</span><span class="sxs-lookup"><span data-stu-id="b09ed-160">For lists within the Role Center, you can also choose the down arrow near the page title in the navigation bar above the list, and then choose **Show filter pane**.</span></span>

<span data-ttu-id="b09ed-161">![Visa filterruta](media/open-filter-pane.png "Visa filterruta")</span><span class="sxs-lookup"><span data-stu-id="b09ed-161">![Show filter pane](media/open-filter-pane.png "Show filter pane")</span></span>

<span data-ttu-id="b09ed-162">En filterruta är indelad i tre avsnitt: **Vyer**, **Filtrera lista efter** och **Filtrera summor efter**:</span><span class="sxs-lookup"><span data-stu-id="b09ed-162">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="b09ed-163">**Vyer**</span><span class="sxs-lookup"><span data-stu-id="b09ed-163">**Views**</span></span>

  <span data-ttu-id="b09ed-164">Vissa listor inkluderar avsnittet **Vyer**.</span><span class="sxs-lookup"><span data-stu-id="b09ed-164">Some lists will include the **Views** section.</span></span> <span data-ttu-id="b09ed-165">Vyer är varianter av listan som har förkonfigurerats med filter.</span><span class="sxs-lookup"><span data-stu-id="b09ed-165">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="b09ed-166">Om du vill växla till en annan vy i listan, markerar du bara en annan länk.</span><span class="sxs-lookup"><span data-stu-id="b09ed-166">To switch to a different view of your list, simply select another link.</span></span> <span data-ttu-id="b09ed-167">Du kan tillfälligt ändra filter i en vy, men ändringarna kommer inte att sparas permanent.</span><span class="sxs-lookup"><span data-stu-id="b09ed-167">You can temporarily change the filters on a view, but the changes will not be permanently saved.</span></span>

- <span data-ttu-id="b09ed-168">**Filtrera lista efter**</span><span class="sxs-lookup"><span data-stu-id="b09ed-168">**Filter list by**</span></span>

  <span data-ttu-id="b09ed-169">Avsnittet **Filtrera listan efter** är där du lägger till filter på särskilda fält för att minska antalet visade poster.</span><span class="sxs-lookup"><span data-stu-id="b09ed-169">The **Filter list by** section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="b09ed-170">Om du vill lägga till ett filter, markera **+ Filter**, välj fältet som du vill filtrera från något fält i tabellen och ange sedan filterkriterierna i rutan.</span><span class="sxs-lookup"><span data-stu-id="b09ed-170">To add a filter, select **+ Filter**, select the field that you want to filter from any field in the table, and then enter filter criteria in the box.</span></span>

- <span data-ttu-id="b09ed-171">**Filtrera summor efter**</span><span class="sxs-lookup"><span data-stu-id="b09ed-171">**Filter totals by**</span></span>

  <span data-ttu-id="b09ed-172">Vissa listor som visar beräknade fält, till exempel belopp och kvantitet, inkluderar avsnittet **Filtrera summor efter** där du kan justera olika dimensioner som påverkar beräkningar.</span><span class="sxs-lookup"><span data-stu-id="b09ed-172">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="b09ed-173">Till exempel kan du snabbt analysera din kontoplan genom att filtrera belopp till en viss period eller du kan visa summor för försäljningsorder bara från ett visst lagerställe.</span><span class="sxs-lookup"><span data-stu-id="b09ed-173">For example, you can quickly analyze your chart of accounts by filtering amounts to a specific period, or you can view the totals for sales orders only from a specific warehouse.</span></span>

  <span data-ttu-id="b09ed-174">Lägg till ett filter genom att markera **+ Filter**, välj en av de fördefinierade dimensionerna och ange filterkriterierna i rutan.</span><span class="sxs-lookup"><span data-stu-id="b09ed-174">To add a filter, select **+ Filter**, select one of the predefined dimensions, and then add the filter criteria in the box.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b09ed-175">Filter i avsnittet **Filtrera summor efter** styrs av FlowFilter på sidans design.</span><span class="sxs-lookup"><span data-stu-id="b09ed-175">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="b09ed-176">Teknisk information finns i [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="b09ed-176">For technical information, see [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>


### <a name="entering-filter-criteria-in-the-filter-pane"></a><span data-ttu-id="b09ed-177">Ange filterkriterier i filterrutan</span><span class="sxs-lookup"><span data-stu-id="b09ed-177">Entering filter criteria in the filter pane</span></span>
<span data-ttu-id="b09ed-178">Gör något av följande för att välja ett fält att filtrera:</span><span class="sxs-lookup"><span data-stu-id="b09ed-178">To select a field to filter, do one of the following:</span></span>
  - <span data-ttu-id="b09ed-179">Välj **+ Fält** i filterrutan.</span><span class="sxs-lookup"><span data-stu-id="b09ed-179">In the filter pane, choose **+ Field**.</span></span> <span data-ttu-id="b09ed-180">Skriv namnet på det fält som du vill filtrera eller välj ett fält från menyn som visar alla fält i tabellen.</span><span class="sxs-lookup"><span data-stu-id="b09ed-180">Type the name of the field you wish to filter, or pick a field from the menu that displays all fields in the table.</span></span>

  - <span data-ttu-id="b09ed-181">Välj nedpilen i en kolumnrubrik och välj **Filter...**. Detta öppnar filterfönstret och lägger till kolumnen i filterrutan.</span><span class="sxs-lookup"><span data-stu-id="b09ed-181">In a column heading, choose the down arrow, and then choose **Filter...**. This will open the filter pane and add the column to the filter pane.</span></span>

<span data-ttu-id="b09ed-182">Du kan nu skriva eller välja filterkriterier i rutan.</span><span class="sxs-lookup"><span data-stu-id="b09ed-182">You can now type or select your filter criteria in the box.</span></span> <span data-ttu-id="b09ed-183">Typen av fält som du vill filtrera avgör vilka kriterier du kan ange.</span><span class="sxs-lookup"><span data-stu-id="b09ed-183">The type of field you filter determines which criteria you can enter.</span></span> <span data-ttu-id="b09ed-184">Till exempel kommer filtrering av ett fält som har fasta värden bara låta dig välja mellan dessa värden.</span><span class="sxs-lookup"><span data-stu-id="b09ed-184">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="b09ed-185">Mer information om särskilda filtersymboler finns i [Filterkriterier](#FilterCriteria) och [Filtertoken](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="b09ed-185">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="b09ed-186">Kolumner som redan har filter som indikeras av ![filterikon](media/ui-search/filter-icon.png "filterikon") i kolumnrubriken.</span><span class="sxs-lookup"><span data-stu-id="b09ed-186">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") in the column heading.</span></span> <span data-ttu-id="b09ed-187">Om du vill ta bort ett filter, markera kolumnrubriken och välj **Ta bort filter**.</span><span class="sxs-lookup"><span data-stu-id="b09ed-187">To remove a filter, select the column heading, then choose **Clear Filter**.</span></span>


### <a name="entering-filter-criteria-without-the-filter-pane"></a><span data-ttu-id="b09ed-188">Ange filterkriterier utan filterrutan</span><span class="sxs-lookup"><span data-stu-id="b09ed-188">Entering filter criteria without the filter pane</span></span>
<span data-ttu-id="b09ed-189">Du kan ange enkla filter direkt i listan utan att behöva använda filterrutan.</span><span class="sxs-lookup"><span data-stu-id="b09ed-189">You can specify simple filters directly within the list without having to use the filter pane.</span></span>
<span data-ttu-id="b09ed-190">Med något fält valt på en rad, använd kortkommandot **Alt + F3** för att endast visa de poster som har samma värde.</span><span class="sxs-lookup"><span data-stu-id="b09ed-190">With any field selected on a row, use the **Alt+F3** keyboard shortcut to display only the records having that same value.</span></span> <span data-ttu-id="b09ed-191">Du kan sedan välja ett annat fält och använda samma kortkommando igen för att fortsätta att förfina dina filter.</span><span class="sxs-lookup"><span data-stu-id="b09ed-191">You can then select another field and use the same shortcut again to continue refining your filters.</span></span> <span data-ttu-id="b09ed-192">Om det markerade fältet redan är filtrerat kommer **Alt + F3** att ta bort filtret.</span><span class="sxs-lookup"><span data-stu-id="b09ed-192">If the selected field is already filtered, using **Alt+F3** will clear that filter.</span></span>

> [!TIP]
> <span data-ttu-id="b09ed-193">Sök och analysera dina data snabbare genom att använda kombinationer av kortkommandon.</span><span class="sxs-lookup"><span data-stu-id="b09ed-193">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="b09ed-194">Exempelvis markerar du ett fält, använder **Skift + Alt + F3** om du vill lägga till fältet i filterrutan, använder **Ctrl + Retur** om du vill återgå till raderna, markerar ett annat fält och använder **Alt + F3** för att filtrera det värdet.</span><span class="sxs-lookup"><span data-stu-id="b09ed-194">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span>
<span data-ttu-id="b09ed-195">Mer information finns i [Kortkommandon](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="b09ed-195">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>


## <span data-ttu-id="b09ed-196"><a name="FilterCriteria"> </a>Filterkriterier och symboler</span><span class="sxs-lookup"><span data-stu-id="b09ed-196"><a name="FilterCriteria"> </a>Filter criteria and symbols</span></span>
<span data-ttu-id="b09ed-197">När du anger kriterier kan du använda alla siffror och bokstäver som du normalt kan använda i fältet.</span><span class="sxs-lookup"><span data-stu-id="b09ed-197">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="b09ed-198">Dessutom kan du använda specialtecken som du vill filtrera resultatet ytterligare.</span><span class="sxs-lookup"><span data-stu-id="b09ed-198">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="b09ed-199">I tabellen nedan visas de symboler som kan användas i filter.</span><span class="sxs-lookup"><span data-stu-id="b09ed-199">The following tables show the symbols which can be used in filters.</span></span> <span data-ttu-id="b09ed-200">För datum och tid kan du också se [Arbeta med kalenderdatum och tider](ui-enter-date-ranges.md) för mer detaljerad information.</span><span class="sxs-lookup"><span data-stu-id="b09ed-200">For dates and times, you can also refer to [Working with Calendar Dates and Times](ui-enter-date-ranges.md) for more detailed information.</span></span>

> [!IMPORTANT]  
>  <span data-ttu-id="b09ed-201">Det kan finnas fall där fältvärdena innehåller dessa symboler och du vill filtrera efter de.</span><span class="sxs-lookup"><span data-stu-id="b09ed-201">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="b09ed-202">Genom att ibland behöva du inkludera det filteruttryck som innehåller symbolen med citattecken (”).</span><span class="sxs-lookup"><span data-stu-id="b09ed-202">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="b09ed-203">Om du exempelvis vill filtrera poster som börjar med texten till exempel *S&R* är filteruttrycket `'S&R*'`.</span><span class="sxs-lookup"><span data-stu-id="b09ed-203">For example, if you want to filter on records that start with the text *S&R*, the filter expression is `'S&R*'`.</span></span>  

### <a name="-interval"></a><span data-ttu-id="b09ed-204">(..) Intervall</span><span class="sxs-lookup"><span data-stu-id="b09ed-204">(..) Interval</span></span>

|<span data-ttu-id="b09ed-205">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-205">Sample Expression</span></span>|<span data-ttu-id="b09ed-206">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-206">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="b09ed-207">Fr.o.m. 1100 t.o.m. 2100</span><span class="sxs-lookup"><span data-stu-id="b09ed-207">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="b09ed-208">Alla t.o.m. 2500</span><span class="sxs-lookup"><span data-stu-id="b09ed-208">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="b09ed-209">Datum t.o.m. 00-12-31</span><span class="sxs-lookup"><span data-stu-id="b09ed-209">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="b09ed-210">Information för bokföringsperiod 8 och framåt</span><span class="sxs-lookup"><span data-stu-id="b09ed-210">Information for accounting period 8 and thereafter</span></span>|  
|`..23`|<span data-ttu-id="b09ed-211">Från startdatumet till den 23 innevarande månad, innevarande år 23:59:59</span><span class="sxs-lookup"><span data-stu-id="b09ed-211">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="b09ed-212">Från 23 innevarande månad, innevarande år 0:00:00 till tidsperiodens slut</span><span class="sxs-lookup"><span data-stu-id="b09ed-212">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="b09ed-213">Från 22 innevarande månad, innevarande år 0:00:00 till 23 innevarande månad, innevarande år 23:59:59</span><span class="sxs-lookup"><span data-stu-id="b09ed-213">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

### <a name="124-eitheror"></a><span data-ttu-id="b09ed-214">(&#124;) Antingen eller</span><span class="sxs-lookup"><span data-stu-id="b09ed-214">(&#124;) Either/or</span></span>  

|<span data-ttu-id="b09ed-215">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-215">Sample Expression</span></span>|<span data-ttu-id="b09ed-216">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-216">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="b09ed-217">\`1200</span><span class="sxs-lookup"><span data-stu-id="b09ed-217">\`1200</span></span>|<span data-ttu-id="b09ed-218">1300\`</span><span class="sxs-lookup"><span data-stu-id="b09ed-218">1300\`</span></span>|<span data-ttu-id="b09ed-219">Nummer med 1200 eller 1300</span><span class="sxs-lookup"><span data-stu-id="b09ed-219">Numbers with 1200 or 1300</span></span>|  

### <a name="-not-equal-to"></a><span data-ttu-id="b09ed-220">(<>) Inte lika med</span><span class="sxs-lookup"><span data-stu-id="b09ed-220">(<>) Not equal to</span></span>  

|<span data-ttu-id="b09ed-221">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-221">Sample Expression</span></span>|<span data-ttu-id="b09ed-222">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="b09ed-223">Alla nummer förutom 0</span><span class="sxs-lookup"><span data-stu-id="b09ed-223">All numbers except 0</span></span><br /><br /> <span data-ttu-id="b09ed-224">SQL-serveralternativet låter dig kombinera tecknet med ett jokertecken.</span><span class="sxs-lookup"><span data-stu-id="b09ed-224">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="b09ed-225">Till exempel betyder <>A\* inte lika med valfri text som börjar med A.</span><span class="sxs-lookup"><span data-stu-id="b09ed-225">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

### <a name="-greater-than"></a><span data-ttu-id="b09ed-226">(>) Större än</span><span class="sxs-lookup"><span data-stu-id="b09ed-226">(>) Greater than</span></span>  

|<span data-ttu-id="b09ed-227">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-227">Sample Expression</span></span>|<span data-ttu-id="b09ed-228">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-228">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="b09ed-229">Nummer större än 1200</span><span class="sxs-lookup"><span data-stu-id="b09ed-229">Numbers greater than 1200</span></span>|  

### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="b09ed-230">(>=) Större än eller lika med</span><span class="sxs-lookup"><span data-stu-id="b09ed-230">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="b09ed-231">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-231">Sample Expression</span></span>|<span data-ttu-id="b09ed-232">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="b09ed-233">Nummer större än eller lika med 1200</span><span class="sxs-lookup"><span data-stu-id="b09ed-233">Numbers greater than or equal to 1200</span></span>|  

### <a name="-less-than"></a><span data-ttu-id="b09ed-234">(<) Mindre än</span><span class="sxs-lookup"><span data-stu-id="b09ed-234">(<) Less than</span></span>  

|<span data-ttu-id="b09ed-235">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-235">Sample Expression</span></span>|<span data-ttu-id="b09ed-236">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-236">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="b09ed-237">Nummer mindre än 1200</span><span class="sxs-lookup"><span data-stu-id="b09ed-237">Numbers less than 1200</span></span>|  

### <a name="-less-than-or-equal-to"></a><span data-ttu-id="b09ed-238">(<=) Mindre än eller lika med</span><span class="sxs-lookup"><span data-stu-id="b09ed-238">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="b09ed-239">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-239">Sample Expression</span></span>|<span data-ttu-id="b09ed-240">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-240">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="b09ed-241">Nummer mindre än eller lika med 1200</span><span class="sxs-lookup"><span data-stu-id="b09ed-241">Numbers less than or equal to 1200</span></span>|  

### <a name="-and"></a><span data-ttu-id="b09ed-242">(&) och</span><span class="sxs-lookup"><span data-stu-id="b09ed-242">(&) And</span></span>  

|<span data-ttu-id="b09ed-243">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-243">Sample Expression</span></span>|<span data-ttu-id="b09ed-244">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-244">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="b09ed-245">Nummer som är större än 200 och mindre än 1 200.</span><span class="sxs-lookup"><span data-stu-id="b09ed-245">Numbers greater than 200 and less than 1200</span></span>|  

### <a name="-an-exact-character-match"></a><span data-ttu-id="b09ed-246">('') En exakt teckenmatchning</span><span class="sxs-lookup"><span data-stu-id="b09ed-246">('') An exact character match</span></span>  

|<span data-ttu-id="b09ed-247">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-247">Sample Expression</span></span>|<span data-ttu-id="b09ed-248">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-248">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="b09ed-249">Text som matchar man exakt och är skiftlägeskänslig.</span><span class="sxs-lookup"><span data-stu-id="b09ed-249">Text that matches man exactly and is case sensitive.</span></span>|  

### <a name="-case-insensitive"></a><span data-ttu-id="b09ed-250">(@) Okänslig för skiftläge</span><span class="sxs-lookup"><span data-stu-id="b09ed-250">(@) Case insensitive</span></span>  

|<span data-ttu-id="b09ed-251">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-251">Sample Expression</span></span>|<span data-ttu-id="b09ed-252">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-252">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="b09ed-253">Text som börjar med man och är skiftlägesokänslig.</span><span class="sxs-lookup"><span data-stu-id="b09ed-253">Text that starts with man and is case insensitive.</span></span>|  

### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="b09ed-254">(\*) Ett obestämt antal okända bokstäver</span><span class="sxs-lookup"><span data-stu-id="b09ed-254">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="b09ed-255">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-255">Sample Expression</span></span>|<span data-ttu-id="b09ed-256">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-256">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="b09ed-257">Text som innehåller ”Co” och är skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="b09ed-257">Text that contains "Co" and is case sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="b09ed-258">Text som slutar med ”Co” och är skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="b09ed-258">Text that ends with "Co" and is case sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="b09ed-259">Text som börjar med ”Co” och är skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="b09ed-259">Text that begins with "Co" and is case sensitive.</span></span>|  

> [!NOTE]  
>   <span data-ttu-id="b09ed-260">Du kan inte använda `*` när du filtrerar på uppräkningsfält, t.ex fältet **Status** på försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="b09ed-260">You cannot use `*` when filtering on option (enumeration) fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="b09ed-261">För att ange ett filter för den här typen av fält kan du ange det numeriska värdet som en filtreringsparameter.</span><span class="sxs-lookup"><span data-stu-id="b09ed-261">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="b09ed-262">T.ex. i fältet **Status** på en försäljningsorder som har värdena **Öppen**, **Släppt**, **Väntar på godkännande** och **Väntar på förskottsbetalning** använder du värdena `0`, `1`, `2` och `3` för att filtrera för dessa alternativ.</span><span class="sxs-lookup"><span data-stu-id="b09ed-262">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values `0`, `1`, `2`, and `3` to filter for these options.</span></span>

### <a name="-one-unknown-character"></a><span data-ttu-id="b09ed-263">(?) En okänd bokstav</span><span class="sxs-lookup"><span data-stu-id="b09ed-263">(?) One unknown character</span></span>  

|<span data-ttu-id="b09ed-264">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-264">Sample Expression</span></span>|<span data-ttu-id="b09ed-265">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="b09ed-266">Text som exempelvis Hansen eller Hanson</span><span class="sxs-lookup"><span data-stu-id="b09ed-266">Text such as Hansen or Hanson</span></span>|  

### <a name="combined-format-expressions"></a><span data-ttu-id="b09ed-267">Kombinerade uttryck</span><span class="sxs-lookup"><span data-stu-id="b09ed-267">Combined format expressions</span></span>  

|<span data-ttu-id="b09ed-268">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-268">Sample Expression</span></span>|<span data-ttu-id="b09ed-269">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="b09ed-270">\`5999</span><span class="sxs-lookup"><span data-stu-id="b09ed-270">\`5999</span></span>|<span data-ttu-id="b09ed-271">8100..8490\`</span><span class="sxs-lookup"><span data-stu-id="b09ed-271">8100..8490\`</span></span>|<span data-ttu-id="b09ed-272">Ta med post nummer 5999 och poster med nummer fr.o.m. 8100 t.o.m. 8490.</span><span class="sxs-lookup"><span data-stu-id="b09ed-272">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="b09ed-273">\`..1299</span><span class="sxs-lookup"><span data-stu-id="b09ed-273">\`..1299</span></span>|<span data-ttu-id="b09ed-274">1400..\`</span><span class="sxs-lookup"><span data-stu-id="b09ed-274">1400..\`</span></span>|<span data-ttu-id="b09ed-275">Ta med poster med nummer mindre än eller lika med 1299 och nummer större än eller lika med 1400 (d.v.s. alla nummer utom 1300 t.o.m. 1399)</span><span class="sxs-lookup"><span data-stu-id="b09ed-275">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="b09ed-276">Ta med poster med nummer större än 50 och mindre än 100 (d.v.s. nummer fr.o.m. 51 t.o.m. 99)</span><span class="sxs-lookup"><span data-stu-id="b09ed-276">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  


## <span data-ttu-id="b09ed-277"><a name="FilterTokens"></a> Filtertoken</span><span class="sxs-lookup"><span data-stu-id="b09ed-277"><a name="FilterTokens"> </a>Filter tokens</span></span>
<span data-ttu-id="b09ed-278">När du anger filterkriterier kan du även skriva ord som har en speciell betydelse som kallas filtertoken.</span><span class="sxs-lookup"><span data-stu-id="b09ed-278">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="b09ed-279">När du har angett tokenordet, ersätts ordet med värden som det representerar.</span><span class="sxs-lookup"><span data-stu-id="b09ed-279">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="b09ed-280">Detta gör filtreringen enklare genom att minska behovet av att gå till andra sidor för att söka efter värden som du vill lägga till i filtret.</span><span class="sxs-lookup"><span data-stu-id="b09ed-280">This makes filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="b09ed-281">Tabellerna nedan beskriver några av de token som du kan skriva som filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="b09ed-281">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="b09ed-282">Ditt företag kanske använder egna token.</span><span class="sxs-lookup"><span data-stu-id="b09ed-282">Your organization may use custom tokens.</span></span> <span data-ttu-id="b09ed-283">För mer information om den fullständiga uppsättningen med token som finns tillgängliga för dig eller om du vill lägga till fler anpassade variabler, kontakta administratören.</span><span class="sxs-lookup"><span data-stu-id="b09ed-283">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="b09ed-284">Teknisk information finns i [Lägga till filtertoken](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)</span><span class="sxs-lookup"><span data-stu-id="b09ed-284">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)</span></span>


### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="b09ed-285">(%me eller %userid) poster som har tilldelats dig</span><span class="sxs-lookup"><span data-stu-id="b09ed-285">(%me or %userid) Records assigned to you</span></span>

<span data-ttu-id="b09ed-286">Använd `%me` eller `%userid` när du filtrerar i fält som innehåller användar-ID såsom fältet **Tilldelats användar-ID** om du vill visa alla poster som har tilldelats dig.</span><span class="sxs-lookup"><span data-stu-id="b09ed-286">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="b09ed-287">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-287">Sample Expression</span></span>|<span data-ttu-id="b09ed-288">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-288">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="b09ed-289">eller</span><span class="sxs-lookup"><span data-stu-id="b09ed-289">or</span></span><br />`%userid`|<span data-ttu-id="b09ed-290">Poster som är tilldelade till ditt användarkonto.</span><span class="sxs-lookup"><span data-stu-id="b09ed-290">Records that are assigned to your user account.</span></span> |  

### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="b09ed-291">(%mycustomers) Kunder i Mina kunder</span><span class="sxs-lookup"><span data-stu-id="b09ed-291">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="b09ed-292">Använd `%mycustomers` i fältet kund**nr** om du vill visa alla poster för kunder som ingår i listan **mina kunder** i ditt rollcenter.</span><span class="sxs-lookup"><span data-stu-id="b09ed-292">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="b09ed-293">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-293">Sample Expression</span></span>|<span data-ttu-id="b09ed-294">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-294">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="b09ed-295">Kunder i **mina kunder** i rollcentret.</span><span class="sxs-lookup"><span data-stu-id="b09ed-295">Customers in the **My Customers** on your Role Center.</span></span> |  

### <a name="myitems-items-in-my-items"></a><span data-ttu-id="b09ed-296">(%myitems) objekt i Mina objekt</span><span class="sxs-lookup"><span data-stu-id="b09ed-296">(%myitems) Items in My Items</span></span>

<span data-ttu-id="b09ed-297">Använd `%myitems` i fältet objekt**nr** om du vill visa alla poster för objekt som ingår i listan **mina objekt** i ditt rollcenter.</span><span class="sxs-lookup"><span data-stu-id="b09ed-297">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="b09ed-298">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-298">Sample Expression</span></span>|<span data-ttu-id="b09ed-299">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-299">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="b09ed-300">Objekt i **mina objekt** i rollcentret.</span><span class="sxs-lookup"><span data-stu-id="b09ed-300">Items in the **My Items** on your Role Center.</span></span> |  

### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="b09ed-301">(%myvendors) Leverantörer i Mina leverantörer</span><span class="sxs-lookup"><span data-stu-id="b09ed-301">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="b09ed-302">Använd `%myvendors` i fältet leverantörs**nr** om du vill visa alla poster för leverantörer som ingår i listan **mina leverantörer** i ditt rollcenter.</span><span class="sxs-lookup"><span data-stu-id="b09ed-302">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="b09ed-303">Exempel</span><span class="sxs-lookup"><span data-stu-id="b09ed-303">Sample Expression</span></span>|<span data-ttu-id="b09ed-304">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="b09ed-304">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="b09ed-305">Leverantörer i **mina leverantörer** i rollcentret.</span><span class="sxs-lookup"><span data-stu-id="b09ed-305">Vendors in the **My Vendors** on your Role Center.</span></span> |  


## <a name="see-also"></a><span data-ttu-id="b09ed-306">Se även</span><span class="sxs-lookup"><span data-stu-id="b09ed-306">See Also</span></span>
<span data-ttu-id="b09ed-307">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b09ed-307">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b09ed-308">Vanliga frågor om sökning och filtrering</span><span class="sxs-lookup"><span data-stu-id="b09ed-308">Common questions about Searching and Filtering</span></span>](ui-search-filter-faq.md)
