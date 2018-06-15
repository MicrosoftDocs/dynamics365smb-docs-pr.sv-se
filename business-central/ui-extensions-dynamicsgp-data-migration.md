---
title: "Migrera Data från Dynamics GP med tillägget Data Migration | Microsoft Docs"
description: "Använd filnamnstillägget Dynamics GP-datamigrering för att flytta över kunder, leverantörer, lagerartiklar och konton från Dynamics GP till Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 3761bdb0d6b9a51ed309ac4189ff263de76f4679
ms.contentlocale: sv-se
ms.lasthandoff: 05/17/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-business-central"></a><span data-ttu-id="18f23-103">Tillägget Dynamics GP-datamigrering för Business Central</span><span class="sxs-lookup"><span data-stu-id="18f23-103">The Dynamics GP Data Migration Extension for Business Central</span></span> 
<span data-ttu-id="18f23-104">Detta tillägg gör det enkelt att migrera kunder, leverantörer, lagerartiklar och konton från Dynamics GP till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="18f23-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="18f23-105">Om ditt företag använder Dynamics GP i dag, kan du exportera nödvändiga huvudposter och sedan öppna guiden för assisterad konfiguration för att överföra data till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="18f23-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="18f23-106">Mer information finns i [Importera företagsdata från ett annat finanssystem](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="18f23-106">For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="18f23-107">Exportera data från Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="18f23-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="18f23-108">Du måste ha exporterat några av dina befintliga kunder, leverantörer, lagerartiklar och konton till en fill med hjälp av funktionen dataexport i Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="18f23-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="18f23-109">För [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du exportera följande typer av data:</span><span class="sxs-lookup"><span data-stu-id="18f23-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="18f23-110">Konto</span><span class="sxs-lookup"><span data-stu-id="18f23-110">Account</span></span>  
* <span data-ttu-id="18f23-111">Kund</span><span class="sxs-lookup"><span data-stu-id="18f23-111">Customer</span></span>  
* <span data-ttu-id="18f23-112">Artikel</span><span class="sxs-lookup"><span data-stu-id="18f23-112">Item</span></span>  
* <span data-ttu-id="18f23-113">Leverantör</span><span class="sxs-lookup"><span data-stu-id="18f23-113">Vendor</span></span>  

<span data-ttu-id="18f23-114">Tillägget Datamigrering för Dynamics GP mappas automatiskt den exporterade informationen så att dina data är snabbt tillgängliga i ditt nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företag.</span><span class="sxs-lookup"><span data-stu-id="18f23-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="18f23-115">Under processen skapas stödjande installationsinformation, som till exempel bokföringsmallar.</span><span class="sxs-lookup"><span data-stu-id="18f23-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="18f23-116">Lagerartiklar kommer att tas med i systemet med FIFO som kostadsvärderingsmetod.</span><span class="sxs-lookup"><span data-stu-id="18f23-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="18f23-117">Konton ska ställas in som ett segment för huvudkontot från Dynamics GP med dimensioner, eftersom [!INCLUDE[d365fin](includes/d365fin_long_md.md)] inte har kontosegment.</span><span class="sxs-lookup"><span data-stu-id="18f23-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="18f23-118">Se även</span><span class="sxs-lookup"><span data-stu-id="18f23-118">See Also</span></span>
[<span data-ttu-id="18f23-119">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="18f23-119">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="18f23-120">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="18f23-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

