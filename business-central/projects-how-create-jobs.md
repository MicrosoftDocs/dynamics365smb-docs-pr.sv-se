---
title: Skapa ett projektkort för ett projekt och ange aktiviteter
description: För ett nytt projekt kan du skapa ett projektkort med projektaktiviteterna och planeringsrader för att hantera hur och budgetar.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management, task
ms.search.form: 88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6996c82ee184db980879ea98a6f2cbdca1b10852
ms.sourcegitcommit: 55f42d2407e109b4924218cb22129467b53deb08
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557199"
---
# <a name="create-jobs"></a>Skapa projekt
När du vill starta ett nytt projekt måste du skapa ett projektkort med inbyggda projektaktiviteter och projektplaneringsrader, strukturerade i två lager.  

Det första lagret består av projektaktiviteter. Du måste skapa minst en projektaktivitet per projekt eftersom all bokföring refererar till en projektaktivitet. Med åtminstone en projektaktivitet i ditt projekt kan du lägga upp projektplaneringsrader och bokföra förbrukningen i projektet.

Det andra lagret består av projektplaneringsrader som specificerar detaljerad förbrukning av resurser, artiklar och diverse redovisningskostnader.

Lagerstrukturen gör att du kan dela upp projekt i mindre aktiviteter och specificera budget, offerter och registrering mer i detalj. Dessutom att du får en inblick i hur ett projekt fortlöper. Du kan till exempel spåra om du uppfyller uppsatta milstolpar eller om du är i linje med mål för att uppfylla budget.

> [!TIP]
> Välj åtgärden **Nytt projekt** på Rollcentret **Projektchef** för att starta en assisterad inställningsguide som tar dig genom stegen för att skapa ett projekt med integrerade uppgifter och planeringsrader. Efterföljande procedur beskriver hur du utför stegen manuellt. Ett exempel på hur du skapar ett projekt manuellt finns i [Video: hur du skapar ett projekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

Ibland är den part som tar emot en service inte densamma som den part som betalar räkningen. På sidan **Projekt** kan du ange kunden som kommer att dra nytta av projektet i **Sälja till** och parten som ska faktureras i **Fakturera till**. Du kan även ange följande information: 

* Var arbetet sker genom att välja från en lista över leveransadress för kunden.
* Lägga till information om externa referenser för att förenkla kommunikationen med projektet.
* Skriv över projektets standard ekonomiska villkor.

## <a name="to-create-a-job-card"></a>Så här skapar du ett projektkort.
Du skapar ett projektkort och sedan skapar projektaktivitetsrader och projektplaneringsrader för det.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om du vill ange projektet med information om andra projekt väljer du åtgärden **Kopiera projekt**, fyller i fälten efter behov och väljer sedan knappen **OK**.

> [!NOTE]  
>   Om du använder tidrapporter i projektet måste du också ange en person som ansvarar. Denna person kan godkänna tidrapporter för anställdas aktiviteter som är kopplade till projektet. Mer information finns i [Skapa tidrapporter](projects-how-setup-time-sheets.md).

## <a name="to-create-tasks-for-a-job"></a>Skapa aktiviteter för ett projekt
En viktig del när du skapar ett projekt är att ange de olika aktiviteter som ingår i projektet. Du anger uppgifter genom att skapa en rad per uppgift på snabbfliken **Uppgifter** på sidan **Projektkort**. Varje projekt måste ha minst en aktivitet.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.
2. Öppna projektkortet för ett relevant projekt.
3. På snabbfliken **Uppgifter** fyller du i fälten efter behov på en ny rad.
4. Om du vill dra in uppgifter och skapa en hierarki väljer du åtgärden **Uppgifter** och sedan väljer du åtgärden **Indrag för projektaktiviteter**.
5. Upprepa steg 3 och 4 för alla de aktiviteter som du behöver för projektet.
6. Om du vill ange projektaktiviteter med information om andra projektaktiviteter väljer du åtgärden **Kopiera projektaktiviteter från**, fyller i fälten efter behov och väljer sedan knappen **OK**.

## <a name="to-create-planning-lines-for-a-job"></a>Så här skapar du en planeringsrad för ett projekt
Du kan förfina dina nya projektaktiviteter på projektplaneringsrader. En planeringsrad kan används för att samla in den information som du vill spåra för ett projekt. Du kan t.ex. spåra de resurser som krävs av projektet eller vilka artiklar som behövs. Du har till exempel en uppgift för att få en kund att godkänna ett projekt. Du kan associera den aktiviteten med planeringsrader för objekt som att träffa kund och tilldela en resurs.  

En projektplaneringsrad kan ha en av följande typer.  

| Kontakttyp | Beskrivning |
| --- | --- |
| **Budget** |Anger uppskattad förbrukning och kostnader för projektet, vanligtvis i tids- och materialtypsprojekt. Planeringsrader av den här typen kan inte faktureras. |
| **Fakturerbart** |Anger uppskattad fakturering till kunden, vanligtvis som ett fastprisprojekt. |
| **Både Budget och Fakturerbart** |Anger budgeterad förbrukning som motsvarar vad du vill fakturera. |

> [!NOTE]
> När du anger information på projektplaneringsrader fylls kostnadsinformationen i automatiskt. t. ex. baseras kostnaden, priset och rabatten för resurser och artiklar inledningsvis på informationen som definieras på resurs och artikel. 

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.
2. Öppna ett relevant projektkort.
3. Markera ett projekt där fältet **Typ av projektaktivitet** innehåller **Bokföring** och klicka sedan på åtgärden **Projektplaneringsrader**.  
4. På sidan **Projektplaneringsrader**, på en ny rad, fyller du i fält efter behov.
5. Upprepa steg 3 och 4 för alla de planeringsrader som du behöver för projektaktiviteten.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-job"></a>Skapa dokument för lager och distributionslagerplockning för ett jobb
Om du vill skapa dokument för lager och distributionslagerplockning för projekt måste administratören aktivera **Funktionsuppdatering: Aktivera lager- och distributionslagerplockning från projekt** på sidan **funktionshantering**.

Funktionen lägger till åtgärden **Skapa lagerplockning** och **Skapa distributionslagerplockning** på **projektkortet**. Om du vill skapa eller registrera ett plocknings dokument använder du **Artikelinförsel/plockningsrader/transportrader** eller **registrerade plockningsrader**.

Du kan använda åtgärder på följande villkor:
* **Status** för projektet är **öppen**.
* **Radtypen** för projektplaneringsraden är **budget** , eller **både budget och fakturerbar**. 
* **Typen** av projektplaneringsrad är **artikel**.
* **Begär plockning** har aktiverats för den relaterade platsen.
* **Dirigerad art.inf. och plock.** är inaktiverad.

> [!NOTE] 
> Även om inställningen har anropats **kräver plockning** kan du fortfarande bokföra förbrukning direkt från projektjournalraden för lagerstället. När lagerstället har konfigurerats så att plockning krävs men inte leverans, använder du sidan **Lagerplockning** för att organisera och skriva ut plockinformationen. Du kan också använda sidan för att registrera och bokföra resultatet av plockningen, som i sin tur bokför förbrukningen av artiklarna. 
> 
> Om din plats är inställd för att kräva både plockning och leveransbearbetning, vilket innebär att du har valt både **Begär plockning** och **Begär utleverans** på sidan **Platskort** använd **Dist.lager plockning** för att hantera plockningen. Distributionslagerplockningar liknar lagerplockningar. Skillnaden är att istället för att bokföra plockningsinformationen registrerar du plockningen. Registreringen bokförs inte i förbrukningen, utan bara artiklarna kan bokföras. Du lagerchef kan du använda ett plockningskalkylark för att organisera plockninginformation innan du skapar de individuella plockningsinstruktionerna för lager

## <a name="see-also"></a>Se även

[Projekthantering](projects-manage-projects.md)  
[Video: Hur du skapar du ett projekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]