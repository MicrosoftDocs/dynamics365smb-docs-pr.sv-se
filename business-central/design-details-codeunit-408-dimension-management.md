---
title: Designdetaljer - Kodenhet 408 Dimension Management | Microsoft Docs
description: "Kodenhet 408 DimensionManagement är ett funktionsbibliotek som hanterar gemensamma uppgifter som är kopplade till dimensioner, till exempel kopiering från en tabell till en annan eller från ett dokument till ett annat."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 34d4314357aa590304885585016124100ead4ca3
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-codeunit-408-dimension-management"></a>Designdetaljer: Kodenhet 408 Dimension Management
Kodenhet 408 DimensionManagement är ett funktionsbibliotek som hanterar gemensamma uppgifter som är kopplade till dimensioner, till exempel kopiering från en tabell till en annan eller från ett dokument till ett annat. I det här avsnittet beskrivs funktionerna som har ändrats i Microsoft Dynamics NAV 2013 R2 vad som måste göras i funktionerna. Många operationer tas bort, eftersom det inte finns något behov av att kopiera mellan dimensionstabeller.  

## <a name="modified-functions"></a>Ändrade funktioner  

|Funktionsnamn|Ändringsbeskrivning|  
|-------------------|------------------------------|  
|CheckDimSetIDComb|Nya funktion som ersätter övriga kontrollfunktioner och tar emot ett dimensionsuppsättnings-ID som ett argument istället för en dimensionstabell.|  
|CheckDimSetIDComb<br /><br /> CheckDocDimComb<br /><br /> CheckServContractDimComb<br /><br /> CheckDimBuffer<br /><br /> CheckDimComb<br /><br /> CheckDimValueComb|Ta bort. All förbrukning ska ändras till CheckDimSetIDComb.|  
|GetDefaultDim|Ändra för att returnera en heltaldimensionsuppsättnings-ID istället för en uppsättning poster.|  
|CopyJnlLineDimToICJnlDim<br /><br /> CopyICJnlDimToJnlLineDim<br /><br /> CopyDocDimtoICDocDim<br /><br /> CopyICDocDimtoICDocDim|Ändra för att arbeta med DimSetID - > ICJnlLineDim|  

## <a name="deleted-functions"></a>Borttagna funktioner  
 Funktioner som tagits bort från kodmodul 408 i samband med funktionen Dimensionsuppsättningstransaktioner anges nedan.  

> [!CAUTION]  
>  Under uppgraderingen av programkoden från Microsoft Dynamics NAV 2009 eller tidigare versioner till Microsoft Dynamics NAV 2016, är följande funktioner inte tillgängliga i Microsoft Dynamics NAV 2016. Om du har anpassningar som använder en eller flera av funktionerna måste du uppgradera koden därefter.

 InsertJnlLineDim  

 UpdateJnlLineDefaultDim  

 GetJnlLineDefaultDim  

 GetPreviousDocDefaultDim  

 GetPreviousProdDocDefaultDim  

 InsertDocDim  

 UpdateDocDefaultDim  

 ExtractDocDefaultDim  

 InsertProdDocDim  

 UpdateProdDocDefaultDim  

 InsertServContractDim  

 UpdateServcontractDim  

 UpdateDefaultDimNewDimValue  

 GetDocDim  

 GetProdDocDim  

 TypeToTableID1  

 TypeToTableID2  

 TypeToTableID3  

 TypeToTableID4  

 TypeToTableID5  

 DeleteJnlLineDim  

 DeleteDocDim  

 DeletePostedDocDim  

 DeleteProdDocDim  

 DeleteServContractDim  

 ShowJnlLineDim  

 SaveJnlLineDim  

 ShowJnlLineNewDim  

 SaveJnlLineNewDim  

 ShowDocDim  

 SaveDocDim  

 ShowProdDocDim  

 SaveProdDocDim  

 ShowTempDim  

 SaveTempDim  

 ShowTempNewDim  

 SaveTempNewDim  

 SaveServContractDim  

 MoveJnlLineDimToLedgEntryDim  

 MoveDocDimToPostedDocDim  

 MoveOneDocDimToPostedDocDim  

 MoveLedgEntryDimToJnlLineDim  

 MoveDimBufToJnlLineDim  

 MoveDimBufToLedgEntryDim  

 MoveDimBufToPostedDocDim  

 MoveDimBufToGLBudgetDim  

 CopyJnlLineDimToJnlLineDim  

 CopyLedgEntryDimToJnlLineDim  

 CopyDocDimToDocDim  

 CopyPostedDocDimToPostedDocDim  

 CopyDocDimToJnlLineDim  

 CopyDimBufToJnlLineDim  

 CopyDimBufToDocDim  

 CopySCDimToDocDim  

 MoveDocDimToLedgEntryDim  

 MoveDocDimToDocDim  

 MoveDocDimArchvToDocDim  

 MoveLedgEntryDimToDocDim  

 MoveProdDocDimToProdDocDim  

 MoveJnlLineDimToProdDocDim  

 MoveJnlLineDimToDocDim  

 MoveJnlLineDimToJnlLineDim  

 CopyLedgEntryDimToLedgEntryDim  

 MoveTempFromDimToTempToDim  

 TransferTempToDimToDocDim  

 MoveJnlLineDimToBuf  

 CopyICJnlDimToICJnlDim  

 TestDimValue  

 TestNewDimValue  

 MoveDimBufToItemBudgetDim. (Ta bort eftersom tabellen ItemBudgetDim har tagits bort.)  

 GetServContractDim  

 MoveTempDimToBuf  

 UpdateSCInvLineDim  

 CopyJnlLineDimToBuffer  

 UpdateDocDefaultDim2  

## <a name="see-also"></a>Se även
 [Designdetaljer: Dimensionsuppsättningstransaktioner](design-details-dimension-set-entries.md)   
 [Designdetaljer: Översikt över dimensionsuppsättningstransaktioner](design-details-dimension-set-entries-overview.md)   
 [Designdetaljer: Söka efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md)   
 [Designdetaljer: Tabellstruktur](design-details-table-structure.md)   
 [Designdetaljer: Kodexempel på ändrade mönster i ändringar](design-details-code-examples-of-changed-patterns-in-modifications.md)

