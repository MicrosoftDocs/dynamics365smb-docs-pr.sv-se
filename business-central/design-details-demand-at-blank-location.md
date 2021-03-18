---
title: Designdetaljer - Balansera efterfrågan och tillgång | Microsoft Docs
description: Detta ämne introducerar begreppet etfterfrågan, som är den gemensamma termen som vanligtvis används för alla typer av bruttobehov, t.ex försäljningsorder och komponentbehov från en produktionsorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cbafba8d012244b10c142912b357188a1f7eece4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386955"
---
# <a name="design-details-demand-at-blank-location"></a>Designdetaljer: Efterfrågan vid tomt lagerställe
När en användare skapar en begärandehändelse, till exempel en försäljningsorderrad, låter programmet användaren ibland ange en lagerställekod och andra gånger inte, det vill säga ett tomt lagerställe.

För efterfrågan med eller utan lagerställekod fungerar planeringssystemet på ett okomplicerat sätt när:

- Behovsraderna har alltid lagerställekoder och systemet använder lagerställeenheter helt och hållet, inklusive den relevanta lagerställekonfigurationen.
- Behovsraderna har aldrig lagerställekoder och systemet använder inte lagerställeenheter eller någon lagerställekonfiguration (se det sista scenariet i följande avsnitt).

Om behovshändelser ibland har lagerställekoder och ibland inte, kommer planeringssystemet att följa vissa regler beroende på konfigurationen.

## <a name="demand-at-location"></a>Behov vid lagerställe
När planeringssystemet identifierar behov vid ett lagerställe reagerar det på olika sätt beroende på tre viktiga konfigurationsvärden. När planeringen körs kontrolleras de tre konfigurationsvärdena i tur och ordning och planeringen sker därefter.

1. Är fältet **Lagerställe ska finnas** markerat?

    Om ja, då:

2. Finns det en lagerställeenhet för artikeln?

    Om ja, då:

    Artikeln planeras enligt planeringsparametrarna på kortet för lagerställeenheten.

    Om nej, då:

3. Innehåller fältet Komp. vid lagerställe den efterfrågade lagerställekoden?

  Om ja, då:

  Artikeln planeras enligt planeringsparametrarna på artikelkortet.

  Om nej, då:

  Artikeln planeras så här: Partiformningsmetod = Parti-för-parti, Ta med lager = Ja, alla andra planeringsparametrar = Tom, artiklar som använder partiformningsmetoden = Order fortsätter att använda Order tillsammans med andra inställningar.

> [!NOTE]
> Den speciella planläggningen ställde som anges som den sista reaktionen i moment till 3 ovan kallas i det följande för ”minimialternativet”. Denna planeringsinställningen täcker bara det exakta behovet. Alla planeringsparametrar som har definierats ignoreras.

Se scenarioavsnittet nedan för information om varianter av den här planeringslogiken.

## <a name="demand-at-blank-location"></a>Efterfrågan vid tomt lagerställe
Även om fältet **Lagerställe** ska finnas har markerats tillåter programmet att rader skapas utan lagerställekod, vilken också kallas för tomt lagerställe. Detta är en avvikelse för systemet eftersom det har olika konfigurationsvärden som har justerats till att hantera lagerställen (se ovan) och därför kommer planeringsmotorn inte att skapa någon planeringsrad för en behovsrad.

Om fältet **Lagerställe** ska finnas inte har valts men någon av inställningsvärdena för lagerställe finns, betraktas det också som en avvikelse och planeringssystemet kommer att reagera med genom att använda "minimialternativet": Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.

## <a name="scenarios"></a>Scenarierna
Följande scenarier beskriver varianter av efterfrågan vid tomt lagerställe och hur planeringssystemet återgår till ”minimialternativet”.

### <a name="setup-1"></a>Konfiguration 1:
Lagerställe ska finnas = Ja

Lagerställeenheten är inställd på RÖD

Komponenter vid lagerställe = BLÅ

#### <a name="case-11-demand-is-at-red-location"></a>Fall 1.1: Behov finns vid lagerställe RÖD
Artikeln planeras enligt planeringsparametrarna på kortet för lagerställeenheten.

#### <a name="case-12-demand-is-at-blue-location"></a>Fall 1.2: Behov finns vid lagerställe BLÅ
Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.

#### <a name="case-13-demand-is-at-green-location"></a>Fall 1.3: Behov finns vid lagerställe GRÖN
Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.

#### <a name="case-14-demand-is-at-blank-location"></a>Fall 1.4: Behov finns vid lagerställe TOM
Artikeln planeras inte eftersom inget lagerställe har definierats på behovsraden.

### <a name="setup-2"></a>Konfiguration 2:
Lagerställe ska finnas = Ja

Ingen lagerställeenhet finns

Komponenter vid lagerställe = BLÅ

#### <a name="case-21-demand-is-at-red-location"></a>Fall 2.1: Behov finns vid lagerställe RÖD
Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.

#### <a name="case-22-demand-is-at-blue-location"></a>Fall 2.2: Behov finns vid lagerställe BLÅ
Artikeln planeras enligt planeringsparametrarna på artikelkortet.

### <a name="setup-3"></a>Konfiguration 3:
Lagerställe ska finnas = Ja

Ingen lagerställeenhet finns

Komponenter vid lagerställe = BLÅ

#### <a name="case-31-demand-is-at-red-location"></a>Fall 3.1: Behov finns vid lagerställe RÖD
Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.

#### <a name="case-32-demand-is-at-blue-location"></a>Fall 3.2: Behov finns vid lagerställe BLÅ
Artikeln planeras enligt planeringsparametrarna på artikelkortet.

#### <a name="case-33-demand-is-at-blank-location"></a>Fall 3.3: Behov finns vid lagerställe TOM
Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.

### <a name="setup-4"></a>Konfiguration 4:
Lagerställe ska finnas = Ja

Ingen lagerställeenhet finns

Komponenter vid lagerställe = TOM

#### <a name="case-41-demand-is-at-blue-location"></a>Fall 4.1: Behov finns vid lagerställe BLÅ
Artikeln planeras så här: Partiformningsmetod = Parti-för-parti (Order förblir Order), Ta med lager = Ja, alla andra planeringsparametrar = Tom.

#### <a name="case-42-demand-is-at-blank-location"></a>Fall 4.2: Behov finns vid lagerställe TOM
Artikeln planeras enligt planeringsparametrarna på artikelkortet.

Som visas i det sista scenariet är det enda sättet att få ett korrekt resultat från en behovsrad utan lagerställekod att inaktivera alla konfigurationsvärden för lagerställena. Det enda sättet att få stabila planeringsresultat för behov vid lagerställen är att använda lagerställeenheter. Om du företag ofta planerar för behov vid lagerställen rekommenderas det starkt att de använder underavdelningen Lagerställeenheter.

## <a name="see-also"></a>Se även  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]