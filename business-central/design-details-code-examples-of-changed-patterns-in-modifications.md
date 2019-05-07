---
title: Designinformation - Kodexempel på förändrade mönster i ändringar | Microsoft-dokument
description: Kodexempel som anger förändrade mönster i dimensionskodsändring och -migrering för fem olika scenarier. Detta jämför kodexemplen i tidigare versioner med kodexemplen i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-dimension-set-entries
ms.openlocfilehash: 5bb5e5713ed23877006ebb913e01416feac69266
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "915653"
---
# <a name="design-details-code-examples-of-changed-patterns-in-modifications"></a><span data-ttu-id="7ce12-104">Designdetaljer: Kodexempel på ändrade mönster i ändringar</span><span class="sxs-lookup"><span data-stu-id="7ce12-104">Design Details: Code Examples of Changed Patterns in Modifications</span></span>
<span data-ttu-id="7ce12-105">Det här avsnittet innehåller kodexempel för att visa ändrade mönster i dimensionskodändring och flytt för fem olika scenarier.</span><span class="sxs-lookup"><span data-stu-id="7ce12-105">This topic provides code examples to show changed patterns in dimension code modification and migration for five different scenarios.</span></span> <span data-ttu-id="7ce12-106">Detta jämför kodexemplen i tidigare versioner med kodexemplen i Business Central.</span><span class="sxs-lookup"><span data-stu-id="7ce12-106">It compares the code examples in earlier versions to the code examples in Business Central.</span></span>

## <a name="posting-a-journal-line"></a><span data-ttu-id="7ce12-107">Bokför en journalrad</span><span class="sxs-lookup"><span data-stu-id="7ce12-107">Posting a Journal Line</span></span>  
<span data-ttu-id="7ce12-108">Viktiga ändringar är följande:</span><span class="sxs-lookup"><span data-stu-id="7ce12-108">Key changes are listed as follows:</span></span>  

- <span data-ttu-id="7ce12-109">Dimensionstabeller för journalrader tas bort.</span><span class="sxs-lookup"><span data-stu-id="7ce12-109">Journal line dimension tables are removed.</span></span>  

- <span data-ttu-id="7ce12-110">Ett dimensionsuppsättning-ID skapas i fältet **Dimensionsuppsättnings-ID**.</span><span class="sxs-lookup"><span data-stu-id="7ce12-110">A dimension set ID is created in the **Dimension Set ID** field.</span></span>  

<span data-ttu-id="7ce12-111">**Tidigare versioner**</span><span class="sxs-lookup"><span data-stu-id="7ce12-111">**Earlier Versions**</span></span>  

```  
ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  

TempJnlLineDim.DELETEALL;  
TempDocDim.RESET;  
TempDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Line");  
TempDocDim.SETRANGE(  
  "Line No.",SalesLine."Line No.");  
DimMgt.CopyDocDimToJnlLineDim(  
  TempDocDim,TempJnlLineDim);  
ResJnlPostLine.RunWithCheck(  
  ResJnlLine,TempJnlLineDim);  

```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  

ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  

ResJnlLine."Dimension Set ID" :=   
  SalesLine." Dimension Set ID ";  
ResJnlPostLine.Run(ResJnlLine);  

```  

## <a name="posting-a-document"></a><span data-ttu-id="7ce12-112">Bokför ett dokument</span><span class="sxs-lookup"><span data-stu-id="7ce12-112">Posting a Document</span></span>  
 <span data-ttu-id="7ce12-113">När du bokför ett dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)] behöver du inte längre kopiera dokumentets dimensioner.</span><span class="sxs-lookup"><span data-stu-id="7ce12-113">When you post a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you no longer have to copy the document dimensions.</span></span>  

 <span data-ttu-id="7ce12-114">**Tidigare versioner**</span><span class="sxs-lookup"><span data-stu-id="7ce12-114">**Earlier Versions**</span></span>  

```  
DimMgt.MoveOneDocDimToPostedDocDim(  
  TempDocDim,DATABASE::"Sales Line",  
  "Document Type",  
  "No.",  
  SalesShptLine."Line No.",  
  DATABASE::"Sales Shipment Line",  
  SalesShptHeader."No.");  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
SalesShptLine."Dimension Set ID”  
  := SalesLine."Dimension Set ID”  
```  

## <a name="editing-dimensions-from-a-document"></a><span data-ttu-id="7ce12-115">Redigera dimensioner från ett dokument</span><span class="sxs-lookup"><span data-stu-id="7ce12-115">Editing Dimensions from a Document</span></span>  
 <span data-ttu-id="7ce12-116">Du kan redigera dimensioner från ett dokument.</span><span class="sxs-lookup"><span data-stu-id="7ce12-116">You can edit dimensions from a document.</span></span> <span data-ttu-id="7ce12-117">Du kan till exempel redigera en försäljningsorderrad.</span><span class="sxs-lookup"><span data-stu-id="7ce12-117">For example, you can edit a sales order line.</span></span>  

 <span data-ttu-id="7ce12-118">**Tidigare versioner**</span><span class="sxs-lookup"><span data-stu-id="7ce12-118">**Earlier Versions**</span></span>  

```  
Table 37, function ShowDimensions:  
TESTFIELD("Document No.");  
TESTFIELD("Line No.");  
DocDim.SETRANGE("Table ID",DATABASE::"Sales Line");  
DocDim.SETRANGE("Document Type","Document Type");  
DocDim.SETRANGE("Document No.","Document No.");  
DocDim.SETRANGE("Line No.","Line No.");  
DocDimensions.SETTABLEVIEW(DocDim);  
DocDimensions.RUNMODAL;  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
Table 37, function ShowDimensions:  
"Dimension ID" :=   
  DimSetEntry.EditDimensionSet(  
    "Dimension ID");  
```  

## <a name="showing-dimensions-from-posted-entries"></a><span data-ttu-id="7ce12-119">Visar dimensioner från bokförda transaktioner</span><span class="sxs-lookup"><span data-stu-id="7ce12-119">Showing Dimensions from Posted Entries</span></span>  
 <span data-ttu-id="7ce12-120">Du kan visa dimensioner från bokförda transaktioner, till exempel utleveransrader.</span><span class="sxs-lookup"><span data-stu-id="7ce12-120">You can show dimensions from posted entries, such as sales shipment lines.</span></span>  

 <span data-ttu-id="7ce12-121">**Tidigare versioner**</span><span class="sxs-lookup"><span data-stu-id="7ce12-121">**Earlier Versions**</span></span>  

```  
Table 111, function ShowDimensions:  
TESTFIELD("No.");  
TESTFIELD("Line No.");  
PostedDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Shipment Line");  
PostedDocDim.SETRANGE(  
  "Document No.","Document No.");  
PostedDocDim.SETRANGE("Line No.","Line No.");  
PostedDocDimensions.SETTABLEVIEW(PostedDocDim);  
PostedDocDimensions.RUNMODAL;  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
Table 111, function ShowDimensions:  
DimSetEntry.ShowDimensionSet(  
  "Dimension ID");  
```  

## <a name="getting-default-dimensions-for-a-document"></a><span data-ttu-id="7ce12-122">Få standarddimensioner för ett dokument</span><span class="sxs-lookup"><span data-stu-id="7ce12-122">Getting Default Dimensions for a Document</span></span>  
 <span data-ttu-id="7ce12-123">Du kan få standarddimensioner för ett dokument, till exempel en försäljningsorderrad.</span><span class="sxs-lookup"><span data-stu-id="7ce12-123">You can get default dimensions for a document, such as a sales order line.</span></span>  

 <span data-ttu-id="7ce12-124">**Tidigare versioner**</span><span class="sxs-lookup"><span data-stu-id="7ce12-124">**Earlier Versions**</span></span>  

```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
DimMgt.GetPreviousDocDefaultDim(  
  DATABASE::"Sales Header","Document Type",  
  "Document No.",0,  
  DATABASE::Customer,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
DimMgt.GetDefaultDim(  
  TableID,No,SourceCodeSetup.Sales,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
IF "Line No." <> 0 THEN  
  DimMgt.UpdateDocDefaultDim(  
    DATABASE::"Sales Line","Document Type",  
    "Document No.","Line No.",  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code");  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
GetSalesHeader;  
"Dimension ID" :=  
  DimMgt.GetDefaultDimID(  
    TableID,No,SourceCodeSetup.Sales,  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code",  
    SalesHeader."Dimension ID",  
    DATABASE::"Sales Header");

```  

## <a name="see-also"></a><span data-ttu-id="7ce12-125">Se även</span><span class="sxs-lookup"><span data-stu-id="7ce12-125">See Also</span></span>  
<span data-ttu-id="7ce12-126">[Designdetaljer: Dimensionsuppsättningstransaktioner](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="7ce12-126">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
<span data-ttu-id="7ce12-127">[Designdetaljer: Tabellstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="7ce12-127">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="7ce12-128">Designdetaljer: Kodenhet 408 Dimension Management</span><span class="sxs-lookup"><span data-stu-id="7ce12-128">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)
