---
title: Dela kontakter mellan Business Central och Outlook
description: Denna tjänst har djupgående integrering med Microsoft 365 så att du kan dela kontakter mellan Outlook och Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Microsoft 365
ms.search.form: 6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 12ce99a79f465543ecc314b5042e70b6802f86ec
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8142425"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synkronisera kontakter i Business Central med kontakter i Microsoft Outlook

Du kan visa samma kontakter i [!INCLUDE[prod_short](includes/prod_short.md)] som visas i Outlook om du ställer in synkronisering av kontakter. Till exempel om du är en säljare kan du göra vissa av ändringar i Outlook och en del av arbetet i [!INCLUDE[prod_short](includes/prod_short.md)]. Om kontakterna är desamma på båda platser, är ditt arbete enklare.  

En dedikerad mapp i Outlook gör det enklare att hitta och du kan ange ett filter för att endast synkronisera kontakter från [!INCLUDE[prod_short](includes/prod_short.md)] som du vill se i Outlook. När kontaktsynkroniseringen har konfigurerats, kan du starta synkroniseringen manuellt eller ställa in en automatisk synkronisering som synkroniserar kontakterna enligt ett schema.  

## <a name="set-up-synchronization"></a>Konfigurera synkronisering
Du kan ange hur du vill synkronisera kontakter med Outlook på sidan **Konfigurering av Exchange-synkronisering** i [!INCLUDE[prod_short](includes/prod_short.md)]. En förutsättning är att din användarprofil i [!INCLUDE[prod_short](includes/prod_short.md)] måste ange ditt e-postkonto för Microsoft 365. Du kan kontrollera detta i avsnittet **Microsoft 365-autentisering** i din användarprofil i listan **Användare**.  

Sedan på sidan **Konfigurering av Exchange-synkronisering** kan du verifiera att anslutningen till Exchange fungerar och sedan skapa synkroniseringen av kontakter. Öppna sidan **Inställningar för kontaktsynkning** och starta synkroniseringen. Du kan även definiera ett filter för vilka kontakter som ska synkroniseras mellan [!INCLUDE[prod_short](includes/prod_short.md)] och Outlook. Till exempel kan du registrera ett filter i namn, typ, företag eller liknande. Du kan också ändra standardnamnet på mappen som kontakterna kommer att synkroniseras till i Outlook. Standardnamnet är *Business Central*.  

När synkroniseringen har ställts in, synkroniseras alla ändringar som du gör till kontakten i antingen Outlook eller i [!INCLUDE[prod_short](includes/prod_short.md)] till den andra.  

Var och en av dina medarbetare kan också ställa in sin egna Exchange-synkronisering och registrera egna filter på vilka kontakter som ska synkroniseras.  

## <a name="synchronize-contacts"></a>Synkronisera kontakter
Om du vill arbeta med kontakter i [!INCLUDE[prod_short](includes/prod_short.md)], och du sedan tycker att det är lätt att starta synkroniseringen manuellt när det passar dig från listan **kontakter**. Välj bara åtgärden **Synkronisera med Microsoft 365** och bestäm sedan om du vill ändra det filter som du har lagt upp. När du väljer OK kommer synkroniseringen att startas omedelbart och de senaste ändringarna tillämpas på dina kontakter i Outlook.  

I listan **kontakter**, kan du synkronisera kontakterna på två sätt:

* **Synka med Microsoft 365**

  Denna åtgärd synkroniserar alla ändringar från [!INCLUDE[prod_short](includes/prod_short.md)] till Microsoft 365 sedan föregående synkronisering, baserat på senaste ändringsdatum. Inga nya kontakter från Microsoft 365 synkroniseras tillbaka till [!INCLUDE[prod_short](includes/prod_short.md)] också. Detta är vanligtvis snabbare än att göra en fullständig synkronisering.  

* **Full synkronisering med Microsoft 365**

  Denna åtgärd synkroniserar alla kontakter i båda riktningar oavsett senast synkroniserad och senast ändrades.  

I båda fallen synkroniseras bara kontakter från Outlook om de har alla nödvändiga fält ifyllda. De obligatoriska fälten för synkronisering med Microsoft 365 är **Namn**, **E-postadress** och de måste vara av typen Person. [!INCLUDE[prod_short](includes/prod_short.md)] är huvudkontaktinformation, så kontaktinformation i [!INCLUDE[prod_short](includes/prod_short.md)] kommer att sparas i händelse av kopior.  

I Outlook visas kontakter från [!INCLUDE[prod_short](includes/prod_short.md)] i en mapp under **andra kontakter** i vyn **användare**. Om du inte känner till vyn personer i Outlook får du den sedan i navigeringsalternativ längst ned till vänster i Outlook.  

## <a name="see-also"></a>Se även
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Ekonomi](finance.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Använda kontakter (personer) i Outlook på Internet](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]