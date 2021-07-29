---
title: Försäljningsrapporter och -analyser
description: Se vilka försäljningsrapporter och analyser som är tillgängliga i standardversionen av Business Central så att du kan hålla reda på din verksamhet.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 76f93a75f9f7fd52b2495d75bffe648d53f9c844
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543253"
---
# <a name="sales-reports-and-analytics-in-business-central"></a>Försäljningsrapporter och analys i Business Central

Med försäljningsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] kan försäljnings- och affärspersonal få insikter och statistik om aktuella och tidigare försäljningsaktiviteter.  

## <a name="reports"></a>Rapporter

I följande tabell beskrivs några av de viktigaste rapporterna inom försäljningsrapportering.

|Rapportera |Objekt-ID|Beskrivning  |
|---------|---------|---------|
|**Kund - ordersammandrag**|107| Visar orderinformation med kvantitet som ännu ej skickats för varje kund i tre perioder om 30 dagar, med början från det angivna datumet. Det visas också kolumner med order som ska levereras innan och efter de tre perioderna och en kolumn med total per kund. Använd rapporten för att analysera ett företags förväntade försäljningsvolym. |
|**Kunder - 10 i topp**|111| Visar information om kunders inköp och saldon under en vald period. Du kan välja antalet kunder som ska tas med i rapporten. Det är bara kunder som har inköp under perioden, eller ett saldo vid slutet av perioden, som kommer att tas med i rapporten.<br>Kunderna sorteras efter belopp och du kan välja om de ska sorteras per försäljningsbelopp eller saldo. Rapporten ger en snabb överblick över kunder som har köpt mest eller som är skyldiga mest.|
|**Kunder/artikelförsäljning**|113|Visar en lista över artikelförsäljning för varje kund under en vald tidsperiod. Rapporten innehåller information om antal, försäljningsbelopp, vinst och möjlig rabatt. Rapporten kan t.ex. användas för att analysera ett företags kundgrupper.|
|**Lager - kundförsäljning**|713|En översikt ur distributionslagrets perspektiv. Det här är en annan vy jämfört med rapporten **Kund/artikelförsäljning**, och visar artikeln först och sedan kunden som köpte produkten.|
|**Kund - försäljningslista**|119|Visar kundförsäljningen för en period. Den används vid rapporter till tull- och skattemyndigheter. Du kan välja att endast ta med kunder med en total försäljning som överstiger ett minimibelopp. Du kan också ange om du vill att rapporten ska innehålla adressuppgifter för alla kunder.<br>Rapporten baseras på registrerad försäljning (BVA) från kundreskontratransaktioner. Längst ned i rapporten visas den totala rapporterade försäljningen i BVA. Totalsumman baseras på de kunder du har tagit med i rapporten, det vill säga de kunder som finns inom filtren på snabbfliken Kund som har en större totalförsäljning än det belopp som angetts i fältet **Belopp (BVA) större än**, på snabbfliken **Alternativ**.|
|**Kundreskontralista**|121|Visar detaljerade saldon för valda kunder. Använd rapporten i samband med att du avslutar en bokföringsperiod eller ett räkenskapsår.|
|**Kund – råbalans**|129|Visar detaljerade saldon för valda kunder. Du kan använda rapporten för att kontrollera att saldot för en kundbokföringsmall är lika med saldot på motsvarande redovisningskonto för ett visst datum. Använd rapporten i samband med att du avslutar en bokföringsperiod eller ett räkenskapsår. Om du behöver en mer detaljerad version av den här typen av rapport använder du rapporten **Kund detaljerad råbalans** (104).|
|**Försäljningsstatistik**|112|[!INCLUDE [reports-sales-statistics](includes/reports-sales-statistics.md)] |
|**Förs.reservation disp.**|209|Visar artiklar i försäljningsdokument som är disponibla för leverans. Du bestämmer om rapporten ska visa status för varje dokument eller för varje försäljningsrad. När du skriver ut rapporten kan du också uppdatera disponibelt antal för leverans i fältet **Skickas antal** på försäljningsraderna. Sedan kan du med rapportens hjälp bestämma vilka dokument som ska bokföras.<br>Det finns också en funktion som du kan använda för att ställa in mängden varor som ska levereras. **OBS!** Den här rapporten är inte tillgänglig för avancerade distributionslagerfunktioner.|
|**Status för distributionslagerutleverans**|7313|Den här rapporten kan användas för alla platser där fältet **Kräver utleverans** har valts. I rapporten **Status för distributionslagerutleverans** visas alla ej bokförda dokument för en distributionslagerutleverans, inklusive lagerställen, lagerplatskoder, dokumentstatus osv. Den här rapporten är perfekt för att få en översikt.|
|**Lagerplockningslista**|813|Innehåller en lista över de försäljningsorder som innehåller en viss artikel. Följande information visas för respektive artikel: försäljningsorderrad med kundens namn, variantkod, lagerställekod, lagerplatskod, leveransdatum, antal att leverera och enhet. Antalet som ska levereras är summerat per artikel. Rapporten kan användas när artiklarna ska plockas från lagret.<br>**OBS!** Den här rapporten är inte tillgänglig för avancerade distributionslagerfunktioner.|
|**Lager - restorder**|718|Innehåller en lista med de orderrader vars leveransdatum har överskridits. Följande information visas om respektive order per artikel: nummer, kundnamn, kundens telefonnummer, leveransdatum, beställningskvantitet och antal på restorder. Rapporten kan även visa om kunden har andra restnoterade artiklar.|



## <a name="tasks"></a>Uppgifter

I följande artiklar beskrivs några av de viktigaste uppgifterna för att analysera verksamhetens tillstånd:

* [Skapa analysrapporter](bi-how-create-analysis-views-reports.md)  
* [Visa artikeldisposition](inventory-how-availability-overview.md)


## <a name="see-also"></a>Se även

[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Reservera artiklar](inventory-how-to-reserve-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
