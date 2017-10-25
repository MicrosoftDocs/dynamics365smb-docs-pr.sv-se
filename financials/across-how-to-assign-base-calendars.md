---
title: "Så här skapar du Baskalender | Microsoft Docs"
description: "Du kan tilldela företaget och dess affärspartner, till exempel kunder, leverantörer och lagerställen, en baskalender. De angivna arbetsdagarna i kalendern används för att beräkna leveransdatum och inleveransdatum på rader på försäljningsorder, inköpsorder, överföringsorder och produktionsorder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d37170cabe2b03200e3d3f5f7b5c2a679eb8f46c
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-base-calendars"></a><span data-ttu-id="592f2-104">Så här lägger du upp baskalendrar</span><span class="sxs-lookup"><span data-stu-id="592f2-104">How to: Set Up Base Calendars</span></span>
<span data-ttu-id="592f2-105">Du kan tilldela företaget och dess affärspartner, till exempel kunder, leverantörer och lagerställen, en baskalender.</span><span class="sxs-lookup"><span data-stu-id="592f2-105">You can assign a base calendar to your company and its business partners, such as customers, vendors, or locations.</span></span> <span data-ttu-id="592f2-106">De angivna arbetsdagarna i kalendern används för att beräkna leveransdatum och inleveransdatum på rader på försäljningsorder, inköpsorder, överföringsorder och produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="592f2-106">Delivery and receipt dates on future sales order, purchase order, transfer order, and production order lines are calculated according to the calendar’s specified working days.</span></span> <span data-ttu-id="592f2-107">Huvuduppgiften när du lägger upp en ny baskalender är att ange och definiera de lediga dagar som du vill ska gälla.</span><span class="sxs-lookup"><span data-stu-id="592f2-107">The main task in setting up a new base calendar is to specify and define the non-working days that you want to apply.</span></span>  

## <a name="to-set-up-a-base-calendar"></a><span data-ttu-id="592f2-108">Så här lägger du upp en baskalender</span><span class="sxs-lookup"><span data-stu-id="592f2-108">To set up a base calendar</span></span>  
1.  <span data-ttu-id="592f2-109">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Baskalender** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="592f2-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Base Calendar**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="592f2-110">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="592f2-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="592f2-111">Fyll i fältet **Kod**.</span><span class="sxs-lookup"><span data-stu-id="592f2-111">Fill in the **Code** field.</span></span>  
4. <span data-ttu-id="592f2-112">Välj åtgärden **Bibehåll baskalenderändringar**.</span><span class="sxs-lookup"><span data-stu-id="592f2-112">Choose the **Maintain Base Calendar Changes** action.</span></span>
5. <span data-ttu-id="592f2-113">I fönstret **baskalenderändringar** använd fältet **Återkommande system** för att markera ett visst datum eller en viss dag som återkommande ledig dag.</span><span class="sxs-lookup"><span data-stu-id="592f2-113">In the **Base Calendar Changes** window, use the **Recurring System** field to mark a particular date or day as a recurring nonworking day.</span></span> <span data-ttu-id="592f2-114">Du kan välja mellan alternativen **Årligen återkommande** eller **Veckovis återkommande**.</span><span class="sxs-lookup"><span data-stu-id="592f2-114">You can select either the **Annual Recurring** or **Weekly Recurring** option.</span></span>  

    <span data-ttu-id="592f2-115">Om du väljer **Årligen återkommande** måste du även ange vilket datum som avses i fältet **Datum**.</span><span class="sxs-lookup"><span data-stu-id="592f2-115">If you select **Annual Recurring**, you must also enter the relevant date in the **Date** field.</span></span>  

    <span data-ttu-id="592f2-116">Om du väljer **Veckovis återkommande** måste du även ange vilken veckodag som avses i fältet **Dag**.</span><span class="sxs-lookup"><span data-stu-id="592f2-116">If you select **Weekly Recurring**, you must also select the relevant day of the week in the **Day** field.</span></span> <span data-ttu-id="592f2-117">Om du lämnar fältet tomt, måste du fylla i fältet **Datum**.</span><span class="sxs-lookup"><span data-stu-id="592f2-117">If you leave the field empty, you must fill in the **Date** field.</span></span> <span data-ttu-id="592f2-118">Fältet **Dag** fylls i automatiskt.</span><span class="sxs-lookup"><span data-stu-id="592f2-118">The **Day** field is filled in automatically.</span></span>  

<span data-ttu-id="592f2-119">När du gör en transaktion är fältet **Ej arbetsdag** markerat.</span><span class="sxs-lookup"><span data-stu-id="592f2-119">When you make an entry, the **Nonworking** field is selected.</span></span> <span data-ttu-id="592f2-120">Du kan välja att ta bort markeringen för att göra detta till en arbetsdag.</span><span class="sxs-lookup"><span data-stu-id="592f2-120">You can choose to clear the check mark to make it a working day.</span></span>  
 <span data-ttu-id="592f2-121">När du återgår till baskalenderkortet kan du lägga märke till att de lediga dagar som du har angett har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="592f2-121">When you return to the base calendar card, you will observe that the nonworking day entries that you made have been updated.</span></span> <span data-ttu-id="592f2-122">Posterna är nu röda, och **Ej arbetsdag** är markerat.</span><span class="sxs-lookup"><span data-stu-id="592f2-122">These entries now appear in red and the **Nonworking** field is selected.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="592f2-123">När du lägger upp en ny baskalender kan du markera och kopiera rader från en befintligt kalender.</span><span class="sxs-lookup"><span data-stu-id="592f2-123">When setting up a new base calendar, you can select and copy lines from an existing calendar.</span></span> <span data-ttu-id="592f2-124">Det gör du i fönstret **Baskalenderändringar**.</span><span class="sxs-lookup"><span data-stu-id="592f2-124">You do this in the relevant **Base Calendar Changes** window.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="592f2-125">En baskalender som definierats för leverantörer eller lagerställe inverkar på hur datumen beräknas och avrundas till arbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="592f2-125">Any base calendar defined for the vendor or the location affects how the dates are calculated and rounded to working days.</span></span>
<span data-ttu-id="592f2-126">Anger en datumformel för den tid det tar att fylla på artikeln.</span><span class="sxs-lookup"><span data-stu-id="592f2-126">Specifies a date formula for the time that it takes to replenish the item.</span></span> <span data-ttu-id="592f2-127">Den används för att beräkna fältet **Planerat inleveransdatum** om beräkningen är framåt och fältet **Orderdatum** om beräkningen är bakåt.</span><span class="sxs-lookup"><span data-stu-id="592f2-127">It is used to calculate the **Planned Receipt Date** field, if calculating forward, and **Order Date** field, if calculating backwards.</span></span> <span data-ttu-id="592f2-128">Se avsnittet ”Ledtidsberäkning”.</span><span class="sxs-lookup"><span data-stu-id="592f2-128">See the "Lead Time Calculation" section.</span></span>

## <a name="lead-time-calculation"></a><span data-ttu-id="592f2-129">Ledtidsberäkning</span><span class="sxs-lookup"><span data-stu-id="592f2-129">Lead Time Calculation</span></span>
<span data-ttu-id="592f2-130">En baskalender som definierats för leverantörer eller lagerställe inverkar på hur datumen beräknas och avrundas till arbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="592f2-130">Any base calendar defined for the vendor or the location affects how the dates are calculated and rounded to working days.</span></span> <span data-ttu-id="592f2-131">De viktigaste två datumfält på inköpsorderrader beräknas därför på följande sätt under olika omständigheter.</span><span class="sxs-lookup"><span data-stu-id="592f2-131">Accordingly, the two date fields on purchase order lines are calculated as follows under different conditions.</span></span>

|<span data-ttu-id="592f2-132">Beräkningsriktning</span><span class="sxs-lookup"><span data-stu-id="592f2-132">Calculation Direction</span></span>|<span data-ttu-id="592f2-133">Leverantörskalender har definierats</span><span class="sxs-lookup"><span data-stu-id="592f2-133">Vendor Calendar Defined</span></span>|<span data-ttu-id="592f2-134">Leverantörskalender har inte definierats</span><span class="sxs-lookup"><span data-stu-id="592f2-134">Vendor Calendar Not Defined</span></span>|
|---------------------|-----------------------|---------------------------|
|<span data-ttu-id="592f2-135">Framåt</span><span class="sxs-lookup"><span data-stu-id="592f2-135">Forward</span></span>|<span data-ttu-id="592f2-136">planerat inleveransdatum = orderdatum + leverantörsledtid (per leverantörskalendern och avrundat till nästa arbetsdag först i leverantörskalendern och sedan i lagerställekalendern)</span><span class="sxs-lookup"><span data-stu-id="592f2-136">planned receipt date = order date + vendor lead time (per the vendor calendar and rounded to the next working day in first the vendor calendar and then the location calendar)</span></span>|<span data-ttu-id="592f2-137">planerat inleveransdatum = orderdatum + ( leverantörsledtid per lagerställekalendern)</span><span class="sxs-lookup"><span data-stu-id="592f2-137">planned receipt date = order date + vendor lead time (per the location calendar)</span></span>|
|<span data-ttu-id="592f2-138">Bakåt</span><span class="sxs-lookup"><span data-stu-id="592f2-138">Backward</span></span>|<span data-ttu-id="592f2-139">orderdatum = + planerat inleveransdatum - leverantörsledtid (per leverantörskalendern och avrundat till föregående arbetsdag först i leverantörskalendern och sedan i lagerställekalendern)</span><span class="sxs-lookup"><span data-stu-id="592f2-139">order date = planned receipt date - vendor lead time (per the vendor calendar and rounded to the previous working day in first the vendor calendar and then the location calendar)</span></span>|<span data-ttu-id="592f2-140">orderdatum = planerat inleveransdatum - leverantörsledtid (per lagerställekalendern)</span><span class="sxs-lookup"><span data-stu-id="592f2-140">order date = planned receipt date - vendor lead time (per the location calendar)</span></span>|

> [!NOTE]
> <span data-ttu-id="592f2-141">Förutom Ledtidsberäkningen som påverkar det planerade inleveransdatumet och Orderdatum, vilket visas i tabellen ovan distributionslagerhanteringstid och säkerhetsledtid läggas till i formlerna till värdet i fältet **förväntat inleveransdatum** följande: planerat inleveransdatum + Säkerhetsledtid + Ankommande lagerhanteringstid = Förväntat inleveransdatum.</span><span class="sxs-lookup"><span data-stu-id="592f2-141">In addition to the lead time calculation that affects the planned receipt date and order date, as shown in the above table, warehouse handling time and safety lead time may be added to the formulas to make up the value in the **Expected Receipt Date** field, as follows: Planned Receipt Date + Safety Lead Time + Inbound Warehouse Handling Time = Expected Receipt Date.</span></span>

> [!Important]
> <span data-ttu-id="592f2-142">Om ditt lagerställe använder en helt annan kalender än den leverantörerna använder är det viktigt att du lägger upp specifika kalendrar för leverantörerna för att beräkna bästa möjliga leverantörsledtider.</span><span class="sxs-lookup"><span data-stu-id="592f2-142">If your location uses a significantly different calendar than your vendors do, then it is important that you set up specific calendars for those vendors, to calculate optimal vendor lead times.</span></span> <span data-ttu-id="592f2-143">Om du vill veta hur du ställer in leverantörskalendrar, se avsnittet ”Så här tilldelar du en baskalender”.</span><span class="sxs-lookup"><span data-stu-id="592f2-143">For information about how to set up vendor calendars, see the "To assign a base calendar" section.</span></span>

<span data-ttu-id="592f2-144">Innehållet i fältet **Ledtidsberäkning** kopieras från antingen artikelkortet eller lagerställeenhetskortet om ledtiden har angetts för artikeln, eller **Artikelns leverantörskatalog** om ledtiden definieras för leverantören.</span><span class="sxs-lookup"><span data-stu-id="592f2-144">The contents of the **Lead Time Calculation** field is copied from either the item card or the SKU card, if the lead time is defined for the item, or in the **Item Vendor Catalog** window, if the lead time is defined for the vendor.</span></span>

## <a name="to-customize-a-calendar"></a><span data-ttu-id="592f2-145">Så här anpassar du en kalender</span><span class="sxs-lookup"><span data-stu-id="592f2-145">To customize a calendar</span></span>
<span data-ttu-id="592f2-146">Huvuduppgiften när du anpassar en baskalender för företaget, eller någon av dess affärspartner, är att ange eventuella ändringar av status som arbetsdag eller ledig dag.</span><span class="sxs-lookup"><span data-stu-id="592f2-146">The main task in customizing a base calendar for your company, or one of its business partners, is to enter any changes to working and nonworking day status.</span></span>

<span data-ttu-id="592f2-147">I en baskalender visas exempelvis alla lördagar normalt som lediga dagar, medan i en anpassad kalender för ett visst lagerställe kan alla lördagar i november och december fram till julhelgen visas som arbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="592f2-147">For example, while a base calendar would typically list all Saturdays as non-working days, the customized calendar for a particular location may list all Saturdays during the months of November and December, and leading up to the holiday season, as working days.</span></span>

<span data-ttu-id="592f2-148">I proceduren nedan används fallet med lagerstället som exempel:</span><span class="sxs-lookup"><span data-stu-id="592f2-148">The following procedure uses the case of the location as an example.</span></span> <span data-ttu-id="592f2-149">Lägg märke till att du i det här skedet redan har fördelat en baskalender till lagerstället.</span><span class="sxs-lookup"><span data-stu-id="592f2-149">Note that at this point, you have already assigned a base calendar to the location.</span></span>

1. <span data-ttu-id="592f2-150">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="592f2-150">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="592f2-151">Öppna den plats som du vill uppdatera och välj sedan fältet **anpassad kalender**.</span><span class="sxs-lookup"><span data-stu-id="592f2-151">Open the location that you want to update, and then select the **Customized Calendar** field.</span></span> <span data-ttu-id="592f2-152">Observera att en kalender måste markeras i fältet **Baskalenderkod**.</span><span class="sxs-lookup"><span data-stu-id="592f2-152">Note that a calendar must be selected in the **Base Calendar Code** field.</span></span>
3. <span data-ttu-id="592f2-153">I fönstret **Anpassade kalendertransaktioner** väljer du åtgärden **Underhåll ändringar i kalender**.</span><span class="sxs-lookup"><span data-stu-id="592f2-153">In the **Customized Calendar Entries** window opens, choose the **Maintain Customized Calendar Changes** action.</span></span>
4. <span data-ttu-id="592f2-154">I **Anpassade kalenderändringar** lägg till rader för anpassade kalendertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="592f2-154">In the **Customized Calendar Changes**, add lines for customized calendar entries.</span></span>

    <span data-ttu-id="592f2-155">När du registrerar en rad, är kryssrutan **Ej arbetsdag** markerat.</span><span class="sxs-lookup"><span data-stu-id="592f2-155">When you enter a line, the **Nonworking** check box is selected.</span></span> <span data-ttu-id="592f2-156">Du kan ta bort markeringen om du vill ändra status till en arbetsdag.</span><span class="sxs-lookup"><span data-stu-id="592f2-156">You can clear the check box if you want to change the status to a working day.</span></span>

    <span data-ttu-id="592f2-157">Du kan använda fältet **Återkommande system** för att ange ett visst datum eller en viss dag som återkommande ledig dag.</span><span class="sxs-lookup"><span data-stu-id="592f2-157">You can use the **Recurring System** field to set a particular date or day as a recurring nonworking day.</span></span> <span data-ttu-id="592f2-158">Du kan välja mellan alternativen **Årligen återkommande** eller **Veckovis återkommande**.</span><span class="sxs-lookup"><span data-stu-id="592f2-158">You can select either the **Annual Recurring** or **Weekly Recurring** option.</span></span>

    <span data-ttu-id="592f2-159">Om du väljer **Årligen återkommande** måste du även ange vilket datum som avses i fältet **Datum**.</span><span class="sxs-lookup"><span data-stu-id="592f2-159">If you select **Annual Recurring**, you must also enter the relevant date in the **Date** field.</span></span> <span data-ttu-id="592f2-160">Om du väljer **Veckovis återkommande** måste du även ange vilken veckodag som avses i fältet **Dag**.</span><span class="sxs-lookup"><span data-stu-id="592f2-160">If you select **Weekly Recurring**, you must also select the relevant day of the week in the **Day** field.</span></span> <span data-ttu-id="592f2-161">Om du lämnar fältet tomt, måste du fylla i fältet **Datum**.</span><span class="sxs-lookup"><span data-stu-id="592f2-161">If you leave the field empty, you must fill in the **Date** field.</span></span> <span data-ttu-id="592f2-162">Fältet **Dag** fylls i automatiskt.</span><span class="sxs-lookup"><span data-stu-id="592f2-162">The **Day** field is then filled in automatically.</span></span> <span data-ttu-id="592f2-163">Det kan vara praktiskt om du vill markera ett enstaka datum som arbetsdag eller ledig dag.</span><span class="sxs-lookup"><span data-stu-id="592f2-163">This could be useful if you want to mark an individual date as a nonworking or working day.</span></span>

5. <span data-ttu-id="592f2-164">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="592f2-164">Choose the **OK** button.</span></span>

<span data-ttu-id="592f2-165">I fönstret **Anpassade kalendertrans.** kan du lägga märke till att de ändringar som du har gjort har uppdaterats dynamiskt.</span><span class="sxs-lookup"><span data-stu-id="592f2-165">In the **Customized Calendar Entries** window, you will observe that the date entries are updated with the changes that you made.</span></span>

<span data-ttu-id="592f2-166">Observera också, när du öppnar lagerställekortet, att fältet **Anpassad kalender** har värdet **Ja**, vilket indikerar att en anpassad kalender har definierats.</span><span class="sxs-lookup"><span data-stu-id="592f2-166">On the Location card, you will observe that the **Customized Calendar** field contains **Yes**, indicating that a customized calendar has been set up.</span></span>

> [!Important]
> <span data-ttu-id="592f2-167">Om du inte fyller i fältet **Lagerställekod** på en orderrad används företagets kalender.</span><span class="sxs-lookup"><span data-stu-id="592f2-167">If you do not fill in the **Location Code** field on an order line, your company’s calendar is used.</span></span>


<span data-ttu-id="592f2-168">Om du inte fyller i fältet **Speditörkod** på en orderrad används företagets kalender.</span><span class="sxs-lookup"><span data-stu-id="592f2-168">If you do not fill in the **Shipping Agent Code** field on the order line, your company’s calendar is used.</span></span>

> [!NOTE]  
> <span data-ttu-id="592f2-169">Om du ändrar en baskalender som det finns anpassningsändringar av, uppdateras även alla befintliga, anpassade kalendrar automatiskt.</span><span class="sxs-lookup"><span data-stu-id="592f2-169">If you make changes to a base calendar for which customized calendar changes exist, all existing customized calendars are updated automatically.</span></span>

## <a name="to-assign-a-base-calendar"></a><span data-ttu-id="592f2-170">Så här tilldelar du en baskalender</span><span class="sxs-lookup"><span data-stu-id="592f2-170">To assign a base calendar</span></span>  
<span data-ttu-id="592f2-171">Följande procedur schemalägger exempelvis leveransdatum på försäljningsorderrader för en kund.</span><span class="sxs-lookup"><span data-stu-id="592f2-171">The following procedure schedules delivery dates on sales order lines for a customer as an example.</span></span>

<span data-ttu-id="592f2-172">Baskalendrar tilldelas till ditt eget företag, kunder, leverantörer, lagerställen och speditörer på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="592f2-172">Base calendars are assigned to your own company, customers, vendors, locations, and shipping agents as follows:</span></span>  

-   <span data-ttu-id="592f2-173">På korten **Företagsinformation** och **Kund** tilldelas baskalendern på snabbfliken **Leverans**.</span><span class="sxs-lookup"><span data-stu-id="592f2-173">On the **Company Information** and **Customer** cards, the base calendar is assigned on the **Shipping** FastTab.</span></span>  
-   <span data-ttu-id="592f2-174">På kortet **Leverantör**  tilldelas baskalendern på snabbfliken **Inleverans**.</span><span class="sxs-lookup"><span data-stu-id="592f2-174">On the **Vendor** card, the base calendar is assigned on the **Receiving** FastTab.</span></span>  
-   <span data-ttu-id="592f2-175">På kortet **Lagerställe** tilldelas baskalendern på snabbfliken **Lager**.</span><span class="sxs-lookup"><span data-stu-id="592f2-175">On the **Location** card, the base calendar is assigned on the **Warehouse** FastTab.</span></span>  
-   <span data-ttu-id="592f2-176">I fönstret **Speditörer** fördelats baskalendern i fönstret **Speditörsservice**.</span><span class="sxs-lookup"><span data-stu-id="592f2-176">In the **Shipping Agents** window, the base calendar is assigned in the **Shipping Agent Services** window.</span></span>  

1.  <span data-ttu-id="592f2-177">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kunder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="592f2-177">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="592f2-178">Öppna det **Kundkort** som du vill tilldela en anpassad kalender för.</span><span class="sxs-lookup"><span data-stu-id="592f2-178">Open the **Customer** card for whom you will assign a base calendar.</span></span>  
3.  <span data-ttu-id="592f2-179">På Snabbfliken **Leverans**, i fältet **Baskalenderkod**, markera den baskalender som du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="592f2-179">On the **Shipping** FastTab, in the **Base Calendar Code** field, select the base calendar that you want to assign.</span></span>  

> [!IMPORTANT]  
>  -   <span data-ttu-id="592f2-180">Om du inte tilldelar ett företag en baskalender betraktas alla datum som arbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="592f2-180">If you do not assign a base calendar to a company, all dates are calculated as working days.</span></span>  
> -   <span data-ttu-id="592f2-181">Om du anger ett tomt lagerställe på en orderrad betraktas alla datum som arbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="592f2-181">If you enter a blank location on an order line, all dates are calculated as working days.</span></span>  
> -   <span data-ttu-id="592f2-182">En baskalender som definierats för leverantörer eller lagerställe inverkar på hur datumen beräknas och avrundas till arbetsdagar.</span><span class="sxs-lookup"><span data-stu-id="592f2-182">Any base calendar defined for the vendor or the location affects how the dates are calculated and rounded to working days.</span></span>

> [!NOTE]  
>  <span data-ttu-id="592f2-183">Innan du kan skapa några anpassade kalendertransaktioner måste du först tilldela företaget en baskalender.</span><span class="sxs-lookup"><span data-stu-id="592f2-183">Before you can make customized calendar entries, you must first assign a base calendar to the company.</span></span>  

## <a name="see-also"></a><span data-ttu-id="592f2-184">Se även</span><span class="sxs-lookup"><span data-stu-id="592f2-184">See Also</span></span>
[<span data-ttu-id="592f2-185">Inköp</span><span class="sxs-lookup"><span data-stu-id="592f2-185">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="592f2-186">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="592f2-186">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="592f2-187">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="592f2-187">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="592f2-188">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="592f2-188">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
