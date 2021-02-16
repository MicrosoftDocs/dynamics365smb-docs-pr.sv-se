---
title: Så här skapar du ett nytt företag | Microsoft Docs
description: Tabeller och sidor skapas i syfte att kunna använda RapidStart Services, men de innehåller inga data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7583837e515a4fd5fb415fe1b482512e7edf6b5a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754010"
---
# <a name="create-a-new-company"></a><span data-ttu-id="bc8af-103">Skapa ett nytt företag</span><span class="sxs-lookup"><span data-stu-id="bc8af-103">Create a New Company</span></span>
<span data-ttu-id="bc8af-104">Innan du kan använda RapidStart Services för [!INCLUDE[prod_short](includes/prod_short.md)] måste du först skapa ett nytt företag för vilket du vill genomföra en kundimplementering.</span><span class="sxs-lookup"><span data-stu-id="bc8af-104">To use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="bc8af-105">När du skapar ett nytt företag skapas standardtabeller och sidor för [!INCLUDE[prod_short](includes/prod_short.md)] men det inte finns några data i dem.</span><span class="sxs-lookup"><span data-stu-id="bc8af-105">When you create a new company, the standard [!INCLUDE[prod_short](includes/prod_short.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="bc8af-106">Du kan dessutom tillämpa specifika inställningsdata till företaget, när du har initialiserat det.</span><span class="sxs-lookup"><span data-stu-id="bc8af-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="bc8af-107">Information finns i ett konfigurationspaket, en .rapidstart-fil, med innehållet i ett komprimerat format.</span><span class="sxs-lookup"><span data-stu-id="bc8af-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="bc8af-108">Exempelkonfigurationspaket, inklusive lands-/regionspecifika filer, ingår i demonstrationsföretaget CRONUS.</span><span class="sxs-lookup"><span data-stu-id="bc8af-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="bc8af-109">Använd följande procedurer för att använda exempelkonfigurationspaketet med ett nytt företag.</span><span class="sxs-lookup"><span data-stu-id="bc8af-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="bc8af-110">Om du vill använda exempelkonfigurationspaket BASICCONFIG</span><span class="sxs-lookup"><span data-stu-id="bc8af-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="bc8af-111">Öppna företaget CRONUS Sverige AB.</span><span class="sxs-lookup"><span data-stu-id="bc8af-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="bc8af-112">Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="bc8af-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="bc8af-113">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Konfigurationspaket** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bc8af-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="bc8af-114">Välj paketet BASICCONFIG i listan och välj sedan åtgärden **Exportera paket**.</span><span class="sxs-lookup"><span data-stu-id="bc8af-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="bc8af-115">Använd följande procedur för att skapa ett nytt företag och använd BASICCONFIG-paketet som en del av processen.</span><span class="sxs-lookup"><span data-stu-id="bc8af-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="bc8af-116">Så här skapar du ett nytt företag:</span><span class="sxs-lookup"><span data-stu-id="bc8af-116">To create a new company</span></span>  
1. <span data-ttu-id="bc8af-117">Skapa ett nytt företag.</span><span class="sxs-lookup"><span data-stu-id="bc8af-117">Create a new company.</span></span> <span data-ttu-id="bc8af-118">Mer information finns i [Skapa nya företag i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="bc8af-118">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="bc8af-119">Du kan nu importera implementerings-rollcentret för RapidStart Services och importera det konfigurationspaket som du har exporterat från företaget CRONUS Sverige AB.</span><span class="sxs-lookup"><span data-stu-id="bc8af-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="bc8af-120">När du har skapat ett nytt företag, fylls vissa tabeller i automatiskt, även om ingen företagsmall kopplas.</span><span class="sxs-lookup"><span data-stu-id="bc8af-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="bc8af-121">Du kan till exempel granska standardkoderna för att bokföra och gruppera transaktioner på sidan **Källkod**.</span><span class="sxs-lookup"><span data-stu-id="bc8af-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="bc8af-122">Om du anger en lokal version av [!INCLUDE[prod_short](includes/prod_short.md)], ska du granska den här tabellen och överväga alla lokala språkproblem.</span><span class="sxs-lookup"><span data-stu-id="bc8af-122">If you provide a local version of [!INCLUDE[prod_short](includes/prod_short.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="bc8af-123">Om datatabeller</span><span class="sxs-lookup"><span data-stu-id="bc8af-123">About Data Tables</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)]<span data-ttu-id="bc8af-124">-datatabeller finns i två grundläggande typer: Huvud och Inställningar.</span><span class="sxs-lookup"><span data-stu-id="bc8af-124">, data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="bc8af-125">När du vill lägga upp en företagskonfiguration kan du använda dessa typer för att fokusera din konfigurationstrategi.</span><span class="sxs-lookup"><span data-stu-id="bc8af-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="bc8af-126">Huvuddatatabeller</span><span class="sxs-lookup"><span data-stu-id="bc8af-126">Master Data Tables</span></span>  
<span data-ttu-id="bc8af-127">I följande tabell visas exempel på huvuddatatabeller.</span><span class="sxs-lookup"><span data-stu-id="bc8af-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="bc8af-128">När du initialiserar ett nytt företag är de här tabellerna tomma.</span><span class="sxs-lookup"><span data-stu-id="bc8af-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="bc8af-129">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="bc8af-129">Table No.</span></span>|<span data-ttu-id="bc8af-130">Tabellnamn</span><span class="sxs-lookup"><span data-stu-id="bc8af-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="bc8af-131">15</span><span class="sxs-lookup"><span data-stu-id="bc8af-131">15</span></span>|<span data-ttu-id="bc8af-132">Redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="bc8af-132">G/L Account</span></span>|  
|<span data-ttu-id="bc8af-133">18</span><span class="sxs-lookup"><span data-stu-id="bc8af-133">18</span></span>|<span data-ttu-id="bc8af-134">Kund</span><span class="sxs-lookup"><span data-stu-id="bc8af-134">Customer</span></span>|  
|<span data-ttu-id="bc8af-135">23</span><span class="sxs-lookup"><span data-stu-id="bc8af-135">23</span></span>|<span data-ttu-id="bc8af-136">Leverantör</span><span class="sxs-lookup"><span data-stu-id="bc8af-136">Vendor</span></span>|  
|<span data-ttu-id="bc8af-137">27</span><span class="sxs-lookup"><span data-stu-id="bc8af-137">27</span></span>|<span data-ttu-id="bc8af-138">Artikel</span><span class="sxs-lookup"><span data-stu-id="bc8af-138">Item</span></span>|  
|<span data-ttu-id="bc8af-139">5050</span><span class="sxs-lookup"><span data-stu-id="bc8af-139">5050</span></span>|<span data-ttu-id="bc8af-140">Kontakt</span><span class="sxs-lookup"><span data-stu-id="bc8af-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="bc8af-141">Inställningsdatatabeller</span><span class="sxs-lookup"><span data-stu-id="bc8af-141">Setup Data Tables</span></span>  
<span data-ttu-id="bc8af-142">I följande tabell visas exempel på inställningsdatatabeller där du registrerar inställningsinformation i konfigurationsfrågeformulär.</span><span class="sxs-lookup"><span data-stu-id="bc8af-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="bc8af-143">Tabellerna innehåller basinformation om när företaget skapas.</span><span class="sxs-lookup"><span data-stu-id="bc8af-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="bc8af-144">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="bc8af-144">Table No.</span></span>|<span data-ttu-id="bc8af-145">Tabellnamn</span><span class="sxs-lookup"><span data-stu-id="bc8af-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="bc8af-146">98</span><span class="sxs-lookup"><span data-stu-id="bc8af-146">98</span></span>|<span data-ttu-id="bc8af-147">Redovisningsinställningar</span><span class="sxs-lookup"><span data-stu-id="bc8af-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="bc8af-148">311</span><span class="sxs-lookup"><span data-stu-id="bc8af-148">311</span></span>|<span data-ttu-id="bc8af-149">Försäljningsinställningar</span><span class="sxs-lookup"><span data-stu-id="bc8af-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="bc8af-150">312</span><span class="sxs-lookup"><span data-stu-id="bc8af-150">312</span></span>|<span data-ttu-id="bc8af-151">Inköpsinställningar</span><span class="sxs-lookup"><span data-stu-id="bc8af-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="bc8af-152">313</span><span class="sxs-lookup"><span data-stu-id="bc8af-152">313</span></span>|<span data-ttu-id="bc8af-153">Lagerinställningar</span><span class="sxs-lookup"><span data-stu-id="bc8af-153">Inventory Setup</span></span>|  

<span data-ttu-id="bc8af-154">Förutom inställningsdatatabeller har [!INCLUDE[prod_short](includes/prod_short.md)] också inställningsdatatabeller som anger grundläggande information om företaget och dess affärsprocesser.</span><span class="sxs-lookup"><span data-stu-id="bc8af-154">In addition to setup data tables, [!INCLUDE[prod_short](includes/prod_short.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="bc8af-155">I följande tabell visas några av dessa.</span><span class="sxs-lookup"><span data-stu-id="bc8af-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="bc8af-156">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="bc8af-156">Table No.</span></span>|<span data-ttu-id="bc8af-157">Tabellnamn</span><span class="sxs-lookup"><span data-stu-id="bc8af-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="bc8af-158">3</span><span class="sxs-lookup"><span data-stu-id="bc8af-158">3</span></span>|<span data-ttu-id="bc8af-159">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="bc8af-159">Payment Terms</span></span>|  
|<span data-ttu-id="bc8af-160">4</span><span class="sxs-lookup"><span data-stu-id="bc8af-160">4</span></span>|<span data-ttu-id="bc8af-161">Valuta</span><span class="sxs-lookup"><span data-stu-id="bc8af-161">Currency</span></span>|  
|<span data-ttu-id="bc8af-162">6</span><span class="sxs-lookup"><span data-stu-id="bc8af-162">6</span></span>|<span data-ttu-id="bc8af-163">Kundprisgrupper</span><span class="sxs-lookup"><span data-stu-id="bc8af-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="bc8af-164">5700</span><span class="sxs-lookup"><span data-stu-id="bc8af-164">5700</span></span>|<span data-ttu-id="bc8af-165">Lagerställeenhet</span><span class="sxs-lookup"><span data-stu-id="bc8af-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="bc8af-166">Se även</span><span class="sxs-lookup"><span data-stu-id="bc8af-166">See Also</span></span>  
[<span data-ttu-id="bc8af-167">Koppla konfigurationen till nya företag</span><span class="sxs-lookup"><span data-stu-id="bc8af-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="bc8af-168">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="bc8af-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="bc8af-169">Administration</span><span class="sxs-lookup"><span data-stu-id="bc8af-169">Administration</span></span>](admin-setup-and-administration.md)
