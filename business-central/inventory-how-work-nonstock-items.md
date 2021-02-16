---
title: Skapa och hantera katalogartiklar | Microsoft Docs
description: Beskriver hur du byter artiklar som finns i leverantörslistan av artiklar, men inte i listan med poster.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cf6016b2d2f2774807b120ab3d3521af9eaf5f7f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749911"
---
# <a name="work-with-catalog-items"></a>Arbeta med katalogartiklar
Du kan erbjuda vissa artiklar till dina kunder för deras bekvämlighet, som du inte vill hantera i ditt system, tills du börjar sälja dem. När du vill börja hantera sådana artiklar i ditt system, kan du konvertera dem till vanliga artikelkort på två sätt.

* Från ett kort för katalogartikel skapar skapar du ett nytt lagerkort baserat på en mall.
* Från en försäljningsorderrad av typen **Artikel** med ett tomt fält **Nr** väljer du en katalogartikel. Ett artikelkort skapas sedan automatiskt för katalogartikeln.

> [!NOTE]  
> Du kan inte välja en katalogartikel från sidan **Försäljningsfaktura**.<br /><br />
> Du kan välja en katalogartikel från sidan **Försäljningsoffert** men katalogartikeln kommer inte att omvandlas till en vanlig artikel när du använder funktionen **Gör beställning**.

En katalogartikel har vanligtvis artikelnumret från den leverantör som levererar den. Om du vill aktivera konvertering av ett kort för en katalogartikel till ett vanligt artikelkort måste du först ställa in hur leverantörens artikelnumrering konverteras till din egen artikelnumrering.   

> [!Important]
> Katalogartiklar ska inte förväxlas med icke-lagerartiklar, som är vanliga artiklar som ges typen **Inte i lager** för att hålla dem från tillgänglighets- och kostnadsberäkningar, till exempel eftersom de endast används internt och har en låg kostnad. Mer information om typerna finns i [Om artikeltyper](inventory-about-item-types.md).

## <a name="to-create-a-catalog-item"></a>Så här skapar du en katalogartikel
Kort för katalogartiklar har mycket mindre information än normala artikelkort, eftersom du bara använder dem för att erbjuda på offerter och på andra sätt. Därför måste de konverteras till normala artikelkort, innan du kan bokföra försäljningstransaktioner för dem.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Katalogartiklar** och välj sedan tillhörande länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Så här ställer du in katalogartikelnummer konverteras till ditt eget nummer
Om du vill aktivera konvertering av ett kort för katalogartikel till ett vanligt artikelkort måste du först ställa in hur leverantörens artikelnumrering konverteras till dit eget nummerformat.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för katalogartikel** och välj sedan tillhörande länk.
2. Fyll i fälten om det behövs.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>Om du vill omvandla en katalogartikel till en normal artikel
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Katalogartiklar** och välj sedan tillhörande länk.
2. Öppna kortet för den katalogartikel som du vill konvertera till en normalt artikel.
3. På sidan **Katalogartikelkort** väljer du åtgärden **Skapa artikel**.

Ett nytt artikelkort förifyllt med information från katalogartikeln och en relevant artikelmall skapas. Du kan sedan ange eller redigera fält på det nya artikelkortet vid behov. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Om du vill sälja en katalogartikel och konvertera den till en normal artikel
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**. Fyll i övriga fält på snabbfliken **Allmänt** som för alla andra försäljningsorder. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
3. På en ny försäljningsrad i fältet **Typ** väljer du **Artikel**, men lämnar **Nr.** tomt.
4. Välj åtgärden **Rad** och välj sedan åtgärden **Välj katalogartiklar**.

    Katalogartikeln omvandlas till en normal artikel. Ett nytt artikelkort förifyllt med information från katalogartikeln och en relevant artikelmall skapas.
5. På sidan **Katalogartiklar** väljer du den katalogartikel som du vill sälja och väljer sedan knappen **OK**.
6. När försäljningsordern är slutförd väljer du åtgärden **Bokföra**.

Du kan sedan ange eller redigera fält på det nya artikelkortet vid behov. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

> [!NOTE]  
>   En korsreferenspost för artikel skapas automatiskt för den leverantör som levererar artikeln mellan leverantörens artikelnummer och det nya artikelnumret. Mer information finns i [Använd artikeltvärreferenser](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Se även
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Skapa specialorder](sales-how-to-create-special-orders.md)|  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
