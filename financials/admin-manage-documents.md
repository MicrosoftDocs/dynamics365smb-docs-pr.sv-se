---
title: Hantera, ta bort eller komprimera dokument | Microsoft Docs
description: "Behåll historiska data eller ta bort dessa."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 10524be6bcfdc99672496b54903e4f04c33108ce
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="manage-documents"></a><span data-ttu-id="67b6b-103">Hantera dokument</span><span class="sxs-lookup"><span data-stu-id="67b6b-103">Manage Documents</span></span>
<span data-ttu-id="67b6b-104">En central roll, till exempel programadministratören, måste regelbundet hantera historiska dokument genom att ta bort eller komprimera dem.</span><span class="sxs-lookup"><span data-stu-id="67b6b-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="67b6b-105">Ta bort dokument</span><span class="sxs-lookup"><span data-stu-id="67b6b-105">Delete Documents</span></span>
<span data-ttu-id="67b6b-106">I vissa fall kan det hända att du behöver ta bort fakturerade inköpsorder som inte raderats.</span><span class="sxs-lookup"><span data-stu-id="67b6b-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> <span data-ttu-id="67b6b-107">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrolleras att borttagna inköpsorder har fakturerats helt.</span><span class="sxs-lookup"><span data-stu-id="67b6b-107">[!INCLUDE[d365fin](includes/d365fin_md.md)] checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="67b6b-108">Du kan inte ta bort order som inte har fakturerats och inlevererats helt.</span><span class="sxs-lookup"><span data-stu-id="67b6b-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="67b6b-109">Returorder tas vanligtvis bort när de har fakturerats.</span><span class="sxs-lookup"><span data-stu-id="67b6b-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="67b6b-110">När du bokför en faktura överförs den till fönstret **Bokförd inköpskreditnota**.</span><span class="sxs-lookup"><span data-stu-id="67b6b-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** window.</span></span> <span data-ttu-id="67b6b-111">Om du har markerat kryssrutan **Returutleverans i kreditnota** i fönstret **Inköpsinställningar** överförs fakturan till fönstret **Bokförd returutleverans**.</span><span class="sxs-lookup"><span data-stu-id="67b6b-111">If you selected the **Return Shipment on Credit Memo** check box in the **Purchases & Payable Setup** window, then the invoice is transferred to the **Posted Return Shipment** window.</span></span> <span data-ttu-id="67b6b-112">Du kan ta bort dokumenten med hjälp av batch-jobbet **Ta bort faktrd inköpsret.order**.</span><span class="sxs-lookup"><span data-stu-id="67b6b-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="67b6b-113">Innan du tar bort, kontrollerar batch-jobbet om inköpsreturorder är helt levererade eller fakturerade.</span><span class="sxs-lookup"><span data-stu-id="67b6b-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="67b6b-114">Avropsorder tas inte bort när du har behandlat och fakturerat alla relaterade inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="67b6b-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="67b6b-115">Du kan ta bort avropsorder med batch-jobbet **Ta bort fakturerade avropsorder**.</span><span class="sxs-lookup"><span data-stu-id="67b6b-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="67b6b-116">Fakturerade serviceorder tas vanligtvis bort när de har fakturerats helt.</span><span class="sxs-lookup"><span data-stu-id="67b6b-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="67b6b-117">När en faktura bokförs skapas en motsvarande transaktion i fönstret **Bokförda servicefakturor**.</span><span class="sxs-lookup"><span data-stu-id="67b6b-117">When an invoice is posted, a corresponding entry is created in the **Posted Service Invoices** window.</span></span> <span data-ttu-id="67b6b-118">Det bokförda dokumentet kan visas från fönstret **Bokförd servicefaktura**.</span><span class="sxs-lookup"><span data-stu-id="67b6b-118">The posted document can be viewed in the **Posted Service Invoice** window.</span></span>  

<span data-ttu-id="67b6b-119">Serviceordern tas inte bort automatiskt, men om det totala antalet i ordern inte har bokförts från själva serviceordern, utan från fönstret **Servicefaktura**, gäller följande.</span><span class="sxs-lookup"><span data-stu-id="67b6b-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** window.</span></span> <span data-ttu-id="67b6b-120">Då kan du behöva ta bort fakturerade order som inte har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="67b6b-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="67b6b-121">Du kan göra detta genom att köra batch-jobbet **Ta bort fakturerade serviceorder**.</span><span class="sxs-lookup"><span data-stu-id="67b6b-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="67b6b-122">Se även</span><span class="sxs-lookup"><span data-stu-id="67b6b-122">See Also</span></span>  
[<span data-ttu-id="67b6b-123">Installation och administration i Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="67b6b-123">Setup and Administration in Dynamics 365 for Financials</span></span>](admin-setup-and-administration.md)  
