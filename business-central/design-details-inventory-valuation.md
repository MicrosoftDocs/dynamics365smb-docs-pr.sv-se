---
title: Designdetaljer – Lagervärdering | Microsoft Docs
description: Lagervärdering är beräkningen av kostnaden för en lagerartikel.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
---
# Designdetaljer: Lagervärdering
Lagervärdering är fastställandet av kostnaden som tilldelats en lagerartikel, enligt uttryckt i följande ekvation.  

Slutlager = startlager + nettoinköp – kostnaden för sålda varor  

Beräkningen av lagervärderingen använder fältet **Kost.belopp (aktuellt)** i värdetransaktionerna för artikeln. Transaktionerna klassificeras efter transaktionstypen som motsvarar kostnadskomponenter, direkt kostnad, indirekt kostnad, avvikelse, omvärdering och avrundning. Mer information finns i [Designdetaljer: kostnadskomponenter](design-details-cost-components.md).  

Transaktioner har kopplats mot varandra, antingen av fasta kopplingar eller enligt det allmänna antagandet om kostnadsflöde som definieras av värderingsprincipen. En transaktion med lagerminskning kan kopplas till flera ökningar med olika bokföringsdatum och eventuellt olika anskaffningskostnader. Mer information finns i [Designdetaljer: Artikelkoppling](design-details-item-application.md). Därför baseras beräkningen av lagervärdet för ett givet datum på summan av positiva och negativa värdetransaktioner.  

## Lagervärdering – rapport  
För att beräkna lagervärdet i rapporten **Lagervärdering** börjar rapporten med att beräkna värdet för artikelns lager på ett visst startdatum. Det lägger till värdet av lagerökningar och subtraherar sedan värdet av lagerminskningar upp till ett visst slutdatum. Slutresultatet är lagervärdet på slutdatumet. Rapporten beräknar dessa värden genom att summera värdena i fältet **Kost.belopp (aktuellt)** i värdetransaktionerna, med hjälp av bokföringsdatum som filter.  

I den utskrivna rapporten visas alltid faktiska belopp, d.v.s. kostnaden för transaktioner som har bokförts som fakturerade. Om du markerar fältet Ta med förväntad kostnad på snabbfliken Alternativ visas även den förväntade kostnaden för transaktioner som har bokförts som inlevererade eller utlevererade.  

> [!IMPORTANT]  
>  Värden i den rapporten **Lagervärdering** stäms av med lagerkontot i redovisningen vilket betyder att värdetransaktionerna i fråga har bokförts i redovisningen.  

> [!IMPORTANT]  
>  Beloppen i kolumnerna **Värde** i rapporten baseras på bokföringsdatumet för transaktioner för en artikel.  

## Lagervärdering – PIA-rapport  
Ett produktionsföretag måste bestämma värdet av tre typer av lager:  

* Råmateriallager  
* PIA-lager  
* Färdiga varor i lager  

Värdet i PIA-lagret bestäms av efterföljande ekvation:  

* Avslutande PIA-lager = Start-PIA-lager + produktionskostnader – kostnaden för tillverkade varor  

När det gäller inköpt lager utgör värdetransaktioner grunden för lagervärderingen. Beräkningen görs med hjälp av värdena i fältet **Kost.belopp (aktuellt)** för artikel- och kapacitetvärdetransaktionerna som är kopplade till en produktionsorder.  

Avsikten med PIA-lagervärderingen är att fastställa värdet för artiklarna vars tillverkning ännu inte har slutförts på ett givet datum. Därför baseras PIA-lagervärdet på de värdetransaktioner som är kopplade till förbrukningen och kapacitetstransaktionerna. Förbrukningstransaktioner måste vara helt fakturerade vid datumet för värderingen. Därför visar rapporten **Lagervärdering – PIA** kostnaderna som representerar PIA-lagervärdet i två kategorier: förbrukning och kapacitet.  

## Se även  
[Designdetaljer: Avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md)   
[Designdetaljer: Omvärdering](design-details-revaluation.md)   
[Designdetaljer: Bokföring av produktionsorder](design-details-production-order-posting.md)
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]