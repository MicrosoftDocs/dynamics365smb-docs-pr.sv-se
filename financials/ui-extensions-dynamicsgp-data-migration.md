---
title: "Migrera Data från Dynamics GP med tillägget Data Migration | Microsoft Docs"
description: "Använda tillägget Dynamics GP-datamigrering för att flytta över kunder, leverantörer, lagerartiklar och konton från Dynamics GP till Finance and Operations, Business edition."
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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: bfd3ca3e28b6eb3efa2a16cc131b508db6bd1590
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="50018-103">Tillägget Dynamics GP-datamigrering för Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="50018-103">The Dynamics GP Data Migration Extension for Finance and Operations, Business edition</span></span> 
<span data-ttu-id="50018-104">Detta tillägg gör det enkelt att migrera kunder, leverantörer, lagerartiklar och konton från Dynamics GP till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50018-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="50018-105">Om ditt företag använder Dynamics GP i dag, kan du exportera nödvändiga huvudposter och sedan öppna guiden för assisterad konfiguration för att överföra data till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50018-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="50018-106">Mer information finns i [Migrera företagsdata från ett annat finanssystem](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="50018-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="50018-107">Exportera data från Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="50018-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="50018-108">Du måste ha exporterat några av dina befintliga kunder, leverantörer, lagerartiklar och konton till en fill med hjälp av funktionen dataexport i Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="50018-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="50018-109">För [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du exportera följande typer av data:</span><span class="sxs-lookup"><span data-stu-id="50018-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="50018-110">Konto</span><span class="sxs-lookup"><span data-stu-id="50018-110">Account</span></span>  
* <span data-ttu-id="50018-111">Kund</span><span class="sxs-lookup"><span data-stu-id="50018-111">Customer</span></span>  
* <span data-ttu-id="50018-112">Artikel</span><span class="sxs-lookup"><span data-stu-id="50018-112">Item</span></span>  
* <span data-ttu-id="50018-113">Leverantör</span><span class="sxs-lookup"><span data-stu-id="50018-113">Vendor</span></span>  

<span data-ttu-id="50018-114">Tillägget Datamigrering för Dynamics GP mappas automatiskt den exporterade informationen så att dina data är snabbt tillgängliga i ditt nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företag.</span><span class="sxs-lookup"><span data-stu-id="50018-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="50018-115">Under processen skapas stödjande installationsinformation, som till exempel bokföringsmallar.</span><span class="sxs-lookup"><span data-stu-id="50018-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="50018-116">Lagerartiklar kommer att tas med i systemet med FIFO som kostadsvärderingsmetod.</span><span class="sxs-lookup"><span data-stu-id="50018-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="50018-117">Konton ska ställas in som ett segment för huvudkontot från Dynamics GP med dimensioner, eftersom [!INCLUDE[d365fin](includes/d365fin_long_md.md)] inte har kontosegment.</span><span class="sxs-lookup"><span data-stu-id="50018-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="50018-118">Se även</span><span class="sxs-lookup"><span data-stu-id="50018-118">See Also</span></span>
[<span data-ttu-id="50018-119">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="50018-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="50018-120">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="50018-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

