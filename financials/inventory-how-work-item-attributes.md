---
title: Skapa artikelattribut och deldela dem till artiklar | Microsoft Docs
description: "Beskriver hur du ställer in artikelattributvärden, till exempel som kan användas som sökord och tilldela dem till artiklar och artikelkategorier."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f071cca7df5bb1d3eac6f013784c0ca13e36477c
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-item-attributes"></a>Så här arbetar du med Artikelattribut
När kunder gör förfrågningar om en artikel, antingen i motsvarande fält eller via en integrerad webbutik kan kunden fråga eller söka efter egenskaper som till exempel höjd och modellår. För att tillhandahålla denna kundservice kan du tilldela artikelattributvärden av andra typer till artiklarna, som sedan kan användas när du söker efter artiklar.

Du kan också tilldela till artikelattribut till artikelkategorier, som sedan kopplas till artiklarna som använder artikelkategorierna. För mer information finns i [Så här kategoriserar du artiklar](inventory-how-categorize-items.md).

> [!Tip]  
> Om du kopplar bilder till poster, kan tillägget Image Analyzer identifiera attribut i bilden och föreslå attribut så att du kan bestämma om du vill tilldela dem. Filnamnstillägget är klar. Du måste aktivera det. Mer information finns i [tillägget Image Analyzer för Microsoft Dynamics 365 for Financials](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>Så här skapar du artikelattribut
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikelattribut** och välj sedan relaterad länk.
2. I fönstret **Artikelattribut** väljer du åtgärden **Ny**.
3. I fönstret **Artikelattribut** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>    Om du väljer **Alternativ** i fältet **Typ** kan du välja åtgärden **Artikelattributvärden** för att markera eller skapa artikelattributvärden. Mer information finns i avsnittet "Att skapa artikelattributvärden av typen alternativ".  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Så här skapar du värden för artikelattribut av typen alternativ
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikelattribut** och välj sedan relaterad länk.
2. I fönstret **Artikelattribut** markerar du ett artikelattribut av typen **Alternativ** som du vill tilldela värden på, och väljer sedan åtgärden **Artikelattributvärden**.
3. I fönstret **Artikelattributvärden** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Så här tilldelar du ett artikelattribut till en artikel
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.
2. I fönstret **Artiklar** markerar du den artikel som du vill tilldela artikelattribut på, och väljer sedan åtgärden **Attribut**.
3. I fönstret **Artikelattributvärden** väljer du åtgärden **Ny**.
4. Välj sökknappen i fältet **Attribut** och välj ett befintligt artikelattribut. Välj alternativt åtgärden **Ny** för att först skapa en ny artikelattribut som förklaras i avsnittet "Att skapa artikelattribut".
5. I fältet **Värde** anger du artikelattributvärdet , exempelvis "2010" för attributet **modellår** attribute.
6. För artikelattribut av typen **Alternativ** väljer du sökknappen i fältet **Värde** och väljer sedan ett artikelattributvärde. Välj alternativt åtgärden **Ny** för att först skapa ett nytt artikelattributvärde som förklaras i avsnittet "Att skapa värden för artikelattribut av typen Alternativ".
7. Upprepa steg 4 genom 6 för alla artikelattribut som du vill tilldela artikeln.

## <a name="to-assign-item-attributes-to-item-categories"></a>Så här tilldelar du ett artikelattribut till artikelkategorier
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikelkategorier** och välj sedan relaterad länk.
2. I fönstret **Artikelkategorier** markerar du den artikelkategori, som du vill tilldela artikelattributen till och väljer sedan åtgärden **Redigera**.
3. I fönstret **Artikelkategorikort** på snabbfliken **Attribut** väljer du åtgärden **Ny**.
4. Välj sökknappen i fältet **Attribut** och välj ett befintligt artikelattribut. Välj alternativt åtgärden **Ny** för att först skapa en ny artikelattribut som förklaras i avsnittet "Att skapa ett artikelattribut".
5. I fältet **Standaardvärde** väljer du sökknappen och väljer du ett artikelattributvärde.
6. Upprepa steg 4 genom 5 för alla artikelattribut som du vill tilldela artikelkategorin.

> [!NOTE]  
>   Artikelattribut för överordnade artikelkategorier kommer att ärvas av underordnade artikelkategorier. Detta indikeras av fältet **Ärvd från** på snabbfliken **Attribut**. För mer information finns i [Så här kategoriserar du artiklar](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Filtrera artikel efter attribut
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.
2. I fönstret **Artiklar** väljer du åtgärden **Filtrera efter attribut**.
3. I fönstret **Filtrera artiklar efter attribut** väljer du sökknappen i fältet **Attribut** och väljer sedan ett artikelattribut.
4. I fältet **Värde** väljer du sökknappen och väljer du ett befintligt artikelattributvärde att filtrera efter.

    > [!NOTE]  
>   Du kan bara välja värden direkt för artikelattribut som har fasta värden, till exempel färg. För artikelattribut, som har variabelvärden, till exempel bredd, måste du ange artikelattributvärdet, genom att först välja ett villkor. Se steg 5.
5. I fältet **Värde** ett variabelt artikelattribut väljer du sökknappen.
6. I fönstret **Ange filtervärde** i fältet **Villkor** väljer du villkor med listpilen.
7. I fältet **Värde** anger du ett attributvärde för att filtrera artiklar.

    **Exempel** För att filtrera efter artiklar där materialbeskrivningen börjar med "blå", fyller du i fälten enligt följande: fältet **Attribut**: Materialbeskrivning, fältet **Villkor**: Börjar med, **Värde**: blå.
8. Välj **OK**.   

Artiklarna i fönstret **Artiklar** filtreras efter de angivna artikelattributvärdena.

## <a name="see-also"></a>Se även
[Så här kategoriserar du artiklar](inventory-how-categorize-items.md)    
[Så här registrerar du nya objekt](inventory-how-register-new-items.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

