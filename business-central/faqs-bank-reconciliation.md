---
title: Vanliga frågor om bankkontoavstämningshjälp (förhandsversion) med Copilot
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

# <a name="faq-for-bank-account-reconciliation-assist-with-copilot-preview"></a>Vanliga frågor om bankkontoavstämningshjälp med Copilot (förhandsversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Dessa vanliga frågor beskriver AI-effekten av Copilot-hjälp med bankkontoavstämning i [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-bank-reconciliation-assist"></a>Vad är bankavstämningshjälp?

Bankavstämning är en vanlig redovisningsuppgift där organisationer granskar sina bankkontoutdrag för att identifiera transaktioner som ska registreras i [!INCLUDE[prod_short](includes/prod_short.md)]. Den här uppgiften skulle till exempel användas för att identifiera periodiska bankavgifter eller små personalkostnader. Den här uppgiften är vanligtvis en process i flera steg, som börjar med att importera kontoutdrag till [!INCLUDE[prod_short](includes/prod_short.md)], följt av att matcha transaktioner med transaktioner och bokföra nya transaktioner för att återspegla eventuella återstående transaktioner som inte tidigare var kända för dina reskontra. Copilot i [!INCLUDE[prod_short](includes/prod_short.md)] minskar det manuella arbetet genom att matcha fler transaktioner och föreslå redovisningskonton som du kan bokföra på. 

## <a name="what-are-capabilities-of-bank-reconciliation-assist"></a>Vilka är funktionerna för bankavstämningshjälp?

Copilot tillhandahåller AI-driven hjälp med två olika uppgifter: 

- Förbättrad matchning av transaktioner med poster i huvudboken 

   [!INCLUDE[prod_short](includes/prod_short.md)] erbjuder automatiska regler som automatiskt matchar många banktransaktioner med transaktioner. Dessa regler är dock oflexibla och resulterar ofta i många omatchade transaktioner som var och en kräver manuell inspektion och jämförelse. Copilot använder AI-teknik för att inspektera återstående transaktioner och identifiera fler matchningar, baserat på datum, belopp och beskrivningar. Om till exempel flera fakturor har betalats som ett engångsbelopp av en kund, stämmer Copilot av den enskilda kontoutdragsraden med de flera fakturatransaktionerna. 
 
- Föreslagna redovisningskonton 

   För kvarvarande banktransaktioner som inte kan matchas med några transaktioner jämför Copilot använder AI-teknik för att jämföra transaktionsbeskrivningen med redovisningskontonamn och föreslår det mest sannolika redovisningskontot att bokföra på. Copilot kan till exempel föreslå att transaktionen med berättelsen "Bränslestopp24" bokförs på kontot "Transport". 

Copilot ansluter inte till din bank för att hämta eller skicka transaktioner. Denna uppgift förblir helt inom din kontroll och är en förutsättning för att börja använda Copilot-hjälpen, oavsett om dessa transaktioner läggs till i [!INCLUDE[prod_short](includes/prod_short.md)] med en digital bankanslutning, importeras från en kontoutdragsfil eller anges manuellt. 

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Vad är den avsedda användningen av bankavstämningshjälp?

Avstämningshjälpen för bankkonton är utformad för att hjälpa till att identifiera nya transaktioner som kunderna ska redovisa i [!INCLUDE[prod_short](includes/prod_short.md)], för att förbättra noggrannheten i sina redovisningar. Den här aktiviteten är inte avsedd för att upptäcka bedrägerier eller identifiera om kunder har betalat i tid.   

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Hur utvärderades bankavstämningshjälpen? Vilka mått används för att mäta prestanda?

Den här funktionen har testats med hjälp av kombinationer av syntetiska banktransaktionsdata och liknande redovisningskonton och redovisningstransaktioner som omfattar de typiska variationerna och datagränserna för varje fält och på olika språk. Testdata representerar både typisk användning och användning av dåliga aktörer. Prestanda mättes i jämförelse med manuell avstämning av samma data. 

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-the-bank-reconciliation-limitations-when-using-the-system"></a>Vilka är begränsningarna för bankavstämningshjälp? Hur kan användare minimera effekten av bankavstämningsbegränsningar när de använder systemet?

Bankkontoavstämningshjälpen fungerar bäst när redovisningskontonamn, transaktionsbeskrivningar och banktransaktionsbeskrivningar är på samma språk. Blandade språk eller blandat språk i transaktionsbeskrivningar resulterar ofta i färre matchningar och förslag. 

Föreslagna redovisningskonton fungerar bäst på engelska. Även om den här funktionen kan användas på vilket som helst av de tillgängliga [!INCLUDE[prod_short](includes/prod_short.md)] språken, kan användarna uppleva färre transaktionsmatchningar och färre föreslagna redovisningskonton på andra språk. 
<!--

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>What operational factors and settings allow for effective and responsible use of the feature?


-->
## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>I vilka geografiska områden och på vilka språk finns bankavstämningshjälp tillgängligt?

Denna funktion är tillgänglig för alla miljöer, land/regioner och på alla användarspråk. För kundmiljöer i länder/regioner där Azure OpenAI Service inte distribueras måste administratörer först godkänna att data flyttas över gränserna för [!INCLUDE[prod_short](includes/prod_short.md)] för att ansluta till Azure OpenAI Service och för att den här funktionen ska vara tillgänglig. 

För mer information om språk, se föregående fråga om begränsningar.  

## <a name="what-is-expected-of-end-users-when-operating-bank-account-reconciliation-assist"></a>Vad förväntas av slutanvändare när de använder bankkontoavstämningshjälp?

### <a name="while-using-bank-account-reconciliation"></a>När du använder bankkontoavstämning

AI-drivna matchningar och förslag kan ibland vara felaktiga eller ofullständiga. Användare av bankkontoavstämningshjälp måste granska riktigheten i matchningar och förslag från Copilot innan de väljer att behålla dem. Copilot-matchningar och förslag sparas inte i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen förrän du väljer knappen Behåll den och stänger Copilot-fönstret. Du kan också redigera och korrigera eventuella matchningar eller förslag innan du väljer att behålla det. 

### <a name="after-completing-bank-account-reconciliation"></a>När du slutför bankkontoavstämning

Vi rekommenderar att användarna också kontrollerar riktigheten och korrigerar eventuella avvikelser när de har lämnat Copilot-fönstret, inklusive följande aktiviteter: 

- Granska avstämningstestrapporten. 
- Se till att din organisation har lämpliga processer för granskning och revision på plats. 
- Öppna bokförda avstämningar igen med hjälp av funktionen Ångra. 
- Korrigera eventuella felaktiga transaktioner genom omvänd bokföring av transaktioner. 

## <a name="what-is-expected-of-administrators-and-end-users-when-operating-bank-account-reconciliation-assist"></a>Vad förväntas av administratörer och slutanvändare när de använder bankkontoavstämningshjälp?

Slutanvändare, till exempel revisorer, kassörer eller andra som arbetar med affärsredovisning, bör alltid granska riktigheten i matchningar och förslag från Copilot innan de väljer att behålla dem. När du har stämt av med Copilot rekommenderar vi att du granskar avstämningstestrapporten för att verifiera noggrannheten och identifiera eventuella avvikelser. 

Administratörer bör se till att lämpliga redovisningsanvändare har beviljats åtkomst till den här funktionen. 

## <a name="is-copilot-the-only-means-to-completing-bank-account-reconciliation"></a>Är Copilot det enda sättet att slutföra bankkontoavstämning?

Nej – användning av Copilot är valfri. [!INCLUDE[prod_short](includes/prod_short.md)] erbjuder traditionella, icke-AI-drivna sätt att importera kontoutdrag, köra fördefinierade matchningsregler och manuellt tillämpa matchningar och bokföra på lämpliga redovisningskonton. Både det traditionella tillvägagångssättet och Copilot kan användas samtidigt inom en organisation. 

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hur ger jag feedback om AI-genererat innehåll?

Varje gång Copilot ger matchningar eller förslag kan du ge feedback till Microsoft direkt från Copilot-fönstret med hjälp av kontrollerna gilla och ogilla. Din feedback förblir anonym och vi använder dessa uppgifter för att förbättra kvaliteten på tjänsten.


## <a name="see-also"></a>Se även

[Avstämning av bankkonton med hjälp av bankavstämningshjälp (förhandsgranskning)](bank-reconciliation-with-copilot.md)
