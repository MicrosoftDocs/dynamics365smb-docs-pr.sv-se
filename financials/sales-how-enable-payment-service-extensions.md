---
title: "Så här aktiverar du kundbetalningar via betalningstjänster | Microsoft Docs"
description: "Gör det enklare för kunderna att betala sina fakturor genom att aktivera betalningstjänster."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 04/24/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 769fd885e5c6070f8a4f6c9082900ea7f5f6ab8d
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-enable-customer-payments-through-payment-services"></a>Så här aktiverar du kundbetalningar via betalningstjänster
Som alternativ till att samla utbetalningar via banköverföring eller kreditkort, kan dina kunder betala via sina konton med betalningstjänster som t.ex. PayPal eller WorldPay.  

När du har aktiverat en betalningstjänst i [!INCLUDE[d365fin](includes/d365fin_md.md)], är en länk till den här tjänsten tillgänglig på försäljningsdokument som du skickar med e-post till kunder. Kunder kan använda länken för att gå till betalningstjänsten och betala fakturan direkt från försäljningsdokumentet. Om du inte vill inkludera länken, exempelvis om en kund vill betala kontant, kan du ta bort betalningstjänsten från fakturan innan du bokför.  

Tilläggen PayPal Payments Standard och WorldPay Payments Standard är installerade i [!INCLUDE[d365fin](includes/d365fin_md.md)], och klara att aktiveras.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Så här aktiverar du en betalningstjänst i [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Betalningstjänster**, och väljer sedan relaterad länk.  
2. I fönstret **Betalningstjänst** väljer du åtgärden **Ny**.  
3. Välj betalningstjänsten och stäng sedan fönstret.  
4. I fönstret **Betalningstjänst** väljer du åtgärden **Konfiguration**.  
5. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Stäng fönstret.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Välj en betalningstjänst för en försäljningsfaktura
1. Välj åtgärden **Försäljningsfakturor** på startsidan.  
2. Öppna den försäljningsorder som du vill betala med hjälp av betalningstjänsten.  
3. I fältet **Betalningtjänst** väljer du betalningtjänsten.  
  
    **Obs!** Fältet **betalningstjänst** är bara tillgängligt om du har aktiverat betalningstjänsten.  

## <a name="see-also"></a>Se även  
[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]med tillägg](ui-extensions.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

