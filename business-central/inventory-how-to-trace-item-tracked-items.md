---
title: "Spåra artiklar med artikelspårningar | Microsoft Docs"
description: "Det går att se i vilket sammanhang den artikelspårade artikeln har använts, d.v.s. hur och när den togs emot eller tillverkades, överfördes, såldes, förbrukades eller returnerades. Du kan också söka efter alla aktuella instanser av ett visst serie- eller partinummer i databasen. Det gör du med funktionerna för artikelspårning och analys."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: bf16f61e5c3d6ee6af045ded8ec80e426ae6c20a
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="trace-item-tracked-items"></a><span data-ttu-id="ed04e-105">Spåra artiklar med artikelspårning</span><span class="sxs-lookup"><span data-stu-id="ed04e-105">Trace Item-Tracked Items</span></span>
<span data-ttu-id="ed04e-106">Det går att se i vilket sammanhang den artikelspårade artikeln har använts, d.v.s. hur och när den togs emot eller tillverkades, överfördes, såldes, förbrukades eller returnerades.</span><span class="sxs-lookup"><span data-stu-id="ed04e-106">You can see where an item-tracked item was used, including how and when it was received or produced, transferred, sold, consumed, or returned.</span></span> <span data-ttu-id="ed04e-107">Du kan också söka efter alla aktuella instanser av ett visst serie- eller partinummer i databasen.</span><span class="sxs-lookup"><span data-stu-id="ed04e-107">You can also find all current instances of a specific serial or lot number in the database.</span></span> <span data-ttu-id="ed04e-108">Det gör du med funktionerna för artikelspårning och analys.</span><span class="sxs-lookup"><span data-stu-id="ed04e-108">You do this by using the Item Tracing and the Navigate features.</span></span>  

 <span data-ttu-id="ed04e-109">Funktionerna kan vara särskilt användbara när det gäller kvalitetskontrollen i följande fall: när användaren vill få information om vilka kunder som tog emot produkter med ett visst partinummer eller när användaren vill få information om vilket parti en defekt komponent har sitt ursprung i.</span><span class="sxs-lookup"><span data-stu-id="ed04e-109">These features can be particularly useful in quality control when you need to find out which customers received products with a particular lot number or when you need to find out which lot a defective component came from.</span></span>  

 <span data-ttu-id="ed04e-110">På sidan **Artikelspårning** kan du spåra framåt och bakåt i en serie bokförda lagertransaktioner efter serie- eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="ed04e-110">On the **Item Tracing** page, you can trace forwards and backwards in a sequence of posted inventory transactions for the serial or lot number.</span></span>  

 <span data-ttu-id="ed04e-111">På sidan **Navigera** kan du inte se sekvensen av transaktioner, men du kan se alla transaktioner av serie- eller partinummer, både bokförda transaktioner och öppna transaktioner.</span><span class="sxs-lookup"><span data-stu-id="ed04e-111">On the **Navigate** page, you cannot see the sequence of transactions, but you can see all records of the serial or lot number, both posted entries and open records.</span></span>  

 <span data-ttu-id="ed04e-112">De två funktionerna kan användas tillsammans genom att överföra ett spårat serie- eller partinummer till sidan **Navigera** för att slutföra ett spårningsscenario.</span><span class="sxs-lookup"><span data-stu-id="ed04e-112">The two features can be used in combination by transferring a traced serial or lot number to the **Navigate** page to finish a complete trace scenario.</span></span> <span data-ttu-id="ed04e-113">Mer information finns i [Genomgång: Spåra serienummer/partinummer](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="ed04e-113">For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>  

## <a name="to-trace-item-tracked-items"></a><span data-ttu-id="ed04e-114">Se spårade artiklar</span><span class="sxs-lookup"><span data-stu-id="ed04e-114">To trace item-tracked items</span></span>  

1.  <span data-ttu-id="ed04e-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artikelspårning** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ed04e-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Tracing**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ed04e-116">I filterfälten längst upp på sidan ska de specifika artikelnumren anges eller ett filter för artikelnumren som ska spåras.</span><span class="sxs-lookup"><span data-stu-id="ed04e-116">In the filter fields at the top of the page, enter the specific item numbers or a filter on the item numbers that you would like to trace.</span></span>  
3.  <span data-ttu-id="ed04e-117">I fältet **Visa komponenter** väljer om ursprunget för artiklarnas komponenter dessutom ska visas.</span><span class="sxs-lookup"><span data-stu-id="ed04e-117">In the **Show Components** field, select whether you would like to also see where the components for the items came from.</span></span> <span data-ttu-id="ed04e-118">Dina alternativ i det här fältet är följande.</span><span class="sxs-lookup"><span data-stu-id="ed04e-118">Your options in this field are as follows.</span></span>  

    |<span data-ttu-id="ed04e-119">Fält</span><span class="sxs-lookup"><span data-stu-id="ed04e-119">Field</span></span>|<span data-ttu-id="ed04e-120">Description</span><span class="sxs-lookup"><span data-stu-id="ed04e-120">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="ed04e-121">**Nej**</span><span class="sxs-lookup"><span data-stu-id="ed04e-121">**No**</span></span>|<span data-ttu-id="ed04e-122">Genom att välja detta alternativ visas inga komponenter.</span><span class="sxs-lookup"><span data-stu-id="ed04e-122">Select this option if you do not want to see any components.</span></span>|  
    |<span data-ttu-id="ed04e-123">**Endast artikelspårade**</span><span class="sxs-lookup"><span data-stu-id="ed04e-123">**Item-tracked Only**</span></span>|<span data-ttu-id="ed04e-124">Genom att välja detta alternativ visas endast komponenterna med parti- eller serienummer.</span><span class="sxs-lookup"><span data-stu-id="ed04e-124">Select this option if you want to see only components that have lot or serial numbers.</span></span>|  
    |<span data-ttu-id="ed04e-125">**Allt**</span><span class="sxs-lookup"><span data-stu-id="ed04e-125">**All**</span></span>|<span data-ttu-id="ed04e-126">Genom att välja detta alternativ visas alla komponenter.</span><span class="sxs-lookup"><span data-stu-id="ed04e-126">Select this option if you want to see all components.</span></span>|  

4.  <span data-ttu-id="ed04e-127">I fältet **Spårningsmetod** väljer du den metod som ska användas för att spåra artikeln.</span><span class="sxs-lookup"><span data-stu-id="ed04e-127">In the **Trace Method** field, select the method you would like to use for tracing the item.</span></span> <span data-ttu-id="ed04e-128">Alternativen är följande</span><span class="sxs-lookup"><span data-stu-id="ed04e-128">The options are as follows</span></span>  

    |<span data-ttu-id="ed04e-129">Fält</span><span class="sxs-lookup"><span data-stu-id="ed04e-129">Field</span></span>|<span data-ttu-id="ed04e-130">Description</span><span class="sxs-lookup"><span data-stu-id="ed04e-130">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="ed04e-131">**Förbrukning-> Ursprung**</span><span class="sxs-lookup"><span data-stu-id="ed04e-131">**Usage->Origin**</span></span>|<span data-ttu-id="ed04e-132">Med den här metoden börjar artikelspårningen från platsen där artikeln användes till platsen som den kom ifrån.</span><span class="sxs-lookup"><span data-stu-id="ed04e-132">This method traces the item starting from where it was used to where it came from.</span></span> <span data-ttu-id="ed04e-133">Till exempel om en tillverkad artikel har sålts till en kund, visar sidan **Artikelspårning** detta med utleveransraden först, som du kan därefter kan expandera för att visa från vilken produktionsorder artikeln har sitt ursprung.</span><span class="sxs-lookup"><span data-stu-id="ed04e-133">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the sales shipment line first, which you can then expand to see from which production order it came.</span></span>|  
    |<span data-ttu-id="ed04e-134">**Förbrukning-> Ursprung**</span><span class="sxs-lookup"><span data-stu-id="ed04e-134">**Origin->Usage**</span></span>|<span data-ttu-id="ed04e-135">Med den här metoden börjar artikelspårningen från platsen där artikeln lagerfördes till platsen där den användes.</span><span class="sxs-lookup"><span data-stu-id="ed04e-135">This method traces the item starting from where it came into inventory to where it was used.</span></span> <span data-ttu-id="ed04e-136">Till exempel om en tillverkad artikel har sålts till en kund, visar sidan **Artikelspårning** detta med den färdiga produktionsordern först, som du kan därefter kan expandera för att visa på vilken utleveransrad artikeln användes.</span><span class="sxs-lookup"><span data-stu-id="ed04e-136">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the finished production order first, which you can then expand to see sale shipment lines where the item was used.</span></span>|  

5.  <span data-ttu-id="ed04e-137">Välj åtgärden **Spåra** för att utföra spårningen.</span><span class="sxs-lookup"><span data-stu-id="ed04e-137">Choose the **Trace** action to run the trace.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ed04e-138">Om du har tagit emot samma parti i flera transaktioner, kanske sidan **Artikelspårning** inte visar alla transaktioner.</span><span class="sxs-lookup"><span data-stu-id="ed04e-138">If you have received the same lot on more transactions, then the **Item Tracing** page may not show all transactions.</span></span> <span data-ttu-id="ed04e-139">Endast kopplade transaktioner visas.</span><span class="sxs-lookup"><span data-stu-id="ed04e-139">Only applied transactions are shown.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ed04e-140">Om ytterligare transaktionshistorik under en artikelspåringsrad redan har spårats av en annan rad ovanför denna, är kryssrutan **Redan spårad** markerad.</span><span class="sxs-lookup"><span data-stu-id="ed04e-140">If additional transaction history under an item tracing line has already been traced by another line above it, then the **Already Traced** check box is selected.</span></span> <span data-ttu-id="ed04e-141">För att förenkla vyn och göra den tydligare visas inte sådana underliggande rader.</span><span class="sxs-lookup"><span data-stu-id="ed04e-141">To provide a simpler view, such underlying lines are not shown.</span></span>  
>   
>  <span data-ttu-id="ed04e-142">Välj **Gå till redan spårat** om du vill söka efter artikelspårningsrader där transaktionshistoriken redan har spårats.</span><span class="sxs-lookup"><span data-stu-id="ed04e-142">To find the item tracing lines where the transaction history has already been traced, choose the **Go to Already Traced** button.</span></span> <span data-ttu-id="ed04e-143">Den aktuella artikelspårnings raden är markerad, och alla underliggande rader expanderade.</span><span class="sxs-lookup"><span data-stu-id="ed04e-143">The item tracing line in question is selected, and all underlying lines are expanded.</span></span>  

## <a name="to-find-item-tracked-items-with-navigate"></a><span data-ttu-id="ed04e-144">Så här hittar du spårade artiklar med Analysera</span><span class="sxs-lookup"><span data-stu-id="ed04e-144">To find item-tracked items with Navigate</span></span>  

1.  <span data-ttu-id="ed04e-145">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Navigera** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ed04e-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Navigate**, and then select the related link.</span></span>  
2.  <span data-ttu-id="ed04e-146">På Snabbfliken **Artikelspårning**, i fälten **Serienr** och **Partinr**, anger du artikelspårningsnumren som du vill spåra.</span><span class="sxs-lookup"><span data-stu-id="ed04e-146">On the **Item Tracking** FastTab, in the **Serial No.** and **Lot No.** fields, enter the item tracking numbers that you want to trace.</span></span>  
3.  <span data-ttu-id="ed04e-147">Välj åtgärden **Sök** för att hitta alla instanser av serie- eller partinumret i databasen.</span><span class="sxs-lookup"><span data-stu-id="ed04e-147">Choose the **Find** action to find all instances of the serial or lot number in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ed04e-148">Se även</span><span class="sxs-lookup"><span data-stu-id="ed04e-148">See Also</span></span>  
[<span data-ttu-id="ed04e-149">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="ed04e-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ed04e-150">[Detaljer: Artikelspårning](design-details-item-tracking.md)
[Designdetaljer - artikelspårning och reservationer](design-details-item-tracking-and-reservations.md)</span><span class="sxs-lookup"><span data-stu-id="ed04e-150">[Design Details: Item Tracking](design-details-item-tracking.md)
[Design Details - Item Tracking and Reservations](design-details-item-tracking-and-reservations.md)</span></span>  
[<span data-ttu-id="ed04e-151">Reservera artiklar</span><span class="sxs-lookup"><span data-stu-id="ed04e-151">Reserve Items</span></span>](inventory-how-to-reserve-items.md)  
<span data-ttu-id="ed04e-152">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Genomgång: Spåra serienummer/partinummer](walkthrough-tracing-serial-lot-numbers.md)</span><span class="sxs-lookup"><span data-stu-id="ed04e-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)</span></span>

