---
title: Skapa och ändra anpassade layouter för rapporter och dokument
description: Lär dig hur du kan skapa anpassade layouter för att personligt anpassa utseendet på rapporten när den visas, skrivs ut eller sparas.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/06/2022
ms.author: edupont
ms.openlocfilehash: 1d9d61ad7a4e9b0b64fd11d8a2c1a29676a8ddb4
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531978"
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(Äldre) Skapa och ändra anpassade rapportlayouter

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Rapporter har som standard en inbyggd layout för rapporten. Layouten kan vara antingen en RDLC-rapportlayout Word-rapportlayout eller både och. Du kan inte ändra inbyggda layouter, men du kan också skapa anpassade layouter. En rapport kan ha åtskilliga anpassade rapportlayouter.

> [!NOTE]  
> I [!INCLUDE[prod_short](includes/prod_short.md)], omfattar termen "rapporter" även externa dokument som t. ex. fakturor och bekräftelser av inköpsorder som du skickar till kunder som PDF-filer.

Om du vill skapa en anpassad layout kan du antingen kopiera en befintlig anpassad layout eller lägga till en ny. Anpassade layouter baseras ofta på en inbyggd layout. När du lägger till en ny anpassad layout kan du välja att lägga till en RDLC-eller Word-rapportlayout eller både och. Den nya anpassade layouten baseras på den inbyggda layouten för rapporten, om en är tillgänglig. Om det inte finns någon fördefinierad layout för typen skapas en ny, tom layout. Du måste ändra och utforma den här tomma layouten från början. Mer information om RDLC- och Word-rapportlayouter, inbyggda och anpassade layouter och mer finns i [Hantera rapportlayouter](ui-manage-report-layouts.md).  

> [!TIP]
> Du kan använda kontouppställningar för att få information om ekonomiska data som lagras i din kontoplan. Mer information finns i [Förbereda ekonomiska rapporter med kontouppställningar och kontokategorier](bi-how-work-account-schedule.md).

När du har definierat egna rapport layouter kan du välja dem på sidorna för kundkortet och leverantörskortet. Layouterna kommer att användas när du skapar dokument för kunden eller leverantören. Mer information finns i [definiera dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md).

Du kan också använda anpassade rapportlayouter för att lägga till innehåll i e-postmeddelanden. Med hjälp av rapportlayout kan du spara tid och säkerställa konsekvens genom att återanvända samma innehåll när du kommunicerar med kunderna. Om du vill använda anpassade rapportlayout med e-post måste du ange en filtyp för layouten. Du kan inte använda filtypen RDLC. Mer information finns i [ställa in återanvändbara e-posttexter och layouter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="to-create-a-custom-layout"></a>Så här skapar du en anpassad layout

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Val av rapportlayouter** och väljer sedan relaterad länk.

    På sidan **Val av rapportlayout** visas alla rapporter som är tillgängliga i företaget som har angetts i fältet **Företagsnamn** högst upp på sidan.
2. Ange fältet **Företagsnamn** till företaget som du vill skapa rapportlayouten i.
3. Markera raden för rapporten som du skapa layouten för och välj sedan **Anpassa layouter**.  

   På sidan **Anpassa rapportlayouter** visas alla anpassade layouter som är tillgängliga för den valda rapporten.
4. Om du vill skapa en kopia av en befintlig anpassad layout, markera den befintliga anpassade layouten i listan och välj sedan **Kopiera**.  

   Kopian av den anpassade layouten visas på sidan **Anpassa rapportlayouter** och har orden *Kopia av* i fältet **Beskrivning**.
5. Om du vill lägga till en ny anpassad layout som baseras på en inbyggd layout gör du följande steg:  
   1. Välj åtgärden **Ny**. På sidan **Infoga inbyggd layout för en rapport** visas. Fälten **ID** och **Namn** fylls i automatiskt.
   2. Om du vill lägga till en anpassad Word-rapportlayouttyp markerar du kryssrutan **Infoga Word-layout**.
   3. Om du vill lägga till en anpassad RDLC-rapportlayouttyp markerar du kryssrutan **Infoga RDLC-layout**.
   4. Välj **OK**.  

    De nya anpassade layouterna visas på sidan **Anpassa rapportlayouter**. Om en ny layout baseras på en inbyggd layout får den orden **Kopia av en inbyggd layout** i fältet **Beskrivning**. Om det inte fanns en inbyggd layout för rapporten, får den nya layouten orden **Ny layout** i fältet **Beskrivning**, vilket anger att den anpassade layouten är tom.
6. Som standard är fältet **Företagsnamn** tomt, vilket betyder att den anpassade layouten är tillgänglig för rapporten i alla företag. För att du ska kunna göra den anpassade layouten tillgänglig väljer du **Redigera** och ställer sedan in fältet **Företagsnamn** till företaget som du vill ha.

Den anpassade layouten har skapats. Du kan nu ändra den anpassade layouten efter behov.

> [!TIP]
> Tja, du kan exportera rapportresultaten till en Excel-fil för att visa hela datauppsättningen, inklusive alla kolumner, men utan layouten. Excel-filen kan hjälpa dig att verifiera att rapporten returnerar förväntade data eller diagnosproblem. Mer information finns i [Analysera rapportdata med Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Ändra en anpassad layout

Om du vill ändra en rapportlayout måste du först exportera rapportlayouten som en fil till en plats på din dator eller nätverk. Öppna sedan det exporterade dokumentet och gör ändringarna. När du är klar med ändringarna importerar du rapportlayouten.

### <a name="to-modify-a-custom-layout"></a>Ändra en anpassad layout

1. Du kan exportera en anpassad layout från sidan **anpassade rapportlayouter**. Om sidan inte redan är öppen, sök efter och öppna **Val av rapportlayout**, välj rapporten med layouten som du vill ändra och välj sedan åtgärden **Anpassade layouter**.  
2. På sidan **anpassade rapportlayouter** väljer du den layout som du vill ändra, anger **exportera layout**, och välj **spara** eller **Spara som** för att spara rapportlayouten till en plats på datorn eller i nätverket.  
3. Öppna rapportlayoutdokumentet som du sparade och gör ändringar.

   Om du ändrar layouten i Word, öppna layoutdokumentet i Word. Mer redigeringsinformation finns i [Arbeta med Word-layout](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   RDLC rapportlayouter är mer avancerade än Word rapportlayouter. Mer information om att ändra en RDLC-rapportlayout finns i [Designa RDLC rapportlayout](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Glöm inte att spara ändringar när du är klar.

4. Gå tillbaka till sidan **anpassade rapportlayouter**, välj rapportlayouten som du har exporterats och ändrats, och välj sedan åtgärden **Importera layout**.  

5. I dialogrutan **Importera** väljer du **Välj** för att hitta och välja dokumentet och väljer sedan **Öppna**.

> [!IMPORTANT]
> Kom ihåg att importera det rapport dokument som du har ändrat. I annat fall kommer layouten för den nya rapporten inte att vara tillgänglig.

<!--
##  <a name="MakeChangesToLayout"></a> Create and Modify Custom Report Layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word, like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding Fonts in Word Layouts for Consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. For more information about embedding fonts in Word, see [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing Label and Data Fields in Word Layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field that you want to delete, and then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is a more advanced and requires some knowledge of the report dataset. For information about adding fields for data, labels, data, and images, see [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Ändra aktuell rapportlayout](ui-how-change-layout-currently-used-report.md)  
[Så här importerar och exporterar du en anpassad rapport eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Arbeta med rapporter, batch-jobb och XMLports](ui-work-report.md)  
[Förbereda Financial Reporting med kontouppställningar och kontokategorier](bi-how-work-account-schedule.md)  
[Affärsstöd](bi.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
