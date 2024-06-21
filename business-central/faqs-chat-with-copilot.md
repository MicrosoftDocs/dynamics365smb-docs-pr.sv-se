---
title: Vanliga frågor och svar om Ansvarsfull AI för Chatt med Copilot (förhandsversion)
description: 'Dessa vanliga frågor och svar innehåller information om AI-tekniken som används för Chatt med Copilot i Business Central. Den innehåller också viktiga saker att tänka på och information om hur AI används, hur den har testats och utvärderats samt eventuella specifika begränsningar.'
ms.date: 03/18/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI, chat'
---
# Vanliga frågor och svar om Ansvarsfull AI för Chatt med Copilot (förhandsversion)

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Dessa vanliga frågor beskriver AI-effekten av Chatt med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du har allmänna frågor om hur du använder funktionen går du till [Vanliga frågor och svar för chatta med Copilot](chat-with-copilot-faq.md).

## Vad är Chatt med Copilot?

Microsoft Copilot är den AI-drivna assistenten som hjälper till att gnista kreativitet, öka produktiviteten och eliminera tråkiga uppgifter. Du kan chatta med Copilot i Business Central för att svara på frågor och hitta affärsdata genom att uttrycka vad du letar efter på naturligt språk.

Chatt med Copilot, även kallad chatt, är en interaktiv funktion som svarar på frågor och hittar affärsdata relaterade till [!INCLUDE[prod_short](includes/prod_short.md)], utan att användarna behöver navigera i användargränssnittet eller produktdokumentationen. Fönstret Copilot är tillgängligt var som helst i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.

Användare ställer frågor på naturligt språk, som "Hur levererar jag varor till mina kunder direkt från mina leverantörer?" eller "Har vi några kontorsstolar i lager för under 600 USD?" Som svar ger Copilot svar på naturligt språk. Beroende på frågorna kan svaren innehålla oformaterad text, länkar till poster eller sidor i [!INCLUDE[prod_short](includes/prod_short.md)] och länkar till [!INCLUDE[prod_short](includes/prod_short.md)] hjälpartiklar om Microsoft Learn.

## Vilka funktioner finns i Chatt med Copilot?

Du kan chatta med Copilot för att få svar på följande typer av frågor:

### Förklara och vägleda

Användare kan be Copilot att förklara ett specifikt koncept som är relaterat till [!INCLUDE[prod_short](includes/prod_short.md)], till exempel vad som är dimensioner, eller ge vägledning om hur man slutför en uppgift, till exempel hur man bokför en försäljningsorder. Copilot söker i den officiella [!INCLUDE[prod_short](includes/prod_short.md)] dokumentationen som publicerats av Microsoft och ger ett svar baserat på dokumentationen.

- Copilot använder kunskapen på Microsoft Learn (inte en bred webbsökning) för att semantiskt söka endast Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]-dokumentation i Microsoft Learn.

- Copilot vidtar inga åtgärder, skapar inte nya data eller ändrar någon konfiguration. Det sammanfattar helt enkelt alla stycken som den hittar på Microsoft Learn som matchar frågan eller prompten i chatten.

### Hitta affärsdata och relaterade sidor

Användare kan be Copilot att hitta sidor efter namn eller be om poster baserat på deras fält och begränsningar. Om Copilot hittar en matchning svarar den med en länk till relevant post eller sida, som användaren sedan kan välja att öppna.

- Copilot konverterar indata för naturligt språk till en fråga som består av ett tabellsöknings-, sorterings- och filtervillkor.

  Funktionen använder inbyggda datasökningsfunktioner i [!INCLUDE[prod_short](includes/prod_short.md)] för att hitta matchande data från tabeller i företagsdatabasen. Sökningen körs under användarens egen identitet för säkerhet och efterlevnad. Den söker inte utanför [!INCLUDE[prod_short](includes/prod_short.md)] databasen.

- Copilot vidtar inga åtgärder, skapar inte nya data eller ändrar någon konfiguration. Den sammanfattar bara de poster som tagits emot från den inbyggda datasökningen i [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Vad är den avsedda användningen av chatta med Copilot?

Chatt är utformat för företagsanvändning och för att svara på frågor relaterade till [!INCLUDE[prod_short](includes/prod_short.md)] och de affärsdata som den innehåller. Funktionen ger människor möjlighet att lösa vanliga uppgifter som att hitta poster eller få vägledning genom att uttrycka sig med sina egna ord, vilket gör det enklare och mer tillgängligt att arbeta med [!INCLUDE[prod_short](includes/prod_short.md)].

## Hur utvärderades Chatt med Copilot? Vilka mått används för att mäta prestanda?

- Funktionen genomgick omfattande tester under vilka många engelskspråkiga texter som täcker många olika ämnen och sätt att uttrycka avsikter gavs till Copilot. Resultaten utvärderades mot noggrannhet, relevans och säkerhet.
- Funktionen är byggd i enlighet med Microsofts standard för ansvarsfull AI. [Läs mer om ansvarsfull AI från Microsoft](https://aka.ms/RAI).

## Hur övervakar Microsoft kvaliteten på genererat innehåll?

Microsoft har olika system inrättade för att säkerställa att innehåll som genereras av Copilot är av högsta kvalitet, upptäcka missbruk och säkerställa säkerheten för våra kunder och deras data.

Användare har möjlighet att ge feedback på varje Copilot-svar och rapportera felaktigt eller olämpligt innehåll för att hjälpa Microsoft att förbättra den här funktionen. 

- Du ger feedback genom att använda ikonen gilla (tummen upp) eller ogilla (tummen ned) på rutan **Copilot** i [!INCLUDE[prod_short](includes/prod_short.md)].
- Vi analyserar och använder användarfeedback om funktionen för att hjälpa oss att förbättra svaren.
- Om du stöter på olämpligt genererat innehåll rapporterar du det till Microsoft med hjälp av det här feedbackformuläret: [Rapportera missbruk](https://go.microsoft.com/fwlink/?linkid=2249810).
- Microsoft kan inaktivera Copilot-drivna funktioner för utvalda kunder om missbruk av funktionen upptäcks.

## Vilka är begränsningarna för Chatt med Copilot? Hur kan användare minimera effekten av begränsningar av Chatt med Copilot när de använder systemet?

- Allmänna AI-begränsningar

  AI-system är värdefulla verktyg, men de är icke-deterministiska. Innehållet de genererar kanske inte är helt korrekta. Därför är det viktigt att använda ditt omdöme för att granska och verifiera svaren i Copilot innan du fattar beslut som kan påverka intressenter som kunder och partner. För de flesta svar kommer Copilot också att inkludera citat eller referenslänkar som du kan använda för att snabbt verifiera om Copilot har kommit till rätt svar. När du till exempel tillfrågas om hur en uppgift ska utföras innehåller Copilot länkar till källartikeln. När Copilot tillfrågas om att hitta en post baserat på specifika kriterier innehåller den länkar som beskriver listsidan som identifierats som samtalsämne, samt eventuella filter eller sorteringar som användes för att nå ett svar.

- Språkbegränsningar

  - Charr stöds endast på engelska för följande språk: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA.

    Om visningsspråket i [!INCLUDE[prod_short](includes/prod_short.md)] inte är något av dessa språk är chatten inte tillgänglig.

  - Kvaliteten på svaren kan vara lägre under följande förhållanden:
    - Språkspråket är något annat än en-US.
    - När språkinställningen för användaren i [!INCLUDE[prod_short](includes/prod_short.md)] skiljer sig från det primära språket för data i [!INCLUDE[prod_short](includes/prod_short.md)] databasen.

- Specifika bransch-, produkt- och ämnesbegränsningar

   Chatten innehåller inbyggda säkerhetsmekanismer som förhindrar oönskad generering av skadligt innehåll, till exempel sexuellt innehåll eller uppmaning till våld. Ibland arbetar kunder inom där de säljer produkter och tjänster, arbetar med processer som naturligt överlappar vad som kan anses olämpligt i andra sammanhang, eller arbetar med data som kan utlösa dessa skyddsåtgärder. Chatt kanske inte fungerar lika bra i dessa fall.

<!--## What operational factors and settings allow for effective and responsible use of the feature?-->

## Vilka data samlar Chatt med Copilot in och hur används den

Microsoft använder inte dina företagsdata, inklusive den text du skickar till Copilot, för att träna de grundläggande AI-modellerna till förmån för andra. Företagsadministratörer har fullständig kontroll över att styra dessa data som ingår i deras Azure-prenumeration. Eftersom administratörer eller andra i företaget kan ha åtkomst till dessa data enligt din arbetsgivares bedömning rekommenderar vi att användarna inte anger känsliga data som lösenord eller andra hemligheter.

## Vad erbjuder Chatt med Copilot för säkerhet

Chatt är utformat för att vara säkert och körs under användarens identitet, ärver alla säkerhetsbehörigheter och andra begränsningar och fungerar aldrig utanför [!INCLUDE[prod_short](includes/prod_short.md)] plattformens säkerhet. Det innebär att Copilot endast kan komma åt data som användaren har tillgång till.

För användare med SUPER-behörighet kan chatten lättare hitta osäkra data som vanligtvis är svårare att komma åt för andra användare. Organisationer som inte tillämpar [!INCLUDE[prod_short](includes/prod_short.md)] säkerhetsmodellen för att begränsa vilka tabeller och objekt varje användare eller användarroll har åtkomst till kan utsättas för högre risker när de använder chatt. Därför rekommenderar vi att din organisation antingen implementerar [!INCLUDE[prod_short](includes/prod_short.md)] säkerhetsmodellen eller inaktiverar chatten.

## Se även

[Chatt med Copilot (förhandsversion)](chat-with-copilot.md)

