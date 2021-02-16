---
title: Ställa in lager | Microsoft Docs
description: Beskriver hur du ställer in dina lagerprocesser, inklusive överföringsflöden och lagerställen som t.ex. distributionslager.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f5b4e07f128551e978dffb2dedeb3e0257eea1ea
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024568"
---
# <a name="setting-up-inventory"></a><span data-ttu-id="8e66f-103">Ställa in lager</span><span class="sxs-lookup"><span data-stu-id="8e66f-103">Setting Up Inventory</span></span>
<span data-ttu-id="8e66f-104">Innan du kan administrera aktiviteter för lager och lagerkostnader måste du först ställa in de regler och värden som definierar företagets lagerpolicyer.</span><span class="sxs-lookup"><span data-stu-id="8e66f-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="8e66f-105">Du kan förbättra kundservicen och optimera din leverantörskedja genom att fördela ditt lager på olika adresser.</span><span class="sxs-lookup"><span data-stu-id="8e66f-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="8e66f-106">Du kan sedan köpa, lagra eller sälja artiklar på olika lägerställen och överföra lager mellan dessa.</span><span class="sxs-lookup"><span data-stu-id="8e66f-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="8e66f-107">När du har skapat ett lager kan du administrera olika lagerprocesser relaterade till artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="8e66f-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="8e66f-108">Mer information finns i [Hantera lager](inventory-manage-inventory.md) och [Lagerstyrning](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="8e66f-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="8e66f-109">Till</span><span class="sxs-lookup"><span data-stu-id="8e66f-109">To</span></span> | <span data-ttu-id="8e66f-110">Gå till</span><span class="sxs-lookup"><span data-stu-id="8e66f-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="8e66f-111">Definiera dina allmänna lagerinställningar, till exempel nummerserier och hur du använder lägerställen.</span><span class="sxs-lookup"><span data-stu-id="8e66f-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="8e66f-112">Ställa in allmän lagerinformation</span><span class="sxs-lookup"><span data-stu-id="8e66f-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="8e66f-113">Konfigurera en effektiv distributionsmodell med en kombination av olika lagerställen och ansvarsenheter som tilldelas affärspartners eller anställda.</span><span class="sxs-lookup"><span data-stu-id="8e66f-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="8e66f-114">Arbeta med ansvarsenheter</span><span class="sxs-lookup"><span data-stu-id="8e66f-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="8e66f-115">Organisera ditt lager på flera lägerställen, inklusive överföringsflöden.</span><span class="sxs-lookup"><span data-stu-id="8e66f-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="8e66f-116">Konfigurera platser</span><span class="sxs-lookup"><span data-stu-id="8e66f-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="8e66f-117">Skapa artikelkort för de lager, ej i lager eller serviceartiklar som du handlar med.</span><span class="sxs-lookup"><span data-stu-id="8e66f-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="8e66f-118">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="8e66f-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="8e66f-119">Använd funktionen **kopiera artikel** om du snabbt vill skapa ett nytt artikelkort som bygger på ett befintligt artikelkort.</span><span class="sxs-lookup"><span data-stu-id="8e66f-119">Use the **Copy Item** function to quickly create a new item card based on an existing one.</span></span>|[<span data-ttu-id="8e66f-120">Kopiera befintliga artiklar till Skapa nya artiklar</span><span class="sxs-lookup"><span data-stu-id="8e66f-120">Copy Existing Items to Create New Items</span></span>](inventory-how-copy-items.md)|
|<span data-ttu-id="8e66f-121">Lär dig hur dy fyller i fältet **typ** på artikelkorten enligt affärssyftet.</span><span class="sxs-lookup"><span data-stu-id="8e66f-121">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="8e66f-122">Om artikeltyper</span><span class="sxs-lookup"><span data-stu-id="8e66f-122">About Item Types</span></span>](inventory-about-item-types.md)|
|<span data-ttu-id="8e66f-123">Ange flera måttenheter för en artikel som kan användas som alternativa enheter till exempel för försäljning, inköp eller produkttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="8e66f-123">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="8e66f-124">Ställa in måttenheter för artikel</span><span class="sxs-lookup"><span data-stu-id="8e66f-124">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="8e66f-125">Som ett tillägg till artikelkort kan du registrera artikelinformation i ett visst lagerställe eller en viss variant.</span><span class="sxs-lookup"><span data-stu-id="8e66f-125">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="8e66f-126">Ställa in lagerställeenheter</span><span class="sxs-lookup"><span data-stu-id="8e66f-126">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="8e66f-127">Tilldela objekt till kategorier och ge dem attribut som hjälper dig och kunderna att hitta objekt.</span><span class="sxs-lookup"><span data-stu-id="8e66f-127">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="8e66f-128">Kategorisera artiklar</span><span class="sxs-lookup"><span data-stu-id="8e66f-128">Categorize Items</span></span>](inventory-how-categorize-items.md) |
|<span data-ttu-id="8e66f-129">Importera flera artikelbilder samtidigt från en zip-fil där filer namnges enligt artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="8e66f-129">Import multiple item pictures in one go from a zip file where the files are named according to item numbers.</span></span>|[<span data-ttu-id="8e66f-130">Importera flera artikelbilder</span><span class="sxs-lookup"><span data-stu-id="8e66f-130">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)|
|<span data-ttu-id="8e66f-131">Ange standardrapporter som ska användas för olika dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="8e66f-131">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="8e66f-132">Rapportval i Business Central</span><span class="sxs-lookup"><span data-stu-id="8e66f-132">Report Selection in Business Central</span></span>](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="8e66f-133">Se Relaterad utbildning på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="8e66f-133">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="8e66f-134">Se även</span><span class="sxs-lookup"><span data-stu-id="8e66f-134">See Also</span></span>

[<span data-ttu-id="8e66f-135">Hantera lager</span><span class="sxs-lookup"><span data-stu-id="8e66f-135">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="8e66f-136">Hantera inköp</span><span class="sxs-lookup"><span data-stu-id="8e66f-136">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8e66f-137">[Hantera försäljning](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="8e66f-137">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="8e66f-138">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8e66f-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="8e66f-139">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="8e66f-139">General Business Functionality</span></span>](ui-across-business-areas.md)
