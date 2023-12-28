---
title: 'Designdetaljer – Flöden för produktion, montering och projekt'
description: 'Läs om flödet mellan lagerplatser i plockkomponenter och föra in slutartiklar för montering, produktion eller projektorder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
---
# Flöden för produktion, montering och projekt

Interna flöden, som plockningskomponenter och föra in slutartiklar för montering, projekt och produktionsorder liknar ankommande eller avgående flöden. På så sätt kan många av processerna se bekant. I den här artikeln finns information om hur du arbetar med interna distributionslagerflöden med olika komplexitetsnivåer.

## Översikt över olika konfigurationsalternativ

Du kan konfigurera distributionslagerfunktioner på olika sätt. Det är viktigt att du väljer en förbättring av dina processer utan att orsaka omkostnader. I följande tabeller beskrivs typiska konfigurationer för hantering av fysiska varor för produktion, projekt och monteringsorder.

### Ankommande flöde (artikelinförsel)

|Komplexitetsnivå|Beskrivning|Inställningar|Lagerställeskod|Ankommande flöde av produktionsorder|Ankommande flöde av monteringsorder|Ankommande flöde av projekt|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen tilldelad distributionslageraktivitet.|Bokför från order och journaler.||Valfritt. Kontrolleras av växlingsknappen **Lagerställeskod är obligatorisk**.|Produktionsjournal -> utflödesjournal</br><br/> **OBS**! Du kan bokföra utflöde med **produktionsjournal**.|Monteringsorder|Artikelinförsel gäller inte för projekt|  
|Grundläggande|Order för order.|Begär artikelinförsel. </br><br/> **OBS**! Även om inställningarna kallas **Begär plockning**, kan du fortfarande bokföra inleveranser och utleveranser direkt från affärskälldokument på platser där du markerar dessa kryssrutor. |Valfritt. Kontrolleras av växlingsknappen **Lagerställeskod är obligatorisk**.|Produktionsorder -> Lager, artikelinförsel|Monteringsorder|Artikelinförsel gäller inte för projekt|
|Avancerat|Konsoliderade aktiviteter för artikelnförsel för flera källdokument.|Kräver inleverans + Kräver artikelinförsel|Valfritt. Kontrolleras av växlingsknappen **Lagerställeskod är obligatorisk**.|Produktionsorder -> utflödesjournal|Monteringsorder -> internförflyttning | Artikelinförsel gäller inte för projekt|
|Avancerat|Samma som ovan + Dirigerad art.inf. och plock. aktiviteter|Dirigerad art.inf. och plock. (beroende växlingar aktiveras automatiskt)|Obligatoriskt|Samma som ovan.|Samma som ovan.| Artikelinförsel gäller inte för projekt|

Vissa konfigurationer tillåter inte att dedikerade distributionslagerdokument används för att registrera artikelinförslar. Om lagerstället använder lagerplatser kan du dock använda allmänna transportdokument för att flytta producerade eller monterade artiklar till lagerstället. Läs mer på [Flytta artiklar internt i grundläggande distributionslagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### Avgående flöde (plockning)

|Komplexitetsnivå|Beskrivning|Inställningar|Lagerställeskod|Avgående flöde av produktionsorder|Avgående flöde av monteringsorder|Avgående flöde av projekt|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen tilldelad distributionslageraktivitet.|Bokför från order och journaler.||Valfritt. Kontrolleras av växlingsknappen **Lagerställeskod är obligatorisk**.|Produktionsjournal -> förbrukningsjournal </br><br/> **OBS**! Du kan bokföra förbrukning med **produktionsjournal**.|Monteringsorder|Projekt -> Projektjournal|  
|Grundläggande|Order för order.|Begär plockning. </br><br/> **OBS**! Även om inställningarna kallas **Begär plockning**, kan du fortfarande bokföra utflöde direkt från affärskälldokument på platser där du markerar dessa kryssrutor. <!-- ToDo Test prod output-->|Valfritt. Kontrolleras av växlingsknappen **Lagerställeskod är obligatorisk**.|Produktionsorder -> Lagerplockning|Monteringsorder -> lagerförflyttning</br><br/>**Lagerförflyttningen** kan bara användas med lagerplatser.|Projekt -> Lagerplockning|
|Avancerat|Konsoliderade plockningsaktiviteter för flera källdokument.|Begär utleverans + begär plockning|Valfritt. Kontrolleras av växlingsknappen Lagerställeskod är obligatorisk|Produktionsorder -> Plockningskalkylark -> Förbrukningsjournal |Monteringsorder -> Distributionslagerplockning| Projekt -> Distributionslagerplockning -> Projektjournal |
|Avancerat|Samma som ovan + Dirigerad art.inf. och plock. aktiviteter|Dirigerad art.inf. och plock. (beroende växlingar aktiveras automatiskt)|Obligatoriskt|Samma som ovan.|Samma som ovan.| Dirigerad plockning och artikelinförsel stöds inte för projekt|

Liknande ankommande flöden tillåter vissa konfigurationer inte att dedikerade distributionslagerdokument används för att registrera artikelinförslar. Om lagerplatsen kan du dock använda allmänna transportdokument för att flytta producerade eller monterade artiklar. Läs mer på [Flytta artiklar](warehouse-move-items.md).

## Distributionslager utan särskild distributionslageraktivitet

Även om du inte har särskilda distributionslageraktiviteter vill du förmodligen fortfarande hålla reda på saker som förbrukning och produktionsutflöde. I följande artiklar finns information om hur du behandlar inleveranser för källdokument.

* [Så här registrerar du förbrukning och utflöde för en utsläppt produktionsorderrad](production-how-to-register-consumption-and-output.md)
* [Montera Artiklar](assembly-how-to-assemble-items.md)
* [Registrera förbrukning eller användning för projekt](projects-how-record-job-usage.md)

## Grundläggande distributionslagerkonfiguration

De inkommande och utgående flödena i en grundläggande distributionslagerkonfiguration omfattar följande inställningar på sidan **Lagerställekort**:

* För ingående flöde (artikelinförsel) aktiverar du växlingsknappen **Begär artikelinförsel** men inaktiverar växlingsknappen **Begär inleverans**.
* För ingående flöde (artikelinförsel) aktiverar du växlingsknappen **Begär artikelinförsel** men inaktiverar växlingsknappen **Begär inleverans**.

### Flöden till och från produktion i en grundläggande lagerkonfiguration  

Använd dokumentet **Lagerplockning** för att plocka produktionskomponenter i flödet till produktion. För att föra in de produkter du tillverkar, använd dokumentet **Lagerinförsel**.

För lagerställen som använder lagerplatser är lagerförflyttningsdokument särskilt användbara vid komponentbokföring. För att lära dig mer om hur komponentförbrukningen bokförs från till-produktion eller öppen produktionslagerplats, gå till [Bokföring av produktionskomponenter i distributionslager](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Lagerförflyttningar är viktiga dokument om du använder med bokföringsmetoderna **Plocka + framåt** eller **plocka + bakåt**. Läs mer [bokföringsmetoder](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Fälten **Till prod.-lagerplats – kod**, **Från prod.lagerplats – kod** och **Öppen prod.lagerplats kod** på lagerställekortet eller maskin-/produktionsgruppkorten definierar standardflöden till och från produktionsområden.
* Hantera transport av producerade artiklar på sidan **internförflyttning** utan en relation till en produktionsorder.

### Flöden till och från montering i en grundläggande lagerkonfiguration  

Bokföra monteringsutflöde och förbrukning direkt från en monteringsorder.

> [!NOTE]
> **Lagerplockning** och **Lagerinförsel** dokument stöds inte för monteringsorder.

För lagerställen som använder lagerplatser:

* Använd dokument **lagerförflyttning** för att flytta monteringskomponenter till monteringsområdet.
* Fältet **Till monteringsplats – kod** och **Från monteringsplats – kod** på lagerställekortet definierar standardflöden till och från monteringsområden.
* Hantera transport av monterade artiklar på sidan **internförflyttning** utan en relation till en monteringsorder.

[!INCLUDE [prod_short](includes/prod_short.md)] stöder monteringsflöden montering mot lager och montering mot kundorder. Läs mer på [Förstå montering mot kundorder och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock) I samband med Warehouse Management är montering mot lager en del av det interna distributionslagerflödet och montering mot kundorder finns i det avgående lagerflödet. Mer information finns på [Hantering av artikel för montering mot kundorder i lagerplockningar](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### Flöden för projekthantering i en grundläggande lagerkonfiguration

Använd dokumentet **Lagerplockning** för att plocka projektkomponenter i flödet till projekthantering.

För ett lagerställe som använder lagerplatser definierar fältet **Lagerplatskod för projekt** på lager stället standardflödena till projekthanteringen.

## Avancerad distributionslagerkonfiguration  

De inkommande och utgående flödena i en grundläggande distributionslagerkonfiguration omfattar följande inställningar på sidan **Lagerställekort**:

* För ingående flöde (artikelinförsel) aktiverar du växlingsknappen **Begär artikelinförsel** och växlingsknappen **Begär inleverans**.
* För ingående flöde (artikelinförsel) aktiverar du växlingsknappen **Begär artikelinförsel** och **Begär inleverans**.

### Flöden till och från produktion i en avancerad lagerkonfiguration

Använd dokumenten **Distributionslagerplockning** och sidan **Plockningsförslag** för att plocka komponenter för produktion.

För lagerställen som använder lagerplatser:

* **Warehouse Movement** dokument och sidan **Transportkalkylark** är särskilt användbara vid komponentbokföring. Läs mer på [Bokföring av produktionskomponenter i distributionslagret](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* Fälten **Till prod.-lagerplats – kod**, **Från prod.lagerplats – kod** och **Öppen prod.lagerplats kod** på lagerställekortet eller maskin-/produktionsgruppkorten definierar standardflöden till och från produktionsområden. 
* Hantera transport av producerade artiklar på sidan **Transportkalkylark** eller **Dist.lager intern art.införsel** utan en relation till en produktionsorder.

### Flöden till och från montering i en avancerad lagerkonfiguration

Använd dokumenten **Distributionslagerplockning** och sidan **Plockningsförslag** för att plocka komponenter för montering.

För lagerställen som använder lagerplatser:

* Fältet **Till monteringsplats – kod** och **Från monteringsplats – kod** på lagerställekortet definierar standardflöden till och från monteringsområden.
* Hantera transport av monteringsartiklar på sidan **Transportkalkylark** eller **Dist.lager intern art.införsel** utan en relation till en monteringsorder.

[!INCLUDE [prod_short](includes/prod_short.md)] stöder monteringsflöden montering mot lager och montering mot kundorder. Läs mer på [Förstå montering mot kundorder och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock) 

Montering mot lager en del av det interna distributionslagerflödet och montering mot kundorder finns i det avgående lagerflödet. Läs mer på [Hantera artiklar för montering mot kundorder i distributionslagerutleveranser](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### Flöden för projekthantering i en avancerad lagerkonfiguration

Använd dokumenten **Distributionslagerplockning** och sidan **Plockningsförslag** för att plocka komponenter i flödet för projekthantering.

För ett lagerställe som använder lagerplatser definierar fältet **Lagerplatskod för projekt** på lagerstället standardflödena till projektområdet.

## Se även  

[Warehouse Management – översikt](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
