---
title: Skapa produktionsstrukturer
description: 'Lära dig hur du skapar en produktionsstruktur, nya versioner av en produktionsstruktur och hur du använder beräkningsformeln för antal.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'production bom, bills of material,'
ms.search.form: '911, 912, 917, 9287, 99000786, 99000787, 99000788, 99000789, 99000795, 99000797, 99000800, 99000809, 99000811, 99000812, 99000818'
ms.date: 06/22/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Skapa produktionsstrukturer

En produktionsstruktur innehåller standarddata som beskriver de komponenter och underenheter som används vid produktion av en överordnad artikel. När en produktionsorder har skapats för den överordnade artikeln, avgör dess produktionsstruktur beräkningen av materialbehoven enligt vad som visas på sidan **Prod.order komponenter**.

[!INCLUDE[prod_short](includes/prod_short.md)] stödjer även monteringsstrukturer. Du använder monteringsorder för att slutboka artiklar från komponenter i en enkel sätt, som kan utföras av en eller flera grundläggande resurser, som inte är maskin- eller produktionsgrupper, eller utan något resurser. Det kan exempelvis vara en monteringsprocess att välja två som vinflaska och en kaffesäck och sedan packa dem som presentartiklar. Mer information finns i [Monteringsstrukturer eller produktionsstrukturer](inventory-how-work-boms.md#assembly-boms-or-production-boms).  

> [!TIP]
> I appen **Contoso Coffe Demo Data** ingår demonstrationsprodukter för olika produktionsstrukturscenarier som kan användas i en testmiljö, till exempel under en utvärdering. Lär dig hur du ställer in data för Contoso Coffee och söker efter genomgångar för olika scenarier på [Introduktion till Contoso Coffee Demo Data](contoso-coffee/contoso-coffee-intro.md).

Innan du kan skapa en verksamhetsföljd måste följande vara på plats:  

- Artikelkort kan skapas för överordnade artiklar som ingår i produktionen. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).
- Produktionsresurser har ställts in. Mer information finns i [Skapa produktionsgrupper och maskingrupper](production-how-to-set-up-work-and-machine-centers.md).

## Skapa en ny produktionsstruktur.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Produktionsstrukturer** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ställ in värdet i fältet **Status** till **Ny** eller **Under utveckling** om du vill redigera strukturen. Aktivera den genom att ställa in fältet **Status** till **Godkänd**.  

    Så här fyller du i produktionsstrukturrader
5. I fältet **Typ** anger du om artikeln på strukturraden är en vanlig artikel eller en produktionsstruktur. Om artikeln på raden är en produktionsstruktur måste den redan finnas som en godkänd produktionsstruktur.  
6. I fältet **Nr.** och markera den aktuella artikeln eller produktionsstrukturen (eller skriv in namnet direkt i fältet).  
7. I fältet **Antal per** anger du hur många enheter av artikeln som ingår i den överordnade artikeln (exempel: 4 hjul ingår i 1 bil).  
8. I fältet **Kassation %** kan du ange en fast procentandel av komponenterna som kasseras under produktionen. När komponenterna är klara att förbrukas i en släppt produktionsorder så läggs detta procenttal till i den förväntade kvantiteten i fältet **Förbrukningskvantitet** i en produktionsjournal. Mer information finns i [Registrera förbrukning och utdata](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Kassationsprocentandelen motsvarar komponenter som kasseras under produktionen (när de plockas från ett lager). Kassationsprocentandelen på verksamhetsföljdsrader motsvarar utlevererat material som kasseras (innan det placeras i ett lager).  

9. I fältet **Operationsföljdslänkkod** anger du en kod för att ansluta komponenten till en särskild operation. För mer information, se [Så här skapar du operationsföljdslänk](production-how-to-create-routings.md#to-create-routing-links).
10. Om du vill kopiera rader från en befintlig produktionsstruktur klickar du på åtgärden **Kopiera struktur** och väljer de befintliga raderna.  
11. Godkänn produktionsstrukturen.  
12. Nu kan du koppla den nya produktionsstrukturen till kortet för den aktuella överordnade artikeln. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).  

> [!NOTE]  
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)] Om du vill beräkna om standardkostnaden för artikeln från artikelkortet, välj **Produktion** och sedan åtgärden **Ber. standardkostnad**.  

## Så här skapar du nya versioner av produktionsstrukturer

Nya versioner av produktionsstrukturer används till exempel när en artikel ersätts av en annan artikel, eller när en kund begär en specialversion av en produkt. Med versionsprincipen kan olika versioner av en produktionsstruktur hanteras. Strukturen i produktionsstrukturversionen motsvarar strukturen i produktionsstrukturen. Den största skillnaden är versionernas giltighetstid. Giltigheten definieras av startdatum.  

Startdatum anger början av en versions giltighetsperiod. I alla andra fall är startdatumet ett filtreringskriterium för beräkningar och utvärderingar. Prod.strukturversionen gäller tills nästa versions giltighetsstartdatum infaller.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Produktionsstrukturer** och välj sedan relaterad länk.  
2. Markera produktionsstrukturen som ska kopieras och välj sedan åtgärden **Versioner**.  
3. Välj åtgärden **Ny**.  
4. Fyll i fälten om det behövs.
5. I fältet **Versionskod** anger du en identifiering som är unik för versionen. Du kan använda valfria siffror och bokstäver.  

    Den nyskapade versionen tilldelas automatiskt statusen **Ny**.
6. När produktionsstrukturversionen har slutförts kan du ange **Status** till **godkänd**.  

Versionens giltighetstid anges i fältet **Startdatum**.  

> [!NOTE]  
> Med alternativet **Artikel** i fältet **Typ** kan du använda en artikel från standarduppgifterna om artiklar i produktionsstrukturen. Om artikeln även har en produktionsstruktur, där fältet **Prod.struktursnr** är ifyllt på artikelkortet, beaktas också denna.  
>
> Välj alternativet **Prod.struktur** om du vill använda en fiktiv prod.struktur på raden.  
>
> Fiktiva prod.strukturer fungerar som struktureringsprodukter. Den här typen av produktionsstruktur leder aldrig till en färdig produkt, men används enbart för att bedöma den härledda efterfrågan. Fiktiva prod.strukturer har inga egna standarduppgifter om artiklar.

## Antal beräkningsformel på produktionsstrukturer

Antal beräknas med hänsyn till olika dimensioner, som också anges på produktionsstrukturraderna. Dimensionerna avser en orderenhet för respektive artikel. Längd, bredd, djup och vikt kan anges som dimensioner.  

Kolumnerna Beräkningsformel, Längd, Bredd, Djup och Vikt visas inte eftersom de endast används av vissa användare. Om du vill beräkna antal måste du först visa dessa kolumner.  

Relationen i en enskild komponent definieras av en beräkningsformel. Följande uppgifter kan ingå i beräkningsformeln:  

- **Tom** – Utan hänsyn till dimensioner. (Antal = Antal per.)  
- **Längd** – Antal = Antal per * Längd  
- **Längd x bredd** – Antal = Antal per * Längd x bredd  
- **Längd x bredd x djup** – Antal = Antal per x Längd x bredd x djup  
- **Vikt** – Antal = Antal per x vikt  
- **Fast kvantitet** kvantitet = kvantitet per

> [!NOTE]
> Med beräkningsformeln för **fast kvantitet** ser du till att förbrukningen av en komponent är densamma, oavsett kassation eller utflöde. För produktions order komponenter, när fältet **beräkningsformel** är inställt på fast antal, är fältet **Fast kvantitet** och **Förväntad kvantitet** alltid lika med **kvantiteten per** fält. Den procentuella kassation som har definierats på samma rad ignoreras. Fast kvantitet respekteras av rapporten **Artikeldisposition**. I rapporten visas artikeln som flaskhals, om disponibelt antal är mindre än antalet i fältet **Antal per överordnad**. Fälten **Kan skapa överordnad** och **Kan skapa toppartikel** är alltid tomma, oavsett tillgänglig kvantitet. Fast kvantitet ingår också i beräkningar för standardkostnader. Partistorleken för den producerade artikeln påverkar kostnaden som har allokerats för en artikel.

### Exempel

I en produktionsstruktur behövs 70 metalldelar med dimensionerna längd = 0,20 m och bredd = 0,15 m. Värdena anges så här: Beräkningsformel = längd * bredd, längd = 20, bredd = 15, antal per = 70. Antalet anges som Antal per * längd * bredd, d.v.s. Antal = 70 * 0,20 m * 0,15 m = 2,1 m2.  

## Se även

[Skapa verksamhetsföljder](production-how-to-create-routings.md)  
[Hantera produktvarianter](inventory-item-variants.md)  
[Genomgång: varianter](contoso-coffee/manufacturing/variants.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Planerad](production-planning.md)  
[Arbeta med strukturer](inventory-how-work-BOMs.md)  
[Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
