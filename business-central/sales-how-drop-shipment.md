---
title: Koppla en försäljningsorder till en inköpsorder för direktleverans | Microsoft Docs
description: Beskriver hur du skapar en försäljningsorder som är länkad till en inköpsorder för att tillåta leverans direkt från leverantören till kunden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 50198afaa8caae9a11a06a25357fa94ad26b0b8f
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943191"
---
# <a name="make-drop-shipments"></a>Skapa direktleveranser
Direktleverans innebär leverans av artiklar från någon av företagets leverantörer direkt till någon av företagets kunder.

När en försäljningsorder har markerats för direktleverans och du skapar en inköpsorder som anger kunden i fältet **Leverans**, **Kundadress** kan du länka de två dokumenten och på så sätt instruera leverantören att leverera direkt till kunden.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Så här skapar du försäljningsorder för direktleveranser
För att förbereda en direktleverans skapar du en försäljningsorder för en artikel som vanligt, förutom att du måste ange på försäljningsraden att försäljningen kräver direktleverans.

1. Skapa en försäljningsorder för en artikel. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
2. På försäljningsorderraden för direktleveransartikeln markerar du kryssrutan **Direktleverans**. Använda funktionen **Välj kolumner** om fältet inte visas. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Så här skapar du inköpsorder för direktleverans
Om du vill förbereda en direktleverans för den artikel som ska säljas kan du skapa en inköpsorder som vanligt förutom att du måste ange på inköpsordern att den ska levereras till din kund och inte till dig själv.

1. Skapa en inköpsorder. Fyll inte i några fält på raderna. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).
2. Välj **Kundadress** i fältet **Leverans**.
3. I fältet **Kund** markerar du kunden som du säljer till.
3. Välj åtgärden **Direktleverans** och välj sedan åtgärden **Hämta förs.order**.
4. På sidan **Försäljningslista** väljer du den försäljningsorder som du förberedde i [Så här skapar du försäljningsorder för direktleveranser](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
5. Välj knappen **OK**.

Radinformationen från försäljningsordern infogas på inköpsorderraden.

Du kan nu instruera leverantören att leverera artiklarna till kunden, till exempel genom att e-posta inköpsordern som en PDF.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Om du vill se den länkade inköpsordern från försäljningsordern
* Markera försäljningsordern direktleverans, välj åtgärden **Order**, välj åtgärden **Direktleverans** och välj sedan åtgärden **Inköpsorder**.

## <a name="to-post-a-drop-shipment"></a>Så här bokför du en direktutleverans
När leverantören har levererat artiklarna kan du bokföra försäljningsordern som levererad. Du kan också bokföra inköpsordern, men endast med alternativet **Ta emot** tills försäljningsordern har fakturerats.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.
2. Öppna den försäljningsorder som du skapade i [Att skapa en försäljningsorder för en direktleverans]() .
3. I fältet **Levereras antal** anger du hur många av orderkvantiteten som ska levereras, hela eller delvis orderkvantitet.
4. Välj åtgärden **Bokför** eller **Bokför och skicka**.
5. Markera antingen alternativet **Leverera** för att fakturera senare eller alternativet **Leverera och fakturera** för att fakturera omedelbart.

## <a name="see-also"></a>Se även
[Skapa specialorder](sales-how-to-create-special-orders.md)  
[Köpa artiklar för en försäljning](purchasing-how-purchase-products-sale.md)  
[Sälja produkter](sales-how-sell-products.md)  
[Registrera inköp](purchasing-how-record-purchases.md)  
[Försäljning](sales-manage-sales.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
