---
title: "Planera med och utan lagerställen | Microsoft Docs"
description: "Det är viktigt att förstå att planera med eller utan lagerställekoder på behovsrader."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 964bcd38897e676baa993399fe772b8ccfdc9ea0
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="planning-with-or-without-locations"></a>Planera med och utan lagerställen.
Vid planering med eller utan lagerställekod på behovsrader, fungerar planeringssystemet på ett okomplicerat sätt när:  

-   behovsraderna alltid har lagerställekoder och systemet helt och hållet använder lagerställeenheter, inklusive den relevanta lagerställekonfigurationen.  
-   behovsraderna aldrig har lagerställekoder och systemet inte använder lagerställeenheter eller någon lagerställekonfiguration (se det sista scenariet nedan).  

Om behovsraderna ibland har lagerställekoder och ibland inte, kommer planeringssystemet att följa vissa regler beroende på konfigurationen.  

## <a name="demand-at-location"></a>Behov vid lagerställe  
När planeringssystemet identifierar behov vid ett lagerställe (en rad med en lagerställekod) reagerar det på olika sätt beroende på tre viktiga konfigurationsvärden.  

När planeringen körs kontrolleras de tre konfigurationsvärdena i tur och ordning och planeringen sker därefter:  

1.  Är fältet **Lagerställe ska finnas** markerat?  

    Om ja, då:  

2.  Finns det en lagerställeenhet för artikeln?  

    Om ja, då:  

    Artikeln planeras enligt planeringsparametrarna på kortet för lagerställeenheten.  

    Om nej, då:  

3.  Innehåller fältet **Komp. vid lagerställe** den efterfrågade lagerställekoden?  

    Om ja, då:  

    Artikeln planeras enligt planeringsparametrarna på artikelkortet.  

    Om nej, då:  

    Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti*, Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom. (De artiklar som använder partiformningsmetoden  *Order* fortsätter att använda  *Order* samt andra inställningar.)  

> [!NOTE]  
>  Detta minimialternativ täcker bara det exakta behovet. Alla planeringsparametrar som har definierats ignoreras.  

Se variationerna i scenarierna nedan.  

## <a name="demand-at-blank-location"></a>Behov vid tomt lagerställe  
Även om kryssrutan **Lagerställe** är markerat, tillåter systemet att rader skapas utan lagerställekod – vilka också kallas för *TOM*. Detta är en avvikelse för systemet eftersom det har olika konfigurationsvärden som har justerats till att hantera lagerställen (se ovan) och därför kommer planeringsmotorn inte att skapa någon planeringsrad för en behovsrad. Om fältet **Lagerställe ska finnas** inte är markerat men om något av de andra konfigurationsvärdena för lagerstället har angetts, betraktas även detta som en avvikelse och planeringssystemet reagerar genom att skicka ut "minimialternativet":   
Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir *Order)*, Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.  

Se variationerna i inställningsscenarierna nedan.  

### <a name="setup-1"></a>Konfiguration 1:  

-   Lagerställe ska finnas = *Ja*  
-   Lagerställeenheten är inställd på  *RÖD*  
-   Komp. vid lagerställe =  *BLÅ*  

#### <a name="case-11-demand-is-at--red-location"></a>Fall 1.1: Behov finns vid lagerställe *RÖD*  

Artikeln planeras enligt planeringsparametrarna på kortet för lagerställeenheten (inklusive möjlig överföring).  

#### <a name="case-12-demand-is-at--blue-location"></a>Fall 1.2: Behov finns vid lagerställe *BLÅ*  

Artikeln planeras enligt planeringsparametrarna på artikelkortet.  

#### <a name="case-13-demand-is-at--green-location"></a>Fall 1.3: Behov finns vid lagerställe  *GRÖN*  

Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir  *Order*), Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.  

#### <a name="case-14-demand-is-at--blank-location"></a>Fall 1.4: Behov finns vid lagerställe *TOM*  

Artikeln planeras inte eftersom inget lagerställe har definierats på behovsraden.  

### <a name="setup-2"></a>Konfiguration 2:  

-   Lagerställe ska finnas = *Ja*  
-   Ingen lagerställeenhet finns  
-   Komp. vid lagerställe =  *BLÅ*  

#### <a name="case-21-demand-is-at--red-location"></a>Fall 2.1: Behov finns vid lagerställe  *RÖD*  

Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir  *Order*), Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.  

#### <a name="case-22-demand-is-at--blue-location"></a>Fall 2.2: Behov finns vid lagerställe *BLÅ*  

Artikeln planeras enligt planeringsparametrarna på artikelkortet.  

### <a name="setup-3"></a>Konfiguration 3:  

-   Lagerställe ska finnas = *Ja*  
-   Ingen lagerställeenhet finns  
-   Komp. vid lagerställe =  *BLÅ*  

#### <a name="case-31-demand-is-at--red-location"></a>Fall 3.1: Behov finns vid lagerställe  *RÖD*  

Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir  *Order*), Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.  

#### <a name="case-32-demand-is-at--blue-location"></a>Fall 3.2: Behov finns vid lagerställe *BLÅ*  

Artikeln planeras enligt planeringsparametrarna på artikelkortet.  

#### <a name="case-33-demand-is-at--blank-location"></a>Fall 3.3: Behov finns vid lagerställe  *TOM*  

Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir  *Order*), Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.  

### <a name="setup-4"></a>Konfiguration 4:  

-   Lagerställe ska finnas = *Ja*  
-   Ingen lagerställeenhet finns  
-   Komp. vid lagerställe =  *TOM*  

#### <a name="case-41-demand-is-at--blue-location"></a>Fall 4.1: Behov finns vid lagerställe  *BLÅ*  

Artikeln planeras så här: Partiformningsmetod =  *Parti-för-parti* ( *Order* förblir  *Order*), Ta med lager =  *Ja*, alla andra planeringsparametrar = Tom.  

#### <a name="case-42-demand-is-at--blank-location"></a>Fall 4.2: Behov finns vid lagerställe  *TOM*  

Artikeln planeras enligt planeringsparametrarna på artikelkortet.  

Som du ser i det sista scenariet, går det bara att korrigera resultat från en behovsrad utan lagerställekod genom att inaktivera alla konfigurationsvärden för lagerställena. Det enda sättet att få stabila planeringsresultat för behov vid lagerställen är att använda lagerställeenheter.  

Om du ofta planerar för behov vid lagerställen rekommenderas det starkt att du använder funktionen Lagerställeenheter.  

## <a name="see-also"></a>Se även
[Planerad](production-planning.md)    
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

