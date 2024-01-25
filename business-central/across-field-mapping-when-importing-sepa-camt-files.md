---
title: Fältmappning vid import av SEPA CAMT-filer | Microsoft Docs
description: På europeiska marknader kan du importera bankutdragsfiler i regionala SEPA-standarder (Single Euro Payments Area).
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/06/2023
ms.custom: bap-template
---
# Fältmappning vid import av SEPA CAMT-filer

[!INCLUDE[prod_short](includes/prod_short.md)] stöder de regionala SEPA-standardena (Single Euro Payments Area) för import av SEPA-kontoutdrag (CAMT-format). Mer information finns i [Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

 SEPA CAMT-standarden har lokala varianter. Därför kanske du måste ändra den generiska definitionen av datautbytet representeras av koden **SEPA CAMT** på sidan **Definitioner för bokföringsbyte** för att anpassa den till en lokal variation av standarden. Följande tabeller visar element-till-fält-mappning för tabellerna 81, 273 och 274 i SEPA CAMT-implementeringen i [!INCLUDE[prod_short](includes/prod_short.md)].  

 Information om att skapa och justera en dataintegreringsdefinition finns i [Ställa in dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

## CAMT-datamappning till fält i tabellen Redovisningsjournal (81)  

|Elementsökväg|Meddelandeelement|Datatyp|Beskrivning|Identifierare för negativt tecken|Fältnr|Fältnamn|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Belopp|Decimal|Penningbeloppet för kassatransaktionen||13|Belopp|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Text|Anger om transaktionen är en kreditering- eller debiteringstransaktion|DBIT|13|Belopp|  
|Stmt/Ntry/BookgDt/Dt|Datum|Datum|Datumet när en transaktion bokförs på ett konto i kontoföretagets böcker||5|Bokföringsdatum|  
|Stmt/Ntry/BookgDt/DtTm|Datum/tid|Datum/tid|Datumet och tiden när en transaktion bokförs på ett konto i kontoföretagets böcker||5|Bokföringsdatum|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Namn|Text|Namnet på den part som är skyldig en mängd pengar till (den ultimata) fordringsägaren||1221|Information om betalare|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Ostrukturerat|Text|Information som levereras så att du matcha/stämma av en transaktion med artiklarna som betalningen är avsedd att reglera, till exempel kommersiella fakturor i ett kundreskontrasystem, i en ostrukturerad form||8|Beskrivning|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Text|Ytterligare information om transaktionen||1222|Transaktionsinformation|  

## CAMT-datamappning till fält i tabellen Bankkontoavstämning (273)  

|Elementsökväg|Meddelandeelement|Datatyp|Beskrivning|Identifierare för negativt tecken|Fältnr|Fältnamn|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Datum|Datum och tid när meddelandet skapades||3|Kontoutdragets datum|  
|Stmt/Motkonto/Belopp|Belopp|Decimal|Det belopp som kommer från de nettoberäknade beloppen för alla debet- och kredittransaktioner||4|Kontoutdragets slutsaldo|  

## CAMT-datamappning till fält i tabellen Bankkontoavstämningsrad (274)  

|Elementsökväg|Meddelandeelement|Datatyp|Beskrivning|Identifierare för negativt tecken|Fältnr|Fältnamn|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Belopp|Decimal|Penningbeloppet för kassatransaktionen||7|Transaktionsbelopp|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Text|Anger om transaktionen är en kreditering- eller debiteringstransaktion|DBIT|7|Transaktionsbelopp|  
|Stmt/Ntry/BookgDt/Dt|Datum|Datum|Datumet när en transaktion bokförs på ett konto i kontoföretagets böcker||5|Bokföringsdatum|  
|Stmt/Ntry/BookgDt/DtTm|Datum/tid|Datum/tid|Datumet och tiden när en transaktion bokförs på ett konto i kontoföretagets böcker||5|Bokföringsdatum|  
|Stmt/Ntry/ValDt/Dt|Datum|Datum|Datumet när anläggningstillgångar blir tillgängliga för kontoägaren i händelse av en kredittransaktion, eller upphör att vara tillgängliga för kontoägaren i händelse av en debettransaktion||12|Valuteringsdag|  
|Stmt/Ntry/ValDt/DtTm|Datum/tid|Datum/tid|Datumet och tiden när anläggningstillgångar blir tillgängliga för kontoägaren i händelse av en kredittransaktion, eller upphör att vara tillgängliga för kontoägaren i händelse av en debettransaktion||12|Valuteringsdag|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Namn|Text|Namnet på den part som är skyldig en mängd pengar till (den ultimata) fordringsägaren||15|Information om betalare|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Ostrukturerat|Text|Information som levereras så att du matcha/stämma av en transaktion med artiklarna som betalningen är avsedd att reglera, till exempel kommersiella fakturor i ett kundreskontrasystem, i en ostrukturerad form||6|Beskrivning|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Text|Ytterligare information om transaktionen||16|Transaktionsinformation|  

 Element i noden **Ntry** som importeras till [!INCLUDE[prod_short](includes/prod_short.md)] men inte är kopplade till vissa fält lagras i tabellen **Def.kod för bokföringsbyt** table. Användare kan visa dessa element från **Betalningsavstämningsjournal**, **Betalningskoppling**, och **bankkontoavstämning** genom att välja åtgärden **Information om bankutdragsrad**. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]
> Vid import av CAMT-kontoutdrag [!INCLUDE[prod_short](includes/prod_short.md)] måste varje transaktion vara unik, vilket innebär att fältet **Transaktions-ID** som kommer från taggen *Stmt/Ntry/NtryDtls/TxDtls/ReFS/EndToEndId* i CAMT-filen måste vara unikt i den öppna bankkontoavstämningen. Om informationen inte finns ignorerar [!INCLUDE[prod_short](includes/prod_short.md)] betalningen. Om en tidigare bankavstämning på samma bankkonto bokfördes med samma transaktions-ID som för den aktuella importen, kommer den aktuella transaktionen inte att stämmas av automatiskt, men den kan fortfarande importeras.

## Se även  

[Konfigurera dataintegration](across-set-up-data-exchange.md)  
[Utbyta data elektroniskt](across-data-exchange.md)  
[Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Använda XML-uppställningar för att förbereda datautbytesdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]