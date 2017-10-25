---
title: "Så här omstrukturerar du distributionslager | Microsoft Docs"
description: kanske vill du omstrukturera distributionslagret med nya lagerplatskoder och nya lagerplatsegenskaper.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: da5928be8280bad2eac379a5f0e5b19ddc2d12bc
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-restructure-warehouses"></a><span data-ttu-id="7256d-103">Så här: Omstrukturera distributionslager</span><span class="sxs-lookup"><span data-stu-id="7256d-103">How to: Restructure Warehouses</span></span>
<span data-ttu-id="7256d-104">Du kanske vill omstrukturera distributionslagret med nya lagerplatskoder och nya lagerplatsegenskaper.</span><span class="sxs-lookup"><span data-stu-id="7256d-104">You may want to restructure your warehouse with new bin codes and new bin characteristics.</span></span> <span data-ttu-id="7256d-105">Den typen av aktivitet utförs inte särskilt ofta, men det kan uppstå situationer när en omgruppering är nödvändig för att åstadkomma en effektivare drift.</span><span class="sxs-lookup"><span data-stu-id="7256d-105">You will not undertake this kind of activity very often, but situations can occur where a reclassification is necessary to achieve or maintain a more efficient operation.</span></span> <span data-ttu-id="7256d-106">Som exempel:</span><span class="sxs-lookup"><span data-stu-id="7256d-106">For example:</span></span>  

- <span data-ttu-id="7256d-107">Du kanske vill växla till lagerplatskoder som stöder automatisk datainsamling, exempelvis med handenheter.</span><span class="sxs-lookup"><span data-stu-id="7256d-107">You might want to switch to bin codes that support the use of automatic data capture, for example, with hand-held devices.</span></span>  
- <span data-ttu-id="7256d-108">Distributionslagret kanske har köpt in nya ställningar som ger andra möjligheter att lagra artiklar.</span><span class="sxs-lookup"><span data-stu-id="7256d-108">The warehouse may have purchased a new rack system that gives new possibilities in item storage.</span></span>  
- <span data-ttu-id="7256d-109">Företaget kanske har ändrat sitt artikelsortiment och flyttat distributionslagret till en ny plats för att kunna hantera förändringen.</span><span class="sxs-lookup"><span data-stu-id="7256d-109">The company may have altered its item assortment and moved the warehouse to a new physical location to accommodate this change.</span></span>  

<span data-ttu-id="7256d-110">Om distributionslagret är inställt på lagerplatser, men inte dirigerad artikelinförsel och plockning, strukturera om distributionslagret genom att skapa nya lagerplatser du vill använda.</span><span class="sxs-lookup"><span data-stu-id="7256d-110">If your warehouse is set up to use bins but not directed put-away and pick, restructure your warehouse by creating the new bins that you want to use in the future.</span></span>  

## <a name="to-restructure-a-basic-warehouse-that-uses-bins-only"></a><span data-ttu-id="7256d-111">Om du vill omstrukturera en vanlig dist.lager som använder lagerplatser bara</span><span class="sxs-lookup"><span data-stu-id="7256d-111">To restructure a basic warehouse that uses bins only</span></span>  
1.  <span data-ttu-id="7256d-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7256d-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7256d-113">På snabbfliken **lager** anger du fältet **Standardlagerplatsval** till **Senaste lagerplats**.</span><span class="sxs-lookup"><span data-stu-id="7256d-113">On the **Warehouse** FastTab, set the **Default Bin Selection** field to **Last-Used Bin**.</span></span>  
3.  <span data-ttu-id="7256d-114">Flytta allt innehåll på de nuvarande lagerplatserna till de nya lagerplatserna som du precis har skapat.</span><span class="sxs-lookup"><span data-stu-id="7256d-114">Move all the contents of your current bins to the new bins that you have just created.</span></span>  

    1.  <span data-ttu-id="7256d-115">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikelgrupperingsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7256d-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclassification Journal**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="7256d-116">Markera en rad och välj sedan åtgärden **Hämta lagerplatsinnehåll**.</span><span class="sxs-lookup"><span data-stu-id="7256d-116">Select a journal line, and then choose the **Get Bin Content** action.</span></span>  
    3.  <span data-ttu-id="7256d-117">På Snabbfliken **Lagerplatsinnehåll** , ställer du in filter i **Lagerställekod**, **Lagerplatskod**, och **Artikelnr** fältet för att ange innehållet som du vill flytta.</span><span class="sxs-lookup"><span data-stu-id="7256d-117">On the **Bin Content** FastTab, set filters in the **Location Code**, **Bin Code**, and **Item No.** fields to specify the content that you want to move.</span></span>  
    4.  <span data-ttu-id="7256d-118">Välj den **OK** på för att fylla i en journalrad.</span><span class="sxs-lookup"><span data-stu-id="7256d-118">Choose the **OK** button to fill a journal line.</span></span>  
    5.  <span data-ttu-id="7256d-119">Markera den lagerplats till vilken artiklarna ska flyttas i fältet **Ny lagerplatskod**.</span><span class="sxs-lookup"><span data-stu-id="7256d-119">In the **New Bin Code** field, select the bin to which the items should be moved.</span></span>  
    6.  <span data-ttu-id="7256d-120">Upprepa steg b till e för allt lagerplatsinnehåll som du vill flytta.</span><span class="sxs-lookup"><span data-stu-id="7256d-120">Repeat steps b through e for all bin content that you want to move.</span></span>  
    7.  <span data-ttu-id="7256d-121">Välj åtgärden **Bokföra**.</span><span class="sxs-lookup"><span data-stu-id="7256d-121">Choose the **Post** action.</span></span>  

<span data-ttu-id="7256d-122">Du har nu tömt lagerplatser där artiklarna användes.</span><span class="sxs-lookup"><span data-stu-id="7256d-122">You have now emptied the bins where the items used to be.</span></span> <span data-ttu-id="7256d-123">Standardlagerplatserna för artiklarna har nu ändrats till de nya lagerplatser.</span><span class="sxs-lookup"><span data-stu-id="7256d-123">The default bins for your items have now been changed to the new bins.</span></span>  

## <a name="to-restructure-an-advanced-warehouse-that-uses-directed-put-away-and-pick"></a><span data-ttu-id="7256d-124">Omstrukturera en avancerad lager som använder dirigerad artikelinförsel och plockning</span><span class="sxs-lookup"><span data-stu-id="7256d-124">To restructure an advanced warehouse that uses directed put-away and pick</span></span>  

1.  <span data-ttu-id="7256d-125">Ska de nya lagerplatserna som du vill använda i framtiden.</span><span class="sxs-lookup"><span data-stu-id="7256d-125">Create the new bins that you want to use in the future.</span></span> <span data-ttu-id="7256d-126">Mer information finns i [Så här: Skapa lagerplatser](warehouse-how-to-create-individual-bins.md).</span><span class="sxs-lookup"><span data-stu-id="7256d-126">For more information, see [How to: Create Bins](warehouse-how-to-create-individual-bins.md).</span></span>  
2.  <span data-ttu-id="7256d-127">Flytta allt innehåll på de nuvarande lagerplatserna till de nya lagerplatserna som du precis har skapat.</span><span class="sxs-lookup"><span data-stu-id="7256d-127">Move all the contents of your current bins to the new bins that you just created.</span></span>  

    1.  <span data-ttu-id="7256d-128">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lageromgrupperingsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7256d-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Reclassification Journal**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="7256d-129">För de lagerplatser där det inte sker någon transport av artiklar skapar du en rad för varje aktuell lagerplats i **Dist.lager omgrupperingsjnl** med den gamla lagerplatskoden, **Från lagerplatskod** och den nya lagerplatskoden, **Till lagerplatskod**.</span><span class="sxs-lookup"><span data-stu-id="7256d-129">For the bins where no real movement of items is involved, create a line for each of your current bins in the **Warehouse Reclassification Journal** with the old bin code, **From Bin Code**, and the new bin code, **To Bin Code**.</span></span>  
    3.  <span data-ttu-id="7256d-130">Om vissa transporter innefattar fysiska transporter som du vill att lagerpersonalen ska utföra använder du **Transportförslag** för att förbereda transportinstruktioner i stället för att använda lagergrupperingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="7256d-130">If some of the movements involve actual physical movements that you want employees to perform, use **Movement Worksheets** to prepare movement instructions instead of using the warehouse reclassification journal.</span></span> <span data-ttu-id="7256d-131">För mer information, se [Så här: Flytta artiklar avancerad distributionslagerkonfiguration](warehouse-how-to-move-items-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="7256d-131">For more information, see [How to: Move Items in Advanced Warehouse Configurations](warehouse-how-to-move-items-in-advanced-warehousing.md).</span></span>  

3.  <span data-ttu-id="7256d-132">När de gamla lagerplatserna är tomma gruppera om dem som **KS** typ av lagerplatsen, för att se till att de inte inkluderas i artikelflöden.</span><span class="sxs-lookup"><span data-stu-id="7256d-132">When the old bins are emptied, reclassify them as **QC** type bins to ensure that they are not included in item flows.</span></span>  

    1.  <span data-ttu-id="7256d-133">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7256d-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="7256d-134">Markera raden med lagerstället, och välj sedan åtgärden **Lagerplatser**.</span><span class="sxs-lookup"><span data-stu-id="7256d-134">Select the line with the location, and then choose the **Bins** action.</span></span>  
    3.  <span data-ttu-id="7256d-135">I **Lagerplatser** fönstret i **Lagerplatstyp kod** fältet, ange **KS** för var och en av de gamla lagerplatserna som du tömde i steg 3 i föregående process.</span><span class="sxs-lookup"><span data-stu-id="7256d-135">In the **Bins** window, in the **Bin Type Code** field, enter **QC** for each of the old bins that you emptied in step 3 in the previous procedure.</span></span>  

<span data-ttu-id="7256d-136">Du har nu tagit bort lagerplatserna från lagerflödet och har omklassificerat dem, som KS-lagerplatser. KS-lagerplatser har inte några av aktivitetsfälten i fältet **Lagerplatstyper** valda och därför inte beaktas av objektflödet.</span><span class="sxs-lookup"><span data-stu-id="7256d-136">You have now removed the bins from the warehouse flow, and reclassified them as QC bins. QC bins have none of the activity fields in the **Bin Types** window selected and are therefore not considered by the item flow.</span></span> <span data-ttu-id="7256d-137">(Mer information finns i [Så här: Skapa Lagerplatstyper](warehouse-how-to-set-up-bin-types.md).)</span><span class="sxs-lookup"><span data-stu-id="7256d-137">For more information, see [How to: Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="to-delete-a-bin"></a><span data-ttu-id="7256d-138">Så här tar du bort en lagerplats</span><span class="sxs-lookup"><span data-stu-id="7256d-138">To delete a bin</span></span>  

1.  <span data-ttu-id="7256d-139">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7256d-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7256d-140">Markera lagerstället där du vill ta bort lagerplatser väljer du åtgärden **Lagerplatser**.</span><span class="sxs-lookup"><span data-stu-id="7256d-140">Select the location where you want to delete bins. Choose the **Bins** action.</span></span>  
3.  <span data-ttu-id="7256d-141">Markera raderna för de lagerplatser som du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="7256d-141">Select the lines for the bins that you want to delete.</span></span>  
4.  <span data-ttu-id="7256d-142">Välj åtgärden **Radera**.</span><span class="sxs-lookup"><span data-stu-id="7256d-142">Choose the **Delete** action.</span></span>  

<span data-ttu-id="7256d-143">Om du klickar på **Ja** tas lagerplatsen bort för framtida användning, men lagerplatskoden finns kvar i alla distributionslagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="7256d-143">If you choose the **Yes** button, the bin is deleted for use in the future, but the bin code in all warehouse entries remains the same.</span></span>  

<span data-ttu-id="7256d-144">Om du vill byta namn på en lagerplats så att alla poster som tillhör lagerplatsen också får det nya namnet kan du göra det i fönstret **Lagerplatser**, inklusive lagerplatsinnehåll, aktivitetsrader för distributionslager, registrerade aktivitetsrader för distributionslager, förslagsrader för distributionslager, inleveransrader för distributionslager, bokförda inleveransrader för distributionslager, utleveransrader för distributionslager, bokförda utleveransrader för distributionslager och distributionslagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="7256d-144">If you want to rename a bin so that all records associated with the bin are also renamed, including bin contents, warehouse activity lines, registered warehouse activity lines, warehouse worksheet lines, warehouse receipt lines, posted warehouse receipt lines, warehouse shipment lines, posted warehouse shipment lines, and warehouse entries, you can do so in the **Bins** window.</span></span>  

## <a name="to-rename-a-bin-and-change-the-bin-code-in-all-records"></a><span data-ttu-id="7256d-145">Så här byter du namn på en lagerplats och ändrar lagerplatskoden i alla poster</span><span class="sxs-lookup"><span data-stu-id="7256d-145">To rename a bin and change the bin code in all records</span></span>  

1.  <span data-ttu-id="7256d-146">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7256d-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7256d-147">Välj lagerstället där du vill byta namn på en lagerplats eller ändra lagerplatskoden och klicka på åtgärden **Lagerplatser**.</span><span class="sxs-lookup"><span data-stu-id="7256d-147">Select the location where you want to rename a bin or change the bin code, and then choose the **Bins** action.</span></span>  
3.  <span data-ttu-id="7256d-148">I **Kod** fältet, ange lagerplatsen du vill ändra och ange en ny lagerplatskod.</span><span class="sxs-lookup"><span data-stu-id="7256d-148">Select the bin that you want to change and enter a new bin code in the **Code** field.</span></span>  
4.  <span data-ttu-id="7256d-149">Välj **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7256d-149">Choose the **Yes** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7256d-150">Om du väljer **ja** , och det finns många transaktioner som rör den här lagerplatsen, till exempel, eftersom du inte har tagit bort de dokument för en tid, kan det ta en stund byta namn på samtliga transaktioner.</span><span class="sxs-lookup"><span data-stu-id="7256d-150">If you choose **Yes** and there are many entries concerning this bin, for example, because you have not deleted warehouse documents for some time, it may take some time to rename all the records.</span></span> <span data-ttu-id="7256d-151">Använd batch-jobbet **Ta bort reg. dist.lagerdok.** innan du startar bytanamnprocessen, om du använder den här metoden.</span><span class="sxs-lookup"><span data-stu-id="7256d-151">Therefore, if you use this method, consider running the batch job **Delete Registered Whse. Documents** before you start the renaming process.</span></span> <span data-ttu-id="7256d-152">Observera också att det enda dokumenten som tas bort i det här batch-jobbet är artikelinförsel, plockning och transport.</span><span class="sxs-lookup"><span data-stu-id="7256d-152">Also note that the only documents that are deleted in this batch job are put-aways, picks, and movements.</span></span>  
>   
>  <span data-ttu-id="7256d-153">Om du byter namn på en inleveranslagerplats eller en leveranslagerplats, alla bokförd inleveranser och utleveranser som gäller för lagerplatsen, byts namn på.</span><span class="sxs-lookup"><span data-stu-id="7256d-153">If you are renaming a receiving bin or a shipping bin, all the posted receipts or shipments that refer to the bin in question are renamed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7256d-154">Se även</span><span class="sxs-lookup"><span data-stu-id="7256d-154">See Also</span></span>  
[<span data-ttu-id="7256d-155">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="7256d-155">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="7256d-156">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="7256d-156">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="7256d-157">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="7256d-157">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="7256d-158">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="7256d-158">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="7256d-159">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="7256d-159">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="7256d-160">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7256d-160">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
