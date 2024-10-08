---
title: Spärra leverantörer
description: Läs hur du kan spärra leverantörer från att inkluderas i transaktioner eller bara spärra nya betalningar till dem.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: 27
ms.date: 07/19/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="block-vendors"></a>Spärra leverantörer
Du kan spärra en leverantör, till exempel på grund av insolvens, så att leverantören inte kan läggas till i inköpsdokument eller så att inga betalningar kan bokföras för leverantören.

De olika spärrningsalternativen för leverantörer beskrivs i registeren nedan.  

|Alternativ|Beskrivning|  
|--------------------|------------|  
|**Tomt**|Transaktioner tillåts för den här leverantören.|
|**Betalning**|Det går inte att skapa nya betalningar för den här leverantören.|  
|**Alla**|Inga transaktioner tillåts för den här leverantören.|  

## <a name="to-block-a-vendor"></a>Om du vill spärra en leverantör
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.
2. Välj den leverantör som du vill spärra.
3. I fältet **Spärrade** väljer du ett av spärrningsalternativen.

## <a name="see-also"></a>Se även
[Registrera nya leverantörer](purchasing-how-register-new-vendors.md)  
[Göra betalningar](payables-make-payments.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
