---
title: Så här ställer du in automatiska kontobokföringsmallar
description: Om du vill använda automatiska kontokoder måste du skapa en automatisk kontobokföringsmall.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2822ffb9fab32501b0766eaa51a36d3a31d1bb6c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "925596"
---
# <a name="set-up-automatic-account-posting-groups"></a><span data-ttu-id="92094-103">Ställ in automatiska kontobokföringsmallar</span><span class="sxs-lookup"><span data-stu-id="92094-103">Set Up Automatic Account Posting Groups</span></span>
<span data-ttu-id="92094-104">Om du vill använda automatiska kontokoder måste du skapa en automatisk kontobokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="92094-104">To use automatic account codes, you must create an automatic account posting group.</span></span>  

## <a name="to-set-up-automatic-account-posting-groups"></a><span data-ttu-id="92094-105">Så här ställer du in automatiska kontobokföringsmallar</span><span class="sxs-lookup"><span data-stu-id="92094-105">To set up automatic account posting groups</span></span>  

1.  <span data-ttu-id="92094-106">Välj ikonen ![Söka efter sida eller rapport](../../media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Automatkontering** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="92094-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Auto. Acc. Groups**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="92094-107">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="92094-107">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="92094-108">Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Allmänt**.</span><span class="sxs-lookup"><span data-stu-id="92094-108">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="92094-109">Fält</span><span class="sxs-lookup"><span data-stu-id="92094-109">Field</span></span>|<span data-ttu-id="92094-110">Description</span><span class="sxs-lookup"><span data-stu-id="92094-110">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="92094-111">**Nr**</span><span class="sxs-lookup"><span data-stu-id="92094-111">**No.**</span></span>|<span data-ttu-id="92094-112">Ange ett unikt alfanumeriskt nummer för den automatiska kontobokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="92094-112">Enter a unique alphanumeric number for the automatic account posting group.</span></span>|  
    |<span data-ttu-id="92094-113">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="92094-113">**Description**</span></span>|<span data-ttu-id="92094-114">Ange en beskrivning av den automatiska kontobokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="92094-114">Enter a description for the automatic account posting group.</span></span>|  

4.  <span data-ttu-id="92094-115">Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Automatkonteringsrad**.</span><span class="sxs-lookup"><span data-stu-id="92094-115">On the **Automatic Acc. Line** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="92094-116">Fält</span><span class="sxs-lookup"><span data-stu-id="92094-116">Field</span></span>|<span data-ttu-id="92094-117">Description</span><span class="sxs-lookup"><span data-stu-id="92094-117">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="92094-118">**Allokeringsprocent**</span><span class="sxs-lookup"><span data-stu-id="92094-118">**Allocation Percentage**</span></span>|<span data-ttu-id="92094-119">Ange procentandelen av ursprungsradbeloppet som ska fördelas.</span><span class="sxs-lookup"><span data-stu-id="92094-119">Enter the percentage of the source line amount that is to be allocated.</span></span>|  
    |<span data-ttu-id="92094-120">**Redovisningskontonr**</span><span class="sxs-lookup"><span data-stu-id="92094-120">**G/L Account No.**</span></span>|<span data-ttu-id="92094-121">Ange numret på redovisningskontot som fördelningen ska bokföras på.</span><span class="sxs-lookup"><span data-stu-id="92094-121">Enter the general ledger account number to which the allocation should be posted.</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="92094-122">I fältet **Totalt saldo** summeras fältet **Allokeringsprocent** för de automatiska kontoraderna i en bokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="92094-122">The **Total Balance** field totals the **Allocation Percentage** field for automatic account lines in a posting group.</span></span> <span data-ttu-id="92094-123">Om den totala fördelningsprocenten för en bokföringsmall inte blir noll visas ett felmeddelande när posten bokförs.</span><span class="sxs-lookup"><span data-stu-id="92094-123">If the total allocation percent for a posting group does not balance to zero, an error message will be displayed when the item is posted.</span></span>  

5.  <span data-ttu-id="92094-124">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="92094-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="92094-125">Se även</span><span class="sxs-lookup"><span data-stu-id="92094-125">See Also</span></span>  
 <span data-ttu-id="92094-126">[Automatiska kontokoder](automatic-account-codes.md) </span><span class="sxs-lookup"><span data-stu-id="92094-126">[Automatic Account Codes](automatic-account-codes.md) </span></span>  
 [<span data-ttu-id="92094-127">Ställa in bokföringsmallar</span><span class="sxs-lookup"><span data-stu-id="92094-127">Setting Up Posting Groups</span></span>](../../finance-posting-groups.md)  
 [<span data-ttu-id="92094-128">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="92094-128">Working with General Journals</span></span>](../../ui-work-general-journals.md)
