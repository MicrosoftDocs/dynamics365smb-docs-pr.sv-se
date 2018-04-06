---
title: Designdetaljer - Integrering med lager | Microsoft Docs
description: Lagerledningsmodulen och lagermodulen interagerar med varandra i inventeringsjournalen och i lager- eller distributionslagerjustering.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 00a12f3f2203ed3b22cfee1af6aa8f155ca5fe4b
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-integration-with-inventory"></a>Designdetaljer: Integrering med lager
Lagerledningsmodulen och lagermodulen interagerar med varandra i inventeringsjournalen och i lager- eller distributionslagerjustering.  
  
## <a name="physical-inventory"></a>Physical Inventory  
 Fönstret **Dist.lager inventeringsjournal** används med fönstret **Inventeringsjournal** för alla avancerade distributionslagerplatser. Lagret på lagerplatsnivå beräknas, och en utskriven lista levereras till lagerpersonalen. Listan visar vilka artiklar i vilka lagerplatser som ska inventeras.  
  
 Lagerpersonalen anger det räknade antalet i fönstret **Dist.lager inventeringsjournal** och bokför sedan journalen.  
  
 Om det inventerade antalet är större än antalet på journalraden bokförs en transport för skillnaden från standardjusteringslagerplatsen till den inventerade lagerplatsen. Det ökar antalet på den inventerade lagerplatsen och minskar antalet i standardjusteringlagerplatsen.  
  
 Om det inventerade antalet är mindre än antalet på journalraden bokförs en transport för skillnaden från den inventerade lagerplatsen till standardjusteringslagerplatsen. Det minskar antalet på den inventerade lagerplatsen och ökar antalet i standardjusteringlagerplatsen.  
  
 I avancerad lagerkonfiguration hämtas värdet i fältet **Beräknat antal** från artikeltransaktioner, och värdet i fältet **Antal inventerat** hämtas från distributionslagertransaktioner exklusive justeringslagerplatsinnehåll. Fältet **Antal** anger skillnaden mellan de första två fälten, som ska vara lika med innehållet på justeringslagerplatsen.  
  
 När du bokför inventeringjournalen uppdateras lagret och standardjusteringlagerplatsen.  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a>Distributionslagerjusteringar till artikeltransaktioner  
 Du kan använda fönstret **Artikeljournal** och funktionen **Beräkna dist.lager justering** för att justera lagret i artikeltransaktioner i enlighet med en justering som har gjorts av objektantalet på en lagerplats i distributionslagret. För att skapa en koppling mellan lagret och distributionslagret måste du definiera en standardjusteringlagerplats per lagerställe.  
  
 Standardjusteringlagerplatsen registrerar artiklar i distributionslagret när du bokför en ökning för lagret. Om du bokför en minskning, minskas antalet på lagerplatsen också. I båda fallen skapas artikeltransaktioner och distributionslagerposter.  
  
> [!NOTE]  
>  Justeringslagerplatsen inkluderas inte i dispositionsberäkningarna.  
  
 Om du vill justera lagerplatsinnehåll kan du använda distributionslagerartikeljournalen, från vilken du kan ange artikelnummer, zonkoden, lagerplatskod och antal som du vill justera.  
  
 Om du anger ett positivt antal och bokför raden ökar lagret som lagras på lagerplatsen, och antalet på standardjusteringslagerplatsen minskar på motsvarande sätt.  
  
## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)   
 [Designdetaljer: Disposition i distributionslagret](design-details-availability-in-the-warehouse.md)
