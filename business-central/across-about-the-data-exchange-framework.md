---
title: Om ramverket för datautbyte
description: I det här avsnittet beskrivs hur du använder Data Exchange Framework för att hantera utbytet av data i affärsdokument som fakturor med dina affärspartners.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Data exchange framework, data files, data exchange, electronic document, invoice, Business Central, business document, standard-compliant file, OCR
ms.date: 06/10/2021
ms.author: edupont
ms.openlocfilehash: 53c0bcbf03f989175783ebb93228815712c25552
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439124"
---
# <a name="about-the-data-exchange-framework"></a>Om ramverket för datautbyte

Du kan använda ramverket för dataintegrering för att hantera utbytet av affärsdokument, bankfiler, valutakurser och andra datafiler med dina affärspartner.

Som administratör eller Microsoft-partner kan du använda ramverket i nya integreringsfunktioner genom att ställa in vilka data som ska utbytas och hur. Exempelvis varierar formatet på filer för utbyte av data i bankfiler, elektroniska dokument, valutakurser och annat med ERP-system beroende på leverantören av datafilen eller strömmen och på land/region. [!INCLUDE[prod_short](includes/prod_short.md)] stöder olika bankfilformat och datatjänststandarder. För att få stöd för andra elektroniska dokumentformat använder du ramverket för datautbyte.

 Följande diagram visar arkitekturen för ramverket för datautbyte.  

 ![Ramverk för dataintegrering &#45; Importera.](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Ramverk för dataintegrering &#45; Exportera.](media/across-data-exchange/dataexchangeframework_export.png)  

## <a name="electronic-documents"></a>Elektroniska dokument

Som alternativ till att e-posta en filbilaga kan du skicka och ta emot elektroniska affärsdokument. Med elektroniska dokument menas en standarduppfyllande fil som representerar ett affärsdokument, till exempel en faktura från en leverantör som du kan ta emot och konvertera till en inköpsorder i [!INCLUDE[prod_short](includes/prod_short.md)] . Utbytet av elektroniska dokument mellan två handelspartners utförs av en extern leverantör av dokumentväxlingstjänster. Den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] stöder utskick och mottagning av elektroniska fakturor och kreditnotor i PEPPOL-format, som stöds av de största leverantörerna av dokumentväxlingstjänster. En större leverantör av dokumentväxlingstjänster är förkonfigurerad och klar att ställa in för ditt företag. Om du vill tillhandahålla stöd för andra elektroniska dokumentformat måste du skapa nya datumutbytesdefinitioner med hjälp av ramverket för datautbyte.  

 Från PDF- eller bildfiler som representerar inkommande dokument kan du låta en extern OCR-tjänst (Optical Character Recognition) skapa elektroniska dokument som du kan konvertera till dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)] som du gör för elektroniska PEPPOL-dokument. När du exempelvis tar emot en faktura i PDF-format från leverantören, kan du skicka den till OCR-tjänsten från sidan **Inkommande dokument**. Efter några sekunder får du tillbaka filen tillbaka som en elektronisk faktura som kan omvandlas till en inköpsfaktura för leverantören. Om du skicka filen till OCR-tjänsten via e-post, skapas en ny inkommande dokumentpost automatiskt när du får tillbaka det elektroniskt dokument.  

 Om du vill skicka exempelvis en försäljningsfaktura som ett elektroniskt PEPPOL-dokument väljer du **Elektroniskt dokument** i dialogrutan **Bokför och skicka**. Härifrån kan du också ange kundens dokument för standardprofil för dokumentutskick. Först måste du skapa olika huvuddata, som företagsinformation, kunder, artiklar och enheter. De används för att identifiera dina affärspartner och artiklar vid konvertering av data i fält i [!INCLUDE[prod_short](includes/prod_short.md)] till element i den utgående dokumentfilen. Datakonverteringen och utskicket av PEPPOL-försäljningsfakturan utförs av dedikerade kodenheter och XMLports som representeras av det elektroniska dokumentformatet **PEPPOL**.  

 Om du exempelvis vill ta emot en faktura från en leverantör som ett elektroniskt PEPPOL-dokument behandlar du dokumentet på sidan **Inkommande dokument** för att konvertera det till en inköpsfaktura i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan antingen konfigurera jobbköfunktionen för regelbunden behandling av sådana filer eller starta processen manuellt. Först måste du skapa olika huvuddata, som företagsinformation, leverantörer, artiklar och enheter. De används för att identifiera dina affärspartner och artiklar när du konverterar data i element i den inkommande dokumentfilen till fält i [!INCLUDE[prod_short](includes/prod_short.md)]. Mottagningen och datakonverteringen av PEPPOL-fakturan utförs av ramverket för datautbyte som representeras i definitionen för datautbyte i **PEPPOL – Faktura**.  

  Om du vill ta emot, till exempel, en faktura som ett elektroniskt OCR-dokument, behandlar du det som när du tar emot ett elektroniskt PEPPOL-dokument. Mottagningen och konverteringen av elektroniska dokument från OCR utförs av ramverket för datautbyte som representeras i definitionen för datautbyte i **OCR – Faktura**.  

## <a name="bank-files"></a>Bankfiler

Filformaten för utbyte av bankdata med ERP-system varierar beroende på leverantören av filen och på landet eller regionen. [!INCLUDE[prod_short](includes/prod_short.md)] stöder import och export av SEPA-bankfiler (Single Euro Payments Area) och med tillägget AMC Banking 365 Fundamentals kan du ansluta till ett AMC Banking 365 Fundamentals-tillägg som tillhandahålls av en extern leverantör, AMC Consult. För att få stöd för andra elektroniska dokumentformat använder du ramverket för datautbyte.  

Om du vill exportera SEPA-krediteringsöverföringar väljer du knappen **Exportera betalningar till fil** på sidan **Betalningsjournal** och överför sedan filen för att bearbeta betalningarna i din bank. Först måste du skapa olika huvuddata, som bankkonto, leverantörer och betalningssätt. Datakonverteringen och exporten av SEPA-bankdata utförs av en dedikerad codeunit och XMLport som representeras i bankexport-/importinställningarna för **SEPA-kreditöverföring**. Du kan också konfigurera tillägget AMC Banking 365 Fundamentals för att utföra exporten som representeras av datautbytesdefinitionen **AMC Banking 365 Fundamentals-tillägget – kreditöverföring**.  

 Om du vill exportera instruktioner för SEPA-direktdebitering väljer du knappen **Exportera autogirofil** på sidan **Samlingar med autogiro** och skickar dem sedan till din bank för automatisk inkassering av de relevanta kundbetalningarna. Först måste du skapa bankkonton, kunder, fullmakter för autogiro och betalningssätt. Datakonverteringen och exporten av SEPA-bankdata utförs av en dedikerad codeunit och XMLport som representeras i bankexport/-importinställningarna för **SEPA Autogiro**.  

 Om du vill importera SEPA-bankutdrag väljer du knappen Importera bankutdrag på sidan **Betalningsavstämningsjournal** och **Bankkontoavstämning** och fortsätter sedan med att koppla varje bankutdragspost till betalningar eller bankkontoposter, manuellt eller automatiskt. Först måste du konfigurera bankkonton. Importen och datakonverteringen av SEPA-bankdata utförs av ramverket för datautbyte som representeras i definitionen för datautbyte i **SEPA AMT**. Du kan också konfigurera tillägget AMC Banking 365 Fundamentals för att utföra importen som representeras av datautbytesdefinitionen **AMC Banking 365 Fundamentals-tillägget – kontoutdrag**.  

 Dessutom stöder de lokala versionerna av [!INCLUDE[prod_short](includes/prod_short.md)] olika andra filformat för att importera och exportera bankdata, lönetransaktioner och andra data. För mer information, se landningssidan [Lokal funktionalitet](about-localization.md) för ditt land/din region under Hjälp.  

## <a name="currency-exchange-rates"></a>Valutakurser

Du kan ställa in en extern tjänst för kontinuerlig uppdatering av aktuella valutakurser. Tjänsten, som tillhandahåller valutakurser, aktiveras av en datautbytesdefinition. Därför är sidan **Inställning valutakursuppdatering** en kondenserad vy av sidan **Data Exchange definitionen** för definitionen av datautbytet i fråga.  

För alla utbyten av data i XML-filer kan du förbereda dataväxlingsinställningen genom att ladda den relaterade XML-schemafilen på sidan **Visningsprogram för XML-schema**. Här väljer du dataelementen som du vill utbyta med [!INCLUDE[prod_short](includes/prod_short.md)] och sedan initialiserar du antingen en definition för datautbyte eller genererar en XMLport.

## <a name="see-also"></a>Se även

[Utbyta data elektroniskt](across-data-exchange.md)  
[Använda XML-scheman för att förbereda datautbytesdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Konfigurera datautbyte](across-set-up-data-exchange.md)  
[Inkommande dokument](across-income-documents.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]