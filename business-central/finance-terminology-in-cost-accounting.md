---
title: Terminologi i kostnadsredovisning | Microsoft Docs
description: I det här avsnittet definieras de viktigaste begreppen som används i kostnadskalkylering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b82b5dce54d9427fbd653bd8dd185d4c086d0459
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923901"
---
# <a name="terminology-in-cost-accounting"></a>Terminologi i kostnadsredovisning
I det här avsnittet definieras de viktigaste begreppen som används i kostnadskalkylering.  

## <a name="key-terms"></a>Begrepp  
 Följande tabell visar definitioner av de viktigaste begreppen i kostnadskalkylering.  

|**Term**|**Definition**|  
|--------------|--------------------|  
|Fördelningsnyckel|Fördelningsnyckeln utgör basen som används för att fördela kostnader. Det är vanligtvis ett antal, till exempel kvadratmeter, antal anställda eller använda man-timmar. Exempelvis två avdelningar med 20 respektive 10 anställda som delar på lunchrumskostnaderna. Kostnaderna fördelas mellan avdelningarna genom att använda en fördelningsnyckel som representerar antalet anställda. Två tredjedelar av kostnaderna fördelas på den första avdelning och en tredjedel fördelas på den andra avdelningen.|  
|Fördelningskälla|Fördelningskällan bestämmer vilka kostnader som fördelas. Fördelningar definieras i tabeller för fördelningskällor och fördelningsmål. Varje fördelning består av en fördelningskälla och en eller flera fördelningsmål. Alla kostnader för uppvärmning som är en fördelningskälla kan t.ex. fördelas på kostnadsställena för verkstaden, produktionen och säljavdelningen, som i sin tur är fördelningsmål.|  
|Fördelningsmål|Fördelningsmålen bestämmer vart kostnaderna fördelas. Fördelningar definieras i tabeller för fördelningskällor och fördelningsmål. Varje fördelning består av en fördelningskälla och en eller flera fördelningsmål. Alla kostnader för uppvärmning som är en fördelningskälla kan t.ex. fördelas på kostnadsställena för verkstaden, produktionen och säljavdelningen, som i sin tur är fördelningsmål.|  
|Kostnadsredovisning|I kostnadsredovisning registreras faktiska kostnader för drift, processer, avdelningar eller produkter. De här kostnaderna fördelas på kostnadsställen och kostnadsbärare, genom att använda olika kostnadsfördelningsmetoder. Chefer använder statistik och rapporter, till exempel kostnadsfördelningsblad och vinstanalys, för att fatta beslut och reducera kostnader. Kostnadsredovisningen hämtar data från redovisningen, men de fungerar oberoende av varandra. Därför påverkar transaktioner som har bokförts i kostnadsredovisningen inte data i redovisningen.|  
|Kostnadstyp|Planen för kostnadstyper har samma funktion som kontoplanen för redovisningskonton. De struktureras ofta på liknande sätt. Därför är det möjligt att överföra kontoplanen för redovisningen till planen för kostnadstyper och sedan att ändra den. Kontoplanen för kostnadstyper kan även skapas från början.|  
|Kostnadsställe|Kostnadsställen är oftast avdelningar och resultatenheter som ansvarar för kostnader och intäkter. Kostnadsställen kan synkroniseras med dimensioner i redovisningen. Det är också möjligt att lägga till nya kostnadsställen som definierar egna sorteringar med delsumma.|  
|Kostnadsbärare|Kostnadsbärare är produkter, produktgrupper eller tjänster i ett företag, färdiga varor i ett företag, som bär de slutliga kostnaderna. Kostnadsbärarna går att synkronisera med dimensioner i redovisningen. Det är också möjligt att lägga till nya kostnadsbärare som definierar egna sorteringar med delsumma.|  
|Kostnadsfördelning|Kostnadsfördelningen är en process som fördelar kostnader på kostnadsställen eller kostnadsbärare. Till exempel fördelas timpenningen för lastbilsföraren på försäljningsavdelningen på kostnadsstället för försäljningsavdelningen. Du behöver inte koppla timpenning till andra kostnadsställen. Ett annat exempel är att kostnaden för ett kostsamt datorsystem fördelas på produkterna i företaget som använder systemet.|  
|Dynamisk fördelning|Dynamisk fördelning är beroende av fördelningsbaser som kan ändras, till exempel antal anställda på en avdelning eller försäljningsintäkter av ett projekt under en viss tid. Det finns nio fördefinierade dynamiska fördelningsbaser som användare kan definiera med hjälp av fem filter.|  
|Direkt kostnad|Direkta kostnader är kostnader som kan hänföras direkt till en kostnadsbärare, till exempel ett material som köps för en viss produkt.|  
|Fast kostnad|Fasta kostnader är de kostnader som inte beror på vilken mängd varor eller tjänster som produceras av verksamheten. De tenderar att vara relaterade till tid, till exempel lön eller hyra att betalas per månad. De är i motsats till rörliga kostnader, som är volymrelaterade och betalas per det antal som tillverkas.|  
|Indirekt kostnad|Indirekta kostnader går inte att direkt fördela på en kostnadsbärare, till exempel en särskild funktion eller produkt. De indirekta kostnaderna kan vara antingen fasta eller rörliga. Indirekta kostnader kan vara skatt, administration, personal och säkerhetskostnader och kallas också omkostnader.|  
|Nivå|Nivån används för att definiera en order. Nivå anges som ett tal mellan 1 och 99. Fördelningsbokföringen följer ordningen på nivåerna. Exempelvis ser nivå till att administration först fördelas på verkstaden innan verkstaden fördelas på fordon och produktion.|  
|Fast fördelning|Fast fördelning baseras på fasta värden, till exempel kvadratmeter, eller en fördelningssats, till exempel 5:2:4.|  
|Rörelsekostnad|Rörelsekostnader är återkommande kostnader som är relaterade till driften i en verksamhet, en enhet och en komponent.|  
|Omkostnad|Omkostnader refererar till pågående kostnader för att driva en verksamhet. De är alla kostnader i resultaträkningen utom direkt arbete, direkt material och direkta kostnader. Omkostnader innefattar redovisningskostnader, annonsering, avskrivning, försäkringar, räntor, juridiska arvoden, hyra, reparation, förbrukningsvaror, skatter, telefonräkningar, resor och verktyg.|  
|Stegvis rörlig kostnad|Stegvis rörliga kostnader ändras dramatiskt vid vissa tidpunkter eftersom de avser stora inköp som inte är spridda över tiden. En anställd kan till exempel producera 100 bord på en månad. Den anställdes lön är konstant i intervallet ett till 100 bord. Om företaget vill kunna producera 110 bord behövs två anställda. Alltså blir kostnaden dubbel.|  
|Andel|Den delen som fördelas mellan kostnadsställen eller kostnadsbärare.|  
|Fast viktning|Kostnader fördelas enligt fördelningsnycklar, som kan ändras genom att använda en multiplikator. <br />Exempelvis två avdelningar med 20 respektive 10 anställda som delar på lunchrumskostnaderna. Kostnaderna fördelas mellan avdelningarna genom att använda en fördelningsnyckel som representerar antalet anställda som äter i matsalen. På den första avdelning äter endast anställda fem i matsalen, så den avdelningen har en multiplikator på 0,25. Basen för fördelningen är 20 x 0,25 = 5. Det totala antalet anställda som äter i matsalen är 15. EN tredjedel av kostnaderna fördelas på den första avdelning och två tredjedelar fördelas på den andra avdelningen.|  
|Rörlig kostnad|Rörliga kostnader är kostnader som ändras i proportion till aktiviteten i en verksamhet. Rörliga kostnader är summan av marginalkostnaderna utslaget på alla producerade enheter. Fasta kostnader och rörliga kostnader utgör de två komponenterna i den totala kostnaden.|  
|Variant|En variant används som en valfri användardefinierad etikett för fördelningar. Syftet med etiketten är att filtrera fördelningsgrupper.|  

## <a name="see-also"></a>Se även  
 [Om kostnadsredovisning](finance-about-cost-accounting.md)   
 [Redovisa kostnader](finance-manage-cost-accounting.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
