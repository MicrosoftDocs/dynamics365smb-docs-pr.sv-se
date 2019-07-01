---
title: Tillägg för skicka kundremissa | Microsoft Docs
description: Beskriver tillägget för skicka kundremissa som möjliggör e-post och skicka om kundremissa från betalningsjournalen och leverantörsreskontratransaktionerna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 06/06/2019
ms.author: sgroespe
ms.openlocfilehash: 9caa026f9edec42e56a035cf8d99228ca18c3c36
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621258"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="f7917-103">Skicka kundremissa</span><span class="sxs-lookup"><span data-stu-id="f7917-103">Send Remittance Advice</span></span>
<span data-ttu-id="f7917-104">När kundremissa används för att meddela leverantörerna om de betalningar som görs kan du nu skicka kundremissa i bulk från betalningsjournalen och skicka om när du har utfört betalningar från leverantörsreskontratransaktioner genom att använda dokumentutskicksprofiler.</span><span class="sxs-lookup"><span data-stu-id="f7917-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="f7917-105">Denna funktion stöds endast i Business Central online och lokalt i följande länder: Storbritannien, USA, Kanada, Australien, Nya Zeeland och Sydafrika.</span><span class="sxs-lookup"><span data-stu-id="f7917-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="f7917-106">Du kan skicka kundremissa på två olika sätt:</span><span class="sxs-lookup"><span data-stu-id="f7917-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="f7917-107">Gå till sidan **utbetalningsjournal** och välj **Navigera**, **betalningar**, **skicka kundremissa** för att skicka kundremissa via e-ost för en eller föera utbetalningsjournaltyper</span><span class="sxs-lookup"><span data-stu-id="f7917-107">In the **Payment Journal** page, choose **Navigate**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="f7917-108">På sidan **leverantörsreskontratransaktioner** väljer du åtgärder, funktioner, skicka kundremissa för att skicka kundremissa via e-post efter bokföring av leverantörsbetalningar, för en av flera leverantörsreskontratransaktioner</span><span class="sxs-lookup"><span data-stu-id="f7917-108">I the **Vendor Ledger Entries** page, choose Action, Functions, Send Remittance Advice to email remittance advice after posting of vendor payments, for one of multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="f7917-109">Se även</span><span class="sxs-lookup"><span data-stu-id="f7917-109">See Also</span></span>
[<span data-ttu-id="f7917-110">Betalningsförslag för lev.</span><span class="sxs-lookup"><span data-stu-id="f7917-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="f7917-111">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="f7917-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="f7917-112">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7917-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>