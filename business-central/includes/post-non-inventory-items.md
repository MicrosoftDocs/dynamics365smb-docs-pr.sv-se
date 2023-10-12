---
author: brentholtorf
ms.topic: include
ms.date: 09/21/2023
ms.author: bholtorf
---

Personalen på distributionslager kan leverera och ta emot artiklar som inte finns i lager tillsammans med fysiska varor på försäljnings- och inköpsorder. Artiklar som inte finns i lagret är immateriella, t.ex. försäkringskostnader eller extra kostnader.

Försäljnings- och inköpsorder har ofta olika typer av saker på sina rader. Order kan till exempel innehålla redovisningsartiklar, konton och anläggningstillgångar. Om du använder distributionslagerdokument för att hantera fysiska artiklar kan du även bokföra vissa typer av artiklar som inte finns i lager. Följande är exempel på distributionslagerdokument:

* Lager, artikelinförsel
* Inleveranser på dist.lager
* Lagerplockningar
* Utleveranser från distributionslager

Om du vill göra det möjligt för distributionslagerarbetare att leverera och ta emot artiklar som inte finns i lagret fyller du i fältet **Automatisk bokföring av icke-lagerföring via lagerplats.** på sidorna **Försäljningsinställningar** och **Inköpsinställningar**. Fältet erbjuder följande alternativ:

|Alternativ  |Description  |
|---------|---------|
|Inga     |Leverera samt ta heller inte emot artiklar som inte finns i lager.         |
|Kopplade/tilldelade     | Bokför artikelomkostnader och andra rader för artiklar som inte finns i lager och som har tilldelats eller kopplats till fysiska artiklar. Om du vill koppla rader för icke-lager artiklar till fysiska artiklar använder du åtgärden **Koppla till lagerrad**.        |
|Alla     | Bokför alla rader för produkter som inte finns i lager i källdokumentet så snart minst en artikel har bokförts av distributionslagerdokumentet.        |

> [!NOTE]
> Alternativet **Fullständig** i fältet **Leveransavisering** på försäljningsordern har högre prioritet än valet i **Automatisk bokföring av icke-invt. via dist.lager.** fältet på sidan **Försäljningsinställningar**.