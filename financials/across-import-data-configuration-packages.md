---
title: "Använda Excel för att föra över äldre data till Financials | Microsoft Docs"
description: "Använda standardkonfigurationspaketet för att lägga till kundinformation i Excel och importera data till 365 Dynamics for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/27/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0151b1c3d8bddd4692c494d1c0e5d1c036da424e
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Importera data från äldre redovisningsprogrammet med ett konfigurationspaket.
Du kan importera huvuddata och vissa transaktionsdata från andra finansiella system baserat på standardkonfigurationspaketet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I fönstret **konfigurationspaket** kan du arbeta med paket för att importera och validera data innan du installerar paketet.  

Om du känner till RapidStart-tjänster för Microsoft Dynamics, känner du också till konfigurationpaket. Standardkonfigurationspaketet stöder de vanligaste typerna av data som du vill importera från äldre system. I Excel kan du sedan lägga till data från äldre system och konfigurera dem enligt affärslogik på [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="working-with-data-in-excel"></a>Arbeta med data i excel
När du exporterar standardkonfigurationspaketet till Excel innehåller den genererade arbetsboken ett kalkylblad för varje register i förpackningen. För att underlätta dina arbetsuppgifter kan du dra nytta av XML behandlingsverktygen som ingår i Excel. Du kan även använda inbyggda Excel funktioner för att hjälp med dataformatering och för att ange data i rätt cell. Lägg till exempel till ett tomt kalkylblad och kopiera befintliga data till det. Gör en Excel-formel för att koppla data i omformnings förslaget mellan fälten i den exporterade förslaget och de bakåtkompatibla data för kunden. När du har mappat alla data kopierar du intervallet av data till tabellförslaget.  

> [!IMPORTANT]  
>  Ändra inte kolumnerna i förslag. Om de flyttats, ändras eller tas bort, kan förslaget inte importeras till [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="tables-in-the-default-configuration-package"></a>Tabellerna i standardkonfigurationpaketet
Standardkonfigurationspaketet stöder följande tabeller:

-   Betalningsvillkor
-   Kund prisgrupp
-   Utleveransvillkor
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
När kunddatan har registrerats i dataflyttningsfilerna i Excel importerar du data till [!INCLUDE[d365fin](includes/d365fin_md.md)]. I fönstret **konfigurationspaket** kan du importera data från Excel-filen och du kan kontrollera att data är konsekventa med [!INCLUDE[d365fin](includes/d365fin_md.md)] innan du installerar paketet.

## <a name="see-also"></a>Se även
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
