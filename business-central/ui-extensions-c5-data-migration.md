---
title: "Använda tillägget C5 Data-migrering | Microsoft Docs"
description: "Använda det här tillägget för att flytta över kunder, leverantörer, artiklar och redovisningskonton från Microsoft Dynamics C5 2012 till Business Central."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5c89d841cdf0e92af4a3dc497cb9c807798e3924
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---

# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="7fe61-103">Tillägget C5 Datamigrering </span><span class="sxs-lookup"><span data-stu-id="7fe61-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="7fe61-104">Det här tillägget gör det enkelt att flytta över kunder, leverantörer, artiklar och dina redovisningskonton från Microsoft Dynamics C5 2012 till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7fe61-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7fe61-105">Du kan också migrera historiska transaktioner för redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="7fe61-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="7fe61-106">Företag i [!INCLUDE[d365fin](includes/d365fin_md.md)] får inte innehålla några data.</span><span class="sxs-lookup"><span data-stu-id="7fe61-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="7fe61-107">Dessutom, när du har startat en flyttning ska du inte skapa kunder, leverantörer, artiklar eller konton förrän migreringen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="7fe61-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="7fe61-108">Vilka data överförs?</span><span class="sxs-lookup"><span data-stu-id="7fe61-108">What Data is Migrated?</span></span>
<span data-ttu-id="7fe61-109">Följande data överförs för respektive enhet:</span><span class="sxs-lookup"><span data-stu-id="7fe61-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="7fe61-110">**Kunder**</span><span class="sxs-lookup"><span data-stu-id="7fe61-110">**Customers**</span></span>
* <span data-ttu-id="7fe61-111">Kontakter</span><span class="sxs-lookup"><span data-stu-id="7fe61-111">Contacts</span></span>  
* <span data-ttu-id="7fe61-112">Plats</span><span class="sxs-lookup"><span data-stu-id="7fe61-112">Location</span></span>
* <span data-ttu-id="7fe61-113">Land</span><span class="sxs-lookup"><span data-stu-id="7fe61-113">Country</span></span>
* <span data-ttu-id="7fe61-114">Kunddimensioner (avdelning, center, ändamål)</span><span class="sxs-lookup"><span data-stu-id="7fe61-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7fe61-115">Utleveransmetod</span><span class="sxs-lookup"><span data-stu-id="7fe61-115">Shipment method</span></span>
* <span data-ttu-id="7fe61-116">Säljare</span><span class="sxs-lookup"><span data-stu-id="7fe61-116">Sales Person</span></span>
* <span data-ttu-id="7fe61-117">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="7fe61-117">Payment terms</span></span>
* <span data-ttu-id="7fe61-118">Betalningssätt</span><span class="sxs-lookup"><span data-stu-id="7fe61-118">Payment method</span></span>
* <span data-ttu-id="7fe61-119">Kundprisgrupp</span><span class="sxs-lookup"><span data-stu-id="7fe61-119">Customer price group</span></span>
* <span data-ttu-id="7fe61-120">Fakturarabatt för kund</span><span class="sxs-lookup"><span data-stu-id="7fe61-120">Customer invoice discount</span></span>

<span data-ttu-id="7fe61-121">Om du flyttar konton, flyttas även följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="7fe61-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7fe61-122">Kundbokföringsinställning</span><span class="sxs-lookup"><span data-stu-id="7fe61-122">Customer posting setup</span></span>
* <span data-ttu-id="7fe61-123">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="7fe61-123">General journal batch</span></span>
* <span data-ttu-id="7fe61-124">Öppna kundreskontratransaktioner (kundreskontratransaktioner)</span><span class="sxs-lookup"><span data-stu-id="7fe61-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="7fe61-125">**Leverantör**</span><span class="sxs-lookup"><span data-stu-id="7fe61-125">**Vendors**</span></span>
* <span data-ttu-id="7fe61-126">Kontakter</span><span class="sxs-lookup"><span data-stu-id="7fe61-126">Contacts</span></span>
* <span data-ttu-id="7fe61-127">Plats</span><span class="sxs-lookup"><span data-stu-id="7fe61-127">Location</span></span>
* <span data-ttu-id="7fe61-128">Land</span><span class="sxs-lookup"><span data-stu-id="7fe61-128">Country</span></span>
* <span data-ttu-id="7fe61-129">Leverantörsdimensioner (avdelning, center, ändamål)</span><span class="sxs-lookup"><span data-stu-id="7fe61-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7fe61-130">Fakturarabatt</span><span class="sxs-lookup"><span data-stu-id="7fe61-130">Invoice discount</span></span>
* <span data-ttu-id="7fe61-131">Utleveransmetod</span><span class="sxs-lookup"><span data-stu-id="7fe61-131">Shipment method</span></span>
* <span data-ttu-id="7fe61-132">Inköpare</span><span class="sxs-lookup"><span data-stu-id="7fe61-132">Purchaser</span></span>
* <span data-ttu-id="7fe61-133">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="7fe61-133">Payment terms</span></span>
* <span data-ttu-id="7fe61-134">Betalningssätt</span><span class="sxs-lookup"><span data-stu-id="7fe61-134">Payment method</span></span>
* <span data-ttu-id="7fe61-135">Fakturarabatter för leverantör</span><span class="sxs-lookup"><span data-stu-id="7fe61-135">Vendor invoice discount</span></span>

<span data-ttu-id="7fe61-136">Om du flyttar konton, flyttas även följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="7fe61-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7fe61-137">Leverantörsbokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="7fe61-137">Vendor posting setup</span></span>
* <span data-ttu-id="7fe61-138">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="7fe61-138">General journal batch</span></span>
* <span data-ttu-id="7fe61-139">Öppna transaktioner (leverantörsreskonstratransaktioner)</span><span class="sxs-lookup"><span data-stu-id="7fe61-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="7fe61-140">**Artiklar**</span><span class="sxs-lookup"><span data-stu-id="7fe61-140">**Items**</span></span>
* <span data-ttu-id="7fe61-141">Plats</span><span class="sxs-lookup"><span data-stu-id="7fe61-141">Location</span></span>
* <span data-ttu-id="7fe61-142">Land</span><span class="sxs-lookup"><span data-stu-id="7fe61-142">Country</span></span>
* <span data-ttu-id="7fe61-143">Artikeldimensioner (avdelning, center, ändamål)</span><span class="sxs-lookup"><span data-stu-id="7fe61-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7fe61-144">Försäljningsradrabatter</span><span class="sxs-lookup"><span data-stu-id="7fe61-144">Sales line discounts</span></span>
* <span data-ttu-id="7fe61-145">Kundrabattgrupper</span><span class="sxs-lookup"><span data-stu-id="7fe61-145">Customer discount groups</span></span>
* <span data-ttu-id="7fe61-146">Artikelrabattgrupper</span><span class="sxs-lookup"><span data-stu-id="7fe61-146">Item discount groups</span></span>
* <span data-ttu-id="7fe61-147">Försäljningspris</span><span class="sxs-lookup"><span data-stu-id="7fe61-147">Sales price</span></span>
* <span data-ttu-id="7fe61-148">Tullnummer</span><span class="sxs-lookup"><span data-stu-id="7fe61-148">Tariff number</span></span>
* <span data-ttu-id="7fe61-149">Måttenheter</span><span class="sxs-lookup"><span data-stu-id="7fe61-149">Units of measure</span></span>
* <span data-ttu-id="7fe61-150">Artikelspårningskod</span><span class="sxs-lookup"><span data-stu-id="7fe61-150">Item tracking code</span></span>
* <span data-ttu-id="7fe61-151">Kundprisgrupp</span><span class="sxs-lookup"><span data-stu-id="7fe61-151">Customer price group</span></span>
* <span data-ttu-id="7fe61-152">Monteringsstrukturer</span><span class="sxs-lookup"><span data-stu-id="7fe61-152">Assembly BOMs</span></span>

<span data-ttu-id="7fe61-153">Om du flyttar konton, flyttas även följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="7fe61-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7fe61-154">Lagerbokföringsinställning</span><span class="sxs-lookup"><span data-stu-id="7fe61-154">Inventory posting setup</span></span>
* <span data-ttu-id="7fe61-155">Bokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="7fe61-155">General posting setup</span></span>
* <span data-ttu-id="7fe61-156">Artikeljournaler</span><span class="sxs-lookup"><span data-stu-id="7fe61-156">Item journal batch</span></span>
* <span data-ttu-id="7fe61-157">Öppna transaktioner (artikeltransaktioner)</span><span class="sxs-lookup"><span data-stu-id="7fe61-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="7fe61-158">Om det finns öppna transaktioner med utländska valutor flyttas även valutakurserna för dessa valutor.</span><span class="sxs-lookup"><span data-stu-id="7fe61-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="7fe61-159">Andra valutakurser överförs inte.</span><span class="sxs-lookup"><span data-stu-id="7fe61-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="7fe61-160">**Kontoplan**</span><span class="sxs-lookup"><span data-stu-id="7fe61-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="7fe61-161">Standarddimensioner: avdelning, kostnadsställe, ändamål</span><span class="sxs-lookup"><span data-stu-id="7fe61-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="7fe61-162">Historiska redovisningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="7fe61-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="7fe61-163">Historiska redovisningstransaktioner hanteras på olika sätt.</span><span class="sxs-lookup"><span data-stu-id="7fe61-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="7fe61-164">När du migrerar data ställer du in en parameter för **aktuell period**.</span><span class="sxs-lookup"><span data-stu-id="7fe61-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="7fe61-165">Den här parametern anger hur du behandlar redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="7fe61-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="7fe61-166">Transaktioner efter detta datum migreras individuellt.</span><span class="sxs-lookup"><span data-stu-id="7fe61-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="7fe61-167">Transaktioner före det här datumet läggs samman per konto och flyttas över som ett enstaka belopp.</span><span class="sxs-lookup"><span data-stu-id="7fe61-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="7fe61-168">Låt oss anta att det finns transaktioner i 2015, 2016, 2017, 2018, och du anger 01 januari 2017 i fältet Aktuell period.</span><span class="sxs-lookup"><span data-stu-id="7fe61-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="7fe61-169">För varje konto samlas belopp för transaktioner på eller före den 31 december 2106 i en enda redovisningsjournalrad för varje redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="7fe61-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="7fe61-170">Alla transaktioner efter detta datum migreras individuellt.</span><span class="sxs-lookup"><span data-stu-id="7fe61-170">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="7fe61-171">Migrera data</span><span class="sxs-lookup"><span data-stu-id="7fe61-171">To migrate data</span></span>
<span data-ttu-id="7fe61-172">Det är bara några steg för att exportera data från C5 och importera den i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="7fe61-172">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="7fe61-173">I C5 använd funktionen **exportera databas** för att exportera data.</span><span class="sxs-lookup"><span data-stu-id="7fe61-173">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="7fe61-174">Skicka sedan exportmappen till en komprimerad mapp.</span><span class="sxs-lookup"><span data-stu-id="7fe61-174">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="7fe61-175">I [!INCLUDE[d365fin](includes/d365fin_md.md)], välj ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Datamigrering** och välj sedan **Datamigrering**.</span><span class="sxs-lookup"><span data-stu-id="7fe61-175">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="7fe61-176">Följ instruktionerna i assisterad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fe61-176">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="7fe61-177">Se till att använda **Importera från Microsoft Dynamcis C5 2012** som datakälla.</span><span class="sxs-lookup"><span data-stu-id="7fe61-177">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="7fe61-178">Visa status för migreringen.</span><span class="sxs-lookup"><span data-stu-id="7fe61-178">Viewing the Status of the Migration</span></span>
<span data-ttu-id="7fe61-179">Använd sidan **översikt över datamigrering** för att övervaka flyttningen.</span><span class="sxs-lookup"><span data-stu-id="7fe61-179">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="7fe61-180">På sidan visas information som till exempel antal enheter som migreringen omfattar, flyttning och antalet artiklar som har överförts och om de lyckades.</span><span class="sxs-lookup"><span data-stu-id="7fe61-180">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="7fe61-181">Den visar antalet fel, låter dig ta reda på vad som orsakade problemet och, när det är möjligt, gör det enkelt att gå till enheten för att lösa problemen.</span><span class="sxs-lookup"><span data-stu-id="7fe61-181">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="7fe61-182">Mer information finns i nästa avsnitt i den här artikeln.</span><span class="sxs-lookup"><span data-stu-id="7fe61-182">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="7fe61-183">Medan du väntar på resultat från migreringen, måste du uppdatera sidan för att visa resultatet.</span><span class="sxs-lookup"><span data-stu-id="7fe61-183">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="7fe61-184">Undvika dubbel bokföring</span><span class="sxs-lookup"><span data-stu-id="7fe61-184">How to Avoid Double-Posting</span></span>
<span data-ttu-id="7fe61-185">För att undvika dubbel bokföring i redovisningen används följande balansräkningskonton för öppna transaktioner:</span><span class="sxs-lookup"><span data-stu-id="7fe61-185">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="7fe61-186">För leverantörer använder vi A/P-konto från leverantörsbokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="7fe61-186">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="7fe61-187">För kunder använder vi A/P-konto från kundbokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="7fe61-187">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="7fe61-188">För artiklar skapar vi en bokföringsinställning där kontot för lagerjusteringar är det konto som anges som lagerkontot i fönstret Lagerbokföringsinställning.</span><span class="sxs-lookup"><span data-stu-id="7fe61-188">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="7fe61-189">Felkorrigering</span><span class="sxs-lookup"><span data-stu-id="7fe61-189">Correcting Errors</span></span>
<span data-ttu-id="7fe61-190">Om något går fel och ett fel uppstår kommer fältet **Status** att visa **Slutförd med fel** och fältet **Antal fel** visar hur många.</span><span class="sxs-lookup"><span data-stu-id="7fe61-190">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="7fe61-191">Om du vill visa en lista över felen, öppnar du sidan **migreringsfel** genom att välja:</span><span class="sxs-lookup"><span data-stu-id="7fe61-191">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="7fe61-192">Numret i fältet **antal fel** för enheten.</span><span class="sxs-lookup"><span data-stu-id="7fe61-192">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="7fe61-193">Enheten och åtgärden **Visa fel**.</span><span class="sxs-lookup"><span data-stu-id="7fe61-193">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="7fe61-194">På sidan **migreringsfel**, om du vill korrigera ett fel kan du välja ett felmeddelande och sedan välja **redigera post** för att visa de migrerade data för enheten.</span><span class="sxs-lookup"><span data-stu-id="7fe61-194">On the **Data Migration Errors** page, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="7fe61-195">Om du har flera fel att fixa kan du välja **reparera flera fel** för att redigera poster i en lista.</span><span class="sxs-lookup"><span data-stu-id="7fe61-195">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="7fe61-196">Du behöver öppna enskilda poster om felet orsakades av en relaterad post.</span><span class="sxs-lookup"><span data-stu-id="7fe61-196">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="7fe61-197">Om t.ex. en leverantör inte vill migrera om en e-postadress för en av deras kontakter har ett felaktigt format.</span><span class="sxs-lookup"><span data-stu-id="7fe61-197">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="7fe61-198">När du har korrigerat ett eller flera fel kan du välja **Migrera** för att endast överföra de enheter som har fastställts, utan att behöva starta om flyttningen helt.</span><span class="sxs-lookup"><span data-stu-id="7fe61-198">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="7fe61-199">Om du har kopplat mer än ett fel, kan du använda funktionen **Välj flera** om du vill markera flera rader att migrera.</span><span class="sxs-lookup"><span data-stu-id="7fe61-199">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="7fe61-200">Om det finns fel som inte är viktiga att fixa kan du välja dem och sedan välja **hoppa över val**.</span><span class="sxs-lookup"><span data-stu-id="7fe61-200">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="7fe61-201">Om du har artiklar som ingår i en struktur kan du behöva migrera flera gånger om det ursprungliga objektet inte skapas innan alla varianter som refererar till den.</span><span class="sxs-lookup"><span data-stu-id="7fe61-201">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="7fe61-202">Om en artikelvariant skapas först blir kan referensen till det ursprungliga objektet orsaka ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="7fe61-202">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="7fe61-203">Kontrollera data efter migrering</span><span class="sxs-lookup"><span data-stu-id="7fe61-203">Verifying Data After Migrating</span></span>
<span data-ttu-id="7fe61-204">Ett sätt att kontrollera att informationen överförs på rätt sätt är att titta på följande sidor i C5 och [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7fe61-204">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="7fe61-205">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="7fe61-205">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="7fe61-206">Batch-jobb som ska användas</span><span class="sxs-lookup"><span data-stu-id="7fe61-206">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="7fe61-207">Kundtransaktioner</span><span class="sxs-lookup"><span data-stu-id="7fe61-207">Customer Entries</span></span>| <span data-ttu-id="7fe61-208">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="7fe61-208">General Journals</span></span>| <span data-ttu-id="7fe61-209">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="7fe61-209">CUSTMIGR</span></span> |
|<span data-ttu-id="7fe61-210">Leverantörstransaktioner</span><span class="sxs-lookup"><span data-stu-id="7fe61-210">Vendor Entries</span></span>| <span data-ttu-id="7fe61-211">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="7fe61-211">General Journals</span></span>| <span data-ttu-id="7fe61-212">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="7fe61-212">VENDMIGR</span></span>|
|<span data-ttu-id="7fe61-213">Artikeltransaktioner</span><span class="sxs-lookup"><span data-stu-id="7fe61-213">Item Entries</span></span>| <span data-ttu-id="7fe61-214">Artikeljournaler</span><span class="sxs-lookup"><span data-stu-id="7fe61-214">Item Journals</span></span>| <span data-ttu-id="7fe61-215">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="7fe61-215">ITEMMIGR</span></span> |
|<span data-ttu-id="7fe61-216">Redovisningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="7fe61-216">G/L Entries</span></span>| <span data-ttu-id="7fe61-217">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="7fe61-217">General Journals</span></span>| <span data-ttu-id="7fe61-218">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="7fe61-218">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="7fe61-219">Stoppa datamigrering</span><span class="sxs-lookup"><span data-stu-id="7fe61-219">Stopping Data Migration</span></span>
<span data-ttu-id="7fe61-220">Du kan förhindra migrering av data genom att välja **Stoppa alla migreringar**.</span><span class="sxs-lookup"><span data-stu-id="7fe61-220">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="7fe61-221">Om du gör det kommer alla väntande migreringar också stoppas.</span><span class="sxs-lookup"><span data-stu-id="7fe61-221">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fe61-222">Se även</span><span class="sxs-lookup"><span data-stu-id="7fe61-222">See Also</span></span>
<span data-ttu-id="7fe61-223">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="7fe61-223">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="7fe61-224">Komma igång</span><span class="sxs-lookup"><span data-stu-id="7fe61-224">Getting Started</span></span>](product-get-started.md)

