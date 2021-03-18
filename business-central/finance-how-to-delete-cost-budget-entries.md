---
title: Så här – Ta bort kostnadsbudgettransaktioner | Microsoft Docs
description: Du använder batch-jobbet Ta bort kostnadsbudgettransaktioner för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b4c81aa62f3548819db3451130c49fd11984b33a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387380"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="b7b80-103">Ta bort kostnadsbudgettransaktioner</span><span class="sxs-lookup"><span data-stu-id="b7b80-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="b7b80-104">Du använder batch-jobbet **Ta bort kostnadsbudgettransaktioner** för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen.</span><span class="sxs-lookup"><span data-stu-id="b7b80-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="b7b80-105">För att förhindra luckor i kostnadsbudgettransaktionerna och kostnadsjournalstransaktionerna kan du inte ta bort en enstaka post eller en gruppera poster i mitten av listan över registerposter.</span><span class="sxs-lookup"><span data-stu-id="b7b80-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="b7b80-106">Ta bort kostnadsbudgettransaktioner</span><span class="sxs-lookup"><span data-stu-id="b7b80-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="b7b80-107">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Ta bort kostnadsbudgettransaktioner** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b7b80-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="b7b80-108">**Till journalnr**</span><span class="sxs-lookup"><span data-stu-id="b7b80-108">The **To Register No.**</span></span> <span data-ttu-id="b7b80-109">-fältet innehåller det sista registerpostnumret och kan inte ändras.</span><span class="sxs-lookup"><span data-stu-id="b7b80-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="b7b80-110">Använd fältet **från att registrera nr**</span><span class="sxs-lookup"><span data-stu-id="b7b80-110">You can use the **From Register No.**</span></span> <span data-ttu-id="b7b80-111">för att välja ett registerpostnummer från vilket borttagningen ska börja.</span><span class="sxs-lookup"><span data-stu-id="b7b80-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="b7b80-112">Välj **OK** för att ta bort de valda kostnadsbudgettransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="b7b80-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b7b80-113">För att undvika ofrivillig borttagning av kostnadsbudgettransaktioner kan du stänga registerposter genom att markera raderna som **Avslutade** i fältet **Avslutat** på sidan **Kostnadsbudgetregister**.</span><span class="sxs-lookup"><span data-stu-id="b7b80-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b7b80-114">Se även</span><span class="sxs-lookup"><span data-stu-id="b7b80-114">See Also</span></span>  
<span data-ttu-id="b7b80-115">[Redovisa kostnader](finance-manage-cost-accounting.md)
[Skapa kostnadsbudgetar](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="b7b80-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="b7b80-116">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b7b80-116">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]