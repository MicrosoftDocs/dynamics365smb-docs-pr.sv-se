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
ms.openlocfilehash: 9d0058c707862144592278d08a494175adf67a2a
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115442"
---
# <a name="setting-up-purchasing"></a><span data-ttu-id="3f320-103">Ställa in inköp</span><span class="sxs-lookup"><span data-stu-id="3f320-103">Setting Up Purchasing</span></span>
<span data-ttu-id="3f320-104">Innan du kan hantera inköpsprocesser måste du konfigurera reglerna och värdena som definierar företagets inköpspolicyer.</span><span class="sxs-lookup"><span data-stu-id="3f320-104">Before you can manage purchase processes, you must configure the rules and values that define the company's purchase policies.</span></span>

<span data-ttu-id="3f320-105">Du måste ställa in de allmänna inställningarna, till exempel vilka inköpsdokument som är obligatoriska och hur deras värden ska bokföras.</span><span class="sxs-lookup"><span data-stu-id="3f320-105">You must define the general setup, such as which purchase documents are required and how their values are posted.</span></span> <span data-ttu-id="3f320-106">Dessa allmänna inställningar görs vanligtvis bara en gång, under den initiala implementeringen.</span><span class="sxs-lookup"><span data-stu-id="3f320-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="3f320-107">En separat serie uppgifter relaterade till att registrera nya leverantörer är att registrera alla specialpriser eller rabattavtal som du har med varje leverantör.</span><span class="sxs-lookup"><span data-stu-id="3f320-107">A separate series of tasks related to registering new vendors is to record any special price or discount agreements that you have with each vendor.</span></span>

<span data-ttu-id="3f320-108">Finansrelaterade inköp, till exempel betalningssätt och valutor, beskrivs i avsnittet Finans.</span><span class="sxs-lookup"><span data-stu-id="3f320-108">Finance-related purchase setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="3f320-109">Mer information finns i [Konfigurera ekonomi](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="3f320-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="3f320-110">Om du vill</span><span class="sxs-lookup"><span data-stu-id="3f320-110">To</span></span> | <span data-ttu-id="3f320-111">Gå till</span><span class="sxs-lookup"><span data-stu-id="3f320-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="3f320-112">Skapa ett leverantörskort för varje leverantör som du har köpt av</span><span class="sxs-lookup"><span data-stu-id="3f320-112">Create a vendor card for each vendor that you purchase from</span></span>|[<span data-ttu-id="3f320-113">Registrera nya leverantörer</span><span class="sxs-lookup"><span data-stu-id="3f320-113">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md) |
| <span data-ttu-id="3f320-114">Ange de olika rabatterna och specialpriserna som leverantörerna beviljar dig beroende på artikel, kvantitet och/eller datum</span><span class="sxs-lookup"><span data-stu-id="3f320-114">Enter the different discounts and special prices that vendors grant you depending on item, quantities, and/or date</span></span> |[<span data-ttu-id="3f320-115">Registrera inköpspris, rabatt och betalningsavtal</span><span class="sxs-lookup"><span data-stu-id="3f320-115">Record Purchase Price, Discount, and Payment Agreements</span></span>](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| <span data-ttu-id="3f320-116">Prioritera leverantörer</span><span class="sxs-lookup"><span data-stu-id="3f320-116">Prioritize vendors</span></span> |[<span data-ttu-id="3f320-117">Prioritera leverantörer</span><span class="sxs-lookup"><span data-stu-id="3f320-117">Prioritize Vendors</span></span>](purchasing-how-prioritize-vendors.md) |
| <span data-ttu-id="3f320-118">Konfigurera inköpare</span><span class="sxs-lookup"><span data-stu-id="3f320-118">Set up purchasers</span></span> |[<span data-ttu-id="3f320-119">Konfigurera inköpare</span><span class="sxs-lookup"><span data-stu-id="3f320-119">Set Up Purchasers</span></span>](purchasing-how-setup-purchasers.md) |
|<span data-ttu-id="3f320-120">Ange standardrapporter som ska användas för olika dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="3f320-120">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="3f320-121">Rapportval i Business Central</span><span class="sxs-lookup"><span data-stu-id="3f320-121">Report Selection in Business Central</span></span>](across-report-selections.md)|

> [!TIP]
> <span data-ttu-id="3f320-122">Beroende på ditt geografiska läge kan vissa sidor innehålla fält som inte beskrivs i artiklarna som anges här, detta eftersom de gäller lokala funktioner eller anpassningar.</span><span class="sxs-lookup"><span data-stu-id="3f320-122">Depending on your geographical location, some pages can contain fields that are not described in the articles that are listed here because they apply to local functionality or customizations.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="external-document-number"></a><span data-ttu-id="3f320-123">Externt dokumentnummer</span><span class="sxs-lookup"><span data-stu-id="3f320-123">External document number</span></span>

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="3f320-124">Se Relaterad utbildning på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="3f320-124">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="3f320-125">Se även</span><span class="sxs-lookup"><span data-stu-id="3f320-125">See Also</span></span>

[<span data-ttu-id="3f320-126">Inköp</span><span class="sxs-lookup"><span data-stu-id="3f320-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="3f320-127">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3f320-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]