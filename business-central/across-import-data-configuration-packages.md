---
title: "Använda Excel för att importera data till Financials | Microsoft Docs"
description: "Använd standardkonfigurationspaketet för att lägga till kundinformation i Excel och återimportera data till Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4526e8b11c9cbae36c7db58259499fbfa1b0c243
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Importera data från äldre redovisningsprogram med ett konfigurationspaket.
Du kan importera huvuddata och vissa transaktionsdata från andra finansiella system baserat på standardkonfigurationspaketet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I fönstret **Konfigurationspaket** kan du arbeta med paket för att importera och validera data innan du installerar paketet.  

> [!NOTE]  
> Konfigurationspaket ingår i RapidStart Services för [!INCLUDE[d365fin](includes/d365fin_md.md)], ett omfattande verktyg för att skapa nya lösningar baserade på kundernas affärskrav och konfigurationsdata. RapidStart Services inkluderar även funktioner för import av äldre data. Mer information finns i [Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

> [!TIP]  
>   Alternativt kan du använda guider för datamigrering för att importera data från QuickBooks eller Dynamics GP. Mer information finns i [QuickBooks datamigrering](ui-extensions-quickbooks-data-migration.md) eller [Dynamics GP datamigrering](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="working-with-data-in-excel"></a>Arbeta med data i excel
När du exporterar standardkonfigurationspaketet till Excel innehåller den genererade arbetsboken ett kalkylblad för varje register i förpackningen. För att underlätta dina arbetsuppgifter kan du dra nytta av XML behandlingsverktygen som ingår i Excel. Du kan även använda inbyggda Excel funktioner för att hjälp med dataformatering och för att ange data i rätt cell. Lägg till exempel till ett tomt kalkylblad och kopiera befintliga data till det. Gör en Excel-formel för att koppla data i omformnings kalkylarket mellan fälten i den exporterade kalkylarket och de bakåtkompatibla data för kunden. När du har mappat alla data kopierar du intervallet av data till tabellkalkylarket.  

> [!IMPORTANT]  
>  Ändra inte kolumnerna i kalkylark. Om de flyttats, ändras eller tas bort, kan kalkylarket inte importeras till [!INCLUDE[d365fin](includes/d365fin_md.md)].

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
-   Redovisningsjournalrad
-   Artikeljournalrad
-   Kundbokföringsmall
-   Leverantörsbokföringsmall
-   Lagerbokföringsmall
-   Måttenhet
-   Gen. rörelsebokföringsmall
-   Produktbokföringsmall
-   Bokföringsinställningar
-   Distrikt
-   Artikelkategori
-   Förs.pris
-   Inköpspris

## <a name="importing-customer-data"></a>Importera kunddata
När kunddatan har registrerats i datamigreringsfilerna i Excel importerar du data till [!INCLUDE[d365fin](includes/d365fin_md.md)]. I fönstret **konfigurationspaket** kan du importera data från Excel-filen och du kan kontrollera att data är konsekventa med [!INCLUDE[d365fin](includes/d365fin_md.md)] innan du installerar paketet.

## <a name="see-also"></a>Se även
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[QuickBooks datamigrering](ui-extensions-quickbooks-data-migration.md)  
[Dynamics GP Datamigrering](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

