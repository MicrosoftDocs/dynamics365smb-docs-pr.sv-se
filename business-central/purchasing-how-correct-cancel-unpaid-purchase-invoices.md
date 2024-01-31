---
title: Korrigera eller annullera obetalda inköpsfakturor (innehåller video)
description: 'Förklarar hur du kan korrigera, avbryta eller ångra en bokförd inköpsfaktura eller skapa en inköpskreditnota automatiskt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '138, 140, 146'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Korrigera eller annullera obetalda inköpsfakturor

Du kan korrigera eller annullera en bokförd inköpsfaktura. Det är användbart om du vill rätta till ett skrivfel eller om du vill ändra inköpet tidigt i orderprocessen.

Om du redan har betalt för produkter på den bokförda inköpsfakturan kan du inte rätta eller annullera den från själva den bokförda inköpsfakturan. I stället måste du skapa en inköpskreditnota manuellt för att återföra inköpet, alternaivt hanterat med en inköpsreturorder. Detsamma gäller om du vill ändra en bokförd inköpsfaktura som baseras på en kombinerad inleverans. Mer information finns i [Så här behandlar du inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md).

På sidan **Bokförd inköpsfaktura** kan du välja knappen **Korrigera** eller knappen **Avbryt**. När du uppdaterar eller avbryter en bokförd inköpsfaktura gäller den korrigerande inköpskreditnotan för alla redovisnings- och inventeringstransaktioner som skapades när den ursprungliga inköpsfakturan bokfördes. Det återför den bokförda inköpsfakturan i dina ekonomiska transaktioner och lämnar bokförd korrigering av inköpskreditnota för din verifieringskedja. I det följande beskrivs användningen av **Korrigera** och **Avbryt**.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## Korrigera en bokförd inköpsfaktura

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **bokförda inköpsfakturor** och väljer sedan relaterad länk.  
2. Markera den bokförda inköpsfakturan som du vill korrigera.  

    > [!NOTE]  
    >   Om kryssrutan **Avbruten** kan du inte rätta den bokförda inköpsfakturan, eftersom den redan har korrigerats eller annullerats.
3. På sidan **Bokförd inköpsfaktura** väljer du **korrigera**.

    En ny inköpsfaktura med samma information skapas där du kan göra rättningen. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md). Fältet **Avbruten** på den först bokförda inköpsfakturan ändras till **Ja**.

    En inköpskreditnota skapas automatiskt och bokförs för att annullera den ursprungligt bokförda inköpsfakturan.
4. Välj **Visa korrigerande kreditnota** för att visa de bokförda inköpskreditnotorna som annullerar den ursprungliga bokförda inköpsfakturan.

## Avbryta en bokförd inköpsfaktura

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **bokförda inköpsfakturor** och väljer sedan relaterad länk.  
2. Markera den bokförda inköpsfakturan som du vill annullera.

    > [!NOTE]  
    >   Om kryssrutan **Avbruten** kan du inte avbryta den bokförda inköpsfakturan, eftersom den redan har korrigerats eller annullerats.
3. På sidan **Bokförd inköpsfaktura** väljer du **Annullera**.

    En inköpskreditnota skapas automatiskt och bokförs för att annullera den ursprungligt bokförda inköpsfakturan. Fältet **Avbruten** på den först bokförda inköpsfakturan ändras till **Ja**.
4. Välj **Visa korrigerande kreditnota** för att visa de bokförda inköpskreditnotorna som annullerar den ursprungliga bokförda inköpsfakturan.

### Delfakturabokföring stöds också

Om annulleringen är knuten till en delfakturabokföring uppdateras den ursprungliga inköpsorderraden så att den återspeglar det annullerade fakturerade antalet. Fälten **Ant. att fakturera** och **Antal fakturerat** på den relaterade inköpsorderraden återställs till värdena före delbokföringen.

## Se även

[Inköp](purchasing-manage-purchasing.md)  
[Registrera inköp](purchasing-how-record-purchases.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
