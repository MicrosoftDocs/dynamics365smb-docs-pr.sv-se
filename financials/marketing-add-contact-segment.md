---
title: Definiera kontakter i ett segment | Microsoft Docs
description: "När du har skapat ett segment kan du kan lägga till kontakter i segmentet, exempelvis som en del av en marknadsföringskampanj där du riktar dig mot vissa kunder."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 159359a6d7cb051bd3cda0e750ba52f8d2a06e18
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="add-contacts-to-segments"></a>Lägga till kontakter i segment
När du har skapat ett segment och angett grundläggande information om det kan du lägga till kontakter i segmentet. Det kan du göra genom att manuellt fylla i raderna i fönstret **Segment**, men det är enklare och går snabbare att använda åtgärden **Lägg till kontakter**.

## <a name="to-add-a-contact-to-a-segment"></a>Lägga till kontakter i ett segment
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Segment** och välj sedan relaterad länk.  
2. Markera segmentet och välj sedan åtgärden **Lägg till kontakter**. Fönstret för batch-jobbet **Lägg till kontakter** öppnas.
3. I avsnittet **Kontakt** anger du filter för att ange den information som ska användas när du väljer särskilda kontakter.

Om du vill ange ytterligare filter upprepar du den här proceduren på alla de återstående avsnitt. Välj sedan **OK**.

Om du har lagt till kontakter av misstag och vill gå tillbaka ett steg väljer du åtgärden **Gå tillbaka**.

## <a name="to-refine-the-number-of-contacts"></a>Om du vill förfina antalet kontakter
När du har valt kontakter i ett segment kanske du bestämmer dig för att ta bort några av dem, men behålla andra. Du kan ta bort kontakter manuellt från raderna i fönstret **Segment**, men det är enklare och går snabbare att använda åtgärden **Förfina kontakter**.

1. Öppna segmentet.
2. Välj **kontakter**, och välj sedan åtgärden **förfina kontakter**. Fönstret **Ta bort kontakter - förfina** öppnas.
3. I avsnittet **Kontakt** anger du filter för att ange den information som ska användas för att välja de kontakter som ska tas bort från segmentet.
4. Lägg till ytterligare filter vid behov och välj sedan knappen **OK**.

Du kan förfina ett segment så många gånger som du vill. Klicka på **Gå tillbaka** om du har förfinat ett segment av misstag och vill gå tillbaka till föregående steg.

Du kan visa en lista över de segmentvillkor som har använts genom att klicka på avsnittet **Allmänt** och välja fältet **Antal kriteriumåtgärder**.

## <a name="to-reduce-the-number-of-contacts"></a>Om du vill minska antalet kontakter
När du har valt kontakter i ett segment kanske du vill ta bort några av dem. Du kan göra detta genom att manuellt ta bort dem från raderna i fönstret Segment, men det går enklare och snabbare att ange vilka kontakter som ska tas bort med funktionen Reducera kontakter och vilka som ska behållas med funktionen Förfina urval.

1. Öppna segmentet.
2. Välj kontakter, och välj sedan åtgärden **Minska kontakter**. Fönstret **Ta bort kontakter - reducera** visas.
3. I avsnittet **Kontakt** anger du filter för att ange den information som ska användas för att välja de kontakter som ska tas bort från segmentet.
4. Lägg till ytterligare filter vid behov och välj sedan knappen **OK**.

Du kan reducera ett segment så många gånger som du vill. Klicka på åtgärden **Gå tillbaka** om du har förfinat ett segment av misstag och vill gå tillbaka till föregående steg.

## <a name="see-also"></a>Se även
[Skapa ett segment](marketing-how-create-segment.md)   
[Hantera segment](marketing-segments.md)  
[Hantera Försäljningsmöjligheter](marketing-manage-sales-opportunities.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

