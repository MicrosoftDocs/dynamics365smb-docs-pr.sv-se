---
title: Importera lönetransaktioner | Microsoft Docs
description: Om du vill hantera lön, importera och bokföra ekonomiska transaktioner från leverantören lön i redovisningen med hjälp av filtillägget lön, till exempel Ceridian eller Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 3e8260d747f692a44b09a537aa17cdbf0de83fff
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782649"
---
# <a name="import-payroll-transactions"></a><span data-ttu-id="a2ab3-103">Importera lönetransaktioner</span><span class="sxs-lookup"><span data-stu-id="a2ab3-103">Import Payroll Transactions</span></span>
<span data-ttu-id="a2ab3-104">För att ta hänsyn till lönutbetalningar och relaterade transaktioner måste du importera och bokföra finansiella transaktioner som gjorts av ditt lönesystem i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="a2ab3-105">För att göra detta måste du först importera en fil som du får från lönelistleverantören till sidan **Redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="a2ab3-106">Sedan mappar du de externa kontona i lönefilen till det relevanta redovisningskontot.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="a2ab3-107">Slutligen bokför du lönetransaktioner enligt kontomappningen.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="a2ab3-108">Om du vill använda denna funktion måste ett tillägg för lönelisteimport ha installerats och aktiverats.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="a2ab3-109">Tilläggen Ceridian lön och importera Quickbooks lön är förinstallerade i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a2ab3-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a2ab3-110">Mer information finns i [Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a2ab3-110">For more information, see [Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="a2ab3-111">Att importera en lönefil</span><span class="sxs-lookup"><span data-stu-id="a2ab3-111">To import a payroll file</span></span>
1. <span data-ttu-id="a2ab3-112">Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="a2ab3-113">I relevant redovisningsjournal väljer du åtgärden **Importera lönetransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="a2ab3-114">En assisterad inställningsguide öppnas.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="a2ab3-115">Följ anvisningarna på sidan **Importera lönetransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-115">Follow the steps on the **Import Payroll Transactions** page.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="a2ab3-116">I steget som berör mappning av externa löneposter till dina redovisningskonton kommer mappningarna som du skapar att sparas till nästa gång samma poster importeras.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="a2ab3-117">Detta sparar tid samtidigt som du inte behöver fylla i fältet **Kontonr** manuellt i redovisningsjournalen när du har importerat återkommande lönetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="a2ab3-118">När du väljer knappen **OK** i den assisterade inställningsguiden, fylls sidan **Redovisningsjournal** med rader som representerar de transaktioner som lönefilen innehåller, samt med relevanta konton redan ifyllda i fälten **Redovisningsjournal** i enlighet med de mappningar som du har gjort i guiden.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** page is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="a2ab3-119">Ändra eller bokför journalrader som för alla andra redovisningtransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a2ab3-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="a2ab3-120">Mer information finns i [Bokföra transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="a2ab3-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="a2ab3-121">Se även</span><span class="sxs-lookup"><span data-stu-id="a2ab3-121">See Also</span></span>
[<span data-ttu-id="a2ab3-122">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="a2ab3-122">Finance</span></span>](finance.md)  
<span data-ttu-id="a2ab3-123">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="a2ab3-123">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="a2ab3-124">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="a2ab3-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
