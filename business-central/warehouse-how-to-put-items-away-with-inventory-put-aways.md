---
title: 'Så här: Införa artiklar med lagerartikelinförslar'
description: Lär dig använda lagerinförseldokumentet för att registrera och bokföra artikelinförsel och inleveransinformation.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 09/19/2023
ms.custom: bap-template
ms.search.forms: '7375,'
---
# Föra in artiklar med lagerartikelinförsel

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du ta emot objekt och lägga undan dem med någon av fyra metoder, enligt beskrivningen i följande tabell.

|Metod|inkommande behandling|Begär inleverans|Begär artikelinförsel|Komplexitetsnivå (mer information på [Warehouse Management – översikt](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokföra inleverans och lagerinförsel från orderraden|||Ingen tilldelad distributionslageraktivitet.|  
|B|Bokföra inleverans och lagerinförsel från ett lagerinförseldokument||Aktiverat|Grundläggande: Order för order|  
|A|Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument|Aktiverat||Grundläggande: Konsoliderad inleverans-/utleveransbokföring för flera order.|  
|D|Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument|Aktiverat|Aktiverat|Avancerat|  

Läs mer i [Inkommande distributionslagerflöde](design-details-inbound-warehouse-flow.md).

I denna artikel hänvisas till metod B i tabellen.

När lagerstället har konfigurerats så att artikelinförsel krävs men inte inleverans, använder du dokumentet **Lagerartikelinförsel** för att registrera och bokföra artikelinförsel och inleveransinformation för källdokumenten. Inkommande källdokumenten kan göras för inköpsorder, försäljningsreturorder och inkommande överföringar.

> [!NOTE]
> Produktion och monteringsutflöde representerar också inkommande källdokument. Läs mer om hantering av produktions- och monteringsutflöde för interna processer på [Designdetaljer: Interna distributionslagerflöden](design-details-internal-warehouse-flows.md).

Du kan skapa en lagerartikelinförsel på tre sätt:  

* Skapa lagerartikelinförseln direkt från själva källdokumentet.  
* Skapa lagerartikelinförslar för flera källdokument samtidigt med hjälp av ett batch-jobb.  
* Skapa artikelinförseln i två steg genom att först släppa källdokumentet för att göra artiklarna tillgängliga för artikelinförsel. Du kan skapa lagerartikelinförseln baserat på källdokumentet med sidan **Lagerartikelinförsel**.  

## Så här skapar du en lagerartikelinförsel från källdokumentet

1. I källdokumentet, som kan vara en inköpsorder, försäljningsreturorder, inkommande överföringsorder, välj åtgärden **Skapa lagerartikelinförsel/plocka**.  
2. Markera kryssrutan **Skapa lagerinförsel/plockning**.
3. Välj knappen **OK**. En ny lagerinförsel har skapats.

## Så här skapar du flera lagerartikelinförslar med batch-jobbet:

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Skapa lagerinförsel/plockning/rörelse** och väljer sedan relaterad länk. 
2. På snabbfliken **Dist.lagerkrav** använder du fälten **Ursprungsnr** och **Källdokument** om du vill filtrera efter vissa typer av dokument eller intervall med dokumentnummer. Du kan till exempel endast skapa artikelinförseln för inköpsorder.
3. På snabbfliken **Alternativ**, markera kryssrutan **Skapa lagerinförsel**.
4. Välj **OK**. Anger numret för den bokförda artikelinförseln i lagret.

## Så här skapar du artikelinförseln i två steg

### Så här begär du en lagerinförsel genom att släppa källdokumentet

När du släpper inköpsorder, försäljningsreturorder och inkommande överföringsorder, blir artiklarna på order tillgängliga för artikelinförsel. Följande steg beskriver hur du gör artiklarna på en inköpsorder klara att föras in.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.
2. Markera den inköpsorder som du vill släppa och välj sedan åtgärden **Släpp**.  

### Så här skapar du en lagerartikelinförsel från källdokumentet

En distributionslagerarbetare kan skapa en ny lagerinförsel baserat på det släppta källdokumentet.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Lagerinförsel** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **Källdokument** markerar du den typ av källdokument som du lägger ifrån dig.  
4. I fältet **Ursprungsnr** markerar du källdokumentet.  
5. Välj åtgärden **Hämta källdokument** för att välja från en lista över inkommande källdokument som är klara för artikelinförsel för på lagerstället.  
6. Välj knappen **OK** för att fylla artikelinförselrader enligt det valda källdokumentet.  

## När du vill registrera lagerinförsel.

1. På sidan **lagerartikelinförsel**, öppna ett befintligt lagerinförseldokument.  
2. I fältet **Lagerställeskod** på artikelinförselrader föreslår lagerplats där artiklarna måste föras in baserat på artikelns standardlagerplats. Du kan ändra lagerplats vid behov.  
3. Utför artikelinförseln och ange den faktiska kvantitet som förts in i fältet **Ant. att hantera**.

    Om du måste placera artiklar för en rad på flera lagerställen, t.ex. om den utsedda lagerplatsen är full, använder du funktionen **Dela rad**, på snabbfliken **Rader**. Åtgärden skapar en rad för återstående antal att hantera.  
4. När du har fört in artiklarna väljer du åtgärden **Bokföra**.  

    * Bokför inleveransen av de källdokumentrader som har förts in
    * Om lagerstället använder lagerställen kommer bokföringen även att skapa distributionslagertransaktioner för att bokföra ändringar i antalet lagerställen.

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
