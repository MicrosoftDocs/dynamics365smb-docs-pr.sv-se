---
title: Vanliga frågor om Berätta
description: Den här artikeln innehåller svar på frågor från våra partners och kunder som ofta frågar om Berätta.
author: brentholtorf
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'find, search, Tell Me'
ms.search.form: TellMe
ms.date: 03/20/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---
# <a name="tell-me-faq"></a>Vanliga frågor om Berätta

I det här avsnittet besvaras frågor som våra erfarna användare ofta frågar om funktionen Berätta vad du vill göra.

## <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Är alla åtgärder från den aktuella sidan synliga i Berätta?

Nej. Delåtgärder, till exempel Försäljningsraddelar eller faktaboxar, visas inte i Berätta.

## <a name="can-i-search-for-a-specific-record"></a>Kan jag söka efter en specifik post?

Ja. Om du till exempel snabbt vill hitta en försäljningsorder anger du dess identifierare och väljer sedan **Sök i företagsdata**. Om du bara känner till kundens namn anger du detta. Funktionen Berätta ordnar resultaten efter typ så att du kan hitta ordern under kategorin Försäljningsorder.

## <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Filtreras resultaten i Berätta efter behörigheter?

Om användaren inte har AccessByPermissions visas inte åtgärder. Sidor och rapporter visas däremot i sökresultaten men kräver att användaren har behörighet att komma åt dem. Ett meddelande visas om användaren inte har behörighet att visa objektet.

## <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Visar Berätta innehåll från mina anpassningar eller installerat tillägg från tredje parter?

Åtgärder, sidor och rapporter som kommer från tillägg tas upp av Berätta. Teknisk information om hur du gör egna sidor och rapporter synliga kan finns i [Lägga lägga till sidor och rapporter till Sökning](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

## <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Vad gör att detta skiljer sig från vad som tidigare var känt som Sidsökning?

Sidsökning har utvecklats till Berätta för att hjälpa dig att få projektet gjort fortare. Sidsökning kan bara hjälpa dig att navigera till sidor och rapporter. På teknisk nivå baseras Berätta inte längre på äldre MenuSuite-begrepp.

## <a name="i-use-on-premises--does-that-include-tell-me"></a>Du kan använda lokal [!INCLUDE[prod_short](includes/prod_short.md)]. Omfattar detta Berätta?

Du kan använda Berätta i den lokala webbklienten för att hitta åtgärder, sidor och rapporter, men inte appar och konsulttjänster i AppSource.

## <a name="is-tell-me-available-for-all-form-factors"></a>Är Berätta tillgänglig för alla formfaktorer?

Ja. Den introducerades på telefoner och surfplattor i Business Central 2023 utgivningscykel 2. I 2023 utgivningscykel 2, it måste det aktiveras i [Funktionshantering](/dynamics365/business-central/dev-itpro/administration/feature-management) med hjälp av reglaget **Funktion: Sök efter sidor och data i mobilappen**. I 2024 utgivningscykel 1 och senare är det alltid aktiverat.

<!-- removed in v20 because of Help pane
### <a name="are-the-documentation-results-available-in-any-language"></a>Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

## <a name="does-tell-me-give-me-help-on-how-to-use-pages-reports-and-other-things"></a>Kan jag få hjälp med att använda sidor, rapporter och andra saker?

Nej, men det är lätt att komma åt informationen från Hjälp fönstret. Välj bara åtgärden **Sök i hjälpen** på sidan **Berätta vad du vill göra** eller välj <kbd>Ctrl</kbd>+<kbd>F1</kbd> på tangentbordet. Om du vill veta mer om rutan Hjälp går du till [rutan Hjälp](product-help-and-support.md#help-pane).

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Varför visas inte en bokmärkesikon för mina sökresultat?

Ikonen för bokmärket visas inte i fönstret Berätta när anpassningar inaktiveras för en användarroll.

## <a name="see-also"></a>Se även

[Spara och anpassa listvyer](ui-views.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Söka efter sidor med rollutforskaren](ui-role-explorer.md)  
[Förse en sida eller rapport med ett bokmärke på ditt rollcenter](ui-bookmarks.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
