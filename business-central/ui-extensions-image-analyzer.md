---
title: "Använda tillägget Image Analyzer | Microsoft Docs"
description: "Detta tillägg låter dig analysera bilder av kontaktpersoner och artiklar för att söka efter egenskaper, så att du snabbt kan tilldela dem i Business Central."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 06/19/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: b767588b4dae6953371e112fd4e8e5cd4af7b1e0
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---

# <a name="the-image-analyzer-extension-for-microsoft-business-central"></a><span data-ttu-id="f3232-103">Tillägget Image Analyzer för Microsoft Business Central</span><span class="sxs-lookup"><span data-stu-id="f3232-103">The Image Analyzer Extension for Microsoft Business Central</span></span>
<span data-ttu-id="f3232-104">Tillägget Image Analyzer använder kraftfulla bildanalyser från Computer Vision API för Microsoft Cognitive Services för att identifiera attribut i bilder du importerar för artiklar och kontaktpersoner, så att du lätt kan gå igenom och tilldela dem.</span><span class="sxs-lookup"><span data-stu-id="f3232-104">The Image Analyzer extension uses powerful image analytics provided by the Computer Vision API for Microsoft Cognitive Services to detect attributes in the images that you import for items and contact persons, so you can easily review and assign them.</span></span> <span data-ttu-id="f3232-105">För artiklar, kan attribut vara om artikel är en tabell eller en bil eller om den är röd eller blå.</span><span class="sxs-lookup"><span data-stu-id="f3232-105">For items, attributes could be whether the item is a table or a car, and whether it is red or blue.</span></span> <span data-ttu-id="f3232-106">För kontaktpersoner kan attribut vara kön och ålder.</span><span class="sxs-lookup"><span data-stu-id="f3232-106">For contact persons, attributes can be gender or age.</span></span>

<span data-ttu-id="f3232-107">Image Analyzer föreslår attribut baserat på etiketter som  Computer Vision API hittar och konfidensnivå.</span><span class="sxs-lookup"><span data-stu-id="f3232-107">Image Analyzer suggests attributes based on tags that the Computer Vision API finds, and a confidence level.</span></span> <span data-ttu-id="f3232-108">Som standard föreslås attribut endast om det är minst 80 % till att attributet är korrekt.</span><span class="sxs-lookup"><span data-stu-id="f3232-108">By default, it suggests attributes only if it is at least 80% sure that the attribute is correct.</span></span> <span data-ttu-id="f3232-109">Du kan ange en annan konfidensintervall, om det behövs.</span><span class="sxs-lookup"><span data-stu-id="f3232-109">You can set another confidence level, if needed.</span></span> <span data-ttu-id="f3232-110">Mer information om hur etiketter och konfidensnivå fastställs finns [Computer Vision API](https://go.microsoft.com/fwlink/?linkid=851476).</span><span class="sxs-lookup"><span data-stu-id="f3232-110">To learn more about how the tags and confidence level are determined, see [Computer Vision API](https://go.microsoft.com/fwlink/?linkid=851476).</span></span>  

<span data-ttu-id="f3232-111">Image Analyzer är gratis [!INCLUDE[d365fin](includes/d365fin_md.md)], men det finns en gräns för hur många artiklar som du kan analysera under en viss tidsperiod.</span><span class="sxs-lookup"><span data-stu-id="f3232-111">Image Analyzer is free in [!INCLUDE[d365fin](includes/d365fin_md.md)], but there is a limit to the number of items that you can analyze during a certain period of time.</span></span> <span data-ttu-id="f3232-112">Som standard kan du analysera 100 bilder per månad.</span><span class="sxs-lookup"><span data-stu-id="f3232-112">By default, you can analyze 100 images per month.</span></span>

<span data-ttu-id="f3232-113">När du har aktiverat tillägget körs Image Analyzer när du importerar en bild till en artikel eller kontaktperson.</span><span class="sxs-lookup"><span data-stu-id="f3232-113">After you enable the extension, Image Analyzer runs each time you import an image to an item or contact person.</span></span> <span data-ttu-id="f3232-114">Du ser de attribut och konfidensnivå och information direkt och bestämmer vad du vill göra med varje attribut.</span><span class="sxs-lookup"><span data-stu-id="f3232-114">You will see the attributes, confidence level, and details right away, and can decide what to do with each attribute.</span></span> <span data-ttu-id="f3232-115">Om du har importerat bilder innan du valde tillägget Image Analyzer måste du gå till artikel- eller kontaktkorten och välja åtgärd **analysera bild**.</span><span class="sxs-lookup"><span data-stu-id="f3232-115">If you imported images before you enabled the Image Analyzer extension, you must go to the item or contact cards and choose the **Analyze Picture** action.</span></span>  

>   [!NOTE]  
>   <span data-ttu-id="f3232-116">Genom att aktivera det här tillägget accepterar du att Microsoft kan lagra data och använda den för att förbättra Microsoft-tjänster, som gör Computer Vision API bättre.</span><span class="sxs-lookup"><span data-stu-id="f3232-116">By enabling this extension you agree that Microsoft may store your data and use it to improve Microsoft services, such as making the Computer Vision API better.</span></span> <span data-ttu-id="f3232-117">För att skydda din integritet har vidtagit åtgärder för att göra data anonym och skydda den.</span><span class="sxs-lookup"><span data-stu-id="f3232-117">To help protect your privacy, we take steps to make your data anonymous and keep it secure.</span></span> <span data-ttu-id="f3232-118">Vi vill inte publicera informationen eller andra användare kan använda den.</span><span class="sxs-lookup"><span data-stu-id="f3232-118">We will not publish your data or let other people use it.</span></span> <span data-ttu-id="f3232-119">Du kan ta bort bilden från objekt i [!INCLUDE[d365fin](includes/d365fin_md.md)], men Computer Vision API  har fortfarande bilden sin avidentifierade form.</span><span class="sxs-lookup"><span data-stu-id="f3232-119">You can remove the image from the item in [!INCLUDE[d365fin](includes/d365fin_md.md)], however, the Computer Vision API will still have the image in its de-identified form.</span></span> <span data-ttu-id="f3232-120">Mer information finns i [Microsoft Trust Center](https://go.microsoft.com/fwlink/?linkid=851463).</span><span class="sxs-lookup"><span data-stu-id="f3232-120">For more information, see [Microsoft Trust Center](https://go.microsoft.com/fwlink/?linkid=851463).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3232-121">Krav</span><span class="sxs-lookup"><span data-stu-id="f3232-121">Requirements</span></span>
<span data-ttu-id="f3232-122">Det finns några krav för bilder:</span><span class="sxs-lookup"><span data-stu-id="f3232-122">There are a few requirements for the images:</span></span>

* <span data-ttu-id="f3232-123">Bildformat: JPEG, PNG, GIF, BMP</span><span class="sxs-lookup"><span data-stu-id="f3232-123">Image formats: JPEG, PNG, GIF, BMP</span></span>  
* <span data-ttu-id="f3232-124">Maximal filstorlek: mindre än 4 MB</span><span class="sxs-lookup"><span data-stu-id="f3232-124">Maximum file size: Less than 4 MB</span></span>  
* <span data-ttu-id="f3232-125">Bilddimensioner: större än 50 x 50 bildpunkter</span><span class="sxs-lookup"><span data-stu-id="f3232-125">Image dimensions: Greater than 50 x 50 pixels</span></span>  

## <a name="blacklisting-suggested-attributes"></a><span data-ttu-id="f3232-126">Svartlista föreslagna attribut</span><span class="sxs-lookup"><span data-stu-id="f3232-126">Blacklisting suggested attributes</span></span>
<span data-ttu-id="f3232-127">Om analysen föreslår ett attribut som du inte vill visa kan du Svartlista attributet.</span><span class="sxs-lookup"><span data-stu-id="f3232-127">If the analysis suggests an attribute that you do not want to see you can blacklist the attribute.</span></span> <span data-ttu-id="f3232-128">Var försiktig.</span><span class="sxs-lookup"><span data-stu-id="f3232-128">Use caution, however.</span></span> <span data-ttu-id="f3232-129">Svartlistade attribut föreslås inte för andra artiklar eller kontaktpersoner antingen.</span><span class="sxs-lookup"><span data-stu-id="f3232-129">Blacklisted attributes are not suggested for other items or contact persons either.</span></span> <span data-ttu-id="f3232-130">Du kan ångra Svartlistning av attribut genom att välja **Svartlistade attribut**, och ta bort attributet från listan.</span><span class="sxs-lookup"><span data-stu-id="f3232-130">If you regret blacklisting an attribute, you can choose **Blacklisted Attributes**, and then delete the attribute from the list.</span></span>

## <a name="to-enable-image-analyzer"></a><span data-ttu-id="f3232-131">Så här aktiverar du Image Analyzer</span><span class="sxs-lookup"><span data-stu-id="f3232-131">To enable Image Analyzer</span></span>
<span data-ttu-id="f3232-132">Tillägget Image Analyzer är inbyggt i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f3232-132">The Image Analyzer extension is built-in to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f3232-133">Du måste aktivera den.</span><span class="sxs-lookup"><span data-stu-id="f3232-133">You just need to turn it on.</span></span>

> [!NOTE]  
> <span data-ttu-id="f3232-134">Om du vill aktivera tillägget Image Analyzer, måste du vara administratör.</span><span class="sxs-lookup"><span data-stu-id="f3232-134">To enable the Image Analyzer extension, you must be an administrator.</span></span> <span data-ttu-id="f3232-135">Kontrollera att du har tilldelats användarbehörighetsuppsättning **SUPER**.</span><span class="sxs-lookup"><span data-stu-id="f3232-135">Make sure that you are assigned the **SUPER** user permission set.</span></span>

1. <span data-ttu-id="f3232-136">Om du vill aktivera tillägget Image Analyzer, gör du något av följande:</span><span class="sxs-lookup"><span data-stu-id="f3232-136">To enable the Image Analyzer extension, do one of the following:</span></span>

* <span data-ttu-id="f3232-137">Öppna en artikel eller kontaktkort.</span><span class="sxs-lookup"><span data-stu-id="f3232-137">Open an item or contact card.</span></span> <span data-ttu-id="f3232-138">I meddelandefältet, välj **analysera bilder**, och följ sedan stegen i assisterade inställningsguide.</span><span class="sxs-lookup"><span data-stu-id="f3232-138">In the notification bar, choose **Analyze Images**, and then follow the steps in the assisted setup guide.</span></span>  
* <span data-ttu-id="f3232-139">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Anslutningar till tjänst** och sedan **Inställningar för bildanalys**.</span><span class="sxs-lookup"><span data-stu-id="f3232-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose **Image Analysis Setup**.</span></span> <span data-ttu-id="f3232-140">Markera kryssrutan **Aktivera analysera bilder**, och följ sedan stegen i assisterade inställningsguide.</span><span class="sxs-lookup"><span data-stu-id="f3232-140">Choose the **Enable Image Analyzer** check box, and then complete the steps in the assisted setup guide.</span></span>  

>   [!TIP]  
>   <span data-ttu-id="f3232-141">Sidan **inställningar för analys av bilden** låter dig också öppna där du kan ändra graden av säkerhet för attributförslag.</span><span class="sxs-lookup"><span data-stu-id="f3232-141">The **Image Analysis Setup** page is also where you can change the degree of confidence for attribute suggestions.</span></span> <span data-ttu-id="f3232-142">Om du till exempel kräver en högre grad av säkerhet anger du en högre procentandel.</span><span class="sxs-lookup"><span data-stu-id="f3232-142">For example, if you want to require a greater degree of confidence, you can enter a higher percentage.</span></span>

## <a name="to-analyze-an-image-of-an-item"></a><span data-ttu-id="f3232-143">Så här analyserar du en bild av en artikel</span><span class="sxs-lookup"><span data-stu-id="f3232-143">To analyze an image of an item</span></span>
<span data-ttu-id="f3232-144">Följande steg beskriver hur du analyserar en bild som har hämtats innan du valde Image Analyzer-tillägget.</span><span class="sxs-lookup"><span data-stu-id="f3232-144">The following steps describe how to analyze an image that was imported before you enabled the Image Analyzer extension.</span></span>  

1. <span data-ttu-id="f3232-145">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="f3232-145">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f3232-146">Välj artikel och välj sedan åtgärden **analysera bild**.</span><span class="sxs-lookup"><span data-stu-id="f3232-146">Choose the item, and then choose the **Analyze Picture** action.</span></span>  
3. <span data-ttu-id="f3232-147">Sidan **Image Analyzer-attribut** visar identifierade attribut, konfidensintervall och annan information om attributet.</span><span class="sxs-lookup"><span data-stu-id="f3232-147">The **Image Analyzer Attributes** page displays the detected attributes, the confidence level, and other details about the attribute.</span></span> <span data-ttu-id="f3232-148">Använd alternativet **åtgärd att utföra** för att ange vad som ska ske med attributet.</span><span class="sxs-lookup"><span data-stu-id="f3232-148">Use the **Action to perform** options to specify what to do with the attribute.</span></span>  

>   [!TIP]  
>   <span data-ttu-id="f3232-149">Du kan lägga till namnet på attributet till artikelbeskrivningen genom att välja **lägga till en artikelbeskrivning**.</span><span class="sxs-lookup"><span data-stu-id="f3232-149">You can add the name of the attribute to the item description by choosing **Add to item description**.</span></span> <span data-ttu-id="f3232-150">Det kan exempelvis vara användbart för att snabbt lägga till detaljer.</span><span class="sxs-lookup"><span data-stu-id="f3232-150">For example, this can be useful for quickly adding detail.</span></span>  

## <a name="to-analyze-a-picture-of-a-contact-person"></a><span data-ttu-id="f3232-151">Så här analyserar du en bild av en kontaktperson</span><span class="sxs-lookup"><span data-stu-id="f3232-151">To analyze a picture of a contact person</span></span>
<span data-ttu-id="f3232-152">Följande steg beskriver hur du analyserar en bild som har hämtats innan du valde Image Analyzer-tillägget.</span><span class="sxs-lookup"><span data-stu-id="f3232-152">The following steps describe how to analyze an image that was imported before you enabled the Image Analyzer extension.</span></span>  

1. <span data-ttu-id="f3232-153">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kontakter** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="f3232-153">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f3232-154">Välj kontaktperson och välj sedan åtgärden **analysera bild**.</span><span class="sxs-lookup"><span data-stu-id="f3232-154">Choose the contact person, and then choose the **Analyze Picture** action.</span></span>  
3. <span data-ttu-id="f3232-155">På snabbfliken **profilfrågeformulär** granska förslagen och gör ändringar om det behövs.</span><span class="sxs-lookup"><span data-stu-id="f3232-155">On the **Profile Questionnaire** FastTab, review the suggestions, and make corrections if needed.</span></span>  

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a><span data-ttu-id="f3232-156">Använda ditt konto för Computer Vision API</span><span class="sxs-lookup"><span data-stu-id="f3232-156">To use your own account for the Computer Vision API</span></span>
<span data-ttu-id="f3232-157">Använd även ditt eget konto för Computer Vision API, till exempel om du vill analysera mer bilder än vad vi kan.</span><span class="sxs-lookup"><span data-stu-id="f3232-157">You can also use your own account for the Computer Vision API, for example, if you want to analyze more images than we allow.</span></span>  

1. <span data-ttu-id="f3232-158">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten") ange **Image Analyzer-inställningar** och sedan relevant länk..</span><span class="sxs-lookup"><span data-stu-id="f3232-158">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Image Analyzer Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f3232-159">Ange **API-URI** och **API-nyckeln** som du har fått för Computer Vision API.</span><span class="sxs-lookup"><span data-stu-id="f3232-159">Enter the **API URI** and **API Key** that you received for Computer Vision API.</span></span>  

>   [!NOTE]  
>   <span data-ttu-id="f3232-160">Du måste lägga till **/analysera** i slutet av API-URI, om den inte redan finns där.</span><span class="sxs-lookup"><span data-stu-id="f3232-160">You must add **/analyze** at the end of the API URI, if it isn't already there.</span></span> <span data-ttu-id="f3232-161">Som exempel: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.</span><span class="sxs-lookup"><span data-stu-id="f3232-161">For example: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.</span></span>

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a><span data-ttu-id="f3232-162">Om du vill se hur många analyser som du har kvar i den aktuella perioden</span><span class="sxs-lookup"><span data-stu-id="f3232-162">To see how many analyses you have left in the current period</span></span>
<span data-ttu-id="f3232-163">Du kan visa antalet analyser som du har gjort och hur många du ändå kan göra, under den aktuella perioden.</span><span class="sxs-lookup"><span data-stu-id="f3232-163">You can view the number of analyses you've done, and how many you can still do, in the current period.</span></span>  

1. <span data-ttu-id="f3232-164">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten") ange **Image Analyzer-inställningar** och sedan relevant länk..</span><span class="sxs-lookup"><span data-stu-id="f3232-164">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Image Analyzer Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f3232-165">**Gränstyp**, **begränsa värde**, och **Utförda analyser** ger användarinformation.</span><span class="sxs-lookup"><span data-stu-id="f3232-165">The **Limit type**, **Limit value**, and **Analyzes performed** provide the usage information.</span></span>  

## <a name="to-stop-using-the-image-analyzer-extension"></a><span data-ttu-id="f3232-166">SLuta använda tillägget Image Analyzer</span><span class="sxs-lookup"><span data-stu-id="f3232-166">To stop using the Image Analyzer extension</span></span>
1. <span data-ttu-id="f3232-167">Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Anslutningar till tjänst** och sedan **Inställningar för Image Analyzer**.</span><span class="sxs-lookup"><span data-stu-id="f3232-167">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose **Image Analyzer Setup**.</span></span>  
2. <span data-ttu-id="f3232-168">Avmarkera kryssrutan **Aktivera Image Analyzer**.</span><span class="sxs-lookup"><span data-stu-id="f3232-168">Clear the **Enable Image Analyzer** check box.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3232-169">Se även</span><span class="sxs-lookup"><span data-stu-id="f3232-169">See Also</span></span>
[<span data-ttu-id="f3232-170">Arbeta med artikelattribut</span><span class="sxs-lookup"><span data-stu-id="f3232-170">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
<span data-ttu-id="f3232-171">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="f3232-171">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="f3232-172">Komma igång</span><span class="sxs-lookup"><span data-stu-id="f3232-172">Getting Started</span></span>](product-get-started.md)  
