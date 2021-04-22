---
title: Hantera användarinställningar och inställningar som administratör
description: Hantera användarinställningar och inställningar i Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 04/01/2021
ms.author: soalex
ms.openlocfilehash: 36850a2d0d8f85a0436b5d268c3cd2653b2f785f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779763"
---
# <a name="manage-user-settings-and-preferences"></a>Hantera användarinställningar och inställningar

Som administratör kan du konfigurera användarinställningar i [!INCLUDE[prod_short](includes/prod_short.md)] på samma sätt som enskilda användare kan hantera egna inställningar på sidan **Mina inställningar**.  

Få en översikt över alla användare i listan **Användare** och ändra enskilda inställningar genom att välja åtgärden **Användarinställningar** för den relevanta användaren.

> [!TIP]
> Listan **Användarinställningar** visar de aktuella inställningarna för varje användare. Om du vill visa eller redigera enskilda användare väljer du åtgärden **Visa** eller **Redigera**.

Sidan **Kort för användarinställningar** liknar sidan **Mina inställningar** som varje användare har åtkomst till, och det är ett kraftfullt verktyg för dig som administratör för att ställa in standardinställningar och rensa anpassade sidor, till exempel.  

## <a name="types-of-user-settings"></a>Typer av användarinställningar

*Användarinställningar* är inte samma sak som *Användarinställningar*, som är om användaren som en enhet och användarens behörighet i systemet. Dessutom har användarinställningarna ingenting med användarens anpassning att göra, t. ex. lätta ändringar i användargränssnittet. Användarinställningar bestämmer de fördefinierade inställningarna för varje användare i olika delar av hur programmet visar sig för användaren. I följande stycke visas de fem olika typerna av användarinställningar och inställningar som kan anges av administratören:

- **Företag**  

  Den här inställningen anger vilket företag som ska loggas in vid nästa inloggning. En användare kan ha åtkomst till flera företag och kan vara aktiv i flera företag.

- **Roll**  

  Rollen eller profilen beskriver användarens funktion i företaget, till exempel *säljchef*, *bokföringsansvarig* eller *inköpsagent*. Profilen bestämmer sedan användarens rollcenter, den startsida som användarna kommer att se när de loggar in. Profilen påverkar inte åtkomsträttigheterna till funktionaliteten i [!INCLUDE[prod_short](includes/prod_short.md)].  

- **Språk**  

  Definierar det programspråk som [!INCLUDE[prod_short](includes/prod_short.md)] visar text, beskrivningar och felmeddelanden i. Om [!INCLUDE[prod_short](includes/prod_short.md)]-användarna synkroniseras från Microsoft 365 används språkinställningarna från Microsoft 365, förutsatt att användaren vill använda samma inställningar i Office-produkter och [!INCLUDE[prod_short](includes/prod_short.md)]. Administratören kan ändra standardinställningen och varje användare kan välja mellan tillgängliga språk på sidan Mina inställningar. Men de återställs till värdet från Microsoft 365 när nästa synkronisering har utförts.

  Om språkinställningen från Microsoft 365 motsvarar ett språk som stöds i [!INCLUDE[prod_short](includes/prod_short.md)] kommer det här språket att väljas för användaren.  

  > [!NOTE]
  > Du kanske måste installera ett språkprogram för [!INCLUDE[prod_short](includes/prod_short.md)] för att språket ska kunna visas på rätt sätt. Därför bör du installera de språkprogram som behövs innan användarna loggar in första gången så att de får en bra erfarenhet från den första dagen. Mer information finns i listan över [språk som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
- **Region**  

  Definierar hur datum och nummer visas på [!INCLUDE[prod_short](includes/prod_short.md)] klienten, t. ex. om du vill använda europeiska eller amerikanska datumformat, eller hur du vill visa decimaltecknet och tusenavgränsare i belopp. Om [!INCLUDE[prod_short](includes/prod_short.md)]-användarna synkroniseras från Microsoft 365 används de nationella inställningarna från Microsoft 365, förutsatt att användaren vill använda samma inställningar i Office-produkter och [!INCLUDE[prod_short](includes/prod_short.md)]. En administratör eller användare kan ändra inställningarna manuellt i [!INCLUDE[prod_short](includes/prod_short.md)], men de återställs till ett värde från Microsoft 365 när nästa synkronisering utförs.

- **Tidszon**  

  Definierar den tidszon i vilken användaren befinner sig. Detta är för närvarande inte synkroniserat från Microsoft 365 och måste anges manuellt.  

- **Undervisningstips**

  [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]Som administratör kan du stänga av undervisningstips för alla användare, till exempel om du håller på att registrera användare som redan är bekanta med [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Om en Microsoft 365-användarsynkronisering görs medan användarna är inloggade på [!INCLUDE[prod_short](includes/prod_short.md)] måste dessa användare uppdatera webbläsaren eller logga ut och sedan in igen på [!INCLUDE[prod_short](includes/prod_short.md)] för att kunna se ett annat språk som anges av synkroniseringsåtgärden.

## <a name="overview-of-all-user-specific-changes"></a>Översikt över alla användarspecifika ändringar

Som administratör kan du få en översikt över enskilda ändringar till [!INCLUDE [prod_short](includes/prod_short.md)] varje användare kan ha gjort på olika sidor i [!INCLUDE [prod_short](includes/prod_short.md)]. När användare gör ändringar i sin upplevelse i [!INCLUDE [prod_short](includes/prod_short.md)] dessa förändringar kommer att återspeglas i listan **Användaranpassningar**. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## <a name="to-review-or-delete-user-personalizations"></a>Så här granskar eller tar du bort användaranpassningar

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **Anpassade sidor** och välj sedan relaterad länk.
2. Visar en lista över användare och deras anpassade sidor. Om du vill ta bort en användares anpassning klickar du på relevant rad eller väljer **Hantera** och väljer sedan **Ta bort**.

Detta tar bort anpassningen och användarens upplevelse av den relevanta sidan återgår till standardtillståndet.

## <a name="see-also"></a>Se även

[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Tillgänglighet för land/region och språk som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Byta språk och plats](about-locale-language.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
