---
title: Utbyt data | Microsoft Docs
description: Du kan utbyta data mellan Business Central och externa filer eller strömmar i gemensamma affärsuppgifter, till exempel för att skicka och ta emot elektroniska dokument och importera och exportera bankfiler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2954fd3146b81f6511cec64f228714445b5fc486
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188714"
---
# <a name="exchanging-data"></a>Utbyta data
Du kan utbyta data mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och externa filer eller strömmar i gemensamma affärsuppgifter, till exempel för att skicka och ta emot elektroniska dokument och importera och exportera bankfiler.  

Innan du kan skicka och ta emot elektroniska dokument eller importera och exportera bankfiler måste du konfigurera ramverket för datautbyte för att bearbeta datafilerna eller strömmarna. Dessutom måste du ställa in relaterade områden, till exempel kunder som du skickar elektroniska fakturor till, och tillägget AMC Banking 365 Fundamentals om du distribuerar bankfilskonverteringar till en extern tjänsteleverantör. Mer information finns i [Konfigurera datautbyte](across-set-up-data-exchange.md).  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**För att**|**Gå till**|  
|------------|-------------|  
|Konverterar försäljningsdokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] till ett standardiserat format och skickar dem som elektroniska dokument som dina kunder kan ta emot i sina system.|[Skicka elektroniska dokument](sales-how-to-send-electronic-documents.md)|  
|Skicka PDF eller bildfiler till en leverantör av OCR-tjänster och få tillbaka dem som elektroniska dokument som därefter kan konverteras till dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md)|  
|Ta emot elektroniska dokument, antingen från OCR-servicen eller dokumentutbytestjänsten, i ett standardiserat format som du konverterar till relevanta dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Ta emot och omvandla elektroniska dokument](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Förbered för att importera kontoutdraget till sidan **Betalningsavstämningsjournal** som det första steget för avstämning av betalningar eller till fönstret **Bankkontoavstämning** som det första steget för avstämning av betalningar eller till sidan.|[Skapa tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)|  
|Exportera betalningar från sidan **Betalningsjournal** till en bankfil som du överför till ditt elektroniska bankkonto för bearbetning.|[Exportera betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)|
|Göra elektroniska betalningar i enlighet med EU:s kreditöverföringsstandard SEPA.|[Gör betalningar med tillägget AMC Banking 365 Fundamentals eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Be din bank att överföra betalningsbeloppen från kunders bankkonton till företagets konto enligt inställningarna för SEPA-autogiro.|[Skapa insamlingsposter för SEPA Autogiro och exportera till en bankfil](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)|  
|Använd en tjänstleverantör av valutakurser för att uppdatera sidan **valutor**.|[Uppdatera valutakurser](finance-how-update-currencies.md)|  
|Visa vilka filelement som mappas till fält i [!INCLUDE[d365fin](includes/d365fin_md.md)] när du importerar SEPA CAMT-kontoutdragsfiler.|[Fältmappning vid import av SEPA CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Visa vilka fält i [!INCLUDE[d365fin](includes/d365fin_md.md)] som mappas till filelement när betalningsfiler exporteras med tillägget AMC Banking 365 Fundamentals.|[Fältmappning vid export av betalningsfiler med tillägget AMC Banking 365 Fundamentals](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Se även  
[Konfigurera datautbyte](across-set-up-data-exchange.md)  
[Utbyta data elektroniskt](across-data-exchange.md)  
[Fakturaförsäljning](sales-how-invoice-sales.md)   
[Registrera inköp](purchasing-how-record-purchases.md)  
[Inkommande dokument](across-income-documents.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
