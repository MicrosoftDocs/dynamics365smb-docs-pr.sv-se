---
title: "Använda tillägget QuickBooks-migrering | Microsoft Docs"
description: "Beskriver hur du använder tillägget för att migrera kunder, leverantörer, artiklar och konton från QuickBooks Online till Dynamics 365."
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 05/24/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: e73db91a37fd5aee249de032d231df2c5e36b4ba
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---

# <a name="the-quickbooks-online-data-migration-extension-for-dynamics-365-business-edition"></a><span data-ttu-id="47365-103">Tillägget QuickBooks Online datamigrering för Dynamics 365 Business edition</span><span class="sxs-lookup"><span data-stu-id="47365-103">The QuickBooks Online Data Migration Extension for Dynamics 365 Business edition</span></span>
<span data-ttu-id="47365-104">Tillägget ingår i assisterade guiden **datamigrering** som hjälper dig att migrera viktiga affärsdata från QuickBooks Online till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="47365-104">This extension is included in the **Data Migration** assisted setup guide to help you migrate important business data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="47365-105">Detta är exempelvis användbart när företaget växer och du har bestämt dig för att uppgradera ditt program för hantering av företag genom att börja använda [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="47365-105">For example, this is useful when your business is growing, and you've decided to upgrade your business management app by starting to use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="what-data-can-i-import-from-quickbooks-online"></a><span data-ttu-id="47365-106">Vilka data kan jag importera från QuickBooks Online?</span><span class="sxs-lookup"><span data-stu-id="47365-106">What data can I import from QuickBooks Online?</span></span>
<span data-ttu-id="47365-107">Du kan importera följande data från QuickBooks Online till [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="47365-107">You can import the following data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

* <span data-ttu-id="47365-108">Kunder</span><span class="sxs-lookup"><span data-stu-id="47365-108">Customers</span></span>
* <span data-ttu-id="47365-109">Leverantör</span><span class="sxs-lookup"><span data-stu-id="47365-109">Vendors</span></span>
* <span data-ttu-id="47365-110">Artiklar</span><span class="sxs-lookup"><span data-stu-id="47365-110">Items</span></span>
* <span data-ttu-id="47365-111">Kontoplan</span><span class="sxs-lookup"><span data-stu-id="47365-111">Chart of accounts</span></span>
* <span data-ttu-id="47365-112">Transaktion för ingående saldo i redovisningen</span><span class="sxs-lookup"><span data-stu-id="47365-112">Beginning balance transaction in the general ledger</span></span>
* <span data-ttu-id="47365-113">Tillgängliga kvantiteter för lagerartiklar</span><span class="sxs-lookup"><span data-stu-id="47365-113">On-hand quantities for inventory items</span></span>
* <span data-ttu-id="47365-114">Öppna dokument för kunder och leverantörer, till exempel fakturor, kreditnotor och betalningar</span><span class="sxs-lookup"><span data-stu-id="47365-114">Open documents for customers and vendors, such as invoices, credit memos, and payments</span></span>

<span data-ttu-id="47365-115">Vi migrerar endast hela belopp på försäljnings- och inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="47365-115">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="47365-116">Vi uppdaterar inte delvis betalda belopp.</span><span class="sxs-lookup"><span data-stu-id="47365-116">We do not update partially paid amounts.</span></span> <span data-ttu-id="47365-117">Exempelvis om en kund har betalat 300 av totalt 500 kronor på en försäljningsfaktura, migrerar vi hela 500.</span><span class="sxs-lookup"><span data-stu-id="47365-117">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="47365-118">Om du har fått delbetalningar, måste du uppdatera dessa manuellt innan eller efter du migrerar data.</span><span class="sxs-lookup"><span data-stu-id="47365-118">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="47365-119">Vi rekommenderar att installera utestående transaktioner innan du migrerar för att underlätta efteråt.</span><span class="sxs-lookup"><span data-stu-id="47365-119">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]  
>   <span data-ttu-id="47365-120">Vi migrerar inte inköpsorder eller försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="47365-120">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="47365-121">Innan du börjar</span><span class="sxs-lookup"><span data-stu-id="47365-121">Before you start</span></span>
<span data-ttu-id="47365-122">En viktig del av är att ange konton för att migrera transaktionerna till.</span><span class="sxs-lookup"><span data-stu-id="47365-122">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="47365-123">Det är praktiskt att planera den här mappningen innan du migrerar data.</span><span class="sxs-lookup"><span data-stu-id="47365-123">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="47365-124">Exempelvis konton där du bokför transaktioner för:</span><span class="sxs-lookup"><span data-stu-id="47365-124">For example, the accounts where you post transactions for:</span></span>  

* <span data-ttu-id="47365-125">Försäljning av artiklar eller tjänster till kunder.</span><span class="sxs-lookup"><span data-stu-id="47365-125">The sale of items or services to customers.</span></span>
* <span data-ttu-id="47365-126">Köp av varor eller tjänster från en leverantör.</span><span class="sxs-lookup"><span data-stu-id="47365-126">The purchase of items or services from vendors.</span></span>  
* <span data-ttu-id="47365-127">Justeringar i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="47365-127">Adjustments in the general ledger.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="47365-128"> kräver att redovisningskonton har tilldelade kontonummer.</span><span class="sxs-lookup"><span data-stu-id="47365-128"> requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="47365-129">Kontrollera att nummer tilldelas till kontona i QuickBooks Online.</span><span class="sxs-lookup"><span data-stu-id="47365-129">Make sure that account numbers are assigned to your accounts in QuickBooks Online.</span></span>

<span data-ttu-id="47365-130">Transaktioner i QuickBooks Online måste ha skattebelopp, du ställer in ett skattekonto för din skattemyndighet i [!INCLUDE[d365fin](includes/d365fin_md.md)] innan du kan bokföra transaktioner.</span><span class="sxs-lookup"><span data-stu-id="47365-130">If transactions in QuickBooks Online have tax amounts, you must set up a tax account for your tax jurisdictions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you can post transactions.</span></span>

## <a name="how-do-i-start-using-the-extension"></a><span data-ttu-id="47365-131">Hur börjar jag använda tillägget?</span><span class="sxs-lookup"><span data-stu-id="47365-131">How do I start using the extension?</span></span>
<span data-ttu-id="47365-132">Komma igång enkelt.</span><span class="sxs-lookup"><span data-stu-id="47365-132">Getting started is easy.</span></span> <span data-ttu-id="47365-133">Allt du behöver göra är att köra den assisterade guiden **datamigrering**.</span><span class="sxs-lookup"><span data-stu-id="47365-133">All you need to do is run the **Data Migration** assisted setup guide.</span></span> <span data-ttu-id="47365-134">Så här gör du:</span><span class="sxs-lookup"><span data-stu-id="47365-134">Here's how:</span></span>

1. <span data-ttu-id="47365-135">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Assisterad konfiguration** och välj sedan **Migrera affärsdata**.</span><span class="sxs-lookup"><span data-stu-id="47365-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose **Migrate business data**.</span></span>
2. <span data-ttu-id="47365-136">Följ instruktionerna i varje steg i guiden assisterad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="47365-136">Follow the instructions on each step in the assisted setup guide.</span></span>

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="47365-137">Vad gör jag efter att jag har migrerat data?</span><span class="sxs-lookup"><span data-stu-id="47365-137">What do I do after I migrate data?</span></span>
<span data-ttu-id="47365-138">När du har migrerat data har transaktionerna statusen **ej bokförda**, så att du kan granska dem och göra ändringar.</span><span class="sxs-lookup"><span data-stu-id="47365-138">After you migrate data, transactions have the status **Unposted**, so you can review them and make adjustments.</span></span> <span data-ttu-id="47365-139">Gå till sidan där du normalt hittar dem om du vill granska transaktionerna.</span><span class="sxs-lookup"><span data-stu-id="47365-139">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="47365-140">Till exempel för att visa ej bokförda fakturor, går du till sidan **försäljningsfakturor**.</span><span class="sxs-lookup"><span data-stu-id="47365-140">For example, to review unposted sales invoices, go to the **Sales Invoices** page.</span></span> <span data-ttu-id="47365-141">Om du vill gå igenom journaler, går du till sidan **betalningsjournaler**.</span><span class="sxs-lookup"><span data-stu-id="47365-141">To review payment journals, go to the **Payment Journals** page.</span></span>   

<span data-ttu-id="47365-142">Det finns några saker som du bör göra:</span><span class="sxs-lookup"><span data-stu-id="47365-142">There are a few things in particular that you should do:</span></span>

* <span data-ttu-id="47365-143">Om transaktionerna i QuickBooks Online har markerade eller rabatterade belopp måste du manuellt lägga till beloppen till de relaterade transaktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)]innan du bokför dem.</span><span class="sxs-lookup"><span data-stu-id="47365-143">If the transactions in QuickBooks Online had markup or discount amounts, you must manually add the amounts to the related transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you post them.</span></span>
* <span data-ttu-id="47365-144">Om du använder moms kan du behöva lägga till en rörelsebokföringsmall och en produktbokföringsmall till bokföringsinställningar så att du kan bokföra moms.</span><span class="sxs-lookup"><span data-stu-id="47365-144">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
* <span data-ttu-id="47365-145">Kontrollera de ingående saldona för konton i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="47365-145">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="47365-146">QuickBooks Online sparar inte aktuellt saldo för alla konton, så du kan behöva åtgärda ingående saldon.</span><span class="sxs-lookup"><span data-stu-id="47365-146">QuickBooks Online does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="47365-147">Se även</span><span class="sxs-lookup"><span data-stu-id="47365-147">See Also</span></span>
[<span data-ttu-id="47365-148">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="47365-148">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="47365-149">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="47365-149">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  

