---
title: Överföra och bokföra kostnadstransaktioner
description: Innan du definierar kostnadsfördelningar, måste du förstå hur kostnadstransaktioner kommer från olika källor.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 1100, 1103, 1104, 1108, 1113, 1135
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: fcff82e597a47541c5077de47594bb9916a40d67
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136016"
---
# <a name="transferring-and-posting-cost-entries"></a>Överföra och bokföra kostnadstransaktioner

Innan du definierar kostnadsfördelningar, måste du förstå hur kostnadstransaktioner kommer från följande källor:  

- Automatisk överföring av redovisningstransaktioner.  
- Manuell kostnadsbokföring för rena kostnadstransaktioner, interna avgifter och manuella fördelningar.  
- Automatiska fördelningsbokföringar för faktiska kostnader.  
- Överföring av budgettransaktioner till faktisk.

## <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Villkor för överföring av redovisningstransaktioner till kostnadstransaktioner
Det är viktigt att förstå villkor för överföring av redovisningstransaktioner mot kostnadstransaktioner. Under överföringen använder batchjobbet **Överför redovisningstransaktioner till kostnadsredovisning** följande villkor för att bestämma om och hur redovisningstransaktionerna överförs.  

Redovisningstransaktioner överförs om:  

- Transaktionerna har dimensionsvärden som motsvarar antingen ett kostnadsställe eller en kostnadsbärare.  
- Transaktionerna har dimensionsvärden som motsvarar ett kostnadsställe och en kostnadsbärare. För dessa verifikationer har kostnadsstället prioritet. Det gör att det går att undvika en situation där en kostnadstyp visas både i en kostnadsbärare och ett kostnadsställe och därigenom räknas två gånger i statistiken.  
- Verifikationsnumret i transaktionerna är tomt, så att visas med verifikationsnumret 0000 i kostnadstransaktionerna.  
- Transaktionerna överförs till en kostnadstyp som används för kombinerade transaktioner, och dessa transaktioner överförs som en kombinerad transaktionen antingen månatligt eller dagligen.  

Redovisningstransaktioner överförs inte om:  

- Transaktionerna har dimensionsvärden som inte motsvarar ett kostnadsställe eller en kostnadsbärare.  
- Transaktionerna har ett belopp på noll.  
- Transaktionerna har ett redovisningskonto som har tagits bort.  
- Transaktionerna har ett redovisningskonto som inte är av typen **Resultaträkning**.  
- Transaktionerna har ett redovisningskonto som inte har kopplats till en kostnadstyp.  
- Transaktionerna har ett bokföringsdatum före startdatum för **Startdatum för överföring till redovisning**.  
- Transaktionerna har bokförts med ett stängningsdatum. Dessa är vanliga transaktioner som nollställer saldot i resultaträkningen i slutet av året.

## <a name="transferring-general-ledger-entries-to-cost-entries"></a>Överföring av redovisningstransaktioner till kostnadstransaktioner
Du kan överföra redovisningstransaktioner till kostnadstransaktioner.  

Innan du kör processen för att överföra redovisningstransaktioner till kostnadstransaktioner, måste du förbereda överföringen för att undvika manuella rättningsbokföringar.  

### <a name="to-prepare-the-transfer"></a>Så här förbereder du överföringen  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Inställningar för kostnadsredovisning** och välj sedan relaterad länk.  
2.  På sidan **Inställningar för kostnadsredovisning** kontrollerar du att fältet **startdatum för överföring till redovisning** anges till rätt värde.  
3.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Lista över kostnadstyper** och väljer sedan relaterad länk.  
4.  På sidan **Kostnadstypkort** kontrollerar du att fältet **Redovisningskontointervall** är korrekt länkat för alla kostnadstyper som tar transaktioner från redovisningen.  
5.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
6.  För varje relevant redovisningskonto på sidan **Redovisningskontokort** kontrollerar du att fältet **Kostnadstypsnr.** är korrekt länkat till en kostnadstyp. Mer information finns i [Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md).  
7.  Kontrollera att alla relevanta redovisningstransaktioner har dimensionsvärden som motsvarar ett kostnadsställe och en kostnadsbärare.  

### <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Så här överför du redovisningstransaktioner till kostnadstransaktioner  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Överför redovisningstransaktioner till kostnadsredovisning** och välj sedan relaterad länk.  
2.  Välj **Ja** för att starta överföringen. Processen överför alla redovisningstransaktioner som inte redan har överförts.  

Under överföringen skapar processen anslutningar i transaktionerna i tabellerna **Kostnadstransaktion** och **Bokförd journal för kostnad**. Det gör det möjligt att spåra ursprunget till kostnadstransaktionerna.

## <a name="automatic-transfer-and-combined-entries"></a>Automatisk överföring och kombinerade transaktioner
I kostnadsredovisningen kan du överföra redovisningstransaktioner till en kostnadstyp, genom att använda en kombinerad bokföring. Du kan ange om en kostnadstyp tar emot kombinerade transaktioner i fältet **Kombinera transaktioner** i kostnadstypsdefinitionen. Alternativen beskrivs i tabellen nedan.  

|Kombinera transaktioner|Description|  
|---------------------|-----------------|  
|Ingen|Varje redovisningstransaktion överförs individuellt till motsvarande kostnadstyp.|  
|Dag|Redovisningstransaktioner med samma bokföringsdatum överförs som en post till motsvarande kostnadstyp.|  
|Månad|Alla redovisningstransaktioner i samma kalendermånad överförs som en post till motsvarande kostnadstyp.|  

> [!IMPORTANT]  
>  Om du har markerat kryssrutan **Automatisk överföring från redovisning** på sidan **Inställningar för kostnadsredovisning**, [!INCLUDE[prod_short](includes/prod_short.md)] uppdaterar kostnadsredovisningen efter varje bokföring i redovisningen. Kombinerade transaktioner är inte möjliga.

## <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a>Resultat av överföring av redovisningstransaktioner till kostnadstransaktioner
Under överföringen av redovisningstransaktioner till kostnadstransaktioner skapar [!INCLUDE[prod_short](includes/prod_short.md)] anslutningar i transaktionerna i tabellen **Redov.trans**, tabellen **kostnadstransaktion** och tabellen **Bokförd journal för kostnad** för att göra det möjligt att spåra anslutningar mellan kostnadstransaktioner och redovisningstransaktioner.  

### <a name="general-ledger-entries"></a>Redovisningstransaktioner  
För varje redovisningstransaktion som har överförts till kostnadsredovisning fyller fältet [!INCLUDE[prod_short](includes/prod_short.md)] i kostnadsfältet **Trans. nr.**  

### <a name="cost-entries"></a>Kostnadstransaktioner  
För varje kostnadstransaktion sparar [!INCLUDE[prod_short](includes/prod_short.md)] löpnumret för motsvarande redovisningstransaktion i fältet **Löpnr redovisning** i tabellen **Kostnadstransaktion**.  

För kombinerade kostnadstransaktioner sparar [!INCLUDE[prod_short](includes/prod_short.md)] transaktionsnumret för den senaste redovisningstransaktionen, som är transaktionen med det högsta numret.  

Fältet **Redovisningskonto** i tabellen **Kostnadstransaktion** innehåller numret på det redovisningskonto som kostnadstransaktionen kommer ifrån.  

För enstaka kostnadstransaktioner överför [!INCLUDE[prod_short](includes/prod_short.md)] bokföringstexten från redovisningstransaktionen till textfältet **Beskrivning**. För kombinerade transaktioner visar textfältet dessa transaktioner överförda som kombinerade transaktioner. Till exempel för en kombinerad transaktion för månaden Oktober 2013 kan texten vara **Kombinerade transaktioner, Oktober 2013**.  

### <a name="cost-register"></a>Bokförd journal för kostnad  
I tabellen **Bokförd journal för kostnad** skapar [!INCLUDE[prod_short](includes/prod_short.md)] en transaktion med källöverföringen från redovisningen. Transaktionen registrerar första och sista löpnumret för redovisningstransaktionerna som har överförts, i tillägg till första och sista löpnumret för kostnadstransaktionerna som skapas.

## <a name="see-also"></a>Se även  
 [Om kostnadsredovisning](finance-about-cost-accounting.md)   
 [Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md)   
 [Definiera och fördela kostnader](finance-define-and-allocate-costs.md)   
 [Redovisa kostnader](finance-manage-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]