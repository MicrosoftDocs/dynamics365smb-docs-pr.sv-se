---
title: Så här bokför du kapaciteter | Microsoft Docs
description: I kapacitetsjournalen bokför du förbrukade kapaciteter som inte kopplats till produktionsordern. Underhållsarbete måste till exempel kopplas till kapacitet, men inte till en produktionsorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8f41a5033c79ec500a635d27f8296d01d895ed27
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787933"
---
# <a name="post-capacities"></a>Bokför kapaciteter
I kapacitetsjournalen bokför du förbrukade kapaciteter som inte kopplats till produktionsordern. Underhållsarbete måste till exempel kopplas till kapacitet, men inte till en produktionsorder.  

## <a name="to-post-capacities"></a>Så här bokför du kapaciteter  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **kapacitetsjournaler** och välj sedan relaterad länk.  
2.  Fyll i fälten **Bokföringsdatum** och **Verifikationsnummer** .  
3.  I fältet **Typ** anger du kapacitetstypen, endera **Maskingrupp** eller **Produktionsgrupp**, som du bokför.  
4.  I fältet **Nr.** skriv numret på den artikel som har beställts.  
5.  Ange relevanta uppgifter i övriga fält, t. ex. **Starttid**, **Sluttid**, **Antal** och **Kassation**.  
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


[!INCLUDE[footer-include](includes/footer-banner.md)]