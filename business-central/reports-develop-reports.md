---
title: Utveckla rapportlayouter och datauppsättningar
description: Innehåller en översikt över Business Central-data.
author: kennieNP
ms.topic: conceptual
ms.devlang: al
ms.reviewer: bholtorf
ms.search.keywords: feature overview
ms.date: 02/03/2022
ms.author: kepontop
ms.service: dynamics-365-business-central
---

# Utveckla rapportlayouter och datauppsättningar för Business Central

En rapport i [!INCLUDE[prod_short](includes/prod_short.md)] består av ett rapportobjekt som definierar _datauppsättningen_ för rapporten (vilka data som är tillgängliga) och ett antal _rapportlayouter_ (hur data presenteras).  

## Utveckla rapportlayouter

Kanske vill du ändra befintliga rapportlayouter i [!INCLUDE[prod_short](includes/prod_short.md)]? Beroende på vilken teknik som används i layouten är det här något som du kanske kan göra själv (Excel- och kanske även Word-layouter), eller så kanske du behöver en utvecklare för att göra det (pixel-perfekta RDLC-layouter).

| Om du vill | Gå till |
|--|--|
| Lär dig mer om olika typer av layouter (Word, Excel och RDLC) | [Layouttyper (Word, Excel och RDLC)](ui-manage-report-layouts.md) |
| Lär dig hur du kan skapa en ny rapportlayout. | [Skapa en ny layout](ui-how-create-custom-report-layout.md) |
| Lär dig mer om vilka teckensnitt som installerats i [!INCLUDE[prod_short](includes/prod_short.md)] online så att de kan användas i rapportlayouter. | [Använda teckensnitt i layouter](ui-fonts.md) |
| Lär dig att arbeta med Word-layouter. | [Arbeta med Word-layouter](ui-how-add-fields-word-report-layout.md) |
| Lär dig hur du kan importera och exportera layoutfiler. | [Importera/exportera en layout](ui-how-import-and-export-report-layout.md) |
| Lär dig hur du uppdaterar en layoutdefinition i [!INCLUDE[prod_short](includes/prod_short.md)] med en ny layoutfil. | [Importera/exportera en layout](ui-how-import-and-export-report-layout.md) |
| Lär dig hur du ändrar standardlayout för en rapport. | [Ändra standardlayout](ui-how-change-layout-currently-used-report.md) |
<!-- | Lär dig att arbeta med Excel-layouter | [Arbeta med Excel-layouter](ui-how-add-fields-word-report-layout.md) | -->

## Utveckla rapportdatauppsättningar

 Om du vill ändra definitionerna av datauppsättningarna som definierar vilka data som är tillgängliga i rapporten, behöver du en utvecklare som känner till programmeringsspråket AL och verktygen för att utveckla rapportobjekt och rapporttillägg.

| Om du vill | Gå till |
|--|--|
| Lär dig att programmera rapporter i AL | [Rapportutvecklingsguide](/dynamics365/business-central/dev-itpro/developer/devenv-reports) |
| Lär dig hur du får rapporter att prestera | [Rapportprestandaguide](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-reports) |

## Se även

[Business Intelligence och rapporteringsöversikt](reports-use-reports.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]