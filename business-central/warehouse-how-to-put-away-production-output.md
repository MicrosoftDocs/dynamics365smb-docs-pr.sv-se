---
title: Införa utflöde från produktion
description: Hur du för in utflöde från produktionen beror på hur distributionslagret har ställts in som lagerställe.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e97f0e13f7b07ff59fd05908b6a3239d6cf70ebd
ms.sourcegitcommit: 026484766988b8727649c02fc8990b0646999bf1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5498643"
---
# <a name="put-away-production-or-assembly-output"></a>Föra in produktions- eller monteringsutflöde

Hur du för in utflöde från produktionen beror på hur distributionslagret har ställts in som lagerställe. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).  

I grundläggande lagerkonfigurationer där ditt lagerställe kräver bearbetning av artikelinförsel använder du dokumentet **Lager, artikelinförsel** för att bokföra produktionsutflöde och bokföra artikelinförsel för utflöde.  

> [!NOTE]  
> Lagerartikelinförsel stöds inte för monteringsprocesser. Du bokför en monteringsorder för att registrera utdata. Om du använder lagerplatser kan du flytta artiklar mellan olika lagerplatser senare. Mer information finns i [Flytta artiklar ad hoc i grundläggande distributionslagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

I avancerade lagerkonfigurationer där ditt lagerställe kräver både artikelinförsel- och inleveransbearbetning skapar du antingen ett internt artikelinförseldokument eller ett transportdokument för att föra in utflödet.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Så här för du in produktionsutflöde med lagerartikelinförsel

Det första steget när du skapar ett utflöde är att skapa det inkommande distributionslagerkravet. Förfrågan informerar distributionslagret att produktions- eller monteringsordern utflöde är klart för artikelinförsel.

### <a name="to-create-the-inbound-warehouse-request"></a>Så här skapar du det inkommande distributionslagerkravet  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Släppt produktionsorder** och välj sedan relaterad länk.  
2.  På produktionsordern som är klar för artikelinförsel väljer du åtgärden **Skapa inkommande dist.lagerbegäran**.  

> [!NOTE]  
> Du kan också skapa inkommande distributionslagerkrav genom att välja fältet **Skapa inkommande begärande** när du uppdaterar produktionsordern. Mer information finns i [Uppdatera eller omplanera produktionsorder](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Så här för du in utflöde med Lagerartikelinförsel:  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lagerinförsel** och välj sedan relaterad länk.  
2.  Skapa en ny lagerinförsel. Mer information finns i [Införa artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Om du vill komma åt produktionsorderns utflöde väljer du åtgärden **Hämta källdokument** och väljer den släppta produktionsordern.  
4.  Fyll i artikelinförselraderna efter behov.
5.  När raderna är färdiga att bokföras klickar du på **Bokför**. Bokföringen skapar de nödvändiga distributionslagertransaktionerna och bokför utflödet av artiklarna.  

Du kan också skapa en **Lagerinförsel** direkt från den släppta produktionsordern. Mer information finns i [Införa artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

När du bokför en lagerinförsel antas det att alla åtgärder bokförs enligt standardverksamhetsföljden, det vill säga att uflödesantalet bokförs enligt den senaste åtgärden. Du kan använda utflödesjournalen om du vill bokföra avvikelser i utflödesantalet, konfigurationen och bearbetningstiderna. Om det krävs att du bokför delvis efter att du har skapat lagerinförseln, kan du göra det för omställningstiderna och antalet för alla åtgärder utom den sista. I det fallet styrs den sista åtgärden av lagerinförseln.  

Om “Omställning, bearbetningstid” för den sista åtgärden måste bokföras, anger du utflödesantalet för den sista åtgärden till 0. Du kan också välja att inte bokföra den sista raden alls genom att ta bort den  

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>För att föra in monterings- eller produktionsutflöde i avancerade distributionslagerkonfigurationer
När du bokför utflöde från produktion eller monteringsorder på det lagerställe som har ställts in för att använda dirigerad artikelinförsel och plockning, placeras utflödet på den lagerplats som definierats i produktions- eller monteringsordern. 

I följande tabell beskrivs olika sätt att flytta artiklar i distributionslagret med avancerade konfigurationer, där alla lageraktiviteter måste utföras i ett riktat arbetsflöde. 

|**Om du vill**|**Se**|  
|------------|-------------|  
|Flytta artiklar med förslag för distributionslagertransport.|[Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet)|  
|Skapa en intern artikelinförsel för att föra in producerade eller monterade artiklar i en avancerad lagerkonfiguration.|[Skapa en intern artikelinförsel](warehouse-how-to-create-put-aways-from-internal-put-aways.md#to-create-an-internal-put-away)|

> [!NOTE]  
> Du kan inte ange källdokumentnumret, t. ex. produktionsordernumret, i dokument för intern artikelinförsel, artikelinförsel eller transport, för någon av de här procedurerna.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
