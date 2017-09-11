---
title: "Ställa in befattningsnivåer för kontaktpersoner | Microsoft Docs"
description: "Du kan definiera en befattningsnivå och tilldela den till din kontakt om du vill ange vilken befattningsnivå de har i företaget, t.ex. företagsledning."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 927c27998bfaeb8d7247158cde1d1eb958a6911f
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="d2160-103">Så här: Skapa befattningsnivåer för kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="d2160-103">How to: Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="d2160-104">Du kan använda befattningsnivåer på kontakterna om du vill ange vilken befattningsnivå de har i företaget, t.ex. företagsledning.</span><span class="sxs-lookup"><span data-stu-id="d2160-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="d2160-105">Du kan använda den här informationen, när du anger uppgifter om kontakterna.</span><span class="sxs-lookup"><span data-stu-id="d2160-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="d2160-106">Att använda befattningsnivåer på kontakter är en två-stegsprocess.</span><span class="sxs-lookup"><span data-stu-id="d2160-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="d2160-107">Först definierar du befattningsnivåkoden.</span><span class="sxs-lookup"><span data-stu-id="d2160-107">First, you define the organizational level code.</span></span> <span data-ttu-id="d2160-108">Du måste bara utföra den här steget en gång för varje befattningsnivå.</span><span class="sxs-lookup"><span data-stu-id="d2160-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="d2160-109">När du har en befattningsnivåkod kan du börja koppla koden till kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="d2160-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="d2160-110">för att definiera en befattningsnivåkod</span><span class="sxs-lookup"><span data-stu-id="d2160-110">to define an organizational level code</span></span>
<span data-ttu-id="d2160-111">Befattningsnivåkoden anger typen eller kategorin av befattningsnivån, som t.ex. VD eller CFO.</span><span class="sxs-lookup"><span data-stu-id="d2160-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="d2160-112">Du kan ha flera befattningsnivåkoder.</span><span class="sxs-lookup"><span data-stu-id="d2160-112">You can have several organizational level codes.</span></span> <span data-ttu-id="d2160-113">För att definiera befattningsnivån använder du fönstret **Befattningsnivåer**.</span><span class="sxs-lookup"><span data-stu-id="d2160-113">To define the organizational level, you use the **Organizational Levels** window.</span></span>

1. <span data-ttu-id="d2160-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), gå till **Befattningsnivåer** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d2160-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="d2160-115">Välj åtgärden **Ny** och fyll i en kod och en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="d2160-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="d2160-116">Koden kan bestå av högst 11 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="d2160-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="d2160-117">för att tilldela befattningsnivåer till en kontaktperson</span><span class="sxs-lookup"><span data-stu-id="d2160-117">to assign organizational levels to a contact person</span></span>
<span data-ttu-id="d2160-118">Du kan endast tilldela befattningsnivåer till kontaktpersoner, inte kontaktföretag.</span><span class="sxs-lookup"><span data-stu-id="d2160-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="d2160-119">Du kan endast tilldela en befattningsnivå per kontakt.</span><span class="sxs-lookup"><span data-stu-id="d2160-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="d2160-120">Öppna kontakten .</span><span class="sxs-lookup"><span data-stu-id="d2160-120">Open the contact.</span></span>
2. <span data-ttu-id="d2160-121">I fältet **Befattningsnivåer** väljer du den kod som du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="d2160-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="d2160-122">När du har fördelat befattningsnivåer till kontakterna kan du använda informationen för att skapa segment.</span><span class="sxs-lookup"><span data-stu-id="d2160-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="d2160-123">När du har tilldelat kontakterna arbetsansvar kan du använda dessa uppgifter för urval av kontakter till segmenten.</span><span class="sxs-lookup"><span data-stu-id="d2160-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="d2160-124">Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="d2160-124">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d2160-125">Se även</span><span class="sxs-lookup"><span data-stu-id="d2160-125">See Also</span></span>
[<span data-ttu-id="d2160-126">Skapa kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="d2160-126">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="d2160-127">Skapa kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="d2160-127">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
<span data-ttu-id="d2160-128">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d2160-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

