---
title: 'Så här: Aktivera plockning med FEFO | Microsoft Docs'
description: FEFO-metoden (First-Expired-First-Out) är en sorteringsmetod som säkerställer att de äldsta artiklar, de med de tidigaste utgångsdatumen, plockas först.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a5e25c9df3ccd98436945b0070773d5b48eb54ac
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "917895"
---
# <a name="enable-picking-items-by-fefo"></a>Aktivera plockning av artiklar med FEFO
FEFO-metoden (First-Expired-First-Out) är en sorteringsmetod som säkerställer att de äldsta artiklarna - de med tidigast utgångsdatum - plockas först.  

 Den här funktionen fungerar bara, när dessa villkor är uppfyllt:  

-   Artikel måste ha en serie-/partinummer.  
-   På artikelns artikelspårningskod har angetts, fältet **SN specifik spårning för dist.lager** , eller **Parti specifik spårning distr.lager** måste väljas.  
-   Artikeln måste bokföras till lagret med ett utgångsdatum.  
-   På lagerställekortet måste kryssrutan **Begär plockning** vara markerad.  
-   Kryssrutan **Plocka enligt FEFO** på lagerställekortet måste vara markerat.  
-   På lagerställekortet måste kryssrutan **Lagerplats ska finnas** vara markerad.  

 När alla villkor uppfylls, sorteras serie-/partinumrerade artiklar som ska plockas med de äldsta första alla plockningar och transporter, utom artiklar som använder SN-närmare visst eller partispecifik spårning.  

> [!NOTE]  
> Om någon serie-/partinumrerade artiklar använder specifik spårning, är de respekterade först och under dem, listas de återstående, icke-specifika serie-/partinummer enligt FEFO.
<br /><br />
Om två serie-/partinumrerade artiklar har samma utgångsdatum, väljs artikeln med det lägsta serie - eller partinummer.
<br /><br />
När du plockar serie-/partinumrerade artiklar på lagerplatser som har ställs in för dirigerad artikelinförsel och plockning, plockas bara kvantiteter på lagerplatser av typen *Plock* enligt FEFO.  
<br /><br />
Om du vill aktivera transporter enligt FEFO antingen på sidan **Lagerförflyttning** eller på sidan **Transportförslag**, måste du lämna fältet **Från lagerplats** tomt.  
<br /><br />
Om fältet **Endast utgångsbokföring** är markerat kommer endast artiklar som inte har förfallit att tas med i plockningen. Detta gäller även om du inte använder plockning enligt FEFO.

## <a name="see-also"></a>Se även  
[Plocka artiklar](warehouse-pick-items.md)   
[Plocka artiklar för utleverans från dist.lager](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Plocka artiklar med lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
