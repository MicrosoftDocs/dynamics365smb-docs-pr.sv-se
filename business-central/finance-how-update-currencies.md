---
title: Uppdatera valutakurser | Microsoft Docs
description: "För att använda flera valutor i din verksamhet, kan du lägga upp en kod för varje valuta och använda en extern valutakurstjänst."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: sv-se
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a><span data-ttu-id="c1b2d-103">Uppdatera valutakurser</span><span class="sxs-lookup"><span data-stu-id="c1b2d-103">Update Currency Exchange Rates</span></span>
<span data-ttu-id="c1b2d-104">Eftersom företag verkar i allt fler länder/regioner blir det alltmer viktigt att de kan använda och rapportera ekonomiska siffror i fler än en valuta.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-104">As companies operate in increasingly more countries/regions, it becomes more important that they be able to trade and report financials in more than one currency.</span></span> <span data-ttu-id="c1b2d-105">Du måste ange en kod för varje valuta du använder om du köper eller säljer i andra valutor än din lokala valuta, har tillgångar eller skulder i andra valutor eller registrerar transaktioner i olika valutor.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-105">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>

<span data-ttu-id="c1b2d-106">Din redovisning ställs in för att använda den lokala valutan (BVA) men du kan ställa in en annan valuta med en tilldelad aktuell valutakurs.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-106">Your general ledger is set up to use your local currency (LCY), but you can set it up to also use another currency with a current exchange rate assigned.</span></span> <span data-ttu-id="c1b2d-107">Genom att ange en andra valuta som en så kallad alternativ rapporteringsvaluta kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] registrera belopp automatiskt i både BVA och den alternativa rapporteringsvalutan för varje redovisningstransaktion och för andra transaktioner, t.ex. momstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-107">By designating a second currency as a so-called additional reporting currency, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically record amounts in both LCY and this additional reporting currency on each G/L entry and other entries, such as VAT entries.</span></span> <span data-ttu-id="c1b2d-108">Mer information finns i [Ställa in en alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md).</span><span class="sxs-lookup"><span data-stu-id="c1b2d-108">For more information, see [Set Up an Additional Reporting Currency](finance-how-setup-additional-currencies.md).</span></span>

## <a name="adjusting-exchange-rates"></a><span data-ttu-id="c1b2d-109">Justera valutakurser</span><span class="sxs-lookup"><span data-stu-id="c1b2d-109">Adjusting Exchange Rates</span></span>
<span data-ttu-id="c1b2d-110">Eftersom valutakurser ständigt fluktuerar måste alternativa valutavärden i systemet justeras med jämna mellanrum.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-110">Because exchange rates fluctuate constantly, additional currency equivalents in your system must be adjusted periodically.</span></span> <span data-ttu-id="c1b2d-111">Om dessa justeringar inte görs kan de belopp som har konverterats från utländska (eller alternativa) valutor och bokförts i huvudboken i BVA vara missvisande.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-111">If these adjustments are not done, amounts that have been converted from foreign (or additional) currencies and posted to the general ledger in LCY may be misleading.</span></span> <span data-ttu-id="c1b2d-112">Dessutom måste dagliga transaktioner som bokförs innan en daglig valutakurs har registrerats i programmet uppdateras efter det att den dagliga valutakursinformationen har registrerats.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-112">In addition, daily entries posted before a daily exchange rate is entered into the program must be updated after the daily exchange rate information is entered.</span></span> <span data-ttu-id="c1b2d-113">Batch-jobbet Justera valutakurser används för att justera valutakurserna för bokförda kund-, leverantörs- och bankkontotransaktioner.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-113">The Adjust Exchange Rates batch job is used to adjust the exchange rates of posted customer, vendor and bank account entries.</span></span> <span data-ttu-id="c1b2d-114">Det kan även användas för att uppdatera belopp i alternativ rapporteringsvaluta för redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-114">It can also update additional reporting currency amounts on G/L entries.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="c1b2d-115">Så här konfigurerar du en valutakurstjänst</span><span class="sxs-lookup"><span data-stu-id="c1b2d-115">To set up a currency exchange rate service</span></span>
<span data-ttu-id="c1b2d-116">Du kan använda en extern tjänst, till exempel FloatRates, för kontinuerlig uppdatering av aktuella valutakurser.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-116">You can use an external service to keep your currency exchange rates up to date, such as FloatRates.</span></span>

1. <span data-ttu-id="c1b2d-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Valutakurstjänster** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="c1b2d-118">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-118">Choose the **New** action.</span></span>
3. <span data-ttu-id="c1b2d-119">På sidan **Valutakurstjänster** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-119">On the **Currency Exchange Rate Service** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="c1b2d-120">Välj kryssrutan **aktiverad** om du vill aktivera tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-120">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="c1b2d-121">Så här uppdaterar du valutakurser från en tjänst</span><span class="sxs-lookup"><span data-stu-id="c1b2d-121">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="c1b2d-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Valutor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="c1b2d-123">Välj åtgärden **uppdatera valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-123">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="c1b2d-124">Värdet i fältet **valutakurs** på sidan **valutor** uppdateras med den senaste valutakursen.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-124">The value in the **Exchange Rate** field on the **Currencies** page is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1b2d-125">Se även</span><span class="sxs-lookup"><span data-stu-id="c1b2d-125">See Also</span></span>
[<span data-ttu-id="c1b2d-126">Ställa in en alternativ rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-126">Set Up an Additional Reporting Currency</span></span>](finance-how-setup-additional-currencies.md)  
[<span data-ttu-id="c1b2d-127">Avsluta år och perioder</span><span class="sxs-lookup"><span data-stu-id="c1b2d-127">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="c1b2d-128">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c1b2d-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

