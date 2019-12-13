---
title: Spärra artiklar för försäljning eller inköp
description: I Business Central kan en artikel markeras som spärrad för försäljning, spärrad för inköp eller spärrad för alla syften.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 12/04/2019
ms.author: sgroespe
ms.openlocfilehash: 0218cf1b4982b9e8c5b5c2817590bc5ebd8f1941
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896067"
---
# <a name="block-items-from-sales-or-purchasing"></a>Spärra artiklar för försäljning eller inköp
Du kan spärra en artikel så att den inte kan registreras på försäljnings- eller inköpsrader eller bokföras i en transaktion.  

I följande tabell visas vad som händer när artiklar spärras.  

|Alternativ|Description|  
|--------------------|------------|  
|**Spärrad för försäljning**|Du kan inte registrera artikeln i ett försäljningsdokument eller en artikeljournal för försäljning.|  
|**Spärrad för inköp**|Du kan inte registrera artikeln i ett inköpsdokument, en artikeljournal för inköp eller i planeringsprocesser för inköp.|  
|**Spärrad**|Du kan inte använda artikeln för någon artikeltransaktion.|  

> [!NOTE]
> Spärrade artiklar kan returneras. Detta innebär att inga av inställningarna ovan gäller när artikeln används för returorder och kreditnotor.

När du använder funktionen **kopiera dokument** för att skapa nya dokument som bygger på befintliga dokument, får du ett meddelande om något av artiklarna på källdokumentraderna är blockerat. De spärrade dokumentraderna tas inte med i det nya dokumentet och ett meddelande visar en översikt över alla dokumentrader som har spärrats i källdokumentet.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Så här spärrar du en artikel så att den inte kan registreras på försäljningsrader  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.  
2.  Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för försäljning**.  

Om du försöker registrera artikeln i ett försäljningsdokument eller på en journalrad visas ett felmeddelande om att artikeln är spärrad.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Så här spärrar du en artikel så att den inte kan registreras på inköpsrader  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.  
2.  Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för inköp**.  

Om du försöker registrera artikeln i ett inköpsdokument eller på en journalrad visas ett felmeddelande om att artikeln är spärrad.

## <a name="to-block-an-item-from-being-posted"></a>Så här spärrar du en artikel så att den inte kan bokföras
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.
2. Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad**.

Om du försöker bokföra någon typ av transaktion för artikeln visas ett felmeddelande om att artikeln är spärrad.

## <a name="see-also"></a>Se även  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
