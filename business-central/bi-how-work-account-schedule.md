---
title: "Skapa ekonomiska rapporter med hjälp av kontouppställningar"
description: "Beskriver hur du kan använda kontouppställningar för att skapa olika vyer och rapporten för att analysera ekonomisk prestandadata."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 69034b0eb97b595d0fbf5795e1fac34ecd775afe
ms.contentlocale: sv-se
ms.lasthandoff: 06/11/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Förbereda ekonomiska rapporter, kontouppställningar och kategorier
Du kan använda kontouppställningar för att få information om ekonomiska data som lagras i din kontoplan. Kontouppställningar analyserar siffror för redovisningskonton och jämför redovisningstransaktioner med redovisningsbudgettransaktioner. Resultaten visas i diagram i Rollcentret, till exempel diagram för kassaflöde och i rapporter såsom resultaträknings- och balansräkningsrapporter.

Du öppnar dessa två rapporter, till exempel med åtgärden **finansiella rapporter** på Business Manager och rollcenter för redovisare.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller några exempel på kontouppställningar som du kan använda direkt eller så kan du ange egna rader och kolumner för att jämföra siffrorna. Du kan till exempel skapa kontouppställningar för att beräkna vinstmarginaler på dimensioner som avdelningar eller kundgrupper. Du kan skapa så många anpassade finansiella rapporter som du önskar.  

Ställa in kontouppställningar kräver en förståelse för den ekonomiska informationen i kontoplanen. Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna. Detta kräver att budgetar som skapas. Mer information finns i [Skapa redovisningsbudgetar](finance-how-create-budgets.md)

## <a name="account-categories-and-account-schedules"></a>Kontokategorier och kontouppställningar
Du kan använda kontokategorier för att ändra layout på din redovisning. När du har upprättat din kontokategorier i fönstret **Redovisningskontokategorier** och du väljer åtgärden **Skapa kontouppställningar** uppdateras de underliggande kontouppställningarna för de centrala ekonomiska rapporterna. Nästa gång du kör någon av dessa rapporter, till exempel rapport för kontoavstämning kommer nya summor och underposter att läggas till, baserat på ändringarna. Mer information finns i avsnittet "Kontokategorier" i [Förstå redovisning och kontoplan](finance-general-ledger.md).  

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
> Om du inte tilldelar en standardkolumnlayout till kontouppställningen måste du  lägga upp kolumner manuellt.

### <a name="to-copy-an-existing-account-schedule"></a>Kopiera en befintlig kontouppställning
Kontouppställningar i standardversionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] utgör grunden för de ekonomiska standardrapporter, som kanske inte passar ditt företag. Du kan snabbt skapa dina egna finansiella rapporter, du kan starta genom att kopiera en befintlig kontouppställning.
1. I fönstret **kontouppställningar** markerar du en kontouppställning, och välj sedan åtgärden **kopiera kontouppställning**.
2. I fönstret **Kopiera kontouppställning** fyller du i fälten efter behov och väljer sedan knappen **OK**.

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

## <a name="comparing-accounting-periods-using-period-formulas"></a>Jämföra bokföringsperioder med hjälp av periodformler
Din kontouppställning kan jämföra resultaten av olika bokföringsperioder, till exempel den här månaden eller samma månad förra året. För att göra detta lägger du till en kolumn med fältet **Formel jämförelseperiod** fält och anger sedan fältet till en periodformel.  

En bokföringsperiod måste inte matcha kalendern, men varje räkenskapsår måste ha lika många bokföringsperioder, även om perioderna kan vara olika långa.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] använder periodformeln för att beräkna beloppet från jämförelseperioden i förhållande till perioden som representeras av datumfiltret i en rapportbegäran. Jämförelseperioden baseras på perioden för startdatumet i datumfiltret. Följande förkortningar för perioder används:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Förkortning</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>P</p></td>
<td><p>Period</p></td>
</tr>
<tr class="even">
<td><p>SP</p></td>
<td><p>Sista perioden i ett räkenskapsår, halvår eller kvartal.</p></td>
</tr>
<tr class="odd">
<td><p>CP</p></td>
<td><p>Aktuell period under räkenskapsåret, halvår eller kvartal.</p></td>
</tr>
<tr class="even">
<td><p>RÅ</p></td>
<td><p>Räkenskapsåret. Till exempel RÅ 1..3] anger det första kvartalet under aktuellt räkenskapsår.</p></td>
</tr>
</tbody>
</table>

Exempel på formler:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Formel</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;Tomt&gt;</p></td>
<td><p>Aktuell period</p></td>
</tr>
<tr class="even">
<td><p>-1P</p></td>
<td><p>Föregående period</p></td>
</tr>
<tr class="odd">
<td><p>-1RÅ[1..SP]</p></td>
<td><p>Hela föregående räkenskapsåret</p></td>
</tr>
<tr class="even">
<td><p>-1RÅ</p></td>
<td><p>Aktuell period i föregående räkenskapsår</p></td>
</tr>
<tr class="odd">
<td><p>-1RÅ[1..3]</p></td>
<td><p>Första kvartalet i föregående räkenskapsår</p></td>
</tr>
<tr class="even">
<td><p>-1RÅ[1..LP]</p></td>
<td><p>Från början på föregående räkenskapsår till och med aktuell period i föregående räkenskapsår</p></td>
</tr>
<tr class="odd">
<td><p>-1RÅ[LP..SP]</p></td>
<td><p>Från aktuell period i föregående räkenskapsår till och med sista perioden i föregående räkenskapsår</p></td>
</tr>
</tbody>
</table>

Om du vill beräkna utifrån regelbundna tidsperioder måste du skriva en formel i fältet **Jämförelse datumformel**.

> [!NOTE]
> Det är inte alltid transparent som perioder som du jämför eftersom du kan ange ett filter för en rapport som omfattar andra datum än de bokföringsperioder som återspeglas i data i kontoplanen. Exempelvis kan du skapa kontouppställningar som du vill jämföra denna period med samma period föregående år, så att du kan ange **Filter för jämförande period** till *-1FY*. Sedan kan du köra rapporten 28 februari och ange datumfilter till januari och februari. Som ett resultat jämför kontouppställningen januari och februari i år med januari föregående år, vilket är den enda avslutade bokföringsperioden av de två för föregående år.  


## <a name="see-also"></a>Se även
[Affärsstöd](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

