---
title: "Använda tillägget QuickBooks-migrering | Microsoft Docs"
description: "Beskriver hur du använder tillägget för att importera kunder, leverantörer, artiklar och konton från QuickBooks skrivbord till Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 37d90316ea0be5489fb5abe33645de3fe0d3cf90
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="f2a96-103">Tillägget QuickBooks datamigrering för Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="f2a96-103">The QuickBooks Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="f2a96-104">Detta tillägg gör det enkelt att migrera kunder, leverantörer, artiklar och konton från QuickBooks till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f2a96-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f2a96-105">Om ditt företag använder QuickBooks i dag, kan du exportera nödvändig information och sedan öppna guiden för assisterad installation för att överföra data till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f2a96-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="f2a96-106">Mer information finns i [Importera företagsdata från ett annat finanssystem](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="f2a96-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks"></a><span data-ttu-id="f2a96-107">Exportera data från QuickBooks</span><span class="sxs-lookup"><span data-stu-id="f2a96-107">Exporting Data from QuickBooks</span></span>
<span data-ttu-id="f2a96-108">Du måste ha exporterat en del eller alla av dina befintliga kunder, leverantörer, lagerartiklar och konton till en Intuit Interchange Format-fil (IIF ).</span><span class="sxs-lookup"><span data-stu-id="f2a96-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="f2a96-109">Tillägget QuickBooks datamigrering innehåller en standardmappning avQuickBooks data så att du kan använda dina befintliga data för att testa det nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företaget.</span><span class="sxs-lookup"><span data-stu-id="f2a96-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="f2a96-110">Standardmappningen ska vara tillräcklig i de flesta fall, men du kan ändra mappningen i guiden för assisterad installation.</span><span class="sxs-lookup"><span data-stu-id="f2a96-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="f2a96-111">I QuickBooks innehåller arkiv-menyn verktyg till exportlistor.</span><span class="sxs-lookup"><span data-stu-id="f2a96-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="f2a96-112">För [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du exportera följande listor:</span><span class="sxs-lookup"><span data-stu-id="f2a96-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="f2a96-113">Kundlista</span><span class="sxs-lookup"><span data-stu-id="f2a96-113">Customer List</span></span>  
* <span data-ttu-id="f2a96-114">Leverantörslista</span><span class="sxs-lookup"><span data-stu-id="f2a96-114">Vendor List</span></span>  
* <span data-ttu-id="f2a96-115">Artikellista</span><span class="sxs-lookup"><span data-stu-id="f2a96-115">Item List</span></span>  
* <span data-ttu-id="f2a96-116">Redov.kontolista</span><span class="sxs-lookup"><span data-stu-id="f2a96-116">Account List</span></span>  

<span data-ttu-id="f2a96-117">Exporterade data sparas som en IIF-fil som du sedan kan överföra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f2a96-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="f2a96-118">Se även</span><span class="sxs-lookup"><span data-stu-id="f2a96-118">See Also</span></span>
[<span data-ttu-id="f2a96-119">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="f2a96-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="f2a96-120">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="f2a96-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

