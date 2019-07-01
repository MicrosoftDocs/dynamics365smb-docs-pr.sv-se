---
title: Importerar många artikelbilder från en ZIP-fil | Microsoft Docs
description: Du kan importera flera artikelbilder samtidigt. Bara ge bildfilerna namn som motsvarar dina artikelnummer, komprimera dem till en zip-fil och använd sedan sidan Importera artikelbilder för att hantera vilka artikelbilder som ska importeras.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fa859d3e350cedb845df47521ee58ba8d2e4aade
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243072"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="15940-104">Importera flera artikelbilder</span><span class="sxs-lookup"><span data-stu-id="15940-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="15940-105">Du kan importera flera artikelbilder samtidigt.</span><span class="sxs-lookup"><span data-stu-id="15940-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="15940-106">Bara ge bildfilerna namn som motsvarar dina artikelnummer, komprimera dem till en zip-fil och använd sedan sidan **Importera artikelbilder** för att hantera vilka artikelbilder som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="15940-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="15940-107">Alla vanliga filformat stöds.</span><span class="sxs-lookup"><span data-stu-id="15940-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="15940-108">Namnge bildfiler med artikelnamnen och förbered ZIP-filen</span><span class="sxs-lookup"><span data-stu-id="15940-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="15940-109">På platsen där artikelbilderna sparas ska du namnge varje filnamn i enlighet med numret på den relaterade artikeln.</span><span class="sxs-lookup"><span data-stu-id="15940-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="15940-110">Som exempel:</span><span class="sxs-lookup"><span data-stu-id="15940-110">For example:</span></span>

    |<span data-ttu-id="15940-111">Artikelnr</span><span class="sxs-lookup"><span data-stu-id="15940-111">Item No.</span></span>|<span data-ttu-id="15940-112">Filnamn</span><span class="sxs-lookup"><span data-stu-id="15940-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="15940-113">1000</span><span class="sxs-lookup"><span data-stu-id="15940-113">1000</span></span>|<span data-ttu-id="15940-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="15940-114">1000.bmp</span></span>|
    |<span data-ttu-id="15940-115">1001</span><span class="sxs-lookup"><span data-stu-id="15940-115">1001</span></span>|<span data-ttu-id="15940-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="15940-116">1001.bmp</span></span>|
    |<span data-ttu-id="15940-117">1002</span><span class="sxs-lookup"><span data-stu-id="15940-117">1002</span></span>|<span data-ttu-id="15940-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="15940-118">1002.bmp</span></span>|

2. <span data-ttu-id="15940-119">Samla alla filer i ZIP-filen.</span><span class="sxs-lookup"><span data-stu-id="15940-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="15940-120">Till exempel i Windows Explorer, markerar du filerna och väljer **skicka till**, **komprimerad mapp**.</span><span class="sxs-lookup"><span data-stu-id="15940-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="15940-121">För att importera artikelbilder</span><span class="sxs-lookup"><span data-stu-id="15940-121">To import item pictures</span></span>
1. <span data-ttu-id="15940-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lagerinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="15940-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="15940-123">Välj åtgärden **Importera artikelbilder**.</span><span class="sxs-lookup"><span data-stu-id="15940-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="15940-124">I fältet **Välj en ZIP-fil** markerar du relevant ZIP-mapp och väljer sedan knappen **öppna**.</span><span class="sxs-lookup"><span data-stu-id="15940-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="15940-125">En rad för varje artikel och bild skapas på sidan **Importera artikelbilder**.</span><span class="sxs-lookup"><span data-stu-id="15940-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="15940-126">För artikelkort som redan har en bild markeras kryssrutan **bilden finns redan**.</span><span class="sxs-lookup"><span data-stu-id="15940-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="15940-127">Om du inte vill att några befintliga bilder ska bytas ut avmarkerar du kryssrutan **ersätta bilder**.</span><span class="sxs-lookup"><span data-stu-id="15940-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="15940-128">Om du vill ta bort de enskilda befintliga bilderna som ska ersättas tar du bort de aktuella raderna.</span><span class="sxs-lookup"><span data-stu-id="15940-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="15940-129">Välj åtgärden **Importera bilder**.</span><span class="sxs-lookup"><span data-stu-id="15940-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="15940-130">Fältet **importstatus** uppdateras för att visa om bildimporten har hoppas över eller slutförts.</span><span class="sxs-lookup"><span data-stu-id="15940-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="15940-131">Se även</span><span class="sxs-lookup"><span data-stu-id="15940-131">See Also</span></span>
[<span data-ttu-id="15940-132">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="15940-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="15940-133">Skapa nummerserier</span><span class="sxs-lookup"><span data-stu-id="15940-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="15940-134">Lager</span><span class="sxs-lookup"><span data-stu-id="15940-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="15940-135">Inköp</span><span class="sxs-lookup"><span data-stu-id="15940-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="15940-136">Försäljning</span><span class="sxs-lookup"><span data-stu-id="15940-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="15940-137">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="15940-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>