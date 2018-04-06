---
title: Utbyt data | Microsoft Docs
description: "Du kan utbyta data mellan Finance and Operations, Business edition och externa filer eller strömmar i samband med gemensamma affärsuppgifter, till exempel för att skicka och ta emot elektroniska dokument samt importera och exportera bankfiler."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5e9e0d0d7850d6f66a16bfe46363e57292d88fb6
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="exchanging-data"></a>Utbyta data
Du kan utbyta data mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och externa filer eller strömmar i gemensamma affärsuppgifter, till exempel för att skicka och ta emot elektroniska dokument och importera och exportera bankfiler.  

Innan du kan skicka och ta emot elektroniska dokument eller importera och exportera bankfiler måste du konfigurera ramverket för datautbyte för att bearbeta de inbegripna datafilerna eller strömmarna. Dessutom måste du skapa relaterade områden. Dessa omfattar huvuddata för kunder som du skickar till elektroniska fakturor till och bankdatakonverteringstjänsten om du distribuerar bankfilkonverteringar till en extern tjänsteleverantör. Mer information finns i [Konfigurera datautbyte](across-set-up-data-exchange.md).  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**För att**|**Gå till**|  
|------------|-------------|  
|Konverterar försäljningsdokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] till ett standardiserat format och skickar dem som elektroniska dokument som dina kunder kan ta emot i sina system.|[Skicka elektroniska dokument](sales-how-to-send-electronic-documents.md)|  
|Skicka PDF eller bildfiler till en leverantör av OCR-tjänster och få tillbaka dem som elektroniska dokument som därefter kan konverteras till dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md)|  
|Ta emot elektroniska dokument, antingen från OCR-servicen eller dokumentutbytestjänsten, i ett standardiserat format som du konverterar till relevanta dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Ta emot och omvandla elektroniska dokument](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Importera kontoutdraget till fönstret **Betalningsavstämningsjournal** som det första steget för avstämning av betalningar eller till fönstret **Bankkontoavstämning** som det första steget för avstämning av betalningar eller till fönstret.|[Konfigurera bankfeedtjänsten Envestnet Yodlee](bank-how-setup-bank-statement-service.md)|  
|Exportera betalningar från fönstret **Betalningsjournal** till en bankfil som du överför till ditt elektroniska bankkonto för bearbetning.|[Exportera betalningar till en bankfil](payables-how-export-payments-bank-file.md)|
|Göra elektroniska betalningar i enlighet med EU:s kreditöverföringsstandard SEPA.|[Göra betalningar med tjänsten för bankdatakonvertering eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Be din bank att överföra betalningsbeloppen från kunders bankkonton till företagets konto enligt inställningarna för SEPA-autogiro.|[Skapa insamlingsposter för SEPA Autogiro och exportera till en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Använd en tjänstleverantör av valutakurser för att uppdatera fönstret **valutor**.|[Uppdatera valutakurser](finance-how-update-currencies.md)|  
|Visa vilka filelement som mappas till fält i [!INCLUDE[d365fin](includes/d365fin_md.md)] när du importerar SEPA CAMT-kontoutdragsfiler.|[Fältmappning vid import av SEPA CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Visa vilka fält som mappas i [!INCLUDE[d365fin](includes/d365fin_md.md)] för att lagra element när du exporterar betalningsfiler med hjälp av tjänsten för bankdatakonvertering.|[Fältmappning vid export av betalningsfiler via bankdatakonverteringstjänst](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Se även  
[Konfigurera datautbyte](across-set-up-data-exchange.md)  
[Utbyta data elektroniskt](across-data-exchange.md).  
[Fakturaförsäljning](sales-how-invoice-sales.md)   
[Registrera inköp](purchasing-how-record-purchases.md)  
[Inkommande dokument](across-income-documents.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  

