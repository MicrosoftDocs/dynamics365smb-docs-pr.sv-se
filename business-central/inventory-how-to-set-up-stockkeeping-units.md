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
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4870e82d4390e0a96a137579d035fee0e54b19eb
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="34b28-103">Ställa in lagerställeenheter</span><span class="sxs-lookup"><span data-stu-id="34b28-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="34b28-104">Du kan använda lagerställeenheter för att registrera artikelinformation som rör ett visst lagerställe eller en viss variantkod.</span><span class="sxs-lookup"><span data-stu-id="34b28-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="34b28-105">Lagerplatsenheter fungerar som komplement till artikelkort.</span><span class="sxs-lookup"><span data-stu-id="34b28-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="34b28-106">De ersätter dem inte även om de är relaterade till dem.</span><span class="sxs-lookup"><span data-stu-id="34b28-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="34b28-107">Med lagerställeenheter kan du ha olika information om en artikel på ett visst lagerställe (t.ex. ett distributionslager eller ett distributionscenter) eller om en särskild variant, (t.ex. olika hyllnummer och olika återanskaffningsinformation) av samma artikel.</span><span class="sxs-lookup"><span data-stu-id="34b28-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="34b28-108">Så här skapar du lagerställeenheter</span><span class="sxs-lookup"><span data-stu-id="34b28-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="34b28-109">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lagerställeenheter**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="34b28-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="34b28-110">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="34b28-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="34b28-111">Fyll i fälten på kortet.</span><span class="sxs-lookup"><span data-stu-id="34b28-111">Fill in the fields on the card.</span></span> <span data-ttu-id="34b28-112">Följande fält är obligatoriska: **Artikelnr**, **Lagerställekod**och/eller **Variantkod**.</span><span class="sxs-lookup"><span data-stu-id="34b28-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="34b28-113">När du har skapat den första lagerställeenheten för en artikel, markeras kryssrutan **Lagerställeenhet finns** på **artikelkortet**.</span><span class="sxs-lookup"><span data-stu-id="34b28-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="34b28-114">Om du vill skapa flera lagerställeenheter för en artikel, kan du använda batch-jobbet **Skapa lagerställeenhet**.</span><span class="sxs-lookup"><span data-stu-id="34b28-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="34b28-115">Informationen på **lagerställeenhetskortet** har högre prioritet än informationen på **artikelkortet**.</span><span class="sxs-lookup"><span data-stu-id="34b28-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>  

## <a name="see-also"></a><span data-ttu-id="34b28-116">Se även</span><span class="sxs-lookup"><span data-stu-id="34b28-116">See Also</span></span>  
[<span data-ttu-id="34b28-117">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="34b28-117">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="34b28-118">Ställa in lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="34b28-118">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="34b28-119">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="34b28-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="34b28-120">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="34b28-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="34b28-121">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="34b28-121">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="34b28-122">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="34b28-122">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="34b28-123">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="34b28-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

