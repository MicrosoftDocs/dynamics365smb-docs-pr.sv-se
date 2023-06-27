---
title: Ställ in och använd Shopify koppling
description: Olika integrationsscenarier för att demonstrera arbetsflöden mellan Shopify och Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector" />Genomgång: ställa in och använda Shopify anslutningsprogram

I det här avsnittet beskrivs några typiska scenarier och du får öva på att testa eller utbilda användare i det integrerade [!INCLUDE[prod_short](../includes/prod_short.md)] området och Shopify butiken.

## <a name="prerequisites" />Förutsättningar

### <a name="shopify" />Shopify

Du måste ha följande:

- Ett Shopify-konto
- En onlinebutik med Shopify

Mer information om hur du skapar Shopify testversioner och rekommenderade inställningar finns i [ skapa och ställa in Shopify konto](shopify-account.md).

### <a name="business-central" />Business Central

Du måste ha ett [!INCLUDE[prod_short](../includes/prod_short.md)]-konto. 

Du kan t.ex. skapa demokonto eller starta utvärdering. Lär dig mer när du [ Förbered demonstrationsmiljöer av Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) och [ Registrera dig för testversionen](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop" />Ansluta Business Central till butiken på Shopify

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör något av följande:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I fältet **kod** ange `DEMO1`.
4. I fältet **Shopify URL** anger du webbadressen till den onlinebutik som du vill ansluta till.
5. Aktivera reglaget **Aktiverad**, granska och godkänn villkoren.

Konfigurera Shopify enligt beskrivningen i följande steg:

1. Slå på brytaren **Logg aktiverad**.
2. Inaktivera reglaget **Tillåt synkronisering i bakgrunden**.
3. Välj **Till Shopify** i fältet **Synkronisera artikel**.
4. Välj **Till Shopify** i fältet **Synkronisera artikelbilder**.
5. Aktivera växlingsknappen **Synkronisera artikelattribut**.
6. Aktivera växlingsknappen **Lager spårat**.
7. Välj **Neka** i fältet **Standardlagerprincip**.
8. Aktivera växlingsknappen **Skapa okända automatiskt**.
9. Fyll i fältet **Kundmallkod** med rätt mall.
10. Fyll i **Leveranskostnadskonto**, **Drickskonto** med intäktskontot. Du kan till exempel använda `40100` i USA.
11. Aktivera växlingsknappen **Skapa order automatiskt**.

Konfigurera platsmappning:

1. Välj åtgärden **Platser** för att öppna **Shopify-butiksplatser**.
2. Välj åtgärden **Hämta Shopify-platser** för att importera alla platser som har definierats i Shopify.
3. I **Platsfilter**, ange `''|EAST|MAIN`.
4. Inaktivera **Inaktiverad** för att aktivera lagersynkronisering för utvalda Shopify-plats.

## <a name="walkthrough-start-selling-products-online" />Genom gång: börja sälja produkter online

### <a name="scenario" />Scenario

Anta att du vill prova Shopify som en onlinebutik utan att behöva ägna mycket tid på att skapa saker, speciellt eftersom du redan håller dina artiklar i [!INCLUDE[prod_short](../includes/prod_short.md)] . När du startat Shopify onlinebutiken får du omedelbart nya kunder som är nöjda med din butik och deras inköpsupplevelser. De bestämmer sig för att lämna dricks i kassan.

### <a name="steps" />Steg

I [!INCLUDE[prod_short](../includes/prod_short.md)] gå igenom följande:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-produkter** och välj relaterad länk.
2. Välj åtgärden **Lägg till artiklar**.
3. Ange *Butikskod* i fältet **DEMO1**.
4. Ställ in filtret `CHAIR` i fältet **artikelkategorikod** (lägg till filter fält om det behövs).
5. Välj **OK** och vänta tills den första synkroniseringen av artiklar och priser har slutförts.
6. Välj åtgärden **Synkronisera produktbilder**.
7. Välj åtgärden **Synkronisera lager**.

I **Shopify onlinebutik**
> [!Tip]  
> Öppna **Shopify administration**, genom att gå till URL-adressen som anges i fältet **URL** på sidan **Shopify butikskort**. Välj sedan ögon ikonen bredvid **Online-butiken** försäljningskanalen för onlinebutiken, som finns i listrutan för **Shopify administration**. 

Öppna produktkatalogen. Meddelanden:

* Produkttitlar, bilder och priser.
* Tillgänglighets indikator (säljs för produkter utanför lagret).

Välj en produkt som kan säljas, till exempel `BERLIN Swivel Chair, yellow`. Observera att beskrivningen innehåller objektattribut.

Klicka på knappen **Köp nu** och gå till kassan.

1. I fältet **E-post eller mobilnummer** ange `cl@contoso.com` (eller skicka e-post dit du vill få order- och fraktbekräftelser).
2. I **förnamn** och **efternamn**, ange `Claudia Lawson`.
3. Ange lokal adress.
4. Markera kryssrutan **Spara den här informationen för nästa gång**.
5. Klicka på knappen **Fortsätt till leverans**.
6. Spara `Standard` som leveransmetod och välj knappen **Fortsätt till betalning**.
7. Välj `10%` tips.
8. I fältet **kreditkort** ange `1` om du använder *(för test) Falsk gateway* eller anger `5555 5555 5555 4444` om du använder *Shopify Payments* i testläge.
9. Fyll i fälten **Namn på kort**.
10. I fältet **Utgångsdatumet**, ange aktuell månad/år.
11. I fältet **Säkerhetskod** ange `111`.
12. Klicka på **Betala nu**.

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör något av följande:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify Order** och väljer sedan relaterad länk
2. Välj åtgärden **Synkronisera ordrar från Shopify**.
3. Välj **OK**.

Den importerade ordern är klar för bearbetning.

1. Välj den importerade ordern om du vill öppna fönstret **Shopify Order**.
2. Lägg märke till att den nya kunden och försäljningsordern har skapats.
3. Utforska åtgärder för **Risk** och **Leveranskostnader**.
4. Välj åtgärden **Försäljningsorder** för att öppna fönstret **Försäljningsorder**. Försäljningsorder är ett behov, som om det behövs, kan omfattas av montering, produktion eller inköp med hjälp av planeringsmotorn. Den har också stöd för olika lagerhanteringsprocesser med komplett separation av uppgifter.
5. Välj åtgärden **Öppna igen**.
6. I fältet **Agent** ange `DHL`.
7. I **Godsupplysningsnr.**, ange `123456789`.
8. Välj åtgärden **bokför**, välj alternativet **Leverera och fakturera**, och välj sedan **OK**-knappen.

Nu kan fysiska och ekonomiska data registreras i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det är dags att meddela Shopify om ändringarna.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Synkronisera försändelser till Shopify** och välj relaterad länk.
2. Välj **OK**.

I **Shopify Admin** meddelande om att ordern nu är markerad som *uppfylld*. Du kan också granska försändelseinformationen och visa spårnings-URL:en där. Om du kör **Synkronisera order från Shopify** kommer ordern att arkiveras i båda systemen.

## <a name="walkthrough-invite-your-customers-to-your-new-online-store" />Genomgång: Bjud in dina kunder till din nya onlinebutik

### <a name="scenario-1" />Scenario

Efter en lyckad snabbstart av den nya onlinebutiken vill du att de aktuella kunderna ska besöka den och börja montera order.

### <a name="steps-1" />Steg

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör något av följande:

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den butik **DEMO1** som du vill synkronisera kunder för och öppna sidan **Shopify butikskort**.
3. Välj åtgärden **Synkronisera kunder**.

I **Shopify Admin** meddelande om att kunderna har importerats. Öppna en av kunderna och notera att kundens för- och efternamn kommer från fältet **kontaktnamn** av **kundkortet**. Företagsnamnet kan hittas i standard adressen som är kopplat till kunden. Välj **Skicka kontodeltagare** för att bjuda in kunden.

## <a name="walkthrough-fine-tuning-of-item-management" />Genomgång: finjustering av artikelhantering

### <a name="scenario-2" />Scenario

Du vill lägga till mer flexibilitet och kontrollera dina processer runt objekthantering. Du vill förbättra produktbeskrivningen och vill lägga till fler granskningssteg innan produkterna blir tillgängliga för slutkunden.

### <a name="steps-2" />Steg

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör något av följande:

Förbereda data.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kundprismall** och väljer sedan relaterad länk.
2. Lägg till en ny prisgrupp. I fältet **kod** ange `SHOPIFY`.
3. Stäng fönstret **Kundprisgrupp**.
4. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.

Välj artikel **1896-S, Aten skrivbord** och kör följande steg.

1. Välj åtgärden för **varianter** och Lägg sedan till två varianter `PREMIUM, Athens Desk, Premium edition` och `ESSENTIAL, Athens Desk, Essential edition`.
2. Välj åtgärden **utökad text** och skapa en ny utökad text som gäller för alla språkkoder. I fältet **Beskrivning** ange `Shopify`. 
3. Lägg till följande text med HTML-taggar: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`.
4. Välj åtgärden **försäljningspriser** och lägg till nya priser som visas i följande tabell:

  |Rad|**Förs.typ**|**Förs.kod**|Kontakttyp|Kod|Variantkod<br>(lägg till fältet via anpassning)|Styckpris|
  |------|------------|------------|------------|------------|------------|------------|
  |1|Kundprisgrupp|SHOPIFY|Artikel|1896-S|ESSENTIAL|700|
  |2|Kundprisgrupp|SHOPIFY|Artikel|1896-S|PREMIUM|1 000|

5. Välj åtgärden **försäljningsrabatter** och lägg till en ny rabatt:

* **Försäljningstyp** *Kundrabattgrupp*
* **Förs.kod** *BUTIK*
* **Typ** *Artikel*
* **Kod** *1896-S*
* **Måttenhetskod** *PCS*
* **Radrabatt %** *10*

6. Välj åtgärden **artikelreferenser** och följande lägg till rader:

  |Rad|**Referenstyp**|**Referensnr**|Variantkod|
  |------|------------|------------|------------|
  |1|Streckkod|77777777|ESSENTIAL|
  |2|Streckkod|11111111|PREMIUM|


Välj artikeln **1920-S, ANTWERP konferensbord** och kör följande steg.

1. Välj **Justera lager** och ange fältet **Nytt lager** ange `100` för plats *ÖST* och *VÄST*. 
2. Välj **OK**.

Justera inställningar för synkronisering.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den *DEMO1* butik som du vill synkronisera artiklar för och öppna sidan Shopify butikskort.
3. Välj *SHOPIFY* i fältet **kundprisgrupp** .
4. Välj *BUTIK* i fältet **Kundrabattgrupp** .
5. Aktivera fältet **Synkronisera utökad text för artikel**.
6. Välj *Artikelnr + variantkod* i fältet **SKU-mappning** .
7. Välj *utkast* i fältet **status för skapade produkter** .
8. Välj *status att arkivera* i fältet **åtgärd för borttagen produkt** .

Kör synkronisering.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den *DEMO1* butik som du vill synkronisera artiklar för och öppna sidan **Shopify butikskort**.
3. Välj åtgärden **Produkter** för att öppna fönstret **Shopify Produkter**.
4. Välj åtgärden **Lägg till artiklar**.
5. Ange filter *TABLE* på fältet **Artikelkategorikod**.
6. Välj åtgärden **Synkronisera produktbilder**.
7. Välj åtgärden **Synkronisera lager**.

Produkter läggs till. Observera att statusen är *utkast* och att objekt inte visas i Shopify onlinebutiken.

1. Välj rad med artikel *1920-S, ANTWERP konferensbord*. I fältet **SEO-rubrik**, ange `Rectangular meeting table Antwerp, 10 seats, black`.
2. Markera *Aktiv* i fältet **Status**.
3. Markera raden med artikel *1906-S, ATHENS, mobil pelare* och välj åtgärd **Ta bort**.

I **Shopify Admin**-meddelandet att alla produkter har olika status.

* *ANTWERP Conference-tabell* är *aktiv* eftersom vi ändrade status i fönstret **Shopify produkt**.
* *ATHENS Desk* är *utkast* eftersom vi konfigurerade standard status för alla tillagda produkter som *utkast*.
* *ATHENS mobil pelare* är *arkiverad* eftersom vi konfigurerade butiken att automatiskt tilldela status *arkiverat* för borttagna produkter.

Observera att lager för ANTWERP Conference-tabellen är 100 eftersom vi har konfigurerat systemet att använda lager endast från två platser HUVUD och ÖSTRA. Lagret på andra platser (VÄST) ignoreras.

* Öppna *ANTWERP Conference-tabell*, meddelande **Anpassad typ**, **leverantör**, **vikt**, **kostnad per artikel** och avsnittet **förhandsversion av sökmotorlista**.
* Öppna *Athens Desk*, bläddra ned till avsnittet **varianter** och lägg märke till hur **SKU** är ifyllt.
* Väl **Redigera** om du vill granska streckkoder och priser.
* Ändra status för *Aten Desk* till *aktiv* och välj **Förhandsgranska**-åtgärd.

I **Shopify onlinebutik** öppna produktkatalogen, hitta *ATHENS Desk*-produkten. Lägg märke till att olika alternativ är tillgängliga. För olika alternativ är priserna olika. Beakta information om rabatt.

## <a name="walkthrough-import-items-from-shopify" />Genomgång: Importera artiklar från Shopify

### <a name="scenario-3" />Scenario

Du har redan en lyckad onlinebutik och vill börja använda [!INCLUDE[prod_short](../includes/prod_short.md)] som verksamhetshanteringsprogram. Du vill importera så mycket data Shopify som möjligt. 

### <a name="steps-3" />Steg

Det här är en förlängning av [ genomgången: påbörja försäljning av produkter online](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Du kan också prova med egna data, till exempel Shopify butiken eller sandbox.

I [!INCLUDE[prod_short](../includes/prod_short.md)], gör något av följande:

#### <a name="prepare-data" />Förbereda data

1. Växla till en kostnadsfri provperiod på 30 dagar utan exempeldata. Mer information finns i [ lägga till egna data till en tom testversion](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
3. Välj åtgärden **Ny**.
4. I fältet **kod** ange `DEMO2`.
5. I fältet **Shopify URL** anger du webbadressen till den onlinebutik som du vill ansluta till.
6. Aktivera reglaget **Aktiverad**, granska och godkänn villkoren.

Konfigurera Shopify enligt beskrivningen i följande steg:

7. Aktivera brytaren **Logg aktiverad**.
8. Inaktivera reglaget **Tillåt synkronisering i bakgrunden**.
9. Välj **Från Shopify** i fältet **Synkronisera artikel**.
5. Aktivera växlingsknapp **Skapa okända artiklar automatiskt**.
11. Fyll i fältet **Artikelmallkod** med rätt mall.
12. Välj **Från Shopify** i fältet **Synkronisera artikelbilder**.
13. Välj **Alla kunder** i **kundimporten från Shopify**.
14. Aktivera växlingsknapp **Skapa okända kunder automatiskt**.
15. Fyll i fältet **Kundmallkod** med rätt mall.
16. Fyll i **Leveranskostnadskonto**, **Drickskonto** med intäktskontot. Du kan till exempel använda `40100` i USA.
17. Aktivera växlingsknappen **Skapa order automatiskt**.

#### <a name="run-the-synchronization" />Kör synkronisering

1. Välj ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den *DEMO2* butik som du vill synkronisera data för och öppna sidan **Shopify butikskort**.
3. Välj åtgärden **Synkronisera produkter**.
4. Välj åtgärden **Synkronisera produktbilder**.
5. Välj åtgärden **Synkronisera kunder**.

### <a name="results" />Resultat

* Shopify produkter importeras. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-produkter** och välj relaterad länk.
* Objekt med bilder skapas. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artikel** och välj sedan relaterad länk.
* Shopify kunderna importeras. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") ikon, ange **Shopify Kunder** och väljer sedan relaterad länk.
* Kunderna skapas. Välj ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") ikon, ange **Kunder** och väljer sedan relaterad länk.


## <a name="see-also" />Se även

[Kom igång med Shopify-kopplingen](get-started.md)  
