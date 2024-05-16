---
title: Synkronisera och uppfylla försäljningsordrar
description: Konfigurera och kör import och behandling av försäljningsordrar från Shopify.
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129, 30150, 30151, 30145, 30147'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
---

# <a name="synchronize-and-fulfill-sales-orders"></a>Synkronisera och uppfylla försäljningsordrar

I den här artikeln beskrivs nödvändiga inställningar och steg som måste slutföras för att synkronisera och uppfylla försäljningsordrar från Shopify i [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Ange import av ordrar på Shopify-butikskortet

Ange en **valutakod** om din onlinebutik använder en annan valuta än den lokala valutan (BVA). Den angivna valutan måste ha växlingskurser konfigurerade. Lämna fältet tomt om din onlinebeställning använder samma valuta som [!INCLUDE[prod_short](../includes/prod_short.md)]. 

Du kan få åtkomst till butiksvalutan i inställningarna för [butiksinformation](https://www.shopify.com/admin/settings/general) i din Shopify Admin. Shopify kan konfigureras så att olika valutor accepteras, men importerade order kan användas i olika butiksvalutor. Importerade order till [!INCLUDE[prod_short](../includes/prod_short.md)] använder dock butiksvaluta.

En vanlig Shopify-order kan inkludera kostnader förutom delsumman, till exempel fraktkostnader eller dricks. Dessa belopp bokförs direkt till det redovisningskonto som du vill använda för specifika transaktionstyper:

* **Konto för leveransavgifter**
* **Konto för sålda presentkort**: mer information finns på [Presentkort](synchronize-orders.md#gift-cards)
* **Drickskonto**  

Aktivera **Skapa ordrar automatiskt** för att automatiskt skapa försäljningsdokument i [!INCLUDE[prod_short](../includes/prod_short.md)] när Shopify-ordern har importerats.

Om du vill släppa ett försäljningsdokument automatiskt aktiverar du alternativet **Frisläpp försäljningsorder automatiskt**.

Om du inte vill skicka automatiska leveransbekräftelser till kunder stänger du av växlingsknappen **Skicka leveransbekräftelse**. Det kan vara användbart att stänga av växlingsknappen om du säljer digitala varor eller vill använda en annan meddelandemekanism.

Om du väljer fältet **Shopify ordernr på dokumentraden**, [!INCLUDE [prod_short](../includes/prod_short.md)] sätter in försäljningsraden **Kommentar** med Shopify ordernummer.

> [!NOTE]
> Försäljningsdokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)] länkar till  Shopify-ordern och du kan lägga till fältet **Shopify ordernr.** Fält till listan eller kortsidorna för försäljningsorder, fakturor och leveranser. Om du vill veta mer om hur du lägger till ett fält går du till [Börja anpassa med hjälp av anpassningsläget](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode). 

I fältet **Skatteområdesprioritet** prioritera hur man väljer ett momsriktnummer för adresser på beställningar. Den Shopify order du importerade innehåller information om moms. Moms beräknas om när du skapar försäljnings dokumentet, så det är viktigt att moms- eller skatteinställningar är korrekta i [!INCLUDE[prod_short](../includes/prod_short.md)]. Mer information om moms finns i [ställa in moms för Shopify anslutningen](setup-taxes.md).

Ange hur du bearbetar returer och återbetalningar:

* **Tom** anger att du inte importerar och behandlar returer och återbetalningar.
* **Endast import** anger att du importerar information, men du kommer att manuellt skapa motsvarande kreditnotor.
* **Skapa kreditnota automatiskt** anger att du importerar information och [!INCLUDE[prod_short](../includes/prod_short.md)] skapar kredit notorna automatiskt. Det här alternativet innebär att du måste aktivera funktionen för växlingsknappen **Skapa automatiskt försäljningsorder**.

Ange en plats för returer och redovisningskonton för återbetalningar för varor och andra återbetalningar.

* **Refund Account non-restock Items** anger ett redovisningskontonummer för artiklar där du inte vill ha en lagerrättelse.
* **Återbetalningskonto** anger ett redovisningskontonummer för differensen mellan det totala återbetalade beloppet och det totala beloppet för artiklarna.

Lär dig mer om [Returer och återbetalningar](synchronize-orders.md#returns-and-refunds)

### <a name="shipment-method-mapping"></a>Mappning av utleveransmetoder

**Kod för utleveransmetod** för försäljningsdokument som importeras från Shopify kan fyllas i automatiskt. Du måste konfigurera **Mappning av utleveransmetoder**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill definiera mappning för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Mappning av utleveransmetoder**. Posterna för utleveransmetoder som definierats i inställningarna för [**Leverans**](https://www.shopify.com/admin/settings/payments) under **Shopify-admin** skapas automatiskt.
4. I fältet **Namn** ser du namnet på utleveransmetoden från Shopify.
5. Ange **Kod för utleveransmetod** med motsvarande utleveransmetod i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Om flera leveranskostnader är kopplade till en försäljningsorder väljs endast en som utleveransmetod och tilldelas försäljningsdokument.

### <a name="location-mapping"></a>Mappning av platser

Lagerställesmappningen krävs för att fylla i **lagerställeskoden** för försäljningsdokumentrader som importeras från Shopify. Detta är viktigt om växlingsknappen **Lagerställe ska finnas** aktiveras kort för **Lagerinställningar** annars kommer du inte att kunna skapa försäljningsdokument.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill konfigurera kartläggningen av platser för att öppna **Shopify-butikskort**.
3. Välj åtgärden **Platser** för att öppna **Shopify-butiksplatser**.
4. Välj åtgärden **Hämta Shopify-platser** för att importera alla platser som har definierats i Shopify. Du hittar dem i inställningarna för [**Platser**](https://www.shopify.com/admin/settings/locations) under panelen **Shopify-admin**. 
5. Ange **Kod för standardlagerställe** med motsvarande plats i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Platsmappning används också för att synkronisera lager. Om du vill ha mer information går du till [Synkronisera lager till Shopify](synchronize-items.md#sync-inventory-to-shopify).
  
## <a name="run-the-order-synchronization"></a>Kör ordersynkronisering

Följande förfarande beskriver hur du importerar och uppdaterar försäljningsordrar.

> [!NOTE]  
> Det går inte att importera arkiverade ordrar i Shopify. Om du behöver kontrollera orderstatusen öppnar du ordern från sidan [order](https://www.shopify.com/admin/orders) i panelen **Shopify admin** och granskar orderdetaljer.
> 
> Inaktivera **Arkivera order automatiskt** i avsnittet **Orderbehandling** av inställningarna för **kassan** under **Shopify-admin** för att säkerställa att alla ordrar importeras till [!INCLUDE[prod_short](../includes/prod_short.md)]. Om du behöver importera arkiverade ordrar använder du åtgärden **Avarkivera ordrar** på sidan [Ordrar](https://www.shopify.com/admin/orders) på panelen **Shopify admin**. 

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill importera ordrar för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Ordrar**.
4. Välj åtgärden **Synkronisera ordrar från Shopify**.
5. Definiera filter för ordrar vid behov. Du kan till exempel importera helt betalda ordrar eller de som har låg risknivå.

   > [!NOTE]  
   > När du filtrerar efter tagg bör du använda filtertoken `@` och `*`. Om du t.ex. vill importera order som innehåller *tag1* använder du `@*tag1*`. `@` kommer att säkerställa att resultatet är skiftlägesokänsligt, medan `*` hitta beställningar med flera taggar.

6. Välj **OK**.

Du kan också söka efter batchjobbet **Synkronisera ordrar från Shopify**.

Du kan schemalägga uppgifter så att de utförs på ett automatiserat sätt. Läs mer i [Schemalägg återkommande uppgifter](background.md#to-schedule-recurring-tasks).

### <a name="under-the-hood"></a>Under huven

Shopify anslutningsprogram importerar order i två steg:

1. Order rubriker importeras till tabellen **Shopify order som ska importeras** när de matchar vissa villkor:

   * De arkiveras. Det innebär att du kan inkludera eller utesluta order från synkronisering genom att arkivera eller ta bort arkiveringen i Shopify-administratören.
   * De skapades eller ändrades efter den senaste synkroniseringen. Det innebär att du kan tvinga fram återimport av en viss order om du ändrar den, till exempel genom att lägga till **Anteckningar** eller **Tagg**.

2. Den importerar Shopify order och kompletterande information.

   * Shopify anslutningsprogram behandlar alla poster i tabellen **Shopify ordern som ska importeras** som matchar de filter kriterier som du har angett på sidan för förfrågan **Synkronisera order från Shopify**. Exempelvis taggar, kanal eller status för uppfyllelse. Om du inte har angett några filter behandlas alla poster.
   * Vid import av Shopify-order, begär Shopify-anslutningsprogrammet ytterligare information från Shopify:

     * Orderhuvuden
     * Orderrader
     * Information om leverans och uppfyllelse
     * Transaktioner
     * Returer och återbetalningar, om detta konfigureras

Sidan **Shopify-order att importera** är användbar när du felsöker problem med orderimport. Du kan bedöma vilka order som är tillgängliga och vidta följande steg:

* Kontrollera om ett fel har blockerat importen av en specifik order och utforska informationen om felet. Kontrollera fältet **Har fel**.
* Endast processer för specifika order. Du måste fylla i **Butikskod**, välj en eller fler order och sedan åtgärden **Importera valda order** .
* Ta bort order från sidan **Shopify-order att importera** för att undanta dem från synkroniseringen.

## <a name="review-imported-orders"></a>Granska importerade order

När importen är klar kan du utforska Shopify beställa och hitta all relaterad information, såsom betalningstransaktioner, fraktkostnader, risknivå, orderattribut och taggar eller uppfyllelser, om beställningen redan utfördes i Shopify. Du kan också se orderbekräftelser som har skickats till kunden genom att välja åtgärden **Shopify-statussida**.

> [!NOTE]  
> Du kan navigera till fönstret **Shopify-ordrar** direkt, så visas ordrar med statusen *Öppen* från alla butiker. För att granska slutförda ordrar måste du öppna sidan **Shopify-ordrar** från sidan **Shopify-butikskort**.

Innan försäljningsdokument skapas i [!INCLUDE[prod_short](../includes/prod_short.md)] kan du använda åtgärden **Synkronisera order från Shopify**-åtgärd på sidan **Shopify Order** för att importera specifika order igen.

Du kan också markera en order som betald, vilket är användbart i ett B2B-scenario där betalningar behandlas utanför Shopify kassan. Välj åtgärden **Markera som betald** på sidan **Shopify Order**. Du kan också markera en order som makulerad för att starta återbetalningsflödet Shopify. Välj åtgärden **Avbryt order** på sidan **Shopify Order**, fyll i fälten efter behov på sidan **Shopify avbryt order** och tryck på **OK**. Du måste köra ordersynkronisering för att importera uppdateringarna till [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="create-sales-documents-in-business-central"></a>Skapa försäljningsdokument i Business Central

Om reglaget **Skapa ordrar automatiskt** har aktiverats på **Shopify-butikskortet** försöker [!INCLUDE[prod_short](../includes/prod_short.md)] att skapa ett försäljningsdokument när ordern har importerats. Om problem som en saknad kund eller produkt uppstår måste du åtgärda problemen och sedan skapa försäljningsordern igen.

### <a name="to-create-sales-documents"></a>Skapa försäljningsdokument

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill synkronisera ordrar för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Ordrar**.
4. Välj den order som du vill skapa ett försäljningsdokument för och välj åtgärden **Skapa försäljningsdokument**.
5. Välj **Ja**.

Om Shopify-ordern måste uppfyllas skapas **försäljningsordern**. För uppfyllda Shopify order, t.ex. order som endast innehåller ett presentkort eller som redan hanteras i Shopify, skapas **försäljningsfakturan**.

Ett försäljningsdokument skapas och kan hanteras med hjälp av standardfunktionerna i [!INCLUDE[prod_short](../includes/prod_short.md)].

Om du vill återskapa försäljningsdokument kan du använda åtgärden **Ta bort länk för bearbetade dokument** på sidan **Shopify Order**. Observera att den här åtgärden inte tar bort det redan skapade försäljningsdokumentet. Du måste bearbeta det manuellt.

### <a name="manage-missing-customers"></a>Hantera saknade kunder

Om inställningarna gör att en kund inte kan skapas automatiskt och en motsvarande kund inte kan hittas tilldelar du en kund till Shopify-ordern manuellt. Det finns några sätt att tilldela kunder order:

* Tilldela **Förs.kundnr.** och **Faktureringskundnr.** direkt på sidan **Shopify-ordern** genom att välja en kund i listan över befintliga kunder.
* Välj en kundmall, skapa och tilldela kunden via åtgärden **Skapa ny kund** i **Shopify-ordern**. Shopify-kunden måste ha minst en adress. Order som skapats via Shopify POS försäljningskanal saknar ofta adressinformation.
* Mappa befintliga kunder till relaterade **Shopify-kunder** på sidan **Shopify-kunder** och sedan välja åtgärden **Hitta mappning** i **Shopify-ordern**.

### <a name="how-the-connector-chooses-which-customer-to-use"></a>Så väljer kopplingen vilken kund som ska användas

Funktionen *Importera order från Shopify* försöker att välja kunder i följande ordning:

1. Om **Standardkundnr** definieras i **Shopify kundmall** för **Kod för leveransland/-region**, sedan **Standardkundnr.** oavsett inställningar i **Kundimport från Shopify** och **Kundmappningstyp**. Läs mer i [Kundmall per land](synchronize-customers.md#customer-template-per-countryregion).
2. Om **Kundimport från Shopify** anges till *Ingen* och **Standardkundnr.** definieras på sidan **Shopify butikskort**, sedan **Standardkundnr.** .

Nästa steg beror på **Kundmappningstyp**.

* Om det är **Ta alltid standardkunden** använder kopplingen sedan kunden som definierats i fältet **Standardkundnr** på sidan **Shopify-butikskort**.
* Om det är **Via e-post/telefon** försöker kopplingen hitta befintliga kunder genom ID först, sedan via e-post och sedan via telefonnummer. Om kunden inte hittas skapar kopplingen en ny kund.
* Om det är **Genom faktureringsinfo** försöker kopplingen att hitta befintliga kunder genom ID först och sedan genom information om faktureringsadressen. Om kunden inte hittas skapar kopplingen en ny kund.

> [!NOTE]  
> Kopplingen använder information från faktureringsadressen och skapar en faktureringskund i [!INCLUDE[prod_short](../includes/prod_short.md)]. Försäljningskunden är densamma som faktureringskunden.

För B2B-order är flödet detsamma, även om kontaktanvändning använder fälten **Standardföretagsnummer**, **Företagsimport från Shopify**, **Företagsmappningstyp** på sidan **Shopify butikskort**. Observera att det inte finns något **standardföretagsnr.** i **Shopify kundmallen** som för B2B förväntas den ha namngivna kunder.

### <a name="different-processing-rules-for-orders"></a>Olika bearbetningsregler för order

Du kanske vill hantera order på olika sätt utifrån en regel. Order från en specifik försäljningskanal, som kassa, bör därför använda standardkunden, men du vill att din onlinebutik ska ha verklig information om kunden.

Ett sätt att ta itu med detta är att skapa ett extra Shopify-butikskort och använda filter på sidan **Synkronisera order från Shopify** begäran.

Exempel: du har både onlinebutik och Shopify kassa. För din kassa vill du använda en fast kund, men för onlinebutiken vill du skapa kunder i [!INCLUDE[prod_short](../includes/prod_short.md)]. I proceduren nedan beskrivs de steg på hög nivå som visas. Mer information finns i motsvarande hjälpartiklar.

1. Skapa en Shopify butik kallad *BUTIK* och koppla den till ditt Shopify-konto.
1. Konfigurera synkronisering av artikel/produkt så att den här butiken hanterar produktinformation.
1. Ange att kunderna importeras med order. Kontakten ska hitta kunder genom att söka efter sin e-postadress. Om det inte finns någon adress används kundmallen för att skapa en ny kund.
1. Skapa en Shopify butik kallad *KASSA* och koppla den till samma Shopify-konto.
1. Kontrollera att synkronisering av artikel/produkt har inaktiverats.
1. Välj det anslutningsprogram som använder standardkunden.
1. Skapa en återkommande jobbkötransaktion för rapport 30104 **Synkronisera order från Shopify**. Välj **BUTIK** i fältet **Shopify butikskod** och använd filter för att hämta alla order utom de som skapas av kassans försäljningskanal. Till exempel **<>Buktikskassa**
1. Skapa en återkommande jobbkötransaktion för rapport 30104 **Synkronisera order från Shopify**. Välj **KASSA** i fältet **Shopify butikskod** och använd filter för att hämta order som genererats av kassans försäljningskanal. Till exempel, **butikskassa**.

Varje jobbkö kommer att importera och bearbeta order inom de definierade filtren och använda reglerna från motsvarande Shopify butikskort. De skapar till exempel försäljningsorder för standardkunden.

> [!Important]
> För att undvika konflikter när du behandlar order måste du använda samma jobbkö för båda jobbkötransaktionerna.

### <a name="impact-of-order-editing"></a>Effekten av orderredigering

I Shopify:

|Redigera|Inverkan på Shopify-order som ännu inte behandlats i [!INCLUDE[prod_short](../includes/prod_short.md)] | Inverkan på Shopify-order som redan har behandlats i [!INCLUDE[prod_short](../includes/prod_short.md)] |
|------|-----------|-----------|
|Ändra uppfyllelseplatsen | En uppfyllelseplats är synkroniserad med [!INCLUDE[prod_short](../includes/prod_short.md)]. | En uppfyllelseplats är synkroniserad med [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Redigera en order och öka antal|Importerad order kommer att använda ny kvantitet.| Anslutningsprogrammet identifierar ändrings- och markeringsorder. |
|Redigera en order och minska antal|Importerad order kommer att använda ny kvantitet. Shopify återbetalning med 0 belopp importeras som inte kan konverteras till en kreditnota.| Anslutningsprogrammet identifierar ändrings- och markeringsorder. |
|Redigera en order och ta bort befintlig artikel |Borttaget objekt importeras inte. Shopify återbetalning med 0 belopp importeras som inte kan konverteras till en kreditnota.| Anslutningsprogrammet identifierar ändrings- och markeringsorder. |
|Redigera en order och lägg till nytt objekt | Ursprungliga och tillagda objekt kommer att importeras. | Anslutningsprogrammet identifierar ändrings- och markeringsorder. |
|Bearbetningsorder: uppfyllelse, uppdatera betalningsinformation | Orderrubriken kommer att uppdateras. |Orderrubriken kommer att uppdateras. Uppfyllelse kommer inte att synkroniseras med Shopify.|
|Annullera betald order | Orderhuvudet kommer att uppdateras, för att behandlas separat |Anslutningsprogrammet identifierar ändrings- och markeringsorder. |
|Annullera obetald order | Borttaget objekt importeras inte. Shopify återbetalning med 0 belopp importeras som inte kan konverteras till kreditnota. |Anslutningsprogrammet identifierar ändrings- och markeringsorder. |

Om beställningen redan har behandlats i [!INCLUDE[prod_short](../includes/prod_short.md)] anslutningsprogram visar följande felmeddelande: *Ordern har redan bearbetats i Business Central, men en utgåva har mottagits från Shopify. Ändringar har inte spridits till den bearbetade ordern i Business Central. Uppdatera de bearbetade dokumenten så att de matchar mottagna data från Shopify. Om du vill tvinga fram synkroniseringen använder du åtgärden "Synkronisera order från Shopify" på Shopify Order kortsidan.*

Beroende på status på det skapade försäljningsdokumentet kan du utföra följande åtgärder:

1. Ta bort skapade försäljningsdokument
2. Välj åtgärden **Ta bort länk för bearbetade dokument** för att återställa indikatorn **Bearbetat**.
3. Välj åtgärden **Synkronisera order från Shopify** om du vill uppdatera enskilda order med senaste data från Shopify.

I [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Redigera|Effekt|
|------|-----------|
|Ändra platsen till en annan plats. Bokför leverans. | Ordern kommer att markera som uppfylld. Uppfyllelseplats från Shopify kommer att användas. |
|Minska antal. Bokför leverans. | Ordern i Shopify markeras som delvis uppfylld. |
|Öka antal. Bokför leverans. | Uppfyllelse kommer inte att synkroniseras med Shopify. Det är samma sak om uppfyllelsen delades upp i Shopify men bearbetades som en rad in [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Lägg till ett nytt objekt. Bokför leverans. | Ordern i Shopify markeras som uppfylld. Nya rader kommer inte att läggas till. |

## <a name="synchronize-shipments-to-shopify"></a>Synkronisera försändelser till Shopify

När en försäljningsorder som skapas från en Shopify-order skickas kan du synkronisera försändelserna till Shopify.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Synkronisera försändelser till Shopify** och välj relaterad länk.
2. Definiera filter för försändelser vid behov. Du kan till exempel uppdatera försändelsen som bokförts ett visst datum.
3. Välj **OK**.

Ordern i Shopify markeras som uppfylld. Kunden meddelas automatiskt om försändelsen via e-post eller SMS. Om en speditör och en spårningskod anges på försändelsen inkluderas spårningsinformationen i e-postmeddelandet.

Du kan också använda åtgärden **Synkronisera utleveranser** på sidorna Shopify försäljningsorders eller Shopify butik.

Du kan schemalägga uppgifter så att de utförs på ett automatiserat sätt. Läs mer i [Schemalägg återkommande uppgifter](background.md#to-schedule-recurring-tasks).

> [!Important]
> Platsen, inklusive tom plats, som definieras i raden Bokad leverans måste ha en matchande post i Shopify plats. Annars kommer den här raden inte att skickas tillbaka till Shopify. Lära dig mer på [platsmappning](synchronize-orders.md#location-mapping).

Glöm inte att köra **Synkronisera ordrar från Shopify** för att uppdatera uppfyllandestatusen för ordern i [!INCLUDE[prod_short](../includes/prod_short.md)]. Kopplingsfunktionen arkiverar också helt betalda och uppfyllda ordrar i både Shopify och [!INCLUDE[prod_short](../includes/prod_short.md)] under förutsättning att villkoren uppfylls. 

### <a name="shipping-agents-and-tracking-url"></a>Speditörer och spårnings-URL

Om dokumentet **Bokförd utleverans** innehåller **Speditörskod** och/eller **Paketspårningsnr** skickas den här informationen till Shopify och slutkunder i ett e-postmeddelande med bekräftelse på försändelsen.

Spårningsföretaget fylls i följande ordning (från högsta till lägsta) baserat på fraktagentens post:

1. **Shopify-spårningsföretag**
1. **Namn**
1. **Kod**

Om fältet **Spårnings-URL för paket** har fyllts i för posten Speditör innehåller också försändelsebekräftelsen en spårnings-URL.

## <a name="returns-and-refunds"></a>Returer och återbetalningar

I en integration mellan  Shopify och [!INCLUDE[prod_short](../includes/prod_short.md)] är det viktigt att kunna synkronisera så mycket affärsdata som möjligt. Det gör det enklare att hålla ekonomi- och lagernivåerna aktuella i [!INCLUDE[prod_short](../includes/prod_short.md)]. De data som du kan synkronisera innehåller returer och återbetalningar som registrerats i Shopify administration eller Shopify kassa.

Returer och återbetalningar importeras med tillhörande order om du har aktiverat bearbetningstypen på det Shopify butikskortet.

Returer importeras endast i informationssyfte. Det finns ingen bearbetningslogik associerad med dem.

Ekonomi och, om det behövs, lagertransaktioner bearbetas via återbetalningar. Återbetalningar kan inkludera produkter eller bara belopp, t.ex. om en handlare har beslutat att kompensera fraktavgifter eller något annat belopp.

Du kan skapa försäljningskreditnotor för återbetalningar. Kreditnotorna kan ha följande typer av rader:

|Kontakttyp|Nr.|Kommentar|
|-|-|-|
|Redovisningskonto|Konto för sålda presentkort| Använd för återbetalningar relaterade till presentkort.|
|Redovisningskonto|Återbetalningskonto för artiklar som inte återanskaffas | Används för återbetalningar som avser produkter som inte har återanskaffats. |
|Artikel |Art.nr| Används för återbetalningar som avser produkter som har återanskaffats. Gäller för direkta återbetalningar eller återbetalningar som är kopplade till återbetalningar. Lagerställekoden på kreditnotsraden anges utifrån det värde som valts för returplatsen.|
|Redovisningskonto| Återbetalningskonto | Använd för andra återbetalade belopp som inte är relaterade till produkter eller presentkort. Exempelvis tips eller om du manuellt angav ett belopp att återbetala i Shopify. |

> [!Note]
> Returplatserna, inklusive tomma platser, som definieras i **Shopify butikskortet** , används på den skapade kreditnotan. De ursprungliga platserna ignoreras från order eller leveranser.

## <a name="gift-cards"></a>Presentkort

I Shopify-butiken kan du sälja presentkort, som senare kan användas till att betala för riktiga produkter.

När du hanterar presentkort är det viktigt att ange ett värde i fältet **Konto för sålda presentkort** i fönstret **Shopify-butikskort**. Det sålda presentkortet synkroniseras med ordrar på raden. Ett använt presentkort kommer också att importeras med ordern, men nu som en transaktion. Observera att presentkortet inte minskar beloppet att fakturera.

För att granska de utfärdare och använda presentkorten väljer du ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta vad du vill göra") och anger **Presentkort** och väljer sedan relaterad länk.

## <a name="see-also"></a>Se även

[Komma i gång med Shopify-anslutningsprogrammet](get-started.md)  
