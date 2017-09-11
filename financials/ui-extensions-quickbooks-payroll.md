---
title: "Använda QuickBooks tillägg för import av lönefil till | Microsoft Docs"
description: "Beskriver hur du använder tillägget för att importera lön och lönetransaktioner från tjänsten Quickbooks lön."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 03/29/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b719a7d2b6b5590ae63920b63aaba8c2313a8661
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="the-quickbooks-payroll-file-import-extension-to-dynamics-365-for-financials"></a><span data-ttu-id="c47d8-103">QuickBooks tillägg för import av lönefil till Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="c47d8-103">The Quickbooks Payroll File Import Extension to Dynamics 365 for Financials</span></span>
<span data-ttu-id="c47d8-104">För att ta hänsyn till lönutbetalningar och relaterade transaktioner måste du importera och bokföra finansiella transaktioner som gjorts av ditt lönesystem i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="c47d8-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="c47d8-105">För att göra detta måste du först importera en fil som du får från lönelistleverantören till fönstret **Redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="c47d8-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="c47d8-106">Sedan mappar du de externa kontona i lönefilen till det relevanta redovisningskontot.</span><span class="sxs-lookup"><span data-stu-id="c47d8-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="c47d8-107">Slutligen bokför du lönetransaktioner enligt kontomappningen.</span><span class="sxs-lookup"><span data-stu-id="c47d8-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="c47d8-108">Mer information finns i [Så här importerar du lönetransaktioner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="c47d8-108">For more information, see [How to: Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="c47d8-109">Med QuickBooks-importtillägget för lönefiler kan du importera lönetransaktioner från QuickBooks-lönetjänsten.</span><span class="sxs-lookup"><span data-stu-id="c47d8-109">The Quickbooks Payroll File Import extension allows you to import payroll transaction from the Quickbooks Payroll service.</span></span>

## <a name="see-also"></a><span data-ttu-id="c47d8-110">Se även</span><span class="sxs-lookup"><span data-stu-id="c47d8-110">See Also</span></span>
<span data-ttu-id="c47d8-111">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="c47d8-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="c47d8-112">[Ekonomi](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="c47d8-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="c47d8-113">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c47d8-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

