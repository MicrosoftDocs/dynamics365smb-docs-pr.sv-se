---
title: Felmeddelanden "Bokföringsdatumet är inte inom ditt tillåtna intervall för bokföringsdatum"
description: Lös felet bakom meddelandet "bokföringsdatumet är inte inom det tillåtna intervallet av bokföringsdatum" när du kör batch-jobbet Justera kostn. – artikeltrans.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/17/2021
ms.author: edupont
ms.openlocfilehash: 68d0fc68b799306fafa4e4fc0fb5f6cb146faca9
ms.sourcegitcommit: 772af6954539c65743d1a2f59e8a37d30bd30278
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/27/2021
ms.locfileid: "7557309"
---
# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Felmeddelande "Bokföringsdatumet är inte inom ditt tillåtna intervall för bokföringsdatum..."

När du använder batch-jobbet **Justera kost. – artikeltrans.** kan du köra följande felmeddelande:

**Bokföringsdatumet är inte inom det tillåtna intervallet för bokföringsdatum**

Det här felmeddelandet anger att användaren inte har tillåtelse att bokföra transaktioner för det aktuella datumet, och kan åtgärdas genom att användarinställningarna ändras.

## <a name="change-the-user-setup"></a>Ändra användarinställningar  

|Användar-ID  |Tillåt bokföring fr.o.m.  | Tillåt bokföring t.o.m.  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

Användaren i detta exempel har ett tillåtet datumintervall för bokföring från den 11 september till den 30 september, och får därmed inte bokföra justeringsvärdetransaktionen med bokföringsdatum 10 september.  

### <a name="overview-of-involved-posting-date-setup"></a>Översikt över berörda inställningar för bokföringsdatum

#### <a name="inventory-periods"></a>Lagerperioder

|Slutdatum  |Name  |Avslutad  |
|---------|---------|---------|
|2020-01-31     |2020 januari      |  Ja    |
|2020-02-28     |Februari 2020     |  Ja    |
|2020-03-31     |Mars 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Maj 2020        |  Ja    |
|2020-06-30     |Juni 2020       |  Ja    |
|2020-07-31     |Juli 2020        |   Ja   |
|2020-08-31     |Augusti 2020     |   Ja   |
|2020-09-30     |September 2020.  |         |
|2020-10-31     |Oktober 2020    |         |
|2020-11-30     |November 2020   |         |
|2020-12-31     |December 202   |         |  

#### <a name="general-ledger-setup"></a>Redovisningsinställningar

|Fält|Värde|
|---------|---------|
|Tillåt bokföring fr.o.m.:  |  2020-09-10      |
|Tillåt bokföring t.o.m.:    |  2020-09-30      |
|Tidsregistrering:       |         |
|Lokalt adressformat:|   Postnr      |  

#### <a name="user-setup"></a>Användarinställningar

|Användar-ID  |Tillåt bokföring fr.o.m.  | Tillåt bokföring t.o.m.  |
|---------|---------|--------|
|ANVÄNDARNAMN |  2020-09-10      |2020-09-30      |

Tilldela ett bredare tillåtet intervall för bokföringsdatum som i lagerperioden eller redovisningskonfigurationen för att undvika konflikten som orsakar felmeddelandet. Justeringsvärdestransaktionen med bokföringsdatum 10 september kommer att bokföras med denna inställning.
  
## <a name="see-also"></a>Se även  

[Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Designdetaljer: Lagerkostnader](design-details-inventory-costing.md)  
[Designdetaljer: Artikelkoppling](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
