---
title: "Definiera koder för standardtjänster | Microsoft Docs"
description: "Lär dig mer om att lägga upp koder för serviceaktiviteter som du utför ofta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bca816da5473ea3f5f8eab892125e32a045ffec3
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-standard-service-codes"></a>Skapa standardtjänstekoder
När du utför en vanlig typ av service behöver du ofta skapa servicedokument som använder servicerader som innehåller liknande information. Om du vill göra det enklare att skapa de här raderna, lägger du in standardtjänstkoder som har en fördefinierad grupp med servicerader. Raderna infogas automatiskt när du väljer koden i ett servicedokument. Du kan ställa in ett antal standardtjänstekoder, och varje kod kan ha ett obegränsat antal servicerader av olika typer, inklusive artikel, resurs, kostnad eller standardtext kopplade till sig. Du skapar servicerader för varje standardtjänstkod på kortet **standardtjänstkod**. Du kan sedan tilldela standardtjänstkoderna till serviceartikelgrupper på sidan **Standardgruppkoder för serviceartiklar**. Senare när du skapar ett servicedokument kan du använda åtgärden **få standardtjänstkoder** för att lägga till serviceraderna.  
  
> [!Tip]
>  Du kan använda samma begrepp för att skapa rader i försäljnings- och inköpsdokument. Mer information finns i [Skapa återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md).    
  
## <a name="to-set-up-a-standard-service-code"></a>Så här skapar du standardtjänstkoder    
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Standardservicekoder**, och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Fyll i serviceraderna som är kopplade till den här servicekoden.  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a>Så här tilldelar du en standardtjänstkod till en serviceartikelgrupp
1. Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Serviceartikelgrupper** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Fyll i serviceraderna som är kopplade till den här servicekoden.  

## <a name="see-also"></a>Se även
[Servicehantering](service-service.md)
