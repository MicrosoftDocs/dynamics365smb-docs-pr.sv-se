---
title: "Ställa in Arbetsansvar för kontakter | Microsoft Docs"
description: "Du kan definiera ett arbetsansvar och tilldela den till en kontakt för att ange vilka aktiviteter som kontakten ansvarar för i företaget, till exempel IT- eller produktionsorder."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fd949573e7bfd1b6ce1fc849625a1a3474013f96
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-job-responsibilities-for-contact-persons"></a><span data-ttu-id="3224b-103">Så här: Ange arbetsansvar för kontaktpersonerna.</span><span class="sxs-lookup"><span data-stu-id="3224b-103">How to: Set Up Job Responsibilities for Contact Persons</span></span>
<span data-ttu-id="3224b-104">Du kan lägga till information om arbetsansvar för kontaktpersoner för att ange vad kontaktpersonen ansvarar för i företaget, till exempel IT, ledning eller produktion.</span><span class="sxs-lookup"><span data-stu-id="3224b-104">You can add information about the job responsibilities of contact persons to indicate what the contact person is responsible for within their company, for example, IT, management, or production.</span></span> <span data-ttu-id="3224b-105">Du kan använda den här informationen, när du anger uppgifter om kontakterna.</span><span class="sxs-lookup"><span data-stu-id="3224b-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="3224b-106">Att använda arbetsansvar på kontakter är en två-stegsprocess.</span><span class="sxs-lookup"><span data-stu-id="3224b-106">Using job responsibilities on contacts is a two-step process.</span></span> <span data-ttu-id="3224b-107">Först definierar du arbetsansvarkoden.</span><span class="sxs-lookup"><span data-stu-id="3224b-107">First, you define the job responsibility code.</span></span> <span data-ttu-id="3224b-108">Du måste bara utföra den här steget en gång för varje arbetsansvar.</span><span class="sxs-lookup"><span data-stu-id="3224b-108">You only have to perform this step one time for each job responsibility.</span></span> <span data-ttu-id="3224b-109">När du har en arbetsansvarkod kan du börja koppla koden till kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="3224b-109">Once you have a job responsibility code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-job-responsibility-code"></a><span data-ttu-id="3224b-110">så här definierar du arbetsansvarkod</span><span class="sxs-lookup"><span data-stu-id="3224b-110">to define a job responsibility code</span></span>
<span data-ttu-id="3224b-111">Arbetsansvarkoden definierar typen eller kategorin för projektet, som t.ex. MARKNADSFÖRING eller KÖP.</span><span class="sxs-lookup"><span data-stu-id="3224b-111">The job responsibility code defines the type or category of the job, such a MARKETING or PURCHASE.</span></span> <span data-ttu-id="3224b-112">Du kan ha flera arbetsansvarkoder.</span><span class="sxs-lookup"><span data-stu-id="3224b-112">You can have several job responsibility codes.</span></span> <span data-ttu-id="3224b-113">Att definiera arbetsansvaret använder du fönstret **Arbetsansvar**.</span><span class="sxs-lookup"><span data-stu-id="3224b-113">To define the job responsibility, you use the **Job Responsibilities** window.</span></span>

1. <span data-ttu-id="3224b-114">Välj ikonen ![söka efter sida eller rapport](media/ui-search/search_small.png "ikonen söka efter sida eller rapport"), ange **arbetsansvar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3224b-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Responsibilities**, and then choose the related link.</span></span>
2. <span data-ttu-id="3224b-115">Välj åtgärden **Ny** och fyll i en kod och en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="3224b-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="3224b-116">Koden kan bestå av högst 11 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="3224b-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a><span data-ttu-id="3224b-117">så här tilldelar du arbetsansvaret till en kontaktperson</span><span class="sxs-lookup"><span data-stu-id="3224b-117">to assign job responsibilities to a contact person</span></span>
<span data-ttu-id="3224b-118">Du kan inte tilldela arbetsansvar till kontaktföretag.</span><span class="sxs-lookup"><span data-stu-id="3224b-118">You cannot assign job responsibilities to contact companies.</span></span>

1. <span data-ttu-id="3224b-119">Öppna kontaktperson.</span><span class="sxs-lookup"><span data-stu-id="3224b-119">Open the contact person.</span></span>
2. <span data-ttu-id="3224b-120">Välj åtgärden **Person** och sedan **Arbetsansvar**.</span><span class="sxs-lookup"><span data-stu-id="3224b-120">Choose the **Person** action, and then choose the **Job Responsibilities** action.</span></span> <span data-ttu-id="3224b-121">Fönstret **Kontakt arbetsansvar** öppnas.</span><span class="sxs-lookup"><span data-stu-id="3224b-121">The **Contact Job Responsibilities** window opens.</span></span>
3. <span data-ttu-id="3224b-122">I fältet **Arbetsansvarskod**, markera det arbetsansvar du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="3224b-122">In the **Job Responsibility Code** field, select the job responsibility that you want to assign.</span></span>

<span data-ttu-id="3224b-123">Upprepa stegen för varje arbetsansvar du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="3224b-123">Repeat these steps to assign as many job responsibilities as you want.</span></span> <span data-ttu-id="3224b-124">Arbetsansvar kan också tilldelas i kontaktlista på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="3224b-124">You can also assign job responsibilities from the contact list by following the same procedure.</span></span>

<span data-ttu-id="3224b-125">Antalet arbetsansvar som du har tilldelat kontakter anges automatiskt i fältet **Antal arbetsansvar** i avsnittet **Segmentering** på fönstret **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="3224b-125">The number of job responsibilities you have assigned to the contact is displayed in the **No. of Job Responsibilities** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="3224b-126">När du har tilldelat kontakterna arbetsansvar kan du använda dessa uppgifter för urval av kontakter till segmenten.</span><span class="sxs-lookup"><span data-stu-id="3224b-126">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="3224b-127">Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="3224b-127">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3224b-128">Se även</span><span class="sxs-lookup"><span data-stu-id="3224b-128">See Also</span></span>
[<span data-ttu-id="3224b-129">Skapa kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="3224b-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="3224b-130">Skapa kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="3224b-130">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="3224b-131">Arbeta med Financials</span><span class="sxs-lookup"><span data-stu-id="3224b-131">Working with Financials</span></span>](ui-work-product.md)

