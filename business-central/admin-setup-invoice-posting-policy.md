---
title: Definiera en bokföringspolicy för faktura för användare
description: Använd regler för fakturabokföring för att kontrollera om en användare kan bokföra försäljnings- och inköpsfakturor.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.forms: '119, 9807,'
---

# Definiera en bokföringspolicy för faktura för användare

Företag har ofta unika processer för att bokföra försäljnings- och inköpsfakturor och leveranser. Processer kan till exempel variera från en person som bokför allt på en inköpsorder, till flera anställda. Du kan begränsa användare från bokföringsfakturor eller kräva att fakturor bokförs tillsammans med leveranser eller inleveranser.

## Så här anger du bokföringspolicy

På sidan **användarinställningar** i fälten **Bokföringspolicy för försäljningsfaktura** och **Bokföringsprincip för inköpsfaktura** välj ett av följande alternativ:

* **Tillåten** (standard) – Behåll det nuvarande beteendet, där en användare kan välja vilket inläggsalternativ som ska användas, som t.ex. **leverera**, **faktura** och **leverera och fakturera**. 
* **Förbjuden** – hindrar användaren från att bokföra fakturor. I Business Central visas en bekräftelse dialogruta som endast innehåller alternativ **leverans** och **mottagning**.
* **Obligatorisk** – gör att användaren kan bokföra fakturor tillsammans med inleveranser eller utleveranser. I Business Central visas en bekräftelse dialogruta med alternativ **leverans och fakturera** och **mottagning och fakturera**.

## Inverkan på dokument

I följande tabell beskrivs hur fakturana bokföringsprinciper påverkar dokument.

|Dokument | Alternativ 1: Tillåt <br>Visar en serie alternativ| Alternativ 2: otillåtet <br>Bekräftelsedialogruta | Alternativ 3: obligatorisk <br>Bekräftelsedialogruta|
|--|--|--|--|
|Försäljningsorder |- Leverera <br>- Fakturera <br>- Leverera och fakturera |Vill du bokföra utleveranserna? |Vill du bokföra utleveransen och fakturan?|
|Försäljningsreturorder |- Inleverera <br>- Fakturera <br>- Inleverera och fakturera |Vill du bokföra inleveransen? |Vill du bokföra inleveransen och fakturan?|
|Lagerplockning |- Leverera <br>- Leverera och fakturera |Vill du bokföra utleveranserna? |Vill du bokföra utleveransen och fakturan?|
|Inköpsorder |- Inleverera <br>- Fakturera <br>- Inleverera och fakturera |Vill du bokföra inleveransen? |Vill du bokföra inleveransen och fakturan?|
|Inköpsreturorder |- Leverera <br>- Fakturera <br>- Leverera och fakturera |Vill du bokföra utleveranserna? |Vill du bokföra utleveransen och fakturan?|
|Lagerinförsel |- Inleverera <br>- Inleverera och fakturera |Vill du bokföra inleveransen? |Vill du bokföra inleveransen och fakturan?|
|Dist.lager utleverans |- Leverera <br>- Leverera och fakturera | Vill du bokföra utleveranserna? |Vill du bokföra utleveransen och fakturan?|

   > [!Note]
   > Inställningen påverkar inte bokföring av redovisningsjournalrader där du kan välja **faktura** i fältet **dokumenttyp**.

## Se även

[Fakturaförsäljning](sales-how-invoice-sales.md)  
[Registrera inköp med inköpsfakturor och order](purchasing-how-record-purchases.md)  
[Köpa artiklar för en försäljning genom att skapa inköpsfakturor](purchasing-how-purchase-products-sale.md)
[Bli klara för affärsverksamhet](ui-get-ready-business.md)  
