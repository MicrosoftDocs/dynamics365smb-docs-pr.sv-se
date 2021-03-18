---
title: Så här definierar du leveransmetoder
description: Du kan lägga upp en kod för var och en av dina leveransmetoder , samt ange information om dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 03/09/2021
ms.author: edupont
ms.openlocfilehash: 096b609d26ad24785f90634d725d751ac57b346e
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573307"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="7c062-103">Så här definierar du leveransmetoder</span><span class="sxs-lookup"><span data-stu-id="7c062-103">Set Up Shipment Methods</span></span>

<span data-ttu-id="7c062-104">Utleveransmetoderna är ofta beroende av vilka artiklar, kunder eller leverantörer som avses.</span><span class="sxs-lookup"><span data-stu-id="7c062-104">Shipment methods often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="7c062-105">Om kunden t. ex. bor på en ö kan han eller hon välja att få artiklarna levererade per flyg eller båt.</span><span class="sxs-lookup"><span data-stu-id="7c062-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="7c062-106">Vissa kunder kan kräva leverans nästa dag.</span><span class="sxs-lookup"><span data-stu-id="7c062-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="7c062-107">En del kanske vill plocka upp ordern.</span><span class="sxs-lookup"><span data-stu-id="7c062-107">Some may want to pick up the order.</span></span> <span data-ttu-id="7c062-108">På kund- och leverantörskorten kan du ange vilken typ av leverans som önskas.</span><span class="sxs-lookup"><span data-stu-id="7c062-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="7c062-109">Du upprättar en beskrivning och en kod för varje leveransvillkor på sidan **Leveransmetoder**.</span><span class="sxs-lookup"><span data-stu-id="7c062-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="7c062-110">Du kan t. ex. upprätta koden FOB och i fältet **Beskrivning** skriver du Fritt ombord.</span><span class="sxs-lookup"><span data-stu-id="7c062-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="7c062-111">Du kan skriva in koden i fältet **Leveransmetodkod** någon annanstans i systemet, t. ex. på ett kundkort.</span><span class="sxs-lookup"><span data-stu-id="7c062-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="7c062-112">När du sedan skapar nya order, fakturor, kreditnotor, etc. fyller systemet i den beskrivning, som representeras av koden.</span><span class="sxs-lookup"><span data-stu-id="7c062-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="7c062-113">Du kan ändra den i dokumentet om det behövs.</span><span class="sxs-lookup"><span data-stu-id="7c062-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-method"></a><span data-ttu-id="7c062-114">Så här definierar du utleveransvillkor</span><span class="sxs-lookup"><span data-stu-id="7c062-114">To set up a shipment method</span></span>

1. <span data-ttu-id="7c062-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **leveransmetoder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7c062-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="7c062-116">På sidan **Leveransmetoder** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7c062-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="7c062-117">På den nya raden anger du en kod och en beskrivning för leveransmetoden.</span><span class="sxs-lookup"><span data-stu-id="7c062-117">On the new line, specify a code and description for the shipment method.</span></span>

> [!TIP]
> <span data-ttu-id="7c062-118">Om du använder Incoterms ställer du in utleveransmetoder för att representera relevanta Incoterms-regler.</span><span class="sxs-lookup"><span data-stu-id="7c062-118">If you use Incoterms, set up shipment methods to represent the relevant Incoterms rules.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7c062-119">Se även</span><span class="sxs-lookup"><span data-stu-id="7c062-119">See Also</span></span>

[<span data-ttu-id="7c062-120">Så här konfigurerar du speditörer</span><span class="sxs-lookup"><span data-stu-id="7c062-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
[<span data-ttu-id="7c062-121">Spåra paket</span><span class="sxs-lookup"><span data-stu-id="7c062-121">Track Packages</span></span>](sales-how-track-packages.md)  
[<span data-ttu-id="7c062-122">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="7c062-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="7c062-123">Lager</span><span class="sxs-lookup"><span data-stu-id="7c062-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="7c062-124">Ställa in lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="7c062-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="7c062-125">Monteringshantering</span><span class="sxs-lookup"><span data-stu-id="7c062-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="7c062-126">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="7c062-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="7c062-127">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7c062-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="7c062-128">Incoterms på iccwbo.org</span><span class="sxs-lookup"><span data-stu-id="7c062-128">Incoterms on iccwbo.org</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]