---
title: Skapa och hantera katalogartiklar
description: Beskriver hur du säljer artiklar som du inte har kvar i listan över artiklar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.search.forms: 5725, 5726, 5732
ms.date: 06/20/2022
ms.author: bholtorf
ms.openlocfilehash: c12eb256d4e7f1e211e28dacf4c403406dba3d85
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077013"
---
# <a name="work-with-catalog-items"></a>Arbeta med katalogartiklar

Katalog artiklar är artiklar som du inte hanterar [!INCLUDE[prod_short](includes/prod_short.md)] förrän du säljer dem. När du använder åtgärden **Välj katalog artikel** för att lägga till en katalogartikel på en rad i en försäljningsorder eller offert, konverteras katalog artikeln till en vanlig artikel.

> [!NOTE]  
> Du kan inte välja en katalogartikel från sidan **Försäljningsfaktura**.

En katalogartikel har vanligtvis artikelnumret från den leverantör som levererar den. Innan du kan konvertera en katalogartikel till en normal artikel måste du ange hur leverantörens artikel nummer ska konverteras till artikel numret. För mer information, se [Så här ställer du in katalogartikelnummer konverteras till ditt eget nummer](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Katalogartiklar ska inte förväxlas med icke-lagerartiklar, som är vanliga artiklar som ges typen **Inte i lager** för att hålla dem från tillgänglighets- och kostnadsberäkningar, till exempel eftersom de endast används internt och har en låg kostnad. Mer information om typerna finns i [Om artikeltyper](inventory-about-item-types.md).

## <a name="create-a-catalog-item"></a>Skapar du en katalogartikel

Kort för katalogartiklar har mycket mindre information än normala artikelkort, eftersom du bara använder dem för att erbjuda på offerter och på andra sätt. Därför måste de konverteras till normala artikelkort, innan du kan bokföra försäljningstransaktioner för dem.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **katalogartiklar** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Ställ in katalogartikelnummer konverteras till ditt eget nummer

Innan du kan konvertera en katalogartikel till en normal artikel måste du ange hur leverantörens artikel nummer ska konverteras till artikel numret.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inställning av katalogartiklar** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs.

## <a name="convert-a-catalog-item-to-a-normal-item"></a>Om du vill omvandla en katalogartikel till en normal artikel

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **katalogartiklar** och väljer sedan relaterad länk.
2. Öppna kortet för den katalogartikel som du vill konvertera till en normalt artikel.
3. På sidan **Katalogartikelkort** väljer du åtgärden **Skapa artikel**.

Ett nytt artikelkort förifyllt med information från katalogartikeln och en relevant artikelmall skapas. Du kan sedan ange eller redigera fält på det nya artikelkortet vid behov. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Om du vill sälja en katalogartikel och konvertera den till en normal artikel

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**. Fyll i övriga fält på snabbfliken **Allmänt** som för alla andra försäljningsorder. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
3. På en ny försäljningsrad i fältet **Typ** väljer du **Artikel**, men lämnar **Nr.** tomt.
4. Välj åtgärden **Rad** och välj sedan åtgärden **Välj katalogartiklar**.

    Katalogartikeln omvandlas till en normal artikel. Ett nytt artikelkort förifyllt med information från katalogartikeln och en relevant artikelmall skapas.
5. På sidan **Katalogartiklar** väljer du den katalogartikel som du vill sälja och väljer sedan knappen **OK**.
6. När försäljningsordern är slutförd väljer du åtgärden **Bokföra**.

Du kan sedan ange eller redigera fält på det nya artikelkortet vid behov. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

> [!NOTE]  
> En artikelreferens skapas mellan leverantörens artikelnummer och det nya artikelnumret. Mer information finns i [Använd artikelreferenser](inventory-how-use-item-cross-refs.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Skapa specialorder](sales-how-to-create-special-orders.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
