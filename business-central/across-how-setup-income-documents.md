---
title: Ställa in inkommande dokument
description: 'Du kan använda funktionen inkommande dokument för att skapa elektroniska dokument, hantera OCR-uppgifter, importera fakturor och konvertera bildfiler.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="set-up-incoming-documents" />Ställa in inkommande dokument

Om du skapar redovisningsjournalrader från inkommande dokumentposter måste du ange vilken journalmall och batch som ska användas på sidan **Inställning av inkommande dokument**.

När funktionen för **Inkommande dokument** är inställd, kan du använda olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i . De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner. Mer information finns i [Så här skapar du inkommande dokumentposter](across-how-create-income-document-records.md).

## <a name="to-set-up-the-incoming-documents-feature" />Så här konfigurerar du funktionen för inkommande dokument

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inkommande dokumentkonfiguration** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Som en del av inställningen måste du bestämma om du vill kräva godkännande av inkommande dokument. Om du vill kräva godkännande måste du [ställa in godkännare och arbetsflöde för godkännande](#to-set-up-approvers-of-incoming-document-records). Om organisationen inte avser att kräva godkännande kan du hoppa över nästa avsnitt.

Slutligen, om du använder en OCR-tjänst för att konvertera PDF- eller bildfiler som representerar inkommande dokument, [måste du installera det](#to-set-up-an-ocr-service). Annars kan du hoppa över avsnittet.

## <a name="to-set-up-approvers-of-incoming-document-records" />Så här konfigurerar du godkännare för inkommande dokument

Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter om inte dokumenten har godkänts först, upprätta en godkännandeprocess för de inkommande dokumenten. Godkännare för inkommande dokument måste skapas som användare av arbetsflöde för godkännande.

Innan du kan skapa arbetsflöden som innehåller godkännandesteg, måste du skapa arbetsflödeanvändare som är inblandade i godkännandeprocessen. På sidan **Användarinställningar för godkännande** anger du även beloppsgränser för vissa typer av förfrågningar och definierar ersättande godkännare som godkännandebegäran kan delegeras till när den ursprungliga godkännaren är frånvarande. Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service" />Så här konfigurerar du en OCR-tjänst

Om du vill aktivera PDF-och bildfiler i elektroniska dokument som du kan omvandla till fakturor, kredit notor eller journal rader, ställer du in OCR-funktionen. Du kan också skapa transaktioner manuellt för att visa de externa dokumenten.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **OCR serviceinställningar** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Dina inloggningsdata krypteras automatiskt.

Mer information finns i [Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics-365-business-central" />Se relaterad [Microsoft utbildning](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Se även

[Inkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
