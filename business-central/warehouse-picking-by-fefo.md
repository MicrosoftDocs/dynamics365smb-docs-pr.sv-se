---
title: 'Så här: Aktivera plockning med FEFO | Microsoft Docs'
description: FEFO-metoden (First-Expired-First-Out) är en sorteringsmetod som säkerställer att de äldsta artiklar, de med de tidigaste utgångsdatumen, plockas först.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3a47c9daeeab036055a0644e1b389735f7440106
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784073"
---
# <a name="enable-picking-items-by-fefo"></a>Aktivera plockning av artiklar med FEFO
FEFO-metoden (First-Expired-First-Out) är en sorteringsmetod som säkerställer att de äldsta artiklarna – de med tidigast utgångsdatum – plockas först.  

 Den här funktionen fungerar bara, när dessa villkor är uppfyllt:  

-   Artikel måste ha en serie-/partinummer.  
-   På artikelns artikelspårningskod har angetts, fältet **SN dist.lager spårning** , eller **Parti dist.lager spårning** måste väljas.  
-   Artikeln måste bokföras till lagret med ett utgångsdatum.  
-   På platsen måste växlingsknappar **Begär plockning**, **Plocka enligt FEFO** och **Lagerplats ska finnas** aktiveras.  

 När alla villkor uppfylls, sorteras serie-/partinumrerade artiklar som ska plockas med de äldsta första alla plockningar och transporter, utom artiklar som använder SN-närmare visst eller partispecifik spårning.  

> [!NOTE]  
> Om någon serie-/partinumrerade artiklar använder specifik spårning, är de respekterade först och under dem, listas de återstående, icke-specifika serie-/partinummer enligt FEFO.
<br /><br />
Om två serie-/partinumrerade artiklar har samma utgångsdatum, väljs artikeln med det lägsta serie – eller partinummer.
<br /><br />
När du plockar serie-/partinumrerade artiklar på lagerställen som har ställs in för dirigerad artikelinförsel och plockning, plockas bara kvantiteter på lagerställen av typen *Plock* enligt FEFO.  
<br /><br />
Om du vill aktivera transporter enligt FEFO, lämna fältet **Från lagerplats** tomt på sidan **Lagerförflyttning** på sidan **Transportkalkylark**.  
<br /><br />
Om fältet **Endast utgångsbokföring** markeras på **Artikelspårning kodkort**, endast föremål som inte har löpt ut ingår i valet och raderna sorteras enligt FEFO-principen.

## <a name="see-also"></a>Se även  
[Plocka artiklar](warehouse-pick-items.md)   
[Plocka artiklar för utleverans från dist.lager](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Plocka artiklar med lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]