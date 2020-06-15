---
title: Spärra artiklar för försäljning eller inköp
description: Du kan förhindra att en artikel används, t.ex. i försäljnings- eller inköpsdokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 467b43b14f1905018c2a26a06c15abc5a0a17e99
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410650"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="4e2bf-103">Spärra artiklar för försäljning eller inköp</span><span class="sxs-lookup"><span data-stu-id="4e2bf-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="4e2bf-104">Du kan spärra en artikel så att den inte kan registreras på rader i försäljnings- eller inköpsdokument, och du kan även spärra den från att publiceras i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-104">You can block an item from being entered on lines in sales or purchase documents, and you can block it from being posted in any transaction.</span></span> <span data-ttu-id="4e2bf-105">Detta kan till exempel vara användbart när en artikel har en känd defekt.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-105">For example, this is useful when an item has a known defect.</span></span> <span data-ttu-id="4e2bf-106">Om någon väljer en spärrad artikel i ett försäljnings- eller inköpsdokument kommer ett meddelande att informera dem om att artikeln är spärrad.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-106">If someone chooses a blocked item on a sales or purchase document a message will inform them that the item is blocked.</span></span>

<span data-ttu-id="4e2bf-107">I följande tabell beskrivs vad som händer när artiklar spärras.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-107">The following table describes what occurs when items are blocked.</span></span>  

|<span data-ttu-id="4e2bf-108">Alternativ</span><span class="sxs-lookup"><span data-stu-id="4e2bf-108">Option</span></span>|<span data-ttu-id="4e2bf-109">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4e2bf-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="4e2bf-110">**Spärrad för försäljning**</span><span class="sxs-lookup"><span data-stu-id="4e2bf-110">**Sales Blocked**</span></span>|<span data-ttu-id="4e2bf-111">Du kan inte registrera artikeln i ett försäljningsdokument eller en artikeljournal för försäljning.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-111">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="4e2bf-112">**Spärrad för inköp**</span><span class="sxs-lookup"><span data-stu-id="4e2bf-112">**Purchasing Blocked**</span></span>|<span data-ttu-id="4e2bf-113">Du kan inte registrera artikeln i ett inköpsdokument, en artikeljournal för inköp eller i planeringsprocesser för inköp.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-113">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="4e2bf-114">**Spärrad**</span><span class="sxs-lookup"><span data-stu-id="4e2bf-114">**Blocked**</span></span>|<span data-ttu-id="4e2bf-115">Du kan inte använda artikeln för någon artikeltransaktion.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-115">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="4e2bf-116">Spärrade artiklar kan returneras.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-116">Blocked items can be returned.</span></span> <span data-ttu-id="4e2bf-117">Detta innebär att inga av inställningarna ovan gäller när artikeln används för returorder och kreditnotor.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-117">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="4e2bf-118">När du använder funktionen **Kopiera från dokument** för att skapa nya dokument som bygger på befintliga dokument får du ett meddelande om något av artiklarna på källdokumentraderna är blockerat.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-118">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="4e2bf-119">De spärrade dokumentraderna tas inte med i det nya dokumentet och ett meddelande visar en översikt över alla dokumentrader som har spärrats i källdokumentet.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-119">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="4e2bf-120">Så här spärrar du en artikel så att den inte kan registreras på försäljningsrader</span><span class="sxs-lookup"><span data-stu-id="4e2bf-120">To block an item from being entered on sales lines</span></span>  
1.  <span data-ttu-id="4e2bf-121">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4e2bf-122">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för försäljning**.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-122">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="4e2bf-123">Så här spärrar du en artikel så att den inte kan registreras på inköpsrader</span><span class="sxs-lookup"><span data-stu-id="4e2bf-123">To block an item from being entered on purchase lines</span></span>  
1.  <span data-ttu-id="4e2bf-124">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4e2bf-125">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för inköp**.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-125">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="4e2bf-126">Så här spärrar du en artikel så att den inte kan bokföras</span><span class="sxs-lookup"><span data-stu-id="4e2bf-126">To block an item from being posted</span></span>
1. <span data-ttu-id="4e2bf-127">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="4e2bf-128">Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad**.</span><span class="sxs-lookup"><span data-stu-id="4e2bf-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e2bf-129">Se även</span><span class="sxs-lookup"><span data-stu-id="4e2bf-129">See Also</span></span>  
[<span data-ttu-id="4e2bf-130">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="4e2bf-130">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="4e2bf-131">Lager</span><span class="sxs-lookup"><span data-stu-id="4e2bf-131">Inventory</span></span>](inventory-manage-inventory.md)  
