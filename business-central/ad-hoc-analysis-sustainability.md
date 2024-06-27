---
title: Ad hoc-analys av data för hållbarhet
description: Lär dig hur du använder dataanalysläget iför att analysera data för hållbarhet.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI, sustainability, ESG'
ms.search.form: '6220,'
ms.date: 06/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad hoc-analys av data för hållbarhet

Den här artikeln förklarar hur du använder funktionen **Dataanalys** för att analysera data för hållbarhet direkt från listsidor och frågor. Du behöver inte köra en rapport eller växla till ett annat program, till exempel Excel. Funktionen ger ett interaktivt och mångsidigt sätt att beräkna, sammanfatta och undersöka data. I stället för att köra rapporter med alternativ och filter kan du lägga till flera flikar som representerar olika uppgifter eller vyer för informationen. Några exempel är "utsläppsöversikt" eller "utsläpp per scope" eller någon annan vy du kan tänka dig. Mer information om hur du använder funktionen **Dataanalys** finns i [Analysera lista och frågedata med analysläge](analysis-mode.md).

Använd följande listsidor för ad hoc-analys av data för hållbarhet:

- [Hållbarhetstransaktioner](https://businesscentral.dynamics.com/?page=6220)

## Scenarier för ad hoc-analys för hållbarhet

Använd funktionen **dataanalys** för snabb faktakontroll och ad hoc-analys:

- Om du inte vill köra en rapport.
- Om det inte finns någon rapport för dina specifika behov.
- Om du snabbt vill iterera för att få en bra överblick över en del av din verksamhet.

Följande avsnitt innehåller exempel på scenarier för hållbarhet i [!INCLUDE [prod_short](includes/prod_short.md)].

| Yta | Till... | Öppna sidan i analysläge | Använda dessa fält |
| ---- | ----- | ------------------------------- |------------------- |
| [Utsläppsöversikt (summan per kategori)](#example-emission-overview-sum-by-category) | Analysera dina utsläpp per kategori. | [Hållbarhetstransaktioner](https://businesscentral.dynamics.com/?page=6220) | **Kontokategori**, **Kontonamn**, **Utsläpp NH4**, **Utsläpp CO2** och **Utsläpp N2O**.|
| [Genomsnittliga utsläpp per kategori](#example-average-emissions-by-category) | Analysera dina genomsnittliga utsläpp per kategori. | [Hållbarhetstransaktioner](https://businesscentral.dynamics.com/?page=6220) | **Kontokategori**, **Kontonamn**, **Utsläpp NH4**, **Utsläpp CO2** och **Utsläpp N2O**.|
| [Utsläpp per scope](#example-emissions-by-scope) | Analysera dina utsläpp per scope. | [Hållbarhetstransaktioner](https://businesscentral.dynamics.com/?page=6220) | **Utsläpps-scope**, **Kontokategori**, **Utsläpp NH4**, **Utsläpp CO2** och **Utsläpp N2O**.|

## Exempel: Utsläppsöversikt (summan per kategori)

Följ dessa steg för att analysera dina utsläpp per kategori:

1. Öppna sidan [Hållbarhetstransaktioner](https://businesscentral.dynamics.com/?page=6220) och aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet**).
1. Aktivera **Pivot**-läget (finns direkt ovanför **Sökfältet**).
1. Dra fälten **Kontokategori** och **Kontonamn** till området **Radgrupper**. Dra fälten i den ordningen.
1. Dra fälten **Utsläpp NH4**, **Utsläpp CO2** och **Utsläpp N2O** till området **Värden**.
1. Byt namn på analysfliken till **Utsläppsöversikt (sum)** eller något som beskriver den här analysen för dig.

Följande bild visar resultatet av de här stegen.

:::image type="content" source="media/data-analysis-sustainability-entries.png" alt-text="Exempel 1 på hur du gör dataanalyser på sidan Hållbarhetstransaktioner." lightbox="media/data-analysis-sustainability-entries.png":::

## Exempel: Genomsnittliga utsläpp per kategori

Följ dessa steg för att analysera dina genomsnittliga utsläpp per kategori:

1. Öppna sidan [Hållbarhetstransaktioner](https://businesscentral.dynamics.com/?page=6220) och aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet**).
1. Aktivera **Pivot**-läget (finns direkt ovanför **Sökfältet**).
1. Dra fälten **Kontokategori** och **Kontonamn** till området **Radgrupper**. Dra fälten i den ordningen.
1. Dra fälten **Utsläpp NH4**, **Utsläpp CO2** och **Utsläpp N2O** till området **Värden**.
1. För varje fält i området **Värden** markerar du dem och ändrar aggregeringsfunktionen till `Average`.
1. Byt namn på analysfliken till **Utsläppsöversikt (avg)** eller något som beskriver den här analysen för dig.

Följande bild visar resultatet av de här stegen.

:::image type="content" source="media/data-analysis-sustainability-entries-avg.png" alt-text="Exempel 2 på hur du gör dataanalyser på sidan Hållbarhetstransaktioner." lightbox="media/data-analysis-sustainability-entries-avg.png":::

## Exempel: Utsläpp per scope

Följ dessa steg för att analysera dina utsläpp per scope:

1. Öppna sidan [Hållbarhetstransaktioner](https://businesscentral.dynamics.com/?page=6220) och aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet**).
1. Aktivera **Pivot**-läget (finns direkt ovanför **Sökfältet**).
1. Dra fälten **Utsläpps-scope** och **Kontokategori** till området **Radgrupper**. Dra fälten i den ordningen.
1. Dra fälten **Utsläpp NH4**, **Utsläpp CO2** och **Utsläpp N2O** till området **Värden**.
1. Byt namn på analysfliken till **Utsläppsöversikt per scope** eller något som beskriver den här analysen för dig.

Följande bild visar resultatet av de här stegen.

:::image type="content" source="media/data-analysis-sustainability-entries-scope.png" alt-text="Exempel 3 på hur du gör dataanalyser på sidan Hållbarhetstransaktioner." lightbox="media/data-analysis-sustainability-entries-scope.png":::

## Underlag för ad hoc-analys av hållbarhet

Den information som du anger i en hållbarhetsjournal är tillfällig och kan ändras så länge den finns i journalen. När du bokför hållbarhetsjournalen, överförs informationen till transaktioner på hållbarhetstransaktioner eller enskilda hållbarhetskonton, där den inte kan ändras. Du kan emellertid bokföra återföring eller rättning av transaktioner. Listsidan [Hållbarhetstransaktioner](https://businesscentral.dynamics.com/?page=6220) är den huvudsakliga datakällan för ad hoc-analys av hållbarhetsdata.

Mer information om hur du bokför hållbarhetstransaktioner finns i [Registrera hållbarhetstransaktioner](finance-sustainability-journal.md).

## Se även

[Registrera hållbarhetstransaktioner](finance-sustainability-journal.md)  
[Inbyggda hållbarhetsrapporter](sustainability-reports.md)   
[Översikt över analyser, business intelligence och rapportering](reports-bi-reporting.md)  
[Översikt över hållbarhetshantering](finance-manage-sustainability.md)   
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
