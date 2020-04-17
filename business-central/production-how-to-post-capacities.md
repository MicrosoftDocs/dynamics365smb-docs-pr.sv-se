---
title: Så här bokför du kapaciteter | Microsoft Docs
description: I kapacitetsjournalen bokför du förbrukade kapaciteter som inte kopplats till produktionsordern. Underhållsarbete måste till exempel kopplas till kapacitet, men inte till en produktionsorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e244f66e5bb080ff1bec0177d31079e0af39e701
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191601"
---
# <a name="post-capacities"></a><span data-ttu-id="30849-104">Bokför kapaciteter</span><span class="sxs-lookup"><span data-stu-id="30849-104">Post Capacities</span></span>
<span data-ttu-id="30849-105">I kapacitetsjournalen bokför du förbrukade kapaciteter som inte kopplats till produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="30849-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="30849-106">Underhållsarbete måste till exempel kopplas till kapacitet, men inte till en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="30849-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="30849-107">Så här bokför du kapaciteter</span><span class="sxs-lookup"><span data-stu-id="30849-107">To post capacities</span></span>  
1.  <span data-ttu-id="30849-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **kapacitetsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="30849-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="30849-109">Fyll i fälten **Bokföringsdatum** och **Verifikationsnummer** .</span><span class="sxs-lookup"><span data-stu-id="30849-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="30849-110">I fältet **Typ** anger du kapacitetstypen, endera **Maskingrupp** eller **Produktionsgrupp**, som du bokför.</span><span class="sxs-lookup"><span data-stu-id="30849-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="30849-111">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="30849-111">In the **No.**</span></span> <span data-ttu-id="30849-112">skriv numret på den artikel som har beställts.</span><span class="sxs-lookup"><span data-stu-id="30849-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="30849-113">Ange relevanta uppgifter i övriga fält, t.ex. **Starttid**, **Sluttid**, **Antal** och **Kassation**.</span><span class="sxs-lookup"><span data-stu-id="30849-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="30849-114">Välj åtgärden **Bokför** om du vill bokföra fakturan.</span><span class="sxs-lookup"><span data-stu-id="30849-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="30849-115">Så här visar du produktionsgruppstransaktioner</span><span class="sxs-lookup"><span data-stu-id="30849-115">To view work center ledger entries</span></span>  
<span data-ttu-id="30849-116">På sidan **produktionsgruppkort** och **maskingruppkort** kan du se bokförd kapacitet till följd av avslutade produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="30849-116">In the **Work Center Card** and **Machine Center Card** pages, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="30849-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **produktionsgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="30849-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="30849-118">Öppna relevant **produktionsgrupp**kort i listan och klicka på åtgärden **Kapacitetstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="30849-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="30849-119">På sidan **Kapacitetstransaktioner** visas de transaktioner som bokförts från produktionsgruppen i den ordning de bokförts i.</span><span class="sxs-lookup"><span data-stu-id="30849-119">The **Capacity Ledger Entries** page displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="30849-120">Se även</span><span class="sxs-lookup"><span data-stu-id="30849-120">See Also</span></span>  
<span data-ttu-id="30849-121">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="30849-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="30849-122">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="30849-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="30849-123">[Planerad](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="30849-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="30849-124">Lager</span><span class="sxs-lookup"><span data-stu-id="30849-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="30849-125">Inköp</span><span class="sxs-lookup"><span data-stu-id="30849-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="30849-126">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="30849-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
