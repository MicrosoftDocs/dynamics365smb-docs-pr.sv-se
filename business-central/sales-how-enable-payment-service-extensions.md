---
title: Aktivera kundbetalningar via betalningstjänster | Microsoft Docs
description: Gör det enklare för kunderna att betala sina fakturor genom att aktivera betalningstjänster.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7bd02b7d802faa3b0766d6689eaa223ba3e3573a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316458"
---
# <a name="enable-customer-payments-through-payment-services"></a>Aktivera kundbetalningar via betalningstjänster
Som alternativ till att samla utbetalningar via banköverföring eller kreditkort, kan dina kunder betala via sina konton med betalningstjänster som t.ex. Microsoft Pay, PayPal eller WorldPay.  

När du har aktiverat en betalningstjänst i [!INCLUDE[d365fin](includes/d365fin_md.md)], är en länk till den här tjänsten tillgänglig på försäljningsdokument som du skickar med e-post till kunder. Kunder kan använda länken för att gå till betalningstjänsten och betala fakturan direkt från försäljningsdokumentet. Om du inte vill inkludera länken, exempelvis om en kund vill betala kontant, kan du ta bort betalningstjänsten från fakturan innan du bokför.  

Tilläggen Microsoft Pay, PayPal Payments Standard och WorldPay Payments Standard är installerade i [!INCLUDE[d365fin](includes/d365fin_md.md)] och klara att aktiveras.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365fin_mdmd"></a>Så här aktiverar du en betalningstjänst i [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Betalningstjänster** och välj sedan relaterad länk.  
2. På sidan **Betalningstjänst** väljer du åtgärden **Ny**.  
3. Välj betalningstjänsten och stäng sedan sidan.  
4. På sidan **Betalningstjänst** väljer du åtgärden **Installation**.  
5. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Stäng sidan.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Välja en betalningstjänst för en försäljningsfaktura
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Försäljningsfakturor** och välj sedan relaterad länk.  
2. Öppna den försäljningsfaktura som du vill betala med hjälp av betalningstjänsten.  
3. I fältet **Betalningtjänst** väljer du betalningtjänsten.  

    > [!NOTE]  
    > Fältet **betalningstjänst** är bara tillgängligt om du har aktiverat betalningstjänsten.  

## <a name="see-also"></a>Se även  
[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
