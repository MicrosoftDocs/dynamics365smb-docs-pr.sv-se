---
title: Mer information om redovisning och kontoplanen | Microsoft Docs
description: Beskriver redovisningen, kontoplanen och kontokategorierna.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06becfd7e54803fea925e8364719576bef0a8bab
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="9a20f-103">Så här fungerar i redovisningen och kontoplanen</span><span class="sxs-lookup"><span data-stu-id="9a20f-103">Understanding the General Ledger and the COA</span></span>
<span data-ttu-id="9a20f-104">Redovisningen lagrar dina ekonomiska data, och kontoplanen visar de konton som alla redovisningstransaktioner bokförs på.</span><span class="sxs-lookup"><span data-stu-id="9a20f-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9a20f-105"> inkluderar en standardkontoplan som är klar att stödja din verksamhet.</span><span class="sxs-lookup"><span data-stu-id="9a20f-105"> includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="9a20f-106">Redovisningsinställning och bokföringingsinställning</span><span class="sxs-lookup"><span data-stu-id="9a20f-106">General Ledger Setup and General Posting Setup</span></span>
<span data-ttu-id="9a20f-107">Inställningarna för redovisningen är kärnan i ekonomiska processer eftersom den definierar hur du bokför data.</span><span class="sxs-lookup"><span data-stu-id="9a20f-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="9a20f-108">I fönstret **Redovisningsinställningar** anger du hur du vill hantera vissa bokföringsfrågor i företaget som t.ex.:</span><span class="sxs-lookup"><span data-stu-id="9a20f-108">In the **General Ledger Setup** window, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="9a20f-109">Öresutjämning</span><span class="sxs-lookup"><span data-stu-id="9a20f-109">Invoice rounding details</span></span>  
* <span data-ttu-id="9a20f-110">Adresslayout</span><span class="sxs-lookup"><span data-stu-id="9a20f-110">Address formats</span></span>  
* <span data-ttu-id="9a20f-111">Ekonomisk rapportering</span><span class="sxs-lookup"><span data-stu-id="9a20f-111">Financial reporting</span></span>  

<span data-ttu-id="9a20f-112">På liknande sätt i fönstret **Bokföringsinställningar** anger du hur du vill ange kombinationer av allmän bokföringsmallar och allmäna produktbokföringsmallar.</span><span class="sxs-lookup"><span data-stu-id="9a20f-112">Similarly, in the **General Posting Setup** window, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="9a20f-113">Bokföringsmallar mappar enheter som t.ex. kunder, leverantörer, artiklar, resurser och försäljning och inköpsdokument till redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="9a20f-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="9a20f-114">Du fyller i en rad för varje kombination av rörelse- och produktbokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="9a20f-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="9a20f-115">Mer information finns i [Inställning av bokföringsmall](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="9a20f-115">For more information, see [Posting Group Setups](finance-posting-groups.md)</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="9a20f-116">Kontoplanen</span><span class="sxs-lookup"><span data-stu-id="9a20f-116">The Chart of Accounts</span></span>
<span data-ttu-id="9a20f-117">Kontoplanen visar alla redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="9a20f-117">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="9a20f-118">Från kontoplanen, kan du göra sådant som:</span><span class="sxs-lookup"><span data-stu-id="9a20f-118">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="9a20f-119">Visa rapporter som visar transaktioner och saldon.</span><span class="sxs-lookup"><span data-stu-id="9a20f-119">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="9a20f-120">Avslut av resultatkonton.</span><span class="sxs-lookup"><span data-stu-id="9a20f-120">Close your income statement.</span></span>  
* <span data-ttu-id="9a20f-121">Öppna redovisningkontokortet om du vill lägga till eller ändra inställningar.</span><span class="sxs-lookup"><span data-stu-id="9a20f-121">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="9a20f-122">Visa en lista med bokföringsmallar som bokför på det konto.</span><span class="sxs-lookup"><span data-stu-id="9a20f-122">See a list of posting groups that post to that account.</span></span>  

<span data-ttu-id="9a20f-123">Du kan lägga till, ändra eller ta bort konton i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="9a20f-123">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="9a20f-124">Men för att undvika avvikelser bör du inte ta bort ett redovisningskonto om dess data används i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="9a20f-124">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="9a20f-125">Kontokategorier</span><span class="sxs-lookup"><span data-stu-id="9a20f-125">Account Categories</span></span>
<span data-ttu-id="9a20f-126">Med kontokategorier kan du mappa redovisningskonton till kategorier som en anpassning av strukturen på din redovisning.</span><span class="sxs-lookup"><span data-stu-id="9a20f-126">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="9a20f-127">Fönstret **Redovisningskontokategorier** visar de kategorierna och delkategorierna och redovisningskontona som har tilldelats dem.</span><span class="sxs-lookup"><span data-stu-id="9a20f-127">The **G/L Account Categories** window shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="9a20f-128">Du kan skapa nya delkategorier och tilldela de kategorierna till befintliga konton.</span><span class="sxs-lookup"><span data-stu-id="9a20f-128">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="9a20f-129">Du skapar en kategorigrupp, genom att dra in andra delkategorier under en rad i fönstret **redovisningskontokategorier**.</span><span class="sxs-lookup"><span data-stu-id="9a20f-129">You create a category group by indenting other subcategories under a line in the **G/L Account Categories** window.</span></span> <span data-ttu-id="9a20f-130">Detta gör det lätt för dig att få en översikt, eftersom varje journal visar ett totalt saldo.</span><span class="sxs-lookup"><span data-stu-id="9a20f-130">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="9a20f-131">Du kan till exempel skapa delkategorier för andra typer av anläggningstillgångar och sedan skapa kategorigrupper för t.ex. anläggningstillgångar jämfört med omsättningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="9a20f-131">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="9a20f-132">För varje delkategori kan du ange om konton för den kategorin måste tas med i vissa typer av ekonomiska rapporter.</span><span class="sxs-lookup"><span data-stu-id="9a20f-132">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="9a20f-133">Du kan använda kontokategorier för att ändra layout på din redovisning.</span><span class="sxs-lookup"><span data-stu-id="9a20f-133">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="9a20f-134">Till exempel har det standardinställda saldo vid kontoavstämning en enkelt transaktion för kontanter under tillgångar.</span><span class="sxs-lookup"><span data-stu-id="9a20f-134">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="9a20f-135">Om du vill att saldot överväger handkassa och check, kan du:</span><span class="sxs-lookup"><span data-stu-id="9a20f-135">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="9a20f-136">Lägga till två nya underkategorierna.</span><span class="sxs-lookup"><span data-stu-id="9a20f-136">Add two new subcategories.</span></span> <span data-ttu-id="9a20f-137">En för handkassa och ett för ditt checkkonto.</span><span class="sxs-lookup"><span data-stu-id="9a20f-137">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="9a20f-138">Ange ytterligare rapportdefinitionen **kassakonton** för dessa underkategorier.</span><span class="sxs-lookup"><span data-stu-id="9a20f-138">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="9a20f-139">Dra in dem under underkategorin **kontant**.</span><span class="sxs-lookup"><span data-stu-id="9a20f-139">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="9a20f-140">Nästa gång du har genererat kontouppställningar kommer saldot visa ett totalt saldo för kontanter och två rader med saldon för handkassa och checkräkningskontot.</span><span class="sxs-lookup"><span data-stu-id="9a20f-140">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9a20f-141">Se även</span><span class="sxs-lookup"><span data-stu-id="9a20f-141">See Also</span></span>
[<span data-ttu-id="9a20f-142">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="9a20f-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="9a20f-143">Ställa in eller ändra kontoplanen</span><span class="sxs-lookup"><span data-stu-id="9a20f-143">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="9a20f-144">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="9a20f-144">Business Intelligence</span></span>](bi.md)  

