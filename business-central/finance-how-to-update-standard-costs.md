---
title: Så här kan du uppdatera standardkostnader | Microsoft Docs
description: Du måste regelbundet uppdatera standardkostnader för komponenter och överföra de nya kostnaderna till den överordnade artikeln.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7fb47fe72d323182973e970867ad6648652bc62f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183242"
---
# <a name="update-standard-costs"></a>Uppdatera standardkostnader
Du måste regelbundet uppdatera standardkostnader för komponenter och överföra de nya kostnaderna till den överordnade artikeln. Processen består typiskt av följande fyra steg:  

1.  Uppdatera kostnader på komponent- och kapacitetsnivå. Mer information finns i batch-jobbet **Föreslå artikelstandardkostnad**.  
2.  Konsolidera och summera komponent- och kapacitetskostnader för att beräkna den totala produktions- eller monteringskostnaden för artiklarna.  
3.  Använd standardkostnaderna som angavs när du körde de föregående batch-jobben. Standardkostnaderna börjar inte gälla förrän de implementeras. Mer information finns i Implementera standardkostnadsändringar.  
4.  Inför ändringarna för att uppdatera fältet **Styckkostnad** för artikelkortet och utföra lageromvärderingen. Mer information finns i [Omvärdera lager](inventory-how-revalue-inventory.md).  

Mer information finns i [Om att beräkna standardkostnad](finance-about-calculating-standard-cost.md).  
## <a name="to-update-standard-costs"></a>Uppdatera standardkostnader  
1.  Kör batch-jobbet **Justera kost. - artikeltrans.**  
2.  Kör batch-jobbet **Bokför lagerkostnad i redov.**  
3.  Öppna **Standardkostnadsformulär** och använd en eller flera av följande funktioner:  

    1.  Kör batch-jobbet **Föreslå artikelstandardkostnad**.  
    2.  Granska resultaten och gör nödvändiga ändringar.  
    3.  Kör batch-jobbet **Föreslå standardkostnad för kapacitet**.  
    4.  Granska resultaten och gör nödvändiga ändringar.
    5. Kör batch-jobbet **Uppsummerad standardkostnad**.
    6.  Granska resultaten och gör nödvändiga ändringar.
    7.  Kör batch-jobbet **Implementera standardkostnadsändringar**.  
4.  Granska och bokför sidan **Omvärderingsjournal** , vilken har fyllts på med transaktioner från föregående steg i den här processen.  

## <a name="see-also"></a>Se även  
 [Om beräkning av standardkostnad](finance-about-calculating-standard-cost.md)   
 [Hantera lagerkostnader](finance-manage-inventory-costs.md)   
 [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md) [Finans](finance.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
