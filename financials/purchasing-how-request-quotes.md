---
title: "Skapa en inköpsoffert för att begära en offert från leverantören | Microsoft Docs"
description: "Beskriver hur du skapar ett försäljningserbjudande eller begäran om förslag (Offertförfrågan) för att registrera ditt erbjudande till kunden att sälja produkter under vissa villkor."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: fe51ade7a46ab7a8fdf77419a0098ac47fe2e5d1
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-request-quotes"></a>Så här begär du offerter
En inköpsoffert kan användas som ett preliminärt utkast av en inköpsorder, som sedan kan göras om till en inköpsfaktura eller en order.


## <a name="to-create-a-purchase-quote"></a>Så här skapar du en inköpsoffert:
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsofferter** och välj sedan relaterad länk.
2. Skapa ett nytt dokument på samma sätt som du gör en inköpsorder. Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Så här gör du om inköpsofferter till inköpsorder:
När du har accepterat leverantörens offert, kan du omvandla den till en inköpsfaktura eller en order för att behandla inköpet.

1. Öppna en inköpsoffert som är redo att konvertera och välj sedan åtgärden **skapa order**.

Inköpsofferten tas bort från databasen. En inköpsfaktura eller försäljningsorder har skapats baserat på informationen i inköpsofferten där du kan bearbeta inköpet. I fältet **Offertnr** på inköpsfakturan eller inköpsordern kan du ange numret på inköpsofferten som den har skapats från.

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Så här skickar du dokument som e-post](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

