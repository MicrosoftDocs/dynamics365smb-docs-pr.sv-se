---
title: "Utföra produktion | Microsoft Docs"
description: "När behov har planerats och material har tagits utt enligt produktionsstrukturerna kan de faktiska produktionsoperationerna inledas och sedan genomföras i den ordning som definieras av operationsföljden för produktionsorder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: e27ceb91b25669a31d95256385cb7e5acd9160bd
ms.contentlocale: sv-se
ms.lasthandoff: 09/27/2017

---
# <a name="manufacturing"></a>Produktion
När behov har planerats och material har tagits utt enligt produktionsstrukturerna kan de faktiska produktionsoperationerna inledas och sedan genomföras i den ordning som definieras av operationsföljden för produktionsorder.  

En viktig del i att genomföra produktionen, ur systemsynvinkel, är att bokföra produktionsutflöde i databasen för att rapportera förlopp och uppdatera lagret med färdiga artiklar. Du kan bokföra utflöde manuellt genom att fylla i och bokföra journalrader efter produktionsoperationerna. Du kan också göra det automatiskt genom bokföra framåt. I så fall bokförs materialförbrukning automatiskt tillsammans med utflödet när produktionsordern ändras eller slutförs.  

I stället för att använda batch-journalen för utflödesbokföring för flera produktionsorder, kan du använda fönstret **Produktionsjournal** när du bokför förbrukning och/eller utflöde för en produktionsorderrad.

Innan du kan skapa artiklar måste du göra olika inställningar, till exempel för produktionsgrupper, operationsföljder och produktionsstrukturer. Mer information finns i [Konfigurera tillverkning](production-configure-production-processes.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Förstå hur produktionsorder fungerar.|[Om produktionsorder](production-about-production-orders.md)|
|Skapa produktionsorder manuellt.|[Så här skapar du ett produktionsorder](production-how-to-create-production-orders.md)|
|Lägga ut alla eller valda operationer i en produktionsorder på en underleverantör.|[Så här lägger du ut legotillverkning för produktion](production-how-to-subcontract-manufacturing.md)|
|Registrera och bokföra produktionsutflödet, tillsammans med material- och tidsförbrukningen, för en enskild släppt produktionsorderrad.|[Så här bokför du förbrukning och utflöde för en utsläppt produktionsorderrad.](production-how-to-register-consumption-and-output.md)|  
|Batch-bokföra komponentkvantiteten som används per operation i en journal som kan behandla flera planerade produktionsorder.|[Så här: batch-bokföra förbrukning](production-how-to-post-consumption.md)|
|Bokför kvantiteten för färdiga artiklar och tiden som spenderats per operation i en journal som kan behandla flera släppta produktionsorder.|[Så här: Batch-bokför utflöde och körtid](production-how-to-post-output-quantity.md)|  
|Bokföra det antal artiklar som producerats i varje slutförd operation, men som inte räknas som färdigt utflöde utan som kasserat material.|[Så här bokför du kassationen:](production-how-to-post-scrap.md)|
|Visa beläggningen på fabriken till följd av planerade och släppta produktionsorder.|[Så här visar du beläggning på produktions- och maskingrupper](production-how-to-view-the-load-on-work-centers.md)|      
|Använda fönstret **Kapacitetsjournal** för att bokföra förbrukade kapaciteter som inte tilldelats en produktionsorder, till exempel underhållsarbete.|[Så här bokför du kapaciteter](production-how-to-post-capacities.md)|  
|Beräkna och justera kostnaden för färdiga produktionsartiklar och förbrukade komponenter för avstämning.|[Om kostnader för färdiga produktionsorder](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Se även  
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)      
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

