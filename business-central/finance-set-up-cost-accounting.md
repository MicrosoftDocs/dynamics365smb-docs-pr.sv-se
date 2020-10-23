---
title: Ställa in kostnadsredovisning | Microsoft Docs
description: Innan du börjar arbeta med kostnadsredovisning, måste du utföra inställningsuppgifter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d39d30891d822c25b0ce4aaec84bbbbc714ae311
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910761"
---
# <a name="setting-up-cost-accounting"></a>Ställa in kostnadsredovisning
Innan du börjar arbeta med kostnadsredovisning, måste du utföra inställningsuppgifter.

## <a name="balances-between-cost-type-cost-center-and-cost-object"></a>Saldon mellan kostnadstyp, kostnadsställe och kostnadsbärare
När du lägger upp kostnadsredovisning måste du kontrollera att alla transaktioner har kopplats till en kostnadstyp samt ett kostnadsställe eller en kostnadsbärare. Det innebär att varje kostnadstransaktion måste ha en tilldelad kostnadstyp och en kod för kostnadsställe eller kostnadsbärare. Denna regel ser till att alla kostnadstransaktioner visas i antingen kostnadsställena eller kostnadsbärarna, men inte på båda platserna.  

Genom att göra det, kan du skapa följande ekvation:  

*Kostnadstypssaldo* = *Kostnadsställesaldo* + *Kostnadsbärarsaldo*  

När du skriver ut rapporter med kostnadstyper, kostnadsställen och kostnadsbärare kan du analysera det här förhållandet.

## <a name="setting-up-cost-types"></a>Lägga upp kostnadstyper
Listan över kostnadstyper liknar kontoplanen i redovisningen. Du kan definiera planen för kostnadstyper på följande sätt:  

-   Strukturera planen över kostnadstyper på samma sätt som resultaträkningens konton i kontoplanen i redovisningen. Sedan kan du överföra kontoplanen i redovisningen till planen över kostnadstyper. Du kan göra nödvändiga justeringar efter överföringen.  
-   Skapa ny plan över kostnadstyper eller lägg till nya kostnadstyper till befintlig plan över kostnadstyper. Du måste skapa varje ny kostnadstyp för sig.  

### <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Överföra kontoplanen i redovisningen till redovisningsplanen över kostnadstyper  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lista över kostnadstyper** och välj sedan relaterad länk.  
2.  Välj åtgärden **Hämta kostnadstyper från kontoplan** action. Välj **ja** i dialogrutan för att bekräfta överföringen. Funktionen använder kontoplanen i redovisningen för att skapa en plan över kostnadstyper.  

    Planen över kostnadstyper innehåller nu alla resultaträkningskonton i redovisningen inklusive rubriker och delsummor. Du kan ändra planen över kostnadstyper efter behov. Du kan till exempel ta bort dubbletter av befintliga kostnadstyper.  

    > [!IMPORTANT]  
    >  Funktionen **Registrera kostnadstyper i kontoplan** uppdaterar relationen mellan kontoplanen och planen över kostnadstyper. Fältet **nr.** -fältet fylls och verifieras för att se till att varje redovisningskonto är kopplade till endast ett kostnadstyp. Kör funktionen automatiskt, före överföring av redovisningstransaktioner mot kostnadsredovisning.  

### <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Så här skapar du nya kostnadstyper på sidan Lista över kostnadsbärare.  
1.  Öppna sidan **Lista över kostnadstyper** i redigeringsläge.  
2.  Fyll i fälten som beskrivs efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Du kan lägga upp och underhålla kostnadstupen antingen i kortet **Kort för Kostnadstyper** eller på sidan **Lista över Kostnadstyper**. I den här proceduren skapar du Kostnadstyper på sidan **Lista över kostnadstyper**.

3.  När du har skapat alla kostnadstyper väljer du åtgärden **Indrag för kostnadstyper**. Välj **ja** i dialogrutan.  
4.  Koppla den nya kostnadstypen till motsvarande redovisningskonto.  

    > [!IMPORTANT]  
    >  Om du har angett definitioner i fältet **Summering** för rader av typen **Till-summa** innan du kör funktionen **Indrag för kostnadstyper** måste du ange definitionerna igen eftersom funktionen ersätter alla värden i alla **Till-summa**-fält.  

### <a name="to-update-cost-types"></a>Uppdatera kostnadstyper  
1.  Markera om du vill att planen över kostnadstyper automatiskt ska uppdateras när kontoplanen ändras på sidan **Inställningar för kostnadsredovisning**.  
2.  I fältet **Justera redovisningskonto** kan du välja något av följande alternativ.  

- **Ingen justering** - Ingen motsvarande ändring görs i planen över kostnadstyper när du ändrar kontoplanen.  
- **Automatisk** - Det görs en motsvarande ändring i planen över kostnadstyper när du ändrar kontoplanen.  
- **Fråga** - Ett meddelande visas och frågar om du vill göra en motsvarande ändring i planen över kostnadstyper när du ändrar kontoplanen.

## <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definiera relationen mellan kostnadstyper och redovisningskonton
Relationen mellan kostnadstypen och redovisningskontot skapas i kostnadstypen och i redovisningskontot.  

* Fältet **Redovisningskontointervall** i tabellen **Kostnadstyp** bestämmer vilka redovisningskonton som tillhör en kostnadstyp.  
* Fältet **Kostnadstypsnr.** i kontoplanen bestämmer vilken kostnadstyp ett redovisningskonto tillhör.  

Dessa två fält fylls i automatiskt när du använder funktionen **Hämta kostnadstyper från kontoplan**.  

### <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Relationen mellan redovisningskonton och kostnadstyper  
Det finns en många till en-relation mellan kostnadstyper och redovisningskonton. Flera redovisningskonton kan tillhöra en kostnadstyp, men varje redovisningskonto tillhör endast en kostnadstyp. Tabellen nedan beskriver informationen i sambandet.  

|Samband|**Redovisningskontointervall**|**Kostnadstypsnr**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Ett redovisningskonto för varje kostnadstyp|Ett redovisningskonton|En kostnadstyp|  
|Flera redovisningskonton för en kostnadstyp|Redovisningskontointervall, exempelvis 7110..7193 för varje redovisningskonto|För varje redovisningskonto i intervallet finns det bara en kostnadstyp|  
|Kostnadstyper utan motsvarande redovisningskonton|<Empty>||  
|Redovisningskonton vars transaktioner inte kommer att överföras||<Empty>|  

### <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Kostnadstyper utan en relation till redovisningen  
En kostnadstyp kan inte ha en koppling till redovisningskonton, om ett av följande villkor gäller:  

* Konton för rörelseredovisning, till exempel Beräkna ränta och avskrivning, tar endast kostnader från rörelseredovisningen.  
* Hjälpkostnadstyper, till exempel kostnadstyper 9901, 9902 och 9903 i databasen [!INCLUDE[d365fin](includes/d365fin_md.md)] används som kredit- och debetkonton för fördelningar.  
* Hjälpkontot 9920 i databasen [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller faktiska periodiseringar som visar skillnaden mellan kostnader och utgifterna från redovisningen.

## <a name="setting-up-cost-centers"></a>Lägga upp kostnadsställen
Kostnadsställen är avdelningar som ansvarar för kostnader och intäkter. Planen för kostnadsställen liknar dimensionsinformationen för redovisningen. Du kan definiera planen för kostnadsställen på följande sätt:  

-   Överför dimensionsvärden i redovisningen till företagets plan för kostnadsställen. Du kan göra nödvändiga justeringar efter överföringen.  
-   Skapa en ny plan för kostnadsstället som är oberoende av redovisningen, eller lägg till ett nytt kostnadsställe i en befintlig plan för kostnadsställen. Du måste skapa varje kostnadsställe var för sig.  

### <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Överföra dimensionsvärden i redovisningen till planen för kostnadsställen  
1.  Skapa en dimension som ska vara kostnadsställesdimensionen på sidan **Uppdatera kostnadsredovisningsdimensioner**. Endast värdena från dimensionen överförs.  
2.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lista över kostnadsställe** och välj sedan relaterad länk.  
3.  Välj **Hämta kostnadsställen från dimension** för att överföra dimensionsvärden till planen för kostnadsställen på fliken **Åtgärder** i gruppen **Funktioner**. Funktionen överför de dimensionsvärden som du har definierat i steg 1.  

    > [!NOTE]  
    >  Du kan ställa in fältet **Justera dimension för kostnadsställe** för att definiera en enkelriktad synkronisering av dimensionsvärden från redovisningen till diagrammet över kostnadsställen. Du kan inte definiera en synkronisering av diagrammet över kostnadsställen till dimensionsvärden från redovisningen.  

Diagrammet över kostnadsställen innehåller nu alla angivna dimensionsvärden från redovisningen inklusive titlar och delsummor.  

### <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a>Så här skapar du nya kostnadsställen på sidan Lista över kostnadsställen.  
Du kan lägga upp och underhålla kostnadsställen antingen i kortet **Kort för kostnadsställe** eller på sidan **Lista över kostnadsställen**. I den här proceduren skapar du kostnadsställen på sidan **Lista över kostnadsställen**.  

1. Öppna sidan **Lista över kostnadsställe** i redigeringsläge.  
2. Ange kostnadsställets kod i fältet **Kod**. Alla kostnadsställen måste ha en kod.  
3. Ange kostnadsställets namn i fältet **Namn**.  
4. Välj listpilen i fältet **Radtyp** för att ange syftet med kostnadsstället.  

    - För kostnadsställen av typen **Summa** måste du fylla fältet **Summering**. Använd **eller** operatorn som är en vertikal rad (**&#124;**) för att ange intervall av kostnadsställen.  
    - För kostnadsställen av radtypen **till-summa** fylls det här fältet i automatiskt när du använder indragsfunktionen.  
5.  Fyll i fälten **Sorteringsordning** och **Kostnadssubtyp**.  
6.  Välj nästa tomma rad för att skapa ett nytt kostnadsställe, och upprepa sedan steg 2 till 5.  
7.  När du har skapat alla kostnadsställen, väljer du åtgärden **Indrag för kostnadstyper**. Välj **Ja**.  

> [!IMPORTANT]  
>  Om du har angett definitioner i fältet  **Summering** för **Till-summa**-kostnadsställen innan du kör indragsfunktionen måste du ange dessa igen. Funktionen ersätter värdena i alla fält för **slutsummor**.

## <a name="setting-up-cost-objects"></a>Lägga upp kostnadsbärare
Kostnadsbärare är projekt, produkter eller tjänster i ett företag. Planen för kostnadsbärare liknar dimensionsinformationen för redovisningen. Du kan definiera planen för kostnadsbärare på följande sätt:  

* Överför dimensionsvärden i redovisningen till företagets plan för kostnadsbärare. Du kan göra nödvändiga justeringar efter överföringen.  
* Skapa en ny plan för kostnadsbäraren som är oberoende av redovisningen, eller lägg till en ny kostnadsbäraren i en befintlig plan för kostnadsbärare. Du måste skapa varje kostnadsbärare var för sig.  

### <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Så här överför du dimensionsvärden från redovisningen till kontoplanen för kostnadsbärare  
1.  Skapa en dimension som ska vara kostnadsbärardimensionen på sidan **Uppdatera CA-dimensioner**. Endast värdena från dimensionen överförs.  
2.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lista över kostnadsbärare** och välj sedan relaterad länk.  
3.  Välj åtgärden **Hämta kostnadsbärare från dimension** för att överföra dimensionsvärden till planen för kostnadsbärare. Funktionen överför de dimensionsvärden som du har definierat i steg 1.  

    > [!NOTE]  
    >  Du kan ställa in fältet **Justera dimension för kostnadsbärare** för att definiera en enkelriktad synkronisering av dimensionsvärden från redovisningen till diagrammet över kostnadsställen. Du kan inte definiera en synkronisering av diagrammet över kostnadsbärare till dimensionsvärden från redovisningen.  

Diagrammet över kostnadsbärare innehåller nu alla angivna dimensionsvärden från redovisningen inklusive rubriker och delsummor.  

### <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Så här skapar du nya kostnadsbärare på sidan Lista över kostnadsbärare.  
Du kan lägga upp och underhålla kostnadsbärare antingen i kortet **Kort för kostnadsbärare** eller på sidan **Lista över kostnadsbärare**. I den här proceduren skapar du kostnadsbärare på sidan **Lista över kostnadsbärare**.  

1.  Öppna sidan **Lista över kostnadsbärare** i redigeringsläge.  
2.  Ange kostnadsbäraren kod i fältet **Kod**. Alla kostnadsbärare måste ha en kod.  
3.  Ange kostnadsbärarens namn i fältet **Namn**.  
4.  Välj listpilen i fältet **Radtyp** för att ange syftet med kostnadsbäraren.  

    * För kostnadsbärare av radtypen **Summa** fyller du i fältet **Summa från/till**. Använd operatorn **eller** som är ett vertikalt streck (**&#124;**), för att ange intervall av kostnadsbärare.  
    * För kostnadsbärare av radtypen **slutsumma** fylls det här fältet i automatiskt när du använder indragsfunktionen.  
5.  Fyll i fältet **Bokföringsdatum**.  
6.  Välj nästa tomma rad för att skapa en ny kostnadsbäraren och upprepa sedan steg 2 till 5.  
7.  När du har skapat alla kostnadsbärare, väljer du åtgärden **Indrag för kostnadsbärare**. Välj **Ja**.  

> [!IMPORTANT]  
>  Om du har angett definitioner i fälten **Summa från/till** för **Till-summa** för kostnadsbärare innan du kör indragsfunktionen måste du ange dessa igen. Funktionen ersätter värdena i alla fält för **slutsummor**.

## <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definiera kostnadsställen och kostnadsbärare för kontoplanen
Du kan automatiskt överföra kostnads- och intäktstransaktioner från redovisningen till kostnadsredovisningen antingen för varje redovisningsbokföring eller med ett batch-jobb. När du gör överföringen överför, [!INCLUDE[d365fin](includes/d365fin_md.md)] endast de transaktioner som redan är länkade till ett kostnadsställe eller en kostnadsbärare. Om du vill skapa en meningsfullt överföring måste du kontrollera att kostnadsställena och kostnadsbärarna definierats korrekt.  

### <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Ange standarddimensionsvärden för redovisningskonton  
För varje redovisningskonto kan du ange standarddimensionsvärden i tabellen **Standarddimension**. Följande exempel visar hur du anger att det alltid ska finnas ett kostnadsställe för avdelningen, men aldrig är en kostnadsbärare för ett projekt när du bokför på ett redovisningskonto.  

|**Dimensionskod**|**Bokförs med**|  
|------------------------------------------|-----------------------------------------|  
|Avdelning|Kod alltid|  
|Objekt|Ingen kod|  

### <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definiera dimensionsvärden för omkostnader och direkta kostnader  
 Du kan överföra omkostnader till ett kostnadsställe och direkta kostnader till en kostnadsbärare. Följande tabell visar den optimala kombinationen av installationsvärden för dimensioner.  

|Överför till|Kostnadsställebokföring|Kostnadsbärarbokföring|  
|-----------------|-------------------------|-------------------------|  
|Kostnadsställe|Kod alltid|Ingen kod|  
|Kostnadsbärare|Ingen kod|Kod alltid|  

> [!NOTE]  
>  Markera kryssrutan **Kontrollera redovisningsbokföringar** för att se till att de fördefinierade kostnadsställena och kostnadsbärarna som du skapar i redovisningen automatiskt överförs till kostnadsredovisningen.

## <a name="see-also"></a>Se även  
[Redovisa kostnader](finance-manage-cost-accounting.md)  
[Överföra och bokföra kostnadstransaktioner](finance-transfer-and-post-cost-entries.md)   
[Definiera och fördela kostnader](finance-define-and-allocate-costs.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
