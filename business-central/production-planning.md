---
title: Leveransplanering | Microsoft Docs
description: "Förbereda en detaljerad genomförbar plan och produktionsplan för slutmontering för försäljnings- och produktionsbehov."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a512e8e4e693a44015bc7675e5126259a5eff92b
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="planning"></a>Planering
De produktionsoperationer som krävs för att omvandla inflöde till färdiga varor måste planeras varje dag eller varje vecka beroende på vad det är för produkt och vilka volymer det handlar om. [!INCLUDE[d365fin](includes/d365fin_md.md)] erbjuder funktioner för att leverera mot förväntat och faktiskt behov från försäljning, montering och produktion samt för distributionsplanering med lagerställeenheter och lageröverföringar.

> [!NOTE]
> Det här avsnittet beskriver främst planering för de bolag som deltar i produktionen eller monteringshantering där den resulterande leveransorder kan vara tillverkning, montering, överföring eller inköpsorder. Det huvudsakliga gränssnittet för den här planeringen är fönstret **planeringsförslag**.

> [!INCLUDE[d365fin](includes/d365fin_md.md)] stöder också leveransplanering för grossistföretag där de resulterande leveransordrarna endast kan vara överföring och inköpsorder. Huvudsakliga gränssnittet för den här planeringen är fönstret **inköpskalkylark** som indirekt beskrivs i det här avsnittet eftersom de flesta funktioner gäller för båda kalkylark.

Innan du kan planera och genomföra produktionsorder måste du konfigurera produktionskapaciteterna, till exempel att skapa fabrikskalendrar, verksamhetsflöden, produktionsstrukturer och maskingrupper. Mer information finns i [Konfigurera tillverkning](production-configure-production-processes.md).

Planering kan ses som det som krävs för att förbereda leveransorder i monterings- eller produktionsavdelningar för att uppfylla efterfrågan. Mer information finns i [monteringshantering](assembly-assemble-items.md) och [Produktion](production-manage-manufacturing.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|En kort indroduktione till hur planeringssystemet kan användas för att upptäcka och prioritera behov och föreslå en konsoliderad försörjningsplan.|[Om planeringsfunktioner](production-about-planning-functionality.md)|
|Förstå hur planeringssystemet fungerar och hur du justerar algoritmerna för att uppfylla planeringskrav i olika miljöer.|[Designdetaljer: Leveransplanering](design-details-supply-planning.md)|
|Läsa mer om hur planeringslogiken skiljer mellan behov på lagerställen som finns med i inställningarna för lagerställeenhet och behov utan lagerställekoder.|[Planera med och utan lagerställen.](production-planning-with-without-locations.md)|
|Planeras utifrån förväntad försäljnings- och produktionsorder.|[Skapa en produktionsprognos](production-how-to-create-a-forecast.md)|  
|Automatiskt skapa en-mot-en-produktionsorder från försäljningsorder för att täcka det exakta behovet på den försäljningsorderraden.|[Så här skapar du produktionsorder från försäljningsorder](production-how-to-create-production-orders-from-sales-orders.md)|
|Skapa en projektproduktionsorder direkt från en försäljningsorder med flera rader så att den representerar ett produktionsprojekt.|[Planera projektorder](production-how-to-plan-project-orders.md)|
|Använda fönstret **Orderplanering** för att manuellt planera för försäljnings- eller produktionsbehovet på en strukturnivå i taget.|[Planera ny behovsorder efter order](production-how-to-plan-for-new-demand.md)|
|Använd fösntret **planeringsförslag** för att köra både Prod.program och Nettobehov för att automatiskt skapa en hög eller detaljerad försörjningsplan på alla artikelnivåer.|[Kör du komplett planering, nettobehov och produktionsplan](production-how-to-run-mps-and-mrp.md)|
|Köra inköpskalkylarket för att automatiskt skapa en detaljerad försörjningsplan för att täcka behovet av artiklar som endast kan återanskaffas via inköp eller överföring.|Sidan **Inköpskalkylark**|  
|initialisera eller uppdatera en produktionsorder som grovplanerade operationer i produktionsplanen.|[Omplanera eller uppdatera produktionsorder direkt](production-how-to-replan-refresh-production-orders.md)|
|Omberäkna produktions- eller maksingruppkalender på grund av planeringsändringar.|Avsnittet ”Beräkna en produktionsgruppkalender” i [Skapa fabrikskalendrar](production-how-to-create-work-center-calendars.md)|
|Spåra det orderbehov (spårat antal), den prognos, den försäljningsavropsorder eller den planeringsparameter (ej spårat antal) som gett upphov till den aktuella planeringsraden.|[Spåra relationer mellan tillgång och efterfrågan](production-how-track-demand-supply.md)|
|Visa det planerade tillgängliga lagret för en artikel i olika vyer och kunna se vilka bruttobehov, planerade orderinleveranser och andra händelser som kommer att påverka det med tiden.|[Visa artikeldisposition](inventory-how-availability-overview.md)|  
|Utför utvalda planeringsaktiviteter, exempelvis ändra eller lägga till planeringsförslagsrader, i en grafisk översikt över leveransplaneringen.|[Ändra planeringsförslag i en grafisk vy](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a>Se även
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

