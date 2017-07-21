---
title: "Registrera fakturerbara timmar och budgeterad förbrukning av jobbresurs | Microsoft Docs"
description: "Beskriver hur du registrerar förbrukning eller användning av artiklar eller resurser i ett projekt för att underlätta projekthantering."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2b42abaed502c49a595a35656570548e48321b46
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-record-usage-for-jobs"></a>Så här kan du registrera förbrukning för projekt
I fönstret **Projektplaneringsrader** kan du förhandsgranska och registrera förbrukningen i olika delar av projektet, som uppdateras automatiskt medan du ändrar och överför information mellan projekt och projektjournaler eller projektfakturor. Detta innebär att du har konfigurerat ett projekt så att **Använd förbrukningslänk** aktiveras. Mer information finns i [Så här skapar du Projekt](projects-how-setup-jobs.md).  

Till exempel för planeringsrader av typen **Budget** kan du ange antal av en resurs och hur stort antal som ska överföras till projektjournalen. Om typen av planeringsrad är **Fakturerbar** kan du ange antal av resursen och hur stort antal som ska överföras till en faktura. Genom att jämföra antalet som har överförts till journalen eller fakturan med det återstående antalet, kan du snabbt granska information om förbrukning.

Efterföljande procedurer beskriver hur du registrerar verkligt (fakturerbart), eller budgeterat projektpris och kostnader. För information om att uppskatta budgeterade värden under planering, se [Så här hanterar du projektbudget](projects-how-manage-budgets.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Så här kan du registrera förbrukning på en projektplaneringsrad av typen Budget
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projekt** och välj sedan relaterad länk.  
2. Välj relevant projekt och välj sedan åtgärden **Projektplaneringsrader**.
3. Välj en projektplaneringsrad av typen **Budget** eller skriv **Både Budget och Fakturerbart** som du vill registrera förbrukning för.
4. Gå till fältet **Antal att överföra till journal** och ange hur stort antal som ska överföras. Standardkvantiteten är samma värde som du angav i fältet **Antal**.

    Fältet **Återstående antal** visar kvantiteten som återstår för att slutföra projektet och att överföras till journalen.  
5. Välj åtgärden **Skapa projektjournalrader**.
6. I fönstret **Projekt - Överför projektplaneringsrad** fyller du i fälten efter behov och väljer sedan knappen **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Välj åtgärden **Öppna projektjournal**.  
8. I fönstret **Projektjournal** väljer du relevant rad och väljer sedan åtgärden **Bokför**.
9. I fönstret **Projektplaneringsrader** granskar du den registrerade förbrukningen genom att observera fälten **Antal**, **Återstående antal** och **Antal att överföra till journal**.  
10. Upprepa steg 3 till 8 om du vill registrera extra förbrukning.  

## <a name="to-record-usage-for-a-job-planning-line-of-type-billable"></a>Så här kan du registrera förbrukning på en projektplaneringsrad av typen Fakturerbart
I nästa uppgift registrerar du också förbrukning, men för en projektplaneringsrad av typen **Fakturerbart**. I det här fallet faktureras vanligtvis förbrukningen, men du kan även överföra den till en journal. Men om du gör det skapas en projektplaneringsrad av typen **Budget** för att matcha fakturerbar rad. Mer information finns i [Så här hanterar du projektbudget](projects-how-manage-budgets.md).

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projekt** och välj sedan relaterad länk.
2. Välj relevant projekt och välj sedan åtgärden **Projektplaneringsrader**.  
3. Välj en projektplaneringsrad av typen **Fakturerbart**, som du vill registrera förbrukning för.
4. Gå till fältet **Antal att överföra till faktura** och ange hur stort antal som ska överföras. Standardkvantiteten är samma värde som du angav i fältet **Antal**.

    Fältet **Antal att fakturera** visar kvantiteten som återstår för att slutföra projektet och faktureras.  
5. Välj åtgärden **Skapa försäljningsfaktura**.
6. I fönstret **Projekt - Överför till förs.faktura** fyller du i fälten efter behov och väljer sedan knappen **OK**.
7. I fönstret **Projektplaneringsrader** väljer du relevant rad och väljer sedan åtgärden **Bokför**.
8. Granska den registrerade förbrukningen, genom att observera fälten **Antal**, **Antal att fakturera**, **Antal att överföra till faktura** och om försäljningsfakturan överförs, fältet **Antal fakturerat**.
9. Upprepa steg 3 till 8 om du vill registrera extra förbrukning.  
10. Om du vill granska en relaterad bokförd försäljningsfaktura, välj **Försäljningsfakturor/kreditnotor**.  
11. Välj relevant faktura och välj åtgärden **Öppna försäljningsfaktura/-kreditnota** i fönstret **Projektfakturor**.         

## <a name="to-create-job-journal-lines-from-job-planning-lines"></a>Så här skapar du projektjournalrader från projektplaneringsrader
När du är klar att bokföra ekonomisk information för projektet, måste du skapa projektjournalrader som du kan bokföra.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projekt** och välj sedan relaterad länk.  
2. Välj relevant öppet projekt och välj sedan åtgärden **Projektplaneringsrader**.  
3. I fönstret **Projektplaneringsrader** på en relevant projektplaneringsrad i fältet **Antal att överföra till journal** anger du det antal som du vill överföra till en projektjournal.  
4. Välj åtgärden **Skapa projektjournalrader**.
5. I fönstret **Projekt - Överför projektplaneringsrad** fyller du i fält efter behov.  
6. Välj **OK**. Projektjournalrader skapas.
7. Om du vill validera överföringen öppnar du den relevanta projektjournalen och kontrollerar transaktionerna.  
8. Välj åtgärden**Bokför** när projektjournalraderna har slutförts.  

## <a name="to-create-job-journal-lines-manually"></a>Så här skapar du projektjournalrader manuellt
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projektjournaler** och välj sedan relaterad länk.  
2. Välj relevant projektjournalnamn i fältet **Journalnamn**.  
3. Ange dokumentnummer, projektnumret, projektaktivitetsnummer, typ och antal av typen som förbrukas, på en ny rad.  
4. Välj åtgärden**Bokför** när projektjournalraderna har slutförts.  

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Granska planeringsrader för en projekttransaktion
När du har bokfört projektjournalrader kan du se de planeringsrader som är kopplade till de projektjournaltransaktioner som har bokförts.

> [!NOTE]  
>   Detta kräver att kryssrutan **Använd förbrukningslänk** har valts för projektet, eller är standardinställningen för alla projekt i organisationen. Mer information finns i [Så här skapar du Projekt](projects-how-setup-jobs.md).  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Projektjournaler** och välj sedan relaterad länk.  
2. Välj en relevant projektjournal och välj sedan åtgärden **Transaktioner**.  
3. I fönstret **Projekttransaktioner** väljer du åtgärden **Visa kopplade projektplaneringsrader**.

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)      
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

