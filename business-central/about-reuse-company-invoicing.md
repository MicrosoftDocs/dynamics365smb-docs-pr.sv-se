---
title: Använd fakturering och Business Central
description: Lösning för att komma åt Microsoft Invoicing när du har registrerat dig för Dynamics 365 Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Invoicing, Microsoft 365'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Använda samma Microsoft 365-konto i [!INCLUDE[prod_short](includes/prod_long.md)] och Microsoft Invoicing
När du registrerar dig för en testversion av [!INCLUDE[prod_short](includes/prod_short.md)] kan du byta till en 30 dagar lång utvärderingsfas, starta en prenumeration eller sluta använda [!INCLUDE[prod_short](includes/prod_short.md)]. Ibland kan det hända att du har sett något som kallas **Microsoft Invoicing** och klickat på den. Detta var en app som ingick i det som nu är Microsoft 365 Business Standard och tidigare kallades för Microsoft 365 Business Premium-prenumeration, så det är inte alla som har sett den panelen i sin Microsoft 365-upplevelse.  

Microsoft Invoicing är inte längre tillgängligt, men om du behöver logga in på fakturering för att hämta data kanske du får ett meddelande om att du inte kan komma åt Microsoft Invoicing eftersom ditt konto används i [!INCLUDE[prod_short](includes/prod_short.md)].  

Ett liknande meddelande visas om du installerar det mobila programmet för Invoicing.  

## Lösning
Invoicing och [!INCLUDE[prod_short](includes/prod_short.md)] har en delad plattform. Det innebär att du identifieras som en befintlig användare i [!INCLUDE[prod_short](includes/prod_short.md)] när du klickar på Fakturering i administrationscentret för Microsoft 365. Det beror på att Invoicing inte kan använda samma företag som [!INCLUDE[prod_short](includes/prod_short.md)].  

Du måste därför logga in på [!INCLUDE[prod_short](includes/prod_short.md)] och döpa om ditt befintliga företag och sedan skapa ett nytt företag som du kan använda i Fakturering. Inga data flyttas eller skrivs över i samband med denna lösning.

### Byta namn på ditt företag
1. Logga in på [!INCLUDE[prod_short](includes/prod_short.md)].
2. I det övre högra hörnet väljer du ikonen **Inställningar** ![Inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och sedan **Mina inställningar**.
3. I fältet **företag** väljer du ett annat företag.
4. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Företag** och väljer sedan relaterad länk.  
5. På sidan **Företag** väljer du knappen **Redigera lista**.  
6. Byt namn på posten *Mitt företag* till något annat.  

    Vänta några minuter. Vi kommer att genomföra ett antal ändringar i den underliggande databasen, och det tar ett tag.
7.  När systemet är redo igen väljer du knappen **Skapa nytt företag**.  
8.  I dialogrutan som visas anger du namnet som *Mitt företag* och väljer sedan alternativet **Produktion – endast konfigurationsdata**.  

Detta tar återigen några minuter. När processen är klar kommer du att få åtkomst till Fakturering som en del av din Microsoft 365 Business Standard-upplevelse. Men endast för export av data eftersom faktureringsprogrammet är föråldrat.  

### Om mina data
När du byter namn på det ursprungliga Mitt företag döps de databastabeller som lagrar dina befintliga [!INCLUDE[prod_short](includes/prod_short.md)]-data om, men själva informationen ändras inte.  

Om du använder såväl Invoicing som [!INCLUDE[prod_short](includes/prod_short.md)] lagras datan i två olika behållare (de två företagen). Inget delas, så du måste hantera kunder och artiklar i båda företagen.  

## Se även
[Vanliga frågor och svar](across-faq.yml)  
[Administration](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]