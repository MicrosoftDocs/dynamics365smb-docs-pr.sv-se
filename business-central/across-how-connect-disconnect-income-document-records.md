---
title: Skapa inkommande dokumentposter från dokument
description: Du kan lagra externa affärsdokument genom att koppla dokumentfilerna till de relaterade inkommande dokumentposterna.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 609a57cd1d87a8a3518d6eaf7bc3fe8fc142953a
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134362"
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Skapa inkommande dokumentposter direkt från dokument och transaktioner
Du kan lagra externa affärsdokument i [!INCLUDE[prod_short](includes/prod_short.md)] genom att koppla dokumentfilerna till de relaterade inkommande dokumentposterna. Om dokumentet, t. ex. en inköpsfaktura, inte ursprungligen skapades som en inkommande dokumentpost kan du fortfarande skapa och koppla en inkommande dokumentpost till den senare. Du kan även bifoga inkommande dokumentfiler till bokförda inköps- och försäljningsdokument och till leverantörs-, kund – och redovisningsposter genom att använda till exempel faktaboxen **Inkommande dokumentfiler** t. ex. på sidorna **Bokförda inköpsfakturor** och **Lev.reskontratransaktioner**.

Från sidorna **Kontoplan** och **Redovisningstransaktioner** kan du använda en sökfunktion för att hitta redovisningsposter för bokförda inköps- och försäljningsdokument som inte har inkommande dokumentposter, och sedan länka dem till centralt befintliga poster eller skapa nya med bifogade dokumentfiler. Mer information finns i [Söka efter bokförda dokument utan inkommande dokumentposter](across-how-find-posted-documents-without-income-document-records.md).

Följande tillvägagångssätt visar hur du bifoga en fil till en befintlig inköpsfaktura som inte har skapats från en inkommande dokumentpost och hur du bifogar en fil till en leverantörsreskontrapost. Att bifoga en fil till bokförda inköps- eller försäljningsdokument fungerar på liknande sätt.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Så här skapar du och kopplar en inköpsfaktura från en inköpsfaktura
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.
2. Markera raden för en inköpsfaktura som du vill bifoga en fil till och välj sedan åtgärden **Skapa inkommande dokument från fil**.
3. Eller markera raden för en inköpsfaktura som du vill bifoga en fil till och välj sedan åtgärden **Bifoga fil**.
4. Markera filen som representerar det inkommande dokumentet i fråga och välj sedan knappen **Öppna** på sidan **Infoga fil**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Så här skapar du och kopplar en inköpsfaktura från en leverantörsreskontrapost
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Lev.reskontratransaktioner** och välj sedan relaterad länk.
2. Markera raden för en leverantörsreskontratransaktion som du vill bifoga en fil till och välj sedan åtgärden **Skapa inkommande dokument från fil**.
3. Eller markera raden för en leverantörsreskontratransaktion som du vill bifoga en fil till och välj sedan åtgärden **Bifoga fil**.
4. Markera filen som representerar det inkommande dokumentet i fråga och välj sedan knappen **Öppna** på sidan **Infoga fil**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Så här tar du bort kopplingen från en inkommande dokumentpost till ett bokfört dokument
Du kan ta bort bifogade filer från ej bokförda dokument när som helst genom att radera posten för det inkommande dokumentet. Om dokumentet är bokfört måste du först ta bort kopplingen från den inkommande dokumentposten.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inkommande dokument** och väljer sedan relaterad länk.
2. Markera raden för en inkommande dokumentpost som kopplas till ett bokfört dokument som du vill ta bort, och välj sedan åtgärden **Ta bort referens till post**.

Kopplingen till det bokförda dokumentet tas bort. Du kan nu fortsätta med att koppla en annan inkommande dokumentpost till det bokförda dokumentet enligt vad som beskrivs i det här avsnittet.

## <a name="see-also"></a>Se även
[Bearbeta inkommande dokument](across-process-income-documents.md)  
[Inkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]