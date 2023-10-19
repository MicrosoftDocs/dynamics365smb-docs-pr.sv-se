---
title: Introduktion till servicehantering för Contoso Coffee
description: Den här artikeln introducerar dig till Consoso Coffee-demonstrationsdata för servicehantering.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# <a name="introduction-to-contoso-coffee-service-management"></a>Introduktion till servicehantering för Contoso Coffee

Contoso Coffee är ett fiktivt företag som tillverkar kaffemaskiner för privat och kommersiellt bruk. **Contoso Coffee**-programmen för Business Central lägger till demonstrationsdata som du kan använda för att lära dig använda funktionerna för servicehantering i Business Central.

Detta program innehåller flera element som används för de viktigaste genomgångarna:

- Resurser med tilldelade färdigheter
- Artiklar konfigurerade att skapa serviceartiklar
- Låneartiklar

> [!IMPORTANT]
> Innan du kör något av scenarierna för Contoso Coffee bokför du eventuella artikeljournalrader med ingående balanser. Mer information finns i avsnittet [Konfigurera data för Contoso Coffee](#set-up-contoso-coffee-service-management-data).
>
> 
## <a name="set-up-contoso-coffee-service-management-data"></a>Konfigurera servicehanteringsdata för Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

När relevanta program har installerats går du till sidan [Contosos demoverktyg](https://businesscentral.dynamics.com/?page=5194) i [!INCLUDE [prod_short](../../includes/prod_short.md)] väljer du raden *Servicemodul* och använder åtgärden **Konfigurera** för att förbereda modulerna. Inställningarna beskrivs i följandetabeller:  

|Fält  |Description  |
|---------|---------|
|**Kundnr**  |Den kund som ska användas för scenarierna i försäljningsåtgärderna.|
|**Leverantörsnr**  |Den leverantör som ska användas för alla scenarier i inköpsåtgärder.|
|**Artikel 1 nr.**  |Den artikel som ska användas för reparations- och underhållsscenarier.|
|**Serviceartikelnr 1.**  |Artikeln av typen "service" som ska använda reparationsscenariot.|
|**Serviceartikelnr 2.**  |Artikeln av typen "service" som ska använda reparationsscenariot.|
|**Resurs 1 nr.**  |Den resurs som ska användas för kontraktscenarierna.|
|**Resurs 2 nr.**  |Den resurs som ska användas för reparationsscenarierna.|
|**Serviceplats** |Anger det distributionslager som du vill använda för serviceåtgärder. Standardvärdet är *HUVUD*, men du kan ändra detta så att det passar dina behov.|


Välj åtgärden **Skapa demonstrationsdata** när du är klar. Det tar några minuter att lägga till data i den underliggande databasen, men sedan är det dags att köra de olika scenarierna.  

## <a name="scenarios"></a>Scenarierna

Demonstrationsdata för Contoso Coffee stöder för närvarande följande servicescenarier för test och utbildning:

1. Skapa serviceorder för ad hoc-reparationsbegäran, placera och ta emot låneartiklar, registrera tid och fakturera kunder med [genomgång av serviceorder för serviceartiklar](service-basic-flow-order.md)
2. Skapa servicekontrakt, generera serviceorder, fakturera kontraktsavgifter och fördela resurser med [genomgång av servicekontrakt för serviceartiklar](service-contract-flow.md)

Läs stegen för respektive scenario i den relevanta artikeln.  

> [!IMPORTANT]
> Servicegenomgångar kräver att användarupplevelsen är inställd på **Premium** på sidan **Företagsinformation**.


## <a name="see-also"></a>Se även

[Tjänst](../../service-service.md)
