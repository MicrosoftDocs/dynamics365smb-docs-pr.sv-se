---
title: Vanliga frågor om bankkontoavstämningshjälp med Copilot (förhandsversion)
description: 'Dessa vanliga frågor och svar innehåller information om AI-tekniken som används för att stämma av bankkonton och kontoutdrag Business Central. Den innehåller också viktiga saker att tänka på och information om hur AI används, hur den har testats och utvärderats samt eventuella specifika begränsningar.'
ms.date: 03/27/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# Vanliga frågor om bankkontoavstämningshjälp med Copilot (förhandsversion)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Dessa vanliga frågor beskriver AI-effekten av Microsoft Copilot-hjälp med bankkontoavstämning i [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Vad är bankavstämningshjälp?

Bankavstämning är en vanlig redovisningsuppgift där organisationer granskar sina bankkontoutdrag för att identifiera transaktioner som ska registreras i [!INCLUDE[prod_short](includes/prod_short.md)]. Den här uppgiften skulle till exempel användas för att identifiera periodiska bankavgifter eller små personalkostnader.

Bankavstämning är vanligtvis en process i flera steg. Först importeras kontoutdrag till [!INCLUDE[prod_short](includes/prod_short.md)]. Därefter matchas transaktioner med reskontraposter. Slutligen bokförs nya transaktioner för att återspegla eventuella återstående transaktioner som du inte tidigare kände till.

Copilot i [!INCLUDE[prod_short](includes/prod_short.md)] minskar det manuella arbetet genom att matcha fler transaktioner och föreslå redovisningskonton som du kan bokföra på.

## Vilka är funktionerna för bankavstämningshjälp?

Copilot tillhandahåller AI-driven hjälp med två olika uppgifter:

- Förbättrad matchning av transaktioner med poster i huvudboken

    [!INCLUDE[prod_short](includes/prod_short.md)] erbjuder automatiska regler som automatiskt matchar många banktransaktioner med transaktioner. Dessa regler är dock oflexibla och resulterar ofta i många omatchade transaktioner som var och en kräver manuell inspektion och jämförelse. Copilot använder AI-teknik för att inspektera omatchade transaktioner och identifiera fler matchningar, baserat på datum, belopp och beskrivningar. Om kunden till exempel betalar flera fakturor som ett engångsbelopp, stämmer Copilot av den enskilda kontoutdragsraden med de flera fakturatransaktionerna.

- Föreslagna redovisningskonton

    För kvarvarande banktransaktioner som inte kan matchas med några transaktioner jämför Copilot använder AI-teknik för att jämföra transaktionsbeskrivningen med redovisningskontonamn och föreslår det mest sannolika redovisningskontot att bokföra på. Om till exempel omatchade transaktioner har berättelsen*Bränslestopp 24* kan Copilot föreslå att du bokför dem på kontot *Transport*.

Copilot ansluter inte till din bank för att hämta eller skicka transaktioner. Denna uppgift förblir helt inom din kontroll. Det är en förutsättning för att börja använda Copilot-hjälpen, oavsett om dessa transaktioner läggs till i [!INCLUDE[prod_short](includes/prod_short.md)] med en digital bankanslutning, importeras från en kontoutdragsfil eller anges manuellt.

## Vad är den avsedda användningen av bankavstämningshjälp?

Avstämningshjälpen för bankkonton är utformad för att förbättra hjälpa till att noggrannheten i redovisningen genom att hjälpa kunderna identifiera nya transaktioner som de ska redovisa i [!INCLUDE[prod_short](includes/prod_short.md)]. Det är inte avsett för att upptäcka bedrägerier eller för att identifiera om kunder betalade i tid.

## Hur utvärderades bankavstämningshjälpen? Vilka mått används för att mäta prestanda?

Bankkontoavstämning har testats med hjälp av kombinationer av syntetiska banktransaktionsdata och liknande redovisningskonton och redovisningstransaktioner som omfattar de typiska variationerna och datagränserna för varje fält och på olika språk. Testdata representerar både typisk användning och användning av dåliga aktörer. Prestanda mättes i jämförelse med manuell avstämning av samma data.

## Vilka är begränsningarna för bankavstämningshjälp? Hur kan användare minimera påverkan av dessa begränsningar när de använder systemet?

Bankkontoavstämningshjälpen fungerar bäst när redovisningskontonamn, transaktionsbeskrivningar och banktransaktionsbeskrivningar är på samma språk. Blandade språk eller blandat språk för transaktionsbeskrivningar resulterar ofta i färre matchningar och förslag.

Föreslagna redovisningskonton fungerar bäst på något av de språk som stöds (se nästa avsnitt för en lista över språk). Användare kan uppleva färre transaktionsmatchningar och färre föreslagna redovisningskonton på andra språk.

## I vilka geografiska områden och på vilka språk finns bankavstämningshjälp tillgängligt? 

- Tillgängliga geografiska områden

  Bankkontoavstämning är tillgängligt i alla geografiska [Business Central länder/regioner som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). För kundmiljöer i länder/regioner där Azure OpenAI Service inte distribueras måste administratörer godkänna att data flyttas över gränserna för [!INCLUDE [prod_short](includes/prod_short.md)] för att ansluta till Azure OpenAI Service. Läs mer om [Copilot dataförflyttning mellan geografiska områden](ai-copilot-data-movement.md).

- Tillgängliga språk

  [!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

För mer information om språk, se föregående fråga om begränsningar.

## Vad förväntas av systemanvändare när de använder bankkontoavstämningshjälp?

### Under en bankkontoavstämning

AI-drivna matchningar och förslag kan ibland vara felaktiga eller ofullständiga. Användare av bankkontoavstämningshjälp måste granska riktigheten i matchningar och förslag från Copilot innan de väljer att behålla dem. Copilot-matchningar och förslag sparas inte i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen förrän du väljer knappen **Behåll den** och stänger Copilot-fönstret. Du kan redigera och korrigera eventuella matchningar eller förslag innan du väljer att behålla dem.

### När du slutför bankkontoavstämning

Vi rekommenderar att användarna också kontrollerar riktigheten och korrigerar eventuella avvikelser när de lämnar Copilot-fönstret. Denna process bör omfatta följande aktiviteter:

- Granska avstämningstestrapporten.
- Se till att din organisation har lämpliga processer för granskning och revision på plats.
- Öppna bokförda avstämningar igen med hjälp av funktionen **Ångra**.
- Korrigera eventuella felaktiga transaktioner genom omvänd bokföring av transaktioner.

## Vad förväntas av administratörer och systemanvändare när de använder bankkontoavstämningshjälp?

Systemanvändare, till exempel revisorer, kassörer eller andra som arbetar med affärsredovisning, bör alltid granska riktigheten i matchningar och förslag från Copilot innan de väljer att behålla dem. När användarna har stämt av med Copilot rekommenderar vi att de granskar avstämningstestrapporten för att verifiera noggrannheten och identifiera eventuella avvikelser.

Administratörer bör se till att lämpliga redovisningsanvändare har beviljats åtkomst till den här funktionen.

## Är Copilot det enda sättet att slutföra bankkontoavstämning?

Nr. Användning av Copilot är valfri. [!INCLUDE[prod_short](includes/prod_short.md)] erbjuder traditionella, icke-AI-drivna sätt att importera kontoutdrag, köra fördefinierade matchningsregler och manuellt tillämpa matchningar och bokföra på lämpliga redovisningskonton. Både det traditionella tillvägagångssättet och Copilot kan användas samtidigt inom en organisation.

## Hur ger jag feedback om AI-genererat innehåll?

Varje gång Copilot ger matchningar eller förslag kan du ge feedback till Microsoft direkt från Copilot-fönstret med hjälp av kontrollerna gilla (tummen upp) och ogilla (tummen ned). Din feedback förblir anonym och vi använder dessa uppgifter för att förbättra kvaliteten på tjänsten.

## Se även

[Stämma av bankkonton med Copilot (förhandsversion)](bank-reconciliation-with-copilot.md)
