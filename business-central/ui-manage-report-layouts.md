---
title: Hantera rapport- och dokumentlayouter
description: 'Använd rapportlayouter för att anpassa dokument, till exempel för att anpassa teckensnitt, logotyp eller inställningar för de PDF-filer som du skickar till kunder.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="report-and-document-layouts-overview" />Rapport- och dokumentlayouter, översikt

En rapportlayout kontrollerar rapportens format och innehåll, som vilka datafält i en rapportdatauppsättning som visas i rapporten och hur de ordnas, textstil, bilder och mycket annat. Från [!INCLUDE[prod_short](includes/prod_short.md)] kan du ändra vilken layout som används på en rapport, skapa en ny layout eller ändra befintliga layouter.

> [!NOTE]  
> I [!INCLUDE[prod_short](includes/prod_short.md)], omfattar termen "rapporter" även externa dokument som t. ex. fakturor och bekräftelser av inköpsorder som du skickar till kunder som PDF-filer.

Du kan också använda rapportlayouter för att lägga till innehåll i e-postmeddelanden. Med hjälp av rapportlayout kan du spara tid och säkerställa konsekvens genom att återanvända samma innehåll när du kommunicerar med kunderna. Om du vill använda anpassade rapportlayout med e-post måste du ange en filtyp för layouten. Du kan inte använda filtypen RDLC. Mer information finns i [ställa in återanvändbara e-posttexter och layouter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="introduction" />Introduktion

En rapportlayout ställer i synnerhet in följande:

* Rubrik- och datafälten som ska inkluderas från datauppsättningen för [!INCLUDE[prod_short](includes/prod_short.md)]-rapporten.
* Textformatet, till exempel teckensnittstyp, storlek och färg.
* Företagslogotypen och dess position.
* Allmänna sidinställningar, till exempel marginaler och bakgrundbilder.

En rapport kan ställas in med åtskilliga rapportlayouter, som du kan växla mellan. 

<!--You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed. For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).-->

Det finns två viktiga aspekter av rapportlayouten som påverkar hur du arbetar med dem: *layouttyp* och *layoutkälla*. Typen av layout visar vilken typ av fil som layouten baseras på. Layoutkällan anger layoutens ursprung.

## <a name="layout-types" />Layouttyper

Det finns fyra typer av rapportlayouter som du kan använda i rapporter: Word, RDLC, Excel och extern.

### <a name="word" />Word

Word-layout är baserad på Word-dokument (filtypen .docx). Word-layouter gör att du kan utforma rapportlayouter med hjälp av Microsoft Word. En Word-layout bestämmer rapportens innehåll – styr hur innehållselement organiseras och hur de ser ut. Ett Word-dokument med layout använder vanligtvis tabeller för att ordna innehållet, där cellerna kan innehålla datafält, text eller bilder.

[![Exempel på ett rapportlayoutdokument för Business Central.](media/word-layout-overview.png)](media/word-layout-overview.png#lightbox) 

<!--![Example of a word report layout document for Business Central.](media/nav_wordreportlayout_edit_in_word_example.png) -->

Mer information finns i [Arbeta med Word-layout](ui-how-add-fields-word-report-layout.md).

### <a name="excel" />Excel

Excel-layouter baseras på Microsoft Excel arbetsböcker (.xlsx-filtyper). De ger dig möjlighet att skapa rapporter med hjälp av välbekanta Excel-funktioner för sammanfattning, analys och presentation av data med verktyg med formler, PivotTables och PivotCharts, etc.

[![Visar ett exempel på en Excel-layout.](media/excel-layout-2.png)](media/excel-layout-2.png#lightbox)

Mer information finns i [Arbeta med Excel-layout](ui-excel-report-layouts.md).

### <a name="rdlc" />RDLC

RDLC-layouter baseras på layoutfiler för klientrapportdefinition (.rdl- eller .rdlc-filtyper). Dessa layouter skapas och ändras genom att använda SQL Server Report Builder eller Microsoft RDLC Report Designer. Utformningen av RDLC-layouter liknar Word-layouter, där layouten avgör vilka fält som ska visas och hur de är ordnade. Att utforma RDLC-layouter är mer avancerat än Word-layouter.

[![Visar ett exempel på en RDLC-layout.](media/rdlc-layout-overview.png)](media/rdlc-layout-overview.png#lightbox)

Mer information finns i [Arbeta med RDLC-layouter](ui-rdlc-report-layouts.md).

### <a name="external" />Externt

En extern layouttyp avser en avancerad typ som är speciellt utformad för specifika rapporter. Rapporterna och själva layouterna tillhandahålls vanligt vis av partner, inte av Microsoft. Layoutens faktiska filtyp kan variera beroende på providern.

Mer information finns i [utveckla en anpassad rapportåtergivning](/dynamics365/business-central/dev-itpro/developer/devenv-report-custom-render).

## <a name="layout-sources" />Layoutkällor

Förutom typen är layouterna ytterligare indelade i tre kategorier beroende på källa eller ursprung.

* Tilläggslayout

   Tilläggslayout är layouter som ingår i ett tillägg som har installerats på miljön. Dessa layouter är vanligtvis standardlayouter från Microsoft, till exempel i basprogrammet. Det kan också vara layouter som ingår i tillägg från andra programvaruleverantörer. Du kan känna igen tilläggslayouter på sidan **Rapportlayouter** eftersom tilläggsnamnet och utgivaren visas i kolumnen **Tillägg**.

* Användardefinierade layouter

   Den andra typen av layouter är slutanvändaren. En användare med rätt behörighet från insidan av Business Central kan lägga till nya layouter på olika sätt. Du kan till exempel utgå från en befintlig tilläggslayout eller en annan användardefinierad layout. I **rapportlayouter** har användardefinierad layout en tom kolumn för **tillägg**.

   Mer information finns i [Kom igång med att skapa rapportlayouter](ui-get-started-layouts.md).

* Anpassade layouter

  Anpassade layouter är också layouter som skapas av användare. Skillnaden är att dessa layouter skapas från äldre sida med **anpassad rapportlayout** och att de endast kan vara Word- och RDLC. Även om du fortfarande kan skapa anpassade layouter fasar de ut i sin fördel med användardefinierade layouter.

  Mer information finns i [(Äldre) Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).

För information som hjälper dig att avgöra vilken typ som passar bäst, se [bestämma vilken typ av layout du vill ha](ui-get-started-layouts.md#decide).

> [!IMPORTANT]
> Det är viktigt att komma ihåg att du inte kan ändra tilläggsritningar från Business Central-klienten. Du kan till exempel inte ändra layoutens namn, eller ladda upp och ersätta det med en annan version. Om du försöker visas ett felmeddelande. Du måste skapa en användardefinierad eller anpassad layout baserad på tilläggslayouten istället.

<!--
### <a name="built-in-and-custom-report-layouts" />Built-in and custom report layouts



[!INCLUDE[prod_short](includes/prod_short.md)] includes several built-in layouts. Built-in layouts are predefined layouts that are designed for specific reports. [!INCLUDE[prod_short](includes/prod_short.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both. You can’t modify a built-in report layout from [!INCLUDE[prod_short](includes/prod_short.md)] but you use them as a starting point for building your own custom report layouts.

Custom layouts are report layouts that you design to change the appearance of a report. You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout. Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed. For example, you can have different layouts for each [!INCLUDE[prod_short](includes/prod_short.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.


Deciding on whether to use a Word, Excel, or RDLC layout type will depend on how you want the generated report to look and your knowledge of tools for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* The general design concepts for Word and RDLC layouts are similar. However each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. This means that the same report might look different when using the Word report layout compared to the RDLC report layout.

* The process for setting up Word, Excel, and RDLC report layouts on reports is the same. The main difference is in the way you modify the layouts. Word and especially Excel layouts are typically easier to create and modify than RDLC report layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.

* Not all reports and document have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

For information about how to switch the layout currently used on a report, see [Set the Layout Used by a Report](ui-set-report-layout.md).

-->



## <a name="see-related-microsoft-training" />Se relaterad [Microsoft utbildning](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also" />Se även

[Uppdatera anpassade rapportlayouter](ui-update-report-layouts.md)  
[Skapa och ändra anpassade rapportlayouter](ui-how-create-custom-report-layout.md)  
[Så här importerar och exporterar du en anpassad rapport eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Definiera speciell dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Arbeta med rapporter, batch-jobb och XMLports](ui-work-report.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
