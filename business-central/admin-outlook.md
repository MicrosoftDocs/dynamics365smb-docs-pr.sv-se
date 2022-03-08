---
title: Hämta Business Central-tillägget för Outlook
description: Lär dig installera Business Central-tillägget för Outlook för ditt företag eller för egen användning.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, Outlook
ms.search.form: 1831, 1832
ms.date: 08/13/2021
ms.author: jswymer
ms.openlocfilehash: 7d248158b7efa5960bbaeaf4b99f3ef8655b627c
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012373"
---
# <a name="get-the-business-central-add-in-for-outlook"></a>Hämta Business Central-tillägget för Outlook

Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du hantera affärsinteraktioner med dina kunder och leverantörer, direkt i Microsoft Outlook. Med [!INCLUDE[prod_short](includes/prod_short.md)] Outlook-tillägget kan du visa ekonomiska data som är relaterade till kunder och leverantörer. Du kan också skapa och skicka ekonomiska dokument, till exempel offerter och fakturor.  

Det finns två sätt att få fram Business Central-tillägget för Outlook installerat, beroende på din roll i organisationen:

- Som Microsoft 365-administratör använder du *Centraliserad distribution* för att installera tillägget automatiskt för hela organisationen, grupperna eller specifika användare.

- För varje användare installerar du tillägget för egen användning, om din administratör inte redan har distribuerat det åt dig.

## <a name="about-the-business-central-add-in-for-outlook"></a>Om Business Central-tillägget för Outlook

Business Central-tillägget för Outlook består av två mindre tillägg:

- Information om kontakt

    Det här tillägget ger användare med [!INCLUDE[prod_short](includes/prod_short.md)] kund- eller leverantörsinformation i Outlook-e-postmeddelanden och kalendermöten. Du kan också skapa och skicka [!INCLUDE[prod_short](includes/prod_short.md)] affärsdokument, t.ex. försäljningsofferter och fakturor till en kontakt. <!--To support these task, the add-in adds actions to the Outlook ribbon, in the **Business Central** group. --> 

- Dokumentvy

    När ett e-postmeddelande hänvisar till ett affärs dokumentnummer i e-postmeddelandet, ger det här tillägget en direkt, direkt länk från e-postmeddelandet till det verkliga affärsdokumentet i [!INCLUDE[prod_short](includes/prod_short.md)].

Mer information om vad du kan göra med tilläggen finns i [använda Business Central som inkorgen för företaget i Outlook](work-outlook-addin.md).

Varje tillägg tillhandahålls som en XML-fil, som kallas *manifest*, som måste installeras i Outlook för alla som vill använda den här funktionen. Dessa filer beskriver hur du aktiverar tilläggen och ansluter till Business Central när de används i Outlook. Arbetet med dessa filer utförs vanligtvis av en administratör. Som normal användare behöver du oftast inte hantera dessa filer direkt. Antingen konfigurerar din administratör tillägget så att det installeras automatiskt åt dig, eller så använder du den inbyggda installationen för att hantera installationen.

## <a name="deploy-the-add-in-by-using-centralized-deployment-as-an-admin"></a>Distribuera tillägget med hjälp av centraliserad distribution som en administratör

Centraliserad distribution är en funktion i administratörscentret för Microsoft 365 som du använder för att automatiskt installera tillägg i användarnas Office-appar, som Outlook. Det är det rekommenderade sättet för administratörer att distribuera Office-tillägg till användare och grupper inom organisationen.

> [!NOTE]
> För Business Central lokal, se [Konfigurera tillägget för Outlook-integration med Business Central lokal](/dynamics365/business-central/dev-itpro/administration/setting-up-office-add-ins-outlook-inbox) i administrationsinnehållet (endast engelska).

### <a name="prerequisites"></a>Förutsättningar

- En Microsoft 365-prenumeration  
- Användare tilldelas en Microsoft 365-licens  
- Ditt Microsoft 365-konto har rollen *Global administratör* eller *Exchange-administratör*

### <a name="deploy-the-add-in"></a>Distribuera tillägget

1. I Business Central, välj ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"). anger du **Assisterad konfiguration** och väljer sedan relaterad länk.
2. Välj **Outlook-tillägget centraliserad distribution** för att starta guiden för assisterad konfiguration.
3. Gå igenom den första sidan och välj **Nästa** för att öppna sidan för att hämta tilläggen.
4. Markera kryssrutan för de tillägg som du vill distribuera i kolumnen **distribution** och välj **Hämta och fortsätt**.

    En fil med namnet *OutlookAddins.zip* hämtas till enheten.

5. I det här skedet är du klar med det arbete som du behöver för att göra i Business Central, så du kan välja **klart**.

   >[!TIP]
   > Innan du väljer **Nästa** väljer du länken **Gå till Microsoft 365 (öppnar ett nytt fönster)** för att öppna och logga in på administrationscentret för Microsoft 365 i ett nytt webbläsarfönster. Du kommer att behöva gå till administrationscentret för Microsoft 365 i ett senare steg i alla fall.

6. Gå till mappen där OutlookAddins.zip har hämtats och extrahera filerna **Contact Insights.xml** och **Document View.xml** från zip-mappen till en valfri mapp.

    Mer information finns i [komprimera och packa upp filer och mappar](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).
7. Logga in på administrationscentret för Microsoft 365 och gå sedan till [Integrerade appar](https://go.microsoft.com/fwlink/?linkid=2163967).

8. Välj **överför egna appar**.
9. På sidan **Ladda upp appar att distribuera**, välj **Ladda upp manifest-fil (.xml) Ladda upp** > **Välj fil**.
10. Markera en av de filer som du har extraherat tidigare t.ex. **Content Insights.xml**.
11. Följ instruktionerna för att tilldela användare och distribuera tillägget.
12. Upprepa steg 9 till 11 för den andra tilläggsfilen om du vill.

> [!IMPORTANT]
> En grön bockmarkering visas när tillägget distribueras till administrationscentret. Det kan ta upp till 24 timmar innan användaren ser tillägget i automatiskt-appen. Användare kan behöva starta om Outlook även.

När du är klar kan du alltid ändra distributionen i administrationscentret för Microsoft 365, som att tilldela fler användare. Mer information om distribution av tillägg i administrationscenter finns i [distribuera tillägg i administrationscenter](/microsoft-365/admin/manage/manage-deployment-of-add-in).

## <a name="install-the-add-in-for-your-own-use"></a><a name="install"></a>Installera tillägget för egen användning

Om ditt företag tillåter det, kan du installera Business Central-tillägget för bara dig själv. Kontakta administratören om du är osäker.

1. I Business Central, välj ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"). ikonen, ange **Hämta Outlook-tillägget** och sedan väljer du relaterad länk.
2. Läs sidan och välj **Nästa** när du är klar.
3. Om du vill ta emot ett välkomstmeddelande från Business Central med en översikt över tillägget aktiverar du **Skicka exempel på e-postmeddelande**.
4. Välj **Slutför** för att slutföra installationen.

Business Central ansluter till e-postservern och installerar tillägget i Outlook. Det tar inte lång tid. Du är nu redo att börja använda tillägget i Outlook.

### <a name="for-business-central-on-premises"></a><a name="onprem"></a>För Business Central lokalt

Om du använder Business Central lokalt kan det vara något annorlunda att installera tillägget.

1. I Business Central, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikonen, ange **Hämta Outlook-tillägget** och sedan väljer du relaterad länk.
2. Läs sidan och välj **Nästa** när du är klar.
3. Gör något av följande, beroende på vilken sida du ser:

    - Om knappen **Installera till min Outlook** visas, väljer du den och allt är klart.
    - Om knappen **nästa** visas väljer du den. På nästa sida, om du vill ta emot ett välkomstmeddelande från Business Central med en översikt över tillägget aktiverar du **Skicka exempel på e-postmeddelande**. Välj sedan **Slutför** och allt är klart.
    - Om du ser knappen **Hämta tillägg** väljer du den och går sedan vidare till nästa steg.
4. När du väljer **Hämta tillägg** hämtas en fil med namnet *OutlookAddins.zip* till enheten. Filen bör visas längst upp i webbläsaren.

   Gå till mappen där OutlookAddins.zip har hämtats och extrahera filerna **Contact Insights.xml** och **Document View.xml** från zip-mappen till en valfri mapp. Mer information om hur du extraherar filer finns i [komprimera och packa upp filer och mappar](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).

5. Öppna Outlook och välj **Hämta tillägg** från menyfliksområdet. Eller, om du använder Outlook på webben, välj rullgardinsmenyn för alla nya eller befintliga e-postmeddelanden och välj sedan **Hämta tillägg**.
6. Välj **Mina tillägg** > **Lägg till ett anpassat tillägg** > **Lägg till från en fil**.
7. Välj en av de XML-filer som du extraherade, som **Contact Insights.xml**, sedan **Öppna** > **Installera**.
8. Upprepa steg 6 och 7 för den andra XML-filen om du har hämtat en.

Du är nu redo att börja använda tillägget i Outlook.

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