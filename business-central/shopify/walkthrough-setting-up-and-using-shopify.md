---
title: Ställ in och använd Shopify koppling
description: Olika integrationsscenarier för att demonstrera arbetsflöden mellan Shopify och Business Central
ms.date: 08/30/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector"></a>Genomgång: ställa in och använda Shopify anslutningsprogram

I det här avsnittet beskrivs några typiska scenarier och du får öva på att testa eller utbilda användare i det integrerade [!INCLUDE[prod_short](../includes/prod_short.md)] området och Shopify butiken.

## <a name="prerequisites"></a>Förutsättningar

### <a name="shopify"></a>Shopify

Du måste ha följande:

- Ett Shopify-konto
- En onlinebutik med Shopify

Mer information om hur du skapar Shopify testversioner och rekommenderade inställningar finns i [Skapa och ställa in ett Shopify-konto](shopify-account.md).

### <a name="business-central"></a>Business Central

Du måste ha ett [!INCLUDE[prod_short](../includes/prod_short.md)]-konto.

Du kan t.ex. skapa demokonto eller starta utvärdering. Lär dig mer när du [ Förbered demonstrationsmiljöer av Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) och [ Registrera dig för testversionen](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop"></a>Ansluta Business Central till butiken på Shopify

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör följande:

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butiker** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I fältet **Kod** ange **DEMO1**.
4. I fältet **Shopify URL** anger du webbadressen för den onlinebutik som du vill ansluta till.
5. Aktivera reglaget **Aktiverad**, granska och godkänn villkoren.

För att konfigurera Shopify-butiken, följ dessa steg:

1. Inaktivera reglaget **Tillåt synkronisering i bakgrunden**.
2. Välj *Till Shopify* i fältet **Synkronisera artikel**.
3. Välj *Till Shopify* i fältet **Synkronisera artikelbilder**.
4. Aktivera växlingsknappen **Synkronisera artikelattribut**.
5. Aktivera växlingsknappen **Lager spårat**.
6. Välj *Neka* i fältet **Standardlagerprincip**.
7. Aktivera växlingsknappen **Skapa okända automatiskt**.
8. Fyll i fältet **Mallkod för kund/företag** med rätt mall.
9. Fyll i **Leveranskostnadskonto**, **Drickskonto** med intäktskontot. I USA använder **du till exempel 40210**.
10. Aktivera växlingsknappen **Skapa order automatiskt**.
11. Stäng av växlingsknappen **Släpp försäljningsorder automatiskt**.

Konfigurera platsmappning:

1. Välj åtgärden **Platser** för att öppna **Shopify-butiksplatser**.
2. Välj åtgärden **Hämta Shopify-platser** för att importera alla platser som har definierats i Shopify. Välj post med **Är primär** är markerad.
3. I lagerställefiltret **anger** du **''|ÖST|HUVUDSAKLIG**.
4. Om du vill aktivera en lagersynkronisering för ett valt Shopify lagerställe går du till fältet **Lagerberäkning** Välj **Beräknat disponibelt saldo i dag**.

## <a name="walkthrough-start-selling-products-online"></a>Genom gång: börja sälja produkter online

### <a name="scenario"></a>Scenario

Anta att du vill prova Shopify som en onlinebutik utan att behöva ägna mycket tid på att konfigurera, speciellt eftersom du redan håller dina artiklar i [!INCLUDE[prod_short](../includes/prod_short.md)] . När du startat Shopify onlinebutiken får du omedelbart nya kunder som är nöjda med din butik och deras inköpsupplevelser. De bestämmer sig för att lämna dricks i kassan.

### <a name="steps"></a>Steg

I [!INCLUDE[prod_short](../includes/prod_short.md)], följ dessa steg:

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och anger **Shopify-produkter** och väljer sedan relaterad länk.
2. Välj **Lägg till artiklar**.
3.  **I fältet Fabrikskod** anger du **DEMO1**.
4. I fältet **Artikelkategorikod** ställer du in filtret **STOL.**
5. Aktivera växlingsknappen **Synkronisera produktbilder**.
6. Aktivera växlingsknappen **Synkronisera lager**.
7. Välj **OK** och vänta tills den första synkroniseringen av artiklar, priser, bilder och lager är klar.

I **Shopify onlinebutik**:
> [!Tip]  
> Öppna **Shopify administration**, genom att gå till URL-adressen som anges i fältet **URL** på sidan **Shopify butikskort**. Välj sedan ögon ikonen bredvid **Online-butiken** försäljningskanalen för onlinebutiken, som finns i listrutan för **Shopify administration**. 

Öppna produktkatalogen. Meddelanden:

* Produkttitlar, bilder och priser.
* Tillgänglighets indikator (säljs för produkter utanför lagret).

Välj vilken produkt som helst som kan säljas. Till exempel BERLIN svängstol, **gul**. Observera att beskrivningen innehåller objektattribut.

Välj **Köp nu** och gå till kassan.

1. I fältet **E-post eller mobiltelefonnummer** anger **cl@contoso.com**  du (eller en e-postadress dit du vill ta emot order- och leveransbekräftelser).
2. I fälten **Förnamn** och **Efternamn** anger du **Claudia** och **Lawson**.
3. Ange lokal adress.
4. Markera kryssrutan **Spara den här informationen för nästa gång**.
6. Behåll *Standard* som leveransmetod.
8.  **I fältet Kredit kort nummer** anger **du 1** om du använder **(för testning) falsk gateway** eller anger **5555 5555 5555 4444** om du använder **Shopify betalningar** i testläge.
9. Fyll i fälten **Namn på kort**.
10. I fältet **Utgångsdatumet**, ange aktuell månad/år.
11. I säkerhetskoden **anger** du **111**.
12. Valfritt: Välj **10 %**  dricks.
13. Välj **Betala nu**.

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör något av följande:

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify-order** och väljer sedan relaterad länk.
2. Välj åtgärden **Synkronisera ordrar från Shopify**.
3. Välj **OK**.

Den importerade ordern är klar för bearbetning.

1. Välj den importerade ordern om du vill öppna fönstret **Shopify Order**.
2. Lägg märke till att den nya kunden och försäljningsordern har skapats.
3. Utforska åtgärderna Risker **och** **Fraktkostnader** .
4. Välj **Försäljningsorder** för att öppna fönstret **Försäljningsorder**. Försäljningsorder är ett behov, som om det behövs, kan omfattas av montering, produktion eller inköp med hjälp av planeringsmotorn. Den har också stöd för olika lagerhanteringsprocesser med komplett separation av uppgifter.
6. I fältet **Agent** anger du **DHL**. Öppna ordningen igen om det behövs genom att välja åtgärden **Öppna igen**.
7. I Paketspårningsnr **anger** du **123456789**.
8. Välj åtgärden **bokför**, välj alternativet **Leverera och fakturera** och välj sedan **OK**.

Nu kan fysiska och ekonomiska data registreras i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det är dags att meddela Shopify om ändringarna.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Synkronisera försändelser till Shopify** och välj relaterad länk.
2. Välj **OK**.

I **Shopify Admin** meddelande om att ordern nu är markerad som *uppfylld*. Du kan också granska försändelseinformationen och visa spårnings-URL:en där. Om du kör **Synkronisera order från Shopify** kommer ordern att arkiveras i båda systemen.

## <a name="walkthrough-add-your-customers-to-your-new-online-store"></a>Genomgång: Lägg in dina kunder till din nya onlinebutik

### <a name="scenario-1"></a>Scenario

Efter en lyckad snabbstart av den nya onlinebutiken vill du att de aktuella kunderna ska besöka den och börja montera order. Beroende på din Shopify-plan och process kan du prova B2B- och DTC-flöden.

### <a name="dtc-steps"></a>DTC-steg

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör följande:

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") ikon, ange **Shopify Kunder** och väljer sedan relaterad länk.
2. Välj **Lägg till kunder**.
3.  **I fältet Fabrikskod** anger du **DEMO1**.
4. I fältet **Nr.** Ställer du in filtret **20000.**
5. Välj **OK** och vänta tills den första synkroniseringen av kunder har slutförts.

I **Shopify Admin** meddelande om att kunderna har importerats. Öppna kunderna och notera att kundens för- och efternamn kommer från fältet **kontaktnamn** av **kundkortet**. Företagsnamnet kan hittas i standard adressen som är kopplat till kunden. Om du använder **klassiska kundkonton** kan du Välj **Skicka kontoinbjudan** för att bjuda in kunden. Med **Nya kundkonton** krävs inget lösenord för att kunder ska kunna logga in. I stället Shopify  kan dina kunder logga in med en 6-siffrig engångsverifieringskod som skickas via e-post. 

### <a name="b2b-steps"></a>B2B-steg

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör följande:

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") ikon, ange **Shopify företag** och väljer sedan relaterad länk.
2. Välj **Lägg till företag**.
3. I fältet Fabrikskod **anger** du **DEMO1**.
4. Ställ in filtret **30000** på **Nr.** .
5. Välj **OK** och vänta tills den första synkroniseringen av kunder har slutförts.

Lägg **Shopify märke till att både företaget och kunden har importerats i Admin**. Öppna kunderna och lägg märke till att faktaboxen Företag har länkar till företaget, platsen och tilldelade behörigheter.
För att bjuda in kunden, Välj **[...]** i faktaboxen **Företag** och sedan Välj **Skicka e-post för B2B-åtkomst**.

## <a name="walkthrough-fine-tuning-of-item-management"></a>Genomgång: finjustering av artikelhantering

### <a name="scenario-2"></a>Scenario

Du vill lägga till mer flexibilitet och kontrollera dina processer runt objekthantering. Du vill förbättra produktbeskrivningen och vill lägga till fler granskningssteg innan produkterna blir tillgängliga för alla kunder.

### <a name="steps-1"></a>Steg

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör följande:

Förbereda data.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kundprismall** och väljer sedan relaterad länk.
2. Lägg till en ny prisgrupp. I fältet **Kod** anger du **SHOPIFY.**
3. Stäng fönstret **Kundprisgrupp**.
4. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.
5. Välj artikel **1896-S, Athens Desk** och följ sedan dessa steg:

6.  **VäljVarianter** åtgärd och sedan lägga till två varianter: **PREMIUM, Athens Desk, Premium edition** och **ESSENTIAL, Athens Desk, Essential edition**.
7. Välj åtgärden **Marknadsföringstext** och använd **Utkast med Copilot**  för att få kreativ och engagerande text. Om förslag på marknadsföringstext inte är aktiverat anger du bara: "**Enkel snygg design** smälter in i vilken ensemble som helst. *Finns i två upplagor.*.
8. Välj åtgärden **försäljningspriser** och lägg till nya priser som visas i följande tabell:

   |Rad|Förs.typ|Förs.kod|Kontakttyp|Kod|Variantkod<br>(lägg till fältet via anpassning)|Styckpris|
   |------|------------|------------|------------|----------------|------------|------------|
   |1|Kundprisgrupp|SHOPIFY|Artikel|1896-S|ESSENTIAL|700|
   |2|Kundprisgrupp|SHOPIFY|Artikel|1896-S|PREMIUM|1 000|

9. Välj åtgärden **försäljningsrabatter** och lägg till en ny rabatt:

   * **Försäljningstyp** *Kundrabattgrupp*
   * **Förs.kod** *BUTIK*
   * **Typ** *Artikel*
   * **Kod** *1896-S*
   * **Måttenhetskod** *PCS*
   * **Radrabatt %** *10*

10.  **VäljArtikelreferenser** och lägg till följande rader:

   |Rad|Referenstyp|Referensnr|Variantkod|
   |------|------------|------------|------------|
   |1|Streckkod|77777777|ESSENTIAL|
   |2|Streckkod|11111111|PREMIUM|

11. Välj artikeln **1920-S, ANTWERP konferensbord** och gör följande steg:
12. Välj **Justera lager** och ange **100** för **lagerställena** ÖST och **VÄST i fältet Nytt**  **lager**.
13. Välj **OK**.

Justera inställningar för synkronisering.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den **DEMO1-butik** som du vill synkronisera artiklar för för att öppna **Shopify sidan Butik kort** .
3. Aktivera fältet **Synkronisera marknadsföringstext**.
4. I fältet **Lagerställeenhet mappning**  Välj **Artikelnr + Variantkod**.
5. I fältet **Standardlagerprincip** Välj **Fortsätt**.
6. I fältet **Status för skapade produkter** Välj **Utkast**.
7.  **I fältet Åtgärd för borttagen produkt** Välj **Status till arkiverad**.
8. I fältet **Kundprisgrupp**, Välj **SHOPIFY.**
9. I fältet **Kundrabattgrupp**, Välj **DETALJHANDEL.**

Kör synkronisering.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den **DEMO1-butik** som du vill synkronisera artiklar för för att öppna **Shopify sidan Butik kort** .
3. Välj **Produkter** för att öppna **Shopify sidan Produkter** .
4. Välj åtgärden **Lägg till artiklar**.
5. Ställ in filtertabellen **|DESK** i fältet **Artikelkategorikod** .
6. Aktivera växlingsknappen **Synkronisera produktbilder**.
7. Aktivera växlingsknappen **Synkronisera lager**.
8. Välj **OK** och vänta tills den första synkroniseringen av artiklar, priser, bilder och lager är klar.

Produkter läggs till. Observera att statusen är inställd på **Utkast** och därför är artiklar inte synliga i onlinebutiken Shopify .

1. Välj raden med artikel **1920-S, ANTWERP konferensbord**. I SEO-titeln anger du **Rektangulärt mötesbord Antwerpen**, 10 platser, svart **.**
2. I fältet **Status** Välj **Aktiv**.
3. Välj raden med artikel **1906-S, ATEN, Mobile Piedestal** och sedan Välj **Delete**.

I **Shopify Admin**-meddelandet att alla produkter har olika status.

* *ANTWERP konferensbord* är *aktivt* eftersom vi ändrade dess status på **Shopify produktsidan** .
* *ATHENS Desk* är *utkast* eftersom vi konfigurerade standard status för alla tillagda produkter som *utkast*.
* *ATHENS mobil pelare* är *arkiverad* eftersom vi konfigurerade butiken att automatiskt tilldela status *arkiverat* för borttagna produkter.

Observera att lagret för ANTWERP Conference Table är 100, eftersom vi konfigurerade systemet för att endast använda lager från två platser, MAIN och EAST. Lagret på en annan plats (VÄST) ignoreras.

* Öppna *ANTWERP Conference-tabell*, meddelande **Anpassad typ**, **leverantör**, **vikt**, **kostnad per artikel** och avsnittet **förhandsversion av sökmotorlista**.
* Öppna *Athens Desk*, bläddra ned till avsnittet **varianter** och lägg märke till hur **SKU** är ifyllt.
* Om du vill granska streckkod och priser Välj **Redigera**.
* Ändra status **för Athens Desk** till **Aktiv** och Välj **förhandsversion**.

 Shopify Öppna produktkatalogen i webbutiken och hitta **produkten ATHENS Desk** . Lägg märke till att olika alternativ är tillgängliga. För olika alternativ är priserna olika. Beakta information om rabatt.

### <a name="additional-steps-for-b2b"></a>Ytterligare steg för B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Du kan konfigurera anslutningsprogram så att den automatiskt skapar och tilldelar katalog för exporterade företag. Stegen nedan är användbara om du vill ha mer exakt kontroll över vad som är tillgängligt för B2B-kunder.

Skapa och tilldela en katalog i **Shopify Admin**.

1. Välj **Produkter** och sedan **Kataloger** i sidofältet i **Shopify administration**.
2. Skapa en katalog för specifika produkter. Ge den titeln "B2B". 
3. Välj **Hantera och sedan** Hantera produkter och **priser**.
4. Välj den **Undantaget** filter, hitta **ATEN-skrivbord** och välj **Inkludera i katalog.**
5. Välj **Kunder** och sedan **Företag** i sidofältet **Shopify i admin**.
6. Välj **Konsthögskolan**, välj **[...]**, och sedan **Lägg till kataloger** och lägg till den **B2B-katalog** som skapades tidigare.

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör följande:

Förbereda data.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.
2. Välj artikel **1896-S, Athens Desk** och följ sedan dessa steg:
3. Välj åtgärden **försäljningsrabatter** och lägg till en ny rabatt:

   * **Försäljningstyp** *Kundrabattgrupp*
   * **Förs.kod** *VOLYMPART*
   * **Typ** *Artikel*
   * **Kod** *1896-S*
   * **Måttenhetskod** *PCS*
   * **Radrabatt %** *25*

4. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och anger **Shopify-kataloger** och väljer sedan relaterad länk.
5. Välj **Hämta kataloger**.
6.  **I fältet Fabrikskod** anger du **DEMO1**.
7. Välj transaktionen med *B2B-katalog* som du vill synkronisera priser för.
8. Aktivera växlingsknappen **Synkroniseringspriser**.
9. I fältet **Kundprisgrupp**, Välj **SHOPIFY.**
10. I fältet **Kundrabattgrupp** Välj **STOR ACC**.
11. Välj **Synkronisera priser** och vänta tills synkroniseringen av priser har slutförts.

I **Shopify Administration undersöker du priserna för B2B-katalogen** **.** 

I **Shopify onlinebutik** öppna produktkatalogen, hitta *ATHENS Desk*-produkten. Anteckna pris- och rabattinformation.

## <a name="walkthrough-check-out-and-order-synchronization-for-individual-buyer-and-company-representative"></a>Genomgång: Checka ut och ordersynkronisering för enskild inköpare och företagsrepresentant

Det här är en förlängning av [ genomgången: påbörja försäljning av produkter online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Du kan också prova med dina egna data, till exempel med din Shopify butik eller sandlåda.

Enskild köpare

1. I **Shopify onlinebutik**. Välj ikonen **Konton**. Ange e-post du har tillgång till.
2. Logga in med en 6-siffrig engångsverifieringskod som skickas via e-post du angav.
3. Utforska produktkatalogen, bör du kunna se alla produkter med detaljhandelspriser.
4. Välj Essential-variant och välj **Köp nu** och fortsätt till kassan.
5. Fyll i fältet **förnamn** och **efternamn**.
6. Ange lokal adress.
7. Behåll *Standard* som leveransmetod.
8.  **I fältet** Kredit kort anger **du 1** om du använder **(för testning) falsk gateway** eller anger **5555 5555 5555 4444** om du använder **Shopify betalningar** i testläge.
9. I fältet **Utgångsdatumet**, ange aktuell månad/år.
10. I säkerhetskoden **anger** du **111**.
11. Fyll i fälten **Namn på kort**.
12. Välj **Betala nu**.

Företagsrepresentant

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. I **Shopify administration**.
2. Välj **Kunder** och sedan **Företag** i sidofältet i **Shopify administration**.
3. Öppna posten *Konsthögskolan*.
4. Välj **[...]** i faktaboxen **för Konsthögskolan**, sedan **Redigera betalningsvillkor** och sedan Välj **Förfaller den uppfyllelse**.
5. Välj **[...]** i faktaboxen **Kunder** och sedan **Lägg till kund** och lägg sedan till den med den e-postadress som du använde för att logga in i butiken tidigare.
6. I **Shopify onlinebutik**. Välj ikonen **Konton**. Ange e-post du har tillgång till.
7. Logga in med en 6-siffrig engångsverifieringskod som skickas via e-post du angav.
8. Utforska produktkatalogen, bör du bara kunna se produkt som lagts till i B2B-katalogen med specialpriser.
9. Välj den väsentliga varianten, Välj **Köp den nu** och fortsätt till kassan.
10. Observera att konto, Leverera till och betalningsmetod är ifyllda.
11. Fyll i **fältet** PO-nummer med **PO-12345**.
12. Välj **Skicka order**.

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör något av följande:

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify-order** och väljer sedan relaterad länk.
2. Välj åtgärden **Synkronisera ordrar från Shopify**.
3. Välj **OK**.

Den importerade ordern är klar för bearbetning.

1. Välj den importerade ordern för att öppna **Shopify Beställningssida** .
2. Observera att båda beställningarna skickades av samma person, de är kopplade till två olika kunder.
3. I ordern som skickas för företagets räkning kan du se ett värde i **fältet PO-nummer**, som också överförs till fältet **Externt dokumentnr.** för det skapade försäljningsdokumentet.
4. Eftersom vi har konfigurerat B2B-företaget att hantera betalningar utanför Shopify anges Finansiell **status till** Väntande **·**. När du har tagit emot betalningen Välj **åtgärden Markera som betald** . Den ekonomiska statusen uppdateras i Shopify.

## <a name="walkthrough-import-items-customers-companies-from-shopify"></a>Genomgång: Importera varor, kunder, företag från Shopify

### <a name="scenario-3"></a>Scenario

Du har redan en lyckad onlinebutik och vill börja använda [!INCLUDE[prod_short](../includes/prod_short.md)] som verksamhetshanteringsprogram. Du vill importera så mycket data Shopify som möjligt.

### <a name="steps-2"></a>Steg

Detta är en fortsättning på [Genomgång: Börja sälja produkter online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) och [Genomgång: Lägg till dina kunder till din nya webbutik](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). Du kan också prova med dina egna data, till exempel med din Shopify butik eller sandlåda.

I [!INCLUDE[prod_short](../includes/prod_short.md)] följer du stegen som anges härnäst.

#### <a name="prepare-data"></a>Förbereda data

1. Växla till en kostnadsfri provperiod på 30 dagar utan exempeldata. Mer information finns i [ lägga till egna data till en tom testversion](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butiker** och väljer sedan relaterad länk.
3. Välj **Ny**.
4. I fältet **Kod** ange **DEMO2**.
5. I fältet **Shopify URL** anger du webbadressen till den onlinebutik som du vill ansluta till.
6. Aktivera reglaget **Aktiverad**, granska och godkänn villkoren.

Konfigurera Shopify butiken enligt beskrivningen här:

1. Inaktivera reglaget **Tillåt synkronisering i bakgrunden**.
2. I fältet **Synkronisera objekt** Välj **Från Shopify**.
3. Aktivera växlingsknappen **Skapa okända objekt** automatiskt.
4. Fyll i fältet **Artikelmallkod** med rätt mall.
5. I fältet **Synkronisera artikelbilder** Välj **Från Shopify**.
6. I fältet **Lagerställeenhet mappning**  Välj **Artikelnr + Variantkod**.
7. I **fältet Kundimport från Shopify** Välj **Alla kunder**.
8. Aktivera växlingsknappen **Skapa okända automatiskt**.
9. Fyll i fältet **Mallkod för kund/företag** med rätt mall.
10.  **I fältet Företagsimport från Shopify** Välj **Alla kunder**.
11. Aktivera växlingsknappen **Skapa okänt företag** automatiskt.

#### <a name="run-the-synchronization"></a>Kör synkronisering

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den *DEMO2* butik som du vill synkronisera data för och öppna sidan **Shopify butikskort**.
3. Välj **Synkronisera produkter**.
4. Välj **Synkronisera produktbilder**.
5. Välj **Synkronisera kunder**.
6. Välj **Synkronisera företag**

### <a name="results"></a>Resultat

* Shopify produkter importeras. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och anger **Shopify-produkter** och väljer sedan relaterad länk.
* Objekt med bilder skapas. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artikel** och välj sedan relaterad länk.
* Shopify Kunder importeras. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") ikon, ange **Shopify Kunder** och väljer sedan relaterad länk.
* Shopify Företag importeras. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") ikon, ange **Shopify företag** och väljer sedan relaterad länk.
* Kunderna skapas. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") ikon, ange **Kunder** och väljer sedan relaterad länk.

## <a name="see-also"></a>Se även

[Komma i gång med Shopify-anslutningsprogrammet](get-started.md)  
