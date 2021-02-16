---
title: Analysera kassaflöden | Microsoft Docs
description: Beskriver hur du använder kontantcykel, intäkter och kostnader, kassaflöde och kassaflödesprognosdiagrammet för att analysera tidigare flöden av likvida medel från och till ditt företag.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f3f7e9c33e5dab3de6461fcda5732168f0e6e89b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751036"
---
# <a name="analyzing-cash-flow-in-your-company"></a><span data-ttu-id="1a3c8-103">Analysera kassaflödet i företaget</span><span class="sxs-lookup"><span data-stu-id="1a3c8-103">Analyzing Cash Flow in Your Company</span></span>
<span data-ttu-id="1a3c8-104">Diagrammen i rollcentret Revisor ger en inblick som hjälper dig att ta beslut om vad du ska göra med dina kontanter.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-104">The charts on the Accountant Role Center provide insights that can help you make solid decisions about what to do with your cash.</span></span>  

| <span data-ttu-id="1a3c8-105">För att svara på frågor som de här</span><span class="sxs-lookup"><span data-stu-id="1a3c8-105">To answer questions like these</span></span> | <span data-ttu-id="1a3c8-106">Använd det här diagrammet</span><span class="sxs-lookup"><span data-stu-id="1a3c8-106">Use this chart</span></span> |
| --- | --- |
| <span data-ttu-id="1a3c8-107">Hur länge binder försäljningsprocessen upp mina kontanter?</span><span class="sxs-lookup"><span data-stu-id="1a3c8-107">How long does the sales process tie up my cash?</span></span></br> <span data-ttu-id="1a3c8-108">Bör jag öka eller minska lagernivåer?</span><span class="sxs-lookup"><span data-stu-id="1a3c8-108">Should I increase or reduce inventory levels?</span></span> |<span data-ttu-id="1a3c8-109">Kassacykel</span><span class="sxs-lookup"><span data-stu-id="1a3c8-109">Cash Cycle</span></span> |
| <span data-ttu-id="1a3c8-110">När kom kontanter in och ut till mitt företag?</span><span class="sxs-lookup"><span data-stu-id="1a3c8-110">When did cash move in and out of my company?</span></span></br> <span data-ttu-id="1a3c8-111">Är vissa perioder bättre än andra?</span><span class="sxs-lookup"><span data-stu-id="1a3c8-111">Are some periods better than others?</span></span> |<span data-ttu-id="1a3c8-112">Kassaflöde</span><span class="sxs-lookup"><span data-stu-id="1a3c8-112">Cash Flow</span></span> |
| <span data-ttu-id="1a3c8-113">Verkar siffrorna fel för en period?</span><span class="sxs-lookup"><span data-stu-id="1a3c8-113">Do the numbers seem off for a period?</span></span></br> <span data-ttu-id="1a3c8-114">Bör jag ta undersöka saken?</span><span class="sxs-lookup"><span data-stu-id="1a3c8-114">Should I investigate?</span></span> |<span data-ttu-id="1a3c8-115">Inkomst och utgift</span><span class="sxs-lookup"><span data-stu-id="1a3c8-115">Income & Expense</span></span> |
| <span data-ttu-id="1a3c8-116">När kan ett överskott eller underskott av kontanter ske?</span><span class="sxs-lookup"><span data-stu-id="1a3c8-116">When might a cash surplus or deficit happen?</span></span></br> <span data-ttu-id="1a3c8-117">Bör jag betala av skulder eller låna för att täcka kommande utgifter?</span><span class="sxs-lookup"><span data-stu-id="1a3c8-117">Should I pay down debt, or borrow to meet upcoming expenses?</span></span> |<span data-ttu-id="1a3c8-118">Kassaflödesprognoser</span><span class="sxs-lookup"><span data-stu-id="1a3c8-118">Cash Flow Forecasts</span></span> |

<span data-ttu-id="1a3c8-119">I Rollcentret Revisor under **finansiell prestanda**, erbjuder diagrammen **kontantcykel**, **kassaflöde**, och **inkomster och utgifter** olika sätt att analysera kassaflöde:</span><span class="sxs-lookup"><span data-stu-id="1a3c8-119">On the Accountant Role Center, under **Finance Performance**, the **Cash Cycle**, **Cash Flow**, and **Income & Expense** charts offer ways to analyze cash flow:</span></span>  

* <span data-ttu-id="1a3c8-120">Visa siffrorna för en period med hjälp av skjutreglaget för tidslinje.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-120">See figures for a period by using the timeline slider.</span></span>  
* <span data-ttu-id="1a3c8-121">Filtrera diagrammet genom att välja källan i förklaringen.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-121">Filter the chart by choosing the source in the legend.</span></span>  
* <span data-ttu-id="1a3c8-122">Ändra längden på perioden, eller gå till föregående eller nästa period, genom att välja alternativ i listrutan **finansiell prestanda**.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-122">Change the length of the period, or go to the previous or next period, by choosing options on the **Finance Performance** drop down.</span></span>  
* <span data-ttu-id="1a3c8-123">Visa transaktionerna genom att välja en punkt i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-123">View the entries by choosing a point in the chart.</span></span> <span data-ttu-id="1a3c8-124">Till exempel en punkt på tidslinjen eller ett kolumnsegment.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-124">For example, a point on the timeline or a column segment.</span></span> <span data-ttu-id="1a3c8-125">Om siffrorna verkar fel kan du göra justeringar där.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-125">If the numbers seem off, this is where you can make adjustments.</span></span>  

<span data-ttu-id="1a3c8-126">Även om den är olika liknar den diagrammet **kassaflödesprognos**.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-126">Although it's separate, the **Cash Flow Forecast** chart is similar.</span></span> <span data-ttu-id="1a3c8-127">Du visar detaljer, filtrerar resultat och ändrar vad som visas på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-127">You view details, filter results, and change what is displayed in the same ways.</span></span> <span data-ttu-id="1a3c8-128">Om du ändrar en inställning kan du uppdatera prognosen genom att välja **kassaflödesprognos**, och sedan **Omberäkna prognos**.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-128">If you change a setting, you can refresh the forecast by choosing **Cash Flow Forecast**, and then **Recalculate Forecast**.</span></span>

<span data-ttu-id="1a3c8-129">Om du vill undersöka prognosen, förutom prognostransaktioner, kan du också titta på kassaflödeskalkylbladet.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-129">If you want to examine the forecast, in addition to forecast entries, you can also look at the cash flow worksheet.</span></span> <span data-ttu-id="1a3c8-130">Du kan t.ex se hur prognosen:</span><span class="sxs-lookup"><span data-stu-id="1a3c8-130">For example, you can see how the forecast:</span></span>

* <span data-ttu-id="1a3c8-131">Hanterar bekräftade försäljningar och inköp.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-131">Handles confirmed sales and purchases.</span></span>  
* <span data-ttu-id="1a3c8-132">Subtraherar leverantörsreskontra och lägger till kundreskontra.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-132">Subtracts payables and adds receivables.</span></span>  
* <span data-ttu-id="1a3c8-133">Hoppar över dubbla försäljningsorder och inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-133">Skips duplicate sales orders and purchase orders.</span></span>  

## <a name="to-view-a-cash-flow-worksheet"></a><span data-ttu-id="1a3c8-134">Att visa ett kassaflödeskalkylblad</span><span class="sxs-lookup"><span data-stu-id="1a3c8-134">To view a cash flow worksheet</span></span>
1. <span data-ttu-id="1a3c8-135">Sök efter **Kassaflödesprognoser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-135">Search for **Cash Flow Forecasts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1a3c8-136">Välj en kassaflödesprognos och välj sedan åtgärden **kassaflödeskalkylblad**.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-136">Choose a cash flow forecast, and then choose the **Cash Flow Worksheet** action.</span></span>  
3. <span data-ttu-id="1a3c8-137">På sidan **kassaflödekalkylblad** väljer du åtgärden **Föreslå kalkylarksrader**.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-137">On the **Cash Flow Worksheet** page, choose the **Suggest Worksheet Lines** action.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="1a3c8-138">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="1a3c8-138">See Related Training at [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="1a3c8-139">Se även</span><span class="sxs-lookup"><span data-stu-id="1a3c8-139">See Also</span></span>
[<span data-ttu-id="1a3c8-140">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="1a3c8-140">Setting Up Finance</span></span>](finance-setup-finance.md)  
<span data-ttu-id="1a3c8-141">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1a3c8-141">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="1a3c8-142">Ställa in analys för kassaflöde</span><span class="sxs-lookup"><span data-stu-id="1a3c8-142">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  
