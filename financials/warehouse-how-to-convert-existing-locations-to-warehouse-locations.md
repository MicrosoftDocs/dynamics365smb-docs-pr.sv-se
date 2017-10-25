---
title: "Så här: Konvertera befintliga lagerställen till distributionslagerplatser | Microsoft Docs"
description: "Du kan definiera att ett befintligt lagerställe ska använda zoner och lagerplatser och fungera som ett distributionslager."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 01081b166df81a76bba984bcb679069e59c660c9
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-convert-existing-locations-to-warehouse-locations"></a><span data-ttu-id="a637f-103">Så här: Konvertera befintliga lagerställen till distributionslagerplatser</span><span class="sxs-lookup"><span data-stu-id="a637f-103">How to: Convert Existing Locations to Warehouse Locations</span></span>
<span data-ttu-id="a637f-104">Du kan definiera att ett befintligt lagerställe ska använda zoner och lagerplatser och fungera som ett distributionslager.</span><span class="sxs-lookup"><span data-stu-id="a637f-104">You can enable an existing inventory location to use zones and bins and to operate as a warehouse location.</span></span>  

<span data-ttu-id="a637f-105">Batch-jobbet där ett lagerställe definieras som ett distributionslager skapar ursprungliga distributionslagertransaktioner för dist.lager justeringslagerplatsen för alla artiklar som finns på lagerstället.</span><span class="sxs-lookup"><span data-stu-id="a637f-105">The batch job to enable a location for warehouse operation creates initial warehouse entries for the warehouse adjustment bin for all items that have inventory in the location.</span></span> <span data-ttu-id="a637f-106">Dessa ursprungliga transaktioner balanseras när transaktioner för fysiskt lager registreras när batch-jobbet är färdigt.</span><span class="sxs-lookup"><span data-stu-id="a637f-106">These initial entries will be balanced when warehouse physical inventory entries are entered after the batch job is run.</span></span>  

<span data-ttu-id="a637f-107">Du kan skapa zoner och lagerplatser före eller efter konverteringen.</span><span class="sxs-lookup"><span data-stu-id="a637f-107">You can create zones and bins either before or after the conversion.</span></span> <span data-ttu-id="a637f-108">Den enda lagerplatsen som du måste skapa före konverteringen är den som ska användas som en framtida justeringslagerplats.</span><span class="sxs-lookup"><span data-stu-id="a637f-108">The only bin that you must create before the conversion is the one that is to be used as the future adjustment bin.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="a637f-109">Du rensar alla negativa lagersaldon och eventuella öppna distributionslagerdokument innan du konverterar platsen för dist.lagerhantering, genom att köra en rapport för att hitta artiklar med negativt lagersaldo och öppna distributionslagerdokument för lagerstället.</span><span class="sxs-lookup"><span data-stu-id="a637f-109">To clear all negative inventory and any open warehouse documents before you convert the location for warehouse handling, run a report to identify the items with negative inventory and open warehouse documents for the location.</span></span> <span data-ttu-id="a637f-110">Mer information finns i Kontrollera negativt lagersaldo
.</span><span class="sxs-lookup"><span data-stu-id="a637f-110">For more information, see Check on Negative Inventory.</span></span>  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a><span data-ttu-id="a637f-111">Så här aktiverar du ett befintligt lagerställe att fungera som ett distributionslager</span><span class="sxs-lookup"><span data-stu-id="a637f-111">To enable an existing location to operate as a warehouse location</span></span>  
1.  <span data-ttu-id="a637f-112">Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Skapa dist.lagerplats** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a637f-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Warehouse Location**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a637f-113">I **Lagerställekod** fältet, ange det lagerställe som du vill aktivera för distributionslagerbearbetning.</span><span class="sxs-lookup"><span data-stu-id="a637f-113">In the **Location Code** field, specify the location that you want to enable for warehouse processing.</span></span>  
3.  <span data-ttu-id="a637f-114">I **Justering lagerplatskod** fältet, ange lagerplatsen på platsen dit ej synkroniserade dist.lager transaktioner lagras.</span><span class="sxs-lookup"><span data-stu-id="a637f-114">In the **Adjustment Bin Code** field, specify the bin at the location where unsynchronized warehouse entries are stored.</span></span> <span data-ttu-id="a637f-115">Mer information finns i avsnittet ”Att synkronisera de justerade lagertransaktionerna med tillhörande artikeltransaktioner” i [Så här: Inventera, justera och gruppera lager](inventory-how-count-adjust-reclassify.md).</span><span class="sxs-lookup"><span data-stu-id="a637f-115">For more information, see the "To synchronize the adjusted warehouse entries with the related item ledger entries" section in [How to: Count, Adjust, and Reclassify Inventory](inventory-how-count-adjust-reclassify.md).</span></span>  

    <span data-ttu-id="a637f-116">Med hjälp av öppna artikeltransaktioner för angivet lagerställe skapas dist.lager journalrader som summerar alla kombinationer av artikelnummer, variantkod, enhetskod och, vid behov, partinr och serienummer kombineras i artikeltransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="a637f-116">Using the open item ledger entries for the specified location, warehouse journal lines are created that sum up every combination of Item No., Variant Code, Unit of Measure Code, and, if necessary, Lot No. and Serial No. in the item ledger entries.</span></span> <span data-ttu-id="a637f-117">Distributionslagerjorunalraderna bokförs sedan.</span><span class="sxs-lookup"><span data-stu-id="a637f-117">The warehouse journal lines are then posted.</span></span> <span data-ttu-id="a637f-118">Vid bokföringen skapas distributionslagertransaktioner som placerar lagret i distributionslagrets justeringslagerplats.</span><span class="sxs-lookup"><span data-stu-id="a637f-118">This posting creates warehouse entries that place the inventory in the warehouse adjustment bin.</span></span> <span data-ttu-id="a637f-119">**Justering lagerplatskod** anges också på lagerställekortet.</span><span class="sxs-lookup"><span data-stu-id="a637f-119">The **Adjustment Bin Code** on the location card is also set.</span></span>  

4.  <span data-ttu-id="a637f-120">Om du vill se vilka artiklar som lagts till i justeringslagerplatsen under batch-jobbet kan du köra rapporten **Dist.lager just.lagerplats**.</span><span class="sxs-lookup"><span data-stu-id="a637f-120">To see which items were added to the adjustment bin during the batch job, run the **Warehouse Adjustment Bin** report.</span></span>  
5.  <span data-ttu-id="a637f-121">När batch-jobbet **Skapa dist.lagerplats** är färdigt utför du och bokför en inventering av lagret.</span><span class="sxs-lookup"><span data-stu-id="a637f-121">When the **Create Warehouse Location** batch job has completed, perform and post a warehouse physical inventory.</span></span> <span data-ttu-id="a637f-122">Mer information finns i [så här: Inventera, justera och gruppera lager](inventory-how-count-adjust-reclassify.md).</span><span class="sxs-lookup"><span data-stu-id="a637f-122">For more information, see [How to: Count, Adjust, and Reclassify Inventory](inventory-how-count-adjust-reclassify.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a637f-123">Du bör köra det här batch-jobbet **Skapa dist.lagerplats** vid ett tillfälle då det inte påverkar det dagliga arbetet i systemet.</span><span class="sxs-lookup"><span data-stu-id="a637f-123">It is recommended that you run the **Create Warehouse Location** batch job at a time when it will not impact the daily work in the system.</span></span> <span data-ttu-id="a637f-124">I det här jobbet bearbetas alla transaktioner i tabellen **Artikeltransaktion** och om det finns många artikeltransaktioner kan jobbet ta flera timmar.</span><span class="sxs-lookup"><span data-stu-id="a637f-124">This job processes each entry in the **Item Ledger Entry** table, and if there are a large number of item ledger entries, the job can last several hours.</span></span>  

 <span data-ttu-id="a637f-125">För lagerställen där lagerstyrningsdokument inte användes före konverteringen måste du på nytt öppna och släppa källdokument som var delvis inlevererade eller delvis utlevererade före konverteringen.</span><span class="sxs-lookup"><span data-stu-id="a637f-125">For those locations that did not use warehouse management documents before the conversion, you must re-open and release any source documents that were partially received or partially shipped before the conversion.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a637f-126">Se även</span><span class="sxs-lookup"><span data-stu-id="a637f-126">See Also</span></span>  
[<span data-ttu-id="a637f-127">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="a637f-127">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="a637f-128">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="a637f-128">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="a637f-129">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="a637f-129">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="a637f-130">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="a637f-130">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="a637f-131">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="a637f-131">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="a637f-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a637f-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
