---
title: Uppdatera valutakurser | Microsoft Docs
description: Spåra belopp i olika valutor med hjälp av valutakoder och låt Business Central hjälpa dig att justera valutakurser för bokförda transaktioner till en extern tjänst.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 06/04/2019
ms.author: sgroespe
ms.openlocfilehash: 2958cf5dd124fd9437217214ea0df28944d07651
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621097"
---
# <a name="update-currency-exchange-rates"></a>Uppdatera valutakurser
Eftersom företag verkar i allt fler länder/regioner blir det alltmer viktigt att de kan använda och rapportera ekonomiska siffror i fler än en valuta. Du måste ange en kod för varje valuta du använder om du köper eller säljer i andra valutor än din lokala valuta, har tillgångar eller skulder i andra valutor eller registrerar transaktioner i olika valutor.

Din redovisning ställs in för att använda den lokala valutan (BVA) men du kan ställa in en annan valuta med en tilldelad aktuell valutakurs. Genom att ange en andra valuta som en så kallad alternativ rapporteringsvaluta kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] registrera belopp automatiskt i både BVA och den alternativa rapporteringsvalutan för varje redovisningstransaktion och för andra transaktioner, t.ex. momstransaktioner. Mer information finns i [Ställa in en alternativ rapporteringsvaluta](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Justera valutakurser
Eftersom valutakurser ständigt fluktuerar måste alternativa valutavärden i systemet justeras med jämna mellanrum. Om dessa justeringar inte görs kan de belopp som har konverterats från utländska (eller alternativa) valutor och bokförts i huvudboken i BVA vara missvisande. Dessutom måste dagliga transaktioner som bokförs innan en daglig valutakurs har registrerats i programmet uppdateras efter det att den dagliga valutakursinformationen har registrerats.

Batch-jobbet **Justera valutakurser** används för att manuellt justera valutakurserna för bokförda kund-, leverantörs- och bankkontotransaktioner. Det kan även användas för att uppdatera belopp i alternativ rapporteringsvaluta för redovisningstransaktioner. Du kan också låta valutakurserna justeras automatiskt med hjälp av en tjänst. Mer information finns i [Så här konfigurerar du en valutakurstjänst](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

### <a name="effect-on-customers-and-vendors"></a>Påverkan på kunder och leverantörer
För kund- och leverantörskonton justeras valutan med hjälp av valutakursen från det bokföringsdatum som angetts i batchjobbet. I batch-jobbet beräknas skillnaderna för enskilda valutasaldon och beloppen bokförs på det redovisningskonto som angetts i fältet **Kursvinster väntade** eller **Kursförluster befarade** på sidan **Valutor**. Mottransaktioner bokförs automatiskt till redovisningens försäljnings-/inköpskonto.

Batch-jobbet behandlar alla öppna kundredovisningstransaktioner och leverantörstransaktioner. Om det finns valutakursdifferens i någon transaktion skapas i batch-jobbet en ny detaljerad kund- eller leverantörstransaktion som återger det justerade beloppet på kund- eller leverantörstransaktionen.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensioner på kund-/leverantörstransaktioner
Justeringstransaktionerna tilldelas dimensioner från kund-/leverantörsreskontratransaktionerna, och justeringarna bokförs per kombination av dimensionsvärden.

### <a name="effect-on-bank-accounts"></a>Påverkan på bankkonton
För bankkonton justerar batchjobbet valutan efter valutakursen på det bokföringsdatum som angetts i batchjobbet. I batch-jobbet beräknas skillnaderna för varje bankkonto med valutakod och beloppen bokförs på det redovisningskonto som angetts i fältet **Kursvinster konstaterade** eller **Kursförluster konstaterade** på sidan **Valutor**. Mottransaktioner bokförs automatiskt på de redovisningsbankkonton som angetts i bankkontobokföringsmallarna. Batch-jobbet beräknar en transaktion per valuta per bokföringsmall.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensioner för bankkontotransaktioner
Justeringstransaktionerna för bankkontots redovisningskonto och för vinst-/förlustkontot tilldelas bankkontots standarddimensioner.

### <a name="effect-on-gl-accounts"></a>Påverkan på redovisningskonton
Om du bokför i alternativ rapporteringsvaluta kan du låta nya redovisningstransaktioner för valutajusteringar mellan BVA och den alternativa rapporteringsvalutan skapas i batch-jobbet. I batch-jobbet beräknas differenser för varje redovisningstransaktion och redovisningstransaktionen justeras enligt innehållet i fältet **Valutakursjustering** för varje redovisningskonto.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensioner för redovisningskontotransaktioner
Justeringstransaktionerna tilldelas dimensioner från de redovisningskonton de bokförs på.

> [!Important]
> Innan du kan använda batchjobbet måste du ange de valutakurser som ska användas vid justering av de utländska valutasaldona. Du gör det med sidan **valutakurser**.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Så här konfigurerar du en valutakurstjänst
Du kan använda en extern tjänst, till exempel FloatRates, för kontinuerlig uppdatering av aktuella valutakurser.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Valutakurstjänster** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På sidan **Valutakurstjänster** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj kryssrutan **aktiverad** om du vill aktivera tjänsten.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Så här uppdaterar du valutakurser från en tjänst
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Valutor** och välj sedan relaterad länk.
2. Välj åtgärden **uppdatera valutakurser**.

Värdet i fältet **valutakurs** på sidan **valutor** uppdateras med den senaste valutakursen.

## <a name="see-also"></a>Se även
[Ställa in en alternativ rapporteringsvaluta.](finance-how-setup-additional-currencies.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
