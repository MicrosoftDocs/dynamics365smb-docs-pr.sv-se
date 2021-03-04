---
title: Registrera speciella försäljningsspriser och rabatter för kunder | Microsoft Docs
description: Beskriver hur du definierar alternativa priser och rabattavtal som du vill koppla till försäljningsdokument när du säljer till olika kunder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0873c45262dd9606ac187f5aab07b09677f6c1c8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035612"
---
# <a name="record-special-sales-prices-and-discounts"></a>Registrera speciella försäljningspriser och rabatter

De olika pris- och rabattavtalen som gäller när du säljer till olika kunder måste definieras så att de överenskomna reglerna och värdena tillämpas på de försäljningsdokument som du skapar för kunden.

När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[prod_short](includes/prod_short.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader. Mer information finns i [bästa prisberäkning](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

När det gäller priser kan du infoga ett särskilt försäljningspris på försäljningsrader, om en viss kombination av kund, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns. Mer information finns i avsnitten [Så här lägger du upp ett försäljningspris för en kund](#to-set-up-a-sales-price-for-a-customer) och [Beräkning av bästa pris](#best-price-calculation).  

När det gäller rabatter kan du ställa in och använda två olika typer av försäljningsrabatter:

| Rabattyp | Beskrivning |
| --- | --- |
| **Förs.radrabatt** |En beloppsrabatt som infogas på försäljningsrader, om en viss kombination av kund, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns. En procentrabatt som dras av från dokumentets summa om värdebeloppet för alla rader i ett försäljningsdokument överstiger ett viss minimivärde. |
| **Fakturarabatt** |En procentrabatt som dras av från dokumentets summa om värdebeloppet för alla rader i ett inköpsdokument överstiger ett viss minimivärde. |

Eftersom försäljningsradrabatter och försäljningspriser baseras på en kombination av artikel och kund, kan du också utföra den här konfigurationen från artikelkortet för artikeln när reglerna och värdena gäller.

> [!NOTE]  
> Om du inte vill att en artikel någonsin ska säljas till rabatterat pris, lämna bara rabattfält på artikelkortet tomt och inte ta med artikeln i någon inställning för radrabatt.

## <a name="sales-invoice-discounts-and-service-charges"></a>Försäljningsfakturarabatter och faktureringsavgifter

När du använder fakturarabatter, avgör det fakturerade beloppets storlek hur stor rabatt som ges.  

På sidan **Kundfakturarabatter** kan du även lägga till en faktureringsavgift i fakturor som överstiger ett visst belopp.  

Innan du kan använda fakturarabatter vid försäljning måste du ange viss information. Du måste bestämma följande:  

- vilka kunder som ska erhålla den här typen av rabatt  
- vilka rabattsatser i procent som ska användas  

Om du vill att fakturarabatter beräknas automatiskt kan du ange detta på sidan **Försäljningsinställningar**.  

För varje kund kan du ange om fakturarabatt ska ges i de fall villkoren uppfylls (d.v.s. om fakturabeloppet överstiger angivet belopp). Du kan definiera fakturarabattvillkoren i lokal valuta för inrikes kunder och i utländsk valuta för kunder i utlandet.  

Du kan koppla rabattsatser i procent till särskilda fakturabelopp på sidan **Kundfakturarabatter** för respektive kund. Du kan ange ett obegränsat antal rabattsatser. Alternativt kan du koppla flera kunder till samma sida.  

Förutom (eller i stället för) en procentuell rabatt kan du koppla en faktureringsavgift till ett särskilt fakturabelopp.  

> [!TIP]  
> Innan du anger den här informationen kan det vara praktiskt att skapa ett utkast av den rabattstruktur som du vill använda. På så sätt blir det enklare att se vilka kunder som kan kopplas till samma fakturarabattsida. Ju färre sidor som behöver definieras, ju snabbare går det att ange basinformationen.

För utbildning inom försäljningsrabatter, se [Ställa in rabatter för dina kunder](/learn/modules/customer-discounts-dynamics-365-business-central/index) på Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Beräkna fakturarabatter på försäljning

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Så här skapar du försäljningsradrabatter för en kund

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Radrabatter.**.

    På fältet **försäljningsradrabatter** förifylls fältet **Försäljningstyp** med **Kund** och fältet **Försäljningskod** förifylls med kundnumret.
3. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja en speciell försäljningsradrabatt till kunden.

> [!Note]
> När du öppnar fönstren **Förs.priser** och **Förs.radrabatter** från en specifik kund, ställs fälten **Förs.typfilter** och **Förs.kodfilter** in för kunden och kan inte ändras eller tas bort, vilket anges med det nedtonade värdet i fältet **Förs.kodfilter**.
>
> Om du vill ställa in priser eller radrabatter för alla kunder, en kundprisgrupp eller en kampanj måste du öppna fönstren från ett artikelkort. Du kan också använda sidan **Försäljningsprisförslag** för försäljningspriser. Mer information finns i [Så här uppdaterar du flera artikelpriser samtidigt](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices)priser.  

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Så här definierar du radrabatt för en kund

När du har bestämt vilka kunder som är aktuella för fakturarabatter, skriver du fakturarabattkoderna på kundkorten och lägger upp villkoren för respektive kod.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna kundkortet för en kund som är aktuell för fakturarabatter.
3. Välj i fältet  **Fakturarabattkod** koden för den fakturarabatt som ska användas vid beräkning av fakturarabatter för kunden.

    > [!NOTE]  
    > Fakturarabattkoder representeras av befintliga kundkort. Detta aktiverar dig att snabbt tilldela fakturarabattvillkor till kunder, genom att välja namnet på en andra kunder som ska ha dessa villkor. Ställ in kundspecifika villkor för fakturarabatt genom att ange fältet **Fakturarabattkod** som kundens kundkod, och fortsätt sedan till nästa steg.

4. På sidan **Kundkort** väljer du åtgärden **Fakturarabatter**. Sidan **Kundfakturarabatter** öppnas.
5. Ange valutakoden som du vill definiera fakturarabattvillkor för i fältet **Valutakod**. Lämna det här fältet tomt om du vill ange fakturarabattvillkor i SEK.
6. I fältet **Minimibelopp** kan du om du vill ange det minimibelopp som en faktura måste vara på för att komma på fråga för rabatt.
7. Fakturarabatten beräknas som en procentandel av fakturabeloppet i fältet **Rabatt %**.
8. Upprepa steg 5 till och med 7 för varje valuta som kunden ska ta emot en annan fakturarabatt för.

Fakturarabatten ställs nu in i fältet och fördelas till kunden i fråga. När du väljer kundkoden i fältet **Fakturarabattkod** på andra kundkort, kopplas samma fakturarabatt till dessa kunder.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Så här skapar du försäljningspriser för en kund:

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Priser.**.

    På fältet **Försäljningspriser** förifylls fältet **Försäljningstyp** med **Kund** och fältet **Försäljningskod** förifylls med kundnumret.
3. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja ett speciellt försäljningspris till kunden.

## <a name="to-copy-sales-prices"></a>Så här kopierar du försäljningspriser

Om du vill kopiera försäljningspriser, till exempel kopiera en viss kunds försäljningspriser och använda dem till en kundprisgrupp, måste du köra **Föreslå förs.pris i kalkylarket**. batchjobb, som du startar från sidan **Försäljningsprisförslag**.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningspriskalkylark** och välj sedan relaterad länk.  
2. Välj **Föreslå förs.pris i ändringsformulär** .  
3. På snabbfliken **Förs.priser** fyller du i fälten **Förs.typ** och **Förs.kod** för de försäljningspriser som du vill kopiera.  
4. I den övre delen av sidan fyller du i fälten **Förs.typ** och **Förs.kod** med de uppgifter som du vill kopiera försäljningspriserna till.  
5. Om du vill skapa nya priser med batch-jobbet markerar du kryssrutan **Skapa nya priser**.  
6. Klicka på knappen **OK** för att fylla i raderna på sidan **Försäljningspriskalkylark** med de föreslagna nya priserna och ange att de nu gäller för den valda försäljningstypen.  

> [!NOTE]  
> Batch-jobbet tar bara fram förslag, det genomför inte förändringarna. Om du är nöjd med förslagen och vill använda dem, d.v.s. infoga dem i **Förs.priser** väljer du åtgärden **Implementera prisändring** på sidan **Försäljningsprisförslag**.

## <a name="to-bulk-update-item-prices"></a>Så här uppdaterar du flera artikelpriser samtidigt

Om du vill uppdatera priser i bulk, till exempel ökar alla priser med vissa procentsats måste du köra **Föreslå artikelpris i förslag.**  batch-jobb. Du hittar en länk till batch-jobbet på sidan **Försäljningsprisförslag**.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningspriskalkylark** och välj sedan relaterad länk.  
2. Välj **Föreslå artikelpris i förslag** .  
3. På snabbfliken **Artikel** fyller du i fältet **Artikelnr.** eller **Lagerbokföringsmall** eller andra fält med de ursprungliga artikelpriser som du vill uppdatera.  
4. I den övre delen av sidan fyller du i fälten **Förs.typ** och **Förs.kod** med de uppgifter som du vill kopiera försäljningspriserna till.
5. Om du vill att batch-jobbet ska föreslå artikelpriset automatiskt anger du justeringen i fältet **justeringsfaktor**. Du kan till exempel ange 1,15 i **justeringsfaktor** för 15 % ökning av artikelpris.  
6. Om du vill skapa nya priser med batch-jobbet markerar du fältet **Skapa nya priser**.  
7. Klicka på **OK** för att fylla i raderna på sidan **Försäljningspriskalkylark** med de föreslagna nya priserna och ange att de nu gäller för den valda **artikel**.  

> [!NOTE]
> Batch-jobbet tar bara fram förslag, det genomför inte förändringarna. Om du är nöjd med förslagen och vill använda dig av dem, d.v.s. infoga dem i tabellen **Förs.priser**, kan du använda batch-jobbet **Implementera prisändring** som du hittar under fliken **Åtgärder** i gruppen **Funktioner** på sidan **Försäljningspris ändringsformulär**.

## <a name="best-price-calculation"></a>Bästa prisberäkning

När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[prod_short](includes/prod_short.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader.

Det bästa priset är det lägsta tillåtna priset med den högsta tillåtna radrabatten för ett visst datum. [!INCLUDE[prod_short](includes/prod_short.md)] beräknar automatiskt detta när du skriver in enhetspriset och radrabattens procentsats för artiklar på nytt dokument och journalrader.

> [!NOTE]  
> Följande beskriver hur det bästa priset beräknas för försäljning. Beräkningen är samma för inköp.

1. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerar kombinationen av faktureringskund och artikel och beräknar sedan tillämpligt enhetspris och radrabattens procentsats utifrån följande villkor:

    - Finns det ett särskilt avtal om priser eller radrabatter för den här kunden, eller tillhör kunden en grupp som har ett sådant avtal?
    - Ingår artikeln eller artikelrabattgruppen på raden i något av dessa pris-/rabatt-avtal?
    - Ligger orderdatumet (eller fakturans och kreditnotans bokföringsdatum) inom avtalet om priser eller radrabatter?
    - Har någon enhetskod angetts? I så fall gör [!INCLUDE[prod_short](includes/prod_short.md)] en sökning efter priser eller rabatter med samma enhetskod och efter priser eller rabatter som saknar enhetskod.

2. [!INCLUDE[prod_short](includes/prod_short.md)] kontrolelrar om pris/rabattavtal tillämpas på uppgifter i dokumentet eller journalen och infogar det tillämpliga enhetspriset och radrabattens procentsats enligt följande villkor:

    - Finns det krav på en lägsta kvantitet i pris-/ rabattavtalet som är uppfyllda?
    - Finns det krav på valuta i pris-/ rabattavtalet som är uppfyllda? I så fall infogas det lägsta priset och den högsta radrabatten för den valutan, även om de skulle ge ett bättre pris i lokala valutan. Om det inte finns några pris-/rabattavtal för den angivna valutakoden infogar [!INCLUDE[prod_short](includes/prod_short.md)] det lägsta priset och den högsta radrabatten i dina lokala valuta.

Om inga specialpriser kan beräknas för artiklarna på raden infogas antingen det senaste inköpspriset eller à-priset från artikelkortet.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]