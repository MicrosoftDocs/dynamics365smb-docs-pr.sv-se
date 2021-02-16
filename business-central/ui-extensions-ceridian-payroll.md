---
title: Importera löner eller lönedata med hjälp av tillägget Ceridian
description: Använd det här tillägget för att importera lönetransaktioner från tjänsterna Ceridian personal/lön (USA) och Ceridian PowerPay (Kanada).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 717c8937ea4c057b51acb3c346d950d6b7c0a43e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757323"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="c349f-103">Tillägget Ceridian löner </span><span class="sxs-lookup"><span data-stu-id="c349f-103">The Ceridian Payroll Extension</span></span>

<span data-ttu-id="c349f-104">För att ta hänsyn till lönutbetalningar och relaterade transaktioner måste du importera och bokföra finansiella transaktioner som gjorts av ditt lönesystem i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="c349f-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="c349f-105">För att göra detta måste du först importera en fil som du får från lönelistleverantören till sidan **Redovisningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="c349f-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="c349f-106">Sedan mappar du de externa kontona i lönefilen till det relevanta redovisningskontot.</span><span class="sxs-lookup"><span data-stu-id="c349f-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="c349f-107">Slutligen bokför du lönetransaktioner enligt kontomappningen.</span><span class="sxs-lookup"><span data-stu-id="c349f-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="c349f-108">Mer information finns i [Så här importerar du lönetransaktioner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="c349f-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="c349f-109">Tillägget Ceridian lön låter dig importera lönetransaktioner från tjänsterna Ceridian personal/lön (USA) och Ceridian PowerPay (Kanada).</span><span class="sxs-lookup"><span data-stu-id="c349f-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="c349f-110">Se även</span><span class="sxs-lookup"><span data-stu-id="c349f-110">See Also</span></span>

<span data-ttu-id="c349f-111">[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c349f-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="c349f-112">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="c349f-112">Finance</span></span>](finance.md)  
<span data-ttu-id="c349f-113">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c349f-113">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
