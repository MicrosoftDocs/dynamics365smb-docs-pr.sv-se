---
title: Kör aktiviteter i bakgrunden och samtidigt
description: Konfigurera synkronisering av data mellan Business Central och Shopify i bakgrunden.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 4a67f6fc58fb8b158563ce58baab55e7fda2ccb1
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728606"
---
# <a name="run-tasks-in-the-background"></a>Kör uppgifter i bakgrunden

Det är effektivt att köra vissa uppgifter samtidigt och på ett automatiserat sätt. Du kan utföra sådana uppgifter i bakgrunden och du kan också ange ett schema när du vill att uppgifterna ska köras automatiskt. Om du vill köra uppgifter i bakgrunden stöds två lägen:

- Manuellt utlösta uppgifter schemaläggs direkt via **Jobbkötransaktioner**.
- Återkommande uppgifter schemaläggs i **Jobbkötransaktioner**.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Kör uppgifter i bakgrunden för en specifik butik

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange namnet på **Shopify-butiken** och väljer butiksnamnet i listan.
2. Välj den butik som du vill synkronisera artiklar för och öppna sidan **Shopify-butikskort**.
3. Aktivera reglaget **Tillåt synkronisering i bakgrunden**.

När synkroniseringsåtgärden aktiveras, i stället för en uppgift som körs i förgrunden, ombeds du att vänta. När den är klar kan du fortsätta med nästa åtgärd. Uppgiften skapas som **Jobbkötransaktion** och startar direkt på ett icke-blockerande sätt.

## <a name="to-schedule-recurring-tasks"></a>Så här schemalägger du återkommande uppgifter

Du kan schemalägga följande återkommande uppgifter så att de utförs på ett automatiserat sätt. Läs mer om schemaläggning av uppgifter på [jobbkö](../admin-job-queues-schedule-tasks.md).

|Uppgift|Objekt|
|------|------------|
|**Synkronisera order från Shopify**|Rapport 30104 Synkronisera order från Shopify|
|**Behandla Shopify-order**|Rapport 30103 Shopify skapa försäljningsorder|
|**Synkronisera utleveranser till Shopify**|Rapport 30109 Synkronisera utleverans till Shopify|
|**Synkronisera produkter och/eller priser**|Rapport 30108 Shopify Synkronisera produkter|
|**Synka lager**|Rapport 30102 Synkronisera lager till Shopify|
|**Synkronisera bilder**|Rapport 30107 Shopify Synkronisera bilder|
|**Synka kunder**|Rapport 30100 Shopify Synkronisera kunder|
|**Synkronisera betalningar**|Rapport 30105 Shopify Synkronisera betalningar|

> [!NOTE]
> Vissa element kan uppdateras av flera uppgifter, till exempel när du importerar beställningar, beroende på inställningen i **Shopify butikskort**, kan systemet också importera och uppdatera kund- och/eller produktdata. Kom ihåg att använda samma jobbkö för att undvika konflikter.

## <a name="see-also"></a>Se även

[Kom igång med kopplingen för Shopify](get-started.md)  
