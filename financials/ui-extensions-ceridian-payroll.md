---
title: "Importera löner eller lönedata med hjälp av tillägget Ceridian | Microsoft Docs"
description: "Använd det här tillägget för att importera lönetransaktioner från tjänsterna Ceridian personal/lön (USA) och Ceridian PowerPay (Kanada)."
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
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 3c67d6bd4d24d5b58462fa05168f2ac764b2c695
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---
# <a name="the-ceridian-payroll-extension-to-dynamics-365-business-edition"></a><span data-ttu-id="7949b-103">Tillägget Ceridian lön till Dynamics 365 Business edition.</span><span class="sxs-lookup"><span data-stu-id="7949b-103">The Ceridian Payroll Extension to Dynamics 365 Business edition</span></span> 
<span data-ttu-id="7949b-104">För att ta hänsyn till lönutbetalningar och relaterade transaktioner måste du importera och bokföra finansiella transaktioner som gjorts av ditt lönesystem i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="7949b-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="7949b-105">För att göra detta måste du först importera en fil som du får från lönelistleverantören till fönstret **Redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="7949b-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="7949b-106">Sedan mappar du de externa kontona i lönefilen till det relevanta redovisningskontot.</span><span class="sxs-lookup"><span data-stu-id="7949b-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="7949b-107">Slutligen bokför du lönetransaktioner enligt kontomappningen.</span><span class="sxs-lookup"><span data-stu-id="7949b-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="7949b-108">Mer information finns i [Så här importerar du lönetransaktioner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="7949b-108">For more information, see [How to: Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="7949b-109">Tillägget Ceridian lön låter dig importera lönetransaktioner från tjänsterna Ceridian personal/lön (USA) och Ceridian PowerPay (Kanada).</span><span class="sxs-lookup"><span data-stu-id="7949b-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="7949b-110">Se även</span><span class="sxs-lookup"><span data-stu-id="7949b-110">See Also</span></span>
<span data-ttu-id="7949b-111">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="7949b-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="7949b-112">[Ekonomi](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="7949b-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="7949b-113">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7949b-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

