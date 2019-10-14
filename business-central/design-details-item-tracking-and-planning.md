---
title: Designdetaljer - Artikelspårning och planering | Microsoft Docs
description: Eftersom de lagras i reservationssystemet koordineras artikelspårningsnummer helt med orderspårningsposter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0b83cc4daea4e37dae1e1ef7437276205b76cbe5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303354"
---
# <a name="design-details-item-tracking-and-planning"></a>Designdetaljer: Artikelkoppling och planering
Eftersom de lagras i reservationssystemet koordineras artikelspårningsnummer helt med orderspårningsposter. Det betyder att artiklar med orderspårningsposter kan tilldelas artikelspårningsnummer. Artiklar som har artikelspårningsnummer kan bli orderspårningsposter. Mer information finns i [Designdetaljer: Design av artikelspårning](design-details-item-tracking-design.md).

Mer information om de integrerade systemet finns i [Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md).

Eftersom orderspårning endast sker med specifik artikelkoppling, gäller koordinationen med artikelspårningsnummer endast för artiklar som ställs in för att använda specifik artikelspårning. Detta anges med fälten **SN-specifik spårning** och **Partispecifik spårning** på artikelkortet, som anger följande:

- Artikeln måste ha ett serienummer eller partinummer när den är bokförd.
- Artikeln ska kopplas till samma serienummer eller partinummer när den är bokförd avgående.

I enlighet med standardprinciper för balansering av tillgång/efterfrågan matchar planeringssystemet och den relaterade orderspårningsfunktionen endast tillgång och efterfrågan som har artikelspårningsnummer om artikeln i fråga använder specifik artikelspårning. I alla andra fall ignoreras planeringen och orderspårningssystemet artikelspårningsnummer när de kopplar tillgång för att uppfylla efterfrågan eller kopplar efterfrågan till tillgång. För mer information, se [Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md)

Till exempel när orderspårning finns för en viss artikel tyder det på att transaktioner för artikeln redan finns i tabellen **Reservationstransaktion**, som är kärnan i reservationssystemet, innan artikelspårningsnummer har definierats. Därför gäller följande kopplingsbegränsningar för de artikelspårningsnummer som ska orderspåras:

- Efterfrågan med ett serienummer eller ett partinummer kan endast täcka tillgång med samma serienummer eller partinummer.
- Efterfrågan utan ett serienummer eller ett partinummer kan täcka all tillgång, med eller utan ett serienummer eller partinummer.

Förutom konsekvenserna för dynamisk orderspårning har artikelspårningskopplingarnas begränsningar ingen större påverkan på planeringssystemet.

På tillförselsidan anges ett serie- eller partinummer vanligtvis inte förrän ordern har bokförts, t.ex. en inköpsinleverans till distributionslagret. När du registrerar ett serie- eller partinummer på efterfråganssidan, t.ex. för en försäljningsorder, finns det serie- eller partinumret redan i lagret. Artikelspårningsnummer är vanligtvis inga problem vid leveransplanering.

För artiklar som använder specifik artikelspårning måste alla serie- eller partinummer med efterfrågan matchas av motsvarande tillgång. I de flesta fall är det ingen mening att beställa ett visst serie- eller partinummer, så planeringen av inköps- eller produktionstillförsel påverkas förmodligen inte. När du överför artiklar från ett lagerställe till ett annat, är det dock troligt att överföringen gäller för ett visst parti, så planeringen av överföringstillgångar kan påverkas av den specifika kopplingsbegränsningen.

Mer information finns i [Designdetaljer: Planerade överföringar](design-details-transfers-in-planning.md).

## <a name="balancing-demand-and-supply"></a>Balansera efterfrågan och tillgång
Om en artikel kräver särskild artikelspårning skapas en orderspårningslänk från artikelns hela artikelspårningsefterfrågan till en motsvarande artikelspårningstillgång, med den enda begränsningen att tillgången ska komma före efterfrågan. Om under dessa omständigheter ingen artikelspårningstillgång kan hittas som motsvarar den objektspårningsspecifika efterfrågan, skapas en ny artikelspårningstillgång omedelbart och utan att överväga orderstorlek, planeringsparametrar eller ändrad tidpunkt för befintlig leverans av samma serie- eller partinummer.

Om artikelspårningsnummer tilldelas på efterfråganssidan eller på tillgångssidan utan att kräva särskild artikelspårning skapas en orderspårningslänk från efterfrågan till den tillgången, baserat på lämpligaste tidpunkt och antal, som i den vanliga balanseringsproceduren. Det angivna artikelspårningsnumret ingår i orderspårningsposten på samma sätt som alla angivna artikelspårningsantal definierar en ände av orderspårningslänken. Det betyder att artikelspårningsnumret som angetts bevaras, medan det även är en del av orderspårningsposten.

Om artikelspårningsnummer tilldelas på tillgångssidan utan att kräva särskild artikelspårning, betraktas tillgången som fast av planeringssystemet. Ingen storleksändring eller omplanering föreslås för den här efterfrågan, men tillgången beaktas när planeringssystemet försöker uppfylla bruttobehovet.

Mer information finns i [Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md).  

## <a name="see-also"></a>Se även  
[Designdetaljer: Artikelkopplingsdesign](design-details-item-tracking-design.md)  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)  
[Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)  
