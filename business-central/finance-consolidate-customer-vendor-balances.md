---
title: Konsolidera saldon för ett företag som är en kund och en leverantör
description: Beskriver hur du konsoliderar saldon för en kund som även är leverantör.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '5052, 21, 5050'
ms.date: 10/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Konsolidera saldon för ett företag som är en kund och en leverantör
Ett företag som du gör affärer med kan vara både kund och leverantör. I så fall kan du undvika att göra onödiga betalningar eller inleveranser – och eventuellt spara in på transaktions avgifter – genom att konsolidera företagets kund-och leverantörssaldon. Konsolideringen jämför företagets saldon som leverantör och som kund, och genererar sedan nettobeloppet så att antingen kundens eller leverantörens saldo blir kvar, beroende på vilket belopp som har blivit högre. 

Om du vill konsolidera saldona måste du först länka kund-och leverantörs företagen med hjälp av en kontakt som har typen **Företag**. En kund eller leverantör kan bara ha en kontakt av typen **Företag**. Mer information finns i [Skapa kontakter](marketing-create-contact-companies.md).

När du har länkat företagen erbjuder sidan **Kundkort** fältet **Saldo som leverantör**, och sidan **Leverantörskort** innehåller fältet **Saldo som kund**.

Även om detta inte är ett krav är kund-och leverantörsföretagen vanligen samma juridiska person. 

## Innan du börjar
Innan du konsoliderar saldon anger du några inställningar på sidan **Marknadsföringsinställningar**. 

* På snabbfliken **Interaktioner** måste du ange affärsrelationskoder i fälten **Kunder** och **Leverantörer**. [!INCLUDE[prod_short](includes/prod_short.md)] använder den här informationen för att bestämma vilken typ av relation som ska visas för kontakter. 
* Valfritt: På snabbfliken **Dubbletter** kan du aktivera eller inaktivera dubblettsökning. Som standard är sökning för dubbletter aktiverad. Mer information finns i [Hantera dubbletter](#handling-duplicates). 

## Länka en befintlig kund och ett leverantörsföretag genom en kontakt
Följande steg beskriver hur du länkar en kund och en leverantör via en kontakt.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** eller **Leverantör** och väljer sedan relaterad länk.
2. Välj kunden eller leverantören och välj sedan åtgärden **Kontakt**.   
3. Välj kontakt och välj sedan åtgärden **Länka med befintlig**.
4. Välj vilken typ av enhet du vill skapa en affärsrelation med.
5. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## Skapa en leverantör från en kund eller omvänt
Du kan skapa en ny leverantör från en befintlig kund, eller en ny kund från en leverantör. Från sidan **Kund** eller **Leverantör** öppnar du sidan **Kontakt**. Välj åtgärden **Skapa som** och därefter antingen alternativet **Kund** eller **Leverantör**. 

## Skapa en ny kund eller leverantör och koppla denne via en leverantörs- eller kundkontakt
1. Skapa ett nytt kundkort eller en ny leverantör. Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md) eller [Registrera nya kunder](sales-how-register-new-customers.md).
2. När du har ställt in kunden eller leverantören väljer du åtgärden **Skapa** och väljer sedan antingen **Kund** eller **Leverantör**. 

## För att konsolidera saldon för kund och leverantör för ett kontaktföretag
På sidan **Utbetalningsjournal** använder du åtgärden **Nettosaldon för kund/leverantör** för att konsolidera kund- och leverantörssalson till ett enda nettobelopp. Åtgärden skapar - men bokför inte - utbetalningsjournalrader som innehåller nettosaldon.

> [!NOTE]
> Om kund- eller leverantörssaldot innehåller belopp i olika valutor skapas en rad för beloppet i respektive valuta.

## Hantera dubbletter
Om du aktiverar dubblettsökning på snabbfliken **Dubbletter** på sidan **Marknadsföringsinställningar** visas en varning när du ändrar värdena i fält som ingår i inställningen för kopiering av söksträngar. När en dubblett hittas kan du utföra följande åtgärder:

* Kombinera de dubblerade kontakterna till en enda kontakt som är samma för både kunden och leverantören med hjälp av funktionen **Slå ihop med** på sidan **Kontaktkort**. Att slå samman kontakter utförs vanligtvis när kunden och leverantören är samma juridiska person. Mer information finns i [Koplla dubblettposter](sales-how-merge-duplicate-records.md). 
* Ta bort leverantörens affärsrelation för kontakt med leverantör eller kund, och använd sedan åtgärden **Länka till befintlig** för att länka till en annan kontakt.    

## Se även
[Försäljning](sales-manage-sales.md)  
[Registrera nya kunder](sales-how-register-new-customers.md)  
