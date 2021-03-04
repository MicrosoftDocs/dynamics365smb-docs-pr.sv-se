---
title: Så här skapar du specialorder | Microsoft Docs
description: Du kan skapa en specialorder för en specifik katalogartikel som inte finns i lagret och som ska levereras till en specifik kund. Leverantören levererar artikeln till distributionslagret så att du sedan kan leverera den till kunden, som en enskild leverans eller tillsammans med andra artiklar på en annan order.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c4549492e118d1b4367e89f2b0169f43ba7f8393
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748249"
---
# <a name="create-special-orders"></a>Skapa specialorder
Du kan skapa en specialorder för en specifik katalogartikel som inte finns i lagret och som ska levereras till en specifik kund. Leverantören levererar artikeln till distributionslagret så att du sedan kan leverera den till kunden, som en enskild leverans eller tillsammans med andra artiklar på en annan order.  

Specialorder anger att inköps- och försäljningsordern är länkade för att säkerställa att den specifika katalogartikeln plockas och levereras till kunden.  

Innan den här funktionen kan användas måste de kund-, leverantörs- och artikelkort som behövs för ordern läggas upp.  

## <a name="to-create-a-special-order"></a>Så här skapar du en specialorder  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**. Skapa och fyll i  försäljningsorder för artikeln. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
3.  Fyll i försäljningsraden på snabbfliken **Rader** . I fältet **Inköpskod**, välj en inköpskod som har fältet **Specialorder** markerat.

    Därefter måste du skapa en inköpsorder från ett inköpsförslag.  
4. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Rekvisitionskalkylark** och välj sedan tillhörande länk.  
5. Välj åtgärden **Specialorder** och väljer sedan åtgärden **Hämta förs.order**.  
6.  På sidan **Hämta förs.order** visar resultat där **Verifikationsnr** är numret på försäljningsordern. Välj **OK**. En inköpskalkylarksrad skapas för artikeln.  
7.  På inköpskalkylarksraden, i fältet **Åtgärdsmeddelande**, väljer du **Ny**.  
8.  På sidan **Inköpsförslag** väljer du åtgärden **Verkställ åtgärdsmeddelande**. Sidan **Skapa inköpsorder** visas. Välj knappen **OK**.  

    Du får meddelande om att inköpsorderna har skapats. Välj **OK**.  

En inköpsorder som skapas som en specialorder för en försäljningsorder respekteras av planeringssystemet när behov och tillgång balanseras. Det innebär att inköpsordern (tillgång) förblir länkad till försäljningsordern (behov) även om inköpsorden kan tillgodose ett annat, tidigare behov. Mer information finns i [Designdetaljer: Partiformningsmetoder](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Du kan använda funktionen Specialorder om artikeln redan har reserverats. Därför, för artiklar som säljs på särskilda order, kontrollera att fältet **Reservera** på artikelkortet har angetts till **alltid**.  

## <a name="see-also"></a>Se även  
[Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md)  
[Försäljning](sales-manage-sales.md)  
[Skapa direktleveranser](sales-how-drop-shipment.md)   
[Designdetaljer: Partiformningsmetoder](design-details-reservation-order-tracking-and-action-messaging.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]