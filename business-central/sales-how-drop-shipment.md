---
title: Göra direktutleveranser
description: Beskriver hur du skapar en försäljningsorder som är länkad till en inköpsorder för att tillåta leverans direkt från leverantören till kunden.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: direct shipment
ms.date: 05/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="make-drop-shipments"></a>Göra direktutleveranser

Direktleverans innebär leverans av artiklar från någon av företagets leverantörer direkt till någon av företagets kunder.

När en försäljningsorder har markerats för direktleverans och du skapar en inköpsorder som anger kunden i fältet **Leverans**, **Kundadress** kan du länka de två dokumenten för att instruera leverantören att leverera direkt till kunden.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Så här skapar du försäljningsorder för direktleveranser

För att förbereda en direktleverans skapar du en försäljningsorder för en artikel och anger på försäljningsraden att försäljningen kräver direktleverans.

1. Skapa en försäljningsorder för en artikel. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
2. På försäljningsorderraden för direktleveransartikeln markerar du kryssrutan **Direktleverans**. Alternativt, i fältet **Inköpskod**, välj en inköpskod som har fältet **Direktleverans** markerat.

> [!TIP]
> Som standard är kryssrutan Direktleverans och fältet INköpskod inte tillgänglig på raderna. Om den inte är det kan du lägga till den genom att anpassa avsnittet av sidan som innehåller raderna. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Så här skapar du inköpsorder för direktleverans

När du förbereder en direktleverans anger du på inköpsordern att den måste levereras till kunden, inte till dig själv.

1. Skapa en inköpsorder. Fyll inte i några fält på raderna. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).
2. Välj **Kundadress** i fältet **Leverans**.
3. I fältet **Kund** markerar du kunden som du säljer till.
4. Välj åtgärden **Direktleverans** och välj sedan åtgärden **Hämta förs.order**.
5. På sidan **Försäljningslista** väljer du den försäljningsorder som du förberedde i [Så här skapar du försäljningsorder för direktleveranser](#to-create-a-sales-order-for-drop-shipment).
6. Välj knappen **OK**.

Radinformationen från försäljningsordern infogas på inköpsorderraden.

Du kan nu be din leverantör att skicka artiklarna direkt till kunden. Du kan till exempel skicka ordern via e-post.

Om din leverantör tillhandahåller ytterligare information, till exempel ett spårningsnummer, kan du lägga till den informationen som en kommentar på en inköpsorderrad. Om du vill lägga till en kommentar på en rad, på fältet **Typ** väljer du **Kommentar** och anger sedan informationen i fältet **Beskrivning**.  

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Så här skapar du flera inköpsorder för direktleveranser

Du kan också använda inköpskalkylarket för att skapa inköpsorder. Fördelen med att använda inköpskalkylarket är att du kan skapa inköpsorder för alla utestående direktleveranser. Det innebär att du inte behöver skapa varje order för sig.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inköpskalkylark** och väljer sedan relaterad länk.
2. Välj åtgärden **Direktleverans** och välj sedan åtgärden **Hämta förs.order**.
3. Om det behövs anger du filterkriterier för de order du vill få och väljer sedan knappen **OK**.
4. Granska inköpsorderraderna och i fältet **Leverantörsnr** väljer du leverantör som levererar erforderliga varor.
5. Välj åtgärden **Utför åtgärdsmeddelande** för att konvertera mottagna rader till en inköpsorder.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Om du vill se den länkade inköpsordern från försäljningsordern

Markera försäljningsordern direktleverans, välj åtgärden **Order**, välj åtgärden **Direktleverans** och välj sedan åtgärden **Inköpsorder**.

## <a name="to-post-a-drop-shipment"></a>Så här bokför du en direktutleverans

När leverantören har levererat artiklarna kan du bokföra försäljningsordern som levererad. Du kan också bokföra inköpsordern, men endast med alternativet **Ta emot** tills försäljningsordern har fakturerats.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
2. Öppna den säljorder som du skapade i [För att skapa en säljorder för dropshipment](#to-create-a-sales-order-for-drop-shipment).
3. I fältet **Levereras antal** anger du hur många av orderkvantiteten som ska levereras, hela eller delvis orderkvantitet.
4. Välj åtgärden **Bokför** eller **Bokför och skicka**.
5. Markera antingen alternativet **Leverera** för att fakturera senare eller alternativet **Leverera och fakturera** för att fakturera omedelbart.

> [!TIP]
> Glöm inte att du måste bokföra inköpsorderfakturan.

## <a name="see-also"></a>Se även

[Skapa specialorder](sales-how-to-create-special-orders.md)  
[Köpa artiklar för en försäljning](purchasing-how-purchase-products-sale.md)  
[Sälja produkter](sales-how-sell-products.md)  
[Registrera inköp](purchasing-how-record-purchases.md)  
[Försäljning](sales-manage-sales.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
