---
title: Arbeta med RDLC-layouter
description: Få en introduktion till RDLC-rapportlayout.
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 12/04/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# Arbeta med RDLC-layouter

RDLC-layouter baseras på layoutfiler för rapportdefinition (.rdl- eller .rdlc-filtyper). Design begreppen för RDLC layouter liknar andra typer av layouter. Layouten avgör vilka fält som ska visas och hur de är ordnade. Att utforma RDLC-layouter är mer avancerat än Word- och Excel-layouter.

[![Visar de olika elementen i en RDLC-layout.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## Verktyg som krävs

Om du vill ändra RDL-layouter kan du använda antingen Microsoft SQL Server Report Builder eller Microsoft Visual Studio med tillägget RDLC Report Designer.

- Report Builder är en fristående app som är installerad på din dator av dig eller en administratör. Med Business Central på plats installeras Report Builder automatiskt tillsammans med Business Central Server-installationen. Mer information om hur du installerar Report Builder finns i [installera Report Builder](/sql/reporting-services/install-windows/install-report-builder) i dokumentationen till SQL Server.

- RDLC Report Designer är ett tillägg för Visual Studio 2019 och senare. Du kan hämta och installera RDLC Report Designer från [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## Skapa och ändra RDLC-layouter

Att skapa och ändra RDLC-layouter är en avancerad uppgift som normalt görs av privilegierade användare eller utvecklare. De grundläggande begreppen är inte specifika för layouterna i Business Central-rapporter. Därför bör du läsa följande dokumentation:

- [Skapa layoutrapporten RDL](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

   I den här artikeln beskrivs hur du skapar en RDLC-rapportlayout med hjälp av AL-koden.

- [Rapporter, rapportdelar och rapportdefinitioner](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

   Detta länkar till SQL Server Reporting Services-dokumentationen för RDL/RDLC. Den här artikeln förklarar koncepten bakom RDL/RDLC och hur du använder Report Builder.

> [!NOTE]
> Report Builder kan tolka filtypen RDL, inte. rdlc. Layoutfiler som exporteras från Business Central är .rdlc-filtyper. Om du vill ändra de här layouterna i Report Builder byter du namn på filtypen till. RDL.

## Se även

[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Ange layout för en rapport](ui-set-report-layout.md)  
[Kom igång med att skapa rapportlayouter](ui-get-started-layouts.md)  
[Arbeta med rapporter och batch-jobb och XMLports](ui-work-report.md)  
[Affärsstöd](bi.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analysera rapportdata med Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
