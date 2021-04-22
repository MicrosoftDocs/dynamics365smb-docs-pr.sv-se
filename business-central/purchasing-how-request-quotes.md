---
title: Skapa en inköpsoffert för att begära en offert | Microsoft Docs
description: Beskriver hur du skapar ett försäljningserbjudande eller begäran om förslag (Offertförfrågan) för att registrera ditt erbjudande till kunden att sälja produkter under vissa villkor.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 416c5a4e4376932c16a1496f2db2b0c79307d22b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772625"
---
# <a name="request-quotes"></a>Begär offerter
En inköpsoffert kan användas som ett preliminärt utkast för en inköpsorder, som sedan kan göras om till en inköpsfaktura eller en order.


## <a name="to-create-a-purchase-quote"></a>Så här skapar du en inköpsoffert:
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsofferter** och välj sedan tillhörande länk.
2. Skapa ett nytt dokument på samma sätt som du gör en inköpsorder. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Så här gör du om inköpsofferter till inköpsorder:
När du har accepterat leverantörens offert kan du omvandla den till en inköpsfaktura eller en order för att behandla inköpet.

1. Öppna en inköpsoffert som är redo att konvertera och välj sedan åtgärden **skapa order**.

Inköpsofferten tas bort från databasen. En inköpsfaktura eller försäljningsorder skapas baserat på informationen i inköpsofferten där du kan bearbeta inköpet. I fältet **Offertnr** på inköpsfakturan eller inköpsordern kan du ange numret på inköpsofferten som den har skapats från.

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Skicka dokument som e-transaktion](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]