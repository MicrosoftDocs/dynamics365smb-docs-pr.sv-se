---
title: Så här bokför du kapaciteter | Microsoft Docs
description: I kapacitetsjournalen bokför du förbrukade kapaciteter som inte kopplats till produktionsordern. Underhållsarbete måste till exempel kopplas till kapacitet, men inte till en produktionsorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2fa0038745664c269d6d471c6d9373a9174df201
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759198"
---
# <a name="post-capacities"></a>Bokför kapaciteter
I kapacitetsjournalen bokför du förbrukade kapaciteter som inte kopplats till produktionsordern. Underhållsarbete måste till exempel kopplas till kapacitet, men inte till en produktionsorder.  

## <a name="to-post-capacities"></a>Så här bokför du kapaciteter  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **kapacitetsjournaler** och välj sedan relaterad länk.  
2.  Fyll i fälten **Bokföringsdatum** och **Verifikationsnummer** .  
3.  I fältet **Typ** anger du kapacitetstypen, endera **Maskingrupp** eller **Produktionsgrupp**, som du bokför.  
4.  I fältet **Nr.** skriv numret på den artikel som har beställts.  
5.  Ange relevanta uppgifter i övriga fält, t.ex. **Starttid**, **Sluttid**, **Antal** och **Kassation**.  
6.  Välj åtgärden **Bokför** om du vill bokföra fakturan.  

## <a name="to-view-work-center-ledger-entries"></a>Så här visar du produktionsgruppstransaktioner  
På sidan **produktionsgruppkort** och **maskingruppkort** kan du se bokförd kapacitet till följd av avslutade produktionsorder.    
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **produktionsgrupper** och välj sedan relaterad länk.  
2.  Öppna relevant **produktionsgrupp** kort i listan och klicka på åtgärden **Kapacitetstransaktioner**.  

På sidan **Kapacitetstransaktioner** visas de transaktioner som bokförts från produktionsgruppen i den ordning de bokförts i.   

## <a name="see-also"></a>Se även  
[Produktion](production-manage-manufacturing.md)    
[Ställa in Produktion](production-configure-production-processes.md)  
[Planerad](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
