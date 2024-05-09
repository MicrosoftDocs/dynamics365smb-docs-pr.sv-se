---
title: Använda Excel för att importera data
description: Använd standardkonfigurationspaketet för att lägga till kundinformation i Excel och återimportera data till Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'migration, Excel'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Importera affärsdata från andra ekonomisystem

När du registrerar dig på [!INCLUDE[prod_short](includes/prod_short.md)], kan du välja att skapa ett tomt företag så att du kan överföra din egen information och testa det nya [!INCLUDE[prod_short](includes/prod_short.md)]-företaget. Beroende på finanslösningen som används i din verksamhet idag, kan du överföra information om kunder, leverantörer, lager och bankkonton.  

Från ditt Rollcenter kan du starta en guide för assisterad konfiguration som hjälper dig att överföra affärsdata från en Excel-fil eller andra format. Typen av filer som du kan överföra, beror på tilläggen som är tillgängliga. Du kan till exempel migrera data från QuickBooks, eftersom [!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett tillägg som ska hantera omvandlingen från QuickBooks. Om du vill migrera data från andra finanslösningar, måste du antingen kontrollera om det finns ett tillägg för den lösningen eller importera från Excel.  

[!INCLUDE[prod_short](includes/prod_short.md)] inkluderar mallar förkonton, kunder, leverantörer och lagerartiklar som du kan välja att koppla, när du importerar dina data. Om du vill importera artikelbilder kan du använda en särskild funktion på sidan **Lagerinställningar**. Mer information finns i [importera flera artikelbilder](inventory-how-import-item-pictures.md).

> [!TIP]  
> Vi rekommenderar att du använder guider för datamigrering för att importera data från Dynamics GP, Dynamics NAV eller QuickBooks. Mer information finns i [Migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsinnehållet, eller [QuickBooks-datamigrering](ui-extensions-quickbooks-data-migration.md).

## Arbeta med data i Excel

Du kan använda Excel-tillägget för att förbereda befintligt innehåll för användning i [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Visa och redigera i Excel från Business Central](across-work-with-excel.md).  

## Importera data från konfigurationspaket

Du kan konfigurera lösningsspecifika konfigurationspaket för större implementeringsarbete. Mer information finns i [Konfigurera konfigurationspaket för företag](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (endast på engelska) i administrationsinnehållet.  

> [!NOTE]  
> Att arbeta med konfigurationspaket innebär avancerade funktioner och vi rekommenderar att du kontaktar din återförsäljningspartner. Mer information finns i [Ställa in konfigurationspaket för företag](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (endast på engelska).

Du kan importera huvuddata och vissa transaktionsdata från andra finansiella system baserat på standardkonfigurationspaketet i [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **konfigurationspaket** kan du arbeta med paket för att importera och validera data innan du installerar paketet. Till exempel kan du exportera konfigurationspaketet till Excel och konfigurera dina data där. Sedan kan du importera datan från Excel igen. Paketet består av 27 register, inklusive huvuddata som t. ex. kunder, leverantörer, artiklar och konton, andra grundläggande inställningstabeller, som till exempel leveransmetoder och transaktionstabeller som t. ex. rubrik och rader.  

När du exporterar standardkonfigurationspaketet till Excel innehåller den genererade arbetsboken ett kalkylblad för varje register i förpackningen. För att underlätta dina arbetsuppgifter kan du dra nytta av XML behandlingsverktygen som ingår i Excel. Du kan även använda inbyggda Excel funktioner för att hjälp med dataformatering och för att ange data i rätt cell. Lägg till exempel till ett tomt kalkylblad och kopiera befintliga data till det. Gör en Excel-formel för att koppla data i omformnings kalkylarket mellan fälten i den exporterade kalkylarket och de bakåtkompatibla data för kunden. När du har mappat alla data kopierar du intervallet av data till tabellkalkylarket.  

> [!IMPORTANT]  
> Ändra inte kolumnerna i kalkylark. Om de flyttats, ändras eller tas bort, kan kalkylarket inte importeras till [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Fält av BLOB-typen kan inte exporteras/importeras med Excel.

### Tabellerna i standardkonfigurationspaketet

Standardkonfigurationspaketet stöder följande tabeller:

- Betalningsvillkor
- Kund prisgrupp
- Utleveransmetod
- Säljare/Inköpare
- Plats
- Redovisningskonto
- Kund
- Leverantör
- Artikel
- Försäljningshuvud
- Försäljningsrad
- Inköpshuvud
- Inköpsrad
- Redovisnings- journalrad
- Artikeljournalrad
- Kundbokföringsmall
- Leverantörsbokföringsmall
- Lagerbokföringsmall
- Måttenhet
- Redovisnings- Rörelsebokföringsmall
- Redovisnings- Produktbokföringsmall
- Bokföringsinställningar
- Distrikt
- Artikelkategori
- Förs.pris
- Inköpspris

## Se även

[Migrera lokala data till Business Central Online (endast på engelska)](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[Ställa in konfigurationspaket för företag](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)  
[QuickBooks datamigrering](ui-extensions-quickbooks-data-migration.md)  
[Importera flera artikelbilder](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]