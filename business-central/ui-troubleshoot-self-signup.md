---
title: "Felsök problem med registrering av Self Service | Microsoft Docs"
description: "Få veta mer om de vanligaste orsakerna till varför du kanske inte kan slutföra registreringen till Business Central, samt hur du åtgärdar dem."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: f1d432ae73696e9e81bdc96c939051b676008e54
ms.contentlocale: sv-se
ms.lasthandoff: 05/28/2018

---
# <a name="troubleshooting-self-service-sign-up"></a>Felsöka registrering av Self Service
Det går enkelt och snabbt att registrera sig för [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan skapa ett gratis konto, även om du är en befintlig organisation. Detta inlägg tar upp frågor som du kan ha under registreringen.

## <a name="what-email-address-can-i-use-with-business-central"></a>Vilken e-postadress kan jag använda med Business Central?
[!INCLUDE[d365fin](includes/d365fin_md.md)] kräver att du använder en e-postadress från ditt arbete eller skola för att registrera dig. [!INCLUDE[d365fin](includes/d365fin_md.md)] har inte stöd för e-postadresser som tillhandahålls av e-posttjänster för konsumenter eller telekommunikationsleverantörer. Dessa omfattar outlook.com, hotmail.com, gmail.com, etc..

Om du försöker att registrera dig med en personlig e-postadress kommer du att få ett meddelande som indikerar att du använder en e-postadress från arbete eller skola.

## <a name="troubleshooting"></a>Felsökning
I många fall kan registrering för [!INCLUDE[d365fin](includes/d365fin_md.md)] göras genom att följa registreringsprocessen. Men det finns flera anledningar till att du inte kan slutföra registrering av Self Service. Tabellen nedan summerar några av de vanligaste orsakerna till att du inte kan slutföra registreringen och lösningar till dessa problem.

| Symptom/felmeddelande | Orsak och lösning |
| --- | --- |
| För Office 365-e-postadresser som inte är registrerade i ett land som stöds får du ett meddelande liknande detta under registreringen:<br /><br />**Vi har inte stöd för ditt land eller din region ännu.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] stöder för närvarande endast Office 365-e-postkonton som är registrerade på ett begränsat antal marknader. För mer information, se [Regional disposition](#regional-availability). |
| Personliga e-postadress som till exempel nancy@gmail.com stöds inte. Du får ett meddelande som följande under registreringen:<br /><br />**Du angav en personlig e-postadress: ange din e-postadress för arbetet så att vi kan lagra dina företagsdata på ett säkert sätt.**<br> eller <br> **Som ser ut som en personlig e-postadress. Ange din jobbadress så att vi kan ansluta dig till andra i företaget. Och oroa dig inte. Vi delar inte din adress med vem som helst.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] har inte stöd för e-postadresser som tillhandahålls av e-posttjänster för konsumenter eller telekommunikationsleverantörer. För att slutföra registreringen kan du försöka igen genom att använda en e-postadress som tilldelats av ditt arbete eller skola. Om du fortfarande inte kan registrera och är villig att slutföra en mer avancerad installationsprocess, kan du registrera dig för en ny Office 365 provprenumeration och använda den e-postadressen till att registrera dig. |
| .gov eller .mil-e-postadress får du ett meddelande som följande under registrering:<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] är inte tillgänglig: [!INCLUDE[d365fin](includes/d365fin_md.md)] är inte tillgängligt för användare med e-postadresser som t.ex. .gov eller .mil just nu. Använd en annan jobbadress eller med kom tillbaka senare.** <br>eller <br>**Vi kan inte lutföra registreringen. Det ser ut som att [!INCLUDE[d365fin](includes/d365fin_md.md)] inte är tillgängligt för ditt arbete eller skola.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] har inte stöd för e-postadresserna .gov eller .mil för tillfället. |
| Registrering av Self Service har inte aktiverats. Du får ett meddelande som följande under registreringen:<br /><br />**Vi kan inte slutföra registreringen. IT-avdelningen har inaktiverat registrering för [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kontakta dem för fullständig registrering.** <br>eller <br> **Som ser ut som en personlig e-postadress. Ange din jobbadress så att vi kan ansluta dig till andra i företaget. Och oroa dig inte. Vi delar inte din adress med vem som helst.** |Din organisations IT-administratör har inaktiverat registrering av Self Service för [!INCLUDE[d365fin](includes/d365fin_md.md)]. För att slutföra registreringen kontaktar du din IT-administratör och be dem att följa instruktionerna på sidan för att låta befintliga användare registrera sig i [!INCLUDE[d365fin](includes/d365fin_md.md)] och låta nya användare gå med din befintliga klientorganisation. Du kan även få detta problem om du registrerade dig på Office 365 via en partner. |
| E-postadressen är inte ett Office 365-ID. Du får ett meddelande som följande under registreringen:<br /><br />**Vi hittar inte dig på contoso.com. Använder du ett annat ID på arbetet eller i skolan? Försök logga in med det och om det inte fungerar kan du kontakta IT-avdelningen.** |Dina organisation använder ID för att logga in på Office 365 och andra Microsoft-tjänster, som skiljer sig från din e-postadress. Din e-postadress kan till exempel vara Nancy.Smith@contoso.com men ditt ID är nancys@contoso.com. Använd det användar-id som organisationen har tilldelat för att logga in på Office 365 eller någon annan Microsoft-tjänst för att slutföra registreringen. Om du inte vet vad det är kontaktar du din IT-administratör. Om du fortfarande inte kan registrera och är villig att slutföra en mer avancerad installationsprocess, kan du registrera dig för en ny Office 365 provprenumeration och använda den e-postadressen till att registrera dig. |
| Om ditt Office 365-konto har registrerats i ett land som stöds och du registrerar dig för [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett annat land, visas ett meddelande liknande följande i samband med registrering:<br /><br />**Vi har inte stöd för ditt land eller din region ännu.**| Organisationens Office 365-prenumeration har registrerats för ett specifikt land i Office 365-administrationsportalen. Registreringsupplevelsen för [!INCLUDE[d365fin](includes/d365fin_md.md)] använder samma språk och nationella inställningar som den aktuella webbläsaren, och därmed kan du få du felmeddelandet trots att du befinner dig i ett land som stöds. Be IT-administratören att kontrollera det land som anges i organisationsprofilen i [Office 365-administrationsportalen](https://portal.office.com/adminportal/home#/companyprofile). Du kanske måste använda ett annat konto för [!INCLUDE[d365fin](includes/d365fin_md.md)].|

## <a name="regional-availability"></a>Regional tillgänglighet
[!INCLUDE[d365fin](includes/d365fin_md.md)] finns just nu på följande marknader:

| Europa | Nordamerika |
| --- | --- |
| Österrike | Kanada |
| Belgien | USA |
| Danmark | |
| Tyskland | |
| Finland | |
| Frankrike | |
| Italienska | |
| Nederländerna | |
| Spanien | |
| Sverige | |
| Schweiz | |
| Storbritannien | |

## <a name="see-also"></a>Se även
[Välkommen till [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](index.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

