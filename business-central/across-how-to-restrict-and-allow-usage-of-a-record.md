---
title: Så här begränsar och tillåter du användning av en post | Microsoft Docs
description: Om du vill begränsa en post från att användas i vissa aktiviteter, till exempel tills posten har godkänts, kan du inkorporera två arbetsflödessvar i ett arbetsflöde som kontrollerar användningen av posten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbb22a00e878e8c4d75cb5fcdbcc27a28d9d22a4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783997"
---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="df93f-103">Begränsa och tillåt användningen av en post</span><span class="sxs-lookup"><span data-stu-id="df93f-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="df93f-104">Om du vill begränsa en post från att användas i vissa aktiviteter, till exempel tills posten har godkänts, kan du inkorporera två arbetsflödessvar i ett arbetsflöde som kontrollerar användningen av posten.</span><span class="sxs-lookup"><span data-stu-id="df93f-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="df93f-105">Ett arbetsflödessvar ska begränsa användningen av posten enligt definitionen i arbetsflödeshändelsen och villkoren.</span><span class="sxs-lookup"><span data-stu-id="df93f-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="df93f-106">Ett annat arbetsflödessvar ska tillåta användning av posten enligt definitionen i arbetsflödeshändelsen och villkoren.</span><span class="sxs-lookup"><span data-stu-id="df93f-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="df93f-107">Två svar finns i den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] för detta ändamål: **Tillåt användning av en post**</span><span class="sxs-lookup"><span data-stu-id="df93f-107">Two responses exist in the generic version of [!INCLUDE[prod_short](includes/prod_short.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="df93f-108">och **tillåt användningen av en post.**.</span><span class="sxs-lookup"><span data-stu-id="df93f-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="df93f-109">Den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] erbjuder stöd för att begränsa en post från att bokföras, från att exporteras som en utbetalning och från att skrivas ut som en check.</span><span class="sxs-lookup"><span data-stu-id="df93f-109">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="df93f-110">För att stödja andra begränsningar måste en Microsoft-partner anpassa programkoden.</span><span class="sxs-lookup"><span data-stu-id="df93f-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="df93f-111">Arbetsflödesfunktionen för att begränsa och tillåta poster att användas är inte relaterad till funktionen att spärra artikel-, kund- och leverantörsposter från att bokföras.</span><span class="sxs-lookup"><span data-stu-id="df93f-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="df93f-112">Följande procedur beskriver hur du begränsar inköpsorder från att bokföras tills de har godkänts.</span><span class="sxs-lookup"><span data-stu-id="df93f-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="df93f-113">Det nya arbetsflödet baseras på det befintliga arbetsflödesmallen Arbetsflöde för godkännande av inköpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="df93f-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="df93f-114">Så här skapar du ett arbetsflödessteg som begränsar bokföring av icke godkända inköpsorder</span><span class="sxs-lookup"><span data-stu-id="df93f-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="df93f-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="df93f-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="df93f-116">På sidan **Arbetsflöden** skapar du ett nytt arbetsflöde som kallas Arbetsflöde för godkännande av inköpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="df93f-116">On the **Workflows** page, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="df93f-117">Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="df93f-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="df93f-118">Välj åtgärden **Kopiera från arbetsflödesmallen**.</span><span class="sxs-lookup"><span data-stu-id="df93f-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="df93f-119">Välj fältet **Källarbetsflödekod** och välj sedan på sidan **arbetsflödesmallen**, välj arbetsflödesmallen Arbetsflöde för godkännande av inköpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="df93f-119">Choose the **Source Workflow Code** field, and then, on the **Workflow Templates** page, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="df93f-120">Lägg märke till att de första två arbetsflödesstegen är om du vill begränsa och sedan tillåta användning av inköpsfakturor.</span><span class="sxs-lookup"><span data-stu-id="df93f-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="df93f-121">Fortsätt genom att ändra händelsevillkoret i det första steget i det nya arbetsflödet för att ange att det gäller inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="df93f-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="df93f-122">På snabbfliken **Arbetsflödessteg** väljer du fältet **Händelsevillkor** och sedan för filtret **Dokumenttyp**, välj **Order**.</span><span class="sxs-lookup"><span data-stu-id="df93f-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="df93f-123">Fortsätt med att redigera, ta bort eller lägga till andra arbetsflödessteg så att de passar en affärsprocess som börjar med att begränsa så att icke godkända inköpsorder bokförs.</span><span class="sxs-lookup"><span data-stu-id="df93f-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="df93f-124">Se även</span><span class="sxs-lookup"><span data-stu-id="df93f-124">See Also</span></span>  
<span data-ttu-id="df93f-125">[Skapa arbetsflöden](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="df93f-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="df93f-126">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="df93f-126">Workflow</span></span>](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]