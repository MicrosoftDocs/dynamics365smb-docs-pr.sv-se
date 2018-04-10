---
title: "Ställa in kontoplanen | Microsoft Docs"
description: "Du kan ändra standardkontona i kontoplanen och du kan lägga till nya konton."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cce6320e24ba8d73825e7cb71ada262c5af242a7
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="a984e-103">Ställa in eller ändra kontoplanen</span><span class="sxs-lookup"><span data-stu-id="a984e-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="a984e-104">Kontoplanen visar huvudbokskontona som lagrar dina ekonomiska data.</span><span class="sxs-lookup"><span data-stu-id="a984e-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="a984e-105"> inkluderar en standardkontoplan som är klar att stödja din verksamhet.</span><span class="sxs-lookup"><span data-stu-id="a984e-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="a984e-106">Du kan dock ändra standardkontona och du kan lägga till nya konton.</span><span class="sxs-lookup"><span data-stu-id="a984e-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="a984e-107">Lägga till eller ändra konton</span><span class="sxs-lookup"><span data-stu-id="a984e-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="a984e-108">Från Kontoplan kan du öppna varje Redovisningskonto och lägga till eller ändra inställningar.</span><span class="sxs-lookup"><span data-stu-id="a984e-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="a984e-109">Du kan ta bort ett redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="a984e-109">You can delete a general ledger account.</span></span> <span data-ttu-id="a984e-110">Men om du tar bort det, måste följande förutsättningar gälla:</span><span class="sxs-lookup"><span data-stu-id="a984e-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="a984e-111">Saldot på kontot måste vara noll.</span><span class="sxs-lookup"><span data-stu-id="a984e-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="a984e-112">Fältet **Tillåt borttag. av redov.konto** måste anges i fönstret **Redovisningsinställningar** och kontot får inte ha några redovisningstransaktioner på eller efter det datumet.</span><span class="sxs-lookup"><span data-stu-id="a984e-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="a984e-113">Om fältet **Kontr. redov.kontoanv.** i fönstret **Redovisningsinställningar** markeras får kontot inte användas i någon av följande bokföringsgrupper eller bokföringsinställningar.</span><span class="sxs-lookup"><span data-stu-id="a984e-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="a984e-114"> kommer att förhindra att du tar bort ett redovisningskonto som lagrar data som behövs i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="a984e-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a984e-115">Se även</span><span class="sxs-lookup"><span data-stu-id="a984e-115">See Also</span></span>
[<span data-ttu-id="a984e-116">Redovisningen och kontoplanen</span><span class="sxs-lookup"><span data-stu-id="a984e-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="a984e-117">Hantera bankkonton</span><span class="sxs-lookup"><span data-stu-id="a984e-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="a984e-118">Arbeta med dimensioner</span><span class="sxs-lookup"><span data-stu-id="a984e-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="a984e-119">Importera från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="a984e-119">Importing from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="a984e-120">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a984e-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
