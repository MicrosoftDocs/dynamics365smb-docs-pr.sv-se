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
ms.date: 01/13/2020
ms.author: bholtorf
ms.openlocfilehash: 3e66c2d6beb24c82fcd314caeac00f3c7b20412a
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953161"
---
# <a name="analyzing-cash-flow-in-your-company"></a><span data-ttu-id="1d0c4-103">Analysera kassaflödet i företaget</span><span class="sxs-lookup"><span data-stu-id="1d0c4-103">Analyzing Cash Flow in Your Company</span></span>
<span data-ttu-id="1d0c4-104">Som de säger - kontanter är det som styr.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-104">As they say, cash is king.</span></span> <span data-ttu-id="1d0c4-105">Diagrammen i rollcentret Revisor ger en inblick som hjälper dig att ta beslut om vad du ska göra med dina kontanter.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-105">The charts on the Accountant Role Center provide insight that can help you make solid decisions about what to do with your cash.</span></span>  

| <span data-ttu-id="1d0c4-106">För att svara på frågor som de här</span><span class="sxs-lookup"><span data-stu-id="1d0c4-106">To answer questions like these</span></span> | <span data-ttu-id="1d0c4-107">Använd det här diagrammet</span><span class="sxs-lookup"><span data-stu-id="1d0c4-107">Use this chart</span></span> |
| --- | --- |
| <span data-ttu-id="1d0c4-108">Hur länge binder försäljningsprocessen upp mina kontanter?</span><span class="sxs-lookup"><span data-stu-id="1d0c4-108">How long does the sales process tie up my cash?</span></span></br> <span data-ttu-id="1d0c4-109">Bör jag öka eller minska lagernivåer?</span><span class="sxs-lookup"><span data-stu-id="1d0c4-109">Should I increase or reduce inventory levels?</span></span> |<span data-ttu-id="1d0c4-110">Kassacykel</span><span class="sxs-lookup"><span data-stu-id="1d0c4-110">Cash Cycle</span></span> |
| <span data-ttu-id="1d0c4-111">När kom kontanter in och ut till mitt företag?</span><span class="sxs-lookup"><span data-stu-id="1d0c4-111">When did cash move in and out of my company?</span></span></br> <span data-ttu-id="1d0c4-112">Är vissa perioder bättre än andra?</span><span class="sxs-lookup"><span data-stu-id="1d0c4-112">Are some periods better than others?</span></span> |<span data-ttu-id="1d0c4-113">Kassaflöde</span><span class="sxs-lookup"><span data-stu-id="1d0c4-113">Cash Flow</span></span> |
| <span data-ttu-id="1d0c4-114">Verkar siffrorna fel för en period?</span><span class="sxs-lookup"><span data-stu-id="1d0c4-114">Do the numbers seem off for a period?</span></span></br> <span data-ttu-id="1d0c4-115">Bör jag ta undersöka saken?</span><span class="sxs-lookup"><span data-stu-id="1d0c4-115">Should I investigate?</span></span> |<span data-ttu-id="1d0c4-116">Inkomst och utgift</span><span class="sxs-lookup"><span data-stu-id="1d0c4-116">Income & Expense</span></span> |
| <span data-ttu-id="1d0c4-117">När kan ett överskott eller underskott av kontanter ske?</span><span class="sxs-lookup"><span data-stu-id="1d0c4-117">When might a cash surplus or deficit happen?</span></span></br> <span data-ttu-id="1d0c4-118">Bör jag betala av skulder eller låna för att täcka kommande utgifter?</span><span class="sxs-lookup"><span data-stu-id="1d0c4-118">Should I pay down debt, or borrow to meet upcoming expenses?</span></span> |<span data-ttu-id="1d0c4-119">Kassaflödesprognoser</span><span class="sxs-lookup"><span data-stu-id="1d0c4-119">Cash Flow Forecasts</span></span> |

<span data-ttu-id="1d0c4-120">I Rollcentret Revisor under **finansiell prestanda**, erbjuder diagrammen **kontantcykel**, **kassaflöde**, och **inkomster och utgifter** olika sätt att analysera kassaflöde:</span><span class="sxs-lookup"><span data-stu-id="1d0c4-120">On the Accountant Role Center, under **Finance Performance**, the **Cash Cycle**, **Cash Flow**, and **Income & Expense** charts offer ways to analyze cash flow:</span></span>  

* <span data-ttu-id="1d0c4-121">Visa siffrorna för en period med hjälp av skjutreglaget för tidslinje.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-121">See figures for a period by using the timeline slider.</span></span>  
* <span data-ttu-id="1d0c4-122">Filtrera diagrammet genom att välja källan i förklaringen.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-122">Filter the chart by choosing the source in the legend.</span></span>  
* <span data-ttu-id="1d0c4-123">Ändra längden på perioden, eller gå till föregående eller nästa period, genom att välja alternativ i listrutan **finansiell prestanda**.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-123">Change the length of the period, or go to the previous or next period, by choosing options on the **Finance Performance** drop down.</span></span>  
* <span data-ttu-id="1d0c4-124">Visa transaktionerna genom att välja en punkt i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-124">View the entries by choosing a point in the chart.</span></span> <span data-ttu-id="1d0c4-125">Till exempel en punkt på tidslinjen eller ett kolumnsegment.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-125">For example, a point on the timeline or a column segment.</span></span> <span data-ttu-id="1d0c4-126">Om siffrorna verkar fel kan du göra justeringar där.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-126">If the numbers seem off, this is where you can make adjustments.</span></span>  

<span data-ttu-id="1d0c4-127">Även om den är olika liknar den diagrammet **kassaflödesprognos**.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-127">Although it's separate, the **Cash Flow Forecast** chart is similar.</span></span> <span data-ttu-id="1d0c4-128">Du visar detaljer, filtrerar resultat och ändrar vad som visas på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-128">You view details, filter results, and change what is displayed in the same ways.</span></span> <span data-ttu-id="1d0c4-129">Om du ändrar en inställning kan du uppdatera prognosen genom att välja **kassaflödesprognos**, och sedan **Omberäkna prognos**.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-129">If you change a setting, you can refresh the forecast by choosing **Cash Flow Forecast**, and then **Recalculate Forecast**.</span></span>

<span data-ttu-id="1d0c4-130">Om du vill undersöka prognosen, förutom prognostransaktioner, kan du också titta på kassaflödeskalkylbladet.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-130">If you want to examine the forecast, in addition to forecast entries, you can also look at the cash flow worksheet.</span></span> <span data-ttu-id="1d0c4-131">Du kan t.ex se hur prognosen:</span><span class="sxs-lookup"><span data-stu-id="1d0c4-131">For example, you can see how the forecast:</span></span>

* <span data-ttu-id="1d0c4-132">Hanterar bekräftade försäljningar och inköp.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-132">Handles confirmed sales and purchases.</span></span>  
* <span data-ttu-id="1d0c4-133">Subtraherar leverantörsreskontra och lägger till kundreskontra.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-133">Subtracts payables and adds receivables.</span></span>  
* <span data-ttu-id="1d0c4-134">Hoppar över dubbla försäljningsorder och inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-134">Skips duplicate sales orders and purchase orders.</span></span>  

## <a name="to-view-a-cash-flow-worksheet"></a><span data-ttu-id="1d0c4-135">Att visa ett kassaflödeskalkylblad</span><span class="sxs-lookup"><span data-stu-id="1d0c4-135">To view a cash flow worksheet</span></span>
1. <span data-ttu-id="1d0c4-136">Sök efter **Kassaflödesprognoser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-136">Search for **Cash Flow Forecasts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1d0c4-137">Välj en kassaflödesprognos och välj sedan åtgärden **kassaflödeskalkylblad**.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-137">Choose a cash flow forecast, and then choose the **Cash Flow Worksheet** action.</span></span>  
3. <span data-ttu-id="1d0c4-138">På sidan **kassaflödekalkylblad** väljer du åtgärden **Föreslå kalkylarksrader**.</span><span class="sxs-lookup"><span data-stu-id="1d0c4-138">On the **Cash Flow Worksheet** page, choose the **Suggest Worksheet Lines** action.</span></span>  

## <a name="see-related-training-at-microsoft-learnlearnmodulesforecast-cash-flow-dynamics-365-business-centralindex"></a><span data-ttu-id="1d0c4-139">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="1d0c4-139">See Related Training at [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="1d0c4-140">Se även</span><span class="sxs-lookup"><span data-stu-id="1d0c4-140">See Also</span></span>
[<span data-ttu-id="1d0c4-141">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="1d0c4-141">Setting Up Finance</span></span>](finance-setup-finance.md)  
<span data-ttu-id="1d0c4-142">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1d0c4-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="1d0c4-143">Ställa in analys för kassaflöde</span><span class="sxs-lookup"><span data-stu-id="1d0c4-143">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  
