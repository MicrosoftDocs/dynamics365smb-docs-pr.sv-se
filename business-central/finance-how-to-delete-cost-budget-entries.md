---
title: "Så här - Ta bort kostnadsbudgettransaktioner | Microsoft Docs"
description: "Du använder batch-jobbet Ta bort kostnadsbudgettransaktioner för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: 7a5647bcb5a58cdf0a38ec037994d6cbe7a9504d
ms.contentlocale: sv-se
ms.lasthandoff: 11/29/2018

---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="892b0-103">Ta bort kostnadsbudgettransaktioner</span><span class="sxs-lookup"><span data-stu-id="892b0-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="892b0-104">Du använder batch-jobbet **Ta bort kostnadsbudgettransaktioner** för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen.</span><span class="sxs-lookup"><span data-stu-id="892b0-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="892b0-105">För att förhindra luckor i kostnadsbudgettransaktionerna och kostnadsjournalstransaktionerna kan du inte ta bort en enstaka post eller en gruppera poster i mitten av listan över registerposter.</span><span class="sxs-lookup"><span data-stu-id="892b0-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="892b0-106">Ta bort kostnadsbudgettransaktioner</span><span class="sxs-lookup"><span data-stu-id="892b0-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="892b0-107">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Ta bort kostnadsbudgettransaktioner** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="892b0-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="892b0-108">**Till journalnr**</span><span class="sxs-lookup"><span data-stu-id="892b0-108">The **To Register No.**</span></span> <span data-ttu-id="892b0-109">-fältet innehåller det sista registerpostnumret och kan inte ändras.</span><span class="sxs-lookup"><span data-stu-id="892b0-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="892b0-110">Använd fältet **från att registrera nr**</span><span class="sxs-lookup"><span data-stu-id="892b0-110">You can use the **From Register No.**</span></span> <span data-ttu-id="892b0-111">för att välja ett registerpostnummer från vilket borttagningen ska börja.</span><span class="sxs-lookup"><span data-stu-id="892b0-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="892b0-112">Välj **OK** för att ta bort de valda kostnadsbudgettransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="892b0-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="892b0-113">För att undvika ofrivillig borttagning av kostnadsbudgettransaktioner kan du stänga registerposter genom att markera raderna som **Avslutade** i fältet **Avslutat** på sidan **Kostnadsbudgetregister**.</span><span class="sxs-lookup"><span data-stu-id="892b0-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="892b0-114">Se även</span><span class="sxs-lookup"><span data-stu-id="892b0-114">See Also</span></span>  
<span data-ttu-id="892b0-115">[Redovisa kostnader](finance-manage-cost-accounting.md)
[Skapa kostnadsbudgetar](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="892b0-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="892b0-116">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="892b0-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

