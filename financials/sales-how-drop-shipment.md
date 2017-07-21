---
title: "Skapa en försäljningsorder som är kopplad till en inköpsorder för en direktleverans | Microsoft Docs"
description: "Beskriver hur du skapar en försäljningsorder som är länkad till en inköpsorder för att tillåta leverans direkt från leverantören till kunden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 977debf7386ad1113ef54147b20fd24c7c285a78
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-make-drop-shipments"></a>Så här utför du direktleveranser
Direktleverans innebär leverans av artiklar från någon av företagets leverantörer direkt till någon av företagets kunder.

När en försäljningsorder är markerad för direktleverans, och du skapar en inköpsorder där du anger kunden i fältet **Förs.kundnr.** kan du länka de två dokumenten och därmed instruera leverantören att leverera direkt till kunden.

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Så här skapar du försäljningsorder för direktleveranser
För att förbereda en direktleverans skapar du en försäljningsorder för en artikel som vanligt, förutom att du måste ange på försäljningsraden att försäljningen kräver direktleverans.

1. Skapa en försäljningsorder för en artikel. Mer information finns i [Så här säljer du produkter](sales-how-sell-products.md).
2. På försäljningsorderraden för direktleveransartikeln markerar du kryssrutan **Direktleverans**. Använd funktionen **Välj kolumner** om fältet inte visas. Mer information finns i [Användaranpassning](ui-user-personalization.md).

> [!NOTE]  
>   Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Så här skapar du inköpsorder för direktleverans
Om du vill förbereda en direktleverans för den artikel som ska säljas kan du skapa en inköpsorder som vanligt förutom att du måste ange på inköpsordern att den ska levereras till din kund och inte till dig själv.

1. Skapa en inköpsorder. Fyll inte i några fält på raderna. Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md).
2. I fältet **Förs.kundnr.** markerar du kunden som du säljer till.
3. Välj åtgärden **Direktleverans** och välj sedan åtgärden **Hämta förs.order**.
4. I fönstret **Försäljningslista** väljer du den försäljningsorder som du förberedde i avsnittet "Så här skapar du försäljningsorder för direktleveranser".
5. Välj **OK**.

Radinformationen från försäljningsordern infogas på inköpsorderraden.

Du kan nu instruera leverantören att leverera artiklarna till kunden, till exempel genom att e-posta inköpsordern som en PDF.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Om du vill se den länkade inköpsordern från försäljningsordern
* Markera försäljningsordern direktleverans, välj åtgärden **Order**, välj åtgärden **Direktleverans** och välj sedan åtgärden **Inköpsorder**.

## <a name="to-post-a-drop-shipment"></a>Så här bokför du en direktutleverans
När leverantören har levererat artiklarna kan du bokföra försäljningsordern som levererad. Du kan också bokföra inköpsordern, men endast med alternativet **Ta emot** tills försäljningsordern har fakturerats.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.
2. Öppna den försäljningsorder som du skapade i avsnittet "Att skapa en försäljningsorder för en direktleverans" .
3. I fältet **Levereras antal** anger du hur många av orderkvantiteten som ska levereras, hela eller delvis orderkvantitet.
4. Välj åtgärden **Bokför** eller **Bokför och skicka**.
5. Markera antingen alternativet **Leverera** för att fakturera senare eller alternativet **Leverera och fakturera** för att fakturera omedelbart.

## <a name="see-also"></a>Se även
[Så här säljer du produkter](sales-how-sell-products.md)  
[Så här registrerar du inköp](purchasing-how-record-purchases.md)  
[Försäljning](sales-manage-sales.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

