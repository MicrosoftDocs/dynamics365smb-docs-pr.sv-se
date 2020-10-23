---
title: Tillägg för skicka kundremissa | Microsoft Docs
description: Beskriver tillägget för skicka kundremissa som möjliggör e-post och skicka om kundremissa från betalningsjournalen och leverantörsreskontratransaktionerna.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f6afaa9ade29c955033914b608806c3fb0f5a310
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912227"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="4a071-103">Skicka kundremissa</span><span class="sxs-lookup"><span data-stu-id="4a071-103">Send Remittance Advice</span></span>

<span data-ttu-id="4a071-104">När kundremissa används för att meddela leverantörerna om de betalningar som görs kan du nu skicka kundremissa i bulk från betalningsjournalen och skicka om när du har utfört betalningar från leverantörsreskontratransaktioner genom att använda dokumentutskicksprofiler.</span><span class="sxs-lookup"><span data-stu-id="4a071-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="4a071-105">Denna funktion stöds endast i Business Central online och lokalt i följande länder: Storbritannien, USA, Kanada, Australien, Nya Zeeland och Sydafrika.</span><span class="sxs-lookup"><span data-stu-id="4a071-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="4a071-106">Du kan skicka kundremissa på två olika sätt:</span><span class="sxs-lookup"><span data-stu-id="4a071-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="4a071-107">Gå till sidan **Utbetalningsjournal** och välj **Relaterat**, **Betalningar**, **Skicka kundremissa** för att skicka kundremissa via e-post för en eller flera utbetalningsjournaltyper</span><span class="sxs-lookup"><span data-stu-id="4a071-107">In the **Payment Journal** page, choose **Related**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="4a071-108">På sidan **leverantörsreskontratransaktioner** välj **åtgärder**, **funktioner**, **skicka kundremissa** via e-post efter bokföring av leverantörsbetalningar, för en av flera leverantörsreskontratransaktioner</span><span class="sxs-lookup"><span data-stu-id="4a071-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="4a071-109">Se även</span><span class="sxs-lookup"><span data-stu-id="4a071-109">See Also</span></span>

[<span data-ttu-id="4a071-110">Betalningsförslag för lev.</span><span class="sxs-lookup"><span data-stu-id="4a071-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="4a071-111">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="4a071-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="4a071-112">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4a071-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4a071-113">Skicka dokument via e-post</span><span class="sxs-lookup"><span data-stu-id="4a071-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
