---
title: Designdetaljer – Icke-avdragsgill moms
description: 'Denna artikel ger information om ej avdragsgill moms (VAT) är den moms som betalas av en inköpare, men det är inte avdragsgill från köparens egen momsskuld.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
---

# Designdetaljer: Icke-avdragsgill moms

Ej avdragsgill moms (VAT) är den moms som betalas av en inköpare, men det är inte avdragsgill från köparens egen momsskuld. Eftersom det kan vara svårt att veta var och hur en artikel används, måste du kontakta lokala skattemyndigheter i ditt land eller region för att avgöra om en viss procent andel av momsen är avdragsgill. Även när du vet att en viss procentandel av momsen inte är avdragsgill finns det olika modeller för att hantera icke avdragsgilla belopp då de är relaterade till **artiklar** och **anläggningstillgångar**.

## Förutsättningar för att använda icke avdragsgill moms

Följ de här stegen om du vill använda och bokföra icke avdragsgill moms.

1. På sidan **momsinställning**, välj **Aktivera ej avdragsgill moms** för att aktivera funktionen.
2. På sidan **Bokföringsinställningar för moms** väljer du vilka momsbokföringsmallar som kan använda icke avdragsgill moms.

## Exempel

För följande exempel är icke avdragsgill moms aktiverad och följande inställningar slutförs:

- Fältet **Moms produktbokföringsmall** anges till **NDVAT**.
- På sidan **Bokföringsinställningar för moms**:

    - **NDVAT** anges som momsproduktbokföringsmall och **INRIKES** anges som rörelsebokföringsmall för moms.
    - Värdet i fältet **Moms-ID** måste vara unikt.
    - Fältet **Moms %** anges till **25**.
    - Fältet **Tillåt icke avdragsgill moms** till **Tillåt**.
    - Fältet **Icke avdragsgill moms %** till **100**.
    - Fältet **Momsberäkningstyp** ställs in som **Normal moms**.
    - Endast kontot för utgående moms och ingående moms är konfigurerade.

Alla exempel använder artiklar och anläggningstillgångar där produktbokföringsmallar för moms är **NDVAT**.

### Artiklar

En ny artikel har **NDVAT** angetts som produktbokföringsmallar för moms. I inköpsdokumentet **Antal** = **1** och **Inköpspris exkl. moms** = **1 000,00**.

Oavsett vilket alternativ som används är resultatet i momstransaktionen detsamma.

| Dokumenttyp | Kontakttyp | Bas | Momsbelopp | Icke-avdragsgillt nettobelopp | Icke-avdragsgillt momsbelopp |
|---|---|---|---|---|---|
| Fakturera | Inköp | 0.00 | 0.00 | 1,000.00 | 250.00 |

Informationen visas i värdetransaktionerna.

> [!NOTE]
> Du kan aktivera fältet **Använd för artikelkostnad** på sidan **momsinställningar** .

#### Använd för artikelkostnad har inte aktiverats

| Artikeltransaktionstyp | Transaktionstyp | Kost.belopp (faktiskt) | Antal i artikeltrans. |
|---|---|---|---|
| Inköp | Direkt kostnad | 1,000.00 | 1 |

#### Använd för artikelkostnad har aktiverats

| Artikeltransaktionstyp | Transaktionstyp | Kost.belopp (faktiskt) | Antal i artikeltrans. |
|---|---|---|---|
| Inköp | Direkt kostnad | 1,250.00 | 1 |

### Anläggningstillgångar

En ny anläggningstillgång har förvärvskostnadskontot inställt på att använda **NDVAT** produktbokföringsmallen med moms. I inköpsdokumentet **Antal** = **1** och **Inköpspris exkl. moms** = **1 000,00**.

Oavsett vilket alternativ som används är resultatet i momstransaktionen detsamma.

| Dokumenttyp | Kontakttyp | Bas | Momsbelopp | Icke-avdragsgillt nettobelopp | Icke-avdragsgillt momsbelopp |
|---|---|---|---|---|---|
| Fakturera | Inköp | 0.00 | 0.00 | 1,000.00 | 250.00 |

Informationen visas i anläggningstillgångstransaktionerna.

> [!NOTE]
> Du kan aktivera fältet **Använd för kostnad för anläggningstillgång** på sidan **momsinställningar** .

#### Använd för anläggningstillgångens kostnad är inte aktiverad

| Dokumenttyp | Anl. bokföringstyp | Momsbelopp | Momsbelopp |
|---|---|---|---|
| Fakturera | Anskaffningskostnad | 1,000.00 | 250.00 |

#### Använd för anläggningstillgångens kostnad är aktiverad

| Dokumenttyp | Anl. bokföringstyp | Momsbelopp | Momsbelopp |
|---|---|---|---|
| Fakturera | Anskaffningskostnad | 1,000.00 | 250.00 |
| Fakturera | Anskaffningskostnad | 250.00 | 0.00 |

## Se även

[Konfigurera ej avdragsgill moms](finance-setup-nondeductible-vat.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
