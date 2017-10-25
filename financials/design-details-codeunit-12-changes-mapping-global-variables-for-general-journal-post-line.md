---
title: "Designdetaljer: Ändringar i kodmodul 12: Mappa globala variabler för bokföring av rad i redovisningsjournalen | Microsoft Docs"
description: "Följande ändringar har införts i den här versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)]."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f2c15ecfe98bbbbb8154f46032201221ca32e32e
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="codeunit-12-changes-mapping-global-variables-for-general-journal-post-line"></a>Ändringar i kodmodul 12: Mappa globala variabler för bokföring av rad i redovisningsjournalen
Följande ändringar har genomförts i den här versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Kommentar**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Post 98;|GLSetup@1009 : Post 98;|Oförändrat|  
|SalesSetup@1010 : Post 311;||Ändrad till lokal|  
|PurchSetup@1011 : Post 312;||Ändrad till lokal|  
|AccountingPeriod@1012 : Post 50;||Ändrad till lokal|  
|GLAcc@1013 : Post 15;||Ändrad till lokal|  
|GLEntry@1014 : Post 17;|GlobalGLEntry@1014 : Post 17;|Namnet har bytts|  
|GLEntryTmp@1015: TEMPORÄR post 17;|TempGLEntryBuf@1010: TEMPORÄR post 17;|Namnet har bytts|  
|TempGLEntryVAT@1016: TEMPORÄR post 17;|TempGLEntryVAT@1016: TEMPORÄR post 17;|Oförändrat|  
|OrigGLEntry@1017 : Post 17;||Borttaget|  
|VATPostingSetup@1019 : Post 325;||Ändrad till lokal|  
|Cust@1020 : Post 18;||Ändrad till lokal|  
|Vend@1021 : Post 23;||Ändrad till lokal|  
|GenJnlLine@1022 : Post 81;||Ändrad till lokal|  
|GLReg@1029 : Post 45;|GLReg@1029 : Post 45;|Oförändrat|  
|CustPostingGr@1030 : Post 92;||Ändrad till lokal|  
|VendPostingGr@1031 : Post 93;||Ändrad till lokal|  
|Currency@1032 : Post 4;||Ändrad till lokal|  
|AddCurrency@1033 : Post 4;|AddCurrency@1033 : Post 4;|Oförändrat|  
|ApplnCurrency@1034 : Post 4;||Ändrad till lokal|  
|CurrExchRate@1035 : Post 330;|CurrExchRate@1035 : Post 330;|Oförändrat|  
|VATEntry@1038 : Post 254;|VATEntry@1038 : Post 254;|Oförändrat|  
|BankAcc@1039 : Post 270;||Ändrad till lokal|  
|BankAccLedgEntry@1040 : Post 271;||Ändrad till lokal|  
|CheckLedgEntry@1041 : Post 272;||Ändrad till lokal|  
|CheckLedgEntry2@1042 : Post 272;||Ändrad till lokal|  
|BankAccPostingGr@1043 : Post 277;||Ändrad till lokal|  
|GenJnlTemplate@1044 : Post 80;||Ändrad till lokal|  
|TaxJurisdiction@1045 : Post 320;||Ändrad till lokal|  
|TaxDetail@1046 : Post 322;|TaxDetail@1046 : Post 322;|Oförändrat|  
|FAGLPostBuf@1047: TEMPORÄR post 5637;||Ändrad till lokal|  
|UnrealizedCustLedgEntry@1084 : Post 21;|UnrealizedCustLedgEntry@1084 : Post 21;|Oförändrat|  
|UnrealizedVendLedgEntry@1085 : Post 25;|UnrealizedVendLedgEntry@1085 : Post 25;|Oförändrat|  
|GLEntryVATEntryLink@1087 : Post 253;|GLEntryVATEntryLink@1087 : Post 253;|Oförändrat|  
|TempVATEntry@1088: TEMPORÄR post 254;|TempVATEntry@1088: TEMPORÄR post 254;|Oförändrat|  
|ReversedGLEntryTemp@1089: TEMPORÄR post 17;||Flyttad till Codeunit17|  
|CostAccSetup@1092 : Post 1108;||Ändrad till lokal|  
|GenJnlCheckLine@1048 : Kodmodul 11;|GenJnlCheckLine@1001 : Kodmodul 11;|Oförändrat|  
|ExchAccGLJnlLine@1049 : Kodmodul 366;||Ändrad till lokal|  
|FAJnlPostLine@1050 : Kodmodul 5632;||Ändrad till lokal|  
|SalesTaxCalculate@1051 : Kodmodul 398;||Ändrad till lokal|  
|GenJnlApply@1052 : Kodmodul 225;||Ändrad till lokal|  
|DimMgt@1053 : Kodmodul 408;||Ändrad till lokal|  
|JobPostLine@1028 : Kodmodul 1001;||Ändrad till lokal|  
|TransferGlEntriesToCA@1091 : Kodmodul 1105;||Ändrad till lokal|  
||PaymentToleranceMgt@1002 : Kodmodul 426;|Monterade|  
||AddCurrencyCode@1117 : Kod[10];|Monterade|  
|FiscalYearStartDate@1054 : Datum;|FiscalYearStartDate@1011 : Datum;|Oförändrat|  
|NextEntryNo@1055 : Heltal;|NextEntryNo@1022 : Heltal;|Oförändrat|  
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
|NextVATEntryNo@1064 : Heltal;|NextVATEntryNo@1064 : Heltal;|Oförändrat|  
|FirstNewVATEntryNo@1065 : Heltal;|FirstNewVATEntryNo@1065 : Heltal;|Oförändrat|  
|NextTransactionNo@1066 : Heltal;|NextTransactionNo@1066 : Heltal;|Oförändrat|  
|NextConnectionNo@1067 : Heltal;|NextConnectionNo@1067 : Heltal;|Oförändrat|  
|InsertedTempGLEntryVAT@1068 : Heltal;|InsertedTempGLEntryVAT@1027 : Heltal;|Oförändrat|  
|LastDocNo@1069 : Kod[20];|LastDocNo@1023 : Kod[20];|Oförändrat|  
|LastLineNo@1070 : Heltal;||Borttaget|  
|LastDate@1071 : Datum;|LastDate@1021 : Datum;|Oförändrat|  
|LastDocType@1072: faktura, betalning, kreditnota, räntefaktura eller betalningspåminnelse.|LastDocType@1025: faktura, betalning, kreditnota, räntefaktura eller betalningspåminnelse.|Oförändrat|  
|NextCheckEntryNo@1073 : Heltal;|NextCheckEntryNo@1028 : Heltal;|Oförändrat|  
|AddCurrGLEntryVATAmt@1075 : Decimal;|AddCurrGLEntryVATAmt@1017 : Decimal;|Oförändrat|  
|CurrencyDate@1076 : Datum;|CurrencyDate@1020 : Datum;|Oförändrat|  
|CurrencyFactor@1077 : Decimal;|CurrencyFactor@1019 : Decimal;|Oförändrat|  
|UseCurrFactorOnly@1078 : Booelskt;|UseCurrFactorOnly@1078 : Booelskt;|Oförändrat|  
|NonAddCurrCodeOccured@1079 : Booelskt;|NonAddCurrCodeOccured@1079 : Booelskt;|Oförändrat|  
|FADimAlreadyChecked@1080 : Booelskt;|FADimAlreadyChecked@1080 : Booelskt;|Oförändrat|  
|AllApplied@1081 : Booelskt;||Ändrad till lokal|  
|OverrideDimErr@1018 : Booelskt;|OverrideDimErr@1018 : Booelskt;|Oförändrat|  
|JobLine@1036 : Booelskt;|JobLine@1036 : Booelskt;|Oförändrat|  
|Prepayment@1037 : Booelskt;||Borttaget|  
|CheckUnrealizedCust@1082 : Booelskt;|CheckUnrealizedCust@1082 : Booelskt;|Oförändrat|  
|CheckUnrealizedVend@1083 : Booelskt;|CheckUnrealizedVend@1083 : Booelskt;|Oförändrat|  
|GLEntryNo@1090 : Heltal;|GLEntryNo@1026 : Heltal;|Oförändrat|  
||GLSetupRead@1015 : Booelskt;|Monterade|  
||AmountRoundingPrecision@1012 : Decimal;|Monterade|  
||CrCardTransactionEntryNo@1013 : Heltal;|Monterade|  

## <a name="see-also"></a>Se även  
 [Designdetaljer - Ändringar i kodmodul 12: ändringar i bokföringsprocedurer i redovisningsjournalen](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)

