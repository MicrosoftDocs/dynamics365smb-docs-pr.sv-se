---
title: Ställa in betalningsvillkor
description: I basversionen av Business Central använder du betalningsvillkor för att hantera förfallodatum och kassarabatter.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 82c60333f038f647fa4c9c2bbd68019b9c1f8026
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783803"
---
# <a name="set-up-payment-terms"></a>Ställa in betalningsvillkor

Betalningsvillkor avgör hur du hanterar förfallodatum och kassarabatter. Du kan ange valfritt antal koder för betalningsvillkor och använda datumformler för att definiera betalningsvillkoren. När du registrerar dig för [!INCLUDE [prod_short](includes/prod_short.md)] för första gången erbjuder demonstrationsföretaget några betalsätt som företagen ofta använder. Du kan emellertid lägga till hur många rader du vill.  

Du kan tilldela betalningsvillkor till kunder och leverantörer så att samma villkor alltid används i de försäljnings- inköpsdokument som du skapar för dem. Vid behov kan du ändra villkoren i försäljnings- eller inköpsdokumentet, till exempel om du vill att en viss kund ska betala dig inom 7 dagar i stället för sedvanliga 14 dagar. Standardbetalningsvillkoret som tilldelats leverantören ändras inte. Samma betalningsvillkor finns för försäljnings- och inköpsdokument.

När du sedan bokför en faktura beräknar [!INCLUDE [prod_short](includes/prod_short.md)] kassarabatterna baserat på betalningsvillkoren. Även datumet för kassarabatten, till exempel det senaste datum då kunden kan betala för att erhålla rabatt på betalningen, beräknas vid denna tidpunkt.  

När du bokför en kreditnota kommer på samma sätt [!INCLUDE [prod_short](includes/prod_short.md)] att beräkna eventuella kassarabatter som baseras på betalningsvillkoren. Rabatten för kreditnotor beräknas enligt samma principer som kassarabatter för fakturor. När en kreditnota kopplas till en faktura minskas ett eventuellt kassarabattbelopp för fakturan med kassarabattbeloppet för kreditnotan.  

Om du vill skicka påminnelser om förfallna betalningar måste du ange nivåer och villkor för betalningspåminnelser. Mer information finns i [Ange villkor och nivåer för påminnelser](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Så här definierar du betalningsvillkor

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Betalningsvillkor** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

När du har ställt in betalningsvillkoren tilldelar du dem till kunder och leverantörer. Du kan också tilldela betalningsvillkor till dina betalsätt.  

> [!TIP]
> I basversionen av [!INCLUDE [prod_short](includes/prod_short.md)] stöds inte betalningsvillkor med delbetalningar. Istället måste du använda funktionen för förskottsbetalning. Mer information finns i [Ange Förskottsbetalningar](finance-set-up-prepayments.md).
>
> I vissa länder *kan* du ställa in betalningsvillkor med delbetalningar. Om du vill veta om den här funktionen stöds i ditt land kan du läsa avsnittet **Lokal funktionalitet** i navigeringsrutan till vänster på webbplatsen [Docs.microsoft.com](about-localization.md).

## <a name="see-also"></a>Se även

[Konfigurera betalsätt](finance-payment-methods.md)  
[Konfigurera förskottsbetalningar](finance-set-up-prepayments.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Registrera nya kunder](sales-how-register-new-customers.md)  
[Registrera nya leverantörer](purchasing-how-register-new-vendors.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]