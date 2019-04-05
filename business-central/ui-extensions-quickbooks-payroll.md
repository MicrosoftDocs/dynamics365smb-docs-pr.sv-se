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
ms.date: 01/09/2019
ms.author: bholtorf
ms.openlocfilehash: ac68f8a4d67224ad55b1c34ff9b2e4ffa2c372aa
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807300"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a>QuickBook-tillägg för import av lönefil
Använd filnamnstillägget QuickBooks-lön för att importera lönetransaktioner från QuickBooks till redovisningskonton i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Exempelvis är detta användbart när du omvandlar från QuickBooks till [!INCLUDE[d365fin](includes/d365fin_md.md)], eller om du vill lägga ut din lön men också vill hålla reda på informationen i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="steps-to-import-payroll-data"></a>Steg för att importera lönedata
Det första steget är för dig eller så kanske din revisor använder exportfunktioner i QuickBooks för att exportera lönedata till en .IIF-fil. Nästa steg är att öppna sidan **redovisningsjournaler** i [!INCLUDE[d365fin](includes/d365fin_md.md)] och använda åtgärden **importera lönetransaktioner** för att importera filen. Under importprocessen mappar du redovisningskontona från QuickBooks till motsvarande konton i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det sista steget är att bokföra lönetransaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] enligt kontomappningen. 

Mer information finns i [Så här importerar du lönetransaktioner](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Se även
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)    
[Ekonomi](finance.md)    
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
