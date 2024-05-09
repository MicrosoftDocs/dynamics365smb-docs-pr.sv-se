---
title: Ad hoc-analys av försäljningsdata
description: Lär dig hur du använder dataanalysläget för att analysera försäljningsdata.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad hoc-analys av försäljningsdata

Den här artikeln förklarar hur du använder funktionen **Dataanalys** för att analysera försäljningsdata direkt från listsidor och frågor. Du behöver inte köra en rapport eller växla till ett annat program, till exempel Excel. Funktionen ger ett interaktivt och mångsidigt sätt att beräkna, sammanfatta och undersöka data. I stället för att köra rapporter med alternativ och filter kan du lägga till flera flikar som representerar olika uppgifter eller vyer för informationen. Några exempel är "Mina kunder" eller "Försäljningsstatistik" eller någon annan vy du kan tänka dig. Mer information om hur du använder funktionen **Dataanalys** finns i [Analysera lista och frågedata med analysläge](analysis-mode.md).

Använd följande listsidor för ad hoc-analys av försäljningsprocesser:

- [Försäljningsordrar](https://businesscentral.dynamics.com/?page=9305)
- Redovisningstransaktioner
- [Kundreskontratransaktioner](https://businesscentral.dynamics.com/?page=25)
- Artikeltransaktioner
- Bokförda försäljningsfakturor
- Försäljningsreturorder

## Ad hoc-analysscenarier för försäljning

Använd funktionen **dataanalys** för snabb faktakontroll och ad hoc-analys:

- Om du inte vill köra en rapport.
- Om det inte finns någon rapport för dina specifika behov.
- Om du snabbt vill iterera för att få en bra överblick över en del av din verksamhet.

Följande avsnitt innehåller exempel på försäljningsscenarier i [!INCLUDE [prod_short](includes/prod_short.md)].

| Yta | Till... | Öppna sidan i analysläge | Använda dessa fält |
| ---- | ----- | ------------------------------- |------------------- |
| [Försäljning (förväntad försäljningsvolym)](#example-sales-expected-sales-volume) | Analysera din förväntade försäljningsvolym. | [Försäljningsordrar](https://businesscentral.dynamics.com/?page=9305) | **Försäljningskundnamn**, **Försäljningskundnr.**, **Nr.** , **Belopp**, **Dokumentdatum år** och **Dokumentdatum månad**. |
| [Försäljning (Kundförsäljning i volym)](#example-sales-customer-sales-by-volume) | Få en överblick över kunder som har köpt mest eller som är skyldiga mest. | [Kundreskontratransaktioner](https://businesscentral.dynamics.com/?page=25) | **Kundnamn**, **Verifikationsnr**, **Belopp** och **Återstående belopp**. |
| [Finans (Kundfordringar)](#example-finance-accounts-receivables) | Se vad dina kunder är skyldiga dig, till exempel uppdelat i tidsintervall för när belopp ska betalas. | [Kundreskontratransaktioner](https://businesscentral.dynamics.com/?page=25) | **Kundnamn**, **Förfallodatum** och **Återstående belopp**. |

## Exempel: Försäljning (förväntad försäljningsvolym)

Så här analyserar du förväntad försäljningsvolym och försäljningsbelopp för ej levererade order för varje kund per år eller månad:

1. Öppna listan [Försäljningsorder](https://businesscentral.dynamics.com/?page=9305) och aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet**).
1. Aktivera **Pivot**-läget (finns direkt ovanför **Sökfältet**).
1. Dra **Försäljningskundnamn**, **Försäljningskundnr.** och **Nr.** till området **Radgrupper**. Dra fälten i den ordningen.
1. Dra fältet **Belopp** till området **Värden**.
1. Dra fälten **Dokument, Datum, År** och **Dokument Datum Månad** till området **Kolumnetiketter**. Dra fälten i den ordningen.
1. Om du vill göra analysen för ett visst år eller kvartal använder du ett filter på menyn **Ytterligare filter**. Menyn finns till höger på sidan, precis under menyn **Kolumner**.
1. Byt namn på analysfliken till **Förväntad försäljningsvolym** eller något som beskriver den här analysen för dig.

## Exempel: Försäljning (Kundförsäljning i volym)

För att producera en överblick över kunder som har köpt mest eller som är skyldiga mest, följ dessa stegen:

1. Öppna listan [Kundreskontratransaktioner](https://businesscentral.dynamics.com/?page=25) och aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet**).
1. Dra fältet **Kundnamn** till området **Radgrupper** och fältet **Dokumentnr.** under den.
1. Välj fälten **Belopp** och **Återstående belopp**.
1. Om du vill göra analysen för ett visst år eller kvartal använder du ett filter på menyn **Ytterligare filter**. Menyn finns till höger på sidan, precis under menyn **Kolumner**.
1. Byt namn på analysfliken till **Kund efter försäljningsvolym** eller något som beskriver den här analysen för dig.

Följande bild visar resultatet av de här stegen.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Exempel på hur du gör dataanalyser på sidan Redovisningstransaktioner." lightbox="media/data-analysis-customer-ledger-entries.png":::

## Exempel: Finans (Kundfordringar)

För att se vad dina kunder är skyldiga dig, till exempel uppdelat i tidsintervall för när belopp ska betalas gör du följande steg:

1. Öppna listan [Kundreskontratransaktioner](https://businesscentral.dynamics.com/?page=25) och aktivera analysläget.
1. På menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet**).
1. Aktivera **Pivot**-läget (finns direkt ovanför **Sökfältet**).
1. Dra fältet **Kundnamn** till området **Radgrupper** och dra fältet **Återstående belopp** till området **Värden**.
1. Dra **Förfallodatum månad** till området **Kolumnetiketter**.
1. Om du vill göra analysen för ett visst år eller kvartal använder du ett filter på menyn **Ytterligare filter**. Menyn finns till höger på sidan, precis under menyn **Kolumner**.
1. Byt namn på analysfliken till **Ålderskonton per månad** eller något som beskriver den här analysen för dig.

## Underlag för ad hoc-analys av försäljning

När du har angett information om en försäljningsorder och lagt till alla försäljningsorderrader kan du bokföra ordern. Bokföring skapas en leverans och en faktura. [!INCLUDE [prod_short](includes/prod_short.md)] uppdaterar kundens konto, huvudbok och artikeltransaktioner:

- För varje försäljningsorder skapas en försäljningstransaktion i tabellen **Redovisningstransaktion**. Dessutom skapas en transaktion på kundens konto i tabellen **Kundreskontra** och en redovisningstransaktion på det relevanta kontot för leverantörsreskontra. Dessutom kan bokföring av inköpsordern resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet.
- För varje orderrad skapas en artikeltransaktion i tabellen **Artikeltransaktion** (om försäljningsraden innehåller artikelnummer) eller en redovisningstransaktion i tabellen **Redovisningstransaktion** (om försäljningsraden innehåller ett redovisningskonto). Därutöver registreras order alltid i tabellerna **Utleveranshuvud** och **Försäljningsfakturahuvud**.

Om du vill veta mer om att lägga upp försäljningar går [Bokföra försäljning](ui-post-sales.md).

## Se även

[Bokföra försäljning](ui-post-sales.md)  
[Analysera listdata och frågedata med analysläge](analysis-mode.md)  
[Översikt försäljningsanalys](sales-analytics-overview.md)  
[Översikt över analyser, business intelligence och rapportering](reports-bi-reporting.md)  
[Försäljningsöversikt](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]