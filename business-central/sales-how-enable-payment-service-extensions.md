---
title: "Aktivera kundbetalningar via betalningstjänster | Microsoft Docs"
description: "Gör det enklare för kunderna att betala sina fakturor genom att aktivera betalningstjänster."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5853080ef39196e95c293415e9b81502ff03d5ed
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="enable-customer-payments-through-payment-services"></a>Aktivera kundbetalningar via betalningstjänster
Som alternativ till att samla utbetalningar via banköverföring eller kreditkort, kan dina kunder betala via sina konton med betalningstjänster som t.ex. Microsoft Pay, PayPal, or WorldPay.  

När du har aktiverat en betalningstjänst i [!INCLUDE[d365fin](includes/d365fin_md.md)], är en länk till den här tjänsten tillgänglig på försäljningsdokument som du skickar med e-post till kunder. Kunder kan använda länken för att gå till betalningstjänsten och betala fakturan direkt från försäljningsdokumentet. Om du inte vill inkludera länken, exempelvis om en kund vill betala kontant, kan du ta bort betalningstjänsten från fakturan innan du bokför.  

Tilläggen Microsoft Pay, PayPal Payments Standard och WorldPay Payments Standard är installerade i [!INCLUDE[d365fin](includes/d365fin_md.md)], och klara att aktiveras.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Så här aktiverar du en betalningstjänst i [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Betalningstjänster** och välj sedan relaterad länk.  
2. I fönstret **Betalningstjänst** väljer du åtgärden **Ny**.  
3. Välj betalningstjänsten och stäng sedan fönstret.  
4. I fönstret **Betalningstjänst** väljer du åtgärden **Konfiguration**.  
5. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Stäng fönstret.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Välja en betalningstjänst för en försäljningsfaktura
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsfakturor** och välj sedan relaterad länk.  
2. Öppna den försäljningsfaktura som du vill betala med hjälp av betalningstjänsten.  
3. I fältet **Betalningtjänst** väljer du betalningtjänsten.  

    > [!NOTE]  
    > Fältet **betalningstjänst** är bara tillgängligt om du har aktiverat betalningstjänsten.  

## <a name="see-also"></a>Se även  
[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

