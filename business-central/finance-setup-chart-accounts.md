---
title: Skapa kontoplanen
description: "Du kan ändra standardkontona i kontoplanen och du kan lägga till nya konton."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 9ed8bc069fc702a1b2d8d893531baca5eab7a903
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="7d2d7-103">Ställa in eller ändra kontoplanen</span><span class="sxs-lookup"><span data-stu-id="7d2d7-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="7d2d7-104">Kontoplanen visar huvudbokskontona som lagrar dina ekonomiska data.</span><span class="sxs-lookup"><span data-stu-id="7d2d7-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="7d2d7-105">inkluderar en standardkontoplan som är klar att stödja din verksamhet.</span><span class="sxs-lookup"><span data-stu-id="7d2d7-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="7d2d7-106">Du kan dock ändra standardkontona och du kan lägga till nya konton.</span><span class="sxs-lookup"><span data-stu-id="7d2d7-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="7d2d7-107">Lägga till eller ändra konton</span><span class="sxs-lookup"><span data-stu-id="7d2d7-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="7d2d7-108">Från Kontoplan kan du öppna varje Redovisningskonto och lägga till eller ändra inställningar.</span><span class="sxs-lookup"><span data-stu-id="7d2d7-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7d2d7-109">Du kan ta bort ett redovisningskonto.</span><span class="sxs-lookup"><span data-stu-id="7d2d7-109">You can delete a general ledger account.</span></span> <span data-ttu-id="7d2d7-110">Men om du tar bort det, måste följande förutsättningar gälla:</span><span class="sxs-lookup"><span data-stu-id="7d2d7-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="7d2d7-111">Saldot på kontot måste vara noll.</span><span class="sxs-lookup"><span data-stu-id="7d2d7-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="7d2d7-112">Fältet **Tillåt borttag. av redov.konto** måste anges på sidan **Redovisningsinställningar** och kontot får inte ha några redovisningstransaktioner på eller efter det datumet.</span><span class="sxs-lookup"><span data-stu-id="7d2d7-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="7d2d7-113">Om fältet **Kontr. redov.kontoanv.** på sidan **Redovisningsinställningar** markeras får kontot inte användas i någon av följande bokföringsgrupper eller bokföringsinställningar.</span><span class="sxs-lookup"><span data-stu-id="7d2d7-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="7d2d7-114">kommer att förhindra att du tar bort ett redovisningskonto som lagrar data som behövs i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="7d2d7-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7d2d7-115">Se även</span><span class="sxs-lookup"><span data-stu-id="7d2d7-115">See Also</span></span>
[<span data-ttu-id="7d2d7-116">Redovisningen och kontoplanen</span><span class="sxs-lookup"><span data-stu-id="7d2d7-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="7d2d7-117">Hantera bankkonton</span><span class="sxs-lookup"><span data-stu-id="7d2d7-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="7d2d7-118">Arbeta med dimensioner</span><span class="sxs-lookup"><span data-stu-id="7d2d7-118">Working with Dimensions</span></span>](finance-dimensions.md)  
<span data-ttu-id="7d2d7-119">[Importera data från andra finansiella system](across-import-data-configuration-packages.md)(across-import-data-configuration-packages.md)</span><span class="sxs-lookup"><span data-stu-id="7d2d7-119">[Importing Data from Other Finance Systems](across-import-data-configuration-packages.md)(across-import-data-configuration-packages.md)</span></span>  
[<span data-ttu-id="7d2d7-120">Arbeta med kontouppställningar</span><span class="sxs-lookup"><span data-stu-id="7d2d7-120">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="7d2d7-121">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7d2d7-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

