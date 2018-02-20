---
title: "Så här begränsar och tillåter du användning av en post | Microsoft Docs"
description: "Om du vill begränsa en post från att användas i vissa aktiviteter, till exempel tills posten har godkänts, kan du inkorporera två arbetsflödessvar i ett arbetsflöde som kontrollerar användningen av posten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4636cdedc2c99d1aa7cfc2dc361f7135aa3c4199
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="06eb9-103">Begränsa och tillåt användningen av en post</span><span class="sxs-lookup"><span data-stu-id="06eb9-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="06eb9-104">Om du vill begränsa en post från att användas i vissa aktiviteter, till exempel tills posten har godkänts, kan du inkorporera två arbetsflödessvar i ett arbetsflöde som kontrollerar användningen av posten.</span><span class="sxs-lookup"><span data-stu-id="06eb9-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="06eb9-105">Ett arbetsflödessvar ska begränsa användningen av posten enligt definitionen i arbetsflödeshändelsen och villkoren.</span><span class="sxs-lookup"><span data-stu-id="06eb9-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="06eb9-106">Ett annat arbetsflödessvar ska tillåta användning av posten enligt definitionen i arbetsflödeshändelsen och villkoren.</span><span class="sxs-lookup"><span data-stu-id="06eb9-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="06eb9-107">Två svar finns i den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] för detta ändamål: **Tillåt användning av en post**</span><span class="sxs-lookup"><span data-stu-id="06eb9-107">Two responses exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="06eb9-108">och **tillåt användningen av en post.**.</span><span class="sxs-lookup"><span data-stu-id="06eb9-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="06eb9-109">Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] erbjuder stöd för att begränsa en post från att bokföras, från att exporteras som en utbetalning och från att skrivas ut som en check.</span><span class="sxs-lookup"><span data-stu-id="06eb9-109">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="06eb9-110">För att stödja andra begränsningar måste en Microsoft-partner anpassa programkoden.</span><span class="sxs-lookup"><span data-stu-id="06eb9-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="06eb9-111">Arbetsflödesfunktionen för att begränsa och tillåta poster att användas är inte relaterad till funktionen att spärra artikel-, kund- och leverantörsposter från att bokföras.</span><span class="sxs-lookup"><span data-stu-id="06eb9-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="06eb9-112">Följande procedur beskriver hur du begränsar inköpsorder från att bokföras tills de har godkänts.</span><span class="sxs-lookup"><span data-stu-id="06eb9-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="06eb9-113">Det nya arbetsflödet baseras på det befintliga arbetsflödesmallen Arbetsflöde för godkännande av inköpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="06eb9-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="06eb9-114">Så här skapar du ett arbetsflödessteg som begränsar bokföring av icke godkända inköpsorder</span><span class="sxs-lookup"><span data-stu-id="06eb9-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="06eb9-115">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="06eb9-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="06eb9-116">I fönstret **Arbetsflöden** skapar du ett nytt arbetsflöde som kallas Arbetsflöde för godkännande av inköpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="06eb9-116">In the **Workflows** window, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="06eb9-117">Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="06eb9-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="06eb9-118">Välj åtgärden **Kopiera från arbetsflödesmallen**.</span><span class="sxs-lookup"><span data-stu-id="06eb9-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="06eb9-119">Välj fältet **Källarbetsflödekod** och välj sedan i fönstret **arbetsflödesmallen**, välj arbetsflödesmallen Arbetsflöde för godkännande av inköpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="06eb9-119">Choose the **Source Workflow Code** field, and then, in the **Workflow Templates** window, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="06eb9-120">Lägg märke till att de första två arbetsflödesstegen är om du vill begränsa och sedan tillåta användning av inköpsfakturor.</span><span class="sxs-lookup"><span data-stu-id="06eb9-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="06eb9-121">Fortsätt genom att ändra händelsevillkoret i det första steget i det nya arbetsflödet för att ange att det gäller inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="06eb9-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="06eb9-122">På snabbfliken **Arbetsflödessteg** väljer du fältet **Händelsevillkor** och sedan för filtret **Dokumenttyp**, välj **Order**.</span><span class="sxs-lookup"><span data-stu-id="06eb9-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="06eb9-123">Fortsätt med att redigera, ta bort eller lägga till andra arbetsflödessteg så att de passar en affärsprocess som börjar med att begränsa så att icke godkända inköpsorder bokförs.</span><span class="sxs-lookup"><span data-stu-id="06eb9-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="06eb9-124">Se även</span><span class="sxs-lookup"><span data-stu-id="06eb9-124">See Also</span></span>  
<span data-ttu-id="06eb9-125">[Skapa arbetsflöden](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="06eb9-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="06eb9-126">Arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="06eb9-126">Workflow</span></span>](across-workflow.md)   

