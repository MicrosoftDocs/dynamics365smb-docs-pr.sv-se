---
title: Fördela intäkter och kostnader till flera redovisningskonton
description: Läs om hur du fördelar kostnader på ett eller flera konton i redovisningen.
author: brentholtorf
ms.author: bholtorf
ms.date: 09/04/2023
ms.topic: conceptual
ms.search.keywords: 'allocate, allocation, accounts'
ms.search.form: '39, 2673, 2670, 2674,'
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="allocate-revenue-and-costs-to-multiple-general-ledger-accounts"></a>Fördela intäkter och kostnader till flera redovisningskonton

I den här artikeln beskrivs hur du använder fördelningskonton för att fördela belopp i försäljnings- och inköpsdokument samt i redovisningsjournalrader till olika redovisningskonton. Du kan fördela belopp genom fast eller variabel fördelning.  

Vid fördelning delas en redovisningsjournalrad upp i de rader som definierats på sidan **Fördelningskonto**. Om du till exempel delar upp en hyreskostnad på tre sätt med hjälp av dimensioner får du tre rader att bokföra för fördelningen. Du får därför sex redovisningsrader (eller möjligen fler, om du använder moms eller omsättningsskatt). Även om detta bokför fler redovisningstransaktioner än du kanske behöver, kan du återföra enskilda rader istället för att återföra hela fördelningen.

Allokeringskonton fungerar också med uppskov. Mer information om periodiseringar finns i [Periodisera intäkter och utgifter](finance-how-defer-revenue-expenses.md).

I följande tabell beskrivs de fördelningsmetoder som du kan använda.

|Allokeringsmetod  |Description  |
|---------|---------|
|Åtgärdat     | När du vill dela upp utgifter på ett sätt som upprepas över en längre tidsperiod kan du använda en fast fördelning. Med en fast fördelning kan du definiera fördelningsdelningen. Uppdelningen ändras bara när du ändrar konfigurationen på sidan **Fördelningskonto**.        |
|Olika     | Om du vill fördela intäkter eller utgifter baserat på värden som ändras över tid använder du variabelallokeringsmetoden. Med hjälp av variabla fördelningar kan du ange vilka källor som ska användas för att beräkna fördelningsprocenten. Den här metoden är till exempel användbar för att dela upp personalkostnader efter varierande personalantal på olika avdelningar. Ett annat exempel är fördelningen av hyreskostnaden baserat på produktionsgolvet, som kan variera per produktionslinje över tid. Variabla fördelningar använder en kombination av dimensioner och statistiska konton för att bestämma hur beloppen fördelas under en tidsperiod. Mer information om statistiska konton finns i [Analysera data med statistiska konton](bi-use-statistical-accounts.md). Om du vill lära dig mer om dimensioner går du till [Arbeta med dimensioner](finance-dimensions.md).        |

## <a name="use-a-fixed-share-or-percentage-method-to-allocate-amounts"></a>Använda en metod med fast andel eller procentsats för att fördela belopp

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Fördelningskonto** och välj sedan relaterad länk.  
1. På sidan **Fördelningskonton** väljer du åtgärden **Ny**.
1. Fyll i fälten **Nr.** och **Namn** .
1. I fältet **Kontotyp** väljer du **Fast**.
1. I fältet **Målkontotyp** väljer du **Redovisningskonto** eller **Bankkonto**.
1. I fältet **Målkontonummer** väljer du det konto som värdet ska bokföras på.
1. Tillval: Välj åtgärden **Dimensioner** och ange sedan vilka dimensioner som ska bokföras för raden.
1. I fälten **Andel** och **Procent** anger du hur beloppen ska fördelas till målkontot.
  
   > [!TIP]
   > Om du anger det faktiska belopp som ska fördelas för en fast fördelning i fältet **Andel** visar fältet **Procent** procentandelen av det totala beloppet.
1. Upprepa den här processen för varje konto som ska inkluderas i fördelningen.

## <a name="use-a-variable-method-to-allocate-amounts"></a>Använda en variabelmetod för att fördela belopp

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Fördelningskonto** och välj sedan relaterad länk.  
1. På sidan **Fördelningskonton** väljer du åtgärden **Ny**.
1. Fyll i fälten **Nr.** och **Namn** .
1. I fältet **Kontotyp** väljer du **Variabel**.
1. I fältet **Målkontotyp** väljer du **Redovisningskonto**.
1. I fältet **Målkontonummer** väljer du det konto som värdet ska bokföras på.
1. I fältet **Typ av nedbrytningskonto** väljer du **Statistiskt konto**.
1. I fältet **Beräkningsperiod** väljer du den period som beloppen ska fördelas för.
1. Valfritt: Om du vill filtrera efter specifika globala dimensionsvärden väljer du åtgärden **Filter för nedbrytningskontosaldo** och anger sedan filtervärdena.
1. Tillval: Välj åtgärden **Dimensioner** och ange sedan vilka dimensioner som ska bokföras för raden.

## <a name="allocate-amounts-on-the-fly"></a>Tilldela belopp i farten

Du skapar allokeringskonton för att dela intäkter och kostnader för redovisningskonton och bankkonton. Automatisering av fördelningar kan spara tid. Om du däremot vill använda allokeringskonton, men inte vill skapa dem för varje redovisningskonto, kan du spara ännu mer tid.

Med alternativet Ärva från överordnat element kan du använda fördelningskontot för att dela upp belopp för valfritt redovisningskonto på en rad i ett dokument eller en journal. I fältet **Kontotyp** på en dokument- eller journalrad väljer du ett redovisningskonto och väljer sedan fördelningskontot i fältet **Fördelningskontonr.**. Beloppet på raden delas upp för redovisningskontot enligt inställningarna på ditt fördelningskonto. Detta är ett mindre transparent sätt att fördela, men du behöver inte skapa ett allokeringskonto specifikt för redovisningskontot.

Ad hoc-tilldelningar är enkla att ställa in. Istället för att ange ett bank- eller redovisningskonto i fältet **Typ av målkonto** på sidan **Fördelningskonto** väljer du alternativet **Ärv från överordnat element**. Lämna fältet **Målkontonummer** tomt. När du väljer redovisningskonto på dokument- eller journalraden används det kontot för att fördela belopp.

## <a name="verify-that-amounts-distribute-correctly-before-you-post-them"></a>Kontrollera att beloppen fördelas korrekt innan du bokför dem

Det finns några olika sätt att kontrollera att beloppen fördelas korrekt:

* På sidan **Fördelningskonto** väljer du åtgärden **Testa fördelning**. Använd fältet **Belopp att fördela** för att testa olika belopp.
* På sidan **Redovisningsjournaler** väljer du journalen och använder sedan åtgärden **Förhandsgranska bokföring**.

## <a name="adjust-the-distribution"></a>Justera fördelningen

Om du hittar något i en fördelning som du vill ändra kan du justera fördelningen innan du bokför den.  

1. Öppna dokumentet eller journalen som har den fördelning som du vill ändra.
1. Välj raden och välj sedan åtgärden **Omfördela kontofördelningar**.
1. Gör justeringen på sidan **Ändra fördelningar**.

## <a name="post-an-allocation-transaction"></a>Bokför en fördelningstransaktion

Följande steg beskriver hur du bokför en fördelningstransaktion från en redovisningsjournal. Stegen är desamma som för försäljnings- och inköpsdokument.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler** och välj sedan relaterad länk.  
1. Skapa en ny rad. Fyll i fälten på samma sätt som för andra typer av redovisningsjournaler.
1. Om du använder en fast eller variabel tilldelning fyller du i följande fält:
    1. I fältet **Kontotyp** väljer du **Fördelningskonto**.
    1. I fältet **Kontonr.** väljer du fördelningskonto.
1. Om du använder en fördelning som använder alternativet Ärv från överordnat element gör du följande:
    1. I fältet **Kontotyp** väljer du **Redovisningskonto**.
    1. I fältet **Kontonr.** väljer du redovisningskontot.
    1. I fältet **Fördelningskontonr.** väljer du det fördelningskonto som har konfigurerats för att använda alternativet Ärv från överordnat element. 
1. Välj **Bokför**.

## <a name="see-also"></a>Se även

[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
