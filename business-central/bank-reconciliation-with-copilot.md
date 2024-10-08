---
title: Stämma av bankkonton med Copilot (förhandsversion)
description: Lär dig hur du använder Copilot för att stämma av bankkonton i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template
---

# <a name="reconcile-bank-accounts-with-copilot-preview"></a>Stämma av bankkonton med Copilot (förhandsversion)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

I denna artikel beskrivs hur du använder bankkontoavstämningshjälp för att hjälpa dig att stämma av banktransaktioner med poster i huvudboken i Microsoft Dynamics 365 Business Central.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="about-bank-account-reconciliation-assist"></a>Om bankkontoavstämningshjälp

Bankkontoavstämningshjälp är en uppsättning AI-drivna funktioner som hjälper dig att stämma av bankkonton. Det erbjuder två olika uppgifter genom Copilot:

- Förbättrad matchning av transaktioner med poster i huvudboken

    Du kanske redan känner till knappen **Matcha automatiskt** på sidan **Bankkontoavstämn.** som automatiskt matchar de flesta banktransaktioner med poster i huvudboken. Vi hänvisar till denna åtgärden som *automatisk*. Även om automatisk matchning fungerar bra kan algoritmerna som används ibland resultera i många omatchade transaktioner. Copilot använder AI-teknik för att inspektera omatchade transaktioner och identifiera fler matchningar, baserat på datum, belopp och beskrivningar. Om kunden till exempel betalar flera fakturor som ett engångsbelopp, stämmer Copilot av den enskilda kontoutdragsraden med de flera fakturatransaktionerna.

    [Läs mer om den här uppgiften](#reconcile-bank-accounts-with-copilot).

- Föreslagna redovisningskonton

    För kvarvarande banktransaktioner som inte kan matchas med några transaktioner jämför Copilot transaktionsbeskrivningen med redovisningskontonamn och föreslår det mest sannolika redovisningskontot att bokföra på. Om till exempel omatchade transaktioner har berättelsen*Bränslestopp 24* kan Copilot föreslå att du bokför dem på kontot *Transport*.

    [Läs mer om den här uppgiften](#post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts).

## <a name="available-languages"></a>Tillgängliga språk

[!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

## <a name="prerequisites"></a>Förutsättningar

- Bankkontoavstämningshjälp är aktiverad. En administratör måste slutföra denna uppgift. [Läs mer om hur du konfigurerar Copilot- och AI-funktioner](enable-ai.md).
- Bankkonton i Business Central som du vill stämma av är länkade till ett onlinebankkonto eller konfigurerade med importformat för bankutdrag.
- Du är bekant med bankkontoavstämning i Business Central enligt beskrivningen i [Stäm av bankkonton](bank-how-reconcile-bank-accounts-separately.md).

## <a name="reconcile-bank-accounts-with-copilot"></a>Stämma av bankkonton med Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot i bankkontoavstämning är tänkt att användas som ett komplement till åtgärden automatisk matchning. När du använder Copilot körs därför åtgärden automatisk matchning först för att göra de första matchningarna. Sedan körs Copilot för att försöka matcha transaktioner som åtgärden automatisk matchning inte hanterade.

Du kan använda två sätt för att stämma av bankkonton med Copilot:

- Använd Copilot för att starta en ny avstämning av ett bankkonto, direkt från listan **bankkontoavstämning**.
- Använd Copilot på en ny eller befintlig avstämning på kortet **bankkontoavstämning**.

# [Från bankkontoavstämningslistan](#tab/fromlist)

För den här metoden kan du skapa och stämma av en ny bankkontoavstämning från grunden. Denna metod kräver att du väljer bankkontot. Om bankkontot inte är kopplat till ett onlinekonto måste du även importera kontoutdragsfilen.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bankkontoavstämningar** och väljer sedan relaterad länk.
1. Välj **Stäm av med Copilot** för att öppna fönstret **Stäm av med Copilot**.
1. Ange fältet **Utför avstämning för det här bankkonto** till det bankkonto som du vill stämma av.

    ![Skärmbild som visar fönstret Avstämning med Copilot för avstämning från början.](media/reconcile-bank-accounts-new-copilot.svg)

1. Om det valda bankkontot inte är kopplat till ett onlinebankkonto måste du importera kontoutdragsfilen. Om du vill importera filen väljer du antingen värdet i fältet **Använd transaktionsdata** från eller väljer gemknappen bredvid knappen **Generera**. Använd sedan **Välj filen som ska importeras** för att importera kontoutdragsfilen genom att antingen dra den från enheten eller bläddra i enheten.
1. Om du vill stämma av med Copilot väljer du **Generera**.

    Copilot börjar generera föreslagna matchningar. När det är klart öppnas resultatet av matchningsprocessen i fönstret **Stäm av med Copilot**.

1. Granska de föreslagna matchningarna enligt beskrivningen i följande avsnitt.

# [Från kortet bankkontoavstämning](#tab/fromcard)

För den här metoden använder du Copilot antingen på en ny bankkontoavstämning som du skapar manuellt eller genom att redigera en befintlig avstämning.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bankkontoavstämningar** och väljer sedan relaterad länk.
1. Gör något av följande:

    - Välj **Ny** för att starta en ny avstämning.
    - Markera och öppna en befintlig avstämning i listan.

1. På kortet **Avstämning av bankkonto** väljer du **Stäm av med Copilot**

    ![Skärmbild som visar knappen Avstämning med Copilot på en bankkontoavstämningskortet.](media/bank-reconciliation-copilot-card.svg)

    Copilot börjar generera föreslagna matchningar. När det är klart öppnas resultatet av matchningsprocessen i fönstret **Stäm av med Copilot**.

1. Granska de föreslagna matchningarna enligt beskrivningen i följande avsnitt.
---

### <a name="review-save-or-discard-proposed-matches"></a>Granska, spara eller ignorera föreslagna matchningar

När du har kört Copilot visas detaljerade resultat i fönstret **Stäm av med Copilot**, inklusive eventuella föreslagna matchningar. Vid denna tidpunkt har ingen matchning som Copilot föreslog sparats. Därför har du möjlighet att granska förslagen och spara eller ignorera dem som du vill.

![Skärmbild som visar föreslagna matchningar i fönstret Avstämning med Copilot.](media/bank-reconciliation-copilot-window.png)

Fönstret **Stämma av med Copilot** är uppdelat i två delar. Det övre avsnittet innehåller allmän information om resultatet. I det nedre avsnittet **Matcha förslag** visas de matchningar som föreslagits av Copilot.

I följande tabell beskrivs fälten i övre avsnittet.

| Fält | Description |
|---|---|
| Automatiskt matchade | Antalet kontoutdragsrader som den automatiska åtgärden matchade. Välj värdet för att visa avstämningskortet. |
| Copilot-matchad | Antalet kontoutdragsrader som Copilot föreslog matchningar för. Du kan se detaljer om matcherna i avsnittet **Matcha förslag**. |
| Kontoutdragets slutsaldo | Det slutsaldo som står på det bankkontoutdrag som du stämmer av med. |
| Bokför om helt kopplad | Aktivera det här alternativet om du vill bokföra bankkontoavstämningen automatiskt när alla rader (100 %) matchas och du har valt **Behåll den**. |

I avsnittet **Matchningsförslag** granskar du de föreslagna matchningarna rad för rad. Vidta sedan lämpliga åtgärder:

- Om du vill ignorera en enstaka föreslagen matchning markerar du den i listan och väljer sedan **Ta bort rad**.
- Om du vill ignorera alla föreslagna matchningar och stänga fönstret **Stämma av med Copilot**, välj knappen Ignorera (papperskorgen) ![knappen Ignorera.](media/copilot-delete-trash-can.png) bredvid knappen **Behåll** längst ned i fönstret.
- Om du vill bokföra den fullständigt matchade avstämningen automatiskt när du sparar den aktiverar du alternativet **Bokför om helt kopplad**.
- Om du vill spara de matchningar som för närvarande visas i fönstret **Stämma av med Copilot**, välj **Behåll**.

## <a name="post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts"></a>Boka omatchade banktransaktionsbelopp till föreslagna redovisningskonton

Det här avsnittet lär du dig hur du använder Copilot för att bokföra oavstämda bankkontoutdragsradbelopp (anges i fältet **Differens**) till ett redovisningskonto. Den här uppgiften kan bara utföras från en befintlig avstämning.

1. Gå till listan **Bankkontoavstämningar** och öppna den befintliga avstämningen som innehåller de avstämda raderna.

    Det här steget ger dig en tydlig bild av alla oavstämda kontoutdragsrader som måste överföras till redovisningskontot.

1. I fönstret **Bankkontoutdragsrader** identifierar du bankkontoutdragsrader och markerar en eller flera rader som du vill stämma av.

    Copilot fokuserar på de valda raderna för att bokföra nya betalningar på redovisningskontot.

1. Välj **Bokför skillnaden till redovisningskonto** för att starta processen.

    ![Skärmbild som visar knappen Bokför skillnaden till redovisningskonto på bankkontoavstämningskortet.](media/bank-reconciliation-transfer-gl-copilot-card.png)

    Copilot börjar generera förslag för att bokföra nya betalningar.

1. Efter Copilot har genererat förslag öppnas fönstret **Copilot-förslag för bokföring av skillnader till huvudkonton** redovisningskonton.

    Avsnittet **Matcha förslag** i detta fönster visar förslagen. Upplevelsen liknar upplevelsen för att avstämma med Copilot.

    ![Skärmbild som visar Copilot-förslag för bokföringsskillnader till fönster för huvudkonton.](media/bank-reconciliation-gl-transfer-proposed-matches.png)

1. Granska varje förslag rad för rad för att säkerställa att de föreslagna betalningarna är bokförda.

    - Om du detaljgranskar förslaget genom att välja det i listan kommer du till en lista över konton. Härifrån kan du välja ett annat konto. Du kan endast göra den här typen av manuell korrigering när du använder flödet **Bokför skillnad till redovisningskonto**, inte i matchande flöde.
    - Om du väljer **Spara** bredvid ett förslag kan du lägga till mappningen på sidan **Mappa text till konto**. Nästa gång texten visas under matchningen mappas den till det föreslagna kontot.

1. Ignorera eller spara förslag.

    - För att ignorera ett specifikt förslag, välj det i listan och välj sedan **Ta bort rad**. Om du vill ignorera alla förslag och stänga Copilot väljer du knappen Ignorera (papperskorgen) ![knappen Ignorera.](media/copilot-delete-trash-can.png) bredvid knappen **Behåll** längst ned i fönstret.
    - Om förslagen uppfyller dina krav och du vill spara dem väljer du **Behåll detta**.

         Detta steg bekräftar överföringen av de valda förslagen från bankkontot till redovisningskontot. Den bokför nya betalningar på de föreslagna redovisningskontona och kopplar motsvarande rader till de resulterande bankkontotransaktionerna.

## <a name="next-steps"></a>Nästa steg

[Validera bankkontoavstämning](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)

## <a name="see-also"></a>Se även

[Felsöka Copilot- och AI-funktioner](ai-copilot-troubleshooting.md)  
[Ansvarig AI vanliga frågor för bankavstämningshjälp](faqs-bank-reconciliation.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md)  
[Tillämpa betalningar automatiskt och jämka bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md)
