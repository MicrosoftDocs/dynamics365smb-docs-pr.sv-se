---
title: Spärra artiklar för försäljning eller inköp
description: Du kan spärra en artikel så att den inte kan registreras på rader i försäljnings- eller inköpsdokument, och du kan även spärra den från att publiceras i en transaktion.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/03/2022
ms.author: bholtorf
ms.openlocfilehash: 0783cc97233e40aacb4d9222dceea006a4cf8a59
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744849"
---
# <a name="block-items-from-sales-or-purchasing"></a>Spärra artiklar för försäljning eller inköp

Du kan spärra en artikel så att den inte kan registreras på rader i försäljnings- eller inköpsdokument, och du kan även spärra den från att publiceras i en transaktion. Detta kan till exempel vara användbart när en artikel har en känd defekt. Om någon väljer en spärrad artikel i ett försäljnings- eller inköpsdokument kommer ett meddelande att informera dem om att artikeln är spärrad.

I följande tabell beskrivs vad som händer när artiklar spärras.  

|Alternativ|Description|  
|--------------------|------------|  
|**Spärrad för försäljning**|Du kan inte registrera artikeln i ett försäljningsdokument eller en artikeljournal för försäljning.|  
|**Spärrad för inköp**|Du kan inte registrera artikeln i ett inköpsdokument, en artikeljournal för inköp eller i planeringsprocesser för inköp.|  
|**Spärrad**|Det går inte att inkludera artikeln i transaktioner.|  

> [!NOTE]
> Spärrade artiklar kan returneras. Detta innebär att inga av inställningarna ovan gäller för returorder och kreditnotor.

När du använder åtgärden **Kopiera från dokument** för att skapa nya dokument som bygger på befintliga dokument får du ett meddelande om något av artiklarna på källdokumentraderna är blockerat. De spärrade dokumentraderna tas inte med i det nya dokumentet och ett meddelande visar en översikt över alla dokumentrader som har spärrats i källdokumentet.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Så här spärrar du en artikel så att den inte kan registreras på försäljningsrader  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2. Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för försäljning**.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Så här spärrar du en artikel så att den inte kan registreras på inköpsrader  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2. Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad för inköp**.  

## <a name="to-block-an-item-from-being-posted"></a>Så här spärrar du en artikel så att den inte kan bokföras

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Välj den artikel som du vill spärra och markera sedan kryssrutan **Spärrad**.

## <a name="see-also"></a>Se även  

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]