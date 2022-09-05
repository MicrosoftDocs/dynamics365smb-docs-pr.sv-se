---
title: Synkronisera och uppfylla försäljningsordrar
description: Konfigurera och kör import och behandling av försäljningsordrar från Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30124, 30125, 30128, 30129, 30130, 30131, 30132, 30133, 30134,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 3a8f6b2188c2a315bbed1ef99e23b6bbfafae40f
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361399"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Synkronisera och uppfylla försäljningsordrar

I den här artikeln beskrivs nödvändiga inställningar och steg som måste slutföras för att synkronisera och uppfylla försäljningsordrar från Shopify i [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Ange import av ordrar på Shopify-butikskortet

En vanlig Shopify-order kan inkludera kostnader förutom delsumman, till exempel fraktkostnader eller dricks. Dessa belopp bokförs direkt till det redovisningskonto som du vill använda för specifika transaktionstyper:

- **Konto för leveranskostnad**
- **Konto för sålda presentkort**: mer information finns på [Presentkort](synchronize-orders.md#gift-cards)
- **Drickskonto**  

Aktivera **Skapa ordrar automatiskt** för att automatiskt skapa försäljningsdokument i [!INCLUDE[prod_short](../includes/prod_short.md)] när Shopify-ordern har importerats.
Försäljningsdokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)] innehåller en länk till Shopify-ordern. Om du aktiverar **Shopify-ordernr på dokumentraden** upprepas den här informationen på försäljningsraden som *Kommentar*.

I fältet **Skatteområdeskälla** kan du definiera prioritet för hur skatteområdeskod eller rörelsebokföringsmallar för moms ska väljas baserat på adress. Det här steget är relevant för länder med moms. Läs mer vid [Skatteanmärkningar](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Mappning av utleveransmetoder

**Kod för utleveransmetod** för försäljningsdokument som importeras från Shopify kan fyllas i automatiskt. Du måste konfigurera **Mappning av utleveransmetoder**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill definiera mappning för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Mappning av utleveransmetoder**. Posterna för utleveransmetoder som definierats i inställningarna för [**Leverans**](https://www.shopify.com/admin/settings/payments) under **Shopify-admin** skapas automatiskt.
4. I fältet **Namn** ser du namnet på utleveransmetoden från Shopify.
5. Ange **Kod för utleveransmetod** med motsvarande utleveransmetod i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Om flera leveranskostnader är kopplade till en försäljningsorder väljs endast en som utleveransmetod och tilldelas försäljningsdokument.

### <a name="payment-method-mapping"></a>Mappning av betalningssätt

För att fylla i **Kod för betalningssätt** för försäljningsdokument som importerats från Shopify automatiskt måste du konfigurera **Mattning av betalningssätt**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill definiera mappning för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Mappning av betalningssätt**.
4. I fälten **Gateway** och **Kreditkortsföretag** anger du namnet på betalningssättet från Shopify. Posten skapas automatiskt när du importerar Shopify-ordrar.
5. Ange **Kod för betalningssätt** med motsvarande betalningssätt i [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Ange **Prioritet** för ärenden när kunden använder flera betalningsmedel. Betalningssättet med högst prioritet väljs i försäljningsdokumentet. Om båda betalningssätten har samma prioritet används det betalningssätt som har högst belopp.

> [!NOTE]  
> Om motsvarande betalningsmetod i [!INCLUDE[prod_short](../includes/prod_short.md)] har **Balanskontotyp** och **Balanskontotyp** fylls i, då kommer fakturasystemet under bokföringen att skapa en balanseringspost av typen *Betalning* och ansluta den till typen *Faktura* i kundreskontra transaktionen.

### <a name="location-mapping"></a>Mappning av platser

För att fylla i **Lagerställekod** för försäljningsdokument som importerats från Shopify automatiskt måste du konfigurera **Shopify butiksplatser**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill konfigurera kartläggningen av platser för att öppna **Shopify-butikskort**.
3. Välj åtgärden **Platser** för att öppna **Shopify-butiksplatser**.
4. Välj åtgärden **Hämta Shopify-platser** för att importera alla platser som har definierats i Shopify. Du hittar dem i inställningarna för [**Platser**](https://www.shopify.com/admin/settings/locations) under panelen **Shopify-admin**. Observera att platsen som är markerad som *standard* kommer att användas när du importerar ouppfyllda Shopify order.
5. Ange **Kod för standardlagerställe** med motsvarande plats i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Du måste konfigurera plats mappningen om växlingsknappen **Lagerställe ska finnas** aktiveras kort för **Lagerinställningar** annars kommer du inte att kunna skapa försäljningsdokument.

## <a name="run-the-order-synchronization"></a>Kör ordersynkronisering

Följande förfarande beskriver hur du importerar och uppdaterar försäljningsordrar.

> [!NOTE]  
> Det går inte att importera arkiverade ordrar i Shopify. Inaktivera **Arkivera order automatiskt** i avsnittet **Orderbehandling** av inställningarna för **kassan** under **Shopify-admin** för att säkerställa att alla ordrar importeras till [!INCLUDE[prod_short](../includes/prod_short.md)]. Om du behöver importera arkiverade ordrar använder du åtgärden **Avarkivera ordrar** på sidan [Ordrar](https://www.shopify.com/admin/orders) på panelen **Shopify admin**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill importera ordrar för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Ordrar**.
4. Välj åtgärden **Synkronisera ordrar från Shopify**.
5. Definiera filter för ordrar vid behov. Du kan till exempel importera helt betalda ordrar eller de som har låg risknivå.
6. Välj **OK**.

Du kan också söka efter batchjobbet **Synkronisera ordrar från Shopify**.

Du kan schemalägga uppgifter så att de utförs på ett automatiserat sätt. Läs mer i [Schemalägg återkommande uppgifter](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Granska importerade order

När importen är klar kan du utforska Shopify beställa och hitta all relaterad information, såsom betalningstransaktioner, fraktkostnader, risknivå eller uppfyllelser, om beställningen redan utfördes i Shopify. Du kan också se orderbekräftelser som har skickats till kunden genom att välja åtgärden **Shopify-statussida**.

> [!NOTE]  
> Du kan navigera till fönstret **Shopify-ordrar** direkt, så visas ordrar med statusen *Öppen* från alla butiker. För att granska slutförda ordrar måste du öppna sidan **Shopify-ordrar** från fönstret **Shopify-butikskort**.

## <a name="create-sales-documents-in-business-central"></a>Skapa försäljningsdokument i Business Central

Om reglaget **Skapa ordrar automatiskt** har aktiverats på **Shopify-butikskortet** försöker [!INCLUDE[prod_short](../includes/prod_short.md)] att skapa ett försäljningsdokument när ordern har importerats. Om problem som en saknad kund eller produkt uppstår måste du åtgärda problemen och sedan skapa försäljningsordern igen.

### <a name="to-create-sales-documents"></a>Skapa försäljningsdokument

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill synkronisera ordrar för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Ordrar**.
4. Välj den order som du vill skapa ett försäljningsdokument för och välj åtgärden **Skapa försäljningsdokument**.
5. Välj **Ja**.

Om Shopify-ordern måste uppfyllas skapas **försäljningsordern**. För uppfyllda Shopify order, t.ex. order som endast innehåller ett presentkort eller som redan hanteras i Shopify, skapas **försäljningsfakturan**.

Ett försäljningsdokument skapas nu och kan hanteras med hjälp av standardfunktionerna i [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="manage-missing-customers"></a>Hantera saknade kunder

Om inställningarna gör att en kund inte kan skapas automatiskt och en befintlig kund inte kan hittas tilldelar du en kund till Shopify-ordern manuellt. Detta kan göras på några få sätt:

- Du kan tilldela **Försäljningskundnr** direkt på sidan **Shopify-ordern** genom att välja en kund i listan över befintliga kunder.
- Du kan välja en kundmallskod, skapa och tilldela kunden via åtgärden **Skapa ny kund** i **Shopify-ordern**.
- Du kan mappa befintliga kunder till relaterade **Shopify-kunder** i fönstret **Shopify-kunder** och sedan välja åtgärden **Hitta mappning** i **Shopify-ordern**.

### <a name="tax-remarks"></a>Skatteanmärkningar

Den importerade Shopify ordern innehåller information om skatt, men momsen kommer att räknas om när du skapar försäljnings dokumentet så det är viktigt att moms-och moms inställningarna är korrekta i [!INCLUDE[prod_short](../includes/prod_short.md)].

- Flera moms- och skattesatser. Vissa produktkategorier omfattas till exempel av reducerade skattesatser. Artiklarna måste finnas i [!INCLUDE[prod_short](../includes/prod_short.md)] och mappas till Shopify-produkter. I annat fall används momsproduktbokföringsmallen med automatiskt skapande av saknade artiklar.

- Adressberoende skattesatser. Använd fältet **Skatteområdesprioritet** tillsammans med tabellen **Kundmallar** för att skriva över standardlogik som fylls i **Skatteområdeskod** i försäljningsdokumentet. I fältet **Skatteområdesprioritet** anges prioritet som används för att bestämma information om land/region och län/provins. Sedan hittas motsvarande post i Shopify-kundmallarna och **Skatteområdeskod**, **Skattepliktig** och **Moms rörelsebokföringsmall** används när ett försäljningsdokument skapas.

- Priser inklusive moms. Fältet **Priser inklusive skatt**/**Priser inklusive moms** i det skapade försäljningsdokumentet beror inte på kunden, utan på **Kundmall** från sidan **Shopify butikskort** eller kundmall per land.

### <a name="impact-of-order-editing"></a>Effekten av orderredigering

I Shopify:

|Redigera|Påverkan|
|------|-----------|
|Ändra uppfyllelseplatsen | Den ursprungliga platsen kommer att synkroniseras med [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Redigera en order och ändra antal| Order huvud och tilläggs tabeller uppdateras på [!INCLUDE[prod_short](../includes/prod_short.md)] rader. |
|Redigera en order och lägg till nytt objekt | Orderrubriken uppdateras, raderna kommer inte att uppdateras. |

I [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Redigera|Påverkan|
|------|-----------|
|Ändra platsen till en annan plats, mappad till Shopify platserna. Bokför leverans. | När uppfyllelse har synkroniserats uppdateras platsen i Shopify. |
|Ändra platsen till en annan plats, mappad inte till Shopify platserna. Bokför leverans. | Uppfyllelse kommer inte att synkroniseras med Shopify. |
|Ändra minsknings antal. Bokför leverans. | Ordern i Shopify markeras som delvis uppfylld. |
|Lägg till ett nytt objekt. Bokför leverans. | Ordern i Shopify markeras som uppfylld. Raderna uppdateras inte. |

## <a name="synchronize-shipments-to-shopify"></a>Synkronisera försändelser till Shopify

När en försäljningsorder som skapas från en Shopify-order skickas kan du synkronisera försändelserna till Shopify.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Synkronisera försändelser till Shopify** och välj relaterad länk.
2. Definiera filter för försändelser vid behov. Du kan till exempel uppdatera försändelsen som bokförts ett visst datum.
3. Välj **OK**.

Ordern i Shopify markeras som uppfylld. Kunden meddelas automatiskt om försändelsen via e-post eller SMS. Om en speditör och en spårningskod anges på försändelsen inkluderas spårningsinformationen i e-postmeddelandet.

> [!NOTE]  
> Glöm inte att köra **Synkronisera ordrar från Shopify** för att uppdatera uppfyllandestatusen för ordern i [!INCLUDE[prod_short](../includes/prod_short.md)]. Kopplingsfunktionen arkiverar också helt betalda och uppfyllda ordrar i både Shopify och [!INCLUDE[prod_short](../includes/prod_short.md)] under förutsättning att villkoren uppfylls.

### <a name="shipping-agents-and-tracking-url"></a>Speditörer och spårnings-URL

Om dokumentet **Bokförd utleverans** innehåller **Speditörskod** och/eller **Paketspårningsnr** skickas den här informationen till Shopify och slutkunder i ett e-postmeddelande med bekräftelse på försändelsen.

Spårningsföretaget fylls i följande ordning (från högsta till lägsta) baserat på fraktagentens post:

- **Shopify-spårningsföretag**
- **Namn**
- **Kod**

Om fältet **Spårnings-URL för paket** har fyllts i för posten Speditör innehåller också försändelsebekräftelsen en spårnings-URL.

## <a name="gift-cards"></a>Presentkort

I Shopify-butiken kan du sälja presentkort, som senare kan användas till att betala för riktiga produkter.

När du hanterar presentkort är det viktigt att ange ett värde i fältet **Konto för sålda presentkort** i fönstret **Shopify-butikskort**. Det sålda presentkortet synkroniseras med ordrar på raden. Ett använt presentkort kommer också att importeras med ordern, men nu som en transaktion. Observera att presentkortet inte minskar beloppet att fakturera.

För att granska de utfärdare och använda presentkorten väljer du ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta vad du vill göra") och anger **Presentkort** och väljer sedan relaterad länk.

## <a name="transactions-and-payouts"></a>Transaktioner och utbetalningar

När en kund färdigställer sin kassa i onlinebutiken sparas informationen om betalningar som en **transaktion**. Det kan finnas flera transaktioner kopplade till ordern, till exempel när en kund använder ett presentkort för att betala en del av kostnaden och sedan använder ett kredit kort eller PayPal för det återstående beloppet. 

Om du använder Shopify betalning som betalningsprovider kan du utöver information om de pengar som erhållits från kunden av betalnings förmedlaren även Visa utbetalningar från Shopify till ditt bankkonto. 

### <a name="transactions"></a>Transaktioner

De betalningstransaktioner som ägde rum på Shopify synkroniseras med ordrarna och kan visas från *Shopify-ordern*.

För att granska alla transaktioner väljer du ikonen med ![glödlampan som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") och anger **Transaktioner** och väljer sedan relaterad länk.

Om du har konfigurerat en mappning för betalningsmetod kommer det skapade försäljningsdokumentet att ha en tilldelad betalningsmetod kod. Mer information finns i [mappning betalningsmetod](#payment-method-mapping).

### <a name="payouts"></a>Utbetalningar

Om din butik har Shopify Payments aktiverat får du betalningar genom *Shopify Payouts* när en kund betalar med Shopify Payments och snabbkassa.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill synkronisera utbetalningar för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Synkronisera utbetalningar**.

För att granska alla utbetalningar väljer du ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta vad du vill göra") och anger **Utbetalningar** och väljer sedan relaterad länk.

**Utbetalningar** är endast avsedda som information och påverkar inte redovisningen eller bank redovisningen, men de kan vara användbara när du behandlar ditt bankkonto utdrag.

## <a name="see-also"></a>Se även

[Kom igång med kopplingen för Shopify](get-started.md)  
