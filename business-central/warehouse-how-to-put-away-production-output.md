---
title: Så här för du in Produktionsutflöde | Microsoft Docs
description: Hur du för in utflöde från produktionen beror på hur distributionslagret har ställts in som lagerställe.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d7f941c5f0467f65ec3f94f00cacdd9c8fda6dc6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248406"
---
# <a name="put-away-production-or-assembly-output"></a>Föra in produktions- eller monteringsutflöde
Hur du för in utflöde från produktionen beror på hur distributionslagret har ställts in som lagerställe. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).  

I grundläggande lagerkonfiguration där ditt lagerställe kräver artikelinförselbearbetning, men inte inleveransbearbetning, använder du dokumentet **Lagerartikelinförsel** för att ordna och registrera artikelinförsel av utflöde.  

I avancerade lagerkonfigurationer där ditt lagerställe kräver både artikelinförsel- och inleveransbearbetning skapar du antingen ett internt artikelinförseldokument eller ett transportdokument för att föra in utflödet.  

Det första steget när du skapar ett utflöde är att skapa det ankommande distributionslagerkravet. Förfrågan informerar distributionslagret att produktions- eller monteringsordern utflöde är klart för artikelinförsel.

## <a name="to-create-the-inbound-warehouse-request"></a>Så här skapar du det ankommande distributionslagerkravet  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Släppt produktionsorder** och välj sedan relaterad länk.  
2.  På produktionsordern som är klar för artikelinförsel väljer du åtgärden **Skapa ankommande dist.lagerbegäran**.  

> [!NOTE]  
>  Du kan också skapa ankommande distributionslagerkrav genom att markera kryssrutan **Skapa ankommande rekvisition** när du uppdaterar produktionsordern. Mer information finns i [Uppdatera eller omplanera produktionsorder](production-how-to-replan-refresh-production-orders.md).  

## <a name="to-put-output-away-with-an-inventory-put-away"></a>Så här för du in utflöde med Lagerartikelinförsel:  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lagerinförsel** och välj sedan relaterad länk.  
2.  Skapa en ny lagerinförsel. Mer information finns i [Införa artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Om du vill komma åt produktionsorderns utflöde väljer du åtgärden **Hämta källdokument** och väljer den släppta produktionsordern.  
4.  Fyll i artikelinförselraderna efter behov.
5.  När raderna är färdiga att bokföras klickar du på **Bokför**. Bokföringen skapar de nödvändiga distributionslagertransaktionerna och bokför utflödet av artiklarna.  

Du kan också skapa en **Lagerinförsel** direkt från den släppta produktionsordern. Mer information finns i [Införa artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

När du bokför en lagerinförsel antas det att alla åtgärder bokförs enligt standardverksamhetsföljden, det vill säga att uflödesantalet bokförs enligt den senaste åtgärden. Du kan använda utflödesjournalen om du vill bokföra avvikelser i utflödesantalet, konfigurationen och bearbetningstiderna. Om det krävs att du bokför delvis efter att du har skapat lagerinförseln, kan du göra det för omställningstiderna och antalet för alla åtgärder utom den sista. I det fallet styrs den sista åtgärden av lagerinförseln.  

Om “Omställning, bearbetningstid” för den sista åtgärden måste bokföras, anger du utflödesantalet för den sista åtgärden till 0. Du kan också välja att inte bokföra den sista raden alls genom att ta bort den  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a>Så här för du in utflöde med en intern artikelinförsel
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Dist.lager intern art.införsel** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. Fyll i huvudet på en ny intern artikelinförsel med åtminstone **Lagerställekod**.  
4. Fyll i en rad för varje artikel som du vill flytta till distributionslagerplatsen. Du behöver endast fylla i fälten **Artikelnr** och **Antal**.  

    > [!NOTE]  
    >  När du väljer fältet **Artikelnr.** öppnas **Lagerplatsinnehåll lista** i stället för **Artikellista**. Det beror på att du vill föra in en artikel som finns på en viss lagerplats, ett lagerplatsinnehåll, och inte bara en artikel, och du vet redan vilken lagerplats som artikeln ska tas från.  

4.  Om du vill fylla kalkylarksraderna med hela lagerinnehållet eller det filtrerade lagerinnehållet från lager på platsen väljer du åtgärden **Hämta lagerplatsinnehåll**.  
5.  Välj åtgärden **Skapa artikelinförsel** så att de artiklar som du vill plocka ut från produktionen hamnar på en artikelinförselinstruktion där de väntar på att lagras i distributionslagret.  

> [!NOTE]  
>  När du har angett att ett distributionslager ska använda riktad artikelinförsel och plockning länkas lagret till tillverkningsstället via standardproduktionslagerplatser: de ankommande och avgående produktionslagerplatserna och den öppna fabrikslagerplatsen, som alla definieras på snabbfliken **Lagerplatser** på lagerställekortet. När du bokför utflödet för en produktionsorder placeras utflödet automatiskt i **Avgående produktionslagerplats**. Du följer samma procedur som ovan för att föra in produktionsutflödet, med det undantaget att i stället för att använda artikelns standardlagerplats flyttar eller för du in artiklarna från **Avgående produktionslagerplats** till deras respektive standardlagerplats.  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a>Om du vill manuellt ange en lagerplats för att lagra artiklar från produktionsutflödet:  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Transportförslag** och välj sedan relaterad länk.  
2.  Fyll i huvudet och skapa en rad för varje artikel som du vill flytta till distributionslagret.  
3.  Fyll i fälten **Från lagerplatskod** och **Till lagerplatskod** och ange kvantiteten i fältet **Antal**.  
4.  Om du vill fylla kalkylarksraderna med hela lagerinnehållet eller det filtrerade lagerinnehållet från lager på platsen väljer du åtgärden **Hämta lagerplatsinnehåll**.  
5. Välj åtgärden **Skapa transport**. Transportinstruktionerna för distributionslagret skapas med Ta- och Placera-rader som lagerpersonalen ska utföra.  

> [!NOTE]  
>  Du kan inte ange källdokumentnumret, t.ex. produktionsordernumret, i dokument för intern artikelinförsel, artikelinförsel eller transport, för någon av de här procedurerna.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
