---
title: Ad hoc-analyser inom inköp
description: Lär dig hur du använder dataanalysläget iför att analysera data i inköp.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analyses-in-purchasing"></a>Ad hoc-analyser inom inköp

Den här artikeln förklarar hur du analyserar inköpsdata från listsidor och frågor med hjälp av funktionen **Dataanalys**. Med funktionen kan du analysera data direkt från sidan, utan att behöva köra en rapport eller öppna ett annat program, t.ex. Excel. Dataanalys ger ett interaktivt och mångsidigt sätt att beräkna, sammanfatta och undersöka data. I stället för att köra rapporter med alternativ och filter kan du lägga till flera flikar som representerar olika uppgifter eller vyer för informationen. Några exempel är "Mina leverantörer" eller "Inköpsstatistik" eller någon annan vy du kan tänka dig. Mer information om hur du använder funktionen **Dataanalys** finns i [Analysera lista och frågedata med analysläge](analysis-mode.md).

Använd följande listsidor för ad hoc-analys av inköpsprocesser:

- [Inköpsordrar](https://businesscentral.dynamics.com/?page=9307)
- [Inköpsrader](https://businesscentral.dynamics.com/?page=518)
- [Bokförda inköpsfakturor](https://businesscentral.dynamics.com/?page=146)
- [Leverantörsreskontratransaktioner](https://businesscentral.dynamics.com/?page=29)
- [Redovisningstransaktioner](https://businesscentral.dynamics.com/?page=20)

## <a name="ad-hoc-analysis-scenarios-for-purchasing"></a>Ad hoc-analysscenarier för inköp

Använd funktionen **dataanalys** för snabb faktakontroll och ad hoc-analys:

- Om du inte vill köra en rapport
- Om det inte finns någon rapport för dina specifika behov
- Om du snabbt vill iterera för att få en bra överblick över en del av din verksamhet.

Följande avsnitt innehåller exempel på inköpsscenarier i [!INCLUDE [prod_short](includes/prod_short.md)].

| Yta | Till... | Öppna sidan i analysläge | Använda dessa fält |
| ---- | ----- | ------------------------------- |------------------- |
| [Översikt över GRNI (moms)](#example-goods-received-not-invoiced-grni-overview) | Få en översikt över inlevererade, ej fakturerade varor (GRNI) från flera leverantörer. | **Typ**, **Inlevererat bel. ej faktrd (BVA)** (filter i dessa fält), **Leverantörsnr.**, **Dokumentnr.**, **Nr.** och **Inlevererat bel. ej faktrd (BVA)** <br> **OBS!** Du måste anpassa sidan för att lägga till dessa fält. För mer information, gå till [Anpassa arbetsytan](ui-personalization-user.md). | 
| [Ekonomi (Leverantörsskulder)](#example-finance-accounts-payable) | Se vad du är skyldig dina kunder, kanske uppdelat i tidsintervall för när belopp ska betalas. | [Leverantörsreskontratransaktioner](https://businesscentral.dynamics.com/?page=29) | **Leverantörsnamn**, **Dokumenttyp**, **Verifikationsnr.**, **Förfallodatum år**, **Förfallodatum månad** och **Återstående belopp**. |

## <a name="example-goods-received-not-invoiced-grni-overview"></a>Exempel: Översikt över inlevererade varor, ej fakturerade (GRNI)

Följ dessa steg för att skapa en översikt över varor mottagna, ej fakturerade (GRNI) över leverantörer:
 
1. Öppna listsidan [Inköpsrader](https://businesscentral.dynamics.com/?page=518).
1. Anpassa sidan för att lägga till fältet **Mottaget belopp, ej fakturerat**. Om du vill anpassa sidan väljer du **Inställningar** och sedan **Anpassa**.
1. Aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet**).
1. I menyn **Ytterligare filter** (till höger, precis under menyn **Kolumner**), ange följande filter:
    - **Typ = Artikel**
    - **Inlevns bel. ej faktrd (BVA) > 0**. 
1. Dra the **Leverantörsnr.**, **Verifikationsnr.**, and **Nr.** till området **Radgrupper**. Dra fälten i den ordningen.
1. Lägg till fältet **Inlevererat bel. ej faktrd (LCY)** om du vill ta med det i översikten.
1. Om du vill göra analysen för ett visst år eller kvartal använder du ett filter på menyn **Ytterligare filter**. Menyn finns till höger på sidan, precis under menyn **Kolumner**.
1. Byt namn på analysfliken till **Översikt över inlevererade varor (GRNI)** eller något som beskriver den här analysen för dig.

## <a name="example-finance-accounts-payable"></a>Exempel: Finans (Leverantörsskulder)

För att se vad du är skyldig dina leverantörer, kanske uppdelat i tidsintervall för när belopp ska betalas gör du följande steg:

1. Öppna listsidan [Transaktioner för leverantörsreskontra](https://businesscentral.dynamics.com/?page=29) och aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet**).
1. Aktivera **Pivot**-läget (finns direkt ovanför **Sökfältet**).
1. Dra **Leverantörsnamn**, **Dokumenttyp** och **Verifikationsnr.** till området **Radgrupper** och dra sedan fältet **Återstående belopp** till området **Värden**.
1. Dra fälten **Förfallodatum år** och **Förfallodatum månad** till området **Kolumnetiketter**. Dra fälten i den ordningen.
1. Om du vill göra analysen för ett visst år eller kvartal använder du ett filter på menyn **Ytterligare filter** (till höger på sidan, precis under menyn **Kolumner**).
1. Byt namn på analysfliken till **Lev.skulder - ålder per månad** eller något som beskriver den här analysen för dig.

Följande bild visar resultatet av de här stegen.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Exempel på hur du gör dataanalyser på sidan Redovisningstransaktioner." lightbox="media/data-analysis-vendor-ledger-entries.png":::

## <a name="data-foundation-for-ad-hoc-analysis-on-purchasing"></a>Underlag för ad hoc-analys av inköp

När du bokför ett inköpdokument uppdaterar [!INCLUDE [prod_short](includes/prod_short.md)] leverantörens konto, redovisningen, artikeltransaktionstransaktionerna samt resurstransaktionstransaktionerna:

- För respektive inköpsdokument skapas en inköpstransaktion i tabellen **Redovisningstransaktion**. Dessutom skapas en transaktion på leverantörens konto i tabellen **Lev.reskontratransaktion** och en redovisningstransaktion på det relevanta kontot för leverantörsskulder. Dessutom kan bokföring av inköpet resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet.
- För varje inköpsrad, som tillämpligt, skapas poster i:
  - Tabellen **Artikeltransaktion** om inköpsraden är av typen Artikel.
  - Tabellen **Redovisningstransaktion** om inköpsraderna är av typen Redovisningskonto.
  - Tabellen **Resurstransaktion** om inköpsraden är av typen Resurs.
- Dessutom registreras inköpsdokument alltid i tabellerna **Inleveranshuvud** och **Inköpsfakturahuvud**.

Läs mer på [Bokföra inköp](purchasing-how-record-purchases.md#posting-purchases).

## <a name="see-also"></a>Se även

[Bokföra inköp](purchasing-how-record-purchases.md#posting-purchases)  
[Analysera listdata och frågedata med analysläge](analysis-mode.md)  
[Inköpsöversikt](purchasing-manage-purchasing.md)  
[Översikt över analyser, business intelligence och rapportering](reports-bi-reporting.md)  
[Inköpsöversikt](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
