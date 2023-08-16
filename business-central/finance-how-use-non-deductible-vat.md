---
title: Använd ej avdragsgill moms
description: I den här artikeln beskrivs hur du använder och rapporterar icke-avdragsgill moms.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, return, settlement'
ms.search.form: '50, 51, 52, 161, 187, 317, 403, 6640, 9401'
ms.date: 04/26/2023
ms.custom: bap-template
---

# Använd ej avdragsgill moms

I den här artikeln beskrivs hur du använder och rapporterar icke-avdragsgill moms.

## Skapa en inköpsfaktura med icke-avdragsgill moms

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.
2. Välj **Ny** för att skapa en inköpsfaktura och ange lämplig information i fakturahuvudet.
3. I avsnittet **Rader** skapar du en ny rad av vilken typ som helst, baserat på momsföretagsbokföringsgruppen och momsproduktbokföringsgruppen där du konfigurerar icke-avdragsgill moms.
4. I fältet **Antal** och **A-pris senaste inköp**, ange lämpliga värden.

    Om du markerade kryssrutan **Visa icke-avdragsgill moms på rader** på sidan **Momsinställningar** beräknas beloppen i fälten **Icke-avdragsgillt nettobelopp** och **Icke-avdragsgillt momsbelopp** baserat på fältet **Icke-avdragsgill moms %** på sidan **Bokföringsinställningar för moms**.

5. Bokföra fakturan

## Skapa en inköpsorder med icke-avdragsgill moms

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.
2. Välj **Ny** för att skapa en inköpsorder och ange lämplig information i dokumenthuvudet.
3. I avsnittet **Rader** skapar du en ny rad av vilken typ som helst, baserat på momsföretagsbokföringsgruppen och momsproduktbokföringsgruppen där du konfigurerar icke-avdragsgill moms.
4. I fältet **Antal** och **A-pris senaste inköp**, ange lämpliga värden.

    Om du markerade kryssrutan **Visa icke-avdragsgill moms på rader** på sidan **Momsinställningar** beräknas beloppen i fälten **Icke-avdragsgillt nettobelopp** och **Icke-avdragsgillt momsbelopp** baserat på fältet **Icke-avdragsgill moms %** på sidan **Bokföringsinställningar för moms**.

5. Bokför inköpsordern.

## Justera avrundade momsbelopp före bokföring av dokument

Om momsbelopp inte är avrundade på samma sätt i miljön och i det externa redovisningssystemet (det ursprungliga fakturadokumentet), kan du justera momsbeloppet innan du bokför dokumentet. Följ de här stegen innan du bokför dokumentet innan du gör den här ändringen.

1. I åtgärdsfönstret, välj **Statistik**.
2. Om du arbetar med en inköpsfaktura gör du så här:

    1. På snabbfliken **Rader** väljer du moms beloppet eller det icke-avdragsgilla momsbelopp
    2. Ställ in de värden du behöver från originaldokumentet och stäng sedan **Inköpsfakturastatistik**.

3.  Om du arbetar med en inköpsorder gör du så här:

    1. På snabbfliken **Fakturering**, välj **Antal momsrader** för att öppna sidan **Momsbeloppsrader**.
    2. Välj det momsbelopp eller icke-avdragsgillt momsbelopp som du vill korrigera.
    3. Ange de värden du behöver från originaldokumentet, stäng sidan **Momsbelopprader** och stäng sidan **Inköpsorderstatistik**.

Om du vill använda justeringar av momsbelopp måste du aktivera justeringarna. På sidan**Redovisningsinställningar** i fältet **Max. tillåten momsdifferens** ange högsta tillåtna momsbelopp för rättelse. På sidan **Inköpsinställningar** väljer du **Tillåt momsdifferens**.

Du kan justera värdena i fälten **Momsbelopp** och **Icke-avdragsgillt momsbelopp**. Värdet i fältet **Avdragsgillt momsbelopp** är resultatet av dessa två värden. Det belopp som du anger i **Icke-avdragsgillt momsbelopp** field can't be more than the amount that you enter in the **VAT Amount** field. Fältet **Max. tillåten momsdifferens** på sidan **Redovisningsinställningar** fungerar oberoende för avdragsgillt och icke-avdragsgillt momsbelopp på statistiska sidor när du vill justera momsbelopp.

> [!IMPORTANT]
> Du kan inte använda icke-avdragsgill moms på förskottsfakturorna.

## Se även

[Ekonomihantering](finance.md)

[Konfigurera beräknings- och bokföringsmetoder för moms](finance-setup-vat.md)  

[Konfigurera icke-avdragsgill moms](finance-setup-nondeductible-vat.md)

[Designdetaljer om icke-avdragsgill moms](design-details-nondeductible-vat.md)

[Rapportera moms till skattemyndigheterna](finance-how-report-vat.md)

[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
