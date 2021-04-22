---
title: Designdetaljer - Sida för artikelspårningsrader | Microsoft Docs
description: Mer information om hur du hanterar flödet av serie- och partinummer i lagret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f1dd05c8074189656bfafc5d0541504136f99390
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774920"
---
# <a name="design-details-item-tracking-lines-page"></a>Designdetaljer - Sida för artikelspårningsrader
Artikelspårningposter och reservationposter skapas i reservationssystemet, och deras disposition beräknas dynamiskt. Data som har angetts på sidan **Artikelspårningsrader** hanteras i en tillfällig version av tabellen **Spårningsspecifikation**. När sidan har stängts sparas aktiva data i tabellen **Reservationstransaktion** och historiska data sparas i tabellen **Spårningsspecifikation**. Mer information finns i [Designdetaljer: Aktiva kontra historiska artikelspårningstransaktioner](design-details-active-versus-historic-item-tracking-entries.md)  
  
Sökningar från fälten **Serienr** och **Partinr** visar dispositionen baserat på både tabellen **Artikeltransaktion** och tabellen **Reservationstransaktion** utan datumfilter. I matrisen med antalsfält i rubriken på sidan **Artikelspårningsrader** visas dynamisk antalen och summorna för artikelspårningsnummer som anges på raderna på sidan. Antalet måste stämma överens med antalet på dokumentraden, vilket indikeras av värdet **0** i fälten **Odefinierad** i huvudet på sidan.  
  
För att koordinera flödet av serie- och partinummer genom lagret finns följande regler för att registrera data på sidan **Artikelspårningsrader**:  
  
* För både ankommande och utgående artikelspårningsrader kan du inte ange ett serienummer, med eller utan partinummer, mer än en gång i samma instans av sidan **Artikelspårningsrader**. Om du försöker att ange en valfri kombination av serie- eller partinummer som redan finns på sidan visas ett felmeddelande som spärrar dataregistreringen.  
* För ankommande artikelspårningsrader kan du inte bokföra det relaterade dokument om en artikel av samma variant och med samma serienumret redan finns i lagret. Om du försöker att bokföra en positiv rad för en lagerartikel med samma variant och serienummer spärrar ett felmeddelande bokföringen. Men för både ankommande och utgående artikelspårningsrader i öppna dokument kan du använda samma kombination av serie- eller partinummer som hör till olika källdokumentrader, d.v.s. som finns i olika instanser av sidan **Artikelspårningsrader** tills det relaterade dokumentet har bokförts.  
* Om artikeln ställs in för serienummerspecifik spårning eller artikelnummerspecifik spårning kan du inte bokföra en utgående dokumentrad, såvida inte en artikel med det angivna serie- eller partinumret finns i lager. Om du försöker att bokföra en avgående dokumentrad för en artikel med ett serie-/partinummer som inte finns i lagret spärrar ett felmeddelande bokföringen.  
  
Reglerna för att registrera data på sidan **Artikelspårningsrader** stöder även kopplingsprinciperna som styr orderspårning, planering och reservation. Mer information finns i [Designdetaljer: Artikelkoppling och planering](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Objektspårning](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]