---
title: Ad hoc-analys av data för anläggningstillgångar
description: Lär dig hur du använder dataanalysläget iför att analysera data för anläggningstillgångar.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5604, 20'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-fixed-assets-data"></a>Ad hoc-analys av data för anläggningstillgångar

Den här artikeln förklarar hur du använder funktionen **Dataanalys** för att analysera data för anläggningstillgångar direkt från listsidor och frågor. Du behöver inte köra en rapport eller växla till ett annat program, till exempel Excel. Funktionen ger ett interaktivt och mångsidigt sätt att beräkna, sammanfatta och undersöka data. I stället för att köra rapporter med alternativ och filter kan du lägga till flera flikar som representerar olika uppgifter eller vyer för informationen. Några exempel är "Totala tillgångar", "Avskrivningar över tid" eller någon annan vy du kan tänka dig. Mer information om hur du använder funktionen **Dataanalys** finns i [Analysera lista och frågedata med analysläge](analysis-mode.md).

Använd följande listsidor för att börja göra ad hoc-analys av anläggningstillgångars processer:

- [Anl.transaktioner](https://businesscentral.dynamics.com/?page=5604)
- [Redovisningstransaktioner](https://businesscentral.dynamics.com/?page=20)

## <a name="fixed-assets-ad-hoc-analysis-scenarios"></a>Scenarier för ad hoc-analys av anläggningstillgångar

Använd funktionen **dataanalys** för snabb faktakontroll och ad hoc-analys:

- Om du inte vill köra en rapport.
- Om det inte finns någon rapport för dina specifika behov.
- Om du snabbt vill iterera för att få en bra överblick över en del av din verksamhet.

Följande avsnitt innehåller exempel på scenarier för anläggningstillgångar i [!INCLUDE [prod_short](includes/prod_short.md)].

| Yta | Till... | Öppna sidan i analysläge | Använda dessa fält |
| ---- | ----- | ------------------------------- |------------------- |
| [Anläggningstillgångar (Aktuellt värde)](#example-fixed-assets-current-value) | Spåra tillgångsvärde, både över alla tillgångar och på en enda tillgång. | [Anl.transaktioner](https://businesscentral.dynamics.com/?page=5604) | **Avskrivningsregel**, **Anl.nr.**, **Anl.bokf.datum**, **Anl. bokföringstyp** och **Belopp** |
| [Tillgångarnas värde förändras över tid](#example-asset-value-changes-over-time) | Spåra tillgångarnas värde förändras över tid. | [Anl.transaktioner](https://businesscentral.dynamics.com/?page=5604) | **Anl.bokföringstyp**, **Anl.bokf.datum** och **Belopp** |
|[Avskrivningar av anläggningstillgångar över tid](#example-fixed-asset-depreciations-over-time) | Spåra avskrivningar över tid, både över alla tillgångar och på en enskild tillgång. | [Anl.transaktioner](https://businesscentral.dynamics.com/?page=5604) | **Avskrivningsregel**, **Anl.nr.**, **Anl.bokf.År**, **Anl.bokf.Månad**, **Belopp** och **Anl.bokföringstyp** |

### <a name="example-fixed-assets-current-value"></a>Exempel: anläggningstillgångars aktuella värde

Så här spårar du värdet på en eller flera anläggningstillgångar:

1. Öppna listan [Redovisningsposter](https://businesscentral.dynamics.com/?page=5604) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Dra fälten **Avskrivningsregel** och **Anl.nr.** till området **Radgrupper**.
1. Välj fälten **Anl.bokf.datum** och **Anl.bokföringstyp**.
1. Dra **Belopp** till området **Värden**.
1. Byt namn på analysfliken till **Översikt över tillgångar – värde** eller något som beskriver den här analysen.

Följande bild visar resultatet av de här stegen.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Exempel på hur du gör dataanalyser på sidan redovisning för anläggningstillgångar för att se tillgångens värde." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

### <a name="example-asset-value-changes-over-time"></a>Exempel: tillgångarnas värde förändras över tid

Så här spårar du förändringar i tillgångarnas värde över tid:

1. Öppna listan [Redovisningsposter](https://businesscentral.dynamics.com/?page=5604) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Aktivera växlingsknappen **Pivot-läget** (finns direkt ovanför **Sökfältet** till höger).
1. Dra fältet **Anl.bokföringstyp** till området **Radgrupper**.
1. Dra fälten **Anl.bokf.År** och **Anl.bokf.Månad** till området **Kolumnetiketter**.
1. Dra **Belopp** till området **Värden**.
1. Byt namn på analysfliken till **Tillgångarnas värde förändras över tid** eller något som beskriver den här analysen.

Följande bild visar resultatet av de här stegen.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png" alt-text="Exempel på hur du gör dataanalyser på sidan redovisning för anläggningstillgångar för att se tillgångarnas värde förändras över tid." lightbox="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png":::

### <a name="example-fixed-asset-depreciations-over-time"></a>Exempel: avskrivningar av anläggningstillgångar över tid

Följ dessa steg för att spåra avskrivningar för en eller flera anläggningstillgångar:

1. Öppna listan [Redovisningsposter](https://businesscentral.dynamics.com/?page=5604) och välj :::image type="content" source="media/analysis-mode-icon.png" alt-text="Aktivera analysläge."::: för att aktivera analysläget.
1. Gå till menyn **Kolumner** och ta bort alla kolumner (markera rutan bredvid **sökfältet** till höger).
1. Aktivera växlingsknappen **Pivot-läget** (finns direkt ovanför **Sökfältet** till höger).
1. Dra fälten **Avskrivningsregel** och **Anl.nr.** till området **Radgrupper**.
1. Dra fälten **Anl.bokf.År** och **Anl.bokf.Månad** till området **Kolumnetiketter**.
1. Dra **Belopp** till området **Värden**.
1. I filterfältet **Anl.bokföringstyp** välj **Avskrivning**.
1. Byt namn på analysfliken till **Avskrivningar över tid** eller något som beskriver den här analysen.

Följande bild visar resultatet av de här stegen.

:::image type="content" source="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png" alt-text="Exempel på hur du gör dataanalyser på sidan redovisning för anläggningstillgångar för att se avskrivningar över tiden." lightbox="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png":::

## <a name="data-foundation-for-ad-hoc-analysis-on-fixed-assets"></a>Underlag för ad hoc-analys av anläggningstillgångar

När du bokför anläggningstillgångsjournaler [!INCLUDE [prod_short](includes/prod_short.md)] skapas transaktioner i tabellen **Anl. transaktion**. Därför görs ad hoc-analyser av anläggningstillgångar vanligtvis på sidan [redovisning för anläggningstillgångar](https://businesscentral.dynamics.com/?page=5604).

## <a name="contributors"></a>Deltagare

*Microsoft underhåller den här artikeln. Delar av exemplen skrevs ursprungligen av följande deltagare.*

* [Aldona Stec](https://www.linkedin.com/in/aldona-stec-25283bb1) | [!INCLUDE[prod_short](includes/prod_short.md)] Konsult

## <a name="see-also"></a>Se även

[Analysera listdata och frågedata med analysläge](analysis-mode.md)  
[Översikt över analys av anläggningstillgångar](fa-analytics-overview.md)  
[Översikt över analyser, business intelligence och rapportering](reports-bi-reporting.md)  
[Översikt över anläggningstillgångar](fa-manage.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
