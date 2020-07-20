---
title: Hantera användarinställningar och inställningar i Dynamics 365 Business Central
description: Hantera användarinställningar och inställningar i Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 06/17/2020
ms.author: soalex
ms.openlocfilehash: 633a0872a878843f26d627dcd76e69d1c851ef8a
ms.sourcegitcommit: 3945f16d6d9c9853651e6291ce1465a44fd71fc8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/17/2020
ms.locfileid: "3460426"
---
# <a name="manage-user-settings-and-preferences"></a>Hantera användarinställningar och inställningar

Som administratör kan du ange användarinställningar i [!INCLUDE[d365fin](includes/d365fin_md.md)] på samma sätt som enskilda användare kan hantera egna inställningar på sidan **Mina inställningar**.  

## <a name="types-of-user-settings"></a>Typer av användarinställningar

*Användarinställningar* är inte samma sak som *Användarinställningar*, som är om användaren som en enhet och användarens behörighet i systemet. Dessutom har användarinställningarna ingenting med användarens anpassning att göra, t.ex. lätta ändringar i användargränssnittet. Användarinställningarna bestämmer användarens inställningar i olika delar av hur programmet visar sig för användaren. I följande stycke visas de fem olika typerna av användarinställningar och inställningar som kan anges av administratören:

- **Företag**  

  Den här inställningen anger vilket företag som ska loggas in vid nästa inloggning. En användare kan ha åtkomst till flera företag och kan vara aktiv i flera företag.

- **Profil (roller)**  

  Profilen beskriver användarens funktion i företaget, till exempel *säljchef*, *bokföringsansvarig* eller *inköpsagent*. Profilen bestämmer sedan användarens rollcenter, den startsida som användarna kommer att se när de loggar in. Profilen påverkar inte åtkomsträttigheterna till funktionaliteten i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

- **Språk-ID (nationella inställningar)**  

  Definierar hur datum och nummer visas på [!INCLUDE[d365fin](includes/d365fin_md.md)] klienten, t.ex. om du vill använda europeiska eller amerikanska datumformat, eller hur du vill visa decimaltecknet och tusenavgränsare i belopp. Om [!INCLUDE[d365fin](includes/d365fin_md.md)] användarna synkroniseras från Office 365 används de nationella inställningarna från Office 365, förutsatt att användaren vill använda samma inställningar i Office-produkter och [!INCLUDE[d365fin](includes/d365fin_md.md)]. En administratör eller användare kan ändra inställningarna manuellt i [!INCLUDE[d365fin](includes/d365fin_md.md)], men de återställs till ett värde från Office 365 när nästa synkronisering utförs.

- **Språk**  

  Definierar det programspråk som [!INCLUDE[d365fin](includes/d365fin_md.md)] visar text, beskrivningar och felmeddelanden i. Om [!INCLUDE[d365fin](includes/d365fin_md.md)] användarna synkroniseras från Office 365 används språkinställningarna från Office 365, förutsatt att användaren vill använda samma inställningar i Office-produkter och [!INCLUDE[d365fin](includes/d365fin_md.md)]. En administratör eller användare kan ändra inställningarna manuellt i [!INCLUDE[d365fin](includes/d365fin_md.md)], men de återställs till ett värde från Office 365 när nästa synkronisering utförs.

  Om språkinställningen från Office 365 motsvarar ett språk som stöds i [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer det här språket att väljas för användaren.  

  > [!NOTE]
  > Du kanske måste installera ett språkprogram för [!INCLUDE[d365fin](includes/d365fin_md.md)] för att språket ska kunna visas på rätt sätt. Därför bör du installera de språkprogram som behövs innan användarna loggar in första gången så att de får en bra erfarenhet från den första dagen. Mer information finns i listan över [språk som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
- **Tidszon**  

  Definierar den tidszon i vilken användaren befinner sig. Detta är för närvarande inte synkroniserat från Office 365 och måste anges manuellt.  

> [!NOTE]
> Om en Office 365 användarsynkronisering görs medan användarna är inloggade [!INCLUDE[d365fin](includes/d365fin_md.md)] måste dessa användare uppdatera webbläsaren eller logga ut och sedan in igen för [!INCLUDE[d365fin](includes/d365fin_md.md)] att kunna se ett annat språk som anges av synkroniseringsåtgärden.

## <a name="overview-of-all-user-settings"></a>Översikt över alla användarinställningar

Administratörer har möjlighet att ange eller ändra dessa inställningar för användare i respektive företag. Det gör du på sidan **användaranpassning**. Posterna på den här sidan återspeglar den enskilda användarens val för ovanstående inställningar, en post per användare. När användarna ändrar sina inställningar på sidan **Mina inställningar** dessa ändringar i listan **Användaranpassningar**. Administratörer kan också ange de här inställningarna för användarna innan de loggar in första gången, så att användarna inte behöver göra det själva, så att de får en bättre *Start*-upplevelse.

> [!NOTE]
> Användaranpassningar har inget att göra med de *personliga* lätta ändringarna som användaren kan göra i användargränssnittet.

## <a name="to-review-or-make-changes-to-user-settings"></a>Så här granskar eller ändrar du användarinställningar

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **användaranpassning** och välj sedan relaterad länk.
2. Visar en lista över användare och deras inställningar. Om du vill ändra en användares inställningar klickar du på **användar-ID** eller väljer **hantera** och **redigera**.
3. Kortet **användaranpassning** för den specifika användarens inställningar visas och du kan göra önskade ändringar.  

## <a name="see-also"></a>Se även

[Komma igång](product-get-started.md)  
[Tillgänglighet för land/region och språk som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Byta språk och plats](about-locale-language.md)  
