---
title: Så här skapar du Operationsföljder | Microsoft Docs
description: En verksamhetsföljd innehåller standarddata som samlar processkraven för en viss producerad artikel. När en produktionsorder har skapats för den överordnade artikeln, avgör dess produktionsstruktur beräkningen av materialbehoven enligt vad som visas på sidan **Prod.orderverksamhetsföljd**.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3f2d67cae2042f2f70db155aedbb85df6e19c96e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "927384"
---
# <a name="create-routings"></a>Skapa verksamhetsföljder
Tillverkningsföretag använder verksamhetsföljder för att visa produktionsprocessen.

Operationsföljden utgör också grunden för processplanering, kapacitetsplanering, planerad fördelning av materialbehov och produktionsdokument.  

För produktionsstrukturer kopplas verksamhetsföljderna till produktionens slutartikel. En verksamhetsföljd innehåller standarddata som samlar processkraven för en viss producerad artikel. När en produktionsorder har skapats för den överordnade artikeln, avgör dess produktionsstruktur beräkningen av materialbehoven enligt vad som visas på sidan **Prod.orderverksamhetsföljd**.  

Innan du kan skapa en verksamhetsföljd måste följande vara på plats:  

- Artikelkort kan skapas för överordnade artiklar som ingår i produktionen. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).
- Produktionsresurser har ställts in. Mer information finns i [Skapa produktionsgrupper och maskingrupper](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-routing"></a>Så här skapar du en verksamhetsföljd  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Operationsföljder** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  I fältet **Typ**, markera **Seriell** för att beräkna produktionsverksamhetsföljden efter det värde som anges i fältet **Operationsnr**. .   
    Välj **Parallell** för att beräkna operationerna enligt värdet i fältet **Nästa verksamhetsnr**. .  
5.  Ställ in värdet i fältet **Status** till **Ny** eller **Under utveckling** om du vill redigera verksamhetsföljden. Aktivera den genom att ställa in fältet **Status** till **Godkänd**.  

    Så här fyller du i verksamhetsföljdrader
6.  I fältet **Operationsnr.** anger du numret för den första operationen, till exempel **10**.  
7.  I fältet **Typ** anger du vilken typ av resurs som används (till exempel **Produktionsgrupp**).  
8.  I fältet **Nr.** markerar du den resurs som ska användas (eller skriv in namnet direkt i fältet).  
9.  I fältet **Operationsföljdslänkkod** anger du en kod för att ansluta komponenten till en särskild operation. För mer information, se [Så här skapar du operationsföljdslänk](production-how-to-create-routings.md#to-create-routing-links).
10.  I fälten **Bearbetningstid** och **Omställningstid** anger du processtiderna som krävs för att genomföra operationen.

    > [!NOTE]
    > Omställningstiden beräknas per produktionsorder, och bearbetningstiden beräknas per producerad artikel.  

11.  I fältet **Samtidiga kapaciteter**, ange hur många enheter av den markerade resursen som används för att utföra operationen. Till exempel halveras körtiden om två personer tilldelas till en förpackningsoperation.  
12.  Fortsätt att fylla i rader för alla operationer som krävs för att producera den aktuella artikeln.  
13.  Om du vill kopiera rader från en befintlig verksamhetsföljd klickar du på åtgärden **Kopiera verksamhetsföljd** och väljer de befintliga raderna.  
14. Godkänn verksamhetsföljden.  
15. Nu kan du koppla den nya verksamhetsföljden till kortet för den aktuella produktionsartikeln genom att fylla i **verksamhetsföljdnr.**. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).  

> [!NOTE]  
>  Kom också ihåg att om du vill beräkna om standardkostnaden för artikeln från kortet **Artikel**: välj åtgärden **Produktion**, välj åtgärden **Beräkna standardkostnad** och välj sedan åtgärden **Alla nivåer**.  

## <a name="to-create-routing-links"></a>Så här skapar du en verksamhetsföljdslänk
Du kan skapa verksamhetsföljdslänkar för att koppla ihop komponenter med specifika operationer för att behålla deras förhållande även om produktionsstrukturen eller verksamhetsföljden ändras. Detta gör det också lättare att bokföra komponenter vid rätt tidpunkt, dvs. när den angivna kopplade operationen startar – inte när hela ordern släpps. Mer information finns i [Bokför komponenter enligt verksamhetens utflöde](production-how-to-flush-components-according-to-operation-output.md).  

En annan viktig fördel är att länkade komponenter och operationer visas i en logisk processtruktur när du använder sidan **Produktionsjournal** för bokföring av utdata och förbrukning.  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Operationsföljder** och välj sedan relaterad länk.  
2.  Öppna verksamhetsföljden som innehåller operationen du vill länka.  

    Se till att verksamhetsföljden har statusen är **Under utveckling**.  

3.  På den aktuella verksamhetsföljdsraden, i fältet **Operationsföljdslänkkod**, markera en kod.  
4.  Fortsätt genom att lägga till olika verksamhetsföljdslänkkoder i andra operationer i verksamhetsföljden, om det behövs.  

    > [!NOTE]  
    >  Du bör inte använda samma verksamhetsföljdslänkkod i olika operationer i en verksamhetsföljd, eftersom en komponent då av misstag kan länkas till två olika operationer, så att den förbrukas två gånger.  
    >   
    >  Du bör ge verksamhetsföljdslänkkoden samma namn som operationen, så att alla verksamhetsföljdslänkar blir verksamhetsspecifika.

5.  Ställ in statusen för verksamhetsföljden till **Godkänd**.  

    Operationsföljdslänkkoder tilldelas nu till operationer. Nu måste du skapa den faktiska länken genom att tilldela samma koder till specifika komponenter i den aktuella produktionsstrukturen.  

6.  Öppna den **produktionsstruktur** som innehåller komponenterna som du vill länka till operationerna ovan. För mer information, se [Skapa produktionsstrukturer](production-how-to-create-production-boms.md).
7.  Se till att strukturen har statusen **Under utveckling**.  
8.  På den aktuella prod.strukturraden, i fältet **Operationsföljdslänkkod**, markera koden som du precis har tilldelat den aktuella operationen.  
9. Fortsätt genom att lägga till verksamhetsföljdslänkkoder till andra komponenter utifrån de unika operationer där de används.  
10. Ställ in statusen för produktionsstrukturen till **Godkänd**.  

    > [!NOTE]  
    >  Om du vill aktivera verksamhetsföljdslänkar för en befintlig produktionsorder måste du först uppdatera den. För mer information, se [Skapa produktionsorder](production-how-to-create-production-orders.md).  

De markerade komponenterna länkas till de markerade operationerna när du skapar eller uppdaterar en produktionsorder som använder den aktuella produktionsstrukturen och verksamhetsföljden. Detta visas på sidan **Prod. Ordern komponenter** under produktionsordern, och där kan du också ta bort och lägga till de definierade verksamhetsföljdslänkkoderna när som helst.

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a>Tilldela personal, verktyg och kvalitetsmått för verksamhetsföljdsuppgifter.
Om du behöver personal med kvalifikationer, specialkunskaper eller särskild behörighet för en operation kan du tilldela sådan personal till operationen. Dessutom kan du tilldela åtgärden med verktyg och kvalitet. Nedan beskrivs hur du tilldelar personal: Momentet är liknande för andra typer av åtgärdsinformation.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Operationsföljder** och välj sedan relaterad länk.  
2.  Öppna relevant verksamhetsföljd.  
3.  På snabbfliken **rader** markerar du raden som du vill behandla och klickar på åtgärden **personal**.  
4.  Fyll i fälten på sidan **Operationsföljd personal**.  
5.  Välj **OK** för att stänga sidan. Angivna värden kopieras och tilldelas till operationen.    

## <a name="to-create-a-new-versions-of-a-routing"></a>Så här skapar du nya versioner av verksamhetsföljder  
Med versionsprincipen kan du hantera flera versioner av en verksamhetsföljd. Strukturen på verksamhetsföljdsversionen motsvarar strukturen på verksamhetsföljden som består av huvud och rader. Den grundläggande skillnaden definieras av startdatumet.  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Operationsföljder** och välj sedan relaterad länk.  
2.  Markera verksamhetsföljden som ska kopieras och klicka på åtgärden **versioner**.  
3. På sidan **verksamhetsföljdversioner** väljer du åtgärden **Ny**.
4. Fyll i fälten om det behövs.
5.  I fältet **Versionskod** anger du en identifiering som är unik för versionen. Du kan använda valfria siffror och bokstäver.  

    Den nyskapade versionen tilldelas automatiskt statusen **Ny**.  
6.  Om du vill skapa rader för åtgärden, markera den första tomma raden och fyll i **Åtgärdsnr.** enligt verksamhetssekvensen.

    Raderna i operationen sorteras i stigande ordning efter operationsnummer. Du rekommenderas välja tillräcklig bredd för det här steget för att kunna göra ändringar senare. **Nästa verksamhetsnr.** Fältet refererar till följande operation. Operationsnumret kan anges direkt.

7. När verksamhetsföljdversionen har slutförts kan du ange **Status** till **godkänd**.

Versionens giltighetstid anges i fältet **Startdatum**.  

## <a name="see-also"></a>Se även  
[Skapa produktionsstrukturer](production-how-to-create-production-boms.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planerad](production-planning.md)   
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
