---
title: Så här plockar du artiklar med Lagerplockning
description: Om det lagerställe som du vill plocka från har konfigurerats så att plockbehandling krävs men inte leveransbearbetning, använder du lagerplockningsdokument för att registrera och bokföra plocknings- och leveransinformation för dina källdokument.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 79b373ec522d2cd8f99c6b0a98db0df7f9d1793f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533704"
---
# <a name="pick-items-with-inventory-picks"></a>Plocka artiklar med lagerplockning

När det lagerställe som du vill plocka från har konfigurerats så att plockbehandling krävs men inte leveransbearbetning, använder du sidan **Lagerplockning** för att registrera och bokföra plocknings- och leveransinformation för dina källdokument. Det utgående källdokumentet kan vara en försäljningsorder, en utgående överföringsorder eller en produktionsorder vars komponenter är klara att plockas.

> [!NOTE]  
> Komponenter för monteringsorder kan inte plockas eller bokföras med lagerplockningar. Använd istället sidan **lagerförflyttning**. Mer information finns i [Flytta komponenter till ett verksamhetsområde i grundläggande lagerstyrning](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)
>
> Om plockning- och leveransförsäljningsradantal läggs till i order ska du följa vissa regler när du skapar lagerplockningsraderna. Mer information finns i avsnittet [hantera artiklar för montering mot kundorder i lagerplockningar](#handling-assemble-to-order-items-with-inventory-picks).  

Du kan skapa en lagerartikelplockning på tre sätt:  

- Skapa plockningen i två steg genom att först begära en lagerplockning genom att släppa källdokument. Det signalerar till distributionslagret att källdokumentet är klart för plockning. Lagerplockning kan sedan skapas från sidan **Lagerplockning** baserat på källdokumentet.  
- Skapa lagerplockningen direkt från själva källdokumentet.  
- Du kan skapa lagerplockningar för flera källdokument samtidigt med hjälp av batch-jobbet.  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Så här begär du en lagerplockning genom att släppa källdokumentet

För försäljningsorder, inköpsreturorder och utgående överföringsorder skapar du distributionslagerkravet genom att släppa ordern. Nedan beskrivs hur du gör detta från en försäljningsorder.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
2. Markera den försäljningsorder som du vill släppa och välj sedan åtgärden **Släpp**.

Om det gäller produktionsorder skapar du automatisktdistributionslagerkravet för plockningen av komponenterna som kallas *bokföring*, när produktionsorderns status ändras till **Släppt** eller när den släppta produktionsordern skapas. Mer information finns i [Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md).

När distributionslagerkravet har skapats kan någon som arbetar i distributionslagret och plockar artiklar se att källdokumentet är klart att plockas, och kan då skapa ett nytt plockningsdokument från distributionslagerkravet.  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Så här skapar du en lagerplockning från källdokumentet:

Nu när begäran har skapats kan lagerpersonalen skapa en ny lagerplockning baserat på släppta källdokument.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **lagerplockning** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
    Kontrollera att fältet **Nr.** fälten på snabbfliken **Allmänt** fylls i.
3. I fältet **Källdokument** markerar du den typ av källdokument som du plockar för.  
4. I fältet **Ursprungsnr** markerar du källdokumentet.  
5. Välj åtgärden **Hämta källdokument** för att välja från en lista över utgående källdokument som är klara för plockning för på lagerstället.  
6. Välj **OK** för att fylla plockrader enligt det valda källdokumentet.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Så här skapar du en lagerplockning från källdokumentet

1. I källdokumentet, som kan vara en försäljningsorder, inköpsreturorder, utgående överföringsorder eller en produktionsorder, klickar du på åtgärden **Skapa lagerartikelinförsel/plocka**.
2. Markera kryssrutan **Skapa lagerplockning**.  
3. Välj knappen **OK**. En ny lagerplockning skapas.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Så här skapar du flera lagerplockningar med batch-jobbet

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Skapa lagerinförsel/plockning** och väljer sedan relaterad länk.  
2. På snabbfliken **Dist.lagerkrav** använder du fälten **Ursprungsnr** och **Källdokument** om du vill filtrera efter vissa typer av dokument eller intervall med dokumentnummer. Du kan till exempel skapa plockningar för enbart försäljningsorder.  
3. Välj fältet **Skapa lagerinförsel** på kryssrutan **Skapa lagerplockning**.
4. Välj knappen **OK**. De specifika lagerplockningarna jar skapats.

> [!NOTE]  
> Om plockning- och leveransförsäljningsradantal läggs till i order ska du följa vissa regler när du skapar lagerplockningsraderna. Mer information finns i avsnittet [hantera artiklar för montering mot kundorder i lagerplockningar](#handling-assemble-to-order-items-with-inventory-picks).  
>
> I grundläggande lagerkonfiguration plockas artiklar för montering mot försäljningsorder från den kopplade försäljningsordern som förklaras i det här avsnittet. Mer information finns i avsnittet [hantera artiklar för montering mot kundorder i lagerplockningar](#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="to-record-the-inventory-picks"></a>När du vill registrera lagerplockning.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **lagerplockning** och väljer sedan relaterad länk.  
2. I fältet **Lagerställeskod** på plockningsraderna, är lagerstället som artiklarna måste plockas från antyder per artiklarna standardlagerplats. Du kan ändra lagerstället på den här sidan om det behövs.  
3. Utför plockningen och ange information för den faktiska kvantiteten som förts in i fältet **Ant. att hantera**.

    Om det är nödvändigt att plocka artiklar för en rad på flera lagerställen, t. ex. eftersom de inte finns på den utsedda lagerstället, använder du funktionen **Dela rad**, på snabbfliken **Rader**. Mer information om hur du delar upp rader finns i [Dela dist.lageraktivitetsrader](warehouse-how-to-split-warehouse-activity-lines.md).  
4. När du har utfört plockningen, väljer du åtgärden **Bokföra**.  

Vid bokföringsprocessen bokförs leverans av de källdokumentrader som har plockats, eller om det gäller produktionsorder bokförs förbrukningen vid bokföringsprocessen. Om lagerstället använder lagerställen kommer bokföringen även att skapa distributionslagertransaktioner för att bokföra ändringar i antalet lagerställen.  

## <a name="to-delete-inventory-pick-lines"></a>Ta bort lagerplockningsrader

Om artiklar i lagerplockningen inte är tillgängliga, kan du ta bort de lagerplockningsrader när du har bokfört dem och har sedan ta bort dokumentet lagerplockning. Källdokumentet, till exempel en försäljningsorder eller en produktionsorder, har sedan återstående artiklar som ska plockas som kan erhållas via en ny lagerplockning senare när artiklarna blir tillgängliga.  

> [!WARNING]  
> Den här processen är inte möjlig, om serienr/partinr angetts i källdokumentet. Till exempel om en försäljningsorderrad innehåller en serienr/partinr, då det artikelspårning specifikation tas bort om en lagerplockningsrad för serienr/partinr tas bort.  
>
> Om lagerplockningsrader har serienr/partinr som inte är tillgängliga, måste du inte ta bort de aktuella raderna. I stället måste ändra fältet **Ant. att hantera** till noll, bokföra faktisk plockning och sedan bort lagerplockningsdokument. Det garanterar att lagerplockningsraderna för de serienr/partinr kan återskapas från senare försäljningsorder.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Hantering av artikel för montering mot kundorder i lagerplockningar

Sidan **Lagerplockning** används också för att plocka och leverera för försäljning där artiklar måste vara församlade, innan de kan levereras. Mer information finns i [Sälja artiklar monterade mot order](assembly-how-to-sell-items-assembled-to-order.md).

Artiklar som ska levereras, inte fysiskt finns i en lagerplats, förrän de är bokförda och församlade som utflöde på en lagerplats i monteringsområdet. Det innebär att plocka artiklar för montering mot kundorder för utleverans följer ett speciellt flöde. Från en lagerplats tar lagerarbetare monteringsartiklarna till ett leveransdocka och bokför sedan lagerplockningen. Bokförda lagerplockningen bokför sedan monteringsutflödet, komponentförbrukningen och utleveransen.

Du kan lägga upp [!INCLUDE[prod_short](includes/prod_short.md)] för att automatiskt skapa en lagertransport, när monteringsartikeln för lagerplockningen skapas. Du anger dessa inställningar genom att välja fältet **skapa transporter automatiskt** på sidan **Monteringsinställningar** Mer information finns i [Flytta komponenter till ett verksamhetsområde i grundläggande lagerstyrning](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Lagerplockningsrader för försäljningsartiklar skapas på olika sätt beroende på om ingen, några eller alla försäljningsradantal monteras mot kundorder.

I vanliga lagerförsäljningar, när du använder lagerplockningar för att bokföra utleveransen av lagerantal, skapas en lagerplockrad eller flera om artikeln ligger i olika lagerställen för varje försäljningsorderrad. Denna plockningsrad baseras på antalet i **Ant. att utleverera**.

I montering mot kundorder försäljning, där hela antalet på försäljningsorderraden är monterad till order, skapas en lagerplockningsrad för det antal. Detta innebär att värdet i fältet Antal att montera är lika med värdet i fältet **Antal att leverera**. Fältet **montering mot kundorder** är markerat på raden.

Om ett monteringsutflöde har angetts för lagerstället, när värdet i fältet **Lagerpl.kod för mont. mot lev.** eller värdet i **Från monteringsplats – kod** i den ordern infogas i fältet **Lagerställeskod** på lagerplockningsraden.

Om ingen lagerställeskod anges på försäljningsorderraden, och ingen monteringsutflöde har angetts för lagerstället, är **Lagerställeskod** på lagerplockningsraden tomt. Lagerarbetaren måste öppna sidan **Lagerställesinnehåll** och markera den lagerplats där monteringsartiklarna är församlade.

I alla scenarier där en del av antalet måste först vara församlad och ett annat ska plockas från lagret, skapas ett minimum på två lagerplockningsrader. En plockningsrad är för antal för montering mot kundorder. Den andra plockningsraden beror på vilka lagerställen som kan uppfylla det återstående antalet från lagret. Lagerställeskoder på de två raderna är ifyllt olika sätt, som beskrivs för de två olika försäljningstyperna. Mer information finns i avsnittet Kombinationsscenarion i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Genomgång: Plockning och leverans i grundläggande lagerkonfiguration](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
