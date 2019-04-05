---
title: Elektroniska dokument i Business Central   | Microsoft Docs
description: Introduktion till att skicka och ta emot elektroniska dokument i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 147a7e41d490167fceb76ff89de1f6c628223914
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "808276"
---
# <a name="exchanging-data-electronically"></a>Utbyta data elektroniskt.
Du kan använda ramverket för dataintegration för att utbyta affärsdokument, bankfiler, valutakurser och andra datafiler med dina affärspartner.

## <a name="electronic-documents"></a>Elektroniska dokument
Som alternativ till att e-posta en filbilaga kan du skicka och ta emot elektroniska affärsdokument. Med elektroniska dokument menas en standarduppfyllande fil som representerar ett affärsdokument, till exempel en faktura från en leverantör som du kan ta emot och konvertera till en inköpsorder i [!INCLUDE[d365fin](includes/d365fin_md.md)] . Utbytet av elektroniska dokument mellan två handelspartners utförs av en extern leverantör av dokumentväxlingstjänster. Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] stöder utskick och mottagning av elektroniska fakturor och kreditnotor i PEPPOL-format, som stöds av de största leverantörerna av dokumentväxlingstjänster. En större leverantör av dokumentväxlingstjänster är förkonfigurerad och klar att ställa in för ditt företag. Om du vill tillhandahålla stöd för andra elektroniska dokumentformat måste du skapa nya datumutbytesdefinitioner med hjälp av ramverket för datautbyte.  

Från PDF- eller bildfiler som representerar inkommande dokument kan du låta en extern OCR-tjänst (Optical Character Recognition) skapa elektroniska dokument som du kan konvertera till dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du gör för elektroniska PEPPOL-dokument. När du exempelvis tar emot en faktura i PDF-format från leverantören, kan du skicka den till OCR-tjänsten från sidan **Inkommande dokument**. Efter några sekunder får du tillbaka filen tillbaka som en elektronisk faktura som kan omvandlas till en inköpsfaktura för leverantören. Om du skicka filen till OCR-tjänsten via e-post, skapas en ny inkommande dokumentpost automatiskt när du får tillbaka det elektroniskt dokument.  

Om du vill skicka exempelvis en försäljningsfaktura som ett elektroniskt PEPPOL-dokument väljer du **Elektroniskt dokument** i dialogrutan **Bokför och skicka**. Härifrån kan du också ange kundens dokument för standardprofil för dokumentutskick. Först måste du skapa olika huvuddata, som företagsinformation, kunder, artiklar och enheter. De används för att identifiera dina affärspartner och artiklar vid konvertering av data i fält i [!INCLUDE[d365fin](includes/d365fin_md.md)] till element i den utgående dokumentfilen. Datakonverteringen och utskicket av PEPPOL-försäljningsfakturan utförs av dedikerade kodenheter och XMLports som representeras av det elektroniska dokumentformatet **PEPPOL**.  

Om du exempelvis vill ta emot en faktura från en leverantör som ett elektroniskt PEPPOL-dokument behandlar du dokumentet på sidan **Inkommande dokument** för att konvertera det till en inköpsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan antingen konfigurera jobbköfunktionen för regelbunden behandling av sådana filer eller starta processen manuellt. Först måste du skapa olika huvuddata, som företagsinformation, leverantörer, artiklar och enheter. De används för att identifiera dina affärspartner och artiklar när du konverterar data i element i den inkommande dokumentfilen till fält i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mottagningen och datakonverteringen av PEPPOL-fakturan utförs av ramverket för datautbyte som representeras i definitionen för datautbyte i **PEPPOL – Faktura**.  

 Om du vill ta emot, till exempel, en faktura som ett elektroniskt OCR-dokument, behandlar du det som när du tar emot ett elektroniskt PEPPOL-dokument. Mottagningen och konverteringen av elektroniska dokument från OCR utförs av ramverket för datautbyte som representeras i definitionen för datautbyte i **OCR – Faktura**.  

## <a name="bank-files"></a>Bankfiler  
 Filformaten för utbyte av bankdata med ERP-system varierar beroende på leverantören av filen och på landet/regionen. Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] stöder import och export av SEPA-bankfiler (Single Euro Payments Area) och en bankdatakonverteringstjänst tillhandahålls av den externa leverantören AMC Consult. För att få stöd för andra elektroniska dokumentformat använder du ramverket för datautbyte.  

Om du vill exportera SEPA-krediteringsöverföringar väljer du knappen **Exportera betalningar till fil** på sidan **Betalningsjournal** och överför sedan filen för att bearbeta betalningarna i din bank. Först måste du skapa olika huvuddata, som bankkonto, leverantörer och betalningssätt. Datakonverteringen och exporten av SEPA-bankdata utförs av en dedikerad codeunit och XMLport som representeras i bankexport-/importinställningarna för **SEPA-kreditöverföring**. Du kan också konfigurera bankdatakonverteringstjänsten för att utföra exporten som representeras av definitionen för datautbyte i **Bankdatakonverteringstjänst – kreditöverföring**.  

Om du vill exportera instruktioner för SEPA-direktdebitering väljer du knappen **Exportera autogirofil** på sidan **Samlingar med autogiro** och skickar dem sedan till din bank för automatisk inkassering av de relevanta kundbetalningarna. Först måste du skapa bankkonton, kunder, fullmakter för autogiro och betalningssätt. Datakonverteringen och exporten av SEPA-bankdata utförs av en dedikerad codeunit och XMLport som representeras i bankexport/-importinställningarna för **SEPA Autogiro**.  

Om du vill importera SEPA-bankutdrag väljer du knappen Importera bankutdrag på sidan **Betalningsavstämningsjournal** och **Bankkontoavstämning** och fortsätter sedan med att koppla varje bankutdragspost till betalningar eller bankkontoposter, manuellt eller automatiskt. Först måste du konfigurera bankkonton. Importen och datakonverteringen av SEPA-bankdata utförs av ramverket för datautbyte som representeras i definitionen för datautbyte i **SEPA AMT**. Du kan också konfigurera bankdatakonverteringstjänsten för att utföra importen som representeras av definitionen för datautbyte i **Bankdatakonverteringstjänst – bankkontoutdrag**.  

 Dessutom stöder de lokala versionerna av [!INCLUDE[d365fin](includes/d365fin_md.md)] andra olika filformat för att importera/exportera bankdata, lönetransaktioner och andra data. För mer information, se hjälpavsnittet “lokala funktioner” i din landsversion av [!INCLUDE[d365fin](includes/d365fin_md.md)] .  

## <a name="currency-exchange-rates"></a>Valutakurser  
Du kan ställa in en extern tjänst för kontinuerlig uppdatering av aktuella valutakurser. Tjänsten, som tillhandahåller valutakurser, aktiveras av en datautbytesdefinition. Därför är sidan **Inställning valutakursuppdatering** en kondenserad vy av sidan **Data Exchange definitionen** för definitionen av datautbytet i fråga.  

För alla utbyten av data i XML-filer kan du förbereda dataväxlingsinställningen genom att ladda den relaterade XML-schemafilen på sidan **Visningsprogram för XML-schema**. Här väljer du dataelementen som du vill utbyta med [!INCLUDE[d365fin](includes/d365fin_md.md)] och sedan initialiserar du antingen en definition för datautbyte eller genererar en XMLport.  

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|Om du vill|Gå till|  
|--------|---------|  
|Lär dig hur den ramverket för datautbyte fungerar.|[Om ramverket för datautbyte](across-about-the-data-exchange-framework.md)|  
|Förbered för datautbyte i en fil genom att återanvända filens xml-schema. Skapa dataintegrationsdefinitioner. Konfigurera huvuddata för utskick av elektroniska dokument. Konfigurera olika bankimport-/exportfält.|[Konfigurera datautbyte](across-set-up-data-exchange.md)|  
|Använd definitioner för datautbyte och skicka PEPPOL-fakturor, ta emot PEPPOL-fakturor, importera bankkontoutdrag och exportera bankbetalningfiler.|[Utbyta data](across-exchange-data.md)|  

## <a name="see-also"></a>Se även  
[Om ramverket för datautbyte](across-about-the-data-exchange-framework.md)  
[Använda XML-scheman för att förbereda dataintegreringsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Konfigurera datautbyte](across-set-up-data-exchange.md)  
[Utbyta data](across-exchange-data.md)  
[Inkommande dokument](across-income-documents.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)
