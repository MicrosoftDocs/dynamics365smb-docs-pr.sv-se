---
title: "Felsöka registrering av Self Service | Microsoft Docs "
description: "Felsök Azure AD-problem vid registrering."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2016
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 9bd980c6c6172d736915119806c0ba154b22bc8a
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="troubleshooting-self-service-sign-up"></a>Felsöka registrering av Self Service
Det går enkelt och snabbt att registrera sig för [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan skapa ett gratis konto, även om du är en befintlig organisation. Detta inlägg tar upp frågor som du kan ha under registreringen.

## <a name="what-email-address-can-i-use-with-financials"></a>Vilken e-postadress kan jag använda med Financials?
[!INCLUDE[d365fin](includes/d365fin_md.md)] kräver att du använder en e-postadress från ditt arbete eller skola för att registrera dig. [!INCLUDE[d365fin](includes/d365fin_md.md)] har inte stöd för e-postadresser som tillhandahålls av e-posttjänster för konsumenter eller telekommunikationsleverantörer. Dessa omfattar outlook.com, hotmail.com, gmail.com, etc..

Om du försöker att registrera dig med en personlig e-postadress kommer du att få ett meddelande som indikerar att du använder en e-postadress från arbete eller skola.

## <a name="troubleshooting"></a>Felsökning
I många fall kan registrering för [!INCLUDE[d365fin](includes/d365fin_md.md)] göras genom att följa registreringsprocessen. Men det finns flera anledningar till att du inte kan slutföra registrering av Self Service. Tabellen nedan summerar några av de vanligaste orsakerna till att du inte kan slutföra registreringen och lösningar till dessa problem.

| Symptom/felmeddelande | Orsak och lösning |
| --- | --- |
| För Office 365 e-postadresser, som inte är registrerade i USA, får du ett meddelande som detta under registreringen:<br /><br />**Vi har inte stöd för ditt land eller din region ännu.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] har för närvarande endast stöd för Office 365 USA-registrerade e-postkonton. |
| Personliga e-postadress som till exempel nancy@gmail.com stöds inte. Du får ett meddelande som följande under registreringen:<br /><br />**Du angav en personlig e-postadress: ange din e-postadress för arbetet så att vi kan lagra dina företagsdata på ett säkert sätt.**<br> eller <br> **Som ser ut som en personlig e-postadress. Ange din jobbadress så att vi kan ansluta dig till andra i företaget. Och oroa dig inte. Vi delar inte din adress med vem som helst.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] har inte stöd för e-postadresser som tillhandahålls av e-posttjänster för konsumenter eller telekommunikationsleverantörer. För att slutföra registreringen kan du försöka igen genom att använda en e-postadress som tilldelats av ditt arbete eller skola. Om du fortfarande inte kan registrera och är villig att slutföra en mer avancerad installationsprocess, kan du registrera dig för en ny Office 365 provprenumeration och använda den e-postadressen till att registrera dig. |
| .gov eller .mil-e-postadress får du ett meddelande som följande under registrering:<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] är inte tillgänglig: [!INCLUDE[d365fin](includes/d365fin_md.md)] är inte tillgängligt för användare med e-postadresser som t.ex. .gov eller .mil just nu. Använd en annan jobbadress eller med kom tillbaka senare.** <br>eller <br>**Vi kan inte lutföra registreringen. Det ser ut som att [!INCLUDE[d365fin](includes/d365fin_md.md)] inte är tillgängligt för ditt arbete eller skola.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] har inte stöd för e-postadresserna .gov eller .mil för tillfället. |
| Registrering av Self Service har inte aktiverats. Du får ett meddelande som följande under registreringen:<br /><br />**Vi kan inte slutföra registreringen. IT-avdelningen har inaktiverat registrering för [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kontakta dem för fullständig registrering.** <br>eller <br> **Som ser ut som en personlig e-postadress. Ange din jobbadress så att vi kan ansluta dig till andra i företaget. Och oroa dig inte. Vi delar inte din adress med vem som helst.** |Din organisations IT-administratör har inaktiverat registrering av Self Service för [!INCLUDE[d365fin](includes/d365fin_md.md)]. För att slutföra registreringen kontaktar du din IT-administratör och be dem att följa instruktionerna på sidan för att låta befintliga användare registrera sig i [!INCLUDE[d365fin](includes/d365fin_md.md)] och låta nya användare gå med din befintliga klientorganisation. Du kan även få detta problem om du registrerade dig på Office 365 via en partner. |
| E-postadressen är inte ett Office 365-ID. Du får ett meddelande som följande under registreringen:<br /><br />**Vi hittar inte dig på contoso.com. Använder du ett annat ID på arbetet eller i skolan? Försök logga in med det och om det inte fungerar kan du kontakta IT-avdelningen.** |Dina organisation använder ID för att logga in på Office 365 och andra Microsoft-tjänster, som skiljer sig från din e-postadress. Din e-postadress kan till exempel vara Nancy.Smith@contoso.com men ditt ID är nancys@contoso.com. Använd det användar-id som organisationen har tilldelat för att logga in på Office 365 eller någon annan Microsoft-tjänst för att slutföra registreringen. Om du inte vet vad det är kontaktar du din IT-administratör. Om du fortfarande inte kan registrera och är villig att slutföra en mer avancerad installationsprocess, kan du registrera dig för en ny Office 365 provprenumeration och använda den e-postadressen till att registrera dig. |

## <a name="see-also"></a>Se även
[Välkommen till [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](index.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


