---
title: Så här skapar du ett nytt företag | Microsoft Docs
description: Tabeller och sidor skapas i syfte att kunna använda RapidStart Services, men de innehåller inga data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c21d86c67c6020d1a32da4816246bc7aaf96c2ca
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779888"
---
# <a name="create-a-new-company"></a>Skapa ett nytt företag
Innan du kan använda RapidStart Services för [!INCLUDE[prod_short](includes/prod_short.md)] måste du först skapa ett nytt företag för vilket du vill genomföra en kundimplementering. När du skapar ett nytt företag skapas standardtabeller och sidor för [!INCLUDE[prod_short](includes/prod_short.md)] men det inte finns några data i dem.

Du kan dessutom tillämpa specifika inställningsdata till företaget, när du har initialiserat det. Information finns i ett konfigurationspaket, en .rapidstart-fil, med innehållet i ett komprimerat format.  

Exempelkonfigurationspaket, inklusive lands-/regionspecifika filer, ingår i demonstrationsföretaget CRONUS. Använd följande procedurer för att använda exempelkonfigurationspaketet med ett nytt företag.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Om du vill använda exempelkonfigurationspaket BASICCONFIG  
1. Öppna företaget CRONUS Sverige AB. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).
2. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Konfigurationspaket** och välj sedan relaterad länk.  
3. Välj paketet BASICCONFIG i listan och välj sedan åtgärden **Exportera paket**.  

Använd följande procedur för att skapa ett nytt företag och använd BASICCONFIG-paketet som en del av processen.  

## <a name="to-create-a-new-company"></a>Så här skapar du ett nytt företag:  
1. Skapa ett nytt företag. Mer information finns i [Skapa nya företag i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).
2. Du kan nu importera implementerings-rollcentret för RapidStart Services och importera det konfigurationspaket som du har exporterat från företaget CRONUS Sverige AB.

När du har skapat ett nytt företag, fylls vissa tabeller i automatiskt, även om ingen företagsmall kopplas. Du kan till exempel granska standardkoderna för att bokföra och gruppera transaktioner på sidan **Källkod**. Om du anger en lokal version av [!INCLUDE[prod_short](includes/prod_short.md)], ska du granska den här tabellen och överväga alla lokala språkproblem.

## <a name="about-data-tables"></a>Om datatabeller
[!INCLUDE[prod_short](includes/prod_short.md)]-datatabeller finns i två grundläggande typer: Huvud och Inställningar. När du vill lägga upp en företagskonfiguration kan du använda dessa typer för att fokusera din konfigurationstrategi.  

### <a name="master-data-tables"></a>Huvuddatatabeller  
I följande tabell visas exempel på huvuddatatabeller. När du initialiserar ett nytt företag är de här tabellerna tomma.  

|Tabellnr.|Tabellnamn|  
|-------------------|--------------------|  
|15|Redovisningskonto|  
|18|Kund|  
|23|Leverantör|  
|27|Artikel|  
|5050|Kontakt|  

### <a name="setup-data-tables"></a>Inställningsdatatabeller  
I följande tabell visas exempel på inställningsdatatabeller där du registrerar inställningsinformation i konfigurationsfrågeformulär. Tabellerna innehåller basinformation om när företaget skapas.  

|Tabellnr.|Tabellnamn|  
|-------------------|--------------------|  
|98|Redovisningsinställningar|  
|311|Försäljningsinställningar|  
|312|Inköpsinställningar|  
|313|Lagerinställningar|  

Förutom inställningsdatatabeller har [!INCLUDE[prod_short](includes/prod_short.md)] också inställningsdatatabeller som anger grundläggande information om företaget och dess affärsprocesser. I följande tabell visas några av dessa.  

|Tabellnr.|Tabellnamn|  
|-------------------|--------------------|  
|3|Betalningsvillkor|  
|4|Valuta|  
|6|Kundprisgrupper|  
|5700|Lagerställeenhet|

  

## <a name="see-also"></a>Se även  
[Koppla konfigurationen till nya företag](admin-apply-configuration-to-new-companies.md)  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]