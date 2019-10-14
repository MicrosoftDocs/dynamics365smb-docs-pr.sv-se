---
title: Tjänsteorderstatus och reparationsstatus | Microsoft Docs
description: Fältet Status på sidan Serviceorder och serviceartikelns reparationsstatus som visas i fältet Reparationsstatuskod på sidan Serviceorder har ett visst samband i modulen Servicehantering Serviceorderstatus visar reparationsstatus för alla serviceartiklar i serviceordern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f55e33490bb70fae2b37eda6fe0b43f982fe8493
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311602"
---
# <a name="service-order-status-and-repair-status"></a>Tjänsteorderstatus och reparationsstatus
Fältet **Status** på sidan **Serviceorder** och serviceartikelns reparationsstatus som visas i fältet **Reparationsstatuskod** på sidan **Serviceorder** har ett visst samband i Servicehantering Serviceorderstatus visar reparationsstatus för alla serviceartiklar i serviceordern.  

> [!NOTE]  
>  De två statusfälten är inte kopplade till fältet **Släppningsstatus** i huvudet på serviceordern, som styr lagerhanteringen av serviceartiklar.  

 När du ändrar en serviceartikels reparationsstatus på serviceordern uppdateras serviceorderns status. För att se den status som anger den generella reparationsstatusen för enskilda serviceartiklar måste du ange följande:  

* Den serviceorderstatus som respektive reparationsstatus är länkad till. Mer information finns i Tjänsteorderstatus.  
* Prioritetsnivå för varje serverorderstatusalternativ. Mer information finns i Prioritet.  

 När du omvandlar en serviceoffert till en serviceorder ändras reparationsstatus för alla serviceartiklar i ordern till **Initial** och serviceorderstatusen till **Förestående**.  

## <a name="specifying-service-order-status-for-repair-status"></a>Ange serviceorderstatus för reparationsstatus  
Varje reparationsstatus är länkad till en viss serviceorderstatus. Alternativen för serviceorderstatus är **Förestående**, **På gång**, **Stoppad** och **Avslutad**. Det finns nio olika alternativ för reparationsstatus: **Initial**, **På gång**, **Hänvisad**, **Delvis servad**, **Offert avslutad**, **Väntar på kund**, **Beställt reservdelar**, **Reservdelar inlevererade** och **Avslutad**.  

### <a name="pending"></a>Förestående  
Tjänsteorderstatusen **Förestående** anger att servicen kan inledas eller fortsätta när som helst. Därför kan fyra av alternativen för reparationsstatus, nämligen **Initial**, **Hänvisad**, **Delvis servad** och **Reservdelar inlevererade**, alla länkas till den här serviceorderstatusen.  

### <a name="in-process"></a>Pågående  
Tjänsteorderstatusen **På gång** anger att servicen pågår. Därför kan två av alternativen för reparationsstatus, nämligen **På gång** och **Beställt reservdelar**, länkas till den här serviceorderstatusen. Om du länkar statusen **Beställt reservdelar** till servicestatusen **På gång** måste du även länka statusen **Beställt reservdelar** till den här serviceorderstatusen.  

### <a name="on-hold"></a>Stoppad  
Tjänsteorderstatusen **Stoppad** anger att servicen tillfälligt har stoppats i väntan på svar från kunden eller reservdelar innan servicen kan inledas. Därför kan tre av alternativen för reparationsstatus, nämligen **Offert avslutad**, **Beställt reservdelar** och **Väntar på kund**, alla länkas till den här serviceorderstatusen.  

### <a name="finished"></a>Avslutad  
Tjänsteorderstatusen **Avslutad** anger att servicen har slutförts. Därför är reparationsstatusen **Avslutad** länkad till den här statusen.  

## <a name="assigning-priority-to-service-order-status"></a>Tilldela en serviceorderstatus prioritet  
När du ändrar reparationsstatus för en serviceartikel identifieras de serviceorderstatusalternativ som är länkade till olika reparationsstatusalternativ för alla serviceartiklar i ordern. Om serviceartiklarna är kopplade till två eller fler serviceorderstatusalternativ väljs den serviceorderstatus som har högst prioritet.  

Du måste välja vilken serviceorderstatus som innehåller viktigast information om serviceorderstatusen och tilldela den högst prioritet o.s.v.  

### <a name="example"></a>Exempel  
En typisk fördelning av prioritetsnivå kan se ut så här:  

* Pågående – hög  
* Förestående – medelhög  
* Stoppad – medellåg  
* Färdig – låg  

Om t.ex. en serviceartikel har reparationsstatus **Initial**, länkad till serviceorderstatus **Förestående**, en annan har **På gång**, länkad till servicestatus **På gång**, och en tredje har **Beställt reservdelar**, länkad till servicestatus **Stoppad**, blir den resulterande serviceorderstatus **På gång** eftersom den har högst prioritet.  

## <a name="see-also"></a>Se även  
[Ställ in status för tjänsteorder och reparationer](service-order-repair-status.md)  
[Ställa in tjänstehantering](service-setup-service.md)  
