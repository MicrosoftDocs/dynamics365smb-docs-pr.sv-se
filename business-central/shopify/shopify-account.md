---
title: Skapa och ställa in ett Shopify konto
description: Lär dig hur du får ett Shopify konto så att du kan visa arbetsflödet för integrering Shopify och Business Central.
ms.date: 03/04/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
---

# Skapa och ställa in ett Shopify konto



Om du funderar på att använda Shopify som näthandelslösning och behöver ett konto för att validera det Shopify integrerade arbetsflödet har du följande alternativ:

- Få en testversion. Detta är den vanligaste startpunkten för slutanvändare.  
- Skapa utvecklingsbutiker. Det här tillvägagångssättet är för partner som utför återkommande demonstrationer, utbildningar och support.

## Utvärderingsversion (slutanvändare)

Gå till [Shopify webbplatsen ](https://www.shopify.com) och använd ditt e-postkonto för administratörskontot för att registrera dig för en kostnads fri utvärderingsversion. Mer information om hur du skapar och anpassar onlinebutiken finns i [Shopify hjälpcenter](https://help.shopify.com/).

I **Shopify Admin** av skapad butik tillämpa följande **inställningar**:

- Välj en plan i [**plan**](https://www.shopify.com/admin/settings/plan)  inställningarna om du vill kunna testa kassaprocessen.

- Överväg att aktivera *Visa inloggningslänk i rubriken på webbutiken och i kassan* i avsnittet **Konton i webbutik och kassa** i inställning [**Kundkonton**](https://www.shopify.com/admin/settings/customer_accounts) i **Shopify administratör**.
- Överväg att välja *Nytt kundkonto* i avsnittet  **Konton i webbutik och kassa** i inställningarna för kundkonton.
- Överväg att aktivera *Självbetjäningsreturer* i avsnittet **Nya kundkonton** i inställningarna för kundkonton.

- Aktivera testbetalningar. Du har två alternativ. Börja med att gå till inställningar för [**betalningar**](https://www.shopify.com/admin/settings/payments):  
  1. *(för testning) Falsk gateway*. Mer information finns i [Aktivera falsk gateway för test](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* i testläge. Mer information finns i [Testa Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Inaktivera **Arkivera order automatiskt** i avsnittet **Orderbehandling** av inställningarna för [**kassan**](https://www.shopify.com/admin/settings/checkout) i **administrationsdelen för Shopify**.
- Överväg att välja alternativ *företagsnamn – valfritt* i avsnittet **kundinformation** i kassainställningarna.
- Aktivera alternativet **Visa alternativ för dricks i kassan** i avsnittet **dricks** i kassainställningarna om du planerar att visa dricks.

> [!Important]  
> Glöm inte att avbryta din Shopify utvärdering om du vill undvika betalningar.

## Utvecklingsbutik

Börja med att ansluta till [Shopify partnerprogrammet](https://help.shopify.com/partners/about). Därefter använder du **instrumentpanelen för partnern** för att skapa ett utvecklingslager. Läs mer i [Skapa utvecklingsbutiker](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

När du har skapat butiken i **Shopify Admin** av skapad butik tillämpa följande **inställningar**:

- Överväg att aktivera *Visa inloggningslänk i rubriken på webbutiken och i kassan* i avsnittet **Konton i webbutik och kassa** i inställning [**Kundkonton**](https://www.shopify.com/admin/settings/customer_accounts) i **Shopify administratör**.
- Överväg att välja *Nytt kundkonto* i avsnittet  **Konton i webbutik och kassa** i inställningarna för kundkonton.
- Överväg att aktivera *Självbetjäningsreturer* i avsnittet **Nya kundkonton** i inställningarna för kundkonton.
  
- Aktivera testbetalningar. Du har två alternativ. Börja med att gå till inställningar för [**betalningar**](https://www.shopify.com/admin/settings/payments):  
  1. *(för testning) Falsk gateway*. Mer information finns i [Aktivera falsk gateway för test](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* i testläge. Läs mer i [Testa Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).
     
- Inaktivera **Arkivera order automatiskt** i avsnittet **Orderbehandling** av inställningarna för [**kassan**](https://www.shopify.com/admin/settings/checkout) i **administrationsdelen för Shopify**.
- Överväg att välja alternativ *företagsnamn – valfritt* i avsnittet **kundinformation** i kassainställningarna.
- Aktivera alternativet **Visa alternativ för dricks i kassan** i avsnittet **dricks** i kassainställningarna om du planerar att visa dricks.


> [!Note]  
> Utvecklingsarkiv är oftast lösenordsskyddade. När du försöker öppna en specifik sida i onlinebutiken från [!INCLUDE [prod_short](../includes/prod_short.md)], t.ex. gå till en viss produkt eller order, måste du ange lösenordet. När du testar behöver du inte ange ditt lösenord, logga in på Shopify administratören och öppna butiken därifrån. Du behöver inte ange butikens lösenord förrän du stänger webbläsaren eller så upphör sessionen att gälla.  

## Se även

[Komma i gång med Shopify-anslutningsprogrammet](get-started.md)  
[Genomgång: ställa in och använda Shopify anslutningsprogram](walkthrough-setting-up-and-using-shopify.md)
