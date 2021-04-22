---
title: Konfigurera Inkommande dokument | Microsoft Docs
description: Du kan använda funktionen inkommande dokument för att skapa elektroniska dokument, hantera OCR-uppgifter, importera fakturor och konvertera bildfiler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fd35c0af4d2b66f99c0a4a3a65f77826cd9af806
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775928"
---
# <a name="set-up-incoming-documents"></a>Ställa in inkommande dokument

Om du skapar redovisningsjournalrader från inkommande dokumentposter måste du ange vilken journalmall och batch som ska användas på sidan **Inställning av inkommande dokument**.

Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter såvida inte dokumenten har godkänts först, måste du konfigurera godkännare för arbetsflöde.

För att omvandla PDF- och bildfiler till elektroniska dokument som du kan konverteras till, till exempel,inköpsfakturor inne i "[!INCLUDE[prod_short](includes/prod_short.md)]" måste du först konfigurera OCR-funktionen och aktivera tjänsten. Välj ett servicepaket som passar din organisation och/eller ditt land/din region. Du kan också skapa transaktioner manuellt för att visa de externa dokumenten.  

När funktionen för Inkommande dokument är inställd, kan du använda olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i . De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner. Mer information finns i [Bearbeta inkommande dokument](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Så här konfigurerar du funktionen för inkommande dokument

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inkommande dokumentkonfiguration** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Som en del av inställningen måste du bestämma om du vill kräva godkännande av inkommande dokument. Om du vill kräva godkännande måste du ställa in godkännare och arbetsflöde för godkännande. Om organisationen inte avser att kräva godkännande kan du hoppa över nästa avsnitt.  

Slutligen, om du använder en tjänst för att konvertera PDF- eller bildfiler som representerar inkommande dokument, måste du installera det. Annars kan du hoppa över avsnittet.  

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Så här konfigurerar du godkännare för inkommande dokument

Om du vill kan du ställa in en godkännandeprocedur för inkommande dokument. Godkännare för inkommande dokument måste skapas som användare av arbetsflöde för godkännande.

Innan du kan skapa arbetsflöden som innehåller godkännandesteg, måste du skapa arbetsflödeanvändare som är inblandade i godkännandeprocessen. På sidan **Användarinställningar för godkännande** anger du även beloppsgränser för vissa typer av förfrågningar och definierar ersättande godkännare som godkännandebegäran kan delegeras till när den ursprungliga godkännaren är frånvarande. Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Så här konfigurerar du en OCR-tjänst

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för OCR-tjänst** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Dina inloggningsdata krypteras automatiskt.

Mer information finns i [Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-also"></a>Se även

[Bearbeta inkommande dokument](across-process-income-documents.md)  
[Inkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]