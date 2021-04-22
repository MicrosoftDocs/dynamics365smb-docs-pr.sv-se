---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 212f0d228cd2a95990d8144abd8bc8f2e4894a80
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776567"
---
<span data-ttu-id="7f2e1-101">Om du vill använda automatiska kontokoder måste du skapa en automatisk kontobokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-101">To use automatic account codes, you must create an automatic account posting group.</span></span>  

## <a name="to-set-up-automatic-account-posting-groups"></a><span data-ttu-id="7f2e1-102">Så här ställer du in automatiska kontobokföringsmallar</span><span class="sxs-lookup"><span data-stu-id="7f2e1-102">To set up automatic account posting groups</span></span>  

1. <span data-ttu-id="7f2e1-103">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](../../../media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Automatkontering** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-103">Choose the ![Lightbulb that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Auto. Acc. Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7f2e1-104">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-104">Choose the **New** action.</span></span>  
3. <span data-ttu-id="7f2e1-105">Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Allmänt**.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-105">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="7f2e1-106">Fält</span><span class="sxs-lookup"><span data-stu-id="7f2e1-106">Field</span></span>|<span data-ttu-id="7f2e1-107">Description</span><span class="sxs-lookup"><span data-stu-id="7f2e1-107">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="7f2e1-108">**Nr**</span><span class="sxs-lookup"><span data-stu-id="7f2e1-108">**No.**</span></span>|<span data-ttu-id="7f2e1-109">Ange ett unikt alfanumeriskt nummer för den automatiska kontobokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-109">Enter a unique alphanumeric number for the automatic account posting group.</span></span>|  
    |<span data-ttu-id="7f2e1-110">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="7f2e1-110">**Description**</span></span>|<span data-ttu-id="7f2e1-111">Ange en beskrivning av den automatiska kontobokföringsmallen.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-111">Enter a description for the automatic account posting group.</span></span>|  

4. <span data-ttu-id="7f2e1-112">Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Automatkonteringsrad**.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-112">On the **Automatic Acc. Line** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="7f2e1-113">Fält</span><span class="sxs-lookup"><span data-stu-id="7f2e1-113">Field</span></span>|<span data-ttu-id="7f2e1-114">Description</span><span class="sxs-lookup"><span data-stu-id="7f2e1-114">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="7f2e1-115">**Allokeringsprocent**</span><span class="sxs-lookup"><span data-stu-id="7f2e1-115">**Allocation Percentage**</span></span>|<span data-ttu-id="7f2e1-116">Ange procentandelen av ursprungsradbeloppet som ska fördelas.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-116">Enter the percentage of the source line amount that is to be allocated.</span></span>|  
    |<span data-ttu-id="7f2e1-117">**Redovisningskontonr**</span><span class="sxs-lookup"><span data-stu-id="7f2e1-117">**G/L Account No.**</span></span>|<span data-ttu-id="7f2e1-118">Ange numret på redovisningskontot som fördelningen ska bokföras på.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-118">Enter the general ledger account number to which the allocation should be posted.</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="7f2e1-119">I fältet **Totalt saldo** summeras fältet **Allokeringsprocent** för de automatiska kontoraderna i en bokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-119">The **Total Balance** field totals the **Allocation Percentage** field for automatic account lines in a posting group.</span></span> <span data-ttu-id="7f2e1-120">Om den totala fördelningsprocenten för en bokföringsmall inte blir noll visas ett felmeddelande när posten bokförs.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-120">If the total allocation percent for a posting group does not balance to zero, an error message will be displayed when the item is posted.</span></span>  

5. <span data-ttu-id="7f2e1-121">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f2e1-121">Choose the **OK** button.</span></span>  
