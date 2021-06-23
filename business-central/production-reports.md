---
title: Produktionsrapporter och -analyser
description: Se vilka produktionsrapporter och analyser som är tillgängliga i standardversionen av Business Central så att du kan hålla reda på din verksamhet.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 0cacf41f0a055267af5b0ce5a8b68b34d86a1cb5
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216403"
---
# <a name="production-reports-and-analytics-in-business-central"></a>Produktionsrapporter och analys i Business Central

Med produktionsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] kan produktions- och affärspersonal få insikter och statistik om aktuella och tidigare produktionsaktiviteter.  

## <a name="reports"></a>Rapporter

I följande tabell beskrivs några av de viktigaste rapporterna inom produktionsrapportering.

|Rapportera |Objekt-ID|Beskrivning  |
|---------|---------|---------|
|**Expandering struktur**|99000753|Visar en indragen struktur för den eller de artiklar du väljer med filtren. Produktionsstrukturen är helt expanderad för alla nivåer.|
|**Artikel – Kan skapa (tid)**|5871|Visar hur fem olika nyckeltillgänglighetstal ändras med tiden för en strukturartikel. Dessa siffror ändras utifrån förväntad tillgång och efterfrågan och utifrån tillgång baserat på tillgängliga komponenter som kan monteras eller produceras.<br>Du kan använda rapporten för att se om du kan uppfylla en försäljningsorder för en artikel på ett angivet datum genom att se den aktuella tillgängligheten i kombination med potentiellt antal av komponenterna som kan tillhandahållas om en monteringsorder startas. I rapporten visas när och hur många enheter för montering och produktionsartikel som du kan göra baserat på komponentdisposition och artikelns aktuella tillgänglighet. Detta visas som den totala kvantiteten.<br>Informationen visas i ett diagram där varje tillgänglighetssiffra är en rad längs med tidslinjen och som flyttas uppåt och nedåt vid kvantitetsändringar. Kvantitetssiffrorna kommer från samma motor som ger information till fönstret **Artikeldisposition på strukturnivå**. |
|**Kostnadsandeldistribution för struktur**|5872|Visar grafiskt hur en montering eller producerad artikels kostnad är fördelad via dess struktur.<br>Sådan information kan vara praktisk för att till exempel bestämma om du vill byta komponentleverantör, ersätta intern kapacitetsförbrukning med utlagd tillverkning, eller tvärtom, och när du granskar och ändrar en artikels struktur.<br>Det första diagrammet i rapporten innehåller den totala styckkostnaden för den överordnade artikelns komponenter och arbetsresurser, specificerade i upp till fem olika kostnadsandelar, som visas grafiskt med olika färger.<br>Cirkeldiagrammet med texten *Material/arbete* visar den proportionella distributionen mellan den överordnade artikelns material och arbetskostnad, samt produktionsomkostnader. Materialkostnadsandelen inkluderar artikelns materialkostnader. Arbetskostnadsandelen inkluderar kapacitet, omkostnad för kapacitet och underleverantörskostnader. Kostnadsandelarna visas på olika sätt beroende på dina val i fältet **Visa endast**.<br>Cirkeldiagrammet med texten *Direkt/indirekt* visar den proportionella distributionen mellan den överordnade artikelns direkta och indirekta kostnader. Direktkostnadsandelen inkluderar artikelns materialkostnad, kapacitetskostnad och underleverantörskostnad. Den indirekta kostnaden inkluderar omkostnad för kapacitet och omkostnad för produktion.<br>Tabellen längst ned i rapporten tas med när du markerar kryssrutan **Inkludera detaljer**. Detta visar valda värden från fönstret Strukturkostnadsandelar på en nivå eller summerat, beroende på dina val i fältet **Visa kostnadsandelar som**.|
|**Detaljerad beräkning**|99000756|Visar en kostnadslista per artikel där kassation inkluderas.|
|**Där det används (högsta nivå)**|99000757|Visar var artikeln används i produktstrukturen, och hur mycket av den som används.<br>Rapporten visar endast artikeln som där den används när basartikeln används som artikeln på toppnivå. Om artikel "A" till exempel används för att producera artikel "B" och artikel "B" används för att producera artikel "C", visas artikel B om du kör rapporten för artikel A. Om du kör rapporten för artikel B, visas artikel C som där den används.<br>Du kan även öppna fönstret **Raden Där den används** direkt från artikeln.|
|**Jämförelselista för artikelstrukturlista**|99000758|I den här rapporten kan du jämföra liknande slutprodukter med avseende på kostnaderna. Du kan se en lista med alla komponenter och deras kostnader även efter behov. Beräkningsdatumet anges normalt av arbetsdatumet. |
|**Produktionsorderstatistik**|99000791|Anger de olika kostnader som har ackumulerats för den valda produktionsorder.<br>Innehållet i rapporten påminner om det på sidan **Produktionsorderstatistik**.<br>För produktionsorder som använder produktionsprincipen *Tillverka-mot-order*, visar fönstret endast material- och kapacitetskostnad av artiklar på den högsta strukturnivån.|
|**Kapacitet körplan**|99000780|Visar de produktionsorder som väntar på att bearbetas av produktions- och maskingrupperna. Produktionsgruppens eller maskingruppens kapacitet skrivs ut. Rapporten innehåller information om till exempel start-/sluttid och datum per produktionsorder och inflödesantal.|
|**Produktionsgruppbeläggning** eller **maskingruppbeläggning**|99000783 eller 99000784|Båda rapporter visar en lista över beläggningen i en produktions- eller maskingrupp. Produktions-/maskingruppens beläggning är summan av det antal gånger som krävs för att alla planerade och faktiska order ska kunna köras i produktionsgruppen under en viss tidsperiod.|
|**Bristlista, produktionsorder**|99000788|Den här rapporten kan användas för att se alla komponenter som inte är tillgängliga på grund av bristande lager. Översikten kan därför användas för att se i tid, om tidslinjen för en planerad eller släppt produktionsorder kan behållas.|


## <a name="tasks"></a>Uppgifter

I följande artiklar beskrivs några av de viktigaste uppgifterna för att analysera verksamhetens tillstånd:

* [Så här visar du beläggning på produktions- och maskingrupper](production-how-to-view-the-load-on-work-centers.md)  
* [Visa artikeldisposition](inventory-how-availability-overview.md)

## <a name="see-also"></a>Se även

[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
