---
title: "Ställa in lagervärdering och lagerkostnad | Microsoft Docs"
description: "I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: af4c256b59739abce9ec22bce254fe8e2dff4e29
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a><span data-ttu-id="afe9e-103">Ställa in lagervärdering och lagerkostnad</span><span class="sxs-lookup"><span data-stu-id="afe9e-103">Setting Up Inventory Valuation and Costing</span></span>
<span data-ttu-id="afe9e-104">Om du vill se till att lagerkostnaderna registreras korrekt, ställer du in olika fält och fönster innan du gör artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="afe9e-104">To make sure that inventory costs are recorded correctly, you must set up various fields and windows before you begin to make item transactions.</span></span>

<span data-ttu-id="afe9e-105">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="afe9e-105">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="afe9e-106">**Om du vill**</span><span class="sxs-lookup"><span data-stu-id="afe9e-106">**To**</span></span>|<span data-ttu-id="afe9e-107">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="afe9e-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="afe9e-108">ange en värderingsprincip för varje artikel för att styra hur dess ingående kostnad används för att fastställa lagervärde och kostnaden för sålda varor.</span><span class="sxs-lookup"><span data-stu-id="afe9e-108">Set a costing method for each item to govern how its incoming cost is used to assess inventory value and the cost of goods sold.</span></span>|[<span data-ttu-id="afe9e-109">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="afe9e-109">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="afe9e-110">se till att kostnaden automatiskt bokförs i redovisningen när en lagertransaktion bokförs.</span><span class="sxs-lookup"><span data-stu-id="afe9e-110">Ensure that the cost is automatically posted to the general ledger whenever an inventory transaction is posted.</span></span>|<span data-ttu-id="afe9e-111">Fältet **Automatisk kostnadsbokföring** på sidan **Lagerinställning**</span><span class="sxs-lookup"><span data-stu-id="afe9e-111">**Automatic Cost Posting** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="afe9e-112">se till att förväntade kostnader bokförs i redovisningen så att du från de interima redovisningskontona Fkan se en uppskattning av beloppen som förfaller till betalning och kostnaden för de köpta eller sålda artiklarna innan de faktiskt faktureras.</span><span class="sxs-lookup"><span data-stu-id="afe9e-112">Ensure that expected costs are posted to the general ledger to see from the interim G/L accounts an estimate of the amounts due and the cost of the traded items before they are actually invoiced.</span></span>|<span data-ttu-id="afe9e-113">Fältet **Förväntad kost.bokf. i redov.** på sidan **Lagerinställning**</span><span class="sxs-lookup"><span data-stu-id="afe9e-113">**Expected Cost Posting to G/L** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="afe9e-114">ställa in systemet till att automatiskt justera för alla kostnadsändringar varje gång du bokför lagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="afe9e-114">Set the system up to adjust for any cost changes automatically every time you post inventory transactions.</span></span>|[<span data-ttu-id="afe9e-115">Justera artikelkostnader</span><span class="sxs-lookup"><span data-stu-id="afe9e-115">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="afe9e-116">definiera om genomsnittskostnaden ska beräknas endast per artikel eller per artikel för varje lagerställeenhet och för varje variant av artikeln.</span><span class="sxs-lookup"><span data-stu-id="afe9e-116">Define if the average cost is to be calculated per item only or per item for each stockkeping unit and for each variant of the item.</span></span>|<span data-ttu-id="afe9e-117">Fältet **Genoms. kost.ber.typ** på sidan **Lagerinställningar**</span><span class="sxs-lookup"><span data-stu-id="afe9e-117">**Average Cost Calc. Type** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="afe9e-118">välja den tidsperiod som ska användas för att beräkna vägd genomsnittskostnad för de artiklar som du använder genomsnittsvärderingsprincipen för.</span><span class="sxs-lookup"><span data-stu-id="afe9e-118">Select the period of time you would like the program to use for calculating the weighted average cost of items that use the average costing method.</span></span>|<span data-ttu-id="afe9e-119">Fältet **Genomsnittskostnadsperiod** på sidan **Lagerinställningar**</span><span class="sxs-lookup"><span data-stu-id="afe9e-119">**Average Cost Period** field in the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="afe9e-120">definiera lagerperioder för att kontrollera lagervärde över tid genom att inaktivera transaktionsbokföring i avslutade lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="afe9e-120">Define inventory periods to control inventory value over time by disallowing transaction posting in closed inventory periods.</span></span>|[<span data-ttu-id="afe9e-121">Arbeta med lagerperioder</span><span class="sxs-lookup"><span data-stu-id="afe9e-121">Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="afe9e-122">se till att försäljningsreturer kopplas till den ursprungliga avgående transaktionen så att lagervärdet bevaras.</span><span class="sxs-lookup"><span data-stu-id="afe9e-122">Ensure that sales returns are applied to the original outbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="afe9e-123">**Exakt kostnadsåterföring** på sidan **Försäljning & kundreskontra**</span><span class="sxs-lookup"><span data-stu-id="afe9e-123">**Exact Cost Reversing Mandatory** field in the **Sales & Receivables** page</span></span>|  
|<span data-ttu-id="afe9e-124">se till att inköpsreturer kopplas till den ursprungliga ankommande transaktionen så att lagervärdet bevaras.</span><span class="sxs-lookup"><span data-stu-id="afe9e-124">Ensure that purchase returns are applied to the original inbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="afe9e-125">**Exakt kostnadsåterföring** på sidan **Inköp & Leverantörsreskontra**</span><span class="sxs-lookup"><span data-stu-id="afe9e-125">**Exact Cost Reversing Mandatory** field in the **´Purchases & Payables** page</span></span>|
|<span data-ttu-id="afe9e-126">ange avrundningsreglerna som ska användas när artikelpriser justeras eller föreslås och när standardkostnader justeras eller föreslås.</span><span class="sxs-lookup"><span data-stu-id="afe9e-126">Set up the rounding rules to apply when adjusting or suggesting item prices and when adjusting or suggesting standard costs.</span></span>|<span data-ttu-id="afe9e-127">Sidan **Avrundningsmetod**</span><span class="sxs-lookup"><span data-stu-id="afe9e-127">**Rounding Method** page</span></span>|  

## <a name="see-also"></a><span data-ttu-id="afe9e-128">Se även</span><span class="sxs-lookup"><span data-stu-id="afe9e-128">See Also</span></span>  
[<span data-ttu-id="afe9e-129">Hantera lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="afe9e-129">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="afe9e-130">Arbeta med Business Central</span><span class="sxs-lookup"><span data-stu-id="afe9e-130">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="afe9e-131">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="afe9e-131">Finance</span></span>](finance.md)  
