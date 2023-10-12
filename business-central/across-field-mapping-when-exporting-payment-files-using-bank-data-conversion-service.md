---
title: Fältmappning för export av bankbetalningsfiler | Microsoft Docs
description: När du exporterar betalningsfiler med hjälp av AMC Banking 365 Fundamentals-tillägget kommer den data du exporterar att visas för tjänsteleverantören.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Fältmappning vid export av betalningsfiler med hjälp av AMC Banking 365 Fundamentals-tillägget
När du exporterar betalningsfiler med hjälp av AMC Banking 365 Fundamentals-tillägget kommer den data du exporterar att visas för tjänsteleverantören. Serviceleverantören är ansvarig för sekretessen för dessa data. Mer information om AMC Banking 365 Fundamentals-tillägget finns i [Använda AMC Banking 365 Fundamentals-tillägget](ui-extensions-amc-banking.md).  

> [!CAUTION]  
>  När du exporterar betalningsfiler med hjälp av AMC Banking 365 Fundamentals-tillägget kommer vissa av dina affärsdata att visas för tjänsteleverantören. Serviceleverantören, AMC Consult A/S, är ansvarig för sekretessen för dessa data. Mer information finns i [Sekretesspolicy för AMC](https://go.microsoft.com/fwlink/?LinkId=510158).  

> [!NOTE]
> I den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)], ställs en global tjänstleverantör in och ansluts för att konvertera bankdata till valfritt filformat som din bank kräver. I Nordamerikanska versioner kan samma service användas för att skicka betalningsfiler som EFT (Elektronisk överföring), t.ex. det ACH-nätverk som ofta används, men med en något annorlunda metod.

I följande tabell visas de fält i [!INCLUDE[prod_short](includes/prod_short.md)] som du kan exportera data från.  

|Mappat fält|Fält i tabell|Bord|Beskrivning|  
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
|Avsändarbankens namn – datakonv.|Banknamn – datakonvertering|Bankkonto|Namnet på sändarens bankkonto som begärs av AMC Banking 365 Fundamentals-tillägget och anges på bankens kontokort|  

## Se även  
[Konfigurera databyte](across-set-up-data-exchange.md)  
[Byta data elektroniskt](across-data-exchange.md)
[Använda AMC Banking 365 Fundamentals-tillägget](ui-extensions-amc-banking.md)   
[Göra betalningar med AMC Banking 365 Fundamentals-tillägg eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]