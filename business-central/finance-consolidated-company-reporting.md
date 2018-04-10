---
title: "Konsolidera data från flera företag | Microsoft Docs"
description: "Få en översikt av den ekonomiska situationen i ditt företag."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 07/14/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9309868cbcee8fb969c318acfb6ce8844e78b687
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---

# <a name="consolidating-financial-data-from-multiple-companies"></a><span data-ttu-id="5de7f-103">Konsolidera ekonomiska data från flera företag</span><span class="sxs-lookup"><span data-stu-id="5de7f-103">Consolidating Financial Data from Multiple Companies</span></span>
<span data-ttu-id="5de7f-104">Om du har fler än ett företag i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan rapporten Konsoliderad råbalans i rollcentret Revisor ge dig en översikt av hela verksamheten.</span><span class="sxs-lookup"><span data-stu-id="5de7f-104">If you have more than one company in [!INCLUDE[d365fin](includes/d365fin_md.md)], the Consolidated Trial Balance report on the Accountant Role Center can give you an overview of the financial health of your overall business.</span></span>  

<span data-ttu-id="5de7f-105">Rapporten kombinerar redovisningstransaktioner från var och ett av företagen i ett nytt företag som du skapar för att innehålla konsoliderade data.</span><span class="sxs-lookup"><span data-stu-id="5de7f-105">The report combines general ledger entries from each of your companies in a new company that you create to contain the consolidated data.</span></span> <span data-ttu-id="5de7f-106">Detta företag kallas normalt för "det konsoliderade företaget".</span><span class="sxs-lookup"><span data-stu-id="5de7f-106">This company is typically referred to as the "consolidated company".</span></span> <span data-ttu-id="5de7f-107">Det konsoliderade företaget är bara en behållare för konsoliderade data och saknar levande affärsdata.</span><span class="sxs-lookup"><span data-stu-id="5de7f-107">The consolidated company is just a container for the consolidated data, and does not have any live business data.</span></span> <span data-ttu-id="5de7f-108">Företagen som du inkluderar i det konsoliderade företaget blir **Affärsenheter** i rapporten.</span><span class="sxs-lookup"><span data-stu-id="5de7f-108">The companies that you include in the consolidated company become **Business Units** in the report.</span></span>

<span data-ttu-id="5de7f-109">Att konsolidera ekonomiska data kan vara särskilt användbart i samband med koncerninterna processer.</span><span class="sxs-lookup"><span data-stu-id="5de7f-109">Consolidating financial data may especially be relevant in connection with intercompany processes.</span></span> <span data-ttu-id="5de7f-110">Mer information finns i [Hantera koncerninterna transaktioner](intercompany-manage.md).</span><span class="sxs-lookup"><span data-stu-id="5de7f-110">For more information, see [Managing Intercompany Transactions](intercompany-manage.md).</span></span>

<span data-ttu-id="5de7f-111">Du kan konsolidera:</span><span class="sxs-lookup"><span data-stu-id="5de7f-111">You can consolidate:</span></span>  

* <span data-ttu-id="5de7f-112">Genom företag med olika kontoplaner.</span><span class="sxs-lookup"><span data-stu-id="5de7f-112">Across companies that have different charts of accounts.</span></span>  
* <span data-ttu-id="5de7f-113">Företag som använder olika räkenskapsår och olika valutor.</span><span class="sxs-lookup"><span data-stu-id="5de7f-113">Companies that use different fiscal years and different currencies.</span></span>  
* <span data-ttu-id="5de7f-114">Antingen hela beloppet eller en procentandel av ett företags finansiella information</span><span class="sxs-lookup"><span data-stu-id="5de7f-114">Either the full amount or a percentage of a company's financial information</span></span>
* <span data-ttu-id="5de7f-115">Med hjälp av olika valutakurser på enskilda redovisningskonton</span><span class="sxs-lookup"><span data-stu-id="5de7f-115">Using different currency exchange rates in individual G/L accounts</span></span>

<span data-ttu-id="5de7f-116">Det finns två sätt att ställa in rapporten beroende på hur komplicerad ditt företag är:</span><span class="sxs-lookup"><span data-stu-id="5de7f-116">Depending on the complexity of your businesses, there are two ways to set up the report:</span></span>

* <span data-ttu-id="5de7f-117">Om du inte behöver avancerade inställningar, exempelvis med ett företag som du bara har en del av, kan du använda den assisterade konfigurationen **Företagskonsolidering** för att snabbt skapa en konsolidering.</span><span class="sxs-lookup"><span data-stu-id="5de7f-117">If you don't need advanced settings, such as including a company that you only own part of, you can use the **Company Consolidation** assisted setup guide to quickly set up a consolidation.</span></span> <span data-ttu-id="5de7f-118">Guiden hjälper dig att följa de grundläggande stegen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-118">The guide helps you through the basic steps.</span></span>
* <span data-ttu-id="5de7f-119">Om du behöver mer avancerade inställningar kan du ställa in det konsoliderade företaget och koncernföretagen själv.</span><span class="sxs-lookup"><span data-stu-id="5de7f-119">If you do need more advanced settings, you can set up the consolidated company and business units yourself.</span></span>

## <a name="to-do-a-simple-consolidation-setup"></a><span data-ttu-id="5de7f-120">Om du vill ställa in en enkel konsolidering</span><span class="sxs-lookup"><span data-stu-id="5de7f-120">To do a simple consolidation setup</span></span>
<span data-ttu-id="5de7f-121">Om din konsolidering är enkel, till exempel eftersom du äger de koncernföretag som ska konsolideras helt, kommer den assisterade konfigurationen **Företagskonsolidering** att hjälpa dig med följande steg:</span><span class="sxs-lookup"><span data-stu-id="5de7f-121">If your consolidation is straightforward, for example because you wholly-own the business units to consolidate, the **Company Consolidation** assisted setup guide will help you through the following steps:</span></span>

* <span data-ttu-id="5de7f-122">Välj om du vill skapa ett nytt konsoliderat företag eller om du vill konsolidera data i ett företag som du har skapat för konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-122">Choose whether to create a new consolidated company, or whether to consolidate the data in a company that you have already created for the consolidation.</span></span> <span data-ttu-id="5de7f-123">Företaget bör inte innehålla transaktioner.</span><span class="sxs-lookup"><span data-stu-id="5de7f-123">The company should not contain transactions.</span></span>
* <span data-ttu-id="5de7f-124">Förhandsgranska resultatet.</span><span class="sxs-lookup"><span data-stu-id="5de7f-124">Preview the results.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="5de7f-125"> verifierar att huvuddata och transaktioner kan överföras till det konsoliderade företaget.</span><span class="sxs-lookup"><span data-stu-id="5de7f-125"> verifies that the master data and transactions can be successfully transferred to the consolidated company.</span></span>

<span data-ttu-id="5de7f-126">Så här använder du den assisterade konfigurationsguiden:</span><span class="sxs-lookup"><span data-stu-id="5de7f-126">To use the assisted setup guide, follow these steps:</span></span>

1. <span data-ttu-id="5de7f-127">I rollcentret **Revisor** väljer du åtgärden **Assisterad konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-127">On the **Accountant** Role Center, choose the **Assisted Setup** action.</span></span>
2. <span data-ttu-id="5de7f-128">Välj **Ställ in konsolideringsrapportering** och slutför sedan varje steg i den assisterade konfigurationsguiden.</span><span class="sxs-lookup"><span data-stu-id="5de7f-128">Choose **Set up consolidation reporting**, and then complete each step in the assisted setup guide.</span></span>

## <a name="to-do-an-advanced-consolidation-setup"></a><span data-ttu-id="5de7f-129">Så här gör du en avancerad konsolideringskonfiguration</span><span class="sxs-lookup"><span data-stu-id="5de7f-129">To do an advanced consolidation setup</span></span>
<span data-ttu-id="5de7f-130">Om du behöver mer avancerade inställningar för en konsolidering kan du konfigurera konsolideringen manuellt.</span><span class="sxs-lookup"><span data-stu-id="5de7f-130">If you need more advanced settings for your consolidation, you can set up consolidation manually.</span></span> <span data-ttu-id="5de7f-131">Till exempel om du har kunder som du endast delvis äger eller om du har kunder som du inte vill inkludera i konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-131">For example, if you have companies that you own only partially, or you have companies that you don’t want to include in the consolidation.</span></span> <span data-ttu-id="5de7f-132">Du kan lägga upp det konsoliderade företaget i en databas på samma sätt som du lägger upp andra företag.</span><span class="sxs-lookup"><span data-stu-id="5de7f-132">You set up the consolidated company in the say way that you set up other companies.</span></span> <span data-ttu-id="5de7f-133">Mer information finns i [Komma igång med att göra affärer](ui-get-ready-business.md).</span><span class="sxs-lookup"><span data-stu-id="5de7f-133">For more information, see [Getting Ready for Doing Business](ui-get-ready-business.md).</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="5de7f-134"> låter dig lägga upp en lista över företag som ska konsolideras, verifiera redovisningsinformation innan du konsoliderar den, importera filer och generera konsolideringsrapporter.</span><span class="sxs-lookup"><span data-stu-id="5de7f-134"> lets you set up a list of companies to consolidate, verify the accounting data before you consolidate it, import files, and generate consolidation reports.</span></span>  

1. <span data-ttu-id="5de7f-135">Logga in på det konsoliderade företaget.</span><span class="sxs-lookup"><span data-stu-id="5de7f-135">Sign in to the consolidated company.</span></span>
2. <span data-ttu-id="5de7f-136">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Affärsenheter** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5de7f-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Business Units**, and then choose the related link.</span></span>  
3. <span data-ttu-id="5de7f-137">Välj **Ny** och fyll sedan i relevanta fält.</span><span class="sxs-lookup"><span data-stu-id="5de7f-137">Choose **New**, and then fill in the required fields.</span></span>  

<span data-ttu-id="5de7f-138">Om en utländsk valuta används för koncernföretaget måste du ange vilken valutakurs som ska användas vid konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-138">If your business unit uses a foreign currency, you must specify the exchange rate to use in the consolidation.</span></span> <span data-ttu-id="5de7f-139">Dessutom måste du ange konsolideringsinformation på koncernföretagets redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="5de7f-139">You must also enter consolidation information about the business unit's general ledger accounts.</span></span> <span data-ttu-id="5de7f-140">De här processerna beskrivs i följande avsnitt.</span><span class="sxs-lookup"><span data-stu-id="5de7f-140">These processes are described in the following sections.</span></span>

### <a name="to-prepare-general-ledger-accounts-for-consolidation"></a><span data-ttu-id="5de7f-141">Så här förbereder du redovisningskonton för konsolidering</span><span class="sxs-lookup"><span data-stu-id="5de7f-141">To prepare general ledger accounts for consolidation</span></span>
<span data-ttu-id="5de7f-142">Om kontoplanen i affärsenheten skiljer sig från det konsoliderade företaget måste du förbereda redovisningskonton för konsolidering.</span><span class="sxs-lookup"><span data-stu-id="5de7f-142">If the chart of accounts in the business unit differs from the consolidated company, you must prepare general ledger accounts for consolidation.</span></span> <span data-ttu-id="5de7f-143">Du kan ange vilka konton som ska bokföra debet- och kreditbelopp och metoden du använder för att översätta valutor i det konsoliderade företaget.</span><span class="sxs-lookup"><span data-stu-id="5de7f-143">You can specify the accounts to post debits and credits to, and the method to use to translate currencies in the consolidated company.</span></span> <span data-ttu-id="5de7f-144">Detta är till exempel användbart om du kör rapporten ofta.</span><span class="sxs-lookup"><span data-stu-id="5de7f-144">For example, this is useful if you frequently run the report.</span></span>

1. <span data-ttu-id="5de7f-145">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5de7f-145">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5de7f-146">Öppna kortet för kontot och fyll sedan i fälten på snabbfliken **konsolidering**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-146">Open the card for the account, and then fill in the fields on the **Consolidation** FastTab.</span></span>

### <a name="to-specify-exchange-rates-for-consolidations"></a><span data-ttu-id="5de7f-147">Så här anger du valutakurs för konsolidering</span><span class="sxs-lookup"><span data-stu-id="5de7f-147">To specify exchange rates for consolidations</span></span>
<span data-ttu-id="5de7f-148">Om en affärsenhet har en annan valuta än det konsoliderade företaget, måste du ange valutakurser för metoder för varje konto innan du konsoliderar.</span><span class="sxs-lookup"><span data-stu-id="5de7f-148">If a business unit uses a different currency than the consolidated company, you must specify exchange rate methods for each account before you consolidate.</span></span> <span data-ttu-id="5de7f-149">För varje konto bestämmer innehållet i **Konsoliderad omräkningsmetod** valutakursen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-149">For each account, the content of the **Consol. Translation Method** field determines the exchange rate.</span></span> <span data-ttu-id="5de7f-150">På varje affärsenhetskort, i fältet **Valutakurstabell** anger du om konsolideringen ska använda valutakurser från affärsenhetsföretaget eller det konsoliderade företaget.</span><span class="sxs-lookup"><span data-stu-id="5de7f-150">On each business unit card, in the **Currency Exchange Rate Table** field, you specify whether consolidation will use exchange rates from the business unit or the consolidated company.</span></span> <span data-ttu-id="5de7f-151">Om du använder valutakurser från det konsoliderade företaget kan du ändra valutakurserna för en affärsenhet.</span><span class="sxs-lookup"><span data-stu-id="5de7f-151">If you use exchange rates from the consolidated company, you can change the exchange rates for a business unit.</span></span> <span data-ttu-id="5de7f-152">För affärsenheter, om fältet **Valutakurstabell** innehåller **Lokal** kan du ändra valutakursen från affärsenhetskortet.</span><span class="sxs-lookup"><span data-stu-id="5de7f-152">For business units, if the **Currency Exchange Rate Table** field on the business unit card contains **Local**, you can change the exchange rate from the business unit card.</span></span> <span data-ttu-id="5de7f-153">Valutakurserna kopieras från tabellen **Valutakurs**, men du kan ändra dem före konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-153">The exchange rates are copied from the **Currency Exchange Rate** table, but you can change them before consolidating.</span></span>

<span data-ttu-id="5de7f-154">Följande tabell beskriver valutakursmetoderna som du kan använda för konton.</span><span class="sxs-lookup"><span data-stu-id="5de7f-154">The following table describes the exchange rate methods you can use for accounts.</span></span>

|<span data-ttu-id="5de7f-155">Växlingskurs</span><span class="sxs-lookup"><span data-stu-id="5de7f-155">Exchange rate</span></span> | <span data-ttu-id="5de7f-156">Normal användning</span><span class="sxs-lookup"><span data-stu-id="5de7f-156">Typical use</span></span> |
|---|---|
|<span data-ttu-id="5de7f-157">Genomsnittskurs (manuell)</span><span class="sxs-lookup"><span data-stu-id="5de7f-157">Average Rate (Manual)</span></span> | <span data-ttu-id="5de7f-158">Du kan beräkna genomsnittskurs manuellt för den period som ska konsolideras.</span><span class="sxs-lookup"><span data-stu-id="5de7f-158">You manually calculate the average rate for the period to consolidate.</span></span> <span data-ttu-id="5de7f-159">Beräkna genomsnittet antingen som ett aritmetiskt genomsnitt eller som en bästa uppskattning och ange resultatet för varje affärsenhet.</span><span class="sxs-lookup"><span data-stu-id="5de7f-159">Calculate the average either as an arithmetic average or as a best estimate, and specify the result for each business unit.</span></span> <span data-ttu-id="5de7f-160">Används för resultaträkningskonton.</span><span class="sxs-lookup"><span data-stu-id="5de7f-160">Used for income statement accounts.</span></span>|
|<span data-ttu-id="5de7f-161">Slutkurs</span><span class="sxs-lookup"><span data-stu-id="5de7f-161">Closing Rate</span></span> | <span data-ttu-id="5de7f-162">Används för balansräkningskonton.</span><span class="sxs-lookup"><span data-stu-id="5de7f-162">Used for balance sheet accounts.</span></span>|
|<span data-ttu-id="5de7f-163">Senaste slutkurs</span><span class="sxs-lookup"><span data-stu-id="5de7f-163">Last Closing Rate</span></span> | <span data-ttu-id="5de7f-164">Kursen som var giltig på den utländska valutamarknaden vid den tidpunkt då balansräkningen eller resultaträkningen förbereds för.</span><span class="sxs-lookup"><span data-stu-id="5de7f-164">The rate that was valid in the foreign exchange market on the date for which the balance sheet or income statement is being prepared.</span></span> <span data-ttu-id="5de7f-165">Du registrerar denna kurs för varje affärsenhet.</span><span class="sxs-lookup"><span data-stu-id="5de7f-165">You enter this rate for each business unit.</span></span> <span data-ttu-id="5de7f-166">Används för balansräkningskonton.</span><span class="sxs-lookup"><span data-stu-id="5de7f-166">Used for balance sheet accounts.</span></span>|
|<span data-ttu-id="5de7f-167">Historisk kurs</span><span class="sxs-lookup"><span data-stu-id="5de7f-167">Historical Rate</span></span> | <span data-ttu-id="5de7f-168">Valutakursen som användes när transaktionen genomfördes.</span><span class="sxs-lookup"><span data-stu-id="5de7f-168">The exchange rate that was valid when the transaction occurred.</span></span>|
|<span data-ttu-id="5de7f-169">Sammansatt kurs</span><span class="sxs-lookup"><span data-stu-id="5de7f-169">Composite Rate</span></span> | <span data-ttu-id="5de7f-170">Den aktuella perioden omräknas med den genomsnittliga kursen och läggs till det tidigare registrerade saldot i det konsoliderade företaget.</span><span class="sxs-lookup"><span data-stu-id="5de7f-170">The current period amounts are translated at the average rate and added to the previously recorded balance in the consolidated company.</span></span> <span data-ttu-id="5de7f-171">Den här metoden används vanligtvis för konton för balanserade vinstmedel eftersom de innehåller belopp från olika perioder och är därför en summa av belopp som omräknats med olika växelkurser.</span><span class="sxs-lookup"><span data-stu-id="5de7f-171">This method is typically used for retained earnings accounts because they include amounts from different periods and are therefore a composite of amounts translated with different exchange rates.</span></span>|
|<span data-ttu-id="5de7f-172">Aktiekurs</span><span class="sxs-lookup"><span data-stu-id="5de7f-172">Equity Rate</span></span> | <span data-ttu-id="5de7f-173">Detta liknar **Sammansatt**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-173">This is similar to **Composite**.</span></span> <span data-ttu-id="5de7f-174">Differenser bokförs på olika redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="5de7f-174">Differences are posted to separate general ledger accounts.</span></span>|   

<span data-ttu-id="5de7f-175">Om du vill ange valutakurs för affärsenheter gör du följande:</span><span class="sxs-lookup"><span data-stu-id="5de7f-175">To specify exchange rates for business units, follow these steps:</span></span>

1. <span data-ttu-id="5de7f-176">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Affärsenheter** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5de7f-176">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Business Units**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5de7f-177">På sidan **Affärsenhetslista** väljer du affärsenhet och sedan åtgärden **Genomsnittskurs (manuell)**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-177">On the **Business Unit List** page, choose the business unit, and then choose the **Average Rate (Manual)** action.</span></span>   
3. <span data-ttu-id="5de7f-178">På sidan **Ändra valutakurser** har innehållet i fältet **Relationsvalutakurs** kopierats från tabellen **Valutakurs**, men det går att ändra värdet.</span><span class="sxs-lookup"><span data-stu-id="5de7f-178">On the **Change Exchange Rate** page, the contents of the **Relational Exch. Rate** field have been copied from the **Currency Exchange Rate** table, but you can modify them.</span></span> <span data-ttu-id="5de7f-179">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="5de7f-179">Close the page.</span></span>  
4. <span data-ttu-id="5de7f-180">Välj åtgärden **Slutkurs**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-180">Choose the **Closing Rate** action.</span></span>  
5. <span data-ttu-id="5de7f-181">På fältet **Relations- valutakurs belopp** anger du valutakursen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-181">In the **Relational Exch. Rate Amount** field, enter the exchange rate.</span></span>

<!-- ### To include or exclude dimensions

COMMENTING THIS OUT BECAUSE i CANNOT REPRODUCE THE SETTINGS. tHERE IS NO CONSOLIDATION CODE FIELD ON DIMENSIONS OR DIMENSIOIN VALUES.

You can consolidate dimension information and general ledger accounts, as follows:

* To exclude dimension information in the consolidation, leave the **Consolidation Code** field blank, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports described later in this topic.
* To include dimension information in the consolidation, leave the **Consolidation Code** field blank. However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.
* To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code**. -->

### <a name="to-exclude-a-company-from-consolidation"></a><span data-ttu-id="5de7f-182">Om du vill exkludera ett företag från konsolidering</span><span class="sxs-lookup"><span data-stu-id="5de7f-182">To exclude a company from consolidation</span></span>
<span data-ttu-id="5de7f-183">Om du inte vill inkludera en affärsenhet i konsolideringen kan du exkludera den.</span><span class="sxs-lookup"><span data-stu-id="5de7f-183">If you do not want to include a business unit in the consolidation, you can exclude it.</span></span> <span data-ttu-id="5de7f-184">Om du vill göra det, öppnar du affärsenhetskortet och avmarkerar kryssrutan **konsolidera**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-184">To do that, go to the business unit card, and clear the **Consolidate** check box.</span></span>

### <a name="to-include-a-partially-owned-company-in-consolidation"></a><span data-ttu-id="5de7f-185">Om du vill inkludera ett delvis ägt företag i konsolidering</span><span class="sxs-lookup"><span data-stu-id="5de7f-185">To include a partially-owned company in consolidation</span></span>
<span data-ttu-id="5de7f-186">Om du bara äger en del av ett företag kan inkludera en procentandel av varje transaktion som motsvarar procentandelen av det företag som du äger.</span><span class="sxs-lookup"><span data-stu-id="5de7f-186">If you own only part of a company, you can include a percentage of each transaction that corresponds to the percentage of the company you own.</span></span> <span data-ttu-id="5de7f-187">Om du äger 70 % av företaget kommer konsolideringen att innehålla 70 SEK av en faktura på 100 SEK.</span><span class="sxs-lookup"><span data-stu-id="5de7f-187">For example, if you own 70% of the company, consolidation will include $70 of an invoice for $100.</span></span> <span data-ttu-id="5de7f-188">Om du vill ange hur stor procentandel av företaget du äger går du till affärsenhetskortet och anger procentsatsen i fältet **konsolideringsgrad %**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-188">To specify the percentage of the company you own, go to the business unit card, and enter the percentage in the **Consolidation %** field.</span></span>  

### <a name="to-test-the-data-before-you-consolidate"></a><span data-ttu-id="5de7f-189">Så här testar du data före konsolidering</span><span class="sxs-lookup"><span data-stu-id="5de7f-189">To test the data before you consolidate</span></span>
<span data-ttu-id="5de7f-190">Du kan testa data innan du överför den till det konsoliderade företaget.</span><span class="sxs-lookup"><span data-stu-id="5de7f-190">You can test your data before you transfer it to the consolidated company.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="5de7f-191"> tittar efter skillnader i information som finns i affärsenheterna och det konsoliderade företaget.</span><span class="sxs-lookup"><span data-stu-id="5de7f-191"> looks for differences in the information in the business units and the consolidated company.</span></span> <span data-ttu-id="5de7f-192">Till exempel om kontonummer eller dimensionskoder är olika.</span><span class="sxs-lookup"><span data-stu-id="5de7f-192">For example, whether account numbers or dimension codes are different.</span></span> <span data-ttu-id="5de7f-193">Du måste åtgärda felen innan du kan köra rapporten.</span><span class="sxs-lookup"><span data-stu-id="5de7f-193">You must correct errors before you can run the report.</span></span> <span data-ttu-id="5de7f-194">Du kan testa en databas, eller om du importerar data från en XML-fil kan du testa filen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-194">You can test the database or, if you are importing data from an XML file, you can test the file.</span></span>   

1. <span data-ttu-id="5de7f-195">Öppna det konsoliderade företaget.</span><span class="sxs-lookup"><span data-stu-id="5de7f-195">Open the consolidated company.</span></span>  
2. <span data-ttu-id="5de7f-196">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Affärsenheter** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5de7f-196">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Business Units**, and then choose the related link.</span></span>  
3. <span data-ttu-id="5de7f-197">Gör något av följande:</span><span class="sxs-lookup"><span data-stu-id="5de7f-197">Do one of the following:</span></span>  

    * <span data-ttu-id="5de7f-198">Testa en fil genom att välja åtgärden **testa fil**, ange namnet på filen och välj sedan **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-198">To test a file, choose the **Test File** action, enter the name of the file to test, and then choose **Print**.</span></span>  
    * <span data-ttu-id="5de7f-199">Om du vill testa en databas väljer du **Testa databas**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-199">To test the database, choose **Test Database**.</span></span>  

## <a name="to-run-the-consolidation"></a><span data-ttu-id="5de7f-200">Så här kör du konsolideringen</span><span class="sxs-lookup"><span data-stu-id="5de7f-200">To run the consolidation</span></span>
<span data-ttu-id="5de7f-201">När du har testat data kan du starta konsolideringen överför den till det konsoliderade företaget.</span><span class="sxs-lookup"><span data-stu-id="5de7f-201">After you have tested the data, you can transfer it to the consolidated company.</span></span>  

1. <span data-ttu-id="5de7f-202">Logga in på det konsoliderade företaget.</span><span class="sxs-lookup"><span data-stu-id="5de7f-202">Sign in to the consolidated company.</span></span>  
2. <span data-ttu-id="5de7f-203">I rollcentret **Revisor** väljer du åtgärden **Kör konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-203">On the **Accountant Role Center**, choose the **Run Consolidation** action.</span></span>  
3. <span data-ttu-id="5de7f-204">Fyll i relevanta fält.</span><span class="sxs-lookup"><span data-stu-id="5de7f-204">Fill in the required fields.</span></span>  
4. <span data-ttu-id="5de7f-205">I fältet **Var** väljer du **företagsnamn** och väljer sedan det konsoliderade företaget i fältet **Är**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-205">In the **Where** field, choose **Company Name**, and then choose the consolidated company in the **is** field.</span></span>  

## <a name="to-export-and-import-consolidated-data-between-databases"></a><span data-ttu-id="5de7f-206">Exportera och importera konsoliderade data mellan databaser</span><span class="sxs-lookup"><span data-stu-id="5de7f-206">To export and import consolidated data between databases</span></span>
<span data-ttu-id="5de7f-207">Om data för en affärsenheter är i en annan databas måste du exportera konsolideringsdata till en fil innan du kan inkludera den i konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-207">If data for a business unit is in another database, you must export the data to a file before you can include it in the consolidation.</span></span> <span data-ttu-id="5de7f-208">Varje företag måste exporteras var för sig.</span><span class="sxs-lookup"><span data-stu-id="5de7f-208">Each company must be exported separately.</span></span> <span data-ttu-id="5de7f-209">I detta avseende används batch-jobbet **Exportera konsolidering**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-209">For this purpose, use the **Export Consolidation** batch job.</span></span>  

<span data-ttu-id="5de7f-210">När du kör batch-jobbet körs bearbetas alla poster i redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="5de7f-210">After you run the batch job, all entries in general ledger accounts are processed.</span></span> <span data-ttu-id="5de7f-211">För varje kombination av valda dimensioner och datum summeras och exporteras innehållet i fälten **Belopp** för posterna.</span><span class="sxs-lookup"><span data-stu-id="5de7f-211">For every combination of selected dimensions and date, the contents of the entries' **Amount** fields are totaled and exported.</span></span> <span data-ttu-id="5de7f-212">Nästa kombination av valda dimensioner och datum med samma kontonummer bearbetas, sedan bearbetas kombinationerna med nästa kontonummer och så vidare.</span><span class="sxs-lookup"><span data-stu-id="5de7f-212">The next combination of selected dimensions and date with the same account number is processed, then the combinations in the next account number are processed, and so on.</span></span>  

<span data-ttu-id="5de7f-213">De exporterade posterna innehåller följande fält: **Kontonr**, **Bokföringsdatum** och **Belopp**.</span><span class="sxs-lookup"><span data-stu-id="5de7f-213">The exported entries contain the following fields: **Account No.**, **Posting Date**, and **Amount**.</span></span> <span data-ttu-id="5de7f-214">Om även dimensionsinformation har exporterats inkluderas dimensionskoder och dimensionsvärden.</span><span class="sxs-lookup"><span data-stu-id="5de7f-214">If dimensions information was also exported, dimension codes and dimension values are also included.</span></span>  

1. <span data-ttu-id="5de7f-215">För varje exporterad rad, om summan av fälten **Belopp** är ett debetbelopp, kommer kontonumret som har angetts i affärsenhetens fält **Debetkonto konsolidering** att exporteras till raden.</span><span class="sxs-lookup"><span data-stu-id="5de7f-215">For each exported line, if the total of the **Amount** fields is a debit, the account number that is set up in the business unit's **Consol. Debit Acc.** field is exported to the line.</span></span> <span data-ttu-id="5de7f-216">Om summan är ett kreditbelopp, kommer motsvarande nummer i fältet **Kreditkonto konsolid.** att exporteras till raden.</span><span class="sxs-lookup"><span data-stu-id="5de7f-216">If the total is a credit, the corresponding number in the **Consol. Credit Acc.** field is exported to the line.</span></span>  
2. <span data-ttu-id="5de7f-217">Det datum som används för varje exporterad rad är antingen periodens slutdatum eller, om överföringen utförs varje dag, det exakta datumet för beräkningen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-217">The date used for each exported line is either the period's ending date or, if the transfer occurs each day, the exact date of the calculation.</span></span>  
3. <span data-ttu-id="5de7f-218">Det dimensionsvärde som exporteras för transaktionen är det konsoliderade företagets dimensionsvärde som har lagts upp i fältet **Konsolideringskod** för det dimensionsvärdet.</span><span class="sxs-lookup"><span data-stu-id="5de7f-218">The dimension value exported for the entry will be the consolidated company dimension value that is set up in the **Consolidation Code** field for that dimension value.</span></span> <span data-ttu-id="5de7f-219">Om inget dimensionsvärde har angetts för det konsoliderade företaget i fältet **Konsolideringskod** för det dimensionsvärdet, exporteras själva dimensionsvärdet till raden.</span><span class="sxs-lookup"><span data-stu-id="5de7f-219">If no consolidated company dimension value has been entered in the **Consolidated Code** field for that dimension value, the dimension value itself will be exported to the line.</span></span>   
4. <span data-ttu-id="5de7f-220">XML-filerna innehåller dessutom valutakurserna i konsolideringsperioden.</span><span class="sxs-lookup"><span data-stu-id="5de7f-220">The XML files also contain the currency exchange rates in the consolidation period.</span></span> <span data-ttu-id="5de7f-221">Dessa kurser placeras i ett separat avsnitt i början av filen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-221">These rates are included in a separate section at the beginning of the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="5de7f-222">Se även</span><span class="sxs-lookup"><span data-stu-id="5de7f-222">See Also</span></span>
[<span data-ttu-id="5de7f-223">Hantera koncerninterna transaktioner</span><span class="sxs-lookup"><span data-stu-id="5de7f-223">Managing Intercompany Transactions</span></span>](intercompany-manage.md)  
<span data-ttu-id="5de7f-224">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5de7f-224">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5de7f-225">Exportera affärsdata till Excel</span><span class="sxs-lookup"><span data-stu-id="5de7f-225">Exporting Your Business Data to Excel</span></span>](about-export-data.md)
