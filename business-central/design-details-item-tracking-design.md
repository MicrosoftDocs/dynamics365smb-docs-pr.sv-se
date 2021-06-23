---
title: Designdetaljer - Artikelkopplingsdesign
description: I det här avsnittet beskrivs designen bakom artikelspårning i Business Central när den mognar genom produktversioner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 5bb97f1c26ca9264718a96a9f2f7803e248927b3
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214984"
---
# <a name="design-details-item-tracking-design"></a>Designdetaljer: Artikelkopplingsdesign

Artikelspårning i [!INCLUDE[prod_short](includes/prod_short.md)] startar med [!INCLUDE [navnow_md](includes/navnow_md.md)]. Artikelspårningsfunktionen finns i en separat objektstruktur med invecklade länkar till bokförda dokument och artikeltransaktioner och den är integrerad med bokningssystemet, som hanterar reservation, orderspårning och åtgärdsmeddelanden. Mer information finns i [Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden](design-details-reservation-order-tracking-and-action-messaging.md) i designdetaljer för leveransplanering.  

Designen innehåller artikelspårningstransaktioner i beräkningar av den totala tillgängligheten i hela systemet, inklusive planering, produktion och lagerstyrning. Serie- och partinummer används på artikeltransaktionerna för att säkerställa enkel tillgång till historiska data i artikelspårningssyfte. Med 2021 utgivningscykel 1 innehåller artikelspårning i [!INCLUDE [prod_short](includes/prod_short.md)] paketnummer.  

Med tillägg av serie- parti- eller paketnummer hanterar reservationssystemet permanenta artikelattribut, samtidigt som det även hanterar intermittenta länkar mellan tillgång och efterfrågan i form av orderspårningposter och reservationstransaktioner. En annan egenskap som skiljer sig åt för serie- och partinummer jämfört med konventionella reservationdata är att de kan bokföras, antingen delvis eller helt. Därför fungerar tabellen **Reservationstransaktion** (T337) nu med en relaterad tabell, tabellen **Spårningsspecifikation** (T336), som hanterar och visar summan av aktiva och bokförda artikelspårningsantal. Mer information finns i [Designdetaljer: Aktiva kontra historiska artikelspårningstransaktioner](design-details-active-versus-historic-item-tracking-entries.md)  

Följande diagram skisserar utformningen av artikelspårningsfunktionen i [!INCLUDE[prod_short](includes/prod_short.md)].  

![Exempel på artikelspårningsflöde](media/design_details_item_tracking_design.png "Exempel på artikelspårningsflöde")  

Det centrala bokföringsobjektet omformas för att hantera den unika underklassificeringen av en dokumentrad i form av serie- eller partinummer, och särskilda relationstabeller läggs till för att skapa en-till-flera-relationer mellan bokförda dokument och deras delade artikeltransaktioner och värdetransaktioner.  

Kodenhet 22, **Artikeljournal – bokför rad**, delar nu bokföringen enligt de artikelspårningsnummer som anges på dokumentraden. Varje unikt artikelspårningsnummer på raden skapar en egen artikeltransaktion för artikeln. Det betyder att länken från den bokförda dokumentraden till de associerade artikeltransaktionerna nu är en-till-flera-relation. Relationen hanteras av följande relationstabeller för artikelspårning.  

|Fält|Beskrivning|  
|---------------|---------------------------------------|  
|**Artikeltrans. relation** (T6507)|Relaterar levererade eller inlevererade rader till artikeltransaktioner|  
|**Värdetrans. relation** (T6508)|Relaterar fakturerade rader till värdetransaktioner|  

Mer information finns i [Designdetaljer: Bokföringsstruktur för artikelspårning](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Se även

[Designdetaljer: Artikelkoppling](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
