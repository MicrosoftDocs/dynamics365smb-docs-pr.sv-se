---
title: "Registrera speciella försäljningsspriser och rabatter för kunder | Microsoft Docs"
description: "Beskriver hur du definierar alternativa priser och rabattavtal som du vill koppla till försäljningsdokument när du säljer till olika kunder."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3bb16f6f192e3a3ca29911cf6215fe1f00bfcb68
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-record-special-sales-prices-and-discounts"></a>Så här registrerar du speciella försäljningspriser och rabatter
De olika pris- och rabattavtalen som gäller när du säljer till olika kunder måste definieras så att de överenskomna reglerna och värdena tillämpas på de försäljningsdokument som du skapar för kunden.

När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[d365fin](includes/d365fin_md.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader. Mer information finns i avsnittet "Bästa prisberäkning".

När det gäller priser kan du infoga ett särskilt försäljningspris på försäljningsrader, om en viss kombination av kund, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns.

När det gäller rabatter kan du ställa in och använda två olika typer av försäljningsrabatter:

| Rabattyp | Beskrivning |
| --- | --- |
| **Förs.radrabatt** |En beloppsrabatt som infogas på försäljningsrader, om en viss kombination av kund, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns. En procentrabatt som dras av från dokumentets summa om värdebeloppet för alla rader i ett försäljningsdokument överstiger ett viss minimivärde. |
| **Fakturarabatt** |En procentrabatt som dras av från dokumentets summa om värdebeloppet för alla rader i ett inköpsdokument överstiger ett viss minimivärde. |

Eftersom försäljningsradrabatter och försäljningspriser baseras på en kombination av artikel och kund, kan du också utföra den här konfigurationen från artikelkortet för artikeln när reglerna och värdena gäller.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Så här skapar du försäljningspriser för en kund:
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Priser.**.

    Fältet **Förs.typ** är ifyllt med aktuell **kund** och fältet **Förs.kod** innehåller kundnumret.
3. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja ett speciellt försäljningspris till kunden.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Så här skapar du försäljningsradrabatter för en kund
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Radrabatter.**.

    Fältet **Förs.typ** är ifyllt med aktuell **kund** och fältet **Förs.kod** innehåller kundnumret.
3. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja en speciell försäljningsradrabatt till kunden.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Så här definierar du radrabatt för en kund
När du har bestämt vilka kunder som är aktuella för fakturarabatter, skriver du fakturarabattkoderna på kundkorten och lägger upp villkoren för respektive kod.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna kundkortet för en kund som är aktuell för fakturarabatter.
3. Välj i fältet  **Fakturarabattkod** koden för den fakturarabatt som ska användas vid beräkning av fakturarabatter för kunden.

    > [!NOTE]  
>   Fakturarabattkoder representeras av befintliga kundkort. Detta aktiverar dig att snabbt tilldela fakturarabattvillkor till kunder, genom att välja namnet på en andra kunder som ska ha dessa villkor.

    Så här definierar du fakturarabattvillkor för försäljning:
4. I fönstret **Kundkort** väljer du åtgärden **Fakturarabatter**. Fönstret **Kundfakturarabatter** öppnas.
5. Ange valutakoden som du vill definiera fakturarabattvillkor för i fältet **Valutakod**. Lämna det här fältet tomt om du vill ange fakturarabattvillkor i USD.
6. Ange i fältet **Minimibelopp** det minsta belopp som en faktura måste vara på för att komma i fråga för rabatt.
7. Fakturarabatten beräknas som en procentandel av fakturabeloppet i fältet **Rabatt %**.
8. Upprepa steg 5 till och med 7 för varje valuta som kunden ska ta emot en annan fakturarabatt för.

Fakturarabatten ställs nu in i fältet och fördelas till kunden i fråga. När du väljer kundkoden i fältet **Fakturarabattkod** på andra kundkort, kopplas samma fakturarabatt till dessa kunder.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Att arbeta med försäljningsfakturarabatter och faktureringsavgifter
När du använder fakturarabatter, avgör det fakturerade beloppets storlek hur stor rabatt som ges.  

I fönstret **Kundfakturarabatter** kan du även lägga till en faktureringsavgift i fakturor som överstiger ett visst belopp.  

Innan du kan använda fakturarabatter vid försäljning måste du ange en del information i programmet. Du måste bestämma:  

- vilka kunder som ska erhålla den här typen av rabatt.  
- vilka rabattsatser i procent som ska användas.  

Om du fakturerar rabatter till att beräknas automatiskt kan du ange detta i fönstret **Försäljningsinställningar**.  

För varje kund kan du ange om fakturarabatt ska ges i de fall villkoren uppfylls (d.v.s. om fakturabeloppet överstiger angivet belopp). Du kan definiera fakturarabattvillkoren i lokal valuta för inrikes kunder och i utländsk valuta för kunder i utlandet.  

Du kan koppla rabattsatser till särskilda fakturabelopp i fönstret **Kundfakturarabatter**. Varje kund kan ha ett separat fönster. Alternativt kan du koppla flera kunder till samma fönster.  

Förutom (eller i stället för) en procentuell rabatt kan du koppla en faktureringsavgift till ett särskilt fakturabelopp.  

> [!TIP]  
>  Innan du anger den här informationen i programmet kan det vara praktiskt att skapa ett utkast av den rabattstruktur som du vill använda. På så sätt blir det enklare att se vilka kunder som kan kopplas till samma fakturarabattfönster. Ju färre fönster som behöver definieras, ju snabbare går det att ange basinformationen.  

## <a name="best-price-calculation"></a>Bästa prisberäkning
När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[d365fin](includes/d365fin_md.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader.

Det bästa priset är det lägsta tillåtna priset med den högsta tillåtna radrabatten för ett visst datum. [!INCLUDE[d365fin](includes/d365fin_md.md)] beräknar automatiskt detta när du skriver in enhetspriset och radrabattens procentsats för artiklar på nytt dokument och journalrader.

> [!NOTE]  
>   Följande beskriver hur det bästa priset beräknas för försäljning. Beräkningen är samma för inköp.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerar kombinationen av faktureringskund och artikel och beräknar sedan tillämpligt enhetspris och radrabattens procentsats utifrån följande kriterier:

    - Finns det ett särskilt avtal om priser eller radrabatter för den här kunden, eller tillhör kunden en grupp som har ett sådant avtal?
    - Ingår artikeln eller artikelrabattgruppen på raden i något av dessa pris-/rabatt-avtal?
    - Ligger orderdatumet (eller fakturans och kreditnotans bokföringsdatum) inom avtalet om priser eller radrabatter?
    - Har någon enhetskod angetts? I så fall gör [!INCLUDE[d365fin](includes/d365fin_md.md)] en sökning efter priser eller rabatter med samma enhetskod och efter priser eller rabatter som saknar enhetskod.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrolelrar om pris/rabattavtal tillämpas på uppgifter i dokumentet eller journalen och infogar det tillämpliga enhetspriset och radrabattens procentsats enligt följande kriterier:

    - Finns det krav på en lägsta kvantitet i pris-/ rabattavtalet som är uppfyllda?
    - Finns det krav på valuta i pris-/ rabattavtalet som är uppfyllda? I så fall infogas det lägsta priset och den högsta radrabatten för den valutan, även om de skulle ge ett bättre pris i lokala valutan. Om det inte finns några pris-/rabattavtal för den angivna valutakoden infogar [!INCLUDE[d365fin](includes/d365fin_md.md)] det lägsta priset och den högsta radrabatten i dina lokala valuta.

Om inga specialpriser kan beräknas för artiklarna på raden infogas antingen det senaste inköpspriset eller à-priset från artikelkortet.

## <a name="to-copy-sales-prices"></a>Så här kopierar du försäljningspriser  
Om du vill kopiera försäljningspriser, till exempel kopiera en viss kunds försäljningspriser och använda dem till en kundprisgrupp, måste du köra **Föreslå förs.pris i förslaget**.  batch-jobb. Du hittar batch-jobbet i fönstret **Försäljningsprisförslag**.    

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Förs.pris ändringsformulär** och välj sedan relaterad länk.  
2.  Välj **Föreslå förs.pris i ändringsformulär** .  
3.  På snabbfliken **Förs.priser** fyller du i fälten **Förs.typ** och **Förs.kod** för de försäljningspriser som du vill kopiera.  
4.  I den övre delen av fönstret fyller du i fälten **Förs.typ** och **Förs.kod** med de uppgifter som du vill kopiera försäljningspriserna till.  
5.  Om du vill skapa nya priser med batch-jobbet markerar du fältet **Skapa nya priser**.  
6.  Klicka på **OK** för att fylla i raderna i fönstret **Försäljningsprisförslag** med de föreslagna nya priserna och ange att de nu gäller för den valda **försäljningstypen**.  

> [!NOTE]  
>  Batch-jobbet tar bara fram förslag, det genomför inte förändringarna. Om du är nöjd med förslagen och vill använda dig av dem, d.v.s. infoga dem i tabellen **Förs.priser**, kan du använda batch-jobbet **Implementera prisändring** som du hittar under fliken **Åtgärder** i gruppen **Funktioner** i fönstret **Försäljningspris ändringsformulär**.

## <a name="see-also"></a>Se även
[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

