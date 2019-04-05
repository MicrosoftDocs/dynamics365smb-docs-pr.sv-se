---
title: Så här kan du uppdatera standardkostnader | Microsoft Docs
description: Du måste regelbundet uppdatera standardkostnader för komponenter och överföra de nya kostnaderna till den överordnade artikeln.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 88e715ddd2c60c3eb780ffe71d80676fdea00209
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807811"
---
# <a name="update-standard-costs"></a><span data-ttu-id="f78e4-103">Uppdatera standardkostnader</span><span class="sxs-lookup"><span data-stu-id="f78e4-103">Update Standard Costs</span></span>
<span data-ttu-id="f78e4-104">Du måste regelbundet uppdatera standardkostnader för komponenter och överföra de nya kostnaderna till den överordnade artikeln.</span><span class="sxs-lookup"><span data-stu-id="f78e4-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="f78e4-105">Processen består typiskt av följande fyra steg:</span><span class="sxs-lookup"><span data-stu-id="f78e4-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="f78e4-106">Uppdatera kostnader på komponent- och kapacitetsnivå.</span><span class="sxs-lookup"><span data-stu-id="f78e4-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="f78e4-107">Mer information finns i batch-jobbet **Föreslå artikelstandardkostnad**.</span><span class="sxs-lookup"><span data-stu-id="f78e4-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="f78e4-108">Konsolidera och summera komponent- och kapacitetskostnader för att beräkna den totala produktions- eller monteringskostnaden för artiklarna.</span><span class="sxs-lookup"><span data-stu-id="f78e4-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="f78e4-109">Använd standardkostnaderna som angavs när du körde de föregående batch-jobben.</span><span class="sxs-lookup"><span data-stu-id="f78e4-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="f78e4-110">Standardkostnaderna börjar inte gälla förrän de implementeras.</span><span class="sxs-lookup"><span data-stu-id="f78e4-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="f78e4-111">Mer information finns i Implementera standardkostnadsändringar.</span><span class="sxs-lookup"><span data-stu-id="f78e4-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="f78e4-112">Inför ändringarna för att uppdatera fältet **Styckkostnad** för artikelkortet och utföra lageromvärderingen.</span><span class="sxs-lookup"><span data-stu-id="f78e4-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="f78e4-113">Mer information finns i [Omvärdera lager](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="f78e4-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="f78e4-114">Mer information finns i [Om att beräkna standardkostnad](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="f78e4-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="f78e4-115">Uppdatera standardkostnader</span><span class="sxs-lookup"><span data-stu-id="f78e4-115">To update standard costs</span></span>  
1.  <span data-ttu-id="f78e4-116">Kör batch-jobbet **Justera kost. - artikeltrans.**</span><span class="sxs-lookup"><span data-stu-id="f78e4-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="f78e4-117">Kör batch-jobbet **Bokför lagerkostnad i redov.**</span><span class="sxs-lookup"><span data-stu-id="f78e4-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="f78e4-118">Öppna **Standardkostnadsformulär** och använd en eller flera av följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="f78e4-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="f78e4-119">Kör batch-jobbet **Föreslå artikelstandardkostnad**.</span><span class="sxs-lookup"><span data-stu-id="f78e4-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="f78e4-120">Granska resultaten och gör nödvändiga ändringar.</span><span class="sxs-lookup"><span data-stu-id="f78e4-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="f78e4-121">Kör batch-jobbet **Föreslå standardkostnad för kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="f78e4-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="f78e4-122">Granska resultaten och gör nödvändiga ändringar.</span><span class="sxs-lookup"><span data-stu-id="f78e4-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="f78e4-123">Kör batch-jobbet **Uppsummerad standardkostnad**.</span><span class="sxs-lookup"><span data-stu-id="f78e4-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="f78e4-124">Granska resultaten och gör nödvändiga ändringar.</span><span class="sxs-lookup"><span data-stu-id="f78e4-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="f78e4-125">Kör batch-jobbet **Implementera standardkostnadsändringar**.</span><span class="sxs-lookup"><span data-stu-id="f78e4-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="f78e4-126">Granska och bokför sidan **Omvärderingsjournal** , vilken har fyllts på med transaktioner från föregående steg i den här processen.</span><span class="sxs-lookup"><span data-stu-id="f78e4-126">Review and post the **Revaluation Journal** page, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f78e4-127">Se även</span><span class="sxs-lookup"><span data-stu-id="f78e4-127">See Also</span></span>  
 <span data-ttu-id="f78e4-128">[Om beräkning av standardkostnad](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="f78e4-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="f78e4-129">[Hantera lagerkostnader](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="f78e4-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="f78e4-130">[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md) [Finans](finance.md)</span><span class="sxs-lookup"><span data-stu-id="f78e4-130">[Design Details: Costing Methods](design-details-costing-methods.md) [[Finance](finance.md)</span></span>  
 <span data-ttu-id="f78e4-131">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f78e4-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
