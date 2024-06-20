---
title: Tjänsteorderstatus och reparationsstatus
description: Serviceorderstatus visar reparationsstatus för alla serviceartiklar i serviceordern.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="service-order-status-and-repair-status"></a>Tjänsteorderstatus och reparationsstatus

Fältet **Status** på sidan **Serviceorder** och serviceartikelns reparationsstatus som visas i fältet **Reparationsstatuskod** på sidan **Serviceorder** har ett visst samband i Servicehantering Serviceorderstatus visar reparationsstatus för alla serviceartiklar i serviceordern.  

> [!NOTE]  
> De två statusfälten är inte kopplade till fältet **Släppningsstatus** i huvudet på serviceordern, som styr lagerhanteringen av serviceartiklar.  

När du ändrar en serviceartikels reparationsstatus på serviceordern uppdateras serviceorderns status. För att se den status som anger den generella reparationsstatusen för enskilda serviceartiklar måste du ange följande:  

* Den serviceorderstatus som respektive reparationsstatus är länkad till.  
* Prioritetsnivå för varje serverorderstatusalternativ.  

När du omvandlar en serviceoffert till en serviceorder ändras reparationsstatus för alla serviceartiklar i ordern till **Initial** och serviceorderstatusen till **Förestående**.  

> [!NOTE]
> Innan du kan skapa serviceorder måste du ställa in statusen för reparationer och statusprioriteringar för service. Mer information finns i [Ställa in status för om serviceorder och reparationer](service-order-repair-status.md).

## <a name="specifying-service-order-status-for-repair-status"></a>Ange serviceorderstatus för reparationsstatus

Varje reparationsstatus är länkad till en viss serviceorderstatus. Alternativen för serviceorderstatusen är följande:

* **Förestående**
* **Pågående**
* **Stoppad**
* **Avslutad**

Alternativen för reparationsstatus är följande:

* **Initial**
* **Pågående**
* **Refrerad**
* **Delvist servad**
* **Offert avslutad**
* **Väntar på kund**
* **Reservdel beställd**
* **Reservdel inlevererad**
* **Avslutad**  

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

När du sedan skapar en ny serviceorder och lägger till serviceartiklar i den uppdateras fältet **Prioritet** serviceorderhuvudet baserat på prioriteringarna för serviceartiklarna.  

### <a name="example"></a>Exempel

En typisk fördelning av prioritetsnivå kan se ut så här:  

* Pågående – hög  
* Förestående – medelhög  
* Stoppad – medellåg  
* Färdig – låg  

Om t. ex. en serviceartikel har reparationsstatus **Initial**, länkad till serviceorderstatus **Förestående**, en annan har **På gång**, länkad till servicestatus **På gång**, och en tredje har **Beställt reservdelar**, länkad till servicestatus **Stoppad**, blir den resulterande serviceorderstatus **På gång** eftersom den har högst prioritet.  

## <a name="see-also"></a>Se även

[Ställ in status för tjänsteorder och reparationer](service-order-repair-status.md)  
[Ställa in tjänstehantering](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
