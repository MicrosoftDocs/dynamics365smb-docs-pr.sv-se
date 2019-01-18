---
title: "Ställa in webbadresser för kontaktföretag | Microsoft Docs"
description: "Du kan definiera internet- eller webbadresser och tilldela dem till ett företag för att identifiera hur du vill söka efter information om kontakterna."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 8106eeca31fb5a5c4528d47a27f897454d5dac58
ms.contentlocale: sv-se
ms.lasthandoff: 12/11/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="bb4ae-103">Skapa Webbadresser för kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="bb4ae-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="bb4ae-104">Du kan använda webbadresser med dina kontaktföretag för att t.ex. identifiera sökmotorer och webbplatser på Internet som du vill använda för att söka efter information om kontakterna.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="bb4ae-105">När du tilldelar webbadresser anger du vilken sökmotor och vilket sökord som ska användas för att hitta önskad information.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="bb4ae-106">Att använda webbadresser på kontakter är en två-stegsprocess.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="bb4ae-107">Först definierar du webbadresskoden.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-107">First, you define the web source code.</span></span> <span data-ttu-id="bb4ae-108">Du måste bara utföra den här steget en gång för varje webbadress.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="bb4ae-109">När du har en webbadresskod kan du börja koppla koden till kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="bb4ae-110">För att definiera en webbadresskod</span><span class="sxs-lookup"><span data-stu-id="bb4ae-110">To define a web source code</span></span>
1. <span data-ttu-id="bb4ae-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Webbadresser** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="bb4ae-112">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="bb4ae-113">Fyll i fälten **Kod**, **Beskrivning** och **URL**.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="bb4ae-114">Skriv %1 i fältet **URL** för att infoga en platshållare för ett sökord i URL:en.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="bb4ae-115">När du startar webbadress från en kontakt ersätts %1 med sökordet (till exempel namnet på företaget) som du har angett på sidan **Kontakt webbadresser**.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered on the **Contact Web Sources** page.</span></span>

<span data-ttu-id="bb4ae-116">Upprepa stegen för varje webbkälla du vill skapa.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="bb4ae-117">För att tilldela webbadresser till ett kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="bb4ae-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="bb4ae-118">När du tilldelar webbadresser anger du vilken sökmotor och vilket sökord som ska användas för att hitta önskad information.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="bb4ae-119">Öppna kontakten .</span><span class="sxs-lookup"><span data-stu-id="bb4ae-119">Open the contact.</span></span>
2. <span data-ttu-id="bb4ae-120">Välj åtgärden **företag** och sedan **webbadresser**.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="bb4ae-121">Sidan **Kontakt webbadresser** öppnas.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-121">The **Contact Web Sources** page opens.</span></span>
3. <span data-ttu-id="bb4ae-122">I fältet **webbadresskod**, välj webbadressen som du vill tilldela.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="bb4ae-123">Skriv i fältet **Sökord** det sökord som ska användas för att hitta informationen.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="bb4ae-124">Upprepa stegen för varje webbkälla du vill skapa.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="bb4ae-125">Webbadresser kan också tilldelas på sidan **Kontaktlista** på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="bb4ae-125">You can also assign web sources from the **Contact List** page by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb4ae-126">Se även</span><span class="sxs-lookup"><span data-stu-id="bb4ae-126">See Also</span></span>
[<span data-ttu-id="bb4ae-127">Skapa kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="bb4ae-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="bb4ae-128">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bb4ae-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

