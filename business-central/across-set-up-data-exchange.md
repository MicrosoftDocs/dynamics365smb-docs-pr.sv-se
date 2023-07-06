---
title: Konfigurera datautbyte för att skicka och ta emot filer
description: Ställ in ramverket för datautbyte för att utbyta data med externa filer; att skicka och ta emot elektroniska dokument eller importera och exportera bankfiler.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="setting-up-data-exchange"></a><a name="setting-up-data-exchange"></a><a name="setting-up-data-exchange"></a>Konfigurera datautbyte

Innan du kan skicka och ta emot elektroniska dokument eller importera och exportera bankfiler måste du konfigurera ramverket för datautbyte för att bearbeta relevanta filerna. Du måste dessutom konfigurera relaterade områden, exempelvis de kunder som du skickar elektroniska fakturor till, eller också AMC Banking 365 Fundamentals-tillägget om du använder den externa tjänsteleverantören för att konvertera dina bankfiler. Mer information finns i [Utbyta data elektroniskt](across-data-exchange.md).  

 När [!INCLUDE[prod_short](includes/prod_short.md)] har konfiguerats för utbyte av data med externa filer kan användare använda konfigurationen i gemensamma affärsuppgifter, till exempel för att skicka och ta emot elektroniska dokument och importera och exportera bankfiler.  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**För att**|**Gå till**|  
|------------|-------------|  
|Ställ in den förkonfigurerade dokumentväxlingstjänsten för att aktivera att skicka och ta emot elektroniska dokumentet från och till [!INCLUDE[prod_short](includes/prod_short.md)].|[Konfigurera en tjänst för dokumentutbyte](across-how-to-set-up-a-document-exchange-service.md)|  
|Ställ in den förkonfigurerade OCR-tjänsten för att omvandla PDF- eller bildfiler till elektroniska dokument som därefter kan konverteras till dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)]|[Ställa in inkommande dokument](across-how-setup-income-documents.md)|  
|Ställ in en av två förkonfigurerade tjänster för att uppdaterade valutakurser ska få de senaste växelkurserna på sidan **Valutor**.|[Uppdatera valutakurser](finance-how-update-currencies.md)|  
|Dtäll in olika huvuddata, som företagsinformation, kunder, leverantörer, artiklar och enheter relaterade till mappning av data i [!INCLUDE[prod_short](includes/prod_short.md)]|[Konfigurera utskick och mottagning av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Skapa ett bankkonto, en leverantör och en utbetalningsjournal för SEPA-kreditöverföring.|[Konfigurera SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Förbered bankkontoformat, betalningssätt och kundavtal för SEPA-autogiro.|[Ta betalt med SEPA-postförskott](finance-collect-payments-with-sepa-direct-debit.md)|  
|Konfigurera användarautentisering samt URL:en till leverantören av det AMC Banking 365 Fundamentals-tillägg som krävs för att få bankfiler konverterade till just din banks format.|[Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)|  
|Konfigurera och aktivera en extern tjänst som låter dig importera kontoutdrag direkt som bankfeed.|[Ställa in bankutdragstjänsten](bank-how-setup-bank-statement-service.md)|  
|När kontoutdragstjänsten har aktiverats, länkar du bankkonton i [!INCLUDE[prod_short](includes/prod_short.md)]|[Skapa bankkonton](bank-how-setup-bank-accounts.md)|  
|Ställ in dataexport för Intrastat-rapportering i [!INCLUDE[prod_short](includes/prod_short.md)].|[Ställa in Intrastat-rapporter](finance-how-setup-report-intrastat.md)|
|Förbered för att konfigurera en ny datautbytesdefinition för en datafil eller strömma med hjälp av filens XML-schema för att autofylla snabbfliken **Kolumndefinitioner** på sidan **Definitioner för bokföringsbyte**.|[Använda XML-uppställningar för att förbereda dataintegreringsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Konfigurera ramverket för datautbyte så att användare kan ta emot ett nytt inköpsdokumentformat, skicka ett nytt försäljningsdokumentformat, importera en ny bankfil eller göra andra datautbyten.|[Skapa dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/electronic-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Utbyta data elektroniskt](across-data-exchange.md)  
[Inkommande dokument](across-income-documents.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
