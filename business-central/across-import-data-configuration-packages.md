---
title: "Använda Excel för att importera data till Financials | Microsoft Docs"
description: "Använd standardkonfigurationspaketet för att lägga till kundinformation i Excel och återimportera data till Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4526e8b11c9cbae36c7db58259499fbfa1b0c243
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="ee51c-103">Importera data från äldre redovisningsprogram med ett konfigurationspaket.</span><span class="sxs-lookup"><span data-stu-id="ee51c-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="ee51c-104">Du kan importera huvuddata och vissa transaktionsdata från andra finansiella system baserat på standardkonfigurationspaketet i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ee51c-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ee51c-105">I fönstret **Konfigurationspaket** kan du arbeta med paket för att importera och validera data innan du installerar paketet.</span><span class="sxs-lookup"><span data-stu-id="ee51c-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!NOTE]  
> <span data-ttu-id="ee51c-106">Konfigurationspaket ingår i RapidStart Services för [!INCLUDE[d365fin](includes/d365fin_md.md)], ett omfattande verktyg för att skapa nya lösningar baserade på kundernas affärskrav och konfigurationsdata.</span><span class="sxs-lookup"><span data-stu-id="ee51c-106">Configuration packages are part of RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="ee51c-107">RapidStart Services inkluderar även funktioner för import av äldre data.</span><span class="sxs-lookup"><span data-stu-id="ee51c-107">RapidStart Services also offers functionality for import of legacy data.</span></span> <span data-ttu-id="ee51c-108">Mer information finns i [Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="ee51c-108">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

> [!TIP]  
>   <span data-ttu-id="ee51c-109">Alternativt kan du använda guider för datamigrering för att importera data från QuickBooks eller Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="ee51c-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="ee51c-110">Mer information finns i [QuickBooks datamigrering](ui-extensions-quickbooks-data-migration.md) eller [Dynamics GP datamigrering](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="ee51c-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="ee51c-111">Arbeta med data i excel</span><span class="sxs-lookup"><span data-stu-id="ee51c-111">Working with Data in Excel</span></span>
<span data-ttu-id="ee51c-112">När du exporterar standardkonfigurationspaketet till Excel innehåller den genererade arbetsboken ett kalkylblad för varje register i förpackningen.</span><span class="sxs-lookup"><span data-stu-id="ee51c-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="ee51c-113">För att underlätta dina arbetsuppgifter kan du dra nytta av XML behandlingsverktygen som ingår i Excel.</span><span class="sxs-lookup"><span data-stu-id="ee51c-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="ee51c-114">Du kan även använda inbyggda Excel funktioner för att hjälp med dataformatering och för att ange data i rätt cell.</span><span class="sxs-lookup"><span data-stu-id="ee51c-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="ee51c-115">Lägg till exempel till ett tomt kalkylblad och kopiera befintliga data till det.</span><span class="sxs-lookup"><span data-stu-id="ee51c-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="ee51c-116">Gör en Excel-formel för att koppla data i omformnings kalkylarket mellan fälten i den exporterade kalkylarket och de bakåtkompatibla data för kunden.</span><span class="sxs-lookup"><span data-stu-id="ee51c-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="ee51c-117">När du har mappat alla data kopierar du intervallet av data till tabellkalkylarket.</span><span class="sxs-lookup"><span data-stu-id="ee51c-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="ee51c-118">Ändra inte kolumnerna i kalkylark.</span><span class="sxs-lookup"><span data-stu-id="ee51c-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="ee51c-119">Om de flyttats, ändras eller tas bort, kan kalkylarket inte importeras till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ee51c-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="ee51c-120">Tabellerna i standardkonfigurationspaketet</span><span class="sxs-lookup"><span data-stu-id="ee51c-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="ee51c-121">Standardkonfigurationspaketet stöder följande tabeller:</span><span class="sxs-lookup"><span data-stu-id="ee51c-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="ee51c-122">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="ee51c-122">Payment Terms</span></span>
-   <span data-ttu-id="ee51c-123">Kund prisgrupp</span><span class="sxs-lookup"><span data-stu-id="ee51c-123">Customer Price Group</span></span>
-   <span data-ttu-id="ee51c-124">Utleveransmetod</span><span class="sxs-lookup"><span data-stu-id="ee51c-124">Shipment Method</span></span>
-   <span data-ttu-id="ee51c-125">Säljare/Inköpare</span><span class="sxs-lookup"><span data-stu-id="ee51c-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="ee51c-126">Plats</span><span class="sxs-lookup"><span data-stu-id="ee51c-126">Location</span></span>
-   <span data-ttu-id="ee51c-127">Redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="ee51c-127">GL Account</span></span>
-   <span data-ttu-id="ee51c-128">Kund</span><span class="sxs-lookup"><span data-stu-id="ee51c-128">Customer</span></span>
-   <span data-ttu-id="ee51c-129">Leverantör</span><span class="sxs-lookup"><span data-stu-id="ee51c-129">Vendor</span></span>
-   <span data-ttu-id="ee51c-130">Artikel</span><span class="sxs-lookup"><span data-stu-id="ee51c-130">Item</span></span>
-   <span data-ttu-id="ee51c-131">Försäljningshuvud</span><span class="sxs-lookup"><span data-stu-id="ee51c-131">Sales Header</span></span>
-   <span data-ttu-id="ee51c-132">Försäljningsrad</span><span class="sxs-lookup"><span data-stu-id="ee51c-132">Sales Line</span></span>
-   <span data-ttu-id="ee51c-133">Inköpshuvud</span><span class="sxs-lookup"><span data-stu-id="ee51c-133">Purchase Header</span></span>
-   <span data-ttu-id="ee51c-134">Inköpsrad</span><span class="sxs-lookup"><span data-stu-id="ee51c-134">Purchase Line</span></span>
-   <span data-ttu-id="ee51c-135">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="ee51c-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="ee51c-136">Artikeljournalrad</span><span class="sxs-lookup"><span data-stu-id="ee51c-136">Item Journal Line</span></span>
-   <span data-ttu-id="ee51c-137">Kundbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="ee51c-137">Customer Posting Group</span></span>
-   <span data-ttu-id="ee51c-138">Leverantörsbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="ee51c-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="ee51c-139">Lagerbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="ee51c-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="ee51c-140">Måttenhet</span><span class="sxs-lookup"><span data-stu-id="ee51c-140">Unit of Measure</span></span>
-   <span data-ttu-id="ee51c-141">Gen. rörelsebokföringsmall</span><span class="sxs-lookup"><span data-stu-id="ee51c-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="ee51c-142">Produktbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="ee51c-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="ee51c-143">Bokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="ee51c-143">General Posting Setup</span></span>
-   <span data-ttu-id="ee51c-144">Distrikt</span><span class="sxs-lookup"><span data-stu-id="ee51c-144">Territory</span></span>
-   <span data-ttu-id="ee51c-145">Artikelkategori</span><span class="sxs-lookup"><span data-stu-id="ee51c-145">Item Category</span></span>
-   <span data-ttu-id="ee51c-146">Förs.pris</span><span class="sxs-lookup"><span data-stu-id="ee51c-146">Sales Price</span></span>
-   <span data-ttu-id="ee51c-147">Inköpspris</span><span class="sxs-lookup"><span data-stu-id="ee51c-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="ee51c-148">Importera kunddata</span><span class="sxs-lookup"><span data-stu-id="ee51c-148">Importing Customer Data</span></span>
<span data-ttu-id="ee51c-149">När kunddatan har registrerats i datamigreringsfilerna i Excel importerar du data till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ee51c-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ee51c-150">I fönstret **konfigurationspaket** kan du importera data från Excel-filen och du kan kontrollera att data är konsekventa med [!INCLUDE[d365fin](includes/d365fin_md.md)] innan du installerar paketet.</span><span class="sxs-lookup"><span data-stu-id="ee51c-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee51c-151">Se även</span><span class="sxs-lookup"><span data-stu-id="ee51c-151">See Also</span></span>
[<span data-ttu-id="ee51c-152">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="ee51c-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="ee51c-153">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="ee51c-153">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="ee51c-154">QuickBooks datamigrering</span><span class="sxs-lookup"><span data-stu-id="ee51c-154">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="ee51c-155">Dynamics GP Datamigrering</span><span class="sxs-lookup"><span data-stu-id="ee51c-155">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

