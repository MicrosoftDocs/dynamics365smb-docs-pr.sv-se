---
title: 'Genomgång: Utföra kassaflödesprognoser genom att använda kontouppställningar | Microsoft Docs'
description: Den här genomgången beskriver hur du kan använda kontouppställningar för att göra kassaflödesprognoser. Kontouppställningar utför beräkningar som inte kan göras direkt i kontoplaner för kassaflöden. I kontouppställningar kan du skapa delsummor för kassainflöden och utbetalningar. Dessa delsummor kan inkluderas i nya totaler som kan användas vid kassaflödesprognoser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a210792a187bde0217917659f118c58a6a135df2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756547"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="d8a03-106">Genomgång: Utföra kassaflödesprognoser genom att använda kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="d8a03-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="d8a03-107">Den här genomgången beskriver hur du kan använda kontouppställningar för att göra kassaflödesprognoser.</span><span class="sxs-lookup"><span data-stu-id="d8a03-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="d8a03-108">Kontouppställningar utför beräkningar som inte kan göras direkt i kontoplaner för kassaflöden.</span><span class="sxs-lookup"><span data-stu-id="d8a03-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="d8a03-109">I kontouppställningar kan du skapa delsummor för kassainflöden och utbetalningar.</span><span class="sxs-lookup"><span data-stu-id="d8a03-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="d8a03-110">Dessa delsummor kan inkluderas i nya totaler som kan användas vid kassaflödesprognoser.</span><span class="sxs-lookup"><span data-stu-id="d8a03-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="d8a03-111">Om den här genomgången</span><span class="sxs-lookup"><span data-stu-id="d8a03-111">About This Walkthrough</span></span>  
<span data-ttu-id="d8a03-112">I den här genomgången tas följande aktiviteter upp:</span><span class="sxs-lookup"><span data-stu-id="d8a03-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="d8a03-113">Lägga upp ett nytt namn för kassaflödeskontouppställningen.</span><span class="sxs-lookup"><span data-stu-id="d8a03-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="d8a03-114">Skapa kontouppställningsrader.</span><span class="sxs-lookup"><span data-stu-id="d8a03-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="d8a03-115">Lägga upp en ny kolumnlayout.</span><span class="sxs-lookup"><span data-stu-id="d8a03-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="d8a03-116">Koppla en kolumnlayout till en kontouppställning.</span><span class="sxs-lookup"><span data-stu-id="d8a03-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="d8a03-117">Visa och skriva ut kassaflödesprognosen.</span><span class="sxs-lookup"><span data-stu-id="d8a03-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="d8a03-118">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="d8a03-118">Prerequisites</span></span>  
<span data-ttu-id="d8a03-119">För att kunna utföra den här genomgången behöver du:</span><span class="sxs-lookup"><span data-stu-id="d8a03-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d8a03-120">installerad.</span><span class="sxs-lookup"><span data-stu-id="d8a03-120">installed.</span></span>  
- <span data-ttu-id="d8a03-121">Kassaflödeskalkylarksraderna är bokförda.</span><span class="sxs-lookup"><span data-stu-id="d8a03-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="d8a03-122">Roller</span><span class="sxs-lookup"><span data-stu-id="d8a03-122">Roles</span></span>  
<span data-ttu-id="d8a03-123">Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroll:</span><span class="sxs-lookup"><span data-stu-id="d8a03-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="d8a03-124">Controller</span><span class="sxs-lookup"><span data-stu-id="d8a03-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="d8a03-125">Situation</span><span class="sxs-lookup"><span data-stu-id="d8a03-125">Story</span></span>  
<span data-ttu-id="d8a03-126">Ken är controller på CRONUS som varje månad gör kassaflödesprognoser.</span><span class="sxs-lookup"><span data-stu-id="d8a03-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="d8a03-127">Han tar med ekonomi, försäljning, inköp och anläggningstillgångar i prognosen, och sedan visar han den till Sara som är ekonomichef.</span><span class="sxs-lookup"><span data-stu-id="d8a03-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="d8a03-128">Lägga upp ett nytt kontouppställningsnamn</span><span class="sxs-lookup"><span data-stu-id="d8a03-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="d8a03-129">En kontouppställning består av ett kontouppställningsnamn för kassaflöde med en serie rader och en kolumnlayout.</span><span class="sxs-lookup"><span data-stu-id="d8a03-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="d8a03-130">Så här skapar du ett nytt kontouppställningsnamn</span><span class="sxs-lookup"><span data-stu-id="d8a03-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="d8a03-131">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kontoscheman** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d8a03-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d8a03-132">På sidan **Kontouppställningsnamn** väljer du åtgärden **Ny** för att skapa ett nytt kontouppställningsnamn för kassaflöde.</span><span class="sxs-lookup"><span data-stu-id="d8a03-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="d8a03-133">I fältet **Namn** anger du **Prognos**.</span><span class="sxs-lookup"><span data-stu-id="d8a03-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="d8a03-134">I fältet **Beskrivning**, ange **Kassaflödesprognos**.</span><span class="sxs-lookup"><span data-stu-id="d8a03-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="d8a03-135">Lämna fälten **Standard kolumnlayout** och **Analysvynamn** tomma.</span><span class="sxs-lookup"><span data-stu-id="d8a03-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="d8a03-136">Skapa kontouppställningsrader</span><span class="sxs-lookup"><span data-stu-id="d8a03-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="d8a03-137">När ett kontouppställningsnamn har upprättats, definierar Ken varje rad som visas i kontouppställningen för kassaflödet.</span><span class="sxs-lookup"><span data-stu-id="d8a03-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="d8a03-138">Ken definierar rader som kan visas i rapporter förutom rader som bara används vid beräkning.</span><span class="sxs-lookup"><span data-stu-id="d8a03-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="d8a03-139">Så här skapar du kontouppställningsrader</span><span class="sxs-lookup"><span data-stu-id="d8a03-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="d8a03-140">På sidan **Kontouppställningsnamn** väljer du det nya kontouppställningsnamnet **Prognos** som du har skapat och väljer sedan åtgärden **Redigera kontouppställning**.</span><span class="sxs-lookup"><span data-stu-id="d8a03-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created, and then choose the **Edit Account Schedule** action.</span></span>  
2.  <span data-ttu-id="d8a03-141">På sidan **Kontouppställning** anger du varje rad exakt som det visas i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="d8a03-141">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d8a03-142">Med hjälp av funktionen **Infoga kassaflödeskonton** kan du snabbt välja kassaflödeskonton från kontoplanen för kassaflöde och kopiera dem till kontouppställningsrader.</span><span class="sxs-lookup"><span data-stu-id="d8a03-142">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    |<span data-ttu-id="d8a03-143">Rad-nr</span><span class="sxs-lookup"><span data-stu-id="d8a03-143">Row No.</span></span>|<span data-ttu-id="d8a03-144">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d8a03-144">Description</span></span>|<span data-ttu-id="d8a03-145">Summeringstyp</span><span class="sxs-lookup"><span data-stu-id="d8a03-145">Totaling Type</span></span>|<span data-ttu-id="d8a03-146">Summeringsintervall</span><span class="sxs-lookup"><span data-stu-id="d8a03-146">Totaling</span></span>|<span data-ttu-id="d8a03-147">Radtyp</span><span class="sxs-lookup"><span data-stu-id="d8a03-147">Row Type</span></span>|<span data-ttu-id="d8a03-148">Beloppstyp</span><span class="sxs-lookup"><span data-stu-id="d8a03-148">Amount Type</span></span>|<span data-ttu-id="d8a03-149">Visa</span><span class="sxs-lookup"><span data-stu-id="d8a03-149">Show</span></span>|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |<span data-ttu-id="d8a03-150">C10</span><span class="sxs-lookup"><span data-stu-id="d8a03-150">C10</span></span>|<span data-ttu-id="d8a03-151">Belopp</span><span class="sxs-lookup"><span data-stu-id="d8a03-151">Amount</span></span>|<span data-ttu-id="d8a03-152">Nettoförändring</span><span class="sxs-lookup"><span data-stu-id="d8a03-152">Net Change</span></span>|<span data-ttu-id="d8a03-153">Transaktioner</span><span class="sxs-lookup"><span data-stu-id="d8a03-153">Entries</span></span>|<span data-ttu-id="d8a03-154">Nettobelopp</span><span class="sxs-lookup"><span data-stu-id="d8a03-154">Net Amount</span></span>|<span data-ttu-id="d8a03-155">Alltid</span><span class="sxs-lookup"><span data-stu-id="d8a03-155">Always</span></span>|  
    |<span data-ttu-id="d8a03-156">C20</span><span class="sxs-lookup"><span data-stu-id="d8a03-156">C20</span></span>|<span data-ttu-id="d8a03-157">Belopp till datum</span><span class="sxs-lookup"><span data-stu-id="d8a03-157">Amount until Date</span></span>|<span data-ttu-id="d8a03-158">Saldo t.o.m. datum</span><span class="sxs-lookup"><span data-stu-id="d8a03-158">Balance at Date</span></span>|<span data-ttu-id="d8a03-159">Transaktioner</span><span class="sxs-lookup"><span data-stu-id="d8a03-159">Entries</span></span>|<span data-ttu-id="d8a03-160">Nettobelopp</span><span class="sxs-lookup"><span data-stu-id="d8a03-160">Net Amount</span></span>|<span data-ttu-id="d8a03-161">Alltid</span><span class="sxs-lookup"><span data-stu-id="d8a03-161">Always</span></span>|  
    |<span data-ttu-id="d8a03-162">C30</span><span class="sxs-lookup"><span data-stu-id="d8a03-162">C30</span></span>|<span data-ttu-id="d8a03-163">Hela räkenskapsåret</span><span class="sxs-lookup"><span data-stu-id="d8a03-163">Entire Fiscal Year</span></span>|<span data-ttu-id="d8a03-164">Hela räkenskapsåret</span><span class="sxs-lookup"><span data-stu-id="d8a03-164">Entire Fiscal Year</span></span>|<span data-ttu-id="d8a03-165">Transaktioner</span><span class="sxs-lookup"><span data-stu-id="d8a03-165">Entries</span></span>|<span data-ttu-id="d8a03-166">Nettobelopp</span><span class="sxs-lookup"><span data-stu-id="d8a03-166">Net Amount</span></span>|<span data-ttu-id="d8a03-167">Alltid</span><span class="sxs-lookup"><span data-stu-id="d8a03-167">Always</span></span>|  

4.  <span data-ttu-id="d8a03-168">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8a03-168">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="d8a03-169">Koppla kolumnlayouten till kontouppställningsnamnet</span><span class="sxs-lookup"><span data-stu-id="d8a03-169">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="d8a03-170">Nu kan Ken koppla kolumnlayouten till kontouppställningsnamnet.</span><span class="sxs-lookup"><span data-stu-id="d8a03-170">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="d8a03-171">Så här kopplar du kolumnlayouten till kontouppställningsnamnet</span><span class="sxs-lookup"><span data-stu-id="d8a03-171">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="d8a03-172">På sidan **Kontouppställningsnamnet** väljer du **Prognos** i fältet **Namn**.</span><span class="sxs-lookup"><span data-stu-id="d8a03-172">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="d8a03-173">I fältet **Standard kolumnlayout**, välj kolumnlayouten **Kassaflöde** som standardkolumnlayout.</span><span class="sxs-lookup"><span data-stu-id="d8a03-173">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="d8a03-174">Så här visar och skriver du ut kassaflödesprognosen</span><span class="sxs-lookup"><span data-stu-id="d8a03-174">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="d8a03-175">På sidan **Kontouppställningsnamn** väljer du åtgärden **Översikt** för att visa kassaflödesprognosen.</span><span class="sxs-lookup"><span data-stu-id="d8a03-175">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="d8a03-176">På sidan **Kontouppställning översikt** kan du ange ett belopp och sedan visa transaktionerna i kassaflödesprognosen som utgör beloppet.</span><span class="sxs-lookup"><span data-stu-id="d8a03-176">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="d8a03-177">Dessutom kan du visa formeln som används för att beräkna beloppet.</span><span class="sxs-lookup"><span data-stu-id="d8a03-177">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="d8a03-178">Du kan också filtrera beloppen efter datum och dimension.</span><span class="sxs-lookup"><span data-stu-id="d8a03-178">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="d8a03-179">Välj åtgärden **Skriv ut** när du vill skriva ut kassaflödesprognosen.</span><span class="sxs-lookup"><span data-stu-id="d8a03-179">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d8a03-180">Se även</span><span class="sxs-lookup"><span data-stu-id="d8a03-180">See Also</span></span>  
 <span data-ttu-id="d8a03-181">[Arbeta med kontouppställningar](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="d8a03-181">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="d8a03-182">Genomgång av affärsprocesser</span><span class="sxs-lookup"><span data-stu-id="d8a03-182">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="d8a03-183">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d8a03-183">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
