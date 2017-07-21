---
title: "Så här skapar du poster för inkommande dokument | Microsoft Docs"
description: "Du kan skapa poster för inkommande dokument, till exempel e-fakturor och hantera OCR uppgifter, e-handel och dokumentutbyte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 36e1acc3125e325a9fca8fdd9ce797ac50c065c1
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create-incoming-document-records"></a>Så här skapar du inkommande dokumentposter
I fönstret **Inkommande dokument** använder du olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i . De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner.

Om du vill registrera ett externt dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du först skapa eller slutföra en inkommande dokumentpost. Du kan göra detta manuellt eller så kan du ta ett foto på det externa dokumentet och sedan skapa en inkommande dokumentpost med bildfilen bifogad.

Innan du kan använda funktionen för inkommande dokument måste du utföra de nödvändiga inställningarna. Mer information finns i [Så här skapar du inkommande dokument](across-how-setup-income-documents.md).

## <a name="to-approve-or-reject-an-incoming-document"></a>Så här Godkänn eller avvisa ett inkommande dokument.
Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter om inte dokumenten har godkänts först kan du konfigurera godkännare som måste godkänna transaktionerna innan de kan behandlas.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inkommande dokument** och välj sedan relaterad länk.
2. Markera raden med dokumentet som du vill godkänna eller avvisa, och välj sedan åtgärden **godkänna** eller **avvisa**.

Om du godkänner den inkommande dokumentposten markeras kryssrutan **Släppt** på den inkommande dokumentraden. Användaren som ansvarar för att skapa t.ex inköpsfakturor kan fortsätta med att bearbeta transaktionen.

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a>Så här skapar du en inkommande dokumentpost genom att ta ett foto
> [!NOTE]  
>   Följande proceduren gäller endast [!INCLUDE[d365fin](includes/d365fin_md.md)] för surfplatte- och telefonklienter.

1. Välj panelen **Skapa inkommande dokument från kamera** i appfältet och gå sedan till steg 4.
2. Välj annars alternativknappen på appfältet, välj **Inkommande dokument** och välj sedan **Alla**.
3. I fönstret **Inkommande dokument** väljer du ellipsknappen och sedan **Skapa från kamera**. Kameran på Tablet PC:n eller telefonen aktiveras.
4. Ta ett foto av ett dokument, t.ex. ett inköpskvitto, som du vill bearbeta som ett inkommande dokument, och välj sedan knappen **OK** .

En ny inkommande dokumentpost skapas med bilden bifogad.

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>Så här bifogar du en bild till en inkommande dokumentpost genom att ta ett foto
> [!NOTE]  
>   Följande proceduren gäller endast [!INCLUDE[d365fin](includes/d365fin_md.md)] för surfplatte- och telefonklienter.

1. Välj alternativknappen på appfältet, välj **Inkommande dokument** och välj sedan **Alla**.
2. Öppna kortet för en befintlig inkommande dokumentpost.
3. I fönstret **Inkommande dokument** väljer du ellipsknappen och sedan **Bifoga fil från kamera**. Kameran på Tablet PC:n eller telefonen aktiveras.
4. Ta ett foto av ett dokument, t.ex. ett inköpskvitto, som du vill bearbeta som ett inkommande dokument, och välj sedan knappen **OK** .

Bilden har bifogats till den inkommande dokumentposten.

## <a name="to-create-an-incoming-document-record-manually"></a>Så här skapar du en inkommande dokumentpost manuellt
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inkommande dokument** och välj sedan relaterad länk.
2. Välj åtgärden **Skapa från fil**.  
3. Välj en fil och välj sedan **Öppna** i fönstret **Infoga fil**.

    Filen kopplas automatiskt.
4. Välj alternativt åtgärden **Ny**.
5. För att bifoga en fil väljer du åtgärden **Bifoga fil**.
6. Markera filen som representerar det inkommande dokumentet i fråga och välj sedan knappen **Öppna** i fönstret **Infoga fil**.
7. I fönstret **Inkommande dokument** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se även
[Bearbeta inkommande dokument](across-process-income-documents.md)  
[Inkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

