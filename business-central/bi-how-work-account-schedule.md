---
title: "Skapa ekonomiska rapporter med hjälp av kontouppställningar"
description: "Beskriver hur du kan använda kontouppställningar för att skapa olika vyer och rapporten för att analysera ekonomisk prestandadata."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: sv-se
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a><span data-ttu-id="2f452-103">Arbeta med kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="2f452-103">Work with Account Schedules</span></span>
<span data-ttu-id="2f452-104">Du kan använda kontouppställningar för att få information om ekonomiska data som lagras i din kontoplan.</span><span class="sxs-lookup"><span data-stu-id="2f452-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="2f452-105">Kontouppställningar analyserar siffror för redovisningskonton och jämför redovisningstransaktioner med redovisningsbudgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="2f452-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="2f452-106">Resultaten visas i diagram i ditt Rollcenter, till exempel diagram för kassaflöde.</span><span class="sxs-lookup"><span data-stu-id="2f452-106">The results display in charts on your Role Center, such as the Cash Flow chart.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2f452-107"> innehåller några exempel på kontouppställningar som du kan använda direkt eller så kan du ange egna rader och kolumner för att jämföra siffrorna.</span><span class="sxs-lookup"><span data-stu-id="2f452-107"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="2f452-108">Du kan till exempel skapa kontouppställningar för att beräkna vinstmarginaler på dimensioner som avdelningar eller kundgrupper.</span><span class="sxs-lookup"><span data-stu-id="2f452-108">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="2f452-109">Du kan skapa så många anpassade finansiella rapporter som du önskar.</span><span class="sxs-lookup"><span data-stu-id="2f452-109">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="2f452-110">Ställa in kontouppställningar kräver en förståelse för den ekonomiska informationen i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="2f452-110">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="2f452-111">Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="2f452-111">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="2f452-112">Detta kräver att budgetar som skapas.</span><span class="sxs-lookup"><span data-stu-id="2f452-112">This requires that budgets are created.</span></span> <span data-ttu-id="2f452-113">Mer information finns i [Skapa redovisningsbudgetar](finance-how-create-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="2f452-113">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="2f452-114">Kontokategorier och kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="2f452-114">Account Categories and Account Schedules</span></span>
<span data-ttu-id="2f452-115">Du kan använda kontokategorier för att ändra layout på din redovisning.</span><span class="sxs-lookup"><span data-stu-id="2f452-115">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="2f452-116">När du har upprättat din kontokategorier i fönstret **Redovisningskontokategorier** och du väljer åtgärden **Skapa kontouppställningar** uppdateras de underliggande kontouppställningarna för de centrala ekonomiska rapporterna.</span><span class="sxs-lookup"><span data-stu-id="2f452-116">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="2f452-117">Nästa gång du kör någon av dessa rapporter, till exempel kontoavstämning kommer nya summor och underposter att läggas till, baserat på ändringarna.</span><span class="sxs-lookup"><span data-stu-id="2f452-117">The next time you run one of these reports, such as the balance statement, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="2f452-118">Mer information finns i [Redovisning och kontoplan](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="2f452-118">For more information, see [The General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="2f452-119">Så här skapar du nya kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="2f452-119">To create new account schedules</span></span>  
 <span data-ttu-id="2f452-120">Du använder kontouppställningar för att analysera siffror för redovisningskonton eller jämföra redovisningstransaktioner med redovisningsbudgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="2f452-120">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="2f452-121">Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="2f452-121">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="2f452-122">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **kontouppställningar**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2f452-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2f452-123">I fönstret **Kontouppställningsnamn** väljer du åtgärden **Ny** för att skapa ett nytt kontouppställningsnamn.</span><span class="sxs-lookup"><span data-stu-id="2f452-123">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="2f452-124">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="2f452-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="2f452-125">Välj åtgärden **Redigera kontouppställning**.</span><span class="sxs-lookup"><span data-stu-id="2f452-125">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="2f452-126">I fönstret **Kontouppställning** fyller du i fälten.</span><span class="sxs-lookup"><span data-stu-id="2f452-126">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="2f452-127">När du har skapat en ny kontouppställning och skapat raderna måste du skapa kolumner.</span><span class="sxs-lookup"><span data-stu-id="2f452-127">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="2f452-128">Du kan skapa kolumnerna manuellt eller tilldela en fördefinierad kolumnlayout till kontouppställningen.</span><span class="sxs-lookup"><span data-stu-id="2f452-128">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="2f452-129">Välj åtgärden **Redigera inställning av kolumnlayout**.</span><span class="sxs-lookup"><span data-stu-id="2f452-129">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="2f452-130">I fönstret **Kolumnlayout** fyller du i fälten.</span><span class="sxs-lookup"><span data-stu-id="2f452-130">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="2f452-131">Om du inte tilldelar en standardkolumnlayout till kontouppställningen måste du  lägga upp kolumner manuellt.</span><span class="sxs-lookup"><span data-stu-id="2f452-131">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>   

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="2f452-132">Så här skapar du en kolumn för att beräkna procentsatser</span><span class="sxs-lookup"><span data-stu-id="2f452-132">To create a column that calculates percentages</span></span>  
<span data-ttu-id="2f452-133">Du kan lägga till en kolumn i en kontouppställning för att beräkna procentsatser för en summa.</span><span class="sxs-lookup"><span data-stu-id="2f452-133">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="2f452-134">Om du t.ex. har ett antal rader där försäljningen delas upp per dimension kan du lägga till en kolumn för att ange procentsatsen av total försäljning som varje rad representerar.</span><span class="sxs-lookup"><span data-stu-id="2f452-134">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="2f452-135">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **kontouppställningar**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2f452-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="2f452-136">Välj en kontouppställning i fönstret **Kontouppställningsnamn**.</span><span class="sxs-lookup"><span data-stu-id="2f452-136">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="2f452-137">Välj åtgärden **Redigera kontouppställning** för att skapa en kontouppställningsrad för att beräkna den summa som procentsatserna ska baseras på .</span><span class="sxs-lookup"><span data-stu-id="2f452-137">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="2f452-138">Infoga en rad direkt ovanför den första raden för vilken du vill visa en procentsats.</span><span class="sxs-lookup"><span data-stu-id="2f452-138">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="2f452-139">Fyll i fälten på raden på följande sätt: I fältet **summeringstyp** anger du **inställningsbas för procent**.</span><span class="sxs-lookup"><span data-stu-id="2f452-139">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="2f452-140">I fältet **Summeringsintervall** anger du en formel för den summa som procentsatsen kommer att baseras på.</span><span class="sxs-lookup"><span data-stu-id="2f452-140">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="2f452-141">Ange till exempel **11** om rad 11 innehåller den totala försäljningen.</span><span class="sxs-lookup"><span data-stu-id="2f452-141">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="2f452-142">Välj åtgärden **Redigera inställning av kolumnlayout** för att ange en kolumn.</span><span class="sxs-lookup"><span data-stu-id="2f452-142">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="2f452-143">Fyll i fälten på raden på följande sätt: I fältet **kolumntyp** väljer **formeln**.</span><span class="sxs-lookup"><span data-stu-id="2f452-143">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="2f452-144">I fältet **Formel** anger du en formel för det belopp som du vill beräkna en procentsats för, följt av %.</span><span class="sxs-lookup"><span data-stu-id="2f452-144">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="2f452-145">Om till exempel kolumn N innehåller nettoförändringen anger du **N%**.</span><span class="sxs-lookup"><span data-stu-id="2f452-145">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="2f452-146">Upprepa steg 4-7 för varje grupp av kolumner som du vill dela upp per procentsats.</span><span class="sxs-lookup"><span data-stu-id="2f452-146">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="2f452-147">Så här skapar du kontouppställningar med översikter</span><span class="sxs-lookup"><span data-stu-id="2f452-147">To set up account schedules with overviews</span></span>  
<span data-ttu-id="2f452-148">Du kan använda en kontouppställning för att skapa en rapport där redovisningssiffror jämförs med redovisningsbudgetsiffror.</span><span class="sxs-lookup"><span data-stu-id="2f452-148">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="2f452-149">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **kontouppställningar**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2f452-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="2f452-150">Välj en kontouppställning i fönstret **Kontouppställningsnamn**.</span><span class="sxs-lookup"><span data-stu-id="2f452-150">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="2f452-151">Välj åtgärden **Redigera kontouppställning**.</span><span class="sxs-lookup"><span data-stu-id="2f452-151">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="2f452-152">I fönstret **Kontouppställning** väljer du önskat kontouppställningsnamn i fältet **Namn**.</span><span class="sxs-lookup"><span data-stu-id="2f452-152">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="2f452-153">Välj åtgärden **Infoga konton**.</span><span class="sxs-lookup"><span data-stu-id="2f452-153">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="2f452-154">Markera de konton som du vill inkludera i utdraget och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f452-154">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="2f452-155">Kontona infogas i kontouppställningen.</span><span class="sxs-lookup"><span data-stu-id="2f452-155">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="2f452-156">Om du vill kan du ändra kolumnens layout.</span><span class="sxs-lookup"><span data-stu-id="2f452-156">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="2f452-157">Välj åtgärden **Översikt**.</span><span class="sxs-lookup"><span data-stu-id="2f452-157">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="2f452-158">Klicka på snabbfliken **Dimensionsfilter** och ställ in budgetfiltret på önskat filternamn.</span><span class="sxs-lookup"><span data-stu-id="2f452-158">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="2f452-159">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f452-159">Choose the **OK** button.</span></span>  

<span data-ttu-id="2f452-160">Nu kan du kopiera och klistra in budgetutdraget i ett kalkylblad.</span><span class="sxs-lookup"><span data-stu-id="2f452-160">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="2f452-161">Jämföra bokföringsperioder med hjälp av periodformler</span><span class="sxs-lookup"><span data-stu-id="2f452-161">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="2f452-162">Din kontouppställning kan jämföra resultaten av olika bokföringsperioder, till exempel den här månaden eller samma månad förra året.</span><span class="sxs-lookup"><span data-stu-id="2f452-162">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="2f452-163">För att göra detta lägger du till en kolumn med fältet **Formel jämförelseperiod** fält och anger sedan fältet till en periodformel.</span><span class="sxs-lookup"><span data-stu-id="2f452-163">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="2f452-164">En bokföringsperiod måste inte matcha kalendern, men varje räkenskapsår måste ha lika många bokföringsperioder, även om perioderna kan vara olika långa.</span><span class="sxs-lookup"><span data-stu-id="2f452-164">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2f452-165"> använder periodformeln för att beräkna beloppet från jämförelseperioden i förhållande till perioden som representeras av datumfiltret i en rapportbegäran.</span><span class="sxs-lookup"><span data-stu-id="2f452-165"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="2f452-166">Jämförelseperioden baseras på perioden för startdatumet i datumfiltret.</span><span class="sxs-lookup"><span data-stu-id="2f452-166">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="2f452-167">Följande förkortningar för perioder används:</span><span class="sxs-lookup"><span data-stu-id="2f452-167">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2f452-168">Förkortning</span><span class="sxs-lookup"><span data-stu-id="2f452-168">Abbreviation</span></span></th>
<th><span data-ttu-id="2f452-169">Description</span><span class="sxs-lookup"><span data-stu-id="2f452-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f452-170">P</span><span class="sxs-lookup"><span data-stu-id="2f452-170">P</span></span></p></td>
<td><p><span data-ttu-id="2f452-171">Period</span><span class="sxs-lookup"><span data-stu-id="2f452-171">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f452-172">SP</span><span class="sxs-lookup"><span data-stu-id="2f452-172">LP</span></span></p></td>
<td><p><span data-ttu-id="2f452-173">Sista perioden i ett räkenskapsår, halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="2f452-173">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f452-174">CP</span><span class="sxs-lookup"><span data-stu-id="2f452-174">CP</span></span></p></td>
<td><p><span data-ttu-id="2f452-175">Aktuell period under räkenskapsåret, halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="2f452-175">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f452-176">RÅ</span><span class="sxs-lookup"><span data-stu-id="2f452-176">FY</span></span></p></td>
<td><p><span data-ttu-id="2f452-177">Räkenskapsåret.</span><span class="sxs-lookup"><span data-stu-id="2f452-177">Fiscal year.</span></span> <span data-ttu-id="2f452-178">Till exempel RÅ 1..3] anger det första kvartalet under aktuellt räkenskapsår.</span><span class="sxs-lookup"><span data-stu-id="2f452-178">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2f452-179">Exempel på formler:</span><span class="sxs-lookup"><span data-stu-id="2f452-179">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2f452-180">Formel</span><span class="sxs-lookup"><span data-stu-id="2f452-180">Formula</span></span></th>
<th><span data-ttu-id="2f452-181">Description</span><span class="sxs-lookup"><span data-stu-id="2f452-181">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f452-182">&lt;Tomt&gt;</span><span class="sxs-lookup"><span data-stu-id="2f452-182">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="2f452-183">Aktuell period</span><span class="sxs-lookup"><span data-stu-id="2f452-183">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f452-184">-1P</span><span class="sxs-lookup"><span data-stu-id="2f452-184">-1P</span></span></p></td>
<td><p><span data-ttu-id="2f452-185">Föregående period</span><span class="sxs-lookup"><span data-stu-id="2f452-185">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f452-186">-1RÅ[1..SP]</span><span class="sxs-lookup"><span data-stu-id="2f452-186">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="2f452-187">Hela föregående räkenskapsåret</span><span class="sxs-lookup"><span data-stu-id="2f452-187">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f452-188">-1RÅ</span><span class="sxs-lookup"><span data-stu-id="2f452-188">-1FY</span></span></p></td>
<td><p><span data-ttu-id="2f452-189">Aktuell period i föregående räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="2f452-189">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f452-190">-1RÅ[1..3]</span><span class="sxs-lookup"><span data-stu-id="2f452-190">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="2f452-191">Första kvartalet i föregående räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="2f452-191">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f452-192">-1RÅ[1..LP]</span><span class="sxs-lookup"><span data-stu-id="2f452-192">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="2f452-193">Från början på föregående räkenskapsår till och med aktuell period i föregående räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="2f452-193">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f452-194">-1RÅ[LP..SP]</span><span class="sxs-lookup"><span data-stu-id="2f452-194">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="2f452-195">Från aktuell period i föregående räkenskapsår till och med sista perioden i föregående räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="2f452-195">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2f452-196">Om du vill beräkna utifrån regelbundna tidsperioder måste du skriva en formel i fältet **Jämförelse datumformel**.</span><span class="sxs-lookup"><span data-stu-id="2f452-196">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="2f452-197">Det är inte alltid transparent som perioder som du jämför eftersom du kan ange ett filter för en rapport som omfattar andra datum än de bokföringsperioder som återspeglas i data i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="2f452-197">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="2f452-198">Exempelvis kan du skapa kontouppställningar som du vill jämföra denna period med samma period föregående år, så att du kan ange **Filter för jämförande period** till *-1FY*.</span><span class="sxs-lookup"><span data-stu-id="2f452-198">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="2f452-199">Sedan kan du köra rapporten 28 februari och ange datumfilter till januari och februari.</span><span class="sxs-lookup"><span data-stu-id="2f452-199">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="2f452-200">Som ett resultat jämför kontouppställningen januari och februari i år med januari föregående år, vilket är den enda avslutade bokföringsperioden av de två för föregående år.</span><span class="sxs-lookup"><span data-stu-id="2f452-200">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="2f452-201">Se även</span><span class="sxs-lookup"><span data-stu-id="2f452-201">See Also</span></span>
[<span data-ttu-id="2f452-202">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="2f452-202">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="2f452-203">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="2f452-203">Finance</span></span>](finance.md)  
[<span data-ttu-id="2f452-204">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="2f452-204">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="2f452-205">Redovisningen och kontoplanen</span><span class="sxs-lookup"><span data-stu-id="2f452-205">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="2f452-206">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2f452-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

