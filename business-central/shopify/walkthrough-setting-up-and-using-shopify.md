---
title: Ställ in och använd Shopify koppling
description: Olika integrationsscenarier för att demonstrera arbetsflöden mellan Shopify och Business Central
ms.date: 06/21/2022
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
3. I fältet **kod** ange `DEMO1`.
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
9. Fyll i **Leveranskostnadskonto**, **Drickskonto** med intäktskontot. Du kan till exempel använda `40210` i USA.
10. Aktivera växlingsknappen **Skapa order automatiskt**.
11. Stäng av växlingsknappen **Släpp försäljningsorder automatiskt**.

Konfigurera platsmappning:

1. Välj åtgärden **Platser** för att öppna **Shopify-butiksplatser**.
2. Välj åtgärden **Hämta Shopify-platser** för att importera alla platser som har definierats i Shopify. Välj post med **Är primär** är markerad.
3. I **Platsfilter**, ange `''|EAST|MAIN`.
4. Välj *Lagerutveckling över tiden i dag* i fältet **Lagerberäkning** om du vill aktivera lagersynkronisering för vald Shopify-plats.

## <a name="walkthrough-start-selling-products-online"></a>Genom gång: börja sälja produkter online

### <a name="scenario"></a>Scenario

Anta att du vill prova Shopify som en onlinebutik utan att behöva ägna mycket tid på att konfigurera, speciellt eftersom du redan håller dina artiklar i [!INCLUDE[prod_short](../includes/prod_short.md)] . När du startat Shopify onlinebutiken får du omedelbart nya kunder som är nöjda med din butik och deras inköpsupplevelser. De bestämmer sig för att lämna dricks i kassan.

### <a name="steps"></a>Steg

I [!INCLUDE[prod_short](../includes/prod_short.md)], följ dessa steg:

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och anger **Shopify-produkter** och väljer sedan relaterad länk.
2. Välj **Lägg till artiklar**.
3. I fältet **Butikskod** ange `DEMO1`.
4. Ange filter `CHAIR` på fältet **Artikelkategorikod**.
5. Aktivera växlingsknappen **Synkronisera produktbilder**.
6. Aktivera växlingsknappen **Synkronisera lager**.
7. Välj **OK** och vänta tills den första synkroniseringen av artiklar, priser, bilder och lager är klar.

I **Shopify onlinebutik**:
> [!Tip]  
> Öppna **Shopify administration**, genom att gå till URL-adressen som anges i fältet **URL** på sidan **Shopify butikskort**. Välj sedan ögon ikonen bredvid **Online-butiken** försäljningskanalen för onlinebutiken, som finns i listrutan för **Shopify administration**. 

Öppna produktkatalogen. Meddelanden:

* Produkttitlar, bilder och priser.
* Tillgänglighets indikator (säljs för produkter utanför lagret).

Välj en produkt som kan säljas, till exempel `BERLIN Swivel Chair, yellow`. Observera att beskrivningen innehåller objektattribut.

Välj **Köp nu** och gå till kassan.

1. I fältet **E-post eller mobilnummer** ange `cl@contoso.com` (eller skicka e-post dit du vill få order- och fraktbekräftelser).
2. På fälten **förnamn** och **efternamn**, ange `Claudia Lawson`.
3. Ange lokal adress.
4. Markera kryssrutan **Spara den här informationen för nästa gång**.
6. Behåll *Standard* som leveransmetod.
8. I fältet **kreditkortnummer** ange `1` om du använder *(för test) Falsk gateway* eller anger `5555 5555 5555 4444` om du använder *Shopify Payments* i testläge.
9. Fyll i fälten **Namn på kort**.
10. I fältet **Utgångsdatumet**, ange aktuell månad/år.
11. I fältet **Säkerhetskod** ange `111`.
7. Valfritt: Välj `10%` tips.
8. 12. Välj **Betala nu**.

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör något av följande:

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify-order** och väljer sedan relaterad länk.
2. Välj åtgärden **Synkronisera ordrar från Shopify**.
3. Välj **OK**.

Den importerade ordern är klar för bearbetning.

1. Välj den importerade ordern om du vill öppna fönstret **Shopify Order**.
2. Lägg märke till att den nya kunden och försäljningsordern har skapats.
3. Utforska åtgärder för **Risk** och **Leveranskostnader**.
4. Välj **Försäljningsorder** för att öppna fönstret **Försäljningsorder**. Försäljningsorder är ett behov, som om det behövs, kan omfattas av montering, produktion eller inköp med hjälp av planeringsmotorn. Den har också stöd för olika lagerhanteringsprocesser med komplett separation av uppgifter.
6. I fältet **Agent** ange `DHL`. Öppna ordningen igen om det behövs genom att välja åtgärden **Öppna igen**.
7. I **Godsupplysningsnr.**, ange `123456789`.
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
3. I fältet **Butikskod** ange `DEMO1`.
4. Ange filter `20000` på **Nr.** .
5. Välj **OK** och vänta tills den första synkroniseringen av kunder har slutförts.

I **Shopify Admin** meddelande om att kunderna har importerats. Öppna kunderna och notera att kundens för- och efternamn kommer från fältet **kontaktnamn** av **kundkortet**. Företagsnamnet kan hittas i standard adressen som är kopplat till kunden. Om du använder *Klassiska kundkonton* kan du välja **Skicka kontoinbjudan** för att bjuda in kunden. Med *Nya kundkonton* krävs inget lösenord för att kunder ska kunna logga in, utan Shopify låter istället dina kunder logga in med en 6-siffrig engångsverifieringskod som skickas via e-post. 

### <a name="b2b-steps"></a>B2B-steg

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör följande:

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") ikon, ange **Shopify företag** och väljer sedan relaterad länk.
2. Välj **Lägg till företag**.
3. I fältet **Butikskod** ange `DEMO1`.
4. Ange filter `30000` på **Nr.** .
5. Välj **OK** och vänta tills den första synkroniseringen av kunder har slutförts.

I **Shopify administration**, notera att både företaget och kunden importerades. Öppna kunderna och lägg märke till faktaboxen Företag med länk till Företag, plats och tilldelade behörigheter. Välj **[...]** i **Företagets faktaruta och välj sedan**Skicka e-post med B2B-åtkomst** för att bjuda in kunden.

## <a name="walkthrough-fine-tuning-of-item-management"></a>Genomgång: finjustering av artikelhantering

### <a name="scenario-2"></a>Scenario

Du vill lägga till mer flexibilitet och kontrollera dina processer runt objekthantering. Du vill förbättra produktbeskrivningen och vill lägga till fler granskningssteg innan produkterna blir tillgängliga för alla kunder.

### <a name="steps-1"></a>Steg

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör följande:

Förbereda data.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kundprismall** och väljer sedan relaterad länk.
2. Lägg till en ny prisgrupp. I fältet **kod** ange `SHOPIFY`.
3. Stäng fönstret **Kundprisgrupp**.
4. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.
5. Välj artikel *1896-S, Aten skrivbord* och gör följande steg:

6. Välj åtgärden för **varianter** och Lägg sedan till två varianter: `PREMIUM, Athens Desk, Premium edition` och `ESSENTIAL, Athens Desk, Essential edition`.
7. Välj åtgärden **Marknadsföringstext** och använd **Utkast med Copilot**  för att få kreativ och engagerande text. Om förslag på marknadsföringstext inte är aktiverat anger du bara: "**Enkel snygg design** smälter in i vilken ensemble som helst. *Finns i två upplagor."* 
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

10. Välj åtgärden **artikelreferenser** och följande lägg till rader:

   |Rad|Referenstyp|Referensnr|Variantkod|
   |------|------------|------------|------------|
   |1|Streckkod|77777777|ESSENTIAL|
   |2|Streckkod|11111111|PREMIUM|

11. Välj artikeln *1920-S, ANTWERP konferensbord* och gör följande steg:
12. Välj **Justera lager** och ange fältet **Nytt lager** ange `100` för plats *ÖST* och *VÄST*. 
13. Välj **OK**.

Justera inställningar för synkronisering.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den `DEMO1` butik som du vill synkronisera artiklar för och öppna sidan **Shopify butikskort**.
3. Aktivera fältet **Synkronisera marknadsföringstext**.
4. Välj *Artikelnr + variantkod* i fältet **SKU-mappning** .
5. Välj *Fortsätt* i fältet **Standardlagerprincip**.
6. Välj *utkast* i fältet **status för skapade produkter** .
7. Välj *status att arkivera* i fältet **åtgärd för borttagen produkt** .
8. Välj *SHOPIFY* i fältet **kundprisgrupp** .
9. Välj *BUTIK* i fältet **Kundrabattgrupp** .
 
Kör synkronisering.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den `DEMO1` butik som du vill synkronisera artiklar för och öppna sidan **Shopify butikskort**.
3. Välj **Produkter** för att öppna fönstret **Shopify Produkter**.
4. Välj åtgärden **Lägg till artiklar**.
5. Ange filter *TABLE|DESK* på fältet **Artikelkategorikod**.
6. Aktivera växlingsknappen **Synkronisera produktbilder**.
7. Aktivera växlingsknappen **Synkronisera lager**.
8. Välj **OK** och vänta tills den första synkroniseringen av artiklar, priser, bilder och lager är klar.

Produkter läggs till. Observera att statusen är *utkast* och att objekt inte visas i Shopify onlinebutiken.

1. Välj rad med artikel *1920-S, ANTWERP konferensbord*. I fältet **SEO-rubrik**, ange `Rectangular meeting table Antwerp, 10 seats, black`.
2. Markera *Aktiv* i fältet **Status**.
3. Markera raden med artikel *1906-S, ATHENS, mobil pelare* och välj **Ta bort**.

I **Shopify Admin**-meddelandet att alla produkter har olika status.

* *ANTWERP Conference-tabell* är *aktiv* eftersom vi ändrade status i fönstret **Shopify produkt**.
* *ATHENS Desk* är *utkast* eftersom vi konfigurerade standard status för alla tillagda produkter som *utkast*.
* *ATHENS mobil pelare* är *arkiverad* eftersom vi konfigurerade butiken att automatiskt tilldela status *arkiverat* för borttagna produkter.

Observera att lager för ANTWERP Conference-tabellen är 100 eftersom vi har konfigurerat systemet att använda lager endast från två platser HUVUD och ÖSTRA. Lagret på en annan plats (VÄST) ignoreras.

* Öppna *ANTWERP Conference-tabell*, meddelande **Anpassad typ**, **leverantör**, **vikt**, **kostnad per artikel** och avsnittet **förhandsversion av sökmotorlista**.
* Öppna *Athens Desk*, bläddra ned till avsnittet **varianter** och lägg märke till hur **SKU** är ifyllt.
* Välj **Redigera** om du vill granska streckkoder och priser.
* Ändra status för *Aten Desk* till *aktiv* och välj **Förhandsgranska**.

I **Shopify onlinebutik** öppna produktkatalogen, hitta *ATHENS Desk*-produkten. Lägg märke till att olika alternativ är tillgängliga. För olika alternativ är priserna olika. Beakta information om rabatt.

### <a name="additional-steps-for-b2b"></a>Ytterligare steg för B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Du kan konfigurera anslutningsprogram så att den automatiskt skapar och tilldelar katalog för exporterade företag. Stegen nedan är användbara om du vill ha mer exakt kontroll över vad som är tillgängligt för B2B-kunder.

I **Shopify administration**cSkapa och tilldela katalog.

1. Välj **Produkter** och sedan **Kataloger** i sidofältet i **Shopify administration**.
2. Skapa katalog för specifika produkter. Ange rubriken "B2B". 
3. Välj **Hantera** och sedan **Hantera produkter och priser**.
4. Välj filtret *Exklusive* hitta *ATHERN Desk* och välj **Inkludera i katalog**.
5. Välj **Kunder** och sedan **Företag** i sidofältet i **Shopify administration**.
6. Välj *Konsthögskolan* och välj **[...]** och sedan **Lägg till kataloger** och lägg till *B2B*-katalog som skapades tidigare.

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör följande:

Förbereda data.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.

2. Välj artikel **1896-S, Aten skrivbord** och gör följande steg:

3. Välj åtgärden **försäljningsrabatter** och lägg till en ny rabatt:

   * **Försäljningstyp** *Kundrabattgrupp*
   * **Förs.kod** *VOLYMPART*
   * **Typ** *Artikel*
   * **Kod** *1896-S*
   * **Måttenhetskod** *PCS*
   * **Radrabatt %** *25*

4. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och anger **Shopify-kataloger** och väljer sedan relaterad länk.
5. Välj **Hämta kataloger**.
6. I fältet **Butikskod** ange `DEMO1`.
7. Välj transaktion med namnet *B2B-katalog* som du vill synkronisera priser för.
8. Aktivera växlingsknappen **Synkroniseringspriser**.
9. Välj *SHOPIFY* i fältet **kundprisgrupp** .
10. Välj *VOLYMPART* i fältet **Kundrabattgrupp** .
11. Välj **Synkronisera priser** och vänta tills synkroniseringen av priser har slutförts.

I **Shopify administration** undersöker du priser för *B2B-katalogen*.

I **Shopify onlinebutik** öppna produktkatalogen, hitta *ATHENS Desk*-produkten. Observera att priserna är rabattinformation.

## <a name="walkthrough-check-out-and-order-synchronization-for-individual-buyer-and-company-representative"></a>Genomgång: Checka ut och ordersynkronisering för enskild inköpare och företagsrepresentant
Det här är en förlängning av [ genomgången: påbörja försäljning av produkter online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Du kan också prova med egna data, till exempel Shopify butiken eller sandbox.

Enskild köpare

1. I **Shopify onlinebutik**. Välj ikonen **Konton**. Ange e-post du har tillgång till.
2. Logga in med en 6-siffrig engångsverifieringskod som skickas via e-post du angav.
3. Utforska produktkatalogen, bör du kunna se alla produkter med detaljhandelspriser.
4. Välj Essential-variant och välj **Köp nu** och fortsätt till kassan.
5. Fyll i fältet **förnamn** och **efternamn**.
6. Ange lokal adress.
7. Behåll *Standard* som leveransmetod.
8. I fältet **kreditkortnummer** ange `1` om du använder *(för test) Falsk gateway* eller anger `5555 5555 5555 4444` om du använder *Shopify Payments* i testläge.
9. I fältet **Utgångsdatumet**, ange aktuell månad/år.
10. I fältet **Säkerhetskod** ange `111`.
11. Fyll i fälten **Namn på kort**.
12. Välj **Betala nu**.
 
Företagsrepresentant

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. I **Shopify administration**.
2. Välj **Kunder** och sedan **Företag** i sidofältet i **Shopify administration**.
3. Öppna posten *Konsthögskolan*.
4. Välj **[...]** i faxrutan **Konsthögskolan** och sedan **Redigera betalningsvillkor** och välj *Förfaller vid uppfyllelse*.
5. Välj **[...]** i faktarutan **Kunder** och sedan **Lägg till kund** och lägg till en med e-postadress som du använde för att logga in i butiken tidigare.
6. I **Shopify onlinebutik**. Välj ikonen **Konton**. Ange e-post du har tillgång till.
7. Logga in med en 6-siffrig engångsverifieringskod som skickas via e-post du angav.
8. Utforska produktkatalogen, bör du bara kunna se produkt som lagts till i *B2B-katalogen* med specialpriser.
9. Välj Essential-variant och välj **Köp nu** och fortsätt till kassan.
10. Observera att konto, Leverera till, betalningsmetod är ifyllda.
11. Fyll i fältet **inköpsordernumret** med `PO-12345`.
12. Välj **Skicka order**.
 
I [!INCLUDE[prod_short](../includes/prod_short.md)], gör något av följande:

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify-order** och väljer sedan relaterad länk.
2. Välj åtgärden **Synkronisera ordrar från Shopify**.
3. Välj **OK**.

Den importerade ordern är klar för bearbetning.

1. Välj den importerade ordern om du vill öppna fönstret **Shopify Order**.
2. Observera att även om båda beställningarna skickades av samma person, är de kopplade till två olika kunder. 
3. I ordern som skickas för företagets räkning kan du se värdet i fältet **PO-nummer**, som också överförs till fältet **Externt verifikationsnr.** för skapat försäljningsdokument.
4. Eftersom vi har konfigurerat B2B-företaget för att hantera betalningar utanför Shopify är **Finansiell status** är inställd på *Väntande*. När du har fått betalning väljer du åtgärden **Markera som betald**. Finansiell status kommer att uppdateras i Shopify. 

## <a name="walkthrough-import-items-customers-companies-from-shopify"></a>Genomgång: Importera varor, kunder, företag från Shopify

### <a name="scenario-3"></a>Scenario

Du har redan en lyckad onlinebutik och vill börja använda [!INCLUDE[prod_short](../includes/prod_short.md)] som verksamhetshanteringsprogram. Du vill importera så mycket data Shopify som möjligt. 

### <a name="steps-2"></a>Steg

Detta är en fortsättning på [Genomgång: Börja sälja produkter online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) och [Genomgång: Lägg till dina kunder till din nya webbutik](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). Du kan också prova med egna data, till exempel Shopify butiken eller sandbox.

I [!INCLUDE[prod_short](../includes/prod_short.md)] följer du stegen som anges härnäst.

#### <a name="prepare-data"></a>Förbereda data

1. Växla till en kostnadsfri provperiod på 30 dagar utan exempeldata. Mer information finns i [ lägga till egna data till en tom testversion](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butiker** och väljer sedan relaterad länk.
3. Välj **Ny**.
4. I fältet **kod** ange `DEMO2`.
5. I fältet **Shopify URL** anger du webbadressen till den onlinebutik som du vill ansluta till.
6. Aktivera reglaget **Aktiverad**, granska och godkänn villkoren.

Konfigurera Shopify butiken enligt beskrivningen här:

1. Inaktivera reglaget **Tillåt synkronisering i bakgrunden**.
2. Välj *Från Shopify* i fältet **Synkronisera artikel**.
3. Aktivera växlingsknapp **Skapa okända artiklar automatiskt**.
4. Fyll i fältet **Artikelmallkod** med rätt mall.
5. Välj *Från Shopify* i fältet **Synkronisera artikelbilder**.
6. Välj *Artikelnr + variantkod* i fältet **SKU-mappning** .
7. Välj *Alla kunder* i **kundimporten från Shopify**.
8. Aktivera växlingsknapp **Skapa okända kunder automatiskt**.
9. Fyll i fältet **Mallkod för kund/företag** med rätt mall.
10. Välj *Alla kunder* i **företagsimporten från Shopify**.
11. Aktivera växlingsknapp **Skapa okända företag automatiskt**.

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
* Shopify kunderna importeras. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") ikon, ange **Shopify Kunder** och väljer sedan relaterad länk.
* Shopify företag importeras. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") ikon, ange **Shopify företag** och väljer sedan relaterad länk.
* Kunderna skapas. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") ikon, ange **Kunder** och väljer sedan relaterad länk.


## <a name="see-also"></a>Se även

[Komma i gång med Shopify-anslutningsprogrammet](get-started.md)  
