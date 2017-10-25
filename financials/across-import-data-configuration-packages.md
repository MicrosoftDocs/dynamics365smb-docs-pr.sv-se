---
title: "Använda Excel för att importera data till Financials | Microsoft Docs"
description: "Använda standardkonfigurationspaketet för att lägga till kundinformation i Excel och importera data till Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2a38dc36cb9ff609c5582acd489841b20013d4bc
ms.openlocfilehash: 8cf36afea60b089afac8f1c27d126cd19b88ce94
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="8366d-103">Importera data från äldre redovisningsprogrammet med ett konfigurationspaket.</span><span class="sxs-lookup"><span data-stu-id="8366d-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="8366d-104">Du kan importera huvuddata och vissa transaktionsdata från andra finansiella system baserat på standardkonfigurationspaketet i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8366d-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8366d-105">I fönstret **konfigurationspaket** kan du arbeta med paket för att importera och validera data innan du installerar paketet.</span><span class="sxs-lookup"><span data-stu-id="8366d-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

<span data-ttu-id="8366d-106">Om du känner till RapidStart-tjänster för Microsoft Dynamics, känner du också till konfigurationpaket.</span><span class="sxs-lookup"><span data-stu-id="8366d-106">If you are familiar with RapidStart Services for Microsoft Dynamics, you are also familiar with configuration packages.</span></span> <span data-ttu-id="8366d-107">Standardkonfigurationspaketet stöder de vanligaste typerna av data som du vill importera från äldre system.</span><span class="sxs-lookup"><span data-stu-id="8366d-107">The default configuration package supports the most common types of data that you want to import from a legacy system.</span></span> <span data-ttu-id="8366d-108">I Excel kan du sedan lägga till data från äldre system och konfigurera dem enligt affärslogik på [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8366d-108">In Excel, you can then add the data from the legacy system and set it up according to the business logic of the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

> [!TIP]  
>   <span data-ttu-id="8366d-109">Alternativ kan du använda guider för datamigrering för att importera data från QuickBooks eller Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="8366d-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="8366d-110">Mer information finns i [QuickBooks datamigrering](ui-extensions-quickbooks-data-migration.md) eller [Dynamics GP datamigrering ](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="8366d-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="8366d-111">Arbeta med data i excel</span><span class="sxs-lookup"><span data-stu-id="8366d-111">Working with Data in Excel</span></span>
<span data-ttu-id="8366d-112">När du exporterar standardkonfigurationspaketet till Excel innehåller den genererade arbetsboken ett kalkylblad för varje register i förpackningen.</span><span class="sxs-lookup"><span data-stu-id="8366d-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="8366d-113">För att underlätta dina arbetsuppgifter kan du dra nytta av XML behandlingsverktygen som ingår i Excel.</span><span class="sxs-lookup"><span data-stu-id="8366d-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="8366d-114">Du kan även använda inbyggda Excel funktioner för att hjälp med dataformatering och för att ange data i rätt cell.</span><span class="sxs-lookup"><span data-stu-id="8366d-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="8366d-115">Lägg till exempel till ett tomt kalkylblad och kopiera befintliga data till det.</span><span class="sxs-lookup"><span data-stu-id="8366d-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="8366d-116">Gör en Excel-formel för att koppla data i omformnings förslaget mellan fälten i den exporterade förslaget och de bakåtkompatibla data för kunden.</span><span class="sxs-lookup"><span data-stu-id="8366d-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="8366d-117">När du har mappat alla data kopierar du intervallet av data till tabellförslaget.</span><span class="sxs-lookup"><span data-stu-id="8366d-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="8366d-118">Ändra inte kolumnerna i förslag.</span><span class="sxs-lookup"><span data-stu-id="8366d-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="8366d-119">Om de flyttats, ändras eller tas bort, kan förslaget inte importeras till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8366d-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="8366d-120">Tabellerna i standardkonfigurationpaketet</span><span class="sxs-lookup"><span data-stu-id="8366d-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="8366d-121">Standardkonfigurationspaketet stöder följande tabeller:</span><span class="sxs-lookup"><span data-stu-id="8366d-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="8366d-122">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="8366d-122">Payment Terms</span></span>
-   <span data-ttu-id="8366d-123">Kund prisgrupp</span><span class="sxs-lookup"><span data-stu-id="8366d-123">Customer Price Group</span></span>
-   <span data-ttu-id="8366d-124">Utleveransvillkor</span><span class="sxs-lookup"><span data-stu-id="8366d-124">Shipment Method</span></span>
-   <span data-ttu-id="8366d-125">Säljare/Inköpare</span><span class="sxs-lookup"><span data-stu-id="8366d-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="8366d-126">Plats</span><span class="sxs-lookup"><span data-stu-id="8366d-126">Location</span></span>
-   <span data-ttu-id="8366d-127">Redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="8366d-127">GL Account</span></span>
-   <span data-ttu-id="8366d-128">Kund</span><span class="sxs-lookup"><span data-stu-id="8366d-128">Customer</span></span>
-   <span data-ttu-id="8366d-129">Leverantör</span><span class="sxs-lookup"><span data-stu-id="8366d-129">Vendor</span></span>
-   <span data-ttu-id="8366d-130">Artikel</span><span class="sxs-lookup"><span data-stu-id="8366d-130">Item</span></span>
-   <span data-ttu-id="8366d-131">Försäljningshuvud</span><span class="sxs-lookup"><span data-stu-id="8366d-131">Sales Header</span></span>
-   <span data-ttu-id="8366d-132">Försäljningsrad</span><span class="sxs-lookup"><span data-stu-id="8366d-132">Sales Line</span></span>
-   <span data-ttu-id="8366d-133">Inköpshuvud</span><span class="sxs-lookup"><span data-stu-id="8366d-133">Purchase Header</span></span>
-   <span data-ttu-id="8366d-134">Inköpsrad</span><span class="sxs-lookup"><span data-stu-id="8366d-134">Purchase Line</span></span>
-   <span data-ttu-id="8366d-135">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="8366d-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="8366d-136">Artikeljournalrad</span><span class="sxs-lookup"><span data-stu-id="8366d-136">Item Journal Line</span></span>
-   <span data-ttu-id="8366d-137">Kundbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="8366d-137">Customer Posting Group</span></span>
-   <span data-ttu-id="8366d-138">Leverantörsbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="8366d-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="8366d-139">Lagerbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="8366d-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="8366d-140">Måttenhet</span><span class="sxs-lookup"><span data-stu-id="8366d-140">Unit of Measure</span></span>
-   <span data-ttu-id="8366d-141">Gen. rörelsebokföringsmall</span><span class="sxs-lookup"><span data-stu-id="8366d-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="8366d-142">Produktbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="8366d-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="8366d-143">Bokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="8366d-143">General Posting Setup</span></span>
-   <span data-ttu-id="8366d-144">Distrikt</span><span class="sxs-lookup"><span data-stu-id="8366d-144">Territory</span></span>
-   <span data-ttu-id="8366d-145">Artikelkategori</span><span class="sxs-lookup"><span data-stu-id="8366d-145">Item Category</span></span>
-   <span data-ttu-id="8366d-146">Förs.pris</span><span class="sxs-lookup"><span data-stu-id="8366d-146">Sales Price</span></span>
-   <span data-ttu-id="8366d-147">Inköpspris</span><span class="sxs-lookup"><span data-stu-id="8366d-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="8366d-148">Importera kunddata</span><span class="sxs-lookup"><span data-stu-id="8366d-148">Importing Customer Data</span></span>
<span data-ttu-id="8366d-149">När kunddatan har registrerats i dataflyttningsfilerna i Excel importerar du data till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8366d-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8366d-150">I fönstret **konfigurationspaket** kan du importera data från Excel-filen och du kan kontrollera att data är konsekventa med [!INCLUDE[d365fin](includes/d365fin_md.md)] innan du installerar paketet.</span><span class="sxs-lookup"><span data-stu-id="8366d-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="8366d-151">Se även</span><span class="sxs-lookup"><span data-stu-id="8366d-151">See Also</span></span>
[<span data-ttu-id="8366d-152">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="8366d-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="8366d-153">QuickBooks datamigrering</span><span class="sxs-lookup"><span data-stu-id="8366d-153">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="8366d-154">Dynamics GP Datamigrering</span><span class="sxs-lookup"><span data-stu-id="8366d-154">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

