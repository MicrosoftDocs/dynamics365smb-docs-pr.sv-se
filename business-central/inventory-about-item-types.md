---
title: Förstå artikeltyper
description: 'Lär dig om vilka typer av föremål du kan hantera i inventeringen och hur typerna påverkar. Du kan justera lagervärderingen för en artikel som använder FIFO eller genomsnittliga värderingsprinciper, när artikelkostnader ändras av andra skäl än transaktioner.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-item-types"></a>Om artikeltyper

I fältet **Typ** på sidan **artikelkort** kan du ange vilken artikel som används för din verksamhet vilket påverkar i vilken grad du kan hantera varan i lager. I tabellen nedan beskrivs de tre typer av objekt som finns tillgängliga.

|Alternativ|Vanligt syfte|
|------|-----------|
|Lager|Fysiska saker, till exempel cyklar, telefoner och skriv bord som du vill kunna använda som alla lagerprocesser. Lagerartiklar kan även innefatta icke-fysiska artiklar, till exempel programvarulicenser och prenumerationer, om artiklarna har identifieringsnummer, till exempel serienummer. Du kan spåra artikelvärden och lagerdispositionen fullständigt i lagret.|
|Inte i lager|Artiklar som inte finns i lager är vanligtvis fysiska, som t.ex. bultar och pennor, som en rörelse förbrukar men som inte spårar i lagret. Eftersom de exempelvis är lågkostnadsartiklar och endast används internt.|
|Tjänst|En arbetstidsenhet, såsom ett konsulttimme, för begränsat affärsstöd.|

> [!NOTE]
> Typerna **Tjänst** och **Inte i lager** låter dig inte spåra lagerkvantitet och värde. Endast markerade artikeltransaktionstyper och funktioner stöd. Följande tabell listar de funktioner som de tre objekttyperna stöder.

|Artikeltyp|FÖRS|Inköp|Projektförbrukning|Serviceförbrukning|Monteringsförbrukning|Produktion Förbrukning|Monteringsutflöde|Produktionsutflöde|Platsöverföring|Fysisk räkning|Omvärdering av lager|Lagerkostnad|Artikelspårning|Reservation|Lagerstyrning|Planering|Orderplanering|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Lagersaldo|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Inte i lager|Ja|Ja|Ja|Ja|Ja|Ja|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Ja|
|Tjänst|Ja|Ja|Ja|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Nr|Ja|

## <a name="costing-methods-for-types-of-items"></a>Värderingsprinciper för olika typer av artiklar

När du publicerar lagertransaktioner registreras kvantitets- och värdeförändringarna i varulagret i artikeltransaktioner och värdetransaktioner.

Du registrerar kostnaden för lagerartiklar i fältet **Kostnadsbelopp (aktuell)** på sidan **Värdetransaktioner**. När du stämmer av transaktionen i redovisningen visas kostnaden i fältet **Kostnad bokförd i redovisningen**. Mer information om lagerkostnad finns i [Designdetaljer: Lagerkostnad](design-details-inventory-costing.md).

För artiklar som inte finns i lager och tjänstartiklar registreras kostnaden i fältet **Kostnadsbelopp (ej-lagerförd)** på sidan **Värdetransaktioner**. För icke-lager och tjänstartiklar anges kostnaden på försäljnings-, monterings- och produktionsdokument och journaler. Ange standardkostnaden i **Styckkostnad** på sidorna **Artikelkortet** och **Lagerställeenhet**. Kostnader för dessa typer av artiklar stäms inte av mot redovisningen.

## <a name="catalog-and-service-items"></a>Katalog- och tjänstartiklar

Du kan ställa in artiklar som du erbjuder dina kunder men som du inte vill hantera tills du börjar sälja dem som katalogartiklar. Även om katalogartiklar liknar vanliga artiklar av typen **Ej lagerförd** i det här avseendet, ska du inte blanda ihop de två eftersom det finns skillnader. Om du vill lära dig mer går du till [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).

Kundartiklar som du utför service på, till exempel en skrivare kallas för tjänstartiklar. Tjänstartiklar har inget att göra med vanliga eller katalogartiklar. Men servicekomponenter kan dock vara vanliga artiklar. Mer information finns i [Ställa in tjänstartiklar och tjänstartikelkomponenter](service-how-setup-service-items.md).

## <a name="see-also"></a>Se även

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Ställa in lager](inventory-setup-inventory.md)  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
