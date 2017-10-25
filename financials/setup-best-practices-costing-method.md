---
title: "Ställa in bästa metoder - Värderingsprincip | Microsoft Docs"
description: "**Värderingsprincipen** på artikelkortet anger hur artikelns kostnadsflöde registreras och om ett faktiskt eller budgeterat värde ska kapitaliseras och användas i kostnadsberäkningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d4f533d42cc813d3ebc0ccbb00228a6c8e188c14
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="setup-best-practices-costing-method"></a><span data-ttu-id="8d37e-103">Lägga upp bästa metoder: Värderingsprincip</span><span class="sxs-lookup"><span data-stu-id="8d37e-103">Setup Best Practices: Costing Method</span></span>
<span data-ttu-id="8d37e-104">**Värderingsprincipen** på artikelkortet anger hur artikelns kostnadsflöde registreras och om ett faktiskt eller budgeterat värde ska kapitaliseras och användas i kostnadsberäkningen.</span><span class="sxs-lookup"><span data-stu-id="8d37e-104">The **Costing Method** on the item card defines item’s cost flow is recorded and whether an actual or budgeted value is capitalized and used in the cost calculation.</span></span>  

 <span data-ttu-id="8d37e-105">Det är viktigt att ange rätt värderingsprincip enligt artikeltyp och affärsmiljö för att garantera ekonomiska lager.</span><span class="sxs-lookup"><span data-stu-id="8d37e-105">Setting the correct costing method according to item type and business environment is important to ensure economical inventories.</span></span>  

 <span data-ttu-id="8d37e-106">I tabellen nedan finns bästa metod för hur du lägger upp fältet **Värderingsprincip**.</span><span class="sxs-lookup"><span data-stu-id="8d37e-106">The following table provides best practices on how to set up the **Costing Method** field.</span></span> <span data-ttu-id="8d37e-107">Mer information finns i [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8d37e-107">For more information, see [Design Details: Costing Methods](design-details-costing-methods.md).</span></span>  

|<span data-ttu-id="8d37e-108">Inställningsalternativ</span><span class="sxs-lookup"><span data-stu-id="8d37e-108">Setup option</span></span>|<span data-ttu-id="8d37e-109">Best practice</span><span class="sxs-lookup"><span data-stu-id="8d37e-109">Best practice</span></span>|<span data-ttu-id="8d37e-110">Kommentar</span><span class="sxs-lookup"><span data-stu-id="8d37e-110">Comment</span></span>|  
|------------------|-------------------|-------------|  
|<span data-ttu-id="8d37e-111">FIFO</span><span class="sxs-lookup"><span data-stu-id="8d37e-111">FIFO</span></span>|<span data-ttu-id="8d37e-112">Använd där produktkostnaden är fast.</span><span class="sxs-lookup"><span data-stu-id="8d37e-112">Use where the product cost is stable.</span></span><br /><br /> <span data-ttu-id="8d37e-113">Använd för artiklar med ett begränsat hållbarhetstid, eftersom den äldsta varor behöver säljas innan deras hållbarhetstid passerat.</span><span class="sxs-lookup"><span data-stu-id="8d37e-113">Use for items with a limited shelf life, because the oldest goods need to be sold before they pass their sell-by date.</span></span>|<span data-ttu-id="8d37e-114">En artikels styckkostnad är det verkliga värdet på en mottagen artikel, vald enligt FIFO-regeln.</span><span class="sxs-lookup"><span data-stu-id="8d37e-114">An item’s unit cost is the actual value of any receipt of the item, selected by the FIFO rule.</span></span><br /><br /> <span data-ttu-id="8d37e-115">I lagervärdering antas det att de första artiklarna in i lagret säljs först.</span><span class="sxs-lookup"><span data-stu-id="8d37e-115">In inventory valuation, it is assumed that the first items placed in inventory are sold first.</span></span> <span data-ttu-id="8d37e-116">**Obs!**  När priser stiger visar balansräkningen ett högre värde</span><span class="sxs-lookup"><span data-stu-id="8d37e-116">**Note:**  When prices are rising, the balance sheet shows greater value.</span></span> <span data-ttu-id="8d37e-117">Det betyder att skatteskuler ökar, men kreditpoängen och förmåga att låna kontant ökar.</span><span class="sxs-lookup"><span data-stu-id="8d37e-117">This means that tax liabilities increase, but credit scores and the ability to borrow cash improve.</span></span>|  
|<span data-ttu-id="8d37e-118">LIFO (Sist in, först ut)</span><span class="sxs-lookup"><span data-stu-id="8d37e-118">LIFO</span></span>|<span data-ttu-id="8d37e-119">Använd där lagernivåer är konsekvent underhållna eller ökar med tiden.</span><span class="sxs-lookup"><span data-stu-id="8d37e-119">Use where levels of inventories are consistently maintained or increased over time.</span></span>|<span data-ttu-id="8d37e-120">En artikels styckkostnad är det verkliga värdet på en mottagen artikel, vald enligt LIFO-regeln.</span><span class="sxs-lookup"><span data-stu-id="8d37e-120">An item’s unit cost is the actual value of any receipt of the item, selected by the LIFO rule.</span></span><br /><br /> <span data-ttu-id="8d37e-121">I lagervärdering antas det att de senaste artiklarna in i lagret säljs först.</span><span class="sxs-lookup"><span data-stu-id="8d37e-121">In inventory valuation, it is assumed that the last items placed in inventory are sold first.</span></span> <span data-ttu-id="8d37e-122">**Obs!**  När priser vill stiger, minskas värdet på resultaträkningen.</span><span class="sxs-lookup"><span data-stu-id="8d37e-122">**Note:**  When prices are rising, the value on the income statement decreases.</span></span> <span data-ttu-id="8d37e-123">Det betyder att skatteskuler minskar, men din förmåga att låna kontant försämras.</span><span class="sxs-lookup"><span data-stu-id="8d37e-123">This means that tax liabilities decrease, but the ability to borrow cash deteriorates.</span></span> <span data-ttu-id="8d37e-124">**Viktigt:**  Tillåts inte i många länderregioner, eftersom det kan användas för att dölja vinst.</span><span class="sxs-lookup"><span data-stu-id="8d37e-124">**Important:**  Disallowed in many countries/regions, as it can be used to depress profit.</span></span>|  
|<span data-ttu-id="8d37e-125">Genomsnitt</span><span class="sxs-lookup"><span data-stu-id="8d37e-125">Average</span></span>|<span data-ttu-id="8d37e-126">Använd där produktkostnaden inte är fast.</span><span class="sxs-lookup"><span data-stu-id="8d37e-126">Use where the product cost is unstable.</span></span><br /><br /> <span data-ttu-id="8d37e-127">Använd där lager travas eller blandas samman och inte kan åtskiljas, till exempel kemikalier.</span><span class="sxs-lookup"><span data-stu-id="8d37e-127">Use where inventories are piled or mixed together and cannot be differentiated, such as chemicals.</span></span>|<span data-ttu-id="8d37e-128">En artikels styckkostnad är den exakta kostnaden för mottagandet av den aktuella enheten.</span><span class="sxs-lookup"><span data-stu-id="8d37e-128">An item’s unit cost is the exact cost at which the particular unit was received.</span></span>|  
|<span data-ttu-id="8d37e-129">Specifik</span><span class="sxs-lookup"><span data-stu-id="8d37e-129">Specific</span></span>|<span data-ttu-id="8d37e-130">Använd i produktionen eller handel med enkelt härledas artiklar med i höga kostnadspris.</span><span class="sxs-lookup"><span data-stu-id="8d37e-130">Use in production or trade of easily identifiable items with fairly high unit costs.</span></span><br /><br /> <span data-ttu-id="8d37e-131">Använda för artiklar, som lyder under regler.</span><span class="sxs-lookup"><span data-stu-id="8d37e-131">Use for items that are subject to regulation.</span></span><br /><br /> <span data-ttu-id="8d37e-132">Använd för artiklar med serienummer.</span><span class="sxs-lookup"><span data-stu-id="8d37e-132">Use for items with serial numbers.</span></span>|<span data-ttu-id="8d37e-133">En artikels styckkostnad beräknas enligt den genomsnittliga styckkostnaden vid varje tidpunkt efter ett inköp.</span><span class="sxs-lookup"><span data-stu-id="8d37e-133">An item’s unit cost is calculated as the average unit cost at each point in time after a purchase.</span></span><br /><br /> <span data-ttu-id="8d37e-134">För lagervärdering förutsätts att alla lagerartiklar säljs samtidigt.</span><span class="sxs-lookup"><span data-stu-id="8d37e-134">For inventory valuation, it is assumes that all inventories are sold simultaneously.</span></span>|  
|<span data-ttu-id="8d37e-135">Standard</span><span class="sxs-lookup"><span data-stu-id="8d37e-135">Standard</span></span>|<span data-ttu-id="8d37e-136">Använd där kostnadskontroll är kritisk.</span><span class="sxs-lookup"><span data-stu-id="8d37e-136">Use where cost control is critical.</span></span><br /><br /> <span data-ttu-id="8d37e-137">Använd i upprepande produktion för att värdera kostnaderna för direkt material, direkt arbete och produktionsoverheadkostnad.</span><span class="sxs-lookup"><span data-stu-id="8d37e-137">Use in repetitive manufacturing, to value the costs of direct material, direct labor, and manufacturing overhead.</span></span><br /><br /> <span data-ttu-id="8d37e-138">Använd när det finns funktion och personal som underhåller standarder.</span><span class="sxs-lookup"><span data-stu-id="8d37e-138">Use where there is discipline and staff to maintain standards.</span></span>|<span data-ttu-id="8d37e-139">En artikels styckkostnad är förinställd baserad på uppskattning.</span><span class="sxs-lookup"><span data-stu-id="8d37e-139">An item’s unit cost is preset based on estimated.</span></span><br /><br /> <span data-ttu-id="8d37e-140">När den verkliga kostnaden senare realiseras, måste standardkostnaden justeras med den verkliga kostnaden via skillnadsvärden.</span><span class="sxs-lookup"><span data-stu-id="8d37e-140">When the actual cost is realized later, the standard cost must be adjusted to the actual cost through variance values.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="8d37e-141">Se även</span><span class="sxs-lookup"><span data-stu-id="8d37e-141">See Also</span></span>  
 <span data-ttu-id="8d37e-142">[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md) </span><span class="sxs-lookup"><span data-stu-id="8d37e-142">[Design Details: Costing Methods](design-details-costing-methods.md) </span></span>  
 <span data-ttu-id="8d37e-143">[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="8d37e-143">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
 [<span data-ttu-id="8d37e-144">Skapa komplexa moduler med hjälp av bästa metoder</span><span class="sxs-lookup"><span data-stu-id="8d37e-144">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="8d37e-145">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8d37e-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
