---
title: Dela kontakter mellan Business Central och Outlook | Microsoft Docs
description: Denna tjänst har djupgående integrering med Office 365 så att du kan dela kontakter mellan Outlook och Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Office 365
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: f7cf42a003e68d68bf29a3623e9573f6e33eed4b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186626"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synkronisera kontakter i Business Central med kontakter i Microsoft Outlook
Du kan visa samma kontakter i [!INCLUDE[d365fin](includes/d365fin_md.md)] som visas i Outlook om du ställer in synkronisering av kontakter. Till exempel om du är en säljare kan du göra vissa av ändringar i Outlook och en del av arbetet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om kontakterna är desamma på båda platser, är ditt arbete enklare.  

En dedikerad mapp i Outlook gör det enklare att hitta och du kan ange ett filter för att endast synkronisera kontakter från [!INCLUDE[d365fin](includes/d365fin_md.md)] som du vill se i Outlook. När kontaktsynkroniseringen har konfigurerats, kan du starta synkroniseringen manuellt eller ställa in en automatisk synkronisering som synkroniserar kontakterna enligt ett schema.  

## <a name="set-up-synchronization"></a>Konfigurera synkronisering
Du kan ange hur du vill synkronisera kontakter med Outlook på sidan **Konfigurering av Exchange-synkronisering** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. En förutsättning är att din användarprofil i [!INCLUDE[d365fin](includes/d365fin_md.md)] måste ange ditt Office 365 e-postkonto. Du kan kontrollera detta avsnittet **Office 365-autentisering** i din användarprofil i listan **användare**.  

Sedan på sidan **Konfigurering av Exchange-synkronisering** kan du verifiera att anslutningen till Exchange fungerar och sedan skapa synkroniseringen av kontakter. Öppna sidan **Inställningar för kontaktsynkning** och starta synkroniseringen. Du kan även definiera ett filter för vilka kontakter som ska synkroniseras mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och Outlook. Till exempel kan du registrera ett filter i namn, typ, företag eller liknande. Du kan också ändra standardnamnet på mappen som kontakterna kommer att synkroniseras till i Outlook. Standardnamnet är *Business Central*.  

När synkroniseringen har ställts in, synkroniseras alla ändringar som du gör till kontakten i antingen Outlook eller i [!INCLUDE[d365fin](includes/d365fin_md.md)] till den andra.  

Var och en av dina medarbetare kan också ställa in sin egna Exchange-synkronisering och registrera egna filter på vilka kontakter som ska synkroniseras.  

## <a name="synchronize-contacts"></a>Synkronisera kontakter
Om du vill arbeta med kontakter i [!INCLUDE[d365fin](includes/d365fin_md.md)], och du sedan tycker att det är lätt att starta synkroniseringen manuellt när det passar dig från listan **kontakter**. Välj bara åtgärden **synkroniseras med Office 365** och bestäm sedan om du vill ändra det filter som du har lagt upp. När du väljer OK kommer synkroniseringen att startas omedelbart och de senaste ändringarna tillämpas på dina kontakter i Outlook.  

I listan **kontakter**, kan du synkronisera kontakterna på två sätt:

* **Synka med Office 365**

  Denna åtgärd synkroniserar alla ändringar från [!INCLUDE[d365fin](includes/d365fin_md.md)] till Office 365 efter att föregående synkronisering baserats på senast ändrade. Inga kontakter från Office 365 synkroniseras tillbaka till [!INCLUDE[d365fin](includes/d365fin_md.md)] också. Detta är vanligtvis snabbare än att göra en fullständig synkronisering.  

* **Full synkning med Office 365**

  Denna åtgärd synkroniserar alla kontakter i båda riktningar oavsett senast synkroniserad och senast ändrades.  

I båda fallen synkroniseras bara kontakter från Outlook om de har alla nödvändiga fält ifyllda. De obligatoriska fälten för synkronisering med Office 365 är **namn**, **e-postadress** och de måste vara av typen Person. [!INCLUDE[d365fin](includes/d365fin_md.md)] är huvudkontaktinformation, så kontaktinformation i [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer att sparas i händelse av kopior.  

I Outlook visas kontakter från [!INCLUDE[d365fin](includes/d365fin_md.md)] i en mapp under **andra kontakter** i vyn **användare**. Om du inte känner till vyn personer i Outlook får du den sedan i navigeringsalternativ längst ned till vänster i Outlook.  

## <a name="see-also"></a>Se även
[Komma igång](product-get-started.md)  
[Ekonomi](finance.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Använda kontakter (personer) i Outlook på Internet](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  
