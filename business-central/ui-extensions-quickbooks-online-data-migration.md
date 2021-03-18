---
title: Tillägg för QuickBooks Online-migrering | Microsoft Docs
description: Beskriver hur du använder tillägget för att migrera kunder, leverantörer, artiklar och konton från QuickBooks Online till Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 6eb05acc55c86ce8547c2b18b933d669787583d4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386405"
---
# <a name="the-quickbooks-online-data-migration-extension"></a><span data-ttu-id="ff61e-103">Tillägget QuickBooks Online datamigrering</span><span class="sxs-lookup"><span data-stu-id="ff61e-103">The QuickBooks Online Data Migration Extension</span></span>

<span data-ttu-id="ff61e-104">Tillägget ingår i assisterade guiden **datamigrering** som hjälper dig att migrera viktiga affärsdata från QuickBooks Online till [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="ff61e-104">This extension is included in the **Data Migration** assisted setup guide to help you migrate important business data from QuickBooks Online to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="ff61e-105">Detta är exempelvis användbart när företaget växer och du har bestämt dig för att uppgradera ditt program för hantering av företag genom att börja använda [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="ff61e-105">For example, this is useful when your business is growing, and you've decided to upgrade your business management app by starting to use [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="what-data-can-i-import-from-quickbooks-online"></a><span data-ttu-id="ff61e-106">Vilka data kan jag importera från QuickBooks Online?</span><span class="sxs-lookup"><span data-stu-id="ff61e-106">What data can I import from QuickBooks Online?</span></span>

<span data-ttu-id="ff61e-107">Du kan importera följande data från QuickBooks Online till [!INCLUDE[prod_short](includes/prod_short.md)]:</span><span class="sxs-lookup"><span data-stu-id="ff61e-107">You can import the following data from QuickBooks Online to [!INCLUDE[prod_short](includes/prod_short.md)]:</span></span>  

* <span data-ttu-id="ff61e-108">Kunder</span><span class="sxs-lookup"><span data-stu-id="ff61e-108">Customers</span></span>
* <span data-ttu-id="ff61e-109">Leverantör</span><span class="sxs-lookup"><span data-stu-id="ff61e-109">Vendors</span></span>
* <span data-ttu-id="ff61e-110">Artiklar</span><span class="sxs-lookup"><span data-stu-id="ff61e-110">Items</span></span>
* <span data-ttu-id="ff61e-111">Kontoplan</span><span class="sxs-lookup"><span data-stu-id="ff61e-111">Chart of accounts</span></span>
* <span data-ttu-id="ff61e-112">Transaktion för ingående saldo i redovisningen</span><span class="sxs-lookup"><span data-stu-id="ff61e-112">Beginning balance transaction in the general ledger</span></span>
* <span data-ttu-id="ff61e-113">Tillgängliga kvantiteter för lagerartiklar</span><span class="sxs-lookup"><span data-stu-id="ff61e-113">On-hand quantities for inventory items</span></span>
* <span data-ttu-id="ff61e-114">Öppna dokument för kunder och leverantörer, till exempel fakturor, kreditnotor och betalningar</span><span class="sxs-lookup"><span data-stu-id="ff61e-114">Open documents for customers and vendors, such as invoices, credit memos, and payments</span></span>

<span data-ttu-id="ff61e-115">Vi migrerar endast hela belopp på försäljnings- och inköpsdokument.</span><span class="sxs-lookup"><span data-stu-id="ff61e-115">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="ff61e-116">Vi uppdaterar inte delvis betalda belopp.</span><span class="sxs-lookup"><span data-stu-id="ff61e-116">We do not update partially paid amounts.</span></span> <span data-ttu-id="ff61e-117">Exempelvis om en kund har betalat 300 av totalt 500 kronor på en försäljningsfaktura, migrerar vi hela 500.</span><span class="sxs-lookup"><span data-stu-id="ff61e-117">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="ff61e-118">Om du har fått delbetalningar, måste du uppdatera dessa manuellt innan eller efter du migrerar data.</span><span class="sxs-lookup"><span data-stu-id="ff61e-118">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="ff61e-119">Vi rekommenderar att installera utestående transaktioner innan du migrerar för att underlätta efteråt.</span><span class="sxs-lookup"><span data-stu-id="ff61e-119">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]  
> <span data-ttu-id="ff61e-120">Vi migrerar inte inköpsorder eller försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="ff61e-120">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="ff61e-121">Innan du börjar</span><span class="sxs-lookup"><span data-stu-id="ff61e-121">Before you start</span></span>

<span data-ttu-id="ff61e-122">En viktig del av är att ange konton för att migrera transaktionerna till.</span><span class="sxs-lookup"><span data-stu-id="ff61e-122">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="ff61e-123">Det är praktiskt att planera den här mappningen innan du migrerar data.</span><span class="sxs-lookup"><span data-stu-id="ff61e-123">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="ff61e-124">Exempelvis konton där du bokför transaktioner för:</span><span class="sxs-lookup"><span data-stu-id="ff61e-124">For example, the accounts where you post transactions for:</span></span>  

* <span data-ttu-id="ff61e-125">Försäljning av artiklar eller tjänster till kunder.</span><span class="sxs-lookup"><span data-stu-id="ff61e-125">The sale of items or services to customers.</span></span>
* <span data-ttu-id="ff61e-126">Köp av varor eller tjänster från en leverantör.</span><span class="sxs-lookup"><span data-stu-id="ff61e-126">The purchase of items or services from vendors.</span></span>  
* <span data-ttu-id="ff61e-127">Justeringar i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="ff61e-127">Adjustments in the general ledger.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="ff61e-128">kräver att redovisningskonton har tilldelade kontonummer.</span><span class="sxs-lookup"><span data-stu-id="ff61e-128">requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="ff61e-129">Kontrollera att nummer tilldelas till kontona i QuickBooks Online.</span><span class="sxs-lookup"><span data-stu-id="ff61e-129">Make sure that account numbers are assigned to your accounts in QuickBooks Online.</span></span>

<span data-ttu-id="ff61e-130">Transaktioner i QuickBooks Online måste ha skattebelopp, du ställer in ett skattekonto för din skattemyndighet i [!INCLUDE[prod_short](includes/prod_short.md)] innan du kan bokföra transaktioner.</span><span class="sxs-lookup"><span data-stu-id="ff61e-130">If transactions in QuickBooks Online have tax amounts, you must set up a tax account for your tax jurisdictions in [!INCLUDE[prod_short](includes/prod_short.md)] before you can post transactions.</span></span>

## <a name="how-do-i-start-using-the-extension"></a><span data-ttu-id="ff61e-131">Hur börjar jag använda tillägget?</span><span class="sxs-lookup"><span data-stu-id="ff61e-131">How do I start using the extension?</span></span>

<span data-ttu-id="ff61e-132">Komma igång enkelt.</span><span class="sxs-lookup"><span data-stu-id="ff61e-132">Getting started is easy.</span></span> <span data-ttu-id="ff61e-133">Allt du behöver göra är att köra den assisterade guiden **datamigrering**.</span><span class="sxs-lookup"><span data-stu-id="ff61e-133">All you need to do is run the **Data Migration** assisted setup guide.</span></span> <span data-ttu-id="ff61e-134">Så här gör du:</span><span class="sxs-lookup"><span data-stu-id="ff61e-134">Here's how:</span></span>

1. <span data-ttu-id="ff61e-135">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Assisterad konfiguration** och sedan **Migrera affärsdata**.</span><span class="sxs-lookup"><span data-stu-id="ff61e-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Assisted Setup**, and then choose **Migrate business data**.</span></span>
2. <span data-ttu-id="ff61e-136">Följ instruktionerna i varje steg i guiden assisterad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ff61e-136">Follow the instructions on each step in the assisted setup guide.</span></span>

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="ff61e-137">Vad gör jag efter att jag har migrerat data?</span><span class="sxs-lookup"><span data-stu-id="ff61e-137">What do I do after I migrate data?</span></span>

<span data-ttu-id="ff61e-138">När du har migrerat data har transaktionerna statusen **ej bokförda**, så att du kan granska dem och göra ändringar.</span><span class="sxs-lookup"><span data-stu-id="ff61e-138">After you migrate data, transactions have the status **Unposted**, so you can review them and make adjustments.</span></span> <span data-ttu-id="ff61e-139">Gå till sidan där du normalt hittar dem om du vill granska transaktionerna.</span><span class="sxs-lookup"><span data-stu-id="ff61e-139">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="ff61e-140">Till exempel för att visa ej bokförda fakturor, går du till sidan **försäljningsfakturor**.</span><span class="sxs-lookup"><span data-stu-id="ff61e-140">For example, to review unposted sales invoices, go to the **Sales Invoices** page.</span></span> <span data-ttu-id="ff61e-141">Om du vill gå igenom journaler, går du till sidan **betalningsjournaler**.</span><span class="sxs-lookup"><span data-stu-id="ff61e-141">To review payment journals, go to the **Payment Journals** page.</span></span>  

<span data-ttu-id="ff61e-142">Det finns några saker som du bör göra:</span><span class="sxs-lookup"><span data-stu-id="ff61e-142">There are a few things in particular that you should do:</span></span>

* <span data-ttu-id="ff61e-143">Om transaktionerna i QuickBooks Online har markerade eller rabatterade belopp måste du manuellt lägga till beloppen till de relaterade transaktionerna i [!INCLUDE[prod_short](includes/prod_short.md)] innan du bokför dem.</span><span class="sxs-lookup"><span data-stu-id="ff61e-143">If the transactions in QuickBooks Online had markup or discount amounts, you must manually add the amounts to the related transactions in [!INCLUDE[prod_short](includes/prod_short.md)] before you post them.</span></span>
* <span data-ttu-id="ff61e-144">Om du använder moms kan du behöva lägga till en rörelsebokföringsmall och en produktbokföringsmall till bokföringsinställningar så att du kan bokföra moms.</span><span class="sxs-lookup"><span data-stu-id="ff61e-144">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
* <span data-ttu-id="ff61e-145">Kontrollera de ingående saldona för konton i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="ff61e-145">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="ff61e-146">QuickBooks Online sparar inte aktuellt saldo för alla konton, så du kan behöva åtgärda ingående saldon.</span><span class="sxs-lookup"><span data-stu-id="ff61e-146">QuickBooks Online does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff61e-147">Se även</span><span class="sxs-lookup"><span data-stu-id="ff61e-147">See Also</span></span>

[<span data-ttu-id="ff61e-148">Importera affärsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="ff61e-148">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="ff61e-149">[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="ff61e-149">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]