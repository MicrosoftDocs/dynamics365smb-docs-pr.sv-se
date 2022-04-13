---
title: Köpa artiklar för en försäljning
description: Om du vill köpa produkter från en försäljningsfaktura skapar du en inköpsfaktura för en leverantör.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.search.form: 50, 51, 56, 9308
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b7fe34b7edcba01d25107ead47dc917dabde07a5
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514861"
---
# <a name="purchase-items-for-a-sale-by-creating-purchase-invoices"></a>Köpa artiklar till försäljning genom att skapa inköpsfakturor

Du kan använda funktioner snabbt skapa inköpsdokument för saknade artikelkvantiteter som krävs av försäljningen från försäljningsorder och fakturor. Du kan använda två olika funktioner beroende på dokumenttypen.

> [!Note]
> Den här funktionen är för att fylla på försäljningsartiklar i ditt eget lager. Om du vill köpa artiklar för direktutleverans från din leverantör till kunden, måste du skapa en direktleverans. För mer information finns i [Utföra direktleveranser](sales-how-drop-shipment.md).   

|Funktion|Description|
|--------|-----------|
|**Skapa inköpsorder**|Från en försäljningsorder skapar den här funktionen en inköpsorder för varje leverantör av artiklar som levererar artiklarna på försäljningsordern. Du kan redigera inköpskvantiteten innan du skapar inköpsorder. Endast ej tillgängligt antal föreslås.
|**Skapa inköpsfaktura**|Från en försäljningsorder och en försäljningsfaktura skapar funktionen en inköpsfaktura för en vald leverantör för alla eller markerade områden i dokumentet. Hela försäljningskvantiteten föreslås.|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a>Så här skapar du inköpsorder för en eller flera serviceorder från en försäljningsorder
Om du vill skapa en inköpsorder för varje artikelkvantitet som inte är tillgängliga på försäljningsordern, använd funktion **skapa inköpsorder**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
2. Öppna en försäljningsorder som du vill köpa in artiklar för.
3. Välj åtgärden **Skapa inköpsorder**.

    Sidan **skapa inköpsorder** öppnas med en rad för varje annan artikeln på försäljningsordern. Rader för helt tillgängligt antal och inte tillgängligt antal (nedtonade) visas som standard. Du kan välja åtgärden **Visa tillgängliga** för att bara visa rader för ej tillgängligt antal.

    Fältet **antal att köpa** innehåller otillgängliga försäljningskvantiteten som standard.
4. Om du vill köpa en annan kvantitet än inte tillgängligt försäljningsantal, redigera värdet i fältet **antal att köpa**.

    > [!NOTE]  
    >   Du kan också ändra fältet **antal att köpa** på nedtonade rader även om de representerar helt tillgängligt antal.
5. Välj **OK**.

    En inköpsorder skapas för varje leverantör som levererar artiklarna på försäljningsordern, inklusive kvantitetsändring som du gjorde på sidan **skapa inköpsorder**.
7. Fortsätt att behandla inköpsorder, till exempel genom att redigera eller lägga till inköpsorderrader. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a>Så här skapar du en försäljningsorder från en försäljningsfaktura
Om du vill skapa en enda inköpsorder för en eller flera rader i ett försäljningsdokument väljer du först vilken leverantör som du köper från med funktionen **skapa inköpsfaktura**.

> [!NOTE]  
>   Den här funktionen skapar en inköpsfaktura för antalet exakt i det valda försäljningsdokumentet. Om du vill ändra antalet inköp, måste du redigera journalen skapas.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
2. Öppna en försäljningfaktura som du vill köpa in artiklar för.
3. Markera en eller flera försäljningsfakturarader som du vill använda i inköpsfakturan. För att använda alla försäljningsfakturarader väljer du antingen all rader eller inga rader alls.
4. Välj åtgärden **Skapa inköpsfaktura**.
5. Välj antingen **Alla rader** eller **Valda rader** och välj sedan knappen **OK**.  
6. Välj leverantören som du vill köpa alla artiklr frpn i listan över leverantörer som kommer att leverera artiklarna eller tjänsterna och välj sedan knappen **OK**.

    En inköpsfaktura skapas som har en, flera eller alla rader på försäljningsfakturan.
7. Fortsätt att behandla inköpsfakturan, till exempel genom att redigera eller lägga till inköpsfakturarader. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Registrera inköp](purchasing-how-record-purchases.md)  
[Fakturaförsäljning](sales-how-invoice-sales.md)  
[Registrera nya leverantörer](purchasing-how-register-new-vendors.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]