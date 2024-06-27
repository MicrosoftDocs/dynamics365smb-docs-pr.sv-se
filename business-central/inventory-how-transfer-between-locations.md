---
title: Så här överför du artiklar mellan olika distributionslagerplatser
description: Lär dig flytta lager från en plats eller ett lagerställe till en annan med grupperingsjournalen eller med överföringsorder.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 05/24/2024
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
ms.service: dynamics-365-business-central
---
# <a name="transfer-inventory-between-locations"></a>Överföra lager mellan olika lagerställen

Du kan överföra lagerartiklar mellan olika lägerställen genom att skapa överföringsorder. Du kan även använda artikelgrupperingsjournalen.

> [!NOTE]
> Om du vill överföra artiklar måste lägerställen och överföringsflöden ställas in. Om du vill ha mer information om hur du ställer in lagerställen går du till [Skapa lagerställen](inventory-how-setup-locations.md). Det går inte att använda överföringsorder för *tomma* platser.

## <a name="transfer-orders"></a>Överföringsorder

Du kan leverera en utgående överföring från ett lagerställe och ta emot den inkommande överföringen i målet. Du kan:

* Spåra kvantitet i transit
* Definiera kalendrar, verksamhetsföljder och ankommande och avgående hanteringstider för datumberäkning och planering. Mer information om planering finns i [Om planeringsfunktioner](production-about-planning-functionality.md).
* Använd olika distributionslagerfunktioner för inkommande och utgående lagerställen.
* Använd överföringsorder för direkta överföringar, med vissa begränsningar.

## <a name="item-reclassification-journals"></a>Artikelgrupperingsjournaler

Du kan använda sidan **Artikelgrupperingsjournaler** för att:

* Direktöverföring av artiklar mellan lagerställen.
* Flytta artiklar mellan lagerplatser. Om du vill veta mer om överföring av artiklar mellan lagerplatser går du till [ Flytta artiklar oplanerat i grundläggande konfiguration av distributionslager](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Ändra ett parti- eller serienummer till ett nytt parti- eller serienummer. Om du vill veta mer om gruppering av serie- och partinummer går du till [Omgruppera serie- eller partinummer](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Ändra utgångsdatumet till ett nytt datum.
* Omgruppera artiklar från ett tomt lagerställe till ett faktiskt lagerställe.
* Skapa distributionslagertransaktioner om du inte hanterar lageraktiviteter.

## <a name="to-transfer-items-with-a-transfer-order"></a>För att överföra artiklar med en överföringsorder.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **överföringsorder** och väljer sedan relaterad länk.
2. På sidan **Överföringsorder** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Om du har fyllt i fälten **Transitkod**, **Speditörkod** och **Speditör servicekod** på sidan **Överföringsflödespec.** när du lade upp överföringsflödet, fylls motsvarande fält i automatiskt på överföringsordern.

    När du fyller i fältet **Speditörsservice** beräknas datum för inleverans till det aktuella lagerstället genom att speditörens leveranstid tillförs utleveransdatumet.

3. Du kan fylla i rader på flera olika sätt:

    |Alternativ  |Beskrivning  |
    |---------|---------|
    |Manuellt     | På snabbfliken **Rader** fyller du i en rad för en artikel eller använder åtgärden **Välj artiklar** för att välja flera artiklar.        |
    |Automatiskt     | * Välj åtgärden **Hämta lagerställesinnehåll** om du vill välja befintliga artiklar från en viss lagerplats på lagerstället.<br><br>* Välj **Hämta inleveransrader** för att välja artiklar som precis har anlänt till det lagerställe där överföringen sker.        |

    Du kan nu hoppa över artiklarna.
4. Välj åtgärden **bokför**, välj alternativet **leverera**, och välj sedan **OK**-knappen.

    Artiklarna är nu på väg mellan de angivna lägerställena i enlighet med överföringsflöde.

    Som lagerarbetare på utleveranslagerstället fortsätter du med att inleverera artiklarna. Överföringsorderraderna är desamma som när de levereras och kan inte redigeras.
5. Välj åtgärden **bokför**, välj alternativet **inleverera**, och välj sedan **OK**-knappen.

### <a name="post-multiple-transfer-orders-in-a-batch"></a>Bokföra flera överföringsorder i en batch

I proceduren nedan beskrivs hur du bokför överföringsorder i en batch.

1. 1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **överföringsorder** och väljer sedan relaterad länk.  
2. På sidan **Överföringsorder** väljer du de order som ska bokföras.
3. I fältet **Nr.** öppnar du snabbmenyn och väljer **Välj fler**.
4. Markera kryssrutan för raderna för varje beställning som du vill bokföra.
5. Välj åtgärden **bokföra** och välj sedan åtgärden **Bokför batch**.
6. På sidan **Batch-bokför överföringsorder** fyller du i fälten efter behov.

   > [!TIP]
    > För överföringsorder som använder ett transitlagerstället kan du välja antingen **Leverera** eller **Inleverera**. Upprepa det här steget om du vill göra båda. För order där **direkt bokföring** är aktiverad fungerar båda alternativen på samma sätt och bokför ordern helt och hållet.

7. Välj **OK**.
8. Om du vill visa eventuella problem öppnar du sidan **Registrera felmeddelande**.

    > [!NOTE]
    > Det kan ta en stund att bokföra flera dokument och samtidigt blockera andra användare. Överväg att aktivera bakgrundsbokföring. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](/dynamics365/business-central/admin-job-queues-schedule-tasks).

### <a name="schedule-a-job-queue-entry-to-post-multiple-documents-in-a-batch"></a>Tidsplanera en jobbkötransaktion för att bokföra flera dokument i en batch

Du kan också använda jobbkön för att schemalägga bokföringen så att den sker vid en tidpunkt som passar organisationen. Inom ditt företag kanske det exempelvis passar bättre att köra vissa rutiner när merparten av datainmatningen har slutförts för dagen.

Följande förfarande visar hur du konfigurerar rapporten **Batch-bokför överföringsorder** så att denna automatiskt bokför direktöverföringsorder klockan 16.00 på vardagar. Den tiden är bara ett exempel. Stegen är liknande för de övriga dokument som stöds.  

1. Sök efter sidan **Jobbkötransaktioner** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **objekttyp som ska köras** väljer du **Rapport**.  
4. I fältet **Objekt-ID som ska köras** väljer du **5707 Batch-bokför överföringsorder**.
5. Markera kryssrutan **Rapportbegäransida**.
6. På begäransidan **Batch-bokför överföringsorder** välj alternativet **leverans**, filtrera **direktöverföring** och väljer **OK**.

   > [!IMPORTANT]
   > Det är viktigt att du anger filter. Annars bokför [!INCLUDE [prod_short](includes/prod_short.md)] alla dokument, även om de inte är klara. Överväg att applicera ett filter på fältet **Status** för värdet **Släppts**, samt ett filter på fältet **Publiceringsdatum** för värdet **..idag**. Om du vill lära dig mer om filter går du till [ Sortera, söka och filtrering](/dynamics365/business-central/ui-enter-criteria-filters).

7. Markera de relevanta kryssrutorna från **kör på måndagar** till **kör på fredagar**.
8. I fältet **starttid** anger du kl. **16:00**.
9. Välj åtgärden **Ställ in status till klar**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Så här överför du artiklar med artikelgrupperingsjournalen

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artikelgrupperingsjournaler** och väljer sedan relaterad länk.
2. På sidan **Artikelgrupp.journal** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I fältet **Lagerställeskod** ställer du in det lagerställe där artiklarna lagras för tillfället.

    > [!NOTE]  
    > För att överföra artiklar som inte har någon platskod, lämnar du fältet **lagerställekod**.
4. I fältet **Ny lagerställeskod** ställer du in det lagerställe som du vill överföra artiklarna till.
5. Välj åtgärden **Bokföra**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="undo-a-transfer-shipment"></a>Ångra överföringsutleverans

Om du hittar ett fel i en kvantitet på en bokförd överföringsorder, så länge som leveransen inte har tagits emot kan du enkelt korrigera antalet. På sidan **Bokför överföringsutleverans** skapar åtgärden **Ångra utleverans** korrigerande rader, enligt följande:

* Värdet i fältet **Utlevererat antal** på minskas med det antal som du har ångrat.
* Värdet i fältet **Ant. att utleverera** på ökas med det antal som du har ångrat.
* Kryssrutan **Korrigering** markeras för raderna.

Om antalet har levererats i en lagerutleverans infogas en rättningsrad i den bokförda lagerutleveransen.

Om du vill slutföra korrigeringen öppnar du överföringsordern på nytt, anger rätt antal och bokför ordern. Om du använder en lagerutleverans för att skicka order skapar du och bokför en ny lagerutleverans.

## <a name="see-also"></a>Se även

[Hantera lager](inventory-manage-inventory.md)  
[Konfigurera lagerställen](inventory-how-setup-locations.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
