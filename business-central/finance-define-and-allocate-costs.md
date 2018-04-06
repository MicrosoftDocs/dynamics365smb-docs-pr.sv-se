---
title: "Definiera och fördela kostnader | Microsoft Docs"
description: "Kostnadsfördelning flyttar kostnader och intäkter mellan kostnadstyper, kostnadsställen och kostnadsbärare. Du kan definiera valfritt antal fördelningar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7bdddcadf3fb7dceb762354e8fa527158782b676
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

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

|Till|Gå till|  
|--------|---------|  
|Skapa fördelningskälla och dess mål.|[Skapa fördelningskälla och mål](finance-how-to-set-up-allocation-source-and-targets.md)|  
|Skapa olika filter för dynamiska fördelningsbaser.|[Skapa filter för dynamiska fördelningsbaser](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|Visa ett exempel på hur du definierar en fast distribution.|[Scenarioexempel: Definiera fast distribution beräknad på fördelningskvot](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|Visa ett exempel på hur du definierar en dynamisk distribution.|[Scenarioexempel: Definiera dynamisk distribution beräknad på sålda artiklar](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a>Se även  
 [Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md)   
 [Överföra och bokföra kostnadstransaktioner](finance-transfer-and-post-cost-entries.md)   
 [Redovisa kostnader](finance-manage-cost-accounting.md)   
 [Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md)   
 [Om kostnadsredovisning](finance-about-cost-accounting.md)

