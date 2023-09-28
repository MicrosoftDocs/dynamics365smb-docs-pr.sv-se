---
title: Skapa och hantera katalogartiklar
description: Lär dig hur du säljer artiklar som du inte har kvar i listan över artiklar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
---

# <a name="work-with-catalog-items"></a>Arbeta med katalogartiklar

Katalog artiklar är artiklar som du inte hanterar [!INCLUDE[prod_short](includes/prod_short.md)] förrän du säljer dem. När du använder åtgärden **Välj katalogartikel** för att lägga till en katalogartikel på en rad i en försäljningsorder, offert eller avropsorder för försäljning konverteras katalogartikeln till en vanlig artikel.

> [!NOTE]  
> Du kan inte välja en katalogartikel från sidan **Försäljningsfaktura**.

En katalogartikel har vanligtvis artikelnumret från den leverantör som levererar den. Innan du kan konvertera en katalogartikel till en normal artikel måste du ange hur leverantörens artikel nummer ska konverteras till artikel numret. För mer information om artikelnumrering, gå till [Så här ställer du in hur katalogartikelnummer konverteras till ditt eget nummer](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Katalogartiklar ska inte förväxlas med icke-lagerartiklar, som är vanliga artiklar som ges typen **Inte i lager** för att hålla dem från tillgänglighets- och kostnadsberäkningar, till exempel eftersom de endast används internt och har en låg kostnad. Om du vill veta mer om artiklar som inte finns i lager går du till [Om artikeltyper](inventory-about-item-types.md).

## <a name="create-a-catalog-item"></a>Skapar du en katalogartikel

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **katalogartiklar** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Ställ in katalogartikelnummer konverteras till ditt eget nummer

Innan du kan konvertera en katalogartikel till en vanlig artikel måste du ange hur leverantörens artikel nummer ska konverteras till strukturen du använder för artikelnummer.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inställning av katalogartiklar** och väljer sedan relaterad länk.
2. I fältet **Nummerformat** väljer du det alternativ du vill använda.

## <a name="convert-a-catalog-item-to-a-normal-item"></a>Om du vill omvandla en katalogartikel till en normal artikel

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **katalogartiklar** och väljer sedan relaterad länk.
2. Öppna kortet för den katalogartikel som du vill konvertera till en normalt artikel.
3. På sidan **Katalogartikelkort** väljer du åtgärden **Skapa artikel**.

Ett nytt artikelkort förifyllt med information från katalogartikeln och en artikelmall skapas. Du kan redigera informationen om den nya artikeln om det behövs. För att lära dig mer om att skapa artiklar, gå till [Registrera nya artiklar](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Om du vill sälja en katalogartikel och konvertera den till en normal artikel

I följande processer används en försäljningsorder, men stegen är desamma för avropsorder för försäljning och offerter.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**. Fyll i övriga fält på snabbfliken **Allmänt** som för alla andra försäljningsorder. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
3. På en ny försäljningsrad i fältet **Typ** väljer du **Artikel**, men lämnar **Nr.** tomt.
4. Välj åtgärden **Rad** och välj sedan åtgärden **Välj katalogartiklar**.
5. På sidan **Katalogartiklar** väljer du den katalogartikel som du vill sälja och väljer sedan knappen **OK**.
6. När försäljningsordern är slutförd väljer du åtgärden **Bokföra**.

> [!NOTE]  
> En artikelreferens skapas mellan leverantörens artikelnummer och det nya artikelnumret. Om du vill veta mer om artikelreferenser går du till [Använd artikelreferenser](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Se även

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Skapa specialorder](sales-how-to-create-special-orders.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
