---
title: Definiera kontakter i ett segment | Microsoft Docs
description: När du har skapat ett segment kan du kan lägga till kontakter i segmentet, exempelvis som en del av en marknadsföringskampanj där du riktar dig mot vissa kunder.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect, contact, client, customer
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7cf4c0f1241155f464fde5196125b0a1bed2aeee
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784548"
---
# <a name="add-contacts-to-segments"></a>Lägga till kontakter i segment
När du har skapat ett segment och angett grundläggande information om det kan du lägga till kontakter i segmentet. Det kan du göra genom att manuellt fylla i raderna på sidan **Segment** men det är enklare och går snabbare att använda åtgärden **Lägg till kontakter**.

## <a name="to-add-a-contact-to-a-segment"></a>Så här lägger du till kontakter i ett segment
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Segment** och välj sedan tillhörande länk.  
2. Markera segmentet och välj sedan åtgärden **Lägg till kontakter**. Sidan för batch-jobbet **Lägg till kontakter** öppnas.
3. I avsnittet **Kontakt** anger du filter för att ange den information som ska användas när du väljer särskilda kontakter.

Om du vill ange ytterligare filter upprepar du den här proceduren på alla de återstående avsnitt. Välj sedan **OK**.

Om du har lagt till kontakter av misstag och vill gå tillbaka ett steg väljer du åtgärden **Gå tillbaka**.

## <a name="to-refine-the-number-of-contacts"></a>Om du vill förfina antalet kontakter
När du har valt kontakter i ett segment kanske du bestämmer dig för att ta bort några av dem, men behålla andra. Du kan ta bort kontakter manuellt från raderna på sidan **Segment**, men det är enklare och går snabbare att använda åtgärden **Förfina kontakter**.

1. Öppna segmentet.
2. Välj **kontakter**, och välj sedan åtgärden **förfina kontakter**. Sidan **Ta bort kontakter – förfina** öppnas.
3. I avsnittet **Kontakt** anger du filter för att ange den information som ska användas för att välja de kontakter som ska tas bort från segmentet.
4. Lägg till ytterligare filter vid behov och välj sedan knappen **OK**.

Du kan förfina ett segment så många gånger som du vill. Klicka på **Gå tillbaka** om du har förfinat ett segment av misstag och vill gå tillbaka till föregående steg.

Du kan visa en lista över de segmentvillkor som har använts genom att klicka på avsnittet **Allmänt** och välja fältet **Antal kriteriumåtgärder**.

## <a name="to-reduce-the-number-of-contacts"></a>Om du vill minska antalet kontakter
När du har valt kontakter i ett segment kanske du vill ta bort några av dem. Du kan göra detta genom att manuellt ta bort dem från raderna på sidan Segment, men det går enklare och snabbare att ange vilka kontakter som ska tas bort med funktionen Reducera kontakter och vilka som ska behållas med funktionen Förfina urval.

1. Öppna segmentet.
2. Välj kontakter, och välj sedan åtgärden **Minska kontakter**. Sidan **Ta bort kontakter – minska** öppnas.
3. I avsnittet **Kontakt** anger du filter för att ange den information som ska användas för att välja de kontakter som ska tas bort från segmentet.
4. Lägg till ytterligare filter vid behov och välj sedan knappen **OK**.

Du kan reducera ett segment så många gånger som du vill. Klicka på åtgärden **Gå tillbaka** om du har förfinat ett segment av misstag och vill gå tillbaka till föregående steg.

## <a name="see-also"></a>Se även
[Skapa ett segment](marketing-how-create-segment.md)   
[Hantera segment](marketing-segments.md)  
[Hantera Försäljningsmöjligheter](marketing-manage-sales-opportunities.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]