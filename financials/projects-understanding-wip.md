---
title: "PIA-metoder för att beräkna och registrera projektets framsteg | Microsoft Docs"
description: "Beskriver de olika PIA-metoder som kan användas för att bokföra och övervaka ekonomisk information för pågående projekt som är produkter i arbete."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: a0472a85be4911adacf3033c2feb6bd1513af925
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="understanding-wip-methods"></a>Förstå PIA-metoder
[!INCLUDE[d365fin](includes/d365fin_md.md)] stöder följande metoder för att beräkna och registrera värdet för produkter i arbete.

| PIA-metod | Beräkningsformel | Beskrivning av beräkning |
| --- | --- | --- |
| Kostnadsvärde |Bokförd intäkt = Fakturerbart fakturerat pris<br /><br /> Totala uppskattade kostnader = Fakturerbart totalpris x Budget kostnadsgrad<br /><br /> PIA-kostnader = (Färdigställningsgrad - Fakturerat %) x Uppskattade totalkostnader<br /><br /> Färdigställningsgrad = Förbrukning totalkostnad/Budget totalkostnad<br /> Fakturerat % = Fakturerbart fakturerat pris<br /><br /> Fakturerbart totalpris bokförda kostnader = Förbrukning totala kostnader - PIA |Kostnadsvärdesberäkningar inleds med att beräkna värdet av vad som har tillhandhållits genom att ta en del av de uppskattade totalkostnaderna baserat på färdigställningsgrad. Fakturerade kostnader subtraheras genom att ta en del av de uppskattade totalkostnaderna baserat på fakturerad procent.<br /><br /> Den här beräkningen kräver att fakturerbart totalpris, budget totalpris och budget totalkostnader anges korrekt för hela projektet. |
| Försäljningskostnad |Bokförd intäkt = Fakturerbart fakturerat pris<br /><br /> Bokförda kostnader = Budget totalkostnad x Fakturerat %<br /><br /> Fakturerat % = Fakturerbart fakturerat pris/Fakturerbart totalpris<br /><br /> (Fakturerat % finns som kolumn på projektaktivitetsrader)<br /><br /> PIA-kostnader = Förbrukning totalkostnad - Bokförda kostnader |Beräkningar av försäljningskostnader inleds genom att beräkna bokförda kostnader. Kostnader bokförs proportionellt baserat på budget totalkostnader.<br /><br /> Den här beräkningen kräver att fakturerbart totalpris och budget totalkostnader anges korrekt för hela projektet. |
| Försäljningsvärde |Bokförda kostnader = Förbrukning totalkostnad<br /><br /> Bokförd intäkt = Förbrukning totalpris x Förväntad faktureringsgrad<br /><br /> Kostnadsåterställning % = Fakturerbart totalpris/Budget totalpris<br /><br /> PIA-försäljning = Bokförd försäljning - Fakturerbart fakturerat pris |Beräkningar av försäljningsvärde bokför intäkten proportionellt baserat på totala förbrukningskostnader och förväntad kostnadsåterställningsgrad.<br /><br /> Den här beräkningen kräver att fakturerbart totalpris och budget totalpris anges korrekt för hela projektet. |
| Procent färdigställt |Bokförda kostnader = Förbrukning totalkostnad<br /><br /> Bokförd intäkt = Fakturerbart totalpris x Färdigställningsgrad<br /><br /> Färdigställningsgrad = Förbrukning totalkostnad/Budget totalkostnad<br /> (Kallas för "Färdigställningsgrad % på projektaktivitetsrader)<br /><br /> PIA-försäljning = Bokförd försäljning - Fakturerbart fakturerat pris |Beräkningar av färdigställningsgrad bokför intäkter proportionellt baserat på färdigställningsgraden, det vill säga Förbrukning totalkostnad kontra budget kostnader.<br /><br /> Den här beräkningen kräver att fakturerbart totalpris och budget totalkostnader anges korrekt för hela projektet. |
| Slutfört kontrakt |PIA-belopp = PIA-kostnadsbelopp = Förbrukning (totalkostnad)<br /><br /> PIA-försäljningsbelopp = Fakturerbart (Fakturerat pris) |Slutfört kontrakt bokför inte intäkter och kostnader förrän projektet är slutfört. Du kan vilja göra detta när det finns en stor osäkerhet kring uppskattningen av kostnader och intäkter för projektet.<br /><br /> All förbrukning bokförs på kontot för PIA-kostnader (tillgång) och all fakturerad försäljning bokförs på kontot för fakturerad PIA-försäljning (skuld) tills projektet är slutfört. |

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)      
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

