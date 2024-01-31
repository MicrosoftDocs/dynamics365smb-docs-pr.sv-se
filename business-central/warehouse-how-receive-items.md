---
title: Ta emot artiklar
description: Denna artikel är en översikt över olika sätt att inleverera artiklar på ett lagerställe med en distributionslagerinleverans.
author: brentholtorf
ms.author: bholtorf
ms.topic: how-to
ms.date: 09/02/2022
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008'
ms.service: dynamics-365-business-central
---
# Inleverera artiklar med en lagerinleveranser

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du ta emot objekt och lägga undan dem med någon av fyra metoder, enligt beskrivningen i följande tabell.

|Metod|inkommande behandling|Begär inleverans|Begär artikelinförsel|Komplexitetsnivå (mer information på [Warehouse Management – översikt](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokföra inleverans och lagerinförsel från orderraden|||Ingen tilldelad distributionslageraktivitet.|  
|B|Bokföra inleverans och lagerinförsel från ett lagerinförseldokument||Aktiverat|Grundläggande: Order för order|  
|A|Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument|Aktiverat||Grundläggande: Konsoliderad inleverans-/utleveransbokföring för flera order.|  
|D|Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument|Aktiverat|Aktiverat|Avancerat|  

Om du vill veta mer om hur du hanterar inkommande artiklar går du till [Inkommande distributionslagerflöde](design-details-inbound-warehouse-flow.md).

Följande artikel avser metoderna C och D i föregående tabell.

## Inleverera artiklar med en lagerinleverans

När artiklar tas emot i ett distributionslager som konfigureras för att bearbeta distributionslagerinleveranser måste du hämta raderna för det släppta källdokument som utlöste inleveransen. Om du använder lagerplatser kan du antingen acceptera standardlagerplatsen eller ange den lagerplats där artiklarna ska placeras. Den senare kanske krävs när du tar emot en artikel för första gången. Ange sedan antalet artiklar som har tagits emot och bokföra inleveransen.  

Du kan skapa distributionslagerinleverans på två sätt:

* Med en pushmetod när arbetet utförs på orderbasis. Välj åtgärden **Skapa dist.lager inleverans** i källdokumentet, till exempel inköpsorder, försäljningsreturorder eller överföringsorder för att skapa distributionslagerinleverans för ett källdokument.
* Med pullmetoden när du använder åtgärden **Frisläpp** i källdokumentet, t.ex. inköpsorder, försäljningsreturorder eller överföringsorder för att lämna ut dokumentet till lagret. En lageranställd skapar en **Dist.lager inleverans** för ett eller flera släppta källdokument. I proceduren nedan beskrivs hur du skapar en distributionslagerinleverans med en pullmetod. I proceduren nedan beskrivs hur du skapar en distributionslagerinleverans med en pullmetod.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Dist.lager inleveranser** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  

    Fyll i fältet **Lagerställekod** på snabbfliken **Allmänt**. När du hämtar källdokumentrader, kopieras delar av informationen i huvudet till varje rad.

    För ett lagerställe som kräver lagerplats, fyll i **Lagerplatskod**. Beroende på dina inställningar kan [!INCLUDE[prod_short](includes/prod_short.md)] lägga till lagerplatskoden åt dig. Läs mer om [Zon och lagerplatskoder](warehouse-how-receive-items.md#zone-and-bin-codes).  

3. Du kan få källdokument på två sätt:

    1. Välj åtgärden **Hämta källdokument**. Sidan **Källdokument – inkommande** öppnas. Här kan du välja ett eller flera källdokument frisläppta till distributionslager som kräver inleverans.
    2. Välj åtgärden **Filter för att hämta urspr.dok.**. Sidan **Filter att hämta ursprungsdok. – Inkommande** öppnas. Här kan du välja ursprungsdokumentfilter och köra det. Alla släppta källdokumentrader som uppfyller filterkriterierna läggs till på sidan **Dist.lager inleverans**. Läs mer på [Så här använder du filter för att hämta källdokument](warehouse-how-receive-items.md#how-to-use-filters-to-get-source-documents).

4. Ställ in det antal som ska inlevereras.

    Fältet **Ant. att inlevereras** är ifyllt med utestående antal på respektive rad, men du kan ändra antalet som behövs. 

    För att fylla i fältet **Ant. att inlevereras** på alla rader med noll, väljer du åtgärden **Ta bort ant. att inleverera**. Om du till exempel anger antal till noll, är det praktiskt att använda en streckkodsskanner för att uppdatera de inlevererade kvantiteterna. För att lägga till de utestående kvantiteterna från källdokumentet igen, välj åtgärden **Fyll i auto. ant. att inleverera**.  

    På ett distributionslagerinleveransdokument där inlevererad mängd överstiger den beställda anger du den faktiskt inlevererade mängden i fältet **Ant. att inlevereras**. Om ökningen ligger inom den tolerans som anges av den tilldelade koden för överinleverans uppdateras fältet **Överleveranskvantitet** för att visa det antal med vilket värdet i fältet **Antal** överskrids. Om ökningen överskrider toleransen är överinleverans inte tillåten.

5. Bokför lagerinleveransen. Fälten med antal i källdokumenten uppdateras automatiskt och artiklarna läggs till i lager.  

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

    > [!TIP]
    > Om du använder dist.lager artikelinförsel, som refererar till metod D i tabellen i början av denna artikel, inlevereras artiklarna men kan inte plockas förrän de har förts in. Om du vill veta mer om att införa artiklar kan du gå till [Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-warehouse-put-aways.md).
    >
    > Annars kan du använda åtgärden **bokför och skriv ut**. Åtgärden bokför inleveransen och skriver ut den som en artikelinförselinstruktion som visar var artikeln ska placeras.

    > [!NOTE]  
    > Om distributionslagret använder direktutleverans kan du kontrollera om artiklar inte kan direktutlevereras utan att de ska tas bort. För att lära dig mer om montering av artiklar, gå till [Beräkna direktutleverans av artiklar](warehouse-how-to-cross-dock-items.md).

## Så här använder du filter för att hämta källdokument

Från en lagerinleveransen kan du använda sidan **Filter att hämta ursprungsdok.** för att hämta de släppta källdokumentraderna som anger vilka artiklar som ska inlevereras.

1. Välj åtgärden **Filter för att hämta urspr.dok.** i distributionslagerinleveransen.
2. Du skapar ett nytt filter genom att ange en beskrivande kod i fältet **Kod** och väljer sedan åtgärden **Ändra**.

    Sidan **Filterkortet för källdokument - Inkommande** visas.

3. Använd filtren för att definiera vilken typ av källdokumentrader som ska hämtas. Du kan till exempel välja olika typer av källdokument, till exempel inköps- och överföringsorder.
4. Välj **Kör**.  

Alla relaterade källdokumentrader, som uppfyller filtervillkorna, läggs till på sidan **Dist.lager inleverans** som du aktiverade från filter för.

Du kan skapa ett obegränsat antal filterkombinationer. Filter sparas på sidan **Filter att hämta ursprungsdok.** och är tillgängliga nästa gång du behöver den. Du kan ändra villkor när som helst, genom att välja åtgärden **Ändra**.

## Zon och lagerplatskoder

Om du vill ta emot artiklar med klasskoder för distributionslager som skiljer sig från klasskoderna för lagerplats i fältet **Lagerplatskod** i dokumenthuvudet, avmarkera fältet **Lagerplatskod** i huvudet innan du hämtar källdokumentets rader för artiklarna.  
<!-- TBD, table with comparison of various options-->

Om lagerplatser är obligatoriska för lagerställen, läggs zon och lagerplatskoder till i dokumentet för lagerinleverans enligt följande:

* För avancerade konfigurationer som använder dirigerad artikelinförsel och plockning använder [!INCLUDE [prod_short](includes/prod_short.md)] lagerplatskod för inleverans från sidan **Lagerställekort** för lagerstället. Om det inte finns någon lagerplatskod för inleverans anges ingen lagerplats. Om artikeln och inleveransens lagerplatser inte matchar är koden för inleveransens lagerplats tom.
* I andra konfigurationer om lagerplatskod för inleverans inte har angetts använder [!INCLUDE [prod_short](includes/prod_short.md)] lagerplatskoden från källdokumentet.

## Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
