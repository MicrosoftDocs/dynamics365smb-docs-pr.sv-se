---
title: Använda Business Central med Outlook | Microsoft Docs
description: Denna tjänst har långtgående integrering med Office 365 så att du kan hantera alla dina affärskontakter och din e-post till kunder och leverantörer direkt i Outlook.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 08/14/2019
ms.author: edupont
ms.openlocfilehash: 70299f86a1ebc3251780eb05f8b68afeff23fa5e
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887697"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Använda Business Central som en företagsinkorg i Outlook
[!INCLUDE[d365fin](includes/d365fin_md.md)] innebär förmågan att hantera affärsinteraktioner med dina kunder och leverantörer, direkt i Microsoft Outlook. Med tillägget [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du se ekonomiska data som relateras till kunder och leverantörer, samt visa och skicka ekonomiska dokument som t.ex offerter och fakturor.  

## <a name="getting-the-add-in"></a>Skaffa tillägget
Det är lätt att komma igång med tillägget [!INCLUDE[d365fin](includes/d365fin_md.md)] för Outlook. I assisterade konfigurationen **Ställ in din företagsinkorg i Outlook** kan du ställa in anslutningen för dig själv och din organisation om din organisation använder Office 365. Ange ditt Office 365-användarnamn och lösenord om du uppmanas till det och tala om för oss om du vill få ett exempel på ett e-postmeddelande. Tilläggsprogrammet [!INCLUDE[d365fin](includes/d365fin_md.md)] läggs sedan till automatiskt till Outlook. Mer information finns i [minimi kraven för Outlook](product-requirements.md#outlook)  

När du sedan öppnar Outlook visas ett e-postmeddelanden från *Dynamics 365 Business Central-administratören*. De nya tilläggen läggs till på Outlook-menyfliken och i webbläsaren, kan du se tillägget [!INCLUDE[prodshort](includes/prodshort.md)] omedelbart ovanför e-postmeddelandets brödtext. Tillägget uppdateras regelbundet och du får ett meddelande att det finns en ny version för dig i Outlook.  

> [!TIP]
> Om du använder det nya Outlook i en webbläsare, sedan kan [!INCLUDE [prodshort](includes/prodshort.md)] tilläggsprogram vara dolda under **fler åtgärder**.

Vissa företag som använder Office 365 begränsar användarnas behörigheter att använda tillägg. Så bör du kontrollera att du har en Office 365-prenumeration som innehåller e-post och låter dig distribuera tillägg. Om du vill testa tillägget i alla fall kan du [prova Office 365 gratis](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Använda tillägget Information om kontakt
Anta att du får ett e-postmeddelande från en kund som vill ha en offert för vissa artiklar. Direkt i Outlook kan du öppna tilläggsprogrammet [!INCLUDE[d365fin](includes/d365fin_md.md)] som känner igen avsändaren som en kund, och öppnar kundkortet för hans företag. Från denna instrumentbräda kan du se översiktsinformation för kunden samt bläddra ned för mer detaljer för särskilda dokument. Du kan också studera kundens försäljninghistorik. Om det är en ny kontakt kan du skapa den som en kund i [!INCLUDE[d365fin](includes/d365fin_md.md)] utan att lämna Outlook.  

I tilläggsprogrammet kan du skapa en försäljningsoffert och skicka tillbaka den till kunden, utan att lämna Outlook. All information som du behöver för att skicka försäljningsofferten, finns i din företagsinkorg i Outlook.  
När du har angivit data kan du bokföra offerten. Därefter kan du skicka den med e-post. [!INCLUDE[d365fin](includes/d365fin_md.md)] skapar en .PDF-fil med försäljningsofferten och kopplar den till e-postmeddelandet som du har skrivit i tilläggsprogrammet.  

På samma sätt, om du får ett e-postmeddelande från en leverantör, använder du tillägget för att arbeta med leverantörs- och inköpsfakturor.  

Ibland vill du se fler fält än vad du kan se i tilläggsprogrammet, till exempel när du vill fylla i raderna i en faktura. För att ge mer utrymme att arbeta med, kan du öppna tilläggsprogrammet på en separat sida. Det är fortfarande en del avOutlook, men du har mer utrymme. När du anger data för dokumentet den öppnade vyn, sparas ändringar automatiskt. När du är klar med att ange data för dokumentet, kan du välja knappen **OK**. När du väljer tilläggsprogramramen i Outlook uppdateras dokumentet automatiskt med de ändringar som du gjorde i den öppnade vyn.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Skapa fakturor från dina möten
Vissa företag registrerar alla fakturerbara avtalade tider i Outlook-kalendern. Med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du skapa fakturan för kunden från kalenderobjektet: öppna den avtalade tiden och du kan öppna tillägget [!INCLUDE[d365fin](includes/d365fin_md.md)], söka efter befintlig information eller skapa en faktura eller ett annat dokument där.  

## <a name="doing-quick-document-lookup"></a>Utföra snabb dokumentsökning
Tilläggsprogrammet [!INCLUDE[d365fin](includes/d365fin_md.md)] dokumentlänkar ger dig snabb åtkomst till de dokument som nämns i e-postmeddelande. Tilläggsprogrammet är tillgänglig för ett e-postmeddelande, om ett verifikationsnummer känns igen i meddelandets brödtext. När du öppnar tilläggsprogrammet får du en snabb åtkomst till dokumentet.  

Om du till exempel får ett e-postmeddelande som nämner texten *S-QUO100*, identifierar [!INCLUDE[d365fin](includes/d365fin_md.md)] projektet som en försäljningsoffert och du kan öppna dokumentet i Outlook. I Outlook, välj **Dokumentlänkar** omedelbart över e-postmeddelandets brödtext i Outlook. I Outlook Web App väljer du texten *S-QUO1001* i e-postmeddelandets brödtext.  

I tilläggsprogrammet dokumentlänkar kan du, ändra och vidta åtgärder med dokument, precis som du kan i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="adding-the-add-ins-manually"></a>Lägga till tillägg manuellt
Ibland kan tillägg inte läggas till automatiskt i Outlook. Även om du eller en arbetskamrat körde assisterad konfigurationsguide för företaget, kanske inte [!INCLUDE[d365fin](includes/d365fin_md.md)] finns i Outlook. Om det här problemet uppstår, kan du lägga till tillägget [!INCLUDE[d365fin](includes/d365fin_md.md)] manuellt.  

Först måste du kontrollera att du har tillgång till tillägg i Office 365-kontot. Öppna Outlook i webbläsaren, öppna ett meddelande, välj **Fler åtgärder** (...) högst upp i meddelandet och välj **Hämta tillägg** längst ned i listan. Då öppnas sidan **Tillägg för Outlook** där du kan aktivera [!INCLUDE[prodshort](includes/prodshort.md)] för Outlook. När du sedan går tillbaka till Outlook, bör [!INCLUDE[prodshort](includes/prodshort.md)] skrivas ut.  

På samma sätt i den stationära Outlook-klienten kan du kontrollera att [!INCLUDE[d365fin](includes/d365fin_md.md)] finns med på sidan **Hämta tillägg**.  

I båda fallen, om [!INCLUDE[d365fin](includes/d365fin_md.md)] fortfarande inte visas måste du hämta tilläggsmanifestfilerna. För mer information, kontakta Office 365-administratören.

## <a name="using-other-email-accounts"></a>Använda andra e-postkonton

Tilläggen är avsedda att användas med Office 365. Om du använder [!INCLUDE [prodshort](includes/prodshort.md)] lokalt kan administratören avgöra om du kan använda [!INCLUDE [prodshort](includes/prodshort.md)] tilläggen i Outlook. Mer information finns i [vilken e-postadress kan jag använda med [!INCLUDE[prodshort](includes/prodshort.md)]?](across-faq.md#what-email-address-can-i-use-with-) och [funktioner som kräver särskilda omständigheter](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances).  

## <a name="see-also"></a>Se även

[Komma igång](product-get-started.md)  
[Få Business Central på min mobila enhet](install-mobile-app.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Ekonomi](finance.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Minsta krav för Outlook](product-requirements.md#outlook)  
[Använda tillägg i Outlook på Internet](https://support.office.com/en-us/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  
