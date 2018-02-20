---
title: Definiera vilka inkommande dokument Se | Microsoft Docs
description: "Ändra standardläge för inkommande dokument, till exempel e-fakturor, förbättra din översikt över bearbetade och obearbetade poster."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2016
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 65f3c14b29a5fcf7f855d7ea183445cf2fc1bd95
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="manage-many-incoming-document-records"></a>Hantera många inkommande dokumenttransaktioner
När du skapar eller bearbetar inkommande dokumentposter, kan antalet rader i fönstret **Inkommande dokument** växa till en utsträckning att du förlorar översikt. Därför kan du ange inkommande dokumentposter som Bearbetade för att ta bort dem från standardvyn. När du väljer åtgärden **Visa alla** kan du visa både behandlats och outredda transaktioner.

> [!NOTE]  
>   Du kan inte redigera information, koppla filer eller utföra andra processer på inkommande dokumentposter som har angetts till Bearbetad. Du måste först ange den till Obearbetad.

Kryssrutan **Bearbetad** markeras automatiskt för inkommande dokumentposter som har bearbetats, men du kan även markera eller avmarkera kryssrutan manuellt. Beroende på företagets rutiner kan en inkommande dokumentpost bearbetas när ett lagerrelaterat dokument har skapats för det, eller när en fil har bifogats.

> [!NOTE]  
>   När du öppnar fönstret **Inkommande dokument** med åtgärden **Mina inkommande dokument** i rollcentret, kommer endast obearbetade inkommande dokumentposter visas som standard. Detta kallas i detta ämne för"standardvyn".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Så här tar du bort inkommande dokumentposter från standardvyn
1. I fönstret **Inkommande dokument** markerar du en eller flera rader för inkommande dokumentposter som du vill ta bort från standardvyn.
2. Välj åtgärden **Ange som bearbetad**.

    De inkommande dokumentposterna tas bort från standardvyn och kryssrutan **Bearbetad** markeras på raderna.

> [!NOTE]  
>   Du kan också utföra den preliminära för den individuella transaktionen i fönstret **inkommande dokumentkort**.

## <a name="to-view-all-incoming-document-records"></a>Så här visar du inkommande dokumentposter
1. I fönstret **Inkommande dokument** väljer du åtgärden **Visa alla**.

Alla inkommande dokumentposter visas inklusive de som inte har kryssrutan **Behandlad** markerad.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Så här lägger du till inkommande dokumentposter till standardvyn
1. I fönstret **Inkommande dokument** väljer du åtgärden **Visa alla**.
2. Markera en eller flera rader för inkommande dokumentposter som du vill ska visas i standardvyn.
3. Välj åtgärden **Ange som obearbetad**.  

> [!NOTE]  
>   Du kan också utföra den preliminära för den individuella transaktionen i fönstret **inkommande dokumentkort**.

## <a name="see-also"></a>Se även
[Bearbeta inkommande dokument](across-process-income-documents.md)  
[Inkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

