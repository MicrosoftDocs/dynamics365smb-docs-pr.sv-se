---
title: 'Genomgång: Utföra kassaflödesprognoser genom att använda kontouppställningar | Microsoft Docs'
description: Den här genomgången beskriver hur du kan använda kontouppställningar för att göra kassaflödesprognoser. Kontouppställningar utför beräkningar som inte kan göras direkt i kontoplaner för kassaflöden. I kontouppställningar kan du skapa delsummor för kassainflöden och utbetalningar. Dessa delsummor kan inkluderas i nya totaler som kan användas vid kassaflödesprognoser.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 652a151ff50c8492b3dc7df5d17c04ff2d00faad
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807096"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="9bb84-106">Genomgång: Utföra kassaflödesprognoser genom att använda kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="9bb84-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="9bb84-107">Den här genomgången beskriver hur du kan använda kontouppställningar för att göra kassaflödesprognoser.</span><span class="sxs-lookup"><span data-stu-id="9bb84-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="9bb84-108">Kontouppställningar utför beräkningar som inte kan göras direkt i kontoplaner för kassaflöden.</span><span class="sxs-lookup"><span data-stu-id="9bb84-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="9bb84-109">I kontouppställningar kan du skapa delsummor för kassainflöden och utbetalningar.</span><span class="sxs-lookup"><span data-stu-id="9bb84-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="9bb84-110">Dessa delsummor kan inkluderas i nya totaler som kan användas vid kassaflödesprognoser.</span><span class="sxs-lookup"><span data-stu-id="9bb84-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="9bb84-111">Om den här genomgången</span><span class="sxs-lookup"><span data-stu-id="9bb84-111">About This Walkthrough</span></span>  
<span data-ttu-id="9bb84-112">I den här genomgången tas följande aktiviteter upp:</span><span class="sxs-lookup"><span data-stu-id="9bb84-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="9bb84-113">Lägga upp ett nytt namn för kassaflödeskontouppställningen.</span><span class="sxs-lookup"><span data-stu-id="9bb84-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="9bb84-114">Skapa kontouppställningsrader.</span><span class="sxs-lookup"><span data-stu-id="9bb84-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="9bb84-115">Lägga upp en ny kolumnlayout.</span><span class="sxs-lookup"><span data-stu-id="9bb84-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="9bb84-116">Koppla en kolumnlayout till en kontouppställning.</span><span class="sxs-lookup"><span data-stu-id="9bb84-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="9bb84-117">Visa och skriva ut kassaflödesprognosen.</span><span class="sxs-lookup"><span data-stu-id="9bb84-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="9bb84-118">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="9bb84-118">Prerequisites</span></span>  
<span data-ttu-id="9bb84-119">För att kunna utföra den här genomgången behöver du:</span><span class="sxs-lookup"><span data-stu-id="9bb84-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="9bb84-120">installerad.</span><span class="sxs-lookup"><span data-stu-id="9bb84-120">installed.</span></span>  
- <span data-ttu-id="9bb84-121">Kassaflödeskalkylarksraderna är bokförda.</span><span class="sxs-lookup"><span data-stu-id="9bb84-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="9bb84-122">Roller</span><span class="sxs-lookup"><span data-stu-id="9bb84-122">Roles</span></span>  
<span data-ttu-id="9bb84-123">Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroll:</span><span class="sxs-lookup"><span data-stu-id="9bb84-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="9bb84-124">Controller</span><span class="sxs-lookup"><span data-stu-id="9bb84-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="9bb84-125">Situation</span><span class="sxs-lookup"><span data-stu-id="9bb84-125">Story</span></span>  
<span data-ttu-id="9bb84-126">Ken är controller på CRONUS som varje månad gör kassaflödesprognoser.</span><span class="sxs-lookup"><span data-stu-id="9bb84-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="9bb84-127">Han tar med ekonomi, försäljning, inköp och anläggningstillgångar i prognosen, och sedan visar han den till Sara som är ekonomichef.</span><span class="sxs-lookup"><span data-stu-id="9bb84-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="9bb84-128">Lägga upp ett nytt kontouppställningsnamn</span><span class="sxs-lookup"><span data-stu-id="9bb84-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="9bb84-129">En kontouppställning består av ett kontouppställningsnamn för kassaflöde med en serie rader och en kolumnlayout.</span><span class="sxs-lookup"><span data-stu-id="9bb84-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="9bb84-130">Så här skapar du ett nytt kontouppställningsnamn</span><span class="sxs-lookup"><span data-stu-id="9bb84-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="9bb84-131">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontouppställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9bb84-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9bb84-132">På sidan **Kontouppställningsnamn** väljer du åtgärden **Ny** för att skapa ett nytt kontouppställningsnamn för kassaflöde.</span><span class="sxs-lookup"><span data-stu-id="9bb84-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="9bb84-133">I fältet **Namn** anger du **Prognos**.</span><span class="sxs-lookup"><span data-stu-id="9bb84-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="9bb84-134">I fältet **Beskrivning**, ange **Kassaflödesprognos**.</span><span class="sxs-lookup"><span data-stu-id="9bb84-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="9bb84-135">Lämna fälten **Standard kolumnlayout** och **Analysvynamn** tomma.</span><span class="sxs-lookup"><span data-stu-id="9bb84-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="9bb84-136">Skapa kontouppställningsrader</span><span class="sxs-lookup"><span data-stu-id="9bb84-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="9bb84-137">När ett kontouppställningsnamn har upprättats, definierar Ken varje rad som visas i kontouppställningen för kassaflödet.</span><span class="sxs-lookup"><span data-stu-id="9bb84-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="9bb84-138">Ken definierar rader som kan visas i rapporter förutom rader som bara används vid beräkning.</span><span class="sxs-lookup"><span data-stu-id="9bb84-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="9bb84-139">Så här skapar du kontouppställningsrader</span><span class="sxs-lookup"><span data-stu-id="9bb84-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="9bb84-140">På sidan **Kontouppställningsnamn** väljer du det nya kontouppställningsnamnet för **Prognos** som du har skapat.</span><span class="sxs-lookup"><span data-stu-id="9bb84-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="9bb84-141">På fliken **Start** i gruppen **Process** väljer du **Redigera kontouppställning**.</span><span class="sxs-lookup"><span data-stu-id="9bb84-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="9bb84-142">På sidan **Kontouppställning** anger du varje rad exakt som det visas i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="9bb84-142">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="9bb84-143">Med hjälp av funktionen **Infoga kassaflödeskonton** kan du snabbt välja kassaflödeskonton från kontoplanen för kassaflöde och kopiera dem till kontouppställningsrader.</span><span class="sxs-lookup"><span data-stu-id="9bb84-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="9bb84-144">|Rad-nr|Beskrivning |Summeringstyp|Summering|Radtyp|Beloppstyp|Visa|</span><span class="sxs-lookup"><span data-stu-id="9bb84-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="9bb84-145">|-------|-----------|-------------|--------|--------|--- ------|----| | C10|Belopp|Nettoförändring|Transaktioner|Nettobelopp|Alltid|</span><span class="sxs-lookup"><span data-stu-id="9bb84-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="9bb84-146">|C20|Belopp till datum|Saldo till datum|Transaktioner|Nettobelopp|Alltid|</span><span class="sxs-lookup"><span data-stu-id="9bb84-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="9bb84-147">|C30|Hela räkenskapsåret|Hela räkenskapsåret|Transaktioner|Nettobelopp|Alltid|</span><span class="sxs-lookup"><span data-stu-id="9bb84-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="9bb84-148">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bb84-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="9bb84-149">Koppla kolumnlayouten till kontouppställningsnamnet</span><span class="sxs-lookup"><span data-stu-id="9bb84-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="9bb84-150">Nu kan Ken koppla kolumnlayouten till kontouppställningsnamnet.</span><span class="sxs-lookup"><span data-stu-id="9bb84-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="9bb84-151">Så här kopplar du kolumnlayouten till kontouppställningsnamnet</span><span class="sxs-lookup"><span data-stu-id="9bb84-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="9bb84-152">På sidan **Kontouppställningsnamnet** väljer du **Prognos** i fältet **Namn**.</span><span class="sxs-lookup"><span data-stu-id="9bb84-152">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="9bb84-153">I fältet **Standard kolumnlayout**, välj kolumnlayouten **Kassaflöde** som standardkolumnlayout.</span><span class="sxs-lookup"><span data-stu-id="9bb84-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="9bb84-154">Så här visar och skriver du ut kassaflödesprognosen</span><span class="sxs-lookup"><span data-stu-id="9bb84-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="9bb84-155">På sidan **Kontouppställningsnamn** väljer du åtgärden **Översikt** för att visa kassaflödesprognosen.</span><span class="sxs-lookup"><span data-stu-id="9bb84-155">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="9bb84-156">På sidan **Kontouppställning översikt** kan du ange ett belopp och sedan visa transaktionerna i kassaflödesprognosen som utgör beloppet.</span><span class="sxs-lookup"><span data-stu-id="9bb84-156">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="9bb84-157">Dessutom kan du visa formeln som används för att beräkna beloppet.</span><span class="sxs-lookup"><span data-stu-id="9bb84-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="9bb84-158">Du kan också filtrera beloppen efter datum och dimension.</span><span class="sxs-lookup"><span data-stu-id="9bb84-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="9bb84-159">Välj åtgärden **Skriv ut** när du vill skriva ut kassaflödesprognosen.</span><span class="sxs-lookup"><span data-stu-id="9bb84-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9bb84-160">Se även</span><span class="sxs-lookup"><span data-stu-id="9bb84-160">See Also</span></span>  
 <span data-ttu-id="9bb84-161">[Arbeta med kontouppställningar](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="9bb84-161">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="9bb84-162">Genomgång av affärsprocesser</span><span class="sxs-lookup"><span data-stu-id="9bb84-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="9bb84-163">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9bb84-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
