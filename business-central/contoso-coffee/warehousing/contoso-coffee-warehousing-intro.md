---
title: Introduktion till Contoso Coffee
description: Översikt över scenarier som kan vara till hjälp när demonstrationsdatan för Contoso Coffee ska hjälpa dig lära dig hur du använder lagerstyrningsfunktionerna i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Introduktion till lagerstyrning för Contoso Coffee

Contoso Coffee är ett fiktivt företag som tillverkar kaffemaskiner för privat och kommersiellt bruk. **Contoso Coffee**-apparna för Business Central lägger till demonstrationsdata som du kan använda för att lära dig använda lagerstyrningsfunktionerna i Business Central. Du kan konfigurera lagerstyrningsfunktioner på olika sätt, se [Översikt över olika konfigurationsalternativ](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Appen tillhandahåller tre lagerställen som är optimerade för olika scenarier:

- **SILVER**  

  Detta lagerställe har konfigurerats till att använda lagerplatser. Det kan enkelt konfigureras för att stödja Grundläggande eller Avancerad. 

- **GUL**  

  Detta lagerställe använder den avancerade lagerkonfigurationen, men använder inte lagerplatser. Den kan konfigureras för att stödja grundläggande konfigurationer.

- **VIT**  

  Detta lagerställe använder den avancerade lagerkonfigurationen med dirigerad artikelinförsel och plockning, som möjliggör mer avancerade regler för hur artiklar flyttas i hela distributionslagret.

## Konfigurera lagerstyrningsdata för Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

När relevanta program har installerats går du till sidan [Contoso demoverktyg](https://businesscentral.dynamics.com/?page=5194) i [!INCLUDE [prod_short](../../includes/prod_short.md)], väljer raden *Distributionslagermodul* och använder åtgärden **Konfigurera** för att förbereda modulerna. Inställningarna beskrivs i följandetabeller:  

|Fält  |Beskrivning  |
|---------|---------|
|**Lagerplats**  |Lagerstället för grundläggande scenarier.|
|**Lagerställe, avancerat**  |Lagerstället för enkla logistikscenarier.|
|**Lagerställe för dirigerad plockning och artikelinförsel**  |Lagerstället för avancerad logistikscenarier.|
|**Lagerställe, på väg**  |Det lagerställe som ska användas för transitlagerstället i överföringsscenarier.|
|**Kundnr**  |Kunden som ska användas för grundläggande och enkla scenarier vid försäljningsåtgärder.|
|**Leverantörsnr**  |Den leverantör som ska användas för alla scenarier i inköpsåtgärder.|
|**Artikel 1 nr.**  |Huvudartikel att använda för alla scenarier.|
|**Artikel 2 nr.**  |Extra artikel att använda för alla scenarier.|
|**Artikel 3 nr.**  |Artikeln med spårning.|

Välj åtgärden **Skapa demonstrationsdata** när du är klar. Det tar några minuter att lägga till data i den underliggande databasen, men sedan är det dags att köra de olika scenarierna.  

> [!IMPORTANT]
> Om du kör scenarierna kanske du vill kontrollera att användaren har lagts till som för valda lagerställen. Mer information finns i [Så här skapar du dist.lager personal](../../warehouse-how-to-set-up-warehouse-employees.md).

## Scenarierna

Demonstrationsdata för Contoso Coffee stöder för närvarande följande lagerstyrningsscenarier för test och utbildning:

1.  [Genomgång av ankommande och avgående flöde i grundläggande distributionslagerkonfigurationer](warehouse-basic-flow-putaway-pick.md)
2.  [Genomgång av ankommande och avgående flöde i blandade distributionslagerkonfigurationer](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Genomgång av ankommande och avgående flöde i avancerad distributionslagerkonfiguration med dirigerad artikelinförsel och plockning](warehouse-directed-flow.md)

Läs stegen för respektive scenario i den relevanta artikeln.  

## Se även

[Ställa in lager](../../inventory-setup-inventory.md) 
[Hur du ställer in lager](../../inventory-how-setup-locations.md) 
[Lagerstyrning](../../warehouse-manage-warehouse.md) 
[Designdetaljer](../../design-details-warehouse-overview.md) 
