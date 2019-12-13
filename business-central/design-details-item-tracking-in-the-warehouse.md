---
title: Designdetaljer - Artikelspårning i distributionslagret | Microsoft Docs
description: Hantering av serienummer- eller partinummerbruk är främst en distributionslageruppgift, och därför har alla ankommande och avgående distributionslagerdokument standardfunktioner för att tilldela och välja artikelspårningsnummer. Men eftersom reserveringssystemet baseras på artikeltransaktioner stöds inte lageraktivitetsdokument som bara registrerar distributionslagertransaktioner helt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b7fdb0d6495f1512e1ab3bf80eb76a5dad9d87e5
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880190"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a>Designdetaljer: Artikelspårning i distributionslagret
Hantering av serienummer- eller partinummerbruk är främst en distributionslageruppgift, och därför har alla ankommande och avgående distributionslagerdokument standardfunktioner för att tilldela och välja artikelspårningsnummer.  

Men eftersom reserveringssystemet baseras på artikeltransaktioner stöds inte lageraktivitetsdokument som bara registrerar distributionslagertransaktioner helt. Eftersom reservationer och artikelspårningsnummer endast kan hanteras på lagerställenivå, och inte på lagerplats- och zonnivå, kan sidan **Artikelspårningsrader** inte öppnas från distributionslageraktivitetsdokument. Samma gäller för sidan **Reservation**.  

När ett serie- eller partinummer har lagts till i en artikel på en lagerplats kan det flyttas och grupperas fritt i distributionslagret med en oberoende artikelspårningstruktur som är orelaterad till reservationsystemet. Fälten **Serienr** och **Partinr** nås direkt på distributionslagerdokumentrader. När serie- eller partinumret senare ingår i avgående bokföring, synkroniseras det med reservationssystemet som en del av vanlig lagerplatsjustering. Mer information finns i [Designdetaljer: Integrering med lager](design-details-integration-with-inventory.md)  

Däremot beaktar reservationssystemet distributionslageraktiviteter när det beräknar disposition. Till exempel kan artiklar som tilldelats till plockningar, eller som registrerats som plockade,, inte reserveras. Mer information finns i [Designdetaljer: disposition i distributionslagret](design-details-availability-in-the-warehouse.md).

## <a name="see-also"></a>Se även  
[Designdetaljer: Artikelkoppling](design-details-item-tracking.md)  
[Designdetaljer: Integrering med lager](design-details-integration-with-inventory.md)  
[Designdetaljer - Disposition i distributionslagret](design-details-availability-in-the-warehouse.md)  
[Designdetaljer: Artikelkopplingsdesign](design-details-item-tracking-design.md)
