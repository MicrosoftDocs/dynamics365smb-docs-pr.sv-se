---
title: Designdetaljer – Konton i redovisningen | Microsoft Docs
description: 'Om du vill stämma av lager- och kapacitetstransaktioner med redovisningen, bokförs de relaterade värdetransaktionerna på olika redovisningskonton.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
---
# Designdetaljer: Konton i redovisningen
Om du vill stämma av lager- och kapacitetstransaktioner med redovisningen, bokförs de relaterade värdetransaktionerna på olika redovisningskonton. Mer information finns i [detaljer: avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md).  

## Från inventeringstransaktioner  
Följande tabell visar relationen mellan olika typer av lagervärdetransaktioner och konton och motkonton i redovisningen.  

|**Artikeltransaktionstyp**|**Värdetrans.typ**|**Varianstyp**|**Förväntad kostnad**|**Konto**|**Balanskonto**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Inköp|Direkt kostnad||Ja|Lager (interim)|Lagerbokf. (interim)|  
|Inköp|Direkt kostnad||Nej|Lagersaldo|Direkt kostnad kopplad|  
|Inköp|Indirekt kostnad||Nej|Lagersaldo|Omkostnader kopplade|  
|Inköp|Varians|Inköp|Nej|Lagersaldo|Inköpsvarians|  
|Inköp|Omvärdering||Nej|Lagersaldo|Lagerjustering|  
|Inköp|Avrundning||Nej|Lagersaldo|Lagerjustering|  
|Försäljning|Direkt kostnad||Ja|Lager (interim)|KSV (interim)|  
|Försäljning|Direkt kostnad||Nej|Lagersaldo|KSV|  
|Försäljning|Omvärdering||Nej|Lagersaldo|Lagerjustering|  
|Försäljning|Avrundning||Nej|Lagersaldo|Lagerjustering|  
|Positiv justering,Negativ justering,Överföring|Direkt kostnad||Nej|Lagersaldo|Lagerjustering|  
|Positiv justering,Negativ justering,Överföring|Omvärdering||Nej|Lagersaldo|Lagerjustering|  
|Positiv justering,Negativ justering,Överföring|Avrundning||Nej|Lagersaldo|Lagerjustering|  
|(Produktion) Förbrukning|Direkt kostnad||Nej|Lagersaldo|PIA|  
|(Produktion) Förbrukning|Omvärdering||Nej|Lagersaldo|Lagerjustering|  
|(Produktion) Förbrukning|Avrundning||Nej|Lagersaldo|Lagerjustering|  
|Monteringsförbrukning|Direkt kostnad||Nej|Lagersaldo|Lagerjustering|  
|Monteringsförbrukning|Direkt kostnad||Nej|Direkt kostnad kopplad|Lagerjustering|  
|Monteringsförbrukning|Indirekt kostnad||Nej|Omkostnader kopplade|Lagerjustering|  
|(Produktions)utflöde|Direkt kostnad||Ja|Lager (interim)|PIA|  
|(Produktions)utflöde|Direkt kostnad||Nej|Lagersaldo|PIA|  
|(Produktions)utflöde|Indirekt kostnad||Nej|Lagersaldo|Omkostnader kopplade|  
|(Produktions)utflöde|Varians|Material|Nej|Lagersaldo|Materialvarians|  
|(Produktions)utflöde|Varians|Kapacitet|Nej|Lagersaldo|Kapacitetsvarians|  
|(Produktions)utflöde|Varians|Legotillverkning|Nej|Lagersaldo|Legotillverkning varians|  
|(Produktions)utflöde|Varians|Kapacitetsomkostnader|Nej|Lagersaldo|Kapacitetsomkostnader varians|  
|(Produktions)utflöde|Varians|Produktionsomkostnader|Nej|Lagersaldo|Prod.- och omkostnadsvarians|  
|(Produktions)utflöde|Omvärdering||Nej|Lagersaldo|Lagerjustering|  
|(Produktions)utflöde|Avrundning||Nej|Lagersaldo|Lagerjustering|  
|Monteringsutflöde|Direkt kostnad||Nej|Lagersaldo|Lagerjustering|  
|Monteringsutflöde|Omvärdering||Nej|Lagersaldo|Lagerjustering|  
|Monteringsutflöde|Indirekt kostnad||Nej|Lagersaldo|Omkostnader kopplade|  
|Monteringsutflöde|Varians|Material|Nej|Lagersaldo|Materialvarians|  
|Monteringsutflöde|Varians|Kapacitet|Nej|Lagersaldo|Kapacitetsvarians|  
|Monteringsutflöde|Varians|Kapacitetsomkostnader|Nej|Lagersaldo|Kapacitetsomkostnader varians|  
|Monteringsutflöde|Varians|Produktionsomkostnader|Nej|Lagersaldo|Prod.- och omkostnadsvarians|  
|Monteringsutflöde|Avrundning||Nej|Lagersaldo|Lagerjustering|  

## Från kapacitetstransaktioner  
 Följande tabell visar relationen mellan olika typer av kapacitetvärdetransaktioner och konton och motkonton i redovisningen. Kapacitetstransaktioner representerar arbetstid som förbrukats vid monterings- eller produktionsarbete.  

|**Arbetstyp**|**Kapacitetstrans. typ**|**Värdetrans.typ**|**Konto**|**Balanskonto**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Montering|Resurs|Direkt kostnad|Direkt kostnad kopplad|Lagerjustering|  
|Montering|Resurs|Indirekt kostnad|Omkostnader kopplade|Lagerjustering|  
|Produktion|Maskingrupp/Produktionsgrupp|Inköpskostnad|PIA-konto|Direkt kostnad kopplad|  
|Produktion|Maskingrupp/Produktionsgrupp|Indirekt kostnad|PIA-konto|Omkostnader kopplade|  

## Monteringkostnader är alltid faktiska  
 Som visas i tabellen ovan visas inte bokföringar av montering i interimskonton. Det beror på att konceptet med produkter i arbete (PIA) inte är tillämpligt i monteringsutflödesbokföring, till skillnad från i produktionsutflödesbokföring. Monteringkostnader bokförs bara som faktiska kostnader, aldrig som förväntade kostnader.  

 Mer information finns i [Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md)  

## Beräknar antal att bokföra i redovisningen  
 Följande fält i tabellen **Värdetransaktion** används för att beräkna det förväntade kostnadsbeloppet som har bokförts i redovisningen:  

-   Kost.belopp (aktuellt)  
-   Kostnad bokförd i redov.  
-   Kost.belopp (förväntat)  
-   Förväntad kost. bokf. i redov.  

Följande tabell visar hur beloppen att bokföra i redovisningen beräknas för de två olika kostnadstyperna.  

|Kostnadstyp|Beräkning|  
|---------------|-----------------|  
|Faktisk kostnad|Kost.belopp (aktuellt) – kostnad bokförd i redovisningen.|  
|Förväntad kostnad|Kost.belopp (förväntat) – Förväntad kost. bokf. i redov.|  

## Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Lagerbokföring](design-details-inventory-posting.md)   
 [Designdetaljer: Bokföring av förväntad kostnad](design-details-expected-cost-posting.md)  
 [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]