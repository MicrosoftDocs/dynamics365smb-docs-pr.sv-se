---
title: Arbeta med RDLC-layouter
description: Få en introduktion till RDLC-rapportlayout.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/14/2022
ms.author: jswymer
---
# <a name="working-with-rdlc-layouts"></a>Arbeta med RDLC-layouter

RDLC-layouter baseras på layoutfiler för klientrapportdefinition (.rdl- eller .rdlc-filtyper). Design begreppen för RDLC layouter liknar andra typer av layouter. Layouten avgör vilka fält som ska visas och hur de är ordnade. Att utforma RDLC-layouter är mer avancerat än Word- och Excel-layouter.

[![Visar de olika elementen i en RDLC-layout.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## <a name="required-tools"></a>Verktyg som krävs

Om du vill ändra RDL-layouter kan du använda antingen Microsoft SQL Server Report Builder eller Microsoft RDLC Report Designer.

- Report Builder är en fristående app som är installerad på din dator av dig eller en administratör. Med Business Central på plats installeras Report Builder automatiskt tillsammans med Business Central Server-installationen. Mer information om hur du installerar Report Builder finns i [installera Report Builder](/sql/reporting-services/install-windows/install-report-builder) i dokumentationen till SQL Server.

- RDLC Report Designer är ett tillägg för Visual Studio 2017 och senare. Du kan hämta och installera RDLC Report Designer från [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## <a name="create-and-modify-rdlc-layouts"></a>Skapa och ändra RDLC-layouter

Att skapa och ändra RDLC-layouter är en avancerad uppgift som normalt görs av privilegierade användare eller utvecklare. De grundläggande begreppen är inte specifika för layouterna i Business Central-rapporter. Därför bör du läsa följande dokumentation:

- [Skapa layoutrapporten RDL](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

    I den här artikeln beskrivs hur du skapar en RDLC-rapportlayout med hjälp av AL-koden.

- [Rapporter, rapportdelar och rapportdefinitioner](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

 Länkar till SQL Server Reporting Services-dokumentationen för RDL/RDLC. I den här dokumentationen beskrivs begreppen  
Bakom RDL/RDLC och hur Report Builder används.

> [!NOTE]
> Report Builder kan tolka filtypen RDL, inte. rdlc. Layoutfiler som exporteras från Business Central är .rdlc-filtyper. Om du vill ändra de här layouterna i Report Builder byter du namn på filtypen till. RDL.

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Ange layout för en rapport](ui-set-report-layout.md)  
[Kom igång med att skapa rapportlayouter](ui-get-started-layouts.md)  
[Arbeta med rapporter och batch-jobb och XMLports](ui-work-report.md)  
[Affärsstöd](bi.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analysera rapportdata med Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
