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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e75274a4fd42bb379f99a94c27c6fb21e25bc836
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301075"
---
# <a name="set-up-automatic-account-posting-groups"></a><span data-ttu-id="f24f2-103">Ställ in automatiska kontobokföringsmallar</span><span class="sxs-lookup"><span data-stu-id="f24f2-103">Set Up Automatic Account Posting Groups</span></span>
<span data-ttu-id="f24f2-104">Om du vill använda automatiska kontokoder måste du skapa en automatisk kontobokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="f24f2-104">To use automatic account codes, you must create an automatic account posting group.</span></span>  

## <a name="to-set-up-automatic-account-posting-groups"></a><span data-ttu-id="f24f2-105">Så här ställer du in automatiska kontobokföringsmallar</span><span class="sxs-lookup"><span data-stu-id="f24f2-105">To set up automatic account posting groups</span></span>  

1.  <span data-ttu-id="f24f2-106">Välj ikonen ![Söka efter sida eller rapport](../../media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Automatkontering** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="f24f2-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Auto. Acc. Groups**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f24f2-107">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-107">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="f24f2-108">Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Allmänt**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-108">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f24f2-109">Fält</span><span class="sxs-lookup"><span data-stu-id="f24f2-109">Field</span></span>|<span data-ttu-id="f24f2-110">Description</span><span class="sxs-lookup"><span data-stu-id="f24f2-110">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="f24f2-111">**Nr**</span><span class="sxs-lookup"><span data-stu-id="f24f2-111">**No.**</span></span>|<span data-ttu-id="f24f2-112">Ange ett unikt alfanumeriskt nummer för den automatiska kontobokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="f24f2-112">Enter a unique alphanumeric number for the automatic account posting group.</span></span>|  
    |<span data-ttu-id="f24f2-113">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="f24f2-113">**Description**</span></span>|<span data-ttu-id="f24f2-114">Ange en beskrivning av den automatiska kontobokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="f24f2-114">Enter a description for the automatic account posting group.</span></span>|  

4.  <span data-ttu-id="f24f2-115">Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Automatkonteringsrad**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-115">On the **Automatic Acc. Line** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f24f2-116">Fält</span><span class="sxs-lookup"><span data-stu-id="f24f2-116">Field</span></span>|<span data-ttu-id="f24f2-117">Description</span><span class="sxs-lookup"><span data-stu-id="f24f2-117">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="f24f2-118">**Allokeringsprocent**</span><span class="sxs-lookup"><span data-stu-id="f24f2-118">**Allocation Percentage**</span></span>|<span data-ttu-id="f24f2-119">Ange procentandelen av ursprungsradbeloppet som ska fördelas.</span><span class="sxs-lookup"><span data-stu-id="f24f2-119">Enter the percentage of the source line amount that is to be allocated.</span></span>|  
    |<span data-ttu-id="f24f2-120">**Redovisningskontonr**</span><span class="sxs-lookup"><span data-stu-id="f24f2-120">**G/L Account No.**</span></span>|<span data-ttu-id="f24f2-121">Ange numret på redovisningskontot som fördelningen ska bokföras på.</span><span class="sxs-lookup"><span data-stu-id="f24f2-121">Enter the general ledger account number to which the allocation should be posted.</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="f24f2-122">I fältet **Totalt saldo** summeras fältet **Allokeringsprocent** för de automatiska kontoraderna i en bokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="f24f2-122">The **Total Balance** field totals the **Allocation Percentage** field for automatic account lines in a posting group.</span></span> <span data-ttu-id="f24f2-123">Om den totala fördelningsprocenten för en bokföringsmall inte blir noll visas ett felmeddelande när posten bokförs.</span><span class="sxs-lookup"><span data-stu-id="f24f2-123">If the total allocation percent for a posting group does not balance to zero, an error message will be displayed when the item is posted.</span></span>  

5.  <span data-ttu-id="f24f2-124">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f24f2-125">Se även</span><span class="sxs-lookup"><span data-stu-id="f24f2-125">See Also</span></span>  
 <span data-ttu-id="f24f2-126">[Automatiska kontokoder](automatic-account-codes.md) </span><span class="sxs-lookup"><span data-stu-id="f24f2-126">[Automatic Account Codes](automatic-account-codes.md) </span></span>  
 [<span data-ttu-id="f24f2-127">Ställa in bokföringsmallar</span><span class="sxs-lookup"><span data-stu-id="f24f2-127">Setting Up Posting Groups</span></span>](../../finance-posting-groups.md)  
 [<span data-ttu-id="f24f2-128">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="f24f2-128">Working with General Journals</span></span>](../../ui-work-general-journals.md)
