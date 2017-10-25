---
title: "Resultat av överföringen | Microsoft Docs"
description: "Det här avsnittet beskriver vad som händer när du överför redovisningstransaktioner till kostnadstransaktioner."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9f1c3573137d7cd15c8b98813da514f8b8f2e1cd
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a>Resultat av överföring av redovisningstransaktioner till kostnadstransaktioner
Under överföringen av redovisningstransaktioner till kostnadstransaktioner skapar [!INCLUDE[d365fin](includes/d365fin_md.md)] anslutningar i transaktionerna i tabellen **Redov.trans**, tabellen **kostnadstransaktion** och tabellen **Bokförd journal för kostnad** för att göra det möjligt att spåra anslutningar mellan kostnadstransaktioner och redovisningstransaktioner.  

## <a name="general-ledger-entries"></a>Redovisningstransaktioner  
För varje redovisningstransaktion som har överförts till kostnadsredovisning fyller fältet [!INCLUDE[d365fin](includes/d365fin_md.md)] i kostnadsfältet **Trans. nr.**  

## <a name="cost-entries"></a>Kostnadstransaktioner  
För varje kostnadstransaktion sparar [!INCLUDE[d365fin](includes/d365fin_md.md)] löpnumret för motsvarande redovisningstransaktion i fältet **Löpnr redovisning** i tabellen **Kostnadstransaktion**.  

För kombinerade kostnadstransaktioner sparar [!INCLUDE[d365fin](includes/d365fin_md.md)] transaktionsnumret för den senaste redovisningstransaktionen, som är transaktionen med det högsta numret.  

Fältet **Redovisningskonto** i tabellen **Kostnadstransaktion** innehåller numret på det redovisningskonto som kostnadstransaktionen kommer ifrån.  

För enstaka kostnadstransaktioner överför [!INCLUDE[d365fin](includes/d365fin_md.md)] bokföringstexten från redovisningstransaktionen till textfältet **Beskrivning**. För kombinerade transaktioner visar textfältet dessa transaktioner överförda som kombinerade transaktioner. Till exempel för en kombinerad transaktion för månaden Oktober 2013 kan texten vara **Kombinerade transaktioner, Oktober 2013**.  

## <a name="cost-register"></a>Bokförd journal för kostnad  
I tabellen **Bokförd journal för kostnad** skapar [!INCLUDE[d365fin](includes/d365fin_md.md)] en transaktion med källöverföringen från redovisningen. Transaktionen registrerar första och sista löpnumret för redovisningstransaktionerna som har överförts, i tillägg till första och sista löpnumret för kostnadstransaktionerna som skapas.  

## <a name="see-also"></a>Se även  
[Så här: Överföra redovisningstransaktioner till kostnadstransaktioner](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
[Villkor för överföring av redovisningstransaktioner till kostnadstransaktioner](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
[Automatisk överföring och kombinerade transaktioner](finance-automatic-transfer-combined-entries.md)   
[Överföra och bokföra kostnadstransaktioner](finance-transfer-and-post-cost-entries.md)  

