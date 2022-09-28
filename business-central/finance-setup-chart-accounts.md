---
title: Ställa in kontoplan (innehåller video)
description: Kontoplanen visar huvudbokskontona som lagrar dina ekonomiska data. Du kan dock ändra standardkontona i kontoplanen och du kan lägga till nya konton.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.search.form: 16, 17, 18, 118, 386, 391
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: 57dadabe2e96654a919127f17fcc6391786eb90f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533623"
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Ställa in eller ändra kontoplanen

Kontoplanen visar huvudbokskontona som lagrar dina ekonomiska data. [!INCLUDE[prod_short](includes/prod_short.md)] inkluderar en standardkontoplan som är klar att stödja din verksamhet.
Du kan dock ändra standardkontona och du kan lägga till nya konton.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Lägga till eller ändra konton

Från Kontoplan kan du öppna varje Redovisningskonto och lägga till eller ändra inställningar. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Om det behövs kan du använda flera rader för namnet på ett redovisningskonto. På sidan **Redovisningskontokort**, i gruppen **Konto**, väljer du **Extratexter** och fyller sedan i en eller flera rader med texten som ska kopieras och konto namnet.  

För konton av typen **Summa** måste fältet **Summeringsintervall** fyllas i. För konton av typen **Till-summa** fylls det här fältet i automatiskt med hjälp av funktionen Indrag. När du har skapat alla konton väljer du åtgärden **Bearbeta** och väljer sedan **Indrag av kontoplan**.  

> [!IMPORTANT]
> Om du har angett definitioner i fälten **Summeringsintervall** för konton av typen **Till-summa** innan indragsfunktionen används, måste du ange dessa igen eftersom värdena i alla **Till-summa**-fält skrivs över med funktionen.

## <a name="delete-accounts"></a>Ta bort konton

Du kan ta bort ett redovisningskonto. Men om du tar bort det, måste följande förutsättningar gälla:  

* Saldot på kontot måste vara noll.  
* Fältet **Tillåt borttag. av redov.konto** måste anges på sidan **Redovisningsinställningar** och kontot får inte ha några redovisningstransaktioner på eller efter det datumet.  
* Om fältet **Kontr. redov.kontoanv.** på sidan **Redovisningsinställningar** markeras får kontot inte användas i någon av följande bokföringsmallar eller bokföringsinställningar.  

[!INCLUDE[prod_short](includes/prod_short.md)] kommer att förhindra att du tar bort ett redovisningskonto som lagrar data som behövs i kontoplanen.  

## <a name="block-deletion-of-gl-accounts"></a>Spärra borttagning av redovisningskonton

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

I 2022 års utgivningscykel 2 införs extra skydd mot oavsiktlig borttagning av redovisningskonton även i de fall då kriterierna uppfylls.  

Ett nytt fält, **Spärra radering av redovisningskonton** läggs till på sidan **Redovisningsinställningar**. Fältet fungerar som en extra validering när en användare försöker ta bort ett konto där det finns redovisningstransaktioner efter det datum som har angetts i fältet **Kontrollera borttagning av redovisningskonto efter**.

Om fältet **Spärra radering av redovisningskonton** har ställts in på *Ja* kan du inte radera redovisningskonton som har transaktioner efter datumet i fältet **Kontrollera borttagning av redovisningskonto efter**. För att ett sådant konto ska kunna tas bort måste en användare med åtkomst till sidan **Redovisningsinställningar** först ställa in detta fält på *Nej*. Därefter kan kontot tas bort.  

Vi rekommenderar att du ställer in fältet **Spärra radering av redovisningskonton** som *Ja*. Vi rekommenderar också att du alltid har ett datum angivet i fältet **Kontrollera borttagning av redovisningskonto efter**, till exempel den tidpunkt då du måste lagra dina ekonomidata.  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Huvudbok och kontolista](finance-general-ledger.md)  
[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Importera data från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Arbeta med kontouppställningar](bi-how-work-account-schedule.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Avsluta resultatkonton i den franska versionen](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Skriv ut resultaträkningar i den australiska versionen](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Skriv ut resultaträkningar i den nyzeeländska versionen](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Ställ in och stäng resultaträkningssaldon i spanska versionen](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Indrag och validera kontoplanen i den spanska versionen](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
