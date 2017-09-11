---
title: "Ångra en redovisningsjournal genom att bokföra en mottransaktion | Microsoft Docs"
description: "Om du har bokfört en felaktig bokföring i den allmänna journalen, kan du använda funktionen Återför transaktion för att ångra bokföringen med ett korrekt redovisningsspårning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-reverse-journal-posting"></a><span data-ttu-id="9a055-103">Så här: Återföra en journalbokning</span><span class="sxs-lookup"><span data-stu-id="9a055-103">How to: Reverse Journal Posting</span></span>
<span data-ttu-id="9a055-104">För att kunna återföra (ångra) en felaktig bokföring markerar du posten och skapar en korrigeringspost (transaktioner som är identiska med den ursprungliga transaktionen, men har ett motsatt tecken i beloppsfältet) med samma dokumentnummer och bokföringsdatum som den ursprungliga posten automatiskt.</span><span class="sxs-lookup"><span data-stu-id="9a055-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="9a055-105">När du har återfört en post måste du skapa en korrekt post.</span><span class="sxs-lookup"><span data-stu-id="9a055-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="9a055-106">Du kan endast återföra poster som har bokförts från en redovisningsjournalrad.</span><span class="sxs-lookup"><span data-stu-id="9a055-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="9a055-107">En transaktion kan endast återföras en gång.</span><span class="sxs-lookup"><span data-stu-id="9a055-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="9a055-108">Läs mer om hur du bokför från en redovisningsjournal, [så här: bokföra transaktioner direkt till redovisningsmodulen ](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="9a055-108">For more information about posting from a general journal, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="9a055-109">Du kan återföra poster från alla fönster **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="9a055-109">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="9a055-110">Följande procedur baseras fönstret **redovisningstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="9a055-110">The following procedure is based on the **General Ledger Entries** window.</span></span>

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="9a055-111">Att återföra bokföringen av en redovisningstransaktion journal</span><span class="sxs-lookup"><span data-stu-id="9a055-111">To reverse the journal posting of a general ledger entry</span></span>
1. <span data-ttu-id="9a055-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningstransaktioner** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9a055-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="9a055-113">Markera den transaktion som du vill återföra och välj sedan åtgärden **återföringstransaktion**.</span><span class="sxs-lookup"><span data-stu-id="9a055-113">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="9a055-114">Observera att det måste komma från en journalbokföring.</span><span class="sxs-lookup"><span data-stu-id="9a055-114">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="9a055-115">I fönstret **Återför transaktionsposter** väljer du önskad post och klickar på åtgärden **Återför**.</span><span class="sxs-lookup"><span data-stu-id="9a055-115">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="9a055-116">Välj knappen **Ja** på bekräftelsemeddelandet.</span><span class="sxs-lookup"><span data-stu-id="9a055-116">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a055-117">Se även</span><span class="sxs-lookup"><span data-stu-id="9a055-117">See Also</span></span>
[<span data-ttu-id="9a055-118">Så här bokför du transaktioner direkt i redovisningen</span><span class="sxs-lookup"><span data-stu-id="9a055-118">How to: Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="9a055-119">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="9a055-119">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="9a055-120">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="9a055-120">Finance</span></span>](finance.md)  
<span data-ttu-id="9a055-121">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9a055-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

