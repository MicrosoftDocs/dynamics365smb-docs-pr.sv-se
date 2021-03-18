---
title: SÅ här använder du objektfamiljer i produktion | Microsoft Docs
description: Huvuduppgiften när du anpassar en baskalender för företaget, eller någon av dess affärspartner, är att ange eventuella ändringar av status som arbetsdag eller ledig dag.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4c926b8f7663c805f07bcd7c85339b109f85a7ff
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383206"
---
# <a name="work-with-production-families"></a><span data-ttu-id="d5280-103">Arbeta med produktionsfamiljer</span><span class="sxs-lookup"><span data-stu-id="d5280-103">Work with Production Families</span></span>
<span data-ttu-id="d5280-104">En produktionsfamilj är en grupp enskilda artiklar med liknande tillverkningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="d5280-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="d5280-105">Om du utformar produktionsfamiljer kan vissa artiklar tillverkas två eller flera gånger i en produktion, vilket optimerar materialförbrukningen.</span><span class="sxs-lookup"><span data-stu-id="d5280-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="d5280-106">I fältet **Antal** på sidan **Familj** anger du den kvantitet som ska produceras när hela familjen har tillverkats en gång.</span><span class="sxs-lookup"><span data-stu-id="d5280-106">In the **Quantity** field on the **Family** page, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="d5280-107">Exempel</span><span class="sxs-lookup"><span data-stu-id="d5280-107">Example</span></span>
<span data-ttu-id="d5280-108">I stansningsprocesser kan fyra enheter av en artikel produceras av ett ark och tio enheter av en annan artikel av samma ark.</span><span class="sxs-lookup"><span data-stu-id="d5280-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="d5280-109">Stansningsmaskinen stansar alla 14 enheterna i ett steg.</span><span class="sxs-lookup"><span data-stu-id="d5280-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="d5280-110">Genom att skapa produktionsfamiljer minskas spillet eftersom materialet som vanligtvis blir över när stora enheter produceras kan användas till produktionen av små enheter.</span><span class="sxs-lookup"><span data-stu-id="d5280-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="d5280-111">Så här skapar du produktionfamilj</span><span class="sxs-lookup"><span data-stu-id="d5280-111">To set up a production family</span></span>
1. <span data-ttu-id="d5280-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Familjer** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d5280-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="d5280-113">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="d5280-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a><span data-ttu-id="d5280-114">Om du vill skapa baserat på en produktionsfamilj</span><span class="sxs-lookup"><span data-stu-id="d5280-114">To produce based on a production family</span></span>
1. <span data-ttu-id="d5280-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Fast planerad prod.order** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d5280-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="d5280-116">Skapa en nu produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="d5280-116">Create a new production order.</span></span> <span data-ttu-id="d5280-117">För mer information, se [Skapa produktionsorder](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="d5280-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="d5280-118">I fältet **Ursprungstyp** väljer du **Familj**.</span><span class="sxs-lookup"><span data-stu-id="d5280-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="d5280-119">I fältet **Ursprungsnr.** väljer du relevant produktionsfamilj.</span><span class="sxs-lookup"><span data-stu-id="d5280-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5280-120">Se även</span><span class="sxs-lookup"><span data-stu-id="d5280-120">See Also</span></span>
[<span data-ttu-id="d5280-121">Skapa produktionsstrukturer</span><span class="sxs-lookup"><span data-stu-id="d5280-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="d5280-122">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="d5280-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="d5280-123">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="d5280-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="d5280-124">[Planerad](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="d5280-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="d5280-125">Lager</span><span class="sxs-lookup"><span data-stu-id="d5280-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d5280-126">Inköp</span><span class="sxs-lookup"><span data-stu-id="d5280-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="d5280-127">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d5280-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]