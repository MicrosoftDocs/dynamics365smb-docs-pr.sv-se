---
title: Förstå artikeltyper | Microsoft Docs
description: Du kan justera lagervärderingen för en artikel som använder FIFO eller genomsnittliga värderingsprinciper, till exempel när artikelkostnader ändras av andra skäl än transaktioner.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbe603de91c78cf64b2e181136ea6214aa43c5c8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786129"
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
|Inte i lager|Ja|Ja|Ja|Ja|Ja|Ja|Nr|Nr|Nr|Nr|Nr|Nr|Nej|Nej|Nej|Nej|
|Service|Ja|Ja|Ja|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|

## <a name="costing-methods-for-types-of-items"></a>Värderingsprinciper för olika typer av artiklar
När du publicerar lagertransaktioner registreras kvantitets- och värdeförändringarna i varulagret i artikeltransaktioner och värdetransaktioner. 

För lager artiklar anges kostnaden i fältet **Kost.belopp (aktuellt)** på sidan **Värdetransaktioner** och när den stäms av mot redovisningen kommer kostnaden att visas i fältet **Kostnad bokförd i redov.**. Mer information finns i [Designdetaljer: Lagerkostnad](design-details-inventory-costing.md)

För artiklar som inte finns i lager och serviceartiklar registreras kostnaden i fältet **Kostnadsbelopp (ej-lagerförd)** på sidan **Värdetransaktioner**. För icke-lager och serviceartiklar anges kostnaden på försäljnings-, monterings- och produktionsdokument och journaler. Standardkostnaden kan anges i **Styckkostnad** på sidorna **Artikelkortet** och **Lagerställeenhet**. Kostnader för dessa typer av artiklar stäms inte av mot redovisningen. 

## <a name="catalog-and-service-items"></a>Katalog- och serviceartiklar
Artiklar som du erbjuder dina kunder men som du inte vill hantera i ditt system, tills du börjar sälja dem kan ställas in som katalogartiklar. Katalogartiklar ska inte förväxlas med vanliga artiklar av typen Inte i lager. Mer information finns i [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).

Kundernas artiklar som du utför service på, till exempel en skrivare kallas för serviceartiklar. Serviceartiklar har inget att göra med vanliga eller katalogartiklar. Men servicekomponenter kan dock vara vanliga artiklar. Mer information finns i [Ställa in tjänsteartiklar och tjänsteartikelkomponenter](service-how-setup-service-items.md).

## <a name="see-also"></a>Se även
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Ställa in lager](inventory-setup-inventory.md)  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]