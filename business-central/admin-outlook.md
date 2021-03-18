---
title: Använda Business Central med Outlook | Microsoft Docs
description: Denna tjänst har långtgående integrering med Microsoft 365 så att du kan hantera alla dina affärskontakter och din e-post till kunder och leverantörer direkt i Outlook.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6d2e396b21f2d5de2bb341e864df031070df1ca4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377954"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Använda Business Central som en företagsinkorg i Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] innebär förmågan att hantera affärsinteraktioner med dina kunder och leverantörer, direkt i Microsoft Outlook. Med tillägget [!INCLUDE[prod_short](includes/prod_short.md)] kan du se ekonomiska data som relateras till kunder och leverantörer, samt visa och skicka ekonomiska dokument som t.ex offerter och fakturor.  

## <a name="getting-the-add-in"></a>Skaffa tillägget
Det är lätt att komma igång med tillägget [!INCLUDE[prod_short](includes/prod_short.md)] för Outlook. I den assisterade konfigurationen **Ställ in din företagsinkorg i Outlook** kan du ställa in anslutningen för dig själv och din organisation om din organisation använder Microsoft 365. Ange ditt Microsoft 365-användarnamn och lösenord om du uppmanas till det och tala om för oss om du vill få ett exempel på ett e-postmeddelande. Tilläggsprogrammet [!INCLUDE[prod_short](includes/prod_short.md)] läggs sedan till automatiskt till Outlook. Mer information finns i [minimi kraven för Outlook](product-requirements.md#outlook)  

När du sedan öppnar Outlook visas ett e-postmeddelanden från *Dynamics 365 Business Central-administratören*. De nya tilläggen läggs till på Outlook-menyfliken och i webbläsaren, kan du se tillägget [!INCLUDE[prod_short](includes/prod_short.md)] omedelbart ovanför e-postmeddelandets brödtext. Tillägget uppdateras regelbundet och du får ett meddelande att det finns en ny version för dig i Outlook.  

> [!TIP]
> Om du använder det nya Outlook i webben, sedan kan [!INCLUDE[prod_short](includes/prod_short.md)] tilläggsprogram vara dolda under **fler åtgärder**. Om du ofta använder tillägget kan du fästa det så att det alltid visas direkt. Mer information finns i [använda tilläggsprogram i Outlook på webben](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

Om du arbetar med mer än ett [!INCLUDE[prod_short](includes/prod_short.md)]-företag kan du enkelt växla mellan företag i Outlook. I åtgärdsfältet för tillägg, välj **Fler åtgärder**, så kan du se alternativet för att växla mellan företag.  

<!--TEMP-->
> [!NOTE]
> Växla mellan företag kräver [!INCLUDE[prod_short](includes/prod_short.md)] 2019 utgivningsplan 2 eller senare som meddelats i [utgivningsplan](/dynamics365-release-plan/2019wave2/dynamics365-business-central/switch-between-companies-business-inbox-outlook).

Vissa företag som använder Microsoft 365 begränsar användarnas behörigheter att använda tillägg. Du måste därför kontrollera att du har en Microsoft 365-prenumeration som omfattar e-post och som låter dig distribuera tillägg. Om du ändå vill testa tillägget kan du [prova Microsoft 365 gratis](https://www.microsoft.com/microsoft-365/try).  

## <a name="using-the-contact-insights-add-in"></a>Använda tillägget Information om kontakt
Anta att du får ett e-postmeddelande från en kund som vill ha en offert för vissa artiklar. Direkt i Outlook kan du öppna tilläggsprogrammet [!INCLUDE[prod_short](includes/prod_short.md)] som känner igen avsändaren som en kund, och öppnar kundkortet för hans företag. Från denna instrumentbräda kan du se översiktsinformation för kunden samt bläddra ned för mer detaljer för särskilda dokument. Du kan också studera kundens försäljninghistorik. Om det är en ny kontakt kan du skapa den som en kund i [!INCLUDE[prod_short](includes/prod_short.md)] utan att lämna Outlook.  

I tilläggsprogrammet kan du skapa en försäljningsoffert och skicka tillbaka den till kunden, utan att lämna Outlook. All information som du behöver för att skicka försäljningsofferten, finns i din företagsinkorg i Outlook.  
När du har angivit data kan du bokföra offerten. Därefter kan du skicka den med e-post. [!INCLUDE[prod_short](includes/prod_short.md)] skapar en .PDF-fil med försäljningsofferten och kopplar den till e-postmeddelandet som du har skrivit i tilläggsprogrammet.  

På samma sätt, om du får ett e-postmeddelande från en leverantör, använder du tillägget för att arbeta med leverantörs- och inköpsfakturor.  

Ibland vill du se fler fält än vad du kan se i tilläggsprogrammet, till exempel när du vill fylla i raderna i en faktura. För att ge mer utrymme att arbeta med, kan du öppna tilläggsprogrammet på en separat sida. Det är fortfarande en del avOutlook, men du har mer utrymme. När du anger data för dokumentet den öppnade vyn, sparas ändringar automatiskt. När du är klar med att ange data för dokumentet, kan du välja knappen **OK**. När du väljer tilläggsprogramramen i Outlook uppdateras dokumentet automatiskt med de ändringar som du gjorde i den öppnade vyn.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Skapa fakturor från dina möten
Vissa företag registrerar alla fakturerbara avtalade tider i Outlook-kalendern. Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du skapa fakturan för kunden från kalenderobjektet: öppna den avtalade tiden och du kan öppna tillägget [!INCLUDE[prod_short](includes/prod_short.md)], söka efter befintlig information eller skapa en faktura eller ett annat dokument där.  

## <a name="doing-quick-document-lookup"></a>Utföra snabb dokumentsökning
Tilläggsprogrammet [!INCLUDE[prod_short](includes/prod_short.md)] dokumentlänkar ger dig snabb åtkomst till de dokument som nämns i e-postmeddelande. Tilläggsprogrammet är tillgänglig för ett e-postmeddelande, om ett verifikationsnummer känns igen i meddelandets brödtext. När du öppnar tilläggsprogrammet får du en snabb åtkomst till dokumentet.  

Om du till exempel får ett e-postmeddelande som nämner texten *S-QUO100*, identifierar [!INCLUDE[prod_short](includes/prod_short.md)] projektet som en försäljningsoffert och du kan öppna dokumentet i Outlook. I Outlook, välj **Dokumentlänkar** omedelbart över e-postmeddelandets brödtext i Outlook. I Outlook Web App väljer du texten *S-QUO1001* i e-postmeddelandets brödtext.  

I tilläggsprogrammet dokumentlänkar kan du, ändra och vidta åtgärder med dokument, precis som du kan i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="adding-the-add-ins-manually"></a>Lägga till tillägg manuellt
Ibland kan tillägg inte läggas till automatiskt i Outlook. Även om du eller en arbetskamrat körde assisterad konfigurationsguide för företaget, kanske inte [!INCLUDE[prod_short](includes/prod_short.md)] finns i Outlook. Om det här problemet uppstår, kan du lägga till tillägget [!INCLUDE[prod_short](includes/prod_short.md)] manuellt.  

Först måste du kontrollera att du har tillgång till tillägg i Microsoft 365-kontot. Öppna Outlook i webbläsaren, öppna ett meddelande, välj **Fler åtgärder** (...) högst upp i meddelandet och välj **Hämta tillägg** längst ned i listan. Då öppnas sidan **Tillägg för Outlook** där du kan aktivera [!INCLUDE[prod_short](includes/prod_short.md)] för Outlook. När du sedan går tillbaka till Outlook, bör [!INCLUDE[prod_short](includes/prod_short.md)] skrivas ut.  

På samma sätt i den stationära Outlook-klienten kan du kontrollera att [!INCLUDE[prod_short](includes/prod_short.md)] finns med på sidan **Hämta tillägg**.  

I båda fallen, om [!INCLUDE[prod_short](includes/prod_short.md)] fortfarande inte visas måste du hämta tilläggsmanifestfilerna. För mer information, kontakta Microsoft 365-administratören.

## <a name="using-other-email-accounts"></a>Använda andra e-postkonton

Tilläggen är avsedda att användas med Microsoft 365. Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan administratören avgöra om du kan använda [!INCLUDE[prod_short](includes/prod_short.md)] tilläggen i Outlook. Mer information finns i artiklarna [Vilken e-postadress kan jag använda med [!INCLUDE[prod_short](includes/prod_short.md)]?](across-faq.md#email) och [Funktioner som kräver specifika omständigheter](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances?toc=/dynamics365/business-central/toc.json) samt avsnittet [Varför fungerar inte Outlook-tillägget för mina användare?](/dynamics365/business-central/dev-itpro/faq#why-doesnt-the-outlook-add-in-work-for-my-users?toc=/dynamics365/business-central/toc.json) i Vanliga frågor och svar i administratörsinnehållet.  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Komma igång](product-get-started.md)  
[Få Business Central på min mobila enhet](install-mobile-app.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Ekonomi](finance.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Minsta krav för Outlook](product-requirements.md#outlook)  
[Använda tillägg i Outlook på Internet](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]