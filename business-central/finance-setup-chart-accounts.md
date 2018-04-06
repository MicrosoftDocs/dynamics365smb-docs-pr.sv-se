---
title: "Ställa in kontoplanen | Microsoft Docs"
description: "Du kan ändra standardkontona i kontoplanen och du kan lägga till nya konton."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cce6320e24ba8d73825e7cb71ada262c5af242a7
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Ställa in eller ändra kontoplanen
Kontoplanen visar huvudbokskontona som lagrar dina ekonomiska data. [!INCLUDE[d365fin](includes/d365fin_md.md)] inkluderar en standardkontoplan som är klar att stödja din verksamhet.
Du kan dock ändra standardkontona och du kan lägga till nya konton.  

## <a name="adding-or-changing-accounts"></a>Lägga till eller ändra konton
Från Kontoplan kan du öppna varje Redovisningskonto och lägga till eller ändra inställningar.

> [!NOTE]  
>   Du kan ta bort ett redovisningskonto. Men om du tar bort det, måste följande förutsättningar gälla:  

* Saldot på kontot måste vara noll.  
* Fältet **Tillåt borttag. av redov.konto** måste anges i fönstret **Redovisningsinställningar** och kontot får inte ha några redovisningstransaktioner på eller efter det datumet.  
* Om fältet **Kontr. redov.kontoanv.** i fönstret **Redovisningsinställningar** markeras får kontot inte användas i någon av följande bokföringsgrupper eller bokföringsinställningar.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] kommer att förhindra att du tar bort ett redovisningskonto som lagrar data som behövs i kontoplanen.  

## <a name="see-also"></a>Se även
[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Hantera bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Importera från andra finanssystem](upload-data.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

