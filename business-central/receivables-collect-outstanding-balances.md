---
title: Kräva in utestående saldon
description: Lär dig hur du skickar en påminnelse till en kund om en betalning förfaller och lägger till avgifter på grund av förseningen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 81f43ef3f021ef0d348eb14abdffdfda2b3d85fc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758399"
---
# <a name="collect-outstanding-balances"></a>Kräva in utestående saldon

Betalningshanteringen består i att kontrollera om kunderna betalar i tid. Om kunderna har förfallna betalningar, kan du börja med att skicka **kundkontoutdragsrapporten** som betalningspåminnelse. Alternativt kan du skicka betalningspåminnelser.

Du kan använda betalningspåminnelser för att påminna kunder om förfallna belopp. Du kan även använda betalningspåminnelser för att beräkna ränta eller avgifter och inkludera dem i betalningspåminnelsen. Använd räntefakturor om du vill debitera kunder för ränta eller avgifter utan att påminna dem om förfallna belopp.

## <a name="statements"></a>Rapporter

Från kundkortet kan du skapa en rapport med den kundens transaktioner med dig. Sedan skickar du kunden till den genererade PDF-filen. Du kan också använda rapporten **Kundkontoutdrag** för att skicka kunderna en översikt över deras affärer med dig. Kundkontoutdraget kan skickas till Excel för vidare behandling.  

### <a name="to-send-the-customer-statement-report"></a>Om du vill skicka kundkontoutdragsrapporten.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Kundutlåtande** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I **Utdataalternativ** väljer du hur rapporten ska skickas till kunden.

> [!NOTE]
> Om du använder flera valutor, skrivs kundkontoutdragsrapporten alltid ut i kundens valuta. Det sista datumet i en rapportperiod används även som meddelandedatumet och åldersfördelningdatumet, om åldern inkluderas.

## <a name="reminders"></a>Påminnelser

Innan du kan skapa betalningspåminnelser måste du ange betalningspåminnelsevillkor och tilldela dem till dina kunder. Mer information finns i [Ange villkor och nivåer för påminnelser](finance-setup-reminders.md). [!INCLUDE [reminder-terms](includes/reminder-terms.md)] Innehållet på sidan **Räntevillkor** avgör huruvida ränta beräknas på påminnelsen.  

Du kan regelbundet köra batch-jobbet **Skapa betalningspåminnelser** för att skapa betalningspåminnelser för alla kunder med förfallna saldon eller också kan du manuellt skapa en betalningspåminnelse för en specifik kund och sedan låta raderna beräknas och fyllas i automatiskt.  

När du skapat betalningspåminnelserna kan du ändra dem. Texten som visas i början och i slutet av en betalningspåminnelse bestäms av villkoren för betalningspåminnelsenivån och visas i kolumnen **Beskrivning**. Om ett beräknat belopp har infogats automatiskt i den inledande eller avslutande texten justeras inte texten om du tar bort rader. Då måste du använda funktionen **Uppdatera bet.påminnelsetext**.  

För kundreskontratransaktioner med fältet **Stoppad** ifyllt får du inga uppmaningar om att skapa betalningspåminnelser. Men om en betalningspåminnelse skapas med en annan transaktion som bas, kommer en förfallen transaktion som markerats Stoppad också att inkluderas i betalningspåminnelsen. Ränta beräknas inte på rader med den här typen av transaktioner.

När du har skapat betalningspåminnelser och gjort nödvändiga ändringar kan du antingen skriva ut testrapporter eller skicka ut påminnelserna, vanligtvis som e-post.

### <a name="to-create-a-reminder-automatically"></a>Så här skapar du en betalningspåminnelse automatiskt

En betalningspåminnelse liknar en faktura. När du skapar en betalningspåminnelse måste ett betalningspåminnelsehuvud och en eller flera betalningspåminnelserader fyllas i. Du kan använda en funktion för att automatiskt skapa betalningspåminnelser för alla kunder.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Påminnelser** och välj sedan relaterad länk.
2. På sidan **Betalningspåminnelse** väljer du åtgärden **Skapa betalningspåminnelse**.
3. På sidan **skapa betalningspåminnelser** fyller du i fälten för att definiera hur och till vem som betalningspåminnelserna skapas.
4. Välj knappen **OK**.

### <a name="to-create-a-reminder-manually"></a>Så här skapar du en betalningspåminnelse manuellt

På sidan **påminnelse** kan du fylla i snabbfliken **allmännt** manuellt och sedan låta raderna fyllas i automatiskt.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Påminnelser** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält.
4. Välj åtgärden **Föreslå betalningspåminnelserader**.
5. I batch-jobbet **Föreslå betalningspåminnelserader** fyller du i fälten för att definiera hur och till vem som betalningspåminnelserna skapas.
6. Markera kryssrutan **Inkludera stoppade transaktioner** om du vill att betalningspåminnelserna ska innehålla förfallna öppna transaktioner som är stoppade.
7. Markera kryssrutan **Endast transaktioner med förfallna belopp** om du vill att påminnelserna endast ska innehålla förfallna öppna transaktioner. Endast fakturor och betalningar visas som de här transaktionerna för vilka kundens betalningar kan vara försenade.

    > [!Important]
    > Öppna transaktioner som är stoppade infogas, oavsett inställningen i kryssrutan **Endast transaktioner med förfallna belopp**.

8. Välj **OK**.

### <a name="to-replace-reminder-texts"></a>Så här ersätter du betalningspåminnelsetexter

Du kan bestämma vilken text som ska visas på betalningspåminnelsen på flera olika sätt. I vissa fall kan det hända att du vill ersätta de inledande och avslutande texterna som definierats för den aktuella nivån med texter från en annan nivå.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Påminnelser** och välj sedan relaterad länk.
2. Öppna relevant påminnelse, och välj sedan åtgärden **Uppdatera bet.påminnelsetext**.
3. På sidan **Uppdatera bet.påminnelsetext** anger du önskad nicå i fältet **Betalningspåminnelsenivå**.
4. Klicka på **OK** om du vill uppdatera de inledande och avslutande texterna.

### <a name="to-issue-a-reminder"></a>Om du vill utfärda ne betalningspåminnelse

När du har skapat betalningspåminnelser och gjort nödvändiga ändringar kan du antingen skriva ut testrapporter eller skicka ut påminnelserna.

När du skickar ut en betalningspåminnelse överförs informationen till en separat sida för utskickade betalningspåminnelser. Samtidigt bokförs betalningspåminnelsetransaktioner. Om ränta eller någon ytterligare avgift har beräknats bokförs transaktioner i kundreskontran och redovisningen.

När en betalningspåminnelse skickas ut, bokförs transaktionerna enligt vad du angett på sidan **Betalningspåminnelsevillkor**. Denna specifikation bestämmer om ränta och/eller extraavgifter ska bokföras på kundkontot och i redovisningen. Inställningen på sidan **Kundbokföringsmallar** bestämmer vilka konton som bokförs.

För varje kundreskontratransaktion på räntefakturan skapas en transaktion på sidan **Bet.påminnelse/räntetrans.**.

Om kryssrutorna **Bokför ränta** eller **Bokför avgift** är markerade på sidan **Betalningspåminnelsevillkor** skapas även följande transaktioner:

- En transaktion på sidan **Kundreskontratransaktioner**
- En kundfordringar-transaktion på relevant redovisningskonto
- En "ränte-" och/eller en "avgifts"-transaktion på relevant redovisningskonto

Dessutom kan utskickandet av räntefakturor resultera i momstransaktioner.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Påminnelser** och välj sedan relaterad länk.
2. Välj relevant betalningspåminnelse och välj sedan åtgärden **Utskick**.
3. På sidan **Utskick betalningspåminnelser** fyller du i fälten efter behov.
4. Välj **OK**.

Betalningspåminnelsen är avsedd att skickas ut till en angiven e-postadress som en bifogad PDF-fil.

### <a name="to-cancel-an-issued-reminder"></a>För att annullera en utfärdad betalningspåminnelse.

Om påminnelserna utfärdades felaktigt kan du avbryta dem innan de skickas ut. Det kan du göra antingen av en eller som en batch.

1. På sidan **Utfärdade påminnelser**, välj en eller flera rader för utfärdade betalningspåminnelser som du vill avbryta och välj sedan åtgärden **Avbryt**.
2. På sidan **Annullera utfärdade betalningspåminnelser** fyller du i fälten efter behov och väljer sedan knappen **OK**.

## <a name="finance-charges"></a>Räntefakturor

Om en kund inte har betalat på förfallodatumet kan du låta beräkna dröjsmålsränta automatiskt och lägga på den på de förfallna beloppen på kundens konto. Du kan informera kunder om debiterade dröjsmålsräntor genom att skicka räntefakturor.  

> [!NOTE]  
> Du använder räntefakturor för att beräkna dröjsmålsränta och informera dina kunder om dröjsmålsräntor utan att påminna dem om förfallna betalningar. Ett alternativ är att du i stället beräknar ränta på förfallna betalningar när du skapar betalningspåminnelser.  

Innan du kan skapa räntefakturor måste du ange villkoren. Mer information finns i [Konfigurera räntevillkor](finance-setup-finance-charges.md).  

Du kan manuellt skapa en räntefaktura för en enskild kund och fylla i raderna automatiskt. Som Alternativt kan du använda funktionsjobbet **Skapa räntefakturor** för att skapa räntefakturor för alla eller valda kunder med förfallna betalningar.  

När du skapat räntefakturorna kan du ändra dem. Texten som visas i början och i slutet av räntefakturan bestäms av räntevillkoren och visas i kolumnen **Beskrivning** på raderna. Om ett beräknat belopp har infogats automatiskt i den inledande eller avslutande texten justeras inte texten om du tar bort rader. Då måste du använda funktionen **Uppdatera räntefakturatext**.  

När du har skapat räntefakturor och gjort eventuella ändringar kan du antingen skriva ut testrapporter eller skicka ut räntefakturorna, vanligtvis som e-post.

### <a name="to-create-a-finance-charge-memo-manually"></a>Så här skapar du en räntefaktura manuellt

En räntefaktura påminner om en vanlig faktura. Du kan fylla i ett huvud manuellt och ange att raderna ska fyllas i automatiskt, eller så kan du välja att automatiskt skapa räntefakturor för alla kunder.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Räntefakturor** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten efter behov.  
3. Välj åtgärden **Föreslå räntefakturarader**.
4. På sidan **Föreslå räntefakturaraderna** anger du ett filter på snabbfliken **Kundreskontratransaktion** om du bara vill skapa räntefakturor för särskilda transaktioner.

    > [!NOTE]
    > Även om de visas får filtren **Betalning** och **Kreditnot** som **Dokumenttyp** ingen effekt eftersom funktionen **Föreslå räntefakturaraderna** endast hanterar positiva belopp.
5.  Klicka på **OK** för att starta batchjobbet.  

### <a name="to-update-finance-charge-memo-texts"></a>Så här uppdaterar du räntefakturatexter  
I vissa fall kan det hända att du behöver ändra den inledande och avslutande text som angetts för räntevillkoren. Om du gör detta när du har skapat, men ännu inte skickat ut, räntefakturor kan du uppdatera fakturorna med den ändrade texten.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Räntefaktura** och välj sedan relaterad länk.  
2. Öppna den räntefaktura som du vill ändra texten och välj sedan åtgärden **Uppdatera räntefakturatext**.
3. På sidan **Uppdatera räntefakturatext** kan du definiera ett filter om du vill uppdatera flera fakturor.
4. Klicka på **OK** om du vill uppdatera de inledande och avslutande texterna.  

### <a name="to-issue-finance-charge-memos"></a>Att utfärda räntefakturor
När du har skapat räntefakturor och gjort eventuella ändringar kan du antingen skriva ut testrapporter eller skicka ut räntefakturorna.

När en betalningspåminnelse skickas ut, bokförs transaktionerna enligt vad du angett på sidan **Räntevillkor**. Denna specifikation bestämmer om ränta och/eller extraavgifter ska bokföras på kundkontot och i redovisningen. Inställningen på sidan **Kundbokföringsmallar** bestämmer vilka konton som bokförs.

För varje kundreskontratransaktion på räntefakturan skapas en transaktion på sidan **Bet.påminnelse/räntetrans.**.

Om kryssrutorna **Bokför ränta** eller **Bokför avgift** är markerade på sidan **Räntevillkor** skapas även följande transaktioner:

- En transaktion på sidan **Leverantörsreskontratransaktion**.
- En kundfordringar-transaktion på relevant redovisningskonto
- En "ränte-" och/eller en "avgifts"-transaktion på relevant redovisningskonto

Dessutom kan utskickandet av räntefaktura resultera i momstransaktioner.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Räntefakturor** och välj sedan relaterad länk.
2. Välj relevant faktura och välj sedan åtgärden **Utskick**.
3. På sidan **Utskick räntefakturor** fyller du i fälten efter behov.
4. Välj **OK**.

Räntefakturan är avsedd att skickas ut till en angiven e-postadress som en bifogad PDF-fil.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>För att annullera utfärdad räntefaktura.
Om räntefakturor utfärdades felaktigt kan du avbryta dem innan de skickas ut. Det kan du göra antingen av en eller som en batch.
1. På sidan **Utfärdade räntefakturor**, välj en eller flera rader för utfärdade räntefakturor som du vill avbryta och välj sedan åtgärden **Avbryt**.
2. På sidan **Annullera utfärdade räntefakturor** fyller du i fälten efter behov och väljer sedan knappen **OK**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Så här visar du betalningspåminnelse- och räntetransaktioner  
När du skickar ut en betalningspåminnelse skapas en betalningspåminnelsetransaktion på sidan **Bet.påminnelse/räntetrans.** för alla betalningspåminnelserader som innehåller en kundreskontratransaktion. Om du vill kan du visa en översikt över de betalningspåminnelsetransaktioner som skapats för en viss kund.    
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.  
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Transaktioner**.
3. På sidan **Kundreskontratransaktioner** markerar du raden med den transaktion som du vill visa betalningspåminnelsetransaktionerna för och väljer sedan åtgärden **Bet.påminnelse-/räntetrans.**.

## <a name="multiple-interest-rates"></a>Flera räntesatser

När du skapar villkor och betalningspåminnelsevillkor för räntefakturor, så kan du för avgiften för försenad betalning ange flera räntesatser så att avgiften beräknas utifrån olika räntesatser under olika perioder. Om det inte finns mer än en räntesats kommer räntesatsen och perioden som anges på sidorna **Räntevillkor** och **Betalningspåminnelsevillkor** för hela beräkningsperioden att användas. Mer information finns i [Så här ställer du in flera räntesatser](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Konfigurera påminnelsevillkor och nivåer](finance-setup-reminders.md)  
[Konfigurera räntevillkor](finance-setup-finance-charges.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
