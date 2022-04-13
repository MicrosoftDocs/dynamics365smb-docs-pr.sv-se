---
title: Bokför kapaciteter
description: Bokföra förbrukade kapaciteter som inte har tilldelats produktions ordern i kapacitetsjournalen och visa bokförda kapaciteter på sidan kapacitetstransaktioner.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5832, 99000802, 99000820
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 2897ed44eb9df8e0bc8f6a4f6a83a9e18175ecc7
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516750"
---
# <a name="post-capacities"></a>Bokför kapaciteter
I kapacitetsjournalen bokför du förbrukade kapaciteter som inte kopplats till produktionsordern. Underhållsarbete måste till exempel kopplas till kapacitet, men inte till en produktionsorder.  

## <a name="to-post-capacities"></a>Så här bokför du kapaciteter  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kapacitetsjournal** och väljer sedan relaterad länk.  
2.  Fyll i fälten **Bokföringsdatum** och **Verifikationsnummer** .  
3.  I fältet **Typ** anger du kapacitetstypen, endera **Maskingrupp** eller **Produktionsgrupp**, som du bokför.  
4.  I fältet **Nr.** skriv numret på den artikel som har beställts.  
5.  Ange relevanta uppgifter i övriga fält, t. ex. **Starttid**, **Sluttid**, **Antal** och **Kassation**.  
6.  Välj åtgärden **Bokför** om du vill bokföra fakturan.  

## <a name="to-view-work-center-ledger-entries"></a>Så här visar du produktionsgruppstransaktioner  
På sidan **produktionsgruppkort** och **maskingruppkort** kan du se bokförd kapacitet till följd av avslutade produktionsorder.    
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **produktionsgrupper** och väljer sedan relaterad länk.  
2.  Öppna relevant **produktionsgrupp** kort i listan och klicka på åtgärden **Kapacitetstransaktioner**.  

På sidan **Kapacitetstransaktioner** visas de transaktioner som bokförts från produktionsgruppen i den ordning de bokförts i.   

## <a name="see-also"></a>Se även  
[Produktion](production-manage-manufacturing.md)    
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]