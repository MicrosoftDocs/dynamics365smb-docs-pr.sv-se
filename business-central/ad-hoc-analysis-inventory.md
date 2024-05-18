---
title: Ad hoc-analys av lagerdata
description: Lär dig hur du använder dataanalysläget för att analysera lagerdata.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-inventory-data"></a>Ad hoc-analys av lagerdata

Den här artikeln förklarar hur du använder funktionen **Dataanalys** för att analysera lagerdata direkt från listsidor och frågor. Du behöver inte köra en rapport eller växla till ett annat program, till exempel Excel. Funktionen ger ett interaktivt och mångsidigt sätt att beräkna, sammanfatta och undersöka data. I stället för att köra rapporter med alternativ och filter kan du lägga till flera flikar som representerar olika uppgifter eller vyer för informationen. Några exempel är "lager som löper ut" eller "bästsäljare" eller någon annan vy du kan tänka dig. Mer information om hur du använder funktionen **Dataanalys** finns i [Analysera lista och frågedata med analysläge](analysis-mode.md).

Använd följande listsidor för ad hoc-analys av lagerprocesser:

- [Artikeltransaktioner](https://businesscentral.dynamics.com/?page=38)

## <a name="inventory-ad-hoc-analysis-scenarios"></a>Scenarier för ad hoc-analys för inventering

Använd funktionen **dataanalys** för snabb faktakontroll och ad hoc-analys:

- Om du inte vill köra en rapport.
- Om det inte finns någon rapport för dina specifika behov.
- Om du snabbt vill iterera för att få en bra överblick över en del av din verksamhet.

Följande avsnitt innehåller exempel på lagerscenarier i [!INCLUDE [prod_short](includes/prod_short.md)].

| Yta | Till... | Öppna sidan i analysläge | Använda dessa fält |
| ---- | ----- | ------------------------------- |------------------- |
| [Lagerbehållning](#example-inventory-on-hand) | Få en översikt över artiklar som är tillgängliga i ditt lager. | [Artikeltransaktioner](https://businesscentral.dynamics.com/?page=38) | **Artikelnr.**, **Återstående antal** |
|[Exempel: spår som går ut eller gammalt lager](#example-track-expiring-or-old-stock) | Få en överblick över artiklar i ditt lager som har funnits i lager länge och som inte säljer bra. | [Artikeltransaktioner](https://businesscentral.dynamics.com/?page=38) | **Bokföringsdatum år**, **Bokföringsdatum månad**, **Artikelnr**, **Bokföringsdatum**, **Transaktionstyp**, **Antal** och **Återstående antal**. |
| [Returnerade artiklar efter returorsak](#example-returned-items-by-return-reason) | Få en översikt över varor som kunder returnerar, kategoriserade efter returorsaken. Använd detta för analys för kvalitetskontroll. | [Artikeltransaktioner](https://businesscentral.dynamics.com/?page=38) | **Returorsakskod**, **Bokföringsdatummånad**, **Antal**, **Kostnadsbelopp**, **Bokföringsdatum**, **Dokumenttyp**, **Artikelnr** och **Dokumentnr.**. |
| Inventering genomströmning | Få en översikt över inköp och försäljning i lagret per månad eller kvartal. | [Artikeltransaktioner](https://businesscentral.dynamics.com/?page=38) | **Bokföringsdatum år**, **Bokföringsdatum månad**, **Artikelnr**, **Antal**, **Försäljningsbelopp**, **Kostnadsbelopp (aktuellt)** och **Bokföringsdatummånad** |
| [Lagerförflyttningar] | Få en översikt över hur varor i ditt lager flyttas mellan lagerställen. | [Artikeltransaktioner](https://businesscentral.dynamics.com/?page=38) | **Lagerställekod**, **Antal**, **Bokföringsdatum**, **Artikelnr.** |

## <a name="example-inventory-on-hand"></a>Exempel: Lagerbehållning

Så här analyserar du artiklar i lagret som finns i lager:

1. Öppna listan [Artikeltransaktioner](https://businesscentral.dynamics.com/?page=38) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet**).
1. Dra fältet **Art.nr.** till området **Radgrupper**. Dra fälten i den ordningen.
1. Dra fältet **Återstående antal** till området **Värden**.
1. Ställ in filtret **Inte lika** på **0** för **Återstående antal**. Om du inte tillåter negativa lagernivåer anger du filtret **Större än** till **0**.
1. Du kan också lägga till andra fält i analysen och kanske pivotera på lagerställe eller andra fält.
1. Byt namn på analysfliken till **Tillgängligt lager** eller något som beskriver den här analysen.

Följande bild visar resultatet av de här stegen.

:::image type="content" source="media/data-analysis-inventory-on-hand.png" alt-text="Exempel på hur du gör en analys av tillgängligt lager." lightbox="media/data-analysis-inventory-on-hand.png":::

## <a name="example-track-expiring-or-old-stock"></a>Exempel: spår som går ut eller gammalt lager

För att analysera artiklar i ditt lager som har funnits i lager länge och som inte säljer bra följer du stegen nedan:

1. Öppna listan [Artikeltransaktioner](https://businesscentral.dynamics.com/?page=38) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Dra fälten **Bokföringsdatum år**, **Bokföringsdatum månad** och **Artikelnr.** till området **Radgrupper**. Dra fälten i den ordningen.
1. I området **Kolumner** väljer du fälten **Bokföringsdatum**, **Transaktionstyp**, **Antal** och **Återstående antal**.
1. Ställ in filtret **Mindre än** på **Bokföringsdatum** för att definiera vad du menar med "gammal".
1. Byt namn på analysfliken till **Gammalt lager** eller något som beskriver den här analysen.

Följande bild visar resultatet av de här stegen.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Exempel på hur du gör dataanalyser av dödlager på sidan Artikeltransaktioner." lightbox="media/data-analysis-inventory-dead-stock.png":::

## <a name="example-returned-items-by-return-reason"></a>Exempel: Returnerade artiklar efter returorsak

Så här analyserar du returnerade artiklar sorterade efter orsakerna till att de returneras:

1. Öppna listan [Artikeltransaktioner](https://businesscentral.dynamics.com/?page=38).
1. Lägg till fältet **Returorsakskod** genom att anpassa sidan. På menyn **Inställningar** väljer du **Anpassa**.
1. Avsluta anpassningsläget.
1. Välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Öppna analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Dra fälten **Returorsakskod** och **Bokföringsdatum månad** till området **Radgrupper**. Dra fälten i den ordningen.
1. Dra fälten **Antal** och **Kostnadsbelopp** till området **Värden**.
1. Lägg till eventuella andra fält som du vill ha med i analysen och aktivera dem i området **Kolumner**. Du kan till exempel lägga till fälten **Bokföringsdatum**, **Dokumenttyp**, **Artikelnr No.** och **Dokumentnr.**.
1. Byt namn på analysfliken till **Returnerade artiklar efter returorsak** eller något som beskriver den här analysen för dig.  

## <a name="example-inventory-throughput"></a>Exempel: Inventering genomströmning

1. Öppna listan [Artikeltransaktioner](https://businesscentral.dynamics.com/?page=38) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Aktivera växlingsknappen **Pivot-läget** (finns direkt ovanför **Sökfältet** till höger).
1. Dra fälten **Bokföringsdatum år**, **Bokföringsdatum månad** och **Artikelnr.** till området **Radgrupper**.
1. Dra fälten **Antal**, **Försäljningsbelopp** och **Kostnadsbelopp (aktuella)** till området **Värden**.
1. Dra **Bokföringsdatum månad** till området **Kolumngrupper**.
1. Byt namn på analysfliken till **Lageromsättning per månad** eller något som beskriver den här analysen.  

## <a name="inventory-movements"></a>Lagerförflyttningar

Så här spårar du lagertransporter mellan lagerställen:

1. Öppna listan [Artikeltransaktioner](https://businesscentral.dynamics.com/?page=38) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Dra fältet **Platskod** till området **Radgrupper**.
1. Dra fältet **Kvantitet** till området **Värden**.
1. Lägg till eventuella andra fält som du vill ha med i analysen och aktivera dem i området **Kolumner**. Du kan till exempel lägga till fältet **Artikelnr.**.
1. Byt namn på analysfliken till **Tillgängliga rörelser** eller något som beskriver den här analysen.  

   > [!TIP]
   > Om du lägger till fältet Bokföringsdatum kan du även spåra rörelser över tid.

## <a name="data-foundation-for-ad-hoc-analysis-on-inventory"></a>Underlag för ad hoc-analys av lager

När du bokför en försäljningsorder, [!INCLUDE [prod_short](includes/prod_short.md)] uppdaterar kundens konto, huvudbokskonto och artikeltransaktioner.

- För varje försäljningsorderrad skapas en artikeltransaktion i tabellen **Artikeltransaktion** (om försäljningsraderna innehåller artikelnummer). Därutöver registreras order alltid i tabellerna **Utleveranshuvud** och **Försäljningsfakturahuvud**. Om du vill veta mer om att lägga upp försäljningar går [Bokföra försäljning](ui-post-sales.md).

När du bokför ett inköpdokument uppdaterar [!INCLUDE [prod_short](includes/prod_short.md)] leverantörens konto, redovisningen, artikeltransaktionstransaktionerna samt resurstransaktionstransaktionerna.

- För varje inköpsrad skapas transaktioner i tabellen **Artikeltransaktion** (om inköpsraden är av typen Artikel). Dessutom registreras inköpsdokument alltid i tabellerna **Inleveranshuvud** och **Inköpsfakturahuvud**. Läs mer på [Bokföra inköp](purchasing-how-record-purchases.md#posting-purchases).

## <a name="see-also"></a>Se även

[Analysera listdata och frågedata med analysläge](analysis-mode.md)  
[Översikt lageranalys](inventory-analytics-overview.md)  
[Översikt över analyser, business intelligence och rapportering](reports-bi-reporting.md)  
[Lageröversikt](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
