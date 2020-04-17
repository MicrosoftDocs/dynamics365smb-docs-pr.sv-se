---
title: Så här ställer du in inköpstransaktioner för tredje part från EU-land
description: EU trepartshandel sker när du tar emot en inköpsfaktura från en kund som finns i ett land eller en region inom EU och produkterna skickas till ett annat land eller en annan region inom EU utan att passera Sverige.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1da645eb9d12eba5ac99b7b22605cc33f91ca40c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189151"
---
# <a name="set-up-eu-third-party-purchase-transactions"></a>Ställa in treparts EU-inköpstransaktioner
EU trepartshandel sker när du tar emot en inköpsfaktura från en kund som finns i ett land eller en region inom EU och produkterna skickas till ett annat land eller en annan region inom EU utan att passera Sverige. Transaktionsbeloppet måste identifieras och rapporteras separat i enlighet med de svenska reglerna för momsrapportering och kraven för systemet för utbyte av mervärdesskattedata (VAT Information Exchange System, VIES). [!INCLUDE[d365fin](../../includes/d365fin_md.md)] omfattar en svensk tilläggsfunktionalitet så att inköpstransaktioner kan ställas in som EU trepartshandel. Bokförda EU trepartstransaktioner kan då filtreras i momsrapporter och exkluderas från beloppet i kolumnen **Försäljning till kund** i rapporten **Moms- och kvartalsredovisning**.  

## <a name="to-set-up-eu-third-party-purchase-transactions"></a>Så här ställer du in EU trepartsinköpstransaktioner  

1.  Välj ikonen ![Söka efter sida eller rapport](../../media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **inköpsfakturor** och välj sedan relaterad länk.  
2.  Välj en befintlig inköpsfakturan eller åtgärden **Nytt** för att skapa en ny.  
3.  I snabbfliken **Fakturadetaljer** markerar du kryssrutan **Treparts EU-handel**.  
4.  Välj knappen **OK**.  

## <a name="see-also"></a>Se även  
 [Rapportera moms till skattemyndigheterna](../../finance-how-report-vat.md)   
 [Lokal funktionalitet för Sverige](sweden-local-functionality.md)
