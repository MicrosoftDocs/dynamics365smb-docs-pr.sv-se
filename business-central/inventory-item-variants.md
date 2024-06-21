---
title: Hantera produktvarianter
description: 'Lär dig hur du kan registrera produkter som är nästan identiska men som varierar i färg, storlek eller material som artikelvarianter.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="manage-product-variants"></a>Hantera produktvarianter

Artikelvarianter är ett fantastiskt sätt att se till att listan över produkter är under kontroll. Till exempel om du har ett stort antal artiklar som är nästan identiska och endast varierar i färg. Du kan definiera varje variant som en separat artikel. Men du väljer att ställa in en artikel och ange olika färger som varianter av artikeln.  

> [!TIP]
> En praktisk introduktion till hur du använder varianter i produktionen finns i [Genomgång: varianter](contoso-coffee/manufacturing/variants.md) för Contoso Coffee-demodata.  

## <a name="add-variants-to-an-item"></a>Lägga till varianter i en artikel

Om ditt företag har beslutat att använda varianter är det enkelt nog att definiera varianter för en artikel.  

### <a name="to-add-variants"></a>Lägga till varianter

1. Öppna [sidan **Artikellista**](https://businesscentral.dynamics.com/?page=31) och öppna relevant artikel.  
2. På kortet **Artikel** väljer du åtgärden **Artikel** och väljer sedan åtgärden **Varianter**.  
3. På sidan **Artikelvarianter** anger du varianterna.  

När du sedan skapar ett försäljningsdokument och lägger till artikeln kan du ange varianten av artikeln i fältet **Variantkod**. Detsamma gäller för inköpsdokument.  

## <a name="item-availability-by-variant"></a>Artikeldisposition per variant

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a>Kräver användning av varianter

Från och med utgivningscykel 2 år 2022 kan administratörer kräva att användarna anger varianten i dokument och journaler för artiklar som innehåller varianter. Om du vill aktivera funktionen går du till sidan **Lagerinställningar** och väljer fältet **Variant obligatorisk om den finns**. Du kan åsidosätta den globala inställningen för specifika artiklar.  

På artikelkort har fältet **Variant obligatorisk om den finns** följande alternativ:

|Fältvärde |Description|
|---------|----|
|Standard| Inställningen från **Lagerinställningar** gäller för artikeln.|
|Nr| Användare behöver inte ange en variant för den här artikeln.|
|Ja| Om artikeln har en eller flera varianter måste användarna ange relevant variant. Om de inte gör det hindras de från att bokföra transaktionen.|

> [!NOTE]
> Dessa inställningar påverkar inte artiklar som saknar varianter.

Om funktionen är aktiverad kan användarna inte bokföra en transaktion om inte varianten har angetts.

## <a name="categories-attributes-and-variants"></a>Kategorier, attribut och varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Se även

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Ställa in allmän lagerinformation](inventory-how-setup-general.md)  
[Genomgång: varianter](contoso-coffee/manufacturing/variants.md)  
