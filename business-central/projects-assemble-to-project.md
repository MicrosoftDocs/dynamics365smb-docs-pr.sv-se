---
title: Montera till projekt
description: Lär dig hur du använder montering mot kundorder för projekt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/03/2022
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Montera till projekt

Med Montera i projekt kan du förbättra lagerhanteringen genom att endast montera på order när det behövs.

När du väljer en montering mot kundorder på order på en projektplaneringsrad [!INCLUDE [prod_short](includes/prod_short.md)] skapas en monteringsorder. Monteringsordern baseras på projektplaneringsraden och dess rader är baserade på artikelns strukturer. Om du vill lära dig mer om monteringsstrukturer går du till [Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md). Antalet komponenter i monteringsstrukturen multipliceras med partistorleken. På sidan **montering mot kundorderrad** visar detaljer om de länkade monteringsorderraderna. Informationen kan hjälpa dig att anpassa monteringsartikeln. Precis som vid försäljning kan du inte bokföra länkade monteringsorder direkt. Mer information om monteringsorder finns i [Sälja lagerartiklar i flöden för montering mot kundorder](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

Monteringsorder är reserverade för projekt och [!INCLUDE [prod_short](includes/prod_short.md)] synkroniserar artikelspårning mellan projektplaneringsrader och monteringsorder.

## Integrera med hantering av lager

Assemble to project integreras med lagerhanteringsfunktioner för att göra montering och leverans enklare. Processen bidrar också till att säkerställa att flödet från projektmontering till leverans löper smidigt i interna lagerprocesser. Mer information om interna distributionslagerflöden för projekt finns i [Flöden för produktion, montering och projekt](design-details-internal-warehouse-flows.md#flows-to-and-from-assembly-in-a-basic-warehouse-configuration).

I följande tabell beskrivs de lagerkonfigurationer som monteras till orderstöd.

|Konfiguration  |Description  |
|---------|---------|
|**Ingen distributionslagerhantering**|Använda en projektjournal för att bokföra fullständig eller partiell användning. Utdata och förbrukning av komponenter bokförs automatiskt för monteringsordern.         |
|**Lagerplockning**|Använd ett lagerval för att lägga upp hel eller partiell användning. Utdata och förbrukning av komponenter bokförs automatiskt för monteringsordern.          |
|**Dist.lager plockning**|Skapa och registrera lagerplockningar för komponenter och sedan använda en projektjournal för att bokföra förbrukning. [!INCLUDE [prod_short](includes/prod_short.md)] kontrollerar om de förbrukade monteringskomponenterna har plockats. Utdata och förbrukning av komponenter bokförs automatiskt för monteringsordern.         |

## Kända begränsningar

I det här avsnittet beskrivs kända begränsningar för montering till projekt.

* Fältet **Antal att montera i order** är inte tillgängligt för stängda projekt.
* För lagerplockningsscenarier kan antalet som ska **Antal att montera i order** kan vara antingen noll eller lika med kvantiteten. Du kan inte blanda, montera på beställning och montera i lager på en projektplaneringsrad. Du måste skapa separata projektplaneringsrader.
* Montering mot kundorder påverkar inte fakturerbara delar av ett projekt. En sammansättning ingår i försäljningsfakturor, men inte i dess komponenter. Du kan inte redigera fältet **Antal att montering mot kundorder** för fakturerbara rader.
* Orderplaneringen och planeringsförslaget påverkas inte eftersom projektet utgör indata för planeringen. Planeringsmotorn betraktar monteringen som behov.
* Du kan inte ange ett negativt antal i fältet **Antal att montera mot kundorder**.
* Du kan inte ångra en montering.

## Se även

[Projekthantering](projects-manage-projects.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Skapa projekt](projects-how-create-jobs.md)
