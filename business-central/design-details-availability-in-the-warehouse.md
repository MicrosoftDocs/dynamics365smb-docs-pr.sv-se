---
title: Designdetaljer – Disposition i distributionslagret
description: Lära dig mer om de olika faktorer som påverkar artikeldispositionen i distributionslagret.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
---
# <a name="design-details-availability-in-the-warehouse"></a><a name="design-details-availability-in-the-warehouse"></a>Designdetaljer: Disposition i distributionslagret

Håll dig uppdaterad om artikeldispositionen för att säkerställa att utgående order flödar effektivt och att leveranstiderna är optimala.  

Disposition kan variera beroende på flera faktorer. Till exempel:

* Fördelningar på lagerplatsnivå när lageraktiviteter som plockningar och transporter sker.
* När lagerreservationssystemet tillämpar begränsningar för att följa.

Innan du fördelar kvantiteter till plockningar för utgående flöden verifierar [!INCLUDE [prod_short](includes/prod_short.md)] att alla villkor är uppfyllda.

När villkoren inte är uppfyllda visas felmeddelanden. Ett vanligt meddelande är det allmänna "finns inget att hantera". -meddelande. Meddelandet kan visas av flera olika orsaker, både i utgående och inkommande flöden, där en dokumentrad innehåller fältet **Ant. att hantera**.

## <a name="bin-content-and-reservations"></a><a name="bin-content-and-reservations"></a>Lagerplatsinnehåll och reservationer

Artikelantal finns både som dist.lager transaktioner och som artikeltransaktioner i lager. Dessa två transaktionstyper innehåller information om var artiklarna finns och om de är tillgängliga. Distributionslagertransaktioner definierar en artikels tillgänglighet per lagerplats och lagerplatstyp, vilket kallas lagerplatsinnehåll. Artikeltransaktioner definierar en artikels disposition genom dess reservation till avgående dokument.  

[!INCLUDE [prod_short](includes/prod_short.md)] beräknar den kvantitet som är tillgänglig för plockning när lagerplatsinnehållet kopplas till reservationer.  

## <a name="quantity-available-to-pick"></a><a name="quantity-available-to-pick"></a>Disponibelt antal att plocka

[!INCLUDE [prod_short](includes/prod_short.md)] reserverar artiklar för pågående leveranser av försäljningsorder så att de inte plockas för andra försäljningsorder som levereras tidigare. [!INCLUDE [prod_short](includes/prod_short.md)] subtraherar antal artiklar som redan bearbetas enligt följande:

* Kvantiteter som reserverats för andra utgående dokument.
* Antal för befintliga plockningsdokument.
* Kvantiteter som plockats men ännu inte levererats eller förbrukats.  

Resultatet beräknas dynamiskt och visas i fältet **Disponibelt att plocka** på sidan **Plockningskalkylark**. Värdet beräknas också när användaren skapar distributionslagerplockningarna direkt för avgående dokument. Följande utgående källdokument finns:

* Försäljningsorder
* Produktionsförbrukning
* Avgående överföringar

Resultatet blir tillgängligt i dessa dokument i kvantitetsfälten, till exempel i fältet **Ant. att hantera**.  

> [!NOTE]  
> För prioriteten för reservationer subtraheras antalet som ska reserveras från antalet som är disponibelt att plockas. Till exempel om antalet som är tillgängligt på plocklagerplatser är 5 enheter, men 100 enheter finns på införsel-lagerplatser, och du försöker att reservera mer än 5 enheter för ytterligare en order, kommer ett felmeddelande visas eftersom den här extra kvantiteten måste vara tillgänglig på plocklagerplatser.  

### <a name="calculating-the-quantity-available-to-pick"></a><a name="calculating-the-quantity-available-to-pick"></a>Beräknar disponibelt antal att plocka

[!INCLUDE [prod_short](includes/prod_short.md)] beräknar antalet som är tillgängligt att plocka så här:  

disponibelt antal att plocka = antal på plocklagerplatser – antal i plockning och transport – (reserverat antal på plocklagerplatser + reserverat antal i plockning och transport)  

Följande diagram visar de olika elementen i beräkningen.  

![Tillgänglig för plockning med reservationsöverlappning.](media/design_details_warehouse_management_availability_2.png "Tillgänglig för plockning med reservationsöverlappning")  

## <a name="quantity-available-to-reserve"></a><a name="quantity-available-to-reserve"></a>Disponibelt antal att reservera

Eftersom begreppen för lagerplatsinnehåll och reservation finns till samtidigt, måste antalet artiklar som är disponibla att reservera justeras mot fördelningar till utgående distributionslagerdokument.  

Du kan reservera alla lagerartiklar, utom artiklar som har startat avgående bearbetning. Antalet som är tillgängligt att reservera definieras som antalet på alla dokument och alla lagerplatstyper. Följande avgående antal är undantag:  

* Antal i oregistrerade plockdokument  
* Antal i utleveranslagerplatser  
* Antal i till-produktion-lagerplatser  
* Antal i öppna produktionslagerplatser  
* Antal i till-montering-lagerplatser  
* Antal på justeringlagerplatser  

Resultatet visas i fältet **Totalt disponibelt antal** på sidan **Reservation**.  

På en reservationsrad visas antalet som inte kan reserveras, eftersom det har fördelats i distributionslagret, i fältet **Fördelat antal i dist.lager** på sidan **Reservation**.  

### <a name="calculating-the-quantity-available-to-reserve"></a><a name="calculating-the-quantity-available-to-reserve"></a>Beräknar disponibelt antal att reservera

[!INCLUDE [prod_short](includes/prod_short.md)] beräknar antalet som är tillgängligt att reservera så här:  

disponibelt antal att reservera = totalt antal i lager – antal i plockning och transport för källdokument – reserverat antal – antal i avgående lagerplatser  

Följande diagram visar de olika elementen i beräkningen.  

![Tillgänglig för reservering per lagerställefördelning.](media/design_details_warehouse_management_availability_3.png "Tillgänglig för reservering per lagerställefördelning")  

## <a name="see-also"></a><a name="see-also"></a>Se även

[Översikt över Warehouse Management: ](design-details-warehouse-management.md)
[Visa artiklarnas disposition](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
