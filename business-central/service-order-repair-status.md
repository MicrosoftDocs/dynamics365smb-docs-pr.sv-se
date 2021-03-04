---
title: 'Så här: ställa in status för serviceorder och reparationer | Microsoft Docs'
description: Du måste ställa in nio olika alternativ för reparationsstatus som anger hur reparationen och underhållet av serviceartiklarna på serviceorder framskrider.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: f9b8fa679254e4886993ee29a1ceba1cf2542cda
ms.sourcegitcommit: 2d2dfb6c3eca1322835f0167dc7dab614346972e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/19/2020
ms.locfileid: "4038466"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Ställ in status för serviceorder och reparationer

Du måste ställa in olika alternativ för reparationsstatus som anger hur reparationen och underhållet av serviceartiklarna på serviceorder framskrider. Du måste skapa åtminstone nio reparationsstatusalternativ som identifierar situationer eller åtgärder som vidtagits då serviceartiklar servas.  

Du kan ange prioriteringsnivåer för alternativen för serviceorderstatus. De fyra prioriteringarna är **Hög**, **Medelhög**, **Medellåg** och **Låg**.  

När du ändrar en serviceartikels reparationsstatus på serviceordern uppdateras serviceorderns status. Varje serviceartikels reparationsstatus är kopplad till serviceorderstatusen. Om serviceartiklarna är kopplade till två eller fler serviceorderstatusalternativ väljs den serviceorderstatus som har högst prioritet.  

Innan du kan ställa in en reparationsstatus måste du ställa in statusprioriteringar för service.

## <a name="to-set-up-service-status-priorities"></a>Så här skapar du servicestatusprioriteter

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Tjänstorderstatus** och välj sedan relaterad länk.  
2. Välj den serviceorderstatus som du vill ange prioritet för.  
3. I fältet **Prioritet** väljer du önskad prioritet för aktuell serviceorderstatus.  

Upprepa steg 2 och 3 tills du har angett en prioritet för vart och ett av de fyra statusalternativen: **Förestående**, **Pågående**, **Avslutad** och **Pausad**.  

## <a name="to-set-up-a-repair-status"></a>Så här skapar du en reparationsstatus

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **reparationsstatus** och välj sedan relaterad länk.
2. Skapa en ny reparationsstatus.  
3. Fyll i fälten **Kod** och **Beskrivning**.  
4. I fältet **serviceorderstatus** väljer du orderstatus att länka reparationsstatusen till. Fältet **Prioritet** visar prioriteten för den serviceorderstatus som du har valt.  
5. Välj en reparationsstatus Du kan bara välja en. Reparationsstatus kan inte kopplas till mer än ett reparationsstatusalternativ.  
6. Välj fältet **Bokföring tillåten** om du vill kunna bokföra serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.  
7. Markera kryssrutan **Förestående status tillåten** om du vill kunna ändra serviceorderns status manuellt till alternativet **Förestående** på serviceorder som innefattar serviceartiklar med aktuell reparationsstatus.  
8. Markera kryssrutorna **Pågående status tillåten**, **Färdig status tillåten** och **Stoppad status tillåten** på samma sätt.

Upprepa dessa stegen för respektive reparationsstatusalternativ som du vill skapa.

## <a name="see-also"></a>Se även

[Serviceorderstatus och reparationsstatus](service-service-order-status-and-repair-status.md)  
[Ställa in tjänstehantering](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]