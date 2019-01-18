---
title: "Designdetaljer - Balansera tillgång med efterfrågan | Microsoft Docs"
description: "Kärnan av planeringssystemet inbegriper att hantera tillgång och efterfrågan genom att föreslå användarhandlingar för att revidera leveransorder i händelse av obalans. Det sker per kombination av variant och lagerställe."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 037ba35395ba84d4f943b0a45a7fb43c24b34385
ms.contentlocale: sv-se
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-balancing-supply-with-demand"></a>Designdetaljer: Balansera tillgång med efterfrågan
Kärnan av planeringssystemet inbegriper att hantera tillgång och efterfrågan genom att föreslå användarhandlingar för att revidera leveransorder i händelse av obalans. Det sker per kombination av variant och lagerställe.  

Föreställ dig att varje lagerprofil innehåller en sträng med efterfråganshändelser (sorterade efter datum och prioritet) och en motsvarande sträng med tillgångshändelser. Varje händelse refererar tillbaka till sin ursprungstyp och sitt id. Reglerna för motkontering av artikeln är rättframma. Fyra instanser av matchande efterfrågan och tillgång kan uppstå när som helst under processen:  

1. Ingen efterfrågan eller försörjning finns för artikel =>planläggningen har slutförts (eller ska inte starta).  
2. Efterfrågan finns, men det finns inte någon tillgång =>tillgång bör föreslås.  
3. Tillgång finns, men det finns inte efterfrågan på den => tillgång bör annulleras.  
4. Både efterfrågan och tillgång finns => frågor ska ställas och besvaras innan systemet kan se till att efterfrågan kan uppfyllas och tillgången är tillräcklig.  

     Om tidpunkten för av leveransen inte passar, kanske leveransen kan omplaneras enligt följande:  

    1.  Om tillgången placeras tidigare än efterfrågan kan kanske tillgången planeras om så att lagret är så lågt som möjligt.  
    2.  Leverans placeras före efterfrågan, kan kanske leverans omplaneras. Annars kommer systemet att föreslå ny tillgång.  
    3.  Om tillgången uppfyller efterfrågan på datumet kan planeringssystemet fortsätta att undersöka om tillgångens antal kan täcka efterfrågan.  

     När tidsplanen är på plats kan det adekvata antal som ska levereras beräknas enligt följande:  

    1.  Om tillförselantalet är mindre än efterfrågan är det möjligt att tillförselantalet ska ökas (eller inte, om det begränsas av en princip om maximalt antal).  
    2.  Om tillförselantalet är större än efterfrågan är det möjligt att tillförselantalet kan minskas (eller inte, om det begränsas av en princip om lägsta antal).  

     I det här skedet finns någon av följande två situationer:  

    1.  Den aktuella efterfrågan kan täckas, i vilket fall den kan stängas och planeringen för nästa efterfrågan kan starta.  
    2.  Tillgången har nått sitt maximum, och en del av efterfråganskvantiteten täcks inte. I det här fallet kan planeringssystemet stänga den aktuella tillgången och gå vidare till nästa.  

 Du startar om med nästa efterfrågan och den aktuella tillgången eller vice versa. Den aktuella tillgången kan kanske täcka även nästa efterfrågan, eller den aktuella efterfrågan inte ännu inte har täckts helt.  

## <a name="rules-concerning-actions-for-supply-events"></a>Regler angående åtgärder för tillförselhändelser  
När planeringssystemet utför en beräkning uppifrån och ned där tillgången måste uppfylla efterfrågan tas efterfrågan för given, det vill säga den ligger utanför planeringssystemets kontroll. Men tillgångssidan kan hanteras. Därför får du i planeringssystemet ett förslag om att skapa nya leveransorder, att omplanera befintliga och/eller ändra partistorleken. Om en befintlig leveransorder blir överflödig föreslår planeringssystemet att användaren annullerar den.  

Om användaren vill exkludera en befintlig leveransorder från planeringsförslagen, kan han ange att den inte har någon planeringsflexibilitet (Planeringsflexibilitet = Ingen). Överskjutande tillgång för ordern används för att täcka efterfrågan, men ingen åtgärd föreslås.  

I allmänhet har totala tillgång en planeringsflexibilitet som begränsas av villkoren för var och en av de föreslagna åtgärderna.  

-   **Omplanera ut**: Datumet på en befintlig leveransorder kan omplaneras ut för att uppfylla efterfrågans förfallodatum om inte:  

    -   Det representerar lager (alltid på dag noll).  
    -   Den har en order-till-order som är kopplad till en annan efterfrågan.  
    -   Det ligger utanför omplaneringssidan definierat av tidsenheten.  
    -   Det finns en närmare tillgång som kan användas.  
    -   Å andra sidan kan användaren bestämma att inte ändra tidpunkten eftersom:  
    -   Leveransordern redan har kopplats till en annan efterfrågan på ett tidigare datum.  
    -   Den nödvändiga omplaneringen är så minimal att användaren anser den vara försumbar.  

-   **Omplanera in**: Datumet på en befintlig leveransorder kan omplaneras in, utom i följande villkor:  

    -   Det är direkt kopplat till vissa övriga behov  
    -   Det ligger utanför omplaneringssidan definierat av tidsenheten.  

> [!NOTE]  
>  När du planerar en artikel med hjälp av en beställningspunkt, kan leveransorder alltid planeras in om det behövs. Det är vanligt i framåtplanerade leveransorder som aktiveras av en beställningspunkt.  

-   **Öka antalet**: Antalet på en befintlig leveransorder kan ökas för att uppfylla efterfrågan, såvida inte leveransordern är kopplad direkt till en efterfrågan av order-till-order-koppling.  

> [!NOTE]  
>  Även om det är möjligt att öka leveransorder, kan den begränsas på grund av en definierad maximal partistorlek.  

-   **Minska antalet**: En befintlig leveransorder med ett överskott som jämförs med en befintlig efterfrågan kan minskas för att uppfylla efterfrågan.  

> [!NOTE]  
>  Även om antalet kan minskas kan det fortfarande finns ett överskott jämfört med efterfrågan på grund av en definierad lägsta partistorlek eller flera order.  

-   **Annullera**: Som ett specialfall av åtgärden minska antal kan leveransordern annulleras om den har minskats till noll.  
-   **Ny**: Om ingen leveransorder redan finns, eller en befintlig inte kan ändras så att den uppfyller behovskvantiteten på det efterfrågade förfallodatumet, föreslås en ny leveransorder.  

## <a name="determining-the-supply-quantity"></a>Fastställa tillgångsantalet  
Planeringsparametrar som definieras av användaren styr det föreslagna antalet för varje leveransorder.  

När planeringssystemet beräknar antalet på en ny leveransorder eller antalsändringen på en befintlig leveransorder kan det föreslagna antalet skilja sig från det som faktiskt begärdes.  

Om ett maximalt lager eller en fast orderkvantitet väljs kan det föreslagna antalet ökas för att uppfylla det fasta antalet eller det maximal lagret. Om en partiformningsmetod använder en beställningspunkt kan antalet ökas minst för att uppfylla beställningspunkten.  

 Det föreslagna antalet kan ändras i den här sekvensen:  

1. Ned till den maximala partistorleken (om en sådan finns).  
2. Upp till minsta partistorlek  
3. Upp till den närmaste ordermultipeln. (I händelse av felaktiga inställningar kan detta överträda maximal partistorlek).  

## <a name="order-tracking-links-during-planning"></a>Orderspårninglänkar under planering  
Angående orderspårning under planering är det viktigt att nämna att planeringssystemet ordnar om de dynamiskt skapade orderspårninglänkarna för kombinationerna av artikel/variant/lagerställe.  

Det finns två orsaker till detta:  

-   Planeringssystemet måste kunna motivera sina förslag: att alla behov har täckts, och att inga leveransorder är överflödiga.  
-   Dynamiskt skapade orderspårningslänkar måste balanseras om regelbundet.  

Med tiden blir dynamiska orderspårninglänkar obalanserade eftersom hela orderspårningsnätverket inte struktureras om förrän en efterfrågans- eller tillgångshändelse faktiskt stängs.  

Innan tillgången balanseras efter efterfrågan tar programmet bort alla befintliga orderspårningslänkar. Under motkonteringen, när en efterfrågans- eller en tillgångshändelse stängs skapar den nya orderspårninglänkar mellan tillgång och efterfrågan.  

> [!NOTE]  
>  Även om artikeln inte ställts in för dynamisk orderspårning skapar det planerade systemet balanserade orderspårningslänkar som förklaras ovan.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Balansera efterfrågan och tillgång](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Centrala koncept i planeringssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)

