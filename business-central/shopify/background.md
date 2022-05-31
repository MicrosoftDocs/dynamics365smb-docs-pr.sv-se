---
title: Kör uppgifter i bakgrunden
description: Konfigurera synkronisering av data mellan Business Central och Shopify i bakgrunden.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: f353edb4c505fd7b3eb498392abca3ce481b6009
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768166"
---
# <a name="run-tasks-in-the-background"></a>Kör uppgifter i bakgrunden

Det är effektivt att köra vissa uppgifter samtidigt och på ett automatiserat sätt. Du kan utföra sådana uppgifter i bakgrunden och du kan också ange ett schema när du vill att uppgifterna ska köras automatiskt. Om du vill köra uppgifter i bakgrunden stöds två lägen:

- Manuellt utlösta uppgifter schemaläggs direkt via **Jobbkötransaktioner**
- Återkommande uppgifter schemaläggs i **Jobbkötransaktioner**

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Kör uppgifter i bakgrunden för en specifik butik

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange namnet på **Shopify-butiken** och väljer butiksnamnet i listan.
2. Välj den butik som du vill synkronisera artiklar för och öppna sidan **Shopify-butikskort**.
3. Aktivera reglaget **Tillåt synkronisering i bakgrunden**.

När synkroniseringsåtgärden aktiveras, i stället för en uppgift som körs i förgrunden, ombeds du att vänta. När den är klar kan du fortsätta med nästa åtgärd. Uppgiften skapas som **Jobbkötransaktion** och startar direkt på ett icke-blockerande sätt.

## <a name="to-schedule-recurring-tasks"></a>Så här schemalägger du återkommande uppgifter

Du kan schemalägga följande återkommande uppgifter så att de utförs på ett automatiserat sätt. Mer information om schemaläggning av uppgifter finns i [Jobbkö](../admin-job-queues-schedule-tasks.md).

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

## <a name="see-also"></a>Se även

[Kom igång med kopplingen för Shopify](get-started.md)  
