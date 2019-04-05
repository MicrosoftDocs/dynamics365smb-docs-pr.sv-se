---
title: Förstå artikeltyper | Microsoft Docs
description: Du kan justera lagervärderingen för en artikel som använder FIFO eller genomsnittliga värderingsprinciper, till exempel när artikelkostnader ändras av andra skäl än transaktioner.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/18/2018
ms.author: sgroespe
ms.openlocfilehash: 2240840e977bcd1186c74972ce0457deb03058a0
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "808272"
---
# <a name="about-item-types"></a>Om artikeltyper
I fältet **Typ** på sidan **artikelkort** kan du ange vilken artikel som används för din verksamhet och hur den hanteras i systemet. Det finns tre alternativ:

|Alternativ|Vanligt syfte|
|------|-----------|
|Lagersaldo|En fysisk enhet, till exempel en cykel för fullständig affärsstöd.|
|Inte i lager|T.e.x. en fysisk enhet, såsom en bult, för begränsad affärsstöd eftersom artikeln bara används internt i och har en låg kostnad.|
|Service|En arbetstidsenhet, såsom ett konsulttimme, för begränsat affärsstöd.|

Typen **Lager** omfattar fullständig spårning av lagerkvantitet och värde. Därför stöds alla artikeltransaktionstyper och artiklar av typen Lager kan användas med alla funktioner för artikelhantering.

Typerna **Service** och **Inte i lager** omfattar inte spårning av lagerkvantitet och värde. Därför stöds endast markerade artikeltransaktionstyper och funktioner.

De tre artikeltyperna stödjer följande funktioner.

|Artikeltyp|FÖRS|Inköp|Projektförbrukning |Serviceförbrukning|Monteringsförbrukning|Produktion Förbrukning|Monteringsutflöde|Produktionsutflöde|Platsöverföring|Fysisk räkning|Omvärdering av lager|Lagerkostnad|Artikelspårning|Reservation|Lagerstyrning|Planering|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Lagersaldo|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Inte i lager|Ja|Ja|Ja|Ja|Ja|Ja|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|
|Service|Ja|Ja|Ja|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|

> [!NOTE]
> Artiklar som du erbjuder dina kunder men som du inte vill hantera i ditt system, tills du börjar sälja dem kan ställas in som katalogartiklar. Katalogartiklar ska inte förväxlas med vanliga artiklar av typen Inte i lager. Mer information finns i [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).

> [!NOTE]
> Kundernas artiklar som du utför service på, till exempel en skrivare kallas för serviceartiklar. Serviceartiklar har inget att göra med vanliga eller katalogartiklar. Men servicekomponenter kan dock vara vanliga artiklar. Mer information finns i [Ställa in tjänsteartiklar och tjänsteartikelkomponenter](service-how-setup-service-items.md).

## <a name="see-also"></a>Se även
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Ställa in lager](inventory-setup-inventory.md)  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
