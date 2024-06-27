---
title: Leverera artiklar
description: I den här artikeln beskrivs hur du levererar artiklar från distributionslagret.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/10/2024
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
ms.service: dynamics-365-business-central
---

# Utleverera artiklar med en lagerutleverans

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du plocka och inleverera artiklar och använda någon av fyra metoder, enligt beskrivningen i följande tabell.

|Metod|Utgående process|Begär plockning|Kräv utleverans|Komplexitetsnivå (mer information på [Warehouse Management – översikt](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bokföra plockning och utleverans från orderraden|||Ingen tilldelad distributionslageraktivitet.|  
|B|Bokföra plockning och utleverans från ett lagerplockningdokument|Aktiverat||Grundläggande: Order för order|  
|A|Bokföra plockning och utleverans från ett distributionslagerutleveransdokument||Aktiverat|Grundläggande: Konsoliderad inleverans-/utleveransbokföring för flera order.|  
|D|Bokföra plockning från ett distributionslagerplockningdokument och bokföra leveransen från ett distributionslagerutleveransdokument|Aktiverat|Aktiverat|Avancerat|  

För att lära dig mer om artikelutleverans, gå till [avgående distributionslagerflöde](design-details-outbound-warehouse-flow.md).

I denna artikel hänvisas till metod C och D i tabellen. I båda metoder börjar du med att skapa ett utleveransdokument från ett källdokument för företag. Sedan kan du välja de angivna artiklarna för utleverans.

När en lagerställe kräver utleveranser för distributionslagret, kan du leverera artiklar baserat på källdokument som har släppts till distributionslager. När du släpper källdokument blir artiklarna på dem klara att hanteras i distributionslagret. Följande källdokument finns:

* Försäljningsorder
* Inköpsreturorder
* Överföringsorder
* Serviceorder

Du kan skapa distributionslagerutleverans på två sätt:

* Med en pushmetod när arbetet utförs på orderbasis. Välj åtgärden **Skapa distributionslagerutleverans** i källdokumentet för att skapa en distributionslagerutleverans för dokumentet.
* I en pullmetod när du använder åtgärden **Frisläpp** i källdokumentet för att frisläppa den till distributionslagret. En lageranställd skapar en **Distributionslagerutleverans** för ett eller flera släppta källdokument. I proceduren nedan beskrivs hur du skapar en distributionslagerutleverans med en pullmetod.

## För att utleverera artiklar med ett dokument för distributionslagerutleverans

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Distributionslagerutleverans** och väljer sedan relaterad länk.  
2. Välj **Ny**.  
3. I fältet **Nr.** Välj den nummerserie som ska användas för att skapa ett ID för utleveransen.  
4. I fältet **Lagerställekod**, välj det lagerställe du utlevererar från. 

    När du hämtar källdokumentrader, kopieras delar av informationen från lagerstället till varje rad.  
5. Om lagerstället kräver lagerplats, fyll i **Lagerplatskod**. Beroende på dina inställningar kan [!INCLUDE[prod_short](includes/prod_short.md)]] lägga till lagerplatskoden åt dig. Läs mer om [Zon och lagerplatskoder](warehouse-how-ship-items.md#zone-and-bin-codes).  
6. Du kan få källdokument på två sätt:

    * Välj åtgärden **Hämta källdokument**. Sidan **Källdokument** öppnas. Här kan du välja ett eller flera källdokument frisläppta till distributionslager som kräver utleverans.
    * Välj åtgärden **Filter för att hämta urspr.dok.**. Sidan **Filter att hämta ursprungsdok.** öppnas. Du kan välja källdokumentfiltret och använda det. Alla släppta källdokumentrader som uppfyller filterkriterierna läggs till på sidan **Distributionslagerutleverans**. Läs mer på [Så här använder du filter för att hämta källdokument](warehouse-how-ship-items.md#how-to-use-filters-to-get-source-documents).

    > [!NOTE]
    > Om lagerstället använder direktutleveranser och lagerplatser för varje rad kan du visa hur många artiklar som har placerats i direktutleveranslagerställena. [!INCLUDE [prod_short](includes/prod_short.md)] beräknar antalet automatiskt när fälten i utleveransen uppdateras. Om det rör sig om de artiklar som ingår i den utleverans du förbereder, kan du skapa en plockning för alla artiklar och därefter färdigställa utleveransen. Läs mer på [Artiklar för direktutleverans](warehouse-how-to-cross-dock-items.md).

7. Skapa distributionslagerplockning. Om lagerstället kräver plockning, kan du skapa plockningsaktiviteter för utleveranser på något av följande två sätt:

    * Med push-metod där du använder åtgärden **Skapa plockning**. Välj de rader som du vill plocka och ange information om plockningarna. Till exempel vilka lagerplatser som ska tas från och placeras samt hur många enheter som ska hanteras. Lagerplatser kan fördefinieras för distributionslagerstället eller resurs.
    * Med pull-metod där du använder åtgärden **Frisläppa**. På sidan **Plockningskalkylark** kan du använda åtgärden **Hämta dist.lager dokument** för att hämta sina tilldelade plockningar. När distributionslagerplockningar är fullständigt registrerade tas raderna i **Plockningskalkylark** bort. Läs mer på [Plocka artiklar för distributionslagerutleverans](warehouse-how-to-pick-items-for-warehouse-shipment.md).

    > [!TIP]
    > För lagerställen som inte kräver plockning kan du skriva ut distributionslagerutleveransen och använda den som plocklista.

8. Ange antalet som ska levereras.  

    För lagerställen som kräver plockning uppdateras fältet **Ant. att utleverera** automatiskt när plockningen registreras. Annars fylls fältet **Ant. att utleverera** är ifyllt med utestående antal på respektive rad när distributionslagerutleveransraden skapas.

    Du kan ändra kvantiteten, men du kan inte skicka fler varor än antalet i fältet **Utestående ant.** på källdokumentrad eller fältet **Plockat antal** om plockning krävs.

    För att ange värdet i fältet **Ant. att utleverera** på alla rader med noll, väljer du åtgärden **Ta bort ant. att utleverera**. Om du till exempel anger antal till noll, är det praktiskt att använda en streckkodsskanner för att uppdatera de utlevererade kvantiteterna. Om du vill lägga till disponibelt antal för utleverans väljer du åtgärden **Fyll i auto. ant. att utleverera**.

9. Bokför leveransen.

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

## Så här använder du filter för att hämta källdokument

Från en lagerutleverans kan du använda sidan **Filter att hämta ursprungsdok.** för att hämta de släppta källdokumentraderna som anger vilka artiklar som ska utlevereras.

1. Välj åtgärden **Filter för att hämta urspr.dok.** i distributionslagerutleveransen. 
2. Du skapar ett nytt filter genom att ange en beskrivande kod i fältet **Kod** och väljer sedan åtgärden **Ändra**.

    Sidan **Filterkortet för källdokument - avgående** visas.

3. Använd filtren för att definiera vilken typ av källdokumentrader som ska hämtas. Du kan till exempel välja olika typer av källdokument, till exempel försäljnings- och överföringsorder.
4. Välj **Kör**.  

Alla relaterade källdokumentrader, som uppfyller filtervillkorna, läggs till på sidan **Dist.lager inleverans** som du aktiverade från filter för.

Du kan skapa ett obegränsat antal filterkombinationer. Filter sparas på sidan **Filter att hämta ursprungsdok.** och är tillgängliga nästa gång du behöver den. Du kan ändra villkor när som helst, genom att välja åtgärden **Ändra**.

## Zon och lagerplatskoder

Om lagerplatser är obligatoriska på lagerstället föreslår [!INCLUDE [prod_short](includes/prod_short.md)] en zon och en lagerplatskod i utleveransdokument för distributionslager.

* För avancerade konfigurationer där ett lagerställe använder dirigerad artikelinförsel och plockning använder [!INCLUDE [prod_short](includes/prod_short.md)] lagerplatsen som anges i fältet **Utlevns lagerställeskod** på **Lagerställekort**. Om ingen **Utlevns lagerställeskod** anges är fältet tomt. Om artikeln och utleveransens lagerplats inte överensstämmer lämnar [!INCLUDE [prod_short](includes/prod_short.md)] utleveransens lagerplats tomt.
* I andra fall använder [!INCLUDE [prod_short](includes/prod_short.md)] alltid den lagerplats som anges i fältet **Utlevns lagerställeskod** på **Lagerställekod**. Om en lagerplatskod inte har angetts använder [!INCLUDE [prod_short](includes/prod_short.md)] lagerplatskoden från källdokumentet.

## Hantera artiklar för montering mot kundorder i distributionslagerutleveranser

I montering mot kundorder-scenarier är fältet **Ant. att utleverera** på distributionslagerutleveransrader använt för att notera hur många enheter som monteras. Antalet bokförs sedan som monteringsutflöde när distributionslagerutleveransen bokförs. För andra distributionslagerutleveransrader är värdet i **Ant. att utleverera** noll.

När arbetare är klara med att montera en del av eller hela antalet för montering mot kundorder, registrera antalet på **Ant. att utleverera** på distributionslagerutleveransrad. Välj åtgärden **Bokför utleverans**. Monteringsutflödet bokförs, inklusive komponentförbrukningen. En utleverans för kvantiteterna bokförs för försäljningsordern.

Från monteringsordern kan du välja **Montering mot kundorder, dist.lager utleveransrad** för att komma åt distributionslagerutleveransraden.

När distributionslagerutleveransen har bokförts uppdateras olika fält på försäljningsorderraden för att visa förloppet i distributionslagret. Följande fält uppdateras också för att visa hur många antal för montering mot kundorder som återstår att monteras och levereras:

* **ATO Restnot. antal i lager**
* **ATO Restnot. antal i lager (bas)**

> [!NOTE]
> I alla scenarier där en del av antalet måste först vara monterat och ett annat ska levereras från lagret, skapas ett minimum på två distributionslagerutleveransrader. En är för antal för montering mot kundorder, och en är lagerantalet.
>
> Antalet för montering mot kundorder hanteras enligt beskrivningen i den här artikeln. Lagerkvantiteten hanteras som en vanlig distributionslagerutleverans. Mer information om kombinationsscenarion finns i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## Se även

[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
