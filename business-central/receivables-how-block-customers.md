---
title: Så här spärrar du försäljning till kunder
description: Om det behövs kan du spärra en kund från att ingå i försäljningsdokument och andra försäljningstransaktioner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1caf2fb0586cf704e5fc1354b3b4a0be096dc709
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781744"
---
# <a name="block-customers"></a>Spärra kunder
Du kan spärra en kund, till exempel på grund av ett insolvensförfarande, så att kunden inte kan läggas till försäljningsdokument, eller så att inga transaktioner kan bokföras för kunden.

Förutom att spärra en kund, kan du ange ingående transaktioner för en kund som spärrade i samband med påminnelser. Mer information finns i [Så här kräver du in utestående saldon](receivables-collect-outstanding-balances.md).   

Följande tabell anger alternativen för att spärra kunder.  

|Alternativ|Beskrivning|  
|--------------------|------------|  
|**Tomt**|Transaktioner tillåts för den här kunden.|
|**Leverera**|Det går inte att skapa nya order eller nya leveranser för den här kunden. Befintliga leveranser som inte ännu har fakturerats kan faktureras.|  
|**Fakturera**|Det går inte att skapa nya order, nya leveranser eller nya fakturor för den här kunden. Befintliga leveranser som inte ännu har fakturerats kan inte faktureras. Du kan fortfarande skicka påminnelser och räntefakturor till kunden.|  
|**Alla**|Ingen transaktion tillåts för den här kunden, inklusive betalningar.|  

## <a name="to-block-a-customer"></a>Om du vill spärra en kund  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Välj en kund och välj sedan åtgärden **Redigera**.
3. I fältet **Spärrad** anger du vad som ska blockeras i enlighet med beskrivningen i tabellen ovan.

## <a name="see-also"></a>Se även  
[Registrera nya kunder](sales-how-register-new-customers.md)  
[Kräva in utestående saldon](receivables-collect-outstanding-balances.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]