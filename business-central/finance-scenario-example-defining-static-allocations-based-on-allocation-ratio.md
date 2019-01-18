---
title: "Definiera fast distribution beräknad på fördelningskvot | Microsoft Docs"
description: "Statisk fördelning är baserad på ett visst värde, till exempel kvadratmeter eller en fastställd fördelningskvot, till exempel 5:2:4."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: d35fd5de7a0583c3864268d0749384322bf947ed
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a>Scenarioexempel: Definiera fast distribution beräknad på fördelningskvot
Statisk fördelning är baserad på ett visst värde, till exempel kvadratmeter eller en fastställd fördelningskvot, till exempel 5:2:4.  

I det här avsnittet beskrivs hur du definierar tre nya kostnadsbärare som är fördelningsmål för fördelningskällan PROD-kostnadsstället med hjälp av den etablerade fördelningskvoten 5:2:4. De tre målkostnadsbärarna är ACCESSO, PAINT och FITTINGS.  

> [!NOTE]  
>  Exemplet använder demonstrationsdata i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Så här definierar du fördelningskällan PROD-kostnadsstället på snabbfliken Allmänt  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kostnadsfördelning** och välj sedan relaterad länk.  
2.  På sidan **Kostnadsfördelning** väljer du åtgärden **Ny**.  
3.  I fältet **ID**, tryck på Retur eller ange ett id.  
4.  Ange **1** i fältet **Nivå**.  
5.  I fälten **Giltig från** och **Giltig till** anger du datum.  
6.  Ange **PROD** i fältet **Kod för kostnadsställe**.  
7.  I fältet **Kreditera till kostnadstyp** anger du kostnadstyp **9903**.  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Då här definierar du kostnadsbärarna som är fördelningsmål på snabbfliken Rader  

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
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] beräknar automatiskt fältet **Procent** med hjälp av ett procenttal som är beroende av alla tre fördelningskvoterna, som anges i fältet **Del** för alla tre rader.  

## <a name="see-also"></a>Se även  
[Definiera och fördela kostnader](finance-define-and-allocate-costs.md)   

