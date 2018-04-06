---
title: "Så här bokför du kapaciteter | Microsoft Docs"
description: "I kapacitetsjournalen bokför du förbrukade kapaciteter som inte kopplats till produktionsordern. Underhållsarbete måste till exempel kopplas till kapacitet, men inte till en produktionsorder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a30e62bf2bf62c547398d733fcfe80b0204805cf
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="post-capacities"></a><span data-ttu-id="ab048-104">Bokför kapaciteter</span><span class="sxs-lookup"><span data-stu-id="ab048-104">Post Capacities</span></span>
<span data-ttu-id="ab048-105">I kapacitetsjournalen bokför du förbrukade kapaciteter som inte kopplats till produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="ab048-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="ab048-106">Underhållsarbete måste till exempel kopplas till kapacitet, men inte till en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="ab048-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="ab048-107">Så här bokför du kapaciteter</span><span class="sxs-lookup"><span data-stu-id="ab048-107">To post capacities</span></span>  
1.  <span data-ttu-id="ab048-108">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kapacitetsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ab048-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ab048-109">Fyll i fälten **Bokföringsdatum** och **Verifikationsnummer** .</span><span class="sxs-lookup"><span data-stu-id="ab048-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="ab048-110">I fältet **Typ** anger du kapacitetstypen, endera **Maskingrupp** eller **Produktionsgrupp**, som du bokför.</span><span class="sxs-lookup"><span data-stu-id="ab048-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="ab048-111">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="ab048-111">In the **No.**</span></span> <span data-ttu-id="ab048-112">skriv numret på den artikel som har beställts.</span><span class="sxs-lookup"><span data-stu-id="ab048-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="ab048-113">Ange relevanta uppgifter i övriga fält, t.ex. **Starttid**, **Sluttid**, **Antal** och **Kassation**.</span><span class="sxs-lookup"><span data-stu-id="ab048-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="ab048-114">Välj åtgärden **Bokför** om du vill bokföra fakturan.</span><span class="sxs-lookup"><span data-stu-id="ab048-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="ab048-115">Så här visar du produktionsgruppstransaktioner</span><span class="sxs-lookup"><span data-stu-id="ab048-115">To view work center ledger entries</span></span>  
<span data-ttu-id="ab048-116">I fönstren **produktionsgruppkort** och **maskingruppkort** kan du se bokförd kapacitet till följd av avslutade produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="ab048-116">In the **Work Center Card** and **Machine Center Card** windows, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="ab048-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Arbetsskift** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ab048-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ab048-118">Öppna relevant **produktionsgrupp**kort i listan och klicka på åtgärden **Kapacitetstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="ab048-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="ab048-119">I fönstret **Kapacitetstransaktioner** visas de transaktioner som bokförts från produktionsgruppen i den ordning de bokförts i.</span><span class="sxs-lookup"><span data-stu-id="ab048-119">The **Capacity Ledger Entries** window displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="ab048-120">Se även</span><span class="sxs-lookup"><span data-stu-id="ab048-120">See Also</span></span>  
<span data-ttu-id="ab048-121">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="ab048-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="ab048-122">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="ab048-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="ab048-123">[Planerad](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="ab048-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="ab048-124">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="ab048-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ab048-125">Inköp</span><span class="sxs-lookup"><span data-stu-id="ab048-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ab048-126">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ab048-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

