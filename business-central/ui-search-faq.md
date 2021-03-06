---
title: Vanliga frågor och svar om Berätta | Microsoft Docs
description: Den här artikeln innehåller svar på frågor från våra partners och kunder som ofta frågar om Berätta.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 85b1f4f0b677baa5ca8a522acb1b383689f72e9e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783215"
---
# <a name="tell-me-faq"></a>Vanliga frågor om Berätta
I det här avsnittet besvaras frågor som våra erfarna användare ofta frågar om funktionen berätta för mig.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Är alla åtgärder från den aktuella sidan synliga i Berätta?
Nej. Åtgärder i delar, till exempel Försäljningsraddelar eller faktaboxar, visas inte vet i Berätta.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Filtreras resultaten i Berätta efter behörigheter?
Om användaren inte har AccessByPermissions visas inte åtgärder. Sidor och rapporter visas däremot i sökresultaten men kräver att användaren har behörighet att komma åt dem. Ett meddelande visas om användaren inte har behörighet att visa objektet.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Visar Berätta innehåll från mina anpassningar eller installerat tillägg från tredje parter?
Åtgärder, sidor och rapporter som kommer från tillägg tas upp av Berätta, med anpassad hjälpdokumentation gör inte det. Teknisk information om hur du gör egna sidor och rapporter synliga kan finns i [Lägga lägga till sidor och rapporter till Sökning](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Vad gör att detta skiljer sig från vad som tidigare var känt som Sidsökning?
Sidsökning har utvecklats till Berätta för att hjälpa dig att få jobbet gjort fortare. Sidsökning kan bara hjälpa dig att navigera till sidor och rapporter. På teknisk nivå baseras Berätta inte längre på äldre MenuSuite-begrepp.

### <a name="i-use-on-premises-prod_short-does-that-include-tell-me"></a>Du kan använda lokal [!INCLUDE[prod_short](includes/prod_short.md)]. Omfattar detta Berätta?
Du kan använda Berätta i den lokala webbklienten för att hitta åtgärder, sidor och rapporter, men inte dokumentation eller appar och konsulttjänster i AppSource.

### <a name="is-tell-me-available-for-all-form-factors"></a>Är Berätta tillgänglig för alla formfaktorer?
Berätta finns bara i webbklienten eller Windows-skrivbordsapp.

### <a name="are-the-documentation-results-available-in-any-language"></a>Är dokumentationsresultatet på ett annat språk?
Hjälpartiklarna visas på det språk som du har angett i **Mina inställningar**, om det finns hjälp på det språket.

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Varför visas inte en bokmärkesikon för mina sökresultat?
Ikonen för bokmärket visas inte i fönstret berätta för mig när anpassningar inaktiveras för en användarroll.


## <a name="see-also"></a>Se även  
[Spara och anpassa listvyer](ui-views.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Söka efter sidor med rollutforskaren](ui-role-explorer.md)  
[Förse en sida eller rapport med ett bokmärke på ditt rollcenter](ui-bookmarks.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]