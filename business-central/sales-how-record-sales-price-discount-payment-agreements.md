---
title: Registrera speciella försäljningsspriser och rabatter för kunder | Microsoft Docs
description: Beskriver hur du definierar alternativa priser och rabattavtal som du vill koppla till försäljningsdokument när du säljer till olika kunder.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: bb93853d878ec1aa9b8b0095eb89589c35610f1a
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216159"
---
# <a name="record-special-sales-prices-and-discounts"></a>Registrera speciella försäljningspriser och rabatter
> [!NOTE]
> I 2020 års utgivningscykel 2 släppte vi effektiviserade processer för att ställa in och hantera priser och rabatter. Om du är en ny kund som använder den versionen använder du den nya upplevelsen. Om du är en befintlig kund vilar din användning av den nya versionen på om administratören har aktiverat funktionsuppdateringen **Ny försäljningsprisupplevelse** i **Funktionshantering**. Mer information finns i [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management).

De pris- och rabattavtal som gäller när du säljer till olika kunder måste definieras så att de överenskomna reglerna och värdena tillämpas på försäljningsdokument.

När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[prod_short](includes/prod_short.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader. Mer information finns i [bästa prisberäkning](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

När det gäller priser kan du infoga ett särskilt försäljningspris på försäljningsrader, om en viss kombination av kund, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns. Mer information finns i avsnitten [Så här lägger du upp ett försäljningspris för en kund](#to-set-up-a-sales-price-for-a-customer) och [Beräkning av bästa pris](#best-price-calculation).  

När det gäller rabatter kan du ställa in och använda två olika typer av försäljningsrabatter:

| Rabattyp | Beskrivning |
| --- | --- |
| **Förs.radrabatt** |En beloppsrabatt som infogas på försäljningsrader, om en viss kombination av kund, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns. En procentrabatt som dras av från dokumentets summa om värdebeloppet för alla rader i ett försäljningsdokument överstiger ett viss minimivärde. |
| **Fakturarabatt** |En procentrabatt som dras av från försäljningsdokumentets summa om summan av alla rader i dokumentet överstiger ett viss minimivärde. |

Eftersom försäljningspriser och försäljningsradrabatter baseras på en kombination av artikel och kund, kan du också utföra den här konfigurationen från den artikelsida för artikeln där regler och värden gäller.

> [!TIP]  
> Om en artikel aldrig ska säljas till rabatterat pris lämnar du bara rabattfälten på artikelsidan tomma och tar inte med artikeln i några inställningar för radrabatt.

I fälten **Gäller för typ** och **Gäller för nr.** kan du välja vad den här prislistan ska gälla för, till exempel kund- eller kundprisgrupp. Med **Visa kolumner för** kan du visa eller dölja kolumner som är relevanta för att ange priser, rabatter eller priser och rabatter.

Du kan skapa prislistor manuellt eller också använda exempelvis åtgärden **Föreslå rader** för att skapa nya priser för valda artiklar, artikelrabattgrupper, resurser och andra produkttyper. Om du väljer Föreslå rader kan du på sidan Prisrader - Skapa nytt ange filter för att välja produkter som du vill skapa nya prislistrader för. Du kan också ange om du vill överväga en minsta kvantitet vid beräkning av priser, justeringsfaktorn som ska tillämpas för nya prislistrader, samt avrundningsmetoden som ska tillämpas för priser. Med åtgärden **Kopiera rader** kan du kopiera befintliga prislistrader mellan prislistor.

Som standard är statusen för nya prislistor Utkast. När du är klar med att lägga till rader och vill att prisberäkningsmotorn ska inkludera den kan du ändra statusen till Aktiv.

Om du vill granska prislistor och priser som gäller för specifika kunder eller leverantörer går du till sidan **Kund** och väljer **Försäljningsprislistor** - alternativt kan du på sidan **Leverantör** också välja **Inköpsprislistor**. Du kan visa prislistrader i olika prislistor genom att välja **Försäljningspriser** eller **Inköpspriser** på sidorna **Artikel** och **Resurs**.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Så här skapar du försäljningspriser för en kund:

Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**.  

#### <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience/)

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Välj kund och välj sedan åtgärden **Priser**.
3. Fyll i fälten på den första raden efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja ett speciellt försäljningspris till kunden.

#### <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience/)  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Välj kunden och sedan åtgärden **Försäljningsprislistor**. 
3. Välj **Ny** för att skapa en ny försäljningsprislista.
4. På snabbflikarna **Allmänt** och **Moms** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Om du vill lägga till objekt i listan gör du något av följande:
   * Om du vill lägga till många objekt väljer du **Föreslå rader** och anger sedan filtervillkor för att ange vilka typer av objekt som ska läggas till. Du kan också ange ytterligare inställningar för de artiklar som är specifika för prislistan. Du kan ändra dessa senare vid behov.
   * Om du vill kopiera artiklar från en annan prislista väljer du **Kopiera rader** och väljer sedan den prislista som ska kopieras.
   * Om du vill lägga till artiklar manuellt väljer du fältet **Produkttyp** och den produkttyp som prislistan är avsedd för. Beroende på dina val fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Om du vill börja använda prislistan går du till fältet **Status** och väljer **Aktiv**.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Försäljningsfakturarabatter och faktureringsavgifter
När du använder fakturarabatter, avgör fakturans totala belopp storleken på rabatten. På sidan **Kundfakturarabatter** kan du även lägga till en faktureringsavgift i fakturor som överstiger ett visst belopp.  

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
Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. 

#### <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience/)  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Radrabatter**.
3. Fyll i fälten på den första raden efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja en speciell försäljningsradrabatt till kunden.

> [!Note]
> När du öppnar sidorna **Försäljningspriser** och **Försäljningsradrabatter** för en specifik kund ställs fälten **Försäljningstypfilter** och **Försäljningskodfilter** in för kunden och kan inte ändras eller tas bort.
>
> Om du vill ställa in priser eller radrabatter för alla kunder, en kundprisgrupp eller en kampanj måste du öppna sidorna från ett artikelkort. Du kan också använda sidan **Försäljningsprisförslag** för försäljningspriser. Mer information finns i [Så här uppdaterar du flera artikelpriser samtidigt](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience/)  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Välj kunden och sedan åtgärden **Försäljningsprislistor**.
3. Öppna prislistan för vilken radrabatten ska anges.
4. Aktivera växlingsknappen **Tillåt radrabatt**.
5. Skapa en ny rad eller välj en befintlig rad och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. I fältet **Definitioner** väljer du antingen **Pris och rabatt** eller bara **Rabatt**. 
7. I fältet **Radrabatt %** anger du rabattprocenten.

    > [!TIP]
    > Om du redigerar en befintlig rad kan du filtrera raderna genom att välja lämpligt alternativ i fältet **Visa kolumner för**.

    > [!NOTE]  
    > Fakturarabattkoder representeras av befintliga kundkort. Detta aktiverar dig att snabbt tilldela fakturarabattvillkor till kunder, genom att välja namnet på en andra kunder som ska ha dessa villkor. Ställ in kundspecifika villkor för fakturarabatt genom att ange fältet **Fakturarabattkod** som kundens kundkod, och fortsätt sedan till nästa steg.

8. På sidan **Kundkort** väljer du åtgärden **Fakturarabatter**. Sidan **Kundfakturarabatter** öppnas.
9. Ange valutakoden som du vill definiera fakturarabattvillkor för i fältet **Valutakod**. Lämna det här fältet tomt om du vill ange fakturarabattvillkor i din lokala valuta.
10. I fältet **Minimibelopp** kan du om du vill ange det minimibelopp som en faktura måste vara på för att komma på fråga för rabatt.
11. Fakturarabatten beräknas som en procentandel av fakturabeloppet i fältet **Rabatt %**.
12. Upprepa steg 5 till och med 7 för varje valuta som kunden ska ta emot en annan fakturarabatt för.

Fakturarabatten skapas nu och tilldelas kunden. När du väljer kundkoden i fältet **Fakturarabattkod** på andra kundkort, kopplas samma fakturarabatt till dessa kunder.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Så här definierar du radrabatt för en kund
När du har bestämt vilka kunder som är aktuella för fakturarabatter, skriver du fakturarabattkoderna på kundkorten och lägger upp villkoren för respektive kod.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna kundsidan för en kund som är aktuell för fakturarabatter.
3. Välj i fältet  **Fakturarabattkod** koden för den fakturarabatt som ska användas vid beräkning av fakturarabatter för kunden. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Fakturarabattkoder representeras av befintliga kundkort. Detta aktiverar dig att snabbt tilldela fakturarabattvillkor till kunder, genom att välja namnet på en andra kunder som ska ha dessa villkor.

Så här definierar du fakturarabattvillkor för försäljning:

1. På sidan **Kunder** väljer du åtgärden **Fakturarabatter**. Sidan **Kundfakturarabatter** öppnas.
2. Ange valutakoden som du vill definiera fakturarabattvillkor för i fältet **Valutakod**. Lämna det här fältet tomt om du vill ange fakturarabattvillkor i din lokala valuta.
3. Ange i fältet **Minimibelopp** det minsta belopp som en faktura måste vara på för att komma i fråga för rabatt.
4. Fakturarabatten beräknas som en procentandel av fakturabeloppet i fältet **Rabatt %**.
5. Upprepa steg 5 till och med 7 för varje valuta som kunden ska ta emot en annan fakturarabatt för.

## <a name="to-copy-sales-prices"></a>Så här kopierar du försäljningspriser
Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. 

#### <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience/)  

Om du vill kopiera försäljningspriser - till exempel en viss kunds försäljningspriser - och använda dem för en kundprisgrupp, måste du köra **Föreslå förs.pris i förslag**. batch-jobbet på sidan **Försäljningsprisförslag**.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsprisförslag** och välj sedan relaterad länk.  
2. Välj **Föreslå förs.pris i ändringsformulär** .  
3. På snabbfliken **Förs.priser** fyller du i fälten **Förs.typ** och **Förs.kod** för de försäljningspriser som du vill kopiera.  
4. I den övre delen av sidan fyller du i fälten **Förs.typ** och **Förs.kod** med de uppgifter som du vill kopiera försäljningspriserna till.  
5. Om du vill skapa nya priser med batch-jobbet markerar du kryssrutan **Skapa nya priser**.  
6. Klicka på knappen **OK** för att fylla i raderna på sidan **Försäljningsprisförslag** med de föreslagna nya priserna och ange att de nu gäller för den valda försäljningstypen.  

   > [!NOTE]  
   > Batch-jobbet tar bara fram förslag, det genomför inte förändringarna. Om du är nöjd med förslagen och vill använda dem, d.v.s. infoga dem på sidan **Försäljningspriser**, väljer du åtgärden **Implementera prisändringar** på sidan **Försäljningsprisförslag**.

#### <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience/)  

Statusen för prislistan måste vara **Utkast**. 

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsprislistor** och välj sedan relaterad länk. 
2. Välj den prislista som ska kopieras och välj sedan **Kopiera rader**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Du kan inte ha två rader som har samma inställningar men olika priser. Om detta händer visas ett meddelande när du aktiverar en prislista. Du kan välja det pris som ska användas genom att öppna listan och ta bort fel pris.  
  
---

## <a name="to-bulk-update-item-prices"></a>Så här uppdaterar du flera artikelpriser samtidigt
Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. 

#### <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience/)

Om du vill uppdatera flera artikelpriser samtidigt - till exempel höja alla priser med en viss procentsats - måste du köra **Föreslå artikelpris i förslag.**  batch-jobb. Du hittar en länk till batch-jobbet på sidan **Försäljningsprisförslag**.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsprisförslag** och välj sedan relaterad länk.  
2. Välj **Föreslå artikelpris i förslag** .  
3. På snabbfliken **Artikel** fyller du i fältet **Artikelnr.** eller **Lagerbokföringsmall** eller andra fält med de ursprungliga artikelpriser som du vill uppdatera.  
4. I den övre delen av sidan fyller du i fälten **Förs.typ** och **Förs.kod** med de uppgifter som du vill kopiera försäljningspriserna till.
5. Om du vill att batch-jobbet ska föreslå artikelpriset automatiskt anger du justeringen i fältet **justeringsfaktor**. Du kan till exempel ange 1,15 i **justeringsfaktor** för 15 % ökning av artikelpris.  
6. Om du vill skapa nya priser med batch-jobbet markerar du fältet **Skapa nya priser**.  
7. Klicka på **OK** för att fylla i raderna på sidan **Försäljningsprisförslag** med de föreslagna nya priserna och ange att de nu gäller för den valda **artikel**.  

> [!NOTE]
> Batch-jobbet tar bara fram förslag, det genomför inte förändringarna. Om du är nöjd med förslagen och vill använda dig av dem, d.v.s. infoga dem i tabellen **Försäljningspriser**, kan du använda batch-jobbet **Implementera prisändringar** som du hittar under fliken **Åtgärder** i gruppen **Funktioner** på sidan **Förslag för försäljningspris**.

#### <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience/)

Om du vill uppdatera priserna för flera artiklar måste du skapa en ny prislista och sedan kopiera raderna från en befintlig prislista. När du kopierar raderna kan du använda filter för att ange vad som ska kopieras, och du kan ange ett heltal eller decimaltal i fältet **Justeringsfaktor** för att höja eller sänka priserna. Statusen för prislistan måste vara **Utkast**. Om det behövs kan du sedan inaktivera den gamla prislistan.

> [!NOTE]
> Du kan inte ha två rader som har samma inställningar men olika priser. Om detta händer visas ett meddelande när du aktiverar en prislista. Du kan välja det pris som ska användas genom att öppna listan och ta bort fel pris.  

---

## <a name="best-price-calculation"></a>Bästa prisberäkning
När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[d365fin](includes/d365fin_md.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader.

Det bästa priset är det lägsta tillåtna priset med den högsta tillåtna radrabatten för ett visst datum. [!INCLUDE[d365fin](includes/d365fin_md.md)] beräknar automatiskt detta när du skriver in enhetspriset och radrabattens procentsats för artiklar på nytt dokument och journalrader.

> [!NOTE]  
> Följande beskriver hur det bästa priset beräknas för försäljning. Beräkningen är samma för inköp.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerar kombinationen av faktureringskund och artikel och beräknar sedan tillämpligt enhetspris och radrabattens procentsats utifrån följande villkor:

    - Finns det ett särskilt avtal om priser eller radrabatter för den här kunden, eller tillhör kunden en grupp som har ett sådant avtal?
    - Ingår artikeln eller artikelrabattgruppen på raden i något av dessa pris-/rabatt-avtal?
    - Ligger orderdatumet (eller fakturans och kreditnotans bokföringsdatum) inom avtalet om priser eller radrabatter?
    - Har någon enhetskod angetts? I så fall gör [!INCLUDE[d365fin](includes/d365fin_md.md)] en sökning efter priser eller rabatter med samma enhetskod och efter priser eller rabatter som saknar enhetskod.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerar huruvida pris/rabattavtal tillämpas på information i dokumentet eller på journalraden, och infogar sedan det tillämpliga enhetspriset och radrabattens procentsats enligt följande villkor:

    - Finns det krav på en lägsta kvantitet i pris-/ rabattavtalet som är uppfyllda?
    - Finns det krav på valuta i pris-/ rabattavtalet som är uppfyllda? I så fall infogas det lägsta priset och den högsta radrabatten för den valutan, även om de skulle ge ett bättre pris i lokala valutan. Om det inte finns några pris-/rabattavtal för den angivna valutakoden infogar [!INCLUDE[d365fin](includes/d365fin_md.md)] det lägsta priset och den högsta radrabatten i dina lokala valuta.

Om inga specialpriser kan beräknas för artiklarna på raden infogas antingen det senaste inköpspriset eller à-priset från artikelkortet.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]