---
title: Använd korsreferenser för objektet | Microsoft Docs
description: Om du har skapat en tvärreferens mellan den artikelbeskrivning som du använder för en artikel och den beskrivning som används för leverantören som levererar den artikeln och leverantörens artikelbeskrivning infogas automatiskt på inköpsdokument för en leverantör när du fyller i fältet **Tvärreferensnr** .
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1b914c3c1c5e640894f1ee48639c547421c27be4
ms.sourcegitcommit: 0c6f4382fad994fb6aea9dcde3b2dc25382c5968
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484040"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="d70de-104">Använd artikeltvärreferenser</span><span class="sxs-lookup"><span data-stu-id="d70de-104">Use Item Cross References</span></span>
<span data-ttu-id="d70de-105">Om du har skapat en tvärreferens mellan den artikelbeskrivning som du använder för en artikel och den beskrivning som används för leverantören som levererar den artikeln och leverantörens artikelbeskrivning infogas automatiskt på inköpsdokument för en leverantör när du fyller i fältet **Tvärreferensnr**</span><span class="sxs-lookup"><span data-stu-id="d70de-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="d70de-106">.</span><span class="sxs-lookup"><span data-stu-id="d70de-106">field.</span></span> <span data-ttu-id="d70de-107">Samma sak gäller för kundens artikelnummer i försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="d70de-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="d70de-108">I följande procedurer beskrivs hur du använder artikelns tvärreferens på inköpssidan.</span><span class="sxs-lookup"><span data-stu-id="d70de-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="d70de-109">Momenten är liknande för försäljningssidan.</span><span class="sxs-lookup"><span data-stu-id="d70de-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="d70de-110">Så här skapar du en artikeltvärreferens för en leverantörs artikelbeskrivning</span><span class="sxs-lookup"><span data-stu-id="d70de-110">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="d70de-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d70de-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="d70de-112">Öppna kortet för en artikel som du vill skapa en korsreferens till för den artikelbeskrivning som leverantören använder för artikeln.</span><span class="sxs-lookup"><span data-stu-id="d70de-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="d70de-113">Välj åtgärd **tvärreferenser**.</span><span class="sxs-lookup"><span data-stu-id="d70de-113">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="d70de-114">Om du inte hittar åtgärden **artikeltvärreferenser** väljer du om du vill visa fler alternativ och sedan söka efter den under **navigera**, **artikel**.</span><span class="sxs-lookup"><span data-stu-id="d70de-114">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Navigate**, **Item**.</span></span>
  
4. <span data-ttu-id="d70de-115">På en ny rad på sidan **Artikel tvärreferenstrans**, fyll i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="d70de-115">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="d70de-116">.</span><span class="sxs-lookup"><span data-stu-id="d70de-116">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="d70de-117">Ange leverantörens artikelbeskrivning på en inköpsorder</span><span class="sxs-lookup"><span data-stu-id="d70de-117">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="d70de-118">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d70de-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="d70de-119">Skapa en inköpsorder för leverantören som du ställer in en artikeltvärreferens för ovan.</span><span class="sxs-lookup"><span data-stu-id="d70de-119">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="d70de-120">Skapa en inköpsorderrad för artikeln som du ställer in en artikeltvärreferens för ovan.</span><span class="sxs-lookup"><span data-stu-id="d70de-120">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="d70de-121">I **Tvärreferensnummer**</span><span class="sxs-lookup"><span data-stu-id="d70de-121">In the **Cross-Reference No.**</span></span> <span data-ttu-id="d70de-122">välj artikeln artikelkorsreferens som du har skapat och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="d70de-122">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="d70de-123">Fältet **beskrivning** på raden skrivs över med leverantörens artikelbeskrivning som ställs in på korsreferensartikelns transaktion.</span><span class="sxs-lookup"><span data-stu-id="d70de-123">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="d70de-124">Se även</span><span class="sxs-lookup"><span data-stu-id="d70de-124">See Also</span></span>
[<span data-ttu-id="d70de-125">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="d70de-125">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="d70de-126">Lager</span><span class="sxs-lookup"><span data-stu-id="d70de-126">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="d70de-127">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d70de-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
