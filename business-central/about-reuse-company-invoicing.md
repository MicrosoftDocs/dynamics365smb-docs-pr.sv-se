---
title: Använd Invoicing och Business Central | Microsoft Docs
description: Lösning för att komma åt Microsoft Invoicing när du har registrerat dig för Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: b04da7a7fa6d831646c6af9f0606afa90dc00bd6
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188858"
---
# <a name="using-the-same-office-365-account-in-d365fin-and-microsoft-invoicing"></a>Använda samma Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] och Microsoft Invoicing
När du registrerar dig för en provversion av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du byta till en 30 dagar lång utvärderingsfas, starta en prenumeration eller sluta använda [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om du loggar in i Office-portalen kommer du i samtliga fall att se en flik som heter **Microsoft Invoicing** och klicka på den. Detta ingår i Office 365 Business Premium-prenumerationen, så det är inte alla som får se fliken i Office-Portalen.  

Om du öppnar Microsoft Invoicing visas ett meddelande om att du inte har åtkomst till Microsoft Invoicing eftersom ditt konto används i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Ett liknande meddelande visas om du installerar det mobila programmet för Invoicing.  

## <a name="workaround"></a>Lösning
Invoicing och [!INCLUDE[d365fin](includes/d365fin_md.md)] har en delad plattform. Det innebär att du identifieras som en befintlig användare i [!INCLUDE[d365fin](includes/d365fin_md.md)] när du klickar på Fakturering i Office-portalen. Det beror på att Invoicing inte kan använda samma företag som [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Du måste därför logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] och döpa om ditt befintliga företag och sedan skapa ett nytt företag som du kan använda i Fakturering. Inga data flyttas eller skrivs över i samband med denna lösning.

### <a name="to-rename-your-company"></a>Byta namn på ditt företag
1. Logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. I det övre högra hörnet väljer du ikonen **Inställningar** ![Inställningar](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och sedan **Mina inställningar**.
3. I fältet **företag** väljer du ett annat företag.
4. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Företag** och välj sedan tillhörande länk.  
5. På sidan **Företag** väljer du knappen **Redigera lista**.  
6. Byt namn på posten *Mitt företag* till något annat.  

    Vänta några minuter. Vi kommer att genomföra ett antal ändringar i den underliggande databasen, och det tar ett tag.
7.  När systemet är redo igen väljer du knappen **Skapa nytt företag**.  
8.  I dialogrutan som visas anger du namnet som *Mitt företag* och väljer sedan alternativet **Produktion – endast konfigurationsdata**.  

Detta tar återigen några minuter. När processen är klar kommer du att få åtkomst till Invoicing som en del av din Office 365 Business Premium-upplevelse.  

### <a name="what-about-my-data"></a>Om mina data
När du byter namn på det ursprungliga Mitt företag döps de databastabeller som lagrar dina befintliga [!INCLUDE[d365fin](includes/d365fin_md.md)]-data om, men själva informationen ändras inte.  

Om du använder såväl Invoicing som [!INCLUDE[d365fin](includes/d365fin_md.md)] lagras datan i två olika behållare (de två företagen). Inget delas, så du måste hantera kunder och artiklar i båda företagen.  

## <a name="see-also"></a>Se även
[Vanliga frågor och svar](across-faq.md)  
[Administration](admin-setup-and-administration.md)  
