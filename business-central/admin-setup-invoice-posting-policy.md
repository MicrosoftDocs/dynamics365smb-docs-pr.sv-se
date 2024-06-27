---
title: Definiera en bokföringspolicy för faktura för användare
description: Använd regler för fakturabokföring för att kontrollera om en användare kan bokföra försäljnings- och inköpsfakturor.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/12/2024
ms.custom: bap-template
ms.search.forms: '119, 9807,'
ms.service: dynamics-365-business-central
---

# <a name="define-an-invoice-posting-policy-for-users"></a>Definiera en bokföringspolicy för faktura för användare

Företag har ofta unika processer för att bokföra försäljnings- och inköpsfakturor och leveranser. Processer kan till exempel variera från en person som bokför allt på en inköpsorder, till flera anställda. Du kan begränsa användare från bokföringsfakturor eller kräva att fakturor bokförs tillsammans med leveranser eller inleveranser.

## <a name="to-specify-a-posting-policy"></a>Så här anger du bokföringspolicy

På sidan **användarinställningar** i fälten **Bokföringspolicy för försäljningsfaktura** och **Bokföringsprincip för inköpsfaktura** välj ett av följande alternativ:

* **Tillåten** (standard) – Behåll det nuvarande beteendet, där en användare kan välja vilket inläggsalternativ som ska användas, som t.ex. **leverera**, **faktura** och **leverera och fakturera**. 
* **Förbjuden** – hindrar användaren från att bokföra fakturor. [!INCLUDE [prod_short](includes/prod_short.md)] visar en bekräftelsedialogruta som endast innehåller alternativen **Leverera** eller **fakturera**.
* **Obligatorisk** – gör att användaren kan bokföra fakturor tillsammans med inleveranser eller utleveranser. [!INCLUDE [prod_short](includes/prod_short.md)] visar en bekräftelse dialogruta med alternativ **leverans och fakturera** eller **mottagning och fakturera**.

## <a name="effect-on-documents"></a>Inverkan på dokument

I följande tabell beskrivs hur fakturana bokföringsprinciper påverkar dokument.

> [!NOTE]
> När du bokför försäljnings- och inköpsfakturor och kreditnotor har du inga bokföringsalternativ. I dokumenten bokförs alltid de fysiska och ekonomiska transaktionerna tillsammans. Du kan inte delvis bokföra fakturor och kreditnotor.

|Dokument | Alternativ 1: Tillåt <br>Visar en serie alternativ| Alternativ 2: otillåtet <br>Bekräftelsedialogruta | Alternativ 3: obligatorisk <br>Bekräftelsedialogruta|
|--|--|--|--|
|Försäljningsorder |- Leverera <br>- Fakturera <br>- Leverera och fakturera |Vill du bokföra utleveranserna? |Vill du bokföra utleveransen och fakturan?|
|Försäljningsfaktura|Inga alternativ| Bokföring är förbjuden per användarinställning|Vill du bokföra fakturan?|
|Försäljningskreditnota|Inga alternativ|Bokföring är förbjuden per användarinställning|Vill du bokföra kreditnotan?|
|Försäljningreturorder |- Inleverera <br>- Fakturera <br>- Inleverera och fakturera |Vill du bokföra inleveransen? |Vill du bokföra inleveransen och fakturan?|
|Lagerplockning |- Leverera <br>- Leverera och fakturera |Vill du bokföra utleveranserna? |Vill du bokföra utleveransen och fakturan?|
|Inköpsorder |- Inleverera <br>- Fakturera <br>- Inleverera och fakturera |Vill du bokföra inleveransen? |Vill du bokföra inleveransen och fakturan?|
|Inköpsfaktura|Inga alternativ|Bokföring är förbjuden per användarinställning|Vill du bokföra fakturan?|
|Inköpskreditnota|Inga alternativ|Bokföring är förbjuden per användarinställning|Vill du bokföra kreditnotan?|
|Inköpsreturorder |- Leverera <br>- Fakturera <br>- Leverera och fakturera |Vill du bokföra utleveranserna? |Vill du bokföra utleveransen och fakturan?|
|Lagerinförsel |- Inleverera <br>- Inleverera och fakturera |Vill du bokföra inleveransen? |Vill du bokföra inleveransen och fakturan?|
|Dist.lager utleverans |- Leverera <br>- Leverera och fakturera | Vill du bokföra utleveranserna? |Vill du bokföra utleveransen och fakturan?|

   > [!Note]
   > Inställningen påverkar inte bokföring av redovisningsjournalrader där du kan välja **faktura** i fältet **dokumenttyp**.

## <a name="see-also"></a>Se även

[Fakturaförsäljning](sales-how-invoice-sales.md)  
[Registrera inköp med inköpsfakturor och order](purchasing-how-record-purchases.md)  
[Köpa artiklar för en försäljning genom att skapa inköpsfakturor](purchasing-how-purchase-products-sale.md)
[Bli klara för affärsverksamhet](ui-get-ready-business.md)  
