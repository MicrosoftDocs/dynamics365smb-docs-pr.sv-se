---
title: Registrera förbrukning eller användning av projektresurser och artiklar
description: Denna artikel beskriver hur du registrerar förbrukning eller användning av artiklar eller resurser för projekt i projekthantering.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
---
# Registrera förbrukning eller användning för projekt

På sidan **Jobbkort** kan du öppna sidan **Projektplaneringsrader** om du vill granska och registrera användning på olika delar av projektet. Den här informationen uppdateras automatiskt när du ändrar och överför information mellan projekt och projektjournaler eller projektfakturor. Detta innebär att du har aktiverat växlingsknappen **Använd förbrukningslänk som standard** på sidan **Inställningar i projekt**. Läs mer i [Ställa in projekt](projects-how-setup-jobs.md).  

Till exempel för planeringsrader av typen **Budget** kan du ange antal av en resurs och hur stort antal som ska överföras till projektjournalen. Om typen av planeringsrad är **Fakturerbar** kan du ange antal av resursen och hur stort antal som ska överföras till en faktura. Mer information om hur du fakturerar kunden finns i [Fakturera projekt](projects-how-invoice-jobs.md). Genom att jämföra ursprungligt antal, återstående antal eller bokfört antal kan du snabbt granska användningsinformation. För mer information om att uppskatta budgeterade värden i samband med planering, se [Hantera projektbudget](projects-how-manage-budgets.md).  

Efterföljande procedurer beskriver hur du registrerar verklig (budgeterad) kvantitet och kostnader med projektjournal. Du kan också använda inköpsdokument för att registrera inköp för ett projekt. Läs mer i [Hantera projektleveranser](projects-how-manage-project-supplies.md).

## Registrera förbrukning på en projektplaneringsrad av typen Budget

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2. Välj projekt och välj sedan åtgärden **Projektplaneringsrader**. 
3. Välj en projektplaneringsrad av typen **Budget** eller skriv **Både Budget och Fakturerbart** som du vill registrera förbrukning för.   

    > [!NOTE]
    > Du kan också registrera förbrukning på en projektplaneringsrad av typen **Fakturerbart**. Vanligtvis använder du dessa rader för att skapa fakturor, men du kan även överföra informationen till en journal. Läs mer på [fakturaprojekt](projects-how-invoice-jobs.md) 

4. På fältet **Antal att överföra till journal** anger du hur stort antal som ska överföras. Standardkvantiteten är samma värde som du angav i fältet **Antal**.

    Fältet **Återstående antal** visar kvantiteten som återstår för att slutföra projektet och att överföras till journalen.
5. Välj åtgärden **Skapa projektjournalrader**.

    > [!TIP]
    > Om du kommer att lägga till fler projekt planeringsrader för projektet måste du vänta med det här steget tills du har lagt till alla projektplaneringsrader.
6. På sidan **Projekt – Överför projektplaneringsrad** fyller du i fälten efter behov och väljer sedan knappen **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Välj åtgärden **Öppna projektjournal**.  
8. På sidan **Projektjournal** väljer du relevant rad och väljer sedan åtgärden **Bokför**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. På sidan **Projektplaneringsrader** granskar du den registrerade förbrukningen genom att observera fälten **Antal**, **Återstående antal** och **Antal att överföra till journal**.  
10. Upprepa steg 3 till 8 om du vill registrera extra förbrukning.  

## Så här skapar du projektjournalrader manuellt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Jobbjournaler** och väljer sedan relaterad länk.  
2. Välj relevant projektjournalnamn i fältet **Journalnamn**.  
3. Ange dokumentnummer, projektnumret, projektaktivitetsnummer, typ och antal av typen som förbrukas, på en ny rad.  
4. Välj åtgärden**Bokför** när projektjournalraderna har slutförts.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Så här visar du projektförbrukning och uppskattningar och bokföruppdateringar

Du kan visa projektförbrukningen fram till projektet avslutas i ett steg. Det gör du genom att använda batch-jobbet **Projekt – Beräkna återstående förbrukning** för alla aktiviteter fram till och med projektets slut.  

Då kan du spåra och jämföra de ursprungliga uppskattningarna mot faktiskt resultat och göra ändringar eller nya transaktioner efter behov. Du kanske till exempel har uppskattat att ett projekt kräver tio timmar, och fram till dagens datum har det tagit 15 timmar. Du kan lägga till dessa extra fem timmar på den befintliga journalraden eller skapa en ny journalrad om du vill rapportera dessa fem timmar som övertid, som är en annan arbetstyp. Rätt kostnad och pris beräknas, och du kan sedan bokföra detta i journalen.  

> [!NOTE]  
> Artikeltransaktioner skapar artikeltransaktioner och minskar lagerkvantiteten. Batch-jobbet **Bokför lagerkostnad i redov.** överför kostnaden från lagret till redovisningen. Resurstransaktioner skapar resurstransaktioner.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Jobbjournaler** och väljer sedan relaterad länk.  
2. Välj en relevant projektjournal och välj sedan åtgärden **Ber. återstående förbrukning**.  
3. På sidan **Ber. återstående förbrukning** anger du dokumentnumret och bokföringsdatumet som ska infogas i journalen och väljer sedan knappen **OK**.  
4. Uppdatera journalen med eventuella ändringar som kan behövas.  
5. Välj **Bokföra**.

## Skapa dokument för lager och distributionslagerplockning för ett jobb

Om du vill skapa dokument för lager och distributionslagerplockning för projekt måste administratören aktivera **Funktionsuppdatering: Aktivera lager- och distributionslagerplockning från projekt** på sidan **funktionshantering**.

Funktionen lägger till åtgärden **Skapa lagerplockning** och **Skapa distributionslagerplockning** på **projektkortet**. Om du vill skapa eller registrera ett plocknings dokument använder du **Artikelinförsel/plockningsrader/transportrader** eller **registrerade plockningsrader**. Läs mer på [Flöden för produktion, montering och projekt](design-details-internal-warehouse-flows.md).

Du kan använda åtgärder på följande villkor:

* **Status** för projektet är **öppen**.
* **Radtypen** för projektplaneringsraden är **budget** , eller **både budget och fakturerbar**. 
* **Typen** av projektplaneringsrad är **artikel**.
* **Begär plockning** har aktiverats för den relaterade platsen.
* **Dirigerad art.inf. och plock.** är inaktiverad.

> [!NOTE] 
> Även om inställningen har anropats **kräver plockning** kan du fortfarande bokföra förbrukning direkt från projektjournalraden för lagerstället. När lagerstället har konfigurerats så att plockning krävs men inte leverans, använder du sidan **Lagerplockning** för att organisera och skriva ut plockinformationen. Du kan också använda sidan för att registrera och bokföra resultatet av plockningen, som i sin tur bokför förbrukningen av artiklarna. 
> 
> Om din plats är inställd för att kräva både plockning och leveransbearbetning, vilket innebär att du har valt både **Begär plockning** och **Begär utleverans**på sidan **Platskort** använd **Dist.lager plockning** för att hantera plockningen. Distributionslagerplockningar liknar lagerplockningar. Skillnaden är att istället för att bokföra plockningsinformationen registrerar du plockningen. Registreringen bokförs inte i förbrukningen, utan bara artiklarna kan bokföras. Du lagerchef kan du använda ett plockningskalkylark för att organisera plockninginformation innan du skapar de individuella plockningsinstruktionerna för lager

## Granska planeringsrader för en projekttransaktion

När du har bokfört projektjournalrader kan du se de planeringsrader som är kopplade till de projektjournaltransaktioner som har bokförts.

> [!NOTE]  
> Detta kräver att kryssrutan **Använd förbrukningslänk** är markerad för jobbet. Mer information finns i [Skapa projekt](projects-how-setup-jobs.md).  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Jobbjournaler** och väljer sedan relaterad länk.  
2. Välj en relevant projektjournal och välj sedan åtgärden **Transaktioner**.  
3. På sidan **Projekttransaktioner** väljer du åtgärden **Visa kopplade projektplaneringsrader**.

## Se relaterad [Microsoft utbildning](/training/paths/post-job-usage-sales/)

## Se även

[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
