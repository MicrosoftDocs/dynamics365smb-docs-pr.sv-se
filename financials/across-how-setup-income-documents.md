---
title: "Så här konfigurerar du Inkommande dokument | Microsoft Docs"
description: "Så här konfigurerar du Inkommande dokument"
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
ms.openlocfilehash: be99b334117c2e0cb7fe989ecc87dcf71a1d765d
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-incoming-documents"></a>Så här konfigurerar du Inkommande dokument
Om du skapar redovisningsjournalrader från inkommande dokumentposter måste du ange vilken journalmall och batch som ska användas i fönstret **Inställning av inkommande dokument**.

Om du inte vill att användare ska skapa fakturor eller redovisningsjournalrader från inkommande dokumentposter om inte dokumenten har godkänts först, måste du konfigurera godkännare i fönstret **Godkännare för inkommande dokument**.

För att omvandla PDF- och bildfiler till elektroniska dokument som du kan konverteras till, till exempel,inköpsfakturor inne i "[!INCLUDE[d365fin](includes/d365fin_md.md)]" måste du först konfigurera OCR-funktionen och aktivera tjänsten.

När funktionen för Inkommande dokument är inställd, kan du använda olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i . De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner. Mer information finns i [Bearbeta inkommande dokument](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Så här konfigurerar du funktionen för inkommande dokument
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Ställa in inkommande dokument**, och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Så här konfigurerar du godkännare för inkommande dokument
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Ställa in inkommande dokument**, och välj sedan relaterad länk.  
2. I fönstret **Inställning av inkommande dokument** väljer du åtgärden **Godkännare**.

    Fönstret **Godkännare för inkommande dokument** visar alla användare som är inställda i [!INCLUDE[d365fin](includes/d365fin_md.md)].  
3. Markera en eller flera användare som kan godkänna ett inkommande dokument, innan en relaterat dokumentet eller journalrad kan skapas.

När godkännare har konfigurerats i fönstret **Godkännare för inkommande dokument** kan endast dessa användare godkänna ett inkommande dokument om kryssrutan **Kräv godkännande för att skapa** i fönstret **Inställning av inkommande dokument** är markerad.

**Obs!** Denna inställning av godkännande är inte relaterad till arbetsflöden för godkännande. Mer information finns i [Så här använder du arbetsflöden för godkännande](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>Så här konfigurerar du en OCR-tjänst
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **OCR-serviceinställningar**, och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a>Så här kan du kryptera dina inloggningsuppgifter
Du rekommenderas att skydda de inloggningsuppgifter som du anger i fönstret **OCR-serviceinställningar**. Du kan kryptera data på servern genom att skapa nya eller importera befintliga krypteringsnycklar som aktiverar på serverinstansen med anslutningen till databasen.

1. I fönstret **OCR-serviceinställningar** väljer du åtgärden **Krypteringshantering**.
2. Aktivera krypteringen av dina data i fönstret **Datakrypteringshantering**.

## <a name="see-also"></a>Se även
[Bearbeta inkommande dokument](across-process-income-documents.md)  
[Inkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

