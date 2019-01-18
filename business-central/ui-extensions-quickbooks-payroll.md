---
title: "Använda Quickbooks-tillägget för import av lönefil till | Microsoft Docs"
description: "Beskriver hur du använder tillägget för att importera lön och lönetransaktioner från tjänsten Quickbooks lön."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: caf928b653b528c10820a8dfa8feff498c88f4ff
ms.contentlocale: sv-se
ms.lasthandoff: 11/22/2018

---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="fa35e-103">QuickBook-tillägg för import av lönefil</span><span class="sxs-lookup"><span data-stu-id="fa35e-103">The Quickbooks Payroll File Import Extension</span></span>
<span data-ttu-id="fa35e-104">För att ta hänsyn till lönutbetalningar och relaterade transaktioner måste du importera och bokföra finansiella transaktioner som gjorts av ditt lönesystem i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="fa35e-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="fa35e-105">För att göra detta måste du först importera en fil som du får från lönelistleverantören till sidan **Redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="fa35e-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="fa35e-106">Sedan mappar du de externa kontona i lönefilen till det relevanta redovisningskontot.</span><span class="sxs-lookup"><span data-stu-id="fa35e-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="fa35e-107">Slutligen bokför du lönetransaktioner enligt kontomappningen.</span><span class="sxs-lookup"><span data-stu-id="fa35e-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="fa35e-108">Mer information finns i [Så här importerar du lönetransaktioner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="fa35e-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="fa35e-109">Med QuickBooks-importtillägget för lönefiler kan du importera lönetransaktioner från QuickBooks-lönetjänsten.</span><span class="sxs-lookup"><span data-stu-id="fa35e-109">The Quickbooks Payroll File Import extension allows you to import payroll transaction from the Quickbooks Payroll service.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa35e-110">Se även</span><span class="sxs-lookup"><span data-stu-id="fa35e-110">See Also</span></span>
<span data-ttu-id="fa35e-111">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="fa35e-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="fa35e-112">[Ekonomi](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="fa35e-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="fa35e-113">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fa35e-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

