---
title: "Definiera affärsrelationskode för kontakter | Microsoft Docs"
description: "Använd affärsrelationer i Business Central för att hjälpa till med marknadsföring och för att visa vilket affärsförhållande du har till potentiella kunder eller kunder, till exempel en bank eller serviceleverantör."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f879d933822e061913975c1dbac2bf883ad9bbc1
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a><span data-ttu-id="8ff59-103">Ställa in affärsrelationer på kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="8ff59-103">Setting Up Business Relations on Contact Companies</span></span>
<span data-ttu-id="8ff59-104">Affärsrelationer används för att visa vilket affärsförhållande du har till kontakterna, till exempel spekulant, bank, konsult eller serviceleverantör.</span><span class="sxs-lookup"><span data-stu-id="8ff59-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="8ff59-105">Att använda affärsrelationer på kontakter är en två-stegsprocess.</span><span class="sxs-lookup"><span data-stu-id="8ff59-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="8ff59-106">Först definierar du affärsrelationskoden.</span><span class="sxs-lookup"><span data-stu-id="8ff59-106">First, you define the business relation code.</span></span> <span data-ttu-id="8ff59-107">Du måste bara utföra den här steget en gång för varje affärsrelation.</span><span class="sxs-lookup"><span data-stu-id="8ff59-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="8ff59-108">När du har en affärsrelation kan du börja koppla koden till kontaktföretag.</span><span class="sxs-lookup"><span data-stu-id="8ff59-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="8ff59-109">Om du tänker synkronisera kontakterna med leverantörer, kunder eller bankkonton i andra delar av programmet vill du kanske skapa en affärsrelation för dem.</span><span class="sxs-lookup"><span data-stu-id="8ff59-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="8ff59-110">Definiera en affärsrelationskod</span><span class="sxs-lookup"><span data-stu-id="8ff59-110">To define a business relation code</span></span>
<span data-ttu-id="8ff59-111">Affärsrelationkoden definierar en kategori eller en typ av affärsrelation, till exempel BANK eller LAG.</span><span class="sxs-lookup"><span data-stu-id="8ff59-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="8ff59-112">Du kan ha flera affärsrelationskoder.</span><span class="sxs-lookup"><span data-stu-id="8ff59-112">You can have several business relation codes.</span></span> <span data-ttu-id="8ff59-113">För att definiera affärsrelationen använder du fönstret **affärsrelationer**.</span><span class="sxs-lookup"><span data-stu-id="8ff59-113">To define the business relation, you use the **Business Relations** window.</span></span>

1. <span data-ttu-id="8ff59-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Affärsrelationer** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="8ff59-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="8ff59-115">Välj åtgärden **Ny** och fyll i en kod och en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="8ff59-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="8ff59-116">Koden kan bestå av högst 11 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="8ff59-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignBusRelContact"></a> <span data-ttu-id="8ff59-117">Så här tilldelar du affärsrelationer till kontakter</span><span class="sxs-lookup"><span data-stu-id="8ff59-117">To assign business relations to a contact</span></span>
<span data-ttu-id="8ff59-118">Du kan inte tilldela affärsrelationer till en kontaktperson, endast företag.</span><span class="sxs-lookup"><span data-stu-id="8ff59-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="8ff59-119">Öppna kontakten .</span><span class="sxs-lookup"><span data-stu-id="8ff59-119">Open the contact.</span></span>
2. <span data-ttu-id="8ff59-120">Välj åtgärden **företag** och sedan **affärsrelationer**.</span><span class="sxs-lookup"><span data-stu-id="8ff59-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="8ff59-121">Fönstret **Kontakt affärsrelationer** öppnas.</span><span class="sxs-lookup"><span data-stu-id="8ff59-121">The **Contact Business Relations** window opens.</span></span>
3. <span data-ttu-id="8ff59-122">I fältet **Affärsrelationskod**, markera den affärsrelation du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="8ff59-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="8ff59-123">Upprepa stegen för varje affärsrelation du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="8ff59-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="8ff59-124">Affärsrelationer kan också tilldelas i Kontaktlista på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="8ff59-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="8ff59-125">Antalet affärsrelationer som du har tilldelat kontakter anges automatiskt i fältet **Antal affärsrelationer** på avsnittet **Segmentering** på **Kontakt**-fönstret.</span><span class="sxs-lookup"><span data-stu-id="8ff59-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="8ff59-126">När du har tilldelat kontakterna affärsrelationer kan du använda dessa uppgifter för urval av kontakter till segmenten.</span><span class="sxs-lookup"><span data-stu-id="8ff59-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="8ff59-127">Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="8ff59-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8ff59-128">Se även</span><span class="sxs-lookup"><span data-stu-id="8ff59-128">See Also</span></span>
[<span data-ttu-id="8ff59-129">Skapa kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="8ff59-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="8ff59-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8ff59-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
