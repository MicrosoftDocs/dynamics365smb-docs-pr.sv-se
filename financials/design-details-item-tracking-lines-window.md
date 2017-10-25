---
title: "Designdetaljer - Fönster för artikelspårningsrader | Microsoft Docs"
description: "Mer information om hur du hanterar flödet av serie- och partinummer i lagret."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 62070ef4e580a3bd665130c9b017bf164bbe2142
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-item-tracking-lines-window"></a>Designdetaljer: Fönster för artikelspårningsrader
Artikelspårningposter och reservationposter skapas i reservationssystemet, och deras disposition beräknas dynamiskt. Data som har angetts i fönstret **Artikelspårningsrader** hanteras i en tillfällig version av tabellen **Spårningsspecifikation**. När fönstret har stängts sparas aktiva data i tabellen **Reservationstransaktion** och historiska data sparas i tabellen **Spårningsspecifikation**. Mer information finns i [Designdetaljer: Aktiva kontra historiska artikelspårningstransaktioner](design-details-active-versus-historic-item-tracking-entries.md)  
  
Sökningar från fälten **Serienr** och **Partinr** visar dispositionen baserat på både tabellen **Artikeltransaktion** och tabellen **Reservationstransaktion** utan datumfilter. I matrisen med antalsfält i rubriken på fönstret **Artikelspårningsrader** visas dynamisk antalen och summorna för artikelspårningsnummer som anges på raderna i fönstret. Antalet måste stämma överens med antalet på dokumentraden, vilket indikeras av värdet **0** i fälten **Odefinierad** i huvudet på fönstret.  
  
För att koordinera flödet av serie- och partinummer genom lagret finns följande regler för att registrera data i fönstret **Artikelspårningsrader**:  
  
* För både ankommande och utgående artikelspårningsrader kan du inte ange ett serienummer, med eller utan partinummer, mer än en gång i samma instans av fönstret **Artikelspårningsrader**. Om du försöker att ange en valfri kombination av serie- eller partinummer som redan finns i fönstret visas ett felmeddelande som spärrar dataregistreringen.  
* För ankommande artikelspårningsrader kan du inte bokföra det relaterade dokument om en artikel av samma variant och med samma serienumret redan finns i lagret. Om du försöker att bokföra en positiv rad för en lagerartikel med samma variant och serienummer spärrar ett felmeddelande bokföringen. Men för både ankommande och utgående artikelspårningsrader i öppna dokument kan du använda samma kombination av serie- eller partinummer som hör till olika källdokumentrader, d.v.s. som finns i olika instanser av fönstret **Artikelspårningsrader** tills det relaterade dokumentet har bokförts.  
* Om artikeln ställs in för serienummerspecifik spårning eller artikelnummerspecifik spårning kan du inte bokföra en utgående dokumentrad, såvida inte en artikel med det angivna serie- eller partinumret finns i lager. Om du försöker att bokföra en avgående dokumentrad för en artikel med ett serie-/partinummer som inte finns i lagret spärrar ett felmeddelande bokföringen.  
  
Reglerna för att registrera data i fönstret **Artikelspårningsrader** stöder även kopplingsprinciperna som styr orderspårning, planering och reservation. Mer information finns i [Designdetaljer: Artikelspårning och planering](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Objektspårning](design-details-item-tracking.md)
