---
title: Batch-bokför produktionsutflöde och körtid
description: Utflödesantalet representerar arbetsförloppet i form av färdig kvantitet och utnyttjad kapacitet för produktions- eller maskingrupp.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000773, 99000778, 99000823, 99000827'
ms.date: 03/08/2023
ms.author: bholtorf
---
# <a name="batch-post-output-and-run-times"></a>Batch-bokför utflöde och körtider

Utflödesantalet representerar arbetsförloppet i form av färdig kvantitet och utnyttjad kapacitet för produktions- eller maskingrupp.

Du kan välja använda utflödesjournal för att:

* Justera lagret i samband med utflödet av slutartiklar från produktion.
* Registrera kvantiteter och skrot för varje operation i produktionsoperationsföljden.
* Registrera inställning och körtid för produktions- och maskingrupper.

> [!NOTE]
> Om produktionens operationsföljd används uppdateras inventeringen endast när du bokför utflöde antal vid den senaste operationen.

På sidan **Produktionsjournal** kan du utföra samma uppgifter som på sidan **Utflödesjournal** och även bokföra förbrukningsuppgifter. För mer information, se [Så här registrerar du förbrukning och utflöde för en utsläppt produktionsorderrad](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Om du vill bokföra utflödeskvantiteter och/eller registrera körtider för en eller flera produktionsorderrader

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **utflödesjournal** och väljer sedan relaterad länk.  
2. Fyll i fälten med data om produktionsorden och utdata och/eller körtid. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Du kan använda funktionen expandera **Expandera oper.följd** när du vill generera journalrader från produktionsorder.
  
3. Om operationen har slutförts, välj fältet **FÄRDIG**.  
4. Välj åtgärden **Bokför** om du vill bokföra operationer.

    Kapacitetstransaktioner uppdateras för de använda produktions- eller maskingrupperna med information om tid och kvantitet av produktion och kassation. Om du har bokfört den sista operationen kommer artikeln att läggas till i lagret.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-also"></a>Se även

[Bokför kassation manuellt](production-how-to-post-scrap.md)
[Återför utflödesbokföring](production-how-to-reverse-output-posting.md)
[Tillverkning](production-manage-manufacturing.md)
[Konfigurera tillverkning](production-configure-production-processes.md)  
[Planerad](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
