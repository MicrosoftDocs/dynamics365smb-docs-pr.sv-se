---
title: Synkronisera kunder
description: Importera kunder från eller exportera kunder till Shopify
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
---

# <a name="synchronize-customers-and-companies"></a>Synkronisera kunder och företag

När en order importeras från Shopify är informationen om kunden väsentlig för ytterligare behandling av dokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finns två huvudalternativ och flera kombinationer:

* Använd särskild kund för alla order.
* Importera information om kunden från Shopify. Det här alternativet är också tillgängligt när du exporterar kunder till Shopify från [!INCLUDE[prod_short](../includes/prod_short.md)].

Shopify låter dig driva din B2B- och DTC-verksamhet från ett ställe med kraften och enkelheten hos Shopify allt-i-ett-plattformen. Shopify anslutningsprogram fungerar också med olika smaker av e-handel.

Medan Shopify har två enheter, kund och företag, men [!INCLUDE[prod_short](../includes/prod_short.md)] bara har kundenheten, vilket påverkar hur synkroniseringen fungerar.

När du kör DTC skapas köparen i Shopify som en kund. Kunden importeras sedan till [!INCLUDE[prod_short](../includes/prod_short.md)] som Shopify-kund och länkas eller konverteras till en kund.

Om du kör B2B skapas köparen i Shopify som en kund kopplad till ett företag. Kunden importeras till [!INCLUDE[prod_short](../includes/prod_short.md)] som Shopify-kund och företaget importeras till [!INCLUDE[prod_short](../includes/prod_short.md)] som Shopify-företag och länkas eller konverteras till en kund.

Om du vill exportera en kund från [!INCLUDE[prod_short](../includes/prod_short.md)] till Shopify är stegen något olika beroende på vad du vill göra:

* Exportera en kund som Shopify-kund för DTC.
* Exportera en kund som företag och kundpar för B2B-flödet.

## <a name="important-settings-when-importing-dtc-customers-from-shopify"></a>Viktiga inställningar när du importerar DTC-kunder från Shopify

Antingen importerar du kunder från Shopify i bulk eller tillsammans med orderimporten. Du kan hantera processen med följande inställningar:

|Fält|Beskrivning|
|------|-----------|
|**Kundimport från Shopify**|Välj **Alla kunder** om du planerar att importera kunder från Shopify i bulk, antingen manuellt med åtgärden **Synkronisera kunder** eller via jobbkön för återkommande uppdateringar. Oavsett val importeras alltid kundinformationen tillsammans med ordrar. Användningen av den här informationen beror emellertid på **Shopify-kundmallar** och inställningar i fältet **Kundmappningstyp**.|
|**Kundmappningstyp**|Definiera hur kopplingen ska utföra mappning.</br></br>- **Via e-post/telefon** om du vill att anslutningsprogrammet använder information från e-post och telefon för att mappa importerad Shopify-kund till en kund i Business Central.</br></br>- **Genom faktureringsinfo** om du vill att anslutningsprogrammet ska använda adressen för fakturamottagaren för att mappa importerad Shopify-kund till befintlig kund i Business Central.</br></br>Välj **Ta alltid standardkunden** om du vill att systemet använder en kund från **Standardkundnr** . |
|**Shopify kan uppdatera kunder**| Välj detta fält om du vill att kopplingen uppdaterar kunder som hittas, när något av alternativen **Via e-post/telefon** eller **Genom faktureringsinfo** har valts i fältet **Kundmappningstyp**.|
|**Skapa okända kunder automatiskt**| Välj detta fält om du vill att kopplingen skapar saknade kunder när något av alternativen **Via e-post/telefon** eller **Genom faktureringsinfo** har valts i fältet **Kundmappningstyp**. En ny kund skapas med hjälp av importerade data och **Kod för kundmall** definierad på någon av sidorna **Shopify-butikskort** eller **Shopify-kundmall**. Observera att Shopify-kunden måste ha minst en adress. Order som skapats via Shopify POS försäljningskanal saknar ofta adressinformation. Om alternativet inte har aktiverats måste du skapa kunden manuellt och koppla den till Shopify-kunden.|
|**Mallkod för kund.företag**|Använd detta fält tillsammans med **Skapa okända kunder automatiskt**.</br></br> Välj den standardmall som ska användas för automatiskt skapade kunder. Kontrollera att den valda mallen innehåller de obligatoriska fälten, till exempel **Gen. rörelsebokföringsmall**, **Kundbokföringsmall** och moms eller momsrelaterade fält.</br></br>Du kan definiera mallar per land/region i sidan **Shopify-kundmallar**, vilket är användbart för korrekt momsberäkning.</br></br>Läs mer i [Ställa in moms](setup-taxes.md).|

### <a name="customer-template-per-countryregion"></a>Kundmall per land/region

Vissa inställningar kan definieras på lands-/regionnivå eller på läns-/provinsnivå. Inställningarna kan konfigureras i [Leverans](https://www.shopify.com/admin/settings/shipping) på Shopify.

Med **Shopify-kundmallen** kan du göra följande för varje kund:

1. Ange **Standardkundnr**, vilket har högre prioritet än valen i fälten **Kundimport från Shopify** och **Kundmappningstyp**. Används i den importerade försäljningsordern.
2. Definiera **Kod för kundmall**, som används för att skapa saknade kunder om **Skapa okända kunder automatiskt** har aktiverats. Om **Kod för kundmall** är tom använder funktionen **Kod för kundmall** som har definierats på **Shopify-butikskortet**. Systemet försöker först hitta en mall för **lands-/regionkod** för standardadressen. Om det inte finns någon mall används den första adressen.
3. I vissa fall räcker inte den **Kod för kundmall** som definieras för ett land/region inte för att säkerställa korrekt beräkning av skatter (till exempel för länder/regioner med moms). I det här fallet kan **skatteområden** vara ett användbart tillägg.
4. Fältet **Momsområde** innehåller också **Landsnummer** och **Landsnamn**. Det här paret är användbart när kopplingen måste konvertera en kod till ett namn eller vice versa.

> [!NOTE]  
> Landskoderna är ISO 3166-1 alpha-2 landskoder. Läs mer om [landskod](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="important-settings-when-exporting-dtc-customers-to-shopify"></a>Viktiga inställningar när du exporterar DTC-kunder till Shopify

Du kan exportera befintliga kunder till Shopify i bulk. I varje fall kommer en kund och en standardadress skapas. Med följande inställningar kan du hantera processer:

|Fält|Description|
|------|-----------|
|**Kan uppdatera Shopify-kunder**| Aktivera om du till generera uppdateringar senare från Business Central för kunder som redan finns i Shopify.|

Följande krav gäller för export av en kund:

* Kunden måste ha en giltig e-postadress.
* När du exporterar kunder med adresser som inkluderar provinser/stater måste du se till att **ISO-koden** fylls i för länder/regioner.|
* För land/region har valts på kundkortet kontrollerar du **ISO-kod**. För lokala kunder, med tomt land/region, använder Shopify-anslutningsprogrammet det land/den region som anges i **Företagsinformation**.
* Om kunden har ett telefonnummer måste numret vara unikt eftersom Shopify inte ska acceptera ytterligare en kund med samma telefonnummer.
* Om kunden har ett telefonnummer måste det vara i formatet E.164. Olika format stöds om de representerar ett tal som kan ringas upp var som helst i världen. Följande format är giltiga:

  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

När du skapar kunderna i Shopify kan du skicka direkt inbjudningar till dem och på så vis uppmuntra dem att aktivera sina konton.

### <a name="populate-customer-information-in-shopify"></a>Fylla i kundinformation i Shopify

En kund i Shopify har förnamn, efternamn, e-post och/eller telefonnummer. Du kan ange förnamn och efternamn baserat på namn på kundkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Fält i kundkort|Description|
|------|------|-----------|
|1|**Kontaktnamn**|Högsta prioritet om fältet **Kontaktnamn** har fyllts i och fältet **Kontaktkälla** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|
|2|**Namn 2**|Om fältet **Namn 2** har fyllts i och fältet **Källa till namn 2** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|
|3|**Namn**|Lägsta prioritet om fältet **Namn** har fyllts i och fältet **Namnkälla** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|

Det finns också en standardadress för en kund i Shopify. Adressen kan innehålla ett företag och en adress utöver förnamn, efternamn, e-post och/eller telefon. Du kan fylla i fältet **Företag** baserat på data från kundkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Fält i kundkort|Description|
|------|------|-----------|
|1|**Namn**|Högsta prioritet om fältet **Namnkälla** på **Shopify-butikskortet** innehåller *Företagsnamn*.|
|2|**Namn 2**|Lägsta prioritet om fältet **Källa till namn 2** på **Shopify-butikskortet** innehåller *Företagsnamn*.|

För adresser där delstat/provins används väljer du **Kod** eller **Namn** i fältet **delstatskälla** på sidan **Shopify-butikskort**. Koden eller namnet anger vilken typ av data som lagras i [!INCLUDE[prod_short](../includes/prod_short.md)] i fältet **Delstat**. Kom ihåg att initiera kundmallar per land/region så att delstatskoden/namnmappningen är klar. 

## <a name="export-dtc-customers-to-shopify"></a>Exportera DTC-kunder till Shopify

### <a name="initial-sync-of-customers-from-business-central-to-shopify"></a>Inledande synkronisering av kunder från Business Central till Shopify

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikon, ange **Shopify Kunder** och väljer sedan relaterad länk.
2. Välj åtgärden **Lägg till kund**.
3. Ange koden i fältet **Butikskod**. Om du öppnar fönstret **Shopify-kunder** från sidan **Butikskort** fylls butikskoden i automatiskt.
4. Definiera filter för kunder efter behov. Du kan till exempel filtrera efter lands-/regionkod.
5. Välj **OK**.

De resulterande kunderna skapas automatiskt i Shopify med adress.

> [!NOTE]  
> Inledande synkronisering av kunder från [!INCLUDE[prod_short](../includes/prod_short.md)] till Shopify överväger inte inställningen **Kan uppdatera Shopify-kunder**.

### <a name="sync-customers"></a>Synka kunder

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den specifika butik som du vill synkronisera kunder för.
3. Välj åtgärden **Synkronisera kunder**.

Alternativt kan du använda åtgärden **Starta synkronisering av kunder** i fönstret **Shopify-kunder** eller söka efter batchjobbet **Synkronisera kunder**.

Du kan schemalägga uppgifter så att de utförs på ett automatiserat sätt. Läs mer i [Schemalägg återkommande uppgifter](background.md#to-schedule-recurring-tasks).

## <a name="b2b-companies"></a>B2B-företag

Om du använder B2B i Shopify kan du förutom kunder också skapa företag. Du kan koppla en eller flera enskilda kunder till ett företag. Du kan även definiera betalningsvillkor, platser och kataloger.

## <a name="important-settings-when-importing-b2b-companies-from-shopify"></a>Viktiga inställningar när du importerar B2B-företag från Shopify

Oavsett om du importerar företag från Shopify i bulk eller tillsammans med orderimporten kan du använda inställningarna i följande tabell för att hantera processen.

|Fält|Description|
|------|-----------|
|**Företagsimport från Shopify**|Välj **Alla företag** om du planerar att importera kunder från Shopify i bulk, antingen manuellt med åtgärden **Synkronisera företag** eller via jobbkön för återkommande uppdateringar. Oavsett val importeras alltid kundinformationen tillsammans med ordrar. Användningen av den här informationen beror emellertid på **Shopify-företagsmallar** och inställningar i fältet **Typ av företagsmappning**.|
|**Typ av företagsmappning**|Definiera hur anslutningsprogrammet ska utföra mappning.</br></br>- **Via e-post/telefon** om du vill att anslutningsprogrammet mappar importerade Shopify-företag till befintliga kunder i Business Central med hjälp av e-post och telefon från huvudkontakten.</br></br>- Välj **Ta alltid standardföretaget** om du vill att systemet använder ett företag i **Standardföretagsnr** . |
|**Shopify kan uppdatera företag**| Välj detta fält om du vill att anslutningsprogrammet uppdaterar kunder som hittas, när alternativet **Via e-post/telefon** har valts i fältet **Typ av företagsmappning**.|
|**Skapa okända företag automatiskt**| Välj detta fält om du vill att anslutningsprogrammet skapar nya kunder när alternativet **Via e-post/telefon** har valts i fältet **Typ av företagsmappning**. En ny kund skapas med hjälp av importerade data och **Kod för kund-/företagsmall** definierad på någon av sidorna **Shopify-butikskort** eller **Shopify-kundmall**.|
|**Mallkod för kund/företag**|Använd detta fält tillsammans med **Skapa okända företag automatiskt**.</br></br>- Välj den standardmall som ska användas för automatiskt skapade kunder. Se till att de obligatoriska fälten är ifyllda på mallen, t.ex. **Gen. rörelsebokföringsmall**, **Kundbokföringsmall**, **Moms** eller andra momsrelaterade fält.</br></br>- Du kan definiera mallar per land/region i sidan **Shopify-kundmallar**, vilket är användbart för korrekt momsberäkning.</br></br>Läs mer i [Ställa in moms](setup-taxes.md).|

> [!NOTE]  
> Företaget måste ha en huvudkontakt. Annars hoppar anslutningsprogrammet över till företaget.
> Endast ett äldsta lagerställe importeras.
> Endast huvudkontakten importeras.

## <a name="important-settings-when-exporting-b2b-companies-to-shopify"></a>Viktiga inställningar när du exporterar B2B-företag till Shopify

Du kan exportera befintliga kunder till Shopify i bulk som ett företag. I varje fall skapas ett företag och en standardplats och en huvudkontakt. Det är också möjligt att skapa en katalog.

|Fält|Description|
|------|-----------|
|**Kan uppdatera Shopify-företag**| Aktivera om du till generera uppdateringar senare från Business Central för företag som redan finns i Shopify.|
|**Standardkontaktbehörigheter**| Ange vilka behörigheter som måste tilldelas huvudkontakten, du kan välja mellan **Ingen**, **Endast beställning** och **Platsadministratör**.|
|**Skapa katalog automatiskt**| Aktivera det här alternativet om du vill skapa en katalog som innehåller alla produkter. En katalog skapas för varje exporterat företag.|

## <a name="export-b2b-company-to-shopify"></a>Export B2B-företag till Shopify

### <a name="initial-sync-of-b2b-companies-from-business-central-to-shopify"></a>Inledande synkronisering av B2B-företag från Business Central till Shopify

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-företag** och välj relaterad länk.
2. Välj åtgärden **Lägg till företag**.
3. Ange koden i fältet **Butikskod**. Om du öppnar fönstret **Shopify-företag** från sidan **Butikskort** fylls butikskoden i automatiskt.
4. Definiera filter för kunder efter behov. Du kan till exempel filtrera efter lands-/regionkod.
5. Välj **OK**.

De resulterande företaget och kunderna skapas automatiskt i Shopify.

> [!NOTE]  
> Inledande synkronisering av företag från [!INCLUDE[prod_short](../includes/prod_short.md)] till Shopify överväger inte inställningen **Kan uppdatera Shopify-företag**.

### <a name="sync-b2b-company"></a>Synkronisera B2B-företag

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den specifika butik som du vill synkronisera kunder för.
3. Välj åtgärden **Synkronisera företag**.

Alternativt kan du använda åtgärden **Synkronisera företag** på sidan **Shopify-företag** eller söka efter batchprojektet **Synkronisera företag**.

Du kan schemalägga uppgifter så att de körs på ett automatiserat sätt. Läs mer i [Schemalägg återkommande uppgifter](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Se även

[Kom igång med kopplingen för Shopify](get-started.md)  
