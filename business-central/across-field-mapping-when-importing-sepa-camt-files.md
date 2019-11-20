---
title: Fältmappning vid import av SEPA CAMT-filer | Microsoft Docs
description: På europeiska marknader kan du importera bankutdragsfiler i regionala SEPA-standarder (Single Euro Payments Area).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e4c3b60bca16e1f1e72e728d02b07ded11cada09
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692590"
---
# <a name="field-mapping-when-importing-sepa-camt-files"></a>Fältmappning vid import av SEPA CAMT-filer
[!INCLUDE[d365fin](includes/d365fin_md.md)] stöder de regionala SEPA-standardena (Single Euro Payments Area) för import av SEPA-kontoutdrag (CAMT-format). Mer information finns i [Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

 SEPA CAMT-standarden har lokala varianter. Därför kanske du måste ändra den generiska definitionen av datautbytet representeras av koden **SEPA CAMT** på sidan **Definitioner för bokföringsbyte** för att anpassa den till en lokal variation av standarden. Följande tabeller visar element-till-fält-mappning för tabellerna 81, 273 och 274 i SEPA CAMT-implementeringen i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Information om att skapa och justera en dataintegrationsdefinition finns i [Ställa in dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-81"></a>CAMT-datamappning till fält i tabellen Redovisningsjournal (81)  

|Elementsökväg|Meddelandeelement|Datatyp|Beskrivning|Identifierare för negativt tecken|Fältnr|Fältnamn|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Belopp|Decimal|Penningbeloppet för kassatransaktionen||13|Belopp|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Text|Anger om transaktionen är en kreditering- eller debiteringstransaktion|DBIT|13|Belopp|  
|Stmt/Ntry/BookgDt/Dt|Datum|Datum|Datumet när en transaktion bokförs på ett konto i kontoföretagets böcker||5|Bokföringsdatum|  
|Stmt/Ntry/BookgDt/DtTm|Datum/tid|Datum/tid|Datumet och tiden när en transaktion bokförs på ett konto i kontoföretagets böcker||5|Bokföringsdatum|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Namn|Text|Namnet på den part som är skyldig en mängd pengar till (den ultimata) fordringsägaren||1221|Information om betalare|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Ostrukturerat|Text|Information som levereras så att du matcha/stämma av en transaktion med artiklarna som betalningen är avsedd att reglera, till exempel kommersiella fakturor i ett kundreskontrasystem, i en ostrukturerad form||8|Beskrivning|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Text|Ytterligare information om transaktionen||1222|Transaktionsinformation|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273"></a>CAMT-datamappning till fält i tabellen Bankkontoavstämning (273)  

|Elementsökväg|Meddelandeelement|Datatyp|Beskrivning|Identifierare för negativt tecken|Fältnr|Fältnamn|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Datum|Datum och tid när meddelandet skapades||3|Kontoutdragets datum|  
|Stmt/Motkonto/Belopp|Belopp|Decimal|Det belopp som kommer från de nettoberäknade beloppen för alla debet- och kredittransaktioner||4|Kontoutdragets slutsaldo|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274"></a>CAMT-datamappning till fält i tabellen Bankkontoavstämningsrad (274)  

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

 Element i noden **Ntry** som importeras till [!INCLUDE[d365fin](includes/d365fin_md.md)] men inte är kopplade till vissa fält lagras i tabellen **Def.kod för bokföringsbyt** table. Användare kan visa dessa element från **Betalningsavstämningsjournal**, **Betalningskoppling**, och **bankkontoavstämning** genom att välja åtgärden **Information om bankutdragsrad**. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).  
## <a name="see-also"></a>Se även  
[Konfigurera datautbyte](across-set-up-data-exchange.md)  
[Utbyta data elektroniskt](across-data-exchange.md).  
[Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)   
[Använda XML-scheman för att förbereda dataintegreringsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md)  
