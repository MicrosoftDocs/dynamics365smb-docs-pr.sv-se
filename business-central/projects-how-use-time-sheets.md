---
title: Arbeta med tidrapporter för projekt
description: Beskriver hur du skapar en tidrapport för ett projekt, kopierar rader till ordern, definierar arbetstyper, fyller i tidrapporten och skickar den för godkännande.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheets
ms.date: 08/24/2021
ms.author: edupont
ms.openlocfilehash: 02d9536b27290ef27e5954ad6ea9004094e5cfe2
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440647"
---
# <a name="use-time-sheets-for-jobs"></a>Använda tidrapporter för projekt

Du använder batch-jobbet **Skapa tidsrapporter** för att skapa tidrapporter för ett angivet antal perioder eller veckor. Du måste ha behörighet för att kunna skapa tidrapporter.

Du kan kopiera och använda dina projektplaneringsrader i en tidrapport. På så sätt får du bara ange informationen på ett ställe och radinformationen är alltid korrekt.

När du har godkänt tidrapportsposter för ett projekt, kan du bokföra dem i den aktuella projektjournalen eller resursjournalen.

Innan du kan använda tidrapporter måste du ställa in allmän information och ange en administratör och en eller flera godkännare av tidrapporter. Mer information finns i [Skapa tidrapporter](projects-how-setup-time-sheets.md).

## <a name="to-create-a-time-sheet"></a>Så här skapar du en tidrapport

Du kan använda batch-jobbet **Skapa tidsrapporter** för att skapa tidrapporter för ett angivet antal perioder eller veckor. Sedan kan tidrapportsägaren öppna den och registrera tid som har spenderats på en aktivitet.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tidrapporter** och väljer sedan relaterad länk.
2. På sidan **Tidrapporter** väljer du åtgärden **Skapa tidrapporter**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Fälten **Andvänd tidrapport** och **Användar-ID för tidrapportens ägare** måste fyllas i på kortet för resursen på tidrapporten.
4. Välj knappen **OK**.  

På sidan **Tidrapportlista** kan du visa tidrapporter som du har skapat.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Så här kan du kopiera projektplaneringsrader till en tidrapport
Nedan beskrivs hur du skapar snabbt lägger till projektplaneringsrader i en tidrapport.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tidrapporter** och väljer sedan relaterad länk.  
2. Välj en tidrapport för den relevanta tidsperioden på sidan **Tidrapporter**.  
3. Välj åtgärden **Rad** och välj sedan åtgärden **Skapa rader från projektplanering**. Vissa projektplaneringsrader i tidrapporttidsperioden kopieras till tidrapporten för den personen eller maskinen i fältet **Resursnr.** på tidrapporten.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Om du vill definiera arbetstyper och lägga till en till en tidrapport
Du kan definiera arbetstypen för alla tidrapportrader för projekt. På detta sätt kan du lägga till information som du behöver för att fakturera kunden för olika typer av arbete.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tidrapporter** och väljer sedan relaterad länk.   
2. Öppna relevant tidrapport.
3. Välj fältet **Beskrivning**.  
4. På sidan **Projektdetalj för tidrapportsrad** väljer du fältet **Arbetstypkod** och väljer sedan arbetstyp från listan som t. ex. **Mil**.  
5. Om inga arbetstyper finns, väljer du åtgärden **Ny**.
6. På sidan **Arbetstyper** fyller du i fälten efter behov.
7. Upprepa steg 4 för att tilldela den nya arbetstypen till tidrapporten.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Så här kan du återanvända tidrapportsrader i andra tidrapporter
Om din tidrapportsinformation är samma från tidsperiod till tidsperiod kan du spara tid genom att kopiera raderna från den föregående perioden. Sedan kan du ange bara din tidförbrukning för den nya perioden.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tidrapporter** och väljer sedan relaterad länk.  
2. Öppna tidrapporten för en period senare än perioden för en befintlig tidrapport med rader.  
3. Välj åtgärden **Rad** och välj sedan åtgärden **Kopiera rader från föregående tidrapport**.

Raderna kopieras med uppgifter som till exempel typ och beskrivning. Till exempel om raden är relaterad till ett projekt, kopieras **Projektnr** . Alla kopierade rader har statusen **Öppen**. Du kan nu ändra raderna efter behov.

## <a name="to-fill-in-time-sheet-lines-and-submit-for-approval"></a>Fylla i tidrapportrader och skicka för godkännande
Tidrapportsregistrering spåras i timmar, som är standardbasmåttenheten för resurser. Som standard visar en tidrapport vanliga arbetsdagar, från måndag till fredag.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tidrapporter** och väljer sedan relaterad länk.  
2. Välj en tidrapport för aktuell period.
3. Fyll i fälten på en rad efter behov. Ange numret på timmar som används av resursen på respektive veckodag.  

    > [!TIP]  
    >   Du kan granska summan av tidrapportstimmar som du har angett i faktaboxen **Översikt över utfall/budgeterat**.  
4. Upprepa steg 3 för andra arbetstyper som resursen utför.
5. Välj åtgärden **Bearbeta**, välj sedan åtgärden **Skicka** och åtgärden **Alla öppna rader** för att skicka alla rader eller åtgärden **Enbart valda rader** för att endast skicka de rader som har valts på sidan **Tidrapport**.  

    > [!NOTE]  
    >   Du kan endast skicka tidrapportrader som du har angett tid för.  
6. För att ändra informationen på en rad som har angetts som **Skickad** väljer du raden och väljer sedan åtgärden **Öppna igen**.

    > [!NOTE]  
    >   En chef kan avvisa en tidrapportrad som skickas in för godkännande. Om en rad har status **Avvisad** kan du göra ändringar av raden och sedan välja **Skicka** igen.  
7. Välj **OK**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Så här kan du godkänna eller avvisa en tidrapport
En tidrapport måste skickas för godkännande innan den kan användas. Du kan godkänna och avvisa enskilda rader i en tidrapport eller skicka tillbaka dem till avsändaren för ytterligare åtgärd. En tidrapport kan godkännas på två sätt:

* En tidrapportsadministratör kan godkänna alla tidrapporter.
* Personen som anges i fältet **Användar-ID för tidrapportens godkännare** på resurskortet kan godkänna resursens tidrapporter. Mer information finns i [Skapa tidrapporter](projects-how-setup-time-sheets.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Tidrapporter för chef** och väljer sedan relaterad länk.
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
4. För att granska arkiverade tidtabeller, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Tidrapportsarkiv** eller **Tidrapportsarkiv för chef** och väljer sedan relaterad länk.

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ställa in projekthantering](projects-setup-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]