---
title: Använda tidrapporter
description: Lär dig hur du skapar tidrapporter och skickar in dem för godkännande.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 07/27/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="use-time-sheets"></a>Använda tidrapporter

Använd tidrapporter för att spåra frånvaro, samt för att spåra tid och resurser som ägnas åt ett projekt. Med tidsspårning kan du identifiera problem tidigt och undvika fördröjningar eller överskridna kostnader. Med tidrapporter kan en resurs enkelt rapportera tidsförbrukning för en enskild anställd eller en maskin, så att cheferna enkelt kan granska förbrukningen och dess fördelning. I den här artikeln beskrivs hur du arbetar med tidrapporter.  

Du kan kopiera och använda dina projektplaneringsrader i en tidrapport. På så sätt får du bara ange informationen på ett ställe och radinformationen är alltid korrekt. För mer information, gå till [Så här kopierar du projektplaneringsrader till en tidrapport](#copy-job-planning-lines-to-a-time-sheet).

När du har godkänt tidrapportsposter för ett projekt, kan du bokföra dem i den aktuella projektjournalen eller resursjournalen. Mer information finns i [Så här bokför du tidrapportrader i en projektjournal](#to-post-time-sheet-lines-in-a-job-journal) och [Så här bokför du tidrapportrader i en resursjournal](#post-time-sheet-lines-in-a-resource-journal).

Innan du kan använda tidrapporter måste du ställa in allmän information och ange en administratör och en eller flera godkännare av tidrapporter. Om du vill ha mer information om hur du konfigurerar tidrapporter går du till [Konfigurera tidrapporter](projects-how-setup-time-sheets.md).  

> [!TIP]
> Du kan använda tidrapporter på en mobil enhet. För att göra detta kan du behöva aktivera växlingsknappen **Använd ny tidrapport** på sidan [Resursinställningar](https://businesscentral.dynamics.com/?page=462).

## <a name="create-time-sheets"></a>Skapa tidrapporter

Du kan använda sidan **Skapa tidsrapporter** för att skapa tidrapporter för ett angivet antal tidperioder eller veckor. Sedan kan tidrapportsägaren öppna den och registrera tid som har spenderats på en aktivitet. Du kan också [schemalägga batchprojektet så att det körs automatiskt](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Du måste ha behörighet för att kunna skapa tidrapporter. Om du vill veta mer om behörigheter går du till [Konfigurera tidrapporter](projects-how-setup-time-sheets.md).

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Skapa tidrapporter** och väljer sedan relaterad länk.

    > [!TIP]
    > Du kan också använda åtgärden **Skapa tidrapporter** på listsidan **Resurser** och sidan **Resurskort**.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Innan du skapar tidrapporter för en resurs kontrollerar du att fälten **Använd tidrapport** och **Användar-ID för tidrapportsägare** har angetts för dem på sidan **Resurskort**.

    Du kan också välja åtgärden **Schemalägg** för att ange hur ofta du vill att uppgiften ska köras automatiskt. Om du t.ex. vill konfigurera uppgiften så att den körs varje vecka i fyra veckor går du till sidan **Schemalägg en rapport – skapa tidrapporter** och ställer in fältet **Formel för nästa körningsdatum** på **4W**. Om du vill veta mer om hur du schemalägger rapporter går du till [Schemaläggning av en rapport som ska köras](ui-work-report.md#ScheduleReport)  

På sidan **Tidrapporter** kan du visa tidrapporter som du har skapat. Varje tidrapport består av en eller flera rader som definierar den tid som du vill skicka för godkännande. I följande tabell beskrivs de typer av rader som du kan lägga till i tidrapporten.

| **Fält** | **Beskrivning** |
|---|---|
| | Används för att lägga till en notering eller markör i fältet **Beskrivning** på tidrapportraden. Du kan t.ex använda fältet för att kategorisera tidrapportposter. Om du lämnar fältet **Typ** för en tidrapportrad tomt kan du inte ange tidsvärden i veckodagsfälten för den raden. |
| Frånvaro | Används för att registrera den tid då du är frånvarande under en arbetsvecka. Om du vill slutföra informationen för raden anger du frånvarotypen i fältet **Frånvaroorsak**. |
| Monteringsorder | Används för att registrera tid för monteringsorder. En tidrapportrad av den här typen skapas vid bokföring av monteringsorderrader där resursen konfigurerats att använda tidrapporter. Du kan inte manuellt välja en rad av den här typen. |
| Projekt | Används för att registrera användning för ett projekt. För att slutföra informationen för raden anger du det projektnummer och det projektaktivitetsnummer som du vill registrera tiden för. Du kan registrera tid för rader som inte har schemalagts.|
| Resurs | Används för att registrera tidsförbrukning för en resurs. Ange en beskrivning av arbetet för att slutföra informationen för raden. |
| Service | Används om du vill registrera tidsförbrukning för en serviceorder eller en servicekreditnota. |

Du vill till exempel skicka en tidrapport för en vecka där du utförde städuppgifter och hade en ledig dag för ett läkarbesök. I följande tabell visas hur du lägger till rader i tidrapporten.

| Kontakttyp | Description | Arbetstypkod | Kod för arbetstyp |
|--|--|--|--|
| Resurs | Arbetstider | Städning och renhållning |  |
| Frånvaro | Ledig tid |  | Hälsotillstånd |
|  | Jag var tvungen att ta tisdagen ledig på grund av ett läkarbesök. |  |  |

I detta hypotetiska exempel ska du registrera relevanta timmar under aktuella dagar i fälten för respektive veckodag.  

> [!TIP]
> I de flesta fall har företaget fördefinierade arbetstyper för olika typer av rader. I dessa fall väljer du önskad arbetstyp i listan och lägger sedan till en egen beskrivning.  
>
> Välj arbetstyp genom att välja knappen :::image type="icon" source="media/assist-edit-icon.png" border="false"::: i fältet **Beskrivning**, genom att välja åtgärden **Aktivitetsdetaljer** och sedan ange typen på den sida som öppnas, eller genom att välja den i fältet **Kod för arbetstyp** eller fältet **Kod för frånvarotyp**. I det här fallet kan du ignorera avsnittet [För att definiera arbetstyper och lägga till en i en tidrapport](#define-work-types-and-add-one-to-a-time-sheet).  

## <a name="reuse-time-sheet-lines-in-other-time-sheets"></a>Återanvänd tidrapportrader i andra tidrapporter

Om din tidrapportsinformation är samma från tidsperiod till tidsperiod kan du spara tid genom att kopiera raderna från den föregående perioden. Sedan kan du ange bara din tidförbrukning för den nya perioden.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tidrapporter** och väljer sedan relaterad länk.  
2. Öppna tidrapporten för en period senare än perioden för en befintlig tidrapport med rader.  
3. Välj åtgärden **Kopiera rader från föregående tidrapport**.

Raderna kopieras med uppgifter som till exempel typ och beskrivning. Till exempel om raden är relaterad till ett projekt, kopieras **Projektnr** . Alla kopierade rader har statusen **Öppen**. Du kan nu ändra raderna efter behov.

## <a name="copy-job-planning-lines-to-a-time-sheet"></a>Kopiera projektplaneringsrader till en tidrapport

Nedan beskrivs hur du skapar snabbt lägger till projektplaneringsrader i en tidrapport.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ikonen, ange **Tidrapporter** och välj sedan relaterad länk.  
2. På sidan **Tidrapporter** väljer du en tidrapport för relevant tidsperiod.  
3. Välj åtgärden **Skapa rader från projektplanering**. Vissa projektplaneringsrader i tidrapporttidsperioden kopieras till tidrapporten för den personen eller maskinen i fältet **Resursnr.** på tidrapporten.

## <a name="define-work-types-and-add-one-to-a-time-sheet"></a>Definiera arbetstyper och lägg till en i en tidrapport

Du kan definiera arbetstyp för alla tidrapportrader för serviceorder, projektorder och resurser. På detta sätt kan du lägga till information som du behöver för att fakturera kunden för olika typer av arbete.  

1. På sidan **Tidrapporter** väljer du relevant tidrapport.
2. På den första raden i avsnittet **Rader** väljer du fältet **Typ** och sedan relevant typ, exempelvis *Resurs*.  
3. Välj fältet **Beskrivning** och fyll sedan i fälten på sidan **Resursinformation på rad i tidrapport**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Om inga arbetstyper finns väljer du åtgärden **Ny**.
    2. På sidan **Arbetstyper** fyller du i erforderliga fält och återvänder sedan till tidrapporten.
4. Det är frivilligt att fylla i resten av tidrapporten. Mer information finns i avsnittet [För att fylla i tidrapportrader och skicka för godkännande](#fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Liknande åtgärder gäller för att definiera frånvarokoder.

## <a name="fill-in-time-sheet-lines-and-submit-for-approval"></a>Fyll i tidrapportrader och skicka in för godkännande

Tidrapportsregistrering spåras i timmar, som är standardbasmåttenheten för resurser. Som standard visar en tidrapport vanliga arbetsdagar, från måndag till fredag.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tidrapporter** och väljer sedan relaterad länk.  
2. Välj en tidrapport för aktuell period.
3. Fyll i fälten på en rad efter behov. Ange numret på timmar som används av resursen på respektive veckodag.  

    I de flesta fall kan du lägga till en rad av typen *Resurs* och sedan registrera antalet spenderade timmar per dag. Om du vill registrera frånvaro lägger du till en rad av typen *Frånvaro*.  

    > [!TIP]  
    > Du kan granska summan av tidrapportstimmar som du har angett i faktaboxen **Översikt över utfall/budgeterat**.  
4. Upprepa steg 3 för andra arbetstyper som resursen utför.  

    Du bestämmer sedan om du vill skicka alla rader eller markerade rader i tidrapporten.  

    * Om du vill skicka tidrapporten för en eller flera rader väljer du önskad rad och sedan åtgärden **Skicka**.

        Välj alternativet **Endast valda rader** på sidan där du skickar. Radens status ändras från **Öppen** till **Skickad**.
    * Om du vill skicka tidrapporten för alla öppna rader väljer du åtgärden **Skicka** högst upp på sidan **Tidrapport**.  

        Bekräfta att du vill skicka alla öppna rader i den aktuella tidrapporten.  

    > [!NOTE]  
    > Du kan endast skicka tidrapportrader som du har angett tid för.  
5. För att ändra informationen på en rad som har angetts som **Skickad** väljer du raden och väljer sedan åtgärden **Öppna igen**.

    > [!NOTE]  
    > En chef kan komma att avvisa en tidrapportrad som skickas in för godkännande. Om en rad har status **Avvisad** kan du göra ändringar av raden och sedan välja **Skicka** igen.  
6. Välj **OK**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Så här kan du godkänna eller avvisa en tidrapport

En tidrapport måste skickas för godkännande innan den kan användas. Du kan godkänna och avvisa enskilda rader i en tidrapport eller skicka tillbaka dem till avsändaren. Du kan godkänna en tidrapport på två sätt:

* En tidrapportsadministratör kan godkänna alla tidrapporter.
* Personen som anges i fältet **Användar-ID för tidrapportens godkännare** på resurskortet kan godkänna resursens tidrapporter. Om du vill ha mer information om hur du konfigurerar godkännanden går du till [Konfigurera tidrapporter](projects-how-setup-time-sheets.md).

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Tidrapporter för chef** och väljer sedan relaterad länk.
2. Välj en tidrapport från listan.  
3. På sidan **Tidrapport**: 
    1. Välj åtgärden **Bearbeta** och välj sedan åtgärden **Godkänn**.
    2. Välj åtgärden **Alla skickade rader** för att godkänna alla rader eller åtgärden **Enbart valda rader** för att endast godkänna de rader som har valts på sidan **Tidrapport**.
4. Välj knappen **OK**.  
5. Välj alternativt åtgärden **Avvisa** och följ steg 4 till 5.  

> [!TIP]  
> Använd faktaboxarna **Tidrapportsstatus** och **Faktisk/schemalagd översikt** för att få översikt över tidrapportsinformation.

När du har godkänt eller avvisat en tidrapport kan den inte ändras om den inte först öppnas igen. Följande procedur förklarar hur du öppna en godkänd eller avvisad tidrapport igen.

## <a name="reopen-a-time-sheet"></a>Öppna en tidrapport på nytt

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Tidrapporter för chef** eller **Tidrapporter** och väljer sedan relaterad länk.
2. Öppna en tidrapport från listan.  

    > [!NOTE]  
    > Du kan endast öppna rader igen som har statusen **Godkänd**. Du kan inte öppna rader på nytt som har statusen **Avvisad** eller som har bokförts.  
3. På sidan **Tidrapport** väljer du åtgärden **Öppna igen** och väljer sedan åtgärden **Alla inskickade rader** för att öppna alla rader igen, eller åtgärden **Enbart valda rader** för att endast öppna de rader igen som valts på sidan **Tidrapport**.
4. Välj knappen **OK**. Statusen för tidrapportraden eller raderna ändras till **Skickat**.  

## <a name="view-and-approve-time-sheets-by-job"></a>Visa och godkänn tidrapporter per projekt

För ett projekt kan du ange en person som är ansvarig för projektet. Denna informationen är kopplad till tidrapportrader. Länken ger projektledarna en lista över de tidrapporter som ska godkännas. Teamprojektledaren kan till exempel vara ansvarig för vissa projekt i företaget. I så fall bör ledaren utses till **Ansvarig person** på projektkortssidan. Denna vy över tidrapportsinformation visar projektuppgifterna som är kopplade till ett projekt och antalet använda timmar.

> [!NOTE]
> För att kunna godkänna tidrapporter på sidan **Tidrapport för chef efter projekt** måste du först markera ett alternativ för **Tidrapport per projektgodkännande** i fönstret **Resursinställning**. Om du vill ha mer information om hur du konfigurerar godkännanden för resurser går du till [Skapa resurser](projects-how-setup-resources.md).

### <a name="approve-or-reject-a-time-sheet-by-job"></a>Godkänn eller avvisa en tidrapport per projekt

1. I rutan **Sök**, ange **Tidrapporter för chef efter projekt** och välj sedan relaterad länk. [!INCLUDE[prod_short](includes/prod_short.md)] visar en lista över tidrapportrader som är kopplade till de projekt som du har ansvar för.
2. Välj åtgärden **Godkänn** och välj sedan åtgärden **Alla skickade rader** för att godkänna alla rader eller åtgärden **Enbart valda rader** för att endast godkänna de rader som har valts på sidan **Tidrapport**.

    > [!NOTE]
    > Du kan endast godkänna tidrapporter som har statusen **Skickad**.

3. Om du vill lämna ytterligare information om godkännandet eller avslaget väljer du åtgärden **Relaterat**, därefter **Kommentarer** och sedan **Radkommentarer**.
4. Välj **OK**.

> [!NOTE]
> När du godkänner eller avvisar en tidrapportrad efter projekt kan du inte öppna den på nytt eller ändra den på sidan **Tidrapport**.

## <a name="post-time-sheet-lines-in-a-resource-journal"></a>Bokför tidrapportrader i en resursjournal

När du har godkänt tidrapportsposter för en resurs, kan du bokföra dem i den aktuella resursjournalen.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Resursjournaler** och väljer sedan relaterad länk.  
2. Välj åtgärden **Föreslå rader från tidrapporter**.  
3. På sidan **Föreslå resursjournalrader** fyller du i fälten efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Välj **OK**. Transaktioner för förbrukning skapas i resursjournalen, där du kan ändra informationen efter behov.  
5. Välj åtgärden **Bokföra**.  
6. Om du vill bekräfta bokföringen väljer du åtgärden **Transaktioner**. Sidan **Resurstransaktioner** öppnas och visar resultatet av att bokföra resursjournalen.

## <a name="post-time-sheet-lines-in-a-job-journal"></a>Bokföra tidrapportrader i en projektjournal

När du har godkänt tidrapportsposter för ett projekt, kan du bokföra dem i den aktuella projektjournalen.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Jobbjournaler** och väljer sedan relaterad länk.  
2. Välj åtgärden **Föreslå rader från tidrapporter**.  
3. På sidan **Föreslå projektjournalrader** fyller du i fälten efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Välj **OK**. Transaktioner för förbrukning skapas i projektjournalen, där du kan ändra informationen efter behov.  

    > [!NOTE]  
    > Information om arbetstyp och om arbetet är debiterbart kopieras från tidrapportraden. Om det behövs, kan du minska antalet timmar och skapa en delvis bokföring. Om du minskar antalet kommer raden att innehålla det återstående antalet timmar nästa gång du väljer åtgärden **Föreslå rader från tidrapporter**.  
5. Välj åtgärden **Bokföra**.  
6. Om du vill bekräfta bokföringen väljer du åtgärden **Transaktioner**. Sidan **Projekttransaktioner** öppnas och visar resultatet av att bokföra resursjournalen.

## <a name="to-archive-time-sheets"></a>Så här arkiverar du tidrapporter

När du bokför tidrapporter kan du arkivera dem för framtida referens. Du måste bokföra alla rader i en tidrapport innan du kan arkivera den.

> [!NOTE]  
> När du arkiverar en tidrapport tas den bort från listan både på sidan **Tidrapport** och sidan **Tidrapport för chef**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ikonen, ange **Tidrapporter** och välj sedan relaterad länk.
2. Välj åtgärden **Flytta tidrapporter till arkiv**.  
3. På sidan **Flytta tidrapporter till arkiv** fyller du i fälten efter behov och väljer sedan knappen **OK**.  
4. För att granska arkiverade tidrapporter, välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Tidrapportsarkiv** eller **Tidrapportsarkiv för chef** och väljer sedan relaterad länk.

## <a name="see-also"></a>Se även

[Projekthantering](projects-manage-projects.md)  
[Ställa in projekthantering](projects-setup-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
