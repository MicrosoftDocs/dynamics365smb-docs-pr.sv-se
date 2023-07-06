---
title: Införa utflöde från produktion
description: I den här artikeln beskrivs hur du inför produktionsutflödet.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# <a name="put-away-production-or-assembly-output"></a><a name="put-away-production-or-assembly-output"></a><a name="put-away-production-or-assembly-output"></a>Föra in produktions- eller monteringsutflöde

Hur du för in utflöde från produktionen beror på hur distributionslagret har ställts in som lagerställe. Läs mer på [Ställa in lagerstyrning](warehouse-setup-warehouse.md).  

I grundläggande lagerkonfigurationer där ditt lagerställe kräver bearbetning av artikelinförsel använder du dokumentet **Lager, artikelinförsel** för att bokföra produktionsutflöde och bokföra artikelinförsel för utflöde.  

> [!NOTE]  
> Monteringsprocesser stöder inte lagerartikelinförsel. Du bokför en monteringsorder för att registrera utdata. Om du använder lagerplatser kan du flytta artiklar mellan olika lagerplatser senare. Läs mer på [Flytta artiklar ad hoc i grundläggande lagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

I avancerade lagerkonfigurationer där ditt lagerställe kräver både artikelinförsel- och inleveransbearbetning skapar du antingen ett internt artikelinförseldokument eller ett transportdokument för att föra in utflödet.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a><a name="to-put-away-production-output-with-an-inventory-put-away"></a><a name="to-put-away-production-output-with-an-inventory-put-away"></a>Så här för du in produktionsutflöde med lagerartikelinförsel

Det första steget när du inför utflöde är att skapa det inkommande distributionslagerkravet. Förfrågan informerar distributionslagret att produktions- eller monteringsordern utflöde är klart för artikelinförsel.

### <a name="to-create-the-inbound-warehouse-request"></a><a name="to-create-the-inbound-warehouse-request"></a><a name="to-create-the-inbound-warehouse-request"></a>Så här skapar du det inkommande distributionslagerkravet

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Utsläppta produktionsorder** och väljer sedan relaterad länk.  
2. Välj produktionsordern som är klar för artikelinförsel och sedan väljer du åtgärden **Skapa inkommande dist.lagerbegäran**.  

> [!NOTE]  
> Du kan också skapa inkommande distributionslagerkrav genom att välja fältet **Skapa inkommande begärande** när du uppdaterar produktionsordern. Läs mer på [Omplanera eller uppdatera produktionsorder direkt](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a><a name="to-put-output-away-with-an-inventory-put-away"></a><a name="to-put-output-away-with-an-inventory-put-away"></a>Så här för du in utflöde med Lagerartikelinförsel:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Lagerinförsel** och väljer sedan relaterad länk.  
2. Skapa en ny lagerinförsel. Läs mer på [Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Om du vill komma åt produktionsorderns utflöde väljer du åtgärden **Hämta källdokument** och väljer den släppta produktionsordern.  
4. Fyll i artikelinförselraderna efter behov.
5. När raderna är färdiga att bokföras klickar du på **Bokför**. Bokföringen skapar distributionslagertransaktionerna och bokför utflödet av artiklarna.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Du kan också skapa en **Lagerinförsel** direkt från den släppta produktionsordern. Läs mer på [Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

När du bokför en lagerinförsel antas det att alla åtgärder bokförs enligt standardverksamhetsföljden. Det vill säga att uflödesantalet bokförs enligt den senaste åtgärden. Du kan använda utflödesjournalen om du vill bokföra avvikelser i utflödesantalet, konfigurationen och bearbetningstiderna. Om du måste bokföra delvis efter att du har skapat lagerinförseln, kan du göra det för omställningstiderna och antalet för alla åtgärder utom den sista. Den sista åtgärden av lagerinförseln.  

Om “Omställning, bearbetningstid” för den sista åtgärden måste bokföras, anger du utflödesantalet för den sista åtgärden till 0. Du kan välja att inte bokföra den sista raden alls genom att ta bort den.

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a><a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a><a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>För att föra in monterings- eller produktionsutflöde i avancerade distributionslagerkonfigurationer

När du bokför utflöde från produktion eller monteringsorder på det lagerställe som använder dirigerad artikelinförsel och plockning, placeras utflödet på den lagerplats som definierats i produktions- eller monteringsordern. Lära dig mer om olika sätt att flytta artiklar i distributionslagret med avancerade konfigurationer, gå till [Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Du kan inte ange källdokumentnumret, t.ex. produktionsordernumret, i dokument för intern artikelinförsel, artikelinförsel eller transport för processer för produktions- eller monteringsutflöde.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
