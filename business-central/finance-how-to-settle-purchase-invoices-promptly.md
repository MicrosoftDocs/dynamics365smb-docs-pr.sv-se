---
title: Betala inköpsfakturor snabbt
description: Om du vill betala leverantören kontant eller med check kan all nödvändig bokföring göras när du bokför fakturan.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: fb442c7b1e9e7bdcb727ca6de157657e370e254f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746847"
---
# <a name="settle-purchase-invoices-promptly"></a>Betala inköpsfakturor snabbt

Om du vill betala leverantören kontant eller med check kan du bokföra betalningen när du bokför fakturan.  

> [!NOTE]  
> Om du ofta betalar inköpsfakturor kontant, via check eller banöverföring, kan det vara praktiskt att definiera ett särskilt betalningssätt för ett balanskonto och ange detta i fältet **Betalningssätt** på leverantörskortet. Hädanefter infogas motkontonumret i fakturahuvudet automatiskt när du skapar en ny faktura. Mer information finns i [Definiera betalningssätt](finance-payment-methods.md).  

## <a name="to-settle-purchase-invoices-promptly"></a>Så här gör du för att snabbt betala inköpsfakturor:

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Inköpsfakturor** och välj sedan tillhörande länk.  
2. Välj åtgärden **Ny**.  
3. Ange numret på redovisningskassakontot eller bankkontot i fältet **Motkonto** om du vill betala kontant eller via banköverföring .  

> [!IMPORTANT]  
> Fälten **Motkontotyp** och **Motkonto** ingår inte i standardlayouten för fakturahuvudet. För att du ska kunna bokföra betalningen av en faktura måste du kontakta en Microsoft-partner som kan lägga till fälten via kod.  
>
> Denna anpassning krävs endast om du inte anger balanskonton för betalningssätten enligt beskrivningen ovan.

## <a name="see-also"></a>Se även

[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]