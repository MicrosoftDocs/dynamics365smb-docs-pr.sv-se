---
title: Konfigurera priser och rabatter
description: Beskriver hur du definierar standard- och specialpris- och rabattavtal för försäljning och inköp.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: article
ms.search.keywords: 'price, pricing, discount, discounting, rebate, sale, purchase, invoice'
ms.search.form: '459, 460, 7001, 7011, 7015, 7016, 7017, 7018'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-prices-and-discounts"></a>Konfigurera priser och rabatter

> [!NOTE]
> Under 2020 års utgivningscykel 2 släppte vi effektiviserade processer för att ställa in och hantera priser och rabatter. Om du är en ny kund som använder den versionen använder du den nya upplevelsen. Om du är en befintlig kund vilar din användning av den nya versionen på om administratören har aktiverat funktionsuppdateringen **Ny försäljningsprisupplevelse** på sidan **Funktionshantering**. Mer information finns i [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management).

Pris- och rabattstrategier för inköp och försäljning av artiklar och tjänster är grundläggande verktyg för framgångsrika företag. När du har ställt in de artiklar och tjänster som ditt företag köper och säljer kan du definiera vad du betalar eller debiterar för dem, och dessa belopp läggs automatiskt till i försäljnings- och inköpsdokument. 

## <a name="setting-up-prices-and-discounts"></a>Ställa in priser och rabatter

Innan du skapar prislistor måste du definiera dina prissättnings- och rabattstrategier på sidorna **Inställningar för försäljning och kundreskontra** och **Inställningar för inköp och skulder**.

Du kan ställa in och använda två olika typer av rabatter:

| Rabattyp | Beskrivning |
| --- | --- |
| **Radrabatt** |Ett rabattbelopp som anges för rader i försäljnings- och inköpsdokument. Vanligtvis baseras radrabatter på en kombination av kund, artikel, minsta kvantitet, enhet eller tidsperiod som du definierar för försäljning och inköp på sidorna **Inställningar för försäljning och kundreskontra** och **Inställningar för inköp och skulder**.|
| **Fakturarabatt** |En procentrabatt som dras av från försäljnings- och inköpsdokumentets summa om summan av alla rader i dokumentet överstiger ett viss minimivärde. |

Eftersom försäljningspriser och försäljningsradrabatter baseras på en kombination av artikel och kund, kan du också utföra den här konfigurationen från den artikelsida för artikeln där regler och värden gäller.

> [!TIP]  
> Om en artikel aldrig ska säljas till rabatterat pris lämnar du bara rabattfälten på artikelsidan tomma och tar inte med artikeln i några inställningar för radrabatt.

## <a name="about-price-lists"></a>Om prislistor

Prislistor är flexibla och låter dig ange den affärspartner eller aktivitet som de gäller för. Du kan till exempel ställa in en prislista som gäller för alla leverantörer och kunder, eller erbjuda specialpriser eller rabatter för varje affärspartner, kanske baserat på en minsta kvantitet på inköps- eller försäljningsorder, eller en viss kombination av kund, artikel, minsta kvantitet, enhet eller tidsperioder. De priser och rabatter som du definierar tillämpas automatiskt på inköps- och försäljningsdokument. 

## <a name="set-up-prices"></a>Ställ in priser

Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. 

#### [Aktuell upplevelse](#tab/current-experience)  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Välj kund och välj sedan åtgärden **Priser**.
3. Fyll i fälten på den första raden efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja ett speciellt försäljningspris till kunden.

#### [Ny upplevelse](#tab/new-experience)  

Du kan lägga till artiklar och tjänster manuellt för respektive rad, eller också använda åtgärden **Föreslå rader** för att skapa nya priser för valda artiklar, artikelrabattgrupper, resurser och andra produkttyper. Om du väljer **Föreslå rader** kan du på sidan **Prisrader – Skapa Nytt** använda filter för att välja de artiklar eller tjänster som ska inkluderas i prislistan. Du kan också ange om du vill överväga en minsta kvantitet vid beräkning av priser, justeringsfaktorn som ska tillämpas för nya prislistrader, samt avrundningsmetoden som ska tillämpas för priser. 

Som standard är statusen för nya prislistor **Utkast**. När du är redo att börja använda listan kan du ändra statusen till **Aktiv**.

Om du vill granska prislistor och priser som gäller för specifika kunder eller leverantörer går du till sidan **Kund** eller **Leverantör** och väljer antingen åtgärden **Försäljningsprislistor** eller **Inköpsprislistor**. För artiklar och resurser kan du visa prislistrader genom att välja **Försäljningspriser** eller **Inköpspriser** på sidorna **Artikel** och **Resurs**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Välj kunden och sedan åtgärden **Försäljningsprislistor**. 
3. Välj **Ny** för att skapa en ny försäljningsprislista.
4. På snabbflikarna **Allmänt** och **Moms** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Om du vill lägga till objekt i listan gör du något av följande:
   * Om du vill lägga till många objekt väljer du **Föreslå rader** och anger sedan filtervillkor för att ange vilka typer av objekt som ska läggas till. Du kan också ange ytterligare inställningar för de artiklar som är specifika för prislistan. Du kan ändra dessa senare vid behov.
   * Om du vill kopiera artiklar från en annan prislista väljer du **Kopiera rader** och väljer sedan den prislista som ska kopieras.
   * Om du vill lägga till artiklar manuellt väljer du fältet **Produkttyp** och den produkttyp som prislistan är avsedd för. Beroende på dina val fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Om du vill börja använda prislistan går du till fältet **Status** och väljer **Aktiv**.  

---

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Så här skapar du försäljningsradrabatter för en kund

Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. 

#### [Aktuell upplevelse](#tab/current-experience/)  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Radrabatter**.
3. Fyll i fälten på den första raden efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja en speciell försäljningsradrabatt till kunden.

> [!Note]
> När du öppnar sidorna **Försäljningspriser** och **Försäljningsradrabatter** för en specifik kund ställs fälten **Försäljningstypfilter** och **Försäljningskodfilter** in för kunden och kan inte ändras eller tas bort.
>
> Om du vill ställa in priser eller radrabatter för alla kunder, en kundprisgrupp eller en kampanj måste du öppna sidorna från ett artikelkort. Du kan också använda sidan **Försäljningsprisförslag** för försäljningspriser. Mer information finns i [Så här uppdaterar du flera artikelpriser samtidigt](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### [Ny upplevelse](#tab/new-experience/)  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Välj kunden och sedan åtgärden **Försäljningsprislistor**.
3. Öppna prislistan för vilken radrabatten ska anges.
4. Aktivera växlingsknappen **Tillåt radrabatt**.
5. Skapa en ny rad eller välj en befintlig rad och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. I fältet **Definitioner** väljer du antingen **Pris och rabatt** eller bara **Rabatt**. 
7. I fältet **Radrabatt %** anger du rabattprocenten.

   > [!TIP]
   > Om du redigerar en befintlig rad kan du filtrera raderna genom att välja lämpligt alternativ i fältet **Visa kolumner för**.

---

## <a name="work-with-invoice-discounts-and-service-charges"></a>Arbeta med fakturarabatter och faktureringsavgifter

När du använder fakturarabatter, avgör det fakturerade beloppets storlek hur stor rabatt som ges. På sidan **Fakturarabatter** kan du även lägga till en faktureringsavgift i fakturor som överstiger ett visst belopp.  <!--The Invoice Discounts page is hard to find.-->

Innan du kan använda fakturarabatter vid försäljning måste du ange en del information i programmet. Du måste bestämma vilka kunder som ska beviljas den här typen av rabatt och vilka rabattprocentsatser du ska använda.  

Om du fakturerar rabatter till att beräknas automatiskt kan du ange detta på sidan **Försäljningsinställningar**.  

För varje kund kan du ange om fakturarabatt ska ges i de fall villkoren uppfylls (d.v.s. om fakturabeloppet överstiger angivet belopp). Du kan definiera fakturarabattvillkoren i lokal valuta för inrikes kunder och i utländsk valuta för kunder i utlandet.  

Du kan koppla rabattprocentsatser till särskilda fakturabelopp på sidan **Fakturarabatter**. Du kan ange så många procentsatser som du behöver. Varje enskild kund han ha en egen sida, eller också kan du koppla flera kunder till samma sida.  

Förutom (eller i stället för) en procentuell rabatt kan du koppla en faktureringsavgift till ett särskilt fakturabelopp.  

> [!TIP]  
> Innan du börjar ange den här informationen är det en bra idé att förbereda din rabattstruktur i förväg, så det blir lättare att se vilka kunder som ska länkas till samma fakturarabattsida. Mer information om rabatter i Sales finns i [Ställa in rabatter för dina kunder](/training/modules/customer-discounts-dynamics-365-business-central/index).

### <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Så här definierar du radrabatt för en kund

När du har bestämt vilka kunder som är aktuella för fakturarabatter, anger du fakturarabattkoderna på kundkorten och anger villkoren för respektive kod.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Öppna kundsidan för en kund som är aktuell för fakturarabatter.
3. Välj i fältet  **Fakturarabattkod** koden för den fakturarabatt som ska användas vid beräkning av fakturarabatter för kunden. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Fakturarabattkoder representeras av befintliga kundkort. Detta aktiverar dig att snabbt tilldela fakturarabattvillkor till kunder, genom att välja namnet på en andra kunder som ska ha dessa villkor.

Så här definierar du fakturarabattvillkor för försäljning:

1. På sidan **Kunder** väljer du åtgärden **Fakturarabatter**. Sidan **Kundfakturarabatter** öppnas.
2. Ange valutakoden som du vill definiera fakturarabattvillkor för i fältet **Valutakod**. Lämna det här fältet tomt om du vill ange fakturarabattvillkor i SEK.
3. Ange i fältet **Minimibelopp** det minsta belopp som en faktura måste vara på för att komma i fråga för rabatt.
4. Fakturarabatten beräknas som en procentandel av fakturabeloppet i fältet **Rabatt %**.
5. Upprepa steg 5 till och med 7 för varje valuta som kunden ska ta emot en annan fakturarabatt för.

Fakturarabatten ställs nu in i fältet och fördelas till kunden i fråga. När du väljer kundkoden i fältet **Fakturarabattkod** på andra kundkort, kopplas samma fakturarabatt till dessa kunder.

## <a name="to-copy-sales-prices"></a>Så här kopierar du försäljningspriser

Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. 

#### [Aktuell upplevelse](#tab/current-experience/)  

Om du vill kopiera försäljningspriser – till exempel en viss kunds försäljningspriser – och använda dem för en kundprisgrupp, måste du köra **Föreslå förs.pris i förslag**. batch-jobbet på sidan **Försäljningsprisförslag**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäljningsprisförslag** och väljer sedan relaterad länk.  
2. Välj **Föreslå förs.pris i ändringsformulär** .  
3. På snabbfliken **Förs.priser** fyller du i fälten **Förs.typ** och **Förs.kod** för de försäljningspriser som du vill kopiera.  
4. I den övre delen av sidan fyller du i fälten **Förs.typ** och **Förs.kod** med de uppgifter som du vill kopiera försäljningspriserna till.  
5. Om du vill skapa nya priser med batch-jobbet markerar du kryssrutan **Skapa nya priser**.  
6. Klicka på knappen **OK** för att fylla i raderna på sidan **Försäljningsprisförslag** med de föreslagna nya priserna och ange att de nu gäller för den valda försäljningstypen.  

   > [!NOTE]  
   > Batch-jobbet tar bara fram förslag, det genomför inte förändringarna. Om du är nöjd med förslagen och vill använda dem, d.v.s. infoga dem på sidan **Försäljningspriser**, väljer du åtgärden **Implementera prisändringar** på sidan **Försäljningsprisförslag**.

#### [Ny upplevelse](#tab/new-experience/)  

Statusen för prislistan måste vara **Utkast**. 

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäljningsprislistor** och väljer sedan relaterad länk. 
2. Välj den prislista som ska kopieras och välj sedan **Kopiera rader**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Du kan inte ha två rader som har samma inställningar men olika priser. Om detta händer visas ett meddelande när du aktiverar en prislista. Du kan välja det pris som ska användas genom att öppna listan och ta bort fel pris.  
  
---

## <a name="to-bulk-update-item-prices"></a>Så här uppdaterar du flera artikelpriser samtidigt

Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. 

#### [Aktuell upplevelse](#tab/current-experience/)

Om du vill uppdatera flera artikelpriser samtidigt – till exempel höja alla priser med en viss procentsats – måste du köra **Föreslå artikelpris i förslag.** batch-jobb. Du hittar en länk till batch-jobbet på sidan **Försäljningsprisförslag**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Försäljningsprisförslag** och väljer sedan relaterad länk.  
2. Välj **Föreslå artikelpris i förslag** .  
3. På snabbfliken **Artikel** fyller du i fältet **Artikelnr.** eller **Lagerbokföringsmall** eller andra fält med de ursprungliga artikelpriser som du vill uppdatera.  
4. I den övre delen av sidan fyller du i fälten **Förs.typ** och **Förs.kod** med de uppgifter som du vill kopiera försäljningspriserna till.
5. Om du vill att batch-jobbet ska föreslå artikelpriset automatiskt anger du justeringen i fältet **justeringsfaktor**. Du kan till exempel ange 1,15 i **justeringsfaktor** för 15 % ökning av artikelpris.  
6. Om du vill skapa nya priser med batch-jobbet markerar du fältet **Skapa nya priser**.  
7. Klicka på **OK** för att fylla i raderna på sidan **Försäljningsprisförslag** med de föreslagna nya priserna och ange att de nu gäller för den valda **artikel**.  

> [!NOTE]
> Batch-jobbet tar bara fram förslag, det genomför inte förändringarna. Om du är nöjd med förslagen och vill använda dig av dem, d.v.s. infoga dem i tabellen **Försäljningspriser**, kan du använda batch-jobbet **Implementera prisändringar** som du hittar under fliken **Åtgärder** i gruppen **Funktioner** på sidan **Förslag för försäljningspris**.

#### [Ny upplevelse](#tab/new-experience/)

Om du vill uppdatera priserna för flera artiklar måste du skapa en ny prislista och sedan kopiera raderna från en befintlig prislista. När du kopierar raderna kan du använda filter för att ange vad som ska kopieras, och du kan ange ett heltal eller decimaltal i fältet **Justeringsfaktor** för att höja eller sänka priserna. Statusen för prislistan måste vara **Utkast**. Om det behövs kan du sedan inaktivera den gamla prislistan.

> [!NOTE]
> Du kan inte ha två rader som har samma inställningar men olika priser. Om detta händer visas ett meddelande när du aktiverar en prislista. Du kan välja det pris som ska användas genom att öppna listan och ta bort fel pris.  

---

## <a name="calculating-the-best-price"></a>Beräkna bästa pris

När du har registrerat särskilda priser och radrabatter för försäljning och inköp ser [!INCLUDE[d365fin](includes/d365fin_md.md)] till att din vinst på artikelhandeln alltid är optimal, detta genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument, samt i jobb- och artikeljournalrader. Mer information finns i [Bästa prisberäkning](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

## <a name="see-also"></a>Se även

[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
