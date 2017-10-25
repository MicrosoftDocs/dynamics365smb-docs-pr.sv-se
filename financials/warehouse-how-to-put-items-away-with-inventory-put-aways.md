---
title: "Så här: Införa artiklar med lagerartikelinförsel | Microsoft Docs"
description: "När lagerstället har konfigurerats så att artikelinförsel krävs men inte inleverans, använder du dokumentet **Lagerartikelinförsel** för att registrera och bokföra artikelinförsel och inleveransinformation för källdokumenten. Det ankommande källdokumentet kan vara in inköpsorder, en försäljningsreturorder, en ankommande överföringsorder eller en produktionsorder vars utflöde är klart för artikelinförsel."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5de060d742401da62339fb67deff38d0a1e7bddb
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-put-items-away-with-inventory-put-aways"></a>Så här: Införa artiklar med lagerartikelinförslar
När lagerstället har konfigurerats så att artikelinförsel krävs men inte inleverans, använder du dokumentet **Lagerartikelinförsel** för att registrera och bokföra artikelinförsel och inleveransinformation för källdokumenten. Det ankommande källdokumentet kan vara in inköpsorder, en försäljningsreturorder, en ankommande överföringsorder, montering eller en produktionsorder vars utflöde är klart för artikelinförsel.  

Du kan skapa en lagerartikelinförsel på tre sätt:  

- Skapa artikelinförseln i två steg genom att först skapa ett distributionslagerkrav från källdokumentet, som fungerar som en signal till distributionslagret att källdokumentet är klart för artikelinförsel. Lagerartikelinförseln kan sedan skapas från fönstret **Lagerartikelinförsel** baserat på källdokumentet.  
- Skapa lagerartikelinförseln direkt från själva källdokumentet.  
- Du kan skapa lagerartikelinförslar för flera källdokument samtidigt med hjälp av batch-jobbet.  

## <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Så här begär du en lagerinförsel genom att släppa källdokumentet
För försäljningsorder, inköpsreturorder och ingående överföringsorder och montering skapar du distributionslagerkravet genom att släppa ordern. Nedan beskrivs hur du gör detta från en inköpsorder.  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsorder** och välj sedan relaterad länk.
2. Markera den inköpsorder som du vill släppa och välj sedan åtgärden **Släpp**.  

    För produktionsorder skapar du distributionslagerkravet genom att skapa ett ankommande krav från den släppta produktionsordern.  
3.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Släppta produktionsorder** och välj sedan relaterad länk.  
4. Välj åtgärden **Skapa ankommande dist.lagerförslag**.  

> [!NOTE]  
>  Du kan också skapa ankommande distributionslagerkrav genom att markera kryssrutan **Skapa ankommande rekvisition** när du uppdaterar produktionsordern. Mer information finns i [så här: Uppdatera eller omplanera produktionsorder](production-how-to-replan-refresh-production-orders.md).  

När distributionslagerkravet har skapats kan någon som arbetar i distributionslagret och skapar artikelinförslar se att källdokumentet är klart och kan då skapa ett nytt lagerinförseldokument.  

## <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Så här skapar du en lagerartikelinförsel från källdokumentet
Nu när begäran har skapats kan lagerpersonalen skapa en ny artikelinförsel baserat på släppta källdokument.   
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerinförsel** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **Källdokument** markerar du den typ av källdokument som du lägger ifrån dig.  
4. I fältet **Ursprungsnr** markerar du källdokumentet.  
5. Välj åtgärden **Hämta källdokument** för att välja från en lista över ankommande källdokument som är klara för artikelinförsel för på lagerstället.  
6. Välj knappen **OK** för att fylla artikelinförselrader enligt det valda källdokumentet.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Så här skapar du en lagerartikelinförsel från källdokumentet  
1.  I källdokumentet, som kan vara en inköpsorder, försäljningsreturorder, ankommande överföringsorder eller en produktionsorder, klickar du på åtgärden **Skapa lagerartikelinförsel/plocka**.  
2. Markera kryssrutan **Skapa lagerinförsel/plockning**.
3. Välj knappen **OK**. En ny lagerinförsel har skapats.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Så här skapar du flera lagerartikelinförslar med batch-jobbet:  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Skapa lagerinförsel/plockning** och välj sedan relaterad länk.  
2.  På snabbfliken **Dist.lagerkrav** i beställningsfönstret använder du fälten **Ursprungsnr** och **Källdokument** om du vill filtrera efter vissa typer av dokument eller intervall med dokumentnummer.  
3.  Välj fältet **Skapa lagerinförsel** på kryssrutan **Alternativ**.
4.  Välj knappen **OK**. Anger numret för den bokförda artikelinförseln i lagret.

## <a name="to-record-the-inventory-put-away"></a>När du vill registrera lagerinförsel.  
1. Du öppnar ett befintligt artikelinförseldokument genom att välja ett i fönstret **Lagerartikelinförslar**.  
2. I fältet **Lagerplatskod** per artikelns standardlagerplats föreslår på artikelinförsel raderna den lagerplats där artiklarna ska placeras. Du kan ändra lagerplatsen i det här fönstret om det behövs.  
3. Utför artikelinförseln och ange information för den faktiska kvantiteten som förts in i fältet **Ant. att hantera**.

    Om det är nödvändigt att placera artiklar för en rad på flera lagerplatser, t.ex. om den utsedda lagerplatsen är full, använder du funktionen **Dela rad**, på snabbfliken **Rader**. Mer information om hur du delar upp rader finns i [så här: dela dist.lageraktivitet rader](warehouse-how-to-split-warehouse-activity-lines.md).  
4. När du har utfört lagerinförsel, väljer du åtgärden **Bokföra**.  

Vid bokföringen bokförs inleveransen, eller för produktionsorder utflödet, för de källdokumentrader som har förts in. Om lagerstället använder lagerplatser skapas distributionslagertransaktioner som bokför kvantitetsändringarna på lagerplatsen.

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

