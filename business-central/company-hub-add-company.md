---
title: Lägg till företag till företagsnavet
description: Lär dig mer om hur du lägger till företag från andra Business Central-miljöer till företagsnavet så att du kan hantera arbete i olika miljöer.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: accountant, accounting, company hub
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4954287f93ed012709a51f6fbb19d00494c63d54
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436982"
---
# <a name="add-companies-to-your-company-hub"></a>Lägg till företag till företagsnavet

Med företagsnavet kan du komma åt ditt arbete från flera företag från flera olika [!INCLUDE [prod_short](includes/prod_short.md)]-miljöer. Du kan lägga till en eller flera miljöer manuellt, om företagen inte visas automatiskt i företagsnavet.  

På företagsnavets landningssida hittar du menyn **Konfigurera**, från vilken du kan öppna sidan **Miljölänkar**. Välj bara **Ny** och fyll sedan i relevanta fält. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

> [!NOTE]
> Du kan ansluta företagets nav till så många företag som behövs. Du kan emellertid bara ansluta företagsnavet till företag som finns i [!INCLUDE [prod_short](includes/prod_short.md)] online.

## <a name="environment-links"></a>Miljölänkar

En miljölänk är ett kort där du anger [!INCLUDE [prod_short](includes/prod_short.md)]-miljön som är värd för ett eller flera företag som du arbetar i. Datan i ett kort för varje miljö som anges av dig och du kan ändra den efter behov. Men fältet **Miljölänk** är kritiskt – detta är hur du får tillgång till varje företag i [!INCLUDE [prod_short](includes/prod_short.md)]. Använd åtgärden **Testa anslutningen** i menyfliksområdet för att kontrollera att du har angett rätt länk. Länken som du måste ange pekar mot miljön som är värd för det företag som du lägger till, och måste ta med ID-numret för Azure Active Directory (Azure AD) eller organisationens domännamn. Till exempel om de har angett en domän, till exempel MyBusiness.com, är länken till [!INCLUDE [prod_short](includes/prod_short.md)] ```https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1```. Annars ser det ut ungefär så här: ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```  

Länken används när du väljer företag i företagsnavet.  

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Åtgärder för ett företag som anges i företagsnavet.":::

> [!TIP]
> Om du arbetar i en kostnadsfri testversion av [!INCLUDE [prod_short](includes/prod_short.md)] är det enkelt att lägga till företagen i din klientorganisation. Du hittar miljölänken genom att kopiera ID för Azure Active Directory från avsnittet **Felsökning** på sidan Hjälp och support. Miljönamnet är troligen standardvärdet, PRODUKTION. Lägg till den här informationen i fältet **Miljölänk**, till exempel ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```, och välj sedan **Testa anslutningen**. Utvärderingsföretaget läggs till i listan.
>
> Om du har flyttat till företaget med trettio dagars testversion, Mitt företag, kan du lägga till det i listan genom att välja åtgärden **Läs in igen/Läs in alla företag igen** i listan.

## <a name="load-companies"></a>Läs in företag

När du har lagt till dina miljöer visas företagen automatiskt. Om du vet att ett nytt företag har lagts till i en miljö kan du emellertid välja åtgärden **Läs in alla företag igen** för att uppdatera listan. Använd samma åtgärd för att uppdatera data från alla dina företag.  

> [!TIP]
> För att du ska kunna uppdatera informationen i företagsnavet måste du ha tillgång till data i de företag som data kommer från.

## <a name="see-also"></a>Se även

[Hantera arbete i flera företag med företagsnavet](company-hub.md)  
[Resurser för hjälp och support](product-help-and-support.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]