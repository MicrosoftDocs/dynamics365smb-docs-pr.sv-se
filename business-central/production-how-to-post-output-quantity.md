---
title: Batch-bokför produktionsutflöde och körtid
description: Utflödesantalet representerar arbetsförloppet i form av färdig kvantitet och utnyttjad kapacitet för produktions- eller maskingrupp.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4bce7a2e07f9d559df74f4862e9aa841f4cfe6f0
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441603"
---
# <a name="batch-post-output-and-run-times"></a>Batch-bokför utflöde och körtider
Utflödesantalet representerar arbetsförloppet i form av färdig kvantitet och utnyttjad kapacitet för produktions- eller maskingrupp.

Du kan välja använda utflödesjournal för att:
*  Justera lagret i samband med utflödet av slutartiklar från produktion.
*  Registrera kvantiteter och skrot för varje operation i produktionsoperationsföljden.
*  Registrera inställning och körtid för produktions- och maskingrupper.

> [!NOTE]
> Om produktionens operationsföljd används uppdateras inventeringen endast när du bokför utflöde antal vid den senaste operationen.

Med fönstret **Produktionsjournal** kan du utföra samma uppgifter som i fönstret **Utflödesjournal** och samtidigt utföra de relaterade bokföringsuppgifterna för förbrukningen. För mer information, se [Så här registrerar du förbrukning och utflöde för en utsläppt produktionsorderrad](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Om du vill bokföra utflödeskvantiteter och/eller registrera körtider för en eller flera produktionsorderrader
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **utflödesjournal** och väljer sedan relaterad länk.  
2. Fyll i fälten med data om produktionsorden och utdata och/eller körtid. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Du kan använda funktionen expandera **Expandera oper.följd** när du vill generera journalrader från produktionsorder.
  
4. Om operationen har slutförts, välj fältet **FÄRDIG**.  
5. Välj åtgärden **Bokför** om du vill bokföra operationer. 
 
Kapacitetstransaktioner uppdateras för de använda produktions- eller maskingrupperna med information om tid och kvantitet av produktion och kassation. Om du har bokfört den sista operationen kommer artikeln att läggas till i lagret. 

## <a name="see-also"></a>Se även  
[Bokföra kassation manuellt](production-how-to-post-scrap.md)
[Återför utflödesbokföring](production-how-to-reverse-output-posting.md)
[Tillverkning](production-manage-manufacturing.md)    
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
