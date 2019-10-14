---
title: Definiera affärsrelationskode för kontakter | Microsoft Docs
description: Använd affärsrelationer i Business Central för att hjälpa till med marknadsföring och för att visa vilket affärsförhållande du har till potentiella kunder eller kunder, till exempel en bank eller serviceleverantör.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 10/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 6c20dbd1eaa60037f33aee35701c5baa224fbc1c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309394"
---
# <a name="setting-up-business-relations-on-contacts"></a><span data-ttu-id="b63a8-103">Ställa in affärsrelationer på kontakter</span><span class="sxs-lookup"><span data-stu-id="b63a8-103">Setting Up Business Relations on Contacts</span></span>
<span data-ttu-id="b63a8-104">Affärsrelationer används för att visa vilket affärsförhållande du har till kontakterna, till exempel spekulant, bank, konsult eller serviceleverantör.</span><span class="sxs-lookup"><span data-stu-id="b63a8-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="b63a8-105">Att använda affärsrelationer på kontakter är en två-stegsprocess.</span><span class="sxs-lookup"><span data-stu-id="b63a8-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="b63a8-106">Först definierar du affärsrelationskoden.</span><span class="sxs-lookup"><span data-stu-id="b63a8-106">First, you define the business relation code.</span></span> <span data-ttu-id="b63a8-107">Du måste bara utföra den här steget en gång för varje affärsrelation.</span><span class="sxs-lookup"><span data-stu-id="b63a8-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="b63a8-108">När du har en affärsrelation kan du börja koppla koden till kontaktföretag.</span><span class="sxs-lookup"><span data-stu-id="b63a8-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b63a8-109">Om du tänker synkronisera kontakterna med leverantörer, kunder eller bankkonton i andra delar av programmet vill du kanske skapa en affärsrelation för dem.</span><span class="sxs-lookup"><span data-stu-id="b63a8-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="b63a8-110">Definiera en affärsrelationskod</span><span class="sxs-lookup"><span data-stu-id="b63a8-110">To define a business relation code</span></span>
<span data-ttu-id="b63a8-111">Affärsrelationkoden definierar en kategori eller en typ av affärsrelation, till exempel BANK eller LAG.</span><span class="sxs-lookup"><span data-stu-id="b63a8-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="b63a8-112">Du kan ha flera affärsrelationskoder.</span><span class="sxs-lookup"><span data-stu-id="b63a8-112">You can have several business relation codes.</span></span> <span data-ttu-id="b63a8-113">För att definiera affärsrelationen använder du sidan **affärsrelationer**.</span><span class="sxs-lookup"><span data-stu-id="b63a8-113">To define the business relation, you use the **Business Relations** page.</span></span>

1. <span data-ttu-id="b63a8-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Affärsrelationer** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="b63a8-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="b63a8-115">Välj åtgärden **Ny** och fyll i en kod och en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="b63a8-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="b63a8-116">Koden kan bestå av högst 11 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="b63a8-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignBusRelContact"></a> <span data-ttu-id="b63a8-117">Så här tilldelar du affärsrelationer till kontakter</span><span class="sxs-lookup"><span data-stu-id="b63a8-117">To assign business relations to a contact</span></span>
<span data-ttu-id="b63a8-118">Du kan inte tilldela affärsrelationer till en kontaktperson, endast företag.</span><span class="sxs-lookup"><span data-stu-id="b63a8-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="b63a8-119">Öppna kontakten .</span><span class="sxs-lookup"><span data-stu-id="b63a8-119">Open the contact.</span></span>
2. <span data-ttu-id="b63a8-120">Välj åtgärden **företag** och sedan **affärsrelationer**.</span><span class="sxs-lookup"><span data-stu-id="b63a8-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="b63a8-121">Sidan **Kontakt affärsrelationer** öppnas.</span><span class="sxs-lookup"><span data-stu-id="b63a8-121">The **Contact Business Relations** page opens.</span></span>
3. <span data-ttu-id="b63a8-122">I fältet **Affärsrelationskod**, markera den affärsrelation du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="b63a8-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="b63a8-123">Upprepa stegen för varje affärsrelation du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="b63a8-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="b63a8-124">Affärsrelationer kan också tilldelas i Kontaktlista på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="b63a8-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="b63a8-125">Antalet affärsrelationer som du har tilldelat kontakter anges automatiskt i fältet **Antal affärsrelationer** på avsnittet **Segmentering** på **Kontakt**-sidan.</span><span class="sxs-lookup"><span data-stu-id="b63a8-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="b63a8-126">När du har tilldelat kontakterna affärsrelationer kan du använda dessa uppgifter för urval av kontakter till segmenten.</span><span class="sxs-lookup"><span data-stu-id="b63a8-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="b63a8-127">Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="b63a8-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b63a8-128">Se även</span><span class="sxs-lookup"><span data-stu-id="b63a8-128">See Also</span></span>
<span data-ttu-id="b63a8-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b63a8-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
