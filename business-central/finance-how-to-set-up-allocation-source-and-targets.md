---
title: "Så här: ställa in fördelningskälla och mål | Microsoft Docs"
description: "Varje fördelning består av en fördelningskälla och en eller flera fördelningsmål. Fördelningskällan bestämmer vilka kostnader som ska fördelas. Fördelningsmålen bestämmer vart kostnaderna ska fördelas."
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
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0f49faba7360ccf2e93ab62176752a503335f3f1
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-allocation-source-and-targets"></a>Skapa fördelningskälla och mål
Varje fördelning består av en fördelningskälla och en eller flera fördelningsmål. Fördelningskällan bestämmer vilka kostnader som ska fördelas. Fördelningsmålen bestämmer vart kostnaderna ska fördelas.  

## <a name="to-set-up-cost-allocations"></a>Så här lägger du upp kostnadsfördelningar  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kostnadsfördelning** och välj sedan relaterad länk.  
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

