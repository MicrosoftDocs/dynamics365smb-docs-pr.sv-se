---
title: Skapa kontoplanen
description: Du kan ändra standardkontona i kontoplanen och du kan lägga till nya konton.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f14859a641ddf6368a213f396a111a3423f49c4a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377118"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="954a3-103">Ställa in eller ändra kontoplanen</span><span class="sxs-lookup"><span data-stu-id="954a3-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="954a3-104">Kontoplanen visar huvudbokskontona som lagrar dina ekonomiska data.</span><span class="sxs-lookup"><span data-stu-id="954a3-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="954a3-105">inkluderar en standardkontoplan som är klar att stödja din verksamhet.</span><span class="sxs-lookup"><span data-stu-id="954a3-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="954a3-106">Du kan dock ändra standardkontona och du kan lägga till nya konton.</span><span class="sxs-lookup"><span data-stu-id="954a3-106">However, you can change the default accounts, and you can add new accounts.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]


## <a name="adding-or-changing-accounts"></a><span data-ttu-id="954a3-107">Lägga till eller ändra konton</span><span class="sxs-lookup"><span data-stu-id="954a3-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="954a3-108">Från Kontoplan kan du öppna varje Redovisningskonto och lägga till eller ändra inställningar.</span><span class="sxs-lookup"><span data-stu-id="954a3-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="954a3-109">Du kan ta bort ett redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="954a3-109">You can delete a general ledger account.</span></span> <span data-ttu-id="954a3-110">Men om du tar bort det, måste följande förutsättningar gälla:</span><span class="sxs-lookup"><span data-stu-id="954a3-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="954a3-111">Saldot på kontot måste vara noll.</span><span class="sxs-lookup"><span data-stu-id="954a3-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="954a3-112">Fältet **Tillåt borttag. av redov.konto** måste anges på sidan **Redovisningsinställningar** och kontot får inte ha några redovisningstransaktioner på eller efter det datumet.</span><span class="sxs-lookup"><span data-stu-id="954a3-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="954a3-113">Om fältet **Kontr. redov.kontoanv.** på sidan **Redovisningsinställningar** markeras får kontot inte användas i någon av följande bokföringsgrupper eller bokföringsinställningar.</span><span class="sxs-lookup"><span data-stu-id="954a3-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="954a3-114">kommer att förhindra att du tar bort ett redovisningskonto som lagrar data som behövs i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="954a3-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="954a3-115">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="954a3-115">See Related Training at [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="954a3-116">Se även</span><span class="sxs-lookup"><span data-stu-id="954a3-116">See Also</span></span>
[<span data-ttu-id="954a3-117">Huvudbok och kontolista</span><span class="sxs-lookup"><span data-stu-id="954a3-117">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="954a3-118">Jämka bankkonton</span><span class="sxs-lookup"><span data-stu-id="954a3-118">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="954a3-119">Arbeta med dimensioner</span><span class="sxs-lookup"><span data-stu-id="954a3-119">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="954a3-120">Importera data från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="954a3-120">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="954a3-121">Arbeta med kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="954a3-121">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="954a3-122">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="954a3-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]