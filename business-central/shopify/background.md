---
title: Kör aktiviteter i bakgrunden och samtidigt
description: Konfigurera synkronisering av data mellan Business Central och Shopify i bakgrunden.
ms.date: 03/26/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# <a name="run-tasks-in-the-background"></a>Köra uppgifter i bakgrunden

Det är effektivt att köra vissa uppgifter samtidigt och på ett automatiserat sätt. Du kan utföra sådana uppgifter i bakgrunden och du kan också ange ett schema när du vill att uppgifterna ska köras automatiskt. Om du vill köra uppgifter i bakgrunden stöds två lägen:

- Manuellt utlösta uppgifter schemaläggs direkt via **Jobbkötransaktioner**.
- Återkommande uppgifter schemaläggs i **Jobbkötransaktioner**.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Kör uppgifter i bakgrunden för en specifik butik

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-butik** och välj relaterad länk.
2. Välj den butik som du vill köra synkronisering i bakgrunden för och öppna sidan **Shopify-butikskort**.
3. Aktivera reglaget **Tillåt synkronisering i bakgrunden**.

När synkroniseringsåtgärden startar, i stället för att köra en uppgift i förgrunden, ombeds du att vänta. När den är klar kan du fortsätta med nästa åtgärd. Uppgiften skapas som **Jobbkötransaktion** och startar direkt.

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
|**Synkronisera företag**|Rapport 30114 Shopify synkronisera företag (B2B)|
|**Synkronisera betalningar**|Rapport 30105 Shopify Synkronisera betalningar|
|**Synkronisera kataloger**|Rapport 30115 Shopify synkronisera kataloger (B2B)|
|**Synkronisera katalogpriser**|Rapport 30116 Shopify synkronisera katalogpriser (B2B)|

> [!NOTE]
> Vissa element kan uppdateras med flera uppgifter. Till exempel när du importerar beställningar, beroende på inställningen i **Shopify butikskort**, kan systemet också importera och uppdatera kund- och/eller produktdata. Kom ihåg att använda samma jobbkö för att undvika konflikter.

Andra uppgifter som kan vara till hjälp för att automatisera ytterligare behandling av försäljningsdokument:

- Rapport 297 Masspublicera försäljningsfakturor
- Rapport 296 Masspublicera försäljningsordrar

Du kan använda **Shopify ordernr.** för att identifiera försäljningsdokument som har importerats från Shopify.

Om du vill lära dig mer om hur du bokför försäljningsorder i en batch går du till [Skapa en jobbkötransaktion för batchbokföring av försäljningsorder](../ui-batch-posting.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

## <a name="to-check-the-status-of-synchronization"></a>Att kontrollera status för synkronisering

I rollcenter **Chef** erbjuder **Shopify aktiviteter** part offers flera ledtrådar som kan hjälpa dig att snabbt identifiera om det finns problem med Shopify anslutningsprogram.

- **Omappad kund**: Shopify-kund importeras, men länkas inte till en motsvarande kundpost i [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Omappade produkter** – Shopify-produkt importeras, men länkas inte till en motsvarande artikelpost i [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Obearbetade order**: Shopify-order importeras, men försäljningsdokument i [!INCLUDE [prod_short](../includes/prod_short.md)] skapades inte, ofta på grund av omappade produkter eller kunder.
- **Obearbetade leveranser**: Bokförda försäljningsutleveranser som kommer från Shopify-order synkroniseras inte med Shopify.
- **Leveransfel**: Shopify-anslutningsprogram kunde inte synkronisera bokförda försäljningsutleveranser med Shopify.
- **Synkroniseringsfel**: Det finns misslyckade jobbkötransaktioner relaterade till synkronisering med Shopify.

## <a name="see-also"></a>Se även

[Komma i gång med Shopify-anslutningsprogrammet](get-started.md)  
