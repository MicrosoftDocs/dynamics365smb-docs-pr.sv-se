---
title: Försäkra anläggningstillgångar | Microsoft Docs
Description: Du kan tilldela försäkringsbrev för en anläggningstillgång som representeras av ett försäkringskort.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 3e26786d1568cdae30be0bcb17de7a5ed824c364
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184466"
---
# <a name="insure-fixed-assets"></a>Försäkra anläggningstillgångar
En försäkringsbrev för en anläggningstillgång representeras av ett försäkringskort. Du kan koppla en anläggningstillgång till en försäkringspolicy eller flera anläggningstillgångar till en försäkringspolicy.

Du tilldelar en anläggningstillgång till en försäkringspolicy genom att bokföra försäkringstransaktionerna från sidan **Försäkringsjournal**.

Dessutom kan du tilldela en anläggningstillgång till en försäkringspolicy och skapa försäkringstransaktioner när du bokför dess anskaffningskostnad. Du gör detta genom att bokföra en anskaffningskostnad från anläggningstillgångsjournalen med fältet **Försäkringnr.** ifyllt. Kryssrutan **Automatisk försäkringsbokf.** på sidan **Anläggningstillgånginställningar** måste markeras. För mer information, se [Att bokföra en anskaffning av anläggningstillgång manuellt med redovisningsjournalen för anläggningstillgångar](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

Om kryssrutan **Automatisk försäkringsbokf.** på sidan **Anläggningstillgånginställningar** inte har markerats, kommer bokföring av anskaffning från anläggningstillgångsjournalen att skapa rader i fönstret **Försäkringsjournal** som du sedan måste posta manuellt.

> [!WARNING]  
>   Om du inte markerar kryssrutan **Automatisk försäkringsbokf.** på sidan **Anläggningstillgånginställningar** när en försäkringsjournal ska baseras på en journalmall utan en nummerserie. Det är därför att de infogade verifikationsnumren från anläggningstillgångjournalraden annars kommer i konflikt med försäkringsjournalens nummerserie. För mer information om journalmallar och journaler, se [Så här ställer du in allmän information om anläggningstillgångar](fa-how-setup-general.md).

När du har fördelat en fast anläggningstillgång till en försäkringpolicy, markeras kryssrutan **Försäkrad** på anläggningstillgångskortet. När du säljer anläggningstillgången avmarkeras kryssrutan automatiskt.

## <a name="to-create-or-modify-an-insurance-card"></a>Så här skapar eller ändrar du ett försäkringskort
En försäkringpolicy för en anläggningstillgång måste representeras av ett försäkringskort.

När du får information om ändringar av försäkringsbeloppet måste du ange den nya informationen på sidan **försäkringskort** så att försäkringsbrevet analyseras korrekt.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäkring** och välj sedan tillhörande länk.
2. Välj åtgärden **Ny** för att skapa ett nytt kort för en försäkringspolicy. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Alternativt markerar du försäkringspolicym som du vill ändra och väljer sedan åtgärden **Redigera**.

## <a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a>För att koppla en anläggningstillgång till ett försäkringsbrev genom att bokföra från försäkringsjournalen
Du tilldelar en anläggningstillgång till ett försäkringsbrev genom att bokföra från försäkringstransaktionerna.  

Efterföljande procedur beskriver hur du skapar en försäkringsjournalrad manuellt. Om kryssrutan **Automatisk försäkringsbokf.** är markerad på sidan **Anl.inställningar** skapas försäkringsjournalrader automatiskt, när du bokför anskaffningskostnaden. I så fall är allt du måste göra att bokföra journalen.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäkringsjournaler** och välj sedan tillhörande länk.  
2. Öppna den relevanta journalen och fyll i journalraderna som behövs.  
3. För att skapa flera anläggningstillgångar till ett försäkringsbrev skapar du journalrader med samma värdet i fältet**Försäkringsnr.** och olika värden i fältet **Anl.nr**.  
4. Välj åtgärden **Bokföra**.  

    > [!NOTE]  
    >   Transaktionerna från en försäkringsjournal bokförs endast i försäkringstransaktionerna.  

## <a name="to-update-the-insurance-value-of-a-fixed-asset"></a>Om du vill uppdatera försäkringvärdet för en anläggningstillgång
Du kan använda batch-jobbet **Indexera försäkring** när du vill uppdatera värdet för den anläggningstillgång som är försäkrad.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Indexera försäkring** och välj sedan tillhörande länk.
2. Fyll i fälten om det behövs.

    > [!NOTE]  
    >   I fältet **Indextal** anger du en minskning av 5 %, till exempel som 95, medan du anger en ökning med 2 % som 102.  
3. Välj **OK**.  

   Batch-jobbet beräknar det nya beloppet som en procentsats av det totala försäkringsvärdet på sidan **Försäkringsstatistik** och en rad i försäkringsjournalen skapas.  
4. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäkringsjournaler** och välj sedan tillhörande länk.  
5. Öppna relevant försäkringsjournal, granska de skapade värdena och bokför dem i försäkringstransaktionerna.  

## <a name="to-monitor-insurance-coverage"></a>Att bevaka försäkringsskydd
[!INCLUDE[d365fin](includes/d365fin_md.md)] ger dedikerade rapporter och statistiksidor för användning vid analys av försäkringsbrev och om anläggningstillgångarna är över- eller underförsäkrade.  

### <a name="overview-of-insurance-policies"></a>Översikt över försäkringsbrev
Få en översikt över försäkringsbreven genom att skriva ut rapporten **Försäkringslista** rapport. Rapporten visar alla försäkringsbrev och de viktigaste fälten på försäkringskortet visas.  

### <a name="insurance-coverage"></a>Försäkringsskydd
Om du vill se vilka försäkringsbrev som täcker varje tillgång och till vilket belopp kan du förhandsgranska eller skriva ut rapporten **Försäkring med totalvärde**.  

### <a name="overunder-coverage"></a>Över-/underförsäkringsskydd
Du kan kontrollera om anläggningstillgångar är över- eller underförsäkrade på följande sätt:  

* Sidan **Försäkringsstatistik** visas. Ett positivt belopp i fältet **Över-/underförsäkrad** innebär att anläggningstillgången är överförsäkrad. Ett negativt belopp innebär att den är underförsäkrad.  
* Sidan **Anl.statistik** visas. Välj fältet **Totalt försäkrat värde** för att visa sidan **Försäkringstransaktioner**.  
* Rapporten **Över/underförsäkringsskydd**.  
* Rapporten **Försäkringsanalys**.  

### <a name="uninsured-fixed-assets"></a>Oförsäkrade anläggningstillgångar
Om du vill kontrollera att du inte har glömt att koppla en anläggningstillgång till ett försäkringsbrev kan du skriva ut eller förhandsgranska rapporten **Försäkring – oförsäkrade anl.**. Den här rapporten visar de individuella anläggningstillgångar för vilka belopp inte har bokförts till försäkringstransaktionerna.  

## <a name="to-view-insurance-coverage-ledger-entries"></a>Så här visar du försäkringstransaktioner
Du kan visa de transaktioner som du har skapat i försäkringstransaktionerna.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäkring** och välj sedan tillhörande länk.  
2. Välj aktuellt försäkringsbrev och klicka på åtgärden **Försäkringstransaktioner.**.  

## <a name="to-view-the-total-insurance-value-of-fixed-assets"></a>Så här visar du det försäkrade totalvärdet för en anläggningstillgång:
En dedikerad matrissida visar försäkringsbeloppet som registreras för varje försäkringsbrev för varje anläggningstillgång som ett resultat av försäkringsrelaterade belopp som du har bokfört.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäkring** och välj sedan tillhörande länk.  
2. Välj aktuellt försäkringsbrev och klicka på åtgärden **Försäkrat totalvärde per anl.**.  
3. Fyll i fälten om det behövs.  
4. Välj åtgärden **Visa matris**.  
5. Välj ett värde i matrisen för att visa de underliggande försäkringstransaktionerna.  

## <a name="to-correct-insurance-coverage-entries"></a>Så här rättar du försäkringstransaktioner
Om en anläggningstillgång har kopplats till fel försäkringsbrev, kan du rätta detta genom att skapa två omklassificeringsposter från försäkringsjournalen.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäkringsjournaler** och välj sedan tillhörande länk.  
2. Skapa en journalrad för anläggningstillgången och det korrekta försäkringsbrevet där värdet i fältet **Belopp** är positivt.  
3. Skapa en annan journalrad för anläggningstillgången och det felaktiga försäkringsbrevet där värdet i fältet **Belopp** är negativt.  
4. Välj åtgärden **Bokföra**.  

Anläggningstillgången kommer att frigöras från det felaktiga försäkringsbrevet på en andra rad och istället kopplas till korrekt försäkringsbrev på den första raden.  

## <a name="see-also"></a>Se även
[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
