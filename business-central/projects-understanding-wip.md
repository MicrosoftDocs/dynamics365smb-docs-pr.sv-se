---
title: PIA-metoder för att beräkna och registrera projektets framsteg | Microsoft Docs
description: Beskriver de olika PIA-metoder som kan användas för att bokföra och övervaka ekonomisk information för pågående projekt som är produkter i arbete.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 75a2b7d74b93a3dc27441d8a5f0b966ed9d16d09
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388255"
---
# <a name="understanding-wip-methods"></a>Förstå PIA-metoder
Allt eftersom ett projekt fortlöper används material och resurser och de, och andra kostnader, måste bokföras i projektet. Produkter i arbete (PIA) är en funktion som gör att du kan uppskatta värdet i projektet i redovisningen medan projekten pågår. I många fall kan du bokföra kostnader för ett projekt innan du fakturerar projektet. Om endast kostnader bokförts blir er finansiella rapport oriktig.

Om du vill hålla reda på värdet i redovisningen kan du beräkna PIA (Produkter i arbete) och bokföra värdet i redovisningen. Mer information finns i [Övervaka projektframsteg och -resultat](projects-how-monitor-progress-performance.md).

[!INCLUDE[prod_short](includes/prod_short.md)] stöder följande metoder för att beräkna och registrera värdet för produkter i arbete.

| PIA-metod | Beräkningsformel | Beskrivning av beräkning |
| --- | --- | --- |
| Kostnadsvärde |Bokförd intäkt = Fakturerbart fakturerat pris<br /><br /> Totala uppskattade kostnader = Fakturerbart totalpris x Budget kostnadsgrad<br /><br /> PIA-kostnader = (Färdigställningsgrad – Fakturerat %) x Uppskattade totalkostnader<br /><br /> Färdigställningsgrad = Förbrukning totalkostnad/Budget totalkostnad<br /> Fakturerat % = Fakturerbart fakturerat pris<br /><br /> Fakturerbart totalpris bokförda kostnader = Förbrukning totala kostnader – PIA |Kostnadsvärdesberäkningar inleds med att beräkna värdet av vad som har tillhandhållits genom att ta en del av de uppskattade totalkostnaderna baserat på färdigställningsgrad. Fakturerade kostnader subtraheras genom att ta en del av de uppskattade totalkostnaderna baserat på fakturerad procent.<br /><br /> Den här beräkningen kräver att fakturerbart totalpris, budget totalpris och budget totalkostnader anges korrekt för hela projektet. |
| Försäljningskostnad |Bokförd intäkt = Fakturerbart fakturerat pris<br /><br /> Bokförda kostnader = Budget totalkostnad x Fakturerat %<br /><br /> Fakturerat % = Fakturerbart fakturerat pris/Fakturerbart totalpris<br /><br /> (Fakturerat % finns som kolumn på projektaktivitetsrader)<br /><br /> PIA-kostnader = Förbrukning totalkostnad – Bokförda kostnader |Beräkningar av försäljningskostnader inleds genom att beräkna bokförda kostnader. Kostnader bokförs proportionellt baserat på budget totalkostnader.<br /><br /> Den här beräkningen kräver att fakturerbart totalpris och budget totalkostnader anges korrekt för hela projektet. |
| Försäljningsvärde |Bokförda kostnader = Förbrukning totalkostnad<br /><br /> Bokförd intäkt = Förbrukning totalpris x Förväntad faktureringsgrad<br /><br /> Kostnadsåterställning % = Fakturerbart totalpris/Budget totalpris<br /><br /> PIA-försäljning = Bokförd försäljning – Fakturerbart fakturerat pris |Beräkningar av försäljningsvärde bokför intäkten proportionellt baserat på totala förbrukningskostnader och förväntad kostnadsåterställningsgrad.<br /><br /> Den här beräkningen kräver att fakturerbart totalpris och budget totalpris anges korrekt för hela projektet. |
| Procent färdigställt |Bokförda kostnader = Förbrukning totalkostnad<br /><br /> Bokförd intäkt = Fakturerbart totalpris x Färdigställningsgrad<br /><br /> Färdigställningsgrad = Förbrukning totalkostnad/Budget totalkostnad<br /> (Kallas för "Färdigställningsgrad % på projektaktivitetsrader)<br /><br /> PIA-försäljning = Bokförd försäljning – Fakturerbart fakturerat pris |Beräkningar av färdigställningsgrad bokför intäkter proportionellt baserat på färdigställningsgraden, det vill säga Förbrukning totalkostnad kontra budget kostnader.<br /><br /> Den här beräkningen kräver att fakturerbart totalpris och budget totalkostnader anges korrekt för hela projektet. |
| Slutfört kontrakt |PIA-belopp = PIA-kostnadsbelopp = Förbrukning (totalkostnad)<br /><br /> PIA-försäljningsbelopp = Fakturerbart (Fakturerat pris) |Slutfört kontrakt bokför inte intäkter och kostnader förrän projektet är slutfört. Du kan vilja göra detta när det finns en stor osäkerhet kring uppskattningen av kostnader och intäkter för projektet.<br /><br /> All förbrukning bokförs på kontot för PIA-kostnader (tillgång) och all fakturerad försäljning bokförs på kontot för fakturerad PIA-försäljning (skuld) tills projektet är slutfört. |

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)      
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]