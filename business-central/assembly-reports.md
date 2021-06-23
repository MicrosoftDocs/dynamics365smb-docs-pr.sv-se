---
title: Monteringsrapporter och analys i Business Central
description: Se vilka monteringsrapporter och analyser som är tillgängliga i standardversionen av Business Central så att du kan hålla reda på din verksamhet.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 91234cd02736d425116be40137efd9d068b5bd97
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216405"
---
# <a name="assembly-reports-and-analytics-in-business-central"></a>Monteringsrapporter och analys i Business Central

Med monteringsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] kan produktions- och affärspersonal få insikter och statistik om aktuella och tidigare monteringsaktiviteter.  

## <a name="reports"></a>Rapporter

I följande tabell beskrivs några av de viktigaste rapporterna inom monteringsrapportering.

|Rapportera |Objekt-ID|Beskrivning  |
|---------|---------|---------|
|**Monteringsstrukturer**|801|Visar en lista över strukturer: namn, strukturnummer, strukturkomponenter samt övriga strukturer som ingår i strukturen. Strukturkomponenterna definieras i tabellen Strukturkomponent. Här visas även enhet och nödvändigt antal för varje komponent per basenhet. |
|**Artikel – Kan skapa (tid)**|5871|Visar hur fem olika nyckeltillgänglighetstal ändras med tiden för en strukturartikel. Dessa siffror ändras utifrån förväntad tillgång och efterfrågan och utifrån tillgång baserat på tillgängliga komponenter som kan monteras eller produceras.<br>Du kan använda rapporten för att se om du kan uppfylla en försäljningsorder för en artikel på ett angivet datum genom att se den aktuella tillgängligheten i kombination med potentiellt antal av komponenterna som kan tillhandahållas om en monteringsorder startas. I rapporten visas när och hur många enheter för montering och produktionsartikel som du kan göra baserat på komponentdisposition och artikelns aktuella tillgänglighet. Detta visas som den totala kvantiteten.<br>Informationen visas i ett diagram där varje tillgänglighetssiffra är en rad längs med tidslinjen och som flyttas uppåt och nedåt vid kvantitetsändringar. Kvantitetssiffrorna kommer från samma motor som ger information till fönstret **Artikeldisposition på strukturnivå**. |
|**Kostnadsandeldistribution för struktur**|5872|Visar grafiskt hur en montering eller producerad artikels kostnad är fördelad via dess struktur.<br>Sådan information kan vara praktisk för att bestämma om du vill byta komponentleverantör, ersätta intern kapacitetsförbrukning med utlagd tillverkning, eller tvärtom, och när du granskar och ändrar en artikels struktur.<br>Det första diagrammet i rapporten innehåller den totala styckkostnaden för den överordnade artikelns komponenter och arbetsresurser, specificerade i upp till fem olika kostnadsandelar, som visas grafiskt med olika färger.<br>Cirkeldiagrammet med texten *Material/arbete* visar den proportionella distributionen mellan den överordnade artikelns material och arbetskostnad, samt produktionsomkostnader. Materialkostnadsandelen inkluderar artikelns materialkostnader. Arbetskostnadsandelen inkluderar kapacitet, omkostnad för kapacitet och underleverantörskostnader. Kostnadsandelarna visas på olika sätt beroende på dina val i fältet **Visa endast**.<br>Cirkeldiagrammet med texten *Direkt/indirekt* visar den proportionella distributionen mellan den överordnade artikelns direkta och indirekta kostnader. Direktkostnadsandelen inkluderar artikelns materialkostnad, kapacitetskostnad och underleverantörskostnad. Den indirekta kostnaden inkluderar omkostnad för kapacitet och omkostnad för produktion.<br>Tabellen längst ned i rapporten tas med när du markerar kryssrutan Inkludera detaljer. Detta visar valda värden från fönstret Strukturkostnadsandelar på en nivå eller summerat, beroende på vilket alternativ du väljer i fältet Visa kostnadsandelar.|
|**Lista över användning**|809|Visar en lista över vilka strukturer de valda artiklarna ingår i. En användbar översikt om du måste ändra en komponent i en struktur som har infogats i en monteringsartikel. Om din leverantör till exempel inte längre levererar en viss artikel som du har använt till montering/produktion. I så fall ger rapporten en enkel översikt över vilka strukturer komponenten ingår i. Du kan ange ett filter för numret på komponenten.|
|**Struktur – råmaterial**|810|I den här rapporten kan du få en översikt över de komponenter som behövs, både för montering och för produktion. Du kan se lager, basenhet, huvudleverantör om leverantörsnr har angetts i själva artikelkortet och ledtidsberäkningen.|
|**Struktur – undersammansättning**|811|Om du producerar och/eller monterar underenheter, kan du använda den här rapporten för att få en översikt över den här typen av komponent. I den här rapporten visas basenheten, lagersaldot, styckkostnaderna och ett alternativt artikelnummer. |
|**Monteringsstruktur – färdiga varor**|812|Innehåller en lista över artiklar eller strukturer som inte motsvarar strukturkomponenter. **Obs!** Den här rapporten är inte begränsad till enbart struktur, så kom ihåg att ställa in filter i fälten **Monteringsstruktur** eller **Återanskaffningssystem**|
|**Montering mot kundorder – Försäljning**|915|Visar viktiga försäljningssiffror för monteringskomponentartiklar som kan säljas både som en del av en montering i montering mot kundorder-försäljning och som en separat artikel direkt från lagret.<br>Använd den här rapporten för att analysera antal, kostnad, försäljning, vinst och siffrorna av monteringskomponenter för att hantera affärsbeslut, till exempel om du ska prissätta en sats olika eller för att avbryta eller börja använda en speciell artikel i monteringar.<br>Raden **I montering** visar försäljningssiffror för totala antal som ska säljas som en del av en monteringsartikel. Den specifika monteringsartikelförsäljning som leder fram till slutsumma visas om du väljer fältet **Visa monteringsdetaljer**.<br>Fokus ligger på monteringskomponenterna, men beloppen beräknas från vinstmarginalen av sin överordnade, monteringsartikeln. Därefter beräknas försäljningsbelopp för varje komponent från den egna kostnaden och vinstmarginalen av dess överordnade i följande formel.<br>Rapporten innehåller information om artiklar som uppfyller ett eller båda av följande kriterier:<br>– Finns i monteringsstruktur av en artikel som använder monteringsmetoden Montering mot kundorder.<br>– Har sålts som en del av montering mot kundorder-försäljning.|

## <a name="tasks"></a>Uppgifter

I följande artiklar beskrivs några av de viktigaste uppgifterna för att analysera verksamhetens tillstånd:

* [Visa artikeldisposition](inventory-how-availability-overview.md)

## <a name="see-also"></a>Se även

[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med strukturer](inventory-how-work-boms.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
