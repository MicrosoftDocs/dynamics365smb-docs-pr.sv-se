---
title: "Använda tillägget QuickBooks-migrering | Microsoft Docs"
description: "Beskriver hur du använder tillägget för att importera kunder, leverantörer, artiklar och konton från QuickBooks Desktop till Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: fdda803b7cc2f93ae4d7353be28282dc60d904d8
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-business-edition"></a><span data-ttu-id="dfcf9-103">Tillägget QuickBooks datamigrering för Dynamics 365 Business edition</span><span class="sxs-lookup"><span data-stu-id="dfcf9-103">The QuickBooks Data Migration Extension for Dynamics 365 Business edition</span></span>
<span data-ttu-id="dfcf9-104">Detta tillägg gör det enkelt att migrera kunder, leverantörer, artiklar och konton från QuickBooks till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="dfcf9-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="dfcf9-105">Om ditt företag använder QuickBooks i dag, kan du exportera nödvändig information och sedan öppna guiden för assisterad installation för att överföra data till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="dfcf9-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="dfcf9-106">Mer information finns i [Importera företagsdata från ett annat finanssystem](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="dfcf9-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="dfcf9-107">Exportera data från QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="dfcf9-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="dfcf9-108">Du måste ha exporterat en del eller alla av dina befintliga kunder, leverantörer, lagerartiklar och konton till en Intuit Interchange Format-fil (IIF ).</span><span class="sxs-lookup"><span data-stu-id="dfcf9-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="dfcf9-109">Tillägget QuickBooks datamigrering innehåller en standardmappning avQuickBooks data så att du kan använda dina befintliga data för att testa det nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företaget.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="dfcf9-110">Standardmappningen ska vara tillräcklig i de flesta fall, men du kan ändra mappningen i guiden för assisterad installation.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="dfcf9-111">I QuickBooks innehåller arkiv-menyn verktyg till exportlistor.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="dfcf9-112">För [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du exportera följande listor:</span><span class="sxs-lookup"><span data-stu-id="dfcf9-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="dfcf9-113">Kundlista</span><span class="sxs-lookup"><span data-stu-id="dfcf9-113">Customer List</span></span>  
* <span data-ttu-id="dfcf9-114">Leverantörslista</span><span class="sxs-lookup"><span data-stu-id="dfcf9-114">Vendor List</span></span>  
* <span data-ttu-id="dfcf9-115">Artikellista</span><span class="sxs-lookup"><span data-stu-id="dfcf9-115">Item List</span></span>  
* <span data-ttu-id="dfcf9-116">Redov.kontolista</span><span class="sxs-lookup"><span data-stu-id="dfcf9-116">Account List</span></span>  

<span data-ttu-id="dfcf9-117">Exporterade data sparas som en IIF-fil som du sedan kan överföra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="dfcf9-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="dfcf9-118">Hitta tillägget QuickBooks datamigrering</span><span class="sxs-lookup"><span data-stu-id="dfcf9-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="dfcf9-119">Tillägget QuickBooks datamigrering är installerat och klart som en integrerad del av guiden för assisterad konfiguration av datamigrering.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="dfcf9-120">Om du är redo att sätta igång nu, och har exporterat data från QuickBooks, väljer du ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), anger **Assisterad konfiguration** och väljer sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="dfcf9-121">Välj **Migrera affärsdata** och följ sedan anvisningarna i guiden.</span><span class="sxs-lookup"><span data-stu-id="dfcf9-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dfcf9-122">Se även</span><span class="sxs-lookup"><span data-stu-id="dfcf9-122">See Also</span></span>
[<span data-ttu-id="dfcf9-123">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="dfcf9-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="dfcf9-124">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="dfcf9-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

