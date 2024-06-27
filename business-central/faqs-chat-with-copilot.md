---
title: Vanliga frågor och svar om Ansvarsfull AI för Chatt med Copilot (förhandsversion)
description: 'Dessa vanliga frågor och svar innehåller information om AI-tekniken som används för Chatt med Copilot i Business Central. Den innehåller också viktiga saker att tänka på och information om hur AI används, hur den har testats och utvärderats samt eventuella specifika begränsningar.'
ms.date: 06/13/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI, chat'
---
# <a name="responsible-ai-faq-for-chat-with-copilot-preview"></a>Vanliga frågor och svar om Ansvarsfull AI för Chatt med Copilot (förhandsversion)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

Dessa vanliga frågor beskriver AI-effekten av Chatt med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du har allmänna frågor om hur du använder funktionen går du till [Vanliga frågor och svar för chatta med Copilot](chat-with-copilot-faq.md).

## <a name="what-is-chat-with-copilot"></a>Vad är Chatt med Copilot?

Microsoft Copilot är en AI-driven assistent som hjälper dig att vara mer kreativ, produktiv och effektiv. Du kan chatta med Copilot i Business Central för att få svar och insikter om [!INCLUDE[prod_short](includes/prod_short.md)] och dina affärsdata genom att skriva det du vill veta på naturligt språk.

Chatt med Copilot, även kallad chatt, är en interaktiv funktion som svarar på dina frågor utan att du behöver navigera i användargränssnittet eller produktdokumentationen. Fönstret Copilot är tillgängligt var som helst i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.

Du kan ställa frågor på naturligt språk, som "Hur levererar jag varor till mina kunder direkt från mina leverantörer?" eller "Har vi några kontorsstolar i lager för under 600 USD?" Som svar ger Copilot svar på naturligt språk. Beroende på frågorna kan svaren innehålla oformaterad text, länkar till poster eller sidor i [!INCLUDE[prod_short](includes/prod_short.md)] och länkar till [!INCLUDE[prod_short](includes/prod_short.md)] hjälpartiklar om Microsoft Learn.

## <a name="what-are-capabilities-of-chat-with-copilot"></a>Vilka funktioner finns i Chatt med Copilot?

Du kan chatta med Copilot för att få svar på följande typer av frågor:

### <a name="explain-and-guide"></a>Förklara och vägleda

Du kan be Copilot att förklara ett specifikt koncept som är relaterat till [!INCLUDE[prod_short](includes/prod_short.md)], till exempel vad som är dimensioner, eller ge vägledning om hur man slutför en uppgift, till exempel hur man bokför en försäljningsorder. Copilot söker i den officiella [!INCLUDE[prod_short](includes/prod_short.md)] dokumentationen som publicerats av Microsoft och ger ett svar baserat på dokumentationen.

- Copilot använder kunskapen på Microsoft Learn (inte en bred webbsökning) för att semantiskt söka endast Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]-dokumentation i Microsoft Learn.

- Copilot vidtar inga åtgärder, skapar inte nya data eller ändrar någon konfiguration. Det sammanfattar helt enkelt alla stycken som den hittar på Microsoft Learn som matchar frågan eller prompten i chatten.

### <a name="find-business-data-and-related-pages"></a>Hitta affärsdata och relaterade sidor

Du kan be Copilot att hitta sidor efter namn eller be om poster baserat på deras fält och begränsningar. Om Copilot hittar en matchning svarar den med en länk till relevant post eller sida, som du sedan kan välja att öppna.

- Copilot konverterar indata för naturligt språk till en fråga som består av ett tabellsöknings-, sorterings- och filtervillkor.

  Funktionen använder inbyggda datasökningsfunktioner i [!INCLUDE[prod_short](includes/prod_short.md)] för att hitta matchande data från tabeller i företagsdatabasen. Sökningen körs under din egen identitet för säkerhet och efterlevnad. Den söker inte utanför [!INCLUDE[prod_short](includes/prod_short.md)] databasen.

- Copilot vidtar inga åtgärder, skapar inte nya data eller ändrar någon konfiguration. Den sammanfattar bara de poster som tagits emot från den inbyggda datasökningen i [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="what-is-the-intended-use-of-chat-with-copilot"></a>Vad är den avsedda användningen av chatta med Copilot?

Chatt är utformat för företagsanvändning och för att svara på frågor relaterade till [!INCLUDE[prod_short](includes/prod_short.md)] och de affärsdata som den innehåller. Funktionen hjälper dig att lösa vanliga uppgifter som att hitta poster eller få vägledning. Du kan uttrycka dig med dina egna ord, vilket gör ditt arbete enklare och mer tillgängligt när du arbetar med [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="how-was-chat-with-copilot-evaluated-what-metrics-are-used-to-measure-performance"></a>Hur utvärderades Chatt med Copilot? Vilka mått används för att mäta prestanda?

- Funktionen genomgick omfattande tester under vilka många engelskspråkiga texter som täcker många olika ämnen och sätt att uttrycka avsikter gavs till Copilot. Resultaten utvärderades mot noggrannhet, relevans och säkerhet.
  
- Funktionen är byggd i enlighet med Microsofts standard för ansvarsfull AI. [Läs mer om ansvarsfull AI från Microsoft](https://aka.ms/RAI).

## <a name="how-does-microsoft-monitor-the-quality-of-generated-content"></a>Hur övervakar Microsoft kvaliteten på genererat innehåll?

Microsoft har olika system inrättade för att säkerställa att innehåll som genereras av Copilot är av högsta kvalitet, upptäcka missbruk och säkerställa säkerheten för våra kunder och deras data.

Du kan ge feedback på varje Copilot-svar och rapportera felaktigt eller olämpligt innehåll för att hjälpa Microsoft att förbättra den här funktionen. 

- Du kan ge feedback genom att använda ikonen gilla (tummen upp) eller ogilla (tummen ned) på rutan **Copilot** i [!INCLUDE[prod_short](includes/prod_short.md)].
  
- Vi analyserar och använder feedback om funktionen för att hjälpa oss att förbättra svaren.
  
- Om du stöter på olämpligt genererat innehåll rapporterar du det till Microsoft med hjälp av det här feedbackformuläret: [Rapportera missbruk](https://go.microsoft.com/fwlink/?linkid=2249810).
  
- Microsoft kan inaktivera Copilot-drivna funktioner för utvalda kunder om missbruk av funktionen upptäcks.

## <a name="what-are-the-limitations-of-chat-with-copilot-how-can-users-minimize-the-impact-of-the-chat-with-copilot-limitations-when-using-the-system"></a>Vilka är begränsningarna för Chatt med Copilot? Hur kan användare minimera effekten av begränsningar av Chatt med Copilot när de använder systemet?

- Allmänna AI-begränsningar

  AI-system är värdefulla verktyg, men de är icke-deterministiska. Innehållet de genererar kanske inte är korrekt. Därför är det viktigt att använda ditt omdöme för att granska och verifiera svaren i Copilot innan du fattar beslut som kan påverka intressenter som kunder och partner. För de flesta svar kommer Copilot också att inkludera citat eller referenslänkar som du kan använda för att snabbt verifiera om Copilot har kommit till rätt svar. När du till exempel tillfrågas om hur en uppgift ska utföras innehåller Copilot länkar till källartikeln. När Copilot tillfrågas om att hitta en post baserat på specifika kriterier innehåller den länkar som beskriver listsidan som identifierats som samtalsämne. Det ger också information om eventuella filter eller sortering som användes för att nå ett svar.

- Språkbegränsningar

  - Charr stöds endast på engelska för följande språk: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA.

    Om visningsspråket i [!INCLUDE[prod_short](includes/prod_short.md)] inte är något av dessa språk är chatten inte tillgänglig.

  - Kvaliteten på svaren kan vara lägre under följande förhållanden:
    - Språkspråket är något annat än en-US.
    - När språkinställningen för användaren i [!INCLUDE[prod_short](includes/prod_short.md)] skiljer sig från det primära språket för data i [!INCLUDE[prod_short](includes/prod_short.md)] databasen.

- Specifika bransch-, produkt- och ämnesbegränsningar

   Chatten innehåller inbyggda säkerhetsmekanismer som förhindrar oönskad generering av skadligt innehåll, till exempel sexuellt innehåll eller uppmaning till våld. Ibland arbetar kunder inom där de säljer produkter och tjänster, arbetar med processer som naturligt överlappar vad som kan anses olämpligt i andra sammanhang, eller arbetar med data som kan utlösa dessa skyddsåtgärder. Chatt kanske inte fungerar lika bra i dessa fall.

<!--## What operational factors and settings allow for effective and responsible use of the feature?-->

## <a name="what-data-does-chat-with-copilot-collect-and-how-is-it-used"></a>Vilka data samlar Chatt med Copilot in och hur används den

Microsoft använder inte dina företagsdata, inklusive den text du skickar till Copilot, för att träna de grundläggande AI-modellerna till förmån för andra. Företagsadministratörer har fullständig kontroll över att styra dessa data som ingår i deras Azure-prenumeration. Eftersom administratörer eller andra i företaget kan ha åtkomst till dessa data enligt din arbetsgivares bedömning rekommenderar vi att du inte anger känsliga data som lösenord eller andra hemligheter.

## <a name="what-does-chat-with-copilot-offer-for-security"></a>Vad erbjuder Chatt med Copilot för säkerhet

Chatt är utformat för att vara säkert och körs under användarens identitet, ärver alla säkerhetsbehörigheter och andra begränsningar och fungerar aldrig utanför [!INCLUDE[prod_short](includes/prod_short.md)] plattformens säkerhet. Det innebär att Copilot endast kan komma åt data som du har tillgång till.

För användare med SUPER-behörighet kan chatten lättare hitta osäkra data som vanligtvis är svårare att komma åt för andra användare. Organisationer som inte tillämpar [!INCLUDE[prod_short](includes/prod_short.md)] säkerhetsmodellen för att begränsa vilka tabeller och objekt varje användare eller användarroll har åtkomst till kan utsättas för högre risker när de använder chatt. Därför rekommenderar vi att din organisation antingen implementerar [!INCLUDE[prod_short](includes/prod_short.md)] säkerhetsmodellen eller inaktiverar chatten.

## <a name="see-also"></a>Se även

- [Chatt med Copilot (förhandsversion)](chat-with-copilot.md)

