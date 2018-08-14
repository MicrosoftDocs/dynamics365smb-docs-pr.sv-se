---
title: "Påminna eller bötfälla kunder med förfallna betalningar | Microsoft Docs"
description: "Beskriver hur du skickar en påminnelse till en kund om en betalning förfaller och lägger till avgifter på grund av förseningen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 07/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: 566594f04a1b189fe2263a945d8bd7d565539930
ms.contentlocale: sv-se
ms.lasthandoff: 07/09/2018

---
# <a name="collect-outstanding-balances"></a>Kräva in utestående saldon
Betalningshanteringen består i att kontrollera om kunderna betalar i tid. Om kunderna har förfallna betalningar, kan du börja med att skicka kundkontoutdragsrapporten som betalningspåminnelse. Alternativt kan du skicka betalningspåminnelser.

Du kan använda betalningspåminnelser för att påminna kunder om förfallna belopp. Du kan även använda betalningspåminnelser för att beräkna ränta eller avgifter och inkludera dem i betalningspåminnelsen. Använd räntefakturor om du vill debitera kunder för ränta eller avgifter utan att påminna dem om förfallna belopp.

## <a name="reminders"></a>Påminnelser
Innan du kan skapa betalningspåminnelser måste du ange betalningspåminnelsevillkor och tilldela dem till dina kunder. Varje betalningspåminnelse fördefinierar betalningspåminnelsenivåer. Varje betalningspåminnelsenivå inkluderar regler om när en betalningspåminnelse ska skickas ut, till exempel hur många dagar efter fakturans förfallodatum eller datumet för den föregående betalningspåminnelsen. Innehållet i fönstret **Räntevillkor** avgör om ränta beräknas på betalningspåminnelsen.  

Du kan regelbundet köra batch-jobbet **Skapa betalningspåminnelser** för att skapa betalningspåminnelser för alla kunder med förfallna saldon eller också kan du manuellt skapa en betalningspåminnelse för en specifik kund och sedan låta raderna beräknas och fyllas i automatiskt.  

När du skapat betalningspåminnelserna kan du ändra dem. Texten som visas i början och i slutet av en betalningspåminnelse bestäms av villkoren för betalningspåminnelsenivån och visas i kolumnen **Beskrivning**. Om ett beräknat belopp har infogats automatiskt i den inledande eller avslutande texten justeras inte texten om du tar bort rader. Då måste du använda funktionen **Uppdatera bet.påminnelsetext**.  

För kundreskontratransaktioner med fältet **Stoppad** ifyllt får du inga uppmaningar om att skapa betalningspåminnelser. Men om en betalningspåminnelse skapas med en annan transaktion som bas, kommer en förfallen transaktion som markerats Stoppad också att inkluderas i betalningspåminnelsen. Ränta beräknas inte på rader med den här typen av transaktioner.

När du har skapat betalningspåminnelser och gjort nödvändiga ändringar kan du antingen skriva ut testrapporter eller skicka ut påminnelserna, vanligtvis som e-post.

## <a name="finance-charges"></a>Räntefakturor
Om en kund inte har betalat på förfallodatumet kan du låta beräkna dröjsmålsränta automatiskt och lägga på den på de förfallna beloppen på kundens konto. Du kan informera kunder om debiterade dröjsmålsräntor genom att skicka räntefakturor.  

> [!NOTE]  
> Du använder räntefakturor för att beräkna dröjsmålsränta och informera dina kunder om dröjsmålsräntor utan att påminna dem om förfallna betalningar. Ett alternativ är att du i stället beräknar ränta på förfallna betalningar när du skapar betalningspåminnelser.  

Du kan manuellt skapa en räntefaktura för en enskild kund och fylla i raderna automatiskt. Som Alternativt kan du använda funktionsjobbet **Skapa räntefakturor** för att skapa räntefakturor för alla eller valda kunder med förfallna betalningar.  

När du skapat räntefakturorna kan du ändra dem. Texten som visas i början och i slutet av räntefakturan bestäms av räntevillkoren och visas i kolumnen **Beskrivning** på raderna. Om ett beräknat belopp har infogats automatiskt i den inledande eller avslutande texten justeras inte texten om du tar bort rader. Då måste du använda funktionen **Uppdatera räntefakturatext**.  

När du har skapat räntefakturor och gjort eventuella ändringar kan du antingen skriva ut testrapporter eller skicka ut räntefakturorna, vanligtvis som e-post.

## <a name="multiple-interest-rates"></a>Flera räntesatser
När du skapar villkor och betalningspåminnelsevillkor för räntefakturor, så kan du för avgiften för försenad betalning ange flera räntesatser så att avgiften beräknas utifrån olika räntesatser under olika perioder. Om det inte finns mer än en räntesats kommer räntesatsen och perioden som anges i fönstren **Räntevillkor** och **Betalningspåminnelsevillkor** för hela beräkningsperioden att användas. Mer information finns i [Så här ställer du in flera räntesatser](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="to-send-the-customer-statement-report"></a>Om du vill skicka kundkontoutdragsrapporten.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kundkontoutdrag** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I **Utdataalternativ** väljer du hur rapporten ska skickas till kunden.

> [!NOTE]  
>   Om du använder flera valutor, skrivs kundkontoutdragsrapporten alltid ut i kundens valuta. Det sista datumet i en rapportperiod används även som meddelandedatumet och åldersfördelningdatumet, om åldern inkluderas.

## <a name="to-set-up-reminder-terms"></a>Så här ställer du in betalningspåminnelsevillkor
Om en betalning förfaller måste du bestämma när och hur betalningspåminnelsen ska skickas till kunden i fråga. Dessutom kanske du vill debitera kundens konto för ränta eller avgifter. Du kan ange valfritt antal villkor för betalningspåminnelser. För varje påminnelsevillkorskod kan du definiera valfritt antal betalningspåminnelsenivåer.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Betalningspåminnelsevillkor** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs.  
3. Om du vill använda fler än en uppsättning villkor, anger du en kod för varje kombination.

## <a name="to-set-up-reminder-levels"></a>Så här ställer du in nivåer för betalningspåminnelser
Första gången en betalningspåminnelse skapas för en kund används inställningen från nivå 1. När betalningspåminnelsen skickas ut registreras nivånumret på betalningspåminnelsetransaktionerna som skapas och kopplas till de enskilda kundreskontratransaktionerna. Om kunden måste påminnas igen kontrolleras alla betalningspåminnelsetransaktioner som är kopplade till öppna kundreskontratransaktioner så att det högsta nivånumret hittas. Villkoren från nästa nivånummer används sedan för den nya betalningspåminnelsen.

Om du skapar fler betalningspåminnelser än du har definierat nivåer för, används villkoren för den högsta nivån. Du kan skapa så många betalningspåminnelser som fältet **Max. antal påminnelser** i betalningspåminnelsevillkoren tillåter.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Betalningspåminnelsevillkor** och välj sedan relaterad länk.  
2. I fönstret **betalningspåminnelsevillkor** och välj raden med de villkor som du vill ange nivåer för och klicka sedan på åtgärden **Nivåer**.  
3. Fyll i fälten om det behövs.  

    För varje betalningspåminnelsenivå kan du ange särskilda villkor, vilka kan inkludera ytterligare avgifter i både BVA och i utländsk valuta. Du kan definiera många räntefaktureringsavgifter i utländsk valuta för respektive kod i fönstret **Betalningspåminnelsevillkor**.
4. Välj åtgärden **Valutor**.
5. I fönstret **Valutor för betalpåm.nivå** kan du definiera för varje betalningspåminnelsekod och motsvarande nivånummer en valutakod och en tilläggsavgift.

    > [!NOTE]  
    > När du skapar räntefakturor i utländsk valuta används de villkor för utländsk valuta som definieras här för att skapa betalningspåminnelser. Om det inte finns några betalningsvillkor definierade för utländsk valuta används de villkor för BVA som angetts i fönstret **Betalningspåminnelsenivåer** och omvandlas till relevant valuta.

    För varje betalningspåminnelsenivå kan du ange text som ska infogas före (**Inledande text**) eller efter (**Avslutande text**) transaktionerna i betalningspåminnelsen.

6. Välj åtgärden **inledande text** eller **avslutande text** och fyll i fönstret **betalningspåminnelsetext**.
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

Om du skriver exempelvis **du är skyldig %9 %7 som förfaller %2.**, innehåller den resulterande betalningspåminnelsen följande text: **du är skyldig 1 200,50 som förfaller 2014-02-02**.

> [!NOTE]
> Förfallodatumet beräknas enligt den formel du anger. Mer information finns i avsnittet "Använda datumformler" i [Ange datumintervall](ui-enter-date-ranges.md).

När du har angett betalningspåminnelsevillkoren (med ytterligare nivåer och text) anger du någon av koderna på vart och ett av kundkorten. Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).

## <a name="to-create-a-reminder-automatically"></a>Så här skapar du en betalningspåminnelse automatiskt
En betalningspåminnelse liknar en faktura. När du skapar en betalningspåminnelse måste ett betalningspåminnelsehuvud och en eller flera betalningspåminnelserader fyllas i. Du kan använda en funktion för att automatiskt skapa betalningspåminnelser för alla kunder.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Betalningspåminnelser** och välj sedan relaterad länk.
2. I fönstret **Betalningspåminnelse** väljer du åtgärden **Skapa betalningspåminnelse**.
3. I fönstret **skapa betalningspåminnelser** fyller du i fälten för att definiera hur och till vem som betalningspåminnelserna skapas.
4. Välj **OK**.

## <a name="to-create-a-reminder-manually"></a>Så här skapar du en betalningspåminnelse manuellt
I fönstret **påminnelse** kan du fylla i snabbfliken **allmännt** manuellt och sedan låta raderna fyllas i automatiskt.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Betalningspåminnelser** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält.
4. Välj åtgärden **Föreslå betalningspåminnelserader**.
5. I batch-jobbet **Föreslå betalningspåminnelserader** fyller du i fälten för att definiera hur och till vem som betalningspåminnelserna skapas.
6. Markera kryssrutan **Inkludera stoppade transaktioner** om du vill att betalningspåminnelserna ska innehålla förfallna öppna transaktioner som är stoppade.

    > [!Important]
    > Öppna transaktioner som är stoppade infogas, oavsett inställningen i kryssrutan Endast transaktioner med förfallna belopp.

7. Välj **OK**.

## <a name="to-replace-reminder-texts"></a>Så här ersätter du betalningspåminnelsetexter  
Du kan bestämma vilken text som ska visas på betalningspåminnelsen på flera olika sätt. I vissa fall kan det hända att du vill ersätta de inledande och avslutande texterna som definierats för den aktuella nivån med texter från en annan nivå.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Betalningspåminnelser** och välj sedan relaterad länk.
2. Öppna relevant påminnelse, och välj sedan åtgärden **Uppdatera bet.påminnelsetext**.
3. I fönstret **Uppdatera bet.påminnelsetext** anger du önskad nicå i fältet **Betalningspåminnelsenivå**.
3. Klicka på **OK** om du vill uppdatera de inledande och avslutande texterna.

## <a name="to-issue-a-reminder"></a>Om du vill utfärda ne betalningspåminnelse
När du har skapat betalningspåminnelser och gjort nödvändiga ändringar kan du antingen skriva ut testrapporter eller skicka ut påminnelserna.

När du skickar ut en betalningspåminnelse överförs informationen till ett separat fönster för utskickade betalningspåminnelser. Samtidigt bokförs betalningspåminnelsetransaktioner. Om ränta eller någon ytterligare avgift har beräknats bokförs transaktioner i kundreskontran och redovisningen.

När en betalningspåminnelse skickas ut, bokförs transaktionerna enligt vad du angett i fönstret **Betalningspåminnelsevillkor**. Denna specifikation bestämmer om ränta och/eller extraavgifter ska bokföras på kundkontot och i redovisningen. Inställningen i fönstret **Kundbokföringsmallar** bestämmer vilka konton som bokförs.

För varje kundreskontratransaktion på räntefakturan skapas en transaktion i fönstret **Bet.påminnelse-/räntetrans**.

Om kryssrutorna **Bokför ränta** eller **Bokför avgift** är markerade i fönstret **Betalningspåminnelsevillkor** skapas även följande transaktioner:

- En transaktion i tabellen **Leverantörsreskontratransaktion**.
- En kundfordringar-transaktion på relevant redovisningskonto
- En "ränte-" och/eller en "avgifts"-transaktion på relevant redovisningskonto

Dessutom kan utskickandet av räntefakturor resultera i momstransaktioner.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Betalningspåminnelser** och välj sedan relaterad länk.
2. Välj relevant betalningspåminnelse och välj sedan åtgärden **Utskick**.
3. I fönstret **Utskick betalningspåminnelser** fyller du i fälten efter behov.
4. Välj **OK**.

Betalningspåminnelsen är avsedd att skickas ut till en angiven e-postadress som en bifogad PDF-fil.

## <a name="to-set-up-finance-charge-terms"></a>Ange räntevillkoren
Du måste upprätta en kod, som representerar respektive beräkningssätt av dröjsmålsränta. Sedan kan du ange den här koden i fältet **Räntevillkorskod** på kundkorten.

Dröjsmålsräntor kan antingen beräknas med metoden genomsnittligt saldo per dag eller metoden förfallet saldo.

* Metod för förfallet saldo

    Räntan innebär helt enkelt en procentandel av det förfallna beloppet:  
    *Metod för förfallet saldo* - *Räntefaktura* = *Förfallet belopp* x *(ränta / 100)*

*   Metod för genomsnittligt saldo per dag

    Hur många dagar som har passerat sedan betalningen förföll beaktas:  
    *Metod för genomsnittligt saldo per dag* - *Räntefaktura* = *Förfallet belopp* x *(antal dagar försenat / ränteperiod)* x *(ränta/100)*

Dessutom är varje kod i tabellen Räntevillkor kopplad till en undertabell, nämligen Räntetext. För respektive uppsättning av räntevillkor kan du definiera en inledande och/eller avslutande text som kan tas med i räntefakturan.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Räntevillkor** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs.  
3. Om du vill använda fler än en uppsättning räntevillkor, anger du en kod för varje kombination.

    För varje räntevillkor kan du ange särskilda villkor, vilka kan inkludera ytterligare avgifter i både BVA och i utländsk valuta. Du kan definiera många räntefaktureringsavgifter i utländsk valuta för respektive kod i fönstret **räntevillkor**.
4. Välj åtgärden **Valutor**.
5. I fönstret **Valutor för räntevillkor** ange för varje villkor en valutakod och en tilläggsavgift.

    > [!NOTE]  
    > När du skapar dröjsmålsränta i utländsk valuta används de villkor som angett här för att skapa räntefakturor. Om det inte finns några sådana villkor definierade används de dröjsmålsräntevillkor för BVA som angetts i fönstret **Räntevillkor** och omvandlas till relevant valuta.

    För varje räntevillkor kan du ange text som ska infogas före (**Inledande text**) eller efter (**Avslutande text**) transaktionerna i räntefakturan.  
6. Välj åtgärden **inledande text** eller **avslutande text** och fyll i fönstret **Räntetext**.
7. Om du vill infoga relaterade värden i den resulterande Räntetext, anger du följande platshållare i **Text**-fältet.

|Platshållare|Värde|  
|-----------------|-----------|  
|%1|Innehållet i fältet **Dokumentdatum** i räntefakturans huvud|  
|%2|Innehållet i fältet **Förfallodatum** i räntefakturans huvud|  
|%3|Innehållet i fältet **Räntesats** på de relaterade räntevillkor|  
|%4|Innehållet i fältet **Återstående belopp** i räntefakturans huvud|  
|%5|Innehållet i fältet **Räntebelopp** i räntefakturans huvud|  
|%6|Innehållet i fältet **Avgift** i räntefakturans huvud|  
|%7|Påminnelsens totalbelopp.|  
|%8|Innehållet i fältet **Valutakod** i räntefakturans huvud|  
|%9|Innehållet i fältet **Bokföringsdatum** i räntefakturans huvud|  

## <a name="to-create-a-finance-charge-memo-manually"></a>Så här skapar du en räntefaktura manuellt  
En räntefaktura påminner om en vanlig faktura. Du kan fylla i ett huvud manuellt och ange att raderna ska fyllas i automatiskt, eller så kan du välja att automatiskt skapa räntefakturor för alla kunder.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Räntefakturor** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten efter behov.  
3. Välj åtgärden **Föreslå räntefakturarader**.
4. I fönstret **Föreslå räntefakturaraderna** anger du ett filter på snabbfliken **Kundreskontratransaktion** om du bara vill skapa räntefakturor för särskilda transaktioner.  
5.  Klicka på **OK** för att starta batchjobbet.  

## <a name="to-update-finance-charge-memo-texts"></a>Så här uppdaterar du räntefakturatexter  
I vissa fall kan det hända att du behöver ändra den inledande och avslutande text som angetts för räntevillkoren. Om du gör detta när du har skapat, men ännu inte skickat ut, räntefakturor kan du uppdatera fakturorna med den ändrade texten.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Räntefaktura** och välj sedan relaterad länk.  
2. Öppna den räntefaktura som du vill ändra texten och välj sedan åtgärden **Uppdatera räntefakturatext**.
3. I fönstret **Uppdatera räntefakturatext** kan du definiera ett filter om du vill uppdatera flera fakturor.
4. Klicka på **OK** om du vill uppdatera de inledande och avslutande texterna.  

## <a name="to-issue-finance-charge-memos"></a>Att utfärda räntefakturor
När du har skapat räntefakturor och gjort eventuella ändringar kan du antingen skriva ut testrapporter eller skicka ut räntefakturorna.

När en betalningspåminnelse skickas ut, bokförs transaktionerna enligt vad du angett i fönstret **Räntevillkor**. Denna specifikation bestämmer om ränta och/eller extraavgifter ska bokföras på kundkontot och i redovisningen. Inställningen i fönstret **Kundbokföringsmallar** bestämmer vilka konton som bokförs.

För varje kundreskontratransaktion på räntefakturan skapas en transaktion i fönstret **Bet.påminnelse-/räntetrans**.

Om kryssrutorna **Bokför ränta** eller **Bokför avgift** är markerade i fönstret **Räntevillkor** skapas även följande transaktioner:

- En transaktion i tabellen **Leverantörsreskontratransaktion**.
- En kundfordringar-transaktion på relevant redovisningskonto
- En "ränte-" och/eller en "avgifts"-transaktion på relevant redovisningskonto

Dessutom kan utskickandet av räntefaktura resultera i momstransaktioner.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Räntefakturor** och välj sedan relaterad länk.
2. Välj relevant faktura och välj sedan åtgärden **Utskick**.
3. I fönstret **Utskick räntefakturor** fyller du i fälten efter behov.
4. Välj **OK**.

Räntefakturan är avsedd att skickas ut till en angiven e-postadress som en bifogad PDF-fil.

## <a name="to-view-reminder-and-finance-charge-entries"></a>Så här visar du betalningspåminnelse- och räntetransaktioner  
När du skickar ut en betalningspåminnelse skapas en betalningspåminnelsetransaktion i fönstret **Bet.påminnelse/räntetrans.** för alla betalningspåminnelserader som innehåller en kundreskontratransaktion. Om du vill kan du visa en översikt över de betalningspåminnelsetransaktioner som skapats för en viss kund.    
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kunder** och välj sedan relaterad länk.  
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Transaktioner**.
3. I fönstret **Kundreskontratransaktioner** markerar du raden med den transaktion som du vill visa betalningspåminnelsetransaktionerna för och väljer sedan åtgärden **Bet.påminnelse-/räntetrans.**.

## <a name="see-also"></a>Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

