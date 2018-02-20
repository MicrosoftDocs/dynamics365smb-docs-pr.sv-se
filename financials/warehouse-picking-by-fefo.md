---
title: "Så här: Aktivera plockning med FEFO | Microsoft Docs"
description: "FEFO-metoden (First-Expired-First-Out) är en sorteringsmetod som säkerställer att de äldsta artiklar, de med de tidigaste utgångsdatumen, plockas först."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cc45bf06ab5d12cf393d48b7b1c295db28f56b3b
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

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

 När alla kriterier uppfylls, sorteras serie-/partinumrerade artiklar som ska plockas med de äldsta första alla plockningar och transporter, utom artiklar som använder SN-närmare visst eller partispecifik spårning.  

> [!NOTE]  
>  Om någon serie-/partinumrerade artiklar använder specifik spårning, är de respekterade först och under dem, listas de återstående, icke-specifika serie-/partinummer enligt FEFO.  

 Om två serie-/partinumrerade artiklar har samma utgångsdatum, väljs artikeln med det lägsta serie - eller partinummer. Om serie - eller partinummer är samma, väljs artikeln som registrerades först.  

> [!NOTE]  
>  -   När du plockar serie-/partinumrerade artiklar på lagerplatser som har ställs in för dirigerad artikelinförsel och plockning, plockas bara kvantiteter på lagerplatser av typen *Plock* enligt FEFO.  
> -   Om du vill aktivera transporter enligt FEFO antingen i **lagerförflyttning** fönster eller **Transportförslag** fönstret, måste du lämna **Från binge** fältet tomt.  
> -   Om fältet **Endast utgångsbokföring** är markerat kommer endast artiklar som inte har förfallit att tas med i plockningen. Detta gäller även om du inte använder plockning enligt FEFO.  

## <a name="see-also"></a>Se även  
[Plocka artiklar](warehouse-pick-items.md)   
[Plocka artiklar för utleverans från dist.lager](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Plocka artiklar med lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

