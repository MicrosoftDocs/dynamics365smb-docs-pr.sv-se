---
title: "Använda tillägget Image Analyzer | Microsoft Docs"
description: "Detta tillägg låter dig analysera bilder av kontaktpersoner och artiklar för att söka efter egenskaper, så att du snabbt kan tillsätta dem i Finance and Operations, Business edition."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 06/19/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6b7db51399f965f290e8871c74b30b9925553f83
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---

# <a name="the-image-analyzer-extension-for-microsoft-finance-and-operations-business-edition"></a>Tillägget Image Analyzer i Microsoft Finance and Operations, Business edition
Tillägget Image Analyzer använder kraftfulla bildanalyser från Computer Vision API för Microsoft Cognitive Services för att identifiera attribut i bilder du importerar för artiklar och kontaktpersoner, så att du lätt kan gå igenom och tilldela dem. För artiklar, kan attribut vara om artikel är en tabell eller en bil eller om den är röd eller blå. För kontaktpersoner kan attribut vara kön och ålder.

Image Analyzer föreslår attribut baserat på etiketter som  Computer Vision API hittar och konfidensnivå. Som standard föreslås attribut endast om det är minst 80 % till att attributet är korrekt. Du kan ange en annan konfidensintervall, om det behövs. Mer information om hur etiketter och konfidensnivå fastställs finns [Computer Vision API](https://go.microsoft.com/fwlink/?linkid=851476).  

Image Analyzer är gratis [!INCLUDE[d365fin](includes/d365fin_md.md)], men det finns en gräns för hur många artiklar som du kan analysera under en viss tidsperiod. Som standard kan du analysera 100 bilder per månad.

När du har aktiverat tillägget körs Image Analyzer när du importerar en bild till en artikel eller kontaktperson. Du ser de attribut och konfidensnivå och information direkt och bestämmer vad du vill göra med varje attribut. Om du har importerat bilder innan du valde tillägget Image Analyzer måste du gå till artikel- eller kontaktkorten och välja åtgärd **analysera bild**.  

>   [!NOTE]  
>   Genom att aktivera det här tillägget accepterar du att Microsoft kan lagra data och använda den för att förbättra Microsoft-tjänster, som gör Computer Vision API bättre. För att skydda din integritet har vidtagit åtgärder för att göra data anonym och skydda den. Vi vill inte publicera informationen eller andra användare kan använda den. Du kan ta bort bilden från objekt i [!INCLUDE[d365fin](includes/d365fin_md.md)], men Computer Vision API  har fortfarande bilden sin avidentifierade form. Mer information finns i [Microsoft Trust Center](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Krav
Det finns några krav för bilder:

* Bildformat: JPEG, PNG, GIF, BMP  
* Maximal filstorlek: mindre än 4 MB  
* Bilddimensioner: större än 50 x 50 bildpunkter  

## <a name="blacklisting-suggested-attributes"></a>Svartlista föreslagna attribut
Om analysen föreslår ett attribut som du inte vill visa kan du Svartlista attributet. Var försiktig. Svartlistade attribut föreslås inte för andra artiklar eller kontaktpersoner antingen. Du kan ångra Svartlistning av attribut genom att välja **Svartlistade attribut**, och ta bort attributet från listan.

## <a name="to-enable-image-analyzer"></a>Så här aktiverar du Image Analyzer
Tillägget Image Analyzer är inbyggt i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du måste aktivera den.

> [!NOTE]  
> Om du vill aktivera tillägget Image Analyzer, måste du vara administratör. Kontrollera att du har tilldelats användarbehörighetsuppsättning **SUPER**.

1. Om du vill aktivera tillägget Image Analyzer, gör du något av följande:

* Öppna en artikel eller kontaktkort. I meddelandefältet, välj **analysera bilder**, och följ sedan stegen i assisterade inställningsguide.  
* Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Anslutningar till tjänst** och sedan **Inställningar för bildanalys**. Markera kryssrutan **Aktivera analysera bilder**, och följ sedan stegen i assisterade inställningsguide.  

>   [!TIP]  
>   Sidan **inställningar för analys av bilden** låter dig också öppna där du kan ändra graden av säkerhet för attributförslag. Om du till exempel kräver en högre grad av säkerhet anger du en högre procentandel.

## <a name="to-analyze-an-image-of-an-item"></a>Så här analyserar du en bild av en artikel
Följande steg beskriver hur du analyserar en bild som har hämtats innan du valde Image Analyzer-tillägget.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Artiklar** och välj sedan relaterad länk.  
2. Välj artikel och välj sedan åtgärden **analysera bild**.  
3. Sidan **Image Analyzer-attribut** visar identifierade attribut, konfidensintervall och annan information om attributet. Använd alternativet **åtgärd att utföra** för att ange vad som ska ske med attributet.  

>   [!TIP]  
>   Du kan lägga till namnet på attributet till artikelbeskrivningen genom att välja **lägga till en artikelbeskrivning**. Det kan exempelvis vara användbart för att snabbt lägga till detaljer.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Så här analyserar du en bild av en kontaktperson
Följande steg beskriver hur du analyserar en bild som har hämtats innan du valde Image Analyzer-tillägget.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kontakter** och välj sedan relaterad länk.  
2. Välj kontaktperson och välj sedan åtgärden **analysera bild**.  
3. På snabbfliken **profilfrågeformulär** granska förslagen och gör ändringar om det behövs.  

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Använda ditt konto för Computer Vision API
Använd även ditt eget konto för Computer Vision API, till exempel om du vill analysera mer bilder än vad vi kan.  

1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten") ange **Image Analyzer-inställningar** och sedan relevant länk..  
2. Ange **API-URI** och **API-nyckeln** som du har fått för Computer Vision API.  

>   [!NOTE]  
>   Du måste lägga till **/analysera** i slutet av API-URI, om den inte redan finns där. Som exempel: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Om du vill se hur många analyser som du har kvar i den aktuella perioden
Du kan visa antalet analyser som du har gjort och hur många du ändå kan göra, under den aktuella perioden.  

1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten") ange **Image Analyzer-inställningar** och sedan relevant länk..  
2. **Gränstyp**, **begränsa värde**, och **Utförda analyser** ger användarinformation.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>SLuta använda tillägget Image Analyzer
1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Anslutningar till tjänst** och sedan **Inställningar för Image Analyzer**.  
2. Avmarkera kryssrutan **Aktivera Image Analyzer**.  

## <a name="see-also"></a>Se även
[Arbeta med artikelattribut](inventory-how-work-item-attributes.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

