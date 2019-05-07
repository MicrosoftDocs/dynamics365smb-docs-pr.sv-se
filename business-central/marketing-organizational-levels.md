---
title: Ställa in befattningsnivåer för kontaktpersoner | Microsoft Docs
description: Du kan definiera en befattningsnivå och tilldela den till din kontakt om du vill ange vilken befattningsnivå de har i företaget, t.ex. företagsledning.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 68f20af84652f684eaa0d69c98e0dc3cb722ee91
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "931344"
---
# <a name="set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="af29f-103">Skapa befattningsnivåer för kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="af29f-103">Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="af29f-104">Du kan använda befattningsnivåer på kontakterna om du vill ange vilken befattningsnivå de har i företaget, t.ex. företagsledning.</span><span class="sxs-lookup"><span data-stu-id="af29f-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="af29f-105">Du kan använda den här informationen, när du anger uppgifter om kontakterna.</span><span class="sxs-lookup"><span data-stu-id="af29f-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="af29f-106">Att använda befattningsnivåer på kontakter är en två-stegsprocess.</span><span class="sxs-lookup"><span data-stu-id="af29f-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="af29f-107">Först definierar du befattningsnivåkoden.</span><span class="sxs-lookup"><span data-stu-id="af29f-107">First, you define the organizational level code.</span></span> <span data-ttu-id="af29f-108">Du måste bara utföra den här steget en gång för varje befattningsnivå.</span><span class="sxs-lookup"><span data-stu-id="af29f-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="af29f-109">När du har en befattningsnivåkod kan du börja koppla koden till kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="af29f-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="af29f-110">För att definiera en befattningsnivåkod</span><span class="sxs-lookup"><span data-stu-id="af29f-110">To define an organizational level code</span></span>
<span data-ttu-id="af29f-111">Befattningsnivåkoden anger typen eller kategorin av befattningsnivån, som t.ex. VD eller CFO.</span><span class="sxs-lookup"><span data-stu-id="af29f-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="af29f-112">Du kan ha flera befattningsnivåkoder.</span><span class="sxs-lookup"><span data-stu-id="af29f-112">You can have several organizational level codes.</span></span> <span data-ttu-id="af29f-113">För att definiera befattningsnivån använder du sidan **Befattningsnivåer**.</span><span class="sxs-lookup"><span data-stu-id="af29f-113">To define the organizational level, you use the **Organizational Levels** page.</span></span>

1. <span data-ttu-id="af29f-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Befattningsnivåer** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="af29f-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="af29f-115">Välj åtgärden **Ny** och fyll i en kod och en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="af29f-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="af29f-116">Koden kan bestå av högst 11 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="af29f-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="af29f-117">För att tilldela befattningsnivåer till en kontaktperson</span><span class="sxs-lookup"><span data-stu-id="af29f-117">To assign organizational levels to a contact person</span></span>
<span data-ttu-id="af29f-118">Du kan endast tilldela befattningsnivåer till kontaktpersoner, inte kontaktföretag.</span><span class="sxs-lookup"><span data-stu-id="af29f-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="af29f-119">Du kan endast tilldela en befattningsnivå per kontakt.</span><span class="sxs-lookup"><span data-stu-id="af29f-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="af29f-120">Öppna kontakten .</span><span class="sxs-lookup"><span data-stu-id="af29f-120">Open the contact.</span></span>
2. <span data-ttu-id="af29f-121">I fältet **Befattningsnivåer** väljer du den kod som du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="af29f-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="af29f-122">När du har fördelat befattningsnivåer till kontakterna kan du använda informationen för att skapa segment.</span><span class="sxs-lookup"><span data-stu-id="af29f-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="af29f-123">När du har tilldelat arbetsansvar till kontakterna kan du använda dessa uppgifter för urval av kontakter till segmenten.</span><span class="sxs-lookup"><span data-stu-id="af29f-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="af29f-124">Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="af29f-124">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="af29f-125">Se även</span><span class="sxs-lookup"><span data-stu-id="af29f-125">See Also</span></span>
[<span data-ttu-id="af29f-126">Skapar kontakter</span><span class="sxs-lookup"><span data-stu-id="af29f-126">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="af29f-127">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af29f-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
