---
title: Spåra artiklar med artikelspårning
description: Det går att se i vilket sammanhang den artikelspårade artikeln har använts, d.v.s. hur och när den togs emot eller tillverkades, överfördes, såldes, förbrukades eller returnerades. Du kan också söka efter alla aktuella instanser av ett visst serie- eller partinummer i databasen. Det gör du med funktionerna Artikelspårning och Hitta transaktioner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbfe0237beb58f22d3be7bc388d7b2726f05d4ba
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214759"
---
# <a name="trace-item-tracked-items"></a><span data-ttu-id="7dbcc-105">Spåra artiklar med artikelspårning</span><span class="sxs-lookup"><span data-stu-id="7dbcc-105">Trace Item-Tracked Items</span></span>
<span data-ttu-id="7dbcc-106">Det går att se i vilket sammanhang den artikelspårade artikeln har använts, d.v.s. hur och när den togs emot eller tillverkades, överfördes, såldes, förbrukades eller returnerades.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-106">You can see where an item-tracked item was used, including how and when it was received or produced, transferred, sold, consumed, or returned.</span></span> <span data-ttu-id="7dbcc-107">Du kan också söka efter alla aktuella instanser av ett visst serie- eller partinummer i databasen.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-107">You can also find all current instances of a specific serial or lot number in the database.</span></span> <span data-ttu-id="7dbcc-108">Det gör du med funktionerna Artikelspårning och [Hitta transaktioner](ui-find-entries.md).</span><span class="sxs-lookup"><span data-stu-id="7dbcc-108">You do this by using the Item Tracing and the [Find Entries](ui-find-entries.md) features.</span></span>  

<span data-ttu-id="7dbcc-109">Funktionerna kan vara särskilt användbara när det gäller kvalitetskontrollen i följande fall: när användaren vill få information om vilka kunder som tog emot produkter med ett visst partinummer eller när användaren vill få information om vilket parti en defekt komponent har sitt ursprung i.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-109">These features can be particularly useful in quality control when you need to find out which customers received products with a particular lot number or when you need to find out which lot a defective component came from.</span></span>  

 <span data-ttu-id="7dbcc-110">På sidan **Artikelspårning** kan du spåra framåt och bakåt i en serie bokförda lagertransaktioner efter serie- eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-110">On the **Item Tracing** page, you can trace forwards and backwards in a sequence of posted inventory transactions for the serial or lot number.</span></span>  

 <span data-ttu-id="7dbcc-111">På sidan **Hitta transaktioner** kan du inte se sekvensen av transaktioner, men du kan se alla transaktioner av serie- eller partinummer, både bokförda transaktioner och öppna transaktioner.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-111">On the **Find Entries** page, you cannot see the sequence of transactions, but you can see all records of the serial or lot number, both posted entries and open records.</span></span>  

 <span data-ttu-id="7dbcc-112">De två funktionerna kan användas tillsammans genom att överföra ett spårat serie- eller partinummer till sidan **Hitta transaktioner** för att slutföra ett spårningsscenario.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-112">The two features can be used in combination by transferring a traced serial or lot number to the **Find Entries** page to finish a complete trace scenario.</span></span> <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items"></a><span data-ttu-id="7dbcc-113">Se spårade artiklar</span><span class="sxs-lookup"><span data-stu-id="7dbcc-113">To trace item-tracked items</span></span>  

1.  <span data-ttu-id="7dbcc-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Artikelspårning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Tracing**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7dbcc-115">I filterfälten längst upp på sidan ska de specifika artikelnumren anges eller ett filter för artikelnumren som ska spåras.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-115">In the filter fields at the top of the page, enter the specific item numbers or a filter on the item numbers that you would like to trace.</span></span>  
3.  <span data-ttu-id="7dbcc-116">I fältet **Visa komponenter** väljer om ursprunget för artiklarnas komponenter dessutom ska visas.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-116">In the **Show Components** field, select whether you would like to also see where the components for the items came from.</span></span> <span data-ttu-id="7dbcc-117">Dina alternativ i det här fältet är följande.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-117">Your options in this field are as follows.</span></span>  

    |<span data-ttu-id="7dbcc-118">Fält</span><span class="sxs-lookup"><span data-stu-id="7dbcc-118">Field</span></span>|<span data-ttu-id="7dbcc-119">Description</span><span class="sxs-lookup"><span data-stu-id="7dbcc-119">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="7dbcc-120">**Nej**</span><span class="sxs-lookup"><span data-stu-id="7dbcc-120">**No**</span></span>|<span data-ttu-id="7dbcc-121">Genom att välja detta alternativ visas inga komponenter.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-121">Select this option if you do not want to see any components.</span></span>|  
    |<span data-ttu-id="7dbcc-122">**Endast artikelspårade**</span><span class="sxs-lookup"><span data-stu-id="7dbcc-122">**Item-tracked Only**</span></span>|<span data-ttu-id="7dbcc-123">Genom att välja detta alternativ visas endast komponenterna med parti- eller serienummer.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-123">Select this option if you want to see only components that have lot or serial numbers.</span></span>|  
    |<span data-ttu-id="7dbcc-124">**Allt**</span><span class="sxs-lookup"><span data-stu-id="7dbcc-124">**All**</span></span>|<span data-ttu-id="7dbcc-125">Genom att välja detta alternativ visas alla komponenter.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-125">Select this option if you want to see all components.</span></span>|  

4.  <span data-ttu-id="7dbcc-126">I fältet **Spårningsmetod** väljer du den metod som ska användas för att spåra artikeln.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-126">In the **Trace Method** field, select the method you would like to use for tracing the item.</span></span> <span data-ttu-id="7dbcc-127">Alternativen är följande</span><span class="sxs-lookup"><span data-stu-id="7dbcc-127">The options are as follows</span></span>  

    |<span data-ttu-id="7dbcc-128">Fält</span><span class="sxs-lookup"><span data-stu-id="7dbcc-128">Field</span></span>|<span data-ttu-id="7dbcc-129">Description</span><span class="sxs-lookup"><span data-stu-id="7dbcc-129">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="7dbcc-130">**Förbrukning-> Ursprung**</span><span class="sxs-lookup"><span data-stu-id="7dbcc-130">**Usage->Origin**</span></span>|<span data-ttu-id="7dbcc-131">Med den här metoden börjar artikelspårningen från platsen där artikeln användes till platsen som den kom ifrån.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-131">This method traces the item starting from where it was used to where it came from.</span></span> <span data-ttu-id="7dbcc-132">Till exempel om en tillverkad artikel har sålts till en kund, visar sidan **Artikelspårning** detta med utleveransraden först, som du kan därefter kan expandera för att visa från vilken produktionsorder artikeln har sitt ursprung.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-132">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the sales shipment line first, which you can then expand to see from which production order it came.</span></span>|  
    |<span data-ttu-id="7dbcc-133">**Förbrukning-> Ursprung**</span><span class="sxs-lookup"><span data-stu-id="7dbcc-133">**Origin->Usage**</span></span>|<span data-ttu-id="7dbcc-134">Med den här metoden börjar artikelspårningen från platsen där artikeln lagerfördes till platsen där den användes.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-134">This method traces the item starting from where it came into inventory to where it was used.</span></span> <span data-ttu-id="7dbcc-135">Till exempel om en tillverkad artikel har sålts till en kund, visar sidan **Artikelspårning** detta med den färdiga produktionsordern först, som du kan därefter kan expandera för att visa på vilken utleveransrad artikeln användes.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-135">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the finished production order first, which you can then expand to see sale shipment lines where the item was used.</span></span>|  

5.  <span data-ttu-id="7dbcc-136">Välj åtgärden **Spåra** för att utföra spårningen.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-136">Choose the **Trace** action to run the trace.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7dbcc-137">Om du har tagit emot samma parti i flera transaktioner, kanske sidan **Artikelspårning** inte visar alla transaktioner.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-137">If you have received the same lot on more transactions, then the **Item Tracing** page may not show all transactions.</span></span> <span data-ttu-id="7dbcc-138">Endast kopplade transaktioner visas.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-138">Only applied transactions are shown.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7dbcc-139">Om ytterligare transaktionshistorik under en artikelspåringsrad redan har spårats av en annan rad ovanför denna, är kryssrutan **Redan spårad** markerad.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-139">If additional transaction history under an item tracing line has already been traced by another line above it, then the **Already Traced** check box is selected.</span></span> <span data-ttu-id="7dbcc-140">För att förenkla vyn och göra den tydligare visas inte sådana underliggande rader.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-140">To provide a simpler view, such underlying lines are not shown.</span></span>  
>   
>  <span data-ttu-id="7dbcc-141">Välj **Gå till redan spårat** om du vill söka efter artikelspårningsrader där transaktionshistoriken redan har spårats.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-141">To find the item tracing lines where the transaction history has already been traced, choose the **Go to Already Traced** button.</span></span> <span data-ttu-id="7dbcc-142">Den aktuella artikelspårnings raden är markerad, och alla underliggande rader expanderade.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-142">The item tracing line in question is selected, and all underlying lines are expanded.</span></span>  

## <a name="to-find-item-tracked-items-with-find-entries"></a><span data-ttu-id="7dbcc-143">Så här hittar du spårade artiklar med Hitta transaktioner</span><span class="sxs-lookup"><span data-stu-id="7dbcc-143">To find item-tracked items with Find Entries</span></span>  

1. <span data-ttu-id="7dbcc-144">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Hitta transaktioner** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then select the related link.</span></span>  
2. <span data-ttu-id="7dbcc-145">Välj **Åtgärder** > **Sök efter** > **Sök efter artikelreferens**.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-145">Choose **Actions** > **Find by** > **Find by Item Reference**.</span></span>
3. <span data-ttu-id="7dbcc-146">I fälten **Serienr** och **Partinr** anger du artikelspårningsnumren som du vill spåra.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-146">In the **Serial No.** and **Lot No.** fields, enter the item tracking numbers that you want to trace.</span></span>  
4. <span data-ttu-id="7dbcc-147">Välj åtgärden **Sök** för att hitta alla instanser av serie- eller partinumret i databasen.</span><span class="sxs-lookup"><span data-stu-id="7dbcc-147">Choose the **Find** action to find all instances of the serial or lot number in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7dbcc-148">Se även</span><span class="sxs-lookup"><span data-stu-id="7dbcc-148">See Also</span></span>

[<span data-ttu-id="7dbcc-149">Lager</span><span class="sxs-lookup"><span data-stu-id="7dbcc-149">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="7dbcc-150">Arbeta med serienummer, partinummer och paketnummer</span><span class="sxs-lookup"><span data-stu-id="7dbcc-150">Work with Serial, Lot, and Package Numbers</span></span>](inventory-how-work-item-tracking.md)  
[<span data-ttu-id="7dbcc-151">Designdetaljer: Artikelkoppling</span><span class="sxs-lookup"><span data-stu-id="7dbcc-151">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="7dbcc-152">Designdetaljer: Artikelkoppling och reservationer</span><span class="sxs-lookup"><span data-stu-id="7dbcc-152">Design Details - Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="7dbcc-153">Reservera artiklar</span><span class="sxs-lookup"><span data-stu-id="7dbcc-153">Reserve Items</span></span>](inventory-how-to-reserve-items.md)  
<span data-ttu-id="7dbcc-154">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7dbcc-154">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[<span data-ttu-id="7dbcc-155">Hitta transaktioner</span><span class="sxs-lookup"><span data-stu-id="7dbcc-155">Find Entries</span></span>](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]