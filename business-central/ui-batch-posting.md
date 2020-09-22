---
title: Så här bokför du flera dokument på samma gång | Microsoft Docs
description: I stället för att bokföra enskilda dokument var för sig kan du välja flera icke bokförda dokument i en lista för batch-bokföring, antingen för direkt bokföring eller som t.ex. i slutet av dagen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: 2c04dac37b043995a9b78e2f662f9411c3cf9ae1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782524"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Bokföra flera dokument på samma gång

I stället för att bokföra enskilda dokument var för sig kan du välja flera icke bokförda dokument i en lista för direkt bokföring eller för batch-bokföring enligt ett schema, t.ex. i slutet av dagen. Detta kan vara användbart om endast en ansvarig kan bokföra dokument som skapats av andra användare eller undvika problem med system prestanda vid bokföring under arbetstid.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Så här bokför du flera inköpsorder direkt

I proceduren nedan beskrivs hur du bokför flera inköpsorder direkt. Stegen är liknande för alla ingående och utgående dokument.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsorder** och välj sedan relaterad länk.
2. På sidan **inköpsorder** går du vidare för att välja alla order som ska bokföras:
3. I fältet **Nr.** väljer du de tre lodräta punkterna för att öppna snabbmenyn och sedan väljer du åtgärden **Välj fler**.
4. Markera kryssrutan för alla rader som motsvarar order som du vill bokföra samtidigt.
5. Välj åtgärden **bokföra** och välj sedan åtgärden **bokför**.
6. Välj knappen **Ja** på bekräftelsemeddelandet.

## <a name="to-batch-post-multiple-purchase-orders"></a>Så här bokför du flera inköpsorder

I proceduren nedan beskrivs hur du bokför flera inköpsorder. Stegen är liknande för alla inköps- och försäljningsdokument där åtgärden **batch-bokföring** är tillgänglig.

> [!NOTE]
> Masspublicering av dokument sker i bakgrunden. [!INCLUDE [prodshort](includes/prodshort.md)] online omfattar standardjobb för bakgrundsinlägg och masspublicering. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsorder** och välj sedan tillhörande länk.  
2. På sidan **inköpsorder** går du vidare för att välja alla order som ska bokföras:
3. I fältet **Nr.** väljer du de tre lodräta punkterna för att öppna snabbmenyn och sedan väljer du åtgärden **Välj fler**.
4. Markera kryssrutan för alla rader som motsvarar order som du vill bokföra samtidigt.
5. Välj åtgärden **bokföra** och välj sedan åtgärden **Bokför batch-jobb**.
6. På sidan **Batch-bokför inköpsorder** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Välj **OK**.
8. Om du vill visa potentiella problem som uppstod vid batch-bokföring av dokument öppnar du fönstret **registrera felmeddelande**.

Inköpsordern läggs nu till i en dedikerad jobbkötransaktion som definierar när dokumenten bokförs. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

Om du väljer **PDF** i fältet **Rapportutdatatyp**, kommer bokförda inköpsorder vara tillgängliga i delen **rapportinkorg** i rollcentret.

## <a name="see-also"></a>Se även

[Bokför dokument och journaler](ui-post-documents-journals.md)  
[Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)  
[Redigera bokförda dokument](across-edit-posted-document.md)  
[Korrigera eller annullera obetalda inköpsfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
