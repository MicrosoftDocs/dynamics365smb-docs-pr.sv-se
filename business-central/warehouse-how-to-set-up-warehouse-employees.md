---
title: Så här registrerar du distributionslagerpersonal | Microsoft Docs
description: Alla användare som utför distributionslageraktiviteter måste registreras som distributionslageranställda som är tilldelade ett standardlagerställe och eventuellt andra lagerställen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ee03696db25242145232f11da58729b51d65654e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925328"
---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="69a93-103">Registrera distributionslagerpersonal</span><span class="sxs-lookup"><span data-stu-id="69a93-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="69a93-104">Alla användare som utför distributionslageraktiviteter måste registreras som distributionslageranställda som är tilldelade ett standardlagerställe och eventuellt andra lagerställen.</span><span class="sxs-lookup"><span data-stu-id="69a93-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="69a93-105">Denna användarinställning filtrerar alla distributionslageraktiviteter i hela databasen till den anställdes lagerställe, så att han eller hon bara kan utföra distributionslageraktiviteter vid standardlagerstället.</span><span class="sxs-lookup"><span data-stu-id="69a93-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="69a93-106">En användare kan tilldelas andra lagerställen som han eller hon kan visa aktivitetsrader för, men inte utföra aktiviteterna.</span><span class="sxs-lookup"><span data-stu-id="69a93-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="69a93-107">Så här registrerar du distributionslagerpersonal</span><span class="sxs-lookup"><span data-stu-id="69a93-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="69a93-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Distributionslagerpersonal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="69a93-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="69a93-109">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="69a93-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="69a93-110">Välj **Användar-ID** fältet och markera användaren som ska läggas till som distributionslageranvändare.</span><span class="sxs-lookup"><span data-stu-id="69a93-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="69a93-111">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="69a93-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="69a93-112">Gå till fältet **Lagerställekod** och ange koden för lagerstället där användaren ska arbeta.</span><span class="sxs-lookup"><span data-stu-id="69a93-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="69a93-113">Markera kryssrutan **Standard** för att ange att detta är det enda lagerställe som den anställda kan utföra aktiviteter på.</span><span class="sxs-lookup"><span data-stu-id="69a93-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="69a93-114">Upprepa de här stegen om du vill tilldela andra anställda till lagerställen, eller tilldela lagerställen som inte är standard till befintliga anställda.</span><span class="sxs-lookup"><span data-stu-id="69a93-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="69a93-115">Se även</span><span class="sxs-lookup"><span data-stu-id="69a93-115">See Also</span></span>  
[<span data-ttu-id="69a93-116">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="69a93-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="69a93-117">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="69a93-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="69a93-118">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="69a93-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="69a93-119">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="69a93-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="69a93-120">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="69a93-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="69a93-121">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="69a93-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
