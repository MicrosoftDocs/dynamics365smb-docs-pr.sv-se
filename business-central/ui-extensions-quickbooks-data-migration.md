---
title: "Använda tillägget QuickBooks-migrering | Microsoft Docs"
description: "Beskriver hur du använder tillägget för att importera kunder, leverantörer, artiklar och konton från QuickBooks Desktop till Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 583f6947acd3778710f0889736439322d9179ce6
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="the-quickbooks-data-migration-extension"></a><span data-ttu-id="27255-103">Tillägget QuickBooks datamigrering</span><span class="sxs-lookup"><span data-stu-id="27255-103">The QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="27255-104">Detta tillägg gör det enkelt att migrera kunder, leverantörer, artiklar och konton från QuickBooks till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="27255-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="27255-105">Om ditt företag använder QuickBooks i dag, kan du exportera nödvändig information och sedan öppna guiden för assisterad konfiguration för att överföra data till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="27255-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="27255-106">Mer information finns i [Importera företagsdata från ett annat finanssystem](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="27255-106">For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="27255-107">Exportera data från QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="27255-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="27255-108">Du måste ha exporterat en del eller alla av dina befintliga kunder, leverantörer, lagerartiklar och konton till en Intuit Interchange Format-fil (IIF ).</span><span class="sxs-lookup"><span data-stu-id="27255-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="27255-109">Tillägget QuickBooks datamigrering innehåller en standardmappning avQuickBooks data så att du kan använda dina befintliga data för att testa det nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företaget.</span><span class="sxs-lookup"><span data-stu-id="27255-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="27255-110">Standardmappningen ska vara tillräcklig i de flesta fall, men du kan ändra mappningen i guiden för assisterad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="27255-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="27255-111">I QuickBooks innehåller arkiv-menyn verktyg till exportlistor.</span><span class="sxs-lookup"><span data-stu-id="27255-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="27255-112">För [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du exportera följande listor:</span><span class="sxs-lookup"><span data-stu-id="27255-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="27255-113">Kundlista</span><span class="sxs-lookup"><span data-stu-id="27255-113">Customer List</span></span>  
* <span data-ttu-id="27255-114">Leverantörslista</span><span class="sxs-lookup"><span data-stu-id="27255-114">Vendor List</span></span>  
* <span data-ttu-id="27255-115">Artikellista</span><span class="sxs-lookup"><span data-stu-id="27255-115">Item List</span></span>  
* <span data-ttu-id="27255-116">Redov.kontolista</span><span class="sxs-lookup"><span data-stu-id="27255-116">Account List</span></span>  

<span data-ttu-id="27255-117">Exporterade data sparas som en IIF-fil som du sedan kan överföra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="27255-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="27255-118">Hitta tillägget QuickBooks datamigrering</span><span class="sxs-lookup"><span data-stu-id="27255-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="27255-119">Tillägget QuickBooks datamigrering är installerat och klart som en integrerad del av guiden för assisterad konfiguration av datamigrering.</span><span class="sxs-lookup"><span data-stu-id="27255-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="27255-120">Om du är redo att börja nu och har exporterat dina data från QuickBooks, välj ikonen![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Assisterad konfiguration** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="27255-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="27255-121">Välj **Migrera affärsdata** och följ sedan anvisningarna i guiden.</span><span class="sxs-lookup"><span data-stu-id="27255-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="27255-122">Se även</span><span class="sxs-lookup"><span data-stu-id="27255-122">See Also</span></span>
[<span data-ttu-id="27255-123">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="27255-123">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="27255-124">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="27255-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

