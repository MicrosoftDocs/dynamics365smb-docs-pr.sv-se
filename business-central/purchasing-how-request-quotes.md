---
title: Skapa en inköpsoffert för att begära en offert
description: Beskriver hur du skapar ett försäljningserbjudande eller offertförfrågan för att registrera ditt erbjudande till kunden att sälja produkter under vissa villkor.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: 49, 97, 9306, 9346
ms.date: 08/08/2022
ms.author: edupont
ms.openlocfilehash: 113e562a6d8f5b29df6ff2800cc93a151a1d57e8
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532599"
---
# <a name="request-quotes"></a>Begär offerter

En inköpsoffert kan användas som ett preliminärt utkast för en inköpsorder, som sedan kan göras om till en inköpsfaktura.

## <a name="create-a-purchase-quote"></a>Skapa en inköpsoffert

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsofferter** och väljer sedan relaterad länk.
2. Skapa ett nytt dokument på samma sätt som du gör en inköpsorder. Lär dig mer i [registrera inköp](purchasing-how-record-purchases.md).

## <a name="convert-a-purchase-quote-to-a-purchase-order"></a>Konvertera inköpsofferter till inköpsorder

När du har accepterat leverantörens offert kan du omvandla den till en inköpsorder för att behandla inköpet.

1. Öppna en inköpsoffert som är redo att konvertera och välj sedan åtgärden **skapa order**.

Inköpsofferten tas bort från databasen. En inköpsorder skapas utifrån informationen i inköpsofferten som du kan använda för att behandla köpet och sedan bokföra en inköpsfaktura. I fältet **Offertnr** på inköpsfakturan eller inköpsordern kan du ange numret på inköpsofferten som den har skapats från.

> [!NOTE]
> Det går inte att konvertera en inköpsoffert till en inköpsfaktura direkt, som det är möjligt med försäljningsofferter. Om du vill ha mer information om hur du skapar en inköpsfaktura kan du läsa [Registrera inköp med inköps fakturor](purchasing-how-record-purchases.md).

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/learn/modules/create-purchase-documents-dynamics-365-business-central/).

## <a name="see-also"></a>Se även

[Inköp](purchasing-manage-purchasing.md)  
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
