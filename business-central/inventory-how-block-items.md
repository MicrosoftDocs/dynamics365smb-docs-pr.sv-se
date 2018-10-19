---
title: "Spärra artiklar för försäljning eller inköp"
description: "I Business Central kan en artikel markeras som spärrad för försäljning, spärrad för inköp eller spärrad för alla syften."
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0d5ad688cfa6fb58e8383692362105beeee386f8
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="c2117-103">Spärra artiklar för försäljning eller inköp</span><span class="sxs-lookup"><span data-stu-id="c2117-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="c2117-104">Du kan spärra en artikel så att den inte kan registreras på försäljnings- eller inköpsrader eller bokföras i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="c2117-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="c2117-105">I följande tabell visas vad som händer när artiklar spärras.</span><span class="sxs-lookup"><span data-stu-id="c2117-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="c2117-106">Alternativ</span><span class="sxs-lookup"><span data-stu-id="c2117-106">Option</span></span>|<span data-ttu-id="c2117-107">Description</span><span class="sxs-lookup"><span data-stu-id="c2117-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="c2117-108">**Spärrad för försäljning**</span><span class="sxs-lookup"><span data-stu-id="c2117-108">**Sales Blocked**</span></span>|<span data-ttu-id="c2117-109">Du kan inte registrera artikeln i ett försäljningsdokument eller en artikeljournal för försäljning.</span><span class="sxs-lookup"><span data-stu-id="c2117-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="c2117-110">**Spärrad för inköp**</span><span class="sxs-lookup"><span data-stu-id="c2117-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="c2117-111">Du kan inte registrera artikeln i ett inköpsdokument, en artikeljournal för inköp eller i planeringsprocesser för inköp.</span><span class="sxs-lookup"><span data-stu-id="c2117-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="c2117-112">**Spärrad**</span><span class="sxs-lookup"><span data-stu-id="c2117-112">**Blocked**</span></span>|<span data-ttu-id="c2117-113">Du kan inte använda artikeln för någon artikeltransaktion.</span><span class="sxs-lookup"><span data-stu-id="c2117-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="c2117-114">Mer information om hur du spärrar en artikel för alla syften finns i Artikelkort.</span><span class="sxs-lookup"><span data-stu-id="c2117-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="c2117-115">Så här spärrar du en artikel så att den inte kan registreras på försäljningsrader</span><span class="sxs-lookup"><span data-stu-id="c2117-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="c2117-116">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c2117-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c2117-117">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för försäljning**.</span><span class="sxs-lookup"><span data-stu-id="c2117-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="c2117-118">Om du försöker registrera artikeln i ett försäljningsdokument eller på en journalrad visas ett felmeddelande om att artikeln är spärrad.</span><span class="sxs-lookup"><span data-stu-id="c2117-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="c2117-119">Så här spärrar du en artikel så att den inte kan registreras på inköpsrader</span><span class="sxs-lookup"><span data-stu-id="c2117-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="c2117-120">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c2117-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c2117-121">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för inköp**.</span><span class="sxs-lookup"><span data-stu-id="c2117-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="c2117-122">Om du försöker registrera artikeln i ett inköpsdokument eller på en journalrad visas ett felmeddelande om att artikeln är spärrad.</span><span class="sxs-lookup"><span data-stu-id="c2117-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="c2117-123">Så här spärrar du en artikel så att den inte kan bokföras</span><span class="sxs-lookup"><span data-stu-id="c2117-123">To block an item from being posted</span></span>
1. <span data-ttu-id="c2117-124">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c2117-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="c2117-125">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad**.</span><span class="sxs-lookup"><span data-stu-id="c2117-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="c2117-126">Om du försöker bokföra någon typ av transaktion för artikeln visas ett felmeddelande om att artikeln är spärrad.</span><span class="sxs-lookup"><span data-stu-id="c2117-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2117-127">Se även</span><span class="sxs-lookup"><span data-stu-id="c2117-127">See Also</span></span>  
[<span data-ttu-id="c2117-128">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="c2117-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="c2117-129">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="c2117-129">Inventory</span></span>](inventory-manage-inventory.md)  

