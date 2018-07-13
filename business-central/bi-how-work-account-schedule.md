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
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 69034b0eb97b595d0fbf5795e1fac34ecd775afe
ms.contentlocale: sv-se
ms.lasthandoff: 06/11/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a><span data-ttu-id="2a308-103">Förbereda ekonomiska rapporter, kontouppställningar och kategorier</span><span class="sxs-lookup"><span data-stu-id="2a308-103">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>
<span data-ttu-id="2a308-104">Du kan använda kontouppställningar för att få information om ekonomiska data som lagras i din kontoplan.</span><span class="sxs-lookup"><span data-stu-id="2a308-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="2a308-105">Kontouppställningar analyserar siffror för redovisningskonton och jämför redovisningstransaktioner med redovisningsbudgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="2a308-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="2a308-106">Resultaten visas i diagram i Rollcentret, till exempel diagram för kassaflöde och i rapporter såsom resultaträknings- och balansräkningsrapporter.</span><span class="sxs-lookup"><span data-stu-id="2a308-106">The results display in charts on your Role Center, such as the Cash Flow chart, and in reports, such as the Income Statement and the Balance Sheet reports.</span></span>

<span data-ttu-id="2a308-107">Du öppnar dessa två rapporter, till exempel med åtgärden **finansiella rapporter** på Business Manager och rollcenter för redovisare.</span><span class="sxs-lookup"><span data-stu-id="2a308-107">You access these two reports, for example, with the **Financials Statements** action on the Business Manager and Accountant Role Centers.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2a308-108"> innehåller några exempel på kontouppställningar som du kan använda direkt eller så kan du ange egna rader och kolumner för att jämföra siffrorna.</span><span class="sxs-lookup"><span data-stu-id="2a308-108"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="2a308-109">Du kan till exempel skapa kontouppställningar för att beräkna vinstmarginaler på dimensioner som avdelningar eller kundgrupper.</span><span class="sxs-lookup"><span data-stu-id="2a308-109">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="2a308-110">Du kan skapa så många anpassade finansiella rapporter som du önskar.</span><span class="sxs-lookup"><span data-stu-id="2a308-110">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="2a308-111">Ställa in kontouppställningar kräver en förståelse för den ekonomiska informationen i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="2a308-111">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="2a308-112">Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="2a308-112">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="2a308-113">Detta kräver att budgetar som skapas.</span><span class="sxs-lookup"><span data-stu-id="2a308-113">This requires that budgets are created.</span></span> <span data-ttu-id="2a308-114">Mer information finns i [Skapa redovisningsbudgetar](finance-how-create-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="2a308-114">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="2a308-115">Kontokategorier och kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="2a308-115">Account Categories and Account Schedules</span></span>
<span data-ttu-id="2a308-116">Du kan använda kontokategorier för att ändra layout på din redovisning.</span><span class="sxs-lookup"><span data-stu-id="2a308-116">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="2a308-117">När du har upprättat din kontokategorier i fönstret **Redovisningskontokategorier** och du väljer åtgärden **Skapa kontouppställningar** uppdateras de underliggande kontouppställningarna för de centrala ekonomiska rapporterna.</span><span class="sxs-lookup"><span data-stu-id="2a308-117">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="2a308-118">Nästa gång du kör någon av dessa rapporter, till exempel rapport för kontoavstämning kommer nya summor och underposter att läggas till, baserat på ändringarna.</span><span class="sxs-lookup"><span data-stu-id="2a308-118">The next time you run one of these reports, such as the Balance Statement report, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="2a308-119">Mer information finns i avsnittet "Kontokategorier" i [Förstå redovisning och kontoplan](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="2a308-119">For more information, see The "Account Categories" section in [Understanding the General Ledger and the COA](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="2a308-120">Så här skapar du nya kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="2a308-120">To create new account schedules</span></span>  
 <span data-ttu-id="2a308-121">Du använder kontouppställningar för att analysera siffror för redovisningskonton eller jämföra redovisningstransaktioner med redovisningsbudgettransaktioner.</span><span class="sxs-lookup"><span data-stu-id="2a308-121">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="2a308-122">Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="2a308-122">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="2a308-123">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **kontouppställningar**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2a308-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2a308-124">I fönstret **Kontouppställningsnamn** väljer du åtgärden **Ny** för att skapa ett nytt kontouppställningsnamn.</span><span class="sxs-lookup"><span data-stu-id="2a308-124">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="2a308-125">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="2a308-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="2a308-126">Välj åtgärden **Redigera kontouppställning**.</span><span class="sxs-lookup"><span data-stu-id="2a308-126">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="2a308-127">I fönstret **Kontouppställning** fyller du i fälten.</span><span class="sxs-lookup"><span data-stu-id="2a308-127">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="2a308-128">När du har skapat en ny kontouppställning och skapat raderna måste du skapa kolumner.</span><span class="sxs-lookup"><span data-stu-id="2a308-128">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="2a308-129">Du kan skapa kolumnerna manuellt eller tilldela en fördefinierad kolumnlayout till kontouppställningen.</span><span class="sxs-lookup"><span data-stu-id="2a308-129">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="2a308-130">Välj åtgärden **Redigera inställning av kolumnlayout**.</span><span class="sxs-lookup"><span data-stu-id="2a308-130">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="2a308-131">I fönstret **Kolumnlayout** fyller du i fälten.</span><span class="sxs-lookup"><span data-stu-id="2a308-131">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
> <span data-ttu-id="2a308-132">Om du inte tilldelar en standardkolumnlayout till kontouppställningen måste du  lägga upp kolumner manuellt.</span><span class="sxs-lookup"><span data-stu-id="2a308-132">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>

### <a name="to-copy-an-existing-account-schedule"></a><span data-ttu-id="2a308-133">Kopiera en befintlig kontouppställning</span><span class="sxs-lookup"><span data-stu-id="2a308-133">To copy an existing account schedule</span></span>
<span data-ttu-id="2a308-134">Kontouppställningar i standardversionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] utgör grunden för de ekonomiska standardrapporter, som kanske inte passar ditt företag.</span><span class="sxs-lookup"><span data-stu-id="2a308-134">The account schedules in the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] are the basis of the standard financial reports, which may not suit the needs of your business.</span></span> <span data-ttu-id="2a308-135">Du kan snabbt skapa dina egna finansiella rapporter, du kan starta genom att kopiera en befintlig kontouppställning.</span><span class="sxs-lookup"><span data-stu-id="2a308-135">To quickly create your own financial reports, you can start by copying an existing account schedule.</span></span>
1. <span data-ttu-id="2a308-136">I fönstret **kontouppställningar** markerar du en kontouppställning, och välj sedan åtgärden **kopiera kontouppställning**.</span><span class="sxs-lookup"><span data-stu-id="2a308-136">In the **Account Schedules** window, select an account schedule, and then choose the **Copy Account Schedule** action.</span></span>
2. <span data-ttu-id="2a308-137">I fönstret **Kopiera kontouppställning** fyller du i fälten efter behov och väljer sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a308-137">In the **Copy Account Schedule** window, fill in the fields as necessary, and then choose the **OK** button.</span></span>

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="2a308-138">Så här skapar du en kolumn för att beräkna procentsatser</span><span class="sxs-lookup"><span data-stu-id="2a308-138">To create a column that calculates percentages</span></span>  
<span data-ttu-id="2a308-139">Du kan lägga till en kolumn i en kontouppställning för att beräkna procentsatser för en summa.</span><span class="sxs-lookup"><span data-stu-id="2a308-139">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="2a308-140">Om du t.ex. har ett antal rader där försäljningen delas upp per dimension kan du lägga till en kolumn för att ange procentsatsen av total försäljning som varje rad representerar.</span><span class="sxs-lookup"><span data-stu-id="2a308-140">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="2a308-141">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **kontouppställningar**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2a308-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="2a308-142">Välj en kontouppställning i fönstret **Kontouppställningsnamn**.</span><span class="sxs-lookup"><span data-stu-id="2a308-142">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="2a308-143">Välj åtgärden **Redigera kontouppställning** för att skapa en kontouppställningsrad för att beräkna den summa som procentsatserna ska baseras på .</span><span class="sxs-lookup"><span data-stu-id="2a308-143">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="2a308-144">Infoga en rad direkt ovanför den första raden för vilken du vill visa en procentsats.</span><span class="sxs-lookup"><span data-stu-id="2a308-144">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="2a308-145">Fyll i fälten på raden på följande sätt: I fältet **summeringstyp** anger du **inställningsbas för procent**.</span><span class="sxs-lookup"><span data-stu-id="2a308-145">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="2a308-146">I fältet **Summeringsintervall** anger du en formel för den summa som procentsatsen kommer att baseras på.</span><span class="sxs-lookup"><span data-stu-id="2a308-146">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="2a308-147">Ange till exempel **11** om rad 11 innehåller den totala försäljningen.</span><span class="sxs-lookup"><span data-stu-id="2a308-147">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="2a308-148">Välj åtgärden **Redigera inställning av kolumnlayout** för att ange en kolumn.</span><span class="sxs-lookup"><span data-stu-id="2a308-148">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="2a308-149">Fyll i fälten på raden på följande sätt: I fältet **kolumntyp** väljer **formeln**.</span><span class="sxs-lookup"><span data-stu-id="2a308-149">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="2a308-150">I fältet **Formel** anger du en formel för det belopp som du vill beräkna en procentsats för, följt av %.</span><span class="sxs-lookup"><span data-stu-id="2a308-150">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="2a308-151">Om till exempel kolumn N innehåller nettoförändringen anger du **N%**.</span><span class="sxs-lookup"><span data-stu-id="2a308-151">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="2a308-152">Upprepa steg 4-7 för varje grupp av kolumner som du vill dela upp per procentsats.</span><span class="sxs-lookup"><span data-stu-id="2a308-152">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="2a308-153">Så här skapar du kontouppställningar med översikter</span><span class="sxs-lookup"><span data-stu-id="2a308-153">To set up account schedules with overviews</span></span>  
<span data-ttu-id="2a308-154">Du kan använda en kontouppställning för att skapa en rapport där redovisningssiffror jämförs med redovisningsbudgetsiffror.</span><span class="sxs-lookup"><span data-stu-id="2a308-154">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="2a308-155">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **kontouppställningar**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2a308-155">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="2a308-156">Välj en kontouppställning i fönstret **Kontouppställningsnamn**.</span><span class="sxs-lookup"><span data-stu-id="2a308-156">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="2a308-157">Välj åtgärden **Redigera kontouppställning**.</span><span class="sxs-lookup"><span data-stu-id="2a308-157">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="2a308-158">I fönstret **Kontouppställning** väljer du önskat kontouppställningsnamn i fältet **Namn**.</span><span class="sxs-lookup"><span data-stu-id="2a308-158">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="2a308-159">Välj åtgärden **Infoga konton**.</span><span class="sxs-lookup"><span data-stu-id="2a308-159">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="2a308-160">Markera de konton som du vill inkludera i utdraget och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a308-160">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="2a308-161">Kontona infogas i kontouppställningen.</span><span class="sxs-lookup"><span data-stu-id="2a308-161">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="2a308-162">Om du vill kan du ändra kolumnens layout.</span><span class="sxs-lookup"><span data-stu-id="2a308-162">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="2a308-163">Välj åtgärden **Översikt**.</span><span class="sxs-lookup"><span data-stu-id="2a308-163">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="2a308-164">Klicka på snabbfliken **Dimensionsfilter** och ställ in budgetfiltret på önskat filternamn.</span><span class="sxs-lookup"><span data-stu-id="2a308-164">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="2a308-165">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a308-165">Choose the **OK** button.</span></span>  

<span data-ttu-id="2a308-166">Nu kan du kopiera och klistra in budgetutdraget i ett kalkylblad.</span><span class="sxs-lookup"><span data-stu-id="2a308-166">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="2a308-167">Jämföra bokföringsperioder med hjälp av periodformler</span><span class="sxs-lookup"><span data-stu-id="2a308-167">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="2a308-168">Din kontouppställning kan jämföra resultaten av olika bokföringsperioder, till exempel den här månaden eller samma månad förra året.</span><span class="sxs-lookup"><span data-stu-id="2a308-168">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="2a308-169">För att göra detta lägger du till en kolumn med fältet **Formel jämförelseperiod** fält och anger sedan fältet till en periodformel.</span><span class="sxs-lookup"><span data-stu-id="2a308-169">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="2a308-170">En bokföringsperiod måste inte matcha kalendern, men varje räkenskapsår måste ha lika många bokföringsperioder, även om perioderna kan vara olika långa.</span><span class="sxs-lookup"><span data-stu-id="2a308-170">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2a308-171"> använder periodformeln för att beräkna beloppet från jämförelseperioden i förhållande till perioden som representeras av datumfiltret i en rapportbegäran.</span><span class="sxs-lookup"><span data-stu-id="2a308-171"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="2a308-172">Jämförelseperioden baseras på perioden för startdatumet i datumfiltret.</span><span class="sxs-lookup"><span data-stu-id="2a308-172">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="2a308-173">Följande förkortningar för perioder används:</span><span class="sxs-lookup"><span data-stu-id="2a308-173">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a308-174">Förkortning</span><span class="sxs-lookup"><span data-stu-id="2a308-174">Abbreviation</span></span></th>
<th><span data-ttu-id="2a308-175">Description</span><span class="sxs-lookup"><span data-stu-id="2a308-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a308-176">P</span><span class="sxs-lookup"><span data-stu-id="2a308-176">P</span></span></p></td>
<td><p><span data-ttu-id="2a308-177">Period</span><span class="sxs-lookup"><span data-stu-id="2a308-177">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a308-178">SP</span><span class="sxs-lookup"><span data-stu-id="2a308-178">LP</span></span></p></td>
<td><p><span data-ttu-id="2a308-179">Sista perioden i ett räkenskapsår, halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="2a308-179">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a308-180">CP</span><span class="sxs-lookup"><span data-stu-id="2a308-180">CP</span></span></p></td>
<td><p><span data-ttu-id="2a308-181">Aktuell period under räkenskapsåret, halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="2a308-181">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a308-182">RÅ</span><span class="sxs-lookup"><span data-stu-id="2a308-182">FY</span></span></p></td>
<td><p><span data-ttu-id="2a308-183">Räkenskapsåret.</span><span class="sxs-lookup"><span data-stu-id="2a308-183">Fiscal year.</span></span> <span data-ttu-id="2a308-184">Till exempel RÅ 1..3] anger det första kvartalet under aktuellt räkenskapsår.</span><span class="sxs-lookup"><span data-stu-id="2a308-184">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2a308-185">Exempel på formler:</span><span class="sxs-lookup"><span data-stu-id="2a308-185">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a308-186">Formel</span><span class="sxs-lookup"><span data-stu-id="2a308-186">Formula</span></span></th>
<th><span data-ttu-id="2a308-187">Description</span><span class="sxs-lookup"><span data-stu-id="2a308-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a308-188">&lt;Tomt&gt;</span><span class="sxs-lookup"><span data-stu-id="2a308-188">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="2a308-189">Aktuell period</span><span class="sxs-lookup"><span data-stu-id="2a308-189">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a308-190">-1P</span><span class="sxs-lookup"><span data-stu-id="2a308-190">-1P</span></span></p></td>
<td><p><span data-ttu-id="2a308-191">Föregående period</span><span class="sxs-lookup"><span data-stu-id="2a308-191">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a308-192">-1RÅ[1..SP]</span><span class="sxs-lookup"><span data-stu-id="2a308-192">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="2a308-193">Hela föregående räkenskapsåret</span><span class="sxs-lookup"><span data-stu-id="2a308-193">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a308-194">-1RÅ</span><span class="sxs-lookup"><span data-stu-id="2a308-194">-1FY</span></span></p></td>
<td><p><span data-ttu-id="2a308-195">Aktuell period i föregående räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="2a308-195">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a308-196">-1RÅ[1..3]</span><span class="sxs-lookup"><span data-stu-id="2a308-196">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="2a308-197">Första kvartalet i föregående räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="2a308-197">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a308-198">-1RÅ[1..LP]</span><span class="sxs-lookup"><span data-stu-id="2a308-198">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="2a308-199">Från början på föregående räkenskapsår till och med aktuell period i föregående räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="2a308-199">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a308-200">-1RÅ[LP..SP]</span><span class="sxs-lookup"><span data-stu-id="2a308-200">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="2a308-201">Från aktuell period i föregående räkenskapsår till och med sista perioden i föregående räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="2a308-201">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2a308-202">Om du vill beräkna utifrån regelbundna tidsperioder måste du skriva en formel i fältet **Jämförelse datumformel**.</span><span class="sxs-lookup"><span data-stu-id="2a308-202">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="2a308-203">Det är inte alltid transparent som perioder som du jämför eftersom du kan ange ett filter för en rapport som omfattar andra datum än de bokföringsperioder som återspeglas i data i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="2a308-203">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="2a308-204">Exempelvis kan du skapa kontouppställningar som du vill jämföra denna period med samma period föregående år, så att du kan ange **Filter för jämförande period** till *-1FY*.</span><span class="sxs-lookup"><span data-stu-id="2a308-204">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="2a308-205">Sedan kan du köra rapporten 28 februari och ange datumfilter till januari och februari.</span><span class="sxs-lookup"><span data-stu-id="2a308-205">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="2a308-206">Som ett resultat jämför kontouppställningen januari och februari i år med januari föregående år, vilket är den enda avslutade bokföringsperioden av de två för föregående år.</span><span class="sxs-lookup"><span data-stu-id="2a308-206">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="2a308-207">Se även</span><span class="sxs-lookup"><span data-stu-id="2a308-207">See Also</span></span>
[<span data-ttu-id="2a308-208">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="2a308-208">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="2a308-209">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="2a308-209">Finance</span></span>](finance.md)  
[<span data-ttu-id="2a308-210">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="2a308-210">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="2a308-211">Redovisningen och kontoplanen</span><span class="sxs-lookup"><span data-stu-id="2a308-211">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="2a308-212">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2a308-212">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

