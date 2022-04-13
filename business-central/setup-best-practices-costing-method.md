---
title: 'Lägga upp bästa metoder: Värderingsprincip'
description: Värderingsprincipen på artikelkortet anger hur artikelns kostnadsflöde registreras och om ett faktiskt eller budgeterat värde ska kapitaliseras och användas i kostnadsberäkningen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 30, 31
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 95194e3afed89d8a5636e53e1da76c20d81296ef
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522544"
---
# <a name="setup-best-practices-costing-method"></a>Lägga upp bästa praxis: Värderingsprincip

**Värderingsprincipen** på artikelkortet anger hur artikelns kostnadsflöde registreras och om ett faktiskt eller budgeterat värde ska kapitaliseras och användas i kostnadsberäkningen.  

Det är viktigt att ange rätt värderingsprincip enligt artikeltyp och affärsmiljö för att garantera ekonomiska lager.  

I tabellen nedan finns bästa metod för hur du lägger upp fältet **Värderingsprincip**. Mer information finns i [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md).  

|Inställningsalternativ|Best practice|Kommentar|  
|------------------|-------------------|-------------|  
|FIFO|Använd där produktkostnaden är fast.<br /><br /> Använd för artiklar med ett begränsat hållbarhetstid, eftersom den äldsta varor behöver säljas innan deras hållbarhetstid passerat.|En artikels styckkostnad är det verkliga värdet på en mottagen artikel, vald enligt FIFO-regeln.<br /><br /> I lagervärdering antas det att de första artiklarna in i lagret säljs först. **Obs!**  När priser stiger visar balansräkningen ett högre värde Det betyder att skatteskuler ökar, men kreditpoängen och förmåga att låna kontant ökar.|  
|LIFO (Sist in, först ut)|Använd där lagernivåer är konsekvent underhållna eller ökar med tiden.|En artikels styckkostnad är det verkliga värdet på en mottagen artikel, vald enligt LIFO-regeln.<br /><br /> I lagervärdering antas det att de senaste artiklarna in i lagret säljs först. **Obs!**  När priser vill stiger, minskas värdet på resultaträkningen. Det betyder att skatteskuler minskar, men din förmåga att låna kontant försämras. **Viktigt:**  Tillåts inte i många länderregioner, eftersom det kan användas för att dölja vinst.|  
|Genomsnitt|Använd där produktkostnaden inte är fast.<br /><br /> Använd där lager travas eller blandas samman och inte kan åtskiljas, till exempel kemikalier.|En artikels styckkostnad beräknas enligt den genomsnittliga styckkostnaden vid varje tidpunkt efter ett inköp.<br /><br /> För lagervärdering förutsätts att alla lagerartiklar säljs samtidigt.|
|Specifik|Använd i produktionen eller handel med enkelt härledas artiklar med i höga kostnadspris.<br /><br /> Använda för artiklar, som lyder under regler.<br /><br /> Använd för artiklar med serienummer.|En artikels styckkostnad är den exakta kostnaden för mottagandet av den aktuella enheten.|
|Standard|Använd där kostnadskontroll är kritisk.<br /><br /> Använd i upprepande produktion för att värdera kostnaderna för direkt material, direkt arbete och produktionsoverheadkostnad.<br /><br /> Använd när det finns funktion och personal som underhåller standarder.|En artikels styckkostnad är förinställd baserad på uppskattning.<br /><br /> När den verkliga kostnaden senare realiseras, måste standardkostnaden justeras med den verkliga kostnaden via skillnadsvärden.|  

## <a name="see-also"></a>Se även

[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)  
[Designdetaljer: Lagerkostnader](design-details-inventory-costing.md)  
[Skapa komplexa moduler med hjälp av bästa praxis](set-up-complex-application-areas-using-best-practices.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]