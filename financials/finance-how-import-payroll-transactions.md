---
title: "Importera lönetransaktioner | Microsoft Docs"
description: "Om du vill hantera lön, importera och bokföra ekonomiska transaktioner från leverantören lön i redovisningen med hjälp av filtillägget lön, till exempel Ceridian eller Quickbooks."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 06/16/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d53dfb26a3fea663e68a3b558579a59184e9de26
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-import-payroll-transactions"></a><span data-ttu-id="d88f7-103">Så här Importera du lönetransaktioner </span><span class="sxs-lookup"><span data-stu-id="d88f7-103">How to: Import Payroll Transactions</span></span>
<span data-ttu-id="d88f7-104">För att ta hänsyn till lönutbetalningar och relaterade transaktioner måste du importera och bokföra finansiella transaktioner som gjorts av ditt lönesystem i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="d88f7-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="d88f7-105">För att göra detta måste du först importera en fil som du får från lönelistleverantören till fönstret **Redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="d88f7-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="d88f7-106">Sedan mappar du de externa kontona i lönefilen till det relevanta redovisningskontot.</span><span class="sxs-lookup"><span data-stu-id="d88f7-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="d88f7-107">Slutligen bokför du lönetransaktioner enligt kontomappningen.</span><span class="sxs-lookup"><span data-stu-id="d88f7-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d88f7-108">Om du vill använda denna funktion måste ett tillägg för lönelisteimport ha installerats och aktiverats.</span><span class="sxs-lookup"><span data-stu-id="d88f7-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="d88f7-109">Tilläggen Ceridian lön och importera Quickbooks lön är förinstallerade i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d88f7-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d88f7-110">Mer information finns i [Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="d88f7-110">For more information, see [Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="d88f7-111">Att importera en lönefil</span><span class="sxs-lookup"><span data-stu-id="d88f7-111">To import a payroll file</span></span>
1. <span data-ttu-id="d88f7-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d88f7-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="d88f7-113">I relevant redovisningsjournal väljer du åtgärden **Importera lönetransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="d88f7-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="d88f7-114">En assisterad inställningsguide öppnas.</span><span class="sxs-lookup"><span data-stu-id="d88f7-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="d88f7-115">Följ anvisningarna i fönstret **Importera lönetransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="d88f7-115">Follow the steps in the **Import Payroll Transactions** window.</span></span>

    > [!TIP]  
>   <span data-ttu-id="d88f7-116">I steget som berör mappning av externa löneposter till dina redovisningskonton kommer mappningarna som du skapar att sparas till nästa gång samma poster importeras.</span><span class="sxs-lookup"><span data-stu-id="d88f7-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="d88f7-117">Detta besparar dig tid eftersom du inte behöver fylla i fältet **Kontonummer** manuellt</span><span class="sxs-lookup"><span data-stu-id="d88f7-117">This will save you time as you do not have to manually fill in the **Account No.**</span></span> <span data-ttu-id="d88f7-118">varje gång du importerar återkommande lönetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="d88f7-118">field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="d88f7-119">När du väljer knappen **OK** i den assisterade inställningsguiden, fylls fönstret **Redovisningsjournal** med rader som representerar de transaktioner som lönefilen innehåller, samt med relevanta konton redan ifyllda i fälten **Redovisningsjournal** i enlighet med de mappningar som du har gjort i guiden.</span><span class="sxs-lookup"><span data-stu-id="d88f7-119">When you choose the **OK** button in the assisted setup guide, the **General Journal** window is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="d88f7-120">Ändra eller bokför journalrader som för alla andra redovisningtransaktioner.</span><span class="sxs-lookup"><span data-stu-id="d88f7-120">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="d88f7-121">Mer information finns i [Så här bokför du transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="d88f7-121">For more information, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="d88f7-122">Se även</span><span class="sxs-lookup"><span data-stu-id="d88f7-122">See Also</span></span>
[<span data-ttu-id="d88f7-123">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="d88f7-123">Finance</span></span>](finance.md)  
<span data-ttu-id="d88f7-124">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="d88f7-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="d88f7-125">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="d88f7-125">Working with General Journals</span></span>](ui-work-general-journals.md)  

