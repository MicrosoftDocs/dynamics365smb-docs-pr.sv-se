---
title: Använda artikelreferenser
description: 'Skapa referenser mellan beskrivningar, måttenheter och varianter som du och leverantören eller kunden använder för en artikel.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 05/16/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Använda artikelreferenser

Om du köper eller säljer artiklar som du och leverantören eller kunden använder olika villkor för kan du ställa in en referens mellan villkoren för artiklarna och villkoren som kunden eller leverantören för artikeln använder. På så sätt infogas leverantörens eller kundens artikelbeskrivning, enhet eller variantkod automatiskt på de relevanta dokumenten när du fyller i fältet **Artikelreferensnummer.** .  

## Så här ställer du in en artikelreferens

1. Välj ikonen :::image type="icon" source="media/ui-search/search_small.png" border="false":::, ange **Artiklar** och välj sedan relaterad länk.
2. Öppna kortet för en artikel som du vill skapa en referens för.
3. Välj åtgärden **Artikelreferens**.

     Om du inte hittar åtgärden **Artikelreferenser** väljer du att visa fler alternativ och hittar den sedan under **Relaterad** > **artikel**.
  
4. På en ny rad på sidan **Artikel referenstrans.**, fyll i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Följande procedur beskriver hur du anger artikelreferensen på en inköpsorder. Liknande steg gäller för försäljningsdokument och andra inköpsdokument.  

## Ange leverantörens artikelbeskrivning på ett dokument

1. Välj ikonen :::image type="icon" source="media/ui-search/search_small.png" border="false":::, ange **inköpsorder** och välj sedan relaterad länk.
2. Skapa en inköpsorder för leverantören som du ställer in en artikelreferens för ovan.
3. Skapa en inköpsorderrad för artikeln som du ställer in en artikelreferens för ovan.
4. I artikelns referensnummer **.** välj relevant artikelreferens och välj sedan knappen **OK**.

Fältet **beskrivning** på raden skrivs över med leverantörens artikelbeskrivning som ställs in på referensartikelns transaktion. Om artikelreferensen innehåller en variantkod eller en måttenhet kopieras dessa värden också till dokumentet.  

## Skanna streckkoder med Business Central-mobilappen

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

I följande tabell visas de sidor som stöder streckkodsskanning för artikelreferenser från mobilappen [!INCLUDE [prod_short](includes/prod_short.md)].

|Sida  |Fältvärde som du kan skanna  |
|---------|---------|
|Artikelreferens     | Referensnr        |
|Artikeljournalrad     | Artikelreferensnr        |
|Inventeringsorderrad     |Artikelreferensnr         |
|Inköpsrad     |   Artikelreferensnr      |
|Försäljningsrad     | Artikelreferensnr        |

## Se även

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
