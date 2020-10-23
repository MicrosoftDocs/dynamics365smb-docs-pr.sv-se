---
title: Redigera bokförda försäljnings- och inköpsdokument | Microsoft Docs
description: Lära dig olika bokföringsfunktioner för att bokföra inköpsdokument och hur du kan uppdatera bokförda dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: eedfa2a0c0f519f5ea22eb51a779f6f2a090d9bf
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914345"
---
# <a name="edit-posted-documents"></a><span data-ttu-id="23865-103">Redigera bokförda dokument</span><span class="sxs-lookup"><span data-stu-id="23865-103">Edit Posted Documents</span></span>

<span data-ttu-id="23865-104">Ibland måste du uppdatera ett bokfört dokument eftersom information som är relevant för dokumentet har ändrats.</span><span class="sxs-lookup"><span data-stu-id="23865-104">Sometimes you have to update a posted document because information that is relevant to the document has changed.</span></span> <span data-ttu-id="23865-105">I ett bokfört försäljningsdokument kan exempel speditörens godsupplysningsnummer finnas.</span><span class="sxs-lookup"><span data-stu-id="23865-105">On a posted sales document, this can be the shipping agent's package tracking number, for example.</span></span> <span data-ttu-id="23865-106">I ett bokfört inköpsdokument kan det finnas en text för betalningsreferens.</span><span class="sxs-lookup"><span data-stu-id="23865-106">On a posted purchase document, this can be a payment reference text.</span></span>

<span data-ttu-id="23865-107">Du utför ändringen i en redigerbar version av det ursprungliga dokumentet, vilket anges med "**- Uppdatera**" i sidrubriken.</span><span class="sxs-lookup"><span data-stu-id="23865-107">You perform the change on an editable version of the original document, indicated by "**- Update**" in the page title.</span></span> <span data-ttu-id="23865-108">Sidan innehåller en delmängd av fälten som finns ursprungsdokumentet, varav vissa är icke-redigerbara fält som bara visas i informationssyfte.</span><span class="sxs-lookup"><span data-stu-id="23865-108">The page contains a subset of the fields on the original document, of which some are non-editable fields that are shown for information only.</span></span>

<span data-ttu-id="23865-109">Funktionen är tillgänglig för följande dokument på alla marknader som stöds:</span><span class="sxs-lookup"><span data-stu-id="23865-109">The functionality is available for the following documents across all supported markets:</span></span>

- <span data-ttu-id="23865-110">Bokförd utleverans</span><span class="sxs-lookup"><span data-stu-id="23865-110">Posted Sales Shipment</span></span>
- <span data-ttu-id="23865-111">Bokförd inköpsfaktura</span><span class="sxs-lookup"><span data-stu-id="23865-111">Posted Purchase Invoice</span></span>
- <span data-ttu-id="23865-112">Bokförd returutleverans</span><span class="sxs-lookup"><span data-stu-id="23865-112">Posted Return Shipment</span></span>
- <span data-ttu-id="23865-113">Bokförd returinlevns</span><span class="sxs-lookup"><span data-stu-id="23865-113">Posted Return Receipt</span></span>

<span data-ttu-id="23865-114">Följande ytterligare dokument kan redigeras i de angivna länderna eller regionerna:</span><span class="sxs-lookup"><span data-stu-id="23865-114">The following additional documents can be edited in the specified countries or regions:</span></span>

- <span data-ttu-id="23865-115">ES: Bokförd försäljningsfaktura, Bokförd försäljningskreditnota, Bokförd inköpsfaktura, Bokförd inköpskreditnota</span><span class="sxs-lookup"><span data-stu-id="23865-115">ES: Posted Sales Invoice, Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="23865-116">APAC: Bokförd försäljningskreditnota, bokförd inköpskreditnota</span><span class="sxs-lookup"><span data-stu-id="23865-116">APAC: Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="23865-117">RU: Bokförd försäljningskreditnota</span><span class="sxs-lookup"><span data-stu-id="23865-117">RU: Posted Sales Credit Memo</span></span>
- <span data-ttu-id="23865-118">IT: Bokförd överföringsutleverans, Bokförd serviceleverans</span><span class="sxs-lookup"><span data-stu-id="23865-118">IT: Posted Transfer Shipment, Posted Service Shipment</span></span>

## <a name="to-edit-a-posted-sales-shipment"></a><span data-ttu-id="23865-119">Så här redigerar du en bokförd försäljningsutleverans</span><span class="sxs-lookup"><span data-stu-id="23865-119">To edit a posted sales shipment</span></span>

<span data-ttu-id="23865-120">Här följer en beskrivning av hur du redigerar en bokförd försäljningsutleverans.</span><span class="sxs-lookup"><span data-stu-id="23865-120">The following explains how to edit a posted sales shipment.</span></span> <span data-ttu-id="23865-121">Stegen är liknande för de övriga dokument som stöds.</span><span class="sxs-lookup"><span data-stu-id="23865-121">The steps are similar for the other supported documents.</span></span>

1. <span data-ttu-id="23865-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda försäljningsutleveranser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="23865-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipments**, and then choose the related link.</span></span>
2. <span data-ttu-id="23865-123">Markera dokumentet som du vill redigera och välj åtgärden **Uppdatera dokument**.</span><span class="sxs-lookup"><span data-stu-id="23865-123">Select the document that you want to edit, and then choose the **Update Document** action.</span></span> <span data-ttu-id="23865-124">Du kan också öppna dokumentet och välja åtgärden.</span><span class="sxs-lookup"><span data-stu-id="23865-124">Alternatively, open the document and then choose the action.</span></span>
3. <span data-ttu-id="23865-125">På sidan **Bokförd försäljningsutleverans - Uppdatera** redigerar du fältet för **Godsupplysningsnr**</span><span class="sxs-lookup"><span data-stu-id="23865-125">On the **Posted Sales Shipment - Update** page, edit the **Package Tracking No.**</span></span> <span data-ttu-id="23865-126">till exempel.</span><span class="sxs-lookup"><span data-stu-id="23865-126">field, for example.</span></span>
4. <span data-ttu-id="23865-127">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="23865-127">Choose the **OK** button.</span></span>

<span data-ttu-id="23865-128">Den bokförda försäljningsutleveransen uppdateras.</span><span class="sxs-lookup"><span data-stu-id="23865-128">The posted sales shipment is updated.</span></span>

## <a name="see-also"></a><span data-ttu-id="23865-129">Se även</span><span class="sxs-lookup"><span data-stu-id="23865-129">See Also</span></span>

[<span data-ttu-id="23865-130">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="23865-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
[<span data-ttu-id="23865-131">Inköp</span><span class="sxs-lookup"><span data-stu-id="23865-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="23865-132">Bokför dokument och journaler</span><span class="sxs-lookup"><span data-stu-id="23865-132">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="23865-133">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="23865-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
