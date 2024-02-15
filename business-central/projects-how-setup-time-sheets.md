---
title: Konfigurera tidrapporter och deras godkännande
description: 'Du lägger upp tidrapporter för att spåra den tid som använts för uppgifter och projekt, vilket hjälper dig med projekthantering, personal och kapacitet'
ms.reviewer: jswymer
author: brentholtorf
ms.author: bholtorf
mw.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77, 462'
ms.date: 07/27/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-time-sheets"></a>Så här skapar du tidrapporter

Tidrapporter i [!INCLUDE[prod_short](includes/prod_short.md)] hanterar tidregistrering veckovis, med sju dagars steg i taget. Du kan använda dem för att spåra den tid som används för projekt samt för att registrera enkel timregistrering för resurser. Innan du kan använda tidrapporter måste du ange vilka användare som ska skicka in tidrapporter och hur du vill konfigurera tidrapporterna.  

> [!TIP]
> De personer som använder tidrapporter utgör *resurser*. Därför kan du till exempel använda tidrapporter för att spåra arbete för icke-anställda. För att kunna spåra den egna personalens arbete, samt för att kunna använda tidrapporter för att spåra frånvaro bland personalen, måste du associera personal med resurser. Det finns en assisterad konfigurationsguide som kan hjälpa dig att göra det. Mer information om guiden finns i [Konfigurera tidrapporter med hjälp av guiden för assisterad konfiguration](#set-up-time-sheets-with-the-assisted-setup-guide).  

Du kan också ange om och hur tidrapporter ska godkännas. Beroende på organisationens behov kan du ange:

* En eller flera användare som tidrapportsadministratör och godkännare för alla tidrapporter.
* En tidrapportsgodkännare för varje resurs.

När du har konfigurerat tidrapporter kan du skapa dem för resurser, som i sin tur kan bokföra tidrapportrader. Alternativt kan du även tilldela tidrapporter till projektplaneringsrader. Mer information finns i [Använda tidrapporter](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Skapa tidrapporter med hjälp av guiden för assisterad konfiguration

Den assisterade konfigurationsguiden kan hjälpa dig konfigurera tidrapporter.  

> [!TIP]
> Om du har en version tidigare än utgivningscykel 1 (v22) från 2023 måste du aktivera funktionen **Funktionsuppdatering: Ny tidrapportupplevelse** på sidan [Funktionshantering](https://businesscentral.dynamics.com/?page=2610) för att kunna använda denna funktion.
>
> Med den här inställningen kan du också använda tidrapporter på mobila enheter.

Öppna guiden för assisterad konfiguration **Konfigurera tidrapporter** från sidan [Assisterad konfiguration](https://businesscentral.dynamics.com/?page=1801).

Guiden assisterad konfiguration går igenom följande steg:

1. Konfigurera deltagarna i tidrapportsprocesserna.

    På den första sidan i guiden visas antalet användare i din [!INCLUDE [prod_short](includes/prod_short.md)]. Här visas också annan obligatorisk och valfri information.  
2. Ange den första dagen i en arbetsvecka i denna organisation.

    Den första dagen i en arbetsvecka är den första dagen för alla tidrapporter.
3. Ange den person som administrerar tidrapporter.

    Den här personen kan redigera och ta bort alla tidrapporter. Du kan också lägga till samma roll för andra personer på sidan **användarinställningar**.
4. Konfigurera de resurser som ska använda tidrapporter, samt de personer som ska godkänna tidrapporter.

I slutet av installationshandboken kan du välja att [!INCLUDE [prod_short](includes/prod_short.md)] skapa tidrapporter baserat på din konfiguration. Visa de nya tidrapporterna på sidan **Tidrapporter**, som du kan öppna [här](https://businesscentral.dynamics.com/?page=951). Du kan också köra guiden assisterad konfiguration igen eller slutföra installationen manuellt.

> [!IMPORTANT]
> Om du använder utgivningscykel 1 för 2023 (v22) eller senare måste du, för att säkerställa att du kan hantera tidrapporter på mobila enheter, manuellt aktivera alternativet **Använd upplevelsen för ny tidrapport** för konfigurationen av tidrapport enligt beskrivningen i nästa procedur.

## <a name="set-up-time-sheets-manually"></a>Ställ in tidrapporter manuellt

I följande avsnitt beskrivs hur du konfigurerar tidrapporter om du inte använder guiden för assisterad konfiguration för **Konfigurera tidrapporter**.  

### <a name="set-up-general-information-for-time-sheets-manually"></a>Så här anger du allmän information för tidrapporter manuellt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Resurskonfiguration** och väljer sedan relaterad länk.  
1. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!IMPORTANT]
   > Om du använder utgivningscykel 1 för 2023 (v22) eller senare aktiverar du alternativet **Använd ny tidrapportsupplevelse** för att säkerställa att du kan hantera tidrapporter på mobila enheter.
1. För fältet **Tidrapport per projektgodkännande** väljer du ett av följande alternativ.

| Alternativ | Beskrivning |
| --- | --- |
| **Aldrig** |Användaren i fältet **Användar-ID för tidrapportens godkännare** på resurskortet godkänner tidrapporten. |
| **Alltid** |Användaren i fältet **Ansvarig person** på projektkortet godkänner tidrapporten. |
| **Enbart maskin** |Om maskinens tidrapport är länkad till ett projekt, godkänner användaren i fältet **Ansvarig person** på projektkortet tidrapporten. Om maskinens tidrapport är länkad till en resurs, godkänner användaren i fältet **Användar-ID för tidrapportens godkännare** på resurskortet tidrapporten. |

### <a name="assign-a-time-sheet-administrator-manually"></a>Så här tilldelar du en tidrapportsadministratör manuellt

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användarinställning** och väljer sedan relaterad länk.  
3. Välj den användare som ska vara tidrapportsadministratör, och välj sedan kryssrutan **Tidrapportadmin.**  

> [!TIP]  
> Vi rekommenderar att du endast anger en användare som tidrapportsadministratör för ett företag. I följande procedur skapar du en tidrapportägare och godkännare där tidrapportgodkännaren tilldelas för varje resurs.  

### <a name="assign-a-time-sheets-owner-and-approver-manually"></a>Så här tilldelar du en tidrapportsägare och en godkännare manuellt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Resurser** och väljer sedan relaterad länk.
2. Välj den resurs som du vill ställa in möjligheten att använda tidrapporter för, och markera sedan kryssrutan **Använd tidrapport**.  
3. I fältet **Användar-ID för tidrapportens ägare** anger du ID för ägaren av tidrapporten. Ägaren kan ange tidförbrukning på en tidrapport och skicka den för godkännande. Vanligtvis, när resursen är en person, är den person också ägare.  
4. I fältet **Användar-ID för tidrapportens godkännare** anger du ID för godkännaren av tidrapporten. Godkännaren kan godkänna, avvisa eller öppna en tidrapport igen.  

> [!NOTE]  
> Du kan inte ändra ID på tidrapportsgodkännaren om det finns tidrapporter som inte ännu har behandlats och har statusen **Skickad** eller **Öppen**.

## <a name="see-also"></a>Se även

[Använda tidrapporter för projekt](projects-how-use-time-sheets.md)  
[Så här skapar du tidrapporter](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Registrera förbrukning eller användning för projekt](projects-how-record-job-usage.md)  
[Ställa in projekthantering](projects-setup-projects.md)  
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
