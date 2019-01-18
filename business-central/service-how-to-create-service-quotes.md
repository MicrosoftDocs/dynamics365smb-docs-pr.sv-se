---
title: "Så här skapar du Serviceofferter | Microsoft Docs"
description: "Du kan använda sidan **Serviceoffert** för att skapa dokument där du anger information om service, som reparation och underhåll, på serviceartiklar efter kundkrav. Du kan använda en serviceoffert som preliminärt utkast för en serviceorder och sedan omvandla offerten till en serviceorder."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 1486be71b0b848aa48996f4161f8987322a09e32
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="create-service-quotes"></a>Skapa tjänsteofferter
Du kan se serviceofferter som grund för serviceorder. De är i själva verket nästan identiska. De innehåller båda information som till exempel vem kunden är, typ av order, artikeln som behöver service, fakturering- och leveransinformation och information om det faktiska servicearbetet.
 
Du kan använda en serviceoffert som preliminärt utkast för en serviceorder och sedan omvandla offerten till en serviceorder.  
  
## <a name="to-create-a-service-quote"></a>Så här skapar du serviceofferter  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Serviceofferter** och välj sedan relaterad länk.  
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

 
