---
title: "Så här skapar du ett nytt företag | Microsoft Docs"
description: "Tabeller och sidor skapas i syfte att kunna använda RapidStart Services, med de innehåller inga data."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 3b213e85e6b162e875a31f0ab69e3e1f4af9653f
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="create-a-new-company"></a><span data-ttu-id="f8153-103">Skapa ett nytt företag</span><span class="sxs-lookup"><span data-stu-id="f8153-103">Create a New Company</span></span>
<span data-ttu-id="f8153-104">Innan du kan använda RapidStart Services för [!INCLUDE[d365fin](includes/d365fin_md.md)] måste du först skapa ett nytt företag för vilket du vill genomföra en kundimplementering.</span><span class="sxs-lookup"><span data-stu-id="f8153-104">To use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="f8153-105">När du skapar ett nytt företag skapas standardtabeller och sidor för [!INCLUDE[d365fin](includes/d365fin_md.md)] men det inte finns några data i dem.</span><span class="sxs-lookup"><span data-stu-id="f8153-105">When you create a new company, the standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="f8153-106">Du kan dessutom tillämpa specifika inställningsdata till företaget, när du har initialiserat det.</span><span class="sxs-lookup"><span data-stu-id="f8153-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="f8153-107">Information finns i ett konfigurationspaket, en .rapidstart-fil, med innehållet i ett komprimerat format.</span><span class="sxs-lookup"><span data-stu-id="f8153-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="f8153-108">Exempelkonfigurationspaket, inklusive lands-/regionspecifika filer, ingår i demonstrationsföretaget CRONUS.</span><span class="sxs-lookup"><span data-stu-id="f8153-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="f8153-109">Använd följande procedurer för att använda exempelkonfigurationspaketet med ett nytt företag.</span><span class="sxs-lookup"><span data-stu-id="f8153-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="f8153-110">Om du vill använda exempelkonfigurationspaket BASICCONFIG</span><span class="sxs-lookup"><span data-stu-id="f8153-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="f8153-111">Öppna företaget CRONUS Sverige AB.</span><span class="sxs-lookup"><span data-stu-id="f8153-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="f8153-112">Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f8153-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="f8153-113">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationspaket** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="f8153-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="f8153-114">Välj paketet BASICCONFIG i listan och välj sedan åtgärden **Exportera paket**.</span><span class="sxs-lookup"><span data-stu-id="f8153-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="f8153-115">Använd följande procedur för att skapa ett nytt företag och använd BASICCONFIG-paketet som en del av processen.</span><span class="sxs-lookup"><span data-stu-id="f8153-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="f8153-116">Så här skapar du ett nytt företag:</span><span class="sxs-lookup"><span data-stu-id="f8153-116">To create a new company</span></span>  
1. <span data-ttu-id="f8153-117">Skapa ett nytt företag.</span><span class="sxs-lookup"><span data-stu-id="f8153-117">Create a new company.</span></span> <span data-ttu-id="f8153-118">Mer information finns i [Skapa nya företag i [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="f8153-118">For more information, see [Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="f8153-119">Du kan nu importera implementerings-rollcentret för RapidStart Services och importera det konfigurationspaket som du har exporterat från företaget CRONUS Sverige AB.</span><span class="sxs-lookup"><span data-stu-id="f8153-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="f8153-120">När du har skapat ett nytt företag, fylls vissa tabeller i automatiskt, även om ingen företagsmall kopplas.</span><span class="sxs-lookup"><span data-stu-id="f8153-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="f8153-121">Du kan till exempel granska standardkoderna för att bokföra och gruppera transaktioner i det fönstret **Källkod**.</span><span class="sxs-lookup"><span data-stu-id="f8153-121">For example, you can review the standard codes for posting and batch transactions in the **Source Code** window.</span></span> <span data-ttu-id="f8153-122">Om du anger en lokal version av [!INCLUDE[d365fin](includes/d365fin_md.md)], ska du granska den här tabellen och överväga alla lokala språkproblem.</span><span class="sxs-lookup"><span data-stu-id="f8153-122">If you provide a local version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="f8153-123">Om datatabeller</span><span class="sxs-lookup"><span data-stu-id="f8153-123">About Data Tables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f8153-124">-datatabeller finns i två grundläggande typer: Huvud och Inställningar.</span><span class="sxs-lookup"><span data-stu-id="f8153-124">, data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="f8153-125">När du vill lägga upp en företagskonfiguration kan du använda dessa typer för att fokusera din konfigurationstrategi.</span><span class="sxs-lookup"><span data-stu-id="f8153-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="f8153-126">Huvuddatatabeller</span><span class="sxs-lookup"><span data-stu-id="f8153-126">Master Data Tables</span></span>  
<span data-ttu-id="f8153-127">I följande tabell visas exempel på huvuddatatabeller.</span><span class="sxs-lookup"><span data-stu-id="f8153-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="f8153-128">När du initialiserar ett nytt företag är de här tabellerna tomma.</span><span class="sxs-lookup"><span data-stu-id="f8153-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="f8153-129">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="f8153-129">Table No.</span></span>|<span data-ttu-id="f8153-130">Tabellnamn</span><span class="sxs-lookup"><span data-stu-id="f8153-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="f8153-131">15</span><span class="sxs-lookup"><span data-stu-id="f8153-131">15</span></span>|<span data-ttu-id="f8153-132">Redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="f8153-132">G/L Account</span></span>|  
|<span data-ttu-id="f8153-133">18</span><span class="sxs-lookup"><span data-stu-id="f8153-133">18</span></span>|<span data-ttu-id="f8153-134">Kund</span><span class="sxs-lookup"><span data-stu-id="f8153-134">Customer</span></span>|  
|<span data-ttu-id="f8153-135">23</span><span class="sxs-lookup"><span data-stu-id="f8153-135">23</span></span>|<span data-ttu-id="f8153-136">Leverantör</span><span class="sxs-lookup"><span data-stu-id="f8153-136">Vendor</span></span>|  
|<span data-ttu-id="f8153-137">27</span><span class="sxs-lookup"><span data-stu-id="f8153-137">27</span></span>|<span data-ttu-id="f8153-138">Artikel</span><span class="sxs-lookup"><span data-stu-id="f8153-138">Item</span></span>|  
|<span data-ttu-id="f8153-139">5050</span><span class="sxs-lookup"><span data-stu-id="f8153-139">5050</span></span>|<span data-ttu-id="f8153-140">Kontakt</span><span class="sxs-lookup"><span data-stu-id="f8153-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="f8153-141">Inställningsdatatabeller</span><span class="sxs-lookup"><span data-stu-id="f8153-141">Setup Data Tables</span></span>  
<span data-ttu-id="f8153-142">I följande tabell visas exempel på inställningsdatatabeller där du registrerar inställningsinformation i konfigurationsfrågeformulär.</span><span class="sxs-lookup"><span data-stu-id="f8153-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="f8153-143">Tabellerna innehåller basinformation om när företaget skapas.</span><span class="sxs-lookup"><span data-stu-id="f8153-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="f8153-144">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="f8153-144">Table No.</span></span>|<span data-ttu-id="f8153-145">Tabellnamn</span><span class="sxs-lookup"><span data-stu-id="f8153-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="f8153-146">98</span><span class="sxs-lookup"><span data-stu-id="f8153-146">98</span></span>|<span data-ttu-id="f8153-147">Redovisningsinställningar</span><span class="sxs-lookup"><span data-stu-id="f8153-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="f8153-148">311</span><span class="sxs-lookup"><span data-stu-id="f8153-148">311</span></span>|<span data-ttu-id="f8153-149">Försäljningsinställningar</span><span class="sxs-lookup"><span data-stu-id="f8153-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="f8153-150">312</span><span class="sxs-lookup"><span data-stu-id="f8153-150">312</span></span>|<span data-ttu-id="f8153-151">Inköpsinställningar</span><span class="sxs-lookup"><span data-stu-id="f8153-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="f8153-152">313</span><span class="sxs-lookup"><span data-stu-id="f8153-152">313</span></span>|<span data-ttu-id="f8153-153">Lagerinställningar</span><span class="sxs-lookup"><span data-stu-id="f8153-153">Inventory Setup</span></span>|  

<span data-ttu-id="f8153-154">Förutom inställningsdatatabeller har [!INCLUDE[d365fin](includes/d365fin_md.md)] också inställningsdatatabeller som anger grundläggande information om företaget och dess affärsprocesser.</span><span class="sxs-lookup"><span data-stu-id="f8153-154">In addition to setup data tables, [!INCLUDE[d365fin](includes/d365fin_md.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="f8153-155">I följande tabell visas några av dessa.</span><span class="sxs-lookup"><span data-stu-id="f8153-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="f8153-156">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="f8153-156">Table No.</span></span>|<span data-ttu-id="f8153-157">Tabellnamn</span><span class="sxs-lookup"><span data-stu-id="f8153-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="f8153-158">3</span><span class="sxs-lookup"><span data-stu-id="f8153-158">3</span></span>|<span data-ttu-id="f8153-159">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="f8153-159">Payment Terms</span></span>|  
|<span data-ttu-id="f8153-160">4</span><span class="sxs-lookup"><span data-stu-id="f8153-160">4</span></span>|<span data-ttu-id="f8153-161">Valuta</span><span class="sxs-lookup"><span data-stu-id="f8153-161">Currency</span></span>|  
|<span data-ttu-id="f8153-162">6</span><span class="sxs-lookup"><span data-stu-id="f8153-162">6</span></span>|<span data-ttu-id="f8153-163">Kundprisgrupper</span><span class="sxs-lookup"><span data-stu-id="f8153-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="f8153-164">5700</span><span class="sxs-lookup"><span data-stu-id="f8153-164">5700</span></span>|<span data-ttu-id="f8153-165">Lagerställeenhet</span><span class="sxs-lookup"><span data-stu-id="f8153-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="f8153-166">Se även</span><span class="sxs-lookup"><span data-stu-id="f8153-166">See Also</span></span>  
[<span data-ttu-id="f8153-167">Koppla konfigurationen till nya företag</span><span class="sxs-lookup"><span data-stu-id="f8153-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="f8153-168">Konfigurera ett företag med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="f8153-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="f8153-169">Administration</span><span class="sxs-lookup"><span data-stu-id="f8153-169">Administration</span></span>](admin-setup-and-administration.md)

