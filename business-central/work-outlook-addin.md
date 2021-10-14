---
title: Använda Business Central med Outlook | Microsoft Docs
description: Denna tjänst har långtgående integrering med Microsoft 365 så att du kan hantera alla dina affärskontakter och din e-post till kunder och leverantörer direkt i Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 08/13/2021
ms.author: jswymer
ms.openlocfilehash: 5de1ae4dc96419d848103a8b4ea9e11113793242
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589531"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Använda Business Central som en företagsinkorg i Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] erbjuder ett tillägg som gör dig redo att hantera affärsinteraktioner med dina kunder och leverantörer, direkt i Microsoft Outlook. Med tillägget [!INCLUDE[prod_short](includes/prod_short.md)] för avsnittet kan du se ekonomiska data som relateras till kunder och leverantörer, samt visa och skicka ekonomiska dokument som t.ex offerter och fakturor.

[!INCLUDE[prod_short](includes/prod_short.md)] tillägget består av två separata tillägg som ger följande funktioner:

- Information om kontakt

   Med det här tillägget kan du slå upp [!INCLUDE[prod_short](includes/prod_short.md)] kund- eller leverantörsinformation i Outlook-e-postmeddelanden och kalendermöten. Du kan också skapa och skicka [!INCLUDE[prod_short](includes/prod_short.md)] affärsdokument, t.ex. försäljningsofferter och fakturor till en kontakt.

- Dokumentvy

   När ett affärsdokument skickas i ett e-postmeddelande ger tillägget en direkt länk från e-postmeddelandet till det faktiska affärsdokumentet i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="get-started"></a>Kom igång

1. Det första du gör är att hämta [!INCLUDE[prod_short](includes/prod_short.md)] tillägget som installeras i Outlook. Administratören kanske redan har installerat tillägget. Om du inte är säker kan du be administratören att kontrollera om den är installerad eller se nästa steg.

    Om tillägget inte har installerats för dig läser du [installera tillägget för egen användning](admin-outlook.md#install). 

2. Med tillägget installerat kan du komma åt **[!INCLUDE[prod_short](includes/prod_short.md)]** tillägget från alla nya eller befintliga e-postmeddelanden eller avtalade tider i Outlook.

    Börja med att logga in i Outlook och öppna ett e-postmeddelande. Om du använder Outlook-appen går du till menyfliken och söker efter **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Eller om du använder Outlook på webben, längst upp eller längst ner i e-postmeddelandet, leta efter ![ikonen Business Central tillägg i Outlook.](media/outlook-business-central-icon.png) Eller gå till fler åtgärder ![Visa fler åtgärder för ett e-postmeddelande i Outlook.](media/outlook-more-actions-button.png) knappen.

    ![Få tillägg till Business Central-tillägg i Outlook.](media/outlook-business-central-addin.png)

   Om du har installerat tillägget och valt att få ett e-postmeddelande, bör du kontrollera Inkorgen för välkomstmeddelandet. I det här e-postmeddelandet finns information som hjälper dig att komma igång.

Första gången du använder tillägget i en [!INCLUDE[prod_short](includes/prod_short.md)] tilläggsruta kan du bli ombedd att logga in. I så fall väljer du **Logga in nu** och följer instruktionerna på skärmen för att logga in på Business Central med ditt konto.

> [!TIP]
> Om du använder den nya Outlook-webbplatsen på webben kan du fästa dem **[!INCLUDE[prod_short](includes/prod_short.md)]** så att de alltid visas direkt, i stället för att behöva gå till knappen fler åtgärder, vilket gör det enkelt att visa information om kontakter medan du bläddrar igenom olika e-postmeddelanden.

Mer information finns i [använda tilläggsprogram i Outlook på webben](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## <a name="work-with-contacts-and-documents-using-the-contact-insights-add-in"></a>Arbeta med kontakter och dokument med hjälp av tillägget för information om kontakter

Anta att du får ett e-postmeddelande från en kund som vill ha en offert för vissa artiklar. Direkt i Outlook kan du öppna tilläggsprogrammet [!INCLUDE[prod_short](includes/prod_short.md)] som känner igen avsändaren som en kund, och öppnar kundkortet för hans företag. Från denna instrumentbräda kan du se översiktsinformation för kunden samt bläddra ned för mer detaljer för särskilda dokument. Du kan också studera kundens försäljninghistorik. Om det är en ny kontakt kan du skapa den som en kund i [!INCLUDE[prod_short](includes/prod_short.md)] utan att lämna Outlook.  

I tilläggsprogrammet kan du skapa en försäljningsoffert och skicka tillbaka den till kunden, utan att lämna Outlook. All information som du behöver för att skicka försäljningsofferten, finns i din företagsinkorg i Outlook. När du har angivit data kan du bokföra offerten och skicka det via e-post. [!INCLUDE[prod_short](includes/prod_short.md)] skapar en .PDF-fil med försäljningsofferten och kopplar den till e-postmeddelandet som du har skrivit i tilläggsprogrammet.  

På samma sätt, om du får ett e-postmeddelande från en leverantör, använder du tillägget för att arbeta med leverantörs- och inköpsfakturor.  

Ibland vill du se fler fält än vad du kan se i tilläggsprogrammet, till exempel när du vill fylla i raderna i en faktura. För att ge mer utrymme att arbeta med, kan du öppna tilläggsprogrammet på en separat sida. Det är fortfarande en del avOutlook, men du har mer utrymme. När du anger data för dokumentet den öppnade vyn, sparas ändringar automatiskt. I följande avsnitt får du hjälp med några grundläggande uppgifter för att ge dig en allmän förståelse för hur du använder den.

> [!TIP]
> Uppgifterna beskriver hur du använder tillägget från ett e-postmeddelande. Men du kan göra detsamma i en avtalad tid i Outlook.

### <a name="look-up-a-business-contact-when-composing-an-email"></a>Slå upp en företagskontakt när du skriver ett e-postmeddelande

1. Skapa ett nytt e-postmeddelande.
2. I menyfliksområdet, gå till **[!INCLUDE[prod_short](includes/prod_short.md)]** och välj **Information om kontakt**. Eller om du använder Outlook på webben, längst upp eller längst ner i e-postmeddelandet, välj ![ikonen Business Central tillägg i Outlook.](media/outlook-business-central-icon.png) > **Information om kontakt**.
3. I **[!INCLUDE[prod_short](includes/prod_short.md)]** tilläggsrutan som öppnas söker du efter och väljer den kontakt du vill använda.

    En översikt över kontakten visas i rutan och kontakten läggs till på raden **till** i e-postmeddelandet.

### <a name="view-and-change-the-contact-details-or-switch-company"></a>Visa och ändra kontaktinformation eller växla företag

Åtgärds fältet högst upp i [!INCLUDE[prod_short](includes/prod_short.md)] tilläggsrutan innehåller flera åtgärder som gör att du kan gå djupare till detaljer om kontakten och ändra saker.

![Business Central-tillägg i åtgärdsfältet i Outlook.](media/outlook-addin-action-bar.png)

Du kan t.ex. öppna den fullständiga kontaktinformationen som visas i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du arbetar med mer än ett [!INCLUDE[prod_short](includes/prod_short.md)]-företag kan du enkelt växla mellan företag.

### <a name="track-incoming-documents"></a>Spåra inkommande dokument 

Du kanske använder listan **inkommande dokument** i [!INCLUDE[prod_short](includes/prod_short.md)] för att spåra dokument för bearbetning av leverantörer som skickar till dig, till exempel en inköpsfaktura som ska betalas. Om du gör det kan du enkelt skapa poster för inkommande dokument från Outlook-tillägget och inkludera bifogade filer i e-postmeddelandet.

1. När du tar emot ett e-postmeddelande från en leverantör som har en bifogad fil, väljer du ![ikonen Business Central tillägg i Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Information om kontakt**. 

2. I åtgärdsfältet för tillägget, välj **Visa fler åtgärder**, välj **Skicka till inkommande dokument…**. 

### <a name="create-and-send-new-document-to-a-contact"></a>Skapa och skicka ett nytt dokument till en kontakt

1. Välj i menyfliksområdet eller längst ned i e -postmeddelandet ![ikonen Business Central tillägg i Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Nytt** och välj sedan den typ av dokument som du vill skapa, t.ex. **försäljningsoffert**.
2. Gör ändringar i dokumentet i **[!INCLUDE[prod_short](includes/prod_short.md)]** tilläggsrutan.
3. När dokumentet är klart att skickas till kontakten kan du välja **Visa fler åtgärder** och sedan välja åtgärden **Skicka via e-post** i åtgärdsfältet.

## <a name="view-a-document-from-an-email-using-the-document-view-add-in"></a>Visa ett dokument från ett e-postmeddelande med tillägget dokumentvisning

Oavsett om det är ett e-postmeddelande som du har skickat eller tagit emot kan du välja ett [!INCLUDE[prod_short](includes/prod_short.md)] dokument, till exempel försäljningsofferten, direkt i Outlook. Därifrån kan du göra ändringar och navigera till relaterad information &mdash; på samma sätt som i [!INCLUDE[prod_short](includes/prod_short.md)].

Om du använder Outlook-appen väljer du bara **dokumentlänk** högst upp i e-postmeddelandet. För Outlook på webben söker du efter länken dokumentreferens i e-postmeddelandet. Referenslänktexten kommer att innehålla verifikationsnumret som baseras på nummerserien som används i [!INCLUDE[prod_short](includes/prod_short.md)]. Till exempel skulle länken för en försäljningsoffert vara ungefär **försäljningsoffert S-QUO1000**.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Få Business Central på min mobila enhet](install-mobile-app.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Ekonomi](finance.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Minsta krav för Outlook](product-requirements.md#outlook)  
[Använda tillägg i Outlook på Internet](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]