---
title: Följa upp segment och relaterade interaktioner | Microsoft Docs
description: Lär dig mer om att skapa segment för att definiera kontaktgrupper och ange interaktioner för segment.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: aeed39953f6b5219dcc290a3416a9dd7e2e69d89
ms.sourcegitcommit: dac212009aadf3227e54c99976c438f6e56f182a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/02/2019
ms.locfileid: "1446767"
---
# <a name="manage-interactions-for-segments"></a><span data-ttu-id="90d36-103">Hantera interaktioner för segment</span><span class="sxs-lookup"><span data-stu-id="90d36-103">Manage Interactions for Segments</span></span>
<span data-ttu-id="90d36-104">Sidan **Segment** är en typ av formulär där du kan:</span><span class="sxs-lookup"><span data-stu-id="90d36-104">The **Segment** page is a type of worksheet where you can:</span></span>

* <span data-ttu-id="90d36-105">Skapa segment.</span><span class="sxs-lookup"><span data-stu-id="90d36-105">Create segments.</span></span>
* <span data-ttu-id="90d36-106">Spara segmentvillkor som du har använt för att välja kontakter.</span><span class="sxs-lookup"><span data-stu-id="90d36-106">Save the segmentation criteria you have used to select contacts.</span></span>
* <span data-ttu-id="90d36-107">Logga segmentet och registrera interaktioner som innefattar kontakterna i segmentet.</span><span class="sxs-lookup"><span data-stu-id="90d36-107">Log the segment and record interactions involving the contacts within the segment.</span></span>

## <a name="segmenting"></a><span data-ttu-id="90d36-108">Skapa segment</span><span class="sxs-lookup"><span data-stu-id="90d36-108">Segmenting</span></span>
<span data-ttu-id="90d36-109">Det finns flera sätt att skapa segment:</span><span class="sxs-lookup"><span data-stu-id="90d36-109">There are several ways to create segments:</span></span>

* <span data-ttu-id="90d36-110">Du kan manuellt ange på segmentraderna de kontakter du vill ha med i segmentet.</span><span class="sxs-lookup"><span data-stu-id="90d36-110">You can manually enter the contacts you want to include in the segment in the segment lines.</span></span>
* <span data-ttu-id="90d36-111">Du kan välja kontakter.</span><span class="sxs-lookup"><span data-stu-id="90d36-111">You can select contacts.</span></span>
* <span data-ttu-id="90d36-112">Du kan återanvända loggat segment som grund för att skapa ett nytt.</span><span class="sxs-lookup"><span data-stu-id="90d36-112">You can reuse a logged segment as the basis to create a new one.</span></span>
* <span data-ttu-id="90d36-113">Du kan återanvända sparade segmentkriterier.</span><span class="sxs-lookup"><span data-stu-id="90d36-113">You can reuse saved segmentation criteria.</span></span>

## <a name="interactions"></a><span data-ttu-id="90d36-114">Interaktioner</span><span class="sxs-lookup"><span data-stu-id="90d36-114">Interactions</span></span>
<span data-ttu-id="90d36-115">På sidan **Segment** kan du skapa interaktioner för flera kontakter samtidigt.</span><span class="sxs-lookup"><span data-stu-id="90d36-115">On the **Segment** page, you can create interactions for several contacts simultaneously.</span></span> <span data-ttu-id="90d36-116">Du kan exempelvis slå ihop ett segment med ett Microsoft Word-dokument så du kan skicka brev till alla kontakterna i segmentet.</span><span class="sxs-lookup"><span data-stu-id="90d36-116">For example, you can merge a segment with a Microsoft Word document, so that you can send a letter to all the contacts in the segment.</span></span>

<span data-ttu-id="90d36-117">Du kan ange uppgifter om interaktionen för segmentet i **segmenthuvudet**.</span><span class="sxs-lookup"><span data-stu-id="90d36-117">You can specify information about the interaction for the segment on the **Segment** header.</span></span> <span data-ttu-id="90d36-118">Du kan till exempel bestämma vilken interaktionsmall du vill använda för samtliga kontakter, göra en beskrivning, ange korrespondenstyp och så vidare.</span><span class="sxs-lookup"><span data-stu-id="90d36-118">For example, you can decide which interaction template you want to use for all the contacts, specify a description, a correspondence type, and so on.</span></span> <span data-ttu-id="90d36-119">Du kan även ändra den här informationen på segmentraden för varje enskild kontakt genom att exempelvis ange annan beskrivning för en enda kontakt.</span><span class="sxs-lookup"><span data-stu-id="90d36-119">However, you can modify this information in the segment line for each particular contact, for example, by specifying another description for one contact.</span></span> <span data-ttu-id="90d36-120">Om du slår samman ett segment med ett Microsoft Word-dokument kan du anpassa dokumentet för att skickas till en eller flera av kontakterna i segmentet, exempelvis genom att lägga till individuella kommentarer i det.</span><span class="sxs-lookup"><span data-stu-id="90d36-120">If you are merging a segment with a Microsoft Word document, you can personalize the document to be sent for one or several of the contacts within the segment, for example, by adding individualized comments to the document.</span></span>

## <a name="logging"></a><span data-ttu-id="90d36-121">Logga</span><span class="sxs-lookup"><span data-stu-id="90d36-121">Logging</span></span>
<span data-ttu-id="90d36-122">På sidan **Segment** när du väljer **Logg**, registrerar programmet interaktionerna på sidan **Interaktion loggtrans.** och loggar segmentet.</span><span class="sxs-lookup"><span data-stu-id="90d36-122">On the **Segment** page, when you choose **Log**, the application records the interactions on the **Interaction Log Entry** page, and logs the segment.</span></span> <span data-ttu-id="90d36-123">När du har loggat det finns det bara på sidan **Segmentlogg**.</span><span class="sxs-lookup"><span data-stu-id="90d36-123">After you have logged the segment, you can only find it on the **Logged Segments** page.</span></span>

<span data-ttu-id="90d36-124">På sidan **Segmentlogg** kan du skapa ett nytt segment som innehåller ett uppföljningssegment med samma kontakter som det loggade segmentet.</span><span class="sxs-lookup"><span data-stu-id="90d36-124">On the **Logged Segments** page, you can decide to create a follow-up segment containing the same contacts as the segment you have logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="90d36-125">Se även</span><span class="sxs-lookup"><span data-stu-id="90d36-125">See Also</span></span>
[<span data-ttu-id="90d36-126">Skapa segment</span><span class="sxs-lookup"><span data-stu-id="90d36-126">Create Segments</span></span>](marketing-how-create-segment.md)  
[<span data-ttu-id="90d36-127">Skapa interaktioner för segment</span><span class="sxs-lookup"><span data-stu-id="90d36-127">Create Interactions for Segments</span></span>](marketing-how-create-interactions.md)  
[<span data-ttu-id="90d36-128">Hantera segment</span><span class="sxs-lookup"><span data-stu-id="90d36-128">Managing Segments</span></span>](marketing-segments.md)  
[<span data-ttu-id="90d36-129">Inspelningsinteraktioner med kontakter</span><span class="sxs-lookup"><span data-stu-id="90d36-129">Recording Interactions With Contacts</span></span>](marketing-interactions.md)  
[<span data-ttu-id="90d36-130">Hantera Försäljningsmöjligheter</span><span class="sxs-lookup"><span data-stu-id="90d36-130">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="90d36-131">Skapa och hantera kontakter</span><span class="sxs-lookup"><span data-stu-id="90d36-131">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="90d36-132">Arbeta med Business Central</span><span class="sxs-lookup"><span data-stu-id="90d36-132">Working with Business Central</span></span>](ui-work-product.md)
