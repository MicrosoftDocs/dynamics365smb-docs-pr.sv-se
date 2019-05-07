---
title: Skapa underhållnning för anläggningstillgångar | Microsoft Docs
description: Om du vill hantera anläggningstillgångars reparationer och service, kan du ange allmän underhållsinformation, koder för typen av arbete och ett bokföringskonto för kostnader.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ba01ccb88349a1f1943655949a36e2a21f3ae2de
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "913901"
---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="bd769-103">Skapa underhåll för anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="bd769-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="bd769-104">Om du vill hantera underhåll av anläggningstillgångar måste du först ange viss allmän underhållsinformation, ett bokföringskonto för underhållskostnader och underhållskoder för olika typer av arbete, till exempel rutintjänst eller reparation.</span><span class="sxs-lookup"><span data-stu-id="bd769-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="bd769-105">Så här ställer du in allmän underhållsinformation</span><span class="sxs-lookup"><span data-stu-id="bd769-105">To set up general maintenance information</span></span>
<span data-ttu-id="bd769-106">Om du skapar fält för underhåll kan du bokföra underhållskostnader från anläggningstillgångsjournalen.</span><span class="sxs-lookup"><span data-stu-id="bd769-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="bd769-107">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anläggningstillgångar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bd769-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="bd769-108">Markera den fasta anläggningstillgång som du definierar täckning av försäkring för välj sedan åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="bd769-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="bd769-109">Fyll i så många fält som behövs på snabbfliken **Underhåll**.</span><span class="sxs-lookup"><span data-stu-id="bd769-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="bd769-110">Så här skapar du underhållskoder</span><span class="sxs-lookup"><span data-stu-id="bd769-110">To set up maintenance codes</span></span>
<span data-ttu-id="bd769-111">När du bokför underhållskostnader (från en redovisningsjournal eller en inköpsfaktura) fyller du i fältet **Underhållskod** för att ange vilken typ av underhåll som har utförts, t.ex. rutinservice eller reparation.</span><span class="sxs-lookup"><span data-stu-id="bd769-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="bd769-112">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Underhåll** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bd769-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="bd769-113">Lägg upp koder för andra typer av underhållsarbete på sidan **Underhåll**.</span><span class="sxs-lookup"><span data-stu-id="bd769-113">On the **Maintenance** page, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="bd769-114">Så här skapar du underhållskostnader</span><span class="sxs-lookup"><span data-stu-id="bd769-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="bd769-115">Om du vill bokföra underhållskostnader måste du först ange ett kontonummer på sidan **Anl. bokföringsmallar**.</span><span class="sxs-lookup"><span data-stu-id="bd769-115">To post maintenance costs, you must first enter an account number on the **FA Posting Groups** page.</span></span>

1. <span data-ttu-id="bd769-116">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anl. bokföringsmallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bd769-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="bd769-117">Fyll i fältet **Underhållskostnader** för varje bokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="bd769-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="bd769-118">Om du vill att underhållskostnaderna ska fördelas på avdelningar och/eller projekt måste du skapa en fördelningsnyckel</span><span class="sxs-lookup"><span data-stu-id="bd769-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="bd769-119">Mer information finns i [Konfigurera allmänna funktioner för anläggningstillgångar](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="bd769-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bd769-120">Se även</span><span class="sxs-lookup"><span data-stu-id="bd769-120">See Also</span></span>
[<span data-ttu-id="bd769-121">Ställa in anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="bd769-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="bd769-122">Anläggningstillgångar</span><span class="sxs-lookup"><span data-stu-id="bd769-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="bd769-123">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="bd769-123">Finance</span></span>](finance.md)  
[<span data-ttu-id="bd769-124">Komma igång</span><span class="sxs-lookup"><span data-stu-id="bd769-124">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="bd769-125">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bd769-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
