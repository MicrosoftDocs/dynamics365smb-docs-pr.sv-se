---
title: "Ange kedjan funktioner som stöds av Financials | Microsoft Docs"
description: "Få en produktöversikt och lär dig mer om viktiga leveranskedjebegrepp och processer som ingår i ERP-lösningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product overview, ERP
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 3bae84075dc505aa9318590b1fac06e4844ffafe
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="overview-of-supply-chain-functionality"></a><span data-ttu-id="39e56-103">Översikt över försörjningskedjefunktioner</span><span class="sxs-lookup"><span data-stu-id="39e56-103">Overview of Supply Chain Functionality</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="39e56-104"> stöder vanliga logistikprocesser, dock begränsat till behoven hos grossist- och distributionsföretag utan administrerad lagerhantering.</span><span class="sxs-lookup"><span data-stu-id="39e56-104"> supports common supply chain processes, although limited to the needs of wholesale and distribution companies without managed warehouse handling.</span></span>

<span data-ttu-id="39e56-105">Utöver försäljningsorderdokument kan du även administrera ditt orderuppfyllande med försäljningsorder, vilket ger dig möjlighet att exempelvis leverera delar av ett orderantal när den fullständiga kvantiteten inte är tillgänglig på en gång.</span><span class="sxs-lookup"><span data-stu-id="39e56-105">In addition to sales invoice documents, you can manage your order fulfillment with sales orders allowing you to ship parts of an order quantity, for example, because the full quantity is not available at once.</span></span> <span data-ttu-id="39e56-106">Du kan låta artiklar direktlevereras från leverantör till kund genom att länka försäljningsordern till den relaterade inköpsordern.</span><span class="sxs-lookup"><span data-stu-id="39e56-106">You can have items drop shipped directly from a vendor to a customer by linking the sales order to the related purchase order.</span></span>

<span data-ttu-id="39e56-107">Dina lagerkvantiteter uppdateras dynamiskt när du säljer och köper artiklar, och alla säljare erhåller tillgänglighetsinformation och varningar på flera olika sätt.</span><span class="sxs-lookup"><span data-stu-id="39e56-107">Your inventory quantities are dynamically updated as you sell and buy items, and availability information or warnings are shown to sales people in several ways.</span></span> <span data-ttu-id="39e56-108">Du kan ändra lagerkvantiteter manuellt genom att bokföra direkt till artikeltransaktionsposterna, exempelvis efter en inventering.</span><span class="sxs-lookup"><span data-stu-id="39e56-108">You can adjust inventory quantities manually by posting directly to the item ledger entries, for example, after a physical count.</span></span> <span data-ttu-id="39e56-109">Du kan erbjuda och sälja varor till kunderna utan att hålla lager åt dem.</span><span class="sxs-lookup"><span data-stu-id="39e56-109">You can offer and sell items to your customers without maintaining inventory for them.</span></span> <span data-ttu-id="39e56-110">Om du vill inkludera sådana ej lagerförda artiklar i din logistikprocess, konverterar du dem helt enkelt till vanliga artiklar.</span><span class="sxs-lookup"><span data-stu-id="39e56-110">If you want to include such nonstock items to your supply chain process, you simply convert them to normal items.</span></span>

<span data-ttu-id="39e56-111">Förutom inköpsorderdokument kan du även administrera din försörjningssida med inköpsorder som låter dig registrera delinleveranser av en orderkvantitet.</span><span class="sxs-lookup"><span data-stu-id="39e56-111">In addition to purchase invoice documents, you can manage your supply side with purchase orders allowing you to record partial receipts of an order quantity.</span></span> <span data-ttu-id="39e56-112">En enkel planeringsfunktion för inleveransen låter dig initiera en inköpsorder direkt från den försäljningsfaktura som behöver artiklarna.</span><span class="sxs-lookup"><span data-stu-id="39e56-112">A simple supply planning function allows you to initiate a purchase directly from the sales invoice that requires the items.</span></span>

<span data-ttu-id="39e56-113">Försäljnings- och inköpsdokument kan bokföras som levererade eller endast mottagna, eller som levererade eller inlevererade och fakturerade. Detta gör att du kan dela upp orderhandläggar- och revisorrollernas ansvar.</span><span class="sxs-lookup"><span data-stu-id="39e56-113">Both sales and purchase documents can be posted as shipped or received only or as shipped or received and invoiced, allowing you to split the responsibilities of order processors and accounting roles.</span></span>

<span data-ttu-id="39e56-114">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="39e56-114">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="39e56-115">Om du vill</span><span class="sxs-lookup"><span data-stu-id="39e56-115">To</span></span> | <span data-ttu-id="39e56-116">Gå till</span><span class="sxs-lookup"><span data-stu-id="39e56-116">See</span></span> |
| --- | --- |
| <span data-ttu-id="39e56-117">Registrera nya kunder, skapa försäljningserbjudanden, sälj produkter på order eller faktura, till exempel som direktleverans, samt administrera försäljningsreturer.</span><span class="sxs-lookup"><span data-stu-id="39e56-117">Register new customers, make sales offers, sell products on orders or invoices, for example as drop shipments, and manage sales returns.</span></span> |[<span data-ttu-id="39e56-118">Försäljning</span><span class="sxs-lookup"><span data-stu-id="39e56-118">Sales</span></span>](sales-manage-sales.md) |
| <span data-ttu-id="39e56-119">Registrera nya leverantörer, köp artiklar på order eller fakturor, till exempel initierade från en försäljningsfaktura, samt administrera inköpsreturer.</span><span class="sxs-lookup"><span data-stu-id="39e56-119">Register new vendors, purchase items on orders or invoices, for example initiated from a sales invoice, and manage purchase returns.</span></span> |[<span data-ttu-id="39e56-120">Inköp</span><span class="sxs-lookup"><span data-stu-id="39e56-120">Purchasing</span></span>](purchasing-manage-purchasing.md) |
| <span data-ttu-id="39e56-121">Registrera nya fysiska produkter eller tjänsteprodukter, justera lagersaldon och administrera lagervärdet genom att bokföra justerade kostnader i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="39e56-121">Register new physical or service products, adjust inventory quantities, and manage the inventory value by posting adjusted costs to the general ledger.</span></span> |[<span data-ttu-id="39e56-122">Lager</span><span class="sxs-lookup"><span data-stu-id="39e56-122">Inventory</span></span>](inventory-manage-inventory.md) |

## <a name="see-also"></a><span data-ttu-id="39e56-123">Se även</span><span class="sxs-lookup"><span data-stu-id="39e56-123">See Also</span></span>
[<span data-ttu-id="39e56-124">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="39e56-124">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="39e56-125">[Hantera kundreskontra](receivables-manage-receivables.md)   </span><span class="sxs-lookup"><span data-stu-id="39e56-125">[Managing Receivables](receivables-manage-receivables.md)   </span></span>  
[<span data-ttu-id="39e56-126">Ställa in inköp</span><span class="sxs-lookup"><span data-stu-id="39e56-126">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
<span data-ttu-id="39e56-127">[Hantera Leverantörsreskontra](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="39e56-127">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="39e56-128">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39e56-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="39e56-129">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="39e56-129">General Business Functionality</span></span>](ui-across-business-areas.md)

