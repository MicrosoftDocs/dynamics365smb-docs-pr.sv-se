---
title: "Skapa en inköpsorder från en försäljningsfaktura för att köpa varor till försäljning |  Microsoft Docs"
description: "Om du vill köpa produkter från en försäljningsfaktura skapar du en inköpsfaktura för en leverantör."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 05/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2d7eb238395a0b1060668996fbbc3e13d9dd8a94
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-purchase-items-for-a-sale"></a>Så här köper du artiklar för en försäljning
Du kan använda funktioner snabbt skapa inköpsdokument för saknade artikelkvantiteter som krävs av försäljningen från försäljningsorder och fakturor. Du kan använda två olika funktioner beroende på dokumenttypen.
|Funktion|Description|
|--------|-----------|
|**Skapa inköpsorder**|Från en försäljningsorder skapar den här funktionen en inköpsorder för varje leverantör av artiklar som levererar artiklarna på försäljningsordern. Du kan redigera inköpskvantiteten innan du skapar inköpsorder. Endast ej tillgängligt antal föreslås.
|**Skapa inköpsfaktura**|Från en försäljningsorder och en försäljningsfaktura skapar funktionen en inköpsfaktura för en vald leverantör för alla eller markerade områden i dokumentet. Hela försäljningskvantiteten föreslås.|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a>Så här skapar du inköpsorder för en eller flera serviceorder från en försäljningsorder
Om du vill skapa en inköpsorder för varje artikelkvantitet som inte är tillgängliga på försäljningsordern, använd funktion **skapa inköpsorder**. 

> [!NOTE]  
>   Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

1. Välj panelen **Pågående försäljningsorder** på startsidan.
2. Öppna en försäljningsorder som du vill köpa in artiklar för.
3. Välj åtgärden **Skapa inköpsorder**.

    Fönstret **skapa inköpsorder** öppnas med en rad för varje annan artikeln på försäljningsordern. Rader för helt tillgängligt antal och inte tillgängligt antal (nedtonade) visas som standard. Du kan välja åtgärden **Visa tillgängliga** för att bara visa rader för ej tillgängligt antal.

    Fältet **antal att köpa** innehåller otillgängliga försäljningskvantiteten som standard.
4. Om du vill köpa en annan kvantitet än inte tillgängligt försäljningsantal, redigera värdet i fältet **antal att köpa**.

    > [!NOTE]  
>   Du kan också ändra fältet **antal att köpa** på nedtonade rader även om de representerar helt tillgängligt antal.
5. Välj **OK**. 
    
    En inköpsorder skapas för varje leverantör som levererar artiklarna på försäljningsordern, inklusive kvantitetsändring som du gjorde i fönstret **skapa inköpsorder**.
7. Fortsätt att behandla inköpsorder, till exempel genom att redigera eller lägga till inköpsorderrader. Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md).


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a>Så här skapar du en försäljningsorder från en försäljningsfaktura
Om du vill skapa en enda inköpsorder för en eller flera rader i ett försäljningsdokument väljer du först vilken leverantör som du köper från med funktionen **skapa inköpsfaktura**. 

> [!NOTE]  
>   Den här funktionen skapar en inköpsfaktura för antalet exakt i det valda försäljningsdokumentet. Om du vill ändra antalet inköp, måste du redigera journalen skapas.  

1. Välj panelen **Pågående försäljningsfakturor** på startsidan.
2. Öppna en försäljningfaktura som du vill köpa in artiklar för.
3. Markera en eller flera försäljningsfakturarader som du vill använda i inköpsfakturan. För att använda alla försäljningsfakturarader väljer du antingen all rader eller inga rader alls.
4. Välj åtgärden **Skapa inköpsfaktura**.
5. Välj antingen **Alla rader** eller **Valda rader** och välj sedan knappen **OK**.  
6. Välj leverantören som du vill köpa alla artiklr frpn i listan över leverantörer som kommer att leverera artiklarna eller tjänsterna och välj sedan knappen **OK**.

    En inköpsfaktura skapas som har en, flera eller alla rader på försäljningsfakturan.
7. Fortsätt att behandla inköpsfakturan, till exempel genom att redigera eller lägga till inköpsfakturarader. Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Så här registrerar du inköp](purchasing-how-record-purchases.md)  
[Så här fakturerar du försäljning](sales-how-invoice-sales.md)  
[Så här registrerar du nya leverantörer](purchasing-how-register-new-vendors.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

