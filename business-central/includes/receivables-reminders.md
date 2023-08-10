---
author: edupont04
ms.topic: include
ms.date: 02/09/2022
ms.author: edupont
---
Du kan använda betalningspåminnelser för att påminna kunder om förfallna belopp. Du kan även använda betalningspåminnelser för att beräkna ränta eller avgifter och inkludera dem i betalningspåminnelsen.

Innan du kan skapa betalningspåminnelser måste du ange betalningspåminnelsevillkor och tilldela dem till dina kunder. Mer information finns i [Ange villkor och nivåer för påminnelser](../finance-setup-reminders.md). [!INCLUDE [reminder-terms](reminder-terms.md)] Innehållet på sidan **Räntevillkor** avgör huruvida ränta beräknas på påminnelsen.  

Du kan regelbundet köra batch-jobbet **Skapa betalningspåminnelser** för att skapa betalningspåminnelser för alla kunder med förfallna saldon eller också kan du manuellt skapa en betalningspåminnelse för en specifik kund och sedan låta raderna beräknas och fyllas i automatiskt.  

När du skapat betalningspåminnelserna kan du ändra dem. Texten som visas i början och i slutet av en betalningspåminnelse bestäms av villkoren för betalningspåminnelsenivån och visas i kolumnen **Beskrivning**. Om ett beräknat belopp har infogats automatiskt i den inledande eller avslutande texten justeras inte texten om du tar bort rader. Då måste du använda funktionen **Uppdatera bet.påminnelsetext**.  

För kundreskontratransaktioner med fältet **Stoppad** ifyllt får du inga uppmaningar om att skapa betalningspåminnelser. Men om en betalningspåminnelse skapas med en annan transaktion som bas, kommer en förfallen transaktion som markerats Stoppad också att inkluderas i betalningspåminnelsen. Ränta beräknas inte på rader med den här typen av transaktioner.

När du har skapat betalningspåminnelser och gjort nödvändiga ändringar kan du antingen skriva ut testrapporter eller skicka ut påminnelserna, vanligtvis som e-post.

### <a name="to-create-a-reminder-automatically"></a>Så här skapar du en betalningspåminnelse automatiskt

En betalningspåminnelse liknar en faktura. När du skapar en betalningspåminnelse måste ett betalningspåminnelsehuvud och en eller flera betalningspåminnelserader fyllas i. Du kan använda en funktion för att automatiskt skapa betalningspåminnelser för alla kunder.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 0.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Påminnelser** och väljer sedan relaterad länk.
2. På sidan **Betalningspåminnelse** väljer du åtgärden **Skapa betalningspåminnelse**.
3. På sidan **skapa betalningspåminnelser** fyller du i fälten för att definiera hur och till vem som betalningspåminnelserna skapas.
4. Välj knappen **OK**.

### <a name="to-create-a-reminder-manually"></a>Så här skapar du en betalningspåminnelse manuellt

På sidan **påminnelse** kan du fylla i snabbfliken **allmännt** manuellt och sedan låta raderna fyllas i automatiskt.

1. Välj den ![Glödlampa som öppnar funktionen Berätta igen 2.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Påminnelser** och väljer sedan relaterad länk.
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

1. Välj den ![Glödlampa som öppnar funktionen Berätta ytterligare en gång 3.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Påminnelser** och väljer sedan relaterad länk.
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

1. Välj den ![Glödlampa som öppnar funktionen Berätta även här 4.](../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Påminnelser** och väljer sedan relaterad länk.
2. Välj relevant betalningspåminnelse och välj sedan åtgärden **Utskick**.
3. På sidan **Utskick betalningspåminnelser** fyller du i fälten efter behov.
4. Välj **OK**.

Betalningspåminnelsen är avsedd att skickas ut till en angiven e-postadress som en bifogad PDF-fil.

### <a name="to-cancel-an-issued-reminder"></a>För att annullera en utfärdad betalningspåminnelse.

Om påminnelserna utfärdades felaktigt kan du avbryta dem innan de skickas ut. Det kan du göra antingen av en eller som en batch.

1. På sidan **Utfärdade påminnelser**, välj en eller flera rader för utfärdade betalningspåminnelser som du vill avbryta och välj sedan åtgärden **Avbryt**.
2. På sidan **Annullera utfärdade betalningspåminnelser** fyller du i fälten efter behov och väljer sedan knappen **OK**.


