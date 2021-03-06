---
title: Använda Excel för att importera data till Business Central
description: Använd standardkonfigurationspaketet för att lägga till kundinformation i Excel och återimportera data till Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 984186e8bb08cc9e99ab91dbc08f0e85c58e0804
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777954"
---
# <a name="importing-business-data-from-other-finance-systems"></a>Importera verksamhetsdata från andra finanssystem

När du registrerar dig på [!INCLUDE[prod_short](includes/prod_short.md)], kan du välja att skapa ett tomt företag så att du kan överföra din egen information och testa det nya [!INCLUDE[prod_short](includes/prod_short.md)]-företaget. Beroende på finanslösningen som används i din verksamhet idag, kan du överföra information om kunder, leverantörer, lager och bankkonton.  

Från ditt Rollcenter kan du starta en guide för assisterad konfiguration som hjälper dig att överföra affärsdata från en Excel-fil eller andra format. Typen av filer som du kan överföra, beror på tilläggen som är tillgängliga. Du kan till exempel migrera data från QuickBooks, eftersom [!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett tillägg som ska hantera omvandlingen från QuickBooks. Om du vill migrera data från andra finanslösningar, måste du antingen kontrollera om det finns ett tillägg för den lösningen eller importera från Excel.  

[!INCLUDE[prod_short](includes/prod_short.md)] inkluderar mallar förkonton, kunder, leverantörer och lagerartiklar som du kan välja att koppla, när du importerar dina data.

Du kan importera huvuddata och vissa transaktionsdata från andra finansiella system baserat på standardkonfigurationspaketet i [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **konfigurationspaket** kan du arbeta med paket för att importera och validera data innan du installerar paketet.  

> [!TIP]  
> Vi rekommenderar att du använder guider för datamigrering för att importera data från Dynamics GP, Dynamics NAV eller QuickBooks. Mer information finns i [Migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsinnehållet, eller [QuickBooks-datamigrering](ui-extensions-quickbooks-data-migration.md).

> [!NOTE]  
> För större implementeringar kan du använda RapidStart Services för [!INCLUDE[prod_short](includes/prod_short.md)] som är ett omfattande verktyg för att skapa nya lösningar baserade på kundernas affärskrav och konfigurationsdata. RapidStart Services inkluderar även funktioner för import av affärsdata. Mer information finns i [Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Om du vill importera artikelbilder kan du använda en särskild funktion på sidan **Lagerinställningar**. Mer information finns i [importera flera artikelbilder](inventory-how-import-item-pictures.md).

## <a name="importing-data-from-configuration-packages"></a>Importera data från ett konfigurationspaket
[!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett konfigurationspaket som du kan exportera till Excel och ange dina data där. Sedan kan du importera datan från Excel igen. Paketet består av 27 register, inklusive huvuddata som t. ex. kunder, leverantörer, artiklar och konton, andra grundläggande inställningstabeller, som till exempel leveransmetoder och transaktionstabeller som t. ex. rubrik och rader.  

> [!NOTE]  
>   Att arbeta med konfigurationspaket innebär avancerade funktioner och vi rekommenderar att du kontaktar din administratör. Mer information finns i [Importera data från äldre redovisningsprogram med ett konfigurationspaket](across-import-data-configuration-packages.md).

## <a name="working-with-data-in-excel"></a>Arbeta med data i excel
När du exporterar standardkonfigurationspaketet till Excel innehåller den genererade arbetsboken ett kalkylblad för varje register i förpackningen. För att underlätta dina arbetsuppgifter kan du dra nytta av XML behandlingsverktygen som ingår i Excel. Du kan även använda inbyggda Excel funktioner för att hjälp med dataformatering och för att ange data i rätt cell. Lägg till exempel till ett tomt kalkylblad och kopiera befintliga data till det. Gör en Excel-formel för att koppla data i omformnings kalkylarket mellan fälten i den exporterade kalkylarket och de bakåtkompatibla data för kunden. När du har mappat alla data kopierar du intervallet av data till tabellkalkylarket.  

> [!IMPORTANT]  
>  Ändra inte kolumnerna i kalkylark. Om de flyttats, ändras eller tas bort, kan kalkylarket inte importeras till [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Fält av BLOB-typen kan inte exporteras/importeras med Excel.

## <a name="tables-in-the-default-configuration-package"></a>Tabellerna i standardkonfigurationspaketet
Standardkonfigurationspaketet stöder följande tabeller:

-   Betalningsvillkor
-   Kund prisgrupp
-   Utleveransmetod
-   Säljare/Inköpare
-   Plats
-   Redovisningskonto
-   Kund
-   Leverantör
-   Artikel
-   Försäljningshuvud
-   Försäljningsrad
-   Inköpshuvud
-   Inköpsrad
-   Redovisnings- journalrad
-   Artikeljournalrad
-   Kundbokföringsmall
-   Leverantörsbokföringsmall
-   Lagerbokföringsmall
-   Måttenhet
-   Redovisnings- Rörelsebokföringsmall
-   Redovisnings- Produktbokföringsmall
-   Bokföringsinställningar
-   Distrikt
-   Artikelkategori
-   Förs.pris
-   Inköpspris

## <a name="see-also"></a>Se även
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Migrera lokala data till Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[QuickBooks datamigrering](ui-extensions-quickbooks-data-migration.md)  
[Importera flera artikelbilder](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]