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
ms.openlocfilehash: 465954e6549ee7ffd0822438a0ad004686d5b424
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9604784"
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(Äldre) Skapa och ändra anpassade rapportlayouter

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Rapporter har som standard en inbyggd layout. Rapportlayouten kan antingen vara en RDLC-layout (report definition language client side), en Microsoft Word-layout eller både och. Och även om du inte kan ändra inbyggda layouter, så kan du skapa anpassade layouter. En rapport kan ha åtskilliga anpassade rapportlayouter.

> [!NOTE]  
> I [!INCLUDE[prod_short](includes/prod_short.md)] omfattar termen "rapport" även externa dokument som t.ex. försäljningsfakturor och orderbekräftelser som du skickar till kunder som PDF-filer.

Om du vill skapa en anpassad layout kan du antingen kopiera en befintlig anpassad layout eller lägga till en ny. Anpassade layouter baseras ofta på en inbyggd layout. När du lägger till en ny anpassad layout kan du välja att lägga till antingen en RDLC- eller en Word-rapportlayout eller både och. Den nya anpassade layouten baseras på den inbyggda layouten för rapporten, om en är tillgänglig. Om det inte finns någon inbyggd layout för rapporttypen skapas en ny, tom layout. Du måste ändra och utforma den här tomma layouten från början. Läs mer om RDLC- och Word-rapportlayouter, inbyggda och anpassade layouter och mer på [Hantera rapportlayouter](ui-manage-report-layouts.md).  

> [!TIP]
> Du kan använda ekonomiska rapporter för att få information om ekonomiska data som lagras i din kontoplan. Läs mer i [Förbereda Financial Reporting med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md).

När du har definierat egna rapportlayouter kan du välja dem på sidorna för kundkortet och leverantörskortet. Layouterna används sedan när du skapar dokument för kunden eller leverantören. Läs mer i [Definiera dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md).

Du kan också använda anpassade rapportlayouter för att lägga till innehåll i e-postmeddelanden. Med hjälp av rapportlayout kan du spara tid och säkerställa konsekvens genom att återanvända samma innehåll när du kommunicerar med kunderna. Om du vill använda anpassade rapportlayouter med e-post måste filtypen för layouten vara Word. Du kan inte använda filtypen RDLC. Läs mer i [Ställ in återanvändbara e-posttexter och layouter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).

## <a name="create-a-custom-layout"></a>Skapa en anpassad layout

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Val av rapportlayouter** och väljer sedan relaterad länk.

    På sidan **Val av rapportlayout** visas alla rapporter som är tillgängliga i företaget som har angetts i fältet **Företagsnamn** högst upp på sidan.
2. I fältet **Företagsnamn** väljer du företaget som du vill skapa rapportlayouten för.
3. Välj raden för den rapport som du vill skapa layouten för och välj sedan åtgärden **Anpassade layouter**.  

   På sidan **Anpassa rapportlayouter** visas alla anpassade layouter som är tillgängliga för den valda rapporten.
4. Om du vill skapa en kopia av en befintlig anpassad layout, markera den befintliga anpassade layouten i listan och välj sedan **Kopiera**.  

   Kopian av den anpassade layouten visas på sidan **Anpassa rapportlayouter** och har orden *Kopia av* i fältet **Beskrivning**.
5. Om du vill lägga till en ny anpassad layout som baseras på en inbyggd layout följer du dessa steg:  
   1. Välj åtgärden **Ny**. Sidan **Infoga inbyggd layout för en rapport** med fälten **ID** och **Namn** automatiskt ifyllda.
   2. Aktivera **Infoga Word-layout** för att lägga till en anpassad Word-rapportlayout ELLER aktivera **Infoga RDLC-layout** för att lägga till en anpassad RDLC-rapportlayout.
   4. Välj **OK**.  

    De nya anpassade layouterna visas på sidan **Anpassa rapportlayouter**. Om en ny layout baseras på en inbyggd layout visas orden **Kopia av en inbyggd layout** i fältet **Beskrivning**. Om det inte fanns en inbyggd layout för rapporten, får den nya layouten orden **Ny layout** i fältet **Beskrivning**, vilket innebär att den anpassade layouten är tom.
6. Som standard är fältet **Företagsnamn** tomt och den anpassade layouten är tillgänglig för rapporter av alla företag. För att du ska kunna göra den anpassade layouten tillgänglig för ett specifikt företag väljer du **Redigera** och ställer sedan in fältet **Företagsnamn** till företaget som du vill ha.

Den anpassade layouten har skapats och du kan ändra den om du vill.

> [!TIP]
> Du kan exportera rapportresultaten till en Microsoft Excel-fil för att visa hela datauppsättningen, inklusive alla kolumner, men utan layouten. Excel-filen kan hjälpa dig att verifiera att rapporten returnerar förväntade data eller diagnosproblem. Läs mer i [Analysera rapportdata med Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Ändra en anpassad layout

Om du vill ändra en anpassad rapportlayout måste du först exportera rapportlayouten som en fil till en plats på din dator eller nätverk. Öppna sedan det exporterade dokumentet och gör ändringarna. När du är klar med ändringarna importerar du rapportlayouten.

### <a name="modify-a-custom-layout"></a>Ändra en anpassad layout

1. Exportera en anpassad layout från sidan **Anpassade rapportlayouter**. Om sidan inte redan är öppen, sök efter och öppna **Val av rapportlayout**, välj rapporten med layouten som du vill ändra och välj sedan åtgärden **Anpassade layouter**.  
2. På sidan **Anpassade rapportlayouter** väljer du den layout som du vill ändra, väljer åtgärden **Exportera layout** och väljer sedan **Spara** eller **Spara som** för att spara rapportlayouten till en plats på datorn eller i nätverket.  
3. Öppna rapportlayoutdokumentet som du sparade och gör ändringar.

   Om du ändrar layouten i Word, öppna layoutdokumentet i Word. Lär dig mer om att redigera Word-rapporter på [Arbeta med Word-layouter](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   RDLC rapportlayouter är mer avancerade än Word rapportlayouter. Läs mer om att ändra en RDLC-rapportlayout i [Designa RDLC-rapportlayouter](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Glöm inte att spara ändringar när du är klar.

4. Gå tillbaka till sidan **Anpassade rapportlayouter**, välj rapportlayouten som du har exporterat och ändrat, och välj sedan åtgärden **Importera layout**.  

5. I dialogrutan **Importera** väljer du **Välj** för att hitta och välja den ändrade rapportlayouten och väljer sedan **Öppna**.

> [!IMPORTANT]
> Kom ihåg att importera det rapport dokument som du har ändrat. I annat fall kommer layouten för den nya rapporten inte att vara tillgänglig.

<!--
##  <a name="MakeChangesToLayout"></a> Create and modify custom report layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding fonts in Word layouts for consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. Learn more about embedding fonts in Word at [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing label and data fields in Word layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field you want to delete, then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is more advanced and requires some knowledge of the report dataset. Learn more about adding fields for data, labels, and images at [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Ändra aktuell rapportlayout](ui-how-change-layout-currently-used-report.md)  
[Så här importerar och exporterar du en anpassad rapport eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Arbeta med rapporter, batch-jobb och XMLports](ui-work-report.md)  
[Förbereda Financial Reporting med ekonomiska data och kontokategorier](bi-how-work-account-schedule.md)  
[Affärsstöd](bi.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
