---
title: Så här skapar du artikelinförslar från Intern artikelinförsel | Microsoft Docs
description: När artiklar har förts in och innan de plockas till en produktionsorder eller utleverans, förvaras de i distributionslagret som en del av det disponibla lagersaldot.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5095b4dde92b2d6982bfc8a984f10f5b62454800
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756248"
---
# <a name="pick-and-put-away-without-a-source-document"></a>Plocka och lagra utan källdokument
När artiklar har förts in och innan de plockas till en produktionsorder eller utleverans, förvaras de i distributionslagret som en del av det disponibla lagersaldot.  

Det kan uppstå situationer då artiklar måste tas ut från distributionslagrets lagerställen tillfälligt, kanske för att ta som modeller i försäljningspresentationer. Dessa artiklar ägs fortfarande av företaget och ingår i lager, men de är inte tillgängliga för plockning. De registreras på ett en speciell lagerplats som du skapar för det här ändamålet. Tekniskt är artiklar i lagret, men fysiskt, kan de vara i ett konferens- eller demonstrationsdatabasen.  

Det kan även vara så att produktionsenheten plötsligt behöver några artiklar i en tillverkningsprocess. Du kan plocka artiklar till produktionslagerställen med hjälp av internplockning. När processen är klar och utflöde har skapats bokför du förbrukningen av artiklarna och tömmer produktionslagerstället, vilket i sin tur minskar artikelkvantiteten på lagerstället.  

På samma sätt kan artiklar returneras till distributionslagret för artikelinförsel. Artiklarna kan ha tagits ut från det disponibla lagret till en produktionsorder, och sedan inte använts alls. Om du vill att de ska ingå i det tillgängliga lagret igen måste de föras in på lagerstället.  

**Interna artikelinförslar** låter dig utföra artikelinförsel utan att referera till ett visst källdokument. Du kan enkelt ange all information som du behöver för att skapa en plockning eller artikelinförsel.  

> [!NOTE]  
>  Om du inte använder intern plockning och intern artikelinförsel kan du utföra de här justeringarna genom att flytta artiklar från en lagerplats till en annan eller bokföra ändringar av antal för en lagerplats.  
>   
>  När lagerstället använder dirigerad artikelinförsel och plockning, och därmed också lagerplatstyper, kan du inte manuellt flytta artiklar in och ut ur en lagerplats av typen INLEV. Detta beror på att artiklar som finns i en lagerplats av INLEV.-typ måste registreras som införda innan de blir en del av det tillgängliga lagret.  

## <a name="to-create-an-internal-pick"></a>Skapa en intern plockning  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lager intern plockning** och välj sedan relaterad länk.  
2.  Fyll i fälten **Nr.** och fältet **Till lagerställeskod** på snabbfliken **Allmänt**. Fältet **Till lagerställeskod** anger den lagerplats som du vill hämta artiklar från. För produktion skulle den här lagerstället vara den inkommande produktionslagerstället eller den öppna fabrikslagerstället. För andra typer av aktiviteter väljer du Till lagerställeskod för en lagerplatstyp som inte används för plockning, troligtvis en etapplagerplats, leveranslagerplats eller speciallagerplats.  
3.  Välj en artikel i fältet **Artikelnr** och fyll i den kvantitet som du vill plocka.  
4. Välj åtgärden **Skapa plockning**. En plockinstruktion är nu klar att utföras av lagerpersonalen.  

## <a name="to-create-an-internal-put-away"></a>Skapa en intern art.införsel  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lager intern art.införsel** och välj sedan relaterad länk.  
2.  Fyll i fälten **Nr.** och fälten **Från lagerställeskod** på snabbfliken **Allmänt**. Fältet **Från lagerställeskod** anger den lagerplats där de artiklar finns som returneras till lagret, kanske från produktionen.  
3.  Fyll i artikelnumren och kvantiteterna på raderna.  
4.  Välj åtgärden **Skapa artikelinförsel**. En artikelinförselinstruktion är nu klar att utföras av lagerpersonalen.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
