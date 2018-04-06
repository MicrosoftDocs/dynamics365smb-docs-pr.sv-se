---
title: "Skapa ett projektkort för ett projekt och ange aktiviteter | Microsoft Docs"
description: "För ett nytt projekt kan du skapa ett projektkort med projektaktiviteterna och planeringsrader för att hantera hur och budgetar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, task
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ece0a95f83868ac2657fdf41330e7d0a9cce37d6
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="create-jobs"></a>Skapa projekt
När du vill starta ett nytt projekt måste du skapa ett projektkort med inbyggda projektaktiviteter och projektplaneringsrader, strukturerade i två lager.  

Det första lagret består av projektaktiviteter. Du måste skapa minst en projektaktivitet per projekt eftersom all bokföring refererar till en projektaktivitet. Med åtminstone en projektaktivitet i ditt projekt kan du lägga upp projektplaneringsrader och bokföra förbrukningen i projektet.

Det andra lagret består av projektplaneringsrader som specificerar detaljerad förbrukning av resurser, artiklar och diverse redovisningskostnader.

Lagerstrukturen gör att du kan dela upp projekt i mindre aktiviteter och specificera budget, offerter och registrering mer i detalj. Dessutom att du får en inblick i hur ett projekt fortlöper. Du kan till exempel spåra om du uppfyller uppsatta milstolpar eller om du är i linje med mål för att uppfylla budget.

> [!NOTE]  
>   Åtgärden **Nytt projekt** på Rollcentret **Projektchef** startar en guidad hjälp som guidar dig genom stegen för att skapa ett projekt med integrerade uppgifter och planeringsrader. Efterföljande procedur beskriver hur du utför stegen manuellt.

## <a name="to-create-a-job-card"></a>Så här skapar du ett projektkort.
Du skapar ett projektkort och sedan skapar projektaktivitetsrader och projektplaneringsrader för det.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Projekt** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om du vill ange projektet med information om andra projekt väljer du åtgärden **Kopiera projekt**, fyller i fälten efter behov och väljer sedan knappen **OK**.

> [!NOTE]  
>   Om du använder tidrapporter i projektet måste du också ange en person som ansvarar. Denna person kan godkänna tidrapporter för anställdas aktiviteter som är kopplade till projektet. Mer information finns i [Skapa tidrapporter](projects-how-setup-time-sheets.md).

## <a name="to-create-tasks-for-a-job"></a>Skapa aktiviteter för ett projekt
En viktig del när du skapar ett projekt är att ange de olika aktiviteter som ingår i projektet. Du gör detta genom att lägga till nya rader i snabbfliken **Uppgifter** i fönstret **Projektkort**, en aktivitet per rad. Varje projekt måste ha minst en aktivitet.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Projekt** och välj sedan relaterad länk.
2. Öppna projektkortet för ett relevant projekt.
3. På snabbfliken **Uppgifter** fyller du i fälten efter behov på en ny rad.
4. Om du vill dra in uppgifter och skapa en hierarki väljer du åtgärden **Uppgifter** och sedan väljer du åtgärden **Indrag för projektaktiviteter**.
5. Upprepa steg 3 och 4 för alla de aktiviteter som du behöver för projektet.
6. Om du vill ange projektaktiviteter med information om andra projektaktiviteter väljer du åtgärden **Kopiera projektaktiviteter från**, fyller i fälten efter behov och väljer sedan knappen **OK**.

## <a name="to-create-planning-lines-for-a-job"></a>Så här skapar du en planeringsrad för ett projekt
Du kan förfina dina nya projektaktiviteter på projektplaneringsrader. En planeringsrad kan används för att samla in den information som du vill spåra för ett projekt. Med planeringsrader kan du lägga till information som vilka resurser som behövs eller för att samla in vilka artiklar som behövs för att utföra projektet. Du kan till exempel ha en aktivitet för att inhämta kundens godkännande av ett projekt, du kan associera den aktiviteten med planeringsrader för objekt som att träffa kunden och tilldela en resurs.  

En projektplaneringsrad kan ha en av följande typer.  

| Kontakttyp | Beskrivning |
| --- | --- |
| **Budget** |Anger uppskattad förbrukning och kostnader för projektet, vanligtvis i tids- och materialtypsprojekt. Planeringsrader av den här typen kan inte faktureras. |
| **Fakturerbart** |Anger uppskattad fakturering till kunden, vanligtvis som ett fastprisprojekt. |
| **Både Budget och Fakturerbart** |Anger budgeterad förbrukning som motsvarar vad du vill fakturera. |

**Obs**. När du anger information på projektplaneringsrader fylls kostnadsinformationen i automatiskt. T.ex. baseras kostnaden, priset och rabatten för resurser och artiklar inledningsvis på informationen som definieras på resurs- och artikelkort.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Projekt** och välj sedan relaterad länk.
2. Öppna ett relevant projektkort.
3. Markera ett projekt där fältet **Typ av projektaktivitet** innehåller **Bokföring** och klicka sedan på åtgärden **Projektplaneringsrader**.  
4. I fönstret **Projektplaneringsrader**, på en ny rad, fyller du i fält efter behov.
5. Upprepa steg 3 och 4 för alla de planeringsrader som du behöver för projektaktiviteten.

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)      
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

