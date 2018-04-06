---
title: "Så här: Konvertera befintliga lagerställen till distributionslagerplatser | Microsoft Docs"
description: "Du kan definiera att ett befintligt lagerställe ska använda zoner och lagerplatser och fungera som ett distributionslager."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7d4b2c86174386faa86ab6c09faa463d26d3d2ac
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="convert-existing-locations-to-warehouse-locations"></a>Konvertera befintliga lagerställen till distributionslagerplatser
Du kan definiera att ett befintligt lagerställe ska använda zoner och lagerplatser och fungera som ett distributionslager.  

Batch-jobbet där ett lagerställe definieras som ett distributionslager skapar ursprungliga distributionslagertransaktioner för dist.lager justeringslagerplatsen för alla artiklar som finns på lagerstället. Dessa ursprungliga transaktioner balanseras när transaktioner för fysiskt lager registreras när batch-jobbet är färdigt.  

Du kan skapa zoner och lagerplatser före eller efter konverteringen. Den enda lagerplatsen som du måste skapa före konverteringen är den som ska användas som en framtida justeringslagerplats.  

> [!IMPORTANT]  
>  Du rensar alla negativa lagersaldon och eventuella öppna distributionslagerdokument innan du konverterar platsen för dist.lagerhantering, genom att köra en rapport för att hitta artiklar med negativt lagersaldo och öppna distributionslagerdokument för lagerstället. Mer information finns i Kontrollera negativt lagersaldo
.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>Så här aktiverar du ett befintligt lagerställe att fungera som ett distributionslager  
1.  Välj ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Skapa dist.lagerplats** och välj sedan relaterad länk.  
2.  I **Lagerställekod** fältet, ange det lagerställe som du vill aktivera för distributionslagerbearbetning.  
3.  I **Justering lagerplatskod** fältet, ange lagerplatsen på platsen dit ej synkroniserade dist.lager transaktioner lagras. Mer information finns i avsnittet ”Att synkronisera de justerade lagertransaktionerna med tillhörande artikeltransaktioner” i [Inventera, justera och gruppera lager](inventory-how-count-adjust-reclassify.md).  

    Med hjälp av öppna artikeltransaktioner för angivet lagerställe skapas dist.lager journalrader som summerar alla kombinationer av artikelnummer, variantkod, enhetskod och, vid behov, partinr och serienummer kombineras i artikeltransaktionerna. Distributionslagerjorunalraderna bokförs sedan. Vid bokföringen skapas distributionslagertransaktioner som placerar lagret i distributionslagrets justeringslagerplats. **Justering lagerplatskod** anges också på lagerställekortet.  

4.  Om du vill se vilka artiklar som lagts till i justeringslagerplatsen under batch-jobbet kan du köra rapporten **Dist.lager just.lagerplats**.  
5.  När batch-jobbet **Skapa dist.lagerplats** är färdigt utför du och bokför en inventering av lagret. Mer information finns i [Inventera, justera och gruppera om lager](inventory-how-count-adjust-reclassify.md).  

> [!NOTE]  
>  Du bör köra det här batch-jobbet **Skapa dist.lagerplats** vid ett tillfälle då det inte påverkar det dagliga arbetet i systemet. I det här jobbet bearbetas alla transaktioner i tabellen **Artikeltransaktion** och om det finns många artikeltransaktioner kan jobbet ta flera timmar.  

 För lagerställen där lagerstyrningsdokument inte användes före konverteringen måste du på nytt öppna och släppa källdokument som var delvis inlevererade eller delvis utlevererade före konverteringen.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

