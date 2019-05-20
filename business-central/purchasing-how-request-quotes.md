---
title: Skapa en inköpsoffert för att begära en offert | Microsoft Docs
description: Beskriver hur du skapar ett försäljningserbjudande eller begäran om förslag (Offertförfrågan) för att registrera ditt erbjudande till kunden att sälja produkter under vissa villkor.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 109e00637b9e5a110005660bb108ec8e8a551345
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252275"
---
# <a name="request-quotes"></a>Begär offerter
En inköpsoffert kan användas som ett preliminärt utkast för en inköpsorder, som sedan kan göras om till en inköpsfaktura eller en order.


## <a name="to-create-a-purchase-quote"></a>Så här skapar du en inköpsoffert:
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsofferter** och välj sedan relaterad länk.
2. Skapa ett nytt dokument på samma sätt som du gör en inköpsorder. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Så här gör du om inköpsofferter till inköpsorder:
När du har accepterat leverantörens offert kan du omvandla den till en inköpsfaktura eller en order för att behandla inköpet.

1. Öppna en inköpsoffert som är redo att konvertera och välj sedan åtgärden **skapa order**.

Inköpsofferten tas bort från databasen. En inköpsfaktura eller försäljningsorder skapas baserat på informationen i inköpsofferten där du kan bearbeta inköpet. I fältet **Offertnr** på inköpsfakturan eller inköpsordern kan du ange numret på inköpsofferten som den har skapats från.

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
