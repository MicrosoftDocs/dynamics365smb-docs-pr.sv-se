---
title: "Designdetaljer - Hålla sig under överflödesnivån | Microsoft Docs"
description: "När du använder Maximalt antal och Fast orderkvantitet fokuserar planeringssystemet bara på det planerade lagret i den angivna tidsenheten. Det betyder att planeringssystemet kan föreslå överflödig efterfrågan när negativ efterfrågan eller positiva tillförseländringar uppstår utanför den angivna tidsenheten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bbfafc41f22a5582b90683bdacf8135e78e46843
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-staying-under-the-overflow-level"></a>Designdetaljer: Hålla sig under överflödesnivån
När du använder policyer för Maximalt antal och Fast orderkvantitet fokuserar planeringssystemet bara på det planerade lagret i den angivna tidsenheten. Det betyder att planeringssystemet kan föreslå överflödig efterfrågan när negativ efterfrågan eller positiva tillförseländringar uppstår utanför den angivna tidsenheten. Om det av denna anledning föreslås en överflödig leverans, beräknar planeringssystemet vilket antal utleveransen ska minskar till (eller tas bort) för att undvika den överflödiga utleveransen. Denna mängd kallas ”Överflödesnivå”. Överflödet kommuniceras som en planeringsrad med åtgärden **Ändra antal (minska)** eller **Avbryta** eller Annullera och följande varningsmeddelande:  

*Observera! Det planerade lagret [xx] är större än överflödesnivån [xx] på förfallodatumet [xx].*  

![Lagrets överflödesnivå](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")  

##  <a name="calculating-the-overflow-level"></a>Beräknar överflödesnivån  
Överflödesnivån beräknas på olika sätt beroende på planeringsinställningen.  

### <a name="maximum-qty-reordering-policy"></a>Partiformningsmetoden Maximalt antal  
Överflödesnivå = beställningsgräns  

> [!NOTE]  
>  Om en lägsta partistorlek finns kommer den läggas till enligt följande: Överflödesnivå = maximalt lager + minsta partistorlek.  

### <a name="fixed-reorder-qty-reordering-policy"></a>Partiformningsmetoden Fast orderkvantitet  
Överflödesnivå = Beställningsantal + beställningspunkt  

> [!NOTE]  
>  Om den minsta partistorleken är större än beställningspunkten, kommer den att ersätta enligt följande: Överflödesnivå= Beställningsantal + minsta partistorlek  

### <a name="order-multiple"></a>Partistorleksmultipel  
Om en ordermultipel finns justerar den överflödesnivån för partiformningsmetoderna Maximalt antal och Orderkvantitet.  

##  <a name="creating-the-planning-line-with-overflow-warning"></a>Skapa planeringsraden med överflödesvarning  
När en befintlig leverans gör att det planerade lagret blir högre än överflödesnivån vid slutet av en tidsenhet, skapas en planeringsrad. För att varna för den potentiella överflödiga leveransen har planeringsraden ett varningsmeddelande, fältet **Acceptera åtgärdsmeddelande** markeras inte och åtgärdsmeddelandet är antingen Avbryt eller Ändra antal.  

### <a name="calculating-the-planning-line-quantity"></a>Beräknar antal för planeringsraden  
Planeringsradantal = antal för aktuell efterfrågan – (planerat lager – överflödesnivå)  

> [!NOTE]  
>  Som med alla varningsrader ignoreras all största/minsta partistorlek eller partistorleksmultipel.  

### <a name="defining-the-action-message-type"></a>Definiera typen av åtgärdsmeddelande  

-   Om planeringsradantalet är större än 0 är åtgärdsmeddelandet Ändra antal  
-   Om planeringsradantalet är lika med eller mindre än 0 är åtgärdsmeddelandet Avbryt  

### <a name="composing-the-warning-message"></a>Skapar varningsmeddelandet  
I händelse av överflöde visar fönstret **Ej spårade planeringselement** ett varningsmeddelande med följande information:  

-   Den planerade lagernivån som utlöste varningen  
-   Den beräknade överflödesnivån  
-   Förfallodatumet för tillgångshändelsen.  

Exempel: "Det planerade lagret 120 är större än överflödesnivå 60 i 28-01-11”  

## <a name="scenario"></a>Scenario  
I det här scenariot ändrar en kund en försäljningsorder från 70 till 40 stycken mellan två planeringskörningar. Överflödesfunktionen går in för att minska inköpet som föreslogs för den initiala försäljningsantalet.  

### <a name="item-setup"></a>Inställningar för artiklar  

|Partiformningsmetod|Maximalt antal|  
|-----------------------|------------------|  
|Max. partistorlek|100|  
|Beställningspunkt|50|  
|Lager|80|  

### <a name="situation-before-sales-decrease"></a>Läge före försäljningsminskning  

|Händelse|Ändra antal|Planerat lager|  
|-----------|-----------------|-------------------------|  
|Dag ett|Ingen|80|  
|Försäljning|-70|10|  
|Slut på tidsenheten|Ingen|10|  
|Föreslå ny inköpsorder|+90|100|  

### <a name="situation-after-sales-decrease"></a>Läge efter försäljningsminskning  

|Ändra|Ändra antal|Planerat lager|  
|------------|-----------------|-------------------------|  
|Dag ett|Ingen|80|  
|Försäljning|-40|40|  
|Inköp|+90|130|  
|Slut på tidsenheten|Ingen|130|  
|Föreslås för att minska inköpet<br /><br /> order från 90 till 60|-30|100|  

### <a name="resulting-planning-lines"></a>Uppdaterar planeringsrader  
 En planeringsrad (varning) skapas för att minska inköpet med 30 från 90 till 60 för att hålla det planerade lagret på 100 enligt överflödesnivån.  

![Planera enligt överflödesnivån](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")  

> [!NOTE]  
>  Utan funktionen Överflöde skapas ingen varning om den planerade lagernivån är högre än beställningsgränsen. Det kan orsaka en överflödig leverans av 30.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Partiformningsmetoder](design-details-reordering-policies.md)   
[Designdetaljer: Planeringsparametrar](design-details-planning-parameters.md)   
[Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)

