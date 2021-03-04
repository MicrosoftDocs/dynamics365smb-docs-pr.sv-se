---
title: Sök efter dokument utan bilagor | Microsoft Docs
Description: Du kan söka efter redovisningstransaktioner för bokförda inköps- och försäljningsdokument som inte har inkommande elektroniska dokument, till exempel importerade fakturor.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e15284452bb80acc329e46df7361ee9dea556996
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754973"
---
# <a name="find-posted-documents-without-incoming-document-records"></a>Söka efter bokförda dokument utan inkommande dokumentposter
Från sidorna **Kontoplan** och **Redovisningstransaktioner** kan du använda en sökfunktion för att hitta redovisningsposter för bokförda inköps- och försäljningsdokument som inte har inkommande dokumentposter, och sedan länka dem till centralt befintliga poster eller skapa nya med bifogade dokumentfiler.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>Söka efter bokförda dokument utan inkommande dokumentposter
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kontoplan** och välj sedan tillhörande länk.
2. Välj en rad för ett redovisningskonto för vilka redovisningstransaktioner du vill se bokförda inköps- och försäljningsdokument utan inkommande dokumentpost och välj sedan **Bokförda dokument utan inkommande dokument**.
3. Välj alternativt åtgärden **Transaktioner**.
4. På sidan **Redovisningstransaktioner** väljer du åtgärden **Bokförda dokument utan inkommande dokument**.

Sidan **Dokförda dokument utan inkommande dokument** öppnas med visning av bokförda inköps- och försäljningsdokument utan inkommande dokumentposter som representeras av redovisningstransaktioner på det redovisningskonto som du öppnade sidan för. Sidan kan innehålla högst 1000 rader. Som standard innehåller fältet **Datumfilter** därför ett filter som begränsar raderna till poster med bokföringsdatum från början av bokföringsperioden till arbetsdatumet.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Koppla hittade dokument till befintliga inkommande dokumentposter
1. På sidan **Bokförda dokument utan inkommande dokument** väljer du raden för ett bokfört dokument som du vill koppla till en befintlig inkommande dokumentpost och väljer sedan åtgärden **Välj inkommande dokument**.
2. På sidan **Inkommande dokument** väljer du den inkommande dokumentpost som du vill koppla till det hittade bokförda dokumentet och klickar sedan på knappen **OK**.
3. Nu är den valda inkommande dokumentposten kopplad till det bokförda dokumentet på sidan **Bokförda dokument utan inkommande dokument**, som du kan se i faktaboxen **Inkommande dokumentfiler**.

Om en relevant inkommande dokumentpost inte finns på sidan **Inkommande dokument** kan du skapa den. Mer information finns i [Så här skapar du inkommande dokumentposter](across-how-create-income-document-records.md).

## <a name="see-also"></a>Se även
[Bearbeta inkommande dokument](across-process-income-documents.md)  
[Inkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]