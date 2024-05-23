---
title: Ställa in i processer för servicehantering
description: Lär dig hur du ställer in processer som hjälper dig att se till att kunden är nöjd med din tjänster.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'service, number sequences, setup, warnings, fee, contracts, warranties'
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Konfigurera processer för tjänstehantering

Här följer några exempel på de inställningar som du kan använda i tjänstehanteringsprocesser:  
  
* En del allmänna inställningar för olika processer, till exempel varningar, nästa serviceberäkningar för serviceartiklar, bedöma uppstartskostnader, felrapporteringsnivån och så vidare.  
* Typerna av information som en tekniker anger på servicedokument. Du kan till exempel kräva att de anger vilken typ av order, start och/eller slutdatum för arbete och vilken typ av arbete som har utförts.  
* Vissa standardinställningar för svarstider och garantier. Dessa omfattar en standardsvarstiden för att starta tjänsten, rabattsatser för garanti för reservdelar och arbete och hur länge garantierna gäller.  
* Inställningar för kontrakt, till exempel det maximala antalet dagar som du kan använda för serviceorder om du använder orsakskoder när ett kontrakt har annullerats, standardtexter beskrivningar av kontraktvärden.  
* Nummerserierna som ska användas för servicerelaterade dokument och artiklar.  

## Så här anger du allmänna och obligatoriska inställningar

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfigurera servicehantering** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Konfigurera bokföringsprinciper för servicefakturor för användare

Företag har ofta unika processer för att bokföra försäljnings- och inköpsfakturor och leveranser. Processer kan till exempel variera från en person som bokför allt på en på en serviceorder till flera anställda, som var och en arbetar med sina egna sidor.

Du kan använda bokföringsprinciper för att hindra användare från att bokföra servicefakturor eller kräva att de bokför fakturor tillsammans med den relaterade serviceleveransen. För att ställa in en inläggspolicy, på sidan **Användarinställningar** i fältet **Bokföringsprincip för servicefaktura** välj ett av följande alternativ:

* **Tillåten** (standard): Behåll det nuvarande beteendet, där du kan välja vilket inläggsalternativ som ska användas, som t.ex. **leverera**, **faktura** och **leverera och fakturera**.
* **Förbjuden**: hindrar användaren från att bokföra servicefakturor. [!INCLUDE [prod_short](includes/prod_short.md)] visar en bekräftelsedialogruta som endast innehåller alternativet **Leverera**.
* **Obligatoriskt**: Låt personer bokföra fakturor tillsammans med serviceleveranser. [!INCLUDE [prod_short](includes/prod_short.md)] visar en bekräftelsedialogruta som endast innehåller alternativet **Leverera och fakturera**.

Den här inställningen påverkar följande dokument:

* Serviceorder
* Utleveranser från distributionslager
* Servicefakturor
* Servicekreditnotor

Följande tabell beskriver effekterna på olika dokument.

|Dokument  |Tillåt<br>Visar en serie alternativ   |Förbjudet<br>Bekräftelsedialogruta  |Obligatoriskt<br>Bekräftelsedialogruta  |
|---------|---------|---------|---------|
|Tjänsteorder     | * Leverera<br>* Fakturera<br>* Leverera och fakturera<br>* Leverera och förbruka         |* Leverera<br>* Leverera och förbruka  |Vill du bokföra utleveransen och fakturan?         |
|Dist.lager utleverans     |* Leverera<br>* Leverera och fakturera         |Vill du bokföra utleveranserna?         | Vill du bokföra utleveransen och fakturan?        |
|Servicefaktura     | Vill du bokföra fakturan?         | Fel: du kan inte bokföra.       |Vill du bokföra fakturan?         |
|Servicekreditnota     | Vill du bokföra kreditnotan?         | Fel: du kan inte bokföra.        |Vill du bokföra kreditnotan?         |

> [!NOTE]
> När du bokför servicefakturor och kreditnotor har du inga bokföringsalternativ. I dokumenten bokförs alltid de fysiska och ekonomiska transaktionerna tillsammans. Du kan inte delvis bokföra servicefakturor och kreditnotor.

## Se även  

[Konfigurera felrapportering](service-how-setup-fault-reporting.md)  
[Konfigurera resursfördelning](service-how-setup-resource-allocation.md)  
[Skapa koder för standardtjänster](service-how-setup-service-coding.md)  
[Registrera alternativa kostnader för tjänster](service-how-setup-service-costs-pricing.md)  
[Ställa in felsökning](service-how-setup-troubleshooting.md)  
[Servicehantering](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
