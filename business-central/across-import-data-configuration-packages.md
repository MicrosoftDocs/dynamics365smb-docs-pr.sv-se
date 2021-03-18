---
title: Använda Excel för att importera data till Business Central
description: Använd standardkonfigurationspaketet för att lägga till kundinformation i Excel och återimportera data till Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3885d9e07a6ea417bf2dc7de5881e6d3278ca10
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379254"
---
# <a name="importing-business-data-from-other-finance-systems"></a><span data-ttu-id="1937e-103">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="1937e-103">Importing Business Data from Other Finance Systems</span></span>

<span data-ttu-id="1937e-104">När du registrerar dig på [!INCLUDE[prod_short](includes/prod_short.md)], kan du välja att skapa ett tomt företag så att du kan överföra din egen information och testa det nya [!INCLUDE[prod_short](includes/prod_short.md)]-företaget.</span><span class="sxs-lookup"><span data-stu-id="1937e-104">When you sign up for [!INCLUDE[prod_short](includes/prod_short.md)], you can choose to create an empty company so that you can upload your own data and to test your new [!INCLUDE[prod_short](includes/prod_short.md)] company.</span></span> <span data-ttu-id="1937e-105">Beroende på finanslösningen som används i din verksamhet idag, kan du överföra information om kunder, leverantörer, lager och bankkonton.</span><span class="sxs-lookup"><span data-stu-id="1937e-105">Depending on the finance solution that your business uses today, you can transfer information about customers, vendors, inventory, and bank accounts.</span></span>  

<span data-ttu-id="1937e-106">Från ditt Rollcenter kan du starta en guide för assisterad konfiguration som hjälper dig att överföra affärsdata från en Excel-fil eller andra format.</span><span class="sxs-lookup"><span data-stu-id="1937e-106">From the Role Center, you can start an assisted setup guide that helps you transfer the business data from an Excel file or from other formats.</span></span> <span data-ttu-id="1937e-107">Typen av filer som du kan överföra, beror på tilläggen som är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="1937e-107">The type of files you can upload depends on the extensions that are available.</span></span> <span data-ttu-id="1937e-108">Du kan till exempel migrera data från QuickBooks, eftersom [!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett tillägg som ska hantera omvandlingen från QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="1937e-108">For example, you can migrate data from QuickBooks because [!INCLUDE[prod_short](includes/prod_short.md)] includes an extension that handles the conversion from QuickBooks.</span></span> <span data-ttu-id="1937e-109">Om du vill migrera data från andra finanslösningar, måste du antingen kontrollera om det finns ett tillägg för den lösningen eller importera från Excel.</span><span class="sxs-lookup"><span data-stu-id="1937e-109">If you want to migrate data from other finance solutions, you must either check if an extension is available for that solution or import from Excel.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="1937e-110">inkluderar mallar förkonton, kunder, leverantörer och lagerartiklar som du kan välja att koppla, när du importerar dina data.</span><span class="sxs-lookup"><span data-stu-id="1937e-110">includes templates for accounts, customers, vendors, and inventory items that you can choose to apply when you import your data.</span></span>

<span data-ttu-id="1937e-111">Du kan importera huvuddata och vissa transaktionsdata från andra finansiella system baserat på standardkonfigurationspaketet i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1937e-111">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="1937e-112">På sidan **konfigurationspaket** kan du arbeta med paket för att importera och validera data innan du installerar paketet.</span><span class="sxs-lookup"><span data-stu-id="1937e-112">On the **Configuration Packages** page, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!TIP]  
> <span data-ttu-id="1937e-113">Vi rekommenderar att du använder guider för datamigrering för att importera data från Dynamics GP, Dynamics NAV eller QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="1937e-113">We recommend that you use data migration wizards to import data from Dynamics GP, Dynamics NAV, or QuickBooks.</span></span> <span data-ttu-id="1937e-114">Mer information finns i [Migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsinnehållet, eller [QuickBooks-datamigrering](ui-extensions-quickbooks-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="1937e-114">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content, or [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="1937e-115">För större implementeringar kan du använda RapidStart Services för [!INCLUDE[prod_short](includes/prod_short.md)] som är ett omfattande verktyg för att skapa nya lösningar baserade på kundernas affärskrav och konfigurationsdata.</span><span class="sxs-lookup"><span data-stu-id="1937e-115">For larger implementation work, you can use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], which is an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="1937e-116">RapidStart Services inkluderar även funktioner för import av affärsdata.</span><span class="sxs-lookup"><span data-stu-id="1937e-116">RapidStart Services also offers functionality for import of business data.</span></span> <span data-ttu-id="1937e-117">Mer information finns i [Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="1937e-117">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

<span data-ttu-id="1937e-118">Om du vill importera artikelbilder kan du använda en särskild funktion på sidan **Lagerinställningar**.</span><span class="sxs-lookup"><span data-stu-id="1937e-118">To import item pictures, you can use a dedicated function on the **Inventory Setup** page.</span></span> <span data-ttu-id="1937e-119">Mer information finns i [importera flera artikelbilder](inventory-how-import-item-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="1937e-119">For more information, see [Import Multiple Item Pictures](inventory-how-import-item-pictures.md).</span></span>

## <a name="importing-data-from-configuration-packages"></a><span data-ttu-id="1937e-120">Importera data från ett konfigurationspaket</span><span class="sxs-lookup"><span data-stu-id="1937e-120">Importing Data from Configuration Packages</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="1937e-121">innehåller ett konfigurationspaket som du kan exportera till Excel och ange dina data där.</span><span class="sxs-lookup"><span data-stu-id="1937e-121">includes a configuration package that you can export to Excel and set up your data there.</span></span> <span data-ttu-id="1937e-122">Sedan kan du importera datan från Excel igen.</span><span class="sxs-lookup"><span data-stu-id="1937e-122">Then, you can import the data from Excel again.</span></span> <span data-ttu-id="1937e-123">Paketet består av 27 register, inklusive huvuddata som t. ex. kunder, leverantörer, artiklar och konton, andra grundläggande inställningstabeller, som till exempel leveransmetoder och transaktionstabeller som t. ex. rubrik och rader.</span><span class="sxs-lookup"><span data-stu-id="1937e-123">The package consists of 27 tables, including master data such as customers, vendors, items, and accounts, other basic setup tables such as shipping methods, and transactions tables such as sales header and lines.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="1937e-124">Att arbeta med konfigurationspaket innebär avancerade funktioner och vi rekommenderar att du kontaktar din administratör.</span><span class="sxs-lookup"><span data-stu-id="1937e-124">Working with configuration packages is advanced functionality, and we recommend that you contact your administrator.</span></span> <span data-ttu-id="1937e-125">Mer information finns i [Importera data från äldre redovisningsprogram med ett konfigurationspaket](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="1937e-125">For more information, see [Importing Data from Legacy Accounting Software using a Configuration Package](across-import-data-configuration-packages.md).</span></span>

## <a name="working-with-data-in-excel"></a><span data-ttu-id="1937e-126">Arbeta med data i excel</span><span class="sxs-lookup"><span data-stu-id="1937e-126">Working with Data in Excel</span></span>
<span data-ttu-id="1937e-127">När du exporterar standardkonfigurationspaketet till Excel innehåller den genererade arbetsboken ett kalkylblad för varje register i förpackningen.</span><span class="sxs-lookup"><span data-stu-id="1937e-127">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="1937e-128">För att underlätta dina arbetsuppgifter kan du dra nytta av XML behandlingsverktygen som ingår i Excel.</span><span class="sxs-lookup"><span data-stu-id="1937e-128">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="1937e-129">Du kan även använda inbyggda Excel funktioner för att hjälp med dataformatering och för att ange data i rätt cell.</span><span class="sxs-lookup"><span data-stu-id="1937e-129">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="1937e-130">Lägg till exempel till ett tomt kalkylblad och kopiera befintliga data till det.</span><span class="sxs-lookup"><span data-stu-id="1937e-130">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="1937e-131">Gör en Excel-formel för att koppla data i omformnings kalkylarket mellan fälten i den exporterade kalkylarket och de bakåtkompatibla data för kunden.</span><span class="sxs-lookup"><span data-stu-id="1937e-131">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="1937e-132">När du har mappat alla data kopierar du intervallet av data till tabellkalkylarket.</span><span class="sxs-lookup"><span data-stu-id="1937e-132">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="1937e-133">Ändra inte kolumnerna i kalkylark.</span><span class="sxs-lookup"><span data-stu-id="1937e-133">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="1937e-134">Om de flyttats, ändras eller tas bort, kan kalkylarket inte importeras till [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1937e-134">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="1937e-135">Fält av BLOB-typen kan inte exporteras/importeras med Excel.</span><span class="sxs-lookup"><span data-stu-id="1937e-135">Fields of type Blob cannot be exported/imported using Excel.</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="1937e-136">Tabellerna i standardkonfigurationspaketet</span><span class="sxs-lookup"><span data-stu-id="1937e-136">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="1937e-137">Standardkonfigurationspaketet stöder följande tabeller:</span><span class="sxs-lookup"><span data-stu-id="1937e-137">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="1937e-138">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="1937e-138">Payment Terms</span></span>
-   <span data-ttu-id="1937e-139">Kund prisgrupp</span><span class="sxs-lookup"><span data-stu-id="1937e-139">Customer Price Group</span></span>
-   <span data-ttu-id="1937e-140">Utleveransmetod</span><span class="sxs-lookup"><span data-stu-id="1937e-140">Shipment Method</span></span>
-   <span data-ttu-id="1937e-141">Säljare/Inköpare</span><span class="sxs-lookup"><span data-stu-id="1937e-141">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="1937e-142">Plats</span><span class="sxs-lookup"><span data-stu-id="1937e-142">Location</span></span>
-   <span data-ttu-id="1937e-143">Redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="1937e-143">GL Account</span></span>
-   <span data-ttu-id="1937e-144">Kund</span><span class="sxs-lookup"><span data-stu-id="1937e-144">Customer</span></span>
-   <span data-ttu-id="1937e-145">Leverantör</span><span class="sxs-lookup"><span data-stu-id="1937e-145">Vendor</span></span>
-   <span data-ttu-id="1937e-146">Artikel</span><span class="sxs-lookup"><span data-stu-id="1937e-146">Item</span></span>
-   <span data-ttu-id="1937e-147">Försäljningshuvud</span><span class="sxs-lookup"><span data-stu-id="1937e-147">Sales Header</span></span>
-   <span data-ttu-id="1937e-148">Försäljningsrad</span><span class="sxs-lookup"><span data-stu-id="1937e-148">Sales Line</span></span>
-   <span data-ttu-id="1937e-149">Inköpshuvud</span><span class="sxs-lookup"><span data-stu-id="1937e-149">Purchase Header</span></span>
-   <span data-ttu-id="1937e-150">Inköpsrad</span><span class="sxs-lookup"><span data-stu-id="1937e-150">Purchase Line</span></span>
-   <span data-ttu-id="1937e-151">Redovisnings-</span><span class="sxs-lookup"><span data-stu-id="1937e-151">Gen.</span></span> <span data-ttu-id="1937e-152">journalrad</span><span class="sxs-lookup"><span data-stu-id="1937e-152">Journal Line</span></span>
-   <span data-ttu-id="1937e-153">Artikeljournalrad</span><span class="sxs-lookup"><span data-stu-id="1937e-153">Item Journal Line</span></span>
-   <span data-ttu-id="1937e-154">Kundbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="1937e-154">Customer Posting Group</span></span>
-   <span data-ttu-id="1937e-155">Leverantörsbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="1937e-155">Vendor Posting Group</span></span>
-   <span data-ttu-id="1937e-156">Lagerbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="1937e-156">Inventory Posting Group</span></span>
-   <span data-ttu-id="1937e-157">Måttenhet</span><span class="sxs-lookup"><span data-stu-id="1937e-157">Unit of Measure</span></span>
-   <span data-ttu-id="1937e-158">Redovisnings-</span><span class="sxs-lookup"><span data-stu-id="1937e-158">Gen.</span></span> <span data-ttu-id="1937e-159">Rörelsebokföringsmall</span><span class="sxs-lookup"><span data-stu-id="1937e-159">Business Posting Group</span></span>
-   <span data-ttu-id="1937e-160">Redovisnings-</span><span class="sxs-lookup"><span data-stu-id="1937e-160">Gen.</span></span> <span data-ttu-id="1937e-161">Produktbokföringsmall</span><span class="sxs-lookup"><span data-stu-id="1937e-161">Product Posting Group</span></span>
-   <span data-ttu-id="1937e-162">Bokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="1937e-162">General Posting Setup</span></span>
-   <span data-ttu-id="1937e-163">Distrikt</span><span class="sxs-lookup"><span data-stu-id="1937e-163">Territory</span></span>
-   <span data-ttu-id="1937e-164">Artikelkategori</span><span class="sxs-lookup"><span data-stu-id="1937e-164">Item Category</span></span>
-   <span data-ttu-id="1937e-165">Förs.pris</span><span class="sxs-lookup"><span data-stu-id="1937e-165">Sales Price</span></span>
-   <span data-ttu-id="1937e-166">Inköpspris</span><span class="sxs-lookup"><span data-stu-id="1937e-166">Purchase Price</span></span>

## <a name="see-also"></a><span data-ttu-id="1937e-167">Se även</span><span class="sxs-lookup"><span data-stu-id="1937e-167">See Also</span></span>
[<span data-ttu-id="1937e-168">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="1937e-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="1937e-169">Migrera lokala data till Business Central Online</span><span class="sxs-lookup"><span data-stu-id="1937e-169">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[<span data-ttu-id="1937e-170">QuickBooks datamigrering</span><span class="sxs-lookup"><span data-stu-id="1937e-170">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="1937e-171">Importera flera artikelbilder</span><span class="sxs-lookup"><span data-stu-id="1937e-171">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]