---
title: Förändringar i mappning av globala variabler för bokföring i Codeunit 12
description: I tidigare versioner ändrades codeunit 12 för att hjälpa till att förbättra prestandan i bokföringen från redovisningsjournalen. Läs om ändringarna i de globala variablerna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/28/2020
ms.author: edupont
ms.openlocfilehash: 0fc79ba982e17b9295f0f611ca34b4eb615001f3
ms.sourcegitcommit: a95681db16e81af109b34f8e5d88028c1552c6a2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367765"
---
# <a name="historical-changes-to-codeunit-12-mapping-global-variables-for-general-journal-post-line"></a>Historiska ändringar i Codeunit 12: Mappa globala variabler för bokföringsrad i redovisningsjournal

Följande ändringar har implementerats i olika versioner av [!INCLUDE [navnow_md](includes/navnow_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Kommentar**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Record 98;|GLSetup@1009 : Record 98;|Oförändrat|  
|SalesSetup@1010 : Record 311;||Ändrad till lokal|  
|PurchSetup@1011 : Record 312;||Ändrad till lokal|  
|AccountingPeriod@1012 : Record 50;||Ändrad till lokal|  
|GLAcc@1013 : Record 15;||Ändrad till lokal|  
|GLEntry@1014 : Record 17;|GlobalGLEntry@1014 : Record 17;|Namnet har bytts|  
|GLEntryTmp@1015 : TEMPORARY Record 17;|TempGLEntryBuf@1010 : TEMPORARY Record 17;|Namnet har bytts|  
|TempGLEntryVAT@1016 : TEMPORARY Record 17;|TempGLEntryVAT@1016 : TEMPORARY Record 17;|Oförändrat|  
|OrigGLEntry@1017 : Record 17;||Borttaget|  
|VATPostingSetup@1019 : Record 325;||Ändrad till lokal|  
|Cust@1020 : Record 18;||Ändrad till lokal|  
|Vend@1021 : Record 23;||Ändrad till lokal|  
|GenJnlLine@1022 : Record 81;||Ändrad till lokal|  
|GLReg@1029 : Record 45;|GLReg@1029 : Record 45;|Oförändrat|  
|CustPostingGr@1030 : Record 92;||Ändrad till lokal|  
|VendPostingGr@1031 : Record 93;||Ändrad till lokal|  
|Currency@1032 : Record 4;||Ändrad till lokal|  
|AddCurrency@1033 : Record 4;|AddCurrency@1033 : Record 4;|Oförändrat|  
|ApplnCurrency@1034 : Record 4;||Ändrad till lokal|  
|CurrExchRate@1035 : Record 330;|CurrExchRate@1035 : Record 330;|Oförändrat|  
|VATEntry@1038 : Record 254;|VATEntry@1038 : Record 254;|Oförändrat|  
|BankAcc@1039 : Record 270;||Ändrad till lokal|  
|BankAccLedgEntry@1040 : Record 271;||Ändrad till lokal|  
|CheckLedgEntry@1041 : Record 272;||Ändrad till lokal|  
|CheckLedgEntry2@1042 : Record 272;||Ändrad till lokal|  
|BankAccPostingGr@1043 : Record 277;||Ändrad till lokal|  
|GenJnlTemplate@1044 : Record 80;||Ändrad till lokal|  
|TaxJurisdiction@1045 : Record 320;||Ändrad till lokal|  
|TaxDetail@1046 : Record 322;|TaxDetail@1046 : Record 322;|Oförändrat|  
|FAGLPostBuf@1047 : TEMPORARY Record 5637;||Ändrad till lokal|  
|UnrealizedCustLedgEntry@1084 : Record 21;|UnrealizedCustLedgEntry@1084 : Record 21;|Oförändrat|  
|UnrealizedVendLedgEntry@1085 : Record 25;|UnrealizedVendLedgEntry@1085 : Record 25;|Oförändrat|  
|GLEntryVATEntryLink@1087 : Record 253;|GLEntryVATEntryLink@1087 : Record 253;|Oförändrat|  
|TempVATEntry@1088 : TEMPORARY Record 254;|TempVATEntry@1088 : TEMPORARY Record 254;|Oförändrat|  
|ReversedGLEntryTemp@1089 : TEMPORARY Record 17;||Flyttad till Codeunit17|  
|CostAccSetup@1092 : Record 1108;||Ändrad till lokal|  
|GenJnlCheckLine@1048 : Codeunit 11;|GenJnlCheckLine@1001 : Codeunit 11;|Oförändrat|  
|ExchAccGLJnlLine@1049 : Codeunit 366;||Ändrad till lokal|  
|FAJnlPostLine@1050 : Codeunit 5632;||Ändrad till lokal|  
|SalesTaxCalculate@1051 : Codeunit 398;||Ändrad till lokal|  
|GenJnlApply@1052 : Codeunit 225;||Ändrad till lokal|  
|DimMgt@1053 : Codeunit 408;||Ändrad till lokal|  
|JobPostLine@1028 : Codeunit 1001;||Ändrad till lokal|  
|TransferGlEntriesToCA@1091 : Codeunit 1105;||Ändrad till lokal|  
||PaymentToleranceMgt@1002 : Codeunit 426;|Monterade|  
||AddCurrencyCode@1117 : Code[10];|Monterade|  
|FiscalYearStartDate@1054 : Date;|FiscalYearStartDate@1011 : Date;|Oförändrat|  
|NextEntryNo@1055 : Integer;|NextEntryNo@1022 : Integer;|Oförändrat|  
|BalanceCheckAmount@1056 : Decimal;|BalanceCheckAmount@1056 : Decimal;|Oförändrat|  
|BalanceCheckAmount2@1057 : Decimal;|BalanceCheckAmount2@1057 : Decimal;|Oförändrat|  
|BalanceCheckAddCurrAmount@1058 : Decimal;|BalanceCheckAddCurrAmount@1058 : Decimal;|Oförändrat|  
|BalanceCheckAddCurrAmount2@1059 : Decimal;|BalanceCheckAddCurrAmount2@1059 : Decimal;|Oförändrat|  
|CurrentBalance@1060 : Decimal;|CurrentBalance@1060 : Decimal;|Oförändrat|  
|SalesTaxBaseAmount@1061 : Decimal;||Ändrad till lokal|  
|TotalAddCurrAmount@1062 : Decimal;|TotalAddCurrAmount@1062 : Decimal;|Oförändrat|  
|TotalAmount@1063 : Decimal;|TotalAmount@1063 : Decimal;|Oförändrat|  
|UnrealizedRemainingAmountCust@1086 : Decimal;|UnrealizedRemainingAmountCust@1086 : Decimal;|Oförändrat|  
|UnrealizedRemainingAmountVend@1074 : Decimal;|UnrealizedRemainingAmountVend@1074 : Decimal;|Oförändrat|  
|NextVATEntryNo@1064 : Integer;|NextVATEntryNo@1064 : Integer;|Oförändrat|  
|FirstNewVATEntryNo@1065 : Integer;|FirstNewVATEntryNo@1065 : Integer;|Oförändrat|  
|NextTransactionNo@1066 : Integer;|NextTransactionNo@1066 : Integer;|Oförändrat|  
|NextConnectionNo@1067 : Integer;|NextConnectionNo@1067 : Integer;|Oförändrat|  
|InsertedTempGLEntryVAT@1068 : Integer;|InsertedTempGLEntryVAT@1027 : Integer;|Oförändrat|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Oförändrat|  
|LastLineNo@1070 : Integer;||Borttaget|  
|LastDate@1071 : Date;|LastDate@1021 : Date;|Oförändrat|  
|LastDocType@1072 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|LastDocType@1025 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|Oförändrat|  
|NextCheckEntryNo@1073 : Integer;|NextCheckEntryNo@1028 : Integer;|Oförändrat|  
|AddCurrGLEntryVATAmt@1075 : Decimal;|AddCurrGLEntryVATAmt@1017 : Decimal;|Oförändrat|  
|CurrencyDate@1076 : Date;|CurrencyDate@1020 : Date;|Oförändrat|  
|CurrencyFactor@1077 : Decimal;|CurrencyFactor@1019 : Decimal;|Oförändrat|  
|UseCurrFactorOnly@1078 : Boolean;|UseCurrFactorOnly@1078 : Boolean;|Oförändrat|  
|NonAddCurrCodeOccured@1079 : Boolean;|NonAddCurrCodeOccured@1079 : Boolean;|Oförändrat|  
|FADimAlreadyChecked@1080 : Boolean;|FADimAlreadyChecked@1080 : Boolean;|Oförändrat|  
|AllApplied@1081 : Boolean;||Ändrad till lokal|  
|OverrideDimErr@1018 : Boolean;|OverrideDimErr@1018 : Boolean;|Oförändrat|  
|JobLine@1036 : Boolean;|JobLine@1036 : Boolean;|Oförändrat|  
|Prepayment@1037 : Boolean;||Borttaget|  
|CheckUnrealizedCust@1082 : Boolean;|CheckUnrealizedCust@1082 : Boolean;|Oförändrat|  
|CheckUnrealizedVend@1083 : Boolean;|CheckUnrealizedVend@1083 : Boolean;|Oförändrat|  
|GLEntryNo@1090 : Integer;|GLEntryNo@1026 : Integer;|Oförändrat|  
||GLSetupRead@1015 : Boolean;|Monterade|  
||AmountRoundingPrecision@1012 : Decimal;|Monterade|  
||CrCardTransactionEntryNo@1013 : Integer;|Monterade|  

## <a name="see-also"></a>Se även  
 [Designdetaljer – Ändringar i kodmodul 12: ändringar i bokföringsprocedurer i redovisningsjournalen](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]