---
title: Översikt över uppgifter för hantering av inköp
description: 'Beskriver uppgifter för hantering av inköp eller inköpsprocesser, inklusive hur inköpsfakturor och inköpsorder fungerar.'
author: brentholtorf
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '460, 9307'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Inköp

Du skapar en inköpsfaktura eller inköpsorder för att registrera kostnaden för inköp och för att spåra leverantörsskulder. Om du vill kontrollera ett lager används inköpsfakturor också för att uppdatera lagernivåer dynamiskt, så att du kan minimera lagerkostnader och ge bättre service. Inköpskostnaderna, inklusive serviceutgifter, och lagervärde som kommer från bokföring av inköpsfakturor bidrar till vinstsiffror och övriga ekonomiska nyckeltal i rollcentret.

Du måste använda inköpsorder om din inköpsprocess kräver att du t. ex. kan registrera delleveranser av en orderkvantitet eftersom hela kvantiteten inte var tillgänglig hos leverantören. Om du säljer artiklar genom att leverera direkt från din leverantör till kunden, som en direktleverans, måste du även använda inköpsorder. För mer information finns i [Utföra direktleveranser](sales-how-drop-shipment.md). I alla andra aspekter fungerar inköpsorder på samma sätt som inköpsfakturor.

Du kan låta inköpsfakturor skapas automatiskt, genom att använda OCR-tjänsten (optisk teckenigenkänning) för att konvertera PDF-fakturor från leverantörer till elektroniska dokument, som sedan omvandlas till inköpsfakturor av ett arbetsflöde. För att kunna använda den här funktionen måste du först utföra registrera dig för OCR-tjänsten och därefter utföra olika inställningar. Mer information finns i [inkommande dokument](across-income-documents.md).

Produkter kan vara både lagerartiklar och tjänster. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

För alla inköpsprocesser kan du t. ex. inkludera ett arbetsflöde för godkännande för att kräva att stora inköp godkänns av redovisningschefen. Mer information finns i [Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Till | Gå till |
| --- | --- |
| Skapa en inköpsfaktura för att registrera en överenskommelse med en leverantör om att köpa produkter till vissa leverans- och betalningsvillkor. |[Registrera inköp](purchasing-how-record-purchases.md) |
|Skapa en inköpsoffert för att återspegla en anbudsförfrågan från leverantören, som du senare kan konvertera till en inköpsorder.|[Begär offerter](purchasing-how-request-quotes.md)|
| Skapa en inköpsfaktura för alla eller valda rader på en försäljningsfaktura. |[Köpa artiklar för en försäljning](purchasing-how-purchase-products-sale.md) |
|Förstå vad som händer när du bokför inköpsdokument.|[Bokföra inköp](ui-post-purchases.md)|
| Utför en åtgärd på en obetald bokförd inköpsfaktura som automatiskt skapar en kreditnota och antingen annullerar inköpsfakturan eller skapar den på nytt, så att du kan göra korrigeringar. |[Korrigera eller makulera obetalda försäljningsfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Skapa en inköpskreditnota för att återföra en särskild bokförd inköpsfaktura för att visa produkter som du returnerar till leverantören, och vilka belopp som du ska inkassera. |[Behandla inköpsreturer eller annulleringar](purchasing-how-register-new-vendors.md) |
|Förbered för att fakturera flera inleveranser från samma leverantör en gång genom att kombinera inleveranser på en faktura.|[Kombinera inleveranser på en enda faktura](purchasing-how-to-combine-receipts.md)|
|Konvertera till exempel elektroniska fakturor från leverantörer till fakturor i Business Central.|[Ta emot och omvandla elektroniska dokument](purchasing-how-to-receive-and-convert-electronic-documents.md)|
| Lär dig hur [!INCLUDE[prod_short](includes/prod_short.md)] beräknas när du måste beställa en artikel för ett visst datum.|[Datumberäkning för inköp](purchasing-date-calculation-for-purchases.md)|
|Lösa problem när det finns två eller flera poster för samma leverantör.|[Slå samman dubblettposter](sales-how-merge-duplicate-records.md)|
|Hantera ditt engagemang för en leverantör för att köpa stora kvantiteter som levereras i flera leveranser med tiden.|[Arbeta med inköpsavropsorder](sales-how-to-create-blanket-sales-orders.md)|

## Externa dokumentnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Se även

[Ställa in inköp](purchasing-setup-purchasing.md)  
[Registrera nya leverantörer](purchasing-how-register-new-vendors.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Hantera projekt](projects-manage-projects.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
