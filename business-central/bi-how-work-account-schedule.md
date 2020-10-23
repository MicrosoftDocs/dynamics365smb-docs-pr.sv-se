---
title: Skapa ekonomiska rapporter med hjälp av kontouppställningar
description: Beskriver hur du kan använda kontouppställningar för att skapa olika vyer och rapporten för att analysera ekonomisk prestandadata.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 23a90d6529da231194b80f75e570e106d66a99c6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922198"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Förbereda ekonomiska rapporter, kontouppställningar och kategorier

Du kan använda kontouppställningar för att få information om ekonomiska data som lagras i din kontoplan. Kontouppställningar analyserar siffror för redovisningskonton och jämför redovisningstransaktioner med redovisningsbudgettransaktioner. Resultaten visas i diagram i Rollcentret, till exempel diagram för kassaflöde och i rapporter såsom resultaträknings- och balansräkningsrapporter.

Du öppnar dessa två rapporter, till exempel med åtgärden **finansiella rapporter** på Business Manager och rollcenter för redovisare.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller några exempel på kontouppställningar som du kan använda direkt eller så kan du ange egna rader och kolumner för att jämföra siffrorna. Du kan till exempel skapa kontouppställningar för att beräkna vinstmarginaler på dimensioner som avdelningar eller kundgrupper. Du kan skapa så många anpassade finansiella rapporter som du önskar.  

Ställa in kontouppställningar kräver en förståelse för den ekonomiska informationen i kontoplanen. Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna. Detta kräver att budgetar som skapas. Mer information finns i [Skapa redovisningsbudgetar](finance-how-create-budgets.md)

## <a name="account-schedules"></a>Kontouppställningar

Kontouppställningar används för att ordna kontona i kontoplanen på ett sätt som passar presentation av information om dem. Du kan skapa olika layouter för att definiera informationen som du vill hämta från kontoplanen. En av huvudfunktionerna hos en kontouppställning är att tillhandahålla en plats för beräkningar som inte kan göras direkt i kontoplanen, till exempel beräkningar av deltotaler för kontogrupper, vilka kan inkluderas i nya totaler som sedan i sin tur kan användas i andra totaler. Användare kan till exempel skapa kontouppställningar för att beräkna vinstmarginaler på dimensioner som avdelningar eller kundgrupper. Dessutom kan redovisningstransaktionerna och redovisningsbudgettransaktioner filtreras, till exempel efter nettoförändring eller debetbelopp.

Du kan även jämföra två eller flera kontouppställningar och kolumnlayouter med hjälp av formler. Den här typen av jämförelse ger dig möjlighet att:

* Skapa anpassade ekonomirapporter.
* Skapa så många kontouppställningar som behövs, var och en med ett unikt namn.
* Skapa olika rapportlayouter och skriva ut rapporterna med de aktuella siffrorna.

## <a name="gl-account-categories"></a>Redovisningskontokategorier

Du kan använda kontokategorier för att ändra layout på din redovisning. När du har upprättat din kontokategorier på sidan **Redovisningskontokategorier** och du väljer åtgärden **Skapa kontouppställningar** uppdateras de underliggande kontouppställningarna för de centrala ekonomiska rapporterna. Nästa gång du kör någon av dessa rapporter, till exempel rapport för **kontoavstämning** kommer nya summor och underposter att läggas till, baserat på ändringarna.

> [!NOTE]
> Konto kategorierna på den högsta nivån, till exempel noden **skulder**, är fasta och du kan inte lägga till egna. Du kan emellertid ta bort och lägga till kontokategorier på lägre nivåer och ändra deras struktur för att definiera hur det relaterade kontouppställningen ska visas i rapporter.
>
> Du bör skapa och strukturera egna redovisningskonto kategorier från grunden, i en hierarki vid behov, i stället för att försöka omarrangera de befintliga. Du kan t.ex. strukturera om **Skulder** så att de innehåller en nod **Eget kapital** följ **Kortfristiga skulder** och **Långfristiga skulder**.

## <a name="to-create-a-new-account-schedule"></a>Så här skapar du nya kontouppställningar:

Du använder kontouppställningar för att analysera siffror för redovisningskonton eller jämföra redovisningstransaktioner med redovisningsbudgettransaktioner. Du kan till exempel visa redovisningstransaktioner som procentsatser av budgettransaktionerna.

Kontouppställningar i standardversionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] utgör grunden för de ekonomiska standardrapporter, som kanske inte passar ditt företag. Du kan snabbt skapa dina egna finansiella rapporter, du kan starta genom att kopiera en befintlig kontouppställning. Se punkt 3 nedan.

Sidan **Kontouppställning översikt** är där du kan förhandsgranska den finansiella rapport som definieras i kontouppställningen. I det följande är det viktigt att förstå att det du ställer in som kontouppställningsrader och kolumner bara kan visas och godkännas på sidan **Kontouppställning översikt** som du öppnar från en kontouppställning genom att välja åtgärden **översikt**. Själva sidan **kontouppställning** är endast inställningsområde.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kontoscheman** och välj sedan relaterad länk.  
2. På sidan **Kontouppställningar** väljer du åtgärden **Ny** för att skapa ett nytt kontouppställningsnamn.
3. Alternativt väljer du åtgärden **Kopiera kontouppställning** fyller du i de två fälten och väljer sedan knappen **OK**.
4. Fyll i fälten om det behövs. I fältet **Standardkolumnlayout** väljer du en befintlig layout. Du kan redigera den senare om du vill.

    Du kan använda kolumnlayouter för att definiera kolumner för olika parametrar som ekonomiska data på raderna visas. Du kan t.ex. utforma en kolumn för att jämföra nettoförändringen för samma period innevarande och föregående år med fyra kolumner. Mer information finns i avsnittet [Att redigera en kolumnlayout](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Välj åtgärden **Redigera kontouppställning**.
6. Skapa en rad för varje ekonomisk element som du vill ska visas i rapporten, till exempel en rad för omsättningstillgångar och en annan rad för anläggningstillgångar. För inspiration, se befintliga kontouppställningar i demonstrationsföretaget CRONUS.
7. Välj åtgärden **översikt** för att se den resulterande finansiella rapporten.
8. På sidan **Kontouppställning översikt** i fältet **Kolumnlayoutnamn** väljer du en annan kolumnlayout för att visa ekonomiska data med andra parametrar.
9. Välj knappen **OK**.

Du har nu definierat basen för kontouppställningen, raderna för ekonomiska data som ska visas och en befintlig layout för kolumner för att visa data på rader per olika parametrar. Om standardkolumnlayouten som du valde i steg 4 inte passar dina önskemål, följ proceduren nedan.

### <a name="to-edit-a-column-layout"></a>Så här redigerar du en kolumnlayout

För att ange vilka kolumner som ska tas med i den resulterande rapporten använder du kolumnlayouter. Du kan t.ex. utforma en layout för att jämföra nettoförändringen för samma period innevarande och föregående år.

> [!NOTE]
> En utskriven/granskad/sparad version av en kontouppställning kan visa maximalt fem kolumner. Om kontouppställningen endast är avsedd för analys på sidan **Kontouppställning översikt** kan du skapa så många kolumner du vill.

1. På sidan **kontouppställningar**, välj relevant kontouppställning och välj sedan åtgärden **Redigera inställning av kolumnlayout**.
2. På sidan **kolumnlayouter** skapar du en rad för varje kolumn av ekonomiska data som visas i den finansiella rapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Välj knappen **OK**.
4. Öppna sidan **Kontouppställning översikt** med jämna mellanrum för att kontrollera att den nya kolumnlayouten fungerar korrekt.

> [!NOTE]
> Kolumnerna som du anger på varje rad representerar kolumnerna 3 och uppåt på sidan **Kontouppställning översikt**. De två första kolumnerna **Radnr** och **beskrivning** korrigeras.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Så här skapar du en kolumn för att beräkna procentsatser

Du kan lägga till en kolumn i en kontouppställning för att beräkna procentsatser för en summa. Om du t.ex. har ett antal rader där försäljningen delas upp per dimension kan du lägga till en kolumn för att ange procentsatsen av total försäljning som varje rad representerar.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kontoscheman** och välj sedan relaterad länk.
2. På sidan **Kontouppställningsnamn** väljer du kontouppställning.  
3. Välj åtgärden **Redigera kontouppställning** för att skapa en kontouppställningsrad för att beräkna den summa som procentsatserna ska baseras på .  
4. Infoga en rad direkt ovanför den första raden för vilken du vill visa en procentsats.  
5. Fyll i fälten på raden på följande sätt: I fältet **summeringstyp** anger du **inställningsbas för procent**. I fältet **Summeringsintervall** anger du en formel för den summa som procentsatsen kommer att baseras på. Ange till exempel **11** om rad 11 innehåller den totala försäljningen.  
6. Välj åtgärden **Redigera inställning av kolumnlayout** för att ange en kolumn.  
7. Fyll i fälten på raden på följande sätt: I fältet **kolumntyp** väljer **formeln**. I fältet **Formel** anger du en formel för det belopp som du vill beräkna en procentsats för, följt av %. Om till exempel kolumn N innehåller nettoförändringen anger du **N%**.  
8. Upprepa steg 4-7 för varje grupp av kolumner som du vill dela upp per procentsats.

## <a name="to-set-up-account-schedules-with-overviews"></a>Så här skapar du kontouppställningar med översikter

Du kan använda en kontouppställning för att skapa en rapport där redovisningssiffror jämförs med redovisningsbudgetsiffror.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kontoscheman** och välj sedan relaterad länk.
2. På sidan **Kontouppställningsnamn** väljer du kontouppställning.  
3. Välj åtgärden **Redigera kontouppställning**.  
4. På sidan **Kontouppställning** väljer du önskat kontouppställningsnamn i fältet **Namn**.
5. Välj åtgärden **Infoga konton**.  
6. Markera de konton som du vill inkludera i utdraget och välj sedan **OK**.

    Kontona infogas i kontouppställningen. Om du vill kan du ändra kolumnens layout.  
7. Välj åtgärden **Översikt**.  
8. På sidan **Kontouppställning översikt**, på snabbfliken **Dimensionsfilter** ställ in budgetfiltret på önskat filternamn.  
9. Välj **OK**.  

Nu kan du kopiera och klistra in budgetutdraget i ett kalkylblad.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Jämföra bokföringsperioder med hjälp av periodformler

Din kontouppställning kan jämföra resultaten av olika bokföringsperioder, till exempel den här månaden eller samma månad förra året. Det gör du genom att öppna sidan **Kolumnlayout** och anpassa den genom att lägga till fältet **Formel jämförelseperiod** som en kolumn. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md). Du kan sedan ange att fältet ska vara en periodformel.  

En bokföringsperiod måste inte matcha kalendern, men varje räkenskapsår måste ha lika många bokföringsperioder, även om perioderna kan vara olika långa.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] använder periodformeln för att beräkna beloppet från jämförelseperioden i förhållande till perioden som representeras av datumfiltret i en rapportbegäran. Jämförelseperioden baseras på perioden för startdatumet i datumfiltret. Följande förkortningar för perioder används:

| Förkortning | Beskrivning                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Period                                                                                |
| SP           | Sista perioden i ett räkenskapsår, halvår eller kvartal.                                   |
| CP           | Aktuell period under räkenskapsåret, halvåret eller kvartalet. Använd CP i formler för att ange den period som formeln ska börja eller sluta med. Till exempel anger RÅ\[1..CP\] tiden från början av det aktuella räkenskapsåret till den aktuella perioden.|
| RÅ           | Räkenskapsåret. Till exempel anger RÅ\[1..3\] det första kvartalet av det aktuella räkenskapsåret. |

Exempel på formler:

| Formel         | Beskrivning                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Aktuell period                                                                                  |
| \-1P            | Föregående period                                                                                 |
| \-1RÅ\[1..LP\]  | Hela föregående räkenskapsåret                                                                     |
| \-1RÅ           | Aktuell period i föregående räkenskapsår                                                          |
| \-1RÅ\[1..3\]   | Första kvartalet i föregående räkenskapsår                                                           |
| \-1RÅ\[1..CP\]  | Från början av föregående räkenskapsår till och med aktuell period i föregående räkenskapsår, inklusive båda perioderna |
| \-1RÅ\[CP..LP\] | Från aktuell period i föregående räkenskapsår till och med sista perioden i föregående räkenskapsår, inklusive båda perioderna   |

Om du vill beräkna utifrån regelbundna tidsperioder måste du skriva en formel i fältet **Jämförelse datumformel**. Om fältet till exempel har värdet -1å, jämförs [!INCLUDE [prodshort](includes/prodshort.md)] med samma period 1 år tidigare.

> [!NOTE]
> Det är inte alltid transparent som perioder som du jämför eftersom du kan ange ett filter för en rapport som omfattar andra datum än de bokföringsperioder som återspeglas i data i kontoplanen. Exempelvis kan du skapa kontouppställningar som du vill jämföra denna period med samma period föregående år, så att du kan ange **Formel jämförelseperiod** till *-1RÅ*. Sedan kan du köra rapporten 28 februari och ange datumfilter till januari och februari. Som ett resultat jämför kontouppställningen januari och februari i år med januari föregående år, vilket är den enda avslutade bokföringsperioden av de två för föregående år.  

Mer information om datumformler finns i [arbeta med datum och tider för kalender](ui-enter-date-ranges.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Affärsstöd](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
