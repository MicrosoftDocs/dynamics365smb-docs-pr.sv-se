---
title: "Så här använder du Tidrapporter för projekt | Microsoft Docs"
description: "Beskriver hur du använder tidrapporter för projekt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1796436b964f5e1e4220f885e97713848d94bdfb
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-time-sheets-for-jobs"></a>Så här kan du använda tidrapporter för projekt
Du använder batch-jobbet **Skapa tidsrapporter** för att skapa tidrapporter för ett angivet antal perioder eller veckor. Du måste ha behörighet för att kunna skapa tidrapporter.

Du kan kopiera och använda dina projektplaneringsrader i en tidrapport. På så sätt får du bara ange informationen på ett ställe och radinformationen är alltid korrekt.

När du har godkänt tidrapportsposter för ett projekt, kan du bokföra dem i den aktuella projektjournalen eller resursjournalen.

Innan du kan använda tidrapporter måste du ställa in allmän information och ange en administratör och en eller flera godkännare av tidrapporter. Mer information finns i [Så här skapar du tidrapporter](projects-how-setup-time-sheets.md).

**Obs!** den här funktionen kräver att din upplevelse är inställd på **Paket **. Mer information finns i avsnittet [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="to-create-a-time-sheet"></a>Så här skapar du en tidrapport
Du kan använda batch-jobbet **Skapa tidsrapporter** för att skapa tidrapporter för ett angivet antal perioder eller veckor. Sedan kan tidrapportsägaren öppna den och registrera tid som har spenderats på en aktivitet.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Tidrapporter**, och välj sedan relaterad länk.
2. I fönstret **Tidrapporter** väljer du åtgärden **Skapa tidrapporter**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Obs**! Fälten **Andvänd tidrapport** och **Användar-ID för tidrapportens ägare** måste fyllas i på kortet för resursen på tidrapporten.

1. Välj **OK**.  

I fönstret **Tidrapportlista** kan du visa tidrapporter som du har skapat.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Så här kan du kopiera projektplaneringsrader till en tidrapport
Nedan beskrivs hur du skapar snabbt lägger till projektplaneringsrader i en tidrapport.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Tidrapporter**, och välj sedan relaterad länk.  
2. I fönstret **Tidrapportlista** väljer du en tidrapport för den relevanta tidsperioden och väljer sedan åtgärden **Redigera tidrapport**.  
3. Välj åtgärden **Skapa rader från projektplanering**. Vissa projektplaneringsrader i tidrapporttidsperioden kopieras till tidrapporten för den personen eller maskinen i fältet **Resursnr.** i tidrapporten.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Om du vill definiera arbetstyper och lägga till en till en tidrapport
Du kan definiera arbetstypen för alla tidrapportrader för projekt. På detta sätt kan du lägga till information som du behöver för att fakturera kunden för olika typer av arbete.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Tidrapporter**, och välj sedan relaterad länk.   
2. Öppna relevant tidrapport.
3. Välj fältet **Beskrivning**.  
4. I fönstret **Jobbdetalj för tidrapportsrad** väljer du fältet **Arbetstypkod** och väljer sedan arbetstyp från listan som t.ex. **Mil**.  
5. Om inga arbetstyper finns, väljer du åtgärden **Ny**.
6. I fönstret **Arbetstyper** fyller du i fälten efter behov.
7. Upprepa steg 4 för att tilldela den nya arbetstypen till tidrapporten.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Så här kan du återanvända tidrapportsrader i andra tidrapporter
Om din tidrapportsinformation är samma från tidsperiod till tidsperiod kan du spara tid genom att kopiera raderna från den föregående perioden. Sedan kan du ange bara din tidförbrukning för den nya perioden.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Tidrapporter**, och välj sedan relaterad länk.  
2. Öppna tidrapporten för en period senare än perioden för en befintlig tidrapport med rader.  
3. Välj åtgärden **Kopiera rader från föregående tidrapport**.

Raderna kopieras med uppgifter som till exempel typ och beskrivning. Till exempel om raden är relaterad till ett projekt, kopieras **Jobbnr** . Alla kopierade rader har statusen **Öppen**. Du kan nu ändra raderna efter behov.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>Fylla i en tidrapportrad och skicka för godkännande
Tidrapportsregistrering spåras i timmar, som är standardbasmåttenheten för resurser. Som standard visar en tidrapport vanliga arbetsdagar, från måndag till fredag.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Tidrapporter**, och välj sedan relaterad länk.  
2. Välj en tidrapport för den relevanta tidsperioden och välj sedan åtgärden **Redigera tidrapport**.  
3. Fyll i fälten på en rad efter behov. Ange numret på timmar som används av resursen på respektive veckodag.

    **Tips**: Du kan granska summan av tidrapportstimmar som du har angett i faktaboxen **Översikt över utfall/budgeterat**.  
4. Upprepa steg 3 för andra arbetstyper som resursen utför.
5. Välj åtgärden **Skicka** och välj sedan åtgärden **Alla öppna rader** för att skicka alla rader eller åtgärden **Enbart valda rader** för att endast skicka de rader som har valts i fönstret **Tidrapport**.  

    **Obs**! Du kan endast skicka tidrapportrader som du har angett tid för.  
6. För att ändra informationen på en rad som har angetts som **Skickad** väljer du raden och väljer sedan åtgärden **Öppna igen**.

    **Obs**! En chef kan avvisa en tidrapportrad som skickas in för godkännande. Om en rad t.ex. har statusen **Avvisad** kan du göra ändringar av raden och sedan välja **Skicka** igen.  
7. Välj **OK**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Så här kan du godkänna eller avvisa en tidrapport
En tidrapport måste skickas för godkännande innan den kan användas. Du kan godkänna och avvisa enskilda rader i en tidrapport eller skicka tillbaka dem till avsändaren för ytterligare åtgärd. En tidrapport kan godkännas på två sätt:

* En tidrapportsadministratör kan godkänna alla tidrapporter.
* Personen som anges i fältet **Användar-ID för tidrapportens godkännare** på resurskortet kan godkänna resursens tidrapporter. Mer information finns i [Så här skapar du tidrapporter](projects-how-setup-time-sheets.md).

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Tidrapporter för chef**, och välj sedan relaterad länk.
2. Välj en tidrapport från listan.  
3. I fönstret **Tidsrapport** väljer du åtgärden **Godkänn** och väljer sedan åtgärden **Alla skickade rader** för att godkänna alla rader eller åtgärden **Enbart valda rader** för att endast godkänna de rader som valts i fönstret **Tidrapport**.
4. Välj **OK**.  
5. Välj alternativt åtgärden **Avvisa** och följ steg 4 till 5.  

**Tips**! Använd faktaboxarna **Tidrapportsstatus** och **Faktisk/schemalagd översikt** för att få översikt över tidrapportsinformation.

När du har godkänt eller avvisat en tidrapport kan den inte ändras om den inte först öppnas igen. Följande procedur förklarar hur du öppna en godkänd eller avvisad tidrapport igen.

## <a name="to-reopen-a-time-sheet"></a>Så här kan du öppna en tidrapport igen
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger du **Tidrapporter för chef** eller **Tidrapporter**, och välj sedan relaterad länk.
2. Öppna en tidrapport från listan.  

    **Obs**! Du kan endast öppna rader igen som har statusen **Godkänd**. Du kan inte öppna rader igen som har statusen **Avvisad**. Du kan inte öppna en tidrapport igen om den har bokförts.  
3. I fönstret **Tidsrapport** väljer du åtgärden **Öppna igen** och väljer sedan åtgärden **Alla skickade rader** för att öppna alla rader igen eller åtgärden **Enbart valda rader** för att endast öppna de rader igen som valts i fönstret **Tidrapport**.
4. Välj **OK**. Statusen för tidrapportraden eller raderna ändras till **Skickat**.  

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Bokföra tidrapportsrader i en resursjournal
När du har godkänt tidrapportsposter för en resurs, kan du bokföra dem i den aktuella resursjournalen.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger **Resursjournal** och väljer sedan relaterad länk.  
2. Välj åtgärden **Föreslå rader från tidrapporter**.  
3. Fyll i fälten om det behövs.  
4. Välj **OK**. Transaktioner för förbrukning skapas i resursjournalen, där du kan ändra informationen efter behov.  
5. Välj åtgärden **Bokföra**.  
6. Om du vill bekräfta bokföringen väljer du åtgärden **Transaktioner**. Fönstret **Resurstransaktioner** öppnas och visar resultatet av att bokföra resursjournalen.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Bokföra tidrapportsrader i en projektjournal
När du har godkänt tidrapportsposter för ett projekt, kan du bokföra dem i den aktuella projektjournalen.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Projektjournal**, och välj sedan relaterad länk.  
2. Välj åtgärden **Föreslå rader från tidrapporter**.  
3. Fyll i fälten om det behövs.  
4. Välj **OK**. Transaktioner för förbrukning skapas i projektjournalen, där du kan ändra informationen efter behov.  

    **Obs**! Information om arbetstyp och om arbetet är debiterbart kopieras från tidrapportsraden. Om det behövs, kan du minska antalet timmar och skapa en delvis bokföring. Om du minskar antalet kommer raden som skapas att innehålla det återstående antalet timmar nästa gång som du väljer åtgärden **Föreslå rader från tidrapporter**.  
5. Välj åtgärden **Bokföra**.  
6. Om du vill bekräfta bokföringen väljer du åtgärden **Transaktioner**. Fönstret **Projekttransaktioner** öppnas och visar resultatet av att bokföra resursjournalen.

## <a name="to-archive-time-sheets"></a>Så här arkiverar du tidrapporter
När du har bokfört tidrapporter kan du arkivera dem för framtida referens. Alla tidrapportrader måste bokföras innan en tidrapport kan arkiveras.

**Obs**! När du arkiverar en tidrapport, tas den bort från listan både i fönstret **Tidrapport** och i fönstret **Tidrapport för chef**.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Flytta tidrapporter till arkiv**, och välj sedan relaterad länk.  
2. Fyll i fälten på efter behov och välj sedan knappen **OK**.  
3. Om du vill granska arkiverade tidrapporter väljer du i det övre högra hörnet ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger du **Tidrapportarkiv** eller **Tidrapportsarkiv för chef**, och välj sedan relaterad länk.

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ställ in projekthantering](projects-setup-projects.md)    
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)     
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

