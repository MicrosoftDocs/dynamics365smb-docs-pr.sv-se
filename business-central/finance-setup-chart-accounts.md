---
title: Skapa kontoplanen
description: Kontoplanen visar huvudbokskontona som lagrar dina ekonomiska data. Du kan dock ändra standardkontona i kontoplanen och du kan lägga till nya konton.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 506aae83d19c8b04102760017302e83d523f77e8
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6327044"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Ställa in eller ändra kontoplanen

Kontoplanen visar huvudbokskontona som lagrar dina ekonomiska data. [!INCLUDE[prod_short](includes/prod_short.md)] inkluderar en standardkontoplan som är klar att stödja din verksamhet.
Du kan dock ändra standardkontona och du kan lägga till nya konton.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="adding-or-changing-accounts"></a>Lägga till eller ändra konton

Från Kontoplan kan du öppna varje Redovisningskonto och lägga till eller ändra inställningar. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Om det behövs kan du använda flera rader för namnet på ett redovisningskonto. På sidan **Redovisningskontokort**, i gruppen **Konto**, väljer du **Extratexter** och fyller sedan i en eller flera rader med texten som ska kopieras och konto namnet.  

För konton av typen **Summa** måste fältet **Summeringsintervall** fyllas i. För konton av typen **Till-summa** fylls det här fältet i automatiskt med hjälp av funktionen Indrag. När du har skapat alla konton väljer du åtgärden **Bearbeta** och väljer sedan **Indrag av kontoplan**.  

> [!IMPORTANT]
> Om du har angett definitioner i fälten **Summeringsintervall** för konton av typen **Till-summa** innan indragsfunktionen används, måste du ange dessa igen eftersom värdena i alla **Till-summa**-fält skrivs över med funktionen.

## <a name="deleting-accounts"></a>Ta bort konton

Du kan ta bort ett redovisningskonto. Men om du tar bort det, måste följande förutsättningar gälla:  

* Saldot på kontot måste vara noll.  
* Fältet **Tillåt borttag. av redov.konto** måste anges på sidan **Redovisningsinställningar** och kontot får inte ha några redovisningstransaktioner på eller efter det datumet.  
* Om fältet **Kontr. redov.kontoanv.** på sidan **Redovisningsinställningar** markeras får kontot inte användas i någon av följande bokföringsgrupper eller bokföringsinställningar.  

[!INCLUDE[prod_short](includes/prod_short.md)] kommer att förhindra att du tar bort ett redovisningskonto som lagrar data som behövs i kontoplanen.  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Huvudbok och kontolista](finance-general-ledger.md)  
[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Importera data från andra finanssystem](across-import-data-configuration-packages.md)  
[Arbeta med kontouppställningar](bi-how-work-account-schedule.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Avsluta resultatkonton i den franska versionen](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Skriv ut resultaträkningar i den australiska versionen](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Skriv ut resultaträkningar i den nyzeeländska versionen](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Ställ in och stäng resultaträkningssaldon i spanska versionen](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Indrag och validera kontoplanen i den spanska versionen](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]