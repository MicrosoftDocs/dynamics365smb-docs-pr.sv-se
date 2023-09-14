---
title: Planera med och utan lagerställen.
description: 'I det här avsnittet lär du dig om produktion och tillverkning, inklusive leveransplanering, i Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/15/2022
ms.author: bholtorf
---
# Planera med och utan lagerställen.

Innan du börjar använda planeringsmotorn bör du bestämma dig för om du ska använda platser eller inte. Det finns två huvudsakliga enkla sätt:

* behovsraderna alltid har lagerställekoder och systemet helt och hållet använder lagerställeenheter, inklusive den relevanta lagerställekonfigurationen. Lära dig mer på [behov vid lagerställe](#demand-at-location).  
* behovsraderna förses aldrig med lagerställekoder och systemet använder artikelkortet. Se scenariot [behov på "tomt lagerställe"](#demand-at-blank-location) nedan.

## Behov vid lagerställe  

När planeringssystemet identifierar behov vid ett lagerställe (en rad med en lagerställekod) reagerar det på olika sätt beroende på 2 viktiga konfigurationsvärden.  

Under planeringskörning körs kontrolleras de två konfigurationsvärdena i tur och ordning och planeringen sker därefter:  

1. Finns det en lagerställeenhet för artikeln på det efterfrågade lagerstället?  

    Om ja, då:  

    Artikeln planeras enligt planeringsparametrarna på kortet för lagerställeenheten.  

    Om nej, då:  

2. Innehåller fältet **Komponenter på lagerställe** på sidan **Produktionskonfiguration** begärd lagerställeskod?  

    Om ja, då:  

    Artikeln planeras enligt planeringsparametrarna på artikelkortet.  

    Om nej, då:  

    Artikeln planeras enligt "lägsta alternativ" som täcker det exakta behovet. Planeringsparametrarna anges som: Partiformningsmetod = *Parti-för-parti*, Ta med lager = *Ja*, alla andra planeringsparametrar = Tom. (De artiklar som använder partiformningsmetoden  *Order* fortsätter att använda  *Order* samt andra inställningar.)

> [!TIP]
> Om du ofta planerar för behov på olika lagerställen rekommenderar vi att du använder funktionen lagerställeenheter och undvika efterfrågan på tomt lagerställe. Läs mer i [Ställa in lagerställeenheter](inventory-how-to-set-up-stockkeeping-units.md)

Se variationerna i [scenarierna nedan](#scenarios).

> [!NOTE]
> Fältet **Komponenter vid lagerställe** på sidan **Produktionsinställningar** är väldigt viktigt när du styr hur behovsrader med/utan lagerställekoder hanteras i planeringssystemet.
>
> För produktionsbehovet använder [!INCLUDE [prod_short](includes/prod_short.md)] samma lagerställe för detaljmontage och komponenterna som anges i produktionsordern. Om du fyller i det här fältet kan du emellertid dirigera om detaljmontage och komponenterna till ett annat lagerställe.
>
> Du kan också definiera detta för en viss lagerställeenhet genom att välja en annan lagerställekod i fältet **Komponenter på lagerställe** på lagerställeenhetskortet. Observera dock att detta sällan har någon betydelse eftersom planeringslogiken kan komma att förvridas när du planerar för komponenten Lagerställeenhet.

## Efterfrågan vid "tomt lagerställe"

I allmänhet planeras artikeln enligt planerings parametrarna på artikelkortet när ett behov identifieras på en tom plats (en rad utan lagerställekod) i planeringssystemet.

Fältet **Lagerställen obligatoriska** på sidan **Lagerinställningar** samt fältet **Komponenter på lagerställe** på sidan **Produktionskonfiguration** eller lagerställeenheter kommer att påverka hur planeringssystemet hanterar efterfrågerader med/utan platskoder. Om ett av följande påståenden är sant, anses efterfrågan på tomt lagerställe också vara en avvikelse och planeringssystemet kommer att reagera genom att mata ut "minimialternativ": Artikeln planeras enligt: Ombeställningspolicy = *Parti-för-parti* (*Order* förblir *Order*), Ta med lager = *Ja*, alla andra planeringsparametrar = Tom.

* Fältet **Komponenter vid lagerställe** på sidan **Produktionsinställningar** har ett värde.
* En lagerställeenhet finns för den planerade artikeln.
* Fältet **Lagerställe ska finnas** är markerat.

## Scenarierna

Se variationerna i inställningsscenarierna nedan.

### Konfiguration 1

* Lagerställe ska finnas = *Ja*  
* Lagerställeenheten är inställd på *VÄST*  
* Komponent vid lagerställe = *ÖST*  

#### Fall 1.1: Behov finns vid lagerställe *VÄST*

Artikeln planeras enligt planeringsparametrarna på kortet för lagerställeenheten (inklusive möjlig överföring).

#### Fall 1.2: Behov finns vid lagerställe *ÖST*

Artikeln planeras enligt planeringsparametrarna på artikelkortet.

#### Fall 1.3: Behov finns vid lagerställe *NORR*

Artikeln planeras så här: Partiformningsmetod = *Parti-för-parti* (*Order* förblir *Order*), Ta med lager = *Ja*, alla andra planeringsparametrar = Tom.

#### Fall 1.4: Behov finns vid lagerställe *TOM*

Artikeln planeras så här: Partiformningsmetod = *Parti-för-parti* (*Order* förblir *Order*), Ta med lager = *Ja*, alla andra planeringsparametrar = Tom.

### Konfiguration 2

* Lagerställe ska finnas = *Ja*  
* Ingen lagerställeenhet finns  
* Komponent vid lagerställe = *ÖST*  

#### Fall 2.1: Behov finns vid lagerställe *VÄST*

Artikeln planeras så här: Partiformningsmetod = *Parti-för-parti* (*Order* förblir *Order*), Ta med lager = *Ja*, alla andra planeringsparametrar = Tom.

#### Fall 2.2: Behov finns vid lagerställe *ÖST*

Artikeln planeras enligt planeringsparametrarna på artikelkortet.  

### Konfiguration 3

* Lagerställe ska finnas = *Ja*  
* Ingen lagerställeenhet finns  
* Komponent vid lagerställe = *ÖST*  

#### Fall 3.1: Behov finns vid lagerställe *VÄST*

Artikeln planeras så här: Partiformningsmetod = *Parti-för-parti* (*Order* förblir *Order*), Ta med lager = *Ja*, alla andra planeringsparametrar = Tom.

#### Fall 3.2: Behov finns vid lagerställe *ÖST*

Artikeln planeras enligt planeringsparametrarna på artikelkortet.  

#### Fall 3.3: Behov finns vid lagerställe *TOM*

Artikeln planeras så här: Partiformningsmetod = *Parti-för-parti* (*Order* förblir *Order*), Ta med lager = *Ja*, alla andra planeringsparametrar = Tom.

### Konfiguration 4

* Lagerställe ska finnas = *Ja*  
* Ingen lagerställeenhet finns  
* Komp. vid lagerställe = *TOM*  

#### Fall 4.1: Behov finns vid lagerställe *ÖST*

Artikeln planeras så här: Partiformningsmetod = *Parti-för-parti* (*Order* förblir *Order*), Ta med lager = *Ja*, alla andra planeringsparametrar = Tom.

#### Fall 4.2: Behov finns vid lagerställe *TOM*

Artikeln planeras enligt planeringsparametrarna på artikelkortet.

Som du ser i det sista scenariet, går det bara att korrigera resultat från en behovsrad utan lagerställekod genom att inaktivera alla konfigurationsvärden för lagerställena. Det enda sättet att få stabila planeringsresultat för behov vid lagerställen är att använda lagerställeenheter.  

Om du ofta planerar för behov på olika lagerställen rekommenderar vi därför att du använder funktionen Lagerställeenheter.

## Se relaterad utbildning på [Microsoft Learn](/training/paths/trade-get-started-dynamics-365-business-central/).

## Se även

[Planerad](production-planning.md)  
[Konfigurera produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerställeenheter](inventory-how-to-set-up-stockkeeping-units.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)  
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
