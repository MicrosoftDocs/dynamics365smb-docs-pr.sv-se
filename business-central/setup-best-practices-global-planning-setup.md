---
title: "bästa praxis för global planeringsinstallation | Microsoft Docs"
description: "Snabbfliken **Planering** i fönstret **Produktionsinställningar** innehåller flera fält som definierar globala regler för leveransplanering."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5f9eda3b9bb2482a446370058c7bd4a503dde6ee
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-global-planning-setup"></a>Skapa metodtips: konfiguration av global planering
Snabbfliken **Planering** i fönstret **Produktionsinställningar** innehåller flera fält som definierar globala regler för leveransplanering.  

 I tabellen nedan finns best practice för hur du lägger upp valda globala planeringsparameterfält. Välj länken i kolumnen **Inställningsfält** om du vill ha mer information om ett fält.  

|Inställningsfält|Best practice|Kommentar|  
|-----------------|-------------------|-------------|  
|Prognos på lagerställen|Markera om du har prognoser för särskilda platser.||  
|Komponenter vid lagerställe|Om artiklar inte definieras som lagerställeenheter, välj lagerställekoden för huvudlager.|Detta gäller också om du bara använder inköpskalkylarket.|  
|Tom överflödesnivå|Välj **Tillåt standardberäkningen** om du flyttar från Microsoft Dynamics NAV 5.0 eller tidigare.|Använd endast om du vill tillåta några eller alla artiklarna att gå över beställningspunkten.|  
|Standard för utjämningsperiod|Ställ in mellan 1D och 5D.<br /><br /> Ange en längre peridod i [!INCLUDE[d365fin](includes/d365fin_md.md)] om du är ny i planering.|När användare är mer förtrogna med de olika orsakerna till åtgärdsmeddelanden, förkorta dämpningsperioden om du vill tillåta fler ändringsförslag.|  
|Max. avvikelsekvantitet|Ange mellan 5 och 20 procent av artikelns partistorlek.||  

## <a name="see-also"></a>Se även  
 [Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)   
 [Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
 [Skapa komplexa moduler med hjälp av bästa praxis](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

