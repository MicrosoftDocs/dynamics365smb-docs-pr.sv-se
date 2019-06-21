---
title: Spärra artiklar för försäljning eller inköp
description: I Business Central kan en artikel markeras som spärrad för försäljning, spärrad för inköp eller spärrad för alla syften.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8c98e4b893783c795a49e05ab04dc70b03161c6a
ms.sourcegitcommit: bf5f89dfaf5ad9f8f9902941cf3dac3e9f3553e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2019
ms.locfileid: "1594262"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="d2d15-103">Spärra artiklar för försäljning eller inköp</span><span class="sxs-lookup"><span data-stu-id="d2d15-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="d2d15-104">Du kan spärra en artikel så att den inte kan registreras på försäljnings- eller inköpsrader eller bokföras i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="d2d15-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="d2d15-105">I följande tabell visas vad som händer när artiklar spärras.</span><span class="sxs-lookup"><span data-stu-id="d2d15-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="d2d15-106">Alternativ</span><span class="sxs-lookup"><span data-stu-id="d2d15-106">Option</span></span>|<span data-ttu-id="d2d15-107">Description</span><span class="sxs-lookup"><span data-stu-id="d2d15-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="d2d15-108">**Spärrad för försäljning**</span><span class="sxs-lookup"><span data-stu-id="d2d15-108">**Sales Blocked**</span></span>|<span data-ttu-id="d2d15-109">Du kan inte registrera artikeln i ett försäljningsdokument eller en artikeljournal för försäljning.</span><span class="sxs-lookup"><span data-stu-id="d2d15-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="d2d15-110">**Spärrad för inköp**</span><span class="sxs-lookup"><span data-stu-id="d2d15-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="d2d15-111">Du kan inte registrera artikeln i ett inköpsdokument, en artikeljournal för inköp eller i planeringsprocesser för inköp.</span><span class="sxs-lookup"><span data-stu-id="d2d15-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="d2d15-112">**Spärrad**</span><span class="sxs-lookup"><span data-stu-id="d2d15-112">**Blocked**</span></span>|<span data-ttu-id="d2d15-113">Du kan inte använda artikeln för någon artikeltransaktion.</span><span class="sxs-lookup"><span data-stu-id="d2d15-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="d2d15-114">Spärrade artiklar kan returneras.</span><span class="sxs-lookup"><span data-stu-id="d2d15-114">Blocked items can be returned.</span></span> <span data-ttu-id="d2d15-115">Detta innebär att inga av inställningarna ovan gäller när artikeln används för returorder och kreditnotor.</span><span class="sxs-lookup"><span data-stu-id="d2d15-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="d2d15-116">Så här spärrar du en artikel så att den inte kan registreras på försäljningsrader</span><span class="sxs-lookup"><span data-stu-id="d2d15-116">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="d2d15-117">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d2d15-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d2d15-118">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för försäljning**.</span><span class="sxs-lookup"><span data-stu-id="d2d15-118">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="d2d15-119">Om du försöker registrera artikeln i ett försäljningsdokument eller på en journalrad visas ett felmeddelande om att artikeln är spärrad.</span><span class="sxs-lookup"><span data-stu-id="d2d15-119">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="d2d15-120">Så här spärrar du en artikel så att den inte kan registreras på inköpsrader</span><span class="sxs-lookup"><span data-stu-id="d2d15-120">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="d2d15-121">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d2d15-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d2d15-122">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för inköp**.</span><span class="sxs-lookup"><span data-stu-id="d2d15-122">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="d2d15-123">Om du försöker registrera artikeln i ett inköpsdokument eller på en journalrad visas ett felmeddelande om att artikeln är spärrad.</span><span class="sxs-lookup"><span data-stu-id="d2d15-123">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="d2d15-124">Så här spärrar du en artikel så att den inte kan bokföras</span><span class="sxs-lookup"><span data-stu-id="d2d15-124">To block an item from being posted</span></span>
1. <span data-ttu-id="d2d15-125">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d2d15-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="d2d15-126">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad**.</span><span class="sxs-lookup"><span data-stu-id="d2d15-126">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="d2d15-127">Om du försöker bokföra någon typ av transaktion för artikeln visas ett felmeddelande om att artikeln är spärrad.</span><span class="sxs-lookup"><span data-stu-id="d2d15-127">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2d15-128">Se även</span><span class="sxs-lookup"><span data-stu-id="d2d15-128">See Also</span></span>  
[<span data-ttu-id="d2d15-129">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="d2d15-129">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="d2d15-130">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="d2d15-130">Inventory</span></span>](inventory-manage-inventory.md)  
