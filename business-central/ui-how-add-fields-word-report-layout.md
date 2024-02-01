---
title: Så här lägger du till fält i en Word-rapportlayout
description: Detta ämne beskriver hur du lägger till fält i en rapportdatauppsättning i en befintlig Word-rapportlayout för en rapport.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 11/25/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="work-with-word-layouts"></a>Arbeta med Word-layouter

En layout för en Word-rapport bestämmer innehållet i och formatet på en rapport när den förhandsgranskas och skrivs ut från Business Central. Du skapar och ändrar dessa layouter med Microsoft Word.

[![Exempel på ett rapportlayoutdokument för Business Central.](media/word-layout.png)](media/word-layout.png#lightbox) 

När du ändrar en layout i en Word-rapport anger du de fält i rapport datauppsättningen som ska tas med i rapporten och hur fälten är ordnade. Du definierar också rapportens allmänna format, till exempel teckensnitt, teckenstorlek, marginaler och bakgrundsbilder. Du ska normalt ordna innehållet i rapporten genom att lägga till tabeller i layouten.

Du kan göra allmänna formaterings- och layoutändringar, t.ex ändra textteckensnittet, lägga till och ändra en tabell eller ta bort ett datafält, genom att använda de grundläggande redigeringsfunktionerna i Word.

Om du designar en Word-rapportlayout från noll eller lägger till nya datafält, starta då genom att lägga till en tabell som innehåller rader och kolumner som kommer att innehålla datafälten.

> [!TIP]  
> Visa tabellstödlinjerna så att du kan se gränserna mellan tabellceller. Kom ihåg att dölja stödlinjerna när du har redigerat klart. För att visa eller dölja tabellstödlinjer, välj tabellen och välj under **Visa stödlinjer** på fliken **Tabell** under **Layout**.

## <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Inbäddade teckensnitt i Word-ayouter för konsistens

För att säkerställa att rapporterna alltid visas och skrivs ut med planerade teckensnitt, oavsett om en användare öppnar eller skriver ut rapporter, kan du bädda in teckensnitt i Word-dokumentet. Men tänk på att inbäddade teckensnitt kan öka storleken på de Word-filerna väsentligt. Mer information om inbäddade teckensnitt i Word finns i [inbäddade teckensnitt i Word, PowerPoint eller Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

## <a name="adding-data-fields"></a>Lägga till datafält

En rapportdatauppsättning kan bestå av fält som visar rubriker, data och bilder. I det här avsnittet beskrivs proceduren för att lägga fält i en rapportdatauppsättning i en befintlig Word-rapportlayout för en rapport. Du lägger till fält genom att använda den anpassade Word XML-delen för rapporten och att lägga till innehållskontroller som mappar till fälten på rapportdatauppsättningen. Att lägga till fält kräver att du har viss kunskap om rapportens datauppsättning så att du kan identifiera fälten som du vill lägga till i layouten.  
  
> [!NOTE]  
>  Du kan inte ändra inbyggda rapportlayouter<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

### <a name="to-open-the-custom-xml-part-for-the-report-in-word"></a><a name="OpenXMLPart"></a>Så här öppnar du den anpassade XML-delen för rapporten i Word
  
1. Öppna sedan Word-rapportlayoutdokumentet i Word, om inte redan har öppnats.  
  
     Mer information finns i [Skapa och ändra en anpassad rapportlayout](ui-how-create-custom-report-layout.md).  
  
2. Visa fliken **Utvecklare** på menyfliken i Microsoft Word.  
  
     Som standard visas fliken **Utvecklare** inte på menyfliken. Mer information finns i [Visa fliken Utvecklare på menyfliken](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon).  
  
3. På fliken **Utvecklare** väljer du **XML-mappningsruta**.  
  
4. I rutan **XML-mappning**, i listrutan **Anpassad XML-del**, väljer du den anpassade XML-delen för [!INCLUDE[prod_short](includes/prod_short.md)]-rapporten, som vanligtvis är sist i listan. Namnet på den anpassade XML-delen har följande format:  
  
     `urn:microsoft-dynamics-nav/reports/<report_name>/<ID>`  

     `<report_name>` är det namn som har tilldelats rapporten 

     `<ID>` är rapportens ID-nummer.  
  
     När du har valt den anpassade XML-delen visar XML-mappningsrutan de rubriker och fältkontroller som är tillgängliga för rapporten.  
  
### <a name="to-add-a-label-or-data-field"></a>Så här lägger du till en rubrik eller ett datafält
  
1. Placera markören i det dokument som du vill lägga till kontrollen i.  
  
2. I rutan **XML-mappning** högerklickar du på kontrollen som du vill lägga till, väljer **Infoga innehållskontroll** och väljer sedan **Vanlig text**.  
  
    > [!NOTE]  
    >  Du kan inte lägga till ett fält genom att manuellt skriva datauppsättningsfältets namn i innehållskontrollen. Du måste använda fönstret **XML-mappning** för att mappa fälten.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a>Så här lägger du till upprepande rader med datafält för att skapa en lista
  
1. I en tabell lägger du till en tabellrad som innehåller en kolumn för varje fält som du vill upprepa.  
  
   Den här raden fungerar som en platshållare för de upprepande fälten.  
  
2. Markera hela raden.  
  
3. I rutan **XML-mappning** högerklickar du på kontrollen som motsvarar rapportdataobjektet som innehåller fälten som du vill upprepa, välj **Infoga innehållskontroll** och välj **Upprepande**.  
  
4. Lägg till de upprepande fälten på raden enligt följande:  
  
    1. Placera pekaren i en kolumn.  
  
    2. I rutan **XML-mappning** högerklickar du på kontrollen som du vill lägga till, väljer **Infoga innehållskontroll** och väljer sedan **Vanlig text**.  
  
    3. Upprepa steg a och b för varje fält.  
  
## <a name="adding-image-fields"></a>Lägga till bildfält

En rapportdatauppsättning kan omfatta ett fält som innehåller en bild, t. ex. ett företagslogotyp eller en bild av en artikel. Om du vill lägga till en bild från rapportdatauppsättningen infogar du en **Bild**-innehållskontroll.  
  
Bilder justeras i det övre vänstra hörnet av innehållskontrollen och storleksändras automatiskt i förhållande för att passa gränsen för innehållskontrollen.  
  
> [!IMPORTANT]  
> Du kan bara lägga till bilder som har ett format som stöds av Word, till exempel .bmp-, .jpeg- och .png-filtyper. Om du lägger till en bild som har ett format som inte stöds i Word visas ett felmeddelande när du kör rapporten från [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.  
  
### <a name="to-add-an-image"></a>Så här lägger du till en bild
  
1. Placera pekaren i det dokument som du vill lägga till kontrollen i.  
  
2. I rutan **XML-mappning** högerklickar du på kontrollen som du vill lägga till, väljer **Infoga innehållskontroll** och väljer sedan **Bild**.  
  
3. För att öka eller minska bildstorleken drar du ett storlekshandtag bort från eller mot mitten av innehållskontrollen.  

## <a name="removing-label-and-data-fields"></a><a name="RemoveField"></a>Ta bort rubrik- och datafält

Rubrik- och datafält för en rapport finns i innehållskontroller i Word. Efterföljande diagram illustrerar en innehållskontroll när den har valts i Word-dokumentet.  

![Innehållskontroll för fält i Word-rapportlayouter.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

Namnet på rubriken eller datafältet visas i innehållskontrollen. I exemplet är fältnamnet CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>Så här tar du bort en rubrik eller ett datafält

1. Högerklicka på fältet som du vill ta bort och välj **Ta bort innehållskontroll**.  

     Innehållskontrollen tas bort, men fältnamnet förblir som text.  

2. Ta bort den återstående texten efter behov.

## <a name="custom-xml-part-overview"></a>Översikt över anpassad XML-del

Word-rapportlayouter bygger på *anpassade XML-delar*. En anpassad XML för en rapport består av element som motsvarar dataobjekten, kolumner och rubriker som ingår i rapportens datauppsättning. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Den anpassade XML-delen används för att mappa data till en rapport när rapporten körs.

### <a name="xml-structure-of-custom-xml-part"></a>XML-struktur för anpassad XML-del

Följande tabell innehåller en förenklad översikt över XML-dokument av en anpassad XML-del.  
  
|XML-element|Description|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Rubrik|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|XML-namnområdespecifikation. `<reportname>` är det namn som har tilldelats rapporten. `<id>` är det ID som har tilldelats rapporten.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Innehåller alla rubriker för rapporten.<!--OnPren The element includes labels that are related to columns that have the IncludeCaption Property.--><br />-   Etikettelement som är relaterade till kolumner har formatet `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />- Etikett element ha formatet `<LabelName>LabelName</LabelName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Etiketter anges i alfabetisk ordning.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Dataobjekt och kolumner på högsta nivå. Kolumner anges i alfabetisk ordning.<!--OnPrem <br /><br /> The element names and values are determined by the Name Property of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Dataobjekt och kolumner som är inbäddade i dataobjektet på högsta nivå. Kolumner anges i alfabetisk ordning under respektive dataobjekt.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Bokslutselement.|  
  
### <a name="custom-xml-part-in-word"></a>Anpassad XML-del i Word

 I Word öppnar du den anpassade XML-delen i rutan **XML-mappning** och använder sedan rutan för att mappa element till innehållskontroller i Word-dokumentet. Rutan **XML-mappning** är tillgänglig från fliken **Utvecklare** (mer information finns i [Visa fliken Utvecklare på menyfliken](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon)).  
  
 Elementen i rutan **XML-mappning** visas i en struktur som liknar XML-källan. Rubrikfält grupperas under ett gemensamt **Rubriker**-element, och dataobjekt och kolumner ordnas i en hierarkisk struktur som motsvarar XML-källan, med kolumner som anges i alfabetisk ordning. Element identifieras efter sitt kolumnnamn enligt definierat i rapportens datauppsättning i AL-kod. Mer information finns i [Definiera en datauppsättning för rapport](/dynamics365/business-central/dev-itpro/developer/devenv-report-dataset).  
  
 Efterföljande diagram visar den enkla anpassade XML-del från föregående avsnitt i panelen **XML-mappning** i ett Word-dokument.  
  
 ![Klipp av fönstret XML-mappning i Word.](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
* Om du vill lägga till en rubrik eller ett fält i layouten infogar du en innehållskontroll som mappar till elementet i panelen **XML-mappning**.  
  
* Om du vill skapa upprepande rader med kolumner infogar du en **Upprepande**-innehållskontroll för element för det överordnade datartikelelementet och lägger sedan till innehållskontroller för skapa kolumnerna.  
  
* För rubriker är den faktiska texten som visas i den genererade rapporten värdet på egenskapen **Rubrik** för fältet i dataobjekttabellen (om rubriken är kopplad till kolumnen i rapportdatauppsättningen) eller en rubrik i rapportrubrikdesignern (om rubriken inte är kopplad till en kolumn i datauppsättningen).  
  
* Rubrikens språk som visas när du kör rapporten beror på språkinställningen för rapportobjektet.  
  
## <a name="see-also"></a>Se även

[Skapa och ändra en anpassad rapportlayout](ui-how-create-custom-report-layout.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
