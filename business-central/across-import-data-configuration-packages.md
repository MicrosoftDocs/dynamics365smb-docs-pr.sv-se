---
title: Använda Excel för att importera data till Business Central| Microsoft Docs
description: Använd standardkonfigurationspaketet för att lägga till kundinformation i Excel och återimportera data till Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 0d31e710c0b5d9e1dfa63c9c653b740fdcc12f11
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "926538"
---
# <a name="importing-business-data-from-other-finance-systems"></a>Importera verksamhetsdata från andra finanssystem
När du registrerar dig på [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du välja att skapa ett tomt företag så att du kan överföra din egen information och testa det nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företaget. Beroende på finanslösningen som används i din verksamhet idag, kan du överföra information om kunder, leverantörer, lager och bankkonton.  

Från ditt Rollcenter kan du starta en guide för assisterad konfiguration som hjälper dig att överföra affärsdata från en Excel-fil eller andra format. Typen av filer som du kan överföra, beror på tilläggen som är tillgängliga. Du kan till exempel migrera data från QuickBooks, eftersom [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett tillägg som ska hantera omvandlingen från QuickBooks. Om du vill migrera data från andra finanslösningar, måste du antingen kontrollera om det finns ett tillägg för den lösningen eller importera från Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] inkluderar mallar förkonton, kunder, leverantörer och lagerartiklar som du kan välja att koppla, när du importerar dina data.

Du kan importera huvuddata och vissa transaktionsdata från andra finansiella system baserat på standardkonfigurationspaketet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. På sidan **konfigurationspaket** kan du arbeta med paket för att importera och validera data innan du installerar paketet.  

> [!TIP]  
> Alternativt kan du använda guider för datamigrering för att importera data från QuickBooks eller Dynamics GP. Mer information finns i [QuickBooks datamigrering](ui-extensions-quickbooks-data-migration.md) eller [Dynamics GP datamigrering](ui-extensions-dynamicsgp-data-migration.md).

> [!NOTE]  
> För större implementeringar kan du använda RapidStart Services för [!INCLUDE[d365fin](includes/d365fin_md.md)], som är ett omfattande verktyg för att skapa nya lösningar baserade på kundernas affärskrav och konfigurationsdata. RapidStart Services inkluderar även funktioner för import av affärsdata. Mer information finns i [Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Om du vill importera artikelbilder kan du använda en särskild funktion på sidan **Lagerinställningar**. Mer information finns i [importera flera artikelbilder](inventory-how-import-item-pictures.md).

## <a name="importing-data-from-configuration-packages"></a>Importera data från ett konfigurationspaket
[!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett konfigurationspaket som du kan exportera till Excel och ange dina data där. Sedan kan du importera datan från Excel igen. Paketet består av 27 register, inklusive huvuddata som t.ex. kunder, leverantörer, artiklar och konton, andra grundläggande inställningstabeller, som till exempel leveransmetoder och transaktionstabeller som t.ex. rubrik och rader.  

> [!NOTE]  
>   Att arbeta med konfigurationspaket innebär avancerade funktioner och vi rekommenderar att du kontaktar din administratör. Mer information finns i [Importera data från äldre redovisningsprogram med ett konfigurationspaket](across-import-data-configuration-packages.md).

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

## <a name="see-also"></a>Se även
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[QuickBooks datamigrering](ui-extensions-quickbooks-data-migration.md)  
[Dynamics GP Datamigrering](ui-extensions-dynamicsgp-data-migration.md)  
[Importera flera artikelbilder](inventory-how-import-item-pictures.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
