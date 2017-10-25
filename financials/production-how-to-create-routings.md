---
title: "Så här skapar du Operationsföljder | Microsoft Docs"
description: "En operationsföljd innehåller standarddata som samlar processkraven för en viss producerad artikel. När en produktionsorder har skapats för den överordnade artikeln, avgör dess produktionsstruktur beräkningen av materialbehoven enligt vad som visas i fönstret **Prod.orderoperationsföljd**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 166d85bbcf7d97cb513ba668e41fc4a179d8fcc3
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-routings"></a>Så här skapar du operationsföljder
Tillverkningsföretag använder operationsföljder för att visa produktionsprocessen.

Operationsföljden utgör också grunden för processplanering, kapacitetsplanering, planerad tilldelning av materialbehov och produktionsdokument.  

För produktionsstrukturer kopplas operationsföljderna till produktionens slutartikel. En operationsföljd innehåller standarddata som samlar processkraven för en viss producerad artikel. När en produktionsorder har skapats för den överordnade artikeln, avgör dess produktionsstruktur beräkningen av materialbehoven enligt vad som visas i fönstret **Prod.orderoperationsföljd**.  

Innan du kan skapa en operationsföljd måste följande vara på plats:  

- Artikelkort kan skapas för överordnade artiklar som ingår i produktionen. Mer information finns i [Så här registrerar du nya produkter](inventory-how-register-new-items.md).
- Produktionsresurser har ställts in. Mer information finns i [Så här skapar du en Produktionsgrupp och Maskingrupp](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-routing"></a>Så här skapar du en operationsföljd  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Operationsföljder** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  I fältet **Typ**, markera **Seriell** för att beräkna produktionsoperationsföljden efter det värde som anges i fältet **Operationsnr**. .   
    Välj **Parallell** för att beräkna operationerna enligt värdet i fältet **Nästa operationsnr**. .  
5.  Ställ in värdet i fältet **Status** till **Ny** eller **Under utveckling** om du vill redigera operationsföljden. Aktivera den genom att ställa in fältet **Status** till **Godkänd**.  

    Så här fyller du i operationsföljdrader
6.  I fältet **Operationsnr.** anger du numret för den första operationen, till exempel **10**.  
7.  I fältet **Typ** anger du vilken typ av resurs som används (till exempel **Produktionsgrupp**).  
8.  I fältet **Nr.** markerar du den resurs som ska användas (eller skriv in namnet direkt i fältet).  
9.  I fältet **Operationsföljdslänkkod** anger du en kod för att ansluta komponenten till en särskild operation. För mer information, se Så här skapar du en operationsföljdslänk.
10.  I fälten **Bearbetningstid** och **Omställningstid** anger du processtiderna som krävs för att genomföra operationen.  

    > [!NOTE]  
    >  Omställningstiden beräknas per produktionsorder, och bearbetningstiden beräknas per producerad artikel.  

11.  I fältet **Samtidiga kapaciteter**, ange hur många enheter av den markerade resursen som används för att utföra operationen. Till exempel halveras körtiden om två personer tilldelas till en förpackningsoperation.  
12.  Fortsätt att fylla i rader för alla operationer som krävs för att producera den aktuella artikeln.  
13.  Om du vill kopiera rader från en befintlig operationsföljd klickar du på åtgärden **Kopiera operationsföljd** och väljer de befintliga raderna.  
14. Godkänn operationsföljden.  
15. Nu kan du koppla den nya operationsföljden till kortet för den aktuella produktionsartikeln genom att fylla i **operationsföljdnr.**. Mer information finns i [Så här registrerar du nya produkter](inventory-how-register-new-items.md).  

> [!NOTE]  
>  Kom också ihåg att om du vill beräkna om standardkostnaden för artikeln från kortet **Artikel**: välj åtgärden **Produktion**, välj åtgärden **Beräkna standardkostnad** och välj sedan åtgärden **Alla nivåer**.  

## <a name="to-create-routing-links"></a>Så här skapar du en operationsföljdslänk
Du kan skapa operationsföljdslänkar för att koppla ihop komponenter med specifika operationer för att behålla deras förhållande även om produktionsstrukturen eller operationsföljden ändras. Detta gör det också lättare att bokföra komponenter vid rätt tidpunkt, dvs. när den angivna kopplade operationen startar – inte när hela ordern släpps. Mer information finns i [så här: bokföra komponenter enligt operationens utflöde](production-how-to-flush-components-according-to-operation-output.md).  

En annan viktig fördel är att länkade komponenter och operationer visas i en logisk processtruktur när du använder fönstret **Produktionsjournal** för bokföring av utdata och förbrukning.  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Operationsföljder** och välj sedan relaterad länk.  
2.  Öppna operationsföljden som innehåller operationen du vill länka.  

    Se till att operationsföljden har statusen är **Under utveckling**.  

3.  På den aktuella operationsföljdsraden, i fältet **Operationsföljdslänkkod**, markera en kod.  
4.  Fortsätt genom att lägga till olika operationsföljdslänkkoder i andra operationer i operationsföljden, om det behövs.  

    > [!NOTE]  
    >  Du bör inte använda samma operationsföljdslänkkod i olika operationer i en operationsföljd, eftersom en komponent då av misstag kan länkas till två olika operationer, så att den förbrukas två gånger.  
    >   
    >  Du bör ge operationsföljdslänkkoden samma namn som operationen, så att alla operationsföljdslänkar blir operationsspecifika.

5.  Ställ in statusen för operationsföljden till **Godkänd**.  

    Operationsföljdslänkkoder tilldelas nu till operationer. Nu måste du skapa den faktiska länken genom att tilldela samma koder till specifika komponenter i den aktuella produktionsstrukturen.  

6.  Öppna den **produktionsstruktur** som innehåller komponenterna som du vill länka till operationerna ovan. För mer information, se [Så här skapar du produktionsstrukturer](production-how-to-create-production-boms.md).
7.  Se till att strukturen har statusen **Under utveckling**.  
8.  På den aktuella prod.strukturraden, i fältet **Operationsföljdslänkkod**, markera koden som du precis har tilldelat den aktuella operationen.  
9. Fortsätt genom att lägga till operationsföljdslänkkoder till andra komponenter utifrån de unika operationer där de används.  
10. Ställ in statusen för produktionsstrukturen till **Godkänd**.  

    > [!NOTE]  
    >  Om du vill aktivera operationsföljdslänkar för en befintlig produktionsorder måste du först uppdatera den. Mer information finnsi [Så här skapar du ett produktionsorder](production-how-to-create-production-orders.md).  

De markerade komponenterna länkas till de markerade operationerna när du skapar eller uppdaterar en produktionsorder som använder den aktuella produktionsstrukturen och operationsföljden. Detta visas i fönstret **Prod. Ordern komponenter** under produktionsordern, och där kan du också ta bort och lägga till de definierade operationsföljdslänkkoderna när som helst.

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a>Tilldela personal, verktyg och kvalitetsmått för operationsföljdsuppgifter.
Om du behöver personal med kvalifikationer, specialkunskaper eller särskild behörighet för en operation kan du tilldela sådan personal till operationen. Dessutom kan du tilldela åtgärden med verktyg och kvalitet. Nedan beskrivs hur du tilldelar personal: Momentet är liknande för andra typer av åtgärdsinformation.

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Operationsföljder** och välj sedan relaterad länk.  
2.  Öppna relevant operationsföljd.  
3.  På snabbfliken **rader** markerar du raden som du vill behandla och klickar på åtgärden **personal**.  
4.  Fyll i fälten i fönstret **Operationsföljd personal**.  
5.  Välj **OK** för att stänga fönstret. Angivna värden kopieras och tilldelas till operationen.    

## <a name="to-create-a-new-versions-of-a-routing"></a>Så här skapar du nya versioner av operationsföljder  
Med versionsprincipen kan du hantera flera versioner av en operationsföljd. Strukturen på operationsföljdsversionen motsvarar strukturen på operationsföljden som består av huvud och rader. Den grundläggande skillnaden definieras av startdatumet.  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Operationsföljder** och välj sedan relaterad länk.  
2.  Markera operationsföljden som ska kopieras och klicka på åtgärden **versioner**.  
3. I fönstret **operationsföljdversioner** väljer du åtgärden **Ny**.
4. Fyll i fälten om det behövs.
5.  I fältet **Versionskod** anger du en identifiering som är unik för versionen. Du kan använda valfria siffror och bokstäver.  

    Den nyskapade versionen tilldelas automatiskt statusen **Ny**.  
6.  Om du vill skapa rader för åtgärden, markera den första tomma raden och fyll i **Åtgärdsnr.** enligt operationssekvensen.

    Raderna i operationen sorteras i stigande ordning efter operationsnummer. Du rekommenderas välja tillräcklig bredd för det här steget för att kunna göra ändringar senare. **Nästa operationsnr.** Fältet refererar till följande operation. Operationsnumret kan anges direkt.

7. När operationsföljdversionen har slutförts kan du ange **Status** till **godkänd**.

Versionens giltighetstid anges i fältet **Startdatum**.  

## <a name="see-also"></a>Se även  
[Så här skapar du nya produktionsstrukturer](production-how-to-create-production-boms.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planerad](production-planning.md)   
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

