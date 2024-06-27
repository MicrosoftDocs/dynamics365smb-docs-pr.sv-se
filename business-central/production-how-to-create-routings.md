---
title: Skapa operationsföljder
description: 'I den här artikeln får du en översikt över olika sätt att skapa operationsföljder, inklusive nödvändiga krav och hur du skapar routningslänkar.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '99000764, 99000765, 99000766, 99000767, 99000794, 99000796, 99000798, 99000806, 99000808, 99000810, 99000817, 99000834, 99000835, 99000836, 99000837, 99000840, 99000841, 99000844, 99000845'
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# Skapa operationsföljder

Tillverkningsföretag använder verksamhetsföljder för att visa produktionsprocessen.

Operationsföljden utgör också grunden för processplanering, kapacitetsplanering, planerad fördelning av materialbehov och produktionsdokument.  

För produktionsstrukturer kopplas verksamhetsföljderna till produktionens slutartikel. En verksamhetsföljd innehåller standarddata som samlar processkraven för en viss producerad artikel. När en produktionsorder har skapats för den överordnade artikeln, avgör dess produktionsstruktur beräkningen av materialbehoven enligt vad som visas på sidan **Prod.orderverksamhetsföljd**.  

Innan du kan skapa en verksamhetsföljd måste följande installationer vara på plats:  

- Artikelkort kan skapas för överordnade artiklar som ingår i produktionen. Lär dig mer i [Registrera nya artiklar](inventory-how-register-new-items.md).
- Produktionsresurser har ställts in. Mer information finns i [Skapa produktionsgrupper och maskingrupper](production-how-to-set-up-work-and-machine-centers.md).

## Så här skapar du en verksamhetsföljd

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Operationsföljder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I fältet **Typ**, välj ett av följande alternativ:
   - **Seriell** för att beräkna produktionsverksamhetsföljden efter det värde som anges i fältet **Operationsnr.** .  
   - Välj **Parallell** för att beräkna operationerna enligt värdet i fältet **Nästa verksamhetsnr**. .  
5. Ställ in värdet i fältet **Status** till **Ny** eller **Under utveckling** om du vill redigera operationsföljden.  

    Så här fyller du i verksamhetsföljdrader
6. I fältet **Operationsnr.** anger du numret för den första operationen, till exempel **10**.  
7. I fältet **Typ** anger du vilken typ av resurs som används (till exempel **Produktionsgrupp**).  
8. I fältet **Nr.** markerar du den resurs som ska användas (eller skriv in namnet direkt i fältet).  
9. I fältet **Operationsföljdslänkkod** anger du en kod för att ansluta komponenten till en särskild operation. För mer information, se [Så här skapar du operationsföljdslänk](production-how-to-create-routings.md#to-create-routing-links).
10. I fälten **Bearbetningstid** och **Omställningstid** anger du processtiderna som krävs för att genomföra operationen.

     > [!NOTE]
     > Omställningstiden beräknas per produktionsorder, och bearbetningstiden beräknas per producerad artikel.  

11. I fältet **Samtidiga kapaciteter**, ange hur många enheter av den markerade resursen som används för att utföra operationen. Till exempel halveras körtiden om två personer tilldelas till en förpackningsoperation.  
12. Fortsätt att fylla i rader för alla operationer som krävs för att producera den aktuella artikeln.  
13. Om du vill kopiera rader från en befintlig verksamhetsföljd klickar du på åtgärden **Kopiera verksamhetsföljd** och väljer de befintliga raderna.  
14. För att aktivera operationsföljd, i fältet **Status**, välj **Certifierad**.  
15. Nu kan du koppla den nya verksamhetsföljden till kortet för den aktuella produktionsartikeln genom att fylla i **verksamhetsföljdnr.**. Lär dig mer i [Registrera nya artiklar](inventory-how-register-new-items.md).  

> [!NOTE]  
> Glöm inte att beräkna om standardkostnaden för artikeln från **artikelkortet**. Välj åtgärden **Produktion** åtgärden **Beräkna standardkostnad** och välj sedan åtgärden **Alla nivåer**.  

## Så här skapar du en verksamhetsföljdslänk

Du kan skapa verksamhetsföljdslänkar för att koppla ihop komponenter med specifika operationer för att behålla deras förhållande även om produktionsstrukturen eller verksamhetsföljden ändras. Operationsföljdslänkar gör det också lättare att bokföra komponenter vid rätt tidpunkt, dvs. när den angivna kopplade operationen startar – inte när hela ordern släpps. Läs mer i [Bokföra komponenter utifrån operationens utflöde](production-how-to-flush-components-according-to-operation-output.md).  

En annan viktig fördel är att länkade komponenter och operationer visas i en logisk processtruktur när du använder sidan **Produktionsjournal** för bokföring av utdata och förbrukning.  

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Operationsföljder** och väljer sedan relaterad länk.  
2. Öppna verksamhetsföljden som innehåller operationen du vill länka.  

    Se till att verksamhetsföljden har statusen är **Under utveckling**.  

3. På den aktuella verksamhetsföljdsraden, i fältet **Operationsföljdslänkkod**, markera en kod.  
4. Lägg till olika verksamhetsföljdslänkkoder i andra operationer i verksamhetsföljden, om det behövs.  

    > [!NOTE]  
    > Du bör inte använda samma verksamhetsföljdslänkkod i olika operationer i en verksamhetsföljd, eftersom en komponent då av misstag kan länkas till två olika operationer, så att den förbrukas två gånger.  
    >
    > Du bör ge verksamhetsföljdslänkkoden samma namn som operationen, så att alla verksamhetsföljdslänkar blir verksamhetsspecifika.

5. Ställ in statusen för operationsföljden till **Godkänd**.  

    Operationsföljdslänkkoder tilldelas nu till operationer. Nu måste du skapa den faktiska länken genom att tilldela samma koder till specifika komponenter i den aktuella produktionsstrukturen.  

6. Öppna den **produktionsstruktur** som innehåller komponenterna som du vill länka till operationerna ovan. Läs mer på [Skapa produktionsstrukturer](production-how-to-create-production-boms.md).
7. Se till att strukturen har statusen **Under utveckling**.  
8. På den aktuella prod.strukturraden, i fältet **Operationsföljdslänkkod**, markera koden som du precis har tilldelat operationen.  
9. Fortsätt genom att lägga till verksamhetsföljdslänkkoder till andra komponenter utifrån de unika operationer där de används.  
10. Ställ in statusen för produktionsstrukturen till **Godkänd**.  

    > [!NOTE]  
    > Om du vill aktivera verksamhetsföljdslänkar för en befintlig produktionsorder måste du först uppdatera den. Läs mer på [Skapa produktionsorder](production-how-to-create-production-orders.md).  

De markerade komponenterna länkas till de markerade operationerna när du skapar eller uppdaterar en produktionsorder som använder produktionsstrukturen och verksamhetsföljden. Den här länken visas på sidan **Prod.order – komponenter** under produktionsordern. Du kan när som helst ta bort och lägga till länkkoderna för operationsföljd.

## Tilldela personal, verktyg och kvalitetsmått för verksamhetsföljdsuppgifter

Om du behöver personal med kvalifikationer, specialkunskaper eller särskild behörighet för en operation kan du tilldela sådan personal till operationen. Dessutom kan du tilldela åtgärden med verktyg och kvalitet. Nedan beskrivs hur du tilldelar personal: Momentet är liknande för andra typer av åtgärdsinformation.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Operationsföljder** och väljer sedan relaterad länk.  
2. Öppna relevant verksamhetsföljd.  
3. På snabbfliken **rader** markerar du raden som du vill behandla och klickar på åtgärden **verksamhet** och välj sedan åtgärden **Personal**.  
4. Fyll i fälten på sidan **Operationsföljd personal**.  
5. Välj **OK** för att stänga sidan. Angivna värden kopieras och tilldelas till operationen.  

## Så här skapar du nya versioner av verksamhetsföljder

Med versionsprincipen kan du hantera flera versioner av en operationsföljd. Strukturen på operationsföljdsversionen motsvarar strukturen på operationsföljden som består av huvud och rader. Startdatumet definierar den grundläggande skillnaden.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Operationsföljder** och väljer sedan relaterad länk.  
2. Markera verksamhetsföljden som ska kopieras och klicka på åtgärden **versioner**.  
3. På sidan **verksamhetsföljdversioner** väljer du åtgärden **Ny**.
4. I fältet **Versionskod** anger du en identifiering som är unik för versionen. Du kan använda en valfri kombination av siffror och bokstäver.  

    Den nyskapade versionen tilldelas automatiskt statusen **Ny**.  
5. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
6. Om du vill skapa rader för åtgärden, markera den första tomma raden och fyll i **Åtgärdsnr.** enligt verksamhetssekvensen.

    Raderna i operationen finns i stigande ordning efter operationsnummer. Du rekommenderas välja tillräcklig bredd för det här steget för att kunna göra ändringar senare. **Nästa verksamhetsnr.** fältet hänvisar till nästa operation i operationsföljden.

7. När verksamhetsföljdversionen har slutförts kan du välja **Status** till **Certifierad**.

## Se även

[Skapa produktionsstrukturlistor](production-how-to-create-production-boms.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Planerad](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]