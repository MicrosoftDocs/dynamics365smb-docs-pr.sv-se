---
title: Så här skapar du leveransmetoder | Microsoft Docs
description: Du kan lägga upp en kod för var och en av dina leveransmetoder och ange information om dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f1916724c995f875d15b931e919d07d2253dcdb1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748300"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="385da-103">Så här definierar du leveransmetoder</span><span class="sxs-lookup"><span data-stu-id="385da-103">Set Up Shipment Methods</span></span>
<span data-ttu-id="385da-104">Leveransmetoder, även kallade incoterms är ofta beroende av vilka artiklar, kunder eller leverantörer som avses.</span><span class="sxs-lookup"><span data-stu-id="385da-104">Shipment methods, also called incoterms, often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="385da-105">Om kunden t.ex. bor på en ö kan han eller hon välja att få artiklarna levererade per flyg eller båt.</span><span class="sxs-lookup"><span data-stu-id="385da-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="385da-106">Vissa kunder kan kräva leverans nästa dag.</span><span class="sxs-lookup"><span data-stu-id="385da-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="385da-107">En del kanske vill plocka upp ordern.</span><span class="sxs-lookup"><span data-stu-id="385da-107">Some may want to pick up the order.</span></span> <span data-ttu-id="385da-108">På kund- och leverantörskorten kan du ange vilken typ av leverans som önskas.</span><span class="sxs-lookup"><span data-stu-id="385da-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="385da-109">Du upprättar en beskrivning och en kod för varje leveransvillkor på sidan **Leveransmetoder**.</span><span class="sxs-lookup"><span data-stu-id="385da-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="385da-110">Du kan t.ex. upprätta koden FOB och i fältet **Beskrivning** skriver du Fritt ombord.</span><span class="sxs-lookup"><span data-stu-id="385da-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="385da-111">Du kan skriva in koden i fältet **Leveransmetodkod** någon annanstans i systemet, t.ex. på ett kundkort.</span><span class="sxs-lookup"><span data-stu-id="385da-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="385da-112">När du sedan skapar nya order, fakturor, kreditnotor, etc. fyller systemet i den beskrivning, som representeras av koden.</span><span class="sxs-lookup"><span data-stu-id="385da-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="385da-113">Du kan ändra den i dokumentet om det behövs.</span><span class="sxs-lookup"><span data-stu-id="385da-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-code"></a><span data-ttu-id="385da-114">Så här skapar du en leveranskod</span><span class="sxs-lookup"><span data-stu-id="385da-114">To set up a shipment code</span></span>
1. <span data-ttu-id="385da-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **leveransmetoder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="385da-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="385da-116">På sidan **Leveransmetoder** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="385da-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="385da-117">På den nya raden anger du en kod och en beskrivning för leveransmetoden.</span><span class="sxs-lookup"><span data-stu-id="385da-117">On the new line, specify a code and description for the shipment method.</span></span>

## <a name="see-also"></a><span data-ttu-id="385da-118">Se även</span><span class="sxs-lookup"><span data-stu-id="385da-118">See Also</span></span>
[<span data-ttu-id="385da-119">Incoterms</span><span class="sxs-lookup"><span data-stu-id="385da-119">Incoterms</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  
[<span data-ttu-id="385da-120">Så här konfigurerar du speditörer</span><span class="sxs-lookup"><span data-stu-id="385da-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
<span data-ttu-id="385da-121">[Spåra paket](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="385da-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="385da-122">Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="385da-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="385da-123">Lager</span><span class="sxs-lookup"><span data-stu-id="385da-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="385da-124">[Ställa in lagerstyrning](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="385da-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="385da-125">[Monteringshantering](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="385da-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="385da-126">Designdetaljer: Lagerstyrning</span><span class="sxs-lookup"><span data-stu-id="385da-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="385da-127">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="385da-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
