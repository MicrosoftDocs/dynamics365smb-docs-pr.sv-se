---
title: Så här skapar du Serviceofferter | Microsoft Docs
description: Du kan använda sidan **Serviceoffert** för att skapa dokument där du anger information om service, som reparation och underhåll, på serviceartiklar efter kundkrav. Du kan använda en serviceoffert som preliminärt utkast för en serviceorder och sedan omvandla offerten till en serviceorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 92c93b2e0b876920f1c259d31b4d839a5b2ecbc0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388805"
---
# <a name="create-service-quotes"></a>Skapa tjänsteofferter
Du kan se serviceofferter som grund för serviceorder. De är i själva verket nästan identiska. De innehåller båda information som till exempel vem kunden är, typ av order, artikeln som behöver service, fakturering- och leveransinformation och information om det faktiska servicearbetet.
 
Du kan använda en serviceoffert som preliminärt utkast för en serviceorder och sedan omvandla offerten till en serviceorder.  
  
## <a name="to-create-a-service-quote"></a>Så här skapar du serviceofferter  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **serviceofferter** och välj sedan relaterad länk.  
2. Skapa en ny serviceoffert.  
3. I fältet **Nr.** anger du ett nummer för serviceofferten. Om du har angett nummerserier för serviceofferter på sidan **Serviceinställningar** kan du trycka på Retur, så väljs nästa tillgängliga serviceoffertnummer.  
4. I fältet **Kundnr.**  välj relevant kund i listan.  

  > [!Note]  
  >  Kundfälten fylls i automatiskt med information från kortet **Kund**. Om kortet **Kund** inte finns för kunden, och du har lagt upp en kundmall, kan du skapa kunden från serviceofferten. Fyll i relevanta fält och välj sedan åtgärden **Skapa kund**.  
  
5. Beroende på inställningarna på snabbfliken **Obligatoriska fält** om ska finnas på sidan **Serviceinställningar** kanske du måste fylla i fältet **Tjänsteordertyp** på fältet **Säljarkod**.  
6. Fyll i serviceartikelraderna.  
7. Registrera uppskattade kostnader på serviceraderna.  
  
## <a name="see-also"></a>Se även  
[Skapa tjänsteorder](service-how-to-create-service-orders.md)  
[Arbeta med tjänsteuppgifter](service-how-to-work-on-service-tasks.md)  

 

[!INCLUDE[footer-include](includes/footer-banner.md)]