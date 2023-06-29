---
title: Konvertera befintliga lagerställen till distributionslagerställen
description: Du kan definiera att ett befintligt lagerställe ska använda zoner och lagerställen och fungera som ett distributionslager.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: 15
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="convert-existing-locations-to-warehouse-locations"></a><a name="convert-existing-locations-to-warehouse-locations"></a>Konvertera befintliga lagerställen till distributionslagerställen
Du kan definiera att ett befintligt lagerställe ska använda zoner och lagerställen och fungera som ett distributionslager.  

Batch-jobbet där ett lagerställe definieras som ett distributionslager skapar ursprungliga distributionslagertransaktioner för dist.lager justeringslagerstället för alla artiklar som finns på lagerstället. Dessa ursprungliga transaktioner balanseras när transaktioner för fysiskt lager registreras när batch-jobbet är färdigt.  

Du kan skapa zoner och lagerställen före eller efter konverteringen. Den enda lagerstället som du måste skapa före konverteringen är den som ska användas som en framtida justeringslagerplats.  

> [!IMPORTANT]  
>  Du rensar alla negativa lagersaldon och eventuella öppna distributionslagerdokument innan du konverterar platsen för dist.lagerhantering, genom att köra en rapport för att hitta artiklar med negativt lagersaldo och öppna distributionslagerdokument för lagerstället. Mer information finns i Kontrollera negativt lagersaldo.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a><a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>Så här aktiverar du ett befintligt lagerställe att fungera som ett distributionslager
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Skapa dist.lagerplats** och väljer sedan relaterad länk.  
2.  I **Lagerställekod** fältet, ange det lagerställe som du vill aktivera för distributionslagerbearbetning.  
3.  I **Justering lagerställeskod** fältet, ange lagerstället på platsen dit ej synkroniserade dist.lager transaktioner lagras. Mer information finns i [Så här synkroniserar du justerade lagertransaktioner med tillhörande artikeltransaktioner](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).  

    Med hjälp av öppna artikeltransaktioner för angivet lagerställe skapas dist.lager journalrader som summerar alla kombinationer av artikelnummer, variantkod, enhetskod och, vid behov, partinr och serienummer kombineras i artikeltransaktionerna. Distributionslagerjorunalraderna bokförs sedan. Vid bokföringen skapas distributionslagertransaktioner som placerar lagret i distributionslagrets justeringslagerplats. **Justering lagerställeskod** anges också på lagerställekortet.  

4.  Om du vill se vilka artiklar som lagts till i justeringslagerstället under batch-jobbet kan du köra rapporten **Dist.lager just.lagerplats**.  
5.  När batch-jobbet **Skapa dist.lagerplats** är färdigt utför du och bokför en inventering av lagret. Mer information finns i [Inventera, justera och gruppera om lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md).  

> [!NOTE]  
>  Du bör köra det här batch-jobbet **Skapa dist.lagerplats** vid ett tillfälle då det inte påverkar det dagliga arbetet i systemet. I det här jobbet bearbetas alla transaktioner i tabellen **Artikeltransaktion** och om det finns många artikeltransaktioner kan jobbet ta flera timmar.  

 För lagerställen där Warehouse Managementsdokument inte användes före konverteringen måste du på nytt öppna och släppa källdokument som var delvis inlevererade eller delvis utlevererade före konverteringen.  

## <a name="see-also"></a><a name="see-also"></a>Se även
[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
