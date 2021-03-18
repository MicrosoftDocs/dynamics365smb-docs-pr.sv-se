---
title: Aktivera kundbetalningar via betalningstjänster | Microsoft Docs
description: Gör det enklare för kunderna att betala sina fakturor genom att aktivera betalningstjänster.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5fa58c177629fdf386bca0ebfce2b668a55cbc8f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393355"
---
# <a name="enable-customer-payments-through-payment-services"></a>Aktivera kundbetalningar via betalningstjänster
Som alternativ till att samla utbetalningar via banköverföring eller kreditkort, kan dina kunder betala via sina konton med betalningstjänster som t. ex. Microsoft Pay, PayPal eller WorldPay.  

När du har aktiverat en betalningstjänst i [!INCLUDE[prod_short](includes/prod_short.md)], är en länk till den här tjänsten tillgänglig på försäljningsdokument som du skickar med e-post till kunder. Kunder kan använda länken för att gå till betalningstjänsten och betala fakturan direkt från försäljningsdokumentet. Om du inte vill inkludera länken, exempelvis om en kund vill betala kontant, kan du ta bort betalningstjänsten från fakturan innan du bokför.  

Tilläggen Microsoft Pay, PayPal Payments Standard och WorldPay Payments Standard är installerade i [!INCLUDE[prod_short](includes/prod_short.md)] och klara att aktiveras.  

## <a name="to-enable-a-payment-service-in-prod_short"></a>Så här aktiverar du en betalningstjänst i [!INCLUDE[prod_short](includes/prod_short.md)]
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Betalningstjänster** och välj sedan tillhörande länk.  
2. På sidan **Betalningstjänst** väljer du åtgärden **Ny**.  
3. Välj betalningstjänsten och stäng sedan sidan.  
4. På sidan **Betalningstjänst** väljer du åtgärden **Installation**.  
5. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Stäng sidan.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Välja en betalningstjänst för en försäljningsfaktura
1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsfakturor** och välj sedan relaterad länk.  
2. Öppna den försäljningsfaktura som du vill betala med hjälp av betalningstjänsten.  
3. I fältet **Betalningtjänst** väljer du betalningtjänsten.  

    > [!NOTE]  
    > Fältet **betalningstjänst** är bara tillgängligt om du har aktiverat betalningstjänsten.  

## <a name="see-also"></a>Se även  
[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]