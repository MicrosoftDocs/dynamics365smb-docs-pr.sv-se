---
title: "Spärra försäljning till kunders artiklar från försäljning eller inköp"
description: "I Business Central kan en artikel markeras som spärrad för försäljning, spärrad för inköp eller spärrad för alla syften."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 268d098318b77cb89a369e8edc14729a44bedae6
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="block-customers"></a>Spärra kunder
Du kan spärra en kund, till exempel på grund av ett insolvensförfarande, så att kunden inte kan läggas till försäljningsdokument, eller så att inga transaktioner kan bokföras för kunden.

Förutom att spärra en kund, kan du ange ingående transaktioner för en kund som spärrade i samband med påminnelser. Mer information finns i [Så här kräver du in utestående saldon](receivables-collect-outstanding-balances.md).   

De olika spärrningsalternativen beskrivs i tabellen nedan.  

|Alternativ|Description|  
|--------------------|------------|  
|**Tomt**|Transaktioner tillåts för den här kunden.|
|**Leverera**|Det går inte att skapa nya order eller nya leveranser för den här kunden. Befintliga leveranser som inte ännu har fakturerats kan faktureras.|  
|**Fakturera**|Det går inte att skapa nya order, nya leveranser eller nya fakturor för den här kunden. Befintliga leveranser som inte ännu har fakturerats kan inte faktureras.|  
|**Allt**|Ingen transaktion tillåts för den här kunden, inklusive betalningar.|  

## <a name="to-block-a-customer"></a>Om du vill spärra en kund  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kunder** och välj sedan relaterad länk.
2. Välj en kund och välj sedan åtgärden **Redigera**.
3. Fyll i fältet **spärrad** med något av alternativen ovan.

## <a name="see-also"></a>Se även  
[Registrera nya kunder](sales-how-register-new-customers.md)  
[Kräva in utestående saldon](receivables-collect-outstanding-balances.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  

