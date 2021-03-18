---
title: Definiera och fördela kostnader | Microsoft Docs
description: Kostnadsfördelning flyttar kostnader och intäkter mellan kostnadstyper, kostnadsställen och kostnadsbärare. Du kan definiera valfritt antal fördelningar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9d4167751289b26926bdde3148d6f2241df787cf
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388605"
---
# <a name="defining-and-allocating-costs"></a>Definiera och fördela kostnader
Kostnadsfördelning flyttar kostnader och intäkter mellan kostnadstyper, kostnadsställen och kostnadsbärare. Du kan definiera valfritt antal fördelningar. Varje fördelning består av:  

-   En fördelningskälla.  
-   Ett eller flera fördelningsmål.  

Fördelningskällan bestämmer vilka kostnader som måste fördelas, och fördelningsmålen bestämmer var kostnader måste fördelas. Till exempel kan en fördelningskälla vara kostnaderna för kostnadstypen Uppvärmning. Du tilldelar alla uppvärmningskostnader till tre kostnadsställen: Seminarium, Produktion och Försäljning. Dessa kostnadsställen är dina fördelningsmål.  

För varje fördelningskälla definierar du en fördelningsnivå, en giltighetsperiod och en variant som grupp-id. Du kan använda ett batch-jobb för att definiera filter för att välja fördelningsdefinitioner och sedan köra kostnadsfördelningar automatiskt.  

För varje fördelningsmål definierar du en fördelningsbas. Fördelningsbasen kan antingen vara statisk eller dynamisk.  

-   Statisk fördelning är baserad på ett visst värde, till exempel kvadratmetrar eller en fastställd fördelningskvot, till exempel 5:2:4.  
-   Dynamiska fördelningsbaser beror på värden som kan ändras, t.ex hur många anställda i ett kostnadsställe eller försäljningsintäkten för en kostnadsbärare under en viss tidsperiod.  

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

## <a name="setting-up-allocation-source-and-targets"></a>Ställa in fördelningskälla och mål
Varje fördelning består av en fördelningskälla och en eller flera fördelningsmål. Fördelningskällan bestämmer vilka kostnader som ska fördelas. Fördelningsmålen bestämmer vart kostnaderna ska fördelas.  

### <a name="to-set-up-cost-allocations"></a>Så här lägger du upp kostnadsfördelningar  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kostnadsfördelning** och välj sedan relaterad länk.  
2.  På sidan **Kostnadsfördelning** väljer du åtgärden **Redigera**.  
3.  Ange ett ID för fördelningskällan i fältet **ID**.  
4.  Definiera en nivå som ett tal mellan 1 och 99 i fältet **Nivå**. Fördelningsbokföringen följer ordningen på nivåerna.  
5.  Ange en kostnadstyp för att definiera vilka kostnadstyper som fördelas i fältet **Kostnadstypsintervall**. Om samtliga kostnader för en kostnadstyp har fördelats definieras inget intervall.  
6.  Ange ett kostnadsställe tillsammans med kostnader som ska fördelas i fältet **Kod för kostnadsställe**.  
7.  Ange en kostnadsbärar tillsammans med kostnader som ska fördelas i fältet **Kod för kostnadsbärare**. Oftast är detta fält tomt eftersom kostnadsbärare sällan fördelas till andra kostnadsbärare.  
8.  Ange en kostnadstyp i fältet **Kreditera till kostnadstyp**. Kostnaderna som fördelas krediteras till ursprungskostnadstypen. Kredittransaktionen ska bokföras med kostnadstypen som anges här.  
9. Du definierar fördelningsmål på snabbfliken **Rader**. Ange en kostnadstyp på första raden i fältet **Målkostnadstyp**. Det definierar vilken kostnadstyp som fördelningen debiteras på.  
10. Ange den första raden, ange det första fördelningsmålet i fälten **Målkostnadsställe** eller **Målkostnadsobjekt**. De två fälten definierar vilket kostnadsställe eller vilken kostnadsbärare fördelningen debiteras på. Du kan endast fylla i ett av dessa fält, inte båda.  
11. Upprepa samma steg på den andra raden för att skapa ytterligare fördelningsmål.  
12. När du har angett fördelningsmålet och källorna väljer du åtgärden **Beräkna fördelningsnyckel** om du vill beräkna de totala andelsvärdena.  

> [!NOTE]  
>  Markera kryssrutan **Spärrad** om du vill inaktivera fördelningskonfigurationen.

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Skapa filter för dynamiska fördelningsbaser
Den dynamiska fördelningsmetoden bygger på värden som kan ändras. Till exempel antalet anställda i ett kostnadsställe eller artiklar som säljs på en kostnadsbärare för en viss tidsperiod. Det finns nio fördefinierade fördelningsbaser och tolv dynamiska datumintervall. Du kan ange olika filter baserade på fördelningsbasen.  

### <a name="setting-filters-for-dynamic-allocation-bases"></a>Skapa filter för dynamiska fördelningsbaser  
 Följande tabell visar vilka filter är möjliga för olika fördelningsbaser och vilka värden som gäller i fälten **Nummerfilter** och **Gruppfilter**. Tryck på F1 i fälten **Kod för datumfilter** om du vill läsa detaljerad beskrivningar.  

|**Bas**|**Nummerfilter**|**Kod för datumfilter**|**Filter för kostnadsställe**|**Filter för kostnadsbärare**|**Gruppfilter**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Redovisningstransaktioner|Redovisningskonto|Ja|Ja|Ja|Inte tillämpligt|  
|Redov.budgettransaktioner|Redovisningskonto|Ja|Ja|Ja|Redov.budgetnamn|  
|Kostnadstypstransaktioner|Kostnadstyp|Ja|Ja|Ja|Inte tillämpligt|  
|Kostnadsbudgettransaktioner|Kostnadstyp|Ja|Ja|Ja|Budgetnamn|  
|Antal anställda|Inte tillämpligt|Ja|Ja|Ja|Inte tillämpligt|  
|Sålda artiklar (antal)|Artikelnr|Ja|Ja|Ja|Lagerbokföringsmall|  
|Inköpta artiklar (antal)|Artikelnr|Ja|Ja|Ja|Lagerbokföringsmall|  
|Sålda artiklar (belopp)|Artikelnr|Ja|Ja|Ja|Lagerbokföringsmall|  
|Inköpta artiklar (belopp)|Artikelnummer|Ja|Ja|Ja|Lagerbokföringsmall|

## <a name="scenario-1-defining-static-allocations-based-on-allocation-ratio"></a>Scenario 1: Definiera fast distribution beräknad på fördelningskvot
Statisk fördelning är baserad på ett visst värde, till exempel kvadratmeter eller en fastställd fördelningskvot, till exempel 5:2:4.  

I det här avsnittet beskrivs hur du definierar tre nya kostnadsbärare som är fördelningsmål för fördelningskällan PROD-kostnadsstället med hjälp av den etablerade fördelningskvoten 5:2:4. De tre målkostnadsbärarna är ACCESSO, PAINT och FITTINGS.  

> [!NOTE]  
>  Exemplet använder demonstrationsdata i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Så här definierar du fördelningskällan PROD-kostnadsstället på snabbfliken Allmänt  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kostnadsfördelning** och välj sedan relaterad länk.  
2.  På sidan **Kostnadsfördelning** väljer du åtgärden **Ny**.  
3.  I fältet **ID**, tryck på Retur eller ange ett id.  
4.  Ange **1** i fältet **Nivå**.  
5.  I fälten **Giltig från** och **Giltig till** anger du datum.  
6.  Ange **PROD** i fältet **Kod för kostnadsställe**.  
7.  I fältet **Kreditera till kostnadstyp** anger du kostnadstyp **9903**.  

### <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Då här definierar du kostnadsbärarna som är fördelningsmål på snabbfliken Rader  

1.  Ange **9903** i fältet **Målkostnadstyp** på den första raden.  
2.  Välj **ACCESSO** i fältet **Målkostnadsobjekt** på den första raden.  
3.  På den första raden, i fältet **Typ av fördelningsmål**, välj **Alla kostnader** för att definiera hur upplupna kostnader ska fördelas.  
4.  På den första raden, i fältet **Bas**, markera **Fast** för att använda fast fördelning.  
5.  På den första raden, i fältet **Del**, ange fördelningssatsen **5**.  
6.  Ange **9903** i fältet **Målkostnadstyp** på den andra raden.  
7.  Välj **PAINT** i fältet **Målkostnadsobjekt** på den andra raden.  
8.  På den andra raden, i fältet **Typ av fördelningsmål**, välj **Alla kostnader** för att definiera hur upplupna kostnader ska fördelas.  
9. På den andra raden, i fältet **Bas**, markera **Fast** för att använda fast fördelning.  
10. På den andra raden, i fältet **Del**, ange fördelningssatsen **2**.  
11. Ange **9903** i fältet **Målkostnadstyp** på den andra raden.  
12. Välj **FITTINGS** i fältet **Målkostnadsobjekt** på tredje raden.  
13. På tredje raden, i fältet **Typ av fördelningsmål**, välj **Alla kostnader** för att definiera hur upplupna kostnader ska fördelas.  
14. På tredje raden, i fältet **Bas**, markera **Fast** för att använda fast fördelning.  
15. På tredje raden, i fältet **Del**, ange fördelningssatsen **4**.  

> [!IMPORTANT]  
>  [!INCLUDE[prod_short](includes/prod_short.md)] beräknar automatiskt fältet **Procent** med hjälp av ett procenttal som är beroende av alla tre fördelningskvoterna, som anges i fältet **Del** för alla tre rader.

## <a name="scenario-2-defining-dynamic-allocations-based-on-items-sold"></a>Scenario 2 – Definiera dynamisk distribution beräknad på sålda artiklar
I det här avsnittet innehåller exempel på hur du definierar fördelningar med dynamisk fördelning. I exemplet ändrar du dynamisk fördelning av kostnaderna för de SALES-kostnadsstället för att det ska fungera med den nya kostnadsbäraren IT EQUIPMENT. IT EQUIPMENT-paketet har artikelnummer i intervallet 8904-W till 8924-W. Du kan använda föregående års försäljningssiffror för att beräkna antalet andelen. Fördelningen bokförs på hjälpkostnadstypen 9903.  

> [!NOTE]  
>  Exemplet använder demonstrationsdata i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Så här definierar du dynamisk fördelning beräknad på sålda artiklar under föregående år  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kostnadsfördelning** och välj sedan relaterad länk.  
2.  På sidan **Kostnadsfördelning** väljer du åtgärden **Ny**.  
3.  I fältet **ID**, tryck på Retur eller ange ett id.  
4.  Ange **1** i fältet **Nivå**.  
5.  I fälten **Giltig från** och **Giltig till** anger du datum.  
6.  Ange **FÖRS** i fältet **Kod för kostnadsställe**.  
7.  I fältet **Kreditera till kostnadstyp** anger du kostnadstyp **9903**.  
8.  I fältet **Målkostnadstyp** anger du kostnadstyp **9903**.  
9. I fältet **Målkostnadsobjekt** välj **Ny** för att skapa den nya kostnadsbäraren IT EQUIPMENT och fyll i fälten efter behov. Välj **IT EQUIPMENT**. Låt fältet **Målkostnadsställe** vara tomt.  
10. I fältet **Typ av fördelningsmål**, välj **Alla kostnader** för att definiera hur upplupna kostnader ska fördelas.  
11. I fältet **Bas** välj fördelningsbasen **Sålda artikler (belopp)**.  
12. I fältet **Nummerfilter** anger du **8904-W..8924-W**.  
13. I fältet **Kod för datumfilter** anger du **Föregående år**.  
14. Välj åtgärden **Beräkna fördelningsnyckel** för att beräkna andelen.  

> [!IMPORTANT]  
>  [!INCLUDE[prod_short](includes/prod_short.md)] använder föregående år försäljningssiffror för att beräkna en andel för 1596,50 BVA till 100 procent för IT EQUIPMENT-paketet. Det innebär att alla sålda artiklar föregående år är fördelade på kostnadsbäraren IT EQUIPMENT.

## <a name="see-also"></a>Se även  
 [Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md)   
 [Överföra och bokföra kostnadstransaktioner](finance-transfer-and-post-cost-entries.md)   
 [Redovisa kostnader](finance-manage-cost-accounting.md)   
 [Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md)   
 [Om kostnadsredovisning](finance-about-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]