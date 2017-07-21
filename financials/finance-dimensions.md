---
title: Arbeta med Dimensioner | Microsoft Docs
description: "Du kan använda dimensioner för att kategorisera poster, till exempel efter avdelning eller projekt, så att du kan spåra och analysera data."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/16/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b7b69b3419520c482cbe6a84494bbac7ef35bea1
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="working-with-dimensions"></a>Arbeta med dimensioner
Du kan använda dimensioner för att göra det enklare att analysera dokument såsom försäljningsorder. Dimensioner är attribut och värden som kategoriserar transaktioner så att du kan spåra och analysera dem. Dimensioner kan till exempel ange vilket projekt eller vilken avdelning en transaktion kom ifrån.  

T.ex. kan du använda dimensioner i stället för att skapa separata redovisningskonton för varje avdelning och projekt. Detta ger stora möjligheter för analys, utan att skapa en komplicerad kontoplan. Mer information finns i [Affärsstöd](bi.md).

Ett annat exempel är att ställa in en dimension kallad *Avdelning* och använda denna dimension när du bokför försäljningsdokument. Det gör att du kan använda business intelligence-verktyg för att visa vilken avdelning som sålt vilka artiklar.
Ju fler dimensioner du använder, desto mer detaljerade rapporter kan du baseras dina affärsbeslut på. En enda försäljningstransaktion kan till exempel innehålla olika dimensionsinformation som t.ex.:  

* Kontot som artikeln bokfördes till  
* Var artikeln såldes
* Vem som sålde den
* Vilken typ av kund som köpte den  

> [!NOTE]  
>   Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="analyzing-by-dimensions"></a>Analys per dimension
Funktionen dimensioner spelar en viktig roll i affärsstöd, exempelvis när du definierar analysvyer. Mer information finns i [Så här analyserar dy data efter dimension](bi-how-analyze-data-dimension.md).

## <a name="dimension-sets"></a>Dimensionsuppsättningar
En dimensionsuppsättning en är en unik kombination av dimensionsvärden. Den lagras som dimensionsuppsättningstransaktioner i databasen. Varje dimensionsuppsättningstransaktion representerar ett enstaka dimensionsvärde. Dimensionsuppsättningen identifieras av ett gemensamt dimensionsuppsättnings-ID som tilldelats varje dimensionsuppsättningstransaktion som tillhör dimensionsuppsättningen.  

När du skapar en journalrad, dokumenthuvud eller dokumentrad kan du ange en kombination av dimensionsvärden. I stället för att uttryckligen lagra varje dimensionsvärde i databasen tilldelas ett dimensionsuppsättnings-ID till journalraden, dokumenthuvudet eller dokumentraden för att specificera dimensionsuppsättningen.  

## <a name="setting-up-dimensions"></a>Lägga upp dimensioner
Du kan ange de dimensioner och dimensionsvärden för att kategorisera journaler och dokument, till exempel försäljningsorder och inköpsorder. Du ställer in dimensioner i fönstret **Dimensioner** där du skapar en rad för varje dimension som t.ex. *Projekt*, *Avdelning*, *Område* och *Säljare*.

Du kan också ställa in värden för dimensioner. Värden kan till exempel vara avdelningarna i företaget. Dimensionsvärden kan anges i en hierarkisk struktur som liknar kontoplanen, så att data kan brytas ned i olika detaljeringsgrader och delmängder av dimensionsvärden kan räknas samman. Du kan definiera så många dimensioner och dimensionsvärden som behövs och alla i företaget kan använda dem.

Du kan också ställa in vissa globala dimensioner och genvägsdimensioner:  

* **Globala dimensioner** används som filter, till exempel i rapporter och batch-jobb. Du kan använda två globala dimensioner, så välj dimensionerna som du ofta använder.
* **Genvägsdimensioner** är tillgängliga som fält på journal- och dokumentrader. Du kan skapa upp till sex av dessa.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Konfigurera standarddimensioner för kunder, leverantörer och andra konton
Du kan tilldela en standarddimension för ett enskilt konto. Dimensionen kopieras till journal eller dokument när du ange numret på en rad, men du kan ta bort eller ändra koden på raden om det behövs. Du kan också göra en dimension obligatorisk för att bokföra en transaktion med en viss typ av konto.  

### <a name="translating-the-names-of-dimensions"></a>Översätta namnet på dimensionerna
När du skapar en dimension, och särskilt genvägsdimension, skapar du egentligen ett anpassat fält eller kolumnrubrik. Om ditt företag är internationellt kan du ange översättningar för namnet på dimensionen. Dokument som innehåller dimensionen använder det översatta namnet där det är tillämpligt.   

### <a name="example-of-dimension-setup"></a>Exempel på dimensionsinställningarna
Anta att ditt företag vill spåra transaktioner utifrån organisationens struktur och geografiska platser. För att göra detta kan du ange två dimensioner i fönstret **Dimensioner**:

* **OMRÅDE**  
* **AVDELNING**  

| Kod | Name | Kodledtext | Filterledtext |
| --- | --- | --- | --- |
| OMRÅDE |Område |Områdeskod |Analysfilter |
| AVDELNING |Avdelning |Avdelningskod |Avdelningsfilter |

För **OMRÅDE**, lägger du till följande dimensionsvärden:

| Kod | Name | Dimensionsvärdetyp |
| --- | --- | --- |
| 10 |Amerika |Från-summa |
| 2.0 |Nordamerika |Standard |
| 30 |Stillahavsområdet |Standard |
| 40 |Sydamerika |Standard |
| 50 |Amerika, hela |Till-summa |
| 60 |Europa |Från-summa |
| 70 |EU |Standard |
| 80 |Utanför EU |Standard |
| 90 |Europa totalt |Till-summa |

För de två huvudsakliga geografiska områdena, USA och Europa, lägger du till underkategorier för områden med indrag av dimensionsvärden. Då kan du rapportera på försäljning eller utgifter i områden och hämta summorna för de större geografiska områdena. Du kan även välja att använda länder eller regioner som dimensionsvärden, eller länder eller orter, beroende på ditt företag.  
> [!NOTE]  
>   Om du vill upprätta en hierarki måste koderna vara i alfabetisk ordning. Det innefattar koderna för dimensionsvärdena som ges i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

För **AVDELNING**, lägger du till följande dimensionsvärden:

| Kod | Name | Dimensionsvärdetyp |
| --- | --- | --- |
| ADMIN |Administration |Standard |
| PROD |Produktion |Standard |
| FÖRS |FÖRS |Standard |

Med detta inställt lägger du sedan till två dimensioner som de två globala dimensionerna i fönstret **Redovisningsinställningar**. Det betyder att du kan använda OMRÅDE och AVDELNING som filter för redovisningstransaktioner, samt i alla rapporter och kontouppställningar. De båda globala dimensionerna blir dessutom automatiskt tillgängliga för att användas som genvägsdimensioner på transaktionsrader och i dokumenthuvuden.  

## <a name="using-dimensions"></a>Använda dimensioner
I ett dokument som t.ex. en försäljningsorder kan du lägga till dimensionsinformation för både en individuell dokumentrad och själva dokument. T.ex. i fönstret **Försäljningsorder** kan du ange dimensionsvärden för de två första genvägsdimensionerna på den individuella försäljningsraden och du kan lägga till ytterligare dimensionsinformation om du väljer knappen **Dimensioner**.  

Om du istället arbetar med en journal kan du lägga till dimensionsinformation i en transaktion om du har lagt upp genvägsdimensioner som fält direkt på journalraderna.  

Du kan ställa in standarddimensioner för konton eller kontotyper, så att dimensioner och dimensionsvärden fylls i automatiskt.  

## <a name="see-also"></a>Se även
[Affärsstöd](bi.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

