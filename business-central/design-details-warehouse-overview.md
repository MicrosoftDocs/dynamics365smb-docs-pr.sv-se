---
title: Designdetaljer - Lagerhantering översikt | Microsoft Docs
description: För att stödja den fysiska hanteringen av artiklar i zonen och på lagerplatsnivån måste all information spåras för varje transaktion eller transport i distributionslagret. Det hanteras i tabellen **Dist.lager transaktion**. Varje transaktion lagras i ett distributionslagerregister.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b265f8a910ba4d6e36856ce6d4485532b4e1337a
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920828"
---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="3ca85-105">Designdetaljer: Översikt över distributionslager</span><span class="sxs-lookup"><span data-stu-id="3ca85-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="3ca85-106">För att stödja den fysiska hanteringen av artiklar i zonen och på lagerplatsnivån måste all information spåras för varje transaktion eller transport i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="3ca85-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="3ca85-107">Det hanteras i tabellen **Dist.lager transaktion**.</span><span class="sxs-lookup"><span data-stu-id="3ca85-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="3ca85-108">Varje transaktion lagras i ett distributionslagerregister.</span><span class="sxs-lookup"><span data-stu-id="3ca85-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="3ca85-109">Distributionslagerdokument och en distributionslagerjournal används för att registrera artikeltransporter i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="3ca85-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="3ca85-110">Varje gång en artikel i distributionslagret flyttas, tas emot, förs in, plockas, utlevereras eller justeras, registreras distributionslagertransaktioner för att lagra den fysiska informationen om zon, lagerplats och antal.</span><span class="sxs-lookup"><span data-stu-id="3ca85-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span>

<span data-ttu-id="3ca85-111">Tabellen **Lagerplatsinnehåll** används för att hantera alla olika dimensioner av innehållet i en lagerplats per artikel, t.ex enhet, maximal antal och lägsta antal.</span><span class="sxs-lookup"><span data-stu-id="3ca85-111">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="3ca85-112">Tabellen **Lagerplatsinnehåll** innehåller även flödesfält till distributionslagertransaktionerna, distributionslagerinstruktionerna och distributionslagerjournalraderna, som säkerställer att tillgängligheten för en artikel per lagerplats och en lagerplats för en artikel kan beräknas snabbt.</span><span class="sxs-lookup"><span data-stu-id="3ca85-112">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="3ca85-113">Mer information finns i [Designdetaljer: disposition i distributionslagret](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="3ca85-113">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="3ca85-114">När artikeltransaktioner uppstår utanför distributionslagerenheten används en standardjusteringlagerplats per lagerställe för att synkronisera distributionslagerposter med lagerposter.</span><span class="sxs-lookup"><span data-stu-id="3ca85-114">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="3ca85-115">Under inventeringen av distributionslagret registreras alla avvikelser mellan de beräknade och inventerade kvantiteterna på justeringslagerplatsen och sedan bokförs de som korrigerande artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="3ca85-115">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="3ca85-116">Mer information finns i [Designdetaljer: Integrering med lager](design-details-integration-with-inventory.md)</span><span class="sxs-lookup"><span data-stu-id="3ca85-116">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="3ca85-117">Följande illustration ger en översikt över typiska distributionslagerflöden.</span><span class="sxs-lookup"><span data-stu-id="3ca85-117">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="3ca85-118">![Översikt över lagerprocesser](media/design_details_warehouse_management_overview.png "Översikt över lagerprocesser")</span><span class="sxs-lookup"><span data-stu-id="3ca85-118">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "Overview of warehouse processes")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="3ca85-119">Grundläggande eller avancerad lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="3ca85-119">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="3ca85-120">Distributionslagerfunktion i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan implementeras i olika komplexitetsnivåer, beroende på ett företag processer och ordervolym.</span><span class="sxs-lookup"><span data-stu-id="3ca85-120">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="3ca85-121">Den huvudsakliga skillnaden är att aktiviteter utförs order-för-order i grundläggande lagerstyrning, när de konsolideras för flera order i avancerad lagerstyrning.</span><span class="sxs-lookup"><span data-stu-id="3ca85-121">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="3ca85-122">För att skilja mellan de olika komplexitetsnivåerna refererar denna dokumentation till två allmänna benämningar, grundläggande och avancerad lagerstyrning.</span><span class="sxs-lookup"><span data-stu-id="3ca85-122">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="3ca85-123">Den här enkla differentieringen täcker flera olika komplexitetsnivåer som definieras av produktpartiklar och lagerplatsinställningar, där var och en stöds av olika användargränssnittsdokument .</span><span class="sxs-lookup"><span data-stu-id="3ca85-123">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="3ca85-124">Mer information finns i [Designdetaljer: Lagerstyrningsinställningar](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="3ca85-124">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3ca85-125">Den mest avancerade nivån av lagerstyrning kallas för ”WMS-installationer” i denna dokumentation, eftersom den här nivån kräver den mest avancerade partikeln, lagerstyrningssystem (Warehouse Management Systems).</span><span class="sxs-lookup"><span data-stu-id="3ca85-125">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="3ca85-126">Följande olika användargränssnittsdokument används i grundläggande och avancerade lagerhantering.</span><span class="sxs-lookup"><span data-stu-id="3ca85-126">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="3ca85-127">Grundläggande gränssnittsdokument</span><span class="sxs-lookup"><span data-stu-id="3ca85-127">Basic UI Documents</span></span>  

-   <span data-ttu-id="3ca85-128">**Lagerinförsel**</span><span class="sxs-lookup"><span data-stu-id="3ca85-128">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="3ca85-129">**Lagerplockning**</span><span class="sxs-lookup"><span data-stu-id="3ca85-129">**Inventory Pick**</span></span>  
-   <span data-ttu-id="3ca85-130">**Lagertransport**</span><span class="sxs-lookup"><span data-stu-id="3ca85-130">**Inventory Movement**</span></span>  
-   <span data-ttu-id="3ca85-131">**Artikeljournal**</span><span class="sxs-lookup"><span data-stu-id="3ca85-131">**Item Journal**</span></span>  
-   <span data-ttu-id="3ca85-132">**Artikelgrupperingsjournal**</span><span class="sxs-lookup"><span data-stu-id="3ca85-132">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="3ca85-133">(Olika rapporter)</span><span class="sxs-lookup"><span data-stu-id="3ca85-133">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="3ca85-134">Avancerade UI-dokument</span><span class="sxs-lookup"><span data-stu-id="3ca85-134">Advanced UI Documents</span></span>  

-   <span data-ttu-id="3ca85-135">**Dist.lager inleverans**</span><span class="sxs-lookup"><span data-stu-id="3ca85-135">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="3ca85-136">**Artikelinförsel kalkylark**</span><span class="sxs-lookup"><span data-stu-id="3ca85-136">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="3ca85-137">**Dist.lager artikelinförsel**</span><span class="sxs-lookup"><span data-stu-id="3ca85-137">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="3ca85-138">**Plockningskalkylark**</span><span class="sxs-lookup"><span data-stu-id="3ca85-138">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="3ca85-139">**Dist.lager plockning**</span><span class="sxs-lookup"><span data-stu-id="3ca85-139">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="3ca85-140">**Transportkalkylark**</span><span class="sxs-lookup"><span data-stu-id="3ca85-140">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="3ca85-141">**Dist.lager transport**</span><span class="sxs-lookup"><span data-stu-id="3ca85-141">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="3ca85-142">**Intern dist.lager plockning**</span><span class="sxs-lookup"><span data-stu-id="3ca85-142">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="3ca85-143">**Intern dist.lager art.införsel<**</span><span class="sxs-lookup"><span data-stu-id="3ca85-143">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="3ca85-144">**lagerplatsuppläggningskalkylark**</span><span class="sxs-lookup"><span data-stu-id="3ca85-144">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="3ca85-145">**Lagerplatsinnehålluppl kalkylark**</span><span class="sxs-lookup"><span data-stu-id="3ca85-145">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="3ca85-146">**Dist.lager artikeljournal**</span><span class="sxs-lookup"><span data-stu-id="3ca85-146">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="3ca85-147">**Dist.lager Artikelgrupperingsjnl**</span><span class="sxs-lookup"><span data-stu-id="3ca85-147">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="3ca85-148">(Olika rapporter)</span><span class="sxs-lookup"><span data-stu-id="3ca85-148">(Various reports)</span></span>  

<span data-ttu-id="3ca85-149">Se respektive sidavsnitt för mer information om varje dokument.</span><span class="sxs-lookup"><span data-stu-id="3ca85-149">For more information about each document, see the respective page topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="3ca85-150">Terminologi</span><span class="sxs-lookup"><span data-stu-id="3ca85-150">Terminology</span></span>  
<span data-ttu-id="3ca85-151">För att anpassas till de ekonomiska begreppen för inköp och försäljningar refererar lagerdokumentationen för [!INCLUDE[d365fin](includes/d365fin_md.md)] till följande villkor för objektflöde i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="3ca85-151">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="3ca85-152">Term</span><span class="sxs-lookup"><span data-stu-id="3ca85-152">Term</span></span>|<span data-ttu-id="3ca85-153">Description</span><span class="sxs-lookup"><span data-stu-id="3ca85-153">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="3ca85-154">Ankommande flöde</span><span class="sxs-lookup"><span data-stu-id="3ca85-154">Inbound flow</span></span>|<span data-ttu-id="3ca85-155">Artiklar som transporteras in till distributionslagerplatsen, till exempel inköp och ankommande överföringar.</span><span class="sxs-lookup"><span data-stu-id="3ca85-155">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="3ca85-156">Internt flöde</span><span class="sxs-lookup"><span data-stu-id="3ca85-156">Internal flow</span></span>|<span data-ttu-id="3ca85-157">Artiklar som transporteras inom distributionslagerplatsen, till exempel produktionskomponenter och utflöde.</span><span class="sxs-lookup"><span data-stu-id="3ca85-157">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="3ca85-158">Avgående flöde</span><span class="sxs-lookup"><span data-stu-id="3ca85-158">Outbound flow</span></span>|<span data-ttu-id="3ca85-159">Artiklar som transporteras ut ur distributionslagerplatsen, till exempel försäljningar och avgående överföringar.</span><span class="sxs-lookup"><span data-stu-id="3ca85-159">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="3ca85-160">Se även</span><span class="sxs-lookup"><span data-stu-id="3ca85-160">See Also</span></span>  
 [<span data-ttu-id="3ca85-161">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="3ca85-161">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)
