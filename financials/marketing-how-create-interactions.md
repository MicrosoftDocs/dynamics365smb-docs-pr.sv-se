---
title: "Skapa interaktioner på kontakter och segment | Microsoft Docs"
description: "Beskriver hur du kan skapa interaktioner för den kommunikation som du har med dina kontakter och segment i Dynamics 365, till exempel direktreklam."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/15/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 57cbc08ab2e05777fae54018fe714d44b64d14e0
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-interactions-on-contacts-and-segments"></a><span data-ttu-id="44fbe-103">Så här skapar du interaktioner på kontakter och segment</span><span class="sxs-lookup"><span data-stu-id="44fbe-103">How to: Create Interactions on Contacts and Segments</span></span>
<span data-ttu-id="44fbe-104">Du kan skapa interaktioner för att registrera all interaktion och kommunikation som du har med dina kontakter och segment, till exempel direktreklam.</span><span class="sxs-lookup"><span data-stu-id="44fbe-104">You can create interactions to record all the interactions and communications you have with your contacts and segments, for example, direct mail.</span></span>

<span data-ttu-id="44fbe-105">Innan du skapar interaktioner måste du lägga upp interaktionsmallar.</span><span class="sxs-lookup"><span data-stu-id="44fbe-105">Before you create interactions, you must set up interaction templates.</span></span> <span data-ttu-id="44fbe-106">Mer information finns i  [Skapa interaktionsmallar](marketing-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="44fbe-106">For more information, see  [Set Up Interaction Templates](marketing-interactions.md).</span></span>

## <a name="to-create-an-interaction"></a><span data-ttu-id="44fbe-107">Skapa interaktioner så här</span><span class="sxs-lookup"><span data-stu-id="44fbe-107">To create an interaction</span></span>
1. <span data-ttu-id="44fbe-108">Öppna kontakten, säljaren eller interaktionsloggtransaktionen.</span><span class="sxs-lookup"><span data-stu-id="44fbe-108">Open the contact, salesperson, or interaction log entry.</span></span>
2. <span data-ttu-id="44fbe-109">Välj åtgärden **Skapa interaktion**.</span><span class="sxs-lookup"><span data-stu-id="44fbe-109">Choose the **Create Interaction** action.</span></span>
3. <span data-ttu-id="44fbe-110">Fyll i fälten och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="44fbe-110">Fill in the fields, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="44fbe-111">Om du behöver göra något annat aktivitet i **Avbryt** innan du avslutar interaktionen, kan du avsluta guiden och välja om du vill avsluta interaktionen senare.</span><span class="sxs-lookup"><span data-stu-id="44fbe-111">If you need to perform another task before finishing the interaction, you can choose **Cancel** and then finish the interaction at a later time.</span></span> <span data-ttu-id="44fbe-112">Detta senarelägger interaktionen.</span><span class="sxs-lookup"><span data-stu-id="44fbe-112">This postpones the interaction.</span></span>

## <a name="to-finish-and-delete-postponed-interactions"></a><span data-ttu-id="44fbe-113">Så här slutför du och tar bort senarelagda åtgärder</span><span class="sxs-lookup"><span data-stu-id="44fbe-113">To finish and delete postponed interactions</span></span>
1. <span data-ttu-id="44fbe-114">Öppna kontakten, säljaren eller interaktionsloggtransaktionen.</span><span class="sxs-lookup"><span data-stu-id="44fbe-114">Open the contact, salesperson, or interaction log entry.</span></span>
2. <span data-ttu-id="44fbe-115">Välj **Senarelagda interaktioner**.</span><span class="sxs-lookup"><span data-stu-id="44fbe-115">Choose **Postponed Interactions**.</span></span>
3. <span data-ttu-id="44fbe-116">Markera den åtgärd som du vill slutföra och klicka på **Åtgärder**, Fortsätt.</span><span class="sxs-lookup"><span data-stu-id="44fbe-116">Select the interaction you want to finish, and then choose the **Resume** action.</span></span>

## <a name="to-create-an-interaction-on-a-segment"></a><span data-ttu-id="44fbe-117">Så här skapar du interaktioner för segment</span><span class="sxs-lookup"><span data-stu-id="44fbe-117">To create an interaction on a segment</span></span>
1. <span data-ttu-id="44fbe-118">På startsidan väljer du **Aktiva segment** eller väljer ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") anger **Segment**, och sedan väljer relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="44fbe-118">On the Home page, choose **Active Segments**, or choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Segments**, and then choose the related link.</span></span>
2. <span data-ttu-id="44fbe-119">I fönstret **Segment**, i avsnittet **Interaktion**, fyller du i fälten för att specificera vilken interaktion som du vill tilldela segmentet.</span><span class="sxs-lookup"><span data-stu-id="44fbe-119">In the **Segment window**, in the **Interaction** section, fill in the fields to specify which interaction you want to assign to the segment.</span></span>

    <span data-ttu-id="44fbe-120">När du har tilldelat segmentet en interaktion kan du anpassa interaktionen till respektive kontakt i segmentet, exempelvis genom att välja en annan interaktionsmall på raderna i fönstret **Segment**.</span><span class="sxs-lookup"><span data-stu-id="44fbe-120">After you have assigned an interaction to the segment, you can personalize the interaction for each particular contact within the segment, for example, by selecting another interaction template on the lines in the **Segment** window.</span></span>  
3. <span data-ttu-id="44fbe-121">För att logga segmentet och interaktionerna väljer du åtgärden **Logg**.</span><span class="sxs-lookup"><span data-stu-id="44fbe-121">To log the segment and interactions, choose the **Log** action.</span></span> <span data-ttu-id="44fbe-122">Fönstret **Loggsegment** öppnas.</span><span class="sxs-lookup"><span data-stu-id="44fbe-122">The **Log Segment** window opens.</span></span>
4. <span data-ttu-id="44fbe-123">Om du vill skapa ett nytt segment med samma kontakter markerar du kryssrutan **Skapa uppföljningssegment**.</span><span class="sxs-lookup"><span data-stu-id="44fbe-123">If you want to create a new segment containing the same contacts, select the **Create Follow-up Segment** check box.</span></span> <span data-ttu-id="44fbe-124">Innan ett uppföljningssegment kan skapas måste du ange en nummerserie för segment i fönstret **Affärsstödsinställning**.</span><span class="sxs-lookup"><span data-stu-id="44fbe-124">To create a follow-up segment, you must have specified number series for segments in the **Marketing Setup** window.</span></span>

<span data-ttu-id="44fbe-125">Interaktionen registreras för varje kontakt i segmentet i tabellen **Interaktion loggtrans.** och segmentet loggas.</span><span class="sxs-lookup"><span data-stu-id="44fbe-125">An interaction is recorded for each contact within the segment in the **Interaction Log Entry** table, and the segment is logged.</span></span> <span data-ttu-id="44fbe-126">Loggade segment återfinns i fönstret **Segmentlogg**.</span><span class="sxs-lookup"><span data-stu-id="44fbe-126">Logged segments can be found in the **Logged Segment** window.</span></span>

<span data-ttu-id="44fbe-127">Om du har markerat kryssrutan **Skapa uppföljningssegment** skapas automatiskt ett nytt segment med samma kontakter som det segment som du precis har loggat.</span><span class="sxs-lookup"><span data-stu-id="44fbe-127">If you have selected the **Create Follow-up Segment** check box, a new segment is created that contains the same contacts as the segment you have just logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="44fbe-128">Se även</span><span class="sxs-lookup"><span data-stu-id="44fbe-128">See Also</span></span>
[<span data-ttu-id="44fbe-129">Registrera interaktioner</span><span class="sxs-lookup"><span data-stu-id="44fbe-129">Recording Interactions</span></span>](marketing-interactions.md)  
[<span data-ttu-id="44fbe-130">Hantera kontakter</span><span class="sxs-lookup"><span data-stu-id="44fbe-130">Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="44fbe-131">Hantera Försäljningsmöjligheter</span><span class="sxs-lookup"><span data-stu-id="44fbe-131">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="44fbe-132">Ställa in Kundhantering</span><span class="sxs-lookup"><span data-stu-id="44fbe-132">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="44fbe-133">Arbeta med Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="44fbe-133">Working with Dynamics 365</span></span>](ui-work-product.md)

