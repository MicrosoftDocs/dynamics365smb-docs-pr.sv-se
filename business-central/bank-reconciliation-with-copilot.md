---
title: Stämma av bankkonton med avstämningshjälp
description: Lär dig hur du använder Copilot för att stämma av bankkonton i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 10/25/2023
ms.custom: bap-template
---

# Stämma av bankkonton med Copilot (förhandsversion)

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

I denna artikel beskrivs hur du använder bankkontoavstämningshjälp för att hjälpa dig att stämma av banktransaktioner med poster i huvudboken i Business Central.

## Om bankkontoavstämningshjälp

Bankkontoavstämningshjälp är en uppsättning AI-drivna funktioner som hjälper dig att stämma av bankkonton. Bankkontoavstämningshjälp ger dig två olika uppgifter via Copilot:

- Förbättrad matchning av transaktioner med poster i huvudboken

   Du kanske redan känner till **Matcha automatiskt** på sidan **Bankkontoavstämn.** som automatiskt matchar de flesta banktransaktioner med poster i huvudboken. Vi hänvisar till denna åtgärden som *automatisk*. Även om automatisk matchning fungerar bra kan algoritmerna som används ibland resultera i många omatchade transaktioner. Copilot använder AI-teknik för att inspektera återstående transaktioner och identifiera fler matchningar, baserat på datum, belopp och beskrivningar. Om till exempel flera fakturor har betalats som ett engångsbelopp av en kund, stämmer Copilot av den enskilda kontoutdragsraden med de flera fakturatransaktionerna.
   
   Gå till [Stäm av bankkonton med Copilot](#reconcile-bank-accounts-with-copilot).

- Föreslagna redovisningskonton

  För kvarvarande banktransaktioner som inte kan matchas med några transaktioner jämför Copilot transaktionsbeskrivningen med redovisningskontonamn och föreslår det mest sannolika redovisningskontot att bokföra på. Copilot kan till exempel föreslå att transaktioner med berättelsen "Bränslestopp 24" bokförs på kontot "Transport".
  
   Gå till [Överföra omatchade banktransaktioner till föreslagna redovisningskonton](#transfer-unmatched-bank-transactions-to-suggested-general-ledger-accounts).


   
## Förutsättningar

- Bankkontoavstämningshjälp är aktiverad och aktiverad. Denna uppgift utförs av en administratör. [Läs mer om hur du aktiverar Copilot- och AI-funktioner](enable-ai.md).
- Bankkonton i Business Central som du vill stämma av är länkade till ett onlinebankkonto eller konfigurerade med importformat för bankutdrag. 
- Du är bekant med bankkontoavstämning i Business Central enligt beskrivningen i [Stäm av bankkonton](bank-how-reconcile-bank-accounts-separately.md). 

<!--H2s. Required. A how-to article explains how to do a task. The bulk of each H2 should be a procedure.-->
## Stäm av bankkonton med Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot i bankkontoavstämning är tänkt att användas som ett komplement till åtgärden automatisk matchning. När du använder Copilot körs därför åtgärden automatisk matchning först för att göra de första matchningarna. Sedan körs Copilot för att försöka matcha transaktioner som åtgärden automatisk matchning inte hanterade.   

Det finns två sätt att stämma av bankkonton med Copilot. Du kan använda Copilot för att starta en ny avstämning av ett bankkonto, direkt från listan **Bankkontoavstämning** eller så kan du använda Copilot på en ny eller befintlig avstämning på kortet **Bankkontoavstämn.**.

# [Från bankkontoavstämningslistan](#tab/fromlist) 

Med den här metoden kan du skapa och stämma av en ny bankkontoavstämning från grunden. Den här metoden kräver att du väljer bankkontot och importerar kontoutdragsfilen om bankkontot inte är länkat till ett onlinekonto.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bankkontoavstämningar** och väljer sedan relaterad länk. 
1. Välj åtgärden **Stäm av med Copilot** för att öppna fönstret **Stäm av med Copilot**.
1. Ange fältet **Utför avstämning för det här bankkonto** till det bankkonto som du vill stämma av.

   ![Visar fönstret Avstäm med copilot för avstämning från början](media/reconcile-bank-accounts-new-copilot.svg) 
 
1. Om det valda bankkontot inte är kopplat till ett onlinebankkonto måste du importera kontoutdragsfilen. Om du vill importera filen väljer du antingen värdet i fältet **Använd transaktionsdata** från eller väljer gemknappen bredvid knappen **Generera**. Använd sedan **Välj filen som ska importeras** för att importera kontoutdragsfilen genom att antingen dra den från enheten eller bläddra i enheten.
1. Om du vill stämma av med Copilot väljer du **Generera**.

   Copilot börjar generera föreslagna matchningar. När det är klart öppnas resultatet av matchningsprocessen i fönstret Stäm av med Copilot.

1. Granska de föreslagna matchningarna enligt beskrivningen i följande avsnitt.

# [Från kortet bankkontoavstämning](#tab/fromcard) 

Med den här metoden använder du Copilot antingen på en ny bankkontoavstämning som du skapar manuellt eller genom att redigera en befintlig avstämning. 


1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bankkontoavstämningar** och väljer sedan relaterad länk. 
1. Gör något av följande:

   - Välj **Ny** för att starta en ny avstämning. 
   - Markera och öppna en befintlig avstämning i listan.
1. På kortet **Avstämning av bankkonto** väljer du **Stäm av med Copilot**

   ![Visar avstämningen med copilot-åtgärden på bankkontoavstämningskortet](media/bank-reconciliation-copilot-card.svg) 

   Copilot börjar generera föreslagna matchningar. När det är klart öppnas resultatet av matchningsprocessen i fönstret **Stäm av med Copilot**. 

1. Granska de föreslagna matchningarna enligt beskrivningen i följande avsnitt. 
---

### Granska, spara eller ignorera föreslagna matchningar

När du har kört Copilot visas detaljerade resultat i fönstret **Stäm av med Copilot**, inklusive eventuella föreslagna matchningar. Vid denna tidpunkt har inga matchningar som föreslagits av Copilot sparats, så det ger dig möjlighet att inspektera förslagen och spara eller kassera som du vill.

![Visar fönstret Stäm av med copilot med föreslagna matchningar](media/bank-reconciliation-copilot-window.png) 

Fönstret Copilot delas upp i två avdelningar. Det övre avsnittet innehåller allmän information om resultatet, som beskrivs i följande tabell.  I det nedre avsnittet **Matchat förslag** visas de matchningar som föreslagits av Copilot.

|Fält|Beskrivning|
|-|-|
|Automatiskt matchade|Anger hur många rader på kontoutdraget som matchas av åtgärden automatisk matchning. Välj värdet för att visa avstämningskortet.  |
|Copilot-matchad|Anger hur många rader på kontoutdraget som har matchningar föreslagna av Copilot. Du kan se detaljer om matcherna i avsnittet **Föreslagna matchningar**.|
|Kontoutdragets slutsaldo|Anger det slutsaldo som står på det bankkontoutdrag som du stämmer av med.|
|Bokför om helt kopplad|Aktivera den här växeln om du vill bokföra bankkontoavstämningen automatiskt när alla rader (100 %) matchas och du har valt **Behåll den**.|

#### Spara eller ignorera föreslagna matchningar

I avsnittet **Matchade förslag** granskar du de föreslagna matchningarna rad för rad och vidtar sedan lämplig åtgärd:

- Om du vill ignorera en enstaka föreslagen matchning markerar du den i listan och väljer sedan åtgärden **Ta bort rad**.

- För att kassera alla föreslagna matchningar och stänga Copilot-fönstret, välj knappen Kasta (papperskorgen) ![Visar papperskorgsikonen för att radera alla Copilot-förslag för bankkontoavstämning](media/copilot-delete-trash-can.png) bredvid knappen **Behåll detta** längst ned i fönstret.

- Om du vill bokföra den fullständigt matchade avstämningen automatiskt när du sparar den aktiverar du reglaget **Bokför om helt kopplad**.  
- Om du vill spara de matchningar som för närvarande visas i fönstret Copilot väljer du **Behåll**.


## Överföra omatchade banktransaktioner till föreslagna redovisningskonton

I det här avsnittet får du lära dig hur du använder Copilot för att överföra bankkontoutdrag som inte stämts av från bankkontot till ett redovisningskonto. Den här uppgiften kan bara utföras från en befintlig avstämning. 

1. Gå till listan **Bankkontoavstämningar** och öppna den befintliga avstämningen som innehåller de avstämda raderna.

   Börja med att öppna en befintlig bankkontoavstämning. Det här steget ger dig en tydlig bild av alla oavstämda kontoutdragsrader som behöver överföras till redovisningskontot.

2. I fönstret **Bankkontoutdragsrader** identifierar du fönstret Bankkontoutdragsrader och markerar en eller flera rader som du vill stämma av.

   Dessa rader är de kontoutdragsrader som Copilot fokuserar på för överföring till redovisningskontot.

3. Välj **Överför till redovisningskonto** för att starta processen.

   ![Visar överför till redovisning med copilot-åtgärden på bankkontoavstämningskortet](media/bank-reconciliation-transfer-gl-copilot-card.svg) 

   Det här steget får Copilot att börja generera förslag för överföringen.

4. När Copilot har genererat förslag öppnas fönstret **Copilot-förslag för överföring av redovisningskonton** redovisningskonton.

   I det här fönstret visas förslagen i avsnittet **Matchat förslag**. Upplevelsen liknar avstämning med Copilot.

   ![Visar sidan för överföring till redovisning med copilot-föreslagna matchningar för bankkontoavstämning](media/bank-reconciliation-gl-transfer-proposed-matches.png) 

5. Granska varje förslag rad för rad för att säkerställa att de föreslagna överföringarna är korrekta.

   - Om du detaljgranskar förslaget genom att välja det i listan kommer du till en lista över konton. Härifrån kan du välja ett annat konto. Den här typen av manuell korrigering är endast möjlig när du använder flödet **Överför till redovisningskonto**, inte i matchande flöde. 
   - Om du väljer **Spara...** bredvid ett förslag kan du lägga till mappningen på sidan **Mappa text till konto** så att nästa gång texten visas under matchning mappas den till det föreslagna kontot.

6. Ignorera eller spara förslag.

   - Om du vill ignorera ett specifikt förslag, välj det i listan och välj sedan **Ta bort rad**. För att kassera alla förslag och avsluta Copilot-fönstret, välj knappen Kasta (papperskorgen) ![Visar papperskorgsikonen för att radera alla Copilot-förslag för bankkontoavstämning](media/copilot-delete-trash-can.png) bredvid knappen **Behåll detta** längst ned i fönstret.
   
   - Om förslagen uppfyller dina krav och du vill spara dem väljer du **Behåll detta**. 

      Detta steg bekräftar överföringen av de valda förslagen från bankkontot till redovisningskontot. Den bokför nya betalningar på de föreslagna redovisningskontona och kopplar motsvarande rader till de resulterande bankkontotransaktionerna.

## Nästa steg

[Validera bankkontoavstämning](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)  

## Se även
[Felsöka Copilot- och AI-funktioner](ai-copilot-troubleshooting.md)  
[Ansvarig AI vanliga frågor för bankavstämningshjälp](faqs-bank-reconciliation.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md)  
[Tillämpa betalningar automatiskt och jämka bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md) 
