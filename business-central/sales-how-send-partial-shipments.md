---
title: Bearbeta delleveranser
description: Försäljningsorderns leveranser kan behandlas i Business Central med del leveranser med hjälp av fälten Leveransråd och Ant. att utleverera.
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'shipping advice, partial shipments, partial deliveries, trade, customer sales order'
ms.date: 02/14/2024
ms.author: bholtorf
---
# Bearbeta delleveranser

I en del leverans, levereras ingen order på samma gång. Av en order på exempelvis 100 enheter levereras 40 enheter omedelbart och 60 vid senare tillfälle. Det finns ingen begränsning av antalet utleveranser som kan utföras för en order.

Innan du kan använda del leveranser i [!INCLUDE [prod_short](includes/prod_short.md)] måste du dock ange att kunden ska acceptera del leveranser genom att ställa in fältet **leveransråd** på sidan **kundkort**. Om kunden bara godtar fullständiga leveranser men sedan begär eller accepterar en del leverans för en viss försäljningsorder, kan du ändra fältet **leveransråd** innan du bokför.

Som standard [!INCLUDE [prod_short](includes/prod_short.md)] anges fältet på sidan **kundkort** som **delvis**, vilket tillåter del leveranser. Om fältet däremot anges för att specificera **avsluta**, sedan blockeras fältet **Ant. att utleverera** är blockerat i försäljningsorder för den kunden.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## Se även

[Sälja produkter med en kundförsäljningsreturorder](sales-how-sell-products.md)  
[Leverera artiklar](warehouse-how-ship-items.md)  
[Skapa direktleveranser](sales-how-drop-shipment.md)  
[Försäljning](sales-manage-sales.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
