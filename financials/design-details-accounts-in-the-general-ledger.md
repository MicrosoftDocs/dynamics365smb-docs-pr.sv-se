---
title: Designdetaljer - Konton i redovisningen | Microsoft Docs
description: "Om du vill stämma av lager- och kapacitetstransaktioner med redovisningen, bokförs de relaterade värdetransaktionerna på olika redovisningskonton."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a9d313a4fee3dedf74cc2f0c635516397e26d8ef
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-accounts-in-the-general-ledger"></a>Designdetaljer: Konton i redovisningen
Om du vill stämma av lager- och kapacitetstransaktioner med redovisningen, bokförs de relaterade värdetransaktionerna på olika redovisningskonton. Mer information finns i [detaljer: avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger"></a>Från inventeringstransaktioner  
Följande tabell visar relationen mellan olika typer av lagervärdetransaktioner och konton och motkonton i redovisningen.  

|**Artikeltransaktionstyp**|**Värdetrans.typ**|**Varianstyp**|**Förväntad kostnad**|**Konto**|**Balanskonto**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Inköp|Direkt kostnad||Ja|Lager (interim)|Lagerbokf. (interim)|  
|Inköp|Direkt kostnad||Nr|Lagersaldo|Direkt kostnad kopplad|  
|Inköp|Indirekt kostnad||Nr|Lagersaldo|Omkostnader kopplade|  
|Inköp|Varians|Inköp|Nr|Lagersaldo|Inköpsvarians|  
|Inköp|Omvärdering||Nr|Lagersaldo|Lagerjustering|  
|Inköp|Avrundning||Nr|Lagersaldo|Lagerjustering|  
|Försäljning|Direkt kostnad||Ja|Lager (interim)|KSV (interim)|  
|Försäljning|Direkt kostnad||Nr|Lagersaldo|KSV|  
|Försäljning|Omvärdering||Nr|Lagersaldo|Lagerjustering|  
|Försäljning|Avrundning||Nr|Lagersaldo|Lagerjustering|  
|Positiv justering,Negativ justering,Överföring|Direkt kostnad||Nr|Lagersaldo|Lagerjustering|  
|Positiv justering,Negativ justering,Överföring|Omvärdering||Nr|Lagersaldo|Lagerjustering|  
|Positiv justering,Negativ justering,Överföring|Avrundning||Nr|Lagersaldo|Lagerjustering|  
|(Produktion) Förbrukning|Direkt kostnad||Nr|Lagersaldo|PIA|  
|(Produktion) Förbrukning|Omvärdering||Nr|Lagersaldo|Lagerjustering|  
|(Produktion) Förbrukning|Avrundning||Nr|Lagersaldo|Lagerjustering|  
|Monteringsförbrukning|Direkt kostnad||Nr|Lagersaldo|Lagerjustering|  
|Monteringsförbrukning|Direkt kostnad||Nr|Direkt kostnad kopplad|Lagerjustering|  
|Monteringsförbrukning|Indirekt kostnad||Nr|Omkostnader kopplade|Lagerjustering|  
|(Produktions)utflöde|Direkt kostnad||Ja|Lager (interim)|PIA|  
|(Produktions)utflöde|Direkt kostnad||Nr|Lagersaldo|PIA|  
|(Produktions)utflöde|Indirekt kostnad||Nr|Lagersaldo|Omkostnader kopplade|  
|(Produktions)utflöde|Varians|Material|Nr|Lagersaldo|Materialvarians|  
|(Produktions)utflöde|Varians|Kapacitet|Nr|Lagersaldo|Kapacitetsvarians|  
|(Produktions)utflöde|Varians|Legotillverkning|Nr|Lagersaldo|Legotillverkning varians|  
|(Produktions)utflöde|Varians|Kapacitetsomkostnader|Nr|Lagersaldo|Kapacitetsomkostnader varians|  
|(Produktions)utflöde|Varians|Produktionsomkostnader|Nr|Lagersaldo|Prod.- och omkostnadsvarians|  
|(Produktions)utflöde|Omvärdering||Nr|Lagersaldo|Lagerjustering|  
|(Produktions)utflöde|Avrundning||Nr|Lagersaldo|Lagerjustering|  
|Monteringsutflöde|Direkt kostnad||Nr|Lagersaldo|Lagerjustering|  
|Monteringsutflöde|Omvärdering||Nr|Lagersaldo|Lagerjustering|  
|Monteringsutflöde|Indirekt kostnad||Nr|Lagersaldo|Omkostnader kopplade|  
|Monteringsutflöde|Varians|Material|Nr|Lagersaldo|Materialvarians|  
|Monteringsutflöde|Varians|Kapacitet|Nr|Lagersaldo|Kapacitetsvarians|  
|Monteringsutflöde|Varians|Kapacitetsomkostnader|Nr|Lagersaldo|Kapacitetsomkostnader varians|  
|Monteringsutflöde|Varians|Produktionsomkostnader|Nr|Lagersaldo|Prod.- och omkostnadsvarians|  
|Monteringsutflöde|Avrundning||Nr|Lagersaldo|Lagerjustering|  

## <a name="from-the-capacity-ledger"></a>Från kapacitetstransaktioner  
 Följande tabell visar relationen mellan olika typer av kapacitetvärdetransaktioner och konton och motkonton i redovisningen. Kapacitetstransaktioner representerar arbetstid som förbrukats vid monterings- eller produktionsarbete.  

|**Arbetstyp**|**Kapacitetstrans. typ**|**Värdetrans.typ**|**Konto**|**Balanskonto**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Montering|Resurs|Direkt kostnad|Direkt kostnad kopplad|Lagerjustering|  
|Montering|Resurs|Indirekt kostnad|Omkostnader kopplade|Lagerjustering|  
|Produktion|Maskingrupp/Produktionsgrupp|Inköpskostnad|PIA-konto|Direkt kostnad kopplad|  
|Produktion|Maskingrupp/Produktionsgrupp|Indirekt kostnad|PIA-konto|Omkostnader kopplade|  

## <a name="assembly-costs-are-always-actual"></a>Monteringkostnader är alltid faktiska  
 Som visas i tabellen ovan visas inte bokföringar av montering i interimskonton. Det beror på att konceptet med produkter i arbete (PIA) inte är tillämpligt i monteringsutflödesbokföring, till skillnad från i produktionsutflödesbokföring. Monteringkostnader bokförs bara som faktiska kostnader, aldrig som förväntade kostnader.  

 Mer information finns i [Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md)  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a>Beräknar antal att bokföra i redovisningen  
 Följande fält i tabellen **Värdetransaktion** används för att beräkna det förväntade kostnadsbeloppet som har bokförts i redovisningen:  

-   Kost.belopp (aktuellt)  
-   Kostnad bokförd i redov.  
-   Kost.belopp (förväntat)  
-   Förväntad kost. bokf. i redov.  

Följande tabell visar hur beloppen att bokföra i redovisningen beräknas för de två olika kostnadstyperna.  

|Kostnadstyp|Beräkning|  
|---------------|-----------------|  
|Faktisk kostnad|Kost.belopp (aktuellt) - kostnad bokförd i redovisningen.|  
|Förväntad kostnad|Kost.belopp (förväntat) – Förväntad kost. bokf. i redov.|  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Lagerbokföring](design-details-inventory-posting.md)   
 [Designdetaljer: Bokföring av förväntad kostnad](design-details-expected-cost-posting.md)  
 [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

