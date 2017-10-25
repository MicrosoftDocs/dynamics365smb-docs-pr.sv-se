---
title: "Så här kan du planera per order | Microsoft Docs"
description: "Den här planeringsuppgiften kan utföras i fönstret **Orderplanering** där du kan se alla nya behov samt tillgänglighetsinformation och förslag om leverans. Du ser allt du behöver veta och har tillgång till alla verktyg du behöver för att effektivt kunna planera hur du ska möta behov från försäljningsrader och komponentrader och direkt skapa olika typer av leveransorder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 143124fd2e458ee756d47d3f8523380cff6826a9
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-plan-for-new-demand-order-by-order"></a><span data-ttu-id="b7aa2-104">Så här: Planera för nya behov per order</span><span class="sxs-lookup"><span data-stu-id="b7aa2-104">How to: Plan for New Demand Order by Order</span></span>
<span data-ttu-id="b7aa2-105">Den här planeringsuppgiften kan utföras i fönstret **Orderplanering** där du kan se alla nya behov samt tillgänglighetsinformation och förslag om leverans.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-105">This planning task can be performed in the **Order Planning** window, which displays all new demand along with availability information and suggestions for supply.</span></span> <span data-ttu-id="b7aa2-106">Du ser allt du behöver veta och har tillgång till alla verktyg du behöver för att effektivt kunna planera hur du ska möta behov från försäljningsrader och komponentrader och direkt skapa olika typer av leveransorder.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-106">It provides the visibility and tools needed to effectively plan demand from sales lines and component lines and then create different types of supply orders directly.</span></span>  

<span data-ttu-id="b7aa2-107">Du kan gå till fönstret **Orderplanering** på två sätt beroende på vad ditt fokus: från en order som du vill planera för särskilt eller i batch-läge när du vill planera för alla och nya behov.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-107">You can enter the **Order Planning** window in two ways depending on your focus: From an order that you want to plan for specifically or in batch mode because you want to plan for all and any new demand.</span></span>  


## <a name="to-plan-for-new-production-order-demand"></a><span data-ttu-id="b7aa2-108">Så här planerar du för ett nytt produktionsorderbehov</span><span class="sxs-lookup"><span data-stu-id="b7aa2-108">To plan for new production order demand</span></span>  
1.  <span data-ttu-id="b7aa2-109">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Planerade produktionsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Planned Production Orders**, and then choose the related link.</span></span> <span data-ttu-id="b7aa2-110">(Du kan utföra dessa steg för en planerad, fast planerad eller släppt produktionsorder).</span><span class="sxs-lookup"><span data-stu-id="b7aa2-110">(You can perform these steps for planned, firm planned, or released production orders).</span></span>
2.  <span data-ttu-id="b7aa2-111">Öppna produktionsordern som du vill planera för och välj sedan den **Planering** åtgärd.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-111">Open the production order you want to plan for, and then choose the **Planning** action.</span></span>  
3.  <span data-ttu-id="b7aa2-112">I fönstret **Orderplanering** väljer du åtgärden **Skapa inköpsförslag**.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-112">In the **Order Planning** window, choose the **Calculate Plan** action.</span></span>  

<span data-ttu-id="b7aa2-113">I fönstret visas planeringsrader enligt visningsfiltret **Produktionsbehov**, dvs komponentrader med ouppfyllda behov från alla befintliga produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-113">The window displays planning lines according to the view filter **Production Demand**, meaning unfulfilled component lines of all existing production orders.</span></span> <span data-ttu-id="b7aa2-114">Behov för endast en produktionsorder visas inte eftersom det är nödvändigt att planera för en produktionsorder med en översikt över behoven för möjliga tidigare komponentrader.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-114">Demand for only the one production order is not shown because it is necessary to plan for one production order with an overview of demand for potentially earlier components lines.</span></span> <span data-ttu-id="b7aa2-115">Planeringsraderna för produktionsorder som du öppnade fönstret från expanderas.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-115">Planning lines for the production order in context are expanded.</span></span>  

## <a name="to-plan-for-any-new-demand"></a><span data-ttu-id="b7aa2-116">Så här planerar du för valfritt nytt behov</span><span class="sxs-lookup"><span data-stu-id="b7aa2-116">To plan for any new demand</span></span>  
1. <span data-ttu-id="b7aa2-117">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Orderplanering** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Order Planning**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b7aa2-118">I fönstret **Orderplanering** väljer du åtgärden **Skapa inköpsförslag**.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-118">In the **Order Planning** window, choose the **Calculate Plan** action.</span></span>
3.  <span data-ttu-id="b7aa2-119">Välj knappen **Expandera (+)** framför datumet i fältet **Behövd datum** om du vill se de underliggande planeringsraderna som motsvarar behovsrader med otillräcklig tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-119">Choose the **Expand (+)** button in front of the date in the **Demand Date** field to see the underlying planning lines that represent demand lines with insufficient availability.</span></span>  
4.  <span data-ttu-id="b7aa2-120">Du kan se värden för varje expanderad planeringsrad (behovsrad) i informationsfält längst ned i fönstret.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-120">For each expanded planning line, that is, demand line, you can see values in information fields at the bottom of the window.</span></span>  

    |<span data-ttu-id="b7aa2-121">Alternativ</span><span class="sxs-lookup"><span data-stu-id="b7aa2-121">Option</span></span>|<span data-ttu-id="b7aa2-122">Description</span><span class="sxs-lookup"><span data-stu-id="b7aa2-122">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="b7aa2-123">**Antal på andra lagerställen**</span><span class="sxs-lookup"><span data-stu-id="b7aa2-123">**Qty. on Other Locations**</span></span>|<span data-ttu-id="b7aa2-124">Visar om artikeln finns på ett annat lagerställe.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-124">Shows if the item exists on another location.</span></span> <span data-ttu-id="b7aa2-125">I så fall kan du söka efter den och markera den.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-125">You can then look up and select it.</span></span>|  
    |<span data-ttu-id="b7aa2-126">**Ersättningar finns**</span><span class="sxs-lookup"><span data-stu-id="b7aa2-126">**Substitutes Exist**</span></span>|<span data-ttu-id="b7aa2-127">Visar om en ersättningsartikel har skapats för artikeln.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-127">Shows if a substitute item is created for the item.</span></span> <span data-ttu-id="b7aa2-128">I så fall kan du söka efter den och markera den.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-128">You can then look up and select it.</span></span> <span data-ttu-id="b7aa2-129">Observera att den här funktionen bara kan användas för komponenter, dvs från behovsrader av typen **Produktion**.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-129">Note that this feature only applies to components, that is, from demand lines of type **Production**.</span></span>|  
    |<span data-ttu-id="b7aa2-130">**Disponibelt antal**</span><span class="sxs-lookup"><span data-stu-id="b7aa2-130">**Quantity Available**</span></span>|<span data-ttu-id="b7aa2-131">Visar den totala tillgängligheten för artikeln (Lagerutveckling över tiden).</span><span class="sxs-lookup"><span data-stu-id="b7aa2-131">Shows the total availability of the item, that is, the Projected Available Balance.</span></span>|  
    |<span data-ttu-id="b7aa2-132">**Tidigast disponibelt den**</span><span class="sxs-lookup"><span data-stu-id="b7aa2-132">**Earliest Date Available**</span></span>|<span data-ttu-id="b7aa2-133">Visar införseldatum för en inkommande leveransorder som kan täcka behovskvantiteten, men på ett datum som är senare än behovsdatumet.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-133">Shows the arrival date of an inbound supply order that can cover the needed quantity on a date later than the demand date.</span></span>|  

5.  <span data-ttu-id="b7aa2-134">I fältet **Återanskaffningssystem** väljer du vilken typ av leveransorder som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-134">In the **Replenishment System** field, select which type of supply order to create.</span></span>  

    <span data-ttu-id="b7aa2-135">Standardvärdet är värdet på artikelkortet (eller kortet för lagerställeenhet), men du kan ändra det till något av följande tre alternativ:</span><span class="sxs-lookup"><span data-stu-id="b7aa2-135">The default value is that of the item card, or SKU card, but you can change it to one of three options:</span></span>  

    |<span data-ttu-id="b7aa2-136">Alternativ</span><span class="sxs-lookup"><span data-stu-id="b7aa2-136">Option</span></span>|<span data-ttu-id="b7aa2-137">Description</span><span class="sxs-lookup"><span data-stu-id="b7aa2-137">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="b7aa2-138">**Inköp**</span><span class="sxs-lookup"><span data-stu-id="b7aa2-138">**Purchase**</span></span>|<span data-ttu-id="b7aa2-139">Skapar en inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-139">Creates a purchase order.</span></span>|  
    |<span data-ttu-id="b7aa2-140">**Överföring**</span><span class="sxs-lookup"><span data-stu-id="b7aa2-140">**Transfer**</span></span>|<span data-ttu-id="b7aa2-141">Skapar en överföringsorder.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-141">Creates a transfer order.</span></span>|  
    |<span data-ttu-id="b7aa2-142">**Prod.order**</span><span class="sxs-lookup"><span data-stu-id="b7aa2-142">**Prod. Order**</span></span>|<span data-ttu-id="b7aa2-143">Skapar en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-143">Creates a production order.</span></span>|  

    <span data-ttu-id="b7aa2-144">I fönstret **Leverera från** måste du välja ett värde enligt det återanskaffningssystem som du har markerat.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-144">In the **Supply From** field you must select a value according to the selected replenishment system.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="b7aa2-145">Om fältet inte fylls i visas ett felmeddelande när du använder funktionen **Skapa leveransorder**, och ingen leveransorder skapas för den aktuella planeringsraden.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-145">If the field is not filled in, the system will display an error message when you use the **Make Supply Order** function, and no supply order will be created for the planning line in question.</span></span> <span data-ttu-id="b7aa2-146">Detta gäller inte om återanskaffningssystemet är **Prod.order**.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-146">This, however, is not the case if the replenishment system is **Prod. Order**.</span></span>  

6.  <span data-ttu-id="b7aa2-147">I fältet **Leverera från** kan du söka i lämplig lista och välja varifrån leveransen ska ske:</span><span class="sxs-lookup"><span data-stu-id="b7aa2-147">From the **Supply From** field, you can look up in the relevant list and select where the supply should come from:</span></span>  

    - <span data-ttu-id="b7aa2-148">Om återanskaffningssystemet är **Inköp** görs sökningen med sökknappen i fönstret **Artikelleverantörskatalog**.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-148">If replenishment system is **Purchase**, the look-up button in this field looks up in the **Item Vendor Catalog** window.</span></span>  
    - <span data-ttu-id="b7aa2-149">Om återanskaffningssystemet är **Överföring** görs sökningen med sökknappen i fönstret **Lagerställelista**.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-149">If replenishment system is **Transfer**, the look-up button in this field looks up in the **Location List** window.</span></span>  

    <span data-ttu-id="b7aa2-150">Om artikeln finns på ett annat lagerställe visas ett värde i fältet **Antal på andra lagerställen** längst ned, och du kan då söka efter och markera det lagerställe som artikeln ska levereras från när du skapar överföringsordern.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-150">In case the item exists in another location, the **Qty. on Other Location** field at the bottom shows a value and you can then look up and select the location from which the item should be supplied when you make the transfer order.</span></span>  

    <span data-ttu-id="b7aa2-151">Om det finns en ersättningsartikel för artikeln som behövs visas värdet **Ja** i fältet **Ersättningar finns**, och du kan då söka i fönstret **Artikelersättningstrans.** och markera ersättningsartikeln.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-151">If a substitute exists for the demanded item, the **Substitute Exists** field is set to **Yes**, and you can then look up to the **Item Substitution Entries** window and select the substitute.</span></span>  

7.  <span data-ttu-id="b7aa2-152">Markera kryssrutan **Reservera** om du vill skapa en reservation mellan leveransordern som du skapar och den behovsrad som den skapas för.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-152">Select the **Reserve** check box if you want to make a reservation between the supply order you are creating and the demand line that it is created for.</span></span> <span data-ttu-id="b7aa2-153">Som standard är fältet tomt.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-153">It is empty by default.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="b7aa2-154">Du kan bara markera den här kryssrutan om artikeln har **Valfri** eller **Alltid** i fältet **Reservera** på artikelkortet för artikeln.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-154">You can only select this check box if the item has **Optional** or **Always** in the **Reserve** field on its item card.</span></span>  

8.  <span data-ttu-id="b7aa2-155">I fältet **Kvant. mot order** kan du ange den kvantitet som ska anges på leveransordern som du skapar.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-155">In the **Qty. to Order** field, you can enter the quantity that will go on the supply order you are creating.</span></span>   
    <span data-ttu-id="b7aa2-156">Standardvärdet är samma kvantitet som i fältet **Behövt antal**.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-156">The default value is the same quantity as that in the **Needed Quantity** field.</span></span> <span data-ttu-id="b7aa2-157">Men du kan ange ett högre eller lägre värde utifrån din kunskap om behovssituationen.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-157">But you may decide to order more or less than this quantity based on your knowledge of the demand situation.</span></span> <span data-ttu-id="b7aa2-158">Om du till exempel, ser du i fönstret **Orderplanering** att flera ej relaterade behovsrader är för samma inköpta artikel, och, dessa är kring samma datum, kan du kan konsolidera dessa genom att ange den totala behovskvantiteten i fältet **Antal i order** på en rad och sedan ta bort andra, föråldrade planeringsrader för artikeln.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-158">If, for example, you see in the **Order Planning** window that several unrelated demand lines are for the same purchased item, and they are due around the same date, you can consolidate these by entering the total needed quantity in the **Qty. to Order** field of one line, and then delete the other, obsolete planning lines for that item.</span></span>  

9.  <span data-ttu-id="b7aa2-159">I fälten **Förfallodatum** och **Orderdatum** kan du ange de datum som ska gälla för de leveransorder som skapas.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-159">In the **Due Date** and **Order Date** fields, you can enter the dates that should apply to the created supply orders.</span></span>  

    <span data-ttu-id="b7aa2-160">De här två fälten är beroende av varandra i enlighet med värdet i fältet **Standard säkerhetsledtid** som finns under **Produktionsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-160">These two fields are interrelated according to the **Default Safety Lead Time** field, which can be found in the **Manufacturing Setup** window.</span></span> <span data-ttu-id="b7aa2-161">Som standard är värdet för Förfallodatum detsamma som för Behovsdatum, men du kan ändra detta om du vill.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-161">By default, the due date is the same as the demand date, but you can change this as you like.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b7aa2-162"> Om du anger ett senare datum än behovsdatumet får du ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-162">If you enter a date later than the demand date, you will receive a warning message.</span></span>  

## <a name="to-make-supply-orders"></a><span data-ttu-id="b7aa2-163">Så här skapar du leveransorder</span><span class="sxs-lookup"><span data-stu-id="b7aa2-163">To make supply orders</span></span>  
1.  <span data-ttu-id="b7aa2-164">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Planerade produktionsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-164">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Planned Production Orders**, and then choose the related link.</span></span> <span data-ttu-id="b7aa2-165">Du kan utföra dessa steg för en planerad, fast planerad eller släppt produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-165">You can perform these steps for a planned, firm planned, or released production order.</span></span>  
2.  <span data-ttu-id="b7aa2-166">Öppna produktionsordern som du vill planera för och välj sedan den **Planering** åtgärd.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-166">Open the production order you want to plan for, and then choose the **Planning** action.</span></span>  
3.  <span data-ttu-id="b7aa2-167">Placera markören på en planeringsrad och klicka på åtgärder **Skapa order**.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-167">Place the cursor on a relevant planning line, and then choose the **Make Orders** action.</span></span>  
4.  <span data-ttu-id="b7aa2-168">I fönstret **Skapa leveransorder** på snabbfliken **Orderplanering** , i fältet **Skapa order för**, markera ett av följande alternativ.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-168">In the **Make Supply Orders** window, on the **Order Planning** FastTab, in the **Make Orders for** field, select one of the following options.</span></span>  

    |<span data-ttu-id="b7aa2-169">Alternativ</span><span class="sxs-lookup"><span data-stu-id="b7aa2-169">Option</span></span>|<span data-ttu-id="b7aa2-170">Description</span><span class="sxs-lookup"><span data-stu-id="b7aa2-170">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="b7aa2-171">**den aktiva raden**</span><span class="sxs-lookup"><span data-stu-id="b7aa2-171">**The Active Line**</span></span>|<span data-ttu-id="b7aa2-172">Skapa en leveransorder för den rad där markören finns.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-172">Make a supply order only for the line where the cursor is placed.</span></span>|  
    |<span data-ttu-id="b7aa2-173">**den aktiva ordern**</span><span class="sxs-lookup"><span data-stu-id="b7aa2-173">**The Active Order**</span></span>|<span data-ttu-id="b7aa2-174">Skapa en leveransorder för alla rader i ordern där markören finns.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-174">Make supply orders for all lines in the order where the cursor is placed.</span></span>|  
    |<span data-ttu-id="b7aa2-175">**Alla rader**</span><span class="sxs-lookup"><span data-stu-id="b7aa2-175">**All Lines**</span></span>|<span data-ttu-id="b7aa2-176">Skapa leveransorder för alla rader i fönstret **Orderplanering**.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-176">Make supply orders for all lines in the **Order Planning** window.</span></span>|  

5.  <span data-ttu-id="b7aa2-177">På snabbfliken **Alternativ** anger du vilken typ av leveransorder, eller inköpsförslagsrader, som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-177">On the **Options** FastTab, define what kind of supply orders, or requisition worksheet lines, should be made.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="b7aa2-178">De inställningar som du gör i fönstret **Skapa leveransorder** sparas under ditt användar-ID, och de visas igen nästa gång du öppnar fönstret.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-178">The settings you last made in the **Make Supply Orders** window will be saved under your user ID so that they are the same the next time you use the window.</span></span>  

6.  <span data-ttu-id="b7aa2-179">Klicka på **OK** när du vill skapa angivna leveransorder eller inköpsförslagsrader.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-179">Choose the **OK** button to make the suggested supply orders or requisition worksheet lines.</span></span>  

<span data-ttu-id="b7aa2-180">Nu har du planerat för de ouppfyllda behoven genom att skapa motsvarande leveransorder.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-180">You have now planned for the unfulfilled demand by making respective supply orders.</span></span> <span data-ttu-id="b7aa2-181">Exakt hur du ska arbeta med fönstret **Orderplanering** beror på vad som gäller i just ditt företag.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-181">Details about specific work flows when using the **Order Planning** window would depend on a company’s internal policies.</span></span>  

<span data-ttu-id="b7aa2-182">När du är klar med planeringen i fönstret **Orderplanering**, och du till exempel har angett ett alternativt sätt att leverera kvantiteten, kan du fortsätta med att skapa leveransorder för en eller flera av planeringsraderna.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-182">When you have finished your planning work in the **Order Planning** window, for example defined an alternative way to supply the quantity, you can proceed to create supply orders for one or more of the planning lines.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b7aa2-183">De leveransorder som du skapar kan innebära att nya beroende behov uppstår, till exempel behov av underliggande produktionsorder, och därför bör du klicka på **Skapa inköpsförslag** igen för att identifiera dessa behov och hantera dem innan du går vidare i listan.</span><span class="sxs-lookup"><span data-stu-id="b7aa2-183">The supply orders you create may introduce new dependent demand, for example for underlying production orders, and you should therefore choose **Calculate Plan** again to find and resolve this before moving down the list.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b7aa2-184">Se även</span><span class="sxs-lookup"><span data-stu-id="b7aa2-184">See Also</span></span>  
[<span data-ttu-id="b7aa2-185">Planerad</span><span class="sxs-lookup"><span data-stu-id="b7aa2-185">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="b7aa2-186">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="b7aa2-186">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="b7aa2-187">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="b7aa2-187">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="b7aa2-188">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="b7aa2-188">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b7aa2-189">Inköp</span><span class="sxs-lookup"><span data-stu-id="b7aa2-189">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b7aa2-190">[Designdetaljer: Leveransplanering](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="b7aa2-190">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="b7aa2-191">Skapa metodtips: leveransplanering</span><span class="sxs-lookup"><span data-stu-id="b7aa2-191">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="b7aa2-192">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b7aa2-192">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
