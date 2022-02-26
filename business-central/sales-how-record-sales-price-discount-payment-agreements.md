---
title: Registrera försäljningspriser och rabatter för kunder | Microsoft Docs
description: Beskriver hur du lägger upp och använder pris-och rabattavtal för försäljningsdokument.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 1345, 7002, 7007, 7015, 7016, 7023
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 5d03e3c567ed6a2932691cee58685e522814a03f
ms.sourcegitcommit: a6000804ad9a176de5750372d3951547ddb71006
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/25/2021
ms.locfileid: "7865552"
---
# <a name="record-sales-prices-and-discounts"></a>Registrera försäljningspriser och rabatter
> [!NOTE]
> I 2020 års utgivningscykel 2 släppte vi effektiviserade processer för att ställa in och hantera priser och rabatter. Om du är en ny kund som använder den versionen använder du den nya upplevelsen. Om du är en befintlig kund vilar din användning av den nya versionen på om administratören har aktiverat funktionsuppdateringen **Ny försäljningsprisupplevelse** i **Funktionshantering**. Mer information finns i [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] har stöd för olika prissättningsstrategier, från ett pris passar alla-modeller där en artikel alltid säljs till samma pris, specialprisavtal med specifika kunder, kundgrupper eller special erbjudanden när du kör en försäljningskampanj. Du kan till exempel erbjuda ett specialpris på en försäljningsorder under följande förutsättningar:

* När det gäller ett minsta antal
* Det är för en viss typ av artikel.  
* Om den skapas under en viss tidsperiod

Om du vill använda en grundläggande prismodell behöver du bara ange ett enhetspris för en artikel eller resurs. Det priset kommer alltid att användas på försäljningsdokument. För mer avancerade modeller, till exempel när du kör en försäljningskampanj och vill erbjuda särskilda priser, kan du ange kriterier för den på sidan **försäljningspriser** . Du kan erbjuda specialpriser baserat på kombinationer av följande: 

* Kund
* Artikel
* Måttenhet
* Minimiantal
* Datumintervall som anger när priserna är giltiga

När du har lagt upp särskilda priser kan [!INCLUDE[prod_short](includes/prod_short.md)] dessutom automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och på projekt- och artikeljournalrader. Mer information finns i [bästa prisberäkning](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).  

När det gäller försäljningsrabatter kan du ställa in och använda följande typer:

| Rabattyp | Beskrivning |
| --- | --- |
| **Förs.radrabatt** |Ett belopp som infogas på försäljningsrader, om en viss kombination av kund, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns. Dessa kombinationer fungerar på samma sätt som för försäljningspriser. |
| **Fakturarabatt** |En procentrabatt som dras av från försäljningsdokumentets summa om summan av alla rader i dokumentet överstiger ett viss minimivärde. |

> [!TIP]  
> Om en artikel aldrig ska säljas till rabatterat pris lämnar du bara rabattfälten på artikelsidan tomma och tar inte med artikeln i några inställningar för radrabatt.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Så här skapar du försäljningspriser för en kund:

Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. Om funktionsuppdateringen inte är aktiverad följer du anvisningarna på fliken Aktuell upplevelse. 

## <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience)

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Välj kund och välj sedan åtgärden **Priser**.
3. Fyll i fälten på den första raden efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja ett speciellt försäljningspris till kunden.

## <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience)  
Som standard är statusen för nya prislistor Utkast. Utkast av prislistor ingår inte i prisberäkningar. När du är klar med att lägga till rader och vill börja använda priserna ändrar du statusen till Aktiv.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Välj kunden och sedan åtgärden **Försäljningsprislistor**. 
3. Välj **Ny** för att skapa en ny försäljningsprislista.
4. På snabbflikarna **Allmänt** och **Moms** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Du kan lägga till artiklar i listan på följande sätt:
   * Om du vill lägga till många objekt väljer du **Föreslå rader** och anger sedan filtervillkor för att ange vilka typer av objekt som ska läggas till. Du kan också ange andra inställningar för artiklarna. Dessa inställningar är specifika för prislistan. Du kan ändra dessa senare vid behov.
   * Om du vill kopiera artiklar från en annan prislista väljer du **Kopiera rader** och väljer sedan den prislista som ska kopieras.
   * Om du vill lägga till artiklar manuellt väljer du fältet **Produkttyp** på en rad och den produkttyp som prislistan är avsedd för. Beroende på dina val fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Om du vill börja använda prislistan går du till fältet **Status** och väljer **Aktiv**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Använda försäljnings- och inköpsprislistor
> [!NOTE]
> Om du använder prislistor måste administratören ha aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris** i **Funktionshantering**. Mer information finns i [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management).

I fälten **Gäller för typ** och **Gäller för nr.** kan du välja vad den här prislistan ska gälla för, till exempel kund- eller kundprisgrupp. Med fältet **Visa kolumner för** kan du visa eller dölja kolumner som är relevanta för att priser, rabatter eller priser och rabatter.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Konvertera befintliga priser när du aktiverar prisfunktionsuppdateringen
När du aktiverar funktionsuppdateringen **Ny upplevelse för försäljningspris** på sidan **Funktionshantering** öppnas guiden **Uppdatering av funktionsdata**. Använd växlingen **Använd standardpriserna** enligt följande:

* Aktivera det om du vill arbeta med alla priser på samma sida. Befintliga priser konverteras till en standardprislista för vart och ett av följande:

    * FÖRS
    * Inköp
    * Projektförsäljning
    * Projektinköp 

    Därefter kan du redigera alla priser för dessa områden på sidan **Prisförslag**. Standardprislistorna anges på sidorna **Försäljningsinställningar**, **Inköpsinställningar** och **Projektinställningar**. 

    > [!NOTE]
    > Om priser endast är inställda på artikel- eller resurskort fylls inte standardprislistorna i med dessa priser under datauppdateringen. Du kan dock öppna någon av standardprislistor eller pris förslags sidan och använda åtgärden **föreslå rader** för att lägga till prisuppsättningarna på artikel- eller resurskortet. 

* Om du vill använda försäljningsprislistor avmarkerar du det. Befintliga priser kommer att konverteras till en ny prislista för varje kombination av kund, kundgrupp eller kampanj samt start- och slutdatum och valutor. Om du har många kombinationer får du många prislistor.

Om du redan har aktiverat den nya prissättningen kan du skapa standardprislistor manuellt eller ange en befintlig prislista som standard. Om du vill ange en befintlig pris lista som standard aktiverar du alternativet för att **aktivera uppdateringsstandarder** på prislistan. Sidorna **Försäljningsinställningar**, **Inköpsinställningar** och **Projektinställningar** anger du prislistan som standard.

## <a name="editing-active-price-lists"></a>Redigering av aktivt prislistor
För att tillåta personer att redigera priser på aktiva prislistor för varor, resurser, kunder, leverantörer eller andra enheter som använder prissättning, aktivera växling **Tillåt redigering av aktivt pris** på sidan **Försäljningsinställningar** och **Inköpsinställningar**. 

När växlingen **Tillåt redigering av aktivt pris** är inaktiverad måste du för att uppdatera priser i en prislista ändra status för prislistan till **Utkast**, göra ändringen och sedan återaktivera prislistan.

Sidan **prisöversikt** ger en överblick över alla priser över prislistor. Du kan ange filter för att begränsa listan. När du har ändrat priserna måste du använda åtgärden **bekräfta rader** för att kontrollera priserna mot andra prislistrader. Om du t.ex. kontrollerar priserna kan du undvika dubbla eller motstridiga priser. 

> [!NOTE]
> När du redigerar en rad i en aktiv prislista blir radens status Utkast och raden inkluderas inte i prisberäkningarna förrän du använder åtgärden **bekräfta rader**. När du har kontrollerat priset blir Radens status aktiv och kommer att användas i prisberäkningar.

För att lägga till nya priser, på **Prisöversikt**, använd åtgärden **Lägg till nya rader**. Sidan **Prisförslag** öppnas där du lägger till prisrader på följande sätt:

* Genom att föreslå dem utifrån kriterier
* Kopiera dem från andra prislistor
* Ange dem manuellt. 

Efteråt kan du använda åtgärden **implementera prisändring** för att jämföra de nya priserna med andra prislistor för att undvika dubbletter.

## <a name="to-copy-sales-prices"></a>Så här kopierar du försäljningspriser
Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. Om funktionsuppdateringen inte är aktiverad följer du anvisningarna på fliken Aktuell upplevelse.

## <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience)  

Om du vill kopiera försäljningspriser - till exempel en viss kunds försäljningspriser - och använda dem för en kundprisgrupp, måste du köra **Föreslå förs.pris i förslag**. batch-jobbet på sidan **Försäljningsprisförslag**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäljningsprisförslag** och väljer sedan relaterad länk.  
2. Välj **Föreslå förs.pris i ändringsformulär** .  
3. På snabbfliken **Förs.priser** fyller du i fälten **Förs.typ** och **Förs.kod** för de försäljningspriser som du vill kopiera.  
4. I den övre delen av sidan fyller du i fälten **Förs.typ** och **Förs.kod** med de uppgifter som du vill kopiera försäljningspriserna till.  
5. Om du vill skapa nya priser med batch-jobbet markerar du kryssrutan **Skapa nya priser**.  
6. Klicka på knappen **OK** för att fylla i raderna på sidan **Försäljningsprisförslag** med de föreslagna nya priserna och ange att de nu gäller för den valda försäljningstypen.  

   > [!NOTE]  
   > Batch-jobbet tar bara fram förslag, det genomför inte förändringarna. Om du är nöjd med förslagen och vill använda dem, d.v.s. infoga dem på sidan **Försäljningspriser**, väljer du åtgärden **Implementera prisändringar** på sidan **Försäljningsprisförslag**.

## <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience)  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäljningsprislistor** och väljer sedan relaterad länk. 
2. Välj den prislista som ska kopieras och välj sedan **Kopiera rader**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Du kan inte ha två rader som har samma inställningar men olika priser. Om detta händer visas ett meddelande när du aktiverar en prislista. Du kan välja det pris som ska användas genom att öppna listan och ta bort fel pris.  
  
---

## <a name="to-bulk-update-item-prices"></a>Så här uppdaterar du flera artikelpriser samtidigt
Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. Om funktionsuppdateringen inte är aktiverad följer du anvisningarna på fliken Aktuell upplevelse.

### <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience)

Om du vill uppdatera flera artikelpriser samtidigt – till exempel höja alla priser med en viss procentsats kan du fylla i **Försäljningsprisförslag** genom att använda följande batchjobb:

* **Föreslå artikelpris i förslag** Föreslår ändringar genom att tillämpa en justeringsfaktor på befintliga försäljningspriser, eller genom att kopiera befintliga försäljningsprisavtal till andra kunder, kundprisgrupper eller försäljningskampanjer.
* **Föreslå artikelpris i förslag** föreslår ändringar genom att tillämpa en justeringsfaktor på befintliga enhetspriser på artikelkort, eller genom att föreslå priser för nya kombinationer av valuta, måttenheter och så vidare. Enhetspriserna för artiklar ändras inte.    

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäljningsprisförslag** och väljer sedan relaterad länk.  
2. Välj **Föreslå artikelpris i förslag** .  
3. På snabbfliken **Artikel** fyller du i fältet **Artikelnr.** eller **Lagerbokföringsmall** eller andra fält med de ursprungliga artikelpriser som du vill uppdatera.  
4. I den övre delen av sidan fyller du i fälten **Förs.typ** och **Förs.kod** med de uppgifter som du vill kopiera försäljningspriserna till.
5. Om du vill att batch-jobbet ska föreslå artikelpriset automatiskt anger du justeringen i fältet **justeringsfaktor**. Du kan till exempel ange **1,15** i **justeringsfaktor** för **15 %** ökning av artikelpris.  
6. Om du vill skapa nya priser med batch-jobbet markerar du växlingen **Skapa nya priser**.  
7. Välj **OK** för att fylla i raderna på sidan **försäljningsprisförslag** med de föreslagna nya priserna.
8. Använd åtgärden **implementera prisändringar** för att genomföra förslagen . Batch-jobbet skapar förslag men verkställer inte dem.

## <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience)

Om du vill uppdatera priserna för flera artiklar måste du skapa en ny prislista och sedan kopiera raderna från en befintlig prislista. När du kopierar raderna kan du använda filter för att ange vad som ska kopieras, och du kan ange ett heltal eller decimaltal i fältet **Justeringsfaktor** för att höja eller sänka priserna. Statusen för prislistan måste vara **Utkast**. Om det behövs kan du sedan inaktivera den gamla prislistan.

> [!NOTE]
> Du kan inte ha två rader som har samma inställningar men olika priser. Om detta händer visas ett meddelande när du aktiverar en prislista. Du kan välja det pris som ska användas genom att öppna listan och ta bort fel pris.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Försäljningsfakturarabatter och faktureringsavgifter
När du använder fakturarabatter, avgör fakturans totala belopp storleken på rabatten. På sidan **Kundfakturarabatter** kan du även lägga till en faktureringsavgift i fakturor som överstiger ett visst belopp.  

Om du vill att fakturarabatter beräknas automatiskt kan du ange detta på sidan **Försäljningsinställningar** aktivera växlingen **Beräkna fakturarabatt**.  

För varje kund kan du ange om du vill erbjuda faktura rabatter om villkoren är uppfyllda. Till exempel om fakturabeloppet är stort nog. Du kan definiera fakturarabattvillkoren i lokal valuta för inrikes kunder och i utländsk valuta för kunder i utlandet.  

Du kan koppla rabattsatser i procent till särskilda fakturabelopp på sidan **Kundfakturarabatter** för respektive kund. Du kan ange ett obegränsat antal rabattsatser. Varje enskild kund han ha en egen sida, eller också kan du koppla flera kunder till samma sida.  

Förutom (eller i stället för) en procentuell rabatt kan du koppla en faktureringsavgift till ett särskilt fakturabelopp.  

För utbildning inom försäljningsrabatter, se [Ställa in rabatter för dina kunder](/learn/modules/customer-discounts-dynamics-365-business-central/index) på Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Beräkna fakturarabatter på försäljning

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Så här skapar du försäljningsradrabatter för en kund
Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. Om funktionsuppdateringen inte är aktiverad följer du anvisningarna på fliken Aktuell upplevelse.

## <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience)  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Radrabatter**.
3. Fyll i fälten på den första raden efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja en speciell försäljningsradrabatt till kunden.

> [!Note]
> När du öppnar sidorna **Försäljningspriser** och **Försäljningsradrabatter** för en specifik kund ställs fälten **Försäljningstypfilter** och **Försäljningskodfilter** in för kunden och kan inte ändras eller tas bort.
>
> Om du vill ställa in priser eller radrabatter för alla kunder, en kundprisgrupp eller en kampanj måste du öppna sidorna från ett artikelkort. Du kan också använda sidan **Försäljningsprisförslag** för försäljningspriser. Mer information finns i [Så här uppdaterar du flera artikelpriser samtidigt](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

## <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience)  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Välj kunden och sedan åtgärden **Försäljningsprislistor**.
3. Öppna prislistan för vilken radrabatten ska anges.
4. Skapa en ny rad eller välj en befintlig rad och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. I fältet **Definitioner** väljer du antingen **Pris och rabatt** eller bara **Rabatt**. 
6. I fältet **Radrabatt %** anger du rabattprocenten.

   > [!TIP]
   > Du kan filtrera raderna genom att välja lämpligt alternativ i fältet **Visa kolumner för**.   
  
   > [!NOTE]
   > Fakturarabattkoder representeras av befintliga kundkort. Genom att använda kundnamn som koder aktiveras du att snabbt tilldela fakturarabattvillkor till kunder, genom att välja namnet på en andra kunder som ska ha dessa villkor. Ställ in kundspecifika villkor för fakturarabatt genom att ange fältet **Fakturarabattkod** som kundens kundkod, och fortsätt sedan till nästa steg.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Så här definierar du radrabatt för en kund
När du har bestämt vilka kunder som är aktuella för fakturarabatter, skriver du fakturarabattkoderna på kundkorten och lägger upp villkoren för respektive kod.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna kundsidan för en kund som är aktuell för fakturarabatter.
3. Välj i fältet  **Fakturarabattkod** koden för den fakturarabatt som ska användas vid beräkning av fakturarabatter för kunden. 

> [!NOTE]  
> Fakturarabattkoder representeras av befintliga kundkort. Genom att använda kundnamn som koder aktiveras du att snabbt tilldela fakturarabattvillkor till kunder, genom att välja namnet på en andra kunder som ska ha dessa villkor.

Ställ in fakturarabattvillkor för försäljning:

1. På sidan **Kunder** väljer du åtgärden **Fakturarabatter**. Sidan **Kundfakturarabatter** öppnas.
2. Ange valutakoden som du vill definiera fakturarabattvillkor för i fältet **Valutakod**. Lämna det här fältet tomt om du vill ange fakturarabattvillkor i SEK.
3. Ange i fältet **Minimibelopp** det minsta belopp som en faktura måste vara på för att komma i fråga för rabatt.
4. Fakturarabatten beräknas som en procentandel av fakturabeloppet i fältet **Rabatt %**.
5. Upprepa steg 5 till och med 7 för varje valuta som kunden ska ta emot en annan fakturarabatt för.

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