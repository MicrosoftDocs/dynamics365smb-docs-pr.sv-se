---
title: Utföra produktion
description: När behov har planerats och material har tagits utt enligt produktionsstrukturerna kan de faktiska produktionsoperationerna inledas och sedan genomföras i den ordning som definieras av verksamhetsföljden för produktionsorder.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5406, 5407, 5728, 8903, 9011, 9012, 9013, 9041, 9044, 9047, 9323, 9324, 9325, 9326, 9327, 99000784, 99000785'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="manufacturing"></a>Produktion

> [!NOTE]
> Funktionen som beskrivs i det här avsnittet och underavsnitt visas endast i användargränssnittet om du har **Premium**-upplevelsen. Mer information finns i [ändra vilka funktioner som visas](ui-experiences.md).

När behov har planerats och material har tagits utt enligt produktionsstrukturerna kan de faktiska produktionsoperationerna inledas och sedan genomföras i den ordning som definieras av verksamhetsföljden för produktionsorder.  

En viktig del i att genomföra produktionen, ur systemsynvinkel, är att bokföra produktionsutflöde i databasen för att rapportera förlopp och uppdatera lagret med färdiga artiklar. Du kan bokföra utflöde manuellt genom att fylla i och bokföra journalrader efter produktionsoperationerna. Du kan också göra det automatiskt genom bokföra framåt. I så fall bokförs materialförbrukning automatiskt tillsammans med utflödet när produktionsordern ändras eller slutförs.  

I stället för att använda batch-journalen för utflödesbokföring för flera produktionsorder, kan du använda sidan **Produktionsjournal** när du bokför förbrukning och/eller utflöde för en produktionsorderrad.

Innan du kan skapa artiklar måste du göra olika inställningar, till exempel för produktionsgrupper, verksamhetsföljder och produktionsstrukturer. Mer information finns i [Konfigurera tillverkning](production-configure-production-processes.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Förstå hur produktionsorder fungerar.|[Om produktionsorder](production-about-production-orders.md)|
|Skapa produktionsorder manuellt.|[Skapa produktionsorder](production-how-to-create-production-orders.md)|
|Lägga ut alla eller valda operationer i en produktionsorder på en underleverantör.|[Lägga ut legotillverkning för produktion](production-how-to-subcontract-manufacturing.md)|
|Registrera och bokföra produktionsutflödet, tillsammans med material- och tidsförbrukningen, för en enskild släppt produktionsorderrad.|[Bokför förbrukning och utflöde för en utsläppt produktionsorderrad](production-how-to-register-consumption-and-output.md)|  
|Batch-bokföra komponentkvantiteten som används per operation i en journal som kan behandla flera planerade produktionsorder.|[Batch-bokför förbrukning](production-how-to-post-consumption.md)|
|Bokför kvantiteten för färdiga artiklar och tiden som spenderats per operation i en journal som kan behandla flera släppta produktionsorder.|[Batch-bokför utflöde och körtider](production-how-to-post-output-quantity.md)|
|Ångra utdata, till exempel på grund av ett datafel inträffade och felaktiga belopp.  |[Återföra bokföring av utflöde](production-how-to-reverse-output-posting.md)|  
|Bokföra det antal artiklar som producerats i varje slutförd operation, men som inte räknas som färdigt utflöde utan som kasserat material.|[Bokför kassation](production-how-to-post-scrap.md)|
|Visa beläggningen på fabriken till följd av planerade och släppta produktionsorder.|[Visa beläggning på produktions- och maskingrupper](production-how-to-view-the-load-on-work-centers.md)|  
|Använda sidan **Kapacitetsjournal** för att bokföra förbrukade kapaciteter som inte tilldelats en produktionsorder, till exempel underhållsarbete.|[Bokför kapaciteter](production-how-to-post-capacities.md)|  
|Beräkna och justera kostnaden för färdiga produktionsartiklar och förbrukade komponenter för avstämning.|[Om kostnader för färdiga produktionsorder](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Se även

[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
