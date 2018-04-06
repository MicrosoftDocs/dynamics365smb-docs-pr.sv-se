---
title: "Så här: välj för Intern operation i avancerad distributionslagerkonfiguration | Microsoft Docs"
description: "I avancerad distributionslagerkonfiguration, där det har angetts att lagerstället ska använda plockning samt leverans, kan du välja plockkomponenter för produktion- och monteringsaktiviteter med fönstret **Dist.lager plockning**."
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
ms.openlocfilehash: 0a18e88ae9bb34b3cf5aa9d4a28e1d087ba9aa40
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="pick-for-assembly-or-production-in-advanced-warehouse-configurations"></a><span data-ttu-id="9a464-103">Plocka för montering eller produktion i avancerad distributionslagerkonfiguration</span><span class="sxs-lookup"><span data-stu-id="9a464-103">Pick for Assembly or Production in Advanced Warehouse Configurations</span></span>
<span data-ttu-id="9a464-104">I avancerad distributionslagerkonfiguration, där det har angetts att lagerstället ska använda plockning samt leverans, kan du välja plockkomponenter för produktion- och monteringsaktiviteter med fönstret **Dist.lager plockning**.</span><span class="sxs-lookup"><span data-stu-id="9a464-104">In advanced warehouse configurations where the location is set up to use picking as well as shipping, you can pick components for production and assembly activities with the **Warehouse Pick** window.</span></span>  

<span data-ttu-id="9a464-105">Du kan också använda **Transportkalkylark** fönstret för att flytta artiklar mellan lagerplatser ad hoc-, d.v.s till utan att referera till ett ursprungsdokument.</span><span class="sxs-lookup"><span data-stu-id="9a464-105">Alternatively, you can use the **Movement Worksheet** window to move items between bins ad hoc, meaning without reference to a source document.</span></span> <span data-ttu-id="9a464-106">Mer information finns i [Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="9a464-106">For more information, see [Move Items in advanced warehouse configurations](warehouse-how-to-move-items-in-advanced-warehousing.md).</span></span>  

<span data-ttu-id="9a464-107">Information om hur du plockar artiklar för intern verksamhet på grundläggande lagerställen som endast definierats för plockning, se [Flytta komponenter till ett verksamhetsområde i grundläggande distributionslagerkonfiguration](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="9a464-107">For information about picking items for internal operations in basic warehouse locations that are set up for picking only, see [Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>  

<span data-ttu-id="9a464-108">Du kan inte skapa ett dokument för dist.lager plockning från grunden, eftersom en plockningsaktivitet alltid ingår i ett arbetsflöde, i ett pull-/pushscenario.</span><span class="sxs-lookup"><span data-stu-id="9a464-108">You cannot create a warehouse pick document from scratch because a pick activity is always part of a workflow, either in a pull or a push scenario.</span></span>  

<span data-ttu-id="9a464-109">Du kan skapa dokumentet för dist.lager plockning med en pushmetod genom att välja **Skapa dist.lagerplockning** i källdokumentet, till exempel en släppt monteringsorder eller lagerutleverans.</span><span class="sxs-lookup"><span data-stu-id="9a464-109">You can create the warehouse pick document in a push fashion by selecting **Create Whse. Pick** on the source document, such as a released assembly order or warehouse shipment.</span></span> <span data-ttu-id="9a464-110">För mer information, se [Plocka artiklar med lagerplockningar](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="9a464-110">For more information, see [Pick Items with Warehouse Picks](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span></span>  

<span data-ttu-id="9a464-111">Du kan också skapa dokumentet för dist.lager plockning med en pullmetod med hjälp av **Plockningskalkylark** fönstret för att undersöka plockningsförfrågningar, både för leverans och intern operation, och sedan skapa de nödvändiga dokumentet för dist.lager plockning.</span><span class="sxs-lookup"><span data-stu-id="9a464-111">Alternatively, you can create the warehouse pick document in a pull fashion by using the **Pick Worksheet** window to detect pick requests, both for shipment and internal operations, and then create the required warehouse pick documents.</span></span>  

<span data-ttu-id="9a464-112">Nedan förklaras ett pull-scenario där du plockar komponenter för en släppt produktionsorder via **Plockningskalkylark** fönstret.</span><span class="sxs-lookup"><span data-stu-id="9a464-112">The following procedure explains a pull scenario where you pick components for a released production order through the **Pick Worksheet** window.</span></span> <span data-ttu-id="9a464-113">Följande procedur gäller även för en monteringsorder.</span><span class="sxs-lookup"><span data-stu-id="9a464-113">The procedure also applies for an assembly order.</span></span>  

<span data-ttu-id="9a464-114">För att skapa plockning för både pull- och pushscenarier, måste källdokumenten släppas.</span><span class="sxs-lookup"><span data-stu-id="9a464-114">To create pick requests, both for pull and for push scenarios, the source documents in question must be released.</span></span> <span data-ttu-id="9a464-115">Släppa källdokumenten för intern operation på följande sätt.</span><span class="sxs-lookup"><span data-stu-id="9a464-115">Release source documents for internal operations in the following ways.</span></span>  

|<span data-ttu-id="9a464-116">Källdokument</span><span class="sxs-lookup"><span data-stu-id="9a464-116">Source Document</span></span>|<span data-ttu-id="9a464-117">Släppningsmetod</span><span class="sxs-lookup"><span data-stu-id="9a464-117">Release Method</span></span>|  
|---------------------|--------------------|  
|<span data-ttu-id="9a464-118">Produktionsorder</span><span class="sxs-lookup"><span data-stu-id="9a464-118">Production Order</span></span>|<span data-ttu-id="9a464-119">Ändra ordertyp till släppta produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="9a464-119">Change order type to released production order.</span></span>|  
|<span data-ttu-id="9a464-120">Monteringsorder</span><span class="sxs-lookup"><span data-stu-id="9a464-120">Assembly Order</span></span>|<span data-ttu-id="9a464-121">Ändra status till släppt.</span><span class="sxs-lookup"><span data-stu-id="9a464-121">Change status to Released.</span></span>|  

## <a name="to-pick-components-using-the-pick-worksheet"></a><span data-ttu-id="9a464-122">Så här plockar du komponenter med hjälp av plockningskalkylarket</span><span class="sxs-lookup"><span data-stu-id="9a464-122">To pick components using the pick worksheet</span></span>  
1.  <span data-ttu-id="9a464-123">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Plockningskalkylark**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9a464-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Pick Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9a464-124">Välj åtgärden **Hämta dist.lager dokument** och välj sedan de komponentrader från den släppta produktionsordern.</span><span class="sxs-lookup"><span data-stu-id="9a464-124">Choose the **Get Warehouse Documents** action, and then select the component lines from the released production order.</span></span>  
3.  <span data-ttu-id="9a464-125">Analysera raderna, sortera dem för att garantera en effektiv plockningsrunda och kombinera dem med andra kalkylarksrader, om så behövs, för att minimera plockningstiden för den anställda.</span><span class="sxs-lookup"><span data-stu-id="9a464-125">Inspect the lines, sort them to ensure an efficient picking round, and combine them with other worksheet lines if necessary to make best use of employee time.</span></span>  
4.  <span data-ttu-id="9a464-126">Välj åtgärden **Skapa plockning**.</span><span class="sxs-lookup"><span data-stu-id="9a464-126">Choose the **Create Pick** action.</span></span>  
5.  <span data-ttu-id="9a464-127">Definiera hur du skapar dokument för dist.lager plockning och hur här fältet sorterar plockningsrader genom att fylla i **Skapa plockning** fönstret.</span><span class="sxs-lookup"><span data-stu-id="9a464-127">Define how to create the warehouse pick documents and how to sort pick lines by filling fields in the **Create Pick** window.</span></span>  
6.  <span data-ttu-id="9a464-128">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a464-128">Choose the **OK** button.</span></span> <span data-ttu-id="9a464-129">Dokumenten för dist.lager plockning skapas med plockningsrader för varje komponent som krävs i den intern operation.</span><span class="sxs-lookup"><span data-stu-id="9a464-129">Warehouse pick documents are created with pick lines for each component that is required in the internal operation.</span></span>  

<span data-ttu-id="9a464-130">Om internt verksamhetsområde, till exempel ett produktionslagerplats, har upprättats med en standardlagerplats för placering av komponenter som ska användas i operationen, infogas den lagerplatskoden i placeringsraderna på dokumentet för dist.lager plockning för att visa lagerarbetare var artiklarna ska placeras.</span><span class="sxs-lookup"><span data-stu-id="9a464-130">If the internal operation area, such as a production shop floor, is set up with a default bin for placement of components to be used in the operation, then that bin code is inserted in the Place lines on the warehouse pick document to instruct warehouse workers where to place the items.</span></span> <span data-ttu-id="9a464-131">Mer information finns på **Till prod.-lagerplats - kod** eller fältet **Till monteringsplats - kod**.</span><span class="sxs-lookup"><span data-stu-id="9a464-131">For more information, see the **To-Production Bin Code** or the **To-Assembly Bin Code** field.</span></span>

## <a name="filling-the-consumption-bin"></a><span data-ttu-id="9a464-132">Fylla förbrukningslagerplatsen</span><span class="sxs-lookup"><span data-stu-id="9a464-132">Filling the Consumption Bin</span></span>
<span data-ttu-id="9a464-133">Diagrammet visar hur **Lagerplatskod** på produktionsorderkomponentraderna fylls enligt platsinställningen.</span><span class="sxs-lookup"><span data-stu-id="9a464-133">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your location setup.</span></span>

<span data-ttu-id="9a464-134">![Flödesschema för lagerplats](media/binflow.png "BinFlow")</span><span class="sxs-lookup"><span data-stu-id="9a464-134">![Bin flow chart](media/binflow.png "BinFlow")</span></span>  

## <a name="see-also"></a><span data-ttu-id="9a464-135">Se även</span><span class="sxs-lookup"><span data-stu-id="9a464-135">See Also</span></span>
[<span data-ttu-id="9a464-136">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="9a464-136">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="9a464-137">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="9a464-137">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="9a464-138">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="9a464-138">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="9a464-139">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="9a464-139">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="9a464-140">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="9a464-140">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="9a464-141">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9a464-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

