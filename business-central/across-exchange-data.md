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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0091f7ae1e6b22b6228ad903af783fb790faf99d
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692614"
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
|Exportera betalningar från sidan **Betalningsjournal** till en bankfil som du överför till ditt elektroniska bankkonto för bearbetning.|[Exportera betalningar till en bankfil](payables-how-export-payments-bank-file.md)|
|Göra elektroniska betalningar i enlighet med EU:s kreditöverföringsstandard SEPA.|[Göra betalningar med tjänsten för bankdatakonvertering eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Be din bank att överföra betalningsbeloppen från kunders bankkonton till företagets konto enligt inställningarna för SEPA-autogiro.|[Skapa insamlingsposter för SEPA Autogiro och exportera till en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Använd en tjänstleverantör av valutakurser för att uppdatera sidan **valutor**.|[Uppdatera valutakurser](finance-how-update-currencies.md)|  
|Visa vilka filelement som mappas till fält i [!INCLUDE[d365fin](includes/d365fin_md.md)] när du importerar SEPA CAMT-kontoutdragsfiler.|[Fältmappning vid import av SEPA CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Visa vilka fält i [!INCLUDE[d365fin](includes/d365fin_md.md)] som mappas till filelement när betalningsfiler exporteras med tillägget AMC Banking 365 Fundamentals.|[Fältmappning vid export av betalningsfiler med tillägget AMC Banking 365 Fundamentals](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Se även  
[Konfigurera datautbyte](across-set-up-data-exchange.md)  
[Utbyta data elektroniskt](across-data-exchange.md).  
[Fakturaförsäljning](sales-how-invoice-sales.md)   
[Registrera inköp](purchasing-how-record-purchases.md)  
[Inkommande dokument](across-income-documents.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
