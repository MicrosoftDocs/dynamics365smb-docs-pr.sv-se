---
title: Designdetaljer | Microsoft Docs
description: "Detta innehållet innehåller detaljerad teknisk information om komplexa funktioner i Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 9c8ba2d7c2acaeb4c5c683f2f365e474e4f7bfce
ms.contentlocale: sv-se
ms.lasthandoff: 02/02/2018

---
# <a name="design-details"></a><span data-ttu-id="8747b-103">Designdetaljer</span><span class="sxs-lookup"><span data-stu-id="8747b-103">Design Details</span></span>
<span data-ttu-id="8747b-104">Innehållet består av detaljerad teknisk information om komplexa programfunktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8747b-104">This content contains detailed technical information about complex application features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

 <span data-ttu-id="8747b-105">Designdetaljinnehåll är avsett för genomförare, utvecklare och super users, som behöver en djupare insikt för att implementera, anpassa, eller ställa in funktionerna i fråga.</span><span class="sxs-lookup"><span data-stu-id="8747b-105">Design details content is aimed at implementers, developers, and super users who need deeper insight to implement, customize, or set up the features in question.</span></span>  

|<span data-ttu-id="8747b-106">**Om du vill**</span><span class="sxs-lookup"><span data-stu-id="8747b-106">**To**</span></span>|<span data-ttu-id="8747b-107">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="8747b-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="8747b-108">Lär dig mer om designen för att lagra och bokföra dimensioner, inklusive kodexempel på hur du migrerar och uppgraderar dimensionskod.</span><span class="sxs-lookup"><span data-stu-id="8747b-108">Learn about the design for storing and posting dimensions, including code examples on how to migrate and upgrade dimension code.</span></span>|[<span data-ttu-id="8747b-109">Designdetaljer: Dimensionsuppsättningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="8747b-109">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)|  
|<span data-ttu-id="8747b-110">Lär dig hur planeringssystemet fungerar och hur du justerar algoritmerna för att uppfylla planeringskrav i olika miljöer.</span><span class="sxs-lookup"><span data-stu-id="8747b-110">Learn how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="8747b-111">Designdetaljer: Leveransplanering</span><span class="sxs-lookup"><span data-stu-id="8747b-111">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|  
|<span data-ttu-id="8747b-112">Förstå mekanismer i värderingsmotorn, till exempel värderingsprincip och kostnadsjustering och vilka redovisningsprinciper de har utformats för.</span><span class="sxs-lookup"><span data-stu-id="8747b-112">Understand mechanisms in the costing engine, such as costing method and cost adjustment, and which accounting principles they are designed for.</span></span>|[<span data-ttu-id="8747b-113">Designdetaljer: Lagerkalkylering</span><span class="sxs-lookup"><span data-stu-id="8747b-113">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  
|<span data-ttu-id="8747b-114">Lära dig mer om centrala principer bakom avancerade och grundläggande lagerfunktioner och hur de integreras med andra funktioner i försörjningskedjan.</span><span class="sxs-lookup"><span data-stu-id="8747b-114">Learn about central principles behind advanced and basic warehouse features and how they integrate with other supply chain features.</span></span>|[<span data-ttu-id="8747b-115">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="8747b-115">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)|  
|<span data-ttu-id="8747b-116">Lär dig mer om historisk och aktuella utformning av artikelspårningfunktionen och hur den integreras med reservationssystemet för ta med serie-/partinummer i dispositionsberäkningarna.</span><span class="sxs-lookup"><span data-stu-id="8747b-116">Learn about historic and the current design of item tracking functionality and how it integrates with the reservation system to include serial/lot numbers in availability calculations.</span></span>|[<span data-ttu-id="8747b-117">Designdetaljer: Objektspårning</span><span class="sxs-lookup"><span data-stu-id="8747b-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)|  
|<span data-ttu-id="8747b-118">Lär dig mer om funktionen för radbokföring i redovisningsjournalen, inklusive nya förenklingar i utformningen av kodmodul 12.</span><span class="sxs-lookup"><span data-stu-id="8747b-118">Learn about the General Journal Posting Line feature, including recent simplifications to the design of codeunit 12.</span></span>|[<span data-ttu-id="8747b-119">Designdetaljer: Bokföring av rad i redovisningsjournalen</span><span class="sxs-lookup"><span data-stu-id="8747b-119">Design Details: General Journal Post Line</span></span>](design-details-general-journal-post-line.md)|  

## <a name="see-also"></a><span data-ttu-id="8747b-120">Se även</span><span class="sxs-lookup"><span data-stu-id="8747b-120">See Also</span></span>  
 <span data-ttu-id="8747b-121">[Planerad](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="8747b-121">[Planning](production-planning.md) </span></span>  
 <span data-ttu-id="8747b-122">[Hantera lagerkostnader](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="8747b-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="8747b-123">[Lagerstyrning](warehouse-manage-warehouse.md) </span><span class="sxs-lookup"><span data-stu-id="8747b-123">[Warehouse Management](warehouse-manage-warehouse.md) </span></span>  
 [<span data-ttu-id="8747b-124">Ställa in komplexa moduler med hjälp av bästa metoder</span><span class="sxs-lookup"><span data-stu-id="8747b-124">Setting Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="8747b-125">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8747b-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

 ## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 ## [!INCLUDE[d365fin](includes/training_link_md.md)]

