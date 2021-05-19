---
title: Registrera förbrukning eller användning av projektresurser och artiklar
description: Beskriver hur du registrerar förbrukning eller användning av artiklar eller resurser i ett projekt för att underlätta projekthantering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 65975621fff862b64333c87e70f34b75f8e2cbdb
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938102"
---
# <a name="record-consumption-or-usage-for-jobs"></a>Registrera förbrukning eller användning för projekt

På sidan **Projektplaneringsrader** kan du förhandsgranska och registrera förbrukningen i olika delar av projektet, som uppdateras automatiskt medan du ändrar och överför information mellan projekt och projektjournaler eller projektfakturor. Detta kräver att du har konfigurerat ett projekt så att **Använd förbrukningslänk** aktiveras. Mer information finns i [Skapa projekt](projects-how-setup-jobs.md).  

Till exempel för planeringsrader av typen **Budget** kan du ange antal av en resurs och hur stort antal som ska överföras till projektjournalen. Om typen av planeringsrad är **Fakturerbar** kan du ange antal av resursen och hur stort antal som ska överföras till en faktura. Mer information om hur du fakturerar kunden finns i [Fakturera projekt](projects-how-invoice-jobs.md). Genom att jämföra ursprungligt antal, återstående antal eller bokfört antal kan du snabbt granska användningsinformation. För information om att uppskatta budgeterade värden i samband med planering, se [Hantera projektbudget](projects-how-manage-budgets.md).  

Efterföljande procedurer beskriver hur du registrerar verklig (budgeterad) kvantitet och kostnader med projektjournal. Du kan också använda inköpsdokument för att registrera inköp för ett projekt. Mer information finns i [Hantera projektleveranser](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Registrera förbrukning på en projektplaneringsrad av typen Budget

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt** och välj sedan relaterad länk.  
2. Välj relevant projekt och välj sedan åtgärden **Projektplaneringsrader**.
3. Välj en projektplaneringsrad av typen **Budget** eller skriv **Både Budget och Fakturerbart** som du vill registrera förbrukning för.  

    > [!NOTE]
    > Du kan också registrera förbrukning på en projektplaneringsrad av typen **Fakturerbart**. Vanligtvis använder du den här raden för att skapa fakturor, men du kan även överföra den till en journal. Mer information finns i [Så här fakturerar du projekt](projects-how-invoice-jobs.md) <!--However, when you do that, a job planning line of type **Budget** is created to match the billable line. For more information, see [Manage Job Budgets](projects-how-manage-budgets.md).-->

4. Gå till fältet **Antal att överföra till journal** och ange hur stort antal som ska överföras. Standardkvantiteten är samma värde som du angav i fältet **Antal**.

    Fältet **Återstående antal** visar kvantiteten som återstår för att slutföra projektet och att överföras till journalen.  
5. Välj åtgärden **Skapa projektjournalrader**.

    > [!TIP]
    > Om du kommer att lägga till fler projekt planeringsrader för projektet måste du vänta med det här steget tills du har lagt till alla projektplaneringsrader.
6. På sidan **Projekt – Överför projektplaneringsrad** fyller du i fälten efter behov och väljer sedan knappen **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Välj åtgärden **Öppna projektjournal**.  
8. På sidan **Projektjournal** väljer du relevant rad och väljer sedan åtgärden **Bokför**.
9. På sidan **Projektplaneringsrader** granskar du den registrerade förbrukningen genom att observera fälten **Antal**, **Återstående antal** och **Antal att överföra till journal**.  
10. Upprepa steg 3 till 8 om du vill registrera extra förbrukning.  

## <a name="to-create-job-journal-lines-manually"></a>Så här skapar du projektjournalrader manuellt

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Projektjournaler** och välj sedan relaterad länk.  
2. Välj relevant projektjournalnamn i fältet **Journalnamn**.  
3. Ange dokumentnummer, projektnumret, projektaktivitetsnummer, typ och antal av typen som förbrukas, på en ny rad.  
4. Välj åtgärden **Bokför** när projektjournalraderna har slutförts.  

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Så här visar du projektförbrukning och uppskattningar och bokföruppdateringar

Du kan visa projektförbrukningen fram till projektet avslutas i ett steg. Det gör du genom att använda batch-jobbet **Projekt – Beräkna återstående förbrukning** för alla aktiviteter fram till och med projektets slut.  

Då kan du spåra och jämföra de ursprungliga uppskattningarna mot faktiskt resultat och göra ändringar eller nya transaktioner efter behov. Du kanske till exempel har uppskattat att ett projekt kräver tio timmar, och fram till dagens datum har det tagit 15 timmar. Du kan lägga till dessa extra fem timmar på den befintliga journalraden eller skapa en ny journalrad om du vill rapportera dessa fem timmar som övertid, som är en annan arbetstyp. Rätt kostnad och pris beräknas, och du kan sedan bokföra detta i journalen.  

> [!NOTE]  
>   Artikeltransaktioner skapar artikeltransaktioner och minskar lagerkvantiteten. Batch-jobbet **Bokför lagerkostnad i redov.** överför kostnaden från lagret till redovisningen. Resurstransaktioner skapar resurstransaktioner.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projektjournaler** och välj sedan relaterad länk.  
2. Välj en relevant projektjournal och välj sedan åtgärden **Ber. återstående förbrukning**.  
3. På sidan **Ber. återstående förbrukning** anger du dokumentnumret och bokföringsdatumet som ska infogas i journalen och väljer sedan knappen **OK**.  
4. Uppdatera journalen med eventuella ändringar som kan behövas.  
5. Välj **Bokföra**.



## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Granska planeringsrader för en projekttransaktion

När du har bokfört projektjournalrader kan du se de planeringsrader som är kopplade till de projektjournaltransaktioner som har bokförts.

> [!NOTE]  
> Detta kräver att kryssrutan **Använd förbrukningslänk** är markerad för jobbet. Mer information finns i [Skapa projekt](projects-how-setup-jobs.md).  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projektjournaler** och välj sedan relaterad länk.  
2. Välj en relevant projektjournal och välj sedan åtgärden **Transaktioner**.  
3. På sidan **Projekttransaktioner** väljer du åtgärden **Visa kopplade projektplaneringsrader**.

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)      
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
