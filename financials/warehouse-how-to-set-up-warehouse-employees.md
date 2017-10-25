---
title: "Så här registrerar du distributionslagerpersonal | Microsoft Docs"
description: "Alla användare som utför distributionslageraktiviteter måste registreras som distributionslageranställda som är tilldelade ett standardlagerställe och eventuellt andra lagerställen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6fb0aa48352bc35c2e9ee399a3d0b17032a5ed7e
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-warehouse-employees"></a><span data-ttu-id="4f0aa-103">Så här registrerar du distributionslagerpersonal</span><span class="sxs-lookup"><span data-stu-id="4f0aa-103">How to: Set Up Warehouse Employees</span></span>
<span data-ttu-id="4f0aa-104">Alla användare som utför distributionslageraktiviteter måste registreras som distributionslageranställda som är tilldelade ett standardlagerställe och eventuellt andra lagerställen.</span><span class="sxs-lookup"><span data-stu-id="4f0aa-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="4f0aa-105">Denna användarinställning filtrerar alla distributionslageraktiviteter i hela databasen till den anställdes lagerställe, så att han eller hon bara kan utföra distributionslageraktiviteter vid standardlagerstället.</span><span class="sxs-lookup"><span data-stu-id="4f0aa-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="4f0aa-106">En användare kan tilldelas andra lagerställen som han eller hon kan visa aktivitetsrader för, men inte utföra aktiviteterna.</span><span class="sxs-lookup"><span data-stu-id="4f0aa-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="4f0aa-107">Så här registrerar du distributionslagerpersonal</span><span class="sxs-lookup"><span data-stu-id="4f0aa-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="4f0aa-108">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Dist.lager personal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4f0aa-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4f0aa-109">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4f0aa-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="4f0aa-110">Välj **Användar-ID** fältet och markera användaren som ska läggas till som distributionslageranvändare.</span><span class="sxs-lookup"><span data-stu-id="4f0aa-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="4f0aa-111">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f0aa-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="4f0aa-112">Gå till fältet **Lagerställekod** och ange koden för lagerstället där användaren ska arbeta.</span><span class="sxs-lookup"><span data-stu-id="4f0aa-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="4f0aa-113">Markera kryssrutan **Standard** för att ange att detta är det enda lagerställe som den anställda kan utföra aktiviteter på.</span><span class="sxs-lookup"><span data-stu-id="4f0aa-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="4f0aa-114">Upprepa de här stegen om du vill tilldela andra anställda till lagerställen, eller tilldela lagerställen som inte är standard till befintliga anställda.</span><span class="sxs-lookup"><span data-stu-id="4f0aa-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4f0aa-115">Se även</span><span class="sxs-lookup"><span data-stu-id="4f0aa-115">See Also</span></span>  
[<span data-ttu-id="4f0aa-116">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="4f0aa-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="4f0aa-117">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="4f0aa-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="4f0aa-118">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="4f0aa-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="4f0aa-119">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="4f0aa-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="4f0aa-120">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="4f0aa-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="4f0aa-121">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4f0aa-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

