---
title: "Ställa in Branschgrupper för kontaktföretag | Microsoft Docs"
description: "Beskriver hur du definierar en branschgrupp och koppla den till ett företag, till exempel detaljhandel eller bilindustri."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fef570e7e56e348a25ae660fa9248b529d0bfde
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-industry-groups-for-contact-companies"></a><span data-ttu-id="9b847-103">Så här: Skapa branschgrupper på kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="9b847-103">How to: Set Up Industry Groups for Contact Companies</span></span>
<span data-ttu-id="9b847-104">Branschgrupper används för att visa vilken bransch kontakterna tillhör, exempelvis detaljhandel eller bilBransch.</span><span class="sxs-lookup"><span data-stu-id="9b847-104">You use industry groups to indicate the type of industry to which your contacts belong, for example, the retail industry or the automobile industry.</span></span>

<span data-ttu-id="9b847-105">Att använda Branschgrupper på kontakter är en två-stegsprocess.</span><span class="sxs-lookup"><span data-stu-id="9b847-105">Using industry groups on contacts is a two-step process.</span></span> <span data-ttu-id="9b847-106">Först definierar du Branschgruppkoden.</span><span class="sxs-lookup"><span data-stu-id="9b847-106">First, you define the industry group code.</span></span> <span data-ttu-id="9b847-107">Du måste bara utföra den här steget en gång för varje Branschgrupp.</span><span class="sxs-lookup"><span data-stu-id="9b847-107">You only have to perform this step one time for each industry group.</span></span> <span data-ttu-id="9b847-108">När du har en Branschgrupp kan du börja koppla koden till kontaktföretag.</span><span class="sxs-lookup"><span data-stu-id="9b847-108">Once you have an industry group code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9b847-109">Om du tänker synkronisera kontakterna med leverantörer, kunder eller bankkonton i andra delar av programmet vill du kanske skapa en affärsrelation för dem.</span><span class="sxs-lookup"><span data-stu-id="9b847-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-an-industry-group-code"></a><span data-ttu-id="9b847-110">Definiera en Branschgruppskod</span><span class="sxs-lookup"><span data-stu-id="9b847-110">To define an industry group code</span></span>
<span data-ttu-id="9b847-111">Koden för branschgruppen definierar typen eller kategorin för den gruppen, till exempel ANNONS för annonsering eller PRESS för TV och radio.</span><span class="sxs-lookup"><span data-stu-id="9b847-111">The industry group code defines the type or category of the group, such as ADVERT for advertising, or PRESS, for TV and radio.</span></span> <span data-ttu-id="9b847-112">Du kan ha flera branschgruppkoder.</span><span class="sxs-lookup"><span data-stu-id="9b847-112">You can have several industry group codes.</span></span> <span data-ttu-id="9b847-113">För att definiera branschgrupperna använder du fönstret **branschgrupper**.</span><span class="sxs-lookup"><span data-stu-id="9b847-113">To define the industry groups, you use the **Industry Groups** window.</span></span>

1. <span data-ttu-id="9b847-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Branschgrupper** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="9b847-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Industry Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="9b847-115">Välj åtgärden **Ny** och fyll i en kod och en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="9b847-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="9b847-116">Koden kan bestå av högst 11 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="9b847-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="9b847-117"><a name="AssignIndustryGroupContact"></a> Så här tilldelar du industrigrupper till en kontakt</span><span class="sxs-lookup"><span data-stu-id="9b847-117"><a name="AssignIndustryGroupContact"></a> To assign industry groups to a contact</span></span>
<span data-ttu-id="9b847-118">Du kan inte tilldela branschgrupper till en kontaktperson, endast företag.</span><span class="sxs-lookup"><span data-stu-id="9b847-118">You cannot assign industry groups to a contact person - only companies.</span></span>

1. <span data-ttu-id="9b847-119">Öppna kontakten .</span><span class="sxs-lookup"><span data-stu-id="9b847-119">Open the contact.</span></span>
2. <span data-ttu-id="9b847-120">Välj åtgärden **företag** och sedan **branschgrupper**.</span><span class="sxs-lookup"><span data-stu-id="9b847-120">Choose the **Company** action, and then the **Industry Groups** action.</span></span> <span data-ttu-id="9b847-121">Fönstret **Kontakt branschgrupper** öppnas.</span><span class="sxs-lookup"><span data-stu-id="9b847-121">The **Contact Industry Groups** window opens.</span></span>
3. <span data-ttu-id="9b847-122">I fältet **branschgruppkod**, markera den branschgrupp du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="9b847-122">In the **Industry Groups Code** field, select the industry groups you want to assign.</span></span>

<span data-ttu-id="9b847-123">Upprepa stegen för varje branschgrupp du vill skapa.</span><span class="sxs-lookup"><span data-stu-id="9b847-123">Repeat these steps to assign as many industry groups as you want.</span></span> <span data-ttu-id="9b847-124">Branschgrupper kan också tilldelas i Kontaktlista på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="9b847-124">You can also assign industry groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="9b847-125">Antalet branschgrupper som du har tilldelat kontakter anges automatiskt i fältet **Antal branschgrupper** på avnisttet **Segmentering** på **Kontakt**-fönstret.</span><span class="sxs-lookup"><span data-stu-id="9b847-125">The number of industry groups that you have assigned to the contact is displayed in the **No. of Industry Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="9b847-126">När du har tilldelat kontakterna branschgrupper kan du använda dessa uppgifter för urval av kontakter till segmenten.</span><span class="sxs-lookup"><span data-stu-id="9b847-126">After you have assigned industry groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="9b847-127">Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="9b847-127">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9b847-128">Se även</span><span class="sxs-lookup"><span data-stu-id="9b847-128">See Also</span></span>
[<span data-ttu-id="9b847-129">Skapa kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="9b847-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="9b847-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9b847-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

