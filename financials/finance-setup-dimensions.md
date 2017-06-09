---
title: "Ställa in dimensioner | Microsoft Docs"
description: "Du kan ange de dimensioner och dimensionsvärden som du vill använda för att kategorisera journaler och dokument, till exempel försäljningsorder och inköpsorder."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/28/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0da77c5be3b49f715384752ad61fc072aea8525c
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-dimensions"></a>Lägga upp dimensioner
Du kan ange de dimensioner och dimensionsvärden för att kategorisera journaler och dokument, till exempel försäljningsorder och inköpsorder. Du ställer in dimensioner i fönstret **Dimensioner** där du skapar en rad för varje dimension som t.ex. *Projekt*, *Avdelning*, *Område* och *Säljare*.

Du kan också ställa in värden för dimensioner. Värden kan till exempel vara avdelningarna i företaget. Dimensionsvärden kan anges i en hierarkisk struktur som liknar kontoplanen, så att data kan brytas ned i olika detaljeringsgrader och delmängder av dimensionsvärden kan räknas samman. Du kan definiera så många dimensioner och dimensionsvärden som behövs och alla i företaget kan använda dem.

Du kan också ställa in vissa globala dimensioner och genvägsdimensioner:  

* **Globala dimensioner** används som filter, till exempel i rapporter och batch-jobb. Du kan använda två globala dimensioner, så välj dimensionerna som du ofta använder.
* **Genvägsdimensioner** är tillgängliga som fält på journal- och dokumentrader. Du kan skapa upp till sex av dessa.  

**Obs!** den här funktionen kräver att din upplevelse är inställd på **Paket **. Mer information finns i avsnittet [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Konfigurera standarddimensioner för kunder, leverantörer och andra konton
Du kan tilldela en standarddimension för ett enskilt konto. Dimensionen kopieras till journal eller dokument när du ange numret på en rad, men du kan ta bort eller ändra koden på raden om det behövs. Du kan också göra en dimension obligatorisk för att bokföra en transaktion med en viss typ av konto.  

## <a name="translate-the-names-of-dimensions"></a>Översätta namnet på dimensionerna
När du skapar en dimension, och särskilt genvägsdimension, skapar du egentligen ett anpassat fält eller kolumnrubrik. Om ditt företag är internationellt kan du ange översättningar för namnet på dimensionen. Dokument som innehåller dimensionen använder det översatta namnet där det är tillämpligt.   

## <a name="example"></a>Exempel
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
**Obs!** Om du vill upprätta en hierarki måste koderna vara i alfabetisk ordning. Det innefattar koderna för dimensionsvärdena som ges i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

För **AVDELNING**, lägger du till följande dimensionsvärden:

| Kod | Name | Dimensionsvärdetyp |
| --- | --- | --- |
| ADMIN |Administration |Standard |
| PROD |Produktion |Standard |
| FÖRS |FÖRS |Standard |

Med detta inställt lägger du sedan till två dimensioner som de två globala dimensionerna i fönstret **Redovisningsinställningar**. Det betyder att du kan använda OMRÅDE och AVDELNING som filter för redovisningstransaktioner, samt i alla rapporter och kontouppställningar. De båda globala dimensionerna blir dessutom automatiskt tillgängliga för att användas som genvägsdimensioner på transaktionsrader och i dokumenthuvuden.  

Du kan börja lägga till dimensioner i dokument och journaler när detta har ställts in. Mer information finns i [Dimensioner](finance-dimensions.md).  

## <a name="see-also"></a>Se även
[Dimensioner](finance-dimensions.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

