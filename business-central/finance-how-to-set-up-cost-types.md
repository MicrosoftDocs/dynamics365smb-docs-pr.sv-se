---
title: Så här skapar du en Lista över kostnadstyper | Microsoft Docs
description: Planen över kostnadstyper liknar kontoplanen i redovisningen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 2846967648f5c0e0b6015c7990a941642fc27323
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "808121"
---
# <a name="set-up-cost-types"></a><span data-ttu-id="1a9cb-103">Skapa kostnadstyper</span><span class="sxs-lookup"><span data-stu-id="1a9cb-103">Set Up Cost Types</span></span>
<span data-ttu-id="1a9cb-104">Listan över kostnadstyper liknar kontoplanen i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-104">The chart of cost types is similar to the chart of accounts in the general ledger.</span></span> <span data-ttu-id="1a9cb-105">Du kan definiera planen för kostnadstyper på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="1a9cb-105">You can set up the chart of cost types in the following ways:</span></span>  

-   <span data-ttu-id="1a9cb-106">Strukturera planen över kostnadstyper på samma sätt som resultaträkningens konton i kontoplanen i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-106">Structure the chart of cost types similar to the income statement accounts in the general ledger chart of accounts.</span></span> <span data-ttu-id="1a9cb-107">Sedan kan du överföra kontoplanen i redovisningen till planen över kostnadstyper.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-107">Then, you can transfer the general ledger chart of accounts to the chart of cost types.</span></span> <span data-ttu-id="1a9cb-108">Du kan göra nödvändiga justeringar efter överföringen.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-108">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="1a9cb-109">Skapa ny plan över kostnadstyper eller lägg till nya kostnadstyper till befintlig plan över kostnadstyper.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-109">Create new chart of cost types or add new cost types to existing chart of cost types.</span></span> <span data-ttu-id="1a9cb-110">Du måste skapa varje ny kostnadstyp för sig.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-110">You must create each new cost type individually.</span></span>  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a><span data-ttu-id="1a9cb-111">Överföra kontoplanen i redovisningen till redovisningsplanen över kostnadstyper</span><span class="sxs-lookup"><span data-stu-id="1a9cb-111">To transfer the general ledger chart of accounts to the chart of cost types</span></span>  
1.  <span data-ttu-id="1a9cb-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lista över kostnadstyper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1a9cb-113">Välj åtgärden **Hämta kostnadstyper från kontoplan** action.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-113">Choose the **Get Cost Types from Chart of Accounts** action.</span></span> <span data-ttu-id="1a9cb-114">Välj **ja** i dialogrutan för att bekräfta överföringen.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-114">In the dialog box, choose the **Yes** button to confirm the transfer.</span></span> <span data-ttu-id="1a9cb-115">Funktionen använder kontoplanen i redovisningen för att skapa en plan över kostnadstyper.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-115">The function uses the chart of accounts to create a chart of cost types.</span></span>  

    <span data-ttu-id="1a9cb-116">Planen över kostnadstyper innehåller nu alla resultaträkningskonton i redovisningen inklusive rubriker och delsummor.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-116">The chart of cost types now contain all income statement accounts in the general ledger and include headings and subtotals.</span></span> <span data-ttu-id="1a9cb-117">Du kan ändra planen över kostnadstyper efter behov.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-117">You can change the chart of cost types, as necessary.</span></span> <span data-ttu-id="1a9cb-118">Du kan till exempel ta bort dubbletter av befintliga kostnadstyper.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-118">For example, you can delete duplicate existing cost types.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="1a9cb-119">Funktionen **Registrera kostnadstyper i kontoplan** uppdaterar relationen mellan kontoplanen och planen över kostnadstyper.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-119">The **Register Cost Types in Chart of Accounts** function updates the relationship between the chart of accounts and the chart of cost types.</span></span> <span data-ttu-id="1a9cb-120">Fältet **nr.**</span><span class="sxs-lookup"><span data-stu-id="1a9cb-120">The **No.**</span></span> <span data-ttu-id="1a9cb-121">-fältet fylls och verifieras för att se till att varje redovisningskonto är kopplade till endast ett kostnadstyp.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-121">field is filled and verified to make sure that each general ledger account is related to only one cost type.</span></span> <span data-ttu-id="1a9cb-122">Kör funktionen automatiskt, före överföring av redovisningstransaktioner mot kostnadsredovisning.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-122">The function runs automatically before transferring general ledger entries to cost accounting.</span></span>  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a><span data-ttu-id="1a9cb-123">Så här skapar du nya kostnadstyper på sidan Lista över kostnadsbärare.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-123">To set up new cost types in the Chart of Cost Types page</span></span>  
1.  <span data-ttu-id="1a9cb-124">Öppna sidan **Lista över kostnadstyper** i redigeringsläge.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-124">Open the **Chart of Cost Types** page in edit mode.</span></span>  
2.  <span data-ttu-id="1a9cb-125">Fyll i fälten som beskrivs efter behov.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-125">Fill in the fields as described as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  <span data-ttu-id="1a9cb-126">Du kan lägga upp och underhålla kostnadstupen antingen i kortet **Kort för Kostnadstyper** eller på sidan **Lista över Kostnadstyper**.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-126">You can set up and maintain cost types in either the **Cost Type Card** page or on the **Chart of Cost Types** page.</span></span> <span data-ttu-id="1a9cb-127">I den här proceduren skapar du Kostnadstyper på sidan **Lista över kostnadstyper**.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-127">In this procedure, you set up cost types on the **Chart of Cost Types** page.</span></span>

3.  <span data-ttu-id="1a9cb-128">När du har skapat alla kostnadstyper väljer du åtgärden **Indrag för kostnadstyper**.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-128">After you have created all cost types, choose the **Indent Cost Types** action.</span></span> <span data-ttu-id="1a9cb-129">Välj **ja** i dialogrutan.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-129">In the dialog box, choose the **Yes** button.</span></span>  
4.  <span data-ttu-id="1a9cb-130">Koppla den nya kostnadstypen till motsvarande redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-130">Link the new cost type to the corresponding general ledger account.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="1a9cb-131">Om du har angett definitioner i fältet **Summering** för rader av typen **Till-summa** innan du kör funktionen **Indrag för kostnadstyper** måste du ange definitionerna igen eftersom funktionen ersätter alla värden i alla **Till-summa**-fält.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-131">If you have entered definitions in the **Totaling** fields for the line type of **End-Total** before you run the **Indent Cost Types** function, then you must enter the definitions again because the function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="to-update-cost-types"></a><span data-ttu-id="1a9cb-132">Uppdatera kostnadstyper</span><span class="sxs-lookup"><span data-stu-id="1a9cb-132">To update cost types</span></span>  
1.  <span data-ttu-id="1a9cb-133">Markera om du vill att planen över kostnadstyper automatiskt ska uppdateras när kontoplanen ändras på sidan **Inställningar för kostnadsredovisning**.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-133">On the **Cost Accounting Setup** page, select if you want the chart of cost types to be automatically updated when the chart of accounts is changed.</span></span>  
2.  <span data-ttu-id="1a9cb-134">I fältet **Justera redovisningskonto** kan du välja något av följande alternativ.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-134">In the **Align G/L Account** field, you can choose from the following options.</span></span>  

- <span data-ttu-id="1a9cb-135">**Ingen justering** - Ingen motsvarande ändring görs i planen över kostnadstyper när du ändrar kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-135">**No Alignment** - There is no corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="1a9cb-136">**Automatisk** - Det görs en motsvarande ändring i planen över kostnadstyper när du ändrar kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-136">**Automatic** - A corresponding change is made in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="1a9cb-137">**Prompt** - Ett meddelande visas och frågar om du vill göra en motsvarande ändring i planen över kostnadstyper när du ändrar kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-137">**Prompt** - A message is displayed asking if you want to make a corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1a9cb-138">Se även</span><span class="sxs-lookup"><span data-stu-id="1a9cb-138">See Also</span></span>  
[<span data-ttu-id="1a9cb-139">Redovisa kostnader</span><span class="sxs-lookup"><span data-stu-id="1a9cb-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="1a9cb-140">[Definiera kostnadsställen och kostnadsbärare för kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="1a9cb-140">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="1a9cb-141">[Saldon mellan kostnadstyp, kostnadsställe och kostnadsbärare](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="1a9cb-141">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="1a9cb-142">[Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="1a9cb-142">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="1a9cb-143">[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="1a9cb-143">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="1a9cb-144">Om kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="1a9cb-144">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="1a9cb-145">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1a9cb-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
