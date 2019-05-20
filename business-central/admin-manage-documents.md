---
title: Hantera, ta bort eller komprimera dokument | Microsoft Docs
description: Behåll historiska data eller ta bort dessa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 7f0024f54979a563e885242d7160bc2b615493a5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246636"
---
# <a name="manage-documents"></a><span data-ttu-id="ac746-103">Hantera dokument</span><span class="sxs-lookup"><span data-stu-id="ac746-103">Manage Documents</span></span>
<span data-ttu-id="ac746-104">En central roll, till exempel programadministratören, måste regelbundet hantera historiska dokument genom att ta bort eller komprimera dem.</span><span class="sxs-lookup"><span data-stu-id="ac746-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="ac746-105">Ta bort dokument</span><span class="sxs-lookup"><span data-stu-id="ac746-105">Delete Documents</span></span>
<span data-ttu-id="ac746-106">I vissa fall kan det hända att du behöver ta bort fakturerade inköpsorder som inte raderats.</span><span class="sxs-lookup"><span data-stu-id="ac746-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> <span data-ttu-id="ac746-107">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrolleras att borttagna inköpsorder har fakturerats helt.</span><span class="sxs-lookup"><span data-stu-id="ac746-107">[!INCLUDE[d365fin](includes/d365fin_md.md)] checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="ac746-108">Du kan inte ta bort order som inte har fakturerats och inlevererats helt.</span><span class="sxs-lookup"><span data-stu-id="ac746-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="ac746-109">Returorder tas vanligtvis bort när de har fakturerats.</span><span class="sxs-lookup"><span data-stu-id="ac746-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="ac746-110">När du bokför en faktura överförs den till sidan **Bokförd inköpskreditnota**.</span><span class="sxs-lookup"><span data-stu-id="ac746-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** page.</span></span> <span data-ttu-id="ac746-111">Om du har markerat kryssrutan **Returutleverans i kreditnota** på sidan **Inköpsinställningar** överförs fakturan till sidan **Bokförd returutleverans**.</span><span class="sxs-lookup"><span data-stu-id="ac746-111">If you selected the **Return Shipment on Credit Memo** check box on the **Purchases & Payable Setup** page, then the invoice is transferred to the **Posted Return Shipment** page.</span></span> <span data-ttu-id="ac746-112">Du kan ta bort dokumenten med hjälp av batch-jobbet **Ta bort faktrd inköpsret.order**.</span><span class="sxs-lookup"><span data-stu-id="ac746-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="ac746-113">Innan du tar bort, kontrollerar batch-jobbet om inköpsreturorder är helt levererade eller fakturerade.</span><span class="sxs-lookup"><span data-stu-id="ac746-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="ac746-114">Avropsorder tas inte bort när du har behandlat och fakturerat alla relaterade inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="ac746-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="ac746-115">Du kan ta bort avropsorder med batch-jobbet **Ta bort fakturerade avropsorder**.</span><span class="sxs-lookup"><span data-stu-id="ac746-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="ac746-116">Fakturerade serviceorder tas vanligtvis bort när de har fakturerats helt.</span><span class="sxs-lookup"><span data-stu-id="ac746-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="ac746-117">När en faktura bokförs skapas en motsvarande transaktion på sidan **Bokförda servicefakturor**.</span><span class="sxs-lookup"><span data-stu-id="ac746-117">When an invoice is posted, a corresponding entry is created on the **Posted Service Invoices** page.</span></span> <span data-ttu-id="ac746-118">Det bokförda dokumentet kan visas från sidan **Bokförd servicefaktura**.</span><span class="sxs-lookup"><span data-stu-id="ac746-118">The posted document can be viewed on the **Posted Service Invoice** page.</span></span>  

<span data-ttu-id="ac746-119">Tjänsteordern tas inte bort automatiskt, men om det totala antalet i ordern inte har bokförts från själva serviceordern, utan från sidan **Servicefaktura**, gäller följande.</span><span class="sxs-lookup"><span data-stu-id="ac746-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** page.</span></span> <span data-ttu-id="ac746-120">Då kan du behöva ta bort fakturerade order som inte har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ac746-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="ac746-121">Du kan göra detta genom att köra batch-jobbet **Ta bort fakturerade serviceorder**.</span><span class="sxs-lookup"><span data-stu-id="ac746-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ac746-122">Se även</span><span class="sxs-lookup"><span data-stu-id="ac746-122">See Also</span></span>  
[<span data-ttu-id="ac746-123">Administration</span><span class="sxs-lookup"><span data-stu-id="ac746-123">Administration</span></span>](admin-setup-and-administration.md)  
