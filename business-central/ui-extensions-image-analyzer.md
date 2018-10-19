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
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 9a2d7999f3a4ecc3a597b6641ee1db69d754de4c
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---

# <a name="the-image-analyzer-extension"></a>Tillägget Image Analyzer
Tillägget Image Analyzer använder kraftfulla bildanalyser från Computer Vision API för Microsoft Cognitive Services för att identifiera attribut i bilder du importerar för artiklar och kontaktpersoner, så att du lätt kan gå igenom och tilldela dem. För artiklar, kan attribut vara om artikel är en tabell eller en bil eller om den är röd eller blå. För kontaktpersoner kan attribut vara kön och ålder.

Image Analyzer föreslår attribut baserat på etiketter som  Computer Vision API hittar och konfidensnivå. Som standard föreslås attribut endast om det är minst 80 % till att attributet är korrekt. Du kan ange en annan konfidensintervall, om det behövs. Mer information om hur etiketter och konfidensnivå fastställs finns [Computer Vision API](https://go.microsoft.com/fwlink/?linkid=851476).  

Image Analyzer är gratis [!INCLUDE[d365fin](includes/d365fin_md.md)], men det finns en gräns för hur många artiklar som du kan analysera under en viss tidsperiod. Som standard kan du analysera 100 bilder per månad.

När du har aktiverat tillägget körs Image Analyzer när du importerar en bild till en artikel eller kontaktperson. Du ser de attribut och konfidensnivå och information direkt och bestämmer vad du vill göra med varje attribut. Om du har importerat bilder innan du valde tillägget Image Analyzer måste du gå till artikel- eller kontaktkorten och välja åtgärd **analysera bild**.  

## <a name="privacy-notice"></a>Sekretesspolicy
Det här tillägget använder API för visuellt innehåll från Microsoft Cognitive Services, som kan ha olika nivåer av att åtaganden än [!INCLUDE[d365fin](includes/d365fin_md.md)]. När du aktiverar tillägget Image Analyzer skickas kunddata som till exempel en kontaktbild eller en artikelbild till API för visuellt innehåll. Genom att installera det här tillägget godkänner för denna uppsättning data som ska skickas till API för visuellt innehåll. Observera att du kan inaktivera samt avinstallera tillägget Image Analyzer när som helst för att avbryta användningen av funktionen. Mer information finns i [Microsoft Trust Center](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Krav
Det finns några krav för bilder:

* Bildformat: JPEG, PNG, GIF, BMP  
* Maximal filstorlek: mindre än 4 MB  
* Bilddimensioner: större än 50 x 50 bildpunkter  

## <a name="to-enable-image-analyzer"></a>Så här aktiverar du Image Analyzer
Tillägget Image Analyzer är inbyggt i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du måste aktivera den.

> [!NOTE]  
> Om du vill aktivera tillägget Image Analyzer, måste du vara administratör. Kontrollera att du har tilldelats användarbehörighetsuppsättning **SUPER**.

1. Om du vill aktivera tillägget Image Analyzer, gör du något av följande:

* Öppna en artikel eller kontaktkort. I meddelandefältet, välj **analysera bilder**, och följ sedan stegen i assisterade inställningsguide.  
* Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anslutningar till tjänst** och välj sedan **Inställningar för bildanalys**. Markera kryssrutan **Aktivera analysera bilder**, och följ sedan stegen i assisterade inställningsguide.  

    > [!TIP]  
    > Fönstret **Inställningar för bildanalys** låter dig också öppna där du kan ändra graden av säkerhet för attributförslag. Om du till exempel kräver en högre grad av säkerhet anger du en högre procentandel.

## <a name="to-analyze-an-image-of-an-item"></a>Så här analyserar du en bild av en artikel
Följande steg beskriver hur du analyserar en bild som har hämtats innan du valde Image Analyzer-tillägget.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.  
2. Välj artikel och välj sedan åtgärden **analysera bild**.  
3. Fönstret **Image Analyzer-attribut** visar identifierade attribut, konfidensintervall och annan information om attributet. Använd alternativet **åtgärd att utföra** för att ange vad som ska ske med attributet.  

    > [!TIP]  
    > Du kan lägga till namnet på attributet till artikelbeskrivningen genom att välja **lägga till en artikelbeskrivning**. Det kan exempelvis vara användbart för att snabbt lägga till detaljer.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Så här analyserar du en bild av en kontaktperson
Följande steg beskriver hur du analyserar en bild som har hämtats innan du valde Image Analyzer-tillägget.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontakter** och välj sedan relaterad länk.  
2. Välj kontaktperson och välj sedan åtgärden **analysera bild**.  
3. På snabbfliken **profilfrågeformulär** granska förslagen och gör ändringar om det behövs.  

## <a name="blacklisting-suggested-attributes"></a>Svartlista föreslagna attribut
Om analysen föreslår ett attribut som du inte vill visa kan du Svartlista attributet. Var försiktig. Svartlistade attribut föreslås inte för andra artiklar eller kontaktpersoner antingen. Du kan ångra Svartlistning av attribut genom att välja **Svartlistade attribut**, och ta bort attributet från listan.

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Använda ditt konto för Computer Vision API
Använd även ditt eget konto för Computer Vision API, till exempel om du vill analysera mer bilder än vad vi kan.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Image Analyzer-inställning** och välj sedan relaterad länk.  
2. Ange **API-URI** och **API-nyckeln** som du har fått för Computer Vision API.  

    > [!NOTE]  
    > Du måste lägga till **/analysera** i slutet av API-URI, om den inte redan finns där. Som exempel: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Om du vill se hur många analyser som du har kvar i den aktuella perioden
Du kan visa antalet analyser som du har gjort och hur många du ändå kan göra, under den aktuella perioden.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Image Analyzer-inställning** och välj sedan relaterad länk.  
2. **Gränstyp**, **begränsa värde**, och **Utförda analyser** ger användarinformation.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>SLuta använda tillägget Image Analyzer
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anslutningar till tjänst** och välj sedan **Inställningar för Image Analyzer**.  
2. Avmarkera kryssrutan **Aktivera Image Analyzer**.  

## <a name="see-also"></a>Se även
[Arbeta med artikelattribut](inventory-how-work-item-attributes.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Komma igång](product-get-started.md)  

