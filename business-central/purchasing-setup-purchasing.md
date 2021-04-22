---
title: Översikt över uppgifter för inställning av inköp | Microsoft Docs
description: Beskriver uppgifterna för att definiera företagets inköppolicyer och registrerar inköpsprocesserna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 81bbb013cba1039bfe6bb76e8489d5b8ed7c9831
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772510"
---
# <a name="setting-up-purchasing"></a><span data-ttu-id="b3670-103">Ställa in inköp</span><span class="sxs-lookup"><span data-stu-id="b3670-103">Setting Up Purchasing</span></span>
<span data-ttu-id="b3670-104">Innan du kan hantera inköpsprocesser måste du konfigurera reglerna och värdena som definierar företagets inköpspolicyer.</span><span class="sxs-lookup"><span data-stu-id="b3670-104">Before you can manage purchase processes, you must configure the rules and values that define the company's purchase policies.</span></span>

<span data-ttu-id="b3670-105">Du måste ställa in de allmänna inställningarna, till exempel vilka inköpsdokument som är obligatoriska och hur deras värden ska bokföras.</span><span class="sxs-lookup"><span data-stu-id="b3670-105">You must define the general setup, such as which purchase documents are required and how their values are posted.</span></span> <span data-ttu-id="b3670-106">Dessa allmänna inställningar görs vanligtvis bara en gång, under den initiala implementeringen.</span><span class="sxs-lookup"><span data-stu-id="b3670-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="b3670-107">En separat serie uppgifter relaterade till att registrera nya leverantörer är att registrera alla specialpriser eller rabattavtal som du har med varje leverantör.</span><span class="sxs-lookup"><span data-stu-id="b3670-107">A separate series of tasks related to registering new vendors is to record any special price or discount agreements that you have with each vendor.</span></span>

<span data-ttu-id="b3670-108">Finansrelaterade inköp, till exempel betalningssätt och valutor, beskrivs i avsnittet Finans.</span><span class="sxs-lookup"><span data-stu-id="b3670-108">Finance-related purchase setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="b3670-109">Mer information finns i [Konfigurera ekonomi](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="b3670-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="b3670-110">Om du vill</span><span class="sxs-lookup"><span data-stu-id="b3670-110">To</span></span> | <span data-ttu-id="b3670-111">Gå till</span><span class="sxs-lookup"><span data-stu-id="b3670-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="b3670-112">Skapa ett leverantörskort för varje leverantör som du har köpt av</span><span class="sxs-lookup"><span data-stu-id="b3670-112">Create a vendor card for each vendor that you purchase from</span></span>|[<span data-ttu-id="b3670-113">Registrera nya leverantörer</span><span class="sxs-lookup"><span data-stu-id="b3670-113">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md) |
| <span data-ttu-id="b3670-114">Ange de olika rabatterna och specialpriserna som leverantörerna beviljar dig beroende på artikel, kvantitet och/eller datum</span><span class="sxs-lookup"><span data-stu-id="b3670-114">Enter the different discounts and special prices that vendors grant you depending on item, quantities, and/or date</span></span> |[<span data-ttu-id="b3670-115">Registrera inköpspris, rabatt och betalningsavtal</span><span class="sxs-lookup"><span data-stu-id="b3670-115">Record Purchase Price, Discount, and Payment Agreements</span></span>](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| <span data-ttu-id="b3670-116">Prioritera leverantörer</span><span class="sxs-lookup"><span data-stu-id="b3670-116">Prioritize vendors</span></span> |[<span data-ttu-id="b3670-117">Prioritera leverantörer</span><span class="sxs-lookup"><span data-stu-id="b3670-117">Prioritize Vendors</span></span>](purchasing-how-prioritize-vendors.md) |
| <span data-ttu-id="b3670-118">Konfigurera inköpare</span><span class="sxs-lookup"><span data-stu-id="b3670-118">Set up purchasers</span></span> |[<span data-ttu-id="b3670-119">Konfigurera inköpare</span><span class="sxs-lookup"><span data-stu-id="b3670-119">Set Up Purchasers</span></span>](purchasing-how-setup-purchasers.md) |
|<span data-ttu-id="b3670-120">Ange standardrapporter som ska användas för olika dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="b3670-120">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="b3670-121">Rapportval i Business Central</span><span class="sxs-lookup"><span data-stu-id="b3670-121">Report Selection in Business Central</span></span>](across-report-selections.md)|

> [!TIP]
> <span data-ttu-id="b3670-122">Beroende på ditt geografiska läge kan vissa sidor innehålla fält som inte beskrivs i artiklarna som anges här, detta eftersom de gäller lokala funktioner eller anpassningar.</span><span class="sxs-lookup"><span data-stu-id="b3670-122">Depending on your geographical location, some pages can contain fields that are not described in the articles that are listed here because they apply to local functionality or customizations.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="b3670-123">Se Relaterad utbildning på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="b3670-123">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="b3670-124">Se även</span><span class="sxs-lookup"><span data-stu-id="b3670-124">See Also</span></span>

[<span data-ttu-id="b3670-125">Inköp</span><span class="sxs-lookup"><span data-stu-id="b3670-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b3670-126">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b3670-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]