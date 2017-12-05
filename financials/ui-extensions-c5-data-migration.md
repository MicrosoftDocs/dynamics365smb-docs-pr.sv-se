---
title: "Använda tillägget C5 Data-migrering | Microsoft Docs"
description: "Använda det här tillägget för att flytta över kunder, leverantörer, artiklar och redovisningskonton från Microsoft Dynamics C5 2012 till Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 09/26/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2d7d533662936116ffa40ded07b68e845fed810b
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---

# <a name="the-c5-data-migration-extension-for-dynamics-365-for-finance-and-operations-business-edition"></a><span data-ttu-id="f36e6-103">Tillägget för C5-datamigrering för Dynamics 365 for Finance and Operations, Business Edition</span><span class="sxs-lookup"><span data-stu-id="f36e6-103">The C5 Data Migration Extension for Dynamics 365 for Finance and Operations, Business Edition</span></span>
<span data-ttu-id="f36e6-104">Det här tillägget gör det enkelt att flytta över kunder, leverantörer, artiklar och dina redovisningskonton från Microsoft Dynamics C5 2012 till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f36e6-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
> [!Note] 
> <span data-ttu-id="f36e6-105">Företag i [!INCLUDE[d365fin](includes/d365fin_md.md)] får inte innehålla några data.</span><span class="sxs-lookup"><span data-stu-id="f36e6-105">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="f36e6-106">Dessutom, när du har startat en flyttning ska du inte skapa kunder, leverantörer, artiklar eller konton förrän migreringen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="f36e6-106">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="f36e6-107">Migrera data</span><span class="sxs-lookup"><span data-stu-id="f36e6-107">To migrate data</span></span>
<span data-ttu-id="f36e6-108">Det är bara några steg för att exportera data från C5 och importera den i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="f36e6-108">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  
  
1. <span data-ttu-id="f36e6-109">I C5 använd funktionen **exportera databas** för att exportera data.</span><span class="sxs-lookup"><span data-stu-id="f36e6-109">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="f36e6-110">Skicka sedan exportmappen till en komprimerad mapp.</span><span class="sxs-lookup"><span data-stu-id="f36e6-110">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="f36e6-111">I [!INCLUDE[d365fin](includes/d365fin_md.md)], välj ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Sök efter sida eller rapport"), ange **Datamigrering** och välj sedan **Datamigrering**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-111">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="f36e6-112">Följ instruktionerna i assisterad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f36e6-112">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="f36e6-113">Se till att använda **Importera från Microsoft Dynamcis C5 2012** som datakälla.</span><span class="sxs-lookup"><span data-stu-id="f36e6-113">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note] 
> <span data-ttu-id="f36e6-114">Företag lägger ofta till fält för att anpassa C5 till deras specifika verksamhet.</span><span class="sxs-lookup"><span data-stu-id="f36e6-114">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f36e6-115"> flyttar inte över data från anpassade fält.</span><span class="sxs-lookup"><span data-stu-id="f36e6-115"> does not migrate data from custom fields.</span></span> <span data-ttu-id="f36e6-116">Migreringen misslyckas även om det finns fler än 10 anpassade fält.</span><span class="sxs-lookup"><span data-stu-id="f36e6-116">Also, migration will fail if you have more than 10 custom fields.</span></span> 

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="f36e6-117">Visa status för migreringen.</span><span class="sxs-lookup"><span data-stu-id="f36e6-117">Viewing the Status of the Migration</span></span>
<span data-ttu-id="f36e6-118">Använd sidan **översikt över datamigrering** för att övervaka flyttningen.</span><span class="sxs-lookup"><span data-stu-id="f36e6-118">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="f36e6-119">På sidan visas information som till exempel antal enheter som migreringen omfattar, flyttning och antalet artiklar som har överförts och om de lyckades.</span><span class="sxs-lookup"><span data-stu-id="f36e6-119">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="f36e6-120">Den visar antalet fel, låter dig ta reda på vad som orsakade problemet och, när det är möjligt, gör det enkelt att gå till enheten för att lösa problemen.</span><span class="sxs-lookup"><span data-stu-id="f36e6-120">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="f36e6-121">Mer information finns i nästa avsnitt i den här artikeln.</span><span class="sxs-lookup"><span data-stu-id="f36e6-121">For more information, see the next section in this topic.</span></span> 

> [!Note] 
> <span data-ttu-id="f36e6-122">Medan du väntar på resultat från migreringen, måste du uppdatera sidan för att visa resultatet.</span><span class="sxs-lookup"><span data-stu-id="f36e6-122">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="f36e6-123">Felkorrigering</span><span class="sxs-lookup"><span data-stu-id="f36e6-123">Correcting Errors</span></span>
<span data-ttu-id="f36e6-124">Om något går fel och ett fel uppstår kommer fältet **Status** att visa **Slutförd med fel** och fältet **Antal fel** visar hur många.</span><span class="sxs-lookup"><span data-stu-id="f36e6-124">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="f36e6-125">Om du vill visa en lista över felen, öppnar du sidan **migreringsfel** genom att välja:</span><span class="sxs-lookup"><span data-stu-id="f36e6-125">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>

* <span data-ttu-id="f36e6-126">Numret i fältet **antal fel** för enheten.</span><span class="sxs-lookup"><span data-stu-id="f36e6-126">The number in the **Error Count** field for the entity.</span></span> 
* <span data-ttu-id="f36e6-127">Enheten och åtgärden **Visa fel**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-127">The entity, and then the **Show Errors** action.</span></span> 

<span data-ttu-id="f36e6-128">På sidan **migreringsfel**, om du vill korrigera ett fel kan du välja ett felmeddelande och sedan välja **redigera post** för att öppna en sida som visar de migrerade data för enheten.</span><span class="sxs-lookup"><span data-stu-id="f36e6-128">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="f36e6-129">När du har korrigerat ett eller flera fel kan du välja **Migrera** för att endast överföra de enheter som har fastställts, utan att behöva starta om flyttningen helt.</span><span class="sxs-lookup"><span data-stu-id="f36e6-129">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="f36e6-130">Om du har kopplat mer än ett fel, kan du använda funktionen **Välj flera** om du vill markera flera rader att migrera.</span><span class="sxs-lookup"><span data-stu-id="f36e6-130">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="f36e6-131">Om det finns fel som inte är viktiga att fixa kan du välja dem och sedan välja **hoppa över val**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-131">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="f36e6-132">Om du har artiklar som ingår i en struktur kan du behöva migrera flera gånger om det ursprungliga objektet inte skapas innan alla varianter som refererar till den.</span><span class="sxs-lookup"><span data-stu-id="f36e6-132">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="f36e6-133">Om en artikelvariant skapas först blir kan referensen till det ursprungliga objektet orsaka ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="f36e6-133">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="f36e6-134">Kontrollera data efter migrering</span><span class="sxs-lookup"><span data-stu-id="f36e6-134">Verifying Data After Migrating</span></span> 
<span data-ttu-id="f36e6-135">Om du vill kontrollera att informationen överförs på rätt sätt kan du titta på följande sidor i C5 och [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f36e6-135">If you want to verify that your data migrated correctly, you can look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="f36e6-136">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="f36e6-136">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="f36e6-137">Kundtransaktioner</span><span class="sxs-lookup"><span data-stu-id="f36e6-137">Customer Entries</span></span>| <span data-ttu-id="f36e6-138">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="f36e6-138">General Journals</span></span>|
|<span data-ttu-id="f36e6-139">Leverantörstransaktioner</span><span class="sxs-lookup"><span data-stu-id="f36e6-139">Vendor Entries</span></span>| <span data-ttu-id="f36e6-140">Redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="f36e6-140">General Journals</span></span>|
|<span data-ttu-id="f36e6-141">Artikeltransaktioner</span><span class="sxs-lookup"><span data-stu-id="f36e6-141">Item Entries</span></span>| <span data-ttu-id="f36e6-142">Artikeljournaler</span><span class="sxs-lookup"><span data-stu-id="f36e6-142">Item Journals</span></span>|

<span data-ttu-id="f36e6-143">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kallas journalen för migrerade data för **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-143">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span> 

## <a name="stopping-data-migration"></a><span data-ttu-id="f36e6-144">Stoppa datamigrering</span><span class="sxs-lookup"><span data-stu-id="f36e6-144">Stopping Data Migration</span></span>
<span data-ttu-id="f36e6-145">Du kan förhindra migrering av data genom att välja **Stoppa alla migreringar**.</span><span class="sxs-lookup"><span data-stu-id="f36e6-145">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="f36e6-146">Om du gör det kommer alla väntande migreringar också stoppas.</span><span class="sxs-lookup"><span data-stu-id="f36e6-146">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="f36e6-147">Se även</span><span class="sxs-lookup"><span data-stu-id="f36e6-147">See Also</span></span>
<span data-ttu-id="f36e6-148">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="f36e6-148">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="f36e6-149">[Välkommen till [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="f36e6-149">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

