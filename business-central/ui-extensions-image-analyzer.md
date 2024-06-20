---
title: Tillägget Image Analyzer
description: 'Detta tillägg låter dig analysera bilder av kontaktpersoner och artiklar för att söka efter egenskaper, så att du snabbt kan tilldela dem i Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition'
ms.search.form: '2026, 2027, 2029,'
ms.date: 05/19/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="the-image-analyzer-extension"></a>Tillägget Image Analyzer

Tillägget Image Analyzer använder kraftfulla bildanalyser från Computer Vision API för Azure Cognitive Services för att identifiera attribut i bilder du importerar för artiklar och kontaktpersoner, så att du lätt kan gå igenom och tilldela dem. För artiklar, kan attribut vara om artikel är en tabell eller en bil eller om den är röd eller blå. För kontaktpersoner kan attribut vara kön och ålder.

Image Analyzer föreslår attribut baserat på etiketter som Computer Vision API hittar och konfidensnivå. Som standard föreslås attribut endast om det är minst 80 % till att attributet är korrekt. Du kan ange en annan konfidensintervall, om det behövs. Mer information om hur etiketter och konfidensnivå fastställs finns [Computer Vision API](https://go.microsoft.com/fwlink/?linkid=851476).  

Image Analyzer är gratis [!INCLUDE[prod_short](includes/prod_short.md)], men det finns en gräns för hur många artiklar som du kan analysera under en viss tidsperiod. Som standard kan du analysera 100 bilder per månad.

När du har aktiverat tillägget körs Image Analyzer när du importerar en bild till en artikel eller kontaktperson. Du ser de attribut och konfidensnivå och information direkt och bestämmer vad du vill göra med varje attribut. Om du har importerat bilder innan du valde tillägget Image Analyzer måste du gå till artikel- eller kontaktkorten och välja åtgärd **analysera bild**.  

## <a name="privacy-notice"></a>Sekretesspolicy

Det här tillägget använder API för visuellt innehåll från Azure Cognitive Services, som kan ha olika nivåer av att åtaganden än [!INCLUDE[prod_short](includes/prod_short.md)]. När du aktiverar tillägget Image Analyzer skickas kunddata som till exempel en kontaktbild eller en artikelbild till API för visuellt innehåll. Genom att installera det här tillägget godkänner för denna uppsättning data som ska skickas till API för visuellt innehåll. Observera att du kan inaktivera samt avinstallera tillägget Image Analyzer när som helst för att avbryta användningen av funktionen. Mer information finns i [Microsoft säkerhetscenter](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Krav

Det finns några krav för bilder:

* Bildformat: JPEG, PNG, GIF, BMP  
* Maximal filstorlek: mindre än 4 MB  
* Bilddimensioner: större än 50 x 50 bildpunkter  

## <a name="switch-on-the-image-analyzer-extension"></a>Aktivera tillägget Image Analyzer

Tillägget Image Analyzer är inbyggt i [!INCLUDE[prod_short](includes/prod_short.md)]. Du måste aktivera den.

> [!NOTE]  
> Om du vill aktivera tillägget Image Analyzer, måste du vara administratör. Kontrollera att du har tilldelats användarbehörighetsuppsättning **SUPER**. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).

Om du vill aktivera tillägget Image Analyzer, gör du något av följande:

* Öppna en artikel eller kontaktkort. I meddelandefältet, välj **analysera bild**, och följ sedan stegen i assisterade inställningsguide.  
* Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Serviceanslutningar** och väljer sedan **Bildanalysinställningar**. Markera kryssrutan **Aktivera analysera bilder**, och följ sedan stegen i assisterade inställningsguide.  

    > [!TIP]  
    > Sidan **inställningar för analys av bilden** låter dig också öppna där du kan ändra graden av säkerhet för attributförslag. Om du till exempel kräver en högre grad av säkerhet anger du en högre procentandel.

## <a name="analyze-an-item-image"></a>Analysera en artikelbild

Följande steg beskriver hur du analyserar en bild som har hämtats innan du valde Image Analyzer-tillägget.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2. Välj artikel och välj sedan åtgärden **analysera bild**.  
3. Sidan **Image Analyzer-attribut** visar identifierade attribut, konfidensintervall och annan information om attributet. Använd alternativen i **Åtgärd att utföra** för att ange vad som ska göras med attributet eller välj **Lägg till artikelbeskrivning** för att lägga till namnet på attributet till artikelbeskrivningen. Denna åtgärd kan vara användbar för att snabbt lägga till detaljer.

Fältet **Åtgärd att utföra** har följande alternativ:

| Åtgärd | Description |
| ------ | ----------- |
| *Ignorera* | Inga åtgärder utförs. |
| *Använd som attribut* | Värdet läggs till i attributen för artikeln. Mer information: [Arbeta artikelattribut](inventory-how-work-item-attributes.md). |
| *Använd som en kategori* | Det valda värdet läggs till som en kategori. Läs mer på [Kategoriartiklar](inventory-how-categorize-items.md). |
| *Lägg till i blockeringslista* | Om analysen föreslår ett attribut som du inte vill visa kan du blockera attributet. Var försiktig. Blockerade attribut föreslås inte för andra artiklar heller. Du kan ångra blockering av attribut genom att välja **Visa blockerade attribut** och ta bort attributet från listan. |

> [!NOTE]  
> Som standard visar **Artikelattribut** attribut där **Förtroendepoäng** är över **Förtroendepoängtröskel i procent** som definierats i **Bildanalysinställningar**. Om du vill visa alla identifierade attribut väljer du åtgärden **Visa alla attribut**.

## <a name="analyze-a-contact-person-picture"></a>Analysera en kontaktpersonsbild

Följande steg beskriver hur du analyserar en bild som har hämtats innan du valde Image Analyzer-tillägget.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kontakter** och väljer sedan relaterad länk.  
2. Välj kontaktperson och välj sedan åtgärden **analysera bild**.  
3. På snabbfliken **profilfrågeformulär** granska förslagen och gör ändringar om det behövs. Läs mer på [Använda profilfrågeformulär för att klassificera affärskontakter](marketing-create-contact-profile-questionnaire.md).  

    > [!NOTE]  
    >
    > Computer Vision API returnerar följande attribut:
    >
    > * *ålder*
    >
    >     En uppskattad "visuell ålder" i år. Det är hur gammal en person ser ut i motsats till den faktiska biologiska åldern.
    > * *kön*
    >
    >    Man eller kvinna.
    >
    > Computer Vision API returnerar inte förtroendenivå för ålders- och könsattribut.
  
## <a name="use-your-own-computer-vision-api-account"></a>Använda ditt konto för Computer Vision API

Använd även ditt eget konto för Computer Vision API, till exempel om du vill analysera mer bilder än vad standardintegreringen erbjuder.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inställningar för bildanalys** och väljer sedan relaterad länk.
2. Ange **API-URI** och **API-nyckeln** som du har fått för Computer Vision API.  

    > [!NOTE]  
    > Du måste lägga till **/analysera** i slutet av API-URI, om den inte redan finns där. Till exempel: ```https://cronus.api.cognitive.microsoft.com/vision/v2.0/analyze```.

## <a name="see-how-many-analyses-you-have-left-in-the-current-period"></a>Se hur många analyser som du har kvar i den aktuella perioden

Du kan visa antalet analyser som du har gjort och hur många du ändå kan göra, under den aktuella perioden.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inställningar för bildanalys** och väljer sedan relaterad länk.
2. **Gränstyp**, **Gränsvärde**, och **Utförda analyser** ger användarinformation.  

## <a name="stop-using-the-image-analyzer-extension"></a>Sluta använda tillägget Image Analyzer

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceanslutningar** och väljer sedan **Bildanalysinställningar**.  
2. Avmarkera fältet **Aktivera Image Analyzer**.  

Du kan också avinstallera tillägget helt. Du kan alltid hämta det igen från AppSource. Mer information finns i [Installera och avinstallera tillägg i Business Central](ui-extensions-install-uninstall.md#uninstall-an-app).  

## <a name="see-also"></a>Se även

[Arbeta med artikelattribut](inventory-how-work-item-attributes.md)  
[Kategorisera artiklar](inventory-how-categorize-items.md)  
[Använda profilfrågeformulär för att klassificera affärskontakter](marketing-create-contact-profile-questionnaire.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
