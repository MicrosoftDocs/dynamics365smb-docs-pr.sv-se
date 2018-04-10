---
title: "Använda tillägget C5 Data-migrering | Microsoft Docs"
description: "Använda det här tillägget för att flytta över kunder, leverantörer, artiklar och redovisningskonton från Microsoft Dynamics C5 2012 till Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7fe6393ad43dbad032512b2d6d45cc8ee0392236
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="1f5dc-103">Tillägget C5 för datamigrering för Business Central</span><span class="sxs-lookup"><span data-stu-id="1f5dc-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="1f5dc-104">Det här tillägget gör det enkelt att flytta över kunder, leverantörer, artiklar och dina redovisningskonton från Microsoft Dynamics C5 2012 till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1f5dc-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1f5dc-105">Du kan också migrera historiska transaktioner för redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="1f5dc-106">Företag i [!INCLUDE[d365fin](includes/d365fin_md.md)] får inte innehålla några data.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="1f5dc-107">Dessutom, när du har startat en flyttning ska du inte skapa kunder, leverantörer, artiklar eller konton förrän migreringen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

##<a name="what-data-is-migrated"></a><span data-ttu-id="1f5dc-108">Vilka data överförs?</span><span class="sxs-lookup"><span data-stu-id="1f5dc-108">What Data is Migrated?</span></span>
<span data-ttu-id="1f5dc-109">Följande data överförs för respektive enhet:</span><span class="sxs-lookup"><span data-stu-id="1f5dc-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="1f5dc-110">**Kunder**</span><span class="sxs-lookup"><span data-stu-id="1f5dc-110">**Customers**</span></span>
* <span data-ttu-id="1f5dc-111">Plats</span><span class="sxs-lookup"><span data-stu-id="1f5dc-111">Location</span></span>
* <span data-ttu-id="1f5dc-112">Land</span><span class="sxs-lookup"><span data-stu-id="1f5dc-112">Country</span></span>
* <span data-ttu-id="1f5dc-113">Kunddimensioner (avdelning, center, ändamål)</span><span class="sxs-lookup"><span data-stu-id="1f5dc-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1f5dc-114">Utleveransmetod</span><span class="sxs-lookup"><span data-stu-id="1f5dc-114">Shipment method</span></span>
* <span data-ttu-id="1f5dc-115">Säljare</span><span class="sxs-lookup"><span data-stu-id="1f5dc-115">Sales Person</span></span>
* <span data-ttu-id="1f5dc-116">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="1f5dc-116">Payment terms</span></span>
* <span data-ttu-id="1f5dc-117">Betalningssätt</span><span class="sxs-lookup"><span data-stu-id="1f5dc-117">Payment method</span></span>
* <span data-ttu-id="1f5dc-118">Kundprisgrupp</span><span class="sxs-lookup"><span data-stu-id="1f5dc-118">Customer price group</span></span>
* <span data-ttu-id="1f5dc-119">Fakturarabatt för kund</span><span class="sxs-lookup"><span data-stu-id="1f5dc-119">Customer invoice discount</span></span>

<span data-ttu-id="1f5dc-120">Om du flyttar konton, flyttas även följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="1f5dc-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1f5dc-121">Kundbokföringsinställning</span><span class="sxs-lookup"><span data-stu-id="1f5dc-121">Customer posting setup</span></span>
* <span data-ttu-id="1f5dc-122">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="1f5dc-122">General journal batch</span></span>
* <span data-ttu-id="1f5dc-123">Öppna kundreskontratransaktioner (kundreskontratransaktioner)</span><span class="sxs-lookup"><span data-stu-id="1f5dc-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="1f5dc-124">**Leverantör**</span><span class="sxs-lookup"><span data-stu-id="1f5dc-124">**Vendors**</span></span>
* <span data-ttu-id="1f5dc-125">Plats</span><span class="sxs-lookup"><span data-stu-id="1f5dc-125">Location</span></span>
* <span data-ttu-id="1f5dc-126">Land</span><span class="sxs-lookup"><span data-stu-id="1f5dc-126">Country</span></span>
* <span data-ttu-id="1f5dc-127">Leverantörsdimensioner (avdelning, center, ändamål)</span><span class="sxs-lookup"><span data-stu-id="1f5dc-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1f5dc-128">Fakturarabatt</span><span class="sxs-lookup"><span data-stu-id="1f5dc-128">Invoice discount</span></span>
* <span data-ttu-id="1f5dc-129">Utleveransmetod</span><span class="sxs-lookup"><span data-stu-id="1f5dc-129">Shipment method</span></span>
* <span data-ttu-id="1f5dc-130">Inköpare</span><span class="sxs-lookup"><span data-stu-id="1f5dc-130">Purchaser</span></span>
* <span data-ttu-id="1f5dc-131">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="1f5dc-131">Payment terms</span></span>
* <span data-ttu-id="1f5dc-132">Betalningssätt</span><span class="sxs-lookup"><span data-stu-id="1f5dc-132">Payment method</span></span>
* <span data-ttu-id="1f5dc-133">Fakturarabatter för leverantör</span><span class="sxs-lookup"><span data-stu-id="1f5dc-133">Vendor invoice discount</span></span>

<span data-ttu-id="1f5dc-134">Om du flyttar konton, flyttas även följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="1f5dc-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1f5dc-135">Leverantörsbokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="1f5dc-135">Vendor posting setup</span></span>
* <span data-ttu-id="1f5dc-136">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="1f5dc-136">General journal batch</span></span>
* <span data-ttu-id="1f5dc-137">Öppna transaktioner (leverantörsreskonstratransaktioner)</span><span class="sxs-lookup"><span data-stu-id="1f5dc-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="1f5dc-138">**Artiklar**</span><span class="sxs-lookup"><span data-stu-id="1f5dc-138">**Items**</span></span>
* <span data-ttu-id="1f5dc-139">Plats</span><span class="sxs-lookup"><span data-stu-id="1f5dc-139">Location</span></span>
* <span data-ttu-id="1f5dc-140">Land</span><span class="sxs-lookup"><span data-stu-id="1f5dc-140">Country</span></span>
* <span data-ttu-id="1f5dc-141">Artikeldimensioner (avdelning, center, ändamål)</span><span class="sxs-lookup"><span data-stu-id="1f5dc-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1f5dc-142">Försäljningsradrabatter</span><span class="sxs-lookup"><span data-stu-id="1f5dc-142">Sales line discounts</span></span>
* <span data-ttu-id="1f5dc-143">Kundrabattgrupper</span><span class="sxs-lookup"><span data-stu-id="1f5dc-143">Customer discount groups</span></span>
* <span data-ttu-id="1f5dc-144">Artikelrabattgrupper</span><span class="sxs-lookup"><span data-stu-id="1f5dc-144">Item discount groups</span></span>
* <span data-ttu-id="1f5dc-145">Försäljningspris</span><span class="sxs-lookup"><span data-stu-id="1f5dc-145">Sales price</span></span>
* <span data-ttu-id="1f5dc-146">Tullnummer</span><span class="sxs-lookup"><span data-stu-id="1f5dc-146">Tariff number</span></span>
* <span data-ttu-id="1f5dc-147">Måttenheter</span><span class="sxs-lookup"><span data-stu-id="1f5dc-147">Units of measure</span></span>
* <span data-ttu-id="1f5dc-148">Artikelspårningskod</span><span class="sxs-lookup"><span data-stu-id="1f5dc-148">Item tracking code</span></span>
* <span data-ttu-id="1f5dc-149">Kundprisgrupp</span><span class="sxs-lookup"><span data-stu-id="1f5dc-149">Customer price group</span></span>

<span data-ttu-id="1f5dc-150">Om du flyttar konton, flyttas även följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="1f5dc-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1f5dc-151">Lagerbokföringsinställning</span><span class="sxs-lookup"><span data-stu-id="1f5dc-151">Inventory posting setup</span></span>
* <span data-ttu-id="1f5dc-152">Bokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="1f5dc-152">General posting setup</span></span>
* <span data-ttu-id="1f5dc-153">Artikeljournaler</span><span class="sxs-lookup"><span data-stu-id="1f5dc-153">Item journal batch</span></span>
* <span data-ttu-id="1f5dc-154">Öppna transaktioner (artikeltransaktioner)</span><span class="sxs-lookup"><span data-stu-id="1f5dc-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="1f5dc-155">Om det finns öppna transaktioner med utländska valutor flyttas även valutakurserna för dessa valutor.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="1f5dc-156">Andra valutakurser överförs inte.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-156">Other exchange rates are not migrated.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="1f5dc-157">Migrera data</span><span class="sxs-lookup"><span data-stu-id="1f5dc-157">To migrate data</span></span>
<span data-ttu-id="1f5dc-158">Det är bara några steg för att exportera data från C5 och importera den i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="1f5dc-158">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="1f5dc-159">I C5 använd funktionen **exportera databas** för att exportera data.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-159">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="1f5dc-160">Skicka sedan exportmappen till en komprimerad mapp.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-160">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="1f5dc-161">I [!INCLUDE[d365fin](includes/d365fin_md.md)], välj ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Sök efter sida eller rapport"), ange **Datamigrering** och välj sedan **Datamigrering**.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-161">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="1f5dc-162">Följ instruktionerna i assisterad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-162">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="1f5dc-163">Se till att använda **Importera från Microsoft Dynamcis C5 2012** som datakälla.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-163">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="1f5dc-164">Företag lägger ofta till fält för att anpassa C5 till deras specifika verksamhet.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-164">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="1f5dc-165"> flyttar inte över data från anpassade fält.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-165"> does not migrate data from custom fields.</span></span> <span data-ttu-id="1f5dc-166">Migreringen misslyckas även om det finns fler än 10 anpassade fält.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-166">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="1f5dc-167">Visa status för migreringen.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-167">Viewing the Status of the Migration</span></span>
<span data-ttu-id="1f5dc-168">Använd sidan **översikt över datamigrering** för att övervaka flyttningen.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-168">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="1f5dc-169">På sidan visas information som till exempel antal enheter som migreringen omfattar, flyttning och antalet artiklar som har överförts och om de lyckades.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-169">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="1f5dc-170">Den visar antalet fel, låter dig ta reda på vad som orsakade problemet och, när det är möjligt, gör det enkelt att gå till enheten för att lösa problemen.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-170">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="1f5dc-171">Mer information finns i nästa avsnitt i den här artikeln.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-171">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="1f5dc-172">Medan du väntar på resultat från migreringen, måste du uppdatera sidan för att visa resultatet.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-172">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="1f5dc-173">Felkorrigering</span><span class="sxs-lookup"><span data-stu-id="1f5dc-173">Correcting Errors</span></span>
<span data-ttu-id="1f5dc-174">Om något går fel och ett fel uppstår kommer fältet **Status** att visa **Slutförd med fel** och fältet **Antal fel** visar hur många.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-174">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="1f5dc-175">Om du vill visa en lista över felen, öppnar du sidan **migreringsfel** genom att välja:</span><span class="sxs-lookup"><span data-stu-id="1f5dc-175">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="1f5dc-176">Numret i fältet **antal fel** för enheten.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-176">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="1f5dc-177">Enheten och åtgärden **Visa fel**.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-177">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="1f5dc-178">På sidan **migreringsfel**, om du vill korrigera ett fel kan du välja ett felmeddelande och sedan välja **redigera post** för att öppna en sida som visar de migrerade data för enheten.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-178">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="1f5dc-179">När du har korrigerat ett eller flera fel kan du välja **Migrera** för att endast överföra de enheter som har fastställts, utan att behöva starta om flyttningen helt.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-179">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="1f5dc-180">Om du har kopplat mer än ett fel, kan du använda funktionen **Välj flera** om du vill markera flera rader att migrera.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-180">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="1f5dc-181">Om det finns fel som inte är viktiga att fixa kan du välja dem och sedan välja **hoppa över val**.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-181">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="1f5dc-182">Om du har artiklar som ingår i en struktur kan du behöva migrera flera gånger om det ursprungliga objektet inte skapas innan alla varianter som refererar till den.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-182">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="1f5dc-183">Om en artikelvariant skapas först blir kan referensen till det ursprungliga objektet orsaka ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-183">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="1f5dc-184">Kontrollera data efter migrering</span><span class="sxs-lookup"><span data-stu-id="1f5dc-184">Verifying Data After Migrating</span></span>
<span data-ttu-id="1f5dc-185">Ett sätt att kontrollera att informationen överförs på rätt sätt är att titta på följande sidor i C5 och [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1f5dc-185">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="1f5dc-186">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="1f5dc-186">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="1f5dc-187">Kundtransaktioner</span><span class="sxs-lookup"><span data-stu-id="1f5dc-187">Customer Entries</span></span>| <span data-ttu-id="1f5dc-188">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="1f5dc-188">General Journals</span></span>|
|<span data-ttu-id="1f5dc-189">Leverantörstransaktioner</span><span class="sxs-lookup"><span data-stu-id="1f5dc-189">Vendor Entries</span></span>| <span data-ttu-id="1f5dc-190">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="1f5dc-190">General Journals</span></span>|
|<span data-ttu-id="1f5dc-191">Artikeltransaktioner</span><span class="sxs-lookup"><span data-stu-id="1f5dc-191">Item Entries</span></span>| <span data-ttu-id="1f5dc-192">Artikeljournaler</span><span class="sxs-lookup"><span data-stu-id="1f5dc-192">Item Journals</span></span>|

<span data-ttu-id="1f5dc-193">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kallas journalen för migrerade data för **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span>

## <a name="stopping-data-migration"></a><span data-ttu-id="1f5dc-194">Stoppa datamigrering</span><span class="sxs-lookup"><span data-stu-id="1f5dc-194">Stopping Data Migration</span></span>
<span data-ttu-id="1f5dc-195">Du kan förhindra migrering av data genom att välja **Stoppa alla migreringar**.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-195">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="1f5dc-196">Om du gör det kommer alla väntande migreringar också stoppas.</span><span class="sxs-lookup"><span data-stu-id="1f5dc-196">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f5dc-197">Se även</span><span class="sxs-lookup"><span data-stu-id="1f5dc-197">See Also</span></span>
<span data-ttu-id="1f5dc-198">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="1f5dc-198">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="1f5dc-199">Komma igång</span><span class="sxs-lookup"><span data-stu-id="1f5dc-199">Getting Started</span></span>](product-get-started.md) 

