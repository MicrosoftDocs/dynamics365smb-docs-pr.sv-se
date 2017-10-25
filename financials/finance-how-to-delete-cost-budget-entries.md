---
title: "Så här - Ta bort kostnadsbudgettransaktioner | Microsoft Docs"
description: "Du använder batch-jobbet **Ta bort kostnadsbudgettransaktioner** för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen."
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
ms.openlocfilehash: 79c9a58c7cb91ce922b81eec1d2ccad375943203
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-delete-cost-budget-entries"></a><span data-ttu-id="1427e-103">Så här: Ta bort kostnadsbudgettransaktioner</span><span class="sxs-lookup"><span data-stu-id="1427e-103">How to: Delete Cost Budget Entries</span></span>
<span data-ttu-id="1427e-104">Du använder batch-jobbet **Ta bort kostnadsbudgettransaktioner** för att rätta kostnadsbudgettransaktioner i kostnadsbudgetjournalen.</span><span class="sxs-lookup"><span data-stu-id="1427e-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="1427e-105">För att förhindra luckor i kostnadsbudgettransaktionerna och kostnadsjournalstransaktionerna kan du inte ta bort en enstaka post eller en gruppera poster i mitten av listan över registerposter.</span><span class="sxs-lookup"><span data-stu-id="1427e-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="1427e-106">Ta bort kostnadsbudgettransaktioner</span><span class="sxs-lookup"><span data-stu-id="1427e-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="1427e-107">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Ta bort kostnadsbudgettransaktioner** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1427e-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="1427e-108">**Till journalnr**</span><span class="sxs-lookup"><span data-stu-id="1427e-108">The **To Register No.**</span></span> <span data-ttu-id="1427e-109">-fältet innehåller det sista registerpostnumret och kan inte ändras.</span><span class="sxs-lookup"><span data-stu-id="1427e-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="1427e-110">Använd fältet **från att registrera nr**</span><span class="sxs-lookup"><span data-stu-id="1427e-110">You can use the **From Register No.**</span></span> <span data-ttu-id="1427e-111">för att välja ett registerpostnummer från vilket borttagningen ska börja.</span><span class="sxs-lookup"><span data-stu-id="1427e-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="1427e-112">Välj **OK** för att ta bort de valda kostnadsbudgettransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="1427e-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1427e-113">För att undvika ofrivillig borttagning av kostnadsbudgettransaktioner kan du stänga registerposter genom att markera raderna som **Avslutade** i fältet **Avslutat**  i fönstret **Kostnadsbudgetregister**.</span><span class="sxs-lookup"><span data-stu-id="1427e-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field in the **Cost Budget Registers** window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1427e-114">Se även</span><span class="sxs-lookup"><span data-stu-id="1427e-114">See Also</span></span>  
<span data-ttu-id="1427e-115">[Redovisa kostnader](finance-manage-cost-accounting.md)
[Skapa kostnadsbudgetar](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="1427e-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="1427e-116">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1427e-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

