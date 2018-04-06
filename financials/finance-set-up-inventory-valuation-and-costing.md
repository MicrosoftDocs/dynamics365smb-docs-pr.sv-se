---
title: "Ställa in lagervärdering och lagerkostnad | Microsoft Docs"
description: "I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6d1d0da42bbc6bf186845648552eb639731759f
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Ställa in lagervärdering och lagerkostnad
Om du vill se till att lagerkostnaderna registreras korrekt, ställer du in olika fält och fönster innan du gör artikeltransaktioner.

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|ange en värderingsprincip för varje artikel för att styra hur dess ingående kostnad används för att fastställa lagervärde och kostnaden för sålda varor.|[Registrera nya artiklar](inventory-how-register-new-items.md)|  
|se till att kostnaden automatiskt bokförs i redovisningen när en lagertransaktion bokförs.|Fältet **Automatisk kostnadsbokföring** på sidan **Lagerinställning**|  
|se till att förväntade kostnader bokförs i redovisningen så att du från de interima redovisningskontona Fkan se en uppskattning av beloppen som förfaller till betalning och kostnaden för de köpta eller sålda artiklarna innan de faktiskt faktureras.|Fältet **Förväntad kost.bokf. i redov.** på sidan **Lagerinställning**|  
|ställa in systemet till att automatiskt justera för alla kostnadsändringar varje gång du bokför lagertransaktioner.|[Justera artikelkostnader](inventory-how-adjust-item-costs.md)|  
|definiera om genomsnittskostnaden ska beräknas endast per artikel eller per artikel för varje lagerställeenhet och för varje variant av artikeln.|Fältet **Genoms. kost.ber.typ** på sidan **Lagerinställningar**|  
|välja den tidsperiod som ska användas för att beräkna vägd genomsnittskostnad för de artiklar som du använder genomsnittsvärderingsprincipen för.|Fältet **Genomsnittskostnadsperiod** på sidan **Lagerinställningar**|  
|definiera lagerperioder för att kontrollera lagervärde över tid genom att inaktivera transaktionsbokföring i avslutade lagerperioder.|[Arbeta med lagerperioder](finance-how-to-work-with-inventory-periods.md)|  
|se till att försäljningsreturer kopplas till den ursprungliga avgående transaktionen så att lagervärdet bevaras.|**Exakt kostnadsåterföring** på sidan **Försäljning & kundreskontra**|  
|se till att inköpsreturer kopplas till den ursprungliga ankommande transaktionen så att lagervärdet bevaras.|**Exakt kostnadsåterföring** på sidan **Inköp & Leverantörsreskontra**|
|ange avrundningsreglerna som ska användas när artikelpriser justeras eller föreslås och när standardkostnader justeras eller föreslås.|Sidan **Avrundningsmetod**|  

## <a name="see-also"></a>Se även  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Arbeta med Finance and Operations, Business edition](ui-work-product.md)  
[Ekonomi](finance.md)  

