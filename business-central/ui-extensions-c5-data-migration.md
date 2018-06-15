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
ms.date: 04/09/208
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: fa6779ee8fb2bbb453014e32cb7f3cf8dcfa18da
ms.openlocfilehash: 698bde6949c6053501881d07135586810fc81bdd
ms.contentlocale: sv-se
ms.lasthandoff: 04/11/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="6ad88-103">Tillägget C5 för datamigrering för Business Central</span><span class="sxs-lookup"><span data-stu-id="6ad88-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="6ad88-104">Det här tillägget gör det enkelt att flytta över kunder, leverantörer, artiklar och dina redovisningskonton från Microsoft Dynamics C5 2012 till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6ad88-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6ad88-105">Du kan också migrera historiska transaktioner för redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="6ad88-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="6ad88-106">Företag i [!INCLUDE[d365fin](includes/d365fin_md.md)] får inte innehålla några data.</span><span class="sxs-lookup"><span data-stu-id="6ad88-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="6ad88-107">Dessutom, när du har startat en flyttning ska du inte skapa kunder, leverantörer, artiklar eller konton förrän migreringen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="6ad88-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="6ad88-108">Vilka data överförs?</span><span class="sxs-lookup"><span data-stu-id="6ad88-108">What Data is Migrated?</span></span>
<span data-ttu-id="6ad88-109">Följande data överförs för respektive enhet:</span><span class="sxs-lookup"><span data-stu-id="6ad88-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="6ad88-110">**Kunder**</span><span class="sxs-lookup"><span data-stu-id="6ad88-110">**Customers**</span></span>
* <span data-ttu-id="6ad88-111">Plats</span><span class="sxs-lookup"><span data-stu-id="6ad88-111">Location</span></span>
* <span data-ttu-id="6ad88-112">Land</span><span class="sxs-lookup"><span data-stu-id="6ad88-112">Country</span></span>
* <span data-ttu-id="6ad88-113">Kunddimensioner (avdelning, center, ändamål)</span><span class="sxs-lookup"><span data-stu-id="6ad88-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="6ad88-114">Utleveransmetod</span><span class="sxs-lookup"><span data-stu-id="6ad88-114">Shipment method</span></span>
* <span data-ttu-id="6ad88-115">Säljare</span><span class="sxs-lookup"><span data-stu-id="6ad88-115">Sales Person</span></span>
* <span data-ttu-id="6ad88-116">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="6ad88-116">Payment terms</span></span>
* <span data-ttu-id="6ad88-117">Betalningssätt</span><span class="sxs-lookup"><span data-stu-id="6ad88-117">Payment method</span></span>
* <span data-ttu-id="6ad88-118">Kundprisgrupp</span><span class="sxs-lookup"><span data-stu-id="6ad88-118">Customer price group</span></span>
* <span data-ttu-id="6ad88-119">Fakturarabatt för kund</span><span class="sxs-lookup"><span data-stu-id="6ad88-119">Customer invoice discount</span></span>

<span data-ttu-id="6ad88-120">Om du flyttar konton, flyttas även följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="6ad88-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="6ad88-121">Kundbokföringsinställning</span><span class="sxs-lookup"><span data-stu-id="6ad88-121">Customer posting setup</span></span>
* <span data-ttu-id="6ad88-122">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="6ad88-122">General journal batch</span></span>
* <span data-ttu-id="6ad88-123">Öppna kundreskontratransaktioner (kundreskontratransaktioner)</span><span class="sxs-lookup"><span data-stu-id="6ad88-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="6ad88-124">**Leverantör**</span><span class="sxs-lookup"><span data-stu-id="6ad88-124">**Vendors**</span></span>
* <span data-ttu-id="6ad88-125">Plats</span><span class="sxs-lookup"><span data-stu-id="6ad88-125">Location</span></span>
* <span data-ttu-id="6ad88-126">Land</span><span class="sxs-lookup"><span data-stu-id="6ad88-126">Country</span></span>
* <span data-ttu-id="6ad88-127">Leverantörsdimensioner (avdelning, center, ändamål)</span><span class="sxs-lookup"><span data-stu-id="6ad88-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="6ad88-128">Fakturarabatt</span><span class="sxs-lookup"><span data-stu-id="6ad88-128">Invoice discount</span></span>
* <span data-ttu-id="6ad88-129">Utleveransmetod</span><span class="sxs-lookup"><span data-stu-id="6ad88-129">Shipment method</span></span>
* <span data-ttu-id="6ad88-130">Inköpare</span><span class="sxs-lookup"><span data-stu-id="6ad88-130">Purchaser</span></span>
* <span data-ttu-id="6ad88-131">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="6ad88-131">Payment terms</span></span>
* <span data-ttu-id="6ad88-132">Betalningssätt</span><span class="sxs-lookup"><span data-stu-id="6ad88-132">Payment method</span></span>
* <span data-ttu-id="6ad88-133">Fakturarabatter för leverantör</span><span class="sxs-lookup"><span data-stu-id="6ad88-133">Vendor invoice discount</span></span>

<span data-ttu-id="6ad88-134">Om du flyttar konton, flyttas även följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="6ad88-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="6ad88-135">Leverantörsbokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="6ad88-135">Vendor posting setup</span></span>
* <span data-ttu-id="6ad88-136">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="6ad88-136">General journal batch</span></span>
* <span data-ttu-id="6ad88-137">Öppna transaktioner (leverantörsreskonstratransaktioner)</span><span class="sxs-lookup"><span data-stu-id="6ad88-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="6ad88-138">**Artiklar**</span><span class="sxs-lookup"><span data-stu-id="6ad88-138">**Items**</span></span>
* <span data-ttu-id="6ad88-139">Plats</span><span class="sxs-lookup"><span data-stu-id="6ad88-139">Location</span></span>
* <span data-ttu-id="6ad88-140">Land</span><span class="sxs-lookup"><span data-stu-id="6ad88-140">Country</span></span>
* <span data-ttu-id="6ad88-141">Artikeldimensioner (avdelning, center, ändamål)</span><span class="sxs-lookup"><span data-stu-id="6ad88-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="6ad88-142">Försäljningsradrabatter</span><span class="sxs-lookup"><span data-stu-id="6ad88-142">Sales line discounts</span></span>
* <span data-ttu-id="6ad88-143">Kundrabattgrupper</span><span class="sxs-lookup"><span data-stu-id="6ad88-143">Customer discount groups</span></span>
* <span data-ttu-id="6ad88-144">Artikelrabattgrupper</span><span class="sxs-lookup"><span data-stu-id="6ad88-144">Item discount groups</span></span>
* <span data-ttu-id="6ad88-145">Försäljningspris</span><span class="sxs-lookup"><span data-stu-id="6ad88-145">Sales price</span></span>
* <span data-ttu-id="6ad88-146">Tullnummer</span><span class="sxs-lookup"><span data-stu-id="6ad88-146">Tariff number</span></span>
* <span data-ttu-id="6ad88-147">Måttenheter</span><span class="sxs-lookup"><span data-stu-id="6ad88-147">Units of measure</span></span>
* <span data-ttu-id="6ad88-148">Artikelspårningskod</span><span class="sxs-lookup"><span data-stu-id="6ad88-148">Item tracking code</span></span>
* <span data-ttu-id="6ad88-149">Kundprisgrupp</span><span class="sxs-lookup"><span data-stu-id="6ad88-149">Customer price group</span></span>

<span data-ttu-id="6ad88-150">Om du flyttar konton, flyttas även följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="6ad88-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="6ad88-151">Lagerbokföringsinställning</span><span class="sxs-lookup"><span data-stu-id="6ad88-151">Inventory posting setup</span></span>
* <span data-ttu-id="6ad88-152">Bokföringsinställningar</span><span class="sxs-lookup"><span data-stu-id="6ad88-152">General posting setup</span></span>
* <span data-ttu-id="6ad88-153">Artikeljournaler</span><span class="sxs-lookup"><span data-stu-id="6ad88-153">Item journal batch</span></span>
* <span data-ttu-id="6ad88-154">Öppna transaktioner (artikeltransaktioner)</span><span class="sxs-lookup"><span data-stu-id="6ad88-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="6ad88-155">Om det finns öppna transaktioner med utländska valutor flyttas även valutakurserna för dessa valutor.</span><span class="sxs-lookup"><span data-stu-id="6ad88-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="6ad88-156">Andra valutakurser överförs inte.</span><span class="sxs-lookup"><span data-stu-id="6ad88-156">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="6ad88-157">**Kontoplan**</span><span class="sxs-lookup"><span data-stu-id="6ad88-157">**Chart of Accounts**</span></span>  
* <span data-ttu-id="6ad88-158">Standarddimensioner: avdelning, kostnadsställe, ändamål</span><span class="sxs-lookup"><span data-stu-id="6ad88-158">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="6ad88-159">Historiska redovisningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="6ad88-159">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="6ad88-160">Historiska redovisningstransaktioner hanteras på olika sätt.</span><span class="sxs-lookup"><span data-stu-id="6ad88-160">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="6ad88-161">När du migrerar data ställer du in en parameter för **aktuell period**.</span><span class="sxs-lookup"><span data-stu-id="6ad88-161">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="6ad88-162">Den här parametern anger hur du behandlar redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="6ad88-162">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="6ad88-163">Transaktioner efter detta datum migreras individuellt.</span><span class="sxs-lookup"><span data-stu-id="6ad88-163">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="6ad88-164">Transaktioner före det här datumet läggs samman per konto och flyttas över som ett enstaka belopp.</span><span class="sxs-lookup"><span data-stu-id="6ad88-164">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="6ad88-165">Låt oss anta att det finns transaktioner i 2015, 2016, 2017, 2018, och du anger 01 januari 2017 i fältet Aktuell period.</span><span class="sxs-lookup"><span data-stu-id="6ad88-165">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="6ad88-166">För varje konto samlas belopp för transaktioner på eller före den 31 december 2106 i en enda redovisningsjournalrad för varje redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="6ad88-166">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="6ad88-167">Alla transaktioner efter detta datum migreras individuellt.</span><span class="sxs-lookup"><span data-stu-id="6ad88-167">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="6ad88-168">Migrera data</span><span class="sxs-lookup"><span data-stu-id="6ad88-168">To migrate data</span></span>
<span data-ttu-id="6ad88-169">Det är bara några steg för att exportera data från C5 och importera den i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="6ad88-169">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="6ad88-170">I C5 använd funktionen **exportera databas** för att exportera data.</span><span class="sxs-lookup"><span data-stu-id="6ad88-170">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="6ad88-171">Skicka sedan exportmappen till en komprimerad mapp.</span><span class="sxs-lookup"><span data-stu-id="6ad88-171">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="6ad88-172">I [!INCLUDE[d365fin](includes/d365fin_md.md)], välj ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Sök efter sida eller rapport"), ange **Datamigrering** och välj sedan **Datamigrering**.</span><span class="sxs-lookup"><span data-stu-id="6ad88-172">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="6ad88-173">Följ instruktionerna i assisterad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6ad88-173">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="6ad88-174">Se till att använda **Importera från Microsoft Dynamcis C5 2012** som datakälla.</span><span class="sxs-lookup"><span data-stu-id="6ad88-174">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="6ad88-175">Företag lägger ofta till fält för att anpassa C5 till deras specifika verksamhet.</span><span class="sxs-lookup"><span data-stu-id="6ad88-175">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6ad88-176"> flyttar inte över data från anpassade fält.</span><span class="sxs-lookup"><span data-stu-id="6ad88-176"> does not migrate data from custom fields.</span></span> <span data-ttu-id="6ad88-177">Migreringen misslyckas även om det finns fler än 10 anpassade fält.</span><span class="sxs-lookup"><span data-stu-id="6ad88-177">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="6ad88-178">Visa status för migreringen.</span><span class="sxs-lookup"><span data-stu-id="6ad88-178">Viewing the Status of the Migration</span></span>
<span data-ttu-id="6ad88-179">Använd sidan **översikt över datamigrering** för att övervaka flyttningen.</span><span class="sxs-lookup"><span data-stu-id="6ad88-179">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="6ad88-180">På sidan visas information som till exempel antal enheter som migreringen omfattar, flyttning och antalet artiklar som har överförts och om de lyckades.</span><span class="sxs-lookup"><span data-stu-id="6ad88-180">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="6ad88-181">Den visar antalet fel, låter dig ta reda på vad som orsakade problemet och, när det är möjligt, gör det enkelt att gå till enheten för att lösa problemen.</span><span class="sxs-lookup"><span data-stu-id="6ad88-181">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="6ad88-182">Mer information finns i nästa avsnitt i den här artikeln.</span><span class="sxs-lookup"><span data-stu-id="6ad88-182">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="6ad88-183">Medan du väntar på resultat från migreringen, måste du uppdatera sidan för att visa resultatet.</span><span class="sxs-lookup"><span data-stu-id="6ad88-183">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="6ad88-184">Undvika dubbel bokföring</span><span class="sxs-lookup"><span data-stu-id="6ad88-184">How to Avoid Double-Posting</span></span>
<span data-ttu-id="6ad88-185">För att undvika dubbel bokföring i redovisningen används följande balansräkningskonton för öppna transaktioner:</span><span class="sxs-lookup"><span data-stu-id="6ad88-185">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  
  
* <span data-ttu-id="6ad88-186">För leverantörer använder vi A/P-konto från leverantörsbokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="6ad88-186">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="6ad88-187">För kunder använder vi A/P-konto från kundbokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="6ad88-187">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="6ad88-188">För artiklar skapar vi en bokföringsinställning där kontot för lagerjusteringar är det konto som anges som lagerkontot i fönstret Lagerbokföringsinställning.</span><span class="sxs-lookup"><span data-stu-id="6ad88-188">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="6ad88-189">Felkorrigering</span><span class="sxs-lookup"><span data-stu-id="6ad88-189">Correcting Errors</span></span>
<span data-ttu-id="6ad88-190">Om något går fel och ett fel uppstår kommer fältet **Status** att visa **Slutförd med fel** och fältet **Antal fel** visar hur många.</span><span class="sxs-lookup"><span data-stu-id="6ad88-190">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="6ad88-191">Om du vill visa en lista över felen, öppnar du sidan **migreringsfel** genom att välja:</span><span class="sxs-lookup"><span data-stu-id="6ad88-191">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="6ad88-192">Numret i fältet **antal fel** för enheten.</span><span class="sxs-lookup"><span data-stu-id="6ad88-192">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="6ad88-193">Enheten och åtgärden **Visa fel**.</span><span class="sxs-lookup"><span data-stu-id="6ad88-193">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="6ad88-194">På sidan **migreringsfel**, om du vill korrigera ett fel kan du välja ett felmeddelande och sedan välja **redigera post** för att öppna en sida som visar de migrerade data för enheten.</span><span class="sxs-lookup"><span data-stu-id="6ad88-194">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="6ad88-195">När du har korrigerat ett eller flera fel kan du välja **Migrera** för att endast överföra de enheter som har fastställts, utan att behöva starta om flyttningen helt.</span><span class="sxs-lookup"><span data-stu-id="6ad88-195">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="6ad88-196">Om du har kopplat mer än ett fel, kan du använda funktionen **Välj flera** om du vill markera flera rader att migrera.</span><span class="sxs-lookup"><span data-stu-id="6ad88-196">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="6ad88-197">Om det finns fel som inte är viktiga att fixa kan du välja dem och sedan välja **hoppa över val**.</span><span class="sxs-lookup"><span data-stu-id="6ad88-197">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="6ad88-198">Om du har artiklar som ingår i en struktur kan du behöva migrera flera gånger om det ursprungliga objektet inte skapas innan alla varianter som refererar till den.</span><span class="sxs-lookup"><span data-stu-id="6ad88-198">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="6ad88-199">Om en artikelvariant skapas först blir kan referensen till det ursprungliga objektet orsaka ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="6ad88-199">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="6ad88-200">Kontrollera data efter migrering</span><span class="sxs-lookup"><span data-stu-id="6ad88-200">Verifying Data After Migrating</span></span>
<span data-ttu-id="6ad88-201">Ett sätt att kontrollera att informationen överförs på rätt sätt är att titta på följande sidor i C5 och [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6ad88-201">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="6ad88-202">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="6ad88-202">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="6ad88-203">Batch-jobb som ska användas</span><span class="sxs-lookup"><span data-stu-id="6ad88-203">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="6ad88-204">Kundtransaktioner</span><span class="sxs-lookup"><span data-stu-id="6ad88-204">Customer Entries</span></span>| <span data-ttu-id="6ad88-205">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="6ad88-205">General Journals</span></span>| <span data-ttu-id="6ad88-206">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="6ad88-206">CUSTMIGR</span></span> |
|<span data-ttu-id="6ad88-207">Leverantörstransaktioner</span><span class="sxs-lookup"><span data-stu-id="6ad88-207">Vendor Entries</span></span>| <span data-ttu-id="6ad88-208">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="6ad88-208">General Journals</span></span>| <span data-ttu-id="6ad88-209">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="6ad88-209">VENDMIGR</span></span>|
|<span data-ttu-id="6ad88-210">Artikeltransaktioner</span><span class="sxs-lookup"><span data-stu-id="6ad88-210">Item Entries</span></span>| <span data-ttu-id="6ad88-211">Artikeljournaler</span><span class="sxs-lookup"><span data-stu-id="6ad88-211">Item Journals</span></span>| <span data-ttu-id="6ad88-212">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="6ad88-212">ITEMMIGR</span></span> |
|<span data-ttu-id="6ad88-213">Redovisningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="6ad88-213">G/L Entries</span></span>| <span data-ttu-id="6ad88-214">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="6ad88-214">General Journals</span></span>| <span data-ttu-id="6ad88-215">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="6ad88-215">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="6ad88-216">Stoppa datamigrering</span><span class="sxs-lookup"><span data-stu-id="6ad88-216">Stopping Data Migration</span></span>
<span data-ttu-id="6ad88-217">Du kan förhindra migrering av data genom att välja **Stoppa alla migreringar**.</span><span class="sxs-lookup"><span data-stu-id="6ad88-217">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="6ad88-218">Om du gör det kommer alla väntande migreringar också stoppas.</span><span class="sxs-lookup"><span data-stu-id="6ad88-218">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ad88-219">Se även</span><span class="sxs-lookup"><span data-stu-id="6ad88-219">See Also</span></span>
<span data-ttu-id="6ad88-220">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="6ad88-220">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="6ad88-221">Komma igång</span><span class="sxs-lookup"><span data-stu-id="6ad88-221">Getting Started</span></span>](product-get-started.md) 

