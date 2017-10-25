---
title: "Fältmappning för export av bankbetalningsfiler | Microsoft Docs"
description: "När du exporterar betalningsfiler med hjälp av funktionen för bankdatakonvertering kommer de data du exporterar att bli exponerade för bankdatakonverteringstjänsten."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: f81d6dac79817d758ff0ae49322a18f1e5cdc9d8
ms.contentlocale: sv-se
ms.lasthandoff: 09/27/2017

---
# <a name="field-mapping-when-exporting-payment-files-using-bank-data-conversion-service"></a>Fältmappning vid export av betalningsfiler via bankdatakonverteringstjänst
När du exporterar betalningsfiler med hjälp av funktionen för bankdatakonvertering kommer de data du exporterar att bli exponerade för bankdatakonverteringstjänsten. Serviceleverantören är ansvarig för sekretessen för dessa data. Mer information om hur funktionen bankdatakonverteringstjänst fungerar finns i [Om ramverket för datautbyte](across-about-the-data-exchange-framework.md).  

> [!CAUTION]  
>  När du exporterar betalningsfiler med hjälp av funktionen för bankdatakonvertering kommer vissa av dina affärsdata att bli exponerade för tjänstleverantören. Serviceleverantören, AMC Consult A/S, är ansvarig för sekretessen för dessa data. Mer information finns i [Sekretesspolicy för AMC](http://go.microsoft.com/fwlink/?LinkId=510158).  

Följande tabell visar de fält i [!INCLUDE[d365fin](includes/d365fin_md.md)] från vilka data kan exporteras till tjänstleverantören.  

|Mappat fält|Fält i tabell|Bord|Beskrivning]-->|  
|------------------|--------------------|-----------|---------------------------------------|  
|Fordringsägarenr.|Fordringsägarenr.|Bankkonto|Den identifierare som tilldelas ditt företag av din bank för att kräva in betalningar|  
|Avsändarens bankkontonummer|Bankkontonr/IBAN|Bankkonto|Företagets bankkontonummer (IBAN eller annat) som registreras på bankkontokortet|  
|Avsändarens bankclearingstandard|Bankclearingstandard|Bankkonto|Den nationella bankens register som användes för avsändarens bankkonto|  
|Avsändarbankens clearingnr|Bankclearingnummer|Bankkonto|Identifieraren för avsändarens bank i förhållande till bankens namnregister som används|  
|Avsändarbankens BIC-nr|SWIFT kod|Bankkonto|SWIFT-identifieraren för avsändarens bankkonto|  
|Avsändarbankens kontovaluta|Valutakod|Bankkonto|Valutakod för avsändarens bankkonto|  
|Verifikationsnr|Verifikationsnr|Redovisningsjournalrad|Betalningsradens dokumentnummer|  
|Kopplas till externt dok.nr|Kopplas till externt dok.nr|Redovisningsjournalrad|Det externa dokumentnummer på fakturan eller kreditnotan ska betalningsraden ska kopplas till.|  
|Mottagarens ID|Kontonr|Redovisningsjournalrad|Numret för den kund eller leverantör som specificeras på betalningsraden|  
|Betalningsform|Bet.typ för bankdatakonvertering|Betalningssätt|Typen av banköverföring, till exempel inrikes eller internationell|  
|Betalningsreferens|Betalningsreferens|Redovisningsjournalrad|Betalningsradens betalningsreferens|  
|Mottagarens adress|Adress|Kund/Leverantör|Mottagaradressen som anges på kund- eller leverantörskortet|  
|Mottagarens ort|Stad|Kund/Leverantör|Mottagarens stad som anges på kund- eller leverantörskortet|  
|Mottagarens namn|Namn|Kund/Leverantör|Mottagarens namn som anges på kund- eller leverantörskortet|  
|Mottagarens lands-/regionkod|Lands-/regionkod|Kund/Leverantör|Mottagarens kod för land/region som anges på kundens eller leverantörens bankkontokort|  
|Mottagarens postnr|Postnr|Kund/Leverantör|Mottagarens postnummer för land/region som anges på kundens eller leverantörens bankkontokort|  
|Mottagarbankens kontonr|Bankkontonr/IBAN|Kund bankkonto/Leverantör bankkonto|Mottagarens bankkontonummer (IBAN eller annat nummer) som anges på kundens eller leverantörens bankkontokort|  
|Mottagarbankens clearingnr|Bankclearingstandard|Kund bankkonto/Leverantör bankkonto|Den nationella bankens register som användes för mottagarens bankkonto|  
|Mottagarbankens clearingst.|Bankclearingnummer|Kund bankkonto/Leverantör bankkonto|Identifieraren för mottagarens bankkonto i förhållande till bankens namnregister som används|  
|Mottagarens e-postadress|E-post|Kund/Leverantör|E-postadressen till mottagaren|  
|Meddelande till mottagare 1|Meddelande till mottagare|Redovisningsjournalrad|Meddelandet till mottagaren som anges på betalningsraden|  
|Belopp|Belopp|Redovisningsjournalrad|Beloppet på betalningsraden|  
|Valutakod|Valutakod|Redovisningsjournalrad|Valutakoden på betalningsraden|  
|Överföringsdatum|Bokföringsdatum|Redovisningsjournalrad|Bokföringsdatumet för betalningsraden|  
|Fakturabelopp|Ursprungligt belopp|Kund/Lev.reskontratransaktion|Beloppet på den transaktion som betalningen kopplas till.|  
|Fakturadatum|Dokumentdatum|Kund/Lev.reskontratransaktion|Fakturadatumet på den transaktion som betalningen kopplas till|  
|Mottagarbankens adress|Adress|Kund bankkonto/Leverantör bankkonto|Mottagarens adress för bankkontot som anges på kundens eller leverantörens bankkontokort|  
|Mottagarens adress för bankkontot som anges på kundens eller leverantörens bankkontokort|Stad|Kund bankkonto/Leverantör bankkonto|Mottagarens stad för bankkontot som anges på kundens eller leverantörens bankkontokort|  
|Mottagarbankens namn|Namn|Kund bankkonto/Leverantör bankkonto|Mottagarens namn för bankkontot som anges på kundens eller leverantörens bankkontokort|  
|Mottagarbankens land/region|Lands-/regionkod|Kund bankkonto/Leverantör bankkonto|Mottagarens land/region för bankkontot som anges på kundens eller leverantörens bankkontokort|  
|Mottagarbankens postnr|Postnr|Kund bankkonto/Leverantör bankkonto|Mottagarens postnummer för bankkontot som anges på kundens eller leverantörens bankkontokort|  
|Avsändarbankens adress|Adress|Bankkonto|Den adress för avsändarens bankkonto som anges på bankkontokortet|  
|Avsändarbankens ort|Stad|Bankkonto|Den stad för avsändarens bankkonto som anges på bankkontokortet|  
|Avsändarbankens namn|Namn|Bankkonto|Det namn för avsändarens bankkonto som anges på bankkontokortet|  
|Avsändarbankens land/region|Lands-/regionkod|Bankkonto|Landet/regionen för avsändarens bankkonto som anges på bankkontokortet|  
|Avsändarbankens postnr|Postnr|Bankkonto|Det postnummer för avsändarens bankkonto som anges på bankkontokortet|  
|Redovisningsjournalmall|Mallnamn för journal|Redovisningsjournalrad|Redovisningsjournalens mall som används för betalningsraden|  
|Redovisningsjournalnamn|Journalnamn|Redovisningsjournalrad|Redovisningsjournalens batchnamn som används för betalningsraden|  
|Avsändarbankens namn – datakonv.|Banknamn – datakonvertering|Bankkonto|Avsändarens bankkontonamn som begärs av bankdatakonverteringstjänsten och anges på bankkontokortet|  

## <a name="see-also"></a>Se även  
[Konfigurera datautbyte](across-set-up-data-exchange.md)  
[Utbyta data elektroniskt](across-data-exchange.md)
[Så här konfigurerar du bankdatakonverteringstjänsten](bank-how-setup-bank-data-conversion-service.md)   
[Gör betalningar med tjänsten för bankdatakonvertering eller SEPA Kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   

