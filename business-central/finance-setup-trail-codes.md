---
title: Definiera koder för granskningshistorik | Microsoft Docs
description: Lära dig mer om aktiviteterna för att ställa in ursprungskoder och orsakskoder som du kan använda för att spåra granskningshistorik.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9dab74a6a8debd20de781890c3b391457c6034e3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386905"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><span data-ttu-id="efc53-103">Ställa in ursprungskoder och orsakskoder för granskningshistorik</span><span class="sxs-lookup"><span data-stu-id="efc53-103">Setting Up Source Codes and Reason Codes for Audit Trails</span></span>

<span data-ttu-id="efc53-104">Alla bokförda transaktioner tilldelas automatiskt en ursprungskod så att transaktionerna kan spåras till dess ursprung.</span><span class="sxs-lookup"><span data-stu-id="efc53-104">All posted entries are automatically assigned a source code so that transactions can be traced to their origin.</span></span> <span data-ttu-id="efc53-105">Om du vill ge transaktionerna en extra ursprungskod kan du använda uppföljningskoder.</span><span class="sxs-lookup"><span data-stu-id="efc53-105">If you want to give entries a supplementary source code, you can use reason codes.</span></span> <span data-ttu-id="efc53-106">Uppföljningskoder används för att ange varför en transaktion har upprättats.</span><span class="sxs-lookup"><span data-stu-id="efc53-106">Reason codes are used to indicate why an entry was created.</span></span> <span data-ttu-id="efc53-107">När du skapar uppföljningskoder kan du tilldela dem till hela journalmallar och journaler, och du kan tilldela dem till enskilda journalrader och dokument.</span><span class="sxs-lookup"><span data-stu-id="efc53-107">When you set up reason codes, you can assign them to entire journal templates and journal batches, and you can assign them to individual journal lines and documents.</span></span>  

<span data-ttu-id="efc53-108">För både ursprungskoder och orsakskoder bör du använda koder som är lätta att komma ihåg och som är beskrivande.</span><span class="sxs-lookup"><span data-stu-id="efc53-108">For both source codes and reason codes, use codes that are easy to remember and descriptive.</span></span> <span data-ttu-id="efc53-109">Koden måste vara unik och du kan registrera så många koder du vill.</span><span class="sxs-lookup"><span data-stu-id="efc53-109">The code must be unique, and you can set up as many codes as you like.</span></span>

## <a name="define-source-codes"></a><span data-ttu-id="efc53-110">Definiera ursprungskoder</span><span class="sxs-lookup"><span data-stu-id="efc53-110">Define source codes</span></span>

<span data-ttu-id="efc53-111">Ibland behöver du se hur en viss transaktion uppstod, t. ex. om den har sitt ursprung i en redovisningsjournal eller en inköpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="efc53-111">Sometimes, you want see how a particular entry arose, such as whether it came from posting a general journal or a purchase invoice.</span></span> <span data-ttu-id="efc53-112">En ursprungskod anger var en transaktion har skapats.</span><span class="sxs-lookup"><span data-stu-id="efc53-112">A source code indicates where an entry was created.</span></span> <span data-ttu-id="efc53-113">Transaktioner skapas när journaler och fakturor bokförs och när vissa batch-jobb körs.</span><span class="sxs-lookup"><span data-stu-id="efc53-113">Entries are created when journals and invoices are posted and when certain batch jobs are executed.</span></span> <span data-ttu-id="efc53-114">Varje bokföringstyp har en specifik ursprungskod som tilldelas när enskilda transaktioner skapas.</span><span class="sxs-lookup"><span data-stu-id="efc53-114">Each posting type has a specific source code that is assigned when individual entries are created.</span></span>  

<span data-ttu-id="efc53-115">Bokföring av journaler, order, fakturor eller kreditnotor, och körningar av olika batch-jobb, skapar transaktioner i räkenskaperna.</span><span class="sxs-lookup"><span data-stu-id="efc53-115">Posting journals, orders, invoices, or credit memos, and running various batch jobs, creates entries in the financial statements.</span></span> <span data-ttu-id="efc53-116">Fönstret **Ursprungskodinställningar** innehåller flera snabbflikar, en för varje modul.</span><span class="sxs-lookup"><span data-stu-id="efc53-116">The **Source Code Setup** page contains several FastTabs, one for each application area.</span></span> <span data-ttu-id="efc53-117">Varje snabbflik innehåller ursprungskoder som gäller för den modulen.</span><span class="sxs-lookup"><span data-stu-id="efc53-117">Each FastTab contains the source codes that are applicable for that application area.</span></span>

<span data-ttu-id="efc53-118">När du bokför, eller kör ett batch-jobb, kompletterar programmet automatiskt transaktionen med rätt ursprungskod.</span><span class="sxs-lookup"><span data-stu-id="efc53-118">When you post or run a batch job, the correct source code is automatically attached to the entry.</span></span> <span data-ttu-id="efc53-119">När du t. ex. bokför en redovisningsjournal, kodar programmet transaktionen som *REDOVJNL*.</span><span class="sxs-lookup"><span data-stu-id="efc53-119">For example, when you post from the general journal, the entry is coded as *GENJNL*.</span></span> <span data-ttu-id="efc53-120">Du kan sedan filtrera sidan **redovisningstransaktioner** för att visa vilka transaktioner som bokförts från redovisningsjournalen eller från försäljningsdokument, t. ex.</span><span class="sxs-lookup"><span data-stu-id="efc53-120">You can then filter the **General Ledger Entries** page to show which entries were posted from the general journal or from sales documents, for example</span></span>

### <a name="to-define-source-codes"></a><span data-ttu-id="efc53-121">Så här definierar du ursprungskoder</span><span class="sxs-lookup"><span data-stu-id="efc53-121">To define source codes</span></span>

1. <span data-ttu-id="efc53-122">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **Ursprungskodinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="efc53-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Code Setup**, and then choose the related link.</span></span>  

2. <span data-ttu-id="efc53-123">I fönstret **Ursprungskodinställningar** för varje bokföringstyp och batch-jobb, ange relevant källkod.</span><span class="sxs-lookup"><span data-stu-id="efc53-123">In the **Source Code Setup** window, for each each posting type and batch job, specify the relevant source code.</span></span>  

<span data-ttu-id="efc53-124">Du kan ändra innehållet i ett fält senare, så att ändringen påverkar framtida bokföringar.</span><span class="sxs-lookup"><span data-stu-id="efc53-124">You can change the contents of a field later, and that change will then impact future postings.</span></span>

## <a name="change-source-codes"></a><span data-ttu-id="efc53-125">Ändra ursprungskoder</span><span class="sxs-lookup"><span data-stu-id="efc53-125">Change source codes</span></span>

<span data-ttu-id="efc53-126">Det kan hända att du vill ändra en ursprungskod.</span><span class="sxs-lookup"><span data-stu-id="efc53-126">You may want to change a source code.</span></span> <span data-ttu-id="efc53-127">Du kanske t. ex. vill ändra ursprungskoden *GENJNL* till *GNJ*.</span><span class="sxs-lookup"><span data-stu-id="efc53-127">For example, you want to change the source code *GENJNL* to *GNJ*.</span></span>

### <a name="to-change-source-codes"></a><span data-ttu-id="efc53-128">Så här ändrar du ursprungskoder</span><span class="sxs-lookup"><span data-stu-id="efc53-128">To change source codes</span></span>

1. <span data-ttu-id="efc53-129">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **Ursprungskoder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="efc53-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="efc53-130">På raden med den kod som ska ändras markerar du koden i fältet **Kod**.</span><span class="sxs-lookup"><span data-stu-id="efc53-130">On the line with the code to be changed, select the code in the **Code** field.</span></span>

3. <span data-ttu-id="efc53-131">Ange en ny kod och klicka sedan på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="efc53-131">Enter the new code, and then choose the **Yes** button.</span></span> <span data-ttu-id="efc53-132">Du kan också ändra innehållet i fältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="efc53-132">You can also change the contents of the **Description** field.</span></span>

<span data-ttu-id="efc53-133">Alla nya transaktioner som har bokförts från redovisningsjournalen får den nya ursprungskoden.</span><span class="sxs-lookup"><span data-stu-id="efc53-133">All new entries that are posted from the general journal will have the new source code.</span></span>

## <a name="define-reason-codes"></a><span data-ttu-id="efc53-134">Definiera uppföljningskoder</span><span class="sxs-lookup"><span data-stu-id="efc53-134">Define reason codes</span></span>

<span data-ttu-id="efc53-135">Uppföljningskoderna kompletterar ursprungskoderna och används för att ange varför en transaktion har upprättats.</span><span class="sxs-lookup"><span data-stu-id="efc53-135">Reason codes supplement the source codes and are used to indicate why an entry was created.</span></span> <span data-ttu-id="efc53-136">Du kan tilldela uppföljningskoder på enskilda transaktioner och du kan tilldela permanenta koder för särskilda journalmallar och journaler.</span><span class="sxs-lookup"><span data-stu-id="efc53-136">You can assign reason codes on individual entries, and you can assign permanent codes to specific journal templates and journal batches.</span></span> <span data-ttu-id="efc53-137">När en uppföljningskod kopplas till en journalrad eller ett försäljnings- eller inköpshuvud, kommer programmet att märka alla transaktionerna med den angivna uppföljningskoden när de bokförs.</span><span class="sxs-lookup"><span data-stu-id="efc53-137">When a reason code is linked to a journal line or a sales or purchase header, all entries are marked with the reason code when they are posted.</span></span>  

### <a name="to-set-up-reason-codes"></a><span data-ttu-id="efc53-138">Så här lägger du upp uppföljningskoder</span><span class="sxs-lookup"><span data-stu-id="efc53-138">To set up reason codes</span></span>

1. <span data-ttu-id="efc53-139">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **uppföljningskoder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="efc53-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **Reason Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="efc53-140">I fönstret **uppföljningskoder** anger du den första koden i fältet **kod**.</span><span class="sxs-lookup"><span data-stu-id="efc53-140">In the **Reason Codes** window, enter the first code in the **Code** field.</span></span> <span data-ttu-id="efc53-141">Skriv in en beskrivning i fältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="efc53-141">In the **Description** field, enter an explanatory text.</span></span>

<span data-ttu-id="efc53-142">Upprepa den här proceduren för alla koder som du vill använda.</span><span class="sxs-lookup"><span data-stu-id="efc53-142">Repeat the procedure for each code you want to use.</span></span> <span data-ttu-id="efc53-143">Du kan skapa så många koder du vill.</span><span class="sxs-lookup"><span data-stu-id="efc53-143">You can set up any number of codes.</span></span>

<span data-ttu-id="efc53-144">I följande procedur beskrivs hur du lägger till en uppföljningskod i en journalmall, men liknande åtgärder gäller för att lägga till en uppföljningskod till en journalrad eller journal.</span><span class="sxs-lookup"><span data-stu-id="efc53-144">The following procedure describes how to add a reason code to a journal template, but similar steps apply to adding a reason code to a journal line or journal batch.</span></span>  

### <a name="to-assign-reason-codes-to-journal-templates"></a><span data-ttu-id="efc53-145">Så här tilldelar du uppföljningskoder till journalmallar</span><span class="sxs-lookup"><span data-stu-id="efc53-145">To assign reason codes to journal templates</span></span>

1. <span data-ttu-id="efc53-146">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **Redovisningsjournalmallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="efc53-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **General Journal Templates**, and then choose the related link.</span></span>

2. <span data-ttu-id="efc53-147">Ange relevant kod i fältet **Uppföljningskod** på raden med journalmallen.</span><span class="sxs-lookup"><span data-stu-id="efc53-147">On the line with the selected journal template, in the **Reason Code** field, specify the relevant code.</span></span>

3. <span data-ttu-id="efc53-148">Stäng journalmallen.</span><span class="sxs-lookup"><span data-stu-id="efc53-148">Close the journal template.</span></span>

<span data-ttu-id="efc53-149">Den valda uppföljningskoden kopieras till nya journaler som skapas med den här journalmallen.</span><span class="sxs-lookup"><span data-stu-id="efc53-149">The selected reason code will be copied to new journal batches created under this journal template.</span></span> <span data-ttu-id="efc53-150">Du kan tilldela uppföljningskoder till journalmallar i andra moduler på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="efc53-150">You assign reason codes to journal templates in the other application areas in the same way.</span></span>

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><span data-ttu-id="efc53-151">Så här använder du uppföljningskoder i försäljnings- och inköpsdokument</span><span class="sxs-lookup"><span data-stu-id="efc53-151">To use reason codes on sales and purchase documents</span></span>

1. <span data-ttu-id="efc53-152">Öppna relevant försäljnings- eller inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="efc53-152">Open the relevant sales or purchase document.</span></span>

2. <span data-ttu-id="efc53-153">Ange koden i fältet **Uppföljningskod** i försäljnings- eller inköpshuvudet.</span><span class="sxs-lookup"><span data-stu-id="efc53-153">On the sales or purchase header, enter the code in the **Reason Code** field.</span></span>

<span data-ttu-id="efc53-154">När fakturan bokförs kopieras uppföljningskoden till alla redovisnings-, kund- och leverantörstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="efc53-154">When the invoice is posted, the reason code is copied to each general ledger, customer, and vendor entry.</span></span> <span data-ttu-id="efc53-155">Du kan inte tilldela olika uppföljningskoder till de enskilda inköps- och försäljningsraderna eftersom alla rader bokförs som en transaktion.</span><span class="sxs-lookup"><span data-stu-id="efc53-155">You cannot assign different reason codes to the individual purchase and sales lines because all lines are posted as one entry.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="efc53-156">Se Relaterad utbildning på [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="efc53-156">See Related Training at [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="efc53-157">Se även</span><span class="sxs-lookup"><span data-stu-id="efc53-157">See Also</span></span>

[<span data-ttu-id="efc53-158">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="efc53-158">Finance</span></span>](finance.md)  
[<span data-ttu-id="efc53-159">Jämka bankkonton</span><span class="sxs-lookup"><span data-stu-id="efc53-159">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="efc53-160">Arbeta med dimensioner</span><span class="sxs-lookup"><span data-stu-id="efc53-160">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="efc53-161">Importera affärsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="efc53-161">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="efc53-162">Analysera kassaflödet i företaget</span><span class="sxs-lookup"><span data-stu-id="efc53-162">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="efc53-163">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="efc53-163">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]