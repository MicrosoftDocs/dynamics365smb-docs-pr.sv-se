---
title: Mer information om redovisning och kontoplanen | Microsoft Docs
description: Beskriver redovisningen, kontoplanen och kontokategorierna.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dbeb9f9cbe0eff61b28dc4d371a1f8d9031ea1b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747047"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="cc30b-103">Så här fungerar i redovisningen och kontoplanen</span><span class="sxs-lookup"><span data-stu-id="cc30b-103">Understanding the General Ledger and the COA</span></span>

<span data-ttu-id="cc30b-104">Redovisningen lagrar dina ekonomiska data, och kontoplanen visar de konton som alla redovisningstransaktioner bokförs på.</span><span class="sxs-lookup"><span data-stu-id="cc30b-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="cc30b-105">inkluderar en standardkontoplan som är klar att stödja din verksamhet.</span><span class="sxs-lookup"><span data-stu-id="cc30b-105">includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="cc30b-106">Redovisningsinställning och bokföringingsinställning</span><span class="sxs-lookup"><span data-stu-id="cc30b-106">General Ledger Setup and General Posting Setup</span></span>

<span data-ttu-id="cc30b-107">Inställningarna för redovisningen är kärnan i ekonomiska processer eftersom den definierar hur du bokför data.</span><span class="sxs-lookup"><span data-stu-id="cc30b-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="cc30b-108">På sidan **Redovisningsinställningar** anger du hur du vill hantera vissa bokföringsfrågor i företaget som t.ex.:</span><span class="sxs-lookup"><span data-stu-id="cc30b-108">On the **General Ledger Setup** page, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="cc30b-109">Öresutjämning</span><span class="sxs-lookup"><span data-stu-id="cc30b-109">Invoice rounding details</span></span>  
* <span data-ttu-id="cc30b-110">Adresslayout</span><span class="sxs-lookup"><span data-stu-id="cc30b-110">Address formats</span></span>  
* <span data-ttu-id="cc30b-111">Ekonomisk rapportering</span><span class="sxs-lookup"><span data-stu-id="cc30b-111">Financial reporting</span></span>  

<span data-ttu-id="cc30b-112">På liknande sätt p sidan **Bokföringsinställningar** anger du hur du vill ange kombinationer av allmän bokföringsmallar och allmäna produktbokföringsmallar.</span><span class="sxs-lookup"><span data-stu-id="cc30b-112">Similarly, on the **General Posting Setup** page, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="cc30b-113">Bokföringsmallar mappar enheter som t.ex. kunder, leverantörer, artiklar, resurser och försäljning och inköpsdokument till redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="cc30b-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="cc30b-114">Du fyller i en rad för varje kombination av rörelse- och produktbokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="cc30b-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="cc30b-115">Mer information finns i [Inställning av bokföringsmall](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="cc30b-115">For more information, see [Posting Group Setups](finance-posting-groups.md).</span></span>  

> [!TIP]
> <span data-ttu-id="cc30b-116">Sidan **redovisningsinställning** innehåller allmänna fält och fält som är specifika för ditt land eller din region.</span><span class="sxs-lookup"><span data-stu-id="cc30b-116">The **General Ledger Setup** page includes generic fields and fields that are particular to your country or region.</span></span> <span data-ttu-id="cc30b-117">Om du är osäker på innebörden av ett fält föreslår vi att du arbetar med revisorn för att avgöra om det är relevant för organisationen.</span><span class="sxs-lookup"><span data-stu-id="cc30b-117">If you are not sure of the meaning of a field, we suggest you work with your accountant to determine whether it is of relevance to your organization.</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="cc30b-118">Kontoplanen</span><span class="sxs-lookup"><span data-stu-id="cc30b-118">The Chart of Accounts</span></span>

<span data-ttu-id="cc30b-119">Kontoplanen visar alla redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="cc30b-119">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="cc30b-120">Från kontoplanen, kan du göra sådant som:</span><span class="sxs-lookup"><span data-stu-id="cc30b-120">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="cc30b-121">Visa rapporter som visar transaktioner och saldon.</span><span class="sxs-lookup"><span data-stu-id="cc30b-121">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="cc30b-122">Avslut av resultatkonton.</span><span class="sxs-lookup"><span data-stu-id="cc30b-122">Close your income statement.</span></span>  
* <span data-ttu-id="cc30b-123">Öppna redovisningkontokortet om du vill lägga till eller ändra inställningar.</span><span class="sxs-lookup"><span data-stu-id="cc30b-123">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="cc30b-124">Visa en lista med bokföringsmallar som bokför på det konto.</span><span class="sxs-lookup"><span data-stu-id="cc30b-124">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="cc30b-125">Visa separatea debet- och kreditsaldon för ett enskilt konto</span><span class="sxs-lookup"><span data-stu-id="cc30b-125">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="cc30b-126">Du kan lägga till, ändra eller ta bort konton i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="cc30b-126">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="cc30b-127">Men för att undvika avvikelser bör du inte ta bort ett redovisningskonto om dess data används i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="cc30b-127">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="cc30b-128">Kontokategorier</span><span class="sxs-lookup"><span data-stu-id="cc30b-128">Account Categories</span></span>

<span data-ttu-id="cc30b-129">Med kontokategorier kan du mappa redovisningskonton till kategorier som en anpassning av strukturen på din redovisning.</span><span class="sxs-lookup"><span data-stu-id="cc30b-129">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="cc30b-130">Sidan **Redovisningskontokategorier** visar de kategorierna och delkategorierna och redovisningskontona som har tilldelats dem.</span><span class="sxs-lookup"><span data-stu-id="cc30b-130">The **G/L Account Categories** page shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="cc30b-131">Du kan skapa nya delkategorier och tilldela de kategorierna till befintliga konton.</span><span class="sxs-lookup"><span data-stu-id="cc30b-131">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="cc30b-132">Du skapar en kategorigrupp, genom att dra in andra delkategorier under en rad på sidan **redovisningskontokategorier**.</span><span class="sxs-lookup"><span data-stu-id="cc30b-132">You create a category group by indenting other subcategories under a line on the **G/L Account Categories** page.</span></span> <span data-ttu-id="cc30b-133">Detta gör det lätt för dig att få en översikt, eftersom varje journal visar ett totalt saldo.</span><span class="sxs-lookup"><span data-stu-id="cc30b-133">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="cc30b-134">Du kan till exempel skapa delkategorier för andra typer av anläggningstillgångar och sedan skapa kategorigrupper för t.ex. anläggningstillgångar jämfört med omsättningstillgångar.</span><span class="sxs-lookup"><span data-stu-id="cc30b-134">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="cc30b-135">För varje delkategori kan du ange om konton för den kategorin måste tas med i vissa typer av ekonomiska rapporter.</span><span class="sxs-lookup"><span data-stu-id="cc30b-135">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="cc30b-136">Du kan använda kontokategorier för att ändra layout på din redovisning.</span><span class="sxs-lookup"><span data-stu-id="cc30b-136">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="cc30b-137">Till exempel har det standardinställda saldo vid kontoavstämning en enkelt transaktion för kontanter under tillgångar.</span><span class="sxs-lookup"><span data-stu-id="cc30b-137">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="cc30b-138">Om du vill att saldot överväger handkassa och check, kan du:</span><span class="sxs-lookup"><span data-stu-id="cc30b-138">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="cc30b-139">Lägga till två nya underkategorierna.</span><span class="sxs-lookup"><span data-stu-id="cc30b-139">Add two new subcategories.</span></span> <span data-ttu-id="cc30b-140">En för handkassa och ett för ditt checkkonto.</span><span class="sxs-lookup"><span data-stu-id="cc30b-140">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="cc30b-141">Ange ytterligare rapportdefinitionen **kassakonton** för dessa underkategorier.</span><span class="sxs-lookup"><span data-stu-id="cc30b-141">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="cc30b-142">Dra in dem under underkategorin **kontant**.</span><span class="sxs-lookup"><span data-stu-id="cc30b-142">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="cc30b-143">Nästa gång du har genererat kontouppställningar kommer saldot visa ett totalt saldo för kontanter och två rader med saldon för handkassa och checkräkningskontot.</span><span class="sxs-lookup"><span data-stu-id="cc30b-143">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cc30b-144">Se även</span><span class="sxs-lookup"><span data-stu-id="cc30b-144">See Also</span></span>

[<span data-ttu-id="cc30b-145">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="cc30b-145">Finance</span></span>](finance.md)  
[<span data-ttu-id="cc30b-146">Ställa in eller ändra kontoplanen</span><span class="sxs-lookup"><span data-stu-id="cc30b-146">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="cc30b-147">Affärsstöd</span><span class="sxs-lookup"><span data-stu-id="cc30b-147">Business Intelligence</span></span>](bi.md)  
