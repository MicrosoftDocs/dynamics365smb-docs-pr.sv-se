---
title: bästa praxis för global planeringsinstallation | Microsoft Docs
description: Snabbfliken Planering på sidan Produktionsinställningar innehåller flera fält som definierar globala regler för leveransplanering.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a611abd26fd643e75d01aeaefb22a4d0083d5003
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8510642"
---
# <a name="setup-best-practices-global-planning-setup"></a>Skapa metodtips: konfiguration av global planering
Snabbfliken **Planering** på sidan **Produktionsinställningar** innehåller flera fält som definierar globala regler för leveransplanering.  

 I tabellen nedan finns best practice för hur du lägger upp valda globala planeringsparameterfält. Välj länken i kolumnen **Inställningsfält** om du vill ha mer information om ett fält.  

|Inställningsfält|Best practice|Kommentar|  
|-----------------|-------------------|-------------|  
|Prognos på lagerställen|Markera om du har prognoser för särskilda platser.||  
|Komponenter vid lagerställe|Om artiklar inte definieras som lagerställeenheter, välj lagerställekoden för huvudlager.|Detta gäller också om du bara använder inköpskalkylarket.|  
|Tom överflödesnivå|Välj **Tillåt standardberäkningen** om du flyttar från Microsoft Dynamics NAV 5.0 eller tidigare.|Använd endast om du vill tillåta några eller alla artiklarna att gå över beställningspunkten.|  
|Standard för utjämningsperiod|Ställ in mellan 1D och 5D.<br /><br /> Ange en längre peridod i [!INCLUDE[prod_short](includes/prod_short.md)] om du är ny i planering.|När användare är mer förtrogna med de olika orsakerna till åtgärdsmeddelanden, förkorta dämpningsperioden om du vill tillåta fler ändringsförslag.|  
|Max. avvikelsekvantitet %|Ange mellan 5 och 20 procent av artikelns partistorlek.||  

## <a name="see-also"></a>Se även  
 [Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)   
 [Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
 [Skapa komplexa moduler med hjälp av bästa praxis](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]