---
title: Sortering, sökning och filtrering av listor | Microsoft Docs
description: Arbeta effektivt i listor genom att söka i data, sortera kolumner och förfina resultaten med hjälp av kraftfulla filtersymboler och kortkommandon.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5c67ea33937ded164626e4c403522a7dc1f3dca0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912577"
---
# <a name="sorting-searching-and-filtering"></a><span data-ttu-id="bd4b1-103">Sortera, söka och filtrera</span><span class="sxs-lookup"><span data-stu-id="bd4b1-103">Sorting, Searching, and Filtering</span></span>

<span data-ttu-id="bd4b1-104">Det finns några saker som du kan göra som hjälper dig att söka, hitta och begränsa poster i en lista eller i en rapport eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-104">There are a few things that you can do that will help you scan, find, and limit records on a list or in a report or XMLport.</span></span> <span data-ttu-id="bd4b1-105">Dessa inkluderar sortering, sökning och filtrering.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-105">These include sorting, searching, and filtering.</span></span> <span data-ttu-id="bd4b1-106">Du kan använda några eller alla av dessa samtidigt för att snabbt söka efter och analysera data.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

<span data-ttu-id="bd4b1-107">För rapporter och XMLportar kan du, som på listor, ange filter för att begränsa vilka data som ska tas med i rapporten XMLport, men du kan inte sortera och söka.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-107">For reports and XMLports, as on lists, you can set filters to delimit which data to include in the report or XMLport, but you cannot sort and search.</span></span>

> [!TIP]
> <span data-ttu-id="bd4b1-108">När du visar data sida vid sida kan du söka och använda enkel filtrering.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-108">When viewing your data as tiles, you can search and use basic filtering.</span></span> <span data-ttu-id="bd4b1-109">Om du vill använda alla kraftfulla funktioner för sortering, sökning och filtrering, väljer du ikonen ![Visa som lista](media/ui_show_as_list_icon.png "Visa som vänster listpil") om du vill visa posterna som en lista.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-109">To use the full set of powerful features for sorting, searching, and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to view the records as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="bd4b1-110">Sortering</span><span class="sxs-lookup"><span data-stu-id="bd4b1-110">Sorting</span></span>

<span data-ttu-id="bd4b1-111">Med hjälp av sorteringsfunktionen kan du snabbt få en överblick över dina data.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="bd4b1-112">Om t.ex. har många kunder kan du sortera dem efter **Kundnr.**, **Kundbokföringsmall**, **Valutakod**, **Lands-/regionkod**, eller **Momsregistreringsnr.** för att få den översikt som du behöver.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-112">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="bd4b1-113">Om du vill sortera en lista, kan du välja en kolumn rubriktexten för att växla mellan stigande och fallande ordning, eller välja listpilen i kolumnrubriken och välj **stigande** eller **fallande**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-113">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the drop-down arrow in the column heading, and then choose the **Ascending** or **Descending** action.</span></span>  

> [!NOTE]  
> <span data-ttu-id="bd4b1-114">Sortering stöds inte på bilder, BLOB-fält, Flowfilter och fält som inte tillhör samma tabell.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-114">Sorting is not supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="bd4b1-115">Sökning</span><span class="sxs-lookup"><span data-stu-id="bd4b1-115">Searching</span></span>

<!--## Searching by using the Quick Filter -->
<span data-ttu-id="bd4b1-116">Högst upp på varje listsida finns åtgärden ![Söklistikon](media/ui-search/search-list.png "Ikon för Söklista") **Sök** som ger ett snabbt och enkelt sätt att minska posterna i en lista och enbart visa de poster som innehåller de data som du är intresserad av att se.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-116">At the top of each list page, there is a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** action that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you are interested in seeing.</span></span>

<span data-ttu-id="bd4b1-117">Sök genom att bara markera åtgärden **Sök** och skriv den text som du vill söka efter i rutan.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-117">To search, simply choose the **Search** action, and then in the box, type the text that you are looking for.</span></span> <span data-ttu-id="bd4b1-118">Du kan ange bokstäver, siffror och andra symboler.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-118">You can enter letters, numbers, and other symbols.</span></span>

### <a name="fine-tuning-the-search"></a><span data-ttu-id="bd4b1-119">Finjustera sökningen</span><span class="sxs-lookup"><span data-stu-id="bd4b1-119">Fine-tuning the Search</span></span>

<span data-ttu-id="bd4b1-120">Vanligtvis försöker sökningen matcha text i alla fält.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-120">In general, search will attempt to match text across all fields.</span></span> <span data-ttu-id="bd4b1-121">Den skiljer inte mellan versaler och gemener (d.v.s. skiftlägeskänslig) och matchar texten som placeras var som helst i fältet i början, slutet eller i mitten.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-121">It does not distinguish between uppercase and lowercase characters (case insensitive) and will match text placed anywhere in the field, at the beginning, end, or in the middle.</span></span>

<span data-ttu-id="bd4b1-122">Men du kan göra en mer exakt sökning med hjälp av specialtecken.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-122">However, you can make a more exact search by using special characters.</span></span>

- <span data-ttu-id="bd4b1-123">För att hitta endast fältvärden som matchar hela texten och fallet exakt, placera söktexten mellan enskilda citat `''` (till exempel `'man'`).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-123">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="bd4b1-124">För att hitta fältvärden som börjar med en viss text och matchar gemener/versaler, placera `*` efter söktexten (till exempel `man*`).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-124">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="bd4b1-125">För att hitta fältvärden som slutar med en viss text och matchar gemener/versaler, placera `*` före söktexten (till exempel `*man`).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-125">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="bd4b1-126">Om du använder `''`eller `*`, är sökningen skiftlägeskänslig.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-126">When using  `''` or `*`, the search is case sensitive.</span></span> <span data-ttu-id="bd4b1-127">Om du vill göra sökningen skiftlägeskänsligt, placera `@` före texten (till exempel `@man*`).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-127">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="bd4b1-128">I tabellen nedan finns några exempel som förklarar hur du kan använda sökningen.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-128">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="bd4b1-129">Sökkriterier</span><span class="sxs-lookup"><span data-stu-id="bd4b1-129">Search Criteria</span></span>|<span data-ttu-id="bd4b1-130">Söker efter...</span><span class="sxs-lookup"><span data-stu-id="bd4b1-130">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="bd4b1-131">eller</span><span class="sxs-lookup"><span data-stu-id="bd4b1-131">or</span></span> <br />`Man`|<span data-ttu-id="bd4b1-132">Alla poster med fält som innehåller texten **man**, oavsett gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-132">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="bd4b1-133">Till exempel **Manchester**, **manuell**, eller **Idrottsman**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-133">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="bd4b1-134">Alla poster med fält som endast innehåller texten **Man** som matchar gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-134">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="bd4b1-135">Alla poster med fält som börjar med texten <b>Man</b>, som matchar gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-135">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="bd4b1-136">Till exempel **Manchester** men inte **manuell**, eller **Idrottsman**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-136">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="bd4b1-137">Alla poster med fält som börjar med texten **man** oavsett om de är gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-137">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="bd4b1-138">Till exempel **Manchester** och **manuell** men inte **Idrottsman**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-138">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="bd4b1-139">Alla poster som slutar med texten **man** oavsett om de är gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-139">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="bd4b1-140">Till exempel **Idrottsman** men inte **Manchester**, eller **manuell**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-140">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|

> [!TIP]
> <span data-ttu-id="bd4b1-141">Du kan trycka på **F3** för att aktivera och avaktivera sökrutan.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-141">You can press **F3** to activate and deactivate the search box.</span></span> <span data-ttu-id="bd4b1-142">Mer information finns i [Kortkommandon](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-142">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

> [!NOTE]  
> <span data-ttu-id="bd4b1-143">Sökningen matchar inte värden i bilder, BLOB-fält, FlowFilter, FlowFields och andra fält som inte ingår i en tabell.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-143">Search will not match values in images, BLOB fields, FlowFilters, FlowFields, and other fields that are not part of a table.</span></span>

## <a name="filtering"></a><a name="filtering"></a><span data-ttu-id="bd4b1-144">Filtrering</span><span class="sxs-lookup"><span data-stu-id="bd4b1-144">Filtering</span></span>

<span data-ttu-id="bd4b1-145">Filtrering ger ett mer avancerat och flexibelt sätt att kontrollera vilka poster som ska visas i en lista eller inkludera en rapport eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-145">Filtering provides a more advanced and versatile way of controlling which records display on a list or include in a report or XMLport.</span></span> <span data-ttu-id="bd4b1-146">Det finns två stora skillnader mellan sökning och filtrering, enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-146">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="bd4b1-147">**Sökning**</span><span class="sxs-lookup"><span data-stu-id="bd4b1-147">**Searching**</span></span> | <span data-ttu-id="bd4b1-148">**Filtrering**</span><span class="sxs-lookup"><span data-stu-id="bd4b1-148">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="bd4b1-149">**Tillämpliga fält**</span><span class="sxs-lookup"><span data-stu-id="bd4b1-149">**Applicable Fields**</span></span> | <span data-ttu-id="bd4b1-150">Söker i alla fält som visas på sidan.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-150">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="bd4b1-151">Filtrerar ett eller flera fält individuellt med val från något av fälten i tabellen, inklusive fält som inte visas på sidan.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-151">Filters one or more fields individually, selecting from any field on the table, including fields that are not visible on the page.</span></span> |
| <span data-ttu-id="bd4b1-152">**Matchning**</span><span class="sxs-lookup"><span data-stu-id="bd4b1-152">**Matching**</span></span> | <span data-ttu-id="bd4b1-153">Visar poster med fält som matchar söktexten, oavsett versaler eller gemener eller placeringen av texten.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-153">Displays records with fields that match the search text, irrespective of casing or placement of that text.</span></span> | <span data-ttu-id="bd4b1-154">Visar poster där fältet matchar filtret exakt och är skiftlägeskänsliga, om inte särskilda filtersymboler har angetts.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-154">Displays records where the field matches the filter exactly and is case sensitive, unless special filter symbols are entered.</span></span>

<span data-ttu-id="bd4b1-155">Filtrering låter dig visa poster för specifika konton eller kunder, datum, belopp och annan information genom att ange filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-155">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="bd4b1-156">Endast poster som matchar kriteriet visas i listan eller tas med i rapporten, batch-jobbet eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-156">Only records that match the criteria are displayed on the list or included in the report, batch job, or XMLport.</span></span> <span data-ttu-id="bd4b1-157">Om du anger kriterier för flera fält, kommer endast posterna som matchar alla kriterier att visas.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-157">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

<span data-ttu-id="bd4b1-158">För listor visas filtren i ett filterfönster som visas till vänster om listan när du aktiverar den.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-158">For lists, the filters are displayed on a filter pane that appears to the left of the list when you activate it.</span></span> <span data-ttu-id="bd4b1-159">För rapporter, batch-jobb och XMLport-kolumner visas filtren direkt på sidan för begäran.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-159">For reports, batch jobs, and XMLports, the filters are visible directly on the request page.</span></span>

### <a name="filtering-with-option-fields"></a><span data-ttu-id="bd4b1-160">Filtrera med alternativfält</span><span class="sxs-lookup"><span data-stu-id="bd4b1-160">Filtering with Option Fields</span></span>

<span data-ttu-id="bd4b1-161">För "vanliga fält som innehåller data, inställningsdatum eller affärsdata kan du ange filter både genom att markera data och ange filtervärden, och du kan använda symboler för att definiera avancerade filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-161">For "ordinary" fields that hold data, setup date or business data, you can set filters both by selecting data and by typing filter values, and you can use symbols to define advanced filter criteria.</span></span> <span data-ttu-id="bd4b1-162">Mer information finns i [Ange filtervillkor](ui-enter-criteria-filters.md#entering-filter-criteria).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-162">For more information, see [Entering Filter Criteria](ui-enter-criteria-filters.md#entering-filter-criteria).</span></span>

<span data-ttu-id="bd4b1-163">För fält av typen **alternativ**kan du bara ange ett filter genom att välja ett eller flera alternativ i en listruta med tillgängliga alternativ.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-163">For fields of type **Option**, however, you can only set a filter by selecting one or more options from a drop-down list of the available options.</span></span> <span data-ttu-id="bd4b1-164">Ett exempel på ett alternativfält är fältet **status** på sidan **försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-164">An example of an option field is the **Status** field on the **Sales Orders** page.</span></span>

> [!NOTE]
> <span data-ttu-id="bd4b1-165">När du väljer flera alternativ som filtervärde definieras relationen mellan alternativen som *ELLER*.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-165">When you select multiple options as a filter value, the relationship between the options is defined as *OR*.</span></span> <span data-ttu-id="bd4b1-166">Om du till exempel markerar både kryssrutan **öppna** och **släppta** i fältet **status** på sidan **försäljningsorder** betyder det att försäljningsorder som antingen är öppna eller släppta visas.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-166">For example, if you select both the **Open** and the **Released** check box in the **Status** filter field on the **Sales Orders** page, it means that sales orders that are either open or released are displayed.</span></span>

### <a name="setting-filters-on-lists"></a><span data-ttu-id="bd4b1-167">Ange filter för listor</span><span class="sxs-lookup"><span data-stu-id="bd4b1-167">Setting Filters on Lists</span></span>

<span data-ttu-id="bd4b1-168">I listor anger du filter genom att använda filterrutan.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-168">On lists, you set filters by using the filter pane.</span></span> <span data-ttu-id="bd4b1-169">Om du vill visa filterrutan för en lista väljer du listpilen bredvid sidans namn och väljer sedan åtgärden **Visa filterruta**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-169">To display the filter pane for a list, choose the drop-down arrow next to the name of the page, and then choose the **Show filter pane** action.</span></span> <span data-ttu-id="bd4b1-170">Du kan också trycka på **Shift+F3**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-170">Alternatively, press **Shift+F3**.</span></span>

<span data-ttu-id="bd4b1-171">Om du vill visa filterrutan för en kolumn på en lista väljer du listpilen bredvid och väljer sedan åtgärden **Filter**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-171">To display the filter pane for a column on a list, choose the drop-down arrow, and then choose the **Filter** action.</span></span> <span data-ttu-id="bd4b1-172">Du kan också trycka på **Shift+F3**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-172">Alternatively, press **Shift+F3**.</span></span> <span data-ttu-id="bd4b1-173">Filterrutan öppnas och den markerade kolumnen visas som ett filterfält i avsnittet **Filtrera lista efter**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-173">The filter pane opens with the selected column shown as a filter field in the **Filter list by** section.</span></span>

<span data-ttu-id="bd4b1-174">Filterrutan visar en lista över aktuella filter för en lista och gör att du kan ställa in egna anpassade filter på ett eller flera fält genom att välja åtgärden **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-174">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields by choosing the **+ Filter** action.</span></span>

 <span data-ttu-id="bd4b1-175">En filterruta är indelad i tre avsnitt: **Vyer**, **Filtrera lista efter** och **Filtrera summor efter**:</span><span class="sxs-lookup"><span data-stu-id="bd4b1-175">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="bd4b1-176">**Vyer**</span><span class="sxs-lookup"><span data-stu-id="bd4b1-176">**Views**</span></span>

  <span data-ttu-id="bd4b1-177">Vissa listor inkluderar avsnittet **Vyer**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-177">Some lists include the **Views** section.</span></span> <span data-ttu-id="bd4b1-178">Vyer är varianter av listan som har förkonfigurerats med filter.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-178">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="bd4b1-179">Du kan definiera och spara hur många vyer du vill per lista, och vyerna blir tillgängliga för dig på valfri enhet du loggar in på.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-179">You can define and save as many views as you want per list, and the views will be available to you on any device you sign into.</span></span> <span data-ttu-id="bd4b1-180">Mer information finns i avsnittet [Spara och anpassa listvyer](ui-views.md).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-180">For more information, see [Save and Personalize List Views](ui-views.md).</span></span>

- <span data-ttu-id="bd4b1-181">**Filtrera lista efter**</span><span class="sxs-lookup"><span data-stu-id="bd4b1-181">**Filter list by**</span></span>

  <span data-ttu-id="bd4b1-182">Här lägger du till filter på särskilda fält för att minska antalet visade poster.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-182">This is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="bd4b1-183">Du kan lägga till ett filter genom att välja åtgärden **+ Filter** och sedan ange namnet på det fält som du vill filtrera listan efter eller välja ett fält från den nedrullningsbara listan.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-183">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter the list by, or pick a field from the drop-down list.</span></span>

- <span data-ttu-id="bd4b1-184">**Filtrera summor efter**</span><span class="sxs-lookup"><span data-stu-id="bd4b1-184">**Filter totals by**</span></span>

  <span data-ttu-id="bd4b1-185">Vissa listor som visar beräknade fält, till exempel belopp och kvantitet, inkluderar avsnittet **Filtrera summor efter** där du kan justera olika dimensioner som påverkar beräkningar.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-185">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="bd4b1-186">Du kan lägga till ett filter genom att välja åtgärden **+ Filter** och sedan ange namnet på det fält som du vill filtrera listan efter eller välja ett fält från den nedrullningsbara listan.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-186">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter the list by, or pick a field from the drop-down list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="bd4b1-187">Filter i avsnittet **Filtrera summor efter** styrs av FlowFilter på sidans design.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-187">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="bd4b1-188">Teknisk information finns i [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-188">For technical information, see [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>

<span data-ttu-id="bd4b1-189">Du kan ställa in ett enkelt filter direkt på en lista i med hjälp av filterrutan, nämligen ett filter som visar endast poster med samma värde som i den markerade cellen.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-189">You can set a simple filter directly on a list within using the filter pane, namely a filter that displays only records with the same value as in the selected cell.</span></span> <span data-ttu-id="bd4b1-190">Välj en cell på listan, välj listpilen bredvid och väljer sedan åtgärden **Filtrera på det här värdet**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-190">Select a cell on the list, choose the drop-down arrow, and then choose the **Filter to This Value** action.</span></span> <span data-ttu-id="bd4b1-191">Du kan också trycka på **Alt+F3**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-191">Alternatively, press **Alt+F3**.</span></span>

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a><span data-ttu-id="bd4b1-192">Ange filter i rapporter, batch-jobb och XMLport</span><span class="sxs-lookup"><span data-stu-id="bd4b1-192">Setting Filters in Reports, Batch Jobs, and XMLports</span></span>

<span data-ttu-id="bd4b1-193">För rapporter och XMLport-kolumner visas filtren direkt på sidan för begäran.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-193">For reports and XMLports, the filters are visible directly on the request page.</span></span> <span data-ttu-id="bd4b1-194">På sidan för begäran visas de filter som används senast enligt ditt val i fältet **Använd standardvärden från**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-194">The request page displays the last used filters according to your selection in the **Use default values from** field.</span></span> <span data-ttu-id="bd4b1-195">Mer information finns i [Använda sparade inställningar](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-195">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="bd4b1-196">I huvudavsnittet **filter** visas de standardfilterfält som du använder för att avgränsa vilka poster som ska ingå i rapporten or XMLport.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-196">The main **Filter** section shows the default filter fields that you use to delimit which records to include in the report or XMLport.</span></span> <span data-ttu-id="bd4b1-197">Du kan lägga till ett filter genom att välja åtgärden **+ Filter** och sedan ange namnet på det fält som du vill filtrera efter eller välja ett fält från den nedrullningsbara listan.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-197">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

<span data-ttu-id="bd4b1-198">I avsnittet **Filtrera summor efter** kan du justera olika dimensioner som påverkar beräkningarna i rapporten eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-198">In the **Filter totals by** section, you can adjust various dimensions that influence calculations in the report or XMLport.</span></span> <span data-ttu-id="bd4b1-199">Du kan lägga till ett filter genom att välja åtgärden **+ Filter** och sedan ange namnet på det fält som du vill filtrera efter eller välja ett fält från den nedrullningsbara listan.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-199">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

## <a name="entering-filter-criteria"></a><span data-ttu-id="bd4b1-200">Ange villkor i filter</span><span class="sxs-lookup"><span data-stu-id="bd4b1-200">Entering Filter Criteria</span></span>

<span data-ttu-id="bd4b1-201">Både i filterrutan och på sidan för förfrågan anger du filterkriterier i rutan under filterfältet.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-201">Both in the filter pane and on a request page, you enter your filter criteria in the box under the filter field.</span></span>

<span data-ttu-id="bd4b1-202">Typen av filterfält som du vill filtrera avgör vilka kriterier du kan ange.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-202">The type of the filter field determines which criteria you can enter.</span></span> <span data-ttu-id="bd4b1-203">Till exempel kommer filtrering av ett fält som har fasta värden bara låta dig välja mellan dessa värden.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-203">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="bd4b1-204">Mer information om särskilda filtersymboler finns i [Filterkriterier](#FilterCriteria) och [Filtertoken](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-204">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="bd4b1-205">Kolumner som redan har filter som indikeras av ikonen ![filterikon](media/ui-search/filter-icon.png "Filterikon") i kolumnrubriken.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-205">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") icon in the column heading.</span></span> <span data-ttu-id="bd4b1-206">Om du vill ta bort ett filter på en sida klickar du på listpilen i sidrubriken och klickar sedan på åtgärden **Rensa filter**.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-206">To remove a filter, choose the drop-down arrow, and then choose the **Clear Filter** action.</span></span>

> [!TIP]
> <span data-ttu-id="bd4b1-207">Sök och analysera dina data snabbare genom att använda kombinationer av kortkommandon.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-207">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="bd4b1-208">Exempelvis markerar du ett fält, använder **Skift + Alt + F3** om du vill lägga till fältet i filterrutan, använder **Ctrl + Retur** om du vill återgå till raderna, markerar ett annat fält och använder **Alt + F3** för att filtrera det värdet.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-208">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span> <span data-ttu-id="bd4b1-209">Mer information finns i [Kortkommandon](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-209">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

### <a name="filter-criteria-and-symbols"></a><span data-ttu-id="bd4b1-210"><a name="FilterCriteria"> </a>Filterkriterier och symboler</span><span class="sxs-lookup"><span data-stu-id="bd4b1-210"><a name="FilterCriteria"> </a>Filter Criteria and Symbols</span></span>

<span data-ttu-id="bd4b1-211">När du anger kriterier kan du använda alla siffror och bokstäver som du normalt kan använda i fältet.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-211">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="bd4b1-212">Dessutom kan du använda specialtecken (eller operatorer) som du vill filtrera resultatet ytterligare.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-212">In addition, you can use special symbols (or operators) to further filter the results.</span></span> <span data-ttu-id="bd4b1-213">I tabellen nedan visas de symboler som kan användas i filter.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-213">The following tables show the symbols that can be used in filters.</span></span> <span data-ttu-id="bd4b1-214">För datum och tid kan du också se [Arbeta med kalenderdatum och tider](ui-enter-date-ranges.md) för mer detaljerad information.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-214">For dates and times, you can also refer to [Working with Calendar Dates and Times](ui-enter-date-ranges.md) for more detailed information.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="bd4b1-215">Det kan finnas fall där fältvärdena innehåller dessa symboler och du vill filtrera efter de.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-215">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="bd4b1-216">Genom att ibland behöva du inkludera det filteruttryck som innehåller symbolen med citattecken (”).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-216">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="bd4b1-217">Om du exempelvis vill filtrera poster som börjar med texten till exempel *S&R* är filteruttrycket `'S&R*'`.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-217">For example, if you want to filter on records that start with the text *S&R*, the filter expression is `'S&R*'`.</span></span>

<span data-ttu-id="bd4b1-218">I följande avsnitt beskrivs hur du använder olika operatorer.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-218">The following sections describe how to use the different operators.</span></span>

> [!NOTE]
> <span data-ttu-id="bd4b1-219">Om det finns fler än 200 operatorer i ett enda filter, systemet grupperar automatiskt några uttryck inom parenteser `()` i syfte att behandla det.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-219">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="bd4b1-220">Det påverkar inte filtret eller resultaten.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-220">This has no effect on the filter or the results.</span></span>  

#### <a name="-interval"></a><span data-ttu-id="bd4b1-221">(..) Intervall</span><span class="sxs-lookup"><span data-stu-id="bd4b1-221">(..) Interval</span></span>

|<span data-ttu-id="bd4b1-222">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-222">Sample Expression</span></span>|<span data-ttu-id="bd4b1-223">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-223">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="bd4b1-224">Fr.o.m. 1100 t.o.m. 2100</span><span class="sxs-lookup"><span data-stu-id="bd4b1-224">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="bd4b1-225">Alla t.o.m. 2500</span><span class="sxs-lookup"><span data-stu-id="bd4b1-225">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="bd4b1-226">Datum t.o.m. 00-12-31</span><span class="sxs-lookup"><span data-stu-id="bd4b1-226">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="bd4b1-227">Information för bokföringsperiod 8 och framåt</span><span class="sxs-lookup"><span data-stu-id="bd4b1-227">Information for accounting period 8 and thereafter</span></span>|  
|`..23`|<span data-ttu-id="bd4b1-228">Från startdatumet till den 23 innevarande månad, innevarande år 23:59:59</span><span class="sxs-lookup"><span data-stu-id="bd4b1-228">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="bd4b1-229">Från 23 innevarande månad, innevarande år 0:00:00 till tidsperiodens slut</span><span class="sxs-lookup"><span data-stu-id="bd4b1-229">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="bd4b1-230">Från 22 innevarande månad, innevarande år 0:00:00 till 23 innevarande månad, innevarande år 23:59:59</span><span class="sxs-lookup"><span data-stu-id="bd4b1-230">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

#### <a name="124-eitheror"></a><span data-ttu-id="bd4b1-231">(&#124;) Antingen eller</span><span class="sxs-lookup"><span data-stu-id="bd4b1-231">(&#124;) Either/or</span></span>

|<span data-ttu-id="bd4b1-232">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-232">Sample Expression</span></span>|<span data-ttu-id="bd4b1-233">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-233">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="bd4b1-234">Nummer med 1200 eller 1300</span><span class="sxs-lookup"><span data-stu-id="bd4b1-234">Numbers with 1200 or 1300</span></span>|  

#### <a name="-not-equal-to"></a><span data-ttu-id="bd4b1-235">(<>) Inte lika med</span><span class="sxs-lookup"><span data-stu-id="bd4b1-235">(<>) Not equal to</span></span>  

|<span data-ttu-id="bd4b1-236">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-236">Sample Expression</span></span>|<span data-ttu-id="bd4b1-237">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-237">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="bd4b1-238">Alla nummer förutom 0</span><span class="sxs-lookup"><span data-stu-id="bd4b1-238">All numbers except 0</span></span><br /><br /> <span data-ttu-id="bd4b1-239">SQL-serveralternativet låter dig kombinera tecknet med ett jokertecken.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-239">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="bd4b1-240">Till exempel betyder <>A\* inte lika med valfri text som börjar med A.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-240">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

#### <a name="-greater-than"></a><span data-ttu-id="bd4b1-241">(>) Större än</span><span class="sxs-lookup"><span data-stu-id="bd4b1-241">(>) Greater than</span></span>  

|<span data-ttu-id="bd4b1-242">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-242">Sample Expression</span></span>|<span data-ttu-id="bd4b1-243">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-243">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="bd4b1-244">Nummer större än 1200</span><span class="sxs-lookup"><span data-stu-id="bd4b1-244">Numbers greater than 1200</span></span>|  

#### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="bd4b1-245">(>=) Större än eller lika med</span><span class="sxs-lookup"><span data-stu-id="bd4b1-245">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="bd4b1-246">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-246">Sample Expression</span></span>|<span data-ttu-id="bd4b1-247">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-247">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="bd4b1-248">Nummer större än eller lika med 1200</span><span class="sxs-lookup"><span data-stu-id="bd4b1-248">Numbers greater than or equal to 1200</span></span>|  

#### <a name="-less-than"></a><span data-ttu-id="bd4b1-249">(<) Mindre än</span><span class="sxs-lookup"><span data-stu-id="bd4b1-249">(<) Less than</span></span>  

|<span data-ttu-id="bd4b1-250">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-250">Sample Expression</span></span>|<span data-ttu-id="bd4b1-251">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-251">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="bd4b1-252">Nummer mindre än 1200</span><span class="sxs-lookup"><span data-stu-id="bd4b1-252">Numbers less than 1200</span></span>|  

#### <a name="-less-than-or-equal-to"></a><span data-ttu-id="bd4b1-253">(<=) Mindre än eller lika med</span><span class="sxs-lookup"><span data-stu-id="bd4b1-253">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="bd4b1-254">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-254">Sample Expression</span></span>|<span data-ttu-id="bd4b1-255">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-255">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="bd4b1-256">Nummer mindre än eller lika med 1200</span><span class="sxs-lookup"><span data-stu-id="bd4b1-256">Numbers less than or equal to 1200</span></span>|  

#### <a name="-and"></a><span data-ttu-id="bd4b1-257">(&) och</span><span class="sxs-lookup"><span data-stu-id="bd4b1-257">(&) And</span></span>  

|<span data-ttu-id="bd4b1-258">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-258">Sample Expression</span></span>|<span data-ttu-id="bd4b1-259">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-259">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="bd4b1-260">Nummer som är större än 200 och mindre än 1 200.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-260">Numbers greater than 200 and less than 1200</span></span>|  

#### <a name="-an-exact-character-match"></a><span data-ttu-id="bd4b1-261">('') En exakt teckenmatchning</span><span class="sxs-lookup"><span data-stu-id="bd4b1-261">('') An exact character match</span></span>  

|<span data-ttu-id="bd4b1-262">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-262">Sample Expression</span></span>|<span data-ttu-id="bd4b1-263">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-263">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="bd4b1-264">Text som matchar man exakt och är skiftlägeskänslig.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-264">Text that matches man exactly and is case sensitive.</span></span>|  

#### <a name="-case-insensitive"></a><span data-ttu-id="bd4b1-265">(@) Okänslig för skiftläge</span><span class="sxs-lookup"><span data-stu-id="bd4b1-265">(@) Case insensitive</span></span>  

|<span data-ttu-id="bd4b1-266">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-266">Sample Expression</span></span>|<span data-ttu-id="bd4b1-267">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-267">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="bd4b1-268">Text som börjar med man och är skiftlägesokänslig.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-268">Text that starts with man and is case insensitive.</span></span>|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="bd4b1-269">(\*) Ett obestämt antal okända bokstäver</span><span class="sxs-lookup"><span data-stu-id="bd4b1-269">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="bd4b1-270">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-270">Sample Expression</span></span>|<span data-ttu-id="bd4b1-271">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-271">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="bd4b1-272">Text som innehåller ”Co” och är skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-272">Text that contains "Co" and is case sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="bd4b1-273">Text som slutar med ”Co” och är skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-273">Text that ends with "Co" and is case sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="bd4b1-274">Text som börjar med ”Co” och är skiftlägeskänsligt.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-274">Text that begins with "Co" and is case sensitive.</span></span>|  

#### <a name="-one-unknown-character"></a><span data-ttu-id="bd4b1-275">(?) En okänd bokstav</span><span class="sxs-lookup"><span data-stu-id="bd4b1-275">(?) One unknown character</span></span>  

|<span data-ttu-id="bd4b1-276">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-276">Sample Expression</span></span>|<span data-ttu-id="bd4b1-277">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-277">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="bd4b1-278">Text som exempelvis Hansen eller Hanson</span><span class="sxs-lookup"><span data-stu-id="bd4b1-278">Text such as Hansen or Hanson</span></span>|  

#### <a name="combined-format-expressions"></a><span data-ttu-id="bd4b1-279">Kombinerade formatuttryck</span><span class="sxs-lookup"><span data-stu-id="bd4b1-279">Combined Format Expressions</span></span>  

|<span data-ttu-id="bd4b1-280">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-280">Sample Expression</span></span>|<span data-ttu-id="bd4b1-281">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-281">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="bd4b1-282">Ta med post nummer 5999 och poster med nummer fr.o.m. 8100 t.o.m. 8490.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-282">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="bd4b1-283">Ta med poster med nummer mindre än eller lika med 1299 och nummer större än eller lika med 1400 (d.v.s. alla nummer utom 1300 t.o.m. 1399)</span><span class="sxs-lookup"><span data-stu-id="bd4b1-283">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="bd4b1-284">Ta med poster med nummer större än 50 och mindre än 100 (d.v.s. nummer fr.o.m. 51 t.o.m. 99)</span><span class="sxs-lookup"><span data-stu-id="bd4b1-284">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  

### <a name="filter-tokens"></a><span data-ttu-id="bd4b1-285"><a name="FilterTokens"> </a>Filtertoken</span><span class="sxs-lookup"><span data-stu-id="bd4b1-285"><a name="FilterTokens"> </a>Filter Tokens</span></span>
<span data-ttu-id="bd4b1-286">När du anger filterkriterier kan du även skriva ord som har en speciell betydelse som kallas filtertoken.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-286">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="bd4b1-287">När du har angett tokenordet, ersätts ordet med värden som det representerar.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-287">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="bd4b1-288">Detta gör filtreringen enklare genom att minska behovet av att gå till andra sidor för att söka efter värden som du vill lägga till i filtret.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-288">This makes filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="bd4b1-289">Tabellerna nedan beskriver några av de token som du kan skriva som filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-289">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="bd4b1-290">Ditt företag kanske använder egna token.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-290">Your organization may use custom tokens.</span></span> <span data-ttu-id="bd4b1-291">För mer information om den fullständiga uppsättningen med token som finns tillgängliga för dig eller om du vill lägga till fler anpassade variabler, kontakta administratören.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-291">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="bd4b1-292">Teknisk information finns i [Lägga till filtertoken](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="bd4b1-292">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>

#### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="bd4b1-293">(%me eller %userid) poster som har tilldelats dig</span><span class="sxs-lookup"><span data-stu-id="bd4b1-293">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="bd4b1-294">Använd `%me` eller `%userid` när du filtrerar i fält som innehåller användar-ID såsom fältet **Tilldelats användar-ID** om du vill visa alla poster som har tilldelats dig.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-294">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="bd4b1-295">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-295">Sample Expression</span></span>|<span data-ttu-id="bd4b1-296">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-296">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="bd4b1-297">eller</span><span class="sxs-lookup"><span data-stu-id="bd4b1-297">or</span></span><br />`%userid`|<span data-ttu-id="bd4b1-298">Poster som är tilldelade till ditt användarkonto.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-298">Records that are assigned to your user account.</span></span> |  

#### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="bd4b1-299">(%mycustomers) Kunder i Mina kunder</span><span class="sxs-lookup"><span data-stu-id="bd4b1-299">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="bd4b1-300">Använd `%mycustomers` i fältet kund**nr** om du vill visa alla poster för kunder som ingår i listan **mina kunder** i ditt rollcenter.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-300">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="bd4b1-301">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-301">Sample Expression</span></span>|<span data-ttu-id="bd4b1-302">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-302">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="bd4b1-303">Kunder i **mina kunder** i rollcentret.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-303">Customers in the **My Customers** on your Role Center.</span></span> |  

#### <a name="myitems-items-in-my-items"></a><span data-ttu-id="bd4b1-304">(%myitems) objekt i Mina objekt</span><span class="sxs-lookup"><span data-stu-id="bd4b1-304">(%myitems) Items in My Items</span></span>

<span data-ttu-id="bd4b1-305">Använd `%myitems` i fältet objekt**nr** om du vill visa alla poster för objekt som ingår i listan **mina objekt** i ditt rollcenter.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-305">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="bd4b1-306">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-306">Sample Expression</span></span>|<span data-ttu-id="bd4b1-307">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-307">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="bd4b1-308">Objekt i **mina objekt** i rollcentret.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-308">Items in the **My Items** on your Role Center.</span></span> |  

#### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="bd4b1-309">(%myvendors) Leverantörer i Mina leverantörer</span><span class="sxs-lookup"><span data-stu-id="bd4b1-309">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="bd4b1-310">Använd `%myvendors` i fältet leverantörs**nr** om du vill visa alla poster för leverantörer som ingår i listan **mina leverantörer** i ditt rollcenter.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-310">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="bd4b1-311">Exempel</span><span class="sxs-lookup"><span data-stu-id="bd4b1-311">Sample Expression</span></span>|<span data-ttu-id="bd4b1-312">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="bd4b1-312">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="bd4b1-313">Leverantörer i **mina leverantörer** i rollcentret.</span><span class="sxs-lookup"><span data-stu-id="bd4b1-313">Vendors in the **My Vendors** on your Role Center.</span></span> |  

## <a name="see-also"></a><span data-ttu-id="bd4b1-314">Se även</span><span class="sxs-lookup"><span data-stu-id="bd4b1-314">See Also</span></span>

[<span data-ttu-id="bd4b1-315">Vanliga frågor och svar om sökning och filtrering</span><span class="sxs-lookup"><span data-stu-id="bd4b1-315">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.md)  
[<span data-ttu-id="bd4b1-316">Spara och anpassa listvyer</span><span class="sxs-lookup"><span data-stu-id="bd4b1-316">Save and Personalize List Views</span></span>](ui-views.md)  
<span data-ttu-id="bd4b1-317">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bd4b1-317">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
