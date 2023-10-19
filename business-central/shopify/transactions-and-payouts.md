---
title: Synkronisera och transaktioner och utbetalningar
description: Konfigurera och kör import av transaktioner och utbetalningar från Shopify.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30124, 30125, 30130, 30131, 30132, 30133, 30134,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Transaktioner och utbetalningar

När en kund färdigställer sin kassa i onlinebutiken sparas informationen om betalningar som en **transaktion**. Det kan finnas flera transaktioner kopplade till ordern, till exempel när en kund använder ett presentkort för att betala en del av kostnaden och sedan använder ett kredit kort eller PayPal för det återstående beloppet.

Om du använder Shopify betalning som betalningsprovider kan du utöver information om de pengar som erhållits från kunden av betalnings förmedlaren även Visa utbetalningar från Shopify till ditt bankkonto.

## Transaktioner

De betalningstransaktioner som ägde rum på Shopify synkroniseras med ordrarna och kan visas från **Shopify-ordern**.

För att granska alla transaktioner väljer du ikonen med ![glödlampan som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och anger **Transaktioner** och väljer sedan relaterad länk.

Fältet **Bokfört fakturanr.** kan vara användbart i avstämningsprocessen.

Om du har konfigurerat en mappning för betalningsmetod kommer det skapade försäljningsdokumentet att ha en tilldelad betalningsmetod kod. Mer information finns i [mappning betalningsmetod](#payment-method-mapping).

## Utbetalningar

Om din butik har Shopify Payments aktiverat får du betalningar genom **Shopify utbetalningar** när en kund betalar med Shopify betalningar och snabbkassa.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill synkronisera utbetalningar för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Synkronisera utbetalningar**.

För att granska alla utbetalningar väljer du ikonen med ![glödlampan som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och anger **Utbetalningar** och väljer sedan relaterad länk.

**Utbetalningar** är endast avsedda som information och påverkar inte redovisningen eller bank redovisningen, men de kan vara användbara när du behandlar ditt bankkonto utdrag.

## Mappning av betalningssätt

För att fylla i **Kod för betalningssätt** för försäljningsdokument som importerats från Shopify automatiskt måste du konfigurera **Mattning av betalningssätt**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den butik som du vill definiera mappning för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Mappning av betalningssätt**.
4. I fälten **Gateway** och **Kreditkortsföretag** anger du namnet på betalningssättet från Shopify. Posten skapas automatiskt när du importerar Shopify-ordrar.
5. Ange **Kod för betalningssätt** med motsvarande betalningssätt i [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Ange **Prioritet** för ärenden när kunden använder flera betalningsmedel. Betalningssättet med högst prioritet väljs i försäljningsdokumentet. Om båda betalningssätten har samma prioritet används det betalningssätt som har högst belopp.

> [!NOTE]  
> Om motsvarande betalningsmetod i [!INCLUDE[prod_short](../includes/prod_short.md)] har **Balanskontotyp** och **Balanskontotyp** fylls i, då kommer fakturasystemet under bokföringen att skapa en balanseringspost av typen *Betalning* och ansluta den till typen *Faktura* i kundreskontra transaktionen.

## Användningsfall
  
Parter:

* Köpare – person som köper varor från Shopify onlinebutiken.
* Handlare – ditt företag.
* Betalningsförmedlare – företag som underlättar bearbetningen av betalningar. Kan vara Shopify Payments eller tredje part.

### Hur pengar flödar

Köparen köper varor i onlinebutiken. Det sista steget är att behandla betalning.

>[!NOTE]
> Det här exemplet täcker inte fall när betalningen slutförs utanför Shopify kassa, vilket gäller för B2B-scenarier.
  
Köparen betalar med kreditkort, PayPal eller någon lokal betalningsmetod som MobilePay i Danmark. Betalningsförmedlaren tar hela beloppet från köparen. Vid denna tidpunkt flyttas köparnas pengar till betalningsförmedlaren.

Beroende på vilken betalningsleverantör det handlar om, kan det hända att leverantören ser detta pengar på deras konto på betalningsförmedlaren, både mottagna och avdragna provisioner. Betalningsförmedlare tar ofta emot en provision från varje transaktion och i vissa fall kan de ha en fast avgift också.
  
Beroende på betalningsförmedlare utlöser butikerna antingen en överföring av pengarna till deras bankkonto (utbetalning) manuellt eller sker automatiskt inom en definierad period, en gång per dag, en gång per månad och så vidare.
  
Beroende på vilken bank det gäller kan handlaren se den inkommande transaktionen på sina bankkonton via onlinebank eller bankkontoutdrag.

Det finns flera alternativ för hur du kan hantera betalningstransaktioner i [!INCLUDE[prod_short](../includes/prod_short.md)]
  
### Alternativ 1: Stäm av inkommande överföringar till bankkonto mot ursprungliga fakturor
  
Handlare importerar försäljningsorder till [!INCLUDE[prod_short](../includes/prod_short.md)] och bokför utleverans och faktura.

Resultat: systemet skapar en **Kundreskontratransaktion** av typen *Faktura* med hela beloppet anges **Öppet** till Ja. Det **återstående beloppet** är lika med det fakturerade beloppet.

Handelsimporternas bankutdrag med hjälp av betalningsavstämningsjournal.

Problem:

1. Kan vara svårt om det finns flera fakturor (och kreditnotor), men en utbetalning från betalningsförmedlaren med ett klumpsumma.
2. Beloppet matchar vanligen inte på grund av provision. Du kan använda betalningstolerans eller/och kassarabatter för att hantera avgifter.

### Alternativ 2: stämma av inkommande överföringar till bankkontot mot ett interimistiskt konto som representerar pengar hos betalningsförmedlaren
  
Handlare importerar försäljningsorder till [!INCLUDE[prod_short](../includes/prod_short.md)] och bokför utleverans och faktura.
  
Resultat: systemet skapar en kundreskontrapost av typen **Faktura** med hela beloppet anges **Open** till Ja. Det **återstående beloppet** är lika med det fakturerade beloppet.

Men eftersom försäljningsordern har en betalningsmetodkod där fälten **Balanskontotyp** och **Motkontonr.** fylls i skapar systemet automatiskt ytterligare en kundreskontrapost av typen **Betalning** och tillämpar den på kundreskontraposten som skapats tidigare.

>[!NOTE]
> Fältet kod för betalningssätt fylls i baserat på mappning av betalningsmetod. Mer information finns i [mappning betalningsmetod](#payment-method-mapping).
  
Du kan definiera balanskonton för betalningsmetoder på två sätt:

* **Balanskontotyp** anges som *Bank* och **Motkonto** fyll i det särskilda bankkonto som representerar ditt konto hos betalningsförmedlaren.
* **Balanskontotyp** anges som *Redovisningskonto** och **Motkonto.** fyll i det redovisningskonto som representerar ditt konto hos betalningsförmedlaren.

Det är praktiskt att använda ett bankkonto om betalningsleverantören exporterar en typ av kontoutdrag, som du kan importera till betalningsavstämningsjournalen.

Handelsimporternas bankutdrag med hjälp av betalningsavstämningsjournal. Inkommande utbetalning kan bearbetas:

* som överföring från en annan bank. Om överföringen tar några dagar eller med valutakurser, kanske du vill använda ett redovisningskonto.
* Som en skillnad på det redovisningskonto som representerar ditt konto hos betalningsförmedlaren.
  
Återstående saldo på redovisnings- eller bankkontot som representerar ditt konto hos betalningsleverantören kan skrivas av som "avgifter/provision"

Problem:

1. Du kan skapa flera redovisnings- eller bankkonton om du arbetar med flera betalningsförmedlare. Försäljningsorder i [!INCLUDE[prod_short](../includes/prod_short.md)] som endast stöder en betalningsmetodkod, vilket gör det svårt att hantera ärenden när en köpare använder flera betalningsmetoder för en order.

## Se även

[Kom igång med kopplingen för Shopify](get-started.md)  
