---
title: Introduktion till demonstrationsdata för Contoso Coffee
description: Översikt över scenarier som kan vara till hjälp när demonstrationsdatan för Contoso Coffee ska hjälpa dig lära dig hur du använder funktionerna i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.date: 09/20/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '5194,'
ms.custom: bap-template
---

# <a name="introduction-to-contoso-coffee-demo-data"></a>Introduktion till demonstrationsdata för Contoso Coffee

Contoso Coffee är ett fiktivt företag som tillverkar kaffemaskiner för privat och kommersiellt bruk. **Contoso Coffee**-program för [!INCLUDE [prod_short](../includes/prod_short.md)] tillför demodata som du kan använda för att lära dig använda funktionerna i [!INCLUDE [prod_short](../includes/prod_short.md)].  

## <a name="set-up-contoso-coffee-data"></a>Konfigurera data för Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../includes/contoso-coffee-app-install.md)]

När programmen har installerats använder du åtgärden **Konfigurera** på sidan **Contoso-demonstrationsverktyg** för att förbereda följande moduler. Du kan välja att installera alla tillgängliga data, vilket omfattar konfigurations- och produktionsdata, eller endast konfigurationsdata.

 - Den **allmänna modul** för att förbereda allmänna inställningar som [!INCLUDE [prod_short](../includes/prod_short.md)] kräver. Till exempel nummerserier. 

Inställningarna beskrivs i följande tabell:  

|Fält  |Beskrivning  |
|---------|---------|
|**Startår** |Anger det första år som du vill använda för demonstrationsdata för Contoso Coffee. Beroende på företagets konfiguration är året antingen ett kalender år eller ett räkenskapsår.|
|**Lands-/regionskod**|Anger en lands-/regionkod för inrikes kunder och leverantörer.|
|**Företagstyp**    |Anger om det aktuella företaget måste rapportera moms eller omsättningsskatt. |
|**Prisfaktor**     |Anger en faktor för att omvandla ett pris från USD/EUR till lokal valuta. *1* innebär att priset är samma belopp i alla valutor. Ett högre värde används för att hämta priset i lokal valuta. |
|**Avrundningsnoggrannhet**  |Anger den avrundningsprecision som du vill skapa demonstrationsdata med.|

 - Den [produktionsmodul](manufacturing/contoso-coffee-manufacturing-intro.md) som ska förberedas för [produktionsscenarier](manufacturing/contoso-coffee-manufacturing-intro.md#scenarios).
 - Den [lagerstyrningsmodul](warehousing/contoso-coffee-warehousing-intro.md) som ska förberedas för [lagerstyrningsscenarier](warehousing/contoso-coffee-warehousing-intro.md#scenarios)
 - Den [servicemodul](service/contoso-coffee-service-intro.md) som ska förberedas för [servicescenarier](service/contoso-coffee-service-intro.md#scenarios)

När du har konfigurerat de moduler som du vill prova väljer du åtgärden **Generera** för att skapa demonstrationsdata för dem.

## <a name="see-also"></a>Se även

[Produktion](../production-manage-manufacturing.md)  
[Lagerstyrning](../warehouse-manage-warehouse.md)  
[Tjänst](../service-service.md)
<!-- [Projects and Jobs](../projects-manage-projects.md) -->

