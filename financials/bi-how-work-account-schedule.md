---
title: "Arbeta med kontouppställningar | Microsoft Docs"
description: "Beskriver hur du kan använda kontouppställningar för att skapa olika vyer och rapporten för att analysera ekonomisk prestandadata."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7b28d3ec6f4a52c5229d2e121ff1fe8ed847eeb7
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-account-schedules"></a>Arbeta med kontouppställningar
Du kan använda kontouppställningar för att få information om ekonomiska data som lagras i din kontoplan. Kontouppställningar analyserar siffror för redovisningskonton och jämför redovisningstransaktioner med redovisningsbudgettransaktioner. Resultaten visas i diagram i ditt Rollcenter, till exempel diagram för kassaflöde.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller några exempel på kontouppställningar som du kan använda direkt eller så kan du ange egna rader och kolumner för att jämföra siffrorna. Du kan till exempel skapa kontouppställningar för att beräkna vinstmarginaler på dimensioner som avdelningar eller kundgrupper. Du kan skapa så många anpassade finansiella rapporter som du önskar.  

Ställa in kontouppställningar kräver en förståelse för den ekonomiska informationen i kontoplanen. Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna. Detta kräver att budgetar som skapas. Mer information finns i [Skapa redovisningsbudgetar](finance-how-create-budgets.md)

## <a name="account-categories-and-account-schedules"></a>Kontokategorier och kontouppställningar
Du kan använda kontokategorier för att ändra layout på din redovisning. När du har upprättat din kontokategorier i fönstret **Redovisningskontokategorier** och du väljer åtgärden **Skapa kontouppställningar** uppdateras de underliggande kontouppställningarna för de centrala ekonomiska rapporterna. Nästa gång du kör någon av dessa rapporter, till exempel kontoavstämning kommer nya summor och underposter att läggas till, baserat på ändringarna. Mer information finns i [Redovisning och kontoplan](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Så här skapar du nya kontouppställningar  
 Du använder kontouppställningar för att analysera siffror för redovisningskonton eller jämföra redovisningstransaktioner med redovisningsbudgettransaktioner. Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna.

1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **kontouppställningar**, och välj sedan relaterad länk.  
2. I fönstret **Kontouppställningsnamn** väljer du åtgärden **Ny** för att skapa ett nytt kontouppställningsnamn.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj åtgärden **Redigera kontouppställning**.
5. I fönstret **Kontouppställning** fyller du i fälten.  

    När du har skapat en ny kontouppställning och skapat raderna måste du skapa kolumner. Du kan skapa kolumnerna manuellt eller tilldela en fördefinierad kolumnlayout till kontouppställningen.
6. Välj åtgärden **Redigera inställning av kolumnlayout**.
7. I fönstret **Kolumnlayout** fyller du i fälten.

> [!NOTE]  
>   Om du inte tilldelar en standardkolumnlayout till kontouppställningen måste du  lägga upp kolumner manuellt.   

### <a name="to-create-a-column-that-calculates-percentages"></a>Så här skapar du en kolumn för att beräkna procentsatser  
Du kan lägga till en kolumn i en kontouppställning för att beräkna procentsatser för en summa. Om du t.ex. har ett antal rader där försäljningen delas upp per dimension kan du lägga till en kolumn för att ange procentsatsen av total försäljning som varje rad representerar.

1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **kontouppställningar**, och välj sedan relaterad länk.
2. Välj en kontouppställning i fönstret **Kontouppställningsnamn**.  
3. Välj åtgärden **Redigera kontouppställning** för att skapa en kontouppställningsrad för att beräkna den summa som procentsatserna ska baseras på .  
4. Infoga en rad direkt ovanför den första raden för vilken du vill visa en procentsats.  
5. Fyll i fälten på raden på följande sätt: I fältet **summeringstyp** anger du **inställningsbas för procent**. I fältet **Summeringsintervall** anger du en formel för den summa som procentsatsen kommer att baseras på. Ange till exempel **11** om rad 11 innehåller den totala försäljningen.  
6. Välj åtgärden **Redigera inställning av kolumnlayout** för att ange en kolumn.  
7. Fyll i fälten på raden på följande sätt: I fältet **kolumntyp** väljer **formeln**. I fältet **Formel** anger du en formel för det belopp som du vill beräkna en procentsats för, följt av %. Om till exempel kolumn N innehåller nettoförändringen anger du **N%**.  
8. Upprepa steg 4-7 för varje grupp av kolumner som du vill dela upp per procentsats.

## <a name="to-set-up-account-schedules-with-overviews"></a>Så här skapar du kontouppställningar med översikter  
Du kan använda en kontouppställning för att skapa en rapport där redovisningssiffror jämförs med redovisningsbudgetsiffror.

1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **kontouppställningar**, och välj sedan relaterad länk.
2. Välj en kontouppställning i fönstret **Kontouppställningsnamn**.  
3. Välj åtgärden **Redigera kontouppställning**.  
4. I fönstret **Kontouppställning** väljer du önskat kontouppställningsnamn i fältet **Namn**.
5. Välj åtgärden **Infoga konton**.  
6. Markera de konton som du vill inkludera i utdraget och välj sedan **OK**.

    Kontona infogas i kontouppställningen. Om du vill kan du ändra kolumnens layout.  
7. Välj åtgärden **Översikt**.  
8. Klicka på snabbfliken **Dimensionsfilter** och ställ in budgetfiltret på önskat filternamn.  
9. Välj **OK**.  

Nu kan du kopiera och klistra in budgetutdraget i ett kalkylblad.

## <a name="see-also"></a>Se även
[Affärsstöd](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

