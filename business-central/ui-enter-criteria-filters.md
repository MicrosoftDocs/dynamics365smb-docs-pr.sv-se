---
title: Sortering, sökning och filtrering av listor | Microsoft Docs
description: Arbeta effektivt i listor genom att söka i data, sortera kolumner och förfina resultaten med hjälp av filtersymboler och kortkommandon.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a27556350851de61bd31504d0c29ef60df6d890a
ms.sourcegitcommit: 921f0c4043dcda2fb8fc35df1b64310bf32270d7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017180"
---
# <a name="sorting-searching-and-filtering"></a><span data-ttu-id="0efa5-103">Sortera, söka och filtrera</span><span class="sxs-lookup"><span data-stu-id="0efa5-103">Sorting, Searching, and Filtering</span></span>

<span data-ttu-id="0efa5-104">Det finns några saker som du kan göra som hjälper dig att söka, hitta och begränsa poster i en lista eller i en rapport eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="0efa5-104">There are a few things that you can do that will help you scan, find, and limit records on a list or in a report or XMLport.</span></span> <span data-ttu-id="0efa5-105">Dessa inkluderar sortering, sökning och filtrering.</span><span class="sxs-lookup"><span data-stu-id="0efa5-105">These include sorting, searching, and filtering.</span></span> <span data-ttu-id="0efa5-106">Du kan använda några eller alla av dessa samtidigt för att snabbt söka efter och analysera data.</span><span class="sxs-lookup"><span data-stu-id="0efa5-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

<span data-ttu-id="0efa5-107">För rapporter och XMLportar kan du, som i listor, ange filter för att begränsa vilka data som ska tas med i rapporten eller din XMLport, men du kan inte sortera eller söka.</span><span class="sxs-lookup"><span data-stu-id="0efa5-107">For reports and XMLports, as on lists, you can set filters to delimit which data to include in the report or XMLport, but you can't sort and search.</span></span>

> [!TIP]
> <span data-ttu-id="0efa5-108">När du visar data sida vid sida kan du söka och använda filtrering.</span><span class="sxs-lookup"><span data-stu-id="0efa5-108">When viewing your data as tiles, you can search and use filtering.</span></span> <span data-ttu-id="0efa5-109">Om du vill använda alla kraftfulla funktioner för sortering, sökning och filtrering, väljer du ikonen ![Visa som lista](media/ui_show_as_list_icon.png "Visa som vänster listpil") om du vill visa posterna som en lista.</span><span class="sxs-lookup"><span data-stu-id="0efa5-109">To use the full set of powerful features for sorting, searching, and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to view the records as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="0efa5-110">Sortering</span><span class="sxs-lookup"><span data-stu-id="0efa5-110">Sorting</span></span>

<span data-ttu-id="0efa5-111">Med hjälp av sorteringsfunktionen kan du snabbt få en överblick över dina data.</span><span class="sxs-lookup"><span data-stu-id="0efa5-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="0efa5-112">Om du har många kunder kan du till exempelsortera dem efter **Kundnr.**, **Valutakod** eller **Lands-/regionkod** för att få den översikt du behöver.</span><span class="sxs-lookup"><span data-stu-id="0efa5-112">For example, if you have many customers,  you could sort them by **Customer No.**, **Currency Code**, or **Country Region Code** to get the overview you need.</span></span>

<span data-ttu-id="0efa5-113">Om du vill sortera en lista kan du antingen:</span><span class="sxs-lookup"><span data-stu-id="0efa5-113">To sort a list, you can either:</span></span>

- <span data-ttu-id="0efa5-114">Välja en kolumnrubrikstext för att växla mellan stigande och fallande ordning, eller</span><span class="sxs-lookup"><span data-stu-id="0efa5-114">Choose a column heading text to toggle between ascending and descending order, or</span></span>
- <span data-ttu-id="0efa5-115">Välja listpilen i kolumnrubriken och sedan välja åtgärden **Stigande** eller **Fallande**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-115">Choose the drop-down arrow in the column heading, then choose the **Ascending** or **Descending** action.</span></span>  

> [!NOTE]  
> <span data-ttu-id="0efa5-116">Sortering stöds inte på bilder, BLOB-fält, FlowFilter och fält som inte tillhör samma tabell.</span><span class="sxs-lookup"><span data-stu-id="0efa5-116">Sorting isn't supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="0efa5-117">Sökning</span><span class="sxs-lookup"><span data-stu-id="0efa5-117">Searching</span></span>

<!--## Searching by using the Quick Filter -->
<span data-ttu-id="0efa5-118">Högst upp på varje listsida finns åtgärden ![Sök lista](media/ui-search/search-list.png "Ikon för Söklista") **Sök** som ger ett snabbt och enkelt sätt att minska posterna i en lista och enbart visa de poster som innehåller de data som du är intresserad av att se.</span><span class="sxs-lookup"><span data-stu-id="0efa5-118">At the top of each list page, there's a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** action that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you're interested in seeing.</span></span>

<span data-ttu-id="0efa5-119">Sök genom att helt enkelt markera åtgärden **Sök** och ange sedan den text som du vill söka efter i rutan.</span><span class="sxs-lookup"><span data-stu-id="0efa5-119">To search, just choose the **Search** action, and then in the box, type the text that you're looking for.</span></span> <span data-ttu-id="0efa5-120">Du kan ange bokstäver, siffror och andra symboler.</span><span class="sxs-lookup"><span data-stu-id="0efa5-120">You can enter letters, numbers, and other symbols.</span></span>

<span data-ttu-id="0efa5-121">Vanligtvis försöker sökningen matcha text i alla fält.</span><span class="sxs-lookup"><span data-stu-id="0efa5-121">In general, search will attempt to match text across all fields.</span></span> <span data-ttu-id="0efa5-122">Den skiljer inte mellan versaler och gemener (den är alltså skiftlägesokänslig) och matchar texten som placeras var som helst i fältet – i början, i slutet eller i mitten.</span><span class="sxs-lookup"><span data-stu-id="0efa5-122">It doesn't distinguish between uppercase and lowercase characters (case insensitive) and will match text placed anywhere in the field, at the beginning, end, or in the middle.</span></span>

> [!TIP]
> <span data-ttu-id="0efa5-123">Du kan trycka på **F3** för att aktivera och avaktivera sökrutan.</span><span class="sxs-lookup"><span data-stu-id="0efa5-123">You can press **F3** to activate and deactivate the search box.</span></span> <span data-ttu-id="0efa5-124">Mer information finns i [Kortkommandon](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="0efa5-124">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

> [!NOTE]  
> <span data-ttu-id="0efa5-125">Sökningen matchar inte värden i bilder, BLOB-fält, FlowFilter, FlowFields och andra fält som inte ingår i en tabell.</span><span class="sxs-lookup"><span data-stu-id="0efa5-125">Search won't match values in images, BLOB fields, FlowFilters, FlowFields, and other fields that aren't part of a table.</span></span>


### <a name="fine-tuning-the-search-with-filter-criteria"></a><span data-ttu-id="0efa5-126">Finjustera sökningen med filtervillkor</span><span class="sxs-lookup"><span data-stu-id="0efa5-126">Fine-tuning the Search with Filter criteria</span></span>

<span data-ttu-id="0efa5-127">Du kan göra en mer exakt sökning genom att använda filteroperatorer, uttryck och filter-token.</span><span class="sxs-lookup"><span data-stu-id="0efa5-127">You can make a more exact search by using filter operators, expressions, and filter tokens.</span></span> <span data-ttu-id="0efa5-128">Till skillnad från vid filtrering används dessa i alla fält när de används i sökrutan, vilket gör dem mindre effektiva än vid filtrering.</span><span class="sxs-lookup"><span data-stu-id="0efa5-128">Unlike filtering, these are applied across all fields when used in the search box, making them less efficient than filtering.</span></span>

- <span data-ttu-id="0efa5-129">För att hitta endast fältvärden som matchar hela texten och fallet exakt, placera söktexten mellan enskilda citat `''` (till exempel `'man'`).</span><span class="sxs-lookup"><span data-stu-id="0efa5-129">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="0efa5-130">För att hitta fältvärden som börjar med en viss text och matchar gemener/versaler, placera `*` efter söktexten (till exempel `man*`).</span><span class="sxs-lookup"><span data-stu-id="0efa5-130">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="0efa5-131">För att hitta fältvärden som slutar med en viss text och matchar gemener/versaler, placera `*` före söktexten (till exempel `*man`).</span><span class="sxs-lookup"><span data-stu-id="0efa5-131">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="0efa5-132">Om du använder `''` eller `*` är sökningen skiftlägeskänslig.</span><span class="sxs-lookup"><span data-stu-id="0efa5-132">When using  `''` or `*`, the search is case-sensitive.</span></span> <span data-ttu-id="0efa5-133">Om du vill göra sökningen skiftlägeskänsligt, placera `@` före texten (till exempel `@man*`).</span><span class="sxs-lookup"><span data-stu-id="0efa5-133">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="0efa5-134">I tabellen nedan finns några exempel som förklarar hur du kan använda sökningen.</span><span class="sxs-lookup"><span data-stu-id="0efa5-134">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="0efa5-135">Sökkriterier</span><span class="sxs-lookup"><span data-stu-id="0efa5-135">Search Criteria</span></span>|<span data-ttu-id="0efa5-136">Söker efter...</span><span class="sxs-lookup"><span data-stu-id="0efa5-136">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="0efa5-137">eller</span><span class="sxs-lookup"><span data-stu-id="0efa5-137">or</span></span> <br />`Man`|<span data-ttu-id="0efa5-138">Alla poster med fält som innehåller texten **man**, oavsett gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="0efa5-138">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="0efa5-139">Till exempel **Manchester**, **manuell**, eller **Idrottsman**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-139">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="0efa5-140">Alla poster med fält som endast innehåller texten **Man** som matchar gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="0efa5-140">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="0efa5-141">Alla poster med fält som börjar med texten <b>Man</b>, som matchar gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="0efa5-141">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="0efa5-142">Till exempel **Manchester** men inte **manuell**, eller **Idrottsman**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-142">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="0efa5-143">Alla poster med fält som börjar med texten **man** oavsett om de är gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="0efa5-143">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="0efa5-144">Till exempel **Manchester** och **manuell** men inte **Idrottsman**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-144">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="0efa5-145">Alla poster som slutar med texten **man** oavsett om de är gemener eller versaler.</span><span class="sxs-lookup"><span data-stu-id="0efa5-145">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="0efa5-146">Till exempel **Idrottsman** men inte **Manchester**, eller **manuell**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-146">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|


## <a name="filtering"></a><a name="filtering"></a><span data-ttu-id="0efa5-147">Filtrering</span><span class="sxs-lookup"><span data-stu-id="0efa5-147">Filtering</span></span>

<span data-ttu-id="0efa5-148">Filtrering ger ett mer avancerat och flexibelt sätt att kontrollera vilka poster som ska inkluderas i en lista, en rapport eller i XMLport.</span><span class="sxs-lookup"><span data-stu-id="0efa5-148">Filtering provides a more advanced and versatile way to control which records are included in a list, report, or XMLport.</span></span> <span data-ttu-id="0efa5-149">Det finns två stora skillnader mellan sökning och filtrering, enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="0efa5-149">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="0efa5-150">**Sökning**</span><span class="sxs-lookup"><span data-stu-id="0efa5-150">**Searching**</span></span> | <span data-ttu-id="0efa5-151">**Filtrering**</span><span class="sxs-lookup"><span data-stu-id="0efa5-151">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="0efa5-152">**Tillämpliga fält**</span><span class="sxs-lookup"><span data-stu-id="0efa5-152">**Applicable Fields**</span></span> | <span data-ttu-id="0efa5-153">Söker i alla fält som visas på sidan.</span><span class="sxs-lookup"><span data-stu-id="0efa5-153">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="0efa5-154">Filtrerar ett eller flera fält individuellt med val från något av fälten i tabellen, inklusive fält som inte visas på sidan.</span><span class="sxs-lookup"><span data-stu-id="0efa5-154">Filters one or more fields individually, selecting from any field on the table, including fields that aren't visible on the page.</span></span> |
| <span data-ttu-id="0efa5-155">**Matchning**</span><span class="sxs-lookup"><span data-stu-id="0efa5-155">**Matching**</span></span> | <span data-ttu-id="0efa5-156">Visar poster med fält som matchar söktexten, oavsett versaler eller gemener i texten eller dess placering.</span><span class="sxs-lookup"><span data-stu-id="0efa5-156">Displays records with fields that match the search text, no matter the text's case or placement in the field.</span></span> | <span data-ttu-id="0efa5-157">Visar poster där fältet matchar filtret exakt, inklusive skiftlägeskänsligheten, såvida inte särskilda filtersymboler har angetts.</span><span class="sxs-lookup"><span data-stu-id="0efa5-157">Displays records where the field exactly matches the filter, including the text's case, unless special filter symbols are entered.</span></span>

<span data-ttu-id="0efa5-158">Filtrering låter dig visa poster för specifika konton eller kunder, datum, belopp och annan information genom att ange filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="0efa5-158">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="0efa5-159">Endast poster som matchar kriteriet visas i listan eller tas med i rapporten, batch-jobbet eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="0efa5-159">Only records that match the criteria are displayed on the list or included in the report, batch job, or XMLport.</span></span> <span data-ttu-id="0efa5-160">Om du anger kriterier för flera fält, kommer endast posterna som matchar alla kriterier att visas.</span><span class="sxs-lookup"><span data-stu-id="0efa5-160">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

<span data-ttu-id="0efa5-161">För listor visas filtren i ett filterfönster som visas till vänster om listan när du aktiverar den.</span><span class="sxs-lookup"><span data-stu-id="0efa5-161">For lists, the filters are displayed on a filter pane that appears to the left of the list when you activate it.</span></span> <span data-ttu-id="0efa5-162">För rapporter, batch-jobb och XMLport-kolumner visas filtren direkt på sidan för begäran.</span><span class="sxs-lookup"><span data-stu-id="0efa5-162">For reports, batch jobs, and XMLports, the filters are visible directly on the request page.</span></span>

### <a name="filtering-with-option-fields"></a><span data-ttu-id="0efa5-163">Filtrera med alternativfält</span><span class="sxs-lookup"><span data-stu-id="0efa5-163">Filtering with Option Fields</span></span>

<span data-ttu-id="0efa5-164">För "vanliga" fält som innehåller data, inställningsdatum eller affärsdata kan du ange filter både genom att markera data och genom att ange filtervärden, och du kan använda symboler för att definiera avancerade filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="0efa5-164">For "ordinary" fields that hold data, setup date, or business data, you can set filters both by selecting data and by typing filter values, and you can use symbols to define advanced filter criteria.</span></span> <span data-ttu-id="0efa5-165">Mer information finns i [Ange filtervillkor](ui-enter-criteria-filters.md#entering-filter-criteria).</span><span class="sxs-lookup"><span data-stu-id="0efa5-165">For more information, see [Entering Filter Criteria](ui-enter-criteria-filters.md#entering-filter-criteria).</span></span>

<span data-ttu-id="0efa5-166">För fält av typen **alternativ** kan du bara ange ett filter genom att välja ett eller flera alternativ i en listruta med tillgängliga alternativ.</span><span class="sxs-lookup"><span data-stu-id="0efa5-166">For fields of type **Option**, however, you can only set a filter by selecting one or more options from a drop-down list of the available options.</span></span> <span data-ttu-id="0efa5-167">Ett exempel på ett alternativfält är fältet **status** på sidan **försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-167">An example of an option field is the **Status** field on the **Sales Orders** page.</span></span>

> [!NOTE]
> <span data-ttu-id="0efa5-168">När du väljer flera alternativ som filtervärde definieras relationen mellan alternativen som *ELLER*.</span><span class="sxs-lookup"><span data-stu-id="0efa5-168">When you select multiple options as a filter value, the relationship between the options is defined as *OR*.</span></span> <span data-ttu-id="0efa5-169">Om du till exempel markerar både kryssrutan **öppna** och **släppta** i fältet **status** på sidan **försäljningsorder** betyder det att försäljningsorder som antingen är öppna eller släppta visas.</span><span class="sxs-lookup"><span data-stu-id="0efa5-169">For example, if you select both the **Open** and the **Released** check box in the **Status** filter field on the **Sales Orders** page, it means that sales orders that are either open or released are displayed.</span></span>

### <a name="setting-filters-on-lists"></a><span data-ttu-id="0efa5-170">Ange filter för listor</span><span class="sxs-lookup"><span data-stu-id="0efa5-170">Setting Filters on Lists</span></span>

<span data-ttu-id="0efa5-171">I listor anger du filter genom att använda filterrutan.</span><span class="sxs-lookup"><span data-stu-id="0efa5-171">On lists, you set filters by using the filter pane.</span></span> <span data-ttu-id="0efa5-172">Om du vill visa filterrutan för en lista väljer du listpilen bredvid sidans namn och väljer sedan åtgärden **Visa filterruta**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-172">To display the filter pane for a list, choose the drop-down arrow next to the name of the page, and then choose the **Show filter pane** action.</span></span> <span data-ttu-id="0efa5-173">Du kan också trycka på **Shift+F3**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-173">Alternatively, press **Shift+F3**.</span></span>

<span data-ttu-id="0efa5-174">Om du vill visa filterrutan för en kolumn på en lista väljer du listpilen bredvid och väljer sedan åtgärden **Filter**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-174">To display the filter pane for a column on a list, choose the drop-down arrow, and then choose the **Filter** action.</span></span> <span data-ttu-id="0efa5-175">Du kan också trycka på **Shift+F3**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-175">Alternatively, press **Shift+F3**.</span></span> <span data-ttu-id="0efa5-176">Filterrutan öppnas och den markerade kolumnen visas som ett filterfält i avsnittet **Filtrera lista efter**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-176">The filter pane opens with the selected column shown as a filter field in the **Filter list by** section.</span></span>

<span data-ttu-id="0efa5-177">Filterrutan visar en lista över aktuella filter för en lista och gör att du kan ställa in egna anpassade filter på ett eller flera fält genom att välja åtgärden **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-177">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields by choosing the **+ Filter** action.</span></span>

 <span data-ttu-id="0efa5-178">En filterruta är indelad i tre avsnitt: **Vyer**, **Filtrera lista efter** och **Filtrera summor efter**:</span><span class="sxs-lookup"><span data-stu-id="0efa5-178">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="0efa5-179">**Vyer**</span><span class="sxs-lookup"><span data-stu-id="0efa5-179">**Views**</span></span>

  <span data-ttu-id="0efa5-180">Vissa listor inkluderar avsnittet **Vyer**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-180">Some lists include the **Views** section.</span></span> <span data-ttu-id="0efa5-181">Vyer är varianter av listan som har förkonfigurerats med filter.</span><span class="sxs-lookup"><span data-stu-id="0efa5-181">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="0efa5-182">Du kan definiera och spara hur många vyer du vill per lista.</span><span class="sxs-lookup"><span data-stu-id="0efa5-182">You can define and save as many views as you want per list.</span></span> <span data-ttu-id="0efa5-183">Vyerna blir tillgängliga för dig på alla enheter som du loggar in på.</span><span class="sxs-lookup"><span data-stu-id="0efa5-183">The views will be available to you on any device you sign into.</span></span> <span data-ttu-id="0efa5-184">Mer information finns i avsnittet [Spara och anpassa listvyer](ui-views.md).</span><span class="sxs-lookup"><span data-stu-id="0efa5-184">For more information, see [Save and Personalize List Views](ui-views.md).</span></span>

- <span data-ttu-id="0efa5-185">**Filtrera lista efter**</span><span class="sxs-lookup"><span data-stu-id="0efa5-185">**Filter list by**</span></span>

  <span data-ttu-id="0efa5-186">Det är i detta avsnitt som du lägger till filter på särskilda fält för att minska antalet visade poster.</span><span class="sxs-lookup"><span data-stu-id="0efa5-186">This section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="0efa5-187">För att lägga till ett filter väljer du åtgärden **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-187">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="0efa5-188">Därefter anger du namnet på det fält som du vill filtrera listan efter eller väljer ett fält i listrutan.</span><span class="sxs-lookup"><span data-stu-id="0efa5-188">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

- <span data-ttu-id="0efa5-189">**Filtrera summor efter**</span><span class="sxs-lookup"><span data-stu-id="0efa5-189">**Filter totals by**</span></span>

  <span data-ttu-id="0efa5-190">Vissa listor som visar beräknade fält, till exempel belopp och kvantitet, inkluderar avsnittet **Filtrera summor efter** där du kan justera olika dimensioner som påverkar beräkningar.</span><span class="sxs-lookup"><span data-stu-id="0efa5-190">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="0efa5-191">För att lägga till ett filter väljer du åtgärden **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-191">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="0efa5-192">Därefter anger du namnet på det fält som du vill filtrera listan efter eller väljer ett fält i listrutan.</span><span class="sxs-lookup"><span data-stu-id="0efa5-192">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="0efa5-193">Filter i avsnittet **Filtrera summor efter** styrs av FlowFilter på sidans design.</span><span class="sxs-lookup"><span data-stu-id="0efa5-193">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="0efa5-194">Teknisk information finns i [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="0efa5-194">For technical information, see [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>

<span data-ttu-id="0efa5-195">Du kan ställa in ett enkelt filter direkt på en lista i med hjälp av filterrutan, nämligen ett filter som visar endast poster med samma värde som i den markerade cellen.</span><span class="sxs-lookup"><span data-stu-id="0efa5-195">You can set a simple filter directly on a list within using the filter pane, namely a filter that displays only records with the same value as in the selected cell.</span></span> <span data-ttu-id="0efa5-196">Välj en cell på listan, välj listpilen bredvid och väljer sedan åtgärden **Filtrera på det här värdet**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-196">Select a cell on the list, choose the drop-down arrow, and then choose the **Filter to This Value** action.</span></span> <span data-ttu-id="0efa5-197">Du kan också trycka på **Alt+F3**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-197">Alternatively, press **Alt+F3**.</span></span>

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a><span data-ttu-id="0efa5-198">Ange filter i rapporter, batch-jobb och XMLport</span><span class="sxs-lookup"><span data-stu-id="0efa5-198">Setting Filters in Reports, Batch Jobs, and XMLports</span></span>

<span data-ttu-id="0efa5-199">För rapporter och XMLport-kolumner visas filtren direkt på sidan för begäran.</span><span class="sxs-lookup"><span data-stu-id="0efa5-199">For reports and XMLports, the filters are visible directly on the request page.</span></span> <span data-ttu-id="0efa5-200">På sidan för begäran visas de filter som används senast enligt ditt val i fältet **Använd standardvärden från**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-200">The request page displays the last used filters according to your selection in the **Use default values from** field.</span></span> <span data-ttu-id="0efa5-201">Mer information finns i [Använda sparade inställningar](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="0efa5-201">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="0efa5-202">I huvudavsnittet **filter** visas de standardfilterfält som du använder för att avgränsa vilka poster som ska ingå i rapporten or XMLport.</span><span class="sxs-lookup"><span data-stu-id="0efa5-202">The main **Filter** section shows the default filter fields that you use to delimit which records to include in the report or XMLport.</span></span> <span data-ttu-id="0efa5-203">För att lägga till ett filter väljer du åtgärden **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-203">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="0efa5-204">Därefter anger du namnet på det fält som du vill filtrera efter eller väljer ett fält i listrutan.</span><span class="sxs-lookup"><span data-stu-id="0efa5-204">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

<span data-ttu-id="0efa5-205">I avsnittet **Filtrera summor efter** kan du justera olika dimensioner som påverkar beräkningarna i rapporten eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="0efa5-205">In the **Filter totals by** section, you can adjust various dimensions that influence calculations in the report or XMLport.</span></span> <span data-ttu-id="0efa5-206">För att lägga till ett filter väljer du åtgärden **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-206">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="0efa5-207">Därefter anger du namnet på det fält som du vill filtrera efter eller väljer ett fält i listrutan.</span><span class="sxs-lookup"><span data-stu-id="0efa5-207">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

## <a name="entering-filter-criteria"></a><span data-ttu-id="0efa5-208">Ange villkor i filter</span><span class="sxs-lookup"><span data-stu-id="0efa5-208">Entering Filter Criteria</span></span>

<span data-ttu-id="0efa5-209">Både i filterrutan och på sidan för förfrågan anger du filterkriterier i rutan under filterfältet.</span><span class="sxs-lookup"><span data-stu-id="0efa5-209">Both in the filter pane and on a request page, you enter your filter criteria in the box under the filter field.</span></span>

<span data-ttu-id="0efa5-210">Typen av filterfält som du vill filtrera avgör vilka kriterier du kan ange.</span><span class="sxs-lookup"><span data-stu-id="0efa5-210">The type of the filter field determines which criteria you can enter.</span></span> <span data-ttu-id="0efa5-211">Till exempel kommer filtrering av ett fält som har fasta värden bara låta dig välja mellan dessa värden.</span><span class="sxs-lookup"><span data-stu-id="0efa5-211">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="0efa5-212">Mer information om särskilda filtersymboler finns i [Filterkriterier](#FilterCriteria) och [Filtertoken](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="0efa5-212">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="0efa5-213">Kolumner som redan har filter som indikeras av ikonen ![filterikon](media/ui-search/filter-icon.png "Filterikon") i kolumnrubriken.</span><span class="sxs-lookup"><span data-stu-id="0efa5-213">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") icon in the column heading.</span></span> <span data-ttu-id="0efa5-214">Om du vill ta bort ett filter på en sida klickar du på listpilen i sidrubriken och klickar sedan på åtgärden **Rensa filter**.</span><span class="sxs-lookup"><span data-stu-id="0efa5-214">To remove a filter, choose the drop-down arrow, and then choose the **Clear Filter** action.</span></span>

> [!TIP]
> <span data-ttu-id="0efa5-215">Sök och analysera dina data snabbare genom att använda kombinationer av kortkommandon.</span><span class="sxs-lookup"><span data-stu-id="0efa5-215">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="0efa5-216">Exempelvis markerar du ett fält, använder **Skift + Alt + F3** om du vill lägga till fältet i filterrutan, använder **Ctrl + Retur** om du vill återgå till raderna, markerar ett annat fält och använder **Alt + F3** för att filtrera det värdet.</span><span class="sxs-lookup"><span data-stu-id="0efa5-216">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span> <span data-ttu-id="0efa5-217">Mer information finns i [Kortkommandon](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="0efa5-217">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

### <a name="filter-criteria-and-operators"></a><span data-ttu-id="0efa5-218"><a name="FilterCriteria"> </a>Filterkriterier och operatorer</span><span class="sxs-lookup"><span data-stu-id="0efa5-218"><a name="FilterCriteria"> </a>Filter Criteria and Operators</span></span>

<span data-ttu-id="0efa5-219">När du anger kriterier kan du använda alla siffror och bokstäver som du normalt kan använda i fältet.</span><span class="sxs-lookup"><span data-stu-id="0efa5-219">When you enter criteria, you can use all the numbers and letters that you normally use in the field.</span></span> <span data-ttu-id="0efa5-220">Det finns emellertid även en uppsättning specialsymboler som du kan använda som operatorer för att ytterligare filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="0efa5-220">But there's also a set of special symbols that you can use as operators to further filter the results.</span></span> <span data-ttu-id="0efa5-221">I följande avsnitt beskrivs dessa symboler och hur du använder dem som operatorer i filter.</span><span class="sxs-lookup"><span data-stu-id="0efa5-221">The following sections describe these symbols and how to use them as operators in filters.</span></span>

> [!TIP]
> <span data-ttu-id="0efa5-222">Mer information om filtrering av datum och tider finns i [Arbeta med datum och tider i kalendrar](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="0efa5-222">For more information about filtering dates and times, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="0efa5-223">Situationer kan uppstå där det värde du vill applicera filter på innehåller en symbol som är en operator.</span><span class="sxs-lookup"><span data-stu-id="0efa5-223">There may be situations where the value that you want to filter on contains a symbol that's an operator.</span></span> <span data-ttu-id="0efa5-224">För mer information om hur du hanterar dessa situtioner, se [Filtrera värden som innehåller symboler](#symbols) för att få fler instruktioner kring hur situationen ska hanteras.</span><span class="sxs-lookup"><span data-stu-id="0efa5-224">For more information about handling these situtions, see [Filtering on Values That Contain Symbols](#symbols) for more instructions about handling this situation.</span></span>
>
> - <span data-ttu-id="0efa5-225">Om det finns fler än 200 operatorer i ett enda filter, systemet grupperar automatiskt några uttryck inom parenteser `()` i syfte att behandla det.</span><span class="sxs-lookup"><span data-stu-id="0efa5-225">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="0efa5-226">Det påverkar inte filtret eller resultaten.</span><span class="sxs-lookup"><span data-stu-id="0efa5-226">This has no effect on the filter or the results.</span></span>  

#### <a name="-interval"></a><span data-ttu-id="0efa5-227">(..) Intervall</span><span class="sxs-lookup"><span data-stu-id="0efa5-227">(..) Interval</span></span>

|<span data-ttu-id="0efa5-228">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-228">Sample Expression</span></span>|<span data-ttu-id="0efa5-229">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-229">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="0efa5-230">Fr.o.m. 1100 t.o.m. 2100</span><span class="sxs-lookup"><span data-stu-id="0efa5-230">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="0efa5-231">Alla t.o.m. 2500</span><span class="sxs-lookup"><span data-stu-id="0efa5-231">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="0efa5-232">Datum t.o.m. 00-12-31</span><span class="sxs-lookup"><span data-stu-id="0efa5-232">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="0efa5-233">Information för bokföringsperiod 8 och framåt</span><span class="sxs-lookup"><span data-stu-id="0efa5-233">Information for accounting period 8 and after</span></span>|  
|`..23`|<span data-ttu-id="0efa5-234">Från startdatumet till den 23 innevarande månad, innevarande år 23:59:59</span><span class="sxs-lookup"><span data-stu-id="0efa5-234">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="0efa5-235">Från 23 innevarande månad, innevarande år 0:00:00 till tidsperiodens slut</span><span class="sxs-lookup"><span data-stu-id="0efa5-235">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="0efa5-236">Från 22 innevarande månad, innevarande år 0:00:00 till 23 innevarande månad, innevarande år 23:59:59</span><span class="sxs-lookup"><span data-stu-id="0efa5-236">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

#### <a name="124-eitheror"></a><span data-ttu-id="0efa5-237">(&#124;) Antingen eller</span><span class="sxs-lookup"><span data-stu-id="0efa5-237">(&#124;) Either/or</span></span>

|<span data-ttu-id="0efa5-238">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-238">Sample Expression</span></span>|<span data-ttu-id="0efa5-239">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-239">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="0efa5-240">Nummer med 1200 eller 1300</span><span class="sxs-lookup"><span data-stu-id="0efa5-240">Numbers with 1200 or 1300</span></span>|  

#### <a name="-not-equal-to"></a><span data-ttu-id="0efa5-241">(<>) Inte lika med</span><span class="sxs-lookup"><span data-stu-id="0efa5-241">(<>) Not equal to</span></span>  

|<span data-ttu-id="0efa5-242">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-242">Sample Expression</span></span>|<span data-ttu-id="0efa5-243">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-243">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="0efa5-244">Alla nummer förutom 0</span><span class="sxs-lookup"><span data-stu-id="0efa5-244">All numbers except 0</span></span><br /><br /> <span data-ttu-id="0efa5-245">SQL-serveralternativet låter dig kombinera denna symbol med ett jokertecken.</span><span class="sxs-lookup"><span data-stu-id="0efa5-245">The SQL Server Option allows you to combine this symbol with a wild-card expression.</span></span> <span data-ttu-id="0efa5-246">Till exempel betyder <>A\* inte lika med valfri text som börjar med A.</span><span class="sxs-lookup"><span data-stu-id="0efa5-246">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

#### <a name="-greater-than"></a><span data-ttu-id="0efa5-247">(>) Större än</span><span class="sxs-lookup"><span data-stu-id="0efa5-247">(>) Greater than</span></span>  

|<span data-ttu-id="0efa5-248">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-248">Sample Expression</span></span>|<span data-ttu-id="0efa5-249">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-249">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="0efa5-250">Nummer större än 1200</span><span class="sxs-lookup"><span data-stu-id="0efa5-250">Numbers greater than 1200</span></span>|  

#### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="0efa5-251">(>=) Större än eller lika med</span><span class="sxs-lookup"><span data-stu-id="0efa5-251">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="0efa5-252">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-252">Sample Expression</span></span>|<span data-ttu-id="0efa5-253">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-253">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="0efa5-254">Nummer större än eller lika med 1200</span><span class="sxs-lookup"><span data-stu-id="0efa5-254">Numbers greater than or equal to 1200</span></span>|  

#### <a name="-less-than"></a><span data-ttu-id="0efa5-255">(<) Mindre än</span><span class="sxs-lookup"><span data-stu-id="0efa5-255">(<) Less than</span></span>  

|<span data-ttu-id="0efa5-256">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-256">Sample Expression</span></span>|<span data-ttu-id="0efa5-257">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-257">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="0efa5-258">Nummer mindre än 1200</span><span class="sxs-lookup"><span data-stu-id="0efa5-258">Numbers less than 1200</span></span>|  

#### <a name="-less-than-or-equal-to"></a><span data-ttu-id="0efa5-259">(<=) Mindre än eller lika med</span><span class="sxs-lookup"><span data-stu-id="0efa5-259">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="0efa5-260">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-260">Sample Expression</span></span>|<span data-ttu-id="0efa5-261">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-261">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="0efa5-262">Nummer mindre än eller lika med 1200</span><span class="sxs-lookup"><span data-stu-id="0efa5-262">Numbers less than or equal to 1200</span></span>|  

#### <a name="-and"></a><span data-ttu-id="0efa5-263">(&) och</span><span class="sxs-lookup"><span data-stu-id="0efa5-263">(&) And</span></span>  

|<span data-ttu-id="0efa5-264">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-264">Sample Expression</span></span>|<span data-ttu-id="0efa5-265">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="0efa5-266">Nummer som är större än 200 och mindre än 1 200.</span><span class="sxs-lookup"><span data-stu-id="0efa5-266">Numbers greater than 200 and less than 1200</span></span>|  

#### <a name="-an-exact-character-match"></a><span data-ttu-id="0efa5-267">('') En exakt teckenmatchning</span><span class="sxs-lookup"><span data-stu-id="0efa5-267">('') An exact character match</span></span>  

|<span data-ttu-id="0efa5-268">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-268">Sample Expression</span></span>|<span data-ttu-id="0efa5-269">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="0efa5-270">Text som matchar **man** exakt och är skiftlägeskänslig.</span><span class="sxs-lookup"><span data-stu-id="0efa5-270">Text that matches **man** exactly and is case-sensitive.</span></span>|  

#### <a name="-case-insensitive"></a><span data-ttu-id="0efa5-271">(@) Okänslig för skiftläge</span><span class="sxs-lookup"><span data-stu-id="0efa5-271">(@) Case insensitive</span></span>  

|<span data-ttu-id="0efa5-272">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-272">Sample Expression</span></span>|<span data-ttu-id="0efa5-273">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-273">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="0efa5-274">Text som börjar med **man** och är skiftlägesokänslig.</span><span class="sxs-lookup"><span data-stu-id="0efa5-274">Text that starts with **man** and is case insensitive.</span></span>|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="0efa5-275">(\*) Ett obestämt antal okända bokstäver</span><span class="sxs-lookup"><span data-stu-id="0efa5-275">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="0efa5-276">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-276">Sample Expression</span></span>|<span data-ttu-id="0efa5-277">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-277">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="0efa5-278">Text som innehåller **Co** och är skiftlägeskänslig.</span><span class="sxs-lookup"><span data-stu-id="0efa5-278">Text that contains **Co** and is case-sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="0efa5-279">Text som slutar med **Co** och är skiftlägeskänslig.</span><span class="sxs-lookup"><span data-stu-id="0efa5-279">Text that ends with **Co"** and is case-sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="0efa5-280">Text som börjar med **Co** och är skiftlägeskänslig.</span><span class="sxs-lookup"><span data-stu-id="0efa5-280">Text that begins with **Co** and is case-sensitive.</span></span>|  

#### <a name="-one-unknown-character"></a><span data-ttu-id="0efa5-281">(?) En okänd bokstav</span><span class="sxs-lookup"><span data-stu-id="0efa5-281">(?) One unknown character</span></span>  

|<span data-ttu-id="0efa5-282">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-282">Sample Expression</span></span>|<span data-ttu-id="0efa5-283">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-283">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="0efa5-284">Text som exempelvis **Hansen** eller **Hanson**</span><span class="sxs-lookup"><span data-stu-id="0efa5-284">Text such as **Hansen** or **Hanson**</span></span>|  

#### <a name="combined-format-expressions"></a><span data-ttu-id="0efa5-285">Kombinerade formatuttryck</span><span class="sxs-lookup"><span data-stu-id="0efa5-285">Combined Format Expressions</span></span>  

|<span data-ttu-id="0efa5-286">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-286">Sample Expression</span></span>|<span data-ttu-id="0efa5-287">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-287">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="0efa5-288">Ta med post nummer 5999 och poster med nummer fr.o.m. 8100 t.o.m. 8490.</span><span class="sxs-lookup"><span data-stu-id="0efa5-288">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="0efa5-289">Ta med poster med nummer mindre än eller lika med 1299 och nummer större än eller lika med 1400 (d.v.s. alla nummer utom 1300 t.o.m. 1399)</span><span class="sxs-lookup"><span data-stu-id="0efa5-289">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="0efa5-290">Ta med poster med nummer större än 50 och mindre än 100 (d.v.s. nummer fr.o.m. 51 t.o.m. 99)</span><span class="sxs-lookup"><span data-stu-id="0efa5-290">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a><span data-ttu-id="0efa5-291">Filtrera värden som innehåller symboler</span><span class="sxs-lookup"><span data-stu-id="0efa5-291">Filtering on Values That Contain Symbols</span></span>

<span data-ttu-id="0efa5-292">Det kan finnas fall där fältvärden innehåller någon av följande symboler:</span><span class="sxs-lookup"><span data-stu-id="0efa5-292">There may be cases where field values contain the one of the following symbols:</span></span>

- &
- <span data-ttu-id="0efa5-293">(</span><span class="sxs-lookup"><span data-stu-id="0efa5-293">(</span></span>
- <span data-ttu-id="0efa5-294">)</span><span class="sxs-lookup"><span data-stu-id="0efa5-294">)</span></span>
- =
- <span data-ttu-id="0efa5-295">&#124;</span><span class="sxs-lookup"><span data-stu-id="0efa5-295">&#124;</span></span>

<span data-ttu-id="0efa5-296">Om du vill filtrera efter någon av dessa symboler måste du placera filteruttrycket inom citattecken (`'<expression with symbol>'`).</span><span class="sxs-lookup"><span data-stu-id="0efa5-296">If you want to filter on any of these symbols, place the filter expression in single quotes (`'<expression with symbol>'`).</span></span> <span data-ttu-id="0efa5-297">Om du exempelvis vill filtrera poster som börjar med texten *J & V* blir filteruttrycket `'J & V*'`.</span><span class="sxs-lookup"><span data-stu-id="0efa5-297">For example, if you wanted to filter on records that start with the text *J & V*, the filter expression would be `'J & V*'`.</span></span>

<span data-ttu-id="0efa5-298">Detta krav är inte nödvändigt för andra symboler.</span><span class="sxs-lookup"><span data-stu-id="0efa5-298">This requirement isn't necessary for other symbols.</span></span>

### <a name="filter-tokens"></a><span data-ttu-id="0efa5-299"><a name="FilterTokens"> </a>Filtertoken</span><span class="sxs-lookup"><span data-stu-id="0efa5-299"><a name="FilterTokens"> </a>Filter Tokens</span></span>

<span data-ttu-id="0efa5-300">När du anger filterkriterier kan du även skriva ord som har en speciell betydelse som kallas filtertoken.</span><span class="sxs-lookup"><span data-stu-id="0efa5-300">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="0efa5-301">När du har angett tokenordet, ersätts ordet med värden som det representerar.</span><span class="sxs-lookup"><span data-stu-id="0efa5-301">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="0efa5-302">Filtertoken underlättar filtreringen genom att minska behovet av att gå till andra sidor för att söka efter värden som du vill lägga till i filtret.</span><span class="sxs-lookup"><span data-stu-id="0efa5-302">Filter tokens make filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="0efa5-303">Tabellerna nedan beskriver några av de token som du kan skriva som filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="0efa5-303">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="0efa5-304">Ditt företag kanske använder egna token.</span><span class="sxs-lookup"><span data-stu-id="0efa5-304">Your organization may use custom tokens.</span></span> <span data-ttu-id="0efa5-305">För mer information om den fullständiga uppsättningen med token som finns tillgängliga för dig eller om du vill lägga till fler anpassade variabler, kontakta administratören.</span><span class="sxs-lookup"><span data-stu-id="0efa5-305">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="0efa5-306">Teknisk information finns i [Lägga till filtertoken](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="0efa5-306">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>

#### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="0efa5-307">(%me eller %userid) poster som har tilldelats dig</span><span class="sxs-lookup"><span data-stu-id="0efa5-307">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="0efa5-308">Använd `%me` eller `%userid` när du filtrerar i fält som innehåller användar-ID såsom fältet **Tilldelats användar-ID** om du vill visa alla poster som har tilldelats dig.</span><span class="sxs-lookup"><span data-stu-id="0efa5-308">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="0efa5-309">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-309">Sample Expression</span></span>|<span data-ttu-id="0efa5-310">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-310">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="0efa5-311">eller</span><span class="sxs-lookup"><span data-stu-id="0efa5-311">or</span></span><br />`%userid`|<span data-ttu-id="0efa5-312">Poster som är tilldelade till ditt användarkonto.</span><span class="sxs-lookup"><span data-stu-id="0efa5-312">Records that are assigned to your user account.</span></span> |  

#### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="0efa5-313">(%mycustomers) Kunder i Mina kunder</span><span class="sxs-lookup"><span data-stu-id="0efa5-313">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="0efa5-314">Använd `%mycustomers` i fältet kund **nr** om du vill visa alla poster för kunder som ingår i listan **mina kunder** i ditt rollcenter.</span><span class="sxs-lookup"><span data-stu-id="0efa5-314">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="0efa5-315">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-315">Sample Expression</span></span>|<span data-ttu-id="0efa5-316">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-316">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="0efa5-317">Kunder i **mina kunder** i rollcentret.</span><span class="sxs-lookup"><span data-stu-id="0efa5-317">Customers in the **My Customers** on your Role Center.</span></span> |  

#### <a name="myitems-items-in-my-items"></a><span data-ttu-id="0efa5-318">(%myitems) objekt i Mina objekt</span><span class="sxs-lookup"><span data-stu-id="0efa5-318">(%myitems) Items in My Items</span></span>

<span data-ttu-id="0efa5-319">Använd `%myitems` i fältet objekt **nr** om du vill visa alla poster för objekt som ingår i listan **mina objekt** i ditt rollcenter.</span><span class="sxs-lookup"><span data-stu-id="0efa5-319">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="0efa5-320">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-320">Sample Expression</span></span>|<span data-ttu-id="0efa5-321">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-321">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="0efa5-322">Objekt i **mina objekt** i rollcentret.</span><span class="sxs-lookup"><span data-stu-id="0efa5-322">Items in the **My Items** on your Role Center.</span></span> |  

#### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="0efa5-323">(%myvendors) Leverantörer i Mina leverantörer</span><span class="sxs-lookup"><span data-stu-id="0efa5-323">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="0efa5-324">Använd `%myvendors` i fältet leverantörs **nr** om du vill visa alla poster för leverantörer som ingår i listan **mina leverantörer** i ditt rollcenter.</span><span class="sxs-lookup"><span data-stu-id="0efa5-324">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="0efa5-325">Exempel</span><span class="sxs-lookup"><span data-stu-id="0efa5-325">Sample Expression</span></span>|<span data-ttu-id="0efa5-326">Poster som visas</span><span class="sxs-lookup"><span data-stu-id="0efa5-326">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="0efa5-327">Leverantörer i **mina leverantörer** i rollcentret.</span><span class="sxs-lookup"><span data-stu-id="0efa5-327">Vendors in the **My Vendors** on your Role Center.</span></span> |  

## <a name="see-also"></a><span data-ttu-id="0efa5-328">Se även</span><span class="sxs-lookup"><span data-stu-id="0efa5-328">See Also</span></span>

[<span data-ttu-id="0efa5-329">Vanliga frågor och svar om sökning och filtrering</span><span class="sxs-lookup"><span data-stu-id="0efa5-329">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.yml)  
[<span data-ttu-id="0efa5-330">Spara och anpassa listvyer</span><span class="sxs-lookup"><span data-stu-id="0efa5-330">Save and Personalize List Views</span></span>](ui-views.md)  
<span data-ttu-id="0efa5-331">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0efa5-331">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]