---
title: Så här spärrar du försäljning till kunder
description: Om det behövs kan du spärra en kund från att ingå i försäljningsdokument och andra försäljningstransaktioner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dc8014cf0896db1ebbc5f0c5ea22e0f160c1b06d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926553"
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
