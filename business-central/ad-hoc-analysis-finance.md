---
title: Ad hoc-analys av ekonomiska data
description: Lär dig hur du använder dataanalysläget för att analysera ekonomiska data.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad hoc-analys av ekonomiska data

Den här artikeln förklarar hur du använder funktionen **Dataanalys** för att analysera ekonomiska data direkt från listsidor och frågor. Du behöver inte köra en rapport eller växla till ett annat program, till exempel Excel. Funktionen ger ett interaktivt och mångsidigt sätt att beräkna, sammanfatta och undersöka data. I stället för att köra rapporter med alternativ och filter kan du lägga till flera flikar som representerar olika uppgifter eller vyer för informationen. Några exempel är "Totala tillgångar över tid", "Kundreskontra", "Leverantörsreskontra" eller någon annan vy du kan tänka dig. Mer information om hur du använder funktionen **Dataanalys** finns i [Analysera lista och frågedata med analysläge](analysis-mode.md).

Använd följande listsidor för att börja göra ad hoc-analys av ekonomiska processer:

- [Redovisningstransaktioner](https://businesscentral.dynamics.com/?page=20)
- [Kundreskontratransaktioner](https://businesscentral.dynamics.com/?page=25)
- [Leverantörsreskontratransaktioner](https://businesscentral.dynamics.com/?page=29)

## Ad hoc-analysscenarier för ekonomi

Använd funktionen **dataanalys** för snabb faktakontroll och ad hoc-analys:

- Om du inte vill köra en rapport.
- Om det inte finns någon rapport för dina specifika behov.
- Om du snabbt vill iterera för att få en bra överblick över en del av din verksamhet.

Följande avsnitt innehåller exempel på ekonomiscenarier i [!INCLUDE [prod_short](includes/prod_short.md)].

| Yta | Till... | Öppna sidan i analysläge | Använda dessa fält |
| ---- | ----- | ------------------------------- |------------------- |
| [Finans (Kundfordringar)](#example-finance-accounts-receivables) | Se vad dina kunder är skyldiga dig, till exempel uppdelat i tidsintervall för när belopp ska betalas. | [Kundreskontratransaktioner](https://businesscentral.dynamics.com/?page=25) | **Kundnamn**, **Förfallodatum** och **Återstående belopp** |
| [Ekonomi (Leverantörsskulder)](#example-finance-accounts-payable) | Se vad du är skyldig dina kunder, kanske uppdelat i tidsintervall för när belopp ska betalas. | [Leverantörsreskontratransaktioner](https://businesscentral.dynamics.com/?page=29) | **Leverantörsnamn**, **Dokumenttyp**, **Verifikationsnr.**, **Förfallodatum år**, **Förfallodatum månad** och **Återstående belopp**. |
| [Finans (resultaträkning)](#example-finance-income-statement) | Se din inkomst över inkomstkontona från kontoplanen, till exempel uppdelad i tidsintervall för när beloppen bokfördes. | [Redovisningstransaktioner](https://businesscentral.dynamics.com/?page=20) | **Redovisningskontonr.**, **Bokföringsdatum** och **Belopp**. |
| [Finans (totala tillgångar)](#example-finance-total-assets) | Se dina tillgångar över tillgångskontona från kontoplanen, till exempel uppdelad i tidsintervall för när beloppen bokfördes. | [Redovisningstransaktioner](https://businesscentral.dynamics.com/?page=20) | **Redovisningskontonr.**, **Bokföringsdatum** och **Belopp**. |

### Exempel: Finans (Kundfordringar)

För att se vad dina kunder är skyldiga dig, till exempel uppdelat i tidsintervall för när belopp ska betalas gör du följande steg:

1. Öppna listan [Kundreskontratransaktioner](https://businesscentral.dynamics.com/?page=25) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid *sökfältet* till höger).
1. Aktivera växlingsknappen **Pivot*-läget** (finns direkt ovanför **Sökfältet** till höger).
1. Dra nu fältet **Kundnamn** till området **Radgrupper** och dra **Återstående belopp** till området **Värden**.
1. Dra **Förfallodatum månad** till området **Kolumnetiketter**.
1. Om du vill göra analysen för ett visst år eller kvartal använder du ett filter på menyn **Analysfilter** (nedanför menyn **Kolumner** till höger).
1. Byt namn på analysfliken till **Ålderskonton per månad** eller något som beskriver den här analysen.

### Exempel: Finans (Leverantörsskulder)

För att se vad du är skyldig dina leverantörer, kanske uppdelat i tidsintervall för när belopp ska betalas gör du följande steg:

1. Öppna listsidan [Leverantörsreskontratransaktioner](https://businesscentral.dynamics.com/?page=29) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Ange analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet**).
1. Aktivera växlingsknappen **Pivot-läget** (finns direkt ovanför **Sökfältet** till höger).
1. Dra **Leverantörsnamn**, **Dokumenttyp** och **Verifikationsnr.** till området **Radgrupper** och dra sedan fältet **Återstående belopp** till området **Värden**.
1. Dra fälten **Förfallodatum år** och **Förfallodatum månad** till området **Kolumnetiketter**. Dra fälten i den ordningen.
1. Om du vill göra analysen för ett visst år eller kvartal använder du ett filter på menyn **Analysfilter** (nedanför menyn **Kolumner** till höger).
1. Byt namn på analysfliken till **Lev.skulder - ålder per månad** eller något som beskriver den här analysen.

Följande bild visar resultatet av de här stegen.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Exempel på hur du gör dataanalyser på sidan Redovisningstransaktioner." lightbox="media/data-analysis-vendor-ledger-entries.png":::

### Exempel: Finans (resultaträkning)

För att se din inkomst över inkomstkontona från kontoplanen uppdelad i tidsintervall för när beloppen bokfördes gör du följande:

1. Öppna listan [Redovisningstransaktioner](https://businesscentral.dynamics.com/?page=20) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet**).
1. Aktivera växlingsknappen **Pivot-läget** (finns direkt ovanför **Sökfältet** till höger).
1. Dra fältet **Redovisningskontonr** till området **Radgrupper** och dra **Belopp** till området **Värden**.
1. Dra **Bokföringsdatum månad** till området **Kolumnetiketter**.
1. För resultaträkningen filtrerar du på de konton du använder. I [!INCLUDE [prod_short](includes/prod_short.md)] demodata börjar dessa konton med "4", men din kontoplan kan vara annorlunda. Ange ett filter för konton på menyn **Analysfilter** (under menyn **Kolumner** till höger).

   > [!TIP]
   > För att se vilka konton som används i din konfiguration kör du rapporten [råbalans per period](https://businesscentral.dynamics.com/?report=38).

1. Byt namn på analysfliken till **Inkomst per månad** eller något som beskriver den här analysen.

### Exempel: Finans (totala tillgångar)

För att se dina tillgångar över tillgångskontona från kontoplanen uppdelad i tidsintervall för när beloppen bokfördes gör du följande:

1. Öppna listan [Redovisningstransaktioner](https://businesscentral.dynamics.com/?page=20) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Aktivera växlingsknappen **Pivot-läget** (finns direkt ovanför **Sökfältet** till höger).
1. Dra fältet **Redovisningskontonr** till området **Radgrupper** och dra **Belopp** till området **Värden**.
1. Dra **Bokföringsdatum månad** till området **Kolumnetiketter**.
1. För utdraget för totala tillgångar filtrerar du på de konton du använder. I [!INCLUDE [prod_short](includes/prod_short.md)] demodata börjar dessa konton med "10", men din kontoplan kan vara annorlunda. Ange ett filter för lämpliga konton på menyn **Ytterligare filter** (under menyn **Kolumner** till höger).

   > [!TIP]
   > För att se vilka konton som används i din konfiguration kör du rapporten [råbalans per period](https://businesscentral.dynamics.com/?report=38).

1. Byt namn på analysfliken till **Inkomst per månad** eller något som beskriver den här analysen.

## Underlag för ad hoc-analys av ekonomi

När du bokför journaler [!INCLUDE [prod_short](includes/prod_short.md)] skapas transaktioner i tabellen **Redovisningstransaktion**. Därför görs ad hoc-analyser av den allmänna ekonomin vanligtvis på sidan [Redovisningstransaktioner](https://businesscentral.dynamics.com/?page=20). För kundreskontra och leverantörsreskontra kan du analysera [kundreskontratransaktioner](https://businesscentral.dynamics.com/?page=25) respektive [leverantörsreskontratransaktioner](https://businesscentral.dynamics.com/?page=29).

Mer information finns i följande artiklar:

- [Underlag för ad hoc-analys av försäljning](ad-hoc-analysis-sales.md#data-foundation-for-ad-hoc-analysis-on-sales)
- [Underlag för ad hoc-analys av inköp](ad-hoc-analysis-purchasing.md#data-foundation-for-ad-hoc-analysis-on-purchasing)

## Se även

[Analysera listdata och frågedata med analysläge](analysis-mode.md)  
[Översikt över ekonomisk analys](bi.md)  
[Översikt över analyser, business intelligence och rapportering](reports-bi-reporting.md)  
[Översikt över ekonomi](finance.md)   
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]