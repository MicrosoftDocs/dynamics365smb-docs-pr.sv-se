---
title: "Designdetaljer - Lagervärdering | Microsoft Docs"
description: "Lagervärdering XE är fastställandet av kostnaden som tilldelats en lagerartikel, som uttryckt i följande ekvation."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1e2f307a4309389b09e5ce291cb5eca3abee6b88
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-inventory-valuation"></a>Designdetaljer: Lagervärdering
Lagervärdering XE är fastställandet av kostnaden som tilldelats en lagerartikel, som uttryckt i följande ekvation.  

Slutlager = startlager + nettoinköp – kostnaden för sålda varor  

Beräkningen av lagervärderingen använder fältet **Kost.belopp (aktuellt)** i värdetransaktionerna för artikeln. Transaktionerna klassificeras efter transaktionstypen XE "transaktionstyp" som motsvarar kostnadskomponenter, direkt kostnad, indirekt kostnad, avvikelse, omvärdering och avrundning. Mer information finns i [Designdetaljer: kostnadskomponenter](design-details-cost-components.md).  

Transaktioner har kopplats mot varandra, antingen av fasta kopplingar XE "koppling; fast" eller enligt det allmänna antagandet om kostnadsflöde som definieras av värderingsprincipen XE "princip; kostnad" XE "kostnadsprincip" En transaktion med lagerminskning kan kopplas till flera ökningar med olika bokföringsdatum och eventuellt olika anskaffningskostnader XE "anskaffningskostnader". Mer information finns i [Designdetaljer: Artikelkoppling](design-details-item-application.md). Därför baseras beräkningen av lagervärdet  XE "Lagervärde" för ett givet datum på summan av positiva och negativa värdetransaktioner.  

## <a name="inventory-valuation-report"></a>Lagervärdering - rapport  
För att beräkna lagervärdet i rapporten **Lagervärdering** börjar rapporten med att beräkna värdet för artikelns lager på ett visst startdatum. Det lägger till värdet av lagerökningar och subtraherar sedan värdet av lagerminskningar upp till ett visst slutdatum. Slutresultatet är lagervärdet på slutdatumet. Rapporten beräknar dessa värden genom att summera värdena i fältet **Kost.belopp (aktuellt)** i värdetransaktionerna, med hjälp av bokföringsdatum som filter.  

I den utskrivna rapporten visas alltid faktiska belopp, d.v.s. kostnaden för transaktioner som har bokförts som fakturerade. Om du markerar fältet Ta med förväntad kostnad på snabbfliken Alternativ visas även den förväntade kostnaden för transaktioner som har bokförts som inlevererade eller utlevererade.  

> [!IMPORTANT]  
>  Värden i den rapporten **Lagervärdering** stäms av med lagerkontot i redovisningen vilket betyder att värdetransaktionerna i fråga har bokförts i redovisningen.  

> [!IMPORTANT]  
>  Beloppen i kolumnerna **Värde** i rapporten baseras på bokföringsdatumet för transaktioner för en artikel.  

## <a name="inventory-valuation---wip-report"></a>Lagervärdering - PIA-rapport  
Ett produktionsföretag måste bestämma värdet av tre typer av lager:  

* Råmateriallager  
* PIA-lager  
* Färdiga varor i lager  

Värdet i PIA-lagret bestäms av efterföljande ekvation:  

* Avslutande PIA-lager = Start-PIA-lager + produktionskostnader – kostnaden för tillverkade varor  

När det gäller inköpt lager utgör värdetransaktioner grunden för lagervärderingen. Beräkningen görs med hjälp av värdena i fältet **Kost.belopp (aktuellt)** för artikel- och kapacitetvärdetransaktionerna som är kopplade till en produktionsorder.  

Avsikten med PIA-lagervärderingen är att fastställa värdet för artiklarna vars tillverkning ännu inte har slutförts på ett givet datum. Därför baseras PIA-lagervärdet på de värdetransaktioner som är kopplade till förbrukningen och kapacitetstransaktionerna. Förbrukningstransaktioner måste vara helt fakturerade vid datumet för värderingen. Därför visar rapporten **Lagervärdering - PIA** kostnaderna som representerar PIA-lagervärdet i två kategorier: förbrukning och kapacitet.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md)   
[Designdetaljer: Omvärdering](design-details-revaluation.md)   
[Designdetaljer: Bokföring av produktionsorder](design-details-production-order-posting.md)
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

