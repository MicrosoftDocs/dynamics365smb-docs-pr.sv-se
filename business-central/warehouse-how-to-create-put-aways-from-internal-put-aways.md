---
title: Skapa artikelinförslar från intern artikelinförsel
description: I det här avsnittet beskrivs hur du plockar och inför artikelinförsel utan källdokument, hur du skapar en intern plockning och hur du skapar en intern artikelinförsel.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 7354, 7356, 7357, 7358, 7359, 7361
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: f812b988c0cb48cd49890c20ab59a8095327c52f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512582"
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
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Dist.lager intern plockning** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. Fyll i fälten **Nr.** fältet **Lagerställekod** och fältet **Till lagerplatskod** på snabbfliken **Allmänt**. Fältet **Till lagerställeskod** anger den lagerplats där du vill placera plockade artiklar. För produktion skulle den här lagerstället vara den inkommande produktionslagerstället eller den öppna fabrikslagerstället. För andra typer av aktiviteter väljer du en lagerplatskod för en lagerplatstyp som inte används för plockning, troligtvis en etapplagerplats, leveranslagerplats eller speciallagerplats.  
4.  Välj en artikel i fältet **Artikelnr** och fyll i den kvantitet som du vill plocka.  
5. Välj åtgärden **Skapa plockning**. En plockinstruktion är nu klar att utföras av lagerpersonalen. Alternativt kan du välja åtgärden **Frisläppning** och skapa distributionslagerplockningar med hjälp av **Plockförslaget**. Mer information finns i [Planera plockningar i förslag](warehouse-how-to-plan-picks-in-worksheets.md)

## <a name="to-create-an-internal-put-away"></a>Skapa en intern art.införsel  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Dist.lager intern art.införsel** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. Fyll i huvudet på en ny intern artikelinförsel med åtminstone **Nr.** och **Lagerställekod**.
4. Fyll i en rad för varje artikel som du vill flytta till distributionslagerstället. Du behöver endast fylla i fälten **Artikelnr** och **Antal**.

  > [!NOTE]  
  > När du väljer fältet **Artikelnr.** öppnas **Lista för lagerplatsinnehåll** istället för **Artikellistan**. Detta beror på att du vill föra in en artikel som finns på en viss lagerplats – ett *lagerplatsinnehåll* – och inte bara en artikel, och du vet redan vilken lagerplats som artikeln ska tas ifrån.  <!--If you filled in **From Bin Code** in the header, the bin content will be filtered by value defined in the **From Bin Code**.-->
5. Om du vill fylla raderna med hela lagerplatsinnehållet eller det filtrerade lagerplatsinnehållet från lagerplatser på platsen, väljer du åtgärden **Hämta lagerplatsinnehåll**.  
6. Välj åtgärden **Skapa artikelinförsel**. En artikelinförselinstruktion är nu klar att utföras av lagerpersonalen. Alternativt kan du välja åtgärden **Frisläppning** och skapa distributionslagerinförslar med hjälp av **Artikelinförselförslag**. Mer information finns i [Planera artikelinförslar i kalkylark](warehouse-how-to-plan-put-aways-in-worksheets.md)

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
