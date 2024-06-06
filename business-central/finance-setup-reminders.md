---
title: Konfigurera villkor och nivåer för betalningspåminnelser
description: Konfigurera Business Central så att du kan skicka påminnelser om förfallna betalningar och lägga till avgifter eller avgifter på grund av förseningen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 03/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Konfigurera villkor och nivåer för betalningspåminnelser

Du kan använda betalningspåminnelser för att informera kunder och begära betalning. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

> [!TIP]
> När du har ställt in villkor och nivåer för betalningspåminnelser kan du inkludera dem i automatiserade processer för att skapa, utfärda och skicka påminnelser. För att lära dig mer om den automatiserade processen, gå till [Automatisera påminnelser i samlingar](finance-automate-reminders.md).

## Betalningspåminnelsevillkor

Om en betalning förfaller måste du bestämma när och hur betalningspåminnelsen ska skickas till kunden i fråga. Dessutom kanske du vill debitera kundens konto för ränta eller avgifter. Du kan ange valfritt antal villkor för betalningspåminnelser.  

> [!NOTE]
> Om du vill beräkna dröjsmålsränta på förfallna betalningar kan du göra detta när du skapar betalningspåminnelser. Om du däremot endast vill beräkna dröjsmålsränta och informera dina kunder om det utan att skicka betalningspåminnelser bör du använda [räntefakturor](finance-setup-finance-charges.md). Mer information finns i [Betalningspåminnelser](receivables-collect-outstanding-balances.md#reminders) samt [Ränta](receivables-collect-outstanding-balances.md#finance-charges).

### Konfigurera bilagor och brödtexter i e-post för kommunikation

På sidan **Konfiguration av betalningspåminnelsevillkor** kan ställa in bifogade texter och vanliga e-postmeddelanden att använda antingen för alla påminnelsenivåer, eller skapa specifika meddelanden för varje nivå. Meddelandet du skickar för den första påminnelsenivån kan till exempel ha en annan ton eller annat innehåll än den andra eller tredje. Om du vill skapa bilagor och e-postmeddelandetexter för alla nivåer väljer du **Kundkommunikation** högst upp på sidan. För att skapa meddelanden för specifika rader, på snabbfliken **Betalningspåminnelsenivå**, välj en rad och välj sedan **Kundkommunikation** på snabbfliken.

Som standard använder bilagor och e-posttexter din språkinställning. Om du skickar betalningspåminnelser till kunder i andra länder kanske du vill kommunicera på andra språk. Du kan skapa texter för varje språk som [!INCLUDE [prod_short](includes/prod_short.md)] stöder genom att använda **Lägg till text för språk**. Om du gör det kontrollerar du att språken är desamma för bifogade texter och e-posttexter. Om de inte matchar och påminnelseperioden har mer än en nivå kanske automatiseringen inte kan anpassa meddelandet för en eller flera nivåer. För att verifiera att språken matchar, använd åtgärden **Översikt över kommunikation** och jämför kommunikationen för texterna.

När du skickar ett e-postmeddelande är påminnelsen en rapport som du bifogar till e-postmeddelandet. Du definierar rapporten som genererar påminnelsen på sidan **Rapportval – Påminnelse/ränta**, där du också väljer rapporten som innehåller e-postmeddelandets brödtext i **Namn för layout på brödtext i e-post**. När du skickar e-post till dina kunder infogas texterna på snabbfliken **E-posttext** i den rapport som är markerad i fältet **Namn för layout på brödtext i e-post**. Standardrapporten har ett textfält för den här texten. Om du vill kan du redigera rapporten, till exempel för att lägga till eller ta bort innehåll. Redigera layouten för rapporterna på sidan **Rapportlayouter**. Mer information om rapportlayouter finns i [Komma igång med att skapa rapportlayouter](ui-get-started-layouts.md).

> [!NOTE]
> Att kommunicera via e-post direkt från [!INCLUDE [prod_short](includes/prod_short.md)] kräver att du är inställd på att göra det. Mer information om hur du ansluter e-postkonton med [!INCLUDE [prod_short](includes/prod_short.md)] till finns i [Konfigurera e-post](admin-how-setup-email.md).

### Så här ställer du in betalningspåminnelsevillkor

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **påminnelsevillkor** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Om du vill använda fler än en uppsättning villkor, anger du en kod för varje kombination.

## Betalningspåminnelsenivåer

För varje betalningspåminnelseperiod kan du definiera ett obegränsat antal betalningspåminnelsenivåer, men de flesta företag använder bara två eller tre nivåer. Första gången en betalningspåminnelse skapas för en kund används inställningen från nivå 1. När betalningspåminnelsen skickas ut registreras nivånumret på betalningspåminnelsetransaktionerna som skapas och kopplas till de enskilda kundreskontratransaktionerna. Om kunden måste påminnas igen kontrolleras alla betalningspåminnelsetransaktioner som är kopplade till öppna kundreskontratransaktioner så att det högsta nivånumret hittas. Villkoren från nästa nivånummer används sedan för den nya betalningspåminnelsen.

Om du skapar fler betalningspåminnelser än du har definierat nivåer för, används villkoren för den högsta nivån. Du kan skapa så många betalningspåminnelser som fältet **Max. antal påminnelser** i betalningspåminnelsevillkoren tillåter.

### Så här ställer du in nivåer för betalningspåminnelser

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **påminnelsevillkor** och väljer sedan relaterad länk.  
2. På sidan **betalningspåminnelsevillkor** och välj raden med de villkor som du vill ange nivåer för och klicka sedan på åtgärden **Nivåer**.  
3. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > Inställningen i fältet **Beräkna ränta** bestämmer om räntan ska visas på betalningspåminnelsen när betalningspåminnelsen utfärdas. Fältet **Bokför ränta** på sidan **Betalningspåminnelsevillkor** avgör emelelrtid om den beräknade räntan måste bokföras på redovisningskontot och kundkontot.
    >
    > Välj fältet **Beräkna ränta** om du vill ange att ränta ska beräknas.

    För varje betalningspåminnelsenivå anger du ytterligare avgifter i både lokala och utländska valutor. Du kan definiera många räntefaktureringsavgifter i utländsk valuta för respektive kod på sidan **Betalningspåminnelsevillkor**.  

    Ytterligare avgifter kan beräknas på tre olika sätt som definieras av värdet i fältet **Ytterl. avgiftsberäkningstyp**.  

    - **Fast**

        Avgifter beräknas baserat på värdena i fälten **Ytterligare avgift** på raden för själva betalningspåminnelsenivån.  
    - **Enkel dynamik**

        Avgifter beräknas baserat på värdena i fälten i relevant rad på sidan **Inställningar för ytterligare avgifter** för den betalningspåminnelsenivån.
    - **Ackumulerad dynamik**

        Avgifter beräknas baserat på värdena i fälten i kombinerade rader på sidan **Inställningar för ytterligare avgifter** för den betalningspåminnelsenivån.

4. Välj åtgärden **Valutor**.
5. På sidan **Valutor för betalpåm.nivå** kan du definiera för varje betalningspåminnelsekod och motsvarande nivånummer en valutakod och en tilläggsavgift.

    > [!NOTE]  
    > När du skapar räntefakturor i utländsk valuta används de villkor för utländsk valuta som definieras här för att skapa betalningspåminnelser. Om det inte finns några betalningsvillkor definierade för utländsk valuta används de villkor för BVA som angetts på sidan **Betalningspåminnelsenivåer** och omvandlas till relevant valuta.

    För varje betalningspåminnelsenivå kan du ange text som ska infogas före (**Inledande text**) eller efter (**Avslutande text**) transaktionerna i betalningspåminnelsen.

6. Välj åtgärden **Inledande text** eller **Avslutande text** och fyll i på sidan **Betalningspåminnelsetext**.
7. Om du vill infoga relaterade värden i den resulterande betalningspåminnelsetexten, anger du följande platshållare i **Text**-fältet.  

    |Platshållare|Värde|  
    |-----------------|-----------|  
    |%1|Innehållet i fältet **Dokumentdatum** i betalningspåminnelsens huvud|  
    |%2|Innehållet i fältet **Förfallodatum** i betalningspåminnelsens huvud|  
    |%3|Innehållet i fältet **Räntesats** på de relaterade räntevillkor|  
    |%4|Innehållet i fältet **Återstående belopp** i betalningspåminnelsens huvud|  
    |%5|Innehållet i fältet **Räntebelopp** i betalningspåminnelsens huvud|  
    |%6|Innehållet i fältet **Avgift** i betalningspåminnelsens huvud|  
    |%7|Påminnelsens totalbelopp.|  
    |%8|Innehållet i fältet **Betalningspåminnelsenivå** i betalningspåminnelsens huvud|  
    |%9|Innehållet i fältet **Valutakod** i betalningspåminnelsens huvud|  
    |%10|Innehållet i fältet **Bokföringsdatum** i betalningspåminnelsens huvud|  
    |%11|Företagsnamnet|  
    |%12|Innehållet i fältet **Avgift per rad** i betalningspåminnelsens huvud|  

    Om du skriver exempelvis **du är skyldig %9 %7 som förfaller %2.**, påminnelsen innehåller följande text: **Du äger USD 1 200,50 som förfaller 02-02-2024.**.

    > [!NOTE]
    > [!INCLUDE [prod_short](includes/prod_short.md)] förfallodatumet beräknas enligt den formel du anger. Mer information finns i [använda datumformler](ui-enter-date-ranges.md#use-date-formulas).

8. Om du vill ange språk för ett e-postmeddelande väljer du åtgärden **Lägg till text för språk**. Fältet **Språkkod** uppdateras så att ditt val visas. På snabbfliken **E-posttext** anger du innehållet i meddelandet på det valda språket.

När du har angett betalningspåminnelsevillkoren kan du tilldela dem till kunder på kundkortssidorna. Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).  

## Se även

[Kräva in utestående saldon](receivables-collect-outstanding-balances.md)  
[Skicka påminnelser om utestående saldon](receivables-send-reminders.md)  
[Konfigurera räntevillkor](finance-setup-finance-charges.md)  
[Ställa in Finance](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
