---
title: Spärra artiklar för försäljning eller inköp
description: Du kan förhindra att en artikel används, t.ex. i försäljnings- eller inköpsdokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 467b43b14f1905018c2a26a06c15abc5a0a17e99
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410650"
---
# <a name="block-items-from-sales-or-purchasing"></a>Spärra artiklar för försäljning eller inköp
Du kan spärra en artikel så att den inte kan registreras på rader i försäljnings- eller inköpsdokument, och du kan även spärra den från att publiceras i en transaktion. Detta kan till exempel vara användbart när en artikel har en känd defekt. Om någon väljer en spärrad artikel i ett försäljnings- eller inköpsdokument kommer ett meddelande att informera dem om att artikeln är spärrad.

I följande tabell beskrivs vad som händer när artiklar spärras.  

|Alternativ|Beskrivning|  
|--------------------|------------|  
|**Spärrad för försäljning**|Du kan inte registrera artikeln i ett försäljningsdokument eller en artikeljournal för försäljning.|  
|**Spärrad för inköp**|Du kan inte registrera artikeln i ett inköpsdokument, en artikeljournal för inköp eller i planeringsprocesser för inköp.|  
|**Spärrad**|Du kan inte använda artikeln för någon artikeltransaktion.|  

> [!NOTE]
> Spärrade artiklar kan returneras. Detta innebär att inga av inställningarna ovan gäller när artikeln används för returorder och kreditnotor.

När du använder funktionen **Kopiera från dokument** för att skapa nya dokument som bygger på befintliga dokument får du ett meddelande om något av artiklarna på källdokumentraderna är blockerat. De spärrade dokumentraderna tas inte med i det nya dokumentet och ett meddelande visar en översikt över alla dokumentrader som har spärrats i källdokumentet.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Så här spärrar du en artikel så att den inte kan registreras på försäljningsrader  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.  
2.  Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för försäljning**.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Så här spärrar du en artikel så att den inte kan registreras på inköpsrader  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.  
2.  Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för inköp**.  

## <a name="to-block-an-item-from-being-posted"></a>Så här spärrar du en artikel så att den inte kan bokföras
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan tillhörande länk.
2. Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad**.

## <a name="see-also"></a>Se även  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
