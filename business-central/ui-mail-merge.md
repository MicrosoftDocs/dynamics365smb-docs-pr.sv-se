---
title: Använda Word-mallar för masskommunikation | Microsoft Docs
description: Med Word-mallar kan du enkelt skapa dokument som är anpassade för specifika entiteter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 118d8db1266bb7150965ec4d1ce44ece77638764
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788596"
---
# <a name="using-word-templates-for-bulk-communication"></a><span data-ttu-id="dfed4-103">Använda Word-mallar för masskommunikation</span><span class="sxs-lookup"><span data-stu-id="dfed4-103">Using Word Templates for Bulk Communication</span></span>
<span data-ttu-id="dfed4-104">Microsoft Word-mallar kan göra det enklare att kommunicera med enheter som kunder och leverantörer.</span><span class="sxs-lookup"><span data-stu-id="dfed4-104">Microsoft Word templates can make it easier to mass communicate with entities such as customers and vendors.</span></span> <span data-ttu-id="dfed4-105">Du kan till exempel skapa broschyrer för att avisera kunder om en försäljningskampanj, brev för att informera leverantörer om nya inköpsprinciper eller inbjudningar till att locka kontakter till ett kommande evenemang.</span><span class="sxs-lookup"><span data-stu-id="dfed4-105">For example, you can create brochures to alert customers about a sales campaign, letters to inform vendors about a new purchasing policy, or invitations to attract contacts to an upcoming event.</span></span>

<span data-ttu-id="dfed4-106">Du kan använda entiteter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakälla för mallen och lägga till kopplings instruktioner i anpassa dokument för varje entitet.</span><span class="sxs-lookup"><span data-stu-id="dfed4-106">You can use entities in [!INCLUDE[prod_short](includes/prod_short.md)] as the data source for the template, and add merge fields to personalize documents for each entity.</span></span> <span data-ttu-id="dfed4-107">Sammankopplingsfälten hämtas från entiteten i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="dfed4-107">The merge fields come from the entity in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="dfed4-108">När du använder en Word-mall på en entitet infogas data från sammankopplingsfälten i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="dfed4-108">When you apply a Word template to an entity, data from the merge fields is inserted in the document.</span></span>

<span data-ttu-id="dfed4-109">På sidan **Word-mallar** kan du använda en assisterad installations handbok för att hämta en zip-fil som innehåller en DataSource.txt-och en Word-mallfil för en entitet.</span><span class="sxs-lookup"><span data-stu-id="dfed4-109">On the **Word Templates** page, you can use an assisted setup guide to download a ZIP file that contains a DataSource.txt and a Word template file for an entity.</span></span> <span data-ttu-id="dfed4-110">När du har skapat mallen och lagt till sammankopplingsinstruktioner använder du samma stödlinje för att överföra mallen.</span><span class="sxs-lookup"><span data-stu-id="dfed4-110">After you set up the template and add merge fields, you use the same guide to upload the template.</span></span> <span data-ttu-id="dfed4-111">Du kan bara använda Word-mallen och de datakällfiler som du hämtar från [!INCLUDE[prod_short](includes/prod_short.md)] och du måste lagra filerna på samma plats.</span><span class="sxs-lookup"><span data-stu-id="dfed4-111">You can only use the Word template and data source files that you download from [!INCLUDE[prod_short](includes/prod_short.md)], and you must store the files in the same location.</span></span>

> [!NOTE]
> <span data-ttu-id="dfed4-112">När du väljer en entitet för vilken du vill skapa en mall visar listan alla entiteter i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="dfed4-112">When you choose an entity for which to create a template, the list shows all entities in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="dfed4-113">Du kan emellertid inte skapa mallar för alla entiteter.</span><span class="sxs-lookup"><span data-stu-id="dfed4-113">However, you cannot create templates for all entities.</span></span> <span data-ttu-id="dfed4-114">Om namnet på en entitet innehåller specialtecken, till exempel **/**, **.**, **_** eller **-** kan du inte skapa en mall för den.</span><span class="sxs-lookup"><span data-stu-id="dfed4-114">If the name of an entity contains special characters, such as **/**, **.**, **_**, or **-**, you cannot create a template for it.</span></span> <span data-ttu-id="dfed4-115">Namnet på entiteten visas i kolumnen **Objektrubrik**.</span><span class="sxs-lookup"><span data-stu-id="dfed4-115">The name of the entity is shown in the **Object Caption** column.</span></span>

<span data-ttu-id="dfed4-116">När du lägger upp mallen i Word på fliken **Utskick** kan du lägga till sammankopplingsinstruktioner genom att välja **Infoga sammankopplingsfält**.</span><span class="sxs-lookup"><span data-stu-id="dfed4-116">When you are setting up the template in Word, on the **Mailings** tab you can add merge fields by choosing **Insert Merge Field**.</span></span>

> [!NOTE]
> <span data-ttu-id="dfed4-117">Du kan inte använda sammankopplingsfält om fältnamnet innehåller 40 tecken eller mer.</span><span class="sxs-lookup"><span data-stu-id="dfed4-117">You cannot use merge fields if the name of the field contains 40 characters or more.</span></span> <span data-ttu-id="dfed4-118">Du kan till exempel inte använda fältet Company__Information_Customs_Permit_Date eftersom det innehåller 40 tecken.</span><span class="sxs-lookup"><span data-stu-id="dfed4-118">For example, you cannot use the Company__Information_Customs_Permit_Date field because it has 40 characters.</span></span> 

<span data-ttu-id="dfed4-119">När Word-mallen är klar kan du på sidan **Word-mallar** välja **Använd** för att skapa dokumenten.</span><span class="sxs-lookup"><span data-stu-id="dfed4-119">When your Word template is ready, on the **Word Templates** page you can choose **Apply** to generate the documents.</span></span> <span data-ttu-id="dfed4-120">Du kan antingen skapa ett dokument som innehåller avsnitt för varje entitet, eller dela operationen för att skapa ett nytt dokument för varje entitet.</span><span class="sxs-lookup"><span data-stu-id="dfed4-120">You can either create one document that contains sections for each entity, or split the operation to create a new document for each entity.</span></span>

## <a name="to-create-a-word-template"></a><span data-ttu-id="dfed4-121">Skapa en Word-mall</span><span class="sxs-lookup"><span data-stu-id="dfed4-121">To create a Word template</span></span>
1. <span data-ttu-id="dfed4-122">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Word-mallar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="dfed4-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Word Templates**, and then choose the related link.</span></span>
2. <span data-ttu-id="dfed4-123">Följ instruktionerna i assisterad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dfed4-123">Follow the steps in the assisted setup guide.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="dfed4-124">Se även</span><span class="sxs-lookup"><span data-stu-id="dfed4-124">See Also</span></span>
[<span data-ttu-id="dfed4-125">Hantera rapport- och dokumentlayouter</span><span class="sxs-lookup"><span data-stu-id="dfed4-125">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
