---
title: Så här plockar du artiklar med Lagerplockning
description: Lär dig använda lagerplockningar för att registrera och bokföra information om plockning och leverans för källdokument.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 7377'
---
# <a name="pick-items-with-inventory-picks"></a>Plocka artiklar med lagerplockning

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du plocka och inleverera artiklar och använda någon av fyra metoder, enligt beskrivningen i följande tabell.

|Metod|Utgående process|Begär plockning|Kräv utleverans|Komplexitetsnivå (mer information på [Warehouse Management – översikt](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bokföra plockning och utleverans från orderraden|||Ingen tilldelad distributionslageraktivitet.|  
|B|Bokföra plockning och utleverans från ett lagerplockningdokument|Aktiverat||Grundläggande: Order för order|  
|A|Bokföra plockning och utleverans från ett distributionslagerutleveransdokument||Aktiverat|Grundläggande: Konsoliderad inleverans-/utleveransbokföring för flera order.|  
|D|Bokföra plockning från ett distributionslagerplockningdokument och bokföra leveransen från ett distributionslagerutleveransdokument|Aktiverat|Aktiverat|Avancerat|  

Läs mer i [Avgående distributionslagerflöde](design-details-outbound-warehouse-flow.md).

I denna artikel hänvisas till metod B i tabellen.

När det lagerställe som du vill plocka från har konfigurerats så att plockbehandling krävs men inte leveransbearbetning, använder du sidan **Lagerplockning** för att registrera och bokföra plocknings- och leveransinformation för dina källdokument. Avgående källdokumenten kan göras för försäljningsorder, inköpsreturorder och avgående överföringar.

> [!NOTE]
> Produktion och monteringsorder med komponent representerar också avgående källdokument. Läs mer om hantering av produktions- och monteringsutflöde för interna processer på [Designdetaljer: Interna distributionslagerflöden](design-details-internal-warehouse-flows.md).
>
> Även om serviceorder även är utgående källdokument, stöder de inte den grundläggande komplexitetsnivån, order för order.
>
> Om plockning- och leveransförsäljningsradantal läggs till i order ska du följa vissa regler när du skapar lagerplockningsraderna. Mer information finns på [Hantering av artikel för montering mot kundorder i lagerplockningar](#handling-assemble-to-order-items-with-inventory-picks).  

Du kan skapa en lagerartikelplockning på tre sätt:

* Skapa lagerplockningen direkt från källdokumentet.  
* Skapa lagerplockningar för flera källdokument samtidigt med hjälp av batch-jobbet.
* Begär plockningen i två steg genom att först släppa källdokumentet, som fungerar som en signal till distributionslagret att källdokumentet är klart för plockning.

Lagerplockning kan sedan skapas från sidan **Lagerplockning** baserat på källdokumentet.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Så här skapar du en lagerplockning från källdokumentet

1. I källdokumentet, som kan vara en försäljningsorder, inköpsreturorder, utgående överföringsorder eller en produktionsorder, klickar du på åtgärden **Skapa lagerartikelinförsel/plocka**.
2. Markera kryssrutan **Skapa lagerplockning**.  
3. Välj knappen **OK**. En ny lagerplockning skapas.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Så här skapar du flera lagerplockningar med batch-jobbet

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Skapa lagerinförsel/plockning/rörelse** och väljer sedan relaterad länk.  
2. På snabbfliken **Dist.lagerkrav** använder du fälten **Ursprungsnr** och **Källdokument** om du vill filtrera efter vissa typer av dokument eller intervall med dokumentnummer. Du kan till exempel skapa plockningar för enbart försäljningsorder.  
3. På snabbfliken **Alternativ**, markera kryssrutan **Skapa lagerplockning**.
4. Välj **OK**.

## <a name="to-create-the-pick-in-two-steps"></a>Så här skapar du plockningen i två steg

### <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Så här begär du en lagerplockning genom att släppa källdokumentet

För försäljningsorder, inköpsreturorder och utgående överföringsorder skapar du distributionslagerkravet genom att släppa ordern. När du släpper ordern blir artiklarna tillgängliga för plockning.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
2. Markera den försäljningsorder som du vill släppa och välj sedan åtgärden **Släpp**.

### <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Så här skapar du en lagerplockning från källdokumentet:

När du släppt en order kan distributionslagerarbetare upprätta en lagerplockning.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **lagerplockning** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **Källdokument** markerar du den typ av dokument som du plockar för.  
4. I fältet **Ursprungsnr** markerar du källdokumentet.  
5. Välj alternativt åtgärden **Hämta källdokument** för att skapa en lista över utgående källdokument som är klara för plockning för på lagerstället.  
6. Välj knappen **OK** för att fylla plockrader enligt det valda källdokumentet.  

## <a name="to-record-inventory-picks"></a>När du vill registrera lagerplockning

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **lagerplockning** och väljer sedan relaterad länk.  
2. I fältet **Lagerställeskod** på plockningsraderna, är lagerstället som artiklarna måste plockas från antyder per artiklarna standardlagerplats. Du kan ändra lagerstället på den här sidan om det behövs.  
3. Utför plockningen och ange antalet i fältet **Ant. att hantera**.

    Om du måste placera artiklar för en rad på flera lagerställen, t.ex. om hela antalet inte finns på lagret använder du åtgärden **Dela rad**, på snabbfliken **Rader**. Åtgärden skapar en rad för återstående antal att hantera.

4. Välj åtgärden **Bokföra**.  

    * Bokför utleveransen av källdokumentraderna som plockades.
    * Om lagerstället använder lagerställen kommer bokföringen även att skapa distributionslagertransaktioner för att bokföra ändringar i antalet lagerställen.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Hantering av artikel för montering mot kundorder i lagerplockningar

Du kan även använda sidan **Lagerplockning** för att plocka och leverera för försäljning där artiklar måste monteras, innan de kan levereras. Läs mer på [Sälja artiklar som monterats mot kundorder](assembly-how-to-sell-items-assembled-to-order.md).

Artiklar där montering mot kundorder inte fysiskt finns i en lagerplats, förrän de är bokförda som utflöde på en lagerplats. Plocka artiklar för montering mot kundorder från ett lagerställe för utleveranser följer ett speciellt flöde.

1. Från en lagerplats tar lagerarbetare monteringsartiklarna till ett leveransdocka och bokför sedan lagerplockningen.
2. Bokförda lagerplockningen bokför sedan monteringsutflödet, komponentförbrukningen och utleveransen.

Du kan lägga upp [!INCLUDE[prod_short](includes/prod_short.md)] för att automatiskt skapa en lagertransport, när monteringsartikeln för lagerplockningen skapas. Välj fältet **Skapa transporter automatiskt** på sidan **Monteringsinställningar**. Läs mer på [Ställa in grundläggande dist.lager med operationsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

Lagerplockningsrader för försäljningsartiklar skapas på olika sätt beroende på om ingen, några eller alla försäljningsradantal monteras mot kundorder. I scenarier där en del av antalet är monterat och en del plockas från lagret, skapas ett minimum på två lagerplockningsrader.

I försäljning där hela antalet på försäljningsorderraden är monterad till order, skapas en lagerplockningsrad för det antalet. Värdet i fältet **Antal att montera** är lika med värdet i fältet **Antal att leverera**. Fältet **montering mot kundorder** är markerat på raden.

Om ett monteringsutflöde konfigureras för lagerstället innehåller värdet **Lagerställeskod** på inventeringsraden innehåller värdet från följande fält, i följande ordning.

* ***Lagerpl.kod för mont. mot lev.** <!-- not applicable for inv pick-->
* **Från monteringsplats - kod**

Om ingen lagerställeskod anges på försäljningsorderraden och ingen monteringsutflöde har angetts för lagerstället, är **Lagerställeskod** på lagerplockningsraden tomt. Lagerarbetaren måste öppna sidan **Lagerställesinnehåll**och markera den lagerplats där monteringsartiklarna är församlade.

I scenarier där en del av antalet monteras och ett annat ska plockas, skapas ett minimum på två plockningsrader.

* En plockningsrad är för antal för montering mot kundorder. [!INCLUDE [prod_short](includes/prod_short.md)] använder följande fält, i denna ordning, för att fastställa lagerställekoden: **Lagerställekoden**, **Lagerpl.kod för mont. mot lev.** och sedan **Från monteringsplats – kod**. Om dessa fält är tomma måste lagermedarbetaren öppna sidan **Lagerställesinnehåll** och markera den lagerplats där monteringsartiklarna är församlade.  
* Den andra plockningsraden beror på vilka lagerställen som kan uppfylla det återstående antalet. Om artikeln lagras på flera lagerplatser skapas flera rader. Ta rad baseras på antalet i **Ant. att utleverera**.

> [!NOTE]  
> Om artiklar monteras mot kundorder, skapas lagerplockningen för den kopplade försäljningsordern för att skapa en lagerförflyttning för alla monteringskomponenter.  

## <a name="see-also"></a>Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Genomgång: Plockning och leverans i grundläggande lagerkonfiguration](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
