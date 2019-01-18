---
title: "Så här konfigurerar du lagerställeenheter | Microsoft Docs"
description: "Du kan använda lagerställeenheter för att registrera artikelinformation som rör ett visst lagerställe eller en viss variantkod."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: d5582e1857481d32ad146d0732f4c60d1b678c74
ms.contentlocale: sv-se
ms.lasthandoff: 11/20/2018

---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="c6251-103">Ställa in lagerställeenheter</span><span class="sxs-lookup"><span data-stu-id="c6251-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="c6251-104">Du kan använda lagerställeenheter för att registrera artikelinformation som rör ett visst lagerställe eller en viss variantkod.</span><span class="sxs-lookup"><span data-stu-id="c6251-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="c6251-105">Lagerplatsenheter fungerar som komplement till artikelkort.</span><span class="sxs-lookup"><span data-stu-id="c6251-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="c6251-106">De ersätter dem inte även om de är relaterade till dem.</span><span class="sxs-lookup"><span data-stu-id="c6251-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="c6251-107">Med lagerställeenheter kan du ha olika information om en artikel på ett visst lagerställe (t.ex. ett distributionslager eller ett distributionscenter) eller om en särskild variant, (t.ex. olika hyllnummer och olika återanskaffningsinformation) av samma artikel.</span><span class="sxs-lookup"><span data-stu-id="c6251-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="c6251-108">Så här skapar du lagerställeenheter</span><span class="sxs-lookup"><span data-stu-id="c6251-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="c6251-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lagerställeenheter** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c6251-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c6251-110">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c6251-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="c6251-111">Fyll i fälten på kortet.</span><span class="sxs-lookup"><span data-stu-id="c6251-111">Fill in the fields on the card.</span></span> <span data-ttu-id="c6251-112">Följande fält är obligatoriska: **Artikelnr**, **Lagerställekod**och/eller **Variantkod**.</span><span class="sxs-lookup"><span data-stu-id="c6251-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="c6251-113">När du har skapat den första lagerställeenheten för en artikel, markeras kryssrutan **Lagerställeenhet finns** på **artikelkortet**.</span><span class="sxs-lookup"><span data-stu-id="c6251-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="c6251-114">Om du vill skapa flera lagerställeenheter för en artikel, kan du använda batch-jobbet **Skapa lagerställeenhet**.</span><span class="sxs-lookup"><span data-stu-id="c6251-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c6251-115">Informationen på **lagerställeenhetskortet** har högre prioritet än informationen på **artikelkortet**.</span><span class="sxs-lookup"><span data-stu-id="c6251-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>

> [!Warning]
> <span data-ttu-id="c6251-116">Om LAGERSTÄLLEENHETEN levereras via produktion, kommer inte fältet **Standardkostnad** användas för fakturering, och justera den faktiska kostnaden för den producerade artikeln.</span><span class="sxs-lookup"><span data-stu-id="c6251-116">If the SKU is supplied through production, then the **Standard Cost** field is not used when invoicing and adjusting the actual cost of the produced item.</span></span> <span data-ttu-id="c6251-117">I stället används fältet **Standardkostnad** på den underliggande artikelkortet, och eventuella avvikelser beräknas mot kostnadsandelar för artikeln.</span><span class="sxs-lookup"><span data-stu-id="c6251-117">Instead, the **Standard Cost** field on the underlying item card is used, and any variances are calculated against the cost shares of that item.</span></span><br /><br />
> <span data-ttu-id="c6251-118">Eftersom produktionsstrukturer och operationsföljden inte kan tilldelas Lagerställekonfiguration, är styckkostnaden summerad och den relaterade beräkningen av kostnad delar inte heller tillgängliga på Lagerställeenheter.</span><span class="sxs-lookup"><span data-stu-id="c6251-118">Because production BOMs and routing cannot be assigned to SKUs, then the unit cost roll-up and the related calculation of cost shares are also not available on SKUs.</span></span> <span data-ttu-id="c6251-119">Mer information finns i [Om att beräkna standardkostnad](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="c6251-119">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="c6251-120">Se även</span><span class="sxs-lookup"><span data-stu-id="c6251-120">See Also</span></span>  
[<span data-ttu-id="c6251-121">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="c6251-121">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="c6251-122">Ställa in lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="c6251-122">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="c6251-123">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="c6251-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="c6251-124">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="c6251-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c6251-125">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="c6251-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="c6251-126">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="c6251-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="c6251-127">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c6251-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

