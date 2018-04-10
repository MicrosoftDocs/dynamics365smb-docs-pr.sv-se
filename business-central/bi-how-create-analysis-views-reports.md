---
title: Skapa analysrapporter | Microsoft Docs
description: "Beskriver hur du skapar nya analysrapporter för försäljning, inköp och lager, och skapa analysmallar."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: f127cef1af857b5f50f5e14c7376941151b57e91
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
#  <a name="create-analysis-reports"></a>Skapa analysrapporter
Försäljningschefer behöver regelbundet analysera omsättning, bruttovinst och andra viktiga indikatorer på försäljningen. Inköpare är mer intresserade av dynamiken i inköpsvolymer, leverantörens kapacitet och inköpspriser. Logistik- och lagerchefer behöver i sin tur information om lageromsättning, analyser av lagerrörelser och statistik över lagervärdet.  

Du kan använda analysrapporterna när du vill skapa anpassade rapporter baserade på posterna för bokförda transaktioner, till exempel försäljning, inköp, överföringar och lagerjusteringar. I en anpassningsbar rapport kan källdata, som hämtas från artikeltransaktionerna (med tillhörande värdeposter), kombineras, jämföras och presenteras på ett meningsfullt och användardefinierat sätt. På detta sätt påminner analysrapporter om pivottabellrapporter i Microsoft Excel.  

Du kan skapa personanpassade rapporter som fokuserar på dina nyckelkonton utifrån total omsättning både i belopp och sålt antal, bruttovinst och bruttovinstprocent under aktuell månad, samt jämföra dessa siffror med resultatet från tidigare månader eller samma månad förra året och sedan beräkna avvikelser. Allt detta kan du göra i en och samma vy, där du också kan navigera till orsaken till identifierade problemområden genom att klicka på listrutan och få tillgång till information på individuell transaktionsnivå.  

Analysrapporten består av de objekt du vill analysera (till exempel kunder, kundgrupper, säljare, och så vidare) som visas som rader, samt analysparametrar, det vill säga hur du vill analysera objektet. Dessa visas som kolumner (till exempel vinstberäkningar, periodiska jämförelser av försäljningssiffror och volymer eller periodiska jämförelser av utfall och budgeterade siffror).

Förutom analysrapporter, kan du skapa och visa liknande information i analys, som baseras på dimensioner. Mer information finns i [Analysera data efter dimension](bi-how-analyze-data-dimension.md).

## <a name="example"></a>Exempel  
Du kan lägga upp rader så här:  
- Datorer  
- Bildskärmar  
- Reservdelar  

Sedan kan du lägga upp kolumner så här:  

- Försäljning innevarande månad  
- Försäljning förra månaden  
- Försäljning i procent av förra månaden  

## <a name="setting-up-line-and-column-layouts"></a>Lägga upp rad- och kolumnlayout  
 I fönstret **Analysrapport** kan du visa olika rad- och kolumnlayouter efter vad du har lagt upp. Du lägger upp rader eller radmallar i fönstret **Analysradmallar**. I det här fönstret kan du definiera namnet på rapporten och vilka objekt som ska visas på raderna i rapporten. Du lägger upp kolumner i fönstret **Analyskolumnmallar**. I det här fönstret kan du definiera namnet på kolumnmallen och de analysparametrar som du vill visa i rapporten som kolumner. I fönstret **Analyskolumnmallar** representerar varje rad en kolumn i rapporten. Observera att analysraderna och analyskolumnerna är oberoende av varandra.  

Baserat på de rader och kolumner du har lagt upp sammanställs resultatet i rapporten i fönstret **Analysrapport** med hjälp av en matris som kan se ut så här:  

| |Försäljning innevarande månad|Försäljning förra månaden|Försäljning förra månaden %|  
|-|-|-|-|  
|Datorer| | | |  
|Bildskärmar| | | |  
|Reservdelar| | | |  
|Summa| | | |  

 Du kan till exempel lägga upp en uppsättning rader och flera uppsättningar kolumnlayouter om du vill visa månadsrapporter respektive årsrapporter.

 ## <a name="to-set-up-analysis-column-templates"></a>Så här skapar du analyskolumnmallar
Följande procedur är baserad på en analysvy för försäljning. Momentet är liknande för inköp och analysvyer.

I en analysrapport visas analysparametrarna som kolumner. Du kan definiera vilka kolumner som ska ingå i analysrapporten genom att lägga upp analyskolumnmallar.  

En mall innehåller en uppsättning rader där var och en representerar de analyskolumner som finns i analysrapporten. När du definierar en kolumn måste du tilldela en analystypkod till en rad. Denna analystypkod bestämmer typen av källdata i artikeltransaktioner som analysen ska baseras på. Källdata inkluderar kostnad, försäljningsbelopp eller antal och deras tillhörande värdeposter. Du kan lägga upp ett valfritt antal kolumnmallar och sedan skapa nya analysrapporter utifrån dem.    

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport") ange **Kolumnmallar för försäljning** och välj sedan relaterad länk.  
2. Välj den första tomma raden och fyll sedan i fälten efter behov.
3. Välj åtgärden **Kolumner**.  
4. I fönstret **Analyskolumner** fyller du sedan i fälten för att ange vilka kolumner som ska ingå i analysrapporten.  

    > [!NOTE]  
    >   När du definierar en kolumn måste du fylla i fältet **Analystypkoder** för alla kolumntyper utom **Formel**. Du anger analystypkoder i fönstret **Analystyper**.  
    Om du i fältet **Transaktionstyp** väljer **Artikeltransaktion** kopieras de faktiska värdena från artikeltransaktionen. Om du väljer **Artikelbudgettransaktioner** kopieras de budgeterade siffrorna från budgeten.  
5.  Välj **OK** för att spara ändringar.  

## <a name="to-set-up-analysis-line-templates"></a>Så här skapar du analysradmallar  
Följande procedur är baserad på en analysrapport för försäljning. Momentet är liknande för inköp och analysrapporter.

I en analysrapport visas analysobjekten på raderna. Du kan definiera vilka rader som ska ingå i analysrapporten genom att lägga upp analysradmallar.  

En mall innehåller en uppsättning rader som representerar de analysrader som finns i analysrapporten. En rad kan ange en eller ett intervall med artiklar, kunder, leverantörer eller grupper. Du kan också skapa en formel i en rad om du vill summera andra rader. Du kan lägga upp ett valfritt antal radmallar och sedan skapa nya analysrapporter utifrån dem.    

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport") ange **Kolumnmallar för försäljning** och välj sedan relaterad länk.  
2. Välj den första tomma raden och fyll sedan i fälten efter behov.
3. Välj åtgärden **Rader**.  
4. I fönstret **Analysrader** skapar du rader för artiklar, kunder, leverantörer eller säljare som du vill visa siffror för i analysrapporten. Du måste fylla i fälten **Typ**, **Intervall** och **Beskrivning**.  

> [!NOTE]  
>   När du vill skapa många enskilda rader för varje artikel, kund och så vidare, kan du i stället välja lämpligt infogningsalternativ för att fylla i alla relevanta fält på raden. Om du vill kan du senare redigera raderna manuellt. Om du vill infoga rader välj åtgärden **Infoga artiklar** eller **Infoga artikelgrupper**.  

## <a name="to-create-a-new-sales-analysis-report"></a>Så här skapar du en ny försäljningsanalysrapport
Följande procedur är baserad på en analysrapport för försäljning. Momentet är liknande för inköp och analysrapporter.

Du använder analysrapporter för att analysera försäljningsdynamiken efter nyckeltal för försäljning som du själv väljer, till exempel omsättning i både belopp och kvantitet, vinstmarginal eller utfall jämfört med budget. Du kan också använda rapporten för att analysera genomsnittliga försäljningspriser och utvärdera säljarnas resultat.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport") ange **Kolumnmallar för försäljning** och välj sedan relaterad länk.  
2. I fönstret **Analysrapportförsäljning** väljer du åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj åtgärden **Redigera analysrapport**.
5. I fönstret **Försäljningsanalysrapport** väljer du åtgärden **Visa matris**.  

> [!NOTE]  
>   Du kan välja kombinationer av rader och kolumnmallar för att skapa rapporter och tilldela dem unika namn. När du sedan väljer ett rapportnamn slipper du välja rad- eller kolumnmallar i fönstret **Försäljningsanalysrapport**. Du kan efter behov ändra rad- och kolumnmallarna i rapport och sedan återställa den ursprungliga kombinationen igen genom att välja rapporten på nytt.

## <a name="see-also"></a>Se även
[Affärsstöd](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

