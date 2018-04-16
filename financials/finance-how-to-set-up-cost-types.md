---
title: "Så här skapar du en Lista över kostnadstyper | Microsoft Docs"
description: "Planen över kostnadstyper liknar kontoplanen i redovisningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: c89170fd159428d771df105ca16a1d91d29651e4
ms.contentlocale: sv-se
ms.lasthandoff: 04/16/2018

---
# <a name="set-up-cost-types"></a><span data-ttu-id="477ed-103">Skapa kostnadstyper</span><span class="sxs-lookup"><span data-stu-id="477ed-103">Set Up Cost Types</span></span>
<span data-ttu-id="477ed-104">Listan över kostnadstyper liknar kontoplanen i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="477ed-104">The chart of cost types is similar to the chart of accounts in the general ledger.</span></span> <span data-ttu-id="477ed-105">Du kan definiera planen för kostnadstyper på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="477ed-105">You can set up the chart of cost types in the following ways:</span></span>  

-   <span data-ttu-id="477ed-106">Strukturera planen över kostnadstyper på samma sätt som resultaträkningens konton i kontoplanen i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="477ed-106">Structure the chart of cost types similar to the income statement accounts in the general ledger chart of accounts.</span></span> <span data-ttu-id="477ed-107">Sedan kan du överföra kontoplanen i redovisningen till planen över kostnadstyper.</span><span class="sxs-lookup"><span data-stu-id="477ed-107">Then, you can transfer the general ledger chart of accounts to the chart of cost types.</span></span> <span data-ttu-id="477ed-108">Du kan göra nödvändiga justeringar efter överföringen.</span><span class="sxs-lookup"><span data-stu-id="477ed-108">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="477ed-109">Skapa ny plan över kostnadstyper eller lägg till nya kostnadstyper till befintlig plan över kostnadstyper.</span><span class="sxs-lookup"><span data-stu-id="477ed-109">Create new chart of cost types or add new cost types to existing chart of cost types.</span></span> <span data-ttu-id="477ed-110">Du måste skapa varje ny kostnadstyp för sig.</span><span class="sxs-lookup"><span data-stu-id="477ed-110">You must create each new cost type individually.</span></span>  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a><span data-ttu-id="477ed-111">Överföra kontoplanen i redovisningen till redovisningsplanen över kostnadstyper</span><span class="sxs-lookup"><span data-stu-id="477ed-111">To transfer the general ledger chart of accounts to the chart of cost types</span></span>  
1.  <span data-ttu-id="477ed-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lista över kostnadstyper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="477ed-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="477ed-113">Välj åtgärden **Hämta kostnadstyper från kontoplan** action.</span><span class="sxs-lookup"><span data-stu-id="477ed-113">Choose the **Get Cost Types from Chart of Accounts** action.</span></span> <span data-ttu-id="477ed-114">Välj **ja** i dialogrutan för att bekräfta överföringen.</span><span class="sxs-lookup"><span data-stu-id="477ed-114">In the dialog box, choose the **Yes** button to confirm the transfer.</span></span> <span data-ttu-id="477ed-115">Funktionen använder kontoplanen i redovisningen för att skapa en plan över kostnadstyper.</span><span class="sxs-lookup"><span data-stu-id="477ed-115">The function uses the chart of accounts to create a chart of cost types.</span></span>  

    <span data-ttu-id="477ed-116">Planen över kostnadstyper innehåller nu alla resultaträkningskonton i redovisningen inklusive rubriker och delsummor.</span><span class="sxs-lookup"><span data-stu-id="477ed-116">The chart of cost types now contain all income statement accounts in the general ledger and include headings and subtotals.</span></span> <span data-ttu-id="477ed-117">Du kan ändra planen över kostnadstyper efter behov.</span><span class="sxs-lookup"><span data-stu-id="477ed-117">You can change the chart of cost types, as necessary.</span></span> <span data-ttu-id="477ed-118">Du kan till exempel ta bort dubbletter av befintliga kostnadstyper.</span><span class="sxs-lookup"><span data-stu-id="477ed-118">For example, you can delete duplicate existing cost types.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="477ed-119">Funktionen **Registrera kostnadstyper i kontoplan** uppdaterar relationen mellan kontoplanen och planen över kostnadstyper.</span><span class="sxs-lookup"><span data-stu-id="477ed-119">The **Register Cost Types in Chart of Accounts** function updates the relationship between the chart of accounts and the chart of cost types.</span></span> <span data-ttu-id="477ed-120">Fältet **nr.**</span><span class="sxs-lookup"><span data-stu-id="477ed-120">The **No.**</span></span> <span data-ttu-id="477ed-121">-fältet fylls och verifieras för att se till att varje redovisningskonto är kopplade till endast ett kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="477ed-121">field is filled and verified to make sure that each general ledger account is related to only one cost type.</span></span> <span data-ttu-id="477ed-122">Kör funktionen automatiskt, före överföring av redovisningstransaktioner mot kostnadsredovisning.</span><span class="sxs-lookup"><span data-stu-id="477ed-122">The function runs automatically before transferring general ledger entries to cost accounting.</span></span>  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-window"></a><span data-ttu-id="477ed-123">Så här skapar du nya kostnadstyper i fönstret Lista över kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="477ed-123">To set up new cost types in the Chart of Cost Types window</span></span>  
1. <span data-ttu-id="477ed-124">Öppna fönstret **Lista över kostnadstyper** i redigeringsläge.</span><span class="sxs-lookup"><span data-stu-id="477ed-124">Open the **Chart of Cost Types** window in edit mode.</span></span>  
2. <span data-ttu-id="477ed-125">Fyll i fälten som beskrivs efter behov.</span><span class="sxs-lookup"><span data-stu-id="477ed-125">Fill in the fields as described as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]  
   >  <span data-ttu-id="477ed-126">eDu kan lägga upp och underhålla kostnadstupen antingen i kortet **Kort för Kostnadstyper** eller i fönstret **Lista över Kostnadstyper**.</span><span class="sxs-lookup"><span data-stu-id="477ed-126">You can set up and maintain cost types in either the **Cost Type Card** window or in the **Chart of Cost Types** window.</span></span> <span data-ttu-id="477ed-127">I den här proceduren skapar du Kostnadstyper i fönstret **Lista över kostnadstyper**.</span><span class="sxs-lookup"><span data-stu-id="477ed-127">In this procedure, you set up cost types in the **Chart of Cost Types** window.</span></span>

3. <span data-ttu-id="477ed-128">När du har skapat alla kostnadstyper väljer du åtgärden **Indrag för kostnadstyper**.</span><span class="sxs-lookup"><span data-stu-id="477ed-128">After you have created all cost types, choose the **Indent Cost Types** action.</span></span> <span data-ttu-id="477ed-129">Välj **ja** i dialogrutan.</span><span class="sxs-lookup"><span data-stu-id="477ed-129">In the dialog box, choose the **Yes** button.</span></span>  
4. <span data-ttu-id="477ed-130">Koppla den nya kostnadstypen till motsvarande redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="477ed-130">Link the new cost type to the corresponding general ledger account.</span></span>  

   > [!IMPORTANT]  
   >  <span data-ttu-id="477ed-131">Om du har angett definitioner i fältet **Summering** för rader av typen **Till-summa** innan du kör funktionen **Indrag för kostnadstyper** måste du ange definitionerna igen eftersom funktionen ersätter alla värden i alla **Till-summa**-fält.</span><span class="sxs-lookup"><span data-stu-id="477ed-131">If you have entered definitions in the **Totaling** fields for the line type of **End-Total** before you run the **Indent Cost Types** function, then you must enter the definitions again because the function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="to-update-cost-types"></a><span data-ttu-id="477ed-132">Uppdatera kostnadstyper</span><span class="sxs-lookup"><span data-stu-id="477ed-132">To update cost types</span></span>  
1.  <span data-ttu-id="477ed-133">Markera om du vill att planen över kostnadstyper automatiskt ska uppdateras när kontoplanen ändras i fönstret **Inställningar för kostnadsredovisning**.</span><span class="sxs-lookup"><span data-stu-id="477ed-133">In the **Cost Accounting Setup** window, select if you want the chart of cost types to be automatically updated when the chart of accounts is changed.</span></span>  
2.  <span data-ttu-id="477ed-134">I fältet **Justera redovisningskonto** kan du välja något av följande alternativ.</span><span class="sxs-lookup"><span data-stu-id="477ed-134">In the **Align G/L Account** field, you can choose from the following options.</span></span>  

- <span data-ttu-id="477ed-135">**Ingen justering** - Ingen motsvarande ändring görs i planen över kostnadstyper när du ändrar kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="477ed-135">**No Alignment** - There is no corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="477ed-136">**Automatisk** - Det görs en motsvarande ändring i planen över kostnadstyper när du ändrar kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="477ed-136">**Automatic** - A corresponding change is made in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="477ed-137">**Prompt** - Ett meddelande visas och frågar om du vill göra en motsvarande ändring i planen över kostnadstyper när du ändrar kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="477ed-137">**Prompt** - A message is displayed asking if you want to make a corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="477ed-138">Se även</span><span class="sxs-lookup"><span data-stu-id="477ed-138">See Also</span></span>  
[<span data-ttu-id="477ed-139">Redovisa kostnader</span><span class="sxs-lookup"><span data-stu-id="477ed-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="477ed-140">[Definiera relationen mellan kostnadstyper och redovisningskonton](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="477ed-140">[Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md) </span></span>  
<span data-ttu-id="477ed-141">[Definiera kostnadsställen och kostnadsbärare för kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="477ed-141">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="477ed-142">[Saldon mellan kostnadstyp, kostnadsställe och kostnadsbärare](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="477ed-142">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="477ed-143">[Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="477ed-143">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="477ed-144">[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="477ed-144">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="477ed-145">Om kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="477ed-145">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="477ed-146">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="477ed-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

