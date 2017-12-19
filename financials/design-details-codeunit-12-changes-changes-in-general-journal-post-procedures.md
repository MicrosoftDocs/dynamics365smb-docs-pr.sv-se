---
title: "Designdetaljer - Ändringar i kodmodul 12: ändringar i bokföringsprocedurer i redovisningsjournalen | Microsoft Docs"
description: "Följande ändringar har genomförts i den här versionen av Dynamics 365."
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
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: a320e0acbe75c98db525c0dc94edd8c39253d97c
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="codeunit-12-changes-changes-in-general-journal-post-procedures"></a>Ändringar i kodmodul 12: ändringar i bokföringsprocedurer i redovisningsjournalen
Följande ändringar har genomförts i den här versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)].  

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
|Reverse|Reverse|Flyttad till kodmodul 17 Redovisningsjnl – bokför återföring|  
|ReverseCustLedgEntry|ReverseCustLedgEntry|Flyttad till kodmodul 17 Redovisningsjnl – bokför återföring|  
|ReverseVendLedgEntry|ReverseVendLedgEntry|Flyttad till kodmodul 17 Redovisningsjnl – bokför återföring|  
|ReverseBankAccLedgEntry|ReverseBankAccLedgEntry|Flyttad till kodmodul 17 Redovisningsjnl – bokför återföring|  
|ReverseVAT|ReverseVAT|Flyttad till kodmodul 17 Redovisningsjnl – bokför återföring|  
|SetReversalDescription|SetReversalDescription|Flyttad till kodmodul 17 Redovisningsjnl – bokför återföring|  
|ApplyCustLedgEntryByReversal|ApplyCustLedgEntryByReversal|Flyttad till kodmodul 17 Redovisningsjnl – bokför återföring|  
|ApplyVendLedgEntryByReversal|ApplyVendLedgEntryByReversal|Flyttad till kodmodul 17 Redovisningsjnl – bokför återföring|  
|PostPmtDiscountVATByUnapply|PostPmtDiscountVATByUnapply|Flyttad till kodmodul 17 Redovisningsjnl – bokför återföring|  
||CheckDimComb|Tillagd i kodmodul 17 Redovisningsjnl – bokför återföring|  
||CopyCustLedgEntry|Tillagd i kodmodul 17 Redovisningsjnl – bokför återföring|  
||CopyVendLedgEntry|Tillagd i kodmodul 17 Redovisningsjnl – bokför återföring|  
||CopyBankAccLedgEntry|Tillagd i kodmodul 17 Redovisningsjnl – bokför återföring|  
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
|IncludeVATAmount||Flyttad till tabell 81 – redovisningsjournalrad|  
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

