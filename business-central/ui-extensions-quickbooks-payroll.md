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
# <a name="the-quickbooks-payroll-file-import-extension"></a>QuickBook-tillägg för import av lönefil
Använd filnamnstillägget QuickBooks-lön för att importera lönetransaktioner från QuickBooks till redovisningskonton i [!INCLUDE[prod_short](includes/prod_short.md)]. Exempelvis är detta användbart när du omvandlar från QuickBooks till [!INCLUDE[prod_short](includes/prod_short.md)], eller om du vill lägga ut din lön men också vill hålla reda på informationen i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="steps-to-import-payroll-data"></a>Steg för att importera lönedata
Det första steget är för dig eller så kanske din revisor använder exportfunktioner i QuickBooks för att exportera lönedata till en .IIF-fil. Nästa steg är att öppna sidan **redovisningsjournaler** i [!INCLUDE[prod_short](includes/prod_short.md)] och använda åtgärden **importera lönetransaktioner** för att importera filen. Under importprocessen mappar du redovisningskontona från QuickBooks till motsvarande konton i [!INCLUDE[prod_short](includes/prod_short.md)]. Det sista steget är att bokföra lönetransaktioner i [!INCLUDE[prod_short](includes/prod_short.md)] enligt kontomappningen. 

Mer information finns i [Så här importerar du lönetransaktioner](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Se även
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)    
[Ekonomi](finance.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]