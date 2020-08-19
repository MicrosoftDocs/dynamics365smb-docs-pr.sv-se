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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 8218f35bfbbd4c1ff56d86c55598127b0ecd1fec
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676748"
---
# <a name="set-up-automatic-account-posting-groups"></a><span data-ttu-id="5c22c-103">Ställ in automatiska kontobokföringsmallar</span><span class="sxs-lookup"><span data-stu-id="5c22c-103">Set Up Automatic Account Posting Groups</span></span>
<span data-ttu-id="5c22c-104">Om du vill använda automatiska kontokoder måste du skapa en automatisk kontobokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="5c22c-104">To use automatic account codes, you must create an automatic account posting group.</span></span>  

## <a name="to-set-up-automatic-account-posting-groups"></a><span data-ttu-id="5c22c-105">Så här ställer du in automatiska kontobokföringsmallar</span><span class="sxs-lookup"><span data-stu-id="5c22c-105">To set up automatic account posting groups</span></span>  

1.  <span data-ttu-id="5c22c-106">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](../../media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Automatkontering** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="5c22c-106">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Auto. Acc. Groups**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5c22c-107">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5c22c-107">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="5c22c-108">Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Allmänt**.</span><span class="sxs-lookup"><span data-stu-id="5c22c-108">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="5c22c-109">Fält</span><span class="sxs-lookup"><span data-stu-id="5c22c-109">Field</span></span>|<span data-ttu-id="5c22c-110">Description</span><span class="sxs-lookup"><span data-stu-id="5c22c-110">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="5c22c-111">**Nr**</span><span class="sxs-lookup"><span data-stu-id="5c22c-111">**No.**</span></span>|<span data-ttu-id="5c22c-112">Ange ett unikt alfanumeriskt nummer för den automatiska kontobokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="5c22c-112">Enter a unique alphanumeric number for the automatic account posting group.</span></span>|  
    |<span data-ttu-id="5c22c-113">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="5c22c-113">**Description**</span></span>|<span data-ttu-id="5c22c-114">Ange en beskrivning av den automatiska kontobokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="5c22c-114">Enter a description for the automatic account posting group.</span></span>|  

4.  <span data-ttu-id="5c22c-115">Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Automatkonteringsrad**.</span><span class="sxs-lookup"><span data-stu-id="5c22c-115">On the **Automatic Acc. Line** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="5c22c-116">Fält</span><span class="sxs-lookup"><span data-stu-id="5c22c-116">Field</span></span>|<span data-ttu-id="5c22c-117">Description</span><span class="sxs-lookup"><span data-stu-id="5c22c-117">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="5c22c-118">**Allokeringsprocent**</span><span class="sxs-lookup"><span data-stu-id="5c22c-118">**Allocation Percentage**</span></span>|<span data-ttu-id="5c22c-119">Ange procentandelen av ursprungsradbeloppet som ska fördelas.</span><span class="sxs-lookup"><span data-stu-id="5c22c-119">Enter the percentage of the source line amount that is to be allocated.</span></span>|  
    |<span data-ttu-id="5c22c-120">**Redovisningskontonr**</span><span class="sxs-lookup"><span data-stu-id="5c22c-120">**G/L Account No.**</span></span>|<span data-ttu-id="5c22c-121">Ange numret på redovisningskontot som fördelningen ska bokföras på.</span><span class="sxs-lookup"><span data-stu-id="5c22c-121">Enter the general ledger account number to which the allocation should be posted.</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="5c22c-122">I fältet **Totalt saldo** summeras fältet **Allokeringsprocent** för de automatiska kontoraderna i en bokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="5c22c-122">The **Total Balance** field totals the **Allocation Percentage** field for automatic account lines in a posting group.</span></span> <span data-ttu-id="5c22c-123">Om den totala fördelningsprocenten för en bokföringsmall inte blir noll visas ett felmeddelande när posten bokförs.</span><span class="sxs-lookup"><span data-stu-id="5c22c-123">If the total allocation percent for a posting group does not balance to zero, an error message will be displayed when the item is posted.</span></span>  

5.  <span data-ttu-id="5c22c-124">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c22c-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5c22c-125">Se även</span><span class="sxs-lookup"><span data-stu-id="5c22c-125">See Also</span></span>  
 <span data-ttu-id="5c22c-126">[Automatiska kontokoder](automatic-account-codes.md) </span><span class="sxs-lookup"><span data-stu-id="5c22c-126">[Automatic Account Codes](automatic-account-codes.md) </span></span>  
 [<span data-ttu-id="5c22c-127">Ställa in bokföringsmallar</span><span class="sxs-lookup"><span data-stu-id="5c22c-127">Setting Up Posting Groups</span></span>](../../finance-posting-groups.md)  
 [<span data-ttu-id="5c22c-128">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="5c22c-128">Working with General Journals</span></span>](../../ui-work-general-journals.md)
