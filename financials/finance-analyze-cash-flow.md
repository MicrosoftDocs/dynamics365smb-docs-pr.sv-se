---
title: "Analysera kassaflöden | Microsoft Docs"
description: "Beskriver hur du använder kontantcykel, intäkter och kostnader, kassaflöde och kassaflödesprognosdiagrammet för att analysera tidigare flöden av likvida medel från och till ditt företag."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ebf31708fcd95b6d4746f1a3616b0eb104055514
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="analyzing-cash-flow-in-your-company"></a><span data-ttu-id="bed58-103">Analysera kassaflödet i företaget</span><span class="sxs-lookup"><span data-stu-id="bed58-103">Analyzing Cash Flow in Your Company</span></span>
<span data-ttu-id="bed58-104">Som de säger - kontanter är det som styr.</span><span class="sxs-lookup"><span data-stu-id="bed58-104">As they say, cash is king.</span></span> <span data-ttu-id="bed58-105">Diagrammen i rollcentret Revisor ger en inblick som hjälper dig att ta beslut om vad du ska göra med dina kontanter.</span><span class="sxs-lookup"><span data-stu-id="bed58-105">The charts on the Accountant Role Center provide insight that can help you make solid decisions about what to do with your cash.</span></span>  

| <span data-ttu-id="bed58-106">För att svara på frågor som de här</span><span class="sxs-lookup"><span data-stu-id="bed58-106">To answer questions like these</span></span> | <span data-ttu-id="bed58-107">Använd det här diagrammet</span><span class="sxs-lookup"><span data-stu-id="bed58-107">Use this chart</span></span> |
| --- | --- |
| <span data-ttu-id="bed58-108">Hur länge binder försäljningsprocessen upp mina kontanter?</span><span class="sxs-lookup"><span data-stu-id="bed58-108">How long does the sales process tie up my cash?</span></span></br> <span data-ttu-id="bed58-109">Bör jag öka eller minska lagernivåer?</span><span class="sxs-lookup"><span data-stu-id="bed58-109">Should I increase or reduce inventory levels?</span></span> |<span data-ttu-id="bed58-110">Kassacykel</span><span class="sxs-lookup"><span data-stu-id="bed58-110">Cash Cycle</span></span> |
| <span data-ttu-id="bed58-111">När kom kontanter in och ut till mitt företag?</span><span class="sxs-lookup"><span data-stu-id="bed58-111">When did cash move in and out of my company?</span></span></br> <span data-ttu-id="bed58-112">Är vissa perioder bättre än andra?</span><span class="sxs-lookup"><span data-stu-id="bed58-112">Are some periods better than others?</span></span> |<span data-ttu-id="bed58-113">Kassaflöde</span><span class="sxs-lookup"><span data-stu-id="bed58-113">Cash Flow</span></span> |
| <span data-ttu-id="bed58-114">Verkar siffrorna fel för en period?</span><span class="sxs-lookup"><span data-stu-id="bed58-114">Do the numbers seem off for a period?</span></span></br> <span data-ttu-id="bed58-115">Bör jag ta undersöka saken?</span><span class="sxs-lookup"><span data-stu-id="bed58-115">Should I investigate?</span></span> |<span data-ttu-id="bed58-116">Inkomst och utgift</span><span class="sxs-lookup"><span data-stu-id="bed58-116">Income & Expense</span></span> |
| <span data-ttu-id="bed58-117">När kan ett överskott eller underskott av kontanter ske?</span><span class="sxs-lookup"><span data-stu-id="bed58-117">When might a cash surplus or deficit happen?</span></span></br> <span data-ttu-id="bed58-118">Bör jag betala av skulder eller låna för att täcka kommande utgifter?</span><span class="sxs-lookup"><span data-stu-id="bed58-118">Should I pay down debt, or borrow to meet upcoming expenses?</span></span> |<span data-ttu-id="bed58-119">Kassaflödesprognoser</span><span class="sxs-lookup"><span data-stu-id="bed58-119">Cash Flow Forecasts</span></span> |

## <a name="dig-into-the-numbers"></a><span data-ttu-id="bed58-120">Gräv ner dig i siffrorna</span><span class="sxs-lookup"><span data-stu-id="bed58-120">Dig into the numbers</span></span>
<span data-ttu-id="bed58-121">I Rollcentret Revisor under **finansiell prestanda**, erbjuder diagrammen **kontantcykel**, **kassaflöde**, och **inkomster och utgifter** olika sätt att analysera kassaflöde:</span><span class="sxs-lookup"><span data-stu-id="bed58-121">On the Accountant Role Center, under **Finance Performance**, the **Cash Cycle**, **Cash Flow**, and **Income & Expense** charts offer ways to analyze cash flow:</span></span>  

* <span data-ttu-id="bed58-122">Visa siffrorna för en period med hjälp av skjutreglaget för tidslinje.</span><span class="sxs-lookup"><span data-stu-id="bed58-122">See figures for a period by using the timeline slider.</span></span>  
* <span data-ttu-id="bed58-123">Filtrera diagrammet genom att välja källan i förklaringen.</span><span class="sxs-lookup"><span data-stu-id="bed58-123">Filter the chart by choosing the source in the legend.</span></span>  
* <span data-ttu-id="bed58-124">Ändra längden på perioden, eller gå till föregående eller nästa period, genom att välja alternativ i listrutan **finansiell prestanda**.</span><span class="sxs-lookup"><span data-stu-id="bed58-124">Change the length of the period, or go to the previous or next period, by choosing options on the **Finance Performance** drop down.</span></span>  
* <span data-ttu-id="bed58-125">Visa transaktionerna genom att välja en punkt i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="bed58-125">View the entries by choosing a point in the chart.</span></span> <span data-ttu-id="bed58-126">Till exempel en punkt på tidslinjen eller ett kolumnsegment.</span><span class="sxs-lookup"><span data-stu-id="bed58-126">For example, a point on the timeline or a column segment.</span></span> <span data-ttu-id="bed58-127">Om siffrorna verkar fel kan du göra justeringar där.</span><span class="sxs-lookup"><span data-stu-id="bed58-127">If the numbers seem off, this is where you can make adjustments.</span></span>  

<span data-ttu-id="bed58-128">Även om den är olika liknar den diagrammet **kassaflödesprognos**.</span><span class="sxs-lookup"><span data-stu-id="bed58-128">Although it's separate, the **Cash Flow Forecast** chart is similar.</span></span> <span data-ttu-id="bed58-129">Du visar detaljer, filtrerar resultat och ändrar vad som visas på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="bed58-129">You view details, filter results, and change what's displayed in the same ways.</span></span> <span data-ttu-id="bed58-130">Om du ändrar en inställning kan du uppdatera prognosen genom att välja **kassaflödesprognos**, och sedan **Omberäkna prognos**.</span><span class="sxs-lookup"><span data-stu-id="bed58-130">If you change a setting, you can refresh the forecast by choosing **Cash Flow Forecast**, and then **Recalculate Forecast**.</span></span>

<span data-ttu-id="bed58-131">Om du vill undersöka prognosen, förutom prognostransaktioner, kan du också titta på kassaflödeskalkylbladet.</span><span class="sxs-lookup"><span data-stu-id="bed58-131">If you want to examine the forecast, in addition to forecast entries, you can also look at the cash flow worksheet.</span></span> <span data-ttu-id="bed58-132">Du kan t.ex se hur prognosen:</span><span class="sxs-lookup"><span data-stu-id="bed58-132">For example, you can see how the forecast:</span></span>

* <span data-ttu-id="bed58-133">Hanterar bekräftade försäljningar och inköp.</span><span class="sxs-lookup"><span data-stu-id="bed58-133">Handles confirmed sales and purchases.</span></span>  
* <span data-ttu-id="bed58-134">Subtraherar leverantörsreskontra och lägger till kundreskontra.</span><span class="sxs-lookup"><span data-stu-id="bed58-134">Subtracts payables and adds receivables.</span></span>  
* <span data-ttu-id="bed58-135">Hoppar över dubbla försäljningsorder och inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="bed58-135">Skips duplicate sales orders and purchase orders.</span></span>  

### <a name="to-view-a-cash-flow-worksheet"></a><span data-ttu-id="bed58-136">Att visa ett kassaflödeskalkylblad</span><span class="sxs-lookup"><span data-stu-id="bed58-136">To view a cash flow worksheet</span></span>
1. <span data-ttu-id="bed58-137">Sök efter **Kassaflödesprognoser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bed58-137">Search for **Cash Flow Forecasts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bed58-138">Välj en kassaflödesprognos och välj sedan åtgärden **kassaflödeskalkylblad**.</span><span class="sxs-lookup"><span data-stu-id="bed58-138">Choose a cash flow forecast, and then choose the **Cash Flow Worksheet** action.</span></span>  
3. <span data-ttu-id="bed58-139">På sidan **kassaflödekalkylblad** väljer du åtgärden **Föreslå förslagsrader**.</span><span class="sxs-lookup"><span data-stu-id="bed58-139">On the **Cash Flow Worksheet** page, choose the **Suggest Worksheet Lines** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bed58-140">Se även</span><span class="sxs-lookup"><span data-stu-id="bed58-140">See Also</span></span>
[<span data-ttu-id="bed58-141">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="bed58-141">Setting Up Finance</span></span>](finance-setup-finance.md)  
<span data-ttu-id="bed58-142">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bed58-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="bed58-143">Ställa in analysvy för kassaflöde</span><span class="sxs-lookup"><span data-stu-id="bed58-143">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  

