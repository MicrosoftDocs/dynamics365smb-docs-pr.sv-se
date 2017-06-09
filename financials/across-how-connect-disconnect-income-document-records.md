---
title: "Så här ansluter du och kopplar från inkommande dokumentposter från dokument och transaktioner | Microsoft Docs"
description: "Så här ansluter du och kopplar från inkommande dokumentposter från dokument och transaktioner"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 05/12/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d29979de3643cbe542f31d3bc67ee0f47effcd4a
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-connect-and-disconnect-incoming-document-records-from-documents-and-entries"></a>Så här ansluter du och kopplar från inkommande dokumentposter från dokument och transaktioner
Du kan lagra externa affärsdokument i [!INCLUDE[d365fin](includes/d365fin_md.md)] genom att koppla dokumentfilerna till de relaterade inkommande dokumentposterna. Om dokumentet, t.ex. en inköpsfaktura, inte ursprungligen skapades som en inkommande dokumentpost kan du fortfarande skapa och koppla en inkommande dokumentpost till den senare. Du kan även bifoga inkommande dokumentfiler till bokförda inköps- och försäljningsdokument och till leverantörs-, kund - och redovisningsposter genom att använda till exempel faktaboxen **Inkommande dokumentfiler** t.ex. i fönstren **Bokförda inköpsfakturor** och **Lev.reskontratransaktioner**.

Från fönstren **Kontoplan** och **Redovisningstransaktioner** kan du använda en sökfunktion för att hitta redovisningsposter för bokförda inköps- och försäljningsdokument som inte har inkommande dokumentposter och sedan länka dem till befintliga poster eller skapa nya centralt med bifogade dokumentfiler. Mer information finns i [Så här söker du efter bokförda dokument utan inkommande dokumentposter](across-how-find-posted-documents-without-income-document-records.md).

Följande tillvägagångssätt visar hur du bifoga en fil till en befintlig inköpsfaktura som inte har skapats från en inkommande dokumentpost och hur du bifogar en fil till en leverantörsreskontrapost. Att bifoga en fil till bokförda inköps- eller försäljningsdokument fungerar på liknande sätt.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Så här skapar du och kopplar en inköpsfaktura från en inköpsfaktura
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Inköpsfakturor**, och välj sedan relaterad länk.
2. Markera raden för en inköpsfaktura som du vill bifoga en fil till och välj sedan åtgärden **Skapa inkommande dokument från fil**.
3. Eller markera raden för en inköpsfaktura som du vill bifoga en fil till och välj sedan åtgärden **Bifoga fil**.
4. Markera filen som representerar det inkommande dokumentet i fråga och välj sedan knappen **Öppna** i fönstret **Infoga fil**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Så här skapar du och kopplar en inköpsfaktura från en leverantörsreskontrapost
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger du **Lev.reskontratransaktioner** och väljer sedan relaterad länk.
2. Markera raden för en leverantörsreskontratransaktion som du vill bifoga en fil till och välj sedan åtgärden **Skapa inkommande dokument från fil**.
3. Eller markera raden för en leverantörsreskontratransaktion som du vill bifoga en fil till och välj sedan åtgärden **Bifoga fil**.
4. Markera filen som representerar det inkommande dokumentet i fråga och välj sedan knappen **Öppna** i fönstret **Infoga fil**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Så här tar du bort kopplingen från en inkommande dokumentpost till ett bokfört dokument
Du kan ta bort bifogade filer från ej bokförda dokument när som helst genom att radera posten för det inkommande dokumentet. Om dokumentet är bokfört måste du först ta bort kopplingen från den inkommande dokumentposten.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Inkommande dokument**, och välj sedan relaterad länk.
2. Markera raden för en inkommande dokumentpost som kopplas till ett bokfört dokument som du vill ta bort, och välj sedan åtgärden **Ta bort referens till post**.

Kopplingen till det bokförda dokumentet tas bort. Du kan nu fortsätta med att koppla en annan inkommande dokumentpost till det bokförda dokumentet enligt vad som beskrivs i det här avsnittet..

## <a name="see-also"></a>Se även
[Bearbeta inkommande dokument](across-process-income-documents.md)  
[Inkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

