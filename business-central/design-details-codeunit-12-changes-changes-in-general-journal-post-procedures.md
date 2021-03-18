---
title: Ändringar i bokföringsprocedurer i redovisningsjournalen i Codeunit 12
description: I tidigare versioner ändrades codeunit 12 för att hjälpa till att förbättra prestandan i bokföringen från redovisningsjournalen. Läs om ändringarna i bokföringsprocedurer i den här artikeln.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/28/2020
ms.author: edupont
ms.openlocfilehash: 43232e1c38176bc947d33b5e3f55b7535afbcad4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390555"
---
# <a name="historical-changes-to-codeunit-12-changes-in-general-journal-post-procedures"></a>Tidigare ändringar i Codeunit 12: ändringar i bokföringsprocedurer i redovisningsjournalen

Följande ändringar har implementerats i olika versioner av [!INCLUDE [navnow_md](includes/navnow_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Kommentar**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GetGLReg|GetGLReg|Uppdaterad|  
|RunWithCheck|RunWithCheck|Uppdaterad|  
|RunWithoutCheck|RunWithoutCheck|Uppdaterad|  
|Code|Code|Uppdaterad|  
||PostGenJnlLine|Monterade|  
||InitAmounts|Monterade|  
||InitLastDocDate|Monterade|  
|InitVAT|InitVAT|Uppdaterad|  
|PostVAT|PostVAT|Uppdaterad|  
|InsertVAT|InsertVAT|Uppdaterad|  
|SummarizeVAT|SummarizeVAT|Uppdaterad|  
|InsertSummarizedVAT|InsertSummarizedVAT|Uppdaterad|  
|PostGLAcc|PostGLAcc|Uppdaterad|  
|PostCust|PostCust|Uppdaterad|  
|PostVend|PostVend|Uppdaterad|  
|PostBankAcc|PostBankAcc|Uppdaterad|  
|PostFixedAsset|PostFixedAsset|Uppdaterad|  
|PostICPartner|PostICPartner|Uppdaterad|  
|InitCodeUnit|StartPosting|Uppdaterad|  
||ContinuePosting|Monterade|  
|FinishCodeunit|FinishPosting|Uppdaterad|  
||PostUnrealizedVAT|Monterade|  
||CheckPostUnrealizedVAT|Monterade|  
||ExchangeAccounts|Monterade|  
|InitGLEntry|InitGLEntry|Uppdaterad|  
||InitGLEntryVAT|Monterade|  
||InitGLEntryVATCopy|Monterade|  
|InsertGLEntry|InsertGLEntry|Uppdaterad|  
||CreateGLEntry|Monterade|  
||CreateGLEntryBalAcc|Monterade|  
||CreateGLEntryVAT|Monterade|  
||CreateGLEntryVATCollectAdj|Monterade|  
||CreateGLEntryFromVATEntry|Monterade|  
||UpdateCheckAmounts|Monterade|  
|ApplyCustLedgEntry|ApplyCustLedgEntry|Uppdaterad|  
||CalcPmtDiscPossible|Monterade|  
||CalcPmtTolerancePossible|Monterade|  
|CalcPmtTolerance|CalcPmtTolerance|Uppdaterad|  
|CalcPmtDisc|CalcPmtDisc|Uppdaterad|  
|CalcPmtDiscIfAdjVAT|CalcPmtDiscIfAdjVAT|Uppdaterad|  
|CalcPmtDiscTolerance|CalcPmtDiscTolerance|Uppdaterad|  
||CalcPmtDiscVATBases|Monterade|  
||CalcPmtDiscVATAmounts|Monterade|  
||InsertPmtDiscVATForVATEntry|Monterade|  
||InsertPmtDiscVATForGLEntry|Monterade|  
|CalcCurrencyApplnRounding|CalcCurrencyApplnRounding|Uppdaterad|  
|FindAmtForAppln|FindAmtForAppln|Uppdaterad|  
|CalcCurrencyUnrealizedGainLoss|CalcCurrencyUnrealizedGainLoss|Uppdaterad|  
|CalcCurrencyRealizedGainLoss|CalcCurrencyRealizedGainLoss|Uppdaterad|  
|CalcApplication|CalcApplication|Uppdaterad|  
|CalcRemainingPmtDisc|CalcRemainingPmtDisc|Flyttad till kodmodul 426 – hantering av betalningstolerans|  
|CalcAmtLCYAdjustment|CalcAmtLCYAdjustment|Monterade|  
|InitNewCVLedgEntry|InitFromGenJnlLine|Flyttad till tabell 383 – detaljerad KL resk.trans.buff.|  
|InitOldCVLedgEntry|CopyFromCVLedgEntryBuf|Flyttad till tabell 383 – detaljerad KL resk.trans.buff.|  
|InsertDtldCVLedgEntry|InsertDtldCVLedgEntry|Flyttad till tabell 383 – detaljerad KL resk.trans.buff.|  
||InitBankAccLedgEntry|Monterade|  
||InitCheckLedgEntry|Monterade|  
||InitCustLedgEntry|Monterade|  
||InitVendLedgEntry|Monterade|  
||InsertDtldCustLedgEntry|Monterade|  
||InsertDtldVendLedgEntry|Monterade|  
|CustUnrealizedVAT|CustUnrealizedVAT|Uppdaterad|  
|CustPostApplyCustLedgEntry|CustPostApplyCustLedgEntry|Uppdaterad|  
||PrepareTempCustLedgEntry|Monterade|  
|UnapplyCustLedgEntry|UnapplyCustLedgEntry|Uppdaterad|  
|TransferCustLedgEntry|CopyFromGenJnlLine|Flyttad till tabell 21 – kundreskontra|  
|PostDtldCustLedgEntries|PostDtldCustLedgEntries|Uppdaterad|  
||PostDtldCustLedgEntry|Monterade|  
||PostDtldCustLedgEntryUnapply|Monterade|  
||GetDtldCustLedgEntryAccNo|Monterade|  
|ZeroTransNoDtldCustLedgEntries|SetZeroTransNo|Flyttad till tabell 379 – detaljerad kundresk.trans.|  
|AutoEntrForDtldCustLedgEntries||Omstrukturerad till PostDtldCustLedgEntryUnapply|  
|CustUpdateDebitCredit|UpdateDebitCredit|Flyttad till tabell 379 – detaljerad kundresk.trans.|  
|ApplyVendLedgEntry|ApplyVendLedgEntry|Uppdaterad|  
||PrepareTempVendLedgEntry|Monterade|  
|VendPostApplyVendLedgEntry|VendPostApplyVendLedgEntry|Uppdaterad|  
|UnapplyVendLedgEntry|UnapplyVendLedgEntry|Uppdaterad|  
|TransferVendLedgEntry|CopyFromGenJnlLine|Flyttad till tabell 25 – lev.reskontratransaktion|  
|PostDtldVendLedgEntries|PostDtldVendLedgEntries|Uppdaterad|  
||PostDtldVendLedgEntry|Monterade|  
||PostDtldVendLedgEntryUnapply|Monterade|  
||GetDtldVendLedgEntryAccNo|Monterade|  
||PostDtldCVLedgEntry|Monterade|  
||PostDtldCustVATAdjustment|Monterade|  
||PostDtldVendVATAdjustment|Monterade|  
|ZeroTransNoDtldVendLedgEntries|SetZeroTransNo|Flyttad till tabell 380 – detaljerad lev.resk.trans.|  
|AutoEntrForDtldVendLedgEntries||Omstrukturerad till PostDtldVendLedgEntryUnapply|  
|VendUpdateDebitCredit|UpdateDebitCredit|Flyttad till tabell 380 – detaljerad lev.resk.trans.|  
|VendUnrealizedVAT|VendUnrealizedVAT|Uppdaterad|  
||PostUnrealVATEntry|Monterade|  
||PostApply|Monterade|  
|PostUnrealVATByUnapply|PostUnrealVATByUnapply|Uppdaterad|  
||PostUnapply|Monterade|  
||InsertDtldCustLedgEntryUnapply|Monterade|  
||InsertDtldVendLedgEntryUnapply|Monterade|  
||InsertTempVATEntry|Monterade|  
||ProcessTempVATEntry|Monterade|  
||UpdateCustLedgEntry|Monterade|  
||UpdateVendLedgEntry|Monterade|  
|UpdateCalcInterest|UpdateCalcInterest|Uppdaterad|  
|UpdateCalcInterest2|UpdateCalcInterest2|Uppdaterad|  
|GLCalcAddCurrency|GLCalcAddCurrency|Uppdaterad|  
|HandleAddCurrResidualGLEntry|HandleAddCurrResidualGLEntry|Uppdaterad|  
|CalcLCYToAddCurr|CalcLCYToAddCurr|Uppdaterad|  
|CalcAddCurrFactor||Borttaget|  
|GetCurrencyExchRate|GetCurrencyExchRate|Uppdaterad|  
|ExchAmount|ExchangeAmount|Flyttad till tabell 330 – valutakurs|  
|ExchangeAmtLCYToFCY2|ExchangeAmtLCYToFCY2|Uppdaterad|  
|CalcAddCurrForUnapplication|CalcAddCurrForUnapplication|Uppdaterad|  
|CheckNonAddCurrCodeOccurred|CheckNonAddCurrCodeOccurred|Uppdaterad|  
|CheckCalcPmtDisc||Flyttad till kodmodul 426 – hantering av betalningstolerans|  
|CheckCalcPmtDiscCVCust||Flyttad till kodmodul 426 – hantering av betalningstolerans|  
|CheckCalcPmtDiscCust||Flyttad till kodmodul 426 – hantering av betalningstolerans|  
|CheckCalcPmtDiscGenJnlCust||Flyttad till kodmodul 426 – hantering av betalningstolerans|  
|CheckCalcPmtDiscCVVend||Flyttad till kodmodul 426 – hantering av betalningstolerans|  
|CheckCalcPmtDiscVend||Flyttad till kodmodul 426 – hantering av betalningstolerans|  
|CheckCalcPmtDiscGenJnlVend||Flyttad till kodmodul 426 – hantering av betalningstolerans|  
|Reverse|Reverse|Flyttad till Codeunit 17 Redovisningsjnl – bokför återföring|  
|ReverseCustLedgEntry|ReverseCustLedgEntry|Flyttad till Codeunit 17 Redovisningsjnl – bokför återföring|  
|ReverseVendLedgEntry|ReverseVendLedgEntry|Flyttad till Codeunit 17 Redovisningsjnl – bokför återföring|  
|ReverseBankAccLedgEntry|ReverseBankAccLedgEntry|Flyttad till Codeunit 17 Redovisningsjnl – bokför återföring|  
|ReverseVAT|ReverseVAT|Flyttad till Codeunit 17 Redovisningsjnl – bokför återföring|  
|SetReversalDescription|SetReversalDescription|Flyttad till Codeunit 17 Redovisningsjnl – bokför återföring|  
|ApplyCustLedgEntryByReversal|ApplyCustLedgEntryByReversal|Flyttad till Codeunit 17 Redovisningsjnl – bokför återföring|  
|ApplyVendLedgEntryByReversal|ApplyVendLedgEntryByReversal|Flyttad till Codeunit 17 Redovisningsjnl – bokför återföring|  
|PostPmtDiscountVATByUnapply|PostPmtDiscountVATByUnapply|Flyttad till Codeunit 17 Redovisningsjnl – bokför återföring|  
||CheckDimComb|Tillagt i Codeunit 17 Redovisningsjnl – bokför återföring|  
||CopyCustLedgEntry|Tillagt i Codeunit 17 Redovisningsjnl – bokför återföring|  
||CopyVendLedgEntry|Tillagt i Codeunit 17 Redovisningsjnl – bokför återföring|  
||CopyBankAccLedgEntry|Tillagt i Codeunit 17 Redovisningsjnl – bokför återföring|  
|HandlDtlAddjustment|HandleDtldAdjustment|Uppdaterad|  
|CollectAddjustment|CollectAdjustment|Uppdaterad|  
|SetOverDimErr|SetOverDimErr|Uppdaterad|  
|PostJob|PostJob|Uppdaterad|  
|InsertVATEntriesFromTemp|InsertVATEntriesFromTemp|Uppdaterad|  
|CaptureOrRefundCreditCardPmnt|CaptureOrRefundCreditCardPmnt|Uppdaterad|  
|UpdateDOPaymentTransactEntry|UpdateDOPaymentTransactEntry|Uppdaterad|  
|ABSMin|ABSMin|Uppdaterad|  
|GetApplnRoundPrecision|GetApplnRoundPrecision|Uppdaterad|  
|CheckDimValueForDisposal|CheckDimValueForDisposal|Uppdaterad|  
|CalculateCurrentBalance|CalculateCurrentBalance|Uppdaterad|  
|IncludeVATAmount||Flyttad till tabell 81 journalrad|  
|CalcVATAmountFromVATEntry|CalcVATAmountFromVATEntry|Uppdaterad|  
||TotalVATAmountOnJnlLines|Monterade|  
||SetGLRegReverse|Monterade|  
||GetGLSetup|Monterade|  
||ReadGLSetup|Monterade|  
||CheckSalesExtDocNo|Monterade|  
||CheckPurchExtDocNo|Monterade|  
||CheckGLAccDimError|Monterade|  
||GetCurrency|Monterade|  
||PostDtldAdjustment|Monterade|  
||GetNextEntryNo|Monterade|  
||GetNextTransactionNo|Monterade|  
||GetNextVATEntryNo|Monterade|  
||IncrNextVATEntryNo|Monterade|  
||IsNotPayment|Monterade|  
||IsTempGLEntryBufEmpty|Monterade|  
||IsVATAdjustment|Monterade|  
||IsVATExcluded|Monterade|  
||UpdateDimensions|Monterade|  
||UpdateDimensionsFromCustLedgEntry|Monterade|  
||UpdateDimensionsFromVendLedgEntry|Monterade|  
||UpdateTotalAmounts|Monterade|  
||CreateGLEntriesForTotalAmounts|Monterade|  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Ändringar i kodmodul 12: Mappa globala variabler för bokföring av rad i redovisningsjournalen](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]