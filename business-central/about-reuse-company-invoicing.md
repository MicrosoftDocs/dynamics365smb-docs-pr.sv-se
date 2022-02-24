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
ms.date: 04/30/2020
ms.author: bholtorf
ms.openlocfilehash: 7776cd01218f5959734173226574bb4a0d043153
ms.sourcegitcommit: 866f0e6ed9df3397072b9df838e31c3a1f4b626d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/05/2020
ms.locfileid: "3333866"
---
# <a name="using-the-same-office-365-account-in-d365fin-and-microsoft-invoicing"></a>Använda samma Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] och Microsoft Invoicing
När du registrerar dig för en provversion av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du byta till en 30 dagar lång utvärderingsfas, starta en prenumeration eller sluta använda [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ibland kan det hända att du har sett något som kallas **Microsoft Invoicing** och klickat på den. Det här var en app som ingick i Microsoft 365 Business Standard och tidigare kallades för Office 365 Business Premium-prenumeration, så det är inte alla som har sett den panelen i sin Office 365-erfarenhet.  

Microsoft Invoicing är inte längre tillgängligt, men om du behöver logga in på fakturering för att hämta data kanske du får ett meddelande om att du inte kan komma åt Microsoft Invoicing eftersom ditt konto används i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Ett liknande meddelande visas om du installerar det mobila programmet för Invoicing.  

## <a name="workaround"></a>Lösning
Invoicing och [!INCLUDE[d365fin](includes/d365fin_md.md)] har en delad plattform. Det innebär att du identifieras som en befintlig användare i [!INCLUDE[d365fin](includes/d365fin_md.md)] när du klickar på fakturering i Microsoft 365 administratörscenter. Det beror på att Invoicing inte kan använda samma företag som [!INCLUDE[d365fin](includes/d365fin_md.md)].  

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

Detta tar återigen några minuter. När processen är klar kommer du att få åtkomst till Invoicing som en del av din Microsoft 365 Business Standard-upplevelse. Men endast för export av data eftersom faktureringsprogrammet är föråldrat.  

### <a name="what-about-my-data"></a>Om mina data
När du byter namn på det ursprungliga Mitt företag döps de databastabeller som lagrar dina befintliga [!INCLUDE[d365fin](includes/d365fin_md.md)]-data om, men själva informationen ändras inte.  

Om du använder såväl Invoicing som [!INCLUDE[d365fin](includes/d365fin_md.md)] lagras datan i två olika behållare (de två företagen). Inget delas, så du måste hantera kunder och artiklar i båda företagen.  

## <a name="see-also"></a>Se även
[Vanliga frågor och svar](across-faq.md)  
[Administration](admin-setup-and-administration.md)  
