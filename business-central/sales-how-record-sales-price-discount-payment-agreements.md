---
title: Registrera speciella försäljningspriser och rabatter
description: Beskriver hur du definiera pris-och rabattavtal för försäljningsdokument.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 05/29/2024
ms.custom: bap-template
ms.search.keywords: 'special price, alternate price, pricing'
ms.search.form: '7022, 7024'
ms.service: dynamics-365-business-central
---

# <a name="record-special-sales-prices-and-discounts"></a>Registrera speciella försäljningspriser och rabatter

> [!NOTE]
> I 2020 års utgivningscykel 2 introducerade nya enkla processer för att ställa in och hantera priser och rabatter. Om du är en ny kund som använder den senaste versionen använder du den nya upplevelsen. Om du är en befintlig kund vilar din användning av den nya versionen på om administratören har aktiverat funktionsuppdateringen **Ny försäljningsprisupplevelse** i **Funktionshantering**. Lär dig mer på [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrationsinnehållet.

[!INCLUDE[prod_short](includes/prod_short.md)] stöder olika prissättnings strategier, till exempel:

* Ett pris passar alla modeller där en artikel alltid säljs med samma pris.
* Special prisavtal med specifika kunder eller kundgrupper.
* Kampanjer när en försäljning uppfyller kriterier för ett specialerbjudande. Du kan till exempel ha följande kriterier för en order:

  * Det uppfyller minimiantalet
  * Det är före ett visst datum
  * Det innehåller en viss typ av artikel  

Om du vill använda en grundläggande prismodell behöver du bara ange ett enhetspris när du anger en artikel eller resurs. Det priset kommer alltid att användas på försäljningsdokument. För mer avancerade modeller, till exempel när du vill erbjuda specialpriser för en säljkampanj kan du ange kriterier på sidan **försäljningspriser** . Du kan erbjuda specialpriser baserat på kombinationer av följande information:  

* Kund
* Artikel
* Måttenhet
* Minimiantal
* Datum som definierar perioden som priserna är giltiga för.

När du anger särskilda priser kan [!INCLUDE[prod_short](includes/prod_short.md)] dessutom kan du beräkna det bästa priset på försäljnings- och inköpsdokument och på projekt- och artikeljournaler. Läs mer på [Bästa prisberäkning](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

För försäljningsrabatter kan du ställa in två typer:

| Typ av rabatt | Description |
| --- | --- |
| **Förs.radrabatt** |Lägg till belopp som infogas på försäljningsrader som har en viss kombination av kund, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum. Denna typ fungerar på samma sätt som för försäljningspriser. |
| **Fakturarabatt** |En procentrabatt som dras av från försäljningsdokumentets summa om summan av alla rader i dokumentet överstiger ett viss minimivärde. |

> [!TIP]  
> Om en artikel aldrig ska säljas till rabatterat pris lämnar du bara rabattfälten på artikelsidan tomma och tar inte med artikeln i några inställningar för radrabatt.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Så här skapar du försäljningspriser för en kund:

Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. Om funktionsuppdateringen inte är aktiverad följer du anvisningarna på fliken Aktuell upplevelse. 

#### [Aktuell upplevelse](#tab/current-experience/)

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Välj kund och välj sedan åtgärden **Priser**.
3. Fyll i fälten på den första raden efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja ett speciellt försäljningspris till kunden.

#### [Ny upplevelse](#tab/new-experience/)  

Som standard är statusen för nya prislistor **Utkast**. Utkast av prislistor ingår inte i prisberäkningar. När du är klar med att lägga till rader och vill börja använda priserna ändrar du statusen till **Aktiv**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Välj kunden och sedan åtgärden **Försäljningsprislistor**. 
3. Välj **Ny** för att skapa en ny försäljningsprislista.
4. På snabbflikarna **Allmänt** och **Moms** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Om du vill lägga till objekt i listan gör du följande steg:
   * Om du vill lägga till många objekt väljer du **Föreslå rader** och anger sedan filtervillkor för att ange vilka typer av objekt som ska läggas till. Du kan också ange ytterligare inställningar för de artiklar som är specifika för prislistan. Du kan ändra dessa inställningar senare vid behov.
   * Om du vill kopiera artiklar från en annan prislista väljer du **Kopiera rader** och väljer sedan den prislista som ska kopieras.
   * Om du vill lägga till artiklar manuellt väljer du fältet **Produkttyp** och den produkttyp som prislistan är avsedd för. Beroende på dina val fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Om du vill börja använda prislistan går du till fältet **Status** och väljer **Aktiv**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Använda försäljnings- och inköpsprislistor

> [!NOTE]
> Om du använder prislistor måste administratören ha aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris** i **Funktionshantering**. Lär dig mer på [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrationsinnehållet.

De flesta nya försäljningspris upplevelser liknar de aktuella funktionerna, men det finns några skillnader. Dessa skillnader beskrivs i följande avsnitt.

I fälten **Gäller för typ** och **Gäller för nr.** kan du välja vad den här prislistan ska gälla för, till exempel kund- eller kundprisgrupp. Med **Visa kolumner för** kan du visa eller dölja kolumner som är relevanta för att ange priser, rabatter eller priser och rabatter.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Konvertera befintliga priser när du aktiverar prisfunktionsuppdateringen

När du aktiverar funktionsuppdateringen **Ny upplevelse för försäljningspris** på sidan **Funktionshantering** öppnas guiden **Uppdatering av funktionsdata**. Använd växlingen **Använd standardpriserna** enligt följande:

* Aktivera det om du vill arbeta med alla priser på samma sida. Befintliga priser konverteras till en standardprislista för vart och ett av följande dokument:

  * FÖRS
  * Inköp
  * Projektförsäljning
  * Projektinköp

  Du kan redigera alla priser för dessa områden på sidan **Prisförslag**. Standardprislistorna anges på sidorna **Försäljningsinställningar**, **Inköpsinställningar** och **Projektinställningar**.

> [!NOTE]
> Om priser endast är inställda på artikel- eller resurskort fylls inte standardprislistorna i med dessa priser under datauppdateringen. Du kan dock öppna någon av standardprislistorna eller sidan **Prisförslag** och använda åtgärden **Föreslå rader** för att lägga till prisuppsättningarna på artikel- eller resurskortet.

* Om du vill använda försäljningsprislistor avmarkerar du det. Befintliga priser konverteras till en ny prislista för varje kombination av följande saker:

  * Kund
  * Kundgrupp eller kampanj
  * Start- och slutdatum
  * Valutor

Om du har många kombinationer får du många prislistor.

Om du redan har aktiverat den nya prissättningen kan du skapa standardprislistor manuellt eller ange en befintlig prislista som standard. Om du vill ange en befintlig pris lista som standard aktiverar du alternativet för att **aktivera uppdateringsstandarder** på prislistan. På sidorna **Försäljningsinställningar**, **Inköpsinställningar** och **Projektinställningar** anger du prislistan som standard.

### <a name="editing-active-price-lists"></a>Redigera aktiva prislistor

För att tillåta personer att redigera priser på aktiva prislistor för varor, resurser, kunder, leverantörer eller andra enheter som använder prissättning, aktivera växling **Tillåt redigering av aktivt pris** på sidan **Försäljningsinställningar** och **Inköpsinställningar**.

När växlingen **Tillåt redigering av aktivt pris** är inaktiverad måste du för att uppdatera priser i en prislista ändra status för prislistan till **Utkast**, göra ändringen och sedan återaktivera prislistan.

Sidan **prisöversikt** ger en överblick över alla priser över prislistor. Du kan ange filter för att begränsa listan över priser som du kanske vill ändra eller lägga till i. När du har ändrat priserna måste du använda åtgärden **bekräfta rader** för att kontrollera priserna mot andra prislistrader. Genom att kontrollera priser kan du undvika dubbletter och tvetydigheter under prisberäkningen.

> [!NOTE]
> När du redigerar en rad i en aktiv prislista blir radens status **Utkast** och raden kommer inte att beaktas vid prisberäkningen förrän du använder åtgärden **Bekräfta rader**. När du har kontrollerat priset blir radens status **Aktiv** och kommer att beaktas i prisberäkningar.

För att lägga till nya priser, på **Prisöversikt**, använd åtgärden **Lägg till nya rader**. Sidan **Prisförslag** öppnas och du kan lägga till prisrader antingen genom att föreslå dem baserat på kriterier, kopiera dem från andra prislistor eller manuellt ange dem. Efteråt kan du använda åtgärden **implementera prisändring** för att jämföra de nya priserna med andra prislistor för att undvika dubbletter och oklarhet vid prisberäkning.

#### <a name="create-sales-price-lines-based-on-the-unit-price"></a>Skapa försäljningsprisrader baserat på enhetspriset

1. På sidan **Prisförslag** väljer du åtgärden **Föreslå rader**.
2. På sidan **Prisrader – Skapa ny** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I fältet **Produktfilter** definierar du filter för den valda **produkttypen**.
4. Välj fältet **Standard** för att ange inställningar som:
   * Vilka enheter som prislistan ska tilldelas till.
   * Datum då priset gäller.
   * Valutakod.
   * Beloppstypfilter som definierar vilka kolumner som visas på prislisteraderna.
5. Välj **OK**. Nya rader läggs till på sidan **Prisförslag** med de valda inställningarna och enhetspriset från artikelkorten.
6. Redigera de skapade raderna med de nya enhetspriserna eller rabatterna. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="create-sales-price-lines-based-on-existing-price-lists"></a>Skapa försäljningsprisrader baserat på befintliga prislistor

1. På sidan **Prisförslag** väljer du åtgärden **Kopiera rader**.
2. På sidan **Prisrader – kopiera befintliga** väljer du en befintlig prislista i fältet **Från prislista**.
3. I fältet **Prisradsfilter** anger du filter för produkter på den valda prislistan.
4. Välj fältet **Standard** för att ange inställningar som:
   * Vilka enheter som prislistan ska tilldelas till.
   * Datum då priset gäller.
   * Valutakod.
   * Beloppstypfilter som definierar vilka kolumner som visas på prislisteraderna.
5. Fyll i andra fält om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Välj **OK**. Nya rader läggs till på sidan **Prisförslag** med de valda inställningarna.
7. Redigera de skapade raderna med de nya enhetspriserna eller rabatterna. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-sales-prices"></a>Så här kopierar du försäljningspriser

Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. Om funktionsuppdateringen inte är aktiverad följer du anvisningarna på fliken Aktuell upplevelse.

#### [Aktuell upplevelse](#tab/current-experience/)  

Om du vill kopiera försäljningspriser – till exempel en viss kunds försäljningspriser – och använda dem för en kundprisgrupp, måste du köra **Föreslå förs.pris i förslag**. batch-jobbet på sidan **Försäljningsprisförslag**.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningspriskalkylark** och välj sedan relaterad länk.  
2. Välj **Föreslå förs.pris i ändringsformulär** .  
3. På snabbfliken **Förs.priser** fyller du i fälten **Förs.typ** och **Förs.kod** för de försäljningspriser som du vill kopiera.  
4. I den övre delen av sidan fyller du i fälten **Förs.typ** och **Förs.kod** med de uppgifter som du vill kopiera försäljningspriserna till.  
5. Om du vill skapa nya priser med batch-jobbet markerar du kryssrutan **Skapa nya priser**.  
6. Klicka på knappen **OK** för att fylla i raderna på sidan **Försäljningsprisförslag** med de föreslagna nya priserna och ange att de nu gäller för den valda försäljningstypen.  

   > [!NOTE]  
   > Batch-jobbet tar bara fram förslag, det genomför inte förändringarna. Om du är nöjd med förslagen och vill använda dem, d.v.s. infoga dem på sidan **Försäljningspriser**, väljer du åtgärden **Implementera prisändringar** på sidan **Försäljningsprisförslag**.

#### [Ny upplevelse](#tab/new-experience/)  

Du kan ange de inställningar som prislistan ska använda:

* Använd inställningarna från huvudet i listan som du kopierar.
* Använd inställningarna från listan du kopierar till. Om du vill använda inställningarna från prislistan som du kopierar priser till ska du aktivera reglaget **Använd standardinställningar från mål**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsprislistor** och välj sedan relaterad länk.
2. Välj den prislista som ska kopieras och välj sedan **Kopiera rader**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Du kan inte ha två artiklar som har samma inställningar men olika priser. Om detta händer visas ett meddelande när du aktiverar prislistan. Du kan välja det pris som ska användas genom att öppna listan och ta bort fel pris.  
  
---

## <a name="to-bulk-update-item-prices"></a>Så här uppdaterar du flera artikelpriser samtidigt

Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. Om funktionsuppdateringen inte är aktiverad följer du anvisningarna på fliken Aktuell upplevelse.

#### [Aktuell upplevelse](#tab/current-experience/)

Om du vill uppdatera flera artikelpriser samtidigt – till exempel höja alla priser med en viss procentsats kan du fylla sidan Försäljningsprisförslag genom att använda följande batchjobb:

* **Föreslå förs.pris i ett förslag** föreslår ändringar på ett av två sätt:

  * Genom att tillämpa en justeringsfaktor på befintliga försäljningspriser.
  * Genom att kopiera befintliga försäljningsprisavtal till andra kunder, kundprisgrupper eller försäljningskampanjer.

* **Föreslå artikelpris i förslag** föreslår ändringar på ett av två sätt:

  * Genom att tillämpa en justeringsfaktor på befintliga enhetspriser på artikelkort.
  * Genom att föreslå priser för nya kombinationer av valuta, måttenheter och så vidare.

  Detta batchjobb ändrar inte enhetspriserna på artiklar.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningspriskalkylark** och välj sedan relaterad länk.  
2. Välj **Föreslå artikelpris i förslag** .  
3. På snabbfliken **Artikel** fyller du i fältet **Artikelnr.** eller **Lagerbokföringsmall** eller andra fält med de ursprungliga artikelpriser som du vill uppdatera.  
4. I den övre delen av sidan fyller du i fälten **Förs.typ** och **Förs.kod** med de uppgifter som du vill kopiera försäljningspriserna till.
5. Om du vill att batch-jobbet ska föreslå artikelpriset automatiskt anger du justeringen i fältet **Justeringsfaktor**. Du kan till exempel ange 1,15 i **Justeringsfaktor** för 15 % ökning av artikelpris.  
6. Om du vill skapa nya priser med batch-jobbet markerar du växlingen **Skapa nya priser**.  
7. Välj knappen **OK** för att fylla i raderna på sidan **försäljningsprisförslag** med de föreslagna nya priserna.
8. Använd åtgärden **implementera prisändringar** för att genomföra förslagen . Batch-jobbet skapar förslag men verkställer inte dem. 

#### [Ny upplevelse](#tab/new-experience/)

Om du vill uppdatera priserna för flera artiklar måste du skapa en ny prislista och sedan kopiera raderna från en befintlig prislista. När du kopierar raderna kan du använda filter för att ange vad som ska kopieras, och du kan ange ett heltal eller decimaltal i fältet **Justeringsfaktor** för att höja eller sänka priserna. Statusen för prislistan måste vara **Utkast**. Om det behövs kan du sedan inaktivera den gamla prislistan.

> [!NOTE]
> Du kan inte ha två rader som har samma inställningar men olika priser. Om detta händer visas ett meddelande när du aktiverar en prislista. Du kan välja det pris som ska användas genom att öppna listan och ta bort fel pris.  

---

## <a name="best-price-calculation"></a>Bästa prisberäkning

När du har registrerat särskilda priser och radrabatter för försäljning och inköp beräknar [!INCLUDE[prod_short](includes/prod_short.md)] det bästa priset på försäljnings- och inköpsdokument och på projekt- och artikeljournalrader.

Det bästa priset är det lägsta priset med den högsta radrabatten som tillåts för ett visst datum. [!INCLUDE[prod_short](includes/prod_short.md)] beräknar bästa priser när du lägger till enhetspriser och radrabattens procentsats på dokument och journalrader.

> [!NOTE]  
> Följande beskriver hur det bästa priset beräknas för försäljning. Vid inköp är beräkningen detsamma, men baseras på de tillgängliga parametrarna. Artikelrabattgrupper stöds exempelvis inte för inköp.

1. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerar kombinationen av faktureringskund och artikel och beräknar sedan tillämpligt enhetspris och radrabattens procentsats utifrån följande villkor:

    * Finns det ett särskilt avtal om priser eller radrabatter för den här kunden, eller tillhör kunden en grupp som har ett sådant avtal?
    * Ingår artikeln eller artikelrabattgruppen på raden i något av dessa pris-/rabatt-avtal?
    * Ligger datumet inom pris-/rabattavtalets start- och slutdatum? För fakturor och kredit notor är det här datumet i fältet **bokföringsdatum** i dokumenthuvudet. För alla andra dokument är det datumet i fältet **orderdatum** i rubrikerna.
    * Har någon enhetskod angetts? I så fall gör [!INCLUDE[prod_short](includes/prod_short.md)] en sökning efter priser eller rabatter med samma enhetskod och efter priser eller rabatter som saknar enhetskod.

2. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerar om några pris- och rabattavtal gäller för information på dokumentet eller journalraden. Därefter infogas det aktuella enhetspriset och radrabattprocenten med hjälp av följande kriterier:

    * Finns det krav på en lägsta kvantitet i pris-/ rabattavtalet som är uppfyllda?
    * Finns det krav på valuta i pris-/ rabattavtalet som är uppfyllda? I så fall infogas det lägsta priset och den högsta radrabatten för den valutan, även om de skulle ge ett bättre pris i lokala valutan. Om det inte finns några pris-/rabattavtal för den angivna valutakoden infogar [!INCLUDE[prod_short](includes/prod_short.md)] det lägsta priset och den högsta radrabatten i dina lokala valuta.

Om inga specialpriser kan beräknas för artiklarna på raden infogas antingen det senaste inköpspriset eller à-priset från artikelkortet.

## <a name="sales-invoice-discounts-and-service-charges"></a>Försäljningsfakturarabatter och faktureringsavgifter

När du använder fakturarabatter, avgör fakturans totala belopp storleken på rabatten. På sidan **Kundfakturarabatter** kan du även lägga till en faktureringsavgift i fakturor som överstiger ett visst belopp.  

Innan du kan använda fakturarabatter vid försäljning måste du ange viss information. Du måste bestämma följande:  

* vilka kunder som ska erhålla den här typen av rabatt?  
* vilka rabattsatser i procent som ska användas?  

Om du vill att fakturarabatter beräknas automatiskt kan du ange detta på sidan **Försäljningsinställningar** aktivera växlingen **Beräkna fakturarabatt**.  

Du kan ange om du ska ge fakturarabatter när en faktura uppfyller vissa kriterier för varje kund. Till exempel om fakturabeloppet är stort nog. Fakturarabattvillkoren kan vara i lokal valuta för inrikes kunder och i utländsk valuta för kunder i utlandet.  

Du kan koppla rabattsatser i procent till särskilda fakturabelopp på sidan **Kundfakturarabatter** för respektive kund. Du kan ange ett obegränsat antal rabattsatser. Varje enskild kund han ha en egen sida, eller också kan du koppla flera kunder till samma sida.  

Förutom (eller i stället för) en procentuell rabatt kan du koppla en faktureringsavgift till ett särskilt fakturabelopp.  

> [!TIP]  
> Innan du anger den här informationen i programmet kan det vara praktiskt att skapa ett utkast av den rabattstruktur som du vill använda. Strukturen gör det enklare att se vilka kunder som kan kopplas till samma fakturarabattsida. Ju färre sidor som behöver definieras, ju snabbare går det att ange basinformationen.

För utbildning inom försäljningsrabatter, se [Ställa in rabatter för dina kunder](/training/modules/customer-discounts-dynamics-365-business-central/index).

### <a name="calculating-invoice-discounts-on-sales"></a>Beräkna fakturarabatter på försäljning

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Så här skapar du försäljningsradrabatter för en kund

Dessa steg skiljer sig åt beroende på om administratören har aktiverat funktionsuppdateringen **Ny upplevelse för försäljningspris**. Om funktionsuppdateringen inte är aktiverad följer du anvisningarna på fliken Aktuell upplevelse.

#### [Aktuell upplevelse](#tab/current-experience/)  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Radrabatter**.
3. Fyll i fälten på den första raden efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja en speciell försäljningsradrabatt till kunden.

> [!NOTE]
> När du öppnar sidorna **Försäljningspriser** och **Försäljningsradrabatter** för en specifik kund ställs fälten **Försäljningstypfilter** och **Försäljningskodfilter** in för kunden och kan inte ändras eller tas bort.
>
> Om du vill ställa in priser eller radrabatter för alla kunder, en kundprisgrupp eller en kampanj måste du öppna sidorna från ett artikelkort. Du kan också använda sidan **Försäljningsprisförslag** för försäljningspriser. Läs mer på [Så här uppdaterar du flera artikelpriser samtidigt](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### [Ny upplevelse](#tab/new-experience/)  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Välj kunden och sedan åtgärden **Försäljningsprislistor**.
3. Öppna prislistan för vilken radrabatten ska anges.
4. Skapa en ny rad eller välj en befintlig rad och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. I fältet **Definitioner** väljer du antingen **Pris och rabatt** eller bara **Rabatt**. 
6. I fältet **Radrabatt %** anger du rabattprocenten.

    > [!TIP]
    > Om du redigerar en befintlig rad kan du filtrera raderna genom att välja lämpligt alternativ i fältet **Visa kolumner för**.

    > [!NOTE]  
    > Fakturarabattkoder representeras av befintliga kundkort. Detta aktiverar dig att snabbt tilldela fakturarabattvillkor till kunder, genom att välja namnet på en andra kunder som ska ha dessa villkor. Ställ in kundspecifika villkor för fakturarabatt genom att ange fältet **Fakturarabattkod** som kundens kundkod, och fortsätt sedan till nästa steg.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Så här definierar du radrabatt för en kund

När du har bestämt vilka kunder som är aktuella för fakturarabatter, anger du fakturarabattkoderna på kundkortsidor. Ställ sedan in villkoren för varje kod.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna kundsidan för en kund som är aktuell för fakturarabatter.
3. Välj i fältet  **Fakturarabattkod** koden för den fakturarabatt som ska användas vid beräkning av fakturarabatter för kunden.

> [!NOTE]  
> Fakturarabattkoder representeras av befintliga kundkort. Detta aktiverar dig att snabbt tilldela fakturarabattvillkor till kunder, genom att välja namnet på en andra kunder som ska ha dessa villkor.

Gå vidare för att definiera nya fakturarabattvillkor för försäljning.

1. På sidan **Kunder** väljer du åtgärden **Fakturarabatter**. Sidan **Kundfakturarabatter** öppnas.
2. I fältet **Valutakod** anger du koden för en valuta som fakturarabattvillkoren på raden ska gälla. Lämna det här fältet tomt om du vill ange fakturarabattvillkor i SEK.
3. Ange i fältet **Minimibelopp** det minsta belopp som en faktura måste vara på för att komma i fråga för rabatt.
4. Fakturarabatten beräknas som en procentandel av fakturabeloppet i fältet **Rabatt %**.
5. Upprepa steg 5 till och med 7 för varje valuta som kunden ska ta emot en annan fakturarabatt för.

## <a name="see-also"></a>Se även

[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Ställ in kundprisgrupper](sales-how-to-set-up-customer-price-groups.md)  
[Ställ in kundrabattgrupper](sales-how-to-set-up-customer-discount-groups.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
