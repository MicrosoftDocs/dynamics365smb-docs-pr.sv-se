---
title: Kolumndefinitioner i ekonomiska rapporter
description: Beskriver hur kolumndefinitioner i ekonomiska rapporter fungerar.
author: kennieNP
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 488, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# Kolumndefinitioner i ekonomiska rapporter

Använd kolumndefinitioner för att ange vilka kolumner som ska tas med i rapporten. Du kan t.ex. utforma en rapportlayout för att jämföra nettoförändringen för samma period innevarande och föregående år. Du kan ha upp till 15 kolumner i en kolumndefinition. Flera kolumner är till exempel praktiskt om du t.ex. visar budgetar i tolv månader med en kolumn som visar summan.

## Skapa eller redigera en kolumndefinition

Följ dessa steg för att skapa eller redigera en kolumndefinition.

> [!NOTE]
> En utskriven, granskad och sparad version av en ekonomisk rapport visar maximalt fem kolumner. Om en ekonomisk rapport däremot endast är avsedd för analys på sidan **Ekonomisk rapport** kan du skapa så många kolumner du vill.

1. På sidan **Ekonomiska rapporter** väljer du den relevanta ekonomiska rapporten och väljer sedan åtgärden **Redigera kolumndefinition**.
1. På sidan **Kolumndefinition** skapar du en rad för varje kolumn av ekonomiska data som visas i den finansiella rapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Välj **OK**.
1. Öppna sidan **Ekonomisk rapport** med jämna mellanrum för att kontrollera att den nya kolumndefinitionen fungerar korrekt.

## Inbyggda kolumndefinitioner

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller exempel på kolumndefinitioner som hjälper dig att snabbt komma igång med att skapa ekonomirapporter som passar dina behov.

<!-- update this when we release the new templates in 24.1
| Column definition code | Description | How to use this column definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 |
-->

## Exempel: Skapa en kolumndefinition för att beräkna procentsatser

Du kanske vill lägga till en kolumn i en ekonomisk rapport för att beräkna procentsatser för en summa. Om du t. ex. har rader där försäljningen delas upp per dimension kan du lägga till en kolumn för att ange procentsatsen av total försäljning i varje rad.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 2.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ekonomiska rapporter** och väljer sedan relaterad länk.
1. På sidan **Ekonomiska rapporter** väljer du en ekonomisk rapport.  
1. Välj åtgärden **Redigera ekonomisk rapport** för att skapa en ekonomisk rapportrad för att beräkna den summa som procentsatserna ska baseras på.  
1. Lägg till en rad direkt ovanför den första raden för vilken du vill visa en procentsats.  
1. Fyll i fälten på den första raden enligt följande: 
    1. I fältet **Summeringstyp** anger du **inställningsbas för procent**. 
    1. I fältet **Summeringsintervall** anger du en formel för den summa som procentsatsen kommer att baseras på. Ange till exempel **11** om rad 11 innehåller den totala försäljningen.  
1. Välj åtgärden **Redigera kolumndefinition** för att ange en kolumn.  
1. Fyll i fälten på den första raden enligt följande. 
    1. I fältet **Kolumntyp** väljer du **Formel**. 
    1. I fältet **Formel** anger du en formel för det belopp som du vill beräkna en procentsats för, följt av procentsymbolen (%). Om kolumn N innehåller nettoförändringen anger du **N%**.  
1. Upprepa steg 4–7 för varje grupp av rader som du vill dela upp per procentsats.

## Jämföra bokföringsperioder med hjälp av periodformler

Din ekonomiska rapport kan jämföra resultaten av olika bokföringsperioder, till exempel den senaste månaden eller samma månad förra året. Det gör du genom att öppna sidan **Kolumndefinition** och anpassa den genom att lägga till fältet **Formeljämförelseperiod** som en kolumn. Lär dig hur du [anpassar arbetsytan](ui-personalization-user.md). Du kan sedan ange att fältet ska vara en periodformel.  

En bokföringsperiod måste inte stämma överens med kalendern. Men varje räkenskapsår måste ha lika många bokföringsperioder, även om perioderna kan vara olika långa.  

[!INCLUDE[prod_short](includes/prod_short.md)] använder periodformeln för att beräkna varaktigheten för jämförelseperioden i förhållande till perioden som representeras av datumfiltret i en rapport. Jämförelseperioden baseras på perioden för startdatumet i datumfiltret. I följande tabell visas förkortningarna för periodspecifikationerna.

| Förkortning | Description                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Period.                                                                                |
| SP           | Sista perioden i ett räkenskapsår, halvår eller kvartal.                                   |
| CP           | Aktuell period under räkenskapsåret, halvåret eller kvartalet. Använd CP i formler för att ange den period som formeln ska börja eller sluta med. Till exempel anger RÅ\[1..cp\] tiden från början av det aktuella räkenskapsåret till den aktuella perioden.|
| RÅ           | Räkenskapsåret. Till exempel anger RÅ\[1..3\] det första kvartalet av det aktuella räkenskapsåret. |

Exempel på formler:

| Formel | Description |
|-----|-----|
| \<Blank\>       | Aktuell period. |
| \-1P            | Föregående period.            |
| \-1RÅ\[1..LP\]  | Hela föregående räkenskapsåret.                  |
| \-1RÅ           | Aktuell period i föregående räkenskapsår.       |
| \-1RÅ\[1..3\]   | Första kvartalet i föregående räkenskapsår.        |
| \-1RÅ\[1..cp\]  | Från början av föregående räkenskapsår till och med aktuell period i föregående räkenskapsår, inklusive båda perioderna. |
| \-1RÅ\[CP..LP\] | Från aktuell period i föregående räkenskapsår till och med sista perioden i föregående räkenskapsår, inklusive båda perioderna.   |

Om du vill beräkna utifrån regelbundna tidsperioder måste du skriva en formel i fältet **Jämförelse datumformel**. Om fältet till exempel har värdet -1å, jämför [!INCLUDE [prod_short](includes/prod_short.md)] med samma period 1 år tidigare.

> [!NOTE]
> Det är inte alltid självklart vilka perioder som du jämför eftersom du kan ange ett datumfilter för en rapport som omfattar andra datum än de bokföringsperioder som finns i kontoplanen. Så om du skapar en ekonomisk rapport där du vill jämföra denna period med samma period föregående år, så att du kan ställa in fältet **Formeljämförelseperiod** till **-1RÅ**. Sedan kan du köra rapporten **28 februari** och ange datumfilter till **januari och februari**. Som ett resultat jämför den ekonomiska rapporten januari och februari i år med januari föregående år, vilket är den enda avslutade bokföringsperioden av de två för föregående år.  

Läs mer i [Arbeta med kalenderdatum och tider](ui-enter-date-ranges.md).

[!INCLUDE [report-best-practices-column-defs](includes/report-best-practices-column-defs.md)]

## Importera eller exportera kolumndefinitioner för ekonomiska rapporter

Från och med utgivningscykel 1 för 2024 (version 24.1) kan du importera och exportera kolumndefinitioner för ekonomiska rapporter som RapidStart konfigurationspaket. Till exempel är konfigurationspaket användbara för att dela information med andra företag. Paketet skapas i en .rapidstart-fil, vilket komprimerar innehållet.

> [!NOTE]
> När du importerar kolumndefinitioner för ekonomiska rapporter kommer befintliga poster som har samma namn som de som importeras att bytas ut med de nya definitionerna. Konfigurationspaketet för en rapportdefinition skriver inte över befintliga rad- eller kolumndefinitioner som används i rapportdefinitionen.

Så här importerar eller exporterar du kolumndefinitioner för ekonomiska rapporter:

1. Välj ![glödlampan som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kolumndefinitioner** och väljer sedan relaterad länk.
1. Välj raddefinition och välj sedan åtgärden **Importera kolumndefinition** eller **Exportera kolumndefinition**, beroende på vad du vill göra.

## Se även

[Raddefinitioner i ekonomiska rapporter](bi-row-definitions.md)  
[Förbereda ekonomisk rapportering](bi-how-work-account-schedule.md)  
[Ekonomisk business intelligence](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
