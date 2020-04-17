---
title: Ställa in betalningssätt | Microsoft Docs
description: Du kan använda betalningsmetoder, till exempel, kontrollera, banköverföring, kontant eller PayPal, för att ange hur försäljnings- och inköpsfakturor ska betalas.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 708ae474b15724e151cba367842091763544a434
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182978"
---
# <a name="defining-payment-methods"></a>Definiera betalningssätt
Betalningssätt definierar hur du föredrar att kunderna betalar dig och hur du vill betala dina leverantörer. Metoden kan variera för varje kund eller leverantör. Exempel på typiska betalningssätt är **bank**, **kontanter**, **check** eller **konto**.

Du kan tilldela ett betalningssätt till kunder och leverantörer så att samma metod alltid används på de försäljningsorderrader och inköpsdokument som du skapar dem för. Om det behövs kan du ändra metoden för försäljnings- eller inköpsdokument. Till exempel om du vill betala en viss inköpsfaktura kontant och inte med checkar. Standardbetalningsmetoden som tilldelats leverantören ändras inte.

Samma betalningssätt används för försäljnings- och inköpsdokument. Till exempel ett _kontant_ betalningssätt används både när du gör betalningar och när du tar emot dem. [!INCLUDE[d365fin](includes/d365fin_md.md)] vet att när du skapar en försäljningsfaktura förväntar du dig att erhålla betalning och motsatsen för inköpsfakturor.

Kreditnotor för returer är emellertid undantag eftersom pengar flödar i motsatt riktning från dig till din kund och från din leverantör till dig. Därför tilldelas inte ett standardbetalningssätt för kreditnotor. Det finns emellertid en lösning om du har angett betalningsvillkoren för kunden eller leverantören. Även om fältet **Beräkna kassarabatt i kr.nota** inte är avsett för detta, om du väljer den här kryssrutan på sidan **betalningsvillkor** kommer ett standardbetalningssätt att läggas till när du skapar en kreditnota. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a>Så här definierar du betalningssätt:
[!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller några betalningssätt som företag använder ofta. Du kan emellertid lägga till hur många rader du vill.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **betalningssätt** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Så här kopplar du betalningssätt till en kund eller leverantör
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kund** eller **Leverantör** och välj sedan relaterad länk.
2. I fältet **betalningssättkod**, välj metoden som ska användas som standard för kunden eller leverantören.

## <a name="see-also"></a>Se även
[Registrera nya kunder](sales-how-register-new-customers.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
