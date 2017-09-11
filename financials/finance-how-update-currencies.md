---
title: Uppdatera valutakurser | Microsoft Docs
description: "För att använda flera valutor i din verksamhet, kan du lägga upp en kod för varje valuta och använda en extern valutakurstjänst, som t.ex. Yahoo."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-update-currency-exchange-rates"></a><span data-ttu-id="43d16-103">Så här uppdaterar du valutakurser</span><span class="sxs-lookup"><span data-stu-id="43d16-103">How to: Update Currency Exchange Rates</span></span>
<span data-ttu-id="43d16-104">Du måste ange en kod för varje valuta du använder om du köper eller säljer i andra valutor än din lokala valuta, har tillgångar eller skulder i andra valutor eller registrerar transaktioner i olika valutor.</span><span class="sxs-lookup"><span data-stu-id="43d16-104">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="43d16-105">Den här funktionen kräver att din upplevelse är inställd på **Paket**.</span><span class="sxs-lookup"><span data-stu-id="43d16-105">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="43d16-106">Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="43d16-106">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

<span data-ttu-id="43d16-107">Du kan använda en extern tjänst för kontinuerlig uppdatering av aktuella valutakurser.</span><span class="sxs-lookup"><span data-stu-id="43d16-107">You can use an external service to keep your currency exchange rates up to date.</span></span> <span data-ttu-id="43d16-108">Tjänsten Yahoo valutakurser är förinstallerade och redo att aktiveras.</span><span class="sxs-lookup"><span data-stu-id="43d16-108">The Yahoo Currency Exchange Rates service is preinstalled and ready to enable.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="43d16-109">Så här konfigurerar du en valutakurstjänst</span><span class="sxs-lookup"><span data-stu-id="43d16-109">To set up a currency exchange rate service</span></span>
1. <span data-ttu-id="43d16-110">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Valutakurstjänster** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="43d16-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="43d16-111">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="43d16-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="43d16-112">I fönstret **Valutakurstjänster** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="43d16-112">In the **Currency Exchange Rate Service** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="43d16-113">Välj kryssrutan **aktiverad** om du vill aktivera tjänsten.</span><span class="sxs-lookup"><span data-stu-id="43d16-113">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="43d16-114">Så här uppdaterar du valutakurser från en tjänst</span><span class="sxs-lookup"><span data-stu-id="43d16-114">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="43d16-115">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Valutor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="43d16-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="43d16-116">Välj åtgärden **uppdatera valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="43d16-116">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="43d16-117">Värdet i fältet **valutakurs** i fönstret **valutor** uppdateras med den senaste valutakursen.</span><span class="sxs-lookup"><span data-stu-id="43d16-117">The value in the **Exchange Rate** field in the **Currencies** window is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="43d16-118">Se även</span><span class="sxs-lookup"><span data-stu-id="43d16-118">See Also</span></span>
[<span data-ttu-id="43d16-119">Avsluta år och perioder</span><span class="sxs-lookup"><span data-stu-id="43d16-119">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="43d16-120">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="43d16-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

