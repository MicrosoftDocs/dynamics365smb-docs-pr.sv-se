---
title: Statusfält i dokument
description: 'Lär dig om statusen Öppna och Släppta för offert-, order- eller kreditnota-dokument.'
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,'
ms.search.form: null
ms.date: 09/19/2022
ms.author: bholtorf
---
# <a name="status-field-on-documents"></a><a name="status-field-on-documents"></a>Statusfält i dokument

När du skapar en offert, order eller kreditnota, står det som standard **Öppen** i fältet **Status** i dokumenthuvudet.

När du har fyllt i dokumentet kan du släppa det, och [!INCLUDE[prod_short](includes/prod_short.md)] ändrar värdet i fältet **Status** till **Släppt**. Denna status visar att ordern är klar för nästa steg i processen, innan den bokförs.

| Status | Description |
| ------ | ----------- |
| Öppna   | Du kan göra ändringar i dokumentet. |
| Släppt | Dokumentet har släppts till nästa steg i processen och du kan inte göra ändringar i rader av typen *Artikel* och *Anläggningstillgång*.<br /><br />Du kan öppna ett släppt dokumentet igen om du vill göra ändringar. Om du vill flytta det justerade dokumentet till nästa behandlingsetapp måste du släppa det igen. |
| Väntar på godkännande   | Dokumentet väntar på att godkännas. |
| Väntar på förskottsbetalning | En förskottsfaktura har bokförts för dokumentet. |

## <a name="release-process"></a><a name="release-process"></a>Släppningsprocess

Utsläppsförloppet kan användas på olika sätt för att förenkla det vanliga arbetsflödet, t.ex. företagets rutiner för godkännande eller för att starta lageraktiviteter.

### <a name="approval-procedures"></a><a name="approval-procedures"></a>Rutiner för godkännande

Utsläppsförloppet kan användas inom företaget för att visa att en annan användare har godkänt dokumentet, eller att en extern kontakt klarar att uppfylla specifikationerna i dokumentet. Här är några exempel:

* En inköpsorder kan inte släppas förrän den har bekräftats av leverantören.
* En annan användare måste (t.ex. av säkerhetsskäl) godkänna en order som du har skapat innan du kan släppa den.
* En kreditnota som du har skapat måste släppas av den chef som godkänner returer.

Lär dig mer om arbetsflöde för godkännande på [Använda arbetsflöden](across-use-workflows.md).

### <a name="warehouse-activities"></a><a name="warehouse-activities"></a>Lageraktiviteter

Så länge en order har status **Öppen**, börjar lagret inte att förbereda in- eller utleverans av artiklarna på ordern. Genom att släppa ordern visar du att den är färdig och kan tas med i lageraktiviteterna.

## <a name="reopen-a-released-order"></a><a name="reopen-a-released-order"></a>Öppna en släppt order igen

Om du vill göra ändringar i en släppt order, kan du öppna ordern igen. För de rader som redan har behandlats av lagret, kan du dock bara öka antalet.

När du gör ändringarna och släpper beställningen igen räknar [!INCLUDE [prod_short](includes/prod_short.md)] om moms och fakturarabatt.

Om du gör ändringar i en order som redan är släppt, måste du meddela lagret om ändringarna.

> [!NOTE]
> Om du vill bokföra en öppen order eller kreditnota utan att släppa den först, släpper [!INCLUDE [prod_short](includes/prod_short.md)] dokumentet automatiskt när du bokför det. Om du bokför order eller kreditnotor med hjälp av funktionen **Bokför batch-jobb**, kan du välja att bara bokföra de order eller kreditnotor som du har släppt.

## <a name="see-also"></a><a name="see-also"></a>Se även

[Sälja produkter med en kundförsäljningsreturorder](sales-how-sell-products.md)  
[Registrera inköp med inköpsfakturor](purchasing-how-record-purchases.md)  
[Leverera artiklar](warehouse-how-ship-items.md)  
[Ta emot artiklar](warehouse-how-receive-items.md)  
[Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md)  
[Sortera, söka och filtrera listor](ui-enter-criteria-filters.md)  
[Arkivera dokument](across-how-to-archive-documents.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
