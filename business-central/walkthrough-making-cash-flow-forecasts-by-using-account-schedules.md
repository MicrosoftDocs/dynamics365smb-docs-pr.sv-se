---
title: "Genomgång: Utföra kassaflödesprognoser genom att använda kontouppställningar | Microsoft Docs"
description: "Den här genomgången beskriver hur du kan använda kontouppställningar för att göra kassaflödesprognoser. Kontouppställningar utför beräkningar som inte kan göras direkt i kontoplaner för kassaflöden. I kontouppställningar kan du skapa delsummor för kassainflöden och utbetalningar. Dessa delsummor kan inkluderas i nya totaler som kan användas vid kassaflödesprognoser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3747515bbea41a207c9467600065b5049b7f3575
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="9f9e6-106">Genomgång: Utföra kassaflödesprognoser genom att använda kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="9f9e6-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="9f9e6-107">Den här genomgången beskriver hur du kan använda kontouppställningar för att göra kassaflödesprognoser.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="9f9e6-108">Kontouppställningar utför beräkningar som inte kan göras direkt i kontoplaner för kassaflöden.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="9f9e6-109">I kontouppställningar kan du skapa delsummor för kassainflöden och utbetalningar.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="9f9e6-110">Dessa delsummor kan inkluderas i nya totaler som kan användas vid kassaflödesprognoser.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="9f9e6-111">Om den här genomgången</span><span class="sxs-lookup"><span data-stu-id="9f9e6-111">About This Walkthrough</span></span>  
<span data-ttu-id="9f9e6-112">I den här genomgången tas följande aktiviteter upp:</span><span class="sxs-lookup"><span data-stu-id="9f9e6-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="9f9e6-113">Lägga upp ett nytt namn för kassaflödeskontouppställningen.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="9f9e6-114">Skapa kontouppställningsrader.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="9f9e6-115">Lägga upp en ny kolumnlayout.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="9f9e6-116">Koppla en kolumnlayout till en kontouppställning.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="9f9e6-117">Visa och skriva ut kassaflödesprognosen.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="9f9e6-118">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="9f9e6-118">Prerequisites</span></span>  
<span data-ttu-id="9f9e6-119">För att kunna utföra den här genomgången behöver du:</span><span class="sxs-lookup"><span data-stu-id="9f9e6-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9f9e6-120"> installerad.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-120"> installed.</span></span>  
- <span data-ttu-id="9f9e6-121">Kassaflödeskalkylarksraderna är bokförda.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="9f9e6-122">Roller</span><span class="sxs-lookup"><span data-stu-id="9f9e6-122">Roles</span></span>  
<span data-ttu-id="9f9e6-123">Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroll:</span><span class="sxs-lookup"><span data-stu-id="9f9e6-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="9f9e6-124">Controller</span><span class="sxs-lookup"><span data-stu-id="9f9e6-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="9f9e6-125">Situation</span><span class="sxs-lookup"><span data-stu-id="9f9e6-125">Story</span></span>  
<span data-ttu-id="9f9e6-126">Ken är controller på CRONUS som varje månad gör kassaflödesprognoser.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="9f9e6-127">Han tar med ekonomi, försäljning, inköp och anläggningstillgångar i prognosen, och sedan visar han den till Sara som är ekonomichef.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="9f9e6-128">Lägga upp ett nytt kontouppställningsnamn</span><span class="sxs-lookup"><span data-stu-id="9f9e6-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="9f9e6-129">En kontouppställning består av ett kontouppställningsnamn för kassaflöde med en serie rader och en kolumnlayout.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="9f9e6-130">Så här skapar du ett nytt kontouppställningsnamn</span><span class="sxs-lookup"><span data-stu-id="9f9e6-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="9f9e6-131">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **kontouppställningar**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9f9e6-132">I fönstret **Kontouppställningsnamn** väljer du åtgärden **Ny** för att skapa ett nytt kontouppställningsnamn för kassaflöde.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-132">In the **Account Schedule Names** window, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="9f9e6-133">I fältet **Namn** anger du **Prognos**.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="9f9e6-134">I fältet **Beskrivning**, ange **Kassaflödesprognos**.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="9f9e6-135">Lämna fälten **Standard kolumnlayout** och **Analysvynamn** tomma.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="9f9e6-136">Skapa kontouppställningsrader</span><span class="sxs-lookup"><span data-stu-id="9f9e6-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="9f9e6-137">När ett kontouppställningsnamn har upprättats, definierar Ken varje rad som visas i kontouppställningen för kassaflödet.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="9f9e6-138">Ken definierar rader som kan visas i rapporter förutom rader som bara används vid beräkning.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="9f9e6-139">Så här skapar du kontouppställningsrader</span><span class="sxs-lookup"><span data-stu-id="9f9e6-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="9f9e6-140">I fönstret **Kontouppställningsnamn** väljer du det nya kontouppställningsnamnet för **Prognos** som du har skapat.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-140">In the **Account Schedule Names** window, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="9f9e6-141">På fliken **Start** i gruppen **Process** väljer du **Redigera kontouppställning**.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="9f9e6-142">I fönstret **Kontouppställning** anger du varje rad exakt som det visas i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-142">In the **Account Schedule** window, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="9f9e6-143">Med hjälp av funktionen **Infoga kassaflödeskonton** kan du snabbt välja kassaflödeskonton från kontoplanen för kassaflöde och kopiera dem till kontouppställningsrader.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="9f9e6-144">|Rad-nr|Beskrivning |Summeringstyp|Summering|Radtyp|Beloppstyp|Visa|</span><span class="sxs-lookup"><span data-stu-id="9f9e6-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="9f9e6-145">|-------|-----------|-------------|--------|--------|--- ------|----| | C10|Belopp|Nettoförändring|Transaktioner|Nettobelopp|Alltid|</span><span class="sxs-lookup"><span data-stu-id="9f9e6-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="9f9e6-146">|C20|Belopp till datum|Saldo till datum|Transaktioner|Nettobelopp|Alltid|</span><span class="sxs-lookup"><span data-stu-id="9f9e6-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="9f9e6-147">|C30|Hela räkenskapsåret|Hela räkenskapsåret|Transaktioner|Nettobelopp|Alltid|</span><span class="sxs-lookup"><span data-stu-id="9f9e6-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="9f9e6-148">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="9f9e6-149">Koppla kolumnlayouten till kontouppställningsnamnet</span><span class="sxs-lookup"><span data-stu-id="9f9e6-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="9f9e6-150">Nu kan Ken koppla kolumnlayouten till kontouppställningsnamnet.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="9f9e6-151">Så här kopplar du kolumnlayouten till kontouppställningsnamnet</span><span class="sxs-lookup"><span data-stu-id="9f9e6-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="9f9e6-152">Välj **Kontouppställningsnamnet** i fönstret **Prognos** i fältet **Namn**.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-152">In the **Account Schedule Names** window, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="9f9e6-153">I fältet **Standard kolumnlayout**, välj kolumnlayouten **Kassaflöde** som standardkolumnlayout.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="9f9e6-154">Så här visar och skriver du ut kassaflödesprognosen</span><span class="sxs-lookup"><span data-stu-id="9f9e6-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="9f9e6-155">I fönstret **Kontouppställningsnamn** väljer du åtgärden **Översikt** för att visa kassaflödesprognosen.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-155">In the **Account Schedule Names** window, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="9f9e6-156">I fönstret **Kontouppställning översikt** kan du ange ett belopp och sedan visa transaktionerna i kassaflödesprognosen som utgör beloppet.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-156">In the **Acc. Schedule Overview** window, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="9f9e6-157">Dessutom kan du visa formeln som används för att beräkna beloppet.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="9f9e6-158">Du kan också filtrera beloppen efter datum och dimension.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="9f9e6-159">Välj åtgärden **Skriv ut** när du vill skriva ut kassaflödesprognosen.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9f9e6-160">Se även</span><span class="sxs-lookup"><span data-stu-id="9f9e6-160">See Also</span></span>  
 <span data-ttu-id="9f9e6-161">[Arbeta med kontouppställningar](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="9f9e6-161">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="9f9e6-162">Genomgång av affärsprocesser</span><span class="sxs-lookup"><span data-stu-id="9f9e6-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="9f9e6-163">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9f9e6-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

