---
title: Skapa artikelattribut och koppla dem till artiklar
description: Beskriver hur du ställer in artikelattributvärden, till exempel som kan användas som sökord och tilldela dem till artiklar och artikelkategorier.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.search.forms: 7507, 7509, 7506, 7505, 7503, 7502, 7510, 7504, 7501, 7500, 9110, 5734, 7508
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 73ee4d6e2c8a2630e75ff2ccb1210c46c58b4ba3
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130378"
---
# <a name="work-with-item-attributes"></a>Arbeta med artikelattribut
När kunder gör förfrågningar om en artikel, antingen i motsvarande fält eller via en integrerad webbutik kan kunden fråga eller söka efter egenskaper som till exempel höjd och modellår. För att tillhandahålla denna kundservice kan du tilldela artikelattributvärden av andra typer till artiklarna, som sedan kan användas när du söker efter artiklar.

Du kan också tilldela till artikelattribut till artikelkategorier, som sedan kopplas till artiklarna som använder artikelkategorierna. Mer information finns i [Kategorisera artikel](inventory-how-categorize-items.md).

> [!Tip]  
> Om du kopplar bilder till poster, kan tillägget Image Analyzer identifiera attribut i bilden och föreslå attribut så att du kan bestämma om du vill tilldela dem. Filnamnstillägget är klar. Du måste aktivera det. Mer information finns i [Tillägget Image Analyzer för](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>Så här skapar du artikelattribut
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikelattribut** och väljer sedan relaterad länk.
2. På sidan **Artikelattribut** väljer du åtgärden **Ny**.
3. På sidan **Artikelattribut** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Om du väljer **Alternativ** i fältet **Typ** kan du välja åtgärden **Artikelattributvärden** för att skapa artikelattributvärden. Mer information finns i [Att skapa artikelattributvärden av typen alternativ](inventory-how-work-item-attributes.md#to-create-values-for-item-attributes-of-type-option).  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Så här skapar du värden för artikelattribut av typen alternativ
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikelattribut** och väljer sedan relaterad länk.
2. På sidan **Artikelattribut** markerar du ett artikelattribut av typen **Alternativ** som du vill tilldela värden på, och väljer sedan åtgärden **Artikelattributvärden**.
3. På sidan **Artikelattributvärden** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Så här tilldelar du ett artikelattribut till en artikel
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. På sidan **Artiklar** markerar du den artikel som du vill tilldela artikelattribut på, och väljer sedan åtgärden **Attribut**.
3. På sidan **Artikelattributvärden** väljer du åtgärden **Ny**.
4. Välj sökknappen i fältet **Attribut** och välj ett befintligt artikelattribut. Välj alternativt åtgärden **Ny** för att först skapa en ny artikelattribut som förklaras i [Att skapa artikelattribut](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. I fältet **Värde** anger du artikelattributvärdet , exempelvis "2010" för attributet **modellår** attribute.
6. För artikelattribut av typen **Alternativ** väljer du sökknappen i fältet **Värde** och väljer sedan ett artikelattributvärde. Välj alternativt åtgärden **Ny** för att först skapa ett nytt artikelattributvärde som förklaras i [Att skapa värden för artikelattribut av typen Alternativ](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-items).
7. Upprepa steg 4 genom 6 för alla artikelattribut som du vill tilldela artikeln.

## <a name="to-assign-item-attributes-to-item-categories"></a>Så här tilldelar du ett artikelattribut till artikelkategorier
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikelkategorier** och väljer sedan relaterad länk.
2. På sidan **Artikelkategorier** markerar du den artikelkategori, som du vill tilldela artikelattributen till och väljer sedan åtgärden **Redigera**.
3. På sidan **Artikelkategorikort** på snabbfliken **Attribut** väljer du åtgärden **Ny**.
4. Välj sökknappen i fältet **Attribut** och välj ett befintligt artikelattribut. Välj alternativt åtgärden **Ny** för att först skapa en ny artikelattribut som förklaras i [Att skapa artikelattribut](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. I fältet **Standaardvärde** väljer du sökknappen och väljer du ett artikelattributvärde.
6. Upprepa steg 4 genom 5 för alla artikelattribut som du vill tilldela artikelkategorin.

> [!NOTE]  
>   Artikelattribut för överordnade artikelkategorier kommer att ärvas av underordnade artikelkategorier. Detta indikeras av fältet **Ärvd från** på snabbfliken **Attribut**. Mer information finns i [Kategorisera artiklar](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Filtrera artikel efter attribut
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. På sidan **Artiklar** väljer du åtgärden **Filtrera efter attribut**.
3. På sidan **Filtrera artiklar efter attribut** väljer du sökknappen i fältet **Attribut** och väljer sedan ett artikelattribut.
4. I fältet **Värde** väljer du sökknappen och väljer du ett befintligt artikelattributvärde att filtrera efter.

    > [!NOTE]  
    >   Du kan bara välja värden direkt för artikelattribut som har fasta värden, till exempel färg. För artikelattribut, som har variabelvärden, till exempel bredd, måste du ange artikelattributvärdet, genom att först välja ett villkor. Se steg 5.
5. I fältet **Värde** ett variabelt artikelattribut väljer du sökknappen.
6. På sidan **Ange filtervärde** i fältet **Villkor** väljer du villkor med listpilen.
7. I fältet **Värde** anger du ett attributvärde för att filtrera artiklar.

    **Exempel** För att filtrera efter artiklar där materialbeskrivningen börjar med "blå", fyller du i fälten enligt följande: fältet **Attribut**: Materialbeskrivning, fältet **Villkor**: Börjar med, **Värde**: blå.
8. Välj knappen **OK**.   

Artiklarna på sidan **Artiklar** filtreras efter de angivna artikelattributvärdena.

## <a name="see-also"></a>Se även
[Kategorisera artiklar](inventory-how-categorize-items.md)    
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]