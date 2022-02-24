---
title: Designdetaljer - Integrering med lager | Microsoft Docs
description: Lagerledningsmodulen och lagermodulen interagerar med varandra i inventeringsjournalen och i lager- eller distributionslagerjustering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: bbc9c0e55041f4584ae7609f727179737adaa041
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185354"
---
# <a name="design-details-integration-with-inventory"></a>Designdetaljer: Integrering med lager
Lagerledningsmodulen och lagermodulen interagerar med varandra i inventeringsjournalen och i lager- eller distributionslagerjustering.  
  
## <a name="physical-inventory"></a>Fysiskt lager  
 Sidan **Dist.lager inventeringsjournal** används med sidan **Inventeringsjournal** för alla avancerade distributionslagerplatser. Lagret på lagerplatsnivå beräknas, och en utskriven lista levereras till lagerpersonalen. Listan visar vilka artiklar i vilka lagerplatser som ska inventeras.  
  
 Lagerpersonalen anger det räknade antalet på sidan **Dist.lager inventeringsjournal** och bokför sedan journalen.  
  
 Om det inventerade antalet är större än antalet på journalraden bokförs en transport för skillnaden från standardjusteringslagerplatsen till den inventerade lagerplatsen. Det ökar antalet på den inventerade lagerplatsen och minskar antalet i standardjusteringlagerplatsen.  
  
 Om det inventerade antalet är mindre än antalet på journalraden bokförs en transport för skillnaden från den inventerade lagerplatsen till standardjusteringslagerplatsen. Det minskar antalet på den inventerade lagerplatsen och ökar antalet i standardjusteringlagerplatsen.  
  
 I avancerad lagerkonfiguration hämtas värdet i fältet **Beräknat antal** från artikeltransaktioner, och värdet i fältet **Antal inventerat** hämtas från distributionslagertransaktioner exklusive justeringslagerplatsinnehåll. Fältet **Antal** anger skillnaden mellan de första två fälten, som ska vara lika med innehållet på justeringslagerplatsen.  
  
 När du bokför inventeringjournalen uppdateras lagret och standardjusteringlagerplatsen.  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a>Distributionslagerjusteringar till artikeltransaktioner  
 Du kan använda sidan **Artikeljournal** och funktionen **Beräkna dist.lager justering** för att justera lagret i artikeltransaktioner i enlighet med en justering som har gjorts av objektantalet på en lagerplats i distributionslagret. För att skapa en koppling mellan lagret och distributionslagret måste du definiera en standardjusteringlagerplats per lagerställe.  
  
 Standardjusteringlagerplatsen registrerar artiklar i distributionslagret när du bokför en ökning för lagret. Om du bokför en minskning, minskas antalet på lagerplatsen också. I båda fallen skapas artikeltransaktioner och distributionslagerposter.  
  
> [!NOTE]  
>  Justeringslagerplatsen inkluderas inte i dispositionsberäkningarna.  
  
 Om du vill justera lagerplatsinnehåll kan du använda distributionslagerartikeljournalen, från vilken du kan ange artikelnummer, zonkoden, lagerplatskod och antal som du vill justera.  
  
 Om du anger ett positivt antal och bokför raden ökar lagret som lagras på lagerplatsen, och antalet på standardjusteringslagerplatsen minskar på motsvarande sätt.  
  
## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)   
 [Designdetaljer: Disposition i distributionslagret](design-details-availability-in-the-warehouse.md)