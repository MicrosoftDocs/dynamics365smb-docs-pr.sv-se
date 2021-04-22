---
title: Så här ställer du in inköpstransaktioner för tredje part från EU-land
description: EU trepartshandel sker när du tar emot en inköpsfaktura från en kund som finns i ett land eller en region inom EU och produkterna skickas till ett annat land eller en annan region inom EU utan att passera Sverige.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 34fd4dca2479d45c3eeda2d6ef48b99dca669b65
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776569"
---
# <a name="set-up-eu-third-party-purchase-transactions"></a>Ställa in treparts EU-inköpstransaktioner
EU trepartshandel sker när du tar emot en inköpsfaktura från en kund som finns i ett land eller en region inom EU och produkterna skickas till ett annat land eller en annan region inom EU utan att passera Sverige. Transaktionsbeloppet måste identifieras och rapporteras separat i enlighet med de svenska reglerna för momsrapportering och kraven för systemet för utbyte av mervärdesskattedata (VAT Information Exchange System, VIES). [!INCLUDE[prod_short](../../includes/prod_short.md)] omfattar en svensk tilläggsfunktionalitet så att inköpstransaktioner kan ställas in som EU trepartshandel. Bokförda EU trepartstransaktioner kan då filtreras i momsrapporter och exkluderas från beloppet i kolumnen **Försäljning till kund** i rapporten **Moms- och kvartalsredovisning**.  

## <a name="to-set-up-eu-third-party-purchase-transactions"></a>Så här ställer du in EU trepartsinköpstransaktioner  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](../../media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsfakturor** och välj sedan tillhörande länk.  
2.  Välj en befintlig inköpsfakturan eller åtgärden **Nytt** för att skapa en ny.  
3.  I snabbfliken **Fakturadetaljer** markerar du kryssrutan **Treparts EU-handel**.  
4.  Välj knappen **OK**.  

## <a name="see-also"></a>Se även  
 [Rapportera moms till skattemyndigheterna](../../finance-how-report-vat.md)   
 [Lokal funktionalitet för Sverige](sweden-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]