---
title: Spärra artiklar för försäljning eller inköp
description: I Business Central kan en artikel markeras som spärrad för försäljning, spärrad för inköp eller spärrad för alla syften.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 12/04/2019
ms.author: sgroespe
ms.openlocfilehash: 0218cf1b4982b9e8c5b5c2817590bc5ebd8f1941
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896067"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="8526a-103">Spärra artiklar för försäljning eller inköp</span><span class="sxs-lookup"><span data-stu-id="8526a-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="8526a-104">Du kan spärra en artikel så att den inte kan registreras på försäljnings- eller inköpsrader eller bokföras i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="8526a-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="8526a-105">I följande tabell visas vad som händer när artiklar spärras.</span><span class="sxs-lookup"><span data-stu-id="8526a-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="8526a-106">Alternativ</span><span class="sxs-lookup"><span data-stu-id="8526a-106">Option</span></span>|<span data-ttu-id="8526a-107">Description</span><span class="sxs-lookup"><span data-stu-id="8526a-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="8526a-108">**Spärrad för försäljning**</span><span class="sxs-lookup"><span data-stu-id="8526a-108">**Sales Blocked**</span></span>|<span data-ttu-id="8526a-109">Du kan inte registrera artikeln i ett försäljningsdokument eller en artikeljournal för försäljning.</span><span class="sxs-lookup"><span data-stu-id="8526a-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="8526a-110">**Spärrad för inköp**</span><span class="sxs-lookup"><span data-stu-id="8526a-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="8526a-111">Du kan inte registrera artikeln i ett inköpsdokument, en artikeljournal för inköp eller i planeringsprocesser för inköp.</span><span class="sxs-lookup"><span data-stu-id="8526a-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="8526a-112">**Spärrad**</span><span class="sxs-lookup"><span data-stu-id="8526a-112">**Blocked**</span></span>|<span data-ttu-id="8526a-113">Du kan inte använda artikeln för någon artikeltransaktion.</span><span class="sxs-lookup"><span data-stu-id="8526a-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="8526a-114">Spärrade artiklar kan returneras.</span><span class="sxs-lookup"><span data-stu-id="8526a-114">Blocked items can be returned.</span></span> <span data-ttu-id="8526a-115">Detta innebär att inga av inställningarna ovan gäller när artikeln används för returorder och kreditnotor.</span><span class="sxs-lookup"><span data-stu-id="8526a-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="8526a-116">När du använder funktionen **kopiera dokument** för att skapa nya dokument som bygger på befintliga dokument, får du ett meddelande om något av artiklarna på källdokumentraderna är blockerat.</span><span class="sxs-lookup"><span data-stu-id="8526a-116">When you use the **Copy Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="8526a-117">De spärrade dokumentraderna tas inte med i det nya dokumentet och ett meddelande visar en översikt över alla dokumentrader som har spärrats i källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="8526a-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="8526a-118">Så här spärrar du en artikel så att den inte kan registreras på försäljningsrader</span><span class="sxs-lookup"><span data-stu-id="8526a-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="8526a-119">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8526a-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8526a-120">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för försäljning**.</span><span class="sxs-lookup"><span data-stu-id="8526a-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="8526a-121">Om du försöker registrera artikeln i ett försäljningsdokument eller på en journalrad visas ett felmeddelande om att artikeln är spärrad.</span><span class="sxs-lookup"><span data-stu-id="8526a-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="8526a-122">Så här spärrar du en artikel så att den inte kan registreras på inköpsrader</span><span class="sxs-lookup"><span data-stu-id="8526a-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="8526a-123">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8526a-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8526a-124">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för inköp**.</span><span class="sxs-lookup"><span data-stu-id="8526a-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="8526a-125">Om du försöker registrera artikeln i ett inköpsdokument eller på en journalrad visas ett felmeddelande om att artikeln är spärrad.</span><span class="sxs-lookup"><span data-stu-id="8526a-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="8526a-126">Så här spärrar du en artikel så att den inte kan bokföras</span><span class="sxs-lookup"><span data-stu-id="8526a-126">To block an item from being posted</span></span>
1. <span data-ttu-id="8526a-127">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8526a-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="8526a-128">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad**.</span><span class="sxs-lookup"><span data-stu-id="8526a-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="8526a-129">Om du försöker bokföra någon typ av transaktion för artikeln visas ett felmeddelande om att artikeln är spärrad.</span><span class="sxs-lookup"><span data-stu-id="8526a-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="8526a-130">Se även</span><span class="sxs-lookup"><span data-stu-id="8526a-130">See Also</span></span>  
[<span data-ttu-id="8526a-131">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="8526a-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="8526a-132">Lager</span><span class="sxs-lookup"><span data-stu-id="8526a-132">Inventory</span></span>](inventory-manage-inventory.md)  
