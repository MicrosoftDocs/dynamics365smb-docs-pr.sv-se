---
title: Hantera lager- och produktionskostnader | Microsoft Docs
description: Många av funktionerna inom kostnadskalkylering utförs i underliggande processer som användaren inte behöver bry sig om, till exempel transaktionskoppling och automatisk kostnadsjustering, men ett antal fält, sidor och rapporter riktar sig mot användare som direkt eller indirekt hanterar kostnader för artiklar eller driften.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 27c036dac88bce71ecfefa064d05ac3cdd8e8225
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807050"
---
# <a name="handling-inventory-and-manufacturing-costs"></a>Hantera lager- och produktionskostnader
Många av funktionerna inom kostnadskalkylering utförs i underliggande processer som användaren inte behöver bry sig om, till exempel transaktionskoppling och automatisk kostnadsjustering, men ett antal fält, sidor och rapporter riktar sig mot användare som direkt eller indirekt hanterar kostnader för artiklar eller driften.  

 Att tilldela artikelomkostnader till inköpsdokument är ett exempel på en indirekt uppgift inom kostnadskalkylering. Att uppdatera styckkostnad för en artikel i monterings- eller produktionsstrukturen är ett exempel på en mer direkt uppgift inom kostnadskalkylering.  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|regelbundet eller automatiskt uppdatera styckkostnaden för en eller flera artiklar så att alla kostnadsändringar från ankommande transaktioner, till exempel de för inköp eller produktionsutflöde, flyttas fram till relaterade avgående transaktioner, till exempel försäljningar eller överföringar.|[Justera artikelkostnader](inventory-how-adjust-item-costs.md)|  
|få en inblick i genomsnittskostnadsdynamiken för att fatta beslut om prissättning eller spåra kostnadsfluktuationer orsakade av informationsregistreringsfel.|[Registrera nya artiklar](inventory-how-register-new-items.md)|  
|skapa en produktionsartikels standardkostnad genom att ange de tre kostnadsslagen: materialkostnad, kapacitetskostnad och underleverantörskostnad.|[Om beräkning av standardkostnad](finance-about-calculating-standard-cost.md)|  
|beräkna styckkostnaden för en strukturartikel baserat på styckkostnaderna för dess underliggande komponenter.|[Arbeta med strukturer](inventory-how-work-BOMs.md)|  
|slutföra kostnadskalkyleringslivscykeln för en producerad artikel genom att justera kostnaderna och stämma av värdetransaktionerna med redovisningen.|[Om kostnader för färdiga produktionsorder](finance-about-finished-production-order-costs.md)|  
|ändra värdet för en artikel i lager eller värdet för en artikeltransaktion, till exempel en inköpstransaktion.|[Omvärdera lager](inventory-how-revalue-inventory.md)|
|manuellt ångra en artikelkoppling eller koppla om artikeltransaktioner som skapats i programmet.|[Ta bort och koppla om artikeltransaktioner](finance-how-to-remove-and-reapply-item-entries.md)|  
|Du kan använda fältet **Kopplas från löpnr** i artikeljournal för att skapa en fast koppling mellan en inkommande transaktion och den ursprungliga utgående transaktionen.|[Avsluta öppna artikeltransaktioner som skapas från en fast koppling i artikeljournalen](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a>Se även  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)
[Designdetaljer: Lagerkostnad](design-details-inventory-costing.md)
