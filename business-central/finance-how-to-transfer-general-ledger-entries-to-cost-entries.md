---
title: "Så här: Överföra redovisningstransaktioner till kostnadstransaktioner | Microsoft Docs"
description: "Du kan överföra redovisningstransaktioner till kostnadstransaktioner."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 62ed00ef7ca278245b9cdd1a28a4ee70cf9a8f11
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Överföra redovisningstransaktioner till kostnadstransaktioner
Du kan överföra redovisningstransaktioner till kostnadstransaktioner.  

Innan du kör processen för att överföra redovisningstransaktioner till kostnadstransaktioner, måste du förbereda överföringen för att undvika manuella rättningsbokföringar.  

## <a name="to-prepare-the-transfer"></a>Så här förbereder du överföringen  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inställningar för kostnadsredovisning** och välj sedan relaterad länk.  
2.  I fönstret **Inställningar för kostnadsredovisning** kontrollerar du att fältet **startdatum för överföring till redovisning** anges till rätt värde.  
3.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lista över kostnadstyper** och välj sedan relaterad länk.  
4.  I fönstret **Kostnadstypkort** kontrollerar du att fältet **Redovisningskontointervall** är korrekt länkat för alla kostnadstyper som tar transaktioner från redovisningen.  
5.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontoplan** och välj sedan relaterad länk.  
6.  För varje relevant redovisningskonto i fönstret **Redovisningskontokort** kontrollerar du att fältet **Kostnadstypsnr.** är korrekt länkat till en kostnadstyp. För mer information, se [Definiera relationen mellan kostnadstyper och redovisningskonton](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)  
7.  Kontrollera att alla relevanta redovisningstransaktioner har dimensionsvärden som motsvarar ett kostnadsställe och en kostnadsbärare.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Så här överför du redovisningstransaktioner till kostnadstransaktioner  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Överför redovisningstransaktioner till kostnadsredovisning** och välj sedan relaterad länk.  
2.  Välj **Ja** för att starta överföringen. Processen överför alla redovisningstransaktioner som inte redan har överförts.  

    Under överföringen skapar processen anslutningar i transaktionerna i tabellerna **Kostnadstransaktion** och **Bokförd journal för kostnad**. Det gör det möjligt att spåra ursprunget till kostnadstransaktionerna.  

## <a name="see-also"></a>Se även  
 [Villkor för överföring av redovisningstransaktioner till kostnadstransaktioner](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Automatisk överföring och kombinerade transaktioner](finance-automatic-transfer-combined-entries.md)   
 [Resultat av överföringen](finance-results-of-the-transfer.md)   
 [Överföra och bokföra kostnadstransaktioner](finance-transfer-and-post-cost-entries.md)   
 [Definiera relationen mellan kostnadstyper och redovisningskonton](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

