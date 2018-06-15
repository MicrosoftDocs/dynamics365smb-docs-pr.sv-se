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
ms.date: 05/17/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 379cfd2731bba2df6f5e31d2b8de2d72e2064ebb
ms.contentlocale: sv-se
ms.lasthandoff: 05/17/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a><span data-ttu-id="9610f-103">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="9610f-103">Importing Business Data from Other Finance Systems</span></span>
<span data-ttu-id="9610f-104">När du registrerar dig på [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du välja att skapa ett tomt företag så att du kan överföra din egen information och testa det nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företaget.</span><span class="sxs-lookup"><span data-stu-id="9610f-104">When you sign up for [!INCLUDE[d365fin](includes/d365fin_md.md)], you can choose to create an empty company so that you can upload your own data and to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="9610f-105">Beroende på finanslösningen som används i din verksamhet idag, kan du överföra information om kunder, leverantörer, lager och bankkonton.</span><span class="sxs-lookup"><span data-stu-id="9610f-105">Depending on the finance solution that your business uses today, you can transfer information about customers, vendors, inventory, and bank accounts.</span></span>  

<span data-ttu-id="9610f-106">Från ditt Rollcenter kan du starta en guide för assisterad konfiguration som hjälper dig att överföra affärsdata från en Excel-fil eller andra format.</span><span class="sxs-lookup"><span data-stu-id="9610f-106">From the Role Center, you can start an assisted setup guide that helps you transfer the business data from an Excel file or from other formats.</span></span> <span data-ttu-id="9610f-107">Typen av filer som du kan överföra, beror på tilläggen som är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="9610f-107">The type of files you can upload depends on the extensions that are available.</span></span> <span data-ttu-id="9610f-108">Du kan till exempel migrera data från QuickBooks, eftersom [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett tillägg som ska hantera omvandlingen från QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="9610f-108">For example, you can migrate data from QuickBooks because [!INCLUDE[d365fin](includes/d365fin_md.md)] includes an extension that handles the conversion from QuickBooks.</span></span> <span data-ttu-id="9610f-109">Om du vill migrera data från andra finanslösningar, måste du antingen kontrollera om det finns ett tillägg för den lösningen eller importera från Excel.</span><span class="sxs-lookup"><span data-stu-id="9610f-109">If you want to migrate data from other finance solutions, you must either check if an extension is available for that solution or import from Excel.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9610f-110"> inkluderar mallar förkonton, kunder, leverantörer och lagerartiklar som du kan välja att koppla, när du importerar dina data.</span><span class="sxs-lookup"><span data-stu-id="9610f-110"> includes templates for accounts, customers, vendors, and inventory items that you can choose to apply when you import your data.</span></span>

<span data-ttu-id="9610f-111">Du kan importera huvuddata och vissa transaktionsdata från andra finansiella system baserat på standardkonfigurationspaketet i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9610f-111">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="9610f-112">I fönstret **konfigurationspaket** kan du arbeta med paket för att importera och validera data innan du installerar paketet.</span><span class="sxs-lookup"><span data-stu-id="9610f-112">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!TIP]  
> <span data-ttu-id="9610f-113">Alternativt kan du använda guider för datamigrering för att importera data från QuickBooks eller Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="9610f-113">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="9610f-114">Mer information finns i [QuickBooks datamigrering](ui-extensions-quickbooks-data-migration.md) eller [Dynamics GP datamigrering](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="9610f-114">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="9610f-115">För större implementeringar kan du använda RapidStart Services för [!INCLUDE[d365fin](includes/d365fin_md.md)], som är ett omfattande verktyg för att skapa nya lösningar baserade på kundernas affärskrav och konfigurationsdata.</span><span class="sxs-lookup"><span data-stu-id="9610f-115">For larger implementation work, you can use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], which is an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="9610f-116">RapidStart Services inkluderar även funktioner för import av affärsdata.</span><span class="sxs-lookup"><span data-stu-id="9610f-116">RapidStart Services also offers functionality for import of business data.</span></span> <span data-ttu-id="9610f-117">Mer information finns i [Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="9610f-117">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

## <a name="importing-data-from-configuration-packages"></a><span data-ttu-id="9610f-118">Importera data från ett konfigurationspaket</span><span class="sxs-lookup"><span data-stu-id="9610f-118">Importing Data from Configuration Packages</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9610f-119"> innehåller ett konfigurationspaket som du kan exportera till Excel och ange dina data där.</span><span class="sxs-lookup"><span data-stu-id="9610f-119"> includes a configuration package that you can export to Excel and set up your data there.</span></span> <span data-ttu-id="9610f-120">Sedan kan du importera datan från Excel igen.</span><span class="sxs-lookup"><span data-stu-id="9610f-120">Then, you can import the data from Excel again.</span></span> <span data-ttu-id="9610f-121">Paketet består av 27 register, inklusive huvuddata som t.ex. kunder, leverantörer, artiklar och konton, andra grundläggande inställningstabeller, som till exempel leveransmetoder och transaktionstabeller som t.ex. rubrik och rader.</span><span class="sxs-lookup"><span data-stu-id="9610f-121">The package consists of 27 tables, including master data such as customers, vendors, items, and accounts, other basic setup tables such as shipping methods, and transactions tables such as sales header and lines.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="9610f-122">Att arbeta med konfigurationspaket innebär avancerade funktioner och vi rekommenderar att du kontaktar din administratör.</span><span class="sxs-lookup"><span data-stu-id="9610f-122">Working with configuration packages is advanced functionality, and we recommend that you contact your administrator.</span></span> <span data-ttu-id="9610f-123">Mer information finns i [Importera data från äldre redovisningsprogram med ett konfigurationspaket](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="9610f-123">For more information, see [Importing Data from Legacy Accounting Software using a Configuration Package](across-import-data-configuration-packages.md).</span></span>

## <a name="working-with-data-in-excel"></a><span data-ttu-id="9610f-124">Arbeta med data i excel</span><span class="sxs-lookup"><span data-stu-id="9610f-124">Working with Data in Excel</span></span>
<span data-ttu-id="9610f-125">När du exporterar standardkonfigurationspaketet till Excel innehåller den genererade arbetsboken ett kalkylblad för varje register i förpackningen.</span><span class="sxs-lookup"><span data-stu-id="9610f-125">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="9610f-126">För att underlätta dina arbetsuppgifter kan du dra nytta av XML behandlingsverktygen som ingår i Excel.</span><span class="sxs-lookup"><span data-stu-id="9610f-126">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="9610f-127">Du kan även använda inbyggda Excel funktioner för att hjälp med dataformatering och för att ange data i rätt cell.</span><span class="sxs-lookup"><span data-stu-id="9610f-127">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="9610f-128">Lägg till exempel till ett tomt kalkylblad och kopiera befintliga data till det.</span><span class="sxs-lookup"><span data-stu-id="9610f-128">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="9610f-129">Gör en Excel-formel för att koppla data i omformnings kalkylarket mellan fälten i den exporterade kalkylarket och de bakåtkompatibla data för kunden.</span><span class="sxs-lookup"><span data-stu-id="9610f-129">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="9610f-130">När du har mappat alla data kopierar du intervallet av data till tabellkalkylarket.</span><span class="sxs-lookup"><span data-stu-id="9610f-130">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="9610f-131">Ändra inte kolumnerna i kalkylark.</span><span class="sxs-lookup"><span data-stu-id="9610f-131">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="9610f-132">Om de flyttats, ändras eller tas bort, kan kalkylarket inte importeras till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9610f-132">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="9610f-133">Tabellerna i standardkonfigurationspaketet</span><span class="sxs-lookup"><span data-stu-id="9610f-133">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="9610f-134">Standardkonfigurationspaketet stöder följande tabeller:</span><span class="sxs-lookup"><span data-stu-id="9610f-134">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="9610f-135">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="9610f-135">Payment Terms</span></span>
-   <span data-ttu-id="9610f-136">Kund prisgrupp</span><span class="sxs-lookup"><span data-stu-id="9610f-136">Customer Price Group</span></span>
-   <span data-ttu-id="9610f-137">Utleveransmetod</span><span class="sxs-lookup"><span data-stu-id="9610f-137">Shipment Method</span></span>
-   <span data-ttu-id="9610f-138">Säljare/Inköpare</span><span class="sxs-lookup"><span data-stu-id="9610f-138">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="9610f-139">Plats</span><span class="sxs-lookup"><span data-stu-id="9610f-139">Location</span></span>
-   <span data-ttu-id="9610f-140">Redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="9610f-140">GL Account</span></span>
-   <span data-ttu-id="9610f-141">Kund</span><span class="sxs-lookup"><span data-stu-id="9610f-141">Customer</span></span>
-   <span data-ttu-id="9610f-142">Leverantör</span><span class="sxs-lookup"><span data-stu-id="9610f-142">Vendor</span></span>
-   <span data-ttu-id="9610f-143">Artikel</span><span class="sxs-lookup"><span data-stu-id="9610f-143">Item</span></span>
-   <span data-ttu-id="9610f-144">Försäljningshuvud</span><span class="sxs-lookup"><span data-stu-id="9610f-144">Sales Header</span></span>
-   <span data-ttu-id="9610f-145">Försäljningsrad</span><span class="sxs-lookup"><span data-stu-id="9610f-145">Sales Line</span></span>
-   <span data-ttu-id="9610f-146">Inköpshuvud</span><span class="sxs-lookup"><span data-stu-id="9610f-146">Purchase Header</span></span>
-   <span data-ttu-id="9610f-147">Inköpsrad</span><span class="sxs-lookup"><span data-stu-id="9610f-147">Purchase Line</span></span>
-   <span data-ttu-id="9610f-148">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="9610f-148">Gen. Journal Line</span></span>
-   <span data-ttu-id="9610f-149">Artikeljournalrad</span><span class="sxs-lookup"><span data-stu-id="9610f-149">Item Journal Line</span></span>
-   <span data-ttu-id="9610f-150">Kundbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="9610f-150">Customer Posting Group</span></span>
-   <span data-ttu-id="9610f-151">Leverantörsbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="9610f-151">Vendor Posting Group</span></span>
-   <span data-ttu-id="9610f-152">Lagerbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="9610f-152">Inventory Posting Group</span></span>
-   <span data-ttu-id="9610f-153">Måttenhet</span><span class="sxs-lookup"><span data-stu-id="9610f-153">Unit of Measure</span></span>
-   <span data-ttu-id="9610f-154">Gen. rörelsebokföringsmall</span><span class="sxs-lookup"><span data-stu-id="9610f-154">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="9610f-155">Produktbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="9610f-155">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="9610f-156">Bokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="9610f-156">General Posting Setup</span></span>
-   <span data-ttu-id="9610f-157">Distrikt</span><span class="sxs-lookup"><span data-stu-id="9610f-157">Territory</span></span>
-   <span data-ttu-id="9610f-158">Artikelkategori</span><span class="sxs-lookup"><span data-stu-id="9610f-158">Item Category</span></span>
-   <span data-ttu-id="9610f-159">Förs.pris</span><span class="sxs-lookup"><span data-stu-id="9610f-159">Sales Price</span></span>
-   <span data-ttu-id="9610f-160">Inköpspris</span><span class="sxs-lookup"><span data-stu-id="9610f-160">Purchase Price</span></span>

## <a name="see-also"></a><span data-ttu-id="9610f-161">Se även</span><span class="sxs-lookup"><span data-stu-id="9610f-161">See Also</span></span>
[<span data-ttu-id="9610f-162">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="9610f-162">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="9610f-163">QuickBooks datamigrering</span><span class="sxs-lookup"><span data-stu-id="9610f-163">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="9610f-164">Dynamics GP Datamigrering</span><span class="sxs-lookup"><span data-stu-id="9610f-164">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

