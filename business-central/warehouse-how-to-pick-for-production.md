---
title: 'Plocka eller flytta artiklar för produktion, montering eller projekt i grundläggande distributionslagerkonfigurationer'
description: 'När distributionslagrets lagerställe kräver att du behandlar plock, men inte utleveranser, använder du sidan Lagerplockning för att registrera plockning av komponenter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.forms: '9330, 931, 990008, 89, 900, 902'
---
# Plocka för produktion, montering eller jobb i grundläggande distributionslagerkonfigurationer

Hur du för in plockningskomponenter för produktions, jobb eller monteringsorder beror på hur distributionslagret har ställts in som lagerställe. Läs mer på [Ställa in lagerstyrning](warehouse-setup-warehouse.md).

I en avancerad lagerkonfiguration för det utgående flödet (plocka), på sidan **Lagerställekort** för lagerstället, slå på växlingsknappen **Begär plockning** men stäng av växlingsknappen **Kräver utleverans**.

Använd följande dokumenten för interna åtgärder:

* Lagerplockning
* Lagertransport

## Lagerplockningar

* När du registrerar en lagerplockning för en intern operation, bokförs till exempel produktion eller ett projekt, förbrukningen av markerade komponenterna samtidigt.
* Växlingsknappen **Lagerplats obligatorisk** på sidan **Lagerställekort** är valfritt.
* Om du använder lagerplockningar definierar fältet **Lagerställeskod** på en produktionsorderkomponentrad eller projektplaneringsrader lagerstället *ta*. Komponenterna minskas i lagerplatsen när du bokför förbrukningen.

## Lagerförflyttningar

* Lagertransport kräver att du stänger av växlingsknappen **Lagerplats obligatorisk** på sidan **Lagerställekort** för platsen.
* Lagerförflyttningar fungerar bara med produktionsorderna komponentrader och monteringsorderrader.
* När du registrerar en lagerförflyttning för en intern operation, registrerar du bara en fysisk transport av komponenter till en lagerplats i verksamhetsområdet. Du bokför inte förbrukning.
* Om du använder lagerförflyttningar definierar fältet **Lagerställeskod** på en produktionsorderkomponentrad, lagerstället *plats* i verksamhetsområdet. Lagerplatsen plats är där lagerpersonalen måste placera komponenterna.
* Registrera förbrukningen av plockade komponenter separat genom att bokföra en förbrukningsjournal eller monteringsorder.

>[!NOTE]
> Även om du har inaktiverat växlingsknappen **Kräver plockning** kan du använda ett dokument för **Dist.lager plockning**. Distributionslagerplockningar liknar **lagerplockningar**. Detta är användbart om du vill använda plockning i åtgärder och skicka i utgående lagerflöden.

### Produktion

Använd dokumentet **Lagerplockning** för att plocka produktionskomponenter i flödet till produktion.

För lagerställen som använder lagerplatser kan du utöka flödet till produktionen genom att använda dokumentet **Lagertransport**. Lagerförflyttningar är särskilt användbara vid bokföring av komponent. För att lära dig mer om hur komponentförbrukningen bokförs från till-produktion eller öppen produktionslagerplats, gå till [Bokföring av produktionskomponenter i en grundläggande konfiguration av distributionslager](#flushing-production-components-in-a-basic-warehouse-configuration).

### Montering  

Använd dokument **lagerförflyttning** för att flytta monteringskomponenter till monteringsområdet.

> [!NOTE]
> Dokumentet **Lagerförflyttning** kräver lagerplatser.

[!INCLUDE [prod_short](includes/prod_short.md)] stöder montering mot lager och montering mot kundorder typer för monteringsflöden. Om du vill lära dig mer om montering på beställning i det utgående lagerflödet, gå till [Hantering av artikel för montering mot kundorder med lagerplockning](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### Projekthantering  

Använd dokumentet **Lagerplockning** för att plocka projektkomponenter i flödet till projekthantering.

För lagerställen som använder lagerplatser kan du utöka flödet till projekt med dokumentet **Lagertransport**.

> [!NOTE]
> Möjligheten att plocka komponenter för projektplaneringsrader har lagts till [!INCLUDE[d365fin](includes/d365fin_md.md)] i utgivningscykel 2 år 2022. Om du vill börja använda funktionen måste en administratör aktivera **Funktionsuppdatering: Aktivera lager- och distributionslagerplockning från Projekt** på sidan **Funktionshantering**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] använder värdet i fältet **Återstående antal** på projektplaneringsraden när lagerplockningar skapas. Om du vill använda lagerplockningar för projekt måste du aktivera **Tillämpa användningslänk** på sidan **Projektkort** för projektet. På så sätt kan du spåra användningen mot din plan. Om du inte aktiverar detta fortsätter det återstående antalet att vara **0** och lagerplockningen skapas inte. Mer information finns i [Konfigurera projaktanvändningsspårning](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

## Plocka eller flytta för produktion, montering och projekt i en grundläggande lagerkonfiguration

Du kan skapa en lagerartikelplockning eller lagerförflyttning på tre sätt:  

* Från själva källdokumentet.  
* För flera källdokument samtidigt med hjälp av ett batch-jobb.  
* I två steg. Släpp källdokumentet för att göra källdokumentet klart för plockning. Skapa lagerplockningen eller transporten från dokumenten **lagerplockning** eller **lagerförflyttning**  dokumenten. Lagerplockning eller transport baseras på källdokumentet.  

### Så här skapar du en lagerplockning från källdokumentet

1. I källdokumentet, som kan vara en produktionsorder eller ett projekt, väljer du åtgärden **Skapa lagerartikelinförsel/plocka**.  
2. Markera kryssrutan **Skapa lagerplockning**.
3. Välj **OK**.

### Så här skapar du en lagerförflyttning från källdokumentet

1. I källdokumentet, som kan vara en produktionsorder, monteringsorder eller ett projekt, väljer du åtgärden **Skapa lagerartikelinförsel/plocka**.  
2. Markera kryssrutan **Skapa lagerförflyttning**.
3. Välj **OK**.

### Så här skapar du flera lagerplockningar eller transport med batch-jobbet

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Skapa lagerinförsel/plockning/rörelse** och väljer sedan relaterad länk.  
2. På snabbfliken **Dist.lagerkrav** använder du fälten **Ursprungsnr** och **Källdokument** om du vill filtrera efter vissa typer av dokument eller intervall med dokumentnummer. Du kan till exempel skapa plockningar för enbart produktionsorder.
3. På snabbfliken **Alternativ** aktiverar du växlingsknapparna **Skapa lagerplockning** eller **Skapa lagerförflyttning**.
4. Välj **OK**.

### Så här skapar du lagerplockningar eller rörelser i två steg

Om du vill plocka eller flytta komponenter för källdokumenten i två steg måste du släppa källdokumentet så att det är klart för plockning. Släppa källdokumenten för intern operation på följande sätt.  

|Källdokument|Släppningsmetod|  
|---------------------|--------------------|  
|Produktionsorder|På sidan **Planerad produktionsorder** ändrar du statusen för en order till **Släppt** eller använd sidan **Släppt produktionsorder** för att skapa en släppt produktionsorder.|  
|Monteringsorder|Ändrar statusen på en produktionsorder till **Släppt**.|
|Projekt | Ändra status för att **öppna** eller skapa projekt med statusen öppen direkt.|  

En lagerpersonal som har tilldelats plockningsartiklar kan skapa ett lagerartikelinförsel dokument för källdokumentet.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **lagerplockning** och eller **lagerförflyttning** väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **Källdokument** markerar du den typ av källdokument som du artikelinförsel är för.

    > [!NOTE]
    > Du kan inte använda dokument för **lagerplockning** för att plocka monteringskomponenter.
4. I fältet **Ursprungsnr** markerar du källdokumentet.  
5. Välj alternativt åtgärden **Hämta källdokument** för att välja dokumentet från en lista över inkommande källdokument som är klara för plockning på lagerstället.  
6. Välj **OK** för att fylla plock- eller transportrader enligt det valda källdokumentet.  

## När du vill registrera lagerplockning

1.  På sidan **lagerplockning** öppnar du dokumentet för att registrera plockning för.  
2. I fältet **Lagerställeskod** på plockningsraderna, är lagerplats som artiklarna måste plockas från lagerplatsen där artiklarna finns. Du kan ändra lagerplats vid behov.
3. Utför plockningen och ange plockningsantalet i fältet **Ant. att hantera**.

    Om du måste placera artiklar för en rad på flera lagerställen, t.ex. om hela antalet inte finns på lagret använder du åtgärden **Dela rad**, på snabbfliken **Rader**. Åtgärden skapar en rad för återstående antal att hantera.  
4. Välj åtgärden **Bokföra**.  

Följande händer under bokföringsförfarandet:

* Bokför förbrukningen av källdokumentraderna som plockades.
* Om lagerstället använder lagerställen kommer bokföringen även att skapa distributionslagertransaktioner för att bokföra ändringar i antalet lagerställen.

[!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## När du vill registrera lagerförflyttning

1.  På sidan **lagerförflyttning** öppnar du dokumentet för att registrera transporten för.  
2. I fältet **lagerplatskod** på plockningsraderna, föreslås lagerplatsen som artiklarna måste plockas från artikelns standardlagerplats och tillgänglighet. Du kan ändra lagerplats vid behov.  
3. Utför transport och ange flyttat antal i fältet **Ant. att hantera**. Värdet för Ta och Placera raderna måste vara samma. Annars kan du inte registrera transporten.

    Om du måste placera artiklar för en rad på flera lagerställen, t.ex. om hela antalet inte finns på lagret använder du åtgärden **Dela rad**, på snabbfliken **Rader**. Åtgärden skapar en rad för återstående antal att hantera.  
4. Välj åtgärden **Registrera lagertransport**.  

Följande händer under bokföringsförfarandet:

* Dist.lager transaktioner indikerar nu att komponenterna finns på lagerställen som har angetts på källdokumentets orderrader.. Till exempel monteringsorder, produktionskomponenter eller projektplaneringsrad.

>[!NOTE]
> Till skillnad från när du vill flytta komponenter med en lagerplockning, förbrukning inte bokförs när du registrerar en lagerförflyttning. Du registrerar förbrukning som ett separat steg genom att bokföra källdokumentet.

## Bokföra komponenter för produktion i en grundläggande lagerkonfiguration

Bokföringsmetoder påverkar flödet av komponenter i produktionen. Läs mer i [Bokföra komponenter utifrån operationens utflöde](production-how-to-flush-components-according-to-operation-output.md). Beroende på vilken bokföringsmetod som valts kan du plocka komponenter för produktion på följande sätt:

* Använd ett dokument för **Lagerplockning** för att registrera plockning för artiklar som använder **manuell** bokföringsmetod. När du registrerar en lagerplockning bokförs förbrukningen av plockade komponenter. 
* Använd ett dokument för **lagerförflyttning** med en referens till ett källdokument för att registrera plockningar för komponenter som använder **Manuell** bokföringsmetod. Du måste registrera förbrukning separat. Läs mer på [Batch-bokföra produktionsförbrukning](production-how-to-post-consumption.md). 
* Använd ett dokument för **lagerförflyttning** med en referens till ett källdokument för att registrera plockningar för komponenter som använder **Plocka + framåt** och **Plocka + bakåt** bokföringsmetod. Förbrukningen av komponenterna sker automatiskt antingen när du ändrar produktionsorderns status eller startar eller avslutar en åtgärd. Alla nödvändiga komponenter måste vara tillgängliga. Annars stoppas bokförs förbrukning som stoppas för den komponenten.
* Använd ett dokument för **lagerförflyttning** utan en hänvisning till ett källdokument eller andra sätt att registrera rörelsen av komponenter som använder bokföringsmetoden **Framåt** eller **Bakåt**. Förbrukningen av komponenterna sker automatiskt antingen när du ändrar produktionsorderns status eller startar eller avslutar en åtgärd. Alla nödvändiga komponenter måste vara tillgängliga. Annars stoppas bokförd förbrukning för den komponenten. Läs mer på [Flytta artiklar internt i grundläggande distributionslagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### Exempel

Du har en produktionsorder för 15 STYCK av artikeln SP-SCM1004. Några av artiklarna på komponentlistan måste bokföras manuellt i en förbrukningsjournal, och andra artiklar på listan kan plockas och bokföras automatiskt med hjälp av bokföringsmetoden **Plocka + bakåt**.  

Följande steg ger ett exempel på de åtgärder som olika användare gör och det relaterade svaret:  

1. Produktionsledaren släpper produktionsordern. Artiklar med bokföringsmetoden **Framåt** och utan verksamhetsföljdlänk dras av från den öppna produktionslagerplatsen.  
2. Arbetsledaren väljer åtgärden **Skapa lagerartikelinförsel/Plocka** för produktionsordern och aktiverar växlingsknappen **Skapa lagerplockning** och **Skapa lagerförflyttning**. Ett lagerplockningsdokument skapas för artiklar med bokföringsmetoden **Manuell** och en lagerförflyttning skapas för artiklar med bokföringsmetoden **Plockning + bakåt** och **Plockning + framåt**.
3. Lagerchefen tilldelar plockningar och transport till lagerarbetare.
4. Lagerarbetaren plockar artiklarna från lämpliga lagerställen och placerar dem i Till produktion-lagerstället eller lagerstället som anges på lagerförflyttning. Lagerplatsen kan vara för produktionsgrupp eller maskingrupp.  
5. Lagerarbetaren bokför plockningen. Antalet dras av från lagerplatserna.
6. Lagerarbetaren bokför transport. Antalet dras av från plocklagerställena och läggs till i förbrukningslagerstället. Fältet **Plockat antal** på komponentlistan för alla plockade artiklar uppdateras.  
7. Maskinoperatorn informerar produktionschefen att slutartiklarna är klara.  
8. Produktionsledaren använder utflödesjournalen eller produktionsjournalen för att bokföra utflödet. Antalet komponent artiklar som använder bokföringsmetoden **Plocka + Framåt** eller **Plocka + Bakåt** med operationsföljdslänkar dras från till produktionslagerplatsen.
9. Produktionschefen ändrar status för produktionsorder till **Avslutad**. Antalet av komponentartiklarna som använder bokföringsmetoden **Bakåt** dras av från öppna produktionslagerplatsen och antalet av komponentartiklarna som använder bokföringsmetoden **Plocka + bakåt** och ingen operationsföljdslänk dras av från till produktion-lagerplatsen.  

 Följande illustration visas när fältet **Lagerställeskod** på komponentlistan fylls enligt inställningen för lagerstället eller maskin-/produktionsgruppen.  

:::image type="content" source="media/binflow.png" alt-text="Översikt över när och hur fältet Lagerplatskod fylls i.":::

## Se relaterad [Microsoft utbildning](/training/paths/pick-ship-items-business-central/)

## Se även

[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
