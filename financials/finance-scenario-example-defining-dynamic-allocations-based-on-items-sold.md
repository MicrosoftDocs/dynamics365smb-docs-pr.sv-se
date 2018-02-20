---
title: "Scenarioexempel - Definiera dynamisk distribution beräknad på sålda artiklar | Microsoft Docs"
description: "I det här avsnittet innehåller exempel på hur du definierar fördelningar med dynamisk fördelning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d8622d11cd23e506d1b85b18dbe5facb740c7753
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a>Scenarioexempel: Definiera dynamisk distribution beräknad på sålda artiklar
I det här avsnittet innehåller exempel på hur du definierar fördelningar med dynamisk fördelning. I exemplet ändrar du dynamisk fördelning av kostnaderna för de SALES-kostnadsstället för att det ska fungera med den nya kostnadsbäraren IT EQUIPMENT. IT EQUIPMENT-paketet har artikelnummer i intervallet 8904-W till 8924-W. Du kan använda föregående års försäljningssiffror för att beräkna antalet andelen. Fördelningen bokförs på hjälpkostnadstypen 9903.  

> [!NOTE]  
>  Exemplet använder demonstrationsdata i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Så här definierar du dynamisk fördelning beräknad på sålda artiklar under föregående år  

1.  Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kostnadsfördelningar** och välj sedan relaterad länk.  
2.  I fönstret **Kostnadsfördelning** väljer du åtgärden **Ny**.  
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
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)]  använder föregående år försäljningssiffror för att beräkna en andel för 1596,50 BVA till 100 procent för IT EQUIPMENT-paketet. Det innebär att alla sålda artiklar föregående år är fördelade på kostnadsbäraren IT EQUIPMENT.  

## <a name="see-also"></a>Se även  
 [Skapa filter för dynamiska fördelningsbaser](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Skapa fördelningskälla och mål](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Definiera och fördela kostnader](finance-define-and-allocate-costs.md)   
 [Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md)   
 [Om kostnadsredovisning](finance-about-cost-accounting.md)

