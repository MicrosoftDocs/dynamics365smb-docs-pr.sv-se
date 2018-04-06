---
title: "Designdetaljer - Design av artikelspårning | Microsoft Docs"
description: "Detta avsnit beskriver designen bakom artikelspårningen i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4d2b4d9e55851564b003ed9c85178237f8689122
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-item-tracking-design"></a>Designdetaljer: Artikelkopplingsdesign
I den första versionen av artikelspårning i [!INCLUDE[d365fin](includes/d365fin_md.md)] 2.60 registrerades serienummer eller partinummer direkt i artikeltransaktioner. Designen gav fullständig tillgänglighetsinformation och enkel spårning av historiska transaktioner, men den saknade flexibilitet och funktioner.  

Från [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.00 där artikelspårningsfunktion fanns i en separat objektstruktur med invecklade länkar till bokförda dokument och artikeltransaktioner. Design var flexibel och rik på funktioner, men artikelspårningstransaktioner var ingick inte helt i dispositionsberäkningarna.  

Sedan [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60 är artikelspårningsfunktionen integrerade med reservationssystemet, som hanterar reservation, orderspårning och åtgärdsmeddelanden. Mer information finns i "Designdetaljer: Reservation, orderspårning och åtgärdsmeddelanden" i "Designdetaljer: Leveransplanering".  

Den senaste designen innehåller artikelspårningstransaktioner i beräkningar av den totala tillgängligheten i hela systemet, inklusive planering, produktion och lagerstyrning. Det gamla konceptet att ha serie- och partinummer på artikeltransaktionerna återinförs för att säkerställa enkel tillgång till historiska data i artikelspårningssyfte. I samband med artikelspårningförbättringar i [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60 utvidgades reservationssystemet till nätverksenheter för icke-order, till exempel journaler, fakturor och kreditnotor.  

Med tillägg av serie- eller partinummer hanterar reservationssystemet permanenta artikelattribut, samtidigt som det även hanterar intermittenta länkar mellan tillgång och efterfrågan i form av orderspårningposter och reservationstransaktioner. En annan egenskap som skiljer sig åt för serie- och partinummer jämfört med konventionella reservationdata är att de kan bokföras, antingen delvis eller helt. Därför fungerar tabellen **Reservationstransaktion** (T337) nu med en relaterad tabell, tabellen **Spårningsspecifikation** (T336), som hanterar och visar summan av aktiva och bokförda artikelspårningsantal. Mer information finns i [Designdetaljer: Aktiva kontra historiska artikelspårningstransaktioner](design-details-active-versus-historic-item-tracking-entries.md)  

Följande diagram skisserar utformningen av artikelspårningsfunktionen i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

![Design för artikelspårning](media/design_details_item_tracking_design.png "design_details_item_tracking_design")  

Det centrala bokföringsobjektet omformas för att hantera den unika underklassificeringen av en dokumentrad i form av serie- eller partinummer, och särskilda relationstabeller läggs till för att skapa en-till-flera-relationer mellan bokförda dokument och deras delade artikeltransaktioner och värdetransaktioner.  

Kodenhet 22, **Artikeljournal – bokför rad**, delar nu bokföringen enligt de artikelspårningsnummer som anges på dokumentraden. Varje unikt artikelspårningsnummer på raden skapar en egen artikeltransaktion för artikeln. Det betyder att länken från den bokförda dokumentraden till de associerade artikeltransaktionerna nu är en-till-flera-relation. Relationen hanteras av följande relationstabeller för artikelspårning.  

|Fält|Beskrivning|  
|---------------|---------------------------------------|  
|**Artikeltrans. relation** (T6507)|Relaterar levererade eller inlevererade rader till artikeltransaktioner|  
|**Värdetrans. relation** (T6508)|Relaterar fakturerade rader till värdetransaktioner|  

Mer information finns i [Designdetaljer: Bokföringsstruktur för artikelspårning](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Se även  
[Designdetaljer: Artikelkoppling](design-details-item-tracking.md)

