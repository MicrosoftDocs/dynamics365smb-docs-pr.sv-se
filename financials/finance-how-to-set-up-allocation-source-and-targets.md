---
title: "Så här: ställa in fördelningskälla och mål | Microsoft Docs"
description: "Varje fördelning består av en fördelningskälla och en eller flera fördelningsmål. Fördelningskällan bestämmer vilka kostnader som ska fördelas. Fördelningsmålen bestämmer vart kostnaderna ska fördelas."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 1aa37745b232ec2535fe8060330d0bc7442dca3d
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-allocation-source-and-targets"></a>Så här: ställa in fördelningskälla och mål
Varje fördelning består av en fördelningskälla och en eller flera fördelningsmål. Fördelningskällan bestämmer vilka kostnader som ska fördelas. Fördelningsmålen bestämmer vart kostnaderna ska fördelas.  

## <a name="to-set-up-cost-allocations"></a>Så här lägger du upp kostnadsfördelningar  
1.  Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kostnadsfördelning** och väljer sedan relaterad länk.  
2.  I fönstret **Kostnadsfördelning** väljer du åtgärden **Redigera**.  
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

## <a name="see-also"></a>Se även  
[Redovisa kostnader](finance-manage-cost-accounting.md)  
 [Skapa filter för dynamiska fördelningsbaser](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Scenarioexempel: Definiera fast distribution beräknad på fördelningskvot](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)   
 [Scenarioexempel: Definiera dynamisk distribution beräknad på sålda artiklar](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Definiera och fördela kostnader](finance-define-and-allocate-costs.md)   
 [Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

