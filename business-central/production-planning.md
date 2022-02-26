---
title: Leveransplanering
description: Förbereda en detaljerad genomförbar plan och produktionsplan för slutmontering för försäljnings- och produktionsbehov.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.for: 291, 292, 293, 295, 517, 9010, 9038
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c589fbccabed3f8e021e503ee8a1fbac17ad5db7
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972625"
---
# <a name="planning"></a>Planering

De produktionsoperationer som krävs för att omvandla inflöde till färdiga varor måste planeras varje dag eller varje vecka beroende på vad det är för produkt och vilka volymer det handlar om. [!INCLUDE[prod_short](includes/prod_short.md)] erbjuder funktioner för att leverera mot förväntat och faktiskt behov från försäljning, montering och produktion samt för distributionsplanering med lagerställeenheter och lageröverföringar.

> [!NOTE]
> Det här avsnittet beskriver främst planering för de bolag som deltar i produktionen eller monteringshantering där den resulterande leveransorder kan vara tillverkning, montering, överföring eller inköpsorder. Det huvudsakliga gränssnittet för den här planeringen är sidan **planeringsförslag**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] stöder också leveransplanering för grossistföretag där de resulterande leveransordrarna endast kan vara överföring och inköpsorder. Huvudsakliga gränssnittet för den här planeringen är sidan **inköpskalkylark** som indirekt beskrivs i det här avsnittet eftersom de flesta funktioner gäller för båda kalkylark.

Planering kan ses som det som krävs för att förbereda leveransorder i inköps-, monterings- eller produktionsavdelningar för att uppfylla efterfrågan på försäljning och slutartikel. Mer information finns i [Inköp](purchasing-manage-purchasing.md), [monteringshantering](assembly-assemble-items.md) och [Produktion](production-manage-manufacturing.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|En kort indroduktione till hur planeringssystemet kan användas för att upptäcka och prioritera behov och föreslå en konsoliderad försörjningsplan.|[Om planeringsfunktioner](production-about-planning-functionality.md)|
|Förstå hur planeringssystemet fungerar och hur du justerar algoritmerna för att uppfylla planeringskrav i olika miljöer.|[Designdetaljer: Leveransplanering](design-details-supply-planning.md)|
|Läsa mer om hur planeringslogiken skiljer mellan behov på lagerställen som finns med i inställningarna för lagerställeenhet och behov utan lagerställekoder.|[Planera med och utan lagerställen.](production-planning-with-without-locations.md)|
|Prognostisera efterfrågan utifrån förväntade försäljnings- och produktionskomponenter.|[Skapa en efterfrågeprognos](production-how-to-create-a-forecast.md)|  
|Skapa en-mot-en- eller projektproduktionsorder från försäljningsorder för att täcka det exakta behovet på den försäljningsordern.|[Så här skapar du produktionsorder från försäljningsorder](production-how-to-create-production-orders-from-sales-orders.md)|
|Använd sidan **Orderplanering** för att manuellt planera för försäljnings- eller produktionsbehovet på en strukturnivå i taget.|[Planera ny behovsorder efter order](production-how-to-plan-for-new-demand.md)|
|Använd sidan **planeringsförslag** för att köra både Prod.program och Nettobehov för att automatiskt skapa en hög eller detaljerad försörjningsplan på alla artikelnivåer.|[Kör du komplett planering, nettobehov och produktionsplan](production-how-to-run-mps-and-mrp.md)|
|Använd sidan **Inköpskalkylark** för att automatiskt skapa en detaljerad försörjningsplan för att täcka behovet av artiklar som endast kan återanskaffas via inköp eller överföring.|[Inköpskalkylark](production-about-planning-functionality.md#requisition-worksheet)|  
|initialisera eller uppdatera en produktionsorder som grovplanerade operationer i produktionsplanen.|[Omplanera eller uppdatera produktionsorder direkt](production-how-to-replan-refresh-production-orders.md)|
|Omberäkna produktions- eller maksingruppkalender på grund av planeringsändringar.|[Så här beräknar du en produktionsgruppkalender](production-how-to-create-work-center-calendars.md#to-calculate-a-work-center-calendar)|
|Spåra det orderbehov (spårat antal), den prognos, den försäljningsavropsorder eller den planeringsparameter (ej spårat antal) som gett upphov till den aktuella planeringsraden.|[Spåra relationer mellan tillgång och efterfrågan](production-how-track-demand-supply.md)|
|Visa det planerade tillgängliga lagret för en artikel i olika vyer och kunna se vilka bruttobehov, planerade orderinleveranser och andra händelser som kommer att påverka det med tiden.|[Visa artikeldisposition](inventory-how-availability-overview.md)|  
<!--|Utför utvalda planeringsaktiviteter, exempelvis ändra eller lägga till planeringsförslagsrader, i en grafisk översikt över leveransplaneringen.|[Ändra planeringsförslag i en grafisk vy](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|-->

## <a name="see-also"></a>Se även

[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)  
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
