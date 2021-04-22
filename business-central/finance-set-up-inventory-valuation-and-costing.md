---
title: Ställa in lagervärdering och lagerkostnad | Microsoft Docs
description: I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2194a29247b6ec3c2ee87dfbfe6631f433d0514e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783728"
---
# <a name="setting-up-inventory-valuation-and-costing"></a>Ställa in lagervärdering och lagerkostnad

Om du vill se till att lagerkostnaderna registreras korrekt, ställer du in olika fält och sidor innan du gör artikeltransaktioner. Vanligtvis väljer företag en specifik värderingsprincip och tillämpar den på lagerartiklar, till exempel för att hjälpa dem att spåra värdet av artiklar i lager.  

> [!TIP]
> En introduktion till kostnadsredovisning i [!INCLUDE [prod_short](includes/prod_short.md)] finns i [Om lagerkostnadsredovisning](finance-learn-about-costing.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

|**Om du vill**|**Se**|  
|------------|-------------|
|Ange en värderingsprincip som företaget använder som standard för att styra hur dess ingående kostnad används för att fastställa lagervärde och kostnaden för sålda varor.|[Ställa in allmän lagerinformation](inventory-how-setup-general.md)|  
|Ange en värderingsprincip för enskilda artiklar om de kräver en annan värderingsprincip.|[Registrera nya artiklar](inventory-how-register-new-items.md)|  
|se till att kostnaden automatiskt bokförs i redovisningen när en lagertransaktion bokförs.|Fältet **Automatisk kostnadsbokföring** på sidan **Lagerinställning**|  
|se till att förväntade kostnader bokförs i redovisningen så att du från de interima redovisningskontona Fkan se en uppskattning av beloppen som förfaller till betalning och kostnaden för de köpta eller sålda artiklarna innan de faktiskt faktureras.|Fältet **Förväntad kost.bokf. i redov.** på sidan **Lagerinställning**|  
|ställa in systemet till att automatiskt justera för alla kostnadsändringar varje gång du bokför lagertransaktioner.|[Justera artikelkostnader](inventory-how-adjust-item-costs.md)|  
|Definiera om genomsnittskostnaden ska beräknas endast per artikel eller per artikel för varje lagerställeenhet och för varje variant av artikeln.|Fältet **Genoms. kost.ber.typ** på sidan **Lagerinställningar**|  
|välja den tidsperiod som ska användas för att beräkna vägd genomsnittskostnad för de artiklar som du använder genomsnittsvärderingsprincipen för.|Fältet **Genomsnittskostnadsperiod** på sidan **Lagerinställningar**|  
|definiera lagerperioder för att kontrollera lagervärde över tid genom att inaktivera transaktionsbokföring i avslutade lagerperioder.|[Arbeta med lagerperioder](finance-how-to-work-with-inventory-periods.md)|  
|se till att försäljningsreturer kopplas till den ursprungliga utgående transaktionen så att lagervärdet bevaras.|**Exakt kostnadsåterföring** på sidan **Försäljning & kundreskontra**|  
|se till att inköpsreturer kopplas till den ursprungliga inkommande transaktionen så att lagervärdet bevaras.|**Exakt kostnadsåterföring** på sidan **Inköp & Leverantörsreskontra**|
|ange avrundningsreglerna som ska användas när artikelpriser justeras eller föreslås och när standardkostnader justeras eller föreslås.|Sidan **Avrundningsmetod**|  

## <a name="see-also"></a>Se även

[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Ställa in allmän lagerinformation](inventory-how-setup-general.md)  
[Stämma av lagerkostnader med redovisningen](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Lägga upp bästa praxis: Värderingsprincip](setup-best-practices-costing-method.md)  
[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)  
[Designinformation: ändra värderingsprinciper för artiklar](design-details-changing-costing-methods.md)  
[Arbeta med Business Central](ui-work-product.md)  
[Ekonomi](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]