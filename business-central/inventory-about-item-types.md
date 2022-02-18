---
title: Förstå artikeltyper
description: Du kan justera lagervärderingen för en artikel som använder FIFO eller genomsnittliga värderingsprinciper, när artikelkostnader ändras av andra skäl än transaktioner.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 9297, 5845, 30,
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: acb6ab4436f32760d905701348a242a4374b6b2d
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059628"
---
# <a name="about-item-types"></a>Om artikeltyper
I fältet **Typ** på sidan **artikelkort** kan du ange vilken artikel som används för din verksamhet vilket påverkar i vilken grad du kan hantera varan i lager. I tabellen nedan beskrivs de tre typer av objekt som finns tillgängliga.

|Alternativ|Vanligt syfte|
|------|-----------|
|Lager|Fysiska saker, till exempel cyklar, telefoner och skriv bord som du vill kunna använda som alla lagerprocesser. Det kan även innefatta icke-fysiska artiklar, till exempel programvarulicenser och prenumerationer, om artiklarna har identifieringsnummer, till exempel serienummer. Du kan spåra artikelvärden och lagerdispositionen fullständigt i lagret.|
|Inte i lager|Artiklar som inte finns i lager är vanligtvis fysiska, som t.ex. bultar och pennor, som en rörelse förbrukar men inte vill kunna spåra i lagret. Eftersom de exempelvis är lågkostnadsartiklar och endast används internt.|
|Tjänst|En arbetstidsenhet, såsom ett konsulttimme, för begränsat affärsstöd.|

> [!NOTE]
> Typerna **Tjänst** och **Inte i lager** omfattar inte stöd av lagerkvantitet och värde. Endast markerade artikeltransaktionstyper och funktioner stöd.

Följande tabell listar de funktioner som de tre objekttyperna stöder.

|Artikeltyp|FÖRS|Inköp|Projektförbrukning |Serviceförbrukning|Monteringsförbrukning|Produktion Förbrukning|Monteringsutflöde|Produktionsutflöde|Platsöverföring|Fysisk räkning|Omvärdering av lager|Lagerkostnad|Artikelspårning|Reservation|Lagerstyrning|Planering|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Lagersaldo|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Inte i lager|Ja|Ja|Ja|Ja|Ja|Ja|Nr|Nr|Nr|Nr|Nr|Nr|Nej|Nej|Nej|Nej|
|Tjänst|Ja|Ja|Ja|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|Nej|

## <a name="costing-methods-for-types-of-items"></a>Värderingsprinciper för olika typer av artiklar
När du publicerar lagertransaktioner registreras kvantitets- och värdeförändringarna i varulagret i artikeltransaktioner och värdetransaktioner. 

För lager artiklar anges kostnaden i fältet **Kost.belopp (aktuellt)** på sidan **Värdetransaktioner** och när den stäms av mot redovisningen kommer kostnaden att visas i fältet **Kostnad bokförd i redov.**. Mer information finns i [Designdetaljer: Lagerkostnad](design-details-inventory-costing.md)

För artiklar som inte finns i lager och tjänstartiklar registreras kostnaden i fältet **Kostnadsbelopp (ej-lagerförd)** på sidan **Värdetransaktioner**. För icke-lager och tjänstartiklar anges kostnaden på försäljnings-, monterings- och produktionsdokument och journaler. Standardkostnaden kan anges i **Styckkostnad** på sidorna **Artikelkortet** och **Lagerställeenhet**. Kostnader för dessa typer av artiklar stäms inte av mot redovisningen. 

## <a name="catalog-and-service-items"></a>Katalog- och tjänstartiklar
Artiklar som du erbjuder dina kunder men som du inte vill hantera i ditt system, tills du börjar sälja dem kan ställas in som katalogartiklar. Katalogartiklar ska inte förväxlas med vanliga artiklar av typen Inte i lager. Mer information finns i [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).

Kundernas artiklar som du utför service på, till exempel en skrivare kallas för tjänstartiklar. Tjänstartiklar har inget att göra med vanliga eller katalogartiklar. Men servicekomponenter kan dock vara vanliga artiklar. Mer information finns i [Ställa in tjänstartiklar och tjänstartikelkomponenter](service-how-setup-service-items.md).

## <a name="see-also"></a>Se även
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Ställa in lager](inventory-setup-inventory.md)  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]