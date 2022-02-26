---
title: Designdetaljer - Disposition i distributionslagret | Microsoft Docs
description: Systemet måste ha en konstant kontroll på artikeltillgänglighet i distributionslagret, så att avgående beställningar kan flöda effektivt och ge bästa möjliga leveranser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 7d23dc10ffb215ee2ac160c9ec9b9fd1ddb5cc2d
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442541"
---
# <a name="design-details-availability-in-the-warehouse"></a>Designdetaljer: Disposition i distributionslagret
Systemet måste ha en konstant kontroll på artikeltillgänglighet i distributionslagret, så att avgående beställningar kan flöda effektivt och ge bästa möjliga leveranser.  

Dispositionen varierar beroende på fördelningar på lagerplatsnivån när distributionslageraktiviteter, till exempel plockning och transport, inträffar och när lagerreservationssystemet har begränsningar som ska uppfyllas. En ganska komplex algoritm kontrollerar att alla villkor är uppfyllda innan antal tilldelas till plockningar för utgående flöden.

Om ett eller flera villkor inte uppfylls kan olika felmeddelanden visas, inklusive det allmänna "inget att hantera". -meddelande. Meddelandet "Inget att hantera." kan finnas flera olika orsaker, både i utgående och ankommande flöden, där en direkt eller indirekt involverad dokumentrad innehåller fältet **Ant. att hantera**.

> [!NOTE]
> Informationen kommer snart att publiceras här om möjliga orsaker och lösningar för "inget att hantera". -meddelande.

## <a name="bin-content-and-reservations"></a>Lagerplats och reservationer  
 I en installation av lagerstyrning finns artikelantalet både som distributionslagertransaktioner, i modulen Distributionslager och som artikeltransaktioner, i modulen Lager. Dessa två transaktionstyper innehåller information om var artiklarna finns och om de är tillgängliga. Distributionslagertransaktioner definierar en artikels tillgänglighet per lagerplats och lagerplatstyp, vilket kallas lagerplatsinnehåll. Artikeltransaktioner definierar en artikels disposition genom dess reservation till avgående dokument.  

 Särskild funktion i plockningsalgoritmen finns för att beräkna den kvantitet som är tillgänglig för plockning när lagerplatsinnehåll kopplas ihop med reservationer.  

## <a name="quantity-available-to-pick"></a>Disponibelt antal att plocka  
 Om till exempel plockningsalgoritmen inte beaktar artikelantal som har reserverats för en väntande försäljningsframgångs, kan dessa artiklar plockas för en annan försäljningsorder som ska utlevereras tidigare, vilket hindrar att den första försäljningen uppfylls. För att undvika den här situationen drar plockningsalgoritmen bort antal som har reserverats för andra avgående dokument, antal på befintliga plockdokument och antal som har plockas men som ännu inte har levererats eller förbrukats.  

 Resultatet visas i fältet **Disponibelt att plocka** på sidan **Plockningskalkylark** där fältet beräknas dynamiskt. Värdet beräknas också när användaren skapar distributionslagerplockningarna direkt för avgående dokument. Sådana utgående dokument kan vara försäljningsorder, produktionsförbrukning eller utgående överföringar, där resultatet visas i de relaterade antalsfälten, till exempel **Ant. att hantera**.  

> [!NOTE]  
>  Angående prioriteten för reservationer subtraheras antalet som ska reserveras från antalet som är disponibelt att plockas. Till exempel om antalet som är tillgängligt på plocklagerplatser är 5 enheter, men 100 enheter finns på införsel-lagerplatser, och du försöker att reservera mer än 5 enheter för ytterligare en order, kommer ett felmeddelande visas eftersom den här extra kvantiteten måste vara tillgänglig på plocklagerplatser.  

### <a name="calculating-the-quantity-available-to-pick"></a>Beräknar disponibelt antal att plocka  
 Antalet som är tillgängligt att plocka beräknas så här:  

 disponibelt antal att plocka = antal på plocklagerplatser - antal i plockning och transport – (reserverat antal på plocklagerplatser + reserverat antal i plockning och transport)  

 Följande diagram visar de olika elementen i beräkningen.  

 ![Tillgänglig för plockning med reservationsöverlappning.](media/design_details_warehouse_management_availability_2.png "Tillgänglig för plockning med reservationsöverlappning")  

## <a name="quantity-available-to-reserve"></a>Disponibelt antal att reservera  
 Eftersom begreppen för lagerplatsinnehåll och reservation finns till samtidigt, måste antalet artiklar som är disponibla att reservera justeras mot fördelningar till utgående distributionslagerdokument.  

 Det bör vara möjligt att reservera alla artiklar i lager, utom de som har inlett avgående behandling. Antalet som är tillgängligt att reservera definieras som antalet på alla dokument och alla lagerplatstyper, utom följande avgående antal:  

-   Antal i oregistrerade plockdokument  
-   Antal i utleveranslagerplatser  
-   Antal i till-produktion-lagerplatser  
-   Antal i öppna produktionslagerplatser  
-   Antal i till-montering-lagerplatser  
-   Antal på justeringlagerplatser  

 Resultatet visas i fältet **Totalt disponibelt antal** på sidan **Reservation**.  

 På en reservationsrad visas antalet som inte kan reserveras, eftersom det har fördelats i distributionslagret, i fältet **Fördelat antal i dist.lager** på sidan **Reservation**.  

### <a name="calculating-the-quantity-available-to-reserve"></a>Beräknar disponibelt antal att reservera  
 Antalet som är tillgängligt att reservera beräknas så här:  

 disponibelt antal att reservera = totalt antal i lager - antal i plockning och transport för källdokument - reserverat antal - antal i avgående lagerplatser  

 Följande diagram visar de olika elementen i beräkningen.  

 ![Tillgänglig för reservering per lagerställefördelning.](media/design_details_warehouse_management_availability_3.png "Tillgänglig för reservering per lagerställefördelning")  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
 [Visa artikeldisposition](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]