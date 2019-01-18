---
title: "Så här lägger du till fält i en Word-rapportlayout | Microsoft Docs"
description: "Beskriver hur du lägger till fält i en rapportdatauppsättning i en befintlig Word-rapportlayout för en rapport."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/22/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 78c689aafe31cdec7be1e1740422f781352bbd3c
ms.openlocfilehash: 5293b5298a2084c8cd36ae4dcc60beda75f5014e
ms.contentlocale: sv-se
ms.lasthandoff: 10/25/2018

---
# <a name="add-fields-to-a-word-report-layout"></a>Lägga till fält i en Word-rapportlayout
En rapportdatauppsättning kan bestå av fält som visar rubriker, data och bilder. I det här avsnittet beskrivs proceduren för att lägga fält i en rapportdatauppsättning i en befintlig Word-rapportlayout för en rapport. Du lägger till fält genom att använda den anpassade Word XML-delen för rapporten och att lägga till innehållskontroller som mappar till fälten på rapportdatauppsättningen. Att lägga till fält kräver att du har viss kunskap om rapportens datauppsättning så att du kan identifiera fälten som du vill lägga till i layouten.  
  
> [!NOTE]  
>  Du kan inte ändra inbyggda rapportlayouter<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

##  <a name="OpenXMLPart"></a>Så här öppnar du den anpassade XML-delen för rapporten i Word  
  
1.  Öppna sedan Word-rapportlayoutdokumentet i Word, om inte redan har öppnats.  
  
     Mer information finns i [Skapa och ändra en anpassad rapportlayout](ui-how-create-custom-report-layout.md).  
  
2.  Visa fliken **Utvecklare** på menyfliken i Microsoft Word.  
  
     Som standard visas fliken **Utvecklare** inte på menyfliken. Mer information finns i [Visa fliken Utvecklare på menyfliken](https://go.microsoft.com/fwlink/?LinkID=389631).  
  
3.  På fliken **Utvecklare** väljer du **XML-mappningsruta**.  
  
4.  I rutan **XML-mappning** i listrutan **Anpassad XML-del** väljer du den anpassade XML-delen för ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->-rapport, som vanligtvis är sist i listan. Namnet på den anpassade XML-delen har följande format:  
  
     urn:microsoft-dynamics-nav/reports/*report_name*/*ID*  
  
     *report_name* är namnet som har tilldelats rapportobjektet i <!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.  
  
     *ID* är rapportens id-nummer.  
  
     När du har valt den anpassade XML-delen visar XML-mappningsrutan de rubriker och fältkontroller som är tillgängliga för rapporten.  
  
### <a name="to-add-a-label-or-data-field"></a>Så här lägger du till en rubrik eller ett datafält  
  
1.  Placera markören i det dokument som du vill lägga till kontrollen i.  
  
2.  I rutan **XML-mappning** högerklickar du på kontrollen som du vill lägga till, väljer **Infoga innehållskontroll** och väljer sedan **Vanlig text**.  
  
    > [!NOTE]  
    >  Du kan inte lägga till ett fält genom att manuellt skriva datauppsättningsfältets namn i innehållskontrollen. Du måste använda fönstret **XML-mappning** för att mappa fälten.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a>Så här lägger du till upprepande rader med datafält för att skapa en lista  
  
1.  I en tabell lägger du till en tabellrad som innehåller en kolumn för varje fält som du vill upprepa.  
  
     Den här raden fungerar som en platshållare för de upprepande fälten.  
  
2.  Markera hela raden.  
  
3.  I rutan **XML-mappning** högerklickar du på kontrollen som motsvarar rapportdataobjektet som innehåller fälten som du vill upprepa, välj **Infoga innehållskontroll** och välj **Upprepande**.  
  
4.  Lägg till de upprepande fälten på raden enligt följande:  
  
    1.  Placera pekaren i en kolumn.  
  
    2.  I rutan **XML-mappning** högerklickar du på kontrollen som du vill lägga till, väljer **Infoga innehållskontroll** och väljer sedan **Vanlig text**.  
  
    3.  Upprepa steg a och b för varje fält.  
  
## <a name="adding-image-fields"></a>Lägga till bildfält  
 En rapportdatauppsättning kan omfatta ett fält som innehåller en bild, t.ex. ett företagslogotyp eller en bild av en artikel. Om du vill lägga till en bild från rapportdatauppsättningen infogar du en **Bild**-innehållskontroll.  
  
 Bilder justeras i det övre vänstra hörnet av innehållskontrollen och storleksändras automatiskt i förhållande för att passa gränsen för innehållskontrollen.  
  
> [!IMPORTANT]  
>  Du kan bara lägga till bilder som har ett format som stöds av Word, till exempel .bmp-, .jpeg- och .png-filtyper. Om du lägger till en bild som har ett format som inte stöds i Word, kommer du att få ett fel när du kör rapporten från ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->-klienten.  
  
#### <a name="to-add-an-image"></a>Så här lägger du till en bild  
  
1.  Placera pekaren i det dokument som du vill lägga till kontrollen i.  
  
2.  I rutan **XML-mappning** högerklickar du på kontrollen som du vill lägga till, väljer **Infoga innehållskontroll** och väljer sedan **Bild**.  
  
3.  För att öka eller minska bildstorleken drar du ett storlekshandtag bort från eller mot mitten av innehållskontrollen.  

## <a name="custom-xml-part-overview"></a>Översikt över anpassad XML-del
Word-rapportlayouter bygger på *anpassade XML-delar*. En anpassad XML för en rapport består av element som motsvarar dataobjekten, kolumner och rubriker som ingår i rapportens datauppsättning. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Den anpassade XML-delen används för att mappa data till en rapport när rapporten körs.

  
### <a name="xml-structure-of-custom-xml-part"></a>XML-struktur för anpassad XML-del  
Följande tabell innehåller en förenklad översikt över XML-dokument av en anpassad XML-del.  
  
|XML-element|Description|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Rubrik|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|XML-namnområdespecifikation. `<reportname>` är det namn som har tilldelats rapporten. `<id>` är det ID som har tilldelats rapporten.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Innehåller alla rubriker för rapporten.<!--OnPren The element includes labels that are related to columns that have the [IncludeCaption Property](../FullExperience/Name%20Property-duplicate.md).--><br />-  Etikettelement som är relaterade till kolumner har formatet `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />-  Etikett element ha formatet `<LabelName>LabelName</LabelName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-  Rubriker anges i alfabetisk ordning.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Dataobjekt och kolumner på högsta nivå. Kolumner anges i alfabetisk ordning.<!--OnPrem <br /><br /> The element names and values are determined by the [Name Property-duplicate](../FullExperience/Name%20Property-duplicate.md) of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Dataobjekt och kolumner som är inbäddade i dataobjektet på högsta nivå. Kolumner anges i alfabetisk ordning under respektive dataobjekt.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Bokslutselement.|  
  
### <a name="custom-xml-part-in-word"></a>Anpassad XML-del i Word  
 I Word öppnar du den anpassade XML-delen i rutan **XML-mappning** och använder sedan rutan för att mappa element till innehållskontroller i Word-dokumentet. Rutan **XML-mappning** är tillgänglig från fliken **Utvecklare** (mer information finns i [Visa fliken Utvecklare på menyfliken](https://go.microsoft.com/fwlink/?LinkID=389631)).  
  
 Elementen i rutan **XML-mappning** visas i en struktur som liknar XML-källan. Rubrikfält grupperas under ett gemensamt **Rubriker**-element, och dataobjekt och kolumner ordnas i en hierarkisk struktur som motsvarar XML-källan, med kolumner som anges i alfabetisk ordning. Element identifieras efter deras namn som har definierats av egenskapen Namn i datauppsättnings-designern för rapporten i ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.  
  
 Efterföljande diagram visar den enkla anpassade XML-del från föregående avsnitt i panelen **XML-mappning** i ett Word-dokument.  
  
 ![Bild av fönstret XML-mappning i word](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
-   Om du vill lägga till en rubrik eller ett fält i layouten infogar du en innehållskontroll som mappar till elementet i panelen **XML-mappning**.  
  
-   Om du vill skapa upprepande rader med kolumner infogar du en **Upprepande**-innehållskontroll för element för det överordnade datartikelelementet och lägger sedan till innehållskontroller för skapa kolumnerna.  
  
-   För rubriker är den faktiska texten som visas i den genererade rapporten värdet på egenskapen **Rubrik** för fältet i dataobjekttabellen (om rubriken är kopplad till kolumnen i rapportdatauppsättningen) eller en rubrik i rapportrubrikdesignern (om rubriken inte är kopplad till en kolumn i datauppsättningen).  
  
-   Rubrikens språk som visas när du kör rapporten beror på språkinställningen för rapportobjektet. <!--OnPrem For more information, see [Multiple Document Languages](../FullExperience/Viewing%20the%20Application%20in%20Different%20Languages.md).-->  
  
## <a name="see-also"></a>Se även  
 [Skapa och ändra en anpassad rapportlayout](ui-how-create-custom-report-layout.md)   

