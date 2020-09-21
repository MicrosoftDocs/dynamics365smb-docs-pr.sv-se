---
title: Så är skriver ut en lagerplocklista från en försäljningsorder
description: Du kan skriva ut en lagerplocklista direkt från en försäljningsorder, försäljningsfaktura och andra utgående försäljningsdokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/27/2020
ms.author: edupont
ms.openlocfilehash: fadf974c41b34a5beb7b3b313847cc6a5bfcec78
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781641"
---
# <a name="print-the-picking-list"></a><span data-ttu-id="a8932-103">Skriv ut plocklistan</span><span class="sxs-lookup"><span data-stu-id="a8932-103">Print the Picking List</span></span>
<span data-ttu-id="a8932-104">Du kan skriva ut en lista med inventering direkt från en försäljningsorder, en försäljningsfaktura eller något annat dokument som initierar leverans av varor.</span><span class="sxs-lookup"><span data-stu-id="a8932-104">You can print an inventory picking list directly from a sales order, a sales invoice, or any other document that initiates shipment of items.</span></span>

<span data-ttu-id="a8932-105">Den här rapporten används vanligtvis i företag utan dedikerad funktionalitet för lagerstyrning, så att en lager arbetare enkelt kan visa eller skriva ut plocklistan från det relaterade försäljningsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="a8932-105">This report is typically used in companies without dedicated functionality for warehouse management, so that an inventory worker can simply view or print the picking list from the related sales document.</span></span> <span data-ttu-id="a8932-106">I företag med högre volym eller mer komplexa processer planeras och utförs plockningen i dedikerade distributions lagerdokument.</span><span class="sxs-lookup"><span data-stu-id="a8932-106">In companies with higher volume or more complex processes, picking is planned and performed in dedicated warehouse documents.</span></span> <span data-ttu-id="a8932-107">Mer information finns i [Plocka artiklar](warehouse-pick-items.md).</span><span class="sxs-lookup"><span data-stu-id="a8932-107">For more information, see [Pick Items](warehouse-pick-items.md).</span></span>

## <a name="to-print-a-picking-list-from-a-sales-order"></a><span data-ttu-id="a8932-108">För att skriva ut en plockningslista från en försäljningsorder</span><span class="sxs-lookup"><span data-stu-id="a8932-108">To print a picking list from a sales order</span></span>  
<span data-ttu-id="a8932-109">Följande procedur är baserad på en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="a8932-109">The following procedure is based on a sales order.</span></span> <span data-ttu-id="a8932-110">Stegen är liknande för alla försäljningsdokument som kan användas för att initiera leverans av artiklar.</span><span class="sxs-lookup"><span data-stu-id="a8932-110">The steps are similar for all sales documents that can be used to initiate shipment of items.</span></span>

1. <span data-ttu-id="a8932-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **försäljningsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a8932-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a8932-112">Öppna en försäljningsorder som du vill plocka artiklar för.</span><span class="sxs-lookup"><span data-stu-id="a8932-112">Open the sales order that you want to pick items for.</span></span>  
3. <span data-ttu-id="a8932-113">Välj åtgärden **Rapport** och sedan åtgärden **Plockningslista efter order**.</span><span class="sxs-lookup"><span data-stu-id="a8932-113">Choose the **Report** action, and then choose the **Picking List by Order** action.</span></span>  
4. <span data-ttu-id="a8932-114">Välj **Skriv ut** för att skriva ut plockningslistan eller välj **Förhandsgranska** på för att visa den på skärmen.</span><span class="sxs-lookup"><span data-stu-id="a8932-114">Choose the **Print** button to print the picking list or choose the **Preview** button to view it on the screen.</span></span>

<span data-ttu-id="a8932-115">Du kan också spara plockningslistan som ett dokument, t.ex. skicka till någon eller lägga till en bilaga till försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="a8932-115">You can also save the picking list as a document, for example, to send to someone or to add as an attachment to the sales order.</span></span> <span data-ttu-id="a8932-116">För mer information, se [Hantera bifogade filer, länkar och anteckningar på kort och dokument](ui-how-add-link-to-record.md).</span><span class="sxs-lookup"><span data-stu-id="a8932-116">For more information, see [Manage Attachments, Links, and Notes on Cards and Documents](ui-how-add-link-to-record.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a8932-117">Om du använde funktionen **Expandera struktur** på försäljningsordern visas bara komponenterna för den relaterade monteringsartikeln i rapporten.</span><span class="sxs-lookup"><span data-stu-id="a8932-117">If you used the **Explode BOM** function on the sales order, then only the components of the related assembly item are shown in the report.</span></span> <span data-ttu-id="a8932-118">Mer information finns i [Arbeta med strukturer](inventory-how-work-BOMs.md).</span><span class="sxs-lookup"><span data-stu-id="a8932-118">For more information, see [Work with Bills of Material](inventory-how-work-BOMs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a8932-119">Se även</span><span class="sxs-lookup"><span data-stu-id="a8932-119">See Also</span></span>  
[<span data-ttu-id="a8932-120">Lager</span><span class="sxs-lookup"><span data-stu-id="a8932-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a8932-121">Plocka artiklar</span><span class="sxs-lookup"><span data-stu-id="a8932-121">Pick Items</span></span>](warehouse-pick-items.md)  
<span data-ttu-id="a8932-122">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a8932-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>   
