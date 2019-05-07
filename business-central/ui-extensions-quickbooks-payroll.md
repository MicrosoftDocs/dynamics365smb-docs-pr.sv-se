---
title: Använda Quickbooks-tillägget för import av lönefil till | Microsoft Docs
description: Detta ämnet beskriver hur du använder tillägget för att importera lön och lönetransaktioner från Quickbooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c7ac2a17ecc0c2a33ea166968f577ca46e8282ed
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "920541"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="23ac5-103">QuickBook-tillägg för import av lönefil</span><span class="sxs-lookup"><span data-stu-id="23ac5-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="23ac5-104">Använd filnamnstillägget QuickBooks-lön för att importera lönetransaktioner från QuickBooks till redovisningskonton i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="23ac5-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="23ac5-105">Exempelvis är detta användbart när du omvandlar från QuickBooks till [!INCLUDE[d365fin](includes/d365fin_md.md)], eller om du vill lägga ut din lön men också vill hålla reda på informationen i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="23ac5-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="23ac5-106">Steg för att importera lönedata</span><span class="sxs-lookup"><span data-stu-id="23ac5-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="23ac5-107">Det första steget är för dig eller så kanske din revisor använder exportfunktioner i QuickBooks för att exportera lönedata till en .IIF-fil.</span><span class="sxs-lookup"><span data-stu-id="23ac5-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="23ac5-108">Nästa steg är att öppna sidan **redovisningsjournaler** i [!INCLUDE[d365fin](includes/d365fin_md.md)] och använda åtgärden **importera lönetransaktioner** för att importera filen.</span><span class="sxs-lookup"><span data-stu-id="23ac5-108">The second step is to open the **General Journals** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="23ac5-109">Under importprocessen mappar du redovisningskontona från QuickBooks till motsvarande konton i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="23ac5-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="23ac5-110">Det sista steget är att bokföra lönetransaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] enligt kontomappningen.</span><span class="sxs-lookup"><span data-stu-id="23ac5-110">The final step is to post the payroll transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] according to the account mapping.</span></span> 

<span data-ttu-id="23ac5-111">Mer information finns i [Så här importerar du lönetransaktioner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="23ac5-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="23ac5-112">Se även</span><span class="sxs-lookup"><span data-stu-id="23ac5-112">See Also</span></span>
<span data-ttu-id="23ac5-113">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="23ac5-113">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="23ac5-114">[Ekonomi](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="23ac5-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="23ac5-115">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="23ac5-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
