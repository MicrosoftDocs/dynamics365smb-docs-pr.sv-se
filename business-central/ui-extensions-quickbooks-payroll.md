---
title: Använda Quickbooks-tillägget för import av lönefil till | Microsoft Docs
description: Detta ämnet beskriver hur du använder tillägget för att importera lön och lönetransaktioner från Quickbooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 838095fe81af36a421a49f19400b0abd5cdce17b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784771"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="d7a92-103">QuickBook-tillägg för import av lönefil</span><span class="sxs-lookup"><span data-stu-id="d7a92-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="d7a92-104">Använd filnamnstillägget QuickBooks-lön för att importera lönetransaktioner från QuickBooks till redovisningskonton i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d7a92-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d7a92-105">Exempelvis är detta användbart när du omvandlar från QuickBooks till [!INCLUDE[prod_short](includes/prod_short.md)], eller om du vill lägga ut din lön men också vill hålla reda på informationen i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d7a92-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="d7a92-106">Steg för att importera lönedata</span><span class="sxs-lookup"><span data-stu-id="d7a92-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="d7a92-107">Det första steget är för dig eller så kanske din revisor använder exportfunktioner i QuickBooks för att exportera lönedata till en .IIF-fil.</span><span class="sxs-lookup"><span data-stu-id="d7a92-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="d7a92-108">Nästa steg är att öppna sidan **redovisningsjournaler** i [!INCLUDE[prod_short](includes/prod_short.md)] och använda åtgärden **importera lönetransaktioner** för att importera filen.</span><span class="sxs-lookup"><span data-stu-id="d7a92-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="d7a92-109">Under importprocessen mappar du redovisningskontona från QuickBooks till motsvarande konton i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d7a92-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d7a92-110">Det sista steget är att bokföra lönetransaktioner i [!INCLUDE[prod_short](includes/prod_short.md)] enligt kontomappningen.</span><span class="sxs-lookup"><span data-stu-id="d7a92-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="d7a92-111">Mer information finns i [Så här importerar du lönetransaktioner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="d7a92-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d7a92-112">Se även</span><span class="sxs-lookup"><span data-stu-id="d7a92-112">See Also</span></span>
<span data-ttu-id="d7a92-113">[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="d7a92-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="d7a92-114">[Ekonomi](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="d7a92-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="d7a92-115">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d7a92-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]