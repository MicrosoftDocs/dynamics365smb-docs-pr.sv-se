---
title: Skapa analysrapporter
description: 'Beskriver hur du skapar nya analysrapporter för försäljning, inköp och lager, och skapa analysmallar.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: bholtorf
---
# Skapa analysrapporter

Försäljningschefer behöver regelbundet analysera omsättning, bruttovinst och andra viktiga indikatorer på försäljningen. Inköpare är mer intresserade av dynamiken i inköpsvolymer, leverantörens kapacitet och inköpspriser. Logistik- och lagerchefer behöver i sin tur information om lageromsättning, analyser av lagerrörelser och statistik över lagervärdet. Därför finns det ingen analysrapport som passar alla.

Du kan anpassa analysrapporterna baserade på bokförda transaktioner, till exempel försäljning, inköp, överföringar och lagerjusteringar. I en anpassningsbar rapport kan källdata, som hämtas från artikeltransaktionerna (med tillhörande värdeposter), kombineras, jämföras och presenteras på ett meningsfullt och användardefinierat sätt. På detta sätt påminner analysrapporter om pivottabellrapporter i Microsoft Excel.  

Du kan t.ex. skapa en personlig rapport som fokuserar på nyckelkonton när det gäller total produktomsättning i belopp och sålda kvantiteter, bruttovinst och procentsats för bruttovinst under den aktuella månaden. Sedan kan du låta den jämföra de siffrorna med resultatet från föregående månader eller samma månad föregående år och beräkna avvikelser. Allt detta kan du göra i en och samma vy, där du också kan navigera till orsaken till identifierade problemområden och till och med välja listrutan för att fokusera på information på individuell transaktionsnivå.  

Analysrapporten består av de objekt du vill analysera (till exempel kunder, kundgrupper, säljare och så vidare) som visas som rader, samt analysparametrar, det vill säga hur du vill analysera objektet. Dessa visas som kolumner (till exempel vinstberäkningar, periodiska jämförelser av försäljningssiffror och volymer eller periodiska jämförelser av utfall och budgeterade siffror). 

Förutom analysrapporter kan du skapa och visa liknande information i analysvyer (baserade på dimensioner). Läs mer i [Analysera data efter dimensioner](bi-how-analyze-data-dimension.md).

## Exempel

Du kan lägga upp dessa rader (objekt som du vill analysera):  

- Datorer  
- Bildskärmar  
- Reservdelar  

Sedan kan du skapa dessa kolumner (hur du vill att objekten ska analyseras):  

- Försäljning innevarande månad  
- Försäljning förra månaden  
- Försäljning i procent av förra månaden  

## Lägga upp rad- och kolumnlayouter

På sidan **Analysrapport** kan du visa olika rad- och kolumnlayouter som du konfigurerar på:

* På sidan **Analysradsmallar** kan du definiera namnet på rapporten och vilka objekt som ska visas på raderna i rapporten samt
* På sidan **Analyskolumnmallar** kan du definiera namnet på kolumnmallen och de analysparametrar som du vill visa i rapporten som kolumner. Varje rad på den här sidan representerar en kolumn i rapporten. 

Observera att analysraderna och analyskolumnerna är oberoende av varandra.  

Baserat på de rader och kolumner du har lagt upp sammanställer [!INCLUDE[prod_short](includes/prod_short.md)] resultatet i rapporten på sidan **Analysrapport** som följande tabell.  

|- |Försäljning innevarande månad|Försäljning förra månaden|Försäljning förra månaden %|  
|-|-|-|-|  
|Datorer| | | |  
|Bildskärmar| | | |  
|Reservdelar| | | |  
|Summa| | | |  

Du kan till exempel lägga upp en grupp rader och flera grupper kolumnlayouter om du vill visa månadsrapporter respektive årsrapporter.

## Skapa analyskolumnmallar

Följande procedur är baserad på analysvyer för försäljning. Momentet är liknande för inköp och analysvyer.

En analyskolumnmall innehåller en uppsättning rader, där var och en representerar en analyskolumn som du vill ha i analysrapporten. När du definierar en kolumn måste du tilldela en analystypkod till en rad. Denna analystypkod bestämmer typen av källdata i artikeltransaktioner som analysen ska baseras på. Källdata kan inkludera kostnad, försäljningsbelopp eller antal och deras tillhörande värdeposter. Du kan lägga upp ett valfritt antal kolumnmallar och sedan skapa nya analysrapporter utifrån dem.    

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kolumnmallar för försäljning** och väljer sedan relaterad länk.  
2. Välj den första tomma raden och fyll sedan i fälten efter behov.
3. Välj åtgärden **Kolumner**.  
4. På sidan **Analyskolumner** fyller du sedan i fälten för att ange vilka kolumner som du vill ha i analysrapporten.  

    > [!NOTE]  
    > När du definierar en kolumn måste du fylla i fältet **Analystypkoder** för alla kolumntyper utom **Formel**. Du anger analystypkoder på sidan **Analystyper**.  
    
    Om du i fältet **Transaktionstyp** väljer **Artikeltransaktion** kopieras de faktiska värdena från artikeltransaktionen. Om du väljer **Artikelbudgettransaktioner** kopieras de budgeterade siffrorna från budgeten.  
5. Välj **OK** om du vill spara ändringarna.  

## Skapa analysradmallar

Följande procedur är baserad på en analysrapport för försäljning. Momentet är liknande för inköp och analysrapporter.

En analysradmall innehåller en uppsättning rader, där var och en representerar en analysrad som du vill ha i analysrapporten. En rad kan ange en eller ett intervall med artiklar, kunder, leverantörer eller grupper. Du kan också skapa en formel i en rad om du vill summera andra rader. Du kan lägga upp ett valfritt antal radmallar och sedan skapa nya analysrapporter utifrån dem.   

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Radmallar för försäljning** och väljer sedan relaterad länk.  
2. Välj den första tomma raden och fyll sedan i fälten efter behov.
3. Välj åtgärden **Rader**.  
4. På sidan **Analysrader** skapar du rader för artiklar, kunder, leverantörer eller säljare som du vill visa siffror för i analysrapporten. Du måste fylla i fälten **Typ**, **Intervall** och **Beskrivning**.  

> [!NOTE]  
> För att skapa många enskilda rader för varje artikel, kund och så vidare, kan du i stället välja lämpligt infogningsalternativ för att fylla i alla relevanta fält på raden. Om du vill kan du senare redigera raderna manuellt. Om du vill infoga rader väljer du åtgärden **Infoga artiklar** eller **Infoga artikelgrupper**.  

## Skapa en ny försäljningsanalysrapport

Följande procedur är baserad på en analysrapport för försäljning. Momentet är liknande för inköp och analysrapporter.

Med analysrapporter kan du analysera försäljningsdynamiken efter nyckeltal för försäljning, till exempel omsättning i både belopp och kvantitet, vinstmarginal och utfall jämfört med budget. Du kan också använda analysrapporter för att analysera genomsnittliga försäljningspriser och utvärdera säljarnas resultat.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Försäljningsanalysrapporter** och väljer sedan relaterad länk.  
2. På sidan **Analysrapportförsäljning** väljer du åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj åtgärden **Redigera analysrapport**.
5. På sidan **Försäljningsanalysrapport** väljer du åtgärden **Visa matris**.  

> [!NOTE]  
> Du kan välja kombinationer av rader och kolumnmallar för att skapa rapporter och tilldela dem unika namn. Om du gör det behöver du inte välja rad- och kolumnmallar på sidan **Försäljningsanalysrapport**. Du kan efter behov ändra rad- och kolumnmallarna i rapport och sedan återställa den ursprungliga kombinationen igen genom att välja rapporten på nytt.

## Se även

[Financial Business Intelligence](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
