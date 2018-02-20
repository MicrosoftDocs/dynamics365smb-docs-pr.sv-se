---
title: "Skapa underhållnning för anläggningstillgångar | Microsoft Docs"
description: "Om du vill hantera anläggningstillgångars reparationer och service, kan du ange allmän underhållsinformation, koder för typen av arbete och ett bokföringskonto för kostnader."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7ae4abacf22d3610194ea56bbaa997390cb7df0a
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="3bc91-103">Skapa underhåll för anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="3bc91-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="3bc91-104">Om du vill hantera underhåll av anläggningstillgångar måste du först ange viss allmän underhållsinformation, ett bokföringskonto för underhållskostnader och underhållskoder för olika typer av arbete, till exempel rutintjänst eller reparation.</span><span class="sxs-lookup"><span data-stu-id="3bc91-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="3bc91-105">Så här ställer du in allmän underhållsinformation</span><span class="sxs-lookup"><span data-stu-id="3bc91-105">To set up general maintenance information</span></span>
<span data-ttu-id="3bc91-106">Om du skapar fält för underhåll kan du bokföra underhållskostnader från anläggningstillgångsjournalen.</span><span class="sxs-lookup"><span data-stu-id="3bc91-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="3bc91-107">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anläggningstillgångar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3bc91-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="3bc91-108">Markera den fasta anläggningstillgång som du definierar täckning av försäkring för välj sedan åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="3bc91-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="3bc91-109">Fyll i så många fält som behövs på snabbfliken **Underhåll**.</span><span class="sxs-lookup"><span data-stu-id="3bc91-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="3bc91-110">Så här skapar du underhållskoder</span><span class="sxs-lookup"><span data-stu-id="3bc91-110">To set up maintenance codes</span></span>
<span data-ttu-id="3bc91-111">När du bokför underhållskostnader (från en redovisningsjournal eller en inköpsfaktura) fyller du i fältet **Underhållskod** för att ange vilken typ av underhåll som har utförts, t.ex. rutinservice eller reparation.</span><span class="sxs-lookup"><span data-stu-id="3bc91-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="3bc91-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Underhåll** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3bc91-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="3bc91-113">Lägg upp koder för andra typer av underhållsarbete i fönstret **Underhåll**.</span><span class="sxs-lookup"><span data-stu-id="3bc91-113">In the **Maintenance** window, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="3bc91-114">Så här skapar du underhållskostnader</span><span class="sxs-lookup"><span data-stu-id="3bc91-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="3bc91-115">Om du vill bokföra underhållskostnader måste du först ange ett kontonummer i fönstret **Anl. bokföringsmallar**.</span><span class="sxs-lookup"><span data-stu-id="3bc91-115">To post maintenance costs, you must first enter an account number in the **FA Posting Groups** window.</span></span>

1. <span data-ttu-id="3bc91-116">Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Anl. bokföringsmallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3bc91-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="3bc91-117">Fyll i fältet **Underhållskostnader** för varje bokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="3bc91-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3bc91-118">Om du vill att underhållskostnaderna ska fördelas på avdelningar och/eller projekt måste du skapa en fördelningsnyckel</span><span class="sxs-lookup"><span data-stu-id="3bc91-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="3bc91-119">Mer information finns i [Konfigurera allmänna funktioner för anläggningstillgångar](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="3bc91-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3bc91-120">Se även</span><span class="sxs-lookup"><span data-stu-id="3bc91-120">See Also</span></span>
[<span data-ttu-id="3bc91-121">Ställa in anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="3bc91-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="3bc91-122">Anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="3bc91-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="3bc91-123">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="3bc91-123">Finance</span></span>](finance.md)  
<span data-ttu-id="3bc91-124">[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="3bc91-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="3bc91-125">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3bc91-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

