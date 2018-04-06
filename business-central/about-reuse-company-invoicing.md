---
title: "Använd Invoicing och Business Central | Microsoft Docs"
description: "Lösning för att komma åt Microsoft Invoicing när du har registrerat dig för Dynamics 365 Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7c23fdd29b8fa4da0d5eb4d86e244bd847e9e9fb
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a>Använda samma Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] och Microsoft Invoicing
När du registrerar dig för en provversion av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du byta till en 30 dagar lång utvärderingsfas, starta en prenumeration eller sluta använda [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om du loggar in i Office-portalen kommer du i samtliga fall att se en flik som heter **Business center** och klicka på den. Detta ingår i Office 365 Business Premium-prenumerationen, så det är inte alla som får se fliken i Office-Portalen.  

Om du öppnar Business center visas avsnittet **Invoicing**. Om du öppnar detta avsnitt visas ett meddelande om att du inte har åtkomst till Microsoft Invoicing eftersom ditt konto används i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Ett liknande meddelande visas om du installerar det mobila programmet för Invoicing.  

## <a name="workaround"></a>Lösning
Invoicing och [!INCLUDE[d365fin](includes/d365fin_md.md)] har en delad plattform. Det innebär att du identifieras som en befintlig användare i [!INCLUDE[d365fin](includes/d365fin_md.md)] när du klickar på Invoicing i Business center. Det beror på att Invoicing inte kan använda samma företag som [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Du måste därför logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] och döpa om ditt befintliga företag och sedan skapa ett nytt företag som du kan använda i Invoicing. Inga data flyttas eller skrivs över i samband med denna lösning.

### <a name="to-rename-your-company"></a>Byta namn på ditt företag
1.  Logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Företag** och välj sedan relaterad länk.  
3.  I fönstret **Företag** väljer du knappen **Redigera lista**.  
4.  Byt namn på posten *Mitt företag* till något annat.  

    Vänta några minuter. Vi kommer att genomföra ett antal ändringar i den underliggande databasen, och det tar ett tag.
5.  När systemet är redo igen väljer du knappen **Skapa nytt företag**.  
6.  I dialogrutan som visas anger du namnet som *Mitt företag* och väljer sedan alternativet **Produktion – endast konfigurationsdata**.  

Detta tar återigen några minuter. När processen är klar kommer du att få åtkomst till Invoicing som en del av din Office 365 Business Premium-upplevelse.  

### <a name="what-about-my-data"></a>Om mina data
När du byter namn på det ursprungliga Mitt företag döps de databastabeller som lagrar dina befintliga [!INCLUDE[d365fin](includes/d365fin_md.md)]-data om, men själva informationen ändras inte.  

Om du använder såväl Invoicing som [!INCLUDE[d365fin](includes/d365fin_md.md)] lagras datan i två olika behållare (de två företagen). Inget delas, så du måste hantera kunder och artiklar i båda företagen.  

## <a name="see-also"></a>Se även
[Vanliga frågor och svar](across-faq.md)  
[Installation och administration](admin-setup-and-administration.md)  

