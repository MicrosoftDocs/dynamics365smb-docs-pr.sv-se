---
title: "Ställa in lagervärdering och lagerkostnad | Microsoft Docs"
description: "I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: aa5ee6d9942390a2b4ad0aa8787172b0f7b141d0
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-inventory-valuation-and-costing"></a><span data-ttu-id="e8963-103">Ställa in lagervärdering och lagerkostnad</span><span class="sxs-lookup"><span data-stu-id="e8963-103">Setting Up Inventory Valuation and Costing</span></span>
<span data-ttu-id="e8963-104">Om du vill se till att lagerkostnaderna registreras korrekt, ställer du in olika fält och fönster innan du gör artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="e8963-104">To make sure that inventory costs are recorded correctly, you must set up various fields and windows before you begin to make item transactions.</span></span>

<span data-ttu-id="e8963-105">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="e8963-105">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="e8963-106">**Om du vill**</span><span class="sxs-lookup"><span data-stu-id="e8963-106">**To**</span></span>|<span data-ttu-id="e8963-107">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="e8963-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="e8963-108">ange en värderingsprincip för varje artikel för att styra hur dess ingående kostnad används för att fastställa lagervärde och kostnaden för sålda varor.</span><span class="sxs-lookup"><span data-stu-id="e8963-108">Set a costing method for each item to govern how its incoming cost is used to assess inventory value and the cost of goods sold.</span></span>|[<span data-ttu-id="e8963-109">Så här registrerar du nya objekt</span><span class="sxs-lookup"><span data-stu-id="e8963-109">How to: Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="e8963-110">se till att kostnaden automatiskt bokförs i redovisningen när en lagertransaktion bokförs.</span><span class="sxs-lookup"><span data-stu-id="e8963-110">Ensure that the cost is automatically posted to the general ledger whenever an inventory transaction is posted.</span></span>|<span data-ttu-id="e8963-111">Fältet **Automatisk kostnadsbokföring** på sidan **Lagerinställning**</span><span class="sxs-lookup"><span data-stu-id="e8963-111">**Automatic Cost Posting** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="e8963-112">se till att förväntade kostnader bokförs i redovisningen så att du från de interima redovisningskontona Fkan se en uppskattning av beloppen som förfaller till betalning och kostnaden för de köpta eller sålda artiklarna innan de faktiskt faktureras.</span><span class="sxs-lookup"><span data-stu-id="e8963-112">Ensure that expected costs are posted to the general ledger to see from the interim G/L accounts an estimate of the amounts due and the cost of the traded items before they are actually invoiced.</span></span>|<span data-ttu-id="e8963-113">Fältet **Förväntad kost.bokf. i redov.** på sidan **Lagerinställning**</span><span class="sxs-lookup"><span data-stu-id="e8963-113">**Expected Cost Posting to G/L** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="e8963-114">ställa in systemet till att automatiskt justera för alla kostnadsändringar varje gång du bokför lagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="e8963-114">Set the system up to adjust for any cost changes automatically every time you post inventory transactions.</span></span>|[<span data-ttu-id="e8963-115">Så här justerar du artikelkostnader</span><span class="sxs-lookup"><span data-stu-id="e8963-115">How to: Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="e8963-116">definiera om genomsnittskostnaden ska beräknas endast per artikel eller per artikel för varje lagerställeenhet och för varje variant av artikeln.</span><span class="sxs-lookup"><span data-stu-id="e8963-116">Define if the average cost is to be calculated per item only or per item for each stockkeping unit and for each variant of the item.</span></span>|<span data-ttu-id="e8963-117">Fältet **Genoms. kost.ber.typ** på sidan **Lagerinställningar**</span><span class="sxs-lookup"><span data-stu-id="e8963-117">**Average Cost Calc. Type** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="e8963-118">välja den tidsperiod som ska användas för att beräkna vägd genomsnittskostnad för de artiklar som du använder genomsnittsvärderingsprincipen för.</span><span class="sxs-lookup"><span data-stu-id="e8963-118">Select the period of time you would like the program to use for calculating the weighted average cost of items that use the average costing method.</span></span>|<span data-ttu-id="e8963-119">Fältet **Genomsnittskostnadsperiod** på sidan **Lagerinställningar**</span><span class="sxs-lookup"><span data-stu-id="e8963-119">**Average Cost Period** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="e8963-120">definiera lagerperioder för att kontrollera lagervärde över tid genom att inaktivera transaktionsbokföring i avslutade lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="e8963-120">Define inventory periods to control inventory value over time by disallowing transaction posting in closed inventory periods.</span></span>|[<span data-ttu-id="e8963-121">Så här kan du arbeta med lagerperioder</span><span class="sxs-lookup"><span data-stu-id="e8963-121">How to: Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="e8963-122">se till att försäljningsreturer kopplas till den ursprungliga avgående transaktionen så att lagervärdet bevaras.</span><span class="sxs-lookup"><span data-stu-id="e8963-122">Ensure that sales returns are applied to the original outbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="e8963-123">**Exakt kostnadsåterföring** på sidan **Försäljning & kundreskontra**</span><span class="sxs-lookup"><span data-stu-id="e8963-123">**Exact Cost Reversing Mandatory** field in the **Sales & Receivables** page</span></span>|  
|<span data-ttu-id="e8963-124">se till att inköpsreturer kopplas till den ursprungliga ankommande transaktionen så att lagervärdet bevaras.</span><span class="sxs-lookup"><span data-stu-id="e8963-124">Ensure that purchase returns are applied to the original inbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="e8963-125">**Exakt kostnadsåterföring** på sidan **Inköp & Leverantörsreskontra**</span><span class="sxs-lookup"><span data-stu-id="e8963-125">**Exact Cost Reversing Mandatory** field in the **´Purchases & Payables** page</span></span>|
|<span data-ttu-id="e8963-126">ange avrundningsreglerna som ska användas när artikelpriser justeras eller föreslås och när standardkostnader justeras eller föreslås.</span><span class="sxs-lookup"><span data-stu-id="e8963-126">Set up the rounding rules to apply when adjusting or suggesting item prices and when adjusting or suggesting standard costs.</span></span>|<span data-ttu-id="e8963-127">Sidan **Avrundningsmetod**</span><span class="sxs-lookup"><span data-stu-id="e8963-127">**Rounding Method** page</span></span>|  

## <a name="see-also"></a><span data-ttu-id="e8963-128">Se även</span><span class="sxs-lookup"><span data-stu-id="e8963-128">See Also</span></span>  
[<span data-ttu-id="e8963-129">Hantera lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="e8963-129">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="e8963-130">Arbeta med Financials</span><span class="sxs-lookup"><span data-stu-id="e8963-130">Working with Financials</span></span>](ui-work-product.md)  
[<span data-ttu-id="e8963-131">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="e8963-131">Finance</span></span>](finance.md)  

