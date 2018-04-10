---
title: "Underhålla anläggningstillgångar | Microsoft Docs"
description: "Du registrerr en underhållspost av reparationer och service för en anläggningstillgång."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 62addbd6bcf11f640749b395efc9d87550c8ee45
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="maintain-fixed-assets"></a><span data-ttu-id="64272-103">Underhålla anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="64272-103">Maintain Fixed Assets</span></span>
<span data-ttu-id="64272-104">Underhållskostnaderna är rutinmässiga periodiska kostnader som utförs för att bevara värdet på en anläggningstillgång.</span><span class="sxs-lookup"><span data-stu-id="64272-104">Maintenance expenses are routine periodic costs undertaken to preserve the value of fixed assets.</span></span> <span data-ttu-id="64272-105">Till skillnad från kapitalförbättringar ökar de inte värden.</span><span class="sxs-lookup"><span data-stu-id="64272-105">Unlike capital improvements, they do not increase values.</span></span>

<span data-ttu-id="64272-106">Du kan registrera och underhålla en aktuell fil om underhåll och service av anläggningstillgångarna så att du enkelt har tillgång ett fullständiga underhållsregister för anläggningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="64272-106">You can record and maintain an up-to-date file on maintenance and service of your fixed assets to have complete maintenance records on a fixed asset easily accessible.</span></span> <span data-ttu-id="64272-107">När en anläggningstillgång skickas på service noterar du all relevant information, som exempelvis servicedatum, leverantörsnummer och serviceföretagets telefonnummer.</span><span class="sxs-lookup"><span data-stu-id="64272-107">Each time a fixed asset is sent to service, you record all relevant information such as date of service, vendor number and service agent's phone number.</span></span> <span data-ttu-id="64272-108">Underhållsregistrering registreras för varje anläggningstillgång från det aktuella anläggningstillgångskortet.</span><span class="sxs-lookup"><span data-stu-id="64272-108">Maintenance registration is recorded for each fixed asset from the relevant fixed asset card.</span></span>

<span data-ttu-id="64272-109">Indexering används för att anpassa värden till den allmänna prisnivån.</span><span class="sxs-lookup"><span data-stu-id="64272-109">Indexation is used to adjust values for general price-level changes.</span></span> <span data-ttu-id="64272-110">Du kan använda batch-jobbet **Indexera anläggningstillgångar** om du vill omberäkna underhållskostnader.</span><span class="sxs-lookup"><span data-stu-id="64272-110">The **Index Fixed Assets** batch job can be used to recalculate the maintenance costs.</span></span>

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a><span data-ttu-id="64272-111">Om du vill registrera underhållsarbete på en anläggningstillgång</span><span class="sxs-lookup"><span data-stu-id="64272-111">To record maintenance work on a fixed asset</span></span>
<span data-ttu-id="64272-112">Varje gång som underhåll har utförts, exempelvis ett servicebesök kan du registrera detta för den aktuella anläggningstillgången i fönstret  **Underhållsregistrering**.</span><span class="sxs-lookup"><span data-stu-id="64272-112">Every time maintenance has been performed, such as a service visit, you can record it for the relevant fixed asset in the **Maintenance Registrations** window.</span></span>  

1. <span data-ttu-id="64272-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anläggningstillgångar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="64272-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="64272-114">Markera den anläggningstillgång som du vill registrera underhåll för och välj sedan åtgärden **Underhållsregistreringar**.</span><span class="sxs-lookup"><span data-stu-id="64272-114">Select the fixed asset that you want to record maintenance for, and then choose the **Maintenance Registration** action.</span></span>
3. <span data-ttu-id="64272-115">I fönstret **Underhållsregistreringar** fyller du i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="64272-115">In the **Maintenance Registration** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a><span data-ttu-id="64272-116">Att bokföra underhållskostnader från en redovisningsjournalen för anläggningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="64272-116">To post maintenance costs from a fixed asset G/L journal</span></span>
1. <span data-ttu-id="64272-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport") , ange **Avskrivningsregellista**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="64272-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Depreciation Book List**, and then choose the related link.</span></span>  
2. <span data-ttu-id="64272-118">Markera den avskrivningsregel som är tilldelad anläggningstillgången och välj sedan åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="64272-118">Select the depreciation book that is assigned to the fixed asset, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="64272-119">I fönstret **Avskrivningsregelkort** ser du till att kryssrutan **Underhåll** inte är markerad.</span><span class="sxs-lookup"><span data-stu-id="64272-119">In the **Depreciation Book Card** window, make sure the **Maintenance** check box is not selected.</span></span> <span data-ttu-id="64272-120">Detta säkerställer att underhållskostnader inte bokförs till redovisningen.</span><span class="sxs-lookup"><span data-stu-id="64272-120">This ensures that maintenance costs are not posted to the general ledger.</span></span>
4. <span data-ttu-id="64272-121">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="64272-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
5. <span data-ttu-id="64272-122">Skapa en första journalrad och fyll i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="64272-122">Create an initial journal line and fill in the fields as necessary.</span></span>
6. <span data-ttu-id="64272-123">Välj **Anskaffningskostnad** i fältet **Underhåll**.</span><span class="sxs-lookup"><span data-stu-id="64272-123">In the **FA Posting Type** field, select **Maintenance**.</span></span>
7. <span data-ttu-id="64272-124">Välj åtgärden **Infoga anl. motkonto**.</span><span class="sxs-lookup"><span data-stu-id="64272-124">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="64272-125">En andra journalrad skapas för motkontot som ställs in för bokföring av underhåll.</span><span class="sxs-lookup"><span data-stu-id="64272-125">A second journal line is created for the balancing account that is set up for maintenance posting.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="64272-126">Steg 7 fungerar bara om du har ställt in följande: I fönstret **Anl. bokföringsmallkort** för den fasta anläggningstillgångens bokföringsmall, innehåller fältet **Underhållskonto** redovisningsdebitkontot och fältet **Underhållskontosaldo** innehåller det redovisningskonto där du vill bokföra mottransaktioner för uppskrivning.</span><span class="sxs-lookup"><span data-stu-id="64272-126">Step 7 only works if you have set up the following: In the **FA Posting Group Card** window for the posting group of the fixed asset, the **Maintenance Account** field contains the general ledger debit account and the **Maintenance Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="64272-127">För mer information, se avsnittet "Att ställa in bokföringsmallar för anläggningstillgångar" i avsnittet [Så här ställer du in allmän information för anläggningstillgångar](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="64272-127">For more information, see the "To set up fixed asset posting groups" section in [Set Up General Fixed Asset Information](fa-how-setup-general.md).</span></span>
8. <span data-ttu-id="64272-128">Välj åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="64272-128">Choose the **Post** action.</span></span>

## <a name="to-follow-up-on-fixed-assets-service-visits"></a><span data-ttu-id="64272-129">Så här följer du upp servicebesök för anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="64272-129">To follow up on fixed assets service visits</span></span>
<span data-ttu-id="64272-130">Du kan skriva ut rapporten **Underhåll – nästa service** om du vill se vilka tillgångar som du har bokat in ett servicebesök för.</span><span class="sxs-lookup"><span data-stu-id="64272-130">You can print the **Maintenance - Next Service** report to see which assets you have scheduled a service visit for.</span></span> <span data-ttu-id="64272-131">Du kan även använda den här rapporten när du uppdaterar fältet **Nästa servicedatum** på anläggningstillgångskortet.</span><span class="sxs-lookup"><span data-stu-id="64272-131">You can also use this report when you are updating the **Next Service Date** field on fixed asset cards.</span></span>  

1. <span data-ttu-id="64272-132">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Underhåll nästa service** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="64272-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance Next Service**, and then choose the related link.</span></span>  
2. <span data-ttu-id="64272-133">Fyll i fälten **Startdatum** och **Slutdatum**.</span><span class="sxs-lookup"><span data-stu-id="64272-133">Fill in the **Starting Date** and **Ending Date** fields.</span></span>  
3. <span data-ttu-id="64272-134">Välj knappen **Skriv ut** eller **Förhandsgranska**.</span><span class="sxs-lookup"><span data-stu-id="64272-134">Choose the **Print** or **Preview** button.</span></span>

## <a name="to-monitor-maintenance-costs"></a><span data-ttu-id="64272-135">Så här övervakar du underhållskostnader:</span><span class="sxs-lookup"><span data-stu-id="64272-135">To monitor maintenance costs</span></span>
<span data-ttu-id="64272-136">Du kan se underhållskostnaderna när du visar statistiken för en anläggningstillgång.</span><span class="sxs-lookup"><span data-stu-id="64272-136">You can view the maintenance costs when you look at the statistics of a fixed asset.</span></span>  

1. <span data-ttu-id="64272-137">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anläggningstillgångar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="64272-137">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="64272-138">Markera den anläggningstillgång som du vill visa underhållskostnader för välj sedan åtgärden **Avskrivningsregler**.</span><span class="sxs-lookup"><span data-stu-id="64272-138">Select the fixed asset you want to view maintenance costs for, and then choose the **Depreciation Books** action.</span></span>
3. <span data-ttu-id="64272-139">I fönstret **Avskrivningsregler för anl.tillg.** väljer du relevant avskrivningsregel för anläggningstillgång åtgärden **Statistik**.</span><span class="sxs-lookup"><span data-stu-id="64272-139">In the **FA Depreciation Books** window, select the relevant fixed asset depreciation book, and then choose the **Statistics** action.</span></span>
4. <span data-ttu-id="64272-140">I **Anl.tillg.statistik** väljer du fältet **Underhåll**.</span><span class="sxs-lookup"><span data-stu-id="64272-140">In the **Fixed Asset Statistics** window, choose the **Maintenance** field.</span></span>

<span data-ttu-id="64272-141">Fönstret **Underhållstransaktioner** öppnas och visar de poster som utgör beloppet i fältet **Underhåll**.</span><span class="sxs-lookup"><span data-stu-id="64272-141">The **Maintenance Ledger Entries** window opens showing the entries that make up the amount in the **Maintenance** field.</span></span>

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a><span data-ttu-id="64272-142">Om du vill visa eller skriva ut underhållskostnader för åtskilliga anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="64272-142">To view or print maintenance costs for multiple fixed assets</span></span>
<span data-ttu-id="64272-143">I rapporten **Underhållsanalys** kan du välja om du vill visa underhåll baaserat på en, två eller tre underhållskoder för ett angivet datum eller en angiven period.</span><span class="sxs-lookup"><span data-stu-id="64272-143">In the **Maintenance - Analysis** report, you can select to see maintenance based on one, two, or three maintenance codes for a specified date or period.</span></span> <span data-ttu-id="64272-144">Du kan se summan för alla de markerade tillgångarna eller summan för varje tillgång.</span><span class="sxs-lookup"><span data-stu-id="64272-144">You can see the total of all selected assets or a total for each asset.</span></span>

1. <span data-ttu-id="64272-145">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Underhållsanalys** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="64272-145">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance Analysis**, and then choose the related link.</span></span>
2. <span data-ttu-id="64272-146">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="64272-146">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="64272-147">Välj knappen **Skriv ut** eller **Förhandsgranska**.</span><span class="sxs-lookup"><span data-stu-id="64272-147">Choose the **Print** or **Preview** button.</span></span>

## <a name="to-view-maintenance-ledger-entries"></a><span data-ttu-id="64272-148">Så här visar du underhållstransaktioner</span><span class="sxs-lookup"><span data-stu-id="64272-148">To view maintenance ledger entries</span></span>
<span data-ttu-id="64272-149">Du kan också studera underhållskostnader genom att visa underhållstransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="64272-149">You can also study maintenance costs by viewing the maintenance ledger entries.</span></span>  

1. <span data-ttu-id="64272-150">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anläggningstillgångar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="64272-150">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="64272-151">Markera den fasta anläggningstillgång som du vill visa transaktioner för välj sedan åtgärden **Avskrivningsregler**.</span><span class="sxs-lookup"><span data-stu-id="64272-151">Select the fixed asset that you want to view ledger entries for, and then choose the **Depreciation Books** action.</span></span>
3. <span data-ttu-id="64272-152">I fönstret **Avskrivningsregler för anl.tillg.** väljer du relevant avskrivningsregel för anläggningstillgång åtgärden **Underhållstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="64272-152">In the **FA Depreciation Books** window, select the relevant fixed asset depreciation book, and then choose the **Maintenance Ledger Entries** action.</span></span>

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a><span data-ttu-id="64272-153">Om du vill visa eller skriva ut underhållstransaktioner för åtskilliga anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="64272-153">To view or print maintenance ledger entries for multiple fixed assets</span></span>
<span data-ttu-id="64272-154">I rapporten **Underhåll - Uppgifter** kan du visa eller skriva ut underhållstransaktioner för en eller flera anläggningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="64272-154">In the **Maintenance - Details** report, you can view or print maintenance ledger entries for one or many fixed assets.</span></span>  

1. <span data-ttu-id="64272-155">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Underhållsdetaljer** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="64272-155">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance Details**, and then choose the related link.</span></span>
2. <span data-ttu-id="64272-156">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="64272-156">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="64272-157">Välj knappen **Skriv ut** eller **Förhandsgranska**.</span><span class="sxs-lookup"><span data-stu-id="64272-157">Choose the **Print** or **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="64272-158">Se även</span><span class="sxs-lookup"><span data-stu-id="64272-158">See Also</span></span>
[<span data-ttu-id="64272-159">Anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="64272-159">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="64272-160">Ställa in anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="64272-160">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="64272-161">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="64272-161">Finance</span></span>](finance.md)  
[<span data-ttu-id="64272-162">Komma igång</span><span class="sxs-lookup"><span data-stu-id="64272-162">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="64272-163">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="64272-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
