---
title: Registrera fakturerbara timmar och budgeterad förbrukning av jobbresurs | Microsoft Docs
description: Beskriver hur du registrerar förbrukning eller användning av artiklar eller resurser i ett projekt för att underlätta projekthantering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 06/26/2020
ms.author: edupont
ms.openlocfilehash: 324de3ce7b5cbffff59c78f1e5374daf6fa8fd1d
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784844"
---
# <a name="record-usage-for-jobs"></a>Registrera förbrukning för projekt

På sidan **Projektplaneringsrader** kan du förhandsgranska och registrera förbrukningen i olika delar av projektet, som uppdateras automatiskt medan du ändrar och överför information mellan projekt och projektjournaler eller projektfakturor. Detta innebär att du har konfigurerat ett projekt så att **Använd förbrukningslänk som standard** aktiveras. Mer information finns i [Skapa projekt](projects-how-setup-jobs.md).  

Till exempel för planeringsrader av typen **Budget** kan du ange antal av en resurs och hur stort antal som ska överföras till projektjournalen. Om typen av planeringsrad är **Fakturerbar** kan du ange antal av resursen och hur stort antal som ska överföras till en faktura. Genom att jämföra antalet som har överförts till journalen eller fakturan med det återstående antalet, kan du snabbt granska information om förbrukning.

Efterföljande procedurer beskriver hur du registrerar verkligt (fakturerbart), eller budgeterat projektpris och kostnader. För information om att uppskatta budgeterade värden i samband med planering, se [Hantera projektbudget](projects-how-manage-budgets.md).  

> [!TIP]
> I följande avsnitt använder vi termen *Registrera förbrukning* för att täcka två uppgifter: registrera projektplaneringsrader och fakturera kunden på lämpligt sätt.

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Registrera förbrukning på en projektplaneringsrad av typen Budget

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt** och välj sedan tillhörande länk.  
2. Välj relevant projekt och välj sedan åtgärden **Projektplaneringsrader**.
3. Välj en projektplaneringsrad av typen **Budget** eller skriv **Både Budget och Fakturerbart** som du vill registrera förbrukning för.
4. Gå till fältet **Antal att överföra till journal** och ange hur stort antal som ska överföras. Standardkvantiteten är samma värde som du angav i fältet **Antal**.

    Fältet **Återstående antal** visar kvantiteten som återstår för att slutföra projektet och att överföras till journalen.  
5. Välj åtgärden **Skapa projektjournalrader**.

    > [!TIP]
    > Om du kommer att lägga till fler projekt planeringsrader för projektet måste du vänta med det här steget tills du har lagt till alla projektplaneringsrader.
6. På sidan **Projekt - Överför projektplaneringsrad** fyller du i fälten efter behov och väljer sedan knappen **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Välj åtgärden **Öppna projektjournal**.  
8. På sidan **Projektjournal** väljer du relevant rad och väljer sedan åtgärden **Bokför**.
9. På sidan **Projektplaneringsrader** granskar du den registrerade förbrukningen genom att observera fälten **Antal**, **Återstående antal** och **Antal att överföra till journal**.  
10. Upprepa steg 3 till 8 om du vill registrera extra förbrukning.  

## <a name="to-record-usage-for-a-job-planning-line-of-type-billable"></a>Registrera förbrukning på en projektplaneringsrad av typen Fakturerbart

I nästa uppgift registrerar du också förbrukning, men för en projektplaneringsrad av typen **Fakturerbart**. I det här fallet faktureras vanligtvis förbrukningen, men du kan även överföra den till en journal. Men om du gör det skapas en projektplaneringsrad av typen **Budget** för att matcha fakturerbar rad. Mer information finns i [Hantera projektbudget](projects-how-manage-budgets.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Jobb** och välj sedan relaterad länk.
2. Välj relevant projekt och välj sedan åtgärden **Projektplaneringsrader**.  
3. Välj en projektplaneringsrad av typen **Fakturerbart**, som du vill registrera förbrukning för.
4. Gå till fältet **Antal att överföra till faktura** och ange hur stort antal som ska överföras. Standardkvantiteten är samma värde som du angav i fältet **Antal**.

    Fältet **Antal att fakturera** visar kvantiteten som återstår för att slutföra projektet och faktureras.  
5. Välj åtgärden **Skapa försäljningsfaktura**.

    > [!TIP]
    > Om du kommer att lägga till fler projekt planeringsrader för projektet måste du vänta med det här steget tills du har lagt till alla projektplaneringsrader.
6. På sidan **Projekt - Överför till förs.faktura** fyller du i fälten efter behov och väljer sedan knappen **OK**.
7. Granska den registrerade förbrukningen, genom att observera fälten **Antal**, **Antal att fakturera**, **Antal att överföra till faktura** och om försäljningsfakturan överförs, fältet **Antal fakturerat**.
8. Upprepa steg 3 till 7 om du vill registrera extra förbrukning.  
9. Om du vill granska en relaterad bokförd försäljningsfaktura, välj **Försäljningsfakturor/kreditnotor**.  

    Om det finns fler än en faktura för det här projektet måste du välja den relevanta fakturan på sidan **projektfakturor** och sedan välja åtgärden **Öppna försäljningsfaktura/-kreditnota**.  

## <a name="to-create-job-journal-lines-from-job-planning-lines"></a>Så här skapar du projektjournalrader från projektplaneringsrader

När du är klar att bokföra ekonomisk information för projektet, måste du skapa projektjournalrader som du kan bokföra.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Jobb** och välj sedan relaterad länk.  
2. Välj relevant öppet projekt och välj sedan åtgärden **Projektplaneringsrader**.  
3. På sidan **Projektplaneringsrader** på en relevant projektplaneringsrad i fältet **Antal att överföra till journal** anger du det antal som du vill överföra till en projektjournal.  
4. Välj åtgärden **Skapa projektjournalrader**.
5. På sidan **Projekt - Överför projektplaneringsrad** fyller du i fält efter behov.  
6. Välj knappen **OK**. Projektjournalrader skapas.
7. Om du vill validera överföringen öppnar du den relevanta projektjournalen och kontrollerar transaktionerna.  
8. Välj åtgärden**Bokför** när projektjournalraderna har slutförts.  

## <a name="to-create-job-journal-lines-manually"></a>Så här skapar du projektjournalrader manuellt

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Jobbjournaler** och välj sedan relaterad länk.  
2. Välj relevant projektjournalnamn i fältet **Journalnamn**.  
3. Ange dokumentnummer, projektnumret, projektaktivitetsnummer, typ och antal av typen som förbrukas, på en ny rad.  
4. Välj åtgärden**Bokför** när projektjournalraderna har slutförts.  

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Granska planeringsrader för en projekttransaktion

När du har bokfört projektjournalrader kan du se de planeringsrader som är kopplade till de projektjournaltransaktioner som har bokförts.

> [!NOTE]  
> Detta kräver att kryssrutan **Använd förbrukningslänk som standard** har valts för projektet, eller är standardinställningen för alla projekt i organisationen. Mer information finns i [Skapa projekt](projects-how-setup-jobs.md).  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Jobbjournaler** och välj sedan relaterad länk.  
2. Välj en relevant projektjournal och välj sedan åtgärden **Transaktioner**.  
3. På sidan **Projekttransaktioner** väljer du åtgärden **Visa kopplade projektplaneringsrader**.

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)      
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
