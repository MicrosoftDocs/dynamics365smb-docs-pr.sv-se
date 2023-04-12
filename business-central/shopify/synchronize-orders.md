---
title: Synkronisera och uppfylla försäljningsordrar
description: Konfigurera och kör import och behandling av försäljningsordrar från Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129,'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Synkronisera och uppfylla försäljningsordrar

I den här artikeln beskrivs nödvändiga inställningar och steg som måste slutföras för att synkronisera och uppfylla försäljningsordrar från Shopify i [!INCLUDE[prod_short](../includes/prod_short.md)].

## Ange import av ordrar på Shopify-butikskortet

Ange en **valutakod** om din onlinebutik använder en annan valuta än den lokala valutan (BVA). Den angivna valutan måste ha växlingskurser konfigurerade. Lämna fältet tomt om din onlinebeställning använder samma valuta som [!INCLUDE[prod_short](../includes/prod_short.md)]. 

Du kan se butiksvalutan i inställningarna [butiksinformation](https://www.shopify.com/admin/settings/general) i din Shopify Admin. Shopify kan konfigureras så att olika valutor accepteras, men importerade order kan användas i [!INCLUDE[prod_short](../includes/prod_short.md)] butiksvaluta.

En vanlig Shopify-order kan inkludera kostnader förutom delsumman, till exempel fraktkostnader eller dricks. Dessa belopp bokförs direkt till det redovisningskonto som du vill använda för specifika transaktionstyper:

* **Konto för leveransavgifter**
* **Konto för sålda presentkort**: mer information finns på [Presentkort](synchronize-orders.md#gift-cards)
* **Drickskonto**  

Aktivera **Skapa ordrar automatiskt** för att automatiskt skapa försäljningsdokument i [!INCLUDE[prod_short](../includes/prod_short.md)] när Shopify-ordern har importerats.

Om du vill släppa ett försäljningsdokument automatiskt aktiverar du alternativet **Frisläpp försäljningsorder automatiskt**.

Försäljningsdokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)] länkar till Shopify ordern, och du kan lägga till ett fält som inte redan visas på sidan. Om du vill veta mer om hur du lägger till ett fält går du till [Börja anpassa en sida med banderollen **Anpassa**](../ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner). Om du aktiverar **Shopify-ordernr på dokumentraden** upprepas den här informationen på försäljningsraden som **Kommentar**.

I fältet **Skatteområdeskälla** kan du definiera prioritet för hur skatteområdeskod eller rörelsebokföringsmallar för moms ska väljas baserat på adress. Den importerade Shopify ordern innehåller information om skatt, men momsen kommer att räknas om när du skapar försäljnings dokumentet så det är viktigt att moms-och moms inställningarna är korrekta i [!INCLUDE[prod_short](../includes/prod_short.md)]. Mer information om moms finns i [ställa in moms för Shopify anslutningen](setup-taxes.md).

### Mappning av utleveransmetoder

**Kod för utleveransmetod** för försäljningsdokument som importeras från Shopify kan fyllas i automatiskt. Du måste konfigurera **Mappning av utleveransmetoder**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill definiera mappning för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Mappning av utleveransmetoder**. Posterna för utleveransmetoder som definierats i inställningarna för [**Leverans**](https://www.shopify.com/admin/settings/payments) under **Shopify-admin** skapas automatiskt.
4. I fältet **Namn** ser du namnet på utleveransmetoden från Shopify.
5. Ange **Kod för utleveransmetod** med motsvarande utleveransmetod i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Om flera leveranskostnader är kopplade till en försäljningsorder väljs endast en som utleveransmetod och tilldelas försäljningsdokument.

### Mappning av platser

Platsmappning krävs för tre syften:

* För att synkronisera inventeringen finns mer information i [Synkronisera inventering till Shopify](synchronize-items.md#sync-inventory-to-shopify)
* Om du vill fylla i **lagerställekod** för försäljningsdokument som importerats från Shopify. Detta är viktigt om växlingsknappen **Lagerställe ska finnas** aktiveras kort för **Lagerinställningar** annars kommer du inte att kunna skapa försäljningsdokument.
* För att uppdatera Shopify ordern med information om uppfyllelse baserat på sidan **bokförda utleveranser**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill konfigurera kartläggningen av platser för att öppna **Shopify-butikskort**.
3. Välj åtgärden **Platser** för att öppna **Shopify-butiksplatser**.
4. Välj åtgärden **Hämta Shopify-platser** för att importera alla platser som har definierats i Shopify. Du hittar dem i inställningarna för [**Platser**](https://www.shopify.com/admin/settings/locations) under panelen **Shopify-admin**. Observera att platsen som är markerad som *standard* kommer att användas när du importerar ouppfyllda Shopify order.
5. Ange **Kod för standardlagerställe** med motsvarande plats i [!INCLUDE[prod_short](../includes/prod_short.md)].

## Kör ordersynkronisering

Följande förfarande beskriver hur du importerar och uppdaterar försäljningsordrar.

> [!NOTE]  
> Det går inte att importera arkiverade ordrar i Shopify. Inaktivera **Arkivera order automatiskt** i avsnittet **Orderbehandling** av inställningarna för **kassan** under **Shopify-admin** för att säkerställa att alla ordrar importeras till [!INCLUDE[prod_short](../includes/prod_short.md)]. Om du behöver importera arkiverade ordrar använder du åtgärden **Avarkivera ordrar** på sidan [Ordrar](https://www.shopify.com/admin/orders) på panelen **Shopify admin**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill importera ordrar för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Ordrar**.
4. Välj åtgärden **Synkronisera ordrar från Shopify**.
5. Definiera filter för ordrar vid behov. Du kan till exempel importera helt betalda ordrar eller de som har låg risknivå.

> [!NOTE]  
> När du filtrerar efter tagg bör du använda filtertoken `@` och `*`. Om du t. ex. vill importera order som innehåller *tag1* använder du `@*tag1*`. `@` kommer att säkerställa att resultatet är skiftlägesokänsligt, medan `*` hitta beställningar med flera taggar.

6. Välj **OK**.

Du kan också söka efter batchjobbet **Synkronisera ordrar från Shopify**.

Du kan schemalägga uppgifter så att de utförs på ett automatiserat sätt. Läs mer i [Schemalägg återkommande uppgifter](background.md#to-schedule-recurring-tasks).

## Granska importerade order

När importen är klar kan du utforska Shopify beställa och hitta all relaterad information, såsom betalningstransaktioner, fraktkostnader, risknivå, orderattribut och taggar eller uppfyllelser, om beställningen redan utfördes i Shopify. Du kan också se orderbekräftelser som har skickats till kunden genom att välja åtgärden **Shopify-statussida**.

> [!NOTE]  
> Du kan navigera till fönstret **Shopify-ordrar** direkt, så visas ordrar med statusen *Öppen* från alla butiker. För att granska slutförda ordrar måste du öppna sidan **Shopify-ordrar** från fönstret **Shopify-butikskort**.

## Skapa försäljningsdokument i Business Central

Om reglaget **Skapa ordrar automatiskt** har aktiverats på **Shopify-butikskortet** försöker [!INCLUDE[prod_short](../includes/prod_short.md)] att skapa ett försäljningsdokument när ordern har importerats. Om problem som en saknad kund eller produkt uppstår måste du åtgärda problemen och sedan skapa försäljningsordern igen.

### Skapa försäljningsdokument

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill synkronisera ordrar för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Ordrar**.
4. Välj den order som du vill skapa ett försäljningsdokument för och välj åtgärden **Skapa försäljningsdokument**.
5. Välj **Ja**.

Om Shopify-ordern måste uppfyllas skapas **försäljningsordern**. För uppfyllda Shopify order, t.ex. order som endast innehåller ett presentkort eller som redan hanteras i Shopify, skapas **försäljningsfakturan**.

Ett försäljningsdokument skapas nu och kan hanteras med hjälp av standardfunktionerna i [!INCLUDE[prod_short](../includes/prod_short.md)].

### Hantera saknade kunder

Om inställningarna gör att en kund inte kan skapas automatiskt och en befintlig kund inte kan hittas tilldelar du en kund till Shopify-ordern manuellt. Detta kan göras på några få sätt:

* Du kan tilldela **Försäljningskundnr** och **Faktureringskundnr.** direkt på sidan **Shopify-ordern** genom att välja en kund i listan över befintliga kunder.
* Du kan välja en kundmallskod, skapa och tilldela kunden via åtgärden **Skapa ny kund** i **Shopify-ordern**. Observera att Shopify-kunden måste ha minst en adress. Order som skapats via Shopify POS försäljningskanal saknar ofta adressinformation.
* Du kan mappa befintliga kunder till relaterade **Shopify-kunder** i fönstret **Shopify-kunder** och sedan välja åtgärden **Hitta mappning** i **Shopify-ordern**.

### Så väljer kopplingen vilken kund som ska användas

Funktionen *Importera order från Shopify* försöker att välja kunder i följande ordning:

1. Om **Standardkundnr** definieras i **Shopify-kundmall** för motsvarande land används **Standardkundnr** oavsett inställningar i **Kundimport från Shopify** och **Kundmappningstyp**. Läs mer i [Kundmall per land](synchronize-customers.md#customer-template-per-country).
2. Om **Kundimport från Shopify** anges till *Ingen* och **Standardkundnr.** definieras på sidan **Shopify butikskort**, sedan **Standardkundnr.** .

Nästa steg beror på **Kundmappningstyp**.

* Om det är **Ta alltid standardkunden** använder kopplingen sedan kunden som definierats i fältet **Standardkundnr** på sidan **Shopify-butikskort**.
* Om det är **Via e-post/telefon** försöker kopplingen hitta befintliga kunder genom ID först, sedan via e-post och sedan via telefonnummer. Om kunden inte hittas skapar kopplingen en ny kund.
* Om det är **Genom faktureringsinfo** försöker kopplingen att hitta befintliga kunder genom ID först och sedan genom information om faktureringsadressen. Om kunden inte hittas skapar kopplingen en ny kund.

> [!NOTE]  
> Kopplingen använder information från faktureringsadressen och skapar en faktureringskund i [!INCLUDE[prod_short](../includes/prod_short.md)]. Försäljningskunden är densamma som faktureringskunden.

### Effekten av orderredigering

I Shopify:

|Redigera|Påverkan för redan importerad order|Påverkan för order som importeras för första gången|
|------|-----------|-----------|
|Ändra uppfyllelseplatsen | Den ursprungliga platsen är i rader | En uppfyllelseplats är synkroniserad med [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Redigera en order och öka antal| Orderhuvud och tilläggstabeller uppdateras på [!INCLUDE[prod_short](../includes/prod_short.md)] rader.| Importerad order kommer att använda ny kvantitet|
|Redigera en order och minska antal| Orderhuvud och tilläggstabeller uppdateras på [!INCLUDE[prod_short](../includes/prod_short.md)] rader.| Den importerade ordern kommer att använda den ursprungliga kvantiteten, fältet bevarat antal innehåller ett nytt värde.|
|Redigera en order och ta bort befintlig artikel | Orderhuvud och tilläggstabeller uppdateras på [!INCLUDE[prod_short](../includes/prod_short.md)] rader.| Borttagen artikel importeras fortfarande kommer fältet uppfyllt antal att innehålla noll. |
|Redigera en order och lägg till nytt objekt | Orderrubriken uppdateras, raderna kommer inte att uppdateras. | Ursprungliga och tillagda objekt kommer att importeras. |
|Bearbetningsorder: uppfyllelse, uppdatera betalningsinformation | Orderrubriken uppdateras, raderna kommer inte att uppdateras. |Ändringen påverkar inte hur order importeras.|
|Annullera order | Orderrubriken uppdateras, raderna kommer inte att uppdateras. |Annullerad order importeras inte |

I [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Redigera|Påverkan|
|------|-----------|
|Ändra platsen till en annan plats, mappad till Shopify platserna. Bokför leverans. | Ordern markeras som uppfylld. Den ursprungliga platsen kommer att användas. |
|Ändra platsen till en annan plats, mappad inte till Shopify platserna. Bokför leverans. | Uppfyllelse kommer inte att synkroniseras med Shopify. |
|Minska antal. Bokför leverans. | Ordern i Shopify markeras som delvis uppfylld. |
|Öka antal. Bokför leverans. | Uppfyllelse kommer inte att synkroniseras med Shopify. |
|Lägg till ett nytt objekt. Bokför leverans. | Ordern i Shopify markeras som uppfylld. Raderna uppdateras inte. |

## Synkronisera försändelser till Shopify

När en försäljningsorder som skapas från en Shopify-order skickas kan du synkronisera försändelserna till Shopify.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Synkronisera försändelser till Shopify** och välj relaterad länk.
2. Definiera filter för försändelser vid behov. Du kan till exempel uppdatera försändelsen som bokförts ett visst datum.
3. Välj **OK**.

Ordern i Shopify markeras som uppfylld. Kunden meddelas automatiskt om försändelsen via e-post eller SMS. Om en speditör och en spårningskod anges på försändelsen inkluderas spårningsinformationen i e-postmeddelandet.

Du kan också använda åtgärden **Synkronisera utleveranser** på sidorna Shopify försäljningsorders eller Shopify butik.

Du kan schemalägga uppgifter så att de utförs på ett automatiserat sätt. Läs mer i [Schemalägg återkommande uppgifter](background.md#to-schedule-recurring-tasks).

>[!Important]
>Platsen, inklusive tom plats, som definieras i raden Bokad leverans måste ha en matchande post i Shopify plats. Annars kommer den här raden inte att skickas tillbaka till Shopify. Lära dig mer på [platsmappning](synchronize-orders.md#location-mapping).

Glöm inte att köra **Synkronisera ordrar från Shopify** för att uppdatera uppfyllandestatusen för ordern i [!INCLUDE[prod_short](../includes/prod_short.md)]. Kopplingsfunktionen arkiverar också helt betalda och uppfyllda ordrar i både Shopify och [!INCLUDE[prod_short](../includes/prod_short.md)] under förutsättning att villkoren uppfylls.

### Speditörer och spårnings-URL

Om dokumentet **Bokförd utleverans** innehåller **Speditörskod** och/eller **Paketspårningsnr** skickas den här informationen till Shopify och slutkunder i ett e-postmeddelande med bekräftelse på försändelsen.

Spårningsföretaget fylls i följande ordning (från högsta till lägsta) baserat på fraktagentens post:

* **Shopify-spårningsföretag**
* **Namn**
* **Kod**

Om fältet **Spårnings-URL för paket** har fyllts i för posten Speditör innehåller också försändelsebekräftelsen en spårnings-URL.

## Presentkort

I Shopify-butiken kan du sälja presentkort, som senare kan användas till att betala för riktiga produkter.

När du hanterar presentkort är det viktigt att ange ett värde i fältet **Konto för sålda presentkort** i fönstret **Shopify-butikskort**. Det sålda presentkortet synkroniseras med ordrar på raden. Ett använt presentkort kommer också att importeras med ordern, men nu som en transaktion. Observera att presentkortet inte minskar beloppet att fakturera.

För att granska de utfärdare och använda presentkorten väljer du ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta vad du vill göra") och anger **Presentkort** och väljer sedan relaterad länk.

## Se även

[Kom igång med kopplingen för Shopify](get-started.md)  
