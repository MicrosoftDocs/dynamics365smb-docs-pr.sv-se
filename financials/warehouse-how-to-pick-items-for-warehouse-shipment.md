---
title: "Så här: plocka artiklar för Dist.lager utleverans | Microsoft Docs"
description: "När Lagerställe är inställt på att begära plockningsbearbetning så väl som utleveransbearbetning använder du plockningsdokumenten för att skapa och bearbeta plockningsinformationen innan du bokför Lagerutleveransen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e4568214469e80dce7ea91ff7574d1be8ca9ac7a
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-pick-items-for-warehouse-shipment"></a><span data-ttu-id="97620-103">Så här: plocka artiklar för Dist.lager utleverans</span><span class="sxs-lookup"><span data-stu-id="97620-103">How to: Pick Items for Warehouse Shipment</span></span>
<span data-ttu-id="97620-104">När Lagerställe är inställt på att begära plockningsbearbetning så väl som utleveransbearbetning använder du plockningsdokumenten för att skapa och bearbeta plockningsinformationen innan du bokför Lagerutleveransen.</span><span class="sxs-lookup"><span data-stu-id="97620-104">When the location is set up to require warehouse pick processing as well as warehouse shipment processing, you use the warehouse pick documents to create and process pick information prior to posting the warehouse shipment.</span></span>  

<span data-ttu-id="97620-105">Du kan inte skapa ett dokument för dist.lager plockning från grunden, eftersom en plockningsaktivitet alltid ingår i ett arbetsflöde, i ett pull-/pushscenario.</span><span class="sxs-lookup"><span data-stu-id="97620-105">You cannot create a warehouse pick document from scratch because a pick activity is always part of a workflow, either in a pull or a push scenario.</span></span>  

<span data-ttu-id="97620-106">Du kan skapa dokumentet för dist.lager plockning med ett pullmetod genom att öppna ett tomt distributionslagerdokumentet, hitta källdokument som släpps till leveransen, och sedan skapa plockningsraderna för de utleveranser.</span><span class="sxs-lookup"><span data-stu-id="97620-106">You can create warehouse pick documents in a pull fashion by opening an empty warehouse shipment document, detect source documents that are released to shipment, and then create warehouse pick lines for those shipments.</span></span> <span data-ttu-id="97620-107">Du kan använda **Hämta källdokument** , eller **Filter för att hämta urspr.dok.** funktioner för att undersöka källdokument som är klara för utleverans.</span><span class="sxs-lookup"><span data-stu-id="97620-107">You can use the **Get Source Documents** or **Use Filter to Get Source Documents** functions to detect source documents that are ready for shipment.</span></span>

<span data-ttu-id="97620-108">Du kan också använda **Plockningsförslag** fönstret för att flytta plockningsrader i batchläge.</span><span class="sxs-lookup"><span data-stu-id="97620-108">Alternatively, you can use the **Pick Worksheet** window to pull and create pick lines in batch mode.</span></span> <span data-ttu-id="97620-109">Mer information finns i [Så här planerar du plockningar i förslaget](warehouse-how-to-plan-picks-in-worksheets.md).</span><span class="sxs-lookup"><span data-stu-id="97620-109">For more information, see [How to: Plan Picks in Worksheets](warehouse-how-to-plan-picks-in-worksheets.md).</span></span>  

<span data-ttu-id="97620-110">Du kan också skapa dokument för dist.lager plockning med pushmetod från **Dist.lager utleverans** fönstret, genom att välja **Skapa plockning**.</span><span class="sxs-lookup"><span data-stu-id="97620-110">You can also create warehouse pick documents in a push fashion from the **Warehouse Shipment** window by selecting **Create Pick**.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="97620-111">Plockning för distributionslagerutleverans av artiklar som är monterade till försäljningsorder som har levererats, följer samma steg för distributionslager som vanliga plockning för utleverans, enligt beskrivningen i det här avsnittet.</span><span class="sxs-lookup"><span data-stu-id="97620-111">Picking for warehouse shipment of items that are assembled to the sales order being shipped follows the same steps as for regular warehouse picks for shipment, as described in this topic.</span></span> <span data-ttu-id="97620-112">Numret på plockningsrader per antal som ska levereras kan vara många-till-en, eftersom plockning för distributionslager är för monteringskomponenter och inte för monteringsartikeln.</span><span class="sxs-lookup"><span data-stu-id="97620-112">However, the number of pick lines per quantity to ship may be many to one because you pick the components, not the assembly item.</span></span>  
>   
>  <span data-ttu-id="97620-113">Distributionslagerplockningsrader skapas för värdet i fältet **Återstående antal** på raderna i monteringsorder som är kopplad till försäljningsorderraden som levereras.</span><span class="sxs-lookup"><span data-stu-id="97620-113">The warehouse pick lines are created for the value in the **Remaining Quantity** field on the lines of the assembly order that is linked to the sales order line that is being shipped.</span></span> <span data-ttu-id="97620-114">Det gör att alla komponenter kan plockas i en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="97620-114">This ensures that all components are picked in one action.</span></span>  
>   
>  <span data-ttu-id="97620-115">Mer information finns i avsnittet ”Hantera artiklar för montering mot kundorder i distributionslagerutleveranser”.</span><span class="sxs-lookup"><span data-stu-id="97620-115">For more information, see the “Handling Assemble-to-Order Items in Warehouse Shipments” section.</span></span>  
>   
>  <span data-ttu-id="97620-116">Information om hur du plockar komponenter för monteringsorder, inklusive lagerställen, där monteringsartikeln inte ska betalas på en utleverans, se [så här: Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="97620-116">For information about picking components for assembly orders generally, including situations where the assembly item is not due on a sales shipment, see [How to: Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  

## <a name="to-pick-items-for-warehouse-shipment"></a><span data-ttu-id="97620-117">Så här plocka artiklar för utleverans</span><span class="sxs-lookup"><span data-stu-id="97620-117">To pick items for warehouse shipment</span></span>  
1.  <span data-ttu-id="97620-118">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Plockningar**, och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="97620-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Picks**, and then choose the related link.</span></span>  

    <span data-ttu-id="97620-119">Om du vill arbeta med en viss plockning väljer du plockningen från listan eller filtrerar listan för att söka efter de plockningar som specifikt har tilldelats dig.</span><span class="sxs-lookup"><span data-stu-id="97620-119">If you need to work on a particular pick, select the pick from the list or filter the list to find the picks that have been assigned to you specifically.</span></span> <span data-ttu-id="97620-120">Öppna plockningskortet.</span><span class="sxs-lookup"><span data-stu-id="97620-120">Open the pick card.</span></span>  
2.  <span data-ttu-id="97620-121">Om **Tilldelat användar-ID** är tomt, anger du ID för att identifiera själv om det behövs.</span><span class="sxs-lookup"><span data-stu-id="97620-121">If the **Assigned User ID** field is empty, enter your ID to identify yourself if necessary.</span></span>  
3.  <span data-ttu-id="97620-122">Utför den faktiska plockning av artiklar.</span><span class="sxs-lookup"><span data-stu-id="97620-122">Perform the actual picking of items.</span></span>  

    <span data-ttu-id="97620-123">Om distributionslagret har konfigurerats att använda lagerplatser, då artikelns standardlagerplatser används för att föreslå var du vill hämta artiklar från.</span><span class="sxs-lookup"><span data-stu-id="97620-123">If the warehouse is set up to use bins, then the items’ default bins are used to suggest where to take the items from.</span></span> <span data-ttu-id="97620-124">instruktionerna visas som två separata rader, minst en för varje åtgärdstyp, en för ta och en för placera.</span><span class="sxs-lookup"><span data-stu-id="97620-124">The instructions appear as two separate lines, at least one for each action type, Take and Place.</span></span>  

    <span data-ttu-id="97620-125">Om distributionslagret är inställt på dirigerad artikelinförsel och plockning, lagerplatsordningen används för att beräkna de bästa lagerplatserna som ska plockas från, och de lagerplatser föreslås på plockningsraderna.</span><span class="sxs-lookup"><span data-stu-id="97620-125">If the warehouse is set up to use directed put-away and pick, then the bin ranking is used to calculate the best bins to pick from, and those bins are then suggested on the pick lines.</span></span> <span data-ttu-id="97620-126">instruktionerna visas som två separata rader, minst en för varje åtgärdstyp, en för ta och en för placera.</span><span class="sxs-lookup"><span data-stu-id="97620-126">The instructions appear as two separate lines, at least one for each action type, Take and Place.</span></span>  

4.  <span data-ttu-id="97620-127">När du har utfört plockningen och placerat artiklarna i utleveransområdet eller på lagerplatsen för utleveranser väljer du åtgärden **Registrera plockning**.</span><span class="sxs-lookup"><span data-stu-id="97620-127">When you have performed the pick and placed the items in the shipping area or shipping bin, choose the **Register Pick** action.</span></span>  

<span data-ttu-id="97620-128">Den person som ansvarar för utleverans kan nu få artiklarna till ett leveransdockan och bokföra leveransen, inklusive relaterade källdokumentet, i fönstret **Dist.lager utleverans**.</span><span class="sxs-lookup"><span data-stu-id="97620-128">The person responsible for shipment can now bring the items to the shipment dock and post the shipment, including the related source document, in the **Warehouse Shipment** window.</span></span> <span data-ttu-id="97620-129">För mer information finns i [Så här levererar du artiklar](warehouse-how-ship-items.md).</span><span class="sxs-lookup"><span data-stu-id="97620-129">For more information, see [How to: Ship Items](warehouse-how-ship-items.md).</span></span>   

<span data-ttu-id="97620-130">Förutom plockning för källdokument, som beskrivs i det här avsnittet, kan du ta och placera artiklar mellan lagerplatser, utan att referera till källdokument.</span><span class="sxs-lookup"><span data-stu-id="97620-130">In addition to picking for source documents, as described in this topic, you can take and place items between bins without referring to source documents.</span></span> <span data-ttu-id="97620-131">Mer information finns i [så här: Plocka och föra in utan ett källdokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md).</span><span class="sxs-lookup"><span data-stu-id="97620-131">For more information, see [How to: Pick and Put Away Without a Source Document](warehouse-how-to-create-put-aways-from-internal-put-aways.md).</span></span>  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a><span data-ttu-id="97620-132">Hantera artiklar för montering mot kundorder i distributionslagerutleveranser</span><span class="sxs-lookup"><span data-stu-id="97620-132">Handling Assemble-to-Order Items in Warehouse Shipments</span></span>
<span data-ttu-id="97620-133">I montering mot kundorder-scenarier är fältet **Ant. att utleverera** på distributionslagerutleveransrader använt för att notera hur många enheter som monteras.</span><span class="sxs-lookup"><span data-stu-id="97620-133">In assemble-to-order scenarios, the **Qty. to Ship** field on warehouse shipment lines is used to record how many units are assembled.</span></span> <span data-ttu-id="97620-134">Det angivna antalet bokförs sedan som monteringsutflöde när distributionslagerutleveransen bokförs.</span><span class="sxs-lookup"><span data-stu-id="97620-134">The specified quantity is then posted as assembly output when the warehouse shipment is posted.</span></span>

<span data-ttu-id="97620-135">För andra distributionslagerutleveransrader är värdet i **Ant. att utleverera** noll från början.</span><span class="sxs-lookup"><span data-stu-id="97620-135">For other warehouse shipment lines, the value in the **Qty. to Ship** field is zero from the start.</span></span>

<span data-ttu-id="97620-136">När arbetare ansvariga för slutfört monterande av komponenter för montering eller hela antalet för montering mot kundorder, registrerar de i fältet **Ant. att utleverera** på distributionslagerutleveransraden i avancerade konfigurationer och väljer åtgärden **Bokför utleverans**.</span><span class="sxs-lookup"><span data-stu-id="97620-136">When workers in charge of assembly finish assembling parts or all of the assemble-to-order quantity, they record it in the **Qty. to Ship** field on the warehouse shipment line and then choose the **Post Shipment** action.</span></span> <span data-ttu-id="97620-137">Resultatet blir att det motsvarande monteringsutflödet bokförs, inklusive komponentförbrukningen.</span><span class="sxs-lookup"><span data-stu-id="97620-137">The result is that the corresponding assembly output is posted, including the component consumption.</span></span> <span data-ttu-id="97620-138">En utleverans för kvantiteterna bokförs för försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="97620-138">A sales shipment for the quantity is posted for the sales order.</span></span>

<span data-ttu-id="97620-139">Från monteringsordern kan du välja **Montering mot kundorder, dist.lager utleveransrad** för att komma åt distributionslagerutleveransraden.</span><span class="sxs-lookup"><span data-stu-id="97620-139">From the assembly order, you can choose **Asm.-to-Order Whse. Shpt. Line** to access the warehouse shipment line.</span></span> <span data-ttu-id="97620-140">Det är praktiskt exempelvis för arbetare som inte använder vanligtvis **Dist.lager utleverans**-fönstret.</span><span class="sxs-lookup"><span data-stu-id="97620-140">This is convenient for workers who do not typically use the **Warehouse Shipment** window.</span></span>

<span data-ttu-id="97620-141">När distributionslagerutleveransen har bokförts uppdateras olika fält på försäljningsorderraden för att visa förloppet i distributionslagret.</span><span class="sxs-lookup"><span data-stu-id="97620-141">After the warehouse shipment is posted, various fields on the sales order line are updated to show progress in the warehouse.</span></span> <span data-ttu-id="97620-142">Följande fält uppdateras också för att visa hur många antal för montering mot kundorder som återstår att monteras och levereras:</span><span class="sxs-lookup"><span data-stu-id="97620-142">The following fields are also updated to show how many assemble-to-order quantities remain to be assembled and shipped:</span></span>

- <span data-ttu-id="97620-143">**ATO Restnot. antal i lager**</span><span class="sxs-lookup"><span data-stu-id="97620-143">**ATO Whse. Outstanding Qty.**</span></span>
- <span data-ttu-id="97620-144">**ATO Restnot. antal i lager (bas)**</span><span class="sxs-lookup"><span data-stu-id="97620-144">**ATO Whse. Outstd. Qty. (Base)**</span></span>

> [!NOTE]
> <span data-ttu-id="97620-145">I alla scenarier där en del av antalet måste först vara monterat och ett annat ska levereras från lagret, skapas ett minimum på två distributionslagerutleveransrader.</span><span class="sxs-lookup"><span data-stu-id="97620-145">In combination scenarios, in which a part of the quantity must first be assembled and another must be shipped from inventory, two warehouse shipment lines are created.</span></span> <span data-ttu-id="97620-146">En är för antal för montering mot kundorder, och en är lagerantalet.</span><span class="sxs-lookup"><span data-stu-id="97620-146">One is for the assemble-to-order quantity, and one is for the inventory quantity.</span></span>

> <span data-ttu-id="97620-147">I så fall hanteras antal för montering mot kundorder som beskrivs i det här avsnittet, och lagerantalet behandlas som andra distributionslagerutleveransrader.</span><span class="sxs-lookup"><span data-stu-id="97620-147">In that case, the assemble-to-order quantity is handled as described in this topic, and the inventory quantity is handled as any other regular warehouse shipment line.</span></span> <span data-ttu-id="97620-148">Mer information om alla kombinationsscenarier finns i [Förstå montering mot kundorder och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md.</span><span class="sxs-lookup"><span data-stu-id="97620-148">For more information about combination scenarios, see [Understanding Assemble to Order and Assemble to Stock](assembly-assemble-to-order-or-assemble-to-stock.md.</span></span>

## <a name="see-also"></a><span data-ttu-id="97620-149">Se även</span><span class="sxs-lookup"><span data-stu-id="97620-149">See Also</span></span>  
[<span data-ttu-id="97620-150">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="97620-150">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="97620-151">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="97620-151">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="97620-152">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="97620-152">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="97620-153">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="97620-153">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="97620-154">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="97620-154">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="97620-155">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="97620-155">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
