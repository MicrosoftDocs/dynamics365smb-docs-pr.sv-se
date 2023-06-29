---
title: Utbyta data
description: 'Utbyta elektroniska affärsdokument, t.ex. bankfiler, mellan Business Central och externa parter.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'exchange data, external files, electronic documents, AMC Banking, OCT, SEPA'
ms.date: 06/10/2021
ms.author: edupont
---
# <a name="exchanging-data"></a><a name="exchanging-data"></a>Utbyta data
Du kan utbyta data mellan [!INCLUDE[prod_short](includes/prod_short.md)] och externa filer eller strömmar i gemensamma affärsuppgifter, till exempel för att skicka och ta emot elektroniska dokument och importera och exportera bankfiler.  

Innan du kan skicka och ta emot elektroniska dokument eller importera och exportera bankfiler måste du konfigurera ramverket för datautbyte för att bearbeta datafilerna eller strömmarna. Du måste dessutom konfigurera relaterade områden, exempelvis de kunder som du skickar elektroniska fakturor till, samt AMC Banking 365 Fundamentals-tillägget om du distribuerar bankfilskonverteringar till en extern tjänsteleverantör. Mer information finns i [Konfigurera datautbyte](across-set-up-data-exchange.md).  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**För att**|**Gå till**|  
|------------|-------------|  
|Konverterar försäljningsdokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)] till ett standardiserat format och skickar dem som elektroniska dokument som dina kunder kan ta emot i sina system.|[Skicka elektroniska dokument](sales-how-to-send-electronic-documents.md)|  
|Skicka PDF eller bildfiler till en leverantör av OCR-tjänster och få tillbaka dem som elektroniska dokument som därefter kan konverteras till dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)].|[Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md)|  
|Ta emot elektroniska dokument, antingen från OCR-servicen eller dokumentutbytestjänsten, i ett standardiserat format som du konverterar till relevanta dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)].|[Ta emot och omvandla elektroniska dokument](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Förbered för att importera kontoutdraget till sidan **Betalningsavstämningsjournal** som det första steget för avstämning av betalningar eller till fönstret **Bankkontoavstämning** som det första steget för avstämning av betalningar eller till sidan.|[Skapa tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)|  
|Exportera betalningar från sidan **Betalningsjournal** till en bankfil som du överför till ditt elektroniska bankkonto för bearbetning.|[Exportera betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)|
|Göra elektroniska betalningar i enlighet med EU:s kreditöverföringsstandard SEPA.|[Gör betalningar med tillägget AMC Banking 365 Fundamentals eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Be din bank att överföra betalningsbeloppen från kunders bankkonton till företagets konto enligt inställningarna för SEPA-autogiro.|[Skapa insamlingsposter för SEPA Autogiro och exportera till en bankfil](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)|  
|Använd en tjänstleverantör av valutakurser för att uppdatera sidan **valutor**.|[Uppdatera valutakurser](finance-how-update-currencies.md)|  
|Visa vilka filelement som mappas till fält i [!INCLUDE[prod_short](includes/prod_short.md)] när du importerar SEPA CAMT-kontoutdragsfiler.|[Fältmappning vid import av SEPA CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Exportera data för Intrastat-rapportering i [!INCLUDE[prod_short](includes/prod_short.md)].|[Ställa in Intrastat-rapporter](finance-how-setup-report-intrastat.md)|
|Visa vilka fält i [!INCLUDE[prod_short](includes/prod_short.md)] som mappas till filelement när du exporterar betalningsfiler med hjälp av AMC Banking 365 Fundamentals-tillägget.|[Fältmappning vid export av betalningsfiler med hjälp av AMC Banking 365 Fundamentals-tillägget](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a><a name="see-also"></a>Se även
[Konfigurera databyte](across-set-up-data-exchange.md)  
[Utbyta data elektroniskt](across-data-exchange.md)  
[Fakturaförsäljning](sales-how-invoice-sales.md)   
[Registrera inköp](purchasing-how-record-purchases.md)  
[Inkommande dokument](across-income-documents.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
