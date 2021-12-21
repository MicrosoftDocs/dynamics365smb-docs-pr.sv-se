---
title: Använd tidrapporter
description: Beskriver hur du skapar en tidrapport, definierar arbetstyper, fyller i tidrapporten och skickar den för godkännande.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheets
ms.search.form: 973
ms.date: 12/13/2021
ms.author: edupont
ms.openlocfilehash: a5fdd86d63fa19a0a7f473d58abf34242e4e5cd5
ms.sourcegitcommit: 41876b559872fe7adbfa5b59a6e1a71dc907fb15
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920909"
---
# <a name="use-time-sheets"></a>Använd tidrapporter

Du kan använda tidrapporter i [!INCLUDE [prod_short](includes/prod_short.md)] för att spåra frånvaro samt för att spåra tid och resurser som ägnas åt ett projekt. Med tidshantering kan du identifiera problem tidigt och undvika fördröjningar eller överskridna kostnader. Med tidrapporter kan en resurs enkelt rapportera tidsförbrukning för en enskild anställd eller en maskin, och en chef kan enkelt granska förbrukningen och dess fördelning. Denna artikel beskriver hur du skapar en tidrapport, definierar arbetstyper, fyller i tidrapporten och skickar den för godkännande.  

Du kan kopiera och använda dina projektplaneringsrader i en tidrapport. På så sätt får du bara ange informationen på ett ställe och radinformationen är alltid korrekt.

När du har godkänt tidrapportsposter för ett projekt, kan du bokföra dem i den aktuella projektjournalen eller resursjournalen.

Innan du kan använda tidrapporter måste du ställa in allmän information och ange en administratör och en eller flera godkännare av tidrapporter. Mer information finns i [Skapa tidrapporter](projects-how-setup-time-sheets.md).  

> [!TIP]
> Från och med 2021 utgivningscykel 2 kan du hantera tilldelade tidsrapporter på en mobil enhet. Administratören måste emellertid kanske aktivera **funktionsuppdateringen: ny tidrapport** på sidan [funktionshantering](https://businesscentral.dynamics.com/?page=2610) om du vill använda den här funktionen. Mer information finns i [Skapa tidrapporter](projects-how-setup-time-sheets.md).

## <a name="to-create-time-sheets"></a>Så här skapar du tidrapporter

Du kan använda batch-jobbet **Skapa tidsrapporter** för att skapa tidrapporter för ett angivet antal perioder eller veckor. Sedan kan tidrapportsägaren öppna den och registrera tid som har spenderats på en aktivitet.  

> [!IMPORTANT]
> Du måste ha behörighet för att kunna skapa tidrapporter.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tidrapporter** och väljer sedan relaterad länk.
2. På sidan **Tidrapporter** väljer du åtgärden **Skapa tidrapporter**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Fälten **Andvänd tidrapport** och **Användar-ID för tidrapportens ägare** måste fyllas i på kortet för resursen på tidrapporten.
4. Välj knappen **OK**.  

På sidan **Tidrapporter** kan du visa tidrapporter som du har skapat. Varje tidrapport består av en eller flera rader som definierar den tid som du vill skicka för godkännande. I följande tabell beskrivs de typer av rader som du kan lägga till i tidrapporten.

| **Fält** | **Beskrivning** |
|---|---|
| | Används för att lägga till en notering eller markör i fältet **Beskrivning** på tidrapportraden. Du kan t.ex använda fältet för att kategorisera tidrapportposter. Om du lämnar fältet **Typ** för en tidrapportrad tomt kan du inte ange tidsvärden i veckodagsfälten för den raden. |
| Frånvaro | Används för att registrera tid då du är frånvarande under en arbetsvecka. Om du vill slutföra informationen för raden anger du frånvarotypen i fältet **Frånvaroorsak**. |
| Monteringsorder | Används för att registrera tid för monteringsorder. En tidrapportrad av den här typen skapas vid bokföring av monteringsorderrader där resursen konfigurerats att använda tidrapporter. Du kan inte manuellt välja en rad av den här typen. |
| Projekt | Används för att registrera användning för ett projekt. För att slutföra informationen för raden anger du det projektnummer och det projektaktivitetsnummer som du vill registrera tiden för. Du kan registrera tid för rader som inte har schemalagts.|
| Resurs | Används för att registrera tidsförbrukning för en resurs. Ange en beskrivning av arbetet för att slutföra informationen för raden. |
| Service | Används om du vill registrera tidsförbrukning för en serviceorder eller en servicekreditnota. |

Om du t. ex. vill skicka en tidrapport för en arbetsvecka där du arbetat med rengöringsuppgifter merparten av dagarna men hade en dag ledigt på grund av läkarbesök, lägger du till rader enligt tabellen nedan.

| Typ | Beskrivning | Arbetstypkod | Kod för arbetstyp |
|--|--|--|--|
| Resurs | Arbetstider | Städning och renhållning |  |
| Frånvaro | Ledig tid |  | Hälsa |
|  | Jag var tvungen att ta tisdagen ledig på grund av ett läkarbesök. |  |  |

I detta hypotetiska exempel ska du registrera relevanta timmar under aktuella dagar i fälten för respektive veckodag.  

> [!TIP]
> I de flesta fall har företaget fördefinierade arbetstyper för olika typer av rader. I dessa fall väljer du önskad arbetstyp i listan och lägger sedan till en egen beskrivning.  
>
> Välj arbetstyp genom att välja knappen :::image type="icon" source="media/assist-edit-icon.png" border="false"::: i fältet **Beskrivning**, genom att välja åtgärden **Aktivitetsdetaljer** och sedan ange typen på den sida som öppnas, eller genom att välja den i fältet **Kod för arbetstyp** eller fältet **Kod för frånvarotyp**. I det här fallet kan du ignorera avsnittet [För att definiera arbetstyper och lägga till en i en tidrapport](#to-define-work-types-and-add-one-to-a-time-sheet).  

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Så här kan du återanvända tidrapportsrader i andra tidrapporter

Om din tidrapportsinformation är samma från tidsperiod till tidsperiod kan du spara tid genom att kopiera raderna från den föregående perioden. Sedan kan du ange bara din tidförbrukning för den nya perioden.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tidrapporter** och väljer sedan relaterad länk.  
2. Öppna tidrapporten för en period senare än perioden för en befintlig tidrapport med rader.  
3. Välj åtgärden **Kopiera rader från föregående tidrapport**.

Raderna kopieras med uppgifter som till exempel typ och beskrivning. Till exempel om raden är relaterad till ett projekt, kopieras **Projektnr** . Alla kopierade rader har statusen **Öppen**. Du kan nu ändra raderna efter behov.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Så här kan du kopiera projektplaneringsrader till en tidrapport
Nedan beskrivs hur du skapar snabbt lägger till projektplaneringsrader i en tidrapport.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ikonen, ange **Tidrapporter** och välj sedan relaterad länk.  
2. På sidan **Tidrapporter** väljer du en tidrapport för relevant tidsperiod.  
3. Välj åtgärden **Skapa rader från projektplanering**. Vissa projektplaneringsrader i tidrapporttidsperioden kopieras till tidrapporten för den personen eller maskinen i fältet **Resursnr.** på tidrapporten.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Om du vill definiera arbetstyper och lägga till en till en tidrapport

Du kan definiera arbetstyp för alla tidrapportsrader för serviceorder, projektorder och resurser. På detta sätt kan du lägga till information som du behöver för att fakturera kunden för olika typer av arbete.  

1. På sidan **Tidrapporter** väljer du relevant tidrapport.
2. På den första raden i avsnittet **Rader** väljer du fältet **Typ** och sedan relevant typ, exempelvis *Resurs*.  
3. Välj fältet **Beskrivning** och fyll sedan i fälten på sidan **Resursinformation på rad i tidrapport**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Om inga arbetstyper finns, väljer du åtgärden **Ny**.
    2. På sidan **Arbetstyper** fyller du i erforderliga fält och återvänder sedan till tidrapporten.
4. Det är frivilligt att fylla i resten av tidrapporten. Mer information finns i avsnittet [För att fylla i tidrapportrader och skicka för godkännande](#to-fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Liknande åtgärder gäller för att definiera frånvarokoder.

## <a name="to-fill-in-time-sheet-lines-and-submit-for-approval"></a>Fylla i tidrapportrader och skicka för godkännande

Tidrapportsregistrering spåras i timmar, som är standardbasmåttenheten för resurser. Som standard visar en tidrapport vanliga arbetsdagar, från måndag till fredag.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tidrapporter** och väljer sedan relaterad länk.  
2. Välj en tidrapport för aktuell period.
3. Fyll i fälten på en rad efter behov. Ange numret på timmar som används av resursen på respektive veckodag.  

    I de flesta fall kan du lägga till en rad av typen *Resurs* och sedan registrera antalet spenderade timmar per dag. Om du vill registrera frånvaro lägger du till en rad av typen *Frånvaro*.  

    > [!TIP]  
    > Du kan granska summan av tidrapportstimmar som du har angett i faktaboxen **Översikt över utfall/budgeterat**.  
4. Upprepa steg 3 för andra arbetstyper som resursen utför.  

    Härnäst måste du bestämma om du vill skicka alla rader i tidrapporten eller om du vill skicka enskilda rader.  

    * Om du vill skicka tidrapporten för en eller flera rader väljer du önskad rad och sedan åtgärden **Skicka**.

        Välj alternativet **Endast valda rader** på sidan där du skickar. Radens status ändras från *Öppen* till *Skickad*.
    * Om du vill skicka tidrapporten för alla öppna rader väljer du åtgärden **Skicka** högst upp på sidan **Tidrapport**.  

        Du ombeds bekräfta att du vill skicka alla öppna rader i den aktuella tidrapporten.  

    > [!NOTE]  
    > Du kan endast skicka tidrapportrader som du har angett tid för.  
5. För att ändra informationen på en rad som har angetts som **Skickad** väljer du raden och väljer sedan åtgärden **Öppna igen**.

    > [!NOTE]  
    >   En chef kan avvisa en tidrapportrad som skickas in för godkännande. Om en rad har status **Avvisad** kan du göra ändringar av raden och sedan välja **Skicka** igen.  
6. Välj **OK**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Så här kan du godkänna eller avvisa en tidrapport
En tidrapport måste skickas för godkännande innan den kan användas. Du kan godkänna och avvisa enskilda rader i en tidrapport eller skicka tillbaka dem till avsändaren för ytterligare åtgärd. En tidrapport kan godkännas på två sätt:

* En tidrapportsadministratör kan godkänna alla tidrapporter.
* Personen som anges i fältet **Användar-ID för tidrapportens godkännare** på resurskortet kan godkänna resursens tidrapporter. Mer information finns i [Skapa tidrapporter](projects-how-setup-time-sheets.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Tidrapporter för chef** och väljer sedan relaterad länk.
2. Välj en tidrapport från listan.  
3. På sidan **Tidrapport**, 
    1. Välj åtgärden **Bearbeta** och välj sedan åtgärden **Godkänn**.
    2. Välj åtgärden **Alla skickade rader** för att godkänna alla rader eller åtgärden **Enbart valda rader** för att endast godkänna de rader som har valts på sidan **Tidrapport**.
4. Välj knappen **OK**.  
5. Välj alternativt åtgärden **Avvisa** och följ steg 4 till 5.  

> [!TIP]  
>   Använd faktaboxarna **Tidrapportsstatus** och **Faktisk/schemalagd översikt** för att få översikt över tidrapportsinformation.

När du har godkänt eller avvisat en tidrapport kan den inte ändras om den inte först öppnas igen. Följande procedur förklarar hur du öppna en godkänd eller avvisad tidrapport igen.

## <a name="to-reopen-a-time-sheet"></a>Öppna en tidrapport igen
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Tidrapporter för chef** eller **Tidrapporter** och väljer sedan relaterad länk.
2. Öppna en tidrapport från listan.  

    > [!NOTE]  
    >   Du kan endast öppna rader igen som har statusen **Godkänd**. Du kan inte öppna rader igen som har statusen **Avvisad**. Du kan inte öppna en tidrapport igen om den har bokförts.  
3. På sidan **Tidsrapport** väljer du åtgärden **Öppna igen** och väljer sedan åtgärden **Alla skickade rader** för att öppna alla rader igen eller åtgärden **Enbart valda rader** för att endast öppna de rader igen som valts på sidan **Tidrapport**.
4. Välj knappen **OK**. Statusen för tidrapportraden eller raderna ändras till **Skickat**.  

## <a name="to-view-and-approve-time-sheets-by-job"></a>Visa och godkänna tidrapporter per projekt

För ett projekt kan du ange en person som är ansvarig för projektet. Denna information är kopplad till tidrapportsrader och kan användas för att generera en lista över tidrapporter som en projektledare behöver granska och godkänna. Till exempel teamprojektledaren kan vara ansvarig för vissa projekt i företaget. I så fall bör ledaren utses som **Ansvarig person** på projektkortet. I den här vyn över tidrapportsinformation kan du visa projektuppgifterna som är kopplade till ett projekt och antalet använda timmar.

> [!NOTE]
> För att kunna godkänna tidrapporter i fönstret **Tidrapport för chef efter projekt** måste du först markera ett alternativ för **Tidrapport per projektgodkännande** i fönstret **Resursinställning**. Mer information finns i [Ange resurser](projects-how-setup-resources.md).

### <a name="to-approve-or-reject-a-time-sheet-by-job"></a>Så här kan du godkänna eller avvisa en tidrapport per projekt

1. I rutan **Sök**, ange **Tidrapporter för chef efter projekt** och välj sedan relaterad länk. [!INCLUDE[prod_short](includes/prod_short.md)] visar en lista över tidrapportsrader som är kopplade till de projekt som du har ansvar för.
2. Välj åtgärden **Godkänn** och välj sedan åtgärden **Alla skickade rader** för att godkänna alla rader eller åtgärden **Enbart valda rader** för att endast godkänna de rader som har valts på sidan **Tidrapport**.

    > [!NOTE]
    > Du kan endast godkänna tidrapporter som har statusen **Skickad**.

3. Om du vill lämna ytterligare information om godkännandet eller avslaget väljer du åtgärden **Relaterat**, väljer sedan **Kommentarer** och sedan **Radkommentarer** och gör dina kommentarer.
4. Välj **OK**.

> [!NOTE]
> När du har godkänt eller avvisat en tidrapportsrad efter projekt kan den inte öppnas igen eller ändras i fönstret **Tidrapport**.

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Bokföra tidrapportsrader i en resursjournal
När du har godkänt tidrapportsposter för en resurs, kan du bokföra dem i den aktuella resursjournalen.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Resursjournaler** och väljer sedan relaterad länk.  
2. Välj åtgärden **Föreslå rader från tidrapporter**.  
3. På sidan **Föreslå resursjournalrader** fyller du i fälten efter behov.  
4. Välj **OK**. Transaktioner för förbrukning skapas i resursjournalen, där du kan ändra informationen efter behov.  
5. Välj åtgärden **Bokföra**.  
6. Om du vill bekräfta bokföringen väljer du åtgärden **Transaktioner**. Sidan **Resurstransaktioner** öppnas och visar resultatet av att bokföra resursjournalen.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Bokföra tidrapportsrader i en projektjournal
När du har godkänt tidrapportsposter för ett projekt, kan du bokföra dem i den aktuella projektjournalen.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Jobbjournaler** och väljer sedan relaterad länk.  
2. Välj åtgärden **Föreslå rader från tidrapporter**.  
3. På sidan **Föreslå projektjournalrader** fyller du i fälten efter behov.  
4. Välj **OK**. Transaktioner för förbrukning skapas i projektjournalen, där du kan ändra informationen efter behov.  

    > [!NOTE]  
    >   Information om arbetstyp och om arbetet är debiterbart kopieras från tidrapportsraden. Om det behövs, kan du minska antalet timmar och skapa en delvis bokföring. Om du minskar antalet kommer raden som skapas att innehålla det återstående antalet timmar nästa gång som du väljer åtgärden **Föreslå rader från tidrapporter**.  
5. Välj åtgärden **Bokföra**.  
6. Om du vill bekräfta bokföringen väljer du åtgärden **Transaktioner**. Sidan **Projekttransaktioner** öppnas och visar resultatet av att bokföra resursjournalen.

## <a name="to-archive-time-sheets"></a>Så här arkiverar du tidrapporter
När du har bokfört tidrapporter kan du arkivera dem för framtida referens. Alla tidrapportrader måste bokföras innan en tidrapport kan arkiveras.

> [!NOTE]  
>   När du arkiverar en tidrapport, tas den bort från listan både på sidan **Tidrapport** och sidan **Tidrapport för chef**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tidrapporter** och väljer sedan relaterad länk.
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