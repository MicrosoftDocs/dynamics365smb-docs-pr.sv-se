---
title: "Designdetaljer - Bokföring av förväntad kostnad | Microsoft Docs"
description: "Förväntade kostnader representerar uppskattningen av exempelvis en inköpt artikels kostnad som du registrerar innan fakturan för artikeln erhålls."
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
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 50ac9cbb946fedc687eb5ea1373c99d68f3d322b
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-expected-cost-posting"></a>Designdetaljer: Bokföring av förväntad kostnad
Förväntade kostnader representerar uppskattningen av exempelvis en inköpt artikels kostnad som du registrerar innan fakturan för artikeln erhålls.  

 Du kan bokföra förväntade kostnader till lagret och redovisningen. När du bokför ett antal som bara har inlevererats eller levererats men inte fakturerats, skapas en värdetransaktion med den förväntade kostnaden. Den förväntade kostnaden påverkar lagervärdet men bokförs inte till redovisningen om du inte har ställt in systemet att göra det.  

> [!NOTE]  
>  Förväntade kostnader hanteras endast för artikeltransaktioner. Förväntade kostnader är inte för immateriella transaktionstyper, till exempel kapacitet och artikelomkostnader.  

 Om endast antalsdelen för en lagerökning har bokförts ändras lagervärdet inte i redovisningen, om du inte har markerat kryssrutan **Förväntad kost.bokf. i redov.** i fönstret the **Lagerinställningar**. I så fall bokförs förväntade kostnader på interimskonton vid tidpunkten för inleveransen. När inleveransen har fakturerats helt balanseras interimskontona och den faktiska kostnaden bokförs till lagerkontot.  

 För att stödja avstämning och spårbarhet visar den fakturerade värdetransaktionen det förväntade kostnadsbeloppet som har bokförts för att motkontera interimskontona.  

## <a name="example"></a>Exempel  
 Följande exempel visar förväntade kostnaden om kryssrutan **Automatisk kostnadsbokföring** och kryssrutan **Förväntad kost.bokf. i redov.** är markerad i fönstret **Lagerinställningar**.  

 Du bokför en inköpsorder som mottagen. Förväntad kostnad är 95,00 BVA.  

 **Värdetransaktioner**  

|Bokföringsdatum|Transaktionstyp|Kost.belopp (förväntat)|Förväntad kost. bokf. i redov.|Förväntad kostnad|Artikeltrans.löpnr|Löpnr|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|01-01-20|Inköpskostnad|95.00|95.00|Ja|1|1|  

 **Relationstransaktioner i redovisning – tabellen Artikeltransaktionsrelation**  

|Löpnr redovisning|Värdelöpnr|Bokf. redov.journalnr|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  

 **Redovisningstransaktioner**  

|Bokföringsdatum|Redovisningskonto|Kontonr. (En-US-demo)|Belopp|Löpnr|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|Lagerkontoredovisning (interim)|5530|-95.00|2|  
|01-01-20|Lager (interim)|2131|95.00|1|  

 Du kan bokföra inköpsordern som fakturerad vid ett senare tillfälle. Fakturerad kostnad är 100,00 BVA.  

 **Värdetransaktioner**  

|Bokföringsdatum|Kost.belopp (aktuellt)|Kost.belopp (förväntat)|Kostnad bokförd i redov.|Förväntad kostnad|Artikeltrans.löpnr|Löpnr|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|01-15-20|100,00|-95.00|100,00|Nej|1|2|  

 **Relationstransaktioner i redovisning – tabellen Artikeltransaktionsrelation**  

|Löpnr redovisning|Värdelöpnr|Bokf. redov.journalnr|  
|--------------------|---------------------|-----------------------|  
|3|2|2|  
|4|2|2|  
|5|2|2|  
|6|2|2|  

 **Redovisningstransaktioner**  

|Bokföringsdatum|Redovisningskonto|Kontonr. (En-US-demo)|Belopp|Löpnr|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-15-20|Lagerkontoredovisning (interim)|5530|95.00|4|  
|01-15-20|Lager (interim)|2131|-95.00|3|  
|01-15-20|Direkt kostnad kopplad - konto|7291|-100|6|  
|01-15-20|Lagerkonto|2130|100|5|  

## <a name="see-also"></a>Se även
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)   
 [Designdetaljer: Avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md)   
 [Designdetaljer: Lagerbokföring](design-details-inventory-posting.md)   
 [Designdetaljer: Varians](design-details-variance.md)  
 [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

