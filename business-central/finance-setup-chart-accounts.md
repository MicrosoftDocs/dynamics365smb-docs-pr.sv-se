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
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 9f84af8bb4ac3be9132ab621906c463cfc9b91ff
ms.contentlocale: sv-se
ms.lasthandoff: 05/17/2018

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
[Importera data från andra finansiella system](across-import-data-configuration-packages.md)(across-import-data-configuration-packages.md)  
[Arbeta med kontouppställningar](bi-how-work-account-schedule.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

