---
title: "Med hjälp av Dynamics 365 for Financials som din företagsinkorg i Outlook | Microsoft Docs"
description: "Med hjälp av Dynamics 365 for Financials som din företagsinkorg i Outlook"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 03/28/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a872c8817c412953a64cb1adb8f8234f2801e8fa
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-as-your-business-inbox-in-outlook"></a>Med hjälp av Dynamics 365 for Financials som din företagsinkorg i Outlook
[!INCLUDE[d365fin](includes/d365fin_md.md)] innebär förmågan att hantera affärsinteraktioner med dina kunder och leverantörer, direkt i Microsoft Outlook. Med tillägget [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du se ekonomiska data som relateras till kunder och leverantörer, samt visa och skicka ekonomiska dokument som t.ex offerter och fakturor.  

## <a name="get-the-add-in"></a>Få tilläggsprogrammet
I [!INCLUDE[d365fin](includes/d365fin_md.md)] är ett av stegen i den assisterade installationen Komma igång i fönstret **Sköt din verksamhet i Office 365**. I fönstret, när du väljer knappen **Konfigurera i Outlook** måste du ange ditt användarnamn och lösenord för Office 365. Tilläggsprogrammet [!INCLUDE[d365fin](includes/d365fin_md.md)] läggs sedan till automatiskt till Outlook.  

När du sedam öppnar Outlook visas ett e-postmeddelanden från Financials Admin. Den nya tilläggsprogrammet läggs till på Outlooks menyflik i Outlooks webbåtkomst. Du kan se den i menyfliken för tillägg omedelbart ovanför e-postmeddelandets brödtext. Själva tillägget uppdateras regelbundet och du får ett meddelande att det finns en ny version för dig i Outlook.  

Vissa företag som använder Office 365, begränsar användares behörigheter att distribuera tillägg. Så du måste kontrollera att du har en Office 365-prenumeration som innehåller e-postmeddelande och tillåter att du distribuerar tillägg. Om du vill testa tillägget i alla fall kan du [prova Office 365 gratis ](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Använda tilläggsprogrammet Information om kontakt
Anta att du får ett e-postmeddelande från en kund som vill ha en offert för vissa artiklar. Direkt i Outlook kan du öppna tilläggsprogrammet Financials som känner igen avsändaren som en kund, och öppnar kundkortet för hans företag. Från denna instrumentbräda kan du se översiktsinformation för kunden samt bläddra ned för mer detaljer för särskilda dokument. Du kan också studera kundens försäljninghistorik. Om det är en ny kund kan du skapa den som en kund i [!INCLUDE[d365fin](includes/d365fin_md.md)] utan att lämna Outlook.  

I tilläggsprogrammet kan du skapa en försäljningsoffert och skicka tillbaka den till kunden, utan att lämna Outlook. All information som du behöver för att skicka försäljningsofferten, finns i din företagsinkorg i Outlook.  
När du har angivit data kan du bokföra offerten. Därefter kan du skicka den med e-post. [!INCLUDE[d365fin](includes/d365fin_md.md)] skapar en .PDF-fil med försäljningsofferten och kopplar den till e-postmeddelandet som du har skrivit i tilläggsprogrammet.  

På samma sätt, om du får ett e-postmeddelande från en leverantör, använder du tillägget för att arbeta med leverantörs- och inköpsfakturor.  

Ibland vill du se fler fält än vad du kan se i tilläggsprogrammet, till exempel när du vill fylla i raderna i en faktura. För att ge mer utrymme att arbeta med, kan du öppna tilläggsprogrammet i ett separat fönster. Det är fortfarande en del avOutlook, men du har mer utrymme. När du anger data för dokumentet den öppnade vyn, sparas ändringar automatiskt. När du är klar med att ange data för dokumentet, kan du välja knappen **OK**. När du väljer tilläggsprogramramen i Outlook uppdateras dokumentet automatiskt med de ändringar som du gjorde i den öppnade vyn.  

## <a name="create-invoices-from-your-meeting-appointments"></a>Skapa fakturor från möten
Vissa företag registrerar alla fakturerbara avtalade tider i Outlook-kalendern. Med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du skapa fakturan för kunden från kalenderobjektet: öppna den avtalade tiden och du kan öppna tillägget [!INCLUDE[d365fin](includes/d365fin_md.md)], söka efter befintlig information eller skapa en faktura eller ett annat dokument där.  

## <a name="quick-document-lookup"></a>Snabb dokumentuppslagning
Tilläggsprogrammet [!INCLUDE[d365fin](includes/d365fin_md.md)] dokumentlänkar ger dig snabb åtkomst till de dokument som nämns i e-postmeddelande. Tilläggsprogrammet är tillgänglig för ett e-postmeddelande, om ett verifikationsnummer känns igen i meddelandets brödtext. När du öppnar tilläggsprogrammet får du en snabb åtkomst till dokumentet.  

Om du till exempel får ett e-postmeddelande som nämner texten *S-QUO100*, identifierar [!INCLUDE[d365fin](includes/d365fin_md.md)] projektet som en försäljningsoffert och du kan öppna dokumentet i Outlook. I Outlook, välj **Dokumentlänkar** omedelbart över e-postmeddelandets brödtext i Outlook. I Outlook Web App väljer du texten *S-QUO1001* i e-postmeddelandets brödtext.  

I tilläggsprogrammet dokumentlänkar kan du, ändra och vidta åtgärder med dokument, precis som du kan i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="adding-the-add-ins-manually"></a>Lägga till tillägg manuellt
Ibland kan tillägg inte läggas till automatiskt i Outlook. Även om du eller en arbetskamrat körde assisterad installationsguide för företaget, kanske inte [!INCLUDE[d365fin](includes/d365fin_md.md)] finns i Outlook. Om det här problemet uppstår, kan du lägga till tillägget [!INCLUDE[d365fin](includes/d365fin_md.md)] manuellt.  

Först måste du kontrollera att du har tillgång till tillägg i Office 365-kontot. Öppna Outlooks webbåtkomst i en webbläsare och lägg sedan till `/owa/#path=/options/manageapps` till URL-adressen i adressfältet. Då öppnas sidan **Hantera tillägg** där du kan aktivera Financials för Outlook. När du sedan går tillbaka till Outlook, bör [!INCLUDE[d365fin](includes/d365fin_md.md)] skrivas ut.  

På samma sätt i den stationära Outlook-klienten kan du kontrollera att [!INCLUDE[d365fin](includes/d365fin_md.md)] finns med i fönstret **Hantera tillägg**.  

I båda fallen, om [!INCLUDE[d365fin](includes/d365fin_md.md)] fortfarande inte visas måste du hämta tilläggsmanifestfilerna. Mer information finns i , eller kontakta Office 365-administratören.

## <a name="see-also"></a>Se även
[Välkommen till [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Ekonomi](finance.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  

