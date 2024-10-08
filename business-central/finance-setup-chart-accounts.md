---
title: Ställa in eller ändra kontoplanen
description: Lär dig ställa in kontoplanen visar huvudbokskontona med redovisningskonton som lagrar dina ekonomiska data.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 04/23/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Ställa in eller ändra kontoplanen

Kontoplanen visar huvudbokskontona som lagrar dina ekonomiska data. [!INCLUDE[prod_short](includes/prod_short.md)] inkluderar en standardkontoplan som är klar att stödja din verksamhet. Du kan dock ändra standardkontona och du kan lägga till nya konton.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Lägga till eller ändra konton

Från kontoplanen kan du öppna varje redovisningskonto och lägga till eller ändra inställningar. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Om det behövs kan du använda flera rader för namnet på ett redovisningskonto. På sidan **Redovisningskontokort**, i gruppen **Konto**, väljer du **Extratexter** och fyller sedan i en eller flera rader med kontonamnet och kopierad text.  

För konton av typen **Summa** måste fältet **Summeringsintervall** fyllas i. För konton av typen **Till-summa** fylls det här fältet i automatiskt med hjälp av funktionen Indrag. När du har ställt in konton väljer du åtgärden **Bearbeta** och väljer sedan **Indrag av kontoplan**.  

> [!IMPORTANT]
> Om du har angett definitioner i fälten **Summeringsintervall** för konton av typen **Till-summa** innan indragsfunktionen används, måste du ange dessa igen eftersom värdena i alla **Till-summa**-fält skrivs över med funktionen.

## <a name="delete-accounts"></a>Ta bort konton

Du kan ta bort ett redovisningskonto. Men om du tar bort det, måste följande villkor gälla:  

* Saldot på kontot måste vara noll.  
* Fältet **Tillåt borttag. av redov.konto** måste anges på sidan **Redovisningsinställningar** och kontot får inte ha några redovisningstransaktioner på eller efter det datumet.  
* Om fältet **Kontr. redov.kontoanv.** på sidan **Redovisningsinställningar** markeras får kontot inte användas i någon av följande bokföringsmallar eller bokföringsinställningar.  

[!INCLUDE[prod_short](includes/prod_short.md)] förhindrar dig från att ta bort ett redovisningskonto som lagrar data som behövs i kontoplanen.  

Du kan också ange när personer ska tillåta att ta bort konton. På sidan **Redovisningsinställningar** fungerar växlingsknappen **Spärra radering av redovisningskonton** tillsammans med datumet i **Kontrollera borttagning av redovisningskonto efter** för att fungera som en extra validering. Om du aktiverar växlingsknappen **Spärra radering av redovisningskonton** kan du radera redovisningskonton som har transaktioner efter datumet i fältet **Kontrollera borttagning av redovisningskonto efter**. För att radera ett sådant konto måste någon med tillgång till sidan **Redovisningsinställningar** måste stänga av växlingsknappen **Spärra radering av redovisningskonton**.  

Aktivera **Spärra radering av redovisningskonton** anses ofta vara bästa praxis, och så även att ställa in datumet i fältet **Kontrollera borttagning av redovisningskonto efter** till exempel det datum efter vilket du måste lagra dina finansdata.  

### <a name="video-guidance"></a>Videovägledning

Den här videon visar hur man anger om och när personer kan ta bort huvudbokkonton.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1g3oY]

## <a name="learning-path-set-up-the-chart-of-accounts-in-dynamics-365-business-central"></a>Utbildningsväg: Ställ in kontoplanen i Dynamics 365 Business Central

Vill du lära dig hur du ställer in kontoplanen i [!INCLUDE [prod_short](includes/prod_short.md)]? Börja sedan med följande utbildningsväg i [Ställ in kontoplanen i Dynamics 365 Business Central](/training/modules/chart-accounts-dynamics-365-business-central).

## <a name="see-also"></a>Se även

[Huvudbok och kontolista](finance-general-ledger.md)  
[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Importera data från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Arbeta med ekonomiska rapporter](bi-how-work-account-schedule.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Avsluta resultatkonton i den franska versionen](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Skriv ut resultaträkningar i den australiska versionen](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Skriv ut resultaträkningar i den nyzeeländska versionen](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Ställ in och stäng resultaträkningssaldon i spanska versionen](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Indrag och validera kontoplanen i den spanska versionen](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
