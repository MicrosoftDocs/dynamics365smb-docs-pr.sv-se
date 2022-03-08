---
title: Rapporter och analyser för anläggningstillgångar
description: Se vilka försäljningsrapporter och analyser som är tillgängliga i standardversionen av Business Central så att du kan hålla reda på dina anläggningstillgångar.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: c28e62a2de51323e0a7dcd2f4b5ea26d5896d718
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543374"
---
# <a name="fixed-assets-reports-and-analytics-in-business-central"></a>Rapporter för anläggningstillgångar och analys i Business Central

För att hjälpa dig att hantera dina anläggningstillgångar i [!INCLUDE [prod_short](includes/prod_short.md)] är standardrapporter och analyser inbyggda. Det överskrider traditionella rapporteringsbegränsningar för att hjälpa dig att effektivt utforma olika typer av rapporter.  

## <a name="reports"></a>Rapporter

I följande tabell beskrivs några av de viktigaste rapporterna inom rapportering av anläggningstillgångar.

| Rapportera | Objekt-ID | Beskrivning |
|--|--|--|
| **Anläggningstillgångslista** | 5601 | Visar en lista över anläggningstillgångar och deras inställningsinformation för en viss avskrivningsregel. |
| **Anl.tillg. - Anskaffningslista** | 5608 | Visa en lista över alla tillgångar som förvärvats inom ett visst datumintervall. Du kan också ta med anläggningstillgångar som har skapats men ännu inte förvärvats. |
| **Anläggningstillgång - detaljer** | 5604 | Visar anläggningstillgångstransaktionerna för anläggningstillgångar. |
| **Analys av anläggningstillgång** | 5600 | En analysrapport där du kan ange två datumkolumner och tre datakolumner som ska visas i rapporten. Om du till exempel vill generera en rapport som ska användas för avstämning med redovisningen, lägger du till kolumner för anskaffningskostnad vid slutdatum, avskrivning vid slutdatum och bokföringsvärde vid slutdatum. En kontrollrapport kan ha anskaffning/nettoförändring, nedskrivning/nettoförändring och uppskrivning/nettoförändring, så varje förändring i anläggningstillgång kan kontrolleras om det behövs. Om du väljer fältet **budgetrapport** och anger ett slutdatum i framtiden, kommer rapporten att beräkna den framtida avskrivningen och kan ge uppskattningar för framtida avskrivning och bokföringsvärden om du har valt dessa fält som rapportkolumner. |
| **Planerat värde för anläggningstillgång** | 5607 | Visar planerade avskrivningsbelopp och bokföringsvärde för en framtida period för tillgångar. Rapporten är användbar när du använder olika avskrivningsmetoder för tillgångar och vill beräkna nästa års avskrivning till exempel. Använd rapporten när du vill skapa budgetbeloppen för avskrivning genom att välja en budget och fältet **Kopiera till Redov. budget**. |
| **Anl. bokföringsvärde 01** | 5605 | Visar detaljerad information om anskaffningskostnad, avskrivnings- och bokföringsvärde för både individuella anläggningstillgångar och grupper av anläggningstillgångar. För var och en av de tre belopptyperna beräknas beloppen i början och i slutet av en angiven period liksom även för perioden i sig. Om du väljer fältet **budgetrapport** kommer rapporten att beräkna den förväntade avskrivningen för perioden. Ange en *grupptyp* om du vill att anläggningstillgångarna ska grupperas i rapporten och att grupptotaler ska skrivas ut. Om du t.ex. har definierat sex anläggningstillgångsindelningar väljer du alternativet *Anl. indelningskod* för att få grupptotaler utskrivna för var och en av de sex indelningskoderna.|
| **Anl. bokföringsvärde 02** | 5606 |Visar fördelningen av bokföringsvärde för anläggningstillgångar genom ändringar i anskaffning, avskrivning och uppskrivning inom perioden med en ytterligare uppdelning genom tillägg och avyttringar inom perioden. Använd den här rapporten när du vill beskriva förändringar av anläggningstillgångar under en given period när många olika ändringar sker genom grupperingen av anläggningstillgångarna. Om du väljer fältet **budgetrapport** kommer rapporten att beräkna den förväntade avskrivningen för perioden. Ange en *grupptyp* om du vill att anläggningstillgångarna ska grupperas i rapporten och att grupptotaler ska skrivas ut. Om du t.ex. har definierat sex anläggningstillgångsindelningar väljer du alternativet *Anl. indelningskod* för att få grupptotaler utskrivna för var och en av de sex indelningskoderna. |
| **Redovisningsanalys av anläggningstillgång**| 5610 |Visar en analys av anläggningstillgångarna med olika slags data för både individuella anläggningstillgångar och/eller grupper av anläggningstillgångar. På snabbfliken Anläggningstillgång kan du definiera filter om du vill att rapporten endast ska omfatta vissa anläggningstillgångar. Anpassa rapporten efter dina specifika behov på snabbfliken Alternativ. Rapporten liknar rapporten **analys av anläggningstillgångar**, men specifikt för att stämma av redovisningen och särskilt för validering av avyttringstransaktioner. Rapporten förutsätter att du känner till de redovisningskonton som har angetts i bokföringsinställningarna. |
| **Anl.tillg. - bokförda journaler** |5603  |Visar bokförda anläggningstillgångstransaktioner som är sorterade och uppdelade efter journalnummer. Du kan bestämma vilka bokförda journalers transaktioner som ska visas genom att definiera ett filter. Det är viktigt att du definierar ett filter annars kan rapporten visa en oerhörd mängd information. |

## <a name="see-also"></a>Se även

[Analysera bokslut i Microsoft Excel](finance-analyze-excel.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Hantera anläggningstillgångar](fa-manage.md)  
[Översikt över lokala funktioner](about-localization.md)  
[Revisorupplevelse i [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
