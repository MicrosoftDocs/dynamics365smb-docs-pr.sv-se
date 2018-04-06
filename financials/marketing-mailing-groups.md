---
title: "Ställa in utskicksgrupper för kontakter | Microsoft Docs"
description: "Du kan använda utskicksgrupper för att identifiera grupper av kontakter som ska få samma information, t.ex. för en marknadsföringskampanj."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7402899cb7fe369503eee1b451dc652180e96264
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="2cc58-103">Skapa utskicksgrupper för kontakter</span><span class="sxs-lookup"><span data-stu-id="2cc58-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="2cc58-104">Utskicksgrupper används för att definiera kontaktgrupper som du vill ge samma information.</span><span class="sxs-lookup"><span data-stu-id="2cc58-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="2cc58-105">Du kan till exempel skapa en utskicksgrupp med de kontakter du vill skicka flyttkort till eller en annan grupp för att skicka julklappar.</span><span class="sxs-lookup"><span data-stu-id="2cc58-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="2cc58-106">Att använda utskicksgrupper på kontakter är en två-stegsprocess.</span><span class="sxs-lookup"><span data-stu-id="2cc58-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="2cc58-107">Först definierar du utskicksgruppkoden.</span><span class="sxs-lookup"><span data-stu-id="2cc58-107">First, you define the mailing group code.</span></span> <span data-ttu-id="2cc58-108">Du måste bara utföra den här steget en gång för varje utskicksgrupp.</span><span class="sxs-lookup"><span data-stu-id="2cc58-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="2cc58-109">När du har en utskicksgrupp kan du börja koppla koden till kontaktföretag.</span><span class="sxs-lookup"><span data-stu-id="2cc58-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="2cc58-110">Definiera utskicksgruppkoder</span><span class="sxs-lookup"><span data-stu-id="2cc58-110">To define mailing group codes</span></span>
<span data-ttu-id="2cc58-111">Utskicksgruppkoden definierar typen eller kategorin för den gruppen, till exempel FLYTTA för kontorsflyttning eller GÅVA för julklappar.</span><span class="sxs-lookup"><span data-stu-id="2cc58-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="2cc58-112">Du kan ha flera branschgruppkoder.</span><span class="sxs-lookup"><span data-stu-id="2cc58-112">You can have several industry group codes.</span></span> <span data-ttu-id="2cc58-113">För att definiera branschgrupperna använder du fönstret **utskicksgrupper**.</span><span class="sxs-lookup"><span data-stu-id="2cc58-113">To define the industry groups, you use the **Mailing Groups** window.</span></span>

1. <span data-ttu-id="2cc58-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Utskicksgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="2cc58-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="2cc58-115">Välj åtgärden **Ny** och fyll i en kod och en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="2cc58-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="2cc58-116">Koden kan bestå av högst 11 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="2cc58-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignMailGroupContact"></a> <span data-ttu-id="2cc58-117">Så här tilldelar du utskicksgrupp till en kontakt</span><span class="sxs-lookup"><span data-stu-id="2cc58-117">To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="2cc58-118">Öppna kontakten .</span><span class="sxs-lookup"><span data-stu-id="2cc58-118">Open the contact.</span></span>
2. <span data-ttu-id="2cc58-119">Välj åtgärden **Utskicksgrupper**.</span><span class="sxs-lookup"><span data-stu-id="2cc58-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="2cc58-120">Fönstret **Kontakt utskicksgrupp** öppnas.</span><span class="sxs-lookup"><span data-stu-id="2cc58-120">The **Contact Mailing Groups** window opens.</span></span>
3. <span data-ttu-id="2cc58-121">I fältet **Utskicksgruppskod**, markera den utskicksgrupp du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="2cc58-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="2cc58-122">Upprepa stegen för varje utskicksgrupp du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="2cc58-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="2cc58-123">Utskicksgrupper kan också tilldelas i Kontaktlista på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="2cc58-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="2cc58-124">Antalet utskicksgrupper som du har tilldelat kontakter anges automatiskt i fältet **Antal utskicksgrupper** på avsnittet **Segmentering** på **Kontakt**-fönstret.</span><span class="sxs-lookup"><span data-stu-id="2cc58-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="2cc58-125">När du har tilldelat kontakterna utskicksgrupp kan du använda dessa uppgifter för urval av kontakter till segmenten.</span><span class="sxs-lookup"><span data-stu-id="2cc58-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="2cc58-126">Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="2cc58-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2cc58-127">Se även</span><span class="sxs-lookup"><span data-stu-id="2cc58-127">See Also</span></span>
[<span data-ttu-id="2cc58-128">Skapa kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="2cc58-128">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="2cc58-129">Skapa kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="2cc58-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="2cc58-130">Arbeta med Financials</span><span class="sxs-lookup"><span data-stu-id="2cc58-130">Working with Financials</span></span>](ui-work-product.md)

