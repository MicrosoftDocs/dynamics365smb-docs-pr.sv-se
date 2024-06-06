---
title: 'SÅ här: Dela Dist.lageraktivitetsrader'
description: Läs om hur du delar upp lageraktivitetsrader om den tillgängliga kapaciteten på en föreslagen lagerplats inte är tillräcklig.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 9314, 9313, 9315, 9330'
---
# <a name="split-warehouse-activity-lines"></a>Dela rader för dist.lageraktivitet

I distributionslagerartikelinförslar, -transporter och -plockningar, samt i lagerartikelinförslar och lagerplockningar, föreslås lagerställen för plockning och införsel av artiklar. det faktiska antalet på den lagerplats som föreslås kanske inte räcker, eller också finns det inte tillräckligt mycket plats på lagerstället för införsel av det aktuella antalet. I så fall kan du dela upp raden, så att artiklarna på en rad tas från, eller placeras på, fler än en lagerplats.  

Följande procedur gäller för följande distributionslagerdokument:

* Distributionslager, artikelinförslar
* Distributionslagerförflyttningar
* Distributionslagerplockningar
* Lager, artikelinförsel
* Lagerförflyttningar
* Lagerplockningar  

## <a name="to-split-warehouse-activity-lines"></a>Att dela Dist.lageraktivitet rader

1. Öppna en lageraktivitetsrad där du försöker manipulera ett otillräckligt antal.  
2. I fältet **Ant. att hantera**, ange det antal som du kan hantera.  
3. På snabbfliken **Rader** väljer du åtgärden **Åtgärder** och väljer sedan åtgärden **Funktioner** och sedan åtgärden **Dela rad**. En ny rad visas. Raden är en kopia av den ursprungliga raden, med den skillnaden att fältet **Ant. att hantera** innehåller det antal som du tog bort från den ursprungliga raden.  
4. Tilldela en lagerplats och zon, om du använder dirigerad artikelinförsel och plockning, en zon, eller fortsätt att dela upp raden efter behov tills du har önskat antal lagerställen för hela kvantiteten.  

> [!NOTE]  
> Om lagerstället är inställt på dirigerad artikelinförsel och plockning, och du delar raderna, måste du vara förtrogen med distributionslagret och kunna välja en lagerplats som passar artikelns lagringskrav och uppfyller de allmänna kraven i distributionslagerdokumentet. Du skulle till exempel inte dela en rad i ett plockningsdokument och placera några artiklar i volymlagret.  

## <a name="see-also"></a>Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
