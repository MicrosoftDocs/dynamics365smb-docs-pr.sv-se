---
title: Så här skapar du poster för inkommande dokument | Microsoft Docs
description: Du kan skapa poster för inkommande dokument, till exempel e-fakturor och hantera OCR uppgifter, e-handel och dokumentutbyte.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 637bb7ae6a757681ab0ada1b61ba0ec303a9cb97
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384755"
---
# <a name="create-incoming-document-records"></a>Skapa inkommande dokumentposter
På sidan **Inkommande dokument** använder du olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i . De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner.

Om du vill registrera ett externt dokument i [!INCLUDE[prod_short](includes/prod_short.md)], måste du först skapa eller slutföra en inkommande dokumentpost. Du kan göra detta manuellt eller så kan du ta ett foto på det externa dokumentet och sedan skapa en inkommande dokumentpost med bildfilen bifogad.

Innan du kan använda funktionen för inkommande dokument måste du utföra de nödvändiga inställningarna. Mer information finns i [Skapa inkommande dokument](across-how-setup-income-documents.md).

## <a name="to-approve-or-reject-an-incoming-document"></a>Så här Godkänn eller avvisa ett inkommande dokument.
Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter om inte dokumenten har godkänts först kan du konfigurera godkännare som måste godkänna transaktionerna innan de kan behandlas.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inkommande dokument** och välj sedan relaterad länk.
2. Markera raden med dokumentet som du vill godkänna eller avvisa, och välj sedan åtgärden **godkänna** eller **avvisa**.

Om du godkänner den inkommande dokumentposten markeras kryssrutan **Släppt** på den inkommande dokumentraden. Användaren som ansvarar för att skapa t.ex inköpsfakturor kan fortsätta med att bearbeta transaktionen.

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a>Så här skapar du en inkommande dokumentpost genom att ta ett foto
> [!NOTE]  
>   Följande proceduren gäller endast [!INCLUDE[prod_short](includes/prod_short.md)] för surfplatte- och telefonklienter.

1. Välj panelen **Skapa inkommande dokument från kamera** i appfältet och gå sedan till steg 4.
2. Välj annars alternativknappen på appfältet, välj **Inkommande dokument** och välj sedan **Alla**.
3. På sidan **Inkommande dokument** väljer du ellipsknappen och sedan **Skapa från kamera**. Kameran på Tablet PC:n eller telefonen aktiveras.
4. Ta ett foto av ett dokument, t. ex. ett inköpskvitto, som du vill bearbeta som ett inkommande dokument, och välj sedan knappen **OK** .

    En ny inkommande dokumentpost skapas med bilden bifogad.

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>Så här bifogar du en bild till en inkommande dokumentpost genom att ta ett foto
> [!NOTE]  
>   Följande proceduren gäller endast [!INCLUDE[prod_short](includes/prod_short.md)] för surfplatte- och telefonklienter.

1. Välj alternativknappen på appfältet, välj **Inkommande dokument** och välj sedan **Alla**.
2. Öppna kortet för en befintlig inkommande dokumentpost.
3. På sidan **Inkommande dokument** väljer du ellipsknappen och sedan **Bifoga fil från kamera**. Kameran på Tablet PC:n eller telefonen aktiveras.
4. Ta ett foto av ett dokument, t. ex. ett inköpskvitto, som du vill bearbeta som ett inkommande dokument, och välj sedan knappen **OK** .

    Bilden har bifogats till den inkommande dokumentposten.

## <a name="to-create-an-incoming-document-record-manually"></a>Så här skapar du en inkommande dokumentpost manuellt
1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inkommande dokument** och välj sedan relaterad länk.
2. Välj åtgärden **Skapa från fil**.  
3. Välj en fil och välj sedan **Öppna** på sidan **Infoga fil**. Filen kopplas automatiskt.
4. Välj alternativt åtgärden **Ny**.
5. För att bifoga en fil väljer du åtgärden **Bifoga fil**.
6. Markera filen som representerar det inkommande dokumentet i fråga och välj sedan knappen **Öppna** på sidan **Infoga fil**.
7. På sidan **Inkommande dokument** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se även
[Bearbeta inkommande dokument](across-process-income-documents.md)  
[Inkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]