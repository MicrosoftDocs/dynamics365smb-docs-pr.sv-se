---
title: Hantera produktvarianter
description: 'Lär dig hur du kan registrera produkter som är nästan identiska men som varierar i färg, storlek eller material som artikelvarianter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Hantera produktvarianter

Artikelvarianter är ett fantastiskt sätt att se till att listan över produkter är under kontroll. Till exempel om du har ett stort antal artiklar som är nästan identiska och endast varierar i färg. Du kan definiera varje variant som en separat artikel. Men du kan också välja att ställa in en artikel och ange olika färger som varianter av artikeln.  

> [!TIP]
> En praktisk introduktion till hur du använder varianter i produktionen finns i [Genomgång: varianter](contoso-coffee/manufacturing/variants.md) för Contoso Coffee-demodata.  

## Lägga till varianter i en artikel

Det är enkelt att definiera varianter för en artikel.  

### Lägga till varianter

1. Öppna [sidan **Artikellista**](https://businesscentral.dynamics.com/?page=31) och öppna sedan relevant artikel.  
2. På sidan **Artikelkort** väljer du åtgärden **Varianter**.  
3. På sidan **Artikelvarianter** anger du varianterna.  

När du sedan skapar ett försäljningsdokument och lägger till artikeln kan du ange varianten av artikeln i fältet **Variantkod**. Detsamma gäller för inköpsdokument.  

## Artikeldisposition per variant

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## Kräver användning av varianter

Från och med utgivningscykel 2 år 2022 kan administratörer kräva att användarna anger varianten i dokument och journaler för artiklar som innehåller varianter. Om du vill aktivera funktionen går du till sidan **Lagerinställningar** och väljer fältet **Variant obligatorisk om den finns**. Du kan åsidosätta den globala inställningen för specifika artiklar.  

På artikelkort har fältet **Variant obligatorisk om den finns** följande alternativ:

|Fältvärde |Description|
|---------|----|
|Standard (Nej)| Inställningen från **Lagerinställningar** gäller för artikeln.|
|Nr| Användare behöver inte ange en variant för den här artikeln.|
|Ja| Om artikeln har en eller flera varianter måste användarna ange relevant variant. Om de inte gör det hindras de från att bokföra transaktionen.|

> [!NOTE]
> Dessa inställningar påverkar inte artiklar som saknar varianter.

Om funktionen är aktiverad kan användarna inte bokföra en transaktion om inte varianten har angetts.

## Kategorier, attribut och varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## Se även

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Ställa in allmän lagerinformation](inventory-how-setup-general.md)  
[Genomgång: varianter](contoso-coffee/manufacturing/variants.md)  
